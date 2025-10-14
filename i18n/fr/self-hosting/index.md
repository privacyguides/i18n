---
title: Auto-Hébergement
meta_title: "Logiciels et services autohébergés - Privacy Guides"
description: Pour nos lecteurs les plus avancés, l'auto-hébergement de logiciel et de services peut donner des garanties additionnelles en termes de confidentialité en leur permettant d'avoir un contrôle maximal sur leurs données.
cover: router.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-server-network: Fournisseurs de services](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

**Autohéberger** des logiciels et des services peut vous permettre d'atteindre des niveaux élevés de confidentialité grâce à la souveraineté numérique, en particulier par rapport aux serveurs cloud contrôlés par des entreprises ou des développeurs. L'auto-hébergement désigne le fait d'héberger vos applications et vos données sur votre propre hardware.

L'auto-hébergement nécessite des connaissances techniques avancées et une bonne compréhension des risques associés. En devanant votre propre hébergeur, et potentiellement celui d'autres personnes, vous acceptez de prendre certaines responsabilités spécifiques. Mal utiliser des logiciels dédiés à la confidentialité en auto-hébergement implique parfois des risques plus grands qu'utiliser les services d'un tiers chiffrés de bout en bout par exemple. Il peut donc être préférable de n'y avoir recours que si vous êtes vraiment à l'aise.

## :material-dns: Le filtrage DNS

<div class="grid cards" markdown>

- ![Logo de AdGuard Home](../assets/img/self-hosting/adguard-home.svg){ .twemoji loading=lazy } [AdGuard Home](dns-filtering.md#adguard-home)
- ![Logo de Pi-Hole](../assets/img/self-hosting/pi-hole.svg){ .twemoji loading=lazy } [Pi-Hole](dns-filtering.md#pi-hole)

</div>

[Pour en savoir plus :material-arrow-right-drop-circle:](dns-filtering.md)

## :material-email: Serveurs de messagerie (mail)

<div class="grid cards" markdown>

- ![logo de Stalwart](../assets/img/self-hosting/stalwart.svg){ .twemoji loading=lazy } [Stalwart](email-servers.md#stalwart)
- ![logo de Mailcow](../assets/img/self-hosting/mailcow.svg){ .twemoji loading=lazy } [Mailcow](email-servers.md#mailcow)
- ![logo de Mail-in-a-Box](../assets/img/self-hosting/mail-in-a-box.svg){ .twemoji loading=lazy } [Mail-in-a-Box](email-servers.md#mail-in-a-box)

</div>

[En savoir plus :material-arrow-right-drop-circle:](email-servers.md)

## :material-file-multiple-outline: Gestion des fichiers

<div class="grid cards" markdown>

- ![Logo de PhotoPrism](../assets/img/self-hosting/photoprism.svg){ .twemoji loading=lazy } [PhotoPrism](file-management.md#photoprism)
- ![Logo de FreedomBox](../assets/img/self-hosting/freedombox.svg){ .twemoji loading=lazy } [FreedomBox](file-management.md#freedombox)
- ![Logo de Nextcloud](../assets/img/self-hosting/nextcloud.svg){ .twemoji loading=lazy } [Nextcloud](file-management.md#nextcloud)

</div>

[Pour en savoir plus :material-arrow-right-drop-circle:](file-management.md)

## :material-form-textbox-password: Gestion des mots de passe

### Vaultwarden

<div class="admonition recommendation" markdown>

![Logo de Vaultwarden](../assets/img/self-hosting/vaultwarden.svg#only-light){ align=right }
![Logo de Vaultwarden](../assets/img/self-hosting/vaultwarden-dark.svg#only-dark){ align=right }

**Vaultwarden** est une implémentation alternative du serveur de synchronisation de [Bitwarden](../passwords.md#bitwarden) écrit en Rust et compatible avec les clients officiels de Bitwarden, parfaitement adapté à l'auto-hébergement lorsque l'utilisation du [service officiel](https://github.com/bitwarden/server), gourmand en ressources, n'est pas idéale.

[:octicons-repo-16: Dépôt](https://github.com/dani-garcia/vaultwarden#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/dani-garcia/vaultwarden/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/dani-garcia/vaultwarden){ .card-link title="Code Source" }
[:octicons-heart-16:](https://github.com/sponsors/dani-garcia){ .card-link title="Contribuer" }

</div>

## :material-account-supervisor-circle-outline: Réseaux sociaux

L'auto-hébergement de vos propres instances de réseaux sociaux peut être un bon moyen de contourner une potentielle [censure au niveau serveur](../social-networks.md#censorship-resistance) d'un administrateur ou d'une équipe d'administration de serveur public.

### Mastodon

<div class="admonition recommendation" markdown>

![Logo de Mastodon](../assets/img/social-networks/mastodon.svg){ align=right }

**Mastodon** est un réseau social basé sur un protocole web ouvert et un logiciel libre et open-source. Il utilise le protocole décentralisé **:simple-activitypub: ActivityPub**.

[:octicons-home-16:](https://joinmastodon.org){ .card-link title= "Page d'accueil" }
[:octicons-info-16:](https://docs.joinmastodon.org/admin/prerequisites){ .card-link title="Documentation Adiministrateurs" }

</div>

Mastodon [intègre le réseau Tor](https://docs.joinmastodon.org/admin/optional/tor) pour les cas extrêmes ou même le fournisseur d'hébergement est sujet à la censure, cela peut néanmoins limiter l'accès à votre contenu aux autres serveurs qui intègre eux même Tor (comme la plupart des autres services cachés).

Mastodon possède une communauté d'auto-hébergement importante et active, et son administration est très bien documentée. Contrairement à beaucoup d'autre plateforme ActivityPub qui requière des connaissances techniques très importante en cas de problème, les versions de Mastodon sont très stables et testées au préalable, et peut généralement être exécuté sans problème de manière sécurisée par n'importe qui pouvant utiliser un terminal Linux et suivre des instructions étape par étape.

### Element

<div class="admonition recommendation" markdown>

![logo de Element](../assets/img/social-networks/element.svg){ align=right }

**Element** est le client phare du protocole **:simple-matrix: Matrix**, un standard ouvert qui permet des communications décentralisées grâces à salons de discussion fédérés.

[:octicons-home-16:](https://element.io){ .card-link title="Page d'accueil" }
[:octicons-info-16:](https://element-hq.github.io/synapse/latest){ .card-link title="Documentation Administrateur" }
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Code Source" }

</div>

## :material-flip-to-front: Les Frontends

L'auto-hébergement de votre propre instance d'un frontend web peut vous aider à contourner les limitations que vous pouvez rencontrer sur les instances publiques à fort trafic. Afin de vous fondre dans la masse, il est aussi important que d'autres personnes utilisent votre instance. Vous devriez faire attention à l'endroit et à la manière dont vous hébergez, car l'utilisation par d'autres personnes sera liée à votre hébergement.

<div class="grid cards" markdown>

- ![Logo de Redlib](../assets/img/frontends/redlib.svg){ .lg .middle .twemoji } [**Redlib (Reddit)**](../frontends.md#redlib)

  ---

  [:octicons-info-16:](https://github.com/redlib-org/redlib#deployment){ .card-link title="Documentation Administrateur" }
  [:octicons-code-16:](https://github.com/redlib-org/redlib){ .card-link title="Code Source" }

- ![Logo de ProxiTok](../assets/img/frontends/proxitok.svg){ .lg .middle .twemoji } [**ProxiTok (TikTok)**](../frontends.md#proxitok)

  ---

  [:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki/Self-hosting){ .card-link title="Documentation Admnistrateur" }
  [:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Code Source" }

- ![Logo de Invidious](../assets/img/frontends/invidious.svg#only-light){ .twemoji }![Logo de Invidious](../assets/img/frontends/invidious-dark.svg#only-dark){ .twemoji } [**Invidious (YouTube)**](../frontends.md#invidious)

  ---

  [:octicons-home-16:](https://invidious.io){ .card-link title="Page d'accueil" }
  [:octicons-info-16:](https://docs.invidious.io/installation){ .card-link title="Documentation Administrateur" }
  [:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Code Source" }

- ![Logo de Piped](../assets/img/frontends/piped.svg){ .twemoji } [**Piped (YouTube)**](../frontends.md#piped)

  ---

  [:octicons-info-16:](https://docs.piped.video/docs/self-hosting){ .card-link title="Documentation Administrateur" }
  [:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Code Source" }

</div>

## Plus d'outils...

Si vous vous sentez capable d'auto-héberger des logiciels après avoir lu leur documentation, des options d'auto-hébergement sont disponibles dans nos autres recommandations.

<div class="grid cards" markdown>

- ![Logo de Peergos](../assets/img/cloud/peergos.svg){ .twemoji } [**Peergos**](../cloud.md#peergos)

  ---

  [:octicons-home-16:](https://peergos.org){ .card-link title="Page d'Accueil" }
  [:octicons-info-16:](https://github.com/peergos/peergos#usage---running-locally-to-log-in-to-another-instance){ .card-link title="Documentation Admin" }
  [:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Code Source" }

- ![Logo de Addy.io](../assets/img/email-aliasing/addy.svg){ .twemoji } [**Addy.io**](../email-aliasing.md#addyio)

  ---

  [:octicons-home-16:](https://addy.io){ .card-link title="Page d'accueil" }
  [:octicons-info-16:](https://addy.io/self-hosting){ .card-link title="Documentation Administrateur" }
  [:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Code Source" }

- ![Logo de SimpleLogin](../assets/img/email-aliasing/simplelogin.svg){ .twemoji } [**SimpleLogin**](../email-aliasing.md#simplelogin)

  ---

  [:octicons-home-16:](https://addy.io){ .card-link title="Page d'accueil" }
  [:octicons-info-16:](https://github.com/simple-login/app#prerequisites){ .card-link title="Documentation Administrateur" }
  [:octicons-code-16:](https://github.com/simple-login){ .card-link title="Code Source" }

- ![Logo de Ente](../assets/img/photo-management/ente.svg){ .twemoji } [**Ente Photos**](../photo-management.md#ente-photos)

  ---

  [:octicons-home-16:](https://ente.io){ .card-link title="Page d'Accueil" }
  [:octicons-info-16:](https://help.ente.io/self-hosting){ .card-link title="Documentation Admin" }
  [:octicons-code-16:](https://github.com/ente-io/ente){ .card-link title="Code Source" }

- ![Logo de CryptPad](../assets/img/document-collaboration/cryptpad.svg){ .twemoji } [**CryptPad**](../document-collaboration.md#cryptpad)

  ---

  [:octicons-home-16:](https://cryptpad.fr){ .card-link title="Page d'accueil" }
  [:octicons-info-16:](https://docs.cryptpad.org/en/admin_guide/index.html){ .card-link title="Documentation Administrateur" }
  [:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="Code Source" }

- ![Logo de Send](../assets/img/file-sharing-sync/send.svg){ .twemoji } [**Send**](../file-sharing.md#send)

  ---

  [:octicons-home-16:](https://send.vis.ee){ .card-link title="Page d'Accueil" }
  [:octicons-info-16:](https://github.com/timvisee/send/blob/master/docs/deployment.md){ .card-link title="Documentation Admin" }
  [:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="Code Source" }

- ![Logo de LibreTranslate](../assets/img/language-tools/libretranslate.png){ .twemoji } [**LibreTranslate**](../language-tools.md#libretranslate)

  ---

  [:octicons-home-16:](https://libretranslate.com){ .card-link title="Page d'Accueil" }
  [:octicons-info-16:](https://docs.libretranslate.com){ .card-link title="Documentation Admin" }
  [:octicons-code-16:](https://github.com/LibreTranslate/LibreTranslate){ .card-link title="Code Source" }

- ![Logo de Miniflux](../assets/img/news-aggregators/miniflux.svg#only-light){ .twemoji }![Miniflux logo](../assets/img/news-aggregators/miniflux-dark.svg#only-dark){ .twemoji } [**Miniflux**](../news-aggregators.md#miniflux)

  ---

  [:octicons-home-16:](https://miniflux.app){ .card-link title="Page d'accueil" }
  [:octicons-info-16:](https://miniflux.app/docs/index.html#administration-guide){ .card-link title="Documentation Administrateur" }
  [:octicons-code-16:](https://github.com/miniflux/v2){ .card-link title="Code Source" }

- ![Logo de Standard Notes](../assets/img/notebooks/standard-notes.svg){ .twemoji } [**Standard Notes**](../notebooks.md#standard-notes)

  ---

  [:octicons-home-16:](https://standardnotes.com){ .card-link title="Page d'accueil" }
  [:octicons-info-16:](https://standardnotes.com/help/47/can-i-self-host-standard-notes){ .card-link title="Documentation Administrateur" }
  [:octicons-code-16:](https://github.com/standardnotes){ .card-link title="Code Source" }

- ![Logo de PrivateBin](../assets/img/pastebins/privatebin.svg){ .twemoji } [**PrivateBin**](../pastebins.md#privatebin)

  ---

  [:octicons-home-16:](https://privatebin.info){ .card-link title="Page d'accueil" }
  [:octicons-info-16:](https://github.com/PrivateBin/PrivateBin/blob/master/doc/Installation.md){ .card-link title="Documentation Administrateur" }
  [:octicons-code-16:](https://github.com/PrivateBin/PrivateBin){ .card-link title="Code Source" }

- ![Logo de Paaster](../assets/img/pastebins/paaster.svg){ .twemoji } [**Paaster**](../pastebins.md#paaster)

  ---

  [:octicons-home-16:](https://paaster.io){ .card-link title="Page d'accueil" }
  [:octicons-info-16:](https://github.com/WardPearce/paaster#deployment){ .card-link title="Documentation Administrateur" }
  [:octicons-code-16:](https://github.com/WardPearce/paaster){ .card-link title="Code Source" }

- ![Logo de SimpleX Chat](../assets/img/messengers/simplex.svg){ .twemoji } [**SimpleX Chat**](../real-time-communication.md#simplex-chat)

  ---

  [:octicons-home-16:](https://simplex.chat){ .card-link title="Page d'accueil" }
  [:octicons-info-16:](https://simplex.chat/docs/server.html){ .card-link title="Documentation Administrateur" }
  [:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Code Source" }

</div>
