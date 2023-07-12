---
meta_title: "プライベートVPNサービスのおすすめと比較、スポンサーや広告なし - Privacy Guides"
title: "VPNサービス"
icon: material/vpn
description: これらは、あなたのプライバシーとセキュリティをオンラインで保護するための最高のVPNサービスです。 ここで、あなたを監視しようとしないプロバイダーを見つけてください。
cover: vpn.png
---

ISPや公共Wi-Fiネットワーク、またはファイルのTorrent中の、追加の**プライバシー保護**手段をお探しの場合で、リスクを理解している場合は、VPNはあなたにとっての解決策になるかもしれません。 以下のプロバイダは他のプロバイダと比較して洗練されていると、私たちは考えています。

<div class="grid cards" markdown>

- ![Proton VPN logo](assets/img/vpn/protonvpn.svg){ .twemoji } [Proton VPN](#proton-vpn)
- ![IVPN logo](assets/img/vpn/mini/ivpn.svg){ .twemoji } [IVPN](#ivpn)
- ![Mullvad logo](assets/img/vpn/mullvad.svg){ .twemoji } [Mullvad](#mullvad)

</div>

!!! danger "VPNを利用しても匿名性は確保できません"

    VPNを使用しても、ブラウジング習慣は匿名化**されません**。安全でない通信（HTTP）に保護が追加されることも**ありません**。
    
    **匿名性**を確保したい場合は、VPN**ではなく**Tor Browserをご利用ください。
    
    追加の**セキュリティ**を確保したい場合は、ウェブサイトへの接続に常にHTTPSを使用するのが有効です。 VPNは、優れたセキュリティ対策の代わりにはなりません。
    
    [Torをダウンロード](https://www.torproject.org/){ .md-button .md-button--primary } [Torの神話とよくある質問](advanced/tor-overview.md){ .md-button }

[VPNの詳細な概要 :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## 推奨プロバイダー

私たちがおすすめするプロバイダは、暗号化を使用し、Moneroを受け入れ、WireGuardとOpenVPNに対応し、ノーログポリシーを持っています。 詳細については、[基準の完全なリスト](#criteria)をお読みください。

### Proton VPN

!!! recommendation annotate

    ![Proton VPN logo](assets/img/vpn/protonvpn.svg){ align=right }
    
    **Proton VPN**はVPN分野の強力な候補であり、2016 年から運営されています。 Proton AGはスイスに本社を置き、限定的な無料層と、より機能的なプレミアムオプションを提供している。
    
    [:octicons-home-16: Homepage](https://protonvpn.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://protonvpn.com/support/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id1437005085)
        - [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
        - [:simple-windows11: Windows](https://protonvpn.com/download-windows)
        - [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup/)

#### :material-check:{ .pg-green } 67か国

Proton VPN has [servers in 67 countries](https://protonvpn.com/vpn-servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. This is because of a shorter route (fewer hops) to the destination.
{ .annotate }

1. Last checked: 2022-09-16

We also think it's better for the security of the VPN provider's private keys if they use [dedicated servers](https://en.wikipedia.org/wiki/Dedicated_hosting_service), instead of cheaper shared solutions (with other customers) such as [virtual private servers](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } 独立監査済み

As of January 2020, Proton VPN has undergone an independent audit by SEC Consult. SEC Consult found some medium and low risk vulnerabilities in Proton VPN's Windows, Android, and iOS applications, all of which were "properly fixed" by Proton VPN before the reports were published. None of the issues identified would have provided an attacker remote access to your device or traffic. You can view individual reports for each platform at [protonvpn.com](https://protonvpn.com/blog/open-source/). In April 2022 Proton VPN underwent [another audit](https://protonvpn.com/blog/no-logs-audit/) and the report was [produced by Securitum](https://protonvpn.com/blog/wp-content/uploads/2022/04/securitum-protonvpn-nologs-20220330.pdf). A [letter of attestation](https://proton.me/blog/security-audit-all-proton-apps) was provided for Proton VPN's apps on 9th November 2021 by [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } オープンソースクライアント

Proton VPN provides the source code for their desktop and mobile clients in their [GitHub organization](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Accepts Cash

Proton VPN, in addition to accepting credit/debit cards, PayPal, and [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), also accepts **cash/local currency** as an anonymous form of payment.

#### :material-check:{ .pg-green } WireGuard対応

Proton VPN mostly supports the WireGuard® protocol. [WireGuard](https://www.wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://www.wireguard.com/protocol/). Additionally, WireGuard aims to be simpler and more performant.

Proton VPN [recommends](https://protonvpn.com/blog/wireguard/) the use of WireGuard with their service. On Proton VPN's Windows, macOS, iOS, Android, ChromeOS, and Android TV apps, WireGuard is the default protocol; however, [support](https://protonvpn.com/support/how-to-change-vpn-protocols/) for the protocol is not present in their Linux app.

#### :material-alert-outline:{ .pg-orange } Remote Port Forwarding

Proton VPN currently only supports ephemeral remote [port forwarding](https://protonvpn.com/support/port-forwarding/) via NAT-PMP, with 60 second lease times. The Windows app provides an easy to access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup/). Torrent applications often support NAT-PMP natively.

#### :material-check:{ .pg-green } モバイルクライアント

In addition to providing standard OpenVPN configuration files, Proton VPN has mobile clients for [App Store](https://apps.apple.com/us/app/protonvpn-fast-secure-vpn/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android&hl=en_US), and [GitHub](https://github.com/ProtonVPN/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } Additional Functionality

Proton VPN clients support two factor authentication on all platforms except Linux at the moment. Proton VPN has their own servers and datacenters in Switzerland, Iceland and Sweden. They offer adblocking and known malware domains blocking with their DNS service. Additionally, Proton VPN also offers "Tor" servers allowing you to easily connect to onion sites, but we still strongly recommend using [the official Tor Browser](https://www.torproject.org/) for this purpose.

#### :material-alert-outline:{ .pg-orange } Killswitch feature is broken on Intel-based Macs

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch/) on Intel-based Macs when using the VPN killswitch. If you require this feature, and you are using a Mac with Intel chipset, you should consider using another VPN service.

### IVPN

!!! recommendation

    ![IVPN logo](assets/img/vpn/ivpn.svg){ align=right }
    
    **IVPN**はプレミアムVPNプロバイダの一つで、2009年から運営されています。 IVPNの拠点はジブラルタルです。
    
    [:octicons-home-16: Homepage](https://www.ivpn.net/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.ivpn.net/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://www.ivpn.net/knowledgebase/general/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/ivpn){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
        - [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
        - [:simple-appstore: App Store](https://apps.apple.com/app/ivpn-serious-privacy-protection/id1193122683)
        - [:simple-windows11: Windows](https://www.ivpn.net/apps-windows/)
        - [:simple-apple: macOS](https://www.ivpn.net/apps-macos/)
        - [:simple-linux: Linux](https://www.ivpn.net/apps-linux/)

#### :material-check:{ .pg-green } 35か国

IVPN has [servers in 35 countries](https://www.ivpn.net/server-locations).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. This is because of a shorter route (fewer hops) to the destination.
{ .annotate }

1. Last checked: 2022-09-16

We also think it's better for the security of the VPN provider's private keys if they use [dedicated servers](https://en.wikipedia.org/wiki/Dedicated_hosting_service), instead of cheaper shared solutions (with other customers) such as [virtual private servers](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } 独立監査済み

IVPN has undergone a [no-logging audit from Cure53](https://cure53.de/audit-report_ivpn.pdf) which concluded in agreement with IVPN's no-logging claim. IVPN has also completed a [comprehensive pentest report Cure53](https://cure53.de/summary-report_ivpn_2019.pdf) in January 2020. IVPN has also said they plan to have [annual reports](https://www.ivpn.net/blog/independent-security-audit-concluded) in the future. A further review was conducted [in April 2022](https://www.ivpn.net/blog/ivpn-apps-security-audit-2022-concluded/) and was produced by Cure53 [on their website](https://cure53.de/pentest-report_IVPN_2022.pdf).

#### :material-check:{ .pg-green } オープンソースクライアント

As of February 2020 [IVPN applications are now open-source](https://www.ivpn.net/blog/ivpn-applications-are-now-open-source). Source code can be obtained from their [GitHub organization](https://github.com/ivpn).

#### :material-check:{ .pg-green } Accepts Cash and Monero

In addition to accepting credit/debit cards and PayPal, IVPN accepts Bitcoin, **Monero** and **cash/local currency** (on annual plans) as anonymous forms of payment.

#### :material-check:{ .pg-green } WireGuard対応

IVPN supports the WireGuard® protocol. [WireGuard](https://www.wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://www.wireguard.com/protocol/). Additionally, WireGuard aims to be simpler and more performant.

IVPN [recommends](https://www.ivpn.net/wireguard/) the use of WireGuard with their service and, as such, the protocol is the default on all of IVPN's apps. IVPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://www.wireguard.com/install/).

#### :material-alert-outline:{ .pg-orange } Remote Port Forwarding

IVPN previously supported port forwarding, but removed the option in [June 2023](https://www.ivpn.net/blog/gradual-removal-of-port-forwarding). Missing this feature could negatively impact certain applications, especially peer-to-peer applications like torrent clients.

#### :material-check:{ .pg-green } モバイルクライアント

In addition to providing standard OpenVPN configuration files, IVPN has mobile clients for [App Store](https://apps.apple.com/us/app/ivpn-serious-privacy-protection/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), and [GitHub](https://github.com/ivpn/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } 追加機能

IVPN clients support two factor authentication (Mullvad's clients do not). IVPN also provides "[AntiTracker](https://www.ivpn.net/antitracker)" functionality, which blocks advertising networks and trackers from the network level.

### Mullvad

!!! recommendation

    ![Mullvad logo](assets/img/vpn/mullvad.svg){ align=right }
    
    **Mullvad**は、透明性とセキュリティに重点を置いた、高速で安価なVPNです。 **2009年**から運営されています。 Mullvadの拠点はスウェーデンで、フリートライアルはありません。
    
    [:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://mullvad.net/en/help/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/mullvad){ .card-link title="Source Code" }
    
    ??? ダウンロード
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
        - [:simple-appstore: App Store](https://apps.apple.com/app/mullvad-vpn/id1488466513)
        - [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
        - [:simple-windows11: Windows](https://mullvad.net/en/download/windows/)
        - [:simple-apple: macOS](https://mullvad.net/en/download/macos/)
        - [:simple-linux: Linux](https://mullvad.net/en/download/linux/)

#### :material-check:{ .pg-green } 41か国

Mullvad has [servers in 41 countries](https://mullvad.net/servers/).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. This is because of a shorter route (fewer hops) to the destination.
{ .annotate }

1. Last checked: 2023-01-19

We also think it's better for the security of the VPN provider's private keys if they use [dedicated servers](https://en.wikipedia.org/wiki/Dedicated_hosting_service), instead of cheaper shared solutions (with other customers) such as [virtual private servers](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } 独立監査済み

Mullvad's VPN clients have been audited by Cure53 and Assured AB in a pentest report [published at cure53.de](https://cure53.de/pentest-report_mullvad_v2.pdf). The security researchers concluded:

> Cure53 and Assured AB are happy with the results of the audit and the software leaves an overall positive impression. With security dedication of the in-house team at the Mullvad VPN compound, the testers have no doubts about the project being on the right track from a security standpoint.

In 2020 a second audit [was announced](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app/) and the [final audit report](https://cure53.de/pentest-report_mullvad_2020_v2.pdf) was made available on Cure53's website:

> The results of this May-June 2020 project targeting the Mullvad complex are quite positive. [...] The overall application ecosystem used by Mullvad leaves a sound and structured impression. The overall structure of the application makes it easy to roll out patches and fixes in a structured manner. More than anything, the findings spotted by Cure53 showcase the importance of constantly auditing and re-assessing the current leak vectors, in order to always ensure privacy of the end-users. With that being said, Mullvad does a great job protecting the end-user from common PII leaks and privacy related risks.

In 2021 an infrastructure audit [was announced](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit/) and the [final audit report](https://cure53.de/pentest-report_mullvad_2021_v1.pdf) was made available on Cure53's website. Another report was commissioned [in June 2022](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data/) and is available on [Assured's website](https://www.assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf).

#### :material-check:{ .pg-green } オープンソースクライアント

Mullvad provides the source code for their desktop and mobile clients in their [GitHub organization](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Accepts Cash and Monero

Mullvad, in addition to accepting credit/debit cards and PayPal, accepts Bitcoin, Bitcoin Cash, **Monero** and **cash/local currency** as anonymous forms of payment. They also accept Swish and bank wire transfers.

#### :material-check:{ .pg-green } WireGuard対応

Mullvad supports the WireGuard® protocol. [WireGuard](https://www.wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://www.wireguard.com/protocol/). Additionally, WireGuard aims to be simpler and more performant.

Mullvad [recommends](https://mullvad.net/en/help/why-wireguard/) the use of WireGuard with their service. It is the default or only protocol on Mullvad's Android, iOS, macOS, and Linux apps, but on Windows you have to [manually enable](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app/) WireGuard. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://www.wireguard.com/install/).

#### :material-check:{ .pg-green } IPv6 Support

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support/), as opposed to other providers which block IPv6 connections.

#### :material-alert-outline:{ .pg-orange } Remote Port Forwarding

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports/). Missing this feature could negatively impact certain applications, especially peer-to-peer applications like torrent clients.

#### :material-check:{ .pg-green } モバイルクライアント

Mullvad has published [App Store](https://apps.apple.com/app/mullvad-vpn/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } 追加機能

Mullvadは、どのノードを[所有またはレンタル](https://mullvad.net/en/servers/)しているのかについて非常に透明性があります。 They use [ShadowSocks](https://shadowsocks.org/) in their ShadowSocks + OpenVPN configuration, making them more resistant against firewalls with [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) trying to block VPNs. Supposedly, [China has to use a different method to block ShadowSocks servers](https://github.com/net4people/bbs/issues/22). Mullvad's website is also accessible via Tor at [o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion).

## 基準

!!! 危険

    It is important to note that using a VPN provider will not make you anonymous, but it will give you better privacy in certain situations. A VPN is not a tool for illegal activities. Don't rely on a "no log" policy.

**Please note we are not affiliated with any of the providers we recommend. This allows us to provide completely objective recommendations.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any VPN provider wishing to be recommended, including strong encryption, independent security audits, modern technology, and more. We suggest you familiarize yourself with this list before choosing a VPN provider, and conduct your own research to ensure the VPN provider you choose is as trustworthy as possible.

### テクノロジー

We require all our recommended VPN providers to provide OpenVPN configuration files to be used in any client. **If** a VPN provides their own custom client, we require a killswitch to block network data leaks when disconnected.

**Minimum to Qualify:**

- Support for strong protocols such as WireGuard & OpenVPN.
- Killswitch built in to clients.
- Multihop support. Multihopping is important to keep data private in case of a single node compromise.
- If VPN clients are provided, they should be [open-source](https://en.wikipedia.org/wiki/Open_source), like the VPN software they generally have built into them. We believe that [source code](https://en.wikipedia.org/wiki/Source_code) availability provides greater transparency about what your device is actually doing.

**最良の場合：**

- WireGuardとOpenVPNをサポート。
- 高度に構成可能なオプションを備えたキルスイッチ（特定のネットワークや起動時などで有効/無効）
- 使いやすいVPNクライアント
- [IPv6](https://en.wikipedia.org/wiki/IPv6)をサポートする。 サーバーがIPv6経由の着信接続を許可し、IPv6アドレスでホストされているサービスにアクセスできるようになることを期待しています。
- [リモートポート転送](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) 機能はP2P（[Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)）ファイル共有ソフトウェアの使用時やサーバー（Mumbleなど）のホスト時に接続を作成するのに役立ちます。

### プライバシー

私たちは、推奨するプロバイダーができるだけデータを収集しないことを望んでいます。 登録時に個人情報を収集しないこと、匿名の支払い方法を受け入れることが求められます。

**最低条件：**

- [匿名の仮想通貨](cryptocurrency.md)**もしくは**現金支払いオプション。
- 登録に個人情報が必要ありません。最大でもユーザー名、パスワード、電子メールのみです。

**最良の場合：**

- 複数の[匿名支払いオプション](advanced/payments.md)に対応。
- 個人情報が一切必要ありません。（自動生成されたユーザー名、電子メールは必要ないなど）

### セキュリティ

A VPN is pointless if it can't even provide adequate security. We require all our recommended providers to abide by current security standards for their OpenVPN connections. Ideally, they would use more future-proof encryption schemes by default. We also require an independent third-party to audit the provider's security, ideally in a very comprehensive manner and on a repeated (yearly) basis.

**最低条件：**

- Strong Encryption Schemes: OpenVPN with SHA-256 authentication; RSA-2048 or better handshake; AES-256-GCM or AES-256-CBC data encryption.
- Forward Secrecy.
- Published security audits from a reputable third-party firm.

**最良の場合：**

- 強力な暗号化：RSA-4096
- 前方秘匿性
- 評判の良い第三者機関による包括的な公開セキュリティ監査。
- バグ報奨金プログラムおよび/または協調的な脆弱性開示プロセス。

### 信頼

あなたは偽の身分証を持つ人物に自分の財政を託すことはないでしょう、それではなぜインターネットデータではそれらを信頼するのですか？ 推奨されるプロバイダーには、自社の所有権やリーダーシップについて公表することが求められます。 また、特に政府からの要請がどのように処理されるかについて、透明性の高い報告が頻繁に行われることを望んでいます。

**最低条件：**

- 公の場でのリーダーシップやオーナーシップ。

**最良の場合：**

- 公の場でのリーダーシップ。
- 頻繁な透明性レポート。

### マーケティング

私たちが推奨するVPNプロバイダーには、責任あるマーケティングを求めます。

**最低条件：**

- アナリティクスを自己ホストする必要があります。（つまり、Googleアナリティクスは不可） プロバイダーのサイトは、オプトアウトを希望するユーザーのために [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) に準拠しなければならない。

無責任なマーケティングをしてはいけない：

- 匿名性を100％保証すること。 誰かが何かを100％だと主張するとき、それは失敗の確実性がないことを意味します。 私たちは、人々が多くの方法で簡単に匿名化を解除できることを知っています：
    - 匿名化ソフトウェア（Tor、VPNなど）を使用せずにアクセスした個人情報（メールアカウント、固有のペンネームなど）を再利用する。
    - [ブラウザフィンガープリント](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- 単一回線のVPNは、定期的に変更される3ホップ以上の回線であるTorよりも「匿名性が高い」と主張する。
- 責任ある言葉を使用してください：つまり、VPNが「切断されている」または「接続されていない」と言うのは問題ありませんが、誰かが「公開されている」、「脆弱」、または「侵害されている」と主張することは、正しくない可能性のある憂慮すべき言葉を不必要に使用することです。 例えば、その人は単に他のVPNプロバイダーのサービスを利用しているだけかもしれないし、Torを使っているだけかもしれない。

**最良の場合：**

教育的かつ消費者にとって有用な責任あるマーケティングには以下のものがあります:

- 代わりに[Tor](tor.md)を使用する必要がある場合との正確な比較。
- [.onion サービス](https://en.wikipedia.org/wiki/.onion)を介したVPNプロバイダーのウェブサイトの利用可能性

### 追加機能

厳密な要件ではありませんが、推奨するプロバイダーを決定する際に考慮した要素がいくつかあります。 これらには、広告ブロック/トラッカーブロッキング機能、令状のカナリア、マルチホップ接続、優れたカスタマーサポート、許可される同時接続数などが含まれます。
