---
title: Gestion des photos
icon: material/image
description: Outils de gestion des photos pour protéger vos photos personnelles des regards indiscrets des fournisseurs de stockage cloud et d'autres accès non autorisés.
cover: photo-management.webp
---

La plupart des solutions cloud de gestion de photos, telles que Google Photos, Flickr et Amazon Photos, ne protègent pas vos photos contre l'accès par le fournisseur de stockage cloud lui-même. Ces options préservent la confidentialité de vos photos personnelles, tout en vous permettant de ne les partager qu'avec votre famille et des personnes de confiance.

## Ente Photos

<div class="admonition recommendation" markdown>

![Ente logo](assets/img/photo-management/ente.svg#only-light){ align=right }
![Ente logo](assets/img/photo-management/ente-dark.svg#only-dark){ align=right }

**Ente Photos** is an end-to-end encrypted photo backup service which supports automatic backups on iOS and Android. Their code is fully open-source, both on the client side and on the server side. It is [self-hostable](https://github.com/ente-io/ente/tree/main/server#self-hosting). It underwent an [audit by Cure53](https://ente.io/blog/cryptography-audit) in March 2023 and by [Fallible](https://ente.io/reports/Fallible-Audit-Report-19-04-2023.pdf) in April 2023. The free trial offers 5GB of storage, for a year.

[:octicons-home-16: Homepage](https://ente.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ente.io/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ente-io/ente){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.photos)
- [:simple-android: Android](https://ente.io/download)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1542026904)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=photos)
- [:fontawesome-brands-windows: Windows](https://ente.io/download)
- [:simple-apple: macOS](https://ente.io/download)
- [:simple-linux: Linux](https://ente.io/download)
- [:octicons-globe-16: Web](https://web.ente.io)

</details>

</div>

## Stingle

<div class="admonition recommendation" markdown>

![logo Stingle](assets/img/photo-management/stingle.png#only-light){ align=right }
![logo Stingle](assets/img/photo-management/stingle-dark.png#only-dark){ align=right }

**Stingle** est une application de galerie et d'appareil photo avec une fonctionnalité intégrée de sauvegarde et de synchronisation chiffrée de bout en bout pour vos photos et vos vidéos. Le stockage commence à 1 Go pour les comptes gratuits sur leur cloud, ou vous pouvez héberger votre propre serveur API Stingle pour une indépendance totale.

[:octicons-home-16: Homepage](https://stingle.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://stingle.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://stingle.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/stingle){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.stingle.photos)
- [:simple-android: Android](https://f-droid.org/en/packages/org.stingle.photos)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1582535448)
- [:simple-github: GitHub](https://github.com/stingle/stingle-photos-android/releases)

</details>

</div>

## PhotoPrism

<div class="admonition recommendation" markdown>

![logo PhotoPrism](assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** est une plateforme auto-hébergée pour la gestion des photos. It supports album syncing and sharing as well as a variety of other [features](https://photoprism.app/features). Elle n'inclut pas le E2EE, il est donc préférable de l'héberger sur un serveur en lequel vous avez confiance et que vous contrôlez.

[:octicons-home-16: Homepage](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Les fournisseurs à hébergement cloud doivent appliquer du chiffrement de bout en bout.
- Doit avoir une offre gratuite ou une période d'essai pour les tests.
- Must support TOTP or FIDO2 multi-factor authentication, or passkey logins.
- Doit offrir une interface web prennant en charge les fonctionnalités de base de gestion des fichiers.
- Doit permettre d'exporter facilement tous les fichiers/documents.
- Doit utiliser un chiffrement standard et audité.
- Doit être open-source.

### Dans le meilleur des cas

- Devrait disposer d'un audit publié par une tierce partie indépendante et réputée.
