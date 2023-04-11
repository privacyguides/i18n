---
title: "Email Diensten"
icon: material/email
description: Deze e-mailproviders bieden een uitstekende plaats om jouw e-mails veilig op te slaan, en vele bieden interoperabele OpenPGP versleuteling met andere providers.
---

E-mail is bijna een noodzaak voor het gebruik van elke online dienst, maar wij raden het niet aan voor gesprekken van persoon tot persoon. In plaats van e-mail te gebruiken om andere mensen te contacteren, kunt u overwegen een instant messenger te gebruiken die forward secrecy ondersteunt.

[Aanbevolen Instant Messengers](real-time-communication.md ""){.md-button}

Voor al het andere raden wij verschillende e-mailproviders aan op basis van duurzame bedrijfsmodellen en ingebouwde beveiligings- en privacyfuncties.

- [OpenPGP-compatibele e-mailproviders :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [Andere versleutelde aanbieders :material-arrow-right-drop-circle:](#more-providers)
- [E-mail Aliasing Services :material-arrow-right-drop-circle:](#email-aliasing-services)
- [Zelf-gehoste opties :material-arrow-right-drop-circle:](#self-hosting-email)

## OpenPGP compatibele diensten

Deze providers ondersteunen standaard OpenPGP-encryptie/decryptie en het Web Key Directory (WKD) -standaard, waardoor provider-agnostische E2EE-e-mails mogelijk zijn. Een Proton Mail-gebruiker zou bijvoorbeeld een E2EE-bericht kunnen sturen naar een Mailbox.org-gebruiker, of je zou OpenPGP-versleutelde meldingen kunnen ontvangen van internetdiensten die dit ondersteunen.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

!!! warning "Waarschuwing"

    Wanneer gebruik wordt gemaakt van E2EE-technologie zoals OpenPGP, zullen e-mailberichten nog steeds metagegevens bevatten die niet zijn versleuteld in de header van het e-mailbericht. Lees meer over [e-mail metadata](basics/email-security.md#email-metadata-overview).
    
    OpenPGP ondersteunt ook geen forward secrecy, wat betekent dat als jouw of de geadresseerde's privésleutel ooit wordt gestolen, alle eerdere berichten die ermee zijn versleuteld, openbaar worden. [Hoe bescherm ik mijn privésleutels?](basics/email-security.md#how-do-i-protect-my-private-keys)

### Proton Mail

!!! recommendation

    ![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }
    
    **Proton Mail** is een e-maildienst met focus op privacy, encryptie, veiligheid en gebruiksgemak. Ze zijn al actief sinds **2013**. Proton AG is gevestigd in Genève, Zwitserland. Accounts beginnen met 500 MB opslagruimte met hun gratis abonnement.
    
    [:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Privacybeleid" }.
    [:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentatie}
    [:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Broncode" }
    
    ??? downloads "Downloaden"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id979659905)
        - [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
        - [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
        - [:simple-apple: macOS](https://proton.me/mail/bridge#download)
        - [:simple-linux: Linux](https://proton.me/mail/bridge#download)
        - [:octicons-browser-16: Web](https://mail.proton.me)

Gratis accounts hebben enkele beperkingen, zoals het niet kunnen doorzoeken van bodytekst en geen toegang tot [Proton Mail Bridge](https://proton.me/mail/bridge), die nodig is om een [aanbevolen desktop e-mailclient](email-clients.md) (bv. Thunderbird) te gebruiken. Betaalde accounts bevatten functies zoals Proton Mail Bridge, extra opslagruimte en ondersteuning voor aangepaste domeinen. Een [attestatiebrief](https://proton.me/blog/security-audit-all-proton-apps) werd op 9 november 2021 verstrekt voor de apps van Proton Mail door [Securitum](https://research.securitum.com).

Als je Proton Unlimited, Business of Visionary hebt, krijg je ook [SimpleLogin](#simplelogin) Premium gratis.

Proton Mail heeft interne crash rapporten die ze **niet** delen met derden. Dit kan worden uitgeschakeld in: **Instellingen** > **Ga naar Instellingen** > **Account** > **Beveiliging en privacy** > **Crashmeldingen versturen**.

#### :material-check:{ .pg-green } Aangepaste domeinen en aliassen

Betaalde Proton Mail abonnees kunnen hun eigen domein met de dienst gebruiken of een [catch-all](https://proton.me/support/catch-all) adres. Proton Mail ondersteunt ook [subadressering](https://proton.me/support/creating-aliases), wat handig is voor mensen die geen domein willen kopen.

#### :material-check:{ .pg-green } Privé betaalmethoden

Proton Mail [accepteert](https://proton.me/support/payment-options) contant geld per post, naast standaard creditcard/debetkaart, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), en PayPal-betalingen.

#### :material-check:{ .pg-green } Accountbeveiliging

Proton Mail ondersteunt TOTP [two factor authentication](https://proton.me/support/two-factor-authentication-2fa) en [hardware security keys](https://proton.me/support/2fa-security-key) met behulp van FIDO2 of U2F standaarden. Voor het gebruik van een hardware beveiligingssleutel moet eerst TOTP tweefactorauthenticatie worden ingesteld.

#### :material-check:{ .pg-green } Gegevensbeveiliging

Proton Mail heeft [zero-access encryptie](https://proton.me/blog/zero-access-encryption) in rust voor jouw e-mails en [agenda's](https://proton.me/news/protoncalendar-security-model). Gegevens die zijn beveiligd met zero-access encryptie zijn alleen voor jouw toegankelijk.

Bepaalde informatie opgeslagen in [Proton Contacts](https://proton.me/support/proton-contacts), zoals namen en e-mailadressen, zijn niet beveiligd met zero-access encryptie. Contact velden die zero-access encryptie ondersteunen, zoals telefoonnummers, worden aangegeven met een hangslot pictogram.

#### :material-check:{ .pg-green } Email encryptie

Proton Mail heeft [OpenPGP encryptie](https://proton.me/support/how-to-use-pgp) geïntegreerd in hun webmail. E-mails naar andere Proton Mail-accounts worden automatisch versleuteld, en versleuteling naar niet-Proton Mail-adressen met een OpenPGP-sleutel kan eenvoudig worden ingeschakeld in je accountinstellingen. Je kunt hiermee ook [berichten versleutelen naar niet-Proton Mail adressen](https://proton.me/support/password-protected-emails) zonder dat zij zich hoeven aan te melden voor een Proton Mail account of software zoals OpenPGP hoeven te gebruiken.

Proton Mail ondersteunt ook de ontdekking van openbare sleutels via HTTP van hun [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Hierdoor kunnen mensen die geen Proton Mail gebruiken de OpenPGP sleutels van Proton Mail accounts gemakkelijk vinden, voor cross-provider E2EE.


#### :material-information-outline:{ .pg-blue } Beëindiging van account

Als je een betaald account hebt en je na 14 dagen [niet je rekening hebt betaald](https://proton.me/support/delinquency), krijg je geen toegang meer tot je gegevens. Na 30 dagen wordt uw account delinquent en ontvangt u geen inkomende e-mail meer. Tijdens deze periode word je nog steeds gefactureerd.

#### :material-information-outline:{ .pg-blue } Aanvullende functionaliteit

Proton Mail biedt een "Unlimited" account voor €9,99/maand, die ook toegang geeft tot Proton VPN, naast meerdere accounts, domeinen, aliassen en 500 GB opslagruimte.

Proton Mail heeft geen digitale erfenis functie.

### Mailbox.org

!!! recommendation

    ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }
    
    **Mailbox.org** is een e-maildienst gericht op veiligheid, is reclamevrij en wordt 100% mogelijk gemaakt door milieuvriendelijke energie. Ze zijn sinds 2014 in bedrijf. Mailbox.org is gevestigd in Berlijn, Duitsland. Accounts beginnen met 2 GB opslagruimte, die naar behoefte kan worden uitgebreid.
    
    [:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacybeleid" }
    [:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentatie}
    
    ??? downloads "Downloaden"
    
        - [:octicons-browser-16: Web](https://login.mailbox.org)

#### :material-check:{ .pg-green } Aangepaste domeinen en aliassen

Mailbox.org laat je je eigen domein gebruiken en ze ondersteunen [catch-all](https://kb.mailbox.org/display/MBOKBEN/Using+catch-all+alias+with+own+domain) adressen. Mailbox.org ondersteunt ook [subadressering](https://kb.mailbox.org/display/BMBOKBEN/What+is+an+alias+and+how+do+I+use+it), wat handig is als je geen domein wilt kopen.

#### :material-check:{ .pg-green } Privé betaalmethoden

Mailbox.org accepteert geen Bitcoin of andere cryptocurrencies als gevolg van het feit dat hun betalingsverwerker BitPay zijn activiteiten in Duitsland heeft opgeschort. Echter aanvaarden ze wel contant geld per post, contante betaling op bankrekening, bankoverschrijving, kredietkaart, PayPal en een paar Duitse verwerkers: paydirekt en Sofortüberweisung.

#### :material-check:{ .pg-green } Accountbeveiliging

Mailbox.org ondersteunt [twee-factor authenticatie](https://kb.mailbox.org/display/MBOKBEN/How+to+use+two-factor+authentication+-+2FA) alleen voor hun webmail. Je kunt TOTP of een [Yubikey](https://en.wikipedia.org/wiki/YubiKey) gebruiken via de [Yubicloud](https://www.yubico.com/products/services-software/yubicloud). Webstandaarden zoals [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) worden nog niet ondersteund.

#### :material-information-outline:{ .pg-blue } Gegevensbeveiliging

Mailbox.org maakt encryptie van inkomende mail mogelijk met behulp van hun [versleutelde mailbox](https://kb.mailbox.org/display/MBOKBEN/The+Encrypted+Mailbox). Nieuwe berichten die je ontvangt, worden dan onmiddellijk versleuteld met jouw openbare sleutel.

Echter, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), het softwareplatform dat wordt gebruikt door Mailbox.org, [ondersteunt niet](https://kb.mailbox.org/display/BMBOKBEN/Encryption+of+calendar+and+address+book) de versleuteling van je adresboek en agenda. Een [standalone optie](calendar.md) kan geschikter zijn voor die informatie.

#### :material-check:{ .pg-green } Email encryptie

Mailbox.org heeft [geïntegreerde encryptie](https://kb.mailbox.org/display/MBOKBEN/Send+encrypted+e-mails+with+Guard) in hun webmail, wat het verzenden van berichten naar mensen met openbare OpenPGP-sleutels vereenvoudigt. Ook kunnen [ontvangers op afstand een e-mail](https://kb.mailbox.org/display/MBOKBEN/My+recipient+does+not+use+PGP) op de servers van Mailbox.org ontsleutelen. Deze functie is nuttig wanneer de ontvanger op afstand geen OpenPGP heeft en geen kopie van de e-mail in zijn eigen mailbox kan ontsleutelen.

Mailbox.org ondersteunt ook de ontdekking van publieke sleutels via HTTP vanuit hun [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Hierdoor kunnen mensen buiten Mailbox.org gemakkelijk de OpenPGP sleutels van Mailbox.org accounts vinden, voor cross-provider E2EE.

#### :material-information-outline:{ .pg-blue } Beëindiging van account

Je account wordt ingesteld op een beperkt gebruikersaccount zodra je contract is beëindigd, na [30 dagen wordt deze onherroepelijk verwijderd](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Extra functionaliteit

Je kan je Mailbox.org-account openen via IMAP/SMTP met behulp van hun [.onion-service](https://kb.mailbox.org/display/MBOKBEN/The+Tor+exit+node+of+mailbox.org). Hun webmail interface is echter niet toegankelijk via hun .onion dienst en kan je te maken krijgen met TLS-certificaatfouten.

Alle accounts hebben een beperkte cloud opslag die [kan worden versleuteld](https://kb.mailbox.org/display/MBOKBEN/Encrypt+files+on+your+Drive). Mailbox.org biedt ook de alias [@secure.mailbox.org](https://kb.mailbox.org/display/MBOKBEN/Ensuring+E-Mails+are+Sent+Securely), die de TLS-versleuteling op de verbinding tussen mailservers afdwingt, anders wordt het bericht helemaal niet verzonden. Mailbox.org ondersteunt ook [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) naast standaard toegangsprotocollen zoals IMAP en POP3.

Mailbox.org heeft een digitale nalatenschap functie voor alle abonnementen. Je kunt kiezen of je wilt dat jouw gegevens worden doorgegeven aan jouw erfgenamen, mits zij een aanvraag indienen en jouw testament overleggen. Je kunt ook een persoon nomineren met naam en adres.

## Meer providers

Deze providers slaan je e-mails op met zero-knowledge encryptie, waardoor ze geweldige opties zijn om je opgeslagen e-mails veilig te houden. Zij ondersteunen echter geen interoperabele versleutelingsnormen voor E2EE-communicatie tussen aanbieders.

<div class="grid cards" markdown>

- ![StartMail logo](assets/img/email/startmail.svg#only-light){ .twemoji }![StartMail logo](assets/img/email/startmail-dark.svg#only-dark){ .twemoji } [StartMail](email.md#startmail)
- ![Tutanota logo](assets/img/email/tutanota.svg){ .twemoji } [Tutanota](email.md#tutanota)

</div>

### StartMail

!!! recommendation

    ![StartMail-logo](assets/img/email/startmail.svg#only-light){ align=right }
    ![StartMail-logo](assets/img/email/startmail-dark.svg#only-dark){ align=right }
    
    **StartMail** is een e-maildienst met de nadruk op veiligheid en privacy door het gebruik van standaard OpenPGP-versleuteling. StartMail is sinds 2014 actief en is gevestigd in Boulevard 11, Zeist Nederland. Accounts beginnen met 10GB. Ze bieden een 30 dagen proefperiode.
    
    [:octicons-home-16: Homepage](https://www.startmail.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.startmail.com/en/privacy/){ .card-link title="Privacybeleid" }
    [:octicons-info-16:](https://support.startmail.com){ .card-link title=Documentatie}
    
    ??? downloads "Downloaden"
    
        - [:octicons-browser-16: Web](https://mail.startmail.com/login)

#### :material-check:{ .pg-green } Aangepaste domeinen en aliassen

Persoonlijke accounts kunnen [aangepaste of Quick](https://support.startmail.com/hc/en-us/articles/360007297457-Aliases) aliassen gebruiken. [Aangepaste domeinen](https://support.startmail.com/hc/en-us/articles/4403911432209-Setup-a-custom-domain) zijn ook beschikbaar.

#### :material-alert-outline:{ .pg-orange } Privé betaalmethodes

StartMail accepteert Visa, MasterCard, American Express en Paypal. StartMail heeft ook andere [betalingsopties](https://support.startmail.com/hc/en-us/articles/360006620637-Payment-methods) zoals [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) (momenteel alleen voor Persoonlijke accounts) en SEPA Direct Debit voor accounts ouder dan een jaar.

#### :material-check:{ .pg-green } Accountbeveiliging

StartMail ondersteunt TOTP tweefactorauthenticatie [alleen voor webmail](https://support.startmail.com/hc/en-us/articles/360006682158-Two-factor-authentication-2FA). Zij staan geen U2F-authenticatie met beveiligingssleutel toe.

#### :material-information-outline:{ .pg-blue } Gegevensbeveiliging

StartMail heeft [zero access encryptie bij rust](https://www.startmail.com/en/whitepaper/#_Toc458527835), met behulp van hun "user vault" systeem. Wanneer je inlogt, wordt de kluis geopend, en de e-mail wordt dan uit de wachtrij naar de kluis verplaatst, waar hij wordt ontsleuteld met de bijbehorende privésleutel.

StartMail ondersteunt het importeren van [contacten](https://support.startmail.com/hc/en-us/articles/360006495557-Import-contacts) echter, ze zijn alleen toegankelijk in de webmail en niet via protocollen zoals [CalDAV](https://en.wikipedia.org/wiki/CalDAV). Contacten worden ook niet opgeslagen met behulp van zero knowledge encryptie.

#### :material-check:{ .pg-green } Email encryptie

StartMail heeft [encryptie](https://support.startmail.com/hc/en-us/sections/360001889078-Encryption) geïntegreerd in hun webmail, wat het versturen van versleutelde berichten met openbare OpenPGP-sleutels vereenvoudigt. Ze ondersteunen echter niet de Web Key Directory-standaard, waardoor de ontdekking van de openbare sleutel van een Startmail-postvak uitdagender wordt voor andere e-mailproviders of -clients.

#### :material-information-outline:{ .pg-blue } Beëindiging van account

Bij afloop van jouw account, zal StartMail jouw account definitief verwijderen na [6 maanden in 3 fasen](https://support.startmail.com/hc/en-us/articles/360006794398-Account-expiration).

#### :material-information-outline:{ .pg-blue } extra functionaliteit

StartMail maakt proxying van afbeeldingen in e-mails mogelijk. Als je toestaat dat het beeld op afstand wordt geladen, weet de verzender niet wat jouw IP-adres is.

StartMail biedt geen digitale erfenisfunctie.

### Tutanota

!!! recommendation

    ![Tutanota logo](assets/img/email/tutanota.svg){ align=right }
    
    **Tutanota** is een e-maildienst met de nadruk op veiligheid en privacy door het gebruik van encryptie. Tutanota is actief sinds **2011** en is gevestigd in Hannover, Duitsland. Accounts beginnen met 1GB opslagruimte met hun gratis plan.
    
    [:octicons-home-16: Homepage](https://tutanota.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://tutanota.com/privacy){ .card-link title="Privacybeleid" }
    [:octicons-info-16:](https://tutanota.com/faq){ .card-link title=Documentatie}
    [:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Broncode" }
    [:octicons-heart-16:](https://tutanota.com/community/){ .card-link title=Bijdragen }
    
    ??? downloads "Downloaden"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
        - [:simple-appstore: App Store](https://apps.apple.com/app/tutanota/id922429609)
        - [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
        - [:simple-windows11: Windows](https://tutanota.com/#download)
        - [:simple-apple: macOS](https://tutanota.com/#download)
        - [:simple-linux: Linux](https://tutanota.com/#download)
        - [:octicons-browser-16: Web](https://mail.tutanota.com/)

Tutanota ondersteunt het [IMAP protocol](https://tutanota.com/faq/#imap) em het gebruik van e-mailclients van derden niet[](email-clients.md), en je zult ook niet in staat zijn om [externe e-mailaccounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) toe te voegen aan de Tutanota app. Beide [E-mail import](https://github.com/tutao/tutanota/issues/630) of [submappen](https://github.com/tutao/tutanota/issues/927) worden momenteel ondersteund, hoewel dit binnenkort [zal worden gewijzigd](https://tutanota.com/blog/posts/kickoff-import). E-mails kunnen [individueel of per bulk selectie](https://tutanota.com/howto#generalMail) per map worden geëxporteerd, wat onhandig kan zijn als je veel mappen hebt.

#### :material-check:{ .pg-green } Aangepaste domeinen en aliassen

Betaalde Tutanota accounts kunnen tot 5 [aliassen gebruiken](https://tutanota.com/faq#alias) en [aangepaste domeinen](https://tutanota.com/faq#custom-domain). Tutanota staat geen [subadressering (plus adressen)](https://tutanota.com/faq#plus)toe, maar je kunt een [catch-all](https://tutanota.com/howto#settings-global) gebruiken met een aangepast domein.

#### :material-information-outline:{ .pg-blue } Privé betaalmethodes

Tutanota accepteert alleen rechtstreeks creditcards en PayPal, maar Bitcoin en Monero kunnen worden gebruikt om cadeaubonnen te kopen via hun [partnerschap](https://tutanota.com/faq/#cryptocurrency) met Proxystore.

#### :material-check:{ .pg-green } Accountbeveiliging

Tutanota ondersteunt [twee-factor authenticatie](https://tutanota.com/faq#2fa) met TOTP of U2F.

#### :material-check:{ .pg-green } Gegevensbeveiliging

Tutanota heeft [zero access encryptie bij rust](https://tutanota.com/faq#what-encrypted) voor jouw e-mails, [adresboek contacten](https://tutanota.com/faq#encrypted-address-book), en [kalenders](https://tutanota.com/faq#calendar). Dit betekent dat de berichten en andere gegevens die in jouw account zijn opgeslagen, alleen door je kunnen worden gelezen.

#### :material-information-outline:{ .pg-blue } Email Encryptie

Tutanota [maakt geen gebruik van OpenPGP](https://www.tutanota.com/faq/#pgp). Tutanota-accounts kunnen alleen versleutelde e-mails ontvangen van niet-Tutanota-e-mailaccounts wanneer ze worden verzonden via een [tijdelijke Tutanota-postvak](https://www.tutanota.com/howto/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Beëindiging van account

Tutanota zal [inactieve gratis accounts](https://tutanota.com/faq#inactive-accounts) verwijderen na zes maanden. Je kunt een gedeactiveerd gratis account opnieuw gebruiken als je betaalt.

#### :material-information-outline:{ .pg-blue } extra functionaliteit

Tutanota biedt de zakelijke versie van [Tutanota aan non-profitorganisaties](https://tutanota.com/blog/posts/secure-email-for-non-profit) gratis of met een fikse korting.

Tutanota heeft ook een zakelijke functie genaamd [Secure Connect](https://tutanota.com/secure-connect/). Dit zorgt ervoor dat het klantcontact met het bedrijf gebruik maakt van E2EE. De functie kost €240/j.

Tutanota biedt geen digitale erfenis functie.

## E-mail aliasing diensten

Met een e-mail aliasing dienst kun je gemakkelijk een nieuw e-mailadres genereren voor elke website waarvoor je je aanmeldt. De e-mailaliassen die je aanmaakt worden dan doorgestuurd naar een e-mailadres vanjouw keuze, waardoor zowel jouw "hoofd"-e-mailadres als de identiteit van jouw e-mailprovider wordt verborgen. Echte e-mailaliasing is beter dan de door veel providers gebruikte en ondersteunde plus-adressering, waarmee je aliassen kunt maken als jouwnaam+[anythinghere]@voorbeeld.com, omdat websites, adverteerders en traceringsnetwerken triviaal alles na het +-teken kunnen verwijderen om jouw echte e-mailadres te ontdekken.

<div class="grid cards" markdown>

- ![AnonAddy logo](assets/img/email/anonaddy.svg#only-light){ .twemoji }![AnonAddy logo](assets/img/email/anonaddy-dark.svg#only-dark){ .twemoji } [AnonAddy](email.md#anonaddy)
- ![SimpleLogin logo](assets/img/email/simplelogin.svg){ .twemoji } [SimpleLogin](email.md#simplelogin)

</div>

E-mailaliasing kan fungeren als een waarborg voor het geval jouw e-mailprovider ooit ophoudt te werken. In dat scenario kun je jouw aliassen gemakkelijk omleiden naar een nieuw e-mailadres. Op zijn beurt stelt je echter vertrouwen in de aliasingdienst om te blijven functioneren.

Het gebruik van een speciale e-mail aliasing dienst heeft ook een aantal voordelen ten opzichte van een catch-all alias op een aangepast domein:

- Aliassen kunnen individueel worden in- en uitgeschakeld wanneer je ze nodig hebt, zodat websites je niet willekeurig e-mailen.
- Antwoorden worden verzonden vanaf het aliasadres, waardoor jouw echte e-mailadres wordt afgeschermd.

Ze hebben ook een aantal voordelen ten opzichte van "tijdelijke e-mail" diensten:

- Aliassen zijn permanent en kunnen weer worden ingeschakeld als je iets moet ontvangen zoals een wachtwoord-reset.
- E-mails worden naar jouw vertrouwde mailbox gestuurd in plaats van opgeslagen door de alias provider.
- Tijdelijke e-maildiensten hebben doorgaans openbare mailboxen die voor iedereen die het adres kent toegankelijk zijn, aliassen zijn privé.

Onze aanbevelingen voor e-mailaliassen zijn providers waarmee je aliassen kunt aanmaken op domeinen die zij beheren, en op jouw eigen aangepaste domein(en) voor een bescheiden jaarlijks bedrag. Ze kunnen ook zelf worden gehost als je maximale controle wilt. Het gebruik van een eigen domein kan echter ook nadelen hebben voor de privacy: Als je de enige persoon bent die ouw aangepaste domein gebruikt, kunnen jouw acties op verschillende websites gemakkelijk worden getraceerd door simpelweg naar de domeinnaam in het e-mailadres te kijken en alles voor het at (@) teken te negeren.

Het gebruik van een aliasingdienst vereist dat je zowel jouw e-mailprovider als jouw aliasingprovider vertrouwt met jouw onversleutelde berichten. Sommige aanbieders verzachten dit enigszins met automatische PGP-versleuteling, die het aantal partijen dat je moet vertrouwen terugbrengt van twee naar één door inkomende e-mails te versleutelen voordat ze bij je uiteindelijke postbusaanbieder worden afgeleverd.

### AnonAddy

!!! recommendation

    ![AnonAddy logo](assets/img/email/anonaddy.svg#only-light){ align=right }
    ![AnonAddy logo](assets/img/email/anonaddy-dark.svg#only-dark){ align=right }
    
    **AnonAddy** laat je gratis 20 domein aliassen aanmaken op een gedeeld domein, of onbeperkt "standaard" aliassen die minder anoniem zijn.
    
    [:octicons-home-16: Homepage](https://anonaddy.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://anonaddy.com/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://app.anonaddy.com/docs/){ .card-link title=Documentatie}
    [:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Broncode" }
    [:octicons-heart-16:](https://anonaddy.com/donate/){ .card-link title=Bijdragen }
    
    ??? downloads "Downloaden"
    
        - [:simple-android: Android](https://anonaddy.com/faq/#is-there-an-android-app)
        - [:material-apple-ios: iOS](https://anonaddy.com/faq/#is-there-an-ios-app)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/en-GB/firefox/addon/anonaddy/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/anonaddy-anonymous-email/iadbdpnoknmbdeolbapdackdcogdmjpe)

Het aantal gedeelde aliassen (die eindigen op een gedeeld domein zoals @anonaddy.me) dat je kunt aanmaken is beperkt tot 20 op het gratis plan van AnonAddy en 50 op hun $12/maand plan. Je kunt onbeperkt standaard aliassen aanmaken (die eindigen op een domein zoals @[username].anonaddy.com of een aangepast domein op betaalde plannen), echter, zoals eerder vermeld, kan dit nadelig zijn voor de privacy omdat mensen uw standaard aliassen triviaal aan elkaar kunnen linken op basis van de domeinnaam alleen. Onbeperkte gedeelde aliassen zijn beschikbaar voor $36/jaar.

Opmerkelijke gratis functies:

- [x] 20 Gedeelde Aliassen
- [x] Onbeperkt aantal standaard aliassen
- [ ] Geen uitgaande antwoorden
- [x] 2 Ontvanger Mailboxen
- [x] Automatische PGP-versleuteling

### SimpleLogin

!!! recommendation

    ![Simplelogin logo](assets/img/email/simplelogin.svg){ align=right }
    
    **SimpleLogin** is een gratis dienst die e-mailaliassen op verschillende gedeelde domeinnamen biedt, en optioneel betaalde functies zoals onbeperkte aliassen en aangepaste domeinen.
    
    [:octicons-home-16: Homepage](https://simplelogin.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://simplelogin.io/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://simplelogin.io/docs/){ .card-link title=Documentatie}
    [:octicons-code-16:](https://github.com/simple-login){ .card-link title="Broncode" }
    
    ??? downloads "Downloaden"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
        - [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/en-US/firefox/addon/simplelogin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
        - [:simple-safari: Safari](https://apps.apple.com/app/id1494051017)

SimpleLogin werd [overgenomen door Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) met ingang van 8 april 2022. Als je Proton Mail gebruikt voor uw primaire mailbox, is SimpleLogin een goede keuze. Aangezien beide producten nu eigendom zijn van hetzelfde bedrijf, hoeft je nog maar op één entiteit te vertrouwen. Wij verwachten ook dat SimpleLogin in de toekomst nauwer zal worden geïntegreerd met het aanbod van Proton. SimpleLogin blijft forwarding naar elke e-mailprovider van jouw keuze ondersteunen. Securitum [heeft begin 2022 een audit uitgevoerd op](https://simplelogin.io/blog/security-audit/) SimpleLogin en alle problemen [zijn aangepakt](https://simplelogin.io/audit2022/web.pdf).

Je kunt jouw SimpleLogin account in de instellingen koppelen aan jouw Proton account. Als je Proton Unlimited, Business of Visionary Plan hebt, heb je SimpleLogin Premium gratis.

Opmerkelijke gratis functies:

- [x] 10 Gedeelde Aliassen
- [x] Onbeperkt antwoorden
- [x] 1 Ontvanger Mailbox

## Onze criteria

Gevorderde systeembeheerders kunnen overwegen hun eigen e-mailserver op te zetten. Mailservers vereisen aandacht en voortdurend onderhoud om de zaken veilig te houden en de mailbezorging betrouwbaar.

### Gecombineerde softwareoplossingen

!!! recommendation

    ![Mailcow logo](assets/img/email/mailcow.svg){ align=right }
    
    **Mailcow** is een meer geavanceerde mailserver, perfect voor mensen met wat meer Linux ervaring. Het heeft alles wat je nodig hebt in een Docker container: Een mailserver met DKIM-ondersteuning, antivirus- en spammonitoring, webmail en ActiveSync met SOGo, en webgebaseerd beheer met 2FA-ondersteuning.
    
    [:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailcow.github.io/mailcow-dockerized-docs/){ .card-link title=Documentatie}
    [:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Broncode" }
    [:octicons-heart-16:](https://www.servercow.de/mailcow?lang=en#sal){ .card-link title=Bijdrage leveren }

!!! recommendation

    ![Mail-in-a-Box logo](assets/img/email/mail-in-a-box.svg){ align=right }
    
    **Mail-in-a-Box** is een geautomatiseerd setup script voor het implementeren van een mailserver op Ubuntu. Het doel ervan is om het voor mensen gemakkelijker te maken om hun eigen mailserver op te zetten.
    
    [:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentatie}
    [:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Broncode" } }

Voor een meer handmatige aanpak hebben we deze twee artikelen uitgekozen:

- [Een mailserver opzetten met OpenSMTPD, Dovecot en Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd/) (2019)
- [Hoe run je je eigen mailserver](https://www.c0ffee.net/blog/mail-server-guide/) (augustus 2017)

## Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaard criteria](about/criteria.md) hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je zich vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat het de juiste keuze voor je is.

### Technologie

Wij beschouwen deze kenmerken als belangrijk om een veilige en optimale dienst te kunnen verlenen. Je zou moeten nagaan of de provider de functies heeft die je nodig hebt.

**Minimum om in aanmerking te komen:**

- Versleutelt e-mail accountgegevens in rust met zero-access encryptie.
- Exportmogelijkheid als [Mbox](https://en.wikipedia.org/wiki/Mbox) of individuele .eml met [RFC5322](https://datatracker.ietf.org/doc/rfc5322/) standaard.
- Sta gebruikers toe hun eigen [domeinnaam te gebruiken](https://en.wikipedia.org/wiki/Domain_name). Aangepaste domeinnamen zijn belangrijk voor gebruikers omdat ze zo hun agentschap van de dienst kunnen behouden, mocht het slecht aflopen of overgenomen worden door een ander bedrijf dat privacy niet hoog in het vaandel heeft staan.
- Werkt op eigen infrastructuur, d.w.z. niet gebaseerd op e-mail service providers van derden.

**Beste geval:**

- Versleutelt alle accountgegevens (Contacten, Agenda's, etc) in rust met zero-access encryptie.
- Geïntegreerde webmail E2EE/PGP-codering voor het gemak.
- Ondersteuning voor [WKD](https://wiki.gnupg.org/WKD) om een verbeterde ontdekking van publieke OpenPGP sleutels via HTTP mogelijk te maken. GnuPG-gebruikers kunnen een sleutel krijgen door te typen: `gpg --locate-key example_user@example.com`
- Ondersteuning voor een tijdelijke mailbox voor externe gebruikers. Dit is handig wanneer je een versleutelde e-mail wilt verzenden, zonder een echte kopie naar jouw ontvanger te sturen. Deze e-mails hebben meestal een beperkte levensduur en worden daarna automatisch verwijderd. Zij vereisen ook niet dat de ontvanger cryptografie configureert zoals OpenPGP.
- Beschikbaarheid van de diensten van de e-mailprovider via een [onion service](https://en.wikipedia.org/wiki/.onion).
- [Ondersteuning voor subadressering](https://en.wikipedia.org/wiki/Email_address#Subaddressing).
- Catch-all of alias functionaliteit voor diegenen die hun eigen domeinen bezitten.
- Gebruik van standaard e-mail toegangsprotocollen zoals IMAP, SMTP of [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standaard toegangsprotocollen zorgen ervoor dat klanten al hun e-mail gemakkelijk kunnen downloaden, mochten zij naar een andere provider willen overstappen.

### Privacy

Wij geven er de voorkeur aan dat de door ons aanbevolen aanbieders zo weinig mogelijk gegevens verzamelen.

**Minimum om in aanmerking te komen:**

- Beschermt het IP adres van de afzender. Filter het uit de weergave in het `Received` header veld.
- Vereisen geen persoonlijk identificeerbare informatie (PII) naast een gebruikersnaam en een wachtwoord.
- Privacybeleid dat voldoet aan de vereisten van de GDPR.
- Mag niet in de VS worden gehost wegens [ECPA](https://en.wikipedia.org/wiki/Electronic_Communications_Privacy_Act#Criticism) die [nog moet worden hervormd](https://epic.org/ecpa/).

**Beste geval:**

- Accepteert [anonieme betalingsopties](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), contant geld, cadeaukaarten, etc.)

### Veiligheid

Email servers verwerken veel zeer gevoelige gegevens. We verwachten dat providers de beste praktijken in de branche zullen toepassen om hun gebruikers te beschermen.

**Minimum om in aanmerking te komen:**

- Bescherming van webmail met 2FA, zoals TOTP.
- Zero access encryptie, bouwt voort op encryptie in rust. De provider heeft geen decryptiesleutels voor de gegevens die ze hebben. Dit voorkomt dat een malafide werknemer gegevens lekt waartoe hij toegang heeft, of dat een tegenstander op afstand gegevens vrijgeeft die hij heeft gestolen door ongeoorloofde toegang tot de server te verkrijgen.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) ondersteuning.
- Geen [TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS) fouten/kwetsbaarheden bij profilering door tools zoals [Hardenize](https://www.hardenize.com), [testssl.sh](https://testssl.sh) of [Qualys SSL Labs](https://www.ssllabs.com/ssltest), dit omvat certificaatgerelateerde fouten, slechte of zwakke ciphersuites, zwakke DH-parameters zoals die welke hebben geleid tot [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Een geldig [MTA-STS](https://tools.ietf.org/html/rfc8461) en [TLS-RPT](https://tools.ietf.org/html/rfc8460) beleid.
- Geldig [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) records.
- Geldige [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) en [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) records.
- Geldige [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) en [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) records.
- Zorg voor een correct [DMARC](https://en.wikipedia.org/wiki/DMARC) record en beleid of gebruik [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) voor verificatie. Als DMARC-authenticatie wordt gebruikt, moet het beleid worden ingesteld op `reject` of `quarantine`.
- Een server suite voorkeur van TLS 1.2 of hoger en een plan voor [RFC8996](https://datatracker.ietf.org/doc/rfc8996/).
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) indiening, ervan uitgaande dat SMTP wordt gebruikt.
- Beveiligingsnormen voor websites, zoals:
    - [HTTP Strict Transport Security](https://nl.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subbron Integriteit](https://en.wikipedia.org/wiki/Subresource_Integrity) als dingen van externe domeinen worden geladen.
- Moet het bekijken van [Message headers](https://en.wikipedia.org/wiki/Email#Message_header)ondersteunen, aangezien dit een cruciale forensische functie is om te bepalen of een e-mail een phishing-poging is.

**Beste geval:**

- Ondersteuning voor hardware-authenticatie, d.w.z. U2F en [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn). U2F en WebAuthn zijn veiliger omdat zij een privésleutel gebruiken die is opgeslagen op een hardware-apparaat aan de clientzijde om mensen te authenticeren, in tegenstelling tot een gedeeld geheim dat is opgeslagen op de webserver en aan de clientzijde wanneer TOTP wordt gebruikt. Bovendien zijn U2F en WebAuthn beter bestand tegen phishing omdat hun authenticatierespons gebaseerd is op de geauthenticeerde [domeinnaam](https://en.wikipedia.org/wiki/Domain_name).
- [DNS Certificatie Autoriteit Autorisatie (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in aanvulling op DANE ondersteuning.
- Implementatie van [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), dit is nuttig voor mensen die posten naar mailinglijsten [RFC8617](https://tools.ietf.org/html/rfc8617).
- Programma's voor bug-bounty's en/of een gecoördineerd proces voor de openbaarmaking van kwetsbaarheden.
- Beveiligingsnormen voor websites, zoals:
    - [Inhoud beveiligingsbeleid (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163/)

### Vertrouwen

Je zou je financiën niet toevertrouwen aan iemand met een valse identiteit, dus waarom zou je hen je e-mail toevertrouwen? Wij eisen van onze aanbevolen aanbieders dat zij hun eigendom of leiderschap openbaar maken. Wij zouden ook graag zien dat regelmatig verslag wordt uitgebracht over de transparantie, met name wat betreft de wijze waarop verzoeken van de overheid worden behandeld.

**Minimum om in aanmerking te komen:**

- Publiekelijk leiderschap of eigendom.

**Beste geval:**

- Publieksgericht leiderschap.
- Frequente transparantieverslagen.

### Marketing

Bij de e-mail providers die we aanbevelen zien we graag verantwoorde marketing.

**Minimum om in aanmerking te komen:**

- Moet zelf analytics hosten (geen Google Analytics, Adobe Analytics, etc). De site van de aanbieder moet ook voldoen aan [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) voor degenen die zich willen afmelden.

Mag geen marketing hebben die onverantwoord is:

- Claims van "onbreekbare encryptie." Encryptie moet worden gebruikt met de bedoeling dat zij in de toekomst niet meer geheim is wanneer de technologie bestaat om haar te kraken.
- Garanties van 100% bescherming van de anonimiteit. Wanneer iemand beweert dat iets 100% is, betekent dit dat er geen zekerheid is voor mislukking. We weten dat mensen zichzelf vrij gemakkelijk kunnen deanonimiseren op een aantal manieren, bv.:

- Hergebruik van persoonlijke informatie, bijv. (e-mailaccounts, unieke pseudoniemen, enz.) waartoe zij toegang hadden zonder anonimiteitssoftware (Tor, VPN, enz.)
- [Browser vingerafdrukken](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Beste geval:**

- Duidelijke en gemakkelijk te lezen documentatie. Dit omvat zaken als het instellen van 2FA, e-mailclients, OpenPGP, enz.

### Extra functionaliteit

Hoewel het geen strikte vereisten zijn, zijn er nog enkele andere factoren met betrekking tot gemak of privacy die wij in aanmerking hebben genomen bij het bepalen van de aan te bevelen providers.
