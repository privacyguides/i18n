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

Torネットワークに接続するアプリには長短があり、どれを使うかは脅威モデルによります。 If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using mobile browser apps like [Onion Browser](#onion-browser-ios) to access the Tor network is probably fine. 日常的にTorを使う人が増えることはTorのマイナスイメージをやわらげ、ISPや政府が作成しているかもしれない「Torユーザーリスト」の質を下げることになります。

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

Tor Browserを直接コンピューターにインストールするだけではなく、[Qubes OS](desktop.md#qubes-os)上の[Whonix](desktop.md#whonix)のようにTorネットワークに接続するためのOSもあり、Tor Browser単体で使うよりもよりセキュリティを強化することができます。

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser**はiOS上でTorネットワークを経由し匿名でウェブブラウジングすることができるオープンソースのブラウザで、[Tor Project](https://support.torproject.org/glossary/onion-browser)が支持しています。 [:material-star-box: Onion Browserの最新レビュー](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review/)

[:octicons-home-16: ウェブページ](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="プライバシーポリシー" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=ドキュメント}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="ソースコード" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=貢献 }

<details class="downloads" markdown>
<summary>ダウンロード</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browserはデスクトップ版のTor Browserと同じレベルでプライバシーを保護することはできません。 Onion Serviceへアクセスするカジュアルな利用には適していますが、高度な追跡や監視を警戒する場合、匿名化ツールとして利用するべきではありません。

[特に](https://github.com/privacyguides/privacyguides.org/issues/2929)、Onion Browserはすべての接続がTorを経由することを*保証*していません。 ビルトインのTorを使う場合、Webkitの制約のために[実際のIPアドレスがWebRTCやオーディオ・ビデオストリーム経由でリークする**可能性があります**](https://onionbrowser.com/faqs)。 It is *safer* to use Onion Browser alongside [Orbot](alternative-networks.md#orbot), but this still comes with some limitations on iOS.
