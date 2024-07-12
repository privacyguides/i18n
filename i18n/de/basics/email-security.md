---
meta_title: "Warum E-Mail nicht die beste Wahl für Privatsphäre und Sicherheit ist - Privacy Guides"
title: E-Mail-Sicherheit
icon: material/email
description: Email is inherently insecure in many ways, and these are some of the reasons it isn't our top choice for secure communications.
---

E-Mail ist von Natur aus eine unsichere Form der Kommunikation. Du kannst deine E-Mail-Sicherheit mit Tools wie OpenPGP verbessern, die Ende-zu-Ende-Verschlüsselung zu deinen Nachrichten hinzufügen, aber OpenPGP hat im Vergleich zur Verschlüsselung in anderen Messaging-Anwendungen eine Reihe von Nachteilen. Auch können einige E-Mail-Daten aufgrund der Art und Weise, wie E-Mails konzipiert sind, niemals von sich aus verschlüsselt werden.

Daher sind E-Mails am besten geeignet, um Transaktions-E-Mails (wie Benachrichtigungen, Bestätigungs-E-Mails, Passwortrücksetzungen usw.) von den Online-Diensten zu empfangen, für die du dich anmeldest, und nicht für die Kommunikation mit anderen.

## Übersicht zur E-Mail-Verschlüsselung

Die Standardmethode zum Hinzufügen von E2EE zu E-Mails zwischen verschiedenen E-Mail-Anbietern ist die Verwendung von OpenPGP. Es gibt verschiedene Implementierungen des OpenPGP-Standards, die bekanntesten sind [GnuPG](https://en.wikipedia.org/wiki/GNU_Privacy_Guard) und [OpenPGP.js](https://openpgpjs.org).

Es gibt noch einen anderen, bei Unternehmen beliebten Standard namens [S/MIME](https://en.wikipedia.org/wiki/S/MIME), für den jedoch ein von einer [Zertifizierungsstelle](https://en.wikipedia.org/wiki/Certificate_authority) ausgestelltes Zertifikat erforderlich ist (nicht alle von diesen stellen S/MIME-Zertifikate aus). It has support in [Google Workplace](https://support.google.com/a/topic/9061730) and [Outlook for Web or Exchange Server 2016, 2019](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480).

Selbst wenn du OpenPGP verwendest, unterstützt es keine [Forward Secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), d. h. wenn entweder dein privater Schlüssel oder der des Empfängers gestohlen wird, sind alle vorherigen Nachrichten, die damit verschlüsselt wurden, offengelegt. Aus diesem Grund empfehlen wir [Instant Messenger](../real-time-communication.md) mit Forward Secrecy, für persönliche Kommunikation, wann immer möglich, anstelle von E-Mails.

## Was ist der Web Key Directory Standard?

Der Web Key Directory (WKD) Standard ermöglicht es E-Mail-Clients, den OpenPGP-Schlüssel für andere Postfächer zu ermitteln, auch wenn diese bei einem anderen Anbieter gehostet werden. E-Mail-Clients, die WKD unterstützen, fragen den Server des Empfängers nach einem Schlüssel, der auf dem Domainnamen der E-Mail-Adresse basiert. Wenn du beispielsweise eine E-Mail an `jonah@privacyguides.org` sendest, fragt dein E-Mail-Programm bei `privacyguides.org` nach dem OpenPGP-Schlüssel von Jonah, und falls `privacyguides.org` einen Schlüssel für dieses Konto hat, wird deine Nachricht automatisch verschlüsselt.

Neben den [von uns empfohlenen E-Mail-Clients](../email-clients.md), die WKD unterstützen, gibt es auch einige Webmail-Anbieter, die WKD unterstützen. Ob *dein eigener* Schlüssel für andere bei WKD veröffentlicht wird, hängt von deiner Domainkonfiguration ab. Verwendest du einen [E-Mail-Anbieter](../email.md#openpgp-compatible-services), der WKD unterstützt, wie z. B. Proton Mail oder Mailbox.org, können diese deinen OpenPGP-Schlüssel auf ihrer Domain für dich veröffentlichen.

Um deine eigene Domain zu verwenden, musst du WKD separat konfigurieren. Kontrollierst du deinen Domainnamen, kannst du WKD unabhängig von deinem E-Mail-Anbieter einrichten. Eine einfach Möglichkeit das zu tun, ist die Nutzung der Funktion „[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)“ von keys.openpgp.org, indem du einen CNAME-Eintrag auf der `openpgpkey-Subdomain` deiner Domain setzt, der auf `wkd.keys.openpgp.org` zeigt, und dann deinen Schlüssel auf [keys.openpgp.org](https://keys.openpgp.org) hochlädst. Alternativ kannst du [WKD selbst auf deinem Webserver hosten](https://wiki.gnupg.org/WKDHosting).

Wenn du eine gemeinsam genutzte Domain eines Anbieters verwendest, welcher WKD nicht unterstützt, wie z.B. @gmail.com, kannst du deinen OpenPGP-Schlüssel auf diese Weise nicht mit anderen teilen.

### Welche E-Mail-Clients unterstützen E2EE?

E-Mail-Anbieter, die dir die Verwendung von Standard-Zugriffsprotokollen wie IMPA und SMTP ermöglichen, können mit jedem der [von uns empfohlenen E-Mail-Clients](../email-clients.md) verwendet werden. Abhängig von der Authentifizierungsmethode kann dies zu einer Verringerung der Sicherheit führen, wenn entweder der Anbieter oder der E-Mail-Client OATH oder eine Bridge-Anwendung nicht unterstützt, da eine [Multi-Faktor-Authentifizierung](multi-factor-authentication.md) mit einer reinen Passwort-Authentifizierung nicht möglich ist.

### Wie schütze ich meine privaten Schlüssel?

Eine Smartcard (wie z. B. ein [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) oder [Nitrokey](../security-keys.md#nitrokey)) funktioniert, indem sie eine verschlüsselte E-Mail-Nachricht von einem Gerät (Telefon, Tablet, Computer usw.) empfängt, auf dem ein E-Mail-/Webmail-Client läuft. Die Nachricht wird dann von der Smartcard entschlüsselt und der entschlüsselte Inhalt an das Gerät zurückgeschickt.

Es ist vorteilhaft, wenn die Entschlüsselung auf der Smartcard erfolgt, um zu vermeiden, dass dein privater Schlüssel möglicherweise einem kompromittierten Gerät preisgegeben wird.

## Übersicht über E-Mail-Metadaten

Email metadata is stored in the [message header](https://en.wikipedia.org/wiki/Email#Message_header) of the email message and includes some visible headers that you may have seen such as: `To`, `From`, `Cc`, `Date`, `Subject`. There are also a number of hidden headers included by many email clients and providers that can reveal information about your account.

Client software may use email metadata to show who a message is from and what time it was received. Servers may use it to determine where an email message must be sent, among [other purposes](https://en.wikipedia.org/wiki/Email#Message_header) which are not always transparent.

### Who Can View Email Metadata?

Email metadata is protected from outside observers with [Opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS) protecting it from outside observers, but it is still able to be seen by your email client software (or webmail) and any servers relaying the message from you to any recipients including your email provider. Sometimes email servers will also use third-party services to protect against spam, which generally also have access to your messages.

### Why Can't Metadata be E2EE?

Email metadata is crucial to the most basic functionality of email (where it came from, and where it has to go). E2EE was not built into the email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt email metadata, only the message body itself. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as who you're emailing, the subject lines, when you're emailing, etc.
