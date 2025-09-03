---
meta_title: "Doporučení na šifrované soukromé e-maily – Privacy Guides"
title: "E-mailové služby"
icon: material/email
description: Tito poskytovatelé e-mailu jsou skvělí pro bezpečné uchovávání e-mailů, a mnozí z nich nabízejí interoperabilní OpenPGP šifrování s ostatními poskytovateli.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Chrání před těmito hrozbami:</small>

- [:material-server-network: Poskytovatelé služeb](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

E-mail je prakticky nezbytný pro používání jakékoliv online služby, ale nedoporučujeme jej pro osobní konverzace. Namísto e-mailu zvažte možnost kontaktování pomocí chatovacích služeb, které podporují dopřednou bezpečnost.

[Doporučené messengery](real-time-communication.md ""){.md-button}

## Doporučení poskytovatelé

Pro všechno ostatní doporučujeme různé e-mailové poskytovatele, kteří mají udržitelný byznys model a vestavěné funkce pro zachování bezpečnosti a soukromí. Přečtěte si náš [úplný seznam kritérií](#criteria) pro více informací.

| Poskytovatel                | OpenPGP / WKD                          | IMAP / SMTP                                                     | Zero-Access šifrování                                  | Anonymní platební metody                               |
| --------------------------- | -------------------------------------- | --------------------------------------------------------------- | ------------------------------------------------------ | ------------------------------------------------------ |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Pouze placené tarify | :material-check:{ .pg-green }                          | Hotovost                                               |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                                   | :material-information-outline:{ .pg-blue } Pouze maily | Hotovost                                               |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                          | :material-check:{ .pg-green }                          | Monero <br>Hotovost prostřednictvím třetí strany |

Můžete navíc, nebo místo, zvážit používání kromě zmíněných e-mailových poskytovatelů i používání dedikované [služby pro e-mailové aliasy](email-aliasing.md#recommended-providers) pro ochranu vašeho soukromí. Tyto služby vám mimo jiné mohou pomoct chránit vaši pravou adresu před spamem, zabránit marketingovým týmům v korelování mezi jednotlivými účty a šifrovat všechny příchozí zprávy pomocí PGP.

- [Více informací](email-aliasing.md)

## Služby kompatibilní s OpenPGP

Tito poskytovatelé nativně podporují OpenPGP (de)šifrování a [standard Web Key Directory (WKD)](basics/email-security.md#what-is-the-web-key-directory-standard), který umožňuje posílání koncově šifrovaných e-mailů bez ohledu na poskytovatele. Například uživatel Proton Mailu může poslat koncově šifrovanou zprávu uživateli Mailbox.org, nebo může přijímat notifikace šifrované pomocí OpenPGP z internetových služeb, které to podporují.

<div class="grid cards" markdown>

- ![logo Proton Mail](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![logo Mailbox.org](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Varování</p>

I při používání E2EE technologie, jako je OpenPGP, budou vaše e-maily přesto obsahovat některá metadata, která nebudou šifrovaná v hlavičce e-mailu, obvykle včetně předmětu. Přečtěte si více o [e-mailových metadatech](basics/email-security.md#email-metadata-overview).

OpenPGP také nepodporuje dopřednou bezpečnost, což znamená, že pokud někdo jiný získá soukromý klíč, ať už váš, nebo protistrany, všechny vaše předchozí šifrované zprávy budou odhaleny.

- [Jak mohu ochránit své soukromé klíče?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![logo Proton Mail](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** je e-mailová služba se zaměřením na soukromí, šifrování, bezpečnost a snadné používání. Fungují od roku 2013. Proton AG sídlí v Ženevě ve Švýcarsku.

Tarif Proton Free obsahuje 500 MB úložiště pro e-mail, které můžete zdarma rozšířit až na 1 GB.

[:octicons-home-16: Homepage](https://proton.me/cs/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion stránka" }
[:octicons-eye-16:](https://proton.me/cs/legal/privacy){ .card-link title="Zásady ochrany osobních údajů" }
[:octicons-info-16:](https://proton.me/support/cs/mail){ .card-link title="Podpora" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Zdrojový kód" }

<details class="downloads" markdown>
<summary>Ke stažení</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Bezplatné účty mají některá omezení, např. nemohou vyhledávat v textu zpráv nebo nemají přístup k [Proton Mail Bridge](https://proton.me/mail/bridge), který je nutný pro používání s [doporučenými desktopovými e-mailovými klienty](email-clients.md) (např. s Thunderbirdem). Placené účty zahrnují funkce, jako je např. Proton Mail Bridge, dodatečné úložiště nebo podpora vlastních domén. Pokud máte tarif Proton Unlimited nebo jakýkoliv Proton tarif pro více uživatelů, získáte také [SimpleLogin](email-aliasing.md#simplelogin) Premium zdarma.

[Osvědčení](https://proton.me/blog/security-audit-all-proton-apps) bylo uděleno aplikacím Proton Mail 9. října 2021 firmou [Securitum](https://research.securitum.com).

Proton Mail generuje interní hlášení o pádech, které ale **nejsou** sdílené se třetími stranami. Můžete je ve webové aplikaci zakázat následovně: :gear: → **Všechna nastavení** → **Účet** → **Bezpečnost a soukromí** → **Soukromí a sběr dat**.

#### :material-check:{ .pg-green } Vlastní domény a aliasy

Uživatelé placených tarifů Proton Mailu mohou používat vlastní domény se službou nebo [univerzální](https://proton.me/support/catch-all) adresu. Proton Mail také podporuje [sub-adresování](https://proton.me/support/creating-aliases), což je užitečné pro lidi, kteří si nechtějí kupovat doménu.

#### :material-check:{ .pg-green } Soukromé platební metody

Proton Mail kromě běžných plateb kreditní či debetní kartou [přijímá](https://proton.me/support/payment-options) také [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), PayPal a dokonce i **hotovost** zaslanou poštou.

#### :material-check:{ .pg-green } Zabezpečení účtu

Proton Mail podporuje [dvoufaktorové ověřování](https://proton.me/support/two-factor-authentication-2fa) pomocí TOTP a [hardwarové bezpečnostní klíče](https://proton.me/support/2fa-security-key) pomocí standardů FIDO2 a U2F. Používání hardwarových bezpečnostních klíčů nejprve vyžaduje nastavení TOTP dvoufaktorového ověření.

#### :material-check:{ .pg-green } Data Security

Proton Mail has [zero-access encryption](https://proton.me/blog/zero-access-encryption) at rest for your emails and [calendars](https://proton.me/news/protoncalendar-security-model). Data secured with zero-access encryption is only accessible by you.

Certain information stored in [Proton Contacts](https://proton.me/support/proton-contacts), such as display names and email addresses, are not secured with zero-access encryption. Contact fields that support zero-access encryption, such as phone numbers, are indicated with a padlock icon.

#### :material-check:{ .pg-green } Email Encryption

Proton Mail has [integrated OpenPGP encryption](https://proton.me/support/how-to-use-pgp) in their webmail. Emails to other Proton Mail accounts are encrypted automatically, and encryption to non-Proton Mail addresses with an OpenPGP key can be enabled easily in your account settings. Proton also supports automatic external key discovery with WKD. This means that emails sent to other providers which use WKD will be automatically encrypted with OpenPGP as well, without the need to manually exchange public PGP keys with your contacts. They also allow you to [encrypt messages to non-Proton Mail addresses without OpenPGP](https://proton.me/support/password-protected-emails), without the need for them to sign up for a Proton Mail account.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. This allows people who don't use Proton Mail to find the OpenPGP keys of Proton Mail accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Proton's own domains, like `@proton.me`. If you use a custom domain, you must [configure WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Account Termination

If you have a paid account and your [bill is unpaid](https://proton.me/support/delinquency) after 14 days, you won't be able to access your data. After 30 days, your account will become delinquent and won't receive incoming mail. You will continue to be billed during this period. Proton will [delete inactive free accounts](https://proton.me/support/inactive-accounts) after one year. You **cannot** reuse the email address of a deactivated account.

#### :material-information-outline:{ .pg-blue } Additional Functionality

Proton Mail's [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) plan also enables access to other Proton services in addition to providing multiple custom domains, unlimited hide-my-email aliases, and 500 GB of storage.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** is an email service with a focus on being secure, ad-free, and powered by 100% eco-friendly energy. They have been in operation since 2014. Mailbox.org is based in Berlin, Germany.

Accounts start with up to 2 GB storage, which can be upgraded as needed.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Vlastní domény a aliasy

Mailbox.org lets you use your own domain, and they support [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) addresses. Mailbox.org also supports [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green } Soukromé platební metody

Mailbox.org doesn't accept any cryptocurrencies as a result of their payment processor BitPay suspending operations in Germany. However, they do accept **cash** by mail, **cash** payment to bank account, bank transfer, credit card, PayPal, and a couple of German-specific processors: Paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } Zabezpečení účtu

Mailbox.org supports [two-factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. You can use either TOTP or a [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via the [YubiCloud](https://yubico.com/products/services-software/yubicloud). Web standards such as [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) are not yet supported.

#### :material-information-outline:{ .pg-blue } Data Security

Mailbox.org allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). New messages that you receive will then be immediately encrypted with your public key.

However, [Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. A [standalone option](calendar.md) may be more appropriate for that data.

#### :material-check:{ .pg-green } Email Encryption

Mailbox.org has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox.org's servers. This feature is useful when the remote recipient does not have OpenPGP and cannot decrypt a copy of the email in their own mailbox.

Mailbox.org also supports the discovery of public keys via HTTP from their WKD. This allows people outside of Mailbox.org to find the OpenPGP keys of Mailbox.org accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Mailbox.org's own domains, like `@mailbox.org`. If you use a custom domain, you must [configure WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Account Termination

Your account will be set to a restricted user account when your contract ends. It will be irrevocably deleted after [30 days](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Additional Functionality

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). However, their webmail interface cannot be accessed via their .onion service, and you may experience TLS certificate errors.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox.org also supports [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) in addition to standard access protocols like IMAP and POP3.

Mailbox.org has a digital legacy feature for all plans. You can choose whether you want any of your data to be passed to heirs, providing that they apply and provide your testament. Alternatively, you can nominate a person by name and address.

## More Providers

These providers store your emails with zero-knowledge encryption, making them great options for keeping your stored emails secure. However, they don't support interoperable encryption standards for E2EE communications between different providers.

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

#### :material-check:{ .pg-green } Vlastní domény a aliasy

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/support#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/support#plus), but you can use a [catch-all](https://tuta.com/support#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } Private Payment Methods

Tuta only directly accepts credit cards and PayPal, however [**cryptocurrency**](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with ProxyStore.

#### :material-check:{ .pg-green } Zabezpečení účtu

Tuta supports [two-factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Data Security

Tuta has [zero-access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). This means the messages and other data stored in your account are only readable by you.

#### :material-information-outline:{ .pg-blue } Email Encryption

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Account Termination

Tuta will [delete inactive free accounts](https://tuta.com/support#inactive-accounts) after six months. You can reuse a deactivated free account if you pay.

#### :material-information-outline:{ .pg-blue } Additional Functionality

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/secure-email-for-non-profit) for free or with a heavy discount.

## Criteria

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an email provider, and conduct your own research to ensure the email provider you choose is the right choice for you.

### Technology

We regard these features as important in order to provide a safe and optimal service. You should consider whether the provider has the features you require.

**Minimum to Qualify:**

- Must encrypt email account data at rest with zero-access encryption.
- Must be capable of exporting emails as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .EML with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Custom domain names are important to users because it allows them to maintain their agency from the service, should it turn bad or be acquired by another company which doesn't prioritize privacy.
- Must operate on owned infrastructure, i.e. not built upon third-party email service providers.

**Best Case:**

- Should encrypt all account data (contacts, calendars, etc.) at rest with zero-access encryption.
- Should provide integrated webmail E2EE/PGP encryption as a convenience.
- Should support WKD to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key with this command: `gpg --locate-key example_user@example.com`.
- Support for a temporary mailbox for external users. This is useful when you want to send an encrypted email without sending an actual copy to your recipient. These emails usually have a limited lifespan and then are automatically deleted. They also don't require the recipient to configure any cryptography like OpenPGP.
- Should support [sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Should allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Custom domain names are important to users because it allows them to maintain their agency from the service, should it turn bad or be acquired by another company which doesn't prioritize privacy.
- Catch-all or alias functionality for those who use their own domains.
- Should use standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.
- Email provider's services should be available via an [onion service](https://en.wikipedia.org/wiki/.onion).

### Privacy

We prefer our recommended providers to collect as little data as possible.

**Minimum to Qualify:**

- Must protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Must not require personally identifiable information (PII) besides a username and a password.
- Privacy policy must meet the requirements defined by the GDPR.

**Best Case:**

- Should accept [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Should be hosted in a jurisdiction with strong email privacy protection laws.

### Security

Email servers deal with a lot of very sensitive data. We expect that providers will adopt industry best practices in order to protect their customers.

**Minimum to Qualify:**

- Protection of webmail with 2FA, such as [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Zero-access encryption, which builds on encryption at rest. The provider does not have the decryption keys to the data they hold. This prevents a rogue employee leaking data they have access to or remote adversary from releasing data they have stolen by gaining unauthorized access to the server.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) support.
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLS 1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- A valid [MTA-STS](https://tools.ietf.org/html/rfc8461) and [TLS-RPT](https://tools.ietf.org/html/rfc8460) policy.
- Valid [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) records.
- Valid [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) and [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) records.
- Must have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. If DMARC authentication is being used, the policy must be set to `reject` or `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) submission, assuming SMTP is used.
- Website security standards such as:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subresource Integrity](https://en.wikipedia.org/wiki/Subresource_Integrity) if loading things from external domains.
- Must support viewing of [message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**Best Case:**

- Should support hardware authentication, i.e. U2F and [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in addition to DANE support.
- Should implement [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Published security audits from a reputable, third-party firm.
- Bug-bounty programs and/or a coordinated vulnerability-disclosure process.
- Website security standards such as:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Trust

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? We require our recommended providers to be public about their ownership or leadership. We also would like to see frequent transparency reports, especially in regard to how government requests are handled.

**Minimum to Qualify:**

- Public-facing leadership or ownership.

**Best Case:**

- Frequent transparency reports.

### Marketing

With the email providers we recommend, we like to see responsible marketing.

**Minimum to Qualify:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.).
- Must not have any irresponsible marketing, which can include the following:
    - Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
    - Guarantees of protecting anonymity 100%. When someone makes a claim that something is 100%, it means there is no certainty for failure. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:
        - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software such as Tor
        - [Browser fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Best Case:**

- Clear and easy-to-read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### Additional Functionality

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
