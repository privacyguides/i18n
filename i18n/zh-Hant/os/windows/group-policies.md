---
title: 群組原則設置
---

除了修改登錄機碼本身之外，**本機群組原則編輯器**是無需安裝第三方工具即可更改系統許多方面的最強大方法。 更改這些設定需要 [專業版](index.md#windows-editions) 或更高版本。

這些設定應在全新安裝的 Windows 進行。 在現有安裝上設定它們應該可行，但還是有可能會引發不可預測的行為，須自行承擔風險。

所有設定在群組原則編輯器中都附有說明，非常詳細地準確說明了它們的作用。 更改時請注意這些描述，準確了解我們在此建議的內容。 當 Windows 附帶的解釋不充分時，我們在下面解釋了我們的一些選擇。

## 系統管理範本

可開啟「gpedit.msc」並導覽至左側側邊欄中的「**本機電腦政策**」>「**電腦設定**」>「**系統管理範本**」來找到這些設定。 此頁面上的標題對應於管理範本中的資料夾/子資料夾，項目符號對應於各個原則。

若要變更任何群組政策，請雙擊它，然後根據下面的建議在出現的視窗頂部選擇「啟用」或「停用」。 某些群組原則可以配置的其他設置，如果是這種情況，下面也會註明相應的設置。

### 系統

#### Device Guard

- 打開虛擬化型安全性:**啟用**
  - 平台安全性層級:**安全開機與 DMA 保護**
  - 安全啟動設定:**已啟用**

#### 網際網路通訊管理

- 關閉 Windows 客戶經驗改進計畫:**已啟用**
- 關閉 Windows 錯誤報告:**已啟用**
- 關閉 Windows Messenger 客戶經驗改進計畫:**已啟用**

Note that disabling the Windows Customer Experience Improvement Program also disables some other tracking features that can be individually controlled with Group Policy as well. We don't list them all here or disable them because this setting covers that.

#### OS 原則

- 允許剪貼簿歷程記錄:**已停用**
- 允許裝置之間剪貼簿同步處理:**已停用**
- Enables Activity Feed: **Disabled**
- 允許公佈使用者活動:**已停用**
- 允許上傳使用者活動:**已停用**

#### 使用者設定檔

- 關閉廣告識別碼:**已啟用**

### Windows 元件

#### 自動播放原則

AutoRun and AutoPlay are features which allow Windows to run a script or perform some other task when a device is connected, sometimes avoiding security measures that involve user consent. This could allow untrusted devices to run malicious code without your knowledge. It's a security best practice to disable these features, and simply open files on your external disks manually.

- 關閉自動播放:**已啟用**
- 不允非磁區裝置的自動播放:**已啟用**
- 設定 AutoRun 命令的預設行為:**已啟用**
  - 預設 AutoRun 行為:**不執行任何 AutoRun 命令**

#### BitLocker 磁碟機加密

You may wish to re-encrypt your operating system drive after changing these settings.

- Choose drive encryption method and cipher strength (Windows Vista, Windows Server 2008, Windows 7): **Enabled**
  - Select the encryption method: **AES-256**

Setting the cipher strength for the Windows 7 policy still applies that strength to newer versions of Windows.

##### 作業系統硬碟

- Require additional authentication at startup: **Enabled**
- Allow enhanced PINs for startup: **Enabled**

Despite the names of these policies, this doesn't _require_ you to do anything by default, but it will unlock the _option_ to have a more complex setup (such as requiring a PIN at startup in addition to the TPM) in the Bitlocker setup wizard.

#### 雲端內容

- Turn off cloud optimized content: **Enabled**
- Turn off cloud consumer account state content: **Enabled**
- Do not show Windows tips: **Enabled**
- Turn off Microsoft consumer experiences: **Enabled**

#### Credential User Interface

- Require trusted path for credential entry: **Enabled**
- Prevent the use of security questions for local accounts: **Enabled**

#### Data Collection and Preview Builds

- Allow Diagnostic Data: **Enabled**
  - Options: **Send required diagnostic data** (Pro Edition); or
  - Options: **Diagnostic data off** (Enterprise or Education Edition)
- Limit Diagnostic Log Collection: **Enabled**
- Limit Dump Collection: **Enabled**
- Limit optional diagnostic data for Desktop Analytics: **Enabled**
  - Options: **Disable Desktop Analytics collection**
- Do not show feedback notifications: **Enabled**

#### 檔案總管

- Turn off account-based insights, recent, favorite, and recommended files in File Explorer: **Enabled**

#### MDM

- Disable MDM Enrollment: **Enabled**

#### OneDrive

- Save documents to OneDrive by default: **Disabled**
- Prevent OneDrive from generating network traffic until the user signs in to OneDrive: **Enabled**
- Prevent the usage of OneDrive for file storage: **Enabled**

This last setting disables OneDrive on your system; make sure to change it to **Disabled** if you use OneDrive.

#### Push To Install

- Turn off Push To Install service: **Enabled**

#### 搜尋

- Allow Cortana: **Disabled**
- Don't search the web or display web results in Search: **Enabled**
- Set what information is shared in Search: **Enabled**
  - Type of information: **Anonymous info**

#### 同步設定

- Do not sync: **Enabled**

#### 文本輸入

- Improve inking and typing recognition: **Disabled**

#### Windows 錯誤報告

- Do not send additional data: **Enabled**
- Consent > Configure Default consent: **Enabled**
  - Consent level: **Always ask before sending data**
