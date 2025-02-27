---
title: Alias de courrier électronique
icon: material/email-lock
description: Un service d'alias d'adresses électroniques vous permet de générer facilement une nouvelle adresse électronique pour chaque site web auquel vous vous inscrivez.
cover: email-aliasing.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Surveillance Capitalism](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }
- [:material-account-search: Public Exposure](basics/common-threats.md#limiting-public-information){ .pg-green }

An **email aliasing service** allows you to easily generate a new email address for every website you register for. Les alias que vous générez sont ensuite transférés vers une adresse électronique de votre choix, masquant ainsi votre adresse électronique "principale" et l'identité de votre [fournisseur d'adresses électroniques](email.md). Un véritable alias d'adresse électronique est préférable à l'adressage plus couramment utilisé et pris en charge par de nombreux fournisseurs, qui vous permet de créer des alias du type "nom de famille+[n'importe où]@exemple.com", parce que les sites web, les annonceurs et les réseaux de suivi peuvent trivialement supprimer tout ce qui se trouve après le signe `+`. Des organisations telles que l'[IAB] (https://en.wikipedia.org/wiki/Interactive_Advertising_Bureau) exigent que les annonceurs [normalisent les adresses électroniques] (https://shkspr.mobi/blog/2023/01/the-iab-loves-tracking-users-but-it-hates-users-tracking-them) afin qu'elles puissent être corrélées et suivies, sans tenir compte des souhaits des utilisateurs en matière de protection de la vie privée.

<div class="grid cards" markdown>

