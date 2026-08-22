---
title: DNS-провайдеры
icon: material/dns
description: We recommend choosing these encrypted DNS providers to replace your ISP's default configuration.
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Защищает от следующих угроз:</small>

- [:material-account-cash: Капитализм слежки](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Зашифрованный **DNS** со сторонними серверами следует использовать только для обхода базовой [блокировки DNS](https://en.wikipedia.org/wiki/DNS_blocking), если вы уверены, что это не повлечет за собой никаких последствий. Зашифрованный DNS не поможет вам скрыть какую-либо активность в интернете.

[Узнайте больше о DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## Рекомендованные провайдеры

These are our favorite public DNS resolvers based on their privacy and security characteristics, and their worldwide performance. Some of these services offer basic DNS-level blocking of malware or trackers depending on the server you choose, but if you want to be able to see and customize what is blocked, you should use a dedicated DNS filtering product instead.

| DNS-провайдер                                                              | Протоколы                                                                     | Логирование / Политика конфиденциальности | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | Фильтрация                                                                                                                                                       | Профиль конфигурации Apple                                                                                                                                                                                                 |
| -------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------- | -------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**AdGuard Public DNS**](https://adguard-dns.io/en/public-dns.html)        | Без шифрования <br>DoH/3 <br>DoT <br>DoQ <br>DNSCrypt | Анонимное[^1]                             | Анонимное                                                      | Зависит от выбранного сервера. Используемый список фильтрации можно найти здесь. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardSDNSFilter) | Да [:octicons-link-external-24:](https://adguard-dns.io/en/blog/encrypted-dns-ios-14.html)                                                                                                                                 |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | Без шифрования <br>DoH/3 <br>DoT                                  | Anonymized[^2]                            | Нет                                                            | Зависит от выбранного сервера.                                                                                                                                   | Нет [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846)                                                                                                  |
| [**Control D Free DNS**](https://controld.com/free-dns)                    | Без шифрования <br>DoH/3 <br>DoT <br>DoQ                    | No[^3]                                    | Нет                                                            | Зависит от выбранного сервера.                                                                                                                                   | Да <br>[:simple-apple: iOS](https://docs.controld.com/docs/ios-platform) <br>[:material-apple-finder: macOS](https://docs.controld.com/docs/macos-platform#manual-setup-profile)                               |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | DoH <br>DoT                                                             | No[^4]                                    | Нет                                                            | Зависит от выбранного сервера. Используемый список фильтрации можно найти здесь. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)           | Да [:octicons-link-external-24:](https://github.com/mullvad/encrypted-dns-profiles)                                                                                                                                        |
| [**Quad9**](https://quad9.net)                                             | Без шифрования <br>DoH/3 <br>DoT <br>DoQ <br>DNSCrypt | Anonymized[^5]                            | Необязательное[^5]                                             | Зависит от выбранного сервера. Malware blocking is included by default.                                                                                          | Да <br>[:simple-apple: iOS](https://docs.quad9.net/Setup_Guides/iOS/iOS_14_and_later_(Encrypted)) <br>[:material-apple-finder: macOS](https://docs.quad9.net/Setup_Guides/MacOS/Big_Sur_and_later_(Encrypted)) |

## Облачная фильтрация DNS

These DNS filtering solutions offer a web dashboard where you can customize the block lists to your exact needs. These services can be used easily across multiple networks.

### Control D

<div class="admonition recommendation" markdown>

![Логотип Control D](assets/img/dns/control-d.svg){ align=right }

**Control D** — это настраиваемый DNS-сервис, позволяющий блокировать угрозы безопасности, нежелательный контент и рекламу на уровне DNS.

Помимо платных тарифных планов, они предлагают ряд готовых DNS-резолверов, которыми можно пользоваться бесплатно.

[:octicons-home-16: Главная](https://controld.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://controld.com/privacy){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://docs.controld.com/docs/getting-started){ .card-link title="Документация" }
[:octicons-code-16:](https://github.com/Control-D-Inc/ctrld){ .card-link title="Исходный код" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.controld.setuputility)
- [:simple-appstore: App Store](https://apps.apple.com/app/1518799460)
- [:simple-github: GitHub](https://github.com/Control-D-Inc/ctrld/releases)
- [:fontawesome-brands-windows: Windows](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-apple: macOS](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-linux: Linux](https://docs.controld.com/docs/ctrld)

</details>

</div>

### NextDNS

<div class="admonition recommendation" markdown>

![NextDNS logo](assets/img/dns/nextdns.svg){ align=right }

**NextDNS** — это настраиваемый DNS-сервис, позволяющий блокировать угрозы безопасности, нежелательный контент и рекламу на уровне DNS.

They offer a fully functional free plan for limited use.

[:octicons-home-16: Главная](https://nextdns.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextdns.io/privacy){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://help.nextdns.io){ .card-link title="Документация" }
[:octicons-code-16:](https://github.com/nextdns/nextdns){ .card-link title="Исходный код" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/nextdns/id1463342498)
- [:simple-github: GitHub](https://github.com/nextdns/nextdns/releases)
- [:fontawesome-brands-windows: Windows](https://github.com/nextdns/nextdns/wiki/Windows)
- [:simple-apple: macOS](https://apps.apple.com/us/app/nextdns/id1464122853)
- [:simple-linux: Linux](https://github.com/nextdns/nextdns/wiki)

</details>

</div>

When used with an account, NextDNS will enable insights and logging features by default (as some features require it). Вы можете самостоятельно выбрать время и место хранения ваши логов или вовсе отключить их.

NextDNS's free plan is fully functional, but should not be relied upon for security or other critical filtering applications, because after 300,000 DNS queries in a month all filtering, logging, and other account-based functionality are disabled. It can still be used as a regular DNS provider after that point, so your devices will continue to function and make secure queries via DNS-over-HTTPS (DoH), just without your filter lists.

NextDNS also offers a public DoH service at `https://dns.nextdns.io` and DNS-over-TLS/QUIC (DoT/DoQ) at `dns.nextdns.io`, which are available by default in Firefox and Chromium, and subject to their default, no-logging [privacy policy](https://nextdns.io/privacy).

## Зашифрованные DNS-прокси

Зашифрованные DNS-прокси создают локальный прокси-сервер, на который будут перенаправляться запросы с вашего системного [незашифрованного DNS-резолвера](advanced/dns-overview.md#unencrypted-dns). Обычно они подходят для устройств, не поддерживающих [зашифрованный DNS](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

<div class="admonition recommendation" markdown>

![Логотип RethinkDNS](assets/img/android/rethinkdns.svg#only-light){ align=right }
![Логотип RethinkDNS](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** — это открытый Android-клиент, поддерживающий [DoH](advanced/dns-overview.md#dns-over-https-doh), [DoT](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) и DNS-прокси. It also provides additional functionality such as caching DNS responses, locally logging DNS queries, and using the app as a firewall.

[:octicons-home-16: Главная](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title="Документация" }
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Исходный код" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

While RethinkDNS takes up the Android VPN slot, you can still use a VPN or Orbot with the app by [adding a WireGuard configuration](https://docs.rethinkdns.com/proxy/wireguard) or [manually configuring Orbot as a Proxy server](https://docs.rethinkdns.com/firewall/orbot), respectively.

### DNSCrypt-Proxy

<div class="admonition recommendation" markdown>

![Логотип DNSCrypt-Proxy](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**DNSCrypt-Proxy** — это DNS-прокси с поддержкой [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DoH](advanced/dns-overview.md#dns-over-https-doh) и [анонимизированного DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

[:octicons-repo-16: Репозиторий](https://github.com/DNSCrypt/dnscrypt-proxy#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title="Документация"}
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Исходный код" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title=Поддержать" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Внимание!</p>

Функция анонимизированного DNS [не](advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns) анонимизирует весь остальной трафик.

</div>

## Критерии

**Обратите внимание, что у нас нет связей ни с одним проектом, которые мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Мы рекомендуем ознакомиться с данным списком перед выбором и провести самостоятельное исследование, чтобы убедиться, что для вас это правильный выбор.

Все DNS...

- Должны поддерживать [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- Должны поддерживать [QNAME Minimization](advanced/dns-overview.md#what-is-qname-minimization).
- Должны анонимизировать [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) или отключить ее по умолчанию.

Кроме того, все публичные провайдеры...

- Must not log any personal data to disk.
    - As noted in the footnotes, some providers collect query information for purposes like security research, but in such cases, the data must not be associated with any PII such as IP address, etc.
- Should support [anycast](https://en.wikipedia.org/wiki/Anycast) or geo-steering.

[^1]: AdGuard хранит показатели производительности их DNS серверов, содержащие в себе количество выполненных запросов к определенному серверу, количество заблокированных запросов и скорость обработки. Он также ведет и хранит базу данных доменов, запрошенных в течение последних 24 часов.

    > Нам нужна эта информация, чтобы выявлять и блокировать новые трекеры и угрозы. Также мы храним информацию о том, сколько раз тот или иной трекер был заблокирован. Нам нужна эта информация, чтобы удалять устаревшие правила из наших фильтров.

    AdGuard DNS: [*Privacy Policy*](https://adguard-dns.io/en/privacy.html) [^2]: Cloudflare collects and stores only the limited DNS query data that is sent to the 1.1.1.1 resolver. The 1.1.1.1 resolver service does not log personal data, and the bulk of the limited non-personally identifiable query data is stored only for 25 hours.

    1.1.1.1 Public DNS Resolver: [*Cloudflare’s commitment to privacy*](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) [^3]: Control D only logs specific account data for Premium resolvers with custom DNS profiles. Free resolvers do not retain any data.

    Control D: [*Privacy Policy*](https://controld.com/privacy) [^4]: Mullvad's DNS service is available to both subscribers and non-subscribers of Mullvad VPN. Их политика конфиденциальности утверждает, что они ни в каком виде не сохраняют DNS-запросы.

    Mullvad: [*No-logging of user activity policy*](https://mullvad.net/en/help/no-logging-data-policy) [^5]: Quad9 collects some data for the purposes of threat monitoring and response. Эти данные могут быть изменены и переданы, например, в целях исследования безопасности. Quad9 не собирает и не хранит IP-адреса и другую информацию, которую они считают идентифицирующей пользователя.

    Quad9: [*Политика в отношении данных и конфиденциальности*](https://quad9.net/privacy/policy)
