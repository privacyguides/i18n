---
meta_title: "Warum E-Mail nicht die beste Wahl für Privatsphäre und Sicherheit ist - Privacy Guides"
title: E-Mail-Sicherheit
icon: material/email
description: Email is insecure in many ways, and these are some of the reasons it isn't our top choice for secure communications.
---

E-Mail ist von Natur aus eine unsichere Form der Kommunikation. You can improve your email security with tools such as OpenPGP, which add end-to-end encryption to your messages, but OpenPGP still has a number of drawbacks compared to encryption in other messaging applications.

Daher sind E-Mails am besten geeignet, um Transaktions-E-Mails (wie Benachrichtigungen, Bestätigungs-E-Mails, Passwortrücksetzungen usw.) von den Online-Diensten zu empfangen, für die du dich anmeldest, und nicht für die Kommunikation mit anderen.

## Übersicht zur E-Mail-Verschlüsselung

Die Standardmethode zum Hinzufügen von E2EE zu E-Mails zwischen verschiedenen E-Mail-Anbietern ist die Verwendung von OpenPGP. There are different implementations of the OpenPGP standard, the most common being [GnuPG](../encryption.md#gnu-privacy-guard) and [OpenPGP.js](https://openpgpjs.org).

Even if you use OpenPGP, it does not support [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), which means if the private key of either you or the message recipient is ever stolen, all previous messages encrypted with it will be exposed. Aus diesem Grund empfehlen wir [Instant Messenger](../real-time-communication.md) mit Forward Secrecy, für persönliche Kommunikation, wann immer möglich, anstelle von E-Mails.

There is another standard which is popular with business called [S/MIME](https://en.wikipedia.org/wiki/S/MIME), however it requires a certificate issued from a [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (not all of them issue S/MIME certificates, and often a yearly payment is required). In some cases it is more usable than PGP because it has support in popular/mainstream email applications like Apple Mail, [Google Workplace](https://support.google.com/a/topic/9061730), and [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). However, S/MIME does not solve the issue of lack of forward secrecy, and isn't particularly more secure than PGP.

## Was ist der Web Key Directory Standard?

The [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. E-Mail-Clients, die WKD unterstützen, fragen den Server des Empfängers nach einem Schlüssel, der auf dem Domainnamen der E-Mail-Adresse basiert. Wenn du beispielsweise eine E-Mail an `jonah@privacyguides.org` sendest, fragt dein E-Mail-Programm bei `privacyguides.org` nach dem OpenPGP-Schlüssel von Jonah, und falls `privacyguides.org` einen Schlüssel für dieses Konto hat, wird deine Nachricht automatisch verschlüsselt.

Neben den [von uns empfohlenen E-Mail-Clients](../email-clients.md), die WKD unterstützen, gibt es auch einige Webmail-Anbieter, die WKD unterstützen. Ob *dein eigener* Schlüssel für andere bei WKD veröffentlicht wird, hängt von deiner Domainkonfiguration ab. If you use an [email provider](../email.md#openpgp-compatible-services) which supports WKD, such as Proton Mail or Mailbox Mail, they can publish your OpenPGP key on their domain for you.

Um deine eigene Domain zu verwenden, musst du WKD separat konfigurieren. Kontrollierst du deinen Domainnamen, kannst du WKD unabhängig von deinem E-Mail-Anbieter einrichten. One easy way to do this is to use the "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" feature from the `keys.openpgp.org` server: Set a CNAME record on the `openpgpkey` subdomain of your domain pointed to `wkd.keys.openpgp.org`, then upload your key to [keys.openpgp.org](https://keys.openpgp.org). Alternativ kannst du [WKD selbst auf deinem Webserver hosten](https://wiki.gnupg.org/WKDHosting).

If you use a shared domain from a provider which doesn't support WKD, like `@gmail.com`, you won't be able to share your OpenPGP key with others via this method.

### Welche E-Mail-Clients unterstützen E2EE?

E-Mail-Anbieter, die dir die Verwendung von Standard-Zugriffsprotokollen wie IMPA und SMTP ermöglichen, können mit jedem der [von uns empfohlenen E-Mail-Clients](../email-clients.md) verwendet werden. Depending on the authentication method, this may lead to decreased security if either the provider or the email client does not support [OAuth](account-creation.md#sign-in-with-oauth) or a bridge application as [multifactor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### Wie schütze ich meine privaten Schlüssel?

Eine Smartcard (wie z. B. ein [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) oder [Nitrokey](../security-keys.md#nitrokey)) funktioniert, indem sie eine verschlüsselte E-Mail-Nachricht von einem Gerät (Telefon, Tablet, Computer etc.) empfängt, auf dem ein E-Mail-/Webmail-Client läuft. Die Nachricht wird dann von der Smartcard entschlüsselt und der entschlüsselte Inhalt an das Gerät zurückgeschickt.

Es ist vorteilhaft, wenn die Entschlüsselung auf der Smartcard erfolgt, um zu vermeiden, dass dein privater Schlüssel möglicherweise einem kompromittierten Gerät preisgegeben wird.

## Übersicht über E-Mail-Metadaten

Email metadata is stored in the [message header](https://en.wikipedia.org/wiki/Email#Message_header) of the email message and includes some visible headers that you may have seen such as `To`, `From`, `Cc`, `Date`, and `Subject`. Viele E-Mail-Clients und -Anbieter fügen außerdem eine Reihe von versteckten Header-Zeilen hinzu, die Informationen über dein Konto preisgeben können.

E-Mail-Programm können Metadaten verwenden, um anzuzeigen, von wem eine Nachricht stammt und wann sie empfangen wurde. Server können sie verwenden, um zu bestimmen, wohin eine E-Mail gesendet werden muss, neben [anderen Zwecken](https://de. wikipedia. org/wiki/Header_(E-Mail)), die nicht immer transparent sind.

### Wer kann E-Mail-Metadaten einsehen?

Email metadata is protected from outside observers with [opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS), but it is still able to be seen by your email client software (or webmail) and any servers relaying the message from you to any recipients including your email provider. Manchmal verwenden E-Mail-Server auch Dienste von Drittanbietern zum Schutz vor Spam, die in der Regel auch Zugang zu deinen Nachrichten haben.

### Warum können Metadaten nicht E2EE werden?

E-Mail-Metadaten sind entscheidend für die grundlegenden Funktionen von E-Mails (woher sie kommen und wohin sie gehen sollen). E2EE was not built into standard email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
