---
meta_title: "Encrypted Private Email Recommendations - Privacy Guides"
title: "Email szolgáltatások"
icon: material/email
description: Ezek az e-mail szolgáltatók nagyszerű helyet kínálnak az e-mailek biztonságos tárolására, és sokan kínálnak más szolgáltatókkal együttműködő OpenPGP titkosítást.
cover: email.webp
---

Email is practically a necessity for using any online service, however we do not recommend it for person-to-person conversations. Ahelyett, hogy e-mailben lépnél kapcsolatba másokkal, fontold meg egy olyan azonnali üzenetküldő használatát, amely támogatja a forward secrecy-t, vagyis szó szerint az előre titkosítást.

[Recommended Instant Messengers](real-time-communication.md ""){.md-button}

Minden más esetre olyan e-mail szolgáltatókat ajánlunk, amelyek fenntartható üzleti modelleken és beépített biztonsági, adat- és magánéletvédelmi funkciókon alapulnak.

- [OpenPGP-kompatibilis e-mail szolgáltatók :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [Egyéb titkosított szolgáltatók :material-arrow-right-drop-circle:](#more-providers)
- [Saját szerveren futtatható lehetőségek :material-arrow-right-drop-circle:](#self-hosting-email)

Az itt ajánlott e-mail szolgáltatók mellett (vagy helyett) érdemes megfontolni egy dedikált [e-mail alias szolgáltatást](email-aliasing.md) is a magánélet védelme érdekében. Ezek a szolgáltatások többek között segíthetnek megvédeni a valódi potaládádat a spamektől, megakadályozhatják, hogy a marketingesek összekapcsolják a fiókjaidat, és PGP-vel titkosíthatják az összes bejövő üzenetedet.

- [More Information :material-arrow-right-drop-circle:](email-aliasing.md)

## OpenPGP-kompatibilis szolgáltatások

Ezek a szolgáltatók natívan támogatják az OpenPGP titkosítást/visszafejtést és a [Web Key Directory szabványt](basics/email-security.md#what-is-the-web-key-directory-standard), lehetővé téve a szolgáltatófüggetlen, végponttól-végpontig titkosított e-maileket. Például egy Proton Mail felhasználó küldhet végponttól-végpontig titkosított üzenetet egy Mailbox.org felhasználónak, de fogadhatsz OpenPGP-titkosított értesítéseket olyan internetes szolgáltatásoktól is, amelyek támogatják azt.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Figyelmeztetés</p>

Az OpenPGP-hez hasonló végponttól-végpontig titkosító technológiák használata esetén az e-mail fejlécében továbbra is maradnak olyan metaadatok, amik nincsenek titkosítva, általában beleértve az üzenet tágyát is! Tudj meg többet az [e-mail metaadatokról](basics/email-security.md#email-metadata-overview).

Az OpenPGP nem támogatja a Forward secrecy-t sem, ami azt jelenti, hogy ha a tőled vagy a címzettől ellopják a privát kulcsot, azzal az összes korábbi, ezzel titkosított üzenet is nyilvánosságra kerül. [Hogyan védhetem a privát kulcsaimat?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }

A **Proton Mail** egy olyan e-mail szolgáltatás, amely a magánéletre, a titkosításra, a biztonságra és az egyszerű használatra helyezi a hangsúlyt. **2013** óta működnek. A Proton AG székhelye Genfben, Svájcban található. A fiókok 500 MB induló tárhellyel kezdődnek a ingyenes csomagban.

[:octicons-home-16: Főoldal](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion szolgáltatás" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Adatvédelem" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Dokumentáció}
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Forráskód" }

<details class="downloads" markdown>
<summary>Letöltés</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
- [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Az ingyenes fiókoknak vannak bizonyos korlátai, például nem tudnak keresni a szövegben, és nem férnek hozzá a [Proton Mail Bridge-hez](https://proton.me/mail/bridge), ami egy [ajánlott asztali e-mail kliens](email-clients.md) (pl. Thunderbird) használatához szükséges átjáró. A fizetős fiókok olyan funkciókat is tartalmaznak, mint a Proton Mail Bridge, további tárhely és egyéni domainek támogatása. A Proton Mail alkalmazást 2021. november 9-én a [Securitum](https://research.securitum.com) [tanúsította](https://proton.me/blog/security-audit-all-proton-apps).

Ha Proton Unlimited, Business vagy Visionary csomaggal rendelkezel, a [SimpleLogin](#simplelogin) Premiumot is ingyenesen használhatod.

Proton Mail has internal crash reports that they **do not** share with third parties. Ez kikapcsolható a: **Beállítások** > **Fiók** > **Biztonság és adatvédelem** > **Adatvédelem és adatgyűjtés** > **Hibajelentések küldése**.

#### :material-check:{ .pg-green } Custom Domains and Aliases

Paid Proton Mail subscribers can use their own domain with the service or a [catch-all](https://proton.me/support/catch-all) address. Proton Mail also supports [sub-addressing](https://proton.me/support/creating-aliases), which is useful for people who don't want to purchase a domain.

#### :material-check:{ .pg-green } Private Payment Methods

Proton Mail [accepts](https://proton.me/support/payment-options) cash by mail in addition to standard credit/debit card, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), and PayPal payments.

#### :material-check:{ .pg-green } Account Security

Proton Mail supports TOTP [two factor authentication](https://proton.me/support/two-factor-authentication-2fa) and [hardware security keys](https://proton.me/support/2fa-security-key) using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two factor authentication first.

#### :material-check:{ .pg-green } Data Security

Proton Mail has [zero-access encryption](https://proton.me/blog/zero-access-encryption) at rest for your emails and [calendars](https://proton.me/news/protoncalendar-security-model). Data secured with zero-access encryption is only accessible by you.

Certain information stored in [Proton Contacts](https://proton.me/support/proton-contacts), such as display names and email addresses, are not secured with zero-access encryption. Contact fields that support zero-access encryption, such as phone numbers, are indicated with a padlock icon.

#### :material-check:{ .pg-green } Email Encryption

Proton Mail has [integrated OpenPGP encryption](https://proton.me/support/how-to-use-pgp) in their webmail. Emails to other Proton Mail accounts are encrypted automatically, and encryption to non-Proton Mail addresses with an OpenPGP key can be enabled easily in your account settings. Proton also supports automatic external key discovery with [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This means that emails sent to other providers which use WKD will be automatically encrypted with OpenPGP as well, without the need to manually exchange public PGP keys with your contacts. They also allow you to [encrypt messages to non-Proton Mail addresses without OpenPGP](https://proton.me/support/password-protected-emails), without the need for them to sign up for a Proton Mail account.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. This allows people who don't use Proton Mail to find the OpenPGP keys of Proton Mail accounts easily, for cross-provider E2EE. This only applies to email addresses ending in one of Proton's own domains, like @proton.me. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Account Termination

If you have a paid account and your [bill is unpaid](https://proton.me/support/delinquency) after 14 days, you won't be able to access your data. After 30 days, your account will become delinquent and won't receive incoming mail. You will continue to be billed during this period.

#### :material-information-outline:{ .pg-blue } Additional Functionality

Proton Mail offers an "Unlimited" account for €9.99/Month, which also enables access to Proton VPN in addition to providing multiple accounts, domains, aliases, and 500GB of storage.

Proton Mail doesn't offer a digital legacy feature.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** is an email service with a focus on being secure, ad-free, and privately powered by 100% eco-friendly energy. They have been in operation since 2014. Mailbox.org is based in Berlin, Germany. Accounts start with 2 GB of storage, which can be upgraded as needed.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Custom Domains and Aliases

Mailbox.org lets you use your own domain, and they support [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) addresses. Mailbox.org also supports [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green } Private Payment Methods

Mailbox.org doesn't accept any cryptocurrencies as a result of their payment processor BitPay suspending operations in Germany. However, they do accept Cash by mail, cash payment to bank account, bank transfer, credit card, PayPal and couple of German-specific processors: paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } Account Security

Mailbox.org supports [two factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. You can use either TOTP or a [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via the [YubiCloud](https://yubico.com/products/services-software/yubicloud). Web standards such as [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) are not yet supported.

#### :material-information-outline:{ .pg-blue } Data Security

Mailbox.org allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). New messages that you receive will then be immediately encrypted with your public key.

However, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. A [standalone option](calendar.md) may be more appropriate for that information.

#### :material-check:{ .pg-green } Email Encryption

Mailbox.org has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox.org's servers. This feature is useful when the remote recipient does not have OpenPGP and cannot decrypt a copy of the email in their own mailbox.

Mailbox.org also supports the discovery of public keys via HTTP from their [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This allows people outside of Mailbox.org to find the OpenPGP keys of Mailbox.org accounts easily, for cross-provider E2EE. This only applies to email addresses ending in one of Mailbox.org's own domains, like @mailbox.org. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Account Termination

Your account will be set to a restricted user account when your contract ends, after [30 days it will be irrevocably deleted](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Additional Functionality

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). However, their webmail interface cannot be accessed via their .onion service and you may experience TLS certificate errors.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox.org also supports [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) in addition to standard access protocols like IMAP and POP3.

Mailbox.org has a digital legacy feature for all plans. You can choose whether you want any of your data to be passed to heirs providing that they apply and provide your testament. Alternatively, you can nominate a person by name and address.

## More Providers

These providers store your emails with zero-knowledge encryption, making them great options for keeping your stored emails secure. However, they don't support interoperable encryption standards for E2EE communications between different providers.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg){ .twemoji } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg){ align=right }

**Tuta** is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since **2011** and is based in Hanover, Germany. Accounts start with 1GB storage with their free plan.

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/faq){ .card-link title=Documentation}
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

Tuta doesn't support the [IMAP protocol](https://tuta.com/faq/#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/posts/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/howto#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } Custom Domains and Aliases

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/faq#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/faq#plus), but you can use a [catch-all](https://tuta.com/howto#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } Private Payment Methods

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/faq/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green } Account Security

Tuta supports [two factor authentication](https://tuta.com/faq#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Data Security

Tuta has [zero access encryption at rest](https://tuta.com/faq#what-encrypted) for your emails, [address book contacts](https://tuta.com/faq#encrypted-address-book), and [calendars](https://tuta.com/faq#calendar). This means the messages and other data stored in your account are only readable by you.

#### :material-information-outline:{ .pg-blue } Email Encryption

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Account Termination

Tuta will [delete inactive free accounts](https://tuta.com/faq#inactive-accounts) after six months. You can reuse a deactivated free account if you pay.

#### :material-information-outline:{ .pg-blue } Additional Functionality

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/posts/secure-email-for-non-profit) for free or with a heavy discount.

Tuta also has a business feature called [Secure Connect](https://tuta.com/secure-connect). This ensures customer contact to the business uses E2EE. The feature costs €240/y.

Tuta doesn't offer a digital legacy feature.

## Saját Üzemeltetésű Email

Advanced system administrators may consider setting up their own email server. Mail servers require attention and continuous maintenance in order to keep things secure and mail delivery reliable.

### Combined software solutions

<div class="admonition recommendation" markdown>

![Mailcow logo](assets/img/email/mailcow.svg){ align=right }

**Mailcow** is a more advanced mail server perfect for those with a bit more Linux experience. It has everything you need in a Docker container: A mail server with DKIM support, antivirus and spam monitoring, webmail and ActiveSync with SOGo, and web-based administration with 2FA support.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

</div>

<div class="admonition recommendation" markdown>

![Mail-in-a-Box logo](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** is an automated setup script for deploying a mail server on Ubuntu. Its goal is to make it easier for people to set up their own mail server.

[:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }

</div>

For a more manual approach we've picked out these two articles:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://c0ffee.net/blog/mail-server-guide) (August 2017)

## Követelmények

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any Email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an Email provider, and conduct your own research to ensure the Email provider you choose is the right choice for you.

### Technológia

We regard these features as important in order to provide a safe and optimal service. You should consider whether the provider which has the features you require.

**Alap Elvárások Minősítéshez:**

- Encrypts email account data at rest with zero-access encryption.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Custom domain names are important to users because it allows them to maintain their agency from the service, should it turn bad or be acquired by another company which doesn't prioritize privacy.
- Operates on owned infrastructure, i.e. not built upon third-party email service providers.

**Legjobb esetben:**

- Encrypts all account data (Contacts, Calendars, etc.) at rest with zero-access encryption.
- Integrated webmail E2EE/PGP encryption provided as a convenience.
- Support for [WKD](https://wiki.gnupg.org/WKD) to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key by typing: `gpg --locate-key example_user@example.com`
- Support for a temporary mailbox for external users. This is useful when you want to send an encrypted email, without sending an actual copy to your recipient. These emails usually have a limited lifespan and then are automatically deleted. They also don't require the recipient to configure any cryptography like OpenPGP.
- Availability of the email provider's services via an [onion service](https://en.wikipedia.org/wiki/.onion).
- [Sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing) support.
- Catch-all or alias functionality for those who own their own domains.
- Use of standard email access protocols such as IMAP, SMTP or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.

### Adatvédelem

Jobban szeretjük, ha az általunk ajánlott szolgáltatók a lehető legkevesebb adatot gyűjtik.

**Alap elvárások minősítéshez:**

- Protect sender's IP address. Filter it from showing in the `Received` header field.
- Don't require personally identifiable information (PII) besides a username and a password.
- Privacy policy that meets the requirements defined by the GDPR.

**Legjobb esetben:**

- Accepts [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Hosted in a jurisdiction with strong email privacy protection laws.

### Adatbiztonság

Email servers deal with a lot of very sensitive data. We expect that providers will adopt best industry practices in order to protect their members.

**Alap elvárások minősítéshez:**

- Protection of webmail with 2FA, such as TOTP.
- Zero access encryption, builds on encryption at rest. The provider does not have the decryption keys to the data they hold. This prevents a rogue employee leaking data they have access to or remote adversary from releasing data they have stolen by gaining unauthorized access to the server.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) support.
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLSv1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- A valid [MTA-STS](https://tools.ietf.org/html/rfc8461) and [TLS-RPT](https://tools.ietf.org/html/rfc8460) policy.
- Valid [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) records.
- Valid [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) and [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) records.
- Have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. If DMARC authentication is being used, the policy must be set to `reject` or `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) submission, assuming SMTP is used.
- Website security standards such as:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subresource Integrity](https://en.wikipedia.org/wiki/Subresource_Integrity) if loading things from external domains.
- Must support viewing of [Message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**Legjobb esetben:**

- Support for hardware authentication, i.e. U2F and [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn). U2F and WebAuthn are more secure as they use a private key stored on a client-side hardware device to authenticate people, as opposed to a shared secret that is stored on the web server and on the client side when using TOTP. Furthermore, U2F and WebAuthn are more resistant to phishing as their authentication response is based on the authenticated [domain name](https://en.wikipedia.org/wiki/Domain_name).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in addition to DANE support.
- Implementation of [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), this is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Bug-bounty programok és/vagy összehangolt sebezhetőség-közzétételi folyamat.
- Website security standards such as:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Bizalom

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? Az általunk ajánlott szolgáltatóktól elvárjuk, hogy nyilvánosak legyenek a tulajdonlásukról vagy vezetésükről. Szeretnénk továbbá gyakori átláthatósági jelentéseket látni, különösen a kormányzati kérelmek kezelésének módját illetően.

**Alap elvárások minősítéshez:**

- Nyilvános vezetés vagy tulajdonlás.

**Legjobb esetben:**

- Nyilvános vezetés.
- Gyakori átláthatósági jelentések.

### Marketing

With the email providers we recommend we like to see responsible marketing.

**Alap elvárások minősítéshez:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.). The provider's site must also comply with [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) for those who wish to opt-out.

Nem használhat felelőtlen marketinget:

- Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
- Az anonimitás 100%-os védelmének garantálása. Ha valaki azt állítja, hogy valami 100%-os, az azt jelenti, hogy nem merülhet fel meghibásodás. Tudjuk, hogy személyek elég könnyen és számos módon deanonimizálni tudják magukat, pl.:

    - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
    - [Böngésző fingerprintelés](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Legjobb esetben:**

- Clear and easy to read documentation. Ez többek között olyan dolgokat foglal magában, mint a kétlépcsős hitelesítés, az e-mail kliensek, vagy az OpenPGP beállítása.

### További funkciók

Bár ezek nem szigorú követelmények, más kényelmi vagy adatvédelmi tényezőket is figyelembe vettünk, amikor eldöntöttük, mely szolgáltatókat ajánljuk.
