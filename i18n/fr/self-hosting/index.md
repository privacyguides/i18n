---
title: Auto-Hébergement
meta_title: "Logiciels et Services Auto-Hébergés - Privacy Guides"
description: Pour nos lecteurs les plus expérimentés, les logiciels et les services auto-hébergés permettent de contrôler au maximum vos données afin d'avoir les meilleures garanties en termes de confidentialité.
cover: router.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-server-network: Fournisseurs de services](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

Les **logiciels et services auto-hébergés** peuvent être un bon moyen d'atteindre un plus haut niveau de souveraineté numérique, en particulier en remplaçant les clouds contrôlés par des entreprises ou des développeurs. By self-hosting, we mean hosting applications and data on your own hardware.

L'auto-hébergement nécessite des connaissances techniques avancées et une bonne compréhension des risques associés. En devanant votre propre hébergeur, et potentiellement celui d'autres personnes, vous acceptez de prendre certaines responsabilités spécifiques. Mal utiliser des logiciels dédiés à la confidentialité en auto-hébergement implique parfois des risques plus grands qu'utiliser les services d'un tiers chiffrés de bout en bout par exemple. Il peut donc être préférable de n'y avoir recours que si vous êtes vraiment à l'aise.

## :material-email: Serveurs de messagerie (mail)

<div class="grid cards" markdown>

- ![logo de Stalwart](../assets/img/self-hosting/stalwart.svg){ .twemoji loading=lazy } [Stalwart](email-servers.md#stalwart)
- ![logo de Mailcow](../assets/img/self-hosting/mailcow.svg){ .twemoji loading=lazy } [Mailcow](email-servers.md#mailcow)
- ![logo de Mail-in-a-Box](../assets/img/self-hosting/mail-in-a-box.svg){ .twemoji loading=lazy } [Mail-in-a-Box](email-servers.md#mail-in-a-box)

</div>

[En savoir plus :material-arrow-right-drop-circle:](email-servers.md)

## :material-account-supervisor-circle-outline: Réseaux sociaux

L'auto-hébergement de vos propres instances de réseaux sociaux peut être un bon moyen de contourner une potentielle [censure au niveau serveur](../social-networks.md#censorship-resistance) d'un administrateur ou d'une équipe d'administration de serveur public.

### Mastodon

<div class="admonition recommendation" markdown>

![Logo de Mastodon](../assets/img/social-networks/mastodon.svg){ align=right }

**Mastodon** est un réseau social basé sur un protocole web ouvert et un logiciel libre et open-source. Il utilise le protocole décentralisé **:simple-activitypub: ActivityPub**.

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

Self-hosting your own instance of a web-based frontend can help you circumvent rate limits that you may encounter on high-traffic, public instances. It is important that you have other people using your instance as well in order for you to blend in. Vous devriez faire attention à l'endroit et à la manière dont vous hébergez, car l'utilisation par d'autres personnes sera liée à votre hébergement.

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
