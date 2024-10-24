---
meta_title: "프라이버시 중점 PC, Mac용 웹 브라우저 - Privacy Guides"
title: "데스크톱 브라우저"
icon: material/laptop
description: These privacy-protecting browsers are what we currently recommend for standard/non-anonymous internet browsing on desktop systems.
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

<small>Protects against the following threat(s):</small>

- [:material-account-cash: 감시 자본주의(Surveillance Capitalism)](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our currently recommended **desktop web browsers** and configurations for standard/non-anonymous browsing. 강력한 프라이버시 보호 및 핑거프린팅 방지가 기본 제공되는 브라우저를 원하신다면 [Mullvad Browser](#mullvad-browser)를, 평범한 인터넷 브라우저 중 Google Chrome의 적절한 대체제를 원하신다면 [Firefox](#firefox)를, Chromium 브라우저 호환성이 필요하시다면 [Brave](#brave)를 추천드립니다.

익명으로 인터넷을 탐색해야 하는 경우라면, [Tor](tor.md)를 사용해야 합니다. 본 내용에서 몇 가지 권장 설정을 알려드리고 있지만, Tor 브라우저를 제외한 모든 브라우저는 *누군가* 어떻게든 추적할 수 있습니다.

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** is a version of [Tor Browser](tor.md#tor-browser) with Tor network integrations removed. It aims to provide to VPN users Tor Browser's anti-fingerprinting browser technologies, which are key protections against [:material-eye-outline: Mass Surveillance](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. Tor 프로젝트에서 개발하고 [Mullvad](vpn.md#mullvad)에서 배포합니다. Mullvad VPN 사용이 필수적이지 **않습니다**.

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

[Tor 브라우저](tor.md)와 마찬가지로, Mullvad Browser는 브라우저 핑거프린트를 모든 Mullvad Browser 사용자끼리 동일하게 만들어 핑거프린팅을 방지하도록 설계되었습니다. 기본 보안 등급(*Standard*, *Safer*, *Safest*)에 따라 자동으로 설정되는 기본 설정 및 확장 프로그램을 포함하고 있습니다. 따라서 브라우저의 [보안 등급](https://tb-manual.torproject.org/security-settings) 외에 다른 설정을 변경하지 않는 것이 중요합니다. 추가적인 수정을 할 경우 고유한 핑거프린트를 갖게 됩니다. 즉 이 브라우저를 쓰는 의미가 사라집니다. 만약 핑거프린팅을 신경 쓰지 않고 자유로운 브라우저 설정을 원하실 경우, [Firefox](#firefox)를 추천드립니다.

### 핑거프린팅 방지

[VPN](vpn.md)을 사용하지 **않을** 경우, Mullvad 브라우저는 [Naive 핑거프린팅 스크립트](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting)에 대해 여타 비공개 탐색 브라우저(Firefox+[Arkenfox](#arkenfox-advanced), [Brave](#brave))와 동일한 수준의 보호 기능을 제공합니다. Mullvad 브라우저는 다른 비공개 탐색 브라우저에서 제공하는 유연성과 편의성을 일부 희생하여, 별도로 설정할 필요 없이 핑거프린트 보호 기능을 기본으로 제공합니다.

==가장 강력한 핑거프린팅 방지 보호를 원하시는 경우, **Mullvad 브라우저와 VPN을 같이 사용**하실 것을 권장합니다.==(Mullvad VPN 혹은 그 외 권장 VPN 서비스) Mullvad 브라우저와 VPN을 사용하면 핑거프린트, IP 주소 대역을 다른 많은 사용자와 공유하여 '군중' 사이에 섞일 수 있습니다. 이 전략은 고급 추적 스크립트를 막을 수 있는 유일한 방법이자, Tor 브라우저에서 사용하는 것과 동일한 핑거프린트 방지 기술이기도 합니다.

Mullvad Browser는 특정 VPN 서비스에 의존하지 않으므로 어떤 VPN이든 같이 사용할 수 있습니다. 하지만 '군중 속에 섞여드는 효과'를 얻기 위해서는 여러분과 동일한 VPN을 사용하면서 Mullvad 브라우저도 사용하는 사람들이 존재한다는 전제가 필요합니다. 특히나 Mullvad 브라우저가 출시된지 얼마 되지 않은 지금 시점에서는 다른 VPN 서비스보다 Mullvad VPN의 사용자 중에 Mullvad 브라우저를 사용하는 사람이 많을 것입니다. Mullvad 브라우저는 VPN 연결 기능을 내장하고 있지 않으며, 브라우저 이용에 앞서 VPN 사용 여부를 확인하는 기능 또한 없습니다. 사용자는 VPN 연결을 따로 설정하고 관리해야 합니다.

Mullvad 브라우저는 *uBlock Origin*, *NoScript* 브라우저 확장 프로그램이 기본 설치되어 있습니다. While we typically discourage adding *additional* [browser extensions](browser-extensions.md), these extensions that come pre-installed with the browser should **not** be removed or configured outside their default values, because doing so would noticeably make your browser fingerprint distinct from other Mullvad Browser users. 추가로, Mullvad 브라우저에는 'Mullvad Browser Extension' 확장 프로그램이 기본 설치되어 있습니다. Mullvad VPN 외 VPN 서비스를 사용하더라도 안전하게 사용할 수 있는 확장 프로그램이지만, 이 확장 프로그램을 제거하더라도 브라우저 핑거프린트에 영향을 주지 않으니 제거하고자 하는 경우 안심하고 제거해도 좋습니다.

### 사생활 보호 모드

Mullvad 브라우저는 항상 사생활 보호 모드로 작동하므로 방문 기록, 쿠키, 기타 사이트 데이터는 브라우저를 닫을 때마다 매번 지워집니다. 북마크, 브라우저 설정, 확장 프로그램 설정은 유지됩니다.

이는 고급 추적을 방지하기 위해서 필요하지만, 편의성 및 일부 Firefox 기능(멀티 컨테이너 등)을 희생합니다. 하지만 여러분은 여러 브라우저를 사용할 수 있습니다. 로그인이 유지되어야 하는 사이트나 Mullvad 브라우저에서 제대로 작동하지 않는 사이트는 Firefox+Arkenfox를 사용하고, 그 외 일반적인 브라우저 탐색에는 Mullvad 브라우저를 사용하는 방법도 있습니다.

### Mullvad Leta

Mullvad 브라우저는 DuckDuckGo가 기본 [검색 엔진](search-engines.md)으로 설정되어 있지만, Mullvad VPN 구독 시 사용 가능한 **Mullvad Leta** 검색 엔진도 기본 설치되어 있습니다. Mullvad Leta queries Google's paid search API directly, which is why it is limited to paying subscribers. However, it is possible for Mullvad to correlate search queries and Mullvad VPN accounts because of this limitation. 이러한 이유로, 저희는 Mullvad가 VPN 구독자에 대한 정보를 거의 수집하지 않는다는 점을 알고 있음에도 불구하고 Mullvad Leta 사용을 권장하지 않습니다.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox 로고](assets/img/browsers/firefox.svg){ align=right }

**Firefox**는 [다양한 추적](https://support.mozilla.org/ko/kb/enhanced-tracking-protection-firefox-desktop#w_hyangsangdoen-cujeog-bangji-gineungi-cadanhaneun-geos)을 방지하는 [향상된 추적 방지 기능](https://support.mozilla.org/ko/kb/enhanced-tracking-protection-firefox-desktop) 등 강력한 프라이버시 설정을 제공합니다.

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title=Documentation}
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Firefox includes a unique [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) in downloads from Mozilla's website and uses telemetry in Firefox to send the token. The token is **not** included in releases from the [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Recommended Firefox Configuration

이러한 옵션은 :material-menu: → **설정**에서 확인할 수 있습니다.

#### 검색

-

여러분의 지역에 따라 검색 제안 기능이 제공되지 않을 수도 있습니다.

검색 제안 기능은 실제로 검색을 누르지 않더라도 주소창에 입력하는 모든 내용을 기본 검색 엔진으로 전송합니다. 검색 제안을 비활성화하여 검색 엔진 제공 업체에 전송하는 데이터를 보다 신중하게 조절할 수 있습니다.

##### Firefox Suggest (미국 한정)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. 검색 제안 사용을 비활성화한 것과 마찬가지 이유로 해당 기능을 비활성화할 것을 권장드립니다. **주소 표시줄** 헤더에 이러한 옵션이 표시되지 않는 경우 이는 무시하셔도 좋습니다.

- [ ] Uncheck **Suggestions from Firefox**
- [ ] **스폰서에서 제안** 비활성화

#### 개인 정보 및 보안

##### 향상된 추적 방지 기능

- [x] 향상된 추적 방지 기능에서 **엄격** 활성화

소셜 미디어 추적기, 핑거프린팅 스크립트(*모든* 핑거프린팅으로부터 보호하지는 못함), 암호화폐 채굴기, 교차 사이트 추적 쿠키 및 기타 추적 콘텐츠를 차단합니다. 향상된 추적 방지 기능은 대부분의 일반적인 위협을 방지하지만, 웹사이트 사용성을 해치지 않도록 설계되었기 때문에 모든 추적 경로를 차단하지는 못합니다.

##### 종료 시 데이터 정리

특정 사이트의 로그인을 유지하려면 **쿠키 및 사이트 데이터** → **예외 관리...**에서 예외를 허용할 수 있습니다.

- [x] **Firefox를 닫을 때 쿠키와 사이트 데이터를 삭제** 활성화

이 기능은 영구적인 쿠키로부터 여러분을 보호합니다. 하지만 한 번의 브라우저 세션 중에 획득한 쿠키로부터 여러분을 보호하지는 않습니다. 이 기능을 활성화해두면 브라우저 쿠키를 정리하고자 할 때 Firefox를 재시작하기만 하면 됩니다. 사이트별 예외를 설정해 자주 이용하는 특정 사이트의 로그인을 유지할 수 있습니다.

##### 원격 분석

- [ ] **Firefox가 기술과 상호 작용 정보를 Mozilla에 전송하도록 허용** 비활성화
- [ ] **Firefox가 연구를 설치하고 실행하도록 허용** 비활성화
- [ ] **Firefox가 사용자를 대신하여 백로그된 충돌 보고서를 보내도록 허용** 비활성화

> Firefox는 사용자의 Firefox 버전 및 언어, 기기 운영 체제 및 하드웨어 구성, 메모리, 충돌 및 오류에 대한 기본 정보, 업테이트 및 세이프 브라우징 같은 자동화 프로세스의 결과, 활성화 여부 등의 데이터를 당사(Mozilla)로 전송합니다. Firefox가 당사에 데이터를 전송할 때 사용자의 IP 주소는 당사 서버 로그의 일부로 일시적으로 수집됩니다.

Additionally, the Mozilla Accounts service collects [some technical data](https://mozilla.org/privacy/mozilla-accounts). If you use a Mozilla Account you can opt-out:

1. [accounts.firefox.com 프로필 설정](https://accounts.firefox.com/settings#data-collection) 열기
2. **데이터 수집 및 사용** > **Firefox 계정 개선에 참여** 비활성화

##### Website Advertising Preferences

- [ ] Uncheck **Allow websites to perform privacy-preserving ad measurement**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.

##### HTTPS-Only Mode

- [x] **모든 창에서 HTTPS 전용 모드 사용** 활성화

의도치 않게 일반 텍스트 HTTP로 웹사이트에 연결되는 것을 방지합니다. 최근에는 대부분의 사이트가 HTTPS를 지원하므로, 일상적인 웹 탐색에는 크게 영향을 미치지 않습니다.

##### DNS over HTTPS

If you use a [DNS over HTTPS provider](dns.md):

- [x] Select **Max Protection** and choose a suitable provider

Max Protection enforces the use of DNS over HTTPS, and a security warning will show if Firefox can’t connect to your secure DNS resolver, or if your secure DNS resolver says that records for the domain you are trying to access do not exist. This stops the network you're connected to from secretly downgrading your DNS security.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (고급)

<div class="admonition tip" markdown>
<p class="admonition-title">Use Mullvad Browser for advanced anti-fingerprinting</p>

[Mullvad 브라우저](#mullvad-browser)는 Arkenfox와 동일한 핑거프린팅 방지 보호 기능을 기본으로 제공합니다(이러한 보호 기능은 Mullvad VPN을 사용하지 않더라도 그대로 누릴 수 있습니다). VPN을 함께 사용할 경우, Mullvad 브라우저는 Arkenfox가 차단하지 못하는 고급 추적 스크립트까지 차단할 수 있습니다. 단, Arkenfox는 훨씬 더 유연성 있고, 사이트별 예외를 통해 특정 웹사이트에서 로그인 유지 등이 가능하다는 장점이 있습니다.

</div>

[Arkenfox 프로젝트](https://github.com/arkenfox/user.js)는 신중하게 고려된 Firefox용 옵션 모음을 제공합니다. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly—which you can [easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. 저희는 전체 [위키](https://github.com/arkenfox/user.js/wiki) 내용을 읽어보실 것을 **강력히 권장드립니다**. Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox는 캔버스 무작위화(Randomization)와 Firefox에 기본 탑재된 핑거프린트 방지 구성 설정을 통해 기본적이거나 순진한(Naive) 추적 스크립트를 차단하는 것만 목표로 합니다. Mullvad 브라우저나 Tor 브라우저에서 사용하는 방식이자, 고급 핑거프린트 추적 스크립트를 막을 수 있는 유일한 방법인 '다른 사용자들 사이에 섞여들게 하는 것'은 Arkenfox의 목표가 아닙니다. 물론, 여러분은 여러 브라우저를 사용할 수 있습니다. 로그인이 유지되어야 하는 사이트나 믿을 만한 사이트는 Firefox+Arkenfox를 사용하고, 그 외 일반적인 브라우저 탐색에는 Mullvad 브라우저를 사용하는 방법도 있습니다.

## Brave

<div class="admonition recommendation annotate" markdown>

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

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Brave adds a "[referral code](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" to the file name in downloads from the Brave website, which is used to track which source the browser was downloaded from, for example `BRV002` in a download named `Brave-Browser-BRV002.pkg`. The installer will then ping Brave's server with the referral code at the end of the installation process. If you're concerned about this, you can rename the installer file before opening it.

</div>

### Recommended Brave Configuration

이러한 옵션은 :material-menu: → **설정**에서 확인할 수 있습니다.

#### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

필요에 따라 사이트별로 보호 옵션을 낮출 수 있으나, 기본적으로 다음과 같이 설정할 것을 권장드립니다:

<div class="annotate" markdown>

- [x] Select **Aggressive** under *Trackers & ads blocking*

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. 이 기능을 사용하지 말고 기본 필터 목록을 유지할 것을 권장드립니다. 추가적인 목록을 사용하면 다른 Brave 사용자에 비해 더 눈에 띄게 되며, 만약 Brave에 취약점이 존재하고 여러분이 사용하는 규칙 목록에 악성 규칙이 포함될 경우 공격 표면을 증가시킬 수도 있습니다.

</details>

- [x] Select **Strict** under *Upgrade connections to HTTPS*
- [x] (Optional) Select **Block Scripts** (1)
- [x] Check **Block fingerprinting**
- [x] Select **Block third-party cookies**
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option disables JavaScript, which will break a lot of sites. To unbreak them, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

#### Privacy and security

<div class="annotate" markdown>

- [x] Select **Don't allow sites to use the V8 optimizer** under *Security* → *Manage V8 security* (1)
- [x] Select **Automatically remove permissions from unused sites** under *Sites and Shields Settings*
- [x] Select **Disable non-proxied UDP** under [*WebRTC IP Handling Policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **Prevent sites from fingerprinting me based on my language preferences**

</div>

1. Disabling the V8 optimizer reduces your attack surface by disabling [*some*](https://grapheneos.social/@GrapheneOS/112708049232710156) parts of JavaScript Just-In-Time (JIT) compilation.

<div class="admonition tip" markdown>
<p class="admonition-title">Sanitizing on close</p>

- [x] Select **Delete data sites have saved to your device when you close all windows** under *Sites and Shields Settings* → *Content* → *Additional content settings* → *On-device site data*.

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

##### Tor windows

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) allows you to route your traffic through the Tor network in Private Windows and access .onion services, which may be useful in some cases. However, Brave is **not** as resistant to fingerprinting as the Tor Browser and far fewer people use Brave with Tor, so you will stand out. If your threat model requires strong anonymity, use the [Tor Browser](tor.md#tor-browser).

##### Data Collection

- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**

#### Web3

Brave의 Web3 기능은 잠재적으로 브라우저의 핑거프린트와 공격 표면을 증가시킬 수 있습니다. Unless you use any of these features, they should be disabled.

- Select **Extensions (no fallback)** under *Default Ethereum wallet*
- Select **Extensions (no fallback)** under *Default Solana wallet*

#### Extensions

- [ ] Uncheck all built-in extensions you don't use

#### System

<div class="annotate" markdown>

- [ ] **Brave 종료 후에도 백그라운드 앱을 계속 실행** 비활성화 (1)

</div>

1. 플랫폼에 따라 해당 옵션이 제공되지 않을 수 있습니다.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. 해당 기능은 일부 선정된 제공 업체의 수탁형 계정과 KYC(고객 신원 확인)에 기반하여 동작합니다. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Brave 월렛**은 사용자 컴퓨터 로컬에서 작동하지만, 프라이버시 암호화폐를 지원하지 않으므로 이 또한 사용을 권장하지 않습니다.

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
- Should support Progressive Web Apps. PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps, because PWAs benefit from your browser's regular security updates.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Should not collect telemetry by default.
- Should provide an open-source sync server implementation.
- Should default to a [private search engine](search-engines.md).

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
