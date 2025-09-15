---
meta_title: "Браузер и сеть Tor: Анонимный браузинг - Privacy Guides"
title: "Tor Browser"
icon: simple/torbrowser
description: Защити свой интернет-сёрфинг от посторонних глаз, используя сеть Tor - безопасную сеть, обходящую цензуру.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
    sameAs: https://ru.wikipedia.org/wiki/Tor
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

<small>Защищает от следующих угроз:</small>

- [:material-account-cash: Капитализм слежки](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: Массовое наблюдение](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Цензура](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

**Tor** — это группа серверов, управляемых волонтёрами, которая позволяет тебе бесплатно подключаться и к сети и улучшать твою конфиденциальность и безопасность в Интернете. Частные лица и организации также могут делиться информацией через сеть Tor с помощью "скрытых сервисов .onion" без ущерба для своей конфиденциальности. Поскольку трафик Tor сложно заблокировать и отследить, Tor является эффективным инструментом обхода цензуры.

[Подробный обзор Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: Видео: почему тебе нужен Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Совет</p>

Прежде чем подключаться к Tor, пожалуйста, ознакомься с нашим [обзором](advanced/tor-overview.md) о том, что такое Tor и как безопасно к нему подключаться. Мы часто рекомендуем подключаться к Tor через доверенного [VPN-провайдера](vpn.md), но ты должен делать это **правильно**, чтобы избежать снижения твоей анонимности.

</div>

Существует множество способов подключения к сети Tor с твоего устройства, самым распространенным из которых является **Tor Browser**, форк Firefox, разработанный для [:material-incognito: анонимного](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} посмотра веб-страниц на настольных компьютерах и Android.

Некоторые из этих приложений лучше других; выбор зависит от твоей модели угроз. Если ты обычный пользователь Tor, который не беспокоится о том, что интернет-провайдер собирает улики против тебя, использование мобильных браузерных приложений, таких как [Onion Browser](#onion-browser-ios), для доступа к сети Tor, вероятно, будет нормальным. Увеличение числа людей, использующих Tor в повседневной жизни, помогает уменьшить негативную стигму вокруг Tor и снижает качество "списков пользователей Tor", которые могут составлять интернет-провайдеры и правительства.

Если для тебя важна полная анонимность, используй **только** настольный клиент Tor Browser, в идеале - в конфигурации [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os). Мобильные браузеры менее распространены в Tor (и, как следствие, более подвержены фингерпринтингу), а другие конфигурации не так тщательно проверены на предмет деанонимизации.

## Tor Browser

<div class="admonition recommendation" markdown>

![Логотип Tor Browser](assets/img/browsers/tor.svg){ align=right }

**Tor Browser** — лучший выбор, если тебе нужна анонимность, поскольку он предоставляет доступ к сети Tor и мостам, а также включает настройки по умолчанию и расширения, которые автоматически настраиваются в соответствии с уровнями безопасности по умолчанию: *Обычный*, *Высокий* и *Высший*.


[:octicons-home-16: Домашняя страницы](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title="Документация" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Исходный код" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title="Внести свой вклад" }

<details class="downloads" markdown>
<summary>Скачать</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:fontawesome-brands-windows: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Важно!</p>

Тебе **никогда** не следует устанавливать дополнительные расширения для Tor Browser или редактировать настройки `about:config`, включая те, которые мы предлагаем для Firefox. Расширения браузера и нестандартные настройки выделяют тебя среди других пользователей сети Tor, тем самым делая уникальным твой [отпечаток браузера](https://support.torproject.org/ru/glossary/browser-fingerprinting/).

</div>

Браузер Tor предназначен для предотвращения "отпечатков браузера", или идентификации тебя на основе конфигурации твоего браузера. Поэтому крайне важно, чтобы ты **не** изменял браузер за пределами стандартных [уровней безопасности](https://tb-manual.torproject.org/security-settings). При изменении настройки уровня безопасности ты **обязательно** должен перезапустить браузер перед продолжением его использования. В противном случае [настройки безопасности могут быть применены не полностью](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), что подвергает вас более высокому риску фингерпринтинга и эксплойтов, чем вы можете ожидать, исходя из выбранных настроек.

В дополнение к прямой установке Tor Browser на твой компьютер, существуют также операционные системы, специально разработанные для подключения к сети Tor, такие как [Whonix](desktop.md#whonix) на [Qubes OS](desktop.md#qubes-os), которые обеспечивают еще большую безопасность и защиту, чем стандартный Tor Browser сам по себе.

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Логотип Onion Browser](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** — это браузер с открытым исходным кодом, позволяющий анонимно просматривать интернет через сеть Tor на устройствах iOS и поддерживаемый [Проектом Tor](https://support.torproject.org/glossary/onion-browser).

[:material-star-box: Прочитай наш последний обзор Onion Browser.](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review)

[:octicons-home-16: Домашняя страница](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title="Документация" }
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Исходный код" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title="Внести свой вклад" }

<details class="downloads" markdown>
<summary>Скачать</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser не обеспечивает такой же уровень защиты конфиденциальности, как Tor Browser на настольных платформах. Для повседневного использования это вполне подходящий способ доступа к скрытым сервисам. Но если ты беспокоишься о том, что продвинутые противники могут отследить тебя или следить за тобой, не следует полагаться на это как на инструмент анонимности.

[Примечательно](https://github.com/privacyguides/privacyguides.org/issues/2929), что Onion Browser *не гарантирует*, что все запросы проходят через Tor. При использовании встроенной версии Tor [твой реальный IP **будет** раскрыт через WebRTC и аудио/видео потоки](https://onionbrowser.com/faqs) из-за ограничений WebKit. *Безопаснее* использовать Onion Browser вместе с [Orbot](alternative-networks.md#orbot), но это все равно имеет некоторые ограничения на iOS.
