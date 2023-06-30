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

[Rooting](https://en.wikipedia.org/wiki/Rooting_(Android)) 安卓手机会大大降低安全性，因为它削弱了完整的 [安卓安全模型](https://en.wikipedia.org/wiki/Android_(operating_system)#Security_and_privacy)。 這可能會降低隱私，如果有一個漏洞被降低的安全性所輔助。 常見的 root 方法涉及直接篡改開機分割區，以至於造成無法成功執行Verified Boot。 需要 root 的應用程式也會修改系統分割區，這意味著 Verified Boot 必須維持停用。 直接在使用者介面中暴露 root 也會增加裝置的 [攻擊面](https://en.wikipedia.org/wiki/Attack_surface) ，助長 [特權升級](https://en.wikipedia.org/wiki/Privilege_escalation) 漏洞和 SELinux 政策繞過。

修改 [hosts file](https://en.wikipedia.org/wiki/Hosts_(file)) (AdAway)和永久需要root存取的防火牆(AFWall +)的Adblocker是危險的，不應該使用。 它們也不是解決其預期目的的正確方法。 對於廣告封鎖，建議採加密 [DNS](../dns.md) 或 [VPN](../vpn.md) 伺服器的封鎖解決方案。 RethinkDNS,  TrackerControl 和 AdAway 在非根模式下將佔用VPN 插槽（通過使用本地環回 VPN)，阻止您使用隱私增強服務，如 Orbot 或真正的 VPN 伺服器。

AFWall+ 基於 [封包過濾](https://en.wikipedia.org/wiki/Firewall_(computing)#Packet_filter) 的方法，在某些情況下可能繞過。

我們認為，不值得這些應用程序的可疑隱私利益而犧牲手機 root 的安全。

## 已驗證的啟動

[ Verified Boot](https://source.android.com/security/verifiedboot) ，是 Android 安全模式的重要組成。 它可保護 [邪惡女僕](https://en.wikipedia.org/wiki/Evil_maid_attack) 、惡意軟件的持久性攻擊，確保安全性更新不會造成 [回滾保護降級](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection)。

Android 10 以上版本已從全磁碟加密轉向更靈活的 [檔案加密](https://source.android.com/security/encryption/file-based)。 您的資料使用獨特的加密金鑰加密，而作業系統檔案則未加密。

Verified Boot確保作業系統檔案的完整性，從而防止具有物理訪問權限的對手篡改或安裝裝惡意軟體。 在極少數情況下，惡意軟體能夠利用系統的其他部分並獲得更高的特權訪問權限， Verified Boot 將在重新啟動設備時防止並還原對系統分割區的更改。

不幸的是， OEM 只其庫存 Android 發行版上支持 Verified Boot。 只有少數OEM （例如Google ）支援在其裝置上自訂 AVB 金鑰註冊。 此外，某些 AOSP 衍生版本（如LineageOS或/e/OS ）甚至在對可接受第三方作業系統提供Verified Boot 硬體上不予支援。 建議在購買新設備 **前** 先了解支援情況。 不支援 Verified Boot 的AOSP衍生版本**不予推薦** 。

許多 OEM 也破壞了 Verified Boot，您必須在廠商行銷之餘認知到這點。 例如， Fairphone 3和4在預設情況下並不安全，因為 [股票引導裝載程式信任公開的AVB簽名密鑰](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11)。 這會在庫存 Fairphone 設備中斷 verified boot，因為系統將啟動替代 Android 作業系統（如/e/） [，而不對自定作業系統發出警告](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) 。

## 韌體更新

韌體更新對於維護安全性至關重要，沒有它們，您的設備就無法安全。 OEM 與其合作夥伴簽訂了支援協議，在有限的支持期內提供封閉式元件。 詳情請參閱每月 [Android 安全公告](https://source.android.com/security/bulletin)。

由於手機的元件（例如處理器和無線電技術）依賴於閉源元件，因此更新必須由各自的製造商提供。 因此，您的購買裝置必須在有效的支援週期內。 [高通](https://www.qualcomm.com/news/releases/2020/12/16/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) 和 [三星](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox/) 設備支援年限為 4年，而較便宜產品的支援週期通常更短。 隨著 [Pixel 6](https://support.google.com/pixelphone/answer/4457705)的推出， Google 現在製造自己的 SoC ，他們將提供至少 5年的支持。

對於 OEM 供應商或市場經銷商不提供韌體更新的 EOL 裝置，SoC 製造商不再支援。 這意味著這些設備的安全問題將得不到解決。

例如， Fairphone 推銷其設備有 6年的支持。 然而， SoC （ Fairphone 4上的Qualcomm Snapdragon 750G ）的EOL日期要短得多。 這意味著，無論 Fairphone 是否繼續發布軟體安全更新， Qualcomm Fairphone 4 固件安全更新將於 2023年9月結束。

## Android 版本

重要的是不要使用 [結束生命周期](https://endoflife.date/android) 版本的Android。 較新版本的 Android 不僅會收到作業系統的安全性更新，而且還會收到重要的隱私增強更新。 例如， [，Android 10 之前](https://developer.android.com/about/versions/10/privacy/changes)，任何具有 [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) 權限的應用程式都可存取手機敏感獨特的序列號，如 [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity)， [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier)，SIM卡的 [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity)，而現在則必須是系統應用程式才可以。 系統應用程式僅由 OEM 或 Android 發行版提供。

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
- 存取 [電話號碼](https://developer.android.com/about/versions/11/privacy/permissions#phone-numbers) 相關功能的細微權限。

Android 12:

- 只授予 [近似位置](https://developer.android.com/about/versions/12/behavior-changes-12#approximate-location)的權限。
- 休眠應用/a>的自動重置。</li> 
  
  - [資料存取稽核](https://developer.android.com/about/versions/12/behavior-changes-12#data-access-auditing) 更容易確定應用程式的哪一部分正在執行特定類型的資料存取。</ul> 

Android 13:

- 同意 [鄰近的 wifi 訪問](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). 附近 WiFi 接入點的 MAC地址是應用程式跟蹤用戶位置的常用方式。
- 更多 [細微媒體權限](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions)，這意味著您只能授予對圖像，視頻或音頻文件的存取權限。
- 傳感器的背景使用需要 [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission) 權限。

應用程式可能會要求獲得特定功能的許可。 例如，任何可以掃描二維碼的應用程式都需要相機權限。 有些應用程式可能會要求超過所需的權限。

[Exodus](https://exodus-privacy.eu.org/) 在比較具相似目的的應用程式時可能很有用。 如果某應用程式需要大量權限，並且有很多的廣告和分析，這可能是個壞跡象。 建議查看個別跟蹤器與閱讀其描述而不是只有**計算總數**把所列的項目一視同仁。

!!! warning "警告"

    如果應用程式主要是基於網頁的服務，則跟蹤可能發生在伺服器端。 [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest/)顯示「無追蹤器」，但確實會追蹤使用者在網站上的興趣和行為。 應用程式也許無需廣告業的標準代碼庫來逃避檢測，儘管這不太可能。
    

!!! note "備註"

    [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest/)等隱私友好型應用程式可能會顯示[Google Firebase Analytics] (https://reports.exodus-privacy.eu.org/en/trackers/49/)等追蹤程式。 此程式庫包括[Firebase Cloud Messaging] (https://zh.wikipedia.org/wiki/Firebase_Cloud_Messaging) ，可以在應用程式中提供[推送通知] (https://zh.wikipedia.org/wiki/Push_technology)。 這是Bitwarden的[情況] (https://fosstodon.org/ @ bitwarden/109636825700482007)。 這並不意味 Bitwarden 使用 Google Firebase Analytics 提供的所有分析功能。
    



## 媒體存取

相當多的應用程式讓您須以他們"“共享”"以便上傳媒體檔案。 例如，如果想在Twitter 發佈圖片，請不要授予Twitter 訪問您的“媒體和照片”的權限，因為它將可以訪問您所有圖片。 相反，請前往您的檔案管理器（ documentsUI ） ，按住圖片，然後與Twitter分享。



## 用戶設定檔

多重用戶設定可以在 **設置** → **系統** → **多個用戶** 中找到，是 Android 最簡單的隔離方式。

透過使用者設定檔，可對特定使用者施加限制，例如：打電話、使用簡訊或在裝置上安裝應用程式。 每個用戶設定檔皆使用個自密鑰加密，無法訪問設置上其它用戶的任何資料。 即使是裝置擁有者也無法在不知道用戶密碼的情況下查看其他身份的資料。 多用戶配置設定是一種更安全的隔離方法。



## 工作用設定檔

[工作用設定檔](https://support.google.com/work/android/answer/6191949) 是另一個隔離個別應用的方法，也比單獨的用戶設定檔更為方便。

**設備控制器**應用例如 [Shelter](../android.md#shelter) 需要建立不用企業 行動裝置管理(MDM) 工作設定檔，除非使用自定的Android 作業系統已包括。

工作配置檔需靠裝置控制器才能運作。 控制器必須實現 *File Shuttle* 和 *Contact Search Blocking* 等功能或任何類型的隔離功能。 您還必須完全信任設備控制器應用程序，因為它可以完全訪問工作配置文件中的數據。

此方法通常不如次要用戶配置檔安全，然而它確實允許您在工作和個人配置檔之間同時執行應用程式。



## VPN Killswitch

Android 7以上版本支援VPN killswitch ，無需安裝第三方應用程式即可使用。 此功能可以防止VPN中斷連線時的洩漏。 它可以在 :gear: **設置** → **網路 & 網際網路** → **VPN** → :gear: → **區塊連接沒有 VPN**中找到。



## 全局切換

現代 Android 裝置具有全局切換功能，可停用藍牙和定位服務。 Android 12為相機和麥克風引入了切換功能。 不使用時，建議停用這些功能。 在重新啟用之前，應用程式無法使用已停用的功能（即使授予個別權限）。



## Google

如果您使用的裝置搭載Google服務，無論是您庫存作業系統，還是能夠安全地使用 Google Play服務（如GrapheneOS ）的作業系統，可進行許多其他變更以改善隱私。 我們仍然建議避免使用 Google 服務，或者將 *Shelter* 等設備控制器與 GrapheneOS 的Sandboxed Google Play相結合，將 Google Play 服務限制為特定用戶/工作檔案。



### 進階保護計劃

如果有 Google 帳戶，建議註冊 [進階保護計劃](https://landing.google.com/advancedprotection/)。 任何擁有兩個或多個硬體安全金鑰且支援 [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) 都可免費使用。

進階防護計劃提供強化的威脅監控，並能夠：

- 更嚴格的雙因素驗證；例如 **必須**使用 [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) ，禁用 [SMS OTP](../basics/multi-factor-authentication.md#sms-or-email-mfa)， [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) 和 [OAuth](https://en.wikipedia.org/wiki/OAuth)
- 只有Google 和經過驗證的第三方應用程式才能存取帳戶資料
- 掃描Gmail帳戶上的傳入電子郵件進行 [次網絡釣魚](https://en.wikipedia.org/wiki/Phishing#Email_phishing) 次嘗試
- 使用 Google Chrome 進行更嚴格的 [安全瀏覽器掃描](https://www.google.com/chrome/privacy/whitepaper.html#malware)
- 丟失憑的證帳戶予以更嚴格的恢復程序
  
  如果您使用非沙盒 Google Play 服務（在庫存作業系統上很常見） ，進階保護計劃還附帶 [額外優惠](https://support.google.com/accounts/answer/9764949?hl=en) ，例如：

- 不允許在Google Play 商店、作業系統供應商的應用程式商店之外安裝應用程式，或透過 [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)安裝應用程式

- 強制自動裝置掃描與 [播放保護](https://support.google.com/googleplay/answer/2812853?hl=en#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- 警告您未經驗證的應用程式



### Google Play 系统更新

過去， Android 安全更新必須由作業系統供應商提供。 從 Android 10 開始， Android 變得更模組化， Google 可以通過特權 Play 服務推送 **約** 系統組件的安全更新。

如果您的 EOL 裝置隨附 Android 10 以上高版本，無法執行我們推薦的任何作業系統，那麼您最好還是更維持在 OEM Android 版本（而不是此處未列出的作業系統，如LineageOS 或 /e/OS）。 這將允許您從 Google 獲得 **一些** 安全修復，不會因為使用不安全衍生產品而違反 Android 安全模式增加攻擊面。 我們仍建議您盡快升級至支援的裝置。



### 廣告識別碼

所有安裝 Google Play 服務的裝置都會自動產生 [廣告ID](https://support.google.com/googleplay/android-developer/answer/6048248?hl=en) ，用於定向廣告。 禁用此功能以限制其收集您的資料。

在具有 [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play)的Android 版上，前往 :gear: **設定** → **應用程式** → **Sandboxed Google Play** → **Google 設定** → **廣告**，然後選擇 *刪除廣告ID*。

在具有特權Google Play服務的Android發行版（如 庫存 OSes）上，設置可能在幾個位置。 查看

- :gear: **設定** → **Google** → **廣告**
- :gear: **設定** → **私隱** → **廣告**

可選擇刪除您的廣告ID 或 *選擇退出基於興趣的廣告*，這視 Android OEM 而異。 如果提供刪除首選廣告ID的選項。 如果沒有，請確保選擇退出並重設您的廣告ID。



### SafetyNet 和 Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) 和 [Play Integrity API](https://developer.android.com/google/play/integrity) 通常用於 [銀行應用程式](https://grapheneos.org/usage#banking-apps)。 許多銀行應用程式在 GrapheneOS 使用沙盒Play服務可以正常運作，但一些非金融應用程式有自己的防篡改機制，這可能會失敗。 GrapheneOS 通過了 `basicIntegrity` 檢查，但沒有`ctsProfileMatch` 證明檢查。 Android 8 以上版本的裝置支援硬體認證，如果沒有洩漏金鑰或嚴重漏洞，則無法繞過。

至於 Google 錢包，我們不建議您這樣做，因為他們的 [隱私政策](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en)規定，如果您不想與結盟行銷服務共享您的信用評級和個人信息，必須選擇退出。
