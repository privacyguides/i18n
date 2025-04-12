---
meta_title: "最佳私密和安全的雲端儲存服務提供商 - Privacy Guides"
title: "雲端儲存"
icon: material/file-cloud
description: 許多雲端儲存服務供應商需要您相信他們不會查看您的檔案。 這些都是私密替代品！
cover: cloud.webp
---

<small>防護下列威脅：</small>

- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

**許多雲端儲存提供商** 要求您完全信任他們不會查看您的檔案。 下面列出的替代方案通過實施安全的 E2EE，消除了對信任的需要。

如果這些替代方案不符合您的需求，建議您考慮使用其他雲端提供商的加密軟體，例如 [Cryptomator](encryption.md#cryptomator-cloud) 。 把 Cryptomator 結合在 **任一種** 雲服務商(包含這裡推薦的) 也是好方法，可減低某服務商原生客戶端加密漏洞之風險。

<details class="admonition info" markdown>
<summary>尋找 Nextcloud?</summary>

Nextcloud [仍是](document-collaboration.md#nextcloud) 自我託管檔案管理套件的推薦工具，然而我們目前不推薦第三方 Nextcloud 儲存提供商，因為我們 [不建議](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) 普通使用者使用 Nextcloud 內建的 E2EE 功能。

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Proton Drive logo](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive** 是一個加密雲端儲存提供商，由經營廣受歡迎的加密電子郵件 [Proton Mail](email.md#proton-mail) 的提供商推出。 The initial free storage is limited to 2 GB, but with the completion of [certain steps](https://proton.me/support/more-free-storage-existing-users), additional storage can be obtained up to 5 GB.

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

Proton Drive 網路應用程式已於 [2021](https://proton.me/community/open-source) 接受了 Securitum 獨立審核。

Proton Drive 全新移動客戶端軟體尚未經過第三方公開審核。

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
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): Penetration Testing by Ernst & Young.
    - 該檢測分析了 Tresorit 完整源代碼，並驗證了落實 Tresorit [白皮書](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf)中描述的概念。
    - Ernst & Young 還測試了網路、行動和桌面客戶端： “測試結果發現沒有偏離 Tresorit 的資料機密性聲明。

他們還獲得了數位信任標籤（Digital Trust Label），這是 [Swiss Digital Initiative](https://efd.admin.ch/en/swiss-digital-initiative-en) 發出的認證，要求通過[35 項](https://swiss-digital-initiative.org/criteria)與安全性、隱私性和可靠性相關的標準。

## Peergos

<div class="admonition recommendation" markdown>

![Peergos logo](assets/img/cloud/peergos.svg){ align=right }

**Peergos** 是去中心化協定的儲存、社交媒體和應用程式開源平台。 其提供安全且私密的空間，用戶可以在其中儲存、分享和查看照片、影片、文件等。 Peergos 透過抗量子端對端加密來保護檔案，並確保有關檔案所有資料保持私密。

[:octicons-home-16: Homepage](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://book.peergos.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/peergos/peergos#support){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=peergos.android)
- [:simple-github: GitHub](https://github.com/Peergos/web-ui/releases)
- [:fontawesome-brands-windows: Windows](https://github.com/Peergos/web-ui/releases)
- [:simple-apple: macOS](https://github.com/Peergos/web-ui/releases)
- [:simple-linux: Linux](https://github.com/Peergos/web-ui/releases)
- [:octicons-browser-16: Web](https://peergos.net)

</details>

</div>

Peergos is built on top of the [InterPlanetary File System (IPFS)](https://ipfs.tech), a peer-to-peer architecture that protects against [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}.

Peergos is primarily a web app, but you can self-host the server either as a local cache for your remote Peergos account, or as a standalone storage server which negates the need to register for a remote account and subscription. The Peergos server is a `.jar` file, which means the Java 17+ Runtime Environment ([OpenJDK download](https://azul.com/downloads)) should be installed on your machine to get it working.

Running a local version of Peergos alongside a registered account on their paid, hosted service allows you to access your Peergos storage without any reliance on DNS or TLS certificate authorities, and keep a copy of your data backed up to their cloud. The user experience should be the same whether you run their desktop server or just use their hosted web interface.

Peergos was [audited](https://peergos.org/posts/security-audit-2024) in November 2024 by Radically Open Security and all issues were fixed. They were previously [audited](https://cure53.de/pentest-report_peergos.pdf) by Cure53 in June 2019, and all found issues were subsequently fixed.

## 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 必須執行端對端加密。
- 必須提供免費計劃或試用期以進行測試。
- Must support TOTP or FIDO2 multifactor authentication, or passkey logins.
- 必須提供支援基本檔案管理功能的網頁介面。
- 允許輕鬆匯出所有檔案/文件。

### 最佳情況

最佳情況標準代表我們希望在這個類別的完美項目的應具備的特性。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 客戶端應是開源的。
- 客戶端軟體應由獨立的第三方進行全面審計。
- 應提供 Linux、Android、Windows、macOS 和 iOS 的原生客戶端。
    - 這些用戶端應與雲端儲存供應商的原生作業系統工具整合，例如整合 iOS 的 Files app，或 Android 的 DocumentsProvider 功能。
- 容易與其他用戶輕鬆共享文件。
- 至少在網頁界面應提供基本的文件預覽和編輯功能。

[^1]: [ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001): 2013合規性涉及公司的 [資訊安全管理系統](https://en.wikipedia.org/wiki/Information_security_management) ，涵蓋其雲端服務的銷售、開發、維護和支援。
