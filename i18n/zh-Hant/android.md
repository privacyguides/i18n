---
meta_title: "Android 推薦: GrapheneOS 與 DivestOS - Privacy Guides"
title: "安卓"
icon: 'simple/android'
description: Android 手機可考慮使用這些更為安全與尊重隱私的作業系統。
cover: android.png
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: 私密 Android 作業系統
    url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: 安卓
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://zh.wikipedia.org/wiki/Android_ (operating_system)
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://zh.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: Divest
    image: /assets/img/android/divestos.svg
    url: https://divestos.org/
    sameAs: https://zh.wikipedia.org/wiki/DivestOS
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
    sameAs: https://zh.wikipedia.org/wiki/Google_Pixel
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
    operatingSystem: 安卓
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Auditor
    applicationCategory: Utilities
    operatingSystem: 安卓
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: 安全相機
    applicationCategory: Utilities
    operatingSystem: 安卓
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: 安全的 PDF 檢視器
    applicationCategory: Utilities
    operatingSystem: 安卓
---

![Android 圖標](assets/img/android/android.svg){ align=right }

**安卓開源項目** 是一個由谷歌領導的開源移動操作系統，為世界上大多數移動設備提供動力。 大多數 Android 系統的手機都經過修改，包括侵入性整合與應用程式，如 Google Play 服務，所以使用無這類侵入性功能的 Android 系統版本取代手機原本預設的安裝，可改善行動設備上的隱私。

