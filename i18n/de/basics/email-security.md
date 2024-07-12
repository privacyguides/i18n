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

The Web Key Directory (WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. Email clients which support WKD will ask the recipient's server for a key based on the email address' domain name. For example, if you emailed `jonah@privacyguides.org`, your email client would ask `privacyguides.org` for Jonah's OpenPGP key, and if `privacyguides.org` has a key for that account, your message would be automatically encrypted.

In addition to the [email clients we recommend](../email-clients.md) which support WKD, some webmail providers also support WKD. Whether *your own* key is published to WKD for others to use depends on your domain configuration. If you use an [email provider](../email.md#openpgp-compatible-services) which supports WKD, such as Proton Mail or Mailbox.org, they can publish your OpenPGP key on their domain for you.

If you use your own custom domain, you will need to configure WKD separately. If you control your domain name, you can set up WKD regardless of your email provider. One easy way to do this is to use the "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" feature from keys.openpgp.org, by setting a CNAME record on the `openpgpkey` subdomain of your domain pointed to `wkd.keys.openpgp.org`, then uploading your key to [keys.openpgp.org](https://keys.openpgp.org). Alternatively, you can [self-host WKD on your own web server](https://wiki.gnupg.org/WKDHosting).

If you use a shared domain from a provider which doesn't support WKD, like @gmail.com, you won't be able to share your OpenPGP key with others via this method.

### What Email Clients Support E2EE?

Email providers which allow you to use standard access protocols like IMAP and SMTP can be used with any of the [email clients we recommend](../email-clients.md). Depending on the authentication method, this may lead to the decrease security if either the provider or the email client does not support OATH or a bridge application as [multi-factor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### How Do I Protect My Private Keys?

A smartcard (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smartcard and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smartcard to avoid possibly exposing your private key to a compromised device.

## Email Metadata Overview

Email metadata is stored in the [message header](https://en.wikipedia.org/wiki/Email#Message_header) of the email message and includes some visible headers that you may have seen such as: `To`, `From`, `Cc`, `Date`, `Subject`. There are also a number of hidden headers included by many email clients and providers that can reveal information about your account.

Client software may use email metadata to show who a message is from and what time it was received. Servers may use it to determine where an email message must be sent, among [other purposes](https://en.wikipedia.org/wiki/Email#Message_header) which are not always transparent.

### Who Can View Email Metadata?

Email metadata is protected from outside observers with [Opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS) protecting it from outside observers, but it is still able to be seen by your email client software (or webmail) and any servers relaying the message from you to any recipients including your email provider. Sometimes email servers will also use third-party services to protect against spam, which generally also have access to your messages.

### Why Can't Metadata be E2EE?

Email metadata is crucial to the most basic functionality of email (where it came from, and where it has to go). E2EE was not built into the email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt email metadata, only the message body itself. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as who you're emailing, the subject lines, when you're emailing, etc.
