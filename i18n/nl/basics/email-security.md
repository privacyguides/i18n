---
meta_title: "Waarom e-mail niet de beste keuze is voor privacy en veiligheid - Privacy Guides"
title: E-mail Beveiliging
icon: material/email
description: E-mail is op veel manieren onveilig en dit zijn enkele van de redenen waarom het niet onze eerste keuze is voor veilige communicatie.
---

E-mail is standaard een onveilige vorm van communicatie. Je kunt je e-mailbeveiliging verbeteren met tools zoals OpenPGP, die end-to-end encryptie toevoegen aan je berichten, maar OpenPGP heeft nog steeds een aantal nadelen vergeleken met encryptie in andere berichtenapplicaties.

Als gevolg hiervan wordt e-mail het beste gebruikt voor het ontvangen van transactionele e-mails (zoals meldingen, verificatie e-mails, wachtwoordresets, enz.) van de services waarvoor je je online aanmeldt, niet voor het communiceren met anderen.

## Overzicht van e-mailversleuteling

De standaardmanier om E2EE toe te voegen aan e-mails tussen verschillende e-mailproviders is door OpenPGP te gebruiken. Er zijn verschillende implementaties van de OpenPGP-standaard, waarvan [GnuPG](../encryption.md#gnu-privacy-guard) en [OpenPGP.js](https://openpgpjs.org) de meest voorkomende zijn.

Even if you use OpenPGP, it does not support [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), which means if the private key of either you or the message recipient is ever stolen, all previous messages encrypted with it will be exposed. Daarom bevelen wij [instant messengers](../real-time-communication.md) aan, die indien mogelijk forward secrecy implementeren in plaats van e-mail voor communicatie van persoon tot persoon.

There is another standard which is popular with business called [S/MIME](https://en.wikipedia.org/wiki/S/MIME), however it requires a certificate issued from a [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (not all of them issue S/MIME certificates, and often a yearly payment is required). In some cases it is more usable than PGP because it has support in popular/mainstream email applications like Apple Mail, [Google Workplace](https://support.google.com/a/topic/9061730), and [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). However, S/MIME does not solve the issue of lack of forward secrecy, and isn't particularly more secure than PGP.

## What is the Web Key Directory standard?

The [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. Email clients which support WKD will ask the recipient's server for a key based on the email address' domain name. For example, if you emailed `jonah@privacyguides.org`, your email client would ask `privacyguides.org` for Jonah's OpenPGP key, and if `privacyguides.org` has a key for that account, your message would be automatically encrypted.

In addition to the [email clients we recommend](../email-clients.md) which support WKD, some webmail providers also support WKD. Whether *your own* key is published to WKD for others to use depends on your domain configuration. If you use an [email provider](../email.md#openpgp-compatible-services) which supports WKD, such as Proton Mail or Mailbox Mail, they can publish your OpenPGP key on their domain for you.

If you use your own custom domain, you will need to configure WKD separately. If you control your domain name, you can set up WKD regardless of your email provider. One easy way to do this is to use the "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" feature from the `keys.openpgp.org` server: Set a CNAME record on the `openpgpkey` subdomain of your domain pointed to `wkd.keys.openpgp.org`, then upload your key to [keys.openpgp.org](https://keys.openpgp.org). Alternatively, you can [self-host WKD on your own web server](https://wiki.gnupg.org/WKDHosting).

If you use a shared domain from a provider which doesn't support WKD, like `@gmail.com`, you won't be able to share your OpenPGP key with others via this method.

### Welke e-mailclients ondersteunen E2EE?

E-mailproviders die je in staat stellen standaard toegangsprotocollen zoals IMAP en SMTP te gebruiken, kunnen worden gebruikt met elk van de [e-mailclients die wij aanbevelen](../email-clients.md). Depending on the authentication method, this may lead to decreased security if either the provider or the email client does not support [OAuth](account-creation.md#sign-in-with-oauth) or a bridge application as [multifactor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### Hoe bescherm ik mijn private sleutels?

A smart card (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smart card and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smart card to avoid possibly exposing your private key to a compromised device.

## Overzicht e-mailmetagegevens

Email metadata is stored in the [message header](https://en.wikipedia.org/wiki/Email#Message_header) of the email message and includes some visible headers that you may have seen such as `To`, `From`, `Cc`, `Date`, and `Subject`. Veel e-mailclients en -providers hebben ook een aantal verborgen headers die informatie over jouw account kunnen onthullen.

Client-software kan metagegevens over e-mail gebruiken om aan te geven van wie een bericht afkomstig is en hoe laat het werd ontvangen. Servers kunnen het gebruiken om te bepalen waar een e-mailbericht naartoe moet worden gestuurd, naast [andere doeleinden](https://en.wikipedia.org/wiki/Email#Message_header) die niet altijd transparant zijn.

### Wie kan e-mailmetagegevens bekijken?

Email metadata is protected from outside observers with [opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS), but it is still able to be seen by your email client software (or webmail) and any servers relaying the message from you to any recipients including your email provider. Soms maken e-mailservers ook gebruik van diensten van derden ter bescherming tegen spam, die over het algemeen ook toegang hebben tot jouw berichten.

### Waarom kan metadata niet E2EE zijn?

E-mail metadata is van cruciaal belang voor de meest elementaire functionaliteit van e-mail (waar het vandaan komt, en waar het naartoe moet). E2EE was not built into standard email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
