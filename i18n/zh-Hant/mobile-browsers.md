---
meta_title: "適用於 Android 和 iOS 且尊重隱私的網頁瀏覽器 - Privacy Guides"
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
      - iOS
    subjectOf:
      "@type": 網頁
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Cromite
    image: /assets/img/browsers/cromite.svg
    url: https://cromite.org
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

<small>防護下列威脅：</small>

- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

這些是我們目前推薦的 **行動網路瀏覽器** 以及 標準/非匿名網路瀏覽 的配置。 如果需要匿名瀏覽網際網路，您應該使用 [Tor](tor.md) 代替。

## Brave

<div class="admonition recommendation" markdown>

![Brave 標誌](assets/img/browsers/brave.svg){ align=right }

**Brave 瀏覽器** 內建內容封鎖程式和[隱私權功能](https://brave.com/privacy-features/) ，其中許多功能預設為啟用。

Brave 基於 Chromium 瀏覽器專案構建，因此它應該令人感到熟悉並且具有最少的網站兼容性問題。

[:octicons-home-16: 首頁](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="洋蔥服務" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

### 建議的 Brave 設定

Tor 瀏覽器是真正匿名瀏覽網際網路的唯一途徑。 當您使用 Brave 時，我們建議您更改以下設定，以保護您的隱私免受某些影響，但除了 [Tor 瀏覽器](tor.md#tor-browser)以外的所有瀏覽器都可能以某種方式或另一種方式被 *某人* 追蹤。

=== "Android"

    這些選項可以在 :material-menu: → **設定** → **Brave 防護與安全性** 中找到。

=== "iOS"

    These options can be found in :fontawesome-solid-ellipsis: → **Settings** → **Shields & Privacy**.

#### Brave 防護全域預設設定

Brave 的[防護](https://support.brave.com/hc/articles/360022973471-What-is-Shields)功能包含一些防指紋識別措施。 我們建議在您訪問的所有網頁上[全域](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings)套用這些設定。

防護功能的選項可以根據各網站需要依情況降級，但我們建議預設使用以下設定：

=== "Android"

    <div class="annotate" markdown>

    - [x] 在 *封鎖追蹤器與廣告* 下選擇 **積極**
    - [x] 勾選 **自動重定向 AMP 頁面**
    - [x] 勾選 **自動重新導向追蹤 URL**
    - [x] 將 *升級連線至 HTTPS* 設定為 **要求所有連線使用 HTTPS（嚴格）**
    - [x] （可選）勾選 **阻擋指令稿** (1)
    - [x] 將 *封鎖 Cookies* 設定為 **封鎖第三方 Cookie**
    - [x] 勾選 **封鎖指紋識別**
    - [x] 勾選 **透過語言設定防止指紋辨識攻擊**

    <details class="warning" markdown>
    <summary>使用預設篩選清單</summary>

    Brave 允許您在 **內容過濾** 選單或瀏覽器內部的 `brave://adblock` 頁面中啟用其他內容篩選清單。 我們建議您不要使用此功能；請保留預設的篩選條件清單。 使用額外清單將使您在一般 Brave 用戶中被突顯出來，如果Brave有漏洞，並將惡意規則添加到您使用的清單中，也可能會增加攻擊面。

    </details>

    - [x] 勾選 **當我關閉此網站時忘記我**

    </div>

    1. 此選項會停用 JavaScript，這會破壞許多網站。 若您想要避免破壞它們，您可以為每個需要的網站設定例外，方法是按一下網址列上的 Shield 圖示，然後在 *進階控制* 下取消勾選此設定。

=== "iOS"

    <div class="annotate" markdown>

    - [x] Select **Aggressive** under *Trackers & Ads Blocking*
    - [x] Select **Strict** under *Upgrade Connections to HTTPS*
    - [x] Select **Auto-Redirect AMP pages**
    - [x] Select **Auto-Redirect Tracking URLs**
    - [x] （可選）勾選 **阻擋指令稿** (1)
    - [x] 勾選 **封鎖指紋識別**

    <details class="warning" markdown>
    <summary>使用預設篩選清單</summary>

    Brave allows you to select additional content filters within the **Content Filtering** menu. 我們建議您不要使用此功能；請保留預設的篩選條件清單。 使用額外清單將使您在一般 Brave 用戶中被突顯出來，如果Brave有漏洞，並將惡意規則添加到您使用的清單中，也可能會增加攻擊面。

    </details>

    </div>

    1. 此選項會停用 JavaScript，這會破壞許多網站。 若您想要避免破壞它們，您可以為每個需要的網站設定例外，方法是按一下網址列上的 Shield 圖示，然後在 *進階控制* 下取消勾選此設定。

##### 清除瀏覽資料（僅適用於 Android）

- [x] 勾選 **結束時清除資料**

##### 阻擋社群媒體（僅適用於 Android）

- [ ] 取消勾選所有社交媒體元件

#### 其他隱私設定

=== "Android"

    <div class="annotate" markdown>

    - [x] 將 [*WebRTC IP 處理政策*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc) 設定為 **停用非代理 UDP**
    - [x] （可選） 將 *安全瀏覽* 設定為 **無防護** (1)
    - [ ] 取消勾選 **允許網站檢查是否有已儲存的付款方式**
    - [x] 勾選 **退出時關閉分頁**
    - [ ] 取消勾選 **允許保護私隱的產品分析 (P3A)**
    - [ ] 取消勾選 **自動傳送診斷報告**
    - [ ] 取消勾選 **自動傳送每日使用 ping 到 Brave**

    </div>

    1. Brave 在 Android 上[實作的 安全瀏覽](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) **不會**像電腦版一樣代理 [安全瀏覽服務 的網路請求](https://developers.google.com/safe-browsing/v4/update-api#checking-urls)。 這表示 Google 可能會看到 (並記錄) 您的 IP 位址。 請注意，安全瀏覽功能不適用於沒有 Google Play 服務的 Android 裝置。

=== "iOS"

    - [ ] Uncheck **Allow Privacy-Preserving Product Analytics (P3A)**
    - [ ] 取消勾選 **自動傳送每日使用 ping 到 Brave**

#### Leo

這些選項可以在 :material-menu: → **設定** → **Leo** 中找到。

<div class="annotate" markdown>

- [ ] Uncheck **Show autocomplete suggestions in address bar** (1)

</div>

1. This option is not present in Brave's iOS app.

#### Search engines

These options can be found in :material-menu:/:fontawesome-solid-ellipsis: → **Settings** → **Search engines**.

- [ ] 取消勾選 **顯示搜尋建議**

#### Brave 同步

[Brave 同步](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) 可在不同裝置上訪問瀏覽數據 (歷史記錄，書籤等)，無需帳戶且具 E2EE 保護。

## Cromite (Android)

<div class="admonition recommendation" markdown>

![Cromite logo](assets/img/browsers/cromite.svg){ align=right }

**Cromite** 是一個基於 Chromium 的瀏覽器，內建廣告封鎖、指紋保護及其他 [隱私與安全強化功能](https://github.com/uazo/cromite/blob/master/docs/FEATURES.md)。 它是已停止維護的 **Bromite** 瀏覽器之分支。

[:octicons-home-16: 首頁](https://www.cromite.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uazo/cromite/blob/master/docs/PRIVACY_POLICY.md){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://github.com/uazo/cromite?tab=readme-ov-file#docs){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/uazo/cromite){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-android: F-Droid](https://www.cromite.org/fdroid/repo/?fingerprint=49F37E74DEE483DCA2B991334FB5A0200787430D0B5F9A783DD5F13695E9517B)
- [:simple-github: GitHub](https://github.com/uazo/cromite/releases/latest)

</details>

</div>

### 建議的設定

These options can be found in :material-menu: → :gear: **Settings** → **Privacy and security**.

#### Browsing data

- [x] Select **Close all open tabs on exit**

#### Incognito mode

- [x] Select **Open external links in incognito**

#### 安全

- [x] Select **Always use secure connections**

這可以防止您無意間以明文 HTTP 連線到網站。 HTTP is extremely uncommon nowadays, so this should have little to no impact on your day-to-day browsing.

#### Adblock Plus settings

These options can be found in :material-menu: → :gear: **Settings** → **Adblock Plus settings**.

Cromite contains a customized version of Adblock Plus with EasyList enabled by default, as well as options to select more filter lists within the **FIlter lists** menu.

Using extra lists will make you stand out from other Cromite users and may also increase attack surface if a malicious rule is added to one of the lists you use.

- \[x\] (Optional) Select **Enable anti-circumvention and snippets**

This setting adds an additional Adblock Plus list that may increase the effectiveness of Cromite's content blocking. The warnings about standing out and potentially increasing attack surface apply.

#### Legacy Adblock settings

These options can be found in :material-menu: → :gear: **Settings** → **Legacy Adblock settings**.

- [ ] Uncheck the autoupdate setting

This disables update checks for the unmaintained Bromite adblock filter.

## Mull (Android)

<div class="admonition recommendation" markdown>

![Mull logo](assets/img/browsers/mull.svg){ align=right }

**Mull** 是一款基於 Firefox 的以隱私為重點，去除專有 二進位大型物件（blob） 的 Android 瀏覽器。 與 Firefox 相比，它提供了更強的開箱即用指紋識別保護，並禁用 JavaScript 即時 (JIT) 編譯以增強安全性。 它還刪除了 Firefox 中的所有商業專有元素，例如取代 Google Play 服務引用。

[:octicons-home-16: 首頁](https://divestos.org/pages/our_apps#mull){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://divestos.org/pages/browsers#tuningFenix){ .card-link title="說明文件" }
[:octicons-code-16:](https://codeberg.org/divested-mobile/mull-fenix){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-fdroid: F-Droid](https://f-droid.org/en/packages/us.spotco.fennec_dos)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger "危險"</p>

Android 上基於Firefox (Gecko) 的瀏覽器[缺乏](https://bugzilla.mozilla.org/show_bug.cgi?id=1610822) [網站隔離](https://wiki.mozilla.org/Project_Fission)[^1] ，這是一個強大的安全功能，可防止惡意網站執行類似 [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)) 的攻擊以獲取您開啟的另一個網站的記憶體存取權限[^2] ；基於 Chromium 的瀏覽器（例如：​​[Brave](#brave)）將針對惡意網站提供更強大的保護。

</div>

啟用 DivestOS 的[F-Droid 儲存庫](https://divestos.org/fdroid/official)，以便直接從開發者接收更新。 從預設的 F-Droid 儲存庫下載 Mull 將意味著更新可能會延遲幾天或更長時間。

Mull 透過[Tor 提升專案](https://wiki.mozilla.org/Security/Tor_Uplift)的[Arkenfox](desktop-browsers.md#arkenfox-advanced)的偏好來啟動許多上游高級功能。 使用為 Fennec F-Droid 開發的腳本從 Mozilla 程式碼中刪除商業專有 blob。

### 建議的 Mull 設定

如想封鎖 Mull 中的追蹤器，建議安裝 [uBlock Origin](browser-extensions.md#ublock-origin) 作為內容封鎖程式。

Mull 隨附預設配置的隱私保護設定。 如果想在退出應用程式時自動關閉所有開啟的標籤頁，或清除瀏覽等其他數據，可以考慮在Mull 的設定中配置**退出時刪除瀏覽資料**選項自動歷史記錄和cookie。

與大多數瀏覽器相比，Mull 預設啟用更高級、更嚴格的隱私保護，因此某些網站可能無法載入或正常運作，除非調整這些設定。 如果遇到損壞的網站，可以查閱此[已知問題和解決方法清單](https://divestos.org/pages/broken#mull)，以獲取有關潛在修復的建議。 調整設定以修復網站可能會影響隱私/安全，因此請確保完全理解所遵循的任何說明。

## Safari (iOS)

On iOS, any app that can browse the web is [restricted](https://developer.apple.com/app-store/review/guidelines) to using an Apple-provided [WebKit framework](https://developer.apple.com/documentation/webkit), so a browser like [Brave](#brave) does not use the Chromium engine like its counterparts on other operating systems.

<div class="admonition recommendation" markdown>

![Safari 標誌](assets/img/browsers/safari.svg){ align=right }

**Safari** 是 iOS 預設瀏覽器。 It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites so more devices look identical), and fingerprint randomization, as well as Private Relay for those with a paid iCloud+ subscription.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title="Documentation" }

</details>

</div>

### 建議的 Safari 設定

如果您想要在 Safari 中使用內容阻擋器，我們建議您安裝[AdGuard](browser-extensions.md#adguard)。

The following privacy/security-related options can be found in :gear: **Settings** → **Apps** → **Safari**.

#### Allow Safari to Access

Under **Siri**:

- [ ] Disable **Learn from this App**
- [ ] Disable **Show in App**
- [ ] Disable **Show on Home Screen**
- [ ] Disable **Suggest App**

This prevents Siri from using content from Safari for Siri suggestions.

#### 搜尋

- [ ] Disable **Search Engine Suggestions**

This setting sends whatever you type in the address bar to the search engine set in Safari. 停用搜尋建議可讓您更精確地控制您傳送給搜尋引擎供應商的資料。

#### 主題類別

Safari allows you to separate your browsing with different profiles. All of your cookies, history, and website data are separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

#### 隱私 & 安全

- [x] Enable **Prevent Cross-Site Tracking**

This enables WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). The feature helps protect against unwanted tracking by using on-device machine learning to stop trackers. ITP protects against many common threats, but does not block all tracking avenues because it is designed to not interfere with website usability.

- [x] Enable **Require Face ID/Touch ID to Unlock Private Browsing**

This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

- [ ] Disable **Fraudulent Website Warning**

This setting uses Google Safe Browsing (or Tencent Safe Browsing for users in mainland China or Hong Kong) to protect you while you browse. As such, your IP address may be logged by your Safe Browsing provider. Disabling this setting will disable this logging, but you might be more vulnerable to known phishing sites.

- [ ] Disable **Highlights**

Apple's privacy policy for Safari states:

> When visiting a webpage, Safari may send information calculated from the webpage address to Apple over OHTTP to determine if relevant highlights are available.

#### Settings for Websites

Under **Camera**

- [x] Select **Ask**

Under **Microphone**

- [x] Select **Ask**

Under **Location**

- [x] Select **Ask**

These settings ensure that websites can only access your camera, microphone, or location after you explicitly grant them access.

#### 其他隱私設定

這些選項可以在 :gear: **設定** → **應用程式** → **Safari** → **進階**

##### Fingerprinting Mitigations

**進階追蹤和指紋保護** 設定將隨機化某些值，可使網站更難以進行指紋辨識：

- [x] 選擇 **所有瀏覽** 或 **私密瀏覽**

##### 維護隱私權廣告測量

- [ ] 停用 **維護隱私權廣告測量**

廣告點擊測量通常使用侵犯使用者隱私的追蹤技術。 「[私密點擊測量](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm)」是一項針對 WebKit 的功能和提議的網頁標準，旨在讓廣告商能夠衡量網路活動的效果，同時不損害使用者隱私。

此功能本身沒有什麼隱私疑慮，因此您可以選擇不管它，但我們認為，它在私密瀏覽中自動停用反而顯示出功能被關閉的情況。

#### 總是保持私密瀏覽

開啟 Safari ，然後點按右下角的「標籤」按鈕。 Then, expand the :material-format-list-bulleted: Tab Groups list.

- [x] 選擇 **私密瀏覽**

Safar i的私密瀏覽模式提供額外的隱私保護。 私密瀏覽為每個分頁使用新的[短暫](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral)工作階段，這意味著各個分頁之間是隔離的。 隱私瀏覽還有其他較小的隱私優勢，例如在使用 Safari 的翻譯功能時，不會將網頁位址傳送給 Apple。

Do note that Private Browsing does not save cookies and website data, so it won't be possible to remain signed in to sites. 這可能會帶來不便。

#### iCloud 同步

Safari 的歷史記錄、分頁群組、iCloud 分頁和已儲存密碼的同步都採用 E2EE 加密。 但預設情況下，書籤[並非如此](https://support.apple.com/HT202303)。 Apple 可以根據其[隱私權政策](https://apple.com/legal/privacy/en-ww)解密並存取它們。

您可以為 Safari 書籤和下載啟用 E2EE ，只需啟用「[進階資料防護](https://support.apple.com/HT212520)」即可。 Go to :gear: **Settings** → **iCloud** → **Advanced Data Protection**.

- [x] 開啟 **進階資料保護**

If you use iCloud with Advanced Data Protection disabled, we also recommend setting Safari's default download location to a local folder on your device. This option can be found in :gear: **Settings** → **Apps** → **Safari** → **General** → **Downloads**.

## 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用專案前先熟悉此清單，並自行研究，以確保它是適合您的選擇。

### 最低要求

- 必須支援自動更新
- 必須快速接收來自上游版本的引擎更新
- 必須支援內容封鎖
- 為了使瀏覽器更尊重隱私權而作的任何變動都不應對用戶體驗產生負面影響
