---
meta_title: "Tor Browser and Network: Anonymous Web Browsing - Privacy Guides"
title: "Сеть Tor"
icon: simple/torproject
description: Защитите свой интернет-сёрфинг от посторонних глаз, используя сеть Tor - безопасную сеть, обходящую цензуру.
cover: tor.png
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
    image: /assets/img/browsers/tor.svg
    url: https://www.torproject.org
    sameAs: https://ru.wikipedia.org/wiki/Tor
    applicationCategory: Браузер
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
---

![Tor logo](assets/img/self-contained-networks/tor.svg){ align=right }

Сеть **Tor** - это группа серверов, управляемых волонтёрами, которая позволяет вам бесплатно подключаться к сети и повышать уровень конфиденциальности и безопасности в интернете. Частные лица и организации также могут делиться информацией через сеть Tor с помощью "скрытых сервисов .onion" без ущерба для своей конфиденциальности. Поскольку трафик Tor сложно заблокировать и отследить, Tor является эффективным инструментом обхода цензуры.

[:octicons-home-16:](https://www.torproject.org){ .card-link title=Домашняя страница }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Ресурс" }
[:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Документация }
[:octicons-code-16:](https://gitweb.torproject.org/tor.git){ .card-link title="Исходный код" }
[:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Внести вклад}

Tor работает, направляя ваш трафик через эти серверы, управляемые волонтёрами, вместо прямого соединения с сайтом, который вы пытаетесь посетить. Это скрывает, откуда идет трафик, и ни один сервер на пути соединения не может увидеть полный путь того, откуда и куда идет трафик, то есть даже серверы, которые вы используете для подключения, не могут нарушить вашу анонимность.

[Подробный обзор Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Подключение к Tor

Существует множество способов подключения к сети Tor с вашего устройства, наиболее распространенным из которых является **Tor Browser**, форк Firefox, предназначенный для анонимного просмотра веб-страниц на настольных компьютерах и Android. Помимо перечисленных ниже приложений, существуют также операционные системы, разработанные специально для подключения к сети Tor, такие как [Whonix](desktop.md#whonix) или [Qubes OS](desktop.md#qubes-os), которые обеспечивают еще большую безопасность и защиту, чем стандартный Tor Browser.

### Tor Browser

!!! recommendation

    ![Логотип Tor Browser](assets/img/browsers/tor.svg){ align=right }
    
    **Tor Browser** - это выбор, если вам нужна анонимность, поскольку он предоставляет доступ к сети Tor и мостам, а также включает в себя настройки и расширения, которые автоматически конфигурируются по выбранным уровням безопасности: *Обычный*, *Высокий* и *Высший*.
    
    [:octicons-home-16: Домашняя страница](https://www.torproject.org/ru/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion ресурс" }
    [:octicons-info-16:](https://tb-manual.torproject.org/ru/){ .card-link title=Документация }
    [:octicons-code-16:](https://gitweb.torproject.org/tor-browser.git/){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Поддержать }
    
    ??? загрузить
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
        - [:simple-android: Android](https://www.torproject.org/ru/download/#android)
        - [:simple-windows11: Windows](https://www.torproject.org/ru/download/)
        - [:simple-apple: macOS](https://www.torproject.org/ru/download/)
        - [:simple-linux: Linux](https://www.torproject.org/ru/download/)
        - [:simple-freebsd: FreeBSD](https://www.freshports.org/security/tor)

!!! осторожно

    Вам **никогда** не следует устанавливать дополнительные расширения для Tor Browser или редактировать настройки `about:config`, включая те, которые мы предлагаем для Firefox. Расширения браузера и нестандартные настройки выделяют вас среди других пользователей сети Tor, тем самым делая уникальным ваш [fingerprint](https://support.torproject.org/ru/glossary/browser-fingerprinting/).

Браузер Tor предназначен для предотвращения "отпечатков пальцев", или идентификации вас на основе конфигурации вашего браузера. Поэтому крайне важно, чтобы вы **не** изменяли браузер, помимо установленных по умолчанию [уровней безопасности](https://tb-manual.torproject.org/ru/security-settings/).

### Orbot

!!! recommendation

    ![Orbot logo](assets/img/self-contained-networks/orbot.svg){ align=right }
    
    **Orbot** is a free Tor VPN for smartphones which routes traffic from any app on your device through the Tor network.
    
    [:octicons-home-16: Homepage](https://orbot.app/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
    [:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/orbot/id1609461599)
        - [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

We previously recommended enabling the *Isolate Destination Address* preference in Orbot settings. While this setting can theoretically improve privacy by enforcing the use of a different circuit for each IP address you connect to, it doesn't provide a practical advantage for most applications (especially web browsing), can come with a significant performance penalty, and increases the load on the Tor network. We no longer recommend adjusting this setting from its default value unless you know you need to.[^1]

!!! tip "Tips for Android"

    Orbot can proxy individual apps if they support SOCKS or HTTP proxying. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN killswitch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.
    
    Orbot is often outdated on the Guardian Project's [F-Droid repository](https://guardianproject.info/fdroid) and [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android), so consider downloading directly from the [GitHub repository](https://github.com/guardianproject/orbot/releases) instead.
    
    All versions are signed using the same signature so they should be compatible with each other.

## Relays and Bridges

### Terms of Service; Didn't Read

!!! recommendation

    ![Snowflake logo](assets/img/browsers/snowflake.svg#only-light){ align=right }
    ![Snowflake logo](assets/img/browsers/snowflake-dark.svg#only-dark){ align=right }
    
    **Snowflake** allows you to donate bandwidth to the Tor Project by operating a "Snowflake proxy" within your browser.
    
    People who are censored can use Snowflake proxies to connect to the Tor network. Snowflake is a great way to contribute to the network even if you don't have the technical know-how to run a Tor relay or bridge.
    
    [:octicons-home-16: Homepage](https://snowflake.torproject.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitweb.torproject.org/pluggable-transports/snowflake.git/){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/en-US/firefox/addon/torproject-snowflake/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/snowflake/mafpmfcccpbjnhfhjnllmmalhifmlcie)
        - [:octicons-browser-16: Web](https://snowflake.torproject.org/embed "Leave this page open to be a Snowflake proxy")

??? tip "Embedded Snowflake"

    You can enable Snowflake in your browser by clicking the switch below and ==leaving this page open==. You can also install Snowflake as a browser extension to have it always run while your browser is open, however adding third-party extensions can increase your attack surface.
    
    <center><iframe src="https://snowflake.torproject.org/embed.html" width="320" height="240" frameborder="0" scrolling="no"></iframe></center>
    <small>If the embed does not appear for you, ensure you are not blocking the third-party frame from `torproject.org`. Alternatively, visit [this page](https://snowflake.torproject.org/embed.html).</small>

Snowflake does not increase your privacy in any way, nor is it used to connect to the Tor network within your personal browser. However, if your internet connection is uncensored, you should consider running it to help people in censored networks achieve better privacy themselves. There is no need to worry about which websites people are accessing through your proxy—their visible browsing IP address will match their Tor exit node, not yours.

Running a Snowflake proxy is low-risk, even moreso than running a Tor relay or bridge which are already not particularly risky endeavours. However, it does still proxy traffic through your network which can be impactful in some ways, especially if your network is bandwidth-limited. Make sure you understand [how Snowflake works](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) before deciding whether to run a proxy.

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) and [Whonix's Stream Isolation documentation](https://www.whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
