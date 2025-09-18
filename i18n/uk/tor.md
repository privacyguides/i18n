---
meta_title: "Tor браузер і мережа: Анонімний перегляд вебсторінок"
title: "Tor Browser"
icon: simple/torbrowser
description: Захистіть свій інтернет-серфінг від сторонніх очей, використовуючи мережу Tor - безпечну мережу, яка обходить цензуру.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
    sameAs: https://uk.wikipedia.org/wiki/Tor
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
    subjectOf:
      "@type": Вебсторінка
      url: "./"
---

<small>Захищає від наступних загроз:</small>

- [:material-account-cash: Капіталізм нагляду](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: Масове стеження](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Цензура](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

**Tor** - це група серверів, керованих волонтерами, яка дозволяє вам підключатися безплатно і покращувати вашу конфіденційність і безпеку в Інтернеті. Приватні особи та організації також можуть обмінюватися інформацією через мережу Tor з "прихованими сервісами .onion" без шкоди для своєї конфіденційності. Оскільки трафік Tor важко заблокувати і відстежити, Tor є ефективним інструментом обходу цензури.

[Детальний огляд Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: Відео: Навіщо вам потрібен Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Порада</p>

Перед підключенням до Tor, будь ласка, переконайтеся, що ви прочитали наш [огляд] (advanced/tor-overview.md) про те, що таке Tor і як безпечно до нього підключатися. Ми часто рекомендуємо підключатися до Tor через надійного [VPN-провайдера] (vpn.md), але ви повинні робити це **правильно**, щоб уникнути зниження вашої анонімності.

</div>

Існує безліч способів під'єднатися до мережі Tor з вашого пристрою, найчастіше використовується **Tor Browser**, форк Firefox, призначений для [:material-incognito: анонімного](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} перегляду для настільних комп'ютерів і Android.

Деякі з цих програм кращі за інші; вибір залежить від вашої моделі загроз. Якщо ви звичайний користувач Tor, який не турбується про те, що ваш провайдер збирає докази проти вас, використання додатків для мобільних браузерів, таких як [Onion Browser](#onion-browser-ios), для доступу до мережі Tor, ймовірно, є нормальним рішенням. Збільшення кількості людей, які користуються Tor на щоденній основі, допомагає зменшити негативну стигматизацію Tor і знижує якість "списків користувачів Tor", які можуть складати провайдери та уряди.

Якщо повна анонімність є першочерговою у вашій ситуації, вам слід використовувати **лише** десктопний клієнт Tor Browser, в ідеалі - в поєднанні [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os). Мобільні браузери менш поширені в Tor (і, як наслідок, більш схильні до цифрових відбитків), а інші конфігурації не проходять настільки сувору перевірку на деанонімізацію.

## Браузер Tor

<div class="admonition recommendation" markdown>

![Логотип Tor Browser](assets/img/browsers/tor.svg){align=right}

**Tor Browser** це оптимальний вибір, якщо вам потрібна анонімність, оскільки він надає доступ до мережі Tor і мостів, а також включає в себе стандартні налаштування і розширення, які автоматично налаштовуються на рівні безпеки за замовчуванням: *Стандартний*, *Безпечніший* і *Найбезпечніший*.

[:octicons-home-16: Домашня сторінка ](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title="Документація" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Вихідний код" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Завантаження</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:fontawesome-brands-windows: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Небезпека</p>

Ви **ніколи** не повинні встановлювати додаткові розширення для браузера Tor або змінювати налаштування "about:config", включаючи ті, які ми рекомендуємо для Firefox. Розширення браузера і нестандартні налаштування виділяють вас серед інших користувачів мережі Tor, тим самим полегшуючи доступ до [відбитків] (https://support.torproject.org/glossary/browser-fingerprinting).

</div>

Браузер Tor розроблений таким чином, щоб запобігти зняттю відбитків або ідентифікації вас на основі конфігурації вашого браузера. Тому вкрай важливо, щоб ви **не** змінювали браузер за межами стандартних [рівнів безпеки](https://tb-manual.torproject.org/security-settings). Змінюючи налаштування рівня безпеки, ви завжди **повинні** перезапустити браузер, перш ніж продовжувати користуватися ним. В іншому випадку [налаштування безпеки можуть бути застосовані не в повному обсязі](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), що призведе до більшого ризику зняття відбитків та їх використання зловмисниками, ніж ви можете очікувати, виходячи з обраних налаштувань.

Окрім встановлення Tor Browser безпосередньо на ваш комп'ютер, існують також операційні системи, розроблені спеціально для підключення до мережі Tor, такі як [Whonix](desktop.md#whonix) на [Qubes OS](desktop.md#qubes-os), які забезпечують ще більшу безпеку і захист, ніж стандартний Tor Browser.

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){align=right}

**Onion Browser** - це браузер з відкритим вихідним кодом, який дозволяє анонімно переглядати вебсторінки через мережу Tor на пристроях iOS і схвалений [Tor Project](https://support.torproject.org/glossary/onion-browser).

[:material-star-box: Читайте наш останній огляд Onion Browser.](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review)

[:octicons-home-16: Домашня сторінка](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Політика конфіденційності" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title="Документація" }
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Вихідний код" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Завантаження</summary>

- [:simple-appstore: App Store] (https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser не забезпечує такого ж рівня захисту конфіденційності, як Tor Browser на десктопних платформах. Для повсякденного використання це чудовий спосіб отримати доступ до прихованих сервісів, але якщо ви боїтеся, що вас можуть відстежити або відстежувати просунуті зловмисники, не варто покладатися на нього як на інструмент анонімності.

Слід [зазначити](https://github.com/privacyguides/privacyguides.org/issues/2929), що Onion Browser не *гарантує*, що всі запити проходять через Tor. При використанні вбудованої версії Tor [ваш реальний IP **буде** витікати через WebRTC і аудіо/відео потоки](https://onionbrowser.com/faqs) через обмеження WebKit. *Безпечніше* використовувати Onion Browser разом з [Orbot](alternative-networks.md#orbot), але це все ще має деякі обмеження на iOS.