[:octicons-home-16:](https://source.android.com/){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/){ .card-link title="Source Code" }

這些是我們推薦 Android 作業系統、設備和應用程式，最大程度地提高行動設備的安全和隱私。 了解更多 Android 資訊：

[安卓概况 :material-arrow-right-drop-circle:](os/android-overview.md ""){.md-button}

## AOSP 衍生品

根據設備與這些作業系統的兼容性，列出偏好順序以安裝我們推薦的某款定制 Android 作業系統。

!!! 備註

    由於 OEM 停止支持，壽命終止的設備（如GrapheneOS或CalyxOS的 "延長支授 "設備）沒有完整的安全補丁（軔體更新）。 這些設備無論安裝何種軟體，都不能視為完全安全。

### GrapheneOS

!!! recommendation

    ![GrapheneOS logo](assets/img/android/grapheneos.svg#only-light){ align=right }
    ![GrapheneOS logo](assets/img/android/grapheneos-dark.svg#only-dark){ align=right }
    
    **GrapheneOS** 是隱私與安全的最佳選擇。
    
    GrapheneOS 提供額外的 [安全加固](https://en.wikipedia.org/wiki/Hardening_(computing)) 與隱私改善。 它有 [加固的記憶體分配器](https://github.com/GrapheneOS/hardened_malloc)、網路、感應許可與各類[安全功能](https://grapheneos.org/features). GrapheneOS 還帶有完整的軔體更新與已簽名的建置版本，因此完全支援 verified boot。
    
    [:octicons-home-16: Homepage](https://grapheneos.org/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentation}
    [:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

GrapheneOS 支援 [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), 它可以像其它普通應用一樣在沙盒中執行[Google Play 服務](https://en.wikipedia.org/wiki/Google_Play_Services) 。 這意味著您將可以利用大多數 Google Play 服務，如 [推送通知](https://firebase.google.com/docs/cloud-messaging/)，完全控制其權限和訪問，同時將其包含所選的特定 [工作設定檔](os/android-overview.md#work-profile) 或 [用戶設定檔](os/android-overview.md#user-profiles)。

Google Pixel 手機是目前唯一符合 GrapheneOS [硬體安全要求](https://grapheneos.org/faq#device-support)的設備。

[為何我們推薦 GrapheneOS 而非 CalyxOS :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/ ""){.md-button}

### DivestOS

!!! recommendation

    ![DivestOS logo](assets/img/android/divestos.svg){ align=right }
    
    **DivestOS** 是 [LineageOS](https://lineageos.org/)的分支。
    DivestOS 從 LineageOS 繼承了許多[支援的設備](https://divestos.org/index.php?page=devices&base=LineageOS)。 它具有簽名的建置，因此可在某些非 Pixel 設備上執行 [verified boot](https://source.android.com/security/verifiedboot)。
    
    [:octicons-home-16: Homepage](https://divestos.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://divested.dev/index.php?page=donate){ .card-link title=Contribute }

DivestOS 有自動內核弱點 ([CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [補丁](https://gitlab.com/divested-mobile/cve_checker)、更少的商業專用 blobs 與自定的 [hosts](https://divested.dev/index.php?page=dnsbl) 檔案。 其加固的 WebView, [Mulch](https://gitlab.com/divested-mobile/mulch)，能使 [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) 用在所有架構和 [網路狀態分區](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning)，且接收額外更新。 DivestOS 還包括來自GrapheneOS 內核補丁，並通過 [defconfig hardening](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758)，開啟所有可用的內核安全功能。 3.4 版之後更新的內核都包括全頁[淨化](https://lwn.net/Articles/334747/) ，所有 ~22 Clang 編譯的內核都啟用了 [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471)。

DivestOS 實現了一些最初為 GrapheneOS 開發的系統加固補丁。 DivestOS 16.0以上版本實現了 GrapheneOS [`網際網路`](https://developer.android.com/training/basics/network-ops/connecting) 和感應權限切換， [固化記憶體分配器](https://github.com/GrapheneOS/hardened_malloc)， [exec-spawning](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/#additional-hardening)， [JNI](https://en.wikipedia.org/wiki/Java_Native_Interface) [constification](https://en.wikipedia.org/wiki/Const_(computer_programming))，以及部分 [bionic](https://en.wikipedia.org/wiki/Bionic_(software)) 固化補丁集。 17.1 之後的 GrapheneOS 支援完整 [MAC 隨機化](https://en.wikipedia.org/wiki/MAC_address#Randomization) 選項， [`ptrace_scope`](https://www.kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) 控制，以及自動重啟/Wi-Fi/藍牙 [超時選項](https://grapheneos.org/features)。

DivestOS 以 F-Droid 為預設的應用下載服務。 通常我們建議避免使用 F-Droid，它有不少[安全問題](#f-droid)。 然而 DivestOS 這樣卻不可行，開發者透過 ([DivestOS 官方](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) 與 [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2))的 F-Droid 存取庫來更新他們的應用程式。 我們建議禁用官方 F-Droid 應用，並使用 [Neo Store](https://github.com/NeoApplications/Neo-Store/) ，啟用DivestOS 存取庫，以保持這些組件為最新。 至於其它應用，我們建議的獲取方式仍適用。

!!! 警告

    DivestOS 軔體更新 [status](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS)和品管依所支援的設備不同而異。 雖取決於設備的兼容性，我们仍推薦 GrapheneOS。 對其它設備，DivestOS 是不錯的選項。
    
    並非所有支援設備都可 verified boot，某些設備的表現較好。

## Android 設備

選購設備時，建議儘可能挑選較新的設備。 行動設備的軟體和軔體只支持時間有期限，因此購買新上市的設備可以盡可能地延長其支援壽命。

避免從電信行動營運商購置手機。 它們往往 **鎖定 bootloader** 也不支援 [OEM 解鎖](https://source.android.com/devices/bootloader/locking_unlocking)。 這類手機變體阻止安裝任何替代的 Android 發行版。

從網路市集購買二手手機必須要非常**小心**。 請檢查賣家的信譽 如果是失竊的設備，有可能被列為 [IMEI 黑名單](https://www.gsma.com/security/resources/imei-blacklisting/)。 前一位持有者的活動發生關係也將有風險。

對於 Android 設備與作業系統相容有一些提示:

- 不要購買已經達到或接近其支援壽命的設備，額外的軔體更新必須由製造商提供。
- 不要購買預裝 LineageOS 或/e/OS 或是無適當 [Verified Boot](https://source.android.com/security/verifiedboot) 支持和軔體更新的 Android 手機。 這些設備沒辦檢查是否曾遭篡改。
- 簡而言之，如果這裏沒列出某設備或 Android 發行版，都是有原因的。 請查看 [本站論壇 ](https://discuss.privacyguides.net/) 了解詳情!

### Google Pixel

Google Pixel 是**唯一** 推薦的手機。 由於對第三方作業系統的適當AVB 支持和 Google 定制的 [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) 安全晶片為安全元件，Pixel 硬體安全性比目前市場上其他 Android 設備強。

!!! recommendation

    ![ Google Pixel 6](assets/img/android/google-pixel.png){ align=right }
    
    眾所周知，** Google Pixel**設備具有良好安全性，支持[Verified Boot](https://source.android.com/security/verifiedboot)，即使安裝自定義作業系統時也是如此。
    
    從**Pixel 6**和**6 Pro**開始，Pixel 設備至少有 5年的安全更新保證，確保其使用壽命比其他競爭OEM 廠商 2-4年長得多。
    
    [:material-shopping: Store](https://store.google.com/category/phones){ .md-button .md-button--primary }

Titan M2 這類安全元件比大多數其他手機處理器的可信執行環境更為有限，因為Titan M2 只用於秘密存儲、硬體證明和速率限制，而不是用於運行 "可信 "程式。 沒有安全元件的手機必須使用 TEE *執行所有這些功能* ，從而導致更大的攻擊面。

Google Pixel 手機使用名為Trusty 的 TEE 作業系統，它是 [開源](https://source.android.com/security/trusty#whyTrusty)，與其他許多手機不同。

Pixel 手機很容易安裝 GrapheneOS 只需依其 [網頁安裝程式](https://grapheneos.org/install/web)即可。 如果不敢自行安裝願意多花一點錢，可以看看 [NitroPhone](https://shop.nitrokey.com/shop) ，它們預裝 GrapheneOS，來自著名的 [Nitrokey](https://www.nitrokey.com/about) 公司。

購買 Google Pixel 的一些提醒:

- 如果想買便宜的 Pixel 設備，建議購買"**a**"型號，其為旗艦機發布後的預算款。 通常會有折扣，因為 Google 會出清庫存。
- 考慮在實體商店提供折扣與特價的商品。
- 找找國內線上折扣社區的網站。 這些可提醒有好的商品。
- Google 提供一份其設備 [支援週期](https://support.google.com/nexus/answer/4457705)的列表清單。 設備每日價格可以計算為: $\text{Cost} \over \text {EOL Date}-\text{Current Date}$，意味著設備使用時間越長，每天的費用越低。

## 一般應用

我們在網站上推薦了各種各樣的 Android 應用。 這裡列出的應用程式是 Android 專用、特別加強或取代重要系統功能。

### Shelter

!!! recommendation

    ![Shelter logo](assets/img/android/shelter.svg){ align=right }
    
    **Shelter** 有助於利用 Android 工作設定檔功能隔離或複制設備上的應用程式。.
    
    Shelter 阻止聯繫人利用默認檔案管理器([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui))作跨設定檔搜尋與共享檔案 。
    
    [:octicons-repo-16: Repository](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
    [:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.patreon.com/PeterCxy){ .card-link title=Contribute }

!!! 警告

    推薦使用 Shelter 取代[Insular](https://secure-system.gitlab.io/Insular/)和 [Island](https://github.com/oasisfeng/island)，因為 Shelter 支持[聯繫人搜索屏蔽](https://secure-system.gitlab.io/Insular/faq.html)。
    
    當使用 Shelter 時，將信任置於其開發者，Shelter 作為[設備管理員](https://developer.android.com/guide/topics/admin/device-admin)來創建工作設定檔，它有大量權限訪問存儲在工作設定檔的資料。

### Auditor

!!! recommendation

    ![Auditor logo](assets/img/android/auditor.svg#only-light){ align=right }
    ![Auditor logo](assets/img/android/auditor-dark.svg#only-dark){ align=right }
    
    **Auditor** is an app which leverages hardware security features to provide device integrity monitoring by actively validating the identity of a device and the integrity of its operating system. Currently, it only works with GrapheneOS or the stock operating system for [supported devices](https://attestation.app/about#device-support).
    
    [:octicons-home-16: Homepage](https://attestation.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://attestation.app/about){ .card-link title=Documentation}
    [:octicons-code-16:](https://attestation.app/source){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://attestation.app/donate){ .card-link title=Contribute }
    
    ??? 下載
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

Auditor 通過下列方式鑑證和入侵檢測。

- Using a [Trust On First Use (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) model between an *auditor* and *auditee*, the pair establish a private key in the [hardware-backed keystore](https://source.android.com/security/keystore/) of the *Auditor*.
- The *auditor* can either be another instance of the Auditor app or the [Remote Attestation Service](https://attestation.app).
- The *auditor* records the current state and configuration of the *auditee*.
- 如果在配對完成後發生篡改 *審計對象的作業系統* ，審計人員將意識到設備狀態和配置的變化。
- 您會被提醒注意此一變化。

沒有個人識別資料被提交給證明服務。 建議使用匿名帳戶註冊，並啟用遠程認證，以進行持續監控。

如果您的 [威脅模型](basics/threat-modeling.md) 需要隱私，可以考慮使用 [Orbot](tor.md#orbot) 或VPN，從證明服務中隱藏 IP地址。 為了確保硬體和作業系統真實， [，在設備安裝後連上網際網路之前，立即進行本地認證](https://grapheneos.org/install/web#verifying-installation)。

### 安全相機

!!! recommendation

    ![Secure camera logo](assets/img/android/secure_camera.svg#only-light){ align=right }
    ![Secure camera logo](assets/img/android/secure_camera-dark.svg#only-dark){ align=right }
    
    **Secure Camera** is a camera app focused on privacy and security which can capture images, videos and QR codes. CameraX vendor extensions (Portrait, HDR, Night Sight, Face Retouch, and Auto) are also supported on available devices.
    
    [:octicons-repo-16: Repository](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
    [:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }
    
    ??? 下載
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

Main privacy features include:

- Auto removal of [Exif](https://en.wikipedia.org/wiki/Exif) metadata (enabled by default)
- Use of the new [Media](https://developer.android.com/training/data-storage/shared/media) API, therefore [storage permissions](https://developer.android.com/training/data-storage) are not required
- Microphone permission not required unless you want to record sound

!!! 備註

    Metadata is not currently deleted from video files but that is planned.
    
    The image orientation metadata is not deleted. If you enable location (in Secure Camera) that **won't** be deleted either. If you want to delete that later you will need to use an external app such as [ExifEraser](data-redaction.md#exiferaser).

### 安全的 PDF 檢視器

!!! recommendation

    ![Secure PDF Viewer logo](assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
    ![Secure PDF Viewer logo](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }
    
    **Secure PDF Viewer** is a PDF viewer based on [pdf.js](https://en.wikipedia.org/wiki/PDF.js) that doesn't require any permissions. The PDF is fed into a [sandboxed](https://en.wikipedia.org/wiki/Sandbox_(software_development)) [webview](https://developer.android.com/guide/webapps/webview). This means that it doesn't require permission directly to access content or files.
    
    [內容安全政策](https://en.wikipedia.org/wiki/Content_Security_Policy)用來強制要求 WebView 內的JavaScript 和造型屬性需全為靜態內容。
    
    [:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
    [:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }
    
    ??? 下載
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

## 獲取應用程式

### GrapheneOS App Store

GrapheneOS 應用商店可在 [GitHub](https://github.com/GrapheneOS/Apps/releases)找到。 It supports Android 12 and above and is capable of updating itself. The app store has standalone applications built by the GrapheneOS project such as the [Auditor](https://attestation.app/), [Camera](https://github.com/GrapheneOS/Camera), and [PDF Viewer](https://github.com/GrapheneOS/PdfViewer). If you are looking for these applications, we highly recommend that you get them from GrapheneOS's app store instead of the Play Store, as the apps on their store are signed by the GrapheneOS's project own signature that Google does not have access to.

### Aurora Store

Google Play商店需要登錄 Google 帳戶，這對隱私來說不是很好。 可以使用替代客戶端，如 Aurora Store 來解決這個問題。

!!! recommendation

    ![Aurora Store logo](assets/img/android/aurora-store.webp){ align=right }
    
    **Aurora Store** is a Google Play Store client which does not require a Google Account, Google Play Services, or microG to download apps.
    
    [:octicons-home-16: Homepage](https://auroraoss.com/){ .md-button .md-button--primary }
    [:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Source Code" }
    
    ??? 下載
    
        - [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

Aurora Store不允許其匿名帳戶下載付費應用程式。 You can optionally log in with your Google account with Aurora Store to download apps you have purchased, which does give access to the list of apps you've installed to Google, however you still benefit from not requiring the full Google Play client and Google Play Services or microG on your device.

### Manually with RSS Notifications

For apps that are released on platforms like GitHub and GitLab, you may be able to add an RSS feed to your [news aggregator](/news-aggregators) that will help you keep track of new releases.

![RSS APK](./assets/img/android/rss-apk-light.png#only-light) ![RSS APK](./assets/img/android/rss-apk-dark.png#only-dark) ![APK Changes](./assets/img/android/rss-changes-light.png#only-light) ![APK Changes](./assets/img/android/rss-changes-dark.png#only-dark)

#### GitHub

On GitHub, using [Secure Camera](#secure-camera) as an example, you would navigate to its [releases page](https://github.com/GrapheneOS/Camera/releases) and append `.atom` to the URL:

`https://github.com/GrapheneOS/Camera/releases.atom`

#### GitLab

On GitLab, using [Aurora Store](#aurora-store) as an example, you would navigate to its [project repository](https://gitlab.com/AuroraOSS/AuroraStore) and append `/-/tags?format=atom` to the URL:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

#### 查驗 APK 指紋碼

If you download APK files to install manually, you can verify their signature with the [`apksigner`](https://developer.android.com/studio/command-line/apksigner) tool, which is a part of Android [build-tools](https://developer.android.com/studio/releases/build-tools).

1. Install [Java JDK](https://www.oracle.com/java/technologies/downloads/).

2. Download the [Android Studio command line tools](https://developer.android.com/studio#command-tools).

3. Extract the downloaded archive:

    ```bash
    unzip commandlinetools-*.zip
    cd cmdline-tools
    ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
    ```

4. Run the signature verification command:

    ```bash
    ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
    ```

5. The resulting hashes can then be compared with another source. Some developers such as Signal [show the fingerprints](https://signal.org/android/apk/) on their website.

    ```bash
    Signer #1 certificate DN: CN=GrapheneOS
    Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
    Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
    Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
    ```

### F-Droid

![F-Droid 圖標](assets/img/android/f-droid.svg){ align=right width=120px }

==We do **not** currently recommend F-Droid as a way to obtain apps.== F-Droid is often recommended as an alternative to Google Play, particularly in the privacy community. The option to add third-party repositories and not be confined to Google's walled garden has led to its popularity. F-Droid 另外還有 [可複制建構](https://f-droid.org/en/docs/Reproducible_Builds/) ，用於一些應用程式，並致力於自由和開源軟體。 然而，官方F-Droid 有 [不少問題](https://privsec.dev/posts/android/f-droid-security-issues/)包括客戶端應用、 品質控制、建置方式、簽署和交付套件等等。

由於其構制應用程式的程序，F-Droid 官方資源庫中的應用程式經常在更新上落後。 F-Droid 維護者在用自己的密鑰簽署應用程式時也會重複使用套件 ID，此作法並不理想，因為這給予 F-Droid 團隊終極信任。

其他流行的第三方資源庫，如 [IzzyOnDroid](https://apt.izzysoft.de/fdroid/) ，緩解一些擔憂。 IzzyOnDroid 存儲庫直接從 GitHub 拉取構建，是開發者自己存儲庫的下一個最好的東西。 然而，這不是我們所推薦的，當應用程式進入 F-droid 主倉庫時，通常 [就會從該倉庫刪除](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446)。 雖然可以理解（因為該特定倉庫的作用是應用程式在為 F-Droid 主倉庫接受之前託管工作），它可能會讓所安裝的應用程式不再收到更新。

That said, the [F-Droid](https://f-droid.org/en/packages/) and [IzzyOnDroid](https://apt.izzysoft.de/fdroid/) repositories are home to countless apps, so they can be a useful tool to search for and discover open-source apps that you can then download through Play Store, Aurora Store, or by getting the APK directly from the developer. 重要的是要記住，這些資源庫裏一些應用程式已多年未更新，可能依賴於不支援的程式庫等，構成潛在的安全風險。 使用這種方法尋找新的應用程式時，應該善用最佳判斷。

!!! 備註

    在某些罕見情況下，應用程式開發者將只通過 F-droid 發布（[Gadgetbridge](https://gadgetbridge.org/)就是一例。) 如果真需要這樣的應用程式，建議使用 [Neo Store](https://github.com/NeoApplications/Neo-Store/)，而不是從官方的 F-droid 應用程式來獲得。

## 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

!!! 示例“此部分是新的”

    我們正在努力為我們網站的每個部分建立定義的標準，這可能會有所變化。 如果您對我們的標準有任何疑問，請在[論壇上提問] (https://discuss.privacyguides.net/latest) ，如果沒有列出，請不要認為我們在提出建議時沒有考慮到某些事情。 當我們推薦一個項目時，有許多因素被考慮和討論，記錄每一個項目都是正在進行式。

### 作業系統

- 必須是開源軟體。
- 必須支援 bootloader 鎖定與自定 AVB 密鑰支援。
- Android 主要系統發布後的 1個月內接受更新。
- Must receive Android feature updates (minor version) within 0-14 days of release.
- Must receive regular security patches within 0-5 days of release.
- Must **not** be "rooted" out of the box.
- Must **not** enable Google Play Services by default.
- Must **not** require system modification to support Google Play Services.

### 裝置

- 必須支援至少一個我們推薦的自訂作業系統。
- 必須是目前可在商店買到的新品。
- 至少可獲得 5年的安全更新。
- 必須有專用的安全元件硬體。

### 應用程式

- 此頁面上的應用程式不得適用於網站上的任何其他軟體類別。
- 一般應用程式應擴展或取代核心系統功能。
- 應用程式應定期更新和維護。
