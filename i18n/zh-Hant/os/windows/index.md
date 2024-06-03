---
title: Windows 總覽
icon: simple/windows
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

Especially since the release of Windows 8, Microsoft has demonstrated extremely privacy-invasive behavior with their operating system releases, consistently taking advantage of the fact that Windows is the most widely-used desktop operating system. Windows 10 was widely [criticized](https://www.theguardian.com/technology/2015/jul/31/windows-10-microsoft-faces-criticism-over-privacy-default-settings) for having default settings that sent a lot of data and telemetry back to Microsoft, [including](https://en.wikipedia.org/wiki/Criticism_of_Microsoft#Telemetry_and_data_collection) "User's contacts and calendar events, location data and history, 'telemetry' (diagnostics data) [...] and 'advertising ID', as well as further data when the Cortana assistant is enabled" (which it is by default). Windows 10 also made it much more challenging to change default applications (such as your web browser) away from Microsoft-provided apps, which is behavior that still persists today.

At launch, telemetry could not be disabled in non-enterprise editions of Windows 10. It still cannot be disabled, but Microsoft added the ability to [reduce the teletetry](https://www.extremetech.com/computing/243079-upcoming-windows-update-reduces-spying-microsoft-still-mum-data-collects) sent to them.

Windows 11 has introduced even more privacy-invasive behavior, including:

- Being forced to use a Microsoft account instead of a local account on Home editions, and still hiding away local account options on Pro editions and higher.
- Enabling virtually all data collection options by default.
- Heavily integrating Microsoft services like Bing, OneDrive, and Teams in ways which are difficult to remove.
- Adding (cloud-based) AI features to many areas in Windows and various Microsoft Apps.
- Unnecessarily storing massive amounts of sensitive data. Even data which is stored locally and not sent to Microsoft is still a target for hackers or malware on your device.

Microsoft often abuses the automatic updates feature to add new functionality to your device that collects your data and is enabled by default.

Some privacy features in Windows 11 are locked to devices in the European Union. We have not yet found a way to reliably access those settings worldwide.

## Windows Editions

Many critical privacy and security features are unfortunately locked away behind higher-cost editions of Windows, instead of being available in Windows Home Edition. Some features missing from **Windows Home Edition** include Bitlocker Drive Encryption, Hyper-V, and Windows Sandbox. In our Windows guides we will cover how to use all of these features appropriately, so having a premium edition of Windows will be critical.

**Windows Enterprise** provides the most flexibility when it comes to configuring privacy and security settings built in to Windows. For example, they are the only editions that allow you to enable the highest level of restrictions on data sent to Microsoft via telemetry tools. Unfortunately, Enterprise is not available for retail purchase, so it may not be available to you.

The best version available for _retail_ purchase is **Windows Pro Edition**. This version does not allow you to set some of the most restrictive limitations on Microsoft's telemetry unfortunately, but does have nearly all of the features you'll want to use to secure your device, including Bitlocker, Hyper-V, etc.

Students and teachers may be able to obtain **Windows Education** (equivalent to Enterprise) or **Windows Pro Education** (equivalent to Pro) for free (including on personal devices) from their educational institution. 許多學校透過 OnTheHub 或 Microsoft Azure for Education 與 Microsoft 合作，因此您可以檢查這些網站或學校的福利頁面，看看是否符合資格。 Whether or not you are able to get these licenses depends entirely on your institution. This may be the best way for many people to obtain an Enterprise-level edition of Windows for personal use. There are no additional privacy or security risks associated with using an Education license compared to the retail versions.

不建議使用 Windows 的分支或修改版本，例如 Windows AME。 由於 Windows AME 等 Windows 修改版本不會收到更新，因此 Windows Defender 中的安全功能和防毒定義將落後於當前的威脅情勢，從而易受到攻擊。

## 取得 Windows

目前，僅可購買 Windows 11 授權金鑰，但這些金鑰也適用於 Windows 10，因此仍可購買 Windows 11 專業版金鑰來啟動 Windows 10 安裝。

官方的[Media Creation tool](https://www.microsoft.com/software-download/windows10)是將Windows安裝程式放在 USB 隨身碟上的最佳方法。 Rufus 或 Etcher 等第三方工具可能會意外修改文件，可能導致啟動或其他安裝問題。

此工具僅允許安裝家用版或專業版，因為 Windows 企業版沒有公開可用的下載。 但如有企業版授權金鑰，則可以輕鬆升級專業版。 只需安裝 Windows Pro，無需在安裝過程中輸入許可證金鑰，然後在完成安裝後在「設定」應用程式中輸入您的企業金鑰。 輸入有效的許可證金鑰後，則專業版安裝將自動升級至企業版。

如要安裝教育版，當從機構的福利入口網站取得許可證金鑰時，通常會提供私人下載以及許可證金鑰。
