---
meta_title: "VPN如何保護您的隱私？ VPN概述 - Privacy Guides"
title: VPN 簡介
icon: material/vpn
description: 虛擬私用網路將風險從您的ISP 轉移到您信任的第三方。 你應該記住這些事情。
---

虛擬專用網路是將您的網路末端延伸到世界其它地方的一種方式。

ISP 可以看到網路終端設備（例如數據機）的網際網路進出流量。 HTTPS 等加密協議通常應用在網際網路，因此雖無法確切地知道您發布或閱讀的內容，但還是可以了解您所請求訪問的 [網域名](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns)。

使用 VPN 將您對網路的信任轉移到世界上某處的伺服器，甚至可以向 ISP 隱藏這些資訊。 因此， ISP只會看到您已連接到VPN ，而不會看到您正在傳遞的活動。

!!! note "備註"

    我們在本站提到「虛擬私人網路」時，通常指的是**商業** [VPN 服務商](../vpn.md)，每月向其支付費用以換取路由網路流量安全地通過他們的公共伺服器。 還有許多其他形式的VPN，例如自行託管的 VPN 或由工作場所運營的VPN，它們允許安全地連接到內部/員工網絡資源，但是，這類VPN 通常旨在安全地訪問遠端網絡，而不是保護隱私的網路連線。

## VPN工作原理

VPN 會對裝置和 VPN 提供者擁有的伺服器之間流量進行加密。 在您和 VPN 伺服器之間從任何人的角度來看，似乎是正在連接 VPN 伺服器。 VPN 伺服器和目標網站之間的任何人，他們只能看到連接到網站的 VPN 伺服器。

``` mermaid
flowchart LR
 763931["Your Device<div>(with VPN Client)</div>"] ===|"VPN Encryption"| 404512{"VPN Server"}
 404512 -.-|"No VPN Encryption"| 593753((("The Internet\n(Your Destination)")))
 subgraph 763931["Your Device<div>(with VPN Client)</div>"]
 end
```

請注意，VPN 不會為 VPN 伺服器與網際網路的目的地之間的流量新增任何安全性或加密。 要安全地訪問網站，無論是否使用 VPN，都**必須**確保使用 HTTPS。

## 我應該使用 VPN 嗎？

**是的**，幾乎可以肯定。 VPN 有很多優點，包括：

1. **僅需**對網路連線服務商隱藏您的流量 。
1. 對 ISP 和反盜版組織隱藏您的下載（如 torrents）。
1. 向第三方網站和服務隱藏 IP，幫助您混入防止基於 IP 的追蹤。
1. 可繞過某些內容的地理限制。

VPN 可以提供 Tor 一些相同好處，例如對造訪的網站隱藏 IP 以及在地理位置上轉移您的網路流量，而優秀的 VPN 服務通常不會與壓迫政權的法律當局合作，特別是選擇自身司法管轄範圍之外的 VPN 服務商。

VPN 無法加密裝置與 VPN 伺服器之間連線以外的資料。 VPN 服務商可以像 ISP 一樣查看和修改您的流量，因此最好對他們要有一定程度的信任。 而且沒有方式可以驗證 VPN 提供商的“無記錄”政策是否貫徹。

## 何時不適合用 VPN？

