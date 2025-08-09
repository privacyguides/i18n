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

ブラウザがブラウジングアクティビティを開示し得る、別の方法は[Online Certificate Status Protocol](https://en.wikipedia.org/wiki/Online_Certificate_Status_Protocol)が挙げられます。 HTTPSのウェブサイトにアクセスする際、ブラウザはウェブサイトの[証明書](https://en.wikipedia.org/wiki/Public_key_certificate)が失効していないか確認することがあります。 通常はHTTPプロトコル経由で行われ、暗号化**されていません**。

OCSPリクエストには一意な証明書の[シリアル番号](https://en.wikipedia.org/wiki/Public_key_certificate#Common_fields)が含まれています。 その状態を確認するため「OCSPレスポンダー」に送られます。

ブラウザの動作を[`openssl`](https://en.wikipedia.org/wiki/OpenSSL)コマンドでシミュレートすることができます。

1. サーバーの証明書を取得し、[`sed`](https://en.wikipedia.org/wiki/Sed)コマンドで重要な部分を残し、ファイルに書き出します：

    ```bash
    openssl s_client -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_server.cert
    ```

2. 中間証明書を取得。 [認証局（CA）](https://en.wikipedia.org/wiki/Certificate_authority)は通常、証明書に直接署名せず、「中間」証明書を使います。

    ```bash
    openssl s_client -showcerts -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_and_intermediate.cert
    ```

3. `pg_and_intermediate.cert`の最初の証明書は実際にはStep1のサーバー証明書です。 `sed`で最初のENDまでを削除します：

    ```bash
    sed -n '/^-*END CERTIFICATE-*$/!d;:a n;p;ba' \
        /tmp/pg_and_intermediate.cert > /tmp/intermediate_chain.cert
    ```

4. サーバー証明書のOCSPレスポンダーを取得します：

    ```bash
    openssl x509 -noout -ocsp_uri -in /tmp/pg_server.cert
    ```

    Privacy Guidesの証明書はLet's Encryptの証明書レスポンダーを示しています。 証明書の詳細をすべて確認する場合、以下のコマンドを実行します：

    ```bash
    openssl x509 -text -noout -in /tmp/pg_server.cert
    ```

5. パケットキャプチャを開始します：

    ```bash
    tshark -w /tmp/pg_ocsp.pcap -f "tcp port http"
    ```

6. OCSPリクエストを行います：

    ```bash
    openssl ocsp -issuer /tmp/intermediate_chain.cert \
                 -cert /tmp/pg_server.cert \
                 -text \
                 -url http://r3.o.lencr.org
    ```

7. キャプチャの内容を確認します：

    ```bash
    wireshark -r /tmp/pg_ocsp.pcap
    ```

    「OCSP」プロトコルには「Request」と「Response」の２つのパケットがあります。 「Request」については、各フィールドの隣にある三角形&#9656;を展開することで「シリアル番号」を確認することができます：

    ```bash
    ▸ Online Certificate Status Protocol
      ▸ tbsRequest
        ▸ requestList: 1 item
          ▸ Request
            ▸ reqCert
              serialNumber
    ```

    「Response」についても「シリアル番号」を確認することができます：

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

8. また、`tshark`でシリアル番号のパケットをフィルタすることもできます：

    ```bash
    tshark -r /tmp/pg_ocsp.pcap -Tfields -Y ocsp.serialNumber -e ocsp.serialNumber
    ```

ネットワークの監視者が一般的に公開されているパブリック証明書を持っていれば、シリアル番号と証明書を照合することで、訪問しているサイトを特定することができます。 このプロセスは自動化することができ、IPアドレスとシリアル番号を関連付けることができます。 また、[証明書の透明性](https://en.wikipedia.org/wiki/Certificate_Transparency)のログからシリアル番号を確認することもできます。

## 暗号化DNSを使うべきか？

暗号化DNSを使う*べき*かというフローチャートは以下のとおりです：

``` mermaid
graph TB
    Start[スタート] --> anonymous{匿名化する<br>必要がある？}
    anonymous--> | はい | tor(Torを使う)
    anonymous --> | いいえ | censorship{検閲を<br>避ける？}
    censorship --> | はい | vpnOrTor(VPNやTor<br>を使う)
    censorship --> | いいえ | privacy{ISPから<br>プライバシーを守りたい？}
    privacy --> | はい | vpnOrTor
    privacy --> | いいえ | obnoxious{ISPが不快な<br>リダイレクトをする？}
    obnoxious --> | はい | encryptedDNS(第三者の<br>暗号化DNS<br>を使う)
    obnoxious --> | いいえ | ispDNS{ISPが暗号化DNS<br>に対応している？}
    ispDNS --> | はい | useISP(ISPの<br>暗号化DNS<br>を使う)
    ispDNS --> | いいえ | nothing(何もしない)
```

第三者の暗号化DNSはリダイレクトや基本的な[DNSブロッキング](https://en.wikipedia.org/wiki/DNS_blocking)を回避するため、もしくは初歩的なフィルタリングをするプロバイダに興味がある場合にのみ使うべきです。

[推奨するDNSサーバーのリスト](../dns.md ""){.md-button}

## DNSSECとは？

[DNS Security Extensions](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions)（DNSSEC）はドメイン名検索に対する応答を認証するDNSの機能です。 検索に対してプライバシー保護を行うものではなく、 攻撃者がDNSリクエストに対する応答を操作したり、ポイズニングしたりすることを防ぐものです。

言い換えれば、DNSSECはデータの正当性を保証するために、データにデジタル署名を行うものです。 安全な検索を保証するため、DNSルックアップのプロセスの各レベルで署名が行われます。 その結果、DNSからのすべての応答を信頼することができます。

DNSSECの署名プロセスは法的文書にペンで署名することに似ています。ある人は他の人が作成できない固有の署名をし、裁判所の専門家はその署名を見て、文書がその人によって署名されたことを検証します。 デジタル署名はデータが改ざんされていないことを保証します。

DNSSECはDNSのすべてのレイヤーにわたり、階層的なデジタル署名ポリシーを実装しています。 例えば、`privacyguides.org`を検索する場合、ルートDNSサーバーは`.org`ネームサーバーの鍵に署名し、`.org`ネームサーバーは`privacyguides.org`の権威ネームサーバーの鍵に署名します。

<small>Googleの[DNS Security Extensions（DNSSEC）の概要](https://cloud.google.com/dns/docs/dnssec)およびCloudflareの[DNSSEC: An Introduction](https://blog.cloudflare.com/dnssec-an-introduction)を引用しています。両方とも[CC BY 4.0](https://creativecommons.org/licenses/by/4.0)の下でライセンスされています。</small>

## QNAME minimizationとは？

QNAMEは「修飾名」のことで、例えば`discuss.privacyguides.net`のようなものです。 以前はドメイン名を解決する際、DNSリゾルバーはチェーン内のすべてのサーバーに完全なクエリに関する情報を問い合わせていました。 以下の例では、`discuss.privacyguides.net`のIPアドレスを見つけるリクエストはすべてのDNSサーバープロバイダーに問い合わせをします：

| サーバー                | 質問                                     | 回答                                   |
| ------------------- | -------------------------------------- | ------------------------------------ |
| ルートサーバー             | discuss.privacyguides.netのIPアドレスは何ですか？ | わかりません。.netのサーバーに聞いてみてください。          |
| .netのサーバー           | discuss.privacyguides.netのIPアドレスは何ですか？ | わかりません、Privacy Guidesのサーバーに聞いてください…。 |
| Privacy Guidesのサーバー | discuss.privacyguides.netのIPアドレスは何ですか？ | 5.161.195.190!                       |

「QNAME minimization」によって、DNSリゾルバーはチェーンの次のサーバーを見つけるのに十分な情報のみ問い合わせます。 以下の例では、ルートサーバーは訪問先サイトの完全なドメインを知ることなく、.net TLDの適切なネームサーバーを見つけるのに十分な情報のみ問い合わせされます：

| サーバー                | 質問                                      | 回答                         |
| ------------------- | --------------------------------------- | -------------------------- |
| ルートサーバー             | .netのネームサーバーは何ですか？                      | *.netのサーバー情報を提供*           |
| .netのサーバー           | privacyguides.netのネームサーバーは何ですか？         | *Privacy Guidesのサーバー情報を提供* |
| Privacy Guidesのサーバー | discuss.privacyguides.netのネームサーバーは何ですか？ | このサーバーです！                  |
| Privacy Guidesのサーバー | discuss.privacyguides.netのIPアドレスは何ですか？  | 5.161.195.190              |

このプロセスは少し非効率になりますが、上記の例では中央のルートネームサーバーもTLDのネームサーバーも*完全な*クエリ情報を受け取らないため、ブラウジング習慣の情報送信を減らすことができます。 技術的な説明は[RFC 7816](https://datatracker.ietf.org/doc/html/rfc7816)で定義されています。

## EDNS Client Subnet（ECS）とは？

[EDNS Client Subnet](https://en.wikipedia.org/wiki/EDNS_Client_Subnet)はDNSクエリを行う[ホストもしくはクライアント](https://en.wikipedia.org/wiki/Client_(computing))の[サブネットワーク](https://en.wikipedia.org/wiki/Subnetwork)を再帰的DNSリゾルバーのために指定する方法のことです。

[コンテンツデリバリネットワーク](https://en.wikipedia.org/wiki/Content_delivery_network)のようなクライアントに近いサーバーをクライアントに回答することで、データ配信の「高速化」を意図しています。ビデオストリーミングやJavaScriptウェブアプリの配信でよく使われています。

この機能ではDNSサーバーにクライアントの位置情報（一般的にはIPネットワーク）を伝えるため、プライバシーのコストが発生します。 例えば、IPアドレスが`198.51.100.32`の場合、DNSプロバイダーは`198.51.100.0/24`の情報を権威サーバーと共有する可能性があります。 DNSプロバイダーによっては、この情報を匿名化するため、ほぼ近くの場所の別のIPアドレスを伝えます。

`dig`がインストールされていれば、以下のコマンドでDNSプロバイダーがEDNS情報をDNSネームサーバーに提供しているか確認できます：

```bash
dig +nocmd -t txt o-o.myaddr.l.google.com +nocomments +noall +answer +stats
```

このコマンドはGoogleと通信し、IPアドレスとEDNSクライアントのサブネット情報が返ってくることに注意してください。 別のDNSリゾルバーで試したい場合は、そのIPを指定します。例えば`9.9.9.11`の場合は以下の通りです：

```bash
dig +nocmd @9.9.9.11 -t txt o-o.myaddr.l.google.com +nocomments +noall +answer +stats
```

（以下のように）2番目のedns0-client-subnet TXTレコードがあれば、DNSサーバーはEDNS情報を伝えています。 後に表示されるIPやネットワークは、DNSプロバイダーがGoogleと共有した詳細な情報です。

```text
o-o.myaddr.l.google.com. 60 IN TXT "198.51.100.32"
o-o.myaddr.l.google.com. 60 IN TXT "edns0-client-subnet 198.51.100.0/24"
;; Query time: 64 msec
;; SERVER: 9.9.9.11#53(9.9.9.11)
;; WHEN: Wed Mar 13 10:23:08 CDT 2024
;; MSG SIZE  rcvd: 130
```
