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

[Resumen Detallado de Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: Video: Por qué necesitas Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Consejo</p>

Antes de conectarte a Tor, por favor, asegúrate de haber leído nuestro [resumen](advanced/tor-overview.md) sobre qué es Tor y cómo conectarse a él de forma segura. A menudo recomendamos conectarse a Tor a través de un [proveedor VPN] de confianza(vpn.md), pero tienes que hacerlo **propiamente** para evitar disminuir tu anonimato.

</div>

Hay varias formas de conectarse a la red Tor desde tu dispositivo, la más utilizada es el **Tor Browser**, un fork de Firefox diseñado para la navegación [:material-incognito: anónima](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} para ordenadores de sobremesa y Android.

Algunas de estas aplicaciones son mejores que otras; la decisión depende de tu modelo de amenazas. Si eres un usuario casual de Tor al que no le preocupa que tu ISP recopile pruebas contra ti, usar aplicaciones de navegador móvil como [Onion Browser](#onion-browser-ios) para acceder a la red Tor probablemente esté bien. Aumentar el número de personas que usan Tor a diario ayuda a reducir el mal estigma de Tor, y disminuye la calidad de las "listas de usuarios de Tor" que los ISP y los gobiernos pueden compilar.

Si un anonimato más completo es primordial para tu situación, deberías **solo** usar el cliente de escritorio de Tor Browser, idealmente en una configuración [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os). Los navegadores móviles son menos comunes en Tor (y más susceptibles a las huellas digitales como resultado), y otras configuraciones no se prueban tan rigurosamente contra la desanonimización.

## Tor Browser

<div class="admonition recommendation" markdown>

![Tor Browser logo](assets/img/browsers/tor.svg){ align=right }

**Tor Browser** es la mejor elección si necesitas anonimato, ya que te proporciona acceso a la red y puentes Tor, e incluye ajustes por defecto y extensiones que se configuran automáticamente por los niveles de seguridad por defecto: *Estándar*, *Más seguro* y *El más seguro de todos*.

[:octicons-home-16: Página Principal](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Servicio Onion" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title="Documentación" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title="Contribuir" }

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

El navegador Tor está diseñado para evitar la toma de huellas digirtales o tu identificación debido a la configuración de tu navegador. Por lo tanto, es imperativo que **no** modifiques el navegador más allá de los [niveles de seguridad](https://tb-manual.torproject.org/security-settings) predeterminados. Cuando modifiques la configuración del nivel de seguridad, **deberás** reiniciar siempre el navegador antes de seguir utilizándolo. De lo contrario, [es posible que la configuración de seguridad no se aplique en su totalidad](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), exponiéndote a un riesgo de fingerprinting y exploits mayor de lo que cabría esperar en función de la configuración elegida.

Además de instalar Tor Browser en tu ordenador directamente, también hay sistemas operativos diseñados específicamente para conectarse a la red Tor como [Whonix](desktop.md#whonix) en [Qubes OS](desktop.md#qubes-os), que proporcionan incluso mayor seguridad y protecciones que el Navegador Tor estándar por sí solo.

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** es un navegador de código abierto que te permite navegar por la web de forma anónima a través de la red Tor en dispositivos iOS y está respaldado por el [Proyecto Tor](https://support.torproject.org/glossary/onion-browser).

[:material-star-box: Lee nuestra última reseña sobre Onion Browser.](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review)

[:octicons-home-16: Página Principal](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title="Contribuir" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser no proporciona los mismos niveles de protección de la privacidad que Tor Browser ofrece en las plataformas de escritorio. Para un uso ocasional es una forma perfectamente adecuada de acceder a servicios ocultos, pero si te preocupa ser rastreado o vigilado por adversarios avanzados no deberías confiar en esto como herramienta de anonimato.

[En particular](https://github.com/privacyguides/privacyguides.org/issues/2929), Onion Browser no *garantiza* que todas las peticiones pasen por Tor. Al usar la versión integrada de Tor, [tu IP real **será filtrada** a través de WebRTC y flujos de audio/vídeo](https://onionbrowser.com/faqs) debido a las limitaciones de WebKit. Es *más seguro* utilizar Onion Browser junto con [Orbot](alternative-networks.md#orbot), pero esto sigue teniendo algunas limitaciones en iOS.
