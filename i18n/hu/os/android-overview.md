---
title: Android áttekintés
icon: simple/android
description: Az Android egy nyílt forráskódú operációs rendszer, amely erős biztonsági védelemmel rendelkezik, ezért ez az elsődleges választásunk telefonok esetében.
---

![Android logo](../assets/img/android/android.svg){ align=right }

Az **Android Nyílt Forráskódú Projekt** egy biztonságos mobil operációs rendszer, amely erős [app sandbox-kszal](https://source.android.com/security/app-sandbox), [Verified Boot-tal](https://source.android.com/security/verifiedboot) (AVB) és egy erőteljes [engedély](https://developer.android.com/guide/topics/permissions/overview) ellenőrző rendszerrel rendelkezik.

## A mi tanácsaink

### Egy Android disztribúció kiválasztása

Egy Android telefon vásárlásakor a készülék alapértelmezett operációs rendszere gyakran olyan alkalmazások és szolgáltatások invazív integrációját tartalmazza, amelyek nem részei az [Android Open-Source Project](https://source.android.com/)-nek. Ilyen például a Google Play Szolgáltatások, amely visszavonhatatlan jogosultságokkal rendelkezik a fájljaidhoz, névjegy tárolódhoz, hívásnaplóidhoz, SMS-üzeneteidhez, tartózkodási helyedhez, kamerádhoz, mikrofonodhoz, hardverazonosítóidhoz, stb. való hozzáférésre. Ezek az alkalmazások és szolgáltatások növelik a készüléked támadási felületét, és számos adatvédelmi aggály forrását jelentik az Androiddal kapcsolatban.

Ez a probléma megoldható lehet egy olyan egyedi Android-disztribúció használatával, amely nem tartalmaz ilyen invazív integrációkat. Sajnos sok egyedi Android disztribúció gyakran megsérti az Android biztonsági modellt azzal, hogy nem támogat olyan kritikus biztonsági funkciókat, mint az AVB, a rollback védelem, firmware-frissítések, stb. Egyes disztribúciók [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) buildeket nyújtanak, amelyek védtelenné teszik a root-ot az [ADB](https://developer.android.com/studio/command-line/adb)-n keresztül és [több engedélyt biztosító](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) SELinux policy-kat igényelnek a hibakeresési funkciókhoz, ami tovább növeli a támadási felületet és gyengébb biztonsági modellt eredményez.

Ideális esetben, amikor egyedi Android disztribúciót választasz, győződj meg arról, hogy az, az Android biztonsági modellt követi. A disztribúciónak minimum rendelkeznie kell gyártási buildekkel, AVB támogatással, rollback védelemmel, időszerű firmware és operációs rendszer frissítésekkel, valamint SELinux-xal [enforcing módban](https://source.android.com/security/selinux/concepts#enforcement_levels). Az általunk ajánlott összes Android disztribúció megfelel ezeknek a követelményeknek.

[Android rendszer ajánlásaink :material-arrow-right-drop-circle:](../android.md ""){.md-button}

### Kerüld a rootolást

[Az](https://en.wikipedia.org/wiki/Rooting_(Android)) Android telefonok rootolása jelentősen csökkentheti a biztonságot, mivel gyengíti a teljes [Android biztonsági modellt](https://en.wikipedia.org/wiki/Android_(operating_system)#Security_and_privacy). Ez csökkentheti az adatvédelmet, ha van olyan biztonsági rés, amelynek kihasználását a csökkent biztonság elősegíti. A gyakori rootolási módszerek a boot partíció közvetlen megváltoztatásával járnak, ami lehetetlenné teszi egy sikeres Verified Boot elvégzését. A root-ot igénylő alkalmazások szintén módosítják a rendszerpartíciót, ami azt jelenti, hogy a Verified Boot-nak kikapcsolva kell maradnia. A root közvetlen kitétele a felhasználói felületnek szintén növeli az eszközöd [támadási felületetét](https://en.wikipedia.org/wiki/Attack_surface) és elősegítheti [ jogosultságnöveléses](https://en.wikipedia.org/wiki/Privilege_escalation) sebezhetőségek véghezvitelét és az SELinux házirendek megkerülését.

Reklámblokkolók amik módosítják a[hosts fájlt](https://en.wikipedia.org/wiki/Hosts_(file)) (AdAway) és állandó root hozzáférést igénylő tűzfalak (AFWall+) veszélyesek, és nem használandók. Továbbá ezek nem a megfelelő módon oldják meg a rendeltetésüknek megfelelő feladatokat. Reklámblokkolás esetén inkább a titkosított [DNS](../dns.md), vagy [VPN](../vpn.md) szerver blokkoló megoldásokat javaslunk. A RethinkDNS, TrackerControl és az AdAway nem rootolt módban elfoglalja a VPN-helyet (egy helyi loopback VPN használatával), megakadályozva téged ezzel madatvédelmet fokozó szolgáltatások, például Orbot vagy egy valódi VPN szerver használatában.

Az AFWall+ a [csomagszűrő](https://en.wikipedia.org/wiki/Firewall_(computing)#Packet_filter) megközelítés alapján működik, és bizonyos helyzetekben megkerülhető.

Nem hisszük, hogy egy telefon rootolásával járó biztonsági áldozatok megérik az alkalmazások megkérdőjelezhető adatvédelmi előnyeit.

### Telepíts frissítéseket

Fontos, hogy ne használj egy [lejárt életciklusú](https://endoflife.date/android) Android verziót. Az Android újabb verziói nemcsak biztonsági frissítéseket kapnak az operációs rendszerhez, hanem fontos adatvédelmi fejlesztéseket is.

Például [Android 10 előtt](https://developer.android.com/about/versions/10/privacy/changes) a [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) engedéllyel rendelkező alkalmazások hozzáférhettek a telefon érzékeny és egyedi sorozatszámaihoz, mint például az [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier) vagy a SIM-kárty [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity)-jéhez; míg most már csak rendszeralkalmazások tehetik ezt meg. A rendszeralkalmazásokat csak az OEM vagy az Android disztribúció nyújtja.

### Média megosztása

Az Android beépített megosztási funkcióival elkerülheted, hogy több alkalmazásnak engedélyezd a médiához való hozzáférést. Több alkalmazás lehetővé teszi, hogy "megossz" egy fájlt velük médiafeltöltéshez.

Ha például egy képet szeretnél közzétenni Discordon, megnyithatod a fájlkezelőt vagy a galériát, és megoszthatod a képet a Discord alkalmazással, ahelyett, hogy teljes hozzáférést adnál a Discordnak a médiádhoz és a fényképeidhez.

## Biztonsági védelmek

### Verified Boot

A [Verified Boot](https://source.android.com/security/verifiedboot) az Android biztonsági modelljének egy fontos része. Védelmet nyújt az [evil maid](https://en.wikipedia.org/wiki/Evil_maid_attack) támadások, valamint rosszindulatú programok állandósulása ellen, és biztosítja a [rollback védelem](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection) segítségével, hogy a biztonsági frissítéseket ne lehessen downgradelni.

Az Android 10 és újabb verziói a teljes lemezes titkosítás helyett a rugalmasabb [fájlalapú titkosítást](https://source.android.com/security/encryption/file-based) használja. Az adataidat egyedi titkosítási kulcsok segítségével lesz titkosítva, az operációs rendszer fájljai pedig titkosítatlanok maradnak.

A Verified Boot biztosítja az operációs rendszerfájlok integritását, ezáltal megakadályozza, hogy egy fizikai hozzáféréssel rendelkező támadó változásokat hajtson létre, vagy rosszindulatú programot telepítsen az eszközre. Abban a valószínűtlen esetben, ha rosszindulatú szoftverek képesek kihasználni a rendszer más részeit, és magasabb jogosultságú hozzáférést szereznek, a Verified Boot megakadályozza és visszaállítja a rendszerpartíció változásait az eszköz újraindításakor.

Sajnos OEM-gyártók csak az Android alapkiadásánál kötelesek támogatni a Verified Bootot. Csak néhány OEM-gyártó, például a Google, támogatja az egyéni AVB-kulcsok felvételét az eszközein. Emellett néhány AOSP-változat, például a LineageOS vagy az /e/ OS nem támogatja a Verified Bootot még olyan hardvereken sem, amelyek támogatnák azt harmadik féltől származó operációs rendszereken. Javasoljuk, hogy tájékozódj ennek támogatottságáról ** még mielőtt** új készüléket vásárolnál. A Verified Bootot nem támogató AOSP-változatok **nem** ajánlottak.

Több OEM-gyártó is elrontotta a Verified Boot megvalósítását, amivel a marketingjükön túlmenően is tisztában kell lenned. A Fairphone 3 és 4 például alapértelmezetten nem biztonságosak, mivel az [alap bootloader a nyilvános AVB aláíró kulcsban bízik](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). Ez megtöri a verified bootot egy alapkiadású Fairphone készüléken, mivel a rendszer alternatív Android operációs rendszereket (például /e/) az egyéni operációs rendszerek használatáról szóló [figyelmeztetés nélkül](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) indítja el.

### Firmware-frissítések

A firmware-frissítések kritikus fontosságúak a biztonság fenntartása szempontjából, és nélkülük az eszközöd nem lehet biztonságos. Az OEM-gyártók támogatási megállapodásokat kötnek partnereikkel a zárt forráskódú komponensek korlátozott ideig történő biztosítására. Ezek a havonta megjelenő [Android Security Bulletin](https://source.android.com/security/bulletin)-ben vannak részletezve.

Mivel a telefon összetevői, például a processzor és a rádiótechnológiák zárt forráskódú komponensekre épülnek, a frissítéseket az adott gyártóknak kell biztosítaniuk. Ezért fontos, hogy olyan készüléket vásárolj ami rendelkezik aktív támogatási ciklussal. A [Qualcomm](https://www.qualcomm.com/news/releases/2020/12/16/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) és a [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox/) 4 évig támogatja készülékeit, míg az olcsóbb termékek gyakran rövidebb támogatási ciklusokkal rendelkeznek. A [Pixel 6](https://support.google.com/pixelphone/answer/4457705) bemutatásával a Google mostantól saját SoC-t készít, és legalább 5 év támogatást biztosít.

Az SoC gyártó által már nem támogatott, lejárt életciklusú eszközök nem kaphatnak firmware-frissítéseket OEM-gyártóktól vagy utángyártó Android-forgalmazóktól. Ez azt jelenti, hogy ezekkel az eszközökkel kapcsolatos biztonsági problémák javítatlanok maradnak.

A Fairphone például úgy forgalmazza készülékeit, hogy azok 6 évig kapnak támogatást. Az SoC (Qualcomm Snapdragon 750G a Fairphone 4-ben) azonban jóval rövidebb lejárati dátummal rendelkezik. Ez azt jelenti, hogy a Qualcomm által a Fairphone 4 számára biztosított firmware biztonsági frissítések 2023 szeptemberében véget érnek, függetlenül attól, hogy a Fairphone továbbra is kiad-e szoftveres biztonsági frissítéseket.

### Android engedélyek

[Engedélyek az Androidon](https://developer.android.com/guide/topics/permissions/overview) lehetővé teszik, hogy te szabályozd, az alkalmazások mihez férhetnek hozzá. A Google minden egyes verzióban rendszeresen ad ki javít [javításokat](https://developer.android.com/about/versions/11/privacy/permissions) az engedély rendszerhez. Minden telepített alkalmazás szigorúan [sandboxolva](https://source.android.com/security/app-sandbox) van, ezért nincs szükség vírusirtó alkalmazások telepítésére.

Egy okostelefon az Android legújabb verziójával mindig biztonságosabb lesz, mint egy régi okostelefon egy vírusirtóval, amelyért fizettél. Jobb, ha nem fizetsz vírusirtó szoftverért, és inkább spórolsz egy új okostelefonra, például egy Google Pixel-re.

Android 10:

- A [Scoped Storage](https://developer.android.com/about/versions/10/privacy/changes#scoped-storage) több ellenőrzést biztosít a fájljaid felett, és korlátozhatja, hogy mi férhet hozzá a [külső tárhelyhez](https://developer.android.com/training/data-storage#permissions). Az alkalmazások hozzáférhetnek egy adott könyvtárhoz a külső tárhelyen, valamint képesek lehetnek bizonyos típusú médiát tárolni ott.
- Szigorúbb hozzáférés az [eszköz helyadataihoz](https://developer.android.com/about/versions/10/privacy/changes#app-access-device-location) az `ACCESS_BACKGROUND_LOCATION` engedély bevezetésével. Ez megakadályozza, hogy a háttérben futó alkalmazások a felhasználó kifejezett engedélye nélkül hozzáférjenek a helyadatokhoz.

Android 11:

- [Egyszeri engedélyek](https://developer.android.com/about/versions/11/privacy/permissions#one-time), amelyek lehetővé teszik, hogy csak egy alkalom erejéig adj engedélyt egy alkalmazásnak.
- [Auto-reset permissions](https://developer.android.com/about/versions/11/privacy/permissions#auto-reset), which resets [runtime permissions](https://developer.android.com/guide/topics/permissions/overview#runtime) that were granted when the app was opened.
- Részletes jogosultságok a [telefonszámhoz](https://developer.android.com/about/versions/11/privacy/permissions#phone-numbers) kapcsolódó funkciók eléréséhez.

Android 12:

- Engedély megadása csak a [hozzávetőleges helyadatokhoz](https://developer.android.com/about/versions/12/behavior-changes-12#approximate-location).
- A [hibernált alkalmazások](https://developer.android.com/about/versions/12/behavior-changes-12#app-hibernation) automatikus visszaállítása.
- [Adathozzáférés-felülvizsálás](https://developer.android.com/about/versions/12/behavior-changes-12#data-access-auditing), amely megkönnyíti annak meghatározását, hogy az alkalmazás mely része végez egy adott típusú adathozzáférést.

Android 13:

- Engedély a [közeli wifi hozzáféréshez](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). A közeli WiFi hozzáférési pontok MAC-címei népszerű módja a felhasználó tartózkodási helyének nyomon követésére alkalmazások álltal.
- További [részletes médiaengedélyek](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions), ami azt jelenti, hogy csak képekhez, videókhoz vagy hangfájlokhoz adhatsz hozzáférést.
- Érzékelők háttérben történő használatához mostantól a [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission) engedély szükséges.

Egy alkalmazás engedélyt kérhet egy adott funkciójához. Például minden olyan alkalmazásnak, amely QR-kódokat tud beolvasni, szüksége van a kamera engedélyre. Egyes alkalmazások a szükségesnél több engedélyt kérhetnek.

Az [Exodus](https://exodus-privacy.eu.org/) hasznos lehet hasonló célú alkalmazások összehasonlításakor. Ha egy alkalmazás sok engedélyt igényel, valamint sok reklámot és elemzést tartalmaz, az valószínűleg egy rossz jel. Javasoljuk, hogy tekintsd meg az egyes nyomkövetőket és olvasd el a leírásukat, ahelyett, hogy egyszerűen **megszámolod az összeset** azt feltételezve, hogy a felsorolt tételek egyenlőek.

!!! warning

    Ha egy alkalmazás többnyire egy webalapú szolgáltatás, a nyomon követés történhet a szerveroldalon. A [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest/) azt mutatja, hogy "nincsenek nyomkövetők", de minden bizonnyal nyomon követi a felhasználók érdeklődését és viselkedését az oldalon. Alkalmazások elkerülhetik az észlelést azzal, hogy nem használják a reklámipar által készített szabványos kódkönyvtárakat, bár ez nem valószínű.

!!! note

    Az olyan magánélet-barát alkalmazások, mint a [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest/), megjeleníthetnek néhány nyomkövetőt, mint például a [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49/). Ez a könyvtár tartalmazza a [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging)-et, amely [push értesítéseket](https://en.wikipedia.org/wiki/Push_technology) tud nyújtani az alkalmazásoknak. Ez [a helyzet](https://fosstodon.org/@bitwarden/109636825700482007) a Bitwardennel is. Ez nem jelenti azt, hogy a Bitwarden a Google Firebase Analytics által biztosított összes elemzési funkciót használja.

## Adatvédelmi funkciók

### Felhasználói Profilok

Multiple user profiles can be found in **Settings** → **System** → **Multiple users** and are the simplest way to isolate in Android.

A felhasználói profilok segítségével korlátozásokat szabhatsz meg egy adott profilra vonatkozóan, például: hívások kezdeményezése, SMS használata vagy alkalmazások telepítése a készülékre. Minden profil a saját titkosítási kulcsával van titkosítva, és nem tud hozzáférni más profilok adataihoz. Még a készülék tulajdonosa sem tekintheti meg más profilok adatait a jelszó ismerete nélkül. A több felhasználói profil az izoláció biztonságosabb módja.

### Munkaprofil

A [Munkaprofilok](https://support.google.com/work/android/answer/6191949) egy másik módja egyes alkalmazások elkülönítésének, és kényelmesebb lehet, mint a különálló felhasználói profilok használata.

A **device controller** app such as [Shelter](../android.md#shelter) is required to create a Work Profile without an enterprise MDM, unless you're using a custom Android OS which includes one.

The work profile is dependent on a device controller to function. Features such as *File Shuttle* and *contact search blocking* or any kind of isolation features must be implemented by the controller. You must also fully trust the device controller app, as it has full access to your data inside of the work profile.

This method is generally less secure than a secondary user profile; however, it does allow you the convenience of running apps in both the work and personal profiles simultaneously.

### VPN Killswitch

Android 7 and above supports a VPN killswitch and it is available without the need to install third-party apps. This feature can prevent leaks if the VPN is disconnected. It can be found in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

### Global Toggles

Modern Android devices have global toggles for disabling Bluetooth and location services. Android 12 introduced toggles for the camera and microphone. When not in use, we recommend disabling these features. Apps cannot use disabled features (even if granted individual permission) until re-enabled.

## Google Services

If you are using a device with Google services, either your stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS, there are a number of additional changes you can make to improve your privacy. We still recommend avoiding Google services entirely, or limiting Google Play services to a specific user/work profile by combining a device controller like *Shelter* with GrapheneOS's Sandboxed Google Play.

### Advanced Protection Program

If you have a Google account we suggest enrolling in the [Advanced Protection Program](https://landing.google.com/advancedprotection/). It is available at no cost to anyone with two or more hardware security keys with [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) support.

The Advanced Protection Program provides enhanced threat monitoring and enables:

- Stricter two factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](https://en.wikipedia.org/wiki/OAuth)
- Only Google and verified third-party apps can access account data
- Scanning of incoming emails on Gmail accounts for [phishing](https://en.wikipedia.org/wiki/Phishing#Email_phishing) attempts
- Stricter [safe browser scanning](https://www.google.com/chrome/privacy/whitepaper.html#malware) with Google Chrome
- Stricter recovery process for accounts with lost credentials

 If you use non-sandboxed Google Play Services (common on stock operating systems), the Advanced Protection Program also comes with [additional benefits](https://support.google.com/accounts/answer/9764949?hl=en) such as:

- Not allowing app installation outside of the Google Play Store, the OS vendor's app store, or via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Mandatory automatic device scanning with [Play Protect](https://support.google.com/googleplay/answer/2812853?hl=en#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- Warning you about unverified applications

### Google Play System Updates

In the past, Android security updates had to be shipped by the operating system vendor. Android has become more modular beginning with Android 10, and Google can push security updates for **some** system components via the privileged Play Services.

If you have an EOL device shipped with Android 10 or above and are unable to run any of our recommended operating systems on your device, you are likely going to be better off sticking with your OEM Android installation (as opposed to an operating system not listed here such as LineageOS or /e/ OS). This will allow you to receive **some** security fixes from Google, while not violating the Android security model by using an insecure Android derivative and increasing your attack surface. We would still recommend upgrading to a supported device as soon as possible.

### Advertising ID

All devices with Google Play Services installed automatically generate an [advertising ID](https://support.google.com/googleplay/android-developer/answer/6048248?hl=en) used for targeted advertising. Disable this feature to limit the data collected about you.

On Android distributions with [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), go to :gear: **Settings** → **Apps** → **Sandboxed Google Play** → **Google Settings** → **Ads**, and select *Delete advertising ID*.

On Android distributions with privileged Google Play Services (such as stock OSes), the setting may be in one of several locations. Check

- :gear: **Settings** → **Google** → **Ads**
- :gear: **Settings** → **Privacy** → **Ads**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads*, this varies between OEM distributions of Android. If presented with the option to delete the advertising ID that is preferred. If not, then make sure to opt out and reset your advertising ID.

### SafetyNet and Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) and the [Play Integrity APIs](https://developer.android.com/google/play/integrity) are generally used for [banking apps](https://grapheneos.org/usage#banking-apps). Many banking apps will work fine in GrapheneOS with sandboxed Play services, however some non-financial apps have their own crude anti-tampering mechanisms which might fail. GrapheneOS passes the `basicIntegrity` check, but not the certification check `ctsProfileMatch`. Devices with Android 8 or later have hardware attestation support which cannot be bypassed without leaked keys or serious vulnerabilities.

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt-out if you don't want your credit rating and personal information shared with affiliate marketing services.
