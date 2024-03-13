---
meta_title: "Мобильные браузеры для Android и iOS, соблюдающие конфиденциальность - Privacy Guides"
title: "Мобильные браузеры"
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

Здесь перечислены мобильные браузеры, которые мы рекомендуем, и руководства по их настройке для обычного/неанонимного браузинга. Если вам нужна анонимность в сети, используйте [Tor](tor.md). Мы рекомендуем использовать как можно меньше расширений, так как они имеют привилегированный доступ к браузеру, требуют доверия к их разработчикам, могут [идентифицировать тебя](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), а также [ослабляют](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) изоляцию между сайтами.

## Android

On Android, Firefox is still less secure than Chromium-based alternatives: Mozilla's engine, [GeckoView](https://mozilla.github.io/geckoview), has yet to support [site isolation](https://hacks.mozilla.org/2021/05/introducing-firefox-new-site-isolation-security-architecture) or enable [isolatedProcess](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196).

### Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave основан на Chromium, поэтому он покажется тебе знакомым, а также у него не должно быть проблем совместимости с сайтами.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

#### Рекомендованные настройки

Tor Browser — это единственный способ действительно анонимно пользоваться интернетом. Если ты используешь Brave, мы рекомендуем изменить следующие настройки, чтобы сохранить приватность, но все браузеры кроме [Tor](tor.md#tor-browser) могут *кем-нибудь* отслеживаться в том или ином виде.

Эти настройки можно найти в :material-menu: → **Настройки** → **Brave Щит и конфиденциальность**

##### Щиты

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

##### Общие настройки по умолчанию системы Brave Schields

Опции щитов можно понижать по мере необходимости для каждого конкретного сайта, но по умолчанию мы рекомендуем установить следующие параметры:

<div class="annotate" markdown>

- [x] Select **Aggressive** under **Block trackers & ads**

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. Мы не рекомендуем использовать эту функцию; вместо этого оставь списки фильтров по умолчанию. Использование дополнительных фильтров выделит тебя среди других пользователей Brave, а также может увеличить площадь атаки, если в Brave есть эксплойт и вредоносное правило будет добавлено в один из используемых тобой списков.

</details>

- [x] Выбери **Переключаться на HTTPS**
- [x] Выбери **Всегда использовать безопасные соединения**
- [x] (Опционально) Выбери **Блокировать скрипты** (1)
- [x] Выбери **Строго, может нарушать работу сайтов** в **Блокировать определение отпечатков**

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net) extension.

##### Очистить историю

- [x] Выбери **Удалять данные при выходе**

##### Блокировка соцсетей

- [ ] Отключи все переключатели в этой секции

##### Другие настройки конфиденциальности

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP handling policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Allow sites to check if you have payment methods saved**
- [ ] Uncheck **IPFS Gateway** (1)
- [x] Select **Close tabs on exit**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Automatically send daily usage ping to Brave**

</div>

1. Interplanetary File System (IPFS) - это децентрализованная, peer-to-peer сеть для хранения и обмена данными в распределенной файловой системе. Если ты не используешь эту функцию, отключи ее.

#### Синхронизация

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

## iOS

На iOS любое приложение, которое может открывать веб-страницы, [использует](https://developer.apple.com/app-store/review/guidelines) только предоставляемый Apple [движок WebKit](https://developer.apple.com/documentation/webkit), поэтому нет особых причин использовать сторонний браузер.

### Safari

<div class="admonition recommendation" markdown>

![Логотип Safari](assets/img/browsers/safari.svg){ align=right }

**Safari** — браузер по умолчанию на iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Privacy Report, isolated and ephemeral Private Browsing tabs, iCloud Private Relay, fingerprinting protection by randomizing and presenting a simplified version of the system configuration to websites so more devices look identical, and the ability to lock private tabs with your biometrics/PIN. It also allows you to separate your browsing with different profiles.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentation}

</details>

</div>

#### Рекомендованные настройки

These options can be found in :gear: **Settings** → **Safari**

##### Profiles

All of your cookies, history, and website data will be separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

##### Приватность и защита

- [x] Включи **Без перекрестного отслеживания**

    Это активирует функцию WebKit: [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). Эта функция помогает защититься от нежелательного отслеживания, используя машинное обучение на устройстве для остановки отслеживающих устройств. ITP защищает от многих распространенных угроз, но не блокирует все пути слежения, поскольку разработан таким образом, чтобы не мешать удобству использования сайта.

- [x] Enable **Require Face ID to Unlock Private Browsing**

    This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

