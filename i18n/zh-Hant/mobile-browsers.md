---
meta_title: "尊重隱私的 Android 和 iOS 行動瀏覽器 - Privacy Guides"
title: "行動瀏覽器"
icon: material/cellphone-information
description: 這些瀏覽器是我們目前推薦在行動裝置上使用的標準/非匿名網路瀏覽器。
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": 網頁
    name: 私密行動瀏覽器推薦
    url: "./"
    relatedLink: "../desktop-browsers/"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    applicationCategory: Web Browser
    operatingSystem:
      - Android
    subjectOf:
      "@type": 網頁
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://apple.com/safari
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": 網頁
      url: "./"
---

這些是我們目前推薦的 **行動網路瀏覽器** 以及 標準/非匿名網路瀏覽 的配置。 如果需要匿名瀏覽網際網路，您應該使用 [Tor](tor.md) 代替。

## Android

### Brave

<div class="admonition recommendation" markdown>

![Brave 標誌](assets/img/browsers/brave.svg){ align=right }

**Brave 瀏覽器** 內建內容封鎖程式和[隱私權功能](https://brave.com/privacy-features/) ，其中許多功能預設已啟用。

Brave 基於 Chromium 瀏覽器專案構建，因此它應該令人感到熟悉並且具有最少的網站兼容性問題。

[:octicons-home-16: 首頁](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

#### 建議的 Brave 設定

Tor 瀏覽器是真正匿名瀏覽網際網路的唯一途徑。 當您使用 Brave 時，我們建議您更改以下設定，以保護您的隱私免受某些影響，但除了 [Tor 瀏覽器](tor.md#tor-browser)以外的所有瀏覽器都可能以某種方式或另一種方式被 *某人* 追蹤。

這些選項可以在 :material-menu: → **設定** → **Brave 防護與安全性** 中找到

##### 防護

Brave 的[防護](https://support.brave.com/hc/articles/360022973471-What-is-Shields)功能包含一些防指紋識別措施。 我們建議在您訪問的所有網頁上[全域](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings)套用這些設定。

##### Brave 防護全域預設設定

防護功能的選項可以根據各網站需要依情況降級，但我們建議預設使用以下設定：

<div class="annotate" markdown>

- [x] 在 **封鎖追蹤器與廣告** 下選擇 **積極**

<details class="warning" markdown>
<summary>使用預設過濾器列表</summary>
Brave 可在內部 `brave://adblock`頁面中選擇其他內容過濾器。 我們建議您不要使用此功能；請保留預設的篩選條件清單。 使用額外清單將使您在一般 Brave 用戶中被突顯出來，如果Brave有漏洞，並將惡意規則添加到您使用的清單中，也可能會增加攻擊面。

</details>

- [x] 勾選 **自動重新導向 AMP 頁面**
- [x] 勾選 **自動重新導向追蹤 URL**
- [x] 將 **升級連線至 HTTPS** 設定為 **要求所有連線使用 HTTPS (嚴格)**
- [x] （可選） 勾選 **阻擋指令稿** (1)
- [x] 將 **封鎖 Cookies** 設定為 **封鎖第三方 Cookie**
- [x] 勾選 **封鎖指紋識別**
- [x] 勾選 **透過語言設定防止指紋識別攻擊**

</div>

1. 此選項提供的功能類似於 uBlock Origin 的 進階[封鎖模式](https://github.com/gorhill/uBlock/wiki/Blocking-mode) 或 [NoScript](https://noscript.net) 擴充功能。

##### 清除瀏覽資料

- [x] 勾選 **結束時清除資料**

##### 阻擋社交媒體

- [ ] 取消勾選所有社交媒體元件

##### 其他隱私設定

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP handling policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [x] (Optional) Select **No protection** under **Safe Browsing** (1)
- [ ] Uncheck **Allow sites to check if you have payment methods saved**
- [ ] Uncheck **IPFS Gateway** (2)
- [x] Select **Close tabs on exit**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Automatically send daily usage ping to Brave**

</div>

1. Brave's [implementation of Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) on Android **does not** proxy [Safe Browsing network requests](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) like its desktop counterpart. This means that your IP address may be seen (and logged) by Google. Note that Safe Browsing is not available for Android devices without Google Play Services.
2. 星際檔案系統 (InterPlanetary File System，縮寫為 IPFS) 是一個旨在實現檔案的分散式儲存、共享和持久化的網路傳輸協定。 除非您使用此功能，否則停用它。

#### Leo

These options can be found in :material-menu: → **Settings** → **Leo**

- [ ] Uncheck **Show autocomplete suggestions in address bar**

#### Brave 同步

[Brave 同步](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) 可在不同裝置上訪問瀏覽數據 (歷史記錄，書籤等)，無需帳戶且具 E2EE 保護。

### Mull

<div class="admonition recommendation" markdown>

![Mull logo](assets/img/browsers/mull.svg){ align=right }

**Mull** 是一款基於 Firefox 的隱私去污漬的 Android 瀏覽器。 與 Firefox 相比，它提供了更強的開箱即用指紋識別保護，並禁用 JavaScript 即時 (JIT) 編譯以增強安全性。 它還刪除了 Firefox 中的所有商業專有元素，例如取代 Google Play 服務引用。

[:octicons-home-16: Homepage](https://divestos.org/pages/our_apps#mull){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://divestos.org/pages/browsers#tuningFenix){ .card-link title=Documentation }
[:octicons-code-16:](https://codeberg.org/divested-mobile/mull-fenix){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-fdroid: F-Droid](https://f-droid.org/en/packages/us.spotco.fennec_dos)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger "危險"</p>

Android 上基於Firefox (Gecko) 的瀏覽器[缺乏](https://bugzilla.mozilla.org/show_bug.cgi?id=1610822) [網站隔離](https://wiki.mozilla.org/Project_Fission), [ ^1] 強大的安全功能，可防止惡意網站執行類似[Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)) 的攻擊來獲取對您擁有的另一個網站的內存的存取權限open.[^2] 基於 Chromium 的瀏覽器（例如​​ [Brave](#brave)）將針對惡意網站提供更強大的保護。

</div>

Enable DivestOS's [F-Droid repository](https://divestos.org/fdroid/official) to receive updates directly from the developer. 從預設的 F-Droid 儲存庫下載 Mull 將意味著更新可能會延遲幾天或更長時間。

Mull 透過[Tor 提升專案](https://wiki.mozilla.org/Security/Tor_Uplift)的[Arkenfox](desktop-browsers.md#arkenfox-advanced)的偏好來啟動許多上游高級功能。 使用為 Fennec F-Droid 開發的腳本從 Mozilla 程式碼中刪除商業專有 blob。

#### 建議的 Mull 設定

如想封鎖 Mull 中的追蹤器，建議安裝 [uBlock Origin](browser-extensions.md#ublock-origin) 作為內容封鎖程式。

Mull 隨附預設配置的隱私保護設定。 如果想在退出應用程式時自動關閉所有開啟的標籤頁，或清除瀏覽等其他數據，可以考慮在Mull 的設定中配置**退出時刪除瀏覽資料**選項自動歷史記錄和cookie。

與大多數瀏覽器相比，Mull 預設啟用更高級、更嚴格的隱私保護，因此某些網站可能無法載入或正常運作，除非調整這些設定。 如果遇到損壞的網站，可以查閱此[已知問題和解決方法清單](https://divestos.org/pages/broken#mull)，以獲取有關潛在修復的建議。 調整設定以修復網站可能會影響隱私/安全，因此請確保完全理解所遵循的任何說明。

## iOS

在 iOS 上，任何可以瀏覽網頁的應用程式都被[限制](https://developer.apple.com/app-store/review/guidelines)使用 Apple 提供的 [WebKit 框架](https://developer.apple.com/documentation/webkit)，因此沒有理由使用第三方瀏覽器。

### Safari

<div class="admonition recommendation" markdown>

![Safari 標誌](assets/img/browsers/safari.svg){ align=right }

**Safari** 是 iOS 預設瀏覽器。 It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Privacy Report, isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites so more devices look identical), and Private Relay for those with a paid iCloud+ subscription. It also allows you to separate your browsing with different profiles and lock private tabs with your biometrics/PIN.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title=Documentation}

</details>

</div>

#### 建議的 Safari 設定

如果想封鎖 Safari 追蹤器，建議安裝 [AdGuard](browser-extensions.md#adguard) 作為內容封鎖程式。

可以在 :gear: **Settings** app → **Safari** 中找到以下與隱私/安全相關的選項。

##### 主題類別

您的所有 Cookie、歷史記錄和網站資料將會針對各個主題類別分開。 您應該為不同用途使用不同的主題類別，例如購物、工作或學校。

##### 隱私 & 安全

- [x] 啓用 **防止跨網站跟蹤**

    這將啟用 WebKit 的[智慧追蹤預防](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp)。 該功能利用裝置上的機器學習來阻止跟蹤器不必要的跟蹤。 智慧追蹤預防可保護您免於許多常見威脅，但它不能阻止所有追蹤途徑，因為它被設計為不會干擾網站的可用性。

- [x] 啟用 **需要密碼來解鎖私密瀏覽**

    此設定可在私密瀏覽分頁未使用時使用 生物辨識資訊/PIN 鎖定。

##### 進階 → 隱私權

**進階追蹤和指紋保護** 設定將隨機化某些值，可使網站更難以進行指紋辨識：

- [x] 選擇 **所有瀏覽** 或 **私密瀏覽**

##### 隱私報告

隱私報告提供跨網站追蹤器的快照，瀏覽器如何防止追蹤器在您訪問的網站上分析您的狀況。 它還可以顯示每週報告，以顯示哪些追蹤器隨著時間的推移被封鎖。

隱私權報告可透過「頁面設定」選單存取。

##### 維護隱私權廣告測量

- [ ] 停用 **維護隱私權廣告測量**

廣告點擊測量通常使用侵犯使用者隱私的追蹤技術。 「[私密點擊測量](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm)」是一項針對 WebKit 的功能和提議的網頁標準，旨在讓廣告商能夠衡量網路活動的效果，同時不損害使用者隱私。

此功能本身沒有什麼隱私疑慮，因此您可以選擇不管它，但我們認為，它在私密瀏覽中自動停用反而顯示出功能被關閉的情況。

##### 總是保持私密瀏覽

開啟 Safari ，然後點按右下角的「標籤」按鈕。 然後，展開分頁群組清單。

- [x] 選擇 **私密瀏覽**

Safar i的私密瀏覽模式提供額外的隱私保護。 私密瀏覽為每個分頁使用新的[短暫](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral)工作階段，這意味著各個分頁之間是隔離的。 隱私瀏覽還有其他較小的隱私優勢，例如在使用 Safari 的翻譯功能時，不會將網頁地址傳送給 Apple。

請注意，私密瀏覽不會保存 Cookies 和網站資料，因此無法保持登入狀態。 這可能會帶來不便。

##### iCloud 同步

Safari 的歷史記錄、分頁群組、iCloud 分頁和已儲存密碼的同步都採用 E2EE 加密。 但預設情況下，書籤[並非如此](https://support.apple.com/HT202303)。 Apple 可以根據其[隱私權政策](https://apple.com/legal/privacy/en-ww)解密並存取它們。

您可以為 Safari 書籤和下載啟用 E2EE ，只需啟用「[進階資料防護](https://support.apple.com/HT212520)」即可。 請前往您的 **Apple ID 名稱 → iCloud → 進階資料保護**。

- [x] 開啟 「**進階資料保護**」

如果您在不開啟「進階資料保護」的情況下使用 iCloud ，我們亦建議您檢查，確保 Safari 預設下載位置已設定為裝置上的本機位置。 此選項可在 :gear: **設定** → **Safari** → **一般** → **下載**中找到。

## 標準

**請注意，我們與推薦的任何項目均無關。**除了我們的標準之外，我們還制定了一套[明確的要求](about/criteria.md)，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 必須支援自動更新。
- 必須快速接收來自上游版本的引擎更新。
- 須支援內容阻檔。
- 為了使瀏覽器更尊重隱私權而作的任何變動都不應對用戶體驗產生負面影響。
