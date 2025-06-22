---
meta_title: "VPNはどのようにプライバシーを保護するのか？ VPNの概要 - Privacy Guides"
title: VPNの概要
icon: material/vpn
description: バーチャルプライベートネットワークはISPから信頼する第三者へリスクを移行します。 このことに留意してください。
---

バーチャルプライベートネットワークはネットワークの末端を世界のどこか別の場所に拡張する方法です。

[:material-movie-open-play-outline: 動画：VPNは必要か？](https://www.privacyguides.org/videos/2024/12/12/do-you-need-a-vpn ""){.md-button}

通常、ISPはネットワーク終端装置（モデムなど）に出入りするインターネットトラフィックの流れを見ることができます。 HTTPSのような暗号化プロトコルはインターネット上で一般的に使われているため、ISPは投稿や閲覧内容を正確に見ることはできませんが、[要求するドメイン](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns)は見ることができます。

VPNにより、このような情報もISPから隠すことができ、ネットワークへの信頼を世界のどこかのサーバーに移行することになります。 その結果、ISPはVPNに接続しているということだけがわかり、VPN経由でのアクティビティについては分かりません。

<div class="admonition note" markdown>
<p class="admonition-title">メモ</p>

Privacy Guidesでは「VPN」は**商用**の[VPNプロバイダー](../vpn.md)のことを指します。インターネットトラフィックをVPNプロバイダーのパブリックサーバー経由で安全にルーティングしてもらい、月額料金を支払います。 VPNにはセルフホスティングしたり職場が運用するなど、内部や従業員のネットワークリソースに安全に接続できるようにするものもあります。このようなVPNはインターネット接続のプライバシーを保護するというよりも、リモートネットワークに安全にアクセスすることが目的です。

</div>

## VPNの仕組み

VPNは、あなたのデバイスとVPNプロバイダーが所有するサーバー間のトラフィックを暗号化します。 あなたとVPNサーバーの間にいる人から見ると、あなたがVPNサーバーにアクセスしているように見えます。 VPNサーバーと目的のサイトにいる人から見ると、VPNサーバーがそのウェブサイトにアクセスしているようにしか見えません。

``` mermaid
flowchart LR
 763931["デバイス<div>（VPNクライアントあり）</div>"] ===|"VPN暗号化"| 404512{"VPNサーバー"}
 404512 -.-|"VPN暗号化なし"| 593753(("インターネット<div>（目的のサイト）</div>"))
 subgraph 763931["デバイス<div>（VPNクライアントあり）</div>"]
 end
```

VPNはVPNサーバーとインターネット上の目的のサイト間のトラフィックに対し、セキュリティを強化せず、暗号化しないことに注意してください。 ウェブサイトに安全にアクセスするには、VPNの使用にかかわらず、HTTPSが使われていることを確認する**必要があります**。

## VPNを使うべきですか？

ほぼ確実に**そうすべきです**。 VPNには、次のような多くの利点があります。

1. インターネットサービスプロバイダ**のみ**からトラフィックを隠します。
1. ISPや海賊版対策組織からダウンロード（トレントなど）を隠す。
1. 第三者のウェブサイトやサービスからIPを隠す。 混ぜ合わせることで、IPベースのトラッキングを防ぎます。
1. 特定のコンテンツの地理的制限の解除が行える。

VPNは地理的にネットワークトラフィックを移動させるなどTorと同じような利点*も*あります。また、特に司法管轄外のVPNプロバイダーを選んだ場合、優れたVPNプロバイダーは例えば抑圧的な政権の司法当局に協力しないでしょう。

VPNはデバイスとVPNサーバー間以外の接続は暗号化できません。 ISPが行っているようにVPNプロバイダーはトラフィックを見たり変更したりできるため、VPNプロバイダーを信頼していることに変わりありません。 また、VPNプロバイダーの「ノーログ」ポリシーを確認する方法は一切ありません。

## VPNが適していない場合

[現実の生活のIDやよく知られているID](common-misconceptions.md#complicated-is-better)をオンライン上で使う際にVPNを使うケースではあまり役に立ちません。 そうした場合、銀行のウェブサイトにログインするときなどは、スパム検知や不正検出システムが作動する可能性があります。

VPNによって完全な匿名性は得られないことを覚えておくことが重要です。なぜならVPNプロバイダーはあなたの実際のIPアドレスや訪問先のウェブサイトの情報を持っていますし、直接結びつけることができるお金の流れも知っています。 「ノーログ」ポリシーは単なる約束に過ぎません。もしネットワーク自体からの完全な安全性が必要な場合は、VPNに加え、もしくは代わりに[Tor](../advanced/tor-overview.md)を使うことを検討してください。

また、暗号化されていないHTTPへの接続を保護する目的でVPNを信頼してはいけません。 訪問するウェブサイトで実際に行うことをプライベートかつ安全に保つにはHTTPSを使用する必要があります。 VPNプロバイダーやVPNサーバーと目的のサイトの間にいる潜在的な敵対者からパスワード、セッショントークンやクエリーを安全に守ることができます。 対応している場合、ブラウザのHTTPS-Onlyモードを有効にすることで、接続をHTTPSからHTTPにダウングレードしようとする攻撃を緩和できます。

## VPNで暗号化DNSを使うべきでしょうか？

VPNプロバイダーが暗号化DNSサーバーをホストしていない限り、**おそらく使わないほうがよいでしょう**。 第三者のサーバーのDOH/DOT（やその他の暗号化DNS）を使うことは単に信頼する対象が増えるだけです。 VPNプロバイダーはIPアドレスやその他の方法で訪問したウェブサイトを確認できます。 それでもECHのようなブラウザのセキュリティ機能を有効にするために暗号化DNSを使うという利点はあるかもしれません。 暗号化DNSに依存するブラウザーの技術は比較的新しくまだ普及していません。関係するかどうかは自分自身で調査してください。

暗号化DNSが推奨されるもう一つのよくある理由はDNSスプーフィングを防ぐことです。 しかし、ブラウザは既に**HTTPS**で[TLS証明書](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates)を確認し、警告しているはずです。 **HTTPS**を使用していない場合、敵対者はDNSクエリ以外を変更することだけしかできず、結果はほとんど変わりません。

## Tor*と*VPNを使うべきですか？

そもそもTorはすべての人に必ずしも適していないかもしれません。 [脅威モデル](threat-modeling.md)を考慮してください。もし敵対者がVPNプロバイダーから情報を取得する能力がなければ、VPNを使うだけで十分な保護が得られる可能性があるからです。

もしTorを使うのであれば、商用VPNプロバイダー経由でTorネットワークにアクセスするのが*おそらく*最善の方法でしょう。 しかし、これは複雑な問題であり、[Torの概要](../advanced/tor-overview.md)のページで詳細を説明しています。

## VPNプロバイダーの「Torノード」からTorにアクセスするべきですか？

このような機能は使うべきではありません。Torを使う主な利点はVPNプロバイダーを信用していないことであり、コンピューターからTorに直接接続する代わりにVPNプロバイダーがホストするTorノードを使う場合、この利点は失われてしまいます。

現在、TorはTCPプロトコルのみをサポートしています。 UDP（[WebRTC](https://en.wikipedia.org/wiki/WebRTC)や[HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3)などのプロトコル）や[ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol)などのその他のパケットは捨てられてしまいます。 これを補うために、VPNプロバイダーは通常、TCP以外のパケットをすべてVPNサーバー（ファーストホップ）を経由するようにルーティングします。 [ProtonVPN](https://protonvpn.com/support/tor-vpn)が該当します。 さらに、VPN経由でのTorを使う場合、[Isolated Destination Address](https://whonix.org/wiki/Stream_Isolation)（訪問するドメインごとに異なるTor回線を使う）などTorの重要な機能を制御することはできません。

このような機能は匿名性を保つためではなく、Torからアクセスできないサービスへアクセスするための*便利な*方法としてとらえるべきです。 適切に匿名性を確保するためには実際に[Tor Browser](../tor.md)を使うべきです。

## 商用VPNの所有権

ほとんどのVPNサービスは同じ[数社](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies)が所有しています。 こうした怪しげな企業は小規模なVPNサービスを多数運用することで、実際よりも多くの選択肢があるように錯覚させ、利益を最大化しています。 一般的に、怪しげな会社が運営するVPNプロバイダーのプライバシーポリシーはひどく、インターネットトラフィックを任せるべきではありません。 どのプロバイダーを利用するかは厳密に決める必要があります。

また、VPNのレビューサイトは最高額入札者の単なる広告であることにも注意する必要があります。 ==Privacy Guidesは推奨するプロダクトから収益を得ておらず、アフィリエイトプログラムも利用していません。==

[推奨されるVPN](../vpn.md ""){.md-button}

## VPNのモダンな代替手段

最近では、中央集権的なVPNが抱える問題に対処するために、様々な組織によって試みがなされています。 このような技術は比較的新しいものですが、分野が発展するにつれて注目する価値があります。

### Multi-Party Relays

Multi-Party Relays (MPRs) use multiple nodes owned by different parties, such that no individual party knows both who you are and what you're connecting to. This is the basic idea behind Tor, but now there are some paid services that try to emulate this model.

MPRs seek to solve a problem inherent to VPNs: the fact that you must trust them completely. They accomplish this goal by segmenting the responsibilities between two or more different companies.

One example of a commercially available MPR is Apple's iCloud+ Private Relay, which routes your traffic through two servers:

1. Firstly, a server operated by Apple.

    This server is able to see your device's IP when you connect to it, and has knowledge of your payment information and Apple ID tied to your iCloud subscription. However, it is unable to see what website you are connecting to.

2. Secondly, a server operated by a partner CDN, such as Cloudflare or Fastly.

    This server actually makes the connection to your destination website, but has no knowledge of your device. The only IP address it knows about is Apple's server's.

Other MPRs run by different companies operate in a very similar manner. This protection by segmentation only exists if you trust the two companies to not collude with each other to deanonymize you.

### 分散型VPN

Another attempt at solving the issues with centralized VPN services are dVPNs. These are based on blockchain technology and claim to eliminate trust in a single party by distributing the nodes across lots of different people. However, many times a dVPN will default to a single node, meaning you need to trust that node completely, just like a traditional VPN. Unlike a traditional VPN, this one node that can see all your traffic is a random person instead of your VPN provider that can be audited and has legal responsibilities to uphold their privacy policy. Multi-hop is needed to solve this, but that comes with a stability and performance cost.

Another consideration is legal liability. The exit node will need to deal with legal problems from misuse of the network, an issue that the Tor network has contended with for its entire existence. This discourages regular people from running nodes and makes it more attractive for a malicious actor with lots of resources to host one. This is a big problem if the service is single-node, as the potentially malicious exit node can see who you are and what you're connecting to.

Many dVPNs are used to push a cryptocurrency rather than to make the best service. They also tend to be smaller networks with fewer nodes, making them more vulnerable to [Sybil attacks](https://en.wikipedia.org/wiki/Sybil_attack).

## Related VPN Information

- [VPNとプライバシーレビューサイトの問題点](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites)
- [無料VPNアプリの調査](https://top10vpn.com/research/free-vpn-investigations/ownership)
- [Hidden VPN owners unveiled: 101 VPN products run by just 23 companies](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies)
- [This Chinese company is secretly behind 24 popular apps seeking dangerous permissions](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions)
- [VPN - a Very Precarious Narrative](https://overengineer.dev/blog/2019/04/08/very-precarious-narrative.html) by Dennis Schubert
