---
meta_title: "Интернет браузеры, ориентированные на защиту конфиденциальности для ПК и Mac - Privacy Guides"
title: "Браузеры для настольных компьютеров"
icon: material/laptop
description: В настоящее время мы рекомендуем эти браузеры с фокусом на защиту конфиденциальности для обычного использования на десктопах (ПК и Mac).
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Рекомендации приватных браузеров для настольных компьютеров
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/ru/browser
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Firefox
    image: /assets/img/browsers/firefox.svg
    url: https://firefox.com
    sameAs: https://en.wikipedia.org/wiki/Firefox
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    sameAs: https://en.wikipedia.org/wiki/Brave_(web_browser)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Защищает от следующих угроз:</small>

- [:material-account-cash: Капитализм слежки](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Это наши актуальные рекомендации **десктопных браузеров** и конфигураций для стандартного/неанонимного использования. Мы рекомендуем [Mullvad Browser](#mullvad-browser), если тебе важна надежная защита конфиденциальности и защита от цифровых отпечатков из коробки, [Firefox](#firefox) для людей, ищущих альтернативу Google Chrome, и [Brave](#brave), если тебе нужна совместимость с браузером Chromium.

Если тебе нужна анонимность в сети, то используй [Tor](tor.md). На этой странице мы даем некоторые рекомендации по настройке браузеров, но все браузеры, кроме Tor Browser, могут быть отслежены *кем-то* тем или иным способом.

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Логотип Mullvad Browser](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** это версия [браузера Tor](tor.md#tor-browser) в которой удалили интеграцию сети Tor. Его задача — совместить Mullvad VPN и функции браузера Tor, защищающие от цифровых отпечатков. Эти функции являются важным инструментом против [:material-eye-outline: Массового наблюдения](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. Он разработан проектом Tor и распространяется [Mullvad](vpn.md#mullvad), и **не** требует использования VPN Mullvad.

[:octicons-home-16: Домашняя страница](https://mullvad.net/ru/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="Документация" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Исходный код" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Как и [Tor Browser](tor.md), Mullvad Browser разработан для предотвращения отслеживания, делая цифровые отпечатки вашего браузера идентичными цифровым отпечаткам всех других пользователей Mullvad Browser. Также он содержит настройки и расширения по умолчанию, которые автоматически конфигурируются выбранным уровнем безопасности: *Стандартный*, *Безопасный* и *Самый безопасный*. Поэтому крайне важно не изменять другие настройки браузера, кроме [настроек безопасности](https://tb-manual.torproject.org/security-settings) по умолчанию. Другие модификации сделают твой цифровой отпечаток браузера уникальным, что лишает смысла использование этого браузера. Если ты хочешь более комплексно настроить браузер и цифровые отпечатки тебя не волнуют, то мы рекомендуем использовать [Firefox](#firefox).

### Система скрытия цифровых отпечатков

**Без** использования [VPN](vpn.md), Mullvad Browser обеспечивает такую же защиту от [простых скриптов распознавания цифровых отпечатков](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting), как и другие конфиденциальные браузеры, такие как Firefox+[Arkenfox](#arkenfox-advanced) или [Brave](#brave). Mullvad Browser обеспечивает эту защиту из коробки, в обмен на некоторую гибкость и удобство, которые могут предоставить другие конфиденциальные браузеры.

==Для улучшения системы скрытия цифровых отпечатков мы рекомендуем использовать Mullvad Browser в сочетании **с** VPN==, будь то Mullvad или другой рекомендованный VPN провайдер. При использовании VPN с Mullvad Browser у тебя будет общий цифровой отпечаток браузера и пул IP-адресов со многими другими пользователями, что делает вас одной "толпой" в которой можно спрятаться. Эта стратегия - единственный способ противостоять продвинутым скриптам отслеживания, и это та же самая техника защиты от цифровых отпечатков, которую использует Tor Browser.

Обрати внимание, что, хотя ты и можешь использовать Mullvad Browser с любым VPN провайдером, другие люди с этим VPN также должны использовать Mullvad Browser, чтобы эта "толпа" существовала. Более вероятно, что люди, использующие Mullwad Browser, также используют Mullwad VPN. Mullvad Browser ни имеет встроенной возможности подключаться к VPN, ни проверяет, используете ли вы VPN; ваше VPN-соединение должно быть настроено и управляться отдельно.

Mullvad Browser поставляется с предустановленными расширениями *uBlock Origin* и *NoScript*. Хотя мы обычно не рекомендуем добавлять *дополнительные* [расширения для браузера](browser-extensions.md), эти расширения, которые поставляются предустановленными в браузер, **не** следует удалять или настраивать, потому что это сделает ваш отпечаток браузера заметно отличным от других пользователей Mullvad Browser. Он также поставляется с предустановленным расширением Mullvad Browser Extension, которое *можно* безопасно удалить без влияния на цифровой отпечаток браузера, оставить его тоже безопасно, даже если ты не используешь Mullvad VPN.

### Режим приватного просмотра

Mullvad Browser работает в постоянном режиме приватного просмотра, а это значит, что твоя история, файлы куки и другие данные сайтов будут очищаться при каждом закрытии браузера. Твои закладки, настройки браузера и настройки расширений будут сохранены.

Это необходимо для предотвращения продвинутых форм отслеживания, но за это приходится платить удобством и некоторыми функциями Firefox, например Multi-Account Containers. Помни, что ты всегда можешь использовать несколько браузеров, например: ты можешь использовать Firefox+Arkenfox для сайтов, на которых ты хочешь оставаться залогиненным или которые не работают должным образом в Mullvad Browser, и Mullvad Browser для регулярного браузинга.

### Mullvad Leta

Mullvad Browser поставляется с включенной по умолчанию [поисковой системой](search-engines.md) DuckDuckGo. В нём также есть предустановленная **Mullvad Leta** - поисковая система, для доступа к которой требуется активная подписка Mullvad VPN. Mullvad Leta напрямую использует платный API поисковика Google, поэтому она доступна только для платных подписчиков. Однако благодаря этому ограничению Mullvad теоретически может сопоставить поисковые запросы и учетные записи Mullvad VPN. По этой причине мы не рекомендуем использовать Mullvad Leta, несмотря на то, что Mullvad собирает очень мало информации о своих подписчиках VPN.

## Firefox

<div class="admonition recommendation" markdown>

![Логотип Firefox](assets/img/browsers/firefox.svg){ align=right }

**Firefox** предоставляет сильные настройки конфиденциальности, такие как [Улучшенная защита от отслеживания](https://support.mozilla.org/ru/kb/uluchshennaya-zashita-ot-otslezhivaniya-firefox-dlya-kompyutera), которые могут помочь блокировать различные [типы отслеживания](https://support.mozilla.org/ru/kb/uluchshennaya-zashita-ot-otslezhivaniya-firefox-dlya-kompyutera#w_chto-blokiruet-uluchshennaia-zashchita-ot-otslezhivaniia).

[:octicons-home-16: Домашняя страница](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="Документация" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Исходный код" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Поддержать" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

Firefox добавляет уникальный [маркер загрузки](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) к загрузкам с сайта Mozilla и использует телеметрию для отправки этого маркера. Токен **не** добавляется при скачивании с [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Рекомендуемые настройки Firefox

Эти параметры можно найти в разделе :material-menu: → **Настройки**.

#### Поиск

- [ ] Отключите **Показывать поисковые предложения**

Функции предложения поиска могут быть недоступны в вашем регионе.

Поисковые предложения отправляют все введенные в адресную строку данные в поисковую систему по умолчанию, независимо от того, выполняется ли фактический поиск. Отключение поисковых предложений предоставляет возможность более строго контролировать данные, отправляемые в поисковую систему.

##### Firefox Suggest (Только США)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) - это функция, аналогичная поисковым предложениям, которая доступна только в США. Мы рекомендуем отключить его по той же причине, по которой мы рекомендуем отключать поисковые предложения. Если указанные опции не отображаются в **адресной строке**, это означает, что данная функция недоступна, и вы можете игнорировать эти изменения.

- [ ] Отключите **Suggestions from Firefox**
- [ ] Отключите **Suggestions from sponsors**

#### Приватность и защита

##### Улучшенная защита от отслеживания:

- [x] Выберите **Строгая**

Она обеспечивает защиту, блокируя трекеры социальных сетей, криптомайнеры, межсайтовые куки для отслеживания, скрипты цифровых отпечатков (следует отметить, что она не защищает от *всех* цифровых отпечатков) и другие механизмы слежения. Улучшенная защита от отслеживания обеспечивает защиту от множества распространенных угроз, однако не блокирует все способы отслеживания, поскольку она разработана с учетом минимального или отсутствующего влияния на функциональность сайтов.

##### Отчистка при закрытии

Если вы хотите оставаться залогиненным на некоторых сайтах, вы можете создать исключения в **Куки и данные сайтов** → **Управление исключениями...**

- [x] Включите **Удалять куки и данные сайтов при закрытии Firefox**

Это защитит вас от постоянных файлов куки, но не предотвратит сохранение файлов куки, полученных в течение одного сеанса просмотра. Когда эта функция включена, можно легко очистить куки браузера, просто перезапустив Firefox. Вы можете создать исключения для сайтов, на которых часто бываете и хотите оставаться залогиненным.

##### Сбор и использование данных Firefox

- [ ] Отключите **Разрешить Firefox отправлять технические данные и данные взаимодействия в Mozilla**
- [ ] Отключите **Разрешить Firefox устанавливать и проводить исследования**
- [ ] Отключите **Разрешить Firefox отправлять от вашего имени накопившиеся сообщения о его падениях**

Информация из политики конфиденциальности Mozilla для Firefox:

> Firefox отправляет нам данные о версии и языке вашего Firefox; операционной системе устройства и конфигурации оборудования; памяти, основную информацию о сбоях и ошибках; результаты автоматизированных процессов, таких как обновления, безопасный просмотр и активация. Когда Firefox отправляет нам данные, ваш IP-адрес временно собирается как часть логов нашего сервера.

Кроме того, аккаунт Mozilla собирает [некоторые технические данные](https://mozilla.org/privacy/mozilla-accounts). Если вы используете аккаунт Mozilla, вы можете отключить сбор этих данных:

1. Откройте [настройки вашего профиля на сайте accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Uncheck **Data Collection and Use** > **Help improve Firefox Accounts**

##### Настройка рекламы для веб-сайтов

- [ ] Отключите **Разрешить веб-сайтам проводить измерение рекламы с сохранением приватности**

С выходом Firefox 128 была добавлена новая настройка: [Атрибуция с сохранением конфиденциальности](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA), которая [включена по умолчанию](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA позволяет рекламодателям использовать ваш веб-браузер для оценки эффективности рекламы, заменяя традиционное отслеживание, основанное на JavaScript. Мы считаем, что такое поведение выходит за пределы обязанностей пользовательского агента, и тот факт, что оно отключено по умолчанию в Arkenfox, является дополнительным аргументом для отключения этой функции.

##### Режим "Только HTTPS"

- [x] Включите **Включить режим «Только HTTPS» во всех окнах**

Это предотвращает непреднамеренное подключение к веб-сайту с обычным HTTP-текстом. Протокол HTTP в настоящее время используется крайне редко, поэтому эта настройка практически не должна повлиять на твой ежедневный браузинг.

##### DNS через HTTPS

Если вы используете [провайдера DNS через HTTPS](dns.md):

- [x] Включите **Максимальная защита** и выберите подходящего поставщика

Максимальная защита разрешает только DNS через HTTPS запросы. Если Firefox не сможет подключиться к вашему безопасному провайдеру DNS или если ваш безопасный провайдер DNS не найдёт записи для нужного домена, появится предупреждение безопасности. Это остановит сеть, к которой вы подключены, от секретного понижения безопасности DNS.

#### Синхронизация

[Синхронизация Firefox](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) позволяет получать доступ к данным вашего браузера (история, закладки и т.д.) на всех ваших устройствах и защищает их с использованием сквозного шифрования (E2EE).

### Arkenfox (дополнительно)

<div class="admonition tip" markdown>
<p class="admonition-title">Используйте Mullvad Browser для улучшенной защиты от цифровых отпечатков</p>

[Mullvad Browser](#mullvad-browser) обеспечивает ту же защиту от цифровых отпечатков, что и Arkenfox, и не требует использования VPN Mullvad, чтобы воспользоваться этой защитой. В сочетании с VPN, Mullvad Browser может предотвратить более продвинутые скрипты отслеживания, которые Arkenfox не может. Преимущество Arkenfox в том, что он гораздо более гибкий и позволяет делать исключения для отдельных сайтов, на которых вам необходимо оставаться залогиненными.

</div>

[Проект Arkenfox](https://github.com/arkenfox/user.js) предоставляет набор тщательно подобранных настроек для Firefox. Если вы [решите](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) использовать Arkenfox, [некоторые параметры](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) могут быть субъективно строгими и/или привести к некорректной работе некоторых сайтов, но вы сможете [легко изменить](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) их в соответствии с вашими потребностями. Мы **настоятельно рекомендуем** ознакомиться с их [вики](https://github.com/arkenfox/user.js/wiki). Arkenfox также активирует поддержку [контейнеров](https://support.mozilla.org/kb/containers#w_for-advanced-users).

Arkenfox нацелен только на предотвращение основных или наивных сценариев отслеживания с помощью рандомизации холста и встроенных в Firefox настроек конфигурации сопротивления отпечатку браузера. Он не стремится к тому, чтобы ваш браузер сливался с большой толпой других пользователей Arkenfox так, как это делают Mullvad Browser или Tor Browser, что является единственным способом помешать продвинутым сценариям отслеживания отпечатков браузера. Помните, что всегда можно использовать несколько браузеров. Например, вы можете использовать Firefox+Arkenfox для сайтов, на которых хотите оставаться залогиненным или которые не функционируют корректно в Mullvad Browser, а для обычного серфинга — использовать Mullvad Browser.

## Brave

<div class="admonition recommendation annotate" markdown>

![Логотип Brave](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** содержит встроенный блокировщик рекламы и [функции конфиденциальности](https://brave.com/privacy-features), многие из которых уже включены по умолчанию.

Brave основан на Chromium, поэтому он будет вам знаком, а также не должен вызывать проблем с совместимостью с вебсайтами.

[:octicons-home-16: Домашняя страница](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Сервис Onion" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Документация" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Исходный код" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

Brave добавляет "[реферальный код](https://github. om/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" к имени файла при загрузке с веб-сайта Brave. Этот код используется для отслеживания источника, из которого код был загружен браузер, например `BRV002` в загрузках с именем `Brave-Browser-BRV002.pkg`. В конце процесса установки программа установки отправит на сервер Brave реферальный код. Если вас это беспокоит, вы можете переименовать установочный файл перед его открытием.

</div>

### Рекомендуемые настройки Brave

Эти параметры можно найти в разделе :material-menu: → **Настройки**.

#### Защита

Brave включает в себя несколько мер для борьбы с цифровыми отпечатками в рамках своей функции [Щит/Защита](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Мы рекомендуем настроить эти параметры [глобально](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) для всех страниц, которые вы посещаете.

Опции защиты можно понижать по мере необходимости для каждого конкретного сайта, но по умолчанию мы рекомендуем установить следующие параметры:

<div class="annotate" markdown>

- [x] Выберите **Агрессивный** в секции *Блокировка трекеров и рекламы*

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. Мы не рекомендуем использовать эту функцию; вместо этого оставь списки фильтров по умолчанию. Использование дополнительных фильтров выделит тебя среди других пользователей Brave, а также может увеличить площадь атаки в том случае, если в Brave есть эксплойт и вредоносное правило будет добавлено в один из используемых тобой списков.

</details>

- [x] Выберите **Обязательно** для опции *Переключаться на HTTPS*
- [x] (Опционально) Включите опцию **Блокировать скрипты** (1)
- [x] Включите **Блокировка цифровых отпечатков**
- [x] Выберите **Блокировать сторонние файлы cookie**
- [x] Включите **Удалять данные о посещении этого сайта** (2)
- [ ] Отключите все опции в **Блокировка социальных сетей**

</div>

1. This option disables JavaScript, which will break a lot of sites. To unbreak them, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

#### Конфиденциальность и безопасность

<div class="annotate" markdown>

- [x] Выберите **Запретить сайтам использовать оптимизатор V8** в *Безопасность* → *Оптимизатор V8* (1)
- [x] Включите **Автоматически удалять разрешения для неиспользуемых сайтов** в *Настройки сайта и Shields*
- [x] Выберите **Отключить непроксируемый протокол UDP** в [*Политика обработки IP WebRTC*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Отключите **Использовать сервисы Google для обмена push-сообщениями**
- [x] Включите **Автоматичсеки перенаправлять с AMP-страниц**
- [x] Включите **Автоматичсеки перенаправлять URL-адреса отслеживания**
- [x] Включите **Запрещать сайтам использовать цифровые отпечатки для выбора языка**

</div>

1. Отключение оптимизатора V8 уменьшает площадь атаки за счет отключения [*некоторых*](https://grapheneos.social/@GrapheneOS/112708049232710156) частей компиляции JavaScript Just-In-Time (JIT).

<div class="admonition tip" markdown>
<p class="admonition-title">Отчистка при закрытии</p>

- [x] Выберите **Удалять данные сайтов, сохранённые на устройстве, при закрытии всех окон** в *Настройки сайта и Shields* → *Контент* → *Дополнительные настройки контента* → *Данные сайтов, сохранённые на устройстве*.

Если вы хотите оставаться залогиненным на сайте, который часто посещаете, вы можете настроить исключения для каждого ресурса, кликнув на значок щита в адресной строке.

</div>

##### Окна Tor

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) allows you to route your traffic through the Tor network in Private Windows and access .onion services, which may be useful in some cases. However, Brave is **not** as resistant to fingerprinting as the Tor Browser is, and far fewer people use Brave with Tor, so you will stand out. If your threat model requires strong anonymity, use the [Tor Browser](tor.md#tor-browser).

##### Data Collection

- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**

#### Web3

Функции Web3 в Brave потенциально могут увеличить цифровой отпечаток твоего браузера и площадь атаки. Unless you use any of these features, they should be disabled.

- Select **Extensions (no fallback)** under *Default Ethereum wallet*
- Select **Extensions (no fallback)** under *Default Solana wallet*

#### Extensions

- [ ] Uncheck all built-in extensions you don't use

#### Поисковая система

Мы рекомендуем отключить подсказки поиска в Brave по той же причине, по которой мы рекомендуем отключить эту функцию в [Firefox](#search).

- [ ] Отключите **Показывать подсказки при поиске**

#### Система

<div class="annotate" markdown>

- [ ] Отключите **Продолжить выполнение фоновых приложений после закрытия Brave**, чтобы отключить фоновые приложения (1)

</div>

1. Эта опция присутствует не на всех платформах.

#### Синхронизация Brave

[Синхронизация Brave](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) позволяет синхронизировать данные браузера (историю, закладки и т. д.) между несколькими устройствами без необходимости создавать аккаунт, а также защищает их при помощи E2EE.

#### Награды Brave и Кошелёк

**Вознаграждение Brave** позволяет получать криптовалюту Basic Attention Token (BAT) за выполнение определенных действий в Brave. Она опирается на кастодиальный аккаунт и KYC от определенного числа провайдеров. Мы не рекомендуем использовать BAT в качестве [конфиденциальной криптовалюты](cryptocurrency.md), также мы не рекомендуем использовать [кастодиальный кошелек](advanced/payments.md#wallet-custody), поэтому мы не советуем использовать эту функцию.

**Кошелек Brave** работает локально на твоём компьютере, но не поддерживает никаких конфиденциальных криптовалют, поэтому мы бы не советовали использовать и эту функцию.

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Мы рекомендуем тебе ознакомиться с этим списком, прежде чем выбрать продукт, и провести собственное исследование, чтобы убедиться в правильности своего выбора.

### Минимальные требования

- Должен быть с открытым исходным кодом.
- Должен поддерживать автоматические обновления.
- Must receive engine updates in 0-1 days from upstream release.
- Должен быть доступен на Linux, macOS и Windows.
- Все изменения, направленные на улучшение конфиденциальности браузера, не должны отрицательно сказываться на удобстве его использования.
- Должен блокировать сторонние куки по умолчанию.
- Must support [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Should include built-in content blocking functionality.
- Should support cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Should support Progressive Web Apps (PWAs). PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps because PWAs benefit from your browser's regular security updates.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Should not collect telemetry by default.
- Should provide an open-source sync server implementation.
- Should default to a [private search engine](search-engines.md).

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
