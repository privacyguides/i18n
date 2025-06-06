---
title: "Multifactor Authentication"
icon: 'material/two-factor-authentication'
description: MFA is een cruciaal beveiligingsmechanisme voor de beveiliging van jouw online accounts, maar sommige methoden zijn sterker dan andere.
---

**Multifactor Authentication** (**MFA**) is a security mechanism that requires additional steps beyond entering your username (or email) and password. De meest gebruikelijke methode zijn codes met tijdsbeperking die je via sms of een app kunt ontvangen.

Als een hacker (of tegenstander) jouw wachtwoord weet te achterhalen, krijgt hij toegang tot de account waar dat wachtwoord bij hoort. Een account met MFA dwingt de hacker om zowel het wachtwoord te hebben (iets wat je *weet*) als een apparaat dat je bezit (iets wat je *hebt*), zoals je telefoon.

MFA-methoden variëren in beveiliging, maar zijn gebaseerd op de vooronderstelling dat hoe moeilijker het voor een aanvaller is om toegang te krijgen tot uw MFA-methode, hoe beter. Voorbeelden van MFA-methoden (van zwakste naar sterkste) zijn sms, e-mailcodes, app-pushmeldingen, TOTP, Yubico OTP en FIDO.

## Vergelijking van MFB-methoden

### SMS of e-mail MFA

Het ontvangen van OTP-codes via SMS of e-mail is een van de zwakkere manieren om jouw accounts met MFA te beveiligen. </a> Het verkrijgen van een code via e-mail of sms doet afbreuk aan het idee van "iets wat je *hebt*", omdat er verschillende manieren zijn waarop een hacker jouw telefoonnummer

kan overnemen of toegang tot jouw e-mail kan krijgen zonder fysieke toegang te hebben tot een van jouw apparaten. Als een onbevoegd persoon toegang zou krijgen tot jouw e-mail, zou hij die toegang kunnen gebruiken om zowel jouw wachtwoord te resetten als de verificatiecode te ontvangen, waardoor hij volledige toegang tot jouw account zou krijgen.</p> 



### Push-meldingen

Push notification MFA neemt de vorm aan van een bericht dat naar een app op jouw telefoon wordt gestuurd en waarin je wordt gevraagd nieuwe accountlogins te bevestigen. Deze methode is veel beter dan SMS of e-mail, omdat een aanvaller deze pushmeldingen meestal niet kan krijgen zonder een al aangemeld apparaat, wat betekent dat hij eerst een van jouw andere apparaten zou moeten compromitteren.

We maken allemaal fouten, en het risico bestaat dat u de inlogpoging per ongeluk aanvaardt. Inlogautorisaties via push-notificatie worden doorgaans verzonden naar *alle* jouw apparaten in een keer, waardoor de beschikbaarheid van de MFA-code wordt uitgebreid als je veel apparaten hebt.

De beveiliging van push notification MFA is afhankelijk van zowel de kwaliteit van de app, de servercomponent als het vertrouwen van de ontwikkelaar die de app maakt. Als je een app installeert, kan het ook zijn dat je moet instemmen met invasieve privileges die toegang verlenen tot andere gegevens op jouw apparaat. . en individuele app vereist ook dat je voor elke dienst een specifieke app hebt, die misschien geen wachtwoord vereist om te openen, in tegenstelling tot een goede TOTP generator app.



### Time-based One-time Password (TOTP)

