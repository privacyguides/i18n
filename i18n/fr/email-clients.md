---
title: "Clients e-mails"
icon: material/email-open
description: Ces clients d'e-mail respectent la vie privée et prennent en charge le chiffrement OpenPGP.
cover: email-clients.webp
---

The **email clients** we recommend support both [OpenPGP](encryption.md#openpgp) and strong authentication such as [Open Authorization (OAuth)](https://en.wikipedia.org/wiki/OAuth). OAuth vous permet d'utiliser l'[Authentification à Multi-Facteurs](multi-factor-authentication) et d'empêcher le vol de compte.

<details class="warning" markdown>
<summary>L'e-mail n'assure pas la confidentialité persistante</summary>

When using end-to-end encryption (E2EE) technology like OpenPGP, email will still have [some metadata](basics/email-security.md#email-metadata-overview) that is not encrypted in the header of the email.

OpenPGP ne prend pas non plus en charge la [confidentialité persistante](https://en.wikipedia.org/wiki/Forward_secrecy), ce qui signifie que si votre clé privée ou celle du destinataire est volée, tous les messages précédents chiffrés avec cette clé seront exposés : [comment protéger mes clés privées ?](basics/email-security.md) Envisagez d'utiliser un support qui assure la confidentialité persistante :

[Communication en temps réel](real-time-communication.md ""){.md-button}

</details>

## Multi-plateformes

### Thunderbird

<div class="admonition recommendation" markdown>

![Logo Thunderbird](assets/img/email-clients/thunderbird.svg){ align=right }

**Thunderbird** est un client d'e-mail, de groupes de discussion, de flux d'informations et de chat (XMPP, IRC, Matrix) gratuit, open-source et multiplateforme, développé par la communauté Thunderbird, et précédemment par la Fondation Mozilla.

[:octicons-home-16: Homepage](https://thunderbird.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/thunderbird){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.mozilla.org/products/thunderbird){ .card-link title=Documentation}
[:octicons-code-16:](https://hg.mozilla.org/comm-central){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://thunderbird.net)
- [:simple-apple: macOS](https://thunderbird.net)
- [:simple-linux: Linux](https://thunderbird.net)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.Thunderbird)

</details>

</div>

#### Configuration recommandée

Nous vous recommandons de modifier certains de ces paramètres pour rendre Thunderbird un peu plus privé.

Ces options se trouvent dans :material-menu: → **Paramètres** → **Confidentialité & Sécurité**.

##### Contenu Web

- [ ] Décochez  **Se souvenir des sites web et des liens que j'ai visités**
- [ ] Décochez  **Accepter les cookies des sites**

##### Télémétrie

- [ ] Décochez  **Autoriser Thunderbird à envoyer des données techniques et d'interaction à Mozilla**

#### Thunderbird-user.js (avancé)

[`thunderbird-user.js`](https://github.com/HorlogeSkynet/thunderbird-user.js) is a set of configurations options that aims to disable as many of the web-browsing features within Thunderbird as possible in order to reduce attack surface and maintain privacy. Certains changements sont rétroportés depuis le [projet Arkenfox](https://github.com/arkenfox/user.js).

## Spécifique à une plateforme

### Apple Mail (macOS)

<div class="admonition recommendation" markdown>

![Apple Mail logo](assets/img/email-clients/applemail.png){ align=right }

**Apple Mail** est inclus dans macOS et peut être étendu pour prendre en charge OpenPGP avec [GPG Suite](/encryption/# gpg-suite), ce qui ajoute la possibilité d'envoyer des e-mails chiffrés.

[:octicons-home-16: Homepage](https://support.apple.com/guide/mail/welcome/mac){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/en-ww){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/mail){ .card-link title=Documentation}

</details>

</div>

Apple Mail a la possibilité de charger le contenu distant en arrière-plan ou de le bloquer entièrement et masquer votre adresse IP des expéditeurs sur [macOS](https://support.apple.com/guide/mail/mlhl03be2866/mac) et [iOS](https://support.apple.com/guide/iphone/iphf084865c7/ios).

### Canary Mail (iOS)

<div class="admonition recommendation" markdown>

![Logo de Canary Mail](assets/img/email-clients/canarymail.svg){ align=right }

**Canary Mail** est un client d'e-mail payant conçu pour rendre le chiffrement de bout en bout transparent grâce à des fonctions de sécurité telles que le verrouillage biométrique des applications.

[:octicons-home-16: Homepage](https://canarymail.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://canarymail.io/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://canarymail.io/help){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.canarymail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1236045954)
- [:fontawesome-brands-windows: Windows](https://canarymail.io/downloads.html)

</details>

</div>

<details class="warning" markdown>
<summary>Avertissement</summary>

Canary Mail n'a publié que récemment un client Windows et Android, mais nous ne pensons pas qu'ils soient aussi stables que leurs homologues iOS et Mac.

</details>

Canary Mail est à source fermée. Nous le recommandons en raison du peu de choix disponibles pour les clients d'e-mail sur iOS prenant en charge PGP E2EE.

### FairEmail (Android)

<div class="admonition recommendation" markdown>

![Logo FairEmail](assets/img/email-clients/fairemail.svg){ align=right }

**FairEmail** est une application d'e-mail minimale et open-source, utilisant des standards ouverts (IMAP, SMTP, OpenPGP) avec une faible consommation de données et de batterie.

[:octicons-home-16: Homepage](https://email.faircode.eu){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/M66B/FairEmail/blob/master/PRIVACY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/M66B/FairEmail/blob/master/FAQ.md){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/M66B/FairEmail){ .card-link title="Source Code" }
[:octicons-heart-16:](https://email.faircode.eu/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=eu.faircode.email)
- [:simple-github: GitHub](https://github.com/M66B/FairEmail/releases)

</details>

</div>

### GNOME Evolution (GNOME)

<div class="admonition recommendation" markdown>

![Logo Evolution](assets/img/email-clients/evolution.svg){ align=right }

**Evolution** est une application de gestion des informations personnelles qui fournit des fonctionnalités intégrées d'e-mail, de calendrier et de carnet d'adresses. Evolution has extensive [documentation](https://help.gnome.org/users/evolution/stable) to help you get started.

[:octicons-home-16: Homepage](https://wiki.gnome.org/Apps/Evolution){ .md-button .md-button--primary }
[:octicons-eye-16:](https://wiki.gnome.org/Apps/Evolution/PrivacyPolicy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.gnome.org/users/evolution/stable){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.gnome.org/GNOME/evolution){ .card-link title="Source Code" }
[:octicons-heart-16:](https://gnome.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.gnome.Evolution)

</details>

</div>

### K-9 Mail (Android)

<div class="admonition recommendation" markdown>

![Logo de K-9 Mail](assets/img/email-clients/k9mail.svg){ align=right }

**K-9 Mail** est une application d'e-mail indépendante qui prend en charge les boîtes mail POP3 et IMAP, mais ne prend en charge le push mail que pour IMAP.

À l'avenir, K-9 Mail sera le client Thunderbird [officiel](https://k9mail.app/2022/06/13/K-9-Mail-and-Thunderbird.html) pour Android .

[:octicons-home-16: Homepage](https://k9mail.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://k9mail.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.k9mail.app){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/thundernest/k-9){ .card-link title="Source Code" }
[:octicons-heart-16:](https://k9mail.app/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.fsck.k9)
- [:simple-github: GitHub](https://github.com/thundernest/k-9/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Lorsque vous répondez à un membre d'une liste de diffusion, l'option "répondre" peut également inclure la liste de diffusion. Pour plus d'informations, voir [thundernest/k-9 #3738](https://github.com/thundernest/k-9/issues/3738).

</div>

### Kontact (KDE)

<div class="admonition recommendation" markdown>

![Logo Kontact](assets/img/email-clients/kontact.svg){ align=right }

**Kontact** est une application de gestion des informations personnelles (PIM) issue du projet [KDE](https://kde.org). Il offre un client d'e-mail, un carnet d'adresses, un organiseur et un client RSS.

[:octicons-home-16: Homepage](https://kontact.kde.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kde.org/privacypolicy-apps){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kontact.kde.org/users){ .card-link title=Documentation}
[:octicons-code-16:](https://invent.kde.org/pim/kmail){ .card-link title="Source Code" }
[:octicons-heart-16:](https://kde.org/community/donations){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-linux: Linux](https://kontact.kde.org/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.kde.kontact)

</details>

</div>

### Mailvelope (Navigateur)

<div class="admonition recommendation" markdown>

![Logo Mailvelope](assets/img/email-clients/mailvelope.svg){ align=right }

**Mailvelope** est une extension de navigateur qui permet l'échange d'e-mails chiffrés selon la norme de chiffrement OpenPGP.

[:octicons-home-16: Homepage](https://mailvelope.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailvelope.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mailvelope.com/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mailvelope/mailvelope){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/mailvelope)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/mailvelope/kajibbejlbohfaggdiogboambcijhkke)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/mailvelope/dgcbddhdhjppfdfjpciagmmibadmoapc)

</details>

</div>

### NeoMutt (CLI)

<div class="admonition recommendation" markdown>

![Logo NeoMutt](assets/img/email-clients/mutt.svg){ align=right }

**NeoMutt** est un lecteur d'e-mails en ligne de commande (ou MUA) open-source pour Linux et BSD. C'est un fork de [Mutt](https://fr.wikipedia.org/wiki/Mutt) avec des fonctionnalités supplémentaires.

NeoMutt est un client textuel qui a une courbe d'apprentissage abrupte. Il est cependant très personnalisable.

[:octicons-home-16: Homepage](https://neomutt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://neomutt.org/guide){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/neomutt/neomutt){ .card-link title="Source Code" }
[:octicons-heart-16:](https://paypal.com/paypalme/russon){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-apple: macOS](https://neomutt.org/distro)
- [:simple-linux: Linux](https://neomutt.org/distro)

</details>

</div>

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Qualifications minimales

- Les applications développées pour des systèmes d'exploitation open source doivent être open source.
- Ne doit pas collecter de télémétrie, ou disposer d'un moyen facile de désactiver toute télémétrie.
- Doit prendre en charge le chiffrement des messages OpenPGP.

### Dans le meilleur des cas

Nos critères de cas idéal représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de cette fonctionnalité, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Devrait être open source.
- Devrait être multiplateforme.
- Ne devrait pas collecter de télémétrie par défaut.
- Devrait prendre en charge OpenPGP nativement, c'est-à-dire sans extensions.
- Devrait prendre en charge le stockage local d'e-mails chiffrés par OpenPGP.
