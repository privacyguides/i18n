---
title: iOS 介紹
icon: simple/apple
description: iOS 為 蘋果電腦公司為 iPhone 所開發的移動作業系統。
---

**iOS** 和 **iPadOS** 是 Apple 分別為其 iPhone 和 iPad 產品開發的專有移動作業系統。 如果您擁有 Apple 移動設備，可通過禁用某些內置遙測功能以及強化系統內置的隱私和安全設置來增強隱私。

## 隱私筆記

iOS 設備因其強大的資料保護和對現代最佳作法的遵守而受到安全專家的讚揚。 然而，Apple 生態系統的限制性——尤其是移動設備——仍然在很多方面阻礙了隱私。

我們認為，與任何製造商的庫存 Android 設備相比，iOS 為大多數人提供了水平之上的隱私和安全保護。 不過，如希望或需要完全從 Apple 或 Google 雲獨立，您可以使用 GrapheneOS 等[自定義 Android 作業系統](../android.md)來實現更高的隱私標準服務。

### 激活鎖

所有 iOS 設備在初始設置或重置時都必須根據 Apple 的激活鎖伺服器進行檢查，這意味著**需要**網際網路連接才能使用 iOS 設備。

### 強制的 App Store

IOS 上應用的唯一來源是 Apple App Store，需要 Apple ID 才能訪問。 這意味著 Apple 擁有您在設備上安裝的每個應用記錄，且如果向 App Store 提供付款方式，則可能會將該資訊與您的實際身份聯繫起來。

### 侵入式遙測

