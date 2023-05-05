---
title: Android 개요
icon: simple/android
description: Android는 강력한 보안 및 보호 기능을 갖춘 오픈 소스 운영 체제로, 휴대폰에 있어서 최고의 선택입니다.
---

Android is a secure operating system that has strong [app sandboxing](https://source.android.com/security/app-sandbox), [Verified Boot](https://source.android.com/security/verifiedboot) (AVB), and a robust [permission](https://developer.android.com/guide/topics/permissions/overview) control system.

## Choosing an Android Distribution

When you buy an Android phone, the device's default operating system often comes with invasive integration with apps and services that are not part of the [Android Open-Source Project](https://source.android.com/). An example of such is Google Play Services, which has irrevocable privileges to access your files, contacts storage, call logs, SMS messages, location, camera, microphone, hardware identifiers, and so on. These apps and services increase the attack surface of your device and are the source of various privacy concerns with Android.

This problem could be solved by using a custom Android distribution that does not come with such invasive integration. Unfortunately, many custom Android distributions often violate the Android security model by not supporting critical security features such as AVB, rollback protection, firmware updates, and so on. Some distributions also ship [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) builds which expose root via [ADB](https://developer.android.com/studio/command-line/adb) and require [more permissive](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) SELinux policies to accommodate debugging features, resulting in a further increased attack surface and weakened security model.

Ideally, when choosing a custom Android distribution, you should make sure that it upholds the Android security model. At the very least, the distribution should have production builds, support for AVB, rollback protection, timely firmware and operating system updates, and SELinux in [enforcing mode](https://source.android.com/security/selinux/concepts#enforcement_levels). All of our recommended Android distributions satisfy these criteria.

[Our Android System Recommendations :material-arrow-right-drop-circle:](../android.md ""){.md-button}

## Avoid Rooting

[Rooting](https://en.wikipedia.org/wiki/Rooting_(Android)) Android phones can decrease security significantly as it weakens the complete [Android security model](https://en.wikipedia.org/wiki/Android_(operating_system)#Security_and_privacy). This can decrease privacy should there be an exploit that is assisted by the decreased security. Common rooting methods involve directly tampering with the boot partition, making it impossible to perform successful Verified Boot. Apps that require root will also modify the system partition meaning that Verified Boot would have to remain disabled. Having root exposed directly in the user interface also increases the [attack surface](https://en.wikipedia.org/wiki/Attack_surface) of your device and may assist in [privilege escalation](https://en.wikipedia.org/wiki/Privilege_escalation) vulnerabilities and SELinux policy bypasses.

Adblockers, which modify the [hosts file](https://en.wikipedia.org/wiki/Hosts_(file)) (AdAway) and firewalls (AFWall+) which require root access persistently are dangerous and should not be used. They are also not the correct way to solve their intended purposes. For Adblocking we suggest encrypted [DNS](../dns.md) or [VPN](../vpn.md) server blocking solutions instead. RethinkDNS, TrackerControl and AdAway in non-root mode will take up the VPN slot (by using a local loopback VPN) preventing you from using privacy enhancing services such as Orbot or a real VPN server.

AFWall+ works based on the [packet filtering](https://en.wikipedia.org/wiki/Firewall_(computing)#Packet_filter) approach and may be bypassable in some situations.

We do not believe that the security sacrifices made by rooting a phone are worth the questionable privacy benefits of those apps.

## 자체 검사 부팅

[자체 검사 부팅(Verified Boot)](https://source.android.com/security/verifiedboot)은 Android 보안 모델에서 중요한 부분을 차지하고 있습니다. [Evil maid](https://en.wikipedia.org/wiki/Evil_maid_attack) 공격, 멀웨어 지속성으로부터 보호하고, [롤백 보호](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection)를 통해 보안 업데이트가 다운그레이드되는 일이 없도록 보장합니다.

Android 10 and above has moved away from full-disk encryption to more flexible [file-based encryption](https://source.android.com/security/encryption/file-based). Your data is encrypted using unique encryption keys, and the operating system files are left unencrypted.

Verified Boot ensures the integrity of the operating system files, thereby preventing an adversary with physical access from tampering or installing malware on the device. In the unlikely case that malware is able to exploit other parts of the system and gain higher privileged access, Verified Boot will prevent and revert changes to the system partition upon rebooting the device.

Unfortunately, OEMs are only obliged to support Verified Boot on their stock Android distribution. Only a few OEMs such as Google support custom AVB key enrollment on their devices. Additionally, some AOSP derivatives such as LineageOS or /e/ OS do not support Verified Boot even on hardware with Verified Boot support for third-party operating systems. We recommend that you check for support **before** purchasing a new device. AOSP derivatives which do not support Verified Boot are **not** recommended.

Many OEMs also have broken implementation of Verified Boot that you have to be aware of beyond their marketing. For example, the Fairphone 3 and 4 are not secure by default, as the [stock bootloader trusts the public AVB signing key](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). This breaks verified boot on a stock Fairphone device, as the system will boot alternative Android operating systems such (such as /e/) [without any warning](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) about custom operating system usage.

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

!!! warning "경고"

    If an app is mostly a web-based service, the tracking may occur on the server side. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest/) shows "no trackers" but certainly does track users' interests and behavior across the site. Apps may evade detection by not using standard code libraries produced by the advertising industry, though this is unlikely.

!!! note

    Privacy-friendly apps such as [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest/) may show some trackers such as [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49/). This library includes [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) which can provide [push notifications](https://en.wikipedia.org/wiki/Push_technology) in apps. This [is the case](https://fosstodon.org/@bitwarden/109636825700482007) with Bitwarden. That doesn't mean that Bitwarden is using all of the analytics features that are provided by Google Firebase Analytics.

## Media Access

Quite a few applications allows you to "share" a file with them for media upload. If you want to, for example, tweet a picture to Twitter, do not grant Twitter access to your "media and photos", because it will have access to all of your pictures then. Instead, go to your file manager (documentsUI), hold onto the picture, then share it with Twitter.

## User Profiles

Multiple user profiles can be found in **Settings** → **System** → **Multiple users** and are the simplest way to isolate in Android.

With user profiles, you can impose restrictions on a specific profile, such as: making calls, using SMS, or installing apps on the device. Each profile is encrypted using its own encryption key and cannot access the data of any other profiles. Even the device owner cannot view the data of other profiles without knowing their password. Multiple user profiles are a more secure method of isolation.

## 직장 프로필

[직장 프로필](https://support.google.com/work/android/answer/6191949)은 개별 앱을 격리하는 방식 중 하나로, 경우에 따라서 별도 사용자 프로필을 사용하는 것보다 편리합니다.

여러분이 별도로 해당 기능을 탑재한 커스텀 Android 운영 체제를 사용하는 것이 아닌 한, 엔터프라이즈 MDM 없이 직장 프로필을 생성하려면 [Shelter](#recommended-apps) 등의 **기기 컨트롤러** 앱을 사용해야 합니다.

직장 프로필은 기기 컨트롤러에 따라 작동 방식이 달라집니다. *File Shuttle*, *연락처 검색 차단*을 비롯한 모든 격리 기능은 컨트롤러에서 구현됩니다. 기기 컨트롤러는 직장 프로필 내부 데이터의 전체 접근 권한을 가지고 있으므로, 믿을 수 있는 기기 컨트롤러 앱을 사용해야 합니다.

직장 프로필은 보조 사용자 프로필에 비해 보안성은 떨어집니다. 하지만 개인 프로필과 직장 프로필에서 동시에 앱을 실행할 수 있다는 편리함이 존재합니다.

## VPN 킬 스위치

Android 7 이상은 외부 앱을 설치할 필요 없이 VPN 킬 스위치를 자체적으로 지원합니다. 해당 기능은 VPN 연결이 끊어졌을 때 유출이 발생하지 않도록 방지할 수 있습니다. :gear: **설정** → **네트워크 및 인터넷** → **VPN** → :gear: → **연결 차단(VPN 제외)**에서 확인할 수 있습니다.

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

### Google Play 시스템 업데이트

과거에는 Android 보안 업데이트를 해당 운영 체제 공급업체에서 제공하는 구조였습니다. Android 10 이후부터 Android는 더욱 모듈화되었으며, Google은 Play 서비스를 통해 **일부** 시스템 구성 요소에 보안 업데이트를 제공할 수 있게 되었습니다.

여러분이 사용 중인 기기가 Android 10 이상이면서, 업데이트 지원은 종료되었고, Privacy Guides 권장 운영 체제는 지원하지 않는 경우, 별도 운영 체제(Privacy Guides 권장 목록에 등재되지 않은 LineageOS, /e/ OS 등)를 설치하는 것보다 제조사 Android를 그대로 사용하는 편이 더 나을 수도 있습니다. This will allow you to receive **some** security fixes from Google, while not violating the Android security model by using an insecure Android derivative and increasing your attack surface. 물론, 가능하다면 아직 지원되는 기기로 빨리 업그레이드하는 편이 더욱 좋습니다.

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
