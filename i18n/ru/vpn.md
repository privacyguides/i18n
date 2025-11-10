---
meta_title: "Рекомендации и сравнение приватных VPN-сервисов, без спонсоров и рекламы - Privacy Guides"
title: VPN сервисы
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

[Introduction to the Tor Browser](tor.md#tor-browser){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Подробный обзор VPN :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Рекомендованные провайдеры

Рекомендуемые нами провайдеры используют шифрование, поддерживают WireGuard & OpenVPN и не ведут логи. Для получения дополнительной информации, ознакомьтесь с [полным списком критериев](#criteria).

| Провайдер             | Страны | WireGuard                     | Проброс портов                                  | IPv6                                                               | Анонимные платежи            |
| --------------------- | ------ | ----------------------------- | ----------------------------------------------- | ------------------------------------------------------------------ | ---------------------------- |
| [Proton](#proton-vpn) | 127+   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Частично | :material-information-outline:{ .pg-blue } Ограниченно             | Cash  Monero via third party |
| [IVPN](#ivpn)         | 41+    | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }          | :material-information-outline:{ .pg-blue } Только исходящий трафик | Monero  Cash                 |
| [Mullvad](#mullvad)   | 49+    | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }          | :material-check:{ .pg-green }                                      | Monero  Cash                 |

### Proton VPN

<div class="admonition recommendation" markdown>

![Логотип Proton VPN](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** - сильный игрок в сфере VPN, работающий с 2016 года. Proton AG базируется в Швейцарии и предлагает ограниченный бесплатный доступ, а также более функциональный премиум вариант.

[:octicons-home-16: Homepage](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Source Code" }

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

#### :material-check:{ .pg-green } 127 Countries

Proton VPN has [servers in 127 countries](https://protonvpn.com/vpn-servers)(1) or [10](https://protonvpn.com/support/how-to-create-free-vpn-account) if you use their [free plan](https://protonvpn.com/blog/product-roadmap-winter-2025-2026).(2) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Это происходит из-за более короткого маршрута (меньше промежуточных серверов) до пункта назначения.
{ .annotate }

1. Of which at least 71 are virtual servers, meaning your IP will appear from the country but the server is in another. 12 more locations have both hardware and virtual servers. [Source](https://protonvpn.com/support/how-smart-routing-works)
2. Last checked: 2025-10-28

Мы также считаем, что для безопасности закрытых ключей VPN-провайдера ему следует использовать [выделенные серверы](https://ru.wikipedia.org/wiki/%D0%92%D1%8B%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%BD%D1%8B%D0%B9_%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80), а не более дешевые виртуальные хостинги (которые разделены между несколькими клиентами), такие как [виртуальные частные серверы](https://ru.wikipedia.org/wiki/VPS).

#### :material-check:{ .pg-green } Независимый аудит

Independent security researcher Ruben Santamarta conducted audits for Proton VPN's [browser extensions](https://drive.proton.me/urls/RWDD2SHT98#v7ZrwNcafkG8) and [apps](https://drive.proton.me/urls/RVW8TXG484#uTXX5Fc9GADo) in September 2024 and January 2025, respectively. Proton VPN's infrastrcture has undergone [annual audits](https://protonvpn.com/blog/no-logs-audit) by Securitum since 2022.

Previously, Proton VPN underwent an independent audit by SEC Consult in January 2020. SEC Consult обнаружила несколько уязвимостей среднего и низкого риска в приложениях Proton VPN для Windows, Android и iOS, все из которых Proton VPN "должным образом устранил" ещё до публикации отчетов. Ни одна из выявленных проблем не предоставила бы злоумышленнику удаленный доступ к вашему устройству или трафику. You can view individual reports for each platform in their dedicated [blog post](https://web.archive.org/web/20250307041036/https://protonvpn.com/blog/open-source) on the audit.

#### :material-check:{ .pg-green } Клиенты с открытым исходным кодом

Proton VPN provides the source code for their desktop and mobile clients in their [GitHub organization](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Принимает наличные

Proton VPN, in addition to accepting credit/debit cards, PayPal, and [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), also accepts **cash/local currency** as an anonymous form of payment. You can also use [**Monero**](cryptocurrency.md#monero) to purchase vouchers for Proton VPN Plus and Proton Unlimited via their [official](https://discuss.privacyguides.net/t/add-monero-as-an-anonymous-payment-method-for-proton-services/31058/15) reseller [ProxyStore](https://dys2p.com/en/2025-09-09-proton.html).

#### :material-check:{ .pg-green } Поддержка WireGuard

Proton VPN поддерживает протокол WireGuard®. [WireGuard](https://wireguard.com) – это более новый протокол, в использующий самую современную [криптографию](https://wireguard.com/protocol). Кроме того, WireGuard стремится быть более простым и производительным.

Proton VPN [рекомендует](https://protonvpn.com/blog/wireguard) использовать WireGuard вместе со своим сервисом. Proton VPN также предоставляет генератор конфигураций WireGuard для использования с официальными [приложениями](https://wireguard.com/install) WireGuard.

#### :material-alert-outline:{ .pg-orange } Ограниченная поддержка IPv6

Proton [теперь поддерживает IPv6](https://protonvpn.com/support/prevent-ipv6-vpn-leaks) в своём расширении для браузера и Linux клиенте, но только 80% серверов совместимы с IPv6. На других платформах клиент Proton VPN будет блокировать весь исходящий IPv6-трафик, так что вы можете не беспокоиться об утечке вашего IPv6-адреса, но вы не сможете подключиться ни к сайтам, работающим только на IPv6, ни к Proton VPN из сети, работающей только на IPv6.

#### :material-information-outline:{ .pg-info } Удалённая переадресация портов

В настоящее время Proton VPN поддерживает только эфемерную удаленную [переадресацию портов](https://protonvpn.com/support/port-forwarding) через NAT-PMP с 60-секундным временем аренды. Официальные приложения для Windows и Linux обеспечивают к ней простой доступ, в то время как на других операционных системах вам придётся запустить собственный [NAT-PMP клиент](https://protonvpn.com/support/port-forwarding-manual-setup). Торрент приложения часто поддерживают NAT-PMP нативно.

#### :material-information-outline:{ .pg-blue } Борьба с цензурой

У Proton VPN есть протокол [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol), который *может* помочь в ситуациях, когда такие VPN-протоколы, как OpenVPN или WireGuard, блокируются с помощью ряда простейших приёмов. Stealth инкапсулирует VPN-туннель в сессию TLS, чтобы он выглядел как обычный интернет-трафик.

К сожалению, это не очень хорошо работает в странах, где используются сложные фильтры, анализирующие весь исходящий трафик в попытке обнаружить зашифрованные туннели. Stealth доступен на Android, iOS, Windows и macOS, но пока недоступен на Linux.

#### :material-check:{ .pg-green } Приложения для смартфонов

Proton VPN опубликовал клиенты [App Store](https://apps.apple.com/app/id1437005085) и [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android), оба из которых поддерживают простой в использовании интерфейс, в отличие от необходимости вручную настраивать соединение WireGuard. Клиент для Android также доступен на [GitHub](https://github.com/ProtonVPN/android-app/releases).

<div class="admonition warning" markdown>
<p class="admonition-title">Как отказаться от передачи телеметрии</p>

На Android, Proton скрывает настройки телеметрии под вводящим в заблуждение названием "**Помогите нам бороться с цензурой**" в панели настроек. На других платформах эти настройки можно найти в меню "**Статистика использования**".

Мы отмечаем это, поскольку, хотя мы не обязательно выступаем против передачи анонимной статистики использования разработчикам, важно, чтобы эти настройки было легко найти, и они имели четкие обозначения.

</div>

#### :material-information-outline:{ .pg-blue } Дополнительные замечания

Клиенты Proton VPN поддерживают двухфакторную аутентификацию на всех платформах. Proton VPN имеет собственные серверы и дата-центры в Швейцарии, Исландии и Швеции. Они предлагают блокировку контента и блокировку известного вредоносного ПО с помощью своей DNS-службы. Кроме того, Proton VPN также предлагает "Tor" серверы, позволяющие вам легко подключаться к onion-сайтам, но мы все еще настоятельно рекомендуем использовать [официальный Tor Browser](tor.md#tor-browser) для этой цели.

##### :material-alert-outline:{ .pg-orange } Функция Kill switch работает неисправно на компьютерах Mac на базе Intel

При использовании VPN kill switch на компьютерах Mac на базе Intel [возможны](https://protonvpn.com/support/macos-t2-chip-kill-switch) системные сбои. Если вам необходима эта функция, и вы используете Mac с чипсетом Intel, вам следует рассмотреть возможность использования другой службы VPN.

### IVPN

<div class="admonition recommendation" markdown>

![Логотип IVPN](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** — еще один платный VPN-провайдер, работающий с 2009 года. IVPN базируется в Гибралтаре и не предлагает бесплатную пробную версию.

[:octicons-home-16: Homepage](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Скачать</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-github: GitHub](https://github.com/ivpn/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 41 Countries

IVPN has [servers in 41 countries](https://ivpn.net/status).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Это происходит из-за более короткого маршрута (меньше промежуточных серверов) до пункта назначения.
{ .annotate }

1. Last checked: 2025-10-28

Мы также считаем, что для безопасности закрытых ключей VPN-провайдера ему следует использовать [выделенные серверы](https://ru.wikipedia.org/wiki/%D0%92%D1%8B%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%BD%D1%8B%D0%B9_%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80), а не более дешевые виртуальные хостинги (которые разделены между несколькими клиентами), такие как [виртуальные частные серверы](https://ru.wikipedia.org/wiki/VPS).

#### :material-check:{ .pg-green } Независимый аудит

У IVPN было несколько [независимых аудитов](https://ivpn.net/en/blog/tags/audit) с 2019 года, и они публично объявили о своей приверженности [ежегодным аудитам безопасности](https://ivpn.net/blog/ivpn-apps-security-audit-concluded).

#### :material-check:{ .pg-green } Клиенты с открытым исходным кодом

С февраля 2020 года [приложения IVPN перешли на открытый исходный код](https://ivpn.net/blog/ivpn-applications-are-now-open-source). Исходный код можно получить из их [репозиториев на GitHub](https://github.com/ivpn).

#### :material-check:{ .pg-green } Принимает наличные и Monero

В дополнение к приему кредитных/дебетовых карт и PayPal, IVPN принимает Bitcoin, **Monero** и **наличные/местную валюту** (при годовых планах) в качестве анонимных форм оплаты. You can also purchase [prepaid cards](https://ivpn.net/knowledgebase/billing/voucher-cards-faq) with redeem codes.

#### :material-check:{ .pg-green } Поддержка WireGuard

IVPN поддерживает протокол WireGuard®️. [WireGuard](https://wireguard.com) – это более новый протокол, в использующий самую современную [криптографию](https://wireguard.com/protocol). Кроме того, WireGuard стремится быть более простым и производительным.

IVPN [рекомендует](https://ivpn.net/wireguard) использование WireGuard со своим сервисом, и, таким образом, этот протокол является стандартным во всех приложениях IVPN. IVPN также предлагает генератор конфигурации WireGuard для использования с официальными [приложениями](https://wireguard.com/install) WireGuard.

#### :material-information-outline:{ .pg-blue } Поддержка IPv6

IVPN позволяет [подключаться к сервисам, использующим IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6), но не позволяет подключаться с устройства, использующего IPv6-адрес.

#### :material-alert-outline:{ .pg-orange } Удалённая переадресация портов

Ранее IVPN поддерживал переадресацию портов, но в [июне 2023 года](https://ivpn.net/blog/gradual-removal-of-port-forwarding) эта опция была убрана. Отсутствие этой функции может негативно сказаться на некоторых приложениях, особенно на пиринговых приложениях, таких как торрент-клиенты.

#### :material-check:{ .pg-green } Борьба с цензурой

IVPN имеет режимы обфускации с помощью [V2Ray](https://v2ray.com/en/index.html), что помогает в ситуациях, когда VPN-протоколы, такие, как OpenVPN или WireGuard, заблокированы. В настоящее время эта функция доступна только на настольных компьютерах и [iOS](https://ivpn.net/knowledgebase/ios/v2ray). Он имеет два режима, в которых может использовать [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) через QUIC или TCP-соединения. QUIC — это современный протокол с улучшенным контролем перегрузок, поэтому он может быть быстрее и с меньшей задержкой. В режиме TCP твои данные выглядят как обычный HTTP-трафик.

#### :material-check:{ .pg-green } Приложения для смартфонов

IVPN опубликовал клиенты в [App Store](https://apps.apple.com/app/id1193122683) и [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client) оба поддерживают простой в использовании интерфейс, в отличие от необходимости вручную настраивать соединение WireGuard. Клиент для Android также доступен на [GitHub](https://github.com/ivpn/android-app/releases).

#### :material-information-outline:{ .pg-blue } Дополнительные замечания

Клиенты IVPN поддерживают двухфакторную аутентификацию. IVPN также предоставляет функцию "[AntiTracker](https://ivpn.net/antitracker)", которая блокирует рекламу и трекеры на сетевом уровне.

### Mullvad

<div class="admonition recommendation" markdown>

![Логотип Mullvad](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** - это быстрый и недорогой VPN с серьезным акцентом на прозрачность и безопасность. Он работает с 2009 года. Mullvad базируется в Швеции и предоставляет 14-дневную гарантию возврата денег для [способов оплаты](https://mullvad.net/en/help/refunds), которые это позволяют.

[:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Скачать</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 49 Стран

У Mullvad есть [серверы в 49 странах](https://mullvad.net/servers).(1) Выбор VPN провайдера с ближайшим к вам сервером снизит задержку при передаче трафика. Это происходит из-за более короткого маршрута (меньше промежуточных серверов) до пункта назначения.
{ .annotate }

1. Last checked: 2025-10-28

Мы также считаем, что для безопасности закрытых ключей VPN-провайдера ему следует использовать [выделенные серверы](https://ru.wikipedia.org/wiki/%D0%92%D1%8B%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%BD%D1%8B%D0%B9_%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80), а не более дешевые виртуальные хостинги (которые разделены между несколькими клиентами), такие как [виртуальные частные серверы](https://ru.wikipedia.org/wiki/VPS).

#### :material-check:{ .pg-green } Независимый аудит

У Mullvad было несколько [независимых аудитов](https://mullvad.net/en/blog/tag/audits), и они публично объявили о своих намерениях проводить [ежегодный аудит](https://mullvad.net/en/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) своих приложений и инфраструктуры.

#### :material-check:{ .pg-green } Клиенты с открытым исходным кодом

Mullvad предоставляет исходный код для своих настольных и мобильных клиентов в [GitHub](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Принимает наличные и Monero

Помимо приема кредитных/дебетовых карт и PayPal, Mullvad принимает Bitcoin, Bitcoin Cash, **Monero** и **наличные/местные валюты** как анонимные формы платежа. You can also purchase [prepaid cards](https://mullvad.net/en/help/partnerships-and-resellers) with redeem codes. Mullvad также принимает Swish и банковские переводы, а также несколько европейских платежных систем.

#### :material-check:{ .pg-green } Поддержка WireGuard

Mullvad поддерживает протокол WireGuard®. [WireGuard](https://wireguard.com) – это более новый протокол, в использующий самую современную [криптографию](https://wireguard.com/protocol). Кроме того, WireGuard стремится быть более простым и производительным.

Mullvad [рекомендует](https://mullvad.net/en/help/why-wireguard) использовать WireGuard с их сервисами. It is the only protocol supported on their mobile apps, and their desktop apps will [lose OpenVPN support](https://mullvad.net/en/blog/reminder-that-openvpn-is-being-removed) in 2025. Additionally, their servers will stop accepting OpenVPN connections by January 15, 2026. Mullvad также предлагает генератор конфигурации WireGuard для использования с официальными[приложениями](https://wireguard.com/install) WireGuard.

#### :material-check:{ .pg-green } Поддержка IPv6

Mullvad позволяет [получить доступ к сервисам, размещённым на IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support), и подключиться к ним с устройства, использующего IPv6-адрес.

#### :material-alert-outline:{ .pg-orange } Удаленная переадресация портов

Ранее Mullvad поддерживал переадресацию портов, но в [мае 2023 года](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports) эта возможность была убрана. Отсутствие этой функции может негативно сказаться на некоторых приложениях, особенно на пиринговых приложениях, таких как торрент-клиенты.

#### :material-check:{ .pg-green } Борьба с цензурой

Mullvad предлагает несколько функций, позволяющих обойти цензуру и получить свободный доступ в интернет:

- **Режимы обфускации**: Mullvad имеет два встроенных режима обфускации: "UDP-over-TCP" и ["WireGuard over Shadowsocks"](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard). Эти режимы маскируют ваш VPN-трафик под обычный веб-трафик, что затрудняет его обнаружение и блокировку цензорами. Предположительно, Китаю приходится использовать [новый метод, чтобы нарушить маршрутизацию трафика Shadowsocks.](https://gfw.report/publications/usenixsecurity23/en)
- **Продвинутая обфускация с помощью Shadowsocks и v2ray**: Для более опытных пользователей Mullvad предлагает руководство по использованию плагина [Shadowsocks и v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) с клиентами Mullvad. Такая настройка обеспечивает дополнительный уровень маскировки и шифрования.
- **Пользовательские IP-адреса серверов**: Чтобы противодействовать блокировке IP, вы можете запросить пользовательские IP-адреса серверов у службы поддержки Mullvad. Получив пользовательские IP-адреса, вы можете ввести текстовый файл в настройках "Server IP override" (Переопределение IP-адреса сервера), что заменит выбранные IP-адреса серверов на те, которые не известны цензору.
- **Мосты и прокси**: Mullvad также позволяет использовать мосты или прокси для доступа к своему API (необходимо для аутентификации), что может помочь обойти попытки цензуры, блокирующие доступ к самому API.

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

Мы требуем, чтобы все наши рекомендуемые VPN-провайдеры предоставляли стандартные конфигурационные файлы, которые можно использовать в универсальном клиенте с открытым исходным кодом. **Если** VPN предоставляет свой собственный пользовательский клиент, мы требуем наличия kill switch для блокировки утечки сетевых данных при отключении.

**Минимальные требования:**

- Поддержка надежных протоколов, таких как WireGuard.
- Kill switch встроен в приложения.
- Поддержка Multi-hop. Multi-hop важен для сохранения конфиденциальности данных в случае компрометации одного узла.
- Если предоставляются VPN-клиенты, они должны быть [с открытым исходным кодом](https://en.wikipedia.org/wiki/Open_source), как и VPN-программное обеспечение, которое обычно в них встроено. Мы считаем, что доступность [исходного кода](https://en.wikipedia.org/wiki/Source_code) обеспечивает большую прозрачность относительно того, что программа на самом деле делает.
- Функции защиты от цензуры, разработанные для обхода брандмауэров без DPI.

**В лучшем случае:**

- Kill switch с широкими возможностями настройки (включение/выключение в определенных сетях, при включении и т.д.)
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
- Не принимается личная информация (автогенерируемое имя пользователя, не требуется электронная почта и т.д.).

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

- Должен самостоятельно проводить аналитику (т.е. не Google Analytics).

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
