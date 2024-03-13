---
title: "Front-ends"
icon: material/flip-to-front
description: These open-source frontends for various internet services allow you to access content without JavaScript or other annoyances.
cover: frontends.webp
---

Parfois, des services tentent de vous obliger à créer un compte en bloquant l'accès au contenu par des fenêtres pop-up gênantes. Ils peuvent également ne pas fonctionner sans JavaScript activé. Ces interfaces client peuvent vous permettre de contourner ces restrictions.

Si vous choisissez d'héberger vous-même ces clients, il est important que d'autres personnes utilisent également votre instance pour que vous puissiez vous fondre dans la masse. Vous devriez faire attention à l'endroit et à la manière dont vous hébergez, car l'utilisation par d'autres personnes sera liée à votre hébergement.

Lorsque vous utilisez une instance gérée par quelqu'un d'autre, veillez à lire la politique de confidentialité de cette instance spécifique. Elles peuvent être modifiées par leurs propriétaires et peuvent donc ne pas refléter la politique par défaut. Some instances have [Tor](tor.md) .onion addresses which may grant some privacy as long as your search queries don't contain PII.

## TikTok

### ProxiTok

<div class="admonition recommendation" markdown>

![ProxiTok logo](assets/img/frontends/proxitok.svg){ align=right }

