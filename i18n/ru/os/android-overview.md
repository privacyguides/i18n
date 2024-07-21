---
title: Android Overview
icon: simple/android
description: Android is an open-source operating system with strong security protections, which makes it our top choice for phones.
---

![Логотип Android](../assets/img/android/android.svg){ align=right }

The **Android Open Source Project** is a secure mobile operating system featuring strong [app sandboxing](https://source.android.com/security/app-sandbox), [Verified Boot](https://source.android.com/security/verifiedboot) (AVB), and a robust [permission](https://developer.android.com/guide/topics/permissions/overview) control system.

## Our Advice

### Выбор Android дистрибутива

When you buy an Android phone, the default operating system comes bundled with apps and functionality that are not part of the Android Open Source Project. Many of these apps—even apps like the dialer which provide basic system functionality—require invasive integrations with Google Play Services, which in turn asks for privileges to access your files, contacts storage, call logs, SMS messages, location, camera, microphone, and numerous other things on your device in order for those basic system apps and many other apps to function in the first place. Frameworks like Google Play Services increase the attack surface of your device and are the source of various privacy concerns with Android.

Эта проблема может быть решена с помощью кастомного дистрибутива Android, который не имеет таких интеграций. К сожалению, многие кастомные дистрибутивы Android часто нарушают модель безопасности Android, не поддерживая критические функции безопасности, такие как AVB, защита rollback, обновления прошивки и так далее. Некоторые дистрибутивы поставляют сборки [`userdebug`](https://source.android.com/setup/build/building#choose-a-target), которые используют root с [ADB](https://developer.android.com/studio/command-line/adb) и требуют [более слабых](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) политик SELinux для активации функций отладки, что приводит к увеличенной поверхности атаки и ослабленной модели безопасности.

В идеале, при выборе кастомного дистрибутива Android, вы должны убедиться, что он поддерживает модель безопасности Android. Как минимум, дистрибутив должен иметь production сборки, поддержку AVB, защиту rollback, своевременные обновления прошивки и операционной системы и SELinux в режиме [enforcing](https://source.android.com/security/selinux/concepts#enforcement_levels). Все рекомендованные нами дистрибутивы Android удовлетворяют этим критериям.

[Наши рекомендации Android :material-arrow-right-drop-circle:](../android.md ""){.md-button}

### Избегайте рутинга

[Рутинг](https://en.wikipedia.org/wiki/Rooting_(Android)) телефонов Android может значительно снизить безопасность, так как ослабляет всю [модель безопасности Android](https://en.wikipedia.org/wiki/Android_(operating_system)#Security_and_privacy). Это может снизить конфиденциальность, если произойдет эксплойт, вызванный снижением безопасности. Обычные методы рутинга предполагают прямое вмешательство в загрузочный раздел, что делает невозможным успешное выполнение проверенной загрузки. Apps that require root will also modify the system partition, meaning that Verified Boot would have to remain disabled. Наличие root непосредственно в пользовательском интерфейсе также увеличивает [поверхность атаки](https://ru.wikipedia.org/wiki/%D0%9F%D0%BE%D0%B2%D0%B5%D1%80%D1%85%D0%BD%D0%BE%D1%81%D1%82%D1%8C_%D0%B0%D1%82%D0%B0%D0%BA%D0%B8) вашего устройства и может помочь в [повышении привилегий](https://ru.wikipedia.org/wiki/%D0%9F%D0%BE%D0%B2%D1%8B%D1%88%D0%B5%D0%BD%D0%B8%D0%B5_%D0%BF%D1%80%D0%B8%D0%B2%D0%B8%D0%BB%D0%B5%D0%B3%D0%B8%D0%B9) уязвимостей и обходе политики SELinux.

Content blockers which modify the [hosts file](https://en.wikipedia.org/wiki/Hosts_(file)) (AdAway) and firewalls (AFWall+) which require root access persistently are dangerous and should not be used. Они также не являются корректным способом решения поставленных перед ними задач. For content blocking, we suggest encrypted [DNS](../dns.md) or content blocking functionality provided by a VPN instead. TrackerControl and AdAway in non-root mode will take up the VPN slot (by using a local loopback VPN), preventing you from using privacy enhancing services such as [Orbot](../tor.md#orbot) or a [real VPN provider](../vpn.md).

AFWall+ работает на основе подхода [пакетной фильтрации](https://ru.wikipedia.org/wiki/%D0%9C%D0%B5%D0%B6%D1%81%D0%B5%D1%82%D0%B5%D0%B2%D0%BE%D0%B9_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD#%D0%9F%D0%B0%D0%BA%D0%B5%D1%82%D0%BD%D1%8B%D0%B5_%D1%84%D0%B8%D0%BB%D1%8C%D1%82%D1%80%D1%8B) и в некоторых ситуациях его можно обойти.

Мы не считаем, что стоит жертвовать безопасностью (получение root-доступа), чтобы получить сомнительные преимущества конфиденциальности.

### Install Updates

Важно не использовать [устаревшую](https://endoflife.date/android) версию Android. Newer versions of Android receive not only security updates for the operating system but also important privacy enhancing updates too.

For example, [prior to Android 10](https://developer.android.com/about/versions/10/privacy/changes) any apps with the [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) permission could access sensitive and unique serial numbers of your phone such as [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), or your SIM card's [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity); whereas now they must be system apps to do so. Системные приложения предоставляются только OEM-производителем или дистрибутивом Android.

### Sharing Media

You can avoid giving many apps permission to access your media with Android's built-in sharing features. Many applications allow you to "share" a file with them for media upload.

For example, if you want to post a picture to Discord you can open your file manager or gallery and share that picture with the Discord app, instead of granting Discord full access to your media and photos.

## Security Protections

### Проверенная загрузка

[Проверенная загрузка](https://source.android.com/docs/security/features/verifiedboot?hl=ru) является важной частью модели безопасности Android. Она обеспечивает защиту от [атак злой горничной](https://encyclopedia.kaspersky.ru/glossary/evil-maid/), сохранения вредоносных программ и гарантирует, что обновления безопасности не могут быть понижены с помощью [защиты от отката](https://source.android.com/security/verifiedboot/verified-boot?hl=ru#rollback-protection).

Android 10 и выше перешел от шифрования всего диска к более гибкому [файловому шифрованию](https://source.android.com/security/encryption/file-based?hl=ru). Ваши данные шифруются с помощью уникальных ключей шифрования, а файлы операционной системы остаются незашифрованными.

Проверенная загрузка обеспечивает целостность файлов операционной системы, тем самым не позволяя недоброжелателям с физическим доступом взломать устройство или установить на него вредоносное ПО. В маловероятном случае, если вредоносное ПО сможет использовать другие части системы и получить более высокий привилегированный доступ, проверенная загрузка предотвратит и отменит изменения в системный раздел при перезагрузке устройства.

К сожалению, OEM-производители обязаны поддерживать проверенную загрузку только в своих стоковых дистрибутивах Android. Лишь некоторые OEM-производители, например Google, поддерживают пользовательскую регистрацию ключей AVB на своих устройствах. Кроме того, некоторые производные AOSP, например LineageOS или /e/ OS, не поддерживают проверенную загрузку даже на девайсах с поддержкой проверенной загрузки для сторонних операционных систем. Мы рекомендуем вам проверить наличие поддержки **перед** покупкой нового устройства. Производные AOSP, которые не поддерживают проверенную загрузку, **не** рекомендуются.

Многие OEM-производители также встраивают сломанную реализацию проверенной загрузки. Вы должны помнить об этом и не обращать внимание на их маркетинг. Например, телефоны Fairphone 3 и 4 не защищены по умолчанию, поскольку [стоковый загрузчик доверяет публичному ключу подписи AVB](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). This breaks verified boot on a stock Fairphone device, as the system will boot alternative Android operating systems (such as /e/) [without any warning](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) about custom operating system usage.

### Обновления прошивки

Обновления прошивки имеют критическое значение для поддержания безопасности. Без них ваше устройство не может быть безопасным. OEM-производители имеют соглашения о поддержке со своими партнерами для предоставления компонентов с закрытым исходным кодом на ограниченный период поддержки. Они подробно описаны в ежемесячных [бюллетенях по безопасности Android](https://source.android.com/docs/security/bulletin?hl=ru).

Поскольку компоненты телефона, такие как процессор и радиотехнологии, полагаются на компоненты с закрытым исходным кодом, обновления должны предоставляться соответствующими производителями. Поэтому важно, чтобы вы приобрели устройство в рамках активного цикла поддержки. [Qualcomm](https://www.qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) and [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox) support their devices for 4 years, while cheaper products often have shorter support cycles. With the introduction of the [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google now makes their own SoC, and they will provide a minimum of 5 years of support. With the introduction of the Pixel 8 series, Google increased that support window to 7 years.

Устройства EOL, которые больше не поддерживаются производителем SoC, не могут получать обновления прошивки от OEM-производителей или дистрибьюторов Android. Это означает, что проблемы безопасности этих устройств останутся неисправленными.

Fairphone, for example, markets their Fairphone 4 device as receiving 6 years of support. Однако SoC (Qualcomm Snapdragon 750G в Fairphone 4) имеет значительно более короткую дату выхода из эксплуатации. Это означает, что обновления безопасности прошивки от Qualcomm для Fairphone 4 закончатся в сентябре 2023 года, независимо от того, будет ли Fairphone продолжать выпускать обновления безопасности программного обеспечения.

### Разрешения в Android

[Разрешения в Android](https://developer.android.com/guide/topics/permissions/overview) дают вам контроль над тем, к чему у приложений будет доступ. Google регулярно вносит [исправления](https://developer.android.com/about/versions/11/privacy/permissions) в систему разрешений в каждой следующей версии Android. Все установленные приложения строго [изолированы](https://source.android.com/security/app-sandbox), поэтому нет необходимости устанавливать антивирусные программы.

Смартфон с последней версией Android всегда будет более безопасен, чем старый смартфон с купленным и установленным антивирусом. Лучше не платить за антивирус, а отложить деньги на покупку нового телефона, например Google Pixel.

Android 10:

- [Scoped Storage](https://developer.android.com/about/versions/10/privacy/changes#scoped-storage) дает вам больше контроля над вашими файлами и позволяет ограничить то, что может [получить доступ к внешнему хранилищу](https://developer.android.com/training/data-storage#permissions). Приложения могут иметь определенный каталог во внешнем хранилище, а также возможность хранить там определенные типы файлов.
- Ужесточение доступа к [местоположению устройства](https://developer.android.com/about/versions/10/privacy/changes#app-access-device-location) путем введения разрешения `ACCESS_BACKGROUND_LOCATION`. Это предотвращает доступ приложений к местоположению при работе в фоновом режиме без специального разрешения пользователя.

Android 11:

- [Одноразовые разрешения](https://developer.android.com/about/versions/11/privacy/permissions#one-time) позволяют вам дать разрешение приложению не навсегда, а только на один раз.
- [Автосброс разрешений](https://developer.android.com/about/versions/11/privacy/permissions#auto-reset), который сбрасывает [разрешения на выполнение](https://developer.android.com/guide/topics/permissions/overview#runtime), которые были предоставлены при открытии приложения.
- Детальные разрешения для доступа к функциям, связанным с [телефонным номером](https://developer.android.com/about/versions/11/privacy/permissions#phone-numbers).

Android 12:

- Разрешение на [примерное местоположение](https://developer.android.com/about/versions/12/behavior-changes-12#approximate-location).
- Автоматический сброс [спящих приложений](https://developer.android.com/about/versions/12/behavior-changes-12#app-hibernation).
- [Аудит доступа к данным](https://developer.android.com/about/versions/12/behavior-changes-12#data-access-auditing), который облегчает определение того, какая часть приложения получает доступ к специфичному типу данных.

Android 13:

- A permission for [nearby Wi-Fi access](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). The MAC addresses of nearby Wi-Fi access points were a popular way for apps to track a user's location.
- Более [детальные разрешения на мультимедиа](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions), то есть вы можете предоставить доступ только к изображениям, видео или аудиофайлам.
- Фоновое использование датчиков теперь требует разрешения [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission).

Приложение может запрашивать разрешения для имеющихся функций. Например, приложение, которое может сканировать QR-коды, запросит разрешение на использование камеры. Некоторые приложения могут запрашивать больше разрешений, чем им нужно.

[Exodus](https://exodus-privacy.eu.org) can be useful when comparing apps that have similar purposes. Если приложение запрашивает много разрешений и имеет много рекламы и аналитики, это вероятно плохой знак. Мы рекомендуем обращать внимание на конкретные трекеры и читать их описание, вместо того, чтобы просто **посчитать их общее количество** и предположить, что они все одинаковые.

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

Если приложение в основном представляет собой веб-сервис, отслеживание может происходить на стороне сервера. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest) shows "no trackers" but certainly does track users' interests and behavior across the site. Приложения могут избежать обнаружения, не используя стандартные библиотеки кода, созданные рекламной индустрией, хотя это маловероятно.

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Privacy-friendly apps such as [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest) may show some trackers such as [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49). Эта библиотека включает [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging), которая нужна для поддержки [push-уведомлений](https://en.wikipedia.org/wiki/Push_technology) в приложениях. Именно [это относится](https://fosstodon.org/@bitwarden/109636825700482007) к Bitwarden. Это не означает, что Bitwarden использует все возможности аналитики, которые предоставляет Google Firebase Analytics.

</div>

## Privacy Features

### Профили пользователей

Профили нескольких пользователей находятся в разделе **Настройки** → **Система** → **Пользователи** и являются самым простым способом изоляции в Android.

С помощью профилей пользователей можно наложить ограничения на определенный профиль, например: совершение звонков, использование SMS или установка приложений на устройство. Каждый профиль шифруется с помощью собственного ключа шифрования и не может получить доступ к данным других профилей. Даже владелец устройства не может просматривать данные других профилей, не зная их пароля. Профили пользователей - это более безопасный метод изоляции.

### Рабочий профиль

[Рабочие профили](https://support.google.com/work/android/answer/6191949?hl=ru&sjid=10752136651864735274-EU) - это еще один способ изолировать отдельные приложения, который может быть более удобным, чем отдельные профили пользователей.

Для создания рабочего профиля, не имея корпоративного MDM, требуется **приложение-контроллер устройства**, такое как [Shelter](../android.md#shelter). Кастомные Android могут содержать такую функцию по умолчанию.

Функционирование рабочего профиля зависит от контроллера устройства. Такие функции, как *File Shuttle* и *блокировка поиска контактов* или любые другие функции изоляции должны быть реализованы контроллером. You must also fully trust the device controller app, as it has full access to your data inside the work profile.

Этот метод обычно менее безопасен, чем второй профиль пользователя; однако он позволяет запускать приложения одновременно в рабочем и личном профилях.

### VPN Killswitch

Android 7 and above supports a VPN kill switch, and it is available without the need to install third-party apps. Эта функция может предотвратить утечку данных в случае отключения VPN. Его можно найти в :gear: **Настройки** → **Сеть и интернет** → **VPN** → :gear: → **Блокировать соединения без VPN**.

### Глобальные переключатели

В современных устройствах Android есть глобальные переключатели для отключения Bluetooth и служб определения местоположения. В Android 12 появились переключатели для камеры и микрофона. Когда эти функции не используются, мы рекомендуем отключать их. Apps cannot use disabled features (even if granted individual permissions) until re-enabled.

## Google Services

If you are using a device with Google services—whether with the stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS—there are a number of additional changes you can make to improve your privacy. Мы по-прежнему рекомендуем полностью отказаться от сервисов Google или ограничить сервисы Google Play определенным профилем пользователя/рабочим профилем, объединив контроллер устройства, такой как *Shelter*, с GrapheneOS's Sandboxed Google Play.

### Дополнительная защита

If you have a Google account we suggest enrolling in the [Advanced Protection Program](https://landing.google.com/advancedprotection). Она доступен бесплатно для всех, у кого есть минимум два аппаратных ключа безопасности с поддержкой [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online). Alternatively, you can use [passkeys](https://fidoalliance.org/passkeys).

Программа дополнительной защиты обеспечивает усиленный мониторинг угроз и активирует:

- Stricter two-factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](https://en.wikipedia.org/wiki/OAuth)
- Только Google и проверенные сторонние приложения могут получить доступ к данным аккаунта
- Сканирование входящих писем на аккаунтах Gmail на наличие [фишинга](https://en.wikipedia.org/wiki/Phishing#Email_phishing)
- Stricter [safe browser scanning](https://google.com/chrome/privacy/whitepaper.html#malware) with Google Chrome
- Более строгий процесс восстановления учетных записей с утраченными учетными данными

 If you use non-sandboxed Google Play Services (common on stock operating systems), the Advanced Protection Program also comes with [additional benefits](https://support.google.com/accounts/answer/9764949) such as:

- Not allowing app installation outside the Google Play Store, the OS vendor's app store, or via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Mandatory automatic device scanning with [Play Protect](https://support.google.com/googleplay/answer/2812853?#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- Предупреждение о непроверенных приложениях

### Обновление Google Play

В прошлом обновления безопасности для Android должны были поставляться производителем операционной системы. Android стал более модульным, начиная с Android 10, и Google может распространять обновления безопасности для **некоторых** системных компонентов через привилегированные службы Play Services.

Если у вас есть устройство EOL, поставляемое с Android 10 или выше, и вы не можете запустить ни одну из рекомендованных нами операционных систем на своем устройстве, вам, скорее всего, лучше придерживаться OEM-установки Android (в отличие от операционной системы, не указанной здесь, например, LineageOS или /e/ OS). Это позволит вам получать **некоторые** исправления безопасности от Google, но при этом не нарушать модель безопасности Android, используя небезопасный вариант Android и увеличивая поверхность атаки. Мы по-прежнему рекомендуем как можно скорее перейти на поддерживаемое устройство.

### Рекламный идентификатор

All devices with Google Play Services installed automatically generate an [advertising ID](https://support.google.com/googleplay/android-developer/answer/6048248) used for targeted advertising. Отключите эту функцию, чтобы ограничить объем собираемых о вас данных.

В дистрибутивах андроид с [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), откройте :gear: **Настройки** → **Приложения** → **Sandboxed Google Play** → **Google Settings** → **Реклама**, и выберите *Удалить рекламный идентификатор*.

В дистрибутивах Android с привилегированными службами Google Play (например, в стоковых ОС) эта настройка может находиться в одном из нескольких мест. Проверьте

- :gear: **Настройки** → **Google** → **Реклама**
- :gear: **Настройки** → **Конфиденциальность** → **Реклама**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads* (this varies between OEM distributions of Android). If presented with the option to delete the advertising ID, that is preferred. Если нет, то обязательно откажитесь и сбросьте свой рекламный ID.

### SafetyNet и Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) и [Play Integrity APIs](https://developer.android.com/google/play/integrity) обычно используются для [банковских приложений](https://grapheneos.org/usage#banking-apps). Многие банковские приложения будут отлично работать в GrapheneOS с "изолированными" Play services, однако некоторые нефинансовые приложения имеют свои собственные слабые механизмы защиты от взлома, которые могут дать сбой. GrapheneOS проходит проверку `basicIntegrity`, но не проверку сертификации `ctsProfileMatch`. Устройства с Android 8 или более поздней версией имеют поддержку аппаратной аттестации, которую невозможно обойти без утечки ключей или серьезных уязвимостей.

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt out if you don't want your credit rating and personal information shared with affiliate marketing services.
