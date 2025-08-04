---
title: "DNSの概要"
icon: material/dns
description: ドメインネームシステム（DNS）は「インターネットの電話帳」であり、ブラウザが探しているウェブサイトを見つけるのに役立ちます。
---

[ドメイン・ネーム・システム](https://en.wikipedia.org/wiki/Domain_Name_System)は「インターネットの電話帳」です。 DNSはドメイン名をIPアドレスに変換しており、分散化されたサーバーのネットワークを通じ、ブラウザやその他のサービスはインターネットリソースをロードできるようになります。

## DNSとは？

ウェブサイトにアクセスすると、数値のアドレスが返されます。 たとえば、 `privacyguides.org`にアクセスすると、アドレス `192.98.54.105` が返されます。

DNSはインターネットの[初期](https://en.wikipedia.org/wiki/Domain_Name_System#History)から存在しています。 DNSサーバーとの間で行われるDNSリクエストは、一般的には暗号化**されていません**。 住宅向けの設定では、[DHCP](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol)経由でISPからサーバーが既定されます。

暗号化されていないDNSリクエストは、転送中簡単に**監視し**、**変更**することができます。 世界のいくつかの地域では、ISPは原始的な[DNSフィルタリング](https://en.wikipedia.org/wiki/DNS_blocking)を行うよう命じられています。 ブロックされているドメインのIPアドレスをリクエストすると、サーバーは応答しないか、別のIPアドレスで応答することがあります。 DNSプロトコルは暗号化されていないため、ISPは（またはどのネットワークオペレーターも） [ディープ・パケット・インスペクション](https://en.wikipedia.org/wiki/Deep_packet_inspection)によって 、リクエストを監視できます。 ISPは、どのDNSサーバーが使われているかに関係なく、共通の特徴に基づいてリクエストをブロックすることもできます。

以下では通常の暗号化されていないDNSと[暗号化DNS](#what-is-encrypted-dns)を用いて、外部の観察者が何を見ることができるかを説明します。

### 暗号化されていないDNS

1. [`tshark`](https://wireshark.org/docs/man-pages/tshark.html)（[Wireshark](https://en.wikipedia.org/wiki/Wireshark)プロジェクトの一部）を使い、インターネットのパケットフローを監視、記録します。 このコマンドは指定されたルールに合致するパケットを記録します：

    ```bash
    tshark -w /tmp/dns.pcap udp port 53 and host 1.1.1.1 or host 8.8.8.8
    ```

2. [`dig`](https://en.wikipedia.org/wiki/Dig_(command))（Linux、macOSなど）や[`nslookup`](https://en.wikipedia.org/wiki/Nslookup)（Windows）を使ってDNSルックアップを両方のサーバーに送ります。 ウェブブラウザなどのソフトウェアは暗号化DNSの使用が設定されていない限り、自動的にルックアップを行います。

    === "LinuxとmacOS"

        ```
        dig +noall +answer privacyguides.org @1.1.1.1
        dig +noall +answer privacyguides.org @8.8.8.8
        ```
    === "Windows"

        ```
        nslookup privacyguides.org 1.1.1.1
        nslookup privacyguides.org 8.8.8.8
        ```

3. 次に結果を[分析](https://wireshark.org/docs/wsug_html_chunked/ChapterIntroduction.html#ChIntroWhatIs)します：

    === "Wireshark"

        ```
        wireshark -r /tmp/dns.pcap
        ```

    === "tshark"

        ```
        tshark -r /tmp/dns.pcap
        ```

上記のWiresharkのコマンドを実行すると、上のペインは[フレーム](https://en.wikipedia.org/wiki/Ethernet_frame)が表示され、下のペインには選択したフレームに関するすべてのデータが表示されます。 企業向けフィルタリング・監視ソリューション（政府機関が購入するようなもの）は人手を介さずこの手順を自動的に行い、フレームを集約し、ネットワーク監視者にとって有用な統計データを作成することができます。

| 番号 | 時間       | 参照元       | 宛先        | プロトコル | 長さ  | 詳細                                                                     |
| -- | -------- | --------- | --------- | ----- | --- | ---------------------------------------------------------------------- |
| 1  | 0.000000 | 192.0.2.1 | 1.1.1.1   | DNS   | 104 | Standard query 0x58ba A privacyguides.org OPT                          |
| 2  | 0.293395 | 1.1.1.1   | 192.0.2.1 | DNS   | 108 | Standard query response 0x58ba A privacyguides.org A 198.98.54.105 OPT |
| 3  | 1.682109 | 192.0.2.1 | 8.8.8.8   | DNS   | 104 | Standard query 0xf1a9 A privacyguides.org OPT                          |
| 4  | 2.154698 | 8.8.8.8   | 192.0.2.1 | DNS   | 108 | Standard query response 0xf1a9 A privacyguides.org A 198.98.54.105 OPT |

監視者はこれらのパケットをいずれも変更することができます。

## 「暗号化されたDNS」とは？

暗号化DNSにはいくつかのプロトコルがあり、最も一般的なものは[DNSCrypt](#dnscrypt)、[DNS over TLS](#dns-over-tls-dot)と[DNS over HTTPS](#dns-over-https-doh)です。

### DNSCrypt

[**DNSCrypt**](https://en.wikipedia.org/wiki/DNSCrypt)はDNSクエリを暗号化する初期の方法の一つでした。 DNSCryptは443ポートで動作し、TCPやUDP通信プロトコルの両方で動作します。 DNSCryptは[インターネット技術特別調査委員会（IETF）](https://en.wikipedia.org/wiki/Internet_Engineering_Task_Force)に提出されず、[リクエストフォーコメンツ（RFC）](https://en.wikipedia.org/wiki/Request_for_Comments)のプロセスも経ていないため、一部の[実装](https://dnscrypt.info/implementations)以外では広く使用されていません。 そのため、より人気のある[DNS over HTTPS](#dns-over-https-doh)に大部分が取って代わられています。

### DNS over TLS (DoT)

[**DNS over TLS**](https://en.wikipedia.org/wiki/DNS_over_TLS)はDNS通信を暗号化するもう一つの方法で[RFC 7858](https://datatracker.ietf.org/doc/html/rfc7858)で定められています。 Android9、iOS14、Linuxでは[systemd-resolved](https://freedesktop.org/software/systemd/man/resolved.conf.html#DNSOverTLS=)のバージョン237で初めて対応されました。 DoTは[複雑なプロトコル](https://dnscrypt.info/faq)であり、実装によってRFCへの準拠が異なるため、近年ではDoTよりもDoHが選ばれるようになっています。 また、DoTはファイアウォールで簡単にブロックできる853ポートのみで動作しています。

### DNS over HTTPS (DoH)

[**DNS over HTTPS**](https://en.wikipedia.org/wiki/DNS_over_HTTPS)は[RFC8484](https://datatracker.ietf.org/doc/html/rfc8484)で定められ、[HTTP/2](https://en.wikipedia.org/wiki/HTTP/2)プロトコルでクエリをパッケージ化し、HTTPSによるセキュリティで保護します。 ウェブブラウザではFirefox60やChrome83で初めて対応されました。

DoHのネイティブ実装はiOS14、macOS11、Microsoft WindowsやAndroid13（ただし、[デフォルト](https://android-review.googlesource.com/c/platform/packages/modules/DnsResolver/+/1833144)では有効になりません）で登場しました。 一般的なLinuxデスクトップの対応はsystemdの[実装](https://github.com/systemd/systemd/issues/8639)を待っているため、[サードパーティのソフトウェアをインストールする必要がまだあります](../dns.md#encrypted-dns-proxies)。

### OSでのネイティブサポート

#### Android

Android 9以降ではDNS over TLSをサポートしています。 設定は以下にて確認できます： **設定** &rarr; **ネットワーク & インターネット** &rarr; **プライベートDNS**.

#### Appleデバイス

最新バージョンのiOS、iPadOS、tvOS、macOSはDoTとDoHのどちらにも対応しています。 [構成プロファイル](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web)もしくは[DNS設定API](https://developer.apple.com/documentation/networkextension/dns_settings)でどちらのプロトコルもネイティブ対応しています。

構成プロファイルまたはDNS設定APIを使ったアプリをインストールした後、DNS設定を選択することができます。 VPNが有効な場合、VPNトンネル内での名前解決にはVPNのDNS設定が使われ、システム全体の設定は使われません。

Appleは暗号化DNSプロファイルを作成するためのネイティブインターフェースを提供していません。 [Secure DNS profile creator](https://dns.notjakob.com/tool.html)は暗号化DNSプロファイルを作成するための非公式のツールですが、署名はされません。 署名されたプロファイルが推奨されます。署名はプロファイルの発信元を検証し、整合性を確かめるのに役立ちます。 署名された構成プロファイルは緑色の「検証済み」ラベルがつけられます。 コード署名の詳細については[About Code Signing](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html)を参照してください。

#### Linux

多くのLinuxディストリビューションがDNSルックアップに使用している`systemd-resolved`はまだ[DoHに対応](https://github.com/systemd/systemd/issues/8639)していません。 DoHを使いたい場合、[dnscrypt-proxy](../dns.md#dnscrypt-proxy)のようなプロキシをインストールし、システムリゾルバからのすべてのDNSクエリを受け取り、HTTPS経由で転送するように[設定する](https://wiki.archlinux.org/title/Dnscrypt-proxy)必要があります。

## 外部からは何が見えるのか？

この例では、DoHリクエストを行った際に何が起きているか記録します：

1. まず、 `tshark`を起動：

    ```bash
    tshark -w /tmp/dns_doh.pcap -f "tcp port https and host 1.1.1.1"
    ```

2. 次に、`curl`でリクエストをします：

    ```bash
    curl -vI --doh-url https://1.1.1.1/dns-query https://privacyguides.org
    ```

3. リクエストした後、<kbd>CTRL</kbd>+<kbd>C</kbd>でパケットキャプチャを終了します。

4. Wiresharkで結果を分析します：

    ```bash
    wireshark -r /tmp/dns_doh.pcap
    ```

暗号化された接続で発生する[コネクション確立](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#Connection_establishment)と[TLSハンドシェイク](https://cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake)を見ることができます。 その後の「アプリケーションデータ」パケットにはリクエストしたドメインや返されたIPアドレスは含まれていません。

## なぜ暗号化DNSを使う**べきではない**のか？

インターネットフィルタリング（もしくは検閲）が行われている場所で、禁止されている情報源にアクセスするために、[脅威モデル](../basics/threat-modeling.md)に基づいて考慮すべきことになる可能性はあります。 この目的のために暗号化DNSをつかうことは推奨**しません**。 代わりに[Tor](../advanced/tor-overview.md)や[VPN](../vpn.md)を使ってください。 VPNを使っているのであれば、VPNのDNSサーバーを使う必要があります。 VPNを使うことは、ネットワークアクティビティのすべてをVPNに任せることになります。

DNSルックアップをする際、一般的には情報源にアクセスするためです。 以下では暗号化DNSを使ったとしてもブラウジングのアクティビティが開示される可能性のある方法について説明します：

### IPアドレス

ブラウジングアクティビティを調べる最も単純な方法は、デバイスがアクセスしているIPアドレスを調べることです。 例えば、監視人が`privacyguides.org`のIPアドレスは`198.98.54.105`であることを知っていて、あなたのデバイスが`198.98.54.105`からのデータを要求している場合、あなたはPrivacy Guidesを見ている可能性が高いと分かります。

IPアドレスが少数のウェブサイトをホストしているサーバーにある場合にのみ有効です。 サイトが共有プラットフォーム（GitHub Pages、Cloudflare Pages、Netlify、WordPress、Bloggerなど）上でホストされている場合はあまり役に立ちません。 また、サーバーが[リバースプロキシ](https://en.wikipedia.org/wiki/Reverse_proxy)の後段にホストされている場合も役に立ちません。リバースプロキシを使うことは現代のインターネットでは一般的な方法です。

### サーバー名表示（SNI）

サーバー名表示は一つのIPアドレスに多くのウェブサイトをホストしている際によく使われます。 Cloudflareのようなサービスや、[DoS攻撃](https://en.wikipedia.org/wiki/Denial-of-service_attack)対策の場合もあります。

1. `tshark`で再度キャプチャをします。 Privacy GuidesのIPアドレスのフィルタを追加したため、多くのパケットはキャプチャしません：

    ```bash
    tshark -w /tmp/pg.pcap port 443 and host 198.98.54.105
    ```

2. [https://privacyguides.org](https://privacyguides.org)にアクセスします。

3. ウェブサイトを訪れた後、<kbd>CTRL</kbd> + <kbd>C</kbd>でパケットキャプチャを終了します。

4. 次に結果を分析します：

    ```bash
    wireshark -r /tmp/pg.pcap
    ```

    接続の確立の後、Privacy GuidesのウェブサイトのTLSハンドシェイクが表示されています。 5フレーム目のあたりにあります。 「Client Hello」があります。

5. 各フィールドの隣にある三角形&#9656;を展開します：

    ```text
    ▸ Transport Layer Security
      ▸ TLSv1.3 Record Layer: Handshake Protocol: Client Hello
        ▸ Handshake Protocol: Client Hello
          ▸ Extension: server_name (len=22)
            ▸ Server Name Indication extension
    ```

6. 訪れたウェブサイトが開示しているSNIを見ることができます。 `tshark`コマンドでは、サーバー名表示を含むすべてのパケットの値を直接見ることができます：

    ```bash
    tshark -r /tmp/pg.pcap -Tfields -Y tls.handshake.extensions_server_name -e tls.handshake.extensions_server_name
    ```

つまり「暗号化DNS」を使っていたとしても、SNIを通じてドメインが開示される可能性があるということです。 [TLS v1.3](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_1.3)プロトコルはこのような漏洩を防ぐ[Encrypted Client Hello](https://blog.cloudflare.com/encrypted-client-hello)があります。

各国政府、特に[中国](https://zdnet.com/article/china-is-now-blocking-all-encrypted-https-traffic-using-tls-1-3-and-esni)や[ロシア](https://zdnet.com/article/russia-wants-to-ban-the-use-of-secure-protocols-such-as-tls-1-3-doh-dot-esni)はすでにTLS v1.3を[ブロックしている](https://en.wikipedia.org/wiki/Server_Name_Indication#Encrypted_Client_Hello)かその意向を示しています。 最近、ロシアは[HTTP/3](https://en.wikipedia.org/wiki/HTTP/3)標準を使用する[外国のウェブサイトをブロックし始めました](https://github.com/net4people/bbs/issues/108)。 HTTP/3の一部である[QUIC](https://en.wikipedia.org/wiki/QUIC)プロトコルが`ClientHello`の暗号化を必要としているためです。

### Online Certificate Status Protocol (OCSP)

Another way your browser can disclose your browsing activities is with the [Online Certificate Status Protocol](https://en.wikipedia.org/wiki/Online_Certificate_Status_Protocol). When visiting an HTTPS website, the browser might check to see if the website's [certificate](https://en.wikipedia.org/wiki/Public_key_certificate) has been revoked. This is generally done through the HTTP protocol, meaning it is **not** encrypted.

The OCSP request contains the certificate "[serial number](https://en.wikipedia.org/wiki/Public_key_certificate#Common_fields)", which is unique. It is sent to the "OCSP responder" in order to check its status.

We can simulate what a browser would do using the [`openssl`](https://en.wikipedia.org/wiki/OpenSSL) command.

1. Get the server certificate and use [`sed`](https://en.wikipedia.org/wiki/Sed) to keep just the important part and write it out to a file:

    ```bash
    openssl s_client -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_server.cert
    ```

2. 中間証明書を取得。 [Certificate Authorities (CA)](https://en.wikipedia.org/wiki/Certificate_authority) normally don't sign a certificate directly; they use what is known as an "intermediate" certificate.

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

## Should I use encrypted DNS?

We made this flow chart to describe when you *should* use encrypted DNS:

``` mermaid
graph TB
    Start[Start] --> anonymous{Trying to be<br> anonymous?}
    anonymous--> | Yes | tor(Use Tor)
    anonymous --> | No | censorship{Avoiding<br> censorship?}
    censorship --> | Yes | vpnOrTor(Use<br> VPN or Tor)
    censorship --> | No | privacy{Want privacy<br> from ISP?}
    privacy --> | Yes | vpnOrTor
    privacy --> | No | obnoxious{ISP makes<br> obnoxious<br> redirects?}
    obnoxious --> | Yes | encryptedDNS(Use<br> encrypted DNS<br> with 3rd party)
    obnoxious --> | No | ispDNS{Does ISP support<br> encrypted DNS?}
    ispDNS --> | Yes | useISP(Use<br> encrypted DNS<br> with ISP)
    ispDNS --> | No | nothing(Do nothing)
```

Encrypted DNS with a third party should only be used to get around redirects and basic [DNS blocking](https://en.wikipedia.org/wiki/DNS_blocking) when you can be sure there won't be any consequences, or you're interested in a provider that does some rudimentary filtering.

[List of recommended DNS servers](../dns.md ""){.md-button}

## DNSSECとは？

[Domain Name System Security Extensions](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) (DNSSEC) is a feature of DNS that authenticates responses to domain name lookups. It does not provide privacy protections for those lookups, but rather prevents attackers from manipulating or poisoning the responses to DNS requests.

In other words, DNSSEC digitally signs data to help ensure its validity. In order to ensure a secure lookup, the signing occurs at every level in the DNS lookup process. As a result, all answers from DNS can be trusted.

The DNSSEC signing process is similar to someone signing a legal document with a pen; that person signs with a unique signature that no one else can create, and a court expert can look at that signature and verify that the document was signed by that person. These digital signatures ensure that data has not been tampered with.

DNSSEC implements a hierarchical digital signing policy across all layers of DNS. For example, in the case of a `privacyguides.org` lookup, a root DNS server would sign a key for the `.org` nameserver, and the `.org` nameserver would then sign a key for `privacyguides.org`’s authoritative nameserver.

<small>Adapted from [DNS Security Extensions (DNSSEC) overview](https://cloud.google.com/dns/docs/dnssec) by Google and [DNSSEC: An Introduction](https://blog.cloudflare.com/dnssec-an-introduction) by Cloudflare, both licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0).</small>

## What is QNAME minimization?

A QNAME is a "qualified name", for example `discuss.privacyguides.net`. In the past, when resolving a domain name your DNS resolver would ask every server in the chain to provide any information it has about your full query. In this example below, your request to find the IP address for `discuss.privacyguides.net` gets asked of every DNS server provider:

| サーバー                | 質問                                          | 回答                                   |
| ------------------- | ------------------------------------------- | ------------------------------------ |
| ルートサーバー             | What's the IP of discuss.privacyguides.net? | わかりません。.netのサーバーに聞いてみてください。          |
| .netのサーバー           | What's the IP of discuss.privacyguides.net? | わかりません、Privacy Guidesのサーバーに聞いてください…。 |
| Privacy Guidesのサーバー | What's the IP of discuss.privacyguides.net? | 5.161.195.190!                       |

With "QNAME minimization," your DNS resolver now only asks for just enough information to find the next server in the chain. In this example, the root server is only asked for enough information to find the appropriate nameserver for the .net TLD, and so on, without ever knowing the full domain you're trying to visit:

| サーバー                | 質問                                                   | 回答                                |
| ------------------- | ---------------------------------------------------- | --------------------------------- |
| ルートサーバー             | What's the nameserver for .net?                      | *Provides .net's server*          |
| .netのサーバー           | What's the nameserver for privacyguides.net?         | *Provides Privacy Guides' server* |
| Privacy Guidesのサーバー | What's the nameserver for discuss.privacyguides.net? | This server!                      |
| Privacy Guidesのサーバー | What's the IP of discuss.privacyguides.net?          | 5.161.195.190                     |

While this process can be slightly more inefficient, in this example neither the central root nameservers nor the TLD's nameservers ever receive information about your *full* query, thus reducing the amount of information being transmitted about your browsing habits. Further technical description is defined in [RFC 7816](https://datatracker.ietf.org/doc/html/rfc7816).

## What is EDNS Client Subnet (ECS)?

The [EDNS Client Subnet](https://en.wikipedia.org/wiki/EDNS_Client_Subnet) is a method for a recursive DNS resolver to specify a [subnetwork](https://en.wikipedia.org/wiki/Subnetwork) for the [host or client](https://en.wikipedia.org/wiki/Client_(computing)) which is making the DNS query.

It's intended to "speed up" delivery of data by giving the client an answer that belongs to a server that is close to them such as a [content delivery network](https://en.wikipedia.org/wiki/Content_delivery_network), which are often used in video streaming and serving JavaScript web apps.

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
