---
meta_title: "Navegador y Red Tor: Navegación Web Anónima - Privacy Guides"
title: "Red Tor"
icon: simple/torproject
description: Protege tu navegación por Internet de miradas intrusas utilizando la red Tor, una red segura que elude la censura.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
    image: /assets/img/browsers/tor.svg
    url: https://www.torproject.org
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

![Logotipo de Tor](assets/img/self-contained-networks/tor.svg){ align=right }

La red **Tor** es un grupo de servidores operados por voluntarios que te permite conectarte gratuitamente y mejorar tu privacidad y seguridad en Internet. Individuos y organizaciones también pueden compartir información a través de la red Tor con los "servicios ocultos .onion" sin comprometer su privacidad. Debido a que el tráfico de Tor es difícil de bloquear y rastrear, Tor es una herramienta eficaz para eludir la censura.

[:octicons-home-16:](https://www.torproject.org){ .card-link title=Página Principal}
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Servicio Onion" }
[:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Documentación}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribuir }

Tor funciona enrutando tu tráfico de Internet a través de esos servidores operados por voluntarios, en lugar de hacer una conexión directa con el sitio que estás tratando de visitar. Esto ofusca de dónde viene el tráfico, y ningún servidor en la ruta de conexión es capaz de ver la ruta completa de dónde viene y a dónde va el tráfico, lo que significa que incluso los servidores a los que te estás conectando no pueden romper tu anonimato.

