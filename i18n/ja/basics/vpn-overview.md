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

Using a VPN in cases where you're using your [real-life or well-known identity](common-misconceptions.md#complicated-is-better) online is unlikely to be useful. Doing so may trigger spam and fraud detection systems, such as if you were to log into your bank's website.

It's important to remember that a VPN will not provide you with absolute anonymity because the VPN provider itself will still have access to your real IP address, destination website information, and often a money trail that can be linked directly back to you. "No logging" policies are merely a promise; if you need complete safety from the network itself, consider using [Tor](../advanced/tor-overview.md) in addition to or instead of a VPN.

You also should not trust a VPN to secure your connection to an unencrypted, HTTP destination. In order to keep what you actually do on the websites you visit private and secure, you must use HTTPS. This will keep your passwords, session tokens, and queries safe from the VPN provider and other potential adversaries in between the VPN server and your destination. 対応している場合、ブラウザのHTTPS-Onlyモードを有効にすることで、接続をHTTPSからHTTPにダウングレードしようとする攻撃を緩和できます。

## VPNで暗号化DNSを使うべきでしょうか？

Unless your VPN provider hosts the encrypted DNS servers themselves, **probably not**. Using DOH/DOT (or any other form of encrypted DNS) with third-party servers will simply add more entities to trust. Your VPN provider can still see which websites you visit based on the IP addresses and other methods. All this being said, there may be some advantages to enabling encrypted DNS in order to enable other security features in your browser, such as ECH. Browser technologies which are reliant on in-browser encrypted DNS are relatively new and not yet widespread, so whether they are relevant to you in particular is an exercise we will leave to you to research independently.

Another common reason encrypted DNS is recommended is that it prevents DNS spoofing. しかし、ブラウザは既に**HTTPS**で[TLS証明書](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates)を確認し、警告しているはずです。 If you are not using **HTTPS**, then an adversary can still just modify anything other than your DNS queries and the end result will be little different.

## Should I use Tor *and* a VPN?

Maybe, Tor is not necessarily suitable for everybody in the first place. Consider your [threat model](threat-modeling.md), because if your adversary is not capable of extracting information from your VPN provider, using a VPN alone may provide enough protection.

If you do use Tor then you are *probably* best off connecting to the Tor network via a commercial VPN provider. However, this is a complex subject which we've written more about on our [Tor overview](../advanced/tor-overview.md) page.

## Should I access Tor through VPN providers that provide "Tor nodes"?

You should not use that feature: The primary advantage of using Tor is that you do not trust your VPN provider, which is negated when you use Tor nodes hosted by your VPN instead of connecting directly to Tor from your computer.

現在、TorはTCPプロトコルのみをサポートしています。 UDP (used by [WebRTC](https://en.wikipedia.org/wiki/WebRTC), [HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3), and other protocols), [ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol), and other packets will be dropped. To compensate for this, VPN providers typically will route all non-TCP packets through their VPN server (your first hop). This is the case with [ProtonVPN](https://protonvpn.com/support/tor-vpn). Additionally, when using this Tor over VPN setup, you do not have control over other important Tor features such as [Isolated Destination Address](https://whonix.org/wiki/Stream_Isolation) (using a different Tor circuit for every domain you visit).

The feature should be viewed as a *convenient* way to access hidden services on Tor, not to stay anonymous. For proper anonymity, use the actual [Tor Browser](../tor.md).

## Commercial VPN Ownership

Most VPN services are owned by the same [few companies](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies). These shady companies run lots of smaller VPN services to create the illusion that you have more choice than you actually do and to maximize profit. Typically, these providers that feed into their shell company have terrible privacy policies and shouldn't be trusted with your internet traffic. You should be very strict about which provider you decide to use.

You should also be wary that many VPN review sites are merely advertising vehicles open to the highest bidder. ==Privacy Guides does not make money from recommending external products, and never uses affiliate programs.==

[推奨されるVPN](../vpn.md ""){.md-button}

## Modern VPN Alternatives

Recently, some attempts have been made by various organizations to address some issues which centralized VPNs have. These technologies are relatively new, but worth keeping an eye on as the field develops.

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
