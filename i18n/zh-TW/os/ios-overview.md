---
title: iOS 概述
icon: simple/apple
description: 蘋果公司使用 Unix 作業系統來開發macOS 支援自家的 Mac 電腦。
---

**iOS** 和 **iPadOS** 是 Apple 分別為其 iPhone 和 iPad 產品開發的專有移動作業系統。 如果您擁有 Apple 行動裝置，可透過關閉某些內建遙測功能以及強化系統內建的隱私和安全設定來加強隱私。

## 隱私筆記

iOS 設備因其強大的資料保護和對現代最佳作法的遵守而受到安全專家的讚揚。 然而，Apple 生態系統的限制性——尤其是行動裝置——仍然在很多方面阻礙了隱私。

我們認為，與任何製造商的庫存 Android 設備相比，iOS 為大多數人提供了水平之上的隱私和安全保護。 不過，如果您想要，或有需要完全不使用 Apple 或 Google 的雲端服務，還可以使用諸如 GrapheneOS 等[客製的 Android 作業系統](../android/distributions.md)，來達到更高的隱私保護標準。

### 激活鎖

所有 iOS 設備在初始設定或重置時都必須根據 Apple 的激活鎖伺服器進行檢查，這意味著**需要**網際網路連接才能使用 iOS 設備。

### 強制的 App Store

iOS 上唯一的應用程式來源是 Apple 的 App Store，需要有 Apple 帳號才能使用。 這意味著 Apple 擁有您在設備上安裝的每個應用記錄，且如果向 App Store 提供付款方式，則可能會將該資訊與您的實際身份聯繫起來。

### 侵入式遙測

