---
meta_title: "隱私 VPN 服務建議和比較，無任何贊助商或廣告 - Privacy Guides"
title: "VPN 服務"
icon: material/vpn
description: 保護您線上隱私與安全的最佳 VPN 服務。 Find a provider here that isn't out to spy on you.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>防護下列威脅：</small>

- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

如果您想從 ISP、公共 Wi-Fi 或傳送檔案時獲得更多*隱私*，**VPN**可能是您的解決方案。

<div class="admonition danger" markdown>
<p class="admonition-title">VPN 不提供匿名性</p>

使用 VPN **無法** 讓您的瀏覽習慣保持匿名，也不會為不安全 (HTTP) 的流量增加額外的安全性。

如果您追求的是 **匿名性** ，您應該使用 Tor 瀏覽器。 如果您正在尋求額外的 **安全性** ，您應該始終確保使用 HTTPS 連接到網站。 VPN不能取代良好的安全措施。

[下載 Tor](https://torproject.org){ .md-button .md-button--primary } [Tor 迷思 & 常見問答](advanced/tor-overview.md){ .md-button }

</div>

[VPN 概述 :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## 推薦的供應商

我們推薦的供應商使用加密技術，支援 WireGuard & OpenVPN，並有無記錄政策。 閱讀我們[完整的標準清單](#criteria)，瞭解更多資訊。

| 供應商                   | 國家   | WireGuard                     | 端口轉發                                        | IPv6                                              | 匿名付款方式    |
| --------------------- | ---- | ----------------------------- | ------------------------------------------- | ------------------------------------------------- | --------- |
| [Proton](#proton-vpn) | 112+ | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } 部分支援 | :material-information-outline:{ .pg-blue } 有限支援   | 現金        |
| [IVPN](#ivpn)         | 37+  | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }      | :material-information-outline:{ .pg-blue } 僅限連出流量 | Monero、現金 |
| [Mullvad](#mullvad)   | 45+  | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }      | :material-check:{ .pg-green }                     | Monero、現金 |

### Proton VPN

<div class="admonition recommendation" markdown>

![Proton VPN 標誌](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** 是 VPN 領域的強大競爭者，自 2016 年開始營運。 Proton AG 總部位於瑞士，提供有限的免費方案，以及更多功能的付費方案。

[:octicons-home-16: 首頁](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title="說明文件"}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://protonvpn.com/download-windows)
- [:simple-apple: macOS](https://protonvpn.com/download-macos)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 112 個國家

Proton VPN [在 112 個國家設有伺服器](https://protonvpn.com/vpn-servers)，如果您使用其[免費計劃](https://protonvpn.com/free-vpn/server)，則在 [5 個](https://protonvpn.com/support/how-to-create-free-vpn-account)國家設有伺服器。(1) 選擇擁有距離您最近的伺服器之 VPN 供應商，可減少發送網路流量的延遲。 這是因為到達目的地的路徑較短 (跳數較少)。
{ .annotate }

1. 最近檢查日期: 2024-08-06

我們認為，如果 VPN 供應商使用[專用伺服器](https://en.wikipedia.org/wiki/Dedicated_hosting_service)，而非採用更便宜、與其他客戶共享的解決方案 (例如[虛擬伺服器](https://en.wikipedia.org/wiki/Virtual_private_server))，對其私鑰的安全性會更好。

#### :material-check:{ .pg-green } 獨立稽核

截至 2020 年 1 月， Proton VPN 已通過 SEC Consult 的獨立審計。 SEC Consult 在 Proton VPN Windows、Android 和 iOS 應用程式中發現一些中低風險漏洞，Proton VPN 已在報告發布之前全部 “妥善修復” 了這些漏洞。 所發現的問題都不會讓攻擊者遠端存取您的裝置或流量。 您可以在 [protonvpn.com](https://protonvpn.com/blog/open-source) 查看各個平臺的報告。 2022 年 4 月，Proton VPN 接受[另一次審核](https://protonvpn.com/blog/no-logs-audit)。 [Securitum](https://research.securitum.com) 於 2021 年 11 月 9 日簽發 Proton VPN 的[應用程式認證函](https://proton.me/blog/security-audit-all-proton-apps) 。

#### :material-check:{ .pg-green } 開源客戶端

Proton VPN 在其 [GitHub 組織](https://github.com/ProtonVPN) 中提供桌面和行動裝置客戶端的原始碼。

#### :material-check:{ .pg-green } 接受現金

除了信用卡/簽帳卡、PayPal 和 [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) 以外，Proton VPN 還接受 **現金/當地貨幣** 等匿名付款方式。

#### :material-check:{ .pg-green } 支援 WireGuard

Proton VPN supports the WireGuard® protocol. [WireGuard](https://wireguard.com/protocol) 是一種較新的協議，使用最先進的[密碼學](https://wireguard.com)。 此外，WireGuard 的目標是更簡單，更高效。

Proton VPN [推薦](https://protonvpn.com/blog/wireguard)搭配 WireGuard 使用。 Proton VPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-alert-outline:{ .pg-orange } 有限的 IPv6 支援

Proton 現在在其瀏覽器擴充套件中 [支援 IPv6](https://protonvpn.com/support/prevent-ipv6-vpn-leaks)，但只有 80% 的伺服器相容於 IPv6。 在其他平台上，Proton VPN 客戶端會封鎖所有 IPv6 流量，因此您不必擔心您的 IPv6 位址會被洩漏，但您將無法連線到任何僅允許使用 IPv6 訪問的網站，也無法從僅限 IPv6 的網路連線到 Proton VPN。

#### :material-information-outline:{ .pg-info } 遠端端口轉發

Proton VPN 目前僅支援通過 NAT-PMP 進行短暫的[遠端端口轉發](https://protonvpn.com/support/port-forwarding)，租用時間為 60 秒。 The Windows app provides an easy-to-access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup). BT 客戶端通常原生支援 NAT-PMP。

#### :material-information-outline:{ .pg-blue } 突破網路審查

Proton VPN has their [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) protocol which *may* help in situations where VPN protocols like OpenVPN or WireGuard are blocked with various rudimentary techniques. Stealth 將 VPN 隧道封裝在 TLS 會話中，使其看起來像是一般的網路流量。

不幸的是，在部署了精密過濾器分析所有傳出流量以試圖發現加密隧道的國家，此方法的效果並不理想。 Stealth 可在 Android、iOS、Windows 和 macOS 上使用，但尚未在 Linux 上可用。

#### :material-check:{ .pg-green } 行動裝置客戶端

除了提供標準 OpenVPN 設定檔外，Proton VPN 還在 [App Store](https://apps.apple.com/app/id1437005085)、[Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android) 和 [GitHub](https://github.com/ProtonVPN/android-app/releases) 提供行動裝置客戶端，以供使用者方便連接到他們的伺服器。

#### :material-information-outline:{ .pg-blue } 補充說明

Proton VPN clients support two-factor authentication on all platforms. Proton VPN 在瑞士、冰島和瑞典擁有自己的伺服器和資料中心。 他們透過自己的 DNS 服務，提供內容封鎖和已知的惡意軟體網域。 此外，Proton VPN 還提供 "Tor" 伺服器，可輕鬆連接到洋蔥網站，但我們仍然強烈建議您使用 [官方 Tor 瀏覽器](tor.md#tor-browser) 來完成此類目的。

##### :material-alert-outline:{ .pg-orange } Kill switch feature is broken on Intel-based Macs

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch) on Intel-based Macs when using the VPN kill switch. 如果您需要此功能，但使用的是搭載 Intel 處理器的 Mac 電腦 ，則應考慮使用其他 VPN 服務。

### IVPN

<div class="admonition recommendation" markdown>

![IVPN logo](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** 是另一個高級 VPN 供應商，自 2009 年開始運營。 IVPN 位於直布羅陀，不提供免費試用。

[:octicons-home-16: 首頁](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title="說明文件"}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:fontawesome-brands-windows: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 37 個國家

IVPN 在 [37 個國家/地區設有伺服器](https://ivpn.net/status)。(1) 選擇擁有距離您最近的伺服器之 VPN 供應商，可減少發送網路流量的延遲。 這是因為到達目的地的路徑較短 (跳數較少)。
{ .annotate }

1. 最近檢查日期: 2024-08-06

我們認為，如果 VPN 供應商使用[專用伺服器](https://en.wikipedia.org/wiki/Dedicated_hosting_service)，而非採用更便宜、與其他客戶共享的解決方案 (例如[虛擬伺服器](https://en.wikipedia.org/wiki/Virtual_private_server))，對其私鑰的安全性會更好。

#### :material-check:{ .pg-green } 獨立稽核

IVPN has had multiple [independent audits](https://ivpn.net/en/blog/tags/audit) since 2019 and has publicly announced their commitment to [annual security audits](https://ivpn.net/blog/ivpn-apps-security-audit-concluded).

#### :material-check:{ .pg-green } 開源客戶端

2020 年 2 月起[IVPN 應用程式已開源](https://ivpn.net/blog/ivpn-applications-are-now-open-source)。 原始碼可從他們的 [GitHub 組織](https://github.com/ivpn) 取得。

#### :material-check:{ .pg-green } 接受現金和 Monero

除了接受信用卡/簽帳卡和 PayPal 外，IVPN 還接受比特幣、**Monero** 和 **現金/當地貨幣** (僅限年度方案) 作為匿名付款方式。 [也提供](https://ivpn.net/knowledgebase/billing/voucher-cards-faq).帶有兌換代碼的預付卡。

#### :material-check:{ .pg-green } 支援 WireGuard

IVPN 支援 WireGuard® 協議。 [WireGuard](https://wireguard.com/protocol) 是一種較新的協議，使用最先進的[密碼學](https://wireguard.com)。 此外，WireGuard 的目標是更簡單，更高效。

IVPN [建議](https://ivpn.net/wireguard)搭配 WireGuard 使用，IVPN 在所有平台的應用程式皆已預設為 WireGuard 協議。 IVPN 也提供 WireGuard 設定檔產生器，可用於 WireGuard 的官方[應用程式](https://wireguard.com/install)。

#### :material-information-outline:{ .pg-blue } 支援 IPv6

IVPN 可以[透過 IPv6 連接到服務](https://ivpn.net/knowledgebase/general/do-you-support-ipv6)，但無法從僅支援 IPv6 的裝置連線。

#### :material-alert-outline:{ .pg-orange } 遠端端口轉發

IVPN 曾支援遠端端口轉發，但在 [2023 年 6 月](https://ivpn.net/blog/gradual-removal-of-port-forwarding) 移除了此功能。 缺少此功能可能會對某些應用程式造成負面影響，尤其是 BT 客戶端等點對點應用程式。

#### :material-check:{ .pg-green } 突破網路審查

IVPN has obfuscation modes using [v2ray](https://v2ray.com/en/index.html) which helps in situations where VPN protocols like OpenVPN or WireGuard are blocked. Currently, this feature is only available on Desktop and [iOS](https://ivpn.net/knowledgebase/ios/v2ray). 可透過 QUIC 或 TCP 兩種模式連接 [VMess](https://guide.v2fly.org/en_US/basics/vmess.html)。 QUIC 是一個新的傳輸協議，具有更好的擁塞控制，因此可能速度更快，且延遲更低。 TCP 模式的數據呈現為一般的 HTTP 流量。

#### :material-check:{ .pg-green } 行動裝置客戶端

除了提供標準 OpenVPN 設定檔外，IVPN 還在 [App Store](https://apps.apple.com/app/id1193122683)、[Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client) 和 [GitHub](https://github.com/ivpn/android-app/releases) 提供行動裝置客戶端，以供使用者方便連接到他們的伺服器。

#### :material-information-outline:{ .pg-blue } 補充說明

IVPN clients support two-factor authentication. IVPN 有「[反追蹤](https://ivpn.net/antitracker)」功能，以阻絕來自網路層的廣告與追蹤。

### Mullvad

<div class="admonition recommendation" markdown>

![Mullvad 標誌](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** 是一個快速且便宜的 VPN，非常注重透明和安全性。 他們自 2009 年起開始營運。 Mullvad is based in Sweden and offers a 14-day money-back guarantee for [payment methods](https://mullvad.net/en/help/refunds) that allow it.

[:octicons-home-16: 首頁](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="洋蔥服務" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 49 Countries

Mullvad has [servers in 49 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. 這是因為到達目的地的路徑較短 (跳數較少)。
{ .annotate }

1. Last checked: 2025-03-10

我們認為，如果 VPN 供應商使用[專用伺服器](https://en.wikipedia.org/wiki/Dedicated_hosting_service)，而非採用更便宜、與其他客戶共享的解決方案 (例如[虛擬伺服器](https://en.wikipedia.org/wiki/Virtual_private_server))，對其私鑰的安全性會更好。

#### :material-check:{ .pg-green } 獨立稽核

Mullvad has had multiple [independent audits](https://mullvad.net/en/blog/tag/audits) and has publicly announced their endeavors to conduct [annual audits](https://mullvad.net/en/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) of their apps and infrastructure.

#### :material-check:{ .pg-green } 開源客戶端

Mullvad 在其 [GitHub 組織](https://github.com/mullvad/mullvadvpn-app) 中提供桌面和行動裝置客戶端的原始碼。

#### :material-check:{ .pg-green } 接受現金和 Monero

除了接受信用卡/簽帳卡和 PayPal 外， Mullvad 還接受比特幣, Bitcoin Cash **Monero** 和 **現金/當地貨幣** （年度方案繳費）作為匿名付款方式。 也提供帶有兌換代碼的預付卡。 Mullvad 也接受 Swish 和銀行電匯，以及一些歐洲的付款系統。

#### :material-check:{ .pg-green } 支援 WireGuard

Mullvad 支援 WireGuard® 協議。 [WireGuard](https://wireguard.com/protocol) 是一種較新的協議，使用最先進的[密碼學](https://wireguard.com)。 此外，WireGuard 的目標是更簡單，更高效。

Mullvad [建議](https://mullvad.net/en/help/why-wireguard)搭配 WireGuard 使用。 在 Mullvad 的 Android、iOS、macOS 以及 Linux 平台的應用程式中，WireGuard 已是預設協議；在 Windows 平台則需[手動選擇](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard。 Mullvad 也提供 WireGuard 設定檔產生器，可用於 WireGuard 的官方[應用程式](https://wireguard.com/install)。

#### :material-check:{ .pg-green } IPv6 支援

Mullvad 允許您[存取架設在 IPv6 上的服務](https://mullvad.net/en/blog/2014/9/15/ipv6-support)，且支援使用 IPv6 的裝置連線。

#### :material-alert-outline:{ .pg-orange } 遠端端口轉發

Mullvad 曾支援遠端端口轉發，但在 [2023 年 5 月](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports) 移除了此功能。 缺少此功能可能會對某些應用程式造成負面影響，尤其是 BT 客戶端等點對點應用程式。

#### :material-check:{ .pg-green } 突破網路審查

Mullvad 提供多種功能，協助繞過審查制度，自由存取網際網路：

- **Obfuscation modes**: Mullvad has two built-in obfuscation modes: "UDP-over-TCP" and ["WireGuard over Shadowsocks"](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard). 這些模式會將您的 VPN 流量偽裝成一般的網路流量，使審查員更難偵測和封鎖。 據說，中國會利用[新的方法來擾亂 Shadowsocks 路由的流量](https://gfw.report/publications/usenixsecurity23/en)。
- **使用 Shadowsocks 和 v2ray 進階混淆**：對於更進階的使用者，Mullvad 提供了如何在 Mullvad 用戶端同時使用 [Shadowsocks 以及 v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) 外掛程式的指南。 此設定提供了額外的混淆和加密層。
- **自訂伺服器 IP**：要對抗 IP 封鎖，您可以向 Mullvad 的支援團隊申請自訂伺服器 IP。 收到自訂 IP 後，您可以在「Server IP override」設定中輸入文字檔，這樣就可以用審查員不知道的 IP 位址覆寫所選的伺服器 IP 位址。
- **橋接和代理**：Mullvad 也允許您使用橋接器或代理伺服器來存取他們的 API (驗證時需要)，這有助於繞過存取 API 的審查封鎖。

#### :material-check:{ .pg-green } 行動裝置客戶端

Mullvad 提供 [App Store](https://apps.apple.com/app/id1488466513) 和 [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) 客戶端，兩者都支援易於使用的界面，無須手動配置 WireGuard。 Android 客戶端也可以在 [GitHub](https://github.com/mullvad/mullvadvpn-app/releases) 上下載。

#### :material-information-outline:{ .pg-blue } 補充說明

Mullvad 對於他們[自有或租用](https://mullvad.net/en/servers)的節點透明度非常好。 他們也在應用程式中提供啟用防禦 AI 導向流量分析 ([DAITA](https://mullvad.net/en/blog/daita-defense-against-ai-guided-traffic-analysis)) 的選項。 DAITA 可防禦進階流量分析的威脅，這種分析可用於將 VPN 流量中的模式與特定網站連接起來。

## 標準

<div class="admonition danger" markdown>
<p class="admonition-title">危險</p>

注意，使用 VPN 不會使您匿名，但在某些情況下可以提供更好的隱私。 VPN 不是非法活動的工具。 不要依賴「無日誌」政策。

</div>

**請注意，我們與推薦的任何項目均無任何關聯。 這使我們能夠提供完全客觀的建議。**除了[我們的通用標準](about/criteria.md)外，我們還為任何希望獲得推薦的 VPN 服務商制定了一套明確的要求，包括高強度加密、獨立安全審計、現代技術等。 我們建議您在選擇 VPN 供應商之前先熟悉此清單，並進行自己的研究，盡可能地確保您選擇的 VPN 供應商值得信賴。

### 技術

We require all our recommended VPN providers to provide standard configuration files which can be used in a generic, open-source client. **If** a VPN provides their own custom client, we require a kill switch to block network data leaks when disconnected.

**最低合格要求：**

- Support for strong protocols such as WireGuard.
- Kill switch built in to clients.
- Multi-hop support. Multi-hopping is important to keep data private in case of a single node compromise.
- 如有提供 VPN 用戶端，則應為 [開源](https://en.wikipedia.org/wiki/Open_source)，一如所內建的 VPN 軟體。 我們相信，提供[原始碼](https://en.wikipedia.org/wiki/Source_code)可顯著提高透明度，讓我們知道程式實際在做什麼。
- 抗審查功能可在沒有 DPI 的情況下繞過防火牆。

**最佳情況：**

- Kill switch with highly configurable options (enable/disable on certain networks, on boot, etc.)
- 易於使用的 VPN 客戶端
- 支援 [IPv6](https://en.wikipedia.org/wiki/IPv6)。 我們希望伺服器能允許透過 IPv6 傳入連線，並允許您存取託管在 IPv6 位址上的服務。
- [遠端端口轉發](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) 的功能可協助在使用 P2P ([對等](https://en.wikipedia.org/wiki/Peer-to-peer)) 檔案共享軟體或自建伺服器 (例如 Mumble) 時建立連接。
- 混淆技術可掩蓋網際網路流量的真實性質，旨在繞過像 DPI 等先進的網際網路審查方法。

### 隱私

我們希望所推薦的供應商收集越少資料越好。 必須在註冊時不收集個人資訊，並接受匿名付款方式。

**最低合格要求：**

- [匿名加密貨幣](cryptocurrency.md) **或** 現金支付選項。
- 註冊時無需個人資料：最多只需提供使用者名稱、密碼和電子郵件。

**最佳情況：**

- 接受多種 [匿名付款方式](advanced/payments.md)。
- No personal information accepted (auto-generated username, no email required, etc.).

### 安全

若 VPN 不能提供足夠安全性，它就毫無意義。 We require all our recommended providers to abide by current security standards. 理想中，預設他們會使用更多面向未來的加密方案。 我們要求有獨立的第三方來審核供應商的安全性，理想情況下是每年都能進行全方方面審計。

**最低合格要求：**

- 強固加密方案：具有 SHA-256 驗證的 OpenVPN；RSA-2048 或更好的握手協議；AES-256-GCM 或 AES-256-CBC 數據加密。
- 前向保密。
- 由信譽良好的第三方公司公布的安全審計。
- 使用全磁碟加密或僅使用 RAM 的 VPN 伺服器。

**最佳情況：**

- 最強加密：RSA-4096。
- (可選) 抗量子加密演算法。
- 前向保密。
- 由信譽良好的第三方公司執行公佈的全面安全審計。
- 漏洞獎勵計劃 和/或 協調漏洞披露過程。
- 僅使用 RAM 的 VPN 伺服器。

### 信任

您不會把財務交給身份作假的人處理，又怎會信任他們來處置您的網路資料？ 我們要求推薦的供應商公開其所有權或領導層級狀況。 我們也希望能夠看到經常性的透明度報告，尤其是如何處理政府要求的部份。

**最低合格要求：**

- 面向公眾的領導或所有權。
- 公司所在的司法管轄區不能強迫其進行秘密紀錄。

**最佳情況：**

- 面向公眾的領導。
- 經常性的透明度報告。

### 行銷

對於所推薦的 VPN 服務商，我們樂見更負責任的營銷。

**最低合格要求：**

- Must self-host analytics (i.e., no Google Analytics).

不得有任何不負責任的行銷：

- 保證 100% 匿名性保護。 當有人聲稱某件事 100% 可行時，這意味他對失敗也無從確定。 我們知道有許多方式可以輕易地去匿名化，例如：
    - 重複使用在沒有使用匿名軟體 (例如 Tor、VPN 等) 情況下訪問的個人資訊 (例如電子郵件帳戶，獨特的假名等)
    - [瀏覽器指紋](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- 聲稱單一迴路 VPN 比 Tor「更匿名」，Tor 是由至少三個多跳組成，且經常變化的迴路。
- 使用負責任的用詞：例如，可以說 VPN 已「斷線」或「未連接」，但聲稱某人「已暴露」、「易受攻擊」或「受到威脅」則是不必要且容易造成誤導的驚嚇用語。 例如，此人可能只是正在使用其他 VPN 提供商的服務或 Tor。

**最佳情況：**

負責任的行銷，既具教育意義又對消費者實用，可能包括：

- 準確比較何時應該使用 [Tor](tor.md)。
- VPN 服務商網站可否透過 [.onion 服務](https://en.wikipedia.org/wiki/.onion)造訪。

### 附加功能

雖不是嚴格要求，在決定推薦哪些服務商時我們還會考慮其他一些便利或隱私因素。 其中包括內容封鎖功能、金絲雀安全聲明 (warrant canaries)、出色的客服支援、同時允許連接的數量等。
