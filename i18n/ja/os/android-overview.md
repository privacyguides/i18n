---
title: Androidの概要
icon: simple/android
description: Androidは、強力なセキュリティー保護機能を備えたオープンソースのオペレーティングシステムであり、携帯電話に関する最も優れた選択肢です。
---

![Android logo](../assets/img/android/android.svg){ align=right }

**Androidオープンソースプロジェクト**は、[アプリ・サンドボックス](https://source.android.com/security/app-sandbox)、[確認付きブート](https://source.android.com/security/verifiedboot)（AVB）、[権限](https://developer.android.com/guide/topics/permissions/overview)管理システムを備えた安全なモバイル・オペレーティングシステムです。

## 私たちのアドバイス

### Androidディストリビューションの選択

When you buy an Android phone, the default operating system comes bundled with apps and functionality that are not part of the Android Open Source Project. Many of these apps—even apps like the dialer which provide basic system functionality—require invasive integrations with Google Play Services, which in turn asks for privileges to access your files, contacts storage, call logs, SMS messages, location, camera, microphone, and numerous other things on your device in order for those basic system apps and many other apps to function in the first place. Frameworks like Google Play Services increase the attack surface of your device and are the source of various privacy concerns with Android.

この問題は、そうした強制的な統合を伴わない、カスタムAndroidディストリビューションを使用すると解決できる可能性があります。 しかし残念ながら、多くのカスタムAndroidディストリビューションは、AVBや、ロールバック保護、ファームウェア・アップデートなどの重要なセキュリティ機能をサポートしておらず、しばしばAndroidのセキュリティーモデルに違反しています。 ディストリビューションによっては、[`userdebug`](https://source.android.com/setup/build/building#choose-a-target)ビルドもリリースしています。このビルドは、 [ADB](https://developer.android.com/studio/command-line/adb)経由でrootを公開し、デバッグ機能に対応するために[より寛容な](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code)SELinuxポリシーを必要とするものです。結果、攻撃対象がさらに増加し、セキュリティモデルが弱体化してしまいます。

Androidのカスタムディストリビューションを選択する場合には、Androidのセキュリティーモデルが維持されていることを確認してください。 少なくとも、製品用ビルド、AVBのサポート、ロールバック保護、適時のファームウェアとオペレーティングシステムのアップデート、および[強制モード](https://source.android.com/security/selinux/concepts#enforcement_levels)のSELinuxを持つべきです。 私たちが推奨するAndroidディストリビューションはすべて、これらの基準を満たしています。

[私たちが推奨するAndroidシステム :material-arrow-right-drop-circle:](../android.md ""){.md-button}

### root化を避けること

Android携帯電話の[root化](https://en.wikipedia.org/wiki/Rooting_(Android))を行うと、完全な[Androidセキュリティーモデル](https://en.wikipedia.org/wiki/Android_(operating_system)#Security_and_privacy)が弱められ、セキュリティーが著しく低下する可能性があります。 root化によって低下したセキュリティーの脆弱性が悪用されると、プライバシーが損なわれてしまう可能性があります。 一般的な方法でroot化を行うと、ブートパーティションが直接変更されてしまうため、確認付きブートを行うことはできなくなります。 rootを必要とするアプリはシステムパーティションを変更するため、確認付きブートを無効のままにしておく必要があります。 また、ユーザーインターフェースで直接rootを露出させると、[デバイスの攻撃面](https://en.wikipedia.org/wiki/Attack_surface)が増加し、 [権限昇格](https://en.wikipedia.org/wiki/Privilege_escalation)の脆弱性やSELinuxポリシーのバイパスが助長されるおそれがあります。

Adblockers, which modify the [hosts file](https://en.wikipedia.org/wiki/Hosts_(file)) (AdAway) and firewalls (AFWall+) which require root access persistently are dangerous and should not be used. They are also not the correct way to solve their intended purposes. For Adblocking we suggest encrypted [DNS](../dns.md) or [VPN](../vpn.md) server blocking solutions instead. RethinkDNS, TrackerControl and AdAway in non-root mode will take up the VPN slot (by using a local loopback VPN) preventing you from using privacy enhancing services such as Orbot or a real VPN server.

AFWall+ works based on the [packet filtering](https://en.wikipedia.org/wiki/Firewall_(computing)#Packet_filter) approach and may be bypassable in some situations.

We do not believe that the security sacrifices made by rooting a phone are worth the questionable privacy benefits of those apps.

### アップデートをインストールすること

It's important to not use an [end-of-life](https://endoflife.date/android) version of Android. Newer versions of Android not only receive security updates for the operating system but also important privacy enhancing updates too.

For example, [prior to Android 10](https://developer.android.com/about/versions/10/privacy/changes) any apps with the [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) permission could access sensitive and unique serial numbers of your phone such as [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), or your SIM card's [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity); whereas now they must be system apps to do so. System apps are only provided by the OEM or Android distribution.

### Sharing Media

You can avoid giving many apps permission to access your media with Android's built-in sharing features. Many applications allow you to "share" a file with them for media upload.

For example, if you want to post a picture to Discord you can open your file manager or gallery and share that picture with the Discord app, instead of granting Discord full access to your media and photos.

## セキュリティーの保護

### 確認付きブート

[確認付きブート](https://source.android.com/security/verifiedboot)は、Androidのセキュリティー・モデルの重要な部分です。 It provides protection against [evil maid](https://en.wikipedia.org/wiki/Evil_maid_attack) attacks, malware persistence, and ensures security updates cannot be downgraded with [rollback protection](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection).

Android 10 and above has moved away from full-disk encryption to more flexible [file-based encryption](https://source.android.com/security/encryption/file-based). Your data is encrypted using unique encryption keys, and the operating system files are left unencrypted.

Verified Boot ensures the integrity of the operating system files, thereby preventing an adversary with physical access from tampering or installing malware on the device. In the unlikely case that malware is able to exploit other parts of the system and gain higher privileged access, Verified Boot will prevent and revert changes to the system partition upon rebooting the device.

Unfortunately, OEMs are only obliged to support Verified Boot on their stock Android distribution. Only a few OEMs such as Google support custom AVB key enrollment on their devices. Additionally, some AOSP derivatives such as LineageOS or /e/ OS do not support Verified Boot even on hardware with Verified Boot support for third-party operating systems. We recommend that you check for support **before** purchasing a new device. AOSP derivatives which do not support Verified Boot are **not** recommended.

Many OEMs also have broken implementation of Verified Boot that you have to be aware of beyond their marketing. For example, the Fairphone 3 and 4 are not secure by default, as the [stock bootloader trusts the public AVB signing key](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). This breaks verified boot on a stock Fairphone device, as the system will boot alternative Android operating systems such (such as /e/) [without any warning](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) about custom operating system usage.

### ファームウェアの更新

Firmware updates are critical for maintaining security and without them your device cannot be secure. OEMs have support agreements with their partners to provide the closed-source components for a limited support period. These are detailed in the monthly [Android Security Bulletins](https://source.android.com/security/bulletin).

As the components of the phone, such as the processor and radio technologies rely on closed-source components, the updates must be provided by the respective manufacturers. Therefore, it is important that you purchase a device within an active support cycle. [Qualcomm](https://www.qualcomm.com/news/releases/2020/12/16/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) and [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox/) support their devices for 4 years, while cheaper products often have shorter support cycles. With the introduction of the [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google now makes their own SoC, and they will provide a minimum of 5 years of support. With the introduction of the Pixel 8 series, Google increased that support window to 7 years.

EOL devices which are no longer supported by the SoC manufacturer cannot receive firmware updates from OEM vendors or after market Android distributors. This means that security issues with those devices will remain unfixed.

Fairphone, for example, markets their Fairphone 4 device as receiving 6 years of support. However, the SoC (Qualcomm Snapdragon 750G on the Fairphone 4) has a considerably shorter EOL date. This means that firmware security updates from Qualcomm for the Fairphone 4 will end in September 2023, regardless of whether Fairphone continues to release software security updates.

### Androidのアクセス許可

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

- A permission for [nearby Wi-Fi access](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). The MAC addresses of nearby Wi-Fi access points was a popular way for apps to track a user's location.
- More [granular media permissions](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions), meaning you can grant access to images, videos or audio files only.
- Background use of sensors now requires the [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission) permission.

An app may request a permission for a specific feature it has. For example, any app that can scan QR codes will require the camera permission. Some apps can request more permissions than they need.

[Exodus](https://exodus-privacy.eu.org/) can be useful when comparing apps that have similar purposes. If an app requires a lot of permissions and has a lot of advertising and analytics this is probably a bad sign. We recommend looking at the individual trackers and reading their descriptions rather than simply **counting the total** and assuming all items listed are equal.

!!! 警告

    If an app is mostly a web-based service, the tracking may occur on the server side. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest/) shows "no trackers" but certainly does track users' interests and behavior across the site. Apps may evade detection by not using standard code libraries produced by the advertising industry, though this is unlikely.

!!! メモ

    Privacy-friendly apps such as [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest/) may show some trackers such as [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49/). This library includes [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) which can provide [push notifications](https://en.wikipedia.org/wiki/Push_technology) in apps. This [is the case](https://fosstodon.org/@bitwarden/109636825700482007) with Bitwarden. That doesn't mean that Bitwarden is using all of the analytics features that are provided by Google Firebase Analytics.

## プライバシー機能

### ユーザープロフィール

Multiple user profiles can be found in **Settings** → **System** → **Multiple users** and are the simplest way to isolate in Android.

With user profiles, you can impose restrictions on a specific profile, such as: making calls, using SMS, or installing apps on the device. Each profile is encrypted using its own encryption key and cannot access the data of any other profiles. Even the device owner cannot view the data of other profiles without knowing their password. Multiple user profiles are a more secure method of isolation.

### 仕事用プロフィール

[Work Profiles](https://support.google.com/work/android/answer/6191949) are another way to isolate individual apps and may be more convenient than separate user profiles.

A **device controller** app such as [Shelter](../android.md#shelter) is required to create a Work Profile without an enterprise MDM, unless you're using a custom Android OS which includes one.

The work profile is dependent on a device controller to function. Features such as *File Shuttle* and *contact search blocking* or any kind of isolation features must be implemented by the controller. You must also fully trust the device controller app, as it has full access to your data inside the work profile.

This method is generally less secure than a secondary user profile; however, it does allow you the convenience of running apps in both the work and personal profiles simultaneously.

### VPN キルスイッチ

Android 7 and above supports a VPN kill switch, and it is available without the need to install third-party apps. この機能を使うと、VPNが切断された場合に漏洩を防ぐことができます。 It can be found in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

### Global Toggles

Modern Android devices have global toggles for disabling Bluetooth and location services. Android 12 introduced toggles for the camera and microphone. When not in use, we recommend disabling these features. Apps cannot use disabled features (even if granted individual permission) until re-enabled.

## Google サービス

If you are using a device with Google services, either your stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS, there are a number of additional changes you can make to improve your privacy. We still recommend avoiding Google services entirely, or limiting Google Play services to a specific user/work profile by combining a device controller like *Shelter* with GrapheneOS's Sandboxed Google Play.

### 高度な保護機能プログラム

If you have a Google account we suggest enrolling in the [Advanced Protection Program](https://landing.google.com/advancedprotection/). It is available at no cost to anyone with two or more hardware security keys with [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) support.

The Advanced Protection Program provides enhanced threat monitoring and enables:

- Stricter two-factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](https://en.wikipedia.org/wiki/OAuth)
- Only Google and verified third-party apps can access account data
- Scanning of incoming emails on Gmail accounts for [phishing](https://en.wikipedia.org/wiki/Phishing#Email_phishing) attempts
- Stricter [safe browser scanning](https://www.google.com/chrome/privacy/whitepaper.html#malware) with Google Chrome
- Stricter recovery process for accounts with lost credentials

 If you use non-sandboxed Google Play Services (common on stock operating systems), the Advanced Protection Program also comes with [additional benefits](https://support.google.com/accounts/answer/9764949?hl=en) such as:

- Not allowing app installation outside the Google Play Store, the OS vendor's app store, or via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Mandatory automatic device scanning with [Play Protect](https://support.google.com/googleplay/answer/2812853?hl=en#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- Warning you about unverified applications

### Google Play System Updates

In the past, Android security updates had to be shipped by the operating system vendor. Android has become more modular beginning with Android 10, and Google can push security updates for **some** system components via the privileged Play Services.

If you have an EOL device shipped with Android 10 or above and are unable to run any of our recommended operating systems on your device, you are likely going to be better off sticking with your OEM Android installation (as opposed to an operating system not listed here such as LineageOS or /e/ OS). This will allow you to receive **some** security fixes from Google, while not violating the Android security model by using an insecure Android derivative and increasing your attack surface. We would still recommend upgrading to a supported device as soon as possible.

### 広告ID

All devices with Google Play Services installed automatically generate an [advertising ID](https://support.google.com/googleplay/android-developer/answer/6048248?hl=en) used for targeted advertising. Disable this feature to limit the data collected about you.

On Android distributions with [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), go to :gear: **Settings** → **Apps** → **Sandboxed Google Play** → **Google Settings** → **Ads**, and select *Delete advertising ID*.

On Android distributions with privileged Google Play Services (such as stock OSes), the setting may be in one of several locations. Check

- :gear: **Settings** → **Google** → **Ads**
- :gear: **Settings** → **Privacy** → **Ads**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads*, this varies between OEM distributions of Android. If presented with the option to delete the advertising ID that is preferred. If not, then make sure to opt out and reset your advertising ID.

### SafetyNetとPlay Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation)と[Play Integrity API](https://developer.android.com/google/play/integrity)は、一般的に[銀行アプリ](https://grapheneos.org/usage#banking-apps)に使用されます。 GrapheneOSには、サンドボックス化されたPlayサービスがあり、多くの銀行アプリはうまく動作しますが、一部の非金融アプリには、それ自体の改ざん防止メカニズムが備わっているため、適切に動作しない可能性があります。 GrapheneOSは、 `basicIntegrity` のチェックは通過しますが、 認証チェック `ctsProfileMatch`は通過しません。 Android 8以降を搭載したデバイスには、ハードウェア認証のサポートがあります。これは、キーの漏洩や深刻な脆弱性がない限り回避することはできません。

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt out if you don't want your credit rating and personal information shared with affiliate marketing services.
