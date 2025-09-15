---
meta_title: "Веббраузери, які поважають конфіденційність, для ПК та Mac - Посібники з конфіденційності"
title: Настільні браузери
icon: material/laptop
description: Ці браузери, що захищають конфіденційність, ми наразі рекомендуємо для стандартного/неанонімного перегляду вебсторінок на настільних комп'ютерах.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Рекомендації щодо приватних браузерів
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/en/browser
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
    sameAs: https://uk.wikipedia.org/wiki/Firefox
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
    sameAs: https://uk.wikipedia.org/wiki/Brave_(браузер)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Захищає від наступних загроз:</small>

- [:material-account-cash: Капіталізм нагляду](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Це наші поточні рекомендовані **веббраузери для ПК** та конфігурації для стандартного/неанонімного перегляду. Ми рекомендуємо [Mullvad Browser](#mullvad-browser), якщо вам потрібен надійний захист конфіденційності та захист від цифрових відбитків "з коробки", [Firefox](#firefox) браузер для повсякденних потреб і хорошу альтернативу Google Chrome, і [Brave](#brave), якщо вам потрібна сумісність з браузером Chromium.

Якщо вам потрібно переглядати інтернет анонімно, використовуйте [Tor](tor.md). На цій сторінці ми надаємо деякі рекомендації щодо налаштування, але всі браузери, окрім Tor Browser, так чи інакше будуть відстежуватися *кимось*.

## Браузер Mullvad

<div class="admonition recommendation" markdown>

![Логотип Mullvad Browser](assets/img/browsers/mullvad_browser.svg){align=right}

**Mullvad Browser** - це версія [Tor Browser](tor.md#tor-browser) з вилученою інтеграцією з мережею Tor. Він має на меті надати користувачам VPN засоби Tor Browser проти цифрових відбитків, які є ключовим захистом від [:material-eye-outline: масового стеження] (basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. Він розроблений проєктом Tor і розповсюджується [Mullvad] (vpn.md#mullvad), і **не** вимагає використання VPN від Mullvad.

[:octicons-home-16: Домашня сторінка ](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Політика конфіденційності" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="Документація" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Вихідний код" }

<details class="downloads" markdown>
<summary>Завантаження</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Як і [Tor Browser](tor.md), Mullvad Browser розроблений для запобігання зняття цифрових відбитків, роблячи ваш відбиток ідентичним з відбитками всіх інших користувачів Mullvad Browser, і включає в себе налаштування за замовчуванням і розширення, які автоматично налаштовуються на рівні безпеки за замовчуванням: *Стандартний*, *Безпечний* та *Найбезпечніший*.

Тому вкрай важливо, щоб ви взагалі не змінювали браузер, окрім налаштування [рівнів безпеки](https://tb-manual.torproject.org/security-settings) за замовчуванням. При зміні рівня безпеки завжди **потрібно** перезапускати браузер, перш ніж продовжувати користуватися ним. В іншому випадку [налаштування безпеки можуть бути застосовані не в повному обсязі](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), що призведе до більшого ризику зняття відбитків та їх використання зловмисниками, ніж ви можете очікувати, виходячи з обраних налаштувань.

Будь-які зміни, окрім зміни цього параметра, зроблять ваш відбиток унікальним, що суперечить меті використання цього браузера. Якщо ви хочете налаштувати свій браузер більш детально, а відбитки браузера вас не турбують, ми рекомендуємо [Firefox](#firefox).

### Протидія відбиткам браузера

**Без** використання [VPN](vpn.md) Mullvad Browser забезпечує такий самий захист від [базових скриптів зняття відбитків браузера](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting), як і інші приватні браузери, такі як Firefox+[Arkenfox](#arkenfox-advanced) або [Brave](#brave). Mullvad Browser надає ці засоби захисту "з коробки", шляхом певної гнучкості та зручності, які можуть забезпечити й інші приватні браузери.

==Для найсильнішого захисту від відбитків ми рекомендуємо використовувати Mullvad Browser у поєднанні **з** VPN, будь то Mullvad або інший рекомендований VPN-провайдер. Використовуючи VPN з Mullvad Browser, ви ділитеся відбитком браузера і пулом IP-адрес з багатьма іншими користувачами, створюючи "натовп", з яким можна змішатися. Ця стратегія - єдиний спосіб перешкодити просунутим скриптам стеження, і це той самий метод боротьби з відбитками, що використовується браузером Tor.

Зауважте, що хоча ви можете використовувати Mullvad браузер з будь-яким VPN-провайдером, інші користувачі цього VPN також повинні використовувати Mullvad браузер, щоб існував цей "натовп", що є більш імовірним для Mullvad VPN порівняно з іншими провайдерами, особливо в цей час, коли Mullvad браузер тільки-но запущено. Mullvad Browser не має вбудованого VPN-з'єднання, а також не перевіряє, чи використовуєте ви VPN перед переглядом вебсторінок; ваше VPN-з'єднання має бути налаштоване і кероване окремо.

Mullvad Browser постачається з попередньо встановленими розширеннями *uBlock Origin* та *NoScript*. Хоча ми зазвичай не рекомендуємо додавати *додаткові* [розширення браузера](browser-extensions.md), ці розширення, які постачаються з браузером, **не** слід видаляти або налаштовувати за межами значень за замовчуванням, оскільки це може помітно відрізнити ваш браузер від інших користувачів Mullvad Browser. Він також постачається з попередньо встановленим розширенням для браузера Mullvad, яке *можна* безпечно видалити, не впливаючи на відбитки у браузері, якщо ви бажаєте, але також безпечно зберігати, навіть якщо ви не використовуєте Mullvad VPN.

### Режим приватного перегляду

Браузер Mullvad працює в режимі постійного приватного перегляду, що означає, що ваша історія, файли cookie та інші дані сайту завжди будуть очищені при кожному закритті браузера. Ваші закладки, налаштування браузера та розширення будуть збережені.

Це необхідно для запобігання розширеним формам відстеження, але це відбувається за рахунок зручності та деяких функцій Firefox, таких як контейнери з декількома обліковими записами. Пам'ятайте, що ви завжди можете використовувати кілька браузерів, наприклад, ви можете використовувати Firefox+Arkenfox для кількох сайтів, на яких ви хочете залишатися в системі або які не працюють належним чином у Mullvad Browser, і Mullvad Browser для загального перегляду.

### Mullvad Leta

Mullvad Browser поставляється з [**Mullvad Leta**](search-engines.md#mullvad-leta) як пошуковою системою за замовчуванням, яка функціонує як проксі для результатів пошуку Google або Brave (налаштовується на домашній сторінці Mullvad Leta).

Якщо ви користуєтеся Mullvad VPN, існує певний ризик у використанні таких сервісів, як Mullvad Leta, які пропонуються вашим провайдером VPN. Це пов'язано з тим, що Mullvad теоретично має доступ до вашої справжньої IP-адреси (через свою VPN) та вашої пошукової активності (через Leta), яка може бути тією, яку VPN має приховувати. Попри те, що Mullvad збирає дуже мало інформації про своїх VPN-підписників або користувачів Leta, вам слід розглянути можливість використання іншої [пошукової системи](search-engines.md), якщо цей ризик вас турбує.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox logo](assets/img/browsers/firefox.svg){align=right}

**Firefox** надає сильні налаштування конфіденційності, такі як [Покращений захист від відстеження](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), які можуть допомогти заблокувати різні [типи відстеження](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).

[:octicons-home-16: Домашня сторінка ](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Політика конфіденційності" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="Документація" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Вихідний код" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Завантаження</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Попередження</p>

Firefox включає унікальний [маркер завантаження] (https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) у завантаження з вебсайту Mozilla і використовує телеметрію у Firefox для надсилання маркера. Токен **не включено** до релізів з [Mozilla FTP] (https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Рекомендовані налаштування Firefox

Параметри можна знайти на сторінці :material-menu: → **Налаштування**.

#### Пошук

- [ ] Зніміть прапорець **Показувати пошукові пропозиції**

Функція підказок пошуку може бути недоступна у вашому регіоні.

Пошукові пропозиції надсилають усе, що ви вводите в адресному рядку, до пошукової системи за замовчуванням, незалежно від того, чи вводите ви реальний запит. Вимкнення пошукових пропозицій дозволяє точніше контролювати дані які дані ви відправляєте в пошукову систему.

##### Пропозиції Firefox (лише США)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) - це функція, схожа на пошукові пропозиції, яка доступна лише в США. Ми рекомендуємо вимкнути її з тієї ж причини, з якої ми рекомендуємо вимкнути пошукові пропозиції. Якщо ви не бачите цих опцій під заголовком **адресного рядка**, ви не маєте нового досвіду і можете проігнорувати ці зміни.

- [ ] Зніміть прапорець **Пропозиції від Firefox**
- [ ] Зніміть прапорець **Пропозиції від спонсорів**

#### Приватність і Безпека

##### Розширений захист від стеження

- [x] Виберіть **Надійний** захист від стеження

Це захищає вас, блокуючи трекери соціальних мереж, скрипти цифрових відбитків (зверніть увагу, що це не захищає вас від *усіх* видів відбитків), криптомайнери, файли cookie для міжсайтового відстеження та деякий інший вміст для відстеження. "Надійний" захищає від багатьох поширених загроз, але не блокує всі шляхи відстеження, оскільки він розроблений таким чином, щоб мати мінімальний або нульовий вплив на зручність використання сайту.

##### Дезінфікувати при закритті

Якщо ви хочете залишатися в системі на певних сайтах, ви можете дозволити винятки в розділі **"Файли cookie та дані сайтів"** → **"Керувати винятками"...**

- [x] Позначити **Видаляти файли cookie та дані сайтів під час закриття Firefox**

Це захищає вас від постійних файлів cookie, але не захищає від файлів cookie, отриманих під час одного сеансу перегляду. Якщо цю опцію увімкнено, стає можливим легко очистити файли cookie вашого браузера, просто перезапустивши Firefox. Ви можете встановити винятки для кожного сайту, якщо ви хочете залишатися в системі на певному сайті, який ви часто відвідуєте.

##### Телеметрія

- [ ] Зніміть прапорець **Надсилати технічні й аналітичні дані до Mozilla**
- [ ] Зніміть прапорець **Встановлювати й запускати дослідження**
- [ ] Зніміть прапорець **Автоматично надсилати звіти про збої**

Згідно з політикою конфіденційності Mozilla для Firefox,

> Firefox надсилає нам дані про версію та мову вашого браузера, операційну систему та конфігурацію обладнання, пам'ять, основну інформацію про збої та помилки, результати автоматизованих процесів, таких як оновлення, безпечний перегляд та активація. Коли Firefox надсилає нам дані, ваша IP-адреса тимчасово фіксується в журналах нашого сервера.

Крім того, сервіс Mozilla Accounts збирає [деякі технічні дані](https://mozilla.org/privacy/mozilla-accounts). Якщо ви використовуєте обліковий запис Mozilla, ви можете відмовитися:

1. Open your [profile settings on accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Uncheck **Data Collection and Use** > **Help improve Firefox Accounts**

##### Website Advertising Preferences

- [ ] Uncheck **Allow websites to perform privacy-preserving ad measurement**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.

##### HTTPS-Only Mode

- [x] Select **Enable HTTPS-Only Mode in all windows**

This prevents you from unintentionally connecting to a website in plain-text HTTP. Sites without HTTPS are uncommon nowadays, so this should have little to no impact on your day-to-day browsing.

##### DNS через HTTPS (DNS over HTTPS)

If you use a [DNS over HTTPS provider](dns.md):

- [x] Select **Max Protection** and choose a suitable provider

Max Protection enforces the use of DNS over HTTPS, and a security warning will show if Firefox can’t connect to your secure DNS resolver, or if your secure DNS resolver says that records for the domain you are trying to access do not exist. This stops the network you're connected to from secretly downgrading your DNS security.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (advanced)

<div class="admonition tip" markdown>
<p class="admonition-title">Use Mullvad Browser for advanced anti-fingerprinting</p>

[Mullvad Browser](#mullvad-browser) provides the same anti-fingerprinting protections as Arkenfox out of the box, and does not require the use of Mullvad's VPN to benefit from these protections. Coupled with a VPN, Mullvad Browser can thwart more advanced tracking scripts which Arkenfox cannot. Arkenfox still has the advantage of being much more flexible, and allowing per-site exceptions for websites which you need to stay logged in to.

</div>

The [Arkenfox project](https://github.com/arkenfox/user.js) provides a set of carefully considered options for Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly—which you can [easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. We **strongly recommend** reading through their full [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember that you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave is built upon the Chromium web browser project, so it should feel familiar and have minimal website compatibility issues.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Documentation" }
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
<p class="admonition-title">Warning</p>

Brave adds a "[referral code](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" to the file name in downloads from the Brave website, which is used to track which source the browser was downloaded from, for example `BRV002` in a download named `Brave-Browser-BRV002.pkg`. The installer will then ping Brave's server with the referral code at the end of the installation process. If you're concerned about this, you can rename the installer file before opening it.

</div>

### Recommended Brave Configuration

Параметри можна знайти на сторінці :material-menu: → **Налаштування**.

#### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

Shields' options can be downgraded on a per-site basis as needed, but by default we recommend setting the following:

<div class="annotate" markdown>

- [x] Select **Aggressive** under *Trackers & ads blocking*

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. We advise against using this feature; instead, keep the default filter lists. Using extra lists will make you stand out from other Brave users and may also increase attack surface if there is an exploit in Brave and a malicious rule is added to one of the lists you use.

</details>

- [x] Select **Strict** under *Upgrade connections to HTTPS*
- [x] (Optional) Select **Block Scripts** (1)
- [x] Check **Block fingerprinting**
- [x] Select **Block third-party cookies**
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option disables JavaScript, which will break a lot of sites. To fix them, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.
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

##### Tor windows

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) allows you to route your traffic through the Tor network in Private Windows and access .onion services, which may be useful in some cases. However, Brave is **not** as resistant to fingerprinting as the Tor Browser is, and far fewer people use Brave with Tor, so you will stand out. If your threat model requires strong anonymity, use the [Tor Browser](tor.md#tor-browser).

##### Data Collection

- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**

#### Web3

Brave's Web3 features can potentially add to your browser fingerprint and attack surface. Unless you use any of these features, they should be disabled.

- Select **Extensions (no fallback)** under *Default Ethereum wallet*
- Select **Extensions (no fallback)** under *Default Solana wallet*

#### Extensions

- [ ] Uncheck all built-in extensions you don't use

#### Search engine

We recommend disabling search suggestions in Brave for the same reason we recommend disabling this feature in [Firefox](#search).

- [ ] Зніміть прапорець **Показувати пошукові пропозиції**

#### System

<div class="annotate" markdown>

- [ ] Uncheck **Continue running background apps when Brave is closed** to disable background apps (1)

</div>

1. This option is not present on all platforms.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

### Minimum Requirements

- Must be open-source software.
- Must support automatic updates.
- Must receive engine updates in 0-1 days from upstream release.
- Must be available on Linux, macOS, and Windows.
- Any changes required to make the browser more privacy-respecting must not negatively impact user experience.
- Must block third-party cookies by default.
- Must support [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### Best-Case

Our best-case criteria represents what we would like to see from the perfect project in this category. Our recommendations may not include any or all of this functionality, but those which do may rank higher than others on this page.

- Should include built-in content blocking functionality.
- Should support cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Should support Progressive Web Apps (PWAs). PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps because PWAs benefit from your browser's regular security updates.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Should not collect telemetry by default.
- Should provide an open-source sync server implementation.
- Should default to a [private search engine](search-engines.md).

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
