---
meta_title: "프라이버시 중점 모바일(Android, iOS) 웹 브라우저 - Privacy Guides"
title: "모바일 브라우저"
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

본 내용은 현재 표준/비익명 인터넷 탐색 용도로 권장되는 모바일 웹 브라우저 및 관련 설정 목록입니다. 익명으로 인터넷을 탐색해야 하는 경우라면, [Tor](tor.md)를 사용해야 합니다. 일반적으로 Privacy Guides는 여러분에게 '브라우저 확장 프로그램은 최소한으로만 설치할 것'을 권장드립니다. 브라우저 확장 프로그램은 여러분의 브라우저에 대해서 막대한 접근 권한을 가지며, 확장 프로그램 개발자를 신뢰해야 할 필요성을 발생시키고, 여러분을 보다 [눈에 띄게](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint) 만들고, 사이트 격리를 [약화시킵니다](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ).

## Android

On Android, Firefox is still less secure than Chromium-based alternatives: Mozilla's engine, [GeckoView](https://mozilla.github.io/geckoview), has yet to support [site isolation](https://hacks.mozilla.org/2021/05/introducing-firefox-new-site-isolation-security-architecture) or enable [isolatedProcess](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196).

### Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brace는 Chromium 웹 브라우저 프로젝트 기반으로 구축되었으므로, 친숙하며 웹사이트 호환성 문제가 적습니다.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

#### 권장 설정

진정한 익명 인터넷 탐색이 가능한 유일한 방법은 Tor 브라우저입니다. 다음 설정들은 여러분이 Brave를 사용할 때 특정 주체로부터 프라이버시를 보호할 수 있도록 권장드리는 사항입니다. [Tor 브라우저](tor.md#tor-browser) 이외의 모든 브라우저는 어떤 식으로든 누군가는 특정 대상을 추적할 수 있음을 명심해야 합니다.

이러한 옵션은 :material-menu: → **설정** → **Brave Shields 및 프라이버시**에서 확인할 수 있습니다.

##### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

##### Brave Shields 전역 기본값

필요에 따라 사이트별로 보호 옵션을 낮출 수 있으나, 기본적으로 다음과 같이 설정할 것을 권장드립니다:

<div class="annotate" markdown>

- [x] Select **Aggressive** under **Block trackers & ads**

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. 이 기능을 사용하지 말고 기본 필터 목록을 유지할 것을 권장드립니다. 추가적인 목록을 사용하면 다른 Brave 사용자에 비해 더 눈에 띄게 되며, 만약 Brave에 취약점이 존재하고 여러분이 사용하는 규칙 목록에 악성 규칙이 포함될 경우 공격 표면을 증가시킬 수도 있습니다.

</details>

- [x] **연결을 HTTPS로 업그레이드** 활성화
- [x] **항상 보안 연결 사용** 활성화
- [x] (선택 사항) **스크립트 차단** 활성화 (1)
- [x] **지문 차단**을 **엄격, 사이트가 작동하지 않을 수 있음**으로 설정

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net) extension.

##### 인터넷 사용 기록 삭제

- [x] **종료 시 데이터 지우기** 활성화

##### 소셜 미디어 차단

- [ ] 모든 소셜 미디어 항목 비활성화

##### 기타 프라이버시 설정

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP handling policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Allow sites to check if you have payment methods saved**
- [ ] Uncheck **IPFS Gateway** (1)
- [x] Select **Close tabs on exit**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Automatically send daily usage ping to Brave**

</div>

1. IPFS(InterPlanetary File System)는 분산 파일 시스템에서 데이터를 저장하고 공유하기 위한 탈중앙화 P2P 네트워크입니다. 해당 기능을 사용하지 않는다면 비활성화하세요.

#### Brave 동기화

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

## iOS

iOS에서는 웹 브라우징이 가능한 모든 앱이 Apple에서 제공하는 [Webkit 프레임워크](https://developer.apple.com/documentation/webkit)를 사용하도록 [강제되기 때문에](https://developer.apple.com/app-store/review/guidelines), 타사 웹 브라우저를 사용할 이유가 거의 없습니다.

### Safari

<div class="admonition recommendation" markdown>

![Safari 로고](assets/img/browsers/safari.svg){ align=right }

**Safari**는 iOS 기본 브라우저입니다. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Privacy Report, isolated and ephemeral Private Browsing tabs, iCloud Private Relay, fingerprinting protection by randomizing and presenting a simplified version of the system configuration to websites so more devices look identical, and the ability to lock private tabs with your biometrics/PIN. It also allows you to separate your browsing with different profiles.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentation}

</details>

</div>

#### 권장 설정

These options can be found in :gear: **Settings** → **Safari**

##### Profiles

All of your cookies, history, and website data will be separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

##### 개인 정보 및 보안

