---
title: Обзор Android
icon: simple/android
description: Android - это операционная система с открытым исходным кодом, которая предоставляет надежную защиту, что делает ее нашим главным выбором для телефонов.
---

Android является безопасной операционной системой, имеющей мощную [изоляцию приложений](https://source.android.com/security/app-sandbox), [проверенную загрузка](https://source.android.com/security/verifiedboot) (AVB) и надежную систему управления [разрешениями](https://developer.android.com/guide/topics/permissions/overview).

## Выбор Android дистрибутива

При покупке Android телефона, стандартная операционная система часто содержит приложения и интеграции с сервисами, которые не являются частью [проекта с открытым исходным кодом Android](https://source.android.com/). Примером могут служить Google Play Services, которые имеют неотменяемые привилегии на доступ к вашим файлам, хранилищу контактов, журналам вызовов, SMS-сообщениям, местоположению, камере, микрофону, аппаратным идентификаторам и так далее. Эти приложения и службы увеличивают поверхность атаки вашего устройства и являются источником различных проблем с конфиденциальностью в Android.

Эта проблема может быть решена с помощью кастомного дистрибутива Android, который не имеет таких интеграций. К сожалению, многие кастомные дистрибутивы Android часто нарушают модель безопасности Android, не поддерживая критические функции безопасности, такие как AVB, защита rollback, обновления прошивки и так далее. Некоторые дистрибутивы поставляют сборки [`userdebug`](https://source.android.com/setup/build/building#choose-a-target), которые используют root с [ADB](https://developer.android.com/studio/command-line/adb) и требуют [более слабых](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) политик SELinux для активации функций отладки, что приводит к увеличенной поверхности атаки и ослабленной модели безопасности.

В идеале, при выборе кастомного дистрибутива Android, вы должны убедиться, что он поддерживает модель безопасности Android. Как минимум, дистрибутив должен иметь production сборки, поддержку AVB, защиту rollback, своевременные обновления прошивки и операционной системы и SELinux в режиме [enforcing](https://source.android.com/security/selinux/concepts#enforcement_levels). Все рекомендованные нами дистрибутивы Android удовлетворяют этим критериям.

[Наши рекомендации Android :material-arrow-right-drop-circle:](../android.md ""){.md-button}

## Избегайте рутинга

[Рутинг](https://en.wikipedia.org/wiki/Rooting_(Android)) телефонов Android может значительно снизить безопасность, так как ослабляет всю [модель безопасности Android](https://en.wikipedia.org/wiki/Android_(operating_system)#Security_and_privacy). Это может снизить конфиденциальность, если произойдет эксплойт, вызванный снижением безопасности. Обычные методы рутинга предполагают прямое вмешательство в загрузочный раздел, что делает невозможным успешное выполнение проверенной загрузки. Приложения, требующие root, также будут изменять системный раздел, это означает, что проверенную загрузку придется отключить. Наличие root непосредственно в пользовательском интерфейсе также увеличивает [поверхность атаки](https://ru.wikipedia.org/wiki/%D0%9F%D0%BE%D0%B2%D0%B5%D1%80%D1%85%D0%BD%D0%BE%D1%81%D1%82%D1%8C_%D0%B0%D1%82%D0%B0%D0%BA%D0%B8) вашего устройства и может помочь в [повышении привилегий](https://ru.wikipedia.org/wiki/%D0%9F%D0%BE%D0%B2%D1%8B%D1%88%D0%B5%D0%BD%D0%B8%D0%B5_%D0%BF%D1%80%D0%B8%D0%B2%D0%B8%D0%BB%D0%B5%D0%B3%D0%B8%D0%B9) уязвимостей и обходе политики SELinux.

Адблокеры, которые изменяют [файл hosts](https://en.wikipedia.org/wiki/Hosts_(file)) (AdAway) и брандмауэры (AFWall+), которые постоянно требуют root-доступ, опасны и не должны использоваться. Они также не являются корректным способом решения поставленных перед ними задач. Для блокировки рекламы мы предлагаем зашифрованные [DNS](../dns.md) или [VPN](../vpn.md) с функцией блокировки рекламы. RethinkDNS, TrackerControl и AdAway в режиме без root-доступа будут занимать слот VPN (используя локальный loopback VPN), не позволяя вам использовать службы, повышающие конфиденциальность, такие как Orbot или настоящий VPN-сервер.

AFWall+ работает на основе подхода [пакетной фильтрации](https://ru.wikipedia.org/wiki/%D0%9C%D0%B5%D0%B6%D1%81%D0%B5%D1%82%D0%B5%D0%B2%D0%BE%D0%B9_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD#%D0%9F%D0%B0%D0%BA%D0%B5%D1%82%D0%BD%D1%8B%D0%B5_%D1%84%D0%B8%D0%BB%D1%8C%D1%82%D1%80%D1%8B) и в некоторых ситуациях его можно обойти.

Мы не считаем, что стоит жертвовать безопасностью (получение root-доступа), чтобы получить сомнительные преимущества конфиденциальности.

## Проверенная загрузка

[Проверенная загрузка](https://source.android.com/docs/security/features/verifiedboot?hl=ru) является важной частью модели безопасности Android. Она обеспечивает защиту от [атак злой горничной](https://encyclopedia.kaspersky.ru/glossary/evil-maid/), сохранения вредоносных программ и гарантирует, что обновления безопасности не могут быть понижены с помощью [защиты от отката](https://source.android.com/security/verifiedboot/verified-boot?hl=ru#rollback-protection).

Android 10 и выше перешел от шифрования всего диска к более гибкому [файловому шифрованию](https://source.android.com/security/encryption/file-based?hl=ru). Ваши данные шифруются с помощью уникальных ключей шифрования, а файлы операционной системы остаются незашифрованными.

Проверенная загрузка обеспечивает целостность файлов операционной системы, тем самым не позволяя недоброжелателям с физическим доступом взломать устройство или установить на него вредоносное ПО. В маловероятном случае, если вредоносное ПО сможет использовать другие части системы и получить более высокий привилегированный доступ, проверенная загрузка предотвратит и отменит изменения в системный раздел при перезагрузке устройства.

К сожалению, OEM-производители обязаны поддерживать проверенную загрузку только в своих стоковых дистрибутивах Android. Лишь некоторые OEM-производители, например Google, поддерживают пользовательскую регистрацию ключей AVB на своих устройствах. Кроме того, некоторые производные AOSP, например LineageOS или /e/ OS, не поддерживают проверенную загрузку даже на девайсах с поддержкой проверенной загрузки для сторонних операционных систем. Мы рекомендуем вам проверить наличие поддержки **перед** покупкой нового устройства. Производные AOSP, которые не поддерживают проверенную загрузку, **не** рекомендуются.

Многие OEM-производители также встраивают сломанную реализацию проверенной загрузки. Вы должны помнить об этом и не обращать внимание на их маркетинг. Например, телефоны Fairphone 3 и 4 не защищены по умолчанию, поскольку [стоковый загрузчик доверяет публичному ключу подписи AVB](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). Это нарушает проверенную загрузку на стоковом устройстве Fairphone, поскольку система будет загружать альтернативные операционные системы Android, такие как (например, /e/) [без какого-либо предупреждения](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) об использовании кастомной операционной системы.

## Обновления прошивки

Firmware updates are critical for maintaining security and without them your device cannot be secure. OEMs have support agreements with their partners to provide the closed-source components for a limited support period. These are detailed in the monthly [Android Security Bulletins](https://source.android.com/security/bulletin).

As the components of the phone, such as the processor and radio technologies rely on closed-source components, the updates must be provided by the respective manufacturers. Therefore, it is important that you purchase a device within an active support cycle. [Qualcomm](https://www.qualcomm.com/news/releases/2020/12/16/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) and [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox/) support their devices for 4 years, while cheaper products often have shorter support cycles. With the introduction of the [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google now makes their own SoC and they will provide a minimum of 5 years of support.

EOL devices which are no longer supported by the SoC manufacturer cannot receive firmware updates from OEM vendors or after market Android distributors. This means that security issues with those devices will remain unfixed.

Fairphone, for example, markets their devices as receiving 6 years of support. However, the SoC (Qualcomm Snapdragon 750G on the Fairphone 4) has a considerably shorter EOL date. This means that firmware security updates from Qualcomm for the Fairphone 4 will end in September 2023, regardless of whether Fairphone continues to release software security updates.

## Версии Android

It's important to not use an [end-of-life](https://endoflife.date/android) version of Android. Newer versions of Android not only receive security updates for the operating system but also important privacy enhancing updates too. For example, [prior to Android 10](https://developer.android.com/about/versions/10/privacy/changes), any apps with the [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) permission could access sensitive and unique serial numbers of your phone such as [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), your SIM card's [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity), whereas now they must be system apps to do so. System apps are only provided by the OEM or Android distribution.

## Разрешения в Android

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

- Разрешение на [доступ к устройствам wifi поблизости](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). MAC-адреса близлежащих точек доступа WiFi были популярным способом для приложений отслеживать местоположение пользователя.
- Более [детальные разрешения на мультимедиа](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions), то есть вы можете предоставить доступ только к изображениям, видео или аудиофайлам.
- Фоновое использование датчиков теперь требует разрешения [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission).

Приложение может запрашивать разрешения для имеющихся функций. Например, приложение, которое может сканировать QR-коды, запросит разрешение на использование камеры. Некоторые приложения могут запрашивать больше разрешений, чем им нужно.

[Exodus](https://exodus-privacy.eu.org/) может быть полезен при сравнении приложений с похожими функциями. Если приложение запрашивает много разрешений и имеет много рекламы и аналитики, это вероятно плохой знак. Мы рекомендуем обращать внимание на конкретные трекеры и читать их описание, вместо того, чтобы просто **посчитать их общее количество** и предположить, что они все одинаковые.

!!! warning "Осторожно"

    Если приложение в основном представляет собой веб-сервис, отслеживание может происходить на стороне сервера. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest/) показывает 0 трекеров, но, безусловно, отслеживает интересы и поведение пользователей на сайте. Приложения могут избежать обнаружения, не используя стандартные библиотеки кода, созданные рекламной индустрией, хотя это маловероятно.

!!! note "Примечание"

    Приложения, уважающие вашу конфиденциальность, например [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest/), могут показывать некоторые трекеры, например [Google Firebase Analytics] (https://reports.exodus-privacy.eu.org/en/trackers/49/). Эта библиотека включает [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging), которая нужна для поддержки [push-уведомлений](https://en.wikipedia.org/wiki/Push_technology) в приложениях. Именно [это относится](https://fosstodon.org/@bitwarden/109636825700482007) к Bitwarden. Это не означает, что Bitwarden использует все возможности аналитики, которые предоставляет Google Firebase Analytics.

## Доступ к файлам

Довольно многие приложения позволяют "поделиться" файлом для загрузки медиафайла. Если вы хотите, например, отправить фотографию в Twitter, не предоставляйте Twitter доступ к вашим "медиа и фотографиям", потому что тогда у него будет доступ ко всем вашим фотографиям. Вместо этого зайдите в файловый менеджер (или галерею), долго нажмите на фотографию, а затем поделитесь ею в Twitter.

## Профили пользователей

Профили нескольких пользователей находятся в разделе **Настройки** → **Система** → **Пользователи** и являются самым простым способом изоляции в Android.

С помощью профилей пользователей можно наложить ограничения на определенный профиль, например: совершение звонков, использование SMS или установка приложений на устройство. Каждый профиль шифруется с помощью собственного ключа шифрования и не может получить доступ к данным других профилей. Даже владелец устройства не может просматривать данные других профилей, не зная их пароля. Профили пользователей - это более безопасный метод изоляции.

## Рабочий профиль

[Рабочие профили](https://support.google.com/work/android/answer/6191949?hl=ru&sjid=10752136651864735274-EU) - это еще один способ изолировать отдельные приложения, который может быть более удобным, чем отдельные профили пользователей.

Для создания рабочего профиля, не имея корпоративного MDM, требуется **приложение-контроллер устройства**, такое как [Shelter](../android.md#shelter). Кастомные Android могут содержать такую функцию по умолчанию.

Функционирование рабочего профиля зависит от контроллера устройства. Такие функции, как *File Shuttle* и *блокировка поиска контактов* или любые другие функции изоляции должны быть реализованы контроллером. Вы также должны полностью доверять приложению-контроллеру устройства, поскольку оно имеет полный доступ к вашим данным внутри рабочего профиля.

Этот метод обычно менее безопасен, чем второй профиль пользователя; однако он позволяет запускать приложения одновременно в рабочем и личном профилях.

## VPN Killswitch

Android 7 и выше поддерживает VPN killswitch, и он доступен без необходимости установки сторонних приложений. Эта функция может предотвратить утечку данных в случае отключения VPN. Его можно найти в :gear: **Настройки** → **Сеть и интернет** → **VPN** → :gear: → **Блокировать соединения без VPN**.

## Глобальные переключатели

В современных устройствах Android есть глобальные переключатели для отключения Bluetooth и служб определения местоположения. В Android 12 появились переключатели для камеры и микрофона. Когда эти функции не используются, мы рекомендуем отключать их. Приложения не могут использовать отключенные функции (даже при наличии индивидуального разрешения) до тех пор, пока они не будут снова включены.

## Google

Если вы используете устройство с Google сервисами, либо стоковой операционной системой, либо операционной системой, которая безопасно изолирует службы Google Play, например GrapheneOS, вы можете внести ряд дополнительных изменений для повышения конфиденциальности. Мы по-прежнему рекомендуем полностью отказаться от сервисов Google или ограничить сервисы Google Play определенным профилем пользователя/рабочим профилем, объединив контроллер устройства, такой как *Shelter*, с GrapheneOS's Sandboxed Google Play.

### Дополнительная защита

Если у вас есть учетная запись Google, мы рекомендуем вам зарегистрироваться в [программе дополнительной защиты](https://landing.google.com/intl/ru/advancedprotection/). Она доступен бесплатно для всех, у кого есть минимум два аппаратных ключа безопасности с поддержкой [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online).

Программа дополнительной защиты обеспечивает усиленный мониторинг угроз и активирует:

- Более строгую двухфакторную аутентификацую; например, [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **должна** использоваться и запрещено использование [СМС OTP](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) и [OAuth](https://en.wikipedia.org/wiki/OAuth)
- Только Google и проверенные сторонние приложения могут получить доступ к данным аккаунта
- Сканирование входящих писем на аккаунтах Gmail на наличие [фишинга](https://en.wikipedia.org/wiki/Phishing#Email_phishing)
- Более строгое [сканирование безопасного просмотра](https://www.google.com/chrome/privacy/whitepaper.html#malware) в Google Chrome
- Более строгий процесс восстановления учетных записей с утраченными учетными данными

 Если вы пользуетесь службами Google Play без "песочницы" (часто встречающимися в стоковых операционных системах), программа дополнительной защиты также включает [дополнительные преимущества](https://support.google.com/accounts/answer/9764949?hl=en), например:

- Разрешена установка приложений только из Google Play Store, магазина приложений производителя ОС или через [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Обязательное автоматическое сканирование устройств с помощью [Play Защиты](https://support.google.com/googleplay/answer/2812853?hl=en#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- Предупреждение о непроверенных приложениях

### Обновление Google Play

In the past, Android security updates had to be shipped by the operating system vendor. Android has become more modular beginning with Android 10, and Google can push security updates for **some** system components via the privileged Play Services.

If you have an EOL device shipped with Android 10 or above and are unable to run any of our recommended operating systems on your device, you are likely going to be better off sticking with your OEM Android installation (as opposed to an operating system not listed here such as LineageOS or /e/ OS). This will allow you to receive **some** security fixes from Google, while not violating the Android security model by using an insecure Android derivative and increasing your attack surface. We would still recommend upgrading to a supported device as soon as possible.

### Рекламный идентификатор

All devices with Google Play Services installed automatically generate an [advertising ID](https://support.google.com/googleplay/android-developer/answer/6048248?hl=en) used for targeted advertising. Disable this feature to limit the data collected about you.

В дистрибутивах андроид с [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), откройте :gear: **Настройки** → **Приложения** → **Sandboxed Google Play** → **Google Settings** → **Реклама**, и выберите *Удалить рекламный идентификатор*.

On Android distributions with privileged Google Play Services (such as stock OSes), the setting may be in one of several locations. Check

- :gear: **Настройки** → **Google** → **Реклама**
- :gear: **Настройки** → **Конфиденциальность** → **Реклама**

У вас либо будет опция удаления рекламного идентификатора либо опция *отключения рекламы, основанной на интересах*, это варьируется в зависимости от производителя. If presented with the option to delete the advertising ID that is preferred. If not, then make sure to opt out and reset your advertising ID.

### SafetyNet и Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) and the [Play Integrity APIs](https://developer.android.com/google/play/integrity) are generally used for [banking apps](https://grapheneos.org/usage#banking-apps). Many banking apps will work fine in GrapheneOS with sandboxed Play services, however some non-financial apps have their own crude anti-tampering mechanisms which might fail. GrapheneOS passes the `basicIntegrity` check, but not the certification check `ctsProfileMatch`. Devices with Android 8 or later have hardware attestation support which cannot be bypassed without leaked keys or serious vulnerabilities.

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt-out if you don't want your credit rating and personal information shared with affiliate marketing services.
