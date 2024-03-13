---
meta_title: "Waarom e-mail niet de beste keuze is voor privacy en veiligheid - Privacy Guides"
title: Email beveiliging
icon: material/email
description: E-mail is op vele manieren inherent onveilig, en dit zijn enkele van de redenen waarom het niet onze eerste keuze is voor veilige communicatie.
---

E-mail is standaard een onveilige vorm van communicatie. Je kunt je e-mailbeveiliging verbeteren met tools als OpenPGP, die end-to-end encryptie toevoegen aan je berichten, maar OpenPGP heeft nog steeds een aantal nadelen in vergelijking met encryptie in andere berichtentoepassingen, en sommige e-mailgegevens kunnen nooit inherent worden versleuteld als gevolg van de manier waarop e-mail is ontworpen.

Als gevolg hiervan wordt e-mail het beste gebruikt voor het ontvangen van transactionele e-mails (zoals meldingen, verificatie-e-mails, wachtwoordresets, enz.) van de services waarvoor je je online aanmeldt, niet voor het communiceren met anderen.

## Overzicht van e-mailversleuteling

De standaardmanier om E2EE toe te voegen aan e-mails tussen verschillende e-mailproviders is door OpenPGP te gebruiken. Er zijn verschillende implementaties van de OpenPGP-standaard, waarvan [GnuPG](https://en.wikipedia.org/wiki/GNU_Privacy_Guard) en [OpenPGP.js](https://openpgpjs.org)de meest voorkomende zijn.

Er is een andere standaard die populair is bij bedrijven, [S/MIME](https://en.wikipedia.org/wiki/S/MIME), maar deze vereist een certificaat dat is afgegeven door een [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (niet alle instanties geven S/MIME-certificaten af). It has support in [Google Workplace](https://support.google.com/a/topic/9061730) and [Outlook for Web or Exchange Server 2016, 2019](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480).

Zelfs als je OpenPGP gebruikt, biedt het geen ondersteuning voor [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), wat betekent dat als jouw privésleutel of die van de ontvanger ooit wordt gestolen, alle eerdere berichten die ermee zijn versleuteld, openbaar worden. Daarom bevelen wij [instant messengers](../real-time-communication.md) aan, die indien mogelijk forward secrecy implementeren in plaats van e-mail voor communicatie van persoon tot persoon.

## What is the Web Key Directory standard?

The Web Key Directory (WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. Email clients which support WKD will ask the recipient's server for a key based on the email address' domain name. For example, if you emailed `jonah@privacyguides.org`, your email client would ask `privacyguides.org` for Jonah's OpenPGP key, and if `privacyguides.org` has a key for that account, your message would be automatically encrypted.

In addition to the [email clients we recommend](../email-clients.md) which support WKD, some webmail providers also support WKD. Whether *your own* key is published to WKD for others to use depends on your domain configuration. If you use an [email provider](../email.md#openpgp-compatible-services) which supports WKD, such as Proton Mail or Mailbox.org, they can publish your OpenPGP key on their domain for you.

If you use your own custom domain, you will need to configure WKD separately. If you control your domain name, you can set up WKD regardless of your email provider. One easy way to do this is to use the "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" feature from keys.openpgp.org, by setting a CNAME record on the `openpgpkey` subdomain of your domain pointed to `wkd.keys.openpgp.org`, then uploading your key to [keys.openpgp.org](https://keys.openpgp.org). Alternatively, you can [self-host WKD on your own web server](https://wiki.gnupg.org/WKDHosting).

If you use a shared domain from a provider which doesn't support WKD, like @gmail.com, you won't be able to share your OpenPGP key with others via this method.

### Welke e-mailclients ondersteunen E2EE?

E-mailproviders die je in staat stellen standaard toegangsprotocollen zoals IMAP en SMTP te gebruiken, kunnen worden gebruikt met elk van de [e-mailclients die wij aanbevelen](../email-clients.md). Afhankelijk van de authenticatiemethode kan dit leiden tot een verminderde veiligheid indien de provider of de e-mailclient OATH of een bridge-toepassing niet ondersteunt, aangezien [multifactor authenticatie](/basics/multi-factor-authentication/) niet mogelijk is met gewone wachtwoordauthenticatie.

### Hoe bescherm ik mijn private sleutels?

A smartcard (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](https://nitrokey.com)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. Het bericht wordt vervolgens door de smartcard ontsleuteld en de ontsleutelde inhoud wordt teruggestuurd naar het apparaat.

It is advantageous for the decryption to occur on the smartcard to avoid possibly exposing your private key to a compromised device.

## Overzicht e-mailmetagegevens

E-mail metadata wordt opgeslagen in de [message header](https://en.wikipedia.org/wiki/Email#Message_header) van het e-mailbericht en omvat een aantal zichtbare headers die je wellicht hebt gezien, zoals: `Aan`, `Van`, `Cc`, `Datum`, `Onderwerp`. Veel e-mailclients en -providers hebben ook een aantal verborgen headers die informatie over jouw account kunnen onthullen.

Client-software kan metagegevens over e-mail gebruiken om aan te geven van wie een bericht afkomstig is en hoe laat het werd ontvangen. Servers kunnen het gebruiken om te bepalen waar een e-mailbericht naartoe moet worden gestuurd, naast [andere doeleinden](https://en.wikipedia.org/wiki/Email#Message_header) die niet altijd transparant zijn.

### Wie kan e-mailmetagegevens bekijken?

E-mail metadata wordt beschermd tegen externe waarnemers met [Opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS), maar kan nog steeds worden gezien door jouw e-mail client software (of webmail) en alle servers die het bericht van je doorsturen naar alle ontvangers, inclusief jouw e-mail provider. Soms maken e-mailservers ook gebruik van diensten van derden ter bescherming tegen spam, die over het algemeen ook toegang hebben tot jouw berichten.

### Waarom kan metadata niet E2EE zijn?

E-mail metadata is van cruciaal belang voor de meest elementaire functionaliteit van e-mail (waar het vandaan komt, en waar het naartoe moet). E2EE was oorspronkelijk niet in de e-mailprotocollen ingebouwd; in plaats daarvan was extra software zoals OpenPGP nodig. Omdat OpenPGP-berichten nog steeds met traditionele e-mailproviders moeten werken, kan het niet de metagegevens van e-mail versleutelen, alleen de inhoud van het bericht zelf. Dat betekent dat zelfs wanneer OpenPGP wordt gebruikt, externe waarnemers veel informatie over jouw berichten kunnen zien, zoals wie je e-mailt, de onderwerpregels, wanneer je e-mailt, enz.
