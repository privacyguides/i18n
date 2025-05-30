---
meta_title: "How to Create Internet Accounts Privately - Privacy Guides"
title: "Account Creation"
icon: 'material/account-plus'
description: Creating accounts online is practically an internet necessity, take these steps to make sure you stay private.
---

Vaak melden mensen zich aan voor diensten zonder na te denken. Maybe it's a streaming service to watch that new show everyone's talking about, or an account that gives you a discount for your favorite fast food place. Wat het geval ook is, je moet nu en later rekening houden met de implicaties voor jouw gegevens.

Aan elke nieuwe dienst die je gebruikt, zijn risico's verbonden. Datalekken; onthulling van klanteninformatie aan derden; malafide werknemers die toegang krijgen tot gegevens; het zijn allemaal mogelijkheden die moeten worden overwogen wanneer je jouw informatie verstrekt. Je moet er zeker van zijn dat je de service kunt vertrouwen, daarom raden we niet aan om waardevolle gegevens op te slaan over iets anders dan de meest volwassen en stressgeteste producten. Dat betekent meestal diensten die end-to-end encryptie leveren en een cryptografische audit hebben ondergaan. Een audit vergroot de zekerheid dat het product is ontworpen zonder opvallende beveiligingsproblemen die zijn veroorzaakt door een onervaren ontwikkelaar.

