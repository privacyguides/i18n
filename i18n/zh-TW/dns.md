---
title: "DNS解析器"
icon: material/dns
description: We recommend choosing these encrypted DNS providers to replace your ISP's default configuration.
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>防護下列威脅：</small>

- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

使用第三方伺服器的加密 DNS 只能避開基本的 [DNS 封鎖](https://en.wikipedia.org/wiki/DNS_blocking) ，當您確定不會有不良後果時。 加密的 DNS 無法為您隱藏瀏覽活動。

[了解更多有關 DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## 推薦的提供商

這些是我們喜歡的公共 DNS 解析器，因為它們的隱私和安全特性且它們具備可向全世界提供服務的效能。 Some of these services offer basic DNS-level blocking of malware or trackers depending on the server you choose, but if you want to be able to see and customize what is blocked, you should use a dedicated DNS filtering product instead.

| DNS 提供者                                                                    | 協議                                                                       | 記錄日誌 / 隱私權政策   | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | 過濾                                                                                                         | 已簽署的 Apple 配置描述檔                                                                                                                                                                                                            |
| -------------------------------------------------------------------------- | ------------------------------------------------------------------------ | -------------- | -------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**AdGuard 公共 DNS**](https://adguard-dns.io/en/public-dns.html)            | Cleartext <br>DoH/3 <br>DoT <br>DoQ <br>DNSCrypt | 匿名化[^1]        | 匿名化                                                            | 根據伺服器的選擇。 使用的過濾器列表可以在這裡找到。 [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardSDNSFilter) | Yes [:octicons-link-external-24:](https://adguard-dns.io/en/blog/encrypted-dns-ios-14.html)                                                                                                                                 |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | Cleartext <br>DoH/3 <br>DoT                                  | Anonymized[^2] | 不採納                                                            | 根據伺服器的選擇。                                                                                                  | 沒有 [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846)                                                                                                    |
| [**Control D 免費 DNS**](https://controld.com/free-dns)                      | Cleartext <br>DoH/3 <br>DoT <br>DoQ                    | No[^3]         | 不採納                                                            | 根據伺服器的選擇。                                                                                                  | Yes <br>[:simple-apple: iOS](https://docs.controld.com/docs/ios-platform) <br>[:material-apple-finder: macOS](https://docs.controld.com/docs/macos-platform#manual-setup-profile)                               |
| [**DNS0.eu**](https://dns0.eu)                                             | Cleartext <br>DoH/3 <br>DoH <br>DoT <br>DoQ      | Anonymized[^4] | 匿名化                                                            | 根據伺服器的選擇。                                                                                                  | 有 [:octicons-link-external-24:](https://dns0.eu/zero.dns0.eu.mobileconfig)                                                                                                                                                  |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | DoH <br>DoT                                                        | No[^5]         | 不採納                                                            | 根據伺服器的選擇。 正在使用的過濾器列表可以在這裡找到。 [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)         | Yes [:octicons-link-external-24:](https://github.com/mullvad/encrypted-dns-profiles)                                                                                                                                        |
| [**Quad9**](https://quad9.net)                                             | Cleartext <br>DoH <br>DoT <br>DNSCrypt                 | Anonymized[^6] | 可選                                                             | 根據伺服器的選擇。 Malware blocking is included by default.                                                         | Yes <br>[:simple-apple: iOS](https://docs.quad9.net/Setup_Guides/iOS/iOS_14_and_later_(Encrypted)) <br>[:material-apple-finder: macOS](https://docs.quad9.net/Setup_Guides/MacOS/Big_Sur_and_later_(Encrypted)) |

## 自行託管 DNS 過濾器

在被控制平臺，自主託管 DNS 可提供有用的過濾，例如智慧電視和其他物聯網裝置，因為不需要客戶端軟體。

### Pi-hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](assets/img/dns/pi-hole.svg){ align=right }

**Pi-hole** 是一個開源的 [DNS沉洞](https://zh.wikipedia.org/wiki/DNS%E6%B2%89%E6%B4%9E) ，它使用 [DNS 過濾](https://cloudflare.com/learning/access-management/what-is-dns-filtering/)來阻止不需要的網頁內容，例如廣告。

Pi-hole 設計應用在 Raspberry Pi ，但它並不限於這種硬體。 該軟體良好的 Web 界面，可查看有用資訊和管理被阻止的內容。

[:octicons-home-16: 首頁](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="原始碼" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title=捐款 }

</details>

</div>

### AdGuard Home

<div class="admonition recommendation" markdown>

![AdGuard Home logo](assets/img/dns/adguard-home.svg){ align=right }

**AdGuard Home** 是一個開源的 [DNS沉洞](https://zh.wikipedia.org/wiki/DNS%E6%B2%89%E6%B4%9E) ，使用 [DNS 過濾](https://cloudflare.com/learning/access-management/what-is-dns-filtering/) 來封鎖不需要的網頁內容，例如廣告。

AdGuard Home 提供精美的網頁介面，可查看有用資訊並管理被封鎖的內容。

[:octicons-home-16: 首頁](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="原始碼" }

</details>

</div>

## 雲端 DNS 過濾器

These DNS filtering solutions offer a web dashboard where you can customize the block lists to your exact needs, similarly to a Pi-hole. 這些服務通常比上述自託管服務更容易設定和配置，並且可以更輕鬆地跨多個網路使用（自託管解決方案通常僅限於家用/區域網路，除非您進行更進階的設定）。

### Control D

<div class="admonition recommendation" markdown>

![Control D logo](assets/img/dns/control-d.svg){ align=right }

**Control D** 可自訂的 DNS 服務，可在 DNS 層級封鎖安全性威脅、不必要的內容和廣告。 付費方案之外，他們還提供許多可免費使用的預先配置 DNS 解析器。

[:octicons-home-16: Homepage](https://controld.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://controld.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.controld.com/docs/getting-started){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Control-D-Inc/ctrld){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.controld.setuputility)
- [:simple-appstore: App Store](https://apps.apple.com/app/1518799460)
- [:simple-github: GitHub](https://github.com/Control-D-Inc/ctrld/releases)
- [:fontawesome-brands-windows: Windows](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-apple: macOS](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-linux: Linux](https://docs.controld.com/docs/ctrld)

</details>

</div>

### NextDNS

<div class="admonition recommendation" markdown>

![NextDNS logo](assets/img/dns/nextdns.svg){ align=right }

**NextDNS** 為可自訂的 DNS 服務，可在 DNS 層級封鎖安全性威脅、不必要的內容和廣告。 他們提供功能齊全的免費計劃，但使用受限。

[:octicons-home-16: Homepage](https://nextdns.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextdns.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.nextdns.io){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/nextdns/nextdns){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/nextdns/id1463342498)
- [:simple-github: GitHub](https://github.com/nextdns/nextdns/releases)
- [:fontawesome-brands-windows: Windows](https://github.com/nextdns/nextdns/wiki/Windows)
- [:simple-apple: macOS](https://apps.apple.com/us/app/nextdns/id1464122853)
- [:simple-linux: Linux](https://github.com/nextdns/nextdns/wiki)

</details>

</div>

與帳戶一起使用時，NextDNS 將預設啟用洞察和日誌記錄功能（因為某些功能需求）。 可選擇保留日誌的存留時間和儲存位置，或完全停用日誌。

NextDNS's free plan is fully functional, but should not be relied upon for security or other critical filtering applications, because after 300,000 DNS queries in a month all filtering, logging, and other account-based functionality are disabled. It can still be used as a regular DNS provider after that point, so your devices will continue to function and make secure queries via DNS-over-HTTPS (DoH), just without your filter lists.

NextDNS also offers a public DoH service at `https://dns.nextdns.io` and DNS-over-TLS/QUIC (DoT/DoQ) at `dns.nextdns.io`, which are available by default in Firefox and Chromium, and subject to their default, no-logging [privacy policy](https://nextdns.io/privacy).

## 加密的DNS代理

加密DNS代理軟體提供了一個本地代理，用於將 [個未加密的DNS](advanced/dns-overview.md#unencrypted-dns) 解析器轉發到。 通常，它用於本身無法[加密 DNS](advanced/dns-overview.md#what-is-encrypted-dns) 的平台。

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ align=right }
![RethinkDNS logo](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** is an open-source Android client that supports [DoH](advanced/dns-overview.md#dns-over-https-doh), [DoT](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) and DNS Proxy. 它還提供附加功能，例如快取 DNS 回應、本機記錄 DNS 查詢以及使用應用程式作為防火牆。

[:octicons-home-16: Homepage](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

While RethinkDNS takes up the Android VPN slot, you can still use a VPN or Orbot with the app by [adding a WireGuard configuration](https://docs.rethinkdns.com/proxy/wireguard) or [manually configuring Orbot as a Proxy server](https://docs.rethinkdns.com/firewall/orbot), respectively.

### DNSCrypt-Proxy

<div class="admonition recommendation" markdown>

![DNSCrypt-Proxy logo](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**DNSCrypt-Proxy** is a DNS proxy with support for [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DoH](advanced/dns-overview.md#dns-over-https-doh), and [Anonymized DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

[:octicons-repo-16: Repository](https://github.com/DNSCrypt/dnscrypt-proxy#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Anonymized DNS [不會](advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns) 匿名化其他網路流量。

</div>

## 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用任何項目之前先熟悉此列表，並進行自己的研究，以確保您的正確選擇。

All DNS products...

- Must support [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- Must support [QNAME Minimization](advanced/dns-overview.md#what-is-qname-minimization).
- Must anonymize [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) or disable it by default.

Additionally, all public providers...

- Must not log any personal data to disk.
    - As noted in the footnotes, some providers collect query information for purposes like security research, but in that case the data must not be associated with any PII such as IP address, etc.
- Should support [anycast](https://en.wikipedia.org/wiki/Anycast) or geo-steering.

[^1]: AdGuard 儲存其 DNS 伺服器的總和效能指標，即對特定伺服器的全部請求數量、被封鎖的請求數量，以及處理請求的速度。 They also keep and store the database of domains requested within the last 24 hours.

    > We need this information to identify and block new trackers and threats. We also log how many times this or that tracker has been blocked. We need this information to remove outdated rules from our filters.

    AdGuard DNS: [*Privacy Policy*](https://adguard-dns.io/en/privacy.html) [^2]: Cloudflare collects and stores only the limited DNS query data that is sent to the 1.1.1.1 resolver. The 1.1.1.1 resolver service does not log personal data, and the bulk of the limited non-personally identifiable query data is stored only for 25 hours.

    1.1.1.1 Public DNS Resolver: [*Cloudflare’s commitment to privacy*](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) [^3]: Control D only logs specific account data for Premium resolvers with custom DNS profiles. Free resolvers do not retain any data.

    Control D: [*Privacy Policy*](https://controld.com/privacy) [^4]: DNS0.eu collects some data for their threat intelligence feeds to monitor for newly registered/observed/active domains and other bulk data. 資料與一些[合作夥伴](https://docs.dns0.eu/data-feeds/introduction)共享，例如安全研究。 They do not collect any personally identifiable information.

    DNS0.eu: [*Privacy Policy*](https://dns0.eu/privacy) [^5]: Mullvad's DNS service is available to both subscribers and non-subscribers of Mullvad VPN. 他們的隱私政策明確聲稱他們不會以任何方式記錄 DNS 請求。

    Mullvad: [*No-logging of user activity policy*](https://mullvad.net/en/help/no-logging-data-policy) [^6]: Quad9 collects some data for the purposes of threat monitoring and response. That data may then be remixed and shared for purposes like furthering their security research. Quad9 不會收集或記錄 IP 位址或其他他們認為可識別個人身份的資料。

    Quad9: [*Data and Privacy Policy*](https://quad9.net/privacy/policy)
