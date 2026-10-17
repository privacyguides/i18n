---
meta_title: "안드로이드 및 iOS용 프라이버시 존중 웹 브라우저 - 프라이버시 가이드"
title: 모바일 브라우저
icon: material/cellphone-information
description: 현재 휴대폰에서 표준/비익명 인터넷 탐색 용도로 권장되는 브라우저 목록입니다.
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: 비공개 탐색 모바일 브라우저 권장 목록
    url: "./"
    relatedLink: "../desktop-browsers/"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    applicationCategory: Web Browser
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://apple.com/safari
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-account-cash: 감시 자본주의(Surveillance Capitalism)](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

표준/비익명 인터넷 탐색용으로 현재 권장하는 **모바일 웹 브라우저** 및 설정입니다. 익명으로 인터넷을 탐색해야 하는 경우라면, [토르](tor.md)를 사용해야 합니다.

## 브레이브

<div class="admonition recommendation" markdown>

![브레이브 로고](assets/img/browsers/brave.svg){ align=right }

**브레이브 브라우저**에는 내장 콘텐츠 차단기와 [개인정보 보호 기능](https://brave.com/privacy-features)이 포함되어 있으며, 이들 중 상당수는 기본적으로 활성화되어 있습니다.

브레이브는 크로미움 웹 브라우저 프로젝트 기반으로 구축되었으므로, 친숙하며 웹사이트 호환성 문제가 적습니다.

[:octicons-home-16: 홈페이지](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="어니언 서비스" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id1052879175)
- [:simple-github: 깃허브](https://github.com/brave/brave-browser/releases)
- [:simple-fdroid: F-Droid](https://brave-browser-apk-release.s3.brave.com/fdroid/repo/index.html)

</details>

</div>

### 권장되는 브레이브 설정

진정한 익명 인터넷 탐색이 가능한 유일한 방법은 토르 브라우저입니다. 다음 설정들은 여러분이 브레이브를 사용할 때 특정 주체로부터 프라이버시를 보호할 수 있도록 권장드리는 사항입니다. 다만 [토르 브라우저](tor.md#tor-browser) 이외의 모든 브라우저는 어떤 식으로든 *누군가*에게 추적될 수 있다는 점을 명심해야 합니다.

=== "안드로이드"

    이 옵션은 :material-dots-vertical: → **설정** → **브레이브 쉴드 및 개인정보 보호**에서 찾을 수 있습니다.

=== "iOS"

    이 옵션은 :material-dots-horizontal: → **모든 설정** → **쉴드 및 개인정보 보호**에서 찾을 수 있습니다.

#### 브레이브 쉴드 전역 기본값

브레이브는 [‘쉴드’](https://support.brave.com/hc/articles/360022973471-What-is-Shields) 기능에 몇 가지 지문 추적 방지 조치를 포함하고 있습니다. 방문하는 모든 페이지에 대해 이러한 옵션을 [전체적으로](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) 설정하는 것을 권장합니다.

필요에 따라 사이트별로 보호 옵션을 낮출 수 있으나, 기본적으로 다음과 같이 설정할 것을 권장드립니다:

=== "안드로이드"

    <div class="annotate" markdown>

    - [x] *추적기 및 광고 차단*에서 **‘공격적’** 선택
    - [x] **‘AMP 페이지 자동 리디렉션’** 선택
    - [x] **‘추적 URL 자동 리디렉션’** 선택
    - [x] *HTTPS로 연결 업그레이드*에서 **‘모든 연결에 HTTPS 사용 필수(엄격)’** 선택
    - \[x\] (선택 사항) **‘스크립트 차단’** 선택 (1)
    - [x] *쿠키 차단*에서 **‘타사 쿠키 차단’** 선택
    - [x] **‘핑거프린팅 차단’** 선택
    - [x] **‘언어 설정을 통한 핑거프린팅 방지’** 선택

    <details class="warning" markdown>
    <summary>기본 필터 목록 사용</summary>

    브레이브에서는 **콘텐츠 필터링** 메뉴나 내부 페이지인 `brave://adblock`에서 추가 콘텐츠 필터를 선택할 수 있습니다. 이 기능을 사용하지 말고 기본 필터 목록을 유지할 것을 권장드립니다. 추가적인 목록을 사용하면 다른 브레이브 사용자에 비해 더 눈에 띄게 되며, 만약 브레이브에 취약점이 존재하고 여러분이 사용하는 규칙 목록에 악성 규칙이 포함될 경우 공격 표면을 증가시킬 수도 있습니다.

    </details>

    - [x] *자동 파쇄*에서 **‘사이트 탭이 닫힐 때’** 선택

    </div>

    1. 이 옵션을 선택하면 자바스크립트가 비활성화되어 많은 웹사이트가 제대로 작동하지 않게 됩니다. 사이트가 제대로 작동하지 않으면, 주소 표시줄의 쉴드 아이콘을 탭한 다음 *고급 제어*에서 이 설정을 해제하여 사이트별로 예외를 설정할 수 있습니다.

=== "iOS"

    <div class="annotate" markdown>

    - [x] *추적기 및 광고 차단*에서 **‘공격적’** 선택
    - [x] *HTTPS로 연결 업그레이드*에서 **‘엄격’** 선택
    - [x] **‘AMP 페이지 자동 리디렉션’** 선택
    - [x] **‘추적 URL 자동 리디렉션’** 선택
    - \[x\] (선택 사항) **‘스크립트 차단’** 선택 (1)
    - [x] **‘핑거프린팅 차단’** 선택
    - [x] *자동 파쇄*에서 **‘사이트 탭이 닫힐 때’** 선택

    <details class="warning" markdown>
    <summary>기본 필터 목록 사용</summary>

    브레이브에서는 **콘텐츠 필터링** 메뉴에서 추가 콘텐츠 필터를 선택할 수 있습니다. 이 기능을 사용하지 말고 기본 필터 목록을 유지할 것을 권장드립니다. 추가적인 목록을 사용하면 다른 브레이브 사용자에 비해 더 눈에 띄게 되며, 만약 브레이브에 취약점이 존재하고 여러분이 사용하는 규칙 목록에 악성 규칙이 포함될 경우 공격 표면을 증가시킬 수도 있습니다.

    </details>

    </div>

    1. 이 옵션을 선택하면 자바스크립트가 비활성화되어 많은 웹사이트가 제대로 작동하지 않게 됩니다. 사이트가 제대로 작동하지 않으면, 주소 표시줄의 쉴드 아이콘을 탭한 다음 *고급 제어*에서 이 설정을 해제하여 사이트별로 예외를 설정할 수 있습니다.

#### 기타 개인정보 보호 설정

=== "안드로이드"

    <div class="annotate" markdown>

    - \[x\] (선택 사항) *세이프 브라우징*에서 **‘보호 안 함’** 선택 (1)
    - [x] [*WebRTC IP 처리 정책*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)에서 **‘프록시되지 않은 UDP 비활성화’** 선택
    - [ ] **‘사이트에서 저장된 결제 수단이 있는지 확인하도록 허용’** 선택 해제
    - [x] **‘브레이브의 V8 엔진으로 사이트 속도를 높이지 않는 대신 공격에 대한 저항력을 약간 높이기’** 선택
    - [x] **‘종료 시 탭 닫기’** 선택
    - [ ] **‘개인정보 보호형 제품 분석(P3A) 허용’** 선택 해제
    - [ ] **‘진단 보고서 자동 전송’** 선택 해제
    - [ ] **‘브레이브에 매일 사용량 핑을 자동으로 전송’** 선택 해제

    </div>

    1. 안드로이드용 브레이브의 [세이프 브라우징 구현](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave)은 데스크톱 버전과 달리 [세이프 브라우징 네트워크 요청](https://developers.google.com/safe-browsing/v4/update-api#checking-urls)을 프록시하지 **않습니다**. 즉, 구글이 여러분의 IP 주소를 볼 수 (그리고 기록할 수) 있습니다. 참고로, 구글 플레이 서비스가 없는 안드로이드 기기에서는 세이프 브라우징을 사용할 수 없습니다.

=== "iOS"

    - [ ] **‘개인정보 보호형 제품 분석(P3A) 허용’** 선택 해제
    - [ ] **‘브레이브에 매일 사용량 핑을 자동으로 전송’** 선택 해제

#### 레오 AI

=== "안드로이드"

    이 옵션은 :material-dots-vertical: → **설정** → **레오 AI**에서 찾을 수 있습니다.

    - [ ] **‘주소 표시줄에 자동 완성 제안 표시’** 선택 해제

=== "iOS"

    이 옵션은 :material-dots-horizontal: → **모든 설정** → **레오 AI**에서 찾을 수 있습니다.

    - [ ] **‘빠른 검색 엔진 바에 표시’** 선택 해제

#### 검색 엔진

=== "안드로이드"

    이 옵션은 :material-dots-vertical: → **설정** → **검색 엔진**에서 찾을 수 있습니다.

    - [ ] **‘검색 제안 표시’** 선택 해제

=== "iOS"

    이 옵션은 :material-dots-horizontal: → **모든 설정** → **검색 엔진**에서 찾을 수 있습니다.

    - [ ] **‘빠른 검색 엔진 바에 표시’** 선택 해제

#### 브레이브 싱크

[브레이브 싱크를](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) 사용하면 계정 없이도 모든 기기에서 검색 데이터(검색 기록, 북마크 등)에 액세스할 수 있으며, 종단 간 암호화 (E2EE) 로 데이터를 보호합니다.

## 사파리 (iOS)

iOS에서는 웹을 탐색할 수 있는 모든 앱이 애플이 제공하는 [웹킷 프레임워크](https://developer.apple.com/documentation/webkit)만 사용하도록 [제한](https://developer.apple.com/app-store/review/guidelines)되어 있습니다. 따라서 [브레이브](#brave) 같은 브라우저도 다른 운영 체제에서와 달리 블링크 엔진(크로미움의 핵심 구성 요소)을 사용하지 않습니다.

<div class="admonition recommendation" markdown>

![사파리 로고](assets/img/browsers/safari.svg){ align=right }

**사파리**는 iOS 기본 브라우저입니다. [지능형 추적 방지](https://webkit.org/blog/7675/intelligent-tracking-prevention), 서로 격리된 임시 개인정보 보호 브라우징 탭, 핑거프린팅 방지(웹사이트에 단순화된 시스템 구성 정보를 제공해 더 많은 기기가 동일하게 보이도록 함), 핑거프린트 무작위화 같은 [개인정보 보호 기능](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios)을 갖추고 있으며, 유료 아이클라우드+ 구독자에게는 비공개 릴레이도 제공합니다.

[:octicons-home-16: 홈페이지](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title="문서" }

</details>

</div>

### 권장되는 사파리 설정

다음 개인정보 보호/보안 관련 옵션은 :gear: **설정** → **앱** → **사파리**에서 찾을 수 있습니다.

#### 사파리 접근 허용

**시리**에서:

- [ ] **이 앱에서 학습** 비활성화
- [ ] **앱에서 보기** 비활성화
- [ ] **홈 화면에서 보기** 비활성화
- [ ] **앱 제안** 비활성화

이렇게 하면 시리가 시리 제안에 사파리의 콘텐츠를 사용하지 못하게 됩니다.

#### 검색

- [ ] **검색 엔진 제안** 비활성화

이 설정은 주소 표시줄에 입력하는 모든 내용을 사파리에 설정된 검색 엔진으로 전송합니다. 검색어 제안 기능을 비활성화하면 검색 엔진 제공업체에 어떤 데이터를 전송할지 더 세밀하게 제어할 수 있습니다.

#### 프로필

사파리에서는 서로 다른 프로필로 탐색 활동을 분리할 수 있습니다. 쿠키, 방문 기록, 웹사이트 데이터는 모두 프로필별로 분리됩니다. 쇼핑, 업무, 학교 등 목적에 따라 서로 다른 프로필을 사용하는 것이 좋습니다.

#### 개인 정보 및 보안

- [x] **크로스 사이트 추적 방지** 활성화

이 설정은 웹킷의 [지능형 추적 방지](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp) 기능을 활성화합니다. 이 기능은 기기 내 머신 러닝으로 추적기를 막아 원치 않는 추적으로부터 보호하는 데 도움을 줍니다. ITP는 여러 일반적인 위협으로부터 보호하지만, 웹사이트 사용성을 방해하지 않도록 설계되었기 때문에 모든 추적 경로를 차단하지는 않습니다.

- [x] **개인정보 보호 브라우징을 잠금 해제하려면 Face ID/Touch ID 필요** 활성화

이 설정을 사용하면 사용하지 않을 때 개인정보 보호 탭을 생체 인증/PIN으로 잠글 수 있습니다.

- [ ] **사기성 웹 사이트 경고** 비활성화

이 설정은 탐색 중 사용자를 보호하기 위해 구글 세이프 브라우징(중국 본토 또는 홍콩 사용자의 경우 텐센트 세이프 브라우징)을 사용합니다. 따라서 세이프 브라우징 제공업체가 여러분의 IP 주소를 기록할 수 있습니다. 이 설정을 끄면 이러한 기록은 남지 않지만, 알려진 피싱 사이트에 더 취약해질 수 있습니다.

- [x] **안전하지 않은 연결 경고** 활성화

이 설정은 웹사이트 연결에 HTTPS가 사용되지 않을 경우 경고 화면을 표시합니다. 사파리는 자동으로 사이트를 HTTPS로 업그레이드하려고 시도하므로, 이 경고는 HTTPS 연결을 사용할 수 없을 때만 표시됩니다.

- [ ] **하이라이트** 비활성화

애플의 사파리 개인정보 처리방침에는 다음과 같이 명시되어 있습니다:

> 웹페이지를 방문할 때, 사파리는 관련 하이라이트를 사용할 수 있는지 확인하기 위해 웹페이지 주소를 바탕으로 계산된 정보를 OHTTP를 통해 애플에 전송할 수 있습니다.

#### 웹 사이트 설정

**카메라**에서

- [x] **묻기** 선택

**마이크**에서

- [x] **묻기** 선택

**위치**에서

- [x] **묻기** 선택

이 설정을 사용하면 웹사이트는 여러분이 명시적으로 접근 권한을 허용한 후에만 카메라, 마이크, 위치에 접근할 수 있습니다.

#### 기타 개인정보 보호 설정

이 옵션은 :gear: **설정** → **앱** → **사파리** → **고급**에서 찾을 수 있습니다.

##### 핑거프린팅 완화

**고급 추적 및 핑거프린팅 보호** 설정은 특정 값을 무작위화하여 핑거프린팅을 더 어렵게 만듭니다:

- [x] **모든 브라우징** 또는 **개인정보 보호 브라우징** 선택

##### 개인정보 보호 광고 측정

- [ ] **개인 정보 보호 광고 측정** 비활성화

광고 클릭 측정에는 사용자 개인정보를 침해하는 추적 기술이 사용되는 것이 일반적입니다. [비공개 클릭 측정](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm)은 사용자 프라이버시를 침해하지 않으면서 광고주가 웹 캠페인의 효과를 측정할 수 있도록 하는 것을 목표로 하는 웹킷 기능이자 웹 표준 제안입니다.

해당 기능은 프라이버시 관련 우려가 거의 없으므로 활성화해둘 수도 있으나, 개인정보 보호 브라우징에서 이 기능이 자동으로 비활성화된다는 점을 고려하여, 비활성화할 것으로 명시하였습니다.

#### 항상 개인정보 보호 브라우징

사파리를 열고 우측 하단의 탭 버튼을 탭합니다. 그런 다음 :material-format-list-bulleted: 탭 그룹 목록을 펼칩니다.

- [x] **개인정보 보호**를 활성화합니다.

사파리 개인정보 보호 브라우징 모드는 추가적인 프라이버시 보호 기능을 제공합니다. 개인정보 보호 브라우징 모드는 각 탭마다 새로운 [임시](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) 세션을 사용하여, 탭을 서로 격리합니다. 개인정보 보호 브라우징에는 사파리의 번역 기능을 사용할 때 웹페이지 주소를 애플에 전송하지 않는 등, 그 밖의 소소한 프라이버시 이점도 있습니다.

개인정보 보호 브라우징은 쿠키와 웹사이트 데이터를 저장하지 않으므로, 사이트에 로그인 상태를 유지할 수 없다는 점에 유의하세요. 이로 인해 사용이 불편할 수 있습니다.

#### 아이클라우드 동기화

사파리 방문 기록, 탭 그룹, 아이클라우드 탭, 저장된 암호는 E2EE 동기화됩니다. 하지만 기본적으로 북마크는 E2EE가 [적용되지 않습니다](https://support.apple.com/HT202303). 애플은 자사의 [개인정보 처리방침](https://apple.com/legal/privacy/en-ww)에 따라 북마크를 복호화하고 접근할 수 있습니다.

[고급 데이터 보호](https://support.apple.com/HT212520)를 활성화하면 사파리 북마크와 다운로드에도 E2EE를 적용할 수 있습니다. :gear: **설정** → **아이클라우드** → **고급 데이터 보호**로 이동합니다.

- [x] **고급 데이터 보호** 켜기

고급 데이터 보호를 끈 상태로 아이클라우드를 사용한다면, 사파리의 기본 다운로드 위치를 기기의 로컬 폴더로 설정하는 것도 권장합니다. 이 옵션은 :gear: **설정** → **앱** → **사파리** → **일반** → **다운로드**에서 찾을 수 있습니다.

## 평가 기준

**프라이버시 가이드는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

### 최소 요구 사항

- 자동 업데이트를 지원해야 합니다.
- 업스트림 릴리스의 엔진 업데이트를 신속하게 반영해야 합니다.
- 콘텐츠 차단을 지원해야 합니다.
- 브라우저의 프라이버시를 강화하는 데에 필요한 모든 변경 사항은 사용자 경험에 부정적인 영향을 미치지 않아야 합니다.
