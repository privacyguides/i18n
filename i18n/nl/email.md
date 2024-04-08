---
meta_title: "Aanbevelingen voor versleutelde privé e-mail - Privacy Guides"
title: "Email Diensten"
icon: material/email
description: Deze e-mailproviders bieden een uitstekende plaats om jouw e-mails veilig op te slaan, en vele bieden interoperabele OpenPGP versleuteling met andere providers.
cover: email.webp
---

<!-- markdownlint-disable MD024 -->
E-mail is bijna een noodzaak voor het gebruik van elke online dienst, maar wij raden het niet aan voor gesprekken van persoon tot persoon. In plaats van e-mail te gebruiken om andere mensen te contacteren, kunt u overwegen een instant messenger te gebruiken die forward secrecy ondersteunt.

[Aanbevolen Instant Messengers](real-time-communication.md ""){.md-button}

Voor al het andere raden wij verschillende e-mailproviders aan op basis van duurzame bedrijfsmodellen en ingebouwde beveiligings- en privacyfuncties.

- [OpenPGP-compatibele e-mailproviders :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [Andere versleutelde aanbieders :material-arrow-right-drop-circle:](#more-providers)
- [Zelf-gehoste opties :material-arrow-right-drop-circle:](#self-hosting-email)

In addition to (or instead of) an email provider recommended here, you may wish to consider a dedicated [email aliasing service](email-aliasing.md) to protect your privacy. Among other things, these services can help protect your real inbox from spam, prevent marketers from correlating your accounts, and encrypt all incoming messages with PGP.

- [More Information :material-arrow-right-drop-circle:](email-aliasing.md)

## OpenPGP compatibele diensten

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic E2EE emails. Een Proton Mail-gebruiker zou bijvoorbeeld een E2EE-bericht kunnen sturen naar een Mailbox.org-gebruiker, of je zou OpenPGP-versleutelde meldingen kunnen ontvangen van internetdiensten die dit ondersteunen.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

When using E2EE technology like OpenPGP your email will still have some metadata that is not encrypted in the header of the email, generally including the subject line! Read more about [email metadata](basics/email-security.md#email-metadata-overview).

OpenPGP also does not support Forward secrecy, which means if either your or the recipient's private key is ever stolen, all previous messages encrypted with it will be exposed. [How do I protect my private keys?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** is een e-maildienst met focus op privacy, encryptie, veiligheid en gebruiksgemak. Ze zijn al actief sinds **2013**. Proton AG is gevestigd in Genève, Zwitserland. Accounts beginnen met 500 MB opslagruimte met hun gratis abonnement.

[:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }

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

Gratis accounts hebben enkele beperkingen, zoals het niet kunnen doorzoeken van bodytekst en geen toegang tot [Proton Mail Bridge](https://proton.me/mail/bridge), die nodig is om een [aanbevolen desktop e-mailclient](email-clients.md) (bv. Thunderbird) te gebruiken. Betaalde accounts bevatten functies zoals Proton Mail Bridge, extra opslagruimte en ondersteuning voor aangepaste domeinen. Een [attestatiebrief](https://proton.me/blog/security-audit-all-proton-apps) werd op 9 november 2021 verstrekt voor de apps van Proton Mail door [Securitum](https://research.securitum.com).

If you have the Proton Unlimited, Business, Family, or Visionary Plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

Proton Mail heeft interne crash rapporten die ze **niet** delen met derden. Dit kan worden uitgeschakeld in: **Instellingen** > **Ga naar Instellingen** > **Account** > **Beveiliging en privacy** > **Crashmeldingen versturen**.

#### :material-check:{ .pg-green } Aangepaste domeinen en aliassen

Betaalde Proton Mail abonnees kunnen hun eigen domein met de dienst gebruiken of een [catch-all](https://proton.me/support/catch-all) adres. Proton Mail also supports [sub-addressing](https://proton.me/support/creating-aliases), which is useful for people who don't want to purchase a domain.

#### :material-check:{ .pg-green } Privé betaalmethoden

Proton Mail [accepteert](https://proton.me/support/payment-options) contant geld per post, naast standaard creditcard/debetkaart, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), en PayPal-betalingen.

#### :material-check:{ .pg-green } Accountbeveiliging

Proton Mail ondersteunt TOTP [two factor authentication](https://proton.me/support/two-factor-authentication-2fa) en [hardware security keys](https://proton.me/support/2fa-security-key) met behulp van FIDO2 of U2F standaarden. Voor het gebruik van een hardware beveiligingssleutel moet eerst TOTP tweefactorauthenticatie worden ingesteld.

#### :material-check:{ .pg-green } Gegevensbeveiliging

Proton Mail heeft [zero-access encryptie](https://proton.me/blog/zero-access-encryption) in rust voor jouw e-mails en [agenda's](https://proton.me/news/protoncalendar-security-model). Gegevens die zijn beveiligd met zero-access encryptie zijn alleen voor jouw toegankelijk.

Bepaalde informatie opgeslagen in [Proton Contacts](https://proton.me/support/proton-contacts), zoals namen en e-mailadressen, zijn niet beveiligd met zero-access encryptie. Contact velden die zero-access encryptie ondersteunen, zoals telefoonnummers, worden aangegeven met een hangslot pictogram.

#### :material-check:{ .pg-green } Email encryptie

Proton Mail heeft [OpenPGP encryptie](https://proton.me/support/how-to-use-pgp) geïntegreerd in hun webmail. E-mails naar andere Proton Mail-accounts worden automatisch versleuteld, en versleuteling naar niet-Proton Mail-adressen met een OpenPGP-sleutel kan eenvoudig worden ingeschakeld in je accountinstellingen. Proton also supports automatic external key discovery with [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This means that emails sent to other providers which use WKD will be automatically encrypted with OpenPGP as well, without the need to manually exchange public PGP keys with your contacts. They also allow you to [encrypt messages to non-Proton Mail addresses without OpenPGP](https://proton.me/support/password-protected-emails), without the need for them to sign up for a Proton Mail account.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. Hierdoor kunnen mensen die geen Proton Mail gebruiken de OpenPGP sleutels van Proton Mail accounts gemakkelijk vinden, voor cross-provider E2EE. This only applies to email addresses ending in one of Proton's own domains, like @proton.me. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Beëindiging van account

Als je een betaald account hebt en je na 14 dagen [niet je rekening hebt betaald](https://proton.me/support/delinquency), krijg je geen toegang meer tot je gegevens. Na 30 dagen wordt uw account delinquent en ontvangt u geen inkomende e-mail meer. Tijdens deze periode word je nog steeds gefactureerd.

#### :material-information-outline:{ .pg-blue } Aanvullende functionaliteit

Proton Mail biedt een "Unlimited" account voor €9,99/maand, die ook toegang geeft tot Proton VPN, naast meerdere accounts, domeinen, aliassen en 500 GB opslagruimte.

Proton Mail heeft geen digitale erfenis functie.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** is een e-maildienst gericht op veiligheid, is reclamevrij en wordt 100% mogelijk gemaakt door milieuvriendelijke energie. Ze zijn sinds 2014 in bedrijf. Mailbox.org is gevestigd in Berlijn, Duitsland. Accounts beginnen met 2 GB opslagruimte, die naar behoefte kan worden uitgebreid.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Aangepaste domeinen en aliassen

Mailbox.org lets you use your own domain, and they support [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) addresses. Mailbox.org also supports [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green } Privé betaalmethoden

Mailbox.org accepteert geen Bitcoin of andere cryptocurrencies als gevolg van het feit dat hun betalingsverwerker BitPay zijn activiteiten in Duitsland heeft opgeschort. However, they do accept cash by mail, cash payment to bank account, bank transfer, credit card, PayPal and couple of German-specific processors: paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } Accountbeveiliging

Mailbox.org supports [two factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. You can use either TOTP or a [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via the [YubiCloud](https://yubico.com/products/services-software/yubicloud). Webstandaarden zoals [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) worden nog niet ondersteund.

#### :material-information-outline:{ .pg-blue } Gegevensbeveiliging

Mailbox.org allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Nieuwe berichten die je ontvangt, worden dan onmiddellijk versleuteld met jouw openbare sleutel.

However, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. Een [standalone optie](calendar.md) kan geschikter zijn voor die informatie.

#### :material-check:{ .pg-green } Email encryptie

Mailbox.org has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox.org's servers. Deze functie is nuttig wanneer de ontvanger op afstand geen OpenPGP heeft en geen kopie van de e-mail in zijn eigen mailbox kan ontsleutelen.

Mailbox.org ondersteunt ook de ontdekking van publieke sleutels via HTTP vanuit hun [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Hierdoor kunnen mensen buiten Mailbox.org gemakkelijk de OpenPGP sleutels van Mailbox.org accounts vinden, voor cross-provider E2EE. This only applies to email addresses ending in one of Mailbox.org's own domains, like @mailbox.org. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Beëindiging van account

Your account will be set to a restricted user account when your contract ends. It will be irrevocably deleted after [30 days](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Extra functionaliteit

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). Hun webmail interface is echter niet toegankelijk via hun .onion dienst en kan je te maken krijgen met TLS-certificaatfouten.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox.org ondersteunt ook [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) naast standaard toegangsprotocollen zoals IMAP en POP3.

Mailbox.org heeft een digitale nalatenschap functie voor alle abonnementen. Je kunt kiezen of je wilt dat jouw gegevens worden doorgegeven aan jouw erfgenamen, mits zij een aanvraag indienen en jouw testament overleggen. Je kunt ook een persoon nomineren met naam en adres.

## Meer providers

Deze providers slaan je e-mails op met zero-knowledge encryptie, waardoor ze geweldige opties zijn om je opgeslagen e-mails veilig te houden. Zij ondersteunen echter geen interoperabele versleutelingsnormen voor E2EE-communicatie tussen aanbieders.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg){ .twemoji } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg){ align=right }

**Tuta** is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since **2011** and is based in Hanover, Germany. Accounts beginnen met 1GB opslagruimte met hun gratis plan.

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

Tuta doesn't support the [IMAP protocol](https://tuta.com/faq/#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/posts/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/support#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } Aangepaste domeinen en aliassen

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/support#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/support#plus), but you can use a [catch-all](https://tuta.com/support#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } Privé betaalmethodes

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/faq/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green } Accountbeveiliging

Tuta supports [two factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Gegevensbeveiliging

Tuta has [zero access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). Dit betekent dat de berichten en andere gegevens die in jouw account zijn opgeslagen, alleen door je kunnen worden gelezen.

#### :material-information-outline:{ .pg-blue } Email Encryptie

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Beëindiging van account

Tuta will [delete inactive free accounts](https://tuta.com/support#inactive-accounts) after six months. Je kunt een gedeactiveerd gratis account opnieuw gebruiken als je betaalt.

#### :material-information-outline:{ .pg-blue } extra functionaliteit

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/posts/secure-email-for-non-profit) for free or with a heavy discount.

Tuta doesn't offer a digital legacy feature.

## Onze criteria

Gevorderde systeembeheerders kunnen overwegen hun eigen e-mailserver op te zetten. Mailservers vereisen aandacht en voortdurend onderhoud om de zaken veilig te houden en de mailbezorging betrouwbaar.

### Gecombineerde softwareoplossingen

<div class="admonition recommendation" markdown>

![Mailcow logo](assets/img/email/mailcow.svg){ align=right }

**Mailcow** is een meer geavanceerde mailserver, perfect voor mensen met wat meer Linux ervaring. Het heeft alles wat je nodig hebt in een Docker container: Een mailserver met DKIM-ondersteuning, antivirus- en spammonitoring, webmail en ActiveSync met SOGo, en webgebaseerd beheer met 2FA-ondersteuning.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

</div>

<div class="admonition recommendation" markdown>

![Mail-in-a-Box logo](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** is een geautomatiseerd setup script voor het implementeren van een mailserver op Ubuntu. Het doel ervan is om het voor mensen gemakkelijker te maken om hun eigen mailserver op te zetten.

[:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentatie}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Broncode" } }

</div>

Voor een meer handmatige aanpak hebben we deze twee artikelen uitgekozen:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://c0ffee.net/blog/mail-server-guide) (August 2017)

## Criteria

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an email provider, and conduct your own research to ensure the email provider you choose is the right choice for you.

### Technologie

Wij beschouwen deze kenmerken als belangrijk om een veilige en optimale dienst te kunnen verlenen. Je zou moeten nagaan of de provider de functies heeft die je nodig hebt.

**Minimum om in aanmerking te komen:**

- Versleutelt e-mail accountgegevens in rust met zero-access encryptie.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Sta gebruikers toe hun eigen [domeinnaam te gebruiken](https://en.wikipedia.org/wiki/Domain_name). Aangepaste domeinnamen zijn belangrijk voor gebruikers omdat ze zo hun agentschap van de dienst kunnen behouden, mocht het slecht aflopen of overgenomen worden door een ander bedrijf dat privacy niet hoog in het vaandel heeft staan.
- Werkt op eigen infrastructuur, d.w.z. niet gebaseerd op e-mail service providers van derden.

**Beste geval:**

- Versleutelt alle accountgegevens (Contacten, Agenda's, etc) in rust met zero-access encryptie.
- Geïntegreerde webmail E2EE/PGP-codering voor het gemak.
- Ondersteuning voor [WKD](https://wiki.gnupg.org/WKD) om een verbeterde ontdekking van publieke OpenPGP sleutels via HTTP mogelijk te maken. GnuPG-gebruikers kunnen een sleutel krijgen door te typen: `gpg --locate-key example_user@example.com`
- Ondersteuning voor een tijdelijke mailbox voor externe gebruikers. Dit is handig wanneer je een versleutelde e-mail wilt verzenden, zonder een echte kopie naar jouw ontvanger te sturen. Deze e-mails hebben meestal een beperkte levensduur en worden daarna automatisch verwijderd. Zij vereisen ook niet dat de ontvanger cryptografie configureert zoals OpenPGP.
- Beschikbaarheid van de diensten van de e-mailprovider via een [onion service](https://en.wikipedia.org/wiki/.onion).
- [Sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing) support.
- Catch-all of alias functionaliteit voor diegenen die hun eigen domeinen bezitten.
- Gebruik van standaard e-mail toegangsprotocollen zoals IMAP, SMTP of [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standaard toegangsprotocollen zorgen ervoor dat klanten al hun e-mail gemakkelijk kunnen downloaden, mochten zij naar een andere provider willen overstappen.

### Privacy

Wij geven er de voorkeur aan dat de door ons aanbevolen aanbieders zo weinig mogelijk gegevens verzamelen.

**Minimum om in aanmerking te komen:**

- Beschermt het IP adres van de afzender. Filter het uit de weergave in het `Received` header veld.
- Vereisen geen persoonlijk identificeerbare informatie (PII) naast een gebruikersnaam en een wachtwoord.
- Privacybeleid dat voldoet aan de vereisten van de GDPR.

**Beste geval:**

- Accepteert [anonieme betalingsopties](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), contant geld, cadeaukaarten, etc.)
- Gehost in een jurisdictie met sterke wetgeving ter bescherming van de privacy van e-mails.

### Veiligheid

Email servers verwerken veel zeer gevoelige gegevens. We verwachten dat providers de beste praktijken in de branche zullen toepassen om hun gebruikers te beschermen.

**Minimum om in aanmerking te komen:**

- Bescherming van webmail met 2FA, zoals TOTP.
- Zero access encryptie, bouwt voort op encryptie in rust. De provider heeft geen decryptiesleutels voor de gegevens die ze hebben. Dit voorkomt dat een malafide werknemer gegevens lekt waartoe hij toegang heeft, of dat een tegenstander op afstand gegevens vrijgeeft die hij heeft gestolen door ongeoorloofde toegang tot de server te verkrijgen.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) ondersteuning.
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Een geldig [MTA-STS](https://tools.ietf.org/html/rfc8461) en [TLS-RPT](https://tools.ietf.org/html/rfc8460) beleid.
- Geldig [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) records.
- Geldige [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) en [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) records.
- Geldige [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) en [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) records.
- Zorg voor een correct [DMARC](https://en.wikipedia.org/wiki/DMARC) record en beleid of gebruik [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) voor verificatie. Als DMARC-authenticatie wordt gebruikt, moet het beleid worden ingesteld op `reject` of `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) indiening, ervan uitgaande dat SMTP wordt gebruikt.
- Beveiligingsnormen voor websites, zoals:
    - [HTTP Strict Transport Security](https://nl.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subbron Integriteit](https://en.wikipedia.org/wiki/Subresource_Integrity) als dingen van externe domeinen worden geladen.
- Moet het bekijken van [Message headers](https://en.wikipedia.org/wiki/Email#Message_header)ondersteunen, aangezien dit een cruciale forensische functie is om te bepalen of een e-mail een phishing-poging is.

**Beste geval:**

- Ondersteuning voor hardware-authenticatie, d.w.z. U2F en [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn). U2F en WebAuthn zijn veiliger omdat zij een privésleutel gebruiken die is opgeslagen op een hardware-apparaat aan de clientzijde om mensen te authenticeren, in tegenstelling tot een gedeeld geheim dat is opgeslagen op de webserver en aan de clientzijde wanneer TOTP wordt gebruikt. Bovendien zijn U2F en WebAuthn beter bestand tegen phishing omdat hun authenticatierespons gebaseerd is op de geauthenticeerde [domeinnaam](https://en.wikipedia.org/wiki/Domain_name).
- [DNS Certificatie Autoriteit Autorisatie (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in aanvulling op DANE ondersteuning.
- Implementatie van [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), dit is nuttig voor mensen die posten naar mailinglijsten [RFC8617](https://tools.ietf.org/html/rfc8617).
- Programma's voor bug-bounty's en/of een gecoördineerd proces voor de openbaarmaking van kwetsbaarheden.
- Beveiligingsnormen voor websites, zoals:
    - [Inhoud beveiligingsbeleid (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Vertrouwen

Je zou je financiën niet toevertrouwen aan iemand met een valse identiteit, dus waarom zou je hen je e-mail toevertrouwen? Wij eisen van onze aanbevolen aanbieders dat zij hun eigendom of leiderschap openbaar maken. Wij zouden ook graag zien dat regelmatig verslag wordt uitgebracht over de transparantie, met name wat betreft de wijze waarop verzoeken van de overheid worden behandeld.

**Minimum om in aanmerking te komen:**

- Publiekelijk leiderschap of eigendom.

**Beste geval:**

- Publieksgericht leiderschap.
- Frequente transparantieverslagen.

### Marketing

Bij de e-mail providers die we aanbevelen zien we graag verantwoorde marketing.

**Minimum om in aanmerking te komen:**

- Moet zelf analytics hosten (geen Google Analytics, Adobe Analytics, etc.). De site van de aanbieder moet ook voldoen aan [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) voor degenen die zich willen afmelden.

Mag geen marketing hebben die onverantwoord is:

- Claims van "onbreekbare encryptie." Encryptie moet worden gebruikt met de bedoeling dat zij in de toekomst niet meer geheim is wanneer de technologie bestaat om haar te kraken.
- Garanties van 100% bescherming van de anonimiteit. Wanneer iemand beweert dat iets 100% is, betekent dit dat er geen zekerheid is voor mislukking. We weten dat mensen zichzelf vrij gemakkelijk kunnen deanonimiseren op een aantal manieren, bv.:

    - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
    - [Browser vingerafdrukken](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Beste geval:**

- Duidelijke en gemakkelijk te lezen documentatie. Dit omvat zaken als het instellen van 2FA, e-mailclients, OpenPGP, enz.

### Extra functionaliteit

Hoewel het geen strikte vereisten zijn, zijn er nog enkele andere factoren met betrekking tot gemak of privacy die wij in aanmerking hebben genomen bij het bepalen van de aan te bevelen providers.
