---
title: Android Übersicht
icon: simple/android
description: Android ist ein Open-Source-Betriebssystem mit starken Sicherheitsvorkehrungen, was es zu unserer ersten Wahl für Handys macht.
---

![Android logo](../assets/img/android/android.svg){ align=right }

Das **Android Open-Source Project** ist ein sicheres mobiles Betriebssystem mit starkem [App-Sandboxing](https://source.android.com/security/app-sandbox), [Verified Boot](https://source.android.com/security/verifiedboot) (AVB) und einem robusten [Berechtigungskontrollsystem](https://developer.android.com/guide/topics/permissions/overview).

## Unsere Empfehlung

### Auswahl einer Android-Distribution

Wenn du ein Android-Handy kaufst, wird das Standard-Betriebssystem mit Apps und Funktionen ausgeliefert, die nicht Teil des Android Open Source Project sind. Viele dieser Apps - sogar Apps wie der Dialer, der grundlegende Systemfunktionen bereitstellt - erfordern invasive Integrationen mit Google Play Services, die wiederum Zugriffsrechte auf deine Dateien, Kontakte, Anrufliste, SMS-Nachrichten, Standort, Kamera, Mikrofon und zahlreiche andere Funktionen auf deinem Gerät verlangen, damit diese grundlegenden System-Apps und viele andere Apps überhaupt funktionieren. Frameworks wie Google Play Services erhöhen die Angriffsfläche deines Geräts und sind die Ursache für diverse Datenschutzprobleme bei Android.

Dieses Problem könnte durch die Verwendung einer Custom-Android-Distribution gelöst werden, die nicht mit einer derartigen invasiven Integration einhergeht. Leider verletzen viele Custom-Android-Distributionen oft das Android-Sicherheitsmodell, indem sie kritische Sicherheitsfunktionen wie AVB, Rollback-Schutz, Firmware-Updates usw. nicht unterstützen. Einige Distributionen liefern auch [`userdebug`](https://source.android.com/setup/build/building#choose-a-target)-Builds, die Root über [ADB](https://developer.android.com/studio/command-line/adb) freigeben und [freizügigere](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) SELinux-Richtlinien erfordern, um Debugging-Funktionen zu ermöglichen, was zu einer noch größeren Angriffsfläche und einem schwächeren Sicherheitsmodell führt.

Idealerweise solltest du bei der Auswahl einer Custom-Android-Distribution sicherstellen, dass sie das Android-Sicherheitsmodell einhält. Zumindest sollte die Distribution Produktions-Builds, Unterstützung für AVB, Rollback-Schutz, rechtzeitige Firmware- und Betriebssystem-Updates und SELinux im [Enforcing-Modus](https://source.android.com/security/selinux/concepts#enforcement_levels) bieten. Alle unsere empfohlenen Android-Distributionen erfüllen diese Kriterien.

[Unsere Android-System-Empfehlungen :material-arrow-right-drop-circle:](../android/distributions.md ""){.md-button}

### Vermeide Rooten

Das [Rooten](https://de.wikipedia.org/wiki/Rooten) von Android-Handys kann die Sicherheit erheblich beeinträchtigen, da es das gesamte [Android-Sicherheitsmodell](https://de.wikipedia.org/wiki/Android_(Betriebssystem)#Sicherheit) schwächt. Dies kann zu einer Beeinträchtigung des Datenschutzes führen, wenn die verminderte Sicherheit ausgenutzt wird. Bei den üblichen Rooting-Methoden wird direkt in die Boot-Partition eingegriffen, sodass ein erfolgreicher Verified Boot nicht möglich ist. Anwendungen, die Root benötigen, verändern auch die Systempartition, was bedeutet, dass Verified Boot deaktiviert bleiben muss. Das direkte Aussetzen von Root in der Benutzeroberfläche erhöht ebenfalls die [Angriffsfläche](https://en.wikipedia.org/wiki/Attack_surface) deines Geräts und kann bei [Rechteausweitung](https://de.wikipedia.org/wiki/Rechteausweitung) und SELinux-Richtlinienumgehungen helfen.

Inhaltsblocker, die die [hosts Datei](https://de.wikipedia.org/wiki/Hosts_(Datei)) verändern (AdAway), und Firewalls (AFWall+), welche dauerhaft Root-Zugriff erfordern, sind gefährlich und sollten nicht verwendet werden. Sie sind auch nicht der richtige Weg, um den beabsichtigten Zweck zu erfüllen. Für das Blockieren von Inhalten empfehlen wir stattdessen verschlüsselte [DNS](../dns.md) oder die Inhaltsblockierungsfunktionen, die von einem VPN bereitgestellt werden. TrackerControl und AdAway im Nicht-Root-Modus nehmen den VPN-Slot ein (indem sie ein lokales Loopback-VPN verwenden) und verhindern so, dass du datenschutzfreundliche Dienste wie [Orbot](../tor.md#orbot) oder einen [echten VPN-Anbieter](../vpn.md) nutzen kannst.

AFWall+ basiert auf dem Ansatz der [Paketfilterung](https://en.wikipedia.org/wiki/Firewall_(computing)#Packet_filter) und kann in einigen Situationen umgangen werden.

Wir sind nicht der Meinung, dass die Sicherheitseinbußen, die durch das Rooten eines Smartphones entstehen, die fragwürdigen Datenschutzvorteile dieser Anwendungen wert sind.

### Installiere Updates

Es ist wichtig, dass du keine [veraltete](https://endoflife.date/android) Version von Android verwendest. Neuere Android-Versionen erhalten nicht nur Sicherheitsupdates für das Betriebssystem, sondern auch wichtige Updates zur Verbesserung der Privatsphäre.

[Vor Android 10](https://developer.android.com/about/versions/10/privacy/changes) konnten alle Apps mit der [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) Berechtigung auf sensible und eindeutige Seriennumern deines Handys zugreifen, wie [IMEI](https://de.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier) oder die [IMSI](https://de.wikipedia.org/wiki/International_Mobile_Subscriber_Identity) deiner SIM-Karte, während es sich jetzt um System-Apps handeln muss, um dies zu tun. Systemanwendungen werden nur vom OEM oder der Android-Distribution bereitgestellt.

### Medien teilen

Du kannst vermeiden, vielen Apps die Berechtigung zum Zugriff auf deine Medien zu gewähren, indem du die integrierten Freigabefunktionen von Android nutzt. Viele Apps ermöglichen es dir, eine Datei mit ihnen zu „teilen“ für den Medien-Upload.

Wenn du beispielsweise ein Bild in Discord posten möchtest, kannst du deinen Dateimanager oder deine Galerie öffnen und dieses Bild mit der Discord-App teilen, anstatt Discord vollen Zugriff auf deine Medien und Fotos zu gewähren.

## Sicherheitsmaßnahmen

Zu den Schlüsselkomponenten des Android-Sicherheitsmodells gehören [Verified Boot](#verified-boot), [Firmware-Updates](#firmware-updates) und ein robustes [Berechtigungssystem](#android-permissions). Diese wichtigen Sicherheitsmaßnahmen bilden die Grundlage der Mindestkriterien für unsere Empfehlungen für [Mobiltelefone](../mobile-phones.md) und [Custom-Android-OS](../android/distributions.md).

### Verified Boot

[**Verified Boot**](https://source.android.com/security/verifiedboot) ist ein elementarer Bestandteil des Android-Sicherheitsmodells. Es bietet Schutz vor [Evil Maid Angriffen](https://en.wikipedia.org/wiki/Evil_maid_attack), Malware-Persistenz und stellt sicher, dass Sicherheitsupdates nicht durch [Rollback-Schutz](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection) herbagestuft werden können.

Android 10 and above has moved away from full-disk encryption to more flexible [file-based encryption](https://source.android.com/security/encryption/file-based). Your data is encrypted using unique encryption keys, and the operating system files are left unencrypted.

Verified Boot ensures the integrity of the operating system files, thereby preventing an adversary with physical access from tampering or installing malware on the device. In the unlikely case that malware is able to exploit other parts of the system and gain higher privileged access, Verified Boot will prevent and revert changes to the system partition upon rebooting the device.

Unfortunately, OEMs are only obliged to support Verified Boot on their stock Android distribution. Only a few OEMs such as Google support custom AVB key enrollment on their devices. Additionally, some AOSP derivatives such as LineageOS or /e/ OS do not support Verified Boot even on hardware with Verified Boot support for third-party operating systems. We recommend that you check for support **before** purchasing a new device. AOSP derivatives which do not support Verified Boot are **not** recommended.

Many OEMs also have broken implementation of Verified Boot that you have to be aware of beyond their marketing. For example, the Fairphone 3 and 4 are not secure by default, as the [stock bootloader trusts the public AVB signing key](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). This breaks verified boot on a stock Fairphone device, as the system will boot alternative Android operating systems (such as /e/) [without any warning](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) about custom operating system usage.

### Firmware Updates

**Firmware updates** are critical for maintaining security and without them your device cannot be secure. OEMs have support agreements with their partners to provide the closed-source components for a limited support period. These are detailed in the monthly [Android Security Bulletins](https://source.android.com/security/bulletin).

As the components of the phone, such as the processor and radio technologies rely on closed-source components, the updates must be provided by the respective manufacturers. Therefore, it is important that you purchase a device within an active support cycle. [Qualcomm](https://www.qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) and [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox) support their devices for 4 years, while cheaper products often have shorter support cycles. With the introduction of the [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google now makes their own SoC, and they will provide a minimum of 5 years of support. With the introduction of the Pixel 8 series, Google increased that support window to 7 years.

EOL devices which are no longer supported by the SoC manufacturer cannot receive firmware updates from OEM vendors or after market Android distributors. This means that security issues with those devices will remain unfixed.

Fairphone, for example, markets their Fairphone 4 device as receiving 6 years of support. However, the SoC (Qualcomm Snapdragon 750G on the Fairphone 4) has a considerably shorter EOL date. This means that firmware security updates from Qualcomm for the Fairphone 4 will end in September 2023, regardless of whether Fairphone continues to release software security updates.

### Android Permissions

[**Permissions on Android**](https://developer.android.com/guide/topics/permissions/overview) grant you control over what apps are allowed to access. Google regularly makes [improvements](https://developer.android.com/about/versions/11/privacy/permissions) on the permission system in each successive version. All apps you install are strictly [sandboxed](https://source.android.com/security/app-sandbox), therefore, there is no need to install any antivirus apps.

A smartphone with the latest version of Android will always be more secure than an old smartphone with an antivirus that you have paid for. It's better not to pay for antivirus software and to save money to buy a new smartphone such as a [Google Pixel](../mobile-phones.md#google-pixel).

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

- A permission for [nearby Wi-Fi access](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). The MAC addresses of nearby Wi-Fi access points were a popular way for apps to track a user's location.
- More [granular media permissions](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions), meaning you can grant access to images, videos or audio files only.
- Background use of sensors now requires the [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission) permission.

An app may request a permission for a specific feature it has. For example, any app that can scan QR codes will require the camera permission. Some apps can request more permissions than they need.

[Exodus](https://exodus-privacy.eu.org) can be useful when comparing apps that have similar purposes. If an app requires a lot of permissions and has a lot of advertising and analytics this is probably a bad sign. We recommend looking at the individual trackers and reading their descriptions rather than simply **counting the total** and assuming all items listed are equal.

<div class="admonition warning" markdown>
<p class="admonition-title">Warnung</p>

If an app is mostly a web-based service, the tracking may occur on the server side. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest) shows "no trackers" but certainly does track users' interests and behavior across the site. Apps may evade detection by not using standard code libraries produced by the advertising industry, though this is unlikely.

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Privacy-friendly apps such as [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest) may show some trackers such as [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49). This library includes [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) which can provide [push notifications](https://en.wikipedia.org/wiki/Push_technology) in apps. This [is the case](https://fosstodon.org/@bitwarden/109636825700482007) with Bitwarden. That doesn't mean that Bitwarden is using all of the analytics features that are provided by Google Firebase Analytics.

</div>

## Privacy Features

### User Profiles

Multiple user profiles can be found in **Settings** → **System** → **Multiple users** and are the simplest way to isolate in Android.

With user profiles, you can impose restrictions on a specific profile, such as: making calls, using SMS, or installing apps on the device. Each profile is encrypted using its own encryption key and cannot access the data of any other profiles. Even the device owner cannot view the data of other profiles without knowing their password. Multiple user profiles are a more secure method of isolation.

### Work Profile

[Work Profiles](https://support.google.com/work/android/answer/6191949) are another way to isolate individual apps and may be more convenient than separate user profiles.

A **device controller** app such as [Shelter](../android/general-apps.md#shelter) is required to create a Work Profile without an enterprise MDM, unless you're using a custom Android OS which includes one.

The work profile is dependent on a device controller to function. Features such as *File Shuttle* and *contact search blocking* or any kind of isolation features must be implemented by the controller. You must also fully trust the device controller app, as it has full access to your data inside the work profile.

This method is generally less secure than a secondary user profile; however, it does allow you the convenience of running apps in both the work and personal profiles simultaneously.

### VPN Kill-Switch

Android 7 und höher unterstützt einen VPN-Kill-Switch, der ohne die Installation von Drittanbieter-Apps verfügbar ist. Diese Funktion kann Leaks verhindern, wenn die VPN-Verbindung unterbrochen wird. Du findest sie unter :gear: **Einstellungen** → **Netzwerk & Internet** → **VPN** → :gear: → **Verbindungen ohne VPN blockieren**.

### Global Toggles

Modern Android devices have global toggles for disabling Bluetooth and location services. Android 12 introduced toggles for the camera and microphone. When not in use, we recommend disabling these features. Apps cannot use disabled features (even if granted individual permissions) until re-enabled.

## Google-Dienste

If you are using a device with Google services—whether with the stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS—there are a number of additional changes you can make to improve your privacy. We still recommend avoiding Google services entirely, or limiting Google Play services to a specific user/work profile by combining a device controller like *Shelter* with GrapheneOS's Sandboxed Google Play.

### Advanced Protection Program

If you have a Google account we suggest enrolling in the [Advanced Protection Program](https://landing.google.com/advancedprotection). It is available at no cost to anyone with two or more hardware security keys with [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) support. Alternatively, you can use [passkeys](https://fidoalliance.org/passkeys).

The Advanced Protection Program provides enhanced threat monitoring and enables:

- Stricter two-factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](https://en.wikipedia.org/wiki/OAuth)
- Only Google and verified third-party apps can access account data
- Scanning of incoming emails on Gmail accounts for [phishing](https://en.wikipedia.org/wiki/Phishing#Email_phishing) attempts
- Stricter [safe browser scanning](https://google.com/chrome/privacy/whitepaper.html#malware) with Google Chrome
- Stricter recovery process for accounts with lost credentials

 If you use non-sandboxed Google Play Services (common on stock operating systems), the Advanced Protection Program also comes with [additional benefits](https://support.google.com/accounts/answer/9764949) such as:

- Not allowing app installation outside the Google Play Store, the OS vendor's app store, or via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Mandatory automatic device scanning with [Play Protect](https://support.google.com/googleplay/answer/2812853?#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- Warning you about unverified applications

### Google Play System Updates

In the past, Android security updates had to be shipped by the operating system vendor. Android has become more modular beginning with Android 10, and Google can push security updates for **some** system components via the privileged Play Services.

If you have an EOL device shipped with Android 10 or above and are unable to run any of our recommended operating systems on your device, you are likely going to be better off sticking with your OEM Android installation (as opposed to an operating system not listed here such as LineageOS or /e/ OS). This will allow you to receive **some** security fixes from Google, while not violating the Android security model by using an insecure Android derivative and increasing your attack surface. We would still recommend upgrading to a supported device as soon as possible.

### Advertising ID

All devices with Google Play Services installed automatically generate an [advertising ID](https://support.google.com/googleplay/android-developer/answer/6048248) used for targeted advertising. Disable this feature to limit the data collected about you.

On Android distributions with [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), go to :gear: **Settings** → **Apps** → **Sandboxed Google Play** → **Google Settings** → **Ads**, and select *Delete advertising ID*.

On Android distributions with privileged Google Play Services (such as stock OSes), the setting may be in one of several locations. Check

- :gear: **Settings** → **Google** → **Ads**
- :gear: **Settings** → **Privacy** → **Ads**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads* (this varies between OEM distributions of Android). If presented with the option to delete the advertising ID, that is preferred. If not, then make sure to opt out and reset your advertising ID.

### SafetyNet and Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) and the [Play Integrity APIs](https://developer.android.com/google/play/integrity) are generally used for [banking apps](https://grapheneos.org/usage#banking-apps). Many banking apps will work fine in GrapheneOS with sandboxed Play services, however some non-financial apps have their own crude anti-tampering mechanisms which might fail. GrapheneOS passes the `basicIntegrity` check, but not the certification check `ctsProfileMatch`. Devices with Android 8 or later have hardware attestation support which cannot be bypassed without leaked keys or serious vulnerabilities.

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt out if you don't want your credit rating and personal information shared with affiliate marketing services.
