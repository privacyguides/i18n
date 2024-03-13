---
title: iOS Overview
icon: simple/apple
description: iOS is a mobile operating system developed by Apple for the iPhone.
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

蘋果在 iOS 適當匿名遙測上常發生問題。 [In 2019](https://theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings), Apple was found to transmit Siri recordings—some containing highly confidential information—to their servers for manual review by third-party contractors. While they temporarily stopped that program after that practice was [widely reported on](https://theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana), the problem wasn't completely resolved [until 2021](https://theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance).

最近，人們發現 Apple [即使禁用分析共享， iOS 也會傳輸分析數據 ](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) ，儘管宣稱已匿名處理，這些數據[似乎](https://twitter.com/mysk_co/status/1594515229915979776)很容易連結到唯一的 iCloud 帳戶標識符。

## 建議配置

### iCloud

Apple 產品的大多數隱私和安全問題與其雲服務有關，而不是其硬體或軟體。 當使用 iCloud 等 Apple 服務時，大部分資訊都存儲在他們的伺服器上以密鑰保護，且預設情況下 Apple 可以取用該密鑰。 您可以查看 [Apple 文檔](https://support.apple.com/HT202303)，了解哪些服務是端到端加密的。 任何列為“傳輸中”或“伺服器上”的內容都意味著 Apple 可以在未經您許可下訪問存取該資料。 這種訪問級別偶爾會被執法部門濫用，儘管您的資料在設備上還是安全加密的狀態。當然，Apple 與任何其他公司一樣容易遭受資料洩露。

因此，如果使用 iCloud，則應[啟用**進階資料保護**](https://support.apple.com/HT212520)。 這會使用存儲在您設備上的的密鑰對 iCloud 數據加密（端到端加密）而不是放在 Apple 伺服器的密鑰，以便 iCloud 在發生數據洩露時得到保護，且不會被 Apple 發現。

進階資料保護所用的加密法雖然強大，但[仍然*比不上*](https://discuss.privacyguides.net/t/apple-advances-user-security-with-powerful-new-data-protections/10778/4)其他[雲服務](../cloud.md)的加密，特別是涉及到 iCloud Drive 時。 雖然我們強烈建議在使用 iCloud 時使用進階資料保護，但我們也建議考慮從更加[注重隱私的服務提供商](../tools.md)尋找 iCloud 的替代品，儘管 大多數人不太可能受到這些加密怪癖的影響。

您也可以先限制同步到 iCloud 的內容來保護您的資料。 在「 **設定** 」應用程式的頂部，如果您已登入 iCloud ，便會看到您的姓名和個人資料相片。 選擇該選項，然後選擇 **iCloud**，然後關閉您不想同步到 iCloud 的任何服務的交換機。 如果第三方應用程式與 iCloud 同步，您可能會看到列在「 **顯示全部** 」下的第三方應用程式，您可以在此處停用這些應用程式。

#### iCloud+

付費 **iCloud+** 訂閱（任何 iCloud 存儲方案）附帶一些隱私保護功能。 雖然這些可能為當前 iCloud 客戶提供足夠服務，但我們不建議通過 [VPN](../vpn.md) 購買 iCloud 方案， [獨立電子郵件別名服務](../email.md#email-aliasing-services)僅用在這些功能。

**Private Relay** 為代理服務，通過兩台伺服器中繼 Safari 流量：一台由 Apple 擁有，另一台由第三方提供商（包括 Akamai、Cloudflare 和 Fastly）擁有 ）。 理論上這應該可以防止鏈中的任何單一提供商（包括 Apple）完全了解您連線訪問的網站。 與完整的 VPN 不同，Private Relay 不會保護 Safari 以外其它應用程式的流量。

**Hide My Email** 是 Apple 電子郵件別名服務。 當您在網站或應用程式上*使用 Apple 登錄*時，您可以免費創建電子郵件別名，或者通過付費 iCloud+ 方案生成無數的別名。 Hide My Email 的優點是使用 `@icloud.com` 域作為其別名，與其他電子郵件別名服務相比，它可能不太可能被阻止，但不提供獨立服務提供的功能，例如 例如自動 PGP 加密或多郵箱支持。

#### 媒體 & 購買項目

在「 **設定** 」應用程式的頂部，如果您已登入 Apple ID，便會看到您的姓名和個人資料相片。 選擇該項，然後選擇**媒體 & 購買** > **查看帳戶**。

- [ ] 關閉 **個人化推薦**

#### Find My

**Find My(尋找我的iPhone)** 是一項服務，可讓您跟踪您的 Apple 設備並與朋友和家人分享您的位置。 若設備遭竊，它可以讓您從遠端進行抺除，從而防止小偷訪問您的資料。 Your Find My [location data is E2EE](https://apple.com/legal/privacy/data/en/find-my) when:

- 您的位置已與家人或朋友共享，並且都使用 iOS 15 或更高版本。
- 設備處於離線狀態，且由Find My 網路找到。

設備有連線且遠程使用“尋找 iPhone”來定位您的設備，則位置資料不是 E2EE。 您必須決定權衡是否值得激活防盜鎖。

在「 **設定** 」應用程式的頂部，如果您已登入 Apple ID，便會看到您的姓名和個人資料相片。 選取這項然後再選 **尋找**。 此處您可以選擇是否啟用或禁用“查找設備”功能。

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

預設情況中，您的 iPhone 設備名稱將包含您的名字，所連接的網絡中的其它人都可以看到該名稱。 所以應該將其更改為更一般的名稱，例如“iPhone”。 選擇 **關於** > **名稱** ，然後輸入您喜歡的裝置名稱。

經常安裝 **軟體更新** 以獲得最新的安全修復非常重要。 您可以啟用 **自動更新** ，以保持手機最新，而無需不斷檢查更新。 選擇 **軟體更新** > **自動更新**：

- [x] 打開 **下載 iOS 更新**
- [x] 打開 **安裝 iOS 更新**
- [x] 打開 **安全應變 & 系統檔**

**AirDrop** 可以輕鬆傳輸檔案，但它可能允許陌生人對您發送不想要的檔案。

- [x] 選擇 **AirDrop** > **關閉接收**

**AirPlay** 可讓您將內容從 iPhone 無縫串流到電視； 然而，您可能並不會想要一直維持這樣。 選擇 **AirPlay & 關閉** > **自動串流 AirPlay 到 TVs**:

- [x] 選擇 **絕不** 或 **詢問**

**背景 App 重新整理**可將應用程式在不使用時刷新其內容。 這可能會導致它們建立不必要的連接。 關閉此功能還可節省電池壽命，但可能會影響應用程式接收更新資訊的能力，特別是天氣和消息傳遞的應用。

選擇 **背景 App 重新整理** 並切掉無需在背景下繼續刷新的應用。 若不想讓任何 apps 在背景刷新，可再次選擇 **背景 App 重新整理** 並將其 **關閉**。

#### Siri & 尋找

如果不希望任何人在鎖定時使用 Siri 控制您的手機，可以在此處將其關閉。

- [ ] 關閉 **畫面鎖住時可使用 Siri **

#### Face ID/Touch ID & 密碼

在手機上設置強密碼是確保設備物理安全的最重要步驟。 您必須權衡安全性與便利性：每次輸入較長的密碼很麻煩，但較短的密碼或 PIN 碼很容易被猜到。 設置 Face ID 或 Touch ID 以及強密碼可以在可用性和安全性之間實現良好折衷。

選擇 **打開 Passcode ** 或 **更改 Passcode** > **Passcode 選項** > **自定 字母數字密碼**. Make sure that you create a [secure password](../basics/passwords-overview.md).

如果想使用 Face ID 或 Touch ID，可以立即進行設置。 您的手機將使用之前設置的密碼作為後備密碼，以防生物識別驗證失敗。 生物識別解鎖方法主要是便利，雖然它們確實可以阻止監控攝像頭或身旁的人看到您所輸入的密碼。

如果使用生物識別技術，應該知道如何在緊急情況下快速關閉它們。 按住側面按鈕或電源按鈕以及*任一*音量按鈕，直到看到滑動關閉滑塊為止，這將禁用生物識別功能，需要密碼才能解鎖。 設備重新啟動後還需要您的密碼。

在某些較舊的設備上，可能需要按電源按鈕五次才能禁用生物識別功能，或者具有 Touch ID 的設備，可能只需按住電源按鈕即可。 請事先嘗試此操作，以便知道哪種方法適用您的設備。

**被盜資料保護**是iOS 17.3 的新功能，增加了額外的安全性，當設備在解鎖時被盜時保護您的個人資料。 如在 Apple ID 設定中使用生物辨識技術和「尋找我的裝置」功能，我們建議啟用此新保護：

- [x] 選擇**開啟保護**

After enabling stolen data protection, [certain actions](https://support.apple.com/HT212510) will require biometric authentication without a password fallback (in the event that a shoulder surfer has obtained your PIN), such as using password autofill, accessing payment information, and disabling lost mode. 它還可以在住處或其他「熟悉位置」以外的地點執行的某些操作增加安全延遲，例如需要 1 小時計時器來重設 Apple ID 密碼或退出 Apple ID。 此延遲是為了有時間啟用遺失模式並在小偷重置設備前保護好您的帳戶。

**鎖定時允許存取** 提供您在手機鎖定時可以允許的選項。 禁用的這些選項越多，沒有密碼者可做的事情就越少，但對您來說也就更不方便。 選擇不希望其他人接觸您的手機後訪問其中哪些內容。

- [ ] 關閉 **今日檢視與搜尋**
- [ ] 關閉 **通知中心**
- [ ] 關閉**控制中心**
- [ ] 關閉 **鎖定畫面小工具**
- [] 關閉 **Siri**
- [ ] 關閉 **以 Message 回覆**
- [] 關閉 **共享家庭控制權**
- [] 關閉 **錢包**
- [ ] 關閉**回覆漏接來電**
- [ ] 關閉 **USB 配件**

iPhone 可以抵禦暴力攻擊，在多次嘗試失敗後，需要等待很長時間； 然而，過去已經有一些漏洞可以繞開這個問題。 為了更加安全，可將手機設置為在 10 次密碼嘗試錯誤後自行擦除。

<div class="admonition warning" markdown>
<p class="admonition-title">Warning "警告"</p>

啟用此設置後，別人可以通過多次輸入錯誤密碼來故意擦除您的手機。 確保有適當備份，並且僅在有把握的情況下才啟用此設置。

</div>

- [x] 打開 **清除資料**

#### 隱私

**定位服務**可用在“尋找”和“地圖”等功能。 如果不需要這些功能，可以禁用定位服務。 或者，可以在此處查看並選擇哪些應用程式可以使用您的位置資訊。 選擇 **位置服務**:

- [ ] 關閉 **定位服務**

您在此處決定是否讓 apps  **追蹤**活動。 關閉此功能可禁止所有應用程序利用手機的廣告 ID 進行跟踪。 選擇 **追蹤**:

- [ ] 關閉 **App 追蹤活動請求k**

如果不想加入，請關閉 **感應 & 使用資料研究** 。 選擇 **感應 & 使用資料研究**:

- [ ] 關閉 **感應器 & 使用資料收集**

**安全檢查**可讓您快速查看和撤銷可能有權訪問您資料的某些人員和應用。 您可以在此執行**緊急重置**，立即重置可能有權訪問設備資源的所有人員和應用之權限，且** 管理共享& 訪問權限**允許您查看並自行決定有權訪問設備和帳戶資源的人員和內容。

如不想發送 Apple 使用資料，應該禁用該分析。 選擇**分析& 改進**：

- [ ] 關閉**共享 iPhone Analytics** 或**共享 iPhone & 觀看分析**
- [ ] 關閉 **分享 iCloud 數據分析**
- [ ] 關閉 **改善 Fitness+**
- [ ] 關閉 **安全改進**
- [ ] 關閉 **改善 Siri & 偵測**

關閉 **個人化廣告** 如不願加入針對式行銷。 選擇 **Apple 廣告**

- [ ] 關閉 **個人化的廣告**

**應用程序隱私報告**為內置工具，可讓您查看應用程式使用哪些權限。 選取 **App 隱私報告t**:

- [x] 選擇 **開啟 App 隱私報告**

[封閉模式](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode)是可以啟用的安全設置使手機更能抵抗攻擊。 Be aware that certain apps and features [won't work](https://support.apple.com/HT212650) as they do normally.

- [x] 選擇 **打開封閉模式**

## 其它建議

### E2EE 通話

通過電信運營商使用“電話”應用程式撥打的一般電話不是 E2EE。 FaceTime 的影像語音通話都是 E2EE，或是也可使用 [其他應用](../real-time-communication.md)，例如 Signal。

### 避免 iOS越獄

iPhone 越獄會破壞其安全性更容易受到攻擊。 運行不可信任的第三方軟體可能會導致設備感染惡意軟體。

### 加密的 iMessage

Messages 應用程式中訊息氣泡的顏色指示該訊息是否為 E2EE。 藍色氣泡表示您正將 iMessage 與 E2EE 結合使用，而綠色氣泡表示他們正在使用過時的 SMS 和 MMS 協議。 要在 Messages 中實現 E2EE ，目前唯一方法只有雙方都在 Apple 設備上使用 iMessage。

如果您或您的訊息傳遞夥伴在沒有進階資料保護下啟用 iCloud 備份，則加密密鑰會存儲在 Apple 伺服器，這意味著他們可以訪問您的訊息。 此外，iMessage 的密鑰交換不如 Signal（它允許您查看收件人密鑰並通過 QR 碼進行驗證）等替代方案安全，因此不應依賴它進行敏感內容通訊。

### 塗黑臉孔/資訊

如果想要隱藏照片資訊，可以使用 Apple 內置工具來完成。 打開要編輯的照片，按螢幕右上角的編輯，然後按右上角的標記符號。 按螢幕右下角的加號，然後按矩形圖標。 現在，可以在圖像的任何位置放置一個矩形。 確保按左下角的形狀圖標並選擇填充矩形。 **不要**使用亮光筆來混淆資訊，因為它的不透明度並非 100%。

### iOS Betas

Apple 會為那些希望幫助查找和報告錯誤的人先提供 iOS 測試版。 不建議在手機上安裝測試版軟體。 Beta 版本不夠穩定，可能存在未被發現的安全漏洞。

## 安全重點

### Before First Unlock(初次解鎖之前)

如果您的威脅模型包含鑑識工具，且希望最大程度地減少他人利用漏洞訪問手機的可能性，則應經常重新啟動設備。 重啟後**解鎖設備**之前的狀態稱為“首次解鎖之前”(BFU) ，當設備處於該狀態時，取證鑑識工具[明顯更加困難](https://belkasoft.com/checkm8_glossary)利用漏洞訪問您的資料。 此 BFU 狀態允許您接收電話、簡訊和鬧鐘通知，但設備上的大部分資料為加密且無法訪問。 這可能不切實際，因此請考慮權衡這個作法對於自身情況是否有意義。
