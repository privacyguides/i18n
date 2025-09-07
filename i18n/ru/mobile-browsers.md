---
meta_title: "Браузеры для Android и iOS, соблюдающие конфиденциальность - Privacy Guides"
title: Мобильные браузеры
icon: material/cellphone-information
description: Мы рекомендуем эти браузеры для обычного/неанонимного браузинга в интернете на вашем телефоне.
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Рекомендации приватных браузеров для телефонов
    url: "./"
    relatedLink: "../desktop-browsers/"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    applicationCategory: Web Browser
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Cromite
    image: /assets/img/browsers/cromite.svg
    url: https://cromite.org
    applicationCategory: Web Browser
    operatingSystem:
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://apple.com/safari
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Защищает от следующих угроз:</small>

- [:material-account-cash: Капитализм слежки](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Это наши рекомендуемые в настоящее время **мобильные браузеры** и конфигурации для стандартного/неанонимного просмотра интернета. Если вам нужна анонимность в сети, используйте [Tor](tor.md).

## Brave

<div class="admonition recommendation" markdown>

![Логотип Brave](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** содержит встроенный блокировщик рекламы и [функции конфиденциальности](https://brave.com/privacy-features), многие из которых уже включены по умолчанию.

Brave основан на Chromium, поэтому он покажется тебе знакомым, а также у него не должно быть проблем совместимости с сайтами.

[:octicons-home-16: Домашняя страница](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Сервис Onion" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Документация" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Исходный код" }

<details class="downloads" markdown>
<summary>Скачать</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-fdroid: F-Droid](https://brave-browser-apk-release.s3.brave.com/fdroid/repo/index.html)

</details>

</div>

### Рекомендуемые настройки Brave

Tor Browser — это единственный способ действительно анонимно пользоваться интернетом. Если ты используешь Brave, мы рекомендуем изменить следующие настройки, чтобы сохранить приватность, но все браузеры кроме [Tor](tor.md#tor-browser) могут *кем-нибудь* отслеживаться в том или ином виде.

=== "Android"

    Эти параметры можно найти в :material-menu: → **Настройки** → **Защита Brave и конфиденциальность**.

=== "iOS"

    Эти параметры можно найти в :fontawesome-solid-ellipsis: → **Все настройки** → **Brave Shields & Конфиденциальность**.

#### Общие настройки Brave Shields по умолчанию

Brave включает некоторые меры против снятия цифровых отпечатков в своей функции [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Мы предлагаем настроить эти параметры [глобально](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) для всех страниц, которые вы посещаете.

Опции щитов можно понижать по мере необходимости для каждого конкретного сайта, но по умолчанию мы рекомендуем установить следующие параметры:

=== "Android"

    <div class="annotate" markdown>

    - [x] Выбери **Блокировать трекеры и рекламу (строгий режим)** в *Блокировать трекеры и рекламу*
    - [x] Включи **Автоматически перенаправлять с AMP-страниц**
    - [x] Включи **Автоматически перенаправлять URL-адреса отслеживания**
    - [x] Выбери **Требовать использование HTTPS для всех соединений (обязательно)** в *Переключаться на HTTPS*
    - \[x\] (Опционально) Включи **Блокировать скрипты** (1)
    - [x] Выбери **Блокировать сторонние файлы cookie** в *Блокировать cookie*
    - [x] Включи **Блокировать определение отпечатков**
    - [x] Включи **Защититесь от утечки информации о языковых настройках**

    <details class="warning" markdown>
    <summary>Использование списков фильтров по умолчанию</summary>

    Brave позволяет тебе выбирать дополнительные фильтры контента в меню **Фильтры контента** или на внутренней странице `brave://adblock`. Мы не рекомендуем использовать эту функцию; вместо этого оставь списки фильтров по умолчанию. Использование дополнительных фильтров выделит тебя среди других пользователей Brave, а также может увеличить площадь атаки, если в Brave есть эксплойт и вредоносное правило будет добавлено в один из используемых тобой списков.

    </details>

    - [x] Выбери**Удалять данные о посещении этого сайта**

    </div>

    1. Эта опция отключает JavaScript, что приведет к неработоспособности многих сайтов. Чтобы исправить это, ты можешь установить исключения для отдельных сайтов, нажав на значок Щита в адресной строке и сняв флажок с этой настройки в разделе *Расширенное управление*.

=== "iOS"

    <div class="annotate" markdown>

    - [x] Выбери **Агрессивный** в *Трекеры & Блокировка рекламы*
    - [x] Выбери **Строгое соответствие* в *Переведите подключения на HTTPS*</li>
    - [x] Выбери **Автоматически обходить AMP-страницы**
    - [x] Выбери **Автоматически перенаправлять URL-адреса отслеживания**
    - \[x\] (Опционально) Включи **Блокировать скрипты** (1)
    - [x] Включи **Блокировать идентификацию**
    - [x] Включи **При закрытии вкладок** в *Автоуничтожение данных*

    <details class="warning" markdown>
    <summary>Использование списков фильтров по умолчанию</summary>

    Brave позволяет тебе выбирать дополнительные фильтры контента в меню **Фильтры контента**. Мы не рекомендуем использовать эту функцию; вместо этого оставь списки фильтров по умолчанию. Использование дополнительных фильтров выделит тебя среди других пользователей Brave, а также может увеличить площадь атаки, если в Brave есть эксплойт и вредоносное правило будет добавлено в один из используемых тобой списков.

    </details>

    </div></ul>

    1. Эта опция отключает JavaScript, что приведет к неработоспособности многих сайтов. Чтобы исправить это, ты можешь установить исключения для отдельных сайтов, нажав на значок Щита в адресной строке и сняв флажок с этой настройки в разделе *Расширенное управление*.

##### Очистить историю (только для Android)

- [x] Выбери **Удалять данные при выходе**

##### Блокировка соцсетей (только для Android)

- [ ] Отключи все переключатели в этой секции

#### Другие настройки конфиденциальности

=== "Android"

    <div class="annotate" markdown>

    - [x] Выбери **Отключить непроксируемый протокол UDP** в [*Политика обработки IP WebRTC*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
    - \[x\] (Опционально) Выбери **Защита отключена** в *Безопасный просмотр* (1)
    - [ ] Отключи **Разрешить сайтам проверять наличие сохраненных способов оплаты**
    - [ ] Отключи **Оптимизация и безопасность JavaScript**  под одноимённой настройкой
    - [x] Включи **Закрывать вкладки при выходе**
    - Отключи **Разрешить  выполнение аналитики продукта, не нарушающей конфиденциальности**
    - Отключи **Автоматически отправлять данные диагностики**
    - Отключи **Автоматически отправлять ежедневные данные PING в Brave**

    </div>

    1. [Реализация Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) в Brave на Android **не использует** прокси для [сетевых запросов Safe Browsing](https://developers.google.com/safe-browsing/v4/update-api#checking-urls), как это делает настольная версия. Это означает, что твой IP-адрес может быть виден (и записан) Google. Обрати внимание, что Safe Browsing недоступен для устройств Android без Google Play Services.

=== "iOS"

    - [ ] Отключи **Разрешить выполнение аналитики продукта без нарушения конфиденциальности**
    - [ ] Отключи **Автоматически отправлять ежедневные данные PING в Brave**

#### Leo

Эти параметры можно найти в :material-menu: → **Настройки** → **Leo**.

<div class="annotate" markdown>

[ ] Выключи **Показывать предложения для автозаполнения в адресной строке** (1)

</div>

1. Эта опция отсутствует в приложении Brave для iOS.

#### Поисковые системы

Эти параметры можно найти в :material-menu:/:fontawesome-solid-ellipsis: → **Настройки** → **Поисковые системы**.

- [ ] Отключи **Показывать подсказки при поиске**

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) позволяет твоим данным просмотра (истории, закладкам и т.д.) быть доступными на всех твоих устройствах без необходимости создания учетной записи и защищает их сквозным шифрованием (E2EE).

## Cromite (Android)

<div class="admonition recommendation" markdown>

![Логотип Cromite](assets/img/browsers/cromite.svg){ align=right }

**Cromite** — это браузер на основе Chromium со встроенной блокировкой рекламы, защитой от снятия отпечатка браузера и другими [улучшениями конфиденциальности и безопасности](https://github.com/uazo/cromite/blob/master/docs/FEATURES.md). Это форк браузера **Bromite**, разработка которого была прекращена.

[:octicons-home-16: Домашняя страница](https://cromite.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uazo/cromite/blob/master/docs/PRIVACY_POLICY.md){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://github.com/uazo/cromite?tab=readme-ov-file#docs){ .card-link title="Документация" }
[:octicons-code-16:](https://github.com/uazo/cromite){ .card-link title="Исходный код" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: F-Droid](https://cromite.org/fdroid/repo/?fingerprint=49F37E74DEE483DCA2B991334FB5A0200787430D0B5F9A783DD5F13695E9517B)
- [:simple-github: GitHub](https://github.com/uazo/cromite/releases/latest)

</details>

</div>

### Рекомендованные настройки

Эти параметры можно найти в :material-menu: → :gear: **Настройки** → **Конфиденциальность и безопасность**.

#### Данные просмотра

- [x] Включи **Close all open tabs on exit**

#### Режим Инкогнито

- [x] Включи **Open external links in incognito**

#### Безопасность

- [x] Включи **Всегда использовать безопасные соединения**

Это предотвращает непреднамеренное подключение к веб-сайту по открытому протоколу HTTP. HTTP сегодня встречается крайне редко, поэтому это должно оказывать минимальное влияние или не оказывать никакого влияния на твой повседневный просмотр веб-страниц.

#### Настройки Adblock Plus

Эти параметры можно найти в :material-menu: → :gear: **Настройки** → **Adblock Plus settings**.

Cromite содержит настроенную версию Adblock Plus с включенным по умолчанию списком EasyList, а также опции для выбора дополнительных списков фильтров в меню **Filter lists** (Списки фильтров).

Использование дополнительных списков будет выделять тебя среди других пользователей Cromite и может также увеличить поверхность атаки, если вредоносное правило будет добавлено в один из списков, которые ты используешь.

- \[x\] (Опционально) Включи **Enable anti-circumvention and snippets**

Этот параметр добавляет дополнительный список Adblock Plus, который может повысить эффективность блокировки контента в Cromite. Предупреждения о выделении среди других пользователей и потенциальном увеличении поверхности атаки применимы.

#### Legacy Adblock settings

Эти параметры можно найти в :material-menu: → :gear: **Настройки** → **Legacy Adblock settings**.

- [ ] Отключи настройку автоматического обновления

Это отключает проверку обновлений для неподдерживаемого фильтра Bromite adblock.

## Safari (iOS)

На iOS любое приложение, которое может просматривать веб, [ограничено](https://developer.apple.com/app-store/review/guidelines) использованием предоставленного Apple[фреймворка WebKit](https://developer.apple.com/documentation/webkit), поэтому браузер вроде [Brave](#brave) не использует движок Blink (основной компонент Chromium), как его аналоги на других операционных системах.

<div class="admonition recommendation" markdown>

![Логотип Safari](assets/img/browsers/safari.svg){ align=right }

**Safari** — браузер по умолчанию на iOS. Он включает [функции конфиденциальности](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios), такие как [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), изолированные и временные вкладки приватного просмотра, защиту от фингерпринтинга (путем представления упрощенной версии конфигурации системы веб-сайтам, чтобы больше устройств выглядели идентично), и рандомизацию цифровых отпечатков, а также Private Relay для тех, у кого есть платная подписка iCloud+.

[:octicons-home-16: Домашняя страница](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title="Документация" }

</details>

</div>

### Рекомендуемые настройки Safari

Мы рекомендуем установить [AdGuard](browser-extensions.md#adguard), если ты хочешь использовать блокировщик контента в Safari.

The following privacy/security-related options can be found in :gear: **Settings** → **Apps** → **Safari**.

#### Allow Safari to Access

Under **Siri**:

- [ ] Disable **Learn from this App**
- [ ] Disable **Show in App**
- [ ] Disable **Show on Home Screen**
- [ ] Disable **Suggest App**

This prevents Siri from using content from Safari for Siri suggestions.

#### Поиск

- [ ] Disable **Search Engine Suggestions**

This setting sends whatever you type in the address bar to the search engine set in Safari. Отключение поисковых подсказок позволяет вам более точно контролировать, какие данные вы отправляете провайдеру поисковой системы.

#### Profiles

Safari allows you to separate your browsing with different profiles. All of your cookies, history, and website data are separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

#### Приватность и защита

- [x] Enable **Prevent Cross-Site Tracking**

This enables WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). The feature helps protect against unwanted tracking by using on-device machine learning to stop trackers. ITP protects against many common threats, but does not block all tracking avenues because it is designed to not interfere with website usability.

- [x] Enable **Require Face ID/Touch ID to Unlock Private Browsing**

This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

- [ ] Disable **Fraudulent Website Warning**

This setting uses Google Safe Browsing (or Tencent Safe Browsing for users in mainland China or Hong Kong) to protect you while you browse. As such, your IP address may be logged by your Safe Browsing provider. Disabling this setting will disable this logging, but you might be more vulnerable to known phishing sites.

- [x] Enable **Not Secure Connection Warning**

This setting shows a warning screen if your connection to a website isn't using HTTPS. Safari will automatically try to upgrade the site to HTTPS, so you should only see this when there is no HTTPS connection available.

- [ ] Disable **Highlights**

Apple's privacy policy for Safari states:

> When visiting a webpage, Safari may send information calculated from the webpage address to Apple over OHTTP to determine if relevant highlights are available.

#### Settings for Websites

Under **Camera**

- [x] Select **Ask**

Under **Microphone**

- [x] Select **Ask**

Under **Location**

- [x] Select **Ask**

These settings ensure that websites can only access your camera, microphone, or location after you explicitly grant them access.

#### Other Privacy Settings

These options can be found in :gear: **Settings** → **Apps** → **Safari** → **Advanced**.

##### Fingerprinting Mitigations

The **Advanced Tracking and Fingerprinting Protection** setting will randomize certain values so that it's more difficult to fingerprint you:

- [x] Select **All Browsing** or **Private Browsing**

##### Конфиденциальные рекламные отчеты

- [ ] Отключи **Конфиденциальные рекламные отчеты**

Для измерения количества рекламных кликов традиционно используется технология отслеживания, нарушающая конфиденциальность пользователей. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

Сама по себе эта функция не вызывает особых опасений в плане конфиденциальности, и хотя вы можете оставить ее включенной, мы рекомендуем её отключить, так как она автоматически отключается в Private Browsing.

#### Всегда включенный частный доступ

Откройте Safari и нажмите кнопку Вкладки, расположенную в правом нижнем углу. Then, expand the :material-format-list-bulleted: Tab Groups list.

- [x] Выбери **Частный доступ**

Режим Частный доступ в Safari обеспечивает дополнительную защиту конфиденциальности. Приватный просмотр использует новую [эфемерную](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) сессию для каждой вкладки, то есть вкладки изолированы друг от друга. There are other smaller privacy benefits with Private Browsing too, such as not sending a webpage’s address to Apple when using Safari's translation feature.

Do note that Private Browsing does not save cookies and website data, so it won't be possible to remain signed in to sites. Это может доставить неудобства.

#### Синхронизация iCloud

Синхронизация истории Safari, групп вкладок, вкладок iCloud и сохраненных паролей осуществляется с E2EE. However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://apple.com/legal/privacy/en-ww).

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/HT212520). Go to :gear: **Settings** → **iCloud** → **Advanced Data Protection**.

- [x] Turn on **Advanced Data Protection**

If you use iCloud with Advanced Data Protection disabled, we also recommend setting Safari's default download location to a local folder on your device. This option can be found in :gear: **Settings** → **Apps** → **Safari** → **General** → **Downloads**.

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Мы рекомендуем тебе ознакомиться с этим списком, прежде чем выбрать продукт, и провести собственное исследование, чтобы убедиться в правильности своего выбора.

### Минимальные требования к сервисам

- Должен поддерживать автоматические обновления.
- Must receive engine updates from upstream releases quickly.
- Must support content blocking.
- Любые изменения, необходимые для того, чтобы браузер больше соблюдал конфиденциальность, не должны негативно влиять на опыт использования.
