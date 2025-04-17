---
meta_title: "Tor瀏覽器與網路：匿名網頁瀏覽 - Privacy Guides"
title: "Tor 瀏覽器"
icon: simple/torbrowser
description: 透過Tor 網路來保護您的網際網路瀏覽免受窺探， Tor 網路是一個規避審查的安全網路。
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
    sameAs: https://zh.wikipedia.org/wiki/Tor
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

**Tor** 網路是一組由志願者操作的伺服器，可讓您免費連線，並改善您的隱私權和安全性。 個人和組織還可以通過 Tor 網路與“.onion 隱藏服務”分享資訊，而不會侵犯他們的隱私。 很難阻止和追蹤 Tor 流量，因此它是一種有效的審查規避工具。

[Detailed Tor Overview :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: Video: Why You Need Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor/ ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">溫馨提示</p>

在連接 Tor 之前，請先已閱讀[本站相關介紹概述](advanced/tor-overview.md)，了解 Tor 是什麼以及如何安全地連接使用。 通常建議透過值得信賴的 [VPN 供應商](vpn.md) 來連接 Tor，但其操作必須**正確**，以避免降低匿名性。

</div>

從裝置連線到 Tor 網路的方式有多種，最常用的是 **Tor 瀏覽器** ，它是 Firefox 的分叉，專為在電腦和Android上 [:material-incognito: 匿名](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} 瀏覽而設計

其些應用程式比其他應用程式更好，但再次提醒其選用決定取決於您的威脅模型。 If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using mobile browser apps like [Onion Browser](#onion-browser-ios) to access the Tor network is probably fine. 越多人使用 Tor 有助於減少 Tor 的不良印記，降低 ISP 和政府可能編制的「Tor 用戶清單」內容。

如果更完全的匿名至關重要，則應 **僅使用** 桌面版的 Tor 客戶端應用，最好再加上[Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os) 一起搭配使用。 Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

## Tor 瀏覽器

<div class="admonition recommendation" markdown>

![Tor 瀏覽器標誌](assets/img/browsers/tor.svg){ align=right }

**Tor 瀏覽器** 需要匿名的好選擇，為您提供 Tor 網路和橋接的存取權限，它包含預設設定和擴展其自動配置安全級別有： *標準* 、 *較安全*和*最安全*三種。

[:octicons-home-16: 首頁](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="洋蔥服務" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=文檔 }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="原始碼" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=捐款 }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:fontawesome-brands-windows: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger "危險"</p>

您應該 **永遠不要** 在Tor瀏覽器上安裝任何其他擴充功能，或編輯「關於：配置」設定，包括我們為Firefox建議的設定。 瀏覽器擴充套件和非標準設定會使您在 Tor 網路上曝露，從而使您的瀏覽器更容易變成 [fingerprint](https://support.torproject.org/glossary/browser-fingerprinting)。

</div>

Tor 瀏覽器旨在防止指紋識別----根據您的瀏覽器配置識別您。 因此， **不應** 修改瀏覽器超出預設 [安全級別](https://tb-manual.torproject.org/security-settings)。

除了直接在電腦安裝 Tor 瀏覽器外，還有專門設計用於連接到 Tor 網路的操作系統，例如 [Qubes OS 作業系統](desktop.md#qubes-os) ＋ [Whonix](desktop.md#whonix) ，它們提供比標準 Tor 瀏覽器更高的安全性和保護。

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion 瀏覽器** 是開源瀏覽器，其可讓您在 iOS 設備上匿名瀏覽 Tor 網路，其有 [Tor Project](https://support.torproject.org/glossary/onion-browser/)之保證。 [:material-star-box: Read our latest Onion Browser review.](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review/)

[:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser 不提供與 Tor Browser 在電腦平台上相同等級的隱私保護。 對於日常使用而言，這是存取隱藏服務的絕佳方式，但如果您擔心被先進的對手追蹤或監視，則不應將其視為匿名工具。

[Notably](https://github.com/privacyguides/privacyguides.org/issues/2929), Onion Browser does not *guarantee* all requests go through Tor. When using the built-in version of Tor, [your real IP **will** be leaked via WebRTC and audio/video streams](https://onionbrowser.com/faqs) due to limitations of WebKit. It is *safer* to use Onion Browser alongside [Orbot](alternative-networks.md#orbot), but this still comes with some limitations on iOS.