在 iOS 上，Apple 在適當地將遙測功能與 Apple 帳號取消關聯上一直都有問題。 [2019 年](https://theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings)，Apple 被發現將 Siri 錄音（其中一些包含高度機密資訊）傳輸回其伺服器，以供第三方承包商進行手動審核。 儘管在此作法被[廣泛報導](https://theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana)之後，Apple 已停止該計畫，而該公司也在幾個月後，於後續的 iOS 更新當中推出了一組開關，讓使用者能

**選擇退出**上傳對話給 Siri。 此外，在 2021 年，[Apple 重新修改了 Siri](https://theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance)，使其在本機處理語音記錄，不再傳送至伺服器中。</p> 

最近，人們發現[就算關閉分享使用分析資料](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558)，iOS 也還是會傳輸出去。儘管這些資料應該已進行匿名化處理，不再與 Apple 帳號相關，但這些資料[似乎](https://twitter.com/mysk_co/status/1594515229915979776)還是很容易連結到唯一的 iCloud 帳號識別碼。



### 使用中的 VPN 連線以外的流量

Apple 的[隱私權政策](https://apple.com/legal/privacy/data/en/vpns)針對 VPN 有下列描述：



> 即使已開啟 VPN，一些必要的系統服務流量仍會在 VPN 外部進行，以讓您的裝置能夠正常運作。



## 建議的設定

**註：**本指南假設您使用的是最新版本的 iOS。



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

如果您有登入 Apple 帳號，在**設定**應用程式的頂端，會看到姓名和個人檔案圖片。 選取該項目，然後選擇**媒體與購買項目**→**檢視帳號**。

- [ ] 關閉 **個人化推薦**



#### Find My

**Find My(尋找我的iPhone)** 是一項服務，可讓您跟踪您的 Apple 設備並與朋友和家人分享您的位置。 若設備遭竊，它可以讓您從遠端進行抺除，從而防止小偷訪問您的資料。 在以下情況，「尋找我的」[位置資料為 E2EE](https://apple.com/legal/privacy/data/en/find-my)：

- 您的位置已與家人或朋友共享，並且都使用 iOS 17 或更高版本。
- 設備處於離線狀態，且由Find My 網路找到。

設備有連線且遠程使用“尋找 iPhone”來定位您的設備，則位置資料不是 E2EE。 您必須決定權衡是否值得激活防盜鎖。

在 **設定** 應用程式的頂端，如果您登入了 Apple 帳戶，您會看到您的姓名和個人檔案圖片。 選取這項然後再選 **尋找**。 此處您可以選擇是否啟用或禁用“尋找設備”功能。



### 設定

許多其他與隱私相關的設定可以在**設定**應用中找到。



#### 飛航模式

啟用 **飛航模式** 會阻止您的手機與手機基地塔連線。 您仍然可以連接到 Wi-Fi 和藍牙，因此每當您連接到 Wi-Fi 時，您都可以開啟此設定。



#### Wi-Fi

您可以啟用[硬體位址隨機化](https://support.apple.com/en-us/102509#triswitch)，以保護您不會受到跨 Wi-Fi 網路追蹤，以及在同一個網路中長時間被追蹤。 在目前連線的網路中，點選 :material-information: 按鈕：

- [x] 將**專用 Wi-Fi 位址**設定為**固定**或**輪替**

您也可以選擇 **限制 IP 位址追蹤**。 這與 iCloud Private Relay 類似，但僅影響與“已知跟踪器”的連接。 因為它只影響與潛在惡意伺服器的連接，所以啟用此設定應該沒問題，但如果不希望*任何*流量通過 Apple 的伺服器路由，則可把它關掉。



#### 藍牙

**當您不使用藍牙時，應停用藍牙** ，因為它會增加您被攻擊的機會。 透過控制中心停用藍牙（或 Wi-Fi ）只會暫時停用：您必須在「設定」中關閉藍牙才能保持有效。

- [ ] 關閉 **藍牙**

請注意，每次系統更新後或自動開啟藍牙。



#### 一般設定

預設情況中，您的 iPhone 裝置名稱將包含您的名字，所連接的網路中的其它人都可以看到該名稱。 所以應該將其更改為更一般的名稱，例如“iPhone”。 選擇**關於** → **名稱** ，然後輸入您想要使用的裝置名稱。

It is important to install software updates frequently to get the latest security fixes. You can enable automatic updates to keep your phone up-to-date without needing to constantly check for updates. 選擇**軟體更新**→**自動更新**：

- [x] Turn on **Automatically Install**

**AirDrop** 常被用來分享檔案，但也代表可能有重大的安全性風險。 AirDrop 通訊協定會不斷向周遭環境廣播您的個人資訊，雖有安全防護但[非常薄弱](https://usenix.org/system/files/sec21-heinrich.pdf)。 就是算資源受限的攻擊者，也能輕鬆找出您的身分；中國政府自 2022 年起也[公開承認](https://arstechnica.com/security/2024/01/hackers-can-id-unique-apple-airdrop-users-chinese-authorities-claim-to-do-just-that)使用該技術於公開場所識別 AirDrop 使用者。

- [x] 選取 **AirDrop**→**關閉接收**

**AirPlay** 可讓您將內容從 iPhone 無縫串流到電視； 然而，您可能並不會想要一直維持這樣。 選擇 **AirPlay 與接續互通**→**自動 AirPlay**：

- [x] 選擇 **永不** 或 **詢問**

**背景 App 重新整理**可將應用程式在不使用時刷新其內容。 這可能會導致它們建立不必要的連接。 關閉此功能還可節省電池壽命，但可能會影響應用程式接收更新資訊的能力，特別是天氣和訊息軟體。

選擇 **背景 App 重新整理** 並切掉無需在背景下繼續刷新的應用。 若不想讓任何 apps 在背景刷新，可再次選擇 **背景 App 重新整理** 並將其 **關閉**。



#### Apple Intelligence 與 Siri

This is available if your device supports **[Apple Intelligence](https://support.apple.com/guide/iphone/apple-intelligence-and-privacy-iphe3f499e0e/ios)**. Apple Intelligence uses a combination of on-device processing and their **[Private Cloud Compute](https://security.apple.com/blog/private-cloud-compute)** for things that take more processing power than your device can provide.

To see a report of all the requests made to Apple's servers, you can navigate to **Privacy & Security** → **Apple Intelligence Report** and press **Export Activity** to see activity from the either the last 15 minutes or 7 days, depending on what you set it for. 與會顯示您手機上的應用程式近期存取的權限的**應用程式隱私權報告**類似，Apple Intelligence 報告也會顯示使用 Apple Intelligence 時，有哪些資料被送到 Apple 的伺服器。

Apple Intelligence can integrate with [ChatGPT](https://support.apple.com/guide/iphone/use-chatgpt-with-apple-intelligence-iph00fd3c8c2/ios). If you want ChatGPT integration, you can navigate to **ChatGPT** and press **Set Up**. If you want to disable it, go to the same place:

- [ ] 關閉 **使用 ChatGPT**

如果您維持開啟 ChatGPT 整合功能，也可以讓它每次都要求確認：

- [x] 開啟**確認請求**

如果不希望任何人在鎖定時使用 Siri 控制您的手機，可以在此處將其關閉。

- [ ] 關閉 **畫面鎖住時可使用 Siri**



#### Face ID/Touch ID & 密碼

在手機上設定強密碼是確保設備物理安全的最重要步驟。 您必須權衡安全性與方便性：輸入夠長、夠亂的密碼很麻煩，但密碼如果太短，或只使用 PIN 碼卻又容易被猜到。 設定 Face ID 或 Touch ID 以及強密碼可以在可用性和安全性之間實現良好折衷。

選擇**開啟密碼**或**更改密碼**→**密碼選項**→**自訂英數密碼**。 確認建立[安全密碼](../basics/passwords-overview.md)。

如果想使用 Face ID 或 Touch ID，可以立即進行設定。 您的手機將使用之前設定的密碼作為後備密碼，以防生物識別驗證失敗。 生物識別解鎖方法主要是便利，雖然它們確實可以阻止監控攝像頭或身旁的人看到您所輸入的密碼。

如果使用生物識別技術，應該知道如何在緊急情況下快速關閉它們。 Holding down the [side button](https://support.apple.com/en-us/105103) and *either* volume button until you see the Slide to Power Off slider will disable biometrics, requiring your passcode to unlock. Your passcode will be required after your device restarts.

You can similarly disable biometrics by pressing the side button five times, or for devices with Touch ID, you can hold down the side button and nothing else. 請務必先試著操作一下，這樣才知道您的裝置需使用哪種方法關閉。

**遭竊裝置防護**能增加安全性，萬一裝置在解鎖時被偷走，可保護您的個人資料。 If you enable both biometric authentication and the [Find My](#find-my) iPhone feature, we recommend enabling this protection:

- [x] Turn on **Stolen Device Protection**

啟用被盜設備保護後，[某些操作](https://support.apple.com/HT212510)將需要生物識別身份驗證，無需密碼回退（如果駭客准竊盜已獲得您的 PIN），例如使用密碼自動填寫功能就可訪問支付資訊並關閉遺失模式。 它還可以針對在住家或其他「熟悉位置」以外的地點執行的某些操作加入安全延遲，例如需要 1 小時來重設 Apple 帳號的密碼，或登出 Apple 帳號。 此延遲是為了有時間啟用遺失模式並在小偷重置設備前保護好您的帳戶。

**Allow Access When Locked** presents options for what you can allow when your phone is locked. Pick and choose which feature you want to disable to prevent unauthorized access if someone gets their hands on your phone. 禁用的這些選項越多，沒有密碼者可做的事情就越少，但對您來說也就更不方便。

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
- [ ] 關閉**路線與交通量**
- [ ] 關閉**改進地圖**

您在此處決定是否讓 apps **追蹤** 活動。 關閉此功能可禁止所有應用程式利用手機的廣告 ID 進行跟踪。 選擇 **追蹤**:

- [ ] 關閉 **允許 App 發出追蹤請求**

如果使用者未滿 18 歲，該選項預設停用且無法變更。

如果不想加入，請關閉 **感應 & 使用資料研究** 。 選擇 **感應 & 使用資料研究**:

- [ ] 關閉 **感應器 & 使用資料收集**

**[Safety Check](https://support.apple.com/guide/personal-safety/safety-check-iphone-ios-16-ips2aad835e1/1.0/web/1.0)** allows you to quickly view and revoke certain people and apps that might have permission to access your data. Here, you can perform an **Emergency Reset**, immediately resetting permissions for all people and apps which might have access to device resources. You can also **Manage Sharing & Access**, which allows you to review and customize who and what has access to your device and account resources. If you're in an abusive situation, read Apple's [Personal Safety User Guide](https://support.apple.com/guide/personal-safety/welcome/web) for guidance on what you should do.

You should disable analytics if you don't wish to send usage data to Apple. Select **Analytics & Improvements** and unselect the type(s) of analytics that you don't want to send to Apple.

關閉 **個人化廣告** 如不願加入針對式行銷。 選擇 **Apple 廣告**:

- [ ] 關閉 **個人化廣告**

**App 隱私權報告**為內建工具，可讓您查看應用程式使用哪些權限。 選取 **App 隱私權報告**:

- [x] 選擇 **開啟 App 隱私權報告**

Set wired accessories to ask for permission when you connect them. Select **Wired Accessories**:

- [x] Select **Always Ask** or **Ask for New Accessories**

**[Lockdown Mode](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode)** is a security setting you can enable to make your phone more resistant to attacks. 請注意，某些應用和功能[將無法正常運作](https://support.apple.com/HT212650)。

- [x] 選擇 **開啟封閉模式**



## 其它建議



### E2EE 通話

通過電信運營商使用“電話”應用程式撥打的一般電話不是 E2EE。 FaceTime 視訊和語音通話都有 E2EE 加密。 此外，您也可以使用 Signal 等[其他應用程式](../real-time-communication.md)進行有 E2EE 加密的通話。



### 加密的 iMessage

可從訊息應用程式中，[訊息氣泡的顏色](https://support.apple.com/en-us/104972)該訊息是否經過 E2EE 加密。 藍色氣泡代表您使用的是有 E2EE 加密的 iMessage，而綠色氣泡表示對方正在使用過時的 SMS、MMS 通訊協定或 RCS。 iOS 上的 RCS **未經** E2EE 加密。 目前在 Apple 裝置的訊息應用程式中，唯一能夠以 E2EE 加密傳送訊息的方式，就是雙方都使用 iMessage。

如果您或您的訊息傳遞夥伴在沒有進階資料保護下啟用 iCloud 備份，則加密金鑰會儲存在 Apple 伺服器，這意味著他們可以訪問您的訊息。

By default, you trust Apple's identity servers that you're messaging the right person. To defend yourself from a potentially malicious server, you can enable **[Contact Key Verification](https://support.apple.com/en-us/118246)**. At the top of the **Settings** app where your name is, select it, then go to **Contact Key Verification**.

- [x] Turn on **Verification in iMessage**

Both you and your contacts need to enable Contact Key Verification and follow Apple's [instructions](https://support.apple.com/en-us/118246#verify) for the security assurances mentioned above to take effect.



### 照片權限

當應用程式提示您要存取裝置的照片圖庫時，iOS 會提供您限制應用程式存取內容的選項。

與其讓應用程式能夠存取裝置上的所有照片，您可以點擊權限對話框中的「選擇照片…」選項，讓應用程式只能存取您選擇的照片。 您可以隨時到**設定**→**隱私權與安全性**→**照片**，以變更照片存取權限。

![照片權限](../assets/img/ios/photo-permissions-light.png#only-light) ![照片權限](../assets/img/ios/photo-permissions-dark.png#only-dark)

**只新增照片**是一種只允許應用程式將照片加入圖庫的權限。 並非所有要求存取照片圖庫的應用程式，都提供此選項。

![私人存取](../assets/img/ios/private-access-light.png#only-light) ![私人存取](../assets/img/ios/private-access-dark.png#only-dark)

某些應用程式也支援**私人存取**權限，其功能與「**有限存取**」權限類似。 不過，使用「私人存取」功能分享給應用程式的照片，預設會包含其位置。 如果您不事先[移除照片後設資料](../data-redaction.md)，我們建議您取消勾選此選項。



### 聯絡人權限

同樣地，與其讓應用程式能存取裝置上儲存的所有聯絡人，您可以讓它只存取您選擇的聯絡人。 您可以隨時到**設定**→**隱私權與安全性**→**聯絡人**變更聯絡人的存取權限。

![聯絡人權限](../assets/img/ios/contact-permissions-light.png#only-light) ![聯絡人權限](../assets/img/ios/contact-permissions-dark.png#only-dark)



### 要求生物特徵驗證和隱藏應用程式

iOS 提供以 Touch ID/Face ID 或您的密碼來鎖定大部分應用程式的功能，這對於保護本身未提供相關功能的應用程式當中的敏感內容非常有用。 您可以長按應用程式，選擇**需要 Face ID/Touch ID** 來鎖定該應用程式。 開啟以這種方式鎖定的應用程式之前，或是從其他程式存取資料前，將要求進行生物特徵驗證。 此外，被鎖定的應用程式，也不會顯示通知預覽。

除了以生物特徵鎖定外，您也可以隱藏應用程式，讓它們不會出現在主畫面、應用程式庫、**設定**中的應用程式清單等。 雖然隱藏應用程式在您必須將已解鎖的手機交給他人的情況下可能很有用，但該功能提供的隱藏效果並非絕對，因為隱藏的應用程式在某些地方（例如電量使用清單）仍是可見的。 此外，隱藏應用程式的一個顯著缺點是您將不會收到任何通知。

您可以長按應用程式，然後選擇**要求使用 Face ID/Touch ID**→**隱藏並要求使用 Face ID/Touch ID** 來隱藏應用程式。 請注意，無法隱藏 Apple 內建的應用程式、預設網頁瀏覽器和電子郵件應用程式。 隱藏的應用程式位於應用程式庫底部的**隱藏**資料夾，可使用生物特徵解鎖。 無論您是否隱藏應用程式，此資料夾都會出現在應用程式庫中，這可提供一定程度的合理推諉。



### Guided Access

Sometimes you might want to hand your phone to someone to make a call or do a specific task, but you don't want them to have full access to your phone. In these cases, you can quickly enable **[Guided Access](https://support.apple.com/guide/iphone/lock-iphone-to-one-app-iph7fad0d10/ios)** to lock the phone to one specific app until you authenticate.

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Guided Access isn't foolproof, as it's possible you could leak data unintentionally or the feature could be bypassed. You should only use Guided Access for situations where you casually hand your phone to someone to use. You should not use it as a tool to protect against advanced adversaries.

</div>

### 隱藏圖片中的元素

如果想隱藏照片中的資訊，可以使用 Apple 內建的編輯工具。

You can use the [Clean Up](https://support.apple.com/en-us/121429) feature on supported devices to pixelate faces or remove objects from images.

- 開啟**「照片」**應用程式，點擊您想要調整的照片
- Tap the :material-tune:
- 點擊標示**清除**的按鈕
- 圈選想要刪減的內容。 臉部會被打馬，其他東西將被清除。

我們[針對將文字模糊化的](../data-redaction.md)警告也適用於此，所以建議改為加入不透明度為 100% 的黑色形狀。 除了刪除文字之外，您也可以使用「**照片**」應用程式，將任何臉部或物件塗黑。

<div class="annotate" markdown>

- Tap the image you have selected for redaction
- Tap the :material-tune: → :material-dots-horizontal: (1) → Markup → :material-plus:
- Select **Add Shape** and choose the square or circle
- On the toolbar, tap the circle and choose black as the color for filling in the shape. 您也可以移動圖形，視情況放大。

</div>

1. This may not appear on certain iPhone models.

**不要**使用螢光筆來隱藏資訊，因為它並非完全不透明。



### 避免 iOS越獄

iPhone 越獄會破壞其安全性更容易受到攻擊。 運行不可信任的第三方軟體可能會導致設備感染惡意軟體。



### iOS Betas

Apple 會為那些希望幫助查找和報告錯誤的人先提供 iOS 測試版。 不建議在手機上安裝測試版軟體。 Beta 版本不夠穩定，可能存在未被發現的安全漏洞。



## 安全重點



### Before First Unlock(初次解鎖之前)

如果您的威脅模式包含鑑識工具的[:material-target-account: 針對式攻擊](../basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}，而且您希望盡可能降低被利用漏洞來存取手機的機會，請經常重新啟動裝置。 重啟後**解鎖設備**之前的狀態稱為“首次解鎖之前”(BFU) ，當設備處於該狀態時，取證鑑識工具[明顯更加困難](https://belkasoft.com/checkm8_glossary)利用漏洞訪問您的資料。 此 BFU 狀態允許您接收電話、簡訊和鬧鐘通知，但設備上的大部分資料為加密且無法訪問。 這可能不切實際，因此請考慮權衡這個作法對於自身情況是否有意義。

iPhones [automatically reboot](https://support.apple.com/guide/security/protecting-user-data-in-the-face-of-attack-secf5549a4f5/1/web/1#:~:text=On%20an%20iPhone%20or%20iPad%20with%20iOS%2018%20and%20iPadOS%2018%20or%20later%2C%20a%20new%20security%20protection%20will%20restart%20devices%20if%20they%20remain%20locked%20for%20a%20prolonged%20period%20of%20time.) if they're not unlocked after a period of time.



### MTE

The iPhone 17 line and later offer a security enhancement called [Memory Tagging Extension](https://developer.arm.com/documentation/108035/0100/Introduction-to-the-Memory-Tagging-Extension) (MTE), which makes it significantly harder for an attacker to exploit memory corruption vulnerabilities. This always-on protection depends on hardware support, so it's not available for older devices.

For more details on Apple's implementation of MTE, read the [blog post](https://security.apple.com/blog/memory-integrity-enforcement) published by Apple Security Research. We also cover Apple's implementation of MTE and how it compares to Android's implementation in the Google Pixel 8 series and later in our [own article](https://www.privacyguides.org/posts/2025/09/20/memory-integrity-enforcement-changes-the-game-on-ios).