##### Advanced → Privacy

The **Advanced Tracking and Fingerprinting Protection** setting will randomize certain values so that it's more difficult to fingerprint you:

- [x] Select **All Browsing** or **Private Browsing**

##### Отчет о конфиденциальности

«Отчет о конфиденциальности» представляет собой обзор межсайтовых трекеров, которым в настоящее время запрещено создавать ваш профиль на посещаемом вами сайте. Функция также показывает еженедельный отчет о количестве заблокированных трекеров в течение определенного времени.

Отчет о конфиденциальности доступен через меню "Настройки страницы".

##### Конфиденциальные рекламные отчеты

- [ ] Отключи **Конфиденциальные рекламные отчеты**

Для измерения количества рекламных кликов традиционно используется технология отслеживания, нарушающая конфиденциальность пользователей. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

Сама по себе эта функция не вызывает особых опасений в плане конфиденциальности, и хотя вы можете оставить ее включенной, мы рекомендуем её отключить, так как она автоматически отключается в Private Browsing.

##### Всегда включенный частный доступ

Откройте Safari и нажмите кнопку Вкладки, расположенную в правом нижнем углу. Затем разверните список Группы вкладок.

- [x] Выбери **Частный доступ**

Режим Частный доступ в Safari обеспечивает дополнительную защиту конфиденциальности. Приватный просмотр использует новую [эфемерную](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) сессию для каждой вкладки, то есть вкладки изолированы друг от друга. При использовании частного доступа есть и другие небольшие преимущества, например, не отправлять адрес веб-страницы в Apple при использовании функции перевода в Safari.

Обрати внимание, что частный доступ не сохраняет файлы cookie и данные веб-сайтов, поэтому оставаться залогиненным на сайтах не получится. Это может доставить неудобства.

##### Синхронизация iCloud

Синхронизация истории Safari, групп вкладок, вкладок iCloud и сохраненных паролей осуществляется с E2EE. However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://apple.com/legal/privacy/en-ww).

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/HT212520). Перейди к настройке **Apple ID → iCloud → Расширенная защита данных**.

- [x] Включи **Расширенная защита данных**

Если вы используете iCloud вместе с расширенной защитой данных, мы также рекомендуем проверить, что место по умолчанию для загрузки файлов в Safari установлено локально на устройстве. Эта опция может быть найдена в :gear: **Настройки** → **Safari** → **Основные** → **Загрузки**.

### AdGuard

<div class="admonition recommendation" markdown>

![Логотип AdGuard](assets/img/browsers/adguard.svg){ align=right }

**AdGuard для iOS** — это бесплатный и открытый блокировщик контента для Safari, который использует нативный [API блокировки контента](https://developer.apple.com/documentation/safariservices/creating_a_content_blocker).

AdGuard для iOS имеет несколько премиум-функций, хотя стандартные средства блокировки контента Safari бесплатны.

[:octicons-home-16: Homepage](https://adguard.com/en/adguard-ios/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/ios.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1047223162)

</details>

</div>

Дополнительные списки блокировки замедляют работу браузера и могут упростить атаку, поэтому пользуйся только тем, что тебе необходимо.

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Мы рекомендуем тебе ознакомиться с этим списком, прежде чем выбрать продукт, и провести собственное исследование, чтобы убедиться в правильности своего выбора.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Мы сейчас работаем над установлением точных критериев для каждого раздела нашего сайта, поэтому они могут поменяться в будущем. Если у тебя есть вопросы по поводу наших критериев, пожалуйста, [задавай их на нашем форуме](https://discuss.privacyguides.net/latest) и не думай, что мы не учли что-то при составлении наших рекомендаций, если это не указано здесь. Перед тем, как рекомендовать какой-либо проект мы учитываем и обсуждаем множество факторов. Документирование этих факторов ещё не завершено.

</div>

### Минимальные требования к сервисам

- Должен поддерживать автоматические обновления.
- Должен получать обновления движка в течение 0-1 дня после релиза в upstream.
- Любые изменения, необходимые для того, чтобы браузер больше соблюдал конфиденциальность, не должны негативно влиять на опыт использования.
- Браузеры для Android должны использовать движок Chromium.
    - К сожалению, Mozilla GeckoView все еще менее безопасен, чем Chromium на Android.
    - Браузеры для iOS ограничены использованием WebKit.

### Критерии для расширений

- Не должны копировать встроенную функциональность браузера или ОС.
- Должны непосредственно влиять на конфиденциальность пользователя, т.е. не просто предоставлять информацию.
