---
meta_title: "Интернет браузеры соблюдающие конфиденциальность для ПК и Мак - Privacy Guides"
title: "Браузеры для настольных компьютеров"
icon: material/laptop
description: Эти браузеры обеспечивают более надежную защиту конфиденциальности, чем Google Chrome.
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

Здесь перечислены рекомендуемые браузеры для настольных компьютеров и руководства по их настройке для обычного (не анонимного) браузинга. Мы рекомендуем [Mullvad Browser](#mullvad-browser), если тебе важна надежная защита конфиденциальности и защита от цифровых отпечатков из коробки, [Firefox](#firefox) для людей, ищущих альтернативу Google Chrome, и [Brave](#brave), если тебе нужна совместимость с браузером Chromium.

Если тебе нужна анонимность в сети, то используй [Tor](tor.md). На этой странице мы даем некоторые рекомендации по настройке браузеров, но все браузеры, кроме Tor Browser, могут быть отслежены *кем-то* тем или иным способом.

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Логотип Mullvad Browser](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** - это версия [Tor Browser](tor.md#tor-browser) с удаленными интеграциями сети Tor, предназначенная для предоставления пользователям VPN браузерных технологий Tor Browser по борьбе с цифровыми отпечатками. Он разработан проектом Tor и распространяется [Mullvad](vpn.md#mullvad), и **не** требует использования VPN Mullvad.

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Как и [Tor Browser](tor.md), Mullvad Browser разработан для предотвращения цифровых отпечатков, делая цифровые отпечатки вашего браузера идентичными цифровым отпечаткам всех других пользователей Mullvad Browser. Также он содержит настройки и расширения по умолчанию, которые автоматически конфигурируются выбранным уровнем безопасности: *Standart*, *Safe* и *Safest*. Therefore, it is imperative that you do not modify the browser at all outside adjusting the default [security levels](https://tb-manual.torproject.org/security-settings). Другие модификации сделают твой цифровой отпечаток браузера уникальным, что лишает смысла использование этого браузера. Если ты хочешь более комплексно настроить браузер и цифровые отпечатки тебя не волнуют, то мы рекомендуем использовать [Firefox](#firefox).

### Система скрытия цифровых отпечатков

**Без** использования [VPN](vpn.md), Mullvad Browser обеспечивает такую же защиту от [простых скриптов распознавания цифровых отпечатков](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting), как и другие конфиденциальные браузеры, такие как Firefox+[Arkenfox](#arkenfox-advanced) или [Brave](#brave). Mullvad Browser обеспечивает эту защиту из коробки, в обмен на некоторую гибкость и удобство, которые могут предоставить другие конфиденциальные браузеры.

==Для улучшения системы скрытия цифровых отпечатков мы рекомендуем использовать Mullvad Browser в сочетании **с** VPN==, будь то Mullvad или другой рекомендованный VPN провайдер. При использовании VPN с Mullvad Browser у тебя будет общий цифровой отпечаток браузера и пул IP-адресов со многими другими пользователями, что делает вас одной "толпой" в которой можно спрятаться. Эта стратегия - единственный способ противостоять продвинутым скриптам отслеживания, и это та же самая техника защиты от цифровых отпечатков, которую использует Tor Browser.

Обрати внимание, что, хотя ты и можешь использовать Mullvad Browser с любым VPN провайдером, другие люди с этим VPN также должны использовать Mullvad Browser, чтобы эта "толпа" существовала. Более вероятно, что люди, использующие Mullwad Browser, также используют Mullwad VPN. Mullvad Browser ни имеет встроенной возможности подключаться к VPN, ни проверяет, используете ли вы VPN; ваше VPN-соединение должно быть настроено и управляться отдельно.

Mullvad Browser поставляется с предустановленными расширениями *uBlock Origin* и *NoScript*. While we typically discourage adding *additional* [browser extensions](browser-extensions.md), these extensions that come pre-installed with the browser should **not** be removed or configured outside their default values, because doing so would noticeably make your browser fingerprint distinct from other Mullvad Browser users. Он также поставляется с предустановленным расширением Mullvad Browser Extension, которое *можно* безопасно удалить без влияния на цифровой отпечаток браузера, оставить его тоже безопасно, даже если ты не используешь Mullvad VPN.

### Режим приватного просмотра

Mullvad Browser работает в постоянном режиме приватного просмотра, а это значит, что твоя история, файлы куки и другие данные сайтов будут очищаться при каждом закрытии браузера. Твои закладки, настройки браузера и настройки расширений будут сохранены.

Это необходимо для предотвращения продвинутых форм отслеживания, но за это приходится платить удобством и некоторыми функциями Firefox, например Multi-Account Containers. Помни, что ты всегда можешь использовать несколько браузеров, например: ты можешь использовать Firefox+Arkenfox для сайтов, на которых ты хочешь оставаться залогиненным или которые не работают должным образом в Mullvad Browser, и Mullvad Browser для регулярного браузинга.

### Mullvad Leta

Mullvad Browser поставляется с включенной по умолчанию [поисковой системой](search-engines.md) DuckDuckGo. В нём также есть предустановленная **Mullvad Leta** - поисковая система, для доступа к которой требуется активная подписка Mullvad VPN. Mullvad Leta напрямую запрашивает API платного поиска Google (именно поэтому он ограничен для платных подписчиков), однако из-за этого ограничения Mullvad может связать поисковые запросы и учетные записи Mullvad VPN. По этой причине мы не рекомендуем использовать Mullvad Leta, несмотря на то, что Mullvad собирает очень мало информации о своих подписчиках VPN.

## Firefox

<div class="admonition recommendation" markdown>

![Логотип Firefox](assets/img/browsers/firefox.svg){ align=right }

**Firefox** предоставляет сильные настройки конфиденциальности, такие как [Улучшенная защита от отслеживания](https://support.mozilla.org/ru/kb/uluchshennaya-zashita-ot-otslezhivaniya-firefox-dlya-kompyutera), которые могут помочь блокировать различные [типы отслеживания](https://support.mozilla.org/ru/kb/uluchshennaya-zashita-ot-otslezhivaniya-firefox-dlya-kompyutera#w_chto-blokiruet-uluchshennaia-zashchita-ot-otslezhivaniia).

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://firefox-source-docs.mozilla.org){ .card-link title=Documentation}
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

Firefox includes a unique [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) in downloads from Mozilla's website and uses telemetry in Firefox to send the token. The token is **not** included in releases from the [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Recommended Firefox Configuration

Эти параметры можно найти в :material-menu: → **Настройки**

#### Поиск

- [ ] Отключи **Отображать поисковые предложения**

Функции поисковых предложений могут быть недоступны в твоём регионе.

Поисковые предложения отправляют всё, что ты набираешь в адресной строке, в поисковую систему по умолчанию, независимо от того, запускаешь ли ты фактический поиск. Отключение поисковых предложений позволяет более точно контролировать данные, которые вы отправляете поисковой системе.

#### Приватность и защита

##### Улучшенная защита от отслеживания:

- [x] Выбери **Строгая**

Она защищает тебя, блокируя трекеры социальных сетей, скрипты цифровых отпечатков (обрати внимание, что она не защищает тебя от *всех* цифровых отпечатков), криптомайнеры, межсайтовые файлы куки для отслеживания и некоторые другие средства отслеживания. Улучшенная защита от отслеживания защищает от многих распространенных угроз, но не блокирует все пути отслеживания, поскольку разработана таким образом, чтобы минимально или вообще не влиять на удобство использования сайта.

##### Предложения Firefox (Только США)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. Мы рекомендуем отключить его по той же причине, по которой мы рекомендуем отключать поисковые предложения. Если ты не видишь этих опций в **адресной строке**, то у тебя нет этой функции и ты можешь игнорировать эти изменения.

- [ ] Отключи **Suggestions from the web**
- [ ] Отключи **Suggestions from sponsors**

##### Отчистка при закрытии

Если ты хочешь оставаться залогиненным на некоторых сайтах, то ты можешь создать исключения в **Куки и данные сайтов** → **Управление исключениями...**

- [x] Выбери **Удалять куки и данные сайтов при закрытии Firefox**

Это защитит тебя от постоянных файлов куки, но не защитит от файлов куки, полученных в течение одного сеанса просмотра. Когда эта функция включена, можно легко очистить куки браузера, просто перезапустив Firefox. Ты можешь установить исключения для каждого сайта, если хочешь оставаться залогиненным на определенном сайте, который ты часто посещаешь.

##### Сбор и использование данных Firefox

- [ ] Отключи **Разрешить Firefox отправлять технические данные и данные взаимодействия в Mozilla**
- [ ] Отключи **Разрешить Firefox устанавливать и проводить исследования**
- [ ] Отключи **Разрешить Firefox отправлять от вашего имени накопившиеся сообщения о его падениях**

> Firefox отправляет нам данные о версии и языке вашего Firefox; операционной системе устройства и конфигурации оборудования; памяти, основную информацию о сбоях и ошибках; результаты автоматизированных процессов, таких как обновления, безопасный просмотр и активация. Когда Firefox отправляет нам данные, ваш IP-адрес временно собирается как часть логов нашего сервера.

Additionally, the Firefox Accounts service collects [some technical data](https://mozilla.org/privacy/firefox/#firefox-accounts). Если ты используешь учетную запись Firefox, то ты можешь отключить сбор этих данных:

1. Открой [настройки профиля на сайте accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Отключи **Сбор и использование данных** > **Помогите улучшить ⁨аккаунты Firefox⁩**

##### Режим «Только HTTPS»:

- [x] Выбери **Включить режим «Только HTTPS» во всех окнах**

Это предотвращает непреднамеренное подключение к веб-сайту с обычным HTTP-текстом. Протокол HTTP в настоящее время используется крайне редко, поэтому эта настройка практически не должна повлиять на твой ежедневный браузинг.

##### DNS через HTTPS

Если вы используете [провайдера DNS через HTTPS](dns.md):

- [x] Включите **Максимальная защита** и выберите подходящего поставщика

Максимальная защита разрешает только DNS через HTTPS запросы. Если Firefox не сможет подключиться к вашему безопасному провайдеру DNS или если ваш безопасный провайдер DNS не найдёт записи для нужного домена, появится предупреждение безопасности. Это остановит сеть, к которой вы подключены, от секретного понижения безопасности DNS.

#### Синхронизация

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (дополнительно)

<div class="admonition tip" markdown>
<p class="admonition-title">Use Mullvad Browser for advanced anti-fingerprinting</p>

[Mullvad Browser](#mullvad-browser) обеспечивает ту же защиту от цифровых отпечатков, что и Arkenfox, и не требует использования VPN Mullvad, чтобы воспользоваться этой защитой. В сочетании с VPN, Mullvad Browser может предотвратить более продвинутые скрипты отслеживания, которые Arkenfox не может. Преимущество Arkenfox в том, что он гораздо более гибкий и позволяет делать исключения для отдельных сайтов, на которых вам необходимо оставаться залогиненными.

</div>

[Проект Arkenfox](https://github.com/arkenfox/user.js) предоставляет набор тщательно подобранных настроек для Firefox. Если ты [решишь](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) использовать Arkenfox, то [несколько опций](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) являются субъективно строгими и/или могут привести к неправильной работе некоторых сайтов. [Эти настройки ты можешь легко изменить](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) в соответствии с твоими потребностями. Мы **настоятельно рекомендуем** ознакомиться с их [вики](https://github.com/arkenfox/user.js/wiki). Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox нацелен только на предотвращение основных или наивных сценариев отслеживания с помощью рандомизации холста и встроенных в Firefox настроек конфигурации сопротивления отпечатку браузера. Он не стремится к тому, чтобы ваш браузер сливался с большой толпой других пользователей Arkenfox так, как это делают Mullvad Browser или Tor Browser, что является единственным способом помешать продвинутым сценариям отслеживания отпечатков браузера. Помни, что ты всегда можешь использовать несколько браузеров, например: ты можешь использовать Firefox+Arkenfox для сайтов, на которых ты хочешь оставаться залогиненным или которые не работают должным образом в Mullvad Browser, и Mullvad Browser для регулярного браузинга.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave основан на Chromium, поэтому он покажется тебе знакомым, а также у него не должно быть проблем совместимости с вебсайтами.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-windows11: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

**Пользователям macOS:** При скачивании Brave Browser с их официального сайта вы получаете установщик `.pkg`, который требует прав администратора для запуска (и может запускать другие ненужные скрипты на вашем устройстве). В качестве альтернативы, вы можете скачать последнюю версию файла `Brave-Browser-universal.dmg` из их [GitHub releases](https://github.com/brave/brave-browser/releases/latest), которая предоставляет традиционную установку "перетащить в папку Программы".

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

Brave добавляет "[реферальный код](https://github. om/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" к имени файла при загрузке с веб-сайта Brave. Этот код используется для отслеживания источника, из которого код был загружен браузер, например `BRV002` в загрузках с именем `Brave-Browser-BRV002.pkg`. В конце процесса установки программа установки отправит на сервер Brave реферальный код. Если вас это беспокоит, вы можете переименовать установочный файл перед его открытием.

</div>

### Recommended Brave Configuration

Эти параметры можно найти в разделе :material-menu: → **Настройки**.

#### Настройки

##### Защита

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

Опции щитов можно понижать по мере необходимости для каждого конкретного сайта, но по умолчанию мы рекомендуем установить следующие параметры:

<div class="annotate" markdown>

- [x] Select **Prevent sites from fingerprinting me based on my language preferences**
- [x] Select **Aggressive** under Trackers & ads blocking

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. Мы не рекомендуем использовать эту функцию; вместо этого оставь списки фильтров по умолчанию. Использование дополнительных фильтров выделит тебя среди других пользователей Brave, а также может увеличить площадь атаки в том случае, если в Brave есть эксплойт и вредоносное правило будет добавлено в один из используемых тобой списков.

</details>

- [x] Select **Strict** under **Upgrade connections to HTTPS**
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Strict, may break sites** under Block fingerprinting
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode).
2. Если вы хотите оставаться залогиненными на определенном сайте, который вы часто посещаете, вы можете установить исключения для каждого сайта, нажав на значок щита в адресной строке.

##### Конфиденциальность и безопасность

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP Handling Policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Private window with Tor** (1)

</div>

1. Brave **не так устойчив** к цифровым отпечаткам, как Tor Browser, и гораздо меньше людей используют Brave вместе с Tor, поэтому ты будешь выделяться. Where [strong anonymity is required](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) use the [Tor Browser](tor.md#tor-browser).

<div class="admonition tip" markdown>
<p class="admonition-title">Sanitizing on close</p>

- [x] In the *Sites and Shields Settings* menu, under Content, after clicking on the *On-device site data* menu, select **Delete data sites have saved to your device when you close all windows**

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

##### Расширения

Отключи встроенные расширения, которые ты не используешь, в разделе **Расширения**

- [ ] Отключи **Hangouts**
- [ ] Отключи **WebTorrent**

##### Web3

Функции Web3 в Brave потенциально могут увеличить цифровой отпечаток твоего браузера и площадь атаки. Если ты не используешь эти функции, их следует отключить.

- Выберите **Расширения (без бэкапа)** в Кошелек Ethereum по умолчанию и Кошелек Solana по умолчанию
- В **Метод преобразования IPFS-ресурсов** выберите **Отключено**

##### Система

<div class="annotate" markdown>

- [ ] Отключи **Продолжить выполнение фоновых приложений после закрытия Brave**, чтобы отключить фоновые приложения (1)

</div>

1. Эта опция присутствует не на всех платформах.

#### Синхронизация

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Вознаграждение Brave и Кошелек

**Вознаграждения Brave** позволяют получать криптовалюту Basic Attention Token (BAT) за выполнение определенных действий в Brave. Она опирается на кастодиальный аккаунт и KYC от определенного числа провайдеров. Мы не рекомендуем использовать BAT в качестве [конфиденциальной криптовалюты](cryptocurrency.md), также мы не рекомендуем использовать [кастодиальный кошелек](advanced/payments.md#other-coins-bitcoin-ethereum-etc), поэтому мы не советуем использовать эту функцию.

**Кошелек Brave** работает локально на твоём компьютере, но не поддерживает никаких конфиденциальных криптовалют, поэтому мы бы не советовали использовать и эту функцию.

## Дополнительные ресурсы

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Мы рекомендуем тебе ознакомиться с этим списком, прежде чем выбрать продукт, и провести собственное исследование, чтобы убедиться в правильности своего выбора.

### Минимальные требования

- Должен иметь открытый исходный код.
- Должен поддерживать автоматические обновления.
- Должен получать обновления движка в течение 0-1 дня после релиза в upstream.
- Доступен для Linux, macOS и Windows.
- Любые изменения, необходимые для того, чтобы браузер больше соблюдал конфиденциальность, не должны негативно влиять на опыт использования.
- По умолчанию блокирует сторонние файлы куки.
- Supports [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Включает в себя встроенную функцию блокировки контента.
- Supports cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Supports Progressive Web Apps. PWAs enable you to install certain websites as if they were native apps on your computer. Это может иметь преимущества перед установкой приложений на базе Electron, поскольку вы получаете преимущества от регулярных обновлений безопасности вашего браузера.
- Не включает дополнительные функции (bloatware), которые не влияют на конфиденциальность пользователя.
- По умолчанию не собирает телеметрию.
- Предоставляет реализацию сервера синхронизации с открытым исходным кодом.
- По умолчанию включена [конфиденциальная поисковая система](search-engines.md).

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
