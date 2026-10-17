---
meta_title: "비공개 VPN 서비스 권장 목록 및 각 서비스 비교 (스폰서/광고 없음) - 프라이버시 가이드"
title: VPN 서비스
icon: 자료/Vpn
description: 온라인에서 여러분의 프라이버시와 보안을 지켜 주는 최고의 VPN 서비스를 소개합니다. 여러분을 감시하려 들지 않는 제공업체를 여기에서 찾아보세요.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-account-cash: 감시 자본주의(Surveillance Capitalism)](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

ISP로부터 또는 공용 와이파이 네트워크에서 추가적인 *프라이버시*를 원한다면, **VPN**이 해결책이 될 수 있습니다.

<div class="admonition danger" markdown>
<p class="admonition-title">VPN은 익명성을 제공하지 않습니다</p>

VPN을 사용한다고 해서 여러분의 탐색 습관이 익명으로 유지되는 것은 **아니며**, 보안되지 않은(HTTP) 트래픽에 보안이 추가되는 것도 아닙니다.

**익명성**을 원한다면 토르 브라우저를 사용해야 합니다. 추가적인 **보안**을 원한다면, 웹사이트에 접속할 때 항상 HTTPS를 사용하고 있는지 확인해야 합니다. VPN은 올바른 보안 관행을 대체할 수 없습니다.

[토르 브라우저 소개](tor.md#tor-browser){ .md-button .md-button--primary } [토르에 대한 오해와 FAQ](advanced/tor-overview.md){ .md-button }

</div>

[VPN에 대해서 :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## 권장 제공 업체

프라이버시 가이드 권장 제공 업체는 암호화 사용, 와이어가드 & OpenVPN 지원, 노 로그 정책을 가지고 있습니다. 자세한 사항은 [전체 평가 기준](#criteria)을 참고해 주세요.

| 서비스 제공자            | 국가   | 와이어가드                         | 포트포워딩                                        | IPv6                                              | 익명 결제   |
| ------------------ | ---- | ----------------------------- | -------------------------------------------- | ------------------------------------------------- | ------- |
| [프로톤](#proton-vpn) | 127+ | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } 부분 지원 | :material-information-outline:{ .pg-blue } 제한적 지원 | 현금      |
| [IVPN](#ivpn)      | 41+  | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }       | :material-information-outline:{ .pg-blue } 발신 전용  | 모네로  현금 |
| [멀바드](#mullvad)    | 49+  | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }       | :material-check:{ .pg-green }                     | 모네로  현금 |

### 프로톤 VPN

<div class="admonition recommendation" markdown>

![프로톤 VPN 로고](assets/img/vpn/protonvpn.svg){ align=right }

**프로톤 VPN**은 VPN 분야의 강력한 경쟁자로, 2016년부터 운영되고 있습니다. 프로톤 AG 본사는 스위스에 위치하고 있으며, 제한된 무료 플랜과 더 많은 기능을 갖춘 프리미엄 옵션을 제공합니다.

[:octicons-home-16: 홈페이지](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id1437005085)
- [:simple-github: 깃허브](https://github.com/ProtonVPN/android-app/releases)
- [:fontawesome-brands-windows: 윈도우](https://protonvpn.com/download-windows)
- [:simple-apple: macOS](https://protonvpn.com/download-macos)
- [:simple-linux: 리눅스](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 127개국

프로톤 VPN은 [127개국에 서버](https://protonvpn.com/vpn-servers)를 두고 있습니다.(1) 단, [무료 플랜](https://protonvpn.com/blog/product-roadmap-winter-2025-2026)을 사용하는 경우에는 [10](https://protonvpn.com/support/how-to-create-free-vpn-account)개국입니다.(2) 가까운 서버를 보유한 VPN 제공업체를 선택하면 전송하는 네트워크 트래픽의 지연 시간을 줄일 수 있습니다. 목적지까지의 경로가 더 짧기(Hop 횟수가 적기) 때문입니다.
{ .annotate }

1. 이 중 최소 71개국은 가상 서버로, IP는 해당 국가의 것으로 표시되지만 서버는 실제로 다른 국가에 있습니다. 그 외 12개 지역에는 물리 서버와 가상 서버가 모두 있습니다. [출처](https://protonvpn.com/support/how-smart-routing-works)
2. 최종 확인: 2025-10-28

우리는 VPN 제공자가 독립적인 [데디케이티드 서버](https://en.wikipedia.org/wiki/Dedicated_hosting_service)를 사용하는 것이 제공자의 개인 키를 보호하는데 더 좋다고 봅니다. [개인 사설 서버](https://en.wikipedia.org/wiki/Virtual_private_server)는 더 싸지만, VPN 제공자는 한 서버를 다른 사람들과 같이 쓰게 됩니다.

#### :material-check:{ .pg-green } 독립 감사 여부

독립 보안 연구원 루벤 산타마르타가 2024년 9월과 2025년 1월에 각각 프로톤 VPN의 [브라우저 확장 프로그램](https://drive.proton.me/urls/RWDD2SHT98#v7ZrwNcafkG8)과 [앱](https://drive.proton.me/urls/RVW8TXG484#uTXX5Fc9GADo)에 대한 감사를 수행했습니다. 프로톤 VPN의 인프라는 2022년부터 시큐리텀으로부터 [매년 감사](https://protonvpn.com/blog/no-logs-audit)를 받아 왔습니다.

그 이전인 2020년 1월에는 SEC 컨설트로부터 독립 감사를 받았습니다. SEC 컨설트는 프로톤 VPN의 윈도우, 안드로이드와 iOS 클라이언트에서 취약점을 찾았으며, 이 취약점들은 감사 레포트가 공개되기 전에 모두 적절히 고쳤다고 합니다. 확인된 취약점 중에서 공격자가 사용자의 기기 또는 트래픽에 원격으로 접속하는 것을 허용하는 것은 없습니다. 각 플랫폼별 개별 보고서는 감사에 관한 [블로그 게시물](https://web.archive.org/web/20250307041036/https://protonvpn.com/blog/open-source)에서 확인할 수 있습니다.

#### :material-check:{ .pg-green } 오픈 소스 클라이언트

프로톤 VPN은 데스크톱 및 모바일 클라이언트의 소스 코드를 [깃허브 조직](https://github.com/ProtonVPN)에 공개하고 있습니다.

#### :material-check:{ .pg-green } 현금 결제 가능

프로톤 VPN은 신용카드/체크카드, 페이팔, [비트코인](advanced/payments.md#other-coins-bitcoin-ethereum-etc) 외에도 익명 결제 수단으로 **현금/현지 통화**를 받습니다.

#### :material-check:{ .pg-green } 와이어가드 지원

프로톤 VPN은 와이어가드® 프로토콜을 지원합니다. [와이어가드](https://wireguard.com)는 최첨단 [암호화](https://wireguard.com/protocol)를 사용하는 최신 프로토콜입니다. 또한, 와이어가드는 보다 단순하면서도 더 나은 성능을 목표로 합니다.

프로톤 VPN은 자신들의 서비스에서 와이어가드 사용을 [권장](https://protonvpn.com/blog/wireguard)합니다. 프로톤 VPN은 공식 와이어가드 [앱](https://wireguard.com/install)에서 사용할 수 있는 와이어가드 설정 파일 생성기도 제공합니다.

#### :material-alert-outline:{ .pg-orange } 제한적인 IPv6 지원

프로톤은 이제 브라우저 확장 프로그램과 리눅스 클라이언트에서 [IPv6를 지원](https://protonvpn.com/support/prevent-ipv6-vpn-leaks)하지만, IPv6와 호환되는 서버는 전체의 80%에 불과합니다. 다른 플랫폼에서는 프로톤 VPN 클라이언트가 나가는 IPv6 트래픽을 모두 차단하므로 IPv6 주소가 유출될 걱정은 없지만, IPv6 전용 사이트에 접속할 수 없으며 IPv6 전용 네트워크에서는 프로톤 VPN에 연결할 수도 없습니다.

#### :material-information-outline:{ .pg-info } 원격 포트 포워딩

현재 프로톤 VPN은 NAT-PMP를 통한 임시 원격 [포트 포워딩](https://protonvpn.com/support/port-forwarding)만 지원하며, 임대 시간은 60초입니다. 공식 윈도우 및 리눅스 앱에서는 이 기능을 쉽게 켤 수 있는 옵션을 제공하지만, 다른 운영 체제에서는 직접 [NAT-PMP 클라이언트](https://protonvpn.com/support/port-forwarding-manual-setup)를 실행해야 합니다. 토렌트 애플리케이션은 대부분 NAT-PMP를 지원합니다.

#### :material-information-outline:{ .pg-blue } 검열 우회

프로톤 VPN에는 자체 [스텔스](https://protonvpn.com/blog/stealth-vpn-protocol) 프로토콜이 있어, OpenVPN이나 와이어가드 같은 VPN 프로토콜이 다양한 초보적인 기법으로 차단되는 상황에서 도움이 *될 수도* 있습니다. 스텔스는 VPN 터널을 TLS 세션으로 감싸 일반적인 인터넷 트래픽처럼 보이게 합니다.

안타깝게도 암호화된 터널을 찾아내기 위해 나가는 모든 트래픽을 분석하는 정교한 필터가 배치된 국가에서는 잘 작동하지 않습니다. 스텔스는 안드로이드, iOS, 윈도우, macOS에서 사용할 수 있지만, 리눅스에서는 아직 사용할 수 없습니다.

#### :material-check:{ .pg-green } 모바일 클라이언트

프로톤 VPN은 [앱 스토어](https://apps.apple.com/app/id1437005085)와 [구글 플레이](https://play.google.com/store/apps/details?id=ch.protonvpn.android)에 클라이언트를 출시했으며, 두 클라이언트 모두 와이어가드 연결을 직접 설정할 필요 없이 사용하기 쉬운 인터페이스를 제공합니다. 안드로이드 클라이언트는 [깃허브](https://github.com/ProtonVPN/android-app/releases)에서도 받을 수 있습니다.

<div class="admonition warning" markdown>
<p class="admonition-title">텔레메트리 공유를 끄는 방법</p>

안드로이드에서 프로톤은 설정 패널의 "**검열에 맞서도록 도와주세요**(Help us fight censorship)"라는, 오해의 소지가 있는 이름의 메뉴 안에 텔레메트리 설정을 숨겨 두었습니다. 다른 플랫폼에서는 "**사용 통계**(Usage statistics)" 메뉴에서 이 설정을 찾을 수 있습니다.

개발자와 익명 사용 통계를 공유하는 것을 굳이 말리지는 않지만, 이러한 설정은 쉽게 찾을 수 있고 명확하게 표시되어 있어야 하기 때문에 이 점을 언급합니다.

</div>

#### :material-alert-outline:{ .pg-orange } 추가 참고 사항

프로톤 VPN 클라이언트는 모든 플랫폼에서 2단계 인증을 지원합니다. 프로톤 VPN은 스위스, 아이슬란드와 스웨덴에 자체 서버와 데이터 센터를 보유하고 있습니다. 또한 DNS 서비스를 통해 콘텐츠 차단 및 알려진 악성 코드 차단 기능을 제공합니다. 또한 프로톤 VPN은 어니언 사이트에 쉽게 접속할 수 있는 "토르" 서버도 제공하지만, 이러한 용도로는 여전히 [공식 토르 브라우저](tor.md#tor-browser)를 사용할 것을 강력히 권장합니다.

##### macOS에서는 킬 스위치 기능의 보호 수준이 낮습니다

macOS용 프로톤 VPN의 킬 스위치는 사용자가 의도적으로 VPN 연결을 끊을 때 어떠한 트래픽도 차단하지 않으며, *이는 서버를 전환하면서 연결이 끊기는 경우도 마찬가지입니다.* VPN이 꺼져 있거나 서버를 전환하는 동안에는 민감한 연결을 해서는 안 됩니다. 이 기능은 예기치 않게 VPN 연결이 끊어졌을 때 트래픽 유출을 방지하도록만 설계되었습니다. 그것만으로도 유용한 기능이긴 하지만, VPN이 꺼져 있을 때 모든 트래픽을 차단하는 킬 스위치와 같은 수준의 보호는 제공하지 않습니다.

또한 인텔 기반 맥에서 VPN 킬 스위치를 사용하면 시스템 충돌이 [발생할 수 있습니다](https://protonvpn.com/support/macos-t2-chip-kill-switch). 만약 이 기능이 필요하지만 인텔 기반 맥을 사용하고 있다면, 다른 VPN 서비스를 사용하는 것을 추천합니다.

### IVPN

<div class="admonition recommendation" markdown>

![IVPN 로고](assets/img/vpn/ivpn.svg){ align=right }

**IVPN**은 유료 VPN 서비스 제공 업체입니다. 2009년부터 운영되었습니다. IVPN은 지브롤터에 위치해 있으며 무료 평가판을 제공하지 않습니다.

[:octicons-home-16: 홈페이지](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id1193122683)
- [:octicons-moon-16: 어크레센트](https://accrescent.app/app/net.ivpn.client)
- [:simple-github: 깃허브](https://github.com/ivpn/android-app/releases)
- [:fontawesome-brands-windows: 윈도우](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: 리눅스](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 41개국

IVPN은 [41개국에 서버](https://ivpn.net/status)를 두고 있습니다.(1) 가까운 서버를 보유한 VPN 제공업체를 선택하면 전송하는 네트워크 트래픽의 지연 시간을 줄일 수 있습니다. 목적지까지의 경로가 더 짧기(Hop 횟수가 적기) 때문입니다.
{ .annotate }

1. 최종 확인: 2025-10-28

우리는 VPN 제공자가 독립적인 [데디케이티드 서버](https://en.wikipedia.org/wiki/Dedicated_hosting_service)를 사용하는 것이 제공자의 개인 키를 보호하는데 더 좋다고 봅니다. [개인 사설 서버](https://en.wikipedia.org/wiki/Virtual_private_server)는 더 싸지만, VPN 제공자는 한 서버를 다른 사람들과 같이 쓰게 됩니다.

#### :material-check:{ .pg-green } 독립 감사 여부

IVPN은 2019년부터 여러 차례 [독립 감사](https://ivpn.net/en/blog/tags/audit)를 받았으며, [매년 보안 감사](https://ivpn.net/blog/ivpn-apps-security-audit-concluded)를 받겠다고 공개적으로 약속했습니다.

#### :material-check:{ .pg-green } 오픈 소스 클라이언트

2020년 2월부터 [IVPN 애플리케이션은 오픈 소스로 공개되었습니다](https://ivpn.net/blog/ivpn-applications-are-now-open-source). 소스 코드는 IVPN [깃허브](https://github.com/ivpn)에서 찾아볼 수 있습니다.

#### :material-check:{ .pg-green } 현금 및 모네로 결제 가능

IVPN은 신용카드/체크카드와 페이팔 외에도 익명 결제 수단으로 비트코인, **모네로**, **현금/현지 통화**(연간 플랜 한정)를 받습니다. 교환 코드가 포함된 [선불 카드](https://ivpn.net/knowledgebase/billing/voucher-cards-faq)를 구매할 수도 있습니다.

#### :material-check:{ .pg-green } 와이어가드 지원

IVPN은 와이어가드® 프로토콜을 지원합니다. [와이어가드](https://wireguard.com)는 최첨단 [암호화](https://wireguard.com/protocol)를 사용하는 최신 프로토콜입니다. 또한, 와이어가드는 보다 단순하면서도 더 나은 성능을 목표로 합니다.

IVPN은 자사 서비스에서 와이어가드 사용을 [권장](https://ivpn.net/wireguard)하며, 이에 따라 모든 IVPN 앱에서 와이어가드가 기본 프로토콜로 설정되어 있습니다. IVPN은 공식 와이어가드 [앱](https://wireguard.com/install)에서 사용할 수 있는 와이어가드 설정 파일 생성기도 제공합니다.

#### :material-information-outline:{ .pg-blue } IPv6 지원

IVPN에서는 [IPv6를 사용하는 서비스에 접속](https://ivpn.net/knowledgebase/general/do-you-support-ipv6)할 수 있지만, IPv6 주소를 사용하는 기기에서 연결할 수는 없습니다.

#### :material-alert-outline:{ .pg-orange } 원격 포트 포워딩

IVPN은 이전에 포트 포워딩을 지원했지만, [2023년 6월](https://ivpn.net/blog/gradual-removal-of-port-forwarding)에 이 옵션을 제거했습니다. 이 기능이 없을 경우 토렌트 클라이언트와 같은 P2P 앱을 사용하는 데에 문제가 발생할 수 있습니다.

#### :material-check:{ .pg-green } 검열 우회

IVPN은 [V2Ray](https://v2ray.com/en/index)를 사용하는 난독화 모드를 제공하며, 이는 OpenVPN이나 와이어가드 같은 VPN 프로토콜이 차단된 상황에서 도움이 됩니다. QUIC 또는 TCP 연결을 통해 [VMess](https://guide.v2fly.org/en_US/basics/vmess)를 사용하는 두 가지 모드가 있습니다. QUIC은 혼잡 제어가 더 뛰어난 최신 프로토콜이므로, 지연 시간이 줄어 더 빠를 수 있습니다. TCP 모드는 데이터를 일반적인 HTTP 트래픽처럼 보이게 합니다.

#### :material-check:{ .pg-green } 모바일 클라이언트

IVPN은 [앱 스토어](https://apps.apple.com/app/id1193122683)와 [구글 플레이](https://play.google.com/store/apps/details?id=net.ivpn.client)에 클라이언트를 출시했으며, 두 클라이언트 모두 와이어가드 연결을 직접 설정할 필요 없이 사용하기 쉬운 인터페이스를 제공합니다. 안드로이드 클라이언트는 [깃허브](https://github.com/ivpn/android-app/releases)에서도 받을 수 있습니다.

#### :material-information-outline:{ .pg-blue } 추가 참고 사항

IVPN 클라이언트는 2단계 인증을 지원합니다. IVPN은 네트워크 수준에서 광고 네트워크와 추적기를 차단하는 "[안티트래커](https://ivpn.net/antitracker)" 기능도 제공합니다.

### 멀바드

<div class="admonition recommendation" markdown>

![멀바드 로고](assets/img/vpn/mullvad.svg){ align=right }

**멀바드**는 투명성과 보안에 중점을 둔, 빠르고 저렴한 VPN입니다. 2009년부터 운영되고 있습니다. 멀바드는 스웨덴에 본사를 두고 있으며, 환불이 가능한 [결제 수단](https://mullvad.net/en/help/refunds)에 대해 14일 환불 보장을 제공합니다.

[:octicons-home-16: 홈페이지](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="어니언 서비스" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id1488466513)
- [:simple-github: 깃허브](https://github.com/mullvad/mullvadvpn-app/releases)
- [:fontawesome-brands-windows: 윈도우](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: 리눅스](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 49개국

멀바드는 [49개국에 서버](https://mullvad.net/servers)를 두고 있습니다.(1) 가까운 서버를 보유한 VPN 제공업체를 선택하면 전송하는 네트워크 트래픽의 지연 시간을 줄일 수 있습니다. 목적지까지의 경로가 더 짧기(Hop 횟수가 적기) 때문입니다.
{ .annotate }

1. 최종 확인: 2025-10-28

우리는 VPN 제공자가 독립적인 [데디케이티드 서버](https://en.wikipedia.org/wiki/Dedicated_hosting_service)를 사용하는 것이 제공자의 개인 키를 보호하는데 더 좋다고 봅니다. [개인 사설 서버](https://en.wikipedia.org/wiki/Virtual_private_server)는 더 싸지만, VPN 제공자는 한 서버를 다른 사람들과 같이 쓰게 됩니다.

#### :material-check:{ .pg-green } 독립 감사 여부

멀바드는 여러 차례 [독립 감사](https://mullvad.net/en/blog/tag/audits)를 받았으며, 앱과 인프라에 대해 [매년 감사](https://mullvad.net/en/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit)를 진행하겠다고 공개적으로 밝혔습니다.

#### :material-check:{ .pg-green } 오픈 소스 클라이언트

멀바드 데스크톱, 모바일 클라이언트 소스 코드는 [깃허브](https://github.com/mullvad/mullvadvpn-app)에 공개되어 있습니다.

#### :material-check:{ .pg-green } 현금 및 모네로 결제 가능

멀바드는 신용카드/체크카드와 페이팔 외에도 익명 결제 수단으로 비트코인, 비트코인 캐시, **모네로**, **현금/현지 통화**를 받습니다. 교환 코드가 포함된 [선불 카드](https://mullvad.net/en/help/partnerships-and-resellers)를 구매할 수도 있습니다. 멀바드는 스위시와 은행 송금은 물론, 몇몇 유럽 결제 시스템도 지원합니다.

#### :material-check:{ .pg-green } 와이어가드 지원

멀바드는 와이어가드® 프로토콜을 지원합니다. [와이어가드](https://wireguard.com)는 최첨단 [암호화](https://wireguard.com/protocol)를 사용하는 최신 프로토콜입니다. 또한, 와이어가드는 보다 단순하면서도 더 나은 성능을 목표로 합니다.

멀바드는 자사 서비스에서 와이어가드 사용을 [권장](https://mullvad.net/en/help/why-wireguard)합니다. 모바일 앱에서는 와이어가드가 지원되는 유일한 프로토콜이며, 데스크톱 앱에서도 2025년에 [OpenVPN 지원이 중단](https://mullvad.net/en/blog/reminder-that-openvpn-is-being-removed)될 예정입니다. 또한 멀바드 서버는 2026년 1월 15일까지 OpenVPN 연결 수락을 중단할 예정입니다. 멀바드는 공식 와이어가드 [앱](https://wireguard.com/install)에서 사용할 수 있는 와이어가드 설정 파일 생성기도 제공합니다.

#### :material-check:{ .pg-green } IPv6 지원

멀바드에서는 [IPv6로 호스팅되는 서비스에 접속](https://mullvad.net/en/blog/2014/9/15/ipv6-support)할 수 있고, IPv6 주소를 사용하는 기기에서 연결할 수도 있습니다.

#### :material-alert-outline:{ .pg-orange } 원격 포트 포워딩

멀바드는 이전에 포트 포워딩을 지원했지만, [2023년 5월](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports)에 이 옵션을 제거했습니다. 이 기능이 없을 경우 토렌트 클라이언트와 같은 P2P 앱을 사용하는 데에 문제가 발생할 수 있습니다.

#### :material-check:{ .pg-green } 검열 우회

멀바드는 검열을 우회하고 인터넷에 자유롭게 접속할 수 있도록 여러 기능을 제공합니다:

- **난독화 모드**: 멀바드에는 "UDP-over-TCP"와 ["섀도우삭스를 통한 와이어가드"](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard)라는 두 가지 난독화 모드가 내장되어 있습니다. 이 모드들은 VPN 트래픽을 일반 웹 트래픽으로 위장하여 검열 기관이 탐지하고 차단하기 어렵게 만듭니다. 알려진 바에 따르면, 중국은 [섀도우삭스를 통해 라우팅되는 트래픽을 방해하는 새로운 방법](https://gfw.report/publications/usenixsecurity23/en)을 사용해야 한다고 합니다.
- **섀도우삭스와 v2ray를 이용한 고급 난독화**: 고급 사용자를 위해 멀바드는 멀바드 클라이언트에서 [섀도우삭스 v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) 플러그인을 사용하는 방법에 대한 가이드를 제공합니다. 이 구성은 난독화와 암호화를 한 겹 더 추가합니다.
- **사용자 지정 서버 IP**: IP 차단에 대응하기 위해 멀바드 지원팀에 사용자 지정 서버 IP를 요청할 수 있습니다. 사용자 지정 IP를 받으면 "서버 IP 재정의(Server IP override)" 설정에 해당 텍스트 파일을 입력할 수 있으며, 이렇게 하면 선택한 서버 IP 주소가 검열 기관에 알려지지 않은 주소로 대체됩니다.
- **브리지 및 프록시**: 멀바드는 (인증에 필요한) API에 접근할 때 브리지나 프록시를 사용할 수 있게 해 주므로, API 접근 자체를 차단하는 검열 시도를 우회하는 데 도움이 됩니다.

#### :material-check:{ .pg-green } 모바일 클라이언트

멀바드는 [앱 스토어](https://apps.apple.com/app/id1488466513)와 [구글 플레이](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)에 클라이언트를 출시했으며, 두 클라이언트 모두 와이어가드 연결을 직접 설정할 필요 없이 사용하기 쉬운 인터페이스를 제공합니다. 안드로이드 클라이언트는 [깃허브](https://github.com/mullvad/mullvadvpn-app/releases)에서도 구할 수 있습니다.

#### :material-information-outline:{ .pg-blue } 추가 참고 사항

멀바드는 어떤 노드를 [소유하거나 임대](https://mullvad.net/en/servers)하고 있는지 매우 투명하게 공개합니다. 또한 앱에서 AI 기반 트래픽 분석 방어([DAITA](https://mullvad.net/en/blog/daita-defense-against-ai-guided-traffic-analysis)) 기능을 켤 수 있는 옵션도 제공합니다. DAITA는 VPN 트래픽의 패턴을 특정 웹사이트와 연결하는 데 사용될 수 있는 고급 트래픽 분석 위협으로부터 보호합니다.

## 평가 기준

<div class="admonition danger" markdown>
<p class="admonition-title">위험</p>

VPN은 익명성을 제공하지 않는다는 것을 인지하는 것은 매우 중요합니다. 다만, 특정 상황에서 더 나은 프라이버시를 제공할 수 있습니다. VPN은 불법적인 활동에 사용하는 도구가 아닙니다. "로그 없음" 정책에 의존하면 안됩니다.

</div>

**우리는 위 추천한 제공자와 그 어떤 제휴 관계에 있지 않습니다. 덕분에 완전히 객관적인 추천을 제공할 수 있습니다.** [일반 평가 기준](about/criteria.md) 외에도, 추천을 받고자 하는 VPN 제공업체를 위해 강력한 암호화, 독립 보안 감사, 최신 기술 등을 포함한 명확한 요구 사항을 마련했습니다. VPN 제공업체를 선택하기 전에 이 목록을 숙지하고, 선택한 VPN 제공업체가 최대한 신뢰할 수 있는지 직접 조사해 보시기 바랍니다.

### 기술

권장 제공업체는 현재 VPN에서 사용할 수 있는 최신 기술을 지원해야 합니다.

**최소 요구 사항:**

- 와이어가드 앱과 같은 범용 오픈 소스 클라이언트에서 사용할 수 있는 표준 설정 파일 제공
- 와이어가드와 같은 강력한 프로토콜 지원
- 권장하는 [데스크톱](desktop.md) 및 [모바일](android/distributions.md) 플랫폼용 공식 클라이언트에 제대로 작동하는 킬 스위치 내장 이 킬 스위치는 VPN 연결이 예기치 않게 끊어졌을 때 모든 인터넷 트래픽을 차단할 수 있어야 합니다.
- 멀티홉 지원 멀티홉은 단일 노드가 침해되었을 때도 데이터를 비공개로 유지하는 데 중요합니다.
- VPN 클라이언트를 제공하는 경우, 일반적으로 클라이언트에 내장된 VPN 소프트웨어와 마찬가지로 [오픈 소스](https://en.wikipedia.org/wiki/Open_source)여야 함 [소스 코드](https://en.wikipedia.org/wiki/Source_code)가 공개되어 있으면 프로그램이 실제로 무엇을 하는지 더 투명하게 알 수 있다고 생각합니다.
- DPI를 사용하지 않는 방화벽을 우회하도록 설계된 검열 저항 기능

**우대 사항:**

- 세부적으로 설정 가능한 옵션(특정 네트워크에서 활성화/비활성화, 부팅 시 활성화 등)을 갖춘 킬 스위치를 모든 주요 플랫폼에서 지원
- 사용하기 쉬운 VPN 클라이언트
- [IPv6](https://en.wikipedia.org/wiki/IPv6) 지원 서버들은 IPv6를 통한 연결을 허용하고, IPv6 주소에 호스팅되는 서비스에 접속할 수 있도록 해야 합니다.
- [원격 포트포워딩](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding)을 지원하여 P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) 파일 공유와 멈블과 같은 서비스 호스팅할 수 있음
- DPI 같은 고급 인터넷 검열 방식을 우회하도록 설계된, 인터넷 트래픽의 실제 성격을 위장하는 난독화 기술

### 프라이버시

프라이버시 가이드가 권장하는 제공자들은 최소한의 데이터만을 수집해야 합니다. 가입할 때 개인 정보를 수집하지 않아야 하고, 익명 결제 방식을 허용해야 합니다.

**최소 요구 사항:**

- [익명 암호화폐](cryptocurrency.md) **또는** 현금 결제 옵션
- 가입하는 데에 개인정보 입력이 필수가 아님 (사용자명, 비밀번호, 이메일만 요구)

**우대 사항:**

- 다수의 [익명 결제 수단](advanced/payments.md) 지원
- 개인 정보를 받지 않음 (자동 생성 사용자명, 이메일 불필요 등)

### 보안

적절한 보안을 제공하지 않는 VPN은 없으나마나입니다. 권장 제공업체는 모두 현행 보안 표준을 준수해야 합니다. 미래에도 유효한 암호화 체계를 사용하는 것이 제일 이상적입니다. 또한, 권장하는 제공자들은 외부 감사를 꼭 받아야 하며, 포괄적이면서 주기적으로 (매년) 받는 것이 이상적입니다.

**최소 요구 사항:**

- 강력한 암호화 방식 사용: SHA-256 해시 기반 인증을 이용하는 OpenVPN, RSA-2048 또는 더 강력한 비대칭 암호 알고리즘을 이용하는 핸드셰이크, AES-256-GCM 또는 AES-256-CBC 를 이용하는 데이터 암호화
- 순방향 비밀성 제공
- 검증된 제 3자로부터 보안 감사 결과가 게시됨
- 전체 디스크 암호화를 사용하거나 RAM 전용으로 운영되는 VPN 서버

**우대 사항:**

- 가장 강력한 암호화 방식으로 RSA-4096을 지원
- 선택적 양자 내성 암호화
- 검증된 제 3자로부터 종합적인 보안 감사 결과가 게시됨
- 버그 바운티 프로그램 또는 체계적인 취약점 공개 프로세스가 있음
- RAM 전용 VPN 서버

### 신뢰

가짜 신원을 가진 사람에게 재정을 맡기지 않을 텐데, 인터넷 데이터는 왜 맡기겠습니까? 권장 제공업체는 소유주 또는 경영진을 공개해야 합니다. 또한 특히 정부 요청을 어떻게 처리하는지에 관한 투명성 보고서를 자주 발행하기를 바랍니다.

**최소 요구 사항:**

- 경영진 또는 소유주 공개
- 비밀 로깅을 강제당할 수 없는 관할권에 기반을 둔 회사

**우대 사항:**

- 경영진 공개
- 주기적인 투명성 보고서 발행

### 마케팅

프라이버시 가이드가 권장하는 VPN 제공 업체들은 책임감 있는 마케팅을 할 것이라고 기대하고 있습니다.

**최소 요구 사항:**

- 분석 도구를 자체 호스팅해야 함 (즉, 구글 애널리틱스 사용 금지)

다음과 같은 무책임한 마케팅 방식을 사용하지 않아야 합니다.

- 익명성을 100% 보장해준다는 등의 내용: 만약 누군가가 100%라고 주장한다면, 이는 절대 실패할 수 없다고 하는 것과 같습니다. 익명성을 잃는 방법은 간단하면서도 다양하다는 것은 잘 알려져 있습니다. 예시로는 다음과 같습니다:
    - 익명성 소프트웨어 (토르, VPN 등) 를 사용하지 않고 개인 정보 (이메일 계정, 온라인 아이디) 를 재사용하는 행위
    - [브라우저 핑거프린팅](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- 노드 1개만을 거치는 VPN이 주기적으로 변하는 노드 3개를 거치는 토르보다 익명성을 보호하는데 더 좋다는 주장
- 무책임한 표현 사용 금지: 사이트에서 VPN에 "연결됨" 또는 "연결되지 않음"이라고 표시하는 것은 문제되지 않지만, VPN에 연결되지 않았을 경우 "노출됨", "취약함"과 같은 단어 표현은 필요 이상으로 사용자에게 경고를 주며, 아예 올바르지 않을 수 있습니다. 예시로, 해당 사용자는 타사의 VPN을 사용하고 있거나 토르를 사용하고 있을 수 있습니다.

**우대 사항:**

사용자에게 유용한 책임감 있는 마케팅의 예시는 다음과 같습니다:

- [토르](tor.md)를 사용하기 적합한 상황을 정확하게 설명함
- VPN 제공자의 웹사이트가 [.onion](https://en.wikipedia.org/wiki/.onion)으로도 접근이 가능

### 추가 기능

엄격하게 적용한 요구 사항은 아니지만, 이 외의 요소 일부 또한 고려하여 권장 제공 업체를 결정했습니다. 여기에는 콘텐츠 차단 기능, 워런트 카나리, 우수한 고객 지원, 허용되는 동시 접속 수 등이 포함됩니다.
