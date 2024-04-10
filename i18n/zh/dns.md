---
title: "DNS解析器"
icon: material/dns
description: These are some encrypted DNS providers we recommend switching to, to replace your ISP's default configuration.
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

Encrypted DNS with third-party servers should only be used to get around basic [DNS blocking](https://en.wikipedia.org/wiki/DNS_blocking) when you can be sure there won't be any consequences. 加密的DNS不会帮助你隐藏任何浏览活动。

[Learn more about DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## 推荐的供应商

These are our favorite public DNS resolvers based on their privacy and security characteristics, and their worldwide performance. Some of these services offer basic DNS-level blocking of malware or trackers depending on the server you choose, but if you want to be able to see and customize what is blocked you should use a dedicated DNS filtering product instead.

| DNS供应商                                                                     | 隐私政策                                                                                                 | 协议                                       | 日志记录     | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | 筛选                                                                                                                  | Signed Apple Profile                                                                                                     |
| -------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------- | -------- | -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| [**AdGuard Public DNS**](https://adguard-dns.io/en/public-dns.html)        | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                               | Cleartext   DoH/3   DoT   DoQ   DNSCrypt | 一些[^1]   | Anonymized                                                     | Based on server choice. 正在使用的过滤器列表可以在这里找到。 [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) | Yes [:octicons-link-external-24:](https://adguard.com/en/blog/encrypted-dns-ios-14.html)                                 |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) | Cleartext   DoH/3   DoT                  | 一些[^2]   | No                                                             | Based on server choice.                                                                                             | No [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846) |
| [**Control D Free DNS**](https://controld.com/free-dns)                    | [:octicons-link-external-24:](https://controld.com/privacy)                                          | Cleartext   DoH/3   DoT   DoQ            | 可选[^3]   | No                                                             | Based on server choice.                                                                                             | Yes [:octicons-link-external-24:](https://docs.controld.com/docs/macos-platform)                                         |
| [**dns0.eu**](https://dns0.eu)                                             | [:octicons-link-external-24:](https://dns0.eu/privacy)                                               | Cleartext   DoH/3   DoH   DoT   DoQ      | No       | Anonymized                                                     | Based on server choice.                                                                                             | Yes [:octicons-link-external-24:](https://dns0.eu/zero.dns0.eu.mobileconfig)                                             |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy)                    | DoH   DoT                                | No[^4]   | No                                                             | Based on server choice. 正在使用的过滤器列表可以在这里找到。 [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    | Yes [:octicons-link-external-24:](https://mullvad.net/en/blog/profiles-to-configure-our-encrypted-dns-on-apple-devices)  |
| [**Quad9**](https://quad9.net)                                             | [:octicons-link-external-24:](https://quad9.net/privacy/policy)                                      | Cleartext   DoH   DoT   DNSCrypt         | Some[^5] | 可选                                                             | Based on server choice, malware blocking by default.                                                                | Yes [:octicons-link-external-24:](https://quad9.net/news/blog/ios-mobile-provisioning-profiles)                          |

## Self-Hosted DNS Filtering

自我托管的DNS解决方案对于在智能电视和其他物联网设备等受控平台上提供过滤非常有用，因为不需要客户端软件。

### Pi-hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](assets/img/dns/pi-hole.svg){ align=right }

**Pi-hole** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

Pi-hole被设计为在Raspberry Pi上托管，但它并不局限于这种硬件。 该软件具有一个友好的网络界面，可以查看洞察力和管理封锁的内容。

[:octicons-home-16: Homepage](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Source Code" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title=Contribute }

</details>

</div>

### AdGuard Home

<div class="admonition recommendation" markdown>

![AdGuard Home logo](assets/img/dns/adguard-home.svg){ align=right }

**AdGuard Home** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

AdGuard Home有一个精致的网络界面，可以查看洞察力和管理被阻止的内容。

[:octicons-home-16: 主页](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="隐私政策" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=文档}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="源代码" }

</details>

</div>

## Cloud-Based DNS Filtering

These DNS filtering solutions offer a web dashboard where you can customize the blocklists to your exact needs, similarly to a Pi-hole. These services are usually easier to set up and configure than self-hosted services like the ones above, and can be used more easily across multiple networks (self-hosted solutions are typically restricted to your home/local network unless you set up a more advanced configuration).

### Control D

<div class="admonition recommendation" markdown>

![Control D logo](assets/img/dns/control-d.svg){ align=right }

**Control D** is a customizable DNS service which lets you block security threats, unwanted content, and advertisements on a DNS level. In addition to their paid plans, they offer a number of preconfigured DNS resolvers you can use for free.

[:octicons-home-16: Homepage](https://controld.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://controld.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.controld.com/docs/getting-started){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/Control-D-Inc/ctrld){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-apple: macOS](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-linux: Linux](https://docs.controld.com/docs/ctrld)
- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.controld.setuputility)
- [:simple-appstore: App Store](https://apps.apple.com/app/1518799460)
- [:simple-github: GitHub](https://github.com/Control-D-Inc/ctrld/releases/tag/v1.3.5)

</details>

</div>

### NextDNS

<div class="admonition recommendation" markdown>

![NextDNS logo](assets/img/dns/nextdns.svg){ align=right }

**NextDNS** is a customizable DNS service which lets you block security threats, unwanted content, and advertisements on a DNS level. They offer a fully functional free plan for limited use.

[:octicons-home-16: Homepage](https://nextdns.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextdns.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.nextdns.io){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/nextdns/nextdns){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://github.com/nextdns/nextdns/wiki/Windows)
- [:simple-apple: macOS](https://apps.apple.com/us/app/nextdns/id1464122853)
- [:simple-linux: Linux](https://github.com/nextdns/nextdns/wiki)
- [:simple-appstore: App Store](https://apps.apple.com/app/nextdns/id1463342498)
- [:simple-github: GitHub](https://github.com/nextdns/nextdns/releases)

</details>

</div>

When used with an account, NextDNS will enable insights and logging features by default (as some features require it). You can choose retention time and log storage location for any logs you choose to keep, or disable logs altogether.

NextDNS's free plan is fully functional, but should not be relied upon for security or other critical filtering applications, because after 300,000 DNS queries in a month all filtering, logging, and other account-based functionality is disabled. It can still be used as a regular DNS provider after that point, so your devices will continue to function and make secure queries via DNS-over-HTTPS, just without your filter lists.

NextDNS also offers public DNS-over-HTTPS service at `https://dns.nextdns.io` and DNS-over-TLS/QUIC at `dns.nextdns.io`, which are available by default in Firefox and Chromium, and subject to their default no-logging [privacy policy](https://nextdns.io/privacy).

## Encrypted DNS Proxies

加密的DNS代理软件为 [未加密的DNS](advanced/dns-overview.md#unencrypted-dns) 解析器提供一个本地代理转发。 Typically, it is used on platforms that don't natively support [encrypted DNS](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ align=right }
![RethinkDNS标志](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS**是一个开源的Android客户端，支持 [DNS-over-HTTPS]（advanced/dns-overview.md#dns-over-https-doh）、 [DNS-over-TLS]（advanced/dns-overview.md#dns-over-tls-dot）、 [DNSCrypt]（advanced/dns-overview.md#dnscrypt）和DNS Proxy，同时还可以缓存DNS响应，本地记录DNS查询，也可以作为防火墙使用。

[:octicons-home-16: Homepage](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

### dnscrypt-proxy

<div class="admonition recommendation" markdown>

![dnscrypt-proxy logo](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**dnscrypt-proxy** is a DNS proxy with support for [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), and [Anonymized DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

[:octicons-repo-16: Repository](https://github.com/DNSCrypt/dnscrypt-proxy){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

The anonymized DNS feature does [not](advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns) anonymize other network traffic.

</div>

## Criteria

**请注意，我们与我们推荐的任何项目都没有关系。** 除了 [我们的标准标准](about/criteria.md)，我们还制定了一套明确的要求，使我们能够提供客观的建议。 我们建议你在选择使用一个项目之前熟悉这个清单，并进行自己的研究以确保它是你的正确选择。

### Minimum Requirements

- [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- [QNAME最小化](advanced/dns-overview.md#what-is-qname-minimization).
- Anonymize [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) or disable it by default.
- 倾向于 [anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) 支持或地理转向支持。

[^1]: AdGuard存储其DNS服务器的汇总性能指标，即对特定服务器的完整请求数、被阻止的请求数和处理请求的速度。 他们还保留并存储了过去24小时内请求的域名数据库。 "我们需要这些信息来识别和阻止新的追踪者和威胁。" "我们还记录了这个或那个追踪器被封锁的次数。 我们需要这些信息来从我们的过滤器中删除过时的规则"。 [https://adguard.com/en/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: Cloudflare只收集和存储发送到1.1.1.1解析器的有限DNS查询数据。 1.1.1.1解析器服务不记录个人数据，而且大部分有限的非个人识别的查询数据只存储25小时。 [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: Control D只记录具有自定义DNS配置文件的高级解析器。 自由解析器不记录数据。 [https://controld.com/privacy](https://controld.com/privacy)
[^4]: Mullvad的DNS服务对Mullvad VPN的订阅者和非订阅者都适用。 他们的隐私政策明确声称他们不会以任何方式记录DNS请求。 [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^5]: Quad9收集了一些数据，用于威胁监测和应对。 然后，这些数据可能被重新混合和共享，例如为了安全研究的目的。 Quad9不会收集或记录IP地址或其他他们认为可以识别个人身份的数据。 [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
