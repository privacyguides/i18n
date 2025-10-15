---
title: Gestion des photos
icon: material/image
description: Ces outils de gestion de photos vous permettent de protéger vos photos des regards indiscrets des fournisseurs de cloud et autres intermédiaires non-autorisés.
cover: photo-management.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-bug-outline: Attaque Passive](basics/common-threats.md#security-and-privacy){ .pg-orange }
- [:material-server-network: Fournisseurs de Services](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

La majorité des **gestionnaires de photos** comme Google Photo, Flickr et Amazon Photo ne protègent pas vos photos contre le fait d'être accessible au fournisseur de cloud lui-même. Les options proposées ci-dessous préservent la confidentialité de vos photos personnelles, tout en vous permettant de ne les partager qu'avec votre famille et des personnes de confiance.

## Ente Photos

<div class="admonition recommendation" markdown>

![Logo de Ente](assets/img/photo-management/ente.svg){ align=right }

**Ent Photos** est un service de sauvegarde de photo chiffré de bout-en-bout qui vous permet de sauvegarder automatiquement vos photos sur iOS et Android. Le code est entièrement open-source, côté client et côté serveur. Il est également possible de [l'auto-héberger](https://github.com/ente-io/ente/tree/main/server#self-hosting).

Le plan gratuit offre 10 Go de stockage à condition que vous utilisiez le service au moins une fois par an.

[:octicons-home-16: Page d'Accueil](https://ente.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Politque de Confidentialité" }
[:octicons-info-16:](https://ente.io/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ente-io/ente){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

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

## Critères

**Nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de nos [critères de base](about/criteria.md), nous avons élaboré un ensemble d'exigences clair nous permettant de proposer des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de faire votre choix, et de mener vos propres recherches pour vous assurer que celui-ci corresponde bien à vos besoins.

### Exigences minimales

- Les services basés sur un cloud doivent être chiffrés de bout-en-bout.
- Doit avoir une offre gratuite ou une période d'essai.
- Doit être compatible avec l'authentification multifactorielle TOTP ou FIDO2, ou la connexion par passkey.
- Doit avoir une interface web prenant en charge les fonctionnalités de base de gestion des fichiers.
- Doit permettre d'exporter facilement tous les fichiers/documents.
- Doit être open-source.

### Critères optimaux

- Devrait avoir publié un rapport d'audit provenant d'un organisme indépendant réputé.
