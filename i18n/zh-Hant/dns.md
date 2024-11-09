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

<small>防護下列威脅：</small>

- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

使用第三方伺服器的加密 DNS 只能避開基本的 [DNS 封鎖](https://en.wikipedia.org/wiki/DNS_blocking) ，當您確定不會有不良後果時。 加密的 DNS 無法為您隱藏瀏覽活動。

[了解更多有關 DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## 推薦的提供商

這些是我們喜歡的公共 DNS 解析器，因為它們的隱私和安全特性且它們具備可向全世界提供服務的效能。 其中一些服務根據所選擇的伺服器提供基本的 DNS 等級惡意軟體或追蹤器封鎖功能，但如希望能夠查看和自訂封鎖的內容，則應使用專用的 DNS 過濾產品。

| DNS 提供者                                                                    | 協議                            | 記錄日誌 / 隱私權政策 | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | 過濾                                                                                                  | 已簽署的 Apple 配置描述檔                                                                                                         |
| -------------------------------------------------------------------------- | ----------------------------- | ------------ | -------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| [**AdGuard 公共 DNS**](https://adguard-dns.io/en/public-dns.html)            | 明文  DoH/3  DoT  DoQ  DNSCrypt | 匿名化[^1]      | 匿名化                                                            | 根據伺服器的選擇。 使用的過濾器列表可以在這裡找到。 [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) | Yes [:octicons-link-external-24:](https://adguard-dns.io/en/blog/encrypted-dns-ios-14.html)                              |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | 明文   DoH/3   DoT              | 匿名化[^2]      | 不採納                                                            | 根據伺服器的選擇。                                                                                           | 沒有 [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846) |
| [**Control D 免費 DNS**](https://controld.com/free-dns)                      | 明文  DoH/3  DoT  DoQ           | 不記錄[^3]      | 不採納                                                            | 根據伺服器的選擇。                                                                                           | 有 [:octicons-link-external-24:](https://docs.controld.com/docs/macos-platform)                                           |
| [**dns0.eu**](https://dns0.eu)                                             | 明文   DoH/3   DoH   DoT   DoQ  | 匿名化[^4]      | 匿名化                                                            | 根據伺服器的選擇。                                                                                           | 有 [:octicons-link-external-24:](https://dns0.eu/zero.dns0.eu.mobileconfig)                                               |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | DoH   DoT                     | 不記錄[^5]      | 不採納                                                            | 根據伺服器的選擇。 正在使用的過濾器列表可以在這裡找到。 [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)  | 有 [:octicons-link-external-24:](https://mullvad.net/en/blog/profiles-to-configure-our-encrypted-dns-on-apple-devices)    |
| [**Quad9**](https://quad9.net)                                             | 明文   DoH   DoT   DNSCrypt     | 匿名化[^6]      | 可選                                                             | 根據伺服器選擇，預設會封鎖惡意程式碼。                                                                                 | 有 [:octicons-link-external-24:](https://quad9.net/news/blog/ios-mobile-provisioning-profiles)                            |

## 自行託管 DNS 過濾器

在被控制平臺，自主託管 DNS 可提供有用的過濾，例如智能電視和其他物聯網設備，因為不需要客戶端軟件。

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

這些 DNS 過濾解決方案提供 網頁儀表板，可以在其中根據特定需求自訂封鎖列表，類似於 Pi-hole。 這些服務通常比上述自託管服務更容易設定和配置，並且可以更輕鬆地跨多個網路使用（自託管解決方案通常僅限於家用/本地網路，除非您進行更進階的設定）。

### Control D

<div class="admonition recommendation" markdown>

![Control D logo](assets/img/dns/control-d.svg){ align=right }

**Control D** 可自訂的 DNS 服務，可在 DNS 層級封鎖安全性威脅、不必要的內容和廣告。 付費方案之外，他們還提供許多可免費使用的預先配置 DNS 解析器。

[:octicons-home-16: 首頁](https://controld.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://controld.com/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://docs.controld.com/docs/getting-started){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/Control-D-Inc/ctrld){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-apple: macOS](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-linux: Linux](https://docs.controld.com/docs/ctrld)
- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.controld.setuputility)
- [:simple-appstore: App Store](https://apps.apple.com/app/1518799460)
- [:simple-github: GitHub](https://github.com/Control-D-Inc/ctrld/releases)

</details>

</div>

### NextDNS

<div class="admonition recommendation" markdown>

![NextDNS logo](assets/img/dns/nextdns.svg){ align=right }

**NextDNS** 為可自訂的 DNS 服務，可在 DNS 層級封鎖安全性威脅、不必要的內容和廣告。 他們提供功能齊全的免費計劃，但使用受限。

[:octicons-home-16: 首頁](https://nextdns.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextdns.io/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://help.nextdns.io){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/nextdns/nextdns){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/nextdns/nextdns/wiki/Windows)
- [:simple-apple: macOS](https://apps.apple.com/us/app/nextdns/id1464122853)
- [:simple-linux: Linux](https://github.com/nextdns/nextdns/wiki)
- [:simple-appstore: App Store](https://apps.apple.com/app/nextdns/id1463342498)
- [:simple-github: GitHub](https://github.com/nextdns/nextdns/releases)

</details>

</div>

與帳戶一起使用時，NextDNS 將預設啟用洞察和日誌記錄功能（因為某些功能需求）。 可選擇保留日誌的存留時間和儲存位置，或完全停用日誌。

NextDNS 的免費方案功能齊全，但不應依賴於其提供的安全性及其他重要功能，因為在一個月內進行 300,000 次 DNS 查詢之後，所有過濾、日誌記錄和其他基於帳戶的功能都會被停用。 此後，它仍可以用作常規 DNS 供應商，因此裝置將繼續運作並透過 DNS-over-HTTPS 進行安全的查詢，但沒有過濾功能。

NextDNS 也在 `https://dns.nextdns.io` 提供公共DNS-over-HTTPS 服務，並在 `dns.nextdns.io` 提供DNS-over-TLS/QUIC服務，預設情況下，在 Firefox 和 Chromium 中可用，並遵守其預設無日誌記錄的 [隱私權政策](https://nextdns.io/privacy) 。

## 加密的DNS代理

加密DNS代理軟體提供了一個本地代理，用於將 [個未加密的DNS](advanced/dns-overview.md#unencrypted-dns) 解析器轉發到。 通常，它用於本身無法[加密 DNS](advanced/dns-overview.md#what-is-encrypted-dns) 的平台。

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ align=right }
![RethinkDNS logo](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** 是一個開放原始碼的 Android 用戶端，支援 [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh)、[DNS-over-TLS](advanced/dns-overview.md#dns-over-tls-dot)、[DNSCrypt](advanced/dns-overview.md#dnscrypt) 和 DNS代理。 它還提供附加功能，例如快取 DNS 回應、本機記錄 DNS 查詢以及使用應用程式作為防火牆。

[:octicons-home-16: 首頁](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

雖然 RethinkDNS 會佔用 Android 的 VPN 插槽，但您仍可在應用程式中使用 VPN 或 Orbot，方法是 [自行新增 Wireguard 設定](https://docs.rethinkdns.com/proxy/wireguard) 或 [手動將 Orbot 設定為 Proxy 伺服器](https://docs.rethinkdns.com/firewall/orbot)。

### dnscrypt-proxy

<div class="admonition recommendation" markdown>

![dnscrypt-proxy logo](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**dnscrypt-proxy** 是一個 DNS代理，支持 [DNSCrypt](advanced/dns-overview.md#dnscrypt)、 [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh) 和 [Anonymized DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS)。

[:octicons-repo-16: 儲存庫](https://github.com/DNSCrypt/dnscrypt-proxy){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="原始碼" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title=捐款 }

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

所有 DNS 產品必須支援：

- [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- [QNAME 最小化](advanced/dns-overview.md#what-is-qname-minimization).
- 匿名化 [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) 或 根本不採納。

此外，對於所有公開提供者：

- 偏好有支援 [anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) 或 geo-steering 的服務。
- 不得將任何個人資料記錄在磁碟
    - 正如腳註所述，一些提供者會收集查詢信息，例如用於安全研究等目的，但在這種情況下，數據不得與任何 PII（例如 IP 位址等）相關聯。

[^1]: AdGuard 儲存其 DNS 伺服器的總和效能指標，即對特定伺服器的全部請求數量、被封鎖的請求數量，以及處理請求的速度。 他們還會保存和儲存過去24小時內所請求的網域資料庫。 我們需要這些資訊來識別和阻止新的追蹤器和威脅。 我們還記錄了這些追蹤器被封鎖的次數。 我們需要這些資訊以便在過濾器中刪除過時的規則。 [https://adguard-dns.io/en/privacy.html](https://adguard-dns.io/en/privacy.html)
[^2]: Cloudflare 僅收集並儲存發送至  1.1.1.1解析器的有限 DNS 查詢資料。 1.1.1.1解析器服務不會記錄個人資料，且大部分有限的非個人識別查詢資料僅存儲25小時。 [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: Control D 只有記錄使用自定義 DNS 配置的高級解析器。 免費解析器不記錄數據。 [https://controld.com/privacy](https://controld.com/privacy)
[^4]: dns0.eu 為其威脅情報來源收集一些數據，以監控新註冊/觀察/活動的網域和其他大量資料。 資料與一些[合作夥伴](https://docs.dns0.eu/data-feeds/introduction)共享，例如安全研究。 不收集任何個人識別資訊。 [https://dns0.eu/privacy](https://dns0.eu/privacy)
[^5]: Mullvad 的 DNS 服務可供 Mullvad VPN 的訂閱者和非訂閱者使用。 他們的隱私政策明確聲稱他們不會以任何方式記錄 DNS 請求。 [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^6]: Quad9會收集一些資料，以進行威脅監控和回應。 然後這些資料會被重新混合與共享，例如用於安全研究。 Quad9 不會收集或記錄 IP 位址或其他他們認為可識別個人身份的資料。 [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
