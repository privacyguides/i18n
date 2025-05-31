---
title: Autoalojamiento
meta_title: Software y Servicios Autoalojados - Privacy Guides
description: Para nuestros lectores más técnicos, el software y los servicios autoalojados pueden proporcionar garantías adicionales de privacidad, ya que tienes el máximo control sobre tus datos.
cover: router.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-server-network: Proveedores de Servicios](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

El uso de **software y servicios autoalojados** puede ser una forma de lograr un mayor nivel de privacidad a través de la soberanía digital, en particular la independencia de los servidores en la nube controlados por desarrolladores o vendedores de productos. Por autoalojamiento, nos referimos al alojamiento de aplicaciones y datos en tu propio hardware.

El autoalojamiento de tus propias soluciones requiere conocimientos técnicos avanzados y una profunda comprensión de los riesgos asociados. Al convertirte en anfitrión de ti mismo y, posiblemente, de otros, asumes responsabilidades que de otro modo no tendrías. El autoalojamiento inadecuado de software de privacidad puede dejarte en peor situación que, por ejemplo, el uso de un proveedor de servicios cifrados de extremo a extremo, por lo que es mejor evitarlo si aún no te sientes cómodo haciéndolo.

## :material-email: Servidores de Correo Electrónico

<div class="grid cards" markdown>

- ![Stalwart logo](../assets/img/self-hosting/stalwart.svg){ .twemoji loading=lazy } [Stalwart](email-servers.md#stalwart)
- ![Mailcow logo](../assets/img/self-hosting/mailcow.svg){ .twemoji loading=lazy } [Mailcow](email-servers.md#mailcow)
- ![Mail-in-a-Box logo](../assets/img/self-hosting/mail-in-a-box.svg){ .twemoji loading=lazy } [Mail-in-a-Box](email-servers.md#mail-in-a-box)

</div>

[Más información :material-arrow-right-drop-circle:](email-servers.md)

## :material-account-supervisor-circle-outline: Redes Sociales

El autoalojamiento de tu propia instancia de un software de red social puede ayudarte a eludir la posible [censura a nivel de servidor](../social-networks.md#censorship-resistance) por parte del administrador o el equipo de administración de un servidor público.

### Mastodon

<div class="admonition recommendation" markdown>

![Mastodon logo](../assets/img/social-networks/mastodon.svg){ align=right }

**Mastodon** es una red social basada en protocolos web abiertos y software libre de código abierto. Utiliza el protocolo descentralizado **:simple-activitypub: ActivityPub**.

[:octicons-home-16:](https://joinmastodon.org){ .card-link title="Página Principal" }
[:octicons-info-16:](https://docs.joinmastodon.org/admin/prerequisites){ .card-link title="Documentación de Administración" }

</div>

Mastodon [se integra con la red Tor](https://docs.joinmastodon.org/admin/optional/tor) para escenarios más extremos donde incluso tu proveedor de alojamiento subyacente está sujeto a censura, pero esto podría limitar quién puede acceder a tu contenido a solo otros servidores que se integran con Tor (como la mayoría de los otros servicios ocultos).

Mastodon se beneficia enormemente de una comunidad de autoalojamiento grande y activa, y su administración está ampliamente documentada. Mientras que muchas otras plataformas ActivityPub pueden requerir amplios conocimientos técnicos para ejecutarlas y solucionar problemas, Mastodon tiene versiones muy estables y probadas, y por lo general puede ejecutarse de forma segura sin problemas por cualquier persona que pueda utilizar la línea de comandos de Linux y seguir las instrucciones paso a paso.

### Element

<div class="admonition recommendation" markdown>

![Element logo](../assets/img/social-networks/element.svg){ align=right }

**Element** es el cliente estrella del protocolo **:simple-matrix: Matrix**, un estándar abierto que permite la comunicación descentralizada mediante salas de chat federadas.

[:octicons-home-16:](https://element.io){ .card-link title="Página Principal" }
[:octicons-info-16:](https://element-hq.github.io/synapse/latest){ .card-link title="Documentación de Administración" }
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Código Fuente" }

</div>

## :material-flip-to-front: Interfaces de usuario

El autoalojamiento de tu propia instancia de una interfaz de usuario basada en web puede ayudarte a eludir los límites de tarifa que puedes encontrar en instancias públicas con mucho tráfico. Es importante que otras personas utilicen también tu instancia para que puedas pasar desapercibido. Debes tener cuidado con dónde y cómo alojas, ya que el uso de otras personas estará vinculado a tu alojamiento.

<div class="grid cards" markdown>

- ![Redlib logo](../assets/img/frontends/redlib.svg){ .lg .middle .twemoji } [**Redlib (Reddit)**](../frontends.md#redlib)

    ---

    [:octicons-info-16:](https://github.com/redlib-org/redlib#deployment){ .card-link title="Documentación de Administrador" }
    [:octicons-code-16:](https://github.com/redlib-org/redlib){ .card-link title="Código Fuente" }

- ![ProxiTok logo](../assets/img/frontends/proxitok.svg){ .lg .middle .twemoji } [**ProxiTok (TikTok)**](../frontends.md#proxitok)

    ---

    [:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki/Self-hosting){ .card-link title="Documentación de Administrador" }
    [:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Código Fuente" }

- ![Invidious logo](../assets/img/frontends/invidious.svg#only-light){ .twemoji }![Invidious logo](../assets/img/frontends/invidious-dark.svg#only-dark){ .twemoji } [**Invidious (YouTube)**](../frontends.md#invidious)

    ---

    [:octicons-home-16:](https://invidious.io){ .card-link title="Página Principal" }
    [:octicons-info-16:](https://docs.invidious.io/installation){ .card-link title="Documentación de Administrador" }
    [:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Código Fuente" }

- ![Piped logo](../assets/img/frontends/piped.svg){ .twemoji } [**Piped (YouTube)**](../frontends.md#piped)

    ---

    [:octicons-info-16:](https://docs.piped.video/docs/self-hosting){ .card-link title="Documentación de Administrador" }
    [:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Código Fuente" }

</div>

## Más Herramientas...

Las recomendaciones de herramientas en otras categorías del sitio web también ofrecen una opción de autoalojamiento, por lo que podrías considerarla si confías en tu capacidad para alojar el software después de leer su documentación.

<div class="grid cards" markdown>

- ![Addy.io logo](../assets/img/email-aliasing/addy.svg){ .twemoji } [**Addy.io**](../email-aliasing.md#addyio)

    ---

    [:octicons-home-16:](https://addy.io){ .card-link title="Página Principal" }
    [:octicons-info-16:](https://addy.io/self-hosting){ .card-link title="Documentación de Administrador" }
    [:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Código Fuente" }

- ![SimpleLogin logo](../assets/img/email-aliasing/simplelogin.svg){ .twemoji } [**SimpleLogin**](../email-aliasing.md#simplelogin)

    ---

    [:octicons-home-16:](https://addy.io){ .card-link title="Página Principal" }
    [:octicons-info-16:](https://github.com/simple-login/app#prerequisites){ .card-link title="Documentación de Administrador" }
    [:octicons-code-16:](https://github.com/simple-login){ .card-link title="Código Fuente" }

- ![CryptPad logo](../assets/img/document-collaboration/cryptpad.svg){ .twemoji } [**CryptPad**](../document-collaboration.md#cryptpad)

    ---

    [:octicons-home-16:](https://cryptpad.fr){ .card-link title="Página Principal" }
    [:octicons-info-16:](https://docs.cryptpad.org/en/admin_guide/index.html){ .card-link title="Documentación de Administrador" }
    [:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="Código Fuente" }

- ![Miniflux logo](../assets/img/news-aggregators/miniflux.svg#only-light){ .twemoji }![Miniflux logo](../assets/img/news-aggregators/miniflux-dark.svg#only-dark){ .twemoji } [**Miniflux**](../news-aggregators.md#miniflux)

    ---

    [:octicons-home-16:](https://miniflux.app){ .card-link title="Página Principal" }
    [:octicons-info-16:](https://miniflux.app/docs/index.html#administration-guide){ .card-link title="Documentación de Administrador" }
    [:octicons-code-16:](https://github.com/miniflux/v2){ .card-link title="Código Fuente" }

- ![Standard Notes logo](../assets/img/notebooks/standard-notes.svg){ .twemoji } [**Standard Notes**](../notebooks.md#standard-notes)

    ---

    [:octicons-home-16:](https://standardnotes.com){ .card-link title="Página Principal" }
    [:octicons-info-16:](https://standardnotes.com/help/47/can-i-self-host-standard-notes){ .card-link title="Documentación de Administrador" }
    [:octicons-code-16:](https://github.com/standardnotes){ .card-link title="Código Fuente" }

- ![PrivateBin logo](../assets/img/pastebins/privatebin.svg){ .twemoji } [**PrivateBin**](../pastebins.md#privatebin)

    ---

    [:octicons-home-16:](https://privatebin.info){ .card-link title="Página Principal" }
    [:octicons-info-16:](https://github.com/PrivateBin/PrivateBin/blob/master/doc/Installation.md){ .card-link title="Documentación de Administrador" }
    [:octicons-code-16:](https://github.com/PrivateBin/PrivateBin){ .card-link title="Código Fuente" }

- ![Paaster logo](../assets/img/pastebins/paaster.svg){ .twemoji } [**Paaster**](../pastebins.md#paaster)

    ---

    [:octicons-home-16:](https://paaster.io){ .card-link title="Página Principal" }
    [:octicons-info-16:](https://github.com/WardPearce/paaster#deployment){ .card-link title="Documentación de Administrador" }
    [:octicons-code-16:](https://github.com/WardPearce/paaster){ .card-link title="Código Fuente" }

- ![SimpleX Chat logo](../assets/img/messengers/simplex.svg){ .twemoji } [**SimpleX Chat**](../real-time-communication.md#simplex-chat)

    ---

    [:octicons-home-16:](https://simplex.chat){ .card-link title="Página Principal" }
    [:octicons-info-16:](https://simplex.chat/docs/server.html){ .card-link title="Documentación de Administrador" }
    [:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Código Fuente" }

</div>
