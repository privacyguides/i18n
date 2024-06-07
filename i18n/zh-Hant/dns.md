---
title: "DNS解析器"
icon: material/dns
description: 我們建議切換到這些加密 DNS 提供商，以取代您 ISP 所預設的配置。
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

使用第三方伺服器的加密 DNS 只能避開基本的 [DNS 封鎖](https://en.wikipedia.org/wiki/DNS_blocking) ，當您確定不會有不良後果時。 加密的 DNS 無法為您隱藏瀏覽活動。

[了解更多 DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## 推薦的 DNS 提供商

These are our favorite public DNS resolvers based on their privacy and security characteristics, and their worldwide performance. Some of these services offer basic DNS-level blocking of malware or trackers depending on the server you choose, but if you want to be able to see and customize what is blocked you should use a dedicated DNS filtering product instead.

| DNS 提供者                                                                    | 協議                                  | Logging / Privacy Policy | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | 篩選                                                                                                                | Signed Apple Profile                                                                                                     |
| -------------------------------------------------------------------------- | ----------------------------------- | ------------------------ | -------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| [**AdGuard Public DNS**](https://adguard-dns.io/en/public-dns.html)        | 明文  DoH/3  DoT  DoQ  DNSCrypt       | 匿名化[^1]                  | 匿名化                                                            | Based on server choice. 使用的過濾器列表可以在這裡找到。 [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) | Yes [:octicons-link-external-24:](https://adguard.com/en/blog/encrypted-dns-ios-14.html)                                 |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | Cleartext   DoH/3   DoT             | Anonymized[^2]           | 不是                                                             | Based on server choice.                                                                                           | No [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846) |
| [**Control D Free DNS**](https://controld.com/free-dns)                    | 明文  DoH/3  DoT  DoQ                 | No[^3]                   | 不是                                                             | Based on server choice.                                                                                           | Yes [:octicons-link-external-24:](https://docs.controld.com/docs/macos-platform)                                         |
| [**dns0.eu**](https://dns0.eu)                                             | Cleartext   DoH/3   DoH   DoT   DoQ | Anonymized[^4]           | 匿名化                                                            | Based on server choice.                                                                                           | Yes [:octicons-link-external-24:](https://dns0.eu/zero.dns0.eu.mobileconfig)                                             |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | DoH   DoT                           | No[^5]                   | 不是                                                             | Based on server choice. 正在使用的過濾器列表可以在這裡找到。 [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)  | Yes [:octicons-link-external-24:](https://mullvad.net/en/blog/profiles-to-configure-our-encrypted-dns-on-apple-devices)  |
| [**Quad9**](https://quad9.net)                                             | Cleartext   DoH   DoT   DNSCrypt    | Anonymized[^6]           | 可選的                                                            | Based on server choice, malware blocking by default.                                                              | Yes [:octicons-link-external-24:](https://quad9.net/news/blog/ios-mobile-provisioning-profiles)                          |

## Self-Hosted DNS Filtering

在被控制平臺，自主託管 DNS 可提供有用的過濾，例如智能電視和其他物聯網設備，因為不需要客戶端軟件。

### Pi-hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](assets/img/dns/pi-hole.svg){ align=right }

**Pi-hole** 是一個開源的 [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) ，它使用 [DNS 篩選](https://cloudflare.com/learning/access-management/what-is-dns-filtering/)來阻止不需要的網頁內容，例如廣告。

Pi-hole 設計應用在 Raspberry Pi ，但它不限於這種硬體。 該軟體良好的 Web 界面，可查看有用資訊和管理被阻止的內容。

[:octicons-home-16: Homepage](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Source Code" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title=Contribute }

</details>

</div>

### AdGuard首頁

<div class="admonition recommendation" markdown>

![AdGuard 首頁標誌](assets/img/dns/adguard-home.svg){ align=right }

**AdGuard** 是一個開源的 [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) ，使用[DNS 過濾](https://cloudflare.com/learning/access-management/what-is-dns-filtering/) 來封鎖不需要的網頁內容，例如廣告。

AdGuard 首頁提供精美的網頁介面，可查看有用資訊並管理被封鎖的內容。

[:octicons-home-16: Homepage](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Source Code" }

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
<summary>下載</summary>

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
<summary>下載</summary>

- [:simple-windows11: Windows](https://github.com/nextdns/nextdns/wiki/Windows)
- [:simple-apple: macOS](https://apps.apple.com/us/app/nextdns/id1464122853)
- [:simple-linux: Linux](https://github.com/nextdns/nextdns/wiki)
- [:simple-appstore: App Store](https://apps.apple.com/app/nextdns/id1463342498)
- [:simple-github: GitHub](https://github.com/nextdns/nextdns/releases)

</details>

</div>

與帳戶一起使用時，NextDNS 將預設啟用洞察和日誌記錄功能（因為某些功能需求）。 可選擇保留日誌的存留時間和儲存位置，或完全停用日誌。

NextDNS's free plan is fully functional, but should not be relied upon for security or other critical filtering applications, because after 300,000 DNS queries in a month all filtering, logging, and other account-based functionality is disabled. It can still be used as a regular DNS provider after that point, so your devices will continue to function and make secure queries via DNS-over-HTTPS, just without your filter lists.

NextDNS also offers public DNS-over-HTTPS service at `https://dns.nextdns.io` and DNS-over-TLS/QUIC at `dns.nextdns.io`, which are available by default in Firefox and Chromium, and subject to their default no-logging [privacy policy](https://nextdns.io/privacy).

## 加密的DNS代理

加密DNS代理軟體提供了一個本地代理，用於將 [個未加密的DNS](advanced/dns-overview.md#unencrypted-dns) 解析器轉發到。 Typically, it is used on platforms that don't natively support [encrypted DNS](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ align=right }
![RethinkDNS logo](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** 是一個開源 Android 用戶端工具，支持 [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh)、 [DNS-over-TLS](advanced/dns-overview.md#dns-over-tls-dot)、 [DNSCrypt](advanced/dns-overview.md#dnscrypt)和 DNS 代理，以及快取DNS 回應、本地記錄 DNS 查詢，也可用作防火牆。

[:octicons-home-16: Homepage](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads: "下載"</summary>

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
<summary>Downloads: "下載"</summary>

- [:simple-windows11: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

The anonymized DNS feature does [not](advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns) anonymize other network traffic.

</div>

## 標準

**請注意，我們這裏所推薦專案沒有任何牽扯。 ** 除了 [我們的標準準則](about/criteria.md)外，還有一套明確要求以提出客觀建議。 我們建議您在選擇使用任何項目之前先熟悉此列表，並進行自己的研究，以確保您的正確選擇。

All DNS products must support:

- [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- [QNAME 最小化](advanced/dns-overview.md#what-is-qname-minimization).
- Anonymize [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) or disable it by default.

Additionally, all public providers:

- 首選 [anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) 支援或地理轉向支援。
- Must not log any personal data to disk
    - As noted in our footnotes, some providers collect query information for example, for purposes like security research, but in that case that data must not be associated with any PII such as IP address, etc.

[^1]: AdGuard 儲存其 DNS 伺服器的總和效能指標，即對特定伺服器的全部請求數量、被封鎖的請求數量，以及處理請求的速度。 他們還會保存和儲存過去24小時內所請求的網域資料庫。 我們需要這些資訊來識別和阻止新的追蹤器和威脅。 我們還記錄了這些追蹤器被封鎖的次數。 我們需要這些資訊以便在過濾器中刪除過時的規則。 [https://adguard.com/en/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: Cloudflare 僅收集並儲存發送至  1.1.1.1解析器的有限 DNS 查詢資料。 1.1.1.1解析器服務不會記錄個人資料，且大部分有限的非個人識別查詢資料僅存儲25小時。 [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: Control D 只有記錄使用自定義 DNS 配置的高級解析器。 免費解析器不記錄數據。 [https://controld.com/privacy](https://controld.com/privacy)
[^4]: dns0.eu collects some data for their threat intelligence feeds, to monitor for newly registered/observed/active domains and other bulk data. That data is shared with some [partners](https://docs.dns0.eu/data-feeds/introduction) for e.g. security research. They do not collect any Personally Identifiable Information. [https://dns0.eu/privacy](https://dns0.eu/privacy)
[^5]: Mullvad 的 DNS 服務可供 Mullvad VPN 的訂閱者和非訂閱者使用。 他們的隱私政策明確聲稱他們不會以任何方式記錄 DNS 請求。 [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^6]: Quad9會收集一些資料，以進行威脅監控和回應。 然後這些資料會被重新混合與共享，例如用於安全研究。 Quad9 不會收集或記錄 IP 位址或其他他們認為可識別個人身份的資料。 [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
