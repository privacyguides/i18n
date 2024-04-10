---
meta_title: "Recommandations de fournisseurs d'e-mail privés et chiffrés - Privacy Guides"
title: "Services d'e-mail"
icon: material/email
description: Ces fournisseurs d'e-mail constituent un excellent moyen de stocker vos e-mails en toute sécurité, et nombre d'entre eux proposent un système de chiffrement OpenPGP interopérable avec d'autres fournisseurs.
cover: email.webp
---

<!-- markdownlint-disable MD024 -->
L'e-mail est pratiquement une nécessité pour utiliser n'importe quel service en ligne, mais nous ne le recommandons pas pour les conversations de particulier à particulier. Plutôt que d'utiliser l'e-mail pour contacter d'autres personnes, envisagez d'utiliser un support de messagerie instantanée qui prend en charge la confidentialité persistante.

[Messageries instantanées recommandées](real-time-communication.md ""){.md-button}

Pour tout le reste, nous recommandons une variété de fournisseurs d'email en fonction de la viabilité de leur modèle économique et de leurs fonctions intégrées de sécurité et de confidentialité.

- [Fournisseurs d'e-mails compatibles avec OpenPGP :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [Autres fournisseurs chiffrés :material-arrow-right-drop-circle:](#more-providers)
- [Options d'auto-hébergement :material-arrow-right-drop-circle:](#self-hosting-email)

In addition to (or instead of) an email provider recommended here, you may wish to consider a dedicated [email aliasing service](email-aliasing.md) to protect your privacy. Among other things, these services can help protect your real inbox from spam, prevent marketers from correlating your accounts, and encrypt all incoming messages with PGP.

- [More Information :material-arrow-right-drop-circle:](email-aliasing.md)

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

**Proton Mail** est un service d'e-mail qui met l'accent sur la confidentialité, le chiffrement, la sécurité et la facilité d'utilisation. Il est en activité depuis **2013**. Proton AG a son siège à Genève, en Suisse. Les comptes commencent avec 500 Mo de stockage avec leur offre gratuite.

[:octicons-home-16: Page d'accueil](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Service onion" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
- [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Les comptes gratuits présentent certaines limitations, comme le fait de ne pas pouvoir effectuer de recherche dans le corps du texte et de ne pas avoir accès à [Proton Mail Bridge](https://proton.me/mail/bridge), qui est nécessaire pour utiliser un [client d'e-mail de bureau recommandé](email-clients.md) (par exemple Thunderbird). Les comptes payants comprennent des fonctionnalités telles que Proton Mail Bridge, un espace de stockage supplémentaire et la prise en charge de domaines personnalisés. Une [lettre d'attestation](https://proton.me/blog/security-audit-all-proton-apps) a été fournie pour les applications de Proton Mail le 9 novembre 2021 par [Securitum](https://research.securitum.com).

If you have the Proton Unlimited, Business, Family, or Visionary Plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

Proton Mail dispose de rapports de plantages internes qu'il **ne partage pas** avec des tiers. Ils peuvent être désactivés dans : **Paramètres** > **Aller à Paramètres** > **Compte** > **Sécurité et confidentialité** > **Envoyer des rapports de crash**.

#### :material-check:{ .pg-green } Domaines personnalisés et alias

Les abonnés payants à Proton Mail peuvent utiliser leur propre domaine avec le service ou une adresse [fourre-tout](https://proton.me/support/catch-all). Proton Mail also supports [sub-addressing](https://proton.me/support/creating-aliases), which is useful for people who don't want to purchase a domain.

#### :material-check:{ .pg-green } Modes de paiement privés

Proton Mail [accepte](https://proton.me/support/payment-options) les paiements en espèces par courrier, ainsi que les paiements par carte de crédit/débit, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc)et PayPal.

#### :material-check:{ .pg-green } Sécurité du compte

Proton Mail prend en charge [l'authentification à deux facteurs](https://proton.me/support/two-factor-authentication-2fa) TOTP et les [clés de sécurité matérielles](https://proton.me/support/2fa-security-key) en utilisant les normes FIDO2 ou U2F. L'utilisation d'une clé de sécurité matérielle nécessite la mise en place préalable d'une authentification à deux facteurs TOTP.

#### :material-check:{ .pg-green } Sécurité des données

Proton Mail dispose d'un [chiffrement à accès zéro](https://proton.me/blog/zero-access-encryption) au repos pour vos e-mails et [calendriers](https://proton.me/news/protoncalendar-security-model). Les données sécurisées par un chiffrement à accès zéro ne sont accessibles que par vous.

Certaines informations stockées dans [Proton Contacts](https://proton.me/support/proton-contacts), telles que les noms et les adresses e-mail, ne sont pas sécurisées par un chiffrement à accès zéro. Les champs de contact qui prennent en charge le chiffrement à accès zéro, comme les numéros de téléphone, sont indiqués par une icône de cadenas.

#### :material-check:{ .pg-green } Chiffrement des e-mails

Proton Mail a [du chiffrement OpenPGP intégré](https://proton.me/support/how-to-use-pgp) dans son interface d'e-mail web. Les e-mails destinés à d'autres comptes Proton Mail sont chiffrés automatiquement, et le chiffrement vers des adresses autres que Proton Mail avec une clé OpenPGP peut être activé facilement dans les paramètres de votre compte. Proton prend également en charge la découverte automatique de clés externes avec le [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Cela signifie que les e-mails envoyés à d'autres fournisseurs qui utilisent WKD seront automatiquement chiffrés avec OpenPGP, sans qu'il soit nécessaire d'échanger manuellement des clés PGP publiques avec vos contacts. Ils vous permettent également de [chiffrer des messages destinés à des adresses non Proton Mail sans OpenPGP](https://proton.me/support/password-protected-emails), sans qu'ils aient besoin de s'inscrire à un compte Proton Mail.

Proton Mail publie également les clés publiques des comptes Proton via HTTP à partir de leur WKD. Cela permet aux personnes qui n'utilisent pas Proton Mail de trouver facilement les clés OpenPGP des comptes Proton Mail, pour un E2EE inter-fournisseurs. Cela ne s'applique qu'aux adresses e-mails se terminant par un domaine Proton, comme @proton.me. Si vous utilisez un domaine personnalisé, vous devez [configurer le WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) séparément.

#### :material-information-outline:{ .pg-blue } Résiliation du compte

Si vous avez un compte payant et que votre [facture est impayée](https://proton.me/support/delinquency) après 14 jours, vous ne pourrez pas accéder à vos données. Après 30 jours, votre compte sera en impayé et ne recevra plus d'e-mail entrant. Vous continuerez à être facturé pendant cette période. Proton will [delete inactive free accounts](https://proton.me/support/inactive-accounts) after one year. You **cannot** reuse the email address on a deactivated account.

#### :material-information-outline:{ .pg-blue } Fonctionnalités supplémentaires

Proton Mail propose un compte "Illimité" pour 9,99 €/mois, qui permet également d'accéder à Proton VPN en plus de fournir plusieurs comptes, domaines, alias et 500 Go de stockage.

Proton Mail ne propose pas de fonction d'héritage numérique.

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

Mailbox.org lets you use your own domain, and they support [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) addresses. Mailbox.org also supports [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green } Modes de paiement privés

Mailbox.org n'accepte aucune crypto-monnaie en raison de la suspension des activités de son processeur de paiement BitPay en Allemagne. However, they do accept cash by mail, cash payment to bank account, bank transfer, credit card, PayPal and couple of German-specific processors: paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } Sécurité du compte

Mailbox.org supports [two factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. You can use either TOTP or a [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via the [YubiCloud](https://yubico.com/products/services-software/yubicloud). Les normes web telles que [WebAuthn](https://fr.wikipedia.org/wiki/WebAuthn) ne sont pas encore prises en charge.

#### :material-information-outline:{ .pg-blue } Sécurité des données

Mailbox.org allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Les nouveaux messages que vous recevrez seront alors immédiatement chiffrés avec votre clé publique.

However, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. Une [option tierce](calendar.md) pourrait être plus appropriée pour ces informations.

#### :material-check:{ .pg-green } Chiffrement des e-mails

Mailbox.org has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox.org's servers. Cette fonction est utile lorsque le destinataire distant ne dispose pas d'OpenPGP et ne peut pas déchiffrer une copie de l'e-mail dans sa propre boîte mail.

Mailbox.org prend également en charge la découverte de clés publiques via HTTP à partir de leur [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Cela permet aux personnes extérieures à Mailbox.org de trouver facilement les clés OpenPGP des comptes Mailbox.org, pour un E2EE inter-fournisseurs. Cela ne s'applique qu'aux adresses e-mails se terminant par un domaine Mailbox, comme @mailbox.org. Si vous utilisez un domaine personnalisé, vous devez [configurer le WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) séparément.

#### :material-information-outline:{ .pg-blue } Résiliation du compte

Your account will be set to a restricted user account when your contract ends. It will be irrevocably deleted after [30 days](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Fonctionnalités supplémentaires

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). Cependant, leur interface d'e-mail web n'est pas accessible via leur service .onion et vous pouvez rencontrer des erreurs de certificat TLS.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox.org prend également en charge [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) en plus des protocoles d'accès standard comme IMAP et POP3.

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

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:simple-windows11: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta ne prend pas en charge le [protocole IMAP](https://tuta.com/faq/#imap) ni l'utilisation de [clients d'e-mail](email-clients.md) tiers, et vous ne pourrez pas non plus ajouter [des comptes e-mail externes](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) à l'application Tuta. L'[import d'e-mails](https://github.com/tutao/tutanota/issues/630) n'est pas pris en charge non plus pour le moment, bien que cela soit [amené à changer](https://tuta.com/blog/posts/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/support#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } Domaines personnalisés et alias

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/support#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/support#plus), but you can use a [catch-all](https://tuta.com/support#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } Modes de paiement privés

Tuta n'accepte directement que les cartes de crédit et PayPal, mais [les crypto-monnaies](cryptocurrency.md) peuvent être utilisées pour acheter des cartes-cadeaux grâce à leur [partenariat](https://tuta.com/faq/#cryptocurrency) avec Proxystore.

#### :material-check:{ .pg-green } Sécurité du compte

Tuta supports [two factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Sécurité des données

Tuta has [zero access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). Cela signifie que les messages et autres données stockés dans votre compte ne sont lisibles que par vous.

#### :material-information-outline:{ .pg-blue } Chiffrement des e-mails

Tuta [n'utilise pas OpenPGP](https://tuta.com/support/#pgp). Les comptes Tuta ne peuvent recevoir des e-mails chiffrés provenant de comptes e-mail non Tuta que s'ils sont envoyés via une [boîte mail temporaire Tuta](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Résiliation du compte

Tuta will [delete inactive free accounts](https://tuta.com/support#inactive-accounts) after six months. Vous pouvez réutiliser un compte gratuit désactivé si vous payez.

#### :material-information-outline:{ .pg-blue } Fonctionnalités supplémentaires

Tuta offre la version professionnelle de [Tuta aux organisations à but non lucratif](https://tuta.com/blog/posts/secure-email-for-non-profit) gratuitement ou avec une forte réduction.

Tuta ne propose pas de fonction d'héritage numérique.

## E-mail auto-hébergé

Les administrateurs système peuvent envisager de mettre en place leur propre serveur d'e-mail. Les serveurs d'e-mail requièrent une attention et une maintenance permanente afin de garantir la sécurité et la fiabilité de la distribution des e-mails.

### Solutions logicielles combinées

<div class="admonition recommendation" markdown>

![Logo Mailcow](assets/img/email/mailcow.svg){ align=right }

**Mailcow** est un serveur d'e-mail plus avancé, parfait pour ceux qui ont un peu plus d'expérience de Linux. Il possède tout ce dont vous avez besoin dans un conteneur Docker : un serveur d'e-mail avec prise en charge de DKIM, une surveillance antivirus et spam, une interface d'e-mail web et ActiveSync avec SOGo, et une administration basée sur le web avec prise en charge de l'A2F.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

</div>

<div class="admonition recommendation" markdown>

![Logo Mail-in-a-Box](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** est un script de configuration automatisé pour le déploiement d'un serveur d'e-mail sur Ubuntu. Son objectif est de faciliter la mise en place de son propre serveur d'e-mail.

[:octicons-home-16: Page d'accueil](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Code source" }

</div>

Pour une approche plus manuelle, nous avons choisi ces deux articles :

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://c0ffee.net/blog/mail-server-guide) (August 2017)

## Critères

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an email provider, and conduct your own research to ensure the email provider you choose is the right choice for you.

### Technologie

Nous considérons ces caractéristiques comme importantes afin de fournir un service sûr et optimal. Vous devez vous demander si le fournisseur possède les caractéristiques dont vous avez besoin.

**Minimum pour se qualifier :**

- Chiffre les données du compte e-mail au repos avec un chiffrement à accès zéro.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Permet aux utilisateurs d'utiliser leur propre [nom de domaine](https://en.wikipedia.org/wiki/Domain_name). Les noms de domaine personnalisés sont importants pour les utilisateurs car ils leur permettent de conserver leur indépendance du service, au cas où celui-ci tournerait mal ou serait racheté par une autre société qui ne donne pas priorité à la vie privée.
- Fonctionne sur sa propre infrastructure, c'est-à-dire qu'elle ne repose pas sur des fournisseurs de services d'e-mail tiers.

**Dans le meilleur des cas :**

- Chiffre toutes les données du compte (contacts, calendriers, etc.) au repos avec un chiffrement à accès zéro.
- Une interface d'e-mail web intégrée avec chiffrement E2EE/PGP est fournie à titre de commodité.
- Prise en charge de [WKD](https://wiki.gnupg.org/WKD) pour permettre une meilleure découverte des clés publiques OpenPGP via HTTP. Les utilisateurs de GnuPG peuvent obtenir une clé en tapant : `gpg --locate-key utilisateur_exemple@exemple.fr`
- Prise en charge d'une boîte mail temporaire pour les utilisateurs externes. Cette fonction est utile lorsque vous souhaitez envoyer un e-mail chiffré, sans envoyer une copie réelle à votre destinataire. Ces e-mails ont généralement une durée de vie limitée et sont ensuite automatiquement supprimés. Ils n'obligent pas non plus le destinataire à configurer un système de chiffrement comme OpenPGP.
- Disponibilité des services du fournisseur d'e-mail via un [service onion](https://en.wikipedia.org/wiki/.onion).
- [Sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing) support.
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
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Une préférence pour les serveurs (facultatif sur TLSv1.3) pour des suites de chiffrement fortes qui prennent en charge la confidentialité persistante et le chiffrement authentifié.
- Une politique valide [MTA-STS](https://tools.ietf.org/html/rfc8461) et [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Des enregistrements [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) valides.
- Des enregistrements [SPF](https://fr.wikipedia.org/wiki/Sender_Policy_Framework) et [DKIM](https://fr.wikipedia.org/wiki/DomainKeys_Identified_Mail) valides.
- Disposer d'un enregistrement et d'une politique [DMARC](https://fr.wikipedia.org/wiki/DMARC) appropriés ou utiliser [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) pour l'authentification. Si l'authentification DMARC est utilisée, la politique doit être définie comme suit : `reject` ou `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
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
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

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
