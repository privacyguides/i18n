---
meta_title: "Aanbevelingen voor versleutelde privacyvriendelijke e-mail - Privacy Guides"
title: "Email Diensten"
icon: material/email
description: Deze e-mailproviders bieden een uitstekende plaats om jouw e-mails veilig op te slaan, en vele bieden interoperabele OpenPGP versleuteling met andere providers.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protects against the following threat(s):</small>

- [:material-server-network: Dienstverleners](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

E-mail is bijna een noodzaak voor het gebruik van elke online dienst, maar wij raden het niet aan voor gesprekken van persoon tot persoon. In plaats van e-mail te gebruiken om andere mensen te contacteren, kunt u overwegen een instant messenger te gebruiken die forward secrecy ondersteunt.

[Aanbevolen Instant Messengers](real-time-communication.md ""){.md-button}

## Aanbevolen Providers

Voor al het andere raden wij verschillende e-mailproviders aan op basis van duurzame bedrijfsmodellen en ingebouwde beveiligings- en privacyfuncties. Lees onze [volledige lijst met criteria](#criteria) voor meer informatie.

| Provider                    | OpenPGP / WKD                          | IMAP / SMTP                                                | Zero-Access Encryption                               | Anonymous Payment Methods             |
| --------------------------- | -------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------- | ------------------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Paid plans only | :material-check:{ .pg-green }                        | Contant                               |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                              | :material-information-outline:{ .pg-blue } Mail only | Contant                               |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                        | Monero <br>Cash via third party |

In addition to (or instead of) an email provider recommended here, you may wish to consider a dedicated [email aliasing service](email-aliasing.md#recommended-providers) to protect your privacy. Among other things, these services can help protect your real inbox from spam, prevent marketers from correlating your accounts, and encrypt all incoming messages with PGP.

- [More Information :material-arrow-right-drop-circle:](email-aliasing.md)

## OpenPGP compatibele diensten

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory (WKD) standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic end-to-end encrypted emails. Een Proton Mail-gebruiker zou bijvoorbeeld een E2EE-bericht kunnen sturen naar een Mailbox.org-gebruiker, of je zou OpenPGP-versleutelde meldingen kunnen ontvangen van internetdiensten die dit ondersteunen.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

When using E2EE technology like OpenPGP your email will still have some metadata that is not encrypted in the header of the email, generally including the subject line! Read more about [email metadata](basics/email-security.md#email-metadata-overview).

OpenPGP also does not support forward secrecy, which means if the private key of either you or the message recipient is ever stolen, all previous messages encrypted with it will be exposed.

- [How do I protect my private keys?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** is een e-maildienst met focus op privacy, encryptie, veiligheid en gebruiksgemak. They have been in operation since 2013. Proton AG is based in Geneva, Switzerland.

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

Free accounts have some limitations, such as not being able to search body text and not having access to [Proton Mail Bridge](https://proton.me/mail/bridge), which is required to use a [recommended desktop email client](email-clients.md) (e.g., Thunderbird). Betaalde accounts bevatten functies zoals Proton Mail Bridge, extra opslagruimte en ondersteuning voor aangepaste domeinen. If you have the Proton Unlimited plan or any multi-user Proton plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

Een [attestatiebrief](https://proton.me/blog/security-audit-all-proton-apps) werd op 9 november 2021 verstrekt voor de apps van Proton Mail door [Securitum](https://research.securitum.com).

Proton Mail has internal crash reports that are **not** shared with third parties. This can be disabled in the web app: :gear: → **All Settings** → **Account** → **Security and privacy** → **Privacy and data collection**.

#### :material-check:{ .pg-green } Aangepaste domeinen en aliassen

Betaalde Proton Mail abonnees kunnen hun eigen domein met de dienst gebruiken of een [catch-all](https://proton.me/support/catch-all) adres. Proton Mail also supports [sub-addressing](https://proton.me/support/creating-aliases), which is useful for people who don't want to purchase a domain.

#### :material-check:{ .pg-green } Privé betaalmethoden

Proton Mail [accepts](https://proton.me/support/payment-options) **cash** by mail in addition to standard credit/debit card, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), and PayPal payments.

#### :material-check:{ .pg-green } Accountbeveiliging

Proton Mail supports TOTP [two-factor authentication](https://proton.me/support/two-factor-authentication-2fa) and [hardware security keys](https://proton.me/support/2fa-security-key) using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two-factor authentication first.

#### :material-check:{ .pg-green } Gegevensbeveiliging

Proton Mail heeft [zero-access encryptie](https://proton.me/blog/zero-access-encryption) in rust voor jouw e-mails en [agenda's](https://proton.me/news/protoncalendar-security-model). Gegevens die zijn beveiligd met zero-access encryptie zijn alleen voor jouw toegankelijk.

Bepaalde informatie opgeslagen in [Proton Contacts](https://proton.me/support/proton-contacts), zoals namen en e-mailadressen, zijn niet beveiligd met zero-access encryptie. Contact velden die zero-access encryptie ondersteunen, zoals telefoonnummers, worden aangegeven met een hangslot pictogram.

#### :material-check:{ .pg-green } Email encryptie

Proton Mail heeft [OpenPGP encryptie](https://proton.me/support/how-to-use-pgp) geïntegreerd in hun webmail. E-mails naar andere Proton Mail-accounts worden automatisch versleuteld, en versleuteling naar niet-Proton Mail-adressen met een OpenPGP-sleutel kan eenvoudig worden ingeschakeld in je accountinstellingen. Proton also supports automatic external key discovery with WKD. This means that emails sent to other providers which use WKD will be automatically encrypted with OpenPGP as well, without the need to manually exchange public PGP keys with your contacts. They also allow you to [encrypt messages to non-Proton Mail addresses without OpenPGP](https://proton.me/support/password-protected-emails), without the need for them to sign up for a Proton Mail account.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. This allows people who don't use Proton Mail to find the OpenPGP keys of Proton Mail accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Proton's own domains, like `@proton.me`. If you use a custom domain, you must [configure WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Beëindiging van account

Als je een betaald account hebt en je na 14 dagen [niet je rekening hebt betaald](https://proton.me/support/delinquency), krijg je geen toegang meer tot je gegevens. Na 30 dagen wordt uw account delinquent en ontvangt u geen inkomende e-mail meer. Tijdens deze periode word je nog steeds gefactureerd. Proton will [delete inactive free accounts](https://proton.me/support/inactive-accounts) after one year. You **cannot** reuse the email address of a deactivated account.

#### :material-information-outline:{ .pg-blue } Aanvullende functionaliteit

Proton Mail's [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) plan also enables access to other Proton services in addition to providing multiple custom domains, unlimited hide-my-email aliases, and 500 GB of storage.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** is an email service with a focus on being secure, ad-free, and powered by 100% eco-friendly energy. Ze zijn sinds 2014 in bedrijf. Mailbox.org is gevestigd in Berlijn, Duitsland.

Accounts start with up to 2 GB storage, which can be upgraded as needed.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Aangepaste domeinen en aliassen

Mailbox.org lets you use your own domain, and they support [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) addresses. Mailbox.org also supports [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green } Privé betaalmethoden

Mailbox.org accepteert geen Bitcoin of andere cryptocurrencies als gevolg van het feit dat hun betalingsverwerker BitPay zijn activiteiten in Duitsland heeft opgeschort. However, they do accept **cash** by mail, **cash** payment to bank account, bank transfer, credit card, PayPal, and a couple of German-specific processors: Paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } Accountbeveiliging

Mailbox.org supports [two-factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. You can use either TOTP or a [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via the [YubiCloud](https://yubico.com/products/services-software/yubicloud). Web standards such as [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) are not yet supported.

#### :material-information-outline:{ .pg-blue } Gegevensbeveiliging

Mailbox.org allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Nieuwe berichten die je ontvangt, worden dan onmiddellijk versleuteld met jouw openbare sleutel.

However, [Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. A [standalone option](calendar.md) may be more appropriate for that data.

#### :material-check:{ .pg-green } Email encryptie

Mailbox.org has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox.org's servers. Deze functie is nuttig wanneer de ontvanger op afstand geen OpenPGP heeft en geen kopie van de e-mail in zijn eigen mailbox kan ontsleutelen.

Mailbox.org also supports the discovery of public keys via HTTP from their WKD. This allows people outside of Mailbox.org to find the OpenPGP keys of Mailbox.org accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Mailbox.org's own domains, like `@mailbox.org`. If you use a custom domain, you must [configure WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Beëindiging van account

Your account will be set to a restricted user account when your contract ends. It will be irrevocably deleted after [30 days](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Extra functionaliteit

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). However, their webmail interface cannot be accessed via their .onion service, and you may experience TLS certificate errors.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox.org ondersteunt ook [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) naast standaard toegangsprotocollen zoals IMAP en POP3.

Mailbox.org heeft een digitale nalatenschap functie voor alle abonnementen. You can choose whether you want any of your data to be passed to heirs, providing that they apply and provide your testament. Je kunt ook een persoon nomineren met naam en adres.

## Meer providers

Deze providers slaan je e-mails op met zero-knowledge encryptie, waardoor ze geweldige opties zijn om je opgeslagen e-mails veilig te houden. Zij ondersteunen echter geen interoperabele versleutelingsnormen voor E2EE-communicatie tussen aanbieders.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (formerly *Tutanota*) is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since 2011 and is based in Hanover, Germany.

Free accounts start with 1 GB of storage.

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

Tuta doesn't support the [IMAP protocol](https://tuta.com/support#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/support#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } Aangepaste domeinen en aliassen

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/support#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/support#plus), but you can use a [catch-all](https://tuta.com/support#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } Privé betaalmethodes

Tuta only directly accepts credit cards and PayPal, however [**cryptocurrency**](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with ProxyStore.

#### :material-check:{ .pg-green } Accountbeveiliging

Tuta supports [two-factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Gegevensbeveiliging

Tuta has [zero-access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). Dit betekent dat de berichten en andere gegevens die in jouw account zijn opgeslagen, alleen door je kunnen worden gelezen.

#### :material-information-outline:{ .pg-blue } Email Encryptie

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Beëindiging van account

Tuta will [delete inactive free accounts](https://tuta.com/support#inactive-accounts) after six months. Je kunt een gedeactiveerd gratis account opnieuw gebruiken als je betaalt.

#### :material-information-outline:{ .pg-blue } extra functionaliteit

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/secure-email-for-non-profit) for free or with a heavy discount.

## Criteria

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an email provider, and conduct your own research to ensure the email provider you choose is the right choice for you.

### Technologie

Wij beschouwen deze kenmerken als belangrijk om een veilige en optimale dienst te kunnen verlenen. Je zou moeten nagaan of de provider de functies heeft die je nodig hebt.

**Minimum om in aanmerking te komen:**

- Must encrypt email account data at rest with zero-access encryption.
- Must be capable of exporting emails as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .EML with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Aangepaste domeinnamen zijn belangrijk voor gebruikers omdat ze zo hun agentschap van de dienst kunnen behouden, mocht het slecht aflopen of overgenomen worden door een ander bedrijf dat privacy niet hoog in het vaandel heeft staan.
- Must operate on owned infrastructure, i.e. not built upon third-party email service providers.

**Beste geval:**

- Should encrypt all account data (contacts, calendars, etc.) at rest with zero-access encryption.
- Should provide integrated webmail E2EE/PGP encryption as a convenience.
- Should support WKD to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key with this command: `gpg --locate-key example_user@example.com`.
- Ondersteuning voor een tijdelijke mailbox voor externe gebruikers. This is useful when you want to send an encrypted email without sending an actual copy to your recipient. Deze e-mails hebben meestal een beperkte levensduur en worden daarna automatisch verwijderd. Zij vereisen ook niet dat de ontvanger cryptografie configureert zoals OpenPGP.
- Should support [sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Should allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Aangepaste domeinnamen zijn belangrijk voor gebruikers omdat ze zo hun agentschap van de dienst kunnen behouden, mocht het slecht aflopen of overgenomen worden door een ander bedrijf dat privacy niet hoog in het vaandel heeft staan.
- Catch-all or alias functionality for those who use their own domains.
- Should use standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.
- Email provider's services should be available via an [onion service](https://en.wikipedia.org/wiki/.onion).

### Privacy

Wij geven er de voorkeur aan dat de door ons aanbevolen aanbieders zo weinig mogelijk gegevens verzamelen.

**Minimum om in aanmerking te komen:**

- Must protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Must not require personally identifiable information (PII) besides a username and a password.
- Privacy policy must meet the requirements defined by the GDPR.

**Beste geval:**

- Should accept [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Should be hosted in a jurisdiction with strong email privacy protection laws.

### Veiligheid

Email servers deal with a lot of very sensitive data. We expect that providers will adopt industry best practices in order to protect their customers.

**Minimum om in aanmerking te komen:**

- Protection of webmail with 2FA, such as [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Zero-access encryption, which builds on encryption at rest. De provider heeft geen decryptiesleutels voor de gegevens die ze hebben. Dit voorkomt dat een malafide werknemer gegevens lekt waartoe hij toegang heeft, of dat een tegenstander op afstand gegevens vrijgeeft die hij heeft gestolen door ongeoorloofde toegang tot de server te verkrijgen.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) ondersteuning.
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLS 1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- Geldig [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) records.
- Geldige [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) en [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) records.
- Geldige [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) en [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) records.
- Must have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. Als DMARC-authenticatie wordt gebruikt, moet het beleid worden ingesteld op `reject` of `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) indiening, ervan uitgaande dat SMTP wordt gebruikt.
- Beveiligingsnormen voor websites, zoals:
    - [HTTP Strict Transport Security](https://nl.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subbron Integriteit](https://en.wikipedia.org/wiki/Subresource_Integrity) als dingen van externe domeinen worden geladen.
- Must support viewing of [message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**Beste geval:**

- Should support hardware authentication, i.e. U2F and [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [DNS Certificatie Autoriteit Autorisatie (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in aanvulling op DANE ondersteuning.
- Should implement [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Published security audits from a reputable, third-party firm.
- Programma's voor bug-bounty's en/of een gecoördineerd proces voor de openbaarmaking van kwetsbaarheden.
- Beveiligingsnormen voor websites, zoals:
    - [Inhoud beveiligingsbeleid (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Vertrouwen

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? Wij eisen van onze aanbevolen aanbieders dat zij hun eigendom of leiderschap openbaar maken. Wij zouden ook graag zien dat regelmatig verslag wordt uitgebracht over de transparantie, met name wat betreft de wijze waarop verzoeken van de overheid worden behandeld.

**Minimum om in aanmerking te komen:**

- Publiekelijk leiderschap of eigendom.

**Beste geval:**

- Frequente transparantieverslagen.

### Marketing

With the email providers we recommend, we like to see responsible marketing.

**Minimum om in aanmerking te komen:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.).
- Must not have any irresponsible marketing, which can include the following:
    - Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
    - Guarantees of protecting anonymity 100%. When someone makes a claim that something is 100%, it means there is no certainty for failure. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:
        - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software such as Tor
        - [Browser vingerafdrukken](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Beste geval:**

- Clear and easy-to-read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### Extra functionaliteit

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
