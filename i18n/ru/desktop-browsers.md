---
meta_title: "Интернет браузеры соблюдающие конфиденциальность для PC и Mac - Privacy Guides"
title: "Браузеры для настольных компьютеров"
icon: material/laptop
description: Эти браузеры обеспечивают более надежную защиту конфиденциальности, чем Google Chrome.
cover: desktop-browsers.png
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

Здесь перечислены рекомендуемые браузеры для настольных компьютеров и руководства по их настройке для обычного (не анонимного) пользования интернетом. Мы рекомендуем [Mullvad Browser](#mullvad-browser), если вам важна надежная защита конфиденциальности и защита от определения отпечатков из коробки, [Firefox](#firefox) для казуальных пользователей, ищущих хорошую альтернативу Google Chrome, и [Brave](#brave), если вам нужна совместимость с браузером Chromium.

Если вам нужна анонимность в сети, используйте [Tor](tor.md). Мы даем некоторые рекомендации по настройке на этой странице, но все браузеры, кроме Tor Browser, могут быть отслежены *кем-то* тем или иным способом.

## Mullvad Browser

!!! recommendation

    ![Логотип Mullvad Browser](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    **Mullvad Browser** - это версия [Tor Browser](tor.md#tor-browser) с удаленными интеграциями сети Tor, предназначенная для предоставления пользователям VPN браузерных технологий Tor Browser по борьбе с определением отпечатков. It is developed by the Tor Project and distributed by [Mullvad](vpn.md#mullvad), and does **not** require the use of Mullvad's VPN.
    
    [:octicons-home-16: Домашняя страница](https://mullvad.net/en/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }
    
    ??? загрузить
    
        - [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

Like [Tor Browser](tor.md), Mullvad Browser is designed to prevent fingerprinting by making your browser fingerprint identical to all other Mullvad Browser users, and it includes default settings and extensions that are automatically configured by the default security levels: *Standard*, *Safer* and *Safest*. Therefore, it is imperative that you do not modify the browser at all outside adjusting the default [security levels](https://tb-manual.torproject.org/security-settings/). Other modifications would make your fingerprint unique, defeating the purpose of using this browser. If you want to configure your browser more heavily and fingerprinting is not a concern for you, we recommend [Firefox](#firefox) instead.

### Anti-Fingerprinting

**Without** using a [VPN](vpn.md), Mullvad Browser provides the same protections against [naive fingerprinting scripts](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) as other private browsers like Firefox+[Arkenfox](#arkenfox-advanced) or [Brave](#brave). Mullvad Browser provides these protections out of the box, at the expense of some flexibility and convenience that other private browsers can provide.

==For the strongest anti-fingerprinting protection, we recommend using Mullvad Browser in conjunction **with** a VPN==, whether that is Mullvad or another recommended VPN provider. When using a VPN with Mullvad Browser, you will share a fingerprint and a pool of IP addresses with many other users, giving you a "crowd" to blend in with. This strategy is the only way to thwart advanced tracking scripts, and is the same anti-fingerprinting technique used by Tor Browser.

Note that while you can use Mullvad Browser with any VPN provider, other people on that VPN must also be using Mullvad Browser for this "crowd" to exist, something which is more likely on Mullvad VPN compared to other providers, particularly this close to the launch of Mullvad Browser. Mullvad Browser does not have built-in VPN connectivity, nor does it check whether you are using a VPN before browsing; your VPN connection has to be configured and managed separately.

Mullvad Browser comes with the *uBlock Origin* and *NoScript* browser extensions pre-installed. While we typically [don't recommend](#extensions) adding *additional* browser extensions, these extensions that come pre-installed with the browser should **not** be removed or configured outside their default values, because doing so would noticeably make your browser fingerprint distinct from other Mullvad Browser users. It also comes pre-installed with the Mullvad Browser Extension, which *can* be safely removed without impacting your browser fingerprint if you would like, but is also safe to keep even if you don't use Mullvad VPN.

### Режим приватного просмотра

Mullvad Browser operates in permanent private browsing mode, meaning your history, cookies, and other site data will always be cleared every time the browser is closed. Your bookmarks, browser settings, and extension settings will still be preserved.

This is required to prevent advanced forms of tracking, but does come at the cost of convenience and some Firefox features, such as Multi-Account Containers. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise don't work properly in Mullvad Browser, and Mullvad Browser for general browsing.

### Mullvad Leta

Mullvad Browser comes with DuckDuckGo set as the default [search engine](search-engines.md), but it also comes preinstalled with **Mullvad Leta**, a search engine which requires an active Mullvad VPN subscription to access. Mullvad Leta queries Google's paid search API directly (which is why it is limited to paying subscribers), however because of this limitation it is possible for Mullvad to correlate search queries and Mullvad VPN accounts. For this reason we discourage the use of Mullvad Leta, even though Mullvad collects very little information about their VPN subscribers.

## Firefox

!!! recommendation

    ![Логотип Bromite](assets/img/browsers/bromite.svg){ align=right }
    
    **Bromite** - это браузер, основанный на [Chromium](https://en.wikipedia.org/wiki/Chromium_(web_browser)), с основой на конфиденциальность и безопасность, встроенную блокировку рекламы и некоторую рандомизацию цифровых отпечатков.
    
    [Перейти на bromite.org](https://www.bromite.org){ .md-button .md-button--primary } [Политика конфиденциальности](https://www.bromite.org/privacy){ .md-button } downloads
    
        - [:simple-windows11: Windows](https://www.mozilla.org/firefox/windows)
        - [:simple-apple: macOS](https://www.mozilla.org/firefox/mac)
        - [:simple-linux: Linux](https://www.mozilla.org/firefox/linux)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

!!! warning
    Каждый установщик Firefox с веб-сайта Mozilla имеет в себе уникальный идентификатор, который используется для телеметрии. Идентификатор **не** включен в релизы браузера из [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

### Рекомендованные настройки

Эти параметры можно найти в :material-menu: → **Настройки**

#### Поиск

- [ ] Отключите **Отображать поисковые предложения**

Функции предложения поиска могут быть недоступны в вашем регионе.

Поисковые предложения отправляют все, что вы набираете в адресной строке, в поисковую систему по умолчанию, независимо от того, отправляете ли вы фактический поиск. Отключение поисковых предложений позволяет более точно контролировать данные, которые вы отправляете поставщику поисковых систем.

#### Приватность и защита

##### Улучшенная защита от отслеживания:

- Выберите «Строгая»

Это защищает вас, блокируя трекеры социальных сетей, скрипты цифровых отпечатков (обратите внимание, что это не защищает вас от *всех* цифровых отпечатков), криптомайнеры, межсайтовые файлы cookie для отслеживания и некоторые другие средства отслеживания. Улучшенная защита от отслеживания защищает от многих распространенных угроз, но не блокирует все пути отслеживания, поскольку разработан таким образом, чтобы минимально или вообще не влиять на удобство использования сайта.

##### Предложения Firefox (Только США)

[Firefox Suggest](https://support.mozilla.org/en-US/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. We recommend disabling it for the same reason we recommend disabling search suggestions. If you don't see these options under the **Address Bar** header, you do not have the new experience and can ignore these changes.

- [ ] Uncheck **Suggestions from the web**
- [ ] Uncheck **Suggestions from sponsors**

##### Отчистка при закрытии

Если вы хотите оставаться залогиненными на некоторых сайтах, то вы можете создать исключения в **Куки и данные сайтов** → **Управление исключениями...**

- Выберите «Удалять куки и данные сайтов при закрытии Firefox»

Это защищает вас от постоянных файлов cookie, но не защищает вас от файлов cookie, полученных в течение одного сеанса просмотра. Когда эта функция включена, можно легко очистить куки браузера, просто перезапустив Firefox. Вы можете установить исключения для каждого сайта, если вы хотите оставаться зарегистрированным на определенном сайте, который вы часто посещаете.

##### Сбор и использование данных Firefox

- [ ] Отключите **Разрешить Firefox отправлять технические данные и данные взаимодействия в Mozilla**
- [ ] Отключите **Разрешить Firefox устанавливать и проводить исследования**
- [ ] Отключите **Разрешить Firefox отправлять от вашего имени накопившиеся сообщения о его падениях**

> Firefox sends data about your Firefox version and language; device operating system and hardware configuration; memory, basic information about crashes and errors; outcome of automated processes like updates, safebrowsing, and activation to us. When Firefox sends data to us, your IP address is temporarily collected as part of our server logs.

Кроме того, служба Firefox Accounts собирает [некоторые технические данные](https://www.mozilla.org/en-US/privacy/firefox/#firefox-accounts). Если вы используете учетную запись Firefox, вы можете отключить сбор этих данных:

1. Откройте [настройки профиля на сайте accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Отключие **Сбор и использование данных** > **Помогите улучшить ⁨аккаунты Firefox⁩**

##### Режим «Только HTTPS»:

- Выберите: "Включить режим «Только HTTPS» во всех окнах".

Это предотвращает непреднамеренное подключение к веб-сайту с обычным HTTP-текстом. Протокол HTTP в настоящее время используется крайне редко, поэтому это практически не должно повлиять на ваш ежедневный просмотр веб-страниц.

#### Синхронизация

[Синхронизация Firefox](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) делает данные вашего браузера (история, закладки и т.д.) доступными на всех ваших устройствах и защищает их с помощью E2EE.

### Arkenfox (дополнительно)

!!! совет "Используйте Mullvad Browser для продвинутой защиты от цифровых отпечатков"

    [Mullvad Browser](#mullvad-browser) обеспечивает ту же защиту от цифровых отпечатков, что и Arkenfox, и не требует использования VPN Mullvad, чтобы воспользоваться этой защитой. Coupled with a VPN, Mullvad Browser can thwart more advanced tracking scripts which Arkenfox cannot. Arkenfox still has the advantage of being much more flexible, and allowing per-site exceptions for websites which you need to stay logged in to.

[Проект Arkenfox](https://github.com/arkenfox/user.js) предоставляет набор тщательно подобранных настроек для Firefox. Если ты [решишь](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) использовать Arkenfox, то [несколько опций](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) являются субъективно строгими и/или могут привести к неправильной работе некоторых сайтов. [Эти настройки ты можешь легко изменить](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) в соответствии с твоими потребностями. Мы **настоятельно рекомендуем** ознакомиться с их [вики](https://github.com/arkenfox/user.js/wiki). Arkenfox также включает поддержку [контейнеров](https://support.mozilla.org/ru/kb/kontejnery).

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

## Brave

!!! recommendation

    ![Логотип Brave](assets/img/browsers/brave.svg){ align=right }
    
    **Браузер Brave** включает встроенный блокировщик контента и [инструменты конфиденциальности](https://brave.com/privacy-features/), многие из которых включены по умолчанию.
    
    Brave основан на Chromium, поэтому он покажется вам знакомым, а также у него не должно быть проблем с совместимостью.
    
    [:octicons-home-16: Официальный сайт](https://brave.com/ru/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion-сайт" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Исходный код" }
    
    ??? downloads annotate
    
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
        - [:simple-windows11: Windows](https://brave.com/download/)
        - [:simple-apple: macOS](https://brave.com/download/)
        - [:simple-linux: Linux](https://brave.com/linux/) (1)

    1. We advise against using the Flatpak version of Brave, as it replaces Chromium's sandbox with Flatpak's, which is less effective. Additionally, the package is not maintained by Brave Software, Inc.

### Рекомендованные настройки

Эти параметры можно найти в разделе :material-menu: → **Настройки**.

#### Настройки

##### Защита

Brave включает несколько инструментов защиты от отслеживания в разделе [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-). Мы рекомендуем включить эти настройки [на всех сайтах](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-), которые вы посещаете.

Опции щитов можно понижать по мере необходимости для каждого конкретного сайта, но по умолчанию мы рекомендуем установить следующие параметры:

<div class="annotate" markdown>

- [x] Выберите **Запрещать сайтам использовать цифровые отпечатки для выбора языка**
- [x] Выберите **Агрессивный** в разделе: Блокировка трекеров и рекламы

    ??? предупреждение «Дополнительные фильтры»
        Brave позволяет вам выбрать дополнительные фильтры на внутренней странице `brave://adblock`. Мы не рекомендуем использовать эту функцию; вместо этого оставьте списки фильтров по умолчанию. Использование дополнительных фильтров выделит вас среди других пользователей Brave, а также может увеличить площадь атаки, если в Brave есть эксплойт и вредоносное правило будет добавлено в один из используемых вами списков.

- [x] (Опционально) Выберите **Блокировать скрипты** (1)
- [x] Выберите **Строгий, может нарушать работу вебсайтов** в разделе: Блокировка цифровых отпечатков

</div>

1. Эта опция обеспечивает функциональность, аналогичную расширенным [режимам блокировки](https://github.com/gorhill/uBlock/wiki/Blocking-mode) uBlock Origin или расширения [NoScript](https://noscript.net/).

##### Блокировка социальных сетей

- [ ] Отключите все переключатели в этой секции

##### Конфиденциальность и безопасность

<div class="annotate" markdown>

- [x] Выберите **Отключить непроксируемый протокол UDP** в секции: [Политика обработки IP WebRTC](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Отключите **Использовать сервисы Google для обмена push-сообщениями**
- [ ] Отключите **Разрешить выполнение аналитики продукта, не нарушающей конфиденциальности**
- [ ] Отключите **Автоматически отправлять ежедневные данные PING в Brave**
- [ ] Отключите **Автоматически отправлять данные диагностики**
- [x] Выберите **Всегда использовать безопасные соединения** в подразделе **Безопасность**
- [ ] Отключите **Приватное окно с Tor** (1)

    !!! совет "Отчистка при закрытии"

        - [x] Выберите **Удалять файлы cookie и данные сайтов при закрытии всех окон** в подразделе *Файлы cookie и другие данные сайтов*

        Если вы хотите оставать залогинеными на сайтах, которые вы часто посещаете, вы можете установить исключения в разделе: Специальные настройки.

</div>

1. Brave **не так устойчив** к цифровым отпечаткам, как Tor Browser, и гораздо меньше людей используют Brave вместе с Tor, поэтому вы будете выделяться. Там, где [требуется сильная анонимность](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-) используйте [Tor Browser](tor.md#tor-browser).

##### Расширения

Отключите встроенные расширения, которые вы не используете, в разделе **Расширения**

- [ ] Отключите **Hangouts**
- [ ] Отключите **WebTorrent**

##### Web3

Функции Web3 в Brave потенциально могут увеличить цифровой отпечаток вашего браузера и площадь атаки. Если ты не используешь эти функции, их следует отключить.

- [ ] Set **Default Ethereum Wallet** to **None**
- [ ] Set **Default Solana Wallet** to **None**
- [ ] В **Метод преобразования IPFS-ресурсов** выбери **Отключено**

##### Система

<div class="annotate" markdown>

- [ ] Отключи **Продолжить выполнение фоновых приложений после закрытия Brave**, чтобы отключить фоновые приложения (1)

</div>

1. Эта опция присутствует не на всех платформах.

#### Синхронизация

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) позволяет синхронизировать данные браузера (историю, закладки и т. д.) между несколькими устройствами без необходимости создавать аккаунт, а также защищает их при помощи E2EE.

#### Вознаграждение Brave и Кошелек

**Вознаграждения Brave** позволяет получать криптовалюту Basic Attention Token (BAT) за выполнение определенных действий в Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#other-coins-bitcoin-ethereum-etc), so we would discourage using this feature.

**Кошелек Brave** работает локально на вашем компьютере, но не поддерживает никаких конфиденциальных криптовалют, поэтому мы бы не советовали использовать и эту функцию.

## Дополнительные ресурсы

Обычно, мы рекомендуем использовать как можно меньше расширений, чтобы уменьшить площадь атаки; они имеют привилегированный доступ к твоему браузеру, требуют доверия к их разработчикам, могут [идентифицировать вас](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), а также [ослабляют](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) изоляцию между сайтами. Однако uBlock Origin может оказаться полезным, если вам важна функциональность блокировки контента.

### uBlock Origin

!!! recommendation

    ![Логотип uBlock Origin](assets/img/browsers/ublock_origin.svg){ align=right }
    
    **uBlock Origin** это популярный блокировщик контента, который может помочь тебе блокировать рекламу, трекеры и скрипты цифровых отпечатков.
    
    [:octicons-repo-16: Репозиторий](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Исходный код" }
    
    ??? downloads
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

We suggest following the [developer's documentation](https://github.com/gorhill/uBlock/wiki/Blocking-mode) and picking one of the "modes". Additional filter lists can impact performance and [may increase attack surface](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

##### Other lists

These are some other [filter lists](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) that you may want to consider adding:

- [x] Check **Privacy** > **AdGuard URL Tracking Protection**
- Add [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

## Критерии

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! пример "Эта секция новая"

    We are working on establishing defined criteria for every section of our site, and this may be subject to change. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. Мы учитываем и обсуждаем много факторов, перед тем как рекомендовать какой-то проект, и документирование каждого из них ещё не завершено.

### Минимальные требования к сервисам

- Должны иметь открытый исходный код.
- Должны поддерживать автоматические обновления.
- Должны получать обновления движка в течение 0-1 дня после релиза в upstream.
- Доступны для Linux, macOS и Windows.
- Любые изменения, необходимые для того, чтобы браузер больше соблюдал конфиденциальность, не должны негативно влиять на опыт использования.
- По умолчанию блокируют сторонние файлы cookie.
- Поддерживают [разделение состояний](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) для уменьшения межсайтового отслеживания.[^1]

### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Включает в себя встроенную функцию блокировки контента.
- Поддерживает разделение файлов cookie (как [Multi-Account Контейнеры](https://support.mozilla.org/en-US/kb/containers)).
- Supports Progressive Web Apps.  
  PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps, because you benefit from your browser's regular security updates.
- Does not include add-on functionality (bloatware) that does not impact user privacy.
- По умолчанию не собирает телеметрию.
- Предоставляет реализацию сервера синхронизации с открытым исходным кодом.
- По умолчанию включена [конфиденциальная поисковая система](search-engines.md).

### Критерии для расширений

- Не должны копировать встроенную функциональность браузера или ОС.
- Должны непосредственно влиять на конфиденциальность пользователя, т.е. не просто предоставлять информацию.

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state/).
