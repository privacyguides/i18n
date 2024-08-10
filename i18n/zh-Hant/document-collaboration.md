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
<summary>下載</summary>

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

我們不建議使用 Nextcloud [E2EE App](https://apps.nextcloud.com/apps/end_to_end_encryption) ，因為它可能會導致資料丟失；目前它仍是高度實驗性，未達穩定品質。 For this reason, we don't recommend third-party Nextcloud providers.

</div>

### CryptPad

<div class="admonition recommendation" markdown>

![CryptPad logo](assets/img/document-collaboration/cryptpad.svg){ align=right }

**CryptPad** is a private-by-design alternative to popular office tools. All content on this web service is end-to-end encrypted and can be shared with other users easily.

[:octicons-home-16: Homepage](https://cryptpad.fr){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptpad.fr/pad/#/2/pad/view/GcNjAWmK6YDB3EO2IipRZ0fUe89j43Ryqeb4fjkjehE){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.cryptpad.fr){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/cryptpad){ .card-link title=Contribute }

</details>

</div>

### 標準

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

#### 最低合格要求

In general, we define collaboration platforms as full-fledged suites which could reasonably act as a replacement to Google Drive.

- 它必須是開源的。
- Must make files accessible via WebDAV unless it is impossible due to E2EE.
- Must have sync clients for Linux, macOS, and Windows.
- Must support document and spreadsheet editing.
- Must support real-time document collaboration.
- Must support exporting documents to standard document formats (e.g. ODF).

#### 最佳案例

最佳案例標準代表了我們希望從這個類別的完美項目應具備的功能。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- Should store files in a conventional filesystem.
- Should support TOTP or FIDO2 multi-factor authentication support, or passkey logins.
