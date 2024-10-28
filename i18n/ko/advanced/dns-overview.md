---
title: "DNS 개요"
icon: material/dns
description: DNS, 즉 도메인 네임 시스템은 '인터넷의 전화번호부'라고 할 수 있습니다. DNS가 있기 때문에 여러분은 브라우저에서 원하는 사이트를 찾아 연결할 수 있습니다.
---

[도메인 네임 시스템](https://ko.wikipedia.org/wiki/%EB%8F%84%EB%A9%94%EC%9D%B8_%EB%84%A4%EC%9E%84_%EC%8B%9C%EC%8A%A4%ED%85%9C)은 '인터넷의 전화번호부'라고 할 수 있습니다. DNS는 분산 서버 네트워크를 통해 도메인 이름을 IP 주소로 변환합니다. 브라우저 등의 서비스는 이를 이용해 인터넷 리소스를 로드할 수 있습니다.

## DNS란 무엇인가요?

사이트를 방문하면 숫자로 구성된 주소가 반환됩니다. 예를 들어, `privacyguides.org`를 방문할 경우에는 `192.98.54.105` 주소가 반환됩니다.

DNS는 [인터넷의 초창기](https://ko.wikipedia.org/wiki/%EB%8F%84%EB%A9%94%EC%9D%B8_%EB%84%A4%EC%9E%84_%EC%8B%9C%EC%8A%A4%ED%85%9C#%EC%97%AD%EC%82%AC)부터 존재해 왔습니다. DNS 서버와 주고받는 DNS 요청은 일반적으로 암호화가 적용되어 있지 **않습니다**. 가정 환경에서는 [DHCP](https://ko.wikipedia.org/wiki/%EB%8F%99%EC%A0%81_%ED%98%B8%EC%8A%A4%ED%8A%B8_%EA%B5%AC%EC%84%B1_%ED%94%84%EB%A1%9C%ED%86%A0%EC%BD%9C)를 통해 ISP로부터 서버를 제공받습니다.

암호화되지 않은 DNS 요청은 전송 도중에 쉽게 **감시** 및 **변조**될 수 있습니다. 일부 지역에서는 ISP가 기초적인 [DNS 필터링](https://en.wikipedia.org/wiki/DNS_blocking)을 수행하도록 명령받기도 합니다. 이 경우, ISP가 차단하고 있는 도메인의 IP 주소를 요청하면 서버가 응답하지 않거나, 목적지가 아닌 다른 IP 주소로 응답이 돌아옵니다. DNS 프로토콜은 암호화되지 않아서 ISP를 비롯한 모든 네트워크 사업자는 [DPI](https://ko.wikipedia.org/wiki/%EC%8B%AC%EC%B8%B5_%ED%8C%A8%ED%82%B7_%EA%B2%80%EC%82%AC)를 통해 요청을 모니터링할 수 있습니다. 또한 ISP는 어떤 DNS 서버를 사용하든 공통된 특징을 이용해 요청을 차단하는 것도 가능합니다.

다음 내용은 암호화되지 않은 일반적인 DNS와 [암호화가 적용된 DNS](#what-is-encrypted-dns)를 비교해 외부 관찰자가 볼 수 있는 것은 무엇이 있는지 증명하는 튜토리얼입니다.

### 암호화되지 않은 DNS

1. Using [`tshark`](https://wireshark.org/docs/man-pages/tshark.html) (part of the [Wireshark](https://en.wikipedia.org/wiki/Wireshark) project) we can monitor and record internet packet flow. 다음 명령어는 명시된 규칙을 충족하는 패킷을 기록합니다.

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

3. Next, we want to [analyse](https://wireshark.org/docs/wsug_html_chunked/ChapterIntroduction.html#ChIntroWhatIs) the results:

    === "Wireshark"

        ```
        wireshark -r /tmp/dns.pcap
        ```

    === "tshark"

        ```
        tshark -r /tmp/dns.pcap
        ```

앞선 과정을 거쳐 Wireshark 명령어를 실행하면 상단 창에 여러 [Frame](https://en.wikipedia.org/wiki/Ethernet_frame)이 표시되고, 하단 창에는 선택한 프레임에 대한 모든 데이터가 표시됩니다. 엔터프라이즈 필터링 및 모니터링 솔루션(정부에서 사용하는 솔루션 등을 말합니다)은 사람이 개입할 필요 없이 자동으로 이런 프로세스를 처리하고 집계하여 네트워크 관찰자에게 필요한 통계 데이터를 생성할 수 있습니다.

| No. | Time     | Source    | Destination | Protocol | Length | Info                                                                   |
| --- | -------- | --------- | ----------- | -------- | ------ | ---------------------------------------------------------------------- |
| 1   | 0.000000 | 192.0.2.1 | 1.1.1.1     | DNS      | 104    | Standard query 0x58ba A privacyguides.org OPT                          |
| 2   | 0.293395 | 1.1.1.1   | 192.0.2.1   | DNS      | 108    | Standard query response 0x58ba A privacyguides.org A 198.98.54.105 OPT |
| 3   | 1.682109 | 192.0.2.1 | 8.8.8.8     | DNS      | 104    | Standard query 0xf1a9 A privacyguides.org OPT                          |
| 4   | 2.154698 | 8.8.8.8   | 192.0.2.1   | DNS      | 108    | Standard query response 0xf1a9 A privacyguides.org A 198.98.54.105 OPT |

네트워크 관찰자는 이러한 패킷을 변조할 수 있습니다.

## '암호화된 DNS'란 무엇인가요?

Encrypted DNS can refer to one of a number of protocols, the most common ones being [DNSCrypt](#dnscrypt), [DNS over TLS](#dns-over-tls-dot), and [DNS over HTTPS](#dns-over-https-doh).

### DNSCrypt

[**DNSCrypt**](https://en.wikipedia.org/wiki/DNSCrypt)는 DNS 쿼리를 암호화하는 최초의 방법 중 하나였습니다. DNSCrypt는 443 포트에서 작동하며, TCP/UDP 전송 프로토콜 모두에서 작동합니다. DNSCrypt는 [국제 인터넷 표준화 기구(IETF)](https://ko.wikipedia.org/wiki/%EA%B5%AD%EC%A0%9C_%EC%9D%B8%ED%84%B0%EB%84%B7_%ED%91%9C%EC%A4%80%ED%99%94_%EA%B8%B0%EA%B5%AC)에 제출되지 않았고RFC 절차를 거치지 않았기 때문에, [일부 구현체](https://dnscrypt.info/implementations)를 제외하고는 널리 사용되지 않았습니다. 결과적으로, 보다 널리 사용되는 [DNS over HTTPS](#dns-over-https-doh)로 대체되었습니다.</p> 



### DOT(DNS over TLS)

[**DNS over TLS**](https://en.wikipedia.org/wiki/DNS_over_TLS)는 DNS 통신을 암호화하는 또 다른 방법으로, [RFC 7858](https://datatracker.ietf.org/doc/html/rfc7858)에 정의되어 있습니다. Support was first implemented in Android 9, iOS 14, and on Linux in [systemd-resolved](https://freedesktop.org/software/systemd/man/resolved.conf.html#DNSOverTLS=) in version 237. Preference in the industry has been moving away from DoT to DoH in recent years, as DoT is a [complex protocol](https://dnscrypt.info/faq) and has varying compliance to the RFC across the implementations that exist. 또한, 853 포트를 전용으로 사용하기 때문에 제한적인 방화벽에 의해 쉽게 차단될 수 있다는 문제도 존재합니다.



### DoH(DNS over HTTPS)

[**DNS over HTTPS**](https://en.wikipedia.org/wiki/DNS_over_HTTPS), as defined in [RFC 8484](https://datatracker.ietf.org/doc/html/rfc8484), packages queries in the [HTTP/2](https://en.wikipedia.org/wiki/HTTP/2) protocol and provides security with HTTPS. Firefox 60, Chrome 83과 같은 웹 브라우저에서 처음으로 지원되었습니다.

DoH 네이티브 구현은 iOS 14, macOS 11, Microsoft Windows, Android 13(단, [기본 활성화가 아닙니다](https://android-review.googlesource.com/c/platform/packages/modules/DnsResolver/+/1833144))부터 추가되었습니다. 일반 Linux 데스크톱의 경우, systemd [구현체](https://github.com/systemd/systemd/issues/8639)가 아직 존재하지 않기 때문에 [별도 소프트웨어를 설치해야 합니다](../dns.md#encrypted-dns-proxies).



### 운영 체제 기본 지원



#### Android

Android 9 이상 버전은 DNS over TLS를 지원합니다. 해당 설정은 **설정** &rarr; **네트워크 및 인터넷** &rarr; **비공개 DNS**에서 확인할 수 있습니다.



#### Apple 기기

iOS, iPadOS, tvOS, macOS 최신 버전은 DoT, DoH를 모두 지원합니다. 두 프로토콜 모두 [구성 프로필](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web)이나 [DNS 설정 API](https://developer.apple.com/documentation/networkextension/dns_settings)를 통해 운영 체제에서 기본으로 지원합니다.

구성 프로필이나, DNS 설정 API를 사용하는 앱을 설치하고 나면 DNS 구성에서 선택 가능합니다. VPN이 활성화되어 있는 경우, VPN 연결 내 DNS 요청은 시스템 전체 설정이 아닌 VPN의 DNS 설정을 사용합니다.

Apple은 암호화 DNS 프로필 생성을 위한 기본 인터페이스를 제공하지 않습니다. [보안 DNS 프로필 생성기(Secure DNS profile creator)](https://dns.notjakob.com/tool.html)는 자신만의 암호화 DNS 프로필을 생성할 수 있는 비공식 툴이지만, 프로필 서명은 불가능합니다. 프로필 서명은 프로필 출처 확인 및 무결성 보장에 도움이 되므로, 서명된 프로필이 선호됩니다. 서명된 구성 프로필에는 '확인 완료' 표시가 나타납니다. 코드 서명에 대한 자세한 내용은 [About Code Signing](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html)을 참고하세요.



#### Linux

`systemd-resolved`, which many Linux distributions use to do their DNS lookups, doesn't yet [support DoH](https://github.com/systemd/systemd/issues/8639). If you want to use DoH, you'll need to install a proxy like [dnscrypt-proxy](../dns.md#dnscrypt-proxy) and [configure it](https://wiki.archlinux.org/title/Dnscrypt-proxy) to take all the DNS queries from your system resolver and forward them over HTTPS.



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


We can see the [connection establishment](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#Connection_establishment) and [TLS handshake](https://cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake) that occurs with any encrypted connection. 뒤따르는 'Application Data' 패킷을 살펴보면 요청했던 도메인이나 반환된 IP 주소가 포함되어 있지 않다는 것 또한 확인할 수 있습니다.



## 암호화 DNS를 사용하지 **말아야** 하는 이유는 무엇인가요?

인터넷 필터링(혹은 검열)이 존재하는 지역에서는 '차단된 정보에 접근하는 행위' 자체가 자신의 [위협 모델](../basics/threat-modeling.md)에서 고려해야 할 어떠한 결과를 초래할 수도 있습니다. Privacy Guides는 이러한 목적으로 암호화 DNS를 사용하는 것은 추천드리지 **않습니다**. Use [Tor](../advanced/tor-overview.md) or a [VPN](../vpn.md) instead. VPN을 사용하는 경우, 자신이 사용하는 VPN의 DNS 서버를 사용해야 합니다. VPN을 사용하는 순간부터 이미 자신의 모든 네트워크 활동을 VPN 업체에게 맡기고 있는 것이기 때문입니다.

일반적으로 우리가 무언가에 대한 DNS 조회를 할 때는 해당 리소스에 접근하고자 하는 의도가 있습니다. 다음은 암호화 DNS를 사용하더라도 여러분의 인터넷 탐색 활동이 노출될 수 있는 몇 가지 경우입니다.



### IP 주소

인터넷 탐색 활동을 알아내는 가장 쉬운 방법은 해당 기기에서 접근하는 IP 주소를 확인하는 것입니다. 예를 들어, 어떤 관찰자가 `privacyguides.org`는 `198.98.54.105`에 존재함을 알고 있는 상태에서, 여러분의 기기가 `198.98.54.105`로 데이터를 요청한 것을 확인했다면, 여러분이 Privacy Guides를 방문했을 것으로 예상할 수 있습니다.

이 방식은 해당 IP 주소의 서버가 호스팅하고 있는 웹사이트의 개수가 적을 경우에만 유효합니다. 또한 공유 플랫폼(Github Pages, Cloudflare Pages, Netlify, WordPress, Blogger 등)에서 사이트가 호스팅되고 있는 경우에도 그다지 효과가 없습니다. 최신 인터넷 환경에서는 매우 일반적인 [리버스 프록시](https://ko.wikipedia.org/wiki/%EB%A6%AC%EB%B2%84%EC%8A%A4_%ED%94%84%EB%A1%9D%EC%8B%9C) 뒤에 호스팅되고 있는 경우에도 마찬가지로 그다지 효과가 없습니다.



### SNI(Server Name Indication)

SNI(Server Name Indication, 서버 이름 표시)는 주로 하나의 IP 주소에서 여러 웹사이트를 호스팅하는 경우에 사용됩니다. Cloudflare 등의 서비스나, 그 외 [서비스 거부 공격(DosS공격)](https://ko.wikipedia.org/wiki/%EC%84%9C%EB%B9%84%EC%8A%A4_%EA%B1%B0%EB%B6%80_%EA%B3%B5%EA%B2%A9) 보호 서비스 등이 해당 예시입니다.

1. 마찬가지로 `tshark`로 캡처를 시작합니다. 지나치게 많은 패킷이 캡처되지 않도록 Privacy Guides의 IP 주소 필터를 추가합시다. 
   
   

    ```bash
    tshark -w /tmp/pg.pcap port 443 and host 198.98.54.105
    ```


2. 이제 [https://privacyguides.org](https://privacyguides.org)를 방문합니다.

3. 사이트를 방문한 이후에는 <kbd>CTRL</kbd> + <kbd>C</kbd>로 패킷 캡처를 중지합니다.

4. 이제 결과를 분석합시다. 
   
   

    ```bash
    wireshark -r /tmp/pg.pcap
    ```


연결이 설정이 이루어지고 Privacy Guides 사이트에 대한 TLS 핸드셰이크 과정을 확인할 수 있습니다. 프레임 5 주변에서 "Client Hello"를 확인할 수 있습니다.

5. 각 필드 옆의 삼각형 &#9656;을 눌러 펼칩니다. 
   
   

    ```text
    ▸ Transport Layer Security
      ▸ TLSv1.3 Record Layer: Handshake Protocol: Client Hello
        ▸ Handshake Protocol: Client Hello
          ▸ Extension: server_name (len=22)
            ▸ Server Name Indication extension
    ```


6. 방문 중인 사이트를 나타내는 SNI 값을 확인할 수 있습니다. `tshark` 명령어로 SNI 값을 포함한 모든 패킷 값을 직접 확인 가능합니다. 
   
   

    ```bash
    tshark -r /tmp/pg.pcap -Tfields -Y tls.handshake.extensions_server_name -e tls.handshake.extensions_server_name
    ```


즉, '암호화 DNS'를 사용하더라도 도메인은 SNI를 통해 노출될 가능성이 높습니다. The [TLS v1.3](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_1.3) protocol brings with it [Encrypted Client Hello](https://blog.cloudflare.com/encrypted-client-hello), which prevents this kind of leak.

Governments, in particular [China](https://zdnet.com/article/china-is-now-blocking-all-encrypted-https-traffic-using-tls-1-3-and-esni) and [Russia](https://zdnet.com/article/russia-wants-to-ban-the-use-of-secure-protocols-such-as-tls-1-3-doh-dot-esni), have either already [started blocking](https://en.wikipedia.org/wiki/Server_Name_Indication#Encrypted_Client_Hello) it or expressed a desire to do so. 최근 러시아는 [HTTP/3](https://en.wikipedia.org/wiki/HTTP/3) 표준을 사용하는 [해외 사이트를 차단하기 시작했습니다](https://github.com/net4people/bbs/issues/108). HTTP/3의 일부인 [QUIC](https://ko.wikipedia.org/wiki/QUIC) 프로토콜에서는 `ClientHello` 암호화가 필수적이기 때문입니다.



### OCSP(온라인 인증서 상태 프로토콜)

[OCSP](https://ko.wikipedia.org/wiki/%EC%98%A8%EB%9D%BC%EC%9D%B8_%EC%9D%B8%EC%A6%9D%EC%84%9C_%EC%83%81%ED%83%9C_%ED%94%84%EB%A1%9C%ED%86%A0%EC%BD%9C)를 통해 인터넷 탐색 활동이 노출될 가능성도 있습니다. 여러분이 HTTPS 웹사이트를 방문할 때, 브라우저는 해당 웹사이트의 [인증서](https://ko.wikipedia.org/wiki/%EA%B3%B5%EA%B0%9C_%ED%82%A4_%EC%9D%B8%EC%A6%9D%EC%84%9C)가 만료되었는지 확인합니다. 이 과정은 HTTP 프로토콜을 사용해 이루어집니다. 다시 말해, 암호화가 적용되지 **않습니다**.

OCSP 요청에는 고유한 인증서 [일련번호](https://en.wikipedia.org/wiki/Public_key_certificate#Common_fields)가 포함되어 있습니다. 이는 인증서 상태를 확인하는 과정에서 'OCSP 응답자(Responder)'에게 전송됩니다.

[`openssl`](https://ko.wikipedia.org/wiki/OpenSSL) 명령어로 브라우저의 동작을 시뮬레이션할 수 있습니다.

1. 서버 인증서를 가져오고 [`sed`](https://ko.wikipedia.org/wiki/Sed_(%EC%9C%A0%ED%8B%B8%EB%A6%AC%ED%8B%B0))를 이용해 중요한 부분만 파일에 기록합니다. 
   
   

    ```bash
    openssl s_client -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_server.cert
    ```


2. 중간 인증서(Intermediate Certificate)를 받습니다. [인증 기관(CA)](https://ko.wikipedia.org/wiki/%EC%9D%B8%EC%A6%9D_%EA%B8%B0%EA%B4%80)은 일반적으로 인증서에 직접 서명하지 않고 '중간 인증서'라고 불리는 것을 사용합니다. 
   
   

    ```bash
    openssl s_client -showcerts -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_and_intermediate.cert
    ```


3. `pg_and_intermediate.cert`의 첫 번째 인증서는 1단계에서의 서버에 대한 인증서입니다. `sed` 명령어를 다시 사용해 END가 처음 등장하는 부분까지 제거합니다. 
   
   

    ```bash
    sed -n '/^-*END CERTIFICATE-*$/!d;:a n;p;ba' \
        /tmp/pg_and_intermediate.cert > /tmp/intermediate_chain.cert
    ```


4. 서버 인증서에 대한 OCSP 응답자를 얻어냅니다. 
   
   

    ```bash
    openssl x509 -noout -ocsp_uri -in /tmp/pg_server.cert
    ```


인증서에서 Lets Encrypt 인증서 응답자를 확인할 수 있습니다. 인증서의 모든 세부 정보를 확인하려면 다음 명령어를 사용합니다. 



    ```bash
    openssl x509 -text -noout -in /tmp/pg_server.cert
    ```


5. 패킷 캡처를 시작합니다. 
   
   

    ```bash
    tshark -w /tmp/pg_ocsp.pcap -f "tcp port http"
    ```


6. OCSP 요청을 생성합니다. 
   
   

    ```bash
    openssl ocsp -issuer /tmp/intermediate_chain.cert \
                 -cert /tmp/pg_server.cert \
                 -text \
                 -url http://r3.o.lencr.org
    ```


7. 캡처를 엽니다. 
   
   

    ```bash
    wireshark -r /tmp/pg_ocsp.pcap
    ```


'OCSP' 프로토콜에서 'Request', 'Response'라는 두 패킷을 확인할 수 있습니다. 'Request'에서는 각 필드 옆의 삼각형 &#9656;을 눌러 일련번호(Serial Number)를 확인할 수 있습니다. 



    ```bash
    ▸ Online Certificate Status Protocol
      ▸ tbsRequest
        ▸ requestList: 1 item
          ▸ Request
            ▸ reqCert
              serialNumber
    ```


'Response'에서도 마찬가지로 일련번호를 확인할 수 있습니다. 



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


8. 혹은 `tshark`를 이용해 패킷을 일련번호로 필터링합니다. 
   
   

    ```bash
    tshark -r /tmp/pg_ocsp.pcap -Tfields -Y ocsp.serialNumber -e ocsp.serialNumber
    ```


네트워크 관찰자가 공개적으로 사용할 수 있는 공개 인증서를 가지고 있는 경우, 일련번호를 해당 인증서와 대조할 수 있으므로 여러분이 어떤 사이트를 방문하는지 알아낼 수 있습니다. 이 과정은 자동화될 수 있으며, 일련번호를 IP 주소와 연관시킬 수 있습니다. [인증서 투명성](https://en.wikipedia.org/wiki/Certificate_Transparency) 로그에서 일련번호를 확인하는 것 또한 가능합니다.



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


제3자 서버를 사용하는 암호화 DNS는 '이를 사용함으로써 아무런 문제가 발생하지 않을 것이라고 확신할 수 있을 때' ISP의 기본적인 리디렉션 및 [DNS 차단](https://en.wikipedia.org/wiki/DNS_blocking)을 우회하는 용도로만 사용하거나, 기초적인 DNS 필터링 서비스를 필요로 할 때만 사용해야 합니다.

[권장 DNS 서버 목록](../dns.md ""){.md-button}



## DNSSEC이란 무엇인가요?

DNSSEC([Domain Name System Security Extensions](https://ko.wikipedia.org/wiki/DNSSEC))는 도메인 이름 조회에 대한 응답을 인증하는 DNS 기능입니다. 이 기능은 프라이버시 보호와는 별 관련이 없지만, 공격자가 DNS 요청 응답을 변조하거나 오염시키는 것을 방지합니다.

DNSSEC은 데이터 유효성을 보장하기 위해 데이터에 디지털 서명을 수행합니다. 안전한 조회 과정을 보장하기 위해, 디지털 서명은 DNS 조회 과정의 모든 영역에서 이루어집니다. 결과적으로, 모든 DNS 응답을 신뢰할 수 있습니다.

DNSSEC 서명 과정은 사람이 펜으로 법적 문서에 서명하는 과정과 유사합니다. 다른 사람이 따라 만들 수 없는 고유한 서명으로 서명하고, 법조인은 해당 서명을 보고 문서의 서명이 위조되지 않았음을 확인합니다. 마찬가지로 디지털 서명은 데이터가 변조되지 않았음을 확인합니다.

DNSSEC은 DNS의 모든 계층에 걸쳐 계층적(Hierarchical) 디지털 서명 정책을 구현합니다. 예를 들어 `privacyguides.org`를 조회하는 경우, 루트 DNS 서버는 자신의 키로 서명해 `.org` 네임 서버에게 제공하고, `.org` 네임 서버 또한 자신의 키로 서명해 `privacyguides.org`의 권한 있는 서버에 제공합니다.

<small>Adapted from [DNS Security Extensions (DNSSEC) overview](https://cloud.google.com/dns/docs/dnssec) by Google and [DNSSEC: An Introduction](https://blog.cloudflare.com/dnssec-an-introduction) by Cloudflare, both licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0).</small> 



## QNAME 최소화란 무엇인가요?

QNAME은 '정규화된 이름(Qualified Name)'입니다(예시: `discuss.privacyguides.net`). In the past, when resolving a domain name your DNS resolver would ask every server in the chain to provide any information it has about your full query. In this example below, your request to find the IP address for `discuss.privacyguides.net` gets asked of every DNS server provider:

| Server            | 질문                                    | 응답                                          |
| ----------------- | ------------------------------------- | ------------------------------------------- |
| 루트 서버             | discuss.privacyguides.net의 IP는 무엇인가요? | I don't know, ask .net's server...          |
| .net 서버           | discuss.privacyguides.net의 IP는 무엇인가요? | I don't know, ask Privacy Guides' server... |
| Privacy Guides 서버 | discuss.privacyguides.net의 IP는 무엇인가요? | 5.161.195.190!                              |


With "QNAME minimization," your DNS resolver now only asks for just enough information to find the next server in the chain. In this example, the root server is only asked for enough information to find the appropriate nameserver for the .net TLD, and so on, without ever knowing the full domain you're trying to visit:

| Server            | 질문                                                   | 응답                                |
| ----------------- | ---------------------------------------------------- | --------------------------------- |
| 루트 서버             | What's the nameserver for .net?                      | *Provides .net's server*          |
| .net 서버           | What's the nameserver for privacyguides.net?         | *Provides Privacy Guides' server* |
| Privacy Guides 서버 | What's the nameserver for discuss.privacyguides.net? | This server!                      |
| Privacy Guides 서버 | discuss.privacyguides.net의 IP는 무엇인가요?                | 5.161.195.190                     |


While this process can be slightly more inefficient, in this example neither the central root nameservers nor the TLD's nameservers ever receive information about your *full* query, thus reducing the amount of information being transmitted about your browsing habits. 세부 기술 설명은 [RFC 7816](https://datatracker.ietf.org/doc/html/rfc7816)에 정의되어 있습니다.



## ECS(EDNS 클라이언트 서브넷)란 무엇인가요?

[EDNS 클라이언트 서브넷](https://en.wikipedia.org/wiki/EDNS_Client_Subnet)이란, DNS 쿼리를 생성하는 [호스트나 클라이언트](https://ko.wikipedia.org/wiki/%ED%81%B4%EB%9D%BC%EC%9D%B4%EC%96%B8%ED%8A%B8_(%EC%BB%B4%ED%93%A8%ED%8C%85))의 [서브넷](https://ko.wikipedia.org/wiki/%EB%B6%80%EB%B6%84%EB%A7%9D)을 Recursive DNS 리졸버가 지정할 수 있는 방식입니다.

ECS는 동영상 스트리밍이나 JavaScript 웹 앱 서비스에 때 자주 쓰이는 [콘텐츠 전송 네트워크(CDN)](https://ko.wikipedia.org/wiki/%EC%BD%98%ED%85%90%EC%B8%A0_%EC%A0%84%EC%86%A1_%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC)처럼 클라이언트와 가까운 서버의 응답을 제공하여 데이터 전송 속도를 높이는 기술입니다.

This feature does come at a privacy cost, as it tells the DNS server some information about the client's location, generally your IP network. For example, if your IP address is `198.51.100.32` the DNS provider might share `198.51.100.0/24` with the authoritative server. Some DNS providers anonymize this data by providing another IP address which is approximately near your location.

If you have `dig` installed you can test whether your DNS provider gives EDNS information out to DNS nameservers with the following command:



```bash
dig +nocmd -t txt o-o.myaddr.l.google.com +nocomments +noall +answer +stats
```


Note that this command will contact Google for the test, and return your IP as well as EDNS client subnet information. If you want to test another DNS resolver you can specify their IP, to test `9.9.9.11` for example:



```bash
dig +nocmd @9.9.9.11 -t txt o-o.myaddr.l.google.com +nocomments +noall +answer +stats
```


If the results include a second edns0-client-subnet TXT record (like shown below), then your DNS server is passing along EDNS information. The IP or network shown after is the precise information which was shared with Google by your DNS provider.



```text
o-o.myaddr.l.google.com. 60 IN TXT "198.51.100.32"
o-o.myaddr.l.google.com. 60 IN TXT "edns0-client-subnet 198.51.100.0/24"
;; Query time: 64 msec
;; SERVER: 9.9.9.11#53(9.9.9.11)
;; WHEN: Wed Mar 13 10:23:08 CDT 2024
;; MSG SIZE  rcvd: 130
```
