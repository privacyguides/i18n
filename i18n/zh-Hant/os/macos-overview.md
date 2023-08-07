---
title: macOS 簡介
icon: material/apple-finder
description: macOS 是蘋果電腦的桌面作業系統，搭配其自家硬體提供了堅固的安全。
---

蘋果公司使用 Unix 作業系統來開發**macOS** 支援自家的 Mac 電腦。 為提高 macOS 隱私，用戶可關閉遙測功能以強化現有的隱私與安全設置。

舊款的 Intel-based Macs 與 Hackintoshe 則無法完全支援 macOS 所提供的安全功能。 為提昇資料安全，建議使用帶[Apple silicon](https://support.apple.com/en-us/HT211814)晶片的.較新款 Mac 。

## 隱私筆記

用戶應考量 一些 macOS 值得關注的隱私問題。 這些涉及作業系統本身，而不是蘋果其他應用程式和服務的問題。

### 激活鎖

新款 Apple silicon 設備無需網際網路連接即可設置。 但是，恢復或重置 Mac 將**需要**連接到 Apple 伺服器，以檢查丟失或被盜設備資料庫的激活鎖。

### 應用程式撤銷檢查

當開啟應用程式時，macOS 會執行連線檢查，驗證應用程式是否包含已知惡意軟體，以及開發人員的簽名證書是否被撤銷。

過去這些檢查是通過未加密的 OCSP 協議執行，因此可能會將您運行的應用程式資料洩露到網路上。 Apple 在 2021 年將其 OCSP 服務升級為 HTTPS 加密，並[發布了該服務的日誌記錄政策資訊](https://support.apple.com/HT202491)。 他們還承諾添加一種機制，讓用戶可選擇退出此連線檢查，但截至 2023 年 7 月，該機制尚未添加到 macOS 。

雖然您[可以](https://electiclight.co/2021/02/23/how-to-run-apps-in-private/)相對輕鬆地手動選擇退出此檢查，但除非您會受到 macOS 執行撤銷檢查的嚴重損害，我們不建議這樣做，因為它們在確保阻止受感染的應用程式運行上發揮著重要作用。

## 建議配置

首次設置 Mac 時，您的帳戶將是管理員帳戶，其具有比標準用戶帳戶更高的權限。 macOS 有許多保護措施可以防止惡意軟體和其他程式濫用您的管理員權限，因此使用此帳戶通常是安全的。

然而，破壞利用 `sudo` 這類的保護效用程式中的漏洞問題，已曾[ 發現過](https://bogner.sh/2014/03/another-mac-os-x-sudo-password-bypass/)。 如果想避免運行的程式濫用管理員權限，可以考慮創建第二個標準用戶帳戶用於日常操作。 這樣的另一個好處是，當應用程式需要管理員訪問權限時，它會更加明顯，因為它每次都會提示您輸入憑據。

如果您使用第二個帳戶，則不會嚴格要求在 macOS 登入畫面需登錄到原始管理員帳戶。 當以標準用戶身份執行需要管理員權限的操作時，系統會提示進行身份驗證，這時可以作為標準用戶單次性輸入管理員憑據。 如果希望在登錄畫面中只有一個帳戶，Apple 提供了[隱藏管理員帳戶的指南](https://support.apple.com/HT203998)。

或者，您可以使用 [macOS Enterprise Privileges](https://github.com/SAP/macOS-enterprise-privileges) 之類的實用程式按需升級到管理員權限，但這可能容易受到一些未被發現弪點的利用，一如所有基於軟體的保護。

### iCloud

Apple 產品的大多數隱私和安全問題與其*雲服務*有關，而不是其硬體或軟體。 當使用 iCloud 等 Apple 服務時，大部分資訊都存儲在他們的伺服器上以密鑰保護，且預設情況下 Apple 可以取用該密鑰。 這種訪問級別偶爾會被執法部門濫用，儘管您的資料在設備上還是安全加密的狀態。當然，Apple 與任何其他公司一樣容易遭受資料洩露。

因此，如果使用 iCloud，則應[啟用**進階資料保護**](https://support.apple.com/HT212520)。 This encrypts nearly all of your iCloud data with keys stored on your devices (end-to-end encryption), rather than Apple's servers, so that your iCloud data is secured in the event of a data breach, and otherwise hidden from Apple.

### 系統設定

您應該確認或更改許多內建設置以強化系統。 開啟**設定** 應用程式：

#### 藍牙

- [ ] 取消勾選 **藍牙** (除非目前正使用中)

#### 網路

Depending on if you are using **Wi-Fi** or **Ethernet** (denoted by a green dot and the word "connected"), click on the corresponding icon.

Click on the "Details" button by your network name:

- [x] Check **Limit IP address tracking**

##### 防火牆

防火牆會阻止不必要的網路連接。 防火牆設置越嚴格，您的 Mac 就越安全。 然而某些服務可能會被封鎖。 您應該將防火牆配置得盡可能嚴格，但不會影響使用的服務。

- [x] Check **Firewall**

點擊 **生成（Generate）** 按鈕。

- [x] Check **Block all incoming connections**

如果配置過於嚴格，可以再回來取消勾選此選項。 但如果應用程式請求，macOS 通常會提示用戶允許該應用的傳入連接。

#### 一般設定

您的設備名稱預設為“[您的名字] 的 iMac”。 Because this name is publicly broadcast on your network, you'll want to change your device name to something generic like "Mac".

Click on **About** and type your desired device name into the **Name** field.

##### 軟體更新

您應自動安裝所有可用更新，以確保 Mac 具有最新的安全修復。

點擊 :material-information-outline: **自動更新** 旁邊的小圖標:

- [x] Check **Check for updates**

- [x] Check **Download new updates when available**

- [x] Check **Install macOS updates**

- [x] Check **Install application updates from the App Store**

- [x] Check **Install Security Responses and system files**

#### 隱私 & 安全

每當應用程式請求權限時，它就會顯示在這裡。 您可決定是否允許或拒絕哪些應用程式的特定權限。

##### 定位服務。

您可以個別同意每個應用程式的定位服務權限。 如果不要應用程式使用您的位置，那麼完全關閉定位服務是最私密的選擇。

- [ ] 取消勾選 **定位服務**

##### 資料分析 & 改進

決定是否要與 Apple 和開發者共享分析資料。

- [ ] 取消勾選 **分享 Mac 數據分析**

- [ ] 取消勾選 **改善 Siri & 偵測**

- [ ] 取消勾選 **分享給應用開發人員**

- [ ] 取消勾選 **分享 iCloud Analytics** (如登入 iCloud 方可看到)

##### Apple 廣告

決定是否依使用狀況個人化廣告接收。

- [ ] 取消勾選 **個人化的廣告**

##### 安全

App Store 中的應用程式須遵守更嚴格的安全準則，例如更嚴格的沙盒。 如果需要的應用程式只能從 App Store 獲取，請將**允許從以下位置下載應用程式**設置更改為**App Store** 防止不小心執行其他應用程式。 這是一個不錯的選擇，特別是當您為其他技術能力較低的用戶（例如兒童）設定電腦時。

如果選擇允許某些認定開發者的應用程序，請注意所運行的應用程式以及從何處取得這些應用。

##### FileVault

在具有 Secure Enclave（Apple T2 安全晶片、Apple 晶片）的現代設備上，您的數據會保持加密。如果設備未檢測到數據遭篡改，則會通過硬體密鑰自動解密。 啟用 FileVault 還需要輪入密碼來解密資料，大大提高了安全性，尤其是在關機時或開機後首次登錄時。

在較舊的 Intel 的 Mac 電腦，FileVault 是預設唯一可用的磁盤加密形式，應始終啟用。

- [x] Click **Turn On**

##### Lockdown Mode

[Lockdown Mode](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) disables some features in order to improve security. Some apps or features won't work the same way they do when it's off, for example, [JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers/) and [WASM](https://developer.mozilla.org/en-US/docs/WebAssembly) are disabled in Safari with Lockdown Mode enabled. We recommend enabling Lockdown Mode and seeing whether it significantly impacts your usage, many of the changes it makes are easy to live with.

- [x] Click **Turn On**

### MAC 地址隨機化

Unlike iOS, macOS doesn't give you an option to randomize your MAC address in the settings, so you'll need to do it with a command or a script.

You open up your Terminal and enter this command to randomize your MAC address:

``` zsh
openssl rand -hex 6 | sed 's/\(..\)/\1:/g; s/.$//' | xargs sudo ifconfig en1 ether 
```

en1 is the name of the interface you're changing the MAC address for. 這可能並不適合每台 Mac，因此要進行檢查，可以按住 option 鍵並單擊螢幕右上角的 Wi-Fi 符號。

這將在重新開機時重置。

## 安全保護

macOS 通過不同屬性的多層軟體和硬體保護來進行深度防禦。 這確保了某一層故障不會損害系統的整體安全性。

### 軟體安全

!!! warning "警告"

    macOS 可以安裝測試版更新。 但它們是不穩定的，可能帶有額外遙測，因為其用於測試目的。 Because of this, we recommend you avoid beta software in general.

#### Signed System Volume

macOS's system components are protected in a read-only signed system volume, meaning that neither you nor malware can alter important system files.

The system volume is verified while it's running and any data that's not signed with a valid cryptographic signature from Apple will be rejected.

#### 系統完整性保護

macOS sets certain security restrictions that can't be overridden. These are called Mandatory Access Controls, and they form the basis of the sandbox, parental controls, and System Integrity Protection on macOS.

System Integrity Protection makes critical file locations read-only to protect against modification from malicious code. This is on top of the hardware-based Kernel Integrity Protection that keeps the kernel from being modified in-memory.

#### 應用程式安全性

##### App 沙盒

macOS apps downloaded from the App Store are required to be sandboxed usng the [App Sandbox](https://developer.apple.com/documentation/security/app_sandbox).

!!! warning "警告"

    Software downloaded from outside the official App Store is not required to be sandboxed. You should avoid non-App Store software as much as possible.

##### 防毒軟體

macOS comes with two forms of malware defense:

1. Protection against launching malware in the first place is provided by the App Store's review process for App Store applications, or *Notarization* (part of *Gatekeeper*), a process where third-party apps are scanned for known malware by Apple before they are allowed to run.
2. Protection against other malware and remediation from existing malware on your system is provided by *XProtect*, a more traditional antivirus software built-in to macOS.

We recommend against installing third-party antivirus software as they typically do not have the system-level access required to properly function anyways, because of Apple's limitations on third-party apps, and because granting the high levels of access they do ask for often poses an even greater security and privacy risk to your computer.

##### 備份

macOS comes with automatic backup software called [Time Machine](https://support.apple.com/HT201250), so you can create encrypted backups to an external or network drive in the event of corrupted/deleted files.

### 硬體安全

Many modern security features in macOS—such as modern Secure Boot, hardware-level exploit mitigation, OS integrity checks, and file-based encryption—rely on Apple silicon, and Apple's newer hardware always has the [best security](https://support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1). We only encourage the use of Apple silicon, and not older Intel-based Mac computers or Hackintoshes.

Some of these modern security features are available on older Intel-based Mac computers with the Apple T2 Security Chip, but that chip is susceptible to the *checkm8* exploit which could compromise its security.

If you use Bluetooth accessories such as a keyboard, we recommend that you use official Apple ones as their firmware will automatically be updated for you by macOS. Using third party accessories is fine, but you should remember to install firmware updates for them regularly.

Apple's SoCs focus on minimizing attack surface by relegating security functions to dedicated hardware with limited functionality.

#### Boot ROM

macOS 通過僅允許官方 Apple 軟件在啟動時運行以防止惡意軟體持久存在； 此稱為安全開機。 Mac computers verify this with a bit of read-only memory on the SoC called the boot ROM, which is laid down during the manufacturing of the chip.

The boot ROM forms the hardware root of trust. 這確保惡意軟體無法篡改開機過程。 Mac 啟動時，開機 ROM 第一個運行，為信任鏈中的第一個環節。

Mac 電腦有三種安全模式啟動：*完全安全*、*降低安全性*和*許可安全*，預設的設置為完全安全。 理想情況下，您應該使用完全安全模式，並避免諸如**內核擴展**而迫使降低安全模式。 請務必[檢查](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac)使用的是完全安全模式。

#### Secure Enclave

安全隔離區是內置於 Apple silicon 設備的安全晶片，負責存儲和生成靜態資料以及 Face ID 和 Touch ID 資料的加密密鑰。 它包含自己獨立的開機 ROM。

您可以將安全隔離區想成設備的安全中心：它具有 AES 加密引擎和安全存儲加密密鑰機制，它與系統的其餘部分分開，因此即使主處理器受到損害，也仍然保持安全。

#### Touch ID

Apple Touch ID 功能可使用生物識別技術安全地解鎖設備。

Your biometric data never leaves your device; it's stored only in the Secure Enclave.

#### 硬體麥克風斷線

所有配備 Apple silicon 或 T2 晶片的筆記型電腦都具備在閉合時內置麥克風硬體即斷線的功能。 這意味著即使作業系統受到破壞，攻擊者無法監聽 Mac 的麥克風。

請注意，攝影機沒有硬體斷接，因為只要上蓋關閉時，其視線即會被遮擋。

#### 外圍處理器安全

電腦除了主 CPU 之外還有內建處理器，用於處理網路、圖形、電源管理等事務。 這些處理器可能沒有足夠的安全性且受到損害，因此蘋果試圖減少其硬體中對這類處理器的需求。

當需要使用其中某一種處理器時，Apple 會與供應商合作，以確保該處理器

- 啟動時從主 CPU 運行經過驗證的韌體
- 有自己的安全啟動鏈
- 遵循最低加密標準
- 確保正確撤銷已知的不良韌體
- 已禁用其調試介面
- 使用 Apple 的加密密鑰簽名

#### 直接記憶體存取保護

Apple silicon 將需要直接訪問記憶體的各組件分開。 例如，Thunderbolt 端口無法訪問為內核指定的記憶體。

## 來源

- [Apple 平台安全](https://support.apple.com/guide/security/welcome/web)
