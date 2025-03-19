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

[:octicons-home-16: Pagina Principale](https://nextcloud.com/it/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/it/privacy/){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://nextcloud.com/it/support/){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://nextcloud.com/it/contribute/){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
- [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
- [:fontawesome-brands-windows: Windows](https://nextcloud.com/install/#install-clients)
- [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
- [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Attenzione</p>

Sconsigliamo di utilizzare l'[App E2EE](https://apps.nextcloud.com/apps/end_to_end_encryption) per Nextcloud, in quanto potrebbe causare la perdita di dati; è altamente sperimentale e non dispone di una qualità di produzione. For this reason, we don't recommend third-party Nextcloud providers.

</div>

### CryptPad

<div class="admonition recommendation" markdown>

![CryptPad logo](assets/img/document-collaboration/cryptpad.svg){ align=right }

**CryptPad** is a private-by-design alternative to popular office tools. All content on this web service is end-to-end encrypted and can be shared with other users easily. [:material-star-box: Read our latest CryptPad review.](https://www.privacyguides.org/articles/2025/02/07/cryptpad-review/)

[:octicons-home-16: Homepage](https://cryptpad.fr){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptpad.fr/pad/#/2/pad/view/GcNjAWmK6YDB3EO2IipRZ0fUe89j43Ryqeb4fjkjehE){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.cryptpad.fr){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/cryptpad){ .card-link title=Contribute }

</details>

</div>

### Criteri

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

#### Requisiti minimi

In general, we define collaboration platforms as full-fledged suites which could reasonably act as a replacement to Google Drive.

- Deve essere open source.
- Must make files accessible via WebDAV unless it is impossible due to E2EE.
- Must have sync clients for Linux, macOS, and Windows.
- Must support document and spreadsheet editing.
- Must support real-time document collaboration.
- Must support exporting documents to standard document formats (e.g. ODF).

#### Caso migliore

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- Should store files in a conventional filesystem.
- Should support TOTP or FIDO2 multifactor authentication support, or passkey logins.
