---
title: Serveurs de messagerie
meta_title: "Self-Hosting Email - Privacy Guides"
icon: material/email
description: Pour nos lecteurs plus avancés, l'auto-hébergement de votre propre courrier électronique peut fournir des garanties supplémentaires en matière de confidentalité en vous permettant de contrôler au maximum vos données.
cover: email.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-server-network: Fournisseurs de services](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

Advanced system administrators may consider setting up their own **email server**. Les serveurs mail requière de une attention particulière et une maintenance continue pour garantir leur fiabilité et leur sécurité. En plus des solutions "tout-en-un" présentées ci-dessous, nous avons sélectionné quelques articles qui traitent d'une approche plus manuelle :

- [Mise en place d'un serveur de messagerie avec OpenSMTPD, Dovecot et Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (eng) (2019)
- [Comment gérer son propre serveur de messagerie](https://www.c0ffee.net/blog/mail-server-guide) (eng) (août 2017)

## Stalwart

<div class="admonition recommendation" markdown>

![Stalwart logo](../assets/img/self-hosting/stalwart.svg){ align=right }

**Stalwart** est un serveur de messagerie plus récent écrit en Rust, il prend en charge JMAP en plus des standards IMAP, POP3, et SMTP. Il offre une grande variété d'options de configuration, ainsi que des paramètres par défaut très raisonnable en termes de sécurité et de fonctionnalité qui le rendent facile à utiliser immédiatement. Il dispose d'une administration web avec le support 2FA TOTP et permet d'utiliser votre clé publique PGP pour chiffrer **tous** les messages entrants.

[:octicons-home-16: Page d'accueil](https://stalw.art){ .md-button .md-button--primary }
[:octicons-info-16:](https://stalw.art/docs/get-started){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/stalwartlabs){ .card-link title="Code source" }
[:octicons-heart-16:](https://github.com/sponsors/stalwartlabs){ .card-link title=Contribuer }

</div>

L'[implémentation PGP de Stalwart] (https://stalw.art/docs/encryption/overview) est unique parmi nos recommandations auto-hébergées et vous permet d'exploiter votre propre serveur de messagerie avec un stockage de messages à connaissance nulle (zero-knowledge encryption). En configurant en plus Web Key Directory (WKD) sur votre domaine, et si vous utilisez un client mail qui prend en charge PGP et WKD pour les mails sortants (comme Thunderbird), alors c'est la façon la plus simple d'obtenir la compatibilté E2EE auto-hebergée avec tous les utilisateurs de [Proton Mail](../email.md#proton-mail).

Stalwart n'a **pas** de webmail intégré, vous devrez donc l'utiliser avec un [client mail dédié](../email-clients.md) ou trouver un webmail open-source auto-hébergeable, comme l'application Mail de Nextcloud.

A _Privacy Guides_, nous utilisons Stalwart pour notre propre courrier électronique.

## Mailcow

<div class="admonition recommendation" markdown>

![logo de Mailcow](../assets/img/self-hosting/mailcow.svg){ align=right }

**Mailcow** est un serveur de messagerie avancé, parfait pour les habitués de Linux. Il possède tout ce dont vous avez besoin dans un conteneur Docker : un serveur de messagerie avec prise en charge de DKIM, une surveillance antivirus et spam, un webmail et ActiveSync avec SOGo, et une administration web avec prise en charge de 2FA.

[:octicons-home-16: Page d'accueil](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title=Documentation }
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Code source" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title=Contribuer" }

</div>

## Mail-in-a-Box

<div class="admonition recommendation" markdown>

![Logo de Mail-in-a-Box](../assets/img/self-hosting/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** est un script d'installation automatisé pour déployer un serveur de messagerie sur Ubuntu. Son but est de faciliter la mise en place de son propre serveur de messagerie.

[:octicons-home-16: Page d'accueil](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Code source" }

</div>
