---
title: DNS解析器
icon: material/dns
description: 我們建議選擇這些加密的 DNS 供應商來取代 ISP 的預設設定。
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>防護下列威脅：</small>

- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

只在您確定不會有不良後果時，才應使用第三方伺服器的加密 **DNS** 來避開基本的 [DNS 封鎖](https://en.wikipedia.org/wiki/DNS_blocking)。 加密的 DNS 無法為您隱藏瀏覽活動。

[了解更多有關 DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## 推薦的提供商

這些是我們喜歡的公共 DNS 解析器，因為它們的隱私和安全特性且它們具備可向全世界提供服務的效能。 根據您所選擇的伺服器，其中部份服務會提供基本的 DNS 層級惡意軟體或追蹤器封鎖功能，但您若希望可以檢視與自訂封鎖的內容，則應使用專用的 DNS 過濾產品。

| DNS 提供者                                                                    | 協議                                                                | 記錄日誌 / 隱私權政策 | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | 過濾                                                                                                         | 已簽署的 Apple 配置描述檔                                                                                                                                                                                                          |
| -------------------------------------------------------------------------- | ----------------------------------------------------------------- | ------------ | -------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**AdGuard 公共 DNS**](https://adguard-dns.io/en/public-dns.html)            | 明文 <br>DoH/3 <br>DoT <br>DoQ <br>DNSCrypt | 匿名化[^1]      | 匿名化                                                            | 根據伺服器的選擇。 使用的過濾器列表可以在這裡找到。 [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardSDNSFilter) | 是 [:octicons-link-external-24:](https://adguard-dns.io/en/blog/encrypted-dns-ios-14.html)                                                                                                                                 |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | 明文 <br>DoH/3 <br>DoT                                  | 匿名化[^2]      | 不採納                                                            | 根據伺服器的選擇。                                                                                                  | 沒有 [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846)                                                                                                  |
| [**Control D 免費 DNS**](https://controld.com/free-dns)                      | 明文 <br>DoH/3 <br>DoT <br>DoQ                    | 否[^3]        | 不採納                                                            | 根據伺服器的選擇。                                                                                                  | 是 <br>[:simple-apple: iOS](https://docs.controld.com/docs/ios-platform) <br>[:material-apple-finder: macOS](https://docs.controld.com/docs/macos-platform#manual-setup-profile)                               |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | DoH <br>DoT                                                 | 否[^4]        | 不採納                                                            | 根據伺服器的選擇。 正在使用的過濾器列表可以在這裡找到。 [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)         | 是 [:octicons-link-external-24:](https://github.com/mullvad/encrypted-dns-profiles)                                                                                                                                        |
| [**Quad9**](https://quad9.net)                                             | 明文 <br>DoH <br>DoT <br>DNSCrypt                 | 匿名化[^5]      | 可選                                                             | 根據伺服器的選擇。 預設包含惡意軟體封鎖。                                                                                      | 是 <br>[:simple-apple: iOS](https://docs.quad9.net/Setup_Guides/iOS/iOS_14_and_later_(Encrypted)) <br>[:material-apple-finder: macOS](https://docs.quad9.net/Setup_Guides/MacOS/Big_Sur_and_later_(Encrypted)) |

## 雲端 DNS 過濾器

這些 DNS 過濾解決方案提供網頁儀表板，讓您能根據實際需求自訂封鎖清單。 這些服務可輕鬆應用於多個網路環境。

### Control D

<div class="admonition recommendation" markdown>

![Control D logo](assets/img/dns/control-d.svg){ align=right }

**Control D** 可自訂的 DNS 服務，可在 DNS 層級封鎖安全性威脅、不必要的內容和廣告。

付費方案之外，他們還提供許多可免費使用的預先配置 DNS 解析器。

[:octicons-home-16: 首頁](https://controld.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://controld.com/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://docs.controld.com/docs/getting-started){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/Control-D-Inc/ctrld){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

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

**NextDNS** 為可自訂的 DNS 服務，可在 DNS 層級封鎖安全性威脅、不必要的內容和廣告。

他們提供功能齊全的免費計劃，但使用受限。

[:octicons-home-16: 首頁](https://nextdns.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextdns.io/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://help.nextdns.io){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/nextdns/nextdns){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/nextdns/id1463342498)
- [:simple-github: GitHub](https://github.com/nextdns/nextdns/releases)
- [:fontawesome-brands-windows: Windows](https://github.com/nextdns/nextdns/wiki/Windows)
- [:simple-apple: macOS](https://apps.apple.com/us/app/nextdns/id1464122853)
- [:simple-linux: Linux](https://github.com/nextdns/nextdns/wiki)

</details>

</div>

與帳戶一起使用時，NextDNS 將預設啟用洞察和日誌記錄功能（因為某些功能需求）。 可選擇保留日誌的存留時間和儲存位置，或完全停用日誌。

NextDNS 的免費方案功能完備，但不應作為安全防護或其他關鍵過濾應用程式的依賴方案，因為每月超過三十萬次 DNS 查詢後，所有過濾、記錄及其他基於帳號的功能將被停用。 其此後仍可以當作一般 DNS 供應商使用，因此您的裝置將持續運作，並透過 DNS-over-HTTPS (DoH) 進行安全查詢，只是不會套用您的過濾清單。

NextDNS 也透過 `https://dns.nextdns.io` 提供公開的 DoH 服務，並於 `dns.nextdns.io` 提供 DNS-over-TLS/QUIC (DoT/DoQ)，Firefox 與 Chromium 在預設情況下皆可使用，並遵守其預設無紀錄的[隱私權政策](https://nextdns.io/privacy)。

## 加密的DNS代理

加密DNS代理軟體提供了一個本地代理，用於將 [個未加密的DNS](advanced/dns-overview.md#unencrypted-dns) 解析器轉發到。 通常，它用於本身無法[加密 DNS](advanced/dns-overview.md#what-is-encrypted-dns) 的平台。

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS 標誌](assets/img/android/rethinkdns.svg#only-light){ align=right }
![RethinkDNS 標誌](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** 是支援 [DoH](advanced/dns-overview.md#dns-over-https-doh)、[DoT](advanced/dns-overview.md#dns-over-tls-dot)、[DNSCrypt](advanced/dns-overview.md#dnscrypt) 與 DNS Proxy 的開放原始碼 Android 客戶端。 它還提供附加功能，例如快取 DNS 回應、本機記錄 DNS 查詢以及使用應用程式作為防火牆。

[:octicons-home-16: 首頁](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

雖然 RethinkDNS 會佔用 Android 的 VPN 槽位，但您仍可在應用程式中使用 VPN 或 Orbot，方法是[新增 WireGuard 組態](https://docs.rethinkdns.com/proxy/wireguard)或[手動將 Orbot 設定為代理伺服器](https://docs.rethinkdns.com/firewall/orbot)。

### DNSCrypt-Proxy

<div class="admonition recommendation" markdown>

![DNSCrypt-Proxy 標誌](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**DNSCrypt-Proxy** 是支援 [DNSCrypt](advanced/dns-overview.md#dnscrypt)、[DoH](advanced/dns-overview.md#dns-over-https-doh) 與 [匿名化 DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS) 的 DNS 代理伺服器。

[:octicons-repo-16: 倉庫](https://github.com/DNSCrypt/dnscrypt-proxy#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="原始碼" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title="貢獻" }

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

所有 DNS 產品……

- 必須支援 [DNSSEC](advanced/dns-overview.md#what-is-dnssec)。
- 必須支援 [QNAME 最小化](advanced/dns-overview.md#what-is-qname-minimization)。
- 必須匿名化 [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) 或預設停用。

此外，所有公開供應商……

- 不得將任何個人資料記錄在磁碟上。
    - 如腳註所述，部分服務供應商會為安全研究等目的蒐集查詢資訊，但在此類情況下，該資料不得與任何個人識別資訊（如 IP 位址等）產生關聯。
- 應支援[任播](https://en.wikipedia.org/wiki/Anycast)或 geo-steering。

[^1]: AdGuard 儲存其 DNS 伺服器的總和效能指標，即對特定伺服器的全部請求數量、被封鎖的請求數量，以及處理請求的速度。 他們亦會保留並儲存過去24小時內被查詢的網域名稱資料庫。

    > 我們需要這些資訊來辨識並封鎖新的追蹤器與威脅。 我們也記錄了這些追蹤器被封鎖的次數。 我們需要此資訊以從我們的過濾條件中移除過時的規則。

    AdGuard DNS：[*隱私權政策*](https://adguard-dns.io/en/privacy.html) [^2]: Cloudflare 僅蒐集並儲存傳送至 1.1.1.1 解析器的有限 DNS 查詢資料。 1.1.1.1 解析器服務不會記錄個人資料，且大部分有限的非個人識別查詢資料僅儲存25小時。

    1.1.1.1 公共 DNS 解析器：[*Cloudflare 對隱私的承諾*](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) [^3]： Control D 僅會記錄包含自訂 DNS 設定檔的 Premium 解析器的特定帳號資料。 免費解析器不會保留任何資料。

    Control D: [*Privacy Policy*](https://controld.com/privacy) [^4]: Mullvad's DNS service is available to both subscribers and non-subscribers of Mullvad VPN. 他們的隱私政策明確聲稱他們不會以任何方式記錄 DNS 請求。

    Mullvad: [*No-logging of user activity policy*](https://mullvad.net/en/help/no-logging-data-policy) [^5]: Quad9 collects some data for the purposes of threat monitoring and response. That data may then be remixed and shared for purposes like furthering their security research. Quad9 不會收集或記錄 IP 位址或其他他們認為可識別個人身份的資料。

    Quad9: [*Data and Privacy Policy*](https://quad9.net/privacy/policy)
