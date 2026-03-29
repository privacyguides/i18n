---
title: 照片管理
icon: material/image
description: 這些相片管理工具能保護您的個人相片，使其免於雲端儲存服務供應商及其他未經授權者的窺探。
cover: photo-management.webp
---

<small>防護下列威脅：</small>

- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy){ .pg-orange }
- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

大多數的雲端 **照片管理解決方案** ，例如 Google相簿、Flickr 和 Amazon Photos，都無法保護您的照片不被雲端儲存供應商存取。 這些選項可保護您個人相片的隱私，同時允許您僅與家人和信任的人分享。

## Ente Photos

<div class="admonition recommendation" markdown>

![Ente 標誌](assets/img/photo-management/ente.svg){ align=right }

**Ente Photos**提供端對端加密照片備份服務，支援 iOS 和 Android 的自動備份。 其客戶端與伺服器端的程式碼都完全開放原始碼。 它也可 [自行託管](https://github.com/ente-io/ente/tree/main/server#self-hosting)。

免費方案要求您每年至少要使用該服務一次，該方案提供 10 GB 儲存空間。

[:octicons-home-16: Homepage](https://ente.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ente.com/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ente-io/ente){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.photos)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1542026904)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=photos)
- [:simple-android: Android](https://ente.com/download)
- [:fontawesome-brands-windows: Windows](https://ente.com/download)
- [:simple-apple: macOS](https://ente.com/download)
- [:simple-linux: Linux](https://ente.com/download)
- [:octicons-browser-16: 網頁](https://web.ente.io)

</details>

</div>

The server-side source code and infrastructure which underpins Ente Photos underwent an audit by [Cure53](https://ente.com/blog/cern-audit) in October 2025. Previous audits were completed by [Cure53](https://ente.com/blog/cryptography-audit) in March 2023 and by [Fallible](https://ente.com/reports/Fallible-Audit-Report-19-04-2023.pdf) in April 2023.

## 標準

\*\*請注意，我們與推薦的任何專案均無隸屬關係。\*\*除了[我們的通用標準](about/criteria.md)以外，我們還制定了一套明確的要求，讓我們能夠提供客觀的推薦。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 雲端供應商必須執行 E2EE。
- 必須提供免費計劃或試用期以進行測試。
- 必須支援 TOTP 或 FIDO2 多重要素驗證，或允許使用密碼金鑰登入。
- 必須提供支援基本檔案管理功能的網頁介面。
- 允許輕鬆匯出所有檔案/文件。
- 它必須是開源的。

### 最佳實踐

- 應有來自聲譽良好、獨立的第三方公開稽核報告。
