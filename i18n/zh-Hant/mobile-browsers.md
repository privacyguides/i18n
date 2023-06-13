---
meta_title: "Android 和 iOS 行動版尊隱私的網頁瀏覽器的-Privacy Guides"
title: "行動瀏覽器"
icon: material/cellphone-information
description: 這些瀏覽器是我們目前推薦在手機使用的標準/非匿名互聯網瀏覽器。
cover: mobile-browsers.png
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
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
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://www.apple.com/safari/
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

這些是我們目前推薦的行動網頁瀏覽器和標準/非匿名網際網路瀏覽的配置。 如果你需要匿名瀏覽網際網路，你應該使用 [Tor](tor.md) 代替。 一般來說，我們建議您將擴充功能維持在最低限度：它們在瀏覽器中有特別訪問權限，需要您信任開發人員，它們也會讓瀏覽器 [特徵顯露出來](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)， [弱化](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) 網站隔離。

## 安卓

在安卓系統上， Firefox 仍然不如基於 Chromium 的替代品安全： Mozilla 的引擎 [GeckoView](https://mozilla.github.io/geckoview/)尚未支持 [站點隔離](https://hacks.mozilla.org/2021/05/introducing-firefox-new-site-isolation-security-architecture) 或啟用 [隔離流程](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196)。

### Brave

!!! recommendation

    ![Brave logo](assets/img/browsers/brave.svg){ align=right }
    
    **Brave Browser** 內建內容封鎖程式和[隱私權功能](https://brave.com/privacy-features/) ，其中許多功能預設已啟用。
    
    Brave 建立在 Chromium 瀏覽器專案，因此令人感到熟悉並且具有最小的網站兼容性問題。
    
    [:octicons-home-16: Homepage](https://brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }
    
    ??? downloads anotate "下載"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

#### 建議配置

Tor 瀏覽器是真正匿名瀏覽網際網路的唯一途徑。 當您使用Brave時，我們建議您更改以下設定，以保護您的隱私免受某些影響，但除 [Tor 瀏覽器](tor.md#tor-browser) 外其它覽器在某些方面都可能 *被追蹤* 。

這些選項可以在 :material-menu: → **設置** → **Brave Shields & 隱私**中找到

##### Shields

Brave [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-) 功能包含一些防指紋識別措施。 我們建議您在所有瀏覽的網頁上設定這些選項 [全局](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) 。

##### Brave屏蔽全局默認值

Shields 可以選擇根據需要依各網站情況降級，但我們建議預設以下內容：

<div class="annotate" markdown>

- [x] 阻止追蹤器和廣告 選擇**積極**

    ??? warning "使用預設過濾器列表"
        Brave 允許您在內部 `brave://adblock`頁面中選擇其他內容過濾器。 我們建議您不要使用此功能；請保留預設的篩選條件清單。 使用額外清單將使您在一般 Brave 用戶中被突顯出來，如果Brave有漏洞，並將惡意規則添加到您使用的清單中，也可能會增加攻擊面。

- [x] 選擇 **昇級使用 HTTPS 連接**
- [x] 選擇 **一直使用安全連接**
- [x] (可選的) 選擇 **封鎖腳本** (1)
- [x] **Block fingerprinting** 選擇 **嚴格(可能會打斷網站)**

</div>

1. 此選項提供的功能類似uBlock Origin 進階 [封鎖模式](https://github.com/gorhill/uBlock/wiki/Blocking-mode) 或 [NoScript](https://noscript.net/) 擴展。

##### 清除瀏覽資料

- [x] Select **清除出口**的數據

##### 社交媒體屏蔽

- [ ] 取消勾選所有社交媒體組件

##### 其他隱私設定

<div class="annotate" markdown>

- [x] 選擇 **在[WebRTC IP處理政策](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- []取消勾選 **允許網站檢查您是否儲存了付款方式**
- []取消勾選 **IPFS閘道** (1)
- [x] 選擇 **關閉出口標籤**
- [ ] 取消勾選**允許隱私保護產品分析(P3A)**
- [ ] 取消勾選 **自動發送診斷報告**
- [ ] 取消勾選 **自動發送每日使用情況給Brave**

</div>

1. InterPlanetary File System (IPFS)是一個分散的對等網絡，用於在分布式文件系統中存儲和共享數據。 除非您使用此功能，否則禁用它。

#### Brave 同步

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) 允許您在不同設備上訪問瀏覽數據（歷史記錄，書籤等），而無需帳戶且有 E2EE保護。

## iOS

在 iOS上，任何可以瀏覽網頁的應用程式都是 [限制](https://developer.apple.com/app-store/review/guidelines) 使用 Apple 提供的 [WebKit 框架](https://developer.apple.com/documentation/webkit)，因此沒有理由使用第三方瀏覽器。

### Safari

!!! recommendation

    ![Safari logo](assets/img/browsers/safari.svg){ align=right }
    
    **Safari** 是iOS 預設瀏覽器。 It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention/), Privacy Report, isolated and ephemeral Private Browsing tabs, iCloud Private Relay, and fingerprinting reduction by presenting a simplified version of the system configuration to websites so more devices look identical.
    
    Safari is restricted to Apple devices and is covered by [System Integrity Protection](https://support.apple.com/guide/security/system-integrity-protection-secb7ea06b49/web), a security feature which limits system programs and files to being read-only so they can't be tampered with by you or malware.
    
    [:octicons-home-16: Homepage](https://www.apple.com/safari/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.apple.com/legal/privacy/data/en/safari/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentation}

#### 建議配置

這些選項可在 :gear: **設定** → **Safari** → **隱私權和安全性**中找到。

##### 跨網站追蹤預防

- [x] 啓用 **防止跨網站跟蹤**

這將啟用 WebKit [智慧型跟蹤保護](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp)。 該功能透過設備的機器學習來阻止跟蹤器不必要的跟蹤。 ITP 可以防止許多常見的威脅，但它不會阻止所有跟蹤途徑，因為它的設計不會干擾網站的可用性。

##### 隱私報告

隱私報告提供跨網站追蹤器的快照，瀏覽器如何防止追蹤器在您訪問的網站上分析您的狀況。 它還可以顯示每週報告，以顯示哪些追蹤器隨著時間的推移被封鎖。

隱私權報告可透過「頁面設定」選單存取。

##### 隱私保護廣告測量

- [ ] 禁用 **隱私保留廣告計量**

廣告點擊測量是過去用來追蹤侵犯用戶隱私的技術。 [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm/) 是一個 WebKit 功能和提議的網頁標準，旨在允許廣告商在不影響用戶隱私的情況下衡量網站活動的有效性。

此功能本身沒有什麼隱私疑慮，因此您可以選擇不管它，但我們認為，它在私密瀏覽中自動停用反而顯示出功能被關閉的情況。

##### 一直保持私密瀏覽

開啟Safari ，然後點按右下角的「標籤」按鈕。 然後，擴展標籤組列表。

- [x] 選擇 **私密**

Safari的私人瀏覽模式提供額外的隱私保護。 隱私瀏覽每個標籤分頁使用新的 [短暫](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) 工作階段，這意味著標籤彼此隔離。 隱私瀏覽還有其他較小的隱私優勢，例如在使用Safari的翻譯功能時不會將網頁的地址傳送給Apple。

請注意，「私密瀏覽」不會儲存Cookie和網站資料，因此無法繼續登入網站。 這可能會造成不便。

##### iCloud 同步

Safari 歷史記錄、標籤組、iCloud 標籤分頁和保存密碼的同步都是 E2EE。 但默認情況下，書籤[不是](https://support.apple.com/en-us/HT202303)。 Apple可以根據其 [隱私權政策](https://www.apple.com/legal/privacy/en-ww/)解密並存取它們。

您可以為Safari 書籤和下載啟用 E2EE ，只需啟用 [Advanced Data Protection](https://support.apple.com/en-us/HT212520)即可。 請在 **Apple ID name → iCloud → 進階資料保護**.

- [x] 開啟 **進階資料保護**

如果您在禁用「進階資料保護」的情況下使用iCloud ，我們亦建議您檢查，確保 Safari 預設下載位置已設定為裝置上的本機位置。 此選項可在 :gear: **設定** → **Safari** → **一般** → **下載**中找到。

### AdGuard

!!! recommendation

    ![AdGuard logo](assets/img/browsers/adguard.svg){ align=right }
    
    **適用於 iOS的 AdGuard** 是使用原生[Content Blocker API](https://developer.apple.com/documentation/safariservices/creating_a_content_blocker) 的Safari 免費開源內容封鎖擴展。
    
    iOS 版 AdGuard 有一些高級功能；然而，標準Safari 內容封鎖是免費的。
    
    [:octicons-home-16: Homepage](https://adguard.com/en/adguard-ios/overview.html){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://adguard.com/privacy/ios.html){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="Source Code" }
    
    ??? downloads "下載"
    
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id1047223162)

額外的過濾器清單會減慢速度，並可能會增加您的攻擊面，因此只應用您需要的東西。

## 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

!!! example "此部分是新的"

    我們正在努力為我們網站的每個部分建立定義的標準，這可能會有所變化。 如果您對我們的標準有任何疑問，請在[論壇上提問] (https://discuss.privacyguides.net/latest) ，如果沒有列出，請不要認為我們在提出建議時沒有考慮到某些事情。 當我們推薦一個項目時，有許多因素被考慮和討論，記錄每一個項目都是正在進行式。

### 最低合格要求

- 必須支援自動更新。
- 必須在上遊發布後的0-1天內收到引擎更新。
- 為了使瀏覽器更尊重隱私權而作的任何變動都不應對用戶體驗產生負面影響。
- 安卓版瀏覽器必須使用 Chromium 引擎。
    - 不幸的是， Mozilla GeckoView仍然不如Android上的Chromium安全。
    - iOS瀏覽器僅限於WebKit。

### 擴展元件標準

- 不得複製內建瀏覽器或作業系統功能。
- 必須直接影響用戶隱私，即不得簡單地提供資訊。
