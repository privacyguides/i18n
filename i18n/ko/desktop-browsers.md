---
meta_title: "프라이버시 중점 PC, Mac용 웹 브라우저 - Privacy Guides"
title: "데스크톱 브라우저"
icon: material/laptop
description: Google Chrome보다 강력한 프라이버시 보호 기능을 제공하는 브라우저 목록입니다.
cover: desktop-browsers.png
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

[Tor 브라우저](tor.md)와 마찬가지로, Mullvad Browser는 브라우저 핑거프린트를 모든 Mullvad Browser 사용자끼리 동일하게 만들어 핑거프린팅을 방지하도록 설계되었습니다. 기본 보안 단계(*Standard*, *Safer*, *Safest*)에 따라 자동으로 설정되는 기본 설정 및 확장 프로그램을 포함하고 있습니다. Therefore, it is imperative that you do not modify the browser at all outside adjusting the default [security levels](https://tb-manual.torproject.org/security-settings/). Other modifications would make your fingerprint unique, defeating the purpose of using this browser. If you want to configure your browser more heavily and fingerprinting is not a concern for you, we recommend [Firefox](#firefox) instead.

### Anti-Fingerprinting

**Without** using a [VPN](vpn.md), Mullvad Browser provides the same protections against [naive fingerprinting scripts](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) as other private browsers like Firefox+[Arkenfox](#arkenfox-advanced) or [Brave](#brave). Mullvad Browser provides these protections out of the box, at the expense of some flexibility and convenience that other private browsers can provide.

==For the strongest anti-fingerprinting protection, we recommend using Mullvad Browser in conjunction **with** a VPN==, whether that is Mullvad or another recommended VPN provider. When using a VPN with Mullvad Browser, you will share a fingerprint and a pool of IP addresses with many other users, giving you a "crowd" to blend in with. This strategy is the only way to thwart advanced tracking scripts, and is the same anti-fingerprinting technique used by Tor Browser.

Note that while you can use Mullvad Browser with any VPN provider, other people on that VPN must also be using Mullvad Browser for this "crowd" to exist, something which is more likely on Mullvad VPN compared to other providers, particularly this close to the launch of Mullvad Browser. Mullvad Browser does not have built-in VPN connectivity, nor does it check whether you are using a VPN before browsing; your VPN connection has to be configured and managed separately.

Mullvad Browser comes with the *uBlock Origin* and *NoScript* browser extensions pre-installed. While we typically [don't recommend](#extensions) adding *additional* browser extensions, these extensions that come pre-installed with the browser should **not** be removed or configured outside their default values, because doing so would noticeably make your browser fingerprint distinct from other Mullvad Browser users. It also comes pre-installed with the Mullvad Browser Extension, which *can* be safely removed without impacting your browser fingerprint if you would like, but is also safe to keep even if you don't use Mullvad VPN.

### Private Browsing Mode

Mullvad Browser operates in permanent private browsing mode, meaning your history, cookies, and other site data will always be cleared every time the browser is closed. Your bookmarks, browser settings, and extension settings will still be preserved.

This is required to prevent advanced forms of tracking, but does come at the cost of convenience and some Firefox features, such as Multi-Account Containers. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise don't work properly in Mullvad Browser, and Mullvad Browser for general browsing.

### Mullvad Leta

Mullvad Browser comes with DuckDuckGo set as the default [search engine](search-engines.md), but it also comes preinstalled with **Mullvad Leta**, a search engine which requires an active Mullvad VPN subscription to access. Mullvad Leta queries Google's paid search API directly (which is why it is limited to paying subscribers), however because of this limitation it is possible for Mullvad to correlate search queries and Mullvad VPN accounts. For this reason we discourage the use of Mullvad Leta, even though Mullvad collects very little information about their VPN subscribers.

## Firefox

!!! recommendation

    ![Firefox logo](assets/img/browsers/firefox.svg){ align=right }
    
    **Firefox** provides strong privacy settings such as [Enhanced Tracking Protection](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), which can help block various [types of tracking](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).
    
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

!!! warning
    Firefox includes a unique [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) in downloads from Mozilla's website and uses telemetry in Firefox to send the token. The token is **not** included in releases from the [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

### 권장 설정

이러한 옵션은 :material-menu: → **설정**에서 확인할 수 있습니다

#### 검색

- [ ] **검색 제안 사용** 비활성화

여러분의 지역에 따라 검색 제안 기능이 제공되지 않을 수도 있습니다.

검색 제안 기능은 실제로 검색을 누르지 않더라도 주소창에 입력하는 모든 내용을 기본 검색 엔진으로 전송합니다. 검색 제안을 비활성화하여 검색 엔진 제공 업체에 전송하는 데이터를 보다 신중하게 조절할 수 있습니다.

#### 개인 정보 및 보안

##### 향상된 추적 방지 기능

- [x] 향상된 추적 방지 기능에서 **엄격** 활성화

This protects you by blocking social media trackers, fingerprinting scripts (note that this does not protect you from *all* fingerprinting), cryptominers, cross-site tracking cookies, and some other tracking content. ETP protects against many common threats, but it does not block all tracking avenues because it is designed to have minimal to no impact on site usability.

##### Firefox Suggest (US only)

[Firefox Suggest](https://support.mozilla.org/en-US/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. 검색 제안 사용을 비활성화한 것과 마찬가지 이유로 해당 기능을 비활성화할 것을 권장드립니다. If you don't see these options under the **Address Bar** header, you do not have the new experience and can ignore these changes.

- [ ] Uncheck **Suggestions from the web**
- [ ] Uncheck **Suggestions from sponsors**

##### 종료 시 데이터 정리

특정 사이트의 로그인을 유지하려면 **쿠키 및 사이트 데이터** → **예외 관리...**에서 예외를 허용할 수 있습니다.

- [x] **Firefox를 닫을 때 쿠키와 사이트 데이터를 삭제** 활성화

This protects you from persistent cookies, but does not protect you against cookies acquired during any one browsing session. When this is enabled, it becomes possible to easily cleanse your browser cookies by simply restarting Firefox. You can set exceptions on a per-site basis, if you wish to stay logged in to a particular site you visit often.

##### 원격 분석

- [ ] **Firefox가 기술과 상호 작용 정보를 Mozilla에 전송하도록 허용** 비활성화
- [ ] **Firefox가 연구를 설치하고 실행하도록 허용** 비활성화
- [ ] **Firefox가 사용자를 대신하여 백로그된 충돌 보고서를 보내도록 허용** 비활성화

> Firefox sends data about your Firefox version and language; device operating system and hardware configuration; memory, basic information about crashes and errors; outcome of automated processes like updates, safebrowsing, and activation to us. When Firefox sends data to us, your IP address is temporarily collected as part of our server logs.

또한 Firefox 계정 서비스는 [일부 기술 데이터](https://www.mozilla.org/en-US/privacy/firefox/#firefox-accounts)를 수집합니다. Firefox 계정을 이용하는 경우 이를 거부할 수 있습니다.

1. [accounts.firefox.com 프로필 설정](https://accounts.firefox.com/settings#data-collection) 열기
2. **데이터 수집 및 사용** > **Firefox 계정 개선에 참여** 비활성화

##### HTTPS 전용 모드

- [x] **모든 창에서 HTTPS 전용 모드 사용** 활성화

의도치 않게 일반 텍스트 HTTP로 웹사이트에 연결되는 것을 방지합니다. 최근에는 대부분의 사이트가 HTTPS를 지원하므로, 일상적인 웹 탐색에는 크게 영향을 미치지 않습니다.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (고급)

!!! tip "Use Mullvad Browser for advanced anti-fingerprinting"

    [Mullvad Browser](#mullvad-browser) provides the same anti-fingerprinting protections as Arkenfox out of the box, and does not require the use of Mullvad's VPN to benefit from these protections. Coupled with a VPN, Mullvad Browser can thwart more advanced tracking scripts which Arkenfox cannot. Arkenfox still has the advantage of being much more flexible, and allowing per-site exceptions for websites which you need to stay logged in to.

The [Arkenfox project](https://github.com/arkenfox/user.js) provides a set of carefully considered options for Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly - [which you can easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. We **strongly recommend** reading through their full [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox also enables [container](https://support.mozilla.org/en-US/kb/containers#w_for-advanced-users) support.

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

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

- [x] (선택 사항) **스크립트 차단** 활성화 (1)
- [x] 지문 차단을 **엄격, 사이트가 손상될 수 있음**으로 설정

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
- [x] **보안** 메뉴에서 **항상 보안 연결 사용** 활성화
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

- [ ] **기본 이더리움 월렛**을 **없음**으로 설정
- [ ] **기본 Solana 월렛**을 **없음**으로 설정
- [ ] **IPFS 리소스 리졸빙에 사용하는 방법**을 **사용 중지**로 설정

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

## Additional Resources

In general, we recommend keeping your browser extensions to a minimum to decrease your attack surface; they have privileged access within your browser, require you to trust the developer, can make you [stand out](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), and [weaken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) site isolation. However, uBlock Origin may prove useful if you value content blocking functionality.

### uBlock Origin

!!! recommendation

    ![uBlock Origin logo](assets/img/browsers/ublock_origin.svg){ align=right }
    
    **uBlock Origin** is a popular content blocker that could help you block ads, trackers, and fingerprinting scripts.
    
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

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state/).
