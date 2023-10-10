---
meta_title: "Tor Browserとネットワーク: 匿名のウェブブラウジング - Privacy Guides"
title: "Torネットワーク"
icon: simple/torproject
description: Protect your internet browsing from prying eyes by using the Tor network, a secure network which circumvents censorship.
cover: tor.png
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
    image: /assets/img/browsers/tor.svg
    url: https://www.torproject.org
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

![Tor logo](assets/img/self-contained-networks/tor.svg){ align=right }

**Tor**ネットワークは、ボランティアが運営するサーバ群で、無料で接続でき、インターネット上でのプライバシーとセキュリティの確保に役立ちます。 個人や組織は、プライバシーを損なうことなく、Torネットワーク上で「.onion 秘匿サービス」による情報共有が可能です。 Torトラフィックはブロックや追跡が困難であるため、Torは効果的な検閲回避ツールです。

[:octicons-home-16:](https://www.torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Documentation}
[:octicons-code-16:](https://gitweb.torproject.org/tor.git){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }

Tor works by routing your internet traffic through those volunteer-operated servers, instead of making a direct connection to the site you're trying to visit. This obfuscates where the traffic is coming from, and no server in the connection path is able to see the full path of where the traffic is coming from and going to, meaning even the servers you are using to connect cannot break your anonymity.

[Detailed Tor Overview :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Torへの接続

デバイスからTorネットワークに接続する様々な方法がありますが、 デスクトップコンピューターやAndroid用の匿名ブラウジング用に設計された、Firefoxのフォークの**Tor Browser**が最も一般的に使用されています。 In addition to the apps listed below, there are also operating systems designed specifically to connect to the Tor network such as [Whonix](desktop.md#whonix) on [Qubes OS](desktop.md#qubes-os), which provide even greater security and protections than the standard Tor Browser.

### Tor Browser

!!! recommendation

    ![Tor Browser logo](assets/img/browsers/tor.svg){ align=right }
    
    **Tor Browser** is the choice if you need anonymity, as it provides you with access to the Tor network and bridges, and it includes default settings and extensions that are automatically configured by the default security levels: *Standard*, *Safer* and *Safest*.
    
    [:octicons-home-16: Homepage](https://www.torproject.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
    [:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Documentation }
    [:octicons-code-16:](https://gitweb.torproject.org/tor-browser.git/){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
        - [:simple-android: Android](https://www.torproject.org/download/#android)
        - [:simple-windows11: Windows](https://www.torproject.org/download/)
        - [:simple-apple: macOS](https://www.torproject.org/download/)
        - [:simple-linux: Linux](https://www.torproject.org/download/)

!!! 警告

    Firefoxでおすすめされているものを含め、Tor Browserに追加の拡張機能をインストールしたり、「about:config」の設定を変更したりは、**絶対に**しないでください。 ブラウザ拡張機能や非標準の設定により、Torネットワーク上の他のユーザとあなたが区別されやすくなり、[フィンガープリント](https://support.torproject.org/glossary/browser-fingerprinting)されやすくなります。

Tor Browserはフィンガープリントを防止するよう設計されており、不用意にブラウザの設定を変更するとあなたは特定されやすくなってしまいます。 したがって、デフォルトの[セキュリティーレベル](https://tb-manual.torproject.org/security-settings/)を調整する以外の変更は、**決して**行うべきではありません。

### Orbot

!!! recommendation

    ![Orbot logo](assets/img/self-contained-networks/orbot.svg){ align=right }
    
    **Orbot** is a free Tor VPN for smartphones which routes traffic from any app on your device through the Tor network.
    
    [:octicons-home-16: Homepage](https://orbot.app/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
    [:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribute }
    
    ??? ダウンロード
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/orbot/id1609461599)
        - [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

We previously recommended enabling the *Isolate Destination Address* preference in Orbot settings. While this setting can theoretically improve privacy by enforcing the use of a different circuit for each IP address you connect to, it doesn't provide a practical advantage for most applications (especially web browsing), can come with a significant performance penalty, and increases the load on the Tor network. We no longer recommend adjusting this setting from its default value unless you know you need to.[^1]

!!! tip "Tips for Android"

    Orbot can proxy individual apps if they support SOCKS or HTTP proxying. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN killswitch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.
    
    Orbot is often outdated on the Guardian Project's [F-Droid repository](https://guardianproject.info/fdroid) and [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android), so consider downloading directly from the [GitHub repository](https://github.com/guardianproject/orbot/releases) instead.
    
    All versions are signed using the same signature so they should be compatible with each other.

### Onion Browser

!!! recommendation

    ![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }
    
    **Onion Browser** is an open-source browser that lets you browse the web anonymously over the Tor network on iOS devices and is endorsed by the [Tor Project](https://support.torproject.org/glossary/onion-browser/).
    
    [:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

## リレーとブリッジ

### Snowflake

!!! recommendation

    ![Snowflake logo](assets/img/browsers/snowflake.svg#only-light){ align=right }
    ![Snowflake logo](assets/img/browsers/snowflake-dark.svg#only-dark){ align=right }
    
    **Snowflake** allows you to donate bandwidth to the Tor Project by operating a "Snowflake proxy" within your browser.
    
    People who are censored can use Snowflake proxies to connect to the Tor network. Snowflake is a great way to contribute to the network even if you don't have the technical know-how to run a Tor relay or bridge.
    
    [:octicons-home-16: Homepage](https://snowflake.torproject.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitweb.torproject.org/pluggable-transports/snowflake.git/){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }

You can enable Snowflake in your browser by opening it in another tab and turning the switch on. You can leave it running in the background while you browse to contribute your connection. We don't recommend installing Snowflake as a browser extension; adding third-party extensions can increase your attack surface.

[ブラウザでSnowflakeを実行 :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html ""){.md-button}

Snowflakeはあなたのプライバシーを高めるものではなく、また、あなたのブラウザーでTorネットワークに接続するために使用されるものでもありません。 However, if your internet connection is uncensored, you should consider running it to help people in censored networks achieve better privacy themselves. There is no need to worry about which websites people are accessing through your proxy—their visible browsing IP address will match their Tor exit node, not yours.

Running a Snowflake proxy is low-risk, even moreso than running a Tor relay or bridge which are already not particularly risky endeavours. However, it does still proxy traffic through your network which can be impactful in some ways, especially if your network is bandwidth-limited. プロキシーを設置するかどうかを決定する前に、 [Snowflakeがどのように動作するか](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home)について理解しておきましょう。

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) and [Whonix's Stream Isolation documentation](https://www.whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
