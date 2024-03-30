---
meta_title: "Android Recommendations: GrapheneOS and DivestOS - Privacy Guides"
title: "Android"
icon: 'simple/android'
description: You can replace the operating system on your Android phone with these secure and privacy-respecting alternatives.
cover: android.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Private Android Operating Systems
    url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: Android
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://en.wikipedia.org/wiki/Android_(operating_system)
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
    sameAs: https://en.wikipedia.org/wiki/Google_Pixel
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

[:octicons-home-16:](https://source.android.com){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject){ .card-link title="Source Code" }

Это операционные системы, устройства и приложения для Android, которые мы рекомендуем для обеспечения максимальной безопасности и конфиденциальности вашего мобильного устройства. Чтобы узнать больше об Android:

[Общий обзор Android :material-arrow-right-drop-circle:](os/android-overview.md ""){.md-button}

## Основанные на AOSP

Мы рекомендуем установить на ваше устройство одну из этих кастомных операционных систем Android, перечисленных в порядке предпочтения, в зависимости от совместимости вашего устройства с этими операционными системами.

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Устройства с истекшим сроком службы (например устройства с GrapheneOS или с "расширенной поддержкой" CalyxOS) не имеют полных исправлений безопасности (обновлений прошивки) из-за прекращения поддержки OEM-производителем. Эти устройства нельзя считать полностью безопасными, независимо от установленного программного обеспечения.

</div>

### GrapheneOS

<div class="admonition recommendation" markdown>

![Логотип GrapheneOS](assets/img/android/grapheneos.svg#only-light){ align=right }
![Логотип GrapheneOS](assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** - это лучший выбор для вашей безопасности и конфиденциальности.

GrapheneOS обеспечивает дополнительное [улучшение безопасности](https://en.wikipedia.org/wiki/Hardening_(computing)) и улучшение конфиденциальности. Она имеет [улучшенный memory allocator] (https://github.com/GrapheneOS/hardened_malloc), сетевые и сенсорные разрешения и другие различные [функции безопасности] (https://grapheneos.org/features). GrapheneOS также поставляется с полными обновлениями прошивки и подписанными сборками, поэтому проверенная загрузка полностью поддерживается.

[:octicons-home-16: Homepage](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

</div>

GrapheneOS поддерживает [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), который запускает [Google Play Services](https://en.wikipedia.org/wiki/Google_Play_Services) полностью в песочнице, как любое другое обычное приложение. This means you can take advantage of most Google Play Services, such as [push notifications](https://firebase.google.com/docs/cloud-messaging), while giving you full control over their permissions and access, and while containing them to a specific [work profile](os/android-overview.md#work-profile) or [user profile](os/android-overview.md#user-profiles) of your choice.

Телефоны Google Pixel - единственные устройства, которые в настоящее время отвечают [требованиям аппаратной безопасности](https://grapheneos.org/faq#device-support) GrapheneOS.

[Почему мы рекомендуем GrapheneOS, а не CalyxOS :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos ""){.md-button}

### DivestOS

<div class="admonition recommendation" markdown>

![DivestOS logo](assets/img/android/divestos.svg){ align=right }

**DivestOS** is a soft-fork of [LineageOS](https://lineageos.org).
DivestOS inherits many [supported devices](https://divestos.org/index.php?page=devices&base=LineageOS) from LineageOS. Он имеет подписанные сборки, что делает возможным [verified boot](https://source.android.com/security/verifiedboot) на некоторых не-Pixel устройствах.

[:octicons-home-16: Домашняя страница](https://divestos.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Сервис Onion" }
[:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=Документация}
[:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="Исходный код" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Поддержать }

</div>

DivestOS имеет автоматизированное ([CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [исправление](https://gitlab.com/divested-mobile/cve_checker) уязвимостей ядра, меньше проприетарных зависимостей и кастомный [hosts](https://divested.dev/index.php?page=dnsbl) файл. Its hardened WebView, [Mulch](https://gitlab.com/divested-mobile/mulch), enables [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) for all architectures and [network state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning), and receives out-of-band updates. DivestOS также включает патчи ядра от GrapheneOS и включает все доступные функции безопасности ядра с помощью [defconfig hardening](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). All kernels newer than version 3.4 include full page [sanitization](https://lwn.net/Articles/334747) and all ~22 Clang-compiled kernels have [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) enabled.

В DivestOS реализованы некоторые патчи для защиты системы, изначально разработанные для GrapheneOS. В DivestOS 16.0 и выше реализованы переключатели из GrapheneOS для [`интернета`](https://developer.android.com/training/basics/network-ops/connecting) и сенсоров, [улучшенный memory allocator](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/#additional-hardening), [JNI](https://en.wikipedia.org/wiki/Java_Native_Interface) [constification](https://en.wikipedia.org/wiki/Const_(computer_programming)), и частичные патчи [bionic](https://en.wikipedia.org/wiki/Bionic_(software)). 17.1 and higher features GrapheneOS's per-network full [MAC randomization](https://en.wikipedia.org/wiki/MAC_address#Randomization) option, [`ptrace_scope`](https://kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) control, and automatic reboot/Wi-Fi/Bluetooth [timeout options](https://grapheneos.org/features).

DivestOS использует F-Droid в качестве магазина приложений по умолчанию. We normally [recommend avoiding F-Droid](#f-droid), but doing so on DivestOS isn't viable; the developers update their apps via their own F-Droid repositories ([DivestOS Official](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) and [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2)). We recommend disabling the official F-Droid app and using [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) **with the DivestOS repositories enabled** to keep those components up to date. Для других приложений по-прежнему действуют рекомендованные нами способы их получения.

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

[Статус](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) обновлений прошивки DivestOS и контроль качества варьируются в зависимости от поддерживаемых устройств. Мы по-прежнему рекомендуем GrapheneOS, если ваш телефон её поддерживает. Для других устройств хорошей альтернативой является DivestOS.

Не все поддерживаемые устройства имеют функцию проверенной загрузки, а некоторые выполняют ее лучше, чем другие.

</div>

## Android-устройства

При покупке устройства рекомендуем приобрести как можно более новое. ПО и прошивка мобильных устройств поддерживаются только в течение ограниченного периода времени, поэтому покупка нового устройства продлевает его жизненный цикл настолько, насколько это возможно.

Избегайте покупки телефонов у операторов мобильной связи. У них часто **заблокирован загрузчик** и они не поддерживают [OEM разблокировку](https://source.android.com/devices/bootloader/locking_unlocking). Эти варианты телефонов не позволят вам установить какой-либо альтернативный дистрибутив Android.

Будьте **очень осторожны** при покупке подержанных телефонов в интернет-магазинах. Всегда проверяйте репутацию продавца. If the device is stolen, there's a possibility of it being entered in the [IMEI database](https://gsma.com/get-involved/working-groups/terminal-steering-group/imei-database). Также существует риск связывания вас с действиями предыдущего владельца устройства.

Еще несколько советов относительно устройств Android и совместимости с операционной системой:

- Не покупайте устройства, срок службы которых истек или близок к концу, дополнительные обновления прошивки должны быть предоставлены производителем.
- Не покупайте телефоны с предустановленной LineageOS или /e/ OS или любые телефоны Android без надлежащей поддержки [проверенной загрузки (Verified Boot)](https://source.android.com/security/verifiedboot?hl=ru) и обновлений прошивки. Вы также не сможете проверить, взломаны ли эти устройства.
- Короче, если устройство или дистрибутив Android не указаны в этом списке, вероятно, на это есть веская причина. Check out our [forum](https://discuss.privacyguides.net) to find details!

### Google Pixel

Телефоны Google Pixel - это **единственные** устройства, которые мы рекомендуем к покупке. Телефоны Pixel имеют более высокий уровень аппаратной безопасности, чем любые другие устройства Android, представленные в настоящее время на рынке, благодаря надлежащей поддержке AVB для сторонних операционных систем и кастомным чипам безопасности Google [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html), выступающим в качестве элемента безопасности.

<div class="admonition recommendation" markdown>

![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }

Устройства **Google Pixel** известны хорошей безопасностью и правильной поддержкой [Verified Boot](https://source.android.com/security/verifiedboot), даже при установке сторонних операционных систем.

Beginning with the **Pixel 8** and **8 Pro**, Pixel devices receive a minimum of 7 years of guaranteed security updates, ensuring a much longer lifespan compared to the 2-5 years competing OEMs typically offer.

[:material-shopping: Магазин](https://store.google.com/category/phones){ .md-button .md-button--primary }

</div>

Элементы безопасности, такие как Titan M2, более ограничены, чем процессорная Trusted Execution Environment, используемая в большинстве других телефонов, поскольку они используются только для хранения секретов, аппаратной аттестации и ограничения скорости, а не для запуска "доверенных" программ. Телефоны без защищенного элемента вынуждены использовать TEE для *всех* этих функций, что приводит к увеличению поверхности атаки.

Google Pixel phones use a TEE OS called Trusty which is [open source](https://source.android.com/security/trusty#whyTrusty), unlike many other phones.

Установить GrapheneOS на телефон Pixel легко с помощью [веб-установщика](https://grapheneos.org/install/web). If you don't feel comfortable doing it yourself and are willing to spend a bit of extra money, check out the [NitroPhone](https://shop.nitrokey.com/shop) as they come preloaded with GrapheneOS from the reputable [Nitrokey](https://nitrokey.com/about) company.

Еще несколько советов по покупке Google Pixel:

- Если вы хотите купить устройство Pixel по выгодной цене, мы советуем приобрести модель "**a**" сразу после выхода следующего флагмана. Скидки обычно предоставляются потому, что Google пытается очистить свои запасы.
- Рассмотрите варианты снижения цены и специальные предложения, предлагаемые в физических магазинах.
- Просмотрите сайты общественных онлайн-сделок в вашей стране. Они могут предупредить вас о хороших распродажах.
- Google предоставляет список с указанием [цикла поддержки](https://support.google.com/nexus/answer/4457705?hl=ru&sjid=8188849062388690554-EU#zippy=) для каждого из своих устройств. Стоимость одного дня использования устройства может быть рассчитана как: $\text{Цена} \over \text {Дата окончания поддержки}-\text{Текущая дата}$, что означает, что чем дольше используется устройство, тем ниже стоимость одного дня.
- If the Pixel is unavailable in your region, the [NitroPhone](https://shop.nitrokey.com/shop) can be shipped globally.

## Основные приложения

Мы рекомендуем широкий спектр приложений для Android на этом сайте. Приложения, перечисленные здесь, предназначены исключительно для Android и специально улучшают или заменяют ключевые функции системы.

### Shelter

<div class="admonition recommendation" markdown>

![Логотип Shelter](assets/img/android/shelter.svg){ align=right }

**Shelter** - это приложение, которое поможет вам использовать функциональность рабочего профиля Android для изоляции или дублирования приложений на вашем устройстве.

Shelter поддерживает блокировку поиска контактов между профилями и обмен файлами между профилями через файловый менеджер по умолчанию ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).

[:octicons-repo-16: Repository](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Source Code" }
[:octicons-heart-16:](https://patreon.com/PeterCxy){ .card-link title=Contribute }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

Shelter is recommended over [Insular](https://secure-system.gitlab.io/Insular) and [Island](https://github.com/oasisfeng/island) as it supports [contact search blocking](https://secure-system.gitlab.io/Insular/faq.html).

Используя Shelter, вы полностью доверяете его разработчику, поскольку Shelter действует как [администратор устройства](https://developer.android.com/guide/topics/admin/device-admin) для создания рабочего профиля и имеет широкий доступ к данным, хранящимся в рабочем профиле.

</div>

### Secure Camera

<div class="admonition recommendation" markdown>

![Логотип Secure camera](assets/img/android/secure_camera.svg#only-light){ align=right }
![Логотип Secure camera](assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

**Secure Camera** - это приложение камеры, ориентированное на конфиденциальность и безопасность, которое может снимать изображения, видео и сканировать QR-коды. Расширения производителя CameraX (Портрет, HDR, Ночное зрение, Ретушь лица и Авто) также поддерживаются на доступных устройствах.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

Основные функции конфиденциальности:

- Автоматическое удаление метаданных [Exif](https://en.wikipedia.org/wiki/Exif) (включено по умолчанию)
- Использование нового API [Media](https://developer.android.com/training/data-storage/shared/media), поэтому разрешения [на память](https://developer.android.com/training/data-storage) не требуются
- Разрешение на микрофон не требуется, если вы не хотите записывать звук

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

В настоящее время метаданные не удаляются из видео, но эта функция запланирована.

Метаданные об ориентации изображения не удаляются. Если вы включите функцию определения местоположения (в Secure Camera), эта запись также **не будет** удалена. Если вы хотите удалить его позже, вам нужно будет использовать стороннее приложение, такое как [ExifEraser](data-redaction.md#exiferaser).

</div>

### Secure PDF Viewer

<div class="admonition recommendation" markdown>

![Логотип Secure PDF Viewer](assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Логотип Secure PDF Viewer](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

**Secure PDF Viewer** - это программа просмотра PDF, основанная на [pdf.js](https://en.wikipedia.org/wiki/PDF.js), которая не требует никаких разрешений. PDF открывается в [песочнице](https://en.wikipedia.org/wiki/Sandbox_(software_development)) [webview](https://developer.android.com/guide/webapps/webview). Это означает, что для доступа к содержимому или файлам не требуется прямого разрешения.

[Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) используется для обеспечения того, чтобы JavaScript и свойства стиля в WebView были полностью статическим содержимым.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## Скачивание приложений

### Obtainium

<div class="admonition recommendation" markdown>

![Obtainium logo](assets/img/android/obtainium.svg){ align=right }

**Obtainium** is an app manager which allows you to install and update apps directly from the developer's own releases page (i.e. GitHub, GitLab, the developer's website, etc.), rather than a centralized app store/repository. It supports automatic background updates on Android 12 and higher.

[:octicons-repo-16: Repository](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

Obtainium allows you to download APK installer files from a wide variety of sources, and it is up to you to ensure those sources and apps are legitimate. For example, using Obtainium to install Signal from [Signal's APK landing page](https://signal.org/android/apk) should be fine, but installing from third-party APK repositories like Aptoide or APKPure may pose additional risks. The risk of installing a malicious *update* is lower, because Android itself verifies that all app updates are signed by the same developer as the existing app on your phone before installing them.

### GrapheneOS App Store

Магазин приложений GrapheneOS доступен на [GitHub](https://github.com/GrapheneOS/Apps/releases). Он поддерживается на Android 12 и выше и способен самостоятельно обновляться. The app store has standalone applications built by the GrapheneOS project such as the [Auditor](https://attestation.app), [Camera](https://github.com/GrapheneOS/Camera), and [PDF Viewer](https://github.com/GrapheneOS/PdfViewer). Если вы ищете эти приложения, мы настоятельно рекомендуем вам приобрести их в магазине приложений GrapheneOS, а не в Play Store, так как приложения в их магазине подписаны собственной подписью проекта GrapheneOS, к которой Google не имеет доступа.

### Aurora Store

Для входа в Google Play Store требуется учетная запись Google, что не лучшим образом сказывается на конфиденциальности. Это можно обойти, используя альтернативный клиент, например, Aurora Store.

<div class="admonition recommendation" markdown>

![Логотип Aurora Store](assets/img/android/aurora-store.webp){ align=right }

**Aurora Store** - это клиент Google Play Store, которому для загрузки приложений не требуется учетная запись Google, службы Google Play Services или microG.

[:octicons-home-16: Homepage](https://auroraoss.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

Aurora Store не позволяет загружать платные приложения через анонимный аккаунт. Для загрузки купленных вами раннее приложений в Aurora Store можно, по желанию, залогиниться с учетной записью Google, что дает доступ к списку установленных приложений в Google, однако вы все равно получаете преимущество, поскольку вам не требуется полный клиент Google Play и службы Google Play Services или microG на вашем устройстве.

### Вручную с помощью уведомлений RSS

For apps that are released on platforms like GitHub and GitLab, you may be able to add an RSS feed to your [news aggregator](news-aggregators.md) that will help you keep track of new releases.

![RSS APK](./assets/img/android/rss-apk-light.png#only-light) ![RSS APK](./assets/img/android/rss-apk-dark.png#only-dark) ![APK Changes](./assets/img/android/rss-changes-light.png#only-light) ![APK Changes](./assets/img/android/rss-changes-dark.png#only-dark)

#### GitHub

На GitHub (используем в качестве примера [Secure Camera](#secure-camera)) нужно перейти на [страницу релизов](https://github.com/GrapheneOS/Camera/releases) и добавить `.atom` к URL:

`https://github.com/GrapheneOS/Camera/releases.atom`

#### GitLab

На GitLab (используем в качестве примера [Aurora Store](#aurora-store)) нужно открыть [репозиторий проекта](https://gitlab.com/AuroraOSS/AuroraStore) и добавить `/-/tags?format=atom` к URL:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

#### Проверка цифровых отпечатков APK

Если вы загружаете APK-файлы для установки вручную, вы можете проверить их подпись с помощью утилиты [`apksigner`](https://developer.android.com/studio/command-line/apksigner), которая является частью Android [build-tools](https://developer.android.com/studio/releases/build-tools).

1. Install [Java JDK](https://oracle.com/java/technologies/downloads).

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

5. Затем полученные хэши можно сравнить с другим источником. Some developers such as Signal [show the fingerprints](https://signal.org/android/apk) on their website.

    ```bash
    Signer #1 certificate DN: CN=GrapheneOS
    Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
    Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
    Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
    ```

### F-Droid

![Логотип F-Droid](assets/img/android/f-droid.svg){ align=right width=120px }

==We only recommend F-Droid as a way to obtain apps which cannot be obtained via the means above.== F-Droid is often recommended as an alternative to Google Play, particularly in the privacy community. Возможность добавлять сторонние репозитории и не ограничиваться рамками Google стала причиной его популярности. F-Droid additionally has [reproducible builds](https://f-droid.org/en/docs/Reproducible_Builds) for some applications and is dedicated to free and open-source software. However, there are some security-related downsides to how F-Droid builds, signs, and delivers packages:

Из-за их процесса сборки приложений, приложения в официальном репозитории F-Droid часто не получают обновлений. Владельцы F-Droid повторно используют идентификаторы пакетов при подписании приложений собственными ключами, что не является идеальным, поскольку это дает команде F-Droid абсолютное доверие. Additionally, the requirements for an app to be included in the official F-Droid repo are less strict than other app stores like Google Play, meaning that F-Droid tends to host a lot more apps which are older, unmaintained, or otherwise no longer meet [modern security standards](https://developer.android.com/google/play/requirements/target-sdk).

Other popular third-party repositories for F-Droid such as [IzzyOnDroid](https://apt.izzysoft.de/fdroid) alleviate some of these concerns. Репозиторий IzzyOnDroid берет сборки непосредственно с GitHub и является аналогом собственных репозиториев разработчиков. However, it is not something that we can fully recommend, as apps are typically [removed](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446) from that repository if they are later added to the main F-Droid repository. Хотя в этом есть смысл (поскольку цель этого конкретного репозитория - размещение приложений до того, как они будут приняты в основной репозиторий F-Droid), это может оставить вас с установленными приложениями, которые больше не получают обновлений.

That said, the [F-Droid](https://f-droid.org/en/packages) and [IzzyOnDroid](https://apt.izzysoft.de/fdroid) repositories are home to countless apps, so they can be a useful tool to search for and discover open-source apps that you can then download through other means such as the Play Store, Aurora Store, or by getting the APK directly from the developer. You should use your best judgement when looking for new apps via this method, and keep an eye on how frequently the app is updated. Outdated apps may rely on unsupported libraries, among other things, posing a potential security risk.

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

In some rare cases, the developer of an app will only distribute it through F-Droid ([Gadgetbridge](https://gadgetbridge.org) is one example of this). If you really need an app like that, we recommend using the newer [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) client instead of the original F-Droid app to obtain it. F-Droid Basic can do unattended updates without privileged extension or root, and has a reduced feature set (limiting attack surface).

</div>

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

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
