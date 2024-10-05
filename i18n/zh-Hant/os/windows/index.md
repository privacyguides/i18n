---
title: Windows 總覽
icon: material/microsoft-windows
description: Microsoft Windows 是一種常見的作業系統，開箱即用；但它不是一個尊重隱私的作業系統。 我們的指南涵蓋了在不更換作業系統的情況下對電腦進行一些改進。
---

**Microsoft Windows** 是許多 PC 預設配備的常用作業系統。 以下指南旨在提供一些改善隱私的方法，並透過停用一些不必要的功能來減少預設的遙測和儲存的資料。 隨著時間的推移，微軟會為作業系統增加功能，這些功能有時可能會依賴雲端服務。 這些功能通常需要某些類型的 [可選資料](https://privacy.microsoft.com/data-collection-windows)，有時這些資料會被傳送到遠端伺服器進行處理。

其中一個最新的範例叫做 **Recall**，是 Copilot AI 功能集的一部分。 定期擷取您在電腦上看到的任何內容的螢幕截圖，以便日後展示給您看。 這些「有幫助」的功能會產生相當多的元資料，可以進行法證分析。 在大多數情況下，瀏覽記錄已經足夠，因此可以安全地停用此功能。 Recall 的主要問題是資料會儲存在本機資料庫中，當裝置開機時資料會被解密，這表示如果裝置感染惡意軟體，很容易成為駭客的目標。 Recall 不會刪除資料庫中複製的密碼或財務資訊等敏感資訊，但可以防止對受數位版權管理 (DRM) 系統保護的任何版權內容進行截圖。

不幸的是，在新增此功能時，並沒有過多考慮預設啟用此功能對隱私的影響 (現在 [不再是](https://wired.com/story/microsoft-recall-off-default-security-concerns))。 然而，這並非個別例子。 另一個例子是 Microsoft 在新安裝 Windows 11 時，未經允許就自動 [啟用資料夾備份至 OneDrive](https://neowin.net/news/windows-11-is-now-automatically-enabling-onedrive-folder-backup-without-asking-permission)。

可透過以下指南增強 Windows 上的隱私和安全性，而無需下載任何第三方工具：

- 初始安裝（即將推出）
- [群組原則設定](group-policies.md)
- 隱私設定 (即將推出)
- 應用程式沙盒 (即將推出)
- 安全強化 (即將推出)

<div class="admonition example" markdown>
<p class="admonition-title">本節為新增內容</p>

本節仍在施工中，與其他作業系統相比，Windows 安裝需要花費更多的時間和精力才能使用。

</div>

## 隱私筆記

Microsoft Windows，尤其是那些針對消費者的版本，如 **家用版**，在 [預設](https://theguardian.com/technology/2015/jul/31/windows-10-microsoft-faces-criticism-over-privacy-default-settings) 下通常不會優先使用對隱私友善的功能。 因此，我們經常看到比必要更多的 [資料收集](https://en.wikipedia.org/wiki/Criticism_of_Microsoft#Telemetry_and_data_collection)，卻沒有任何真正的警告說明這是預設行為。 為了在廣告領域與 Google 競爭，[Cortana](https://en.wikipedia.org/wiki/Cortana_\(virtual_assistant\)) 加入了獨特的識別碼，例如「廣告 ID」，以便關聯使用情況，協助廣告商針對性地投放廣告。  在 Windows 10 推出時，非企業版無法停用遙測功能。 現在仍然無法停用，但微軟新增了 [減少](https://extremetech.com/computing/243079-upcoming-windows-update-reduces-spying-microsoft-still-mum-data-collects) 傳送資料的功能。

Windows 11 有許多限制或預設值，例如：

- 要求使用 Microsoft 帳戶而非本機帳戶。
- 使 Windows **專業版** 和 **企業版** 更難找到本機帳戶選項。
- 預設啟用所有資料收集選項，要求使用者「選擇退出」。
- 以難以移除的方式大量整合 Bing、OneDrive 和 Teams 等 Microsoft 服務，並將其視為使用者的唯一選擇。
- 將預設瀏覽器永遠設定為 Edge，或在預設瀏覽器變更時還原為 Edge。
- 在 Windows 和各種 Microsoft 應用程式中加入雲端 AI 功能。
- 不必要地儲存敏感資料。 即使資料儲存在本機且未傳送至微軟，但仍可能成為駭客或惡意軟體的目標。

微軟經常使用自動更新功能為您的裝置新增新功能，並進行收集您的資料且這些功能預設啟用。 某些 [隱私權功能](https://blogs.windows.com/windows-insider/2023/11/16/previewing-changes-in-windows-to-comply-with-the-digital-markets-act-in-the-european-economic-area)，例如 _選擇退出_ 與 Windows 同步線上微軟帳戶的選項，需要您在安裝時選擇 EEA（歐洲經濟區）內的國家。 安裝 Windows 之後，可以將其變更為您真正的國家/地區。

## Windows 版本

遺憾的是，許多重要的隱私與安全功能都被鎖定在成本較高的 Windows 版本，而非 Windows **家用版**。 **家用版** 缺少的一些功能包括 Bitlocker 磁碟機加密、Hyper-V 和 Windows 沙箱。 在 Windows 指南中，我們將介紹如何適當地使用所有這些功能，因此擁有高級版本的 Windows 將是必要的。

Windows **企業版** 在設定 Windows 內建的隱私與安全設定時，提供最大的彈性。 例如，它們是唯一能限制啟用遙測工具，阻止將資料傳回微軟的版本。 遺憾的是，Enterprise 無法零售購買，因此可能無法使用。

可供_零售_購買的最佳版本是 Windows **專業版**，因為它幾乎擁有您想要用來保護裝置的所有功能，包括 Bitlocker、Hyper-V 等。 唯一遺憾的是，微軟的遙測缺少了一些最嚴格的限制。

學生和教師可以從教育機構免費取得 Windows **教育版**（相當於企業版）或 **專業教育版**（相當於專業版）授權，包括在個人裝置上。 許多學校透過 OnTheHub 或 Microsoft Azure for Education 與微軟合作，因此您可以檢查這些網站或學校的福利頁面，看看是否符合資格。 能否獲得這些許可完全取決於機構。 對許多人來說，這可能是取得 Windows 企業版供個人使用的最佳方式。 與零售版本相比，使用教育授權不會帶來額外的隱私或安全風險。

不建議使用第三方修改過的 Windows 版本，例如 Windows AME。 由於修改過的 Windows 版本 (例如 Windows AME) 不會收到更新，Windows Defender 中的安全功能和防毒定義會落後於目前的威脅狀況，讓您有機會受到攻擊，因而使您更不安全。

## 取得 Windows

目前僅有 Windows 11 授權金鑰可供購買，但這些金鑰也可在 Windows 10 上使用，因此您仍可購買 Windows 11 專業版金鑰來啟用 Windows 10。

官方的 [媒體建立工具](https://microsoft.com/software-download/windows11) 是將 Windows 安裝程式放入 USB 隨身碟的最佳方法。 Rufus 或 Etcher 等第三方工具可能會意外修改檔案，這可能會導致開機問題或安裝時出現其他麻煩。

此工具只能讓您安裝**家用版**或**專業版**，因為沒有 Windows **企業版**的公開下載。 如果您有**企業版**授權金鑰，您可以輕鬆從**專業版**升級。 若要執行此動作，請安裝 Windows **專業版**，但在安裝過程中無須輸入授權金鑰，然後在完成安裝後，在「設定」應用程式中輸入您的 **企業版** 金鑰。 輸入有效的授權金鑰後，您的**專業版**安裝將會自動升級為**企業版**。

如果您安裝的是**教育版**授權，通常會有一個私人下載連結，當您從機構的福利入口網站取得授權金鑰時，該連結會與授權金鑰一同提供。
