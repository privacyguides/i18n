---
meta_title: "Empfehlungen für verschlüsselte private E-Mail-Dienste - Privacy Guides"
title: "E-Mail Dienste"
icon: material/email
description: Diese E-Mail-Dienstleister speichern deine E-Mails sicher und viele davon bieten auch interoperable OpenPGP-Verschlüsselung mit anderen Anbietern.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protects against the following threat(s):</small>

- [:material-server-network: Diensteanbieter](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

E-Mail ist praktisch eine Voraussetzung für die Nutzung aller Online-Dienste, wir empfehlen sie jedoch nicht zur Kommunikation von Mensch zu Mensch. Anstatt E-Mails für die Kontaktaufnahme mit anderen Personen zu verwenden, überleg ob du einen Instant Messenger benutzen kannst, der Forward Secrecy (auf Deutsch etwa "vorwärts gerichtete Geheimhaltung") unterstützt.

[Empfohlene Instant Messenger](real-time-communication.md ""){.md-button}

## Empfohlene Anbieter

Für alles andere empfehlen wir eine Reihe von E-Mail-Anbietern, die auf nachhaltigen Geschäftsmodellen basieren und integrierte Sicherheits- und Datenschutzfunktionen bieten. Weitere Informationen findest du in unserem [vollständigen Kriterienkatalog](#criteria).

| Anbieter                    | OpenPGP / WKD                          | IMAP / SMTP                                                           | Null-Zugriff-Verschlüsselung                        | Anonyme Zahlungen                   |
| --------------------------- | -------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------- | ----------------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Nur kostenpflichtige Pläne | :material-check:{ .pg-green }                       | Bargeld                             |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                                         | :material-information-outline:{ .pg-blue } Nur Mail | Bargeld                             |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                                | :material-check:{ .pg-green }                       | Monero & Bargeld über Drittanbieter |

Zusätzlich zu (oder anstelle von) einem hier empfohlenen E-Mail-Anbieter kannst du einen speziellen [E-Mail-Aliasing-Dienst](email-aliasing.md) in Betracht ziehen, um deine Privatsphäre zu schützen. Diese Dienste können unter anderem dazu beitragen, deinen echten Posteingang vor Spam zu schützen, zu verhindern, dass Vermarkter deine Konten miteinander in Verbindung bringen, und alle eingehenden Nachrichten mit PGP zu verschlüsseln.

- [Weitere Informationen :material-arrow-right-drop-circle:](email-aliasing.md)

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

**Proton Mail** ist ein E-Mail-Dienst mit dem Schwerpunkt auf Datenschutz, Verschlüsselung, Sicherheit und Benutzerfreundlichkeit. Sie sind seit 2013 in Betrieb. Die Proton AG hat ihren Sitz in Genf, Schweiz. Der Proton Mail Free Tarif beinhaltet 500 MB Mailspeicher, den du kostenlos auf bis zu 1 GB erweitern kannst.

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

Kostenlose Konten haben einige Einschränkungen, wie z. B. die fehlende Möglichkeit Text zu durchsuchen und keinen Zugang zu [Proton Mail Bridge](https://proton.me/mail/bridge). Diese ist für die Verwendung eines [empfohlenen Desktop-E-Mail-Programms](email-clients.md) (z. B. Thunderbird) erforderlich. Bezahlte Konten umfassen Funktionen wie Proton Mail Bridge, zusätzlichen Speicher und die Nutzung eigener Domains. Am 9. November 2021 wurden durch [Securitum](https://research.securitum.com) ein Sicherheitsaudit durchgeführt und  die Anwendungen von Proton Mail [zertifiziert](https://proton.me/blog/security-audit-all-proton-apps).

If you have the Proton Unlimited plan or any multi-user Proton plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

Proton Mail hat interne Absturzberichte, die sie **nicht** mit Dritten teilen. Dies kann in der Web-App deaktiviert werden: :gear: → **Alle Einstellungen** → **Konto** → **Sicherheit und Datenschutz** → **Privatsphäre und Datenerfassung**.

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

Wenn du ein kostenpflichtiges Konto hast und deine Rechnung [nach 14 Tagen noch nicht bezahlt ist](https://proton.me/de/support/delinquency), kannst du nicht mehr auf Ihre Daten zugreifen. Nach 30 Tagen wird dein Konto als säumig markiert und kann keine E-Mails mehr empfangen. Während dieses Zeitraums werden dir die Kosten weiterhin in Rechnung gestellt. Proton [löscht inaktive kostenlose Konten](https://proton.me/support/inactive-accounts) nach einem Jahr. Du kannst die E-Mail-Adresse eines deaktivierten Kontos **nicht** wiederverwenden.

#### :material-information-outline:{ .pg-blue } Zusätzliche Funktionen

Der [Unlimited-Tarif](https://proton.me/support/proton-plans#proton-unlimited) von Proton Mail ermöglicht auch den Zugang zu anderen Proton-Diensten und bietet darüber hinaus mehrere benutzerdefinierte Domains, eine unbegrenzte Anzahl von "Hide-my-email"-Aliasnamen und 500 GB Speicherplatz.

Proton Mail bietet keine Funktion für deinen digitalen Nachlass.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org-Logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** ist ein E-Mail-Dienst, mit dem Ziel sicher und werbefrei zu sein und der mit 100 % Ökostrom betrieben wird. Er wird seit 2014 betrieben. Mailbox.org hat seinen Sitz in Berlin, Deutschland. Konten beginnen mit 2 GB Speicherplatz, der nach Bedarf erweitert werden kann.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Eigene Domains und Aliase

Bei Mailbox.org kannst du deine eigene Domain verwenden, und es werden [Catch-All-Adressen](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) unterstützt. Mailbox.org unterstützt auch [Subadressen](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), was nützlich ist, wenn du keine eigene Domain kaufen möchtest.

#### :material-check:{ .pg-green } Diskrete Zahlungsmöglichkeiten

Mailbox.org akzeptiert keine Kryptowährungen, da deren Zahlungsanbieter BitPay seinen Betrieb in Deutschland eingestellt hat. Sie akzeptieren jedoch Bargeld per Post, Bareinzahlung auf ein Bankkonto, Banküberweisung, Kreditkarte, PayPal und einige Deutschland spezifische Anbieter: paydirekt und Sofortüberweisung.

#### :material-check:{ .pg-green } Kontosicherheit

Mailbox.org unterstützt die [Zwei-Faktor-Authentisierung](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) nur für Webmail. Du kannst entweder TOTP oder einen [YubiKey](https://en.wikipedia.org/wiki/YubiKey) über die [YubiCloud](https://yubico.com/products/services-software/yubicloud) verwenden. Webstandards wie [WebAuthn](https://de.wikipedia.org/wiki/WebAuthn) werden noch nicht unterstützt.

#### :material-information-outline:{ .pg-blue } Datensicherheit

Mailbox.org ermöglicht die Verschlüsselung von eingehenden E-Mails mit der [verschlüsselten Mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Neue eingehende Nachrichten werden dann sofort mit deinem öffentlichen Schlüssel verschlüsselt.

[Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), die von Mailbox.org genutzte Software-Plattform, [unterstützt jedoch nicht](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) die Verschlüsselung deines Adressbuchs und Kalenders. Eine [eigenständige Lösung](calendar.md) könnte für diese Informationen besser geeignet sein.

#### :material-check:{ .pg-green } E-Mail-Verschlüsselung

Mailbox.org hat die [Verschlüsselung](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in sein Webmail [integriert](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard), was den Versand von Nachrichten an Personen mit öffentlichen OpenPGP-Schlüsseln vereinfacht. Sie erlauben es auch entfernten Empfängern [eine E-Mail](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) auf den Servern von Mailbox.org zu entschlüsseln. Diese Funktion ist nützlich, wenn der Empfänger OpenPGP nicht nutzt und daher eine Kopie der E-Mail in seinem eigenen Postfach nicht entschlüsseln kann.

Mailbox.org unterstützt auch die Suche nach öffentlichen Schlüsseln über HTTP von ihrem [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Dies ermöglicht es Personen, die Mailbox.org nicht verwenden, die OpenPGP-Schlüssel von Mailbox.org-Konten für anbieterübergreifende E2EE leicht zu finden. Dies gilt nur für E-Mail-Adressen, die auf eine der Mailbox.org-eigenen Domains enden, wie @mailbox.org. Um eine eigene Domain zu verwenden, musst du [WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separat konfigurieren.

#### :material-information-outline:{ .pg-blue } Kontokündigung

Nach Ablauf deines Vertrags wird dein Konto zunächst auf ein eingeschränktes Benutzerkonto umgestellt. Dieses wird nach [30 Tagen](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract) unwiderruflich gelöscht.

#### :material-information-outline:{ .pg-blue } Zusätzliche Funktionen

Du kannst auf Ihr Mailbox.org-Konto über IMAP/SMTP zugreifen, indem du deren [.onion-Dienst](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org) nutzt. Auf die Webmail-Schnittstelle kann jedoch nicht über den .onion-Dienst zugegriffen werden und es können TLS-Zertifikatsfehler auftreten.

Alle Konten verfügen über einen begrenzten Cloud-Speicher, der [verschlüsselt werden kann](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org bietet auch den Alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely) an, der die TLS-Verschlüsselung der Verbindung zwischen den Mailservern erzwingt, ansonsten wird die Nachricht erst gar nicht gesendet. Mailbox.org unterstützt neben den Standardzugriffsprotokollen wie IMAP und POP3 auch [Exchange ActiveSync](https://de.wikipedia.org/wiki/Exchange_ActiveSync).

Mailbox.org bietet für alle Tarife eine digitale Hinterlassenschaft an. Du kannst wählen, ob deine Daten an die Erben weitergegeben werden sollen, sofern diese einen Antrag stellen und dein Testament vorlegen. Alternativ kannst du auch eine Person mit Namen und Adresse benennen.

## Weitere Anbieter

Diese Anbieter speichern deine E-Mails mit Zero-Knowledge-Verschlüsselung und sind damit eine gute Option für die Sicherheit deiner gespeicherten E-Mails. Allerdings unterstützen sie keine Interoperablen Verschlüsselungsstandards für Ende zu Ende Verschlüsselung zwischen verschiedenen Anbietern.

<div class="grid cards" markdown>

- ![Tuta Logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (ehemals *Tutanota*) ist ein E-Mail-Dienst mit einem Fokus auf Sicherheit und Privatsphäre durch Verschlüsselung. Tuta ist seit 2011 in Betrieb und hat seinen Sitz in Hannover, Deutschland. Kostenlose Konten beginnen mit 1 GB Speicherplatz.

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

Tuta doesn't support the [IMAP protocol](https://tuta.com/support#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/kickoff-import). E-Mails können [einzeln oder per Massenauswahl](https://tuta.com/support#generalMail) pro Ordner exportiert werden, was bei vielen Ordnern unpraktisch sein kann.

#### :material-check:{ .pg-green } Eigene Domains und Aliase

Bezahlte Tuta-Konten können je nach Tarif entweder 15 oder 30 Aliase und unbegrenzte Aliase auf [benutzerdefinierten Domains](https://tuta.com/support#custom-domain) verwenden. Tuta lässt keine [Unteradressen (Plus-Adressen)](https://tuta.com/support#plus) zu, du kannst aber einen [Catch-All](https://tuta.com/support#settings-global) mit einer benutzerdefinierten Domain verwenden.

#### :material-information-outline:{ .pg-blue } Private Zahlungsmöglichkeiten

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green } Kontosicherheit

Tuta unterstützt die [Zwei-Faktor-Authentisierung](https://tuta.com/support#2fa) entweder mit TOTP oder U2F.

#### :material-check:{ .pg-green } Datensicherheit

Tuta bietet eine [Zero-Access-Verschlüsselung im Ruhezustand](https://tuta.com/support#what-encrypted) für Ihre E-Mails, [Adressbuchkontakte](https://tuta.com/support#encrypted-address-book) und [Kalender](https://tuta.com/support#calendar). Das bedeutet, dass die in deinem Konto gespeicherten Nachrichten und andere Daten nur von dir gelesen werden können.

#### :material-information-outline:{ .pg-blue } E-Mail-Verschlüsselung

Tuta [verwendet kein OpenPGP](https://tuta.com/support/#pgp). Tuta-Konten können verschlüsselte E-Mails von Nicht-Tuta-E-Mail-Konten nur empfangen, wenn sie über ein temporäres Tuta-Postfach [gesendet werden](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Kontokündigung

Tuta [löscht inaktive kostenlose Konten](https://tuta.com/support#inactive-accounts) nach sechs Monaten. Du kannst ein deaktiviertes kostenloses Konto wieder verwenden, wenn du bezahlst.

#### :material-information-outline:{ .pg-blue } Zusätzliche Funktionen

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/secure-email-for-non-profit) for free or with a heavy discount.

Tuta bietet keine Funktion für deinen digitalen Nachlass.

## E-Mail Selbst Hosten

Fortgeschrittene Systemadministratoren können die Einrichtung eines eigenen E-Mail-Servers in Erwägung ziehen. Mailserver erfordern Aufmerksamkeit und ständige Wartung, um die Sicherheit und die Zuverlässigkeit der Mailzustellung zu gewährleisten.

### Kombinierte Software-Lösungen

<div class="admonition recommendation" markdown>

![Mailcow-Logo](assets/img/email/mailcow.svg){ align=right }

**Mailcow** ist ein fortgeschrittener Mailserver, perfekt für diejenigen mit ein wenig mehr Linux-Erfahrung. It has everything you need in a Docker container: a mail server with DKIM support, antivirus and spam monitoring, webmail and ActiveSync with SOGo, and web-based administration with 2FA support.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title="Contribute" }

</div>

<div class="admonition recommendation" markdown>

![Mail-in-a-Box-Logo](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** ist ein automatisches Setup-Skript für die Einrichtung eines Mailservers unter Ubuntu. Sein Ziel ist es, die Einrichtung eines eigenen Mailservers zu erleichtern.

[:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }

</div>

Für einen eher manuellen Ansatz haben wir diese beiden Artikel herausgesucht:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://c0ffee.net/blog/mail-server-guide) (August 2017)

## Kriterien

**Bitte beachte, dass wir mit keinem der von uns empfohlenen Anbieter verbunden sind.** Zusätzlich zu [unseren Standardkriterien](about/criteria.md)haben wir eine Reihe klarer Anforderungen für jeden E-Mail-Anbieter entwickelt, der empfohlen werden möchte, darunter die Umsetzung branchenweit bewährter Verfahren, moderne Technologien und weiteres. Wir empfehlen, sich mit dieser Liste vertraut zu machen, bevor du dich für einen E-Mail-Anbieter entscheidest, und deine eigenen Nachforschungen anzustellst, um sicherzustellen, dass der gewählte E-Mail-Anbieter die richtige Wahl für dich ist.

### Technologien

Wir halten diese Merkmale für wichtig, um einen sicheren und optimalen Service zu bieten. Du solltest prüfen, ob der Anbieter über die von dir gewünschten Funktionen verfügt.

**Mindestvoraussetzung um sich zu qualifizieren:**

- Verschlüsselt die Daten von E-Mail-Konten im Ruhezustand mit Zero-Access-Verschlüsselung.
- Exportmöglichkeit als [Mbox](https://en.wikipedia.org/wiki/Mbox) oder individuelle .eml mit [RFC5322-Standard](https://datatracker.ietf.org/doc/rfc5322).
- Erlaubt es dem Nutzer, seinen eigenen [Domainnamen](https://de.wikipedia.org/wiki/Domain_(Internet)) zu verwenden. Benutzerdefinierte Domänennamen sind für die Nutzer wichtig, da du so deine Identität von dem Dienst fernhalten kannst, falls dieser sich als schlecht erweist oder von einem anderen Unternehmen übernommen wird, bei dem der Datenschutz keine Rolle spielt.
- Arbeitet auf einer eigenen Infrastruktur, d.h. nicht auf der eines Drittanbieters von E-Mail-Diensten.

**Im besten Fall:**

- Verschlüsselt alle Kontodaten (Kontakte, Kalender usw.) im Ruhezustand mit Zero-Access-Verschlüsselung.
- Integrierte Webmail E2EE/PGP-Verschlüsselung als Komfortfunktion.
- Unterstützung für [WKD](https://wiki.gnupg.org/WKD), um die Suche nach öffentlichen OpenPGP-Schlüsseln über HTTP zu verbessern. GnuPG-Benutzer können einen Schlüssel erhalten, indem sie Folgendes eingeben: `gpg --locate-key beispiel_nutzer@example.com`
- Unterstützung für eine temporäre Mailbox für externe Benutzer. Dies ist nützlich, wenn du eine verschlüsselte E-Mail versenden möchtest, ohne eine Kopie an den Empfänger zu senden. Diese E-Mails haben in der Regel eine begrenzte Lebensdauer und werden dann automatisch gelöscht. Sie erfordern auch nicht, dass der Empfänger eine Kryptographie wie OpenPGP konfiguriert.
- Verfügbarkeit der Dienste des E-Mail-Anbieters über einen [onion service](https://de.wikipedia.org/wiki/.onion).
- Unterstützung [von Unteradressen](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Catch-all or alias functionality for those who use their own domains.
- Use of standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standardzugriffsprotokolle stellen sicher, dass die Kunden alle ihre E-Mails problemlos herunterladen können, sollten sie zu einem anderen Anbieter wechseln wollen.

### Datenschutz

Wir ziehen es vor, dass die von uns empfohlenen Anbieter so wenig Daten wie möglich sammeln.

**Mindestvoraussetzung um sich zu qualifizieren:**

- Protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Benötigt keine personenbezogenen Daten (PII) außer eines Benutzernamens und eines Passwortes.
- Datenschutzrichtlinien, die den Anforderungen der DSGVO entsprechen.

**Im besten Fall:**

- Akzeptiert [anonyme Zahlungsmöglichkeiten](advanced/payments.md) ([Kryptowährungen](cryptocurrency.md), Bargeld, Geschenkkarten, etc.)
- Gehostet in einem Land mit strengen Gesetzen zum Schutz des E-Mail-Verkehrs.

### Sicherheit

Auf E-Mail-Servern werden viele sehr sensible Daten verarbeitet. We expect that providers will adopt best industry practices in order to protect their customers.

**Mindestvoraussetzung um sich zu qualifizieren:**

- Schutz von Webmail mit 2FA, wie TOTP.
- Zero access encryption, which builds on encryption at rest. Der Anbieter verfügt nicht über die Entschlüsselungsschlüssel zu den Daten, die er besitzt. So wird verhindert, dass ein abtrünniger Mitarbeitender Daten preisgibt, auf die er/sie Zugriff hat, oder dass ein Angreifender Daten freigibt, die er/sie gestohlen hat, indem er/sie sich unbefugt Zugang zum Server verschafft.
- [DNSSEC](https://de.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) Unterstützung.
- Keine TLS-Fehler oder -Schwachstellen beim Profiling durch Tools wie [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh)oder [Qualys SSL Labs](https://ssllabs.com/ssltest); dies schließt zertifikatsbezogene Fehler und schwache DH-Parameter ein, wie z. B. die, die zu [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)) führten.
- Eine Server-Suite-Präferenz (optional bei TLSv1.3) für starke Cipher-Suites, die Forward Secrecy und authentifizierte Verschlüsselung unterstützen.
- Eine gültige [MTA-STS](https://tools.ietf.org/html/rfc8461) und [TLS-RPT](https://tools.ietf.org/html/rfc8460) Richtlinie.
- Gültige [DANE](https://de.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) Datensätze.
- Gültige [SPF](https://de.wikipedia.org/wiki/Sender_Policy_Framework) und [DKIM](https://de.wikipedia.org/wiki/DomainKeys_Identified_Mail) Einträge.
- Besitzen eines ordnungsgemäßen [DMARC](https://de.wikipedia.org/wiki/DMARC) Datensatzes und einer Richtlinie oder verwenden von [ARC](https://de.wikipedia.org/wiki/Authenticated_Received_Chain) für die Authentifizierung. Wenn die DMARC-Authentifizierung verwendet wird, muss die Richtlinie auf `reject` oder `quarantine` eingestellt sein.
- Eine Server-Suite-Einstellung mit TLS 1.2 oder höher und ein Plan für [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [SMTPS](https://de.wikipedia.org/wiki/SMTPS) Übermittlung, vorausgesetzt, SMTP wird verwendet.
- Website-Sicherheitsstandards wie z. B.:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subresource Integrity](https://en.wikipedia.org/wiki/Subresource_Integrity) wenn Dinge von externen Domains geladen werden.
- Must support viewing of [message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**Im Besten Fall:**

- Unterstützung für Hardware-Authentisierung, z. B. U2F and [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) zusätzlich zur DANE-Unterstützung.
- Implementation of [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Veröffentlichte Sicherheitsaudits durch ein angesehenes Drittunternehmen.
- Bug-Bounty-Programme und/oder ein koordiniertes Verfahren zur Offenlegung von Sicherheitslücken.
- Website-Sicherheitsstandards wie z. B.:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Vertrauen

Du würdest jemandem mit einer gefälschten Identität nicht deine Finanzen anvertrauen, warum solltest du ihm also deine E-Mails anvertrauen? Wir verlangen von den von uns empfohlenen Anbietern, dass sie ihre Eigentumsverhältnisse oder ihre Führungsrolle öffentlich machen. Außerdem wünschen wir uns häufige Transparenzberichte, insbesondere über die Bearbeitung von Regierungsanfragen.

**Mindestvoraussetzung um zu qualifizieren:**

- Öffentliche Führung oder Eigentum.

**Im Besten Fall:**

- Häufige Transparenzberichte.

### Marketing

With the email providers we recommend, we like to see responsible marketing.

**Mindestvoraussetzung um sich zu qualifizieren:**

- Sie müssen Ihre Analyse-Werkzeuge selbst hosten (kein Google Analytics, Adobe Analytics, etc.). The provider's site must also comply with [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) for those who wish to opt out.

Must not have any irresponsible marketing, which can include the following:

- Behauptung einer "unknackbaren Verschlüsselung". Die Verschlüsselung sollte in der Voraussicht eingesetzt werden, dass sie in Zukunft möglicherweise nicht mehr geheim ist, wenn die Technologie vorhanden ist, um sie zu knacken.
- Gewährleistung eines 100%igen Schutzes der Anonymität. Wenn jemand behauptet, etwas sei zu 100% sicher, bedeutet das, dass es keine Sicherheit für ein Scheitern gibt. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:

    - Wiederverwendung persönlicher Informationen (z. B. E-Mail-Konten, eindeutige Pseudonyme usw.), auf die sie ohne Anonymisierungssoftware (Tor, VPN usw.) zugegriffen haben
    - [Browser-Fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Im besten Fall:**

- Clear and easy to read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### Zusätzliche Funktionalitäten

Obwohl es sich nicht um strenge Anforderungen handelt, haben wir bei der Auswahl der zu empfehlenden Anbieter auch andere Faktoren wie Komfort oder Datenschutz berücksichtigt.
