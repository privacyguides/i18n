---
meta_title: "Android 推薦: GrapheneOS 與 DivestOS - Privacy Guides"
title: "Android"
icon: 'simple/android'
description: Android 手機可考慮使用這些更為安全與尊重隱私的作業系統。
cover: android.webp
schema:
  - 
    "@context": http://schema.org
    "@type": 網頁
    name: 私密 Android 作業系統
    url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: Android
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://en.wikipedia.org/wiki/Android_(operating_system)
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": 網頁
      url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: Divest
    image: /assets/img/android/divestos.svg
    url: https://divestos.org/
    sameAs: https://en.wikipedia.org/wiki/DivestOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": Product
    name: Pixel
    brand:
      "@type": Brand
      name: Google
    image: /assets/img/android/google-pixel.png
    sameAs: https://en.wikipedia.org/wiki/Google_Pixel
    review:
      "@type": Review
      author:
        "@type": Organization
        name: Privacy Guides
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Shelter
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Auditor
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Secure Camera
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Secure PDF Viewer
    applicationCategory: Utilities
    operatingSystem: Android
---

![Android 圖標](assets/img/android/android.svg){ align=right }

**安卓開源項目** 是一個由谷歌領導的開源移動操作系統，為世界上大多數移動設備提供動力。 大多數 Android 系統的手機都經過修改，包括侵入性整合與應用程式，如 Google Play 服務，所以使用無這類侵入性功能的 Android 系統版本取代手機原本預設的安裝，可改善行動設備上的隱私。

