---
title: Windows 總覽
icon: material/microsoft-windows
---

**Microsoft Windows** 是廣泛使用的私有商用作業系統。 最新版本的 Windows，尤其是 Windows 11，被廣泛認為是最具隱私侵犯性和最不安全的現代作業系統。

如果可以在 Windows 10 和 Windows 11 之間選擇，我們建議盡可能長時間地使用 Windows 10。 Windows 10 的支援期限將持續到 2025 年 10 月。 然而，目前版本的 Windows 都不會在不進行大量修改的情況下尊重您的隱私，而這些修改通常會被 Microsoft 未來的更新所撤銷。 如果想要保護隱私和尊重用戶偏好的作業系統，請考慮 [Linux](../linux-overview.md)。

Microsoft 不斷在 Windows 11 中新增雲端功能，這些功能預設為啟用，無需使用者同意。 最近（2024 年5 月），他們推出了一個名為**Recall** 的內建鍵盤記錄器（其AI 功能的一部分），它會記錄裝置上的每次擊鍵，並透過定期截圖來記錄螢幕。 這些資料不安全地儲存在本機資料庫，該資料庫在裝置開機時會被解密，意味著很容易成為駭客的目標。 它不會編輯資料庫中複製的密碼或財務資訊等敏感訊息，但它確實透過不記錄受版權保護的內容來保護好萊塢電影製片廠。 此功能目前僅在某些較新的裝置上提供，但它足以說明 Microsoft 是多麼不關心用戶的安全和隱私。

## 指南

可透過以下指南增強 Windows 上的隱私和安全性，而無需下載任何第三方工具：

- 初始安裝 (coming soon)
- [Group Policy Settings](group-policies.md)
- 隱私設定 (coming soon)
- 應用程式沙盒 (coming soon)
- 安全強化 (coming soon)

本節仍在施工，與其他作業系統相比，Windows 安裝需要花費更多的時間和精力才能使用。 Additional guides are coming soon!

## 隱私記錄

特別是自 Windows 8 發布以來，微軟在其作業系統版本中表現出了極其侵犯隱私的行為，一直利用 Windows 是使用最廣泛的桌面作業系統的優勢。 Windows 10 因其預設將大量資料和遙測資料([包括](https://en.wikipedia.org/wiki/Criticism_of_Microsoft#Telemetry_and_data_collection)「使用者的聯絡人和日曆事件、位置資料和歷史記錄、'遙測'（診斷資料） [...])傳回 Microsoft，受到廣泛[批評](https://www.theguardian.com/technology/2015/jul/31/windows-10-microsoft-faces-criticism-over-privacy-default-settings)。 和“廣告 ID”，以及啟用（預設） Cortana 助理時的更多數據”。 Windows 10 也讓更改預設應用程式（例如 Web 瀏覽器）取代 Microsoft 提供的應用程式變得更加困難，這種行為至今仍然存在。

一開始無法在 Windows 10 非企業版中停用遙測。 目前仍無法停用，但微軟[減少遙測](https://www.extremetech.com/computing/243079-upcoming-windows-update-reduces-spying-microsoft-still-mum-data-collections)。

Windows 11 引入了更多侵犯隱私行為，包括：

- 家用版被迫使用 Microsoft 帳戶而不是本機帳戶，而專業版及更高版本會隱藏本機帳戶選項。
- 預設啟用幾乎所有資料收集選項。
- 難以刪除大量整合 Bing、OneDrive 和 Teams 等 Microsoft 服務。
- 將（雲端的）AI 功能新增至 Windows 和各種 Microsoft 應用程式。
- 不必要地儲存大量敏感資料。 即使資料儲存在本機且未傳送至微軟，但仍可能成為駭客或惡意軟體的目標。

微軟經常濫用自動更新功能為裝置添加新功能，並預設為啟用新功能來個人資料。

Windows 11 中的某些隱私功能僅限於在歐盟的裝置。 我們尚未找到可靠方法在全球範圍內存取這些設定。

## Windows 版本

不幸的是，許多重要的隱私和安全功能都鎖定在較昂貴的 Windows 版本，未提供於 Windows 家用版。 **Windows 家用版** 缺少的一些功能包括 Bitlocker 磁碟機加密、Hyper-V 和 Windows Sandbox。 在 Windows 指南中，我們將介紹如何正確使用所有這些功能，因此擁有高級版的 Windows 將至關重要。

**Windows 企業版** 在配置 Windows 內建的隱私和安全設定時提供最大的彈性。 例如，它們是唯一能限制啟用遙測工具，阻止將資料傳回微軟的版本。 遺憾的是，Enterprise 無法零售購買，因此可能無法使用。

可_零售_購買的最佳版本是**Windows 專業版**。 遺憾的是，此版本不能對 Microsoft 遙測設定一些最嚴格的限制，但具有幾乎所有想用來保護裝置的功能，包括 Bitlocker、Hyper-V 等。

學生和教師可以從其教育機構免費取得 **Windows Education**（相當於 Enterprise）或 **Windows Pro Education**（相當於 Pro）（包括個人裝置）。 許多學校透過 OnTheHub 或 Microsoft Azure for Education 與 Microsoft 合作，因此您可以檢查這些網站或學校的福利頁面，看看是否符合資格。 能否獲得這些許可完全取決於機構。 對許多人來說，這可能是取得 Windows 企業版供個人使用的最佳方式。 與零售版本相比，使用教育授權不會帶來額外的隱私或安全風險。

不建議使用 Windows 的分支或修改版本，例如 Windows AME。 由於 Windows AME 等 Windows 修改版本不會收到更新，因此 Windows Defender 中的安全功能和防毒定義將落後於當前的威脅情勢，從而易受到攻擊。

## 取得 Windows

目前，僅可購買 Windows 11 授權金鑰，但這些金鑰也適用於 Windows 10，因此仍可購買 Windows 11 專業版金鑰來啟動 Windows 10 安裝。

官方的[Media Creation tool](https://www.microsoft.com/software-download/windows10)是將Windows安裝程式放在 USB 隨身碟上的最佳方法。 Rufus 或 Etcher 等第三方工具可能會意外修改文件，可能導致啟動或其他安裝問題。

此工具僅允許安裝家用版或專業版，因為 Windows 企業版沒有公開可用的下載。 但如有企業版授權金鑰，則可以輕鬆升級專業版。 只需安裝 Windows Pro，無需在安裝過程中輸入許可證金鑰，然後在完成安裝後在「設定」應用程式中輸入您的企業金鑰。 輸入有效的許可證金鑰後，則專業版安裝將自動升級至企業版。

如要安裝教育版，當從機構的福利入口網站取得許可證金鑰時，通常會提供私人下載以及許可證金鑰。
