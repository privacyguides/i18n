---
title: Partage et synchronisation de fichiers
icon: material/share-variant
description: Découvrez comment partager vos fichiers en toute confidentialité entre vos appareils, avec vos amis et votre famille, ou de manière anonyme en ligne.
cover: file-sharing.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-server-network: Fournisseurs de service](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Découvrez comment partager vos fichiers en toute confidentialité entre vos appareils, avec vos amis et votre famille, ou de manière anonyme en ligne.

## Partage de fichiers

Si vous utilisez déjà [Proton Drive](cloud.md#proton-drive)[^1] ou que vous disposez d'un abonnement à [Bitwarden](passwords.md#bitwarden) Premium[^2], envisagez d'utiliser les fonctionnalités de partage de fichiers qu'ils offrent, tous deux utilisant le cryptage de bout en bout. Sinon, les options autonomes listées ici s'assurent que les fichiers que vous partagez ne sont pas lus par un serveur distant.

### Send

<div class="admonition recommendation" markdown>

![Logo de Send](assets/img/file-sharing-sync/send.svg){ align=right }

**Send** est un fork du service Firefox Send de Mozilla, qui a été abandonné, et qui vous permet d'envoyer des fichiers à d'autres personnes à l'aide d'un lien. Les fichiers sont chiffrés sur votre appareil afin qu'ils ne puissent pas être lus par le serveur, et ils peuvent également être protégés par un mot de passe. Le mainteneur de Send héberge une [instance publique](https://send.vis.ee). Vous pouvez utiliser d'autres instances publiques, ou vous pouvez héberger Send vous-même.

[:octicons-home-16: Page d'Accueil](https://send.vis.ee){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="Instances Publiques"}
[:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="Code Source" }
[:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title="Contribuer" }

</details>

</div>

Send peut être utilisé via son interface web ou via le CLI [ffsend](https://github.com/timvisee/ffsend) . Si vous êtes familier avec la ligne de commande et que vous envoyez fréquemment des fichiers, nous vous recommandons d'utiliser le client CLI pour éviter le chiffrement basé sur JavaScript. Vous pouvez spécifier le flag `--host` pour utiliser un serveur spécifique :

```bash
ffsend upload --host https://send.vis.ee/ FICHIER
```

### OnionShare

<div class="admonition recommendation" markdown>

![Logo OnionShare](assets/img/file-sharing-sync/onionshare.svg){ align=right }

**OnionShare** est un outil open-source qui vous permet de partager en toute sécurité et [:material-incognito: anonymement](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } un fichier de n'importe quelle taille. Il fonctionne en démarrant un serveur web accessible en tant que service oignon Tor, avec une URL non devinable que vous pouvez partager avec les destinataires pour télécharger ou envoyer des fichiers.

[:octicons-home-16: Page d'Accueil](https://onionshare.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="Service Onion" }
[:octicons-info-16:](https://docs.onionshare.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:fontawesome-brands-windows: Windows](https://onionshare.org/#download)
- [:simple-apple: macOS](https://onionshare.org/#download)
- [:simple-linux: Linux](https://onionshare.org/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/org.onionshare.OnionShare)

</details>

</div>

OnionShare offre la possibilité de se connecter via des [ponts Tor](https://docs.onionshare.org/2.6.2/en/tor.html#automatic-censorship-circumvention) pour contourner la [:material-close-outline: Censure](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}.

### Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

- Ne doit pas stocker des données déchiffrées sur un serveur distant.
- Dois être un logiciel open source.
- Doit avoir soit des clients pour Linux, macOS et Windows, soit une interface web.

## Synchronisation de fichiers

### Syncthing (P2P)

<div class="admonition recommendation" markdown>

![Logo de Syncthing](assets/img/file-sharing-sync/syncthing.svg){ align=right }

**Syncthing** est un utilitaire open-source de synchronisation continue de fichiers de pair à pair. Il est utilisé pour synchroniser des fichiers entre deux ou plusieurs appareils via le réseau local ou internet. Syncthing n'utilise pas de serveur centralisé ; il utilise le [Protocole d'Échange de Blocs](https://docs.syncthing.net/specs/bep-v1.html#bep-v1) pour transférer les données entre appareils. Toutes les données sont chiffrées à l'aide de TLS.

[:octicons-home-16: Page d'accueil](https://syncthing.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.syncthing.net){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/syncthing){ .card-link title="Code source" }
[:octicons-heart-16:](https://syncthing.net/donations){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:fontawesome-brands-windows: Windows](https://syncthing.net/downloads)
- [:simple-apple: macOS](https://syncthing.net/downloads)
- [:simple-linux: Linux](https://syncthing.net/downloads)
- [:simple-freebsd: FreeBSD](https://syncthing.net/downloads)

</details>

</div>

### Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

#### Exigences minimales

- Ne doit pas nécessiter un serveur distant/cloud tiers.
- Dois être un logiciel open source.
- Doit avoir soit des clients pour Linux, macOS et Windows, soit une interface web.

#### Critères optimaux

Nos critères optimaux représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de ces fonctionnalités, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Devrait avoir des clients mobiles pour iOS et Android qui prennent au moins en charge la prévisualisation de documents.
- Devrait prendre en charge les sauvegardes de photos depuis iOS et Android, et éventuellement la synchronisation fichiers/dossiers sur Android.

[^1]: ProtonDrive permet de [partager des fichiers ou des dossiers](https://proton.me/support/drive-shareable-link) en générant un lien de partage public ou en envoyant un lien unique à une adresse mail spécifique. Les liens publics peuvent être protégés par un mot de passe, avoir une date limite, et être complètement révoqués, tandis que les liens partagés par mail permettent de personnaliser les permissions, en plus d'être révocables de la même manière. Selon la [politique de confidentialité](https://proton.me/drive/privacy-policy) de Proton Drive, le contenu des fichiers, les noms des dossiers et des fichiers et les aperçus sont chiffrés de bout-en-bout.
[^2]: Avec un abonnement [premium](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans), [Bitwarden Send](https://bitwarden.com/products/send) permet de partager des fichiers et du texte de façon sécurisée avec un [chiffrement de bout-en-bout](https://bitwarden.com/help/send-encryption). Le lien d'envoi peut également être protégé par un [mot de passe](https://bitwarden.com/help/send-privacy/#send-passwords). Bitwarden Send permet également de configurer une [suppression automatique](https://bitwarden.com/help/send-lifespan).
