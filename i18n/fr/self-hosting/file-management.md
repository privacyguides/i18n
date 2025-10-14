---
title: Gestion des fichiers
meta_title: "Outils autohébergés de gestion de fichiers -Privacy Guide"
icon: material/file-multiple-outline
description: Pour nos lecteurs les plus avancés, autohéberger ses outils de gestion de fichier peut permettre d'atteindre un niveau de confidentialité plus élevé en permettant d'avoir un contrôle maximal sur vos données.
cover: cloud.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-server-network: Fournisseurs de services](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

L'auto-hébergement d'outils de **gestion de fichiers** peut permettre de réduire les risques liés aux défauts de chiffrement dans les clients natifs d'un fournisseur de cloud.

## Gestion des photos

### PhotoPrism

<div class="admonition recommendation" markdown>

![Logo de PhotoPrism](../assets/img/self-hosting/photoprism.svg){ align=right }

**PhotoPrism** est une plateforme pour gérer vos photos. Elle prend en charge la synchronisation et le partage d'albums ainsi qu'une variété d'autres [fonctionnalités](https://photoprism.app/features). Le chiffrement de bout-en-bout n'est pas inclus, il est donc préférable de l'héberger sur un serveur de confiance que vous contrôlez vous-même.

[:octicons-home-16: Page d'Accueil](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Code Source" }

</div>

## Partage et synchronisation de fichiers

### FreedomBox

<div class="admonition recommendation" markdown>

![Logo de FreedomBox](../assets/img/self-hosting/freedombox.svg){ align=right }

**FreedomBox** est un système d'exploitation conçu pour fonctionner sur un [ordinateur à carte unique (Single Board Computer ou SBC en anglais)](https://en.wikipedia.org/wiki/Single-board_computer). Son objectif est de simplifier l'installation d'applications serveurs pour des utilisations telles que le partage de documents.

[:octicons-home-16: Page d'Accueil](https://freedombox.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title="Documentation" }
[:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="Code Source" }
[:octicons-heart-16:](https://freedomboxfoundation.org/donate){ .card-link title="Contribuer" }

</div>

### Nextcloud

<div class="admonition recommendation" markdown>

![Logo de Nextcloud](../assets/img/self-hosting/nextcloud.svg){ align=right }

**Nextcloud** est une suite de logiciels client-serveur gratuits et open-source permettant de créer votre propre service d'hébergement de fichiers sur un serveur que vous contrôlez.

[:octicons-home-16: Page d'Accueil](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Code Source" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title="Contribuer" }

<details class="downloads" markdown><summary>Téléchargements</summary>

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

Nous ne recommandons pas l'utilisation de [l'application E2EE](https://apps.nextcloud.com/apps/end_to_end_encryption) pour Nextcloud car elle peut entraîner une perte de données ; elle est hautement expérimentale et n'est pas de qualité de production. C'est pour cela que nous ne recommandons pas d'utiliser les fournisseurs intermédiaires de Nextcloud.

</div>
