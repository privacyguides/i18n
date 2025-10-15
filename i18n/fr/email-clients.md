---
title: "Clients e-mails"
icon: material/email-open
description: Ces clients d'e-mail respectent la vie privée et prennent en charge le chiffrement OpenPGP.
cover: email-clients.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-server-network: Fournisseurs de service](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-target-account: Attaques ciblées](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Les **clients de messagerie** que nous recommandons prennent en charge à la fois [OpenPGP](encryption.md#openpgp) et des méthodes d'authentification sécurisées telle que [Open Authorization(OAuth)](basics/account-creation.md#sign-in-with-oauth). OAuth vous permet d'utiliser [l'authentification multifactorielle](basics/multi-factor-authentication.md) pour vous prémunir contre le vol de compte.

<details class="warning" markdown>
<summary>Un mail ne garantit pas de confidentialité persistante</summary>

Même en utilisant une technologie de chiffrement de bout-en-bout (E2EE) comme OpenPGP, [certaines métadonnées](basics/email-security.md#email-metadata-overview) contenues dans l'en-tête des emails ne seront pas chiffrées.

OpenPGP ne prend pas non plus en charge la [confidentialité persistante](https://en.wikipedia.org/wiki/Forward_secrecy), ce qui signifie que si votre clé privée ou celle du destinataire est volée, tous les messages précédents chiffrés avec cette clé seront exposés : [comment protéger mes clés privées ?](basics/email-security.md) Envisagez d'utiliser un support qui assure la confidentialité persistante :

[Communication en temps réel](real-time-communication.md ""){.md-button}

</details>

## Multi-plateformes

### Thunderbird

<div class="admonition recommendation" markdown>

![Logo Thunderbird](assets/img/email-clients/thunderbird.svg){ align=right }

**Thunderbird** est un client d'e-mail, de groupes de discussion, de flux d'informations et de chat (XMPP, IRC, Matrix) gratuit, open-source et multiplateforme, développé par la communauté Thunderbird, et précédemment par la Fondation Mozilla.

[:octicons-home-16: Page d'Accueil](https://thunderbird.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/thunderbird){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://support.mozilla.org/products/thunderbird){ .card-link title="Documentation" }
[:octicons-code-16:](https://hg.mozilla.org/comm-central){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.thunderbird.android)
- [:simple-github: GitHub](https://github.com/thunderbird/thunderbird-android/releases)
- [:fontawesome-brands-windows: Windows](https://thunderbird.net)
- [:simple-apple: macOS](https://thunderbird.net)
- [:simple-linux: Linux](https://thunderbird.net)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.Thunderbird)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

En répondant à quelqu'un sur une liste mail sur l'application mobile de Thunderbird, l'option "répondre" peut inclure la liste mail. Pour plus d'informations, consultez [thunderbird/thunderbird-android #3738](https://github.com/thunderbird/thunderbird-android/issues/3738).

</div>

#### Configuration recommandée

<div class="annotate" markdown>

Nous vous conseillons de changer certains paramètres pour rendre Thunderbird Desktop un peu plus privé.

Ces options se trouvent dans :material-menu: → **Règlages** → **Confidentialité et Sécurité**.

##### Contenu Web

- [ ] Décocher  **Se souvenir des sites et des liens consultés**
- [ ] Décocher  **Accepter les cookies des sites** (1)

</div>

1. Vous aurrez peut être besoin de garder ces paramètres activés si vous ajoutez certains fournisseurs comme Gmail, ou via le SSO d'une institution. Vous pouvez les désactiver après vous être connecté.

##### Télémétrie

- [ ] Décocher **Autoriser Thunderbird à envoyer des données techniques et d'interractions à Mozilla**

#### Thunderbird-user.js (avancé)

[`thunderbird-user.js`](https://github.com/HorlogeSkynet/thunderbird-user.js) est un ensemble d'options de configuration destiné à désactiver autant de fonctions de navigation web que possible afin de réduire les possibilités d'attaques et de préserver la confidentialité. Certains changements sont retroportés depuis le [projet Arkenfox](desktop-browsers.md#arkenfox-advanced).

## Spécifique à une plateforme

### Apple Mail (macOS)

<div class="admonition recommendation" markdown>

![Logo de Apple Mail](assets/img/email-clients/applemail.png){ align=right }

**Apple Mail** est installé par défaut sur macOS et peut être configuré pour prendre en charge OpenPGP avec [GPG Suite](encryption.md#gpg-suite), ce qui permet d'envoyer des mails chiffrés en PGP.

[:octicons-home-16: Page d'Accueil](https://support.apple.com/guide/mail/welcome/mac){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/en-ww){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://support.apple.com/mail){ .card-link title=Documentation}

</details>

</div>

<div class="admonition info" markdown>
<p class="admonition-title">Pour les personnes utilisant macOS Sonoma</p>

GPG Suite n'a [pas encore](https://gpgtools.com/sonoma) de version stable pour macOS Sonoma.

</div>

Apple Mail peut charger le contenu distant en arrière-plan ou le bloquer complètement ainsi que cacher votre adresse IP aux expéditeurs sur [macOS](https://support.apple.com/guide/mail/mlhl03be2866/mac) et [iOS](https://support.apple.com/guide/iphone/iphf084865c7/ios).

### FairEmail (Android)

<div class="admonition recommendation" markdown>

![Logo de FairEmail](assets/img/email-clients/fairemail.svg){ align=right }

**FairEmail** est une application de messagerie minimale et open-source qui utilise des standards libres (IMAP, SMTP, OpenPGP) et minimise la consommation de la batterie et des données mobiles.

[:octicons-home-16: Page d'Accueil](https://email.faircode.eu){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/M66B/FairEmail/blob/master/PRIVACY.md){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://github.com/M66B/FairEmail/blob/master/FAQ.md){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/M66B/FairEmail){ .card-link title="Code Source" }
[:octicons-heart-16:](https://email.faircode.eu/donate){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=eu.faircode.email)
- [:simple-github: GitHub](https://github.com/M66B/FairEmail/releases)

</details>

</div>

### GNOME Evolution (GNOME)

<div class="admonition recommendation" markdown>

![Logo de Evolution](assets/img/email-clients/evolution.svg){ align=right }

**Evolution** est un gestionnaire d'informations personnelles qui comprend une messagerie, un service de calendrier et un carnet d'adresse. Leur [documentation](https://help.gnome.org/users/evolution/stable) très complète vous permet de facilement configurer l'application.

[:octicons-home-16: Page d'Accueil](https://wiki.gnome.org/Apps/Evolution){ .md-button .md-button--primary }
[:octicons-eye-16:](https://wiki.gnome.org/Apps/Evolution/PrivacyPolicy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://help.gnome.org/users/evolution/stable){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.gnome.org/GNOME/evolution){ .card-link title="Code Source" }
[:octicons-heart-16:](https://gnome.org/donate){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.gnome.Evolution)

</details>

</div>

### Kontact (KDE)

<div class="admonition recommendation" markdown>

![Kontact logo](assets/img/email-clients/kontact.svg){ align=right }

**Kontact** est un gestionnaire d'information personnelle (PIM) issue du projet [KDE](https://kde.org). L'application comprend un client mail, un carnet d'adresse, un client RSS et un agenda.

[:octicons-home-16: Page d'Accueil](https://kontact.kde.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kde.org/privacypolicy-apps){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://kontact.kde.org/users){ .card-link title="Documentation" }
[:octicons-code-16:](https://invent.kde.org/pim/kmail){ .card-link title="Code Source" }
[:octicons-heart-16:](https://kde.org/community/donations){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-linux: Linux](https://kontact.kde.org/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.kde.kontact)

</details>

</div>

### Mailvelope (Navigateur)

<div class="admonition recommendation" markdown>

![Logo de Mailvelope](assets/img/email-clients/mailvelope.svg){ align=right }

**Mailvelope** est une extension de navigateur qui vous permet de chiffrer vos mails selon le standard de chiffrement OpenPGP.

[:octicons-home-16: Page d'Accueil](https://mailvelope.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailvelope.com/privacy-policy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://mailvelope.com/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mailvelope/mailvelope){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/mailvelope)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/mailvelope/kajibbejlbohfaggdiogboambcijhkke)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/mailvelope/dgcbddhdhjppfdfjpciagmmibadmoapc)

</details>

</div>

### NeoMutt (CLI)

<div class="admonition recommendation" markdown>

![Logo de NeoMutt](assets/img/email-clients/mutt.svg){ align=right }

**NeoMutt** est un lecteur de mail open-source pour Linux et BSD qui fonctionne directement par ligne de commande. C'est une fork de [Mutt](https://en.wikipedia.org/wiki/Mutt_(email_client)), avec des fonctionnalités additionnelles.

NeoMutt est un client textuel difficile à prendre en main. Il est cependant très personnalisable.

[:octicons-home-16: Page d'Accueil](https://neomutt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://neomutt.org/guide){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/neomutt/neomutt){ .card-link title="Code Source" }
[:octicons-heart-16:](https://paypal.com/paypalme/russon){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-apple: macOS](https://neomutt.org/distro)
- [:simple-linux: Linux](https://neomutt.org/distro)

</details>

</div>

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer de faire le bon choix.

### Qualifications minimales

- Les applications développées pour des systèmes d'exploitation open-source doivent elle-même être open-source.
- Ne dois pas collecter de données télémétriques, ou dois donner la possibilité de les désactiver facilement.
- Dois prendre en charge le chiffrement OpenPGP.

### Critères optimaux

Nos critères optimaux représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de ces fonctionnalités, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Devrait être open source.
- Devrait être multiplateforme.
- Ne devrait collecter aucune donnée télémétrique par défaut.
- Devrait prendre en charge OpenPGP nativement sans avoir besoin d'extensions.
- Devrait permettre de stocker localement des mails chiffrés avec OpenPGP.
