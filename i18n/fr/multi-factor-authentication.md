---
title: L'authentification multifactorielle
icon: material/two-factor-authentication
description: Sécurisez vos comptes en ligne avec ces outils d'authentification multifactorielle sans compromettre votre vie privée.
cover: multi-factor-authentication.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-target-account: Attaques ciblées](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition note" markdown>
<p class="admonition-title">Clefs de sécurité matérielle (hardware keys)</p>

Nos recommandations de clefs de sécurité matérielle sont désormais trouvables [ici](security-keys.md).

</div>

**Les applications d'authentification multifactorielle** permettent d'utiliser les **Mots de passe temporaires à usage unique (Time-based One-time Passwaords)**, ou **TOTP**, un standard de sécurité adopté par l'Internet Engineering Task Force (IETF). Il s'agit d'une méthode par laquelle les sites web partagent avec vous un secret qui est utilisé par votre application d'authentification pour générer un code à six chiffres (généralement) basé sur l'heure actuelle, que vous saisissez lorsque vous vous connectez pour que le site web puisse le vérifier. Généralement, ces codes sont générés toutes les 30 secondes, et deviennent obsolètes dès qu'un nouveau code est généré. Même si un pirate obtient un code à six chiffres, il n'a aucun moyen d'inverser ce code pour obtenir le secret original, ni de prédire quels seront les codes futurs.

Nous vous recommandons vivement d'utiliser des applications TOTP mobiles plutôt que des alternatives de bureau, car Android et IOS offrent une meilleure sécurité et une meilleure isolation des applications que la plupart des systèmes d'exploitation de bureau.

## Ente Auth

<div class="admonition recommendation" markdown>

![Logo de Ente Auth](assets/img/multi-factor-authentication/ente-auth.svg){ align=right }

**Ente Auth** est une application libre et open-source qui stocke et génère des jetons (token) TOTP. Elle peut être utilisée avec un compte en ligne pour sauvegarder et synchroniser vos jetons entre vos appareils (et y accéder depuis une interface web) de façon sécurisée grâce au chiffrement de bout-en-bout. Elle peut également être utilisée hors ligne sur un seul appareil, sans qu'aucun compte ne soit nécessaire.

[:octicons-home-16: Page d'Accueil](https://ente.io/auth){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://help.ente.io/auth){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ente-io/ente/tree/main/auth#readme){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6444121398)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=auth)
- [:octicons-browser-16: Web](https://auth.ente.io)

</details>

</div>

Le code source côté serveur et l'infrastructure qui sous-tendent Ente Auth (lorsqu'il est utilisé avec un compte en ligne) ont été audité par [Cure53](https://ente.io/blog/cern-audit) en octobre 2025.

## Aegis Authenticator (Android)

<div class="admonition recommendation" markdown>

![Logo de Aegis](assets/img/multi-factor-authentication/aegis.png){ align=right }

**Aegis Authenticator** est une application libre et open-source pour Android qui permet de gérer vos jetons de vérification en 2 étapes pour vos services en ligne. Aegis Authenticator fonctionne complètement hors ligne/localement, mais inclut l'option d'exporter vos jetons pour les sauvegarder, contrairement à de nombreuses alternatives.

[:octicons-home-16: Page d'Accueil](https://getaegis.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="Code Source" }
[:octicons-heart-16:](https://buymeacoffee.com/beemdevelopment){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
- [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

</details>

</div>

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de faire votre choix, et de mener vos propres recherches pour vous assurer que ce choix correspond à vos besoins.

- Le code source doit être accessible au public.
- Ne dois pas nécessiter de connexion à internet.
- La synchronisation cloud doit être optionnelle ; lorsqu'elle est proposée, la synchronisation doit être chiffrée de bout en bout.
