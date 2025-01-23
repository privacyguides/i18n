---
title: iOS 概述
icon: simple/apple
description: 蘋果公司使用 Unix 作業系統來開發macOS 支援自家的 Mac 電腦。
---

**iOS** 和 **iPadOS** 是 Apple 分別為其 iPhone 和 iPad 產品開發的專有移動作業系統。 如果您擁有 Apple 行動裝置，可透過關閉某些內建遙測功能以及強化系統內建的隱私和安全設定來加強隱私。

## 隱私筆記

iOS 設備因其強大的資料保護和對現代最佳作法的遵守而受到安全專家的讚揚。 然而，Apple 生態系統的限制性——尤其是行動裝置——仍然在很多方面阻礙了隱私。

我們認為，與任何製造商的庫存 Android 設備相比，iOS 為大多數人提供了水平之上的隱私和安全保護。 However, you can achieve even higher standards of privacy with a [custom Android operating system](../android/distributions.md) like GrapheneOS, if you want or need to be completely independent of Apple or Google's cloud services.

### 激活鎖

所有 iOS 設備在初始設定或重置時都必須根據 Apple 的激活鎖伺服器進行檢查，這意味著**需要**網際網路連接才能使用 iOS 設備。

### 強制的 App Store

The only source for apps on iOS is Apple's App Store, which requires an Apple Account to access. 這意味著 Apple 擁有您在設備上安裝的每個應用記錄，且如果向 App Store 提供付款方式，則可能會將該資訊與您的實際身份聯繫起來。

### 侵入式遙測

