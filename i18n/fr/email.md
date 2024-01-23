---
meta_title: "Recommandations de fournisseurs d'e-mail privés et chiffrés - Privacy Guides"
title: "Services d'e-mail"
icon: material/email
description: Ces fournisseurs d'e-mail constituent un excellent moyen de stocker vos e-mails en toute sécurité, et nombre d'entre eux proposent un système de chiffrement OpenPGP interopérable avec d'autres fournisseurs.
cover: email.webp
---

L'e-mail est pratiquement une nécessité pour utiliser n'importe quel service en ligne, mais nous ne le recommandons pas pour les conversations de particulier à particulier. Plutôt que d'utiliser l'e-mail pour contacter d'autres personnes, envisagez d'utiliser un support de messagerie instantanée qui prend en charge la confidentialité persistante.

[Messageries instantanées recommandées](real-time-communication.md ""){.md-button}

Pour tout le reste, nous recommandons une variété de fournisseurs d'email en fonction de la viabilité de leur modèle économique et de leurs fonctions intégrées de sécurité et de confidentialité.

- [Fournisseurs d'e-mails compatibles avec OpenPGP :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [Autres fournisseurs chiffrés :material-arrow-right-drop-circle:](#more-providers)
- [Services d'alias d'e-mail :material-arrow-right-drop-circle:](#email-aliasing-services)
- [Options d'auto-hébergement :material-arrow-right-drop-circle:](#self-hosting-email)

## Services compatibles avec OpenPGP

Ces fournisseurs prennent en charge nativement le chiffrement/déchiffrement OpenPGP et la norme [Web Key Directory](basics/email-security.md#what-is-the-web-key-directory-standard), ce qui permet d'obtenir des e-mails E2EE indépendamment du fournisseur. Par exemple, un utilisateur de Proton Mail peut envoyer un message E2EE à un utilisateur de Mailbox.org, ou vous pouvez recevoir des notifications chiffrées par OpenPGP de la part de services internet qui le supportent.

<div class="grid cards" markdown>

- ![logo Proton Mail](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![logo Skiff Mail](assets/img/email/skiff-mail.svg){ .twemoji } [Skiff Mail](email.md#skiff-mail)
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

**Proton Mail** est un service d'e-mail qui met l'accent sur la confidentialité, le chiffrement, la sécurité et la facilité d'utilisation. Il est en activité depuis **2013**. Proton AG a son siège à Genève, en Suisse. Les comptes commencent avec 500 Mo de stockage avec leur offre gratuite.

[:octicons-home-16: Page d'accueil](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Service onion" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
- [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Les comptes gratuits présentent certaines limitations, comme le fait de ne pas pouvoir effectuer de recherche dans le corps du texte et de ne pas avoir accès à [Proton Mail Bridge](https://proton.me/mail/bridge), qui est nécessaire pour utiliser un [client d'e-mail de bureau recommandé](email-clients.md) (par exemple Thunderbird). Les comptes payants comprennent des fonctionnalités telles que Proton Mail Bridge, un espace de stockage supplémentaire et la prise en charge de domaines personnalisés. Une [lettre d'attestation](https://proton.me/blog/security-audit-all-proton-apps) a été fournie pour les applications de Proton Mail le 9 novembre 2021 par [Securitum](https://research.securitum.com).

Si vous avez l'offre Proton Illimité, Entreprise ou Visionnaire, vous obtenez également [SimpleLogin](#simplelogin) Premium gratuitement.

Proton Mail dispose de rapports de plantages internes qu'il **ne partage pas** avec des tiers. Ils peuvent être désactivés dans : **Paramètres** > **Aller à Paramètres** > **Compte** > **Sécurité et confidentialité** > **Envoyer des rapports de crash**.

#### :material-check:{ .pg-green } Domaines personnalisés et alias

Les abonnés payants à Proton Mail peuvent utiliser leur propre domaine avec le service ou une adresse [fourre-tout](https://proton.me/support/catch-all). Proton Mail prend également en charge le [sous-adressage](https://proton.me/support/creating-aliases), ce qui est utile pour les personnes qui ne souhaitent pas acheter un domaine.

#### :material-check:{ .pg-green } Modes de paiement privés

Proton Mail [accepte](https://proton.me/support/payment-options) les paiements en espèces par courrier, ainsi que les paiements par carte de crédit/débit, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc)et PayPal.

#### :material-check:{ .pg-green } Sécurité du compte

Proton Mail prend en charge [l'authentification à deux facteurs](https://proton.me/support/two-factor-authentication-2fa) TOTP et les [clés de sécurité matérielles](https://proton.me/support/2fa-security-key) en utilisant les normes FIDO2 ou U2F. L'utilisation d'une clé de sécurité matérielle nécessite la mise en place préalable d'une authentification à deux facteurs TOTP.

#### :material-check:{ .pg-green } Sécurité des données

Proton Mail dispose d'un [chiffrement à accès zéro](https://proton.me/blog/zero-access-encryption) au repos pour vos e-mails et [calendriers](https://proton.me/news/protoncalendar-security-model). Les données sécurisées par un chiffrement à accès zéro ne sont accessibles que par vous.

Certaines informations stockées dans [Proton Contacts](https://proton.me/support/proton-contacts), telles que les noms et les adresses e-mail, ne sont pas sécurisées par un chiffrement à accès zéro. Les champs de contact qui prennent en charge le chiffrement à accès zéro, comme les numéros de téléphone, sont indiqués par une icône de cadenas.

#### :material-check:{ .pg-green } Chiffrement des e-mails

Proton Mail a [du chiffrement OpenPGP intégré](https://proton.me/support/how-to-use-pgp) dans son interface d'e-mail web. Les e-mails destinés à d'autres comptes Proton Mail sont chiffrés automatiquement, et le chiffrement vers des adresses autres que Proton Mail avec une clé OpenPGP peut être activé facilement dans les paramètres de votre compte. Proton prend également en charge la découverte automatique de clés externes avec le [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Cela signifie que les e-mails envoyés à d'autres fournisseurs qui utilisent WKD, tels que Skiff Mail, seront automatiquement chiffrés avec OpenPGP, sans qu'il soit nécessaire d'échanger manuellement des clés PGP publiques avec vos contacts. Ils vous permettent également de [chiffrer des messages destinés à des adresses non Proton Mail sans OpenPGP](https://proton.me/support/password-protected-emails), sans qu'ils aient besoin de s'inscrire à un compte Proton Mail.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. Cela permet aux personnes qui n'utilisent pas Proton Mail de trouver facilement les clés OpenPGP des comptes Proton Mail, pour un E2EE inter-fournisseurs. Cela ne s'applique qu'aux adresses e-mails se terminant par un domaine Proton, comme @proton.me. Si vous utilisez un domaine personnalisé, vous devez [configurer le WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) séparément.

#### :material-information-outline:{ .pg-blue } Résiliation du compte

Si vous avez un compte payant et que votre [facture est impayée](https://proton.me/support/delinquency) après 14 jours, vous ne pourrez pas accéder à vos données. Après 30 jours, votre compte sera en impayé et ne recevra plus d'e-mail entrant. Vous continuerez à être facturé pendant cette période.

#### :material-information-outline:{ .pg-blue } Fonctionnalités supplémentaires

Proton Mail propose un compte "Illimité" pour 9,99 €/mois, qui permet également d'accéder à Proton VPN en plus de fournir plusieurs comptes, domaines, alias et 500 Go de stockage.

Proton Mail ne propose pas de fonction d'héritage numérique.

### Skiff Mail

<div class="admonition recommendation" markdown>

![logoSkiff Mail](assets/img/email/skiff-mail.svg){ align=right }

**Skiff Mail** est un service d'e-mail web avec E2EE qui a vu le jour en 2020. Il est basé à San Francisco avec des développeurs dans le monde entier. Les comptes commencent avec 10 Go de stockage gratuit.

[:octicons-home-16: Page d'accueil](https://skiff.com/mail){ .md-button .md-button--primary }
[:octicons-eye-16:](https://app.skiff.com/docs/db93c237-84c2-4b2b-9588-19a7cd2cd45a#tyGksN9rkqbo2uGYASxsA6HVLjUoly/wTYK8tncTto8=){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://skiff.com/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/skiff-org/skiff-apps){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: Android](https://play.google.com/store/apps/details?id=com.skemailmobileapp&pli=1)
- [:simple-appstore: iOS](https://apps.apple.com/us/app/skiff-mail/id1619168801)
- [:octicons-browser-16: Web](https://app.skiff.com/mail)

</details>

</div>

Skiff a fait l'objet de quelques [audits](https://skiff.com/transparency) au cours de son développement.

#### :material-check:{ .pg-green } Domaines personnalisés et alias

Vous pouvez créer jusqu'à 3 alias d'e-mail @skiff.com en plus de l'adresse principale de votre compte sur leur plan gratuit. Les comptes gratuits peuvent ajouter 1 [domaine personnalisé](https://skiff.com/blog/custom-domain-setup) et jusqu'à 15 domaines personnalisés avec une offre payante. Vous pouvez créer un nombre illimité d'alias ou un [alias fourre-tout](https://skiff.com/blog/catch-all-email-alias) sur votre domaine personnalisé.

#### :material-alert-outline:{ .pg-orange } Modes de paiement privés

Skiff Mail accepte les paiements en crypto-monnaie via Coinbase Commerce, y compris Bitcoin et Ethereum, mais ils n'acceptent pas notre [crypto-monnaie](cryptocurrency.md) recommandée, Monero. Ils acceptent également les paiements par carte de crédit via Stripe.

#### :material-check:{ .pg-green } Sécurité du compte

Skiff Mail prend en charge l'authentification à deux facteurs TOTP et les clés de sécurité matérielles utilisant les normes FIDO2 ou U2F. L'utilisation d'une clé de sécurité matérielle nécessite la mise en place préalable d'une authentification à deux facteurs TOTP.

#### :material-check:{ .pg-green } Sécurité des données

Skiff Mail dispose d'un chiffrement à accès zéro au repos pour toutes vos données. Cela signifie que les messages et autres données stockés dans votre compte ne sont lisibles que par vous.

#### :material-check:{ .pg-green } Chiffrement des e-mails

Skiff Mail encrypts messages to other Skiff mailboxes automatically with E2EE. On December 18th, 2023, Skiff added support for PGP and automatic public key discovery via Web Key Directory (WKD). This means that emails sent to other providers which use WKD, such as Proton Mail, will be automatically encrypted with OpenPGP as well without the need to exchange public PGP keys with your contacts. New Skiff Mail accounts should have a PGP key automatically generated, while accounts from before this feature was introduced need to generate a new PGP key for their address (or upload an existing private key) in the account's address settings. Skiff Mail only has support for reading messages encrypted with PGP/MIME, not the older PGP/Inline standard. Sending messages with PGP/MIME is the [recommended approach](https://www.gnupg.org/faq/gnupg-faq.html#use_pgpmime), but may pose compatibility issues in some edge cases.

Skiff Mail also publishes the public keys of Skiff Mail accounts via HTTP from their [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This allows people who don't use Skiff Mail to find the OpenPGP keys of Skiff Mail accounts easily, for cross-provider E2EE. This only applies to email addresses ending in one of Skiff's own domains, like @skiff.com. Si vous utilisez un domaine personnalisé, vous devez [configurer le WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) séparément.

Skiff does not have a "temporary inbox" or "passworded email" feature like some other providers have, so that external users without OpenPGP cannot receive or reply to messages with E2EE.

#### :material-information-outline:{ .pg-blue } Résiliation du compte

Les comptes Skiff Mail n'expirent pas, mais les comptes non payés seront invités à supprimer les fonctions payantes activées (telles que les alias supplémentaires) ou à renouveler leur plan avant que le compte ne puisse être utilisé.

#### :material-information-outline:{ .pg-blue } Fonctionnalités supplémentaires

Skiff offre en outre des [fonctions de productivité de l'espace de travail](https://discuss.privacyguides.net/t/skiff-pages-drive-productivity-tools/11758/13), mais nous préférons pour l'instant [d'autres](productivity.md) options pour la collaboration et le partage de fichiers.

Skiff Mail ne propose pas de fonction d'héritage numérique.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Logo de Mailbox.org](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** est un service d'e-mail qui se veut sécurisé, sans publicité et alimenté par une énergie 100% écologique. Il est en activité depuis 2014. Mailbox.org est basé à Berlin, en Allemagne. Les comptes commencent avec 2 Go de stockage, qui peuvent être mis à niveau si nécessaire.

[:octicons-home-16: Page d'accueil](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Domaines personnalisés et alias

Mailbox.org vous permet d'utiliser votre propre domaine et prend en charge les adresses [fourre-tout](https://kb.mailbox.org/display/MBOKBEN/Using+catch-all+alias+with+own+domain). Mailbox.org prend également en charge le [sous-adressage](https://kb.mailbox.org/display/BMBOKBEN/What+is+an+alias+and+how+do+I+use+it), ce qui est utile pour les personnes qui ne souhaitent pas acheter un domaine.

#### :material-check:{ .pg-green } Modes de paiement privés

Mailbox.org n'accepte aucune crypto-monnaie en raison de la suspension des activités de son processeur de paiement BitPay en Allemagne. Cependant, ils acceptent les paiements en espèces par courrier, les paiements en espèces sur compte bancaire, les virements bancaires, les cartes de crédit, PayPal et quelques processeurs spécifiques à l'Allemagne : paydirekt et Sofortüberweisung.

#### :material-check:{ .pg-green } Sécurité du compte

Mailbox.org prend en charge l'[authentification à deux facteurs](https://kb.mailbox.org/display/MBOKBEN/How+to+use+two-factor+authentication+-+2FA) pour son interface d'e-mail web uniquement. Vous pouvez utiliser soit TOTP, soit une [YubiKey](https://fr.wikipedia.org/wiki/YubiKey) via le [YubiCloud](https://www.yubico.com/products/services-software/yubicloud). Les normes web telles que [WebAuthn](https://fr.wikipedia.org/wiki/WebAuthn) ne sont pas encore prises en charge.

#### :material-information-outline:{ .pg-blue } Sécurité des données

Mailbox.org permet le chiffrement des e-mails entrant à l'aide de sa [boîte mails chiffrée](https://kb.mailbox.org/display/MBOKBEN/The+Encrypted+Mailbox). Les nouveaux messages que vous recevrez seront alors immédiatement chiffrés avec votre clé publique.

Cependant, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), la plateforme logicielle utilisée par Mailbox.org, [ne prend pas en charge](https://kb.mailbox.org/display/BMBOKBEN/Encryption+of+calendar+and+address+book) le chiffrement de votre carnet d'adresses et de votre calendrier. Une [option tierce](calendar.md) pourrait être plus appropriée pour ces informations.

#### :material-check:{ .pg-green } Chiffrement des e-mails

Mailbox.org a [du chiffrement intégré](https://kb.mailbox.org/display/MBOKBEN/Send+encrypted+e-mails+with+Guard) dans son interface d'e-mail web, ce qui simplifie l'envoi de messages à des personnes possédant des clés OpenPGP publiques. Ils permettent également aux [destinataires distants de déchiffrer un e-mail](https://kb.mailbox.org/display/MBOKBEN/My+recipient+does+not+use+PGP) sur les serveurs de Mailbox.org. Cette fonction est utile lorsque le destinataire distant ne dispose pas d'OpenPGP et ne peut pas déchiffrer une copie de l'e-mail dans sa propre boîte mail.

Mailbox.org prend également en charge la découverte de clés publiques via HTTP à partir de leur [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Cela permet aux personnes extérieures à Mailbox.org de trouver facilement les clés OpenPGP des comptes Mailbox.org, pour un E2EE inter-fournisseurs. Cela ne s'applique qu'aux adresses e-mails se terminant par un domaine Mailbox, comme @mailbox.org. Si vous utilisez un domaine personnalisé, vous devez [configurer le WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) séparément.

#### :material-information-outline:{ .pg-blue } Résiliation du compte

Votre compte sera défini comme un compte d'utilisateur restreint à la fin de votre contrat, après [30 jours, il sera irrévocablement supprimé](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Fonctionnalités supplémentaires

Vous pouvez accéder à votre compte Mailbox.org via IMAP/SMTP en utilisant leur [service .onion](https://kb.mailbox.org/display/MBOKBEN/The+Tor+exit+node+of+mailbox.org). Cependant, leur interface d'e-mail web n'est pas accessible via leur service .onion et vous pouvez rencontrer des erreurs de certificat TLS.

Tous les comptes sont assortis d'un espace de stockage cloud limité qui [peut être chiffré](https://kb.mailbox.org/display/MBOKBEN/Encrypt+files+on+your+Drive). Mailbox.org propose également l'alias [@secure.mailbox.org](https://kb.mailbox.org/display/MBOKBEN/Ensuring+E-Mails+are+Sent+Securely), qui applique le chiffrement TLS à la connexion entre les serveurs d'e-mail, faute de quoi le message ne sera pas envoyé. Mailbox.org prend également en charge [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) en plus des protocoles d'accès standard comme IMAP et POP3.

Mailbox.org dispose d'une fonction d'héritage numérique pour toutes les offres. Vous pouvez choisir de transmettre certaines de vos données à vos héritiers, à condition d'en faire la demande et de fournir votre testament. Vous pouvez également désigner une personne par son nom et son adresse.

## D'autres fournisseurs

Ces fournisseurs stockent vos e-mails avec un chiffrement à connaissance zéro, ce qui en fait d'excellentes options pour assurer la sécurité de vos e-mails stockés. Cependant, ils ne prennent pas en charge les normes de chiffrement interopérables pour des communications E2EE entre fournisseurs.

<div class="grid cards" markdown>

- ![Logo Tuta](assets/img/email/tuta.svg){ .twemoji } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Logo Tuta](assets/img/email/tuta.svg){ align=right }

**Tuta** est un service d'e-mail qui met l'accent sur la sécurité et la confidentialité grâce à l'utilisation du chiffrement. Tuta est en activité depuis **2011** et est basée à Hanovre, en Allemagne. Les comptes commencent avec 1 Go de stockage avec leur offre gratuite.

[:octicons-home-16: Page d'accueil](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://tuta.com/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Code source" }
[:octicons-heart-16:](https://tuta.com/community/){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/tutanota/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:simple-windows11: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com/)

</details>

</div>

Tuta ne prend pas en charge le [protocole IMAP](https://tuta.com/faq/#imap) ni l'utilisation de [clients d'e-mail](email-clients.md) tiers, et vous ne pourrez pas non plus ajouter [des comptes e-mail externes](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) à l'application Tuta. L'[import d'e-mails](https://github.com/tutao/tutanota/issues/630) n'est pas pris en charge non plus pour le moment, bien que cela soit [amené à changer](https://tuta.com/blog/posts/kickoff-import). Les e-mails peuvent être exportés [individuellement ou par sélection groupée](https://tuta.com/howto#generalMail) par dossier, ce qui peut s'avérer peu pratique si vous avez de nombreux dossiers.

#### :material-check:{ .pg-green } Domaines personnalisés et alias

Les comptes Tuta payants peuvent utiliser 15 ou 30 alias en fonction de leur offre et un nombre illimité d'alias sur [domaines personnalisés](https://tuta.com/faq#custom-domain). Tuta ne permet pas le [sous-adressage (adresses plus)](https://tuta.com/faq#plus), mais vous pouvez utiliser une adresse [fourre-tout](https://tuta.com/howto#settings-global) avec un domaine personnalisé.

#### :material-information-outline:{ .pg-blue } Modes de paiement privés

Tuta n'accepte directement que les cartes de crédit et PayPal, mais [les crypto-monnaies](cryptocurrency.md) peuvent être utilisées pour acheter des cartes-cadeaux grâce à leur [partenariat](https://tuta.com/faq/#cryptocurrency) avec Proxystore.

#### :material-check:{ .pg-green } Sécurité du compte

Tuta prend en charge l'[authentification à deux facteurs](https://tuta.com/faq#2fa) avec TOTP ou U2F.

#### :material-check:{ .pg-green } Sécurité des données

Tuta dispose d'un [chiffrement accès zéro au repos](https://tuta.com/faq#what-encrypted) pour vos e-mails, vos [contacts de carnet d'addresse](https://tuta.com/faq#encrypted-address-book), et vos [calendriers](https://tuta.com/faq#calendar). Cela signifie que les messages et autres données stockés dans votre compte ne sont lisibles que par vous.

#### :material-information-outline:{ .pg-blue } Chiffrement des e-mails

Tuta [n'utilise pas OpenPGP](https://tuta.com/support/#pgp). Les comptes Tuta ne peuvent recevoir des e-mails chiffrés provenant de comptes e-mail non Tuta que s'ils sont envoyés via une [boîte mail temporaire Tuta](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Résiliation du compte

Tuta supprimera [les comptes gratuits inactifs](https://tuta.com/faq#inactive-accounts) après six mois. Vous pouvez réutiliser un compte gratuit désactivé si vous payez.

#### :material-information-outline:{ .pg-blue } Fonctionnalités supplémentaires

Tuta offre la version professionnelle de [Tuta aux organisations à but non lucratif](https://tuta.com/blog/posts/secure-email-for-non-profit) gratuitement ou avec une forte réduction.

Tuta dispose également d'une fonction commerciale appelée [Secure Connect](https://tuta.com/secure-connect/). Cela garantit que le contact du client avec l'entreprise utilise E2EE. La fonctionnalité coûte 240 €/an.

Tuta ne propose pas de fonction d'héritage numérique.

## Services d'alias d'e-mails

Un service d'alias d'e-mails vous permet de générer facilement une nouvelle adresse e-mail pour chaque site web auquel vous vous inscrivez. Les alias que vous créez sont ensuite transférés vers une adresse e-mail de votre choix, ce qui permet de masquer à la fois votre adresse e-mail "principale" et l'identité de votre fournisseur d'e-mail. Un véritable alias d'e-mail est mieux que l'adressage plus, couramment utilisé et pris en charge par de nombreux fournisseurs, qui vous permet de créer des alias tels que votrenom+[nimportequoiici]@exemple.fr, car les sites web, les annonceurs et les réseaux de pistage peuvent trivialement supprimer tout ce qui suit le signe + pour connaître votre véritable adresse e-mail.

<div class="grid cards" markdown>

- ![logo addy.io](assets/img/email/mini/addy.svg){ .twemoji } [addy.io](email.md#addyio)
- ![logo SimpleLogin](assets/img/email/simplelogin.svg){ .twemoji } [SimpleLogin](email.md#simplelogin)

</div>

L'alias d'e-mail peut servir de protection au cas où votre fournisseur d'e-mail cesserait de fonctionner. Dans ce cas, vous pouvez facilement rediriger vos alias vers une nouvelle adresse e-mail. En revanche, vous faites confiance au service d'alias pour qu'il continue de fonctionner.

L'utilisation d'un service d'alias d'e-mail dédié présente également un certain nombre d'avantages par rapport à un alias fourre-tout sur un domaine personnalisé :

- Les alias peuvent être activés et désactivés individuellement lorsque vous en avez besoin, ce qui empêche les sites web de vous envoyer des e-mails de façon aléatoire.
- Les réponses sont envoyées à partir de l'adresse alias, qui masque votre véritable adresse e-mail.

Ils présentent également un certain nombre d'avantages par rapport aux services qui fournissent des "e-mails temporaires" :

- Les alias sont permanents et peuvent être réactivés si vous devez recevoir quelque chose comme une réinitialisation de mot de passe.
- Les e-mails sont envoyés à votre boîte mail de confiance plutôt que d'être stockés par le fournisseur d'alias.
- Les services d'e-mails temporaires proposent généralement des boîtes mail publiques auxquelles peuvent accéder tous ceux qui connaissent l'adresse, tandis que les alias sont privés.

Nos recommandations en matière d'alias d'e-mail sont des fournisseurs qui vous permettent de créer des alias sur des domaines qu'ils contrôlent, ainsi que sur votre ou vos propres domaine(s) personnalisé(s), pour un coût annuel modeste. Ils peuvent également être auto-hébergés si vous souhaitez un contrôle maximal. Toutefois, l'utilisation d'un domaine personnalisé peut présenter des inconvénients en matière de confidentialité : Si vous êtes la seule personne à utiliser votre domaine personnalisé, vos actions peuvent être facilement suivies sur les sites web en regardant simplement le nom de domaine dans l'adresse e-mail et en ignorant tout ce qui se trouve avant le signe arobase (@).

L'utilisation d'un service d'alias nécessite de faire confiance à la fois à votre fournisseur d'e-mail et à votre fournisseur d'alias pour vos messages non chiffrés. Certains fournisseurs atténuent légèrement ce problème grâce au chiffrement automatique PGP, qui réduit le nombre de services auxquels vous devez faire confiance de deux à un en chiffrant les e-mails entrants avant qu'ils ne soient remis à votre fournisseur de boîte mail final.

### addy.io

<div class="admonition recommendation" markdown>

![logo addy.io](assets/img/email/addy.svg#only-light){ align=right }
![logo addy.io](assets/img/email/addy-dark.svg#only-dark){ align=right }

**addy.io** vous permet de créer gratuitement 10 alias de domaine sur un domaine partagé, ou un nombre illimité d'alias "standard" qui sont moins anonymes.

[:octicons-home-16: Page d'accueil](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://app.addy.io/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Code source" }
[:octicons-heart-16:](https://addy.io/donate){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: Android](https://addy.io/faq/#is-there-an-android-app)
- [:material-apple-ios: iOS](https://addy.io/faq/#is-there-an-ios-app)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/addy_io/)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/addyio-anonymous-email-fo/iadbdpnoknmbdeolbapdackdcogdmjpe)

</details>

</div>

Le nombre d'alias partagés (qui se terminent par un domaine partagé comme @addy.io) que vous pouvez créer est limité à 10 sur l'offre gratuite d'addy.io, à 50 sur leur offre à $1/mois et illimité sur leur offre à $4/mois (facturé $3 pour un an). Vous pouvez créer un nombre illimité d'alias standard (qui se terminent par un domaine tel que @[nomdutilisateur].addy.io ou un domaine personnalisé sur les offres payantes), mais, comme nous l'avons déjà mentionné, cela peut nuire à la confidentialité car les gens peuvent trivialement relier vos alias standard en se basant sur le seul nom de domaine. Ils sont utiles lorsqu'un domaine partagé peut être bloqué par un service. Securitum [a audité](https://addy.io/blog/addy-io-passes-independent-security-audit/) addy.io en septembre 2023 et aucune vulnérabilité significative [n'a été identifiée](https://addy.io/addy-io-security-audit.pdf).

Fonctions gratuites notables :

- [x] 10 Alias partagés
- [x] Alias standard illimités
- [ ] Pas de réponses sortantes
- [x] 1 Boîte mail de réception
- [x] Chiffrement automatique PGP

### SimpleLogin

<div class="admonition recommendation" markdown>

![Logo Simplelogin](assets/img/email/simplelogin.svg){ align=right }

**SimpleLogin** est un service gratuit qui fournit des alias d'e-mail sur une variété de noms de domaine partagés, et offre en option des fonctionnalités payantes comme des alias illimités et des domaines personnalisés.

[:octicons-home-16: Page d'accueil](https://simplelogin.io/fr/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplelogin.io/privacy/){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://simplelogin.io/docs/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simple-login){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
- [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/simplelogin/)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
- [:simple-safari: Safari](https://apps.apple.com/app/id1494051017)

</details>

</div>

SimpleLogin a été [acquis par Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) à compter du 8 avril 2022. Si vous utilisez Proton Mail pour votre boîte mail principale, SimpleLogin est un excellent choix. Les deux produits étant désormais détenus par la même société, vous ne devez plus faire confiance qu'à une seule entité. Nous supposons également que SimpleLogin sera plus étroitement intégré aux offres de Proton à l'avenir. SimpleLogin continue de prendre en charge la redirection vers le fournisseur d'e-mail de votre choix. Securitum [a audité](https://simplelogin.io/blog/security-audit/) SimpleLogin début 2022 et tous les problèmes [ont été résolus](https://simplelogin.io/audit2022/web.pdf).

Vous pouvez lier votre compte SimpleLogin avec votre compte Proton dans les paramètres de SimpleLogin. Si vous avez l'offre Proton Illimité, Entreprise, ou Visionnaire, vous aurez SimpleLogin Premium gratuitement.

Fonctions gratuites notables :

- [x] 10 Alias partagés
- [x] Réponses illimitées
- [x] 1 Boîte mail de réception

## E-mail auto-hébergé

Les administrateurs système peuvent envisager de mettre en place leur propre serveur d'e-mail. Les serveurs d'e-mail requièrent une attention et une maintenance permanente afin de garantir la sécurité et la fiabilité de la distribution des e-mails.

### Solutions logicielles combinées

<div class="admonition recommendation" markdown>

![Logo Mailcow](assets/img/email/mailcow.svg){ align=right }

**Mailcow** est un serveur d'e-mail plus avancé, parfait pour ceux qui ont un peu plus d'expérience de Linux. Il possède tout ce dont vous avez besoin dans un conteneur Docker : un serveur d'e-mail avec prise en charge de DKIM, une surveillance antivirus et spam, une interface d'e-mail web et ActiveSync avec SOGo, et une administration basée sur le web avec prise en charge de l'A2F.

[:octicons-home-16: Page d'accueil](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailcow.github.io/mailcow-dockerized-docs/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Code source" }
[:octicons-heart-16:](https://www.servercow.de/mailcow?lang=en#sal){ .card-link title=Contribuer }

</div>

<div class="admonition recommendation" markdown>

![Logo Mail-in-a-Box](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** est un script de configuration automatisé pour le déploiement d'un serveur d'e-mail sur Ubuntu. Son objectif est de faciliter la mise en place de son propre serveur d'e-mail.

[:octicons-home-16: Page d'accueil](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Code source" }

</div>

Pour une approche plus manuelle, nous avons choisi ces deux articles :

- [Configuration d'un serveur mail avec OpenSMTPD, Dovecot et Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd/) (2019)
- [Comment gérer votre propre serveur d'e-mail](https://www.c0ffee.net/blog/mail-server-guide/) (août 2017)

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des fournisseurs que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour tout fournisseur d'e-mail souhaitant être recommandé, y compris la mise en place des bonnes pratiques du secteur, une technologie moderne et bien plus. Nous vous suggérons de vous familiariser avec cette liste avant de choisir un fournisseur d'e-mail, et de mener vos propres recherches pour vous assurer que le fournisseur d'e-mail que vous choisissez est le bon choix pour vous.

### Technologie

Nous considérons ces caractéristiques comme importantes afin de fournir un service sûr et optimal. Vous devez vous demander si le fournisseur possède les caractéristiques dont vous avez besoin.

**Minimum pour se qualifier :**

- Chiffre les données du compte e-mail au repos avec un chiffrement à accès zéro.
- Capacité d'export en tant que [Mbox](https://en.wikipedia.org/wiki/Mbox) ou .eml individuel avec standard [RFC5322](https://datatracker.ietf.org/doc/rfc5322/).
- Permet aux utilisateurs d'utiliser leur propre [nom de domaine](https://en.wikipedia.org/wiki/Domain_name). Les noms de domaine personnalisés sont importants pour les utilisateurs car ils leur permettent de conserver leur indépendance du service, au cas où celui-ci tournerait mal ou serait racheté par une autre société qui ne donne pas priorité à la vie privée.
- Fonctionne sur sa propre infrastructure, c'est-à-dire qu'elle ne repose pas sur des fournisseurs de services d'e-mail tiers.

**Dans le meilleur des cas :**

- Chiffre toutes les données du compte (contacts, calendriers, etc.) au repos avec un chiffrement à accès zéro.
- Une interface d'e-mail web intégrée avec chiffrement E2EE/PGP est fournie à titre de commodité.
- Prise en charge de [WKD](https://wiki.gnupg.org/WKD) pour permettre une meilleure découverte des clés publiques OpenPGP via HTTP. Les utilisateurs de GnuPG peuvent obtenir une clé en tapant : `gpg --locate-key utilisateur_exemple@exemple.fr`
- Prise en charge d'une boîte mail temporaire pour les utilisateurs externes. Cette fonction est utile lorsque vous souhaitez envoyer un e-mail chiffré, sans envoyer une copie réelle à votre destinataire. Ces e-mails ont généralement une durée de vie limitée et sont ensuite automatiquement supprimés. Ils n'obligent pas non plus le destinataire à configurer un système de chiffrement comme OpenPGP.
- Disponibilité des services du fournisseur d'e-mail via un [service onion](https://en.wikipedia.org/wiki/.onion).
- Prise en charge du [sous-adressage](https://en.wikipedia.org/wiki/Email_address#Subaddressing).
- Fonctionnalité fourre-tout ou alias pour ceux qui possèdent leurs propres domaines.
- Utilisation de protocoles standard d'accès aux e-mails tels que IMAP, SMTP ou [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Les protocoles d'accès standard garantissent que les clients peuvent facilement télécharger l'ensemble de leurs e-mails, s'ils souhaitent changer de fournisseur.

### Confidentialité

Nous préférons que nos prestataires recommandés collectent le moins de données possible.

**Minimum pour se qualifier :**

- Protéger l'adresse IP de l'expéditeur. Filtrez-la pour qu'elle n'apparaisse pas dans le champ d'en-tête `Received`.
- Ne demandez pas de Données à Caractère Personnel (DCP) en plus d'un nom d'utilisateur et d'un mot de passe.
- Politique de confidentialité répondant aux exigences définies par le RGPD.

**Dans le meilleur des cas :**

- Accepte des [options de paiement anonymes](advanced/payments.md) ([crypto-monnaie](cryptocurrency.md), argent liquide, cartes cadeaux, etc.)
- Hébergé dans une juridiction disposant de lois strictes en matière de protection de la confidentialité des e-mails.

### Sécurité

Les serveurs d'e-mail traitent un grand nombre de données très sensibles. Nous nous attendons à ce que les prestataires adoptent les meilleures pratiques du secteur afin de protéger leurs membres.

**Minimum pour se qualifier :**

- Protection de l'interface d'e-mail web avec une A2F, tel que TOTP.
- Le chiffrement à accès zéro, qui complète le chiffrement au repos. Le fournisseur ne dispose pas des clés de déchiffrement des données qu'il détient. Cela permet d'éviter qu'un employé malhonnête ne divulgue les données auxquelles il a accès ou qu'un adversaire distant ne divulgue les données qu'il a volées en obtenant un accès non autorisé au serveur.
- Prise en charge de [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions).
- Aucune erreurs ou vulnérabilités TLS lors du profilage par des outils tels que [Hardenize](https://www.hardenize.com/), [testssl.sh](https://testssl.sh/), ou [Qualys SSL Labs](https://www.ssllabs.com/ssltest); cela inclut les erreurs liées aux certificats et les paramètres DH faibles, tels que ceux qui ont conduit à [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Une préférence pour les serveurs (facultatif sur TLSv1.3) pour des suites de chiffrement fortes qui prennent en charge la confidentialité persistante et le chiffrement authentifié.
- Une politique valide [MTA-STS](https://tools.ietf.org/html/rfc8461) et [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Des enregistrements [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) valides.
- Des enregistrements [SPF](https://fr.wikipedia.org/wiki/Sender_Policy_Framework) et [DKIM](https://fr.wikipedia.org/wiki/DomainKeys_Identified_Mail) valides.
- Disposer d'un enregistrement et d'une politique [DMARC](https://fr.wikipedia.org/wiki/DMARC) appropriés ou utiliser [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) pour l'authentification. Si l'authentification DMARC est utilisée, la politique doit être définie comme suit : `reject` ou `quarantine`.
- Une préférence pour une suite de serveur TLS 1.2 ou plus récente et un plan pour [RFC8996](https://datatracker.ietf.org/doc/rfc8996/).
- Une soumission [SMTPS](https://en.wikipedia.org/wiki/SMTPS), en supposant que le SMTP est utilisé.
- Des normes de sécurité des sites web telles que :
    - [HTTP Strict Transport Security](https://fr.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - Une [Intégrité des sous-ressources](https://en.wikipedia.org/wiki/Subresource_Integrity) si des éléments sont chargés depuis des domaines externes.
- Doit prendre en charge l'affichage des [en-têtes de message](https://en.wikipedia.org/wiki/Email#Message_header), car il s'agit d'une fonction d'analyse scientifique essentielle pour déterminer si un e-mail est une tentative de hammeçonnage.

**Dans le meilleur des cas :**

- Prise en charge de l'authentification matérielle, à savoir U2F et [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn). U2F et WebAuthn sont plus sûrs car ils utilisent une clé privée stockée sur un dispositif matériel côté client pour authentifier les personnes, par opposition à un secret partagé qui est stocké sur le serveur web et côté client lors de l'utilisation de TOTP. De plus, U2F et WebAuthn sont plus résistants au phishing car leur réponse d'authentification est basée sur le [nom de domaine](https://en.wikipedia.org/wiki/Domain_name) authentifié.
- Un [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) en plus de la prise en charge de DANE.
- Prise en charge de [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), utile pour les personnes qui publient sur des listes de diffusion [RFC8617](https://tools.ietf.org/html/rfc8617).
- Des programmes de primes aux bugs et/ou un processus coordonné de divulgation des vulnérabilités.
- Des normes de sécurité des sites web telles que :
    - [Content Security Policy (CSP)](https://fr.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163/)

### Confiance

Vous ne confieriez pas vos finances à une personne ayant une fausse identité, alors pourquoi lui confier vos e-mails ? Nous exigeons de nos fournisseurs recommandés qu'ils rendent public leur propriété ou leur direction. Nous aimerions également voir des rapports de transparence fréquents, notamment en ce qui concerne la manière dont les demandes de gouvernement sont traitées.

**Minimum pour se qualifier :**

- Une direction ou un propriétaire public.

**Dans le meilleur des cas :**

- Une direction publique.
- Rapports de transparence fréquents.

### Marketing

Avec les fournisseurs d'e-mail que nous recommandons, nous aimons voir un marketing responsable.

**Minimum pour se qualifier :**

- Doit héberger lui-même ses outils d'analyse de traffic (pas de Google Analytics, Adobe Analytics, etc.). Le site du fournisseur doit également se conformer à [DNT (Do Not Track)](https://fr.wikipedia.org/wiki/Do_Not_Track) pour ceux qui souhaitent refuser.

Ne doit pas avoir de marketing irresponsable :

- Prétendre à un "chiffrement incassable". Le chiffrement doit être utilisé en supposant qu'il ne soit plus secret dans le futur, lorsque la technologie existera pour le décrypter.
- Garantir la protection de l'anonymat à 100%. Lorsque quelqu'un prétend que quelque chose est à 100%, cela signifie qu'il n'y a aucune certitude d'échec. Nous savons que les gens peuvent assez facilement se désanonymiser de plusieurs façons, par exemple :

    - Réutiliser des informations personnelles (par exemple comptes d'e-mail, pseudonymes uniques, etc.) auxquelles ils ont eu accès sans logiciel d'anonymat (Tor, VPN, etc.)
    - [La prise d'empreinte numérique des navigateurs](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Dans le meilleur des cas :**

- Une documentation claire et facile à lire. Notamment pour la mise en place de l'A2F, des clients d'e-mail tiers, d'OpenPGP, etc.

### Fonctionnalités supplémentaires

Bien qu'il ne s'agisse pas d'exigences strictes, nous avons pris en compte d'autres facteurs liés à la commodité ou à la confidentialité pour déterminer les fournisseurs à recommander.
