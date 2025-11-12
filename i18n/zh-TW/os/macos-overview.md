---
title: macOS 概述
icon: material/apple-finder
description: macOS 是蘋果電腦的桌面作業系統，搭配其自家硬體提供了堅固的安全。
---

蘋果公司使用 Unix 作業系統來開發**macOS** 支援自家的 Mac 電腦。 為提高 macOS 隱私，用戶可關閉遙測功能以強化現有的隱私與安全設定。

舊款的 Intel-based Macs 與 Hackintoshe 則無法完全支援 macOS 所提供的安全功能。 為了加強資料安全性，建議使用[Apple Silicon](https://support.apple.com/HT211814)晶片的新款 Mac。

## 隱私筆記

用戶應考量 一些 macOS 值得關注的隱私問題。 這些涉及作業系統本身，而不是蘋果其他應用程式和服務的問題。

### 激活鎖

全新 Apple Silicon 裝置可不需網際網路連線即可設定。 但是，恢復或重置 Mac 將**需要**連接到 Apple 伺服器，以檢查丟失或被盜設備資料庫的激活鎖。

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

- [ ] 關閉**藍牙**（除非目前正在使用）

#### 網路

取決於您使用的是**Wi-Fi** 還是**以太網**（由綠點和“已連接”顯示） ”），點擊相應的圖標。

單擊網路名稱旁邊的“詳細資訊”按鈕：

- [x] 在**私人 Wi-Fi 位址**下選擇**輪替**

- [x] 開啟**限制 IP 位址追蹤**

##### 防火牆

防火牆會阻止不必要的網路連接。 防火牆設定越嚴格，您的 Mac 就越安全。 然而某些服務可能會被封鎖。 您應該將防火牆配置得盡可能嚴格，但不會影響使用的服務。

- [x] 開啟**防火牆**

點擊 **生成（Generate）** 按鈕。

- [x] 勾選**封鎖所有傳入連線**

如果配置過於嚴格，可以再回來取消勾選此選項。 但如果應用程式請求，macOS 通常會提示用戶允許該應用的傳入連接。

#### 一般設定

您的設備名稱預設為“[您的名字] 的 iMac”。 由於此名稱會[在您的網路上公開廣播](https://support.apple.com/guide/mac-help/change-computers-local-hostname-mac-mchlp2322/26/mac/26#:~:text=The%20local%20hostname%2C%20or%20local%20network%20name%2C%20is%20displayed%20at%20the%20bottom%20of%20the%20Sharing%20settings%20window.%20It%20identifies%20your%20Mac%20to%20Bonjour%2Dcompatible%20services.)，因此需將裝置名稱更改為通用名稱，例如「Mac」。

單擊**關於**，然後在**名稱**欄位上輸入想取的設備名稱。

##### 軟體更新

您應自動安裝所有可用更新，以確保 Mac 具有最新的安全修復。

點擊 :material-information-outline: **自動更新** 旁邊的小圖標:

- [x] 開啟**更新推出時就下載**

- [x] 開啟**安裝 macOS 更新**

- [x] 開啟**安裝安全回應與系統檔案**

#### Apple Intelligence 與 Siri

如果您在 macOS 上不使用這些功能，應該關閉：

- [ ] 關閉 **Apple Intelligence**
- [ ] 關閉 **Siri**

只有在您的裝置支援 **[Apple Intelligence](https://apple.com/legal/privacy/data/en/intelligence-engine)** 時才能使用它。 Apple Intelligence 結合裝置內處理與它們的[私人雲端運算](https://security.apple.com/blog/private-cloud-compute)功能，以處理需要比裝置所能提供還更多處理能力的事情。

若要查閱透過 Apple Intelligence 傳送的所有資料報告，您可以到 **隱私權與安全性** → **Apple Intelligence 報告**，然後按下**匯出活動**，即可查看過去 15 分鐘或 7 天內的活動，視您的設定而定。 與會顯示您手機上的應用程式近期存取的權限的**應用程式隱私權報告**類似，Apple Intelligence 報告也會顯示使用 Apple Intelligence 時，有哪些資料被送到 Apple 的伺服器。

預設情況下，ChatGPT 整合功能是關閉的。 如果您不想再使用 ChatGPT 整合功能了，可以切換到 **ChatGPT**：

- [ ] 關閉 **使用 ChatGPT**

如果您維持開啟 ChatGPT 整合功能，也可以讓它每次都要求確認：

- [x] 開啟**確認請求**

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

使用 ChatGPT 提出的所有請求都會傳送到 ChatGPT 的伺服器，不會在裝置上進行處理，也不會像 Apple Intelligence 般使用私人雲端運算功能。

</div>

#### 隱私 & 安全

每當應用程式請求權限時，它就會顯示在這裡。 您可決定是否允許或拒絕哪些應用程式的特定權限。

##### 定位服務。

您可以個別同意每個應用程式的定位服務權限。 如果不要應用程式使用您的位置，那麼完全關閉定位服務是最私密的選擇。

- [ ] 關閉 **定位服務**

##### 資料分析 & 改進

決定是否要與 Apple 和開發者共享分析資料。

##### Apple 廣告

決定是否依使用狀況個人化廣告接收。

- [ ] 關閉 **個人化廣告**

##### FileVault

在具備 Secure Enclave（Apple T2 安全晶片、Apple Silicon）的現代裝置上，您的資料會一直被加密，只要裝置本身未偵測到資料被竄改，就會透過硬體金鑰自動解密。 開啟 [FileVault](../encryption.md#filevault) 時需要輪入密碼來解密資料，大大提高了安全性，尤其是在關機時或開機後首次登入時。

在較舊的 Intel 的 Mac 電腦，FileVault 是預設唯一可用的磁盤加密形式，應始終啟用。

- [x] 點擊 **開啟**

##### 封閉模式

**[鎖定模式](https://support.apple.com/guide/mac-help/lock-mac-targeted-a-cyberattack-ibrw66f4e191/mac)**會關閉某些功能，以提高安全性。 開啟後，某些應用程式或功能可能無法如常運作。 舉例來說，開啟鎖定模式後，Safari 會停用 JavaScript Just-In-Time（[JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers)）編譯和 [WebAssembly](https://developer.mozilla.org/docs/WebAssembly)。 我們建議開啟鎖定模式，看看是否會對日常使用造成重大影響。

- [x] 點擊 **開啟**

### MAC 位址隨機化

macOS 在網路連線中斷而[執行 Wi-Fi 掃描](https://support.apple.com/guide/security/privacy-features-connecting-wireless-networks-secb9cb3140c/web)時，會使用隨機化的 MAC 位址。

您可以將 [MAC 位址](https://support.apple.com/en-us/102509)設定為根據每個網路隨機化，並偶爾輪換，以防止在不同網路之間和同一網路中長時間追蹤。

前往**系統設定** → **網路** → **Wi-Fi** → **詳細資訊**，然後將**私人 Wi-Fi 位址**設定為**固定**（如果您想要使用固定的位址連線），或**輪替**（如果您想要位址定時更換）。

也可以考慮更改您的主機名稱，這是另一個會在您連線的網路中廣播出去的裝置識別資料。 您可能會想要在**系統設定** → **一般** → **分享**中將主機名稱設定為較一般的名稱，例如「MacBook Air」、「Laptop」、「John's MacBook Pro」或「iPhone」。

## 安全保護

macOS 通過不同屬性的多層軟體和硬體保護來進行深度防禦。 這確保了某一層故障不會損害系統的整體安全性。

### 軟體安全

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

macOS 可以安裝測試版更新。 但它們不穩定，且因為是測試用，可能還會有[額外遙測](https://beta.apple.com/privacy)。 因此，我們建議避免使用測試版軟體。

</div>

#### 簽署系統卷宗

macOS 的系統組件受到唯讀的[簽署系統卷宗](https://support.apple.com/guide/security/signed-system-volume-security-secd698747c9/web)之保護，這代表您和惡意軟體都無法更動重要的系統檔案。

系統卷宗在運行時會予以驗證，任何未使用 Apple 的有效加密簽名進行簽署的數據都將遭拒絕。

#### 系統完整性保護

macOS 設定了某些無法覆蓋的安全限制。 這些稱為[強制取用控制](https://support.apple.com/guide/security/system-integrity-protection-secb7ea06b49/1/web/1)，它們構成 macOS 上的沙盒、家長控制和[系統完整性保護](https://support.apple.com/en-us/102149)的基礎。

系統完整保護使重要的檔案成為唯讀，以防止惡意代碼的修改。 這是基於硬體內核完整保護之上，可防止記憶體中的內核遭修改。

#### 應用程式安全性

##### App 沙盒

在 macOS 上，應用程式是否受沙盒保護是由開發人員簽署時決定。 [App Sandbox](https://developer.apple.com/documentation/xcode/configuring-the-macos-app-sandbox) 會透過限制惡意行為者在應用程式被攻擊時可以存取的內容，保護您執行的應用程式。 *單靠* App Sandbox 無法防止惡意開發人員的[:material-package-variant-closed-remove: 供應鏈攻擊](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}。 為此，沙盒需要由開發者以外的人執行，就像在[App Store](https://support.apple.com/guide/security/gatekeeper-and-runtime-protection-sec5599b66df/1/web/1#:~:text=All%20apps%20from%20the%20App%20Store%20are%20sandboxed%20to%20restrict%20access%20to%20data%20stored%20by%20other%20apps.) 中一樣。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

從官方 App Store 之外下載的軟體不需要沙盒。 如果您的威脅模型以防禦 [:material-bug-outline: 被動攻擊](../basics/common-threats.md#security-and-privacy){ .pg-orange }為優先，那麼可能要檢查在 App Store 以外下載的軟體是否於沙盒中運作，這要由開發人員*選擇性加入*。

</div>

您可以透過幾種方式檢查應用程式是否使用 App Sandbox：

您可以使用「[活動監視器](https://developer.apple.com/documentation/security/protecting-user-data-with-app-sandbox#Verify-that-your-app-uses-App-Sandbox)」檢查已執行的應用程式是否受到沙盒保護。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

如果應用程式當中只有部分處理程序受到沙盒保護，不代表所有處理程序都有沙盒保護。

</div>

另外，在執行應用程式之前，您也可以在終端機執行下列指令檢查：

``` zsh
codesign -dvvv --entitlements - <您的應用程式路徑>
```

如果應用程式有沙盒保護，應該會看到下列輸出結果：

``` zsh
    [Key] com.apple.security.app-sandbox
    [Value]
        [Bool] true
```

如果您發現要執行的應用程式尚未沙盒化，則可以採用虛擬機器或獨立裝置等[隔離運作](../basics/common-threats.md#security-and-privacy)方法、使用有沙盒化的其他類似應用程式，或乾脆完全不要使用未經沙盒化的應用程式。

##### 執行時期加固

[執行時期加固（Hardened Runtime）](https://developer.apple.com/documentation/security/hardened_runtime)是應用程式的額外保護形式，可防止某些類別的攻擊。 它會停用某些功能（例如 JIT）來提高應用程式的安全性，以防止被破解。

您可以使用下列指令檢查應用程式是否使用 Hardened Runtime：

``` zsh
codesign -dv <您的應用程式路徑>
```

若有啟用 Hardened Runtime，會看到 `flags=0x10000(runtime)`。 這邊的 `runtime` 輸出代表已啟用 Hardened Runtime。 可能還有其他旗標，但 runtime 旗標就是我們要找的部份。

您可以在活動監視器中開啟一欄名為「Restricted」的旗標，此旗標表示會防止程式透過 macOS 的[動態連結器](https://pewpewthespells.com/blog/blocking_code_injection_on_ios_and_os_x.html)注入程式碼。 理想情況下，這裡應該顯示「是」。

##### 防毒軟體

macOS 提供兩種[惡意軟體防禦](https://support.apple.com/guide/security/protecting-against-malware-sec469d47bd8/1/web/1)機制：

1. 首先，防止啟動惡意軟體是由 App Store 對 App Store 應用程式的審核流程或*公證*（*Gatekeeper* 的一部份），這是 Apple 允許運行之前掃描第三方應用程式是否存在已知惡意軟體的程式。 應用程式必須由開發人員使用 Apple 給予他們的金鑰簽署。 這個機制可確保您執行的軟體來自真正的開發者。 「公證化」也要求開發人員為他們的應用程式啟用執行時期加固，以限制漏洞被利用的方法。
2. *XProtect* 提供針對其他惡意軟體的防護以及修復系統上現有惡意軟體，XProtect 是 macOS 內建較傳統的防病毒軟體。

我們建議不要安裝第三方防毒軟體，它們通常不具備正常運作所需的系統存取權限。且由於 Apple 對第三方應用程式的限制，授予它們所要求的高級別存取權限，反而容易對電腦造成更大的安全和隱私風險。

##### 備份

macOS 內建稱為 [Time Machine](https://support.apple.com/HT201250) 的自動備份軟體，可以將[加密備份](https://support.apple.com/guide/mac-help/keep-your-time-machine-backup-disk-secure-mh21241/mac)建立到外接或網路磁碟，以避免檔案毀損或遭到刪除。

### 硬體安全

macOS 中的許多現代安全功能（例如現代安全啟動、硬體級漏洞利用緩解、作業系統完整性檢查和檔案加密）都依賴 Apple Silicon，Apple 較新硬體一直具有[最佳安全性](https:// support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1)。 我們只鼓勵使用 Apple Silicon，而不推薦較舊的 Intel Mac 電腦或 Hackintosh。

其中一些現代安全功能可在配備Apple T2 安全晶片的 Intel 老式Mac 電腦上使用，但該晶片容易受到*checkm8* 漏洞的攻擊，這可能會損害其安全性。

若您使用鍵盤等藍牙配件，建議最好是 Apple 官方配件，因為 macOS 會[自動更新](https://support.apple.com/en-us/120303#:~:text=Firmware%20updates%20are%20automatically%20delivered%20in%20the%20background%20while%20the%20Magic%20Keyboard%20is%20actively%20paired%20to%20a%20device%20running%20macOS%2C%20iOS%2C%20iPadOS%2C%20or%20tvOS.)其軔體。 使用第三方配件沒問題，但應該記住定期為其更新安裝軔體。

Apple 的 SoC 著重於通過將安全功能轉移到功能有限的專用硬體，以[盡可能減少攻擊面](https://support.apple.com/en-vn/guide/security/secf020d1074/web#:~:text=Security%2Dfocused%20hardware%20follows%20the%20principle%20of%20supporting%20limited%20and%20discretely%20defined%20functions%20to%20minimize%20attack%20surface.)。

#### Boot ROM

macOS 通過僅允許官方 Apple 軟體在開機時運作，以防止惡意軟體持久存在。這也稱為[安全開機](https://support.apple.com/en-vn/guide/security/secac71d5623/1/web/1)。 Mac 電腦利用 SoC 上，稱為 [boot ROM](https://support.apple.com/en-vn/guide/security/aside/sec5240db956/1/web/1) 的唯讀記憶體來驗證此軟體，該儲存空間是在[晶片製造過程中](https://support.apple.com/en-vn/guide/security/secf020d1074/1/web/1#:~:text=which%20is%20laid%20down%20during%20Apple%20SoC%20fabrication)就設定完成​​的。

開機 ROM 構成了硬體信任根。 這可確保惡意軟體無法篡改開機流程，因為 Boot ROM 不可變更。 Mac 啟動時，開機 ROM 第一個運行，為信任鏈中的第一個環節。

Mac 電腦能使用三種[安全性模式](https://support.apple.com/guide/deployment/startup-security-dep5810e849c/web#dep32fb404e1)開機：*完全安全*、*降低安全*，以及*許可式安全*，預設值為完全安全。 理想情況下，您應該使用完全安全模式，並避免使用諸如[核心擴充元件](https://support.apple.com/guide/deployment/system-extensions-in-macos-depa5fb8376f/web#dep51e097f45)</strong>等軟體，而須降低安全模式。 請務必[檢查](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac)使用的是完全安全模式。

#### 安全隔離區

**[Secure Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/web)** 是內建於使用 Apple Silicon 的裝置的安全晶片，負責儲存和產生資料儲存期間，以及 Face ID 和 Touch ID 資料的加密金鑰。 它包含自己的[另一組 Boot ROM](https://support.apple.com/en-vn/guide/security/sec59b0b31ff/web#sec43006c49f)。

您可以將安全隔離區想成裝置的安全中心：它具有 AES 加密引擎和安全儲存加密金鑰機制，它與系統的其餘部分分開，因此即使主處理器受到損害，也仍然保持安全。

#### Touch ID

Apple Touch ID 功能可使用生物識別技術安全地解鎖設備。

您的生物識別資料[永遠不會離開您的裝置](https://www.apple.com/legal/privacy/data/en/touch-id/#:~:text=Touch%C2%A0ID%20data%20does%20not%20leave%20your%20device%2C%20and%20is%20never%20backed%20up%20to%20iCloud%20or%20anywhere%20else.)；它僅儲存在安全隔離區當中。

#### 硬體麥克風斷線

所有配備 Apple Silicon 或 T2 晶片的筆記型電腦，都具備在闔上螢幕時，以[硬體方式中斷](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web)內建麥克風連線的功能。 這意味著即使作業系統受到破壞，攻擊者無法監聽 Mac 的麥克風。

請注意，攝影機沒有硬體斷接，因為只要上蓋關閉時，其視線即會被遮擋。

#### 相機安全指示燈

Mac 內建的相機設計是，如果相機指示燈[沒有亮起](https://support.apple.com/en-us/102177#:~:text=The%20camera%20is%20engineered%20so%20that%20it%20can’t%20activate%20without%20the%20camera%20indicator%20light%20also%20turning%20on.%20This%20is%20how%20you%20can%20tell%20if%20your%20camera%20is%20on.)，就無法開啟相機。

#### 外圍處理器安全

電腦除了主要的 CPU 之外還有其他的[內建處理器](https://support.apple.com/en-vn/guide/security/seca500d4f2b/1/web/1)，用於處理網路、圖形、電源管理等事務。 這些處理器可能沒有足夠的安全性且受到損害，因此蘋果試圖減少其硬體中對這類處理器的需求。

當需要使用其中某一種處理器時，Apple 會與供應商合作，以確保該處理器

- 啟動時從主 CPU 運行經過驗證的韌體
- 有自己的安全啟動鏈
- 遵循最低加密標準
- 確保正確撤銷已知的不良韌體
- 已禁用其調試介面
- 使用 Apple 的加密金鑰簽名

#### 直接記憶體存取保護

Apple Silicon 會將需要[直接存取記憶體](https://support.apple.com/guide/security/direct-memory-access-protections-seca4960c2b5/1/web/1)的各個元件分離。 例如，Thunderbolt 端口無法訪問為內核指定的記憶體。

#### 終端機鍵盤輸入安全

開啟 [Secure Keyboard Entry](https://support.apple.com/guide/terminal/use-secure-keyboard-entry-trml109/mac) 可防止其他應用程式偵測您在終端機中輸入的內容。
