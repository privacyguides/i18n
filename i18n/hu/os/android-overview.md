---
title: Android Áttekintés
icon: simple/android
description: Az Android egy nyílt forráskódú operációs rendszer, amely erős biztonsági védelemmel rendelkezik, ezért ez az elsődleges választásunk telefonok esetében.
---

Az Android egy biztonságos operációs rendszer, amely erős [app sandboxoló](https://source.android.com/security/app-sandbox), [Verified Boot](https://source.android.com/security/verifiedboot) (AVB) és egy robusztus [engedély](https://developer.android.com/guide/topics/permissions/overview) ellenőrző rendszerrel rendelkezik.

## Egy Android Disztribúció Kiválasztása

Egy Android telefon vásárlásakor a készülék alapértelmezett operációs rendszere gyakran olyan alkalmazások és szolgáltatások invazív integrációját tartalmazza, amelyek nem részei az [Android Open-Source Project](https://source.android.com/)-nek. Ilyen például a Google Play Szolgáltatások, amely visszavonhatatlan jogosultságokkal rendelkezik a fájljaidhoz, névjegy tárolódhoz, hívásnaplóidhoz, SMS-üzeneteidhez, tartózkodási helyedhez, kamerádhoz, mikrofonodhoz, hardverazonosítóidhoz, stb. való hozzáférésre. Ezek az alkalmazások és szolgáltatások növelik a készüléked támadási felületét, és számos adatvédelmi aggály forrását jelentik az Androiddal kapcsolatban.

Ez a probléma megoldható lehet egy olyan egyedi Android-disztribúció használatával, amely nem tartalmaz ilyen invazív integrációkat. Sajnos sok egyedi Android disztribúció gyakran megsérti az Android biztonsági modellt azzal, hogy nem támogat olyan kritikus biztonsági funkciókat, mint az AVB, a rollback védelem, firmware-frissítések, stb. Egyes disztribúciók [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) buildeket nyújtanak, amelyek védtelenné teszik a root-ot az [ADB](https://developer.android.com/studio/command-line/adb)-n keresztül és [több engedélyt biztosító](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) SELinux policy-kat igényelnek a hibakeresési funkciókhoz, ami tovább növeli a támadási felületet és gyengébb biztonsági modellt eredményez.

Ideális esetben, amikor egyedi Android disztribúciót választasz, győződj meg arról, hogy az, az Android biztonsági modellt követi. A disztribúciónak minimum rendelkeznie kell gyártási buildekkel, AVB támogatással, rollback védelemmel, időszerű firmware és operációs rendszer frissítésekkel, valamint SELinux-xal [enforcing módban](https://source.android.com/security/selinux/concepts#enforcement_levels). Az általunk ajánlott összes Android disztribúció megfelel ezeknek a követelményeknek.

[Android Rendszer Ajánlásaink :hero-arrow-circle-right-fill:](../android.md ""){.md-button}

## Kerüld a Rootolást

[Az](https://en.wikipedia.org/wiki/Rooting_(Android)) Android telefonok rootolása jelentősen csökkentheti a biztonságot, mivel gyengíti a teljes [Android biztonsági modellt](https://en.wikipedia.org/wiki/Android_(operating_system)#Security_and_privacy). Ez csökkentheti az adatvédelmet, ha van olyan biztonsági rés, amelynek kihasználását a csökkent biztonság elősegíti. A gyakori rootolási módszerek a boot partíció közvetlen megváltoztatásával járnak, ami lehetetlenné teszi egy sikeres Verified Boot elvégzését. A root-ot igénylő alkalmazások szintén módosítják a rendszerpartíciót, ami azt jelenti, hogy a Verified Boot-nak kikapcsolva kell maradnia. A root közvetlen kitétele a felhasználói felületnek szintén növeli az eszközöd [támadási felületetét](https://en.wikipedia.org/wiki/Attack_surface) és elősegítheti [ jogosultságnöveléses](https://en.wikipedia.org/wiki/Privilege_escalation) sebezhetőségek véghezvitelét és az SELinux házirendek megkerülését.

Reklámblokkolók amik módosítják a[hosts fájlt](https://en.wikipedia.org/wiki/Hosts_(file)) (AdAway) és állandó root hozzáférést igénylő tűzfalak (AFWall+) veszélyesek, és nem használandók. Továbbá ezek nem a megfelelő módon oldják meg a rendeltetésüknek megfelelő feladatokat. Reklámblokkolás esetén inkább a titkosított [DNS](../dns.md), vagy [VPN](../vpn.md) szerver blokkoló megoldásokat javaslunk. A RethinkDNS, TrackerControl és az AdAway nem rootolt módban elfoglalja a VPN-helyet (egy helyi loopback VPN használatával), megakadályozva téged ezzel madatvédelmet fokozó szolgáltatások, például Orbot vagy egy valódi VPN szerver használatában.

Az AFWall+ a [csomagszűrő](https://en.wikipedia.org/wiki/Firewall_(computing)#Packet_filter) megközelítés alapján működik, és bizonyos helyzetekben megkerülhető.

Nem hisszük, hogy egy telefon rootolásával járó biztonsági áldozatok megérik az alkalmazások megkérdőjelezhető adatvédelmi előnyeit.

## Verified Boot

A [Verified Boot](https://source.android.com/security/verifiedboot) az Android biztonsági modelljének egy fontos része. Védelmet nyújt az [evil maid](https://en.wikipedia.org/wiki/Evil_maid_attack) támadások, valamint rosszindulatú programok állandósulása ellen, és biztosítja a [rollback védelem](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection) segítségével, hogy a biztonsági frissítéseket ne lehessen downgradelni.

Az Android 10 és újabb verziói a teljes lemezes titkosítás helyett a rugalmasabb [fájlalapú titkosítást](https://source.android.com/security/encryption/file-based) használja. Az adataidat egyedi titkosítási kulcsok segítségével lesz titkosítva, az operációs rendszer fájljai pedig titkosítatlanok maradnak.

A Verified Boot biztosítja az operációs rendszerfájlok integritását, ezáltal megakadályozza, hogy egy fizikai hozzáféréssel rendelkező támadó változásokat hajtson létre, vagy rosszindulatú programot telepítsen az eszközre. Abban a valószínűtlen esetben, ha rosszindulatú szoftverek képesek kihasználni a rendszer más részeit, és magasabb jogosultságú hozzáférést szereznek, a Verified Boot megakadályozza és visszaállítja a rendszerpartíció változásait az eszköz újraindításakor.

Sajnos OEM-gyártók csak az Android alapkiadásánál kötelesek támogatni a Verified Bootot. Csak néhány OEM-gyártó, például a Google, támogatja az egyéni AVB-kulcsok felvételét az eszközein. Emellett néhány AOSP-változat, például a LineageOS vagy az /e/ OS nem támogatja a Verified Bootot még olyan hardvereken sem, amelyek támogatnák azt harmadik féltől származó operációs rendszereken. Javasoljuk, hogy tájékozódj ennek támogatottságáról ** még mielőtt** új készüléket vásárolnál. A Verified Bootot nem támogató AOSP-változatok **nem** ajánlottak.

Több OEM-gyártó is elrontotta a Verified Boot megvalósítását, amivel a marketingjükön túlmenően is tisztában kell lenned. A Fairphone 3 és 4 például alapértelmezetten nem biztonságosak, mivel az [alap bootloader a nyilvános AVB aláíró kulcsban bízik](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). This breaks verified boot on a stock Fairphone device, as the system will boot alternative Android operating systems such (such as /e/) [without any warning](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) about custom operating system usage.

## Firmware Updates

Firmware updates are critical for maintaining security and without them your device cannot be secure. OEMs have support agreements with their partners to provide the closed-source components for a limited support period. These are detailed in the monthly [Android Security Bulletins](https://source.android.com/security/bulletin).

As the components of the phone, such as the processor and radio technologies rely on closed-source components, the updates must be provided by the respective manufacturers. Therefore, it is important that you purchase a device within an active support cycle. [Qualcomm](https://www.qualcomm.com/news/releases/2020/12/16/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) and [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox/) support their devices for 4 years, while cheaper products often have shorter support cycles. With the introduction of the [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google now makes their own SoC and they will provide a minimum of 5 years of support.

EOL devices which are no longer supported by the SoC manufacturer cannot receive firmware updates from OEM vendors or after market Android distributors. This means that security issues with those devices will remain unfixed.

Fairphone, for example, markets their devices as receiving 6 years of support. However, the SoC (Qualcomm Snapdragon 750G on the Fairphone 4) has a considerably shorter EOL date. This means that firmware security updates from Qualcomm for the Fairphone 4 will end in September 2023, regardless of whether Fairphone continues to release software security updates.

## Android Versions

It's important to not use an [end-of-life](https://endoflife.date/android) version of Android. Newer versions of Android not only receive security updates for the operating system but also important privacy enhancing updates too. For example, [prior to Android 10](https://developer.android.com/about/versions/10/privacy/changes), any apps with the [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) permission could access sensitive and unique serial numbers of your phone such as [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), your SIM card's [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity), whereas now they must be system apps to do so. System apps are only provided by the OEM or Android distribution.

## Android Permissions

[Permissions on Android](https://developer.android.com/guide/topics/permissions/overview) grant you control over what apps are allowed to access. Google regularly makes [improvements](https://developer.android.com/about/versions/11/privacy/permissions) on the permission system in each successive version. All apps you install are strictly [sandboxed](https://source.android.com/security/app-sandbox), therefore, there is no need to install any antivirus apps.

A smartphone with the latest version of Android will always be more secure than an old smartphone with an antivirus that you have paid for. It's better not to pay for antivirus software and to save money to buy a new smartphone such as a Google Pixel.

Android 10:

- [Scoped Storage](https://developer.android.com/about/versions/10/privacy/changes#scoped-storage) gives you more control over your files and can limit what can [access external storage](https://developer.android.com/training/data-storage#permissions). Apps can have a specific directory in external storage as well as the ability to store specific types of media there.
- Tighter access on [device location](https://developer.android.com/about/versions/10/privacy/changes#app-access-device-location) by introducing the `ACCESS_BACKGROUND_LOCATION` permission. This prevents apps from accessing the location when running in the background without express permission from the user.

Android 11:

- [One-time permissions](https://developer.android.com/about/versions/11/privacy/permissions#one-time) which allows you to grant a permission to an app just once.
- [Auto-reset permissions](https://developer.android.com/about/versions/11/privacy/permissions#auto-reset), which resets [runtime permissions](https://developer.android.com/guide/topics/permissions/overview#runtime) that were granted when the app was opened.
- Granular permissions for accessing [phone number](https://developer.android.com/about/versions/11/privacy/permissions#phone-numbers) related features.

Android 12:

- A permission to grant only the [approximate location](https://developer.android.com/about/versions/12/behavior-changes-12#approximate-location).
- Auto-reset of [hibernated apps](https://developer.android.com/about/versions/12/behavior-changes-12#app-hibernation).
- [Data access auditing](https://developer.android.com/about/versions/12/behavior-changes-12#data-access-auditing) which makes it easier to determine what part of an app is performing a specific type of data access.

Android 13:

- A permission for [nearby wifi access](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). The MAC addresses of nearby WiFi access points was a popular way for apps to track a user's location.
- More [granular media permissions](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions), meaning you can grant access to images, videos or audio files only.
- Background use of sensors now requires the [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission) permission.

An app may request a permission for a specific feature it has. For example, any app that can scan QR codes will require the camera permission. Some apps can request more permissions than they need.

[Exodus](https://exodus-privacy.eu.org/) can be useful when comparing apps that have similar purposes. If an app requires a lot of permissions and has a lot of advertising and analytics this is probably a bad sign. We recommend looking at the individual trackers and reading their descriptions rather than simply **counting the total** and assuming all items listed are equal.

!!! warning

    If an app is mostly a web-based service, the tracking may occur on the server side. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest/) shows "no trackers" but certainly does track users' interests and behavior across the site. Apps may evade detection by not using standard code libraries produced by the advertising industry, though this is unlikely.

!!! note

    Privacy-friendly apps such as [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest/) may show some trackers such as [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49/). This library includes [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) which can provide [push notifications](https://en.wikipedia.org/wiki/Push_technology) in apps. This [is the case](https://fosstodon.org/@bitwarden/109636825700482007) with Bitwarden. That doesn't mean that Bitwarden is using all of the analytics features that are provided by Google Firebase Analytics.

## Media Access

Quite a few applications allows you to "share" a file with them for media upload. If you want to, for example, tweet a picture to Twitter, do not grant Twitter access to your "media and photos", because it will have access to all of your pictures then. Instead, go to your file manager (documentsUI), hold onto the picture, then share it with Twitter.

## User Profiles

Multiple user profiles can be found in **Settings** → **System** → **Multiple users** and are the simplest way to isolate in Android.

With user profiles, you can impose restrictions on a specific profile, such as: making calls, using SMS, or installing apps on the device. Each profile is encrypted using its own encryption key and cannot access the data of any other profiles. Even the device owner cannot view the data of other profiles without knowing their password. Multiple user profiles are a more secure method of isolation.

## Work Profile

[Work Profiles](https://support.google.com/work/android/answer/6191949) are another way to isolate individual apps and may be more convenient than separate user profiles.

A **device controller** app such as [Shelter](#recommended-apps) is required to create a Work Profile without an enterprise MDM, unless you're using a custom Android OS which includes one.

The work profile is dependent on a device controller to function. Features such as *File Shuttle* and *contact search blocking* or any kind of isolation features must be implemented by the controller. You must also fully trust the device controller app, as it has full access to your data inside of the work profile.

This method is generally less secure than a secondary user profile; however, it does allow you the convenience of running apps in both the work and personal profiles simultaneously.

## VPN Killswitch

Android 7 and above supports a VPN killswitch and it is available without the need to install third-party apps. This feature can prevent leaks if the VPN is disconnected. It can be found in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

## Global Toggles

Modern Android devices have global toggles for disabling Bluetooth and location services. Android 12 introduced toggles for the camera and microphone. When not in use, we recommend disabling these features. Apps cannot use disabled features (even if granted individual permission) until re-enabled.

## Google

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
