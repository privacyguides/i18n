---
title: 写真管理
icon: material/image
description: Photo management tools to keep your personal photos safe from the prying eyes of cloud storage providers and other unauthorized access.
cover: photo-management.webp
---

Most cloud photo management solutions like Google Photos, Flickr, and Amazon Photos don't secure your photos against being accessed by the cloud storage provider themselves. These options keep your personal photos private, while allowing you to share them only with family and trusted people.

## ente

!!! 推奨事項

```
![ente logo](assets/img/photo-management/ente.svg#only-light){ align=right }
![ente logo](assets/img/photo-management/ente-dark.svg#only-dark){ align=right }

**ente** is an end-to-end encrypted photo backup service which supports automatic backups on iOS and Android. It underwent an [audit by Cure53](https://ente.io/blog/cryptography-audit/) in March 2023.

[:octicons-home-16: Homepage](https://ente.io/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ente.io/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ente-io){ .card-link title="Source Code" }

??? downloads

    - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.photos)
    - [:simple-android: Android](https://ente.io/download)
    - [:simple-appstore: App Store](https://apps.apple.com/app/id1542026904)
    - [:simple-github: GitHub](https://github.com/ente-io/photos-app/releases)
    - [:simple-windows11: Windows](https://ente.io/download)
    - [:simple-apple: macOS](https://ente.io/download)
    - [:simple-linux: Linux](https://ente.io/download)
    - [:octicons-globe-16: Web](https://web.ente.io)
```

## Stingle

!!! 推奨事項

```
![Stingle logo](assets/img/photo-management/stingle.png#only-light){ align=right }
![Stingle logo](assets/img/photo-management/stingle-dark.png#only-dark){ align=right }

**Stingle** is a gallery and camera application with built-in, end-to-end encrypted backup and sync functionality for your photos and videos. Storage starts at 1GB for free accounts on their cloud, or you can host your own Stingle API server for total independence.

[:octicons-home-16: Homepage](https://stingle.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://stingle.org/privacy/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://stingle.org/faq/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/stingle){ .card-link title="Source Code" }

??? downloads

    - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.photos)
    - [:simple-android: Android](https://play.google.com/store/apps/details?id=org.stingle.photos)
    - [:simple-appstore: App Store](https://apps.apple.com/in/app/stingle-photos/id1582535448)
    - [:simple-github: GitHub](https://github.com/stingle)
```

## PhotoPrism

!!! 推奨事項

```
![PhotoPrism logo](assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** is a self-hostable platform for managing photos. It supports album syncing and sharing as well as a variety of other [features](https://www.photoprism.app/features). It does not include E2EE, so it's best hosted on a server that you trust and is under your control.

[:octicons-home-16: Homepage](https://www.photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.photoprism.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://www.photoprism.app/kb){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Source Code" }

??? downloads

    - [:simple-github: GitHub](https://github.com/photoprism)
```

## 規準

\*\*私たちは、推薦するどのプロジェクトとも提携していません。\*\*客観的に推薦できるよう、[標準となる規準](about/criteria.md)に加えて、一連の明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

!!! example "この項目は最近作成されました"

```
We are working on establishing defined criteria for every section of our site, and this may be subject to change. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. There are many factors considered and discussed when we recommend a project, and documenting every single one is a work-in-progress.
```

### 最低要件

- Cloud-hosted providers must enforce end-to-end encryption.
- Must offer a free plan or trial period for testing.
- Must support TOTP or FIDO2 multi-factor authentication, or Passkey logins.
- Must offer a web interface which supports basic file management functionality.
- Must allow for easy exports of all files/documents.
- Must use standard, audited encryption.
- Must be open source.

### 満たされることが望ましい基準

- Should have a published audit from a reputable, independent third-party.