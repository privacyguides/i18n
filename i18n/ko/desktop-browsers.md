---
meta_title: "프라이버시 중점 PC, Mac용 웹 브라우저 - Privacy Guides"
title: 데스크톱 브라우저
icon: material/laptop
description: 이러한 개인정보 보호 브라우저는 데스크톱 시스템에서 일반적인/비익명 인터넷 브라우징을 할 때 현재 권장하는 브라우저입니다.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: 비공개 탐색 데스크톱 브라우저 권장 목록
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/ko/browser
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
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
      - Linux
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
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-account-cash: 감시 자본주의(Surveillance Capitalism)](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

다음은 표준/비익명 브라우징을 위해 현재 권장하는 **데스크톱 웹 브라우저** 및 설정입니다. 강력한 프라이버시 보호 및 핑거프린팅 방지가 기본 제공되는 브라우저를 원하신다면 [Mullvad Browser](#mullvad-browser)를, 평범한 인터넷 브라우저 중 Google Chrome의 적절한 대체제를 원하신다면 [Firefox](#firefox)를, Chromium 브라우저 호환성이 필요하시다면 [Brave](#brave)를 추천드립니다.

익명으로 인터넷을 이용해야 한다면, 대신 [Tor 브라우저를](tor.md) 사용해야 합니다. 이 페이지에서는 몇 가지 설정 관련 권장 사항을 제시하고 있지만, 온라인 추적으로부터 가장 효과적으로 보호해 주는 것은 Tor 브라우저입니다.

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**멀바드 브라우져** 는 토르[Tor Browser](tor.md#tor-browser)에서 토르 네트워크 통합 기능이 빠진 브라우져입니다. 이 프로젝트는 VPN 사용자에게 Tor 브라우저의 지문 인식 방지 기술을 제공하는 것을 목표로 하며, 이는 [:material-eye-outline: 대규모 감시](basics/common-threats.md#mass-surveillance-programs)에 대항하는 핵심적인 보호 수단입니다{ .pg-blue }. Tor 프로젝트에서 개발하고 [Mullvad](vpn.md#mullvad)에서 배포합니다. Mullvad VPN 사용이 필수적이지 **않습니다**.

[:octicons-home-16: 홈페이지](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="프라이버시 정책" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title=문서}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

[Tor 브라우저와](tor.md) 마찬가지로, Mullvad 브라우저는 사용자의 브라우저 지문을 다른 수많은 Mullvad 브라우저 사용자들의 지문과 유사하게 만들어 지문 추적을 방지하도록 설계되었으며, *‘표준(Standard*)’, *‘더 안전(Safer* )’, *‘가장 안전(Safest*)’이라는 기본 보안 수준에 따라 자동으로 구성되는 기본 설정과 확장 기능을 포함하고 있습니다.

따라서 기본 [보안 수준을](https://tb-manual.torproject.org/security-settings) 조정하는 것 외에는 브라우저 설정을 절대 아무것도 변경하지 않는 것이 매우 중요합니다. 보안 수준을 조정한 후에는 브라우저를 계속 사용하려면 반드시 브라우저를 다시 시작해야 **합니다**. 그렇지 않으면 [보안 설정이 완전히 적용되지 않을 수 있으며](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), 이로 인해 선택한 설정에 근거해 예상했던 것보다 지문 정보 노출 및 악용에 대한 위험이 더 커질 수 있습니다.

추가적인 수정을 할 경우 고유한 핑거프린트를 갖게 됩니다. 즉 이 브라우저를 쓰는 의미가 사라집니다. 만약 핑거프린팅을 신경 쓰지 않고 자유로운 브라우저 설정을 원하실 경우, [Firefox](#firefox)를 추천드립니다.

### 핑거프린팅 방지

[VPN을](vpn.md) 사용하지 **않더라도**, Mullvad 브라우저는[Firefox+Arkenfox나](#arkenfox-advanced) [Brave와](#brave) 같은 다른 프라이버시 브라우저와 마찬가지로 [단순한 지문 인식 스크립트에](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) 대한 보호 기능을 제공합니다. Mullvad 브라우저는 다른 비공개 탐색 브라우저에서 제공하는 유연성과 편의성을 일부 희생하여, 별도로 설정할 필요 없이 핑거프린트 보호 기능을 기본으로 제공합니다.

==가장 강력한 핑거프린팅 방지 보호를 원하시는 경우, **Mullvad 브라우저와 VPN을 같이 사용**하실 것을 권장합니다.==(Mullvad VPN 혹은 그 외 권장 VPN 서비스) Mullvad 브라우저와 VPN을 사용하면 핑거프린트, IP 주소 대역을 다른 많은 사용자와 공유하여 '군중' 사이에 섞일 수 있습니다. 이 전략은 고급 추적 스크립트에 대응하는 가장 효과적인 방법이며, Tor Browser에서 사용하는 것과 동일한 핑거프린팅 방지 기술입니다.

Mullvad 브라우저는 어떤 VPN 제공업체와도 함께 사용할 수 있지만, 이 “군중(crowd)”이 형성되려면 해당 VPN을 사용하는 다른 사람들도 모두 Mullvad 브라우저를 사용해야 합니다. 이러한 상황은 다른 VPN 제공업체보다 Mullvad VPN에서 더 발생할 가능성이 높습니다. Mullvad 브라우저는 VPN 연결 기능을 내장하고 있지 않으며, 브라우저 이용에 앞서 VPN 사용 여부를 확인하는 기능 또한 없습니다. 사용자는 VPN 연결을 따로 설정하고 관리해야 합니다.

Mullvad 브라우저는 *uBlock Origin*, *NoScript* 브라우저 확장 프로그램이 기본 설치되어 있습니다. 일반적으로 [브라우저 확장 프로그램을](browser-extensions.md) *추가로* 설치하는 것은 권장하지 않지만, 브라우저에 기본으로 설치된 이러한 확장 프로그램은 제거하거나 기본 설정값을 변경해서는 **안** 됩니다. 그렇게 할 경우, 사용자의 브라우저 지문이 다른 Mullvad 브라우저 사용자들의 것과 눈에 띄게 달라질 수 있기 때문입니다. 또한 Mullvad 브라우저 확장 프로그램이 미리 설치되어 있는데, 원하신다면 브라우저 지문에 [영향을 주지](https://mullvad.net/en/help/tag/mullvad-browser#112) 않고 안전하게 제거할 *수* 있지만, Mullvad VPN을 사용하지 않더라도 그대로 두어도 안전합니다.

### 사생활 보호 모드

Mullvad 브라우저는 항상 사생활 보호 모드로 작동하므로 방문 기록, 쿠키, 기타 사이트 데이터는 브라우저를 닫을 때마다 매번 지워집니다. 북마크, 브라우저 설정, 확장 프로그램 설정은 유지됩니다.

이는 고급 추적을 방지하기 위해서 필요하지만, 편의성 및 일부 Firefox 기능(멀티 컨테이너 등)을 희생합니다. 하지만 여러분은 여러 브라우저를 사용할 수 있습니다. 로그인이 유지되어야 하는 사이트나 Mullvad 브라우저에서 제대로 작동하지 않는 사이트는 Firefox+Arkenfox를 사용하고, 그 외 일반적인 브라우저 탐색에는 Mullvad 브라우저를 사용하는 방법도 있습니다.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox 로고](assets/img/browsers/firefox.svg){ align=right }

**Firefox**는 [다양한 추적](https://support.mozilla.org/ko/kb/enhanced-tracking-protection-firefox-desktop#w_hyangsangdoen-cujeog-bangji-gineungi-cadanhaneun-geos)을 방지하는 [향상된 추적 방지 기능](https://support.mozilla.org/ko/kb/enhanced-tracking-protection-firefox-desktop) 등 강력한 프라이버시 설정을 제공합니다.

[:octicons-home-16: 홈페이지](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="문서" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="기여하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

Firefox는 Mozilla 웹사이트에서 다운로드하는 파일에 고유한 [다운로드 토큰](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0)을 포함하며, Firefox의 원격 측정 기능을 통해 이 토큰을 전송합니다. 이 토큰은 [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/ )에서 배포되는 버전에는 **포함되어 있지 않습니다**.

</div>

### 권장 파이어폭스 설정

이 옵션들은 :material-menu: → **설정에서** 찾을 수 있습니다.

#### 검색

-

사용자님의 지역에서는 검색 제안 기능이 제공되지 않을 수 있습니다.

검색어 제안 기능은 지역에 따라 제공되지 않을 수 있습니다. 검색어 제안 기능을 사용하면 실제로 검색을 실행하지 않더라도 주소 표시줄에 입력하는 모든 내용이 기본 검색 엔진으로 전송됩니다. 검색어 제안 기능을 비활성화하면 검색 엔진 제공업체에 어떤 데이터를 전송할지 더 세밀하게 제어할 수 있습니다.

##### Firefox 제안

[Firefox Suggest는](https://support.mozilla.org/kb/firefox-suggest) 검색 제안 기능과 유사한 기능입니다. 검색어 제안 기능을 비활성화하도록 권장하는 것과 같은 이유로 Firefox Suggest도 비활성화할 것을 권장합니다. **주소 표시줄** 항목 아래에 이러한 설정이 보이지 않는다면, 아직 새로운 인터페이스가 적용되지 않은 것이므로 해당 설정은 무시해도 됩니다.

- [ ] **웹에서 제안** 비활성화
- [ ] **스폰서에서 제안** 비활성화

> 모질라에 따르면, [ “파이어폭스 제안 기능의 일부는 현재 일부 지역에서만 이용할 수 있습니다.”](https://support.mozilla.org/kb/firefox-suggest)

#### 개인 정보 및 보안

##### 향상된 추적 방지 기능

- [x] 향상된 추적 방지 기능에서 **엄격** 활성화

이 설정은 소셜 미디어 추적기, 브라우저 지문 수집 스크립트(단, 모든 종류의 지문 수집을 방지하는 것은 아닙니다), 암호화폐 채굴 스크립트, 사이트 간 추적 쿠키 및 기타 일부 추적 콘텐츠를 차단하여 사용자를 보호합니다. ETP는 여러 가지 일반적인 위협으로부터 사용자를 보호하지만, 사이트 사용성에 미치는 영향을 최소화하거나 아예 없도록 설계되었기 때문에 모든 추적 경로를 차단하지는 않습니다.

##### 종료 시 데이터 정리

특정 사이트에 계속 로그인된 상태를 유지하려면, **‘쿠키 및 사이트 데이터’** → **‘예외 관리...**’에서 예외를 허용할 수 있습니다 **.**

- [x] **Firefox를 닫을 때 쿠키와 사이트 데이터를 삭제** 활성화

이 설정은 지속적으로 저장되는 쿠키로부터 사용자를 보호하지만, 하나의 브라우징 세션 동안 획득되는 쿠키까지 방지하지는 못합니다. 이 옵션을 활성화하면 Firefox를 재시작하는 것만으로 브라우저의 쿠키를 간편하게 삭제할 수 있습니다. 자주 방문하는 특정 웹사이트의 로그인 상태를 유지하고 싶다면, 사이트별로 예외를 설정할 수 있습니다.

##### 원격 분석

- [ ] **‘기술 및 상호작용 데이터를 Mozilla에 전송’** 항목의 선택을 해제하세요
- [ ] **‘맞춤형 확장 프로그램 추천 허용’의** 선택을 해제하세요
- [ ] **‘연구 설치 및 실행**’ 선택 해제
- [ ] **‘Mozilla에 일일 사용 현황 핑 보내기**’ 선택 해제
- [ ] **‘충돌 보고서 자동 전송**’ 선택 해제

모질라의 파이어폭스 개인정보 처리방침에 따르면,

> Firefox는 사용자의 Firefox 버전 및 언어, 기기 운영 체제 및 하드웨어 구성, 메모리, 충돌 및 오류에 대한 기본 정보, 업테이트 및 세이프 브라우징 같은 자동화 프로세스의 결과, 활성화 여부 등의 데이터를 당사(Mozilla)로 전송합니다. Firefox가 당사에 데이터를 전송할 때 사용자의 IP 주소는 당사 서버 로그의 일부로 일시적으로 수집됩니다.

또한, Mozilla 계정 서비스는 [일부 기술적 데이터를](https://mozilla.org/privacy/mozilla-accounts) 수집합니다. Mozilla 계정을 사용 중이라면 다음을 통해 수신 거부할 수 있습니다:

1. [accounts.firefox.com 프로필 설정](https://accounts.firefox.com/settings#data-collection) 열기
2. **데이터 수집 및 사용** > **Firefox 계정 개선에 참여** 비활성화

##### HTTPS 전용 모드

- [x] **모든 창에서 HTTPS 전용 모드 사용** 활성화

이를 통해 사용자가 의도치 않게 일반 텍스트 HTTP를 통해 웹사이트에 접속하는 것을 방지할 수 있습니다. 요즘은 HTTPS를 지원하지 않는 사이트가 드물기 때문에, 이는 여러분의 일상적인 웹 브라우징에 거의 또는 전혀 영향을 미치지 않습니다.

##### DNS over HTTPS

[HTTPS를 통한 DNS(DNS over HTTPS) 제공업체](dns.md)를 사용하는 경우:

- [x] **‘최대 보호’를** 선택하고 적합한 제공업체를 선택하세요

최대 보호 모드는 DNS over HTTPS 사용을 강제합니다. Firefox가 보안 DNS 확인 서버에 연결하지 못하거나, 해당 서버가 접속하려는 도메인의 DNS 레코드가 존재하지 않는다고 응답하면 보안 경고가 표시됩니다. 이를 통해 사용자가 연결한 네트워크가 DNS 보안 수준을 몰래 낮추는 행위를 방지할 수 있습니다.

#### 동기화(Sync)

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy)를 사용하면 방문 기록과 북마크 등의 브라우징 데이터를 여러 기기에서 이용할 수 있으며, 해당 데이터는 종단 간 암호화(E2EE)로 보호됩니다.

### Arkenfox (고급)

<div class="admonition tip" markdown>
<p class="admonition-title">고급 지문 추적 방지가 필요하다면 Mullvad Browser를 사용하세요.</p>

[Mullvad Browser](#mullvad-browser)는 기본 설정만으로도 Firefox보다 강력한 브라우저 지문 추적 방지 기능을 제공하며, 이러한 보호 기능을 이용하기 위해 Mullvad VPN을 반드시 사용할 필요는 없습니다. VPN을 함께 사용할 경우, Mullvad 브라우저는 Arkenfox가 차단하지 못하는 고급 추적 스크립트까지 차단할 수 있습니다. Firefox는 여전히 훨씬 유연하다는 장점이 있습니다. 또한 로그인 상태를 유지해야 하는 웹사이트에 대해 사이트별 예외를 설정할 수 있습니다.

</div>

[Arkenfox 프로젝트](https://github.com/arkenfox/user.js)는 Firefox에 적용할 수 있는, 신중하게 검토된 설정 모음을 제공합니다. Arkenfox를 사용하기로 [결정하셨다면](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not), [몇 가지 설정이](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-%5BCommon%5D) 주관적으로 다소 까다롭거나 일부 웹사이트가 제대로 작동하지 않을 수 있습니다. 하지만 이러한 설정은 필요에 따라 [쉽게 변경할](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) 수 있습니다. 해당 [위키의](https://github.com/arkenfox/user.js/wiki) 전체 [내용을](https://github.com/arkenfox/user.js/wiki) 꼼꼼히 읽어보시기를 **강력히 권장합니다**. Arkenfox는 [컨테이너](https://support.mozilla.org/kb/containers#w_for-advanced-users) 지원 기능도 제공합니다.

Arkenfox는 캔버스 무작위화(canvas randomization)와 Firefox에 내장된 지문 추적 방지 설정을 통해 기본적이거나 단순한 추적 스크립트를 방해하는 것을 목표로 합니다. 하지만 Mullvad Browser나 Tor Browser와 달리, 동일한 Arkenfox 설정을 사용하는 다수의 사용자 사이에 브라우저를 섞어 눈에 띄지 않게 만드는 것까지 목표로 하지는 않습니다. 이러한 방식으로 다른 사용자들과 브라우저의 특성을 비슷하게 만들어야 고급 지문 추적 스크립트의 추적을 효과적으로 방해할 수 있습니다. 브라우저를 여러 개 함께 사용해도 된다는 점을 기억하세요. 예를 들어, 로그인 상태를 유지해야 하거나 신뢰하는 일부 웹사이트에는 Firefox와 Arkenfox를 사용하고, 일반적인 웹 브라우징에는 Mullvad Browser를 사용할 수 있습니다.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave 로고](assets/img/browsers/brave.svg){ align=right }

**Brave 브라우저**에는 내장 콘텐츠 차단기와 [개인정보 보호 기능](https://brave.com/privacy-features)이 포함되어 있으며, 이들 중 상당수는 기본적으로 활성화되어 있습니다.

Brace는 Chromium 웹 브라우저 프로젝트 기반으로 구축되었으므로, 친숙하며 웹사이트 호환성 문제가 적습니다.

[:octicons-home-16: 홈페이지](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion 서비스" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

Brave는 Brave 웹사이트에서 다운로드한 파일의 이름에 “[추천 코드](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)”를 추가하는데, 이는 브라우저가 어느 출처에서 다운로드되었는지 추적하기 위한 것입니다. 예를 들어, `Brave-Browser-BRV002.pkg`라는 이름의 다운로드 파일에는 `BRV002`가 포함됩니다. 그러면 설치 프로그램이 설치 과정이 끝날 무렵 추천 코드를 포함해 Brave 서버에 핑을 보냅니다. 이 점이 걱정된다면, 설치 파일을 열기 전에 파일 이름을 변경할 수 있습니다.

</div>

### 권장되는 브레이브 설정

이 옵션들은 :material-menu: → **설정에서** 찾을 수 있습니다.

#### 쉴드

브레이브는 [‘쉴드’](https://support.brave.com/hc/articles/360022973471-What-is-Shields) 기능에 몇 가지 지문 추적 방지 조치를 포함하고 있습니다. 방문하는 모든 페이지에 대해 이러한 옵션을 [전체적으로](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) 설정하는 것을 권장합니다.

필요에 따라 사이트별로 보호 옵션을 낮출 수 있으나, 기본적으로 다음과 같이 설정할 것을 권장드립니다:

<div class="annotate" markdown>

- [x] *추적기 및 광고 차단* 항목에서 **공격적**으로 설정

<details class="warning" markdown>
<summary>기본 필터 목록 사용</summary>

브레이브는 내장된 `brave://adblock` 페이지에서 추가적으로 컨텐츠를 차단할 수 있는 필터를 선택할 수 있습니다. 이 기능을 사용하지 말고 기본 필터 목록을 유지할 것을 권장드립니다. 추가적인 목록을 사용하면 다른 Brave 사용자에 비해 더 눈에 띄게 되며, 만약 Brave에 취약점이 존재하고 여러분이 사용하는 규칙 목록에 악성 규칙이 포함될 경우 공격 표면을 증가시킬 수도 있습니다.

</details>

- [x] *HTTPS로 연결 업그레이드* 항목에서 **엄격**을 선택합니다.
- [x] (선택 사항) **스크립트 차단**을 선택합니다. (1)
- [x] **핑거프린팅 차단**을 선택합니다.
- [x] **제3자 쿠키 차단**을 선택합니다.
- [x] **이 사이트를 닫을 때 내 정보를 잊어주세요**(2)를 선택합니다.
- [ ] 모든 소셜 미디어 구성 요소의 선택을 해제합니다

</div>

1. 이 옵션을 선택하면 자바스크립트가 비활성화되어 많은 웹사이트가 제대로 작동하지 않게 됩니다. To fix them, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.
2. 자주 방문하는 특정 사이트에 로그인 상태를 유지하고 싶다면, 주소 표시줄의 방패 아이콘을 클릭한 후 *‘고급 설정*’에서 해당 설정의 체크 표시를 해제하여 사이트별로 예외를 설정할 수 있습니다.

#### 개인 정보 보호 및 보안

<div class="annotate" markdown>

- [x] *보안* → *자바스크립트 최적화 및 보안 관리*에서 **사이트의 자바스크립트 최적화 사용 허용 안 함**을 선택합니다 (1)
- [x] *사이트 및 쉴드 설정*에서 **사용하지 않는 사이트의 권한을 자동으로 제거**를 선택합니다.
- [x] [*WebRTC IP 처리 정책*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)에서 **프록시되지 않은 UDP 비활성화**를 선택합니다.
- [ ] **푸시 메시징에 Google 서비스 사용** 항목의 체크를 해제합니다.
- [x] **AMP 페이지 자동 리디렉션**을 선택합니다.
- [x] **추적 URL 자동 리디렉션**을 선택합니다.
- [x] **내 언어 기본 설정에 따라 사이트가 내 지문을 식별하는 것을 방지**를 선택합니다.

</div>

1. V8 최적화 기능을 비활성화하면 다음 기능을 비활성화함으로써 공격 표면을 줄일 수 있습니다. [*일부*](https://grapheneos.social/@GrapheneOS/112708049232710156) 자바스크립트 JIT(Just-In-Time) 컴파일 기능을 비활성화함으로써 공격 표면을 줄입니다.

##### Tor 창

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) allows you to route your traffic through the Tor network in Private Windows and access .onion services, which may be useful in some cases. However, Brave is **not** as resistant to fingerprinting as the Tor Browser is, and far fewer people use Brave with Tor, so you will stand out. If your threat model requires strong anonymity, use the [Tor Browser](tor.md#tor-browser).

##### Data Collection

- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**

#### Web3

Brave's Web3 features can potentially add to your browser fingerprint and attack surface. Unless you use any of these features, they should be disabled.

- Select **Extensions (no fallback)** under *Default Ethereum wallet*
- Select **Extensions (no fallback)** under *Default Solana wallet*
- Select **Extensions (no fallback)** under *Default Cardano wallet*

#### Extensions

- [ ] Uncheck all built-in extensions you don't use

#### Search engine

We recommend disabling search suggestions in Brave for the same reason we recommend disabling this feature in [Firefox](#search).

-

#### System

<div class="annotate" markdown>

- [ ] Uncheck **Continue running background apps when Brave is closed** to disable background apps (1)

</div>

1. 플랫폼에 따라 해당 옵션이 제공되지 않을 수 있습니다.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

### 최소 요구 사항

- 오픈 소스 소프트웨어여야 합니다.
- 자동 업데이트를 지원해야 합니다.
- Must receive engine updates in 0-1 days from upstream release.
- Must be available on Linux, macOS, and Windows.
- Any changes required to make the browser more privacy-respecting must not negatively impact user experience.
- Must block third-party cookies by default.
- Must support [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### 우대 사항

평가 기준에서 '우대 사항'은 해당 부문에서 완벽한 프로젝트에 기대하는 바를 나타냅니다. 다음의 우대 사항에 해당하지 않더라도 권장 목록에 포함될 수 있습니다. 단, 우대 사항에 해당할수록 이 페이지의 다른 항목보다 높은 순위를 갖습니다.

- Should include built-in content blocking functionality.
- Should support cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Should support Progressive Web Apps (PWAs). PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps because PWAs benefit from your browser's regular security updates.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Should not collect telemetry by default.
- Should provide an open-source sync server implementation.
- Should default to a [private search engine](search-engines.md).

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
