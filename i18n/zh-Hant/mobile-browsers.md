---
title: "行動瀏覽器"
icon: material/cellphone-information
description: 這些瀏覽器是我們目前推薦在手機使用的標準/非匿名互聯網瀏覽器。
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Private Mobile Browser Recommendations
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
      - 安卓
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

    ! [Brave logo] (assets/img/browsers/brave.svg) {align = right}
    
    * * Brave Browser * *內建內容封鎖程式和[隱私權功能] (https://brave.com/privacy-features/) ，其中許多功能預設已啟用。
    
    Brave 建立在 Chromium 瀏覽器專案，因此令人感到熟悉並且具有最小的網站兼容性問題。
    
    [:octicons-home-16: Homepage](https://brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }
    
    ??? 下載說明
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

#### 建議配置

Tor 瀏覽器是真正匿名瀏覽網際網路的唯一途徑。 當您使用Brave時，我們建議您更改以下設定，以保護您的隱私免受某些影響，但除 [Tor 瀏覽器](tor.md#tor-browser) 外其它覽器在某些方面都可能 *被追蹤* 。

這些選項可以在 :material-menu: → **設置** → **Brave Shields & 隱私**中找到

##### Shields

Brave [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-) 功能包含一些防指紋識別措施。 我們建議您在所有瀏覽的網頁上設定這些選項 [全局](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) 。

##### Brave shields global defaults

Shields' options can be downgraded on a per-site basis as needed, but by default we recommend setting the following:

<div class="annotate" markdown>

- [x] Select **Aggressive** under Block trackers & ads

    ??? warning "Use default filter lists"
        Brave allows you to select additional content filters within the internal `brave://adblock` page. We advise against using this feature; instead, keep the default filter lists. Using extra lists will make you stand out from other Brave users and may also increase attack surface if there is an exploit in Brave and a malicious rule is added to one of the lists you use.

- [x] Select **Upgrade connections to HTTPS**
- [x] Select **Always use secure connections**
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Strict, may break sites** under **Block fingerprinting**

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net/) extension.

##### Clear browsing data

- [x] Select **Clear data on exit**

##### Social Media Blocking

- [ ] Uncheck all social media components

##### Other privacy settings

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP Handling Policy](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Uncheck **Allow sites to check if you have payment methods saved**
- [ ] Uncheck **IPFS Gateway** (1)
- [x] Select **Close tabs on exit**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Automatically send daily usage ping to Brave**

</div>

1. InterPlanetary File System (IPFS) is a decentralized, peer-to-peer network for storing and sharing data in a distributed filesystem. Unless you use the feature, disable it.

#### Brave 同步

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

## iOS

On iOS, any app that can browse the web is [restricted](https://developer.apple.com/app-store/review/guidelines) to using an Apple-provided [WebKit framework](https://developer.apple.com/documentation/webkit), so there is little reason to use a third-party web browser.

### Safari

!!! recommendation

    ! [Safari logo] (assets/img/browsers/safari.svg) {align = right}
    
    * * Safari * *是iOS 預設瀏覽器。 它包括[隱私權功能] (https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0) ，例如智慧追蹤保護、隱私權報告、獨立的私人瀏覽標籤、iCloud 私人中繼和自動HTTPS  升級。
    
    [:octicons-home-16: Homepage](https://www.apple.com/safari/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.apple.com/legal/privacy/data/en/safari/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentation}

#### 建議配置

這些選項可在 :gear: **設定** → **Safari** → **隱私權和安全性**中找到。

##### 跨網站追蹤預防

- [x] Enable **Prevent Cross-Site Tracking**

This enables WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). The feature helps protect against unwanted tracking by using on-device machine learning to stop trackers. ITP protects against many common threats, but it does not block all tracking avenues because it is designed to not interfere with website usability.

##### 隱私報告

隱私報告提供跨網站追蹤器的快照，瀏覽器如何防止追蹤器在您訪問的網站上分析您的狀況。 它還可以顯示每週報告，以顯示哪些追蹤器隨著時間的推移被封鎖。

隱私權報告可透過「頁面設定」選單存取。

##### Privacy Preserving Ad Measurement

- [ ] Disable **Privacy Preserving Ad Measurement**

Ad click measurement has traditionally used tracking technology that infringes on user privacy. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm/) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

The feature has little privacy concerns on its own, so while you can choose to leave it on, we consider the fact that it's automatically disabled in Private Browsing to be an indicator for disabling the feature.

##### Always-on Private Browsing

Open Safari and tap the Tabs button, located in the bottom right. Then, expand the Tab Groups list.

- [x] Select **Private**

Safari's Private Browsing mode offers additional privacy protections. Private Browsing uses a new [ephemeral](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) session for each tab, meaning tabs are isolated from one another. There are also other smaller privacy benefits with Private Browsing, such as not sending a webpage’s address to Apple when using Safari's translation feature.

Do note that Private Browsing does not save cookies and website data, so it won't be possible to remain signed into sites. This may be an inconvenience.

##### iCloud 同步

Safari 歷史記錄、標籤組、iCloud 標籤分頁和保存密碼的同步都是 E2EE。 但默認情況下，書籤[不是](https://support.apple.com/en-us/HT202303)。 Apple可以根據其 [隱私權政策](https://www.apple.com/legal/privacy/en-ww/)解密並存取它們。

您可以為Safari 書籤和下載啟用 E2EE ，只需啟用 [Advanced Data Protection](https://support.apple.com/en-us/HT212520)即可。 Go to your **Apple ID name → iCloud → Advanced Data Protection**.

- [x] Turn On **Advanced Data Protection**

If you use iCloud with Advanced Data Protection disabled, we also recommend checking to ensure Safari's default download location is set to locally on your device. This option can be found in :gear: **Settings** → **Safari** → **General** → **Downloads**.

### AdGuard

!!! recommendation

    ! [AdGuard logo] (assets/img/browsers/adguard.svg) {align = right}
    
    * *適用於 iOS的 AdGuard * *是使用原生[Content Blocker API] (https://developer.apple.com/documentation/safariservices/creating_a_content_blocker 的Safari 免費開源內容封鎖擴展。
    
    iOS 版 AdGuard 有一些高級功能；然而，標準Safari 內容封鎖是免費的。
    
    [:octicons-home-16: Homepage](https://adguard.com/en/adguard-ios/overview.html){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://adguard.com/privacy/ios.html){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="Source Code" }
    
    ??? 下載
    
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id1047223162)

額外的過濾器清單會減慢速度，並可能會增加您的攻擊面，因此只應用您需要的東西。

## 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

!!! 示例“此部分是新的”

    我們正在努力為我們網站的每個部分建立定義的標準，這可能會有所變化。 如果您對我們的標準有任何疑問，請在[論壇上提問] (https://discuss.privacyguides.net/latest) ，如果沒有列出，請不要認為我們在提出建議時沒有考慮到某些事情。 當我們推薦一個項目時，有許多因素被考慮和討論，記錄每一個項目都是正在進行式。

### 最低合格要求

- 必須支援自動更新。
- 必須在上遊發布後的0-1天內收到引擎更新。
- 為了使瀏覽器更尊重隱私權而作的任何變動都不應對用戶體驗產生負面影響。
- 安卓版瀏覽器必須使用 Chromium 引擎。
    - 不幸的是， Mozilla GeckoView仍然不如Android上的Chromium安全。
    - iOS browsers are limited to WebKit.

### 擴展元件標準

- 不得複製內建瀏覽器或作業系統功能。
- 必須直接影響用戶隱私，即不得簡單地提供資訊。
