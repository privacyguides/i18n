---
title: Gestion des photos
icon: material/image
description: These photo management tools keep your personal photos safe from the prying eyes of cloud storage providers and other unauthorized parties.
cover: photo-management.webp
---

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: Passive Attacks](basics/common-threats.md#security-and-privacy){ .pg-orange }
- [:material-server-network: Service Providers](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

Most cloud **photo management solutions** like Google Photos, Flickr, and Amazon Photos don't secure your photos against being accessed by the cloud storage provider themselves. Ces options préservent la confidentialité de vos photos personnelles, tout en vous permettant de ne les partager qu'avec votre famille et des personnes de confiance.

## Ente Photos

<div class="admonition recommendation" markdown>

![Ente logo](assets/img/photo-management/ente.svg){ align=right }

**Ente Photos** is an end-to-end encrypted photo backup service which supports automatic backups on iOS and Android. Their code is fully open source, both on the client side and on the server side. It is also [self-hostable](https://github.com/ente-io/ente/tree/main/server#self-hosting).

Le plan gratuit offre 10 Go de stockage à condition que vous utilisiez le service au moins une fois par an.

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

Ente Photos a fait l'objet d'un audit par [Cure53](https://ente.io/blog/cryptography-audit) en mars 2023 et par [Fallible](https://ente.io/reports/Fallible-Audit-Report-19-04-2023.pdf) en avril 2023.

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

## Critères

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Cloud-hosted providers must enforce E2EE.
- Doit avoir une offre gratuite ou une période d'essai pour les tests.
- Must support TOTP or FIDO2 multifactor authentication, or passkey logins.
- Doit offrir une interface web prennant en charge les fonctionnalités de base de gestion des fichiers.
- Doit permettre d'exporter facilement tous les fichiers/documents.
- Doit être open-source.

### Dans le meilleur des cas

- Should have a published audit from a reputable, independent third party.
