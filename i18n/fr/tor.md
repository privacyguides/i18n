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

[Introduction détaillée de Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Avant de vous connecter à Tor, assurez-vous d'avoir lu notre [introduction](advanced/tor-overview.md) sur ce qu'est Tor et comment s'y connecter en toute sécurité. Nous recommandons souvent de se connecter à Tor via un [fournisseur VPN](vpn.md) de confiance, mais vous devez le faire **correctement** pour éviter de diminuer votre anonymat.

</div>

There are a variety of ways to connect to the Tor network from your device, the most commonly used being the **Tor Browser**, a fork of Firefox designed for [:material-incognito: anonymous](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} browsing for desktop computers and Android.

Certaines de ces applications sont meilleures que d'autres et, une fois encore, la décision dépend de votre modèle de menace. Si vous êtes un utilisateur occasionnel de Tor et que vous ne craignez pas que votre FAI collecte des preuves contre vous, l'utilisation d'applications comme [Orbot](#orbot) ou de navigateurs mobiles pour accéder au réseau Tor est probablement suffisante. L'augmentation du nombre de personnes qui utilisent Tor au quotidien permet de réduire la mauvaise image de Tor et de diminuer la qualité des "listes d'utilisateurs de Tor" que les FAIs et les gouvernements peuvent compiler.

Si un anonymat plus complet est primordial dans votre situation, vous devriez **uniquement** utiliser le client bureau du Navigateur Tor, idéalement dans une configuration [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os). Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against de-anonymization.

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

## Orbot

<div class="admonition recommendation" markdown>

![Logo Orbot](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** est un VPN Tor gratuit pour smartphones qui achemine le trafic de n'importe quelle application sur votre appareil à travers le réseau Tor.

[:octicons-home-16: Page d'accueil](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Code source" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

</details>

</div>

Nous avons précédemment recommandé d'activer la préférence *Isolate Destination Address* dans les paramètres d'Orbot. Bien que ce paramètre puisse théoriquement améliorer la confidentialité en imposant l'utilisation d'un circuit différent pour chaque adresse IP à laquelle vous vous connectez, il n'offre pas d'avantage pratique pour la plupart des applications (en particulier la navigation sur le web), peut s'accompagner d'une pénalité de performance significative et augmente la charge sur le réseau Tor. Nous ne recommandons plus d'ajuster ce paramètre par rapport à sa valeur par défaut, sauf si vous savez que vous en avez besoin.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Conseils pour Android</p>

Orbot peut proxy des applications individuelles si elles supportent le proxying SOCKS ou HTTP. Il peut également proxy toutes vos connexions réseau en utilisant [VpnService](https://developer.android.com/reference/android/net/VpnService) et peut être utilisé avec le killswitch VPN dans :gear: **Paramètres** → **Réseau & Internet** → **VPN** → :gear: → **Bloquer les connexions sans VPN**.

Orbot est souvent obsolète sur le [dépôt F-Droid](https://guardianproject.info/fdroid) du Guardian Project et sur le [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android), alors envisagez à la place de télécharger directement depuis le [dépôt GitHub](https://github.com/guardianproject/orbot/releases).

Toutes les versions sont signées en utilisant la même signature, elles devraient donc être compatibles entre elles.

</div>

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![logo Navigateur Onion](assets/img/self-contained-networks/onion_browser.svg){ align=right }

Le **Navigateur Onion** est un navigateur open-source qui vous permet de naviguer anonymement sur le web via le réseau Tor sur les appareils iOS et qui est soutenu par le [Projet Tor](https://support.torproject.org/glossary/onion-browser). [:material-star-box: Read our latest Onion Browser review.](/articles/2024/09/18/onion-browser-review)

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

[^1]: Le paramètre `IsolateDestAddr` est discuté sur la [liste de diffusion Tor](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) et [Whonix's Stream Isolation documentation](https://whonix.org/wiki/Stream_Isolation), où les deux projets suggèrent que ce n'est généralement pas une bonne approche pour la plupart des gens.
