---
meta_title: "Navigateur et réseau Tor : navigation web anonyme - Privacy Guides"
title: "Réseau Tor"
icon: simple/torproject
description: Protégez votre navigation sur internet des regards indiscrets en utilisant le réseau Tor, un réseau sécurisé qui contourne la censure.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Navigateur Tor
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
    sameAs: https://fr.m.wikipedia.org/wiki/Tor_(r%C3%A9seau)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
---

![Logo Tor](assets/img/self-contained-networks/tor.svg){ align=right }

Le réseau **Tor** est un groupe de serveurs gérés par des bénévoles qui vous permet de vous connecter gratuitement et d'améliorer votre confidentialité et votre sécurité sur Internet. Les particuliers et les organisations peuvent également partager des informations sur le réseau Tor avec des "services cachés .onion" sans compromettre leur vie privée. Parce que le trafic Tor est difficile à bloquer et à tracer, Tor est un outil efficace pour contourner la censure.

[:octicons-home-16:](https://torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

Tor fonctionne en acheminant votre trafic Internet via ces serveurs gérés par des volontaires, au lieu d'établir une connexion directe avec le site que vous essayez de visiter. Cela permet de masquer la provenance du trafic, et aucun serveur sur le chemin de la connexion n'est en mesure de voir le chemin complet de la provenance et de la destination du trafic, ce qui signifie que même les serveurs que vous utilisez pour vous connecter ne peuvent pas briser votre anonymat.

[Introduction détaillée de Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Se connecter à Tor

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Avant de vous connecter à Tor, assurez-vous d'avoir lu notre [introduction](advanced/tor-overview.md) sur ce qu'est Tor et comment s'y connecter en toute sécurité. Nous recommandons souvent de se connecter à Tor via un [fournisseur VPN](vpn.md) de confiance, mais vous devez le faire **correctement** pour éviter de diminuer votre anonymat.

</div>

Il existe plusieurs façons de se connecter au réseau Tor à partir de votre appareil, la plus utilisée étant le **Navigateur Tor**, un fork de Firefox conçu pour la navigation anonyme sur les ordinateurs de bureau et Android.

Certaines de ces applications sont meilleures que d'autres et, une fois encore, la décision dépend de votre modèle de menace. Si vous êtes un utilisateur occasionnel de Tor et que vous ne craignez pas que votre FAI collecte des preuves contre vous, l'utilisation d'applications comme [Orbot](#orbot) ou de navigateurs mobiles pour accéder au réseau Tor est probablement suffisante. L'augmentation du nombre de personnes qui utilisent Tor au quotidien permet de réduire la mauvaise image de Tor et de diminuer la qualité des "listes d'utilisateurs de Tor" que les FAIs et les gouvernements peuvent compiler.

Si un anonymat plus complet est primordial dans votre situation, vous devriez **uniquement** utiliser le client bureau du Navigateur Tor, idéalement dans une configuration [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os). Les navigateurs mobiles sont moins courants sur Tor (et donc plus facilement identifiables), et d'autres configurations ne sont pas aussi rigoureusement testées contre la désanonymisation.

### Navigateur Tor

<div class="admonition recommendation" markdown>

![Logo de Tor Browser](assets/img/browsers/tor.svg){ align=right }

Le **Navigateur Tor** est le choix idéal si vous avez besoin d'anonymat, car il vous donne accès au réseau et aux ponts Tor, et il inclut des paramètres par défaut et des extensions qui sont automatiquement configurées par les niveaux de sécurité par défaut : *Normal*, *Plus sûr* et *Le plus sûr*.

[:octicons-home-16: Homepage](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:simple-windows11: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Vous ne devriez **jamais** installer des extensions supplémentaires sur le Navigateur Tor, y compris celles que nous suggérons pour Firefox. Les extensions de navigateur et les paramètres non standard vous distinguent des autres sur le réseau Tor, rendant ainsi votre navigateur plus facile à la [prise d'empreintes numérique](https://support.torproject.org/fr/glossary/browser-fingerprinting/).

</div>

Le Navigateur Tor est conçu pour empêcher la prise d'empreintes numérique, ou l'identification en fonction de la configuration de votre navigateur. Therefore, it is imperative that you do **not** modify the browser beyond the default [security levels](https://tb-manual.torproject.org/security-settings).

Outre installer le Navigateur Tor sur votre ordinateur, il existe également des systèmes d'exploitation conçus spécifiquement pour se connecter au réseau Tor tels que [Whonix](desktop.md#whonix) sur [Qubes OS](desktop.md#qubes-os), qui offrent une sécurité et des protections encore plus importantes que le Navigateur Tor standard.

### Orbot

<div class="admonition recommendation" markdown>

![Logo Orbot](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** est un VPN Tor gratuit pour smartphones qui achemine le trafic de n'importe quelle application sur votre appareil à travers le réseau Tor.

[:octicons-home-16: Homepage](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

</details>

</div>

Nous avons précédemment recommandé d'activer la préférence *Isolate Destination Address* dans les paramètres d'Orbot. Bien que ce paramètre puisse théoriquement améliorer la confidentialité en imposant l'utilisation d'un circuit différent pour chaque adresse IP à laquelle vous vous connectez, il n'offre pas d'avantage pratique pour la plupart des applications (en particulier la navigation sur le web), peut s'accompagner d'une pénalité de performance significative et augmente la charge sur le réseau Tor. Nous ne recommandons plus d'ajuster ce paramètre par rapport à sa valeur par défaut, sauf si vous savez que vous en avez besoin.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Tips for Android</p>

Orbot peut proxy des applications individuelles si elles supportent le proxying SOCKS ou HTTP. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN killswitch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

Orbot est souvent obsolète sur le [dépôt F-Droid](https://guardianproject.info/fdroid) du Guardian Project et sur le [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android), alors envisagez à la place de télécharger directement depuis le [dépôt GitHub](https://github.com/guardianproject/orbot/releases).

Toutes les versions sont signées en utilisant la même signature, elles devraient donc être compatibles entre elles.

</div>

### Navigateur Onion

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** is an open-source browser that lets you browse the web anonymously over the Tor network on iOS devices and is endorsed by the [Tor Project](https://support.torproject.org/glossary/onion-browser).

[:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

## Relais et ponts

### Snowflake

<div class="admonition recommendation" markdown>

![Logo Snowflake](assets/img/browsers/snowflake.svg#only-light){ align=right }
![Logo Snowflake](assets/img/browsers/snowflake-dark.svg#only-dark){ align=right }

**Snowflake** vous permet de donner de la bande passante au Projet Tor en faisant fonctionner un "proxy Snowflake" dans votre navigateur.

Les personnes censurées peuvent utiliser les proxys Snowflake pour se connecter au réseau Tor. Snowflake est un excellent moyen de contribuer au réseau même si vous n'avez pas le savoir-faire technique pour gérer un relais ou un pont Tor.

[:octicons-home-16: Homepage](https://snowflake.torproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

</details>

</div>

Vous pouvez activer Snowflake dans votre navigateur en l'ouvrant dans un autre onglet et en activant l'interrupteur. Vous pouvez le laisser fonctionner en arrière-plan pendant que vous naviguez pour contribuer avec votre connexion. Nous ne recommandons pas d'installer Snowflake en tant qu'extension de navigateur ; l'ajout d'extensions tierces peut augmenter votre surface d'attaque.

[Exécutez Snowflake dans votre navigateur :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html ""){.md-button}

Snowflake n'améliore en rien votre vie privée et n'est pas utilisé pour se connecter au réseau Tor dans votre navigateur personnel. Toutefois, si votre connexion Internet n'est pas censurée, vous devriez envisager de l'utiliser pour aider les personnes se trouvant sur des réseaux censurés à améliorer elles-mêmes leur vie privée. Il n'y a pas besoin de s'inquiéter des sites web auxquels les gens accèdent via votre proxy - leur adresse IP de navigation visible correspondra à leur nœud de sortie Tor, pas à la vôtre.

Faire fonctionner un proxy Snowflake est peu risqué, encore moins que de faire fonctionner un relais ou un pont Tor qui ne sont déjà pas des entreprises particulièrement risquées. Toutefois, il achemine le trafic par le biais de votre réseau, ce qui peut avoir un impact à certains égards, surtout si votre réseau a une bande passante limitée. Assurez-vous de comprendre [le fonctionnement de Snowflake](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) avant de décider de faire tourner un proxy.

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) and [Whonix's Stream Isolation documentation](https://whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
