---
meta_title: "私密 VPN 服務建議和比較，無任何贊助商或廣告 - Privacy Guides"
title: "VPN 服務"
icon: material/vpn
description: 保護您線上隱私與安全的最佳 VPN 服務。 在這裡尋找一個不會監視您的供應商。
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

## 推薦的提供商

我們推薦的供應商使用加密技術，支援 WireGuard & OpenVPN，並有無記錄政策。 閱讀我們[完整的標準清單](#criteria)，瞭解更多資訊。

| 供應商                   | 國家   | WireGuard                     | 端口轉發                                                   | IPv6                                                       | 匿名支付      |
| --------------------- | ---- | ----------------------------- | ------------------------------------------------------ | ---------------------------------------------------------- | --------- |
| [Proton](#proton-vpn) | 112+ | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Partial Support | :material-information-outline:{ .pg-blue } Limited Support | 現金        |
| [IVPN](#ivpn)         | 37+  | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                 | :material-information-outline:{ .pg-blue } 僅限連出流量          | Monero、現金 |
| [Mullvad](#mullvad)   | 45+  | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                 | :material-check:{ .pg-green }                              | Monero、現金 |

### Proton VPN

<div class="admonition recommendation" markdown>

![Proton VPN 標誌](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** 是 VPN 領域的強大競爭者，自 2016 年開始營運。 Proton AG 總部位於瑞士，提供有限的免費方案，以及更多功能的付費方案。

[:octicons-home-16: 首頁](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title="文檔"}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://protonvpn.com/download-windows)
- [:simple-apple: macOS](https://protonvpn.com/download-macos)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 112 個國家

Proton VPN [在 112 個國家設有伺服器](https://protonvpn.com/vpn-servers)，如果您使用其[免費計劃](https://protonvpn.com/free-vpn/server)，則在[5 個](https://protonvpn.com/support/how-to-create-free-vpn-account)國家設有伺服器。(1) 選擇伺服器距離您最近的 VPN 供應商可減少網路延遲。 這是因為到達目的地的路徑較短 (跳數較少)。
{ .annotate }

1. 最近檢查日期: 2024-08-06

我們認為，如果 VPN 提供商使用[專用伺服器](https://en.wikipedia.org/wiki/Dedicated_hosting_service)，而不是更便宜、與其他客戶共享的解決方案 (例如[虛擬伺服器](https://en.wikipedia.org/wiki/Virtual_private_server))，對其私鑰的安全性會更好。

#### :material-check:{ .pg-green } 獨立稽核

截至 2020 年 1 月， Proton VPN 已通過 SEC Consult 的獨立審計。 SEC Consult 在 Proton VPN Windows、Android 和 iOS 應用程式中發現一些中低風險漏洞，Proton VPN 已在報告發布之前全部 “妥善修復” 了這些漏洞。 所發現的問題都不會讓攻擊者遠端存取您的裝置或流量。 您可以在 [protonvpn.com](https://protonvpn.com/blog/open-source) 查看各個平臺的報告。 2022 年 4 月，Proton VPN 接受[另一次審核](https://protonvpn.com/blog/no-logs-audit)。 [Securitum](https://research.securitum.com) 於 2021 年 11 月 9 日簽發 Proton VPN 的[應用程式認證函](https://proton.me/blog/security-audit-all-proton-apps) 。

#### :material-check:{ .pg-green } 開源客戶端

Proton VPN 在其 [GitHub 組織](https://github.com/ProtonVPN) 中提供桌面和行動裝置客戶端的原始碼。

#### :material-check:{ .pg-green } 接受現金

除了信用卡/簽帳卡、PayPal 和 [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) 以外，Proton VPN 還接受 **現金/當地貨幣** 等匿名付款方式。

#### :material-check:{ .pg-green } 支援 WireGuard

Proton VPN 支援 WireGuard® 協議。 [WireGuard](https://wireguard.com/protocol) 是一種較新的協議，使用最先進的[密碼學](https://wireguard.com)。 此外，WireGuard 的目標是更簡單，更高效。

Proton VPN [推薦](https://protonvpn.com/blog/wireguard)搭配 WireGuard 使用。 在 Proton VPN 的 Windows、macOS、iOS、Android、ChromeOS 以及 Android TV 等平台的應用程式中，WireGuard 已是預設協議；然而， Linux 作業系統的應用程式[尚未支援](https://protonvpn.com/support/how-to-change-vpn-protocols)此協議。

#### :material-alert-outline:{ .pg-orange } Limited IPv6 Support

Proton [now supports IPv6](https://protonvpn.com/support/prevent-ipv6-vpn-leaks) in their browser extension but only 80% of their servers are IPv6-compatible. On other platforms, the Proton VPN client will block all outgoing IPv6 traffic, so you don't have to worry about your IPv6 address being leaked, but you will not be able to connect to any IPv6-only sites, nor will you be able to connect to Proton VPN from an IPv6-only network.

#### :material-information-outline:{ .pg-info } 遠端端口轉發

Proton VPN 目前僅支援通過 NAT-PMP 進行短暫的[遠端端口轉發](https://protonvpn.com/support/port-forwarding)，租用時間為 60 秒。 Windows 應用程式提供簡易使用選項，而其它作業系統則需運行 [NAT-PMP 客戶端](https://protonvpn.com/support/port-forwarding-manual-setup)。 BT 客戶端通常原生支援 NAT-PMP。

#### :material-information-outline:{ .pg-blue } 突破網路審查

Proton VPN 有自己的 [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) 協定，在其它 VPN 協定如 OpenVPN、WireGuard 遭封鎖時*可能*有所幫助。 Stealth 將 VPN 隧道封裝在 TLS 會話中，使其看起來像是一般的網路流量。

不幸的是，在部署了精密過濾器分析所有傳出流量以試圖發現加密隧道的國家，此方法的效果並不理想。 Stealth 可在 Android、iOS、Windows 和 macOS 上使用，但尚未在 Linux 上可用。

#### :material-check:{ .pg-green } 行動裝置客戶端

除了提供標準 OpenVPN 設定檔外，Proton VPN 還在 [App Store](https://apps.apple.com/app/id1437005085)、[Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android) 和 [GitHub](https://github.com/ProtonVPN/android-app/releases) 提供行動裝置客戶端，以供使用者方便連接到他們的伺服器。

#### :material-information-outline:{ .pg-blue } 補充說明

Proton VPN 客戶端目前支持所有平臺上的雙因素身份驗證。 Proton VPN 在瑞士、冰島和瑞典擁有自己的伺服器和資料中心。 他們透過自己的 DNS 服務，提供內容封鎖和已知的惡意軟體網域。 此外，Proton VPN 還提供 "Tor" 伺服器，可輕鬆連接到洋蔥網站，但我們仍然強烈建議您使用 [官方 Tor 瀏覽器](tor.md#tor-browser) 來完成此類目的。

##### :material-alert-outline:{ .pg-orange } Killswitch 無法在基於 Intel 處理器的 Mac 電腦上使用

基於 Intel 處理器的 Mac 電腦 若使用 VPN killswitch 可能會導致[系統崩潰](https://protonvpn.com/support/macos-t2-chip-kill-switch) 。 如果您需要此功能，但使用的是搭載 Intel 處理器的 Mac 電腦 ，則應考慮使用其他 VPN 服務。

### IVPN

<div class="admonition recommendation" markdown>

![IVPN logo](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** 是另一個高級 VPN 提供商，自 2009 年開始運營。 IVPN 位於直布羅陀，不提供免費試用。

[:octicons-home-16: 首頁](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title="文檔"}
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

IVPN 在 [37 個國家/地區設有伺服器](https://ivpn.net/status)。 (1) 選擇擁有距離您最近的伺服器之 VPN 供應商，可減少發送網路流量的延遲。 這是因為到達目的地的路徑較短 (跳數較少)。
{ .annotate }

1. 最近檢查日期: 2024-08-06

我們認為，如果 VPN 提供商使用[專用伺服器](https://en.wikipedia.org/wiki/Dedicated_hosting_service)，而不是更便宜、與其他客戶共享的解決方案 (例如[虛擬伺服器](https://en.wikipedia.org/wiki/Virtual_private_server))，對其私鑰的安全性會更好。

#### :material-check:{ .pg-green } 獨立稽核

IVPN 已通過 [Cure53 的無日誌審計](https://cure53.de/audit-report_ivpn.pdf)，該審計結果與 IVPN 的無日誌聲明一致。 IVPN 還在 2020 年 1 月完成了 [Cure53 的全面滲透測試報告](https://cure53.de/summary-report_ivpn_2019.pdf) 。 IVPN 也表示他們計劃在未來提供[年度報告](https://ivpn.net/blog/independent-security-audit-concluded)。 進一步的審核於 [2022 年 4 月](https://ivpn.net/blog/ivpn-apps-security-audit-2022-concluded)進行，並由 Cure53 [在其網站上公布](https://cure53.de/pentest-report_IVPN_2022.pdf)。

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

IVPN has obfuscation modes using [v2ray](https://v2ray.com/en/index.html) which helps in situations where VPN protocols like OpenVPN or Wireguard are blocked. 此功能目前僅支援桌機版與 [iOS](https://ivpn.net/knowledgebase/ios/v2ray)。 可透過 QUIC 或 TCP 兩種模式連接 [VMess](https://guide.v2fly.org/en_US/basics/vmess.html)。 QUIC 是一個新的傳輸協議，具有更好的擁塞控管，因此可能速度更快，且延遲更低。 TCP 模式的數據呈現為一般的 HTTP 流量。

#### :material-check:{ .pg-green } 行動裝置客戶端

除了提供標準 OpenVPN 設定檔外，IVPN 還在 [App Store](https://apps.apple.com/app/id1193122683)、[Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client) 和 [GitHub](https://github.com/ivpn/android-app/releases) 提供行動裝置客戶端，以供使用者方便連接到他們的伺服器。

#### :material-information-outline:{ .pg-blue } 補充說明

IVPN 用戶端支援雙因子身份驗證。 IVPN 有「[反追蹤](https://ivpn.net/antitracker)」功能，以阻絕來自網路層的廣告與追蹤。

### Mullvad

<div class="admonition recommendation" markdown>

![Mullvad 標誌](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** 是一個快速且便宜的 VPN，非常注重透明和安全性。 他們自 2009 年起開始營運。 Mullvad is based in Sweden and offers a 30-day money-back guarantee for payment methods that allow it.

[:octicons-home-16: 首頁](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="洋蔥服務" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title="文檔" }
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

#### :material-check:{ .pg-green } 45 個國家

Mullvad 在 [45 個國家/地區設有伺服器](https://mullvad.net/servers)。 (1) 選擇距離您最近的伺服器，可減少網路流量的延遲。 這是因為到達目的地的路徑較短 (跳數較少)。
{ .annotate }

1. 最近檢查日期: 2024-08-06

我們認為，如果 VPN 提供商使用[專用伺服器](https://en.wikipedia.org/wiki/Dedicated_hosting_service)，而不是更便宜、與其他客戶共享的解決方案 (例如[虛擬伺服器](https://en.wikipedia.org/wiki/Virtual_private_server))，對其私鑰的安全性會更好。

#### :material-check:{ .pg-green } 獨立稽核

Mullvad 的 VPN 客戶端已通過 Cure53 和 Assured AB 的滲透測試審計，報告[發布於 cure53.de](https://cure53.de/pentest-report_mullvad_v2.pdf)。 安全研究人員得出結論：

> Cure53 和 Assured AB 對審計結果感到滿意，對該軟體整體留下正面的印象。 憑藉 Mullvad VPN 內部團隊在安全方面的投入，測試人員從安全角度判斷該項目走在正確的軌道上。

2020 年，[宣布](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app)進行第二次審計，[最終審計報告](https://cure53.de/pentest-report_mullvad_2020_v2.pdf)已發布在 Cure53 網站上：

> 2020年5月~6月針對 Mullvad  的專案結果是相當正面。 [...] Mullvad 使用的整體應用生態系統給人留下了健全且結構完善的印象。 應用程式整體使用結構化的方式，可更輕鬆地推出補丁和修復措施。 最重要的是，Cure53 所發現的結果展示了持續審計和重新評估當前資訊泄漏途徑的重要性，以始終確保終端使用者的隱私。 Mullvad 在保護終端用戶免受常見的 PII 洩漏和隱私相關風險方面做得很好。

2021 年[宣布](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit)進行基礎設施審計，[最終審計報告](https://cure53.de/pentest-report_mullvad_2021_v1.pdf)已在 Cure53 網站上發布。 另一份報告已於 [2022 年 6 月](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data)發布，可在 [Assured 的網站](https://assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf) 上取得。

#### :material-check:{ .pg-green } 開源客戶端

Mullvad 在其 [GitHub 組織](https://github.com/mullvad/mullvadvpn-app) 中提供桌面和行動裝置客戶端的原始碼。

#### :material-check:{ .pg-green } 接受現金和 Monero

除了接受信用卡/簽帳卡和 PayPal 外， Mullvad 還接受比特幣, Bitcoin Cash **Monero** 和 **現金/當地貨幣** （年度方案繳費）作為匿名付款方式。 也提供帶有兌換代碼的預付卡。 Mullvad also accepts Swish and bank wire transfers, as well as a few European payment systems.

#### :material-check:{ .pg-green } 支援 WireGuard

Mullvad 支援 WireGuard® 協議。 [WireGuard](https://wireguard.com/protocol) 是一種較新的協議，使用最先進的[密碼學](https://wireguard.com)。 此外，WireGuard 的目標是更簡單，更高效。

Mullvad [建議](https://mullvad.net/en/help/why-wireguard)搭配 WireGuard 使用。 在 Mullvad 的 Android、iOS、macOS 以及 Linux 平台的應用程式中，WireGuard 已是預設協議；在 Windows 平台則需[手動選擇](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard。 Mullvad 也提供 WireGuard 設定檔產生器，可用於 WireGuard 的官方[應用程式](https://wireguard.com/install)。

#### :material-check:{ .pg-green } IPv6 支持

Mullvad 允許您[存取架設在 IPv6 上的服務](https://mullvad.net/en/blog/2014/9/15/ipv6-support)，且支援使用 IPv6 的裝置連線。

#### :material-alert-outline:{ .pg-orange } 遠端端口轉發

Mullvad 曾支援遠端端口轉發，但在 [2023 年 5 月](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports) 移除了此功能。 缺少此功能可能會對某些應用程式造成負面影響，尤其是 BT 客戶端等點對點應用程式。

#### :material-check:{ .pg-green } 突破網路審查

Mullvad offers several features to help bypass censorship and access the internet freely:

- **Obfuscation modes**: Mullvad has two built-in obfuscation modes: "UDP-over-TCP" and ["Wireguard over Shadowsocks"](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard). These modes disguise your VPN traffic as regular web traffic, making it harder for censors to detect and block. Supposedly, China has to use a [new method to disrupt Shadowsocks-routed traffic](https://gfw.report/publications/usenixsecurity23/en).
- **Advanced obfuscation with Shadowsocks and v2ray**: For more advanced users, Mullvad provides a guide on how to use the [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) plugin with Mullvad clients. This setup provides an additional layer of obfuscation and encryption.
- **Custom server IPs**: To counter IP-blocking, you can request custom server IPs from Mullvad's support team. Once you receive the custom IPs, you can input the text file in the "Server IP override" settings, which will override the chosen server IP addresses with ones that aren't known to the censor.
- **Bridges and proxies**: Mullvad also allows you to use bridges or proxies to reach their API (needed for authentication), which can help bypass censorship attempts that block access to the API itself.

#### :material-check:{ .pg-green } 行動裝置客戶端

Mullvad 提供 [App Store](https://apps.apple.com/app/id1488466513) 和 [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) 客戶端，兩者都支持易於使用的界面，無須手動配置 WireGuard。 Android 客戶端也可以在 [GitHub](https://github.com/mullvad/mullvadvpn-app/releases) 上下載。

#### :material-information-outline:{ .pg-blue } 補充說明

Mullvad 對於他們[自有或租用](https://mullvad.net/en/servers)的節點透明度非常好。 They also provide the option to enable Defense Against AI-guided Traffic Analysis ([DAITA](https://mullvad.net/en/blog/daita-defense-against-ai-guided-traffic-analysis)) in their apps. DAITA protects against the threat of advanced traffic analysis which can be used to connect patterns in VPN traffic with specific websites.

## 標準

<div class="admonition danger" markdown>
<p class="admonition-title">危險</p>

注意，使用 VPN 不會使您匿名，但在某些情況下可以提供更好的隱私。 VPN 不是非法活動的工具。 不要依賴「無日誌」政策。

</div>

**請注意我們和所推薦的服務商沒有任何利害關係。 這使我們能夠提供完全客觀的建議。** 除了 [我們的標準條件](about/criteria.md)外，我們還為任何希望獲得推薦的 VPN 服務商制定了一套明確的要求，包括強大的加密、獨立的安全審計、現代技術等。 我們建議您在選擇 VPN 供應商之前先熟悉此清單，並進行自己的研究，盡可能地確保您選擇的 VPN 供應商值得信賴。

### 技術

我們要求所有推薦的 VPN 服務商有提供 OpenVPN 配置檔案，以便用在任何客戶端。 **如果** VPN 提供自己的客戶端，則要求有 killswitch 來阻止未連接 VPN 時網路資料遭洩漏。

**最低合格要求：**

- 支援強固的協議，如 WireGuard & OpenVPN。
- 客戶端內建 Killswitch。
- 支援多跳連接 (Multihop)。 萬一單個節點受損，多跳方式就非常重要，才能保持數據的私密性。
- 如有提供 VPN 用戶端，則應為 [開源](https://en.wikipedia.org/wiki/Open_source)，一如所內建的 VPN 軟體。 我們相信，可取得的[源代碼](https://en.wikipedia.org/wiki/Source_code)可為用戶設備實際運作提供更高的透明度。
- Censorship resistance features designed to bypass firewalls without DPI.

**最佳案例：**

- Killswitch 具高度可配置選項（啟用/禁用某些網路、開機時等等）
- 易於使用的 VPN 客戶端
- [IPv6](https://en.wikipedia.org/wiki/IPv6) support. 我們預期伺服器將允許透過 IPv6 傳入連線，並允許您存取託管在 IPv6 位址上的服務。
- [遠端端口轉發](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) 的功能可協助在使用P2P ([對等](https://en.wikipedia.org/wiki/Peer-to-peer)) 檔案共享軟體或自建伺服器 (例如 Mumble) 時建立連接。
- Obfuscation technology which camouflages the true nature of internet traffic, designed to circumvent advanced internet censorship methods like DPI.

### 隱私

我們希望所推薦的提供商盡可能減少客戶資料收集。 不收集註冊時的個人資訊，並接受匿名形式的付款是必需的。

**最低合格要求：**

- [匿名加密貨幣](cryptocurrency.md) **或** 現金支付選項。
- 註冊時無需個人資料：最多只需提供使用者名稱、密碼和電子郵件。

**最佳案例：**

- 接受多種 [匿名付款方式](advanced/payments.md)。
- 無需任何個人資訊（自動生成的用戶名稱、不要求電子郵件等）。

### 安全

若 VPN 不能提供足夠安全性，它就毫無意義。 我們要求所有推薦的供應商遵守其 OpenVPN 連接的現行安全標準。 理想中，預設他們會使用更多面向未來的加密方案。 我們要求有獨立的第三方來審核供應商的安全性，理想情況下是每年都能進行全方方面審計。

**最低合格要求：**

- 強固加密方案：具有 SHA-256 驗證的 OpenVPN；RSA-2048 或更好的握手；AES-256-GCM 或 AES-256-CBC 數據加密。
- 前向保密。
- 由信譽良好的第三方公司執行公佈的全面安全審計。
- VPN servers that use full-disk encryption or are RAM-only.

**最佳案例：**

- 最強加密： RSA-4096。
- Optional quantum-resistant encryption.
- 前向保密。
- 由信譽良好的第三方公司執行公佈的全面安全審計。
- 漏洞獎勵計劃 和/或 協調漏洞披露過程。
- RAM-only VPN servers.

### 信任

您不會把財務資料交給身份作假的人，又怎會信任他們來處置您的網路資料？ 我們要求推薦的供應商公開其所有權或領導層級狀況。 我們也希望看到頻繁的透明度報告，特別是關於如何處理政府要求的報告。

**最低合格要求：**

- 面向公眾的領導或所有權。
- Company based in a jurisdiction where it cannot be forced to do secret logging.

**最佳案例：**

- 面向公眾的領導。
- 頻繁的透明度報告。

### 行銷

對於所推薦的 VPN 服務商，我們樂見更負責任的營銷。

**最低合格要求：**

- 必須自行託管分析工具 (例如不使用 Google Analytics)。 供應商的網站還必須遵守 [DNT (Do Not Track, 請勿追蹤) ](https://en.wikipedia.org/wiki/Do_Not_Track) 的要求，以供選擇退出的人使用。

不得有任何不負責任的行銷：

- 保證 100% 匿名性保護。 當有人聲稱某件事 100% 可行時，這意味他對失敗也無從確定。 我們知道有許多方式可以輕易地去匿名化，例如：
    - 重複使用在沒有使用匿名軟體 (例如 Tor、VPN 等) 情況下訪問的個人資訊 (例如電子郵件帳戶，獨特的假名等)
    - [瀏覽器指紋](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- 聲稱單一迴路 VPN 比 Tor “更匿名” ， Tor 是由三個或更多個跳組成經常變化的迴路。
- 使用負責任的語言：也就是說，可以說VPN “已斷開”或“未連接” ，但是聲稱某人“暴露” ， “易受攻擊”或“受損”是不必要的使用可能不正確的警告語言。 例如，此人可能只是使用其他VPN提供商的服務或使用Tor。

**最佳案例：**

負責任的行銷，既具教育意義又對消費者實用，可能包括：

- 與何時應使用 [Tor](tor.md) 的準確比較。
- VPN 服務商網站可否透過 [.onion 服務](https://en.wikipedia.org/wiki/.onion)訪問。

### 附加功能

雖不是嚴格要求，在決定推薦哪些服務商時我們還會考慮其他一些便利或隱私因素。 These include content blocking functionality, warrant canaries, excellent customer support, the number of allowed simultaneous connections, etc.
