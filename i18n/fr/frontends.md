---
title: "Front-ends"
icon: material/flip-to-front
description: Ces clients applicatifs open source pour divers services internet vous permettent d'accéder au contenu sans JavaScript ou d'autres inconvénients.
cover: frontends.webp
---

Parfois, des services tentent de vous obliger à créer un compte en bloquant l'accès au contenu par des fenêtres pop-up gênantes. Ils peuvent également ne pas fonctionner sans JavaScript activé. Ces interfaces client peuvent vous permettre de contourner ces restrictions.

Si vous choisissez d'héberger vous-même ces clients, il est important que d'autres personnes utilisent également votre instance pour que vous puissiez vous fondre dans la masse. Vous devriez faire attention à l'endroit et à la manière dont vous hébergez, car l'utilisation par d'autres personnes sera liée à votre hébergement.

Lorsque vous utilisez une instance gérée par quelqu'un d'autre, veillez à lire la politique de confidentialité de cette instance spécifique. Elles peuvent être modifiées par leurs propriétaires et peuvent donc ne pas refléter la politique par défaut. Certaines instances ont des adresses Tor .onion qui peuvent garantir une certaine confidentialité tant que vos requêtes de recherche ne contiennent pas de DCP.

## TikTok

### ProxiTok

!!! recommendation

    ![Logo ProxiTok](assets/img/frontends/proxitok.svg){ align=right }
    
    **ProxiTok** est un client applicatif open source pour le site web [TikTok](https://www.tiktok.com) qui est également auto-hébergeable.
    
    Il existe un certain nombre d'instances publiques, dont certaines bénéficient de la prise en charge des services oignon [Tor](https://www.torproject.org).
    
    [:octicons-repo-16: Dépôt](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
    [:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Instances Publiques"}
    [:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Code Source" }

!!! tip "Conseil"

    ProxiTok est utile si vous souhaitez désactiver JavaScript dans votre navigateur, comme avec le [Navigateur Tor](https://www.torproject.org/) sur le niveau de sécurité Le plus sûr.

## YouTube

### FreeTube

!!! recommendation

    ![Logo FreeTube](assets/img/frontends/freetube.svg){ align=right }
    
    **FreeTube** est une application de bureau gratuite et open-source pour [YouTube](https://youtube.com). Lorsque vous utilisez FreeTube, votre liste d'abonnement et vos listes de lecture sont enregistrées localement sur votre appareil.
    
    Par défaut, FreeTube bloque toutes les publicités YouTube. En outre, FreeTube intègre en option [SponsorBlock](https://sponsor.ajay.app) pour vous aider à sauter les segments de vidéos sponsorisées.
    
    [:octicons-home-16: Page d'accueil](https://freetubeapp.io/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Politique de Confidentialité" }
    [:octicons-info-16:](https://docs.freetubeapp.io){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Code Source" }
    [:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title=Contribuer }
    
    ??? downloads "Téléchargements"
    
        - [:simple-windows11: Windows](https://freetubeapp.io/#download)
        - [:simple-apple: macOS](https://freetubeapp.io/#download)
        - [:simple-linux: Linux](https://freetubeapp.io/#download)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

!!! warning "Avertissement"

    Lorsque vous utilisez FreeTube, votre adresse IP peut encore être connue de YouTube, [Invidious](https://instances.invidious.io) ou [SponsorBlock](https://sponsor.ajay.app/) selon votre configuration. Envisagez d'utiliser un [VPN](vpn.md) ou [Tor](https://www.torproject.org) si votre [modèle de menace](basics/threat-modeling.md) nécessite de masquer votre adresse IP.

### Yattee

!!! recommendation

    ![Logo Yattee](assets/img/frontends/yattee.svg){ align=right }
    
    **Yattee** est un lecteur vidéo gratuit et open-source orienté vie privée pour iOS, tvOS et macOS pour [YouTube](https://youtube.com). Lorsque vous utilisez Yattee, votre liste d'abonnement est enregistrée localement sur votre appareil.
    
    Vous devrez suivre quelques [étapes supplémentaires](https://gonzoknows.com/posts/Yattee/) avant de pouvoir utiliser Yattee pour regarder YouTube, en raison des restrictions de l'App Store.
    
    [:octicons-home-16: Page d'accueil](https://github.com/yattee/yattee){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Politique de Confidentialité" }
    [:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Code Source" }
    [:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title=Contribuer }
    
    ??? downloads "Téléchargements"
    
        - [:simple-apple: App Store](https://apps.apple.com/us/app/yattee/id1595136629)
        - [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

!!! warning "Avertissement"

    Lorsque vous utilisez Yattee, votre adresse IP peut encore être connue de YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) ou [SponsorBlock](https://sponsor.ajay.app/) selon votre configuration. Envisagez d'utiliser un [VPN](vpn.md) ou [Tor](https://www.torproject.org) si votre [modèle de menace](basics/threat-modeling.md) nécessite de masquer votre adresse IP.

Par défaut, Yattee bloque toutes les publicités YouTube. En outre, Yattee s'intègre en option à [SponsorBlock](https://sponsor.ajay.app) pour vous aider à sauter les segments vidéo sponsorisés.

### LibreTube (Android)

!!! recommendation

    ![Logo LibreTube](assets/img/frontends/libretube.svg#only-light){ align=right }
    ![Logo LibreTube](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }
    
    **LibreTube** est une application Android gratuite et open-source pour [YouTube](https://youtube.com) qui utilise l'API [Piped](#piped).
    
    LibreTube vous permet de stocker votre liste d'abonnement et vos listes de lecture localement sur votre appareil Android, ou dans un compte sur l'instance Piped de votre choix, ce qui vous permet d'y accéder de manière transparente sur d'autres appareils également.
    
    [:octicons-home-16: Page d'accueil](https://libre-tube.github.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/libre-tube/LibreTube#privacy-policy-and-disclaimer){ .card-link title="Politique de confidentialité" }
    [:octicons-info-16:](https://github.com/libre-tube/LibreTube#readme){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Source code" }
    
    ??? downloads "Téléchargements"
    
        - [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

!!! warning "Avertissement"

    Lorsque vous utilisez LibreTube, votre adresse IP sera visible par l'instance [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) que vous avez choisie et/ou [SponsorBlock](https://sponsor.ajay.app/) en fonction de votre configuration. Envisagez d'utiliser un [VPN](vpn.md) ou [Tor](https://www.torproject.org) si votre [modèle de menace](basics/threat-modeling.md) nécessite de masquer votre adresse IP.

Par défaut, LibreTube bloque toutes les publicités YouTube. En outre, Libretube utilise [SponsorBlock](https://sponsor.ajay.app) pour vous aider à sauter les segments vidéo sponsorisés. Vous pouvez configurer entièrement les types de segments que SponsorBlock va ignorer, ou le désactiver complètement. Il existe également un bouton sur le lecteur vidéo lui-même pour le désactiver pour une vidéo spécifique si vous le souhaitez.

### NewPipe (Android)

!!! recommendation annotate

    ![Logo Newpipe](assets/img/frontends/newpipe.svg){ align=right }
    
    **NewPipe** est une application Android gratuite et open-source pour [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com), et [PeerTube](https://joinpeertube.org/) (1).
    
    Votre liste d'abonnement et vos listes de lecture sont enregistrées localement sur votre appareil Android.
    
    [:octicons-home-16: Homepage ](https://newpipe.net){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://teamnewpipe.github.io/documentation/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Code source" }
    [:octicons-heart-16:](https://newpipe.net/donate/){ .card-link title=Contribuer }
    
    ??? downloads "Téléchargements"
    
        - [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

1. L'instance par défaut est [FramaTube](https://framatube.org/), mais d'autres peuvent être ajoutées via **Paramètres** → **Contenu** → **Instances PeerTube**

!!! warning "Avertissement"

    Lorsque vous utilisez NewPipe, votre adresse IP sera visible par les fournisseurs vidéo utilisés. Envisagez d'utiliser un [VPN](vpn.md) ou [Tor](https://www.torproject.org) si votre [modèle de menace](basics/threat-modeling.md) nécessite de masquer votre adresse IP.

### Invidious

!!! recommendation

    ![Invidious logo](assets/img/frontends/invidious.svg#only-light){ align=right }
    ![Invidious logo](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }
    
    **Invidious** est une interface gratuite et open-source pour [YouTube](https://youtube.com) qui est également auto-hébergable.
    
    Il existe un certain nombre d'instances publiques, dont certaines bénéficient de la prise en charge des services oignon [Tor](https://www.torproject.org).
    
    [:octicons-home-16: Homepage ](https://invidious.io){ .md-button .md-button--primary }
    [:octicons-server-16:](https://instances.invidious.io){ .card-link title="Instances publiques"}
    [:octicons-info-16:](https://docs.invidious.io/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://invidious.io/donate/){ .card-link title=Contribuer }

!!! warning "Avertissement"

    Invidious n'utilise pas de proxy pour les flux vidéo par défaut. Les vidéos regardées via Invidious seront toujours connectées directement aux serveurs de Google (par exemple, `googlevideo.com`) ; cependant, certaines instances prennent en charge la vidéo par proxy : il suffit d'activer *Proxy videos* dans les paramètres des instances ou d'ajouter `&local=true` à l'URL.

!!! tip "Conseil"

    Invidious est utile si vous souhaitez désactiver JavaScript dans votre navigateur, comme c'est le cas avec [le navigateur Tor](https://www.torproject.org/) au niveau de sécurité le plus sûr. Il n'assure pas à lui seul la protection de la vie privée, et nous ne recommandons pas de se connecter à des comptes.

### Piped

!!! recommendation

    ![Logo Piped](assets/img/frontends/piped.svg){ align=right }
    
    **Piped** est une interface gratuite et open-source pour [YouTube](https://youtube.com) qui est également auto-hébergeable.
    
    Piped nécessite JavaScript pour fonctionner et il existe un certain nombre d'instances publiques.
    
    [:octicons-repo-16: Dépôt](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
    [:octicons-server-16:](https://piped.kavin.rocks/preferences#ddlInstanceSelection){ .card-link title="Instances Publiques"}
    [:octicons-info-16:](https://piped-docs.kavin.rocks/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Code Source" }
    [:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title=Contribuer }

!!! tip "Conseil"

    Piped est utile si vous souhaitez utiliser [SponsorBlock](https://sponsor.ajay.app) sans installer d'extension ou pour accéder à des contenus limités en âge sans compte. Il n'assure pas à lui seul la protection de la vie privée, et nous ne recommandons pas de se connecter à des comptes.

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

!!! example "Cette section est récente"

    Nous travaillons à l'établissement de critères définis pour chaque section de notre site, et celles-ci peuvent être sujet à changement. Si vous avez des questions sur nos critères, veuillez [poser la question sur notre forum](https://discuss.privacyguides.net/latest) et ne supposez pas que nous n'avons pas pris en compte un élément dans nos recommandations s'il ne figure pas dans la liste. De nombreux facteurs sont pris en compte et discutés lorsque nous recommandons un projet, et la documentation de chacun d'entre eux est en cours.

Clients recommandés...

- Doit être un logiciel open source.
- Doit être auto-hébergeable.
- Doit fournir toutes les fonctionnalités de base du site web accessibles aux utilisateurs anonymes.

Nous ne prenons en compte que les clients des sites web qui sont...

- Normalement accessible uniquement si JavaScript est activé.