Apple has historically had problems with properly disassociating their telemetry from Apple Accounts on iOS. In [2019](https://theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings), Apple was found to transmit Siri recordings—some containing highly confidential information—to their servers for manual review by third-party contractors. Though Apple temporarily stopped that program after that practice was [widely reported on](https://theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana), the company rolled out a switch to [**opt out** of uploading conversations with Siri](https://theguardian.com/technology/2019/oct/30/apple-lets-users-opt-out-of-having-siri-conversations-recorded) a few months later in the succeeding iOS update. Moreover, in 2021, [Apple reworked Siri](https://theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance) so that it processes voice recordings locally rather than sending it to their servers.

More recently, Apple has been found to transmit analytics [even when analytics sharing is disabled](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) on iOS, and this data [appears](https://twitter.com/mysk_co/status/1594515229915979776) to be easily linked to unique iCloud account identifiers despite supposedly being decoupled from Apple Accounts.

### Traffic Outside Active VPN Connections

Apple's [privacy policy regarding VPNs](https://apple.com/legal/privacy/data/en/vpns) states:

> Even when a VPN is active, some traffic that is necessary for essential system services will take place outside the VPN so that your device can function properly.

## 建議的設定

**Note:** This guide assumes that you're running the latest version of iOS.

### iCloud

Apple 產品的大多數隱私和安全問題與其雲服務有關，而不是其硬體或軟體。 當使用 iCloud 等 Apple 服務時，大部分資訊都儲存在他們的伺服器上以金鑰保護，且預設情況下 Apple 可以取用該金鑰。 您可以查看 [Apple 文檔](https://support.apple.com/HT202303)，了解哪些服務是端對端加密的。 任何列為“傳輸中”或“伺服器上”的內容都意味著 Apple 可以在未經您許可下訪問存取該資料。 這種訪問級別偶爾會被執法部門濫用，儘管您的資料在設備上還是安全加密的狀態。當然，Apple 與任何其他公司一樣容易遭受資料洩露。

因此，如果使用 iCloud，則應[啟用**進階資料保護**](https://support.apple.com/HT212520)。 這會使用儲存在您裝置上的的金鑰對 iCloud 數據加密（端對端加密）而不是放在 Apple 伺服器的金鑰，以便 iCloud 在發生數據洩露時得到保護，且不會被 Apple 發現。

進階資料保護所用的加密法雖然強大，但[仍然*比不上*](https://discuss.privacyguides.net/t/apple-advances-user-security-with-powerful-new-data-protections/10778/4)其他[雲端服務](../cloud.md)的加密，特別是涉及到 iCloud Drive 時。 雖然我們強烈建議在使用 iCloud 時使用進階資料保護，但我們也建議考慮從更加[注重隱私的服務提供商](../tools.md)尋找 iCloud 的替代品，儘管 大多數人不太可能受到這些加密怪癖的影響。

您也可以先限制同步到 iCloud 的內容來保護您的資料。 在「 **設定** 」應用程式的頂部，如果您已登入 iCloud ，便會看到您的姓名和個人資料相片。 選擇該選項，然後選擇 **iCloud**，然後關閉您不想同步到 iCloud 的任何服務的交換機。 如果第三方應用程式與 iCloud 同步，您可能會看到列在「 **顯示全部** 」下的第三方應用程式，您可以在此處停用這些應用程式。

#### iCloud+

付費 **iCloud+** 訂閱（任何 iCloud 儲存方案）附帶一些隱私保護功能。 雖然這些能為當前 iCloud 客戶提供足夠服務，但不建議通過 [VPN](../vpn.md) 購買 iCloud 方案，和將 [獨立電子郵件別名服務](../email-aliasing.md)僅用在這些功能。

[**Private Relay**](https://apple.com/legal/privacy/data/en/icloud-relay) 是一項代理服務，可透過兩個伺服器轉發您裝置上所有 Safari 、DNS 查詢和未加密流量：一個由 Apple 擁有，另一個由第三方供應商（包括 Akamai、Cloudflare 和 Fastly）擁有。 理論上這應該可以防止鏈中的任何單一提供商（包括 Apple）完全了解您連線訪問的網站。 與 VPN 不同，Private Relay 不保護已加密的流量。

**Hide My Email** 是 Apple 電子郵件別名服務。 當您在網站或應用程式上*使用 Apple 登錄*時，您可以免費創建電子郵件別名，或者通過付費 iCloud+ 方案生成無數的別名。 Hide My Email 的優點是使用 `@icloud.com` 域作為其別名，與其他電子郵件別名服務相比，它可能不太可能被阻止，但不提供獨立服務提供的功能，例如 例如自動 PGP 加密或多郵箱支援。

#### 媒體 & 購買項目

At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to an Apple Account. Select that, then select **Media & Purchases** → **View Account**.

- [ ] 關閉 **個人化推薦**

#### Find My

**Find My(尋找我的iPhone)** 是一項服務，可讓您跟踪您的 Apple 設備並與朋友和家人分享您的位置。 若設備遭竊，它可以讓您從遠端進行抺除，從而防止小偷訪問您的資料。 在以下情況，「尋找我的」[位置資料為 E2EE](https://apple.com/legal/privacy/data/en/find-my)：

- 您的位置已與家人或朋友共享，並且都使用 iOS 17 或更高版本。
- 設備處於離線狀態，且由Find My 網路找到。

設備有連線且遠程使用“尋找 iPhone”來定位您的設備，則位置資料不是 E2EE。 您必須決定權衡是否值得激活防盜鎖。

At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to an Apple Account. 選取這項然後再選 **尋找**。 此處您可以選擇是否啟用或禁用“查找設備”功能。

### 設定

許多其他與隱私相關的設定可以在**設定**應用中找到。

#### 飛航模式

啟用 **飛航模式** 會阻止您的手機與手機基地塔連線。 您仍然可以連接到 Wi-Fi 和藍牙，因此每當您連接到 Wi-Fi 時，您都可以開啟此設定。

#### Wi-Fi

You can enable [hardware address randomization](https://support.apple.com/en-us/102509#triswitch) to protect you from tracking across Wi-Fi networks, and on the same network over time. On the network you are currently connected to, tap the :material-information: button:

- [x] Set **Private Wi-Fi Address** to **Fixed** or **Rotating**

您也可以選擇 **限制 IP 位址追蹤**。 這與 iCloud Private Relay 類似，但僅影響與“已知跟踪器”的連接。 因為它只影響與潛在惡意伺服器的連接，所以啟用此設定應該沒問題，但如果不希望*任何*流量通過 Apple 的伺服器路由，則可把它關掉。

#### 藍牙

**當您不使用藍牙時，應停用藍牙** ，因為它會增加您被攻擊的機會。 透過控制中心停用藍牙（或 Wi-Fi ）只會暫時停用：您必須在「設定」中關閉藍牙才能保持有效。

- [ ] 關閉 **藍牙**

Note that Bluetooth is automatically turned on after every system update.

#### 一般設定

預設情況中，您的 iPhone 裝置名稱將包含您的名字，所連接的網路中的其它人都可以看到該名稱。 所以應該將其更改為更一般的名稱，例如“iPhone”。 Select **About** → **Name** and enter the device name you prefer.

經常安裝 **軟體更新** 以獲得最新的安全修復非常重要。 您可以啟用 **自動更新** ，以保持手機最新，而無需不斷檢查更新。 Select **Software Update** → **Automatic Updates**:

- [x] 打開 **下載 iOS 更新**
- [x] 打開 **安裝 iOS 更新**
- [x] 打開 **安全應變 & 系統檔**

**AirDrop** is commonly used to easily share files, but it represents a significant privacy risk. The AirDrop protocol constantly broadcasts your personal information to your surroundings, with [very weak](https://www.usenix.org/system/files/sec21-heinrich.pdf) security protections. Your identity can easily be discovered by attackers even with limited resources, and the Chinese government has [openly acknowledged](https://arstechnica.com/security/2024/01/hackers-can-id-unique-apple-airdrop-users-chinese-authorities-claim-to-do-just-that/) using such techniques to identify AirDrop users in public since 2022.

- [x] Select **AirDrop** → **Receiving Off**

**AirPlay** 可讓您將內容從 iPhone 無縫串流到電視； 然而，您可能並不會想要一直維持這樣。 Select **AirPlay & Continuity** → **Automatically AirPlay**:

- [x] 選擇 **絕不** 或 **詢問**

**背景 App 重新整理**可將應用程式在不使用時刷新其內容。 這可能會導致它們建立不必要的連接。 Turning this off can also save battery life, but may affect an app's ability to receive updated information, particularly weather and messaging apps.

選擇 **背景 App 重新整理** 並切掉無需在背景下繼續刷新的應用。 若不想讓任何 apps 在背景刷新，可再次選擇 **背景 App 重新整理** 並將其 **關閉**。

#### Siri & 尋找

如果不希望任何人在鎖定時使用 Siri 控制您的手機，可以在此處將其關閉。

- [ ] 關閉 **畫面鎖住時可使用 Siri**

#### Face ID/Touch ID & 密碼

在手機上設定強密碼是確保設備物理安全的最重要步驟。 您必須權衡安全性與便利性：每次輸入較長的密碼很麻煩，但較短的密碼或 PIN 碼很容易被猜到。 設定 Face ID 或 Touch ID 以及強密碼可以在可用性和安全性之間實現良好折衷。

Select **Turn Passcode On** or **Change Passcode** → **Passcode Options** → **Custom Alphanumeric Code**. 確認建立[安全密碼](../basics/passwords-overview.md)。

如果想使用 Face ID 或 Touch ID，可以立即進行設定。 您的手機將使用之前設定的密碼作為後備密碼，以防生物識別驗證失敗。 生物識別解鎖方法主要是便利，雖然它們確實可以阻止監控攝像頭或身旁的人看到您所輸入的密碼。

如果使用生物識別技術，應該知道如何在緊急情況下快速關閉它們。 按住側面按鈕或電源按鈕以及*任一*音量按鈕，直到看到滑動關閉滑塊為止，這將禁用生物識別功能，需要密碼才能解鎖。 設備重新啟動後還需要您的密碼。

On some older devices, you may have to press the power button five times to disable biometrics instead, or for devices with Touch ID, you may just have to hold down the power button and nothing else. 請事先嘗試此操作，以便知道哪種方法適用您的設備。

**Stolen Device Protection** adds additional security intended to protect your personal data if your device is stolen while unlocked. If you use biometrics and the Find My Device feature in your Apple Account settings, we recommend enabling this new protection:

- [x] 選擇**開啟保護**

啟用被盜設備保護後，[某些操作](https://support.apple.com/HT212510)將需要生物識別身份驗證，無需密碼回退（如果駭客准竊盜已獲得您的 PIN），例如使用密碼自動填寫功能就可訪問支付資訊並關閉遺失模式。 It also adds a security delay to certain actions performed away from your home or another "familiar location," such as requiring a 1-hour timer to reset your Apple Account password or sign out of your Apple Account. 此延遲是為了有時間啟用遺失模式並在小偷重置設備前保護好您的帳戶。

**鎖定時允許存取** 提供您在手機鎖定時可以允許的選項。 禁用的這些選項越多，沒有密碼者可做的事情就越少，但對您來說也就更不方便。 選擇不希望其他人接觸您的手機後訪問其中哪些內容。

- [ ] 關閉 **今天概覽和搜尋**
- [ ] 關閉 **通知中心**
- [ ] 關閉 **控制中心**
- [ ] 關閉 **鎖定畫面小工具**
- [ ] 關閉 **Siri**
- [ ] 關閉 **以 Message 回覆**
- [ ] 關閉 **家庭控制**
- [ ] 關閉 **錢包**
- [ ] 關閉 **回撥未接來電**
- [ ] 關閉 **USB 配件**

iPhone 可以抵禦暴力攻擊，在多次嘗試失敗後，需要等待很長時間； 然而，過去已經有一些漏洞可以繞開這個問題。 為了更加安全，可將手機設定為在 10 次密碼嘗試錯誤後自行擦除。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

啟用此設置後，別人可以通過多次輸入錯誤密碼來故意擦除您的手機。 確保有適當備份，並且僅在有把握的情況下才啟用此設定。

</div>

- [x] 打開 **清除資料**

#### 隱私 & 安全

**定位服務**可用在“尋找”和“地圖”等功能。 如果不需要這些功能，可以禁用定位服務。 或者，可以在此處查看並選擇哪些應用程式可以使用您的位置資訊。 選擇 **定位服務**:

- [ ] 關閉 **定位服務**

在這些設定中，最近曾使用您位置的應用程式旁會出現紫色箭頭，而灰色箭頭則表示您的位置在過去 24 小時內曾被存取。 如果您決定開啟位置服務，Apple 預設會將其用於系統服務。 您可以在此檢視並挑選哪些服務可以使用您的位置資訊。 不過，如果您不想向 Apple 提交位置分析資料（他們會利用這些資料來改善 Apple Maps），您也可以在此停用該功能。 選擇**分析與改進功能**：

- [ ] 關閉 **分享 iPhone 分析**
- [ ] Turn off **Routing & Traffic**
- [ ] Turn off **Improve Maps**

您在此處決定是否讓 apps **追蹤** 活動。 關閉此功能可禁止所有應用程式利用手機的廣告 ID 進行跟踪。 選擇 **追蹤**:

- [ ] 關閉 **允許 App 發出追蹤請求**

如果使用者未滿 18 歲，該選項預設停用且無法變更。

如果不想加入，請關閉 **感應 & 使用資料研究** 。 選擇 **感應 & 使用資料研究**:

- [ ] 關閉 **感應器 & 使用資料收集**

**安全檢查**可讓您快速查看和撤銷可能有權訪問您資料的某些人員和應用。 可在此處執行**緊急重設**，立即重設可能有權存取設備資源的所有人員和應用程式權限。 也可以**管理共享和共享存取權限**讓您查看並自訂有權存取裝置和帳戶資源的人員和內容。

如不想發送 Apple 使用資料，應該禁用該分析。 選擇 **分析與改進功能**：

- [ ] 關閉**分享 iPhone 分析** 或**分享 iPhone & 觀看分析**
- [ ] 關閉 **分享 iCloud 數據分析**
- [ ] 關閉 **改善 Fitness+**
- [ ] 關閉 **改進安全性**
- [ ] 關閉 **改進 Siri 與聽寫**
- [ ] Turn off **Improve Assistive Voice Features**
- [ ] Turn off **Improve AR Location Accuracy**

關閉 **個人化廣告** 如不願加入針對式行銷。 選擇 **Apple 廣告**:

- [ ] 關閉 **個人化廣告**

**App 隱私權報告**為內建工具，可讓您查看應用程式使用哪些權限。 選取 **App 隱私權報告**:

- [x] 選擇 **開啟 App 隱私權報告**

[封閉模式](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode)是可以啟用的安全設定使手機更能抵抗攻擊。 請注意，某些應用和功能[將無法正常運作](https://support.apple.com/HT212650)。

- [x] 選擇 **開啟封閉模式**

## 其它建議

### E2EE 通話

通過電信運營商使用“電話”應用程式撥打的一般電話不是 E2EE。 Both FaceTime Video and FaceTime Audio calls are E2EE. Alternatively, you can use [another app](../real-time-communication.md) like Signal for E2EE calls.

### 加密的 iMessage

The [color of the message bubble](https://support.apple.com/en-us/104972) in the Messages app indicates whether your messages are E2EE or not. A blue bubble indicates that you're using iMessage with E2EE, while a green bubble indicates the other party is using either the outdated SMS and MMS protocols or RCS. RCS on iOS is **not** E2EE. Currently, the only way to have E2EE in Messages is for both parties to be using iMessage on Apple devices.

如果您或您的訊息傳遞夥伴在沒有進階資料保護下啟用 iCloud 備份，則加密金鑰會儲存在 Apple 伺服器，這意味著他們可以訪問您的訊息。 Additionally, iMessage's key exchange is not as secure as alternative implementations like Signal's (which allows you to view the recipients key and verify by QR code), so it shouldn't be relied on for particularly sensitive communications.

### Photo Permissions

When an app prompts you for access to your device's photo library, iOS provides you with options to limit what an app can access.

Rather than allow an app to access all the photos on your device, you can allow it to only access whichever photos you choose by tapping the "Select Photos..." option in the permission dialog. You can change photo access permissions at any time by navigating to **Settings** → **Privacy & Security** → **Photos**.

![Photo Permissions](../assets/img/ios/photo-permissions-light.png#only-light) ![Photo Permissions](../assets/img/ios/photo-permissions-dark.png#only-dark)

**Add Photos Only** is a permission that only gives an app the ability to download photos to the photo library. Not all apps which request photo library access provide this option.

![Private Access](../assets/img/ios/private-access-light.png#only-light) ![Private Access](../assets/img/ios/private-access-dark.png#only-dark)

Some apps also support **Private Access**, which functions similarly to the **Limited Access** permission. However, photos shared to apps using Private Access include their location by default. We recommend unchecking this setting if you do not [remove photo metadata](../data-redaction.md) beforehand.

### Contact Permissions

Similarly, rather than allow an app to access all the contacts saved on your device, you can allow it to only access whichever contacts you choose. You can change contact access permissions at any time by navigating to **Settings** → **Privacy & Security** → **Contacts**.

![Contact Permissions](../assets/img/ios/contact-permissions-light.png#only-light) ![Contact Permissions](../assets/img/ios/contact-permissions-dark.png#only-dark)

### Require Biometrics and Hide Apps

iOS offers the ability to lock most apps behind Touch ID/Face ID or your passcode, which can be useful for protecting sensitive content in apps which do not provide the option themselves. You can lock an app by long-pressing on it and selecting **Require Face ID/Touch ID**. Any app locked in this way requires biometric authentication whenever opening it or accessing its contents in other apps. Also, notification previews for locked apps will not be shown.

In addition to locking apps behind biometrics, you can also hide apps so that they don't appear on the Home Screen, App Library, the app list in **Settings**, etc. While hiding apps may be useful in situations where you have to hand your unlocked phone to someone else, the concealment provided by the feature is not absolute, as a hidden app is still visible in some places such as the battery usage list. Moreover, one notable tradeoff of hiding an app is that you will not receive any of its notifications.

You can hide an app by long-pressing on it and selecting **Require Face ID/Touch ID** → **Hide and Require Face ID/Touch ID**. Note that pre-installed Apple apps, as well as the default web browser and email app, cannot be hidden. Hidden apps reside in a **Hidden** folder at the bottom of the App Library, which can be unlocked using biometrics. This folder appears in the App Library whether you hid any apps or not, which provides you a degree of plausible deniability.

### Redacting Elements in Images

If you need to hide information in a photo, you can use Apple's built-in editing tools to do so.

If your device supports it, you can use the [Clean Up](https://support.apple.com/en-us/121429) feature to pixelate faces or remove objects from images.

- Open the **Photos** app and tap the photo you have selected for redaction
- Tap the :material-tune: (at the bottom of the screen)
- Tap the button labeled **Clean Up**
- Draw a circle around whatever you want to redact. Faces will be pixelated and it will attempt to delete anything else.

Our warning [against blurring text](../data-redaction.md) also applies here, so we recommend to instead add a black shape with 100% opacity over it. In addition to redacting text, you can also black out any face or object using the **Photos** app.

- Tap the image you have selected for redaction
- Tap the :material-tune: (at the bottom of the screen) → markup symbol (top right) → plus icon at the bottom right
- Select **Add Shape** and choose the square or circle
- On the toolbar, tap the circle (left-most option) and choose black as the color for filling in the shape. You can also move the shape and increase its size as you see fit.

**Don't** use the highlighter to obfuscate information, as its opacity is not quite 100%.

### 避免 iOS越獄

iPhone 越獄會破壞其安全性更容易受到攻擊。 運行不可信任的第三方軟體可能會導致設備感染惡意軟體。

### iOS Betas

Apple 會為那些希望幫助查找和報告錯誤的人先提供 iOS 測試版。 不建議在手機上安裝測試版軟體。 Beta 版本不夠穩定，可能存在未被發現的安全漏洞。

## 安全重點

### Before First Unlock(初次解鎖之前)

If your threat model includes [:material-target-account: Targeted Attacks](../basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} that involve forensic tools, and you want to minimize the chance of exploits being used to access your phone, you should restart your device frequently. 重啟後**解鎖設備**之前的狀態稱為“首次解鎖之前”(BFU) ，當設備處於該狀態時，取證鑑識工具[明顯更加困難](https://belkasoft.com/checkm8_glossary)利用漏洞訪問您的資料。 此 BFU 狀態允許您接收電話、簡訊和鬧鐘通知，但設備上的大部分資料為加密且無法訪問。 這可能不切實際，因此請考慮權衡這個作法對於自身情況是否有意義。