**ProxiTok** is an open-source frontend to the [TikTok](https://tiktok.com) website that is also self-hostable.

There are a number of public instances, with some instances having [Tor](tor.md) onion services support.

[:octicons-repo-16: Dépôt](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Instances Publiques"}
[:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Code Source" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

ProxiTok is useful if you want to disable JavaScript in your browser, such as [Tor Browser](tor.md#tor-browser) on the Safest security level.

</div>

## YouTube

### FreeTube

<div class="admonition recommendation" markdown>

![Logo FreeTube](assets/img/frontends/freetube.svg){ align=right }

**FreeTube** est une application de bureau gratuite et open-source pour [YouTube](https://youtube.com). Lorsque vous utilisez FreeTube, votre liste d'abonnement et vos listes de lecture sont enregistrées localement sur votre appareil.

Par défaut, FreeTube bloque toutes les publicités YouTube. En outre, FreeTube intègre en option [SponsorBlock](https://sponsor.ajay.app) pour vous aider à sauter les segments de vidéos sponsorisées.

[:octicons-home-16: Homepage](https://freetubeapp.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.freetubeapp.io){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://freetubeapp.io/#download)
- [:simple-apple: macOS](https://freetubeapp.io/#download)
- [:simple-linux: Linux](https://freetubeapp.io/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

When using FreeTube, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io) or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

### Yattee

<div class="admonition recommendation" markdown>

![Logo Yattee](assets/img/frontends/yattee.svg){ align=right }

**Yattee** est un lecteur vidéo gratuit et open-source orienté vie privée pour iOS, tvOS et macOS pour [YouTube](https://youtube.com). Lorsque vous utilisez Yattee, votre liste d'abonnement est enregistrée localement sur votre appareil.

You will need to take a few [extra steps](https://gonzoknows.com/posts/Yattee) before you can use Yattee to watch YouTube, due to App Store restrictions.

[:octicons-home-16: Homepage](https://github.com/yattee/yattee){ .md-button .md-button--primary }
[:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-apple: App Store](https://apps.apple.com/app/id1595136629)
- [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

When using Yattee, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

Par défaut, Yattee bloque toutes les publicités YouTube. En outre, Yattee s'intègre en option à [SponsorBlock](https://sponsor.ajay.app) pour vous aider à sauter les segments vidéo sponsorisés.

### LibreTube (Android)

<div class="admonition recommendation" markdown>

![Logo LibreTube](assets/img/frontends/libretube.svg#only-light){ align=right }
![Logo LibreTube](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }

**LibreTube** est une application Android gratuite et open-source pour [YouTube](https://youtube.com) qui utilise l'API [Piped](#piped).

LibreTube vous permet de stocker votre liste d'abonnement et vos listes de lecture localement sur votre appareil Android, ou dans un compte sur l'instance Piped de votre choix, ce qui vous permet d'y accéder de manière transparente sur d'autres appareils également.

[:octicons-home-16: Homepage](https://libre-tube.github.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/libre-tube/LibreTube#privacy-policy-and-disclaimer){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/libre-tube/LibreTube#readme){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

When using LibreTube, your IP address will be visible to the [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) instance you choose and/or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

Par défaut, LibreTube bloque toutes les publicités YouTube. En outre, Libretube utilise [SponsorBlock](https://sponsor.ajay.app) pour vous aider à sauter les segments vidéo sponsorisés. Vous pouvez configurer entièrement les types de segments que SponsorBlock va ignorer, ou le désactiver complètement. Il existe également un bouton sur le lecteur vidéo lui-même pour le désactiver pour une vidéo spécifique si vous le souhaitez.

### NewPipe (Android)

<div class="admonition recommendation annotate" markdown>

![Newpipe logo](assets/img/frontends/newpipe.svg){ align=right }

**NewPipe** is a free and open-source Android application for [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com), and [PeerTube](https://joinpeertube.org) (1).

Votre liste d'abonnement et vos listes de lecture sont enregistrées localement sur votre appareil Android.

[:octicons-home-16: Homepage](https://newpipe.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://teamnewpipe.github.io/documentation){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Source Code" }
[:octicons-heart-16:](https://newpipe.net/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

</details>

</div>

1. The default instance is [FramaTube](https://framatube.org), however more can be added via **Settings** → **Content** → **PeerTube instances**

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Lorsque vous utilisez NewPipe, votre adresse IP sera visible par les fournisseurs vidéo utilisés. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

### Invidious

<div class="admonition recommendation" markdown>

![Invidious logo](assets/img/frontends/invidious.svg#only-light){ align=right }
![Invidious logo](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }

**Invidious** est une interface gratuite et open-source pour [YouTube](https://youtube.com) qui est également auto-hébergable.

There are a number of public instances, with some instances having [Tor](tor.md) onion services support.

[:octicons-home-16: Homepage](https://invidious.io){ .md-button .md-button--primary }
[:octicons-server-16:](https://instances.invidious.io){ .card-link title="Public Instances"}
[:octicons-info-16:](https://docs.invidious.io){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Source Code" }
[:octicons-heart-16:](https://invidious.io/donate){ .card-link title=Contribute }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Invidious n'utilise pas de proxy pour les flux vidéo par défaut. Videos watched through Invidious will still make direct connections to Google's servers (e.g. `googlevideo.com`); however, some instances support video proxying—simply enable *Proxy videos* within the instances' settings or add `&local=true` to the URL.

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Invidious is useful if you want to disable JavaScript in your browser, such as [Tor Browser](tor.md#tor-browser) on the Safest security level. Il n'assure pas à lui seul la protection de la vie privée, et nous ne recommandons pas de se connecter à des comptes.

</div>

### Piped

<div class="admonition recommendation" markdown>

![Logo Piped](assets/img/frontends/piped.svg){ align=right }

**Piped** est une interface gratuite et open-source pour [YouTube](https://youtube.com) qui est également auto-hébergeable.

Piped nécessite JavaScript pour fonctionner et il existe un certain nombre d'instances publiques.

[:octicons-repo-16: Repository](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
[:octicons-server-16:](https://piped.kavin.rocks/preferences#ddlInstanceSelection){ .card-link title="Public Instances"}
[:octicons-info-16:](https://piped-docs.kavin.rocks){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title=Contribute }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Piped est utile si vous souhaitez utiliser [SponsorBlock](https://sponsor.ajay.app) sans installer d'extension ou pour accéder à des contenus limités en âge sans compte. Il n'assure pas à lui seul la protection de la vie privée, et nous ne recommandons pas de se connecter à des comptes.

</div>

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

<div class="admonition example" markdown>
<p class="admonition-title">Cette section est nouvelle</p>

Nous travaillons à l'établissement de critères définis pour chaque section de notre site, et celles-ci peuvent être sujet à changement. Si vous avez des questions sur nos critères, veuillez [poser la question sur notre forum](https://discuss.privacyguides.net/latest) et ne supposez pas que nous n'avons pas pris en compte un élément dans nos recommandations s'il ne figure pas dans la liste. De nombreux facteurs sont pris en compte et discutés lorsque nous recommandons un projet, et la documentation de chacun d'entre eux est en cours.

</div>

Clients recommandés...

- Doit être un logiciel open source.
- Doit être auto-hébergeable.
- Doit fournir toutes les fonctionnalités de base du site web accessibles aux utilisateurs anonymes.

Nous ne prenons en compte que les clients des sites web qui sont...

- Normalement accessible uniquement si JavaScript est activé.
