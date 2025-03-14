---
title: Android
description: 我們建議您使用隱私且安全的替代方案來取代侵犯隱私的預設 Android 功能。
icon: simple/android
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": 網頁
    name: Android 建議
    url: ./
  - "@context": http://schema.org
    "@type": CreativeWork
    name: Android
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://zh.wikipedia.org/wiki/Android
---

![Android logo](../assets/img/android/android.svg){ align=right }

**Android 開源專案** （AOSP）是一個由 Google 領導的開源行動裝置作業系統，為世界上大多數行動裝置提供支援。 大多數搭載 Android 的手機都經過修改，包含侵入性整合和應用程式（例如：Google Play 服務），您可以透過把手機預設安裝的 Android 版本 替換為不含這些侵入性功能的 Android 版本 ，這將顯著改善行動裝置上的隱私。

[Android 概述 :material-arrow-right-drop-circle:](../os/android-overview.md){ .md-button .md-button--primary }

## 我們的建議

### 避免 Google 服務

有許多方法可以在 Android 上取得應用程式，同時避開 Google Play 。 只要有可能，在從非私人來源取得您的應用程式之前，請嘗試使用其中一種方法：

[應用程式獲取途徑 :material-arrow-right-drop-circle:](obtaining-apps.md){ .md-button }

除了手機預先安裝的應用程式之外，還有許多更具隱私性的替代品，例如相機應用程式。 除了本網站推薦的一般 Android 應用程式之外，我們也建立了一份 Android 專用的系統級程式清單，您可能會發現這些程式很有用。

[常規應用程式 :material-arrow-right-drop-circle:](general-apps.md){ .md-button }

### 安裝自訂發行版

購買 Android 手機時，該設備的預設作業系統通常綁入非 Android 開源專案的應用程式與服務，成為侵入性整合。 其中許多應用程式-- 甚至是提供基本系統功能的撥號器等應用程式-- 都需放到 Google Play 服務進行侵入式整合，且 Google Play 服務需要存取檔案、聯絡人儲存、通話記錄、簡訊、位置、攝影機、麥克風以及設備上的許多內容的權限，這樣基本系統程式和其他應用程式才能運行。 這些應用程式和服務增加了設備的攻擊面，成為 Android 各種隱私問題的來源。

這個問題可以透過使用另一種 Android 發行版（通常稱為 _客製化 ROM_）來解決，這種套件不會有這種入侵性的整合。 不幸的是，許多自定義 Android 發行版常常違反 Android 安全模型，不支援重要的安全功能，如 AVB 、回滾保護、韌體更新等。 有些發行版提供 [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) 版本的構建，這種版本可透過 [ADB](https://developer.android.com/studio/command-line/adb) 暴露 root，並需要 更寬鬆的 SELinux 政策以允許除錯功能，這會進一步增加攻擊面和削弱安全模型。

理想情況下，在選擇客製 Android 發行版時，應該確保它符合Android 安全模型。 至少，該發行版應該具有生產構建，支援 AVB ，回滾保護，及時韌體和作業系統更新，以及SELinux [強制模式](https://source.android.com/security/selinux/concepts#enforcement_levels) 。 我們推薦的所有 Android 發行版都符合這些標準：

[建議的發行版 :material-arrow-right-drop-circle:](distributions.md){ .md-button }

### 避免 Root

[Rooting](https://zh.wikipedia.org/zh-tw/Root_%28Android%29) Android 手機會大幅降低安全性，因為它會削弱完整的 [Android 安全模型](https://en.wikipedia.org/wiki/Android_\(operating_system\)#Security_and_privacy) 。 如果有人利用降低的安全性來進行攻擊，這可能會威脅到您的隱私。 常見的 root 方法涉及直接篡改開機分割區，以至於造成無法成功執行驗證啟動。 需要 root 的應用程式也會修改系統磁碟分割，這意味著 Verified Boot 必須維持停用。 在使用者介面中直接暴露 root 也會增加裝置的攻擊面，並可能有助於 [特權提升](https://zh.wikipedia.org/zh-tw/%E7%89%B9%E6%9D%83%E6%8F%90%E5%8D%87) 漏洞和繞過 SELinux 政策。

修改 [hosts 檔案](https://zh.wikipedia.org/zh-tw/Hosts%E6%96%87%E4%BB%B6) （AdAway） 的內容封鎖程式，以及需要 root 存取權限的防火牆 (AFWall+) 都很危險，不應該使用。 它們也不是解決預期目的的正確方法。 對於內容阻擋，我們建議使用加密 [DNS](../dns.md) ，或改用 VPN 提供的內容封鎖功能。 TrackerControl 和 AdAway 在非 root 模式下會佔用 VPN 插槽（透過使用本機環回 VPN），使您無法使用 [Orbot](../tor.md#orbot) 或 [VPN](../vpn.md) 等增強隱私的服務。

AFWall+ 以 [封包過濾](https://en.wikipedia.org/wiki/Firewall_\(computing\)#Packet_filter) 方式運作，在某些情況下可能會被繞過。

我們不認為為了手機 root 所犧牲的安全性，值得讓人懷疑這些應用程式對隱私權的益處。

### 定期安裝更新

重要的是，不要使用 [產品壽命結束](https://endoflife.date/android) 版本的 Android。 較新版本的 Android 不僅會收到作業系統的安全性更新，而且還會收到重要的隱私增強更新。

舉例來說， [在 Android 10 之前](https://developer.android.com/about/versions/10/privacy/changes) 任何具有 [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) 權限的應用程式都可以存取手機敏感且獨特的序號，例如 [IMEI](https://zh.wikipedia.org/wiki/%E5%9B%BD%E9%99%85%E7%A7%BB%E5%8A%A8%E8%AE%BE%E5%A4%87%E8%AF%86%E5%88%AB%E7%A0%81) 、 [MEID](https://zh.wikipedia.org/wiki/%E7%A7%BB%E5%8A%A8%E8%AE%BE%E5%A4%87%E8%AF%86%E5%88%AB%E7%A0%81) 或 SIM 卡的 [IMSI](https://zh.wikipedia.org/wiki/%E5%9B%BD%E9%99%85%E7%A7%BB%E5%8A%A8%E7%94%A8%E6%88%B7%E8%AF%86%E5%88%AB%E7%A0%81) ；而現在則必須是系統應用程式才能這麼做。 而系統應用程式僅由 OEM 或 Android 發行版提供。

### 使用內建的分享功能

透過 Android 內建的分享功能，您可以避免給予許多應用程式存取媒體的權限。 許多應用程式都允許您與它「分享」檔案，以便上傳媒體。

例如，如果您要張貼一張圖片到 Discord，您可以開啟檔案管理員或圖庫，然後與 Discord 應用程式分享該圖片，而不是允許 Discord 完全存取您的媒體和相片。
