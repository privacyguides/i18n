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

**ente**提供端對端加密照片備份服務，支援 iOS 和 Android 的自動備份。 Their code is fully open-source, both on the client side and on the server side. It is [self-hostable](https://github.com/ente-io/ente/tree/main/server#self-hosting). It underwent an [audit by Cure53](https://ente.io/blog/cryptography-audit/) in March 2023 and by [Fallible](https://ente.io/reports/Fallible-Audit-Report-19-04-2023.pdf) in April 2023.

[:octicons-home-16: Homepage](https://ente.io/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ente.io/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ente-io){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "下載"</summary>

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

[:octicons-home-16: Homepage](https://stingle.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://stingle.org/privacy/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://stingle.org/faq/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/stingle){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "下載"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.stingle.photos)
- [:simple-android: Android](https://f-droid.org/en/packages/org.stingle.photos/)
- [:simple-appstore: App Store](https://apps.apple.com/in/app/stingle-photos/id1582535448)
- [:simple-github: GitHub](https://github.com/stingle)

</details>

</div>

## PhotoPrism

<div class="admonition recommendation" markdown>

![PhotoPrism logo](assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** 是一個管理照片的自架平台。 它支援相簿同步和共享以及各種其他[功能](https://www.photoprism.app/features)。 它不包括 E2EE，因此最好將其託管在信任且能控制的伺服器上。

[:octicons-home-16: Homepage](https://www.photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.photoprism.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://www.photoprism.app/kb){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "下載"</summary>

- [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>

## 標準

請注意，我們所推薦專案沒有任何瓜葛。 除[標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

<div class="admonition example" markdown>
<p class="admonition-title">此部份新增</p>

我們正在努力為我們網站的每個部分建立定義的標準，這可能會有所變化。 如果您對我們的標準有任何疑問，請在 [論壇上提問](https://discuss.privacyguides.net/latest) ，如果沒有列出，請不要認為我們在提出建議時沒有考慮到某些事情。 當我們推薦一個項目時，有許多因素被考慮和討論，記錄每一個項目都是正在進行式。

</div>

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
