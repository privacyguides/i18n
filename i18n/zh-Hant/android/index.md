---
title: Android
description: Our advice for replacing privacy-invasive default Android features with private and secure alternatives.
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

[General Android Overview :material-arrow-right-drop-circle:](../os/android-overview.md){ .md-button .md-button--primary }

## 我們的建議

### Replace Google Services

There are many methods of obtaining apps on Android while avoiding Google Play. Whenever possible, try using one of these methods before getting your apps from non-private sources:

[Obtaining Applications :material-arrow-right-drop-circle:](obtaining-apps.md){ .md-button }

There are also many private alternatives to the apps that come pre-installed on your phone, such as the camera app. Besides the Android apps we recommend throughout this site in general, we've created a list of system utilities specific to Android which you might find useful.

[General App Recommendations :material-arrow-right-drop-circle:](general-apps.md){ .md-button }

### Install a Custom Distribution

購買 Android 手機時，該設備的預設作業系統通常綁入非 Android 開源專案的應用程式與服務，成為侵入性整合。 其中許多應用程式-- 甚至是提供基本系統功能的撥號器等應用程式-- 都需放到 Google Play 服務進行侵入式整合，且 Google Play 服務需要存取檔案、聯絡人儲存、通話記錄、簡訊、位置、攝影機、麥克風以及設備上的許多內容的權限，這樣基本系統程式和其他應用程式才能運行。 這些應用程式和服務增加了設備的攻擊面，成為 Android 各種隱私問題的來源。

This problem could be solved by using an alternative Android distribution, commonly known as a _custom ROM_, that does not come with such invasive integration. 不幸的是，許多自定義 Android 發行版常常違反 Android 安全模式，不支持重要的安全功能，如 AVB 、回滾保護、韌體更新等。 Some distributions also ship [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) builds which expose root via [ADB](https://developer.android.com/studio/command-line/adb) and require [more permissive](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug\&type=code) SELinux policies to accommodate debugging features, resulting in a further increased attack surface and weakened security model.

理想情況下，在選擇客製 Android 發行版時，應該確保它符合Android 安全模型。 At the very least, the distribution should have production builds, support for AVB, rollback protection, timely firmware and operating system updates, and SELinux in [enforcing mode](https://source.android.com/security/selinux/concepts#enforcement_levels). All of our recommended Android distributions satisfy these criteria:

[Recommended Distributions :material-arrow-right-drop-circle:](distributions.md){ .md-button }

### Avoid Root

[Rooting](https://en.wikipedia.org/wiki/Rooting_\(Android\)) Android phones can decrease security significantly as it weakens the complete [Android security model](https://en.wikipedia.org/wiki/Android_\(operating_system\)#Security_and_privacy). 如果有人利用降低的安全性來進行攻擊，這可能會降低隱私權。 常見的 root 方法涉及直接篡改開機分割區，以至於造成無法成功執行驗證啟動。 需要 root 的應用程式也會修改系統磁碟分割，這意味著驗證開機必須維持停用。 Having root exposed directly in the user interface also increases the attack surface of your device and may assist in [privilege escalation](https://en.wikipedia.org/wiki/Privilege_escalation) vulnerabilities and SELinux policy bypasses.

Content blockers which modify the [hosts file](https://en.wikipedia.org/wiki/Hosts_\(file\)) (AdAway) and firewalls (AFWall+) which require root access persistently are dangerous and should not be used. 它們也不是解決預期目的的正確方法。 For content blocking, we suggest encrypted [DNS](../dns.md) or content blocking functionality provided by a VPN instead. TrackerControl and AdAway in non-root mode will take up the VPN slot (by using a local loopback VPN), preventing you from using privacy enhancing services such as [Orbot](../tor.md#orbot) or a [real VPN provider](../vpn.md).

AFWall+ works based on the [packet filtering](https://en.wikipedia.org/wiki/Firewall_\(computing\)#Packet_filter) approach and may be bypassable in some situations.

我們不認為為了手機 root 所犧牲的安全性，值得讓人懷疑這些應用程式對隱私權的益處。

### Install Updates Regularly

It's important to not use an [end-of-life](https://endoflife.date/android) version of Android. 較新版本的 Android 不僅會收到作業系統的安全性更新，而且還會收到重要的隱私增強更新。

For example, [prior to Android 10](https://developer.android.com/about/versions/10/privacy/changes) any apps with the [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) permission could access sensitive and unique serial numbers of your phone such as [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), or your SIM card's [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity); whereas now they must be system apps to do so. 系統應用程式僅由 OEM 或 Android 發行版提供。

### Use Built-in Sharing Features

透過 Android 內建的分享功能，您可以避免給予許多應用程式存取媒體的權限。 許多應用程式都允許您與它「分享」檔案，以便上傳媒體。

例如，如果您要張貼一張圖片到 Discord，您可以開啟檔案管理員或圖庫，然後與 Discord 應用程式分享該圖片，而不是允許 Discord 完全存取您的媒體和相片。
