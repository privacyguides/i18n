---
meta_title: "Recommandations de fournisseurs d'e-mail privés et chiffrés - Privacy Guides"
title: "Services d'e-mail"
icon: material/email
description: Ces fournisseurs d'e-mail constituent un excellent moyen de stocker vos e-mails en toute sécurité, et nombre d'entre eux proposent un système de chiffrement OpenPGP interopérable avec d'autres fournisseurs.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protège contre les menaces suivantes:</small>

- [:material-server-network: Fournisseurs de service](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

L'e-mail est pratiquement une nécessité pour utiliser n'importe quel service en ligne, mais nous ne le recommandons pas pour les conversations de particulier à particulier. Plutôt que d'utiliser l'e-mail pour contacter d'autres personnes, envisagez d'utiliser un support de messagerie instantanée qui prend en charge la confidentialité persistante.

[Messageries instantanées recommandées](real-time-communication.md ""){.md-button}

## Fournisseurs recommandés

Pour tout le reste, nous recommandons une variété de fournisseurs d'email en fonction de la viabilité de leur modèle économique et de leurs fonctions intégrées de sécurité et de confidentialité. Lisez notre \[liste complète de critères\](#criteres) pour plus d'informations.

| Fournisseur                 | OpenPGP / WKD                          | IMAP / SMTP                                                               | Chiffrement zéro accès                                       | Paiements anonymes                   |
| --------------------------- | -------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------ |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Abonnements payants uniquement | :material-check:{ .pg-green }                                | Argent liquide                       |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                                             | :material-information-outline:{ .pg-blue } E-mails seulement | Argent liquide                       |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                                    | :material-check:{ .pg-green }                                | Monero & argent liquide via un tiers |

En plus (ou à la place) d'un fournisseur de courrier électronique recommandé ici, vous pouvez envisager un [service d'alias de courrier électronique](email-aliasing.md) dédié pour protéger votre vie privée. Ces services permettent notamment de protéger votre boîte de réception réelle contre le spam, d'empêcher les spécialistes du marketing d'établir une corrélation entre vos comptes et de crypter tous les messages entrants à l'aide de PGP.

- [En savoir plus :material-arrow-right-drop-circle:](email-aliasing.md)

## Services compatibles avec OpenPGP

