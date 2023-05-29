---
title: "DNS 개요"
icon: material/dns
description: DNS, 즉 도메인 네임 시스템은 '인터넷의 전화번호부'라고 할 수 있습니다. DNS가 있기 때문에 여러분은 브라우저에서 원하는 사이트를 찾아 연결할 수 있습니다.
---

[도메인 네임 시스템](https://ko.wikipedia.org/wiki/%EB%8F%84%EB%A9%94%EC%9D%B8_%EB%84%A4%EC%9E%84_%EC%8B%9C%EC%8A%A4%ED%85%9C)은 '인터넷의 전화번호부'라고 할 수 있습니다. DNS는 분산 서버 네트워크를 통해 도메인 이름을 IP 주소로 변환합니다. 브라우저 등의 서비스는 이를 이용해 인터넷 리소스를 로드할 수 있습니다.

## DNS란 무엇인가요?

사이트를 방문하면 숫자로 구성된 주소가 반환됩니다. 예를 들어, `privacyguides.org`를 방문할 경우에는 `192.98.54.105` 주소가 반환됩니다.

DNS는 [인터넷의 초창기](https://ko.wikipedia.org/wiki/%EB%8F%84%EB%A9%94%EC%9D%B8_%EB%84%A4%EC%9E%84_%EC%8B%9C%EC%8A%A4%ED%85%9C#%EC%97%AD%EC%82%AC)부터 존재해 왔습니다. DNS 서버와 주고받는 DNS 요청은 일반적으로 암호화가 적용되어 있지 **않습니다**. In a residential setting, a customer is given servers by the ISP via [DHCP](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol).

암호화되지 않은 DNS 요청은 전송 도중에 쉽게 **감시** 및 **변조**될 수 있습니다. 일부 지역에서는 ISP가 기초적인 [DNS 필터링](https://en.wikipedia.org/wiki/DNS_blocking)을 수행하도록 명령받기도 합니다. 이 경우, ISP가 차단하고 있는 도메인의 IP 주소를 요청하면 서버가 응답하지 않거나, 목적지가 아닌 다른 IP 주소로 응답이 돌아옵니다. As the DNS protocol is not encrypted, the ISP (or any network operator) can use [DPI](https://en.wikipedia.org/wiki/Deep_packet_inspection) to monitor requests. ISPs can also block requests based on common characteristics, regardless of which DNS server is used. Unencrypted DNS always uses [port](https://en.wikipedia.org/wiki/Port_(computer_networking)) 53 and always uses UDP.

Below, we discuss and provide a tutorial to prove what an outside observer may see using regular unencrypted DNS and [encrypted DNS](#what-is-encrypted-dns).

### 암호화되지 않은 DNS

1. [`tshark`](https://www.wireshark.org/docs/man-pages/tshark.html)를 이용하면 인터넷 패킷 흐름을 모니터링하고 기록할 수 있습니다(tshark는 [Wireshark](https://ko.wikipedia.org/wiki/%EC%99%80%EC%9D%B4%EC%96%B4%EC%83%A4%ED%81%AC) 프로젝트의 일부입니다). 다음 명령어는 명시된 규칙을 충족하는 패킷을 기록합니다.

    ```bash
    tshark -w /tmp/dns.pcap udp port 53 and host 1.1.1.1 or host 8.8.8.8
    ```

2. 이후 Linux, macOS 등에서는 [`dig`](https://en.wikipedia.org/wiki/Dig_(command)) 명령어를, Windows에서는 [`nslookup`](https://en.wikipedia.org/wiki/Nslookup) 명령어를 사용해 두 서버로 DNS 조회를 전송할 수 있습니다. 웹 브라우저 등의 소프트웨어는 암호화된 DNS를 사용하도록 설정된 경우가 아니라면 이러한 조회를 자동으로 수행합니다.

    === "Linux, macOS"

        ```
        dig +noall +answer privacyguides.org @1.1.1.1
        dig +noall +answer privacyguides.org @8.8.8.8
        ```
    === "Windows"

        ```
        nslookup privacyguides.org 1.1.1.1
        nslookup privacyguides.org 8.8.8.8
        ```

3. 이제 결과를 [분석](https://www.wireshark.org/docs/wsug_html_chunked/ChapterIntroduction.html#ChIntroWhatIs)합니다.

    === "Wireshark"

        ```
        wireshark -r /tmp/dns.pcap
        ```

    === "tshark"

        ```
        tshark -r /tmp/dns.pcap
        ```

앞선 과정을 거쳐 Wireshark 명령어를 실행하면 상단 창에 여러 [Frame](https://en.wikipedia.org/wiki/Ethernet_frame)이 표시되고, 하단 창에는 선택한 프레임에 대한 모든 데이터가 표시됩니다. 엔터프라이즈 필터링 및 모니터링 솔루션(정부에서 사용하는 솔루션 등을 말합니다)은 사람이 개입할 필요 없이 자동으로 이런 프로세스를 처리하고 집계하여 네트워크 관찰자에게 필요한 통계 데이터를 생성할 수 있습니다.

| 번호 | 소요 시간    | 출발지       | 목적지       | 프로토콜 | 길이  | 정보                                                                     |
| -- | -------- | --------- | --------- | ---- | --- | ---------------------------------------------------------------------- |
| 1  | 0.000000 | 192.0.2.1 | 1.1.1.1   | DNS  | 104 | Standard query 0x58ba A privacyguides.org OPT                          |
| 2  | 0.293395 | 1.1.1.1   | 192.0.2.1 | DNS  | 108 | Standard query response 0x58ba A privacyguides.org A 198.98.54.105 OPT |
| 3  | 1.682109 | 192.0.2.1 | 8.8.8.8   | DNS  | 104 | Standard query 0xf1a9 A privacyguides.org OPT                          |
| 4  | 2.154698 | 8.8.8.8   | 192.0.2.1 | DNS  | 108 | Standard query response 0xf1a9 A privacyguides.org A 198.98.54.105 OPT |

네트워크 관찰자는 이러한 패킷을 변조할 수 있습니다.

## '암호화된 DNS'란 무엇인가요?

'암호화 DNS'는 여러 프로토콜이 존재합니다. 일반적인 종류는 다음과 같습니다.

### DNSCrypt

[**DNSCrypt**](https://en.wikipedia.org/wiki/DNSCrypt)는 DNS 쿼리를 암호화하는 최초의 방법 중 하나였습니다. DNSCrypt는 443 포트에서 작동하며, TCP/UDP 전송 프로토콜 모두에서 작동합니다. DNSCrypt는 [국제 인터넷 표준화 기구(IETF)](https://ko.wikipedia.org/wiki/%EA%B5%AD%EC%A0%9C_%EC%9D%B8%ED%84%B0%EB%84%B7_%ED%91%9C%EC%A4%80%ED%99%94_%EA%B8%B0%EA%B5%AC)에 제출되지 않았고

RFC 절차를 거치지 않았기 때문에, [일부 구현체](https://dnscrypt.info/implementations)를 제외하고는 널리 사용되지 않았습니다. 결과적으로, 보다 널리 사용되는 [DNS over HTTPS](#dns-over-https-doh)로 대체되었습니다.</p> 



### DOT(DNS over TLS)

[**DNS over TLS**](https://en.wikipedia.org/wiki/DNS_over_TLS)는 DNS 통신을 암호화하는 또 다른 방법으로, [RFC 7858](https://datatracker.ietf.org/doc/html/rfc7858)에 정의되어 있습니다. Android 9, iOS 14, Linux([systemd-resolved](https://www.freedesktop.org/software/systemd/man/resolved.conf.html#DNSOverTLS=) 237 버전)에서 처음으로 지원되었습니다. DoT는 [복잡한 프로토콜](https://dnscrypt.info/faq/)인데다가 구현체마다 RFC 준수 여부가 다양하기 때문에, 최근 몇 년 동안은 업계 선호도가 DoT에서 DoH로 이동하고 있습니다. 또한, 853 포트를 전용으로 사용하기 때문에 제한적인 방화벽에 의해 쉽게 차단될 수 있다는 문제도 존재합니다.



### DoH(DNS over HTTPS)

[**DNS over HTTPS**](https://en.wikipedia.org/wiki/DNS_over_HTTPS)는 [RFC 8484](https://datatracker.ietf.org/doc/html/rfc8484)에 정의되어 있으며, 쿼리를 [HTTP/2](https://ko.wikipedia.org/wiki/HTTP/2) 프로토콜에 패키징하여 HTTPS를 통해 보안을 제공합니다. Firefox 60, Chrome 83과 같은 웹 브라우저에서 처음으로 지원되었습니다.

DoH 네이티브 구현은 iOS 14, macOS 11, Microsoft Windows, Android 13(단, [기본 활성화가 아닙니다](https://android-review.googlesource.com/c/platform/packages/modules/DnsResolver/+/1833144))부터 추가되었습니다. 일반 Linux 데스크톱의 경우, systemd [구현체](https://github.com/systemd/systemd/issues/8639)가 아직 존재하지 않기 때문에 [별도 소프트웨어를 설치해야 합니다](../dns.md#encrypted-dns-proxies).



## 외부 주체는 무엇을 볼 수 있나요?

다음 예시에서는 DoH 요청 시 실제로 어떤 일이 일어나는지 기록해보겠습니다.

1. 먼저 `tshark`를 실행합니다. 
   
   

    ```bash
    tshark -w /tmp/dns_doh.pcap -f "tcp port https and host 1.1.1.1"
    ```


2. 이후 `curl`를 이용해 요청을 생성합니다. 
   
   

    ```bash
    curl -vI --doh-url https://1.1.1.1/dns-query https://privacyguides.org
    ```


3. 요청 후 <kbd>CTRL</kbd> + <kbd>C</kbd>를 눌러 패킷 캡처를 중지합니다.

4. Wireshark에서 결과를 분석합니다. 
   
   

    ```bash
    wireshark -r /tmp/dns_doh.pcap
    ```


[연결 생성](https://ko.wikipedia.org/wiki/%EC%A0%84%EC%86%A1_%EC%A0%9C%EC%96%B4_%ED%94%84%EB%A1%9C%ED%86%A0%EC%BD%9C#%EC%97%B0%EA%B2%B0_%EC%83%9D%EC%84%B1) 및 [TLS 핸드셰이크](https://www.cloudflare.com/ko-kr/learning/ssl/what-happens-in-a-tls-handshake/)가 모든 암호화 연결에서 발생하는 것을 확인할 수 있습니다. 뒤따르는 'Application Data' 패킷을 살펴보면 요청했던 도메인이나 반환된 IP 주소가 포함되어 있지 않다는 것 또한 확인할 수 있습니다.



## 암호화 DNS를 사용하지 **말아야** 하는 이유는 무엇인가요?

In locations where there is internet filtering (or censorship), visiting forbidden resources may have its own consequences which you should consider in your [threat model](../basics/threat-modeling.md). We do **not** suggest the use of encrypted DNS for this purpose. Use [Tor](https://torproject.org) or a [VPN](../vpn.md) instead. If you're using a VPN, you should use your VPN's DNS servers. When using a VPN, you are already trusting them with all your network activity.

When we do a DNS lookup, it's generally because we want to access a resource. Below, we will discuss some of the methods that may disclose your browsing activities even when using encrypted DNS:



### IP 주소

The simplest way to determine browsing activity might be to look at the IP addresses your devices are accessing. For example, if the observer knows that `privacyguides.org` is at `198.98.54.105`, and your device is requesting data from `198.98.54.105`, there is a good chance you're visiting Privacy Guides.

This method is only useful when the IP address belongs to a server that only hosts few websites. It's also not very useful if the site is hosted on a shared platform (e.g. Github Pages, Cloudflare Pages, Netlify, WordPress, Blogger, etc.). It also isn't very useful if the server is hosted behind a [reverse proxy](https://en.wikipedia.org/wiki/Reverse_proxy), which is very common on the modern Internet.



### SNI(Server Name Indication)

Server Name Indication is typically used when a IP address hosts many websites. This could be a service like Cloudflare, or some other [Denial-of-service attack](https://en.wikipedia.org/wiki/Denial-of-service_attack) protection.

1. Start capturing again with `tshark`. We've added a filter with our IP address so you don't capture many packets: 
   
   

    ```bash
    tshark -w /tmp/pg.pcap port 443 and host 198.98.54.105
    ```


2. Then we visit [https://privacyguides.org](https://privacyguides.org).

3. After visiting the website, we want to stop the packet capture with <kbd>CTRL</kbd> + <kbd>C</kbd>.

4. Next we want to analyze the results: 
   
   

    ```bash
    wireshark -r /tmp/pg.pcap
    ```


We will see the connection establishment, followed by the TLS handshake for the Privacy Guides website. Around frame 5. you'll see a "Client Hello".

5. Expand the triangle &#9656; next to each field: 
   
   

    ```text
    ▸ Transport Layer Security
      ▸ TLSv1.3 Record Layer: Handshake Protocol: Client Hello
        ▸ Handshake Protocol: Client Hello
          ▸ Extension: server_name (len=22)
            ▸ Server Name Indication extension
    ```


6. We can see the SNI value which discloses the website we are visiting. The `tshark` command can give you the value directly for all packets containing a SNI value: 
   
   

    ```bash
    tshark -r /tmp/pg.pcap -Tfields -Y tls.handshake.extensions_server_name -e tls.handshake.extensions_server_name
    ```


This means even if we are using "Encrypted DNS" servers, the domain will likely be disclosed through SNI. The [TLS v1.3](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_1.3) protocol brings with it [Encrypted Client Hello](https://blog.cloudflare.com/encrypted-client-hello/), which prevents this kind of leak.

Governments, in particular [China](https://www.zdnet.com/article/china-is-now-blocking-all-encrypted-https-traffic-using-tls-1-3-and-esni/) and [Russia](https://www.zdnet.com/article/russia-wants-to-ban-the-use-of-secure-protocols-such-as-tls-1-3-doh-dot-esni/), have either already [started blocking](https://en.wikipedia.org/wiki/Server_Name_Indication#Encrypted_Client_Hello) it or expressed a desire to do so. Recently, Russia has [started blocking foreign websites](https://github.com/net4people/bbs/issues/108) that use the [HTTP/3](https://en.wikipedia.org/wiki/HTTP/3) standard. This is because the [QUIC](https://en.wikipedia.org/wiki/QUIC) protocol that is a part of HTTP/3 requires that `ClientHello` also be encrypted.



### OCSP(온라인 인증서 상태 프로토콜)

Another way your browser can disclose your browsing activities is with the [Online Certificate Status Protocol](https://en.wikipedia.org/wiki/Online_Certificate_Status_Protocol). When visiting an HTTPS website, the browser might check to see if the website's [certificate](https://en.wikipedia.org/wiki/Public_key_certificate) has been revoked. This is generally done through the HTTP protocol, meaning it is **not** encrypted.

The OCSP request contains the certificate "[serial number](https://en.wikipedia.org/wiki/Public_key_certificate#Common_fields)", which is unique. It is sent to the "OCSP responder" in order to check its status.

We can simulate what a browser would do using the [`openssl`](https://en.wikipedia.org/wiki/OpenSSL) command.

1. Get the server certificate and use [`sed`](https://en.wikipedia.org/wiki/Sed) to keep just the important part and write it out to a file: 
   
   

    ```bash
    openssl s_client -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_server.cert
    ```


2. Get the intermediate certificate. [Certificate Authorities (CA)](https://en.wikipedia.org/wiki/Certificate_authority) normally don't sign a certificate directly; they use what is known as an "intermediate" certificate. 
   
   

    ```bash
    openssl s_client -showcerts -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_and_intermediate.cert
    ```


3. The first certificate in `pg_and_intermediate.cert` is actually the server certificate from step 1. We can use `sed` again to delete until the first instance of END: 
   
   

    ```bash
    sed -n '/^-*END CERTIFICATE-*$/!d;:a n;p;ba' \
        /tmp/pg_and_intermediate.cert > /tmp/intermediate_chain.cert
    ```


4. Get the OCSP responder for the server certificate: 
   
   

    ```bash
    openssl x509 -noout -ocsp_uri -in /tmp/pg_server.cert
    ```


Our certificate shows the Lets Encrypt certificate responder. If we want to see all the details of the certificate we can use: 



    ```bash
    openssl x509 -text -noout -in /tmp/pg_server.cert
    ```


5. Start the packet capture: 
   
   

    ```bash
    tshark -w /tmp/pg_ocsp.pcap -f "tcp port http"
    ```


6. Make the OCSP request: 
   
   

    ```bash
    openssl ocsp -issuer /tmp/intermediate_chain.cert \
                 -cert /tmp/pg_server.cert \
                 -text \
                 -url http://r3.o.lencr.org
    ```


7. Open the capture: 
   
   

    ```bash
    wireshark -r /tmp/pg_ocsp.pcap
    ```


There will be two packets with the "OCSP" protocol: a "Request" and a "Response". For the "Request" we can see the "serial number" by expanding the triangle &#9656; next to each field: 



    ```bash
    ▸ Online Certificate Status Protocol
      ▸ tbsRequest
        ▸ requestList: 1 item
          ▸ Request
            ▸ reqCert
              serialNumber
    ```


For the "Response" we can also see the "serial number": 



    ```bash
    ▸ Online Certificate Status Protocol
      ▸ responseBytes
        ▸ BasicOCSPResponse
          ▸ tbsResponseData
            ▸ responses: 1 item
              ▸ SingleResponse
                ▸ certID
                  serialNumber
    ```


8. Or use `tshark` to filter the packets for the Serial Number: 
   
   

    ```bash
    tshark -r /tmp/pg_ocsp.pcap -Tfields -Y ocsp.serialNumber -e ocsp.serialNumber
    ```


If the network observer has the public certificate, which is publicly available, they can match the serial number with that certificate and therefore determine the site you're visiting from that. The process can be automated and can associate IP addresses with serial numbers. It is also possible to check [Certificate Transparency](https://en.wikipedia.org/wiki/Certificate_Transparency) logs for the serial number.



## "제가 암호화 DNS를 사용해야 할까요?"

Privacy Guides는 여러분이 *언제 암호화 DNS를 사용해야 할지* 판단할 수 있도록 플로우차트로 정리해 보았습니다.



``` mermaid
graph TB
    Start[시작] --> anonymous{익명성을<br>원하시나요?}
    anonymous--> | 예 | tor(Tor를 사용하세요)
    anonymous --> | 아니요 | censorship{검열 회피가<br>목적인가요?}
    censorship --> | 예 | vpnOrTor(VPN이나 Tor를<br>사용하세요)
    censorship --> | 아니요 | privacy{ISP로부터의<br>프라이버시가<br>목적인가요?}
    privacy --> | 예 | vpnOrTor
    privacy --> | 아니요 | obnoxious{"ISP의 간섭이<br>성가신가요?<br>(강제 리다이렉트 등)"}
    obnoxious --> | 예 | encryptedDNS(제3자 암호화 DNS를<br>사용하세요)
    obnoxious --> | 아니요 | ispDNS{ISP에서<br>암호화 DNS를<br>지원하나요?}
    ispDNS --> | 예 | useISP(ISP 암호화 DNS를<br>사용하세요)
    ispDNS --> | 아니요 | nothing(아무 것도<br>할 필요 없습니다)
```


Encrypted DNS with a third-party should only be used to get around redirects and basic [DNS blocking](https://en.wikipedia.org/wiki/DNS_blocking) when you can be sure there won't be any consequences or you're interested in a provider that does some rudimentary filtering.

[권장 DNS 서버 목록](../dns.md ""){.md-button}



## DNSSEC이란 무엇인가요?

[Domain Name System Security Extensions](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) (DNSSEC) is a feature of DNS that authenticates responses to domain name lookups. It does not provide privacy protections for those lookups, but rather prevents attackers from manipulating or poisoning the responses to DNS requests.

In other words, DNSSEC digitally signs data to help ensure its validity. In order to ensure a secure lookup, the signing occurs at every level in the DNS lookup process. As a result, all answers from DNS can be trusted.

The DNSSEC signing process is similar to someone signing a legal document with a pen; that person signs with a unique signature that no one else can create, and a court expert can look at that signature and verify that the document was signed by that person. These digital signatures ensure that data has not been tampered with.

DNSSEC implements a hierarchical digital signing policy across all layers of DNS. For example, in the case of a `privacyguides.org` lookup, a root DNS server would sign a key for the `.org` nameserver, and the `.org` nameserver would then sign a key for `privacyguides.org`’s authoritative nameserver.

<small>Adapted from [DNS Security Extensions (DNSSEC) overview](https://cloud.google.com/dns/docs/dnssec) by Google and [DNSSEC: An Introduction](https://blog.cloudflare.com/dnssec-an-introduction/) by Cloudflare, both licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).</small> 



## What is QNAME minimization?

A QNAME is a "qualified name", for example `privacyguides.org`. QNAME minimisation reduces the amount of information sent from the DNS server to the [authoritative name server](https://en.wikipedia.org/wiki/Name_server#Authoritative_name_server).

Instead of sending the whole domain `privacyguides.org`, QNAME minimization means the DNS server will ask for all the records that end in `.org`. Further technical description is defined in [RFC 7816](https://datatracker.ietf.org/doc/html/rfc7816).



## ECS(EDNS 클라이언트 서브넷)란 무엇인가요?

The [EDNS Client Subnet](https://en.wikipedia.org/wiki/EDNS_Client_Subnet) is a method for a recursive DNS resolver to specify a [subnetwork](https://en.wikipedia.org/wiki/Subnetwork) for the [host or client](https://en.wikipedia.org/wiki/Client_(computing)) which is making the DNS query.

It's intended to "speed up" delivery of data by giving the client an answer that belongs to a server that is close to them such as a [content delivery network](https://en.wikipedia.org/wiki/Content_delivery_network), which are often used in video streaming and serving JavaScript web apps.

This feature does come at a privacy cost, as it tells the DNS server some information about the client's location.
