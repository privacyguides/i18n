---
meta_title: "Navigateur et réseau Tor : navigation web anonyme - Privacy Guides"
title: "Navigateur Tor"
icon: simple/torbrowser
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

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Capitalisme de surveillance](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: Surveillance de masse](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Censure](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

**Tor** est un groupe de serveurs gérés par des bénévoles qui vous permet de vous connecter gratuitement et d'améliorer votre confidentialité et votre sécurité sur Internet. Les particuliers et les organisations peuvent également partager des informations sur le réseau Tor avec des "services cachés .onion" sans compromettre leur vie privée. Parce que le trafic Tor est difficile à bloquer et à tracer, Tor est un outil efficace pour contourner la censure.

[Detailed Tor Overview :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: Video: Why You Need Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor/ ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Avant de vous connecter à Tor, assurez-vous d'avoir lu notre [introduction](advanced/tor-overview.md) sur ce qu'est Tor et comment s'y connecter en toute sécurité. Nous recommandons souvent de se connecter à Tor via un [fournisseur VPN](vpn.md) de confiance, mais vous devez le faire **correctement** pour éviter de diminuer votre anonymat.

</div>

There are a variety of ways to connect to the Tor network from your device, the most commonly used being the **Tor Browser**, a fork of Firefox designed for [:material-incognito: anonymous](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} browsing for desktop computers and Android.

Certaines de ces applications sont meilleures que d'autres et, une fois encore, la décision dépend de votre modèle de menace. If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using mobile browser apps like [Onion Browser](#onion-browser-ios) to access the Tor network is probably fine. L'augmentation du nombre de personnes qui utilisent Tor au quotidien permet de réduire la mauvaise image de Tor et de diminuer la qualité des "listes d'utilisateurs de Tor" que les FAIs et les gouvernements peuvent compiler.

Si un anonymat plus complet est primordial dans votre situation, vous devriez **uniquement** utiliser le client bureau du Navigateur Tor, idéalement dans une configuration [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os). Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

## Navigateur Tor

<div class="admonition recommendation" markdown>

![Logo de Tor Browser](assets/img/browsers/tor.svg){ align=right }

Le **Navigateur Tor** est le choix idéal si vous avez besoin d'anonymat, car il vous donne accès au réseau et aux ponts Tor, et il inclut des paramètres par défaut et des extensions qui sont automatiquement configurées par les niveaux de sécurité par défaut : *Normal*, *Plus sûr* et *Le plus sûr*.

[:octicons-home-16: Page d'accueil](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Service onion" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Code source" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:fontawesome-brands-windows: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Vous ne devriez **jamais** installer des extensions supplémentaires sur le Navigateur Tor, y compris celles que nous suggérons pour Firefox. Les extensions de navigateur et les paramètres non standard vous distinguent des autres sur le réseau Tor, rendant ainsi votre navigateur plus facile à la [capture d'empreintes numérique](https://support.torproject.org/fr/glossary/browser-fingerprinting/).

</div>

Le Navigateur Tor est conçu pour empêcher la capture d'empreintes numérique, ou l'identification en fonction de la configuration de votre navigateur. Il est donc impératif de **ne pas** modifier le navigateur au-delà des [niveaux de sécurité](https://tb-manual.torproject.org/security-settings) par défaut.

Outre installer le Navigateur Tor sur votre ordinateur, il existe également des systèmes d'exploitation conçus spécifiquement pour se connecter au réseau Tor tels que [Whonix](desktop.md#whonix) sur [Qubes OS](desktop.md#qubes-os), qui offrent une sécurité et des protections encore plus importantes que le Navigateur Tor standard.

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![logo Navigateur Onion](assets/img/self-contained-networks/onion_browser.svg){ align=right }

Le **Navigateur Onion** est un navigateur open-source qui vous permet de naviguer anonymement sur le web via le réseau Tor sur les appareils iOS et qui est soutenu par le [Projet Tor](https://support.torproject.org/glossary/onion-browser). [:material-star-box: Read our latest Onion Browser review.](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review/)

[:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser does not provide the same levels of privacy protections as Tor Browser does on desktop platforms. For casual use it is a perfectly fine way to access hidden services, but if you're concerned about being traced or monitored by advanced adversaries you should not rely on this as an anonymity tool.

[Notably](https://github.com/privacyguides/privacyguides.org/issues/2929), Onion Browser does not *guarantee* all requests go through Tor. When using the built-in version of Tor, [your real IP **will** be leaked via WebRTC and audio/video streams](https://onionbrowser.com/faqs) due to limitations of WebKit. It is *safer* to use Onion Browser alongside [Orbot](alternative-networks.md#orbot), but this still comes with some limitations on iOS.
