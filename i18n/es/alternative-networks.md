---
title: Redes alternativas
icon: material/vector-polygon
description: Estas herramientas te permiten acceder a redes distintas a la World Wide Web.
cover: alternative-networks.webp
---

<small>Protects against the following threat(s):</small>

- [:material-server-network: Service Providers](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-eye-outline: Mass Surveillance](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }
- [:material-account-cash: Surveillance Capitalism](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

## Redes anonimizadoras

Cuando se trata de redes anonimizadoras, querenos destacar que [Tor](advanced/tor-overview.md) es nuestra primera opción. Es la red anónima más utilizada, fuertemente estudiada y activamente desarrollada. Using other networks could be more likely to endanger your [:material-incognito: Anonymity](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }, unless you know what you're doing.

### Tor

<div class="admonition recommendation" markdown>

![Tor logo](assets/img/self-contained-networks/tor.svg){ align=right }

La red **Tor** es un grupo de servidores operados por voluntarios que te permiten conectarte de manera gratuita, además de mejorar tu privacidad y seguridad en Internet. Individuos y organizaciones también pueden compartir información a través de la red Tor con los "servicios ocultos .onion" sin comprometer su privacidad. Because Tor traffic is difficult to block and trace, Tor is an effective [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray } circumvention tool.

[:octicons-home-16:](https://torproject.org){ .card-link title=Página principal }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Servicio Onion" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentación}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Código fuente" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribuir }

</div>

La manera recomendada de acceder a la red Tor es por medio del Navegador Tor, que explicamos más a detalle en una página dedicada:

[Información del Navegador Tor :material-arrow-right-drop-circle:](tor.md){ .md-button .md-button--primary } [Revisión detallada de Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md){ .md-button }

<div class="admonition example" markdown>
<p class="admonition-title">¡Pruébalo!</p>

Puedes acceder a _Privacy Guides_ a través de tor en [xoe4vn5uwdztif6goazfbmogh6wh5jc4up35bqdflu6bkdc5cas5vjqd.onion](http://www.xoe4vn5uwdztif6goazfbmogh6wh5jc4up35bqdflu6bkdc5cas5vjqd.onion).

</div>

#### Snowflake

<div class="admonition recommendation" markdown>

![Snowflake logo](assets/img/browsers/snowflake.svg#only-light){ align=right }
![Snowflake logo](assets/img/browsers/snowflake-dark.svg#only-dark){ align=right }

**Snowflake** te permite donar ancho de banda al Proyecto Tor, operando un "proxy de Snowflake" desde tu navegador.

Las personas censuradas pueden usar los proxies de Snowflake para conectarse a la red Tor. Snowflake es una gran manera de contribuir a la red, incluso si no tienes los conocimientos técnicos para operar un nodo o puente de Tor.

[:octicons-home-16: Página principal](https://snowflake.torproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentación}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="Código fuente" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribuir }

</details>

</div>

Puedes activar Snowflake en tu navegador al abrirlo en otra pestaña y activar el interruptor. Puedes dejarlo corriendo de fonto mientras navegas para contribuir con tu conexión. No recomendamos instalar Snowflake como una extensión del navegador, porque agregar extensiones de terceros puede aumentar tu superficie de ataque.

[Ejecuta Snowflake en tu navegador :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html){ .md-button }

Snowflake no aumenta tu privacidad de ninguna manera, ni se utiliza para conectar con la red Tor desde tu navegador personal. Sin embargo, si tu conexión a Internet no está censurada, deberías considerar ejecutarlo para ayudar a mejorar la privacidad de las personas en redes censuradas. No es necesasrio preocuparte sobre cuales páginas acceden las personas a través de tu proxy—su dirección IP visible coincidirá con su nodo de salida de Tor, no el tuyo.

Running a Snowflake proxy is low-risk, even more so than running a Tor relay or bridge which are already not particularly risky endeavours. Sin embargo, el tráfico de proxy pasa a través de tu red, lo que puede impactar de varias maneras, especialmente si el tráfico de tu red es limitado. Asegúrate de comprender [cómo funciona Snowflake](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) antes de tomar la decisión de ejecutar un proxy.

### I2P (El Proyecto de Internet Invisible)

<div class="admonition recommendation" markdown>

![logo de I2P](assets/img/self-contained-networks/i2p.svg#only-light){ align=right }
![logo de I2P](assets/img/self-contained-networks/i2p-dark.svg#only-dark){ align=right }

**I2P** es una capa de red que cifra tus conexiones y las enruta a través de una red de computadoras distribuidas alrededor del mundo. Está enfocada principalmente en crear una red alternativa que protege la privacidad, en vez de anonimizar las conexiones regulares a Internet.

[:octicons-home-16: Página principal](https://geti2p.net/en){ .md-button .md-button--primary }
[:octicons-info-16:](https://geti2p.net/en/about/software){ .card-link title=Documentación }
[:octicons-code-16:](https://github.com/i2p/i2p.i2p){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://geti2p.net/en/get-involved){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.i2p.android)
- [:simple-android: Android](https://geti2p.net/en/download#android)
- [:fontawesome-brands-windows: Windows](https://geti2p.net/en/download#windows)
- [:simple-apple: macOS](https://geti2p.net/en/download#mac)
- [:simple-linux: Linux](https://geti2p.net/en/download#unix)

</details>

</div>

A diferencia de Tor, todo el tráfico de I2P es interno a la red I2P, lo que significa que los sitios web regulares de Internet **no** se pueden acceder directamente desde I2P. En su lugar, puedes conectarte a sitios web que son alojador de manera anónima y directamente en la red I2P, que son llamados "eepsites" y tienen dominios terminados en `.i2p`.

<div class="admonition example" markdown>
<p class="admonition-title">¡Pruébalo!</p>

Puedes tratar de conectarte a _Privacy Guides_ a través de I2P en [privacyguides.i2p](http://privacyguides.i2p/?i2paddresshelper=fvbkmooriuqgssrjvbxu7nrwms5zyhf34r3uuppoakwwsm7ysv6q.b32.i2p).

</div>

Además, a diferencia de Tor, cada nodo de I2P retransmite el tráfico para otros usuarios por defecto, en vez de depender de voluntarios dedicados a la retransmisión para ejecutar los nodos. Hay aproximadamente [10,000](https://metrics.torproject.org/networksize.html) repetidores y puentes en la red Tor, comparador a los ~50,000 en I2P, significando que hay potenciamente más formas de enrutar tu tráfico para maximizar el anonimato. I2P también tiende a ser más eficiente que Tor, pero esto puede deberse a que Tor está más enfocado en el tráfico regular de Internet "limpio", por lo que usa más nodos de salida con cuellos de botella. El rendimiento del servicio oculto es, por lo general, considerado mucho mejor en I2P a comparación de Tor. Mientras la ejecución de aplicaciones como BitTorrent es complicado en Tor (y puede impactar masivamente el rendimiento de la red Tor), es muy fácil y eficiente en I2P.

Sin embargo, I2P presenta sus desventajas. La dependencia de Tor en nodos de salida dedicados significa que más personas en entornos menos seguros pueden usarlo, y los repetidores que existen en Tor son probablemente más eficientes y estables, porque generalmente no son ejecutados en conexiones residenciales. Tor también está más enfocado en la **privacidad del navegador** (ej: protección ante las huellas dactilares), con un [Navegador Tor](tor.md) dedicado para anonimizar la actividad de navegación lo máximo posible. I2P es usado a través de tu [navegador regular de Internet](desktop-browsers.md) y mientras puedes configurar tu navegador para que proteja mejor tu privacidad, probablemente tu navegador no tiene la misma huella dactilar que otros usuarios de I2P (no hay una "multitud" para camuflarte).

Es probable que Tor sea más resistente a la censura, debido a su robusta red de puentes y diversos [transportes conectables](https://tb-manual.torproject.org/circumvention). Por otro lado, I2P usa servidores de directorio para la conexión inicial, que pueden ser variables/no fiables y ejecutados por voluntarios, a comparación de los codificados/fiables que Tor usa y probablemente son más fáciles de bloquear.
