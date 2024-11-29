---
meta_title: "VPN 如何保護隱私？ VPN 概述 - Privacy Guides"
title: VPN 簡介
icon: material/vpn
description: 虛擬私用網路將風險從您的ISP 轉移到您信任的第三方。 應該記住這些事情。
---

虛擬專用網路是將您的網路末端延伸到世界其它地方的一種方式。

ISP 可以看到網路終端設備（例如數據機）的網際網路進出流量。 HTTPS 等加密協議通常應用在網際網路，因此雖無法確切地知道您發布或閱讀的內容，但還是可以了解您所請求訪問的 [網域名](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns)。

使用 VPN 將您對網路的信任轉移到世界上某處的伺服器，甚至可以向 ISP 隱藏這些資訊。 因此， ISP只會看到您已連接到VPN ，而不會看到您正在傳遞的活動。

<div class="admonition note" markdown>
<p class="admonition-title">Note "備註"</p>

我們在本站提到「虛擬私人網路」時，通常指的是**商業** [VPN 服務商](../vpn.md)，每月向其支付費用以換取路由網路流量安全地通過他們的公共伺服器。 還有許多其他形式的VPN，例如自行託管的 VPN 或由工作場所運營的VPN，它們允許安全地連接到內部/員工網路資源，但是，這類VPN 通常旨在安全地訪問遠端網路，而不是保護隱私的網路連線。

</div>

## VPN工作原理

VPN 會對裝置和 VPN 提供者擁有的伺服器之間流量進行加密。 在您和 VPN 伺服器之間從任何人的角度來看，似乎是正在連接 VPN 伺服器。 VPN 伺服器和目標網站之間的任何人，他們只能看到連接到網站的 VPN 伺服器。

