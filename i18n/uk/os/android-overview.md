---
title: Android Overview
icon: simple/android
description: Android is an open-source operating system with strong security protections, which makes it our top choice for phones.
---

![Android logo](../assets/img/android/android.svg){ align=right }

The **Android Open Source Project** is a secure mobile operating system featuring strong [app sandboxing](https://source.android.com/security/app-sandbox), [Verified Boot](https://source.android.com/security/verifiedboot) (AVB), and a robust [permission](https://developer.android.com/guide/topics/permissions/overview) control system.

## Our Advice

### Вибір прошивки Android

When you buy an Android phone, the default operating system comes bundled with apps and functionality that are not part of the Android Open Source Project. Many of these apps—even apps like the dialer which provide basic system functionality—require invasive integrations with Google Play Services, which in turn asks for privileges to access your files, contacts storage, call logs, SMS messages, location, camera, microphone, and numerous other things on your device in order for those basic system apps and many other apps to function in the first place. Frameworks like Google Play Services increase the attack surface of your device and are the source of various privacy concerns with Android.

Ця проблема може бути вирішена за допомогою користувацької прошивки Android, яка не постачається з такою інвазивною інтеграцією. На жаль, багато користувацьких прошивок Android часто порушують модель безпеки Android, не підтримуючи критичні функції безпеки, такі як AVB, захист від відкату, оновлення мікропрограми тощо. Деякі дистрибутиви також постачають збірки [`налагодження`](https://source.android.com/setup/build/building#choose-a-target), які надають доступ root через [ADB](https://developer.android.com/studio/command-line/adb) та потребують [більш дозвільних](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) політик SELinux для функцій налагодження, в результаті чого це призводить до збільшення поверхні атаки та ослаблення моделі безпеки.

В ідеалі, вибираючи користувальницький дистрибутив Android, ви повинні переконатися, що він підтримує модель безпеки Android. Принаймні, дистрибутив повинен мати виробничі збірки, підтримку AVB, захист від відкату, своєчасне оновлення прошивки та операційної системи, а також SELinux в [примусовому режимі (enforcing mode)](https://source.android.com/security/selinux/concepts#enforcement_levels). Всі наші рекомендовані прошивки Android відповідають цим критеріям.

[Наші рекомендації для системи Android :material-arrow-right:](../android/distributions.md ""){.md-button}

### Уникайте рутування

[Рутування](https://en.wikipedia.org/wiki/Rooting_(Android)) Android пристроїв може значно знизити безпеку, оскільки це послаблює повну [модель безпеки Android](https://en.wikipedia.org/wiki/Android_(operating_system)#Security_and_privacy). Це може знизити конфіденційність у разі використання експлойта, якому сприяє зниження безпеки. Поширені методи отримання root-прав передбачають втручання в розділ boot, що унеможливлює успішне виконання Verified Boot. Apps that require root will also modify the system partition, meaning that Verified Boot would have to remain disabled. Наявність root-доступу безпосередньо в інтерфейсі користувача також збільшує [поверхню атаки](https://en.wikipedia.org/wiki/Attack_surface) вашого пристрою і може сприяти [підвищенню привілеїв](https://en.wikipedia.org/wiki/Privilege_escalation), вразливостей та обходу політики SELinux.

Content blockers which modify the [hosts file](https://en.wikipedia.org/wiki/Hosts_(file)) (AdAway) and firewalls (AFWall+) which require root access persistently are dangerous and should not be used. Вони також не є правильним способом вирішення своїх цілей. For content blocking, we suggest encrypted [DNS](../dns.md) or content blocking functionality provided by a VPN instead. TrackerControl and AdAway in non-root mode will take up the VPN slot (by using a local loopback VPN), preventing you from using privacy enhancing services such as [Orbot](../tor.md#orbot) or a [real VPN provider](../vpn.md).

AFWall+ використовує підхід на основі [пакетної фільтрації](https://en.wikipedia.org/wiki/Firewall_(computing)#Packet_filter), та його можна обійти в деяких ситуаціях.

Ми не вважаємо, що жертви безпеки, які приносить рутування телефону, варті сумнівних переваг конфіденційності цих програм.

### Install Updates

It's important to not use an [end-of-life](https://endoflife.date/android) version of Android. Newer versions of Android receive not only security updates for the operating system but also important privacy enhancing updates too.

For example, [prior to Android 10](https://developer.android.com/about/versions/10/privacy/changes) any apps with the [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) permission could access sensitive and unique serial numbers of your phone such as [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), or your SIM card's [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity); whereas now they must be system apps to do so. System apps are only provided by the OEM or Android distribution.

### Sharing Media

You can avoid giving many apps permission to access your media with Android's built-in sharing features. Many applications allow you to "share" a file with them for media upload.

For example, if you want to post a picture to Discord you can open your file manager or gallery and share that picture with the Discord app, instead of granting Discord full access to your media and photos.

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

Пристрої EOL, які більше не підтримуються виробником SoC, не можуть отримувати оновлення мікропрограми від OEM-виробників або сторонніх дистриб'юторів Android. Це означає, що проблеми безпеки на цих пристроях залишаться не усуненими. [Qualcomm](https://www.qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) and [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox) support their devices for 4 years, while cheaper products often have shorter support cycles. With the introduction of the [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google now makes their own SoC, and they will provide a minimum of 5 years of support. With the introduction of the Pixel 8 series, Google increased that support window to 7 years.

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

Для цього потрібен **контролер пристрою** такий як [Shelter](#recommended-apps), якщо ви не використовуєте CalyxOS, яка вже містить в собі контролер.

Робочий профіль залежить від функціонування контролера пристрою. Кожен профіль зашифрований за допомогою власного ключа шифрування і не може отримати доступ до даних будь-яких інших профілів. Навіть власник пристрою не може переглядати дані профілів, не знаючи їхніх паролів. Multiple user profiles are a more secure method of isolation.

### Робочий профіль

[Робочі профілі](https://support.google.com/work/android/answer/6191949) - це ще один спосіб ізоляції програм, який може бути зручнішим, ніж окремі профілі користувачів.

A **device controller** app such as [Shelter](../android/general-apps.md#shelter) is required to create a Work Profile without an enterprise MDM, unless you're using a custom Android OS which includes one.

Робочий профіль залежить від функціонування контролера пристрою. Такі функції як *Файловий шатл* та *блокування пошуку контактів* або будь-які інші функції ізоляції повинні бути реалізовані контролером. You must also fully trust the device controller app, as it has full access to your data inside the work profile.

Цей метод, як правило, є менш безпечним, ніж додатковий профіль користувача; однак, він дозволяє вам зручно запускати додатки як в робочому, так і в особистому профілях одночасно.

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
