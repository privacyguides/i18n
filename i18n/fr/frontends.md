---
title: "Front-ends"
icon: material/flip-to-front
description: Ces frontends open-source pour différents services internet vous permettent d'accéder au contenu sans JavaScript ou d'autres désagréments.
cover: frontends.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-account-cash: Capitalisme de surveillance](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Parfois, des services tentent de vous obliger à créer un compte en bloquant l'accès au contenu par des fenêtres pop-up gênantes. Ils peuvent également ne pas fonctionner sans JavaScript activé. Ces frontends vous permettent de contourner ces restrictions.

Si vous choisissez d'héberger vous-même ces clients, il est important que d'autres personnes utilisent également votre instance pour que vous puissiez vous fondre dans la masse. Vous devriez faire attention à l'endroit et à la manière dont vous hébergez, car l'utilisation par d'autres personnes sera liée à votre hébergement.

Lorsque vous utilisez une instance gérée par quelqu'un d'autre, veillez à lire la politique de confidentialité de cette instance spécifique (si disponible). Elles peuvent être modifiées par leurs propriétaires et peuvent donc ne pas refléter la politique par défaut. Certaines instances ont des adresses .onion [Tor](tor.md), ce qui peut vous garantir une certaine confidentialité tant que vos requêtes ne contiennent pas d'information personnellement identifiable.

## Reddit

### Redlib

<div class="admonition recommendation" markdown>

![Logo de Redlib](assets/img/frontends/redlib.svg){ align=right }

**Redlib** est une frontend open-source auto-hébergeable du site web [Reddit](https://reddit.com). Vous pouvez accèder à Redlib via un certain nombre d'instances publiques.

[:octicons-repo-16: Dépôt](https://github.com/redlib-org/redlib){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/redlib-org/redlib-instances/blob/main/instances.md){ .card-link title="Instances Publique" }
[:octicons-info-16:](https://github.com/redlib-org/redlib?tab=readme-ov-file#table-of-contents){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/redlib-org/redlib){ .card-link title="Code Source" }

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Le site [Old Reddit](https://old.reddit.com) ne nécessite pas autant de JavaScript que le nouveau site de Reddit, mais a récemment bloqué son accès aux adresses IP réservées aux VPNs publics.  Vous pouvez utiliser Old Reddit en combinaison avec l'Onion [Tor](tor.md) sortit en [octobre 2022](https://forum.torproject.org/t/reddit-onion-service-launch/5305) ici [https://old.reddittorjg6rue252oqsxryoxengawnmo46qy4kyii5wtqnwfj4ooad.onion](https://old.reddittorjg6rue252oqsxryoxengawnmo46qy4kyii5wtqnwfj4ooad.onion).

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Redilb peut être utile si vous souhaitez désactiver JavaScript dans votre navigateur, comme sur le niveau de sécurité le plus élevé du [navigateur Tor](tor.md#tor-browser).

</div>

## TikTok

### ProxiTok

<div class="admonition recommendation" markdown>

![Logo de ProxiTok](assets/img/frontends/proxitok.svg){ align=right }

**ProxiTok**st une frontend open-source auto-hébergeable du site web [TikTok](https://tiktok.com).

Il existe un grand nombre d'instances publiques, dont certaines avec un service onion de [Tor](tor.md) ou un eepsite [I2P](alternative-networks.md#i2p-the-invisible-internet-project).

[:octicons-repo-16: Dépôt](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Instances Publiques" }
[:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Code Source" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

ProxiTok peut être utile si vous souhaitez désactiver JavaScript dans votre navigateur, comme sur le niveau de sécurité le plus élevé du [navigateur Tor](tor.md#tor-browser).

</div>

## YouTube

**Remarque :** YouTube a progressivement apporté des modifications à son lecteur vidéo et à son API, ce qui a permis de contrecarrer certaines méthodes utilisées par les frontends pour extraire des données de YouTube. Si vous rencontrez des problèmes de fiabilité avec une des frontends de YouTube, essayez d'en utiliser une autre qui utilise une méthode d'extraction différente.

### Invidious

<div class="admonition recommendation" markdown>

![Invidious logo](assets/img/frontends/invidious.svg#only-light){ align=right }
![Invidious logo](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }

**Invidious** est une interface gratuite et open-source pour [YouTube](https://youtube.com) qui est également auto-hébergable.

Il existe un grand nombre d'instances publiques, dont certaines avec un service onion de [Tor](tor.md) ou un eepsite [I2P](alternative-networks.md#i2p-the-invisible-internet-project).

[:octicons-home-16: Page d'Accueil](https://invidious.io){ .md-button .md-button--primary }
[:octicons-server-16:](https://docs.invidious.io/instances){ .card-link title="Instances Publiques" }
[:octicons-info-16:](https://docs.invidious.io){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Code Source" }
[:octicons-heart-16:](https://invidious.io/donate){ .card-link title="Contribuer" }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Invidious n'utilise pas de proxy pour les flux vidéo par défaut. Les vidéos regardées via Invidious sont quand même directement connectées aux serveurs de Google (par exemple `googlevideo.com`) ; cependant, certaines instances vous permettent d'utiliser le proxy vidéo - activez simplement *Proxy videos* dans les réglages des instances ou ajoutez `&local=true` dans l'URL.

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Invidious peut être utile si vous souhaitez désactiver JavaScript dans votre navigateur, comme sur le niveau de sécurité le plus élevé du [navigateur Tor](tor.md#tor-browser). Il n'assure pas à lui seul la protection de la vie privée, et nous ne recommandons pas de se connecter à des comptes.

</div>

### Piped

<div class="admonition recommendation" markdown>

![Logo Piped](assets/img/frontends/piped.svg){ align=right }

**Piped** est une interface gratuite et open-source pour [YouTube](https://youtube.com) qui est également auto-hébergeable.

Piped nécessite JavaScript pour fonctionner et il existe un certain nombre d'instances publiques.

[:octicons-repo-16: Dépôt](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/TeamPiped/documentation/blob/main/content/docs/public-instances/index.md){ .card-link title="Instances Publiques" }
[:octicons-info-16:](https://docs.piped.video/docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Code Source" }
[:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title="Contribuer" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Piped peut être utile si vous voulez utiliser [SponsorBlock](https://sponsor.ajay.app) sans installer d'extension. Il n'assure pas à lui seul la protection de la vie privée, et nous ne recommandons pas de se connecter à des comptes.

</div>

### FreeTube

<div class="admonition recommendation" markdown>

![Logo FreeTube](assets/img/frontends/freetube.svg){ align=right }

**FreeTube** est une application de bureau gratuite et open-source pour [YouTube](https://youtube.com). FreeTube extraits les données de YouTube grâce à son API intégré basé sur [YouTube.js](https://github.com/LuanRT/YouTube.js) ou l'API de [Invidious](#invidious). Vous pouvez choisir lequel des deux utiliser par défaut, le deuxième sera utilisé en cas de problème.

Lorsque vous utilisez FreeTube, votre liste d'abonnement, vos playlists et votre historique de recherche et de visionnage sont sauvegardés localement sur votre appareil.

[:octicons-home-16: Page d'Accueil](https://freetubeapp.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://docs.freetubeapp.io){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Code Source" }
[:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:fontawesome-brands-windows: Windows](https://freetubeapp.io/#download)
- [:simple-apple: macOS](https://freetubeapp.io/#download)
- [:simple-linux: Linux](https://freetubeapp.io/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

When using FreeTube, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io), or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

Par défaut, FreeTube bloque toutes les publicités YouTube. In addition, FreeTube optionally integrates with [SponsorBlock](https://sponsor.ajay.app) to help you skip sponsored video segments.

### Yattee

<div class="admonition recommendation" markdown>

![Yattee logo](assets/img/frontends/yattee.svg){ align=right }

**Yattee** is a free and open-source privacy oriented video player for iOS, tvOS, and macOS for [YouTube](https://youtube.com). Due to App Store restrictions, you will need to take a few [extra steps](https://web.archive.org/web/20230330122839/https://gonzoknows.com/posts/Yattee) before you can use Yattee to watch YouTube. Yattee allows you to connect to instances of [Invidious](#invidious) or [Piped](#piped).

When using Yattee, your subscription list is saved locally on your device.

[:octicons-home-16: Homepage](https://github.com/yattee/yattee){ .md-button .md-button--primary }
[:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-apple: App Store](https://apps.apple.com/app/id1595136629)
- [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

When using Yattee, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances), or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

Par défaut, Yattee bloque toutes les publicités YouTube. En outre, Yattee s'intègre en option à [SponsorBlock](https://sponsor.ajay.app) pour vous aider à sauter les segments vidéo sponsorisés.

### LibreTube (Android)

<div class="admonition recommendation" markdown>

![Logo LibreTube](assets/img/frontends/libretube.svg#only-light){ align=right }
![Logo LibreTube](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }

**LibreTube** est une application Android gratuite et open-source pour [YouTube](https://youtube.com) qui utilise l'API [Piped](#piped).

Votre liste d'abonnement et vos listes de lecture sont enregistrées localement sur votre appareil Android.

[:octicons-home-16: Homepage](https://libretube.dev){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/libre-tube/LibreTube/blob/master/PRIVACY_POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://libretube.dev/#faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/libre-tube/LibreTube#donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

When using LibreTube, your IP address will be visible to YouTube, [Piped](https://github.com/TeamPiped/Piped/wiki/Instances), or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

Par défaut, LibreTube bloque toutes les publicités YouTube. Additionally, LibreTube uses [SponsorBlock](https://sponsor.ajay.app) to help you skip sponsored video segments. Vous pouvez configurer entièrement les types de segments que SponsorBlock va ignorer, ou le désactiver complètement. Il existe également un bouton sur le lecteur vidéo lui-même pour le désactiver pour une vidéo spécifique si vous le souhaitez.

### NewPipe (Android)

<div class="admonition recommendation annotate" markdown>

![NewPipe logo](assets/img/frontends/newpipe.svg){ align=right }

**NewPipe** is a free and open-source Android application for [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com), and [PeerTube](https://joinpeertube.org) (1).

Votre liste d'abonnement et vos listes de lecture sont enregistrées localement sur votre appareil Android.

[:octicons-home-16: Homepage](https://newpipe.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://newpipe.net/FAQ){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Source Code" }
[:octicons-heart-16:](https://newpipe.net/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

</details>

</div>

1. The default instance is [FramaTube](https://framatube.org), however more can be added via **Settings** → **Content** → **PeerTube instances**.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Lorsque vous utilisez NewPipe, votre adresse IP sera visible par les fournisseurs vidéo utilisés. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

We only consider frontends if one of the following is true for a platform:

- Normally only accessible with JavaScript enabled.
- Normally only accessible with an account.
- Blocks access from commercial [VPNs](vpn.md).

Clients recommandés...

- Doit être un logiciel open source.
- Doit être auto-hébergeable.
- Doit fournir toutes les fonctionnalités de base du site web accessibles aux utilisateurs anonymes.
