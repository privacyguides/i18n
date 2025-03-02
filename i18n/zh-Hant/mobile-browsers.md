---
meta_title: "尊重隱私的 Android 和 iOS 網路瀏覽器 - Privacy Guides"
title: "行動瀏覽器"
icon: material/cellphone-information
description: 我們目前推薦的這些瀏覽器適合在手機上進行標準/非匿名的網路瀏覽。
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": 網頁
    name: 推薦的隱私行動瀏覽器
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
    applicationCategory: 網路瀏覽器
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>防護下列威脅：</small>

- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

這些是我們目前推薦的**行動瀏覽器**與其設定，適合普通或非匿名的網頁瀏覽。 如果您需要匿名瀏覽網際網路，應該使用 [Tor](tor.md)。

## Brave

<div class="admonition recommendation" markdown>

![Brave 標誌](assets/img/browsers/brave.svg){ align=right }

**Brave 瀏覽器** 內建內容封鎖程式和[隱私權功能](https://brave.com/privacy-features/) ，其中許多功能預設為啟用。

Brave 基於 Chromium 瀏覽器專案構建，因此使用起來應該會感到熟悉，並且具有最少的網站兼容性問題。

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

Tor 瀏覽器是真正匿名瀏覽網際網路的唯一途徑。 當您使用 Brave 時，我們建議您更改以下設定，以保護您的隱私免受第三者影響，但除了 [Tor 瀏覽器](tor.md#tor-browser)以外的所有瀏覽器都可能以某種方式或另一種方式被 *某人* 追蹤。

=== "Android"

    這些選項可以在 :material-menu: → **設定** → **Brave 防護與安全性** 中找到。

=== "iOS"

    這些選項可以在 :fontawesome-solid-ellipsis: → **設定** → **Shields 與隱私權** 中找到。

#### Brave 防護全域預設設定

Brave 的[防護 (Shields)](https://support.brave.com/hc/articles/360022973471-What-is-Shields) 功能包含一些防指紋識別措施。 我們建議在您訪問的所有網頁上[全域](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings)套用這些設定。

防護功能的選項可以根據各網站需要依情況降級，但我們建議預設使用以下設定：

=== "Android"

    <div class="annotate" markdown>

    - [x] 將 *封鎖追蹤器與廣告* 設定為 **積極**
    - [x] 勾選 **自動重定向 AMP 頁面**
    - [x] 勾選 **自動重新導向追蹤 URL**
    - [x] 將 *升級連線至 HTTPS* 設定為 **要求所有連線使用 HTTPS (嚴格)**
    - \[x\] (選擇性) 勾選 **阻擋指令稿** (1)
    - [x] 將 *封鎖 Cookies* 設定為 **封鎖第三方 Cookie**
    - [x] 勾選 **封鎖指紋識別**
    - [x] 勾選 **透過語言設定防止指紋辨識攻擊**

    <details class="warning" markdown>
    <summary>使用預設篩選清單</summary>

    Brave 允許您在 **內容過濾** 選單或瀏覽器內部的 `brave://adblock` 頁面中啟用其他內容篩選清單。 我們建議您不要使用此功能；請保留預設的內容篩選清單。 使用額外的清單將使您從其他 Brave 使用者中脫穎而出，並且如果 Brave 存在漏洞，而您使用的清單之一被加入了惡意規則，也可能會增加攻擊面。

    </details>

    - [x] 勾選 **當我關閉此網站時忘記我**

    </div>

    1. 此選項會停用 JavaScript，這會破壞許多網站。 若您想要避免破壞它們，可以針對個別需要的網站設定例外。只需按一下網址列上的 Shield 圖示，然後在 *進階控制* 下取消勾選此設定即可。

=== "iOS"

    <div class="annotate" markdown>

    - [x] 將 *追蹤器和廣告封鎖* 設定為 **積極**
    - [x] 將 *將連線升級為 HTTPS* 設定為 **嚴格**
    - [x] 勾選 **自動重新導向 AMP 頁面**
    - [x] 勾選 **自動重新導向追蹤 URL**
    - \[x\] (選擇性) 勾選 **封鎖指令碼** (1)
    - [x] 勾選 **封鎖指紋識別**
    - [x] Select **Site Tabs Closed** under *Auto Shred*

    <details class="warning" markdown>
    <summary>使用預設篩選清單</summary>

    Brave 允許您在 **內容過濾** 選單中啟用其他內容篩選清單。 我們建議您不要使用此功能；請保留預設的內容篩選清單。 使用額外的清單將使您從其他 Brave 使用者中脫穎而出，並且如果 Brave 存在漏洞，而您使用的清單之一被加入了惡意規則，也可能會增加攻擊面。

    </details>

    </div>

    1. 此選項會停用 JavaScript，這會破壞許多網站。 若您想要避免破壞它們，可以針對個別需要的網站設定例外。只需按一下網址列上的 Shield 圖示，然後在 *進階控制* 下取消勾選此設定即可。

##### 清除瀏覽資料 (僅適用於 Android)

- [x] 勾選 **結束時清除資料**

##### 阻擋社群媒體 (僅適用於 Android)

- [ ] 取消勾選所有社群媒體元件

#### 其他隱私設定

=== "Android"

    <div class="annotate" markdown>

    - [x] 將 [*WebRTC IP 處理政策*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc) 設定為 **停用非代理 UDP**
    - [x] （可選） 將 *安全瀏覽* 設定為 **無防護** (1)
    - [ ] 取消勾選 **允許網站檢查是否有已儲存的付款方式**
    - [ ] Uncheck **V8 Optimizer** under *Manage V8 security*
    - [x] 勾選 **退出時關閉分頁**
    - [ ] 取消勾選 **允許保護私隱的產品分析 (P3A)**
    - [ ] 取消勾選 **自動傳送診斷報告**
    - [ ] 取消勾選 **自動傳送每日使用 ping 到 Brave**

    </div>

    1. Brave 在 Android 上[實作的安全瀏覽](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) **不會** 像電腦版一樣代理 [安全瀏覽服務的網路請求](https://developers.google.com/safe-browsing/v4/update-api#checking-urls)。 這表示 Google 可能會看到 (並記錄) 您的 IP 位址。 請注意，安全瀏覽功能不適用於沒有 Google Play 服務的 Android 裝置。

=== "iOS"

    - [ ] 取消勾選 **允許保護隱私的產品分析 (P3A)**
    - [ ] 取消勾選 **自動傳送每日使用 ping 到 Brave**

#### Leo

這些選項可以在 :material-menu: → **設定** → **Leo** 中找到。

<div class="annotate" markdown>

- [ ] 取消勾選 **在網址列顯示自動完成建議** (1)

</div>

1. Brave 的 iOS 版應用程式中沒有此選項。

#### 搜尋引擎

這些選項可以在 :material-menu:/:fontawesome-solid-ellipsis: → **設定** → **搜尋引擎** 中找到。

- [ ] 取消勾選 **顯示搜尋建議**

#### Brave 同步

[Brave 同步](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) 可在不同裝置上存取瀏覽數據 (歷史記錄，書籤等)，無需帳戶且受 E2EE 保護。

## Cromite (Android)

<div class="admonition recommendation" markdown>

![Cromite 標誌](assets/img/browsers/cromite.svg){ align=right }

**Cromite** 是一個基於 Chromium 的瀏覽器，內建廣告封鎖、指紋保護及其他[隱私與安全強化功能](https://github.com/uazo/cromite/blob/master/docs/FEATURES.md)。 它是已停止維護的 **Bromite** 瀏覽器之分支。

[:octicons-home-16: Homepage](https://cromite.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uazo/cromite/blob/master/docs/PRIVACY_POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/uazo/cromite?tab=readme-ov-file#docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/uazo/cromite){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: F-Droid](https://cromite.org/fdroid/repo/?fingerprint=49F37E74DEE483DCA2B991334FB5A0200787430D0B5F9A783DD5F13695E9517B)
- [:simple-github: GitHub](https://github.com/uazo/cromite/releases/latest)

</details>

</div>

### 建議的設定

這些選項可以在 :material-menu: → :gear: **設定** → **隱私權和安全性** 中找到。

#### Browsing data

- [x] 勾選 **Close all open tabs on exit**

#### 無痕模式

- [x] 勾選 **Open external links in incognito**

#### 安全性

- [x] 勾選 **一律使用安全連線**

這可以防止您無意間以明文 HTTP 連線到網站。 如今，僅支援 HTTP 的網站已不多見，因此這對您日常瀏覽的影響幾乎沒有影響。

#### Adblock Plus settings

這些選項可以在 :material-menu: → :gear: **設定** → **Adblock Plus settings** 中找到。

Cromite contains a customized version of Adblock Plus with EasyList enabled by default, as well as options to select more filter lists within the **Filter lists** menu.

使用額外的清單將使您從其他 Cromite 使用者中脫穎而出，並且如果瀏覽器存在漏洞，而您使用的清單之一被加入了惡意規則，也可能會增加攻擊面。

- \[x\] (選擇性) 勾選 **Enable anti-circumvention and snippets**

此設定會新增額外的 Adblock Plus 清單，可能會提高 Cromite 封鎖內容的效能。 關於從其他使用者中脫穎而出和潛在增加攻擊面的警告仍然適用。

#### Legacy Adblock settings

這些選項可以在 :material-menu: → :gear: **設定** → **Legacy Adblock settings** 中找到。

- [x] 勾選 Autoupdate disabled

這會停用對已停止維護的 Bromite 廣告過濾器的更新檢查。

## Safari (iOS)

在 iOS 上，任何可以瀏覽網頁的應用程式都[只能](https://developer.apple.com/app-store/review/guidelines)使用 Apple 提供的 [WebKit 框架](https://developer.apple.com/documentation/webkit)，因此 [Brave](#brave) 這類瀏覽器無法像其他作業系統一樣使用 Chromium 引擎。

<div class="admonition recommendation" markdown>

![Safari 標誌](assets/img/browsers/safari.svg){ align=right }

**Safari** 是 iOS 的預設瀏覽器。 It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites, so more devices look identical), and fingerprint randomization, as well as Private Relay for those with a paid iCloud+ subscription.

[:octicons-home-16: 首頁](https://www.apple.com/tw/safari/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.apple.com/tw/legal/privacy/data/zh-tw/safari/){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://support.apple.com/zh-tw/guide/iphone/iph1fbef4daa/ios){ .card-link title="說明文件" }

</details>

</div>

### 建議的 Safari 設定

如果您想要在 Safari 中使用內容阻擋器，我們建議您安裝 [AdGuard](browser-extensions.md#adguard)。

可以在 :gear: **設定** → **Safari** 中找到以下與隱私及安全相關的選項。

#### 允許 SAFARI 取用

在 **Siri 與搜尋** 選單中:

- [ ] 停用 **從此 App 學習**
- [ ] 停用 **在 App 中顯示**
- [ ] 停用 **在主畫面上顯示**
- [ ] 停用 **建議 App**

這可以防止 Siri 使用 Safari 中的內容來提供 Siri 建議。

#### 搜尋

- [ ] 停用 **搜尋引擎建議**

此設定會將您在網址列中輸入的內容傳送至 Safari 中設定的搜尋引擎。 停用搜尋建議可讓您更精確地控制您傳送給搜尋引擎供應商的資料。

#### 主題類別

Safari 可以使用不同的主題類別來分隔您的瀏覽。 您的所有 Cookie、歷史記錄和網站資料將會針對各個主題類別分開。 您應該為不同用途使用不同的主題類別，例如購物、工作或學校。

#### 隱私權與安全性

- [x] 啟用 **防止跨網站追蹤**

這將啟用 WebKit 的[智慧追蹤預防](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp)。 該功能利用裝置上的機器學習來阻止追蹤器，從而防止使用者被追蹤。 智慧追蹤預防可保護您免於許多常見威脅，但不能阻止所有追蹤途徑，因為它被設計為不會干擾網站的可用性。

- [x] 啟用 **需要 Face ID/Touch ID 來解鎖私密瀏覽**

此設定可在私密瀏覽分頁未使用時使用 生物辨識/PIN 鎖定。

- [ ] 停用 **詐騙網站警告**

此設定使用 Google 安全瀏覽功能 (中國大陸或香港的使用者則使用騰訊安全瀏覽) 在瀏覽時保護你的安全。 因此，您的 IP 位址可能會被安全瀏覽功能供應商記錄下來。 停用此設定可以防止被記錄，但也可能會更容易受到已知釣魚網站的攻擊。

- [x] Enable **Not Secure Connection Warning**

This setting shows a warning screen if your connection to a website isn't using HTTPS. Safari will automatically try to upgrade the site to HTTPS, so you should only see this when there is no HTTPS connection available.

- [ ] 停用 **Highlights**

Apple 的 Safari 隱私權政策規定：

> 瀏覽網頁時，Safari 可能會透過 OHTTP 將從網頁位址計算出的資訊傳送給 Apple，以判斷是否有相關的重點內容。

#### 網站設定

將 **相機**

- [x] 設定為 **詢問**

將 **麥克風**

- [x] 設定為 **詢問**

將 **位置**

- [x] 設定為 **詢問**

這些設定可確保網站只有在您選擇允許後，才能存取您的相機、麥克風或位置。

#### 其他隱私設定

這些選項可以在 :gear: **設定** → **Safari** → **進階** 中找到。

##### 進階追蹤和指紋保護

**進階追蹤和指紋保護** 設定將隨機化某些參數，可使網站更難以進行指紋辨識：

- [x] 選擇 **所有瀏覽** 或 **私密瀏覽**

##### 維護隱私權廣告測量

- [ ] 停用 **維護隱私權廣告測量**

廣告點擊測量通常會使用侵犯使用者隱私的追蹤技術。 「[私密點擊測量](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm)」是一項針對 WebKit 的功能和提議的網頁標準，旨在讓廣告商能夠衡量網路活動的效果，同時不損害使用者隱私。

這個功能本身沒有什麼隱私疑慮，因此您可以選擇不管它，但我們認為，它在私密瀏覽中自動停用反而顯示出應該關閉該功能的理由。

#### 總是保持私密瀏覽

打開 Safari ，然後按一下右下角的標籤按鈕。 然後展開 :material-format-list-bulleted: 標籤頁群組列表。

- [x] 選擇 **私密瀏覽**

Safari 的私密瀏覽模式提供額外的隱私保護。 私密瀏覽為每個分頁使用新的[短暫](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral)工作階段，這意味著各個分頁之間是隔離的。 There are other smaller privacy benefits with Private Browsing too, such as not sending a webpage’s address to Apple when using Safari's translation feature.

要注意的是，私密瀏覽不會保存 Cookies 和網站資料，因此無法保持登入狀態。 這可能會帶來不便。

#### iCloud 同步

Safari 的歷史記錄、分頁群組、iCloud 分頁和已儲存密碼的同步都採用 E2EE 加密。 但預設情況下，書籤[並非如此](https://support.apple.com/HT202303)。 Apple 可以根據其[隱私權政策](https://apple.com/legal/privacy/en-ww)解密並存取它們。

您可以為 Safari 書籤和下載啟用 E2EE ，只需啟用「[進階資料保護](https://support.apple.com/HT212520)」即可。 前往 :gear: **Settings** → **iCloud** → **進階資料保護**。

- [x] 開啟 **進階資料保護**

如果您在不開啟「進階資料保護」的情況下使用 iCloud ，我們亦建議您檢查，確保 Safari 的預設下載位置已設定為裝置上的本機位置。 這些選項可以在 :gear: **設定** → **Safari** → **一般** → **下載項目** 中找到。

## 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用專案前先熟悉此清單，並自行研究，以確保它是適合您的選擇。

### 最低要求

- 必須支援自動更新
- 必須快速接收來自上游版本的引擎更新
- 必須支援內容封鎖
- 為了使瀏覽器更尊重隱私權而作的任何變動都不應對用戶體驗產生負面影響
