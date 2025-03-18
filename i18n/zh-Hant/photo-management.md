---
title: 照片管理
icon: material/image
description: 照片管理工具可確保個人照片免受雲端儲存提供者的窺視和其他未經授權的存取。
cover: photo-management.webp
---

<small>防護下列威脅：</small>

- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy){ .pg-orange }
- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

大多數的雲端 **照片管理解決方案** ，例如 Google相簿、Flickr 和 Amazon Photos，都無法保護您的照片不被雲端儲存供應商存取。 這些選項可保護您個人相片的隱私，同時允許您僅與家人和信任的人分享。

## Ente Photos

<div class="admonition recommendation" markdown>

![Ente logo](assets/img/photo-management/ente.svg#only-light){ align=right }
![Ente logo](assets/img/photo-management/ente-dark.svg#only-dark){ align=right }

**Ente Photos**提供端對端加密照片備份服務，支援 iOS 和 Android 的自動備份。 其客戶端和伺服器端的程式碼都完全開源。 它也可 [自行託管](https://github.com/ente-io/ente/tree/main/server#self-hosting)。 The free plan offers 5 GB of storage as long as you use the service at least once a year.

[:octicons-home-16: 首頁](https://ente.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://ente.io/faq){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/ente-io/ente){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.photos)
- [:simple-android: Android](https://ente.io/download)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1542026904)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=photos)
- [:fontawesome-brands-windows: Windows](https://ente.io/download)
- [:simple-apple: macOS](https://ente.io/download)
- [:simple-linux: Linux](https://ente.io/download)
- [:octicons-globe-16: 網頁版](https://web.ente.io)

</details>

</div>

Ente Photos 於 2023 年 3 月接受 [Cure53 稽核](https://ente.io/blog/cryptography-audit) ，並於 2023 年 4 月接受 [Fallible 稽核](https://ente.io/reports/Fallible-Audit-Report-19-04-2023.pdf) 。

## Stingle

<div class="admonition recommendation" markdown>

![Stingle logo](assets/img/photo-management/stingle.png#only-light){ align=right }
![Stingle logo](assets/img/photo-management/stingle-dark.png#only-dark){ align=right }

**Stingle** 是一款照片庫與相機應用程式，內建端對端加密備份與同步功能，可儲存您的相片與影片。 Storage starts at 1 GB for free accounts on their cloud, or you can host your own Stingle API server for total independence.

[:octicons-home-16: 首頁](https://stingle.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://stingle.org/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://stingle.org/faq){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/stingle){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.stingle.photos)
- [:simple-android: Android](https://f-droid.org/en/packages/org.stingle.photos)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1582535448)
- [:simple-github: GitHub](https://github.com/stingle/stingle-photos-android/releases)

</details>

</div>

## PhotoPrism

<div class="admonition recommendation" markdown>

![PhotoPrism logo](assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** 是一個可 自行託管 的相片管理平台。 它支援相簿同步與分享，以及多個 [功能](https://photoprism.app/features)。 它在設計上未採納 E2EE，因此最好託管在您信任且在您控制之下的伺服器上。

[:octicons-home-16: 首頁](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>

## 標準

\*\*請注意，我們與推薦的任何項目均無關。\*\*除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 雲端託管提供商必須強制執行端對端加密。
- 必須提供免費方案或試用期以進行測試。
- Must support TOTP or FIDO2 multifactor authentication, or passkey logins.
- 必須提供支援基本檔案管理功能的網頁介面。
- 允許輕鬆匯出所有檔案/文件。
- 它必須是開源的。

### 最佳實踐

- 應有來自聲譽良好、獨立的第三方公開稽核報告。
