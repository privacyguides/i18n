---
title: "چارەسەرکەرانی DNS"
icon: material/dns
description: ئەمانە هەندێک لە دابینکەرانی DNSـی شفرکراون، کە پێشنیاری بەکارهێنانیان دەکەین. بۆ ڕزگارت بوون لە شێوەپێدراوە بنەڕەتیکانی ISPـیەکەت.
cover: dns.webp
---

DNSـی شفرکراو تەنها دەبێت بەکار بهێنرێت لەگەڵ ڕاژەکاری لایەنی سێیەم بۆ تێپەڕاندنی [قەدەغەکردنێکی DNSـی](https://en.wikipedia.org/wiki/DNS_blocking) سادە. کاتێک دڵنیا دەبیت کە هیچ دەرئەنجامێک نابێت. DNSـی شفرکراو یارمەتیت نادات لە شاردنەوەی هیچ یەکێک لە چالاکیەکانی گەڕانت.

[دەربارەی DNS زیاتر فێربە:material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## دابینکەرانی پێشنیارکراو

| دابینکەری DNS                                                              | سیاسەتی تایبەتێتـی                                                                                   | پڕۆتۆکۆڵەکان                                                                 | هەڵگرتنی تۆمار     | ECS            | پاڵاوتن                                                                                                                                                |
| -------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ------------------ | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [**AdGuard**](https://adguard.com/en/adguard-dns/overview.html)            | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                               | Cleartext <br> DoH/3 <br> DoT <br> DoQ <br> DNSCrypt | هەندێک[^1]         | Yes            | Based on personal configuration. لیستی پاڵاوتنی بەکارهێنراو لێرە دەدۆزرێتەوە. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) | Cleartext <br> DoH <br> DoT                                      | هەندێک[^2]         | نەخێر          | Based on personal configuration.                                                                                                                       |
| [**Control D**](https://controld.com/free-dns)                             | [:octicons-link-external-24:](https://controld.com/privacy)                                          | Cleartext <br> DoH/3 <br> DoT <br> DoQ                     | ئارەزوومەندانە[^3] | نەخێر          | Based on personal configuration.                                                                                                                       |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy)                    | DoH <br> DoT                                                           | نەخێر[^4]          | نەخێر          | Based on personal configuration. لیستی پاڵاوتنی بەکارهێنراو لێرە دەدۆزرێتەوە. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    |
| [**NextDNS**](https://nextdns.io)                                          | [:octicons-link-external-24:](https://nextdns.io/privacy)                                            | Cleartext <br> DoH/3 <br> DoT <br> DoQ                     | ئارەزوومەندانە[^5] | ئارەزوومەندانە | Based on personal configuration.                                                                                                                       |
| [**Quad9**](https://quad9.net)                                             | [:octicons-link-external-24:](https://quad9.net/privacy/policy)                                      | Cleartext <br> DoH <br> DoT <br> DNSCrypt                  | هەندێک[^6]         | ئارەزوومەندانە | Based on personal configuration, Malware blocking by default.                                                                                          |

### Criteria

**تکایە تێبینی ئەوە بکە کە ئێمە سەر بە هیچ کام لەو پرۆژانە نین کە پێشنیاری دەکەین.** وە جگە لە [ پێوەرە بنچینەییەکانمان](about/criteria.md), ئێمە کۆمەڵێک مەرجی ڕوونمان دامەزراندووە بۆ ئەوەی ڕێگەمان پێبدات پێشنیاری ڕاست بکەین. ئێمە پێشنیاری ئەوە دەکەین کە تۆ خۆت ئاشنا بکەیت لەگەڵ ئەم لیستە پێش هەڵبژاردن و بەکارهێنانی دابینکەرەکە وە لێکۆڵینەوەی خۆت بکەیت بۆ دڵنیابوون لەوەی، کە ئەمە هەڵبژاردنێکی گونجاوە بۆ تۆ.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

ئێمە کار لەسەر دانانی پێوەرە پێناسەکراوەکان دەکەین بۆ هەموو بەشێکی ماڵپەڕەکەمان, وە ئەمە لەوانەیە بگۆڕدرێت. ئەگەر هیچ پرسیارێکت هەیە سەبارەت بە پێوەرەکانی ئێمە. ئەوا تکایە [لە سەکۆکەمان پرسیار بکە](https://discuss.privacyguides.net/latest). وە وادامەنێ کە ئێمە هیچ شتێکمان لەبەرچاو نەگرتوە لە کاتی دروستکردنی پێشنیارەکانمان ئەگەر لە لیستەکە نەبێت. چەندین هۆکار هەن کە لەبەرچاو دەگرین و گفتوگۆیان لەسەر دەکرێت کاتێک پێشنیاری پرۆژەیەک دەکەین. وە تۆمارکردنی هەریەکەیان کارێکی بەردەوامە.

</div>

- پێویستە بشتگیری [DNSSEC](advanced/dns-overview.md#what-is-dnssec) بکات.
- [بچووکردنەوەی QNAME](advanced/dns-overview.md#what-is-qname-minimization).
- ڕێگە بە ناچالاک کردنی [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) بدات.
- پەسند کردنی [Anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) یان پشتگیری "ئاڕاستەی-جوگرافی".

## Native Operating System Support

### Android

ئەندرۆید 9 و سەرووتر پشتگیری DNS دەکەن لە ڕێگەی TLS. ڕێکخستنەکان دەتوانرێ بدۆزرێتەوە لە: **Settings**&rarr;**Network & Internet**&rarr;**Private DNS**.

### Apple Devices

کۆتا وەشەنەکان لە tvOS، iPadOS، iOS لەگەڵ macOS هەموویان پشتگیری لە DoT و DoH دەکەن. هەردوو پرۆتۆکۆلەکە بە شێوەیەکی ڕەسەن پشتگیری دەکرێن لە ڕێگەی [شێوەپێدانی پڕؤفایلەکان](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) یان لە ڕێگەی [ڕێکخستنەکانیDNS API](https://developer.apple.com/documentation/networkextension/dns_settings).

دوای دامەزراندنی شێوەپێدانێکی پڕۆفایل یان کاربەرنامەیەک کە ڕێکخستنەکانی DNS API بەکاردێنێ، دەتوانیت شێوەپێدانی DNS دیاریبکەیت. ئەگەر VPN چالاک بێت، چارەسەری ناو تونێلی VPNـەکە ڕێکخستەنەکانی DNSـی VPNـەکە بەکاردێنیت. نەک ڕێکخستەنە فراوانەکەی سیستەمەکەت.

#### پرۆفایلە واژۆکراوەکان

Apple ڕووکارێکی بنەچەیی دابین ناکات بۆ دروستکردنی پرۆفایلی DNSـی شفرەکراو. [ دروستکەری پرۆفایلی DNSـی پارێزراو](https://dns.notjakob.com/tool.html) ئامرازێکی نافەرمییە بۆ دروستکردنی پرۆفایلی DNSـی شفرەکراوی تایبەت بەخۆت، بەڵام هەرچۆنێک بێت ئەوان واژۆ ناکرێن. پرۆڤایلی واژۆکراو پەسندن؛ واژۆکە سەرچاوەی پرۆفایلەکە ڕوون دەکاتەوە و یارمەتیدەرە بۆ دڵنیابوون لە ڕاستی پرۆفایلەکان. نیشانەیەکی "پشتڕاستکراو" بە ڕەنگی سەوز دراوە بە پرۆفایلی شێوەپێدانی واژۆکراو. بۆ زانیاری زیاتر لەسەر هێمای واژۆکان، [ دەربارەی هێمای واژۆکان](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html) ببینە. **Signed profiles** are offered by [AdGuard](https://adguard.com/en/blog/encrypted-dns-ios-14.html), [NextDNS](https://apple.nextdns.io), and [Quad9](https://quad9.net/news/blog/ios-mobile-provisioning-profiles).

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

`systemd-resolved`، کە زۆربەی دابەشکراوانی لینوکس بەکاری دێنن بۆ ئەنجامدانی گەرانی DNSـەکەیان. تاوەکو ئێستا [پشتگیری لە DoH ناکات](https://github.com/systemd/systemd/issues/8639). ئەگەر دەتەوێت DoH بەکاربێنی، ئەوا پێویستت بە دابەزاندی چارەسەرکەرێک هەیە وەک [dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy) هەیە وە [دەستکاری کردنی](https://wiki.archlinux.org/title/Dnscrypt-proxy) بۆ ئەوەی هەموو داواکاریەکانی DNSـەکەت کە لەلایەن سیستەمی چارەسەرکەرەکەت دێت بنێرێدرێت لەڕێگای HTTPSـەوە.

</div>

## Encrypted DNS Proxies

نەرمەواڵەی بریکارانی DNSـی شفرکراو، بریکارێکی ناوخۆیی دابین دەکەن بۆ ئەوەی [چارەسەرکەری DNSـی شفر نەکراو](advanced/dns-overview.md#unencrypted-dns) ڕووی تێ بکات. بەشێوەیەکی گشتی بەکاردەهێنرێت لەسەر ئەو ئامێرانەی، کە لە بنچینەوە پشتگیری لە [DNSـی شفرکراو](advanced/dns-overview.md#what-is-encrypted-dns) ناکەن.

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

## Self-hosted Solutions

سەرپەرشتیکردنی-خودی DNS چارەسەرێکی بەسوودە بۆ دابینکردنی پاڵاوتن بۆ ئامێرە سەرپەرشتی کراوەکانی وەک تەلەڤزیۆنی زیرەک و ئامێرە زیرەکەکانی تر، چونکە پێویستی بە هیچ نەرمەواڵەیەکی ڕاژەخواز نیە.

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

[^1]: AdGuard توانای ئەرک بەجێهێنانی ڕاژەی DNSـەکانیان کۆ دەکەنەوە، بەتایبەتی ژمارەی داواکاریە تەواوەکان بۆ ڕاژەیەکی دیاریکراو، ژمارەی داواکاریە قەدەغەکراوەکان، و خێرایی وەڵامدانەوەی داواکاریەکان. هەروەها ئەوان ئەو بنکە داتایانە هەڵدەگرن و کۆیدەکەنەوە، کە دۆمەینەکانی لێوە داواکراوە لە ماوەی 24 کاتژمێری ڕابردوو. "پێویستمان بەم زانیاریە هەیە بۆ ناسینەوە و ڕاگرتنی شوێنگران و هەڕەشە نوێیەکان" "هەروەها ئێمە تۆماری دەکەین کە چەند جار ئەم یان ئەو شوێنگرە ڕێگری لێکراوە. ئێمە پێویستمان بەم زانیاریە هەیە بۆ سڕینەوەی یاسای بەرسەرچوو لە پاڵاوتنەکانمان." [https://adguard.com/en/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: Cloudflare تەنها ئەو داتایە سنووردارە کۆدەکاتەوە و هەڵیدەگرێت، کە نێردراون لایەن DNS بۆ چارەسەرکەری 1.1.1.1. خزمەتگوزاری چارەسەرکەری 1.1.1.1 داتای کەسی تۆمار ناکات، وە ئەو بەشە داتایە سنووردارە نا-کەسیە ناسراوانە تەنها بۆ ماوەی 25 کاتژمێر هەڵدەگیرێن دەکرێت. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: Control D تەنها داتای ناسینەوە بۆ ئەو کەسانە تۆمار دەکات کە بەژداربووی چارەسەرکانیانن، وە پرۆفایلی DNSـی تایبەتیان هەیە. چارەسەرکەرە بەخۆڕایەکان داتا تۆمار ناکەن. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: خزمەتگوزاری DNSـی Mullvad بەردەستە بۆ هەردووک لە بەکارهێنەری بەرژداربوو و نابەژداربوو. سیاسەتی تایبەتێتی ئەوان بە ڕوونی بانگەشەی ئەوە دەکات، کە بە هیچ شێوازێک داواکاریەکانی DNSـەکانیان تۆمار ناکەن. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^5]: NextDNS can provide insights and logging features on an opt-out basis. دەتوانی ماوەی هێشتنەوە هەڵبژێریت و ئەو شوێنی هەڵگرتنی تۆمارەکان دیاری بکەیت بۆ هەر جۆرێکی تۆمارەکە کە هەڵیدەبژێریت بۆ هێشتنەوە. ئەگەر بە تایبەتی داوانەکرابێت، هیچ داتایەک تۆمار ناکرێت. [https://nextdns.io/privacy](https://nextdns.io/privacy)
[^6]: Quad9 هەندێک داتا کۆ دەکاتەوە بۆ مەبەستی ئاگاداربوون لە هەڕەشە و وەڵامدانەوە. ئەو داتایە لەوانەیە دواتر دووبارە ببەسترێتەوە و هاوبەشی پێ بکرێت، بۆ مەبەستی لێکۆڵینەوەی ئاسایشی. Quad9 ناونیشانی IP یان ئەو داتایانەی تر کۆناکاتەوە و تۆماریان ناکات، کە بە داتای ناسینەوەی کەسی دادەنێرن. [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
