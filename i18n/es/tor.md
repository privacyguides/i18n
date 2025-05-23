---
meta_title: "Navegador y Red Tor: Navegación Web Anónima - Privacy Guides"
title: "Tor Browser"
icon: simple/torbrowser
description: Protege tu navegación por Internet de miradas intrusas utilizando la red Tor, una red segura que elude la censura.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
    sameAs: https://es.wikipedia.org/wiki/Tor_(red_de_anonimato)
    applicationCategory: Navegador Web
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: Vigilancia masiva](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Censura](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

**Tor** es un grupo de servidores operados por voluntarios que te permiten conectarte gratuitamente, además de mejorar tu privacidad y seguridad en Internet. Individuos y organizaciones también pueden compartir información a través de la red Tor con los "servicios ocultos .onion" sin comprometer su privacidad. Debido a que el tráfico de Tor es difícil de bloquear y rastrear, Tor es una herramienta eficaz para eludir la censura.

[Detailed Tor Overview :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: Video: Why You Need Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Consejo</p>

Antes de conectarte a Tor, por favor, asegúrate de haber leído nuestro [resumen](advanced/tor-overview.md) sobre qué es Tor y cómo conectarse a él de forma segura. A menudo recomendamos conectarse a Tor a través de un [proveedor VPN] de confianza(vpn.md), pero tienes que hacerlo **propiamente** para evitar disminuir tu anonimato.

</div>

Hay varias formas de conectarse a la red Tor desde tu dispositivo, la más utilizada es el **Tor Browser**, un fork de Firefox diseñado para la navegación [:material-incognito: anónima](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} para ordenadores de sobremesa y Android.

Some of these apps are better than others; making a determination comes down to your threat model. If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using mobile browser apps like [Onion Browser](#onion-browser-ios) to access the Tor network is probably fine. Aumentar el número de personas que usan Tor a diario ayuda a reducir el mal estigma de Tor, y disminuye la calidad de las "listas de usuarios de Tor" que los ISP y los gobiernos pueden compilar.

Si un anonimato más completo es primordial para tu situación, deberías **solo** usar el cliente de escritorio de Tor Browser, idealmente en una configuración [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os). Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

## Tor Browser

<div class="admonition recommendation" markdown>

![Tor Browser logo](assets/img/browsers/tor.svg){ align=right }

**Tor Browser** is the top choice if you need anonymity, as it provides you with access to the Tor network and bridges, and it includes default settings and extensions that are automatically configured by the default security levels: *Standard*, *Safer* and *Safest*.

[:octicons-home-16: Homepage](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:fontawesome-brands-windows: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Peligro</p>

**Nunca** deberías instalar ninguna extensión adicional en el Navegador Tor, ni siquiera las que sugerimos para Firefox. Las extensiones del navegador y las configuraciones no estándar te hacen destacar de los demás en la red Tor, haciendo así que tu navegador sea más fácil de [fingerprint](https://support.torproject.org/glossary/browser-fingerprinting).

</div>

El navegador Tor está diseñado para evitar la toma de huellas digirtales o tu identificación debido a la configuración de tu navegador. Por lo tanto, es imperativo que **no** modifiques el navegador más allá de los [niveles de seguridad](https://tb-manual.torproject.org/security-settings) predeterminados. When modifying the security level setting, you **must** always restart the browser before continuing to use it. De lo contrario, [es posible que la configuración de seguridad no se aplique en su totalidad](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), exponiéndote a un riesgo de fingerprinting y exploits mayor de lo que cabría esperar en función de la configuración elegida.

Además de instalar Tor Browser en tu ordenador directamente, también hay sistemas operativos diseñados específicamente para conectarse a la red Tor como [Whonix](desktop.md#whonix) en [Qubes OS](desktop.md#qubes-os), que proporcionan incluso mayor seguridad y protecciones que el Navegador Tor estándar por sí solo.

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** es un navegador de código abierto que te permite navegar por la web de forma anónima a través de la red Tor en dispositivos iOS y está respaldado por el [Proyecto Tor](https://support.torproject.org/glossary/onion-browser).

[:material-star-box: Read our latest Onion Browser review.](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review)

[:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser no proporciona los mismos niveles de protección de la privacidad que Tor Browser ofrece en las plataformas de escritorio. Para un uso ocasional es una forma perfectamente adecuada de acceder a servicios ocultos, pero si te preocupa ser rastreado o vigilado por adversarios avanzados no deberías confiar en esto como herramienta de anonimato.

[Notably](https://github.com/privacyguides/privacyguides.org/issues/2929), Onion Browser does not *guarantee* all requests go through Tor. When using the built-in version of Tor, [your real IP **will** be leaked via WebRTC and audio/video streams](https://onionbrowser.com/faqs) due to limitations of WebKit. It is *safer* to use Onion Browser alongside [Orbot](alternative-networks.md#orbot), but this still comes with some limitations on iOS.
