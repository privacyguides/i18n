---
title: Document Collaboration
icon: material/account-group
description: Most online office suites do not support E2EE, meaning the cloud provider has access to everything you do.
cover: document-collaboration.webp
---

<small>Protects against the following threat(s):</small>

- [:material-server-network: Service Providers](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

Most online office suites do not support E2EE, meaning the cloud provider has access to everything you do. The provider's privacy policy may legally protect your rights, but it does not provide technical access constraints.

## Collaboration Platforms

### Nextcloud

<div class="admonition recommendation" markdown>

![Nextcloud logo](assets/img/document-collaboration/nextcloud.svg){ align=right }

**Nextcloud** is a suite of free and open-source client-server software for creating your own file hosting services on a private server you control.

[:octicons-home-16: Homepage](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Source Code" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
- [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
- [:fontawesome-brands-windows: Windows](https://nextcloud.com/install/#install-clients)
- [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
- [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Privacy Guides는 Nextcloud용 [E2EE 앱](https://apps.nextcloud.com/apps/end_to_end_encryption)을 사용하는 것을 권장드리지 않습니다. 데이터 손실이 발생할 수 있고, 실험적인 성향이 강하며, 실사용할 만한 품질이 아니기 때문입니다. For this reason, we don't recommend third-party Nextcloud providers.

</div>

### CryptPad

<div class="admonition recommendation" markdown>

![CryptPad logo](assets/img/document-collaboration/cryptpad.svg){ align=right }

**CryptPad** is a private-by-design alternative to popular office tools. All content on this web service is end-to-end encrypted and can be shared with other users easily. [:material-star-box: Read our latest CryptPad review.](https://www.privacyguides.org/articles/2025/02/07/cryptpad-review)

[:octicons-home-16: Homepage](https://cryptpad.fr){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptpad.fr/pad/#/2/pad/view/GcNjAWmK6YDB3EO2IipRZ0fUe89j43Ryqeb4fjkjehE){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.cryptpad.fr){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/cryptpad){ .card-link title=Contribute }

</details>

</div>

### 평가 기준

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

#### 최소 요구 사항

In general, we define collaboration platforms as full-fledged suites which could reasonably act as a replacement to Google Drive.

- 오픈 소스여야 합니다.
- Must make files accessible via WebDAV unless it is impossible due to E2EE.
- Must have sync clients for Linux, macOS, and Windows.
- Must support document and spreadsheet editing.
- Must support real-time document collaboration.
- Must support exporting documents to standard document formats (e.g. ODF).

#### 우대 사항

평가 기준에서 '우대 사항'은 해당 부문에서 완벽한 프로젝트에 기대하는 바를 나타냅니다. 다음의 우대 사항에 해당하지 않더라도 권장 목록에 포함될 수 있습니다. 단, 우대 사항에 해당할수록 이 페이지의 다른 항목보다 높은 순위를 갖습니다.

- Should store files in a conventional filesystem.
- Should support TOTP or FIDO2 multifactor authentication support, or passkey logins.
