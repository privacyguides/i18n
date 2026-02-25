---
meta_title: "Empfehlungen für verschlüsselte private E-Mail-Dienste - Privacy Guides"
title: E-Mail Dienste
icon: material/email
description: Diese E-Mail-Dienstleister speichern deine E-Mails sicher und viele davon bieten auch interoperable OpenPGP-Verschlüsselung mit anderen Anbietern.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-server-network: Diensteanbieter](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

E-Mail ist praktisch eine Voraussetzung für die Nutzung aller Online-Dienste, wir empfehlen sie jedoch nicht zur Kommunikation von Mensch zu Mensch. Anstatt E-Mails für die Kontaktaufnahme mit anderen Personen zu verwenden, überleg ob du einen Instant Messenger benutzen kannst, der Forward Secrecy (auf Deutsch etwa "vorwärts gerichtete Geheimhaltung") unterstützt.

[Empfohlene Instant Messenger](real-time-communication.md ""){.md-button}

## Empfohlene Anbieter

Für alles andere empfehlen wir eine Reihe von E-Mail-Anbietern, die auf nachhaltigen Geschäftsmodellen basieren und integrierte Sicherheits- und Datenschutzfunktionen bieten. Weitere Informationen findest du in unserem [vollständigen Kriterienkatalog](#criteria).

| Anbieter                      | OpenPGP / WKD                          | IMAP / SMTP                                                           | Null-Zugriff-Verschlüsselung                        | Anonyme Zahlungsmethoden                    |
| ----------------------------- | -------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------- | ------------------------------------------- |
| [Proton Mail](#proton-mail)   | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Nur kostenpflichtige Pläne | :material-check:{ .pg-green }                       | Bar<br>Monero über Dritte             |
| [Mailbox Mail](#mailbox-mail) | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                                         | :material-information-outline:{ .pg-blue } Nur Mail | Bargeld                                     |
| [Tuta](#tuta)                 | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                                | :material-check:{ .pg-green }                       | Monero über Dritte<br>Bar über Dritte |

Zusätzlich (oder statt) eines Email-Providers die hier empfohlen sind, kann man ebenfalls einen [E-Mail-Aliasing-Service](email-aliasing.md#recommended-providers) benutzen, um deine Privatsphäre zu schützen. Diese Dienste können unter anderem dazu beitragen, deinen echten Posteingang vor Spam zu schützen, zu verhindern, dass Vermarkter deine Konten miteinander in Verbindung bringen, und alle eingehenden Nachrichten mit PGP zu verschlüsseln.

- [Weitere Informationen :material-arrow-right-drop-circle:](email-aliasing.md)

## OpenPGP-kompatible Dienste

Diese Anbieter unterstützen OpenPGP verschlüsselung/entschlüsselung und den [Web Key Directory (WKD) Standard](basics/email-security.md#what-is-the-web-key-directory-standard), was dir erlaubt End-zu-End-Verschlüsselung unabhängig vom Anbieter zu haben. Zum Beispiel, ein Proton Mail Nutzer könnte eine E2EE Nachricht einen Mailbox Mail Nutzer schicken, oder du könntest auch OpenPGP-verschlüsselte Benachrichtigungen von Internetservices bekommen, die es unterstützen.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](#proton-mail)
- ![Mailbox Mail logo](assets/img/email/mailbox-mail.svg){ .twemoji } [Mailbox Mail](#mailbox-mail)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warnung</p>

Wenn du eine E2EE-Technologie wie OpenPGP verwendest, enthält deine E-Mail immer noch einige unverschlüsselte Metadaten im Header bzw. Quelltext der E-Mail, einschließlich der Betreffzeile! Lies mehr über [E-Mail-Metadaten](basics/email-security.md#email-metadata-overview).



- [Wie schütze ich meine privaten schlüssel?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** ist ein E-Mail-Dienst mit dem Schwerpunkt auf Datenschutz, Verschlüsselung, Sicherheit und Benutzerfreundlichkeit. Sie sind seit 2013 in Betrieb. Die Proton AG hat ihren Sitz in Genf, Schweiz.

Der Proton Free Plan kommt mit 500 MB von Mail-Speicher, was du kostenlos auf 1 GB erhöhen kannst.

[:octicons-home-16: Homepage](https://proton.me/de/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/de/mail/privacy-policy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://proton.me/de/support/mail){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Quellcode" }

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

Kostenlose Konten haben Beschränkungen, z.B. kann man nicht Nachrichten mithilfe des Email Körpers suchen und man hat kein Zugriff zur [Proton Mail Bridge](https://proton.me/mail/bridge), die gebraucht wird, um einer der empfohlenen [Email-Clients](email-clients.md) wie z.B. Thunderbird zu benutzen. Bezahlte Konten umfassen Funktionen wie Proton Mail Bridge, zusätzlichen Speicher und die Nutzung eigener Domains. Der Proton Unlimited Plan oder jeder Multi-Nutzer Proton Plan beinhaltet Zugriff zu [SimpleLogin](email-aliasing.md#simplelogin) Premium.

Ein [Bescheinigungsschreiben](https://res.cloudinary.com/dbulfrlrz/images/v1714639878/wp-pme/letter-of-attestation-proton-mail-20211109_3138714c61/letter-of-attestation-proton-mail-20211109_3138714c61.pdf) wurde für Proton Mails Apps im November 2021 von [Securitum](https://research.securitum.com) zur Verfügung gestellt.

Proton Mail hat interne Ausfallberichte, die **nicht** mit Dritten geteilt werden und die deaktiviert werden können.

=== "Web"

    Von deinem Postfach, klicke auf :gear: → **Alle Einstellungen** → **Konto** → **Sicherheit und Datenschutz** →**Privatsphäre und Datenerfassung**.

    - [ ] Deaktiviere **Nutzungsdiagnosedaten sammeln**
    - [ ] Deaktiviere **Absturzberichte senden**

=== "Handy"

    Von deinem Postfach, Wähle :material-menu: →:gear: **Einstellungen** → wähle dein Benutzername.

    - [ ] Deaktiviere **Absturzberichte senden**
    - [ ] Deaktiviere **Nutzungsdiagnosedaten sammeln**

#### :material-check:{ .pg-green } Eigene Domains und Aliase

Nutzer eines kostenpflichtigen Proton Mail Tarifs können ihre eigene Domain oder eine [Catch-All](https://proton.me/support/catch-all) Adresse nutzen. Proton Mail unterstützt auch [Subadressen](https://proton.me/support/creating-aliases), was für Personen nützlich ist, die keine eigene Domain erwerben möchten.

#### :material-check:{ .pg-green } Diskrete Zahlungsmöglichkeiten

Proton Mail [nimmt](https://proton.me/support/payment-options) **Bargeld** per Post sowie Standardüberweisung/Debit Karte, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) und PayPal Zahlungen an. Zusätzlich, kann man auch [**Monero**](cryptocurrency.md#monero) benutzen, um Gutscheine für Proton Mail Plus oder Proton Unlimited über deren [offiziellen](https://discuss.privacyguides.net/t/add-monero-as-an-anonymous-payment-method-for-proton-services/31058/15) Reseller [ProxyStore](https://dys2p.com/en/2025-09-09-proton.html) kaufen.

#### :material-check:{ .pg-green } Kontosicherheit

Proton Mail unterstützt TOTP [Zwei-Faktor-Authentisierung](https://proton.me/support/two-factor-authentication-2fa) und [Hardware-Sicherheitsschlüssel](https://proton.me/support/2fa-security-key) mittels FIDO2 oder U2F Standard. Um einen Hardware-Sicherheitsschlüssel zu nutzen, muss zuerst ein TOTP Code eingerichtet sein.

#### :material-check:{ .pg-green } Datensicherheit

Proton Mail verfügt über [Zero-Access-Verschlüsselung](https://proton.me/de/blog/zero-access-encryption) bei Ablage auf dem Server für deine E-Mails und [Kalender](https://proton.me/de/blog/protoncalendar-security-model). Die mit einer Zero-Access-Verschlüsselung gesicherten Daten sind nur für dich zugänglich.

Bestimmte Informationen, die in [Proton Contacts](https://proton.me/support/proton-contacts) gespeichert sind, wie z. B. Anzeigenamen und E-Mail-Adressen, sind nicht mit einer Zero-Access-Verschlüsselung gesichert. Kontaktfelder, die eine Zero-Access-Verschlüsselung unterstützen, wie z. B. Telefonnummern, sind mit einem Vorhängeschloss-Symbol gekennzeichnet.

#### :material-check:{ .pg-green } E-Mail-Verschlüsselung

Proton Mail hat [die OpenPGP-Verschlüsselung](https://proton.me/support/how-to-use-pgp) in sein Webmail integriert. E-Mails an andere Proton Mail-Konten werden automatisch verschlüsselt. Die Verschlüsselung an Nicht-Proton Mail-Adressen mit einem OpenPGP-Schlüssel kannst du ganz einfach in deinen Kontoeinstellungen aktivieren. Proton unterstützt ebenfalls automatische externe Schlüssel-Entdeckung mit WKD. Das bedeutet, dass E-Mails an andere Anbieter, die WKD verwenden, automatisch auch mit OpenPGP verschlüsselt werden, ohne dass du manuell öffentliche PGP-Schlüssel mit deinen Kontakten austauschen musst. Außerdem ist es möglich, [Nachrichten an Nicht-Proton-Mail-Adressen ohne OpenPGP zu verschlüsseln](https://proton.me/support/password-protected-emails), ohne dass die Empfänger ein Proton-Mail-Konto benötigen.

Auch veröffentlicht Proton Mail öffentlichen Schlüssel der Proton-Konten über HTTP von ihrem WKD. Dies erlaubt Leute die nicht Proton Mail benutzen, leichter die OpenPGP Schlüsseln von Proton Mail Konten für anbieterübergreifender E2EE zu finden. Dies gilt nur für E-mail-Adressen, die mit den Domänen von Proton enden, z.B. `@proton.me`. Wenn du deine eigenen Domains benutzt, musst du selber [WKD konfigurieren](basics/email-security.md#what-is-the-web-key-directory-standard).

#### :material-information-outline:{ .pg-blue } Kontokündigung

Wenn du ein kostenpflichtiges Konto hast und deine Rechnung [nach 14 Tagen noch nicht bezahlt ist](https://proton.me/de/support/delinquency), kannst du nicht mehr auf Ihre Daten zugreifen. Nach 30 Tagen wird dein Konto als säumig markiert und kann keine E-Mails mehr empfangen. Während dieses Zeitraums werden dir die Kosten weiterhin in Rechnung gestellt. Proton [löscht inaktive kostenlose Konten](https://proton.me/support/inactive-accounts) nach einem Jahr. Du kannst die E-Mail-Adresse eines deaktivierten Kontos **nicht** wiederverwenden.

#### :material-information-outline:{ .pg-blue } Zusätzliche Funktionen

Proton Mails [Unlimited Plan](https://proton.me/support/proton-plans#proton-unlimited) erlaubt Zugriff zu anderen Proton-Diensten sowie mehrere benutzerdefinierte Domains, unlimitierte hide-my-email-Aliases und 500 GB Speicher.

### Mailbox Mail

<div class="admonition recommendation" markdown>

![Mailbox Mail logo](assets/img/email/mailbox-mail.svg){ align=right }

**Mailbox Mail** (ehemalig *Mailbox.org*) ist ein E-Mail-Anbieter mit Fokus auf Sicherheit sowie Werbungsfreiheit und wird von 100% umweltverträglicher Energie betrieben. Er wird seit 2014 betrieben. Mailbox Mail hat ihren Sitz in Berlin, Deutschland.

Konten starten mit bis zu 2 GB Speicher, welches bei Nachfrage erweitert werden kann.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/de/datenschutz){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://kb.mailbox.org/de/privat){ .card-link title="Dokumentation" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Eigene Domains und Aliase

Mailbox Mail lässt dir deine eigene Domain benutzen, und sie unterstützen [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) Adressen. Mailbox Mail unterstützt ebenfalls [Unteradressen](https://kb.mailbox.org/de/privat/e-mail/e-mail-aliasse-bei-mailbox/#was-genau-ist-ein-alias), was Nutzvoll ist, wenn du keine Domain kaufen möchtest.

#### :material-check:{ .pg-green } Diskrete Zahlungsmöglichkeiten

Mailbox Mail unterstützt keine Kryptowährung da deren Zahlungsanbieter BitPay ihre Geschäfte in Deutschland abgebrochen haben. Allerdings nehmen sie **Bargeld** über Post, **Bareinzahlung auf Bankkonto **, Überweisung, Kreditkarten, PayPal und manche deutschen Zahlungsanbieter: Paydirekt und Sofortüberweisung an.

#### :material-check:{ .pg-green } Kontosicherheit

Mailbox Mail unterstützt [Zwei-Faktor-Authentifizierung](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) nur für ihre Webmail. Du kannst entweder TOTP oder einen [YubiKey](security-keys.md#yubikey)über die [YubiCloud](https://yubico.com/products/services-software/yubicloud) benutzen. Webstandards wie [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) sind noch nicht unterstützt.

#### :material-information-outline:{ .pg-blue } Datensicherheit

Mailbox Mail erlaubt für Verschlüsselung von eingehende Mails über ihre [verschlüsselte Mailbox](https://kb.mailbox.org/de/privat/e-mail/e-mails-definitiv-sicher-versenden/#der-sichere-e-mail-empfang). Neue eingehende Nachrichten werden dann sofort mit deinem öffentlichen Schlüssel verschlüsselt.

Allerdings unterstützt die Softwareplattform die von Mailbox Mail verwendet wird, [Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange) nicht die [Verschlüsselung deines Adressbuches oder deines Kalenders](https://kb.mailbox.org/de/privat/sicherheit-privatsphaere/sind-kalender-und-adressbuch-verschluesselt/#kalender-und-adressbuch-sind-derzeit-nicht-verschl%C3%BCsselt). Eine [eigenständige Option](calendar.md) könnte daher für diese Daten geeigneter sein.

#### :material-check:{ .pg-green } E-Mail-Verschlüsselung

Mailbox Mail has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox Mail's servers. Diese Funktion ist nützlich, wenn der Empfänger OpenPGP nicht nutzt und daher eine Kopie der E-Mail in seinem eigenen Postfach nicht entschlüsseln kann.

Mailbox Mail also supports the discovery of public keys via HTTP from their WKD. This allows people outside of Mailbox Mail to find the OpenPGP keys of Mailbox Mail accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Mailbox Mail's own domains, like `@mailbox.org`. Wenn du deine eigenen Domains benutzt, musst du selber [WKD konfigurieren](basics/email-security.md#what-is-the-web-key-directory-standard).

#### :material-information-outline:{ .pg-blue } Kontokündigung

Nach Ablauf deines Vertrags wird dein Konto zunächst auf ein eingeschränktes Benutzerkonto umgestellt. Dieses wird nach [30 Tagen](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract) unwiderruflich gelöscht.

#### :material-information-outline:{ .pg-blue } Zusätzliche Funktionen

You can access your Mailbox Mail account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). Auf die Webmail-Schnittstelle kann jedoch nicht über den .onion-Dienst zugegriffen werden und es können TLS-Zertifikatsfehler auftreten.

Alle Konten verfügen über einen begrenzten Cloud-Speicher, der [verschlüsselt werden kann](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox Mail also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox Mail also supports [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) in addition to standard access protocols like IMAP and POP3.

Mailbox Mail has a digital legacy feature for all plans. You can choose whether you want any of your data to be passed to heirs, providing that they apply and provide your testament. Alternativ kannst du auch eine Person mit Namen und Adresse benennen.

## Weitere Anbieter

Diese Anbieter speichern deine E-Mails mit Zero-Knowledge-Verschlüsselung und sind damit eine gute Option für die Sicherheit deiner gespeicherten E-Mails. Allerdings unterstützen sie keine Interoperablen Verschlüsselungsstandards für Ende zu Ende Verschlüsselung zwischen verschiedenen Anbietern.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (ehemals *Tutanota*) ist ein E-Mail-Dienst mit einem Fokus auf Sicherheit und Privatsphäre durch Verschlüsselung. Tuta ist seit 2011 in Betrieb und hat seinen Sitz in Hannover, Deutschland.

Kostenlose Konten starten mit 1 GB Speicher.

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/de/privacy-policy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://tuta.com/de/support){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://tuta.com/de/community){ .card-link title="Mitwirken" }

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

Tuta unterstützt weder das [IMAP-Protokoll](https://tuta.com/support#imap) noch die Verwendung von [E-Mail-Clients](email-clients.md) von Drittanbietern, und du kannst auch keine [externen E-Mail-Konten](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) zur Tuta-App hinzufügen. Auch der [E-Mail-Import](https://github.com/tutao/tutanota/issues/630) wird derzeit nicht unterstützt, was sich aber [bald ändern](https://tuta.com/blog/kickoff-import) soll. E-Mails können [einzeln oder per Massenauswahl](https://tuta.com/support#generalMail) pro Ordner exportiert werden, was bei vielen Ordnern unpraktisch sein kann.

#### :material-check:{ .pg-green } Eigene Domains und Aliase

Bezahlte Tuta-Konten können je nach Tarif entweder 15 oder 30 Aliase und unbegrenzte Aliase auf [benutzerdefinierten Domains](https://tuta.com/support#custom-domain) verwenden. Tuta lässt keine [Unteradressen (Plus-Adressen)](https://tuta.com/support#plus) zu, du kannst aber einen [Catch-All](https://tuta.com/support#settings-global) mit einer benutzerdefinierten Domain verwenden.

#### :material-information-outline:{ .pg-blue } Private Zahlungsmöglichkeiten

Tuta only directly accepts credit cards and PayPal, however you can use [**cryptocurrency**](cryptocurrency.md) to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with ProxyStore.

#### :material-check:{ .pg-green } Kontosicherheit

Tuta unterstützt die [Zwei-Faktor-Authentisierung](https://tuta.com/support#2fa) entweder mit TOTP oder U2F.

#### :material-check:{ .pg-green } Datensicherheit

Tuta has [zero-access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). Das bedeutet, dass die in deinem Konto gespeicherten Nachrichten und andere Daten nur von dir gelesen werden können.

#### :material-information-outline:{ .pg-blue } E-Mail-Verschlüsselung

Tuta [verwendet kein OpenPGP](https://tuta.com/support/#pgp). Tuta-Konten können verschlüsselte E-Mails von Nicht-Tuta-E-Mail-Konten nur empfangen, wenn sie über ein temporäres Tuta-Postfach [gesendet werden](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Kontokündigung

Tuta [löscht inaktive kostenlose Konten](https://tuta.com/support#inactive-accounts) nach sechs Monaten. Du kannst ein deaktiviertes kostenloses Konto wieder verwenden, wenn du bezahlst.

#### :material-information-outline:{ .pg-blue } Zusätzliche Funktionen

Tuta bietet die Business-Version von [Tuta für gemeinnützige Organisationen](https://tuta.com/blog/secure-email-for-non-profit) kostenlos oder mit einem starken Rabatt.

## Kriterien

**Bitte beachte, dass wir mit keinem der von uns empfohlenen Anbieter verbunden sind.** Zusätzlich zu [unseren Standardkriterien](about/criteria.md)haben wir eine Reihe klarer Anforderungen für jeden E-Mail-Anbieter entwickelt, der empfohlen werden möchte, darunter die Umsetzung branchenweit bewährter Verfahren, moderne Technologien und weiteres. Wir empfehlen, sich mit dieser Liste vertraut zu machen, bevor du dich für einen E-Mail-Anbieter entscheidest, und deine eigenen Nachforschungen anzustellst, um sicherzustellen, dass der gewählte E-Mail-Anbieter die richtige Wahl für dich ist.

### Technologien

Wir halten diese Merkmale für wichtig, um einen sicheren und optimalen Service zu bieten. You should consider whether the provider has the features you require.

**Mindestvoraussetzung um sich zu qualifizieren:**

- Must encrypt email account data at rest with zero-access encryption.
- Must be capable of exporting emails as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .EML with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Benutzerdefinierte Domänennamen sind für die Nutzer wichtig, da du so deine Identität von dem Dienst fernhalten kannst, falls dieser sich als schlecht erweist oder von einem anderen Unternehmen übernommen wird, bei dem der Datenschutz keine Rolle spielt.
- Must operate on owned infrastructure, i.e. not built upon third-party email service providers.

**Im besten Fall:**

- Should encrypt all account data (contacts, calendars, etc.) at rest with zero-access encryption.
- Should provide integrated webmail E2EE/PGP encryption as a convenience.
- Should support WKD to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key with this command: `gpg --locate-key example_user@example.com`.
- Unterstützung für eine temporäre Mailbox für externe Benutzer. This is useful when you want to send an encrypted email without sending an actual copy to your recipient. Diese E-Mails haben in der Regel eine begrenzte Lebensdauer und werden dann automatisch gelöscht. Sie erfordern auch nicht, dass der Empfänger eine Kryptographie wie OpenPGP konfiguriert.
- Should support [sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Should allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Benutzerdefinierte Domänennamen sind für die Nutzer wichtig, da du so deine Identität von dem Dienst fernhalten kannst, falls dieser sich als schlecht erweist oder von einem anderen Unternehmen übernommen wird, bei dem der Datenschutz keine Rolle spielt.
- Catch-all or alias functionality for those who use their own domains.
- Should use standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.
- Email provider's services should be available via an [onion service](https://en.wikipedia.org/wiki/.onion).

### Datenschutz

Wir ziehen es vor, dass die von uns empfohlenen Anbieter*innen so wenig Daten wie möglich sammeln.

**Mindestvoraussetzung um zu qualifizieren:**

- Must protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Must not require personally identifiable information (PII) besides a username and a password.
- Privacy policy must meet the requirements defined by the GDPR.

**Im besten Fall:**

- Should accept [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Should be hosted in a jurisdiction with strong email privacy protection laws.

### Sicherheit

Email servers deal with a lot of very sensitive data. We expect that providers will adopt industry best practices in order to protect their customers.

**Mindestvoraussetzung um zu qualifizieren:**

- Protection of webmail with 2FA, such as [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Zero-access encryption, which builds on encryption at rest. Der Anbieter verfügt nicht über die Entschlüsselungsschlüssel zu den Daten, die er besitzt. So wird verhindert, dass ein abtrünniger Mitarbeitender Daten preisgibt, auf die er/sie Zugriff hat, oder dass ein Angreifender Daten freigibt, die er/sie gestohlen hat, indem er/sie sich unbefugt Zugang zum Server verschafft.
- [DNSSEC](https://de.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) Unterstützung.
- Keine TLS-Fehler oder -Schwachstellen beim Profiling durch Tools wie [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh)oder [Qualys SSL Labs](https://ssllabs.com/ssltest); dies schließt zertifikatsbezogene Fehler und schwache DH-Parameter ein, wie z. B. die, die zu [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)) führten.
- A server suite preference (optional on TLS 1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- Eine gültige [MTA-STS](https://tools.ietf.org/html/rfc8461) und [TLS-RPT](https://tools.ietf.org/html/rfc8460) Richtlinie.
- Gültige [DANE](https://de.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) Datensätze.
- Gültige [SPF](https://de.wikipedia.org/wiki/Sender_Policy_Framework) und [DKIM](https://de.wikipedia.org/wiki/DomainKeys_Identified_Mail) Einträge.
- Must have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. Wenn die DMARC-Authentifizierung verwendet wird, muss die Richtlinie auf `reject` oder `quarantine` eingestellt sein.
- Eine Server-Suite-Einstellung mit TLS 1.2 oder höher und ein Plan für [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [SMTPS](https://de.wikipedia.org/wiki/SMTPS) Übermittlung, vorausgesetzt, SMTP wird verwendet.
- Website-Sicherheitsstandards wie z. B.:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subresource Integrity](https://en.wikipedia.org/wiki/Subresource_Integrity) wenn Dinge von externen Domains geladen werden.
- Muss die Anzeige von [Message Headers](https://de.wikipedia.org/wiki/Header_(E-Mail)) unterstützen, da dies eine wichtige forensische Funktion ist, um festzustellen, ob eine E-Mail ein Phishing-Versuch ist.

**Im besten Fall:**

- Should support hardware authentication, i.e. U2F und [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) zusätzlich zur DANE-Unterstützung.
- Should implement [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Published security audits from a reputable, third-party firm.
- Bug-Bounty-Programme und/oder ein koordiniertes Verfahren zur Offenlegung von Sicherheitslücken.
- Website-Sicherheitsstandards wie z. B.:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Vertrauen

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? Wir setzen für die von uns empfohlenen Anbietern voraus, dass sie ihre Eigentumsverhältnisse oder ihre Führungsrolle öffentlich gemacht haben. Außerdem wünschen wir uns häufige Transparenzberichte, insbesondere über die Bearbeitung von Regierungsanfragen.

**Mindestvoraussetzung um zu qualifizieren:**

- Öffentliche Führung oder Eigentum.

**Im besten Fall:**

- Häufige Transparenzberichte.

### Marketing

With the email providers we recommend, we like to see responsible marketing.

**Mindestvoraussetzung um zu qualifizieren:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.).
- Must not have any irresponsible marketing, which can include the following:
    - Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
    - Guarantees of protecting anonymity 100%. When someone makes a claim that something is 100%, it means there is no certainty for failure. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:
        - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software such as Tor
        - [Browser-Fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Im besten Fall:**

- Clear and easy-to-read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### Zusätzliche Funktionalitäten

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
