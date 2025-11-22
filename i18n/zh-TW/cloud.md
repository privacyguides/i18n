---
meta_title: "最佳私密和安全的雲端儲存服務提供商 - Privacy Guides"
title: 雲端儲存
icon: material/file-cloud
description: 許多雲端儲存服務供應商需要您相信他們不會查看您的檔案。 這些都是私密替代品！
cover: cloud.webp
---

<small>防護下列威脅：</small>

- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

**許多雲端儲存提供商** 要求您完全信任他們不會查看您的檔案。 下列替代方案透過實作安全的端到端加密，消除了對信任的需求。

如果這些替代方案不符合您的需求，建議您考慮使用其他雲端提供商的加密軟體，例如 [Cryptomator](encryption.md#cryptomator-cloud) 。 把 Cryptomator 結合在 **任一種** 雲服務商(包含這裡推薦的) 也是好方法，可減低某服務商原生客戶端加密漏洞之風險。

<details class="admonition info" markdown>
<summary>尋找 Nextcloud?</summary>

對於較具技術背景的讀者來說，Nextcloud [仍是](self-hosting/file-management.md#nextcloud)自架檔案管理套裝軟體的推薦工具，不過我們目前不建議使用第三方 Nextcloud 儲存空間提供者，因為我們[不建議](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29)一般使用者使用 Nextcloud 內建的端到端加密功能。

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Proton Drive logo](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive** 是一個加密雲端儲存提供商，由經營廣受歡迎的加密電子郵件 [Proton Mail](email.md#proton-mail) 的提供商推出。

初始的免費儲存空間限制為 2 GB，但完成[特定步驟](https://proton.me/support/more-free-storage-existing-users)後，可獲得最多 5 GB 的額外儲存空間。

[:octicons-home-16: 首頁](https://proton.me/drive){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/drive/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)
- [:fontawesome-brands-windows: Windows](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

Proton Drive 網頁應用程式已於[2021年](https://proton.me/community/open-source)通過了 Securitum 的獨立稽核，但全新的行動客戶端尚未經過第三方的公開稽核。

## Tresorit

<div class="admonition recommendation" markdown>

![Tresorit logo](assets/img/cloud/tresorit.svg){ align=right }

**Tresorit** 為 2011年創辦於瑞士- 匃牙利的加密雲端儲存供應商。 Tresorit 由瑞士郵政擁有，瑞士郵政是瑞士的國家郵政服務。

[:octicons-home-16: 首頁](https://tresorit.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tresorit.com/legal/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://support.tresorit.com){ .card-link title="說明文件" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.tresorit.mobile)
- [:simple-appstore: App Store](https://apps.apple.com/app/id722163232)
- [:fontawesome-brands-windows: Windows](https://tresorit.com/download)
- [:simple-apple: macOS](https://tresorit.com/download)
- [:simple-linux: Linux](https://tresorit.com/download)

</details>

</div>

Tresorit 已獲得多項獨立安全稽核：

- [2022](https://tresorit.com/blog/tresorit-receives-iso-27001-certification): ISO/IEC 27001:2013[^1] Compliance [Certification](https://certipedia.com/quality_marks/9108644476) by TÜV Rheinland InterCert Kft
- [2021](https://tresorit.com/blog/fresh-penetration-testing-confirms-tresorit-security): Penetration Testing by Computest
    - 該檢查評估了Tresorit 網頁用戶端、Android 應用程式、Windows 應用程式和相關基礎設施的安全性。
    - Computest 發現了兩個已解決的漏洞。
- [2019年](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture)：安永的滲透測試。
    - 該檢測分析了 Tresorit 完整源代碼，並驗證了落實 Tresorit [白皮書](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf)中描述的概念。
    - 安永另外還測試了網路、行動裝置與桌面客戶端。 他們的結論是：

        > 測試結果未發現任何偏離 Tresorit 資料保密性聲明的情況。

他們也獲得了數位信任標籤，這是 [Swiss Digital Initiative](https://efd.admin.ch/en/swiss-digital-initiative-en) 發出的認證，要求通過 [35 項](https://swiss-digital-initiative.org/criteria)與安全、隱私與可靠性相關的標準。

## Peergos

<div class="admonition recommendation" markdown>

![Peergos logo](assets/img/cloud/peergos.svg){ align=right }

**Peergos** 是去中心化協定的儲存、社交媒體和應用程式開源平台。 其提供了安全且私人的空間，讓使用者可以儲存、分享、檢視與編輯他們的照片、影片、文件等等。

Peergos 採用抗量子加密的端到端加密技術保護您的檔案，確保所有檔案相關資料皆保持私密。 其也可以[自行架設](https://book.peergos.org/features/self)。

[:octicons-home-16: 首頁](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://book.peergos.org){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="原始碼" }
[:octicons-heart-16:](https://github.com/peergos/peergos#support){ .card-link title="貢獻" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=peergos.android)
- [:simple-github: GitHub](https://github.com/Peergos/web-ui/releases)
- [:fontawesome-brands-windows: Windows](https://peergos.org/download#windows)
- [:simple-apple: macOS](https://peergos.org/download#macos)
- [:simple-linux: Linux](https://peergos.org/download#linux)
- [:octicons-browser-16: 網頁](https://peergos.net)

</details>

</div>

Peergos 建基於[星際檔案系統 (IPFS)](https://ipfs.tech)，這是點對點的架構，可防止[:material-close-outline:審查](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}。

Peergos 的客戶端、伺服器與命令列介面都是從相同的二進位檔執行。 此外，Peergos 也包含[同步引擎](https://book.peergos.org/features/sync)（可透過原生應用程式存取），用來雙向同步本機資料夾與 Peergos 資料夾，以及 [WebDAV 橋接](https://book.peergos.org/features/webdav)，讓其他應用程式存取您的 Peergos 儲存空間。 欲了解 Peergos 的完整功能概覽，請參閱其官方文件。

Peergos 於2024年11月接受 Radically Open Security 的[稽核](https://peergos.org/posts/security-audit-2024)，所有問題均已修正。 他們先前曾接受 Cure53 的[稽核](https://cure53.de/pentest-report_peergos.pdf)，所有發現的問題隨後都修復了。

## 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 必須強制端到端加密。
- 必須提供免費計劃或試用期以進行測試。
- 必須支援 TOTP 或 FIDO2 多重要素驗證，或允許使用 passkey 登入。
- 必須提供支援基本檔案管理功能的網頁介面。
- 允許輕鬆匯出所有檔案/文件。

### 最佳情況

最佳情況標準代表我們希望在這個類別的完美項目的應具備的特性。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 客戶端應是開源的。
- 客戶端應由獨立第三方進行全面稽核。
- 應提供 Linux、Android、Windows、macOS 和 iOS 的原生客戶端。
    - 這些用戶端應與雲端儲存供應商的原生作業系統工具整合，例如整合 iOS 的 Files app，或 Android 的 DocumentsProvider 功能。
- 應支援與其他使用者輕鬆地分享檔案。
- 至少在網頁界面應提供基本的文件預覽和編輯功能。

[^1]: [ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001): 2013合規性涉及公司的 [資訊安全管理系統](https://en.wikipedia.org/wiki/Information_security_management) ，涵蓋其雲端服務的銷售、開發、維護和支援。
