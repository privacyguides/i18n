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

**Tor** is a group of volunteer-operated servers that allows you to connect for free and improve your privacy and security on the Internet. Частные лица и организации также могут делиться информацией через сеть Tor с помощью "скрытых сервисов .onion" без ущерба для своей конфиденциальности. Поскольку трафик Tor сложно заблокировать и отследить, Tor является эффективным инструментом обхода цензуры.

[Подробный обзор Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Before connecting to Tor, please ensure you've read our [overview](advanced/tor-overview.md) on what Tor is and how to connect to it safely. We often recommend connecting to Tor through a trusted [VPN provider](vpn.md), but you have to do so **properly** to avoid decreasing your anonymity.

</div>

Существует множество способов подключения к сети Tor с твоего устройства, наиболее распространенным из которых является **Tor Browser**, форк Firefox, предназначенный для анонимного просмотра веб-страниц на настольных компьютерах и Android.

Some of these apps are better than others, and again making a determination comes down to your threat model. If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using apps like [Orbot](#orbot) or mobile browser apps to access the Tor network is probably fine. Increasing the number of people who use Tor on an everyday basis helps reduce the bad stigma of Tor, and lowers the quality of "lists of Tor users" that ISPs and governments may compile.

If more complete anonymity is paramount to your situation, you should **only** be using the desktop Tor Browser client, ideally in a [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os) configuration. Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

## Tor Browser

<div class="admonition recommendation" markdown>

![Логотип Tor Browser](assets/img/browsers/tor.svg){ align=right }

**Tor Browser** - это выбор, если тебе нужна анонимность, поскольку он предоставляет доступ к сети Tor и мостам, а также включает в себя настройки и расширения, которые автоматически конфигурируются по выбранным уровням безопасности: *Обычный*, *Высокий* и *Высший*.

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

Тебе **никогда** не следует устанавливать дополнительные расширения для Tor Browser или редактировать настройки `about:config`, включая те, которые мы предлагаем для Firefox. Расширения браузера и нестандартные настройки выделяют тебя среди других пользователей сети Tor, тем самым делая уникальным твой [отпечаток браузера](https://support.torproject.org/ru/glossary/browser-fingerprinting/).

</div>

Браузер Tor предназначен для предотвращения "отпечатков браузера", или идентификации тебя на основе конфигурации твоего браузера. Therefore, it is imperative that you do **not** modify the browser beyond the default [security levels](https://tb-manual.torproject.org/security-settings).

In addition to installing Tor Browser on your computer directly, there are also operating systems designed specifically to connect to the Tor network such as [Whonix](desktop.md#whonix) on [Qubes OS](desktop.md#qubes-os), which provide even greater security and protections than the standard Tor Browser alone.

## Orbot

<div class="admonition recommendation" markdown>

![Логотип Orbot](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** - это бесплатный Tor VPN для смартфонов, который направляет трафик от любого приложения на твоём устройстве через сеть Tor.

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

Ранее мы рекомендовали включать *Изолировать адреса назначения* в настройках Orbot. Хотя эта настройка теоретически может улучшить конфиденциальность за счет принудительного использования отдельной схемы для каждого IP-адреса, к которому ты подключаешься, она не дает практического преимущества для большинства приложений (особенно для просмотра веб-страниц), может сопровождаться значительным снижением производительности и увеличивает нагрузку на сеть Tor. We no longer recommend adjusting this setting from its default value unless you know you need to.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Tips for Android</p>

Orbot может проксировать отдельные приложения, если они поддерживают SOCKS или HTTP проксирование. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN killswitch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

В [репозитории F-Droid](https://guardianproject.info/fdroid) проекта Guardian и [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android) часто загружена устаревшая версия Orbot, поэтому его лучше загружать непосредственно с [оепозитория GitHub](https://github.com/guardianproject/orbot/releases).

Все версии подписаны одной и той же подписью, поэтому они должны быть совместимы друг с другом.

</div>

## Onion Browser

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