[:octicons-home-16:](https://source.android.com){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject){ .card-link title="Source Code" }

這些是我們推薦 Android 作業系統、設備和應用程式，最大程度地提高行動設備的安全和隱私。 了解更多 Android 資訊：

[安卓概况 :material-arrow-right-drop-circle:](os/android-overview.md ""){.md-button}

## AOSP 衍生品

根據設備與這些作業系統的兼容性，列出偏好順序以安裝我們推薦的某款定制 Android 作業系統。

<div class="admonition note" markdown>
<p class="admonition-title">Note "備註"</p>

由於 OEM 停止支持，壽命終止的設備（如 GrapheneOS 或CalyxOS 的 "延長支授 "設備）沒有完整的安全補丁（軔體更新）。 這些設備無論安裝何種軟體，都不能視為完全安全。

</div>

### GrapheneOS

<div class="admonition recommendation" markdown>

![GrapheneOS logo](assets/img/android/grapheneos.svg#only-light){ align=right }
![GrapheneOS logo](assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** 是隱私與安全的最佳選擇。

GrapheneOS 提供額外的 [安全加固](https://en.wikipedia.org/wiki/Hardening_(computing)) 與隱私改善。 它有 [加固的記憶體分配器](https://github.com/GrapheneOS/hardened_malloc)、網路、感應許可與各類[安全功能](https://grapheneos.org/features). GrapheneOS 還帶有完整的軔體更新與已簽名的建置版本，因此完全支援 verified boot。

[:octicons-home-16: Homepage](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

</div>

GrapheneOS 支援 [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), 它可以像其它普通應用一樣在沙盒中執行[Google Play 服務](https://en.wikipedia.org/wiki/Google_Play_Services) 。 這意味可利用大多數 Google Play 服務，如 [推送通知](https://firebase.google.com/docs/cloud-messaging)，完全控制其權限和訪問，同時將其包含所選的特定 [工作設定檔](os/android-overview.md#work-profile) 或 [用戶設定檔](os/android-overview.md#user-profiles)。

Google Pixel 手機是目前唯一符合 GrapheneOS [硬體安全要求](https://grapheneos.org/faq#future-devices)的設備。

[為何我們推薦 GrapheneOS 而非 CalyxOS :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos ""){.md-button}

### DivestOS

<div class="admonition recommendation" markdown>

![DivestOS logo](assets/img/android/divestos.svg){ align=right }

**DivestOS** 是 [LineageOS](https://lineageos.org)的分支。
DivestOS 從 LineageOS 繼承了許多[支援的設備](https://divestos.org/index.php?page=devices&base=LineageOS)。 它具有簽名的建置，因此可在某些非 Pixel 設備上執行 [verified boot](https://source.android.com/security/verifiedboot)。

[:octicons-home-16: Homepage](https://divestos.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="Source Code" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Contribute }

</div>

DivestOS 有自動內核弱點 ([CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [補丁](https://gitlab.com/divested-mobile/cve_checker)、更少的商業專用 blobs 與自定的 [hosts](https://divested.dev/index.php?page=dnsbl) 檔案。 其強化 WebView，[Mulch](https://gitlab.com/divested-mobile/mulch)，支援 適用於所有架構的[CFI](https://en.wikipedia.org/wiki/Control - flow_integrity)和[網路狀態分割](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning)，並接收外帶更新。 DivestOS 還包括來自GrapheneOS 內核補丁，並通過 [defconfig hardening](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758)，開啟所有可用的內核安全功能。 3.4 版之後更新的內核都包括全頁[淨化](https://lwn.net/Articles/334747) ，所有 ~22 Clang 編譯的內核都啟用了 [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471)。

DivestOS 實現了一些最初為 GrapheneOS 開發的系統加固補丁。 DivestOS 16.0以上版本實現了 GrapheneOS [`網際網路`](https://developer.android.com/training/basics/network-ops/connecting) 和感應權限切換， [固化記憶體分配器](https://github.com/GrapheneOS/hardened_malloc)， [exec-spawning](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/#additional-hardening)， [JNI](https://en.wikipedia.org/wiki/Java_Native_Interface) [constification](https://en.wikipedia.org/wiki/Const_(computer_programming))，以及部分 [bionic](https://en.wikipedia.org/wiki/Bionic_(software)) 固化補丁集。 17.1 及更新版本具有GrapheneOS 的各個網路完整[MAC 隨機化](https://en.wikipedia.org/wiki/MAC_address#Randomization)選項，[`ptrace_scope`](https:/ /kernel. org/doc/html/latest/admin-guide/LSM/Yama.html) 控制，以及自動重新啟動/Wi-Fi/藍牙[逾時選項](https:// /grapheneos.org/features)。

DivestOS 以 F-Droid 為預設的應用下載服務。 通常建議 [少用 F-Droid](#f-droid)，然而這對 DivestOS 卻不可行，開發者透過 ([DivestOS 官方](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) 與 [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2))的 F-Droid 存取庫來更新他們的應用程式。 建議禁用官方 F-Droid 應用，並使用 [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic)**一併啟用DivestOS 存取庫**，以保持這些組件為最新。 至於其它應用，我們建議的獲取方式仍適用。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

DivestOS 軔體更新 [status](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS)和品管依所支援的設備不同而異。 雖取決於設備的兼容性，我们仍推薦 GrapheneOS。 對其它設備，DivestOS 是不錯的選項。

並非所有支援設備都可 verified boot，某些設備的表現較好。

</div>

## Android 設備

選購設備時，建議儘可能挑選較新的設備。 行動設備的軟體和軔體只支持時間有期限，因此購買新上市的設備可以盡可能地延長其支援壽命。

避免從電信行動營運商購置手機。 它們往往 **鎖定 bootloader** 也不支援 [OEM 解鎖](https://source.android.com/devices/bootloader/locking_unlocking)。 這類手機變體阻止安裝任何替代的 Android 發行版。

從網路市集購買二手手機必須要非常**小心**。 請檢查賣家的信譽 如果設備被盜，它有可能被輸入到 [IMEI 資料庫](https://gsma.com/get-involved/working-groups/terminal-steering-group/imei-database)。 前一位持有者的活動發生關係也將有風險。

對於 Android 設備與作業系統相容有一些提示:

- 不要購買已經達到或接近其支援壽命的設備，額外的軔體更新必須由製造商提供。
- 不要購買預裝 LineageOS 或/e/OS 或是無適當 [Verified Boot](https://source.android.com/security/verifiedboot) 支持和軔體更新的 Android 手機。 這些設備沒辦檢查是否曾遭篡改。
- 簡而言之，如果這裏沒列出某設備或 Android 發行版，都是有原因的。 請造訪[論壇](https://discuss.privacyguides.net)以了解詳細資訊！

### Google Pixel

Google Pixel 是**唯一** 推薦的手機。 由於對第三方作業系統的適當AVB 支持和 Google 定制的 [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) 安全晶片為安全元件，Pixel 硬體安全性比目前市場上其他 Android 設備強。

<div class="admonition recommendation" markdown>

![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }

眾所周知，**Google Pixel** 設備具有良好安全性，支持 [Verified Boot](https://source.android.com/security/verifiedboot)，即使安裝自定義作業系統時也是如此。

從 **Pixel 8**和 **8 Pro** 開始，Pixel 設備至少有 7年的安全更新保證，確保其使用壽命比其他競爭OEM 廠商 2-5年長得多。

[:material-shopping: Store](https://store.google.com/category/phones){ .md-button .md-button--primary }

</div>

Titan M2 這類安全元件比大多數其他手機處理器的可信執行環境更為有限，因為Titan M2 只用於秘密存儲、硬體證明和速率限制，而不是用於運行 "可信 "程式。 沒有安全元件的手機必須使用 TEE *執行所有這些功能* ，從而導致更大的攻擊面。

Google Pixel 手機使用名為Trusty 的 TEE 作業系統，它是 [開源](https://source.android.com/security/trusty#whyTrusty)，與其他許多手機不同。

Pixel 手機很容易安裝 GrapheneOS 只需依其 [網頁安裝程式](https://grapheneos.org/install/web)即可。 如果不敢自行安裝願意多花一點錢，可以看看 [NitroPhone](https://shop.nitrokey.com/shop) ，它們預裝 GrapheneOS，來自著名的 [Nitrokey](https://nitrokey.com/about) 公司。

購買 Google Pixel 的一些提醒:

- 如果想買便宜的 Pixel 設備，建議購買"**a**"型號，其為旗艦機發布後的預算款。 通常會有折扣，因為 Google 會出清庫存。
- 考慮在實體商店提供折扣與特價的商品。
- 找找國內線上折扣社區的網站。 這些可提醒有好的商品。
- Google 提供一份其設備 [支援週期](https://support.google.com/nexus/answer/4457705)的列表清單。 設備每天的價格可以計算如下： <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline" class="tml-display" style="display:inline math;"> <mfrac> <mtext>成本</mtext> <mrow> <mtext>產品終期 日期</mtext> <mo>−</mo> <mtext>當前日期</mtext> </mrow> </mfrac> </math> ，意味著設備的使用時間越長，每日成本就越低。
- 如果你的地區無法購得 Pixel ， [NitroPhone](https://shop.nitrokey.com/shop) 可提供全球配送。

## 一般應用

我們在網站上推薦了各種各樣的 Android 應用。 這裡列出的應用程式是 Android 專用、特別加強或取代重要系統功能。

### Shelter

<div class="admonition recommendation" markdown>

![Shelter logo](assets/img/android/shelter.svg){ align=right }

**Shelter** 有助於利用 Android 工作設定檔功能隔離或複制設備上的應用程式。.

Shelter 阻止聯繫人利用默認檔案管理器([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui))作跨設定檔搜尋與共享檔案 。

[:octicons-repo-16: Repository](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Source Code" }
[:octicons-heart-16:](https://patreon.com/PeterCxy){ .card-link title=Contribute }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

推薦使用 Shelter 取代 [Insular](https://secure-system.gitlab.io/Insular)和 [Island](https://github.com/oasisfeng/island)，因為 Shelter 支持[聯繫人搜索屏蔽](https://secure-system.gitlab.io/Insular/faq.html)。

當使用 Shelter 時，將信任置於其開發者，Shelter 作為[設備管理員](https://developer.android.com/guide/topics/admin/device-admin)來創建工作設定檔，它有大量權限訪問存儲在工作設定檔的資料。

</div>

### Secure Camera

<div class="admonition recommendation" markdown>

![Secure camera logo](assets/img/android/secure_camera.svg#only-light){ align=right }
![Secure camera logo](assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

**Secure Camera** 專注於隱私和安全的相機應用，可以捕捉圖像、影片和二維碼。 CameraX 供應商擴展（肖像、HDR、夜視、面部修飾和自動）也支持可用設備。

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>下載 Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

主要隱私功能包括：

- 自動移除 [Exif](https://en.wikipedia.org/wiki/Exif) 中繼資料 (設預啟用)
- 使用新的 [媒介](https://developer.android.com/training/data-storage/shared/media) API，因此不需要 [儲存權限](https://developer.android.com/training/data-storage)。
- 除非需錄制聲音，否則無需麥克風權限。

<div class="admonition note" markdown>
<p class="admonition-title">Note "備註"</p>

目前影片沒有刪除中繼資料，未來計畫要刪除。

圖片方向的中繼資料未刪除。 如果 (Secure Camera) 開啟定位， 也 **不會** 被不會偵測到。 如果之後想刪除，必須使用外部應用如[ExifEraser](data-redaction.md#exiferaser-android)。

</div>

### Secure PDF Viewer

<div class="admonition recommendation" markdown>

![Secure PDF Viewer logo](assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Secure PDF Viewer logo](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

**Secure PDF Viewer** 是基於 [pdf.js](https://en.wikipedia.org/wiki/PDF.js)的PDF 瀏覽器，無需任何權限。 此 PDF 被送入 [sandboxed](https://en.wikipedia.org/wiki/Sandbox_(software_development)) [webview](https://developer.android.com/guide/webapps/webview)。 這意味著它不需要權限就能直接存取內容或檔案。

[內容安全政策](https://en.wikipedia.org/wiki/Content_Security_Policy)用來強制要求 WebView 內的JavaScript 和造型屬性需全為靜態內容。

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary> 下載: Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## 獲取應用程式

### Obtainium

<div class="admonition recommendation" markdown>

![Obtainium logo](assets/img/android/obtainium.svg){ align=right }

**Obtainium** 應用管理器可以直接透過開發者自己的發佈頁來安裝與更新應用。(例如 GitHub, GitLab 等等.), 取代集中式的應用商店或代碼儲存庫。  在 Android 12 以上版本，可支援自動背景更新。

[:octicons-repo-16: Repository](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ImranR98/Obtainium/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads "下載"</summary>

- [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

Obtainium 可以從不同來源下載 APK  安裝檔，由使用者自行判斷其來源與應用是否可靠合法。 例如使用 Obtainium 從 [Signal APK 登錄頁 ](https://signal.org/android/apk) 來下載安裝 Signal 應該沒問題，但如果透過第三方 APK 儲放庫如 Aptoide o 或 APKPure 則可能有其它風險。 安裝惡意*更新*的風險較低，因為 Android 自身會在安裝之前驗證所有應用程式更新是否由與手機上現有應用程式為相同開發人員所簽署。

### GrapheneOS App Store

GrapheneOS 應用商店可在 [GitHub](https://github.com/GrapheneOS/Apps/releases)找到。 它支持Android 12 以上版本，並且能夠自行更新。 應用程式商店擁有由 GrapheneOS 專案建立的獨立應用程序，例如 [Auditor](https://attestation.app)、[相機](https://github.com/GrapheneOS/Camera)和[PDF 檢視器](https://github.com/GrapheneOS/PdfViewer)。 如果正在尋找這些應用程式，強烈建議從 GrapheneOS 應用程式商店而不是 Google Play 商店獲得，因為 GrapheneOS 會對自家商店的應用程式簽署 Google 無法訪問的簽名。

### Aurora Store

Google Play商店需要登錄 Google 帳戶，這對隱私來說不是很好。 可以使用替代客戶端，如 Aurora Store 來解決這個問題。

<div class="admonition recommendation" markdown>

![Aurora Store logo](assets/img/android/aurora-store.webp){ align=right }

**Aurora Store** 為 Google Play Store 客戶端，其無須 Google 帳戶 或 microG 即可下戴應用。

[:octicons-home-16: Homepage](https://auroraoss.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "下載"</summary>

- [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

Aurora Store不允許其匿名帳戶下載付費應用程式。 您可以選擇使用 Google 帳戶登錄 Aurora Store 來下載所購買的應用程式，這確實可以訪問您的 Google 安裝應用程式列表。 但仍可受益於裝置上不需要完整的 Google Play 用戶端和 Google Play 服務或 microG。

### 手動使用 RSS 通知

在GitHub和GitLab 等平台上發布的應用程式，也可在 [新聞聚合器](news-aggregators.md) 下添加 RSS 源，有助於追踪新版本消息。

![RSS APK](./assets/img/android/rss-apk-light.png#only-light) ![RSS APK](./assets/img/android/rss-apk-dark.png#only-dark) ![APK Changes](./assets/img/android/rss-changes-light.png#only-light) ![APK Changes](./assets/img/android/rss-changes-dark.png#only-dark)

#### GitHub

在 GitHub，以 [Secure Camera](#secure-camera) 為例，可以導航到它的 [發布頁](https://github.com/GrapheneOS/Camera/releases) ，並在URL 最後加 `.atom`。

`https://github.com/GrapheneOS/Camera/releases.atom`

#### GitLab

在GitLab ，以 [Aurora Store](#aurora-store) 為例，可以導航到其 [專案存取庫](https://gitlab.com/AuroraOSS/AuroraStore) ，並在URL 最後加 `/-/tags?format=atom`。

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

#### 查驗 APK 指紋碼

如果想下載 APK 檔案進行手動安裝，可用 [`apksigner`](https://developer.android.com/studio/command-line/apksigner) 工具驗證其簽名，這是 Android [build-tools](https://developer.android.com/studio/releases/build-tools)的一部分。

1. 安裝 [Java JDK](https://oracle.com/java/technologies/downloads).

2. 下載 [Android Studio 命令列工具](https://developer.android.com/studio#command-tools).

3. 解壓縮下載的存檔:

    ```bash
    unzip commandlinetools-*.zip
    cd cmdline-tools
    ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
    ```

4. 執行簽名驗證指令:

    ```bash
    ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
    ```

5. 產生的雜湊結果可與另一個來源進行比對。 某些開發者例如 Signal 在會其官網顥示其[指紋碼](https://signal.org/android/apk)。

    ```bash
    Signer #1 certificate DN: CN=GrapheneOS
    Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
    Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
    Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
    ```

### F-Droid

![F-Droid 圖標](assets/img/android/f-droid.svg){ align=right width=120px }

==我們只建議用 F-Droid 來獲取無法在上述管道取得的應用程式。== F-Droid 經常被推薦為 Google Play 替代品，特別是隱私社區。 可添加第三方資源庫的選項與不被局限在 Google 圍牆花園，導致了它的流行。 F-Droid 另外還有 [可複制建構](https://f-droid.org/en/docs/Reproducible_Builds) ，用於一些應用程式，並致力於自由和開源軟體。 不過F-Droid 建置、簽署和交付包的方式存在一些安全缺失：

由於其構制應用程式的程序，F-Droid 官方資源庫中的應用程式經常在更新上落後。 F-Droid 維護者在用自己的密鑰簽署應用程式時也會重複使用套件 ID，此作法並不理想，因為這給予 F-Droid 團隊終極信任。 此外，應用程式納入官方 F-Droid 儲存庫中的要求不如 Google Play 等其他應用程式商店嚴格，這意味著 F-Droid 往往會託管更多較舊、未維護或不符合[現代安全標準](https://developer.android.com/google/play/requirements/target-sdk)的應用程式。

其他流行的 F-Droid 第三方資源庫，如 [IzzyOnDroid](https://apt.izzysoft.de/fdroid) ，緩解一些擔憂。 IzzyOnDroid 存儲庫直接從 GitHub 拉取構建，是開發者自己存儲庫的下一個最好的東西。 然而，這不是我們所推薦的，當應用程式進入 F-droid 主倉庫時，通常 [就會從該倉庫刪除](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446)。 雖然可以理解（因為該特定倉庫的作用是應用程式在為 F-Droid 主倉庫接受之前託管工作），它可能會讓所安裝的應用程式不再收到更新。

也就是說， [F-droid](https://f-droid.org/en/packages) 和 [IzzyOnDroid](https://apt.izzysoft.de/fdroid) 存取庫有無數應用程式，所以它們成為搜索和發現開源應用程式的有用工具，然後通過 Play Store、Aurora Store 或直接從開發者獲得 APK 下載。 透過此方法尋找新應用程式時，應該做出最佳判斷，並密切注意應用程式的更新頻率。 過時的應用程式可能依賴不支援的程式庫，從而帶來潛在的安全風險。

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

在某些罕見情況下，應用程式開發者將只通過 F-droid 發布（[Gadgetbridge](https://gadgetbridge.org)就是一例。) 如果真需要這樣的應用程式，建議使用 [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic/) ，而不是從官方的 F-droid 應用程式來獲得。 F-Droid Basic 可以進行無需特權或 root 的更新，且具降低的功能集（限制攻擊面）。

</div>

## 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 作業系統

- 必須是開源軟體。
- 必須支援 bootloader 鎖定與自定 AVB 密鑰支援。
- Android 主要系統發布後的 1個月內接受更新。
- 必须在发布后0-14天内收到安卓功能更新（小版本）。
- 必須在發布後 5 天內收到定期安全補丁。
- 必須 **不可打破常規地** root 。
- 必須**不要**預設啟用 Google Play 服務。
- 必須 **不用** 系統調配以支援 Google Play 服務。

### 裝置

- 必須支援至少一個我們推薦的自訂作業系統。
- 必須是目前可在商店買到的新品。
- 至少可獲得 5年的安全更新。
- 必須有專用的安全元件硬體。

### 應用程式

- 此頁面上的應用程式不得適用於網站上的任何其他軟體類別。
- 一般應用程式應擴展或取代核心系統功能。
- 應用程式應定期更新和維護。
