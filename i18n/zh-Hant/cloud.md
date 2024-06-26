---
meta_title: "最佳私有和安全的雲端儲存服務提供商 - Privacy Guides"
title: "雲端儲存"
icon: material/file-cloud
description: 許多雲端儲存服務供應商需要您相信他們不會查看您的檔案。 這些都是私密替代品！
cover: cloud.webp
---

許多雲端儲存服務供應商需要您完全信任他們不會查看您的檔案。 下面列出的替代方案通過實施安全的 E2EE，消除了對信任的需要。

如果這些替代方案不符合您的需求，建議您考慮使用其他雲端提供商的加密軟件，例如 [Cryptomator](encryption.md#cryptomator-cloud) 。 把 Cryptomator 結合在 **任一種** 雲服務商(包含這裡推薦的) 也是好方法，可減低某服務商原生客立端加密漏洞之風險。

<details class="TYPE" markdown>
<summary>尋找 Nextcloud?</summary>

Nextcloud 是[仍是一款受推薦的工具](productivity.md)，可用於自我託管檔案管理套件，但目前不推薦第三方 Nextcloud儲存服務提供商，我們 [[不建議使用 ](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29)Nextcloud 家庭用戶版內置的 E2EE 功能。

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Proton Drive logo](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive** 是來自流行的加密電子郵件供應商[Proton Mail](email.md#proton-mail)的瑞士加密雲存儲供應商。 一開始免費儲存空間僅 2GB，但完成某些步驟後，可獲得最多 5GB 的額外儲存空間。

[:octicons-home-16: Homepage](https://proton.me/drive){ class="md-button md-button--primary" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)
- [:simple-windows11: Windows](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

Proton Drive 網路應用程式已於 [2021](https://proton.me/community/open-source) 接受了 Securitum 獨立審核。

Proton Drive 全新移動客戶端軟體尚未經過第三方公開審核。

## Tresorit

<div class="admonition recommendation" markdown>

![Tresorit logo](assets/img/cloud/tresorit.svg){ align=right }

**Tresorit** 為 2011年創辦於瑞士- 匃牙利的加密雲端儲存供應商。 Tresorit 由瑞士郵政擁有，瑞士郵政是瑞士的國家郵政服務。

[:octicons-home-16: Homepage](https://tresorit.com){ class="md-button md-button--primary" }
[:octicons-eye-16:](https://tresorit.com/legal/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.tresorit.com){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.tresorit.mobile)
- [:simple-appstore: App Store](https://apps.apple.com/app/id722163232)
- [:simple-windows11: Windows](https://tresorit.com/download)
- [:simple-apple: macOS](https://tresorit.com/download)
- [:simple-linux: Linux](https://tresorit.com/download)

</details>

</div>

Tresorit 已獲得多項獨立安全稽核：

- [2022](https://tresorit.com/blog/tresorit-receives-iso-27001-certification): ISO/IEC 27001:2013[^1] Compliance [Certification](https://certipedia.com/quality_marks/9108644476) by TÜV Rheinland InterCert Kft
- [2021](https://tresorit.com/blog/fresh-penetration-testing-confirms-tresorit-security): Penetration Testing by Computest
    - 該檢查評估了Tresorit 網頁用戶端、Android 應用程式、Windows 應用程式和相關基礎設施的安全性。
    - Computest 發現了兩個已解決的漏洞。
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): Penetration Testing by Ernst & Young.
    - 該檢測分析了 Tresorit 完整源代碼，並驗證了落實 Tresorit [白皮書](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf)中描述的概念。
    - Ernst & Young 還測試了網絡、行動和桌面客戶端： “測試結果發現沒有偏離 Tresorit 的資料機密性聲明。

他們還獲得了數位信任標籤，這是 [Swiss Digital Initiative](https://www.efd.admin.ch/efd/en/home/digitalisierung/swiss-digital-initiative.html) 的認證，該認證要求通過與安全性，隱私和可靠性相關的 [35標準](https://digitaltrust-label.swiss/criteria) 。

## Peergos

<div class="admonition recommendation" markdown>

![Peergos logo](assets/img/cloud/peergos.svg){ align=right }

**Peergos** 是去中心化協定的儲存、社交媒體和應用程式開源平台。 其提供安全且私密的空間，用戶可以在其中儲存、分享和查看照片、影片、文件等。 Peergos 透過抗量子端對端加密來保護檔案，並確保有關檔案所有資料保持私密。 它建構在 [IPFS（星際檔案系統）](https://ipfs.tech) 。

[:octicons-home-16: Homepage](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://book.peergos.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:octicons-globe-16: 網頁版](https://peergos.net)
- [:simple-windows11: Windows](https://github.com/Peergos/web-ui/releases)
- [:simple-apple: macOS](https://github.com/Peergos/web-ui/releases)
- [:simple-linux: Linux](https://github.com/Peergos/web-ui/releases)

</details>

</div>

Peergos 主要為 Web 應用程序，但可自行託管伺服器，作為遠端 Peergos 帳戶的本地緩存，或作為獨立的儲存伺服器，無需註冊遠端帳戶和訂閱。 Peergos 伺服器是 `.jar` 檔案，這表示 Java 17+ 執行時間環境（[OpenJDK 下載](https://azul.com/downloads)）應該是安裝在電腦上以使其正常工作。

透過註冊帳戶在其付費託管服務上運行本地版本的 Peergos ，用戶可在不依賴 DNS 或 TLS 憑證授權單位的情況下存取 Peergos 存儲，並將資料副本備份到其雲端。 無論運行他們的桌面伺服器還是僅使用他們的託管 Web 介面，使用者體驗都應該是相同的。

Peergos 於 2019 年 9 月接受了 Cure53 的[審核](https://cure53.de/pentest-report_peergos.pdf)，所有發現的問題隨後都做了修復。

此外，它還沒有 Android 應用程式，但已在 [開發中](https://discuss.privacyguides.net/t/peergos-private-storage-sharing-social-media-and-application-platform/11825/25)。 目前的解決方法是改用移動 [PWA](https://peergos.net)。

## 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 必須執行端到端加密。
- 必須提供免費計劃或試用期以進行測試。
- 必須支援 TOTP 或 FIDO2 多因素驗證，或密鑰登入。
- 必須提供支援基本檔案管理功能的網頁介面。
- 允許輕鬆匯出所有檔案/文件。
- 必須使用經審核的標準加密。

### 最好的情况

最佳案例標準代表了我們希望從這個類別的完美項目應具備的條件。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 客戶端應是開源的。
- 客戶端軟體應由獨立的第三方進行全面審計。
- 應提供 Linux、Android、Windows、macOS 和 iOS 的原生客戶端。
    - 這些用戶端應與雲端儲存供應商的原生作業系統工具整合，例如整合 iOS 的 Files app，或 Android 的 DocumentsProvider 功能。
- 容易與其他用戶輕鬆共享文件。
- 至少在網頁界面應提供基本的文件預覽和編輯功能。

[^1]: [ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001): 2013合規性涉及公司的 [資訊安全管理系統](https://en.wikipedia.org/wiki/Information_security_management) ，涵蓋其雲端服務的銷售、開發、維護和支援。
