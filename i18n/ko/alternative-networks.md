---
title: "대체 네트워크"
icon: material/vector-polygon
description: 이 도구를 사용하면 월드 와이드 웹 이외의 네트워크에 접속할 수 있습니다.
cover: alternative-networks.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-server-network: 서비스 제공업체](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-eye-outline: 대규모 감시](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }
- [:material-account-cash: 감시 자본주의](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

## 익명화 네트워크 { #anonymizing-networks }

익명화 네트워크와 관련해서는 [토르](advanced/tor-overview.md)가 프라이버시 가이드의 최우선 선택지라는 점을 특별히 강조하고 싶습니다. 토르는 단연 가장 많이 사용되고, 가장 철저하게 연구되었으며, 가장 활발하게 개발되고 있는 익명 네트워크입니다. 무엇을 하는지 잘 알지 못한다면, 다른 네트워크를 사용할 경우 [:material-incognito: 익명성](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }이 위험해질 가능성이 더 높습니다.

### 토르 { #tor }

<div class="admonition recommendation" markdown>

![토르 로고](assets/img/self-contained-networks/tor.svg){ align=right }

**토르** 네트워크는 무료로 연결하여 인터넷에서 프라이버시와 보안을 향상할 수 있는, 자원봉사자가 운영하는 서버 그룹입니다. 개인과 단체는 ".onion 히든 서비스"를 통해 프라이버시를 침해받지 않고 토르 네트워크에서 정보를 공유할 수도 있습니다. 토르 트래픽은 차단하고 추적하기 어렵기 때문에, 토르는 효과적인 [:material-close-outline: 검열](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray } 우회 도구입니다.

[:octicons-home-16:](https://torproject.org){ .card-link title="홈페이지" }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="어니언 서비스" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title="문서"}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title="후원하기" }

</div>

토르 네트워크에 접속하는 권장 방법은 공식 토르 브라우저를 사용하는 것이며, 이에 대해서는 전용 페이지에서 자세히 다루고 있습니다:

[토르 브라우저 정보 :material-arrow-right-drop-circle:](tor.md){ .md-button .md-button--primary } [토르 상세 개요 :material-arrow-right-drop-circle:](advanced/tor-overview.md){ .md-button }

다른 도구로도 토르 네트워크에 접속할 수 있으며, 어떤 도구를 사용할지는 위협 모델에 따라 결정하면 됩니다. ISP가 여러분에게 불리한 증거를 수집하는 것을 걱정하지 않는 일반 토르 사용자라면, [오봇](#orbot) 같은 앱이나 모바일 브라우저 앱으로 토르 네트워크에 접속해도 괜찮을 것입니다. 일상적으로 토르를 사용하는 사람이 늘어나면 토르에 대한 부정적인 낙인을 줄이고, ISP와 정부가 작성할 수 있는 "토르 사용자 목록"의 가치를 떨어뜨릴 수 있습니다.

<div class="admonition example" markdown>
<p class="admonition-title">직접 해 보세요!</p>

토르를 통해 [xoe4vn5uwdztif6goazfbmogh6wh5jc4up35bqdflu6bkdc5cas5vjqd.onion](http://www.xoe4vn5uwdztif6goazfbmogh6wh5jc4up35bqdflu6bkdc5cas5vjqd.onion)에서 _프라이버시 가이&#xB4DC;_&#xC5D0; 접속해 볼 수 있습니다.

</div>

#### 오봇 { #orbot }

<div class="admonition recommendation" markdown>

![오봇 로고](assets/img/self-contained-networks/orbot.svg){ align=right }

**오봇**은 기기의 모든 앱 트래픽을 토르 네트워크로 라우팅하는 모바일 애플리케이션입니다.

[:octicons-home-16: 홈페이지](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title="문서" }
[:octicons-code-16:](https://orbot.app/code){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id1609461599)
- [:simple-github: 깃허브](https://github.com/guardianproject/orbot/releases)
- [:simple-fdroid: F-Droid](https://guardianproject.info/fdroid)

</details>

</div>

이전에는 오봇 설정에서 _목적지 주소 격리_(Isolate Destination Address) 환경설정을 활성화할 것을 권장했습니다. 이 설정은 연결하는 IP 주소마다 서로 다른 회로를 사용하도록 강제하여 이론적으로는 프라이버시를 향상할 수 있지만, 대부분의 애플리케이션(특히 웹 브라우징)에서는 실질적인 이점이 없고, 성능이 크게 저하될 수 있으며, 토르 네트워크의 부하를 늘립니다. 필요하다는 것을 확실히 알고 있는 경우가 아니라면 더 이상 이 설정을 기본값에서 변경하지 않을 것을 권장합니다.[^1]

\=== "안드로이드"

```
오봇은 SOCKS 또는 HTTP 프록시를 지원하는 개별 앱을 프록시할 수 있습니다. 또한 [VpnService](https://developer.android.com/reference/android/net/VpnService)를 사용해 모든 네트워크 연결을 프록시할 수 있으며, :gear: **설정** → **네트워크 및 인터넷** → **VPN** → :gear: → **VPN 없는 연결 차단**의 VPN 킬 스위치와 함께 사용할 수 있습니다.

구글 플레이와 가디언 프로젝트의 F-Droid 저장소에 있는 오봇은 오래된 버전인 경우가 많으므로, 대신 깃허브 저장소에서 직접 다운로드하는 것을 고려해 보세요. 모든 버전은 같은 서명으로 서명되므로 서로 호환됩니다.
```

\=== "iOS"

```
iOS에서 오봇에는 충돌이나 유출을 일으킬 수 있는 몇 가지 제한이 있습니다. iOS에는 안드로이드처럼 VPN 없는 연결을 차단하는 효과적인 OS 수준 기능이 없으며, 네트워크 확장 프로그램에 인위적인 메모리 제한이 있어 오봇에서 충돌 없이 토르를 실행하기가 어렵습니다. 현재로서는 항상 모바일 기기보다 데스크톱 컴퓨터에서 토르를 사용하는 것이 더 안전합니다.
```

#### 스노플레이크 { #snowflake }

<div class="admonition recommendation" markdown>

![스노플레이크 로고](assets/img/self-contained-networks/snowflake.svg#only-light){ align=right }
![스노플레이크 로고](assets/img/self-contained-networks/snowflake-dark.svg#only-dark){ align=right }

**스노플레이크**를 사용하면 브라우저에서 "스노플레이크 프록시"를 운영하여 토르 프로젝트에 대역폭을 기부할 수 있습니다.

검열을 받는 사람들은 스노플레이크 프록시를 사용해 토르 네트워크에 연결할 수 있습니다. 스노플레이크는 토르 릴레이나 브리지를 운영할 기술적 지식이 없더라도 네트워크에 기여할 수 있는 좋은 방법입니다.

[:octicons-home-16: 홈페이지](https://snowflake.torproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title="문서"}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title="후원하기" }

</details>

</div>

브라우저의 다른 탭에서 스노플레이크를 열고 스위치를 켜면 활성화할 수 있습니다. 브라우징하는 동안 백그라운드에서 계속 실행해 두어 연결을 기여할 수 있습니다. 서드파티 확장 프로그램을 추가하면 공격 표면이 늘어날 수 있으므로, 스노플레이크를 브라우저 확장 프로그램으로 설치하는 것은 권장하지 않습니다.

[브라우저에서 스노플레이크 실행하기 :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html){ .md-button }

스노플레이크는 여러분의 프라이버시를 어떤 식으로도 향상하지 않으며, 개인 브라우저에서 토르 네트워크에 연결하는 데 사용되지도 않습니다. 하지만 여러분의 인터넷 연결이 검열되지 않는다면, 검열된 네트워크에 있는 사람들이 더 나은 프라이버시를 얻을 수 있도록 스노플레이크를 실행하는 것을 고려해 보세요. 사람들이 여러분의 프록시를 통해 어떤 웹사이트에 접속하는지 걱정할 필요는 없습니다. 그들의 브라우징 IP 주소는 여러분이 아니라 토르 출구 노드로 표시되기 때문입니다.

스노플레이크 프록시를 운영하는 것은 위험이 낮으며, 그 자체로도 특별히 위험하지 않은 토르 릴레이나 브리지 운영보다도 위험이 더 낮습니다. 하지만 여러분의 네트워크를 통해 트래픽을 프록시하므로, 특히 네트워크 대역폭이 제한된 경우 어느 정도 영향이 있을 수 있습니다. 프록시 운영 여부를 결정하기 전에 [스노플레이크의 작동 방식](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home)을 반드시 이해하세요.

### I2P(보이지 않는 인터넷 프로젝트) { #i2p-the-invisible-internet-project }

<div class="admonition recommendation" markdown>

![I2P 로고](assets/img/self-contained-networks/i2p.svg#only-light){ align=right }
![I2P 로고](assets/img/self-contained-networks/i2p-dark.svg#only-dark){ align=right }

**I2P**는 연결을 암호화하고 전 세계에 분산된 컴퓨터 네트워크를 거쳐 라우팅하는 네트워크 계층입니다. 일반 인터넷 연결을 익명화하기보다는, 프라이버시를 보호하는 대안 네트워크를 만드는 데 주로 중점을 둡니다.

[:octicons-home-16: 홈페이지](https://geti2p.net/en){ .md-button .md-button--primary }
[:octicons-info-16:](https://geti2p.net/en/about/software){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/i2p/i2p.i2p){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://geti2p.net/en/get-involved){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=net.i2p.android)
- [:simple-android: 안드로이드](https://geti2p.net/en/download#android)
- [:fontawesome-brands-windows: 윈도우](https://geti2p.net/en/download#windows)
- [:simple-apple: macOS](https://geti2p.net/en/download#mac)
- [:simple-linux: 리눅스](https://geti2p.net/en/download#unix)

</details>

</div>

토르와 달리 모든 I2P 트래픽은 I2P 네트워크 내부에서만 오가므로, I2P에서는 일반 인터넷 웹사이트에 직접 접속할 수 **없습니다**. 대신 I2P 네트워크에서 익명으로 직접 호스팅되는 웹사이트에 접속할 수 있는데, 이를 "이프사이트(eepsite)"라고 하며 도메인이 `.i2p`로 끝납니다.

<div class="admonition example" markdown>
<p class="admonition-title">직접 해 보세요!</p>

I2P를 통해 [privacyguides.i2p](http://privacyguides.i2p/?i2paddresshelper=fvbkmooriuqgssrjvbxu7nrwms5zyhf34r3uuppoakwwsm7ysv6q.b32.i2p)에서 _프라이버시 가이&#xB4DC;_&#xC5D0; 접속해 볼 수 있습니다.

</div>

또한 토르와 달리 모든 I2P 노드는 전담 릴레이 자원봉사자가 노드를 운영하는 데 의존하는 대신, 기본적으로 다른 사용자의 트래픽을 중계합니다. 토르 네트워크에는 약 [10,000](https://metrics.torproject.org/networksize.html)개의 릴레이와 브리지가 있는 반면 I2P에는 약 50,000개가 있으므로, 익명성을 극대화하기 위해 트래픽을 라우팅할 수 있는 경로가 잠재적으로 더 많습니다. 또한 I2P는 토르보다 성능이 더 좋은 경향이 있는데, 이는 토르가 일반 "클리어넷" 인터넷 트래픽에 더 중점을 두어 병목 현상이 더 심한 출구 노드를 사용하는 데서 비롯된 부작용일 가능성이 높습니다. 히든 서비스 성능은 일반적으로 토르보다 I2P에서 훨씬 더 좋은 것으로 여겨집니다. 비트토렌트 같은 P2P 애플리케이션을 토르에서 실행하기는 어렵지만(그리고 토르 네트워크 성능에 막대한 영향을 줄 수 있지만), I2P에서는 매우 쉽고 성능도 좋습니다.

하지만 I2P의 접근 방식에도 단점이 있습니다. 토르는 전담 출구 노드에 의존하므로 덜 안전한 환경에 있는 더 많은 사람이 사용할 수 있으며, 토르의 릴레이는 일반적으로 가정용 회선에서 운영되지 않으므로 성능과 안정성이 더 뛰어날 가능성이 높습니다. 또한 토르는 브라우징 활동을 최대한 익명으로 만들기 위한 전용 [토르 브라우저](tor.md)를 갖추고 있어 **브라우저 프라이버시**(즉, 핑거프린팅 방지)에 훨씬 더 중점을 둡니다. I2P는 [일반 웹 브라우저](desktop-browsers.md)로 사용하며, 브라우저를 프라이버시를 더 잘 보호하도록 구성할 수는 있지만, 다른 I2P 사용자와 같은 브라우저 핑거프린트를 갖기는 어려울 것입니다(그런 면에서 섞여 들어갈 "군중"이 없습니다).

토르는 견고한 브리지 네트워크와 다양한 [플러거블 트랜스포트](https://tb-manual.torproject.org/circumvention) 덕분에 검열에 더 강할 가능성이 높습니다. 반면 I2P는 초기 연결에 자원봉사자가 운영하는, 다양하고 신뢰되지 않은 디렉터리 서버를 사용합니다. 이에 비해 토르가 사용하는 하드코딩된 신뢰된 디렉터리 서버는 차단하기가 더 쉬울 가능성이 높습니다.

[^1]: `IsolateDestAddr` 설정은 [토르 메일링 리스트](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403)와 [후닉스의 스트림 격리 문서](https://whonix.org/wiki/Stream_Isolation)에서 논의되었으며, 두 프로젝트 모두 이 설정이 대부분의 사람에게 좋은 방법이 아니라고 말합니다.
