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

[:octicons-home-16: Page d'accueil](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Code source" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

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

Nous ne recommandons pas l'utilisation de [l'application E2EE](https://apps.nextcloud.com/apps/end_to_end_encryption) pour Nextcloud car elle peut entraîner une perte de données ; elle est hautement expérimentale et n'est pas de qualité de production. For this reason, we don't recommend third-party Nextcloud providers.

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

### Critères

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

#### Exigences minimales

In general, we define collaboration platforms as full-fledged suites which could reasonably act as a replacement to Google Drive.

- Doit être open-source.
- Must make files accessible via WebDAV unless it is impossible due to E2EE.
- Must have sync clients for Linux, macOS, and Windows.
- Must support document and spreadsheet editing.
- Must support real-time document collaboration.
- Must support exporting documents to standard document formats (e.g. ODF).

#### Dans le meilleur des cas

Nos critères de cas idéal représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de cette fonctionnalité, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Should store files in a conventional filesystem.
- Should support TOTP or FIDO2 multi-factor authentication support, or passkey logins.