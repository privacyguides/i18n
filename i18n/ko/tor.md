---
meta_title: "Tor 브라우저 및 네트워크: 익명 웹 탐색 - Privacy Guides"
title: "Tor 네트워크"
icon: simple/torproject
description: 검열 우회 보안 네트워크인 Tor 네트워크를 사용해 여러분의 인터넷 탐색이 감시당하지 않도록 보호하세요.
cover: tor.png
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor 브라우저
    image: /assets/img/browsers/tor.svg
    url: https://www.torproject.org
    sameAs: https://ko.wikipedia.org/wiki/%ED%86%A0%EB%A5%B4_(%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC)
    applicationCategory: 웹 브라우저
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

**Tor** 네트워크는 자원 봉사 형태로 운영되는 서버 그룹으로, 무료로 연결하여 인터넷에서 프라이버시와 보안을 향상시킬 수 있습니다. 개인 및 단체는 'Onion hidden 서비스'를 통해, 프라이버시를 침해받는 일 없이 Tor 네트워크에서 정보를 공유할 수 있습니다. Tor 트래픽은 차단 및 추적이 어렵기 때문에 검열 우회에 효과적입니다.

[:octicons-home-16:](https://www.torproject.org){ .card-link title=홈페이지 }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion 서비스" }
[:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=문서}
[:octicons-code-16:](https://gitweb.torproject.org/tor.git){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=기부 }

Tor는 방문하려는 사이트에 직접 연결하는 방식이 아닌, 자원 봉사자가 운영하는 서버를 통해 인터넷 트래픽을 전송합니다. 이러한 방식을 통해 트래픽의 출처를 알 수 없게 만들고, 연결 경로상의 서버 또한 트래픽의 전체 경로는 볼 수 없으므로, 연결에 사용한 서버조차도 여러분의 익명성을 깨트릴 수 없습니다.

[자세한 Tor 개요 :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Tor 연결하기

기기에서 Tor 네트워크에 연결하는 방법은 다양합니다. 가장 일반적으로 사용하는 방법은 데스크톱 PC와 Android 용으로 만들어진 **Tor 브라우저**(익명 브라우징을 위해 설계된 Firefox 포크)입니다. In addition to the apps listed below, there are also operating systems designed specifically to connect to the Tor network such as [Whonix](desktop.md#whonix) on [Qubes OS](desktop.md#qubes-os), which provide even greater security and protections than the standard Tor Browser.

### Tor 브라우저

!!! recommendation

    ![Tor Browser logo](assets/img/browsers/tor.svg){ align=right }
    
    **Tor Browser** is the choice if you need anonymity, as it provides you with access to the Tor network and bridges, and it includes default settings and extensions that are automatically configured by the default security levels: *Standard*, *Safer* and *Safest*.
    
    [:octicons-home-16: 홈페이지](https://www.torproject.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion 서비스" }
    [:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=문서 }
    [:octicons-code-16:](https://gitweb.torproject.org/tor-browser.git/){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
        - [:simple-android: Android](https://www.torproject.org/download/#android)
        - [:simple-windows11: Windows](https://www.torproject.org/download/)
        - [:simple-apple: macOS](https://www.torproject.org/download/)
        - [:simple-linux: Linux](https://www.torproject.org/download/)
        - [:simple-freebsd: FreeBSD](https://www.freshports.org/security/tor)

!!! danger "위험"

    Tor 브라우저에서는 **절대로** 추가 확장 프로그램을 설치하거나, (Firefox 관련 내용에서 권장드린 설정을 포함해) `about:config` 설정을 수정해서는 안 됩니다. 브라우저 확장 프로그램 및 별도 설정을 사용할 경우, Tor 네트워크상의 다른 사용자들 사이에서 여러분은 차별화됩니다. 이는 여러분의 브라우저가 [핑거프린팅](https://support.torproject.org/glossary/browser-fingerprinting)하기 쉬워짐을 의미합니다.

Tor 브라우저는 핑거프린팅 및 브라우저 설정 기반 사용자 식별을 방지하도록 설계되었습니다. Therefore, it is imperative that you do **not** modify the browser beyond the default [security levels](https://tb-manual.torproject.org/security-settings/).

### Orbot

!!! recommendation

    ![Orbot logo](assets/img/self-contained-networks/orbot.svg){ align=right }
    
    **Orbot** is a free Tor VPN for smartphones which routes traffic from any app on your device through the Tor network.
    
    [:octicons-home-16: 홈페이지](https://orbot.app/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://orbot.app/faqs){ .card-link title=문서}
    [:octicons-code-16:](https://orbot.app/code){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://orbot.app/donate){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/orbot/id1609461599)
        - [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

We previously recommended enabling the *Isolate Destination Address* preference in Orbot settings. While this setting can theoretically improve privacy by enforcing the use of a different circuit for each IP address you connect to, it doesn't provide a practical advantage for most applications (especially web browsing), can come with a significant performance penalty, and increases the load on the Tor network. We no longer recommend adjusting this setting from its default value unless you know you need to.[^1]

!!! tip "Tips for Android"

    Orbot can proxy individual apps if they support SOCKS or HTTP proxying. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN killswitch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.
    
    Orbot is often outdated on the Guardian Project's [F-Droid repository](https://guardianproject.info/fdroid) and [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android), so consider downloading directly from the [GitHub repository](https://github.com/guardianproject/orbot/releases) instead.
    
    All versions are signed using the same signature so they should be compatible with each other.

## Relays and Bridges

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
    
    ??? downloads
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/en-US/firefox/addon/torproject-snowflake/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/snowflake/mafpmfcccpbjnhfhjnllmmalhifmlcie)
        - [:octicons-browser-16: Web](https://snowflake.torproject.org/embed "Leave this page open to be a Snowflake proxy")

??? tip "Embedded Snowflake"

    You can enable Snowflake in your browser by clicking the switch below and ==leaving this page open==. You can also install Snowflake as a browser extension to have it always run while your browser is open, however adding third-party extensions can increase your attack surface.
    
    <center><iframe src="https://snowflake.torproject.org/embed.html" width="320" height="240" frameborder="0" scrolling="no"></iframe></center>
    <small>If the embed does not appear for you, ensure you are not blocking the third-party frame from `torproject.org`. Alternatively, visit [this page](https://snowflake.torproject.org/embed.html).</small>

Snowflake does not increase your privacy in any way, nor is it used to connect to the Tor network within your personal browser. However, if your internet connection is uncensored, you should consider running it to help people in censored networks achieve better privacy themselves. There is no need to worry about which websites people are accessing through your proxy—their visible browsing IP address will match their Tor exit node, not yours.

Running a Snowflake proxy is low-risk, even moreso than running a Tor relay or bridge which are already not particularly risky endeavours. However, it does still proxy traffic through your network which can be impactful in some ways, especially if your network is bandwidth-limited. Make sure you understand [how Snowflake works](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) before deciding whether to run a proxy.

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) and [Whonix's Stream Isolation documentation](https://www.whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
