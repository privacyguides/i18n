---
meta_title: "Tor瀏覽器與網絡:匿名網頁瀏覽 - Privacy Guides"
title: "Tor 瀏覽器"
icon: simple/torbrowser
description: 透過Tor 網絡來保護您的網際網路瀏覽免受窺探， Tor 網絡是一個規避審查的安全網絡。
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
    sameAs: https://en.wikipedia.org/wiki/Tor_(network)
    applicationCategory: 網頁瀏覽器
    operatingSystem:
      - Windows 作業系統
      - macOS
      - Linux
      - Android
    subjectOf:
      "@type": 網頁
      url: "./"
---

<small>防護下列威脅：</small>

- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: 大規模監控](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: 審查](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

**Tor** 網絡是一組由志願者操作的伺服器，可讓您免費連線，並改善您的隱私權和安全性。 個人和組織還可以通過 Tor 網絡與“.onion 隱藏服務”分享資訊，而不會損害他們的隱私。 很難阻止和追蹤 Tor 流量，因此它是一種有效的審查規避工具。

[詳細的 Tor 總覽  :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">溫馨提示</p>

在連接 Tor 之前，請先已閱讀[本站相關介紹概述](advanced/tor-overview.md)，了解 Tor 是什麼以及如何安全地連接使用。 通常建議透過值得信賴的 [VPN 供應商](vpn.md) 來連接 Tor，但其操作必須**正確**，以避免降低匿名性。

</div>

從裝置連線到 Tor 網路的方式有多種，最常用的是 **Tor 瀏覽器** ，它是 Firefox 的分叉，專為在電腦和Android上 [:material-incognito: 匿名](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} 瀏覽而設計

其些應用程式比其他應用程式更好，但再次提醒其選用決定取決於您的威脅模型。 如果是Tor 的一般使用者，不擔心 ISP 收集針對您的證據，那麼使用[Orbot](#orbot) 等應用程式或行動瀏覽器應用程式訪用 Tor 網絡可能沒問題。 越多人使用 Tor 有助於減少 Tor 的不良印記，降低 ISP 和政府可能編制的「Tor 用戶清單」內容。

如果更完全的匿名至關重要，則應 **僅使用** 桌面版的 Tor 客戶端應用，最好再加上[Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os) 一起搭配使用。 行動瀏覽器在 Tor 上較不常見 (因此也更容易被識別指紋)，而且其所採用的其他配置也沒有經過嚴格的去匿名化測試。

## Tor 瀏覽器

<div class="admonition recommendation" markdown>

![Tor 瀏覽器標誌](assets/img/browsers/tor.svg){ align=right }

**Tor 瀏覽器** 需要匿名的好選擇，為您提供 Tor 網絡和橋接的存取權限，它包含預設設置和擴展其自動配置安全級別有： *標準* 、 *更安全*和*最安全*三種。

[:octicons-home-16: Homepage](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:fontawesome-brands-windows: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger "危險"</p>

您應該 **永遠不要** 在Tor瀏覽器上安裝任何其他擴充功能，或編輯「關於：配置」設定，包括我們為Firefox建議的設定。 瀏覽器擴充套件和非標準設置會使您在 Tor 網絡上突顯出來，從而使您的瀏覽器更容易變成 [fingerprint](https://support.torproject.org/glossary/browser-fingerprinting)。

</div>

Tor 瀏覽器旨在防止指紋識別----根據您的瀏覽器配置識別您。 因此， **不應** 修改瀏覽器超出預設 [安全級別](https://tb-manual.torproject.org/security-settings)。

除了直接在電腦安裝 Tor 瀏覽器外，還有專門設計用於連接到 Tor 網絡的操作系統，例如 [Qubes OS 作業系統](desktop.md#qubes-os) [Whonix](desktop.md#whonix)，它們提供比標準 Tor 瀏覽器更高的安全性和保護。

## Orbot

<div class="admonition recommendation" markdown>

![Orbot標誌](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** 是一款免費的Tor VPN ，適用於智慧型手機，可讓裝置上的任何應用程式流量通過 Tor 網絡。

[:octicons-home-16: Homepage](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

</details>

</div>

我們之前建議在 Orbot 設定中啟用 *隔離目標地址* 偏好設定。 雖然從理論上講，此設置可以強制您連接不同 IP地址使用不同的迴路來改善隱私，但它並未為大多數應用程式（特別是 Web瀏覽）提供實際優勢，可能會帶來顯著的效能拖累，增加 Tor 網絡的負載。 我們不再建議您從預設值調整此設定，除非您知道需要調整。[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Android 提示</p>

Orbot 可以代理個別應用程式，如果它們有支援 SOCKS 或 HTTP 代理。 它也能使用 [VpnService](https://developer.android.com/reference/android/net/VpnService) 代理您的所有網路連接，其 VPN killswitch 設置在 :gear: **Settings** → **Network &amp; internet** → **VPN** → :gear: → **Block connections without VPN**.。

Guardian Project 的[F-Droid repository](https://guardianproject.info/fdroid)和 [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android) 上Orbot 往往不是最新版，因此請考慮直接從 [GitHub repository](https://github.com/guardianproject/orbot/releases) 下載。

所有版本都使用同一個簽名，因此它們應該相互兼容。

</div>

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion 瀏覽器** 是開源瀏覽器，其可讓您在 iOS 設備上匿名瀏覽 Tor 網絡，其有 [Tor Project](https://support.torproject.org/glossary/onion-browser/)之保證。 [:material-star-box: 閱讀我們最新的 Onion Browser 評論](/articles/2024/09/18/onion-browser-review/)

[:octicons-home-16: 首頁](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=文檔}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="原始碼" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=捐款 }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser 不提供與 Tor Browser 在電腦平台上相同等級的隱私保護。 對於日常使用而言，這是存取隱藏服務的絕佳方式，但如果您擔心被先進的對手追蹤或監視，則不應將其視為匿名工具。

[^1]: `IsolateDestAddr` 設定問題已在 [Tor 郵件群組](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) 中討論過而且在 [Whonix's 串流隔離文檔](https://whonix.org/wiki/Stream_Isolation)，兩項專案都認為對大多數人而言它並不是好方法。
