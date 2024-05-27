---
title: 照片管理
icon: material/image
description: 照片管理工具可確保個人照片免受雲端儲存提供者的窺視和其他未經授權的存取。
cover: photo-management.webp
---

大多數雲端照片管理方案（例如 Google Photos、Flickr 和 Amazon Photos）無法保護您的照片不被雲端儲存供應商存取。 這些選項可保密個人照片，同時允許您僅與家人和信任的人分享。

## ente

<div class="admonition recommendation" markdown>

![ente logo](assets/img/photo-management/ente.svg#only-light){ align=right }
![ente logo](assets/img/photo-management/ente-dark.svg#only-dark){ align=right }

**ente**提供端對端加密照片備份服務，支援 iOS 和 Android 的自動備份。 其客戶端和伺服器端的程式碼都完全開源。 它可以 [自行託管](https://github.com/ente-io/ente/tree/main/server#self-hosting). 它分別於2023 年3 月接受了[Cure53](https://ente.io/blog/cryptography-audit) 和 2023 年 4 月[Fallible](https://ente.io/reports/Fallible-Audit-Report-19-04-2023.pdf)審核。 免費試用有1年份的 1GB 儲存容量。

[:octicons-home-16: Homepage](https://ente.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ente.io/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ente-io){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.photos)
- [:simple-android: Android](https://ente.io/download)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1542026904)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases)
- [:simple-windows11: Windows](https://ente.io/download)
- [:simple-apple: macOS](https://ente.io/download)
- [:simple-linux: Linux](https://ente.io/download)
- [:octicons-globe-16: Web](https://web.ente.io)

</details>

</div>

## Stingle

<div class="admonition recommendation" markdown>

![Stingle logo](assets/img/photo-management/stingle.png#only-light){ align=right }
![Stingle logo](assets/img/photo-management/stingle-dark.png#only-dark){ align=right }

**Stingle** 是一款圖庫和相機應用程序，內建端對端加密備份和同步功能，適用於照片和影片。 免費帳戶的雲端儲存空間為 1GB，或者自行託管 Stingle API 伺服器來實現完全獨立。

[:octicons-home-16: Homepage](https://stingle.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://stingle.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://stingle.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/stingle){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.stingle.photos)
- [:simple-android: Android](https://f-droid.org/en/packages/org.stingle.photos)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1582535448)
- [:simple-github: GitHub](https://github.com/stingle)

</details>

</div>

## PhotoPrism

<div class="admonition recommendation" markdown>

![PhotoPrism logo](assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** 是一個管理照片的自架平台。 支援相簿同步和共享以及各種其他[功能](https://photoprism.app/features)。 它不包括 E2EE，因此最好將其託管在信任且能控制的伺服器上。

[:octicons-home-16: Homepage](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>

## 標準

請注意，我們所推薦專案沒有任何瓜葛。 除[標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 雲端託管提供者須強制執行端對端加密。
- 必須提供免費計劃或試用期以進行測試。
- 必須支援 TOTP 或 FIDO2 多因素驗證，或 Passkey 登入。
- 必須提供支援基本檔案管理功能的網頁介面。
- 允許輕鬆匯出所有檔案/文件。
- 必須使用經審核的標準加密。
- 它必須是開源的。

### 最佳案例：

- 應有來自聲譽良好、獨立的第三方公開審查報告。
