---
title: "DNS-провайдеры"
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

Зашифрованный DNS со сторонними серверами следует использовать только для обхода базовой [блокировки DNS](https://en.wikipedia.org/wiki/DNS_blocking), если вы уверены, что это не повлечет за собой никаких последствий. Зашифрованный DNS не поможет вам скрыть какую-либо активность в интернете.

[Узнайте больше о DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## Рекомендованные провайдеры

These are our favorite public DNS resolvers based on their privacy and security characteristics, and their worldwide performance. Some of these services offer basic DNS-level blocking of malware or trackers depending on the server you choose, but if you want to be able to see and customize what is blocked, you should use a dedicated DNS filtering product instead.

| DNS-провайдер                                                              | Протоколы                                                                | Logging / Privacy Policy | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | Фильтрация                                                                                                                                                | Signed Apple Profile                                                                                                                                                                                                        |
| -------------------------------------------------------------------------- | ------------------------------------------------------------------------ | ------------------------ | -------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**AdGuard Public DNS**](https://adguard-dns.io/en/public-dns.html)        | Cleartext <br>DoH/3 <br>DoT <br>DoQ <br>DNSCrypt | Anonymized[^1]           | Anonymized                                                     | Based on server choice. Используемый список фильтрации можно найти здесь. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardSDNSFilter) | Yes [:octicons-link-external-24:](https://adguard-dns.io/en/blog/encrypted-dns-ios-14.html)                                                                                                                                 |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | Cleartext <br>DoH/3 <br>DoT                                  | Anonymized[^2]           | Нет                                                            | Based on server choice.                                                                                                                                   | No [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846)                                                                                                    |
| [**Control D Free DNS**](https://controld.com/free-dns)                    | Cleartext <br>DoH/3 <br>DoT <br>DoQ                    | No[^3]                   | Нет                                                            | Based on server choice.                                                                                                                                   | Yes <br>[:simple-apple: iOS](https://docs.controld.com/docs/ios-platform) <br>[:material-apple-finder: macOS](https://docs.controld.com/docs/macos-platform#manual-setup-profile)                               |
| [**DNS0.eu**](https://dns0.eu)                                             | Cleartext <br>DoH/3 <br>DoH <br>DoT <br>DoQ      | Anonymized[^4]           | Anonymized                                                     | Based on server choice.                                                                                                                                   | Yes [:octicons-link-external-24:](https://dns0.eu/zero.dns0.eu.mobileconfig)                                                                                                                                                |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | DoH <br>DoT                                                        | No[^5]                   | Нет                                                            | Based on server choice. Используемый список фильтрации можно найти здесь. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)           | Yes [:octicons-link-external-24:](https://github.com/mullvad/encrypted-dns-profiles)                                                                                                                                        |
| [**Quad9**](https://quad9.net)                                             | Cleartext <br>DoH <br>DoT <br>DNSCrypt                 | Anonymized[^6]           | Необязательное[^5]                                             | Based on server choice. Malware blocking is included by default.                                                                                          | Yes <br>[:simple-apple: iOS](https://docs.quad9.net/Setup_Guides/iOS/iOS_14_and_later_(Encrypted)) <br>[:material-apple-finder: macOS](https://docs.quad9.net/Setup_Guides/MacOS/Big_Sur_and_later_(Encrypted)) |

## Self-Hosted DNS Filtering

DNS с самостоятельным хостингом полезно для обеспечения фильтрации на управляемых платформах, таких как телевизоры Smart TV и устройства IoT (Internet of Things - Интернет вещей), поскольку для этого не требуется клиентское ПО.

### Pi-hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](assets/img/dns/pi-hole.svg){ align=right }

**Pi-hole** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

Pi-hole создана для развертывания на Raspberry Pi, но она не требует именно такого специфичного оборудования. Решение предлагает дружелюбный веб-интерфейс для просмотра подробных отчетов и управления блокировкой контента.

[:octicons-home-16: Homepage](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Source Code" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title=Contribute }

</details>

</div>

### AdGuard Home

<div class="admonition recommendation" markdown>

![AdGuard Home logo](assets/img/dns/adguard-home.svg){ align=right }

**AdGuard Home** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

AdGuard Home предлагает продуманный интерфейс для просмотра развёрнутых отчетов и управления блокировкой контента.

[:octicons-home-16: Официальный сайт](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=Документация}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Исходный код" }

</details>

</div>

## Cloud-Based DNS Filtering

These DNS filtering solutions offer a web dashboard where you can customize the block lists to your exact needs, similarly to a Pi-hole. These services are usually easier to set up and configure than self-hosted services like the ones above, and can be used more easily across multiple networks (self-hosted solutions are typically restricted to your home/local network unless you set up a more advanced configuration).

### Control D

<div class="admonition recommendation" markdown>

![Control D logo](assets/img/dns/control-d.svg){ align=right }

**Control D** is a customizable DNS service which lets you block security threats, unwanted content, and advertisements on a DNS level. In addition to their paid plans, they offer a number of preconfigured DNS resolvers you can use for free.

[:octicons-home-16: Homepage](https://controld.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://controld.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.controld.com/docs/getting-started){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Control-D-Inc/ctrld){ .card-link title="Source Code" }

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

**NextDNS** is a customizable DNS service which lets you block security threats, unwanted content, and advertisements on a DNS level. They offer a fully functional free plan for limited use.

[:octicons-home-16: Homepage](https://nextdns.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextdns.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.nextdns.io){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/nextdns/nextdns){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/nextdns/id1463342498)
- [:simple-github: GitHub](https://github.com/nextdns/nextdns/releases)
- [:fontawesome-brands-windows: Windows](https://github.com/nextdns/nextdns/wiki/Windows)
- [:simple-apple: macOS](https://apps.apple.com/us/app/nextdns/id1464122853)
- [:simple-linux: Linux](https://github.com/nextdns/nextdns/wiki)

</details>

</div>

When used with an account, NextDNS will enable insights and logging features by default (as some features require it). You can choose retention time and log storage location for any logs you choose to keep, or disable logs altogether.

NextDNS's free plan is fully functional, but should not be relied upon for security or other critical filtering applications, because after 300,000 DNS queries in a month all filtering, logging, and other account-based functionality are disabled. It can still be used as a regular DNS provider after that point, so your devices will continue to function and make secure queries via DNS-over-HTTPS (DoH), just without your filter lists.

NextDNS also offers a public DoH service at `https://dns.nextdns.io` and DNS-over-TLS/QUIC (DoT/DoQ) at `dns.nextdns.io`, which are available by default in Firefox and Chromium, and subject to their default, no-logging [privacy policy](https://nextdns.io/privacy).

## Зашифрованные DNS-прокси

Зашифрованные DNS-прокси создают локальный прокси-сервер, на который будут перенаправляться запросы с вашего системного [незашифрованного DNS-резолвера](advanced/dns-overview.md#unencrypted-dns). Typically, it is used on platforms that don't natively support [encrypted DNS](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ align=right }
![RethinkDNS logo](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** is an open-source Android client that supports [DoH](advanced/dns-overview.md#dns-over-https-doh), [DoT](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) and DNS Proxy. It also provides additional functionality such as caching DNS responses, locally logging DNS queries, and using the app as a firewall.

[:octicons-home-16: Homepage](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

While RethinkDNS takes up the Android VPN slot, you can still use a VPN or Orbot with the app by [adding a WireGuard configuration](https://docs.rethinkdns.com/proxy/wireguard) or [manually configuring Orbot as a Proxy server](https://docs.rethinkdns.com/firewall/orbot), respectively.

### DNSCrypt-Proxy

<div class="admonition recommendation" markdown>

![DNSCrypt-Proxy logo](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**DNSCrypt-Proxy** is a DNS proxy with support for [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DoH](advanced/dns-overview.md#dns-over-https-doh), and [Anonymized DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

[:octicons-repo-16: Repository](https://github.com/DNSCrypt/dnscrypt-proxy#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

The anonymized DNS feature does [not](advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns) anonymize other network traffic.

</div>

## Критерии

**Обратите внимание, что у нас нет связей ни с одним проектом, которые мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Мы рекомендуем ознакомиться с данным списком перед выбором и провести самостоятельное исследование, чтобы убедиться, что для вас это правильный выбор.

All DNS products...

- Must support [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- Must support [QNAME Minimization](advanced/dns-overview.md#what-is-qname-minimization).
- Must anonymize [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) or disable it by default.

Additionally, all public providers...

- Must not log any personal data to disk.
    - As noted in the footnotes, some providers collect query information for purposes like security research, but in that case the data must not be associated with any PII such as IP address, etc.
- Should support [anycast](https://en.wikipedia.org/wiki/Anycast) or geo-steering.

[^1]: AdGuard хранит показатели производительности их DNS серверов, содержащие в себе количество выполненных запросов к определенному серверу, количество заблокированных запросов и скорость обработки. They also keep and store the database of domains requested within the last 24 hours.

    > We need this information to identify and block new trackers and threats. We also log how many times this or that tracker has been blocked. We need this information to remove outdated rules from our filters.

    AdGuard DNS: [*Privacy Policy*](https://adguard-dns.io/en/privacy.html) [^2]: Cloudflare collects and stores only the limited DNS query data that is sent to the 1.1.1.1 resolver. The 1.1.1.1 resolver service does not log personal data, and the bulk of the limited non-personally identifiable query data is stored only for 25 hours.

    1.1.1.1 Public DNS Resolver: [*Cloudflare’s commitment to privacy*](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) [^3]: Control D only logs specific account data for Premium resolvers with custom DNS profiles. Free resolvers do not retain any data.

    Control D: [*Privacy Policy*](https://controld.com/privacy) [^4]: DNS0.eu collects some data for their threat intelligence feeds to monitor for newly registered/observed/active domains and other bulk data. That data is shared with some [partners](https://docs.dns0.eu/data-feeds/introduction) for e.g. security research. They do not collect any personally identifiable information.

    DNS0.eu: [*Privacy Policy*](https://dns0.eu/privacy) [^5]: Mullvad's DNS service is available to both subscribers and non-subscribers of Mullvad VPN. Их политика конфиденциальности утверждает, что они ни в каком виде не сохраняют DNS-запросы.

    Mullvad: [*No-logging of user activity policy*](https://mullvad.net/en/help/no-logging-data-policy) [^6]: Quad9 collects some data for the purposes of threat monitoring and response. That data may then be remixed and shared for purposes like furthering their security research. Quad9 не собирает и не хранит IP-адреса и другую информацию, которую они считают идентифицирующей пользователя.

    Quad9: [*Data and Privacy Policy*](https://quad9.net/privacy/policy)
