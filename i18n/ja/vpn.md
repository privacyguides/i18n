---
meta_title: "プライベートVPNサービスの推奨事項と比較、スポンサーや広告なし - Privacy Guides"
title: "VPNサービス"
icon: material/vpn
description: オンラインでのプライバシーとセキュリティを保護するための最良のVPNサービス。 ひそかにあなたを監視することがないVPNサービスプロバイダーを挙げています。
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>以下の脅威から保護します：</small>

- [:material-account-cash: 監視資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

ISPや公衆Wi-Fiから*プライバシー*をさらに保護したい場合やP2Pソフトを使う際にそうしたい場合、**VPN**を使うことは良い方法になります。

<div class="admonition danger" markdown>
<p class="admonition-title">VPNでは匿名性を確保することはできません</p>

VPNを使用しても、ブラウジング傾向を匿名化したり、安全ではない（HTTP）通信のセキュリティが強化されたりすることは**ありません**。

**匿名性**を確保するには、Tor Browserを使用してください。 **セキュリティ**を強化するには、常にウェブサイトへの接続にHTTPSを使用してください。 VPNは、優れたセキュリティーの代わりにはなりません。

[Torのダウンロード](https://torproject.org){ .md-button .md-button--primary } [Tor神話とよくある質問](advanced/tor-overview.md){ .md-button }

</div>

[VPNの詳細な概要 :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## 推奨するサービスプロバイダー

推奨するプロバイダーは暗号化され、WireGuardとOpenVPNへ対応し、ノーログポリシーがあります。 詳細については、[基準の完全なリスト](#criteria)をお読みください。

| プロバイダー                | サーバーロケーション国数 | WireGuard                     | ポートフォワーディング                                 | IPv6                                                       | 匿名での支払い   |
| --------------------- | ------------ | ----------------------------- | ------------------------------------------- | ---------------------------------------------------------- | --------- |
| [Proton](#proton-vpn) | 112以上        | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } 一部対応 | :material-information-outline:{ .pg-blue } 制限あり            | 現金        |
| [IVPN](#ivpn)         | 37以上         | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }      | :material-information-outline:{ .pg-blue } アウトバウンドトラフィックのみ | Monero、現金 |
| [Mullvad](#mullvad)   | 45以上         | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }      | :material-check:{ .pg-green }                              | Monero、現金 |

### Proton VPN

<div class="admonition recommendation" markdown>

![Proton VPN ロゴ](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN**はVPNの分野において強力なサービスプロバイダーであり、2016年から運営されています。 Proton AGはスイスに本社を置き、機能が限定された無料枠と、より多くの機能を備えたプレミアムオプションを提供しています。

[:octicons-home-16: ウェブページ](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="プライバシーポリシー" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title=ドキュメント}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="ソースコード" }

<details class="downloads" markdown>
<summary>ダウンロード</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://protonvpn.com/download-windows)
- [:simple-apple: macOS](https://protonvpn.com/download-macos)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 112カ国

Proton VPNは[112カ国にサーバーを設置しています](https://protonvpn.com/vpn-servers)。[free plan](https://protonvpn.com/free-vpn/server)は[5カ国](https://protonvpn.com/support/how-to-create-free-vpn-account)のみです。(1) VPNプロバイダーの最も近いサーバーを選ぶことで、ネットワークトラフィックのレイテンシーを小さくすることができます。 これは目的地までのルートが短い(ホップが少ない) ことによります。
{ .annotate }

1. 最終確認：2024-08-06

また、VPNプロバイダの秘密鍵のセキュリティを考えると、できれば[バーチャルプライベートサーバー](https://en.wikipedia.org/wiki/Virtual_private_server)のような安価な(他の顧客との)共有ソリューションではなく[専用サーバー](https://en.wikipedia.org/wiki/Dedicated_hosting_service)を使用したほうがいいと考えています。

#### :material-check:{ .pg-green } 独立監査済み

2020年1月時点で、Proton VPNはSEC Consultによる独立監査を受けました。 SEC ConsultはProton VPNのWindows、Android、iOSアプリに中、低リスクの脆弱性を発見しましたが、これらすべてはProton VPNによって報告書が公表される前に「適切に修正」されました。 確認された問題はいずれも攻撃者がデバイスやトラフィックへリモートアクセスを可能にするものではありませんでした。 [protonvpn.com](https://protonvpn.com/blog/open-source)で各プラットフォーム個別のレポートを見ることができます。 2022年4月にProton VPNは[別の監査](https://protonvpn.com/blog/no-logs-audit)を受けました。 2021年11月9日に[Securitum](https://research.securitum.com)から [監査証明書](https://proton.me/blog/security-audit-all-proton-apps) がProton VPNアプリに対して提供されました。

#### :material-check:{ .pg-green } オープンソースクライアント

Proton VPNはデスクトップおよびモバイルクライアントのソースコードを[GitHub organization](https://github.com/ProtonVPN)で提供しています。

#### :material-check:{ .pg-green } 現金の受け入れ

Proton VPNはクレジットおよびデビットカード、PayPal、そして[Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc)に加え、さらに**現金および現地通貨**を匿名での支払い方法として受け入れています。

#### :material-check:{ .pg-green } WireGuard対応

Proton VPNはWireGuard®プロトコルに対応しています。 [Wireguard](https://wireguard.com)は最先端の[暗号化技術](https://wireguard.com/protocol)を用いた新しいプロトコルです。 加えて、WireGuardはよりシンプルかつより高性能であることを目指しています。

Proton VPNはWireGuardを用いることを[推奨](https://protonvpn.com/blog/wireguard)しています。 また、Proton VPNでは公式のWireGuard[アプリ](https://wireguard.com/install)で使用するWireGuard設定を作成できます。

#### :material-alert-outline:{ .pg-orange } IPv6の対応は制限あり

Protonはブラウザの拡張機能とLinux向けクライアントで[現在、IPv6に対応しています](https://protonvpn.com/support/prevent-ipv6-vpn-leaks)が、IPv6に対応したサーバーは80%のみです。 他のプラットフォームではProtonVPNクライアントはすべてのIPv6のアウトバウンドトラフィックをブロックするため、使用しているIPv6アドレスが漏れる心配はありませんが、IPv6専用のサイトには接続できず、IPv6専用ネットワークからProtonVPNに接続することもできません。

#### :material-information-outline:{ .pg-info } リモートポートフォワーディング

Proton VPNでは、NAT-PMP経由の60秒でリリースされる一時的なリモート[ポートフォワーディング](https://protonvpn.com/support/port-forwarding)のみ対応しています。 公式のWindows・Linuxアプリでは簡単に設定することができますが、他のOSでは[NAT-PMPクライアント](https://protonvpn.com/support/port-forwarding-manual-setup)を自分で実行する必要があります。 Torrentアプリは多くの場合NAT-PMPをネイティブサポートしています。

#### :material-information-outline:{ .pg-blue } 検閲への対抗

Proton VPNにはOpenVPNもしくはWireGuardのようなVPNプロトコルを様々な初歩的な技術でブロックすることを防ぐ*可能性のある *[Stealth](https://protonvpn.com/blog/stealth-vpn-protocol)プロトコルがあります。 StealthではTLSセッションにおけるVPNトンネルをカプセル化し、他の通常のインターネットトラフィックのように見せかけます。

残念ながら、暗号化されたトンネルを見つけるためにすべてのアウトバウンドトラフィックを分析するような、より高度なフィルタを使う国ではあまり有効ではありません。 StealthはAndroid、iOS、WindowsとmacOSで利用可能ですが、Linuxではまだ利用できません。

#### :material-check:{ .pg-green } モバイルクライアント

Proton VPNは[App Store](https://apps.apple.com/app/id1437005085)と[Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)でクライアントをダウンロードでき、どちらもWireGuard接続を手動で設定する必要がなく、使いやすいインターフェースがあります。 Android向けのクライアントは[GitHub](https://github.com/ProtonVPN/android-app/releases)でも公開されています。

#### :material-information-outline:{ .pg-blue } 追記事項

Proton VPNクライアントはすべてのプラットフォームで二要素認証に対応しています。 Proton VPNはスイス、アイスランド、スウェーデンに独自のサーバーとデータセンターを持っています。 DNSサービスで広告ブロックと既知のマルウェアブロックをしています。 また、Proton VPNにはonionサイトに簡単に接続することのできるTorサーバーがありますが、[公式のTor Browser](tor.md#tor-browser)の使用を強く推奨します。

##### :material-alert-outline:{ .pg-orange } キルスイッチ機能はIntelベースのMacでは正常に機能しない

VPNキルスイッチを使っている際、システムクラッシュが[発生する可能性があります](https://protonvpn.com/support/macos-t2-chip-kill-switch)。 この機能が必要で、Intelチップセットを搭載したMacを使用している場合は別のVPNサービスの利用を検討する必要があります。

### IVPN

<div class="admonition recommendation" markdown>

![IVPN logo](assets/img/vpn/ivpn.svg){ align=right }

**IVPN**はプレミアムVPNプロバイダの一つで、2009年から運営されています。 IVPNはジブラルタルに拠点があり、無料トライアルはありません。

[:octicons-home-16: ウェブページ](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="プライバシーポリシー" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title=ドキュメント}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="ソースコード" }

<details class="downloads" markdown>
<summary>ダウンロード</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:fontawesome-brands-windows: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 37カ国

IVPNは[37カ国にサーバー](https://ivpn.net/status)を設置しています。(1) VPNプロバイダーの最も近いサーバーを選ぶことで、ネットワークトラフィックのレイテンシーを小さくすることができます。 これは目的地までのルートが短い(ホップが少ない) ことによります。
{ .annotate }

1. 最終確認：2024-08-06

また、VPNプロバイダの秘密鍵のセキュリティを考えると、できれば[バーチャルプライベートサーバー](https://en.wikipedia.org/wiki/Virtual_private_server)のような安価な(他の顧客との)共有ソリューションではなく[専用サーバー](https://en.wikipedia.org/wiki/Dedicated_hosting_service)を使用したほうがいいと考えています。

#### :material-check:{ .pg-green } 独立監査済み

IVPNは2019年から複数の[独立した監査](https://ivpn.net/en/blog/tags/audit)を受けており、[1年ごとのセキュリティ監査](https://ivpn.net/blog/ivpn-apps-security-audit-concluded)を受けることを公表しています。

#### :material-check:{ .pg-green } オープンソースクライアント

2020年2月時点で[IVPNのアプリケーションはオープンソースとなっています](https://ivpn.net/blog/ivpn-applications-are-now-open-source)。 ソースコードは[GitHub](https://github.com/ivpn)から入手できます。

#### :material-check:{ .pg-green } 現金とMoneroが利用可能

IVPNはクレジット・デビットカードやPayPalでの支払いに加え、匿名での支払い手段としてBitcoinや**Monero**と**現金・現地通貨**での支払い（年間プランの場合）を受け付けています。 引き換えコード付きプリペイドカードも[利用可能](https://ivpn.net/knowledgebase/billing/voucher-cards-faq)です。

#### :material-check:{ .pg-green } WireGuard対応

IVPNはWireGuard®️プロトコルをサポートしています。 [Wireguard](https://wireguard.com)は最先端の[暗号化技術](https://wireguard.com/protocol)を用いた新しいプロトコルです。 加えて、WireGuardはよりシンプルかつより高性能であることを目指しています。

IVPNはWireGuardの使用を[推奨](https://ivpn.net/wireguard)しており、IVPNのすべてのアプリケーションでデフォルトとなっています。 また、公式のWireGuard[アプリ](https://wireguard.com/install)で使用するWireGuard設定を作成できます。

#### :material-information-outline:{ .pg-blue } IPv6の対応

IVPNでは[IPv6を使用するサービスへの接続](https://ivpn.net/knowledgebase/general/do-you-support-ipv6)はできますが、IPv6を使用するデバイスからの接続はできません。

#### :material-alert-outline:{ .pg-orange } リモートポートフォワーディング

IVPNでは以前、ポートフォワーディングに対応していましたが、[2023年6月](https://ivpn.net/blog/gradual-removal-of-port-forwarding)にオプションを削除しました。 この機能の削除により、特にトレント・クライアントなどのピア・ツー・ピアアプリケーションには悪影響を及ぼす可能性があります。

#### :material-check:{ .pg-green } 検閲への対抗

IVPNには[V2Ray](https://v2ray.com/en/index.html)を用いた難読化モードがあり、OpenVPNやWireGuardなどのVPNプロトコルがブロックされている状況で役立ちます。 現在、この機能はデスクトップと[iOS](https://ivpn.net/knowledgebase/ios/v2ray)でのみ利用可能です。 QUICもしくはTCPで[VMess](https://guide.v2fly.org/en_US/basics/vmess.html)を使用する2つのモードがあります。 QUICは輻輳制御がより優れているモダンなプロトコルで高速化・レイテンシーの低下が期待できます。 TCPではデータは通常のHTTPトラフィックとして扱われます。

#### :material-check:{ .pg-green } モバイルクライアント

IVPNは[App Store](https://apps.apple.com/app/id1193122683)と[Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)でクライアントをダウンロードでき、どちらもWireGuard接続を手動で設定する必要がなく、使いやすいインターフェースがあります。 Android向けクライアントは[GitHub](https://github.com/ivpn/android-app/releases)でも公開されています。

#### :material-information-outline:{ .pg-blue } 追記事項

IVPNのクライアントは二要素認証に対応しています。 また、[AntiTracker](https://ivpn.net/antitracker)機能により、広告ネットワークやトラッカーをネットワークレベルでブロックすることができます。

### Mullvad

<div class="admonition recommendation" markdown>

![Mullvad ロゴ](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad**は、透明性とセキュリティに重点を置いた、高速で安価なVPNです。 2009年からサービスが稼働しました。 Mullvadはスウェーデンに拠点を置き、[支払い](https://mullvad.net/en/help/refunds)には14日間の返金保証があります。

[:octicons-home-16: ウェブページ](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="プライバシーポリシー" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title=ドキュメント}
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="ソースコード" }

<details class="downloads" markdown>
<summary>ダウンロード</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 49カ国

Mullvadは[49カ国にサーバー](https://mullvad.net/servers)を設置しています。(1) VPNプロバイダーの最も近いサーバーを選ぶことで、ネットワークトラフィックのレイテンシーを小さくすることができます。 これは目的地までのルートが短い(ホップが少ない) ことによります。
{ .annotate }

1. 最終確認：2025-03-10

また、VPNプロバイダの秘密鍵のセキュリティを考えると、できれば[バーチャルプライベートサーバー](https://en.wikipedia.org/wiki/Virtual_private_server)のような安価な(他の顧客との)共有ソリューションではなく[専用サーバー](https://en.wikipedia.org/wiki/Dedicated_hosting_service)を使用したほうがいいと考えています。

#### :material-check:{ .pg-green } 独立監査済み

Mullvadは複数の[独立した監査](https://mullvad.net/en/blog/tag/audits)を受けており、アプリとインフラの[年次監査](https://mullvad.net/en/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit)の実施を公表しています。

#### :material-check:{ .pg-green } オープンソースクライアント

Mullvadはデスクトップおよびモバイルクライアントのソースコードを[GitHub](https://github.com/mullvad/mullvadvpn-app)で公開しています。

#### :material-check:{ .pg-green } 現金とMoneroが利用可能

Mullvadはクレジット・デビットカードやPayPalでの支払いに加え、匿名での支払手段としてBitcoin、Bitcoin Cash、**Monero**と**現金・現地通貨**での支払いを受け付けています。 引き換えコード付きのプリペイドカードも利用可能です。 また、Swishや銀行振込、いくつかのヨーロッパの支払いシステムにも対応しています。

#### :material-check:{ .pg-green } WireGuard対応

MullvadはWireGuard®️プロトコルをサポートしています。 [Wireguard](https://wireguard.com)は最先端の[暗号化技術](https://wireguard.com/protocol)を用いた新しいプロトコルです。 加えて、WireGuardはよりシンプルかつより高性能であることを目指しています。

MullvadはWireGuardを用いることを[推奨](https://mullvad.net/en/help/why-wireguard)しています。 Android、iOS、macOSとLinuxアプリではデフォルトもしくは利用できる唯一のプロトコルですが、WindowsではWireGuardを[手動で有効にする](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app)必要があります。 また、公式のWireGuard[アプリ](https://wireguard.com/install)で使用するWireGuard設定を作成できます。

#### :material-check:{ .pg-green } IPv6のサポート

Mullvadでは[IPv6でホストされているサービスへのアクセス](https://mullvad.net/en/blog/2014/9/15/ipv6-support)ができ、IPv6アドレスを使用しているデバイスからのアクセスもできます。

#### :material-alert-outline:{ .pg-orange } リモートポートフォワーディング

Mullvadでは以前、ポートフォワーディングに対応していましたが、[2023年3月](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports)にオプションを削除しました。 この機能の削除により、特にトレント・クライアントなどのピア・ツー・ピアアプリケーションには悪影響を及ぼす可能性があります。

#### :material-check:{ .pg-green } 検閲への対抗

Mullvadには検閲を回避し、自由にインターネットにアクセスするための機能があります：

- **難読化モード**：「UDP-over-TCP」と[「WireGuard over Shadowsocks」](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard)の2つのモードがあります。 VPNトラフィックを通常のウェブトラフィックに偽装し、検閲当局による検出とブロックを困難にします。 おそらく、中国は[Shadowsocks経由のトラフィックを妨害するために新しい方法](https://gfw.report/publications/usenixsecurity23/en)を使う必要があります。
- **Shadowsocksとv2rayによる高度な難読化**：高度なユーザーのためにMullvadクライアント上で[Shadowsocksをv2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray)プラグインと使うための方法を公開しています。 設定することで、難読化と暗号化レイヤーが追加されます。
- **カスタムサーバーIP**：IPブロックに対抗するため、MullvadのサポートチームにカスタムサーバーIPをリクエストできます。 カスタムIPを受取り、「Server IP override」の設定でテキストファイルを入力します。検閲当局に知られていない選択したサーバーのIPアドレスで上書きします。
- **ブリッジおよびプロキシ**：Mullvadでは（認証に必要な）APIにアクセスするためのブリッジやプロキシを利用できます。APIへのアクセスをブロックする検閲を回避することができます。

#### :material-check:{ .pg-green } モバイルクライアント

Mullvadは[App Store](https://apps.apple.com/app/id1488466513)と[Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)でクライアントをダウンロードでき、どちらもWireGuard接続を手動で設定する必要がなく、使いやすいインターフェースがあります。 Android向けクライアントは[GitHub](https://github.com/mullvad/mullvadvpn-app/releases)でも公開されています。

#### :material-information-outline:{ .pg-blue } 追記事項

Mullvadはノードごとに[所有もしくはレンタル](https://mullvad.net/en/servers)しているかに関して非常に透明性が高いです。 また、アプリではDefense Against AI-guided Traffic Analysis ([DAITA](https://mullvad.net/en/blog/daita-defense-against-ai-guided-traffic-analysis)) を使うこともできます。 DAITAはVPNトラフィックのパターンと特定のウェブサイトを関連付ける高度なトラフィック分析の脅威から保護します。

## 規準

<div class="admonition danger" markdown>
<p class="admonition-title">警告</p>

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
