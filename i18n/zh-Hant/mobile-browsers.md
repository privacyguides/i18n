---
meta_title: "Android 和 iOS 行動版尊隱私的網頁瀏覽器的-Privacy Guides"
title: "行動瀏覽器"
icon: material/cellphone-information
description: 這些瀏覽器是我們目前推薦在手機使用的標準/非匿名互聯網瀏覽器。
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": 網頁
    name: 私人行動瀏覽器建議
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

這些是我們目前推薦的行動網頁瀏覽器和標準/非匿名網際網路瀏覽的配置。 如果你需要匿名瀏覽網際網路，你應該使用 [Tor](tor.md) 代替。 一般來說，我們建議您將擴充功能維持在最低限度：它們在瀏覽器中有特別訪問權限，需要您信任開發人員，它們也會讓瀏覽器 [特徵顯露出來](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)， [弱化](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) 網站隔離。

## 安卓

在 Android 上，Firefox 的安全性仍然低於基於 Chromium 的替代品：Mozilla引擎 [GeckoView](https://mozilla.github.io/geckoview) 尚未支援 [站點隔離](https://hacks.mozilla.org/2021/05/introducing-firefox-new-site-isolation-security-architecture)或啟用[隔離進程](https://bugzilla.mozilla. org/show_bug.cgi?id=1565196)。

### Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** 內建內容封鎖程式和[隱私權功能](https://brave.com/privacy-features/) ，其中許多功能預設已啟用。

Brave 建立在 Chromium 瀏覽器專案，因此令人感到熟悉並且具有最小的網站兼容性問題。

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "下載"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

#### 建議的 Brave 設定

Tor 瀏覽器是真正匿名瀏覽網際網路的唯一途徑。 當您使用Brave時，我們建議您更改以下設定，以保護您的隱私免受某些影響，但除 [Tor 瀏覽器](tor.md#tor-browser) 外其它覽器在某些方面都可能 *被追蹤* 。

這些選項可以在 :material-menu: → **設置** → **Brave Shields & 隱私**中找到

##### Shields

Brave [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) 功能中包含一些防指紋措施。 我們建議在您訪問的所有網頁上[全域](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings)配置這些選項。

##### Brave屏蔽全局默認值

Shields 可以選擇根據需要依各網站情況降級，但我們建議預設以下內容：

<div class="annotate" markdown>

- [x] **阻止追蹤器和廣告**底下請選擇**積極**

<details class="warning" markdown>
<summary>使用預設過濾器列表</summary>
Brave 可在內部 `brave://adblock`頁面中選擇其他內容過濾器。 我們建議您不要使用此功能；請保留預設的篩選條件清單。 使用額外清單將使您在一般 Brave 用戶中被突顯出來，如果Brave有漏洞，並將惡意規則添加到您使用的清單中，也可能會增加攻擊面。

</details>

- [x] 選擇 **昇級使用 HTTPS 連接**
- [x] 選擇 **一直使用安全連接**
- [x] (可選的) 選擇 **封鎖腳本** (1)
- [x] **Block fingerprinting** 選擇 **嚴格(可能會打斷網站)**

</div>

1. 此選項提供的功能類似uBlock Origin 進階 [封鎖模式](https://github.com/gorhill/uBlock/wiki/Blocking-mode) 或 [NoScript](https://noscript.net) 擴展。

##### 清除瀏覽資料

- [x] Select **清除出口**的數據

##### 社交媒體屏蔽

- [ ] 取消勾選所有社交媒體組件

##### 其他隱私設定

<div class="annotate" markdown>

- [x] 選擇 **在[WebRTC IP處理政策](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)**
- [ ]取消勾選 **允許網站檢查您是否儲存了付款方式**
- [ ]取消勾選 **IPFS閘道** (1)
- [x] 選擇 **關閉出口標籤**
- [ ] 取消勾選**允許隱私保護產品分析(P3A)**
- [ ] 取消勾選 **自動發送診斷報告**
- [ ] 取消勾選 **自動發送每日使用情況給Brave**

</div>

1. InterPlanetary File System (IPFS)是一個分散的對等網絡，用於在分布式文件系統中存儲和共享數據。 除非您使用此功能，否則禁用它。

#### Brave 同步

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) 可在不同設備上訪問瀏覽數據（歷史記錄，書籤等），而無需帳戶且具 E2EE保護。

## iOS

在 iOS上，任何可以瀏覽網頁的應用程式都是 [限制](https://developer.apple.com/app-store/review/guidelines) 使用 Apple 提供的 [WebKit 框架](https://developer.apple.com/documentation/webkit)，因此沒有理由使用第三方瀏覽器。

### Safari

<div class="admonition recommendation" markdown>

![Safari logo](assets/img/browsers/safari.svg){ align=right }

**Safari** 是iOS 預設瀏覽器。 它包括[隱私功能](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0)如: [智慧追蹤預防](https://webkit.org/blog/7675/intelligent-tracking-prevention）、隱私權報告、獨立且短暫的私密瀏覽標籤、iCloud 私密中繼、透過隨機化並向網站呈現簡化版本的系統配置來實現指紋保護，以便更多設備看起來相同，以及使用生物識別資訊/PIN 鎖定私人標籤的能力。 它可以使用不同的配置檔來分開瀏覽。

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentation}

</details>

</div>

#### 建議的 Firefox 設定

這些選項可以在 :gear: **Safari** →**設定**中找到。

##### 設定檔

所有 cookie、歷史記錄和網站資料對於每個設定檔都是獨立的。 您應該將不同設定檔用於不同目的，例如 購物、工作或上學。

##### 隱私 & 安全

- [x] 啓用 **防止跨網站跟蹤**

    這將啟用 WebKit [智慧型跟蹤保護](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp)。 該功能透過設備的機器學習來阻止跟蹤器不必要的跟蹤。 ITP 可以防止許多常見的威脅，但它不會阻止所有跟蹤途徑，因為它的設計不會干擾網站的可用性。

- [x] 啟用**需要Face ID 才能解鎖私密瀏覽**

    此設定可將私人分頁在不使用時鎖定在生物辨識/PIN 裏。

##### 進階 → 隱私

**進階追蹤與指紋辨識保護**設定將隨機化某些值，以便更難進行指紋辨識：

- [x] 選擇 **所有瀏覽** 或 **私密瀏覽**

##### 隱私報告

隱私報告提供跨網站追蹤器的快照，瀏覽器如何防止追蹤器在您訪問的網站上分析您的狀況。 它還可以顯示每週報告，以顯示哪些追蹤器隨著時間的推移被封鎖。

隱私權報告可透過「頁面設定」選單存取。

##### 隱私保護廣告測量

- [ ] 禁用 **隱私保留廣告計量**

廣告點擊測量是過去用來追蹤侵犯用戶隱私的技術。 [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) 是一個 WebKit 功能和提議的網頁標準，旨在允許廣告商在不影響用戶隱私的情況下衡量網站活動的有效性。

此功能本身沒有什麼隱私疑慮，因此您可以選擇不管它，但我們認為，它在私密瀏覽中自動停用反而顯示出功能被關閉的情況。

##### 一直保持私密瀏覽

開啟Safari ，然後點按右下角的「標籤」按鈕。 然後，擴展標籤組列表。

- [x] 選擇 **私密**

Safari的私人瀏覽模式提供額外的隱私保護。 隱私瀏覽每個標籤分頁使用新的 [短暫](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) 工作階段，這意味著標籤彼此隔離。 隱私瀏覽還有其他較小的隱私優勢，例如在使用Safari的翻譯功能時不會將網頁的地址傳送給Apple。

請注意，「私密瀏覽」不會儲存Cookie和網站資料，因此無法繼續登入網站。 這可能會造成不便。

##### iCloud 同步

Safari 歷史記錄、標籤組、iCloud 標籤分頁和保存密碼的同步都是 E2EE。 但預設情況下，書籤[沒有](https://support.apple.com/HT202303)。 Apple可以根據其 [隱私權政策](https://apple.com/legal/privacy/en-ww)解密並存取它們。

您可以為Safari 書籤和下載啟用 E2EE ，只需啟用 [Advanced Data Protection](https://support.apple.com/HT212520)即可。 請在 **Apple ID name → iCloud → 進階資料保護**.

- [x] 開啟 **進階資料保護**

如果您在禁用「進階資料保護」的情況下使用iCloud ，我們亦建議您檢查，確保 Safari 預設下載位置已設定為裝置上的本機位置。 此選項可在 :gear: **設定** → **Safari** → **一般** → **下載**中找到。

## 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 必須支援自動更新。
- 必須在上遊發布後的0-1天內收到引擎更新。
- 為了使瀏覽器更尊重隱私權而作的任何變動都不應對用戶體驗產生負面影響。
- 安卓版瀏覽器必須使用 Chromium 引擎。
    - 不幸的是， Mozilla GeckoView仍然不如Android上的Chromium安全。
    - iOS瀏覽器僅限於WebKit。
