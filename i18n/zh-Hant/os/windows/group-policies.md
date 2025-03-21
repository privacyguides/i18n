---
title: 群組原則設定
description: 設定群組政策使 Windows 更尊重隱私的快速指南。
---

Outside modifying the registry itself, the **Local Group Policy Editor** is the most powerful way to change many aspects of your system without installing third-party tools. 更改這些設定需要 [專業版](index.md#windows-editions) 或更高版本。

These settings should be set on a brand-new installation of Windows. Setting them on your existing installation should work, but may introduce unpredictable behavior and is done at your own risk.

所有設定在群組原則編輯器中都附有說明，非常詳細地準確說明了它們的作用。 更改時請注意這些描述，準確了解我們在此建議的內容。 當 Windows 附帶的解釋不充分時，我們在下面解釋了我們的一些選擇。

## 系統管理範本

可開啟「gpedit.msc」並導覽至左側側邊欄中的「**本機電腦政策**」>「**電腦設定**」>「**系統管理範本**」來找到這些設定。 此頁面上的標題對應於管理範本中的資料夾/子資料夾，項目符號對應於各個原則。

若要變更任何群組政策，請雙擊它，然後根據下面的建議在出現的視窗頂部選擇「啟用」或「停用」。 某些群組原則可以配置的其他設定，如果是這種情況，下面也會註明相應的設定。

### 系統

#### 裝置防護

- 開啟虛擬化型安全性:**啟用**
    - 選取平台安全性層級: **安全開機及 DMA 保護**
    - 安全啟動設定: **已啟用**

#### 網際網路通訊管理

- 關閉 Windows 客戶經驗改進計畫: **已啟用**
- 關閉 Windows 錯誤報告: **已啟用**
- 關閉 Windows Messenger 客戶經驗改進計畫: **已啟用**

請注意，停用 Windows 客戶經驗改進計畫也會停用一些其他也可以透過群組原則單獨控制的追蹤功能。 我們不會在這裡列出全部或停用它們，因為此設定涵蓋了這些。

#### OS 原則

- 允許剪貼簿歷程記錄: **已停用**
- 允許在裝置之間的剪貼簿同步處理: **已停用**
- 啟用活動摘要: **已停用**
- 允許公佈使用者活動: **已停用**
- 允許上傳使用者活動: **已停用**

#### 使用者設定檔

- 關閉廣告識別碼: **已啟用**

### Windows 元件

#### 自動播放原則

自動執行和自動播放功能讓 Windows 在連接裝置時執行腳本或執行某些其他任務，有時會繞過使用者同意的安全措施。 這可能導致您在不知情的情況下，讓未信任的設備執行惡意程式碼。 因此，最佳的安全做法是停用這些功能，並改為手動開啟外接磁碟的檔案。

- 關閉自動播放: **已啟用**
- 不允許非磁碟區裝置的自動播放: **已啟用**
- 設定 AutoRun 的預設行為: **已啟用**
    - 預設 AutoRun 行為: **不執行任何 AutoRun 命令**

#### BitLocker 磁碟機加密

在變更以下設定後，您可能需要重新加密作業系統磁碟機。

- 選擇磁碟機加密演算法及金鑰加密強度 (Windows Vista, Windows Server 2008, Windows 7): **已啟用**
    - 選取加密方法:**AES-256**

即使針對 Windows 7 政策設定加密強度，此強度仍適用於較新的 Windows 版本。

##### 作業系統磁碟機

- 啟動時需要其它驗證:**已啟用**
- 允許用於啟動的 PIN 增強:**己啟用**

Despite the names of these policies, this doesn't _require_ you to do anything by default, but it will unlock the _option_ to have a more complex setup (such as requiring a PIN at startup in addition to the TPM) in the BitLocker setup wizard.

#### 雲端內容

- 關閉雲端最佳化內容:**已啟用**
- 關閉雲端消費者狀態內容:**已啟用**
- 不顯示 Windows 祕訣:**已啟用**
- 關閉 Microsoft 消費者體驗:**已啟用**

#### 認證使用者介面

- 要求認證項目之信任的路徑:**已啟用**
- 禁止本機使用者使用安全性問題:\*\*_已啟用_

#### 資料收集與預覽組建

- 允許電腦分析處理:**已啟用**
    - 選項: **傳送必要的診斷資料** (專業版) 或是
    - 選項: **關閉診斷資料** (企業版或教育版)
- 限制診斷記錄檔集合: **已啟用**
- 限制傾印集合: **已啟用**
- 限制用於電腦分析的選擇性診斷資料: **已啟用**
    - 選項: **停用 電腦分析 收集**
- 不顯示意見反應通知: **已啟用**

#### 檔案總管

- 關閉帳戶型深入解析、最近使用、我的最愛和建議的檔案檔案總管: **已啟用**

#### MDM

- 停用 (MDM) 註冊: **已啟用**

#### OneDrive

- 預設將文件儲存到 OneDrive:**已停用**
- 防止 OneDrive 在使用者登入 OneDrive 前產生網路流量:**已啟用**
- 防止使用 OneDrive 儲存檔案: **已啟用**

最後一項設定會停用系統上的 OneDrive；如有使用 OneDrive，請務必將其變更為 **停用**。

#### 推送安裝

- 關閉裝送安裝服務:**已啟用**

#### 搜尋

- 允許 Cortana: **已停用**
- 不要在[搜尋] 中搜尋網路或顯示網路搜尋結果:**已啟用**
- 設定 [搜尋] 中可分享的資訊:**已啟用**
    - 資訊類型:**匿名資訊**

#### 同步您的設定

- 不要同步: **已啟用**

#### 文字輸入

- 改進手寫筆跡與鍵入辨識:**已停用**

#### Windows 錯誤報告

- 不要傳送其它資料:**已啟用**
- 同意 > 設定預設同意: **已啟用**
    - 同意層級: **傳送資料前一律詢問**
