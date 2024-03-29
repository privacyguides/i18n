---
title: "Розв'язувачі DNS"
icon: material/dns
description: Ось кілька провайдерів зашифрованих DNS, на яких ми рекомендуємо перейти, щоб замінити конфігурацію за замовчуванням вашого Інтернет-провайдера.
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

Зашифрований DNS на сторонніх серверах слід використовувати, щоб обійти базове [блокування за DNS](https://en.wikipedia.org/wiki/DNS_blocking) лише тоді, коли ви впевнені, що це не матиме жодних наслідків. Зашифрований DNS не допоможе вам приховати будь-яку вашу веб-активність.

[Дізнайтеся більше про DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## Рекомендовані DNS-провайдери

| DNS-провайдер                                                              | Політика конфіденційності                                                                            | Протоколи                                                                    | Логування       | ECS         | Фільтрація                                                                                                                                                   |
| -------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | --------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [**AdGuard**](https://adguard.com/en/adguard-dns/overview.html)            | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                               | Cleartext <br> DoH/3 <br> DoT <br> DoQ <br> DNSCrypt | Деяке[^1]       | Yes         | Based on personal configuration. Список використовуваних фільтрів можна знайти тут. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) | Незашифрований текст <br> DoH/3 <br> DoT                         | Деяке[^2]       | Ні          | Based on personal configuration.                                                                                                                             |
| [**Control D**](https://controld.com/free-dns)                             | [:octicons-link-external-24:](https://controld.com/privacy)                                          | Незашифрований текст <br> DoH/3 <br> DoT <br> DoQ          | Опціонально[^3] | Ні          | Based on personal configuration.                                                                                                                             |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy)                    | DoH <br> DoT                                                           | Немає[^4]       | Ні          | Based on personal configuration. Список використовуваних фільтрів можна знайти тут. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    |
| [**NextDNS**](https://nextdns.io)                                          | [:octicons-link-external-24:](https://nextdns.io/privacy)                                            | Незашифрований текст <br> DoH/3 <br> DoT <br> DoQ          | Опціонально[^5] | Опціонально | Based on personal configuration.                                                                                                                             |
| [**Quad9**](https://quad9.net)                                             | [:octicons-link-external-24:](https://quad9.net/privacy/policy)                                      | Незашифрований текст <br> DoH <br> DoT <br> DNSCrypt       | Деяке[^6]       | Опціонально | Based on personal configuration, Malware blocking by default.                                                                                                |

### Criteria

**Зверніть увагу, що ми не пов'язані з жодним з проектів, які ми рекомендуємо.** На додаток до [наших стандартних критеріїв](about/criteria.md), ми розробили чіткий набір вимог, які дозволяють нам надавати об'єктивні рекомендації. Ми пропонуємо вам ознайомитися з цим списком перед тим, як вибрати проект, і провести власне дослідження, щоб переконатися, що це правильний вибір для вас.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Ми працюємо над встановленням чітких критеріїв для кожного розділу нашого сайту, і вони можуть бути змінені. Якщо у вас виникли запитання щодо наших критеріїв, будь ласка, [запитайте на нашому форумі] (https://discuss.privacyguides.net/latest) і не думайте, що ми не врахували щось, коли складали наші рекомендації, якщо це не вказано тут. Коли ми рекомендуємо проєкт, ми враховуємо та обговорюємо багато факторів, і документування кожного з них є постійним процесом.

</div>

- Повинен підтримувати [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- [Мінімізація QNAME](advanced/dns-overview.md#what-is-qname-minimization).
- Дозвіл відключити [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs).
- Віддавайте перевагу підтримці [anycast,](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) або підтримці геонавігації.

## Native Operating System Support

### Android

Android 9 і вище підтримує DNS через TLS. Налаштування можна знайти тут: **Налаштування** &rarr; **Мережа & Інтернет** &rarr; **Приватний DNS**.

### Apple Devices

Останні версії iOS, iPadOS, tvOS та macOS підтримують як DoT, так і DoH. Обидва протоколи підтримуються нативно через [профілі конфігурації](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) або через [API налаштувань DNS](https://developer.apple.com/documentation/networkextension/dns_settings).

Після встановлення профілю конфігурації або програми, яка використовує API налаштувань DNS, можна вибрати конфігурацію DNS. Якщо VPN активна, при вирішенні в тунелі VPN будуть використовуватися налаштування DNS VPN, а не ваші загальносистемні налаштування.

#### Підписані профілі

Apple не надає власного інтерфейсу для створення зашифрованих профілів DNS. [Secure DNS profile creator](https://dns.notjakob.com/tool.html) — неофіційний інструмент для створення власних зашифрованих DNS профілів, які, однак, не будуть підписані. Підписаним профілям надається перевага; підпис підтверджує походження профілю і допомагає забезпечити цілісність профілів. Підписаним профілям конфігурації присвоюється зелена мітка "Перевірено". Для отримання додаткової інформації про підписання коду див. [Про підписання коду](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html). **Signed profiles** are offered by [AdGuard](https://adguard.com/en/blog/encrypted-dns-ios-14.html), [NextDNS](https://apple.nextdns.io), and [Quad9](https://quad9.net/news/blog/ios-mobile-provisioning-profiles).

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

`systemd-resolved`, за якою багато дистрибутивів Linux здійснюють вирішення своїх DNS-пошуків, поки що не [підтримують DoH](https://github.com/systemd/systemd/issues/8639). Якщо ви хочете використовувати DoH, вам потрібно встановити проксі на кшталт [dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy) і [налаштувати його] (https://wiki.archlinux.org/title/Dnscrypt-proxy), щоб він приймав усі DNS-запити від вашого системного розв'язувача і перенаправляв їх через HTTPS.

</div>

## Encrypted DNS Proxies

Програмне забезпечення для проксі-серверів із зашифрованим DNS надає локальний проксі-сервер для перенаправлення на [незашифрованого DNS](advanced/dns-overview.md#unencrypted-dns). Зазвичай він використовується на платформах, які не підтримують [зашифрований DNS](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ align=right }
![RethinkDNS logo](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** - клієнт для Android з відкритим вихідним кодом, що підтримує [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), [DNS-over-TLS](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) і DNS Proxy, а також кешування DNS-відповідей, локальне ведення логів DNS-запитів і може використовуватися в якості фаєрвола.

[:octicons-home-16: Homepage](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

### dnscrypt-proxy

<div class="admonition recommendation" markdown>

![dnscrypt-proxy logo](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**dnscrypt-proxy** - це DNS-проксі з підтримкою [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh) та [Anonymized DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

<div class="admonition warning" markdown>
<p class="admonition-title">The anonymized DNS feature does <a href="advanced/dns-overview.md#why-shouldnt-i0-use-encrypted-dns"><strong>not</strong></a> anonymize other network traffic.</p>
</div>

[:octicons-repo-16: Repository](https://github.com/DNSCrypt/dnscrypt-proxy){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

## Self-hosted Solutions

Самостійно розміщене рішення DNS корисно для забезпечення фільтрації на контрольованих платформах, таких як Smart TV та інші пристрої IoT, оскільки не потрібно клієнтське програмне забезпечення.

### AdGuard Home

<div class="admonition recommendation" markdown>

![AdGuard Home logo](assets/img/dns/adguard-home.svg){ align=right }

**AdGuard Home** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

AdGuard Home має відшліфований веб-інтерфейс для перегляду аналітики та керування заблокованим контентом.

[:octicons-home-16: Домашня сторінка](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Політика конфіденційності" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=Документація}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Вихідний код" }

</details>

</div>

### Pi-hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](assets/img/dns/pi-hole.svg){ align=right }

**Pi-hole** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

Pi-hole розроблений для розміщення на Raspberry Pi, але він не обмежується цим обладнанням. Програмне забезпечення має зручний веб-інтерфейс для перегляду аналітики та управління заблокованим контентом.

[:octicons-home-16: Homepage](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Source Code" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title=Contribute }

</details>

</div>

[^1]: AdGuard зберігає агреговані показники продуктивності своїх DNS-серверів, а саме: кількість завершених запитів до певного сервера, кількість заблокованих запитів і швидкість обробки запитів. Вони також ведуть і зберігають базу даних доменів, до яких надходили запити протягом останніх 24 годин. "Нам потрібна ця інформація, щоб виявляти та блокувати нові трекери та загрози". "Ми також фіксуємо, скільки разів той чи інший трекер був заблокований. Нам потрібна ця інформація, щоб видалити застарілі правила з наших фільтрів". [https://adguard.com/en/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: Cloudflare збирає та зберігає лише обмежену кількість даних DNS-запитів, які надсилаються до вирішувача 1.1.1.1. Сервіс 1.1.1.1 не реєструє особисті дані, а основна частина обмежених неперсоніфікованих даних запитів зберігається лише протягом 25 годин. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: Control D веде журнали лише для преміум-вирішувачів зі спеціальними профілями DNS. Безкоштовні розв'язувачі не логують дані. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: DNS-сервіс Mullvad доступний обом підписникам та не підписникам Mullvad VPN. У їхній політиці конфіденційності чітко зазначено, що вони не реєструють DNS-запити жодним чином. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^5]: When used with an account, NextDNS will enable insights and logging features by default (as some features require it). You can choose retention time and log storage location for any logs you choose to keep, or disable logs altogether. If used without an account, no data is logged. [https://nextdns.io/privacy](https://nextdns.io/privacy)
[^6]: Quad9 збирає деякі дані з метою моніторингу загроз та реагування на них. Потім ці дані можуть бути змішані та поширені, наприклад, з метою дослідження безпеки. Quad9 не збирає і не записує IP-адреси або інші дані, які вони вважають особистими. [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
