---
meta_title: "Titkosított privát e-mail ajánlások – Privacy Guides"
title: Email szolgáltatások
icon: material/email
description: Ezek az e-mail szolgáltatók nagyszerű helyet kínálnak az e-mailek biztonságos tárolására, és sokan kínálnak más szolgáltatókkal együttműködő OpenPGP titkosítást.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protects against the following threat(s):</small>

- [:material-server-network: Service Providers](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Az email gyakorlatilag elengedhetetlen bármilyen online szolgáltatás használatához, azonban nem ajánljuk személyes beszélgetésekhez. Ahelyett, hogy e-mailben lépnél kapcsolatba másokkal, fontold meg egy olyan azonnali üzenetküldő használatát, amely támogatja a forward secrecy-t, vagyis szó szerint az előre titkosítást.

[Ajánlott azonnali üzenetküldők](real-time-communication.md ""){.md-button}

## Ajánlott Szolgáltatók

Minden más esetre olyan emailszolgáltatókat ajánlunk, amelyek fenntartható üzleti modelleken és beépített biztonsági, adat- és magánéletvédelmi funkciókon alapulnak. Read our [full list of criteria](#criteria) for more information.

| Provider                      | OpenPGP / WKD                          | IMAP / SMTP                                                | Zero-Access Encryption                               | Anonymous Payment Methods             |
| ----------------------------- | -------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------- | ------------------------------------- |
| [Proton Mail](#proton-mail)   | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Paid plans only | :material-check:{ .pg-green }                        | Cash                                  |
| [Mailbox Mail](#mailbox-mail) | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                              | :material-information-outline:{ .pg-blue } Mail only | Cash                                  |
| [Tuta](#tuta)                 | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                        | Monero <br>Cash via third party |

In addition to (or instead of) an email provider recommended here, you may wish to consider a dedicated [email aliasing service](email-aliasing.md#recommended-providers) to protect your privacy. Ezek a szolgáltatások többek között segíthetnek megvédeni a valódi potaládádat a spamektől, megakadályozhatják, hogy a marketingesek összekapcsolják a fiókjaidat, és PGP-vel titkosíthatják az összes bejövő üzenetedet.

- [További információ :material-arrow-right-drop-circle:](email-aliasing.md)

## OpenPGP-kompatibilis szolgáltatások

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory (WKD) standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic end-to-end encrypted emails. For example, a Proton Mail user could send an E2EE message to a Mailbox Mail user, or you could receive OpenPGP-encrypted notifications from internet services which support it.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](#proton-mail)
- ![Mailbox Mail logo](assets/img/email/mailbox-mail.svg){ .twemoji } [Mailbox Mail](#mailbox-mail)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Figyelmeztetés</p>

Az OpenPGP-hez hasonló végponttól-végpontig titkosító technológiák használata esetén az e-mail fejlécében továbbra is maradnak olyan metaadatok, amik nincsenek titkosítva, általában beleértve az üzenet tágyát is! Tudj meg többet az [e-mail metaadatokról](basics/email-security.md#email-metadata-overview).

OpenPGP also does not support forward secrecy, which means if the private key of either you or the message recipient is ever stolen, all previous messages encrypted with it will be exposed.

- [How do I protect my private keys?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }

A **Proton Mail** egy olyan e-mail szolgáltatás, amely a magánéletre, a titkosításra, a biztonságra és az egyszerű használatra helyezi a hangsúlyt. They have been in operation since 2013. Proton AG is based in Geneva, Switzerland.

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

Free accounts have some limitations, such as not being able to search body text and not having access to [Proton Mail Bridge](https://proton.me/mail/bridge), which is required to use a [recommended desktop email client](email-clients.md) (e.g., Thunderbird). A fizetős fiókok olyan funkciókat is tartalmaznak, mint a Proton Mail Bridge, további tárhely és egyéni domainek támogatása. If you have the Proton Unlimited plan or any multi-user Proton plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

A Proton Mail alkalmazást 2021. november 9-én a [Securitum](https://research.securitum.com) [tanúsította](https://proton.me/blog/security-audit-all-proton-apps).

Proton Mail has internal crash reports that are **not** shared with third parties. This can be disabled in the web app: :gear: → **All Settings** → **Account** → **Security and privacy** → **Privacy and data collection**.

#### :material-check:{ .pg-green } Egyedi domainek és álnevek

A fizetős Proton Mail előfizetők saját domain címmel is használhatják a szolgáltatást, vagy egy [gyűjtőcímet](https://proton.me/support/catch-all) hozhatnak létre. A Proton Mail támogatja [az alcímzést](https://proton.me/support/creating-aliases) is, ami hasznos azok számára, akik nem akarnak domaint vásárolni.

#### :material-check:{ .pg-green } Privát fizetési módok

Proton Mail [accepts](https://proton.me/support/payment-options) **cash** by mail in addition to standard credit/debit card, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), and PayPal payments.

#### :material-check:{ .pg-green } Fiók biztonsága

Proton Mail supports TOTP [two-factor authentication](https://proton.me/support/two-factor-authentication-2fa) and [hardware security keys](https://proton.me/support/2fa-security-key) using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two-factor authentication first.

#### :material-check:{ .pg-green } Adatbiztonság

A Proton Mail [zéró hozzáférésű titkosítással](https://proton.me/blog/zero-access-encryption) védi az e-maileket és [naptárakat](https://proton.me/news/protoncalendar-security-model). A zéró hozzáférésű titkosítással védett adatokhoz csak Ön férhet hozzá.

A [Proton Contactsban](https://proton.me/support/proton-contacts) tárolt bizonyos információk, például a megjelenített nevek és e-mail címek nem biztosítottak zéró hozzáférésű titkosítással. A zéró hozzáférésű titkosítást támogató kapcsolati mezők, például a telefonszámok, lakat ikonjával vannak jelölve.

#### :material-check:{ .pg-green } E-mail titkosítás

A Proton Mail [integrálta az OpenPGP titkosítást](https://proton.me/support/how-to-use-pgp) a webmailjébe. A más Proton Mail-fiókokba küldött e-mailek automatikusan titkosítva vannak, és a nem Proton Mail-címekre küldött, OpenPGP-kulccsal rendelkező e-mailek titkosítása egyszerűen engedélyezhető a fiók beállításaiban. Proton also supports automatic external key discovery with WKD. Ez azt jelenti, hogy a WKD-t használó más szolgáltatóknak küldött e-maileket automatikusan az OpenPGP-vel is titkosítja, anélkül, hogy manuálisan kellene nyilvános PGP-kulcsokat cserélnie a kapcsolattartóival. Az [OpenPGP nélkül, nem Proton Mail címekre küldött üzeneteket titkosíthatod](https://proton.me/support/password-protected-emails), anélkül, hogy a címzetteknek Proton Mail fiókot kellene regisztrálniuk.

A Proton Mail a Proton-fiókok nyilvános kulcsait is közzéteszi HTTP-n keresztül a WKD-ből. This allows people who don't use Proton Mail to find the OpenPGP keys of Proton Mail accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Proton's own domains, like `@proton.me`. If you use a custom domain, you must [configure WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Fiók megszüntetése

Ha előfizetéssel rendelkezel, de 14 napon túli [fizetetlen számlád](https://proton.me/support/delinquency) van, nem férhetsz hozzá adataidhoz. 30 nap elteltével fiókod fizetésképtelenné válik, és nem fogadja a beérkező leveleket. Ebben az időszakban továbbra is kiszámlázzák a szolgáltatást. Proton will [delete inactive free accounts](https://proton.me/support/inactive-accounts) after one year. You **cannot** reuse the email address of a deactivated account.

#### :material-information-outline:{ .pg-blue } További funkciók

Proton Mail's [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) plan also enables access to other Proton services in addition to providing multiple custom domains, unlimited hide-my-email aliases, and 500 GB of storage.

### Mailbox Mail

<div class="admonition recommendation" markdown>

![Mailbox Mail logo](assets/img/email/mailbox-mail.svg){ align=right }

**Mailbox Mail** is an email service with a focus on being secure, ad-free, and powered by 100% eco-friendly energy. 2014 óta működnek. Mailbox Mail is based in Berlin, Germany.

Accounts start with up to 2 GB storage, which can be upgraded as needed.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Letöltés</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Egyedi domainek és álnevek

Mailbox Mail lets you use your own domain, and they support [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) addresses. Mailbox Mail also supports [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green } Privát fizetési módok

Mailbox Mail doesn't accept any cryptocurrencies as a result of their payment processor BitPay suspending operations in Germany. However, they do accept **cash** by mail, **cash** payment to bank account, bank transfer, credit card, PayPal, and a couple of German-specific processors: Paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } Fiók biztonsága

Mailbox Mail supports [two-factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. You can use either TOTP or a [YubiKey](security-keys.md#yubikey) via the [YubiCloud](https://yubico.com/products/services-software/yubicloud). Web standards such as [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) are not yet supported.

#### :material-information-outline:{ .pg-blue } Adatbiztonság

Mailbox Mail allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). A kapott új üzeneteket ezután azonnal titkosítja a nyilvános kulcsával.

However, [Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox Mail, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. A [standalone option](calendar.md) may be more appropriate for that data.

#### :material-check:{ .pg-green } E-mail titkosítás

Mailbox Mail has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox Mail's servers. Ez a funkció akkor hasznos, ha a távoli címzett nem rendelkezik OpenPGP-vel, és nem tudja visszafejteni az e-mail másolatát a saját postafiókjában.

Mailbox Mail also supports the discovery of public keys via HTTP from their WKD. This allows people outside of Mailbox Mail to find the OpenPGP keys of Mailbox Mail accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Mailbox Mail's own domains, like `@mailbox.org`. If you use a custom domain, you must [configure WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Fiók megszüntetése

Your account will be set to a restricted user account when your contract ends. It will be irrevocably deleted after [30 days](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } További funkciók

You can access your Mailbox Mail account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). However, their webmail interface cannot be accessed via their .onion service, and you may experience TLS certificate errors.

Minden fiókhoz korlátozott felhőalapú tárhely tartozik, amely [titkosítható](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox Mail also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox Mail also supports [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) in addition to standard access protocols like IMAP and POP3.

Mailbox Mail has a digital legacy feature for all plans. You can choose whether you want any of your data to be passed to heirs, providing that they apply and provide your testament. Alternatívaként nevet és címet is megadhatsz egy személynek.

## További szolgáltatók

Ezek a szolgáltatók zéró hozzáférésű titkosítással tárolják az e-maileket, így kiválóan alkalmasak a tárolt e-mailek biztonságban tartására. Nem támogatják azonban a különböző szolgáltatók közötti E2EE-kommunikáció interoperábilis titkosítási szabványait.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](#tuta)

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

#### :material-check:{ .pg-green } Egyedi domainek és álnevek

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/support#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/support#plus), but you can use a [catch-all](https://tuta.com/support#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } Privát fizetési módok

Tuta only directly accepts credit cards and PayPal, however [**cryptocurrency**](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with ProxyStore.

#### :material-check:{ .pg-green } Fiók biztonsága

Tuta supports [two-factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Adatbiztonság

Tuta has [zero-access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). Ez azt jelenti, hogy a fiókodban tárolt üzeneteket és egyéb adatokhoz kizárólag te férhetsz hozzá.

#### :material-information-outline:{ .pg-blue } E-mail titkosítás

A Tuta [nem használja az OpenPGP-t](https://tuta.com/support/#pgp). A Tuta fiókok csak akkor fogadhatnak titkosított e-maileket nem Tuta e-mail fiókokból, ha azokat egy [ideiglenes Tuta postafiókon](https://tuta.com/support/#encrypted-email-external) keresztül küldik.

#### :material-information-outline:{ .pg-blue } Fiók megszüntetése

Tuta will [delete inactive free accounts](https://tuta.com/support#inactive-accounts) after six months. Egy deaktivált ingyenes fiókot újra felhasználhatsz, ha fizetsz érte.

#### :material-information-outline:{ .pg-blue } További funkciók

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/secure-email-for-non-profit) for free or with a heavy discount.

## Követelmények

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an email provider, and conduct your own research to ensure the email provider you choose is the right choice for you.

### Technológia

Ezeket a funkciókat fontosnak tartjuk a biztonságos és optimális szolgáltatás nyújtása érdekében. You should consider whether the provider has the features you require.

**Alap Elvárások Minősítéshez:**

- Must encrypt email account data at rest with zero-access encryption.
- Must be capable of exporting emails as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .EML with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Az egyéni domain nevek azért fontosak a felhasználók számára, mert lehetővé teszik számukra, hogy megőrizzék a függetlenedési képességüket a szolgáltatástól, ha az rosszra fordulna, vagy ha egy másik vállalat felvásárolná, amely nem helyezi előtérbe az adatvédelmet.
- Must operate on owned infrastructure, i.e. not built upon third-party email service providers.

**Legjobb esetben:**

- Should encrypt all account data (contacts, calendars, etc.) at rest with zero-access encryption.
- Should provide integrated webmail E2EE/PGP encryption as a convenience.
- Should support WKD to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key with this command: `gpg --locate-key example_user@example.com`.
- Ideiglenes postafiók támogatása külső felhasználók számára. This is useful when you want to send an encrypted email without sending an actual copy to your recipient. Ezek az e-mailek általában korlátozott élettartamúak, majd automatikusan törlődnek. A címzettnek nem kell semmilyen titkosítást konfigurálnia, mint az OpenPGP esetében.
- Should support [sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Should allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Az egyéni domain nevek azért fontosak a felhasználók számára, mert lehetővé teszik számukra, hogy megőrizzék a függetlenedési képességüket a szolgáltatástól, ha az rosszra fordulna, vagy ha egy másik vállalat felvásárolná, amely nem helyezi előtérbe az adatvédelmet.
- Catch-all or alias functionality for those who use their own domains.
- Should use standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.
- Email provider's services should be available via an [onion service](https://en.wikipedia.org/wiki/.onion).

### Adatvédelem

Jobban szeretjük, ha az általunk ajánlott szolgáltatók a lehető legkevesebb adatot gyűjtik.

**Alap elvárások minősítéshez:**

- Must protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Must not require personally identifiable information (PII) besides a username and a password.
- Privacy policy must meet the requirements defined by the GDPR.

**Legjobb esetben:**

- Should accept [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Should be hosted in a jurisdiction with strong email privacy protection laws.

### Adatbiztonság

Email servers deal with a lot of very sensitive data. We expect that providers will adopt industry best practices in order to protect their customers.

**Alap elvárások minősítéshez:**

- Protection of webmail with 2FA, such as [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Zero-access encryption, which builds on encryption at rest. A szolgáltató nem rendelkezik a birtokában lévő adatok visszafejtési kulcsaival. Ez megakadályozza, hogy egy rosszhiszemű alkalmazott kiszivárogtassa az adatokat, amelyekhez hozzáfér, vagy egy távoli ellenfél a szerverhez való jogosulatlan hozzáféréssel kiadja az ellopott adatokat.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) támogatás.
- Nincsenek TLS-hibák vagy sebezhetőségek, amikor olyan eszközökkel profilozzák, mint a [Hardenize](https://hardenize.com), a [testssl.sh](https://testssl.sh) vagy a [Qualys SSL Labs](https://ssllabs.com/ssltest); ez magában foglalja a tanúsítványokkal kapcsolatos hibákat és a gyenge DH-paramétereket, például azokat, amelyek a [Logjamhoz](https://en.wikipedia.org/wiki/Logjam_(computer_security)) vezettek.
- A server suite preference (optional on TLS 1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- Érvényes [MTA-STS](https://tools.ietf.org/html/rfc8461) és [TLS-RPT](https://tools.ietf.org/html/rfc8460) házirend.
- Érvényes [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) rekordok.
- Érvényes [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) és [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) rekordok.
- Must have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. Ha DMARC-hitelesítést használ, a házirendet `elutasításra` vagy `karanténba` kell állítani.
- A TLS 1.2 vagy újabb szervercsomag előnyben részesítése és az [RFC8996](https://datatracker.ietf.org/doc/rfc8996) tervezése.
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) beküldés, feltéve, hogy SMTP-t használnak.
- Weboldal biztonsági szabványok, mint például:
    - [HTTP szigorú szállítási biztonság (Strict Transport Security)](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Alforrás integritás](https://en.wikipedia.org/wiki/Subresource_Integrity), ha külső tartományokból tölt be dolgokat.
- Must support viewing of [message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**Legjobb esetben:**

- Should support hardware authentication, i.e. U2F and [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [DNS-hitelesítésszolgáltatói engedélyezési (CAA) erőforrásrekord](https://tools.ietf.org/html/rfc6844) a DANE-támogatás mellett.
- Should implement [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Published security audits from a reputable, third-party firm.
- Bug-bounty programok és/vagy összehangolt sebezhetőség-közzétételi folyamat.
- Weboldal biztonsági szabványok, mint például:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Megbízhatóság

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? Az általunk ajánlott szolgáltatóktól elvárjuk, hogy nyilvánosak legyenek a tulajdonlásukról vagy vezetésükről. Szeretnénk továbbá gyakori átláthatósági jelentéseket látni, különösen a kormányzati kérelmek kezelésének módját illetően.

**Alap elvárások minősítéshez:**

- Átlátható vezetés vagy tulajdonlás.

**Legjobb esetben:**

- Gyakori átláthatósági jelentések.

### Marketing

With the email providers we recommend, we like to see responsible marketing.

**Alap elvárások minősítéshez:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.).
- Must not have any irresponsible marketing, which can include the following:
    - Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
    - Guarantees of protecting anonymity 100%. When someone makes a claim that something is 100%, it means there is no certainty for failure. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:
        - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software such as Tor
        - [Böngésző fingerprintelés](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Legjobb esetben:**

- Clear and easy-to-read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### További funkciók

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
