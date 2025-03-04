---
meta_title: "プライベートVPNサービスの推奨事項と比較、スポンサーや広告なし - Privacy Guides"
title: "VPNサービス"
icon: material/vpn
description: The best VPN services for protecting your privacy and security online. Find a provider here that isn't out to spy on you.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Surveillance Capitalism](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

If you're looking for additional *privacy* from your ISP, on a public Wi-Fi network, or while torrenting files, a **VPN** may be the solution for you.

<div class="admonition danger" markdown>
<p class="admonition-title">VPNs do not provide anonymity</p>

Using a VPN will **not** keep your browsing habits anonymous, nor will it add additional security to non-secure (HTTP) traffic.

If you are looking for **anonymity**, you should use the Tor Browser. If you're looking for added **security**, you should always ensure you're connecting to websites using HTTPS. VPNは、優れたセキュリティーの代わりにはなりません。

[Download Tor](https://torproject.org){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[VPNの詳細な概要 :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## 推奨するサービスプロバイダー

Our recommended providers use encryption, support WireGuard & OpenVPN, and have a no logging policy. 詳細については、[基準の完全なリスト](#criteria)をお読みください。

| Provider              | Countries | WireGuard                     | Port Forwarding                                        | IPv6                                                       | Anonymous Payments |
| --------------------- | --------- | ----------------------------- | ------------------------------------------------------ | ---------------------------------------------------------- | ------------------ |
| [Proton](#proton-vpn) | 112+      | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Partial Support | :material-information-outline:{ .pg-blue } Limited Support | 現金                 |
| [IVPN](#ivpn)         | 37+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                 | :material-information-outline:{ .pg-blue } Outgoing Only   | Monero, Cash       |
| [Mullvad](#mullvad)   | 45+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                 | :material-check:{ .pg-green }                              | Monero, Cash       |

### Proton VPN

<div class="admonition recommendation" markdown>

![Proton VPN ロゴ](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN**はVPNの分野において強力なサービスプロバイダーであり、2016年から運営されています。 Proton AGはスイスに本社を置き、機能が限定された無料枠と、より多くの機能を備えたプレミアムオプションを提供しています。

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

Proton VPN has [servers in 112 countries](https://protonvpn.com/vpn-servers) or [5](https://protonvpn.com/support/how-to-create-free-vpn-account) if you use their [free plan](https://protonvpn.com/free-vpn/server).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. これは目的地までのルートが短い(ホップが少ない) ことによります。
{ .annotate }

1. Last checked: 2024-08-06

また、VPNプロバイダの秘密鍵のセキュリティを考えると、できれば[バーチャルプライベートサーバー](https://en.wikipedia.org/wiki/Virtual_private_server)のような安価な(他の顧客との)共有ソリューションではなく[専用サーバー](https://en.wikipedia.org/wiki/Dedicated_hosting_service)を使用したほうがいいと考えています。

#### :material-check:{ .pg-green } 独立監査済み

2020年1月時点で、Proton VPNはSEC Consultによる独立監査を受けました。 SEC ConsultはProton VPNのWindows、Android、iOSアプリに中、低リスクの脆弱性を発見しましたが、これらすべてはProton VPNによって報告書が公表される前に「適切に修正」されました。 確認された問題はいずれも攻撃者がデバイスやトラフィックへリモートアクセスを可能にするものではありませんでした。 You can view individual reports for each platform at [protonvpn.com](https://protonvpn.com/blog/open-source). In April 2022 Proton VPN underwent [another audit](https://protonvpn.com/blog/no-logs-audit). 2021年11月9日に[Securitum](https://research.securitum.com)から [監査証明書](https://proton.me/blog/security-audit-all-proton-apps) がProton VPNアプリに対して提供されました。

#### :material-check:{ .pg-green } オープンソースクライアント

Proton VPNはデスクトップおよびモバイルクライアントのソースコードを[GitHub organization](https://github.com/ProtonVPN)で提供しています。

#### :material-check:{ .pg-green } 現金の受け入れ

Proton VPNはクレジットおよびデビットカード、PayPal、そして[Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc)に加え、さらに**現金および現地通貨**を匿名での支払い方法として受け入れています。

#### :material-check:{ .pg-green } WireGuard対応

Proton VPN supports the WireGuard® protocol. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). 加えて、WireGuardはよりシンプルかつより高性能であることを目指しています。

Proton VPN [recommends](https://protonvpn.com/blog/wireguard) the use of WireGuard with their service. Proton VPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-alert-outline:{ .pg-orange } Limited IPv6 Support

Proton [now supports IPv6](https://protonvpn.com/support/prevent-ipv6-vpn-leaks) in their browser extension but only 80% of their servers are IPv6-compatible. On other platforms, the Proton VPN client will block all outgoing IPv6 traffic, so you don't have to worry about your IPv6 address being leaked, but you will not be able to connect to any IPv6-only sites, nor will you be able to connect to Proton VPN from an IPv6-only network.

#### :material-information-outline:{ .pg-info } Remote Port Forwarding

Proton VPN currently only supports ephemeral remote [port forwarding](https://protonvpn.com/support/port-forwarding) via NAT-PMP, with 60 second lease times. The Windows app provides an easy-to-access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup). Torrentアプリは多くの場合NAT-PMPをネイティブサポートしています。

#### :material-information-outline:{ .pg-blue } Anti-Censorship

Proton VPN has their [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) protocol which *may* help in situations where VPN protocols like OpenVPN or WireGuard are blocked with various rudimentary techniques. Stealth encapsulates the VPN tunnel in TLS session in order to look like more generic internet traffic.

Unfortunately, it does not work very well in countries where sophisticated filters that analyze all outgoing traffic in an attempt to discover encrypted tunnels are deployed. Stealth is available on Android, iOS, Windows, and macOS, but it's not yet available on Linux.

#### :material-check:{ .pg-green } モバイルクライアント

In addition to providing standard OpenVPN configuration files, Proton VPN has mobile clients for [App Store](https://apps.apple.com/app/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android), and [GitHub](https://github.com/ProtonVPN/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } Additional Notes

Proton VPN clients support two-factor authentication on all platforms. Proton VPNはスイス、アイスランド、スウェーデンに独自のサーバーとデータセンターを持っています。 They offer content blocking and known-malware blocking with their DNS service. Additionally, Proton VPN also offers "Tor" servers allowing you to easily connect to onion sites, but we still strongly recommend using [the official Tor Browser](tor.md#tor-browser) for this purpose.

##### :material-alert-outline:{ .pg-orange } Kill switch feature is broken on Intel-based Macs

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch) on Intel-based Macs when using the VPN kill switch. この機能が必要で、Intelチップセットを搭載したMacを使用している場合は別のVPNサービスの利用を検討する必要があります。

### IVPN

<div class="admonition recommendation" markdown>

![IVPN logo](assets/img/vpn/ivpn.svg){ align=right }

**IVPN**はプレミアムVPNプロバイダの一つで、2009年から運営されています。 IVPN is based in Gibraltar and does not offer a free trial.

[:octicons-home-16: Homepage](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:fontawesome-brands-windows: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 37 Countries

IVPN has [servers in 37 countries](https://ivpn.net/status).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. これは目的地までのルートが短い(ホップが少ない) ことによります。
{ .annotate }

1. Last checked: 2024-08-06

また、VPNプロバイダの秘密鍵のセキュリティを考えると、できれば[バーチャルプライベートサーバー](https://en.wikipedia.org/wiki/Virtual_private_server)のような安価な(他の顧客との)共有ソリューションではなく[専用サーバー](https://en.wikipedia.org/wiki/Dedicated_hosting_service)を使用したほうがいいと考えています。

#### :material-check:{ .pg-green } 独立監査済み

IVPN has had multiple [independent audits](https://ivpn.net/en/blog/tags/audit) since 2019 and has publicly announced their commitment to [annual security audits](https://ivpn.net/blog/ivpn-apps-security-audit-concluded).

#### :material-check:{ .pg-green } オープンソースクライアント

As of February 2020 [IVPN applications are now open source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). Source code can be obtained from their [GitHub organization](https://github.com/ivpn).

#### :material-check:{ .pg-green } 現金とMoneroが利用可能

In addition to accepting credit/debit cards and PayPal, IVPN accepts Bitcoin, **Monero** and **cash/local currency** (on annual plans) as anonymous forms of payment. Prepaid cards with redeem codes are [also available](https://ivpn.net/knowledgebase/billing/voucher-cards-faq).

#### :material-check:{ .pg-green } WireGuard対応

IVPNはWireGuard®️プロトコルをサポートしています。 [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). 加えて、WireGuardはよりシンプルかつより高性能であることを目指しています。

IVPN [recommends](https://ivpn.net/wireguard) the use of WireGuard with their service and, as such, the protocol is the default on all of IVPN's apps. IVPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-information-outline:{ .pg-blue } IPv6 Support

IVPN allows you to [connect to services using IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6) but doesn't allow you to connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } リモートポートフォワーディング

IVPN previously supported port forwarding, but removed the option in [June 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). Missing this feature could negatively impact certain applications, especially peer-to-peer applications like torrent clients.

#### :material-check:{ .pg-green } Anti-Censorship

IVPN has obfuscation modes using [v2ray](https://v2ray.com/en/index.html) which helps in situations where VPN protocols like OpenVPN or WireGuard are blocked. Currently, this feature is only available on Desktop and [iOS](https://ivpn.net/knowledgebase/ios/v2ray). It has two modes where it can use [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) over QUIC or TCP connections. QUIC is a modern protocol with better congestion control and therefore may be faster with reduced latency. The TCP mode makes your data appear as regular HTTP traffic.

#### :material-check:{ .pg-green } モバイルクライアント

In addition to providing standard OpenVPN configuration files, IVPN has mobile clients for [App Store](https://apps.apple.com/app/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), and [GitHub](https://github.com/ivpn/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } Additional Notes

IVPN clients support two-factor authentication. IVPN also provides "[AntiTracker](https://ivpn.net/antitracker)" functionality, which blocks advertising networks and trackers from the network level.

### Mullvad

<div class="admonition recommendation" markdown>

![Mullvad ロゴ](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad**は、透明性とセキュリティに重点を置いた、高速で安価なVPNです。 They have been in operation since 2009. Mullvad is based in Sweden and offers a 14-day money-back guarantee for [payment methods](https://mullvad.net/en/help/refunds) that allow it.

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

#### :material-check:{ .pg-green } 45 Countries

Mullvad has [servers in 45 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. これは目的地までのルートが短い(ホップが少ない) ことによります。
{ .annotate }

1. Last checked: 2024-08-06

また、VPNプロバイダの秘密鍵のセキュリティを考えると、できれば[バーチャルプライベートサーバー](https://en.wikipedia.org/wiki/Virtual_private_server)のような安価な(他の顧客との)共有ソリューションではなく[専用サーバー](https://en.wikipedia.org/wiki/Dedicated_hosting_service)を使用したほうがいいと考えています。

#### :material-check:{ .pg-green } 独立監査済み

Mullvad has had multiple [independent audits](https://mullvad.net/en/blog/tag/audits) and has publicly announced their endeavors to conduct [annual audits](https://mullvad.net/en/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) of their apps and infrastructure.

#### :material-check:{ .pg-green } オープンソースクライアント

Mullvad provides the source code for their desktop and mobile clients in their [GitHub organization](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } 現金とMoneroが利用可能

Mullvad, in addition to accepting credit/debit cards and PayPal, accepts Bitcoin, Bitcoin Cash, **Monero** and **cash/local currency** as anonymous forms of payment. Prepaid cards with redeem codes are also available. Mullvad also accepts Swish and bank wire transfers, as well as a few European payment systems.

#### :material-check:{ .pg-green } WireGuard対応

MullvadはWireGuard®️プロトコルをサポートしています。 [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). 加えて、WireGuardはよりシンプルかつより高性能であることを目指しています。

Mullvad [recommends](https://mullvad.net/en/help/why-wireguard) the use of WireGuard with their service. It is the default or only protocol on Mullvad's Android, iOS, macOS, and Linux apps, but on Windows you have to [manually enable](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-check:{ .pg-green } IPv6のサポート

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) and connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } リモートポートフォワーディング

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). Missing this feature could negatively impact certain applications, especially peer-to-peer applications like torrent clients.

#### :material-check:{ .pg-green } Anti-Censorship

Mullvad offers several features to help bypass censorship and access the internet freely:

- **Obfuscation modes**: Mullvad has two built-in obfuscation modes: "UDP-over-TCP" and ["WireGuard over Shadowsocks"](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard). These modes disguise your VPN traffic as regular web traffic, making it harder for censors to detect and block. Supposedly, China has to use a [new method to disrupt Shadowsocks-routed traffic](https://gfw.report/publications/usenixsecurity23/en).
- **Advanced obfuscation with Shadowsocks and v2ray**: For more advanced users, Mullvad provides a guide on how to use the [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) plugin with Mullvad clients. This setup provides an additional layer of obfuscation and encryption.
- **Custom server IPs**: To counter IP-blocking, you can request custom server IPs from Mullvad's support team. Once you receive the custom IPs, you can input the text file in the "Server IP override" settings, which will override the chosen server IP addresses with ones that aren't known to the censor.
- **Bridges and proxies**: Mullvad also allows you to use bridges or proxies to reach their API (needed for authentication), which can help bypass censorship attempts that block access to the API itself.

#### :material-check:{ .pg-green } モバイルクライアント

Mullvad has published [App Store](https://apps.apple.com/app/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Additional Notes

Mullvad is very transparent about which nodes they [own or rent](https://mullvad.net/en/servers). They also provide the option to enable Defense Against AI-guided Traffic Analysis ([DAITA](https://mullvad.net/en/blog/daita-defense-against-ai-guided-traffic-analysis)) in their apps. DAITA protects against the threat of advanced traffic analysis which can be used to connect patterns in VPN traffic with specific websites.

## 規準

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

VPNプロバイダーを利用すると、特定の状況下ではより良いプライバシーが得られますが、VPNプロバイダーは匿名性を与えるものではないことに注意が必要です。 VPNは違法行為のためのツールではありません。 「ログなし」ポリシーに依存しないでください。

</div>

**私たちは、推奨するいずれのプロバイダーとも提携していません。 This allows us to provide completely objective recommendations.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any VPN provider wishing to be recommended, including strong encryption, independent security audits, modern technology, and more. プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

### テクノロジー

We require all our recommended VPN providers to provide standard configuration files which can be used in a generic, open-source client. **If** a VPN provides their own custom client, we require a kill switch to block network data leaks when disconnected.

**最低条件：**

- Support for strong protocols such as WireGuard.
- Kill switch built in to clients.
- Multi-hop support. Multi-hopping is important to keep data private in case of a single node compromise.
- If VPN clients are provided, they should be [open source](https://en.wikipedia.org/wiki/Open_source), like the VPN software they generally have built into them. We believe that [source code](https://en.wikipedia.org/wiki/Source_code) availability provides greater transparency about what the program is actually doing.
- Censorship resistance features designed to bypass firewalls without DPI.

**満たされることが望ましい基準：**

- Kill switch with highly configurable options (enable/disable on certain networks, on boot, etc.)
- 使いやすいVPNクライアントであること。
- [IPv6](https://en.wikipedia.org/wiki/IPv6) support. サーバーがIPv6経由の着信接続を許可し、IPv6アドレスでホストされているサービスにアクセスできることが望ましい。
- [リモートポート転送](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding)機能が備わっていること。リモートポート転送機能は、P2P（[Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)）ファイル共有ソフトウェアを使用していたり、サーバー（Mumbleなど）をホストしていたりする際に接続を確立することを支援するものです。
- Obfuscation technology which camouflages the true nature of internet traffic, designed to circumvent advanced internet censorship methods like DPI.

### プライバシー

私たちは、推奨するサービスプロバイダーができるだけデータを収集しないことを望んでいます。 登録時に個人情報を収集しないこと、また、匿名の支払い方法を受け入れることが必要です。

**最低条件：**

- [匿名の暗号通貨](cryptocurrency.md)**もしくは**現金支払いオプションがあること。
- 登録に個人情報を必要としないこと。必要とする場合でもユーザー名、パスワード、電子メールを超えないこと。

**満たされることが望ましい基準：**

- 複数の[匿名支払いオプション](advanced/payments.md)に対応していること。
- No personal information accepted (auto-generated username, no email required, etc.).

### セキュリティー

A VPN is pointless if it can't even provide adequate security. We require all our recommended providers to abide by current security standards. Ideally, they would use more future-proof encryption schemes by default. We also require an independent third-party to audit the provider's security, ideally in a very comprehensive manner and on a repeated (yearly) basis.

**最低条件：**

- 強力な暗号化スキーム: SHA-256認証、RSA-2048以上のハンドシェイク、AES-256-GCMまたはAES-256-CBCによるデータ暗号化を使用したOpenVPN
- 前方秘匿性があること。
- 信頼できる第三者機関によるセキュリティ監査を公表
- VPN servers that use full-disk encryption or are RAM-only.

**満たされることが望ましい基準：**

- 強力な暗号化：RSA-4096
- Optional quantum-resistant encryption.
- 前方秘匿性があること。
- 信頼できる第三者機関による包括的な公開セキュリティ監査。
- バグ報奨金プログラム、協調的な脆弱性開示プロセス。
- RAM-only VPN servers.

### 信頼

あなたは偽の身分証を持つ人物に自分の財政を託すことはないでしょう。インターネットのデータに関しても、同じことが言えるはずです。 推奨されるサービスプロバイダーには、自社の所有権やリーダーシップについて公表することが求められます。 また、特に政府からの要請がどのように処理されるかについて、透明性の高い報告が頻繁に行われることを望んでいます。

**最低条件：**

- 公的なリーダーシップまたはオーナーシップ。
- Company based in a jurisdiction where it cannot be forced to do secret logging.

**満たされることが望ましい基準：**

- 公的なリーダーシップ。
- 頻繁な透明性レポート。

### マーケティング

私たちが推奨するVPNプロバイダーには、責任あるマーケティングを求めます。

**最低条件：**

- Must self-host analytics (i.e., no Google Analytics).

無責任なマーケティングを行わないこと。

- 匿名性を100％保証するという主張。 誰かが何かを100％だと主張するとき、それは失敗の確実性が全く存在しないということを意味します。 私たちは、人々が以下のような多くの方法で簡単に匿名化を解除できることを知っています。
    - 匿名化ソフトウェア（Tor、VPNなど）を使用せずにアクセスした個人情報（メールアカウント、固有のペンネームなど）を再利用すること。
    - [ブラウザーのフィンガープリンティングを行うこと。](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- 単一回線のVPNが、定期的に変更される3ホップ以上の回線であるTorよりも「匿名性が高い」という主張。
- 責任ある言葉遣いをしてください。VPNが「切断されている」または「接続されていない」と表現するのは問題ありませんが、誰かが「公開されている」とか「脆弱である」、または「侵害されている」と主張するのは、警戒感を煽る言葉を不必要に、しかも誤った可能性のある仕方で使用しているにすぎません。 例えば、その人は単に他のVPNプロバイダーのサービスを利用していたり、Torを使ったりしているだけかもしれません。

**満たされることが望ましい基準：**

教育的かつ消費者にとって有用で責任あるマーケティングには、以下のものがあります。

- 代わりに[Tor](tor.md)を使用する必要がある場合との正確な比較を行うこと。
- [.onion サービス](https://en.wikipedia.org/wiki/.onion)を介してVPNプロバイダーのウェブサイトを閲覧できること。

### 追加機能

厳密な要件ではありませんが、推奨するサービスプロバイダーを決定する際に考慮した要素がいくつかあります。 These include content blocking functionality, warrant canaries, excellent customer support, the number of allowed simultaneous connections, etc.
