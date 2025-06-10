---
meta_title: "비공개 VPN 서비스 권장 목록 및 각 서비스 비교 (스폰서/광고 없음) - Privacy Guides"
title: "VPN 서비스"
icon: 자료/Vpn
description: The best VPN services for protecting your privacy and security online. Find a provider here that isn't out to spy on you.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: 감시 자본주의(Surveillance Capitalism)](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

If you're looking for additional *privacy* from your ISP, on a public Wi-Fi network, or while torrenting files, a **VPN** may be the solution for you.

<div class="admonition danger" markdown>
<p class="admonition-title">VPNs do not provide anonymity</p>

Using a VPN will **not** keep your browsing habits anonymous, nor will it add additional security to non-secure (HTTP) traffic.

If you are looking for **anonymity**, you should use the Tor Browser. If you're looking for added **security**, you should always ensure you're connecting to websites using HTTPS. VPN은 올바른 보안 관행을 대체할 수 없습니다.

[Download Tor](https://torproject.org){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[VPN에 대해서 :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## 권장 제공 업체

Privacy Guides 권장 제공 업체는 암호화 사용, WireGuard & OpenVPN 지원, 노 로그 정책을 가지고 있습니다. 자세한 사항은 [전체 평가 기준](#criteria)을 참고해 주세요.

| 서비스 제공자               | 국가   | WireGuard                     | 포트포워딩                                                  | IPv6                                                       | 익명 결제   |
| --------------------- | ---- | ----------------------------- | ------------------------------------------------------ | ---------------------------------------------------------- | ------- |
| [Proton](#proton-vpn) | 112+ | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Partial Support | :material-information-outline:{ .pg-blue } Limited Support | 현금      |
| [IVPN](#ivpn)         | 37+  | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                 | :material-information-outline:{ .pg-blue } Outgoing Only   | 모네로, 현금 |
| [Mullvad](#mullvad)   | 49+  | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                 | :material-check:{ .pg-green }                              | 모네로, 현금 |

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
- [:fontawesome-brands-windows: Windows](https://protonvpn.com/download-windows)
- [:simple-apple: macOS](https://protonvpn.com/download-macos)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 112 Countries

Proton VPN has [servers in 112 countries](https://protonvpn.com/vpn-servers) or [5](https://protonvpn.com/support/how-to-create-free-vpn-account) if you use their [free plan](https://protonvpn.com/free-vpn/server).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. 목적지까지의 경로가 더 짧기(Hop 횟수가 적기) 때문입니다.
{ .annotate }

1. Last checked: 2024-08-06

우리는 VPN 제공자가 독립적인 [데디케이티드 서버](https://en.wikipedia.org/wiki/Dedicated_hosting_service)를 사용하는 것이 제공자의 개인 키를 보호하는데 더 좋다고 봅니다. [개인 사설 서버](https://en.wikipedia.org/wiki/Virtual_private_server)는 더 싸지만, VPN 제공자는 한 서버를 다른 사람들과 같이 쓰게 됩니다.

#### :material-check:{ .pg-green } 독립 감사 여부

2020년 1월에 Proton VPN은 SEC Consult로부터 독립 감사를 받았습니다. SEC Consult는 Proton VPN의 Windows, Android와 iOS 클라이언트에서 취약점을 찾았으며, 이 취약점들은 감사 레포트가 공개되기 전에 모두 적절히 고쳤다고 합니다. 확인된 취약점 중에서 공격자가 사용자의 기기 또는 트래픽에 원격으로 접속하는 것을 허용하는 것은 없습니다. You can view individual reports for each platform at [protonvpn.com](https://protonvpn.com/blog/open-source). In April 2022 Proton VPN underwent [another audit](https://protonvpn.com/blog/no-logs-audit). A [letter of attestation](https://proton.me/blog/security-audit-all-proton-apps) was provided for Proton VPN's apps on 9th November 2021 by [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } 오픈 소스 클라이언트

Proton VPN 데스크톱, 모바일 클라이언트는 [GitHub](https://github.com/ProtonVPN)에 공개되어 있습니다.

#### :material-check:{ .pg-green } 현금 결제 가능

Proton VPN은 신용카드, 체크카드, 페이팔 외에도 [비트코인](advanced/payments.md#other-coins-bitcoin-ethereum-etc)과 **현금** 결제도 받습니다.

#### :material-check:{ .pg-green } WireGuard 지원

Proton VPN supports the WireGuard® protocol. [WireGuard](https://wireguard.com)는 최첨단 [암호화](https://wireguard.com/protocol)를 사용하는 최신 프로토콜입니다. 또한, WireGuard는 보다 단순하면서도 더 나은 성능을 목표로 합니다.

Proton VPN은 자신들의 서비스에서 WireGuard 사용을 [권장](https://protonvpn.com/blog/wireguard)합니다. Proton VPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-alert-outline:{ .pg-orange } Limited IPv6 Support

Proton [now supports IPv6](https://protonvpn.com/support/prevent-ipv6-vpn-leaks) in their browser extension and Linux client, but only 80% of their servers are IPv6-compatible. On other platforms, the Proton VPN client will block all outgoing IPv6 traffic, so you don't have to worry about your IPv6 address being leaked, but you will not be able to connect to any IPv6-only sites, nor will you be able to connect to Proton VPN from an IPv6-only network.

#### :material-information-outline:{ .pg-info } Remote Port Forwarding

Proton VPN currently only supports ephemeral remote [port forwarding](https://protonvpn.com/support/port-forwarding) via NAT-PMP, with 60 second lease times. The official Windows and Linux apps provide an easy-to-access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup). 토렌트 애플리케이션은 대부분 NAT-PMP를 지원합니다.

#### :material-information-outline:{ .pg-blue } Anti-Censorship

Proton VPN has their [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) protocol which *may* help in situations where VPN protocols like OpenVPN or WireGuard are blocked with various rudimentary techniques. Stealth encapsulates the VPN tunnel in TLS session in order to look like more generic internet traffic.

Unfortunately, it does not work very well in countries where sophisticated filters that analyze all outgoing traffic in an attempt to discover encrypted tunnels are deployed. Stealth is available on Android, iOS, Windows, and macOS, but it's not yet available on Linux.

#### :material-check:{ .pg-green } 모바일 클라이언트

Proton VPN has published [App Store](https://apps.apple.com/app/id1437005085) and [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/ProtonVPN/android-app/releases).

<div class="admonition warning" markdown>
<p class="admonition-title">How to opt out of sharing telemetry</p>

On Android, Proton hides telemetry settings under the misleadingly labeled "**Help us fight censorship**" menu in the settings panel. On other platforms these settings can be found under the "**Usage statistics**" menu.

We are noting this because while we don't necessarily recommend against sharing anonymous usage statistics with developers, it is important that these settings are easily found and clearly labeled.

</div>

#### :material-information-outline:{ .pg-blue } Additional Notes

Proton VPN clients support two-factor authentication on all platforms. Proton VPN은 스위스, 아이슬란드와 스웨덴에 자체 서버와 데이터 센터를 보유하고 있습니다. They offer content blocking and known-malware blocking with their DNS service. Additionally, Proton VPN also offers "Tor" servers allowing you to easily connect to onion sites, but we still strongly recommend using [the official Tor Browser](tor.md#tor-browser) for this purpose.

##### :material-alert-outline:{ .pg-orange } Kill switch feature is broken on Intel-based Macs

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch) on Intel-based Macs when using the VPN kill switch. 만약 이 기능이 필요하지만 Intel 기반 Mac을 사용하고 있다면, 다른 VPN 서비스를 사용하는 것을 추천합니다.

### IVPN

<div class="admonition recommendation" markdown>

![IVPN 로고](assets/img/vpn/ivpn.svg){ align=right }

**IVPN**은 유료 VPN 서비스 제공 업체입니다. 2009년부터 운영되었습니다. IVPN은 지브롤터에 위치해 있으며 무료 평가판을 제공하지 않습니다.

[:octicons-home-16: Homepage](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-github: GitHub](https://github.com/ivpn/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 37 Countries

IVPN has [servers in 37 countries](https://ivpn.net/status).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. 목적지까지의 경로가 더 짧기(Hop 횟수가 적기) 때문입니다.
{ .annotate }

1. Last checked: 2024-08-06

우리는 VPN 제공자가 독립적인 [데디케이티드 서버](https://en.wikipedia.org/wiki/Dedicated_hosting_service)를 사용하는 것이 제공자의 개인 키를 보호하는데 더 좋다고 봅니다. [개인 사설 서버](https://en.wikipedia.org/wiki/Virtual_private_server)는 더 싸지만, VPN 제공자는 한 서버를 다른 사람들과 같이 쓰게 됩니다.

#### :material-check:{ .pg-green } 독립 감사 여부

IVPN has had multiple [independent audits](https://ivpn.net/en/blog/tags/audit) since 2019 and has publicly announced their commitment to [annual security audits](https://ivpn.net/blog/ivpn-apps-security-audit-concluded).

#### :material-check:{ .pg-green } 오픈 소스 클라이언트

As of February 2020 [IVPN applications are now open source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). 소스 코드는 IVPN [GitHub](https://github.com/ivpn)에서 찾아볼 수 있습니다.

#### :material-check:{ .pg-green } 현금 및 Monero 결제 가능

In addition to accepting credit/debit cards and PayPal, IVPN accepts Bitcoin, **Monero** and **cash/local currency** (on annual plans) as anonymous forms of payment. Prepaid cards with redeem codes are [also available](https://ivpn.net/knowledgebase/billing/voucher-cards-faq).

#### :material-check:{ .pg-green } WireGuard 지원

IVPN은 WireGuard® 프로토콜을 지원합니다. [WireGuard](https://wireguard.com)는 최첨단 [암호화](https://wireguard.com/protocol)를 사용하는 최신 프로토콜입니다. 또한, WireGuard는 보다 단순하면서도 더 나은 성능을 목표로 합니다.

IVPN [recommends](https://ivpn.net/wireguard) the use of WireGuard with their service and, as such, the protocol is the default on all of IVPN's apps. IVPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-information-outline:{ .pg-blue } IPv6 지원

IVPN allows you to [connect to services using IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6) but doesn't allow you to connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } 원격 포트 포워딩

IVPN previously supported port forwarding, but removed the option in [June 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). 이 기능이 없을 경우 토렌트 클라이언트와 같은 P2P 앱을 사용하는 데에 문제가 발생할 수 있습니다.

#### :material-check:{ .pg-green } Anti-Censorship

IVPN has obfuscation modes using [V2Ray](https://v2ray.com/en/index.html) which helps in situations where VPN protocols like OpenVPN or WireGuard are blocked. Currently, this feature is only available on Desktop and [iOS](https://ivpn.net/knowledgebase/ios/v2ray). It has two modes where it can use [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) over QUIC or TCP connections. QUIC is a modern protocol with better congestion control and therefore may be faster with reduced latency. The TCP mode makes your data appear as regular HTTP traffic.

#### :material-check:{ .pg-green } 모바일 클라이언트

IVPN has published [App Store](https://apps.apple.com/app/id1193122683) and [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/ivpn/android-app/releases).

#### :material-information-outline:{ .pg-blue } Additional Notes

IVPN clients support two-factor authentication. IVPN also provides "[AntiTracker](https://ivpn.net/antitracker)" functionality, which blocks advertising networks and trackers from the network level.

### Mullvad

<div class="admonition recommendation" markdown>

![Mullvad 로고](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** 투명성과 보안에 중점을 둔, 속도가 빠르면서 비싸지 않은 VPN입니다. They have been in operation since 2009. Mullvad is based in Sweden and offers a 14-day money-back guarantee for [payment methods](https://mullvad.net/en/help/refunds) that allow it.

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
- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 49 Countries

Mullvad has [servers in 49 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. 목적지까지의 경로가 더 짧기(Hop 횟수가 적기) 때문입니다.
{ .annotate }

1. Last checked: 2025-03-10

우리는 VPN 제공자가 독립적인 [데디케이티드 서버](https://en.wikipedia.org/wiki/Dedicated_hosting_service)를 사용하는 것이 제공자의 개인 키를 보호하는데 더 좋다고 봅니다. [개인 사설 서버](https://en.wikipedia.org/wiki/Virtual_private_server)는 더 싸지만, VPN 제공자는 한 서버를 다른 사람들과 같이 쓰게 됩니다.

#### :material-check:{ .pg-green } 독립 감사 여부

Mullvad has had multiple [independent audits](https://mullvad.net/en/blog/tag/audits) and has publicly announced their endeavors to conduct [annual audits](https://mullvad.net/en/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) of their apps and infrastructure.

#### :material-check:{ .pg-green } 오픈 소스 클라이언트

Mullvad 데크스톱, 모바일 클라이언트 소스 코드는 [GitHub](https://github.com/mullvad/mullvadvpn-app)에 공개되어 있습니다.

#### :material-check:{ .pg-green } 현금 및 Monero 결제 가능

Mullvad, in addition to accepting credit/debit cards and PayPal, accepts Bitcoin, Bitcoin Cash, **Monero** and **cash/local currency** as anonymous forms of payment. Prepaid cards with redeem codes are also available. Mullvad also accepts Swish and bank wire transfers, as well as a few European payment systems.

#### :material-check:{ .pg-green } WireGuard 지원

Mullvad는 WireGuard® 프로토콜을 지원합니다. [WireGuard](https://wireguard.com)는 최첨단 [암호화](https://wireguard.com/protocol)를 사용하는 최신 프로토콜입니다. 또한, WireGuard는 보다 단순하면서도 더 나은 성능을 목표로 합니다.

Mullvad [recommends](https://mullvad.net/en/help/why-wireguard) the use of WireGuard with their service. It is the default or only protocol on Mullvad's Android, iOS, macOS, and Linux apps, but on Windows you have to [manually enable](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-check:{ .pg-green } IPv6 지원

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) and connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } 원격 포트 포워딩

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). 이 기능이 없을 경우 토렌트 클라이언트와 같은 P2P 앱을 사용하는 데에 문제가 발생할 수 있습니다.

#### :material-check:{ .pg-green } Anti-Censorship

Mullvad offers several features to help bypass censorship and access the internet freely:

- **Obfuscation modes**: Mullvad has two built-in obfuscation modes: "UDP-over-TCP" and ["WireGuard over Shadowsocks"](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard). These modes disguise your VPN traffic as regular web traffic, making it harder for censors to detect and block. Supposedly, China has to use a [new method to disrupt Shadowsocks-routed traffic](https://gfw.report/publications/usenixsecurity23/en).
- **Advanced obfuscation with Shadowsocks and v2ray**: For more advanced users, Mullvad provides a guide on how to use the [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) plugin with Mullvad clients. This setup provides an additional layer of obfuscation and encryption.
- **Custom server IPs**: To counter IP-blocking, you can request custom server IPs from Mullvad's support team. Once you receive the custom IPs, you can input the text file in the "Server IP override" settings, which will override the chosen server IP addresses with ones that aren't known to the censor.
- **Bridges and proxies**: Mullvad also allows you to use bridges or proxies to reach their API (needed for authentication), which can help bypass censorship attempts that block access to the API itself.

#### :material-check:{ .pg-green } 모바일 클라이언트

Mullvad has published [App Store](https://apps.apple.com/app/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. 안드로이드 클라이언트는 [Github](https://github.com/mullvad/mullvadvpn-app/releases)에서도 구할 수 있습니다.

#### :material-information-outline:{ .pg-blue } Additional Notes

Mullvad is very transparent about which nodes they [own or rent](https://mullvad.net/en/servers). They also provide the option to enable Defense Against AI-guided Traffic Analysis ([DAITA](https://mullvad.net/en/blog/daita-defense-against-ai-guided-traffic-analysis)) in their apps. DAITA protects against the threat of advanced traffic analysis which can be used to connect patterns in VPN traffic with specific websites.

## 평가 기준

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

VPN은 익명성을 제공하지 않는다는 것을 인지하는 것은 매우 중요합니다. 다만, 특정 상황에서 더 나은 프라이버시를 제공할 수 있습니다. VPN은 불법적인 활동에 사용하는 도구가 아닙니다. "로그 없음" 정책에 의존하면 안됩니다.

</div>

**우리는 위 추천한 제공자와 그 어떤 제휴 관계에 있지 않습니다. This allows us to provide completely objective recommendations.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any VPN provider wishing to be recommended, including strong encryption, independent security audits, modern technology, and more. We suggest you familiarize yourself with this list before choosing a VPN provider, and conduct your own research to ensure the VPN provider you choose is as trustworthy as possible.

### 기술

We require all our recommended VPN providers to provide standard configuration files which can be used in a generic, open-source client. **If** a VPN provides their own custom client, we require a kill switch to block network data leaks when disconnected.

**최소 요구 사항:**

- Support for strong protocols such as WireGuard.
- Kill switch built in to clients.
- Multi-hop support. Multi-hopping is important to keep data private in case of a single node compromise.
- If VPN clients are provided, they should be [open source](https://en.wikipedia.org/wiki/Open_source), like the VPN software they generally have built into them. We believe that [source code](https://en.wikipedia.org/wiki/Source_code) availability provides greater transparency about what the program is actually doing.
- Censorship resistance features designed to bypass firewalls without DPI.

**우대 사항:**

- Kill switch with highly configurable options (enable/disable on certain networks, on boot, etc.)
- 사용하기 쉬운 VPN 클라이언트
- [IPv6](https://en.wikipedia.org/wiki/IPv6) support. 서버들은 IPv6를 통한 연결을 허용하고, IPv6 주소에 호스팅되는 서비스에 접속할 수 있도록 해야 합니다.
- [원격 포트포워딩](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding)을 지원하여 P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) 파일 공유와 Mumble과 같은 서비스 호스팅할 수 있음
- Obfuscation technology which camouflages the true nature of internet traffic, designed to circumvent advanced internet censorship methods like DPI.

### 프라이버시

Privacy Guides이 권장하는 제공자들은 최소한의 데이터만을 수집해야 합니다. 가입할 때 개인 정보를 수집하지 않아야 하고, 익명 결제 방식을 허용해야 합니다.

**최소 요구 사항:**

- [익명 암호화폐](cryptocurrency.md) **또는** 현금 결제 옵션
- 가입하는 데에 개인정보 입력이 필수가 아님 (사용자명, 비밀번호, 이메일만 요구)

**우대 사항:**

- 다수의 [익명 결제 수단](advanced/payments.md) 지원
- No personal information accepted (auto-generated username, no email required, etc.).

### 보안

적절한 보안을 제공하지 않는 VPN은 없으나마나입니다. We require all our recommended providers to abide by current security standards. 미래에도 유효한 암호화 체계를 사용하는 것이 제일 이상적입니다. 또한, 권장하는 제공자들은 외부 감사를 꼭 받아야 하며, 포괄적이면서 주기적으로 (매년) 받는 것이 이상적입니다.

**최소 요구 사항:**

- 강력한 암호화 방식 사용: SHA-256 해시 기반 인증을 이용하는 OpenVPN, RSA-2048 또는 더 강력한 비대칭 암호 알고리즘을 이용하는 핸드셰이크, AES-256-GCM 또는 AES-256-CBC 를 이용하는 데이터 암호화
- 순방향 비밀성 제공
- 검증된 제 3자로부터 보안 감사 결과가 게시됨
- VPN servers that use full-disk encryption or are RAM-only.

**우대 사항:**

- 가장 강력한 암호화 방식으로 RSA-4096을 지원
- Optional quantum-resistant encryption.
- 순방향 비밀성 제공
- 검증된 제 3자로부터 종합적인 보안 감사 결과가 게시됨
- 버그 바운티 프로그램 또는 체계적인 취약점 공개 프로세스가 있음
- RAM-only VPN servers.

### 신뢰

You wouldn't trust your finances to someone with a fake identity, so why trust them with your internet data? We require our recommended providers to be public about their ownership or leadership. We also would like to see frequent transparency reports, especially in regard to how government requests are handled.

**최소 요구 사항:**

- Public-facing leadership or ownership.
- Company based in a jurisdiction where it cannot be forced to do secret logging.

**우대 사항:**

- Public-facing leadership.
- Frequent transparency reports.

### 마케팅

Privacy Guides가 권장하는 VPN 제공 업체들은 책임감 있는 마케팅을 할 것이라고 기대하고 있습니다.

**최소 요구 사항:**

- Must self-host analytics (i.e., no Google Analytics).

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

엄격하게 적용한 요구 사항은 아니지만, 이 외의 요소 일부 또한 고려하여 권장 제공 업체를 결정했습니다. These include content blocking functionality, warrant canaries, excellent customer support, the number of allowed simultaneous connections, etc.
