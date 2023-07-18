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

您應該確認或更改許多內建設置以強化系統。 Open the **Settings** app:

#### 藍牙

- [ ] Uncheck **Bluetooth** (unless you are currently using it)

#### 網路

Depending on if you are using **Wi-Fi** or **Ethernet** (denoted by a green dot and the word "connected"), click on the corresponding icon.

Click on the "Details" button by your network name:

- [x] Check **Limit IP address tracking**

##### 防火牆

防火牆會阻止不必要的網路連接。 The stricter your firewall settings are, the more secure your Mac is. However, certain services will be blocked. You should configure your firewall to be as strict as you can without blocking services you use.

- [x] Check **Firewall**

點擊 **生成（Generate）** 按鈕。

- [x] Check **Block all incoming connections**

If this configuration is too strict, you can come back and uncheck this. However, macOS will typically prompt you to allow incoming connections for an app if the app requests it.

#### 一般設定

By default, your device name will be something like "[your name]'s iMac". Because this name is publicly broadcast on your network, you'll want to change your device name to something generic like "Mac".

Click on **About** and type your desired device name into the **Name** field.

##### 軟體更新

You should automatically install all available updates to make sure your Mac has the latest security fixes.

Click the small :material-information-outline: icon next to **Automatic Updates**:

- [x] Check **Check for updates**

- [x] Check **Download new updates when available**

- [x] Check **Install macOS updates**

- [x] Check **Install application updates from the App Store**

- [x] Check **Install Security Responses and system files**

#### 隱私 & 安全

Whenever an application requests a permission, it will show up here. 您可決定是否允許或拒絕哪些應用程式的特定權限。

##### 定位服務。

您可以個別同意每個應用程式的定位服務權限。 如果不要應用程式使用您的位置，那麼完全關閉定位服務是最私密的選擇。

- [ ] Uncheck **Location Services**

##### Analytics & Improvements

Decide whether you want to share analytics data with Apple and developers.

- [ ] Uncheck **Share Mac Analytics**

- [ ] Uncheck **Improve Siri & Dictation**

- [ ] Uncheck **Share with app developers**

- [ ] Uncheck **Share iCloud Analytics** (visible if you are signed in to iCloud)

##### Apple 廣告

Decide whether you want personalized ads based on your usage.

- [ ] Uncheck **Personalized Ads**

##### 安全

Apps from the App Store are subject to stricter security guidelines, such as stricter sandboxing. If the only apps you need are available from the App Store, change the **Allow applications downloaded from** setting to **App Store** to prevent accidentally running other apps. This is a good option particularly if you are configuring a machine for other, less technical users such as children.

If you choose to also allow applications from identified developers, be careful about the apps you run and where you obtain them.

##### FileVault

On modern devices with a Secure Enclave (Apple T2 Security Chip, Apple silicon), your data is always encrypted, but is decrypted automatically by a hardware key if your device doesn't detect it's been tampered with. Enabling FileVault additionally requires your password to decrypt your data, greatly improving security, especially when powered off or before the first login after powering on.

On older Intel-based Mac computers, FileVault is the only form of disk encryption available by default, and should always be enabled.

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

en1 is the name of the interface you're changing the MAC address for. This might not be the right one on every Mac, so to check you can hold the option key and click the Wi-Fi symbol at the top right of your screen.

這將在重新開機時重置。

## 安全保護

macOS employs defense in depth by relying on multiple layers of software and hardware-based protections, with different properties. This ensures that a failure in one layer does not compromise the system's overall security.

### 軟體安全

!!! warning "警告"

    macOS allows you to install beta updates. These are unstable and may come with extra telemetry since they're for testing purposes. Because of this, we recommend you avoid beta software in general.

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

Some of these modern security features are available on older Intel-based Mac computers with the Apple T2 Security Chip, but that chip is susceptible to the *checkm8* exploit which could compromise its security,

If you use Bluetooth accessories such as a keyboard, we recommend that you use official Apple ones as their firmware will automatically be updated for you by macOS. Using third party accessories is fine, but you should remember to install firmware updates for them regularly.

Apple's SoCs focus on minimizing attack surface by relegating security functions to dedicated hardware with limited functionality.

#### Boot ROM

macOS prevents malware persistence by only allowing official Apple software to run at boot time; this is known as secure boot. Mac computers verify this with a bit of read-only memory on the SoC called the boot ROM, which is laid down during the manufacturing of the chip.

The boot ROM forms the hardware root of trust. This ensures that malware cannot tamper with the boot process. When your Mac boots up, the boot ROM is the first thing that runs, forming the first link in the chain of trust.

Mac computers can be configured to boot in three security modes: *Full Security*, *Reduced Security*, and *Permissive Security*, with the default setting being Full Security. You should ideally be using Full Security mode and avoid things like **kernel extensions** that force you to lower your security mode. Make sure to [check](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac) that you're using Full Security mode.

#### Secure Enclave

The Secure Enclave is a security chip built into devices with Apple silicon which is responsible for storing and generating encryption keys for data at rest as well as Face ID and Touch ID data. It contains its own separate boot ROM.

You can think of the Secure Enclave as your device's security hub: it has an AES encryption engine and a mechanism to securely store your encryption keys, and it's separated from the rest of the system, so even if the main processor is compromised, it should still be safe.

#### Touch ID

Apple's Touch ID feature allows you to securely unlock your devices using biometrics.

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
