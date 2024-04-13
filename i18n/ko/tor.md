---
meta_title: "Tor 브라우저 및 네트워크: 익명 웹 탐색 - Privacy Guides"
title: "Tor 브라우저"
icon: simple/torbrowser
description: 검열 우회 보안 네트워크인 Tor 네트워크를 사용해 여러분의 인터넷 탐색이 감시당하지 않도록 보호하세요.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor 브라우저
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
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

**Tor** is a group of volunteer-operated servers that allows you to connect for free and improve your privacy and security on the Internet. 개인 및 단체는 'Onion hidden 서비스'를 통해, 프라이버시를 침해받는 일 없이 Tor 네트워크에서 정보를 공유할 수 있습니다. Tor 트래픽은 차단 및 추적이 어렵기 때문에 검열 우회에 효과적입니다.

[자세한 Tor 개요 :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Tor에 연결하기 전에 [개요](advanced/tor-overview.md)에서 Tor가 무엇인지, 그리고 어떻게 안전하게 연결하는지 읽어보시기 바랍니다. 신뢰할 수 있는 [VPN 제공자](vpn.md)들을 통해 Tor에 접속하는 것을 권장하기도 하지만, 제대로 설정하지 않으면 익명성을 유지하기 어려울 수 있습니다.

</div>

기기에서 Tor 네트워크에 연결하는 방법은 다양합니다. 가장 일반적으로 사용하는 방법은 데스크톱 PC와 Android 용으로 만들어진 **Tor 브라우저**(익명 브라우징을 위해 설계된 Firefox 포크)입니다.

Some of these apps are better than others, and again making a determination comes down to your threat model. If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using apps like [Orbot](#orbot) or mobile browser apps to access the Tor network is probably fine. Tor를 일상에서 사용하는 사용자가 증가한다면 Tor에 대한 부정적인 이미지를 해소할 수 있고, 정부 또는 ISP가 Tor 사용자 명단을 수집하는 행위의 가치를 줄일 수 있습니다.

If more complete anonymity is paramount to your situation, you should **only** be using the desktop Tor Browser client, ideally in a [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os) configuration. Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

## Tor 브라우저

<div class="admonition recommendation" markdown>

![Tor Browser 로고](assets/img/browsers/tor.svg){ align=right }

**Tor 브라우저**는 익명성이 필요한 경우 선택해야 할 브라우저입니다. 이 브라우저는 Tor 네트워크와 브릿지에 접근할 수 있도록 해주며, 기본 보안 수준인 Standard, Safer, Safest에 따라 자동으로 구성되는 기본 설정과 확장 기능을 탑재하고 있습니다.

[:octicons-home-16: Homepage](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:simple-windows11: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Tor 브라우저에서는 **절대로** 추가 확장 프로그램을 설치하거나, (Firefox 관련 내용에서 권장드린 설정을 포함해) `about:config` 설정을 수정해서는 안 됩니다. 브라우저 확장 프로그램 및 별도 설정을 사용할 경우, Tor 네트워크상의 다른 사용자들 사이에서 여러분은 차별화됩니다. 이는 여러분의 브라우저가 [핑거프린팅](https://support.torproject.org/glossary/browser-fingerprinting)하기 쉬워짐을 의미합니다.

</div>

Tor 브라우저는 핑거프린팅 및 브라우저 설정 기반 사용자 식별을 방지하도록 설계되었습니다. Therefore, it is imperative that you do **not** modify the browser beyond the default [security levels](https://tb-manual.torproject.org/security-settings).

Tor Browser를 컴퓨터에 설치해서 연결하는 방법도 있지만, [Qubes OS](desktop.md#qubes-os)의 [Whonix](desktop.md#whonix)처럼 Tor 네트워크에 연결하기 위한 용도로 만들어진 운영 체제도 있습니다. 이러한 연결 방식은 Tor Browser를 사용하는 것보다 더 강력한 보안을 제공합니다.

## Orbot

<div class="admonition recommendation" markdown>

![Orbot logo](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot**는 기기의 어떤 앱이든 해당 앱의 트래픽을 Tor 네트워크를 통해 라우팅하는 스마트폰용 무료 Tor VPN입니다.

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

이전에는 Orbot 설정에서 *Isolate Destination Address* 옵션을 활성화하도록 권장했었습니다. 이론적으로, 이 옵션은 연결이 발생하는 모든 IP 주소마다 다른 경로를 사용하도록 하여 프라이버시를 향상시킬 수 있습니다. 하지만 대부분의 애플리케이션(특히 웹 브라우저)에 실질적인 이점을 제공하지 않으며, 상당한 성능 저하를 초래하고 Tor 네트워크의 부하를 증가시킵니다. We no longer recommend adjusting this setting from its default value unless you know you need to.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Tips for Android</p>

Orbot은 앱이 SOCKS/HTTP 프록시를 지원하는 경우 개별적으로 프록시를 적용하는 것도 가능합니다. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN killswitch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

Guardian Project [F-Droid 저장소](https://guardianproject.info/fdroid), [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)에서의 Orbot은 구버전인 경우가 많으므로, [GitHub 저장소](https://github.com/guardianproject/orbot/releases)에서 직접 다운로드하는 것을 추천드립니다.

모든 버전은 동일한 서명을 사용하여 서명되므로 서로 호환됩니다.

</div>

## Onion Browser

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** is an open-source browser that lets you browse the web anonymously over the Tor network on iOS devices and is endorsed by the [Tor Project](https://support.torproject.org/glossary/onion-browser).

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

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) and [Whonix's Stream Isolation documentation](https://whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
