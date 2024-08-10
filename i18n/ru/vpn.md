---
meta_title: "Рекомендации и сравнение приватных VPN-сервисов, без спонсоров и рекламы - Privacy Guides"
title: "VPN сервисы"
icon: material/vpn
description: Это лучшие VPN-сервисы для защиты вашей конфиденциальности и безопасности в Интернете. Найдите провайдера, который не будет шпионить за вами.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Капитализм слежки](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

If you're looking for additional *privacy* from your ISP, on a public Wi-Fi network, or while torrenting files, a **VPN** may be the solution for you.

<div class="admonition danger" markdown>
<p class="admonition-title">VPNs do not provide anonymity</p>

Using a VPN will **not** keep your browsing habits anonymous, nor will it add additional security to non-secure (HTTP) traffic.

If you are looking for **anonymity**, you should use the Tor Browser. If you're looking for added **security**, you should always ensure you're connecting to websites using HTTPS. VPN не является заменой полезных привычек для обеспечения безопасности.

[Download Tor](https://torproject.org){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Подробный обзор VPN :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Рекомендованные провайдеры

Our recommended providers use encryption, support WireGuard & OpenVPN, and have a no logging policy. Для получения дополнительной информации, ознакомьтесь с \[полным списком критериев\](#_18).

| Provider              | Countries | WireGuard                     | Port Forwarding                                            | IPv6                                                     | Anonymous Payments |
| --------------------- | --------- | ----------------------------- | ---------------------------------------------------------- | -------------------------------------------------------- | ------------------ |
| [Proton](#proton-vpn) | 112+      | :material-check:{ .pg-green } | :material-information-outline:{ .pg-blue } Partial Support | :material-alert-outline:{ .pg-orange }                   | Наличные           |
| [IVPN](#ivpn)         | 37+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                     | :material-information-outline:{ .pg-blue } Outgoing Only | Monero, Cash       |
| [Mullvad](#mullvad)   | 45+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                            | Monero, Cash       |

### Proton VPN

<div class="admonition recommendation" markdown>

![Логотип Proton VPN](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** - сильный соперник в сфере VPN, работающий с 2016 года. Proton AG базируется в Швейцарии и предлагает ограниченный бесплатный доступ, а также более функциональный премиум вариант.

[:octicons-home-16: Homepage](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://protonvpn.com/download-windows)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 112 Countries

Proton VPN has [servers in 112 countries](https://protonvpn.com/vpn-servers) or [5](https://protonvpn.com/support/how-to-create-free-vpn-account) if you use their [free plan](https://protonvpn.com/free-vpn/server).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Это происходит из-за более короткого маршрута (меньше промежуточных серверов) до пункта назначения.
{ .annotate }

1. Last checked: 2024-08-06

Мы также считаем, что для безопасности закрытых ключей VPN-провайдера ему следует использовать [выделенные серверы](https://ru.wikipedia.org/wiki/%D0%92%D1%8B%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%BD%D1%8B%D0%B9_%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80), а не более дешевые виртуальные хостинги (которые разделены между несколькими клиентами), такие как [виртуальные частные серверы](https://ru.wikipedia.org/wiki/VPS).

#### :material-check:{ .pg-green } Независимый аудит

По состоянию на январь 2020 года компания Proton VPN прошла независимый аудит от SEC Consult. SEC Consult обнаружила несколько уязвимостей среднего и низкого риска в приложениях Proton VPN для Windows, Android и iOS, все из которых Proton VPN "должным образом устранил" ещё до публикации отчетов. Ни одна из выявленных проблем не предоставила бы злоумышленнику удаленный доступ к вашему устройству или трафику. You can view individual reports for each platform at [protonvpn.com](https://protonvpn.com/blog/open-source). In April 2022 Proton VPN underwent [another audit](https://protonvpn.com/blog/no-logs-audit). [Аттестационное письмо](https://proton.me/blog/security-audit-all-proton-apps) было предоставлено для приложений Proton VPN 9 ноября 2021 года компанией [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } Клиенты с открытым исходным кодом

Proton VPN предоставляет исходный код для своих настольных и мобильных клиентов в своём [GitHub](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Принимает наличные

Помимо приема кредитных/дебетовых карт и PayPal, Proton VPN принимает [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) и **наличные/местные валюты** как анонимные формы платежа.

#### :material-check:{ .pg-green } Поддержка WireGuard

Proton VPN, в основном, поддерживает протокол WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Кроме того, WireGuard стремится быть более простым и производительным.

Proton VPN [recommends](https://protonvpn.com/blog/wireguard) the use of WireGuard with their service. On Proton VPN's Windows, macOS, iOS, Android, ChromeOS, and Android TV apps, WireGuard is the default protocol; however, [support](https://protonvpn.com/support/how-to-change-vpn-protocols) for the protocol is not present in their Linux app.

#### :material-alert-outline:{ .pg-orange } No IPv6 Support

Proton VPN's servers are only compatible with IPv4. The Proton VPN applications will block all outgoing IPv6 traffic, so you don't have to worry about your IPv6 address being leaked, but you will not be able to connect to any IPv6-only sites, and you will not be able to connect to Proton VPN from an IPv6-only network.

#### :material-information-outline:{ .pg-info } Remote Port Forwarding

Proton VPN currently only supports ephemeral remote [port forwarding](https://protonvpn.com/support/port-forwarding) via NAT-PMP, with 60 second lease times. The Windows app provides an easy to access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup). Торрент приложения часто поддерживают NAT-PMP нативно.

#### :material-information-outline:{ .pg-blue } Anti-Censorship

Proton VPN has their [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) protocol which *may* help in situations where VPN protocols like OpenVPN or Wireguard are blocked with various rudimentary techniques. Stealth encapsulates the VPN tunnel in TLS session in order to look like more generic internet traffic.

Unfortunately, it does not work very well in countries where sophisticated filters that analyze all outgoing traffic in an attempt to discover encrypted tunnels are deployed. Stealth is available on Android, iOS, Windows, and macOS, but it's not yet available on Linux.

#### :material-check:{ .pg-green } Приложения для смартфонов

In addition to providing standard OpenVPN configuration files, Proton VPN has mobile clients for [App Store](https://apps.apple.com/app/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android), and [GitHub](https://github.com/ProtonVPN/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } Additional Notes

Proton VPN clients support two factor authentication on all platforms. Proton VPN имеет собственные серверы и дата-центры в Швейцарии, Исландии и Швеции. They offer content blocking and known-malware blocking with their DNS service. Additionally, Proton VPN also offers "Tor" servers allowing you to easily connect to onion sites, but we still strongly recommend using [the official Tor Browser](tor.md#tor-browser) for this purpose.

##### :material-alert-outline:{ .pg-orange } Функция Killswitch не работает на Mac на базе Intel

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch) on Intel-based Macs when using the VPN killswitch. Если вам необходима эта функция, и вы используете Mac с чипсетом Intel, вам следует рассмотреть возможность использования другой службы VPN.

### IVPN

<div class="admonition recommendation" markdown>

![Логотип IVPN](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** — еще один платный VPN-провайдер, работающий с 2009 года. IVPN is based in Gibraltar and does not offer a free trial.

[:octicons-home-16: Homepage](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Source Code" }

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

IVPN has [servers in 37 countries](https://ivpn.net/status).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Это происходит из-за более короткого маршрута (меньше промежуточных серверов) до пункта назначения.
{ .annotate }

1. Last checked: 2024-08-06

Мы также считаем, что для безопасности закрытых ключей VPN-провайдера ему следует использовать [выделенные серверы](https://ru.wikipedia.org/wiki/%D0%92%D1%8B%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%BD%D1%8B%D0%B9_%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80), а не более дешевые виртуальные хостинги (которые разделены между несколькими клиентами), такие как [виртуальные частные серверы](https://ru.wikipedia.org/wiki/VPS).

#### :material-check:{ .pg-green } Независимый аудит

IVPN прошла [аудит отсутствия логов от Cure53](https://cure53.de/audit-report_ivpn.pdf), который подтвердил заявление IVPN о том, что они не сохраняют логи. IVPN также подготовила [отчет о комплексном пентесте Cure53](https://cure53.de/summary-report_ivpn_2019.pdf) в январе 2020 года. IVPN has also said they plan to have [annual reports](https://ivpn.net/blog/independent-security-audit-concluded) in the future. A further review was conducted [in April 2022](https://ivpn.net/blog/ivpn-apps-security-audit-2022-concluded) and was produced by Cure53 [on their website](https://cure53.de/pentest-report_IVPN_2022.pdf).

#### :material-check:{ .pg-green } Клиенты с открытым исходным кодом

As of February 2020 [IVPN applications are now open source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). Исходный код можно получить из их [репозиториев на GitHub](https://github.com/ivpn).

#### :material-check:{ .pg-green } Принимает наличные и Monero

In addition to accepting credit/debit cards and PayPal, IVPN accepts Bitcoin, **Monero** and **cash/local currency** (on annual plans) as anonymous forms of payment. Prepaid cards with redeem codes are [also available](https://ivpn.net/knowledgebase/billing/voucher-cards-faq).

#### :material-check:{ .pg-green } Поддержка WireGuard

IVPN поддерживает протокол WireGuard®️. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Кроме того, WireGuard стремится быть более простым и производительным.

IVPN [recommends](https://ivpn.net/wireguard) the use of WireGuard with their service and, as such, the protocol is the default on all of IVPN's apps. IVPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-information-outline:{ .pg-blue } IPv6 Support

IVPN allows you to [connect to services using IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6) but doesn't allow you to connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } Удалённая переадресация портов

IVPN previously supported port forwarding, but removed the option in [June 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). Отсутствие этой функции может негативно сказаться на некоторых приложениях, особенно на пиринговых приложениях, таких как торрент-клиенты.

#### :material-check:{ .pg-green } Anti-Censorship

IVPN has obfuscation modes using the [v2ray](https://v2ray.com/en/index.html) project which helps in situations where VPN protocols like OpenVPN or Wireguard are blocked. Currently this feature is only available on Desktop and [iOS](https://ivpn.net/knowledgebase/ios/v2ray). It has two modes where it can use [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) over QUIC or TCP connections. QUIC is a modern protocol with better congestion control and therefore may be faster with reduced latency. The TCP mode makes your data appear as regular HTTP traffic.

#### :material-check:{ .pg-green } Приложения для смартфонов

In addition to providing standard OpenVPN configuration files, IVPN has mobile clients for [App Store](https://apps.apple.com/app/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), and [GitHub](https://github.com/ivpn/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } Additional Notes

IVPN clients support two factor authentication. IVPN also provides "[AntiTracker](https://ivpn.net/antitracker)" functionality, which blocks advertising networks and trackers from the network level.

### Mullvad

<div class="admonition recommendation" markdown>

![Логотип Mullvad](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** - это быстрый и недорогой VPN с серьезным акцентом на прозрачность и безопасность. They have been in operation since 2009. Mullvad is based in Sweden and does not offer a free trial.

[:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Source Code" }

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

#### :material-check:{ .pg-green } 45 Countries

Mullvad has [servers in 45 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Это происходит из-за более короткого маршрута (меньше промежуточных серверов) до пункта назначения.
{ .annotate }

1. Last checked: 2024-08-06

Мы также считаем, что для безопасности закрытых ключей VPN-провайдера ему следует использовать [выделенные серверы](https://ru.wikipedia.org/wiki/%D0%92%D1%8B%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%BD%D1%8B%D0%B9_%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80), а не более дешевые виртуальные хостинги (которые разделены между несколькими клиентами), такие как [виртуальные частные серверы](https://ru.wikipedia.org/wiki/VPS).

#### :material-check:{ .pg-green } Независимый аудит

Приложения Mullvad VPN прошли аудит от Cure53 и Assured AB в отчёте на проникновение [опубликованном на сайте cure53.de](https://cure53.de/pentest-report_mullvad_v2.pdf). Исследователи безопасности пришли к выводу:

> Cure53 и Assured AB довольны результатами аудита, а программное обеспечение оставляет в целом положительное впечатление. Учитывая преданность безопасности внутренней команды Mullvad VPN, у тестеров нет сомнений в том, что проект находится на правильном пути с точки зрения безопасности.

In 2020 a second audit [was announced](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app) and the [final audit report](https://cure53.de/pentest-report_mullvad_2020_v2.pdf) was made available on Cure53's website:

> Результаты этого проекта, осуществляемого в мае-июне 2020 года и направленного на комплекс Mullvad, весьма позитивны. [...] Общая экосистема приложений, используемая Mullvad, оставляет впечатление надежности и структурированности. Общая структура приложения позволяет легко и структурировано внедрять исправления и патчи. Более того, результаты, обнаруженные Cure53, демонстрируют важность постоянного аудита и переоценки текущих векторов утечки, чтобы всегда обеспечивать конфиденциальность конечных пользователей. Mullvad отлично справляется с защитой конечных пользователей от утечек личной информации и рисков, связанных с конфиденциальностью.

In 2021 an infrastructure audit [was announced](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) and the [final audit report](https://cure53.de/pentest-report_mullvad_2021_v1.pdf) was made available on Cure53's website. Another report was commissioned [in June 2022](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data) and is available on [Assured's website](https://assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf).

#### :material-check:{ .pg-green } Клиенты с открытым исходным кодом

Mullvad предоставляет исходный код для своих настольных и мобильных клиентов в [GitHub](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Принимает наличные и Monero

Mullvad, in addition to accepting credit/debit cards and PayPal, accepts Bitcoin, Bitcoin Cash, **Monero** and **cash/local currency** as anonymous forms of payment. Prepaid cards with redeem codes are also available. Mullvad also accepts Swish and bank wire transfers.

#### :material-check:{ .pg-green } Поддержка WireGuard

Mullvad поддерживает протокол WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Кроме того, WireGuard стремится быть более простым и производительным.

Mullvad [recommends](https://mullvad.net/en/help/why-wireguard) the use of WireGuard with their service. It is the default or only protocol on Mullvad's Android, iOS, macOS, and Linux apps, but on Windows you have to [manually enable](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-check:{ .pg-green } Поддержка IPv6

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) and connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } Удаленная переадресация портов

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). Отсутствие этой функции может негативно сказаться на некоторых приложениях, особенно на пиринговых приложениях, таких как торрент-клиенты.

#### :material-check:{ .pg-green } Anti-Censorship

Mullvad has obfuscation an mode using [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) which may be useful in situations where VPN protocols like OpenVPN or Wireguard are blocked.

#### :material-check:{ .pg-green } Приложения для смартфонов

Mullvad has published [App Store](https://apps.apple.com/app/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. Клиент для Android также доступен на [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Additional Notes

Mullvad is very transparent about which nodes they [own or rent](https://mullvad.net/en/servers). They use [ShadowSocks](https://shadowsocks.org) in their ShadowSocks + OpenVPN configuration, making them more resistant against firewalls with [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) trying to block VPNs. Предположительно, [Китаю приходится использовать другой метод для блокировки серверов ShadowSocks](https://github.com/net4people/bbs/issues/22).

## Критерии

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Важно отметить, что использование VPN не сделает вас анонимным, но в определенных ситуациях это обеспечит вам лучшую конфиденциальность. VPN не является инструментом для незаконной деятельности. Не полагайтесь на политику "отсутствия логов".

</div>

**Обратите внимание, что мы не связаны ни с одним из рекомендуемых нами провайдеров. Это позволяет нам давать абсолютно объективные рекомендации.** Помимо [наших стандартных критериев](about/criteria.md), мы разработали четкий набор требований к любому VPN-провайдеру, желающему быть рекомендованным, включая надежное шифрование, независимый аудит безопасности, современные технологии и многое другое. Мы рекомендуем вам ознакомиться с этим списком перед выбором VPN-провайдера, а также провести собственное исследование, чтобы убедиться, что выбранный вами VPN-провайдер заслуживает максимального доверия.

### Технологии

Мы требуем, чтобы все рекомендуемые нами VPN-провайдеры предоставляли файлы конфигурации OpenVPN для использования в любом клиенте. **Если** VPN предоставляет свой собственный пользовательский клиент, мы требуем наличия killswitch для блокировки утечки сетевых данных при отключении.

**Минимальные требования:**

- Поддержка надежных протоколов, таких как WireGuard & OpenVPN.
- Killswitch встроен в приложения.
- Поддержка Multihop. Multihop важен для сохранения конфиденциальности данных в случае компрометации одного узла.
- If VPN clients are provided, they should be [open source](https://en.wikipedia.org/wiki/Open_source), like the VPN software they generally have built into them. Мы считаем, что доступность [исходного кода](https://en.wikipedia.org/wiki/Source_code) обеспечивает большую прозрачность в отношении того, что на самом деле делает ваше устройство.

**В лучшем случае:**

- Killswitch с широкими возможностями настройки (включение/выключение в определенных сетях, при включении и т.д.)
- Простые в использовании приложения VPN
- Поддержка [IPv6](https://en.wikipedia.org/wiki/IPv6). Мы ожидаем, что серверы будут разрешать входящие соединения через IPv6 и позволят вам получить доступ к услугам, размещенным на адресах IPv6.
- Возможность [удаленной переадресации портов](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) помогает создавать соединения при использовании программного обеспечения для обмена файлами P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) или хостинга сервера (например, Mumble).
- Obfuscation technology which pads data packets with random data to circumvent internet censorship.

### Конфиденциальность

Мы предпочитаем, чтобы рекомендуемые нами поставщики собирали как можно меньше данных. Не собирали личную информацию при регистрации и принимали анонимные формы оплаты.

**Минимальные требования:**

- [Анонимная криптовалюта](cryptocurrency.md) **или** возможность оплаты наличными.
- Для регистрации не требуется никакой личной информации: Только имя пользователя, пароль и, максимум электронная почта.

**В лучшем случае:**

- Принимает множество [анонимных вариантов оплаты](advanced/payments.md).
- Не принимается личная информация (автогенерируемое имя пользователя, не требуется электронная почта и т.д.).

### Безопасность

VPN бессмысленен, если он даже не может обеспечить адекватную безопасность. Мы требуем, чтобы все рекомендуемые нами провайдеры соблюдали современные стандарты безопасности для своих соединений OpenVPN. В идеале, они должны по умолчанию использовать более перспективные схемы шифрования. Мы также требуем, чтобы независимая третья сторона провела аудит безопасности провайдера, в идеале - в полном объеме и на повторяющейся (ежегодной) основе.

**Минимальные требования:**

- Надежные схемы шифрования: OpenVPN с аутентификацией SHA-256; рукопожатие RSA-2048 или лучше; шифрование данных AES-256-GCM или AES-256-CBC.
- Прямая секретность.
- Опубликованные аудиты безопасности от авторитетной сторонней фирмы.

**В лучшем случае:**

- Самое сильное шифрование: RSA-4096.
- Прямая секретность.
- Опубликованные аудиты безопасности от авторитетной сторонней фирмы.
- Программы "bug-bounty" и/или скоординированный процесс раскрытия информации об уязвимостях.

### Доверие

Вы бы не доверили свои финансы человеку с фальшивой личностью, так зачем доверять ему свой интернет трафик? Мы требуем, чтобы рекомендованные нами поставщики услуг открыто заявляли о своих владельцах или своём руководстве. Мы также хотели бы видеть частые отчеты о прозрачности, особенно в отношении того, как обрабатываются правительственные запросы.

**Минимальные требования:**

- Руководство или владение, ориентированное на общественность.

**В лучшем случае:**

- Лидерство, ориентированное на общественность.
- Частые отчеты о прозрачности.

### Маркетинг

От провайдеров VPN, которых мы рекомендуем, мы ожидаем ответственный маркетинг.

**Минимальные требования:**

- Должен самостоятельно проводить аналитику (т.е. не Google Analytics). Сайт провайдера также должен соответствовать требованиям [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) для людей, которые хотят отказаться от аналитики.

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

Хотя это и не является строгими требованиями, существуют и другие факторы удобства или конфиденциальности, на которые мы обращали внимание при выборе рекомендуемых провайдеров. These include content blocking functionality, warrant canaries, multihop connections, excellent customer support, the number of allowed simultaneous connections, etc.
