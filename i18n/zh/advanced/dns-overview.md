---
title: "DNS简介"
icon: material/dns
description: 域名系统是 “互联网的电话簿”，帮助浏览器找到网站。
---

The [Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System) is the 'phone book of the Internet'. DNS将域名转换为IP地址，以便浏览器和其他服务可以通过分散的服务器网络加载互联网资源。

## 什么是DNS？

当您访问某个网站时，系统会返回一个数字地址。 例如，当你访问 `privacyguides.org`时，会返回地址 `192.98.54.105`。

DNS自互联网的 [早期](https://en.wikipedia.org/wiki/Domain_Name_System#History) 以来一直存在。 与DNS服务器间的通讯通常是 **未** 加密的。 在家用场景下，客户通过 [DHCP](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol)获得由ISP提供的服务器。

未加密的DNS请求可能会被轻易地 **被监视** ，或者在传输过程中 **被修改**。 在世界的某些地方，Isp被要求做原始的 [DNS过滤](https://en.wikipedia.org/wiki/DNS_blocking)。 当你请求一个被封锁的域名的IP地址时，服务器可能不会回应，或可能以不同的IP地址回应。 由于DNS协议没有加密，ISP（或任何网络运营商）可以使用 [DPI](https://en.wikipedia.org/wiki/Deep_packet_inspection) 来监控请求。 ISP还可以基于共有特性阻止请求，无论使用的是哪个DNS服务器。

下面，我们将探讨并提供一个教程来验证一下外部观察者对于使用常规未加密DNS和 [加密DNS](#what-is-encrypted-dns)这两种情况下分别可能看到什么。

### 未加密DNS

1. Using [`tshark`](https://wireshark.org/docs/man-pages/tshark.html) (part of the [Wireshark](https://en.wikipedia.org/wiki/Wireshark) project) we can monitor and record internet packet flow. 此命令记录符合指定规则的数据包:

    ```bash
    tshark -w /tmp/dns.pcap udp port 53 and host 1.1.1.1 or host 8.8.8.8
    ```

2. We can then use [`dig`](https://en.wikipedia.org/wiki/Dig_(command)) (Linux, macOS, etc.) or [`nslookup`](https://en.wikipedia.org/wiki/Nslookup) (Windows) to send the DNS lookup to both servers. Web浏览器等软件会自动执行这些查找，除非它们被配置为使用加密的DNS。

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

3. Next, we want to [analyze](https://wireshark.org/docs/wsug_html_chunked/ChapterIntroduction.html#ChIntroWhatIs) the results:

    === "Wireshark"

        ```
        wireshark -r /tmp/dns.pcap
        ```

    === "tshark"

        ```
        tshark -r /tmp/dns.pcap
        ```

如果运行上面的Wireshark命令，顶部窗格显示“[帧](https://en.wikipedia.org/wiki/Ethernet_frame)” ，底部窗格显示有关所选帧的所有数据。 企业过滤和监控解决方案（如政府购买的解决方案）可以自动完成这一过程，无需人工干预，并可以汇总多帧数据以产生对网络观察者有用的统计数据。

| No. | 时间       | 来源        | 目的地       | 协议  | 长度  | 信息                                                                     |
| --- | -------- | --------- | --------- | --- | --- | ---------------------------------------------------------------------- |
| 1   | 0.000000 | 192.0.2.1 | 1.1.1.1   | 云存储 | 104 | Standard query 0x58ba A privacyguides.org OPT                          |
| 2   | 0.293395 | 1.1.1.1   | 192.0.2.1 | 云存储 | 108 | Standard query response 0x58ba A privacyguides.org A 198.98.54.105 OPT |
| 3   | 1.682109 | 192.0.2.1 | 8.8.8.8   | 云存储 | 104 | Standard query 0xf1a9 A privacyguides.org OPT                          |
| 4   | 2.154698 | 8.8.8.8   | 192.0.2.1 | 云存储 | 108 | Standard query response 0xf1a9 A privacyguides.org A 198.98.54.105 OPT |

观察者可以修改这些数据包中的任何一个。

## 什么是“加密DNS” ？

Encrypted DNS can refer to one of a number of protocols, the most common ones being [DNSCrypt](#dnscrypt), [DNS over TLS](#dns-over-tls-dot), and [DNS over HTTPS](#dns-over-https-doh).

### DNSCrypt

[**DNSCrypt**](https://en.wikipedia.org/wiki/DNSCrypt) 是首批加密DNS查询的方法之一。 DNSCrypt在端口443上运行，并可以使用TCP或UDP传输协议。 DNSCrypt has never been submitted to the [Internet Engineering Task Force (IETF)](https://en.wikipedia.org/wiki/Internet_Engineering_Task_Force) nor has it gone through the [Request for Comments (RFC)](https://en.wikipedia.org/wiki/Request_for_Comments) process, so it has not been used widely outside a few [implementations](https://dnscrypt.info/implementations). 因此，它在很大程度上被更流行的 [DNS over HTTPS](#dns-over-https-doh)取代了。

### DNS over TLS (DoT)

[**DNS over TLS**](https://en.wikipedia.org/wiki/DNS_over_TLS) 是另一种加密DNS通信的方法，在 [RFC 7858](https://datatracker.ietf.org/doc/html/rfc7858)中被定义。 Support was first implemented in Android 9, iOS 14, and on Linux in [systemd-resolved](https://freedesktop.org/software/systemd/man/resolved.conf.html#DNSOverTLS=) in version 237. Preference in the industry has been moving away from DoT to DoH in recent years, as DoT is a [complex protocol](https://dnscrypt.info/faq) and has varying compliance to the RFC across the implementations that exist. DoT也在一个专用的853端口上运行，该端口很容易被限制性的防火墙阻断。

### DNS over HTTPS (DoH)

[**DNS over HTTPS**](https://en.wikipedia.org/wiki/DNS_over_HTTPS), as defined in [RFC 8484](https://datatracker.ietf.org/doc/html/rfc8484), packages queries in the [HTTP/2](https://en.wikipedia.org/wiki/HTTP/2) protocol and provides security with HTTPS. 由Firefox 60和Chrome 83等Web浏览器首次实现支持。

DoH的原生实现出现在iOS 14、macOS 11、微软Windows和Android 13中（然而，它不会被默认启用 [](https://android-review.googlesource.com/c/platform/packages/modules/DnsResolver/+/1833144)）。 一般的Linux桌面支持还在等待systemd [实现](https://github.com/systemd/systemd/issues/8639) ，所以 [目前依然需要安装第三方软件](../dns.md#linux)。

### Native Operating System Support

#### Android

安卓9及以上系统支持通过TLS的DNS。 这些设置可以在下面找到。 **设置** &rarr; **网络 & 互联网** &rarr; **私人DNS**。

#### Apple Devices

最新版本的iOS、iPadOS、tvOS和macOS，同时支持DoT和DoH。 通过 [配置文件](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) ，或通过 [DNS设置API](https://developer.apple.com/documentation/networkextension/dns_settings)，这两种协议都得到了本地支持。

在安装配置文件或使用DNS设置API的应用程序后，可以选择DNS配置。 如果VPN处于激活状态，在VPN隧道内的解析将使用VPN的DNS设置，而不是你整个系统的设置。

苹果公司没有为创建加密的DNS配置文件提供本地接口。 [安全DNS配置文件创建者](https://dns.notjakob.com/tool.html) 是一个非官方的工具，用于创建你自己的加密DNS配置文件，然而它们将不会被签署。 签名的档案是首选；签名验证了档案的来源，有助于确保档案的完整性。 绿色的 "已验证 "标签被赋予已签署的配置文件。 关于代码签名的更多信息，见 [关于代码签名](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html)。

#### Linux系统

`systemd-resolved`, which many Linux distributions use to do their DNS lookups, doesn't yet [support DoH](https://github.com/systemd/systemd/issues/8639). If you want to use DoH, you'll need to install a proxy like [dnscrypt-proxy](../dns.md#dnscrypt-proxy) and [configure it](https://wiki.archlinux.org/title/Dnscrypt-proxy) to take all the DNS queries from your system resolver and forward them over HTTPS.

## 外部一方能看到什么？

在本示例中，我们将记录当我们提出DoH请求时会发生什么：

1. 首先，启动 `tshark`。

    ```bash
    tshark -w /tmp/dns_doh.pcap -f "tcp port https and host 1.1.1.1"
    ```

2. 其次，使用 `curl`提出请求：

    ```bash
    curl -vI --doh-url https://1.1.1.1/dns-query https://privacyguides.org
    ```

3. 在提出请求后，我们可以用 <kbd>CTRL</kbd> + <kbd>C</kbd>停止抓包。

4. Analyze the results in Wireshark:

    ```bash
    wireshark -r /tmp/dns_doh.pcap
    ```

We can see the [connection establishment](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#Connection_establishment) and [TLS handshake](https://cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake) that occurs with any encrypted connection. 当查看下面的“应用程序数据”数据包时，没有一个数据包包含我们请求的域或返回的IP地址。

## 为什么我**不应该** 使用加密的DNS？

在有互联网过滤（或审查）的地方，访问被禁止的资源可能会有自己的后果，你应该在你的 [威胁模型](../basics/threat-modeling.md)。 我们 **不** 建议为此目的使用加密的DNS。 Use [Tor](../advanced/tor-overview.md) or a [VPN](../vpn.md) instead. 如果您使用的是VPN ，则应使用VPN的DNS服务器。 使用VPN时，您已经信任它们的所有网络活动。

当我们进行DNS查找时，通常是因为我们想要访问资源。 下面，我们将讨论一些即使在使用加密的DNS时也可能泄露你的浏览活动的方法。

### IP 地址

确定浏览活动的最简单方法可能是查看你的设备所访问的IP地址。 例如，如果观察者知道 `privacyguides.org` 在 `198.98.54.105`，而你的设备正在从 `198.98.54.105`请求数据，你很有可能正在访问隐私指南。

这种方法只有在IP地址属于一个只承载少数网站的服务器时才有用。 It's also not very useful if the site is hosted on a shared platform (e.g. GitHub Pages, Cloudflare Pages, Netlify, WordPress, Blogger, etc.). 如果服务器托管在一个 [反向代理](https://en.wikipedia.org/wiki/Reverse_proxy)，它也不是很有用，这在现代互联网上非常普遍。

### 服务器名称指示（SNI）

Server Name Indication is typically used when an IP address hosts many websites. 这可能是一个像Cloudflare这样的服务，或其他一些 [拒绝服务攻击](https://en.wikipedia.org/wiki/Denial-of-service_attack) 保护。

1. 再次开始捕获 `tshark`。 We've added a filter with our IP address, so you don't capture many packets:

    ```bash
    tshark -w /tmp/pg.pcap port 443 and host 198.98.54.105
    ```

2. 然后我们访问 [https://privacyguides.org](https://privacyguides.org)。

3. 访问完网站后，我们要用 <kbd>CTRL</kbd> + <kbd>C</kbd>停止抓包。

4. 接下来我们要分析结果：

    ```bash
    wireshark -r /tmp/pg.pcap
    ```

    我们将看到连接的建立，然后是隐私指南网站的TLS握手。 第5帧左右。 你会看到一个 "Client Hello"。

5. 展开每个字段旁边的三角形 &#9656;。

    ```text
    ▸ Transport Layer Security
      ▸ TLSv1.3 Record Layer: Handshake Protocol: Client Hello
        ▸ Handshake Protocol: Client Hello
          ▸ Extension: server_name (len=22)
            ▸ Server Name Indication extension
    ```

6. 我们可以看到SNI值，它披露了我们正在访问的网站。 `tshark` 命令可以直接给你包含SNI值的所有数据包的值。

    ```bash
    tshark -r /tmp/pg.pcap -Tfields -Y tls.handshake.extensions_server_name -e tls.handshake.extensions_server_name
    ```

这意味着即使我们使用 "加密DNS "服务器，域名也可能通过SNI被披露。 The [TLS v1.3](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_1.3) protocol brings with it [Encrypted Client Hello](https://blog.cloudflare.com/encrypted-client-hello), which prevents this kind of leak.

Governments, in particular [China](https://zdnet.com/article/china-is-now-blocking-all-encrypted-https-traffic-using-tls-1-3-and-esni) and [Russia](https://zdnet.com/article/russia-wants-to-ban-the-use-of-secure-protocols-such-as-tls-1-3-doh-dot-esni), have either already [started blocking](https://en.wikipedia.org/wiki/Server_Name_Indication#Encrypted_Client_Hello) it or expressed a desire to do so. [最近，俄罗斯开始封锁使用 [HTTP/3](https://en.wikipedia.org/wiki/HTTP/3) 标准的外国网站](https://github.com/net4people/bbs/issues/108)。 这是因为作为HTTP/3一部分的 [QUIC](https://en.wikipedia.org/wiki/QUIC) 协议要求 `ClientHello` 也被加密。

### 在线证书状态协议（OCSP）

你的浏览器披露你的浏览活动的另一种方式是通过 [在线证书状态协议](https://en.wikipedia.org/wiki/Online_Certificate_Status_Protocol)。 当访问一个HTTPS网站时，浏览器可能会检查该网站的 [证书](https://en.wikipedia.org/wiki/Public_key_certificate) 是否已被撤销。 这通常是通过HTTP协议完成的，这意味着它是 **，而不是** 加密的。

该OCSP请求包含证书"[序列号](https://en.wikipedia.org/wiki/Public_key_certificate#Common_fields)"，该证书是唯一的。 它被发送到 "OCSP响应者"，以检查其状态。

我们可以使用 [`openssl`](https://en.wikipedia.org/wiki/OpenSSL) 命令来模拟浏览器会做什么。

1. 获取服务器证书，并使用 [`sed`](https://en.wikipedia.org/wiki/Sed) ，只保留重要部分，并将其写入文件。

    ```bash
    openssl s_client -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_server.cert
    ```

2. 获得中间证书。 [证书颁发机构（CA）](https://en.wikipedia.org/wiki/Certificate_authority) ，通常不直接签署证书；他们使用所谓的 "中间 "证书。

    ```bash
    openssl s_client -showcerts -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_and_intermediate.cert
    ```

3. `pg_and_intermediate.cert` 中的第一个证书实际上是步骤1中的服务器证书。 我们可以再次使用 `sed` ，删除直到END的第一个实例。

    ```bash
    sed -n '/^-*END CERTIFICATE-*$/!d;:a n;p;ba' \
        /tmp/pg_and_intermediate.cert > /tmp/intermediate_chain.cert
    ```

4. 获取服务器证书的OCSP应答器。

    ```bash
    openssl x509 -noout -ocsp_uri -in /tmp/pg_server.cert
    ```

    我们的证书显示的是Lets Encrypt证书响应者。 如果我们想查看证书的所有详细信息，我们可以使用：

    ```bash
    openssl x509 -text -noout -in /tmp/pg_server.cert
    ```

5. 开始捕获数据包。

    ```bash
    tshark -w /tmp/pg_ocsp.pcap -f "tcp port http"
    ```

6. 提出OCSP请求。

    ```bash
    openssl ocsp -issuer /tmp/intermediate_chain.cert \
                 -cert /tmp/pg_server.cert \
                 -text \
                 -url http://r3.o.lencr.org
    ```

7. 打开捕获。

    ```bash
    wireshark -r /tmp/pg_ocsp.pcap
    ```

    在 "OCSP "协议中会有两个数据包：一个 "请求 "和一个 "响应"。 对于 "请求"，我们可以通过展开每个字段旁边的三角形 &#9656; ，看到 "序列号"。

    ```bash
    ▸ Online Certificate Status Protocol
      ▸ tbsRequest
        ▸ requestList: 1 item
          ▸ Request
            ▸ reqCert
              serialNumber
    ```

    对于 "回应"，我们也可以看到 "序列号"。

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

8. 或者使用 `tshark` 来过滤序列号的数据包。

    ```bash
    tshark -r /tmp/pg_ocsp.pcap -Tfields -Y ocsp.serialNumber -e ocsp.serialNumber
    ```

如果网络观察者拥有公开的公共证书，他们可以将序列号与该证书相匹配，从而从中确定你所访问的网站。 这个过程可以自动化，并能将IP地址与序列号联系起来。 也可以检查 [证书透明度](https://en.wikipedia.org/wiki/Certificate_Transparency) 日志中的序列号。

## 我应该使用加密的DNS吗？

我们做了这个流程图来描述你什么时候 *应该* 使用加密的DNS。

``` mermaid
图TB
    开始[Start] --> 匿名{尝试<br> 匿名？}
    anonymous--> | Yes | tor(使用Tor)
    anonymous--> | No | censorship{Avoiding<br> censorship?｝
    审查 --> | 是 | vpnOrTor(使用<br> VPN或Tor)
    审查 --> | 不 | 隐私{想从ISP那里获得隐私<br>？}。
    privacy --> | Yes | vpnOrTor
    privacy --> | No | obnoxious{ISP使<br> obnoxious<br> redirects? }
    obnoxious --> | Yes | encryptedDNS(使用第三方的<br> 加密DNS<br> )
    obnoxious --> | No | ispDNS{ISP是否支持<br> 加密DNS？ }
    ispDNS --> | 是 | useISP(与ISP一起使用<br> 加密DNS<br> )
    ispDNS --> | 否 | nothing(什么都不做)
```

Encrypted DNS with a third party should only be used to get around redirects and basic [DNS blocking](https://en.wikipedia.org/wiki/DNS_blocking) when you can be sure there won't be any consequences, or you're interested in a provider that does some rudimentary filtering.

[推荐的DNS服务器列表](../dns.md ""){.md-button}

## 什么是DNSSEC？

[域名系统安全扩展](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) (DNSSEC)是DNS的一项功能，对域名查询的响应进行认证。 它不为这些查询提供隐私保护，而是防止攻击者操纵或毒害对DNS请求的响应。

换句话说，DNSSEC对数据进行数字签名，以帮助确保其有效性。 为了确保安全查询，签名发生在DNS查询过程中的每一级。 因此，来自DNS的所有答案都可以被信任。

DNSSEC的签署过程类似于某人用笔签署一份法律文件；该人用一个独特的签名签署，其他人无法创建，法院专家可以查看该签名并验证该文件是由该人签署的。 这些数字签名确保数据没有被篡改。

DNSSEC在DNS的所有层面上实现了分层的数字签名政策。 例如，在 `privacyguides.org` 查询的情况下，根 DNS 服务器将签署 `.org` 名称服务器的密钥，然后 `.org` 名称服务器将签署 `privacyguides.org`的权威名称服务器的密钥。

<small>Adapted from [DNS Security Extensions (DNSSEC) overview](https://cloud.google.com/dns/docs/dnssec) by Google and [DNSSEC: An Introduction](https://blog.cloudflare.com/dnssec-an-introduction) by Cloudflare, both licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0).</small>

## 什么是QNAME最小化？

合法名是一个 “合法的名字”，例如 `discuss.privacyguides.net`。 过去，在解析域名时，DNS 解析器会要求链中的每台服务器提供有关您完整查询的任何信息。 在下面的示例中，您请求查找 `discuss.privacyguides.net` 的 IP 地址时会向每个 DNS 服务器提供商提出请求：

| 服务器                 | 询问                                    | 响应                            |
| ------------------- | ------------------------------------- | ----------------------------- |
| 根服务器                | discuss.privacyguides.net 的 IP 地址是什么？ | 我不知道，问 .net 的服务器...           |
| .net 的服务器           | discuss.privacyguides.net 的 IP 地址是什么？ | 我不知道，问 Privacy Guides 的服务器... |
| Privacy Guides 的服务器 | discuss.privacyguides.net 的 IP 地址是什么？ | 5.161.195.190!                |

有了 “QNAME 最小化” 技术，DNS 解析器现在只请求能够找到链中的下一个服务器的信息。 在这个例子中，根服务器只要求提供足够的信息，以便能够找到 .net TLD 的名称服务器，以此类推，而不会知道您要访问的完整域名：

| 服务器                 | 询问                                    | 响应                       |
| ------------------- | ------------------------------------- | ------------------------ |
| 根服务器                | .net 的名称服务器是什么？                       | *提供 .net 的服务器*           |
| .net 的服务器           | privacyguides.net 的名称服务器是什么？          | *提供 Privacy Guides 的服务器* |
| Privacy Guides 的服务器 | discuss.privacyguides.net 的名称服务器是什么？  | 就是此服务器！                  |
| Privacy Guides 的服务器 | discuss.privacyguides.net 的 IP 地址是什么？ | 5.161.195.190            |

虽然这个过程的效率会稍低一些，但在这个例子中，中央根域名服务器和顶级域名的域名服务器都不会收到您的 *完整* 查询的信息，从而减少了有关您的浏览习惯的信息传输量。 进一步的技术描述在 [RFC 7816](https://datatracker.ietf.org/doc/html/rfc7816)中定义。

## 什么是EDNS客户子网（ECS）？

[EDNS 客户端子网](https://en.wikipedia.org/wiki/EDNS_Client_Subnet) 是递归 DNS 解析器为 [主机或客户端](https://en.wikipedia.org/wiki/Client_(computing)) 进行 DNS 查询时，指定一个 [子网](https://en.wikipedia.org/wiki/Subnetwork) 的一种方法。

它的目的是 "加快 "数据的交付，给客户一个属于离他们很近的服务器的答案，如 [内容交付网络](https://en.wikipedia.org/wiki/Content_delivery_network)，这通常用于视频流和服务JavaScript网络应用。

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
