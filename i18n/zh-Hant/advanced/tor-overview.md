---
title: "Tor 簡介"
icon: 'simple/torproject'
description: Tor 是一個免費使用的去中心化網路，其讓用戶在使用網際網路之際盡可能地保護自己的隱私。
---

![Tor logo](../assets/img/self-contained-networks/tor.svg){ align=right }

[Tor </strong>](../alternative-networks.md#tor)是一個免費使用的去中心化網路，其讓用戶在使用網際網路之際盡可能地保護自己的隱私。 如果使用得當，該網路可以實現私人和匿名瀏覽和通訊。 很難阻止和追蹤 Tor 流量，因此它是一種有效的審查規避工具。

Tor 的工作原理是通過志願者運營的服務器來引導您的網際網路路徑，而不是直接連接到您試圖訪問的網站。 這樣可以混淆流量來源，所連接的伺服器都無法看到流量來去的完整路徑，也意味著即使您連接的伺服器無法破壞您的匿名性。

[:octicons-home-16:](https://torproject.org){ .card-link title=首頁 }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="洋蔥服務" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=文檔}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="原始碼" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=捐款 }

## 安全連接Tor

在連接到 Tor 之前，應先仔細考慮想透過 Tor 實現什麼目的，想要對誰隱藏網路活動資訊。

在自由的國家，透過 Tor 存取普通內容，無需擔心 ISP 或本地網路管理員知道您正在使用 Tor，反而可能會幫助 [消除Tor 使用污名化](https://2019.www.torproject.org/about/torusers.html.en) ，您可以透過標準方式直接連接到Tor，例如[Tor 瀏覽器](../tor.md)。

如果您有能力使用可信任的 VPN 供應商，且有**以下任一情況**，那麼最好應透過 VPN 連接 Tor：

- 已使用[可信任的 VPN 服務](../vpn.md)
- 威脅模型包括能夠從 ISP 提取資訊的對手。
- 您的威脅模型將 ISP 作為對手
- 您的威脅模型包括本地網路管理員，再來是您的 ISP 成為敵對方

由於各種原因，我們已[一般建議](../basics/vpn-overview.md)絕大多數人使用值得信賴的VPN 提供商，以下有關透過 VPN 連接到Tor的建議可能適用。 <mark>在連接到 Tor 之前無需停用 VPN</mark>，某些線上資源讓您相信這一點。

直接連接到 Tor 將使您的連接在任何本地網路管理員或 ISP 面前脫穎突出。 網路管理員過去已[偵測並將此類流量作關聯性](https://edition.cnn.com/2013/12/17/justice/massachusetts-harvard-hoax)，以識別網路上的特定 Tor 使用者並對其進行去匿名化。 另一方面，連接 VPN 並不會太可疑，因為日常消費者使用商業 VPN 服務來執行各種日常任務例如繞過地理限制，即使在網路限制嚴格的國家也是如此。

所以應在**在**連接到 Tor 網路之前盡力隱藏自己的 IP 位址。 只需連接到VPN（透過電腦上安裝的客戶端），然後正常存取[Tor](../tor.md)（例如透過Tor 瀏覽器）即可做到這一點。 這將建立一個連接鏈，例如：

- [x] 你 → VPN → Tor → 網際網路

從 ISP 的角度來看，用戶似乎正在存取 VPN（提供的相關保護）。 從 VPN 角度，他們可以看到您正在連接到 Tor 網絡，但看不到您訪問哪些網站。 從Tor 角度，可以正常連接，但萬一發生某種 Tor 網路洩露的情況（不太可能發生），只有 VPN 的IP 會被暴露，且所用的VPN 也會*額外*妥協才能使您去匿名化。

這**不是**規避審查的建議，如 Tor 被 ISP 完全封鎖， VPN 也可能遭封鎖。 相反，此建議旨在使流量與常見 VPN 用戶流量更好地融合，透過掩蓋從 ISP 連接到 Tor 的事實來提供某種程度的合理推諉。

---

我們**強烈反對**以任何其他方式將 Tor 與 VPN 結合。 不要以下任何相似方式配置連接：

- 你 → Tor → VPN → 網際網路
- 你 → VPN → Tor → VPN → 網際網路
- 任何其它設定

有些 VPN 提供者和其他出版物會推薦這些**不良**配置，以逃避某些地區的 Tor 禁令（出口節點被網站阻止）。 [通常](https://support.torproject.org/#about_change-paths)，Tor 會經常更改通過網路的迴路路徑。 當選擇永久*目的地* VPN（在*Tor 之後*連接到VPN 伺服器）時，就消除了此番優勢且嚴重損害匿名性。

此類不良配置很難無意中完成，因為它通常涉及在 Tor 瀏覽器內設置自訂代理設置，或在 VPN 用戶端內設置自訂代理設定（透過 Tor 瀏覽器路由 VPN 流量）。 只要避免這些非預設配置，可能就沒問題。

---

<div class="admonition info" markdown>
<p class="admonition-title">VPN/SSH 指紋</p>

Tor Project [指出](https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN#vpnssh-fingerprinting) *理論上*使用 VPN 對 ISP 隱藏 Tor 活動可能並非萬無一失。 人們發現 VPN 很容易受到網站流量指紋辨識的影響，攻擊者仍然可猜測正在造訪哪個網站，因為所有網站都有特定的流量模式。

因此，相信 VPN 隱藏的加密 Tor 流量也可以透過類似的方法被偵測，這並非沒道理。 沒有這個主題的研究論文，我們仍然認為使用 VPN 的好處遠遠超過這些風險，但需要記住這點。

如果仍認為可插拔傳輸（橋接器）可以針對網站流量指紋識別提供 VPN 無法提供的額外保護，那麼可以選擇結合使用橋接器**和** VPN。

</div>

確定是否應該先使用 VPN 連接到 Tor 網絡需要一些常識和了解當地政府和 ISP 與所連接內容的政策。 然而在多數情況下，最好被視為連接到商業 VPN 網絡，而不是直接連到 Tor 網路。 如果VPN 服務商在您的地區受到審查，那麼也可以考慮使用Tor 可插拔傳輸（例如 Snowflake 或 meek ）作為替代方案，但使用這些橋接器可能比標準WireGuard/OpenVPN 隧道引起更多懷疑。

## Tor 並非是

Tor 網路並非在任何情況下都是完美的隱私保護工具，其存在一些應仔細考慮的缺點。 如果 Tor 適合您的需求，則這些缺點不應阻止 Tor 使用，但在決定哪種解決方案最適合時仍然需要考慮這些問題。

### Tor 不是免費的 VPN

*Orbot* 行動應用，讓許多人誤將 Tor 描述為適用所有裝置流量的「免費 VPN」。 然而，與典型的 VPN 相比，這樣使用 Tor 會有某些危險。

不同於 Tor 出口節點，VPN 服務商通常不會*主動*[惡意](#caveats)。 Tor 出口節點可由任何人創建，它們是網路日誌記錄和修改的熱點。 2020 年許多 Tor 出口節點被記錄將 HTTPS 流量降級為 HTTP，以便[「劫持」加密貨幣交易](https://therecord.media/thousands-of-tor-exit-nodes-attacked-cryptocurrency-users-over-the-past-year)。 其他出口節點攻擊，例如用惡意軟體替換通過未加密通道的下載。 HTTPS 確實某程度緩解了這些威脅。

正如我們已提過的，Tor 在網路上很容易識別。 與實際的 VPN 服務不同，使用 Tor 會讓您成為可能試圖逃避當局的人。 在理想的世界中，Tor 會被網路管理員和當局視為一種多種用途的工具（就像如何看待VPN）。但現實中，Tor 的認知仍然遠不如承認商業 VPN 的正當性，因此使用真正的 VPN 提供看似合理的推諉，例如 「我只是用它來觀看 Netflix，」等等。

### Tor 的使用並非無法偵測

**即便使用橋接器和可插拔傳輸，**Tor 專案並未提供任何工具來對ISP 隱藏正在使用 Tor 的事實。 即使使用模糊的「可插拔傳輸」或非公共橋接器也不能隱藏正在使用私人通訊通道的事實。 最受歡迎的可插拔傳輸，例如obfs4（將流量混淆為「看起來沒什麼」）和meek（使用網域前置來偽裝流量）可以是[使用相當標準的流量分析技術檢測](https://www.hackerfactor.com/blog/ index.php?/archives/889-Tor-0day-Burning-Bridges.html)。 Snowflake 也有類似的問題， *在 Tor 連線建立之前*[很容易被偵測到](https://hackerfactor.com/blog/index.php?/archives/944-Tor-0day-Snowflake.html)。

還有這三種以外的可插拔傳輸，但通常依賴透過隱蔽性來逃避偵測的安全性。 它們不是不可能被檢測，只是使用者太少，以至於不值得為它們建立檢測器。 如果特別遭受監控，則不應依賴它們。

了解繞過審查和逃避檢測兩者的差異很重要。 要實現前者更容易，因為網路審查員實際上存在許多現實限制，但這些技術並沒有掩蓋這個事實：監視網路使用的相關單位知道您——*的確在* — —使用Tor 。

### Tor 瀏覽器不是最*安全*的瀏覽器

匿名性常常與安全性相矛盾：Tor 的匿名性要求每個使用者都是相同的，這會造成單一文化（所有 Tor 瀏覽器使用者都存在相同的錯誤）。 依網路安全的經驗法則，單一文化通常認為不好：透過多樣性（Tor 所缺乏的）實現安全性，透過將漏洞限制在較小的群體中，提供了自然隔離通常是可取的，但這種多樣性對於匿名性來說也不太有利。

此外，Tor 瀏覽器是 Firefox 的擴展支援版本，僅接收被視為*嚴重*和*高*漏洞的補丁>（不是*中*和*低*）。 這意味著攻擊者可以（例如）：

1. 在 Firefox nightly 或 beta 版本中尋找新的嚴重/高危險漏洞，然後檢查它們可否利用在 Tor 瀏覽器（此漏洞週期可能會持續數週）。
2. 將*多個*中/低漏洞連結在一起，直到它們獲得所需的存取等級（此漏洞週期可能會持續數月或更長時間）。

面臨瀏覽器漏洞風險者應考慮採取額外的保護措施來防禦Tor 瀏覽器漏洞，例如在[Qubes](../os/qubes-overview.md) 使用Whonix 來限制 Tor 瀏覽安全的虛擬器並防止洩漏。

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
- Tor 出口節點可以**修改**通過的未加密流量。 這意味著未加密的流量（例如純 HTTP 流量）可能會被惡意出口節點變更。 **切勿**透過Tor 從未加密的`http://` 網站下載文件，確保瀏覽器設定為始終將HTTP 流量升級為HTTPS。
- Tor 出口節點還可以監控通過它們的流量。 包含個人識別資訊的未加密流量可能會讓您在該出口節點被消除匿名。 再次強調，建議僅透過 Tor 使用 HTTPS。
- 能被動監視全球*所有*網路流量的強大對手（「全球被動對手」）**並不是** Tor 所能防禦的對手（即便將​​Tor [與VPN](#safely-connecting-to-tor) 也無法改變此一事實）。
- 資金雄厚、能夠被動監視全球*大多數*網路流量的對手仍然有*機會*通過進階流量分析去匿名化Tor 用戶。

如果您希望使用 Tor 瀏覽網頁，我們只建議使用 **官方** Tor 瀏覽器：它旨在防止指紋。

- [Tor 瀏覽器 :material-arrow-right-drop-circle:](../tor.md#tor-browser)

### 橋接器提供的保護

Tor 橋接器通常被認為是向 ISP 隱藏 Tor 使用情況的替代方法，而不是 VPN（我們建議盡可能使用後者 ）。 需要考慮的是，雖然橋接器可以提供足夠的審查規避，但這只是*暫時*的好處。 它們無法充分保護您，防止 ISP 透過歷史流量日誌分析發現您*過去*連接 Tor。

請考慮以下場景來理解：透過橋接器連接到 Tor，而 ISP 沒有偵測到它，因為他們沒有對流量進行複雜分析，因此一切都按預期進行。 現在，4個月過去，橋接器 IP 已經公開了。 這種情況在橋接器中很常見，它們被發現並被封鎖的頻率相對較高，但不是立即發生。

您的 ISP 想要辨識出 4 個月前 Tor 用戶，透過其有限的元資料記錄，他們可以看到您連接到的 IP 位址其實是 Tor 橋接器。 您幾乎沒有其他藉口進行此類連接，因此 ISP 可以非常有信心地說您當時是 Tor 用戶。

對比我們所推薦的場景，透過 VPN 連接到 Tor。 假設 4 個月後，您的 ISP 再次想要識別 4 個月前使用過 Tor 的任何人。 他們的日誌幾乎肯定可以識別 4 個月前的流量，他們可能僅能看到所連接的 VPN IP 位址。 大多數 ISP 僅長期保留元數據，而不是您要求的流量完整內容。 儲存全部流量資料需要大量空間，而幾乎所有威脅行為者都不具備這種能力。

ISP 肯定不會截取所有資料包級資料與將其永久存儲，他們*無法利用深度資料包檢查等先進技術* 來確認通過VPN 連接的內容，因此你有合理的推諉能力。

因此，橋接器在規避網路審查時提供了最大的好處，但*目前*它們還未能充分取代**所有</em >結合使用 VPN 和 Tor 的好處。 再次強調，這並不是*反對*使用 Tor 橋接器，但在做出決定時應該了解其限制。 在某些情況下，橋接器可能是*唯一*選項（例如，如果所有VPN 提供者都被封鎖），因此您仍然可以在這些情況下使用它們，但請記住此限制。</p>

如果認為橋接器比 VPN 的加密隧道更能幫助防禦指紋識別或其他進階網路分析，那麼可以一直選擇將橋接器與 VPN 結合使用。 這樣，即使對手取得對 VPN 隧道某程度的可見性，您仍然受到可插拔傳輸混淆技術的保護。 如果決定走這條路，建議您連接到 VPN 後面的 obfs4 橋，以獲得最佳的指紋識別保護，而不是 meek 或 Snowflake。

[可能](https://discuss.privacyguides.net/t/clarify-tors-weaknesses-with-respect-to-observability/3676/16)目前正在試驗中的[WebTunnel](https:// forum.torproject.org/t/tor-relays-announcement-webtunnel-a-new-pluggable-transport-for-bridges-now-available-for-deployment/8180) 可插拔傳輸可以減輕其中一些擔憂。 我們將繼續關注這項技術的發展。

## 其他資源

- [Tor 瀏覽器用戶手冊](https://tb-manual.torproject.org)
- [ Tor 如何運作 - Computerphile](https://invidious.privacyguides.net/embed/QRYzre4bf7I?local=true) <small>(YouTube)</small>
- [Tor O洋蔥服務- Computerphile](https://invidious.privacyguides.net/embed/lVcbq_a5N9I?local=true) <small>(YouTube)</small>

[^1]: 迴路中的第一個節點被稱為“入口守衛”或“守衛”。 它是一個快速和穩定的中繼站，作迴路中的第一個入口通常會維持 2~3個月，以防止已知的匿名破壞攻擊。 其餘的迴路則會依每次訪問網站而變化，這些中繼節點共同提供Tor  完整隱私保護。 了解更多關於守衛中繼的運作，請參考 [部落格文章](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) 和 [入口守衛論文paper](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf)。 ([https://support.torproject.org/tbb/tbb-2/](https://support.torproject.org/tbb/tbb-2))

[^2]: 中繼標記：迴路位置（例如， “Guard” ， “Exit” ， “BadExit” ） ，迴路屬性（例如， “Fast” ， “Stable” ）或角色（例如， “Authority” ， “HSDir” ）這些中繼節點的特殊（ dis- ）資格，是由目錄機構分配並在目錄協議規範中進一步定義。 ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html))
