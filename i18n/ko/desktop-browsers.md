---
meta_title: "프라이버시 중점 PC, Mac용 웹 브라우저 - Privacy Guides"
title: "데스크톱 브라우저"
icon: material/laptop
description: Google Chrome보다 강력한 프라이버시 보호 기능을 제공하는 브라우저 목록입니다.
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

본 내용은 현재 표준/비익명 인터넷 탐색 용도로 권장되는 데스크톱 웹 브라우저 및 관련 설정 목록입니다. 강력한 프라이버시 보호 및 핑거프린팅 방지가 기본 제공되는 브라우저를 원하신다면 [Mullvad Browser](#mullvad-browser)를, 평범한 인터넷 브라우저 중 Google Chrome의 적절한 대체제를 원하신다면 [Firefox](#firefox)를, Chromium 브라우저 호환성이 필요하시다면 [Brave](#brave)를 추천드립니다.

익명으로 인터넷을 탐색해야 하는 경우라면, [Tor](tor.md)를 사용해야 합니다. 본 내용에서 몇 가지 권장 설정을 알려드리고 있지만, Tor 브라우저를 제외한 모든 브라우저는 *누군가* 어떻게든 추적할 수 있습니다.

## Mullvad Browser

!!! recommendation

    ![Mullvad Browser 로고](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    **Mullvad Browser**는 [Tor 브라우저](tor.md#tor-browser)에서 Tor 네트워크 통합을 제거한 버전입니다. Tor 브라우저의 핑거프린팅 방지 브라우저 기술을 VPN 사용자에게 제공하는 것을 주된 목적으로 합니다. Tor 프로젝트에서 개발하고 [Mullvad](vpn.md#mullvad)에서 배포합니다. Mullvad VPN 사용이 필수적이지 **않습니다**.
    
    [:octicons-home-16: 홈페이지](https://mullvad.net/en/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=문서}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="소스 코드" }
    
    ??? downloads "다운로드"
    
        - [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

[Tor 브라우저](tor.md)와 마찬가지로, Mullvad Browser는 브라우저 핑거프린트를 모든 Mullvad Browser 사용자끼리 동일하게 만들어 핑거프린팅을 방지하도록 설계되었습니다. 기본 보안 등급(*Standard*, *Safer*, *Safest*)에 따라 자동으로 설정되는 기본 설정 및 확장 프로그램을 포함하고 있습니다. 여러분은 브라우저의 기본 [보안 등급](https://tb-manual.torproject.org/security-settings/) 외에 추가적인 수정을 해서는 안 됩니다. 추가적인 수정을 할 경우 고유한 핑거프린트를 갖게 됩니다. 즉 이 브라우저를 쓰는 의미가 사라집니다. 만약 핑거프린팅을 신경 쓰지 않고 자유로운 브라우저 설정을 원하실 경우, [Firefox](#firefox)를 추천드립니다.

### 핑거프린팅 방지

[VPN](vpn.md)을 사용하지 **않을** 경우, Mullvad 브라우저는 [Naive 핑거프린팅 스크립트](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting)에 대해 여타 비공개 탐색 브라우저(Firefox+[Arkenfox](#arkenfox-advanced), [Brave](#brave))와 동일한 수준의 보호 기능을 제공합니다. Mullvad 브라우저는 다른 비공개 탐색 브라우저에서 제공하는 유연성과 편의성을 일부 희생하여, 별도로 설정할 필요 없이 핑거프린트 보호 기능을 기본으로 제공합니다.

==가장 강력한 핑거프린팅 방지 보호를 원하시는 경우, **Mullvad 브라우저와 VPN을 같이 사용**하실 것을 권장합니다.==(Mullvad VPN 혹은 그 외 권장 VPN 서비스) Mullvad 브라우저와 VPN을 사용하면 핑거프린트, IP 주소 대역을 다른 많은 사용자와 공유하여 '군중' 사이에 섞일 수 있습니다. 이 전략은 고급 추적 스크립트를 막을 수 있는 유일한 방법이자, Tor 브라우저에서 사용하는 것과 동일한 핑거프린트 방지 기술이기도 합니다.

Mullvad Browser는 특정 VPN 서비스에 의존하지 않으므로 어떤 VPN이든 같이 사용할 수 있습니다. 하지만 '군중 속에 섞여드는 효과'를 얻기 위해서는 여러분과 동일한 VPN을 사용하면서 Mullvad 브라우저도 사용하는 사람들이 존재한다는 전제가 필요합니다. 특히나 Mullvad 브라우저가 출시된지 얼마 되지 않은 지금 시점에서는 다른 VPN 서비스보다 Mullvad VPN의 사용자 중에 Mullvad 브라우저를 사용하는 사람이 많을 것입니다. Mullvad 브라우저는 VPN 연결 기능을 내장하고 있지 않으며, 브라우저 이용에 앞서 VPN 사용 여부를 확인하는 기능 또한 없습니다. 사용자는 VPN 연결을 따로 설정하고 관리해야 합니다.

Mullvad 브라우저는 *uBlock Origin*, *NoScript* 브라우저 확장 프로그램이 기본 설치되어 있습니다. 일반적으로는 브라우저 확장 프로그램을 *추가로* 설치하는 것을 [권장하지 않지만](#extensions), 기본 설치되어 있는 이러한 확장 프로그램은 제거하거나 기본 설정을 변경해서는 **안 됩니다**. 다른 Mullvad 브라우저 사용자와 핑거프린트가 차별화되기 때문입니다. 추가로, Mullvad 브라우저에는 'Mullvad Browser Extension' 확장 프로그램이 기본 설치되어 있습니다. Mullvad VPN 외 VPN 서비스를 사용하더라도 안전하게 사용할 수 있는 확장 프로그램이지만, 이 확장 프로그램을 제거하더라도 브라우저 핑거프린트에 영향을 주지 않으니 제거하고자 하는 경우 안심하고 제거해도 좋습니다.

### 사생활 보호 모드

Mullvad 브라우저는 항상 사생활 보호 모드로 작동하므로 방문 기록, 쿠키, 기타 사이트 데이터는 브라우저를 닫을 때마다 매번 지워집니다. 북마크, 브라우저 설정, 확장 프로그램 설정은 유지됩니다.

이는 고급 추적을 방지하기 위해서 필요하지만, 편의성 및 일부 Firefox 기능(멀티 컨테이너 등)을 희생합니다. 하지만 여러분은 여러 브라우저를 사용할 수 있습니다. 로그인이 유지되어야 하는 사이트나 Mullvad 브라우저에서 제대로 작동하지 않는 사이트는 Firefox+Arkenfox를 사용하고, 그 외 일반적인 브라우저 탐색에는 Mullvad 브라우저를 사용하는 방법도 있습니다.

### Mullvad Leta

Mullvad 브라우저는 DuckDuckGo가 기본 [검색 엔진](search-engines.md)으로 설정되어 있지만, Mullvad VPN 구독 시 사용 가능한 **Mullvad Leta** 검색 엔진도 기본 설치되어 있습니다. Mullvad Leta는 Google 유료 검색 API(유료 구독자 전용인 이유)에 바로 쿼리를 전송할 수 있지만, '유료 구독자 전용'이라는 점으로 인해 검색 쿼리와 Mullvad VPN 계정 사이의 연결점이 생길 가능성이 존재합니다. 이러한 이유로, 저희는 Mullvad가 VPN 구독자에 대한 정보를 거의 수집하지 않는다는 점을 알고 있음에도 불구하고 Mullvad Leta 사용을 권장하지 않습니다.

## Firefox

!!! recommendation

    ![Firefox 로고](assets/img/browsers/firefox.svg){ align=right }
    
    **Firefox**는 [다양한 추적](https://support.mozilla.org/ko/kb/enhanced-tracking-protection-firefox-desktop#w_hyangsangdoen-cujeog-bangji-gineungi-cadanhaneun-geos)을 방지하는 [향상된 추적 방지 기능](https://support.mozilla.org/ko/kb/enhanced-tracking-protection-firefox-desktop) 등 강력한 프라이버시 설정을 제공합니다.
    
    [:octicons-home-16: 홈페이지](https://firefox.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mozilla.org/privacy/firefox/){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://firefox-source-docs.mozilla.org/){ .card-link title=문서}
    [:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://donate.mozilla.org/){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-windows11: Windows](https://www.mozilla.org/firefox/windows)
        - [:simple-apple: macOS](https://www.mozilla.org/firefox/mac)
        - [:simple-linux: Linux](https://www.mozilla.org/firefox/linux)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

!!! warning "경고"
    Firefox는 Mozilla 웹사이트에서 다운로드할 경우 고유한 [다운로드 토큰](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0)이 포함되며, 해당 토큰은 Firefox 원격 분석 데이터 전송 시에 함께 전송됩니다. 고유 다운로드 토큰은 [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/) 릴리스에는 포함되어 있지 **않습니다**.

### 권장 설정

이러한 옵션은 :material-menu: → **설정**에서 확인할 수 있습니다

#### 검색

- [ ] **검색 제안 사용** 비활성화

여러분의 지역에 따라 검색 제안 기능이 제공되지 않을 수도 있습니다.

검색 제안 기능은 실제로 검색을 누르지 않더라도 주소창에 입력하는 모든 내용을 기본 검색 엔진으로 전송합니다. 검색 제안을 비활성화하여 검색 엔진 제공 업체에 전송하는 데이터를 보다 신중하게 조절할 수 있습니다.

#### 개인 정보 및 보안

##### 향상된 추적 방지 기능

- [x] 향상된 추적 방지 기능에서 **엄격** 활성화

소셜 미디어 추적기, 핑거프린팅 스크립트(*모든* 핑거프린팅으로부터 보호하지는 못함), 암호화폐 채굴기, 교차 사이트 추적 쿠키 및 기타 추적 콘텐츠를 차단합니다. 향상된 추적 방지 기능은 대부분의 일반적인 위협을 방지하지만, 웹사이트 사용성을 해치지 않도록 설계되었기 때문에 모든 추적 경로를 차단하지는 못합니다.

##### Firefox Suggest (미국 한정)

[Firefox Suggest](https://support.mozilla.org/en-US/kb/firefox-suggest) 기능은 검색 제안과 유사한 기능이며, 현재 미국에서만 사용 가능합니다. 검색 제안 사용을 비활성화한 것과 마찬가지 이유로 해당 기능을 비활성화할 것을 권장드립니다. **주소 표시줄** 헤더에 이러한 옵션이 표시되지 않는 경우 이는 무시하셔도 좋습니다.

- [ ] **웹에서 제안** 비활성화
- [ ] **스폰서에서 제안** 비활성화

##### 종료 시 데이터 정리

특정 사이트의 로그인을 유지하려면 **쿠키 및 사이트 데이터** → **예외 관리...**에서 예외를 허용할 수 있습니다.

- [x] **Firefox를 닫을 때 쿠키와 사이트 데이터를 삭제** 활성화

이 기능은 영구적인 쿠키로부터 여러분을 보호합니다. 하지만 한 번의 브라우저 세션 중에 획득한 쿠키로부터 여러분을 보호하지는 않습니다. 이 기능을 활성화해두면 브라우저 쿠키를 정리하고자 할 때 Firefox를 재시작하기만 하면 됩니다. 사이트별 예외를 설정해 자주 이용하는 특정 사이트의 로그인을 유지할 수 있습니다.

##### 원격 분석

- [ ] **Firefox가 기술과 상호 작용 정보를 Mozilla에 전송하도록 허용** 비활성화
- [ ] **Firefox가 연구를 설치하고 실행하도록 허용** 비활성화
- [ ] **Firefox가 사용자를 대신하여 백로그된 충돌 보고서를 보내도록 허용** 비활성화

> Firefox는 사용자의 Firefox 버전 및 언어, 기기 운영 체제 및 하드웨어 구성, 메모리, 충돌 및 오류에 대한 기본 정보, 업테이트 및 세이프 브라우징 같은 자동화 프로세스의 결과, 활성화 여부 등의 데이터를 당사(Mozilla)로 전송합니다. Firefox가 당사에 데이터를 전송할 때 사용자의 IP 주소는 당사 서버 로그의 일부로 일시적으로 수집됩니다.

또한 Firefox 계정 서비스는 [일부 기술 데이터](https://www.mozilla.org/en-US/privacy/firefox/#firefox-accounts)를 수집합니다. Firefox 계정을 이용하는 경우 이를 거부할 수 있습니다.

1. [accounts.firefox.com 프로필 설정](https://accounts.firefox.com/settings#data-collection) 열기
2. **데이터 수집 및 사용** > **Firefox 계정 개선에 참여** 비활성화

##### HTTPS 전용 모드

- [x] **모든 창에서 HTTPS 전용 모드 사용** 활성화

의도치 않게 일반 텍스트 HTTP로 웹사이트에 연결되는 것을 방지합니다. 최근에는 대부분의 사이트가 HTTPS를 지원하므로, 일상적인 웹 탐색에는 크게 영향을 미치지 않습니다.

##### DNS over HTTPS

If you use a [DNS over HTTPS provider](dns.md):

- [x] Select **Max Protection** and choose a suitable provider

Max Protection enforces the use of DNS over HTTPS, and a security warning will show if Firefox can’t connect to your secure DNS resolver, or if your secure DNS resolver says that records for the domain you are trying to access do not exist. This stops the network you're connected to from secretly downgrading your DNS security.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/)를 이용하면 자신의 모든 기기에서 브라우저 데이터(탐색 기록, 북마크 등)를 동기화할 수 있으며, E2EE로 보호됩니다.

### Arkenfox (고급)

!!! tip "고급 핑거프린팅 방지 기능을 원하신다면 Mullvad 브라우저를 사용하세요"

    [Mullvad 브라우저](#mullvad-browser)는 Arkenfox와 동일한 핑거프린팅 방지 보호 기능을 기본으로 제공합니다(이러한 보호 기능은 Mullvad VPN을 사용하지 않더라도 그대로 누릴 수 있습니다). VPN을 함께 사용할 경우, Mullvad 브라우저는 Arkenfox가 차단하지 못하는 고급 추적 스크립트까지 차단할 수 있습니다. 단, Arkenfox는 훨씬 더 유연성 있고, 사이트별 예외를 통해 특정 웹사이트에서 로그인 유지 등이 가능하다는 장점이 있습니다.

[Arkenfox 프로젝트](https://github.com/arkenfox/user.js)는 신중하게 고려된 Firefox용 옵션 모음을 제공합니다. Arkenfox를 [사용하기로 결정한](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) 경우, [일부 옵션](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common])은 주관적으로 판단했을 때 지나치게 엄격하거나 웹사이트가 올바르게 작동하지 않을 수 있습니다. 옵션은 필요한 경우 [손쉽게 변경 가능합니다](https://github.com/arkenfox/user.js/wiki/3.1-Overrides). 저희는 전체 [위키](https://github.com/arkenfox/user.js/wiki) 내용을 읽어보실 것을 **강력히 권장드립니다**. Arkenfox에는 [컨테이너](https://support.mozilla.org/ko/kb/containers) 지원 활성화 또한 포함되어 있습니다.

Arkenfox는 캔버스 무작위화(Randomization)와 Firefox에 기본 탑재된 핑거프린트 방지 구성 설정을 통해 기본적이거나 순진한(Naive) 추적 스크립트를 차단하는 것만 목표로 합니다. Mullvad 브라우저나 Tor 브라우저에서 사용하는 방식이자, 고급 핑거프린트 추적 스크립트를 막을 수 있는 유일한 방법인 '다른 사용자들 사이에 섞여들게 하는 것'은 Arkenfox의 목표가 아닙니다. 물론, 여러분은 여러 브라우저를 사용할 수 있습니다. 로그인이 유지되어야 하는 사이트나 믿을 만한 사이트는 Firefox+Arkenfox를 사용하고, 그 외 일반적인 브라우저 탐색에는 Mullvad 브라우저를 사용하는 방법도 있습니다.

## Brave

!!! recommendation

    ![Brave 로고](assets/img/browsers/brave.svg){ align=right }
    
    **Brave 브라우저**에는 콘텐츠 차단기와 [프라이버시 기능](https://brave.com/privacy-features/)이 내장되어 있으며, 이 중 상당수가 기본적으로 활성화되어 있습니다.
    
    Brace는 Chromium 웹 브라우저 프로젝트 기반으로 구축되었으므로, 친숙하며 웹사이트 호환성 문제가 적습니다.
    
    [:octicons-home-16: 홈페이지](https://brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="소스 코드" }
    
    ??? downloads annotate "다운로드"
    
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
        - [:simple-windows11: Windows](https://brave.com/download/)
        - [:simple-apple: macOS](https://brave.com/download/)
        - [:simple-linux: Linux](https://brave.com/linux/) (1)

    1. Flatpak 버전 Brave는 Chromium의 샌드박스 기능을 효과가 떨어지는 Flatpak 샌드박스로 대체하기 때문에, Flatpak 버전은 사용하지 않는 것이 좋습니다. 또한, 해당 패키지는 Brave Software, Inc.에서 직접 관리하는 패키지가 아닙니다.

**macOS users:** The download for Brave Browser from their official website is a `.pkg` installer which requires admin privileges to run (and may run other unnecessary scripts on your machine). As an alternative, you can download the latest `Brave-Browser-universal.dmg` file from their [GitHub releases](https://github.com/brave/brave-browser/releases/latest) page, which provides a traditional "drag to Applications folder" install.

!!! warning "경고"

    Brave adds a "[referral code](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" to the file name in downloads from the Brave website, which is used to track which source the browser was downloaded from, for example `BRV002` in a download named `Brave-Browser-BRV002.pkg`. The installer will then ping Brave's server with the referral code at the end of the installation process. If you're concerned about this, you can rename the installer file before opening it.

### 권장 설정

이러한 옵션은 :material-menu: → **설정**에서 확인할 수 있습니다.

#### 설정

##### 보호

Brave 브라우저의 [보호](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-) 기능에는 핑거프린팅 방지 조치가 포함되어 있습니다. 방문하는 모든 페이지에 [전역적으로](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) 옵션을 설정하는 것이 좋습니다.

필요에 따라 사이트별로 보호 옵션을 낮출 수 있으나, 기본적으로 다음과 같이 설정할 것을 권장드립니다:

<div class="annotate" markdown>

- [x] **언어 환경 설정을 기반으로 사이트가 지문을 남기지 못하게 합니다** 활성화
- [x] 추적기 & 광고 차단을 **공격적**으로 설정

    ??? warning "기본 필터 목록을 사용하세요"
        Brave 브라우저는 `brave://adblock` 내부 페이지에서 추가적인 콘텐츠 필터를 선택할 수 있습니다. 이 기능을 사용하지 말고 기본 필터 목록을 유지할 것을 권장드립니다. 추가적인 목록을 사용하면 다른 Brave 사용자에 비해 더 눈에 띄게 되며, 만약 Brave에 취약점이 존재하고 여러분이 사용하는 규칙 목록에 악성 규칙이 포함될 경우 공격 표면을 증가시킬 수도 있습니다.

- [x] Select **Strict** under **Upgrade connections to HTTPS**
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Strict, may break sites** under Block fingerprinting

</div>

1. 해당 옵션은 uBlock Origin의 고급 [차단 모드](https://github.com/gorhill/uBlock/wiki/Blocking-mode)나 [NoScript](https://noscript.net/) 확장 프로그램과 유사한 기능을 제공합니다.

##### 소셜 미디어 차단

- [ ] 모든 소셜 미디어 항목 비활성화

##### 개인 정보 보호 및 보안

<div class="annotate" markdown>

- [x] [WebRTC IP 처리 방침](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)에서 **프록시가 아닌 UDP 비활성화하기** 선택
- [ ] **푸시 메시지에 Google 서비스 사용** 비활성화
- [ ] **프라이버시 보호 제품 분석(P3A) 허용** 비활성화
- [ ] **일일 사용 Ping을 Brave에 자동으로 보내기** 비활성화
- [ ] **진단 보고서 자동 전송** 비활성화
- [ ] **Tor와 함께하는 개인정보 보호 창** 비활성화 (1)

    !!! tip "종료 시 데이터 정리"

        - [x] **쿠키 및 기타 사이트 데이터** 메뉴에서 **모든 창이 닫히면 쿠키 및 사이트 데이터 삭제** 활성화

        자주 방문하는 특정 사이트의 로그인을 유지하려면 **맞춤설정된 동작** 부분에서 사이트별 예외를 지정할 수 있습니다.

</div>

1. Brave 브라우저의 핑거프린팅 방지 기능은 Tor 브라우저만큼 강력하지 **않습니다**. 또한 Brave에서 Tor를 사용하는 사람은 훨씬 적기 때문에, 더욱 눈에 띄게 됩니다. [강력한 익명성이 필요한 경우라면](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-) [Tor 브라우저](tor.md#tor-browser)를 사용해야 합니다.

##### 확장 프로그램

**확장 프로그램**에서 자신이 사용하지 않는 기본 탑재 확장 프로그램 비활성화

- [ ] **Hangouts** 비활성화
- [ ] **WebTorrent** 비활성화

##### Web3

Brave의 Web3 기능은 잠재적으로 브라우저의 핑거프린트와 공격 표면을 증가시킬 수 있습니다. 여러분이 해당 기능을 사용하지 않는다면 비활성화해야 합니다.

- Select **Extensions (no fallback)** under Default Ethereum wallet and Default Solana wallet
- Set **Method to resolve IPFS resources** to **Disabled**

##### 시스템

<div class="annotate" markdown>

- [ ] **Brave 종료 후에도 백그라운드 앱을 계속 실행** 비활성화 (1)

</div>

1. 플랫폼에 따라 해당 옵션이 제공되지 않을 수 있습니다.

#### 동기화

[Brave 동기화](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync)를 이용하면 계정을 생성하지 않고도 자신의 모든 기기에서 브라우저 데이터(탐색 기록, 북마크 등)를 동기화할 수 있으며, E2EE로 보호됩니다.

#### Brave Rewards 및 Brave 월렛

**Brave Rewards**는 Brave 내에서 특정 작업을 수행하여 BAT(Basic Attention Token) 암호화폐를 받을 수 있는 기능입니다. 해당 기능은 일부 선정된 제공 업체의 수탁형 계정과 KYC(고객 신원 확인)에 기반하여 동작합니다. Privacy Guide는 BAT를 [프라이버시 암호화폐](cryptocurrency.md)로 권장하지 않으며, [수탁형 지갑](advanced/payments.md#other-coins-bitcoin-ethereum-etc) 사용 또한 권장하지 않습니다. 따라서 해당 기능은 사용하지 않을 것을 권장합니다.

**Brave 월렛**은 사용자 컴퓨터 로컬에서 작동하지만, 프라이버시 암호화폐를 지원하지 않으므로 이 또한 사용을 권장하지 않습니다.

## 추가 자료

일반적으로 Privacy Guides는 여러분이 공격 표면을 최소화할 수 있도록, 브라우저 확장 프로그램은 최소한으로만 설치할 것을 권장드립니다. 브라우저 확장 프로그램은 여러분의 브라우저에 대해서 막대한 접근 권한을 가지며, 여러분을 보다 [눈에 띄게](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint) 만들고, 사이트 격리를 [약화시킵니다](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ). 다만 예외적으로, 콘텐츠 차단 기능이 필요하다면 uBlock Origin을 권장드립니다.

### uBlock Origin

!!! recommendation

    ![uBlock Origin 로고](assets/img/browsers/ublock_origin.svg){ align=right }
    
    **uBlock Origin**은 많은 사람들이 사용하는 콘텐츠 차단기입니다. 광고, 추적기, 핑거프린팅 스크립트를 차단하는 용도로 유용합니다.
    
    [:octicons-repo-16: 저장소](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="소스 코드" }
    
    ??? downloads "다운로드"
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

[개발자가 작성한 문서](https://github.com/gorhill/uBlock/wiki/Blocking-mode)를 참고하여 모드 중 하나를 선택할 것을 권장드립니다. 필터 목록 추가는 성능에 영향을 미칠 수 있으며, [공격 표면을 증가시킬 수도 있습니다](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

##### 기타 목록

이 외에 추가를 고려해볼 만한 [필터 목록](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists)은 다음과 같습니다:

- [x] **개인정보** > **AdGuard URL Tracking Protection** 활성화
- [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt) 추가

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

!!! example "이 단락은 최근에 만들어졌습니다"

    Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

### 최소 요구 사항

- 오픈 소스 소프트웨어여야 합니다.
- 자동 업데이트를 지원해야 합니다.
- 업스트림 릴리스 0~1일 이내에 엔진 업데이트를 받아야 합니다.
- Linux, macOS, Windows에서 사용할 수 있어야 합니다.
- 브라우저의 프라이버시를 강화하는 데에 필요한 모든 변경 사항은 사용자 경험에 부정적인 영향을 미치지 않아야 합니다.
- 타사 쿠키를 기본적으로 차단해야 합니다.
- 크로스 사이트 추적을 완화하기 위해 [State Partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning)을 지원해야 합니다.[^1]

### 우대 사항

평가 기준에서 '우대 사항'은 해당 부문에서 완벽한 프로젝트에 기대하는 바를 나타냅니다. 다음의 우대 사항에 해당하지 않더라도 권장 목록에 포함될 수 있습니다. 단, 우대 사항에 해당할수록 이 페이지의 다른 항목보다 높은 순위를 갖습니다.

- 콘텐츠 차단 기능을 내장해야 합니다.
- 쿠키 구획화를 지원해야 합니다. (예시: [멀티 컨테이너](https://support.mozilla.org/ko/kb/containers))
- PWA(Progressive Web App)를 지원해야 합니다.  
  PWA를 사용하면 특정 웹사이트를 마치 네이티브 앱인 것처럼 컴퓨터에 설치할 수 있습니다. 브라우저의 정기적인 보안 업데이트 혜택을 받을 수 있으므로 Electron 기반 앱보다 유리한 점이 있습니다.
- 사용자 프라이버시에 이점을 주지 않는 애드온 기능(블로트웨어)을 포함하지 않아야 합니다.
- 원격 분석 데이터를 기본적으로 수집하지 않아야 합니다.
- 오픈 소스 동기화 서버 구현체를 제공해야 합니다.
- [비공개 검색 엔진](search-engines.md)이 기본으로 설정되어 있어야 합니다.

### 확장 프로그램 평가 기준

- 내장 브라우저 혹은 운영 체제 기능을 복제해서는 안됩니다.
- 사용자 프라이버시에 직접적인 이점을 제공해야 합니다. 단순 정보 제공은 기준 미달입니다.

[^1]: Brave의 자세한 구현 방식은 [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state/)에서 찾아볼 수 있습니다.
