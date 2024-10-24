---
title: "Front-ends"
icon: material/flip-to-front
description: These open-source frontends for various internet services allow you to access content without JavaScript or other annoyances.
cover: frontends.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Capitalisme de surveillance](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Parfois, des services tentent de vous obliger à créer un compte en bloquant l'accès au contenu par des fenêtres pop-up gênantes. Ils peuvent également ne pas fonctionner sans JavaScript activé. These frontends can allow you to circumvent these restrictions.

Si vous choisissez d'héberger vous-même ces clients, il est important que d'autres personnes utilisent également votre instance pour que vous puissiez vous fondre dans la masse. Vous devriez faire attention à l'endroit et à la manière dont vous hébergez, car l'utilisation par d'autres personnes sera liée à votre hébergement.

When you are using an instance run by someone else, make sure to read the privacy policy of that specific instance (if available). Elles peuvent être modifiées par leurs propriétaires et peuvent donc ne pas refléter la politique par défaut. Some instances have [Tor](tor.md) .onion addresses, which may grant some privacy as long as your search queries don't contain personally identifiable information.

## Reddit

### Redlib

<div class="admonition recommendation" markdown>

![Redlib logo](assets/img/frontends/redlib.svg){ align=right }

**Redlib** is an open-source frontend to the [Reddit](https://reddit.com) website that is also self-hostable. You can access Redlib through a number of public instances.

[:octicons-repo-16: Repository](https://github.com/redlib-org/redlib){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/redlib-org/redlib-instances/blob/main/instances.md){ .card-link title="Public Instances" }
[:octicons-info-16:](https://github.com/redlib-org/redlib?tab=readme-ov-file#table-of-contents){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/redlib-org/redlib){ .card-link title="Source Code" }

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

The [Old Reddit](https://old.reddit.com) website doesn't require as much JavaScript as the new Reddit website does, but it has recently blocked access to IP addresses reserved for public VPNs. You can use Old Reddit in conjunction with the [Tor](tor.md) Onion that was [launched in October 2022](https://forum.torproject.org/t/reddit-onion-service-launch/5305) at [https://old.reddittorjg6rue252oqsxryoxengawnmo46qy4kyii5wtqnwfj4ooad.onion](https://old.reddittorjg6rue252oqsxryoxengawnmo46qy4kyii5wtqnwfj4ooad.onion).

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Redlib is useful if you want to disable JavaScript in your browser, such as [Tor Browser](tor.md#tor-browser) on the Safest security level.

</div>

## TikTok

### ProxiTok

<div class="admonition recommendation" markdown>

![ProxiTok logo](assets/img/frontends/proxitok.svg){ align=right }

**ProxiTok** is an open-source frontend to the [TikTok](https://tiktok.com) website that is also self-hostable.

There are a number of public instances, with some that offer a [Tor](tor.md) onion service or an [I2P](alternative-networks.md#i2p-the-invisible-internet-project) eepsite.

[:octicons-repo-16: Repository](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Public Instances" }
[:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Source Code" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

ProxiTok is useful if you want to disable JavaScript in your browser, such as [Tor Browser](tor.md#tor-browser) on the Safest security level.

</div>

## YouTube

**Note:** YouTube has gradually rolled out changes to its video player and API that have thwarted some of the methods used by third-party frontends for extracting YouTube data. If you experience reliability issues with one YouTube frontend, consider trying out another that uses a different extraction method.

### Invidious

<div class="admonition recommendation" markdown>

![Invidious logo](assets/img/frontends/invidious.svg#only-light){ align=right }
![Invidious logo](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }

**Invidious** est une interface gratuite et open-source pour [YouTube](https://youtube.com) qui est également auto-hébergable.

There are a number of public instances, with some that offer a [Tor](tor.md) onion service or an [I2P](alternative-networks.md#i2p-the-invisible-internet-project) eepsite.

[:octicons-home-16: Homepage](https://invidious.io){ .md-button .md-button--primary }
[:octicons-server-16:](https://instances.invidious.io){ .card-link title="Public Instances" }
[:octicons-info-16:](https://docs.invidious.io){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Source Code" }
[:octicons-heart-16:](https://invidious.io/donate){ .card-link title="Contribute" }

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
[:octicons-server-16:](https://github.com/TeamPiped/Piped/wiki/Instances){ .card-link title="Public Instances" }
[:octicons-info-16:](https://docs.piped.video/docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title="Contribute" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Piped is useful if you want to use [SponsorBlock](https://sponsor.ajay.app) without installing an extension. Il n'assure pas à lui seul la protection de la vie privée, et nous ne recommandons pas de se connecter à des comptes.

</div>

### FreeTube

<div class="admonition recommendation" markdown>

![Logo FreeTube](assets/img/frontends/freetube.svg){ align=right }

**FreeTube** est une application de bureau gratuite et open-source pour [YouTube](https://youtube.com). FreeTube extracts data from YouTube using its built-in API based on [YouTube.js](https://github.com/LuanRT/YouTube.js) or the [Invidious](#invidious) API. You can configure either as the default, with the other serving as a fallback.

Lorsque vous utilisez FreeTube, votre liste d'abonnement et vos listes de lecture sont enregistrées localement sur votre appareil.

[:octicons-home-16: Homepage](https://freetubeapp.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.freetubeapp.io){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

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

![Newpipe logo](assets/img/frontends/newpipe.svg){ align=right }

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
