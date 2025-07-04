---
meta_title: "Les meilleurs gestionnaires de mots de passe pour protéger votre vie privée et votre sécurité - Privacy Guides"
title: "Gestionnaires de mots de passe"
icon: material/form-textbox-password
description: Les gestionnaires de mots de passe vous permettent de stocker et gérer en toute sécurité vos mots de passe et autres identifiants.
cover: passwords.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Recommandations de gestionnaires de mots de passe
    url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Bitwarden
    image: /assets/img/password-management/bitwarden.svg
    url: https://bitwarden.com
    sameAs: https://fr.wikipedia.org/wiki/Bitwarden
    applicationCategory: Gestionnaire de mots de passe
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: 1Password
    image: /assets/img/password-management/1password.svg
    url: https://1password.com/fr
    sameAs: https://fr.wikipedia.org/wiki/1Password
    applicationCategory: Gestionnaire de mots de passe
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Proton Pass
    image: /assets/img/password-management/protonpass.svg
    url: https://proton.me/pass
    applicationCategory: Gestionnaire de mots de passe
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Psono
    image: /assets/img/password-management/psono.svg
    url: https://psono.com
    applicationCategory: Gestionnaire de mots de passe
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: KeePassXC
    image: /assets/img/password-management/keepassxc.svg
    url: https://keepassxc.org
    sameAs: https://fr.wikipedia.org/wiki/KeePassXC
    applicationCategory: Gestionnaire de mots de passe
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: KeePassDX
    image: /assets/img/password-management/keepassdx.svg
    url: https://keepassdx.com
    applicationCategory: Gestionnaire de mots de passe
    operatingSystem: Android
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Gopass
    image: /assets/img/password-management/gopass.svg
    url: https://gopass.pw
    applicationCategory: Gestionnaire de mots de passe
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - FreeBSD
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
---

<small>Protects against the following threat(s):</small>

