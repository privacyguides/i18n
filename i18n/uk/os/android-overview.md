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

### Verified Boot

[**Verified Boot**](https://source.android.com/security/verifiedboot) is an important part of the Android security model. Він забезпечує захист від атак [evil maid](https://en.wikipedia.org/wiki/Evil_maid_attack), стійкість до шкідливого програмного забезпечення, та гарантує що оновлення безпеки не можуть бути знижені за допомогою [захисту від відкату](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection).

Android 10 і вище перейшли від повного шифрування диска до більш гнучкішого [шифрування на основі файлів](https://source.android.com/security/encryption/file-based). Ваші дані шифруються за допомогою унікальних ключів шифрування, а файли операційної системи залишаються незашифрованими.

Verified Boot забезпечує цілісність файлів операційної системи, тим самим запобігаючи зловмиснику з фізичним доступом втручатися або встановлювати шкідливе програмне забезпечення на пристрій. У малоймовірному випадку, коли шкідливе програмне забезпечення може експлуатувати інші частини системи та отримувати вищий привілейований доступ, Verified Boot запобігатиме та повертатиме зміни до системного розділу після перезавантаження пристрою.

На жаль, OEM-виробники зобов'язані підтримувати Verified Boot лише на своїй заводській прошивці Android. Лише кілька OEM-виробників, таких як Google, підтримують користувацьку реєстрацію ключів AVB на своїх пристроях. Крім цього, деякі похідні AOSP, такі як LineageOS або /e/ OS, не підтримують Verified Boot навіть на обладнанні з підтримкою Verified Boot для сторонніх операційних систем. Ми рекомендуємо вам перевірити наявність підтримки **перед** придбанням нового пристрою. Похідні AOSP, які не підтримують Verified Boot **не рекомендуються**.

Оновлення мікропрограми є критично важливими для підтримки безпеки, і без них ваш пристрій не може бути захищеним. OEM-виробники мають угоди про підтримку зі своїми партнерами щодо надання компонентів із закритим вихідним кодом протягом обмеженого періоду. This breaks verified boot on a stock Fairphone device, as the system will boot alternative Android operating systems (such as /e/) [without any warning](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) about custom operating system usage.

### Оновлення мікропрограми

**Firmware updates** are critical for maintaining security and without them your device cannot be secure. Тому важливо, щоб ви придбали пристрій в рамках активного циклу підтримки. [Qualcomm](https://www.qualcomm.com/news/releases/2020/12/16/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) та [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox/) підтримують свої пристрої протягом 4 років, тоді як дешевші продукти часто мають коротші цикли підтримки.

Пристрої EOL, які більше не підтримуються виробником SoC, не можуть отримувати оновлення мікропрограми від OEM-виробників або сторонніх дистриб'юторів Android. Це означає, що проблеми безпеки на цих пристроях залишаться не усуненими. [Qualcomm](https://qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) and [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox) support their devices for 4 years, while cheaper products often have shorter support cycles. With the introduction of the [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google now makes their own SoC, and they will provide a minimum of 5 years of support. With the introduction of the Pixel 8 series, Google increased that support window to 7 years.

Важливо не використовувати версії Android з [вичерпаним терміном служби](https://endoflife.date/android). Новіші версії Android не тільки отримують оновлення безпеки для операційної системи, але й важливі оновлення, що покращують конфіденційність.

Fairphone, for example, markets their Fairphone 4 device as receiving 6 years of support. Google регулярно вносить [покращення](https://developer.android.com/about/versions/11/privacy/permissions) у систему дозволів в кожній наступній версії. Всі встановлені вами програми суворо [ізольовані](https://source.android.com/security/app-sandbox), тому немає потреби встановлювати будь-які антивірусні додатки.

### Дозволи Android

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
<p class="admonition-title">Warning</p>

If an app is mostly a web-based service, the tracking may occur on the server side. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest) shows "no trackers" but certainly does track users' interests and behavior across the site. Apps may evade detection by not using standard code libraries produced by the advertising industry, though this is unlikely.

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Privacy-friendly apps such as [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest) may show some trackers such as [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49). This library includes [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) which can provide [push notifications](https://en.wikipedia.org/wiki/Push_technology) in apps. This [is the case](https://fosstodon.org/@bitwarden/109636825700482007) with Bitwarden. That doesn't mean that Bitwarden is using all of the analytics features that are provided by Google Firebase Analytics.

</div>

## Privacy Features

### Профілі користувачів

Multiple **user profiles** can be found in :gear: **Settings** → **System** → **Users** and are the simplest way to isolate in Android.

With user profiles, you can impose restrictions on a specific profile, such as: making calls, using SMS, or installing apps. Кожен профіль зашифрований за допомогою власного ключа шифрування і не може отримати доступ до даних будь-яких інших профілів. Навіть власник пристрою не може переглядати дані профілів, не знаючи їхніх паролів. Multiple user profiles are a more secure method of isolation.

### Робочий профіль

[**Work Profiles**](https://support.google.com/work/android/answer/6191949) are another way to isolate individual apps and may be more convenient than separate user profiles.

A **device controller** app such as [Shelter](../android/general-apps.md#shelter) is required to create a Work Profile without an enterprise MDM, unless you're using a custom Android OS which includes one.

Робочий профіль залежить від функціонування контролера пристрою. Такі функції як *Файловий шатл* та *блокування пошуку контактів* або будь-які інші функції ізоляції повинні бути реалізовані контролером. You must also fully trust the device controller app, as it has full access to your data inside the work profile.

This method is generally less secure than a secondary user profile; however, it does allow you the convenience of running apps in both the owner profile and work profile simultaneously.

### Private Space

**Private Space** is a feature introduced in Android 15 that adds another way of isolating individual apps. You can set up a private space in the owner profile by navigating to :gear: **Settings** → **Security & privacy** → **Private space**. Once set up, your private space resides at the bottom of the app drawer.

Like user profiles, a private space is encrypted using its own encryption key, and you have the option to set up a different unlock method. Like work profiles, you can use apps from both the owner profile and private space simultaneously. Apps launched from a private space are distinguished by an icon depicting a key within a shield.

Unlike work profiles, Private Space is a feature native to Android that does not require a third-party app to manage it. For this reason, we generally recommend using a private space over a work profile, though you can use a work profile alongside a private space.

### VPN Killswitch

Android 7 and above supports a VPN kill switch, and it is available without the need to install third-party apps. Ця функція може запобігти витоку, якщо VPN відключений. It can be found in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

### Глобальні перемикачі

Сучасні пристрої Android мають глобальні перемикачі для вимкнення служб Bluetooth і визначення місцезнаходження. В Android 12 з'явилися перемикачі для камери та мікрофона. Коли вони не використовуються, ми рекомендуємо вимкнути їх. Apps cannot use disabled features (even if granted individual permissions) until re-enabled.

## Google Services

If you are using a device with Google services—whether with the stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS—there are a number of additional changes you can make to improve your privacy. Ми як і раніше рекомендуємо повністю уникати сервісів Google або обмежити сервіси Google Play профілем користувача/робочим профілем, об'єднавши контролер пристрою, такий як *Shelter* з ізольованим Google Play від GrapheneOS.

### Програма додаткового захисту

If you have a Google account we suggest enrolling in the [Advanced Protection Program](https://landing.google.com/advancedprotection). Це дозволить вам отримати **деякі** виправлення безпеки від Google, не порушуючи при цьому моделі безпеки Android використовуючи небезпечну похідну Android і збільшуючи поверхню атаки. Alternatively, you can use [passkeys](https://fidoalliance.org/passkeys).

Програма додаткового захисту забезпечує посилений моніторинг загроз та вмикає:

- Stricter two-factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](https://en.wikipedia.org/wiki/OAuth)
- Доступ до даних облікового запису можуть отримувати лише Google і перевірені сторонні програми
- Сканування вхідних електронних листів в акаунтах Gmail на предмет [спроб фішингу](https://en.wikipedia.org/wiki/Phishing#Email_phishing)
- Stricter [safe browser scanning](https://google.com/chrome/privacy/whitepaper.html#malware) with Google Chrome
- Більш суворий процес відновлення облікових записів з втраченими обліковими даними

 If you use non-sandboxed Google Play Services (common on stock operating systems), the Advanced Protection Program also comes with [additional benefits](https://support.google.com/accounts/answer/9764949) such as:

- Not allowing app installation outside the Google Play Store, the OS vendor's app store, or via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Mandatory automatic device scanning with [Play Protect](https://support.google.com/googleplay/answer/2812853?#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- Попередження про неперевірені додатки

### Оновлення системи Google Play

In the past, Android security updates had to be shipped by the operating system vendor. Android has become more modular beginning with Android 10, and Google can push security updates for **some** system components via the privileged Play Services.

На прошивках Android з привілейованими сервісами Google Play (як на заводських ОС), налаштування може здійснюватися в одному з кількох місць. Перевірте We would still recommend upgrading to a supported device as soon as possible.

### Рекламний ідентифікатор

All devices with Google Play Services installed automatically generate an [advertising ID](https://support.google.com/googleplay/android-developer/answer/6048248) used for targeted advertising. Вимкніть цю функцію, щоб обмежити збір даних про вас.

On Android distributions with [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), go to :gear: **Settings** → **Apps** → **Sandboxed Google Play** → **Google Settings** → **Ads**, and select *Delete advertising ID*.

На прошивках Android з привілейованими сервісами Google Play (як на заводських ОС), налаштування може здійснюватися в одному з кількох місць. Перевірте

- :gear: **Налаштування** → **Google** → **Реклама**
- :gear: **Налаштування** → **Конфіденційність** → **Реклама**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads* (this varies between OEM distributions of Android). If presented with the option to delete the advertising ID, that is preferred. If not, then make sure to opt out and reset your advertising ID.

### SafetyNet та Play API цілісність

[SafetyNet](https://developer.android.com/training/safetynet/attestation) та [Play API цілісність](https://developer.android.com/google/play/integrity) зазвичай використовуються для [банківських додатків](https://grapheneos.org/usage#banking-apps). Many banking apps will work fine in GrapheneOS with sandboxed Play services, however some non-financial apps have their own crude anti-tampering mechanisms which might fail. GrapheneOS проходить перевірку `basicIntegrity`, але не перевірку сертифікації `ctsProfileMatch`. Пристрої з Android 8 або пізнішою версією мають підтримку апаратної атестації, яку неможливо обійти без витоку ключів або серйозних вразливостей.

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt out if you don't want your credit rating and personal information shared with affiliate marketing services.
