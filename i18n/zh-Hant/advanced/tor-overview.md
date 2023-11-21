---
title: "Tor 簡介"
icon: 'simple/torproject'
description: Tor 是一個免費使用的去中心化網路，其讓用戶在使用網際網路之際盡可能地保護自己的隱私。
---

Tor 是一個免費使用的去中心化網路，其讓用戶在使用網際網路之際盡可能地保護自己的隱私。 如果使用得當，該網路可以實現私人和匿名瀏覽和通訊。

## 正在連接到Tor

Before connecting to [Tor](../tor.md), you should carefully consider what you're looking to accomplish by using Tor in the first place, and who you're trying to hide your network activity from.

If you live in a free country, are accessing mundane content via Tor, aren't worried about your ISP or local network administrators having the knowledge that you're using Tor, and want to help [de-stigmatize](https://2019.www.torproject.org/about/torusers.html.en) Tor usage, you can likely connect to Tor directly via standard means like [Tor Browser](../tor.md) without worry.

If you have the ability to access a trusted VPN provider and **any** of the following are true, you almost certainly should connect to Tor through a VPN:

- You already use a [trusted VPN provider](../vpn.md)
- Your threat model includes an adversary which is capable of extracting information from your ISP
- Your threat model includes your ISP itself as an adversary
- Your threat model includes local network administrators before your ISP as an adversary

Because we already [generally recommend](../basics/vpn-overview.md) that the vast majority of people use a trusted VPN provider for a variety of reasons, the following recommendation about connecting to Tor via a VPN likely applies to you. <mark>There is no need to disable your VPN before connecting to Tor</mark>, as some online resources would lead you to believe.

Connecting directly to Tor will make your connection stand out to any local network administrators or your ISP. Detecting and correlating this traffic [has been done](https://edition.cnn.com/2013/12/17/justice/massachusetts-harvard-hoax/) in the past by network administrators to identify and deanonymize specific Tor users on their network. On the other hand, connecting to a VPN is almost always less suspicious, because commercial VPN providers are used by everyday consumers for a variety of mundane tasks like bypassing geo-restrictions, even in countries with heavy internet restrictions.

Therefore, you should make an effort to hide your IP address **before** connecting to the Tor network. You can do this by simply connecting to a VPN (through a client installed on your computer) and then accessing [Tor](../tor.md) as normal, through Tor Browser for example. This creates a connection chain like:

- [x] You → VPN → Tor → Internet

From your ISP's perspective, it looks like you're accessing a VPN normally (with the associated cover that provides you). From your VPN's perspective, they can see that you are connecting to the Tor network, but nothing about what websites you're accessing. From Tor's perspective, you're connecting normally, but in the unlikely event of some sort of Tor network compromise, only your VPN's IP would be exposed, and your VPN would *additionally* have to be compromised to deanonymize you.

This is **not** censorship circumvention advice, because if Tor is blocked entirely by your ISP, your VPN likely is as well. Rather, this recommendation aims to make your traffic blend in better with commonplace VPN user traffic, and provide you with some level of plausible deniability by obscuring the fact that you're connecting to Tor from your ISP.

---

We **very strongly discourage** combining Tor with a VPN in any other manner. Do not configure your connection in a way which resembles any of the following:

- You → Tor → VPN → Internet
- You → VPN → Tor → VPN → Internet
- Any other configuration

Some VPN providers and other publications will occasionally recommend these **bad** configurations to evade Tor bans (exit nodes being blocked by websites) in some places. [Normally](https://support.torproject.org/#about_change-paths), Tor frequently changes your circuit path through the network. When you choose a permanent *destination* VPN (connecting to a VPN server *after* Tor), you're eliminating this advantage and drastically harming your anonymity.

Setting up bad configurations like these is difficult to do accidentally, because it usually involves either setting up custom proxy settings inside Tor Browser, or setting up custom proxy settings inside your VPN client which routes your VPN traffic through the Tor Browser. As long as you avoid these non-default configurations, you're probably fine.

---

!!! info "VPN/SSH Fingerprinting"

    The Tor Project [notes](https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN#vpnssh-fingerprinting) that *theoretically* using a VPN to hide Tor activities from your ISP may not be foolproof. VPNs have been found to be vulnerable to website traffic fingerprinting, where an adversary can still guess what website is being visited, because all websites have specific traffic patterns.
    
    Therefore, it's not unreasonable to believe that encrypted Tor traffic hidden by a VPN could also be detected via similar methods. There are no research papers on this subject, and we still consider the benefits of using a VPN to far outweigh these risks, but it is something to keep in mind.
    
    If you still believe that pluggable transports (bridges) provide additional protection against website traffic fingerprinting that a VPN does not, you always have the option to use a bridge **and** a VPN in conjunction.

Determining whether you should first use a VPN to connect to the Tor network will require some common sense and knowledge of your own government's and ISP's policies relating to what you're connecting to. However, again in most cases you will be better off being seen as connecting to a commercial VPN network than directly to the Tor network. If VPN providers are censored in your area, then you can also consider using Tor pluggable transports (e.g. Snowflake or meek bridges) as an alternative, but using these bridges may arouse more suspicion than standard WireGuard/OpenVPN tunnels.

## Tor 並非是

The Tor network is not the perfect privacy protection tool in all cases, and has a number of drawbacks which should be carefully considered. These things should not discourage you from using Tor if it is appropriate for your needs, but they are still things to think about when deciding which solution is most appropriate for you.

### Tor 不是免費的 VPN

*Orbot* 行動應用，讓許多人誤將 Tor 描述為適用所有裝置流量的「免費 VPN」。 然而，與典型的 VPN 相比，這樣使用 Tor 會有某些危險。

不同於 Tor 出口節點，VPN 服務商通常不會*主動*[惡意](#caveats)。 Tor 出口節點可由任何人創建，它們是網路日誌記錄和修改的熱點。 2020 年許多 Tor 出口節點被記錄將 HTTPS 流量降級為 HTTP，以便[「劫持」加密貨幣交易](https://therecord.media/thousands-of-tor-exit-nodes-attacked-cryptocurrency-users-over-the-past-year)。 Other exit node attacks such as replacing downloads via unencrypted channels with malware have also been observed. HTTPS does mitigate these threats to an extent.

As we've alluded to already, Tor is also easily identifiable on the network. Unlike an actual VPN provider, using Tor will make you stick out as a person likely attempting to evade authorities. In a perfect world, Tor would be seen by network administrators and authorities as a tool with many uses (like how VPNs are viewed), but in reality the perception of Tor is still far less legitimate than the perception of commercial VPNs, so using a real VPN provides you with plausible deniability, e.g. "I was just using it to watch Netflix," etc.

### Tor usage is not undetectable

**Even if you use bridges and pluggable transports,** the Tor Project provides no tools to hide the fact that you are using Tor from your ISP. Even using obfuscated "pluggable transports" or non-public bridges do not hide the fact that you are using a private communications channel. The most popular pluggable transports like obfs4 (which obfuscates your traffic to "look like nothing") and meek (which uses domain fronting to camouflage your traffic) can be [detected](https://www.hackerfactor.com/blog/index.php?/archives/889-Tor-0day-Burning-Bridges.html) with fairly standard traffic analysis techniques. Snowflake has similar issues, and can be [easily detected](https://www.hackerfactor.com/blog/index.php?/archives/944-Tor-0day-Snowflake.html) *before* a Tor connection is even established.

還有這三種以外的可插拔傳輸，但通常依賴透過隱蔽性來逃避偵測的安全性。 它們不是不可能被檢測，只是使用者太少，以至於不值得為它們建立檢測器。 如果特別遭受監控，則不應依賴它們。

了解繞過審查和逃避檢測兩者的差異很重要。 要實現前者更容易，因為網路審查員實際上存在許多現實限制，但這些技術並沒有掩蓋這個事實：監視網路使用的相關單位知道您——*的確在* — —使用Tor 。

### Tor 瀏覽器不是最*安全*的瀏覽器

匿名性常常與安全性相矛盾：Tor 的匿名性要求每個使用者都是相同的，這會造成單一文化（所有 Tor 瀏覽器使用者都存在相同的錯誤）。 As a cybersecurity rule of thumb, monocultures are generally regarded as bad: Security through diversity (which Tor lacks) provides natural segmentation by limiting vulnerabilities to smaller groups, and is therefore usually desirable, but this diversity is also less good for anonymity.

Additionally, Tor Browser is based on Firefox's Extended Support Release builds, which only receives patches for vulnerabilities considered *Critical* and *High* (not *Medium* and *Low*). This means that attackers could (for example):

1. 在 Firefox nightly 或 beta 版本中尋找新的嚴重/高危險漏洞，然後檢查它們可否利用在 Tor 瀏覽器（此漏洞週期可能會持續數週）。
2. Chain *multiple* Medium/Low vulnerabilities together until they get the level of access they're looking for (this vulnerability period can last months or longer).

Those at risk of browser vulnerabilities should consider additional protections to defend against Tor Browser exploits, such as using Whonix in [Qubes](../os/qubes-overview.md) to contain your Tor browsing in a secure VM and protect against leaks.

## 連接明網服務的路徑建立

「明網服務」是用任何瀏覽器都可訪問的網站，例如 [privacyguides.org](https://www.privacyguides.org)。 Tor 允許您匿名連接到某些網站，由數千個志願者運行的伺服器組成的網絡引導您的流量，這些伺服器稱為節點（或中繼）。

每當您連接到 Tor 時，它都會選擇三個節點來構建通往網際網路的路徑，這種路徑稱為「迴路」。

<figure markdown>
  ![Tor 路徑顯示您的設備到達目的地網站之前所連接的入口節點，中間節點和出口節點](../assets/img/how-tor-works/tor-path.svg#only-light)
![Tor 路徑顯示您的設備到達目的地網站之前所連接的入口節點，中間節點和出口節點](../assets/img/how-tor-works/tor-path-dark.svg#only-dark)
  <figcaption>Tor 迴路路徑</figcaption>
</figure>

每個節點都有自己的功能：

### 入口節點

入口節點，通常稱為守護節點，是 Tor 客戶端連接的第一個節點。 入口節點能夠看到您的 IP 位址，但無法看到您正在連接的內容。

不像其它節點 Tor 客戶端會隨機地選取入口節點後持續使用二~三個月以防護某些外部攻擊 [^1]

### 中間節點

中間節點是 Tor 客戶端連接的第二個節點。 它可以看到流量來自哪個節點（入口節點）以及它下一步要去哪個節點。 中間節點無法看到您的 IP 位址或您連接的網域。

對於每個新迴路，中間節點是隨機從所有可用的 Tor 節點中選出。

### 出口節點

出口節點是您的 Web 流量離開 Tor 網路並轉發到所需目的地的點。 出口節點無法看到您的 IP 位址，但它知道將連接到哪個網站。

出口節點將從所有可用的 Tor 節點中隨機選擇，並使用退出中繼標記。[^ 2]

## Onion 服務的路徑建立

“Onion 服務” （也通常被稱為“隱藏服務” ）是只能由 Tor 瀏覽器訪問的網站。 這些網站有一個長串隨機生成的域名，結尾為 `.onion`。

在Tor中連接到 Onion服務的工作原理與連接到明網服務非常相似，但您的流量在到達目的地伺服器之前會通過 **6 個** 節點。 不過就如之前所言，其中只有三個節點會有助 *您的*匿名性，而另外三個節點則是為了保護 * Onion 服務* 匿名性，隱藏該網站的真正  IP 和位置，就如同 Tor 瀏覽器如何隱蔽您的 IP 一樣。

<figure style="width:100%" markdown>
  ![Tor路徑顯示您的流量通過您的三個Tor節點加上三個額外的Tor節點隱藏網站的身份](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![Tor路徑顯示您的流量被路由通過您的三個Tor節點加上三個額外的Tor節點隱藏網站的身份](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Tor電路路徑與洋蔥服務。 <span class="pg-blue">藍色</span> 圍欄中的節點屬於您的瀏覽器，而 <span class="pg-red">紅色</span> 圍欄中的節點屬於伺服器，因此它們的身份對您是隱藏的。</figcaption>
</figure>

## 加密

Tor 使用來自出口，中間和入口節點的密鑰對每個封包（傳輸數據區塊）依序進行三次加密。

一旦 Tor 構建了電路，數據傳輸將按照以下方式進行：

1. 首先：當數據包到達入口節點時，第一層加密被移除。 在這個加密封包中，入口節點將找到另一個具有中間節點地址的加密封包。 然後，入口節點將將封包轉發到中間節點。

2. 其次：當中間節點從入口節點接收到封包時，它也會利用其密鑰刪除一層加密，找到具有出口節點地址的加密數據包。 然後中間節點將數據包轉發到出口節點。

3. 最後：當退出節點收到其數據包時，它將使用其密鑰移除最後一層加密。 出口節點將看到目的地地址，並將封包轉發到該地址。

下面是顯示此過程的圖表。 每個節點都會移除自己的加密層，當目的地伺服器傳回數據時，同樣過程會再反向發生。 例如，出口節點不知道你是誰，但它確實知道封包來自哪個節點，因此添加了自己的加密層並將其發送回來。

<figure markdown>
  ![Tor 加密](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![Tor 加密](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>通過 Tor 網路發送與接數資料</figcaption>
</figure>

Tor 允許我們連接到伺服器，而不讓任何一方知道完整路徑。 入口節點知道你是誰，但不知道你要去哪裡；中間節點不知道你是誰或你要去哪裡；出口節點知道你要去哪裡，但不知道你是誰。 由於出口節點負責了最終連線，目的地伺服器永遠不會知道您的 IP 位址。

## 注意事項

雖然 Tor 確實提供了強大的隱私保證，但必須意識到它並不完美：

- Tor 不會保護您免於錯誤地暴露自己，例如分享了太多有關自身真實身份的資訊。
- Tor 出口節點可以**修改**通過的未加密流量。 這意味著未加密的流量（例如純 HTTP 流量）可能會被惡意出口節點變更。 **Never** download files from an unencrypted `http://` website over Tor, and ensure your browser is set to always upgrade HTTP traffic to HTTPS.
- Tor 出口節點還可以監控通過它們的流量。 包含個人識別資訊的未加密流量可能會讓您在該出口節點被消除匿名。 再次強調，建議僅透過 Tor 使用 HTTPS。
- Powerful adversaries with the capability to passively watch *all* network traffic around the globe ("Global Passive Adversaries") are **not** something that Tor protects you against (and using Tor [with a VPN](#safely-connecting-to-tor) doesn't change this fact).
- Well-funded adversaries with the capability to passively watch *most* network traffic around the globe still have a *chance* of deanonymizing Tor users by means of advanced traffic analysis.

如果您希望使用 Tor 瀏覽網頁，我們只建議使用 **官方** Tor 瀏覽器：它旨在防止指紋。

- [Tor 瀏覽器 :material-arrow-right-drop-circle:](../tor.md#tor-browser)

### 橋接器提供的保護

Tor 橋接器通常被認為是向 ISP 隱藏 Tor 使用情況的替代方法，而不是 VPN（我們建議盡可能使用後者 ）。 需要考慮的是，雖然橋接器可以提供足夠的審查規避，但這只是*暫時*的好處。 它們無法充分保護您，防止 ISP 透過歷史流量日誌分析發現您*過去*連接 Tor。

請考慮以下場景來理解：透過橋接器連接到 Tor，而 ISP 沒有偵測到它，因為他們沒有對流量進行複雜分析，因此一切都按預期進行。 現在，4個月過去，橋接器 IP 已經公開了。 這種情況在橋接器中很常見，它們被發現並被封鎖的頻率相對較高，但不是立即發生。

您的 ISP 想要辨識出 4 個月前 Tor 用戶，透過其有限的元資料記錄，他們可以看到您連接到的 IP 位址其實是 Tor 橋接器。 您幾乎沒有其他藉口進行此類連接，因此 ISP 可以非常有信心地說您當時是 Tor 用戶。

對比我們所推薦的場景，透過 VPN 連接到 Tor。 假設 4 個月後，您的 ISP 再次想要識別 4 個月前使用過 Tor 的任何人。 他們的日誌幾乎肯定可以識別 4 個月前的流量，他們可能僅能看到所連接的 VPN IP 位址。 大多數 ISP 僅長期保留元數據，而不是您要求的流量完整內容。 儲存全部流量資料需要大量空間，而幾乎所有威脅行為者都不具備這種能力。

Because your ISP almost certainly is not capturing all packet-level data and storing it forever, they have no way of determining what you connected to with that VPN *after* the fact with an advanced technique like deep packet inspection, and therefore you have plausible deniability.

Therefore, bridges provide the most benefit when circumventing internet censorship *in the moment*, but they are not an adequate substitute for **all** the benefits that using a VPN alongside Tor can provide. 再次強調，這並不是*反對*使用 Tor 橋接器，但在做出決定時應該了解其限制。 在某些情況下，橋接器可能是*唯一*選項（例如，如果所有VPN 提供者都被封鎖），因此您仍然可以在這些情況下使用它們，但請記住此限制。

如果認為橋接器比 VPN 的加密隧道更能幫助防禦指紋識別或其他進階網路分析，那麼可以一直選擇將橋接器與 VPN 結合使用。 這樣，即使對手取得對 VPN 隧道某程度的可見性，您仍然受到可插拔傳輸混淆技術的保護。 如果決定走這條路，建議您連接到 VPN 後面的 obfs4 橋，以獲得最佳的指紋識別保護，而不是 meek 或 Snowflake。

It is [possible](https://discuss.privacyguides.net/t/clarify-tors-weaknesses-with-respect-to-observability/3676/16) that the [WebTunnel](https://forum.torproject.org/t/tor-relays-announcement-webtunnel-a-new-pluggable-transport-for-bridges-now-available-for-deployment/8180) pluggable transport currently being trialed may mitigate some of these concerns. 我們將繼續關注這項技術的發展。

## 其他資源

- [Tor 瀏覽器用戶手冊](https://tb-manual.torproject.org)
- [ Tor 如何運作 - Computerphile](https://invidious.privacyguides.net/embed/QRYzre4bf7I?local=true) <small>(YouTube)</small>
- [Tor O洋蔥服務- Computerphile](https://invidious.privacyguides.net/embed/lVcbq_a5N9I?local=true) <small>(YouTube)</small>

[^1]: 迴路中的第一個節點被稱為“入口守衛”或“守衛”。 它是一個快速和穩定的中繼站，作迴路中的第一個入口通常會維持 2~3個月，以防止已知的匿名破壞攻擊。 其餘的迴路則會依每次訪問網站而變化，這些中繼節點共同提供Tor  完整隱私保護。 了解更多關於守衛中繼的運作，請參考 [部落格文章](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) 和 [入口守衛論文paper](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf)。 ([https://support.torproject.org/tbb/tbb-2/](https://support.torproject.org/tbb/tbb-2/))

[^2]: 中繼標記：迴路位置（例如， “Guard” ， “Exit” ， “BadExit” ） ，迴路屬性（例如， “Fast” ， “Stable” ）或角色（例如， “Authority” ， “HSDir” ）這些中繼節點的特殊（ dis- ）資格，是由目錄機構分配並在目錄協議規範中進一步定義。 ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html))
