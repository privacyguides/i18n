---
meta_title: "Рекомендации по Android: GrapheneOS и DivestOS - Privacy Guides"
title: "Android"
icon: 'simple/android'
description: Вы можете заменить операционную систему на своем Android на эти безопасные и конфиденциальные альтернативы.
cover: android.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Приватные операционные системы Android
    url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: Android
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://ru.wikipedia.org/wiki/Android
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: Divest
    image: /assets/img/android/divestos.svg
    url: https://divestos.org/
    sameAs: https://en.wikipedia.org/wiki/DivestOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": Product
    name: Pixel
    brand:
      "@type": Brand
      name: Google
    image: /assets/img/android/google-pixel.png
    sameAs: https://ru.wikipedia.org/wiki/Google_Pixel
    review:
      "@type": Review
      author:
        "@type": Organization
        name: Privacy Guides
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Shelter
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Auditor
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Secure Camera
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Secure PDF Viewer
    applicationCategory: Utilities
    operatingSystem: Android
---

![Логотип Android](assets/img/android/android.svg){ align=right }

**Проект с открытым исходным кодом Android** - это мобильная операционная система с открытым исходным кодом под руководством Google, на которой работает большинство мобильных устройств в мире. Большинство телефонов, продаваемых с ОС Android, модифицированы для включения инвазивных интеграций и приложений, таких как Google Play Services, поэтому вы можете значительно улучшить свою конфиденциальность на мобильном устройстве, заменив стандартную ОС телефона на версию Android без этих инвазивных функций.

[:octicons-home-16:](https://source.android.com/){ .card-link title=Домашняя страница}
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Документация}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/){ .card-link title="Исходный код" }

Это операционные системы, устройства и приложения для Android, которые мы рекомендуем для обеспечения максимальной безопасности и конфиденциальности вашего мобильного устройства. Чтобы узнать больше об Android:

[Общий обзор Android :material-arrow-right-drop-circle:](os/android-overview.md ""){.md-button}

## Основанные на AOSP

Мы рекомендуем установить на ваше устройство одну из этих кастомных операционных систем Android, перечисленных в порядке предпочтения, в зависимости от совместимости вашего устройства с этими операционными системами.

!!! note "Примечание"

    Устройства с истекшим сроком службы (например устройства с GrapheneOS или с "расширенной поддержкой" CalyxOS) не имеют полных исправлений безопасности (обновлений прошивки) из-за прекращения поддержки OEM-производителем. Эти устройства нельзя считать полностью безопасными, независимо от установленного программного обеспечения.

### GrapheneOS

