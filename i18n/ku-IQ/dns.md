---
title: "چارەسەرکەرانی DNS"
icon: material/dns
description: ئەمانە هەندێک لە دابینکەرانی DNSـی شفرکراون، کە پێشنیاری بەکارهێنانیان دەکەین. بۆ ڕزگارت بوون لە شێوەپێدراوە بنەڕەتیکانی ISPـیەکەت.
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

DNSـی شفرکراو تەنها دەبێت بەکار بهێنرێت لەگەڵ ڕاژەکاری لایەنی سێیەم بۆ تێپەڕاندنی [قەدەغەکردنێکی DNSـی](https://en.wikipedia.org/wiki/DNS_blocking) سادە. کاتێک دڵنیا دەبیت کە هیچ دەرئەنجامێک نابێت. DNSـی شفرکراو یارمەتیت نادات لە شاردنەوەی هیچ یەکێک لە چالاکیەکانی گەڕانت.

[دەربارەی DNS زیاتر فێربە:material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## دابینکەرانی پێشنیارکراو

These are our favorite public DNS resolvers based on their privacy and security characteristics, and their worldwide performance. Some of these services offer basic DNS-level blocking of malware or trackers depending on the server you choose, but if you want to be able to see and customize what is blocked you should use a dedicated DNS filtering product instead.

| دابینکەری DNS                                                              | سیاسەتی تایبەتێتـی                                                                                   | پڕۆتۆکۆڵەکان                             | هەڵگرتنی تۆمار     | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | پاڵاوتن                                                                                                                                       | Signed Apple Profile                                                                                                     |
| -------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------- | ------------------ | -------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| [**AdGuard Public DNS**](https://adguard-dns.io/en/public-dns.html)        | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                               | Cleartext   DoH/3   DoT   DoQ   DNSCrypt | هەندێک[^1]         | Anonymized                                                     | Based on server choice. لیستی پاڵاوتنی بەکارهێنراو لێرە دەدۆزرێتەوە. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) | Yes [:octicons-link-external-24:](https://adguard.com/en/blog/encrypted-dns-ios-14.html)                                 |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) | Cleartext   DoH/3   DoT                  | هەندێک[^2]         | نەخێر                                                          | Based on server choice.                                                                                                                       | No [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846) |
| [**Control D Free DNS**](https://controld.com/free-dns)                    | [:octicons-link-external-24:](https://controld.com/privacy)                                          | Cleartext   DoH/3   DoT   DoQ            | ئارەزوومەندانە[^3] | نەخێر                                                          | Based on server choice.                                                                                                                       | Yes [:octicons-link-external-24:](https://docs.controld.com/docs/macos-platform)                                         |
| [**dns0.eu**](https://dns0.eu)                                             | [:octicons-link-external-24:](https://dns0.eu/privacy)                                               | Cleartext   DoH/3   DoH   DoT   DoQ      | نەخێر              | Anonymized                                                     | Based on server choice.                                                                                                                       | Yes [:octicons-link-external-24:](https://dns0.eu/zero.dns0.eu.mobileconfig)                                             |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy)                    | DoH   DoT                                | نەخێر[^4]          | نەخێر                                                          | Based on server choice. لیستی پاڵاوتنی بەکارهێنراو لێرە دەدۆزرێتەوە. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    | Yes [:octicons-link-external-24:](https://mullvad.net/en/blog/profiles-to-configure-our-encrypted-dns-on-apple-devices)  |
| [**Quad9**](https://quad9.net)                                             | [:octicons-link-external-24:](https://quad9.net/privacy/policy)                                      | Cleartext   DoH   DoT   DNSCrypt         | Some[^5]           | ئارەزوومەندانە                                                 | Based on server choice, malware blocking by default.                                                                                          | Yes [:octicons-link-external-24:](https://quad9.net/news/blog/ios-mobile-provisioning-profiles)                          |

## Self-Hosted DNS Filtering

سەرپەرشتیکردنی-خودی DNS چارەسەرێکی بەسوودە بۆ دابینکردنی پاڵاوتن بۆ ئامێرە سەرپەرشتی کراوەکانی وەک تەلەڤزیۆنی زیرەک و ئامێرە زیرەکەکانی تر، چونکە پێویستی بە هیچ نەرمەواڵەیەکی ڕاژەخواز نیە.

### Pi-hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](assets/img/dns/pi-hole.svg){ align=right }

**Pi-hole** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

Pi-hole وا دروست کراوە کە لەسەر Rasberry Pi سەرپەرشتی بکرێت ، بەڵام سنووردار نییە بۆ ئەم ڕەقەواڵەیە بە تەنها. نەرمەواڵەکە ڕووکارێکی ڕێک و پێک و ئاسان لە بەکارهێان دەبەخشێت بۆ بینینی تێگەیشتنەکان و بەڕێوەبردنی ناوەڕۆکە قەدەغەکراوەکان.

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

AdGuard Home ڕووکارێکی ڕێک و پێک دەبەخشێتە ماڵپەرەکەی بۆ بینینی تێگەیشتنەکان و بەڕێوەنردنی ناوەڕۆکە قەدەغەکراوەکان.

[:octicons-home-16: پەڕەی سەرەکی](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="سیاسەتی تایبەتێتی" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=دۆکیمێنتەکان}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="سەرچاوەی کۆد" }

</details>

</div>

## Cloud-Based DNS Filtering

These DNS filtering solutions offer a web dashboard where you can customize the blocklists to your exact needs, similarly to a Pi-hole. These services are usually easier to set up and configure than self-hosted services like the ones above, and can be used more easily across multiple networks (self-hosted solutions are typically restricted to your home/local network unless you set up a more advanced configuration).

### Control D

<div class="admonition recommendation" markdown>

![Control D logo](assets/img/dns/control-d.svg){ align=right }

**Control D** is a customizable DNS service which lets you block security threats, unwanted content, and advertisements on a DNS level. In addition to their paid plans, they offer a number of preconfigured DNS resolvers you can use for free.

[:octicons-home-16: Homepage](https://controld.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://controld.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.controld.com/docs/getting-started){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/Control-D-Inc/ctrld){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-apple: macOS](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-linux: Linux](https://docs.controld.com/docs/ctrld)
- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.controld.setuputility)
- [:simple-appstore: App Store](https://apps.apple.com/app/1518799460)
- [:simple-github: GitHub](https://github.com/Control-D-Inc/ctrld/releases/tag/v1.3.5)

</details>

</div>

### NextDNS

<div class="admonition recommendation" markdown>

![NextDNS logo](assets/img/dns/nextdns.svg){ align=right }

**NextDNS** is a customizable DNS service which lets you block security threats, unwanted content, and advertisements on a DNS level. They offer a fully functional free plan for limited use.

[:octicons-home-16: Homepage](https://nextdns.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextdns.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.nextdns.io){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/nextdns/nextdns){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://github.com/nextdns/nextdns/wiki/Windows)
- [:simple-apple: macOS](https://apps.apple.com/us/app/nextdns/id1464122853)
- [:simple-linux: Linux](https://github.com/nextdns/nextdns/wiki)
- [:simple-appstore: App Store](https://apps.apple.com/app/nextdns/id1463342498)
- [:simple-github: GitHub](https://github.com/nextdns/nextdns/releases)

</details>

</div>

When used with an account, NextDNS will enable insights and logging features by default (as some features require it). You can choose retention time and log storage location for any logs you choose to keep, or disable logs altogether.

NextDNS's free plan is fully functional, but should not be relied upon for security or other critical filtering applications, because after 300,000 DNS queries in a month all filtering, logging, and other account-based functionality is disabled. It can still be used as a regular DNS provider after that point, so your devices will continue to function and make secure queries via DNS-over-HTTPS, just without your filter lists.

NextDNS also offers public DNS-over-HTTPS service at `https://dns.nextdns.io` and DNS-over-TLS/QUIC at `dns.nextdns.io`, which are available by default in Firefox and Chromium, and subject to their default no-logging [privacy policy](https://nextdns.io/privacy).

## Encrypted DNS Proxies

نەرمەواڵەی بریکارانی DNSـی شفرکراو، بریکارێکی ناوخۆیی دابین دەکەن بۆ ئەوەی [چارەسەرکەری DNSـی شفر نەکراو](advanced/dns-overview.md#unencrypted-dns) ڕووی تێ بکات. Typically, it is used on platforms that don't natively support [encrypted DNS](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ align=right }
![RethinkDNS logo](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** ڕاژەیەکی سەرچاوە - کراوەی ئەندرۆیدە، کە پشتگیری لە [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh)، [DNS-over-TLS](advanced/dns-overview.md#dns-over-tls-dot)، [DNSCrypt](advanced/dns-overview.md#dnscrypt) و بریکاری DNS دەکات، لەگەڵ کۆکردنەەی وەڵامدانەوەکانی DNS بە شێوەیەکی کاتی، وە تۆمارکردنی داواکاریەکانی DNS. هەروەها دەتوانرێت وەک ئاگرەدیوار بەرکار بهێندرێت.

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

**dnscrypt-proxy** بریکارێکی DNSـە پشتگیری دەکات لە [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), وە [DNSـی نەناسراو](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

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

## Criteria

**تکایە تێبینی ئەوە بکە کە ئێمە سەر بە هیچ کام لەو پرۆژانە نین کە پێشنیاری دەکەین.** وە جگە لە [ پێوەرە بنچینەییەکانمان](about/criteria.md), ئێمە کۆمەڵێک مەرجی ڕوونمان دامەزراندووە بۆ ئەوەی ڕێگەمان پێبدات پێشنیاری ڕاست بکەین. ئێمە پێشنیاری ئەوە دەکەین کە تۆ خۆت ئاشنا بکەیت لەگەڵ ئەم لیستە پێش هەڵبژاردن و بەکارهێنانی دابینکەرەکە وە لێکۆڵینەوەی خۆت بکەیت بۆ دڵنیابوون لەوەی، کە ئەمە هەڵبژاردنێکی گونجاوە بۆ تۆ.

### Minimum Requirements

- [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- [بچووکردنەوەی QNAME](advanced/dns-overview.md#what-is-qname-minimization).
- Anonymize [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) or disable it by default.
- پەسند کردنی [Anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) یان پشتگیری "ئاڕاستەی-جوگرافی".

[^1]: AdGuard توانای ئەرک بەجێهێنانی ڕاژەی DNSـەکانیان کۆ دەکەنەوە، بەتایبەتی ژمارەی داواکاریە تەواوەکان بۆ ڕاژەیەکی دیاریکراو، ژمارەی داواکاریە قەدەغەکراوەکان، و خێرایی وەڵامدانەوەی داواکاریەکان. هەروەها ئەوان ئەو بنکە داتایانە هەڵدەگرن و کۆیدەکەنەوە، کە دۆمەینەکانی لێوە داواکراوە لە ماوەی 24 کاتژمێری ڕابردوو. "پێویستمان بەم زانیاریە هەیە بۆ ناسینەوە و ڕاگرتنی شوێنگران و هەڕەشە نوێیەکان" "هەروەها ئێمە تۆماری دەکەین کە چەند جار ئەم یان ئەو شوێنگرە ڕێگری لێکراوە. ئێمە پێویستمان بەم زانیاریە هەیە بۆ سڕینەوەی یاسای بەرسەرچوو لە پاڵاوتنەکانمان." [https://adguard.com/en/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: Cloudflare تەنها ئەو داتایە سنووردارە کۆدەکاتەوە و هەڵیدەگرێت، کە نێردراون لایەن DNS بۆ چارەسەرکەری 1.1.1.1. خزمەتگوزاری چارەسەرکەری 1.1.1.1 داتای کەسی تۆمار ناکات، وە ئەو بەشە داتایە سنووردارە نا-کەسیە ناسراوانە تەنها بۆ ماوەی 25 کاتژمێر هەڵدەگیرێن دەکرێت. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: Control D تەنها داتای ناسینەوە بۆ ئەو کەسانە تۆمار دەکات کە بەژداربووی چارەسەرکانیانن، وە پرۆفایلی DNSـی تایبەتیان هەیە. چارەسەرکەرە بەخۆڕایەکان داتا تۆمار ناکەن. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: خزمەتگوزاری DNSـی Mullvad بەردەستە بۆ هەردووک لە بەکارهێنەری بەرژداربوو و نابەژداربوو. سیاسەتی تایبەتێتی ئەوان بە ڕوونی بانگەشەی ئەوە دەکات، کە بە هیچ شێوازێک داواکاریەکانی DNSـەکانیان تۆمار ناکەن. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^5]: Quad9 هەندێک داتا کۆ دەکاتەوە بۆ مەبەستی ئاگاداربوون لە هەڕەشە و وەڵامدانەوە. ئەو داتایە لەوانەیە دواتر دووبارە ببەسترێتەوە و هاوبەشی پێ بکرێت، بۆ مەبەستی لێکۆڵینەوەی ئاسایشی. Quad9 ناونیشانی IP یان ئەو داتایانەی تر کۆناکاتەوە و تۆماریان ناکات، کە بە داتای ناسینەوەی کەسی دادەنێرن. [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
