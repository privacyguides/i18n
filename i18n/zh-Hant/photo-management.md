---
title: "照片管理"
icon: material/image
description: These photo management tools keep your personal photos safe from the prying eyes of cloud storage providers and other unauthorized parties.
cover: photo-management.webp
---

<small>防護下列威脅：</small>

- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy){ .pg-orange }
- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

大多數的雲端 **照片管理解決方案** ，例如 Google相簿、Flickr 和 Amazon Photos，都無法保護您的照片不被雲端儲存供應商存取。 這些選項可保護您個人相片的隱私，同時允許您僅與家人和信任的人分享。

## Ente Photos

<div class="admonition recommendation" markdown>

![Ente logo](assets/img/photo-management/ente.svg){ align=right }

**Ente Photos**提供端對端加密照片備份服務，支援 iOS 和 Android 的自動備份。 Their code is fully open source, both on the client side and on the server side. 它也可 [自行託管](https://github.com/ente-io/ente/tree/main/server#self-hosting)。

The free plan offers 5 GB of storage as long as you use the service at least once a year.

[:octicons-home-16: Homepage](https://ente.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ente.io/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ente-io/ente){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.photos)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1542026904)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=photos)
- [:simple-android: Android](https://ente.io/download)
- [:fontawesome-brands-windows: Windows](https://ente.io/download)
- [:simple-apple: macOS](https://ente.io/download)
- [:simple-linux: Linux](https://ente.io/download)
- [:octicons-browser-16: Web](https://web.ente.io)

</details>

</div>

Ente Photos underwent an [audit by Cure53](https://ente.io/blog/cryptography-audit) in March 2023 and by [Fallible](https://ente.io/reports/Fallible-Audit-Report-19-04-2023.pdf) in April 2023.

## Stingle

<div class="admonition recommendation" markdown>

![Stingle logo](assets/img/photo-management/stingle.png#only-light){ align=right }
![Stingle logo](assets/img/photo-management/stingle-dark.png#only-dark){ align=right }

**Stingle** is a gallery and camera application with built-in, E2EE backup and sync functionality for your photos and videos.

Storage starts at 1 GB for free accounts on their cloud, or you can host your own Stingle API server for total independence.

[:octicons-home-16: Homepage](https://stingle.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://stingle.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://stingle.org/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/stingle){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.stingle.photos)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1582535448)
- [:simple-github: GitHub](https://github.com/stingle/stingle-photos-android/releases)

</details>

</div>

## PhotoPrism

<div class="admonition recommendation" markdown>

![PhotoPrism logo](assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** is a self-hostable platform for managing photos. It supports album syncing and sharing as well as a variety of other [features](https://photoprism.app/features). It does not include E2EE, so it's best hosted on a server that you trust and is under your control.

[:octicons-home-16: Homepage](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>

## 標準

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- Cloud-hosted providers must enforce E2EE.
- 必須提供免費計劃或試用期以進行測試。
- Must support TOTP or FIDO2 multifactor authentication, or passkey logins.
- 必須提供支援基本檔案管理功能的網頁介面。
- 允許輕鬆匯出所有檔案/文件。
- 它必須是開源的。

### 最佳實踐

- Should have a published audit from a reputable, independent third party.
