---
meta_title: "Интернет браузеры соблюдающие конфиденциальность для ПК и Мак - Privacy Guides"
title: "Браузеры для настольных компьютеров"
icon: material/laptop
description: These privacy-protecting browsers are what we currently recommend for standard/non-anonymous internet browsing on desktop systems.
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

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Капитализм слежки](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our currently recommended **desktop web browsers** and configurations for standard/non-anonymous browsing. Мы рекомендуем [Mullvad Browser](#mullvad-browser), если тебе важна надежная защита конфиденциальности и защита от цифровых отпечатков из коробки, [Firefox](#firefox) для людей, ищущих альтернативу Google Chrome, и [Brave](#brave), если тебе нужна совместимость с браузером Chromium.

Если тебе нужна анонимность в сети, то используй [Tor](tor.md). На этой странице мы даем некоторые рекомендации по настройке браузеров, но все браузеры, кроме Tor Browser, могут быть отслежены *кем-то* тем или иным способом.

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** is a version of [Tor Browser](tor.md#tor-browser) with Tor network integrations removed. It aims to provide to VPN users Tor Browser's anti-fingerprinting browser technologies, which are key protections against [:material-eye-outline: Mass Surveillance](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. Он разработан проектом Tor и распространяется [Mullvad](vpn.md#mullvad), и **не** требует использования VPN Mullvad.

[:octicons-home-16: Домашняя страница](https://mullvad.net/ru/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/ru/help/privacy-policy){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://mullvad.net/ru/help/tag/mullvad-browser){ .card-link title=Документация}
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

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title=Documentation}
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title=Contribute }

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

Firefox includes a unique [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) in downloads from Mozilla's website and uses telemetry in Firefox to send the token. The token is **not** included in releases from the [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Recommended Firefox Configuration

Эти параметры можно найти в разделе :material-menu: → **Настройки**.

#### Поиск

- [ ] Uncheck **Show search suggestions**

Функции поисковых предложений могут быть недоступны в твоём регионе.

Поисковые предложения отправляют всё, что ты набираешь в адресной строке, в поисковую систему по умолчанию, независимо от того, запускаешь ли ты фактический поиск. Отключение поисковых предложений позволяет более точно контролировать данные, которые вы отправляете поисковой системе.

##### Предложения Firefox (Только США)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. Мы рекомендуем отключить его по той же причине, по которой мы рекомендуем отключать поисковые предложения. Если ты не видишь этих опций в **адресной строке**, то у тебя нет этой функции и ты можешь игнорировать эти изменения.

- [ ] Uncheck **Suggestions from Firefox**
- [ ] Отключи **Suggestions from sponsors**

#### Приватность и защита

##### Улучшенная защита от отслеживания:

- [x] Выбери **Строгая**

Она защищает тебя, блокируя трекеры социальных сетей, скрипты цифровых отпечатков (обрати внимание, что она не защищает тебя от *всех* цифровых отпечатков), криптомайнеры, межсайтовые файлы куки для отслеживания и некоторые другие средства отслеживания. Улучшенная защита от отслеживания защищает от многих распространенных угроз, но не блокирует все пути отслеживания, поскольку разработана таким образом, чтобы минимально или вообще не влиять на удобство использования сайта.

##### Отчистка при закрытии

Если ты хочешь оставаться залогиненным на некоторых сайтах, то ты можешь создать исключения в **Куки и данные сайтов** → **Управление исключениями...**

- [x] Выбери **Удалять куки и данные сайтов при закрытии Firefox**

Это защитит тебя от постоянных файлов куки, но не защитит от файлов куки, полученных в течение одного сеанса просмотра. Когда эта функция включена, можно легко очистить куки браузера, просто перезапустив Firefox. Ты можешь установить исключения для каждого сайта, если хочешь оставаться залогиненным на определенном сайте, который ты часто посещаешь.

##### Сбор и использование данных Firefox

- [ ] Отключи **Разрешить Firefox отправлять технические данные и данные взаимодействия в Mozilla**
- [ ] Отключи **Разрешить Firefox устанавливать и проводить исследования**
- [ ] Отключи **Разрешить Firefox отправлять от вашего имени накопившиеся сообщения о его падениях**

> Firefox отправляет нам данные о версии и языке вашего Firefox; операционной системе устройства и конфигурации оборудования; памяти, основную информацию о сбоях и ошибках; результаты автоматизированных процессов, таких как обновления, безопасный просмотр и активация. Когда Firefox отправляет нам данные, ваш IP-адрес временно собирается как часть логов нашего сервера.

Additionally, the Mozilla Accounts service collects [some technical data](https://mozilla.org/privacy/mozilla-accounts). If you use a Mozilla Account you can opt-out:

1. Открой [настройки профиля на сайте accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Отключи **Сбор и использование данных** > **Помогите улучшить ⁨аккаунты Firefox⁩**

##### Website Advertising Preferences

- [ ] Uncheck **Allow websites to perform privacy-preserving ad measurement**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.

##### HTTPS-Only Mode

- [x] Выбери **Включить режим «Только HTTPS» во всех окнах**

Это предотвращает непреднамеренное подключение к веб-сайту с обычным HTTP-текстом. Протокол HTTP в настоящее время используется крайне редко, поэтому эта настройка практически не должна повлиять на твой ежедневный браузинг.

##### DNS через HTTPS

Если вы используете [провайдера DNS через HTTPS](dns.md):

- [x] Включите **Максимальная защита** и выберите подходящего поставщика

Максимальная защита разрешает только DNS через HTTPS запросы. Если Firefox не сможет подключиться к вашему безопасному провайдеру DNS или если ваш безопасный провайдер DNS не найдёт записи для нужного домена, появится предупреждение безопасности. Это остановит сеть, к которой вы подключены, от секретного понижения безопасности DNS.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (дополнительно)

<div class="admonition tip" markdown>
<p class="admonition-title">Use Mullvad Browser for advanced anti-fingerprinting</p>

[Mullvad Browser](#mullvad-browser) обеспечивает ту же защиту от цифровых отпечатков, что и Arkenfox, и не требует использования VPN Mullvad, чтобы воспользоваться этой защитой. В сочетании с VPN, Mullvad Browser может предотвратить более продвинутые скрипты отслеживания, которые Arkenfox не может. Преимущество Arkenfox в том, что он гораздо более гибкий и позволяет делать исключения для отдельных сайтов, на которых вам необходимо оставаться залогиненными.

</div>

[Проект Arkenfox](https://github.com/arkenfox/user.js) предоставляет набор тщательно подобранных настроек для Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly—which you can [easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. Мы **настоятельно рекомендуем** ознакомиться с их [вики](https://github.com/arkenfox/user.js/wiki). Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

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

### Recommended Brave Configuration

Эти параметры можно найти в разделе :material-menu: → **Настройки**.

#### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

Опции щитов можно понижать по мере необходимости для каждого конкретного сайта, но по умолчанию мы рекомендуем установить следующие параметры:

<div class="annotate" markdown>

- [x] Select **Aggressive** under *Trackers & ads blocking*

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. Мы не рекомендуем использовать эту функцию; вместо этого оставь списки фильтров по умолчанию. Использование дополнительных фильтров выделит тебя среди других пользователей Brave, а также может увеличить площадь атаки в том случае, если в Brave есть эксплойт и вредоносное правило будет добавлено в один из используемых тобой списков.

</details>

- [x] Select **Strict** under *Upgrade connections to HTTPS*
- [x] (Optional) Select **Block Scripts** (1)
- [x] Check **Block fingerprinting**
- [x] Select **Block third-party cookies**
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option disables JavaScript, which will break a lot of sites. To unbreak them, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

#### Privacy and security

<div class="annotate" markdown>

- [x] Select **Don't allow sites to use the V8 optimizer** under *Security* → *Manage V8 security* (1)
- [x] Select **Automatically remove permissions from unused sites** under *Sites and Shields Settings*
- [x] Select **Disable non-proxied UDP** under [*WebRTC IP Handling Policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **Prevent sites from fingerprinting me based on my language preferences**

</div>

1. Disabling the V8 optimizer reduces your attack surface by disabling [*some*](https://grapheneos.social/@GrapheneOS/112708049232710156) parts of JavaScript Just-In-Time (JIT) compilation.

<div class="admonition tip" markdown>
<p class="admonition-title">Sanitizing on close</p>

- [x] Select **Delete data sites have saved to your device when you close all windows** under *Sites and Shields Settings* → *Content* → *Additional content settings* → *On-device site data*.

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

##### Tor windows

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) allows you to route your traffic through the Tor network in Private Windows and access .onion services, which may be useful in some cases. However, Brave is **not** as resistant to fingerprinting as the Tor Browser and far fewer people use Brave with Tor, so you will stand out. If your threat model requires strong anonymity, use the [Tor Browser](tor.md#tor-browser).

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

#### System

<div class="annotate" markdown>

- [ ] Отключи **Продолжить выполнение фоновых приложений после закрытия Brave**, чтобы отключить фоновые приложения (1)

</div>

1. Эта опция присутствует не на всех платформах.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. Она опирается на кастодиальный аккаунт и KYC от определенного числа провайдеров. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Кошелек Brave** работает локально на твоём компьютере, но не поддерживает никаких конфиденциальных криптовалют, поэтому мы бы не советовали использовать и эту функцию.

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Мы рекомендуем тебе ознакомиться с этим списком, прежде чем выбрать продукт, и провести собственное исследование, чтобы убедиться в правильности своего выбора.

### Минимальные требования

- Должен иметь открытый исходный код.
- Должен поддерживать автоматические обновления.
- Must receive engine updates in 0-1 days from upstream release.
- Must be available on Linux, macOS, and Windows.
- Any changes required to make the browser more privacy-respecting must not negatively impact user experience.
- Must block third-party cookies by default.
- Must support [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Should include built-in content blocking functionality.
- Should support cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Should support Progressive Web Apps. PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps, because PWAs benefit from your browser's regular security updates.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Should not collect telemetry by default.
- Should provide an open-source sync server implementation.
- Should default to a [private search engine](search-engines.md).

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
