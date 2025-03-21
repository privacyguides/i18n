---
meta_title: "Titkosított privát e-mail ajánlások – Privacy Guides"
title: "Email szolgáltatások"
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

| Provider                    | OpenPGP / WKD                          | IMAP / SMTP                                                | Zero Access Encryption                               | Anonymous Payments            |
| --------------------------- | -------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------- | ----------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Paid plans only | :material-check:{ .pg-green }                        | Cash                          |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                              | :material-information-outline:{ .pg-blue } Mail only | Cash                          |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                        | Monero & Cash via third-party |

Az itt ajánlott email szolgáltatók mellett (vagy helyett) érdemes megfontolni egy dedikált [e-mail alias szolgáltatást](email-aliasing.md) is a magánélet védelme érdekében. Ezek a szolgáltatások többek között segíthetnek megvédeni a valódi potaládádat a spamektől, megakadályozhatják, hogy a marketingesek összekapcsolják a fiókjaidat, és PGP-vel titkosíthatják az összes bejövő üzenetedet.

- [További információ :material-arrow-right-drop-circle:](email-aliasing.md)

## OpenPGP-kompatibilis szolgáltatások

Ezek a szolgáltatók natívan támogatják az OpenPGP titkosítást/visszafejtést és a [Web Key Directory szabványt](basics/email-security.md#what-is-the-web-key-directory-standard), lehetővé téve a szolgáltatófüggetlen, végponttól-végpontig titkosított emaileket. Például egy Proton Mail felhasználó küldhet végponttól-végpontig titkosított üzenetet egy Mailbox.org felhasználónak, de fogadhatsz OpenPGP-titkosított értesítéseket olyan internetes szolgáltatásoktól is, amelyek támogatják azt.

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

A **Proton Mail** egy olyan e-mail szolgáltatás, amely a magánéletre, a titkosításra, a biztonságra és az egyszerű használatra helyezi a hangsúlyt. They have been in operation since 2013. Proton AG is based in Geneva, Switzerland. The Proton Mail Free plan comes with 500 MB of Mail storage, which you can increase up to 1 GB for free.

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

Az ingyenes fiókoknak vannak bizonyos korlátai, például nem tudnak keresni a szövegben, és nem férnek hozzá a [Proton Mail Bridge-hez](https://proton.me/mail/bridge), ami egy [ajánlott asztali e-mail kliens](email-clients.md) (pl. Thunderbird) használatához szükséges átjáró. A fizetős fiókok olyan funkciókat is tartalmaznak, mint a Proton Mail Bridge, további tárhely és egyéni domainek támogatása. A Proton Mail alkalmazást 2021. november 9-én a [Securitum](https://research.securitum.com) [tanúsította](https://proton.me/blog/security-audit-all-proton-apps).

If you have the Proton Unlimited plan or any multi-user Proton plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

Proton Mail has internal crash reports that are **not** shared with third parties. This can be disabled in the web app: :gear: → **All Settings** → **Account** → **Security and privacy** → **Privacy and data collection**.

#### :material-check:{ .pg-green } Egyedi domainek és álnevek

A fizetős Proton Mail előfizetők saját domain címmel is használhatják a szolgáltatást, vagy egy [gyűjtőcímet](https://proton.me/support/catch-all) hozhatnak létre. A Proton Mail támogatja [az alcímzést](https://proton.me/support/creating-aliases) is, ami hasznos azok számára, akik nem akarnak domaint vásárolni.

#### :material-check:{ .pg-green } Privát fizetési módok

A Proton Mail készpénzt is [elfogad](https://proton.me/support/payment-options) postai úton a szokásos hitelkártyás, [Bitcoin-](advanced/payments.md#other-coins-bitcoin-ethereum-etc) és PayPal-fizetési módok mellett.

#### :material-check:{ .pg-green } Fiók biztonsága

Proton Mail supports TOTP [two-factor authentication](https://proton.me/support/two-factor-authentication-2fa) and [hardware security keys](https://proton.me/support/2fa-security-key) using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two-factor authentication first.

#### :material-check:{ .pg-green } Adatbiztonság

A Proton Mail [zéró hozzáférésű titkosítással](https://proton.me/blog/zero-access-encryption) védi az e-maileket és [naptárakat](https://proton.me/news/protoncalendar-security-model). A zéró hozzáférésű titkosítással védett adatokhoz csak Ön férhet hozzá.

A [Proton Contactsban](https://proton.me/support/proton-contacts) tárolt bizonyos információk, például a megjelenített nevek és e-mail címek nem biztosítottak zéró hozzáférésű titkosítással. A zéró hozzáférésű titkosítást támogató kapcsolati mezők, például a telefonszámok, lakat ikonjával vannak jelölve.

#### :material-check:{ .pg-green } E-mail titkosítás

A Proton Mail [integrálta az OpenPGP titkosítást](https://proton.me/support/how-to-use-pgp) a webmailjébe. A más Proton Mail-fiókokba küldött e-mailek automatikusan titkosítva vannak, és a nem Proton Mail-címekre küldött, OpenPGP-kulccsal rendelkező e-mailek titkosítása egyszerűen engedélyezhető a fiók beállításaiban. A Proton támogatja az automatikus külső kulcskeresést a [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) segítségével. Ez azt jelenti, hogy a WKD-t használó más szolgáltatóknak küldött e-maileket automatikusan az OpenPGP-vel is titkosítja, anélkül, hogy manuálisan kellene nyilvános PGP-kulcsokat cserélnie a kapcsolattartóival. Az [OpenPGP nélkül, nem Proton Mail címekre küldött üzeneteket titkosíthatod](https://proton.me/support/password-protected-emails), anélkül, hogy a címzetteknek Proton Mail fiókot kellene regisztrálniuk.

A Proton Mail a Proton-fiókok nyilvános kulcsait is közzéteszi HTTP-n keresztül a WKD-ből. Ez lehetővé teszi, hogy a Proton Mailt nem használók is könnyen megtalálják a Proton Mail fiókok OpenPGP-kulcsait a szolgáltatóközi E2EE-hez. Ez csak a Proton saját domainjeire végződő e-mail címekre vonatkozik, mint például a @proton.me. Ha egyéni tartományt használsz, kézzel kell [konfigurálni a WKD-t](./basics/email-security.md#what-is-the-web-key-directory-standard).

#### :material-information-outline:{ .pg-blue } Fiók megszüntetése

Ha előfizetéssel rendelkezel, de 14 napon túli [fizetetlen számlád](https://proton.me/support/delinquency) van, nem férhetsz hozzá adataidhoz. 30 nap elteltével fiókod fizetésképtelenné válik, és nem fogadja a beérkező leveleket. Ebben az időszakban továbbra is kiszámlázzák a szolgáltatást. Proton will [delete inactive free accounts](https://proton.me/support/inactive-accounts) after one year. You **cannot** reuse the email address of a deactivated account.

#### :material-information-outline:{ .pg-blue } További funkciók

Proton Mail's [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) plan also enables access to other Proton services in addition to providing multiple custom domains, unlimited hide-my-email aliases, and 500 GB of storage.

A Proton Mail nem kínál digitális örökség funkciót.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

**A **Mailbox.org** egy olyan e-mail szolgáltatás, amelynek középpontjában a biztonság, a reklámmentesség és a 100%-ban környezetbarát energiával működő, magánhálózatról biztosított energia áll. 2014 óta működnek. A Mailbox.org székhelye Berlinben, Németországban található. Accounts start with up to 2 GB storage, which can be upgraded as needed.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Letöltés</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Egyedi domainek és álnevek

A Mailbox.org lehetővé teszi a saját domain használatáz, és támogatja a [gyűjtőcímeket](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name). A Mailbox.org támogatja az [alcímzést](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it) is, ami akkor hasznos, ha nem szeretne domain-t vásárolni.

#### :material-check:{ .pg-green } Privát fizetési módok

A Mailbox.org nem fogad el semmilyen kriptovalutát, mivel a fizetési szolgáltatójuk, a BitPay felfüggesztette működését Németországban. However, they do accept cash by mail, cash payment to bank account, bank transfer, credit card, PayPal and a couple of German-specific processors: paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } Fiók biztonsága

Mailbox.org supports [two-factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. A TOTP vagy a [YubiKey](https://en.wikipedia.org/wiki/YubiKey) a [YubiCloudon](https://yubico.com/products/services-software/yubicloud) keresztül használható. Az olyan webes szabványok, mint a [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn), még nem támogatottak.

#### :material-information-outline:{ .pg-blue } Adatbiztonság

A Mailbox.org lehetővé teszi a bejövő levelek titkosítását a [titkosított postafiók](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox) segítségével. A kapott új üzeneteket ezután azonnal titkosítja a nyilvános kulcsával.

A Mailbox.org által használt szoftverplatform, az [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange) azonban [nem támogatja](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) a címjegyzék és a naptár titkosítását. Az ilyen információk tárolásához megfelelőbb lehet egy [önálló alternatíva](calendar.md).

#### :material-check:{ .pg-green } E-mail titkosítás

A Mailbox.org webmailbe [beépített titkosítást](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) alkalmaz, ami leegyszerűsíti az üzenetek küldését nyilvános OpenPGP-kulcsokkal rendelkező személyeknek. Lehetővé teszik továbbá, hogy a [távoli címzettek visszafejtsenek egy e-mailt](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) a Mailbox.org szerverein. Ez a funkció akkor hasznos, ha a távoli címzett nem rendelkezik OpenPGP-vel, és nem tudja visszafejteni az e-mail másolatát a saját postafiókjában.

A Mailbox.org támogatja a nyilvános kulcsok HTTP-n keresztüli keresését is a [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) segítségével. Ez lehetővé teszi, hogy a Mailbox.org-ot nem használók is könnyen megtalálják a Mailbox.org fiókok OpenPGP-kulcsait a szolgáltatóközi végponttól-végpontig terjedő titkosításhoz. Ez csak a Mailbox.org saját domainjeire végződő e-mail címekre vonatkozik, mint például a @mailbox.org. Ha egyéni tartományt használsz, kézzel kell [konfigurálni a WKD-t](./basics/email-security.md#what-is-the-web-key-directory-standard).

#### :material-information-outline:{ .pg-blue } Fiók megszüntetése

Your account will be set to a restricted user account when your contract ends. It will be irrevocably deleted after [30 days](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } További funkciók

A Mailbox.org fiók a [.onion szolgáltatásuk](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org) segítségével IMAP/SMTP-n keresztül is elérhető. However, their webmail interface cannot be accessed via their .onion service, and you may experience TLS certificate errors.

Minden fiókhoz korlátozott felhőalapú tárhely tartozik, amely [titkosítható](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). A mailbox.org kínálja a [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely) aliast is, amely érvényesíti a TLS titkosítást a levelezőszerverek közötti kapcsolaton, ennek hiányában az üzenet egyáltalán nem lesz elküldve. A Mailbox.org támogatja az [Exchange ActiveSync-et](https://en.wikipedia.org/wiki/Exchange_ActiveSync) is a szabványos hozzáférési protokollok, például az IMAP és a POP3 mellett.

A Mailbox.org minden előfizetési csomagban rendelkezik digitális örökség funkcióval. Elnöntheted, hogy szeretnéd-e, hogy adataid bármelyik örökösre szálljanak, feltéve, hogy ezt kérelmezed és végrendelkezésben rögzíted. Alternatívaként nevet és címet is megadhatsz egy személynek.

## További szolgáltatók

Ezek a szolgáltatók zéró hozzáférésű titkosítással tárolják az e-maileket, így kiválóan alkalmasak a tárolt e-mailek biztonságban tartására. Nem támogatják azonban a különböző szolgáltatók közötti E2EE-kommunikáció interoperábilis titkosítási szabványait.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (formerly *Tutanota*) is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since 2011 and is based in Hanover, Germany. Free accounts start with 1 GB of storage.

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

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with ProxyStore.

#### :material-check:{ .pg-green } Fiók biztonsága

Tuta supports [two-factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Adatbiztonság

Tuta has [zero access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). Ez azt jelenti, hogy a fiókodban tárolt üzeneteket és egyéb adatokhoz kizárólag te férhetsz hozzá.

#### :material-information-outline:{ .pg-blue } E-mail titkosítás

A Tuta [nem használja az OpenPGP-t](https://tuta.com/support/#pgp). A Tuta fiókok csak akkor fogadhatnak titkosított e-maileket nem Tuta e-mail fiókokból, ha azokat egy [ideiglenes Tuta postafiókon](https://tuta.com/support/#encrypted-email-external) keresztül küldik.

#### :material-information-outline:{ .pg-blue } Fiók megszüntetése

Tuta will [delete inactive free accounts](https://tuta.com/support#inactive-accounts) after six months. Egy deaktivált ingyenes fiókot újra felhasználhatsz, ha fizetsz érte.

#### :material-information-outline:{ .pg-blue } További funkciók

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/secure-email-for-non-profit) for free or with a heavy discount.

A Tuta nem kínál digitális örökség funkciót.

## Saját üzemeltetésű email

A haladó rendszergazdák fontolóra vehetik saját e-mail szerver felállítását. A levelezőszerverek figyelmet és folyamatos karbantartást igényelnek a biztonság és a megbízható levélkézbesítés fenntartása érdekében. In addition to the "all-in-one" solutions below, we've picked out a few articles that cover a more manual approach:

- [Levelezőszerver beállítása OpenSMTPD, Dovecot és Rspamd segítségével](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://www.c0ffee.net/blog/mail-server-guide) (August 2017)

### Stalwart

<div class="admonition recommendation" markdown>

![Stalwart logo](assets/img/email/stalwart.svg){ align=right }

**Stalwart** is a newer mail server written in Rust which supports JMAP in addition to the standard IMAP, POP3, and SMTP. It has a wide variety of configuration options, but it also defaults to very reasonable settings (in terms of both security and features) making it easy to use immediately. It has web-based administration with TOTP 2FA support, and it allows you to enter your public PGP key to encrypt **all** incoming messages.

[:octicons-home-16: Homepage](https://stalw.art){ .md-button .md-button--primary }
[:octicons-info-16:](https://stalw.art/docs/get-started){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/stalwartlabs){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/stalwartlabs){ .card-link title="Contribute" }

</div>

Stalwart's [PGP implementation](https://stalw.art/docs/encryption/overview) is unique among our self-hosted recommendations, and allows you to operate your own mail server with zero-knowledge message storage. If you additionally configure Web Key Directory on your domain, and if you use an email client which supports PGP and Web Key Directory for outgoing mail (like Thunderbird), then this is the easiest way to get self-hosted E2EE compatibility with all [Proton Mail](#proton-mail) users.

Stalwart does **not** have an integrated webmail, so you will need to use it with a [dedicated email client](email-clients.md) (or find an open-source webmail to self-host, like Nextcloud's Mail app). We use Stalwart for our own internal email at *Privacy Guides*.

### Mailcow

<div class="admonition recommendation" markdown>

![Mailcow logo](assets/img/email/mailcow.svg){ align=right }

A **Mailcow** egy fejlettebb levelezőszerver, amely tökéletes azok számára, akik kicsit több Linux-tapasztalattal rendelkeznek. It has everything you need in a Docker container: a mail server with DKIM support, antivirus and spam monitoring, webmail and ActiveSync with SOGo, and web-based administration with 2FA support.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title="Contribute" }

</div>

### Mail-in-a-Box

<div class="admonition recommendation" markdown>

![Mail-in-a-Box logo](assets/img/email/mail-in-a-box.svg){ align=right }

A **Mail-in-a-Box** egy automatizált beállítási szkript egy levelezőszerver telepítéséhez Ubuntun. Célja, hogy megkönnyítse az emberek számára saját levelezőszerverük beállítását.

[:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }

</div>

## Követelmények

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an email provider, and conduct your own research to ensure the email provider you choose is the right choice for you.

### Technológia

Ezeket a funkciókat fontosnak tartjuk a biztonságos és optimális szolgáltatás nyújtása érdekében. Meg kell vizsgálnod, hogy az adott szolgáltató rendelkezik-e az általad igényelt funkciókkal.

**Alap Elvárások Minősítéshez:**

- Az email fiókok adatai alapértelmezetten zéró hozzáféréssel legyenek titkosítva.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .EML with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Lehetővé teszi a felhasználók számára, hogy saját [domainnevüket](https://en.wikipedia.org/wiki/Domain_name) használják. Az egyéni domain nevek azért fontosak a felhasználók számára, mert lehetővé teszik számukra, hogy megőrizzék a függetlenedési képességüket a szolgáltatástól, ha az rosszra fordulna, vagy ha egy másik vállalat felvásárolná, amely nem helyezi előtérbe az adatvédelmet.
- Saját infrastruktúrán működik, azaz nem harmadik féltől származó e-mail szolgáltatóra épül.

**Legjobb esetben:**

- Zéró hozzáférésű titkosítással titkosítja az összes fiókadatot (névjegyek, naptárak stb.).
- Integrált webmail E2EE/PGP titkosítás, amely kényelmi funkciót biztosít.
- A [WKD](https://wiki.gnupg.org/WKD) támogatása a nyilvános OpenPGP kulcsok HTTP-n keresztüli jobb felderítésének lehetővé tételéhez. A GnuPG felhasználók kulcsot szerezhetnek a következő paranccsal: `gpg --locate-key example_user@example.com`
- Ideiglenes postafiók támogatása külső felhasználók számára. Ez akkor hasznos, ha titkosított e-mailt szeretne küldeni anélkül, hogy a címzettnek tényleges másolatot küldene. Ezek az e-mailek általában korlátozott élettartamúak, majd automatikusan törlődnek. A címzettnek nem kell semmilyen titkosítást konfigurálnia, mint az OpenPGP esetében.
- Az emailszolgáltató weboldalának elérhetősége egy [.onion szolgáltatáson](https://en.wikipedia.org/wiki/.onion) keresztül.
- Az [alcímzés](https://en.wikipedia.org/wiki/Email_address#Sub-addressing) támogatása.
- Catch-all or alias functionality for those who use their own domains.
- Use of standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). A szabványos hozzáférési protokollok biztosítják, hogy az ügyfelek könnyen letölthessék az összes e-mailjüket, ha másik szolgáltatóhoz szeretnének váltani.

### Adatvédelem

Jobban szeretjük, ha az általunk ajánlott szolgáltatók a lehető legkevesebb adatot gyűjtik.

**Alap elvárások minősítéshez:**

- Protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- A felhasználónevet és jelszót leszámítva ne kérjen személyazonosításra alkalmas adatokat (PII).
- A GDPR által meghatározott követelményeknek megfelelő adatvédelmi politika.

**Legjobb esetben:**

- Elfogadja az [anonim fizetési lehetőségeket](advanced/payments.md)[(kriptopénz](cryptocurrency.md), készpénz, ajándékkártyák stb.)
- Olyan joghatóságban van elhelyezve, ahol erős e-mail adatvédelmi törvények vannak érvényben.

### Adatbiztonság

Az e-mail szerverek sok nagyon érzékeny adatot kezelnek. We expect that providers will adopt best industry practices in order to protect their customers.

**Alap elvárások minősítéshez:**

- A webmail védelme 2FA-val, például TOTP-vel.
- Zero access encryption, which builds on encryption at rest. A szolgáltató nem rendelkezik a birtokában lévő adatok visszafejtési kulcsaival. Ez megakadályozza, hogy egy rosszhiszemű alkalmazott kiszivárogtassa az adatokat, amelyekhez hozzáfér, vagy egy távoli ellenfél a szerverhez való jogosulatlan hozzáféréssel kiadja az ellopott adatokat.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) támogatás.
- Nincsenek TLS-hibák vagy sebezhetőségek, amikor olyan eszközökkel profilozzák, mint a [Hardenize](https://hardenize.com), a [testssl.sh](https://testssl.sh) vagy a [Qualys SSL Labs](https://ssllabs.com/ssltest); ez magában foglalja a tanúsítványokkal kapcsolatos hibákat és a gyenge DH-paramétereket, például azokat, amelyek a [Logjamhoz](https://en.wikipedia.org/wiki/Logjam_(computer_security)) vezettek.
- Kiszolgálói csomag preferencia (a TLSv1.3 esetében opcionális) az erős titkosítási csomagok számára, amelyek támogatják a továbbított titkosítást és a hitelesített titkosítást.
- Érvényes [MTA-STS](https://tools.ietf.org/html/rfc8461) és [TLS-RPT](https://tools.ietf.org/html/rfc8460) házirend.
- Érvényes [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) rekordok.
- Érvényes [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) és [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) rekordok.
- Rendelkezzen megfelelő [DMARC](https://en.wikipedia.org/wiki/DMARC) rekorddal és házirenddel, vagy használjon [ARC-t](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) a hitelesítéshez. Ha DMARC-hitelesítést használ, a házirendet `elutasításra` vagy `karanténba` kell állítani.
- A TLS 1.2 vagy újabb szervercsomag előnyben részesítése és az [RFC8996](https://datatracker.ietf.org/doc/rfc8996) tervezése.
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) beküldés, feltéve, hogy SMTP-t használnak.
- Weboldal biztonsági szabványok, mint például:
    - [HTTP szigorú szállítási biztonság (Strict Transport Security)](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Alforrás integritás](https://en.wikipedia.org/wiki/Subresource_Integrity), ha külső tartományokból tölt be dolgokat.
- Must support viewing of [message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**Legjobb esetben:**

- A hardveres hitelesítés támogatása, pl. U2F and [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [DNS-hitelesítésszolgáltatói engedélyezési (CAA) erőforrásrekord](https://tools.ietf.org/html/rfc6844) a DANE-támogatás mellett.
- Implementation of [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Közzétett biztonsági felülvizsgálatok egy megbízható harmadik feles cégtől.
- Bug-bounty programok és/vagy összehangolt sebezhetőség-közzétételi folyamat.
- Weboldal biztonsági szabványok, mint például:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Megbízhatóság

A pénzügyeidet sem bíznád egy hamis személyazonosságú emberre, akkor miért bíznád rájuk az e-mailjeidet? Az általunk ajánlott szolgáltatóktól megköveteljük, hogy nyilvánosan nyilatkozzanak a tulajdonlásukról vagy vezetésükről. Szeretnénk továbbá gyakori átláthatósági jelentéseket látni, különösen a kormányzati kérelmek kezelésének módját illetően.

**Alap elvárások minősítéshez:**

- Átlátható vezetés vagy tulajdonlás.

**Legjobb esetben:**

- Gyakori átláthatósági jelentések.

### Marketing

With the email providers we recommend, we like to see responsible marketing.

**Alap elvárások minősítéshez:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.).

Must not have any irresponsible marketing, which can include the following:

- A "feltörhetetlen titkosítás" állítása. A titkosítást úgy kell használni, hogy annak nem titkos jellege is figyelembe legyen véve a jövőben, amikor már rendelkezésre áll a feltörésére alkalmas technológia.
- Az anonimitás 100%-os védelmének garantálása. Ha valaki azt állítja, hogy valami 100%-os, az azt jelenti, hogy nem merülhet fel meghibásodás. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:

    - Olyan személyes adatok újrafelhasználása (pl. e-mail fiókok, egyedi álnevek stb.), amelyekhez anonimitási szoftverek (Tor, VPN stb.) nélkül jutottak hozzá.
    - [Böngésző ujjlenyomatolás](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Legjobb esetben:**

- Clear and easy to read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### További funkciók

Bár ezek nem szigorú követelmények, más kényelmi vagy adatvédelmi tényezőket is figyelembe vettünk, amikor eldöntöttük, mely szolgáltatókat ajánljuk.