Bij sommige diensten kan het ook moeilijk zijn om de accounts te verwijderen. Soms kan [gegevens overschrijven](account-deletion.md#overwriting-account-information) die aan een account zijn gekoppeld, maar in andere gevallen bewaart de dienst een hele geschiedenis van wijzigingen in de account.

## Servicevoorwaarden en Privacybeleid

De ToS zijn de regels waarmee je akkoord gaat wanneer je de dienst gebruikt. Bij grotere diensten worden deze regels vaak afgedwongen door geautomatiseerde systemen. Soms kunnen deze geautomatiseerde systemen fouten maken. For example, you may be banned or locked out of your account on some services for using a VPN or VoIP number. Een beroep doen op een dergelijke verbanning is vaak moeilijk en omvat ook een geautomatiseerd proces, wat niet altijd succesvol is. Dit is een van de redenen waarom wij bijvoorbeeld niet aanraden Gmail als e-mail te gebruiken. E-mail is cruciaal voor de toegang tot andere diensten waarvoor je zich misschien hebt aangemeld.

The Privacy Policy is how the service says they will use your data, and it is worth reading so that you understand how your data will be used. Een bedrijf of organisatie is mogelijk niet wettelijk verplicht om alles wat in het beleid staat te volgen (het hangt af van de jurisdictie). We raden je aan om een idee te hebben van wat je lokale wetten zijn en wat ze een provider toestaan om te verzamelen.

Wij raden je aan te zoeken naar bepaalde termen zoals "gegevensverzameling", "gegevensanalyse", "cookies", "advertenties" of "diensten van derden". Sometimes you will be able to opt out from data collection or from sharing your data, but it is best to choose a service that respects your privacy from the start.

Vergeet niet dat je ook jouw vertrouwen stelt in het bedrijf of de organisatie en dat zij hun eigen privacybeleid zullen naleven.

## Authenticatie methodes

Er zijn meestal meerdere manieren om een account aan te maken, elk met hun eigen voor- en nadelen.

### E-mailadres en wachtwoord

De meest gebruikelijke manier om een nieuwe account aan te maken is met een e-mailadres en wachtwoord. Wanneer je deze methode gebruikt, moet je een wachtwoord manager gebruiken en de best practices [volgen](passwords-overview.md) met betrekking tot wachtwoorden.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Je kunt jouw wachtwoord manager ook gebruiken om andere verificatiemethoden te organiseren! Voeg gewoon het nieuwe item toe en vul de juiste velden in, u kunt notities toevoegen voor zaken als beveiligingsvragen of een back-up sleutel.

</div>

Je bent verantwoordelijk voor het beheer van jouw inloggegevens. Voor extra beveiliging kunt je  [MFA](multi-factor-authentication.md) instellen op jouw accounts.

[Lijst van aanbevolen wachtwoordbeheerders](../passwords.md ""){.md-button}

#### E-mail aliassen

Als je jouw echte e-mailadres niet aan een dienst wilt geven, kunt je een alias gebruiken. We describe them in more detail on our email services recommendation page. Met alias diensten kunt je nieuwe e-mailadressen aanmaken die alle e-mails doorsturen naar jouw hoofdadres. This can help prevent tracking across services and help you manage the marketing emails that sometimes come with the sign-up process. Die kunnen automatisch worden gefilterd op basis van de alias waarnaar ze worden gestuurd.

Als een dienst wordt gehackt, kunt je phishing- of spam-e-mails ontvangen op het adres waarmee je je hebt aangemeld. Het gebruik van unieke aliassen voor elke service kan helpen bij het identificeren van precies welke service is gehackt.

[Aanbevolen diensten voor e-mailaliasing](../email-aliasing.md ""){.md-button}

### Meld je aan met... OAuth

[Open Authorization (OAuth)](https://en.wikipedia.org/wiki/OAuth) is an authentication protocol that allows you to register for a service without sharing much information with the service provider, if any, by using an existing account you have with another service instead. Wanneer je iets ziet in de trant van "Aanmelden met *providernaam*" op een registratieformulier, dan betreft dat meestal OAuth.

Wanneer je met OAuth inlogt, wordt een inlogpagina geopend met de aanbieder die je kiest, en jouw bestaande account en nieuwe account zullen worden verbonden. Jouw wachtwoord wordt niet gedeeld, maar sommige basisinformatie wel (je kunt deze bekijken tijdens het inlogverzoek). Dit proces is nodig elke keer dat je wilt inloggen op hetzelfde account.

De belangrijkste voordelen zijn:

- **Security**: You don't have to trust the security practices of the service you're logging into when it comes to storing your login credentials because they are stored with the external OAuth provider. Common OAuth providers like Apple and Google typically follow the best security practices, continuously audit their authentication systems, and don't store credentials inappropriately (such as in plain text).
- **Ease-of-use**: Multiple accounts are managed by a single login.

Maar er zijn ook nadelen:

- **Privacy**: The OAuth provider you log in with will know the services you use.
- **Centralization**: If the account you use for OAuth is compromised, or you aren't able to log in to it, all other accounts connected to it are affected.

OAuth can be especially useful in those situations where you could benefit from deeper integration between services. Onze aanbeveling is om OAuth alleen te gebruiken waar je het nodig hebt, en altijd de hoofdaccount te beschermen met [MFA](multi-factor-authentication.md).

All the services that use OAuth will be as secure as your underlying OAuth provider's account. Als je bijvoorbeeld een account wilt beveiligen met een hardwaresleutel, maar die dienst ondersteunt geen hardwaresleutels, dan kun je jouw OAuth account beveiligen met een hardwaresleutel en nu hebt je in wezen hardware-MFA op al jouw accounts. Het is de moeite waard om op te merken dat zwakke authenticatie op jouw OAuth provider-account betekent dat elke account gekoppeld aan die login ook zwak zal zijn.

There is an additional danger when using *Sign in with Google*, *Facebook*, or another service, which is that typically the OAuth process allows for *bidirectional* data sharing. For example, logging in to a forum with your Twitter account could grant that forum access to do things on your Twitter account such as post, read your messages, or access other personal data. OAuth providers will typically present you with a list of things you are granting the external service access to, and you should always ensure that you read through that list and don't inadvertently grant the external service access to anything it doesn't require.

Malicious applications, particularly on mobile devices where the application has access to the WebView session used for logging in to the OAuth provider, can also abuse this process by hijacking your session with the OAuth provider and gaining access to your OAuth account through those means. Using the *Sign in with* option with any provider should usually be considered a matter of convenience that you only use with services you trust to not be actively malicious.

### Telefoonnummer

We raden je aan services te vermijden waarvoor een telefoonnummer nodig is om je aan te melden. A phone number can identify you across multiple services and depending on data sharing agreements this will make your usage easier to track, particularly if one of those services is breached as the phone number is often **not** encrypted.

Vermijd het geven van jouw echte telefoonnummer als je kunt. Some services will allow the use of VoIP numbers, however these often trigger fraud detection systems, causing an account to be locked down, so we don't recommend that for important accounts.

In veel gevallen moet je een nummer opgeven waarvan je smsjes of telefoontjes kunt ontvangen, vooral wanneer je internationaal winkelt, voor het geval er een probleem is met jouw bestelling bij de grenscontrole. Het is gebruikelijk dat services je nummer gebruiken als verificatiemethode; laat je niet buitensluiten van een belangrijk account omdat je slim wilt zijn en een nepnummer wilt geven!

### Gebruikersnaam en wachtwoord

Bij sommige diensten kunt je je zonder e-mailadres registreren en hoeft je alleen een gebruikersnaam en wachtwoord in te stellen. Deze diensten kunnen meer anonimiteit bieden in combinatie met een VPN of Tor. Houd er rekening mee dat er voor deze accounts hoogstwaarschijnlijk **geen manier is om jouw account** te herstellen als je jouw gebruikersnaam of wachtwoord vergeet.
