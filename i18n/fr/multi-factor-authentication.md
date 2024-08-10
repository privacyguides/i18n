---
title: "Authentification multi-facteurs"
icon: 'material/two-factor-authentication'
description: These tools assist you with securing your internet accounts with Multi-Factor Authentication without sending your secrets to a third-party.
cover: multi-factor-authentication.webp
---

<small>Protects against the following threat(s):</small>

- [:material-target-account: Attaques ciblées](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition note" markdown>
<p class="admonition-title">Hardware Keys</p>

[Hardware security key recommendations](security-keys.md) have been moved to their own category.

</div>

**Multi-Factor Authentication Apps** implement a security standard adopted by the Internet Engineering Task Force (IETF) called **Time-based One-time Passwords**, or **TOTP**. Il s'agit d'une méthode par laquelle les sites web partagent avec vous un secret qui est utilisé par votre application d'authentification pour générer un code à six chiffres (généralement) basé sur l'heure actuelle, que vous saisissez lorsque vous vous connectez pour que le site web puisse le vérifier. En général, ces codes sont régénérés toutes les 30 secondes, et dès qu'un nouveau code est généré, l'ancien devient inutile. Même si un pirate obtient un code à six chiffres, il n'a aucun moyen d'inverser ce code pour obtenir le secret original, ni de prédire quels seront les codes futurs.

Nous vous recommandons vivement d'utiliser des applications TOTP mobiles plutôt que des alternatives de bureau, car Android et IOS offrent une meilleure sécurité et une meilleure isolation des applications que la plupart des systèmes d'exploitation de bureau.

## Ente Auth

<div class="admonition recommendation" markdown>

![Ente Auth logo](assets/img/multi-factor-authentication/ente-auth.svg){ align=right }

**Ente Auth** is a free and open-source app which stores and generates TOTP tokens. Elle peut être utilisée avec un compte en ligne pour sauvegarder et synchroniser vos jetons sur tous vos appareils (et y accéder via une interface web) de manière sécurisée et chiffrée de bout en bout. Elle peut également être utilisée hors ligne sur un seul appareil, sans qu'aucun compte ne soit nécessaire.

[:octicons-home-16: Homepage](https://ente.io/auth){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.ente.io/auth){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ente-io/ente/tree/main/auth#readme){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6444121398)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=auth)
- [:octicons-globe-16: Web](https://auth.ente.io)

</details>

</div>

## Aegis Authenticator (Android)

<div class="admonition recommendation" markdown>

![Logo Aegis](assets/img/multi-factor-authentication/aegis.png){ align=right }

**Aegis Authenticator** est une application gratuite et open-source pour Android qui permet de gérer vos jetons de vérification en 2 étapes pour vos services en ligne. Aegis Authenticator fonctionne complètement hors ligne/localement, mais inclut l'option d'exporter vos jetons pour les sauvegarder, contrairement à de nombreuses alternatives.

[:octicons-home-16: Homepage](https://getaegis.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="Source Code" }
[:octicons-heart-16:](https://buymeacoffee.com/beemdevelopment){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
- [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

</details>

</div>

<!-- markdownlint-disable-next-line -->
## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

- Le code source doit être accessible au public.
- Ne doit pas nécessiter de connexion à internet.
- Cloud syncing must be optional, and (if available) sync functionality must be E2EE.
