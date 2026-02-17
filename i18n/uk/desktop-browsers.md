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

**Without** using a [VPN](vpn.md), Mullvad Browser provides protections against [naive fingerprinting scripts](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) similar to other private browsers like Firefox+[Arkenfox](#arkenfox-advanced) or [Brave](#brave). Mullvad Browser надає ці засоби захисту "з коробки", шляхом певної гнучкості та зручності, які можуть забезпечити й інші приватні браузери.

==Для найсильнішого захисту від відбитків ми рекомендуємо використовувати Mullvad Browser у поєднанні **з** VPN, будь то Mullvad або інший рекомендований VPN-провайдер. Використовуючи VPN з Mullvad Browser, ви ділитеся відбитком браузера і пулом IP-адрес з багатьма іншими користувачами, створюючи "натовп", з яким можна змішатися. Ця стратегія - єдиний спосіб перешкодити просунутим скриптам стеження, і це той самий метод боротьби з відбитками, що використовується браузером Tor.

Note that while you can use Mullvad Browser with any VPN provider, other people on that VPN must also be using Mullvad Browser for this "crowd" to exist, something which is more likely on Mullvad VPN compared to other providers. Mullvad Browser не має вбудованого VPN-з'єднання, а також не перевіряє, чи використовуєте ви VPN перед переглядом вебсторінок; ваше VPN-з'єднання має бути налаштоване і кероване окремо.

Mullvad Browser постачається з попередньо встановленими розширеннями *uBlock Origin* та *NoScript*. Хоча ми зазвичай не рекомендуємо додавати *додаткові* [розширення браузера](browser-extensions.md), ці розширення, які постачаються з браузером, **не** слід видаляти або налаштовувати за межами значень за замовчуванням, оскільки це може помітно відрізнити ваш браузер від інших користувачів Mullvad Browser. Він також постачається з попередньо встановленим розширенням для браузера Mullvad, яке *можна* безпечно видалити, не впливаючи на відбитки у браузері, якщо ви бажаєте, але також безпечно зберігати, навіть якщо ви не використовуєте Mullvad VPN.

### Режим приватного перегляду

Браузер Mullvad працює в режимі постійного приватного перегляду, що означає, що ваша історія, файли cookie та інші дані сайту завжди будуть очищені при кожному закритті браузера. Ваші закладки, налаштування браузера та розширення будуть збережені.

Це необхідно для запобігання розширеним формам відстеження, але це відбувається за рахунок зручності та деяких функцій Firefox, таких як контейнери з декількома обліковими записами. Пам'ятайте, що ви завжди можете використовувати кілька браузерів, наприклад, ви можете використовувати Firefox+Arkenfox для кількох сайтів, на яких ви хочете залишатися в системі або які не працюють належним чином у Mullvad Browser, і Mullvad Browser для загального перегляду.

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

- [ ] Uncheck **Send technical and interaction data to Mozilla**
- [ ] Uncheck **Allow personalized extension recommendations**
- [ ] Uncheck **Install and run studies**
- [ ] Uncheck **Send daily usage ping to Mozilla**
- [ ] Uncheck **Automatically send crash reports**

Згідно з політикою конфіденційності Mozilla для Firefox,

> Firefox надсилає нам дані про версію та мову вашого браузера, операційну систему та конфігурацію обладнання, пам'ять, основну інформацію про збої та помилки, результати автоматизованих процесів, таких як оновлення, безпечний перегляд та активація. Коли Firefox надсилає нам дані, ваша IP-адреса тимчасово фіксується в журналах нашого сервера.

Крім того, сервіс Mozilla Accounts збирає [деякі технічні дані](https://mozilla.org/privacy/mozilla-accounts). Якщо ви використовуєте обліковий запис Mozilla, ви можете відмовитися:

1. Відкрийте [налаштування свого профілю на сторінці accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. [ ] Зніміть прапорець **Збір та використання даних** > **Допоможіть покращити облікові записи Firefox**

##### Налаштування реклами для вебсайтів

- [ ] Зніміть прапорець **Дозволити вебсайтам виконувати вимірювання реклами зі збереженням приватності**

З виходом Firefox 128 було додано новий параметр для [атрибуції зі збереженням конфіденційності](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA), який [увімкнено за замовчуванням](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA дозволяє рекламодавцям використовувати ваш веббраузер для вимірювання ефективності вебкампаній замість традиційного відстеження на основі JavaScript. Ми вважаємо, що така поведінка виходить за рамки обов'язків агента користувача, і той факт, що в Arkenfox вона вимкнена за замовчуванням, є додатковим індикатором для вимкнення цієї функції.

##### HTTPS-режим

- [x] Виберіть **Увімкнути HTTPS-режим у всіх вікнах**

Це запобігає ненавмисному з'єднанню з вебсайтом за допомогою звичайного HTTP. Сьогодні сайти без HTTPS зустрічаються рідко, тому це практично не вплине на ваш повсякденний перегляд вебсторінок.

##### DNS через HTTPS

Якщо ви використовуєте захист [DNS через HTTPS](dns.md):

- [x] Виберіть **Максимальний захист** і виберіть відповідного постачальника

Максимальний захист забезпечує використання DNS через HTTPS, і попередження про небезпеку з'явиться, якщо Firefox не може під'єднатися до вашого захищеного DNS-відповідача або якщо ваш захищений DNS-відповідач повідомляє, що записи для домену, до якого ви намагаєтеся отримати доступ, не існують. Це не дозволить мережі, до якої ви підключені, таємно знизити рівень безпеки вашого DNS.

#### Синхронізація

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) забезпечує доступ до даних браузера (історії, закладок тощо) на всіх ваших пристроях і захищає їх за допомогою E2EE.

### Arkenfox (просунутий рівень)

<div class="admonition tip" markdown>
<p class="admonition-title">Використовуйте Mullvad Browser для розширеного захисту від цифрових відбитків</p>

[Mullvad Browser](#mullvad-browser) provides stronger anti-fingerprinting protections out of the box than Firefox, and does not require the use of Mullvad's VPN to benefit from these protections. У поєднанні з VPN Mullvad Browser може перешкоджати більш просунутим скриптам стеження, чого не може зробити Arkenfox. Firefox still has the advantage of being much more flexible, and allowing per-site exceptions for websites which you need to stay logged in to.

</div>

[Проєкт Arkenfox](https://github.com/arkenfox/user.js) надає набір ретельно продуманих налаштувань для Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-%5BCommon%5D) are subjectively strict and/or may cause some websites to not work properly—which you can [easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. Ми **наполегливо рекомендуємо** прочитати їхню повну [вікі-сторінку](https://github.com/arkenfox/user.js/wiki). Arkenfox також забезпечує підтримку [контейнерів](https://support.mozilla.org/kb/containers#w_for-advanced-users).

Arkenfox має на меті лише перешкоджати базовим або простим скриптам відстеження за допомогою рандомізації вбудованих у Firefox налаштувань захисту від відбитків. Він не має на меті змусити ваш браузер злитися з великим натовпом інших користувачів Arkenfox так само, як це роблять Mullvad Browser або Tor Browser, що є єдиним способом перешкодити просунутим скриптам відстеження цифрових відбитків. Пам'ятайте, що ви завжди можете використовувати кілька браузерів, наприклад, ви можете використовувати Firefox+Arkenfox для кількох сайтів, на яких ви хочете залишатися в системі або яким ви довіряєте, і Mullvad Browser для загального перегляду.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){align=right}

**Браузер Brave** має вбудований блокувальник вмісту та [функції конфіденційності](https://brave.com/privacy-features), багато з яких увімкнено за замовчуванням.

Brave побудований на основі проєкту веббраузера Chromium, тому він має бути знайомим і мати мінімальні проблеми із сумісністю з вебсайтами.

[:octicons-home-16: Домашня сторінка ](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Політика конфіденційності" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Документація" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Вихідний код" }

<details class="downloads" markdown>
<summary>Завантаження</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Попередження</p>

Brave додає "[реферальний код](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" до імені файлу, завантаженого з веб-сайту Brave, який використовується для відстеження джерела, з якого було завантажено браузер, наприклад, "BRV002" у завантаженні з назвою "Brave-Browser-BRV002.pkg". Наприкінці процесу встановлення інсталятор пінгує сервер Brave за допомогою реферального коду. Якщо вас це турбує, ви можете перейменувати файл інсталятора перед тим, як відкрити його.

</div>

### Рекомендовані налаштування Brave

Параметри можна знайти на сторінці :material-menu: → **Налаштування**.

#### Щити

Brave включає деякі заходи проти відбитків у функції ["Щити](https://support.brave.com/hc/articles/360022973471-What-is-Shields) ". Ми рекомендуємо налаштувати ці параметри [глобально](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) для всіх сторінок, які ви відвідуєте.

Параметри екранів можуть бути зменшені для кожного сайту за необхідності, але за замовчуванням ми рекомендуємо встановити такі значення:

<div class="annotate" markdown>

- [x] Виберіть **Агресивно** у розділі *Блокування стеження та реклами*

<details class="warning" markdown>
<summary>Використовуйте списки фільтрів за замовчуванням</summary>

Brave дозволяє вибрати додаткові фільтри вмісту на внутрішній сторінці "brave://adblock". Ми не радимо використовувати цю функцію; натомість збережіть списки фільтрів за замовчуванням. Використання додаткових списків виділить вас серед інших користувачів Brave, а також може збільшити кількість атак, якщо в Brave є експлойт і шкідливе правило буде додано до одного зі списків, які ви використовуєте.

</details>

- [x] Виберіть **Обов'язково** у розділі *Оновлювати з’єднання до HTTPS*
- [x] (необов'язково) Виберіть **Блокувати скрипти** (1)
- [x] Установіть прапорець **Блокувати зчитування цифрового відбитка**
- [x] Виберіть **Блокувати сторонні** у *Блокувати файли cookie*
- [x] Установіть прапорець **Забути мене, коли я закрию цей сайт** (2)
- [x] Зніміть прапорець у всіх компонентах соціальних мереж

</div>

1. Ця опція вимикає JavaScript, що призведе до поломки багатьох сайтів. Щоб виправити їх, ви можете встановити винятки для кожного сайту окремо, натиснувши на іконку Щит в адресному рядку і знявши галочку з цього параметра в розділі *Розширені налаштування*.
2. Якщо ви хочете залишатися в системі на певному сайті, який ви часто відвідуєте, ви можете встановити винятки для кожного сайту, натиснувши на іконку Щит в адресному рядку і знявши прапорець з цього параметра в розділі *Розширені налаштування*.

#### Конфіденційність і безпека

<div class="annotate" markdown>

- [x] Select **Don’t allow sites to use JavaScript optimization** under *Security* → *Manage JavaScript optimization & security* (1)
- [x] Select **Automatically remove permissions from unused sites** under *Sites and Shields Settings*
- [x] Select **Disable non-proxied UDP** under [*WebRTC IP Handling Policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **Prevent sites from fingerprinting me based on my language preferences**

</div>

1. Вимкнення оптимізатора V8 зменшує поверхню атаки шляхом вимкнення [*деяких*](https://grapheneos.social/@GrapheneOS/112708049232710156) частин компіляції JavaScript Just-In-Time (JIT).

##### Вікна Tor

[**Приватне вікно з Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) дозволяє маршрутизувати ваш трафік через мережу Tor у приватному вікні та отримувати доступ до сервісів .onion, що може бути корисно в деяких випадках. Однак Brave **не** настільки стійкий до цифрових відбитків, як Tor Browser, і набагато менше людей використовують Brave з Tor, тому ви будете виділятися. Якщо ваша модель загроз вимагає суворої анонімності, використовуйте [Tor браузер](tor.md#tor-browser).

##### Збір даних

- [ ] Зніміть прапорець **Дозволити аналітику продуктів зі збереженням конфіденційності (P3A)**
- [ ] Зніміть прапорець **Автоматично надсилати щоденний сигнал використання Brave**
- [ ] Зніміть прапорець **Автоматично надсилати діагностичні звіти**

#### Web3

Функції Web3 у Brave потенційно можуть додати до вашого браузера цифрові відбитки та поверхню атаки. Якщо ви не використовуєте жодної з цих функцій, їх слід вимкнути.

- Виберіть **Розширення (без резервного)** у розділі *Типовий гаманець Ethereum*
- Виберіть **Розширення (без резервного)** у розділі *Типовий гаманець Solana*

#### Розширення

- [ ] Зніміть позначку з усіх вбудованих розширень, які ви не використовуєте

#### Пошукова система

Ми рекомендуємо вимкнути пошукові підказки у Brave з тієї ж причини, з якої ми рекомендуємо вимкнути цю функцію у [Firefox](#search).

- [ ] Зніміть прапорець **Оптимізувати підказки пошуку**

#### Система

<div class="annotate" markdown>

- [ ] Зніміть прапорець **Продовжувати роботу фонових програм, коли Brave закрито**, щоб вимкнути фонові програми (1)

</div>

1. Ця опція присутня не на всіх платформах.

#### Синхронізація

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) забезпечує доступ до ваших даних браузера (історії, закладок тощо) на всіх пристроях без необхідності створення облікового запису та захищає їх за допомогою E2EE.

#### Brave Винагороди та Гаманець

**Brave Rewards** дозволяє вам отримувати криптовалюту Basic Attention Token (BAT) за виконання певних дій у Brave. Він спирається на депозитарний рахунок і KYC від обраної кількості провайдерів. Ми не рекомендуємо BAT як [приватну криптовалюту](cryptocurrency.md), а також не рекомендуємо використовувати [гаманець](advanced/payments.md#wallet-custody) для зберігання, тому ми б не рекомендували використовувати цю функцію.

**Brave Wallet** працює локально на вашому комп'ютері, але не підтримує жодних приватних криптовалют, тому ми не рекомендуємо використовувати цю функцію.

## Критерії

**Зверніть увагу, що ми не пов'язані з жодним з проєктів, які ми рекомендуємо.** На додачу до [наших стандартних критеріїв](about/criteria.md), ми розробили чіткий набір вимог, які дозволяють нам надавати об'єктивні рекомендації. Ми пропонуємо вам ознайомитися з цим списком перед тим, як вибрати проєкт, і провести власне дослідження, щоб переконатися, що це правильний вибір для вас.

### Мінімальні вимоги

- Це має бути програмне забезпечення з відкритим вихідним кодом.
- Має підтримувати автоматичне оновлення.
- Повинні отримувати оновлення рушія протягом 0-1 дня з моменту випуску.
- Має бути доступним на Linux, macOS та Windows.
- Будь-які зміни, необхідні для того, щоб зробити браузер більш безпечним для конфіденційності, не повинні негативно впливати на роботу користувачів.
- Має блокувати сторонні файли cookie за замовчуванням.
- Повинен підтримувати [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) для зменшення міжсайтового відстеження.[^1]

### Найкращі практики

Наші найкращі критерії втілюють те, що ми хотіли б бачити від ідеального проєкту в цій категорії. Наші рекомендації можуть не включати всі або деякі з цих функцій, але ті, що включають, можуть мати вищий рейтинг, ніж інші на цій сторінці.

- Повинен мати вбудовану функцію блокування контенту.
- Має підтримувати розділення файлів cookie (а-ля [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Повинні підтримувати прогресивні вебдодатки (PWA). PWA дозволяють встановлювати певні вебсайти так, ніби вони є звичайними програмами на вашому комп'ютері. Це може мати переваги над встановленням додатків на базі Electron, оскільки PWA отримують регулярні оновлення безпеки вашого браузера.
- Не повинен включати додатковий функціонал (bloatware), який не впливає на конфіденційність користувача.
- Не повинен збирати телеметрію за замовчуванням.
- Повинен надавати реалізацію сервера синхронізації з відкритим вихідним кодом.
- За замовчуванням має бути [приватна пошукова система](search-engines.md).

[^1]: Реалізація Brave детально описана в [Оновлення конфіденційності Brave: Розділення мережевого стану для забезпечення конфіденційності](https://brave.com/privacy-updates/14-partitioning-network-state).