- ![addy.io logo](assets/img/email-aliasing/addy.svg){ .twemoji } [addy.io](email-aliasing.md#addyio)
- ![SimpleLogin logo](assets/img/email-aliasing/simplelogin.svg){ .twemoji } [SimpleLogin](email-aliasing.md#simplelogin)

</div>

L'alias d'e-mail peut également servir de protection au cas où votre fournisseur E-Mail cesserait ses activités. Dans ce cas, vous pouvez facilement rediriger vos alias vers une nouvelle adresse e-mail. En revanche, vous faites confiance au service d'alias pour qu'il continue de fonctionner.

L'utilisation d'un service d'alias d'e-mail dédié présente également un certain nombre d'avantages par rapport à un alias fourre-tout sur un domaine personnalisé :

- Les alias peuvent être activés et désactivés individuellement lorsque vous en avez besoin, ce qui empêche les sites web de vous envoyer des courriels au hasard.
- Les réponses sont envoyées à partir de l'adresse alias, masquant ainsi votre véritable adresse électronique.

Ils présentent également un certain nombre d'avantages par rapport aux services de "courrier électronique temporaire" :

- Les alias sont permanents et peuvent être réactivés si vous devez recevoir quelque chose comme une réinitialisation de mot de passe.
- Les courriels sont envoyés à votre boîte aux lettres électronique de confiance plutôt que d'être stockés par le fournisseur d'alias.
- Les services de messagerie temporaire proposent généralement des boîtes aux lettres publiques accessibles à toute personne connaissant l'adresse, alors que les alias sont privés.

Our email aliasing recommendations are providers that allow you to create aliases on domains they control, as well as on your own custom domain(s) for a modest yearly fee. Ils peuvent également être auto-hébergés si vous souhaitez un contrôle maximal. Toutefois, l'utilisation d'un domaine personnalisé peut présenter des inconvénients en matière de protection de la vie privée : Si vous êtes la seule personne à utiliser votre domaine personnalisé, vos actions peuvent être facilement suivies sur les sites web simplement en regardant le nom de domaine dans l'adresse électronique et en ignorant tout ce qui se trouve avant le signe at (@).

L'utilisation d'un service d'alias nécessite de faire confiance à la fois à votre fournisseur de courrier électronique et à votre fournisseur d'alias pour vos messages non cryptés. Some providers mitigate this slightly with automatic PGP encryption[^1], which reduces the number of parties you need to trust from two to one by encrypting incoming emails before they are delivered to your final mailbox provider.

### addy.io

<div class="admonition recommendation" markdown>

![addy.io logo](assets/img/email-aliasing/addy.svg){ align=right }

**addy.io** lets you create 10 domain aliases on a shared domain for free, or unlimited "standard" aliases.

[:octicons-home-16: Homepage](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://addy.io/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://addy.io/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-android: Android](https://addy.io/faq/#is-there-an-android-app)
- [:material-apple-ios: iOS](https://addy.io/faq/#is-there-an-ios-app)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/addy_io)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/addyio-anonymous-email-fo/iadbdpnoknmbdeolbapdackdcogdmjpe)

</details>

</div>

Le nombre d'alias partagés (qui se terminent par un domaine partagé comme @addy.io) que vous pouvez créer est limité à 10 sur le plan gratuit d'addy.io, à 50 sur leur plan à 1 $/mois et illimité sur le plan à 4 $/mois (facturé 3 $ pour un an). You can pay for these plans using [cryptocurrency](https://addy.io/help/subscribing-with-cryptocurrency) or purchase a voucher code from [ProxyStore](https://addy.io/help/voucher-codes), addy.io's official reseller.

Vous pouvez créer un nombre illimité d'alias standard qui se terminent par un domaine comme @[nom d'utilisateur].addy.io ou un domaine personnalisé sur les plans payants. Toutefois, comme indiqué précédemment, cela peut nuire à la protection de la vie privée, car les gens peuvent facilement relier vos alias standard en se basant uniquement sur le nom de domaine. Ils sont utiles lorsqu'un domaine partagé peut être bloqué par un service. Securitum a [audité](https://addy.io/blog/addy-io-passes-independent-security-audit) addy.io en septembre 2023 et aucune vulnérabilité importante [n'a été identifiée](https://addy.io/addy-io-security-audit.pdf).

Fonctionnalités gratuites notables :

- [x] 10 Alias partagés
- [x] Alias standard illimités
- [ ] No Outgoing Replies
- [x] 1 boîte aux lettres pour les destinataires
- [x] Automatic PGP Encryption[^1]

If you cancel your subscription, you will still enjoy the features of your paid plan until the billing cycle ends. After the end of your current billing cycle, most paid features (including any custom domains) will be [deactivated](https://addy.io/faq/#what-happens-if-i-have-a-subscription-but-then-cancel-it), paid account settings will be reverted to their defaults, and catch-all will be enabled if it was previously disabled.

### SimpleLogin

<div class="admonition recommendation" markdown>

![SimpleLogin logo](assets/img/email-aliasing/simplelogin.svg){ align=right }

**SimpleLogin** est un service gratuit qui fournit des alias de courrier électronique sur une variété de noms de domaine partagés, et offre en option des fonctions payantes comme des alias illimités et des domaines personnalisés.

[:octicons-home-16: Homepage](https://simplelogin.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplelogin.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://simplelogin.io/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simple-login){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
- [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/simplelogin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
- [:simple-safari: Safari](https://apps.apple.com/app/id6475835429)

</details>

</div>

SimpleLogin a été [racheté par Proton AG] (https://proton.me/news/proton-and-simplelogin-join-forces) le 8 avril 2022. Si vous utilisez Proton Mail pour votre boîte mail principale, SimpleLogin est un excellent choix. Les deux produits étant désormais détenus par la même société, vous ne devez plus faire confiance qu'à une seule entité. Nous supposons également que SimpleLogin sera plus étroitement intégré aux offres de Proton à l'avenir. SimpleLogin continue de prendre en charge la redirection vers le fournisseur d'e-mail de votre choix. Securitum a [audité](https://simplelogin.io/blog/security-audit) SimpleLogin au début de 2022 et tous les problèmes [ont été résolus](https://simplelogin.io/audit2022/web.pdf).

Vous pouvez lier votre compte SimpleLogin dans les paramètres avec votre compte Proton. If you have Proton Pass Plus, Proton Unlimited, or any multi-user Proton plan, you will have SimpleLogin Premium for free.

You can also purchase a voucher code for SimpleLogin Premium anonymously via their official reseller, [ProxyStore](https://simplelogin.io/faq).

Fonctionnalités gratuites notables :

- [x] 10 Alias partagés
- [x] Réponses illimitées
- [x] 1 boîte aux lettres pour les destinataires
- [ ] Automatic PGP Encryption[^1] is only available on paid plans

When your subscription ends, all aliases you created will still be able to receive and send emails. However, you cannot create any new aliases that would exceed the free plan limit, nor can you add a new domain, directory, or mailbox.

## Critères

\*\*En plus de [nos critères standards] (about/criteria.md), nous évaluons les fournisseurs d'alias d'email selon les mêmes critères que nos [critères pour les fournisseurs d'email] (email.md#criteria), le cas échéant. Nous vous conseillons de vous familiariser avec cette liste avant de choisir un service de courrier électronique et de mener vos propres recherches pour vous assurer que le fournisseur que vous choisissez est celui qui vous convient le mieux.

[^1]: Automatic PGP encryption allows you to encrypt non-encrypted incoming emails before they are forwarded to your mailbox, making sure your primary mailbox provider never sees unencrypted email content.
