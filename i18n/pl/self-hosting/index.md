---
title: Samodzielny hosting
meta_title: "Self-Hosting Software and Services - Privacy Guides"
description: For our more technical readers, self-hosting software and services can provide additional privacy assurances since you have maximum control over your data.
cover: router.webp
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-server-network: Service Providers](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

**Self-hosting** software and services can be a way to achieve a higher level of privacy through digital sovereignty, particularly independence from cloud servers controlled by product developers or vendors. By self-hosting, we mean hosting applications and data on your own hardware.

Self-hosting your own solutions requires advanced technical knowledge and a deep understanding of the associated risks. By becoming the host for yourself and possibly others, you take on responsibilities you might not otherwise have. Self-hosting privacy software improperly can leave you worse off than using e.g. an end-to-end encrypted service provider, so it is best avoided if you are not already comfortable doing so.

## :material-dns: DNS Filtering

<div class="grid cards" markdown>

- ![Logo AdGuard Home](../assets/img/self-hosting/adguard-home.svg){ .twemoji loading=lazy } [AdGuard Home](dns-filtering.md#adguard-home)
- ![Logo Pi-Hole](../assets/img/self-hosting/pi-hole.svg){ .twemoji loading=lazy } [Pi-Hole](dns-filtering.md#pi-hole)

</div>

[Dowiedz się więcej  :material-arrow-right-drop-circle:](dns-filtering.md)

## :material-email: Email Servers

<div class="grid cards" markdown>

- ![Logo Stalwart](../assets/img/self-hosting/stalwart.svg){ .twemoji loading=lazy } [Stalwart](email-servers.md#stalwart)
- ![Logo Mailcow](../assets/img/self-hosting/mailcow.svg){ .twemoji loading=lazy } [Mailcow](email-servers.md#mailcow)
- ![Logo Mail-in-a-Box](../assets/img/self-hosting/mail-in-a-box.svg){ .twemoji loading=lazy } [Mail-in-a-Box](email-servers.md#mail-in-a-box)

</div>

[Dowiedz się więcej  :material-arrow-right-drop-circle:](email-servers.md)

## :material-file-multiple-outline: Zarządzanie plikami

<div class="grid cards" markdown>

- ![Logo PhotoPrism](../assets/img/self-hosting/photoprism.svg){ .twemoji loading=lazy } [PhotoPrism](file-management.md#photoprism)
- ![Logo FreedomBox](../assets/img/self-hosting/freedombox.svg){ .twemoji loading=lazy } [FreedomBox](file-management.md#freedombox)
- ![Logo Nextcloud](../assets/img/self-hosting/nextcloud.svg){ .twemoji loading=lazy } [Nextcloud](file-management.md#nextcloud)

</div>

[Dowiedz się więcej  :material-arrow-right-drop-circle:](file-management.md)

## :material-form-textbox-password: Zarządzanie hasłami

### Vaultwarden

<div class="admonition recommendation" markdown>

![Logo Vaultwarden](../assets/img/self-hosting/vaultwarden.svg#only-light){ align=right }
![Logo Vaultwarden](../assets/img/self-hosting/vaultwarden-dark.svg#only-dark){ align=right }

**Vaultwarden** is an alternative implementation of [Bitwarden](../passwords.md#bitwarden)'s sync server written in Rust and compatible with official Bitwarden clients, perfect for self-hosted deployment where running the resource-heavy, [official service](https://github.com/bitwarden/server) might not be ideal.

[:octicons-repo-16: Repozytorium](https://github.com/dani-garcia/vaultwarden#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/dani-garcia/vaultwarden/wiki){ .card-link title=Dokumentacja}
[:octicons-code-16:](https://github.com/dani-garcia/vaultwarden){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://github.com/sponsors/dani-garcia){ .card-link title=Wesprzyj" }

</div>

## :material-account-supervisor-circle-outline: Sieci społecznościowe

Self-hosting your own instance of a social network software can help circumvent potential [censorship on a server level](../social-networks.md#censorship-resistance) by a public server's administrator or admin team.

### Mastodon

<div class="admonition recommendation" markdown>

![Logo Mastodon](../assets/img/social-networks/mastodon.svg){ align=right }

**Mastodon** is a social network based on open web protocols and free, open-source software. It uses the decentralized **:simple-activitypub: ActivityPub** protocol.

[:octicons-home-16:](https://joinmastodon.org){ .card-link title="Strona główna" }
[:octicons-info-16:](https://docs.joinmastodon.org/admin/prerequisites){ .card-link title="Dokumentacja administratora" }

</div>

Mastodon [integrates with the Tor network](https://docs.joinmastodon.org/admin/optional/tor) for more extreme scenarios where even your underlying hosting provider is subject to censorship, but this may limit who can access your content to only other servers which integrate with Tor (like most other hidden services).

Mastodon benefits greatly from a large and active self-hosting community, and its administration is comprehensively documented. While many other ActivityPub platforms can require extensive technical knowledge to run and troubleshoot, Mastodon has very stable and tested releases, and it can generally be run securely without issue by anyone who can use the Linux command line and follow step-by-step instructions.

### Element

<div class="admonition recommendation" markdown>

![Logo Element](../assets/img/social-networks/element.svg){ align=right }

**Element** is the flagship client for the **:simple-matrix: Matrix** protocol, an open standard that enables decentralized communication by way of federated chat rooms.

[:octicons-home-16:](https://element.io){ .card-link title="Strona główna" }
[:octicons-info-16:](https://element-hq.github.io/synapse/latest){ .card-link title="Dokumentacja administratora" }
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Kod źródłowy" }

</div>

## :material-flip-to-front: Frontendy (Fasady)

Self-hosting your own instance of a web-based frontend can help you circumvent rate limits that you may encounter on high-traffic, public instances. It is important that you have other people using your instance as well in order for you to blend in. Należy zachować ostrożność przy wyborze miejsca i sposobu hostowania, ponieważ aktywność innych osób będzie powiązana z Twoim serwerem.

<div class="grid cards" markdown>

- ![Logo Redlib](../assets/img/frontends/redlib.svg){ .lg .middle .twemoji } [**Redlib (Reddit)**](../frontends.md#redlib)

  ---

  [:octicons-info-16:](https://github.com/redlib-org/redlib#deployment){ .card-link title="Dokumentacja administratora" }
  [:octicons-code-16:](https://github.com/redlib-org/redlib){ .card-link title="Kod źródłowy" }

- ![Logo ProxiTok](../assets/img/frontends/proxitok.svg){ .lg .middle .twemoji } [**ProxiTok (TikTok)**](../frontends.md#proxitok)

  ---

  [:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki/Self-hosting){ .card-link title="Dokumentacja administratora" }
  [:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Kod źródłowy" }

- ![Logo Invidious](../assets/img/frontends/invidious.svg#only-light){ .twemoji }![Logo Invidious](../assets/img/frontends/invidious-dark.svg#only-dark){ .twemoji } [**Invidious (YouTube)**](../frontends.md#invidious)

  ---

  [:octicons-home-16:](https://invidious.io){ .card-link title="Strona główna" }
  [:octicons-info-16:](https://docs.invidious.io/installation){ .card-link title="Dokumentacja administratora" }
  [:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Kod źródłowy" }

- ![Logo Piped](../assets/img/frontends/piped.svg){ .twemoji } [**Piped (YouTube)**](../frontends.md#piped)

  ---

  [:octicons-info-16:](https://docs.piped.video/docs/self-hosting){ .card-link title="Dokumentacja administratora" }
  [:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Kod źródłowy" }

</div>

## Więcej narzędzi...

Tool recommendations in other categories of the website also provide a self-hosted option, so you could consider this if you are confident in your ability to host the software after reading their documentation.

<div class="grid cards" markdown>

- ![Logo Peergos](../assets/img/cloud/peergos.svg){ .twemoji } [**Peergos**](../cloud.md#peergos)

  ---

  [:octicons-home-16:](https://peergos.org){ .card-link title="Strona główna" }
  [:octicons-info-16:](https://github.com/peergos/peergos#usage---running-locally-to-log-in-to-another-instance){ .card-link title="Dokumentacja administratora" }
  [:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Kod źródłowy" }

- ![Logo Addy.io](../assets/img/email-aliasing/addy.svg){ .twemoji } [**Addy.io**](../email-aliasing.md#addyio)

  ---

  [:octicons-home-16:](https://addy.io){ .card-link title="Strona główna" }
  [:octicons-info-16:](https://addy.io/self-hosting){ .card-link title="Dokumentacja administratora" }
  [:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Kod źródłowy" }

- ![Logo SimpleLogin](../assets/img/email-aliasing/simplelogin.svg){ .twemoji } [**SimpleLogin**](../email-aliasing.md#simplelogin)

  ---

  [:octicons-home-16:](https://addy.io){ .card-link title="Strona główna" }
  [:octicons-info-16:](https://github.com/simple-login/app#prerequisites){ .card-link title="Dokumentacja administratora" }
  [:octicons-code-16:](https://github.com/simple-login){ .card-link title="Kod źródłowy" }

- ![Logo Ente](../assets/img/photo-management/ente.svg){ .twemoji } [**Ente Photos**](../photo-management.md#ente-photos)

  ---

  [:octicons-home-16:](https://ente.com){ .card-link title="Strona główna" }
  [:octicons-info-16:](https://ente.com/help/self-hosting/){ .card-link title="Dokumentacja administratora" }
  [:octicons-code-16:](https://github.com/ente-io/ente){ .card-link title="Kod źródłowy" }

- ![Logo CryptPad](../assets/img/document-collaboration/cryptpad.svg){ .twemoji } [**CryptPad**](../document-collaboration.md#cryptpad)

  ---

  [:octicons-home-16:](https://cryptpad.fr){ .card-link title="Strona główna" }
  [:octicons-info-16:](https://docs.cryptpad.org/en/admin_guide/index.html){ .card-link title="Dokumentacja administratora" }
  [:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="Kod źródłowy" }

- ![Logo Send](../assets/img/file-sharing-sync/send.svg){ .twemoji } [**Send**](../file-sharing.md#send)

  ---

  [:octicons-home-16:](https://send.vis.ee){ .card-link title="Strona główna" }
  [:octicons-info-16:](https://github.com/timvisee/send/blob/master/docs/deployment.md){ .card-link title="Dokumentacja administratora" }
  [:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="Kod źródłowy" }

- ![Logo LibreTranslate](../assets/img/language-tools/libretranslate.png){ .twemoji } [**LibreTranslate**](../language-tools.md#libretranslate)

  ---

  [:octicons-home-16:](https://libretranslate.com){ .card-link title="Strona główna" }
  [:octicons-info-16:](https://docs.libretranslate.com){ .card-link title="Dokumentacja administratora" }
  [:octicons-code-16:](https://github.com/LibreTranslate/LibreTranslate){ .card-link title="Kod źródłowy" }

- ![Logo Miniflux](../assets/img/news-aggregators/miniflux.svg#only-light){ .twemoji }![Logo Miniflux](../assets/img/news-aggregators/miniflux-dark.svg#only-dark){ .twemoji } [**Miniflux**](../news-aggregators.md#miniflux)

  ---

  [:octicons-home-16:](https://miniflux.app){ .card-link title="Strona główna" }
  [:octicons-info-16:](https://miniflux.app/docs/index.html#administration-guide){ .card-link title="Dokumentacja administratora" }
  [:octicons-code-16:](https://github.com/miniflux/v2){ .card-link title="Kod źródłowy" }

- ![Logo Standard Notes](../assets/img/notebooks/standard-notes.svg){ .twemoji } [**Standard Notes**](../notebooks.md#standard-notes)

  ---

  [:octicons-home-16:](https://standardnotes.com){ .card-link title="Strona główna" }
  [:octicons-info-16:](https://standardnotes.com/help/47/can-i-self-host-standard-notes){ .card-link title="Dokumentacja administratora" }
  [:octicons-code-16:](https://github.com/standardnotes){ .card-link title="Kod źródłowy" }

- ![Logo PrivateBin](../assets/img/pastebins/privatebin.svg){ .twemoji } [**PrivateBin**](../pastebins.md#privatebin)

  ---

  [:octicons-home-16:](https://privatebin.info){ .card-link title="Strona główna" }
  [:octicons-info-16:](https://github.com/PrivateBin/PrivateBin/blob/master/doc/Installation.md){ .card-link title="Dokumentacja administratora" }
  [:octicons-code-16:](https://github.com/PrivateBin/PrivateBin){ .card-link title="Kod źródłowy" }

- ![Logo Paaster](../assets/img/pastebins/paaster.svg){ .twemoji } [**Paaster**](../pastebins.md#paaster)

  ---

  [:octicons-home-16:](https://paaster.io){ .card-link title="Strona główna" }
  [:octicons-info-16:](https://github.com/WardPearce/paaster#deployment){ .card-link title="Dokumentacja administratora" }
  [:octicons-code-16:](https://github.com/WardPearce/paaster){ .card-link title="Kod źródłowy" }

- ![Logo SimpleX Chat](../assets/img/messengers/simplex.svg){ .twemoji } [**SimpleX Chat**](../real-time-communication.md#simplex-chat)

  ---

  [:octicons-home-16:](https://simplex.chat){ .card-link title="Strona główna" }
  [:octicons-info-16:](https://simplex.chat/docs/server.html){ .card-link title="Dokumentacja administratora" }
  [:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Kod źródłowy" }

</div>