蘋果在 iOS 適當匿名遙測上常發生問題。 [2019 年](https://www.theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings)，Apple 被發現將 Siri 錄音（其中一些包含高度機密信息）傳輸回其伺服器，以供第三方承包商進行手動審核。 雖然這種做法被[廣泛報導](https://www.theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech -microsoft-cortana)後他們暫時停止該計劃，但截至[ 2021 年](https://www.theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance)，此問題仍未完全解決。

最近，人們發現 Apple [即使在禁用分析共享的情況下， iOS 上也會傳輸分析數據 ](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) ，儘管據稱匿名的，這些數據[似乎](https://twitter.com/mysk_co/status/1594515229915979776)很容易連結到唯一的 iCloud 帳戶標識符。 截至 2023 年 7 月，Apple 尚未修復[這些問題](https://gizmodo.com/clarence-thomas-aide-venmo-laywers-supreme-court-1850631585)。

## 建議配置

### iCloud

Apple 產品的大多數隱私和安全問題與其雲服務有關，而不是其硬體或軟體。 當使用 iCloud 等 Apple 服務時，大部分資訊都存儲在他們的伺服器上以密鑰保護，且預設情況下 Apple 可以取用該密鑰。 您可以查看 [Apple 文檔](https://support.apple.com/HT202303)，了解哪些服務是端到端加密的。 任何列為“傳輸中”或“伺服器上”的內容都意味著 Apple 可以在未經您許可下訪問存取該資料。 這種訪問級別偶爾會被執法部門濫用，儘管您的資料在設備上還是安全加密的狀態。當然，Apple 與任何其他公司一樣容易遭受資料洩露。

因此，如果使用 iCloud，則應[啟用**進階資料保護**](https://support.apple.com/HT212520)。 This encrypts nearly all of your iCloud data with keys stored on your devices (end-to-end encryption), rather than Apple's servers, so that your iCloud data is secured in the event of a data breach, and otherwise hidden from Apple.

The encryption used by Advanced Data Protection, while strong, [is not *quite* as robust](https://discuss.privacyguides.net/t/apple-advances-user-security-with-powerful-new-data-protections/10778/4) as the encryption offered by other [cloud services](../cloud.md), particularly when it comes to iCloud Drive. 雖然我們強烈建議在使用 iCloud 時使用進階資料保護，但我們也建議考慮從更加[注重隱私的服務提供商](../tools.md)尋找 iCloud 的替代品，儘管 大多數人不太可能受到這些加密怪癖的影響。

您也可以先限制同步到 iCloud 的內容來保護您的資料。 在「 **設定** 」應用程式的頂部，如果您已登入 iCloud ，便會看到您的姓名和個人資料相片。 選擇該選項，然後選擇 **iCloud**，然後關閉您不想同步到 iCloud 的任何服務的交換機。 如果第三方應用程式與 iCloud 同步，您可能會看到列在「 **顯示全部** 」下的第三方應用程式，您可以在此處停用這些應用程式。

#### iCloud+

A paid **iCloud+** subscription (with any iCloud storage plan) comes with some privacy-protecting functionality. While these may provide adequate service for current iCloud customers, we wouldn't recommend purchasing an iCloud+ plan over a [VPN](../vpn.md) and [standalone email aliasing service](../email.md#email-aliasing-services) just for these features alone.

**Private Relay** is a proxy service which relays your Safari traffic through two servers: one owned by Apple and one owned by a third-party provider (including Akamai, Cloudflare, and Fastly). 理論上這應該可以防止鏈中的任何單一提供商（包括 Apple）完全了解您連線訪問的網站。 與完整的 VPN 不同，Private Relay 不會保護 Safari 以外其它應用程式的流量。

**Hide My Email** is Apple's email aliasing service. You can create an email aliases for free when you *Sign In With Apple* on a website or app, or generate unlimited aliases on demand with a paid iCloud+ plan. Hide My Email has the advantage of using the `@icloud.com` domain for its aliases, which may be less likely to be blocked compared to other email aliasing services, but does not offer functionality offered by standalone services such as automatic PGP encryption or multiple mailbox support.

#### 媒體 & 購買項目

在「 **設定** 」應用程式的頂部，如果您已登入 Apple ID，便會看到您的姓名和個人資料相片。 Select that, then select **Media & Purchases** > **View Account**.

- [ ] Turn off **Personalized Recommendations**

#### Find My

**Find My** is a service that lets you track your Apple devices and share your location with your friends and family. 若設備遭竊，它可以讓您從遠端進行抺除，從而防止小偷訪問您的資料。 Your Find My [location data is E2EE](https://www.apple.com/legal/privacy/data/en/find-my/) when:

- 您的位置已與家人或朋友共享，並且都使用 iOS 15 或更高版本。
- Your device is offline and is located by the Find My Network.

Your location data is not E2EE when your device is online and you use Find My iPhone remotely to locate your device. You will have to make the decision whether these trade-offs are worth the anti-theft benefits of Activation Lock.

在「 **設定** 」應用程式的頂部，如果您已登入 Apple ID，便會看到您的姓名和個人資料相片。 Select that, then select **Find My**. 此處您可以選擇是否啟用或禁用“查找設備”功能。

### 設定

許多其他與隱私相關的設置可以在**設置**應用中找到。

#### 飛航模式

啟用 **飛航模式** 會阻止您的手機與手機基地塔連線。 您仍然可以連接到 Wi-Fi 和藍牙，因此每當您連接到 Wi-Fi 時，您都可以開啟此設置。

#### Wi-Fi

您可以啟用硬體位址隨機化功能，以保護您免受跨 Wi-Fi 網路的追蹤。 在您目前連線的網路上，按下 :material-information: 按鈕：

- [x] 打開 **私人 Wi-Fi 地址**

您也可以選擇 **限制 IP 位址追蹤**。 這與 iCloud Private Relay 類似，但僅影響與“已知跟踪器”的連接。 因為它只影響與潛在惡意伺服器的連接，所以啟用此設置應該沒問題，但如果不希望*任何*流量通過 Apple 的伺服器路由，則可把它關掉。

#### 藍牙

**當您不使用藍牙時，應停用藍牙** ，因為它會增加您被攻擊的機會。 透過控制中心停用藍牙（或 Wi-Fi ）只會暫時停用：您必須在「設定」中關閉藍牙才能保持有效。

- [] 關閉 **藍牙**

#### 一般設定

Your iPhone's device name will by default contain your first name, and this will be visible to anyone on networks you connect to. You should change this to something more generic, like "iPhone." Select **About** > **Name** and enter the device name you prefer.

It is important to install **Software Updates** frequently to get the latest security fixes. You can enable **Automatic Updates** to keep your phone up-to-date without needing to constantly check for updates. Select **Software Update** > **Automatic Updates**:

- [x] Turn on **Download iOS Updates**
- [x] Turn on **Install iOS Updates**
- [x] Turn on **Security Responses & System Files**

**AirDrop** allows you to easily transfer files, but it can allow strangers to send you files you do not want.

- [x] Select **AirDrop** > **Receiving Off**

**AirPlay** lets you seamlessly stream content from your iPhone to a TV; however, you might not always want this. Select **AirPlay & Handoff** > **Automatically AirPlay to TVs**:

- [x] Select **Never** or **Ask**

**Background App Refresh** allows your apps to refresh their content while you're not using them. This may cause them to make unwanted connections. Turning this off can also save battery life, but it may affect an app's ability to receive updated information, particularly weather and messaging apps.

Select **Background App Refresh** and switch off any apps you don't want to continue refreshing in the background. If you don't want any apps to refresh in the background, you can select **Background App Refresh** again and turn it **Off**.

#### Siri & 尋找

If you don't want anyone to be able to control your phone with Siri when it is locked, you can turn that off here.

- [ ] Turn off **Allow Siri When Locked**

#### Face ID/Touch ID & Passcode

在手機上設置強密碼是確保設備物理安全的最重要步驟。 您必須權衡安全性與便利性：每次輸入較長的密碼很麻煩，但較短的密碼或 PIN 碼很容易被猜到。 設置 Face ID 或 Touch ID 以及強密碼可以在可用性和安全性之間實現良好折衷。

Select **Turn Passcode On** or **Change Passcode** > **Passcode Options** > **Custom Alphanumeric Code**. 確認有創建一組[安全密碼](https://www.privacyguides.org/basics/passwords-overview/)。

如果想使用 Face ID 或 Touch ID，可以立即進行設置。 您的手機將使用之前設置的密碼作為後備密碼，以防生物識別驗證失敗。 生物識別解鎖方法主要是便利，雖然它們確實可以阻止監控攝像頭或身旁的人看到您所輸入的密碼。

如果使用生物識別技術，應該知道如何在緊急情況下快速關閉它們。 Holding down the side or power button and *either* volume button until you see the Slide to Power Off slider will disable biometrics, requiring your passcode to unlock. 設備重新啟動後還需要您的密碼。

在某些較舊的設備上，可能需要按電源按鈕五次才能禁用生物識別功能，或者具有 Touch ID 的設備，可能只需按住電源按鈕即可。 請事先嘗試此操作，以便知道哪種方法適用您的設備。

**Allow Access When Locked** gives you options for what you can allow when your phone is locked. The more of these options you disable, the less someone without your password can do, but the less convenient it will be for you. Pick and choose which of these you don't want someone to have access to if they get their hands on your phone.

- [ ] Turn off **Today View and Search**
- [ ] Turn off **Notification Center**
- [ ] Turn off **Control Center**
- [ ] Turn off **Lock Screen Widgets**
- [ ] Turn off **Siri**
- [ ] Turn off **Reply with Message**
- [ ] Turn off **Home Control**
- [ ] Turn off **Wallet**
- [ ] Turn off **Return Missed Calls**
- [ ] Turn off **USB Accessories**

iPhones are already resistant to brute-force attacks by making you wait long periods of time after multiple failed attempts; however, there have historically been exploits to get around this. To be extra safe, you can set your phone to wipe itself after 10 failed passcode attempts.

!!! warning "警告"

    With this setting enabled, someone could intentionally wipe your phone by entering the wrong password many times. Make sure you have proper backups and only enable this setting if you feel comfortable with it.

- [x] Turn on **Erase Data**

#### 隱私

**Location Services** allows you to use features like Find My and Maps. If you don't need these features, you can disable Location Services. Alternatively, you can review and pick which apps can use your location here. Select **Location Services**:

- [ ] Turn off **Location Services**

You can decide to allow apps to request to **track** you here. Disabling this disallows all apps from tracking you with your phone's advertising ID. Select **Tracking**:

- [ ] Turn off **Allow Apps to Request to Track**

You should turn off **Research Sensor & Usage Data** if you don't wish to participate in studies. Select **Research Sensor & Usage Data**:

- [ ] Turn off **Sensor & Usage Data Collection**

**Safety Check** allows you to quickly view and revoke certain people and apps that might have permission to access your data. Here you can perform an **Emergency Reset**, immediately resetting permissions for all people and apps which might have access to device resources, and you can **Manage Sharing & Access** which allows you to go through and customize who and what has access to your device and account resources.

You should disable analytics if you don't wish to send Apple usage data. Select **Analytics & Improvements**:

- [ ] Turn off **Share iPhone Analytics** or **Share iPhone & Watch Analytics**
- [ ] Turn off **Share iCloud Analytics**
- [ ] Turn off **Improve Fitness+**
- [ ] Turn off **Improve Safety**
- [ ] Turn off **Improve Siri & Dictation**

Disable **Personalized Ads** if you don't want targeted ads. Select **Apple Advertising**

- [ ] Turn off **Personalized Ads**

**App Privacy Report** is a built-in tool that allows you to see which permissions your apps are using. Select **App Privacy Report**:

- [x] Select **Turn On App Privacy Report**

[Lockdown Mode](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) is a security setting you can enable to make your phone more resistant to attacks. Be aware that certain apps and features [won't work](https://support.apple.com/en-us/HT212650) as they do normally.

- [x] Select **Turn On Lockdown Mode**

## 其它建議

### E2EE 通話

通過電信運營商使用“電話”應用程式撥打的一般電話不是 E2EE。 Both FaceTime Video and FaceTime Audio calls are E2EE, or you can use [another app](../real-time-communication.md) like Signal.

### Avoid Jailbreaking

Jailbreaking an iPhone undermines its security and makes you vulnerable. Running untrusted, third-party software could cause your device to be infected with malware.

### 加密的 iMessage

The color of the message bubble in the Messages app indicates whether your messages are E2EE or not. A blue bubble indicates that you're using iMessage with E2EE, while a green bubble indicates they're using the outdated SMS and MMS protocols. Currently, the only way to get E2EE in Messages is for both parties to be using iMessage on Apple devices.

If either you or your messaging partner have iCloud Backup enabled without Advanced Data Protection, the encryption key will be stored on Apple's servers, meaning they can access your messages. Additionally, iMessage's key exchange is not as secure as alternative implementations, like Signal (which allows you to view the recipients key and verify by QR code), so it shouldn't be relied on for particularly sensitive communications.

### Blacking Out Faces/Information

If you need to hide information in a photo, you can use Apple's built-in tools to do so. Open the photo you want to edit, press edit in the top right corner of the screen, then press the markup symbol at the top right. Press the plus at the bottom right of the screen, then press the rectangle icon. Now, you can place a rectangle anywhere on the image. Make sure to press the shape icon at the bottom left and select the filled-in rectangle. **Don't** use the highlighter to obfuscate information, because its opacity is not quite 100%.

### iOS Betas

Apple always makes beta versions of iOS available early for those that wish to help find and report bugs. We don't recommend installing beta software on your phone. Beta releases are potentially unstable and could have undiscovered security vulnerabilities.

## 安全重點

### Before First Unlock

If your threat model includes forensic tools and you want to minimize the chance of exploits being used to access your phone, you should restart your device frequently. The state *after* a reboot but *before* unlocking your device is referred to as "Before First Unlock" (BFU), and when your device is in that state it makes it [significantly more difficult](https://belkasoft.com/checkm8_glossary) for forensic tools to exploit vulnerabilities to access your data. This BFU state allows you to receive notifications for calls, texts, and alarms, but most of the data on your device is still encrypted and inaccessible. This can be impractical, so consider whether these trade-offs make sense for your situation.
