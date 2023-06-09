---
meta_title: "Empfehlungen für verschlüsselte private E-Mail-Dienste - Privacy Guides"
title: "E-Mail Dienste"
icon: material/email
description: Diese E-Mail-Dienstleister speichern deine E-Mails sicher und viele davon bieten auch interoperable OpenPGP-Verschlüsselung mit anderen Anbietern.
cover: email.png
---

E-Mail ist praktisch eine Voraussetzung für die Nutzung aller Online-Dienste, wir empfehlen sie jedoch nicht zur Kommunikation von Mensch zu Mensch. Anstatt E-Mails für die Kontaktaufnahme mit anderen Personen zu verwenden, überleg ob du einen Instant Messenger benutzen kannst, der Forward Secrecy (auf Deutsch etwa "vorwärts gerichtete Geheimhaltung") unterstützt.

[Empfohlene Instant Messenger](real-time-communication.md ""){.md-button}

Für alles andere empfehlen wir eine Reihe von E-Mail-Anbietern, die auf nachhaltigen Geschäftsmodellen basieren und integrierte Sicherheits- und Datenschutzfunktionen bieten.

- [OpenPGP-kompatible E-Mail-Anbieter :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [Andere verschlüsselte Anbieter :material-arrow-right-drop-circle:](#more-providers)
- [E-Mail-Alias-Dienste :material-arrow-right-drop-circle:](#email-aliasing-services)
- [Selbstbetreibbare Optionen :material-arrow-right-drop-circle:](#self-hosting-email)

## OpenPGP-kompatible Dienste

Diese Anbieter unterstützen von Haus aus die OpenPGP-Ver- und Entschlüsselung und den Web Key Directory (WKD)-Standard, so dass anbieterunabhängige E2E-verschlüsselte E-Mails möglich sind. Zum Beispiel können Kunden von Proton Mail eine E2EE-Nachricht an Kunden von Mailbox.org senden oder sie können OpenPGP-verschlüsselte Benachrichtigungen von Internetdiensten erhalten, die dies unterstützen.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

!!! warning

    Bei der Verwendung von E2EE-Technologien wie OpenPGP enthalten E-Mails immer noch einige Metadaten in der Kopfzeile der E-Mail die nicht verschlüsselt sind. Mehr über [E-Mail Metadaten](basics/email-security.md#email-metadata-overview).
    
    OpenPGP unterstützt auch keine Perfect Forward Secrecy, d. h. wenn entweder dein eigener privater Schlüssel oder der deines Kommunikationspartners gestohlen wird, sind alle vorher damit verschlüsselten Nachrichten offengelegt. [Wie schütze ich meine privaten Schlüssel?](basics/email-security.md#how-do-i-protect-my-private-keys)

### Proton Mail

!!! recommendation

    ![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }
    
    **Proton Mail** ist ein E-Mail-Dienst mit dem Schwerpunkt auf Datenschutz, Verschlüsselung, Sicherheit und Benutzerfreundlichkeit. Sie sind seit **2013** in Betrieb. Die Proton AG hat ihren Sitz in Genf, Schweiz. Konten im kostenlosen Tarif beginnen mit 1 GB Speicherplatz.
    
    [:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Dienst" }
    [:octicons-eye-16:](https://proton.me/legal/privacy/){ .card-link title="Datenschutzrichtlinie" }
    [:octicons-info-16:](https://proton.me/support/mail/){ .card-link title=Dokumentation}
    [:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Quellcode" }
    
    ??? downloads
    
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id979659905)
        - [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
        - [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
        - [:simple-apple: macOS](https://proton.me/mail/bridge#download)
        - [:simple-linux: Linux](https://proton.me/mail/bridge#download)
        - [:octicons-browser-16: Web](https://mail.proton.me)

Kostenlose Konten haben einige Einschränkungen, wie z. B. die fehlende Möglichkeit Text zu durchsuchen und keinen Zugang zu [Proton Mail Bridge](https://proton.me/mail/bridge). Diese ist für die Verwendung eines [empfohlenen Desktop-E-Mail-Programms](email-clients.md) (z. B. Thunderbird) erforderlich. Bezahlte Konten umfassen Funktionen wie Proton Mail Bridge, zusätzlichen Speicher und die Nutzung eigener Domains. Am 9. November 2021 wurden durch [Securitum](https://research.securitum.com) ein Sicherheitsaudit durchgeführt und  die Anwendungen von Proton Mail [zertifiziert](https://proton.me/blog/security-audit-all-proton-apps).

Wenn du den Proton Unlimited, Business oder Visionary Tarif nutzt, erhältst du zusätzlich [SimpleLogin](#simplelogin) Premium kostenlos dazu.

Proton Mail hat interne Absturzberichte, die sie **nicht** mit Dritten teilen. Die Absturzberichte können in den Einstellungen deaktiviert werden: **Einstellungen** > **Gehe zu Einstellungen** > **Konto** > **Sicherheit und Datenschutz** > **Absturzberichte senden**.

#### :material-check:{ .pg-green } Eigene Domains und Aliase

Nutzer eines kostenpflichtigen Proton Mail Tarifs können ihre eigene Domain oder eine [Catch-All](https://proton.me/support/catch-all) Adresse nutzen. Proton Mail unterstützt auch [Unteradressierung](https://proton.me/support/creating-aliases), dieses ist für Leute nützlich, die keine Domain kaufen möchten.

#### :material-check:{ .pg-green } Diskrete Zahlungsmöglichkeiten

Proton Mail akzeptiert, neben den üblichen Zahlungen per Kredit-/Debitkarte, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc)und PayPal, auch [Bargeld per Post](https://proton.me/support/payment-options).

#### :material-check:{ .pg-green } Kontosicherheit

Proton Mail unterstützt TOTP [Zwei-Faktor-Authentifizierung](https://proton.me/de/support/two-factor-authentication-2fa) und [Hardware-Sicherheitsschlüssel](https://proton.me/de/support/2fa-security-key) unter Verwendung der Standards FIDO2 oder U2F. Für die Verwendung eines Hardwaresicherheitsschlüssels muss zunächst die TOTP-Zwei-Faktor-Authentifizierung eingerichtet werden.

#### :material-check:{ .pg-green } Datensicherheit

Proton Mail verfügt über [Zero-Access-Verschlüsselung](https://proton.me/de/blog/zero-access-encryption) bei Ablage auf dem Server für deine E-Mails und [Kalender](https://proton.me/de/blog/protoncalendar-security-model). Die mit einer Zero-Access-Verschlüsselung gesicherten Daten sind nur für dich zugänglich.

Bestimmte Informationen, die in [Proton Contacts](https://proton.me/support/proton-contacts) gespeichert sind, wie z. B. Anzeigenamen und E-Mail-Adressen, sind nicht mit einer Zero-Access-Verschlüsselung gesichert. Kontaktfelder, die eine Zero-Access-Verschlüsselung unterstützen, wie z. B. Telefonnummern, sind mit einem Vorhängeschloss-Symbol gekennzeichnet.

#### :material-check:{ .pg-green } E-Mail-Verschlüsselung

Proton Mail hat [die OpenPGP-Verschlüsselung](https://proton.me/support/how-to-use-pgp) in sein Webmail integriert. E-Mails an andere Proton Mail-Konten werden automatisch verschlüsselt. Die Verschlüsselung an Nicht-Proton Mail-Adressen mit einem OpenPGP-Schlüssel kannst du ganz einfach in deinen Kontoeinstellungen aktivieren. Es ist auch möglich, [Nachrichten an Nicht-Proton-Mail-Adressen](https://proton.me/de/support/password-protected-emails) zu verschlüsseln, ohne dass diese sich für ein Proton-Mail-Konto anmelden oder Software wie OpenPGP verwenden müssen.

Proton Mail unterstützt auch die Suche nach öffentlichen Schlüsseln über HTTP in ihrem [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Dies ermöglicht es Personen, die Proton Mail nicht verwenden, die OpenPGP-Schlüssel von Proton Mail-Konten für anbieterübergreifende E2EE leicht zu finden.

#### :material-information-outline:{ .pg-blue } Kontokündigung

Wenn du ein kostenpflichtiges Konto hast und deine Rechnung [nach 14 Tagen noch nicht bezahlt ist](https://proton.me/de/support/delinquency), kannst du nicht mehr auf Ihre Daten zugreifen. Nach 30 Tagen wird dein Konto als säumig markiert und kann keine E-Mails mehr empfangen. Während dieses Zeitraums werden dir die Kosten weiterhin in Rechnung gestellt.

#### :material-information-outline:{ .pg-blue } Zusätzliche Funktionen

Proton Mail bietet einen "Unlimited"-Tarif für 9,99 €/Monat an, der zusätzlich zu mehreren Konten, Domains, Aliasen und 500 GB Speicherplatz auch den Zugang zu Proton VPN ermöglicht.

Proton Mail bietet keine Funktion für deinen digitalen Nachlass.

### Mailbox.org

!!! recommendation

    ![Mailbox.org-Logo](assets/img/email/mailboxorg.svg){ align=right }
    
    **Mailbox.org** ist ein E-Mail-Dienst, mit dem Ziel sicher und werbefrei zu sein und der mit 100 % erneuerbaren Energien betrieben wird. Er wird seit 2014 betrieben. Mailbox.org hat seinen Sitz in Berlin, Deutschland. Konten im günstigsten Tarif beginnen mit 2 GB Speicherplatz, der je nach Bedarf erweitert werden kann.
    
    [:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mailbox.org/de/datenschutz){ .card-link title="Datenschutzhinweise" }
    [:octicons-info-16:](https://kb.mailbox.org/de/privat){ .card-link title=Dokumentation}
    
    ??? downloads
    
        - [:octicons-browser-16: Web](https://login.mailbox.org)

#### :material-check:{ .pg-green } Eigene Domains und Aliase

Bei Mailbox.org kannst du deine eigene Domain verwenden, und sie unterstützen [Catch-All](https://kb.mailbox.org/de/privat/e-mail-mit-eigener-domain/eine-eigene-domain-mit-catch-all-benutzen) Adressen. Mailbox.org unterstützt auch die [Subadressierung/Aliasse](https://kb.mailbox.org/de/privat/e-mail-artikel/was-sind-aliasse-und-wie-nutze-ich-sie), was hilfreich ist, wenn du keine Domain kaufen möchtest.

#### :material-check:{ .pg-green } Diskrete Zahlungsmöglichkeiten

Mailbox.org akzeptiert keine Kryptowährungen, da deren Zahlungsanbieter BitPay seinen Betrieb in Deutschland eingestellt hat. Sie akzeptieren jedoch Bargeld per Post, Barzahlung auf ein Bankkonto, Banküberweisung, Kreditkarte, PayPal und einige Deutschland spezifische Anbieter: paydirekt und Sofortüberweisung.

#### :material-check:{ .pg-green } Kontosicherheit

Mailbox.org unterstützt [Zwei-Faktor-Authentifizierung](https://kb.mailbox.org/de/privat/sicherheit-privatsphaere-artikel/die-zwei-faktor-authentifizierung-einrichten) nur für Webmail. Du kannst entweder TOTP oder einen [YubiKey](https://de.wikipedia.org/wiki/Yubikey) über die [YubiCloud](https://www.yubico.com/products/services-software/yubicloud)verwenden. Webstandards wie [WebAuthn](https://de.wikipedia.org/wiki/WebAuthn) werden noch nicht unterstützt.

#### :material-information-outline:{ .pg-blue } Datensicherheit

Mailbox.org ermöglicht die Verschlüsselung eingehender E-Mails mit ihrem [verschlüsselten Postfach](https://kb.mailbox.org/display/MBOKBEN/The+Encrypted+Mailbox). Neue eingehende Nachrichten werden dann sofort mit deinem öffentlichen Schlüssel verschlüsselt.

Allerdings unterstützt [Open-Exchange](https://de.wikipedia.org/wiki/Open-Xchange), die von Mailbox.org verwendete Softwareplattform, [nicht](https://kb.mailbox.org/de/business/sicherheit-privatsphaere-artikel/sind-kalender-und-adressbuch-verschluesselt) die Verschlüsselung deines Adressbuchs und Kalenders. Eine [eigenständige Lösung](calendar.md) könnte für diese Informationen besser geeignet sein.

#### :material-check:{ .pg-green } E-Mail-Verschlüsselung

Mailbox.org hat [eine Verschlüsselung](https://kb.mailbox.org/de/privat/verschluesselung-mit-mailbox-org-guard/verschluesselte-nachrichten-versenden) in ihr Webmail integriert, die den Versand von Nachrichten an Personen mit öffentlichen OpenPGP-Schlüsseln vereinfacht. Sie ermöglichen auch [Empfängern, die kein Mailbox.org Konto besitzen, eine E-Mail auf den Servern von Mailbox.org zu entschlüsseln](https://kb.mailbox.org/de/privat/verschluesselung-mit-mailbox-org-guard/verschluesselte-nachrichten-versenden#VerschluesselteNachrichtenversenden-Waspassiert,wennderEmpf%C3%A4ngerkeinPGPnutzt?). Diese Funktion ist nützlich, wenn der Empfänger OpenPGP nicht nutzt und daher eine Kopie der E-Mail in seinem eigenen Postfach nicht entschlüsseln kann.

Mailbox.org unterstützt auch die Suche nach öffentlichen Schlüsseln über HTTP von ihrem [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Dies ermöglicht es Personen, die Mailbox.org nicht verwenden, die OpenPGP-Schlüssel von Mailbox.org-Konten für anbieterübergreifende E2EE leicht zu finden.

#### :material-information-outline:{ .pg-blue } Kontokündigung

Ihr Konto wird bei Vertragsende auf ein eingeschränktes Benutzerkonto umgestellt, nach [30 Tagen wird es unwiderruflich gelöscht](https://kb.mailbox.org/de/privat/ihr-account-bei-mailbox-org/mailbox-org-bezahlen#mailbox.orgbezahlen-MeineVertragslaufzeitistabgelaufen-wasjetzt?).

#### :material-information-outline:{ .pg-blue } Zusätzliche Funktionen

Du kannst auf dein Mailbox.org-Konto über IMAP/SMTP zugreifen, indem du den [.onion-Dienst](https://kb.mailbox.org/de/privat/sicherheit-privatsphaere-artikel/den-tor-exit-node-von-mailbox-org-verwenden) nutzt. Auf die Webmail-Schnittstelle kann jedoch nicht über den .onion-Dienst zugegriffen werden und es können TLS-Zertifikatsfehler auftreten.

Alle Konten verfügen über einen begrenzten Cloud-Speicher, der [verschlüsselt werden kann](https://kb.mailbox.org/de/privat/datei-cloud-mailbox-org-drive/verschluesselung-im-drive). Mailbox.org bietet auch den Alias [@secure.mailbox.org](https://kb.mailbox.org/de/privat/e-mail-artikel/e-mails-definitiv-sicher-versenden) an, der die TLS-Verschlüsselung der Verbindung zwischen den Mailservern erzwingt, da die Nachricht sonst gar nicht gesendet wird. Mailbox.org unterstützt neben den Standardzugriffsprotokollen wie IMAP und POP3 auch [Exchange ActiveSync](https://de.wikipedia.org/wiki/Exchange_ActiveSync).

Mailbox.org bietet für alle Tarife eine digitale Hinterlassenschaft an. Du kannst wählen, ob deine Daten an die Erben weitergegeben werden sollen, sofern diese einen Antrag stellen und dein Testament vorlegen. Alternativ kannst du auch eine Person mit Namen und Adresse benennen.

## Weitere Anbieter

Diese Anbieter speichern deine E-Mails mit Zero-Knowledge-Verschlüsselung und sind damit eine gute Option für die Sicherheit deiner gespeicherten E-Mails. However, they don't support interoperable encryption standards for E2EE communications between different providers.

<div class="grid cards" markdown>

- ![Skiff Mail logo](assets/img/email/skiff-mail.svg){ .twemoji } [Skiff Mail](email.md#skiff-mail)
- ![Tutanota logo](assets/img/email/tutanota.svg){ .twemoji } [Tutanota](email.md#tutanota)

</div>

### Skiff Mail

!!! recommendation

    ![Skiff Mail logo](assets/img/email/skiff-mail.svg){ align=right }
    
    **Skiff Mail** is a web based email service with E2EE that began in 2020 that is based in San Francisco with developers worldwide. Accounts start with 10GB of free storage.
    
    [:octicons-home-16: Homepage](https://skiff.com/mail){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://app.skiff.com/docs/db93c237-84c2-4b2b-9588-19a7cd2cd45a#tyGksN9rkqbo2uGYASxsA6HVLjUoly/wTYK8tncTto8=){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://skiff.com/help){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/skiff-org/skiff-apps){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-android: Android](https://play.google.com/store/apps/details?id=com.skemailmobileapp&pli=1)
        - [:simple-appstore: iOS](https://apps.apple.com/us/app/skiff-mail/id1619168801)
        - [:octicons-browser-16: Web](https://app.skiff.com/mail)

Skiff has undergone a few [audits](https://skiff.com/transparency) during its development.

#### :material-check:{ .pg-green } Eigene Domains und Aliase

You can create up to 3 additional @skiff.com email aliases in addition to your primary account address on their free plan. [Custom domains](https://skiff.com/blog/custom-domain-setup) are available on their Pro or Business plan, and allow you to create unlimited aliases.

#### :material-alert-outline:{ .pg-orange } Private Payment Methods

Skiff Mail accepts cryptocurrency payments via Coinbase Commerce, including Bitcoin and Ethereum, but they do not accept our recommended [cryptocurrency](cryptocurrency.md), Monero. They also accept credit card payments via Stripe.

#### :material-check:{ .pg-green } Kontosicherheit

Skiff Mail supports TOTP two-factor authentication and hardware security keys using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two-factor authentication first.

#### :material-check:{ .pg-green } Datensicherheit

Skiff Mail has zero access encryption at rest for all of your data. Das bedeutet, dass die in Ihrem Konto gespeicherten Nachrichten und anderen Daten nur von dir gelesen werden können.

#### :material-information-outline:{ .pg-blue } E-Mail-Verschlüsselung

Skiff Mail does not use OpenPGP. Emails are only encrypted with E2EE to other Skiff Mail users. Skiff does not have a "temporary inbox" or "passworded email" feature like some other providers have, so that external users cannot receive or reply to messages with E2EE.

#### :material-information-outline:{ .pg-blue } Kontokündigung

Skiff Mail accounts do not expire, but unpaid accounts will be prompted to remove any enabled paid features (such as additional aliases) or renew their plan before the account can be used.

#### :material-information-outline:{ .pg-blue } Zusätzliche Funktionen

Skiff additionally offers [workspace productivity features](https://discuss.privacyguides.net/t/skiff-pages-drive-productivity-tools/11758/13), but we still prefer [alternative](productivity.md) options for collaborating and file sharing at this time.

Skiff Mail does not offer a digital legacy feature.

### Tutanota

!!! recommendation

    ![Tutanota-Logo](assets/img/email/tutanota.svg){ align=right }
    
    **Tutanota** ist ein E-Mail-Dienst, dessen Schwerpunkt auf Sicherheit und Datenschutz durch Verschlüsselung liegt. Tutanota ist seit **2011** in Betrieb und hat seinen Sitz in Hannover. Konten im kostenlosen Tarif beginnen mit 1 GB Speicherplatz.
    
    [:octicons-home-16: Homepage](https://tutanota.com/de/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://tutanota.com/de/privacy-policy){ .card-link title=Datenschutzrichtlinie }
    [:octicons-info-16:](https://tutanota.com/de/faq){ .card-link title=Dokumentation}
    [:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title=Quellcode }
    [:octicons-heart-16:](https://tutanota.com/de/community/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
        - [:simple-appstore: App Store](https://apps.apple.com/app/tutanota/id922429609)
        - [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
        - [:simple-windows11: Windows](https://tutanota.com/#download)
        - [:simple-apple: macOS](https://tutanota.com/#download)
        - [:simple-linux: Linux](https://tutanota.com/#download)
        - [:octicons-browser-16: Web](https://mail.tutanota.com/)

Tutanota unterstützt nicht das [IMAP-Protokoll](https://tutanota.com/de/faq/#imap) oder die Verwendung von [E-Mail-Clients von Drittanbietern](email-clients.md), und Sie können auch keine [externen E-Mail-Konten](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) zur Tutanota-App hinzufügen. Weder [E-Mail-Import](https://github.com/tutao/tutanota/issues/630) noch [Unterordner](https://github.com/tutao/tutanota/issues/927) werden derzeit unterstützt, obwohl dies [geändert werden soll](https://tutanota.com/de/blog/posts/kickoff-import). E-Mails können [einzeln oder per Massenauswahl](https://tutanota.com/howto#generalMail) pro Ordner exportiert werden, was bei vielen Ordnern unpraktisch sein kann.

#### :material-check:{ .pg-green } Eigene Domains und Aliase

Bezahlte Tutanota-Konten können bis zu 5 [Aliase](https://tutanota.com/faq#alias) und [benutzerdefinierte Domains](https://tutanota.com/de/faq#custom-domain) verwenden. Tutanota erlaubt keine [Subadressierung (plus Adressen)](https://tutanota.com/faq#plus), du kannst aber eine [Catch-All Adresse](https://tutanota.com/howto#settings-global) mit einer benutzerdefinierten Domain verwenden.

#### :material-information-outline:{ .pg-blue } Private Zahlungsmöglichkeiten

Tutanota akzeptiert nur Kreditkarten und PayPal, aber [Kryptowährung](cryptocurrency.md) kann verwendet werden, um Geschenkkarten über ihre [Partnerschaft](https://tutanota.com/de/faq/#cryptocurrency) mit Proxystore zu kaufen.

#### :material-check:{ .pg-green } Kontosicherheit

Tutanota unterstützt [Zwei-Faktor-Authentifizierung](https://tutanota.com/de/faq#2fa) entweder mit TOTP oder U2F.

#### :material-check:{ .pg-green } Datensicherheit

Tutanota bietet [Zero Access Encryption at Rest](https://tutanota.com/de/faq#what-encrypted) für Ihre E-Mails, [Adressbuchkontakte](https://tutanota.com/de/faq#encrypted-address-book)und [Kalender](https://tutanota.com/de/faq#calendar). Das bedeutet, dass die in Ihrem Konto gespeicherten Nachrichten und anderen Daten nur von dir gelesen werden können.

#### :material-information-outline:{ .pg-blue } E-Mail-Verschlüsselung

Tutanota [verwendet kein OpenPGP](https://tutanota.com/de/faq#pgp). Tutanota-Konten können verschlüsselte E-Mails von Nicht-Tutanota-E-Mail-Konten nur empfangen, wenn sie über ein temporäres Tutanota-Postfach [gesendet werden](https://www.tutanota.com/howto/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Kontokündigung

Tutanota löscht [naktive kostenlose Konten](https://tutanota.com/de/faq#inactive-accounts) nach sechs Monaten. Du kannst ein deaktiviertes kostenloses Konto wieder verwenden, wenn du bezahlst.

#### :material-information-outline:{ .pg-blue } Zusätzliche Funktionalität

Tutanota bietet die Business-Version von [Tutanota für gemeinnützige Organisationen](https://tutanota.com/blog/posts/secure-email-for-non-profit) kostenlos oder mit einem starken Rabatt an.

Tutanota hat auch eine Geschäftskundenfunktion namens [Secure Connect](https://tutanota.com/secure-connect/). Dadurch wird sichergestellt, dass der Kundenkontakt zum Unternehmen über E2EE erfolgt. Das Feature kostet 240 €/Jahr.

Tutanota bietet keine Funktion für deinen digitalen Nachlass.

## E-Mail-Aliasing-Dienste

Mit einem E-Mail-Aliasing-Dienst können Sie für jede Website, für die Sie sich anmelden, ganz einfach eine neue E-Mail-Adresse generieren. Die von dir erstellten E-Mail-Aliase werden dann an eine E-Mail-Adresse deiner Wahl weitergeleitet, wobei sowohl deine "Haupt"-E-Mail-Adresse als auch die Identität deines E-Mail-Anbieters verborgen bleiben. Echtes E-Mail-Aliasing ist besser als die von vielen Providern verwendete und unterstützte Plus-Adressierung, mit der du Aliase wie DeinName+[irgendetwas]@example.com erstellen kannst, da Websites, Werbetreibende und Tracking-Netzwerke einfach alles nach dem +-Zeichen entfernen können, um deine wahre E-Mail-Adresse zu erfahren.

<div class="grid cards" markdown>

- ![AnonAddy logo](assets/img/email/anonaddy.svg#only-light){ .twemoji }![AnonAddy logo](assets/img/email/anonaddy-dark.svg#only-dark){ .twemoji } [AnonAddy](email.md#anonaddy)
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

### AnonAddy

!!! recommendation

    ![AnonAddy-Logo](assets/img/email/anonaddy.svg#only-light){ align=right }
    ![AnonAddy-Logo](assets/img/email/anonaddy-dark.svg#only-dark){ align=right }
    
    Mit **AnonAddy** kannst du kostenlos 20 Domain-Aliase auf einer gemeinsam genutzten Domain erstellen oder unbegrenzte "Standard"-Aliase, die weniger anonym sind.
    
    [:octicons-home-16: Homepage](https://anonaddy.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://anonaddy.com/privacy/){ .card-link title=Datenschutzrichtlinie }
    [:octicons-info-16:](https://app.anonaddy.com/docs/){ .card-link title=Dokumentation}
    [:octicons-code-16:](https://github.com/anonaddy){ .card-link title=Quelltext }
    [:octicons-heart-16:](https://anonaddy.com/donate/){ .card-link title=Mitwirken }
    
    ??? downloads
    
        - [:simple-android: Android](https://anonaddy.com/faq/#is-there-an-android-app)
        - [:material-apple-ios: iOS](https://anonaddy.com/faq/#is-there-an-ios-app)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/en-GB/firefox/addon/anonaddy/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/anonaddy-anonymous-email/iadbdpnoknmbdeolbapdackdcogdmjpe)

Die Anzahl der gemeinsamen Aliase (die auf eine gemeinsame Domain wie @anonaddy.me enden), die du erstellen kannst, ist beim kostenlosen Plan von AnonAddy auf 20 und beim $12/Jahr-Plan auf 50 begrenzt. Du kannst eine unbegrenzte Anzahl von Standard-Aliasnamen erstellen (die auf eine Domäne wie @[nutzername].anonaddy.com oder eine benutzerdefinierte Domäne bei kostenpflichtigen Tarifen enden), doch wie bereits erwähnt, kann dies dem Datenschutz abträglich sein, da andere Personen deine Standard-Aliasnamen allein auf der Grundlage des Domänennamens trivialerweise miteinander verknüpfen können. Unbegrenzte gemeinsame Aliase sind für $36/Jahr erhältlich.

Bemerkenswerte kostenlose Funktionen:

- [x] 20 Gemeinsame Aliasnamen
- [x] Unbegrenzte Standard-Aliasnamen
- [ ] Keine ausgehenden Antworten
- [x] 2 Empfänger-Mailboxen
- [x] Automatische PGP-Verschlüsselung

### SimpleLogin

!!! recommendation

    ![Simplelogin-Logo](assets/img/email/simplelogin.svg){ align=right }
    
    **SimpleLogin** ist ein kostenloser Dienst, der E-Mail-Aliase für eine Vielzahl von gemeinsam genutzten Domänennamen bereitstellt und optional kostenpflichtige Funktionen wie unbegrenzte Aliase und benutzerdefinierte Domänen bietet.
    
    [:octicons-home-16: Homepage](https://simplelogin.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://simplelogin.io/privacy/){ .card-link title=Datenschutzrichtlinie }
    [:octicons-info-16:](https://simplelogin.io/docs/){ .card-link title=Dokumentation}
    [:octicons-code-16:](https://github.com/simple-login){ .card-link title=Quelltext }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
        - [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/en-US/firefox/addon/simplelogin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
        - [:simple-safari: Safari](https://apps.apple.com/app/id1494051017)

SimpleLogin wurde zum 8. April 2022 [von der Proton AG übernommen](https://proton.me/news/proton-and-simplelogin-join-forces). Wenn du Proton Mail für dein Hauptpostfach verwendest, ist SimpleLogin eine gute Wahl. Da beide Produkte nun demselben Unternehmen gehören, musst du nur noch einem einzigen Unternehmen vertrauen. Wir gehen außerdem davon aus, dass SimpleLogin in Zukunft enger mit den Angeboten von Proton integriert werden wird. SimpleLogin unterstützt weiterhin die Weiterleitung an einen E-Mail-Anbieter deiner Wahl. Securitum hat SimpleLogin Anfang 2022 [geprüft](https://simplelogin.io/blog/security-audit/) und alle Probleme [wurden behoben](https://simplelogin.io/audit2022/web.pdf).

Du kannst dein SimpleLogin-Konto in den Einstellungen mit deinem Proton-Konto verknüpfen. Wenn du den Proton Unlimited, Business oder Visionary Tarif nutzt, erhältst du zusätzlich SimpleLogin Premium kostenlos dazu.

Bemerkenswerte kostenlose Funktionen:

- [x] 10 Gemeinsame Aliasnamen
- [x] Unbegrenzte Antworten
- [x] 1 Empfänger-Mailbox

## E-Mail Selbst Hosten

Fortgeschrittene Systemadministratoren können die Einrichtung eines eigenen E-Mail-Servers in Erwägung ziehen. Mailserver erfordern Aufmerksamkeit und ständige Wartung, um die Sicherheit und die Zuverlässigkeit der Mailzustellung zu gewährleisten.

### Kombinierte Software-Lösungen

!!! recommendation

    ![Mailcow-Logo](assets/img/email/mailcow.svg){ align=right }
    
    **Mailcow** ist ein fortgeschrittener Mailserver, perfekt für diejenigen mit ein wenig mehr Linux-Erfahrung. Es vereinigt alles was du brauchst in einem Docker-Container: Einen Mailserver mit DKIM-Unterstützung, Virenschutz und Spam-Überwachung, Webmail und ActiveSync mit SOGo, sowie eine webbasierte Verwaltung mit 2FA-Unterstützung.
    
    [:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailcow.github.io/mailcow-dockerized-docs/){ .card-link title=Dokumentation}
    [:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title=Datenschutz }
    [:octicons-heart-16:](https://www.servercow.de/mailcow?lang=en#sal){ .card-link title=Mitwirken }

!!! recommendation

    ![Mail-in-a-Box-Logo](assets/img/email/mail-in-a-box.svg){ align=right }
    
    **Mail-in-a-Box** ist ein automatisches Setup-Skript für die Einrichtung eines Mailservers unter Ubuntu. Sein Ziel ist es, die Einrichtung eines eigenen Mailservers zu erleichtern.
    
    [:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Dokumentation}
    [:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title=Quelltext }

Für einen eher manuellen Ansatz haben wir diese beiden Artikel herausgesucht:

- [Einrichten eines Mailservers mit OpenSMTPD, Dovecot und Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd/) (2019)
- [Wie Sie Ihren eigenen Mailserver betreiben](https://www.c0ffee.net/blog/mail-server-guide/) (August 2017)

## Kriterien

**Bitte beachte, dass wir mit keinem der von uns empfohlenen Anbieter verbunden sind.** Zusätzlich zu [unseren Standardkriterien](about/criteria.md)haben wir eine Reihe klarer Anforderungen für jeden E-Mail-Anbieter entwickelt, der empfohlen werden möchte, darunter die Umsetzung branchenweit bewährter Verfahren, moderne Technologien und weiteres. Wir empfehlen, sich mit dieser Liste vertraut zu machen, bevor sich für einen E-Mail-Anbieter entscheiden wird, und eigene Nachforschungen anzustellen, um sicherzustellen, dass der gewählte E-Mail-Anbieter die richtige Wahl für dich ist.

### Technologien

Wir halten diese Merkmale für wichtig, um einen sicheren und optimalen Service zu bieten. Du solltest prüfen, ob der Anbieter über die von dir gewünschten Funktionen verfügt.

**Mindestvoraussetzung um sich zu qualifizieren:**

- Verschlüsselt die Daten von E-Mail-Konten im Ruhezustand mit Zero-Access-Verschlüsselung.
- Exportmöglichkeit als [Mbox](https://de.wikipedia.org/wiki/Mbox) oder individuelle .eml mit [RFC5322](https://datatracker.ietf.org/doc/rfc5322/) Standard.
- Erlaubt es dem Nutzer, seinen eigenen [Domainnamen](https://de.wikipedia.org/wiki/Domain_(Internet)) zu verwenden. Benutzerdefinierte Domänennamen sind für die Nutzer wichtig, da du so deine Identität von dem Dienst fernhalten kannst, falls dieser sich als schlecht erweist oder von einem anderen Unternehmen übernommen wird, bei dem der Datenschutz keine Rolle spielt.
- Arbeitet auf einer eigenen Infrastruktur, d.h. nicht auf der eines Drittanbieters von E-Mail-Diensten.

**Im besten Fall:**

- Verschlüsselt alle Kontodaten (Kontakte, Kalender usw.) im Ruhezustand mit Zero-Access-Verschlüsselung.
- Integrierte Webmail E2EE/PGP-Verschlüsselung als Komfortfunktion.
- Unterstützung für [WKD](https://wiki.gnupg.org/WKD), um die Suche nach öffentlichen OpenPGP-Schlüsseln über HTTP zu verbessern. GnuPG-Benutzer können einen Schlüssel erhalten, indem sie Folgendes eingeben: `gpg --locate-key beispiel_nutzer@example.com`
- Unterstützung für eine temporäre Mailbox für externe Benutzer. Dies ist nützlich, wenn du eine verschlüsselte E-Mail versenden möchtest, ohne eine Kopie an den Empfänger zu senden. Diese E-Mails haben in der Regel eine begrenzte Lebensdauer und werden dann automatisch gelöscht. Sie erfordern auch nicht, dass der Empfänger eine Kryptographie wie OpenPGP konfiguriert.
- Verfügbarkeit der Dienste des E-Mail-Anbieters über einen [onion service](https://de.wikipedia.org/wiki/.onion).
- [Unterstützung von Unteradressen](https://en.wikipedia.org/wiki/Email_address#Subaddressing).
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
- Keine TLS-Fehler oder -Schwachstellen beim Profiling durch Tools wie [Hardenize](https://www.hardenize.com/), [testssl.sh](https://testssl.sh/)oder [Qualys SSL Labs](https://www.ssllabs.com/ssltest); dies schließt zertifikatsbezogene Fehler und schwache DH-Parameter ein, wie z. B. die, die zu [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)) führten.
- Eine Server-Suite-Präferenz (optional bei TLSv1.3) für starke Cipher-Suites, die Forward Secrecy und authentifizierte Verschlüsselung unterstützen.
- Eine gültige [MTA-STS](https://tools.ietf.org/html/rfc8461) und [TLS-RPT](https://tools.ietf.org/html/rfc8460) Richtlinie.
- Gültige [DANE](https://de.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) Datensätze.
- Gültige [SPF](https://de.wikipedia.org/wiki/Sender_Policy_Framework) und [DKIM](https://de.wikipedia.org/wiki/DomainKeys_Identified_Mail) Einträge.
- Besitzen eines ordnungsgemäßen [DMARC](https://de.wikipedia.org/wiki/DMARC) Datensatzes und einer Richtlinie oder verwenden von [ARC](https://de.wikipedia.org/wiki/Authenticated_Received_Chain) für die Authentifizierung. Wenn die DMARC-Authentifizierung verwendet wird, muss die Richtlinie auf `reject` oder `quarantine` eingestellt sein.
- Eine bevorzugte Server-Suite mit TLS 1.2 oder höher und ein Plan für [RFC8996](https://datatracker.ietf.org/doc/rfc8996/).
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
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163/)

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

- Wiederverwendung persönlicher Informationen (z. B. E-Mail-Konten, eindeutige Pseudonyme usw.), auf die sie ohne Anonymisierungssoftware (Tor, VPN usw.) zugegriffen haben
- [Browser-Fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Im Besten Fall:**

- Klare und leicht zu lesende Dokumentation. Dazu gehören Dinge wie die Einrichtung von 2FA, E-Mail-Clients, OpenPGP, usw.

### Zusätzliche Funktionalitäten

Obwohl es sich nicht um strenge Anforderungen handelt, haben wir bei der Auswahl der zu empfehlenden Anbieter auch andere Faktoren wie Komfort oder Datenschutz berücksichtigt.
