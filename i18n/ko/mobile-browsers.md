---
meta_title: "Privacy Respecting Web Browsers for Android and iOS - Privacy Guides"
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

<small>Protects against the following threat(s):</small>

- [:material-account-cash: 감시 자본주의(Surveillance Capitalism)](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our currently recommended **mobile web browsers** and configurations for standard/non-anonymous internet browsing. 익명으로 인터넷을 탐색해야 하는 경우라면, [Tor](tor.md)를 사용해야 합니다.

## Brave

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
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)

</details>

</div>

### Recommended Brave Configuration

진정한 익명 인터넷 탐색이 가능한 유일한 방법은 Tor 브라우저입니다. 다음 설정들은 여러분이 Brave를 사용할 때 특정 주체로부터 프라이버시를 보호할 수 있도록 권장드리는 사항입니다. [Tor 브라우저](tor.md#tor-browser) 이외의 모든 브라우저는 어떤 식으로든 누군가는 특정 대상을 추적할 수 있음을 명심해야 합니다.

이러한 옵션은 :material-menu: → **설정** → **Brave Shields 및 프라이버시**에서 확인할 수 있습니다.

#### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

#### Brave shields global defaults

필요에 따라 사이트별로 보호 옵션을 낮출 수 있으나, 기본적으로 다음과 같이 설정할 것을 권장드립니다:

<div class="annotate" markdown>

- [x] Select **Aggressive** under **Block trackers & ads**

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. 이 기능을 사용하지 말고 기본 필터 목록을 유지할 것을 권장드립니다. 추가적인 목록을 사용하면 다른 Brave 사용자에 비해 더 눈에 띄게 되며, 만약 Brave에 취약점이 존재하고 여러분이 사용하는 규칙 목록에 악성 규칙이 포함될 경우 공격 표면을 증가시킬 수도 있습니다.

</details>

- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **strict** under **Upgrade connections to HTTPS**
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Block third-party cookies** under **Block Cookies**
- [x] Select **Block fingerprinting**
- [x] Select **Prevent fingerprinting via language settings**

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net) extension.

#### Clear browsing data

- [x] **종료 시 데이터 지우기** 활성화

#### Social Media Blocking

- [ ] 모든 소셜 미디어 항목 비활성화

#### Other privacy settings

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP handling policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [x] (Optional) Select **No protection** under **Safe Browsing** (1)
- [ ] Uncheck **Allow sites to check if you have payment methods saved**
- [ ] Uncheck **IPFS Gateway** (2)
- [x] Select **Close tabs on exit**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Automatically send daily usage ping to Brave**

</div>

1. Brave's [implementation of Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) on Android **does not** proxy [Safe Browsing network requests](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) like its desktop counterpart. This means that your IP address may be seen (and logged) by Google. Note that Safe Browsing is not available for Android devices without Google Play Services.
2. IPFS(InterPlanetary File System)는 분산 파일 시스템에서 데이터를 저장하고 공유하기 위한 탈중앙화 P2P 네트워크입니다. 해당 기능을 사용하지 않는다면 비활성화하세요.

### Leo

These options can be found in :material-menu: → **Settings** → **Leo**

- [ ] Uncheck **Show autocomplete suggestions in address bar**

### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

## Mull (Android)

<div class="admonition recommendation" markdown>

![Mull logo](assets/img/browsers/mull.svg){ align=right }

**Mull** is a privacy oriented and deblobbed Android browser based on Firefox. Compared to Firefox, it offers much greater fingerprinting protection out of the box, and disables JavaScript Just-in-Time (JIT) compilation for enhanced security. It also removes all proprietary elements from Firefox, such as replacing Google Play Services references.

