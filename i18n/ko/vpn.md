---
meta_title: "비공개 VPN 서비스 권장 목록 및 각 서비스 비교 (스폰서/광고 없음) - Privacy Guides"
title: "VPN 서비스"
icon: material/vpn
description: These are the best VPN services for protecting your privacy and security online. Find a provider here that isn’t out to spy on you.
cover: vpn.webp
---

<!-- markdownlint-disable MD024 -->

ISP로부터의 **프라이버시**가 필요하거나, 공용 Wi-Fi에 연결되어 있거나, 토렌트를 사용하는 중이라면 VPN이 알맞는 해결책이 될 수 있습니다. 다만, VPN의 단점들을 인지하고 있어야 합니다. We think these providers are a cut above the rest:

<div class="grid cards" markdown>

- ![Proton VPN 로고](assets/img/vpn/protonvpn.svg){ .twemoji } [Proton VPN](#proton-vpn)
- ![IVPN 로고](assets/img/vpn/mini/ivpn.svg){ .twemoji } [IVPN](#ivpn)
- ![Mullvad 로고](assets/img/vpn/mullvad.svg){ .twemoji } [Mullvad](#mullvad)

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">VPNs do not provide anonymity</p>

VPN은 브라우저 사용 패턴을 익명화하지 않고, 보호되지 않은 트래픽 (HTTP)에 추가적인 보안을 제공하지 않습니다.

If you are looking for **anonymity**, you should use the Tor Browser.

만약 추가적인 보안이 필요하다면, 연결된 웹사이트가 HTTPS를 사용하는지 꼭 확인해야 합니다. VPN은 올바른 보안 관행을 대체할 수 없습니다.

[Download Tor](https://torproject.org){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[VPN에 대해서 :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## 권장 제공 업체

Privacy Guides 권장 제공 업체는 암호화 사용, Monero 결제 지원, WireGuard & OpenVPN 지원, 노 로그 정책을 가지고 있습니다. 자세한 사항은 [전체 평가 기준](#criteria)을 참고해 주세요.

### Proton VPN

<div class="admonition recommendation" markdown>

![Proton VPN 로고](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN**은 VPN 분야의 강력한 경쟁자로, 2016년부터 운영되고 있습니다. Proton AG 본사는 스위스에 위치하고 있으며, 제한된 무료 플랜과 더 많은 기능을 갖춘 프리미엄 옵션을 제공합니다.

[:octicons-home-16: Homepage](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:simple-windows11: Windows](https://protonvpn.com/download-windows)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 91 Countries

Proton VPN has [servers in 91 countries](https://protonvpn.com/vpn-servers) [or 8 if you use their free plan](https://protonvpn.com/free-vpn).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. 목적지까지의 경로가 더 짧기(Hop 횟수가 적기) 때문입니다.
{ .annotate }

1. Last checked: 2024-04-02

우리는 VPN 제공자가 독립적인 [데디케이티드 서버](https://en.wikipedia.org/wiki/Dedicated_hosting_service)를 사용하는 것이 제공자의 개인 키를 보호하는데 더 좋다고 봅니다. [개인 사설 서버](https://en.wikipedia.org/wiki/Virtual_private_server)는 더 싸지만, VPN 제공자는 한 서버를 다른 사람들과 같이 쓰게 됩니다.

#### :material-check:{ .pg-green } 독립 감사 여부

2020년 1월에 Proton VPN은 SEC Consult로부터 독립 감사를 받았습니다. SEC Consult는 Proton VPN의 Windows, Android와 iOS 클라이언트에서 취약점을 찾았으며, 이 취약점들은 감사 레포트가 공개되기 전에 모두 적절히 고쳤다고 합니다. 확인된 취약점 중에서 공격자가 사용자의 기기 또는 트래픽에 원격으로 접속하는 것을 허용하는 것은 없습니다. You can view individual reports for each platform at [protonvpn.com](https://protonvpn.com/blog/open-source). In April 2022 Proton VPN underwent [another audit](https://protonvpn.com/blog/no-logs-audit) and the report was [produced by Securitum](https://protonvpn.com/blog/wp-content/uploads/2022/04/securitum-protonvpn-nologs-20220330.pdf). A [letter of attestation](https://proton.me/blog/security-audit-all-proton-apps) was provided for Proton VPN's apps on 9th November 2021 by [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } 오픈 소스 클라이언트

Proton VPN 데스크톱, 모바일 클라이언트는 [GitHub](https://github.com/ProtonVPN)에 공개되어 있습니다.

#### :material-check:{ .pg-green } 현금 결제 가능

Proton VPN은 신용카드, 체크카드, 페이팔 외에도 [비트코인](advanced/payments.md#other-coins-bitcoin-ethereum-etc)과 **현금** 결제도 받습니다.

#### :material-check:{ .pg-green } WireGuard 지원

Proton VPN은 일반적으로 WireGuard® 프로토콜을 지원합니다. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). 또한, WireGuard는 보다 단순하면서도 더 나은 성능을 목표로 합니다.

Proton VPN [recommends](https://protonvpn.com/blog/wireguard) the use of WireGuard with their service. On Proton VPN's Windows, macOS, iOS, Android, ChromeOS, and Android TV apps, WireGuard is the default protocol; however, [support](https://protonvpn.com/support/how-to-change-vpn-protocols) for the protocol is not present in their Linux app.

#### :material-alert-outline:{ .pg-orange } No IPv6 Support

Proton VPN's servers are only compatible with IPv4. The Proton VPN applications will block all outgoing IPv6 traffic, so you don't have to worry about your IPv6 address being leaked, but you will not be able to connect to any IPv6-only sites, and you will not be able to connect to Proton VPN from an IPv6-only network.

#### :material-alert-outline:{ .pg-orange } 원격 포트 포워딩

Proton VPN currently only supports ephemeral remote [port forwarding](https://protonvpn.com/support/port-forwarding) via NAT-PMP, with 60 second lease times. The Windows app provides an easy to access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup). 토렌트 애플리케이션은 대부분 NAT-PMP를 지원합니다.

#### :material-information-outline:{ .pg-blue } Anti-Censorship

Proton VPN has their [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) protocol which *may* help in situations where VPN protocols like OpenVPN or Wireguard are blocked with various rudimentary techniques. Stealth encapsulates the VPN tunnel in TLS session in order to look like more generic internet traffic.

Unfortunately it does not work very well in countries where sophisticated filters are deployed that analyze all outgoing traffic in an attempt to discover encrypted tunnels. Stealth is also not yet available on [Windows](https://github.com/ProtonVPN/win-app/issues/64) or Linux.

#### :material-check:{ .pg-green } 모바일 클라이언트

In addition to providing standard OpenVPN configuration files, Proton VPN has mobile clients for [App Store](https://apps.apple.com/app/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android), and [GitHub](https://github.com/ProtonVPN/android-app/releases) allowing for easy connections to their servers.

#### :material-alert-outline:{ .pg-orange } Additional Notes

Proton VPN 클라이언트는 Linux를 제외한 모든 플랫폼에서 2단계 인증을 지원합니다. Proton VPN은 스위스, 아이슬란드와 스웨덴에 자체 서버와 데이터 센터를 보유하고 있습니다. They offer content blocking and known-malware blocking with their DNS service. Additionally, Proton VPN also offers "Tor" servers allowing you to easily connect to onion sites, but we still strongly recommend using [the official Tor Browser](https://torproject.org) for this purpose.

##### :material-alert-outline:{ .pg-orange } Intel 기반 Mac에서의 킬스위치 문제

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch) on Intel-based Macs when using the VPN killswitch. 만약 이 기능이 필요하지만 Intel 기반 Mac을 사용하고 있다면, 다른 VPN 서비스를 사용하는 것을 추천합니다.

### IVPN

<div class="admonition recommendation" markdown>

![IVPN 로고](assets/img/vpn/ivpn.svg){ align=right }

**IVPN**은 유료 VPN 서비스 제공 업체입니다. 2009년부터 운영되었습니다. IVPN 본사는 지브롤터에 위치하고 있습니다.

[:octicons-home-16: Homepage](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:simple-windows11: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 37 Countries

IVPN has [servers in 37 countries](https://ivpn.net/status).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. 목적지까지의 경로가 더 짧기(Hop 횟수가 적기) 때문입니다.
{ .annotate }

1. Last checked: 2024-04-02

우리는 VPN 제공자가 독립적인 [데디케이티드 서버](https://en.wikipedia.org/wiki/Dedicated_hosting_service)를 사용하는 것이 제공자의 개인 키를 보호하는데 더 좋다고 봅니다. [개인 사설 서버](https://en.wikipedia.org/wiki/Virtual_private_server)는 더 싸지만, VPN 제공자는 한 서버를 다른 사람들과 같이 쓰게 됩니다.

#### :material-check:{ .pg-green } 독립 감사 여부

IVPN은 [Cure53으로부터 감사](https://cure53.de/audit-report_ivpn.pdf)를 받아 로그가 존재하지 않는다는 IVPN의 주장이 사실임을 보였습니다. 또한, 2020년 1월에 [Cure53은 IVPN 침투 테스트 결과](https://cure53.de/summary-report_ivpn_2019.pdf)를 레포트로 작성하였습니다. IVPN has also said they plan to have [annual reports](https://ivpn.net/blog/independent-security-audit-concluded) in the future. A further review was conducted [in April 2022](https://ivpn.net/blog/ivpn-apps-security-audit-2022-concluded) and was produced by Cure53 [on their website](https://cure53.de/pentest-report_IVPN_2022.pdf).

#### :material-check:{ .pg-green } 오픈 소스 클라이언트

As of February 2020 [IVPN applications are now open source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). 소스 코드는 IVPN [GitHub](https://github.com/ivpn)에서 찾아볼 수 있습니다.

#### :material-check:{ .pg-green } 현금 및 Monero 결제 가능

IVPN은 신용카드, 체크카드, 페이팔과 같은 결제 수단 외에도 비트코인, **Monero**와 **현금** (연간 구독에만 해당) 과 같은 익명 결제 수단 또한 지원합니다.

#### :material-check:{ .pg-green } WireGuard 지원

IVPN은 WireGuard® 프로토콜을 지원합니다. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). 또한, WireGuard는 보다 단순하면서도 더 나은 성능을 목표로 합니다.

IVPN [recommends](https://ivpn.net/wireguard) the use of WireGuard with their service and, as such, the protocol is the default on all of IVPN's apps. IVPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-information-outline:{ .pg-blue } IPv6 Support

IVPN allows you to [connect to services using IPv6](https://www.ivpn.net/knowledgebase/general/do-you-support-ipv6) but doesn't allow you to connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } 원격 포트 포워딩

IVPN previously supported port forwarding, but removed the option in [June 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). 이 기능이 없을 경우 토렌트 클라이언트와 같은 P2P 앱을 사용하는 데에 문제가 발생할 수 있습니다.

#### :material-check:{ .pg-green } Anti-Censorship

IVPN has obfuscation modes using the [v2ray](https://v2ray.com/en/index.html) project which helps in situations where VPN protocols like OpenVPN or Wireguard are blocked. Currently this feature is only available on Desktop and [iOS](https://ivpn.net/knowledgebase/ios/v2ray). It has two modes where it can use [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) over QUIC or TCP connections. QUIC is a modern protocol with better congestion control and therefore may be faster with reduced latency. The TCP mode makes your data appear as regular HTTP traffic.

#### :material-check:{ .pg-green } 모바일 클라이언트

In addition to providing standard OpenVPN configuration files, IVPN has mobile clients for [App Store](https://apps.apple.com/app/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), and [GitHub](https://github.com/ivpn/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } Additional Notes

IVPN 클라이언트는 이중 인증을 지원합니다(Mullvad 클라이언트는 지원하지 않습니다). IVPN also provides "[AntiTracker](https://ivpn.net/antitracker)" functionality, which blocks advertising networks and trackers from the network level.

### Mullvad

<div class="admonition recommendation" markdown>

![Mullvad 로고](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** 투명성과 보안에 중점을 둔, 속도가 빠르면서 비싸지 않은 VPN입니다. **2009년**부터 운영되었습니다. Mullvad 본사는 스웨덴에 위치하고 있으며, 무료 체험을 제공하지 않습니다.

[:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:simple-windows11: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 41 Countries

Mullvad has [servers in 41 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. 목적지까지의 경로가 더 짧기(Hop 횟수가 적기) 때문입니다.
{ .annotate }

1. Last checked: 2024-04-02

우리는 VPN 제공자가 독립적인 [데디케이티드 서버](https://en.wikipedia.org/wiki/Dedicated_hosting_service)를 사용하는 것이 제공자의 개인 키를 보호하는데 더 좋다고 봅니다. [개인 사설 서버](https://en.wikipedia.org/wiki/Virtual_private_server)는 더 싸지만, VPN 제공자는 한 서버를 다른 사람들과 같이 쓰게 됩니다.

#### :material-check:{ .pg-green } 독립 감사 여부

Mullvad의 VPN 클라이언트는 Cure53과 Assured AB의 감사를 받았으며, [cure53.de](https://cure53.de/pentest-report_mullvad_v2.pdf)에 게시된 침투 테스트 레포트를 볼 수 있습니다. 보안 연구원들은 다음과 같은 결론을 내렸습니다.

> Cure53 and Assured AB are happy with the results of the audit and the software leaves an overall positive impression. With security dedication of the in-house team at the Mullvad VPN compound, the testers have no doubts about the project being on the right track from a security standpoint.

In 2020 a second audit [was announced](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app) and the [final audit report](https://cure53.de/pentest-report_mullvad_2020_v2.pdf) was made available on Cure53's website:

> The results of this May-June 2020 project targeting the Mullvad complex are quite positive. ... The overall application ecosystem used by Mullvad leaves a sound and structured impression. The overall structure of the application makes it easy to roll out patches and fixes in a structured manner. More than anything, the findings spotted by Cure53 showcase the importance of constantly auditing and re-assessing the current leak vectors, in order to always ensure privacy of the end-users. With that being said, Mullvad does a great job protecting the end-user from common PII leaks and privacy related risks.

In 2021 an infrastructure audit [was announced](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) and the [final audit report](https://cure53.de/pentest-report_mullvad_2021_v1.pdf) was made available on Cure53's website. Another report was commissioned [in June 2022](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data) and is available on [Assured's website](https://assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf).

#### :material-check:{ .pg-green } 오픈 소스 클라이언트

Mullvad 데크스톱, 모바일 클라이언트 소스 코드는 [GitHub](https://github.com/mullvad/mullvadvpn-app)에 공개되어 있습니다.

#### :material-check:{ .pg-green } 현금 및 Monero 결제 가능

Mullvad는 신용카드, 체크카드, 페이팔과 같은 결제 수단 외에도 비트코인, 비트코인 캐쉬 (Bitcoin Cash), **Monero**와 **현금**과 같은 익명 결제 수단 또한 지원합니다. Swish 및 은행 송금도 가능합니다.

#### :material-check:{ .pg-green } WireGuard 지원

Mullvad는 WireGuard® 프로토콜을 지원합니다. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). 또한, WireGuard는 보다 단순하면서도 더 나은 성능을 목표로 합니다.

Mullvad [recommends](https://mullvad.net/en/help/why-wireguard) the use of WireGuard with their service. It is the default or only protocol on Mullvad's Android, iOS, macOS, and Linux apps, but on Windows you have to [manually enable](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-check:{ .pg-green } IPv6 지원

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) and connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } 원격 포트 포워딩

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). 이 기능이 없을 경우 토렌트 클라이언트와 같은 P2P 앱을 사용하는 데에 문제가 발생할 수 있습니다.

#### :material-check:{ .pg-green } Anti-Censorship

Mullvad has obfuscation an mode using [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) which may be useful in situations where VPN protocols like OpenVPN or Wireguard are blocked.

#### :material-check:{ .pg-green } 모바일 클라이언트

Mullvad has published [App Store](https://apps.apple.com/app/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. 안드로이드 클라이언트는 [Github](https://github.com/mullvad/mullvadvpn-app/releases)에서도 구할 수 있습니다.

#### :material-information-outline:{ .pg-blue } Additional Notes

Mullvad is very transparent about which nodes they [own or rent](https://mullvad.net/en/servers). They use [ShadowSocks](https://shadowsocks.org) in their ShadowSocks + OpenVPN configuration, making them more resistant against firewalls with [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) trying to block VPNs. [중국은 다른 방식으로 ShadowSocks 서버를 막고 있다고 전해집니다](https://github.com/net4people/bbs/issues/22). Mullvad의 웹사이트는 Tor를 이용해서 접속할 수 있습니다. 주소는 [o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion)입니다.

## 평가 기준

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

VPN은 익명성을 제공하지 않는다는 것을 인지하는 것은 매우 중요합니다. 다만, 특정 상황에서 더 나은 프라이버시를 제공할 수 있습니다. VPN은 불법적인 활동에 사용하는 도구가 아닙니다. "로그 없음" 정책에 의존하면 안됩니다.

</div>

**우리는 위 추천한 제공자와 그 어떤 제휴 관계에 있지 않습니다. This allows us to provide completely objective recommendations.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any VPN provider wishing to be recommended, including strong encryption, independent security audits, modern technology, and more. We suggest you familiarize yourself with this list before choosing a VPN provider, and conduct your own research to ensure the VPN provider you choose is as trustworthy as possible.

### 기술

We require all our recommended VPN providers to provide OpenVPN configuration files to be used in any client. **If** a VPN provides their own custom client, we require a killswitch to block network data leaks when disconnected.

**최소 요구 사항:**

- WireGuard와 OpenVPN과 같은 강력한 프로토콜을 지원
- 클라이언트에 킬스위치 (Killswitch)기능이 내장되어 있음
- 멀티홉을 지원함 멀티홉은 한 노드가 공격당할 경우 데이터를 지키는데에 중요하게 사용됩니다.
- If VPN clients are provided, they should be [open source](https://en.wikipedia.org/wiki/Open_source), like the VPN software they generally have built into them. We believe that [source code](https://en.wikipedia.org/wiki/Source_code) availability provides greater transparency about what your device is actually doing.

**우대 사항:**

- WireGuard 및 OpenVPN 지원
- 다양한 설정들을 가진 킬스위치 기능 (일부 네트워크에만 활성화하기, 부팅시에만 활성화하기 등)
- 사용하기 쉬운 VPN 클라이언트
- [IPv6](https://en.wikipedia.org/wiki/IPv6) 지원: 서버들은 IPv6를 통한 연결을 허용하고, IPv6 주소에 호스팅되는 서비스에 접속할 수 있도록 해야 합니다.
- [원격 포트포워딩](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding)을 지원하여 P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) 파일 공유와 Mumble과 같은 서비스 호스팅할 수 있음
- Obfuscation technology which pads data packets with random data to circumvent internet censorship.

### 프라이버시

Privacy Guides이 권장하는 제공자들은 최소한의 데이터만을 수집해야 합니다. 가입할 때 개인 정보를 수집하지 않아야 하고, 익명 결제 방식을 허용해야 합니다.

**최소 요구 사항:**

- [익명 암호화폐](cryptocurrency.md) **또는** 현금 결제 옵션
- 가입하는 데에 개인정보 입력이 필수가 아님 (사용자명, 비밀번호, 이메일만 요구)

**우대 사항:**

- 다수의 [익명 결제 수단](advanced/payments.md) 지원
- 개인 정보를 받지 않음 (자동생성된 사용자명, 이메일 불필요 등)

### 보안

적절한 보안을 제공하지 않는 VPN은 없으나마나입니다. Privacy Guides가 권장하는 모든 제공업체는 OpenVPN 연결에 대한 최신 보안 표준을 따라야 합니다. 미래에도 유효한 암호화 체계를 사용하는 것이 제일 이상적입니다. 또한, 권장하는 제공자들은 외부 감사를 꼭 받아야 하며, 포괄적이면서 주기적으로 (매년) 받는 것이 이상적입니다.

**최소 요구 사항:**

- 강력한 암호화 방식 사용: SHA-256 해시 기반 인증을 이용하는 OpenVPN, RSA-2048 또는 더 강력한 비대칭 암호 알고리즘을 이용하는 핸드셰이크, AES-256-GCM 또는 AES-256-CBC 를 이용하는 데이터 암호화
- 순방향 비밀성 제공
- 검증된 제 3자로부터 보안 감사 결과가 게시됨

**우대 사항:**

- 가장 강력한 암호화 방식으로 RSA-4096을 지원
- 순방향 비밀성 제공
- 검증된 제 3자로부터 종합적인 보안 감사 결과가 게시됨
- 버그 바운티 프로그램 또는 체계적인 취약점 공개 프로세스가 있음

### 신뢰

You wouldn't trust your finances to someone with a fake identity, so why trust them with your internet data? We require our recommended providers to be public about their ownership or leadership. We also would like to see frequent transparency reports, especially in regard to how government requests are handled.

**최소 요구 사항:**

- Public-facing leadership or ownership.

**우대 사항:**

- Public-facing leadership.
- Frequent transparency reports.

### 마케팅

Privacy Guides가 권장하는 VPN 제공 업체들은 책임감 있는 마케팅을 할 것이라고 기대하고 있습니다.

**최소 요구 사항:**

- 애널리틱스 서비스는 자체 호스팅을 해야 합니다. (Google Analytics와 같은 서비스 사용 금지) VPN 제공자의 사이트는 [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) 요구를 준수해야 합니다.

다음과 같은 무책임한 마케팅 방식을 사용하지 않아야 합니다.

- 익명성을 100% 보장해준다는 등의 내용: 만약 누군가가 100%라고 주장한다면, 이는 절대 실패할 수 없다고 하는 것과 같습니다. 익명성을 잃는 방법은 간단하면서도 다양하다는 것은 잘 알려져 있습니다. 예시로는 다음과 같습니다:
    - 익명성 소프트웨어 (Tor, VPN 등) 를 사용하지 않고 개인 정보 (이메일 계정, 온라인 아이디) 를 재사용하는 행위
    - [브라우저 핑거프린팅](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- 노드 1개만을 거치는 VPN이 주기적으로 변하는 노드 3개를 거치는 Tor보다 익명성을 보호하는데 더 좋다는 주장
- 무책임한 표현 사용 금지: 사이트에서 VPN에 "연결됨" 또는 "연결되지 않음"이라고 표시하는 것은 문제되지 않지만, VPN에 연결되지 않았을 경우 "노출됨", "취약함"과 같은 단어 표현은 필요 이상으로 사용자에게 경고를 주며, 아예 올바르지 않을 수 있습니다. 예시로, 해당 사용자는 타사의 VPN을 사용하고 있거나 Tor를 사용하고 있을 수 있습니다.

**우대 사항:**

사용자에게 유용한 책임감 있는 마케팅의 예시는 다음과 같습니다:

- [Tor](tor.md)를 사용하기 적합한 상황을 정확하게 설명함
- VPN 제공자의 웹사이트가 [.onion](https://en.wikipedia.org/wiki/.onion)으로도 접근이 가능

### 추가 기능

엄격하게 적용한 요구 사항은 아니지만, 이 외의 요소 일부 또한 고려하여 권장 제공 업체를 결정했습니다. These include content blocking functionality, warrant canaries, multihop connections, excellent customer support, the number of allowed simultaneous connections, etc.
