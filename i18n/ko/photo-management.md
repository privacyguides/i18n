---
title: Photo Management
icon: material/image
description: These photo management tools keep your personal photos safe from the prying eyes of cloud storage providers and other unauthorized parties.
cover: photo-management.webp
---

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: Passive Attacks](basics/common-threats.md#security-and-privacy){ .pg-orange }
- [:material-server-network: Service Providers](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

Most cloud **photo management solutions** like Google Photos, Flickr, and Amazon Photos don't secure your photos against being accessed by the cloud storage provider themselves. These options keep your personal photos private, while allowing you to share them only with family and trusted people.

## Ente Photos

<div class="admonition recommendation" markdown>

![Ente logo](assets/img/photo-management/ente.svg){ align=right }

**Ente Photos** is an end-to-end encrypted photo backup service which supports automatic backups on iOS and Android. Their code is fully open source, both on the client side and on the server side. It is also [self-hostable](https://github.com/ente-io/ente/tree/main/server#self-hosting).

The free plan offers 10 GB of storage as long as you use the service at least once a year.

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

Ente Photos underwent an audit by [Cure53](https://ente.io/blog/cryptography-audit) in March 2023 and by [Fallible](https://ente.io/reports/Fallible-Audit-Report-19-04-2023.pdf) in April 2023.

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

## 평가 기준

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

### 최소 요구 사항

- Cloud-hosted providers must enforce E2EE.
- 테스트용 무료 요금제/체험판 기간을 제공해야 합니다.
- Must support TOTP or FIDO2 multifactor authentication, or passkey logins.
- 기본적인 파일 관리 기능을 지원하는 웹 인터페이스를 제공해야 합니다.
- 모든 파일/문서를 쉽게 내보낼 수 있어야 합니다.
- 오픈 소스여야 합니다.

### 우대 사항

- Should have a published audit from a reputable, independent third party.
