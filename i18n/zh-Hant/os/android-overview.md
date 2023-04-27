---
title: Android 概述
icon: simple/android
description: Android是一個開源作業系統，具有強大的安全保護，使其成為手機的首選。
---

Android是一個安全的操作系統，具有強大的 [應用程式沙盒](https://source.android.com/security/app-sandbox)， [Verified Boot](https://source.android.com/security/verifiedboot) （AVB）和強大的 [許可](https://developer.android.com/guide/topics/permissions/overview) 控制系統。

## 選擇Android 發佈版本

當購買 Android 手機時，該設備的預設作業系統通常放入非 [Android 開源專案](https://source.android.com/)的應用程式與服務，成為侵入性整合。 例如， Google Play 服務擁有不可撤銷的權限，可存取您的檔案、聯絡人儲存空間、通話記錄、SMS訊息、位置、攝影機、麥克風、硬體識別碼等。 這些應用程式和服務增加了設備的攻擊面，成為 Android 各種隱私問題的來源。

這個問題可以通過使用自訂的 Android 發行版來解決，而這些發行版不會附帶這種侵入性整合。 不幸的是，許多自定義 Android 發行版常常違反 Android 安全模式，不支持重要的安全功能，如 AVB 、回滾保護、韌體更新等。 一些發行版還提供了 [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) 版本，這類版本可通過 [ ADB ](https://developer.android.com/studio/command-line/adb) 暴露了根目錄，且要求 [更寬鬆的](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) SELinux政策以適應調試，導致進一步增加攻擊面並削弱安全模型。

理想情況下，在選擇客製 Android 發行版時，應該確保它符合Android 安全模型。 至少，該發行版應該具有生產構建，支持AVB ，回滾保護，及時韌體和操作系統更新，以及SELinux [開啟模式](https://source.android.com/security/selinux/concepts#enforcement_levels)。 我們推薦的 Android 發行版都符合這些標準。

[Android 系統建議 :material-arrow-right-drop-circle:](../android.md ""){.md-button}

## 避免 Root

[Rooting](https://en.wikipedia.org/wiki/Rooting_(Android)) Android phones can decrease security significantly as it weakens the complete [Android security model](https://en.wikipedia.org/wiki/Android_(operating_system)#Security_and_privacy). 這可能會降低隱私，如果有一個漏洞被降低的安全性所輔助。 常見的 root 方法涉及直接篡改開機分割區，以至於造成無法成功執行Verified Boot。 需要 root 的應用程式也會修改系統分割區，這意味著 Verified Boot 必須維持停用。 直接在使用者介面中暴露 root 也會增加裝置的 [攻擊面](https://en.wikipedia.org/wiki/Attack_surface) ，助長 [特權升級](https://en.wikipedia.org/wiki/Privilege_escalation) 漏洞和 SELinux 政策繞過。

修改 [hosts file](https://en.wikipedia.org/wiki/Hosts_(file)) (AdAway)和永久需要root存取的防火牆(AFWall +)的Adblocker是危險的，不應該使用。 它們也不是解決其預期目的的正確方法。 對於廣告封鎖，建議採加密 [DNS](../dns.md) 或 [VPN](../vpn.md) 伺服器的封鎖解決方案。 RethinkDNS,  TrackerControl 和 AdAway 在非根模式下將佔用VPN 插槽（通過使用本地環回 VPN)，阻止您使用隱私增強服務，如 Orbot 或真正的 VPN 伺服器。

AFWall+ 基於 [封包過濾](https://en.wikipedia.org/wiki/Firewall_(computing)#Packet_filter) 的方法，在某些情況下可能繞過。

我們認為，不值得這些應用程序的可疑隱私利益而犧牲手機 root 的安全。

## 已驗證的啟動

[Verified Boot](https://source.android.com/security/verifiedboot) is an important part of the Android security model. 它可保護 [邪惡女僕](https://en.wikipedia.org/wiki/Evil_maid_attack) 、惡意軟件的持久性攻擊，確保安全性更新不會造成 [回滾保護降級](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection)。

Android 10 以上版本已從全磁碟加密轉向更靈活的 [檔案加密](https://source.android.com/security/encryption/file-based)。 您的資料使用獨特的加密金鑰加密，而作業系統檔案則未加密。

Verified Boot確保作業系統檔案的完整性，從而防止具有物理訪問權限的對手篡改或安裝裝惡意軟體。 在極少數情況下，惡意軟體能夠利用系統的其他部分並獲得更高的特權訪問權限， Verified Boot 將在重新啟動設備時防止並還原對系統分割區的更改。

不幸的是， OEM 只在其 Android 發行版上支持 Verified Boot。 只有少數OEM （例如Google ）支援在其裝置上自訂 AVB 金鑰註冊。 此外，某些 AOSP 衍生版本（如LineageOS或/e/OS ）甚至在對可接受第三方作業系統提供Verified Boot 硬體上不予支援。 建議在購買新設備 **前** 先了解支援情況。 不支援 Verified Boot 的AOSP衍生版本**不予推薦** 。

許多 OEM 也破壞了 Verified Boot，您必須在廠商行銷之餘認知到這點。 例如， Fairphone 3和4在預設情況下並不安全，因為 [股票引導裝載程式信任公開的AVB簽名密鑰](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11)。 This breaks verified boot on a stock Fairphone device, as the system will boot alternative Android operating systems such (such as /e/) [without any warning](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) about custom operating system usage.

## 韌體更新

韌體更新對於維護安全性至關重要，沒有它們，您的設備就無法安全。 OEM 與其合作夥伴簽訂了支援協議，在有限的支持期內提供封閉式元件。 詳情請參閱每月 [Android 安全公告](https://source.android.com/security/bulletin)。

由於手機的元件（例如處理器和無線電技術）依賴於閉源元件，因此更新必須由各自的製造商提供。 因此，您的購買裝置必須在有效的支援週期內。 [高通](https://www.qualcomm.com/news/releases/2020/12/16/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) 和 [三星](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox/) 設備支援年限為 4年，而較便宜產品的支援週期通常更短。 隨著 [Pixel 6](https://support.google.com/pixelphone/answer/4457705)的推出， Google 現在製造自己的 SoC ，他們將提供至少 5年的支持。

對於 OEM 供應商或市場經銷商不提供韌體更新的 EOL 裝置，SoC 製造商不再支援。 這意味著這些設備的安全問題將得不到解決。

例如， Fairphone 推銷其設備有 6年的支持。 然而， SoC （ Fairphone 4上的Qualcomm Snapdragon 750G ）的EOL日期要短得多。 這意味著，無論 Fairphone 是否繼續發布軟體安全更新， Qualcomm Fairphone 4 固件安全更新將於 2023年9月結束。

## Android 版本

重要的是不要使用 [結束生命周期](https://endoflife.date/android) 版本的Android。 較新版本的 Android 不僅會收到作業系統的安全性更新，而且還會收到重要的隱私增強更新。 For example, [prior to Android 10](https://developer.android.com/about/versions/10/privacy/changes), any apps with the [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) permission could access sensitive and unique serial numbers of your phone such as [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), your SIM card's [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity), whereas now they must be system apps to do so. 系統應用程式僅由 OEM 或 Android 發行版提供。

## Android權限

Android</a> 上的

權限可控制允許哪些應用程式作存取。 Google 定期在每個連續版本中對權限系統進行 [改進](https://developer.android.com/about/versions/11/privacy/permissions) 。 安裝的所有應用程式都是嚴格的 [沙盒](https://source.android.com/security/app-sandbox)，因此，沒必要安裝任何防毒應用程式。</p> 

最新版本Android 的智能手機將永遠比裝付費防毒軟體的舊智慧手機更安全。 最好不要為防毒軟件付費，省錢購買新的智慧手機，如Google Pixel。

Android 10:

- [範圍儲存空間](https://developer.android.com/about/versions/10/privacy/changes#scoped-storage) 可讓您更好地控制檔案，並可以限制 [存取外部儲存空間](https://developer.android.com/training/data-storage#permissions)。 應用程式可在外部存儲中具有特定目錄，可以在那裡存儲特定類型的媒體。
- 通過引入 `ACCESS_BACKGROUND_LOCATION` 權限，更緊密地訪問 [設備位置](https://developer.android.com/about/versions/10/privacy/changes#app-access-device-location) 。 這可以防止應用程式在未經用戶明確許可的情況下在後臺運行時訪問位置。

Android 11:

- [一次性權限](https://developer.android.com/about/versions/11/privacy/permissions#one-time) 允許您只授予應用程式單次權限。
- [自動重設權限](https://developer.android.com/about/versions/11/privacy/permissions#auto-reset)，可重設應用程式開啟時授予 [執行時權限](https://developer.android.com/guide/topics/permissions/overview#runtime) 。
- Granular permissions for accessing [phone number](https://developer.android.com/about/versions/11/privacy/permissions#phone-numbers) related features.

Android 12:

- 只授予 [近似位置](https://developer.android.com/about/versions/12/behavior-changes-12#approximate-location)的權限。
- Auto-reset of [hibernated apps](https://developer.android.com/about/versions/12/behavior-changes-12#app-hibernation).
- [Data access auditing](https://developer.android.com/about/versions/12/behavior-changes-12#data-access-auditing) which makes it easier to determine what part of an app is performing a specific type of data access.

Android 13:

- A permission for [nearby wifi access](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). The MAC addresses of nearby WiFi access points was a popular way for apps to track a user's location.
- More [granular media permissions](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions), meaning you can grant access to images, videos or audio files only.
- Background use of sensors now requires the [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission) permission.

An app may request a permission for a specific feature it has. For example, any app that can scan QR codes will require the camera permission. Some apps can request more permissions than they need.

[Exodus](https://exodus-privacy.eu.org/) can be useful when comparing apps that have similar purposes. If an app requires a lot of permissions and has a lot of advertising and analytics this is probably a bad sign. We recommend looking at the individual trackers and reading their descriptions rather than simply **counting the total** and assuming all items listed are equal.

!!! 警告

    If an app is mostly a web-based service, the tracking may occur on the server side. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest/) shows "no trackers" but certainly does track users' interests and behavior across the site. Apps may evade detection by not using standard code libraries produced by the advertising industry, though this is unlikely.
    

!!! 備註

    Privacy-friendly apps such as [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest/) may show some trackers such as [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49/). This library includes [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) which can provide [push notifications](https://en.wikipedia.org/wiki/Push_technology) in apps. This [is the case](https://fosstodon.org/@bitwarden/109636825700482007) with Bitwarden. That doesn't mean that Bitwarden is using all of the analytics features that are provided by Google Firebase Analytics.
    



## 媒體存取

Quite a few applications allows you to "share" a file with them for media upload. If you want to, for example, tweet a picture to Twitter, do not grant Twitter access to your "media and photos", because it will have access to all of your pictures then. Instead, go to your file manager (documentsUI), hold onto the picture, then share it with Twitter.



## User Profiles

Multiple user profiles can be found in **Settings** → **System** → **Multiple users** and are the simplest way to isolate in Android.

With user profiles, you can impose restrictions on a specific profile, such as: making calls, using SMS, or installing apps on the device. Each profile is encrypted using its own encryption key and cannot access the data of any other profiles. Even the device owner cannot view the data of other profiles without knowing their password. Multiple user profiles are a more secure method of isolation.



## Work Profile

[Work Profiles](https://support.google.com/work/android/answer/6191949) are another way to isolate individual apps and may be more convenient than separate user profiles.

A **device controller** app such as [Shelter](#recommended-apps) is required to create a Work Profile without an enterprise MDM, unless you're using a custom Android OS which includes one.

The work profile is dependent on a device controller to function. Features such as *File Shuttle* and *contact search blocking* or any kind of isolation features must be implemented by the controller. You must also fully trust the device controller app, as it has full access to your data inside of the work profile.

This method is generally less secure than a secondary user profile; however, it does allow you the convenience of running apps in both the work and personal profiles simultaneously.



## VPN Killswitch

Android 7以上版本支援VPN killswitch ，無需安裝第三方應用程式即可使用。 This feature can prevent leaks if the VPN is disconnected. It can be found in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.



## 全局切換

Modern Android devices have global toggles for disabling Bluetooth and location services. Android 12為相機和麥克風引入了切換功能。 不使用時，建議停用這些功能。 Apps cannot use disabled features (even if granted individual permission) until re-enabled.



## Google

If you are using a device with Google services, either your stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS, there are a number of additional changes you can make to improve your privacy. We still recommend avoiding Google services entirely, or limiting Google Play services to a specific user/work profile by combining a device controller like *Shelter* with GrapheneOS's Sandboxed Google Play.



### Advanced Protection Program

If you have a Google account we suggest enrolling in the [Advanced Protection Program](https://landing.google.com/advancedprotection/). It is available at no cost to anyone with two or more hardware security keys with [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) support.

The Advanced Protection Program provides enhanced threat monitoring and enables:

- Stricter two factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](https://en.wikipedia.org/wiki/OAuth)
- Only Google and verified third-party apps can access account data
- Scanning of incoming emails on Gmail accounts for [phishing](https://en.wikipedia.org/wiki/Phishing#Email_phishing) attempts
- Stricter [safe browser scanning](https://www.google.com/chrome/privacy/whitepaper.html#malware) with Google Chrome
- Stricter recovery process for accounts with lost credentials
  
  If you use non-sandboxed Google Play Services (common on stock operating systems), the Advanced Protection Program also comes with [additional benefits](https://support.google.com/accounts/answer/9764949?hl=en) such as:

- Not allowing app installation outside of the Google Play Store, the OS vendor's app store, or via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)

- Mandatory automatic device scanning with [Play Protect](https://support.google.com/googleplay/answer/2812853?hl=en#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- Warning you about unverified applications



### Google Play System Updates

In the past, Android security updates had to be shipped by the operating system vendor. Android has become more modular beginning with Android 10, and Google can push security updates for **some** system components via the privileged Play Services.

If you have an EOL device shipped with Android 10 or above and are unable to run any of our recommended operating systems on your device, you are likely going to be better off sticking with your OEM Android installation (as opposed to an operating system not listed here such as LineageOS or /e/ OS). This will allow you to receive **some** security fixes from Google, while not violating the Android security model by using an insecure Android derivative and increasing your attack surface. We would still recommend upgrading to a supported device as soon as possible.



### 廣告識別碼

All devices with Google Play Services installed automatically generate an [advertising ID](https://support.google.com/googleplay/android-developer/answer/6048248?hl=en) used for targeted advertising. Disable this feature to limit the data collected about you.

On Android distributions with [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), go to :gear: **Settings** → **Apps** → **Sandboxed Google Play** → **Google Settings** → **Ads**, and select *Delete advertising ID*.

On Android distributions with privileged Google Play Services (such as stock OSes), the setting may be in one of several locations. 查看

- :gear: **Settings** → **Google** → **Ads**
- :gear: **Settings** → **Privacy** → **Ads**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads*, this varies between OEM distributions of Android. If presented with the option to delete the advertising ID that is preferred. If not, then make sure to opt out and reset your advertising ID.



### SafetyNet and Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) and the [Play Integrity APIs](https://developer.android.com/google/play/integrity) are generally used for [banking apps](https://grapheneos.org/usage#banking-apps). Many banking apps will work fine in GrapheneOS with sandboxed Play services, however some non-financial apps have their own crude anti-tampering mechanisms which might fail. GrapheneOS passes the `basicIntegrity` check, but not the certification check `ctsProfileMatch`. Devices with Android 8 or later have hardware attestation support which cannot be bypassed without leaked keys or serious vulnerabilities.

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt-out if you don't want your credit rating and personal information shared with affiliate marketing services.