TOTP is een van de meest voorkomende vormen van MFB. Wanneer je TOTP instelt, moet je over het algemeen een [QR-code](https://en.wikipedia.org/wiki/QR_code) scannen die een "[gedeeld geheim](https://en.wikipedia.org/wiki/Shared_secret)" tot stand brengt met de dienst die je van plan bent te gebruiken. The shared secret is secured inside the authenticator app's data, and is sometimes protected by a password.

De in de tijd beperkte code wordt dan afgeleid van het gedeelde geheim en de huidige tijd. Aangezien de code slechts korte tijd geldig is, kan een adversair zonder toegang tot het gedeelde geheim geen nieuwe codes genereren.

Als je een hardware beveiligingssleutel hebt met TOTP ondersteuning (zoals een YubiKey met [Yubico Authenticator](https://yubico.com/products/yubico-authenticator)), raden we je aan om je "gedeelde geheimen" op te slaan op de hardware. Hardware zoals de YubiKey werd ontwikkeld met de bedoeling het "gedeelde geheim" moeilijk te ontfutselen en te kopiëren te maken. Een YubiKey is ook niet verbonden met het internet, in tegenstelling tot een telefoon met een TOTP-app.

In tegenstelling tot [WebAuthn](#fido-fast-identity-online)biedt TOTP geen bescherming tegen [phishing](https://en.wikipedia.org/wiki/Phishing) of hergebruikaanvallen. Als een tegenstander een geldige code van je krijgt, mag hij die zo vaak gebruiken als hij wil totdat de code is verlopen (over het algemeen 60 seconden.

Een tegenstander kan een website opzetten om een officiële dienst te imiteren in een poging om je te verleiden jouw gebruikersnaam, wachtwoord en huidige TOTP-code te geven. Als de tegenstander vervolgens deze vastgelegde gegevens gebruikt, kan hij op de echte dienst inloggen en de account kapen.

Hoewel niet perfect, is TOTP veilig genoeg voor de meeste mensen, en wanneer [hardware beveiligingssleutels](../security-keys.md) niet worden ondersteund zijn [authenticator apps](../multi-factor-authentication.md) nog steeds een goede optie.



### Hardware beveiligingssleutels

De YubiKey slaat gegevens op een manipulatiebestendige solid-state chip die [onmogelijk is om toegang te krijgen tot](https://security.stackexchange.com/a/245772) niet-destructief zonder een duur proces en een forensisch laboratorium.

Deze sleutels zijn over het algemeen multifunctioneel en bieden een aantal methoden om zich te authenticeren. Hieronder staan de meest voorkomende.



#### Yubico OTP

Yubico OTP is een authenticatieprotocol dat typisch wordt geïmplementeerd in hardware beveiligingssleutels. Wanneer je besluit Yubico OTP te gebruiken, zal de sleutel een publiek ID, privaat ID, en een Geheime Sleutel genereren die dan geupload wordt naar de Yubico OTP server.

Wanneer je inlogt op een website, hoeft je alleen maar de beveiligingssleutel fysiek aan te raken. De beveiligingssleutel zal een toetsenbord emuleren en een eenmalig wachtwoord in het wachtwoordveld afdrukken.

De dienst zal dan het eenmalige wachtwoord doorsturen naar de Yubico OTP server voor validatie. Zowel op de sleutel als op de validatieserver van Yubico wordt een teller opgehoogd. De OTP kan slechts één keer worden gebruikt, en wanneer een authenticatie met succes plaatsvindt, wordt de teller verhoogd, waardoor hergebruik van de OTP wordt voorkomen. Yubico geeft een [gedetailleerd document](https://developers.yubico.com/OTP/OTPs_Explained.html) over het proces.

<figure markdown>
  Yubico OTP](../assets/img/multi-factor-authentication/yubico-otp.png)
</figure>

Er zijn enkele voor- en nadelen aan het gebruik van Yubico OTP in vergelijking met TOTP.

De Yubico validatieserver is een cloud-gebaseerde dienst, en je vertrouwt op Yubico dat zij jouw gegevens veilig opslaan en je niet profileren. De publieke ID die bij Yubico OTP hoort, wordt op elke website hergebruikt en kan voor derden een extra mogelijkheid zijn om je te profileren. Net als TOTP biedt Yubico OTP geen weerstand tegen phishing.

Als jouw dreigingsmodel vereist dat je verschillende identiteiten op verschillende websites heeft, **gebruik dan geen** Yubico OTP met dezelfde hardware beveiligingssleutel op die websites, aangezien de publieke ID uniek is voor elke beveiligingssleutel.



#### FIDO (Fast IDentity Online)

[FIDO](https://en.wikipedia.org/wiki/FIDO_Alliance) omvat een aantal normen, eerst was er U2F en later [FIDO2](https://en.wikipedia.org/wiki/FIDO2_Project) die de webnorm [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn)omvat.

U2F en FIDO2 verwijzen naar het [Client to Authenticator Protocol](https://en.wikipedia.org/wiki/Client_to_Authenticator_Protocol), dat het protocol is tussen de beveiligingssleutel en de computer, zoals een laptop of telefoon. Het is een aanvulling op WebAuthn, de component die wordt gebruikt om je te authenticeren bij de website (de "Betrouwbare Partij") waarop je probeert in te loggen.

WebAuthn is de meest veilige en private vorm van tweede factor authenticatie. De verificatie-ervaring is vergelijkbaar met Yubico OTP, maar de sleutel drukt geen eenmalig wachtwoord af en valideert niet met een server van een derde partij. In plaats daarvan gebruikt het [openbare sleutel cryptografie](https://en.wikipedia.org/wiki/Public-key_cryptography) voor authenticatie.

<figure markdown>
  ![FIDO](../assets/img/multi-factor-authentication/fido.png)
</figure>

Wanneer je een account aanmaakt, wordt de openbare sleutel naar de dienst gestuurd, en wanneer je inlogt, zal de dienst je vragen bepaalde gegevens te "ondertekenen" met jouw privé-sleutel. Het voordeel hiervan is dat er nooit wachtwoordgegevens door de dienst worden opgeslagen, zodat er voor een adverteerder niets te stelen valt.

This presentation discusses the history of password authentication, the pitfalls (such as password reuse), and the standards for FIDO2 and [WebAuthn](https://webauthn.guide):

- [How FIDO2 and WebAuthn Stop Account Takeovers](https://youtu.be/aMo4ZlWznao) <small>(YouTube)</small>

FIDO2 en WebAuthn hebben superieure beveiligings- en privacy-eigenschappen in vergelijking met andere MFA-methoden.

Typically, for web services it is used with WebAuthn which is a part of the [W3C recommendations](https://en.wikipedia.org/wiki/World_Wide_Web_Consortium#W3C_recommendation_(REC)). Het gebruikt publieke sleutelauthenticatie en is veiliger dan gedeelde geheimen die worden gebruikt in de Yubico OTP- en TOTP-methoden, omdat het de oorsprongsnaam (gewoonlijk de domeinnaam) bij de authenticatie betrekt. Attestatie wordt verstrekt om je te beschermen tegen phishing-aanvallen, aangezien het je helpt vast te stellen dat je de authentieke dienst gebruikt en niet een namaakkopie.

In tegenstelling tot Yubico OTP, gebruikt WebAuthn geen publieke ID, dus de sleutel is **niet** identificeerbaar over verschillende websites. Het maakt ook geen gebruik van een cloud server van derden voor verificatie. Alle communicatie vindt plaats tussen de sleutel en de website waarop je inlogt. FIDO gebruikt ook een teller die bij gebruik wordt opgehoogd om hergebruik van sessies en gekloonde sleutels te voorkomen.

Als een website of dienst WebAuthn ondersteunt voor de authenticatie, is het sterk aan te bevelen dit te gebruiken boven elke andere vorm van MFA.



## Algemene aanbevelingen

Wij hebben deze algemene aanbevelingen:



### Welke methode moet ik gebruiken?

Wanneer je jouw MFA-methode configureert, moet je in gedachten houden dat deze slechts zo veilig is als de zwakste authenticatiemethode die je gebruikt. Dit betekent dat het belangrijk is dat je alleen de beste beschikbare MFA-methode gebruikt. Als je bijvoorbeeld al TOTP gebruikt, moet je e-mail en SMS MFA uitschakelen. Als je al FIDO2/WebAuthn gebruikt, moet je geen Yubico OTP of TOTP gebruiken op jouw account.



### Back-ups

Je moet altijd back-ups hebben voor jouw MFA-methode. Hardwaresleutels kunnen zoekraken, gestolen worden of na verloop van tijd niet meer werken. Het is aan te bevelen om een paar hardware beveiligingssleutels te hebben met dezelfde toegang tot jouw accounts in plaats van slechts één.

Als je TOTP gebruikt met een authenticatie-app, zorg er dan voor dat je een back-up maakt van je herstelsleutels of van de app zelf, of kopieer de "gedeelde geheimen" naar een andere instantie van de app op een andere telefoon of naar een versleutelde container (bijv. [VeraCrypt](../encryption.md#veracrypt-disk)).



### Eerste installatie

Wanneer je een beveiligingssleutel koopt, is het belangrijk dat je de standaardgegevens wijzigt, wachtwoordbeveiliging voor de sleutel instelt, en aanraakbevestiging inschakelt als jouw sleutel dit ondersteunt. Producten zoals de YubiKey hebben meerdere interfaces met afzonderlijke referenties voor elk ervan, dus je moet elke interface overlopen en ook bescherming instellen.



### E-mail en SMS

Als je e-mail moet gebruiken voor MFA, zorg er dan voor dat de e-mailaccount zelf beveiligd is met een goede MFA-methode.

Als je SMS MFA gebruikt, gebruik dan een provider die jouw telefoonnummer niet zonder accounttoegang naar een nieuwe SIM-kaart wisselt, of gebruik een speciaal VoIP-nummer van een provider met vergelijkbare beveiliging om een [SIM-swapaanval te voorkomen](https://en.wikipedia.org/wiki/SIM_swap_scam).

[MFA tools die wij aanbevelen](../multi-factor-authentication.md ""){.md-button}



## Meer plaatsen om MFA op te zetten

Beyond just securing your website logins, multifactor authentication can be used to secure your local logins, SSH keys or even password databases as well.



### macOS

macOS heeft [native ondersteuning](https://support.apple.com/guide/deployment/intro-to-smart-card-integration-depd0b888248/web) voor authenticatie met smartcards (PIV). If you have a smart card or a hardware security key that supports the PIV interface such as the YubiKey, we recommend that you follow your smart card or hardware security vendor's documentation and set up second factor authentication for your macOS computer.

Yubico heeft een handleiding voor [het gebruik van je YubiKey als een smartcard in macOS](https://support.yubico.com/hc/articles/360016649059) die je kan helpen bij het instellen van je YubiKey op macOS.

After your smart card/security key is set up, we recommend running this command in the Terminal:



```text
sudo defaults write /Library/Preferences/com.apple.loginwindow DisableFDEAutoLogin -bool YES
```


Het commando zal voorkomen dat een tegenstander MFA omzeilt wanneer de computer opstart.



### Linux

<div class="admonition warning" markdown>
<p class="admonition-title">Let op</p>

Als de hostnaam van jouw systeem verandert (bijvoorbeeld door DHCP), zou je niet kunnen inloggen. Het is van vitaal belang dat je een correcte hostnaam instelt voor jouw computer alvorens deze gids te volgen.

</div>

De `pam_u2f` module op Linux kan twee-factor authenticatie bieden om in te loggen op de meeste populaire Linux distributies. Als je een hardware beveiligingssleutel hebt die U2F ondersteunt, kun je MFA verificatie instellen voor jouw aanmelding. Yubico heeft een gids genaamd [Ubuntu Linux Login Guide - U2F](https://support.yubico.com/hc/articles/360016649099-Ubuntu-Linux-Login-Guide-U2F) die op elke distributie zou moeten werken. De commando's van de pakketbeheerder - zoals `apt-get`- en de pakketnamen kunnen echter verschillen. Deze gids is **niet** van toepassing op Qubes OS.



### Qubes OS

Qubes OS heeft ondersteuning voor Challenge-Response authenticatie met YubiKeys. Als je een YubiKey hebt met Challenge-Response authenticatie ondersteuning, kijk dan eens naar de Qubes OS [YubiKey documentatie](https://qubes-os.org/doc/yubikey) als je MFA wilt instellen op Qubes OS.



### SSH



#### Hardware Veiligheidssleutels

SSH MFA kan worden ingesteld met behulp van meerdere verschillende authenticatiemethoden die populair zijn met hardware beveiligingssleutels. We raden je aan om de [documentatie](https://developers.yubico.com/SSH) van Yubico te raadplegen over hoe je dit kunt instellen.



#### TOTP

SSH MFA kan ook worden ingesteld met TOTP. DigitalOcean heeft een tutorial beschikbaar gesteld genaamd [How To Set Up Multi-Factor Authentication for SSH on Ubuntu 20.04](https://digitalocean.com/community/tutorials/how-to-set-up-multi-factor-authentication-for-ssh-on-ubuntu-20-04). De meeste dingen zouden hetzelfde moeten zijn, ongeacht de distributie, maar de commando's van de pakketbeheerder - zoals `apt-get`- en de pakketnamen kunnen verschillen.



### KeePass (en KeePassXC)

KeePass and KeePassXC databases can be secured using HOTP or Challenge-Response as a second-factor of authentication. Yubico heeft een document verstrekt voor KeePass [Using Your YubiKey with KeePass](https://support.yubico.com/hc/articles/360013779759-Using-Your-YubiKey-with-KeePass) en er is er ook een op de [KeePassXC](https://keepassxc.org/docs/#faq-yubikey-2fa) website.
