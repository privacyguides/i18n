---
meta_title: "Waarom e-mail niet de beste keuze is voor privacy en veiligheid - Privacy Guides"
title: Email beveiliging
icon: material/email
description: Email is insecure in many ways, and these are some of the reasons it isn't our top choice for secure communications.
---

E-mail is standaard een onveilige vorm van communicatie. You can improve your email security with tools such as OpenPGP, which add End-to-End Encryption to your messages, but OpenPGP still has a number of drawbacks compared to encryption in other messaging applications.

Als gevolg hiervan wordt e-mail het beste gebruikt voor het ontvangen van transactionele e-mails (zoals meldingen, verificatie-e-mails, wachtwoordresets, enz.) van de services waarvoor je je online aanmeldt, niet voor het communiceren met anderen.

## Overzicht van e-mailversleuteling

De standaardmanier om E2EE toe te voegen aan e-mails tussen verschillende e-mailproviders is door OpenPGP te gebruiken. Er zijn verschillende implementaties van de OpenPGP-standaard, waarvan [GnuPG](https://en.wikipedia.org/wiki/GNU_Privacy_Guard) en [OpenPGP.js](https://openpgpjs.org)de meest voorkomende zijn.

Zelfs als je OpenPGP gebruikt, biedt het geen ondersteuning voor [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), wat betekent dat als jouw privésleutel of die van de ontvanger ooit wordt gestolen, alle eerdere berichten die ermee zijn versleuteld, openbaar worden. Daarom bevelen wij [instant messengers](../real-time-communication.md) aan, die indien mogelijk forward secrecy implementeren in plaats van e-mail voor communicatie van persoon tot persoon.

There is another standard which is popular with business called [S/MIME](https://en.wikipedia.org/wiki/S/MIME), however, it requires a certificate issued from a [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (not all of them issue S/MIME certificates, and often a yearly payment is required). In some cases it is more usable than PGP because it has support in popular/mainstream email applications like Apple Mail, [Google Workplace](https://support.google.com/a/topic/9061730), and [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). However, S/MIME does not solve the issue of lack of forward secrecy, and isn't particularly more secure than PGP.

## What is the Web Key Directory standard?

The [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. Email clients which support WKD will ask the recipient's server for a key based on the email address' domain name. For example, if you emailed `jonah@privacyguides.org`, your email client would ask `privacyguides.org` for Jonah's OpenPGP key, and if `privacyguides.org` has a key for that account, your message would be automatically encrypted.

In addition to the [email clients we recommend](../email-clients.md) which support WKD, some webmail providers also support WKD. Whether *your own* key is published to WKD for others to use depends on your domain configuration. If you use an [email provider](../email.md#openpgp-compatible-services) which supports WKD, such as Proton Mail or Mailbox.org, they can publish your OpenPGP key on their domain for you.

If you use your own custom domain, you will need to configure WKD separately. If you control your domain name, you can set up WKD regardless of your email provider. One easy way to do this is to use the "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" feature from keys.openpgp.org, by setting a CNAME record on the `openpgpkey` subdomain of your domain pointed to `wkd.keys.openpgp.org`, then uploading your key to [keys.openpgp.org](https://keys.openpgp.org). Alternatively, you can [self-host WKD on your own web server](https://wiki.gnupg.org/WKDHosting).

If you use a shared domain from a provider which doesn't support WKD, like @gmail.com, you won't be able to share your OpenPGP key with others via this method.

### Welke e-mailclients ondersteunen E2EE?

E-mailproviders die je in staat stellen standaard toegangsprotocollen zoals IMAP en SMTP te gebruiken, kunnen worden gebruikt met elk van de [e-mailclients die wij aanbevelen](../email-clients.md). Depending on the authentication method, this may lead to the decrease security if either the provider or the email client does not support OATH or a bridge application as [multifactor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### Hoe bescherm ik mijn private sleutels?

A smart card (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smart card and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smart card to avoid possibly exposing your private key to a compromised device.

## Overzicht e-mailmetagegevens

E-mail metadata wordt opgeslagen in de [message header](https://en.wikipedia.org/wiki/Email#Message_header) van het e-mailbericht en omvat een aantal zichtbare headers die je wellicht hebt gezien, zoals: `Aan`, `Van`, `Cc`, `Datum`, `Onderwerp`. Veel e-mailclients en -providers hebben ook een aantal verborgen headers die informatie over jouw account kunnen onthullen.

Client-software kan metagegevens over e-mail gebruiken om aan te geven van wie een bericht afkomstig is en hoe laat het werd ontvangen. Servers kunnen het gebruiken om te bepalen waar een e-mailbericht naartoe moet worden gestuurd, naast [andere doeleinden](https://en.wikipedia.org/wiki/Email#Message_header) die niet altijd transparant zijn.

### Wie kan e-mailmetagegevens bekijken?

E-mail metadata wordt beschermd tegen externe waarnemers met [Opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS), maar kan nog steeds worden gezien door jouw e-mail client software (of webmail) en alle servers die het bericht van je doorsturen naar alle ontvangers, inclusief jouw e-mail provider. Soms maken e-mailservers ook gebruik van diensten van derden ter bescherming tegen spam, die over het algemeen ook toegang hebben tot jouw berichten.

### Waarom kan metadata niet E2EE zijn?

E-mail metadata is van cruciaal belang voor de meest elementaire functionaliteit van e-mail (waar het vandaan komt, en waar het naartoe moet). E2EE was oorspronkelijk niet in de e-mailprotocollen ingebouwd; in plaats daarvan was extra software zoals OpenPGP nodig. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
