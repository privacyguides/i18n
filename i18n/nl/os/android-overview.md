---
title: Android Overview
icon: simple/android
description: Android is an open-source operating system with strong security protections, which makes it our top choice for phones.
robots: nofollow, max-snippet:-1, max-image-preview:large
---

![Android logo](../assets/img/android/android.svg){ align=right }

The **Android Open Source Project** is a secure mobile operating system featuring strong [app sandboxing](https://source.android.com/security/app-sandbox), [Verified Boot](https://source.android.com/security/verifiedboot) (AVB), and a robust [permission](https://developer.android.com/guide/topics/permissions/overview) control system.

[:octicons-home-16:](https://source.android.com){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/main){ .card-link title="Source Code" }

[Our Android Advice :material-arrow-right-drop-circle:](../android/index.md ""){.md-button.md-button--primary}

## Security Protections

Key components of the Android security model include [verified boot](#verified-boot), [firmware updates](#firmware-updates), and a robust [permission system](#android-permissions). These important security features form the baseline of the minimum criteria for our [mobile phone](../mobile-phones.md) and [custom Android OS](../android/distributions.md) recommendations.

### Geverifieerde boot

[**Verified Boot**](https://source.android.com/security/verifiedboot) is an important part of the Android security model. Het biedt bescherming tegen [evil maid](https://en.wikipedia.org/wiki/Evil_maid_attack) aanvallen, malware persistentie, en zorgt ervoor dat beveiligingsupdates niet kunnen worden gedowngraded met [rollback protection](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection).

Android 10 en hoger is overgestapt van volledige schijfversleuteling naar meer flexibele [bestandsgebaseerde versleuteling](https://source.android.com/security/encryption/file-based). Jouw gegevens worden versleuteld met unieke encryptiesleutels, en de bestanden van het besturingssysteem blijven onversleuteld.

Verified Boot garandeert de integriteit van de besturingssysteembestanden en voorkomt zo dat een tegenstander met fysieke toegang kan knoeien of malware op het apparaat kan installeren. In het onwaarschijnlijke geval dat malware in staat is om andere delen van het systeem te misbruiken en hogere geprivilegieerde toegang te verkrijgen, zal Verified Boot veranderingen aan de systeempartitie voorkomen en terugdraaien bij het herstarten van het apparaat.

OEM's zijn helaas alleen verplicht om de verspreiding van geverifieerde Boot op hun voorraad Android te ondersteunen. Slechts enkele OEM's, zoals Google, ondersteunen aangepaste AVB key enrollment op hun toestellen. Bovendien ondersteunen sommige AOSP afgeleiden zoals LineageOS of /e/ OS Verified Boot niet, zelfs niet op hardware met Verified Boot-ondersteuning voor besturingssystemen van derden. Wij raden je aan te controleren of er ondersteuning is op **voordat je** een nieuw apparaat aanschaft. AOSP-derivaten die geen Geverifieerde Boot ondersteunen, worden **niet** aanbevolen.

Veel OEM's hebben ook een gebroken uitvoering van Verified Boot waar je je bewust van moet zijn buiten hun marketing. De Fairphone 3 en 4 zijn bijvoorbeeld standaard niet veilig, aangezien de [standaard bootloader vertrouwt op de publieke AVB signing key](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). This breaks verified boot on a stock Fairphone device, as the system will boot alternative Android operating systems (such as /e/) [without any warning](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) about custom operating system usage.

### Firmware-updates

**Firmware updates** are critical for maintaining security and without them your device cannot be secure. OEM's hebben ondersteuningsovereenkomsten met hun partners om de closed-source componenten voor een beperkte ondersteuningsperiode te leveren. Deze worden gedetailleerd beschreven in de maandelijkse [Android Security Bulletins](https://source.android.com/security/bulletin).

Aangezien de onderdelen van de telefoon, zoals de processor en de radiotechnologieën, afhankelijk zijn van closed-source componenten, moeten de updates door de respectieve fabrikanten worden verstrekt. Daarom is het belangrijk dat u een toestel koopt binnen een actieve ondersteuningscyclus. [Qualcomm](https://qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) and [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox) support their devices for 4 years, while cheaper products often have shorter support cycles. With the introduction of the [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google now makes their own SoC, and they will provide a minimum of 5 years of support. With the introduction of the Pixel 8 series, Google increased that support window to 7 years.

EOL-apparaten die niet langer door de SoC-fabrikant worden ondersteund, kunnen geen firmware-updates ontvangen van OEM-verkopers of aftermarket-distributeurs van Android. Dit betekent dat beveiligingsproblemen met die apparaten onopgelost zullen blijven.

Fairphone, for example, markets their Fairphone 4 device as receiving 6 years of support. De SoC (Qualcomm Snapdragon 750G op de Fairphone 4) heeft echter een aanzienlijk kortere EOL-datum. Dit betekent dat de firmware-beveiligingsupdates van Qualcomm voor de Fairphone 4 in september 2023 aflopen, ongeacht of Fairphone doorgaat met het uitbrengen van software-beveiligingsupdates.

### Android-machtigingen

[**Permissions on Android**](https://developer.android.com/guide/topics/permissions/overview) grant you control over what apps are allowed to access. Google brengt regelmatig [verbeteringen aan](https://developer.android.com/about/versions/11/privacy/permissions) in het machtigingssysteem in elke opeenvolgende versie. Alle apps die je installeert zijn strikt [sandboxed](https://source.android.com/security/app-sandbox), daarom is het niet nodig om antivirus apps te installeren.

Een smartphone met de nieuwste versie van Android zal altijd veiliger zijn dan een oude smartphone met een betaalde antivirus. It's better not to pay for antivirus software and to save money to buy a new smartphone such as a [Google Pixel](../mobile-phones.md#google-pixel).

Android 10:

- [Scoped Storage](https://developer.android.com/about/versions/10/privacy/changes#scoped-storage) geeft je meer controle over jouw bestanden en kan beperken wat [toegang heeft tot externe opslag](https://developer.android.com/training/data-storage#permissions). Apps kunnen een specifieke map in externe opslag hebben en de mogelijkheid om daar specifieke soorten media op te slaan.
- Strengere toegang op [apparaatlocatie](https://developer.android.com/about/versions/10/privacy/changes#app-access-device-location) door invoering van de machtiging `ACCESS_BACKGROUND_LOCATION`. Dit voorkomt dat apps op de achtergrond toegang krijgen tot de locatie zonder uitdrukkelijke toestemming van de gebruiker.

Android 11:

- [Eenmalige toestemmingen](https://developer.android.com/about/versions/11/privacy/permissions#one-time) waarmee je eenmalig een machtiging kunt verlenen aan een app.
- [Automatische reset machtigingen](https://developer.android.com/about/versions/11/privacy/permissions#auto-reset), die [runtime machtigingen](https://developer.android.com/guide/topics/permissions/overview#runtime) terugzet die werden toegekend toen de app werd geopend.
- Machtigingen voor toegang tot [telefoon nummer](https://developer.android.com/about/versions/11/privacy/permissions#phone-numbers) gerelateerde functies.

Android 12:

- Een machtiging om alleen de [geschatte locatie](https://developer.android.com/about/versions/12/behavior-changes-12#approximate-location) toe te kennen.
- Auto-reset van [apps in slaapstand](https://developer.android.com/about/versions/12/behavior-changes-12#app-hibernation).
- [Data access auditing](https://developer.android.com/about/versions/12/behavior-changes-12#data-access-auditing) die het gemakkelijker maakt om te bepalen welk deel van een app een bepaald type gegevenstoegang gebruikt.

Android 13:

- A permission for [nearby Wi-Fi access](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). The MAC addresses of nearby Wi-Fi access points were a popular way for apps to track a user's location.
- Een meer [granulaire mediatoestemmingen](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions), wat betekent dat je alleen toegang kan verlenen tot afbeeldingen, video's of audiobestanden.
- Achtergrondgebruik van sensoren vereist nu de toestemming [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission).

Een app kan een toestemming vragen voor een specifieke functie die hij heeft. Bijvoorbeeld, elke app die QR-codes kan scannen heeft toestemming voor de camera nodig. Sommige apps kunnen meer toestemmingen vragen dan ze nodig hebben.

[Exodus](https://exodus-privacy.eu.org) can be useful when comparing apps that have similar purposes. Als een app veel machtigingen nodig heeft en veel advertenties en analytics heeft, is dit waarschijnlijk een slecht teken. Wij raden aan de individuele trackers te bekijken en hun beschrijvingen te lezen in plaats van eenvoudigweg **het totaal** te tellen en aan te nemen dat alle vermelde items gelijk zijn.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Als een app vooral een webdienst is, kan de tracking aan de serverzijde plaatsvinden. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest) shows "no trackers" but certainly does track users' interests and behavior across the site. Apps kunnen detectie omzeilen door geen gebruik te maken van door de reclame-industrie geproduceerde standaardcodebibliotheken, hoewel dit onwaarschijnlijk is.

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Privacy-friendly apps such as [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest) may show some trackers such as [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49). Deze bibliotheek bevat [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) die [pushmeldingen](https://en.wikipedia.org/wiki/Push_technology) in apps kan bieden. Dit [is het geval](https://fosstodon.org/@bitwarden/109636825700482007) met Bitwarden. That doesn't mean that Bitwarden is using all the analytics features that are provided by Google Firebase Analytics.

</div>

## Privacy Features

### Gebruikers Profielen

Multiple **user profiles** can be found in :gear: **Settings** → **System** → **Users** and are the simplest way to isolate in Android.

With user profiles, you can impose restrictions on a specific profile, such as: making calls, using SMS, or installing apps. Elk profiel wordt versleuteld met zijn eigen versleutelingscode en heeft geen toegang tot de gegevens van andere profielen. Zelfs de eigenaar van het apparaat kan de gegevens van andere profielen niet bekijken zonder hun wachtwoord te kennen. Meervoudige gebruikersprofielen zijn een veiligere methode van isolatie.

### Werkprofiel

[**Work Profiles**](https://support.google.com/work/android/answer/6191949) are another way to isolate individual apps and may be more convenient than separate user profiles.

A **device controller** app such as [Shelter](../android/general-apps.md#shelter) is required to create a Work Profile without an enterprise MDM, unless you're using a custom Android OS which includes one.

Het werkprofiel is afhankelijk van een apparaatcontroller om te kunnen functioneren. Functies zoals *File Shuttle* en *contact zoeken blokkeren* of enige vorm van isolatiefuncties moeten door de controller worden geïmplementeerd. You must also fully trust the device controller app, as it has full access to your data inside the work profile.

This method is generally less secure than a secondary user profile; however, it does allow you the convenience of running apps in both the owner profile and work profile simultaneously.

### Private Space

**Private Space** is a feature introduced in Android 15 that adds another way of isolating individual apps. You can set up a private space in the owner profile by navigating to :gear: **Settings** → **Security & privacy** → **Private space**. Once set up, your private space resides at the bottom of the app drawer.

Like user profiles, a private space is encrypted using its own encryption key, and you have the option to set up a different unlock method. Like work profiles, you can use apps from both the owner profile and private space simultaneously. Apps launched from a private space are distinguished by an icon depicting a key within a shield.

Unlike work profiles, Private Space is a feature native to Android that does not require a third-party app to manage it. For this reason, we generally recommend using a private space over a work profile, though you can use a work profile alongside a private space.

### VPN kill switch

Android 7 and above supports a VPN kill switch, and it is available without the need to install third-party apps. Deze functie kan lekken voorkomen als de VPN wordt verbroken. Het kan gevonden worden in :gear: **Instellingen** → **Netwerk & internet** → **VPN** → :gear: → **Blokkeer verbindingen zonder VPN**.

### Globale schakelaars

Moderne Android-toestellen hebben globale toggles voor het uitschakelen van Bluetooth en locatiediensten. Android 12 introduceerde toggles voor de camera en microfoon. Wanneer u deze functies niet gebruikt, raden wij je aan ze uit te schakelen. Apps cannot use disabled features (even if granted individual permissions) until re-enabled.

## Google Services

If you are using a device with Google services—whether with the stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS—there are a number of additional changes you can make to improve your privacy. We still recommend avoiding Google services entirely, or limiting Google Play Services to a specific user/work profile by combining a device controller like *Shelter* with GrapheneOS's Sandboxed Google Play.

### Geavanceerd beschermingsprogramma

If you have a Google account we suggest enrolling in the [Advanced Protection Program](https://landing.google.com/advancedprotection). Het is gratis beschikbaar voor iedereen met twee of meer hardware beveiligingssleutels met [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) ondersteuning. Alternatively, you can use [passkeys](https://fidoalliance.org/passkeys).

Het geavanceerde beschermingsprogramma biedt verbeterde controle op bedreigingen en maakt het mogelijk:

- Stricter two-factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](https://en.wikipedia.org/wiki/OAuth)
- Alleen Google en geverifieerde apps van derden hebben toegang tot accountgegevens
- Scannen van inkomende e-mails op Gmail-accounts voor [phishing](https://en.wikipedia.org/wiki/Phishing#Email_phishing) pogingen
- Stricter [safe browser scanning](https://google.com/chrome/privacy/whitepaper.html#malware) with Google Chrome
- Striktere herstelprocedure voor accounts met verloren inloggegevens

 If you use non-sandboxed Google Play Services (common on stock operating systems), the Advanced Protection Program also comes with [additional benefits](https://support.google.com/accounts/answer/9764949) such as:

- Not allowing app installation outside the Google Play Store, the OS vendor's app store, or via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Mandatory automatic device scanning with [Play Protect](https://support.google.com/googleplay/answer/2812853?#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- Je waarschuwt voor niet geverifieerde toepassingen

### Google Play Systeem Updates

In het verleden moesten beveiligingsupdates voor Android worden verzonden door de leverancier van het besturingssysteem. Android is meer modulair geworden vanaf Android 10, en Google kan beveiligingsupdates pushen voor **sommige** systeemcomponenten via de bevoorrechte Play Services.

Als je een EOL-apparaat hebt dat met Android 10 of hoger wordt geleverd en geen van onze aanbevolen besturingssystemen op jouw apparaat kunt uitvoeren, kun je waarschijnlijk beter bij jouw OEM Android-installatie blijven (in tegenstelling tot een besturingssysteem dat hier niet wordt vermeld, zoals LineageOS of /e/ OS). Hierdoor kunt je **sommige** beveiligingsfixes van Google ontvangen, terwijl je het Android beveiligingsmodel niet schendt door een onveilig Android derivaat te gebruiken en jouw aanvalsoppervlak te vergroten. We raden nog steeds aan zo snel mogelijk te upgraden naar een ondersteund apparaat.

### Reclame-ID

All devices with Google Play Services installed automatically generate an [advertising ID](https://support.google.com/googleplay/android-developer/answer/6048248) used for targeted advertising. Schakel deze functie uit om de over je verzamelde gegevens te beperken.

Op Android distributies met [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), ga naar :gear: **Instellingen** → **Apps** → **Sandboxed Google Play** → **Google Instellingen** → **Advertenties**, en selecteer *Verwijder reclame ID*.

On Android distributions with privileged Google Play Services (which includes the stock installation on most devices), the setting may be in one of several locations. Check

- :gear: **Instellingen** → **Google** → **Advertenties**
- :gear: **Instellingen** → **Privacy** → **Advertenties**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads* (this varies between OEM distributions of Android). If presented with the option to delete the advertising ID, that is preferred. Zo niet, zorg er dan voor dat je je afmeldt en jouw reclame-ID reset.

### SafetyNet en Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) en de [Play Integrity API's](https://developer.android.com/google/play/integrity) worden over het algemeen gebruikt voor [bankapps](https://grapheneos.org/usage#banking-apps). Veel bank apps zullen prima werken in GrapheneOS met sandboxed Play services, maar sommige niet-financiële apps hebben hun eigen grove anti-tampering mechanismen die kunnen falen. GrapheneOS doorstaat de `basicIntegrity` check, maar niet de certificeringscheck `ctsProfileMatch`. Toestellen met Android 8 of later hebben hardware-attestondersteuning die niet kan worden omzeild zonder gelekte sleutels of ernstige kwetsbaarheden.

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt out if you don't want your credit rating and personal information shared with affiliate marketing services.
