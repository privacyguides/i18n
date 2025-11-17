---
title: "選擇您的硬體"
icon: 'material/chip'
description: 隱私保護不能僅聚焦於軟體方面；了解您每天使用的硬體，以保護您的隱私。
---

當談到隱私權的討論時，硬體往往不如軟體那般受到重視。 您的硬體應該被視為建立其他隱私設定的基礎。

## 挑選電腦

您的裝置處理並儲存所有數位資料。 重要的是，您所使用的裝置製造商和開發商必須持續提供安全性更新

### 硬體安全認證

有些裝置會有「硬體安全認證」，例如在設計硬體時，廠商之間會就最佳實踐和建議進行合作：

- [Windows 安全核心電腦](https://learn.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-highly-secure-11) 符合 Microsoft 指定的更高安全性標準。 這些保護並不只適用於 Windows 使用者；其他作業系統的使用者仍可利用其 [DMA 保護](https://learn.microsoft.com/en-us/windows/security/information-protection/kernel-dma-protection-for-thunderbolt) 以及 完全不信任 Microsoft 證書 等功能。
- [Android Ready SE](https://developers.google.com/android/security/android-ready-se) 是廠商之間的合作，以確保其裝置遵循 [最佳實踐](https://source.android.com/docs/security/best-practices/hardware) ，並包含基於硬體的可防篡改儲存裝置，例如加密金鑰。
- 在 Apple SoC 上執行的 macOS 可利用 [硬體安全性](../os/macos-overview.md#hardware-security) ，第三方作業系統可能無法使用此類功能。
- [ChromeOS 的安全性](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper) 在 Chromebook 上可發揮最佳效果，因為它能利用可用的硬體功能，例如 [硬體信任根](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper/#hardware-root-of-trust-and-verified-boot) 。

即使您不使用這些作業系統，參與這些計畫也可能表示製造商在硬體安全性和更新方面遵循最佳實踐。

### 預先安裝的作業系統

新電腦幾乎都會預先安裝 Windows，除非您買的是 Mac 或特殊的 Linux 機器。 通常擦除硬碟並重新安裝您所選擇的作業系統是個好主意，即便是從頭重新安裝 Windows 也同樣如此。 由於硬體廠商與不良軟體廠商之間的協議，預裝的 Windows 通常會預先載入臃腫軟體、[廣告軟體](https://bleepingcomputer.com/news/technology/lenovo-gets-a-slap-on-the-wrist-for-superfish-adware-scandal)，甚至是 [惡意軟體](https://zdnet.com/article/dell-poweredge-motherboards-ship-with-malware) 。

### 韌體更新

硬體經常會有安全問題，這些問題會透過硬體的韌體更新來發現和修補。

從您的主機板到儲存設備，幾乎電腦的每個元件都需要韌體才能運作。 理想的情況是，您裝置的所有元件都能獲得完整支援。 只要裝置受支援，Apple 裝置、Chromebook、大多數 Android 手機和 Microsoft Surface 裝置都會為您處理韌體更新。

如果您自己組裝電腦，可能需要從 OEM 網站下載主機板韌體，手動更新主機板韌體。 如果您使用 Linux，可考慮使用內建的 [`fwupd`](https://fwupd.org) 工具，讓您檢查並套用主機板的任何可用韌體更新。

### TPM/安全加密協處理器

大多數電腦和手機都配備 TPM （或類似的安全加密協處理器），可安全儲存您的加密金鑰，並處理其他與安全相關的功能。 如果您目前使用的機器沒有這些功能，您可能會從購買具有此功能的較新電腦中獲益。 有些桌上型電腦和伺服器主機板有一個「TPM 接口」，可供添加包含 TPM 的小型配件板。

<div class="admonition Note" markdown>
<p class="admonition-title">Note</p>

虛擬 TPM 容易受到側通道攻擊，而外部 TPM 由於與主機板上的 CPU 分離，當攻擊者能夠存取硬體時，容易受到 [監聽](https://pulsesecurity.co.nz/articles/TPM-sniffing) 攻擊。 解決這個問題的方法是將安全加密協處理器包含在 CPU 本身，Apple 的晶片和微軟的 [Pluton](https://microsoft.com/en-us/security/blog/2020/11/17/meet-the-microsoft-pluton-processor-the-security-chip-designed-for-the-future-of-windows-pcs) 就是如此。

</div>

### 生物識別技術

許多裝置都配備了指紋辨識器或臉部辨識功能。 這些方法可能非常方便，但並不完美，有時也會失敗。 當發生這種情況時，大多數裝置都會回退到 PIN 或密碼，這意味著您裝置的安全性仍然取決於密碼。

生物識別技術可以防止有人監視您輸入密碼，因此，如果您的威脅模式中包括肩窺，那麼生物識別技術就是一個很好的選擇。

大多數的臉部辨識實作都需要您看著您的手機，而且也只能在相對較近的距離才能運作，所以您不需要太擔心有人會在未經您同意的情況下，將您的手機對準您的臉部來解鎖。 如果您願意，仍可在手機鎖定時停用生物辨識功能。 在 iOS 上，您可以按住側邊按鈕和音量按鈕 3 秒鐘，在支援 Face ID 的機型上停用 Face ID。 在 Android 上，按住電源按鈕，然後按下功能表上的 鎖定 。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

有些裝置沒有適當的硬體來進行安全的臉部驗證。 有兩種主要類型的臉部驗證機制：2D 和 3D。 3D 類型的臉部辨識利用點陣投影器，讓裝置為您的臉部建立 3D 深度圖。 請確定您的裝置具有此功能。

</div>

Android 為生物辨識定義了三種 [安全等級](https://source.android.com/docs/security/features/biometric/measure#biometric-classes) ，您應該在啟用生物辨識之前檢查您的裝置是否屬於 Class 3。

### 裝置加密

如果您的裝置已進行 [加密](../encryption.md) ，在裝置完全關機 (而非僅是睡眠狀態) 時，也就是在您第一次輸入加密金鑰或鎖定螢幕密碼之前，您的資料是最安全的（相較於其他狀態）。 在手機上，這種較高安全性的狀態稱為 “Before First Unlock（首次解鎖之前）（BFU）”，而一旦您在重新開機/開機後輸入正確密碼，則稱為 “After First Unlock（首次解鎖之後）（AFU）”。 相較於 BFU，AFU 對於數位鑑識工具套件和其他攻擊的防禦能力要低得多。 因此，如果您擔心攻擊者可以實體存取您的裝置（即 可直接取得您的設備實體 ），您應該在不使用裝置時將其關機。

這可能不切實際，所以請考慮是否值得；但無論如何，只要您使用強大的加密金鑰，即使是 AFU 模式也能有效對抗大多數威脅。

## 其他硬體

有些威脅單靠您的內部元件無法防範。 這些選項中有許多都是高度情境性的；請評估您的威脅模型是否真的需要這些選項。

### 實體安全金鑰

硬體金鑰是使用強大加密技術來驗證您的裝置或帳戶的裝置。 其原理是：由於金鑰無法被複製，您可以使用金鑰來保護帳戶，使帳戶只有在實際擁有金鑰的情況下才能被存取，從而消除許多遠端攻擊。

[建議的實體金鑰 :material-arrow-right-drop-circle:](../security-keys.md){ .md-button .md-button--primary } [了解更多有關實體金鑰的事 :material-arrow-right-drop-circle:](multi-factor-authentication.md#hardware-security-keys){ .md-button }

### 相機/麥克風

如果您不想信任作業系統的權限控制，打算直接阻止相機啟動，您可以購買相機阻擋器用以實質上阻止光線進入相機。 您也可以購買沒有內建相機的裝置，使用外接式相機，只要用完就可以拔下。 有些裝置內建了相機阻擋器或硬體開關，可以直接斷開相機的電源。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

您應該購買適合您筆記型電腦尺寸的保護套—且它在您關上蓋子時不應造成損傷。 遮蓋相機會干擾亮度自動調節和臉部驗證功能。

</div>

對於麥克風存取，在大多數情況下，您需要信任作業系統內建的權限控制； 或者，購買沒有內建麥克風的裝置，使用外接式麥克風，使用完後就可以拔下麥克風。 有些裝置，例如：[MacBook 或 iPad](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web)，在您關上蓋子時，麥克風會在硬體方面被斷開連接。

許多電腦的 BIOS 選項可以停用攝影機和麥克風； 當在此處被停用時，這些硬體甚至不會在啟動的系統上顯示為裝置。

### 螢幕防窺片

螢幕防窺片是一種可以覆蓋在正常螢幕上的薄膜，因此螢幕只能從特定角度可見。 如果您的威脅模型包括他人偷看您的螢幕，這些都是很好的方法，但並非萬無一失，因為任何人都可以移動到不同的檢視角度，看到您螢幕上的內容。

### 警醒設備

警醒設備可在沒有人員操作的情況下停止機器運作。 這些設備原本是作為安全措施而設計的，但同樣的概念也可以應用在電子裝置上，在您不在場時鎖上裝置。

有些筆記型電腦能夠[偵測](https://support.microsoft.com/en-us/windows/managing-presence-sensing-settings-in-windows-11-82285c93-440c-4e15-9081-c9e38c1290bb)您是否在場，並在您沒有坐在螢幕前時自動鎖定。 您應該檢查作業系統的設定，看看您的電腦是否支援此功能。

您也可以購買纜線，例如 [Buskill](https://buskill.in)，當纜線中斷時，就會鎖定或抹除您的電腦。

### 反阻絕/邪惡女傭攻擊

要在您擁有裝置之前防止針對您的攻擊，最好的方法是在實體商店購買裝置，而不是下訂寄到您的地址。

確保您的裝置支援安全開機/驗證開機，並且已啟用。 盡可能避免讓您的裝置無人看管。

### 肯辛頓鎖

許多筆記型電腦都配備[肯辛頓鎖孔](https://www.kensington.com/solutions/product-category/security/?srsltid=AfmBOorQOlRnqRJOAqM-Mvl7wumed0wBdiOgktlvdidpMHNIvGfwj9VI)，可用來將**金屬纜線**鎖到機器上的插槽，用來固定您的裝置。 這些鎖具可以是密碼鎖或鑰匙鎖。

就跟所有的鎖一樣，[物理攻擊](https://youtu.be/vgvCxL7dMJk)對肯辛頓鎖相當有效，因此您只應將其用來讓小偷知難而退。 您可以在家中，甚至在公共場所時，利用桌腳或其他不易移動的物體來固定您的筆記型電腦。

## 保護您的網路安全

### 隔離

有許多解決方案可讓您分開在電腦上所做的事情，例如虛擬機器和沙箱。 然而，最好的隔離方式是實體隔離。 這對於那些需要您繞過作業系統中的安全功能的軟體非常有用，例如許多遊戲中附帶的防作弊軟體。

對於玩遊戲來說，指定一台機器為您的「遊戲機」並僅用於這個用途，可能會很有用。 將其保留在獨立的 VLAN 上。 這可能需要使用網管型交換器和支援隔離網路的路由器。

大多數消費型路由器都允許您透過啟用獨立的「訪客」網路來實現這一目標，該網路不能與您的主網路互動。 所有不受信任的裝置都可以放在這裡，包括智慧型冰箱、恆溫器、電視等物聯網裝置。

### 極簡化

正所謂「少即是多」。 連接至網路的裝置越少，潛在的攻擊面就越小，確保它們都保持在最新狀態的工作也就越輕鬆。

在家中四處走動，列出您擁有的所有連線裝置清單，對於您持續追蹤這些裝置會相當有用。

### 路由器

您的路由器會處理所有網路流量，並作為您與開放網際網路之間的第一道防線。

<div class="admonition Note" markdown>
<p class="admonition-title">Note</p>

許多路由器都附有儲存空間，可將檔案存放在上面，這樣您就可以從網路上的任何電腦存取這些檔案。 我們建議您不要將網路裝置用於網路以外的用途。 如果您的路由器受到攻擊，您的檔案也會受到攻擊。

</div>

使用路由器時，最重要的是保持更新。 許多現代的路由器會自動安裝更新，但許多其他的路由器則不會。 您應該在路由器的設定頁面檢查此選項。 在任何瀏覽器的網址列輸入 `192.168.1.1` 或 `192.168.0.1`，通常就可以存取該頁面，前提是您在同一個網路中。 您也可以在作業系統的網路設定中檢查「路由器」或「閘道」。

如果您的路由器不支援自動更新，您需要到製造商的網站下載並手動更新。

許多消費級路由器的支援期間不長。 如果製造商不再支援您的路由器，您可以檢查 [FOSS firmware](../router.md) 是否支援。 您也可以購買預設已安裝 FOSS 韌體的路由器；這些路由器的支援期間往往比大多數路由器長。

有些 ISP 提供結合路由器/數據機的產品。 購買一個獨立的路由器，並將 ISP 路由器/數據機設定為數據機模式，可能對安全性來說較好。 這樣一來，即使 ISP 提供的路由器不再發布更新，您仍然可以獲得安全更新和修補程式。 這也代表任何影響數據機的問題都不會影響路由器，反之亦然。
