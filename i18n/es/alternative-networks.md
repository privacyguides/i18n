---
title: Redes alternativas
icon: material/vector-polygon
description: Estas herramientas te permiten acceder a redes distintas a la World Wide Web.
cover: alternative-networks.webp
---

## Redes anonimizadoras

Cuando se trata de redes anonimizadoras, querenos destacar que [Tor](advanced/tor-overview.md) es nuestra primera opción. Es la red anónima más utilizada, fuertemente estudiada y activamente desarrollada. Usar otras redes podría poner en peligro tu anonimato, a menos que sepas lo que estás haciendo.

### Tor

<div class="admonition recommendation" markdown>

![Tor logo](assets/img/self-contained-networks/tor.svg){ align=right }

La red **Tor** es un grupo de servidores operados por voluntarios que te permiten conectarte de manera gratuita, además de mejorar tu privacidad y seguridad en Internet. Individuos y organizaciones también pueden compartir información a través de la red Tor con los "servicios ocultos .onion" sin comprometer su privacidad. Debido a que el tráfico de Tor es difícil de bloquear y rastrear, Tor es una herramienta eficaz para eludir la censura.

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

Running a Snowflake proxy is low-risk, even more so than running a Tor relay or bridge which are already not particularly risky endeavours. However, it does still proxy traffic through your network which can be impactful in some ways, especially if your network is bandwidth-limited. Make sure you understand [how Snowflake works](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) before deciding whether to run a proxy.

### I2P (The Invisible Internet Project)

<div class="admonition recommendation" markdown>

![I2P logo](assets/img/self-contained-networks/i2p.svg#only-light){ align=right }
![I2P logo](assets/img/self-contained-networks/i2p-dark.svg#only-dark){ align=right }

**I2P** is an network layer which encrypts your connections and routes them via a network of computers distributed around the world. It is mainly focused on creating an alternative, privacy-protecting network rather than making regular internet connections anonymous.

[:octicons-home-16: Homepage](https://geti2p.net/en){ .md-button .md-button--primary }
[:octicons-info-16:](https://geti2p.net/en/about/software){ .card-link title=Documentation }
[:octicons-code-16:](https://github.com/i2p/i2p.i2p){ .card-link title="Source Code" }
[:octicons-heart-16:](https://geti2p.net/en/get-involved){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.i2p.android)
- [:simple-android: Android](https://geti2p.net/en/download#android)
- [:simple-windows11: Windows](https://geti2p.net/en/download#windows)
- [:simple-apple: macOS](https://geti2p.net/en/download#mac)
- [:simple-linux: Linux](https://geti2p.net/en/download#unix)

</details>

</div>

Unlike Tor, all I2P traffic is internal to the I2P network, which means regular internet websites are **not** directly accessible from I2P. Instead, you can connect to websites which are hosted anonymously and directly on the I2P network, which are called "eepsites" and have domains which end in `.i2p`.

<div class="admonition example" markdown>
<p class="admonition-title">¡Pruébalo!</p>

You can try connecting to _Privacy Guides_ via I2P at [privacyguides.i2p](http://privacyguides.i2p/?i2paddresshelper=fvbkmooriuqgssrjvbxu7nrwms5zyhf34r3uuppoakwwsm7ysv6q.b32.i2p).

</div>

Also, unlike Tor, every I2P node will relay traffic for other users by default, instead of relying on dedicated relay volunteers to run nodes. There are approximately [10,000](https://metrics.torproject.org/networksize.html) relays and bridges on the Tor network compared to ~50,000 on I2P, meaning there is potentially more ways for your traffic to be routed to maximize anonymity. I2P also tends to be more performant than Tor, although this is likely a side-effect of Tor being more focused on regular "clearnet" internet traffic and thus using more bottlenecked exit nodes. Hidden service performance is generally considered to be much better on I2P compared to Tor. While running P2P applications like BitTorrent is challenging on Tor (and can massively impact Tor network performance), it is very easy and performant on I2P.

There are downsides to I2P's approach, however. Tor relying on dedicated exit nodes means more people in less safe environments can use it, and the relays that do exist on Tor are likely to be more performant and stable, as they generally aren't run on residential connections. Tor is also far more focused on **browser privacy** (i.e. anti-fingerprinting), with a dedicated [Tor Browser](tor.md) to make browsing activity as anonymous as possible. I2P is used via your [regular web browser](desktop-browsers.md), and while you can configure your browser to be more privacy-protecting, you probably still won't have the same browser fingerprint as other I2P users (there's no "crowd" to blend in with in that regard).

Tor is likely to be more resistant to censorship, due to their robust network of bridges and varying [pluggable transports](https://tb-manual.torproject.org/circumvention). On the other hand, I2P uses directory servers for the initial connection which are varying/untrusted and run by volunteers, compared to the hard-coded/trusted ones Tor uses which are likely easier to block.
