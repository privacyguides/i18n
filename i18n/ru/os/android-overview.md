---
title: Обзор Android
icon: simple/android
description: Android - это операционная система с открытым исходным кодом, обеспечивающая надежную защиту, что делает ее нашим предпочтительным выбором для телефонов.
robots: nofollow, max-snippet:-1, max-image-preview:large
---

![Логотип Android](../assets/img/android/android.svg){ align=right }

**Проект Android с открытым исходным кодом** — это защищенная мобильная операционная система с эффективной [песочницей приложений](https://source.android.com/security/app-sandbox), [проверенной загрузкой](https://source.android.com/security/verifiedboot) (AVB) и надежной системой управления [разрешениями](https://developer.android.com/guide/topics/permissions/overview).

[:octicons-home-16:](https://source.android.com){ .card-link title=Домашняя страница}
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Документация}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/main){ .card-link title="Исходный код" }

[Наши советы по Android :material-arrow-right-drop-circle:](../android/index.md ""){.md-button.md-button--primary}

## Безопасность

Key components of the Android security model include [verified boot](#verified-boot), [firmware updates](#firmware-updates), and a robust [permission system](#android-permissions). These important security features form the baseline of the minimum criteria for our [mobile phone](../mobile-phones.md) and [custom Android OS](../android/distributions.md) recommendations.

### Проверенная загрузка

[**Проверенная загрузка**](https://source.android.com/security/verifiedboot) является важной частью модели безопасности Android. Она обеспечивает защиту от [атак злой горничной](https://encyclopedia.kaspersky.ru/glossary/evil-maid/), сохранения вредоносных программ и гарантирует, что обновления безопасности не могут быть понижены с помощью [защиты от отката](https://source.android.com/security/verifiedboot/verified-boot?hl=ru#rollback-protection).

Android 10 и выше перешел от шифрования всего диска к более гибкому [файловому шифрованию](https://source.android.com/security/encryption/file-based?hl=ru). Ваши данные шифруются с помощью уникальных ключей шифрования, а файлы операционной системы остаются незашифрованными.

Проверенная загрузка обеспечивает целостность файлов операционной системы, тем самым не позволяя недоброжелателям с физическим доступом взломать устройство или установить на него вредоносное ПО. В маловероятном случае, если вредоносное ПО сможет использовать другие части системы и получить более высокий привилегированный доступ, проверенная загрузка предотвратит и отменит изменения в системный раздел при перезагрузке устройства.

К сожалению, OEM-производители обязаны поддерживать проверенную загрузку только в своих стоковых дистрибутивах Android. Лишь некоторые OEM-производители, например Google, поддерживают пользовательскую регистрацию ключей AVB на своих устройствах. Кроме того, некоторые производные AOSP, например LineageOS или /e/ OS, не поддерживают проверенную загрузку даже на девайсах с поддержкой проверенной загрузки для сторонних операционных систем. Мы рекомендуем вам проверить наличие поддержки **перед** покупкой нового устройства. Производные AOSP, которые не поддерживают проверенную загрузку, **не** рекомендуются.

Многие OEM-производители также встраивают сломанную реализацию проверенной загрузки. Вы должны помнить об этом и не обращать внимание на их маркетинг. Например, телефоны Fairphone 3 и 4 не защищены по умолчанию, поскольку [стоковый загрузчик доверяет публичному ключу подписи AVB](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). Это нарушает проверенную загрузку на стоковом устройстве Fairphone, поскольку система будет загружать альтернативные операционные системы Android (например, /e/) [без какого-либо предупреждения](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) об использовании кастомной операционной системы.

### Обновления прошивки

**Обновления прошивки** имеют критическое значение для поддержания безопасности. Без них ваше устройство не может быть безопасным. OEM-производители имеют соглашения о поддержке со своими партнерами для предоставления компонентов с закрытым исходным кодом на ограниченный период поддержки. Они подробно описаны в ежемесячных [бюллетенях по безопасности Android](https://source.android.com/docs/security/bulletin?hl=ru).

Поскольку компоненты телефона, такие как процессор и радиотехнологии, полагаются на компоненты с закрытым исходным кодом, обновления должны предоставляться соответствующими производителями. Поэтому важно, чтобы вы приобрели устройство в рамках активного цикла поддержки. [Qualcomm](https://qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) and [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox) support their devices for 4 years, while cheaper products often have shorter support cycles. With the introduction of the [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google now makes their own SoC, and they will provide a minimum of 5 years of support. With the introduction of the Pixel 8 series, Google increased that support window to 7 years.

Устройства EOL, которые больше не поддерживаются производителем SoC, не могут получать обновления прошивки от OEM-производителей или дистрибьюторов Android. Это означает, что проблемы безопасности этих устройств останутся неисправленными.

Например, Fairphone, утверждает, что Fairphone 4 будет поддерживаться в течение 6 лет. Однако SoC (Qualcomm Snapdragon 750G в Fairphone 4) имеет значительно более короткую дату выхода из эксплуатации. Это означает, что обновления безопасности прошивки от Qualcomm для Fairphone 4 закончатся в сентябре 2023 года, независимо от того, будет ли Fairphone продолжать выпускать обновления безопасности программного обеспечения.

### Разрешения в Android

[**Разрешения в Android**](https://developer.android.com/guide/topics/permissions/overview) дают вам контроль над тем, к чему у приложений будет доступ. Google регулярно вносит [исправления](https://developer.android.com/about/versions/11/privacy/permissions) в систему разрешений в каждой следующей версии Android. Все установленные приложения строго [изолированы](https://source.android.com/security/app-sandbox), поэтому нет необходимости устанавливать антивирусные программы.

Смартфон с последней версией Android всегда будет более безопасен, чем старый смартфон с купленным и установленным антивирусом. Лучше не платить за антивирус, а отложить деньги на покупку нового телефона, например [Google Pixel](../mobile-phones.md#google-pixel).

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

- A permission for [nearby Wi-Fi access](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). MAC-адреса близлежащих точек доступа WiFi были распространённым способом для приложений отслеживать местоположение пользователя.
- Более [детальные разрешения на мультимедиа](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions), то есть вы можете предоставить доступ только к изображениям, видео или аудиофайлам.
- Фоновое использование датчиков теперь требует разрешения [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission).

Приложение может запрашивать разрешения для имеющихся функций. Например, приложение, которое может сканировать QR-коды, запросит разрешение на использование камеры. Некоторые приложения могут запрашивать больше разрешений, чем им нужно.

[Exodus](https://exodus-privacy.eu.org) полезен при сравнении приложений с похожими функциями. Если приложение запрашивает много разрешений и имеет много рекламы и аналитики, это вероятно плохой знак. Мы рекомендуем обращать внимание на конкретные трекеры и читать их описание, вместо того, чтобы просто **посчитать их общее количество** и предположить, что они все одинаковые.

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

Если приложение в основном представляет собой веб-сервис, отслеживание может происходить на стороне сервера. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest) не показывает трекеров, но, безусловно, отслеживает интересы и поведение пользователей на сайте. Приложения могут избежать обнаружения, не используя стандартные библиотеки кода, созданные рекламной индустрией, хотя это маловероятно.

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Примечание</p>

Приложения, уважающие вашу конфиденциальность, например [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest), могут показывать некоторые трекеры, например [Google Firebase Analytics] (https://reports.exodus-privacy.eu.org/en/trackers/49). Эта библиотека включает [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging), которая нужна для поддержки [push-уведомлений](https://en.wikipedia.org/wiki/Push_technology) в приложениях. Именно [это относится](https://fosstodon.org/@bitwarden/109636825700482007) к Bitwarden. Это не означает, что Bitwarden использует все возможности аналитики, которые предоставляет Google Firebase Analytics.

</div>

## Конфиденциальность

### Профили пользователей

Multiple **user profiles** can be found in :gear: **Settings** → **System** → **Users** and are the simplest way to isolate in Android.

With user profiles, you can impose restrictions on a specific profile, such as: making calls, using SMS, or installing apps. Каждый профиль шифруется с помощью собственного ключа шифрования и не может получить доступ к данным других профилей. Даже владелец устройства не может просматривать данные других профилей, не зная их пароля. Профили пользователей - это более безопасный метод изоляции.

### Рабочий профиль

[**Work Profiles**](https://support.google.com/work/android/answer/6191949) are another way to isolate individual apps and may be more convenient than separate user profiles.

A **device controller** app such as [Shelter](../android/general-apps.md#shelter) is required to create a Work Profile without an enterprise MDM, unless you're using a custom Android OS which includes one.

Функционирование рабочего профиля зависит от контроллера устройства. Такие функции, как *File Shuttle* и *блокировка поиска контактов* или любые другие функции изоляции должны быть реализованы контроллером. You must also fully trust the device controller app, as it has full access to your data inside the work profile.

This method is generally less secure than a secondary user profile; however, it does allow you the convenience of running apps in both the owner profile and work profile simultaneously.

### Private Space

**Private Space** is a feature introduced in Android 15 that adds another way of isolating individual apps. You can set up a private space in the owner profile by navigating to :gear: **Settings** → **Security & privacy** → **Private space**. Once set up, your private space resides at the bottom of the app drawer.

Like user profiles, a private space is encrypted using its own encryption key, and you have the option to set up a different unlock method. Like work profiles, you can use apps from both the owner profile and private space simultaneously. Apps launched from a private space are distinguished by an icon depicting a key within a shield.

Unlike work profiles, Private Space is a feature native to Android that does not require a third-party app to manage it. For this reason, we generally recommend using a private space over a work profile, though you can use a work profile alongside a private space.

### VPN kill switch

Android 7 and above supports a VPN kill switch, and it is available without the need to install third-party apps. Эта функция может предотвратить утечку данных в случае отключения VPN. Его можно найти в :gear: **Настройки** → **Сеть и интернет** → **VPN** → :gear: → **Блокировать соединения без VPN**.

### Глобальные переключатели

В современных устройствах Android есть глобальные переключатели для отключения Bluetooth и служб определения местоположения. В Android 12 появились переключатели для камеры и микрофона. Когда эти функции не используются, мы рекомендуем отключать их. Apps cannot use disabled features (even if granted individual permissions) until re-enabled.

## Сервисы Google

If you are using a device with Google services—whether with the stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS—there are a number of additional changes you can make to improve your privacy. We still recommend avoiding Google services entirely, or limiting Google Play Services to a specific user/work profile by combining a device controller like *Shelter* with GrapheneOS's Sandboxed Google Play.

### Дополнительная защита

If you have a Google account we suggest enrolling in the [Advanced Protection Program](https://landing.google.com/advancedprotection). Она доступен бесплатно для всех, у кого есть минимум два аппаратных ключа безопасности с поддержкой [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online). Alternatively, you can use [passkeys](https://fidoalliance.org/passkeys).

Программа дополнительной защиты обеспечивает усиленный мониторинг угроз и активирует:

- Stricter two-factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](../basics/account-creation.md#sign-in-with-oauth)
- Только Google и проверенные сторонние приложения могут получить доступ к данным аккаунта
- Сканирование входящих писем на аккаунтах Gmail на наличие [фишинга](https://en.wikipedia.org/wiki/Phishing#Email_phishing)
- Stricter [safe browser scanning](https://google.com/chrome/privacy/whitepaper.html#malware) with Google Chrome
- Более строгий процесс восстановления учетных записей с утраченными учетными данными

 If you use non-sandboxed Google Play Services (common on stock operating systems), the Advanced Protection Program also comes with [additional benefits](https://support.google.com/accounts/answer/9764949) such as:

- Not allowing app installation outside the Google Play Store, the OS vendor's app store, or via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Mandatory automatic device scanning with [Play Protect](https://support.google.com/googleplay/answer/2812853?#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- Предупреждение о непроверенных приложениях
- Enabling ARM's hardware-based [Memory Tagging Extension (MTE)](https://developer.arm.com/documentation/108035/0100/Introduction-to-the-Memory-Tagging-Extension) for supported apps, which lowers the likelihood of device exploits happening through memory corruption bugs

### Обновление Google Play

В прошлом обновления безопасности для Android должны были поставляться производителем операционной системы. Android стал более модульным, начиная с Android 10, и Google может распространять обновления безопасности для **некоторых** системных компонентов через привилегированные службы Play Services.

Если у вас есть устройство EOL, поставляемое с Android 10 или выше, и вы не можете запустить ни одну из рекомендованных нами операционных систем на своем устройстве, вам, скорее всего, лучше придерживаться OEM-установки Android (в отличие от операционной системы, не указанной здесь, например, LineageOS или /e/ OS). Это позволит вам получать **некоторые** исправления безопасности от Google, но при этом не нарушать модель безопасности Android, используя небезопасный вариант Android и увеличивая поверхность атаки. Мы по-прежнему рекомендуем как можно скорее перейти на поддерживаемое устройство.

### Рекламный идентификатор

All devices with Google Play Services installed automatically generate an [advertising ID](https://support.google.com/googleplay/android-developer/answer/6048248) used for targeted advertising. Отключите эту функцию, чтобы ограничить объем собираемых о вас данных.

On Android distributions with [sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), go to :gear: **Settings** → **Apps** → **Sandboxed Google Play** → **Google Settings** → **All services** → **Ads**.

- [x] Select **Delete advertising ID**

On Android distributions with privileged Google Play Services (which includes the stock installation on most devices), the setting may be in one of several locations. Проверьте

- :gear: **Настройки** → **Google** → **Реклама**
- :gear: **Настройки** → **Конфиденциальность** → **Реклама**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads* (this varies between OEM distributions of Android). If presented with the option to delete the advertising ID, that is preferred. Если нет, то обязательно откажитесь и сбросьте свой рекламный ID.

### SafetyNet и Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) и [Play Integrity APIs](https://developer.android.com/google/play/integrity) обычно используются для [банковских приложений](https://grapheneos.org/usage#banking-apps). Многие банковские приложения будут отлично работать в GrapheneOS с "изолированными" Play services, однако некоторые нефинансовые приложения имеют свои собственные слабые механизмы защиты от взлома, которые могут дать сбой. GrapheneOS проходит проверку `basicIntegrity`, но не проверку сертификации `ctsProfileMatch`. Устройства с Android 8 или более поздней версией имеют поддержку аппаратной аттестации, которую невозможно обойти без утечки ключей или серьезных уязвимостей.

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt out if you don't want your credit rating and personal information shared with affiliate marketing services.
