---
meta_title: "Tor Browser and Network: Anonymous Web Browsing - Privacy Guides"
title: "Tor Network"
icon: simple/torproject
description: Protect your internet browsing from prying eyes by using the Tor network, a secure network which circumvents censorship.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
    sameAs: https://en.wikipedia.org/wiki/Tor_(network)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
---

![Логотип Tor](assets/img/self-contained-networks/tor.svg){ align=right }

Мережа **Tor** - це група серверів, керованих волонтерами, яка дозволяє вам підключатися безкоштовно і покращувати вашу конфіденційність і безпеку в Інтернеті. Приватні особи та організації також можуть обмінюватися інформацією через мережу Tor з "прихованими сервісами .onion" без шкоди для своєї конфіденційності. Оскільки трафік Tor важко заблокувати і відстежити, Tor є ефективним інструментом обходу цензури.

[:octicons-home-16:](https://torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

Tor працює, спрямовуючи ваш інтернет-трафік через ці волонтерські сервери, замість того, щоб встановлювати пряме з'єднання з сайтом, який ви намагаєтесь відвідати. Це приховує, звідки надходить трафік, і жоден сервер у шляху з 'єднання не може побачити повний шлях, звідки надходить трафік, а це означає, що навіть сервери, які ви використовуєте для з' єднання, не можуть порушити вашу анонімність.

[Детальний огляд Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Підключення до Tor

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Before connecting to Tor, please ensure you've read our [overview](advanced/tor-overview.md) on what Tor is and how to connect to it safely. We often recommend connecting to Tor through a trusted [VPN provider](vpn.md), but you have to do so **properly** to avoid decreasing your anonymity.

</div>

Існує безліч способів під'єднатися до мережі Tor з вашого пристрою, найпоширенішим з яких є **Tor Browser**, форк Firefox, призначений для анонімного перегляду веб-сторінок на настільних комп'ютерах і Android.

Some of these apps are better than others, and again making a determination comes down to your threat model. If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using apps like [Orbot](#orbot) or mobile browser apps to access the Tor network is probably fine. Increasing the number of people who use Tor on an everyday basis helps reduce the bad stigma of Tor, and lowers the quality of "lists of Tor users" that ISPs and governments may compile.

If more complete anonymity is paramount to your situation, you should **only** be using the desktop Tor Browser client, ideally in a [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os) configuration. Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

### Tor Browser

<div class="admonition recommendation" markdown>

![Логотип Tor Browser](assets/img/browsers/tor.svg){ align=right }

**Tor Browser** — це вибір, якщо вам потрібна анонімність, оскільки він надає доступ до мережі Tor і мостів, а також включає в себе стандартні налаштування і розширення, які автоматично налаштовуються на рівні безпеки за замовчуванням: *Стандартний*, *Безпечніший* і *Найбезпечніший*.

[:octicons-home-16: Homepage](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:simple-windows11: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Ви **ніколи** не повинні встановлювати додаткові розширення для браузера Tor або змінювати налаштування `about:config`, включаючи ті, які ми рекомендуємо для Firefox. Розширення браузера і нестандартні налаштування виділяють вас серед інших користувачів мережі Tor, тим самим полегшуючи доступ до [fingerprint](https://support.torproject.org/glossary/browser-fingerprinting).

</div>

Браузер Tor розроблений таким чином, щоб запобігти зняттю відбитків або ідентифікації вас на основі конфігурації вашого браузера. Therefore, it is imperative that you do **not** modify the browser beyond the default [security levels](https://tb-manual.torproject.org/security-settings).

In addition to installing Tor Browser on your computer directly, there are also operating systems designed specifically to connect to the Tor network such as [Whonix](desktop.md#whonix) on [Qubes OS](desktop.md#qubes-os), which provide even greater security and protections than the standard Tor Browser alone.

### Orbot

<div class="admonition recommendation" markdown>

![Логотип Orbot](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** — це безкоштовна Tor VPN для смартфонів, яка спрямовує трафік від будь-якої програми на вашому пристрої через мережу Tor.

[:octicons-home-16: Homepage](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

</details>

</div>

We previously recommended enabling the *Isolate Destination Address* preference in Orbot settings. While this setting can theoretically improve privacy by enforcing the use of a different circuit for each IP address you connect to, it doesn't provide a practical advantage for most applications (especially web browsing), can come with a significant performance penalty, and increases the load on the Tor network. We no longer recommend adjusting this setting from its default value unless you know you need to.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Tips for Android</p>

Orbot може спрямовувати через проксі окремі програми, якщо вони підтримують SOCKS або HTTP-проксі. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN killswitch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

Orbot часто застаріває в [F-Droid репозиторії](https://guardianproject.info/fdroid) Guardian Project та [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android) Guardian Project, тому краще завантажуйте безпосередньо з [GitHub репозиторію](https://github.com/guardianproject/orbot/releases).

Всі версії підписуються одним і тим же підписом, тому вони повинні бути сумісні одна з одною.

</div>

### Onion Browser

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** is an open-source browser that lets you browse the web anonymously over the Tor network on iOS devices and is endorsed by the [Tor Project](https://support.torproject.org/glossary/onion-browser).

[:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

## Реле та мости

### Snowflake

<div class="admonition recommendation" markdown>

![Логотип Snowflake](assets/img/browsers/snowflake.svg#only-light){ align=right }
![Логотип Snowflake](assets/img/browsers/snowflake-dark.svg#only-dark){ align=right }

**Snowflake** дозволяє вам пожертвувати пропускну здатність для проекту Tor, використовуючи "проксі-сервер Snowflake" у вашому браузері.

Люди, які зазнають цензури, можуть використовувати проксі-сервери Snowflake для підключення до мережі Tor. Snowflake — це чудовий спосіб зробити внесок у мережу, навіть якщо ви не володієте технічними знаннями для запуску Tor-реле або моста.

[:octicons-home-16: Homepage](https://snowflake.torproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

</details>

</div>

You can enable Snowflake in your browser by opening it in another tab and turning the switch on. You can leave it running in the background while you browse to contribute your connection. We don't recommend installing Snowflake as a browser extension; adding third-party extensions can increase your attack surface.

[Run Snowflake in your Browser :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html ""){.md-button}

Snowflake жодним чином не збільшує вашу конфіденційність і не використовується для підключення до мережі Tor у вашому власному браузері. Однак, якщо ваше інтернет-з'єднання не піддається цензурі, вам варто подумати про його використання, щоб допомогти людям, які перебувають у мережах з цензурою, самим досягти кращої конфіденційності. Вам не потрібно турбуватися про те, до яких сайтів люди отримують доступ через ваш проксі — їх видима IP-адреса буде відповідати їх вихідному вузлу з Tor, а не вашій.

Запуск проксі-сервера Snowflake пов'язаний з навіть меншим ризиком, ніж запуск Tor-реле або моста, які й самі не є особливо ризикованими заходами. Однак він все одно спрямовує трафік проходить через вашу мережу, що може мати певний вплив, особливо якщо ваша мережа має обмежену пропускну здатність. Переконайтеся, що ви розумієте [як працює Snowflake](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) перед тим, як вирішити, чи запускати проксі.

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) and [Whonix's Stream Isolation documentation](https://whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