!!! recommendation

    ![Логотип GrapheneOS](assets/img/android/grapheneos.svg#only-light){ align=right }
    ![Логотип GrapheneOS](assets/img/android/grapheneos-dark.svg#only-dark){ align=right }
    
    **GrapheneOS** - это лучший выбор для вашей безопасности и конфиденциальности.
    
    GrapheneOS обеспечивает дополнительное [улучшение безопасности](https://en.wikipedia.org/wiki/Hardening_(computing)) и улучшение конфиденциальности. Она имеет [улучшенный memory allocator] (https://github.com/GrapheneOS/hardened_malloc), сетевые и сенсорные разрешения и другие различные [функции безопасности] (https://grapheneos.org/features). GrapheneOS также поставляется с полными обновлениями прошивки и подписанными сборками, поэтому проверенная загрузка полностью поддерживается.
    
    [:octicons-home-16: Домашняя страница](https://grapheneos.org/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Политика Конфиденциальности" }
    [:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Документация}
    [:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Поддержать }

GrapheneOS поддерживает [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), который запускает [Google Play Services](https://en.wikipedia.org/wiki/Google_Play_Services) полностью в песочнице, как любое другое обычное приложение. Это означает, что вы можете использовать преимущества большинства служб Google Play, таких как [push-уведомления](https://firebase.google.com/docs/cloud-messaging/), полностью контролируя их разрешения и доступ, а также ограничивая их определенным [рабочим профилем](os/android-overview.md#work-profile) или [профилем пользователя](os/android-overview.md#user-profiles) по вашему выбору.

Телефоны Google Pixel - единственные устройства, которые в настоящее время отвечают [требованиям аппаратной безопасности](https://grapheneos.org/faq#device-support) GrapheneOS.

[Почему мы рекомендуем GrapheneOS, а не CalyxOS :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/ ""){.md-button}

### DivestOS

!!! recommendation

    ![Логотип DivestOS](assets/img/android/divestos.svg){ align=right }
    
    **DivestOS** - это лёгкий форк [LineageOS](https://lineageos.org/).
    DivestOS наследует многие [поддерживаемые устройства](https://divestos.org/index.php?page=devices&base=LineageOS) от LineageOS. Он имеет подписанные сборки, что делает возможным [verified boot](https://source.android.com/security/verifiedboot) на некоторых не-Pixel устройствах.
    
    [:octicons-home-16: Домашняя страница](https://divestos.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Сервис Onion" }
    [:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Поддержать }

DivestOS имеет автоматизированное ([CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [исправление](https://gitlab.com/divested-mobile/cve_checker) уязвимостей ядра, меньше проприетарных зависимостей и кастомный [hosts](https://divested.dev/index.php?page=dnsbl) файл. Его улучшенный WebView, [Mulch](https://gitlab.com/divested-mobile/mulch), обеспечивает [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) для всех архитектур и [разделение состояния сети](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning), а также получает out-of-bands обновления. DivestOS также включает патчи ядра от GrapheneOS и включает все доступные функции безопасности ядра с помощью [defconfig hardening](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). Все ядра новее версии 3.4 включают полную [очистку](https://lwn.net/Articles/334747/) страницы и все ~22 Clang-компилированных ядра активируют [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471).

В DivestOS реализованы некоторые патчи для защиты системы, изначально разработанные для GrapheneOS. В DivestOS 16.0 и выше реализованы переключатели из GrapheneOS для [`интернета`](https://developer.android.com/training/basics/network-ops/connecting) и сенсоров, [улучшенный memory allocator](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/#additional-hardening), [JNI](https://en.wikipedia.org/wiki/Java_Native_Interface) [constification](https://en.wikipedia.org/wiki/Const_(computer_programming)), и частичные патчи [bionic](https://en.wikipedia.org/wiki/Bionic_(software)). В версии 17.1 и выше GrapheneOS поддерживает полную [рандомизацию MAC-адресов](https://en.wikipedia.org/wiki/MAC_address#Randomization) для каждой сети, управление [`ptrace_scope`](https://www.kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) и [таймеры](https://grapheneos.org/features) для автоматического выключения Wi-Fi/Bluetooth или перезагрузки телефона.

DivestOS использует F-Droid в качестве магазина приложений по умолчанию. Обычно мы рекомендуем избегать F-Droid из-за его многочисленных [проблем с безопасностью](#f-droid). Однако на DivestOS это сделать невозможно: разработчики обновляют свои приложения через собственные репозитории F-Droid ([DivestOS Official](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) и [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2)). Мы рекомендуем отключить официальное приложение F-Droid и использовать [Neo Store](https://github.com/NeoApplications/Neo-Store/) с включенными репозиториями DivestOS, чтобы поддерживать эти компоненты в актуальном состоянии. Для других приложений по-прежнему действуют рекомендованные нами способы их получения.

!!! warning "Осторожно"

    [Статус](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) обновлений прошивки DivestOS и контроль качества варьируются в зависимости от поддерживаемых устройств. Мы по-прежнему рекомендуем GrapheneOS, если ваш телефон её поддерживает. Для других устройств хорошей альтернативой является DivestOS.
    
    Не все поддерживаемые устройства имеют функцию проверенной загрузки, а некоторые выполняют ее лучше, чем другие.

## Android-устройства

При покупке устройства рекомендуем приобрести как можно более новое. ПО и прошивка мобильных устройств поддерживаются только в течение ограниченного периода времени, поэтому покупка нового устройства продлевает его жизненный цикл настолько, насколько это возможно.

Избегайте покупки телефонов у операторов мобильной связи. У них часто **заблокирован загрузчик** и они не поддерживают [OEM разблокировку](https://source.android.com/devices/bootloader/locking_unlocking). Эти варианты телефонов не позволят вам установить какой-либо альтернативный дистрибутив Android.

Будьте **очень осторожны** при покупке подержанных телефонов в интернет-магазинах. Всегда проверяйте репутацию продавца. Если устройство украдено, существует вероятность [внесения его IMEI в черный список](https://www.gsma.com/security/resources/imei-blacklisting/). Также существует риск связывания вас с действиями предыдущего владельца устройства.

Еще несколько советов относительно устройств Android и совместимости с операционной системой:

- Не покупайте устройства, срок службы которых истек или близок к концу, дополнительные обновления прошивки должны быть предоставлены производителем.
- Не покупайте телефоны с предустановленной LineageOS или /e/ OS или любые телефоны Android без надлежащей поддержки [проверенной загрузки (Verified Boot)](https://source.android.com/security/verifiedboot?hl=ru) и обновлений прошивки. Вы также не сможете проверить, взломаны ли эти устройства.
- Короче, если устройство или дистрибутив Android не указаны в этом списке, вероятно, на это есть веская причина. Загляните на наш [форум](https://discuss.privacyguides.net/), чтобы узнать подробности!

### Google Pixel

Телефоны Google Pixel - это **единственные** устройства, которые мы рекомендуем к покупке. Телефоны Pixel имеют более высокий уровень аппаратной безопасности, чем любые другие устройства Android, представленные в настоящее время на рынке, благодаря надлежащей поддержке AVB для сторонних операционных систем и кастомным чипам безопасности Google [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html), выступающим в качестве элемента безопасности.

!!! recommendation

    ![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }
    
    Устройства **Google Pixel** известны хорошей безопасностью и правильной поддержкой [Verified Boot](https://source.android.com/security/verifiedboot), даже при установке сторонних операционных систем.
    
    Начиная с **Pixel 6** и **6 Pro**, устройства Pixel получают минимум 5 лет гарантированных обновлений безопасности, что обеспечивает гораздо более длительный срок службы по сравнению с 2-4 годами, которые обычно предлагают конкурирующие OEM-производители.
    
    [:material-shopping: Магазин](https://store.google.com/category/phones){ .md-button .md-button--primary }

Элементы безопасности, такие как Titan M2, более ограничены, чем процессорная Trusted Execution Environment, используемая в большинстве других телефонов, поскольку они используются только для хранения секретов, аппаратной аттестации и ограничения скорости, а не для запуска "доверенных" программ. Телефоны без защищенного элемента вынуждены использовать TEE для *всех* этих функций, что приводит к увеличению поверхности атаки.

Google Pixel phones use a TEE OS called Trusty which is [open source](https://source.android.com/security/trusty#whyTrusty), unlike many other phones.

Установить GrapheneOS на телефон Pixel легко с помощью [веб-установщика](https://grapheneos.org/install/web). Если вам неудобно делать это самостоятельно и вы готовы потратить немного больше денег, обратите внимание на [NitroPhone](https://shop.nitrokey.com/shop), поскольку они поставляются с предустановленной GrapheneOS от авторитетной компании [Nitrokey](https://www.nitrokey.com/about).

Еще несколько советов по покупке Google Pixel:

- Если вы хотите купить устройство Pixel по выгодной цене, мы советуем приобрести модель "**a**" сразу после выхода следующего флагмана. Скидки обычно предоставляются потому, что Google пытается очистить свои запасы.
- Рассмотрите варианты снижения цены и специальные предложения, предлагаемые в физических магазинах.
- Просмотрите сайты общественных онлайн-сделок в вашей стране. Они могут предупредить вас о хороших распродажах.
- Google предоставляет список с указанием [цикла поддержки](https://support.google.com/nexus/answer/4457705?hl=ru&sjid=8188849062388690554-EU#zippy=) для каждого из своих устройств. Стоимость одного дня использования устройства может быть рассчитана как: $\text{Цена} \over \text {Дата окончания поддержки}-\text{Текущая дата}$, что означает, что чем дольше используется устройство, тем ниже стоимость одного дня.

## Основные приложения

Мы рекомендуем широкий спектр приложений для Android на этом сайте. Приложения, перечисленные здесь, предназначены исключительно для Android и специально улучшают или заменяют ключевые функции системы.

### Shelter

!!! recommendation

    ![Логотип Shelter](assets/img/android/shelter.svg){ align=right }
    
    **Shelter** - это приложение, которое поможет вам использовать функциональность рабочего профиля Android для изоляции или дублирования приложений на вашем устройстве.
    
    Shelter поддерживает блокировку поиска контактов между профилями и обмен файлами между профилями через файловый менеджер по умолчанию ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).
    
    [:octicons-repo-16: Репозиторий](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
    [:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://www.patreon.com/PeterCxy){ .card-link title=Поддержать }

!!! warning "Осторожно"

    Shelter рекомендуется вместо [Insular](https://secure-system.gitlab.io/Insular/) и [Island](https://github.com/oasisfeng/island), так как поддерживает [блокировку поиска контактов](https://secure-system.gitlab.io/Insular/faq.html).
    
    Используя Shelter, вы полностью доверяете его разработчику, поскольку Shelter действует как [администратор устройства](https://developer.android.com/guide/topics/admin/device-admin) для создания рабочего профиля и имеет широкий доступ к данным, хранящимся в рабочем профиле.

### Auditor

!!! recommendation

    ![Логотип Auditor](assets/img/android/auditor.svg#only-light){ align=right }
    ![Логотип Auditor](assets/img/android/auditor-dark.svg#only-dark){ align=right }
    
    **Auditor** - это приложение, использующее функции аппаратной безопасности для обеспечения контроля целостности устройства путем активного подтверждения личности устройства и целостности его операционной системы. В настоящее время оно работает только с GrapheneOS или стоковой операционной системой для [поддерживаемых устройств](https://attestation.app/about#device-support).
    
    [:octicons-home-16: Домашняя страница](https://attestation.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://attestation.app/about){ .card-link title=Документация}
    [:octicons-code-16:](https://attestation.app/source){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://attestation.app/donate){ .card-link title=Поддержать }
    
    ??? downloads "Скачать"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

Auditor осуществляет аттестацию и обнаружение вторжений путем:

- Использования модели [Trust On First Use (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) между *аудитором* и *аудируемым*, пара устанавливает приватныйключ в [аппаратное хранилище ключей](https://source.android.com/security/keystore/) *Auditor*.
- *Аудитором* может быть либо другой экземпляр приложения Auditor, либо [Remote Attestation Service](https://attestation.app).
- *Аудитор* записывает текущее состояние и конфигурацию *аудируемого* девайса.
- Если операционная система *аудируемого* девайса изменяется после завершения сопряжения, аудитор заметит изменения в состоянии и конфигурации устройства.
- Вы получите уведомление об изменении.

В службу аттестации не передается информация, позволяющая установить личность. Мы рекомендуем вам зарегистрироваться с анонимной учетной записью и включить удаленную аттестацию для постоянного мониторинга.

Если ваша [модель угроз](basics/threat-modeling.md) требует конфиденциальности, вы можете рассмотреть возможность использования [Orbot](tor.md#orbot) или VPN, чтобы скрыть свой IP-адрес от службы аттестации. Чтобы убедиться в подлинности оборудования и операционной системы, [проведите локальную аттестацию](https://grapheneos.org/install/web#verifying-installation) сразу после настройки устройства и до подключения к Интернету.

### Secure Camera

!!! recommendation

    ![Логотип Secure camera](assets/img/android/secure_camera.svg#only-light){ align=right }
    ![Логотип Secure camera](assets/img/android/secure_camera-dark.svg#only-dark){ align=right }
    
    **Secure Camera** - это приложение камеры, ориентированное на конфиденциальность и безопасность, которое может снимать изображения, видео и сканировать QR-коды. Расширения производителя CameraX (Портрет, HDR, Ночное зрение, Ретушь лица и Авто) также поддерживаются на доступных устройствах.
    
    [:octicons-repo-16: Репозиторий](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
    [:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Поддержать }
    
    ??? downloads "Скачать"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

Основные функции конфиденциальности:

- Автоматическое удаление метаданных [Exif](https://en.wikipedia.org/wiki/Exif) (включено по умолчанию)
- Использование нового API [Media](https://developer.android.com/training/data-storage/shared/media), поэтому разрешения [на память](https://developer.android.com/training/data-storage) не требуются
- Разрешение на микрофон не требуется, если вы не хотите записывать звук

!!! note "Примечание"

    В настоящее время метаданные не удаляются из видео, но эта функция запланирована.
    
    Метаданные об ориентации изображения не удаляются. Если вы включите функцию определения местоположения (в Secure Camera), эта запись также **не будет** удалена. Если вы хотите удалить его позже, вам нужно будет использовать стороннее приложение, такое как [ExifEraser](data-redaction.md#exiferaser).

### Secure PDF Viewer

!!! recommendation

    ![Логотип Secure PDF Viewer](assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
    ![Логотип Secure PDF Viewer](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }
    
    **Secure PDF Viewer** - это программа просмотра PDF, основанная на [pdf.js](https://en.wikipedia.org/wiki/PDF.js), которая не требует никаких разрешений. PDF открывается в [песочнице](https://en.wikipedia.org/wiki/Sandbox_(software_development)) [webview](https://developer.android.com/guide/webapps/webview). Это означает, что для доступа к содержимому или файлам не требуется прямого разрешения.
    
    [Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) используется для обеспечения того, чтобы JavaScript и свойства стиля в WebView были полностью статическим содержимым.
    
    [:octicons-repo-16: Репозиторий](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
    [:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Поддержать }
    
    ??? downloads "Скачать"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

## Скачивание приложений

### Obtainium

!!! recommendation

    ![Obtainium logo](assets/img/android/obtainium.svg){ align=right }
    
    **Obtainium** is an app manager which allows you to install and update apps directly from the developer's own releases page (i.e. GitHub, GitLab, the developer's website, etc.), rather than a centralized app store/repository. It supports automatic background updates on Android 12 and higher.
    
    [:octicons-repo-16: Repository](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
    [:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

Obtainium allows you to download APK installer files from a wide variety of sources, and it is up to you to ensure those sources and apps are legitimate. For example, using Obtainium to install Signal from [Signal's APK landing page](https://signal.org/android/apk/) should be fine, but installing from third-party APK repositories like Aptoide or APKPure may pose additional risks.

Obtainium can also be used to download apps from F-Droid repositories, and may serve as a useful alternative to the official F-Droid clients. However, we generally recommend against apps built by F-Droid or from unofficial F-Droid repositories: Read [our notes on F-Droid](#f-droid) below for more information.

### GrapheneOS App Store

Магазин приложений GrapheneOS доступен на [GitHub](https://github.com/GrapheneOS/Apps/releases). Он поддерживается на Android 12 и выше и способен самостоятельно обновляться. В магазине приложений есть отдельные приложения, созданные в рамках проекта GrapheneOS, такие, как [Auditor](https://attestation.app/), [Camera](https://github.com/GrapheneOS/Camera), и [PDF Viewer](https://github.com/GrapheneOS/PdfViewer). Если вы ищете эти приложения, мы настоятельно рекомендуем вам приобрести их в магазине приложений GrapheneOS, а не в Play Store, так как приложения в их магазине подписаны собственной подписью проекта GrapheneOS, к которой Google не имеет доступа.

### Aurora Store

Для входа в Google Play Store требуется учетная запись Google, что не лучшим образом сказывается на конфиденциальности. Это можно обойти, используя альтернативный клиент, например, Aurora Store.

!!! recommendation

    ![Логотип Aurora Store](assets/img/android/aurora-store.webp){ align=right }
    
    **Aurora Store** - это клиент Google Play Store, которому для загрузки приложений не требуется учетная запись Google, службы Google Play Services или microG.
    
    [:octicons-home-16: Домашняя страница](https://auroraoss.com/){ .md-button .md-button--primary }
    [:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Исходный код" }
    
    ??? downloads "Скачать"
    
        - [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

Aurora Store не позволяет загружать платные приложения через анонимный аккаунт. Для загрузки купленных вами раннее приложений в Aurora Store можно, по желанию, залогиниться с учетной записью Google, что дает доступ к списку установленных приложений в Google, однако вы все равно получаете преимущество, поскольку вам не требуется полный клиент Google Play и службы Google Play Services или microG на вашем устройстве.

### Вручную с помощью уведомлений RSS

Для приложений, которые выпускаются на таких платформах, как GitHub и GitLab, вы можете добавить RSS-ленту в свой [агрегатор новостей](/news-aggregators), которая поможет вам отслеживать новые релизы.

![RSS APK](./assets/img/android/rss-apk-light.png#only-light) ![RSS APK](./assets/img/android/rss-apk-dark.png#only-dark) ![Изменения APK](./assets/img/android/rss-changes-light.png#only-light) ![Изменения APK](./assets/img/android/rss-changes-dark.png#only-dark)

#### GitHub

На GitHub (используем в качестве примера [Secure Camera](#secure-camera)) нужно перейти на [страницу релизов](https://github.com/GrapheneOS/Camera/releases) и добавить `.atom` к URL:

`https://github.com/GrapheneOS/Camera/releases.atom`

#### GitLab

На GitLab (используем в качестве примера [Aurora Store](#aurora-store)) нужно открыть [репозиторий проекта](https://gitlab.com/AuroraOSS/AuroraStore) и добавить `/-/tags?format=atom` к URL:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

#### Проверка цифровых отпечатков APK

Если вы загружаете APK-файлы для установки вручную, вы можете проверить их подпись с помощью утилиты [`apksigner`](https://developer.android.com/studio/command-line/apksigner), которая является частью Android [build-tools](https://developer.android.com/studio/releases/build-tools).

1. Установите [Java JDK](https://www.oracle.com/java/technologies/downloads/).

2. Скачайте [Android Studio command line tools](https://developer.android.com/studio#command-tools).

3. Разархивируйте скачанный архив:

    ```bash
    unzip commandlinetools-*.zip
    cd cmdline-tools
    ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
    ```

4. Запустите команду проверки подписи:

    ```bash
    ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
    ```

5. Затем полученные хэши можно сравнить с другим источником. Некоторые разработчики, такие как Signal, [показывают хэши](https://signal.org/android/apk/) на своем сайте.

    ```bash
    Signer #1 certificate DN: CN=GrapheneOS
    Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
    Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
    Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
    ```

### F-Droid

![Логотип F-Droid](assets/img/android/f-droid.svg){ align=right width=120px }

==В настоящее время мы **не** рекомендуем F-Droid в качестве способа получения приложений.== F-Droid часто рекомендуется в качестве альтернативы Google Play, особенно в сообществе, занимающемся вопросами конфиденциальности. Возможность добавлять сторонние репозитории и не ограничиваться рамками Google стала причиной его популярности. F-Droid дополнительно имеет [воспроизводимые сборки](https://f-droid.org/en/docs/Reproducible_Builds/) для некоторых приложений и является приверженцем свободного программного обеспечения с открытым исходным кодом. Однако есть [заметные проблемы](https://privsec.dev/posts/android/f-droid-security-issues/) с официальным клиентом F-Droid, их контролем качества и тем, как они создают, подписывают и доставляют пакеты.

Из-за их процесса сборки приложений, приложения в официальном репозитории F-Droid часто не получают обновлений. Владельцы F-Droid повторно используют идентификаторы пакетов при подписании приложений собственными ключами, что не является идеальным, поскольку это дает команде F-Droid абсолютное доверие.

Другие популярные сторонние репозитории, такие как [IzzyOnDroid](https://apt.izzysoft.de/fdroid/), решают некоторые из этих проблем. Репозиторий IzzyOnDroid берет сборки непосредственно с GitHub и является аналогом собственных репозиториев разработчиков. Однако мы не рекомендуем этого делать, поскольку приложения обычно [удаляются](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446) из этого репозитория, когда они попадают в основной репозиторий F-Droid. Хотя в этом есть смысл (поскольку цель этого конкретного репозитория - размещение приложений до того, как они будут приняты в основной репозиторий F-Droid), это может оставить вас с установленными приложениями, которые больше не получают обновлений.

Тем не менее, репозитории [F-Droid](https://f-droid.org/en/packages/) и [IzzyOnDroid](https://apt.izzysoft.de/fdroid/) являются домом для бесчисленных приложений, поэтому они могут быть полезным инструментом для поиска и обнаружения приложений с открытым исходным кодом, которые затем можно загрузить через Play Store, Aurora Store или получить APK непосредственно от разработчика. Важно помнить, что некоторые приложения в этих репозиториях не обновлялись годами и могут опираться на неподдерживаемые библиотеки, что, помимо прочего, представляет потенциальную угрозу безопасности. При поиске новых приложений с помощью этого метода следует руководствоваться своими соображениями.

!!! note "Примечание"

    В некоторых редких случаях разработчик приложения будет распространять его только через F-Droid ([Gadgetbridge](https://gadgetbridge.org/) - один из примеров этого). Если вам действительно нужно такое приложение, мы рекомендуем использовать [Neo Store](https://github.com/NeoApplications/Neo-Store/) вместо официального приложения F-Droid для его получения.

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

!!! example "Это новый раздел"

    Мы всё еще работаем над установлением критериев для каждого раздела нашего сайта, поэтому они могут поменяться в будущем. Если у вас есть вопросы по поводу наших критериев, пожалуйста, [задавайте их на нашем форуме](https://discuss.privacyguides.net/latest). Если какой-то критерий здесь не указан, это не значит, что мы его не учли. Перед тем, как рекомендовать какой-либо проект мы учитываем и обсуждаем множество факторов. Документирование этих факторов ещё не завершено.

### Операционные системы

- Должны иметь открытый исходный код.
- Должны поддерживать блокировку загрузчика с поддержкой кастомного ключа AVB.
- Должны получать основные обновления Android в течение 1 месяца после релиза.
- Должны получать обновления функций Android (минорные версии) в течение 14 дней после релиза.
- Должен регулярно получать патчи безопасности в течение 5 дней после релиза.
- По умолчанию root-доступ должен **выключен**.
- По умолчанию Google Play Services должны быть **выключены**.
- **Не** должны требоваться модификации системы для поддержки Google Play Services.

### Девайсы

- Должны поддерживать хотя бы одну из рекомендованных нами кастомных операционных систем.
- Должны продаваться новыми в магазинах.
- Должны получать обновления безопасности минимум 5 лет.
- Должен быть отдельный аппаратный элемент безопасности.

### Приложения

- Приложения на этой странице не должны относиться к какой-либо другой категории программного обеспечения на сайте.
- В целом приложения должны расширять или заменять основную функциональность системы.
- Приложения должны регулярно обновляться и поддерживаться.