如果在線上使用[現實生活或眾所周知的身份](common-misconceptions.md#complicated-is-better)，那麼 VPN 不太可能有用。 這樣做可能會觸發垃圾郵件和欺詐偵測系統，例如您正試圖登入銀行網站。

重要的是請記住，VPN 不會提供絕對的匿名性，因為 VPN 提供者本身仍然會看到用戶的真實 IP 位址、目的地網站資訊，並且通常有可以直接連結回用戶的資金軌跡。 不能僅靠「不記錄」政策指望任何有能力者來保護資料。 如果需要網路本身的完全安全，請考慮使用 [Tor](../advanced/tor-overview.md) 作為 VPN 的補充或替代。

也不該信任 VPN 來保護您與未加密的 HTTP 目標的連線。 為了保持所瀏覽網站活動的私密和安全，您必須使用 HTTPS。 這將確保密碼、會話令牌和查詢免受 VPN 提供者以及 VPN 伺服器和目的地之間其他潛在對手的攻擊。 應在瀏覽器中啟用純 HTTPS 模式（如果支援），以減輕嘗試將連線從 HTTPS 降級為 HTTP 的攻擊。

## 我應該將加密 DNS 與 VPN 一起使用嗎？

除非 VPN 提供者本身託管加密的 DNS 伺服器，否則**可能不會**。 將 DOH/DOT（或任何其他形式的加密 DNS）與第三方伺服器一起使用只會添加更多值得信任的實體。 您的 VPN 提供商仍可以根據 IP 地址和其他方法查看您訪問的網站。 話雖如此，啟用加密 DNS 以便啟用瀏覽器中的其他安全功能（例如 ECH）可能會有一些優點。 依賴瀏覽器內加密 DNS 的瀏覽器技術相對較新，尚未普及，因此它們是否與您特別相關，留給您自行研究。

建議使用加密 DNS 的另一個常見原因是它可以防止 DNS 欺騙。 您的瀏覽器應該已經檢查了 [TLS 憑證](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) 和 **HTTPS** ，並警告您。 如果沒用 **HTTPS**，則對手可以修改您的 DNS 查詢之外的任何東西，最終結果將沒太大差異。

## 我應該*同時* 使用 Tor 與 VPN 嗎？

也許，Tor 從一開始就不一定適合所有人。 考慮[威脅模型](threat-modeling.md)，如果對手無法從 VPN 提供者提取資訊，則單獨使用 VPN 可能就有足夠保護。

如果使用 Tor，那麼*可能*最好透過商業 VPN 提供者連接到 Tor 網絡。 不過這是一個複雜的主題，在 [Tor 概述](../advanced/tor-overview.md) 頁面有更多介紹。

## 應該透過提供「Tor 節點」的 VPN 提供者來存取 Tor 嗎？

不應該使用該功能：使用 Tor 的主要優點是不信任 VPN 提供者，當使用 VPN 託管的 Tor 節點而不是從電腦直接連接到 Tor 時，這一點就被否定了。

目前Tor 僅支援 TCP 協定。 UDP（由 [WebRTC](https://en.wikipedia.org/wiki/WebRTC) 使用，[HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3) 和其他協定）、[ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol) 和其他資料封包將被丟棄。 為了彌補這一點， VPN 提供商通常會引導全部的non-TCP 封包通過他們的 VPN 伺服器（您的第一個跳）。 [ProtonVPN ](https://protonvpn.com/support/tor-vpn/)的情況就是如此。 此外，使用此 Tor over VPN 設定時，您無法控制 Tor 其他重要的功能，例如 [隔離目標位址](https://www.whonix.org/wiki/Stream_Isolation) （為您訪問不同網域使用不同的Tor 迴路）。

The feature should be viewed as a *convenient* way to access hidden services on Tor, not to stay anonymous. For proper anonymity, use the actual [Tor Browser](../tor.md).

## Commercial VPN Ownership

Most VPN services are owned by the same [few companies](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies/). These shady companies run lots of smaller VPN services to create the illusion that you have more choice than you actually do and to maximize profit. Typically, these providers that feed into their shell company have terrible privacy policies and shouldn't be trusted with your internet traffic. You should be very strict about which provider you decide to use.

You should also be wary that many VPN review sites are merely advertising vehicles open to the highest bidder. ==Privacy Guides does not make money from recommending external products, and never uses affiliate programs.==

[Our VPN Recommendations](../vpn.md ""){.md-button}

## Modern VPN Alternatives

Recently, some attempts have been made by various organizations to address some issues which centralized VPNs have. These technologies are relatively new, but worth keeping an eye on as the field develops.

### Multi-Party Relays

Multi-Party Relays (MPRs) use multiple nodes owned by different parties, such that no individual party knows both who you are and what you're connecting to. This is the basic idea behind Tor, but now there are some paid services that try to emulate this model.

MPRs seek to solve a problem inherent to VPNs: the fact that you must trust them completely. They accomplish this goal by segmenting the responsibilities between two or more different companies. For example, Apple's iCloud+ Private Relay routes your traffic through two servers:

1. Firstly, a server operated by Apple.

    This server is able to see your device's IP when you connect to it, and has knowledge of your payment information and Apple ID tied to your iCloud subscription. However, it is unable to see what website you are connecting to.

2. Secondly, a server operated by a partner CDN, such as Cloudflare or Fastly.

    This server actually makes the connection to your destination website, but has no knowledge of your device. The only IP address it knows about is Apple's server's.

Other MPRs run by different companies like Google or INVISV operate in a very similar manner. This protection by segmentation only exists if you trust the two companies to not collude with each other to deanonymize you.

### Decentralized VPNs

Another attempt at solving the issues with centralized VPN services are dVPNs. These are based on blockchain technology and claim to eliminate trust in a single party by distributing the nodes across lots of different people. However, many times a dVPN will default to a single node, meaning you need to trust that node completely, just like a traditional VPN. Unlike a traditional VPN, this one node that can see all your traffic is a random person instead of your VPN provider that can be audited and has legal responsibilities to uphold their privacy policy. Multi-hop is needed to solve this, but that comes with a stability and performance cost.

Another consideration is legal liability. The exit node will need to deal with legal problems from misuse of the network, an issue that the Tor network has contended with for its entire existence. This discourages regular people from running nodes and makes it more attractive for a malicious actor with lots of resources to host one. This is a big problem if the service is single-node, as the potentially malicious exit node can see who you are and what you're connecting to.

Many dVPNs are used to push a cryptocurrency rather than to make the best service. They also tend to be smaller networks with fewer nodes, making them more vulnerable to [Sybil attacks](https://en.wikipedia.org/wiki/Sybil_attack).

## VPN 相關資訊

- [VPN 問題和隱私評論網站](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites/)
- [免費 VPN 應用程式調查](https://www.top10vpn.com/free-vpn-app-investigation/)
- [揭露隱身的 VPN 擁有者：由 23 家公司運營101款 VPN 產品](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies/)
- [這家中國公司祕密支持24個尋求危險權限的流行應用程序](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions/)
- [VPN - a Very Precarious Narrative](https://schub.io/blog/2019/04/08/very-precarious-narrative.html) by Dennis Schubert
