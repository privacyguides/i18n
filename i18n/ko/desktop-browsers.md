---
meta_title: "프라이버시 중점 PC, Mac용 웹 브라우저 - Privacy Guides"
title: 데스크톱 브라우저
icon: material/laptop
description: 현재 데스크톱 시스템에서 일반적인(비익명) 인터넷 브라우징용으로 추천하는 프라이버시 보호 브라우저입니다.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: 프라이버시를 보호하는 데스크톱 브라우저 추천
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/en/browser
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - '리눅스 { #linux }'
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Firefox
    image: /assets/img/browsers/firefox.svg
    url: https://firefox.com
    sameAs: https://ko.wikipedia.org/wiki/%EB%AA%A8%EC%A7%88%EB%9D%BC_%ED%8C%8C%EC%9D%B4%EC%96%B4%ED%8F%AD%EC%8A%A4
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - '리눅스 { #linux }'
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    sameAs: https://en.wikipedia.org/wiki/Brave_(web_browser)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - '리눅스 { #linux }'
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-account-cash: 감시 자본주의](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

다음은 일반적인(비익명) 브라우징을 위해 현재 추천하는 **데스크톱 웹 브라우저**와 설정입니다. 강력한 프라이버시 보호와 핑거프린팅 방지 기능을 별도 설정 없이 바로 원한다면 [멀바드 브라우저](#mullvad-browser)를, 구글 크롬의 좋은 대안을 찾는 일반 사용자라면 [파이어폭스](#firefox)를, 크로미움 브라우저 호환성이 필요하다면 [브레이브](#brave)를 추천합니다.

익명으로 인터넷을 이용해야 한다면 대신 [토르 브라우저](tor.md)를 사용해야 합니다. 이 페이지에서 몇 가지 설정을 권장하고 있지만, 온라인 추적에 대해 가장 강력한 보호를 제공하는 것은 토르 브라우저입니다.

## 멀바드 브라우저

<div class="admonition recommendation" markdown>

![멀바드 브라우저 로고](assets/img/browsers/mullvad_browser.svg){ align=right }

**멀바드 브라우저**는 [토르 브라우저](tor.md#tor-browser)에서 토르 네트워크 통합 기능을 제거한 버전입니다. VPN 사용자에게 토르 브라우저의 핑거프린팅 방지 기술을 제공하는 것을 목표로 하며, 이는 [:material-eye-outline: 대규모 감시](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }에 대한 핵심적인 보호 수단입니다. 토르 프로젝트가 개발하고 [멀바드](vpn.md#mullvad)가 배포하며, 멀바드 VPN을 사용하지 **않아도** 됩니다.

[:octicons-home-16: 홈페이지](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="문서" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: 윈도우](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: 리눅스](https://mullvad.net/en/download/browser/linux)

</details>

</div>

[토르 브라우저](tor.md)와 마찬가지로 멀바드 브라우저는 여러분의 브라우저 핑거프린트를 수많은 다른 멀바드 브라우저 사용자와 비슷하게 만들어 핑거프린팅을 방지하도록 설계되었으며, 기본 보안 수준인 *표준*, *더 안전*, *가장 안전*에 따라 자동으로 구성되는 기본 설정과 확장 프로그램이 포함되어 있습니다.

따라서 기본 [보안 수준](https://tb-manual.torproject.org/security-settings)을 조정하는 것 외에는 브라우저를 절대 수정하지 않는 것이 매우 중요합니다. 보안 수준을 조정했다면, 브라우저를 계속 사용하기 전에 **반드시** 재시작해야 합니다. 그렇지 않으면 [보안 설정이 완전히 적용되지 않을 수 있으며](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), 그 결과 선택한 설정을 보고 예상한 것보다 핑거프린팅과 익스플로잇에 더 큰 위험에 노출될 수 있습니다.

이 설정을 조정하는 것 외의 수정은 여러분의 핑거프린트를 고유하게 만들어, 이 브라우저를 사용하는 의미를 없애 버립니다. 브라우저를 더 많이 설정하고 싶고 핑거프린팅이 걱정되지 않는다면, 대신 [파이어폭스](#firefox)를 추천합니다.

### 핑거프린팅 방지

[VPN](vpn.md)을 사용하지 **않더라도**, 멀바드 브라우저는 파이어폭스+[아켄폭스](#arkenfox-advanced)나 [브레이브](#brave) 같은 다른 프라이버시 브라우저와 비슷하게 [단순한 핑거프린팅 스크립트](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting)로부터 보호해 줍니다. 멀바드 브라우저는 다른 프라이버시 브라우저가 제공하는 유연성과 편의성을 일부 포기하는 대신, 이러한 보호 기능을 별도 설정 없이 기본으로 제공합니다.

==가장 강력한 핑거프린팅 방지 효과를 얻으려면 멀바드 브라우저를 VPN**과 함께** 사용할 것을 권장합니다==. 멀바드 VPN이든 다른 추천 VPN 제공업체든 상관없습니다. 멀바드 브라우저와 VPN을 함께 사용하면 다른 많은 사용자와 핑거프린트 및 IP 주소 풀을 공유하게 되어, 그 속에 섞여 들 수 있는 "군중"이 생깁니다. 이 전략은 고급 추적 스크립트를 방어하는 가장 좋은 방법이며, 토르 브라우저가 사용하는 것과 같은 핑거프린팅 방지 기법입니다.

멀바드 브라우저는 어떤 VPN 제공업체와도 함께 사용할 수 있지만, 이 "군중"이 존재하려면 같은 VPN을 쓰는 다른 사람들도 멀바드 브라우저를 사용해야 한다는 점에 유의하세요. 이는 다른 제공업체보다 멀바드 VPN에서 그럴 가능성이 더 높습니다. 멀바드 브라우저에는 VPN 연결 기능이 내장되어 있지 않으며, 브라우징 전에 VPN을 사용 중인지 확인하지도 않습니다. VPN 연결은 따로 설정하고 관리해야 합니다.

멀바드 브라우저에는 *유블록 오리진*과 *노스크립트* 브라우저 확장 프로그램이 기본으로 설치되어 있습니다. 일반적으로 [브라우저 확장 프로그램](browser-extensions.md)을 *추가로* 설치하는 것은 권장하지 않지만, 브라우저에 기본으로 설치된 이 확장 프로그램들은 제거하거나 기본값과 다르게 설정해서는 **안 됩니다**. 그렇게 하면 여러분의 브라우저 핑거프린트가 다른 멀바드 브라우저 사용자와 눈에 띄게 달라지기 때문입니다. 또한 멀바드 브라우저 확장 프로그램도 기본으로 설치되어 있습니다. 원한다면 브라우저 핑거프린트에 [영향을 주지](https://mullvad.net/en/help/tag/mullvad-browser#112) 않고 안전하게 제거할 *수 있으며*, 멀바드 VPN을 사용하지 않더라도 그대로 두어도 안전합니다.

### 사생활 보호 모드

멀바드 브라우저는 항상 사생활 보호 모드로 작동합니다. 즉, 브라우저를 닫을 때마다 방문 기록, 쿠키, 기타 사이트 데이터가 항상 삭제됩니다. 북마크, 브라우저 설정, 확장 프로그램 설정은 유지됩니다.

이는 고급 형태의 추적을 막기 위해 필요하지만, 편의성과 다중 계정 컨테이너 같은 일부 파이어폭스 기능을 포기해야 합니다. 여러 브라우저를 함께 사용할 수 있다는 점을 기억하세요. 예를 들어, 로그인 상태를 유지하고 싶거나 멀바드 브라우저에서 제대로 작동하지 않는 몇몇 사이트에는 파이어폭스+아켄폭스를 사용하고, 일반적인 브라우징에는 멀바드 브라우저를 사용하는 방법을 고려할 수 있습니다.

## 파이어폭스

<div class="admonition recommendation" markdown>

![파이어폭스 로고](assets/img/browsers/firefox.svg){ align=right }

**파이어폭스**는 다양한 [추적 유형](https://support.mozilla.org/ko/kb/enhanced-tracking-protection-firefox-desktop#w_hyangsangdoen-cujeog-bangji-gineungi-cadanhaneun-geos)을 차단하는 데 도움이 되는 [향상된 추적 방지 기능](https://support.mozilla.org/ko/kb/enhanced-tracking-protection-firefox-desktop) 등 강력한 프라이버시 설정을 제공합니다.

[:octicons-home-16: 홈페이지](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="문서" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="기여하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: 윈도우](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: 리눅스](https://mozilla.org/firefox/linux)
- [:simple-flathub: 플랫허브](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

파이어폭스는 모질라 웹사이트에서 다운로드한 파일에 고유한 [다운로드 토큰](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0)을 포함하고, 파이어폭스의 텔레메트리를 이용해 이 토큰을 전송합니다. 이 토큰은 [모질라 FTP](https://ftp.mozilla.org/pub/firefox/releases/)에서 배포되는 릴리스에는 포함되어 있지 **않습니다**.

</div>

### 권장 파이어폭스 설정

이 옵션은 :material-menu: → **설정**에서 찾을 수 있습니다.

#### 검색

- [ ] **검색 제안 표시** 체크 해제

검색 제안 기능은 여러분의 지역에서 제공되지 않을 수도 있습니다.

검색 제안 기능은 실제로 검색을 실행하는지와 관계없이 주소 표시줄에 입력하는 모든 내용을 기본 검색 엔진으로 전송합니다. 검색 제안 기능을 끄면 검색 엔진 제공업체에 어떤 데이터를 보낼지 더 정밀하게 제어할 수 있습니다.

##### 파이어폭스 제안

[파이어폭스 제안](https://support.mozilla.org/kb/firefox-suggest)은 검색 제안과 비슷한 기능입니다. 검색 제안을 끄도록 권장하는 것과 같은 이유로 이 기능도 끌 것을 권장합니다. **주소 표시줄** 항목 아래에 이 옵션들이 보이지 않는다면 새로운 환경이 적용되지 않은 것이므로, 이 변경 사항은 무시해도 됩니다.

- [ ] **파이어폭스의 제안** 체크 해제
- [ ] **스폰서의 제안** 체크 해제

> 모질라에 따르면 ["파이어폭스 제안의 일부 기능은 현재 일부 지역에서만 이용할 수 있습니다."](https://support.mozilla.org/kb/firefox-suggest)

#### 개인 정보 및 보안

##### 향상된 추적 방지 기능

- [x] 향상된 추적 방지 기능에서 **엄격** 선택

이 설정은 소셜 미디어 추적기, 핑거프린팅 스크립트(단, *모든* 핑거프린팅을 막아 주지는 않습니다), 암호화폐 채굴기, 교차 사이트 추적 쿠키, 기타 일부 추적 콘텐츠를 차단하여 여러분을 보호합니다. ETP는 여러 일반적인 위협으로부터 보호해 주지만, 사이트 사용성에 미치는 영향을 최소화하거나 전혀 없도록 설계되었기 때문에 모든 추적 경로를 차단하지는 않습니다.

##### 종료 시 데이터 삭제

특정 사이트에 로그인된 상태를 유지하려면 **쿠키 및 사이트 데이터** → **예외 관리...**에서 예외를 허용할 수 있습니다

- [x] **파이어폭스를 닫을 때 쿠키와 사이트 데이터 삭제** 체크

이 설정은 지속 쿠키로부터 보호해 주지만, 한 번의 브라우징 세션 동안 얻은 쿠키로부터는 보호하지 못합니다. 이 설정을 켜면 파이어폭스를 다시 시작하는 것만으로 브라우저 쿠키를 쉽게 정리할 수 있습니다. 자주 방문하는 특정 사이트에 로그인된 상태를 유지하고 싶다면, 사이트별로 예외를 설정할 수 있습니다.

##### 텔레메트리

- [ ] **모질라에 기술 및 상호 작용 데이터 보내기** 체크 해제
- [ ] **개인화된 확장 기능 추천 허용** 체크 해제
- [ ] **연구 설치 및 실행** 체크 해제
- [ ] **모질라에 일일 사용 핑 보내기** 체크 해제
- [ ] **충돌 보고서 자동 전송** 체크 해제

파이어폭스에 대한 모질라의 개인정보 처리방침에 따르면,

> 파이어폭스는 사용자의 파이어폭스 버전과 언어, 기기 운영 체제와 하드웨어 구성, 메모리, 충돌 및 오류에 관한 기본 정보, 업데이트·세이프 브라우징·활성화 같은 자동화된 프로세스의 결과에 관한 데이터를 저희에게 전송합니다. 파이어폭스가 저희에게 데이터를 전송할 때, 여러분의 IP 주소는 서버 로그의 일부로 일시적으로 수집됩니다.

또한 모질라 계정 서비스는 [일부 기술 데이터](https://mozilla.org/privacy/mozilla-accounts)를 수집합니다. 모질라 계정을 사용한다면 다음과 같이 수집을 거부할 수 있습니다:

1. [accounts.firefox.com의 프로필 설정](https://accounts.firefox.com/settings#data-collection)을 엽니다
2. **데이터 수집 및 사용** > **파이어폭스 계정 개선 돕기** 체크 해제

##### HTTPS 전용 모드

- [x] **모든 창에서 HTTPS 전용 모드 사용** 선택

이 설정은 의도치 않게 평문 HTTP로 웹사이트에 접속하는 것을 막아 줍니다. 요즘은 HTTPS를 지원하지 않는 사이트가 드물기 때문에, 일상적인 브라우징에는 영향이 거의 또는 전혀 없을 것입니다.

##### DNS over HTTPS

[DNS over HTTPS 제공업체](dns.md)를 사용하는 경우:

- [x] **최대 보호**를 선택하고 적절한 제공업체 선택

최대 보호는 DNS over HTTPS 사용을 강제하며, 파이어폭스가 보안 DNS 리졸버에 연결할 수 없거나 보안 DNS 리졸버가 접속하려는 도메인의 레코드가 존재하지 않는다고 응답하면 보안 경고가 표시됩니다. 이를 통해 연결된 네트워크가 몰래 DNS 보안 수준을 낮추는 것을 막을 수 있습니다.

#### 동기화

[파이어폭스 동기화](https://hacks.mozilla.org/2018/11/firefox-sync-privacy)를 사용하면 브라우징 데이터(방문 기록, 북마크 등)를 모든 기기에서 이용할 수 있으며, 이 데이터는 E2EE로 보호됩니다.

### 아켄폭스(고급)

<div class="admonition tip" markdown>
<p class="admonition-title">고급 핑거프린팅 방지에는 멀바드 브라우저를 사용하세요</p>

[멀바드 브라우저](#mullvad-browser)는 파이어폭스보다 강력한 핑거프린팅 방지 기능을 별도 설정 없이 제공하며, 이러한 보호 기능을 누리기 위해 멀바드 VPN을 사용할 필요도 없습니다. VPN과 함께 사용하면 멀바드 브라우저는 아켄폭스가 막지 못하는 더 고급 추적 스크립트까지 막을 수 있습니다. 그래도 파이어폭스는 훨씬 더 유연하고, 로그인 상태를 유지해야 하는 웹사이트에 사이트별 예외를 허용할 수 있다는 장점이 있습니다.

</div>

[아켄폭스 프로젝트](https://github.com/arkenfox/user.js)는 파이어폭스를 위해 신중하게 검토된 설정 모음을 제공합니다. 아켄폭스를 사용하기로 [결정](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not)했다면, [일부 옵션](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-%5BCommon%5D)은 주관적으로 엄격하거나 일부 웹사이트가 제대로 작동하지 않게 만들 수 있습니다. 이러한 옵션은 필요에 맞게 [쉽게 변경](https://github.com/arkenfox/user.js/wiki/3.1-Overrides)할 수 있습니다. 전체 [위키](https://github.com/arkenfox/user.js/wiki)를 꼼꼼히 읽어 볼 것을 **강력히 권장합니다**. 아켄폭스는 [컨테이너](https://support.mozilla.org/kb/containers#w_for-advanced-users) 지원도 활성화합니다.

아켄폭스는 캔버스 무작위화와 파이어폭스에 내장된 핑거프린팅 저항 설정을 통해 기본적이거나 단순한 추적 스크립트를 막는 것만을 목표로 합니다. 멀바드 브라우저나 토르 브라우저처럼 여러분의 브라우저를 수많은 다른 아켄폭스 사용자 사이에 섞이게 만드는 것은 목표로 하지 않는데, 이것이 고급 핑거프린팅 추적 스크립트를 막는 유일한 방법입니다. 여러 브라우저를 함께 사용할 수 있다는 점을 기억하세요. 예를 들어, 로그인 상태를 유지하고 싶거나 신뢰하는 몇몇 사이트에는 파이어폭스+아켄폭스를 사용하고, 일반적인 브라우징에는 멀바드 브라우저를 사용하는 방법을 고려할 수 있습니다.

## 브레이브

<div class="admonition recommendation annotate" markdown>

![브레이브 로고](assets/img/browsers/brave.svg){ align=right }

**브레이브 브라우저**에는 콘텐츠 차단기와 [프라이버시 기능](https://brave.com/privacy-features)이 내장되어 있으며, 그중 상당수가 기본적으로 활성화되어 있습니다.

브레이브는 크로미움 웹 브라우저 프로젝트를 기반으로 만들어졌기 때문에 익숙하게 느껴지고 웹사이트 호환성 문제도 거의 없습니다.

[:octicons-home-16: 홈페이지](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="어니언 서비스" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-github: 깃허브](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: 윈도우](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: 리눅스](https://brave.com/linux)
- [:simple-flathub: 플랫허브](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

브레이브는 브레이브 웹사이트에서 다운로드한 파일 이름에 "[추천 코드](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)"를 추가합니다. 이 코드는 브라우저를 어디에서 다운로드했는지 추적하는 데 사용되며, 예를 들어 `Brave-Browser-BRV002.pkg`라는 이름의 다운로드 파일에서는 `BRV002`가 추천 코드입니다. 그런 다음 설치 프로그램은 설치 과정이 끝날 때 추천 코드와 함께 브레이브 서버에 핑을 보냅니다. 이 점이 걱정된다면 설치 파일을 열기 전에 파일 이름을 바꾸면 됩니다.

</div>

### 권장 브레이브 설정

이 옵션은 :material-menu: → **설정**에서 찾을 수 있습니다.

#### 실드

브레이브는 [실드](https://support.brave.com/hc/articles/360022973471-What-is-Shields) 기능에 몇 가지 핑거프린팅 방지 조치를 포함하고 있습니다. 이 옵션들은 방문하는 모든 페이지에 [전역으로](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) 설정할 것을 권장합니다.

실드 옵션은 필요에 따라 사이트별로 낮출 수 있지만, 기본적으로 다음과 같이 설정할 것을 권장합니다:

<div class="annotate" markdown>

- [x] *추적기 및 광고 차단*에서 **공격적** 선택

<details class="warning" markdown>
<summary>기본 필터 목록 사용</summary>

브레이브에서는 내부 페이지인 `brave://adblock`에서 추가 콘텐츠 필터를 선택할 수 있습니다. 이 기능은 사용하지 말고 기본 필터 목록을 유지할 것을 권장합니다. 추가 목록을 사용하면 다른 브레이브 사용자들 사이에서 눈에 띄게 되며, 브레이브에 익스플로잇이 존재하고 사용 중인 목록 중 하나에 악성 규칙이 추가되는 경우 공격 표면이 늘어날 수도 있습니다.

</details>

- [x] *HTTPS로 연결 업그레이드*에서 **엄격** 선택
- [x] (선택 사항) **스크립트 차단** 선택 (1)
- [x] **핑거프린팅 차단** 체크
- [x] **타사 쿠키 차단** 선택
- [x] **이 사이트를 닫으면 나를 잊기** 체크 (2)
- [ ] 모든 소셜 미디어 구성 요소 체크 해제

</div>

1. 이 옵션은 자바스크립트를 비활성화하므로 많은 사이트가 제대로 작동하지 않게 됩니다. 이를 해결하려면 주소 표시줄의 실드 아이콘을 클릭하고 *고급 제어*에서 이 설정을 체크 해제하여 사이트별로 예외를 설정할 수 있습니다.
2. 자주 방문하는 특정 사이트에 로그인된 상태를 유지하고 싶다면, 주소 표시줄의 실드 아이콘을 클릭하고 *고급 제어*에서 이 설정을 체크 해제하여 사이트별로 예외를 설정할 수 있습니다.

#### 개인정보 보호 및 보안

<div class="annotate" markdown>

- [x] *보안* → *자바스크립트 최적화 및 보안 관리*에서 **사이트에서 자바스크립트 최적화를 사용하도록 허용하지 않음** 선택 (1)
- [x] *사이트 및 실드 설정*에서 **사용하지 않는 사이트의 권한 자동 삭제** 선택
- [x] [*WebRTC IP 처리 정책*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)에서 **프록시되지 않은 UDP 사용 중지** 선택
- [ ] **푸시 메시지에 구글 서비스 사용** 체크 해제
- [x] **AMP 페이지 자동 리디렉션** 선택
- [x] **추적 URL 자동 리디렉션** 선택
- [x] **언어 설정을 기반으로 한 사이트의 핑거프린팅 방지** 선택

</div>

1. V8 최적화 도구를 비활성화하면 자바스크립트 JIT(Just-In-Time) 컴파일의 [*일부*](https://grapheneos.social/@GrapheneOS/112708049232710156)가 비활성화되어 공격 표면이 줄어듭니다.

##### 토르 창

[**토르 비공개 창**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity)을 사용하면 비공개 창에서 트래픽을 토르 네트워크로 라우팅하고 .onion 서비스에 접속할 수 있어, 경우에 따라 유용할 수 있습니다. 하지만 브레이브는 토르 브라우저만큼 핑거프린팅에 강하지 **않고**, 토르와 함께 브레이브를 사용하는 사람도 훨씬 적기 때문에 눈에 띄게 됩니다. 위협 모델상 강력한 익명성이 필요하다면 [토르 브라우저](tor.md#tor-browser)를 사용하세요.

##### 데이터 수집

- [ ] **개인정보를 보호하는 제품 분석(P3A) 허용** 체크 해제
- [ ] **브레이브에 일일 사용 핑 자동 전송** 체크 해제
- [ ] **진단 보고서 자동 전송** 체크 해제

#### Web3

브레이브의 Web3 기능은 브라우저 핑거프린트와 공격 표면을 늘릴 가능성이 있습니다. 이러한 기능을 사용하지 않는다면 비활성화해야 합니다.

- *기본 이더리움 지갑*에서 **확장 프로그램(대체 없음)** 선택
- *기본 솔라나 지갑*에서 **확장 프로그램(대체 없음)** 선택
- *기본 카르다노 지갑*에서 **확장 프로그램(대체 없음)** 선택

#### 확장 프로그램

- [ ] 사용하지 않는 내장 확장 프로그램을 모두 체크 해제

#### 검색 엔진

[파이어폭스](#search)에서 이 기능을 끄도록 권장하는 것과 같은 이유로, 브레이브에서도 검색 제안을 끌 것을 권장합니다.

- [ ] **검색 제안 표시** 체크 해제

#### 시스템

<div class="annotate" markdown>

- [ ] **브레이브를 닫아도 백그라운드 앱 계속 실행**을 체크 해제하여 백그라운드 앱 비활성화 (1)

</div>

1. 이 옵션은 일부 플랫폼에는 없습니다.

#### 브레이브 동기화

[브레이브 동기화](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync)를 사용하면 계정 없이도 브라우징 데이터(방문 기록, 북마크 등)를 모든 기기에서 이용할 수 있으며, 이 데이터는 E2EE로 보호됩니다.

#### 브레이브 리워드 및 월렛

**브레이브 리워드**를 사용하면 브레이브에서 특정 행동을 할 때 BAT(Basic Attention Token) 암호화폐를 받을 수 있습니다. 이 기능은 일부 선정된 제공업체의 수탁 계정과 KYC에 의존합니다. 저희는 BAT를 [프라이버시 암호화폐](cryptocurrency.md)로 추천하지 않으며 [수탁형 지갑](advanced/payments.md#wallet-custody) 사용도 권장하지 않으므로, 이 기능은 사용하지 않는 것이 좋습니다.

**브레이브 월렛**은 컴퓨터에서 로컬로 작동하지만 프라이버시 암호화폐를 전혀 지원하지 않으므로, 이 기능 역시 사용하지 않는 것이 좋습니다.

## 평가 기준

**저희는 추천하는 프로젝트 중 어느 곳과도 제휴 관계가 없다는 점을 알려 드립니다.** [일반 평가 기준](about/criteria.md) 외에도, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 사용하기로 결정하기 전에 이 목록을 숙지하고, 자신에게 맞는 선택인지 직접 조사해 보시기 바랍니다.

### 최소 요구 사항

- 오픈 소스 소프트웨어여야 합니다.
- 자동 업데이트를 지원해야 합니다.
- 업스트림 릴리스 후 0~1일 이내에 엔진 업데이트를 받아야 합니다.
- 리눅스, macOS, 윈도우에서 사용할 수 있어야 합니다.
- 브라우저의 프라이버시를 강화하는 데 필요한 변경 사항이 사용자 경험에 부정적인 영향을 주어서는 안 됩니다.
- 기본적으로 제3자 쿠키를 차단해야 합니다.
- 교차 사이트 추적을 완화하기 위해 [상태 분할](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning)을 지원해야 합니다.[^1]

### 이상적인 경우

이상적인 경우의 기준은 이 카테고리의 완벽한 프로젝트에 저희가 기대하는 바를 나타냅니다. 저희가 추천하는 항목에 이 기능의 일부 또는 전부가 없을 수도 있지만, 이러한 기능을 갖춘 항목은 이 페이지에서 다른 항목보다 높은 순위에 오를 수 있습니다.

- 콘텐츠 차단 기능이 내장되어 있는 것이 좋습니다.
- 쿠키 구획화([다중 계정 컨테이너](https://support.mozilla.org/ko/kb/containers)와 같은 방식)를 지원하는 것이 좋습니다.
- PWA(Progressive Web App)를 지원하는 것이 좋습니다. PWA를 사용하면 특정 웹사이트를 컴퓨터에 네이티브 앱처럼 설치할 수 있습니다. PWA는 브라우저의 정기 보안 업데이트 혜택을 받기 때문에, 일렉트론 기반 앱을 설치하는 것보다 유리할 수 있습니다.
- 사용자 프라이버시에 영향을 주지 않는 부가 기능(블로트웨어)은 포함하지 않는 것이 좋습니다.
- 기본적으로 텔레메트리를 수집하지 않는 것이 좋습니다.
- 오픈 소스 동기화 서버 구현을 제공하는 것이 좋습니다.
- 기본 검색 엔진이 [프라이버시 검색 엔진](search-engines.md)으로 설정되어 있는 것이 좋습니다.

[^1]: 브레이브의 구현 방식은 [브레이브 프라이버시 업데이트: 프라이버시를 위한 네트워크 상태 분할](https://brave.com/privacy-updates/14-partitioning-network-state)에 자세히 설명되어 있습니다.