Ces fournisseurs prennent en charge nativement le chiffrement/déchiffrement OpenPGP et la norme [Web Key Directory](basics/email-security.md#what-is-the-web-key-directory-standard), ce qui permet d'obtenir des e-mails E2EE indépendamment du fournisseur. Par exemple, un utilisateur de Proton Mail peut envoyer un message E2EE à un utilisateur de Mailbox.org, ou vous pouvez recevoir des notifications chiffrées par OpenPGP de la part de services internet qui le supportent.

<div class="grid cards" markdown>

- ![logo Proton Mail](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![logo Mailbox.org](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Lors de l'utilisation d'une technologie E2EE telle que OpenPGP, votre e-mail contiendra toujours certaines métadonnées non chiffrées dans l'en-tête, y compris généralement la ligne d'objet ! En savoir plus sur les [métadonnées des e-mails](basics/email-security.md#email-metadata-overview).

OpenPGP ne prend pas non plus en charge la confidentialité persistante, ce qui signifie que si votre clé privée ou celle du destinataire est volée, tous les messages précédents chiffrés avec elle seront exposés. [Comment protéger mes clés privées ?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Logo Proton Mail](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** est un service d'e-mail qui met l'accent sur la confidentialité, le chiffrement, la sécurité et la facilité d'utilisation. Ils sont en activité depuis 2013. Proton AG is based in Geneva, Switzerland. The Proton Mail Free plan comes with 500 MB of Mail storage, which you can increase up to 1 GB for free.

[:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/mail/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Les comptes gratuits présentent certaines limitations, comme le fait de ne pas pouvoir effectuer de recherche dans le corps du texte et de ne pas avoir accès à [Proton Mail Bridge](https://proton.me/mail/bridge), qui est nécessaire pour utiliser un [client d'e-mail de bureau recommandé](email-clients.md) (par exemple Thunderbird). Les comptes payants comprennent des fonctionnalités telles que Proton Mail Bridge, un espace de stockage supplémentaire et la prise en charge de domaines personnalisés. Une [lettre d'attestation](https://proton.me/blog/security-audit-all-proton-apps) a été fournie pour les applications de Proton Mail le 9 novembre 2021 par [Securitum](https://research.securitum.com).

If you have the Proton Unlimited plan or any multi-user Proton plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

Proton Mail dispose de rapports de plantages internes qu'il **ne partage pas** avec des tiers. Ils peuvent être désactivés dans l'application web : :gear: → **Tous les paramètres** → **Compte** → **Sécurité et vie privée** → **Vie privée et collecte de données**.

#### :material-check:{ .pg-green } Domaines personnalisés et alias

Les abonnés payants à Proton Mail peuvent utiliser leur propre domaine avec le service ou une adresse [fourre-tout](https://proton.me/support/catch-all). Proton Mail prend également en charge la [sous-adressage](https://proton.me/support/creating-aliases), ce qui est utile pour les personnes qui ne souhaitent pas acheter un domaine.

#### :material-check:{ .pg-green } Modes de paiement privés

Proton Mail [accepte](https://proton.me/support/payment-options) les paiements en espèces par courrier, ainsi que les paiements par carte de crédit/débit, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc)et PayPal.

#### :material-check:{ .pg-green } Sécurité du compte

Proton Mail supports TOTP [two-factor authentication](https://proton.me/support/two-factor-authentication-2fa) and [hardware security keys](https://proton.me/support/2fa-security-key) using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two-factor authentication first.

#### :material-check:{ .pg-green } Sécurité des données

Proton Mail dispose d'un [chiffrement à accès zéro](https://proton.me/blog/zero-access-encryption) au repos pour vos e-mails et [calendriers](https://proton.me/news/protoncalendar-security-model). Les données sécurisées par un chiffrement à accès zéro ne sont accessibles que par vous.

Certaines informations stockées dans [Proton Contacts](https://proton.me/support/proton-contacts), telles que les noms et les adresses e-mail, ne sont pas sécurisées par un chiffrement à accès zéro. Les champs de contact qui prennent en charge le chiffrement à accès zéro, comme les numéros de téléphone, sont indiqués par une icône de cadenas.

#### :material-check:{ .pg-green } Chiffrement des e-mails

Proton Mail a [du chiffrement OpenPGP intégré](https://proton.me/support/how-to-use-pgp) dans son interface d'e-mail web. Les e-mails destinés à d'autres comptes Proton Mail sont chiffrés automatiquement, et le chiffrement vers des adresses autres que Proton Mail avec une clé OpenPGP peut être activé facilement dans les paramètres de votre compte. Proton prend également en charge la découverte automatique de clés externes avec le [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Cela signifie que les e-mails envoyés à d'autres fournisseurs qui utilisent WKD seront automatiquement chiffrés avec OpenPGP, sans qu'il soit nécessaire d'échanger manuellement des clés PGP publiques avec vos contacts. Ils vous permettent également de [chiffrer des messages destinés à des adresses non Proton Mail sans OpenPGP](https://proton.me/support/password-protected-emails), sans qu'ils aient besoin de s'inscrire à un compte Proton Mail.

Proton Mail publie également les clés publiques des comptes Proton via HTTP à partir de leur WKD. Cela permet aux personnes qui n'utilisent pas Proton Mail de trouver facilement les clés OpenPGP des comptes Proton Mail, pour un E2EE inter-fournisseurs. Cela ne s'applique qu'aux adresses e-mails se terminant par un domaine Proton, comme @proton.me. Si vous utilisez un domaine personnalisé, vous devez [configurer le WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) séparément.

#### :material-information-outline:{ .pg-blue } Résiliation du compte

Si vous avez un compte payant et que votre [facture est impayée](https://proton.me/support/delinquency) après 14 jours, vous ne pourrez pas accéder à vos données. Après 30 jours, votre compte sera en impayé et ne recevra plus d'e-mail entrant. Vous continuerez à être facturé pendant cette période. Proton [supprimera les comptes gratuits inactifs](https://proton.me/support/inactive-accounts) après un an. Vous **ne pouvez pas** réutiliser l'adresse e-mail d'un compte désactivé.

#### :material-information-outline:{ .pg-blue } Fonctionnalités supplémentaires

Proton Mail's [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) plan also enables access to other Proton services in addition to providing multiple custom domains, unlimited hide-my-email aliases, and 500 GB of storage.

Proton Mail ne propose pas de fonction d'héritage numérique.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Logo de Mailbox.org](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** est un service d'e-mail qui se veut sécurisé, sans publicité et alimenté par une énergie 100% écologique. Il est en activité depuis 2014. Mailbox.org est basé à Berlin, en Allemagne. Accounts start with up to 2 GB storage, which can be upgraded as needed.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Domaines personnalisés et alias

Mailbox.org vous permet d'utiliser votre propre domaine et prend en charge les adresses [fourre-tout](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name). Mailbox.org prend également en charge le [sous-adressage](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), ce qui est utile si vous ne souhaitez pas acheter un domaine.

#### :material-check:{ .pg-green } Modes de paiement privés

Mailbox.org n'accepte aucune crypto-monnaie en raison de la suspension des activités de son processeur de paiement BitPay en Allemagne. However, they do accept cash by mail, cash payment to bank account, bank transfer, credit card, PayPal and a couple of German-specific processors: paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } Sécurité du compte

Mailbox.org supports [two-factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. Vous pouvez utiliser TOTP ou une [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via [YubiCloud](https://yubico.com/products/services-software/yubicloud). Les normes web telles que [WebAuthn](https://fr.wikipedia.org/wiki/WebAuthn) ne sont pas encore prises en charge.

#### :material-information-outline:{ .pg-blue } Sécurité des données

Mailbox.org permet le chiffrement des e-mails entrant à l'aide de sa [boîte e-mails chiffrée](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Les nouveaux messages que vous recevrez seront alors immédiatement chiffrés avec votre clé publique.

Cependant, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), la plateforme logicielle utilisée par Mailbox.org, [ne prend pas en charge](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) le chiffrement de votre carnet d'adresses et de votre calendrier. Une [option tierce](calendar.md) pourrait être plus appropriée pour ces informations.

#### :material-check:{ .pg-green } Chiffrement des e-mails

Mailbox.org a [du chiffrement intégré](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) dans son interface d'e-mail web, ce qui simplifie l'envoi de messages à des personnes possédant des clés OpenPGP publiques. Ils permettent également aux [destinataires distants de déchiffrer un e-mail](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) sur les serveurs de Mailbox.org. Cette fonction est utile lorsque le destinataire distant ne dispose pas d'OpenPGP et ne peut pas déchiffrer une copie de l'e-mail dans sa propre boîte mail.

Mailbox.org prend également en charge la découverte de clés publiques via HTTP à partir de leur [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Cela permet aux personnes extérieures à Mailbox.org de trouver facilement les clés OpenPGP des comptes Mailbox.org, pour un E2EE inter-fournisseurs. Cela ne s'applique qu'aux adresses e-mails se terminant par un domaine Mailbox, comme @mailbox.org. Si vous utilisez un domaine personnalisé, vous devez [configurer le WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) séparément.

#### :material-information-outline:{ .pg-blue } Résiliation du compte

Votre compte sera marqué comme un compte d'utilisateur restreint à la fin de votre contrat. Il sera irrévocablement supprimé après [30 jours](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Fonctionnalités supplémentaires

Vous pouvez accéder à votre compte Mailbox.org via IMAP/SMTP en utilisant leur [service .onion](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). However, their webmail interface cannot be accessed via their .onion service, and you may experience TLS certificate errors.

Tous les comptes sont assortis d'un espace de stockage cloud limité, qui [peut être chiffré](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org propose également l'alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), qui applique le chiffrement TLS à la connexion entre les serveurs d'e-mail, faute de quoi le message ne sera pas envoyé. Mailbox.org prend également en charge [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) en plus des protocoles d'accès standard comme IMAP et POP3.

Mailbox.org dispose d'une fonction d'héritage numérique pour toutes les offres. Vous pouvez choisir de transmettre certaines de vos données à vos héritiers, à condition d'en faire la demande et de fournir votre testament. Vous pouvez également désigner une personne par son nom et son adresse.

## D'autres fournisseurs

Ces fournisseurs stockent vos e-mails avec un chiffrement à connaissance zéro, ce qui en fait d'excellentes options pour assurer la sécurité de vos e-mails stockés. Cependant, ils ne prennent pas en charge les normes de chiffrement interopérables pour des communications E2EE entre fournisseurs.

<div class="grid cards" markdown>

- ![logo Tuta](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![logo Tuta](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (formerly *Tutanota*) is an email service with a focus on security and privacy through the use of encryption. Tuta est en activité depuis 2011 et est basée à Hanovre, en Allemagne. Free accounts start with 1 GB of storage.

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:fontawesome-brands-windows: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta ne prend pas en charge le [protocole IMAP](https://tuta.com/support#imap) ni l'utilisation de [clients d'e-mail](email-clients.md) tiers, et vous ne pourrez pas non plus ajouter [des comptes e-mail externes](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) à l'application Tuta. L'[importation d'e-mails](https://github.com/tutao/tutanota/issues/630) n'est pas non plus prise en charge actuellement, mais cela [devrait changer](https://tuta.com/blog/kickoff-import). Les e-mails peuvent être exportés [individuellement ou par sélection groupée](https://tuta.com/support#generalMail) par dossier, ce qui peut s'avérer peu pratique si vous avez de nombreux dossiers.

#### :material-check:{ .pg-green } Domaines personnalisés et alias

Les comptes Tuta payants peuvent utiliser 15 ou 30 alias en fonction de leur abonnement et un nombre illimité d'alias sur [domaines personnalisés](https://tuta.com/support#custom-domain). Tuta ne permet pas le [sous-adressage (adresses plus)](https://tuta.com/support#plus), mais vous pouvez utiliser une adresse [fourre-tout](https://tuta.com/support#settings-global) avec un domaine personnalisé.

#### :material-information-outline:{ .pg-blue } Modes de paiement privés

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with ProxyStore.

#### :material-check:{ .pg-green } Sécurité du compte

Tuta supports [two-factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Sécurité des données

Tuta dispose d'un [chiffrement à accès zéro au repos](https://tuta.com/support#what-encrypted) pour vos e-mails, votre [carnet d'adresses, vos contacts](https://tuta.com/support#encrypted-address-book) et vos [calendriers](https://tuta.com/support#calendar). Cela signifie que les messages et autres données stockés dans votre compte ne sont lisibles que par vous.

#### :material-information-outline:{ .pg-blue } Chiffrement des e-mails

Tuta [n'utilise pas OpenPGP](https://tuta.com/support/#pgp). Les comptes Tuta ne peuvent recevoir des e-mails chiffrés provenant de comptes e-mail non Tuta que s'ils sont envoyés via une [boîte mail temporaire Tuta](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Résiliation du compte

Tuta supprimera [les comptes gratuits inactifs](https://tuta.com/support#inactive-accounts) après six mois. Vous pouvez réutiliser un compte gratuit désactivé si vous payez.

#### :material-information-outline:{ .pg-blue } Fonctionnalités supplémentaires

Tuta offre la version professionnelle de [Tuta aux organisations à but non lucratif](https://tuta.com/blog/secure-email-for-non-profit) gratuitement ou avec une forte réduction.

Tuta ne propose pas de fonction d'héritage numérique.

## E-mail auto-hébergé

Les administrateurs système peuvent envisager de mettre en place leur propre serveur d'e-mail. Les serveurs d'e-mail requièrent une attention et une maintenance permanente afin de garantir la sécurité et la fiabilité de la distribution des e-mails.

### Solutions logicielles combinées

<div class="admonition recommendation" markdown>

![Logo Mailcow](assets/img/email/mailcow.svg){ align=right }

**Mailcow** est un serveur d'e-mail plus avancé, parfait pour ceux qui ont un peu plus d'expérience de Linux. It has everything you need in a Docker container: a mail server with DKIM support, antivirus and spam monitoring, webmail and ActiveSync with SOGo, and web-based administration with 2FA support.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title="Contribute" }

</div>

<div class="admonition recommendation" markdown>

![Logo Mail-in-a-Box](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** est un script de configuration automatisé pour le déploiement d'un serveur d'e-mail sur Ubuntu. Son objectif est de faciliter la mise en place de son propre serveur d'e-mail.

[:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }

</div>

Pour une approche plus manuelle, nous avons choisi ces deux articles :

- [Mise en place d'un serveur mail avec OpenSMTPD, Dovecot et Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [Comment gérer votre propre serveur mail](https://c0ffee.net/blog/mail-server-guide) (août 2017)

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des fournisseurs que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour tout fournisseur d'e-mail souhaitant être recommandé, y compris la mise en place des bonnes pratiques du secteur, une technologie moderne et bien plus. Nous vous suggérons de vous familiariser avec cette liste avant de choisir un fournisseur d'e-mail, et de mener vos propres recherches pour vous assurer que le fournisseur d'e-mail que vous choisissez est le bon choix pour vous.

### Technologie

Nous considérons ces caractéristiques comme importantes afin de fournir un service sûr et optimal. Vous devez vous demander si le fournisseur possède les caractéristiques dont vous avez besoin.

**Minimum pour se qualifier :**

- Chiffre les données du compte e-mail au repos avec un chiffrement à accès zéro.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .EML with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Permet aux utilisateurs d'utiliser leur propre [nom de domaine](https://en.wikipedia.org/wiki/Domain_name). Les noms de domaine personnalisés sont importants pour les utilisateurs car ils leur permettent de conserver leur indépendance du service, au cas où celui-ci tournerait mal ou serait racheté par une autre société qui ne donne pas priorité à la vie privée.
- Fonctionne sur sa propre infrastructure, c'est-à-dire qu'elle ne repose pas sur des fournisseurs de services d'e-mail tiers.

**Dans le meilleur des cas :**

- Chiffre toutes les données du compte (contacts, calendriers, etc.) au repos avec un chiffrement à accès zéro.
- Une interface d'e-mail web intégrée avec chiffrement E2EE/PGP est fournie à titre de commodité.
- Prise en charge de [WKD](https://wiki.gnupg.org/WKD) pour permettre une meilleure découverte des clés publiques OpenPGP via HTTP. Les utilisateurs de GnuPG peuvent obtenir une clé en tapant : `gpg --locate-key utilisateur_exemple@exemple.fr`
- Prise en charge d'une boîte mail temporaire pour les utilisateurs externes. Cette fonction est utile lorsque vous souhaitez envoyer un e-mail chiffré, sans envoyer une copie réelle à votre destinataire. Ces e-mails ont généralement une durée de vie limitée et sont ensuite automatiquement supprimés. Ils n'obligent pas non plus le destinataire à configurer un système de chiffrement comme OpenPGP.
- Disponibilité des services du fournisseur d'e-mail via un [service onion](https://en.wikipedia.org/wiki/.onion).
- Support du [sous-adressage](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Catch-all or alias functionality for those who use their own domains.
- Use of standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Les protocoles d'accès standard garantissent que les clients peuvent facilement télécharger l'ensemble de leurs e-mails, s'ils souhaitent changer de fournisseur.

### Confidentialité

Nous préférons que nos prestataires recommandés collectent le moins de données possible.

**Minimum pour se qualifier :**

- Protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Ne demandez pas de Données à Caractère Personnel (DCP) en plus d'un nom d'utilisateur et d'un mot de passe.
- Politique de confidentialité répondant aux exigences définies par le RGPD.

**Dans le meilleur des cas :**

- Accepte des [options de paiement anonymes](advanced/payments.md) ([crypto-monnaie](cryptocurrency.md), argent liquide, cartes cadeaux, etc.)
- Hébergé dans une juridiction disposant de lois strictes en matière de protection de la confidentialité des e-mails.

### Sécurité

Les serveurs d'e-mail traitent un grand nombre de données très sensibles. We expect that providers will adopt best industry practices in order to protect their customers.

**Minimum pour se qualifier :**

- Protection de l'interface d'e-mail web avec une A2F, tel que TOTP.
- Zero access encryption, which builds on encryption at rest. Le fournisseur ne dispose pas des clés de déchiffrement des données qu'il détient. Cela permet d'éviter qu'un employé malhonnête ne divulgue les données auxquelles il a accès ou qu'un adversaire distant ne divulgue les données qu'il a volées en obtenant un accès non autorisé au serveur.
- Prise en charge de [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions).
- Aucune erreurs ou vulnérabilités TLS lors du profilage par des outils tels que [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), ou [Qualys SSL Labs](https://ssllabs.com/ssltest); cela inclut les erreurs liées aux certificats et les paramètres DH faibles, tels que ceux qui ont conduit à [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Une préférence pour les serveurs (facultatif sur TLSv1.3) pour des suites de chiffrement fortes qui prennent en charge la confidentialité persistante et le chiffrement authentifié.
- Une politique valide [MTA-STS](https://tools.ietf.org/html/rfc8461) et [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Des enregistrements [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) valides.
- Des enregistrements [SPF](https://fr.wikipedia.org/wiki/Sender_Policy_Framework) et [DKIM](https://fr.wikipedia.org/wiki/DomainKeys_Identified_Mail) valides.
- Disposer d'un enregistrement et d'une politique [DMARC](https://fr.wikipedia.org/wiki/DMARC) appropriés ou utiliser [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) pour l'authentification. Si l'authentification DMARC est utilisée, la politique doit être définie comme suit : `reject` ou `quarantine`.
- Une préférence pour une suite de serveur TLS 1.2 ou plus récente et un plan pour [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- Une soumission [SMTPS](https://en.wikipedia.org/wiki/SMTPS), en supposant que le SMTP est utilisé.
- Des normes de sécurité des sites web telles que :
    - [HTTP Strict Transport Security](https://fr.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - Une [Intégrité des sous-ressources](https://en.wikipedia.org/wiki/Subresource_Integrity) si des éléments sont chargés depuis des domaines externes.
- Must support viewing of [message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**Dans le meilleur des cas :**

- Prise en charge de l'authentification matérielle, à savoir U2F and [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- Un [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) en plus de la prise en charge de DANE.
- Implementation of [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Des audits de sécurité publiés par une société tierce réputée.
- Des programmes de primes aux bugs et/ou un processus coordonné de divulgation des vulnérabilités.
- Des normes de sécurité des sites web telles que :
    - [Content Security Policy (CSP)](https://fr.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Confiance

Vous ne confieriez pas vos finances à une personne ayant une fausse identité, alors pourquoi lui confier vos e-mails ? Nous exigeons de nos fournisseurs recommandés qu'ils rendent public leur propriété ou leur direction. Nous aimerions également voir des rapports de transparence fréquents, notamment en ce qui concerne la manière dont les demandes de gouvernement sont traitées.

**Minimum pour se qualifier :**

- Une direction ou un propriétaire public.

**Dans le meilleur des cas :**

- Rapports de transparence fréquents.

### Marketing

With the email providers we recommend, we like to see responsible marketing.

**Minimum pour se qualifier :**

- Doit héberger lui-même ses outils d'analyse de traffic (pas de Google Analytics, Adobe Analytics, etc.). The provider's site must also comply with [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) for those who wish to opt out.

Must not have any irresponsible marketing, which can include the following:

- Prétendre à un "chiffrement incassable". Le chiffrement doit être utilisé en supposant qu'il ne soit plus secret dans le futur, lorsque la technologie existera pour le décrypter.
- Garantir la protection de l'anonymat à 100%. Lorsque quelqu'un prétend que quelque chose est à 100%, cela signifie qu'il n'y a aucune certitude d'échec. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:

    - Réutiliser des informations personnelles (par exemple comptes d'e-mail, pseudonymes uniques, etc.) auxquelles ils ont eu accès sans logiciel d'anonymat (Tor, VPN, etc.)
    - [La capture d'empreinte numérique des navigateurs](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Dans le meilleur des cas :**

- Clear and easy to read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### Fonctionnalités supplémentaires

Bien qu'il ne s'agisse pas d'exigences strictes, nous avons pris en compte d'autres facteurs liés à la commodité ou à la confidentialité pour déterminer les fournisseurs à recommander.
