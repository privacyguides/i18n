---
title: نظرة عامة على Android
icon: simple/android
description: نظام Android هو نظام تشغيل مفتوح المصدر، ويوفر حماية أمنية قوية، مما يجعله خيارنا الأول للهواتف.
robots: nofollow, max-snippet:-1, max-image-preview:large
---

![Android logo](../assets/img/android/android.svg){ align=right }

يُعد **Android Open Source Project** نظام تشغيل آمنًا للهواتف، ويتميز بنظام قوي لعزل التطبيقات ([sandboxing](https://source.android.com/security/app-sandbox))، وميزة [Verified Boot (AVB)](https://source.android.com/security/verifiedboot)، ونظام محكم للتحكم في[ الأذونات (permissions)](https://developer.android.com/guide/topics/permissions/overview).

[:octicons-home-16:](https://source.android.com){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/main){ .card-link title="Source Code" }

[نصائحنا لنظام Android :material-arrow-right-drop-circle:](../android/index.md ""){.md-button.md-button--primary}

## وسائل الحماية الأمنية

تشمل أهم عناصر نظام الحماية في Android التحقق من[ سلامة الإقلاع (verified boot)](#verified-boot)، [وتحديثات البرامج الثابتة (Firmware)](#firmware-updates)، [ونظامًا قويًا للتحكم في الأذونات](#android-permissions). تُشكّل ميزات الأمان المهمة هذه الأساس الذي نعتمد عليه في تحديد الحد الأدنى من المعايير لاختيار [الهواتف](../mobile-phones.md) و[أنظمة Android المعدّلة](../android/distributions.md) التي نوصي بها.

### التحقق من سلامة الإقلاع (Verified Boot)

يُعد الـ[**Verified Boot**](https://source.android.com/security/verifiedboot) جزءا مهما من نظام الأمان في Android. يوفّر حماية من هجمات [Evil Maid](https://en.wikipedia.org/wiki/Evil_maid_attack)، ويمنع البرمجيات الخبيثة من البقاء على الجهاز، ويضمن عدم إمكانية الرجوع إلى إصدارات أقدم من التحديثات الأمنية بفضل ميزة [rollback protection](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection).

بدءًا من Android 10، انتقل النظام من تشفير القرص بالكامل إلى [تشفير الملفات](https://source.android.com/security/encryption/file-based)، الذي يوفر مرونة أكبر. تُشفر بياناتك باستخدام مفاتيح تشفير فريدة، بينما تظل ملفات نظام التشغيل غير مشفرة.

يضمن الـVerified Boot سلامة ملفات نظام التشغيل وعدم التلاعب بها، مما يمنع أي مهاجم لديه وصول فعلي إلى الجهاز من تعديل هذه الملفات أو تثبيت برمجيات خبيثة عليه. في حال تمكنت برمجية خبيثة، رغم ندرة حدوث ذلك، من استغلال أجزاء أخرى من النظام والحصول على صلاحيات أعلى، فإن الـ Verified Boot سيمنع استمرار أي تغييرات أُجريت على النظام، ويعيده إلى حالته الأصلية عند إعادة تشغيل الجهاز.

للأسف، لا يُلزم مصنعو الأجهزة (OEMs) بدعم الـVerified Boot إلا في نسخة Android الأصلية التي يوفرونها مع أجهزتهم. لا يدعم تسجيل مفاتيح AVB مخصصة على أجهزته سوى عدد قليل من الشركات المصنعة، مثل Google. بالإضافة إلى ذلك، لا تدعم بعض الأنظمة المشتقة من AOSP، مثل LineageOS و/e/ OS، ميزة الـVerified Boot، حتى على الأجهزة التي تدعم هذه الميزة مع أنظمة تشغيل خارجية. ننصحك بالتأكد من دعم هذه الميزة **قبل** شراء جهاز جديد. لا ننصح باستخدام الأنظمة المشتقة من AOSP التي **لا** تدعم Verified Boot.

كذلك، تطبّق العديد من الشركات المصنعة ميزة الـVerified Boot بشكل غير صحيح، لذا عليك الانتباه إلى هذه المشكلات وعدم الاعتماد على ما تروج له الشركات. على سبيل المثال، لا يتمتع جهازا Fairphone 3 وFairphone 4 بالأمان الكافي بإعداداتهما الافتراضية، لأن [ الـ (bootloader) الأصلي يثق بمفتاح AVB العام المستخدم للتوقيع.](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11) هذا يضعف حماية الـVerified Boot على أجهزة Fairphone التي تعمل بنظامها الأصلي، إذ يمكن للجهاز تشغيل أنظمة Android بديلة (مثل /e/) دون عرض[ أي تحذير](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) بشأن استخدام نظام تشغيل مخصّص.

### تحديثات الـ Firmware

**تحديثات الـ (Firmware) **ضرورية للحفاظ على أمان جهازك، وبدونها لا يمكن أن يكون جهازك آمنا. لدى الشركات المصنعة للأجهزة (OEMs) اتفاقيات مع شركائها لتوفير المكونات مغلقة المصدر لفترة دعم محدودة. تُوضح تفاصيل هذه المكونات في [نشرات أمان Android الشهرية.](https://source.android.com/security/bulletin)

نظرا لأن بعض مكونات الهاتف، مثل المعالج وتقنيات الاتصال اللاسلكي، تعتمد على مكونات مغلقة المصدر، فلا بد أن توفر الشركات المصنعة لهذه المكوّنات التحديثات اللازمة. لذلك، من المهم أن تشتري جهازا لا يزال يحصل على تحديثات ودعم من الشركة المصنعة. توفّر شركتا [Qualcomm](https://qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) و[Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox) الدعم لأجهزتهما لمدة 4 سنوات، بينما غالبا ما تكون فترة الدعم للمنتجات الأقل سعرا أقصر. مع إطلاق [Pixel 6](https://support.google.com/pixelphone/answer/4457705)، بدأت Google بتصنيع نظامها الخاص على شريحة (SoC)، وستوفر الدعم لأجهزتها لمدة لا تقل عن 5 سنوات. مع إطلاق سلسلة Pixel 8، رفعت Google فترة الدعم إلى 7 سنوات.

الأجهزة التي انتهت فترة دعمها (EOL) من الشركة المصنعة للمعالج (SoC) لا يمكنها تلقي تحديثات الـ (Firmware)، سواء من الشركات المصنعة للأجهزة (OEMs) أو من مطوّري إصدارات Android البديلة. هذا يعني أن الثغرات الأمنية في هذه الأجهزة ستظل دون إصلاح.

على سبيل المثال، تروج شركة Fairphone لجهاز Fairphone 4 على أنه سيحصل على الدعم لمدة 6 سنوات. لكن المعالج (SoC) المستخدم في Fairphone 4، وهو Qualcomm Snapdragon 750G، تنتهي فترة دعمه قبل ذلك بوقت طويل. هذا يعني أن تحديثات الـ (Firmware) التي توفرها Qualcomm لجهاز Fairphone 4 ستتوقف في سبتمبر 2023، حتى لو استمرت Fairphone في إصدار تحديثات أمنية للنظام.

### أذونات الـ Android

تتيح لك [**الأذونات في Android **](https://developer.android.com/guide/topics/permissions/overview)التحكم فيما يُسمح للتطبيقات بالوصول إليه. تُجري Google [تحسينات](https://developer.android.com/about/versions/11/privacy/permissions) مستمرة على نظام الأذونات مع كل إصدار جديد. تعمل جميع التطبيقات التي تثبتها داخل بيئات معزولة [(sandboxing)](https://source.android.com/security/app-sandbox) تفرض قيودا صارمة عليها، لذلك لا حاجة لتثبيت أي تطبيق لمكافحة الفيروسات.

الهاتف الذي يعمل بأحدث إصدار من Android سيكون دائما أكثر أمانا من هاتف قديم ثبت عليه تطبيقا مدفوعا لمكافحة الفيروسات. من الأفضل ألا تنفق أموالك على برامج مكافحة الفيروسات، وأن تدّخرها لشراء هاتف جديد مثل [Google Pixel](../mobile-phones.md#google-pixel).

أندرويد 10:

- تمنحك ميزة [Scoped Storage](https://developer.android.com/about/versions/10/privacy/changes#scoped-storage) تحكما أكبر في ملفاتك، وتتيح لك تقييد وصول التطبيقات إلى [وحدة التخزين الخارجية](https://developer.android.com/training/data-storage#permissions). يمكن أن يكون لكل تطبيق مجلد خاص به في وحدة التخزين الخارجية، كما يمكنه تخزين أنواع معينة من ملفات الوسائط فيها.
- فرض قيود أكثر صرامة على الوصول إلى [موقع الجهاز](https://developer.android.com/about/versions/10/privacy/changes#app-access-device-location)، من خلال إضافة إذن `ACCESS_BACKGROUND_LOCATION`. هذا يمنع التطبيقات من معرفة موقعك أثناء عملها في الخلفية، إلا إذا سمحت لها بذلك بشكل واضح.

أندرويد 11:

- أذونات تُستخدم [لمرة واحدة](https://developer.android.com/about/versions/11/privacy/permissions#one-time)، تتيح لك منح التطبيق إذنا لمرة واحدة فقط.
- [إعادة ضبط الأذونات تلقائيا](https://developer.android.com/about/versions/11/privacy/permissions#auto-reset)، حيث تُلغى الأذونات التي مُنحت للتطبيق [أثناء استخدامه](https://developer.android.com/guide/topics/permissions/overview#runtime).
- أذونات منفصلة للتحكم في الوصول إلى الميزات المتعلقة[برقم الهاتف.](https://developer.android.com/about/versions/11/privacy/permissions#phone-numbers)

أندرويد 12:

- إذن يتيح لك مشاركة موقعك [التقريبي فقط](https://developer.android.com/about/versions/12/behavior-changes-12#approximate-location).
- إعادة ضبط أذونات [التطبيقات غير المستخدمة](https://developer.android.com/about/versions/12/behavior-changes-12#app-hibernation) تلقائيًا.
- [تتبّع وصول](https://developer.android.com/about/versions/12/behavior-changes-12#data-access-auditing) التطبيقات إلى البيانات، مما يسهّل معرفة أي جزء من التطبيق يصل إلى نوع معيّن من البيانات.

أندرويد 13:

- إذن للوصول إلى [أجهزة Wi-Fi القريبة](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). كانت التطبيقات تستخدم عناوين MAC الخاصة بنقاط اتصال Wi-Fi القريبة بشكل شائع لتتبع موقع المستخدم.
- More [granular media permissions](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions), meaning you can grant access to images, videos or audio files only.
- Background use of sensors now requires the [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission) permission.

An app may request a permission for a specific feature it has. For example, any app that can scan QR codes will require the camera permission. Some apps can request more permissions than they need.

[Exodus](https://exodus-privacy.eu.org) can be useful when comparing apps that have similar purposes. If an app requires a lot of permissions and has a lot of advertising and analytics this is probably a bad sign. We recommend looking at the individual trackers and reading their descriptions rather than simply **counting the total** and assuming all items listed are equal.

<div class="admonition warning" markdown>
<p class="admonition-title">تنوية</p>

If an app is mostly a web-based service, the tracking may occur on the server side. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest) shows "no trackers" but certainly does track users' interests and behavior across the site. Apps may evade detection by not using standard code libraries produced by the advertising industry, though this is unlikely.

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Privacy-friendly apps such as [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest) may show some trackers such as [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49). This library includes [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) which can provide [push notifications](https://en.wikipedia.org/wiki/Push_technology) in apps. This [is the case](https://fosstodon.org/@bitwarden/109636825700482007) with Bitwarden. That doesn't mean that Bitwarden is using all the analytics features that are provided by Google Firebase Analytics.

</div>

## Privacy Features

### User Profiles

Multiple **user profiles** can be found in :gear: **Settings** → **System** → **Users** and are the simplest way to isolate in Android.

With user profiles, you can impose restrictions on a specific profile, such as: making calls, using SMS, or installing apps. Each profile is encrypted using its own encryption key and cannot access the data of any other profiles. Even the device owner cannot view the data of other profiles without knowing their password. Multiple user profiles are a more secure method of isolation.

### Work Profile

[**Work Profiles**](https://support.google.com/work/android/answer/6191949) are another way to isolate individual apps and may be more convenient than separate user profiles.

A **device controller** app such as [Shelter](../android/general-apps.md#shelter) is required to create a Work Profile without an enterprise MDM, unless you're using a custom Android OS which includes one.

The work profile is dependent on a device controller to function. Features such as *File Shuttle* and *contact search blocking* or any kind of isolation features must be implemented by the controller. You must also fully trust the device controller app, as it has full access to your data inside the work profile.

This method is generally less secure than a secondary user profile; however, it does allow you the convenience of running apps in both the owner profile and work profile simultaneously.

### Private Space

**Private Space** is a feature introduced in Android 15 that adds another way of isolating individual apps. You can set up a private space in the owner profile by navigating to :gear: **Settings** → **Security & privacy** → **Private space**. Once set up, your private space resides at the bottom of the app drawer.

Like user profiles, a private space is encrypted using its own encryption key, and you have the option to set up a different unlock method. Like work profiles, you can use apps from both the owner profile and private space simultaneously. Apps launched from a private space are distinguished by an icon depicting a key within a shield.

Unlike work profiles, Private Space is a feature native to Android that does not require a third-party app to manage it. For this reason, we generally recommend using a private space over a work profile, though you can use a work profile alongside a private space.

### VPN kill switch

Android 7 and above supports a VPN kill switch, and it is available without the need to install third-party apps. This feature can prevent leaks if the VPN is disconnected. It can be found in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

### Global Toggles

Modern Android devices have global toggles for disabling Bluetooth and location services. Android 12 introduced toggles for the camera and microphone. When not in use, we recommend disabling these features. Apps cannot use disabled features (even if granted individual permissions) until re-enabled.

## Google Services

If you are using a device with Google services—whether with the stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS—there are a number of additional changes you can make to improve your privacy. We still recommend avoiding Google services entirely, or limiting Google Play Services to a specific user/work profile by combining a device controller like *Shelter* with GrapheneOS's Sandboxed Google Play.

### Advanced Protection Program

If you have a Google account we suggest enrolling in the [Advanced Protection Program](https://landing.google.com/advancedprotection). It is available at no cost to anyone with two or more hardware security keys with [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) support. Alternatively, you can use [passkeys](https://fidoalliance.org/passkeys).

The Advanced Protection Program provides enhanced threat monitoring and enables:

- Stricter two-factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](../basics/account-creation.md#sign-in-with-oauth)
- Only Google and verified third-party apps can access account data
- Scanning of incoming emails on Gmail accounts for [phishing](https://en.wikipedia.org/wiki/Phishing#Email_phishing) attempts
- Stricter [safe browser scanning](https://google.com/chrome/privacy/whitepaper.html#malware) with Google Chrome
- Stricter recovery process for accounts with lost credentials

 If you use non-sandboxed Google Play Services (common on stock operating systems), the Advanced Protection Program also comes with [additional benefits](https://support.google.com/accounts/answer/9764949) such as:

- Not allowing app installation outside the Google Play Store, the OS vendor's app store, or via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Mandatory automatic device scanning with [Play Protect](https://support.google.com/googleplay/answer/2812853?#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- Warning you about unverified applications
- Enabling ARM's hardware-based [Memory Tagging Extension (MTE)](https://developer.arm.com/documentation/108035/0100/Introduction-to-the-Memory-Tagging-Extension) for supported apps, which lowers the likelihood of device exploits happening through memory corruption bugs

### Google Play System Updates

In the past, Android security updates had to be shipped by the operating system vendor. Android has become more modular beginning with Android 10, and Google can push security updates for **some** system components via the privileged Play Services.

If you have an EOL device shipped with Android 10 or above and are unable to run any of our recommended operating systems on your device, you are likely going to be better off sticking with your OEM Android installation (as opposed to an operating system not listed here such as LineageOS or /e/ OS). This will allow you to receive **some** security fixes from Google, while not violating the Android security model by using an insecure Android derivative and increasing your attack surface. We would still recommend upgrading to a supported device as soon as possible.

### Advertising ID

All devices with Google Play Services installed automatically generate an [advertising ID](https://support.google.com/googleplay/android-developer/answer/6048248) used for targeted advertising. Disable this feature to limit the data collected about you.

On Android distributions with [sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), go to :gear: **Settings** → **Apps** → **Sandboxed Google Play** → **Google Settings** → **All services** → **Ads**.

- [x] Select **Delete advertising ID**

On Android distributions with privileged Google Play Services (which includes the stock installation on most devices), the setting may be in one of several locations. Check

- :gear: **Settings** → **Google** → **Ads**
- :gear: **Settings** → **Privacy** → **Ads**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads* (this varies between OEM distributions of Android). If presented with the option to delete the advertising ID, that is preferred. If not, then make sure to opt out and reset your advertising ID.

### SafetyNet and Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) and the [Play Integrity APIs](https://developer.android.com/google/play/integrity) are generally used for [banking apps](https://grapheneos.org/usage#banking-apps). Many banking apps will work fine in GrapheneOS with sandboxed Play services, however some non-financial apps have their own crude anti-tampering mechanisms which might fail. GrapheneOS passes the `basicIntegrity` check, but not the certification check `ctsProfileMatch`. Devices with Android 8 or later have hardware attestation support which cannot be bypassed without leaked keys or serious vulnerabilities.

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt out if you don't want your credit rating and personal information shared with affiliate marketing services.
