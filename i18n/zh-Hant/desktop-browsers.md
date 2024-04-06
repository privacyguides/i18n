---
meta_title: "尊重隱私的 PC 和 Mac 網路瀏覽器 - Privacy Guides"
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

這些是我們目前推薦的桌面網路瀏覽器和標準/非匿名瀏覽的設定。 如果您重視強大的隱私保護和內建的的反指紋追蹤功能，我們推薦使用 [Mullvad 瀏覽器](#mullvad-browser)；如果您在尋求 Google Chrome 的良好替代方案的休閒用網路瀏覽器，我們推薦使用 [Firefox](#firefox)；如果您需要 Chromium 的瀏覽器相容性，我們推薦使用 [Brave](#brave)。

如果您需要匿名瀏覽網際網路，應該使用 [Tor](tor.md)。 我們在此頁面提供一些設定建議，但除了 Tor 瀏覽器以外的所有瀏覽器都可能以某種方式或另一種方式被 *某人* 追蹤。

## Mullvad 瀏覽器

<div class="admonition recommendation" markdown>

![Mullvad 瀏覽器標誌](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad 瀏覽器**是移除 Tor 網路整合的 [Tor 瀏覽器](tor.md#tor-browser) 版本，，旨在為 VPN 使用者提供 Tor 瀏覽器的反指紋辨識技術。 它由 Tor Porject 開發並由 [Mullvad](vpn.md#mullvad)發佈，且不需要使用 Mullvad 的 VPN。

[:octicons-home-16: 首頁](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="文件" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

與 [Tor 瀏覽器](tor.md)類似，Mullvad 瀏覽器旨在通過使您的瀏覽器指紋與其他 Mullvad 瀏覽器用戶相同來防止指紋識別，並且它還包括根據安全等級自動配置的設定和擴充功能，分為 *標準*、*較安全* 和 *最安全* 三個等級。 因此，除了調整預設的[安全等級](https://tb-manual.torproject.org/security-settings)外，請絕對不要對瀏覽器進行任何修改。 其他修改將使您的指紋變得獨特，從而打破使用此瀏覽器的目的。 如果您希望對瀏覽器進行更多配置，且指紋識別對您來說不是問題，我們建議使用 [Firefox](#firefox)。

### 防止指紋識別

在**不**使用 [VPN](vpn.md) 的情況下，Mullvad 瀏覽器可提供與其他私人瀏覽器 (例如 Firefox + [Arkenfox](#arkenfox-advanced) 或 [Brave](#brave)) 相同的防護措施，以對抗[單純的指紋辨識腳本](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting)。 Mullvad 瀏覽器在開箱即用的情況下提供了這些保護措施，代價是可能會牺牲其他私密瀏覽器所具備的靈活性和便利性。

==要獲得最強大的防指紋辨識防護，我們建議將 Mullvad 瀏覽器 **搭配** VPN 一同使用== ，不論是 Mullvad 或其他推薦的 VPN 供應商皆可。 當您將 VPN 與 Mullvad 瀏覽器搭配使用時，您將與許多其他使用者共用一個指紋和 IP 位址池，以讓你混在「人群」之中。 這個策略是阻止進階追蹤腳本的唯一方法，也是 Tor Browser 使用的相同防指紋辨識技術。

請注意，雖然您可以將 Mullvad 瀏覽器與任何 VPN 供應商一起使用，但該 VPN 上的其他使用者也必須使用 Mullvad 瀏覽器，才能形成這個「人群」，而這在 Mullvad VPN 上比其他供應商更有可能發生，特別是在 Mullvad 瀏覽器推出後不久。 Mullvad 瀏覽器沒有內建 VPN，也不會在瀏覽之前檢查是否使用 VPN，必須另外設定和管理 VPN 連線。

Mullvad 瀏覽器附帶預先安裝的 *uBlock Origin* 和 *NoScript* 擴充功能。 我們通常不建議新增*額外*的[瀏覽器擴充功能](browser-extensions.md)，且這些與瀏覽器預裝的擴充功能**不**應移除或在預設值以外進行設定，一旦隨意更動，您的瀏覽器指紋會明顯有別於其他 Mullvad 瀏覽器使用者。 它還預先安裝了 Mullvad 瀏覽器擴充功能，但也*可*將其安全地移除，而不會影響您的瀏覽器指紋，但即使您不使用 Mullvad VPN，也可以安全地保留它。

### 隱私瀏覽模式

Mullvad 瀏覽器預設總是使用隱私瀏覽模式運行，這意味著您的歷史記錄、Cookie 和其他網站資料在每次關閉瀏覽器時都會被清除。 但書籤、瀏覽器設定和擴充功能設定仍會保留。

這是為了防止進階形式的追蹤，但確實犧牲了便利性和一些 Firefox 功能，例如多重帳戶容器 (Multi-Account Containers，又稱容器分頁功能)。 請記住，您隨時可以使用多個瀏覽器，例如，您可以考慮對希望保持登入狀態或在 Mullvad 瀏覽器中無法正常運作的幾個網站使用 Firefox + Arkenfox，而在一般瀏覽時使用 Mullvad 瀏覽器。

### Mullvad Leta

Mullvad 瀏覽器將 DuckDuckGo 設為預設的[搜尋引擎](search-engines.md)，它也預先安裝了 **Mullvad Leta**，一個需要訂閱 Mullvad VPN 才能使用的搜尋引擎。 Mullvad Leta 使用 Google 的付費搜尋 API (這就是為什麼它僅限於付費訂閱者)，但由於這種限制，Mullvad 可以把搜尋查詢和 Mullvad VPN 帳戶進行關聯。 因此，我們不建議使用 Mullvad Leta，即使 Mullvad 僅收集極少量的 VPN 訂閱者資訊。

## Firefox

<div class="admonition recommendation" markdown>

![Firefox 標誌](assets/img/browsers/firefox.svg){ align=right }

**Firefox** 提供強大的隱私設定，例如[加強型追蹤保護功能](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop)，可以幫助阻擋各種[類型的追蹤](https://support.mozilla.org/zh-TW/kb/enhanced-tracking-protection-firefox-desktop#w_jia-qiang-xing-zhui-zong-bao-hu-gong-neng-hui-feng-suo-shi-mo)。

[:octicons-home-16: 首頁](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://firefox-source-docs.mozilla.org){ .card-link title="文件" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="原始碼" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="捐贈" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-windows11: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Firefox 在 Mozilla 網站的下載中包含一個獨特的[下載令牌](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0)，並使用 Firefox 中的遙測傳送該令牌。 該令牌**不**包含在 [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/) 上的發行版中。

</div>

### 建議的 Firefox 設定

這些選項可以在 :material-menu: → **設定** 中找到

#### 搜尋

- [ ] 取消勾選**顯示搜尋建議**

搜尋建議功能可能無法在您所在的地區使用。

搜尋建議會將您在地址列中輸入的所有內容傳送至預設搜尋引擎，無論您是否實際提交搜尋。 禁用搜尋建議可讓您更精確地控制您傳送給搜尋引擎供應商的資料。

#### 隱私 & 安全

##### 加強型追蹤保護功能

- [x] 選擇 **嚴格** 加強型追蹤保護

通過封鎖社交媒體追蹤器、指紋辨識腳本 (請注意，這無法保護您免於*所有*的指紋辨識)、加密貨幣採礦程式、跨網站 Cookie 和其他追蹤內容來保護您。 加強型追蹤保護功能可保護您免於許多常見威脅，但它不能阻止所有追蹤途徑，因為它被設計為對網站的可用性影響極小或沒有影響。

##### Firefox Suggest (僅限美國)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) 功能只限美國地區，其功能類似於搜尋建議。 我們建議停用此功能的原因與我們建議停用搜尋建議的原因相同。 如果您在 **網址列** 標題下沒有看到這些選項，則表示您還不能使用此功能，可以忽略這些變更。

- [ ] 取消勾選 **Suggestions from the web**
- [ ] 取消勾選 **Suggestions from sponsors**

##### 關閉時清除資料

如果您想在特定網站保持登入，可以在 **Cookie 與網站資料** → **管理例外網站…** 中允許例外。

- [x] 勾選 **關閉 Firefox 時清除 Cookie 與網站資料**

這可以保護您免受持久性 Cookie 的影響，但不能保護您免受在任何一次瀏覽階段的 Cookie。 啟用此功能後，只需重新啟動 Firefox，就能輕鬆清除瀏覽器 Cookie。 如果您希望在經常造訪的特定網站保持登入，可以針對每個網站設定例外。

##### 遙測

- [ ] 取消勾選 **允許 Firefox 傳送技術與互動資料給 Mozilla**
- [ ] 取消勾選k **允許 Firefox 安裝並進行研究**
- [ ] 取消勾選 **允許 Firefox 以您的身分自動回報錯誤報告**

> Firefox 會向我們發送以下數據：您的 Firefox 版本和語言；操作系統和硬體配置；記憶體、關於崩潰和錯誤的基本訊息；更新、安全瀏覽和啟動等自動化流程系統的結果。 當 Firefox 向我們發送數據時，會將您的 IP 位址作為伺服器日誌的一部份暫時收集。

此外，Firefox 帳號服務也會收集[一些技術資料](https://mozilla.org/privacy/firefox/#firefox-accounts)。 如果有使用 Firefox 帳戶，您可以選擇退出：

1. 在 accounts.firefox.com 開啟您的 [個人資料設定](https://accounts.firefox.com/settings#data-collection)
2. 取消勾選 **資料收集與使用** > **幫助我們改善 ⁨Mozilla 帳號⁩**

##### 純 HTTPS 模式

- [x] 勾選 **在所有視窗都開啟純 HTTPS 模式**

這可以防止您無意間以明文 HTTP 連線到網站。 如今，不支援 HTTPS 的網站並不多見，因此這對您日常瀏覽的影響應該很小或沒有影響。

##### DNS over HTTPS

如果您使用 [DNS over HTTPS 提供者](dns.md):

- [x] 選擇 **最大保護** 與合適的提供者

最大保護 強制使用 DNS over HTTPS，如果 Firefox 無法連線到您的安全 DNS 解析器，或者安全 DNS 解析器表示您嘗試存取的網域沒有記錄，則會顯示安全警告。 這可以防止您所連接的網路暗中降低您的 DNS 安全性。

#### 同步

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) 讓您的瀏覽資料 (歷史記錄、書籤等) 在所有裝置上都可存取，並使用端對端加密 (E2EE) 進行保護。

### Arkenfox (進階)

<div class="admonition tip" markdown>
<p class="admonition-title">使用 Mullvad 瀏覽器以進階防止指紋識別</p>

[Mullvad 瀏覽器](#mullvad-browser) 提供與 Arkenfox 相同的防指紋保護，不需要使用 Mullvad VPN 就能獲得這些保護。 再加上 VPN ， Mullvad 瀏覽器可以阻擋 Arkenfox 無法處理的更先進追蹤腳本。 Arkenfox 仍具有更靈活的優勢，可以對需要保持登入狀態的個別網站設定例外。

</div>

[Arkenfox 專案](https://github.com/arkenfox/user.js) 為 Firefox 提供一套經過仔細考量的設定。 如果您[決定](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not)使用 Arkenfox，[有幾個設定](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common])在主觀上過於嚴格，而且可能導致某些網站無法正常運作 - 但是您[可以輕鬆更改](https://github.com/arkenfox/user.js/wiki/3.1-Overrides)以滿足您的需求。 我們**強烈建議**完整閱讀他們的[維基](https://github.com/arkenfox/user.js/wiki)頁面。 Arkenfox 也支援[容器](https://support.mozilla.org/kb/containers#w_for-advanced-users)功能。

Arkenfox的目標只是通過Canvas隨機化和Firefox內置的指紋阻力配置設置來阻止基本或天真的跟蹤腳本。 它的目的不是讓您的瀏覽器與其他許多使用 Arkenfox 的使用者混在一起，那是 Mullvad 瀏覽器或 Tor 瀏覽器的作法，也是阻止進階指紋跟蹤腳本的唯一方法。 請記住，您可以隨時使用多個瀏覽器。例如，您可以考慮將 Firefox + Arkenfox 用於希望保持登入或可以信任的幾個網站，而 Mullvad 瀏覽器則用於一般瀏覽。

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave 標誌](assets/img/browsers/brave.svg){ align=right }

**Brave 瀏覽器** 內建內容封鎖程式和[隱私權功能](https://brave.com/privacy-features/) ，其中許多功能預設已啟用。

Brave 基於 Chromium 瀏覽器專案構建，因此它應該令人感到熟悉並且具有最少的網站兼容性問題。

[:octicons-home-16: 首頁](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="洋蔥服務" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-windows11: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

**macOS 用戶：** 從 Brave 官網下載副檔名為 `.pkg` 的安裝程式，需要以管理員權限執行 (並且可能會在您的機器上執行其他不必要的腳本)。 作為替代方案，您可以從他們的 [GitHub releases](https://github.com/brave/brave-browser/releases/latest) 頁面下載最新的 `Brave-Browser-universal.dmg` 檔案，這提供了傳統的 “拖曳到應用程式文件夾” 安裝方法。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Brave 在官網的下載檔案中新增了 "[推廣代碼](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" 用以追蹤瀏覽器的下載來源，例如從 `BRV002` 下載的檔案名稱為 `Brave-Browser-BRV002.pkg`。 安裝程式會在安裝過程結束後向 Brave 伺服器發送推廣代碼。 如擔心此問題，可在開啟前更改安裝軟體的檔案名稱。

</div>

### 建議的 Brave 設定

這些選項可以在 :material-menu: → **設定** 中找到。

#### 設定

##### 防護

Brave 的[防護](https://support.brave.com/hc/articles/360022973471-What-is-Shields)功能包含一些防指紋識別措施。 我們建議在您訪問的所有網頁上[全域](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings)套用這些設定。

防護功能的選項可以根據各網站需要依情況降級，但我們建議預設使用以下設定：

<div class="annotate" markdown>

- [x] 勾選 **根據我的語言偏好設定，防止網站識別我的指紋**
- [x] 在 **追蹤器與廣告封鎖** 下選擇 **積極**

<details class="warning" markdown>
<summary>使用預設過濾器列表</summary>
Brave 可在內部 `brave://adblock`頁面中選擇其他內容過濾器。 我們建議您不要使用此功能；請保留預設的篩選條件清單。 使用額外清單將使您在一般 Brave 用戶中被突顯出來，如果Brave有漏洞，並將惡意規則添加到您使用的清單中，也可能會增加攻擊面。

</details>

- [x] 在 **升級連線至 HTTPS** 下選擇 **嚴格**
- [x] (可選) 勾選 **封鎖指令碼** (1)
- [x] 在 **封鎖指紋識別功能** 下選擇 **嚴格，可能會破壞網站**
- [x] 勾選 **當我關閉此網站時忘記我** (2)
- [ ] 在 **阻擋社群媒體** 下取消勾選所有社交元件

</div>

1. 此選項提供的功能類似於 uBlock Origin 的進階[封鎖模式](https://github.com/gorhill/uBlock/wiki/Blocking-mode)。
2. 若想在經常造訪的特定站點保持登入，則可以透過網址列中的盾牌圖示來為每個站點設定例外。

##### 隱私權和安全性

<div class="annotate" markdown>

- [x] 選取 **Disable non-proxied UDP** under [WebRTC IP Handling Policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] 取消選取 **使用 Google 服務來推送訊息**
- [ ] 取消選取 **同意隱私防護的產品分析 (P3A)**
- [ ] 取消選取 **自動發送每日使用呼叫至 Brave**
- [ ] 取消選取 **自動傳送診斷報告**
- [ ] 取消選取 **使用 Tor 的私密視窗** (1)

 !!!

</div>

1. Brave 在瀏覽器指紋識別的隱藏能力**不如** Tor 瀏覽器，且使用 Brave 的 Tor 使用者少，因此這將會使您顯得突出。 在[需要強大匿名性](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity)的情況下，請使用 [Tor 瀏覽器](tor.md#tor-browser)。

<div class="admonition tip" markdown>
<p class="admonition-title">離開時清除資料</p>

- [x] In the *Sites and Shields Settings* 選單中的“內容”下，點擊“裝置上網站資料”選單後，選擇“**關閉所有視窗時刪除已儲存至裝置的資料網站**”

如果希望保持登入到經常訪問的特定站點，可在「自訂行為」部分下針對每個站點設定例外。

</div>

##### 擴充功能

在**擴充功能**中關閉不使用的內建擴充功能

- [ ] 取消勾選 **Hangouts**
- [ ] 取消勾選 **WebTorrent**

##### Web3

Brave 的 Web3 功能可能會增加您的瀏覽器指紋和攻擊面。 除非有用到任何功能，否則應停用這些功能。

- 在預設的 以太坊 與 Solana 錢包下選擇 **擴充功能 (無後援)**
- 在 **解析 IPFS 資源的方法** 下選擇 **已停用**

##### 系統

<div class="annotate" markdown>

- [ ] 取消勾選 **在 Brave 關閉時繼續執行背景應用程式** 以停用背景應用程式 (1)

</div>

1. 此功能並不適用於所有平臺。

#### Brave 同步

[Brave 同步](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) 可在不同裝置上訪問瀏覽數據 (歷史記錄，書籤等)，無需帳戶且具 E2EE 保護。

#### Brave 獎勵與錢包

** Brave 獎勵** 可讓您在 Brave 執行某些動作時獲得Basic Attention Token (BAT) 加密貨幣。 它依賴於由少數提供商的託管帳號和 KYC。 我們不建議使用 BAT 作為 [私密加密貨幣](cryptocurrency.md)，也不建議使用 [托管錢包](advanced/payments.md#other-coins-bitcoin-ethereum-etc)，因此我們不建議使用此功能。

**Brave 錢包** 在您的電腦上本地運行，但不支援任何私密加密貨幣，因此我們也不建議使用此功能。

## 其他資源

## 標準

**請注意，我們與推薦的任何項目均無關。**除了我們的標準之外，我們還制定了一套[明確的要求](about/criteria.md)，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 必須是開源軟體。
- 支援自動更新。
- 從上游版本釋出後的 0-1 天內接收引擎更新。
- 可在 Linux、macOS 和 Windows 上使用。
- 為了使瀏覽器更尊重隱私權所作的任何變動都不應對使用者體驗產生負面影響。
- 預設情況下會封鎖第三方 Cookie。
- 支援[狀態分割](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning)以減少跨網站追蹤。[^1]

### 最佳案例

最佳案例標準代表我們希望在這個類別中看到的完美項目應具備的條件。 我們建議的瀏覽器可能不包括以下所有功能，但若包含這些功能會讓該項目在此頁面排名更高。

- 包括內建內容攔截功能。
- 支援 Cookie 區隔 (就像[多帳戶容器](https://support.mozilla.org/kb/containers)一樣)。
- 支援漸進式網絡應用程式。 PWA 使您能夠將某些網站安裝為在您的電腦上，像本機應用程式一樣運行。 這可能比安裝 Electron 應用程式更有優勢，因為您可以受益於瀏覽器的定期安全更新。
- 不包括對使用者隱私沒有影響的附加功能 (bloatware)。
- 預設情況下不收集遙測數據。
- 提供開源同步伺服器實作。
- 預設使用[私密搜尋引擎](search-engines.md)。

[^1]: Brave 的實施詳情請參閱 [Brave 隱私更新：為隱私區隔網路狀態](https://brave.com/privacy-updates/14-partitioning-network-state)。
