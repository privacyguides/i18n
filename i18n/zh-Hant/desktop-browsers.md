---
meta_title: "尊重隱私的 PC 和 Mac 網路瀏覽器 - Privacy Guides"
title: "桌面瀏覽器"
icon: material/laptop
description: 我們目前推薦的這些隱私保護瀏覽器適合在電腦上進行標準/非匿名的網路瀏覽。
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": 網頁
    name: 推薦的隱私桌面瀏覽器
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
    sameAs: https://zh.wikipedia.org/zh-tw/Mozilla_Firefox
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
    sameAs: https://zh.wikipedia.org/zh-tw/Brave%E6%B5%8F%E8%A7%88%E5%99%A8
    applicationCategory: Web Browser
    operatingSystem:
      - Windows 作業系統
      - macOS
      - Linux
    subjectOf:
      "@type": 網頁
      url: "./"
---

<small>防護下列威脅：</small>

- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

這些是我們目前推薦的**桌面瀏覽器**與其設定，適合普通或非匿名的網頁瀏覽。 如果您重視強大的隱私保護和內建的的反指紋追蹤功能，我們推薦使用 [Mullvad 瀏覽器](#mullvad-browser)；如果您在尋求 Google Chrome 替代方案的休閒用網路瀏覽器，我們推薦使用 [Firefox](#firefox)；如果您需要 Chromium 的瀏覽器相容性，我們推薦使用 [Brave](#brave)。

如果您需要匿名瀏覽網際網路，應該使用 [Tor](tor.md)。 我們在此頁面提供了一些設定建議，但除了 Tor 瀏覽器以外的所有瀏覽器都可能以某種方式被*某人*追蹤。

## Mullvad 瀏覽器

<div class="admonition recommendation" markdown>

![Mullvad 瀏覽器標誌](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad 瀏覽器** 是移除 Tor 網路整合的 [Tor 瀏覽器](tor.md#tor-browser) 版本。 它的目的是提供為 VPN 使用者提供 Tor 瀏覽器的反指紋瀏覽器技術，這些技術是對抗 [:material-eye-outline: 大規模監控](basics/common-threats.md#mass-surveillance-programs){ .pg-blue } 的重要保護措施。 它由 Tor 計劃開發，並由 [Mullvad](vpn.md#mullvad)發布，而且 **不需要** 使用 Mullvad 的 VPN。

[:octicons-home-16: 首頁](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="說明文件" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

與 [Tor 瀏覽器](tor.md) 類似，Mullvad 瀏覽器的設計也是透過讓您的瀏覽器指紋與所有 Mullvad 瀏覽器使用者相同來防止指紋識別，並且它還包含根據安全等級自動調整的設定和擴充功能，分為 *標準*、*較安全* 和 *最安全* 三個等級。 因此，除了調整預設的[安全等級](https://tb-manual.torproject.org/security-settings)外，請絕對不要對瀏覽器進行任何修改。 其他修改將使您的指紋變得獨特，從而打破使用此瀏覽器的目的。 如果您希望更深入地調整瀏覽器設定，且您不擔心瀏覽器指紋被識別，我們推薦使用 [Firefox](#firefox)。

### 防止指紋識別

在**不**使用 [VPN](vpn.md) 的情況下，Mullvad 瀏覽器可提供與其他隱私瀏覽器 (例如 Firefox + [Arkenfox](#arkenfox-advanced) 或 [Brave](#brave)) 相同的防護措施，以對抗[單純的指紋辨識腳本](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting)。 Mullvad 瀏覽器在開箱即用的情況下提供了這些保護措施，代價是可能會犧牲其他隱私瀏覽器所具備的靈活性和便利性。

==要獲得最強大的防指紋辨識防護，我們建議將 Mullvad 瀏覽器 **搭配** VPN 一同使用== ，不論是 Mullvad 或其他推薦的 VPN 供應商皆可。 當您將 VPN 與 Mullvad 瀏覽器搭配使用時，您將與許多其他使用者共用一個指紋和 IP 位址池，以讓你混在「人群」之中。 這個策略是阻止進階追蹤腳本的唯一方法，也同樣是 Tor 瀏覽器使用的防指紋辨識技術。

請注意，雖然您可以將 Mullvad 瀏覽器與任何 VPN 供應商一起使用，但該 VPN 上的其他使用者也必須使用 Mullvad 瀏覽器，才能形成這個「人群」，而這在 Mullvad VPN 上比其他供應商更有可能發生，特別是在 Mullvad 瀏覽器推出後不久。 Mullvad 瀏覽器沒有內建 VPN，也不會在瀏覽之前檢查是否使用 VPN，必須另外設定和管理 VPN 連線。

Mullvad 瀏覽器附帶預先安裝的 *uBlock Origin* 和 *NoScript* 擴充功能。 我們通常不建議新增*額外*的[瀏覽器擴充功能](browser-extensions.md)，且這些與瀏覽器預裝的擴充功能**不**應移除或修改成任何預設值以外的設定，一旦隨意更動，您的瀏覽器指紋會明顯有別於其他 Mullvad 瀏覽器使用者。 它還預先安裝了 Mullvad 瀏覽器擴充功能，但也*可*將其安全地移除，而不會影響您的瀏覽器指紋，但即使您不使用 Mullvad VPN，也可以安全地保留它。

### 隱私瀏覽模式

Mullvad 瀏覽器預設總是使用隱私瀏覽模式運行，這意味著您的歷史記錄、Cookie 和其他網站資料在每次關閉瀏覽器時都會被清除。 但書籤、瀏覽器設定和擴充功能設定仍會保留。

這是為了防止進階形式的追蹤，但確實犧牲了便利性和一些 Firefox 功能，例如多重帳戶容器 (Multi-Account Containers，又稱容器分頁功能)。 請記住，您隨時可以使用多個瀏覽器，例如，您可以考慮對希望保持登入狀態或在 Mullvad 瀏覽器中無法正常運作的幾個網站使用 Firefox + Arkenfox，而在一般瀏覽時使用 Mullvad 瀏覽器。

### Mullvad Leta

Mullvad 瀏覽器將 DuckDuckGo 設為預設的[搜尋引擎](search-engines.md)，但它也預裝了 **Mullvad Leta**，一個需要訂閱 Mullvad VPN 才能使用的搜尋引擎。 Mullvad Leta 直接查詢 Google 的付費搜索 API，這也是為什麼它僅限付費訂閱者使用。 然而，由於這個限制，Mullvad 有可能將搜尋字串和 Mullvad VPN 帳戶進行關聯。 因此，我們不建議使用 Mullvad Leta，即使 Mullvad 僅收集極少量的 VPN 訂閱者資訊。

## Firefox

<div class="admonition recommendation" markdown>

![Firefox 標誌](assets/img/browsers/firefox.svg){ align=right }

**Firefox** 提供強大的隱私設定，例如 [加強型追蹤保護功能](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop)，可以幫助阻擋各種[類型的追蹤](https://support.mozilla.org/zh-TW/kb/enhanced-tracking-protection-firefox-desktop#w_jia-qiang-xing-zhui-zong-bao-hu-gong-neng-hui-feng-suo-shi-mo)。

[:octicons-home-16: 首頁](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="說明文件" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="原始碼" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="捐款" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Firefox 在 Mozilla 網站的下載中包含一個獨特的 [下載令牌](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0)，並使用 Firefox 中的遙測功能傳送該令牌。 該令牌**不**包含在 [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/) 上的發行版中。

</div>

### 建議的 Firefox 設定

這些選項可以在 :material-menu: → **設定** 中找到。

#### 搜尋

- [ ] 取消勾選 **顯示搜尋建議**

搜尋建議功能可能無法在您所在的地區使用。

搜尋建議會將您在網址列中輸入的所有內容傳送至預設搜尋引擎，無論您是否實際提交搜尋。 停用搜尋建議可讓您更精確地控制您傳送給搜尋引擎供應商的資料。

##### Firefox Suggest (僅限美國)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) 功能只限美國地區，其功能類似於搜尋建議。 我們建議停用此功能的原因與我們建議停用搜尋建議的原因相同。 如果您在「**網址列**」標題下沒有看到這些選項，則表示您還不能使用此功能，可以忽略這些變更。

- [ ] 取消勾選 **Suggestions from Firefox**
- [ ] 取消勾選 **Suggestions from sponsors**

#### 隱私 & 安全

##### 加強型追蹤保護功能

- [x] 在 加強型追蹤保護 下選擇 **嚴格**

透過封鎖社交媒體追蹤器、指紋辨識腳本 (注意，這並不能保護您免於*所有*的指紋辨識)、加密貨幣挖礦程式、跨網站 Cookie 以及其他追蹤內容來保護您。 加強型追蹤保護功能可保護您免於許多常見威脅，但並不能阻止所有追蹤途徑，因為它的設計考量了網站的可用性。

##### 關閉時清除資料

如果您想在特定網站保持登入，可以在 **Cookie 與網站資料** → **管理例外網站…** 中允許例外。

- [x] 勾選 **關閉 Firefox 時清除 Cookie 與網站資料**

這可以保護您免受持久性 Cookie 的影響，但無法防止在單一瀏覽階段中取得的 Cookie。 啟用此功能後，只需重新啟動 Firefox，就能輕鬆清除瀏覽器 Cookie。 如果您希望在經常造訪的特定網站保持登入，可以針對個別網站設定例外。

##### 遙測

- [ ] 取消勾選 **允許 Firefox 傳送技術與互動資料給 Mozilla**
- [ ] 取消勾選 **允許 Firefox 安裝並進行研究**
- [ ] 取消勾選 **允許 Firefox 以您的身分自動回報錯誤報告**

根據 Mozilla 的 Firefox 隱私權政策：

> Firefox 會向 Mozilla 發送以下數據：您的 Firefox 版本和語言；操作系統和硬體配置；記憶體、關於崩潰和錯誤的基本訊息；更新、安全瀏覽和啟動等自動化流程系統的結果。 當 Firefox 向 Mozilla 發送數據時，會將您的 IP 位址作為伺服器日誌的一部份暫時收集。

此外，Mozilla 帳戶服務也收集[一些技術資料](https://mozilla.org/privacy/mozilla-accounts)。 如果有使用 Mozilla 帳戶，您可以選擇退出。

1. 在 [accounts.firefox.com 開啟您的個人資料設定](https://accounts.firefox.com/settings#data-collection)
2. 取消勾選 **資料收集與使用** > **幫助我們改善 ⁨Mozilla 帳號⁩**

##### 網站廣告偏好設定

- [ ] 取消勾選 **允許網站進行能保護隱私的廣告成效測量**

Firefox 128 發佈時，新增了一個[尊重隱私的成效測量](https://support.mozilla.org/kb/privacy-preserving-attribution) (簡稱 PPA)，並且[預設為開啟狀態](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2)。 PPA 允許廣告商利用您的瀏覽器進行廣告成效測量，進而取代基於 JavaScript 的傳統追蹤方式。 我們認為此行為超出了使用者代理的職責範圍，而 Arkenfox 預設停用此功能的決定，也進一步的表明應該停用這項功能。

##### 純 HTTPS 模式

- [x] 勾選 **在所有視窗都只使用 HTTPS 連線**

這可以防止您無意間以明文 HTTP 連線到網站。 如今，不支援 HTTPS 的網站已不多見，因此這對您日常瀏覽的影響幾乎沒有影響。

##### 基於 HTTPS 的 DNS 服務 (DNS over HTTPS)

如果您使用 [DNS over HTTPS 提供者](dns.md):

- [x] 選擇 **最大保護** 與合適的提供者

最大保護 強制使用 DNS over HTTPS，如果 Firefox 無法連線到您的安全 DNS 解析器，或者安全 DNS 解析器表示您嘗試存取的網域沒有記錄，則會顯示安全警告。 這可以防止您所使用的網路暗中降低您的 DNS 安全性。

#### 同步

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) 讓您的瀏覽資料 (歷史記錄、書籤等) 在所有裝置上都可存取，並使用端對端加密 (E2EE) 進行保護。

### Arkenfox (進階)

<div class="admonition tip" markdown>
<p class="admonition-title">使用 Mullvad 瀏覽器以防止更進階的指紋識別</p>

[Mullvad 瀏覽器](#mullvad-browser) 提供與 Arkenfox 相同的防指紋保護，不需要使用 Mullvad VPN 就能獲得這些保護。 結合 VPN 使用時，Mullvad 瀏覽器 能夠阻擋 Arkenfox 無法處理的進階追蹤腳本。 相較之下，Arkenfox 仍然具有更高的靈活性，可以對需要保持登入狀態的個別網站設定例外。

</div>

[Arkenfox 專案](https://github.com/arkenfox/user.js) 為 Firefox 提供一套經過精心考量的設定。 如果您[決定](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not)使用 Arkenfox，有[幾個選項](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common])可能在主觀上會較為嚴格，且/或可能導致某些網站無法正常運作，不過您可以[輕鬆更改](https://github.com/arkenfox/user.js/wiki/3.1-Overrides)這些選項，以滿足您的需求。 我們**強烈建議**完整閱讀他們的 [Wiki 頁面](https://github.com/arkenfox/user.js/wiki)。 Arkenfox 也支援[容器](https://support.mozilla.org/kb/containers#w_for-advanced-users)功能。

Arkenfox 的目標旨在透過 Canvas 隨機化和 Firefox 內建的抗指紋設定來阻止基本或簡單的追蹤腳本。 它的目的不是讓您的瀏覽器與其他許多使用 Arkenfox 的使用者混在一起，那是 Mullvad 瀏覽器或 Tor 瀏覽器的作法，也是阻止進階指紋跟蹤腳本的唯一方法。 請記住，您可以使用多種瀏覽器。例如：您可以考慮使用 Firefox+Arkenfox 來瀏覽一些您想要保持登入狀態或以其他方式得到您信任的網站；而一般瀏覽則使用 Mullvad Browser。

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave 標誌](assets/img/browsers/brave.svg){ align=right }

**Brave 瀏覽器** 內建內容封鎖程式和[隱私權功能](https://brave.com/privacy-features/) ，其中許多功能預設為啟用。

Brave 基於 Chromium 瀏覽器專案構建，因此使用起來應該會感到熟悉，並且網站相容性問題最小。

[:octicons-home-16: 首頁](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="洋蔥服務" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Brave 在官網的下載的檔案名稱中新增了一個 「[推廣代碼（referral code）](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)」，用於追蹤瀏覽器的下載來源；舉例來說，下載的檔案名為 `Brave-Browser-BRV002.pkg`，則其名稱中的 `BRV002` 就是它的推廣代碼。 安裝程式會在結束後向 Brave 的伺服器發送帶有推廣代碼的遙測。 如果您擔心這個問題，可以在開啟前更改安裝軟體的檔案名稱。

</div>

### 建議的 Brave 設定

這些選項可以在 :material-menu: → **設定** 中找到。

#### 防護

Brave 的[防護](https://support.brave.com/hc/articles/360022973471-What-is-Shields)功能包含一些防指紋識別措施。 我們建議在您訪問的所有網頁上[全域](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings)套用這些設定。

防護功能的選項可以根據各網站需要依情況降級，但我們建議預設使用以下設定：

<div class="annotate" markdown>

- [x] 將 *追蹤器與廣告封鎖* 設定為 **積極**。

<details class="warning" markdown>
<summary>使用預設過濾器清單</summary>

Brave 允許您在內部網頁 brave://settings/shields/filters 內選擇額外的內容過濾器。 我們建議您不要使用此功能；請保留預設的篩選清單。 使用額外的列表會讓您從其他 Brave 使用者中脫穎而出，如果 Brave 中有漏洞，而惡意規則被加入您使用的列表中，也可能會增加攻擊面。

</details>

- [x] 將 *升級連線至 HTTPS* 設定為 **嚴格**
- [x] (選擇性) 選擇 **封鎖指令碼** (1)
- [x] 勾選 **封鎖指紋識別功能**
- [x] 將 *封鎖 Cookie* 設定為 **封鎖第三方 Cookie**
- [x] 勾選 **當我關閉此網站時忘記我** (2)
- [ ] 取消勾選所有社群媒體元件

</div>

1. 此選項會停用 JavaScript，這會破壞許多網站。 若您想要避免破壞它們，可以針對個別需要的網站設定例外。只需點一下網址列上的 Shield 圖示，然後在 *進階控制* 下取消勾選此設定即可。
2. 如果您希望在經常造訪的特定網站保持登入狀態，可以針對個別需要的網站設定例外。只需點一下網址列上的 Shield 圖示，然後在 *進階控制* 下取消勾選此設定即可。

#### 隱私權和安全性

<div class="annotate" markdown>

- [x] 在 *安全性* → *管理 V8 安全性* 底下選擇**禁止網站使用 V8 最佳化工具** (1)
- [x] 在 *網站與 Shields 設定* 下選擇 **自動移除未使用網站的權限**
- [x] 在 [*WebRTC IP 處理政策*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc) 下選擇 **停用非代理 UDP**
- [ ] 取消勾選 **使用 Google 服務來推播訊息**
- [x] 選取 **自動重新導向 AMP 頁面**
- [x] 選取 **自動重新導向追蹤 URL**
- [x] 選取 **根據我的語言偏好設定，防止網站識別我的指紋**

</div>

1. 停用 V8 最佳化工具可減少您的攻擊面。 停用[*部分*](https://grapheneos.social/@GrapheneOS/112708049232710156) JavaScript 即時 (JIT) 編譯的某些部分，從而降低您的攻擊面。

<div class="admonition tip" markdown>
<p class="admonition-title">離開時清除資料</p>

- [x] 在*網站與 Shields 設定* → *內容* → *其他內容設定* → *網站在裝置端的資料* 底下選擇**在所有視窗關閉後刪除網站儲存到裝置的資料**。

如果希望在經常造訪的特定網站上保持登入，可在 *自訂設定* 部分下針對各個網站設定例外。

</div>

##### Tor 視窗

[**使用 Tor 的隱私視窗**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity)允許您在私人視窗中透過 Tor 網路路由流量，並存取 .onion 服務，這在某些情況下可能很有用。 不過，Brave 對指紋辨識的抵抗力**不如** Tor 瀏覽器，而且將 Brave 與 Tor 配合使用的人少得多，因此您會脫穎而出。 如果您的威脅模式需要極高的匿名性，請使用 [Tor 瀏覽器](tor.md#tor-browser)。

##### 資料集合

- [ ] 取消勾選 **允許保護私隱的產品分析 (P3A)**
- [ ] 取消勾選 **自動傳送每日使用 ping 到 Brave**
- [ ] 取消勾選 **自動傳送診斷報告**

#### Web3

Brave 的 Web3 功能可能會增加您的瀏覽器指紋和攻擊面。 除非您使用任何這些功能，否則應將其停用。

- 將 *預設以太坊錢包* 設定為 **擴充功能 (無後援)**
- 將 *預設 Solana 錢包* 設定為 **擴充功能 (無後援)**

#### 擴充功能

- [ ] 取消勾選所有您用不到的內建擴充功能

#### 搜尋引擎

我們建議在 Brave 中停用搜尋建議，原因與我們建議在 [Firefox](#search) 中停用此功能相同。

- [ ] 取消勾選 **顯示搜尋建議**

#### 系統

<div class="annotate" markdown>

- [ ] 取消勾選 **在 Brave 關閉時繼續執行背景應用程式** 以停用背景應用程式 (1)

</div>

1. 此功能並不適用於所有平台。

#### Brave 同步

[Brave 同步](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) 可在不同裝置上訪問瀏覽數據 (歷史記錄，書籤等)，無需帳戶且具 E2EE 保護。

#### Brave Rewards 與錢包

**Brave Rewards** 可讓您在 Brave 執行某些動作時獲得 Basic Attention Token (BAT) 加密貨幣。 它依賴於由少數提供商的託管帳號和 KYC。 我們不建議使用 BAT 作為[隱私加密貨幣](cryptocurrency.md)，也不建議使用[托管錢包](advanced/payments.md#wallet-custody)，因此我們會建議避免使用此功能。

**Brave 錢包** 在您的電腦上本地運行，但不支援任何隱私加密貨幣，因此我們也不建議使用此功能。

## 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用專案前先熟悉此清單，並自行研究，以確保它是適合您的選擇。

### 最低合格要求

- 必須是開源軟體
- 必須支援自動更新
- 必須在上游版本釋出後的 0-1 天內接收引擎更新
- 必須適用於 Linux、macOS 和 Windows
- 為了使瀏覽器更尊重隱私權而作的任何變動都不應對用戶體驗產生負面影響
- 預設情況下會封鎖第三方 Cookie
- 必須支援[狀態分割](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning)，以減少跨網站追蹤。[^1]

### 最佳情況

最佳案例標準代表我們希望在這個類別中看到的完美項目應具備的條件。 我們建議的瀏覽器可能不包括以下所有功能，但若包含這些功能會讓該項目在此頁面排名更高。

- 應該要內建內容攔截功能。
- 應該要支援 Cookie 區隔 (就像[多帳號容器](https://support.mozilla.org/kb/containers)一樣)。
- 應該要支援 漸進式網路應用程式 (PWA)。 PWA 使您能夠將某些網站安裝為在您的電腦上，像本機應用程式一樣運行。 這會比安裝基於 Electron 的應用程式更有優勢，因為 PWA 可以受益於瀏覽器的定期安全更新。
- 不應該包含對使用者隱私沒有益處的附加功能 (bloatware)。
- 預設情況下不應收集遙測。
- 應該要提供開源同步伺服器實作。
- 預設情況下應使用[隱私搜尋引擎](search-engines.md)。

[^1]: Brave 的實施詳情請參閱 [Brave 隱私更新：為隱私區隔網路狀態](https://brave.com/privacy-updates/14-partitioning-network-state)。
