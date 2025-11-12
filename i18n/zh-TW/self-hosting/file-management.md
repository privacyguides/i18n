---
title: 檔案管理
meta_title: "自行架設檔案管理工具 - Privacy Guides"
icon: material/file-multiple-outline
description: 對於技術能力較高的讀者，自行架設檔案管理工具可最大限度地管控您的資料，提供更多的隱私保護。
cover: cloud.webp
---

<small>防護下列威脅：</small>

- [:material-server-network: 服務供應商](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

自行架設自己的**檔案管理**工具可能是個好主意，可降低雲端服務供應商的原生軟體本身加密機制有瑕疵的風險。

## 照片管理

### PhotoPrism

<div class="admonition recommendation" markdown>

![PhotoPrism 圖示](../assets/img/self-hosting/photoprism.svg){ align=right }

**PhotoPrism** 是一個管理相片的平台。 它支援相簿同步和分享，以及一系列其他[功能](https://photoprism.app/features)。 它不包含端對端加密，因此最好架設在您信任，且由您控制的伺服器上。

[:octicons-home-16: 首頁](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="原始碼" }

</div>

## 檔案分享和同步

### FreedomBox

<div class="admonition recommendation" markdown>

![FreedomBox 圖示](../assets/img/self-hosting/freedombox.svg){ align=right }

**FreedomBox** 是一套設計在[單板電腦（SBC）](https://en.wikipedia.org/wiki/Single-board_computer)上運作的作業系統。 其目的是讓架設檔案分享之類的伺服器應用程式變得容易。

[:octicons-home-16: 首頁](https://freedombox.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title="文件" }
[:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="原始碼" }
[:octicons-heart-16:](https://freedomboxfoundation.org/donate){ .card-link title="捐款" }

</div>

### Nextcloud

<div class="admonition recommendation" markdown>

![Nextcloud 圖示](../assets/img/self-hosting/nextcloud.svg){ align=right }

**Nextcloud** 是一套自由及開放原始碼的用戶端-伺服器軟體，可在您控制的私人伺服器上建立自己的檔案託管服務。

[:octicons-home-16: 首頁](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="原始碼" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title="捐款" }

<details class="downloads" markdown><summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
- [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
- [:fontawesome-brands-windows: Windows](https://nextcloud.com/install/#install-clients)
- [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
- [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger "危險"</p>

我們不建議使用 Nextcloud [E2EE App](https://apps.nextcloud.com/apps/end_to_end_encryption) ，因為它可能會導致資料丟失；目前它仍是高度實驗性，未達穩定品質。 因此，我們不推薦第三方 Nextcloud 提供商。

</div>
