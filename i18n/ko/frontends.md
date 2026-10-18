---
title: "프런트엔드"
icon: material/flip-to-front
description: 다양한 인터넷 서비스를 위한 이 오픈 소스 프런트엔드를 사용하면 자바스크립트나 기타 성가신 요소 없이 콘텐츠에 접근할 수 있습니다.
cover: frontends.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-account-cash: 감시 자본주의](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

서비스는 때때로 성가신 팝업으로 콘텐츠 접근을 막아 계정 가입을 강요하려고 합니다. 자바스크립트를 활성화하지 않으면 제대로 작동하지 않을 수도 있습니다. 이러한 프런트엔드를 사용하면 이러한 제한을 우회할 수 있습니다.

이러한 프런트엔드를 직접 자체 호스팅한다면, 다른 사용자들 사이에 섞이기 위해 다른 사람들도 여러분의 인스턴스를 함께 사용하는 것이 중요합니다. 다른 사람들의 사용 내역이 여러분의 호스팅과 연결되므로, 어디서 어떻게 호스팅하는지에 주의해야 합니다.

다른 사람이 운영하는 인스턴스를 사용할 때는 해당 인스턴스의 개인정보 처리방침(있는 경우)을 꼭 읽어 보세요. 개인정보 처리방침은 운영자가 수정할 수 있으므로 기본 정책과 다를 수 있습니다. 일부 인스턴스에는 [토르](tor.md) .onion 주소가 있어, 검색어에 개인 식별 정보가 포함되지 않는 한 어느 정도 프라이버시를 제공할 수 있습니다.

## 레딧 { #reddit }

### 레드립 { #redlib }

<div class="admonition recommendation" markdown>

![레드립 로고](assets/img/frontends/redlib.svg){ align=right }

**레드립**은 자체 호스팅도 가능한 [레딧](https://reddit.com) 웹사이트용 오픈 소스 프런트엔드입니다. 여러 공개 인스턴스를 통해 레드립에 접속할 수 있습니다.

[:octicons-repo-16: 저장소](https://github.com/redlib-org/redlib){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/redlib-org/redlib-instances/blob/main/instances.md){ .card-link title="공개 인스턴스" }
[:octicons-info-16:](https://github.com/redlib-org/redlib?tab=readme-ov-file#table-of-contents){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/redlib-org/redlib){ .card-link title="소스 코드" }

</div>

<div class="admonition note" markdown>
<p class="admonition-title">참고</p>

[올드 레딧](https://old.reddit.com) 웹사이트는 새 레딧 웹사이트만큼 자바스크립트를 많이 필요로 하지 않지만, 최근 공용 VPN에 할당된 IP 주소의 접근을 차단했습니다. 올드 레딧은 [2022년 10월에 출시된](https://forum.torproject.org/t/reddit-onion-service-launch/5305) [토르](tor.md) 어니언 주소 [https://old.reddittorjg6rue252oqsxryoxengawnmo46qy4kyii5wtqnwfj4ooad.onion](https://old.reddittorjg6rue252oqsxryoxengawnmo46qy4kyii5wtqnwfj4ooad.onion)와 함께 사용할 수 있습니다.

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">팁</p>

레드립은 보안 수준이 "가장 안전(Safest)"으로 설정된 [토르 브라우저](tor.md#tor-browser)처럼 브라우저에서 자바스크립트를 비활성화하고 싶을 때 유용합니다.

</div>

## 유튜브 { #youtube }

**참고:** 유튜브는 동영상 플레이어와 API를 점진적으로 변경하여, 서드파티 프런트엔드가 유튜브 데이터를 추출하는 데 사용하는 일부 방법을 막아 왔습니다. 특정 유튜브 프런트엔드에서 안정성 문제가 발생한다면, 다른 추출 방식을 사용하는 프런트엔드를 사용해 보세요.

### 인비디어스 { #invidious }

<div class="admonition recommendation" markdown>

![인비디어스 로고](assets/img/frontends/invidious.svg#only-light){ align=right }
![인비디어스 로고](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }

**인비디어스**는 자체 호스팅도 가능한 [유튜브](https://youtube.com)용 자유 오픈 소스 프런트엔드입니다.

공개 인스턴스가 여러 개 있으며, 그중 일부는 [토르](tor.md) 어니언 서비스나 [I2P](alternative-networks.md#i2p-the-invisible-internet-project) 이프사이트를 제공합니다.

[:octicons-home-16: 홈페이지](https://invidious.io){ .md-button .md-button--primary }
[:octicons-server-16:](https://docs.invidious.io/instances){ .card-link title="공개 인스턴스" }
[:octicons-info-16:](https://docs.invidious.io){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://invidious.io/donate){ .card-link title="후원하기" }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

인비디어스는 기본적으로 동영상 스트림을 프록시하지 않습니다. 인비디어스로 시청하는 동영상은 여전히 구글 서버(예: `googlevideo.com`)에 직접 연결됩니다. 하지만 일부 인스턴스는 동영상 프록시를 지원하므로, 인스턴스 설정에서 *Proxy videos*(동영상 프록시)를 활성화하거나 URL에 `&local=true`를 추가하면 됩니다.

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">팁</p>

인비디어스는 보안 수준이 "가장 안전(Safest)"으로 설정된 [토르 브라우저](tor.md#tor-browser)처럼 브라우저에서 자바스크립트를 비활성화하고 싶을 때 유용합니다. 그 자체로 프라이버시를 제공하지는 않으며, 어떤 계정에도 로그인하지 않을 것을 권장합니다.

</div>

### 파이프드 { #piped }

<div class="admonition recommendation" markdown>

![파이프드 로고](assets/img/frontends/piped.svg){ align=right }

**파이프드**는 자체 호스팅도 가능한 [유튜브](https://youtube.com)용 자유 오픈 소스 프런트엔드입니다.

파이프드는 작동하는 데 자바스크립트가 필요하며, 공개 인스턴스가 여러 개 있습니다.

[:octicons-repo-16: 저장소](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/TeamPiped/documentation/blob/main/content/docs/public-instances/index.md){ .card-link title="공개 인스턴스" }
[:octicons-info-16:](https://docs.piped.video/docs){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title="후원하기" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">팁</p>

파이프드는 확장 프로그램을 설치하지 않고 [스폰서블록](https://sponsor.ajay.app)을 사용하고 싶을 때 유용합니다. 그 자체로 프라이버시를 제공하지는 않으며, 어떤 계정에도 로그인하지 않을 것을 권장합니다.

</div>

### 프리튜브 { #freetube }

<div class="admonition recommendation" markdown>

![프리튜브 로고](assets/img/frontends/freetube.svg){ align=right }

**프리튜브**는 [유튜브](https://youtube.com)용 자유 오픈 소스 데스크톱 애플리케이션입니다. 프리튜브는 [YouTube.js](https://github.com/LuanRT/YouTube.js) 기반의 내장 API나 [인비디어스](#invidious) API를 사용하여 유튜브에서 데이터를 추출합니다. 둘 중 하나를 기본값으로 설정하고, 다른 하나를 대체 수단으로 사용할 수 있습니다.

프리튜브를 사용하면 구독 목록, 재생목록, 시청 기록, 검색 기록이 기기에 로컬로 저장됩니다.

[:octicons-home-16: 홈페이지](https://freetubeapp.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://docs.freetubeapp.io){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: 윈도우](https://freetubeapp.io/#download)
- [:simple-apple: macOS](https://freetubeapp.io/#download)
- [:simple-linux: 리눅스](https://freetubeapp.io/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

프리튜브를 사용할 때는 설정에 따라 유튜브, [인비디어스](https://instances.invidious.io) 또는 [스폰서블록](https://sponsor.ajay.app)이 여전히 여러분의 IP 주소를 알 수 있습니다. [위협 모델](basics/threat-modeling.md)상 IP 주소를 숨겨야 한다면 [VPN](vpn.md)이나 [토르](tor.md) 사용을 고려해 보세요.

</div>

프리튜브는 기본적으로 모든 유튜브 광고를 차단합니다. 또한 프리튜브는 선택적으로 [스폰서블록](https://sponsor.ajay.app)과 연동하여 동영상의 스폰서 구간을 건너뛸 수 있도록 도와줍니다.

### 리브레튜브(안드로이드) { #libretube-android }

<div class="admonition recommendation" markdown>

![리브레튜브 로고](assets/img/frontends/libretube.svg#only-light){ align=right }
![리브레튜브 로고](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }

**리브레튜브**는 [파이프드](#piped) API를 사용하는 [유튜브](https://youtube.com)용 자유 오픈 소스 안드로이드 애플리케이션입니다.

구독 목록과 재생목록은 안드로이드 기기에 로컬로 저장됩니다.

[:octicons-home-16: 홈페이지](https://libretube.dev){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/libre-tube/LibreTube/blob/master/PRIVACY_POLICY.md){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://libretube.dev/#faq){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://github.com/libre-tube/LibreTube#donate){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-github: 깃허브](https://github.com/libre-tube/LibreTube/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

리브레튜브를 사용할 때는 설정에 따라 유튜브, [파이프드](https://github.com/TeamPiped/Piped/wiki/Instances) 또는 [스폰서블록](https://sponsor.ajay.app)이 여러분의 IP 주소를 볼 수 있습니다. [위협 모델](basics/threat-modeling.md)상 IP 주소를 숨겨야 한다면 [VPN](vpn.md)이나 [토르](tor.md) 사용을 고려해 보세요.

</div>

리브레튜브는 기본적으로 모든 유튜브 광고를 차단합니다. 또한 리브레튜브는 [스폰서블록](https://sponsor.ajay.app)을 사용하여 동영상의 스폰서 구간을 건너뛸 수 있도록 도와줍니다. 스폰서블록이 건너뛸 구간 유형을 자유롭게 설정하거나 완전히 비활성화할 수 있습니다. 원한다면 특정 동영상에서만 비활성화할 수 있는 버튼도 동영상 플레이어에 있습니다.

### 뉴파이프(안드로이드) { #newpipe-android }

<div class="admonition recommendation annotate" markdown>

![뉴파이프 로고](assets/img/frontends/newpipe.svg){ align=right }

**뉴파이프**는 [유튜브](https://youtube.com), [사운드클라우드](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [밴드캠프](https://bandcamp.com), [피어튜브](https://joinpeertube.org)(1)용 자유 오픈 소스 안드로이드 애플리케이션입니다.

구독 목록과 재생목록은 안드로이드 기기에 로컬로 저장됩니다.

[:octicons-home-16: 홈페이지](https://newpipe.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://newpipe.net/FAQ){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://newpipe.net/donate){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-github: 깃허브](https://github.com/TeamNewPipe/NewPipe/releases)

</details>

</div>

1. 기본 인스턴스는 [프라마튜브](https://framatube.org)이며, **설정** → **콘텐츠** → **PeerTube 인스턴스**에서 더 추가할 수 있습니다.

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

뉴파이프를 사용할 때는 이용하는 동영상 제공업체에 여러분의 IP 주소가 노출됩니다. [위협 모델](basics/threat-modeling.md)상 IP 주소를 숨겨야 한다면 [VPN](vpn.md)이나 [토르](tor.md) 사용을 고려해 보세요.

</div>

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

프라이버시 가이드는 해당 플랫폼에 대해 다음 중 하나 이상이 해당하는 경우에만 프런트엔드를 고려합니다:

- 일반적으로 자바스크립트를 활성화해야만 접근할 수 있는 경우.
- 일반적으로 계정이 있어야만 접근할 수 있는 경우.
- 상업용 [VPN](vpn.md)의 접근을 차단하는 경우.

추천 프런트엔드는...

- 오픈 소스 소프트웨어여야 합니다.
- 자체 호스팅이 가능해야 합니다.
- 익명 사용자도 웹사이트의 모든 기본 기능을 사용할 수 있어야 합니다.