[:octicons-home-16: Homepage](https://divestos.org/pages/our_apps#mull){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://divestos.org/pages/browsers#tuningFenix){ .card-link title=Documentation }
[:octicons-code-16:](https://codeberg.org/divested-mobile/mull-fenix){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-fdroid: F-Droid](https://f-droid.org/en/packages/us.spotco.fennec_dos)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Firefox (Gecko)-based browsers on Android [lack](https://bugzilla.mozilla.org/show_bug.cgi?id=1610822) [site isolation](https://wiki.mozilla.org/Project_Fission),[^1] a powerful security feature that protects against a malicious site performing a [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability))-like attack to gain access to the memory of another website you have open.[^2] Chromium-based browsers like [Brave](#brave) will provide more robust protection against malicious websites.

</div>

Enable DivestOS's [F-Droid repository](https://divestos.org/fdroid/official) to receive updates directly from the developer. Downloading Mull from the default F-Droid repo will mean your updates could be delayed by a few days or longer.

Mull enables many features upstreamed by the [Tor uplift project](https://wiki.mozilla.org/Security/Tor_Uplift) using preferences from [Arkenfox](desktop-browsers.md#arkenfox-advanced). Proprietary blobs are removed from Mozilla's code using the scripts developed for Fennec F-Droid.

### Recommended Mull Configuration

We would suggest installing [uBlock Origin](browser-extensions.md#ublock-origin) as a content blocker if you want to block trackers within Mull.

Mull comes with privacy protecting settings configured by default. You might consider configuring the **Delete browsing data on quit** options in Mull's settings if you want to close all your open tabs when quitting the app automatically, or clear other data such as browsing history and cookies automatically.

Because Mull has more advanced and strict privacy protections enabled by default compared to most browsers, some websites may not load or work properly unless you adjust those settings. You can consult this [list of known issues and workarounds](https://divestos.org/pages/broken#mull) for advice on a potential fix if you do encounter a broken site. Adjusting a setting in order to fix a website could impact your privacy/security, so make sure you fully understand any instructions you follow.

## Safari (iOS)

iOS에서는 웹 브라우징이 가능한 모든 앱이 Apple에서 제공하는 [Webkit 프레임워크](https://developer.apple.com/documentation/webkit)를 사용하도록 [강제되기 때문에](https://developer.apple.com/app-store/review/guidelines), 타사 웹 브라우저를 사용할 이유가 거의 없습니다.

<div class="admonition recommendation" markdown>

![Safari 로고](assets/img/browsers/safari.svg){ align=right }

**Safari**는 iOS 기본 브라우저입니다. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Privacy Report, isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites so more devices look identical) as well as fingerprint randomization, and Private Relay for those with a paid iCloud+ subscription. It also allows you to separate your browsing with different profiles and lock private tabs with your biometrics/PIN.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title=Documentation}

</details>

</div>

### Recommended Safari Configuration

We would suggest installing [AdGuard](browser-extensions.md#adguard) if you want a content blocker in Safari.

The following privacy/security-related options can be found in the :gear: **Settings** app → **Safari**

#### Profiles

All of your cookies, history, and website data will be separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

#### 개인 정보 및 보안

- [x] **크로스 사이트 추적 방지** 활성화

    Webkit의 [지능형 추적 방지](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp)가 활성화됩니다. 해당 기능은 온 디바이스(On-device) 머신 러닝을 이용해 추적기를 중단시켜 원치 않는 추적을 방지하는 데 도움을 줍니다. 지능형 추적 방지는 많은 일반적인 위협을 방지하지만, 웹사이트 사용성을 방지하지 않도록 설계되었기 때문에 모든 추적 경로를 차단하지는 않습니다.

- [x] Enable **Require Face ID to Unlock Private Browsing**

    This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

#### Advanced → Privacy

The **Advanced Tracking and Fingerprinting Protection** setting will randomize certain values so that it's more difficult to fingerprint you:

- [x] Select **All Browsing** or **Private Browsing**

#### 개인정보 보호 리포트

개인정보 보호 리포트는 현재 방문 중인 웹사이트에서 사용자 정보를 수집하지 못하도록 차단된 크로스 사이트 추적기 정보 요약을 제공합니다. 시간 경과에 따라 어떤 추적기가 차단됐는지 보여주는 주간 리포트를 표시할 수도 있습니다.

개인정보 보호 리포트는 페이지 설정 메뉴에서 접근할 수 있습니다.

#### 개인정보 보호 광고 측정

- [ ] **개인 정보 보호 광고 측정** 비활성화

광고 클릭 측정에는 사용자 개인정보를 침해하는 추적 기술이 사용되는 것이 일반적입니다. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

해당 기능은 프라이버시 관련 우려가 거의 없으므로 활성화해둘 수도 있으나, 개인정보 보호 브라우징에서 이 기능이 자동으로 비활성화된다는 점을 고려하여, 비활성화할 것으로 명시하였습니다.

#### 항상 개인정보 보호 브라우징

Safari를 열고 우측 하단의 탭 버튼을 탭합니다. 이후, 탭 그룹 목록을 펼칩니다.

- [x] **개인정보 보호**를 활성화합니다.

Safari 개인정보 보호 브라우징 모드는 추가적인 프라이버시 보호 기능을 제공합니다. 개인정보 보호 브라우징 모드는 각 탭마다 새로운 [임시](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) 세션을 사용하여, 탭을 서로 격리합니다. 개인정보 보호 브라우징 모드에서는 Safari 번역 기능 사용 시 웹페이지 주소가 Apple에 전송되지 않는 등, 프라이버시에 도움이 되는 여타 소소한 이점도 존재합니다.

단, 개인정보 보호 브라우징 모드는 쿠키 및 웹사이트 데이터를 저장하지 않으므로 사이트 로그인을 유지할 수 없음을 알아두어야 합니다. 이로 인해 사용이 불편할 수 있습니다.

#### iCloud 동기화

Safari 방문 기록, 탭 그룹, iCloud 탭, 저장된 암호는 E2EE 동기화됩니다. However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://apple.com/legal/privacy/en-ww).

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/HT212520). **Apple 사용자 이름 → iCloud → 고급 데이터 보호**로 이동하세요.

- [x] **고급 데이터 보호** 활성화

고급 데이터 보호가 비활성화된 iCloud를 사용하는 경우, 여러분의 기기에서 Safari 기본 다운로드 위치 설정을 확인하고 로컬로 지정할 것을 권장드립니다. 해당 옵션은 :gear: **설정** → **Safari** → **일반** → **다운로드**에서 확인할 수 있습니다.

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

### 최소 요구 사항

- 자동 업데이트를 지원해야 합니다.
- Must receive engine updates from upstream releases quickly.
- Must support content blocking.
- 브라우저의 프라이버시를 강화하는 데에 필요한 모든 변경 사항은 사용자 경험에 부정적인 영향을 미치지 않아야 합니다.
