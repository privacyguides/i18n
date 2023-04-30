---
meta_title: "비공개 VPN 서비스 권장 목록 및 각 서비스 비교 (스폰서/광고 없음) - Privacy Guides"
title: "VPN 서비스"
icon: material/vpn
description: These are the best VPN services for protecting your privacy and security online. Find a provider here that isn’t out to spy on you.
cover: vpn.png
---

ISP로부터의 **프라이버시**가 필요하거나, 공용 Wi-Fi에 연결되어 있거나, 토렌트를 사용하는 중이라면 VPN이 알맞는 해결책이 될 수 있습니다. 다만, VPN의 단점들을 인지하고 있어야 합니다. We think these providers are a cut above the rest:

<div class="grid cards" markdown>

- ![IVPN logo](assets/img/vpn/mini/ivpn.svg){ .twemoji } [IVPN](#ivpn)
- ![Mullvad logo](assets/img/vpn/mullvad.svg){ .twemoji } [Mullvad](#mullvad)
- ![Proton VPN logo](assets/img/vpn/protonvpn.svg){ .twemoji } [Proton VPN](#proton-vpn)

</div>

!!! danger "VPN은 익명성을 제공하지 않습니다"

    VPN은 브라우저 사용 패턴을 익명화하지 않고, 보호되지 않은 트래픽 (HTTP)에 추가적인 보안을 제공하지 않습니다.
    
    만약 익명성이 필요하다면 VPN 대신 Tor 브라우저를 사용해야 합니다.
    
    만약 추가적인 보안이 필요하다면, 연결된 웹사이트가 HTTPS를 사용하는지 꼭 확인해야 합니다. VPN은 올바른 보안 관행을 대체할 수 없습니다.
    
    [Download Tor](https://www.torproject.org/){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

[VPN에 대해서 :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## 권장 제공 업체

Privacy Guides 권장 제공 업체는 암호화 사용, Monero 결제 지원, WireGuard & OpenVPN 지원, 노 로그 정책을 가지고 있습니다. 자세한 사항은 [전체 평가 기준](#criteria)을 참고해 주세요.

### IVPN

!!! recommendation

    ![IVPN 로고](assets/img/vpn/ivpn.svg){ align=right }
    
    **IVPN**은 유료 VPN 서비스 제공 업체입니다. 2009년부터 운영되었습니다. IVPN 본사는 지브롤터에 위치하고 있습니다.
    
    [:octicons-home-16: 홈페이지](https://www.ivpn.net/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.ivpn.net/privacy/){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://www.ivpn.net/knowledgebase/general/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/ivpn){ .card-link title="소스 코드" }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
        - [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
        - [:simple-appstore: App Store](https://apps.apple.com/app/ivpn-serious-privacy-protection/id1193122683)
        - [:simple-windows11: Windows](https://www.ivpn.net/apps-windows/)
        - [:simple-apple: macOS](https://www.ivpn.net/apps-macos/)
        - [:simple-linux: Linux](https://www.ivpn.net/apps-linux/)

#### :material-check:{ .pg-green } 35개 국가

IVPN은 [35개 국가에 서버](https://www.ivpn.net/server-locations)를 보유하고 있습니다.(1) 자신으로부터 가장 가까운 서버를 보유한 VPN 제공 업체를 선택하면 네트워크 트래픽 전송 지연 시간을 줄일 수 있습니다. 목적지까지의 경로가 더 짧기(Hop 횟수가 적기) 때문입니다.
{ .annotate }

1. 마지막 확인: 2022-09-16

We also think it's better for the security of the VPN provider's private keys if they use [dedicated servers](https://en.wikipedia.org/wiki/Dedicated_hosting_service), instead of cheaper shared solutions (with other customers) such as [virtual private servers](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Independently Audited

IVPN has undergone a [no-logging audit from Cure53](https://cure53.de/audit-report_ivpn.pdf) which concluded in agreement with IVPN's no-logging claim. IVPN has also completed a [comprehensive pentest report Cure53](https://cure53.de/summary-report_ivpn_2019.pdf) in January 2020. IVPN has also said they plan to have [annual reports](https://www.ivpn.net/blog/independent-security-audit-concluded) in the future. A further review was conducted [in April 2022](https://www.ivpn.net/blog/ivpn-apps-security-audit-2022-concluded/) and was produced by Cure53 [on their website](https://cure53.de/pentest-report_IVPN_2022.pdf).

#### :material-check:{ .pg-green } 오픈 소스 클라이언트

2020년 2월부터, [모든 IVPN 애플리케이션은 오픈 소스로 공개](https://www.ivpn.net/blog/ivpn-applications-are-now-open-source)되었습니다. 소스 코드는 IVPN [GitHub](https://github.com/ivpn)에서 찾아볼 수 있습니다.

#### :material-check:{ .pg-green } 현금 및 Monero 결제 가능

IVPN은 신용카드, 체크카드, 페이팔과 같은 결제 수단 외에도 비트코인, **Monero**와 **현금** (연간 구독에만 해당) 과 같은 익명 결제 수단 또한 지원합니다.

#### :material-check:{ .pg-green } WireGuard 지원

IVPN은 WireGuard® 프로토콜을 지원합니다. [WireGuard](https://www.wireguard.com)는 최신식 [암호화](https://www.wireguard.com/protocol/)를 사용하는 최신 프로토콜입니다. 또한, WireGuard는 보다 단순하면서도 더 나은 성능을 목표로 합니다.

IVPN은 자신들의 서비스에서 WireGuard 사용을 [권장](https://www.ivpn.net/wireguard/)하며, 모든 IVPN 앱은 WireGuard가 기본값으로 설정되어 있습니다. WireGuard [공식 앱](https://www.wireguard.com/install/)에서 사용할 수 있는 IVPN WireGuard 설정 생성기도 제공하고 있습니다.

#### :material-check:{ .pg-green } 원격 포트 포워딩

원격 [포트 포워딩](https://ko.wikipedia.org/wiki/%ED%8F%AC%ED%8A%B8_%ED%8F%AC%EC%9B%8C%EB%94%A9)은 Pro 요금제에서 사용 가능합니다. 포트 포워딩은 [Client Area에서 활성화](https://www.ivpn.net/knowledgebase/81/How-do-I-activate-port-forwarding.html)할 수 있습니다. IVPN에서 포트 포워딩은 WireGuard/OpenVPN 프로토콜을 사용할 때만 사용 가능하며, [미국 서버에서는 이용할 수 없습니다](https://www.ivpn.net/knowledgebase/116/Port-forwarding-is-not-working-why.html).

#### :material-check:{ .pg-green } 모바일 클라이언트

IVPN은 표준 OpenVPN 설정 파일 외에도, 간편하게 IVPN 서버와 연결 가능한 모바일 클라이언트를 [App Store](https://apps.apple.com/us/app/ivpn-serious-privacy-protection/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), [GitHub](https://github.com/ivpn/android-app/releases)에서 제공하고 있습니다.

#### :material-information-outline:{ .pg-blue } 추가 기능

IVPN 클라이언트는 이중 인증을 지원합니다(Mullvad 클라이언트는 지원하지 않습니다). 또한, IVPN은 네트워크 레벨에서 광고 네트워크 및 추적기를 차단하는 [AntiTracker](https://www.ivpn.net/antitracker)기능을 제공합니다.

### Mullvad

!!! recommendation

    ![Mullvad 로고](assets/img/vpn/mullvad.svg){ align=right }
    
    **Mullvad** 투명성과 보안에 중점을 둔, 속도가 빠르면서 비싸지 않은 VPN입니다. **2009년**부터 운영되었습니다. Mullvad 본사는 스웨덴에 위치하고 있으며, 무료 체험을 제공하지 않습니다.
    
    [:octicons-home-16: 홈페이지](https://mullvad.net/ko){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion 서비스" }
    [:octicons-eye-16:](https://mullvad.net/ko/help/privacy-policy/){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://mullvad.net/ko/help/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/mullvad){ .card-link title="소스 코드" }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
        - [:simple-appstore: App Store](https://apps.apple.com/app/mullvad-vpn/id1488466513)
        - [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
        - [:simple-windows11: Windows](https://mullvad.net/en/download/windows/)
        - [:simple-apple: macOS](https://mullvad.net/en/download/macos/)
        - [:simple-linux: Linux](https://mullvad.net/en/download/linux/)

#### :material-check:{ .pg-green } 41개 국가

Mullvad는 [41개 국가에 서버](https://mullvad.net/servers/)를 보유하고 있습니다.(1) 자신으로부터 가장 가까운 서버를 보유한 VPN 제공 업체를 선택하면 네트워크 트래픽 전송 지연 시간을 줄일 수 있습니다. 목적지까지의 경로가 더 짧기(Hop 횟수가 적기) 때문입니다.
{ .annotate }

1. 마지막 확인: 2023-01-19

We also think it's better for the security of the VPN provider's private keys if they use [dedicated servers](https://en.wikipedia.org/wiki/Dedicated_hosting_service), instead of cheaper shared solutions (with other customers) such as [virtual private servers](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Independently Audited

Mullvad의 VPN 클라이언트는 Cure53과 Assured AB의 감사를 받았으며, [cure53.de](https://cure53.de/pentest-report_mullvad_v2.pdf)에 게시된 침투 테스트 레포트를 볼 수 있습니다. 보안 연구원들은 다음과 같은 결론을 내렸습니다.

> Cure53 and Assured AB are happy with the results of the audit and the software leaves an overall positive impression. With security dedication of the in-house team at the Mullvad VPN compound, the testers have no doubts about the project being on the right track from a security standpoint.

2020년에는 두번째 감사가 [발표되었으며](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app/), [최종 감사 레포트](https://cure53.de/pentest-report_mullvad_2020_v2.pdf)는 Cure53의 사이트에 공개되었습니다.

> The results of this May-June 2020 project targeting the Mullvad complex are quite positive. [...] The overall application ecosystem used by Mullvad leaves a sound and structured impression. The overall structure of the application makes it easy to roll out patches and fixes in a structured manner. More than anything, the findings spotted by Cure53 showcase the importance of constantly auditing and re-assessing the current leak vectors, in order to always ensure privacy of the end-users. With that being said, Mullvad does a great job protecting the end-user from common PII leaks and privacy related risks.

2021년에는 시설 감사가 [발표되었으며](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit/), [최종 감사 결과 레포트](https://cure53.de/pentest-report_mullvad_2021_v1.pdf)가 Cure53의 사이트에 공개되었습니다. [2022년 6월](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data/)에 추가적인 감사가 의뢰되었으며, 해당 보고서는 [Assured의 사이트](https://www.assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf)에 공개되었습니다.

#### :material-check:{ .pg-green } 오픈 소스 클라이언트

Mullvad 데크스톱, 모바일 클라이언트 소스 코드는 [GitHub](https://github.com/mullvad/mullvadvpn-app)에 공개되어 있습니다.

#### :material-check:{ .pg-green } 현금 및 Monero 결제 가능

Mullvad는 신용카드, 체크카드, 페이팔과 같은 결제 수단 외에도 비트코인, 비트코인 캐쉬 (Bitcoin Cash), **Monero**와 **현금**과 같은 익명 결제 수단 또한 지원합니다. They also accept Swish and bank wire transfers.

#### :material-check:{ .pg-green } WireGuard 지원

Mullvad는 WireGuard® 프로토콜을 지원합니다. [WireGuard](https://www.wireguard.com)는 최신식 [암호화](https://www.wireguard.com/protocol/)를 사용하는 최신 프로토콜입니다. 또한, WireGuard는 보다 단순하면서도 더 나은 성능을 목표로 합니다.

Mullvad는 자신들의 서비스에서 WireGuard 사용을 [권장](https://mullvad.net/en/help/why-wireguard/)합니다. WireGuard 프로토콜은 Android, iOS, macOS, Linux의 Mullvad 앱에서는 기본으로 설정되어 있지만, Windows에서는 WireGuard 프로토콜을 [직접 활성화](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app/)해야 합니다. WireGuard [공식 앱](https://www.wireguard.com/install/)에서 사용할 수 있는 Mullvad WireGuard 설정 생성기도 제공하고 있습니다.

#### :material-check:{ .pg-green } IPv6 지원

Mullvad는 차기 네트워크 주소 체계인 [IPv6](https://en.wikipedia.org/wiki/IPv6)를 지원합니다. IPv6 연결들을 차단하는 다른 제공자와 달리 Mullvad의 네트워크는 [IPv6에 호스팅되는 서비스에 접근](https://mullvad.net/en/blog/2014/9/15/ipv6-support/)할 수 있도록 합니다.

#### :material-check:{ .pg-green } 원격 포트 포워딩

Remote [port forwarding](https://en.wikipedia.org/wiki/Port_forwarding) is allowed for people who make one-time payments, but not allowed for accounts with a recurring/subscription-based payment method. This is to prevent Mullvad from being able to identify you based on your port usage and stored subscription information. See [Port forwarding with Mullvad VPN](https://mullvad.net/help/port-forwarding-and-mullvad/) for more information.

#### :material-check:{ .pg-green } 모바일 클라이언트

Mullvad has published [App Store](https://apps.apple.com/app/mullvad-vpn/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } 추가 기능

Mullvad is very transparent about which nodes they [own or rent](https://mullvad.net/en/servers/). They use [ShadowSocks](https://shadowsocks.org/) in their ShadowSocks + OpenVPN configuration, making them more resistant against firewalls with [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) trying to block VPNs. Supposedly, [China has to use a different method to block ShadowSocks servers](https://github.com/net4people/bbs/issues/22). Mullvad's website is also accessible via Tor at [o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion).

### Proton VPN

!!! recommendation annotate

    ![Proton VPN 로고](assets/img/vpn/protonvpn.svg){ align=right }
    
    **Proton VPN**은 VPN 분야의 강력한 경쟁자로, 2016년부터 운영되고 있습니다. Proton AG 본사는 스위스에 위치하고 있으며, 제한된 무료 플랜과 더 많은 기능을 갖춘 프리미엄 옵션을 제공합니다.
    
    [:octicons-home-16: 홈페이지](https://protonvpn.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://protonvpn.com/support/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="소스 코드" }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id1437005085)
        - [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
        - [:simple-windows11: Windows](https://protonvpn.com/download-windows)
        - [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup/)

#### :material-check:{ .pg-green } 67개 국가

Proton VPN은 [67개 국가에 서버](https://protonvpn.com/vpn-servers)를 보유하고 있습니다.(1) 자신으로부터 가장 가까운 서버를 보유한 VPN 제공 업체를 선택하면 네트워크 트래픽 전송 지연 시간을 줄일 수 있습니다. 목적지까지의 경로가 더 짧기(Hop 횟수가 적기) 때문입니다.
{ .annotate }

1. 마지막 확인: 2022-09-16

We also think it's better for the security of the VPN provider's private keys if they use [dedicated servers](https://en.wikipedia.org/wiki/Dedicated_hosting_service), instead of cheaper shared solutions (with other customers) such as [virtual private servers](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Independently Audited

As of January 2020, Proton VPN has undergone an independent audit by SEC Consult. SEC Consult found some medium and low risk vulnerabilities in Proton VPN's Windows, Android, and iOS applications, all of which were "properly fixed" by Proton VPN before the reports were published. None of the issues identified would have provided an attacker remote access to your device or traffic. You can view individual reports for each platform at [protonvpn.com](https://protonvpn.com/blog/open-source/). In April 2022 Proton VPN underwent [another audit](https://protonvpn.com/blog/no-logs-audit/) and the report was [produced by Securitum](https://protonvpn.com/blog/wp-content/uploads/2022/04/securitum-protonvpn-nologs-20220330.pdf). A [letter of attestation](https://proton.me/blog/security-audit-all-proton-apps) was provided for Proton VPN's apps on 9th November 2021 by [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } 오픈 소스 클라이언트

Proton VPN 데스크톱, 모바일 클라이언트는 [GitHub](https://github.com/ProtonVPN)에 공개되어 있습니다.

#### :material-check:{ .pg-green } Accepts Cash

Proton VPN, in addition to accepting credit/debit cards, PayPal, and [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), also accepts **cash/local currency** as an anonymous form of payment.

#### :material-check:{ .pg-green } WireGuard 지원

Proton VPN은 일반적으로 WireGuard® 프로토콜을 지원합니다. [WireGuard](https://www.wireguard.com)는 최신식 [암호화](https://www.wireguard.com/protocol/)를 사용하는 최신 프로토콜입니다. 또한, WireGuard는 보다 단순하면서도 더 나은 성능을 목표로 합니다.

Proton VPN은 자신들의 서비스에서 WireGuard 사용을 [권장](https://protonvpn.com/blog/wireguard/)합니다. WireGuard 프로토콜은 Windows, macOS, iOS, Android, ChromeOS, Android TV의 Proton VPN 앱에서는 기본으로 설정되어 있지만, Linux 앱에서는 [지원되지 않습니다](https://protonvpn.com/support/how-to-change-vpn-protocols/).

#### :material-alert-outline:{ .pg-orange } 원격 포트 포워딩

Proton VPN currently only supports remote [port forwarding](https://protonvpn.com/support/port-forwarding/) on Windows, which may impact some applications. Especially Peer-to-peer applications like Torrent clients.

#### :material-check:{ .pg-green } 모바일 클라이언트

Proton VPN은 표준 OpenVPN 설정 파일 외에도, 간편하게 Proton VPN 서버와 연결 가능한 모바일 클라이언트를 [App Store](https://apps.apple.com/us/app/protonvpn-fast-secure-vpn/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android&hl=en_US), [GitHub](https://github.com/ProtonVPN/android-app/releases)에서 제공하고 있습니다.

#### :material-information-outline:{ .pg-blue } 추가 기능

Proton VPN clients support two factor authentication on all platforms except Linux at the moment. Proton VPN has their own servers and datacenters in Switzerland, Iceland and Sweden. They offer adblocking and known malware domains blocking with their DNS service. Additionally, Proton VPN also offers "Tor" servers allowing you to easily connect to onion sites, but we still strongly recommend using [the official Tor Browser](https://www.torproject.org/) for this purpose.

#### :material-alert-outline:{ .pg-orange } Killswitch feature is broken on Intel-based Macs

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch/) on Intel-based Macs when using the VPN killswitch. If you require this feature, and you are using a Mac with Intel chipset, you should consider using another VPN service.

## 평가 기준

!!! danger

    VPN은 익명성을 제공하지 않는다는 것을 인지하는 것은 매우 중요합니다. 다만, 특정 상황에서 더 나은 프라이버시를 제공할 수 있습니다. VPN은 불법적인 활동에 사용하는 도구가 아닙니다. "로그 없음" 정책에 의존하면 안됩니다.

**우리는 위 추천한 제공자와 그 어떤 제휴 관계에 있지 않습니다. This allows us to provide completely objective recommendations.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any VPN provider wishing to be recommended, including strong encryption, independent security audits, modern technology, and more. We suggest you familiarize yourself with this list before choosing a VPN provider, and conduct your own research to ensure the VPN provider you choose is as trustworthy as possible.

### 기술

We require all our recommended VPN providers to provide OpenVPN configuration files to be used in any client. **If** a VPN provides their own custom client, we require a killswitch to block network data leaks when disconnected.

**최소 요구 사항:**

- WireGuard와 OpenVPN과 같은 강력한 프로토콜을 지원
- 클라이언트에 킬스위치 (Killswitch)기능이 내장되어 있음
- 멀티홉을 지원함 멀티홉은 한 노드가 공격당할 경우 데이터를 지키는데에 중요하게 사용됩니다.
- If VPN clients are provided, they should be [open-source](https://en.wikipedia.org/wiki/Open_source), like the VPN software they generally have built into them. We believe that [source code](https://en.wikipedia.org/wiki/Source_code) availability provides greater transparency about what your device is actually doing.

**우대 사항:**

- WireGuard 및 OpenVPN 지원
- 다양한 설정들을 가진 킬스위치 기능 (일부 네트워크에만 활성화하기, 부팅시에만 활성화하기 등)
- 사용하기 쉬운 VPN 클라이언트
- Supports [IPv6](https://en.wikipedia.org/wiki/IPv6). We expect that servers will allow incoming connections via IPv6 and allow you to access services hosted on IPv6 addresses.
- Capability of [remote port forwarding](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) assists in creating connections when using P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) file sharing software or hosting a server (e.g., Mumble).

### 프라이버시

We prefer our recommended providers to collect as little data as possible. Not collecting personal information on registration, and accepting anonymous forms of payment are required.

**최소 요구 사항:**

- [익명 암호화폐](cryptocurrency.md) **또는** 현금 결제 옵션
- 가입하는 데에 개인정보 입력이 필수가 아님 (사용자명, 비밀번호, 이메일만 요구)

**우대 사항:**

- 다수의 [익명 결제 수단](advanced/payments.md) 지원
- 개인 정보를 받지 않음 (자동생성된 사용자명, 이메일 불필요 등)

### 보안

적절한 보안을 제공하지 않는 VPN은 없으나마나입니다. We require all our recommended providers to abide by current security standards for their OpenVPN connections. Ideally, they would use more future-proof encryption schemes by default. We also require an independent third-party to audit the provider's security, ideally in a very comprehensive manner and on a repeated (yearly) basis.

**최소 요구 사항:**

- Strong Encryption Schemes: OpenVPN with SHA-256 authentication; RSA-2048 or better handshake; AES-256-GCM or AES-256-CBC data encryption.
- Perfect Forward Secrecy (PFS).
- Published security audits from a reputable third-party firm.

**우대 사항:**

- 가장 강력한 암호화 방식으로 RSA-4096을 지원
- Perfect Forward Secrecy (PFS).
- Comprehensive published security audits from a reputable third-party firm.
- Bug-bounty programs and/or a coordinated vulnerability-disclosure process.

### 신뢰

You wouldn't trust your finances to someone with a fake identity, so why trust them with your internet data? We require our recommended providers to be public about their ownership or leadership. We also would like to see frequent transparency reports, especially in regard to how government requests are handled.

**최소 요구 사항:**

- Public-facing leadership or ownership.

**우대 사항:**

- Public-facing leadership.
- Frequent transparency reports.

### 마케팅

With the VPN providers we recommend we like to see responsible marketing.

**최소 요구 사항:**

- Must self-host analytics (i.e., no Google Analytics). The provider's site must also comply with [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) for people who want to opt-out.

Must not have any marketing which is irresponsible:

- Making guarantees of protecting anonymity 100%. When someone makes a claim that something is 100% it means there is no certainty for failure. We know people can quite easily deanonymize themselves in a number of ways, e.g.:
    - Reusing personal information (e.g., email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
    - [Browser fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Claim that a single circuit VPN is "more anonymous" than Tor, which is a circuit of three or more hops that regularly changes.
- Use responsible language: i.e., it is okay to say that a VPN is "disconnected" or "not connected", however claiming that someone is "exposed", "vulnerable" or "compromised" is needless use of alarming language that may be incorrect. For example, that person might simply be on another VPN provider's service or using Tor.

**우대 사항:**

Responsible marketing that is both educational and useful to the consumer could include:

- An accurate comparison to when [Tor](tor.md) should be used instead.
- Availability of the VPN provider's website over a [.onion service](https://en.wikipedia.org/wiki/.onion)

### 추가 기능

While not strictly requirements, there are some factors we looked into when determining which providers to recommend. These include adblocking/tracker-blocking functionality, warrant canaries, multihop connections, excellent customer support, the number of allowed simultaneous connections, etc.
