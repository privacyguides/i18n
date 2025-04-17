---
meta_title: "Рекомендации и сравнение приватных VPN-сервисов, без спонсоров и рекламы - Privacy Guides"
title: "VPN сервисы"
icon: material/vpn
description: Лучшие VPN-сервисы для защиты вашей конфиденциальности и безопасности в интернете. Здесь вы найдёте провайдера, который не будет шпионить за вами.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Защищает от следующих угроз:</small>

- [:material-account-cash: Капитализм слежки](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Если вам нужна дополнительная *конфиденциальность* от интернет-провайдера, в публичной сети Wi-Fi или используя торрент, **VPN** может стать для вас решением.

<div class="admonition danger" markdown>
<p class="admonition-title">VPN не обеспечивает анонимность</p>

Использование VPN **не** сохранит вашу анонимность при просмотре веб-страниц, а также не добавит дополнительной безопасности небезопасному (HTTP) трафику.

Если вам нужна **анонимность**, воспользуйтесь браузером Tor. Если вам нужна дополнительная **безопасность**, убедитесь, что вы подключаетесь к веб-сайтам, используя HTTPS. VPN не является заменой полезных привычек для обеспечения безопасности.

[Скачать Tor](https://torproject.org){ .md-button .md-button--primary } [Мифы о Tor & ЧаВо](advanced/tor-overview.md){ .md-button }

</div>

[Подробный обзор VPN :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Рекомендованные провайдеры

Рекомендуемые нами провайдеры используют шифрование, поддерживают WireGuard & OpenVPN и не ведут логи. Для получения дополнительной информации, ознакомьтесь с [полным списком критериев](#criteria).

| Провайдер             | Страны | WireGuard                     | Проброс портов                                  | IPv6                                                               | Анонимные платежи |
| --------------------- | ------ | ----------------------------- | ----------------------------------------------- | ------------------------------------------------------------------ | ----------------- |
| [Proton](#proton-vpn) | 112+   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Частично | :material-information-outline:{ .pg-blue } Ограниченно             | Наличные          |
| [IVPN](#ivpn)         | 37+    | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }          | :material-information-outline:{ .pg-blue } Только исходящий трафик | Monero, Наличные  |
| [Mullvad](#mullvad)   | 45+    | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }          | :material-check:{ .pg-green }                                      | Monero, Наличные  |

### Proton VPN

<div class="admonition recommendation" markdown>

![Логотип Proton VPN](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** - сильный соперник в сфере VPN, работающий с 2016 года. Proton AG базируется в Швейцарии и предлагает ограниченный бесплатный доступ, а также более функциональный премиум вариант.

[:octicons-home-16: Домашняя страница](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title=Документация}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Исходный код" }

<details class="downloads" markdown>
<summary>Скачать</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://protonvpn.com/download-windows)
- [:simple-apple: macOS](https://protonvpn.com/download-macos)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 112 Стран

У Proton VPN есть [серверы в 112 странах](https://protonvpn.com/vpn-servers) или [5](https://protonvpn.com/support/how-to-create-free-vpn-account), если вы используете [бесплатный план](https://protonvpn.com/free-vpn/server).(1) Выбрав VPN-провайдера с ближайшим к вам сервером снизит задержку исходящего интернет-трафика. Это происходит из-за более короткого маршрута (меньше промежуточных серверов) до пункта назначения.
{ .annotate }

1. Последняя проверка: 06.08.2024

Мы также считаем, что для безопасности закрытых ключей VPN-провайдера ему следует использовать [выделенные серверы](https://ru.wikipedia.org/wiki/%D0%92%D1%8B%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%BD%D1%8B%D0%B9_%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80), а не более дешевые виртуальные хостинги (которые разделены между несколькими клиентами), такие как [виртуальные частные серверы](https://ru.wikipedia.org/wiki/VPS).

#### :material-check:{ .pg-green } Независимый аудит

По состоянию на январь 2020 года компания Proton VPN прошла независимый аудит от SEC Consult. SEC Consult обнаружила несколько уязвимостей среднего и низкого риска в приложениях Proton VPN для Windows, Android и iOS, все из которых Proton VPN "должным образом устранил" ещё до публикации отчетов. Ни одна из выявленных проблем не предоставила бы злоумышленнику удаленный доступ к вашему устройству или трафику. Вы можете просмотреть отдельные отчёты для каждой платформы на сайте [protonvpn.com](https://protonvpn.com/blog/open-source). В апреле 2022 года компания Proton VPN прошла [очередной аудит](https://protonvpn.com/blog/no-logs-audit). [Аттестационное письмо](https://proton.me/blog/security-audit-all-proton-apps) было предоставлено для приложений Proton VPN 9 ноября 2021 года компанией [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } Клиенты с открытым исходным кодом

Proton VPN предоставляет исходный код для своих настольных и мобильных клиентов в своём [GitHub](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Принимает наличные

Помимо приема кредитных/дебетовых карт и PayPal, Proton VPN принимает [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) и **наличные/местные валюты** как анонимные формы платежа.

#### :material-check:{ .pg-green } Поддержка WireGuard

Proton VPN поддерживает протокол WireGuard®. [WireGuard](https://wireguard.com) – это более новый протокол, в использующий самую современную [криптографию](https://wireguard.com/protocol). Кроме того, WireGuard стремится быть более простым и производительным.

Proton VPN [рекомендует](https://protonvpn.com/blog/wireguard) использовать WireGuard вместе со своим сервисом. Proton VPN также предоставляет генератор конфигураций WireGuard для использования с официальными [приложениями](https://wireguard.com/install) WireGuard.

#### :material-alert-outline:{ .pg-orange } Ограниченная поддержка IPv6

Proton [теперь поддерживает IPv6](https://protonvpn.com/support/prevent-ipv6-vpn-leaks) в своём расширении для браузера и Linux клиенте, но только 80% серверов совместимы с IPv6. На других платформах клиент Proton VPN будет блокировать весь исходящий IPv6-трафик, так что вы можете не беспокоиться об утечке вашего IPv6-адреса, но вы не сможете подключиться ни к сайтам, работающим только на IPv6, ни к Proton VPN из сети, работающей только на IPv6.

#### :material-information-outline:{ .pg-info } Удалённая переадресация портов

В настоящее время Proton VPN поддерживает только эфемерную удаленную [переадресацию портов](https://protonvpn.com/support/port-forwarding) через NAT-PMP с 60-секундным временем аренды. Официальные приложения для Windows и Linux обеспечивают к ней простой доступ, в то время как на других операционных системах вам придётся запустить собственный [NAT-PMP клиент](https://protonvpn.com/support/port-forwarding-manual-setup). Торрент приложения часто поддерживают NAT-PMP нативно.

#### :material-information-outline:{ .pg-blue } Борьба с цензурой

У Proton VPN есть протокол [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol), который *может* помочь в ситуациях, когда такие VPN-протоколы, как OpenVPN или WireGuard, блокируются с помощью ряда простейших приёмов. Stealth encapsulates the VPN tunnel in TLS session in order to look like more generic internet traffic.

Unfortunately, it does not work very well in countries where sophisticated filters that analyze all outgoing traffic in an attempt to discover encrypted tunnels are deployed. Stealth is available on Android, iOS, Windows, and macOS, but it's not yet available on Linux.

#### :material-check:{ .pg-green } Приложения для смартфонов

Proton VPN has published [App Store](https://apps.apple.com/app/id1437005085) and [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. Клиент для Android также доступен на [GitHub](https://github.com/ProtonVPN/android-app/releases).

<div class="admonition warning" markdown>
<p class="admonition-title">How to opt out of sharing telemetry</p>

On Android, Proton hides telemetry settings under the misleadingly labeled "**Help us fight censorship**" menu in the settings panel. On other platforms these settings can be found under the "**Usage statistics**" menu.

We are noting this because while we don't necessarily recommend against sharing anonymous usage statistics with developers, it is important that these settings are easily found and clearly labeled.

</div>

#### :material-information-outline:{ .pg-blue } Дополнительные замечания

Клиенты Proton VPN поддерживают двухфакторную аутентификацию на всех платформах. Proton VPN имеет собственные серверы и дата-центры в Швейцарии, Исландии и Швеции. They offer content blocking and known-malware blocking with their DNS service. Additionally, Proton VPN also offers "Tor" servers allowing you to easily connect to onion sites, but we still strongly recommend using [the official Tor Browser](tor.md#tor-browser) for this purpose.

##### :material-alert-outline:{ .pg-orange } Функция Kill switch работает неисправно на компьютерах Mac на базе Intel

При использовании VPN kill switch на компьютерах Mac на базе Intel [возможны](https://protonvpn.com/support/macos-t2-chip-kill-switch) системные сбои. Если вам необходима эта функция, и вы используете Mac с чипсетом Intel, вам следует рассмотреть возможность использования другой службы VPN.

### IVPN

<div class="admonition recommendation" markdown>

![Логотип IVPN](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** — еще один платный VPN-провайдер, работающий с 2009 года. IVPN базируется в Гибралтаре и не предлагает бесплатную пробную версию.

[:octicons-home-16: Домашняя страница](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title=Документация}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Исходный код" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:fontawesome-brands-windows: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 37 Стран

У IVPN есть [серверы в 37 странах](https://ivpn.net/status).(1) Выбрав VPN-провайдера с ближайшим к вам сервером снизит задержку исходящего интернет-трафика. Это происходит из-за более короткого маршрута (меньше промежуточных серверов) до пункта назначения.
{ .annotate }

1. Последняя проверка: 06.08.2024

Мы также считаем, что для безопасности закрытых ключей VPN-провайдера ему следует использовать [выделенные серверы](https://ru.wikipedia.org/wiki/%D0%92%D1%8B%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%BD%D1%8B%D0%B9_%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80), а не более дешевые виртуальные хостинги (которые разделены между несколькими клиентами), такие как [виртуальные частные серверы](https://ru.wikipedia.org/wiki/VPS).

#### :material-check:{ .pg-green } Независимый аудит

IVPN has had multiple [independent audits](https://ivpn.net/en/blog/tags/audit) since 2019 and has publicly announced their commitment to [annual security audits](https://ivpn.net/blog/ivpn-apps-security-audit-concluded).

#### :material-check:{ .pg-green } Клиенты с открытым исходным кодом

С февраля 2020 года [приложения IVPN перешли на открытый исходный код](https://ivpn.net/blog/ivpn-applications-are-now-open-source). Исходный код можно получить из их [репозиториев на GitHub](https://github.com/ivpn).

#### :material-check:{ .pg-green } Принимает наличные и Monero

In addition to accepting credit/debit cards and PayPal, IVPN accepts Bitcoin, **Monero** and **cash/local currency** (on annual plans) as anonymous forms of payment. Prepaid cards with redeem codes are [also available](https://ivpn.net/knowledgebase/billing/voucher-cards-faq).

#### :material-check:{ .pg-green } Поддержка WireGuard

IVPN поддерживает протокол WireGuard®️. [WireGuard](https://wireguard.com) – это более новый протокол, в использующий самую современную [криптографию](https://wireguard.com/protocol). Кроме того, WireGuard стремится быть более простым и производительным.

IVPN [recommends](https://ivpn.net/wireguard) the use of WireGuard with their service and, as such, the protocol is the default on all of IVPN's apps. IVPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-information-outline:{ .pg-blue } Поддержка IPv6

IVPN позволяет [подключаться к сервисам, использующим IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6), но не позволяет подключаться с устройства, использующего IPv6-адрес.

#### :material-alert-outline:{ .pg-orange } Удалённая переадресация портов

Ранее IVPN поддерживал переадресацию портов, но в [июне 2023 года](https://ivpn.net/blog/gradual-removal-of-port-forwarding) эта опция была убрана. Отсутствие этой функции может негативно сказаться на некоторых приложениях, особенно на пиринговых приложениях, таких как торрент-клиенты.

#### :material-check:{ .pg-green } Борьба с цензурой

IVPN has obfuscation modes using [V2Ray](https://v2ray.com/en/index.html) which helps in situations where VPN protocols like OpenVPN or WireGuard are blocked. Currently, this feature is only available on Desktop and [iOS](https://ivpn.net/knowledgebase/ios/v2ray). It has two modes where it can use [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) over QUIC or TCP connections. QUIC is a modern protocol with better congestion control and therefore may be faster with reduced latency. The TCP mode makes your data appear as regular HTTP traffic.

#### :material-check:{ .pg-green } Приложения для смартфонов

IVPN has published [App Store](https://apps.apple.com/app/id1193122683) and [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/ivpn/android-app/releases).

#### :material-information-outline:{ .pg-blue } Дополнительные замечания

Клиенты IVPN поддерживают двухфакторную аутентификацию. IVPN also provides "[AntiTracker](https://ivpn.net/antitracker)" functionality, which blocks advertising networks and trackers from the network level.

### Mullvad

<div class="admonition recommendation" markdown>

![Логотип Mullvad](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** - это быстрый и недорогой VPN с серьезным акцентом на прозрачность и безопасность. Он работает с 2009 года. Mullvad базируется в Швеции и предоставляет 14-дневную гарантию возврата денег для [способов оплаты](https://mullvad.net/en/help/refunds), которые это позволяют.

[:octicons-home-16: Домашняя страница](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion-сайт" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title=Документация}
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Исходный код" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 49 Стран

Mullvad has [servers in 49 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Это происходит из-за более короткого маршрута (меньше промежуточных серверов) до пункта назначения.
{ .annotate }

1. Last checked: 2025-03-10

Мы также считаем, что для безопасности закрытых ключей VPN-провайдера ему следует использовать [выделенные серверы](https://ru.wikipedia.org/wiki/%D0%92%D1%8B%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%BD%D1%8B%D0%B9_%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80), а не более дешевые виртуальные хостинги (которые разделены между несколькими клиентами), такие как [виртуальные частные серверы](https://ru.wikipedia.org/wiki/VPS).

#### :material-check:{ .pg-green } Независимый аудит

Mullvad has had multiple [independent audits](https://mullvad.net/en/blog/tag/audits) and has publicly announced their endeavors to conduct [annual audits](https://mullvad.net/en/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) of their apps and infrastructure.

#### :material-check:{ .pg-green } Клиенты с открытым исходным кодом

Mullvad предоставляет исходный код для своих настольных и мобильных клиентов в [GitHub](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Принимает наличные и Monero

Mullvad, in addition to accepting credit/debit cards and PayPal, accepts Bitcoin, Bitcoin Cash, **Monero** and **cash/local currency** as anonymous forms of payment. Prepaid cards with redeem codes are also available. Mullvad also accepts Swish and bank wire transfers, as well as a few European payment systems.

#### :material-check:{ .pg-green } Поддержка WireGuard

Mullvad поддерживает протокол WireGuard®. [WireGuard](https://wireguard.com) – это более новый протокол, в использующий самую современную [криптографию](https://wireguard.com/protocol). Кроме того, WireGuard стремится быть более простым и производительным.

Mullvad [recommends](https://mullvad.net/en/help/why-wireguard) the use of WireGuard with their service. It is the default or only protocol on Mullvad's Android, iOS, macOS, and Linux apps, but on Windows you have to [manually enable](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-check:{ .pg-green } Поддержка IPv6

Mullvad позволяет [получить доступ к сервисам, размещённым на IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support), и подключиться к ним с устройства, использующего IPv6-адрес.

#### :material-alert-outline:{ .pg-orange } Удаленная переадресация портов

Ранее Mullvad поддерживал переадресацию портов, но в [мае 2023 года](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports) эта возможность была убрана. Отсутствие этой функции может негативно сказаться на некоторых приложениях, особенно на пиринговых приложениях, таких как торрент-клиенты.

#### :material-check:{ .pg-green } Борьба с цензурой

Mullvad offers several features to help bypass censorship and access the internet freely:

- **Obfuscation modes**: Mullvad has two built-in obfuscation modes: "UDP-over-TCP" and ["WireGuard over Shadowsocks"](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard). These modes disguise your VPN traffic as regular web traffic, making it harder for censors to detect and block. Supposedly, China has to use a [new method to disrupt Shadowsocks-routed traffic](https://gfw.report/publications/usenixsecurity23/en).
- **Advanced obfuscation with Shadowsocks and v2ray**: For more advanced users, Mullvad provides a guide on how to use the [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) plugin with Mullvad clients. This setup provides an additional layer of obfuscation and encryption.
- **Custom server IPs**: To counter IP-blocking, you can request custom server IPs from Mullvad's support team. Once you receive the custom IPs, you can input the text file in the "Server IP override" settings, which will override the chosen server IP addresses with ones that aren't known to the censor.
- **Bridges and proxies**: Mullvad also allows you to use bridges or proxies to reach their API (needed for authentication), which can help bypass censorship attempts that block access to the API itself.

#### :material-check:{ .pg-green } Приложения для смартфонов

Оба клиента Mullvad в [App Store](https://apps.apple.com/app/id1488466513) и [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) поддерживают простой в использовании интерфейс, в противовес ручной настройке соединения WireGuard. Клиент для Android также доступен на [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Дополнительные замечания

Mullvad очень открыт в отношении того, какими узлами [владеет или арендует](https://mullvad.net/en/servers). Он также предоставляет возможность включить в своих приложениях Защиту от ИИ-анализа трафика [(DAITA](https://mullvad.net/en/blog/daita-defense-against-ai-guided-traffic-analysis)). DAITA защищает от угрозы продвинутого анализа трафика, который может быть использован для связи шаблонов в VPN трафике с определёнными веб-сайтами.

## Критерии

<div class="admonition danger" markdown>
<p class="admonition-title">Опасность</p>

Важно отметить, что использование VPN не сделает вас анонимным, но в определенных ситуациях это обеспечит вам лучшую конфиденциальность. VPN не является инструментом для незаконной деятельности. Не полагайтесь на политику "отсутствия логов".

</div>

**Обратите внимание, что мы не связаны ни с одним из рекомендуемых нами провайдеров. Это позволяет нам давать абсолютно объективные рекомендации.** Помимо [наших стандартных критериев](about/criteria.md), мы разработали четкий набор требований к любому VPN-провайдеру, желающему быть рекомендованным, включая надежное шифрование, независимый аудит безопасности, современные технологии и многое другое. Мы рекомендуем вам ознакомиться с этим списком перед выбором VPN-провайдера, а также провести собственное исследование, чтобы убедиться, что выбранный вами VPN-провайдер заслуживает максимального доверия.

### Технологии

We require all our recommended VPN providers to provide standard configuration files which can be used in a generic, open-source client. **If** a VPN provides their own custom client, we require a kill switch to block network data leaks when disconnected.

**Минимальные требования:**

- Support for strong protocols such as WireGuard.
- Kill switch built in to clients.
- Multi-hop support. Multi-hopping is important to keep data private in case of a single node compromise.
- If VPN clients are provided, they should be [open source](https://en.wikipedia.org/wiki/Open_source), like the VPN software they generally have built into them. We believe that [source code](https://en.wikipedia.org/wiki/Source_code) availability provides greater transparency about what the program is actually doing.
- Функции защиты от цензуры, разработанные для обхода брандмауэров без DPI.

**В лучшем случае:**

- Kill switch with highly configurable options (enable/disable on certain networks, on boot, etc.)
- Простые в использовании приложения VPN
- Поддержка [IPv6](https://en.wikipedia.org/wiki/IPv6). Мы ожидаем, что серверы будут разрешать входящие соединения через IPv6 и позволят вам получить доступ к услугам, размещенным на адресах IPv6.
- Возможность [удаленной переадресации портов](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) помогает создавать соединения при использовании программного обеспечения для обмена файлами P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) или хостинга сервера (например, Mumble).
- Технология маскировки, скрывающая истинную природу интернет-трафика и предназначенная для обхода передовых методов интернет-цензуры, таких как DPI.

### Конфиденциальность

Мы предпочитаем, чтобы рекомендуемые нами поставщики собирали как можно меньше данных. Не собирали личную информацию при регистрации и принимали анонимные формы оплаты.

**Минимальные требования:**

- [Анонимная криптовалюта](cryptocurrency.md) **или** возможность оплаты наличными.
- Для регистрации не требуется никакой личной информации: Только имя пользователя, пароль и, максимум электронная почта.

**В лучшем случае:**

- Принимает множество [анонимных вариантов оплаты](advanced/payments.md).
- No personal information accepted (auto-generated username, no email required, etc.).

### Безопасность

VPN бессмысленен, если он даже не может обеспечить безопасность надлежащего уровня. Мы требуем, чтобы все рекомендуемые нами провайдеры соблюдали современные стандарты безопасности. В идеале, они должны по умолчанию использовать более перспективные схемы шифрования. Мы также требуем, чтобы независимая третья сторона провела аудит безопасности провайдера, в идеале - в полном объеме и на повторяющейся (ежегодной) основе.

**Минимальные требования:**

- Надежные схемы шифрования: OpenVPN с аутентификацией SHA-256; рукопожатие RSA-2048 или лучше; шифрование данных AES-256-GCM или AES-256-CBC.
- Прямая секретность.
- Опубликованные аудиты безопасности от авторитетной сторонней фирмы.
- VPN-серверы, использующие полнодисковое шифрование или работающие только с оперативной памятью.

**В лучшем случае:**

- Самое сильное шифрование: RSA-4096.
- Дополнительное квантово-устойчивое шифрование.
- Прямая секретность.
- Опубликованные аудиты безопасности от авторитетной сторонней фирмы.
- Программы "bug-bounty" и/или скоординированный процесс раскрытия информации об уязвимостях.
- VPN-серверы только с оперативной памятью.

### Доверие

Вы бы не доверили свои финансы человеку с фальшивой личностью, так зачем доверять ему свой интернет трафик? Мы требуем, чтобы рекомендованные нами поставщики услуг открыто заявляли о своих владельцах или своём руководстве. Мы также хотели бы видеть частые отчеты о прозрачности, особенно в отношении того, как обрабатываются правительственные запросы.

**Минимальные требования:**

- Руководство или владение, ориентированное на общественность.
- Компания, расположенная в юрисдикции, где её нельзя заставить тайно делать логи.

**В лучшем случае:**

- Лидерство, ориентированное на общественность.
- Частые отчеты о прозрачности.

### Маркетинг

От провайдеров VPN, которых мы рекомендуем, мы ожидаем ответственный маркетинг.

**Минимальные требования:**

- Must self-host analytics (i.e., no Google Analytics).

Не должно быть никакого маркетинга, который является безответственным:

- Предоставление гарантий защиты анонимности на 100%. Когда кто-то утверждает: "Это является на 100% ..." - это не означает, что кто-то не может ошибиться. Мы знаем, что люди могут довольно легко деанонимизировать себя различными способами, например:
    - Повторное использование личной информации, например (учетные записи электронной почты, уникальные псевдонимы и т.д.), к которой они получили доступ без программного обеспечения обеспечивающего анонимность (Tor, VPN и т.д.)
    - [Цифровые отпечатки браузера](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Утверждение, что VPN с одним слоем "более анонимен", чем Tor, который представляет собой сеть из трех или более, регулярно меняющихся, слоёв.
- Использует ответственные формулировки: например, можно сказать, что VPN "отключена" или "не подключена", но утверждать, что кто-то "подвержен утечкам", "уязвим" или "скомпрометирован" - это ненужное использование тревожных формулировок, которые могут быть неверными. Например, этот человек может быть просто использует другого провайдера VPN или Tor.

**В лучшем случае:**

Ответственный маркетинг, который является одновременно образовательным и полезным для потребителя, может включать:

- Точное описание ситуаций, когда вместо VPN следует использовать [Tor](tor.md).
- Доступность веб-сайта провайдера VPN через сервис [.onion](https://en.wikipedia.org/wiki/.onion)

### Дополнительная функциональность

Хотя это и не является строгими требованиями, существуют и другие факторы удобства или конфиденциальности, на которые мы обращали внимание при выборе рекомендуемых провайдеров. К ним относятся блокировка контента, свидетельство канарейки, отличная служба поддержки, количество разрешенных одновременных подключений и т. д.
