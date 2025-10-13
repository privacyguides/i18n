---
title: "Alias de courrier électronique"
icon: material/email-lock
description: Un service d'alias d'adresses électroniques vous permet de générer facilement une nouvelle adresse électronique pour chaque site web auquel vous vous inscrivez.
cover: email-aliasing.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-account-cash: Capitalisme de Surveillance](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }
- [:material-account-search: Exposition Publique](basics/common-threats.md#limiting-public-information){ .pg-green }

Lorsque vous avez besoin de créé un compte sur un site web, un **service d'alias mail** vous permet de générer facilement une nouvelle adresse mail. Les alias que vous générez sont ensuite transférés vers une adresse électronique de votre choix, masquant ainsi votre adresse électronique "principale" et l'identité de votre [fournisseur d'adresses électroniques](email.md).

L'alias d'e-mail peut également servir de protection au cas où votre fournisseur E-Mail cesserait ses activités. Dans ce cas, vous pouvez facilement rediriger vos alias vers une nouvelle adresse e-mail. En revanche, vous faites confiance au service d'alias pour qu'il continue de fonctionner.

## Avantages

Utiliser un service qui vous permet de gérer individuellement chaque alias mail présente de nombreux bénéfices par rapport aux méthodes conventionnelles de gestion de boite mail :

### Comparé au Plus Addressing

Un véritable alias d'adresse électronique est préférable à l'adressage plus couramment utilisé et pris en charge par de nombreux fournisseurs, qui vous permet de créer des alias du type "nom de famille+[n'importe où]@exemple.com", parce que les sites web, les annonceurs et les réseaux de suivi peuvent trivialement supprimer tout ce qui se trouve après le signe `+`. Des organisations telles que l'[IAB] (https://en.wikipedia.org/wiki/Interactive_Advertising_Bureau) exigent que les annonceurs [normalisent les adresses électroniques] (https://shkspr.mobi/blog/2023/01/the-iab-loves-tracking-users-but-it-hates-users-tracking-them) afin qu'elles puissent être corrélées et suivies, sans tenir compte des souhaits des utilisateurs en matière de protection de la vie privée.

### Comparé aux alias fourre-tout

L'utilisation d'un service d'alias mail dédié plutôt qu'un alias fourre-tout sur un nom de domaine personnalisé présente plusieurs avantages :

- Les alias peuvent être activés et désactivés individuellement lorsque vous en avez besoin, ce qui empêche les sites web de vous envoyer des courriels au hasard.
- Les réponses sont envoyées à partir de l'adresse alias, masquant ainsi votre véritable adresse électronique.

### Comparé aux services de mail temporaires

Les services d'alias mail permettent de :

- Les alias sont permanents et peuvent être réactivés si vous devez recevoir quelque chose comme une réinitialisation de mot de passe.
- Les courriels sont envoyés à votre boîte aux lettres électronique de confiance plutôt que d'être stockés par le fournisseur d'alias.
- Les services de messagerie temporaire proposent généralement des boîtes aux lettres publiques accessibles à toute personne connaissant l'adresse, alors que les alias sont privés.

## Fournisseurs recommandés

<div class="grid cards" markdown>

- ![Logo de Addy.io](assets/img/email-aliasing/addy.svg){ .twemoji } [Addy.io](email-aliasing.md#addyio)
- ![Logo de SimpleLogin](assets/img/email-aliasing/simplelogin.svg){ .twemoji } [SimpleLogin](email-aliasing.md#simplelogin)

</div>

Les fournisseurs que nous recommandons vous permettent de créer des alias avec leur(s) nom(s) de domaine, mais aussi avec votre propre nom de domaine, moyennant un coût annuel raisonnable. Ils peuvent également être auto-hébergés si vous souhaitez un contrôle maximal. Utiliser votre propre nom de domaine peut cependant parfois nuire à la confidentialité : si vous êtes la seule personne à l'utiliser, il est possible de retracer vos activités sur différents sites web simplement en cherchant le nom de domaine de l'adresse mail que vous avez utilisé.

L'utilisation d'un service d'alias nécessite de faire confiance à la fois à votre fournisseur de courrier électronique et à votre fournisseur d'alias pour vos messages non cryptés. Certains fournisseurs proposent d'atténuer ce problème avec un chiffrement PGP[^1], réduisant ainsi le nombre d'intermédiaires ayant accès à vos données en chiffrant les mails entrants avant qu'ils ne passent par le fournisseur de votre boite mail.

### Addy.io

<div class="admonition recommendation" markdown>

![Logo de Addy.io](assets/img/email-aliasing/addy.svg){ align=right }

**Addy.io** vous permet de créer gratuitement 10 alias avec un nom de domaine partagé, ou un nombre illimité d'alias [standards](https://addy.io/faq/#what-is-a-standard-alias).

[:octicons-home-16: Page d'Accueil](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://addy.io/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Code Source" }
[:octicons-heart-16:](https://addy.io/donate){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-googleplay: Google Play](https://addy.io/faq/#is-there-an-android-app)
- [:simple-appstore: App Store](https://addy.io/faq/#is-there-an-ios-app)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/addy_io)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/iadbdpnoknmbdeolbapdackdcogdmjpe)

</details>

</div>

Le nombre d'alias partagés (qui finissent par un nom de domaine partagé comme `@addy.io `) que vous pouvez créer dépend de [l'abonnement](https://addy.io/#pricing) que vous choisissez. Vous pouvez payer en [cryptomonnaie](https://addy.io/help/subscribing-with-cryptocurrency) ou via une carte cadeau achetée chez [ProxyStore](https://addy.io/help/voucher-codes), le revendeur officiel d'Addy.io.

Vous pouvez créer un nombre illimité d'alias finissant par un domaine comme `@[nom d'utilisateur].addy.io ` ou un nom de domaine personnalisé avec les abonnements payants. Toutefois, comme indiqué précédemment, cela peut nuire à la protection de la vie privée, car les gens peuvent facilement relier vos alias standard en se basant uniquement sur le nom de domaine. Ils sont utiles lorsqu'un domaine partagé peut être bloqué par un service.

Securitum a [audité](https://addy.io/blog/addy-io-passes-independent-security-audit) Addy.io en septembre 2023 et n'a [trouvé](https://addy.io/addy-io-security-audit.pdf) aucune faille significative.

Fonctionnalités gratuites notables :

- [x] 10 Alias partagés
- [x] Alias standard illimités
- [ ] Pas de réponses sortantes
- [x] 1 boîte aux lettres pour les destinataires
- [x] Chiffrement PGP automatique[^1]

Après l'avoir résilié, les avantages de votre abonnement restent valables jusqu'à la fin du cycle de facturation. Passé ce délai, la majorité des fonctionnalités payantes (y compris les noms de domaines personnalisés) seront [désactivées](https://addy.io/faq/#what-happens-if-i-have-a-subscription-but-then-cancel-it), les paramètres payants du compte seront réinitialisés et la fonction fourre tout se réactivera si elle était précedemment désactivée.

### SimpleLogin

<div class="admonition recommendation" markdown>

![Logo de SimpleLogin](assets/img/email-aliasing/simplelogin.svg){ align=right }

**SimpleLogin** est un service gratuit qui fournit des alias de courrier électronique sur une variété de noms de domaine partagés, et offre en option des fonctions payantes comme des alias illimités et des domaines personnalisés.

[:octicons-home-16: Page d'Accueil](https://simplelogin.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplelogin.io/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://simplelogin.io/docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/simple-login){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
- [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/simplelogin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/diacfpipniklenphgljfkmhinphjlfff)
- [:simple-safari: Safari](https://apps.apple.com/app/id6475835429)

</details>

</div>

SimpleLogin a été [racheté par Proton AG] (https://proton.me/news/proton-and-simplelogin-join-forces) le 8 avril 2022. Si vous utilisez Proton Mail pour votre boîte mail principale, SimpleLogin est un excellent choix. Les deux produits étant désormais détenus par la même société, vous ne devez plus faire confiance qu'à une seule entité. Nous supposons également que SimpleLogin sera plus étroitement intégré aux offres de Proton à l'avenir. SimpleLogin continue de prendre en charge la redirection vers le fournisseur d'e-mail de votre choix.

Vous pouvez lier votre compte SimpleLogin dans les paramètres avec votre compte Proton. SimpleLogin est gratuit pour tous les utilisateurs de Proton Pass Plus, Proton Unlimited, ou tout autre abonnement Proton multi utilisateur. Vous pouvez également acheter une bon pour SimpleLogin Premium de façon anonyme via leur fournisseur officiel [ProxyStore](https://simplelogin.io/faq).

Securitum a [audité](https://simplelogin.io/blog/security-audit) SimpleLogin au début de 2022 et tous les problèmes [ont été résolus](https://simplelogin.io/audit2022/web.pdf).

Fonctionnalités gratuites notables :

- [x] 10 Alias partagés
- [x] Réponses illimitées
- [x] 1 boîte aux lettres pour les destinataires
- [ ] Le chiffrement PGP automatique [^1] est disponible uniquement sur les versions payantes

Tous les alias que vous avez créé restent fonctionnels après l'annulation de votre abonnement. Cependant, vous ne pourrez plus créer de nouveaux alias tant que le nombre d'alias excède la limite fixée par la version gratuite, vous ne pourrez pas non plus ajouter un nouveau nom de domaine, dossier ou boite mail.

## Critères

\*\*En plus de [nos critères standards] (about/criteria.md), nous évaluons les fournisseurs d'alias d'email selon les mêmes critères que nos [critères pour les fournisseurs d'email] (email.md#criteria), le cas échéant. Nous vous conseillons de prendre connaissance de l'intégralité de cette liste avant de choisir un fournisseur, et d'effectuer vos propres recherches afin de vous assurer de faire le choix qui vous correspond.

[^1]: Le chiffrement PGP automatique vous permet de chiffrer les mails entrants non chiffrés avant qu'ils ne soient transmis à votre boite mail, afin de vous assurer que votre fournisseur de boite mail n'ai jamais accès au contenu de vos emails.
