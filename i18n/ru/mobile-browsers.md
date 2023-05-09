---
meta_title: "Мобильные браузеры для Android и iOS, соблюдающие конфиденциальность - Privacy Guides"
title: "Мобильные браузеры"
icon: material/cellphone-information
description: Мы рекомендуем эти браузеры для обычного/неанонимного браузинга в интернете на вашем телефоне.
cover: mobile-browsers.png
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
    url: https://www.apple.com/safari/
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

Здесь перечислены мобильные браузеры, которые мы рекомендуем, и руководства по их настройке для обычного/неанонимного браузинга. Если вам нужна анонимность в сети, используйте [Tor](tor.md). Мы рекомендуем использовать как можно меньше расширений, так как они имеют привилегированный доступ к браузеру, требуют доверия к их разработчикам, могут [идентифицировать тебя](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), а также [ослабляют](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) изоляцию между сайтами.

## Android

На Android браузер Firefox менее безопасен, чем основанные на Chromium альтернативы: движок Mozilla, [GeckoView](https://mozilla.github.io/geckoview/), ещё не поддерживает [изоляцию сайтов](https://hacks.mozilla.org/2021/05/introducing-firefox-new-site-isolation-security-architecture) и не включает [isolatedProcess](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196).

### Brave

!!! recommendation

    ![Логотип Brave](assets/img/browsers/brave.svg){ align=right }
    
    **Brave Browser** включает встроенный блокировщик контента и [инструменты конфиденциальности](https://brave.com/privacy-features/), многие из которых включены по умолчанию.
    
    Brave основан на Chromium, поэтому он покажется тебе знакомым, а также у него не должно быть проблем совместимости с сайтами.
    
    [:octicons-home-16: Домашняя страница](https://brave.com/ru/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion-сайт" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Исходный код" }
    
    ??? скачать
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

#### Рекомендованные настройки

Tor Browser — это единственный способ действительно анонимно пользоваться интернетом. Если ты используешь Brave, мы рекомендуем изменить следующие настройки, чтобы сохранить приватность, но все браузеры кроме [Tor](tor.md#tor-browser) могут *кем-нибудь* отслеживаться в том или ином виде.

Эти настройки можно найти в :material-menu: → **Настройки** → **Brave Щит и конфиденциальность**

##### Щиты

Brave включает несколько инструментов защиты от отслеживания в разделе [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-). Мы рекомендуем включить эти настройки [для всех сайтов](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-), которые ты посещаешь.

##### Общие настройки по умолчанию системы Brave Schields

Опции щитов можно понижать по мере необходимости для каждого конкретного сайта, но по умолчанию мы рекомендуем установить следующие параметры:

<div class="annotate" markdown>

- [x] Выбери **Строгий режим** в разделе "Блокировать трекеры и рекламу"

    ??? предупреждение «Используй стандартные фильтры»
        Brave позволяет тебе выбрать дополнительные фильтры на внутренней странице `brave://adblock`. Мы не рекомендуем использовать эту функцию; вместо этого оставь списки фильтров по умолчанию. Использование дополнительных фильтров выделит тебя среди других пользователей Brave, а также может увеличить площадь атаки, если в Brave есть эксплойт и вредоносное правило будет добавлено в один из используемых тобой списков.

- [x] Выбери **Переключаться на HTTPS**
- [x] Выбери **Всегда использовать безопасные соединения**
- [x] (Опционально) Выбери **Блокировать скрипты** (1)
- [x] Выбери **Строго, может нарушать работу сайтов** в **Блокировать определение отпечатков**

</div>

1. Эта опция обеспечивает функциональность, аналогичную расширенным [режимам блокировки](https://github.com/gorhill/uBlock/wiki/Blocking-mode) uBlock Origin или расширения [NoScript](https://noscript.net/).

##### Очистить историю

- [x] Выбери **Удалять данные при выходе**

##### Блокировка соцсетей

- [ ] Отключи все переключатели в этой секции

##### Другие настройки конфиденциальности

<div class="annotate" markdown>

- [x] Выбери **Отключить непроксируемый протокол UDP** в [Политика обработки IP WebRTC](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Отключи **Разрешить сайтам проверять наличие сохраненных способов оплаты**
- [ ] Отключи **Шлюз IPFS** (1)
- [x] Включи **Закрывать вкладки при входе**
- [ ] Отключи **Разрешить выполнение аналитики продукта, не нарушающей конфеденциальности**
- [ ] Отключи **Автоматически отправлять данные диагностики**
- [ ] Отключи **Автоматически отправлять ежедневные данные PING в Brave**

</div>

1. Interplanetary File System (IPFS) - это децентрализованная, peer-to-peer сеть для хранения и обмена данными в распределенной файловой системе. Если ты не используешь эту функцию, отключи ее.

#### Синхронизация

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) позволяет синхронизировать данные браузера (историю, закладки и т. д.) между несколькими устройствами без необходимости создавать аккаунт, а также защищает их при помощи E2EE.

## iOS

На iOS любое приложение, которое может открывать веб-страницы, [использует](https://developer.apple.com/app-store/review/guidelines) только предоставляемый Apple [движок WebKit](https://developer.apple.com/documentation/webkit), поэтому нет особых причин использовать сторонний браузер.

### Safari

!!! recommendation

    ![Логотип Safari](assets/img/browsers/safari.svg){ align=right }
    
    **Safari** — браузер по умолчанию на iOS. Он включает в себя [функции обеспечения конфиденциальности](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0): Intelligent Tracking Protection, отчет о конфиденциальности, изолированные вкладки частного доступа, частный узел iCloud и автоматическое обновление до HTTPS.
    
    [:octicons-home-16: Домашняя страница](https://www.apple.com/ru/safari/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.apple.com/ru/legal/privacy/data/ru/safari/){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://support.apple.com/ru-ru/guide/safari/welcome/mac){ .card-link title=Документация}

#### Рекомендованные настройки

Эти параметры можно найти в разделе :gear: **Настройки** → **Safari** → **Конфиденциальность и безопасность**.

##### Предотвращение перекрёстного отслеживания

- [x] Включи **Предотвращать перекрестное отслеживание**

Это активирует функцию WebKit: [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). Эта функция помогает защититься от нежелательного отслеживания, используя машинное обучение на устройстве для остановки отслеживающих устройств. ITP защищает от многих распространенных угроз, но не блокирует все пути слежения, поскольку разработан таким образом, чтобы не мешать удобству использования сайта.

##### Отчет о конфиденциальности

«Отчет о конфиденциальности» представляет собой обзор межсайтовых трекеров, которым в настоящее время запрещено создавать ваш профиль на посещаемом вами сайте. Функция также показывает еженедельный отчет о количестве заблокированных трекеров в течение определенного времени.

Отчет о конфиденциальности доступен через меню "Настройки страницы".

##### Privacy Preserving Ad Measurement

- [ ] Disable **Privacy Preserving Ad Measurement**

Ad click measurement has traditionally used tracking technology that infringes on user privacy. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm/) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

The feature has little privacy concerns on its own, so while you can choose to leave it on, we consider the fact that it's automatically disabled in Private Browsing to be an indicator for disabling the feature.

##### Always-on Private Browsing

Open Safari and tap the Tabs button, located in the bottom right. Then, expand the Tab Groups list.

- [x] Select **Private**

Safari's Private Browsing mode offers additional privacy protections. Private Browsing uses a new [ephemeral](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) session for each tab, meaning tabs are isolated from one another. There are also other smaller privacy benefits with Private Browsing, such as not sending a webpage’s address to Apple when using Safari's translation feature.

Do note that Private Browsing does not save cookies and website data, so it won't be possible to remain signed into sites. This may be an inconvenience.

##### iCloud Sync

Synchronization of Safari History, Tab Groups, iCloud Tabs and saved passwords are E2EE. However, by default, bookmarks are [not](https://support.apple.com/en-us/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://www.apple.com/legal/privacy/en-ww/).

You can enable E2EE for you Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/en-us/HT212520). Go to your **Apple ID name → iCloud → Advanced Data Protection**.

- [x] Turn On **Advanced Data Protection**

If you use iCloud with Advanced Data Protection disabled, we also recommend checking to ensure Safari's default download location is set to locally on your device. This option can be found in :gear: **Settings** → **Safari** → **General** → **Downloads**.

### AdGuard

!!! recommendation

    ![Логотип AdGuard](assets/img/browsers/adguard.svg){ align=right }
    
    **AdGuard для iOS** — это бесплатный и открытый блокировщик контента для Safari, который использует нативный [API блокировки контента](https://developer.apple.com/documentation/safariservices/creating_a_content_blocker).
    
    AdGuard для iOS имеет несколько премиум-функций, хотя стандартные средства блокировки контента Safari бесплатны.
    
    [:octicons-home-16: Домашняя страница](https://adguard.com/ru/adguard-ios/overview.html){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://adguard.com/ru/privacy/ios.html){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="Исходный код" }
    
    ??? скачать
    
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id1047223162)

Дополнительные списки блокировки замедляют работу браузера и могут упростить атаку, поэтому пользуйся только тем, что тебе необходимо.

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Мы рекомендуем тебе ознакомиться с этим списком, прежде чем выбрать продукт, и провести собственное исследование, чтобы убедиться в правильности своего выбора.

!!! пример "Это новая секция"

    Мы сейчас работаем над установлением точных критериев для каждого раздела нашего сайта, поэтому они могут поменяться в будущем. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. Мы учитываем и обсуждаем много факторов, перед тем как рекомендовать какой-то проект, и документирование каждого из них ещё не завершено.

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
