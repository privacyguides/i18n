---
title: Android 概述
icon: simple/android
description: Android是一個開源作業系統，具有強大的安全保護，使其成為手機的首選。
robots: nofollow, max-snippet:-1, max-image-preview:large
---

![Android 圖標](../assets/img/android/android.svg){ align=right }

**Android 開源專案** 為安全移動作業系統，提供[應用沙盒](https://source.android.com/security/app-sandbox), [驗證開機](https://source.android.com/security/verifiedboot) (AVB) 以及強韌的 [授權](https://developer.android.com/guide/topics/permissions/overview)控制系統。

## 我們的建議

### 選擇 Android 發佈版本

購買 Android 手機時，該設備的預設作業系統通常綁入非 Android 開源專案的應用程式與服務，成為侵入性整合。 其中許多應用程式-- 甚至是提供基本系統功能的撥號器等應用程式-- 都需放到 Google Play 服務進行侵入式整合，且 Google Play 服務需要存取檔案、聯絡人儲存、通話記錄、簡訊、位置、攝影機、麥克風以及設備上的許多內容的權限，這樣基本系統程式和其他應用程式才能運行。 這些應用程式和服務增加了設備的攻擊面，成為 Android 各種隱私問題的來源。

這個問題可以通過使用自訂的 Android 發行版來解決，而這些發行版不會附帶這種侵入性整合。 不幸的是，許多自定義 Android 發行版常常違反 Android 安全模式，不支持重要的安全功能，如 AVB 、回滾保護、韌體更新等。 一些發行版還提供了 [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) 版本，這類版本可通過 [ ADB ](https://developer.android.com/studio/command-line/adb) 暴露了根目錄，且要求 [更寬鬆的](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) SELinux政策以適應調試，導致進一步增加攻擊面並削弱安全模型。

理想情況下，在選擇客製 Android 發行版時，應該確保它符合Android 安全模型。 至少，該發行版應該具有生產構建，支持AVB ，回滾保護，及時韌體和操作系統更新，以及SELinux [開啟模式](https://source.android.com/security/selinux/concepts#enforcement_levels)。 我們推薦的 Android 發行版都符合這些標準。

[Android 系統建議 :material-arrow-right-drop-circle:](../android/distributions.md ""){.md-button}

### 避免 Root

去 [root](https://en.wikipedia.org/wiki/Rooting_(Android)) Android 手機會大幅降低安全性，因為它會削弱完整的[Android 安全模型](https://en.wikipedia.org/wiki/Android_(operating_system)#Security_and_privacy)。 如果有人利用降低的安全性來進行攻擊，這可能會降低隱私權。 常見的 root 方法涉及直接篡改開機分割區，以至於造成無法成功執行驗證啟動。 需要 root 的應用程式也會修改系統磁碟分割，這意味著驗證開機必須維持停用。 直接在使用者介面中暴露 root 也會增加裝置的[攻擊面](https://en.wikipedia.org/wiki/Attack_surface) ，並可能有助於[特權升級](https://en.wikipedia.org/wiki/Privilege_escalation)漏洞和 SELinux 政策繞過。

修改 [hosts 檔案](https://en.wikipedia.org/wiki/Hosts_(file))的內容封鎖程式 (AdAway) 和需要 root 存取權限的防火牆 (AFWall+) 都很危險，不應該使用。 它們也不是解決預期目的的正確方法。 若要封鎖內容，我們建議改用 VPN 提供的加密 [DNS](../dns.md) 或內容封鎖功能。 TrackerControl 和 AdAway 在非 root 模式下會佔用 VPN 插槽（透過使用本機迴路 VPN），使您無法使用 [Orbot](../tor.md#orbot) 或[真正 VPN 供應商](../vpn.md)等增強隱私的服務。

AFWall+ 基於 [封包過濾](https://en.wikipedia.org/wiki/Firewall_(computing)#Packet_filter) 的方法，在某些情況下可能繞過。

我們不認為為了手機 root 所犧牲的安全性，值得讓人懷疑這些應用程式對隱私權的益處。

### 安裝更新

重要的是，不要使用[生命週期結束的](https://endoflife.date/android) Android 版本。 較新版本的 Android 不僅會收到作業系統的安全性更新，而且還會收到重要的隱私增強更新。

舉例來說，[在 Android 10 之前](https://developer.android.com/about/versions/10/privacy/changes)，任何具有 [`read_phone_state`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) 權限的任何應用程式都可以存取手機敏感且獨特的序號，例如 [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity)、[MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier) 或 SIM 卡的 [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity)；而現在則必須是系統應用程式才能這麼做。 系統應用程式僅由 OEM 或 Android 發行版提供。

### 共享的媒體

透過 Android 內建的分享功能，您可以避免給予許多應用程式存取媒體的權限。 許多應用程式都允許您與它「分享」檔案，以便上傳媒體。

例如，如果您要張貼一張圖片到 Discord，您可以開啟檔案管理員或圖庫，然後與 Discord 應用程式分享該圖片，而不是允許 Discord 完全存取您的媒體和相片。

## 安全防護

Android 安全模型的關鍵元件包括[驗證啟動](#verified-boot)、[韌體更新](#firmware-updates)和強大的[權限系統](#android-permissions)。 這些重要的安全功能構成我們的[行動電話](../mobile-phones.md)和[客製 Android 作業系統](../android/distributions.md)建議最低標準的底線。

### 驗證啟動

[**驗證啟動**](https://source.android.com/security/verifiedboot)是 Android 安全模型的重要部分。 它提供防範[惡意內部人員攻擊](https://en.wikipedia.org/wiki/Evil_maid_attack)和惡意軟體持續感染的保護，並透過[回滾保護](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection)確保安全更新無法降級。

Android 10 及以上版本已從全磁碟加密轉變為更靈活的[基於文件的加密](https://source.android.com/security/encryption/file-based)。 您的資料使用獨特的加密金鑰加密，而作業系統檔案則未加密。

驗證啟動可確保作業系統檔案的完整性，從而防止擁有實體存取權限的壞人篡改或在裝置上安裝惡意軟體。 萬一惡意軟體能夠利用系統的其他部分並取得更高的權限存取權，驗證啟動會在重新開機裝置時防止並還原對系統磁碟分割的變更。

不幸的是，OEM （手機代工廠商）僅有義務在其 Android 發行版上支援驗證啟動。 只有 Google 等少數 OEM 廠商的裝置支援自訂 AVB 金鑰註冊。 此外，某些 AOSP 衍生程式 (例如 LineageOS 或 /e/ OS) 不支援驗證啟動，即使在支援第三方作業系統的驗證開機硬體上也是如此。 我們建議您在購買新裝置**之前**先檢查是否有支援。 **不建議**使用不支援驗證開機的 AOSP 衍生版本。

許多 OEM 也破壞了 Verified Boot，您必須在廠商行銷之餘認知到這點。 舉例來說，Fairphone 3 和 4 預設是不安全的，因為[原廠開機載入程式信任公開 AVB 簽署金鑰](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11)。 這會破壞原廠 Fairphone 裝置上的驗證開機，因為系統將會開機其他 Android 作業系統 (例如 /e/)，而不會對客製作業系統的使用發出[任何警告](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust)。

### 韌體更新

**韌體更新**對維護安全性至關重要，沒有韌體更新，您的裝置就不可能安全。 OEM 與合作夥伴簽訂支援協議，在有限的支援期限內提供封閉原始碼元件。 詳情請參閱每月 [Android 安全公告](https://source.android.com/security/bulletin)。

由於手機的元件（例如處理器和無線電技術）依賴於閉源元件，因此更新必須由各自的製造商提供。 因此，您的購買裝置必須在有效的支援週期內。 [高通](https://www.qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and)和[三星](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox)為其裝置提供 4 年的支援，而較便宜的產品通常支援週期較短。 隨著 [Pixel 6](https://support.google.com/pixelphone/answer/4457705) 的推出，Google 現在自家製造 SoC，而且他們會提供至少 5 年的支援。 隨著 Pixel 8 系列的推出，Google 將支援期限延長至 7 年。

不再受 SoC 製造商支援的 EOL （產品生命週期結束）裝置無法從 OEM 供應商或 Android 售後市場經銷商取得韌體更新。 這表示這些裝置的安全問題仍未修正。

例如，Fairphone 宣傳其 Fairphone 4 裝置可獲得 6 年的支援。 然而，SoC（Fairphone 4 採用的高通 Snapdragon 750G）的停產日期則短得多。 這意味著，無論 Fairphone 是否繼續釋出軟體安全更新，高通針對 Fairphone 4 的韌體安全更新將於 2023 年 9 月終止。

### Android 權限

[**Android 上的權限**](https://developer.android.com/guide/topics/permissions/overview)允許您控制哪些應用程式可以存取。 Google 會定期在每個版本中[改善](https://developer.android.com/about/versions/11/privacy/permissions)權限系統。 您安裝的所有應用程式都經過嚴格[的沙箱處理](https://source.android.com/security/app-sandbox)，因此不需要安裝任何防毒應用程式。

配備最新版 Android 的智慧型手機永遠比配備已付費購買的防毒軟體的舊智慧型手機更安全。 最好不要花錢購買防毒軟體，省下來的錢可以買一部新的智慧型手機，例如[Google Pixel](../mobile-phones.md#google-pixel)。

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

- 同意 [鄰近的 Wi-Fi 存取](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). 附近 Wi-Fi 接入點的 MAC地址是應用程式跟蹤用戶位置的常用方式。
- 更多 [細微媒體權限](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions)，這意味著您只能授予對圖像，視頻或音頻文件的存取權限。
- 傳感器的背景使用需要 [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission) 權限。

應用程式可能會要求獲得特定功能的許可。 例如，任何可以掃描二維碼的應用程式都需要相機權限。 有些應用程式可能會要求超過所需的權限。

[Exodus](https://exodus-privacy.eu.org) 在比較具相似目的的應用程式時可能很有用。 如果某應用程式需要大量權限，並且有很多的廣告和分析，這可能是個壞跡象。 建議查看個別跟蹤器與閱讀其描述而不是只有**計算總數**把所列的項目一視同仁。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

如果應用程式主要是基於網頁的服務，則跟蹤可能發生在伺服器端。 [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest/)顯示「無追蹤器」，但確實會追蹤使用者在網站上的興趣和行為。 應用程式也許無需廣告業的標準代碼庫來逃避檢測，儘管這不太可能。

</div>

<div class="admonition note" markdown>
<p class="admonition-title">備註</p>

[Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest/)等隱私友好型應用程式可能會顯示 [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49/)等追蹤程式。 此程式庫包括 [Firebase Cloud Messaging](https://zh.wikipedia.org/wiki/Firebase_Cloud_Messaging) ，可以在應用程式中提供 [推送通知](https://zh.wikipedia.org/wiki/Push_technology)。 這是Bitwarden的 [情況](https://fosstodon.org/ @ bitwarden/109636825700482007)。 這並不意味 Bitwarden 使用 Google Firebase Analytics 提供的所有分析功能。

</div>

## 隱私功能



### 用戶設定檔

多重使用者設定檔可在 **設定** → **系統** → **多重使用者** 中找到，是 Android 中最簡單的隔離方式。

透過使用者設定檔，可對特定使用者施加限制，例如：打電話、使用簡訊或在裝置上安裝應用程式。 每個用戶設定檔皆使用個自密鑰加密，無法訪問設置上其它用戶的任何資料。 即使是裝置擁有者也無法在不知道用戶密碼的情況下查看其他身份的資料。 多用戶配置設定是一種更安全的隔離方法。



### 工作用設定檔

[工作用設定檔](https://support.google.com/work/android/answer/6191949) 是另一個隔離個別應用的方法，也比單獨的用戶設定檔更為方便。

在沒有企業 MDM 的情況下，必須使用 [Shelter](../android/general-apps.md#shelter) 等**裝置控制器**應用程式才能建立工作設定檔，除非您使用的是包含企業 MDM 的自訂 Android 作業系統。

工作設定檔依賴裝置控制器才能運作。 *檔案穿梭*、*連絡人搜尋封鎖*等功能或任何種類的隔離功能都必須由控制器執行。 您也必須完全信任裝置控制器應用程式，因為它可以完全存取您在工作設定檔內的資料。

此方法的安全性通常比第二使用者設定檔低，但卻可讓您同時在工作和個人設定檔中執行應用程式，非常方便。



### VPN Killswitch

Android 7 及以上版本支援 VPN kill switch，無需安裝第三方應用程式即可使用。 此功能可以防止VPN中斷連線時的洩漏。 它可以在 :gear: **設置** → **網路 & 網際網路** → **VPN** → :gear: → **區塊連接沒有 VPN**中找到。



### 全局切換

現代 Android 裝置具有全局切換功能，可停用藍牙和定位服務。 Android 12為相機和麥克風引入了切換功能。 不使用時，建議停用這些功能。 重新啟用前，應用程式無法使用停用的功能 (即使已授予個別權限)。



## Google 服務

如果您使用的是有 Google 服務的裝置，無論是使用原版作業系統或像 GrapheneOS 這樣安全沙盒化 Google Play 服務的作業系統，您都可以做一些額外的變更來改善您的隱私。 我們仍建議完全避免 Google 服務，或結合 *Shelter* 等裝置控制器與 GrapheneOS 的 Sandboxed Google Play，將 Google Play 服務限制於特定使用者/工作設定檔。



### 進階保護計劃

如果您有 Google 帳戶，我們建議您加入[進階保護計劃](https://landing.google.com/advancedprotection)。 任何人只要擁有兩個或以上支援 [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) 的硬體安全金鑰，即可免費使用。 或者，您可以使用[密碼金鑰](https://fidoalliance.org/passkeys)。

進階防護計劃提供強化的威脅監控，並能夠：

- 更嚴格的雙重認證；例如，**必須**使用 [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online)，且不允許使用 [SMS OTP](../basics/multi-factor-authentication.md#sms-or-email-mfa)、[TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) 和 [OAuth](https://en.wikipedia.org/wiki/OAuth)。
- 只有 Google 和經過驗證的第三方應用程式才能存取帳戶資料
- 掃描 Gmail 帳戶收到的電子郵件，以防[釣魚嘗試](https://en.wikipedia.org/wiki/Phishing#Email_phishing)
- 使用 Google Chrome 進行更嚴格的[安全瀏覽器掃描](https://google.com/chrome/privacy/whitepaper.html#malware)
- 更嚴格的憑證遺失帳戶復原程序
  
  如果您使用非沙盒的 Google Play 服務 (常見於一般作業系統)，進階保護方案也會提供[額外的好處](https://support.google.com/accounts/answer/9764949)，例如：

- 不允許安裝 Google Play 商店、作業系統供應商的應用程式商店以外的應用程式，或透過 [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)

- 使用 [Play Protect](https://support.google.com/googleplay/answer/2812853?#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work) 強制自動設備掃描
- 警告您未經驗證的應用程式



### Google Play 系统更新

過去， Android 安全更新必須由作業系統供應商提供。 從 Android 10 開始， Android 變得更模組化， Google 可以通過特權 Play 服務推送 **約** 系統組件的安全更新。

如果您的 EOL 裝置搭載 Android 10 或更高版本，且無法在裝置上執行我們所推薦的任何作業系統，您最好還是堅持使用您的 OEM Android 安裝系統 (相較於 LineageOS 或 /e/ OS 等未在此列出的作業系統)。 這可讓您從 Google 收到**一些**安全修補程式，同時不會因使用不安全的 Android 衍生程式而違反 Android 安全模式，並增加您的攻擊面。 我們仍建議您盡快升級至支援的裝置。



### 廣告識別碼

所有安裝 Google Play 服務的裝置都會自動產生 [廣告ID](https://support.google.com/googleplay/android-developer/answer/6048248) ，用於定向廣告。 禁用此功能以限制其收集您的資料。

在具有 [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play)的Android 版上，前往 :gear: **設定** → **應用程式** → **Sandboxed Google Play** → **Google 設定** → **廣告**，然後選擇 *刪除廣告ID*。

在具有特權Google Play服務的Android發行版（如 庫存 OSes）上，設置可能在幾個位置。 查看

- :gear: **設定** → **Google** → **廣告**
- :gear: **設定** → **私隱** → **廣告**

可選擇刪除您的廣告ID 或 *選擇退出基於興趣的廣告*，這視 Android OEM 而異。 如果提供刪除首選廣告ID 的選項。 如果沒有，請確保選擇退出並重設您的廣告ID。



### SafetyNet 和 Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) 和 [Play Integrity API](https://developer.android.com/google/play/integrity) 通常用於 [銀行應用程式](https://grapheneos.org/usage#banking-apps)。 許多銀行應用程式在 GrapheneOS 使用沙盒Play服務可以正常運作，但一些非金融應用程式有自己的防篡改機制，這可能會失敗。 GrapheneOS 通過了 `basicIntegrity` 檢查，但沒有`ctsProfileMatch` 證明檢查。 Android 8 以上版本的裝置支援硬體認證，如果沒有洩漏金鑰或嚴重漏洞，則無法繞過。

至於 Google 錢包，我們不建議您這樣做，因為他們的 [隱私政策](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en)規定，如果您不想與結盟行銷服務共享您的信用評級和個人信息，必須選擇退出。
