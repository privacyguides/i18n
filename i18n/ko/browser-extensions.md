---
title: 브라우저 확장 프로그램
icon: material/puzzle-outline
description: 다음 브라우저 확장 프로그램은 브라우징 경험을 향상하고 프라이버시를 보호해 줍니다.
cover: browser-extensions.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-account-cash: 감시 자본주의](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

일반적으로 공격 표면을 줄이기 위해 브라우저 확장 프로그램은 최소한으로 유지할 것을 권장합니다. 확장 프로그램은 브라우저 안에서 권한 있는 접근 권한을 가지며, 개발자를 신뢰해야 하고, 여러분을 [눈에 띄게](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint) 만들 수 있으며, 사이트 격리를 [약화](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ)시킬 수 있습니다.

하지만 일부 확장 프로그램은 특정 상황, 특히 [콘텐츠 차단](basics/common-threats.md#mass-surveillance-programs)에 있어서는 이러한 단점을 상쇄하는 기능을 제공하기도 합니다.

당장 필요하지 않은 확장 프로그램이나 브라우저 기능과 중복되는 확장 프로그램은 설치하지 마세요. 예를 들어 [브레이브](desktop-browsers.md#brave) 사용자는 브레이브 실드가 이미 같은 기능을 제공하므로 유블록 오리진을 설치할 필요가 없습니다.

## 콘텐츠 차단기 { #content-blockers }

### 유블록 오리진 { #ublock-origin }

<div class="admonition recommendation" markdown>

![유블록 오리진 로고](assets/img/browsers/ublock_origin.svg){ align=right }

**유블록 오리진**은 광고, 추적기, 핑거프린팅 스크립트를 차단하는 데 도움이 되는 인기 있는 콘텐츠 차단기입니다.

[:octicons-repo-16: 저장소](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title="문서"}
[:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-firefoxbrowser: 파이어폭스](https://addons.mozilla.org/firefox/addon/ublock-origin)
- [:simple-googlechrome: 크롬](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
- [:fontawesome-brands-edge: 엣지](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)
- [:fontawesome-brands-opera: 오페라](https://addons.opera.com/en/extensions/details/ublock/)

</details>

</div>

[개발자 문서](https://github.com/gorhill/uBlock/wiki/Blocking-mode)를 참고하여 "모드" 중 하나를 선택할 것을 권장합니다. 필터 목록을 추가하면 성능에 영향을 줄 수 있으며 [공격 표면이 늘어날 수 있습니다](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

다음은 추가를 고려해 볼 만한 다른 [필터 목록](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists)입니다:

- [x] **개인정보 보호**(Privacy) > **AdGuard URL Tracking Protection** 체크
- [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt) 추가

### 유블록 오리진 라이트 { #ublock-origin-lite }

유블록 오리진에는 원래 확장 프로그램보다 기능이 제한된 "라이트" 버전도 있습니다. 하지만 정식 버전에 비해 몇 가지 뚜렷한 장점이 있으므로, 다음과 같은 경우라면 고려해 볼 만합니다...

- ...(유블록 오리진처럼 신뢰할 수 있는 확장 프로그램이라도) 어떤 확장 프로그램에도 "웹사이트 데이터 읽기/수정" 전체 권한을 부여하고 싶지 않은 경우
- ...리소스(메모리/CPU)를 더 효율적으로 사용하는 콘텐츠 차단기를 원하는 경우[^1]
- ...브라우저가 Manifest V3 확장 프로그램만 지원하는 경우. 크롬이 이에 해당합니다[^2].

<div class="admonition recommendation" markdown>

![유블록 오리진 라이트 로고](assets/img/browsers/ublock_origin_lite.svg){ align=right }

**유블록 오리진 라이트**는 Manifest V3와 호환되는 콘텐츠 차단기입니다. 원래의 _유블록 오리&#xC9C4;_&#xACFC; 비교해 이 확장 프로그램은 작동하는 데 광범위한 "데이터 읽기/수정" 권한이 필요하지 않으므로, 필터 목록에 악성 규칙이 추가되더라도 브라우저에 대한 [:material-bug-outline: 수동적 공격](basics/common-threats.md#security-and-privacy){ .pg-orange } 위험이 낮아집니다.

[:octicons-repo-16: 저장소](https://github.com/uBlockOrigin/uBOL-home#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uBlockOrigin/uBOL-home/wiki/Privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://github.com/uBlockOrigin/uBOL-home/wiki){ .card-link title="문서"}
[:octicons-code-16:](https://github.com/gorhill/uBlock/tree/master/platform/mv3){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googlechrome: 크롬](https://chrome.google.com/webstore/detail/ublock-origin-lite/ddkjiahejlhfcafbddmgiahcphecmpfh)
- [:fontawesome-brands-edge: 엣지](https://microsoftedge.microsoft.com/addons/detail/cimighlppcgcoapaliogpjjdehbnofhn)
- [:simple-safari: 사파리](https://apps.apple.com/app/id6745342698)

</details>

</div>

기본으로 포함되지 않은 필터 목록을 추가할 일이 전혀 없고, [동적 필터링](https://github.com/gorhill/ublock/wiki/dynamic-filtering:-quick-guide)이나 네트워크 로거 같은 고급 옵션도 필요하지 않은 경우에만 이 버전의 유블록 오리진을 추천합니다. 이러한 제한은 Manifest V3 설계상의 한계, 특히 필터링 규칙 수에 대한 엄격한 제한과 확장 프로그램이 일반적으로 원격 리소스를 가져올 수 없다는 점 때문입니다.[^3]

이 버전은 세 가지 차단 수준을 제공합니다. "기본"은 사이트 콘텐츠를 보고 수정하는 특별한 권한 없이 작동하며, "최적"과 "완전" 수준은 그러한 광범위한 권한이 필요하지만 추가 외형 규칙과 스크립틀릿 주입으로 더 나은 필터링 경험을 제공합니다.

기본 필터링 모드를 "최적"이나 "완전"으로 설정하면, 확장 프로그램은 방문하는 **모든** 웹사이트에 대한 읽기/수정 권한을 요청합니다. 하지만 특정 사이트에서 확장 프로그램 팝업 패널의 슬라이더를 조정하여 **사이트별로** 설정을 "최적"이나 "완전"으로 변경할 수도 있습니다. 이렇게 하면 확장 프로그램은 해당 사이트에 대한 읽기/수정 권한만 요청합니다. 따라서 유블록 오리진 라이트의 "권한 없는" 구성을 활용하고 싶다면, 기본 설정은 "기본"으로 두고 그 수준으로 충분하지 않은 사이트에서만 높이는 것이 좋습니다.

유블록 오리진 라이트는 필요할 때마다 차단 목록을 업데이트하는 것이 아니라, 브라우저의 확장 프로그램 마켓플레이스에서 확장 프로그램이 업데이트될 때만 차단 목록 업데이트를 받습니다. 구글은 필터 업데이트에 대해 [신속 심사 절차](https://developer.chrome.com/docs/webstore/skip-review)를 운영하므로, 일반적으로 유블록 오리진 라이트가 릴리스를 게시하는 만큼(지금까지는 2~7일마다) 자주 필터 목록 업데이트를 받을 수 있습니다. 하지만 이른바 "[안전한 규칙](https://developer.chrome.com/docs/extensions/reference/api/declarativeNetRequest#safe_rules)"만 업데이트할 수 있으므로, 고급 기법을 사용하는 목록은 업데이트 빈도가 제한될 수 있습니다.

### 애드가드 { #adguard }

iOS 사용자에게는 [사파리](mobile-browsers.md#safari-ios)를 추천하는데, 안타깝게도 사파리는 유블록 오리진 **라이트**만 지원합니다. 다행히 애드가드가 적절한 대안을 제공합니다:

<div class="admonition recommendation" markdown>

![애드가드 로고](assets/img/browsers/adguard.svg){ align=right }

**iOS용 애드가드**는 네이티브 [콘텐츠 차단기 API](https://developer.apple.com/documentation/safariservices/creating_a_content_blocker)를 사용하는 사파리용 자유 오픈 소스 콘텐츠 차단 확장 프로그램입니다.

[:octicons-home-16: 홈페이지](https://adguard.com/en/adguard-ios/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/ios.html){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title="문서"}
[:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id1047223162)

</details>

</div>

필터 목록을 추가하면 속도가 느려지고 공격 표면이 늘어날 수 있으므로, 필요한 것만 적용하세요. iOS용 애드가드에는 일부 프리미엄 기능이 있지만, 표준 사파리 콘텐츠 차단 기능은 무료입니다.

## 평가 기준 { #criteria }

- 브라우저나 운영 체제에 내장된 기능을 중복해서는 안 됩니다.
- 사용자의 프라이버시에 직접적인 영향을 주어야 합니다. 즉, 단순히 정보만 제공해서는 안 됩니다.

[^1]: 유블록 오리진 라이트는 필터링을 처리하기 위해 확장 프로그램 안에서 자바스크립트 코드를 실행하는 대신, 브라우저가 필터 목록을 직접 처리하게 하는 새로운 API를 사용하므로 _자체적으로는_ 리소스를 소비하지 않습니다. 하지만 이러한 리소스 이점은 [이론적인](https://github.com/uBlockOrigin/uBOL-home/wiki/Frequently-asked-questions-(FAQ)#is-ubol-more-efficient-cpu--and-memory-wise-than-ubo) 것에 불과합니다. 표준 유블록 오리진의 필터링 코드가 브라우저 자체의 필터링 코드보다 더 효율적일 수도 있기 때문입니다. 이는 아직 벤치마크로 검증되지 않았습니다.

[^2]: [브레이브](https://brave.com/blog/brave-shields-manifest-v3/)와 [오페라](https://xcancel.com/Opera_Security/status/2066543496001888753)는 가능한 한 오랫동안 MV2 지원을 유지하겠다고 약속했습니다.

[^3]: MV3 확장 프로그램도 이제 스크립트 사용을 요청할 수 있게 되면서 상황이 바뀌기 시작했습니다. 이를 통해 [애드가드](https://adguard.com/en/blog/adguard-browser-extension-v5-2.html)는 uBOL처럼 규칙을 직접 붙여넣는 대신 URL로 사용자 지정 필터 목록을 가져오는 기능을 제안할 수 있게 되었습니다.
