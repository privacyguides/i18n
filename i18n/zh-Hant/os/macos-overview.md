---
title: macOS 概述
icon: material/apple-finder
description: macOS 是蘋果電腦的桌面作業系統，搭配其自家硬體提供了堅固的安全。
---

蘋果公司使用 Unix 作業系統來開發**macOS** 支援自家的 Mac 電腦。 為提高 macOS 隱私，用戶可關閉遙測功能以強化現有的隱私與安全設定。

舊款的 Intel-based Macs 與 Hackintoshe 則無法完全支援 macOS 所提供的安全功能。 To enhance data security, we recommend using a newer Mac with [Apple Silicon](https://support.apple.com/HT211814).

## 隱私筆記

用戶應考量 一些 macOS 值得關注的隱私問題。 這些涉及作業系統本身，而不是蘋果其他應用程式和服務的問題。

### 激活鎖

Brand-new Apple Silicon devices can be set up without an internet connection. 但是，恢復或重置 Mac 將**需要**連接到 Apple 伺服器，以檢查丟失或被盜設備資料庫的激活鎖。

### 應用程式撤銷檢查

當開啟應用程式時，macOS 會執行連線檢查，驗證應用程式是否包含已知惡意軟體，以及開發人員的簽名證書是否被撤銷。

Apple 的 OCSP 服務使用 HTTPS 加密，因此只有他們能夠看到您開啟了哪些應用程式。 他們 [已公佈](https://support.apple.com/HT202491) 有關這項服務的登錄政策資訊。 此外，他們 [還承諾會](http://lapcatsoftware.com/articles/2024/8/3.html) 新增一個機制，讓人們可以選擇退出這項線上檢查，但 macOS 並未新增這項功能。

雖然 [可以](https://eclecticlight.co/2021/02/23/how-to-run-apps-in-private) 相對輕鬆地手動選擇退出此檢查，但除非您會受到 macOS 執行撤銷檢查的嚴重損害，不建議這樣做，它們在確保阻止受感染的應用程式運行上發揮著重要作用。

## 建議的設定

首次設定 Mac 時，您的帳戶將是管理員帳戶，其具有比標準用戶帳戶更高的權限。 macOS 有許多保護措施可以防止惡意軟體和其他程式濫用您的管理員權限，因此使用此帳戶通常是安全的。

然而，破壞利用 `sudo` 這類的保護效用程式中的漏洞問題，已[ 發現過](https://bogner.sh/2014/03/another-mac-os-x-sudo-password-bypass)。 如果想避免運行的程式濫用管理員權限，可以考慮創建第二個標準用戶帳戶用於日常操作。 這樣的另一個好處是，當應用程式需要管理員訪問權限時，它會更加明顯，因為它每次都會提示您輸入憑據。

如果您使用第二個帳戶，則不會嚴格要求在 macOS 登入畫面需登錄到原始管理員帳戶。 當以標準用戶身份執行需要管理員權限的操作時，系統會提示進行身份驗證，這時可以作為標準用戶單次性輸入管理員憑據。 如果希望在登錄畫面中只有一個帳戶，Apple 提供了[隱藏管理員帳戶的指南](https://support.apple.com/HT203998)。

### iCloud

當使用 iCloud 等 Apple 服務時，大部分資訊都儲存在他們的伺服器上以金鑰保護，且預設情況下 Apple 可以取用該金鑰。 Apple 將此稱為 [標準資料保護](https://support.apple.com/en-us/102651)。

因此，如果使用 iCloud，則應[啟用**進階資料保護**](https://support.apple.com/HT212520)。 它利用存在設備上的金鑰對您的 iCloud 資料（端對端）加密，此金鑰並不在Apple 伺服器，因此發生數據洩露時您的 iCloud 數據可得到保護與隱匿。

如果您希望能夠從 App Store 安裝應用程式，但不想啟用 iCloud，您可以從 App Store 登入 Apple 帳戶，而非 **系統設定**。

### 系統設定

您應該確認或更改許多內建設定以強化系統。 開啟**設定** 應用程式：

#### 藍牙

- [ ] Turn off **Bluetooth** (unless you are currently using it)

#### 網路

取決於您使用的是**Wi-Fi** 還是**以太網**（由綠點和“已連接”顯示） ”），點擊相應的圖標。

單擊網路名稱旁邊的“詳細資訊”按鈕：

- [x] Select **Rotating** under **Private Wi-Fi address**

- [x] Turn on **Limit IP address tracking**

##### 防火牆

防火牆會阻止不必要的網路連接。 防火牆設定越嚴格，您的 Mac 就越安全。 然而某些服務可能會被封鎖。 您應該將防火牆配置得盡可能嚴格，但不會影響使用的服務。

- [x] Turn on **Firewall**

點擊 **生成（Generate）** 按鈕。

- [x] Turn on **Block all incoming connections**

如果配置過於嚴格，可以再回來取消勾選此選項。 但如果應用程式請求，macOS 通常會提示用戶允許該應用的傳入連接。

#### 一般設定

您的設備名稱預設為“[您的名字] 的 iMac”。 Because this name is [publicly broadcast on your network](https://support.apple.com/guide/mac-help/change-computers-local-hostname-mac-mchlp2322/26/mac/26#:~:text=The%20local%20hostname%2C%20or%20local%20network%20name%2C%20is%20displayed%20at%20the%20bottom%20of%20the%20Sharing%20settings%20window.%20It%20identifies%20your%20Mac%20to%20Bonjour%2Dcompatible%20services.), you'll want to change your device name to something generic like "Mac".

單擊**關於**，然後在**名稱**欄位上輸入想取的設備名稱。

##### 軟體更新

您應自動安裝所有可用更新，以確保 Mac 具有最新的安全修復。

點擊 :material-information-outline: **自動更新** 旁邊的小圖標:

- [x] Turn on **Download new updates when available**

- [x] Turn on **Install macOS updates**

- [x] Turn on **Install Security Responses and system files**

#### Apple Intelligence & Siri

If you do not use these features on macOS, you should disable them:

- [ ] Turn off **Apple Intelligence**
- [ ] 關閉 **Siri**

**[Apple Intelligence](https://apple.com/legal/privacy/data/en/intelligence-engine)** is only available if your device supports it. Apple Intelligence uses a combination of on-device processing and their [Private Cloud Compute](https://security.apple.com/blog/private-cloud-compute) for things that take more processing power than your device can provide.

To see a report of all the data sent via Apple Intelligence, you can navigate to **Privacy & Security** → **Apple Intelligence Report** and press **Export Activity** to see activity from the either the last 15 minutes or 7 days, depending on what you set it for. Similar to the **App Privacy Report** which shows you the recent permissions accessed by the apps on your phone, the Apple Intelligence Report likewise shows what is being sent to Apple's servers while using Apple Intelligence.

By default, ChatGPT integration is disabled. If you don't want ChatGPT integration anymore, you can navigate to **ChatGPT**:

- [ ] Turn off **Use ChatGPT**

You can also have it ask for confirmation every time if you leave ChatGPT integration on:

- [x] Turn on **Confirm Requests**

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Any request made with ChatGPT will be sent to ChatGPT's servers, there is no on-device processing and no PCC like with Apple Intelligence.

</div>

#### 隱私 & 安全

每當應用程式請求權限時，它就會顯示在這裡。 您可決定是否允許或拒絕哪些應用程式的特定權限。

##### 定位服務。

您可以個別同意每個應用程式的定位服務權限。 如果不要應用程式使用您的位置，那麼完全關閉定位服務是最私密的選擇。

- [ ] 關閉 **定位服務**

##### 資料分析 & 改進

Decide whether you want to share analytics data with Apple and app developers.

##### Apple 廣告

決定是否依使用狀況個人化廣告接收。

- [ ] 關閉 **個人化廣告**

##### FileVault

On modern devices with a Secure Enclave (Apple T2 Security Chip, Apple Silicon), your data is always encrypted, but is decrypted automatically by a hardware key if your device doesn't detect it's been tampered with. Enabling [FileVault](../encryption.md#filevault) additionally requires your password to decrypt your data, greatly improving security, especially when powered off or before the first login after powering on.

在較舊的 Intel 的 Mac 電腦，FileVault 是預設唯一可用的磁盤加密形式，應始終啟用。

- [x] 點擊 **開啟**

##### 封閉模式

**[Lockdown Mode](https://support.apple.com/guide/mac-help/lock-mac-targeted-a-cyberattack-ibrw66f4e191/mac)** disables some features in order to improve security. Some apps or features won't work the same way they do when it's off. For example, Javascript Just-In-Time ([JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers)) compilation and [WebAssembly](https://developer.mozilla.org/docs/WebAssembly) are disabled in Safari with Lockdown Mode enabled. We recommend enabling Lockdown Mode and seeing whether it significantly impacts daily usage.

- [x] 點擊 **開啟**

### MAC 位址隨機化

macOS uses a randomized MAC address when [performing Wi-Fi scans](https://support.apple.com/guide/security/privacy-features-connecting-wireless-networks-secb9cb3140c/web) while disconnected from a network.

You can set your [MAC address to be randomized](https://support.apple.com/en-us/102509) per network and rotate occasionally to prevent tracking between networks and on the same network over time.

Go to **System Settings** → **Network** → **Wi-Fi** → **Details** and set **Private Wi-Fi address** to either **Fixed** if you want a fixed but unique address for the network you're connected to, or **Rotating** if you want it to change over time.

Consider changing your hostname as well, which is another device identifier that's broadcast on the network you're connected to. You may wish to set your hostname to something generic like "MacBook Air", "Laptop", "John's MacBook Pro", or "iPhone" in **System Settings** → **General** → **Sharing**.

## 安全保護

macOS 通過不同屬性的多層軟體和硬體保護來進行深度防禦。 這確保了某一層故障不會損害系統的整體安全性。

### 軟體安全

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

macOS 可以安裝測試版更新。 These are unstable and may come with [extra telemetry](https://beta.apple.com/privacy) since they're for testing purposes. 因此，我們建議避免使用測試版軟體。

</div>

#### 簽署系統卷宗

macOS's system components are protected in a read-only [signed system volume](https://support.apple.com/guide/security/signed-system-volume-security-secd698747c9/web), meaning that neither you nor malware can alter important system files.

系統卷宗在運行時會予以驗證，任何未使用 Apple 的有效加密簽名進行簽署的數據都將遭拒絕。

#### 系統完整性保護

macOS 設定了某些無法覆蓋的安全限制。 These are called [Mandatory Access Controls](https://support.apple.com/guide/security/system-integrity-protection-secb7ea06b49/1/web/1), and they form the basis of the sandbox, parental controls, and [System Integrity Protection](https://support.apple.com/en-us/102149) on macOS.

系統完整保護使重要的檔案成為唯讀，以防止惡意代碼的修改。 這是基於硬體內核完整保護之上，可防止記憶體中的內核遭修改。

#### 應用程式安全性

##### App 沙盒

On macOS, whether an app is sandboxed is determined by the developer when they sign it. The [App Sandbox](https://developer.apple.com/documentation/xcode/configuring-the-macos-app-sandbox) protects against vulnerabilities in the apps you run by limiting what a malicious actor can access in the event that the app is exploited. The App Sandbox *alone* can't protect against [:material-package-variant-closed-remove: Supply Chain Attacks](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian} by malicious developers. For that, sandboxing needs to be enforced by someone other than the developer themselves, as it is on the [App Store](https://support.apple.com/guide/security/gatekeeper-and-runtime-protection-sec5599b66df/1/web/1#:~:text=All%20apps%20from%20the%20App%20Store%20are%20sandboxed%20to%20restrict%20access%20to%20data%20stored%20by%20other%20apps.).

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

從官方 App Store 之外下載的軟體不需要沙盒。 If your threat model prioritizes defending against [:material-bug-outline: Passive Attacks](../basics/common-threats.md#security-and-privacy){ .pg-orange }, then you may want to check if the software you download outside the App Store is sandboxed, which is up to the developer to *opt in*.

</div>

You can check if an app uses the App Sandbox in a few ways:

You can check if apps that are already running are sandboxed using the [Activity Monitor](https://developer.apple.com/documentation/security/protecting-user-data-with-app-sandbox#Verify-that-your-app-uses-App-Sandbox).

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Just because one of an app's processes is sandboxed doesn't mean they all are.

</div>

Alternatively, you can check apps before you run them by running this command in the terminal:

``` zsh
codesign -dvvv --entitlements - <path to your app>
```

If an app is sandboxed, you should see the following output:

``` zsh
    [Key] com.apple.security.app-sandbox
    [Value]
        [Bool] true
```

If you find that the app you want to run is not sandboxed, then you may employ methods of [compartmentalization](../basics/common-threats.md#security-and-privacy) such as virtual machines or separate devices, use a similar app that is sandboxed, or choose to not use the non-sandboxed app altogether.

##### Hardened Runtime

The [Hardened Runtime](https://developer.apple.com/documentation/security/hardened_runtime) is an extra form of protection for apps that prevents certain classes of exploits. It improves the security of apps against exploitation by disabling certain features like JIT.

You can check if an app uses the Hardened Runtime using this command:

``` zsh
codesign -dv <path to your app>
```

If Hardened Runtime is enabled, you will see `flags=0x10000(runtime)`. The `runtime` output means Hardened Runtime is enabled. There might be other flags, but the runtime flag is what we're looking for here.

You can enable a column in Activity Monitor called "Restricted" which is a flag that prevents programs from injecting code via macOS's [dynamic linker](https://pewpewthespells.com/blog/blocking_code_injection_on_ios_and_os_x.html). Ideally, this should say "Yes".

##### 防毒軟體

macOS comes with two forms of [malware defense](https://support.apple.com/guide/security/protecting-against-malware-sec469d47bd8/1/web/1):

1. 首先，防止啟動惡意軟體是由 App Store 對 App Store 應用程式的審核流程或*公證*（*Gatekeeper* 的一部份），這是 Apple 允許運行之前掃描第三方應用程式是否存在已知惡意軟體的程式。 Apps are required to be signed by the developers using a key given to them by Apple. This ensures that you are running software from the real developers. Notarization also requires that developers enable the Hardened Runtime for their apps, which limits methods of exploitation.
2. *XProtect* 提供針對其他惡意軟體的防護以及修復系統上現有惡意軟體，XProtect 是 macOS 內建較傳統的防病毒軟體。

We recommend against installing third-party antivirus software as they typically do not have the system-level access required to properly function anyway, because of Apple's limitations on third-party apps, and because granting the high levels of access they do ask for often poses an even greater security and privacy risk to your computer.

##### 備份

macOS comes with automatic backup software called [Time Machine](https://support.apple.com/HT201250), so you can create [encrypted backups](https://support.apple.com/guide/mac-help/keep-your-time-machine-backup-disk-secure-mh21241/mac) to an external drive or a network drive in the event of corrupted/deleted files.

### 硬體安全

Many modern security features in macOS—such as modern Secure Boot, hardware-level exploit mitigation, OS integrity checks, and file-based encryption—rely on Apple Silicon, and Apple's newer hardware always has the [best security](https://support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1). We only encourage the use of Apple Silicon, and not older Intel-based Mac computers or Hackintoshes.

其中一些現代安全功能可在配備Apple T2 安全晶片的 Intel 老式Mac 電腦上使用，但該晶片容易受到*checkm8* 漏洞的攻擊，這可能會損害其安全性。

If you use Bluetooth accessories such as a keyboard, we recommend that you use official Apple ones as their firmware will [automatically be updated](https://support.apple.com/en-us/120303#:~:text=Firmware%20updates%20are%20automatically%20delivered%20in%20the%20background%20while%20the%20Magic%20Keyboard%20is%20actively%20paired%20to%20a%20device%20running%20macOS%2C%20iOS%2C%20iPadOS%2C%20or%20tvOS.) for you by macOS. 使用第三方配件沒問題，但應該記住定期為其更新安裝軔體。

Apple's SoCs focus on [minimizing attack surface](https://support.apple.com/en-vn/guide/security/secf020d1074/web#:~:text=Security%2Dfocused%20hardware%20follows%20the%20principle%20of%20supporting%20limited%20and%20discretely%20defined%20functions%20to%20minimize%20attack%20surface.) by relegating security functions to dedicated hardware with limited functionality.

#### Boot ROM

macOS prevents malware persistence by only allowing official Apple software to run at boot time; this is known as [secure boot](https://support.apple.com/en-vn/guide/security/secac71d5623/1/web/1). Mac computers verify this with a bit of read-only memory on the SoC called the [boot ROM](https://support.apple.com/en-vn/guide/security/aside/sec5240db956/1/web/1), which is [laid down during the manufacturing of the chip](https://support.apple.com/en-vn/guide/security/secf020d1074/1/web/1#:~:text=which%20is%20laid%20down%20during%20Apple%20SoC%20fabrication).

開機 ROM 構成了硬體信任根。 This ensures that malware cannot tamper with the boot process, since the boot ROM is immutable. Mac 啟動時，開機 ROM 第一個運行，為信任鏈中的第一個環節。

Mac computers can be configured to boot in [three security modes](https://support.apple.com/guide/deployment/startup-security-dep5810e849c/web#dep32fb404e1): *Full Security*, *Reduced Security*, and *Permissive Security*, with the default setting being Full Security. You should ideally be using Full Security mode and avoid things like **[kernel extensions](https://support.apple.com/guide/deployment/system-extensions-in-macos-depa5fb8376f/web#dep51e097f45)** that force you to lower your security mode. 請務必[檢查](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac)使用的是完全安全模式。

#### 安全隔離區

The **[Secure Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/web)** is a security chip built into devices with Apple Silicon which is responsible for storing and generating encryption keys for data at rest as well as Face ID and Touch ID data. It contains its own [separate boot ROM](https://support.apple.com/en-vn/guide/security/sec59b0b31ff/web#sec43006c49f).

您可以將安全隔離區想成裝置的安全中心：它具有 AES 加密引擎和安全儲存加密金鑰機制，它與系統的其餘部分分開，因此即使主處理器受到損害，也仍然保持安全。

#### Touch ID

Apple Touch ID 功能可使用生物識別技術安全地解鎖設備。

Your biometric data [never leaves your device](https://www.apple.com/legal/privacy/data/en/touch-id/#:~:text=Touch%C2%A0ID%20data%20does%20not%20leave%20your%20device%2C%20and%20is%20never%20backed%20up%20to%20iCloud%20or%20anywhere%20else.); it's stored only in the Secure Enclave.

#### 硬體麥克風斷線

All laptops with Apple Silicon or the T2 chip feature a [hardware disconnect](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web) for the built-in microphone whenever the lid is closed. 這意味著即使作業系統受到破壞，攻擊者無法監聽 Mac 的麥克風。

請注意，攝影機沒有硬體斷接，因為只要上蓋關閉時，其視線即會被遮擋。

#### Secure Camera Indicator

The built-in camera in a Mac is designed so that the camera can't turn on without the camera indicator light [also turning on](https://support.apple.com/en-us/102177#:~:text=The%20camera%20is%20engineered%20so%20that%20it%20can’t%20activate%20without%20the%20camera%20indicator%20light%20also%20turning%20on.%20This%20is%20how%20you%20can%20tell%20if%20your%20camera%20is%20on.).

#### 外圍處理器安全

Computers have [built-in processors](https://support.apple.com/en-vn/guide/security/seca500d4f2b/1/web/1) other than the main CPU that handle things like networking, graphics, power management, etc. 這些處理器可能沒有足夠的安全性且受到損害，因此蘋果試圖減少其硬體中對這類處理器的需求。

當需要使用其中某一種處理器時，Apple 會與供應商合作，以確保該處理器

- 啟動時從主 CPU 運行經過驗證的韌體
- 有自己的安全啟動鏈
- 遵循最低加密標準
- 確保正確撤銷已知的不良韌體
- 已禁用其調試介面
- 使用 Apple 的加密金鑰簽名

#### 直接記憶體存取保護

Apple Silicon separates each component that requires [direct memory access](https://support.apple.com/guide/security/direct-memory-access-protections-seca4960c2b5/1/web/1). 例如，Thunderbolt 端口無法訪問為內核指定的記憶體。

#### Terminal Secure Keyboard Entry

Enable [Secure Keyboard Entry](https://support.apple.com/guide/terminal/use-secure-keyboard-entry-trml109/mac) to prevent other apps from detecting what you type in the terminal.
