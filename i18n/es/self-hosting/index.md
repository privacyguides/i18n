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

## :material-account-supervisor-circle-outline: Social Networks

Self-hosting your own instance of a social network software can help circumvent potential [censorship on a server level](../social-networks.md#censorship-resistance) by a public server's administrator or admin team.

### Mastodon

<div class="admonition recommendation" markdown>

![Mastodon logo](../assets/img/social-networks/mastodon.svg){ align=right }

**Mastodon** is a social network based on open web protocols and free, open-source software. It uses the decentralized **:simple-activitypub: ActivityPub** protocol.

[:octicons-home-16:](https://joinmastodon.org){ .card-link title="Homepage" }
[:octicons-info-16:](https://docs.joinmastodon.org/admin/prerequisites){ .card-link title="Admin Documentation" }

</div>

Mastodon [integrates with the Tor network](https://docs.joinmastodon.org/admin/optional/tor) for more extreme scenarios where even your underlying hosting provider is subject to censorship, but this may limit who can access your content to only other servers which integrate with Tor (like most other hidden services).

Mastodon benefits greatly from a large and active self-hosting community, and its administration is comprehensively documented. While many other ActivityPub platforms can require extensive technical knowledge to run and troubleshoot, Mastodon has very stable and tested releases, and it can generally be run securely without issue by anyone who can use the Linux command line and follow step-by-step instructions.

### Element

<div class="admonition recommendation" markdown>

![Element logo](../assets/img/social-networks/element.svg){ align=right }

**Element** is the flagship client for the **:simple-matrix: Matrix** protocol, an open standard that enables decentralized communication by way of federated chat rooms.

[:octicons-home-16:](https://element.io){ .card-link title="Homepage" }
[:octicons-info-16:](https://element-hq.github.io/synapse/latest){ .card-link title="Admin Documentation" }
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Source Code" }

</div>

## :material-flip-to-front: Frontends

Self-hosting your own instance of a web-based frontend can help you circumvent rate limits that you may encounter on high-traffic, public instances. It is important that you have other people using your instance as well in order for you to blend in. Debes tener cuidado con dónde y cómo alojas, ya que el uso de otras personas estará vinculado a tu alojamiento.

<div class="grid cards" markdown>

- ![Redlib logo](../assets/img/frontends/redlib.svg){ .lg .middle .twemoji } [**Redlib (Reddit)**](../frontends.md#redlib)

    ---

    [:octicons-info-16:](https://github.com/redlib-org/redlib#deployment){ .card-link title="Admin Documentation" }
    [:octicons-code-16:](https://github.com/redlib-org/redlib){ .card-link title="Source Code" }

- ![ProxiTok logo](../assets/img/frontends/proxitok.svg){ .lg .middle .twemoji } [**ProxiTok (TikTok)**](../frontends.md#proxitok)

    ---

    [:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki/Self-hosting){ .card-link title="Admin Documentation" }
    [:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Source Code" }

- ![Invidious logo](../assets/img/frontends/invidious.svg#only-light){ .twemoji }![Invidious logo](../assets/img/frontends/invidious-dark.svg#only-dark){ .twemoji } [**Invidious (YouTube)**](../frontends.md#invidious)

    ---

    [:octicons-home-16:](https://invidious.io){ .card-link title="Homepage" }
    [:octicons-info-16:](https://docs.invidious.io/installation){ .card-link title="Admin Documentation" }
    [:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Source Code" }

- ![Piped logo](../assets/img/frontends/piped.svg){ .twemoji } [**Piped (YouTube)**](../frontends.md#piped)

    ---

    [:octicons-info-16:](https://docs.piped.video/docs/self-hosting){ .card-link title="Admin Documentation" }
    [:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Source Code" }

</div>

## More Tools...

Tool recommendations in other categories of the website also provide a self-hosted option, so you could consider this if you are confident in your ability to host the software after reading their documentation.

<div class="grid cards" markdown>

- ![Addy.io logo](../assets/img/email-aliasing/addy.svg){ .twemoji } [**Addy.io**](../email-aliasing.md#addyio)

    ---

    [:octicons-home-16:](https://addy.io){ .card-link title="Homepage" }
    [:octicons-info-16:](https://addy.io/self-hosting){ .card-link title="Admin Documentation" }
    [:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Source Code" }

- ![SimpleLogin logo](../assets/img/email-aliasing/simplelogin.svg){ .twemoji } [**SimpleLogin**](../email-aliasing.md#simplelogin)

    ---

    [:octicons-home-16:](https://addy.io){ .card-link title="Homepage" }
    [:octicons-info-16:](https://github.com/simple-login/app#prerequisites){ .card-link title="Admin Documentation" }
    [:octicons-code-16:](https://github.com/simple-login){ .card-link title="Source Code" }

- ![CryptPad logo](../assets/img/document-collaboration/cryptpad.svg){ .twemoji } [**CryptPad**](../document-collaboration.md#cryptpad)

    ---

    [:octicons-home-16:](https://cryptpad.fr){ .card-link title="Homepage" }
    [:octicons-info-16:](https://docs.cryptpad.org/en/admin_guide/index.html){ .card-link title="Admin Documentation" }
    [:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="Source Code" }

- ![Miniflux logo](../assets/img/news-aggregators/miniflux.svg#only-light){ .twemoji }![Miniflux logo](../assets/img/news-aggregators/miniflux-dark.svg#only-dark){ .twemoji } [**Miniflux**](../news-aggregators.md#miniflux)

    ---

    [:octicons-home-16:](https://miniflux.app){ .card-link title="Homepage" }
    [:octicons-info-16:](https://miniflux.app/docs/index.html#administration-guide){ .card-link title="Admin Documentation" }
    [:octicons-code-16:](https://github.com/miniflux/v2){ .card-link title="Source Code" }

- ![Standard Notes logo](../assets/img/notebooks/standard-notes.svg){ .twemoji } [**Standard Notes**](../notebooks.md#standard-notes)

    ---

    [:octicons-home-16:](https://standardnotes.com){ .card-link title="Homepage" }
    [:octicons-info-16:](https://standardnotes.com/help/47/can-i-self-host-standard-notes){ .card-link title="Admin Documentation" }
    [:octicons-code-16:](https://github.com/standardnotes){ .card-link title="Source Code" }

- ![PrivateBin logo](../assets/img/pastebins/privatebin.svg){ .twemoji } [**PrivateBin**](../pastebins.md#privatebin)

    ---

    [:octicons-home-16:](https://privatebin.info){ .card-link title="Homepage" }
    [:octicons-info-16:](https://github.com/PrivateBin/PrivateBin/blob/master/doc/Installation.md){ .card-link title="Admin Documentation" }
    [:octicons-code-16:](https://github.com/PrivateBin/PrivateBin){ .card-link title="Source Code" }

- ![Paaster logo](../assets/img/pastebins/paaster.svg){ .twemoji } [**Paaster**](../pastebins.md#paaster)

    ---

    [:octicons-home-16:](https://paaster.io){ .card-link title="Homepage" }
    [:octicons-info-16:](https://github.com/WardPearce/paaster#deployment){ .card-link title="Admin Documentation" }
    [:octicons-code-16:](https://github.com/WardPearce/paaster){ .card-link title="Source Code" }

- ![SimpleX Chat logo](../assets/img/messengers/simplex.svg){ .twemoji } [**SimpleX Chat**](../real-time-communication.md#simplex-chat)

    ---

    [:octicons-home-16:](https://simplex.chat){ .card-link title="Homepage" }
    [:octicons-info-16:](https://simplex.chat/docs/server.html){ .card-link title="Admin Documentation" }
    [:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Source Code" }

</div>