- [x] **크로스 사이트 추적 방지** 활성화

    Webkit의 [지능형 추적 방지](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp)가 활성화됩니다. 해당 기능은 온 디바이스(On-device) 머신 러닝을 이용해 추적기를 중단시켜 원치 않는 추적을 방지하는 데 도움을 줍니다. 지능형 추적 방지는 많은 일반적인 위협을 방지하지만, 웹사이트 사용성을 방지하지 않도록 설계되었기 때문에 모든 추적 경로를 차단하지는 않습니다.

- [x] Enable **Require Face ID to Unlock Private Browsing**

    This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

##### Advanced → Privacy

The **Advanced Tracking and Fingerprinting Protection** setting will randomize certain values so that it's more difficult to fingerprint you:

- [x] Select **All Browsing** or **Private Browsing**

##### 개인정보 보호 리포트

개인정보 보호 리포트는 현재 방문 중인 웹사이트에서 사용자 정보를 수집하지 못하도록 차단된 크로스 사이트 추적기 정보 요약을 제공합니다. 시간 경과에 따라 어떤 추적기가 차단됐는지 보여주는 주간 리포트를 표시할 수도 있습니다.

개인정보 보호 리포트는 페이지 설정 메뉴에서 접근할 수 있습니다.

##### 개인정보 보호 광고 측정

- [ ] **개인 정보 보호 광고 측정** 비활성화

광고 클릭 측정에는 사용자 개인정보를 침해하는 추적 기술이 사용되는 것이 일반적입니다. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

해당 기능은 프라이버시 관련 우려가 거의 없으므로 활성화해둘 수도 있으나, 개인정보 보호 브라우징에서 이 기능이 자동으로 비활성화된다는 점을 고려하여, 비활성화할 것으로 명시하였습니다.

##### 항상 개인정보 보호 브라우징

Safari를 열고 우측 하단의 탭 버튼을 탭합니다. 이후, 탭 그룹 목록을 펼칩니다.

- [x] **개인정보 보호**를 활성화합니다.

Safari 개인정보 보호 브라우징 모드는 추가적인 프라이버시 보호 기능을 제공합니다. 개인정보 보호 브라우징 모드는 각 탭마다 새로운 [임시](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) 세션을 사용하여, 탭을 서로 격리합니다. 개인정보 보호 브라우징 모드에서는 Safari 번역 기능 사용 시 웹페이지 주소가 Apple에 전송되지 않는 등, 프라이버시에 도움이 되는 여타 소소한 이점도 존재합니다.

단, 개인정보 보호 브라우징 모드는 쿠키 및 웹사이트 데이터를 저장하지 않으므로 사이트 로그인을 유지할 수 없음을 알아두어야 합니다. 이로 인해 사용이 불편할 수 있습니다.

##### iCloud 동기화

Safari 방문 기록, 탭 그룹, iCloud 탭, 저장된 암호는 E2EE 동기화됩니다. However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://apple.com/legal/privacy/en-ww).

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/HT212520). **Apple 사용자 이름 → iCloud → 고급 데이터 보호**로 이동하세요.

- [x] **고급 데이터 보호** 활성화

고급 데이터 보호가 비활성화된 iCloud를 사용하는 경우, 여러분의 기기에서 Safari 기본 다운로드 위치 설정을 확인하고 로컬로 지정할 것을 권장드립니다. 해당 옵션은 :gear: **설정** → **Safari** → **일반** → **다운로드**에서 확인할 수 있습니다.

### AdGuard

<div class="admonition recommendation" markdown>

![AdGuard 로고](assets/img/browsers/adguard.svg){ align=right }

**iOS용 AdGuard**는 Safari용 무료 오픈 소스 콘텐츠 차단 확장 프로그램입니다. Safari [Content Blocker API](https://developer.apple.com/documentation/safariservices/creating_a_content_blocker)를 사용합니다.

iOS용 AdGuard에는 몇 가지 프리미엄 기능이 있지만, 표준 Safari 콘텐츠 차단 기능은 무료입니다.

[:octicons-home-16: Homepage](https://adguard.com/en/adguard-ios/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/ios.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1047223162)

</details>

</div>

필터 목록을 추가하면 속도가 느려지고 공격 표면을 증가시킬 수 있으므로, 필요한 것만 적용하시기 바랍니다.

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

</div>

### 최소 요구 사항

- 자동 업데이트를 지원해야 합니다.
- 업스트림 릴리스 0~1일 이내에 엔진 업데이트를 받아야 합니다.
- 브라우저의 프라이버시를 강화하는 데에 필요한 모든 변경 사항은 사용자 경험에 부정적인 영향을 미치지 않아야 합니다.
- Android 브라우저는 Chromium 엔진을 사용해야 합니다.
    - 안타깝게도 Android에서 Mozilla GeckoView는 Chromium보다 보안이 뒤떨어집니다.
    - iOS 브라우저는 Webkit으로 한정됩니다.

### 확장 프로그램 평가 기준

- 내장 브라우저 혹은 운영 체제 기능을 복제해서는 안됩니다.
- 사용자 프라이버시에 직접적인 이점을 제공해야 합니다. 단순 정보 제공은 기준 미달입니다.
