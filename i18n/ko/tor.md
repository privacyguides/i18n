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

![Tor 로고](assets/img/self-contained-networks/tor.svg){ align=right }

**Tor** 네트워크는 자원 봉사 형태로 운영되는 서버 그룹으로, 무료로 연결하여 인터넷에서 프라이버시와 보안을 향상시킬 수 있습니다. 개인 및 단체는 'Onion hidden 서비스'를 통해, 프라이버시를 침해받는 일 없이 Tor 네트워크에서 정보를 공유할 수 있습니다. Tor 트래픽은 차단 및 추적이 어렵기 때문에 검열 우회에 효과적입니다.

[:octicons-home-16:](https://www.torproject.org){ .card-link title=홈페이지 }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion 서비스" }
[:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=문서}
[:octicons-code-16:](https://gitweb.torproject.org/tor.git){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=기부 }

Tor는 방문하려는 사이트에 직접 연결하는 방식이 아닌, 자원 봉사자가 운영하는 서버를 통해 인터넷 트래픽을 전송합니다. 이러한 방식을 통해 트래픽의 출처를 알 수 없게 만들고, 연결 경로상의 서버 또한 트래픽의 전체 경로는 볼 수 없으므로, 연결에 사용한 서버조차도 여러분의 익명성을 깨트릴 수 없습니다.

[자세한 Tor 개요 :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Tor 연결하기

기기에서 Tor 네트워크에 연결하는 방법은 다양합니다. 가장 일반적으로 사용하는 방법은 데스크톱 PC와 Android 용으로 만들어진 **Tor 브라우저**(익명 브라우징을 위해 설계된 Firefox 포크)입니다. 여기에 나열된 앱 외에도, 표준 Tor 브라우저보다 훨씬 더 강력한 보안 및 보호 기능을 제공하는 [Whonix](desktop.md#whonix) + [Qubes OS](desktop.md#qubes-os) 처럼 Tor 네트워크에 연결하도록 특별히 설계된 운영 체제도 존재합니다.

### Tor 브라우저

!!! recommendation

    ![Tor Browser 로고](assets/img/browsers/tor.svg){ align=right }
    
    **Tor 브라우저**는 익명성이 필요한 경우 선택해야 할 브라우저입니다. 이 브라우저는 Tor 네트워크와 브릿지에 접근할 수 있도록 해주며, 기본 보안 수준인 Standard, Safer, Safest에 따라 자동으로 구성되는 기본 설정과 확장 기능을 탑재하고 있습니다.
    
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

!!! danger "위험"

    Tor 브라우저에서는 **절대로** 추가 확장 프로그램을 설치하거나, (Firefox 관련 내용에서 권장드린 설정을 포함해) `about:config` 설정을 수정해서는 안 됩니다. 브라우저 확장 프로그램 및 별도 설정을 사용할 경우, Tor 네트워크상의 다른 사용자들 사이에서 여러분은 차별화됩니다. 이는 여러분의 브라우저가 [핑거프린팅](https://support.torproject.org/glossary/browser-fingerprinting)하기 쉬워짐을 의미합니다.

Tor 브라우저는 핑거프린팅 및 브라우저 설정 기반 사용자 식별을 방지하도록 설계되었습니다. 따라서, 브라우저를 기본 [보안 수준](https://tb-manual.torproject.org/security-settings/)을 벗어나는 수정을 해서는 **안 됩니다**.

### Orbot

!!! recommendation

    ![Orbot logo](assets/img/self-contained-networks/orbot.svg){ align=right }
    
    **Orbot**는 기기의 어떤 앱이든 해당 앱의 트래픽을 Tor 네트워크를 통해 라우팅하는 스마트폰용 무료 Tor VPN입니다.
    
    [:octicons-home-16: 홈페이지](https://orbot.app/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://orbot.app/faqs){ .card-link title=문서}
    [:octicons-code-16:](https://orbot.app/code){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://orbot.app/donate){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/orbot/id1609461599)
        - [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

이전에는 Orbot 설정에서 *Isolate Destination Address* 옵션을 활성화하도록 권장했었습니다. 이론적으로, 이 옵션은 연결이 발생하는 모든 IP 주소마다 다른 경로를 사용하도록 하여 프라이버시를 향상시킬 수 있습니다. 하지만 대부분의 애플리케이션(특히 웹 브라우저)에 실질적인 이점을 제공하지 않으며, 상당한 성능 저하를 초래하고 Tor 네트워크의 부하를 증가시킵니다. 반드시 필요한 경우가 아니라면, 이 옵션을 수정하지 않는 것을 더 이상 권장드리지 않습니다.[^1]

!!! tip "Android용 도움말"

    Orbot은 앱이 SOCKS/HTTP 프록시를 지원하는 경우 개별적으로 프록시를 적용하는 것도 가능합니다. 뿐만 아니라 [VpnService](https://developer.android.com/reference/android/net/VpnService)를 이용해 모든 네트워크 연결에 프록시를 적용할 수도 있으며, VPN 킬 스위치와 함께 사용할 수도 있습니다(:gear: **설정** → **네트워크 및 인터넷** → **VPN** → :gear: → **연결 차단(VPN 제외)**).
    
    Guardian Project [F-Droid 저장소](https://guardianproject.info/fdroid), [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)에서의 Orbot은 구버전인 경우가 많으므로, [GitHub 저장소](https://github.com/guardianproject/orbot/releases)에서 직접 다운로드하는 것을 추천드립니다.
    
    모든 버전은 동일한 서명을 사용하여 서명되므로 서로 호환됩니다.

## 릴레이 및 브리지

### Snowflake

!!! recommendation

    ![Snowflake 로고](assets/img/browsers/snowflake.svg#only-light){ align=right }
    ![Snowflake 로고](assets/img/browsers/snowflake-dark.svg#only-dark){ align=right }
    
    **Snowflake**는 여러분의 브라우저 내에서 'Snowflake 프록시'를 작동시켜 Tor 프로젝트에 대역폭을 기부합니다.
    
    검열을 받고 있는 사람들은 Snowflake 프록시를 사용해 Tor 네트워크에 접속할 수 있습니다. Snowflake는 Tor 릴레이나 브리지를 운영할 기술적 노하우가 없더라도 네트워크에 기여할 수 있는 좋은 방법입니다.
    
    [:octicons-home-16: 홈페이지](https://snowflake.torproject.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=문서}
    [:octicons-code-16:](https://gitweb.torproject.org/pluggable-transports/snowflake.git/){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=기부 }

여러분이 사용하는 브라우저의 다른 탭에 Snowflake를 열고, 활성화 스위치를 켜면 Snowflake를 활성화할 수 있습니다. 브라우저를 사용하는 동안 백그라운드에서 실행시켜 두는 것만으로도 대역폭 기여가 가능합니다. Snowflake 브라우저 확장 프로그램도 존재하지만, Privacy Guides는 여러분의 공격 표면이 늘어날 가능성을 최소화하기 위해 브라우저 확장 프로그램 설치는 권장드리지 않습니다.

[브라우저에서 Snowflake 실행 :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html ""){.md-button}

Snowflake는 어떤 방식으로도 여러분의 프라이버시를 침해하지 않으며, 여러분이 사용하는 브라우저를 Tor 네트워크에 연결해 주지도 않습니다. 그러나, 여러분이 인터넷 연결을 검열받고 있지 않은 상황에 계신 경우, 네트워크를 검열받고 있는 사람들이 프라이버시를 강화할 수 있도록 돕는 걸 고려해주시기 바랍니다. 다른 사람들이 여러분의 프록시를 통해 어떤 사이트에 접근할지 걱정하지 않으셔도 됩니다. 사람들의 IP 주소는 Tor 출구 노드로 표시되며, 프록시 주소로 표시되지 않습니다.

Snowflake 프록시 구동의 위험성은 매우 낮습니다. Tor 릴레이/브리지 구동(이 또한 특별히 위험하지 않습니다)보다도 훨씬 위험성이 낮습니다. 물론 여러분의 네트워크를 통해 프록시 트래픽이 전달되기 때문에, 네트워크 대역폭이 제한된 경우 등에는 여러분에게 영향을 끼칠 수 있습니다. 프록시 구동 여부를 결정하기 전에 [Snowflake 작동 방식](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home)을 이해해 두세요.

[^1]: `IsolateDestAddr` 설정은 [Tor 메일링 리스트](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html), [Whonix Stream Isolation 문서](https://www.whonix.org/wiki/Stream_Isolation)에서 논의되었으며, 두 프로젝트 모두 해당 설정은 대부분의 사람들에게 추천하지 않았습니다.
