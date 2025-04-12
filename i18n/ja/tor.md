---
meta_title: "Tor Browserとネットワーク: 匿名のウェブブラウジング - Privacy Guides"
title: "Tor Browser"
icon: simple/torbrowser
description: 検閲を回避するセキュアなネットワークであるTorネットワークにより、詮索からインターネットブラウジングを保護する。
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
    sameAs: https://en.wikipedia.org/wiki/Tor_(network)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>以下の脅威から保護します：</small>

- [:material-account-cash: 監視資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: 監視社会](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: 検閲](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

**Tor**はボランティアによるサーバー群で、無償で接続が可能であり、インターネット上のプライバシーとセキュリティを向上させることができます。 個人や組織は、プライバシーを損なうことなく、Torネットワーク上で「.onion 秘匿サービス」による情報共有が可能です。 Torトラフィックはブロックや追跡が困難であるため、Torは効果的な検閲回避ツールです。

[Torの概要 :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: 動画：Torが必要な理由](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor/ ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">ヒント</p>

Torに接続する前に、Torと安全に接続する方法についての[概要](advanced/tor-overview.md)を読んでください。 信頼できる[VPNプロバイダー](vpn.md)経由でTorに接続することを推奨しますが、匿名性を低下させないよう**適切に**接続する必要があります。

</div>

Torネットワークへの接続は様々な方法がありますが、Firefoxをフォークし、デスクトップやAndroid用で[:material-incognito: 匿名](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple}ブラウジングを重視した**Tor Browser**が最も利用されています。

Torネットワークに接続するアプリには長短があり、どれを使うかは脅威モデルによります。 ISPが不利な証拠を集めることについて心配しないTorのカジュアルなユーザーであれば、[Orbit](#orbot)などのモバイルブラウザからTorネットワークに接続することは良い方法です。 日常的にTorを使う人が増えることはTorのマイナスイメージをやわらげ、ISPや政府が作成しているかもしれない「Torユーザーリスト」の質を下げることになります。

完全な匿名性が最優先であるなら、デスクトップのTor Browser**のみ**を使うべきであり、[Whonix](desktop.md#whonix)と[Qubes](desktop.md#qubes-os)の構成が理想的です。 モバイルブラウザではTorはあまり使われておらず（そのためフィンガープリンティングされやすい）、匿名化解除に対して厳密にテストはされていません。

## Tor Browser

<div class="admonition recommendation" markdown>

![Tor Browser logo](assets/img/browsers/tor.svg){ align=right }

**Tor Browser**は匿名性に重点をおいたブラウザで、Torネットワークとブリッジへアクセスできます。デフォルトの設定と拡張機能が含まれており、セキュリティのレベル*既定の保護*、*強力な保護*、*最大限の保護*を選ぶことで自動的に設定されます。

[:octicons-home-16: ウェブページ](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=ドキュメント }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="ソースコード" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=貢献 }

<details class="downloads" markdown>
<summary>ダウンロード</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:fontawesome-brands-windows: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">警告</p>

Firefoxでおすすめされているものを含め、Tor Browserに追加の拡張機能をインストールしたり、「about:config」の設定を変更したりは、**絶対に**しないでください。 ブラウザ拡張機能や非標準の設定により、Torネットワーク上の他のユーザとあなたが区別されやすくなり、[フィンガープリント](https://support.torproject.org/glossary/browser-fingerprinting)されやすくなります。

</div>

Tor Browserはフィンガープリントを防止するよう設計されており、不用意にブラウザの設定を変更するとあなたは特定されやすくなってしまいます。 そのため、デフォルトの[セキュリティレベル](https://tb-manual.torproject.org/security-settings)を調整する以外の変更は**行うべきではありません**。

In addition to installing Tor Browser on your computer directly, there are also operating systems designed specifically to connect to the Tor network such as [Whonix](desktop.md#whonix) on [Qubes OS](desktop.md#qubes-os), which provide even greater security and protections than the standard Tor Browser alone.

## Orbot

<div class="admonition recommendation" markdown>

![Orbot logo](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** is a free Tor VPN for smartphones which routes traffic from any app on your device through the Tor network.

[:octicons-home-16: Homepage](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

</details>

</div>

We previously recommended enabling the *Isolate Destination Address* preference in Orbot settings. While this setting can theoretically improve privacy by enforcing the use of a different circuit for each IP address you connect to, it doesn't provide a practical advantage for most applications (especially web browsing), can come with a significant performance penalty, and increases the load on the Tor network. We no longer recommend adjusting this setting from its default value unless you know you need to.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Tips for Android</p>

Orbot can proxy individual apps if they support SOCKS or HTTP proxying. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN kill switch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

Orbot is often outdated on the Guardian Project's [F-Droid repository](https://guardianproject.info/fdroid) and [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android), so consider downloading directly from the [GitHub repository](https://github.com/guardianproject/orbot/releases) instead.

All versions are signed using the same signature, so they should be compatible with each other.

</div>

On iOS, Orbot has some limitations that could potentially cause crashes or leaks: iOS does not have an effective OS-level feature to block connections without a VPN like Android does, and iOS has an artificial memory limit for network extensions that makes it challenging to run Tor in Orbot without crashes. Currently, it is always safer to use Tor on a desktop computer compared to a mobile device.

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** is an open-source browser that lets you browse the web anonymously over the Tor network on iOS devices and is endorsed by the [Tor Project](https://support.torproject.org/glossary/onion-browser). [:material-star-box: Read our latest Onion Browser review.](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review/)

[:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser does not provide the same levels of privacy protections as Tor Browser does on desktop platforms. For casual use it is a perfectly fine way to access hidden services, but if you're concerned about being traced or monitored by advanced adversaries you should not rely on this as an anonymity tool.

[Notably](https://github.com/privacyguides/privacyguides.org/issues/2929), Onion Browser does not *guarantee* all requests go through Tor. When using the built-in version of Tor, [your real IP **will** be leaked via WebRTC and audio/video streams](https://onionbrowser.com/faqs) due to limitations of WebKit. It is *safer* to use Onion Browser alongside Orbot, but this still comes with some limitations on iOS (noted in the Orbot section above).

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) and [Whonix's Stream Isolation documentation](https://whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