``` mermaid
flowchart LR
 763931["你的裝置<div>（安裝了 VPN 客戶端）</div>"] ===|"透過 VPN 加密"| 404512{"VPN 伺服器"}
 404512 -.-|"未經過 VPN 加密"| 593753(("網際網路<div>（您打算訪問的網路資源）</div>"))
 subgraph 763931["你的裝置<div>（安裝了 VPN 客戶端）</div>"]
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

## 什麼時候不適合使用 VPN？

在您使用[真實身份或知名身份](common-misconceptions.md#complicated-is-better)上網的情況下，使用 VPN 不大可能有用。 這樣做可能會觸發垃圾郵件和欺詐偵測系統，例如您正試圖登入銀行網站。

重要的是請記住，VPN 不會提供絕對的匿名性，因為 VPN 提供者本身仍然會看到用戶的真實 IP 位址、目的地網站資訊，並且通常有可以直接連結回用戶的資金軌跡。 不能僅靠「不記錄」政策指望任何有能力者來保護資料。 如果需要網路本身的完全安全，請考慮使用 [Tor](../advanced/tor-overview.md) 作為 VPN 的補充或替代。

也不該信任 VPN 來保護您與未加密的 HTTP 目標的連線。 為了保持所瀏覽網站活動的私密和安全，您必須使用 HTTPS。 這將確保密碼、會話令牌和查詢免受 VPN 提供者以及 VPN 伺服器和目的地之間其他潛在對手的攻擊。 應在瀏覽器中啟用純 HTTPS 模式（如果支援），以減輕嘗試將連線從 HTTPS 降級為 HTTP 的攻擊。

## 我應該將加密 DNS 與 VPN 一起使用嗎？

除非 VPN 提供者本身託管加密的 DNS 伺服器，否則**可能不會**。 將 DOH/DOT（或任何其他形式的加密 DNS）與第三方伺服器一起使用只會添加更多值得信任的實體。 您的 VPN 提供商仍可以根據 IP 位址和其他方法查看您訪問的網站。 話雖如此，啟用加密 DNS 以便啟用瀏覽器中的其他安全功能（例如 ECH）可能會有一些優點。 依賴瀏覽器內加密 DNS 的瀏覽器技術相對較新，尚未普及，因此它們是否與您特別相關，留給您自行研究。

建議使用加密 DNS 的另一個常見原因是它可以防止 DNS 欺騙。 您的瀏覽器應該已經檢查了 [TLS 憑證](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) 和 **HTTPS** ，並警告您。 如果沒用 **HTTPS**，則對手可以修改您的 DNS 查詢之外的任何東西，最終結果將沒太大差異。

## 我應該*同時* 使用 Tor 與 VPN 嗎？

也許，Tor 從一開始就不一定適合所有人。 考慮[威脅模型](threat-modeling.md)，如果對手無法從 VPN 提供者提取資訊，則單獨使用 VPN 可能就有足夠保護。

如果使用 Tor，那麼*可能*最好透過商業 VPN 提供者連接到 Tor 網絡。 不過這是一個複雜的主題，在 [Tor 概述](../advanced/tor-overview.md) 頁面有更多介紹。

## 應該透過提供「Tor 節點」的 VPN 提供者來存取 Tor 嗎？

不應該使用該功能：使用 Tor 的主要優點是不信任 VPN 提供者，當使用 VPN 託管的 Tor 節點而不是從電腦直接連接到 Tor 時，這一點就被否定了。

目前Tor 僅支援 TCP 協定。 UDP（由 [WebRTC](https://en.wikipedia.org/wiki/WebRTC) 使用，[HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3) 和其他協定）、[ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol) 和其他資料封包將被丟棄。 為了彌補這一點， VPN 提供商通常會引導全部的non-TCP 封包通過他們的 VPN 伺服器（您的第一個跳）。 [ProtonVPN](https://protonvpn.com/support/tor-vpn) 就是這種情況。 此外，使用此 Tor over VPN 設定時，將無法控制 Tor 其他重要的功能，例如 [隔離目標位址](https://whonix.org/wiki/Stream_Isolation) （為了訪問不同網域使用不同的Tor 迴路）。

此功能應被視為*便捷*訪問 Tor 隱藏服務的方式，而不是保持匿名。 為了獲得妥適的匿名性，請使用 [Tor 瀏覽器](../tor.md)。

## 商業 VPN 所有權

大多數 VPN 服務都是由[少數公司](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies)擁有。 這些可疑的公司運行許多小型 VPN 服務，製造出一種擁有比實際更多選擇的假象，來實現利潤最大化。 通常這些為空殼公司提供服務的供應商都有糟糕的隱私權政策，不應信任。 請非常嚴格地決定使用哪個提供者。

還應警惕：許多 VPN 評論網站只是向最高出價者開放的廣告工具。 ==Privacy Guides 不會透過推薦外部產品賺錢，且從不使用推廣方案。==

[VPN 建議](../vpn.md ""){.md-button}

## 現代 VPN 替代方案

近來各組織做了一些嘗試來解決集中式 VPN 的一些問題。 這些技術相對較新，但隨著該領域的發展值得關注。

### 多方中繼

多方中繼 (MPR) 使用不同方的多個節點，這樣任何一方都不知道您是誰以及連接到什麼。 這是 Tor 背後的基本思想，現在有一些付費服務試圖模仿這種模式。

MPR 試圖解決 VPN 固有的問題：用戶必須完全信任它們。 他們透過劃分兩個或多個不同公司間的責任來實現此目標。 例如，Apple 的 iCloud+ Private Relay 透過兩個伺服器路由流量：

1. 首先是 Apple 營運的伺服器。

    當連接到裝置時，伺服器能夠查看裝置的 IP，並了解付款資訊以及與 iCloud 訂閱相關的 Apple ID。 但是，它無法查看您連接到哪個網站。

2. 其次，由合作夥伴 CDN 營運的伺服器，例如 Cloudflare 或 Fastly。

    該伺服器實際上會連接到您的目標網站，但不知道您的裝置。 它知道的唯一 IP 位址是 Apple 伺服器 IP 位址。

其他由 Google 或 INVISV 等公司經營的 MPR 運作也非常相似。 只有當相信這兩家公司不會串通對用戶進行去匿名化時，這種分段保護才存在。

### 去中心化 VPN

解決集中式 VPN 問題的另一個嘗試是 dVPN。 它們基於區塊鏈技術，聲稱透過將節點分佈在許多不同的人身上來消除對單一方的信任。 然而，很多時候 dVPN 預設為單一節點，這意味著需要完全信任該節點，就像傳統 VPN 一樣。 與傳統的 VPN 不同，這個可看到您所有流量的節點是隨機的而不是 VPN 提供者，後者可以被審核且承擔維護其隱私權政策的法律責任。 需要多跳來解決這個問題，但會帶來穩定性和效能成本問題。

另一個考慮因素是法律責任。 出口節點需要處理網路濫用帶來的法律問題，這是 Tor 網路自誕生以來一直在處理的問題。 這會阻止一般人運行節點，並使擁有大量資源來託管節點的惡意行為者更具吸引力。 如果服務是單節點的，將是個大問題，因為潛在的惡意出口節點可以看到您是誰以及正在連接到什麼。

許多 dVPN 被用在推送加密貨幣，而不是提供最好的服務。 它們往往是節點少的小型網路，更容易受到[女巫攻擊](https://en.wikipedia.org/wiki/Sybil_attack)。

## VPN 相關資訊

- [VPN 問題和隱私評論網站](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites)
- [免費 VPN 應用程式調查](https://top10vpn.com/research/free-vpn-investigations/ownership)
- [揭露隱身的 VPN 擁有者：由 23 家公司運營101款 VPN 產品](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies)
- [這家中國公司祕密支援 24 個尋求危險權限的流行應用程式](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions)
- [VPN - a Very Precarious Narrative](https://overengineer.dev/blog/2019/04/08/very-precarious-narrative.html) by Dennis Schubert
