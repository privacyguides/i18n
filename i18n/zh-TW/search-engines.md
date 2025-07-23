---
meta_title: "推薦搜尋引擎：匿名的 Google 替代方案 - Privacy Guides"
title: "搜尋引擎"
icon: material/search-web
description: 尊重隱私的搜尋引擎，不會根據您的搜尋紀錄建立廣告檔案。
cover: search-engines.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>防護下列威脅：</small>

- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

使用不會根據您的搜尋紀錄建立廣告檔案的 **搜尋引擎** 。

## 推薦的提供商

根據各家服務的隱私權政策，我們建議這些不會收集個人識別資訊（PII）的搜尋引擎。 **不能保證**這些隱私權政策都有好好落實。

如果您的威脅模型需要向搜尋供應商隱藏您的IP位址，請考慮使用 [VPN](vpn.md) 或 [Tor](tor.md) 。

| 供應商                           | 搜尋索引                                                                                                                                                                        | Tor 隱藏服務                      | 記錄日誌 / 隱私權政策 | 營運國家 |
| ----------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- | ------------ | ---- |
| [Brave Search](#brave-search) | [獨立的](https://brave.com/search-independence)                                                                                                                                | :material-check:{ .pg-green } | 匿名化[^1]      | 美國   |
| [DuckDuckGo](#duckduckgo)     | [Bing](https://help.duckduckgo.com/results/sources)                                                                                                                         | :material-check:{ .pg-green } | 匿名化[^2]      | 美國   |
| [Startpage](#startpage)       | [Google 與 Bing](https://support.startpage.com/hc/articles/4522435533844-What-is-the-relationship-between-Startpage-and-your-search-partners-like-Google-and-Microsoft-Bing) | :material-check:{ .pg-green } | 匿名化[^3]      | 荷蘭   |

### Brave Search

<div class="admonition recommendation" markdown>

![Brave Search logo](assets/img/search-engines/brave-search.svg){ align=right }

**Brave Search** 由 Brave 開發的搜尋引擎。 該索引是針對 Google 搜索進行優化，因此與其他替代方案相比，可以提供更具上下文準確性的結果。

Brave Search 包括獨特的功能，如[討論](https://search.brave.com/help/discussions)，突出了對話為中心的結果，如論壇文章。

[:octicons-home-16: 首頁](https://search.brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://search.brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="洋蔥服務" }
[:octicons-eye-16:](https://search.brave.com/help/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://search.brave.com/help){ .card-link title=說明文件}

</div>

請注意，如果您在登入 Premium 帳戶時使用 Brave Search，可能會讓 Brave 更容易將查詢與特定使用者相關聯。

我們建議停用 [Anonymous usage metrics（匿名使用指標）](https://search.brave.com/help/usage-metrics) ，它預設為啟用，可在設定中停用。

### DuckDuckGo

<div class="admonition recommendation" markdown>

![DuckDuckGo logo](assets/img/search-engines/duckduckgo.svg){ align=right }

**DuckDuckGo** 最主流的隱私搜尋引擎選項之一。 著名的 DuckDuckGo 搜索功能包括 [bangs](https://duckduckgo.com/bang)和許多[即時答案](https://help.duckduckgo.com/duckduckgo-help-pages/features/instant-answers-and-other-features)。 此搜尋引擎使用 Bing 以外的眾多[來源](https://help.duckduckgo.com/results/sources) 來獲取即時答案和其他非主要結果。

DuckDuckGo 是 [Tor瀏覽器](tor.md#tor-browser) 的預設搜尋引擎，也是 Apple 的 [Safari 瀏覽器](mobile-browsers.md#safari-ios) 上為數不多的可用選項之一。

[:octicons-home-16: 首頁](https://duckduckgo.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion){ .card-link title="洋蔥服務" }
[:octicons-eye-16:](https://duckduckgo.com/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://help.duckduckgo.com){ .card-link title=說明文件}

</div>

DuckDuckGo 提供 [另外](https://help.duckduckgo.com/features/non-javascript) 兩種版本搜尋引擎，兩者皆不需要JavaScript。 然而，這些版本缺少特色。 這些版本也可以透過 Tor 洋蔥網址各自附加[ /lite ](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/lite)或[/html](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/html) 的版本。

### Startpage

<div class="admonition recommendation" markdown>

![Startpage logo](assets/img/search-engines/startpage.svg#only-light){ align=right }
![Startpage logo](assets/img/search-engines/startpage-dark.svg#only-dark){ align=right }

**Startpage** 私密搜索引擎。 Startpage 的獨特功能之一是 [匿名視圖](https://startpage.com/en/anonymous-view/) ，它努力標準化用戶活動，使其更難被突出識別。 這個功能可用來隱藏 [某些](https://support.startpage.com/hc/articles/4455540212116-The-Anonymous-View-Proxy-technical-details) 網路與瀏覽器特徵。 不像其名字所示，它並不會使您匿名。 如果您正在尋找匿名性，請改用 [Tor瀏覽器](tor.md#tor-browser)。

[:octicons-home-16: 首頁](https://startpage.com){ .md-button .md-button--primary }
[:simple-torbrowser:](http://startpagel6srwcjlue4zgq3zevrujfaow726kjytqbbjyrswwmjzcqd.onion){ .card-link title="洋蔥服務" }
[:octicons-eye-16:](https://startpage.com/en/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://support.startpage.com/hc/categories/4481917470356-Startpage-Search-Engine){ .card-link title=說明文件}

</div>

Startpage 大股東是System1，它是一家廣告技術公司。 我們不認為這是問題，因為他們有明顯分開的 [隱私政策](https://system1.com/terms/privacy-policy)。 Privacy Guides 團隊曾於[2020年聯繫 Startpage ](https://web.archive.org/web/20210118031008/https://blog.privacytools.io/relisting-startpage)，以消除對 System1對該服務大量投資的擔憂，我們滿意其回覆。

Startpage 先前限制了 VPN 和[Tor](tor.md) 用戶，但他們最近創建[官方](https://support.startpage.com/hc/en- us/ articles/24786602537364-Startpage-s-Tor-onion-service) Tor 隱藏服務，截至2024 年4 月，不再看到對Tor 或[VPN](vpn.md) 用戶施以額外障礙。

## Metasearch 搜尋引擎

[元搜尋引擎](https://en.wikipedia.org/wiki/Metasearch_engine)聚合其他搜尋引擎的結果，例如上面建議的搜尋引擎，但本身不儲存任何資訊。

### SearXNG

<div class="admonition recommendation" markdown>

![SearXNG logo](assets/img/search-engines/searxng.svg){ align=right }

**SearXNG** 是開源、可自架的元搜尋引擎。 它是一個積極維護的 [SearX](https://github.com/searx/searx) 分支。

[:octicons-home-16: Homepage](https://searxng.org){ .md-button .md-button--primary }
[:octicons-server-16:](https://searx.space){ .card-link title="Public Instances"}
[:octicons-code-16:](https://github.com/searxng/searxng){ .card-link title="Source Code" }

</div>

SearXNG 是您和它所聚合的搜尋引擎之間的代理。 您的搜尋查詢仍會傳送至 SearXNG 取得搜尋結果的搜尋引擎。

在自我託管時，重要的是要讓其他人使用您的實例，以便查詢能夠混入其中。 您應該小心處理 SearXNG 託管，因為若有人在您的執行實例上查找非法內容，可能會引起當局的關注。

當您使用 SearXNG 實體時，請務必閱讀他們的隱私權政策。 由於 SearXNG 實體可能會被其擁有者修改，因此它們不一定反映其隱私政策。 有些實體是以 Tor 隱藏服務運行，只要您的搜尋查詢不包含 PII ，這可能會授予一些隱私。

## 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 不得根據其隱私權政策收集 PII。
- 不得要求使用者建立帳戶。

### 最佳情況

最佳情況標準代表我們希望在這個類別的完美項目的應具備的特性。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 應該以開源軟體為基礎。
- 不應該封鎖 Tor退出節點的 IP位址。

[^1]: Brave Search 收集匯總的使用指標，其中包括作業系統和使用者代理程式。 不過他們並未收集 PII。 為提供[匿名本地結果（anonymous local results）](https://search.brave.com/help/anonymous-local-results)，IP 位址會被暫時處理，但不會保留。 [https://search.brave.com/help/privacy-policy](https://search.brave.com/help/privacy-policy)
[^2]: DuckDuckGo **會為產品改進目的記錄** 搜索，但不會記錄您的 IP 位址或任何其他 PII。 [https://duckduckgo.com/privacy](https://duckduckgo.com/privacy)
[^3]: Startpage 記錄詳細信息，例如作業系統、用戶代理和語言。 他們不會記錄 IP 位址、搜尋查詢或其他 PII。 [https://startpage.com/en/privacy-policy](https://startpage.com/en/privacy-policy)
