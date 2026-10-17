---
meta_title: "토르 브라우저 및 네트워크: 익명 웹 탐색 - 프라이버시 가이드"
title: "토르 브라우저"
icon: simple/torbrowser
description: 검열 우회 보안 네트워크인 토르 네트워크를 사용해 여러분의 인터넷 탐색이 감시당하지 않도록 보호하세요.
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

<small>다음 위협으로부터 보호합니다:</small>

- [:material-account-cash: 감시 자본주의(Surveillance Capitalism)](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: 대중 감시(Mass Surveillance)](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: 검열(Censorship)](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

**토르**는 자원봉사자들이 운영하는 서버들의 집합으로, 누구나 무료로 접속하여 인터넷상의 프라이버시와 보안을 향상할 수 있습니다. 개인 및 단체는 'Onion hidden 서비스'를 통해, 프라이버시를 침해받는 일 없이 토르 네트워크에서 정보를 공유할 수 있습니다. 토르 트래픽은 차단 및 추적이 어렵기 때문에 검열 우회에 효과적입니다.

[토르 상세 개요 :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: 영상: 토르가 필요한 이유](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">팁</p>

토르에 연결하기 전에 [개요](advanced/tor-overview.md)에서 토르가 무엇인지, 그리고 어떻게 안전하게 연결하는지 읽어보시기 바랍니다. 신뢰할 수 있는 [VPN 제공자](vpn.md)들을 통해 토르에 접속하는 것을 권장하기도 하지만, 제대로 설정하지 않으면 익명성을 유지하기 어려울 수 있습니다.

</div>

기기에서 토르 네트워크에 연결하는 방법은 다양하지만, 가장 널리 쓰이는 것은 **토르 브라우저**입니다. 토르 브라우저는 데스크톱 컴퓨터와 안드로이드에서 [:material-incognito: 익명](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} 탐색을 할 수 있도록 설계된 파이어폭스 포크입니다.

이러한 앱 중에는 다른 앱보다 나은 것도 있으며, 어떤 것을 선택할지는 여러분의 위협 모델에 따라 달라집니다. ISP가 여러분에 대한 증거를 수집하는 것을 걱정하지 않는 일반 토르 사용자라면, [어니언 브라우저](#onion-browser-ios) 같은 모바일 브라우저 앱으로 토르 네트워크에 접속해도 대체로 괜찮습니다. 토르를 일상에서 사용하는 사용자가 증가한다면 토르에 대한 부정적인 이미지를 해소할 수 있고, 정부 또는 ISP가 토르 사용자 명단을 수집하는 행위의 가치를 줄일 수 있습니다.

보다 완전한 익명성이 무엇보다 중요한 상황이라면 데스크톱용 토르 브라우저 클라이언트**만** 사용해야 하며, 가급적 [후닉스](desktop.md#whonix) + [큐브스](desktop.md#qubes-os) 구성에서 사용하는 것이 이상적입니다. 토르에서 모바일 브라우저는 사용자가 상대적으로 적고 (그 결과 핑거프린팅에 더 취약하며), 그 밖의 구성은 탈익명화에 대해 그만큼 엄격하게 검증되지 않았습니다.

## 토르 브라우저

<div class="admonition recommendation" markdown>

![토르 브라우저 로고](assets/img/browsers/tor.svg){ align=right }

**토르 브라우저**는 익명성이 필요할 때 가장 좋은 선택입니다. 토르 네트워크와 브리지에 접속할 수 있게 해 주며, 기본 보안 수준인 *표준(Standard)*, *더 안전(Safer)*, *가장 안전(Safest)*에 따라 자동으로 구성되는 기본 설정과 확장 프로그램이 포함되어 있습니다.

[:octicons-home-16: 홈페이지](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="어니언 서비스" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title="문서" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title="기여하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: 안드로이드](https://torproject.org/download/#android)
- [:fontawesome-brands-windows: 윈도우](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: 리눅스](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">위험</p>

토르 브라우저에서는 **절대로** 추가 확장 프로그램을 설치하거나, (Firefox 관련 내용에서 권장드린 설정을 포함해) `about:config` 설정을 수정해서는 안 됩니다. 브라우저 확장 프로그램 및 별도 설정을 사용할 경우, 토르 네트워크상의 다른 사용자들 사이에서 여러분은 차별화됩니다. 이는 여러분의 브라우저가 [핑거프린팅](https://support.torproject.org/glossary/browser-fingerprinting)하기 쉬워짐을 의미합니다.

</div>

토르 브라우저는 핑거프린팅 및 브라우저 설정 기반 사용자 식별을 방지하도록 설계되었습니다. 따라서 기본 [보안 수준](https://tb-manual.torproject.org/security-settings) 외에는 브라우저를 수정해서는 **안 됩니다**. 보안 수준 설정을 변경했다면, 브라우저를 계속 사용하기 전에 **반드시** 재시작해야 합니다. 그렇지 않으면 [보안 설정이 완전히 적용되지 않을 수 있으며](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), 이로 인해 선택한 설정에 근거해 예상했던 것보다 지문 정보 노출 및 악용에 대한 위험이 더 커질 수 있습니다.

토르 브라우저를 컴퓨터에 설치해서 연결하는 방법도 있지만, [Qubes OS](desktop.md#qubes-os)의 [Whonix](desktop.md#whonix)처럼 토르 네트워크에 연결하기 위한 용도로 만들어진 운영 체제도 있습니다. 이러한 연결 방식은 토르 브라우저를 사용하는 것보다 더 강력한 보안을 제공합니다.

## 어니언 브라우저 (iOS)

<div class="admonition recommendation" markdown>

![어니언 브라우저 로고](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**어니언 브라우저**는 iOS 기기에서 토르 네트워크를 통해 익명으로 웹을 탐색할 수 있게 해 주는 오픈 소스 브라우저로, [토르 프로젝트](https://support.torproject.org/glossary/onion-browser)에서 권장하는 브라우저입니다.

[:material-star-box: 어니언 브라우저에 대한 최신 리뷰를 읽어보세요.](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review)

[:octicons-home-16: 홈페이지](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title="기여하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id519296448)

</details>

</div>

어니언 브라우저는 데스크톱 플랫폼의 토르 브라우저만큼의 프라이버시 보호 수준을 제공하지 않습니다. 가볍게 사용하는 용도라면 히든 서비스에 접속하는 데 전혀 문제가 없지만, 고도의 능력을 갖춘 공격자에게 추적되거나 감시당하는 것이 걱정된다면 이를 익명성 도구로 의존해서는 안 됩니다.

[특히](https://github.com/privacyguides/privacyguides.org/issues/2929) 어니언 브라우저는 모든 요청이 토르를 거친다는 것을 *보장*하지 않습니다. 내장 버전의 토르를 사용하는 경우, 웹킷의 한계로 인해 [WebRTC 및 오디오/비디오 스트림을 통해 실제 IP가 **유출됩니다**](https://onionbrowser.com/faqs). 어니언 브라우저를 [오봇](alternative-networks.md#orbot)과 함께 사용하는 것이 *더 안전*하지만, iOS에서는 여전히 몇 가지 제약이 따릅니다.
