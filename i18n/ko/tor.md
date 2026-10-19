---
meta_title: "토르 브라우저와 토르 네트워크: 익명 웹 브라우징 - 프라이버시 가이드"
title: "토르 브라우저"
icon: simple/torbrowser
description: 검열을 우회하는 보안 네트워크인 토르 네트워크를 사용해, 여러분의 인터넷 브라우징을 엿보는 눈으로부터 보호하세요.
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

- [:material-account-cash: 감시 자본주의](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: 대규모 감시](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: 검열](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

**토르**는 자원봉사자들이 운영하는 서버들의 집합으로, 누구나 무료로 접속하여 인터넷에서 프라이버시와 보안을 향상할 수 있습니다. 개인과 단체는 ".onion 히든 서비스"를 이용해 프라이버시를 침해받지 않고 토르 네트워크에서 정보를 공유할 수도 있습니다. 토르 트래픽은 차단하거나 추적하기 어렵기 때문에, 토르는 효과적인 검열 우회 도구입니다.

[토르 상세 개요 :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: 영상: 토르가 필요한 이유](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">팁</p>

토르에 연결하기 전에, 토르가 무엇이며 어떻게 안전하게 연결하는지 설명한 [개요](advanced/tor-overview.md)를 꼭 읽어 보세요. 신뢰할 수 있는 [VPN 제공업체](vpn.md)를 통해 토르에 연결하는 것을 권장하는 경우가 많지만, 익명성이 떨어지지 않도록 하려면 **올바르게** 설정해야 합니다.

</div>

기기에서 토르 네트워크에 연결하는 방법은 다양하며, 가장 널리 쓰이는 것은 **토르 브라우저**입니다. 토르 브라우저는 데스크톱 컴퓨터와 안드로이드에서 [:material-incognito: 익명](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} 브라우징을 할 수 있도록 설계된 파이어폭스 포크입니다.

이러한 앱 중에는 더 나은 것도 있고 그렇지 않은 것도 있으며, 무엇을 선택할지는 여러분의 위협 모델에 달려 있습니다. ISP가 여러분에 대한 증거를 수집하는 것을 걱정하지 않는 일반적인 토르 사용자라면, [어니언 브라우저](#onion-browser-ios) 같은 모바일 브라우저 앱으로 토르 네트워크에 접속해도 대체로 괜찮습니다. 토르를 일상적으로 사용하는 사람이 늘어나면 토르에 대한 부정적인 낙인을 줄이는 데 도움이 되고, ISP나 정부가 작성할 수 있는 "토르 사용자 목록"의 신뢰도도 떨어뜨릴 수 있습니다.

보다 완전한 익명성이 무엇보다 중요한 상황이라면 데스크톱용 토르 브라우저 클라이언트**만** 사용해야 하며, 가급적 [후닉스](desktop.md#whonix) + [큐브스](desktop.md#qubes-os) 구성에서 사용하는 것이 이상적입니다. 토르에서 모바일 브라우저는 상대적으로 사용자가 적고 (그 결과 핑거프린팅에 더 취약하며), 그 밖의 구성은 탈익명화에 대해 그만큼 엄격하게 검증되지 않았습니다.

## 토르 브라우저

<div class="admonition recommendation" markdown>

![토르 브라우저 로고](assets/img/browsers/tor.svg){ align=right }

**토르 브라우저**는 익명성이 필요할 때 가장 좋은 선택입니다. 토르 네트워크와 브리지에 접속할 수 있게 해 주며, 기본 보안 수준인 *표준*, *더 안전*, *가장 안전*에 따라 자동으로 구성되는 기본 설정과 확장 프로그램이 포함되어 있습니다.

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

토르 브라우저에는 추가 확장 프로그램을 **절대** 설치하거나 `about:config` 설정을 수정해서는 안 됩니다. 저희가 파이어폭스에 권장하는 확장 프로그램과 설정도 마찬가지입니다. 브라우저 확장 프로그램과 비표준 설정은 토르 네트워크에서 여러분을 다른 사용자들과 구별되게 만들어, 여러분의 브라우저를 [핑거프린팅](https://support.torproject.org/glossary/browser-fingerprinting)하기 쉽게 만듭니다.

</div>

토르 브라우저는 핑거프린팅, 즉 브라우저 구성을 바탕으로 여러분을 식별하는 것을 방지하도록 설계되었습니다. 따라서 기본 [보안 수준](https://tb-manual.torproject.org/security-settings)을 조정하는 것 외에는 브라우저를 수정해서는 **안 됩니다**. 보안 수준 설정을 변경했다면, 브라우저를 계속 사용하기 전에 **반드시** 재시작해야 합니다. 그렇지 않으면 [보안 설정이 완전히 적용되지 않을 수 있으며](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), 그 결과 선택한 설정을 보고 예상한 것보다 핑거프린팅과 익스플로잇에 더 큰 위험에 노출될 수 있습니다.

토르 브라우저를 컴퓨터에 직접 설치하는 방법 외에도, [큐브스 OS](desktop.md#qubes-os) 위에서 실행하는 [후닉스](desktop.md#whonix)처럼 토르 네트워크 연결을 위해 특별히 설계된 운영 체제도 있습니다. 이러한 운영 체제는 일반 토르 브라우저만 사용할 때보다 훨씬 더 강력한 보안과 보호를 제공합니다.

## 어니언 브라우저 (iOS)

<div class="admonition recommendation" markdown>

![어니언 브라우저 로고](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**어니언 브라우저**는 iOS 기기에서 토르 네트워크를 통해 익명으로 웹을 탐색할 수 있게 해 주는 오픈 소스 브라우저로, [토르 프로젝트](https://support.torproject.org/glossary/onion-browser)가 공식적으로 지지하는 브라우저입니다.

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

어니언 브라우저는 데스크톱 플랫폼의 토르 브라우저만큼의 프라이버시 보호 수준을 제공하지 않습니다. 가볍게 사용하는 용도라면 히든 서비스에 접속하는 데 전혀 문제가 없지만, 고도화된 공격자에게 추적되거나 감시당하는 것이 걱정된다면 이를 익명성 도구로 의존해서는 안 됩니다.

[특히](https://github.com/privacyguides/privacyguides.org/issues/2929) 어니언 브라우저는 모든 요청이 토르를 거친다는 것을 *보장*하지 않습니다. 내장된 토르를 사용하는 경우, 웹킷의 한계로 인해 [WebRTC 및 오디오/비디오 스트림을 통해 실제 IP가 **유출됩니다**](https://onionbrowser.com/faqs). 어니언 브라우저를 [오봇](alternative-networks.md#orbot)과 함께 사용하는 것이 *더 안전*하지만, iOS에서는 여전히 몇 가지 제약이 따릅니다.
