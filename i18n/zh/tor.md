---
meta_title: "Tor 浏览器与网络：匿名网页浏览 - Privacy Guides"
title: "Tor浏览器"
icon: simple/torbrowser
description: 使用可规避审查的安全网络 Tor，保护您的网络浏览免受窥探。
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor浏览器
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
    sameAs: https://en.wikipedia.org/wiki/Tor_(network)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows 系统
      - mac系统
      - Linux系统
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>防御以下威胁：</small>

- [:material-account-cash: 监视资本主义](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: 大规模监控](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: 审查](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

**Tor** 是一组由志愿者运营的服务器，允许您免费连接并提高您在互联网上的隐私和安全性。个人和组织也可以通过Tor网络与".onion隐藏服务"分享信息，而不损害其隐私。由于Tor流量难以阻止和跟踪，因此Tor是一种有效的审查规避工具。

[Tor 详细概述 :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: 视频：为什么你需要 Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">提示</p>

在连接到 Tor 之前，请确保您已经阅读了我们的[概述](advanced/tor-overview.md)，了解 Tor 是什么以及如何安全地连接它。我们通常建议通过受信任的 [VPN 提供商](vpn.md)连接到 Tor，但您必须**正确**操作，以避免降低您的匿名性。

</div>

从您的设备连接到 Tor 网络有多种方式，最常用的是 **Tor 浏览器**，它是 Firefox 的一个分支，专为桌面计算机和 Android 上的 [:material-incognito: 匿名](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} 浏览而设计。

这些应用中有些比其他的更好；如何决定取决于您的威胁模型。如果您只是偶尔使用 Tor，且不担心您的 ISP 收集对您不利的证据，那么使用像 [Onion Browser](#onion-browser-ios) 这样的移动浏览器应用来访问 Tor 网络可能就足够了。增加日常使用 Tor 的人数有助于减少 Tor 的不良污名，并降低 ISP 和政府可能编制的“Tor 用户列表”的质量。

如果更彻底的匿名性对您的情况至关重要，您应该**只**使用桌面版 Tor 浏览器客户端，最好是在 [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os) 配置下。移动浏览器在 Tor 上较少见（因此更容易被指纹识别），并且其他配置在防止去匿名化方面没有经过如此严格的测试。

## Tor浏览器

<div class="admonition recommendation" markdown>

![Tor Browser logo](assets/img/browsers/tor.svg){ align=right }

如果您需要匿名，**Tor 浏览器** 是首选，因为它为您提供了访问 Tor 网络和网桥的途径，并且包含了由默认安全级别（*标准*、*较安全* 和 *最安全*）自动配置的默认设置和扩展。

[:octicons-home-16: 主页](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="洋葱服务" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title="文档" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="源代码" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title="贡献" }

<details class="downloads" markdown>
<summary>下载</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:fontawesome-brands-windows: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">危险</p>

您**绝不**应该在 Tor 浏览器上安装任何额外的扩展或编辑 `about:config` 设置，包括我们为 Firefox 建议的那些。浏览器扩展和非标准设置会使您在 Tor 网络中显得与众不同，从而使您的浏览器更容易被[指纹识别](https://support.torproject.org/glossary/browser-fingerprinting)。

</div>

Tor浏览器旨在防止指纹识别，或根据您的浏览器配置识别您。因此，您**绝不能**修改默认[安全级别](https://tb-manual.torproject.org/security-settings)之外的浏览器设置，这一点至关重要。在修改安全级别设置时，您**必须**始终重启浏览器，然后再继续使用。否则，[安全设置可能无法完全生效](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw)，这会使您面临比根据所选设置所预期的更高的指纹识别和漏洞利用风险。

除了直接在您的计算机上安装 Tor 浏览器外，还有专门设计用于连接 Tor 网络的操作系统，例如 [Qubes OS](desktop.md#qubes-os) 上的 [Whonix](desktop.md#whonix)，它们提供比单独使用标准 Tor 浏览器更高的安全性和保护。

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** 是一款开源浏览器，可让您在 iOS 设备上通过 Tor 网络匿名浏览网页，并获得了 [Tor 项目](https://support.torproject.org/glossary/onion-browser)的认可。

[:material-star-box: 阅读我们最新的 Onion Browser 评测。](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review)

[:octicons-home-16: 主页](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="隐私政策" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title="文档" }
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="源代码" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title="贡献" }

<details class="downloads" markdown>
<summary>下载</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser 无法提供与桌面平台上的 Tor 浏览器相同级别的隐私保护。对于日常使用，它是访问隐藏服务的绝佳方式，但如果您担心被高级对手追踪或监控，则不应将其作为匿名工具来依赖。

[值得注意的是](https://github.com/privacyguides/privacyguides.org/issues/2929)，Onion Browser 并不*保证*所有请求都通过 Tor 进行。当使用内置版本的 Tor 时，由于 WebKit 的限制，[您的真实 IP **将**通过 WebRTC 和音视频流泄露](https://onionbrowser.com/faqs)。将 Onion Browser 与 [Orbot](alternative-networks.md#orbot) 配合使用会*更安全*，但这在 iOS 上仍然存在一些限制。