- [:material-target-account: Attaques ciblées](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: Attaques passives](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Fournisseurs de service](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Les **gestionnaires de mots de passe** vous permettent de stocker et de gérer en toute sécurité des mots de passe et autres identifiants à l'aide d'un mot de passe maître.

[Introduction aux mots de passe :material-arrow-right-drop-circle:](basics/passwords-overview.md)

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

Les gestionnaires de mots de passe intégrés dans des logiciels tels que les navigateurs et les systèmes d'exploitation ne sont parfois pas aussi performants que les logiciels de gestion de mots de passe dédiés. The advantage of a built-in password manager is good integration with the software, but it can often be very simple and lack privacy and security features that standalone offerings have.

For example, the password manager in Microsoft Edge doesn't offer end-to-end encryption at all. Le gestionnaire de mots de passe de Google a un chiffrement de bout en bout [optionnel](https://support.google.com/accounts/answer/11350823?hl=fr), et [celui d'Apple](https://support.apple.com/fr-fr/102651) le propose par défaut.

</div>

## Basé sur le cloud

Ces gestionnaires de mots de passe synchronisent vos mots de passe sur un serveur cloud pour un accès facile à partir de tous vos appareils et une sécurité contre la perte d'appareils.

### Bitwarden

<div class="admonition recommendation" markdown>

![Logo de Bitwarden](assets/img/password-management/bitwarden.svg){ align=right }

**Bitwarden** est un gestionnaire de mots de passe et de clés de passe gratuit et open-source. Il vise à résoudre les problèmes de gestion des mots de passe pour les individus, les équipes et les organisations commerciales. Bitwarden est l'une des solutions les plus simples et les plus sûres pour stocker tous vos identifiants et mots de passe tout en les synchronisant de manière pratique entre tous vos appareils.

[:octicons-home-16: Homepage](https://bitwarden.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://bitwarden.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://bitwarden.com/help){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/bitwarden){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.x8bit.bitwarden)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1137397744)
- [:simple-github: GitHub](https://github.com/bitwarden/android/releases)
- [:fontawesome-brands-windows: Windows](https://bitwarden.com/download)
- [:simple-apple: macOS](https://bitwarden.com/download)
- [:simple-linux: Linux](https://bitwarden.com/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/com.bitwarden.desktop)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/bitwarden-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/nngceckbapebfimnlniiiahkandclblb)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/jbkfoedolllekgbhcbcoahefnbanhhlh)
- [:simple-safari: Safari](https://apps.apple.com/app/id1352778147)

</details>

</div>

Bitwarden uses [PBKDF2](https://bitwarden.com/help/kdf-algorithms/#pbkdf2) as its key derivation function (KDF) algorithm by default. It also offers [Argon2](https://bitwarden.com/help/kdf-algorithms/#argon2id), which is more secure, as an alternative. You can change your account's KDF algorithm in the web vault:

- [x] Select **Settings > Security > Keys > KDF algorithm > Argon2id**

Le code côté serveur de Bitwarden est [open source](https://github.com/bitwarden/server), donc si vous ne voulez pas utiliser le cloud Bitwarden, vous pouvez facilement héberger votre propre serveur de synchronisation Bitwarden.

**Vaultwarden** is an alternative implementation of Bitwarden's sync server written in Rust and compatible with official Bitwarden clients, perfect for self-hosted deployment where running the resource-heavy official service might not be ideal. Si vous cherchez à héberger Bitwarden sur votre propre serveur, vous voudrez certainement utiliser Vaultwarden plutôt que le code serveur officiel de Bitwarden.

[:octicons-repo-16: Vaultwarden Repository](https://github.com/dani-garcia/vaultwarden ""){.md-button} [:octicons-info-16:](https://github.com/dani-garcia/vaultwarden/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/dani-garcia/vaultwarden){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/dani-garcia){ .card-link title="Contribute" }

### Proton Pass

<div class="admonition recommendation" markdown>

![Proton Pass logo](assets/img/password-management/protonpass.svg){ align=right }

**Proton Pass** is an open-source, end-to-end encrypted password manager developed by Proton, the team behind [Proton Mail](email.md#proton-mail). It securely stores your login credentials, generates unique email aliases, and supports and stores passkeys.

[:octicons-home-16: Homepage](https://proton.me/pass){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/pass/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/pass){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/protonpass){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=proton.android.pass)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6443490629)
- [:fontawesome-brands-windows: Windows](https://proton.me/pass/download)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/proton-pass)
- [:simple-googlechrome: Chrome](https://chromewebstore.google.com/detail/ghmbeldphafepmbegfdlkpapadhbakde)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/gcllgfdnfnllodcaambdaknbipemelie)
- [:octicons-browser-16: Web](https://pass.proton.me)

</details>

</div>

With the acquisition of SimpleLogin in April 2022, Proton has offered a "hide-my-email" feature that lets you create 10 aliases (free plan) or unlimited aliases (paid plans).

The Proton Pass mobile apps and browser extension underwent an audit performed by Cure53 throughout May and June 2023. The security analysis company concluded:

> Proton Pass apps and components leave a rather positive impression in terms of security.

All issues were addressed and fixed shortly after the [report](https://res.cloudinary.com/dbulfrlrz/images/v1707561557/wp-pme/Cure53-proton-pass-20230717/Cure53-proton-pass-20230717.pdf).

### 1Password

<div class="admonition recommendation" markdown>

![1Password logo](assets/img/password-management/1password.svg){ align=right }

**1Password** is a password manager with a strong focus on security and ease-of-use that allows you to store passwords, passkeys, credit cards, software licenses, and any other sensitive information in a secure digital vault. Your vault is hosted on 1Password's servers for a [monthly fee](https://1password.com/sign-up).

1Password is [audited](https://support.1password.com/security-assessments) on a regular basis and provides exceptional customer support. 1Password est closed source ; cependant, la sécurité du produit est documentée de manière approfondie dans leur [livre blanc sur la sécurité](https://1passwordstatic.com/files/security/1password-white-paper.pdf).

[:octicons-home-16: Homepage](https://1password.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://1password.com/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.1password.com){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onepassword.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1511601750)
- [:fontawesome-brands-windows: Windows](https://1password.com/downloads/windows)
- [:simple-apple: macOS](https://1password.com/downloads/mac)
- [:simple-linux: Linux](https://1password.com/downloads/linux)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/1password-x-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/aeblfdkhhhdcdjpifhhbdiojplfjncoa)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/dppgmdbiimibapkepcbdbmkaabgiofem)
- [:simple-safari: Safari](https://apps.apple.com/app/id1569813296)
- [:octicons-browser-16: Web](https://my.1password.com/signin)

</details>

</div>

Traditionnellement, 1Password offrait une meilleure expérience utilisateur en matière de gestion de mots de passe pour les personnes utilisant macOS et iOS ; cependant, il propose désormais les mêmes fonctionnalités sur toutes les plateformes. Les clients 1Password disposent de nombreuses fonctionnalités destinées aux familles et aux personnes moins techniques comme une interface utilisateur intuitive pour faciliter l'utilisation et la navigation, ainsi que des fonctionnalités avancées. Notamment, presque toutes les fonctionnalités de 1Password sont disponibles dans ses clients de bureau ou mobiles natifs.

Votre coffre-fort 1Password est sécurisé à la fois par votre mot de passe principal et par une clé de sécurité aléatoire de 34 caractères pour chiffrer vos données sur leurs serveurs. Cette clé de sécurité ajoute une couche de protection à vos données, car celles-ci sont sécurisées par une entropie élevée, indépendamment de votre mot de passe principal. De nombreuses autres solutions de gestion des mots de passe dépendent entièrement de la force de votre mot de passe principal pour sécuriser vos données.

### Psono

<div class="admonition recommendation" markdown>

![Logo Psono](assets/img/password-management/psono.svg){ align=right }

**Psono** est un gestionnaire de mots de passe gratuit et open source d'Allemagne, avec un accent sur la gestion des mots de passe pour les équipes. Il peut être [auto-hébergé](#password-management-servers). Psono prend en charge le partage sécurisé de mots de passe, de fichiers, de signets et d'e-mails.

[:octicons-home-16: Page d'accueil](https://psono.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://psono.com/privacy-policy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://doc.psono.com){ .card-link title="Documentation"}
[:octicons-code-16:](https://gitlab.com/psono){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.psono.psono)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1545581224)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/psono-pw-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/eljmjmgjkbmpmfljlmklcfineebidmlo)
- [:simple-docker: Docker Hub](https://hub.docker.com/r/psono/psono-client)

</details>

</div>

Psono fournit une documentation complète pour son produit. Le client web de Psono peut être hébergé par vous-même ; vous pouvez également choisir l'édition Community complète ou l'édition Enterprise avec des fonctionnalités supplémentaires.

En avril 2024, Psono a ajouté la [prise en charge des passkeys](https://psono.com/blog/psono-introduces-passkeys) pour l'extension navigateur uniquement.

### Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

#### Exigences minimales

- Doit utiliser un système E2EE solide, basé sur des normes et moderne.
- Doit avoir des pratiques de chiffrement et de sécurité soigneusement documentées.
- Doit disposer d'un audit publié par une tierce partie indépendante et réputée.
- Toute télémétrie non essentielle doit être facultative.
- Ne doit pas collecter plus de DPI que nécessaire à des fins de facturation.

#### Dans le meilleur des cas

Nos critères de cas idéal représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de cette fonctionnalité, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- La télémétrie devrait être optionnelle (désactivée par défaut) ou ne pas être collectée du tout.
- Devrait être open source et raisonnablement auto-hébergeable.

## Stockage local

Ces options vous permettent de gérer une base de données de mots de passe chiffrés localement.

### KeePassXC

<div class="admonition recommendation" markdown>

![Logo KeePassXC](assets/img/password-management/keepassxc.svg){ align=right }

**KeePassXC** est un fork communautaire de KeePassX, un portage natif multiplateforme de KeePass Password Safe, dans le but de l'étendre et de l'améliorer avec de nouvelles fonctionnalités et des corrections de bugs afin de fournir un gestionnaire de mots de passe open-source riche en fonctionnalités, multiplateforme et moderne.

[:octicons-home-16: Page d'accueil](https://keepassxc.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://keepassxc.org/privacy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://keepassxc.org/docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/keepassxreboot/keepassxc){ .card-link title="Code source" }
[:octicons-heart-16:](https://keepassxc.org/donate){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

    - [:fontawesome-brands-windows: Windows](https://keepassxc.org/download/#windows)
    - [:simple-apple: macOS](https://keepassxc.org/download/#mac)
    - [:simple-linux: Linux](https://keepassxc.org/download/#linux)
    - [:simple-flathub: Flatpak](https://flathub.org/apps/details/org.keepassxc.KeePassXC)
    - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/keepassxc-browser)
    - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/oboonakemofpalcgghocfoadofidjkkk)

</details>

</div>

KeePassXC stocke ses données d'exportation sous forme de fichiers [CSV](https://en.wikipedia.org/wiki/Comma-separated_values). Vous pourriez perdre des données si vous importez ce fichier dans un autre gestionnaire de mots de passe. Nous vous conseillons de vérifier chaque entrée manuellement.

### KeePassDX (Android)

<div class="admonition recommendation" markdown>

![Logo KeePassDX](assets/img/password-management/keepassdx.svg){ align=right }

**KeePassDX** est un gestionnaire de mots de passe léger pour Android ; il permet de modifier des données chiffrées dans un seul fichier au format KeePass et de remplir les formulaires de manière sécurisée.

[:octicons-home-16: Page d'accueil](https://keepassdx.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Kunzisoft/KeePassDX/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/Kunzisoft/KeePassDX){ .card-link title="Code source" }
[:octicons-heart-16:](https://keepassdx.com/#donation){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.free)
- [:simple-github: GitHub](https://github.com/Kunzisoft/KeePassDX/releases)

</details>

</div>

La [version pro](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.pro) de l'application permet de débloquer du contenu cosmétique et des fonctions de protocole non standard, mais surtout, elle aide et encourage le développement.

### Gopass (CLI)

<div class="admonition recommendation" markdown>

![Logo Gopass](assets/img/password-management/gopass.svg){ align=right }

**Gopass** est un gestionnaire de mot de passe minimal pour la ligne de commande écrit en Go. Il peut être utilisé dans les applications de scripting et fonctionne sur tous les principaux systèmes d'exploitation de bureau et de serveur.

[:octicons-home-16: Homepage](https://gopass.pw){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/gopasspw/gopass/tree/master/docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/gopasspw/gopass){ .card-link title="Code source" }
[:octicons-heart-16:](https://github.com/sponsors/dominikschulz){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:fontawesome-brands-windows: Windows](https://gopass.pw/#install-windows)
- [:simple-apple: macOS](https://gopass.pw/#install-macos)
- [:simple-linux: Linux](https://gopass.pw/#install-linux)
- [:simple-freebsd: FreeBSD](https://gopass.pw/#install-bsd)

</details>

</div>

### Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

- Doit être multiplateforme.
