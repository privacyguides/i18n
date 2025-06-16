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

<small>Protège contre les menaces suivantes :</small>

- [:material-account-cash: Capitalisme de surveillance](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: Surveillance de masse](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Censure](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

**Tor** est un groupe de serveurs gérés par des bénévoles qui vous permet de vous connecter gratuitement et d'améliorer votre confidentialité et votre sécurité sur Internet. Les particuliers et les organisations peuvent également partager des informations sur le réseau Tor avec des "services cachés .onion" sans compromettre leur vie privée. Parce que le trafic Tor est difficile à bloquer et à tracer, Tor est un outil efficace pour contourner la censure.

[Vue détaillée de Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary}[:material-movie-open-play-outline: Vidéo: Pourquoi vous avez besoin de Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Avant de vous connecter à Tor, assurez-vous d'avoir lu notre [introduction](advanced/tor-overview.md) sur ce qu'est Tor et comment s'y connecter en toute sécurité. Nous recommandons souvent de se connecter à Tor via un [fournisseur VPN](vpn.md) de confiance, mais vous devez le faire **correctement** pour éviter de diminuer votre anonymat.

</div>

Il existe plusieurs façons de se connecter au réseau Tor depuis votre appareil, la plus utilisée étant le **navigateur Tor**, un dérivé de Firefox conçu pour [:material-incognito: la navigation anonyme](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} sur les ordinateurs de bureau et Android.

Certaines de ces applications sont meilleures que d'autres ; le choix dépend de votre modèle de menaces. Si vous êtes un utilisateur occasionnel de Tor et que vous ne craignez pas que votre FAI collecte des preuves contre vous, l'utilisation d'applications mobiles comme [Onion Browser](#onion-browser-ios) pour accéder au réseau Tor est probablement suffisante. L'augmentation du nombre de personnes qui utilisent Tor au quotidien permet de réduire la mauvaise image de Tor et de diminuer la qualité des "listes d'utilisateurs de Tor" que les FAIs et les gouvernements peuvent compiler.

Si un anonymat plus complet est primordial dans votre situation, vous devriez **uniquement** utiliser le client bureau du Navigateur Tor, idéalement dans une configuration [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os). Les navigateurs mobiles sont moins courants sur Tor (et donc plus facilement identifiables), et d'autres configurations ne sont pas aussi rigoureusement testées contre la désanonymisation.

## Navigateur Tor

<div class="admonition recommendation" markdown>

![logo du navigateur Tor](assets/img/browsers/tor.svg){ align=right }

[:octicons-home-16: Page d'accueil](https://torproject.org/fr){ .md-button .md-button--primary }[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Service Onion" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Code source" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Play Store](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/fr/download/#android)
- [:fontawesome-brands-windows: Windows](https://torproject.org/fr/download)
- [:simple-apple: macOS](https://torproject.org/fr/download)
- [:simple-linux: Linux](https://torproject.org/fr/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Vous ne devriez **jamais** installer des extensions supplémentaires sur le Navigateur Tor, y compris celles que nous suggérons pour Firefox. Les extensions de navigateur et les paramètres non standard vous distinguent des autres sur le réseau Tor, rendant ainsi votre navigateur plus facile à la [capture d'empreintes numérique](https://support.torproject.org/fr/glossary/browser-fingerprinting/).

</div>

Le Navigateur Tor est conçu pour empêcher la capture d'empreintes numérique, ou l'identification en fonction de la configuration de votre navigateur. Il est donc impératif de **ne pas** modifier le navigateur au-delà des [niveaux de sécurité](https://tb-manual.torproject.org/security-settings) par défaut. Lorsque vous réglez le niveau de sécurité, vous **devez** toujours redémarrez le navigateur avant de continuer à l'utiliser. Dans le cas contraire, [les paramètres de sécurité peuvent ne pas être entièrement appliqués](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), ce qui vous expose à un risque plus élevé de captures d'empreinte et de vulnérabilités que vous ne l'auriez imaginé sur la base des paramètres choisis.

Outre installer le Navigateur Tor sur votre ordinateur, il existe également des systèmes d'exploitation conçus spécifiquement pour se connecter au réseau Tor tels que [Whonix](desktop.md#whonix) sur [Qubes OS](desktop.md#qubes-os), qui offrent une sécurité et des protections encore plus importantes que le Navigateur Tor standard.

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![logo Navigateur Onion](assets/img/self-contained-networks/onion_browser.svg){ align=right }

Le **Navigateur Onion** est un navigateur open-source qui vous permet de naviguer anonymement sur le web via le réseau Tor sur les appareils iOS et qui est soutenu par le [Projet Tor](https://support.torproject.org/glossary/onion-browser).

[:material-star-box: Lisez notre dernière critique de Onion Browser.](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review)

Note : Tous les liens ci-dessous redirigent vers des pages en anglais.
[:octicons-home-16: Page d'accueil](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://onionbrowser.com/faqs){.card-link title="Documentation"}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Code source" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser n'offre pas les mêmes niveaux de protection de la vie privée que Tor Browser sur les ordinateurs de bureau. Pour une utilisation occasionnelle, il s'agit d'un moyen tout à fait correct d'accéder à des services cachés, mais si vous craignez d'être tracé ou surveillé par des adversaires avancés, vous ne devriez pas compter sur cet outil d'anonymat.

[Notamment](https://github.com/privacyguides/privacyguides.org/issues/2929), Onion Browser *ne garantit pas* que toutes les requêtes passent par Tor. Lorsque vous utilisez la version intégrée de Tor, [votre véritable IP **sera** divulguée via WebRTC et les flux audio/vidéo](https://onionbrowser.com/faqs) en raison des limitations de WebKit. Il est *plus sûr d* 'utiliser Onion Browser en même temps qu'[Orbot](alternative-networks.md#orbot), mais cela reste limité sur iOS.
