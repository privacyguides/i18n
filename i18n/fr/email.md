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

| Fournisseur                 | OpenPGP / WKD                          | IMAP / SMTP                                                               | Zero-Access Encryption                                       | Anonymous Payment Methods             |
| --------------------------- | -------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Abonnements payants uniquement | :material-check:{ .pg-green }                                | Argent liquide                        |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                                             | :material-information-outline:{ .pg-blue } E-mails seulement | Argent liquide                        |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                                    | :material-check:{ .pg-green }                                | Monero <br>Cash via third party |

In addition to (or instead of) an email provider recommended here, you may wish to consider a dedicated [email aliasing service](email-aliasing.md#recommended-providers) to protect your privacy. Ces services permettent notamment de protéger votre boîte de réception réelle contre le spam, d'empêcher les spécialistes du marketing d'établir une corrélation entre vos comptes et de crypter tous les messages entrants à l'aide de PGP.

- [En savoir plus :material-arrow-right-drop-circle:](email-aliasing.md)

## Services compatibles avec OpenPGP

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory (WKD) standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic end-to-end encrypted emails. Par exemple, un utilisateur de Proton Mail peut envoyer un message E2EE à un utilisateur de Mailbox.org, ou vous pouvez recevoir des notifications chiffrées par OpenPGP de la part de services internet qui le supportent.

<div class="grid cards" markdown>

- ![logo Proton Mail](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![logo Mailbox.org](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Lors de l'utilisation d'une technologie E2EE telle que OpenPGP, votre e-mail contiendra toujours certaines métadonnées non chiffrées dans l'en-tête, y compris généralement la ligne d'objet ! En savoir plus sur les [métadonnées des e-mails](basics/email-security.md#email-metadata-overview).

OpenPGP also does not support forward secrecy, which means if the private key of either you or the message recipient is ever stolen, all previous messages encrypted with it will be exposed.

- [How do I protect my private keys?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Logo Proton Mail](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** est un service d'e-mail qui met l'accent sur la confidentialité, le chiffrement, la sécurité et la facilité d'utilisation. Ils sont en activité depuis 2013. Proton AG is based in Geneva, Switzerland.

The Proton Free plan comes with 500 MB of Mail storage, which you can increase up to 1 GB for free.

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

Free accounts have some limitations, such as not being able to search body text and not having access to [Proton Mail Bridge](https://proton.me/mail/bridge), which is required to use a [recommended desktop email client](email-clients.md) (e.g., Thunderbird). Les comptes payants comprennent des fonctionnalités telles que Proton Mail Bridge, un espace de stockage supplémentaire et la prise en charge de domaines personnalisés. If you have the Proton Unlimited plan or any multi-user Proton plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

Une [lettre d'attestation](https://proton.me/blog/security-audit-all-proton-apps) a été fournie pour les applications de Proton Mail le 9 novembre 2021 par [Securitum](https://research.securitum.com).

Proton Mail dispose de rapports de plantages internes qu'il **ne partage pas** avec des tiers. Ils peuvent être désactivés dans l'application web : :gear: → **Tous les paramètres** → **Compte** → **Sécurité et vie privée** → **Vie privée et collecte de données**.

#### :material-check:{ .pg-green } Domaines personnalisés et alias

Les abonnés payants à Proton Mail peuvent utiliser leur propre domaine avec le service ou une adresse [fourre-tout](https://proton.me/support/catch-all). Proton Mail prend également en charge la [sous-adressage](https://proton.me/support/creating-aliases), ce qui est utile pour les personnes qui ne souhaitent pas acheter un domaine.

#### :material-check:{ .pg-green } Modes de paiement privés

Proton Mail [accepts](https://proton.me/support/payment-options) **cash** by mail in addition to standard credit/debit card, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), and PayPal payments.

#### :material-check:{ .pg-green } Sécurité du compte

Proton Mail supports TOTP [two-factor authentication](https://proton.me/support/two-factor-authentication-2fa) and [hardware security keys](https://proton.me/support/2fa-security-key) using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two-factor authentication first.

#### :material-check:{ .pg-green } Sécurité des données

Proton Mail dispose d'un [chiffrement à accès zéro](https://proton.me/blog/zero-access-encryption) au repos pour vos e-mails et [calendriers](https://proton.me/news/protoncalendar-security-model). Les données sécurisées par un chiffrement à accès zéro ne sont accessibles que par vous.

Certaines informations stockées dans [Proton Contacts](https://proton.me/support/proton-contacts), telles que les noms et les adresses e-mail, ne sont pas sécurisées par un chiffrement à accès zéro. Les champs de contact qui prennent en charge le chiffrement à accès zéro, comme les numéros de téléphone, sont indiqués par une icône de cadenas.

#### :material-check:{ .pg-green } Chiffrement des e-mails

Proton Mail a [du chiffrement OpenPGP intégré](https://proton.me/support/how-to-use-pgp) dans son interface d'e-mail web. Les e-mails destinés à d'autres comptes Proton Mail sont chiffrés automatiquement, et le chiffrement vers des adresses autres que Proton Mail avec une clé OpenPGP peut être activé facilement dans les paramètres de votre compte. Proton also supports automatic external key discovery with WKD. Cela signifie que les e-mails envoyés à d'autres fournisseurs qui utilisent WKD seront automatiquement chiffrés avec OpenPGP, sans qu'il soit nécessaire d'échanger manuellement des clés PGP publiques avec vos contacts. Ils vous permettent également de [chiffrer des messages destinés à des adresses non Proton Mail sans OpenPGP](https://proton.me/support/password-protected-emails), sans qu'ils aient besoin de s'inscrire à un compte Proton Mail.

Proton Mail publie également les clés publiques des comptes Proton via HTTP à partir de leur WKD. This allows people who don't use Proton Mail to find the OpenPGP keys of Proton Mail accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Proton's own domains, like `@proton.me`. If you use a custom domain, you must [configure WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Résiliation du compte

Si vous avez un compte payant et que votre [facture est impayée](https://proton.me/support/delinquency) après 14 jours, vous ne pourrez pas accéder à vos données. Après 30 jours, votre compte sera en impayé et ne recevra plus d'e-mail entrant. Vous continuerez à être facturé pendant cette période. Proton [supprimera les comptes gratuits inactifs](https://proton.me/support/inactive-accounts) après un an. Vous **ne pouvez pas** réutiliser l'adresse e-mail d'un compte désactivé.

#### :material-information-outline:{ .pg-blue } Fonctionnalités supplémentaires

Proton Mail's [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) plan also enables access to other Proton services in addition to providing multiple custom domains, unlimited hide-my-email aliases, and 500 GB of storage.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** is an email service with a focus on being secure, ad-free, and powered by 100% eco-friendly energy. Il est en activité depuis 2014. Mailbox.org est basé à Berlin, en Allemagne.

Accounts start with up to 2 GB storage, which can be upgraded as needed.

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

Mailbox.org n'accepte aucune crypto-monnaie en raison de la suspension des activités de son processeur de paiement BitPay en Allemagne. However, they do accept **cash** by mail, **cash** payment to bank account, bank transfer, credit card, PayPal, and a couple of German-specific processors: Paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } Sécurité du compte

Mailbox.org supports [two-factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. Vous pouvez utiliser TOTP ou une [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via [YubiCloud](https://yubico.com/products/services-software/yubicloud). Web standards such as [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) are not yet supported.

#### :material-information-outline:{ .pg-blue } Sécurité des données

Mailbox.org permet le chiffrement des e-mails entrant à l'aide de sa [boîte e-mails chiffrée](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Les nouveaux messages que vous recevrez seront alors immédiatement chiffrés avec votre clé publique.

However, [Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. A [standalone option](calendar.md) may be more appropriate for that data.

#### :material-check:{ .pg-green } Chiffrement des e-mails

Mailbox.org a [du chiffrement intégré](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) dans son interface d'e-mail web, ce qui simplifie l'envoi de messages à des personnes possédant des clés OpenPGP publiques. Ils permettent également aux [destinataires distants de déchiffrer un e-mail](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) sur les serveurs de Mailbox.org. Cette fonction est utile lorsque le destinataire distant ne dispose pas d'OpenPGP et ne peut pas déchiffrer une copie de l'e-mail dans sa propre boîte mail.

Mailbox.org also supports the discovery of public keys via HTTP from their WKD. This allows people outside of Mailbox.org to find the OpenPGP keys of Mailbox.org accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Mailbox.org's own domains, like `@mailbox.org`. If you use a custom domain, you must [configure WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Résiliation du compte

Votre compte sera marqué comme un compte d'utilisateur restreint à la fin de votre contrat. Il sera irrévocablement supprimé après [30 jours](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Fonctionnalités supplémentaires

Vous pouvez accéder à votre compte Mailbox.org via IMAP/SMTP en utilisant leur [service .onion](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). However, their webmail interface cannot be accessed via their .onion service, and you may experience TLS certificate errors.

Tous les comptes sont assortis d'un espace de stockage cloud limité, qui [peut être chiffré](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org propose également l'alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), qui applique le chiffrement TLS à la connexion entre les serveurs d'e-mail, faute de quoi le message ne sera pas envoyé. Mailbox.org prend également en charge [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) en plus des protocoles d'accès standard comme IMAP et POP3.

Mailbox.org dispose d'une fonction d'héritage numérique pour toutes les offres. You can choose whether you want any of your data to be passed to heirs, providing that they apply and provide your testament. Vous pouvez également désigner une personne par son nom et son adresse.

## D'autres fournisseurs

Ces fournisseurs stockent vos e-mails avec un chiffrement à connaissance zéro, ce qui en fait d'excellentes options pour assurer la sécurité de vos e-mails stockés. Cependant, ils ne prennent pas en charge les normes de chiffrement interopérables pour des communications E2EE entre fournisseurs.

<div class="grid cards" markdown>

- ![logo Tuta](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![logo Tuta](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (formerly *Tutanota*) is an email service with a focus on security and privacy through the use of encryption. Tuta est en activité depuis 2011 et est basée à Hanovre, en Allemagne.

Les comptes gratuits commencent avec 1 Go de stockage.

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

Tuta only directly accepts credit cards and PayPal, however [**cryptocurrency**](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with ProxyStore.

#### :material-check:{ .pg-green } Sécurité du compte

Tuta supports [two-factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Sécurité des données

Tuta has [zero-access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). Cela signifie que les messages et autres données stockés dans votre compte ne sont lisibles que par vous.

#### :material-information-outline:{ .pg-blue } Chiffrement des e-mails

Tuta [n'utilise pas OpenPGP](https://tuta.com/support/#pgp). Les comptes Tuta ne peuvent recevoir des e-mails chiffrés provenant de comptes e-mail non Tuta que s'ils sont envoyés via une [boîte mail temporaire Tuta](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Résiliation du compte

Tuta supprimera [les comptes gratuits inactifs](https://tuta.com/support#inactive-accounts) après six mois. Vous pouvez réutiliser un compte gratuit désactivé si vous payez.

#### :material-information-outline:{ .pg-blue } Fonctionnalités supplémentaires

Tuta offre la version professionnelle de [Tuta aux organisations à but non lucratif](https://tuta.com/blog/secure-email-for-non-profit) gratuitement ou avec une forte réduction.

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des fournisseurs que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour tout fournisseur d'e-mail souhaitant être recommandé, y compris la mise en place des bonnes pratiques du secteur, une technologie moderne et bien plus. Nous vous suggérons de vous familiariser avec cette liste avant de choisir un fournisseur d'e-mail, et de mener vos propres recherches pour vous assurer que le fournisseur d'e-mail que vous choisissez est le bon choix pour vous.

### Technologie

Nous considérons ces caractéristiques comme importantes afin de fournir un service sûr et optimal. Vous devez vous demander si le fournisseur possède les caractéristiques dont vous avez besoin.

**Minimum pour se qualifier :**

- Must encrypt email account data at rest with zero-access encryption.
- Must be capable of exporting emails as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .EML with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Les noms de domaine personnalisés sont importants pour les utilisateurs car ils leur permettent de conserver leur indépendance du service, au cas où celui-ci tournerait mal ou serait racheté par une autre société qui ne donne pas priorité à la vie privée.
- Must operate on owned infrastructure, i.e. not built upon third-party email service providers.

**Dans le meilleur des cas :**

- Should encrypt all account data (contacts, calendars, etc.) at rest with zero-access encryption.
- Should provide integrated webmail E2EE/PGP encryption as a convenience.
- Should support WKD to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key with this command: `gpg --locate-key example_user@example.com`.
- Prise en charge d'une boîte mail temporaire pour les utilisateurs externes. This is useful when you want to send an encrypted email without sending an actual copy to your recipient. Ces e-mails ont généralement une durée de vie limitée et sont ensuite automatiquement supprimés. Ils n'obligent pas non plus le destinataire à configurer un système de chiffrement comme OpenPGP.
- Should support [sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Should allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Les noms de domaine personnalisés sont importants pour les utilisateurs car ils leur permettent de conserver leur indépendance du service, au cas où celui-ci tournerait mal ou serait racheté par une autre société qui ne donne pas priorité à la vie privée.
- Catch-all or alias functionality for those who use their own domains.
- Should use standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.
- Email provider's services should be available via an [onion service](https://en.wikipedia.org/wiki/.onion).

### Confidentialité

Nous préférons que nos prestataires recommandés collectent le moins de données possible.

**Minimum pour se qualifier :**

- Must protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Must not require personally identifiable information (PII) besides a username and a password.
- Privacy policy must meet the requirements defined by the GDPR.

**Dans le meilleur des cas :**

- Should accept [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Should be hosted in a jurisdiction with strong email privacy protection laws.

### Sécurité

Email servers deal with a lot of very sensitive data. We expect that providers will adopt industry best practices in order to protect their customers.

**Minimum pour se qualifier :**

- Protection of webmail with 2FA, such as [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Zero-access encryption, which builds on encryption at rest. Le fournisseur ne dispose pas des clés de déchiffrement des données qu'il détient. Cela permet d'éviter qu'un employé malhonnête ne divulgue les données auxquelles il a accès ou qu'un adversaire distant ne divulgue les données qu'il a volées en obtenant un accès non autorisé au serveur.
- Prise en charge de [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions).
- Aucune erreurs ou vulnérabilités TLS lors du profilage par des outils tels que [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), ou [Qualys SSL Labs](https://ssllabs.com/ssltest); cela inclut les erreurs liées aux certificats et les paramètres DH faibles, tels que ceux qui ont conduit à [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLS 1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- Une politique valide [MTA-STS](https://tools.ietf.org/html/rfc8461) et [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Des enregistrements [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) valides.
- Des enregistrements [SPF](https://fr.wikipedia.org/wiki/Sender_Policy_Framework) et [DKIM](https://fr.wikipedia.org/wiki/DomainKeys_Identified_Mail) valides.
- Must have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. Si l'authentification DMARC est utilisée, la politique doit être définie comme suit : `reject` ou `quarantine`.
- Une préférence pour une suite de serveur TLS 1.2 ou plus récente et un plan pour [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- Une soumission [SMTPS](https://en.wikipedia.org/wiki/SMTPS), en supposant que le SMTP est utilisé.
- Des normes de sécurité des sites web telles que :
    - [HTTP Strict Transport Security](https://fr.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - Une [Intégrité des sous-ressources](https://en.wikipedia.org/wiki/Subresource_Integrity) si des éléments sont chargés depuis des domaines externes.
- Must support viewing of [message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**Dans le meilleur des cas :**

- Should support hardware authentication, i.e. U2F and [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- Un [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) en plus de la prise en charge de DANE.
- Should implement [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Published security audits from a reputable, third-party firm.
- Des programmes de primes aux bugs et/ou un processus coordonné de divulgation des vulnérabilités.
- Des normes de sécurité des sites web telles que :
    - [Content Security Policy (CSP)](https://fr.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Confiance

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? Nous exigeons de nos fournisseurs recommandés qu'ils rendent public leur propriété ou leur direction. Nous aimerions également voir des rapports de transparence fréquents, notamment en ce qui concerne la manière dont les demandes de gouvernement sont traitées.

**Minimum pour se qualifier :**

- Une direction ou un propriétaire public.

**Dans le meilleur des cas :**

- Rapports de transparence fréquents.

### Marketing

With the email providers we recommend, we like to see responsible marketing.

**Minimum pour se qualifier :**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.).
- Must not have any irresponsible marketing, which can include the following:
    - Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
    - Guarantees of protecting anonymity 100%. When someone makes a claim that something is 100%, it means there is no certainty for failure. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:
        - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software such as Tor
        - [Empreinte numérique des navigateurs](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Dans le meilleur des cas :**

- Clear and easy-to-read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### Fonctionnalités supplémentaires

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
