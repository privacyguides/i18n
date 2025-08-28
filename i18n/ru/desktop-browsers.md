---
meta_title: "Интернет браузеры, ориентированные на защиту конфиденциальности для ПК и Mac - Privacy Guides"
title: Браузеры для настольных компьютеров
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

Как и [Tor Browser](tor.md), браузер Mullvad разработан для предотвращения фингерпринтинга, делая отпечаток вашего браузера идентичным всем другим пользователям браузера Mullvad, и включает в себя настройки по умолчанию и расширения, которые автоматически настраиваются в соответствии с уровнями безопасности по умолчанию:  *Standard* (Стандартный),  *Safer* (Повышенный уровень) и  *Safest* (Самый безопасный).

Поэтому крайне важно, чтобы вы никак не модифицировали браузер, кроме настройки стандартных [уровней безопасности](https://tb-manual.torproject.org/security-settings). При изменении уровня безопасности вы **обязательно** должны перезапустить браузер перед продолжением его использования. В противном случае [настройки безопасности могут быть применены не полностью](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), что подвергает вас более высокому риску фингерпринтинга и эксплойтов, чем вы можете ожидать, исходя из выбранных настроек.

Модификации, отличные от регулировки этой настройки, сделают ваш отпечаток уникальным, что сведет на нет цель использования этого браузера. Если ты хочешь более комплексно настроить браузер и цифровые отпечатки тебя не волнуют, то мы рекомендуем использовать [Firefox](#firefox).

### Система скрытия цифровых отпечатков

**Без** использования [VPN](vpn.md), Mullvad Browser обеспечивает такую же защиту от [простых скриптов распознавания цифровых отпечатков](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting), как и другие конфиденциальные браузеры, такие как Firefox+[Arkenfox](#arkenfox-advanced) или [Brave](#brave). Mullvad Browser обеспечивает эту защиту из коробки, в обмен на некоторую гибкость и удобство, которые могут предоставить другие конфиденциальные браузеры.

==Для улучшения системы скрытия цифровых отпечатков мы рекомендуем использовать Mullvad Browser в сочетании **с** VPN==, будь то Mullvad или другой рекомендованный VPN провайдер. При использовании VPN с Mullvad Browser у тебя будет общий цифровой отпечаток браузера и пул IP-адресов со многими другими пользователями, что делает вас одной "толпой" в которой можно спрятаться. Эта стратегия - единственный способ противостоять продвинутым скриптам отслеживания, и это та же самая техника защиты от цифровых отпечатков, которую использует Tor Browser.

Обрати внимание, что, хотя ты и можешь использовать Mullvad Browser с любым VPN провайдером, другие люди с этим VPN также должны использовать Mullvad Browser, чтобы эта "толпа" существовала. Более вероятно, что люди, использующие Mullwad Browser, также используют Mullwad VPN. Mullvad Browser ни имеет встроенной возможности подключаться к VPN, ни проверяет, используете ли вы VPN; ваше VPN-соединение должно быть настроено и управляться отдельно.

Mullvad Browser поставляется с предустановленными расширениями *uBlock Origin* и *NoScript*. Хотя мы обычно не рекомендуем добавлять *дополнительные* [расширения для браузера](browser-extensions.md), эти расширения, которые поставляются предустановленными в браузер, **не** следует удалять или настраивать, потому что это сделает ваш отпечаток браузера заметно отличным от других пользователей Mullvad Browser. Он также поставляется с предустановленным расширением Mullvad Browser Extension, которое *можно* безопасно удалить без влияния на цифровой отпечаток браузера, оставить его тоже безопасно, даже если ты не используешь Mullvad VPN.

### Режим приватного просмотра

Mullvad Browser работает в постоянном режиме приватного просмотра, а это значит, что твоя история, файлы куки и другие данные сайтов будут очищаться при каждом закрытии браузера. Твои закладки, настройки браузера и настройки расширений будут сохранены.

Это необходимо для предотвращения продвинутых форм отслеживания, но за это приходится платить удобством и некоторыми функциями Firefox, например Multi-Account Containers. Помни, что ты всегда можешь использовать несколько браузеров, например: ты можешь использовать Firefox+Arkenfox для сайтов, на которых ты хочешь оставаться залогиненным или которые не работают должным образом в Mullvad Browser, и Mullvad Browser для регулярного браузинга.

### Mullvad Leta

Браузер Mullvad поставляется с [**Mullvad Leta**](search-engines.md#mullvad-leta) в качестве поисковой системы по умолчанию, которая функционирует как прокси для результатов поиска Google или Brave (настраивается на главной странице Mullvad Leta).

Если вы являетесь пользователем Mullvad VPN, то использование таких сервисов, как Mullvad Leta, которые предлагаются вашим провайдером VPN, сопряжено с некоторым риском. Это связано с тем, что Mullvad теоретически имеет доступ к вашему реальному IP-адресу (через их VPN) и вашей поисковой активности (через Leta); последнее — это информация, которую VPN обычно предназначен отделять. Несмотря на то, что Mullvad собирает очень мало информации о своих подписчиках VPN или пользователях Leta, вам следует рассмотреть возможность использования другого [поискового движка](search-engines.md), если этот риск вас беспокоит.

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

Эти настройки можно найти в :material-menu: → **Настройки**.

#### Поиск

- [ ] Отключите **Показывать поисковые предложения**

Функции поисковых предложений могут быть недоступны в вашем регионе.

Поисковые подсказки отправляют всё, что вы вводите в адресной строке, в поисковую систему по умолчанию, независимо от того, выполняете ли вы фактический поиск. Отключение поисковых подсказок позволяет вам более точно контролировать, какие данные вы отправляете провайдеру поисковой системы.

##### Firefox Suggest (Только США)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) — это функция, похожая на поисковые подсказки, которая доступна только в США. Мы рекомендуем отключить её по той же причине, по которой мы рекомендуем отключать поисковые подсказки. Если вы не видите эти параметры в разделе **Адресная строка**, у вас нет нового интерфейса, и вы можете игнорировать эти изменения.

- [ ] Отключите **Suggestions from Firefox**
- [ ] Отключите **Suggestions from sponsors**

#### Приватность и защита

##### Улучшенная защита от отслеживания:

- [x] Выберите **Строгая**

Это защищает вас, блокируя трекеры социальных сетей, скрипты для снятия цифровых отпечатков (обратите внимание, что это не защищает вас от *всех* видов фингерпринтинга), криптомайнеры, межсайтовые отслеживающие куки и некоторый другой отслеживающий контент. ETP защищает от многих распространенных угроз, но не блокирует все пути отслеживания, поскольку она разработана таким образом, чтобы оказывать минимальное влияние на удобство использования сайтов или не оказывать его вообще.

##### Отчистка при закрытии

Если вы хотите оставаться в системе на определенных сайтах, вы можете допустить исключения в **Куки и данные сайтов** → **Управление исключениями...**

- [x] Включите **Удалять куки и данные сайтов при закрытии Firefox**

Это защищает вас от постоянных файлов cookie, но не защищает от файлов cookie, полученных в течение одного сеанса просмотра. Когда эта функция включена, становится возможным легко очистить файлы cookie вашего браузера, просто перезапустив Firefox. Вы можете установить исключения для отдельных сайтов, если хотите оставаться в системе на определенном сайте, который вы часто посещаете.

##### Сбор и использование данных Firefox

- [ ] Отключите **Разрешить Firefox отправлять технические данные и данные взаимодействия в Mozilla**
- [ ] Отключите **Разрешить Firefox устанавливать и проводить исследования**
- [ ] Отключите **Разрешить Firefox отправлять от вашего имени накопившиеся сообщения о его падениях**

Согласно политике конфиденциальности Mozilla для Firefox,

> Firefox отправляет нам данные о версии и языке вашего Firefox; операционной системе устройства и конфигурации оборудования; памяти, основную информацию о сбоях и ошибках; результаты автоматизированных процессов, таких как обновления, безопасный просмотр и активация. Когда Firefox отправляет нам данные, ваш IP-адрес временно собирается как часть логов нашего сервера.

Кроме того, служба учетных записей Mozilla собирает [некоторые технические данные](https://mozilla.org/privacy/mozilla-accounts). Если вы используете учетную запись Mozilla, вы можете отказаться от этого:

1. Откройте [настройки вашего профиля на сайте accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Отключите **Data Collection and Use** > **Help improve Firefox Accounts**

##### Настройка рекламы для веб-сайтов

- [ ] Отключите **Разрешить веб-сайтам проводить измерение рекламы с сохранением приватности**

С выпуском Firefox 128 была добавлена новая настройка [атрибуции с сохранением конфиденциальности](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA), которая [включена по умолчанию](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA позволяет рекламодателям использовать ваш веб-браузер для измерения эффективности веб-кампаний вместо использования традиционного отслеживания на основе JavaScript. Мы считаем это поведение выходящим за рамки обязанностей пользовательского агента, и тот факт, что эта функция отключена по умолчанию в Arkenfox, является дополнительным показателем необходимости отключения этой функции.

##### Режим "Только HTTPS"

- [x] Включите **Включить режим «Только HTTPS» во всех окнах**

Это предотвращает непреднамеренное подключение к веб-сайту по открытому протоколу HTTP. Сайты без HTTPS сегодня встречаются редко, поэтому это должно оказывать минимальное влияние или не оказывать никакого влияния на ваш повседневный просмотр веб-страниц.

##### DNS через HTTPS

Если вы используете [поставщика DNS через HTTPS](dns.md):

- [x] Включите **Максимальная защита** и выберите подходящего поставщика

Максимальная защита обеспечивает использование DNS через HTTPS, и предупреждение о безопасности будет отображаться, если Firefox не может подключиться к вашему безопасному DNS-резолверу, или если ваш безопасный DNS-резолвер сообщает, что записи для домена, к которому вы пытаетесь получить доступ, не существуют. Это предотвращает возможность сети, к которой вы подключены, тайно понизить уровень безопасности вашего DNS.

#### Синхронизация

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) позволяет вашим данным просмотра (истории, закладкам и т.д.) быть доступными на всех ваших устройствах и защищает их сквозным E2EE шифрованием.

### Arkenfox (дополнительно)

<div class="admonition tip" markdown>
<p class="admonition-title">Используйте Mullvad Browser для улучшенной защиты от цифровых отпечатков</p>

[Mullvad Browser](#mullvad-browser) обеспечивает ту же защиту от цифровых отпечатков, что и Arkenfox, и не требует использования VPN Mullvad, чтобы воспользоваться этой защитой. В сочетании с VPN, Mullvad Browser может предотвратить более продвинутые скрипты отслеживания, которые Arkenfox не может. Преимущество Arkenfox в том, что он гораздо более гибкий и позволяет делать исключения для отдельных сайтов, на которых вам необходимо оставаться залогиненными.

</div>

[Проект Arkenfox](https://github.com/arkenfox/user.js) предоставляет набор тщательно продуманных параметров для Firefox. Если вы [решите](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) использовать Arkenfox, [несколько опций](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Общие]) являются субъективно строгими и/или могут привести к некорректной работе некоторых веб-сайтов — их можно [легко изменить](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) в соответствии с вашими потребностями. Мы **настоятельно рекомендуем** ознакомиться с их полной [вики](https://github.com/arkenfox/user.js/wiki). Arkenfox также включает поддержку [контейнеров](https://support.mozilla.org/kb/containers#w_for-advanced-users).

Arkenfox стремится только предотвратить базовые или примитивные отслеживающие скрипты через рандомизацию canvas и встроенные в Firefox настройки сопротивления снятию цифровых отпечатков. Он не стремится сделать ваш браузер неотличимым от большой группы других пользователей Arkenfox так, как это делают браузер Mullvad или Tor Browser, что является единственным способом противодействия продвинутым скриптам отслеживания по цифровым отпечаткам. Не забывайте о возможности использовать разные браузеры. К примеру, Firefox+Arkenfox можно применять для доверенных сайтов, где вам нужно сохранять авторизацию, а браузер Mullvad — для повседневного интернет-серфинга.

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

Эти настройки можно найти в :material-menu: → **Настройки**.

#### Защита

Brave включает некоторые меры против снятия цифровых отпечатков в своей функции [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Мы предлагаем настроить эти параметры [глобально](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) для всех страниц, которые вы посещаете.

Опции щитов можно понижать по мере необходимости для каждого конкретного сайта, но по умолчанию мы рекомендуем установить следующие параметры:

<div class="annotate" markdown>

- [x] Выберите **Агрессивный** в секции *Блокировка трекеров и рекламы*

<details class="warning" markdown>
<summary>Используйте списки фильтров по умолчанию</summary>

Brave позволяет выбирать дополнительные фильтры контента на внутренней странице `brave://adblock`. Мы не рекомендуем использовать эту функцию; вместо этого оставь списки фильтров по умолчанию. Использование дополнительных фильтров выделит тебя среди других пользователей Brave, а также может увеличить площадь атаки в том случае, если в Brave есть эксплойт и вредоносное правило будет добавлено в один из используемых тобой списков.

</details>

- [x] Выберите **Обязательно** для опции *Переключаться на HTTPS*
- [x] (Опционально) Включите опцию **Блокировать скрипты** (1)
- [x] Включите **Блокировка цифровых отпечатков**
- [x] Выберите **Блокировать сторонние файлы cookie**
- [x] Включите **Удалять данные о посещении этого сайта** (2)
- [ ] Отключите все опции в **Блокировка социальных сетей**

</div>

1. Эта опция отключает JavaScript, что приведет к неработоспособности многих сайтов. Чтобы исправить это, вы можете установить исключения для отдельных сайтов, нажав на значок Щита в адресной строке и сняв флажок с этой настройки в разделе *Advanced controls*.
2. Если вы хотите оставаться в системе на определенном сайте, который часто посещаете, вы можете установить исключения для этого сайта, нажав на значок Щита в адресной строке и сняв флажок с этой настройки в разделе *Advanced controls*.

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

##### Окна Tor

[**Приватное окно с Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) позволяет направлять ваш трафик через сеть Tor в приватных окнах и получать доступ к .onion сервисам, что может быть полезно в некоторых случаях. Однако Brave **не** так устойчив к снятию цифровых отпечатков, как Tor Browser, и гораздо меньше людей используют Brave с Tor, поэтому вы будете выделяться. Если ваша модель угроз требует сильной анонимности, используйте [Tor Browser](tor.md#tor-browser).

##### Сбор данных

- Отключите **Разрешить аналитику продукта с сохранением конфиденциальности (P3A)**
- Отключить **Автоматически отправлять ежедневный пинг использования в Brave**
- Отключить **Автоматически отправлять диагностические отчёты**

#### Web3

Brave's Web3 features can potentially add to your browser fingerprint and attack surface. Unless you use any of these features, they should be disabled.

- Select **Extensions (no fallback)** under *Default Ethereum wallet*
- Select **Extensions (no fallback)** under *Default Solana wallet*

#### Extensions

- [ ] Uncheck all built-in extensions you don't use

#### Поисковая система

We recommend disabling search suggestions in Brave for the same reason we recommend disabling this feature in [Firefox](#search).

- [ ] Отключите **Показывать подсказки при поиске**

#### Система

<div class="annotate" markdown>

- [ ] Uncheck **Continue running background apps when Brave is closed** to disable background apps (1)

</div>

1. Эта опция присутствует не на всех платформах.

#### Синхронизация Brave

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Награды Brave и Кошелёк

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

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
