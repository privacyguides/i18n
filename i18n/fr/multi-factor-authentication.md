---
title: "Multi-Factor Authenticators"
icon: 'material/two-factor-authentication'
description: These tools assist you with securing your internet accounts with Multi-Factor Authentication without sending your secrets to a third-party.
cover: multi-factor-authentication.webp
---

## Clés de sécurité matérielles

### YubiKey

<div class="admonition recommendation" markdown>

![YubiKeys](assets/img/multi-factor-authentication/yubikey.png)

Les **YubiKeys** font partie des clés de sécurité les plus populaires. Some YubiKey models have a wide range of features such as: [Universal 2nd Factor (U2F)](https://en.wikipedia.org/wiki/Universal_2nd_Factor), [FIDO2 and WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), [Yubico OTP](basics/multi-factor-authentication.md#yubico-otp), [Personal Identity Verification (PIV)](https://developers.yubico.com/PIV), [OpenPGP](https://developers.yubico.com/PGP), [TOTP and HOTP](https://developers.yubico.com/OATH) authentication.

L'un des avantages de la YubiKey est qu'une seule clé peut faire presque tout (YubiKey 5) ce que vous pouvez attendre d'une clé de sécurité matérielle. We do encourage you to take the [quiz](https://yubico.com/quiz) before purchasing in order to make sure you make the right choice.

[:octicons-home-16: Homepage](https://yubico.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title=Documentation}

</details>

</div>

The [comparison table](https://yubico.com/store/compare) shows the features and how the YubiKeys compare. Nous vous recommandons vivement de choisir des clés de la série YubiKey 5.

YubiKeys can be programmed using the [YubiKey Manager](https://yubico.com/support/download/yubikey-manager) or [YubiKey Personalization Tools](https://yubico.com/support/download/yubikey-personalization-tools). For managing TOTP codes, you can use the [Yubico Authenticator](https://yubico.com/products/yubico-authenticator). Tous les clients de Yubico sont open source.

Pour les modèles qui supportent HOTP et TOTP, il y a 2 emplacements dans l'interface OTP qui peuvent être utilisés pour HOTP et 32 emplacements pour stocker les secrets TOTP. Ces secrets sont stockés et chiffrés sur la clé et ne sont jamais exposés aux appareils sur lesquels elle est branchée. Une fois qu'une graine (secret partagé) est donnée à l'authentificateur Yubico, celui-ci ne donnera que les codes à six chiffres, mais jamais la graine. Ce modèle de sécurité permet de limiter ce qu'un attaquant peut faire s'il compromet l'un des appareils exécutant le Yubico Authenticator et rend la YubiKey résistante à un attaquant physique.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

The firmware of YubiKey is not open source and is not updatable. Si vous souhaitez obtenir des fonctionnalités dans des versions plus récentes du firmware, ou si la version du firmware que vous utilisez présente une vulnérabilité, vous devrez acheter une nouvelle clé.

</div>

### Nitrokey

<div class="admonition recommendation" markdown>

![Nitrokey](assets/img/multi-factor-authentication/nitrokey.jpg){ align=right }

**Nitrokey** possède une clé de sécurité qui prend en charge [FIDO2 et WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) appelée la **Nitrokey FIDO2**. Pour la prise en charge de PGP, vous devez acheter l'une de leurs autres clés comme la **Nitrokey Start**, la **Nitrokey Pro 2** ou la **Nitrokey Storage 2**.

[:octicons-home-16: Homepage](https://nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nitrokey.com/data-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.nitrokey.com){ .card-link title=Documentation}

</details>

</div>

The [comparison table](https://nitrokey.com/#comparison) shows the features and how the Nitrokey models compare. La **Nitrokey 3** répertoriée aura un ensemble de fonctionnalités combinées.

Nitrokey models can be configured using the [Nitrokey app](https://nitrokey.com/download).

Pour les modèles qui supportent HOTP et TOTP, il y a 3 emplacements pour HOTP et 15 pour TOTP. Certaines Nitrokeys peuvent faire office de gestionnaire de mots de passe. Ils peuvent stocker 16 identifiants différents et les chiffrer en utilisant le même mot de passe que l'interface OpenPGP.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Bien que les Nitrokeys ne divulguent pas les secrets HOTP/TOTP à l'appareil auquel ils sont connectés, le stockage HOTP et TOTP n'est **pas** chiffré et est vulnérable aux attaques physiques. Si vous cherchez à stocker des secrets HOTP ou TOTP, nous vous recommandons vivement d'utiliser plutôt un YubiKey.

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

La réinitialisation de l'interface OpenPGP sur une Nitrokey rendra également la base de données des mots de passe [inaccessible](https://docs.nitrokey.com/pro/factory-reset.html).

</div>

The Nitrokey Pro 2, Nitrokey Storage 2, and the upcoming Nitrokey 3 supports system integrity verification for laptops with the [Coreboot](https://coreboot.org) + [Heads](https://osresearch.net) firmware.

Le micrologiciel de la Nitrokey est open source, contrairement à la YubiKey. Le micrologiciel des modèles NitroKey modernes (à l'exception de la **NitroKey Pro 2**) peut être mis à jour.

### Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

#### Exigences minimales

- Doit utiliser des modules de sécurité matériels de haute qualité et resistant aux attaques physiques.
- Doit prendre en charge la dernière spécification FIDO2.
- Ne doit pas permettre l'extraction de la clé privée.
- Les appareils qui coûtent plus de 35 $ doivent prendre en charge la gestion d'OpenPGP et de S/MIME.

#### Dans le meilleur des cas

Nos critères de cas idéal représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de cette fonctionnalité, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Devrait être disponible en format USB-C.
- Devrait être disponible avec NFC.
- Devrait prendre en charge le stockage de secrets de TOTP.
- Devrait prendre en charge les mises à jour sécurisées du micrologiciel.

## Applications d'authentification

Les applications d'authentification implémentent une norme de sécurité adoptée par l'Internet Engineering Task Force (IETF) appelée **Mots de Passe à Usage Unique Basé sur le Temps**, ou **Time based One Time Password (TOTP)**. Il s'agit d'une méthode par laquelle les sites web partagent avec vous un secret qui est utilisé par votre application d'authentification pour générer un code à six chiffres (généralement) basé sur l'heure actuelle, que vous saisissez lorsque vous vous connectez pour que le site web puisse le vérifier. En général, ces codes sont régénérés toutes les 30 secondes, et dès qu'un nouveau code est généré, l'ancien devient inutile. Même si un pirate obtient un code à six chiffres, il n'a aucun moyen d'inverser ce code pour obtenir le secret original, ni de prédire quels seront les codes futurs.

Nous vous recommandons vivement d'utiliser des applications TOTP mobiles plutôt que des alternatives de bureau, car Android et IOS offrent une meilleure sécurité et une meilleure isolation des applications que la plupart des systèmes d'exploitation de bureau.

### ente Auth

<div class="admonition recommendation" markdown>

![ente Auth logo](assets/img/multi-factor-authentication/ente-auth.png){ align=right }

**ente Auth** is a free and open-source app which stores and generates TOTP tokens. Elle peut être utilisée avec un compte en ligne pour sauvegarder et synchroniser vos jetons sur tous vos appareils (et y accéder via une interface web) de manière sécurisée et chiffrée de bout en bout. Elle peut également être utilisée hors ligne sur un seul appareil, sans qu'aucun compte ne soit nécessaire.

[:octicons-home-16: Homepage](https://ente.io/auth){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://github.com/ente-io/auth){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6444121398)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=auth)
- [:octicons-globe-16: Web](https://auth.ente.io)

</details>

</div>

### Aegis Authenticator (Android)

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
### Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

- Le code source doit être accessible au public.
- Ne doit pas nécessiter de connexion à internet.
- Ne doit pas se synchroniser avec un service tiers de synchronisation/sauvegarde cloud.
    - La prise en charge **facultative** de la synchronisation E2EE avec des outils natifs du système d'exploitation est acceptable, par exemple la synchronisation chiffrée via iCloud.
