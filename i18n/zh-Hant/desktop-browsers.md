---
meta_title: "PC 和 Mac上隱私權尊重網頁瀏覽器的 - Privacy Guides"
title: "桌面瀏覽器"
icon: material/laptop
description: 這些網頁瀏覽器提供比 Google Chrome 更強大的隱私保護。
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": 網頁
    name: 私人桌面瀏覽器建議
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/zh-hant/browser
    applicationCategory: Web Browser
    operatingSystem:
      - Windows 作業系統
      - macOS
      - Linux
    subjectOf:
      "@type": 網頁
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Firefox
    image: /assets/img/browsers/firefox.svg
    url: https://firefox.com
    sameAs: https://zh.wikipedia.org/wiki/Firefox
    applicationCategory: Web Browser
    operatingSystem:
      - Windows 作業系統
      - macOS
      - Linux
    subjectOf:
      "@type": 網頁
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    sameAs: https://zh.wikipedia.org/wiki/Brave%E6%B5%8F%E8%A7%88%E5%99%A8
    applicationCategory: Web Browser
    operatingSystem:
      - Windows 作業系統
      - macOS
      - Linux
    subjectOf:
      "@type": 網頁
      url: "./"
---

這些是我們目前推薦的桌面網頁瀏覽器和標準/非匿名瀏覽的配置。 如果您重視強大的隱私保護和內建的的反指紋追蹤功能，我們推薦使用 [Mullvad 瀏覽器](#mullvad-browser)； 如果您在尋求 Google Chrome 的良好替代方案的休閒用網路瀏覽器，我們推薦使用 [Firefox](#firefox)；如果您需要 Chromium 的瀏覽器相容性，我們推薦使用 [Brave](#brave)。

如果您需要匿名瀏覽網際網路，應該使用 [Tor](tor.md)。 我們在此頁面提供一些設定建議，但除了 Tor 瀏覽器之外的所有瀏覽器都可能以某種方式或另一種方式被 *某人* 追蹤。

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Mullvad Browser 標誌](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad 瀏覽器**是移除 Tor 網路整合的 [Tor 瀏覽器](tor.md#tor-browser) 版本，，旨在為 VPN 使用者提供 Tor 瀏覽器的反指紋辨識技術。 它由 Tor Porject 開發並由 [Mullvad](vpn.md#mullvad)發佈，且不需要使用 Mullvad 的 VPN。

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "下載"</summary>

- [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

與 [Tor 瀏覽器](tor.md)一樣， Mullvad 瀏覽器旨在把 Mullvad 瀏覽器用戶的識別指紋弄得一樣，來防止指紋識別，它還包含預設安全級別自動配置的設置和擴展： *標準*， *更安全* 和 *最安全*。 因此，除了調整預設的 [安全等級](https://tb-manual.torproject.org/security-settings)之外，絕對不要修改瀏覽器。 其他修改將使您的指紋獨一無二，破壞使用此瀏覽器的目的。 如果您想重度配置瀏覽器，並且指紋不是問題，則建議使用 [Firefox](#firefox) 。

### 防指印辨識

**沒有** 使用 [VPN](vpn.md)， Mullvad 瀏覽器提供與其他私人瀏覽器（如Firefox +[Arkenfox](#arkenfox-advanced) 或 [Brave](#brave)）相同的保護，防止 [原生的指紋腳本](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) 。 Mullvad Browser 優異地提供這些保護，代價是沒有其它瀏覽器所具備的靈活性和便利。

==需要最強的防指紋辨識保護，建議使用 Mullvad 瀏覽器**搭配**  VPN==無論是 Mullvad VPN 或其它推薦的 VPN 提供商。 Mullvad 瀏覽器使用 VPN 時，您將與許多其他用戶共享指紋和 IP地址池，以讓您混在其中的“人羣”。 這種策略是阻止進階追蹤腳本的唯一方法，也是Tor Browser使用的相同反指紋技術。

請注意，雖然可以將 Mullvad 瀏覽器與任何 VPN 一起使用，但該 VPN 的其他人也必須使用 Mullvad瀏覽器 "人群"才會存在。比起其他提供商， Mullvad VPN 更可能存在相同的人群，特別是Mullvad 瀏覽器的推出。 Mullvad 瀏覽器沒有內建VPN 連接，也不會在瀏覽之前檢查是否使用 VPN，必須單獨配置和管理VPN 連接。

Mullvad 瀏覽器附帶預先安裝的 *uBlock Origin* 和 *NoScript* 擴充功能。 While we typically discourage adding *additional* [browser extensions](browser-extensions.md), these extensions that come pre-installed with the browser should **not** be removed or configured outside their default values, because doing so would noticeably make your browser fingerprint distinct from other Mullvad Browser users. 它還預先安裝了 Mullvad 瀏覽器擴展套件，但也可將之*安全地移除* ，並不會影響瀏覽器指紋，但即使不使用Mullvad VPN ，也可以安全地保留。

### 隱私瀏覽模式

Mullvad 瀏覽器永久以隱私瀏覽模式運行，這意味著歷史記錄、Cookie 和其他網站資料在每次關閉瀏覽器時都會被清除。 但書籤、瀏覽器設定和擴充功能設定仍會保留。

這是為了防止進階形式的跟蹤，但確實犧牲了方便和某些Firefox功能（例如多帳戶容器）為代價。 請記住，您可以隨時使用多個瀏覽器，例如，您可以考慮將Firefox + Arkenfox用於一些您希望保持登錄或在Mullvad瀏覽器中無法正常工作的網站，以及用於一般瀏覽的Mullvad瀏覽器。

### Mullvad Leta

Mullvad Browser 將DuckDuckGo 設置為預設的 [搜索引擎](search-engines.md)，它也預先安裝了 **Mullvad Leta**，這是需要訂閱 Mullvad VPN 才能訪問的搜索引擎。 Mullvad Leta 直接查詢 Google的付費搜索API （這是為什麼僅限於付費用戶） ，但由於這種限制， Mullvad 可以將搜索查詢與 Mullvad VPN 帳戶作關聯。 因此，不鼓勵使用 Mullvad Leta ，即使 Mullvad 收集關於其VPN 用戶的資訊很少。

## Firefox

<div class="admonition recommendation" markdown>

![Firefox標誌](assets/img/browsers/firefox.svg){ align=right }

**Firefox** 提供強大的隱私設定，例如[Enhanced Tracking Protection](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop) ，可以幫助阻止各種[類型的追蹤](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks)。

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://firefox-source-docs.mozilla.org){ .card-link title=Documentation}
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads "下載"</summary>

- [:simple-windows11: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning "警告"</p>

Firefox 在 Mozilla 網站的下載中包含一個獨特的[下載令牌](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0)，並使用 Firefox 中的遙測技術傳送令牌。 [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/)的更新**不**包含該令牌。

</div>

### Recommended Firefox Configuration

這些選項可以在 :material-menu: → **設置**中找到

#### 搜尋

- [ ] 取消勾選**提供搜尋建議**

搜尋建議功能可能無法在您所在的地區使用。

搜尋建議會將您在地址列中輸入的所有內容傳送至預設搜尋引擎，無論您是否實際提交搜尋。 禁用搜尋建議可讓您更精確地控制您傳送給搜尋引擎供應商的資料。

#### 隱私 & 安全

##### 增強的追蹤保護

- [x] Select **嚴格**加強型追蹤保護

通過封鎖社交媒體跟蹤器、指紋腳本（請注意，這並不能防止 *所有* 指紋的侵害）、加密挖礦器、跨站點跟蹤cookie和其他跟蹤內容來保護您。 ETP 可以防止許多常見威脅，但它不能阻止所有跟蹤途徑，因為它的設計對網站的可用性影響很小甚至沒有影響。

##### Firefox建議（僅限美國）

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) 功能只限美國地區，其類似於搜尋建議。 我們建議停用此功能的原因與我們建議停用搜尋建議的原因相同。 如果您在 **地址欄** 標題下沒有看到這些選項，則表示您沒有新的體驗，可以忽略這些變更。

- [ ] 取消勾選 **提供搜尋建議**
- [ ] 取消勾選 **贊助商的建議**

##### 關閉時消毒

如果您想在特定網站保持登錄狀態，可允許 **Cookies 和網站資料中的例外情況** → **管理例外情況...**

- [x] 勾選 **關閉 Firefox 時清除 Cookie 與網站資料**

這可以保護您免受持久性 Cookie 侵害，但不能保護您免受在任何一次瀏覽過程的 Cookie。 啟用此功能後，只需重新啟動 Firefox ，即可輕鬆清除您的瀏覽器 cookie。 您可以設定每個網站的例外情況，如果希望經常訪問的特定網站保持登錄。

##### 遙測

- [ ] 取消勾選 **允許 Firefox 傳送技術與互動資料給 Mozilla**
- [ ] 取消勾選k **允許 Firefox 安裝並進行研究**
- [ ] 取消勾選 **允許 Firefox 以您的身分自動回報錯誤報告**

> Firefox 會傳送有關 Firefox 版本和語言的資料；裝置作業系統和硬體配置；記憶體、有關崩潰和錯誤的基本資訊；更新、安全瀏覽和啟動等自動化程序的結果。 當 Firefox 將資料傳送給我們時，您的IP位址會作為伺服器記錄的一部分暫時收集。

此外，Firefox 帳號服務也會收集[一些技術資料](https://mozilla.org/privacy/firefox/#firefox-accounts)。 如果有使用 Firefox 帳戶，可選擇退出：

1. 在 accounts.firefox.com 開啟您的 [個人資料設定](https://accounts.firefox.com/settings#data-collection)
2. 取消勾選 **資料收集和使用** > **協助改善Firefox帳戶**

##### 純 HTTPS 模式

- [x] 選擇 **在所有視窗都開啟純 HTTPS 模式**

這可以防止您無意中連接到純文字 HTTP 網站。 如今，沒有 HTTPS 的網站已很少見，因此這對日常瀏覽幾乎沒有影響。

##### 通過 HTTPS 的 DNS

如在[HTTPS 底下](dns.md)使用 DNS:

- [x] 選取 **Max Protection** 與合適的供應商。

Max Protection 強制使用 HTTPS 上的 DNS，如果 Firefox 無法連線到安全 DNS 解析器，或安全 DNS 解析器表示所嘗試存取的網域的記錄不存在，則會顯示安全性警告。 這可以阻止秘密連接的網路降低了 DNS 安全性。

#### 同步

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) 可以在不同設備之間 E2EE 地傳輸同步瀏覽資料(訪問記錄與書籤等)。

### Arkenfox （進階）

<div class="admonition tip" markdown>
<p class="admonition-title">使用Mullvad 瀏覽器進階防指紋辨識</p>

[Mullvad瀏覽器](#mullvad-browser) 提供與 Arkenfox 相同的防指紋保護，不需要使用 Mullvad VPN 就能獲得這些保護。 再加上VPN ， Mullvad 瀏覽器可以阻擋 Arkenfox 無法處理的更先進追蹤腳本。 Arkenfox 仍具有更靈活的優勢，可以對需要繼續登錄的網站設置例外。

</div>

[Arkenfox 專案](https://github.com/arkenfox/user.js) 為 Firefox  提供一套完整的考量選項。 如果您 [決定](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) 使用Arkenfox ，則 [有幾個選項](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) 在主觀上嚴格而且可能導致某些網站無法正常運作- [可以輕鬆更改](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) 以滿足需求。  **強列建議**仔細看過他們完整的[維基頁wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox 也啟用[容器](https://support.mozilla.org/kb/containers#w_for-advanced-users)支援。

Arkenfox的目標只是通過Canvas隨機化和Firefox內置的指紋阻力配置設置來阻止基本或天真的跟蹤腳本。 它並不打算讓您的瀏覽器與其他 Arkenfox 用戶的大量混在一起，那是 Mullvad 瀏覽器或 Tor瀏覽器的作法，也是阻止進階指紋跟蹤腳本的唯一方法。 請記住，您可以隨時使用多個瀏覽器，例如，您可以考慮將Firefox + Arkenfox 用於希望保持登錄或可以信任的幾個網站，而 Mullvad 瀏覽器則用於一般瀏覽。

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** 內建內容封鎖程式和[隱私權功能](https://brave.com/privacy-features/) ，其中許多功能預設已啟用。

Brave 建立在 Chromium 瀏覽器專案，因此令人感到熟悉並且具有最小的網站兼容性問題。

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-windows11: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

**macOS 用戶：** 從 Brave 官網下載副檔名 `.pkg` 的安裝器，此需管理員權限方可執行(也可能會需執行其它非必要腳本在機器上)。 或者，自 [GitHub 發佈](https://github.com/brave/brave-browser/releases/latest) 頁下載 `Brave-Browser-universal.dmg`，其提供傳統"拖曳至應用程式資料夾"的安裝方式。

<div class="admonition warning" markdown>
<p class="admonition-title">Warning "警告"</p>

Brave 在官網的下載檔案中新增了 "[推廣碼](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" 用以追蹤該瀏覽器從何處下載，例如`BRV002` 下載的檔名為 `Brave-Browser-BRV002.pkg`。 安裝器在安裝程序尾端會使用推廣代碼來呼叫 Brave 伺服器。 如擔心此問題，可在開啟前更改安裝軟體的檔名。

</div>

### Recommended Brave Configuration

這些選項可以在 :material-menu: → **設定**中找到。

#### 設定

##### Shields

Brave [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) 功能中包含一些防指紋措施。 建議

全域配置這些選項</ a> 在造訪的所有頁面。</p> 

Shields 可以選擇根據需要依各網站情況降級，但我們建議預設以下內容：

<div class="annotate" markdown>

- [x] 選擇 **防止網站根據語言偏好進行指紋辨識**
- [x] 在追蹤器和廣告封鎖下選擇 **侵略性**

<details class="warning" markdown>
<summary>使用預設過濾器列表</summary>
Brave 可在內部 `brave://adblock`頁面中選擇其他內容過濾器。 我們建議您不要使用此功能；請保留預設的篩選條件清單。 使用額外清單將使您在一般 Brave 用戶中被突顯出來，如果Brave有漏洞，並將惡意規則添加到您使用的清單中，也可能會增加攻擊面。

</details>

- [x] 選擇 **嚴格** 位於**升級至 HTTPS 連線**選項底下
- [x] (可選的) 選取 **屏蔽 Scripts** (1)
- [x] 選取 **嚴格, 可能會破壞網站** 屏蔽瀏覽器識別指紋底下
- [x] 勾選**關閉此站後即遺忘** (2)
- [ ] 取消勾選所有的社交媒體元件

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode).
2. 若想在經常造訪的特定站點保持登入，則可以透過網址列中的盾牌圖示來為每個站點設定例外。



##### 隐私和安全

<div class="annotate" markdown>

- [x] 選取 **Disable non-proxied UDP** under [WebRTC IP Handling Policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] 取消選取 **使用 Google 服務來推送訊息**
- [ ] 取消選取 **同意隱私防護的產品分析 (P3A)**
- [ ] 取消選取 **自動發送每日使用呼叫至 Brave**
- [ ] 取消選取 **自動傳送診斷報告**
- [ ] 取消選取 **使用 Tor 的私密視窗** (1)

 !!!

</div>

1. Brave在瀏覽器指紋識別的抵抗力是 **不如** Tor 瀏覽器，且BraveTor 使用者少，容易被突出。 如果[需要強匿名性](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity)，請使用< a href="tor.md#tor-browser">Tor 瀏覽器</a>。

<div class="admonition tip" markdown>
<p class="admonition-title">關閉時消毒</p>

- [x] In the *Sites and Shields Settings* 選單中的“內容”下，點擊“裝置上網站資料”選單後，選擇“**關閉所有視窗時刪除已儲存至裝置的資料網站**”

如果希望保持登入到經常訪問的特定站點，可在「自訂行為」部分下針對每個站點設定例外。

</div>

##### 擴充套件

**Extensions**中關閉不使用的內建擴展套件

- [ ] 取消勾選 **Hangouts**
- [ ] 取消勾選 **WebTorrent**



##### Web3

Brave Web3 功能可能會增加瀏覽器指紋和攻擊面。 除非有用到任何功能，否則應停用這些功能。

- 在預設的 Ethereum 與 Solana 錢包底下選取 **Extensions (no fallback)**
- 設定 **禁用****解析 IPFS 資源的方法**



##### 系統

<div class="annotate" markdown>

- [ ] 取消勾選 **Brave 關閉時繼續執行應用程式** 以禁用背景應用程式(1)

</div>

1. 此功能並不適用於所有平臺。



#### Brave 同步

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) 可在不同設備上訪問瀏覽數據（歷史記錄，書籤等），而無需帳戶且具 E2EE保護。



#### 勇敢獎勵與錢包

** Brave 獎勵** 可讓您在 Brave 執行某些動作時獲得Basic Attention Token (BAT) 加密貨幣。 它依賴於來自特定數量的提供商的託管帳戶和KYC。 我們不建議 BAT 作為 [私有加密貨幣](cryptocurrency.md)，也不建議使用 [保管錢包](advanced/payments.md#other-coins-bitcoin-ethereum-etc)，因此不鼓勵使用此功能。

**Brave Wallet** 在您的電腦上進行本地操作，但不支援任何私人加密貨幣，因此不鼓勵使用此功能。



## 其他資源



## 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。



### 最低合格要求

- 必須是開源軟體。
- 支援自動更新。
- 從上遊版本開始在0-1天內接收引擎更新。
- 適用於Linux、macOS和Windows。
- 為了使瀏覽器更尊重隱私權而作的任何變動都不應對用戶體驗產生負面影響。
- 預設情況下會封鎖第三方Cookie。
- Supports [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]



### 最佳案例

最佳案例標準代表了我們希望從這個類別的完美項目應具備的功能。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 包括內置的內容攔截功能。
- 支持cookie分割（à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)）。
- 支援漸進式網絡應用程式 PWA 可讓您安裝某些網站，就像是電腦上的原生應用程式一樣。 這可能比安裝 Electron 應用程式更有優勢，因為您可以受益於瀏覽器定期安全更新。

- 不包括不影響用戶隱私的附加功能(bloatware)。

- 預設情況下不收集遙測。
- 提供開源同步伺服器實作。
- 預設為 [私密搜尋引擎](search-engines.md)。



[^1]:    
    Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
