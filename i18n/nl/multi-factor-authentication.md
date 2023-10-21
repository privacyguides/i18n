---
title: "Multi-Factor Authenticators"
icon: 'material/two-factor-authentication'
description: Deze tools helpen je jouw internetaccounts te beveiligen met Multi-Factor Authentication zonder jouw geheimen naar een derde partij te sturen.
cover: multi-factor-authentication.webp
---

## Hardware Veiligheidssleutels

### YubiKey

!!! recommendation

    ![YubiKeys](assets/img/multi-factor-authentication/yubikey.png)
    
    De **YubiKeys** behoren tot de meest populaire beveiligingssleutels. Sommige YubiKey modellen hebben een breed scala aan functies, zoals: [Universal 2nd Factor (U2F)](https://en.wikipedia.org/wiki/Universal_2nd_Factor), [FIDO2 en WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), [Yubico OTP](basics/multi-factor-authentication.md#yubico-otp), [Personal Identity Verification (PIV)](https://developers.yubico.com/PIV), [OpenPGP](https://developers.yubico.com/PGP/), [TOTP en HOTP](https://developers.yubico.com/OATH) verificatie.
    
    Een van de voordelen van de YubiKey is dat één sleutel bijna alles kan (YubiKey 5), wat je van een hardware beveiligingssleutel mag verwachten. Wij raden je aan om vóór de aankoop de [quiz](https://www.yubico.com/quiz/) te nemen om er zeker van te zijn dat je de juiste keuze maakt.
    
    [:octicons-home-16: Homepage](https://www.yubico.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://docs.yubico.com/){ .card-link title=Documentatie}

Deze [vergelijkingstabel](https://www.yubico.com/store/compare/) toont de kenmerken en hoe de YubiKeys zich tot elkaar verhouden. Wij raden je ten zeerste aan om sleutels uit de YubiKey 5-serie te kiezen.

YubiKeys kunnen worden geprogrammeerd met behulp van de [YubiKey Manager](https://www.yubico.com/support/download/yubikey-manager/) of [YubiKey Personalization Tools](https://www.yubico.com/support/download/yubikey-personalization-tools/). Voor het beheer van TOTP-codes kunt je de [Yubico Authenticator](https://www.yubico.com/products/yubico-authenticator/)gebruiken. Alle Yubico's clients zijn open source.

Voor modellen die HOTP en TOTP ondersteunen, zijn er 2 slots in de OTP-interface die kunnen worden gebruikt voor HOTP en 32 slots om TOTP geheimen op te slaan. Deze geheimen worden versleuteld opgeslagen op de sleutel en worden nooit blootgesteld aan de apparaten waarop ze zijn aangesloten. Zodra een "seed" ( het gedeeld geheim) aan de Yubico Authenticator is gegeven, zal deze alleen de zescijferige codes geven, maar nooit de seed. Dit beveiligingsmodel beperkt wat een aanvaller kan doen als hij een van de apparaten waarop de Yubico Authenticator draait, in gevaar brengt en maakt de YubiKey bestand tegen een fysieke aanvaller.

!!! warning
    De firmware van YubiKey is niet open-source en kan niet worden geüpdatet. Als je functies in nieuwere firmwareversies wilt, of als er een kwetsbaarheid is in de firmwareversie die je gebruikt, moet je een nieuwe sleutel kopen.

### Nitrokey

!!! recommendation

    ![Nitrokey](assets/img/multi-factor-authentication/nitrokey.jpg){ align=right }
    
    **Nitrokey** heeft een beveiligingssleutel die geschikt is voor [FIDO2 en WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) genaamd de **Nitrokey FIDO2**. Voor PGP-ondersteuning moet je een van hun andere sleutels kopen, zoals de **Nitrokey Start**, **Nitrokey Pro 2** of de **Nitrokey Storage 2**.
    
    [:octicons-home-16: Homepage](https://www.nitrokey.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.nitrokey.com/data-privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://docs.nitrokey.com/){ .card-link title=Documentatie}

De [vergelijkingstabel](https://www.nitrokey.com/#comparison) toont de kenmerken en hoe de Nitrokey-modellen zich verhouden. De genoemde **Nitrokey 3** zal een gecombineerde functieset hebben.

Nitrokey-modellen kunnen worden geconfigureerd met behulp van de [Nitrokey-app](https://www.nitrokey.com/download).

Voor de modellen die HOTP en TOTP ondersteunen, zijn er 3 slots voor HOTP en 15 voor TOTP. Sommige Nitrokeys kunnen functioneren als een wachtwoord manager. Ze kunnen 16 verschillende inloggegevens opslaan en deze versleutelen met hetzelfde wachtwoord als de OpenPGP-interface.

!!! warning

    Hoewel Nitrokeys de HOTP/TOTP geheimen niet vrijgeven aan het apparaat waar ze op aangesloten zijn, is de HOTP en TOTP opslag **niet** versleuteld en is kwetsbaar voor fysieke aanvallen. If you are looking to store HOTP or TOTP secrets, we highly recommend that you use a YubiKey instead.

!!! warning

    Het resetten van de OpenPGP interface op een Nitrokey zal ook de wachtwoord database [inaccessible]maken (https://docs.nitrokey.com/pro/linux/factory-reset).

De Nitrokey Pro 2, Nitrokey Storage 2 en de komende Nitrokey 3 ondersteunen systeemintegriteitscontrole voor laptops met de [Coreboot](https://www.coreboot.org/) + [Heads](https://osresearch.net/) firmware.

Nitrokey's firmware is open-source, in tegenstelling tot de YubiKey. De firmware op moderne NitroKey-modellen (behalve de **NitroKey Pro 2**) kan worden bijgewerkt.

### Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

!!! example "Deze sectie is nieuw"

    We werken aan het vaststellen van gedefinieerde criteria voor elk deel van onze site, en dit kan onderhevig zijn aan verandering. Als je vragen hebt over onze criteria, stel ze dan [op ons forum](https://discuss.privacyguides.net/latest) en neem niet aan dat we iets niet in overweging hebben genomen bij het opstellen van onze aanbevelingen als het hier niet vermeld staat. Er zijn veel factoren die worden overwogen en besproken wanneer wij een project aanbevelen, en het documenteren van elke factor is een werk in uitvoering.

#### Minimale vereisten

- Moet gebruik maken van hoogwaardige, fraudebestendige hardwarebeveiligingsmodules.
- Moet de meest recente FIDO2-specificatie ondersteunen.
- Mag geen extractie van de private sleutel toestaan.
- Apparaten die meer dan 35 dollar kosten, moeten OpenPGP en S/MIME aankunnen.

#### Beste geval

Onze best-case criteria geven aan wat wij zouden willen zien van het perfecte project in deze categorie. Het is mogelijk dat onze aanbevelingen geen of niet alle functies bevatten, maar degene die dat wel doen kunnen hoger gerangschikt worden dan andere op deze pagina.

- Zou beschikbaar moeten zijn in USB-C vorm-factor.
- Zou beschikbaar moeten zijn met NFC.
- Moet TOTP opslag ondersteunen.
- Moet veilige firmware-updates ondersteunen.

## Authenticator Apps

Authenticator Apps implementeren een beveiligingsstandaard die is aangenomen door de Internet Engineering Task Force (IETF), genaamd **Time-based One-time Passwords**, of **TOTP**. Dit is een methode waarbij websites een geheim met je delen dat door jouw authenticator-app wordt gebruikt om een code van zes (meestal) cijfers te genereren op basis van de huidige tijd, die je invoert terwijl je inlogt om de website te controleren. Deze codes worden gewoonlijk om de 30 seconden geregenereerd, en zodra een nieuwe code is gegenereerd, wordt de oude nutteloos. Zelfs als een hacker één zescijferige code bemachtigt, is er geen manier om die code om te keren om het oorspronkelijke geheim te bemachtigen of om anderszins te kunnen voorspellen wat eventuele toekomstige codes zouden kunnen zijn.

Wij raden je ten zeerste aan om mobiele TOTP apps te gebruiken in plaats van desktop alternatieven, aangezien Android en IOS een betere beveiliging en app isolatie hebben dan de meeste desktop besturingssystemen.

### ente Auth

!!! recommendation

    ![ente Auth logo](assets/img/multi-factor-authentication/ente-auth.png){ align=right }
    
    **ente Auth** is a free and open-source app which stores and generates TOTP tokens on your mobile device. It can be used with an online account to backup and sync your tokens across your devices (and access them via a web interface) in a secure, end-to-end encrypted fashion. It can also be used offline on a single device with no account necessary.
    
    [:octicons-home-16: Homepage](https://ente.io/auth){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
    [:octicons-code-16:](https://github.com/ente-io/auth){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/ente-authenticator/id6444121398)
        - [:simple-github: GitHub](https://github.com/ente-io/auth/releases)
        - [:octicons-globe-16: Web](https://auth.ente.io)

### Aegis Authenticator (Android)

!!! recommendation

    ![Aegis logo](assets/img/multi-factor-authentication/aegis.png){ align=right }
    
    **Aegis Authenticator** is a free and open-source app for Android to manage your 2-step verification tokens for your online services. Aegis Authenticator operates completely offline/locally, but includes the option to export your tokens for backup unlike many alternatives.
    
    [:octicons-home-16: Homepage](https://getaegis.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title=Documentatie}
    [:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="Broncode" }
    [:octicons-heart-16:](https://www.buymeacoffee.com/beemdevelopment){ .card-link title=Bijdragen }
    
    ??? downloads "Downloaden"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
        - [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

### Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

!!! example "Deze sectie is nieuw"

    We werken aan het vaststellen van gedefinieerde criteria voor elk deel van onze site, en dit kan onderhevig zijn aan verandering. Als je vragen hebt over onze criteria, stel ze dan [op ons forum](https://discuss.privacyguides.net/latest) en neem niet aan dat we iets niet in overweging hebben genomen bij het opstellen van onze aanbevelingen als het hier niet vermeld staat. Er zijn veel factoren die worden overwogen en besproken wanneer wij een project aanbevelen, en het documenteren van elke factor is een werk in uitvoering.

- Broncode moet openbaar beschikbaar zijn.
- Moet geen internetverbinding vereisen.
- Mag niet synchroniseren met een cloud sync/backup service van derden.
    - **Optioneel is** E2EE sync-ondersteuning met OS-native tools aanvaardbaar, bv. versleutelde sync via iCloud.
