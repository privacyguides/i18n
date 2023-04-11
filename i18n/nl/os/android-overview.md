---
title: Android Overzicht
icon: simple/android
description: Android is een open-source besturingssysteem met sterke beveiliging, waardoor het onze topkeuze is voor telefoons.
---

Android is een veilig besturingssysteem met sterke [app sandboxing](https://source.android.com/security/app-sandbox), [Verified Boot](https://source.android.com/security/verifiedboot) (AVB), en een robuust [permission](https://developer.android.com/guide/topics/permissions/overview) control system.

## Het kiezen van een Android distributie

Wanneer je een Androidtelefoon koopt, wordt het standaardbesturingssysteem van het toestel vaak geleverd met een indringende integratie met apps en diensten die geen deel uitmaken van het [Android Open-Source Project](https://source.android.com/). Een voorbeeld hiervan zijn Google Play Services, die onherroepelijke rechten heeft om toegang te krijgen tot jouw bestanden, contactenopslag, oproeplogs, sms-berichten, locatie, camera, microfoon, hardware-identificaties, enzovoort. Deze apps en diensten vergroten het aanvalsoppervlak van jouw toestel en zijn de bron van diverse privacyproblemen met Android.

Dit probleem kan worden opgelost door een aangepaste Android-distributie te gebruiken die niet met een dergelijke invasieve integratie komt. Helaas schenden veel aangepaste Android-distributies vaak het Android-beveiligingsmodel door cruciale beveiligingsfuncties zoals AVB, terugdraaibeveiliging, firmware-updates, enzovoort, niet te ondersteunen. Sommige distributies leveren ook [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) builds die root blootstellen via [ADB](https://developer.android.com/studio/command-line/adb) en [meer permissieve](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) SELinux policies vereisen om debug-functies te accommoderen, wat resulteert in een verder verhoogd aanvalsoppervlak en een verzwakt beveiligingsmodel.

Idealiter, wanneer je een aangepaste Android distributie kiest, moet je ervoor zorgen dat het het Android beveiligingsmodel handhaaft. Op zijn minst zou de distributie productie builds moeten hebben, ondersteuning voor AVB, rollback bescherming, tijdige firmware en besturingssysteem updates, en SELinux in [enforcing mode](https://source.android.com/security/selinux/concepts#enforcement_levels). Al onze aanbevolen Android distributies voldoen aan deze criteria.

[Onze Android Systeemaanbevelingen :material-arrow-right-drop-circle:](../android.md ""){.md-button}

## Rooting vermijden

[Rooten van](https://en.wikipedia.org/wiki/Rooting_(Android)) Android-telefoons kan de veiligheid aanzienlijk verminderen omdat het het volledige [Android beveiligingsmodel verzwakt](https://en.wikipedia.org/wiki/Android_(operating_system)#Security_and_privacy). Dit kan de privacy verminderen mocht er een exploit zijn die door de verminderde beveiliging wordt geholpen. Bij veelgebruikte rootingmethoden wordt rechtstreeks met de opstartpartitie geknoeid, waardoor het onmogelijk is om een succesvolle Verified Boot uit te voeren. Apps die root vereisen zullen ook de systeempartitie wijzigen, wat betekent dat Verified Boot uitgeschakeld zou moeten blijven. Als root direct in de gebruikersinterface wordt blootgesteld, wordt ook het [aanvalsoppervlak](https://en.wikipedia.org/wiki/Attack_surface) van jouw apparaat vergroot en kan het helpen bij [privilege-escalatie](https://en.wikipedia.org/wiki/Privilege_escalation) kwetsbaarheden en omzeilen van SELinux-beleidslijnen.

Adblockers, die het [hosts file](https://en.wikipedia.org/wiki/Hosts_(file)) (AdAway) wijzigen en firewalls (AFWall+) die voortdurend root-toegang vereisen, zijn gevaarlijk en mogen niet worden gebruikt. Zij zijn ook niet de juiste manier om het beoogde doel te bereiken. Voor Adblocking stellen wij versleutelde [DNS](../dns.md) of [VPN](../vpn.md) serverblokkeringsoplossingen voor. RethinkDNS, TrackerControl en AdAway in niet-root modus zullen het VPN-slot innemen (door gebruik te maken van een lokale loopback VPN) waardoor je geen privacy verhogende diensten zoals Orbot of een echte VPN-server kunt gebruiken.

AFWall+ werkt op basis van de [packet filtering](https://en.wikipedia.org/wiki/Firewall_(computing)#Packet_filter) benadering en kan in sommige situaties omzeild worden.

Wij geloven niet dat de veiligheidsoffers die gemaakt worden door het rooten van een telefoon, de twijfelachtige privacyvoordelen van die apps waard zijn.

## Geverifieerde boot

[Geverifieerde Boot](https://source.android.com/security/verifiedboot) is een belangrijk onderdeel van het Android-beveiligingsmodel. Het biedt bescherming tegen [evil maid](https://en.wikipedia.org/wiki/Evil_maid_attack) aanvallen, malware persistentie, en zorgt ervoor dat beveiligingsupdates niet kunnen worden gedowngraded met [rollback protection](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection).

Android 10 en hoger is overgestapt van volledige schijfversleuteling naar meer flexibele [bestandsgebaseerde versleuteling](https://source.android.com/security/encryption/file-based). Jouw gegevens worden versleuteld met unieke encryptiesleutels, en de bestanden van het besturingssysteem blijven onversleuteld.

Verified Boot garandeert de integriteit van de besturingssysteembestanden en voorkomt zo dat een tegenstander met fysieke toegang kan knoeien of malware op het apparaat kan installeren. In het onwaarschijnlijke geval dat malware in staat is om andere delen van het systeem te misbruiken en hogere geprivilegieerde toegang te verkrijgen, zal Verified Boot veranderingen aan de systeempartitie voorkomen en terugdraaien bij het herstarten van het apparaat.

OEM's zijn helaas alleen verplicht om de verspreiding van geverifieerde Boot op hun voorraad Android te ondersteunen. Slechts enkele OEM's, zoals Google, ondersteunen aangepaste AVB key enrollment op hun toestellen. Bovendien ondersteunen sommige AOSP afgeleiden zoals LineageOS of /e/ OS Verified Boot niet, zelfs niet op hardware met Verified Boot-ondersteuning voor besturingssystemen van derden. Wij raden je aan te controleren of er ondersteuning is op **voordat je** een nieuw apparaat aanschaft. AOSP-derivaten die geen Geverifieerde Boot ondersteunen, worden **niet** aanbevolen.

Veel OEM's hebben ook een gebroken uitvoering van Verified Boot waar je je bewust van moet zijn buiten hun marketing. De Fairphone 3 en 4 zijn bijvoorbeeld standaard niet veilig, aangezien de [standaard bootloader vertrouwt op de publieke AVB signing key](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). Dit breekt geverifieerd opstarten op een standaard Fairphone toestel, omdat het systeem alternatieve Android besturingssystemen zoals (zoals /e/) [zal opstarten zonder enige waarschuwing](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) over aangepast besturingssysteem gebruik.

## Firmware-updates

Firmware-updates zijn van cruciaal belang voor het behoud van de veiligheid en zonder deze updates kan uw toestel niet veilig zijn. OEM's hebben ondersteuningsovereenkomsten met hun partners om de closed-source componenten voor een beperkte ondersteuningsperiode te leveren. Deze worden gedetailleerd beschreven in de maandelijkse [Android Security Bulletins](https://source.android.com/security/bulletin).

Aangezien de onderdelen van de telefoon, zoals de processor en de radiotechnologieën, afhankelijk zijn van closed-source componenten, moeten de updates door de respectieve fabrikanten worden verstrekt. Daarom is het belangrijk dat u een toestel koopt binnen een actieve ondersteuningscyclus. [Qualcomm](https://www.qualcomm.com/news/releases/2020/12/16/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) en [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox/) ondersteunen hun toestellen gedurende 4 jaar, terwijl goedkopere producten vaak kortere ondersteuningscycli hebben. Met de introductie van de [Pixel 6](https://support.google.com/pixelphone/answer/4457705) maakt Google nu hun eigen SoC en zullen ze minimaal 5 jaar ondersteuning bieden.

EOL-apparaten die niet langer door de SoC-fabrikant worden ondersteund, kunnen geen firmware-updates ontvangen van OEM-verkopers of aftermarket-distributeurs van Android. Dit betekent dat beveiligingsproblemen met die apparaten onopgelost zullen blijven.

Fairphone, bijvoorbeeld, brengt hun toestellen op de markt met een ondersteuning van 6 jaar. De SoC (Qualcomm Snapdragon 750G op de Fairphone 4) heeft echter een aanzienlijk kortere EOL-datum. Dit betekent dat de firmware-beveiligingsupdates van Qualcomm voor de Fairphone 4 in september 2023 aflopen, ongeacht of Fairphone doorgaat met het uitbrengen van software-beveiligingsupdates.

## Android-versies

Het is belangrijk om geen [end-of-life](https://endoflife.date/android) versie van Android te gebruiken. Nieuwere versies van Android krijgen niet alleen beveiligingsupdates voor het besturingssysteem, maar ook belangrijke updates die privacy verbeteren. Bijvoorbeeld, [vóór Android 10](https://developer.android.com/about/versions/10/privacy/changes) konden alle apps met de toestemming [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) toegang krijgen tot gevoelige en unieke serienummers van uw telefoon, zoals [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), en uw SIM-kaart [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity). Nu moeten dat systeem-apps zijn om dit te kunnen doen. Systeem-apps worden alleen geleverd door de OEM of de Android-distributie.

## Android-machtigingen

[Machtigingen op Android](https://developer.android.com/guide/topics/permissions/overview) geven je controle over waar apps toegang tot toe krijgen. Google brengt regelmatig [verbeteringen aan](https://developer.android.com/about/versions/11/privacy/permissions) in het machtigingssysteem in elke opeenvolgende versie. Alle apps die je installeert zijn strikt [sandboxed](https://source.android.com/security/app-sandbox), daarom is het niet nodig om antivirus apps te installeren.

Een smartphone met de nieuwste versie van Android zal altijd veiliger zijn dan een oude smartphone met een betaalde antivirus. Het is beter om niet te betalen voor antivirussoftware en geld te sparen om een nieuwe smartphone te kopen, zoals een Google Pixel.

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

- Een permissie voor [nabijgelegen wifi toegang](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). De MAC-adressen van WiFi-toegangspunten in de buurt waren een populaire manier voor apps om de locatie van een gebruiker te traceren.
- Een meer [granulaire mediatoestemmingen](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions), wat betekent dat je alleen toegang kan verlenen tot afbeeldingen, video's of audiobestanden.
- Achtergrondgebruik van sensoren vereist nu de toestemming [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission).

Een app kan een toestemming vragen voor een specifieke functie die hij heeft. Bijvoorbeeld, elke app die QR-codes kan scannen heeft toestemming voor de camera nodig. Sommige apps kunnen meer toestemmingen vragen dan ze nodig hebben.

[Exodus](https://exodus-privacy.eu.org/) kan nuttig zijn bij het vergelijken van apps die vergelijkbare doelen hebben. Als een app veel machtigingen nodig heeft en veel advertenties en analytics heeft, is dit waarschijnlijk een slecht teken. Wij raden aan de individuele trackers te bekijken en hun beschrijvingen te lezen in plaats van eenvoudigweg **het totaal** te tellen en aan te nemen dat alle vermelde items gelijk zijn.

!!! warning

    Als een app vooral een webdienst is, kan de tracking aan de serverzijde plaatsvinden. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest/) toont "geen trackers", maar volgt zeker de interesses en het gedrag van gebruikers op de site. Apps kunnen detectie omzeilen door geen gebruik te maken van door de reclame-industrie geproduceerde standaardcodebibliotheken, hoewel dit onwaarschijnlijk is.

!!! note

    Privacy-vriendelijke apps zoals [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest/) kunnen sommige trackers tonen zoals [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49/). Deze bibliotheek bevat [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) die [pushmeldingen](https://en.wikipedia.org/wiki/Push_technology) in apps kan bieden. Dit [is het geval](https://fosstodon.org/@bitwarden/109636825700482007) met Bitwarden. Dat betekent niet dat Bitwarden alle analysefuncties gebruikt die Google Firebase Analytics biedt.

## Mediatoegang

Heel wat toepassingen laten je toe een bestand te "delen" met hen voor het uploaden van media. Als je bijvoorbeeld een foto naar Twitter wilt tweeten, geef Twitter dan geen toegang tot jouw "media en foto's", want dan heeft het toegang tot al jouw foto's. Ga in plaats daarvan naar je bestandsbeheerder (documentsUI), houd de foto vast en deel hem dan met Twitter.

## Gebruikers Profielen

Meervoudige gebruikersprofielen zijn te vinden in **Instellingen** → **Systeem** → **Meervoudige gebruikers** en zijn de eenvoudigste manier om te isoleren in Android.

Met gebruikersprofielen kun je beperkingen opleggen aan een specifiek profiel, zoals: bellen, sms'en of apps installeren op het toestel. Elk profiel wordt versleuteld met zijn eigen versleutelingscode en heeft geen toegang tot de gegevens van andere profielen. Zelfs de eigenaar van het apparaat kan de gegevens van andere profielen niet bekijken zonder hun wachtwoord te kennen. Meervoudige gebruikersprofielen zijn een veiligere methode van isolatie.

## Werkprofiel

[Werkprofielen](https://support.google.com/work/android/answer/6191949) zijn een andere manier om afzonderlijke apps te isoleren en kunnen handiger zijn dan afzonderlijke gebruikersprofielen.

Een **apparaatcontroller** zoals [Shelter](#recommended-apps) is vereist, tenzij je CalyxOS gebruikt die er een bevat.

Het werkprofiel is afhankelijk van een apparaatcontroller om te kunnen functioneren. Functies zoals *File Shuttle* en *contact zoeken blokkeren* of enige vorm van isolatiefuncties moeten door de controller worden geïmplementeerd. Je moet de apparaatcontroller-app ook volledig vertrouwen, aangezien deze volledige toegang heeft tot jouw gegevens binnen het werkprofiel.

Deze methode is over het algemeen minder veilig dan een secundair gebruikersprofiel; het biedt je echter wel het gemak dat je tegelijkertijd apps kunt uitvoeren in zowel het werk- als het persoonlijke profiel.

## VPN Killswitch

Android 7 en hoger ondersteunt een VPN killswitch en het is beschikbaar zonder de noodzaak om apps van derden te installeren. Deze functie kan lekken voorkomen als de VPN wordt verbroken. Het kan gevonden worden in :gear: **Instellingen** → **Netwerk & internet** → **VPN** → :gear: → **Blokkeer verbindingen zonder VPN**.

## Globale schakelaars

Moderne Android-toestellen hebben globale toggles voor het uitschakelen van Bluetooth en locatiediensten. Android 12 introduceerde toggles voor de camera en microfoon. Wanneer u deze functies niet gebruikt, raden wij je aan ze uit te schakelen. Apps kunnen geen gebruik maken van uitgeschakelde functies (zelfs niet als daarvoor individuele toestemming is verleend) totdat ze weer zijn ingeschakeld.

## Google

Als je een apparaat gebruikt met Google-diensten, hetzij ujouw standaard besturingssysteem of een besturingssysteem dat Google Play Services veilig sandboxed zoals GrapheneOS, zijn er een aantal extra wijzigingen die je kunt aanbrengen om jouw privacy te verbeteren. We raden nog steeds aan om Google diensten volledig te vermijden, of om Google Play diensten te beperken tot een specifiek gebruiker/werkprofiel door een apparaatcontroller zoals *Shelter* te combineren met GrapheneOS's Sandboxed Google Play.

### Geavanceerd beschermingsprogramma

Als je een Google-account hebt, raden wij je aan je in te schrijven voor het [Advanced Protection Program](https://landing.google.com/advancedprotection/). Het is gratis beschikbaar voor iedereen met twee of meer hardware beveiligingssleutels met [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) ondersteuning.

Het geavanceerde beschermingsprogramma biedt verbeterde controle op bedreigingen en maakt het mogelijk:

- Strengere tweefactorauthenticatie; bv. dat [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **moet worden gebruikt** en dat het gebruik van [SMS OTP's](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) en [OAuth](https://en.wikipedia.org/wiki/OAuth)niet is toegestaan
- Alleen Google en geverifieerde apps van derden hebben toegang tot accountgegevens
- Scannen van inkomende e-mails op Gmail-accounts voor [phishing](https://en.wikipedia.org/wiki/Phishing#Email_phishing) pogingen
- Strengere [veilige browser scannen](https://www.google.com/chrome/privacy/whitepaper.html#malware) met Google Chrome
- Striktere herstelprocedure voor accounts met verloren inloggegevens

 Als je gebruikmaakt van niet-sandboxed Google Play Services (gebruikelijk op standaard besturingssystemen), wordt het Advanced Protection Program ook geleverd met [extra voordelen](https://support.google.com/accounts/answer/9764949?hl=en), zoals:

- Installatie van apps buiten de Google Play Store, de app-winkel van de leverancier van het besturingssysteem of via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)is niet toegestaan
- Verplichte automatische apparaatscan met [Play Protect](https://support.google.com/googleplay/answer/2812853?hl=en#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- Je waarschuwt voor niet geverifieerde toepassingen

### Google Play Systeem Updates

In het verleden moesten beveiligingsupdates voor Android worden verzonden door de leverancier van het besturingssysteem. Android is meer modulair geworden vanaf Android 10, en Google kan beveiligingsupdates pushen voor **sommige** systeemcomponenten via de bevoorrechte Play Services.

Als je een EOL-apparaat hebt dat met Android 10 of hoger wordt geleverd en geen van onze aanbevolen besturingssystemen op jouw apparaat kunt uitvoeren, kun je waarschijnlijk beter bij jouw OEM Android-installatie blijven (in tegenstelling tot een besturingssysteem dat hier niet wordt vermeld, zoals LineageOS of /e/ OS). Hierdoor kunt je **sommige** beveiligingsfixes van Google ontvangen, terwijl je het Android beveiligingsmodel niet schendt door een onveilig Android derivaat te gebruiken en jouw aanvalsoppervlak te vergroten. We raden nog steeds aan zo snel mogelijk te upgraden naar een ondersteund apparaat.

### Reclame-ID

Alle apparaten waarop Google Play Services zijn geïnstalleerd, genereren automatisch een [-reclame-ID](https://support.google.com/googleplay/android-developer/answer/6048248?hl=en) die wordt gebruikt voor gerichte reclame. Schakel deze functie uit om de over je verzamelde gegevens te beperken.

Op Android distributies met [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), ga naar :gear: **Instellingen** → **Apps** → **Sandboxed Google Play** → **Google Instellingen** → **Advertenties**, en selecteer *Verwijder reclame ID*.

Op Android distributies met geprivilegieerde Google Play Services (zoals standaard OSes), kan de instelling op een van verschillende locaties staan. Check

- :gear: **Instellingen** → **Google** → **Advertenties**
- :gear: **Instellingen** → **Privacy** → **Advertenties**

Je krijgt de optie om jouw advertentie-ID te verwijderen of om *af te melden voor op interesses gebaseerde advertenties*, dit varieert tussen OEM-distributies van Android. Als de mogelijkheid wordt geboden om de reclame-ID te wissen, heeft dat de voorkeur. Zo niet, zorg er dan voor dat je je afmeldt en jouw reclame-ID reset.

### SafetyNet en Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) en de [Play Integrity API's](https://developer.android.com/google/play/integrity) worden over het algemeen gebruikt voor [bankapps](https://grapheneos.org/usage#banking-apps). Veel bank apps zullen prima werken in GrapheneOS met sandboxed Play services, maar sommige niet-financiële apps hebben hun eigen grove anti-tampering mechanismen die kunnen falen. GrapheneOS doorstaat de `basicIntegrity` check, maar niet de certificeringscheck `ctsProfileMatch`. Toestellen met Android 8 of later hebben hardware-attestondersteuning die niet kan worden omzeild zonder gelekte sleutels of ernstige kwetsbaarheden.

Wat Google Wallet betreft, wij raden dit niet aan vanwege hun [privacybeleid](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), waarin staat dat je zich moet afmelden als je niet wilt dat jouw kredietwaardigheid en persoonlijke gegevens worden gedeeld met affiliate marketingdiensten.