[Descripción detallada de Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Conectándote a Tor

<div class="admonition tip" markdown>
<p class="admonition-title">Consejo</p>

Antes de conectarte a Tor, por favor, asegúrate de haber leído nuestro [overview](advanced/tor-overview.md) sobre qué es Tor y cómo conectarse a él de forma segura. A menudo recomendamos conectarse a Tor a través de un [proveedor VPN] de confianza(vpn.md), pero tienes que hacerlo **propiamente** para evitar disminuir tu anonimato.

</div>

Hay varias maneras de conectarte a la red Tor desde tu dispositivo, la más utilizada es **Tor Browser**, un fork de Firefox diseñado para la navegación anónima para computadoras y Android.

Algunas de estas aplicaciones son mejores que otras y, una vez más, la decisión depende de tu modelo de amenazas. Si eres un usuario ocasional de Tor que no está preocupado porque tu ISP recopile pruebas contra ti, usar aplicaciones como [Orbot](#orbot) o aplicaciones de navegador móvil para acceder a la red Tor probablemente esté bien. Aumentar el número de personas que usan Tor a diario ayuda a reducir el mal estigma de Tor, y disminuye la calidad de las "listas de usuarios de Tor" que los ISP y los gobiernos pueden compilar.

Si un anonimato más completo es primordial para tu situación, deberías **solo** usar el cliente de escritorio de Tor Browser, idealmente en una configuración [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os). Los navegadores móviles son menos comunes en Tor (y más susceptibles de huellas digitales como resultado), y otras configuraciones no se prueban tan rigurosamente contra la desanonimización.

### Tor Browser

<div class="admonition recommendation" markdown>

![Logo del Navegador Tor](assets/img/browsers/tor.svg){ align=right }

**Tor Browser** es la elección si necesitas anonimato, ya que te proporciona acceso a la red de Tor y puentes, e incluye ajustes por defecto y extensiones que estan configuradas automáticamente a los niveles de seguridad por defecto: *Estándar*, *Más seguro* y *Más seguro de todos*.

[:octicons-home-16: Página Principal](https://www.torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Servicio Onion" }
[:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Documentación }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://www.torproject.org/download/#android)
- [:simple-windows11: Windows](https://www.torproject.org/download/)
- [:simple-apple: macOS](https://www.torproject.org/download/)
- [:simple-linux: Linux](https://www.torproject.org/download/)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Peligro</p>

**Nunca** deberías instalar ninguna extensión adicional en el Navegador Tor, ni siquiera las que sugerimos para Firefox. Las extensiones del navegador y las configuraciones no estándar te hacen destacar de los demás en la red Tor, haciendo así que tu navegador sea más fácil de [fingerprint](https://support.torproject.org/glossary/browser-fingerprinting).

</div>

El navegador Tor está diseñado para evitar la toma de huellas digirtales o tu identificación debido a la configuración de tu navegador. Por lo tanto, es imperativo que **no** modifiques el navegador más allá de los [niveles de seguridad](https://tb-manual.torproject.org/security-settings/) predeterminados.

Además de instalar Tor Browser en tu ordenador directamente, también hay sistemas operativos diseñados específicamente para conectarse a la red Tor como [Whonix](desktop.md#whonix) en [Qubes OS](desktop.md#qubes-os), que proporcionan incluso mayor seguridad y protecciones que el Navegador Tor estándar por sí solo.

### Orbot

<div class="admonition recommendation" markdown>

![Orbot logo](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** es una VPN de Tor gratuita para smartphones que enruta el tráfico desde cualquier aplicación en tu dispositivo a través de la red Tor.

[:octicons-home-16: Página Principal](https://orbot.app/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentación}
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/orbot/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

</details>

</div>

Anteriormente recomendamos activar la preferencia *Aislar direcciones de destino* en los ajustes de Orbot. Aunque esta configuración puede mejorar teóricamente la privacidad forzando el uso de un circuito diferente para cada dirección IP a la que se conecte, no proporciona una ventaja práctica para la mayoría de las aplicaciones (especialmente navegación web), puede conllevar una penalización significativa del rendimiento, y aumenta la carga en la red Tor. Ya no recomendamos ajustar esta configuración desde su valor predeterminado a menos que sepa que lo necesita.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Consejos para Android</p>

Orbot puede hacer de proxy de aplicaciones individuales si soportan SOCKS o proxy HTTP. También puede hacer de proxy de todas tus conexiones de red utilizando [VpnService](https://developer.android.com/reference/android/net/VpnService) y se puede utilizar con el killswitch VPN en :gear: **Ajustes** → **Red e internet** → **VPN** → :gear: → **Bloquear conexiones sin VPN**.

Orbot suele estar desactualizado en el [repositorio F-Droid](https://guardianproject.info/fdroid) de Guardian Project y en [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android), así que considera descargarlo directamente desde el [repositorio GitHub](https://github.com/guardianproject/orbot/releases).

Todas las versiones están firmadas con la misma firma, por lo que deberían ser compatibles entre sí.

</div>

### Onion Browser

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** es un navegador de código abierto que te permite navegar de manera anónima, a través de la red Tor en dispositivos iOS y se encuentra respaldado por el [Proyecto Tor](https://support.torproject.org/glossary/onion-browser/).

[:octicons-home-16: Página Principal](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

## Repetidores y puentes

### Snowflake

<div class="admonition recommendation" markdown>

![Snowflake logo](assets/img/browsers/snowflake.svg#only-light){ align=right }
![Snowflake logo](assets/img/browsers/snowflake-dark.svg#only-dark){ align=right }

**Snowflake** te permite donar ancho de banda al Proyecto Tor operando un "proxy Snowflake" dentro de tu navegador.

Las personas censuradas pueden utilizar proxies Snowflake para conectarse a la red Tor. Snowflake es una gran forma de contribuir a la red incluso si no tienes los conocimientos técnicos para dirigir un repetidor o puente Tor.

[:octicons-home-16: Página Principal](https://snowflake.torproject.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentación}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribuir }

</details>

</div>

Puede activar Snowflake en tu navegador abriéndolo en otra pestaña y activando el interruptor. Puedes dejarlo corriendo en segundo plano mientras navegas para contribuir a tu conexión. No recomendamos instalar Snowflake como extensión del navegador; añadir extensiones de terceros puede aumentar la posibilidad de un ataque.

[Ejecute Snowflake en su navegador :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html ""){.md-button}

Snowflake no aumenta tu privacidad de ninguna manera, ni se utiliza para conectarte a la red Tor dentro de tu navegador personal. Sin embargo, si tu conexión a Internet no está censurada, deberías ejecutarlo para ayudar a las personas en redes censuradas a conseguir mejor privacidad. No hay necesidad de preocuparte por los sitios web a los que la gente accede a través de tu proxy-su dirección IP de navegación visible coincidirá con su nodo de salida Tor, no con el tuyo.

Ejecutar un proxy Snowflake es de bajo riesgo, incluso más que ejecutar un relé Tor o un puente ya que no son esfuerzos particularmente arriesgados. Sin embargo, no deja de ser un proxy de tráfico a través de tu red, lo que puede tener consecuencias en algunos aspectos, especialmente si tu red tiene un ancho de banda limitado. Asegúrate de que entiendes [cómo funciona Snowflake](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) antes de decidir si ejecutas un proxy.

[^1]: El ajuste `IsolateDestAddr` se discute en [Tor mailing lis](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) y [Documentación sobre Stream Isolation de Whonix](https://www.whonix.org/wiki/Stream_Isolation), donde ambos proyectos sugieren que no suele ser un buen enfoque para la mayoría de la gente.
