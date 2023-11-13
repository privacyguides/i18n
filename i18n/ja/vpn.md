---
meta_title: "プライベートVPNサービスのおすすめと比較。スポンサーは広告はありません - Privacy Guides"
title: "VPNサービス"
icon: material/vpn
description: これらは、あなたのプライバシーとセキュリティをオンラインで保護するための最も優れたVPNサービスです。 スパイ目的でないVPNサービスプロパイダーをここで見つけましょう。
cover: vpn.webp
---

ISPや公共Wi-Fiネットワークから**プライバシー**をより一層保護したい場合、またはファイルをTorrentで送受信している際にそうしたい場合、リスクを理解している限りで、VPNはあなたにとっての解決策になる可能性があります。 以下のプロバイダは他のプロバイダと比較して洗練されていると、私たちは考えています。

<div class="grid cards" markdown>

- ![Proton VPN ロゴ](assets/img/vpn/protonvpn.svg){ .twemoji } [Proton VPN](#proton-vpn)
- ![IVPN ロゴ](assets/img/vpn/mini/ivpn.svg){ .twemoji } [IVPN](#ivpn)
- ![Mullvad ロゴ](assets/img/vpn/mullvad.svg){ .twemoji } [Mullvad](#mullvad)

</div>

!!! danger "VPNは匿名性を提供しません"

    VPNを使用しても、ブラウジング習慣を匿名化したり、安全でない通信（HTTP）へのセキュリティーが強化されたりすることは**ありません**。
    
    **匿名性**を確保するには、VPNの**代わりに**Tor Browserを使用してください。
    
    **セキュリティー**を強化するには、ウェブサイトへの接続に常にHTTPSを使用してください。 VPNは、優れたセキュリティーの代わりにはなりません。
    
    [Torをダウンロード](https://www.torproject.org/){ .md-button .md-button--primary } [Torの神話とよくある質問](advanced/tor-overview.md){ .md-button }

[VPNの詳細な概要 :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## 推奨するサービスプロバイダー

私たちがおすすめするプロバイダは、暗号化を使用し、Moneroを受け入れ、WireGuardとOpenVPNに対応し、ノーログポリシーを備えています。 詳細については、[基準の完全なリスト](#criteria)をお読みください。

### Proton VPN

!!! recommendation annotate

    ![Proton VPN ロゴ](assets/img/vpn/protonvpn.svg){ align=right }
    
    **Proton VPN**はVPNの分野において強力なサービスプロバイダーであり、2016年から運営されています。 Proton AGはスイスに本社を置き、機能が限定された無料枠と、より多くの機能を備えたプレミアムオプションを提供しています。
    
    [:octicons-home-16: ホームページ](https://protonvpn.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="プライバシーポリシー" }
    [:octicons-info-16:](https://protonvpn.com/support/){ .card-link title=ドキュメント}
    [:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="ソースコード" }
    
    ??? ダウンロード
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
        - [:simple-appstore: App Store](https://apps.apple.com/jp/app/apple-store/id1437005085)
        - [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
        - [:simple-windows11: Windows](https://protonvpn.com/download-windows)
        - [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup/)

#### :material-check:{ .pg-green } 68か国

Proton VPNは[68カ国にサーバー](https://protonvpn.com/vpn-servers)を所有しており、(1) VPNプロバイダを最寄りのサーバに選択することで送信するネットワークトラフィックのレイテンシが軽減されます。 これは目的地までのルートが短い(ホップが少ない) ことによります。
{ .annotate }

1. 最終確認: 2023-07-28

また、VPNプロバイダの秘密鍵のセキュリティを考えると、できれば[バーチャルプライベートサーバー](https://en.wikipedia.org/wiki/Virtual_private_server)のような安価な(他の顧客との)共有ソリューションではなく[専用サーバー](https://en.wikipedia.org/wiki/Dedicated_hosting_service)を使用したほうがいいと考えています。

#### :material-check:{ .pg-green } 独立監査済み

2020年1月時点で、Proton VPNはSEC Consultによる独立監査を受けました。 SEC ConsultはProton VPNのWindows、Android、iOSアプリに中、低リスクの脆弱性を発見しましたが、これらすべてはProton VPNによって報告書が公表される前に「適切に修正」されました。 確認された問題はいずれも攻撃者がデバイスやトラフィックへリモートアクセスを可能にするものではありませんでした。 [protonvpn.com](https://protonvpn.com/blog/open-source/)で各プラットフォームの個別レポートを確認できます。 2022年4月、Proton VPNは[別の監査](https://protonvpn.com/blog/no-logs-audit/)を受け、報告書が[Securitumによって作成されました。](https://protonvpn.com/blog/wp-content/uploads/2022/04/securitum-protonvpn-nologs-20220330.pdf) 2021年11月9日に[Securitum](https://research.securitum.com)から [監査証明書](https://proton.me/blog/security-audit-all-proton-apps) がProton VPNアプリに対して提供されました。

#### :material-check:{ .pg-green } オープンソースクライアント

Proton VPNはデスクトップおよびモバイルクライアントのソースコードを[GitHub organization](https://github.com/ProtonVPN)で提供しています。

#### :material-check:{ .pg-green } 現金の受け入れ

Proton VPNはクレジットおよびデビットカード、PayPal、そして[Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc)に加え、さらに**現金および現地通貨**を匿名での支払い方法として受け入れています。

#### :material-check:{ .pg-green } WireGuard対応

Proton VPNは主にWireGuard®プロトコルをサポートしています。 [WireGuard](https://www.wireguard.com)は最先端の[暗号化](https://www.wireguard.com/protocol/)を使用する新しいプロトコルです。 加えて、WireGuardはよりシンプルかつより高性能であることを目指しています。

Proton VPNはそのサービスでWireGuardを使用することを[推奨](https://protonvpn.com/blog/wireguard/)しています。 Proton VPNのWindows、macOS、iOS、Android、ChromeOS、Android TVアプリではWireGuardがデフォルトのプロトコルになっています。しかし、Linuxアプリではこのプロトコルが[サポート](https://protonvpn.com/support/how-to-change-vpn-protocols/)されていません。

#### :material-alert-outline:{ .pg-orange } リモートポートフォワーディング

Proton VPNは現在NAT-PMP経由で、リース時間は60秒の一時的なリモート[ポートフォワーディング](https://protonvpn.com/support/port-forwarding/)のみをサポートしています。 Windowsアプリにはそれに簡単にアクセスできるオプションがありますが、他のオペレーティングシステムでは独自の[NAT-PMPクライアント](https://protonvpn.com/support/port-forwarding-manual-setup/)を実行する必要があります。 Torrentアプリは多くの場合NAT-PMPをネイティブサポートしています。

#### :material-check:{ .pg-green } モバイルクライアント

標準的なOpenVPN構成ファイルに加えて、Proton VPNは[App Store](https://apps.apple.com/us/app/protonvpn-fast-secure-vpn/id1437005085)、[Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android&hl=en_US)、そして[GitHub](https://github.com/ProtonVPN/android-app/releases)用にモバイルクライアントを用意しており、サーバーへの簡単な接続を可能にしています。

#### :material-information-outline:{ .pg-blue } 追加機能

Proton VPNクライアントは現時点でLinuxを除くすべてのプラットフォームで2要素認証をサポートしています。 Proton VPNはスイス、アイスランド、スウェーデンに独自のサーバーとデータセンターを持っています。 Proton VPNはDNSサービスで広告ブロックと既知のマルウェアドメインブロックを提供しています。 さらに、Proton VPNは「Tor」サーバーも提供しており、簡単にonionサイトへ接続することができますが、それには[公式Tor Browser](https://www.torproject.org/)の使用を強くおすすめします。

#### :material-alert-outline:{ .pg-orange } IntelベースのMacではキルスイッチ機能が正常に動作しません。

VPNキルスイッチを使用しているとき、IntelベースのMacではシステムクラッシュが[発生する可能性があります。](https://protonvpn.com/support/macos-t2-chip-kill-switch/) この機能が必要で、Intelチップセットを搭載したMacを使用している場合は別のVPNサービスの利用を検討する必要があります。

### IVPN

!!! recommendation

    ![IVPN logo](assets/img/vpn/ivpn.svg){ align=right }
    
    **IVPN**はプレミアムVPNプロバイダの一つで、2009年から運営されています。 IVPNの拠点はジブラルタルです。
    
    [:octicons-home-16: ホームページ](https://www.ivpn.net/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.ivpn.net/privacy/){ .card-link title="プライバシーポリシー" }
    [:octicons-info-16:](https://www.ivpn.net/knowledgebase/general/){ .card-link title=ドキュメント}
    [:octicons-code-16:](https://github.com/ivpn){ .card-link title="ソースコード" }
    
    ??? ダウンロード
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
        - [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
        - [:simple-appstore: App Store](https://apps.apple.com/app/ivpn-serious-privacy-protection/id1193122683)
        - [:simple-windows11: Windows](https://www.ivpn.net/apps-windows/)
        - [:simple-apple: macOS](https://www.ivpn.net/apps-macos/)
        - [:simple-linux: Linux](https://www.ivpn.net/apps-linux/)

#### :material-check:{ .pg-green } 35か国

IVPNは[35カ国にサーバー](https://www.ivpn.net/server-locations)を所有しており、(1) VPNプロバイダを最寄りのサーバに選択することで送信するネットワークトラフィックのレイテンシが軽減されます。 これは目的地までのルートが短い(ホップが少ない) ことによります。
{ .annotate }

1. 最終確認: 2023-07-28

また、VPNプロバイダの秘密鍵のセキュリティを考えると、できれば[バーチャルプライベートサーバー](https://en.wikipedia.org/wiki/Virtual_private_server)のような安価な(他の顧客との)共有ソリューションではなく[専用サーバー](https://en.wikipedia.org/wiki/Dedicated_hosting_service)を使用したほうがいいと考えています。

#### :material-check:{ .pg-green } 独立監査済み

IVPN has undergone a [no-logging audit from Cure53](https://cure53.de/audit-report_ivpn.pdf) which concluded in agreement with IVPN's no-logging claim. IVPN has also completed a [comprehensive pentest report Cure53](https://cure53.de/summary-report_ivpn_2019.pdf) in January 2020. IVPN has also said they plan to have [annual reports](https://www.ivpn.net/blog/independent-security-audit-concluded) in the future. A further review was conducted [in April 2022](https://www.ivpn.net/blog/ivpn-apps-security-audit-2022-concluded/) and was produced by Cure53 [on their website](https://cure53.de/pentest-report_IVPN_2022.pdf).

#### :material-check:{ .pg-green } オープンソースクライアント

As of February 2020 [IVPN applications are now open source](https://www.ivpn.net/blog/ivpn-applications-are-now-open-source). Source code can be obtained from their [GitHub organization](https://github.com/ivpn).

#### :material-check:{ .pg-green } 現金とMoneroが利用可能

In addition to accepting credit/debit cards and PayPal, IVPN accepts Bitcoin, **Monero** and **cash/local currency** (on annual plans) as anonymous forms of payment.

#### :material-check:{ .pg-green } WireGuard対応

IVPNはWireGuard®️プロトコルをサポートしています。 [WireGuard](https://www.wireguard.com)は最先端の[暗号化](https://www.wireguard.com/protocol/)を使用する新しいプロトコルです。 加えて、WireGuardはよりシンプルかつより高性能であることを目指しています。

IVPN [recommends](https://www.ivpn.net/wireguard/) the use of WireGuard with their service and, as such, the protocol is the default on all of IVPN's apps. IVPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://www.wireguard.com/install/).

#### :material-alert-outline:{ .pg-orange } リモートポートフォワーディング

IVPN previously supported port forwarding, but removed the option in [June 2023](https://www.ivpn.net/blog/gradual-removal-of-port-forwarding). Missing this feature could negatively impact certain applications, especially peer-to-peer applications like torrent clients.

#### :material-check:{ .pg-green } モバイルクライアント

In addition to providing standard OpenVPN configuration files, IVPN has mobile clients for [App Store](https://apps.apple.com/us/app/ivpn-serious-privacy-protection/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), and [GitHub](https://github.com/ivpn/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } 追加機能

IVPN clients support two factor authentication (Mullvad's clients do not). IVPN also provides "[AntiTracker](https://www.ivpn.net/antitracker)" functionality, which blocks advertising networks and trackers from the network level.

### Mullvad

!!! recommendation

    ![Mullvad ロゴ](assets/img/vpn/mullvad.svg){ align=right }
    
    **Mullvad**は、透明性とセキュリティに重点を置いた、高速で安価なVPNです。 **2009年**から運営されています。 Mullvadの拠点はスウェーデンで、フリートライアルはありません。
    
    [:octicons-home-16: ホームページ](https://mullvad.net/ja){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://mullvad.net/ja/help/privacy-policy/){ .card-link title="プライバシーポリシー" }
    [:octicons-info-16:](https://mullvad.net/ja/help/){ .card-link title=ドキュメント}
    [:octicons-code-16:](https://github.com/mullvad){ .card-link title="ソースコード" }
    
    ??? ダウンロード
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
        - [:simple-appstore: App Store](https://apps.apple.com/jp/app/mullvad-vpn/id1488466513)
        - [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
        - [:simple-windows11: Windows](https://mullvad.net/ja/download/vpn/windows)
        - [:simple-apple: macOS](https://mullvad.net/ja/download/vpn/macos)
        - [:simple-linux: Linux](https://mullvad.net/ja/download/vpn/linux)

#### :material-check:{ .pg-green } 43か国

Mullvadは[43カ国にサーバー](https://mullvad.net/servers/)を所有しており、(1) VPNプロバイダを最寄りのサーバに選択することで送信するネットワークトラフィックのレイテンシが軽減されます。 これは目的地までのルートが短い(ホップが少ない) ことによります。
{ .annotate }

1. 最終確認: 2023-07-28

また、VPNプロバイダの秘密鍵のセキュリティを考えると、できれば[バーチャルプライベートサーバー](https://en.wikipedia.org/wiki/Virtual_private_server)のような安価な(他の顧客との)共有ソリューションではなく[専用サーバー](https://en.wikipedia.org/wiki/Dedicated_hosting_service)を使用したほうがいいと考えています。

#### :material-check:{ .pg-green } 独立監査済み

MullvadのVPNクライアントはCure53とAssured ABによる[cure53.deに公開された](https://cure53.de/pentest-report_mullvad_v2.pdf)ペンテストレポートで監査を受けました。 セキュリティ研究者たちは以下のように結論づけました:

> Cure53とAssured ABは監査の結果に満足しており、このソフトウェアは全体的に好印象を残した。 With security dedication of the in-house team at the Mullvad VPN compound, the testers have no doubts about the project being on the right track from a security standpoint.

In 2020 a second audit [was announced](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app/) and the [final audit report](https://cure53.de/pentest-report_mullvad_2020_v2.pdf) was made available on Cure53's website:

> The results of this May-June 2020 project targeting the Mullvad complex are quite positive. [...] The overall application ecosystem used by Mullvad leaves a sound and structured impression. The overall structure of the application makes it easy to roll out patches and fixes in a structured manner. More than anything, the findings spotted by Cure53 showcase the importance of constantly auditing and re-assessing the current leak vectors, in order to always ensure privacy of the end-users. With that being said, Mullvad does a great job protecting the end-user from common PII leaks and privacy related risks.

In 2021 an infrastructure audit [was announced](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit/) and the [final audit report](https://cure53.de/pentest-report_mullvad_2021_v1.pdf) was made available on Cure53's website. Another report was commissioned [in June 2022](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data/) and is available on [Assured's website](https://www.assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf).

#### :material-check:{ .pg-green } オープンソースクライアント

Mullvad provides the source code for their desktop and mobile clients in their [GitHub organization](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } 現金とMoneroが利用可能

Mullvad, in addition to accepting credit/debit cards and PayPal, accepts Bitcoin, Bitcoin Cash, **Monero** and **cash/local currency** as anonymous forms of payment. They also accept Swish and bank wire transfers.

#### :material-check:{ .pg-green } WireGuard対応

MullvadはWireGuard®️プロトコルをサポートしています。 [WireGuard](https://www.wireguard.com)は最先端の[暗号化](https://www.wireguard.com/protocol/)を使用する新しいプロトコルです。 加えて、WireGuardはよりシンプルかつより高性能であることを目指しています。

Mullvad [recommends](https://mullvad.net/en/help/why-wireguard/) the use of WireGuard with their service. It is the default or only protocol on Mullvad's Android, iOS, macOS, and Linux apps, but on Windows you have to [manually enable](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app/) WireGuard. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://www.wireguard.com/install/).

#### :material-check:{ .pg-green } IPv6のサポート

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support/), as opposed to other providers which block IPv6 connections.

#### :material-alert-outline:{ .pg-orange } リモートポートフォワーディング

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports/). Missing this feature could negatively impact certain applications, especially peer-to-peer applications like torrent clients.

#### :material-check:{ .pg-green } モバイルクライアント

Mullvad has published [App Store](https://apps.apple.com/app/mullvad-vpn/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } 追加機能

Mullvadには、どのノードを[所有またはレンタル](https://mullvad.net/en/servers/)しているのかに関する非常に高い透明性があります。 They use [ShadowSocks](https://shadowsocks.org/) in their ShadowSocks + OpenVPN configuration, making them more resistant against firewalls with [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) trying to block VPNs. Supposedly, [China has to use a different method to block ShadowSocks servers](https://github.com/net4people/bbs/issues/22). Mullvad's website is also accessible via Tor at [o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion).

## 規準

!!! 警告

    VPNプロバイダーを利用すると、特定の状況下ではより良いプライバシーが得られますが、VPNプロバイダーは匿名性を与えるものではないことに注意が必要です。 VPNは違法行為のためのツールではありません。 「ログなし」ポリシーに依存しないでください。

**私たちは、推奨するいずれのプロバイダーとも提携していません。 This allows us to provide completely objective recommendations.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any VPN provider wishing to be recommended, including strong encryption, independent security audits, modern technology, and more. プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

### テクノロジー

We require all our recommended VPN providers to provide OpenVPN configuration files to be used in any client. **If** a VPN provides their own custom client, we require a killswitch to block network data leaks when disconnected.

**最低条件：**

- Support for strong protocols such as WireGuard & OpenVPN.
- Killswitch built in to clients.
- Multihop support. Multihopping is important to keep data private in case of a single node compromise.
- If VPN clients are provided, they should be [open source](https://en.wikipedia.org/wiki/Open_source), like the VPN software they generally have built into them. We believe that [source code](https://en.wikipedia.org/wiki/Source_code) availability provides greater transparency about what your device is actually doing.

**満たされることが望ましい基準：**

- WireGuardとOpenVPNをサポートしていること。
- 高度に構成可能なオプションを備えたキルスイッチ（特定のネットワークや起動時などで有効/無効）があること。
- 使いやすいVPNクライアントであること。
- [IPv6](https://en.wikipedia.org/wiki/IPv6)をサポートしていること。 サーバーがIPv6経由の着信接続を許可し、IPv6アドレスでホストされているサービスにアクセスできることが望ましい。
- [リモートポート転送](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding)機能が備わっていること。リモートポート転送機能は、P2P（[Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)）ファイル共有ソフトウェアを使用していたり、サーバー（Mumbleなど）をホストしていたりする際に接続を確立することを支援するものです。

### プライバシー

私たちは、推奨するサービスプロバイダーができるだけデータを収集しないことを望んでいます。 登録時に個人情報を収集しないこと、また、匿名の支払い方法を受け入れることが必要です。

**最低条件：**

- [匿名の暗号通貨](cryptocurrency.md)**もしくは**現金支払いオプションがあること。
- 登録に個人情報を必要としないこと。必要とする場合でもユーザー名、パスワード、電子メールを超えないこと。

**満たされることが望ましい基準：**

- 複数の[匿名支払いオプション](advanced/payments.md)に対応していること。
- 個人情報を一切要求しないこと（ユーザー名の自動生成を行ったり、電子メールを不要としたりすること）。

### セキュリティー

A VPN is pointless if it can't even provide adequate security. We require all our recommended providers to abide by current security standards for their OpenVPN connections. Ideally, they would use more future-proof encryption schemes by default. We also require an independent third-party to audit the provider's security, ideally in a very comprehensive manner and on a repeated (yearly) basis.

**最低条件：**

- 強力な暗号化スキーム: SHA-256認証、RSA-2048以上のハンドシェイク、AES-256-GCMまたはAES-256-CBCによるデータ暗号化を使用したOpenVPN
- 前方秘匿性があること。
- 信頼できる第三者機関によるセキュリティ監査を公表

**満たされることが望ましい基準：**

- 強力な暗号化：RSA-4096
- 前方秘匿性があること。
- 信頼できる第三者機関による包括的な公開セキュリティ監査。
- バグ報奨金プログラム、協調的な脆弱性開示プロセス。

### 信頼

あなたは偽の身分証を持つ人物に自分の財政を託すことはないでしょう。インターネットのデータに関しても、同じことが言えるはずです。 推奨されるサービスプロバイダーには、自社の所有権やリーダーシップについて公表することが求められます。 また、特に政府からの要請がどのように処理されるかについて、透明性の高い報告が頻繁に行われることを望んでいます。

**最低条件：**

- 公的なリーダーシップまたはオーナーシップ。

**満たされることが望ましい基準：**

- 公的なリーダーシップ。
- 頻繁な透明性レポート。

### マーケティング

私たちが推奨するVPNプロバイダーには、責任あるマーケティングを求めます。

**最低条件：**

- アナリティクスを自己でホストすること（つまり、Googleアナリティクスは不可）。 プロバイダーのサイトは、オプトアウトを希望するユーザーのために[DNT（Do Not Track）](https://en.wikipedia.org/wiki/Do_Not_Track)に準拠しなければなりません。

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

厳密な要件ではありませんが、推奨するサービスプロバイダーを決定する際に考慮した要素がいくつかあります。 これらには、広告ブロックやトラッカーブロッキングの機能、令状のカナリア、マルチホップ接続、優れたカスタマーサポート、許可される同時接続数などが含まれます。
