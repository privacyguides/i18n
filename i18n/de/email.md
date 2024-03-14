---
meta_title: "Empfehlungen für verschlüsselte private E-Mail-Dienste - Privacy Guides"
title: "E-Mail Dienste"
icon: material/email
description: Diese E-Mail-Dienstleister speichern deine E-Mails sicher und viele davon bieten auch interoperable OpenPGP-Verschlüsselung mit anderen Anbietern.
cover: email.webp
---

E-Mail ist praktisch eine Voraussetzung für die Nutzung aller Online-Dienste, wir empfehlen sie jedoch nicht zur Kommunikation von Mensch zu Mensch. Anstatt E-Mails für die Kontaktaufnahme mit anderen Personen zu verwenden, überleg ob du einen Instant Messenger benutzen kannst, der Forward Secrecy (auf Deutsch etwa "vorwärts gerichtete Geheimhaltung") unterstützt.

[Empfohlene Instant Messenger](real-time-communication.md ""){.md-button}

Für alles andere empfehlen wir eine Reihe von E-Mail-Anbietern, die auf nachhaltigen Geschäftsmodellen basieren und integrierte Sicherheits- und Datenschutzfunktionen bieten.

- [OpenPGP-kompatible E-Mail-Anbieter :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [Andere verschlüsselte Anbieter :material-arrow-right-drop-circle:](#more-providers)
- [E-Mail-Alias-Dienste :material-arrow-right-drop-circle:](#email-aliasing-services)
- [Selbstbetreibbare Optionen :material-arrow-right-drop-circle:](#self-hosting-email)

## OpenPGP-kompatible Dienste

Diese Anbieter unterstützen von Haus aus die OpenPGP-Ver- und Entschlüsselung sowie den Web Key Directory Standard, so dass anbieterunabhängige E2E-verschlüsselte E-Mails möglich sind. Zum Beispiel können Kunden von Proton Mail eine E2EE-Nachricht an Kunden von Mailbox.org senden oder sie können OpenPGP-verschlüsselte Benachrichtigungen von Internetdiensten erhalten, die dies unterstützen.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warnung</p>

Wenn du eine E2EE-Technologie wie OpenPGP verwendest, enthält deine E-Mail immer noch einige unverschlüsselte Metadaten im Header bzw. Quelltext der E-Mail, einschließlich der Betreffzeile! Lies mehr über [E-Mail-Metadaten](basics/email-security.md#email-metadata-overview).

OpenPGP unterstützt auch keine Forward Secrecy. Das heißt, wenn entweder dein privater Schlüssel oder der des Empfängers gestohlen wird, sind alle vorher damit verschlüsselten Nachrichten offen. [Wie schütze ich meine privaten Schlüssel?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** ist ein E-Mail-Dienst mit dem Schwerpunkt auf Datenschutz, Verschlüsselung, Sicherheit und Benutzerfreundlichkeit. Sie sind seit **2013** in Betrieb. Die Proton AG hat ihren Sitz in Genf, Schweiz. Konten im kostenlosen Tarif beginnen mit 1 GB Speicherplatz.

[:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion / Tor" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Dokumentation}
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

Kostenlose Konten haben einige Einschränkungen, wie z. B. die fehlende Möglichkeit Text zu durchsuchen und keinen Zugang zu [Proton Mail Bridge](https://proton.me/mail/bridge). Diese ist für die Verwendung eines [empfohlenen Desktop-E-Mail-Programms](email-clients.md) (z. B. Thunderbird) erforderlich. Bezahlte Konten umfassen Funktionen wie Proton Mail Bridge, zusätzlichen Speicher und die Nutzung eigener Domains. Am 9. November 2021 wurden durch [Securitum](https://research.securitum.com) ein Sicherheitsaudit durchgeführt und  die Anwendungen von Proton Mail [zertifiziert](https://proton.me/blog/security-audit-all-proton-apps).

Wenn du den Proton Unlimited, Business oder Visionary Tarif nutzt, erhältst du zusätzlich [SimpleLogin](#simplelogin) Premium kostenlos dazu.

Proton Mail hat interne Absturzberichte, die sie **nicht** mit Dritten teilen. Die Absturzberichte können in den Einstellungen deaktiviert werden: **Einstellungen** > **Gehe zu Einstellungen** > **Konto** > **Sicherheit und Datenschutz** > **Absturzberichte senden**.

#### :material-check:{ .pg-green } Eigene Domains und Aliase

Nutzer eines kostenpflichtigen Proton Mail Tarifs können ihre eigene Domain oder eine [Catch-All](https://proton.me/support/catch-all) Adresse nutzen. Proton Mail unterstützt auch [Subadressen](https://proton.me/support/creating-aliases), was für Personen nützlich ist, die keine eigene Domain erwerben möchten.

#### :material-check:{ .pg-green } Diskrete Zahlungsmöglichkeiten

Proton Mail akzeptiert, neben den üblichen Zahlungen per Kredit-/Debitkarte, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc)und PayPal, auch [Bargeld per Post](https://proton.me/support/payment-options).

#### :material-check:{ .pg-green } Kontosicherheit

Proton Mail unterstützt TOTP [Zwei-Faktor-Authentifizierung](https://proton.me/de/support/two-factor-authentication-2fa) und [Hardware-Sicherheitsschlüssel](https://proton.me/de/support/2fa-security-key) unter Verwendung der Standards FIDO2 oder U2F. Für die Verwendung eines Hardwaresicherheitsschlüssels muss zunächst die TOTP-Zwei-Faktor-Authentifizierung eingerichtet werden.

#### :material-check:{ .pg-green } Datensicherheit

Proton Mail verfügt über [Zero-Access-Verschlüsselung](https://proton.me/de/blog/zero-access-encryption) bei Ablage auf dem Server für deine E-Mails und [Kalender](https://proton.me/de/blog/protoncalendar-security-model). Die mit einer Zero-Access-Verschlüsselung gesicherten Daten sind nur für dich zugänglich.

Bestimmte Informationen, die in [Proton Contacts](https://proton.me/support/proton-contacts) gespeichert sind, wie z. B. Anzeigenamen und E-Mail-Adressen, sind nicht mit einer Zero-Access-Verschlüsselung gesichert. Kontaktfelder, die eine Zero-Access-Verschlüsselung unterstützen, wie z. B. Telefonnummern, sind mit einem Vorhängeschloss-Symbol gekennzeichnet.

#### :material-check:{ .pg-green } E-Mail-Verschlüsselung

Proton Mail hat [die OpenPGP-Verschlüsselung](https://proton.me/support/how-to-use-pgp) in sein Webmail integriert. E-Mails an andere Proton Mail-Konten werden automatisch verschlüsselt. Die Verschlüsselung an Nicht-Proton Mail-Adressen mit einem OpenPGP-Schlüssel kannst du ganz einfach in deinen Kontoeinstellungen aktivieren. Proton unterstützt auch die automatische Erkennung externer Schlüssel mit dem [Web Key Directory (WKD](https://wiki.gnupg.org/WKD)). Das bedeutet, dass E-Mails an andere Anbieter, die WKD verwenden, automatisch auch mit OpenPGP verschlüsselt werden, ohne dass du manuell öffentliche PGP-Schlüssel mit deinen Kontakten austauschen musst. Außerdem ist es möglich, [Nachrichten an Nicht-Proton-Mail-Adressen ohne OpenPGP zu verschlüsseln](https://proton.me/support/password-protected-emails), ohne dass die Empfänger ein Proton-Mail-Konto benötigen.

Auch veröffentlicht Proton Mail öffentlichen Schlüssel der Proton-Konten über HTTP von ihrem WKD. Dies ermöglicht es Personen, die Proton Mail nicht verwenden, die OpenPGP-Schlüssel von Proton Mail-Konten für anbieterübergreifende E2EE leicht zu finden. Dies gilt nur für E-Mail-Adressen, die auf eine der Proton-eigenen Domains enden, wie @proton.me. Um eine eigene Domain zu verwenden, musst du [WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separat konfigurieren.

#### :material-information-outline:{ .pg-blue } Kontokündigung

Wenn du ein kostenpflichtiges Konto hast und deine Rechnung [nach 14 Tagen noch nicht bezahlt ist](https://proton.me/de/support/delinquency), kannst du nicht mehr auf Ihre Daten zugreifen. Nach 30 Tagen wird dein Konto als säumig markiert und kann keine E-Mails mehr empfangen. Während dieses Zeitraums werden dir die Kosten weiterhin in Rechnung gestellt.

#### :material-information-outline:{ .pg-blue } Zusätzliche Funktionen

Proton Mail bietet einen "Unlimited"-Tarif für 9,99 €/Monat an, der neben der Möglichkeit mehrerer Konten, zusätzlicher Domains und Aliasse sowie 500 GB Speicherplatz auch den Zugang zu Proton VPN ermöglicht.

Proton Mail bietet keine Funktion für deinen digitalen Nachlass.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org-Logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** ist ein E-Mail-Dienst, mit dem Ziel sicher und werbefrei zu sein und der mit 100 % erneuerbaren Energien betrieben wird. Er wird seit 2014 betrieben. Mailbox.org hat seinen Sitz in Berlin, Deutschland. Konten im günstigsten Tarif beginnen mit 2 GB Speicherplatz, der je nach Bedarf erweitert werden kann.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/de/datenschutz){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://kb.mailbox.org/de/privat){ .card-link title=Dokumentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Eigene Domains und Aliase

Bei Mailbox.org kannst du deine eigene Domain verwenden, und es werden [Catch-All-Adressen](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) unterstützt. Mailbox.org unterstützt auch [Subadressen](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), was nützlich ist, wenn du keine eigene Domain kaufen möchtest.

#### :material-check:{ .pg-green } Diskrete Zahlungsmöglichkeiten

Mailbox.org akzeptiert keine Kryptowährungen, da deren Zahlungsanbieter BitPay seinen Betrieb in Deutschland eingestellt hat. Sie akzeptieren jedoch Bargeld per Post, Barzahlung auf ein Bankkonto, Banküberweisung, Kreditkarte, PayPal und einige Deutschland spezifische Anbieter: paydirekt und Sofortüberweisung.

#### :material-check:{ .pg-green } Kontosicherheit

Mailbox.org unterstützt die [Zwei-Faktor-Authentisierung](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) nur für Webmail. Du kannst entweder TOTP oder einen [YubiKey](https://en.wikipedia.org/wiki/YubiKey) über die [YubiCloud](https://yubico.com/products/services-software/yubicloud) verwenden. Webstandards wie [WebAuthn](https://de.wikipedia.org/wiki/WebAuthn) werden noch nicht unterstützt.

#### :material-information-outline:{ .pg-blue } Datensicherheit

Mailbox.org ermöglicht die Verschlüsselung von eingehenden E-Mails mit der [verschlüsselten Mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Neue eingehende Nachrichten werden dann sofort mit deinem öffentlichen Schlüssel verschlüsselt.

[Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), die von Mailbox.org genutzte Software-Plattform, [unterstützt jedoch nicht](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) die Verschlüsselung deines Adressbuchs und Kalenders. Eine [eigenständige Lösung](calendar.md) könnte für diese Informationen besser geeignet sein.

#### :material-check:{ .pg-green } E-Mail-Verschlüsselung

Mailbox.org has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox.org's servers. Diese Funktion ist nützlich, wenn der Empfänger OpenPGP nicht nutzt und daher eine Kopie der E-Mail in seinem eigenen Postfach nicht entschlüsseln kann.

Mailbox.org unterstützt auch die Suche nach öffentlichen Schlüsseln über HTTP von ihrem [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Dies ermöglicht es Personen, die Mailbox.org nicht verwenden, die OpenPGP-Schlüssel von Mailbox.org-Konten für anbieterübergreifende E2EE leicht zu finden. This only applies to email addresses ending in one of Mailbox.org's own domains, like @mailbox.org. Um eine eigene Domain zu verwenden, musst du [WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separat konfigurieren.

#### :material-information-outline:{ .pg-blue } Kontokündigung

Ihr Konto wird bei Vertragsende auf ein eingeschränktes Benutzerkonto umgestellt, nach [30 Tagen wird es unwiderruflich gelöscht](https://kb.mailbox.org/de/privat/ihr-account-bei-mailbox-org/mailbox-org-bezahlen#mailbox.orgbezahlen-MeineVertragslaufzeitistabgelaufen-wasjetzt?).

#### :material-information-outline:{ .pg-blue } Zusätzliche Funktionen

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). Auf die Webmail-Schnittstelle kann jedoch nicht über den .onion-Dienst zugegriffen werden und es können TLS-Zertifikatsfehler auftreten.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox.org unterstützt neben den Standardzugriffsprotokollen wie IMAP und POP3 auch [Exchange ActiveSync](https://de.wikipedia.org/wiki/Exchange_ActiveSync).

Mailbox.org bietet für alle Tarife eine digitale Hinterlassenschaft an. Du kannst wählen, ob deine Daten an die Erben weitergegeben werden sollen, sofern diese einen Antrag stellen und dein Testament vorlegen. Alternativ kannst du auch eine Person mit Namen und Adresse benennen.

## Weitere Anbieter

Diese Anbieter speichern deine E-Mails mit Zero-Knowledge-Verschlüsselung und sind damit eine gute Option für die Sicherheit deiner gespeicherten E-Mails. Allerdings unterstützen sie keine Interoperablen Verschlüsselungsstandards für Ende zu Ende Verschlüsselung zwischen verschiedenen Anbietern.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg){ .twemoji } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg){ align=right }

**Tuta** is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since **2011** and is based in Hanover, Germany. Konten im kostenlosen Tarif beginnen mit 1 GB Speicherplatz.

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

#### :material-check:{ .pg-green } Eigene Domains und Aliase

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/faq#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/faq#plus), but you can use a [catch-all](https://tuta.com/howto#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } Private Zahlungsmöglichkeiten

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/faq/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green } Kontosicherheit

Tuta supports [two factor authentication](https://tuta.com/faq#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Datensicherheit

Tuta has [zero access encryption at rest](https://tuta.com/faq#what-encrypted) for your emails, [address book contacts](https://tuta.com/faq#encrypted-address-book), and [calendars](https://tuta.com/faq#calendar). Das bedeutet, dass die in Ihrem Konto gespeicherten Nachrichten und anderen Daten nur von dir gelesen werden können.

#### :material-information-outline:{ .pg-blue } E-Mail-Verschlüsselung

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Kontokündigung

Tuta will [delete inactive free accounts](https://tuta.com/faq#inactive-accounts) after six months. Du kannst ein deaktiviertes kostenloses Konto wieder verwenden, wenn du bezahlst.

#### :material-information-outline:{ .pg-blue } Zusätzliche Funktionen

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/posts/secure-email-for-non-profit) for free or with a heavy discount.

Tuta hat auch eine Geschäftskundenfunktion namens [Secure Connect](https://tuta.com/de/business). Dadurch wird sichergestellt, dass der Kundenkontakt zum Unternehmen über E2EE erfolgt. Das Feature kostet 240 €/Jahr.

Tuta bietet keine Funktion für deinen digitalen Nachlass.

## E-Mail-Aliasing-Dienste

Mit einem E-Mail-Aliasing-Dienst können Sie für jede Website, für die Sie sich anmelden, ganz einfach eine neue E-Mail-Adresse generieren. Die von dir erstellten E-Mail-Aliase werden dann an eine E-Mail-Adresse deiner Wahl weitergeleitet, wobei sowohl deine "Haupt"-E-Mail-Adresse als auch die Identität deines E-Mail-Anbieters verborgen bleiben. Echtes E-Mail-Aliasing ist besser als die von vielen Providern verwendete und unterstützte Plus-Adressierung, mit der du Aliase wie DeinName+[irgendetwas]@example.com erstellen kannst, da Websites, Werbetreibende und Tracking-Netzwerke einfach alles nach dem +-Zeichen entfernen können, um deine wahre E-Mail-Adresse zu erfahren.

<div class="grid cards" markdown>

- ![addy.io logo](assets/img/email/mini/addy.svg){ .twemoji } [addy.io](email.md#addyio)
- ![SimpleLogin logo](assets/img/email/simplelogin.svg){ .twemoji } [SimpleLogin](email.md#simplelogin)

</div>

Das E-Mail-Aliasing kann als Schutz dienen, falls dein E-Mail-Anbieter einmal seinen Betrieb einstellt. In diesem Fall kannst du deine Aliase einfach an eine neue E-Mail-Adresse weiterleiten. Im Gegenzug vertraust du jedoch darauf, dass der Aliasing-Dienst weiterhin funktioniert.

Die Verwendung eines speziellen E-Mail-Aliasdienstes hat auch eine Reihe von Vorteilen gegenüber einem Catch-All-Alias auf einer benutzerdefinierten Domäne:

- Aliasnamen können bei Bedarf individuell ein- und ausgeschaltet werden, um zu verhindern, dass Websites wahllos E-Mails an dich senden.
- Die Antworten werden von der Alias-Adresse gesendet, sodass deine echte E-Mail-Adresse verborgen bleibt.

Sie haben auch eine Reihe von Vorteilen gegenüber "temporären E-Mail-Diensten":

- Aliase sind dauerhaft und können wieder aktiviert werden, wenn du z. B. ein neues Kennwort erhalten musst.
- E-Mails werden an dein vertrauenswürdiges Postfach gesendet und nicht beim Alias-Anbieter gespeichert.
- Temporäre E-Mail-Dienste haben in der Regel öffentliche Postfächer, auf die jeder zugreifen kann, der die Adresse kennt, während Aliase privat sind.

Unsere E-Mail-Aliasing-Empfehlungen beziehen sich auf Anbieter, die es Ihnen ermöglichen, gegen eine geringe Jahresgebühr Aliase für die von dir kontrollierten Domains sowie für deine eigene(n) benutzerdefinierte(n) Domain(s) zu erstellen. Sie können auch selbst gehostet werden, wenn du dir maximale Kontrolle wünscht. Die Verwendung einer benutzerdefinierten Domäne kann jedoch datenschutzbezogene Nachteile haben: Wenn du die einzige Person bist, die deine benutzerdefinierte Domäne verwendet, können deine Aktionen auf verschiedenen Websites leicht nachverfolgt werden, indem einfach der Domänenname in der E-Mail-Adresse betrachtet und alles vor dem @-Zeichen ignoriert wird.

Die Verwendung eines Alias-Dienstes setzt voraus, dass du sowohl deinem E-Mail-Anbieter als auch deinem Alias-Anbieter deine unverschlüsselten Nachrichten anvertraust. Einige Anbieter entschärfen dieses Problem durch die automatische PGP-Verschlüsselung, bei der die Anzahl der Parteien, denen du vertrauen musst, von zwei auf eine reduziert wird, indem eingehende E-Mails verschlüsselt werden, bevor sie an deinen endgültigen Mailbox-Anbieter übermittelt werden.

### addy.io

<div class="admonition recommendation" markdown>

![addy.io logo](assets/img/email/addy.svg#only-light){ align=right }
![addy.io logo](assets/img/email/addy-dark.svg#only-dark){ align=right }

Mit **addy.io** können sie gratis 10 verschiedene Aliase auf einem geteilten Domainnamen erstellen, oder unendlich viele "standard" Aliase, welche weniger anonym sind.

[:octicons-home-16: Homepage](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://app.addy.io/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://addy.io/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: Android](https://addy.io/faq/#is-there-an-android-app)
- [:material-apple-ios: iOS](https://addy.io/faq/#is-there-an-ios-app)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/addy_io)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/addyio-anonymous-email-fo/iadbdpnoknmbdeolbapdackdcogdmjpe)

</details>

</div>

Mit dem gratis-Plan ist die Anzahl der geteilten Aliase (welche in einer geteilten Domäne, wie z.B. @addy.io, enden) auf 10 beschränkt. Für 1$ im Monat erhalten sie 50, und für 4$ im Monat unendlich viele (3$ pro Monat wenn sie jährlich zahlen). Sie können unendlich viele standard Aliase (welche in einer Domäne wie @[Nutzername].addy.io oder einer benutzerdefinierten Domäne mit Abo enden) erstellen, allerdings sind diese, wie schon gesagt, weniger anonym, da schon allein über den Domainnamen alle Aliase miteinander auf eine Person zurückgeführt werden können. Standard Aliase sind sinnvoll, wenn geteilte Domänen von einer Website geblockt werden. Securitum [audited](https://addy.io/blog/addy-io-passes-independent-security-audit) addy.io in September 2023 and no significant vulnerabilities [were identified](https://addy.io/addy-io-security-audit.pdf).

Bemerkenswerte kostenlose Funktionen:

- [x] 10 Gemeinsame Aliasnamen
- [x] Unbegrenzte Standard-Aliasnamen
- [ ] Keine ausgehenden Antworten
- [x] Eine Mailbox zum Empfang
- [x] Automatische PGP-Verschlüsselung

### SimpleLogin

<div class="admonition recommendation" markdown>

![Simplelogin-Logo](assets/img/email/simplelogin.svg){ align=right }

**SimpleLogin** ist ein kostenloser Dienst, der E-Mail-Aliase für eine Vielzahl von gemeinsam genutzten Domänennamen bereitstellt und optional kostenpflichtige Funktionen wie unbegrenzte Aliase und benutzerdefinierte Domänen bietet.

[:octicons-home-16: Homepage](https://simplelogin.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplelogin.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://simplelogin.io/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simple-login){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
- [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/simplelogin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
- [:simple-safari: Safari](https://apps.apple.com/app/id6475835429)

</details>

</div>

SimpleLogin wurde zum 8. April 2022 [von der Proton AG übernommen](https://proton.me/news/proton-and-simplelogin-join-forces). Wenn du Proton Mail für dein Hauptpostfach verwendest, ist SimpleLogin eine gute Wahl. Da beide Produkte nun demselben Unternehmen gehören, musst du nur noch einem einzigen Unternehmen vertrauen. Wir gehen außerdem davon aus, dass SimpleLogin in Zukunft enger mit den Angeboten von Proton integriert werden wird. SimpleLogin unterstützt weiterhin die Weiterleitung an einen E-Mail-Anbieter deiner Wahl. Securitum [audited](https://simplelogin.io/blog/security-audit) SimpleLogin in early 2022 and all issues [were addressed](https://simplelogin.io/audit2022/web.pdf).

Du kannst dein SimpleLogin-Konto in den Einstellungen mit deinem Proton-Konto verknüpfen. Wenn du den Proton Unlimited, Business oder Visionary Tarif nutzt, erhältst du zusätzlich SimpleLogin Premium kostenlos dazu.

Bemerkenswerte kostenlose Funktionen:

- [x] 10 Gemeinsame Aliasnamen
- [x] Unbegrenzte Antworten
- [x] 1 Empfänger-Mailbox

## E-Mail Selbst Hosten

Fortgeschrittene Systemadministratoren können die Einrichtung eines eigenen E-Mail-Servers in Erwägung ziehen. Mailserver erfordern Aufmerksamkeit und ständige Wartung, um die Sicherheit und die Zuverlässigkeit der Mailzustellung zu gewährleisten.

### Kombinierte Software-Lösungen

<div class="admonition recommendation" markdown>

![Mailcow-Logo](assets/img/email/mailcow.svg){ align=right }

**Mailcow** ist ein fortgeschrittener Mailserver, perfekt für diejenigen mit ein wenig mehr Linux-Erfahrung. Es vereinigt alles was du brauchst in einem Docker-Container: Einen Mailserver mit DKIM-Unterstützung, Virenschutz und Spam-Überwachung, Webmail und ActiveSync mit SOGo, sowie eine webbasierte Verwaltung mit 2FA-Unterstützung.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

</div>

<div class="admonition recommendation" markdown>

![Mail-in-a-Box-Logo](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** ist ein automatisches Setup-Skript für die Einrichtung eines Mailservers unter Ubuntu. Sein Ziel ist es, die Einrichtung eines eigenen Mailservers zu erleichtern.

[:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Dokumentation}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title=Quelltext }

</div>

Für einen eher manuellen Ansatz haben wir diese beiden Artikel herausgesucht:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://c0ffee.net/blog/mail-server-guide) (August 2017)

## Kriterien

**Bitte beachte, dass wir mit keinem der von uns empfohlenen Anbieter verbunden sind.** Zusätzlich zu [unseren Standardkriterien](about/criteria.md)haben wir eine Reihe klarer Anforderungen für jeden E-Mail-Anbieter entwickelt, der empfohlen werden möchte, darunter die Umsetzung branchenweit bewährter Verfahren, moderne Technologien und weiteres. Wir empfehlen, sich mit dieser Liste vertraut zu machen, bevor sich für einen E-Mail-Anbieter entscheiden wird, und eigene Nachforschungen anzustellen, um sicherzustellen, dass der gewählte E-Mail-Anbieter die richtige Wahl für dich ist.

### Technologien

Wir halten diese Merkmale für wichtig, um einen sicheren und optimalen Service zu bieten. Du solltest prüfen, ob der Anbieter über die von dir gewünschten Funktionen verfügt.

**Mindestvoraussetzung um sich zu qualifizieren:**

- Verschlüsselt die Daten von E-Mail-Konten im Ruhezustand mit Zero-Access-Verschlüsselung.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Erlaubt es dem Nutzer, seinen eigenen [Domainnamen](https://de.wikipedia.org/wiki/Domain_(Internet)) zu verwenden. Benutzerdefinierte Domänennamen sind für die Nutzer wichtig, da du so deine Identität von dem Dienst fernhalten kannst, falls dieser sich als schlecht erweist oder von einem anderen Unternehmen übernommen wird, bei dem der Datenschutz keine Rolle spielt.
- Arbeitet auf einer eigenen Infrastruktur, d.h. nicht auf der eines Drittanbieters von E-Mail-Diensten.

**Im besten Fall:**

- Verschlüsselt alle Kontodaten (Kontakte, Kalender usw.) im Ruhezustand mit Zero-Access-Verschlüsselung.
- Integrierte Webmail E2EE/PGP-Verschlüsselung als Komfortfunktion.
- Unterstützung für [WKD](https://wiki.gnupg.org/WKD), um die Suche nach öffentlichen OpenPGP-Schlüsseln über HTTP zu verbessern. GnuPG-Benutzer können einen Schlüssel erhalten, indem sie Folgendes eingeben: `gpg --locate-key beispiel_nutzer@example.com`
- Unterstützung für eine temporäre Mailbox für externe Benutzer. Dies ist nützlich, wenn du eine verschlüsselte E-Mail versenden möchtest, ohne eine Kopie an den Empfänger zu senden. Diese E-Mails haben in der Regel eine begrenzte Lebensdauer und werden dann automatisch gelöscht. Sie erfordern auch nicht, dass der Empfänger eine Kryptographie wie OpenPGP konfiguriert.
- Verfügbarkeit der Dienste des E-Mail-Anbieters über einen [onion service](https://de.wikipedia.org/wiki/.onion).
- [Sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing) support.
- Catch-All- oder Alias-Funktionalität für diejenigen, die ihre eigenen Domains besitzen.
- Verwendung von Standard-E-Mail-Zugangsprotokollen wie IMAP, SMTP oder [JMAP](https://de.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standardzugriffsprotokolle stellen sicher, dass die Kunden alle ihre E-Mails problemlos herunterladen können, sollten sie zu einem anderen Anbieter wechseln wollen.

### Datenschutz

Wir ziehen es vor, dass die von uns empfohlenen Anbieter so wenig Daten wie möglich sammeln.

**Mindestvoraussetzung um sich zu qualifizieren:**

- IP-Adresse des Absenders schützen. Der `Received`-Header wird aus der E-Mail entfernt.
- Benötigt keine personenbezogenen Daten (PII) außer eines Benutzernamens und eines Passwortes.
- Datenschutzrichtlinien, die den Anforderungen der DSGVO entsprechen.

**Im Besten Fall:**

- Akzeptiert [anonyme Zahlungsmöglichkeiten](advanced/payments.md) ([Kryptowährungen](cryptocurrency.md), Bargeld, Geschenkkarten, etc.)
- Gehostet in einem Land mit strengen Gesetzen zum Schutz des E-Mail-Verkehrs.

### Sicherheit

Auf E-Mail-Servern werden viele sehr sensible Daten verarbeitet. Wir erwarten, dass die Anbieter die besten Praktiken der Branche übernehmen, um ihre Nutzer zu schützen.

**Mindestvoraussetzung um sich zu qualifizieren:**

- Schutz von Webmail mit 2FA, wie TOTP.
- Zero-Access-Verschlüsselung, baut auf Verschlüsselung im Ruhezustand auf. Der Anbieter verfügt nicht über die Entschlüsselungsschlüssel zu den Daten, die er besitzt. So wird verhindert, dass ein abtrünniger Mitarbeitender Daten preisgibt, auf die er/sie Zugriff hat, oder dass ein Angreifender Daten freigibt, die er/sie gestohlen hat, indem er/sie sich unbefugt Zugang zum Server verschafft.
- [DNSSEC](https://de.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) Unterstützung.
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Eine Server-Suite-Präferenz (optional bei TLSv1.3) für starke Cipher-Suites, die Forward Secrecy und authentifizierte Verschlüsselung unterstützen.
- Eine gültige [MTA-STS](https://tools.ietf.org/html/rfc8461) und [TLS-RPT](https://tools.ietf.org/html/rfc8460) Richtlinie.
- Gültige [DANE](https://de.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) Datensätze.
- Gültige [SPF](https://de.wikipedia.org/wiki/Sender_Policy_Framework) und [DKIM](https://de.wikipedia.org/wiki/DomainKeys_Identified_Mail) Einträge.
- Besitzen eines ordnungsgemäßen [DMARC](https://de.wikipedia.org/wiki/DMARC) Datensatzes und einer Richtlinie oder verwenden von [ARC](https://de.wikipedia.org/wiki/Authenticated_Received_Chain) für die Authentifizierung. Wenn die DMARC-Authentifizierung verwendet wird, muss die Richtlinie auf `reject` oder `quarantine` eingestellt sein.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [SMTPS](https://de.wikipedia.org/wiki/SMTPS) Übermittlung, vorausgesetzt, SMTP wird verwendet.
- Website-Sicherheitsstandards wie z. B.:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subresource Integrity](https://en.wikipedia.org/wiki/Subresource_Integrity) wenn Dinge von externen Domains geladen werden.
- Muss die Anzeige von [Message Headers](https://de.wikipedia.org/wiki/Header_(E-Mail)) unterstützen, da dies eine wichtige forensische Funktion ist, um festzustellen, ob eine E-Mail ein Phishing-Versuch ist.

**Im Besten Fall:**

- Unterstützung für Hardware-Authentifizierung, d.h. U2F und [WebAuthn](https://de.wikipedia.org/wiki/WebAuthn). U2F und WebAuthn sind sicherer, da sie zur Authentifizierung von Personen einen privaten Schlüssel verwenden, der auf einem clientseitigen Hardware-Gerät gespeichert ist, im Gegensatz zu einem gemeinsam genutzten Geheimnis, das bei der Verwendung von TOTP auf dem Webserver und auf der Clientseite gespeichert ist. Darüber hinaus sind U2F und WebAuthn resistenter gegen Phishing, da ihre Authentifizierungsantwort auf dem authentifizierten [Domainnamen](https://de.wikipedia.org/wiki/Domain_(Internet)) basiert.
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) zusätzlich zur DANE-Unterstützung.
- Implementierung von [Authenticated Received Chain (ARC)](https://de.wikipedia.org/wiki/Authenticated_Received_Chain), dies ist nützlich für Leute, die auf Mailinglisten posten [RFC8617](https://tools.ietf.org/html/rfc8617).
- Bug-Bounty-Programme und/oder ein koordiniertes Verfahren zur Offenlegung von Sicherheitslücken.
- Website-Sicherheitsstandards wie z. B.:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Vertrauen

Du würdest jemandem mit einer gefälschten Identität nicht deine Finanzen anvertrauen, warum solltest du ihm also deine E-Mails anvertrauen? Wir verlangen von den von uns empfohlenen Anbietern, dass sie ihre Eigentumsverhältnisse oder ihre Führungsrolle öffentlich machen. Außerdem wünschen wir uns häufige Transparenzberichte, insbesondere über die Bearbeitung von Regierungsanfragen.

**Mindestvoraussetzung um sich zu qualifizieren:**

- Öffentliche Führung oder Eigentum.

**Im Besten Fall:**

- Führung mit Öffentlichkeitsbezug.
- Häufige Transparenzberichte.

### Marketing

Bei den von uns empfohlenen E-Mail-Anbietern legen wir Wert auf ein verantwortungsvolles Marketing.

**Mindestvoraussetzung um sich zu qualifizieren:**

- Sie müssen Ihre Analyse-Werkzeuge selbst hosten (kein Google Analytics, Adobe Analytics, etc.). Die Website des Anbieters muss auch die Anforderungen von [DNT (Do Not Track)](https://de.wikipedia.org/wiki/Do_Not_Track_(Software)) für diejenigen erfüllen, die sich dagegen entscheiden möchten.

Es darf kein Marketing geben, das unverantwortlich ist:

- Behauptung einer "unknackbaren Verschlüsselung". Die Verschlüsselung sollte in der Voraussicht eingesetzt werden, dass sie in Zukunft möglicherweise nicht mehr geheim ist, wenn die Technologie vorhanden ist, um sie zu knacken.
- Gewährleistung eines 100%igen Schutzes der Anonymität. Wenn jemand behauptet, etwas sei zu 100% sicher, bedeutet das, dass es keine Sicherheit für ein Scheitern gibt. Wir wissen, dass Menschen sich auf verschiedene Weise recht einfach deanonymisieren können, z. B.:

    - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
    - [Browser-Fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Im besten Fall:**

- Klare und leicht zu lesende Dokumentation. Dazu gehören Dinge wie die Einrichtung von 2FA, E-Mail-Clients, OpenPGP, usw.

### Zusätzliche Funktionalitäten

Obwohl es sich nicht um strenge Anforderungen handelt, haben wir bei der Auswahl der zu empfehlenden Anbieter auch andere Faktoren wie Komfort oder Datenschutz berücksichtigt.
