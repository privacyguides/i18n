---
title: "محلِّلات أنظمة أسماء النطاقات (DNS)"
icon: material/dns
description: هنا بعض موفِّري خدمة أنظمة أسماء النطاقات المعمَّاة لتستبدل ما ضبطه لك موفِّر خدمة الإنترنت.
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

ينبغي استخدام أنظمة أسماء النطاقات المعمَّاة الموجودة في خوادم جهات خارجية فقط لتجاوز [حظرها](https://en.wikipedia.org/wiki/DNS_blocking)، وذلك إن تيقَّنت من أن ذلك ليست له عواقب. لن يخفي استخدام نظام أسماء نطاق معمًّى ما تتصفَّح.

[استزد علمًا عن أنظمة أسماء النطاقات :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## موفِّرو الخدمة الموصى بهم

These are our favorite public DNS resolvers based on their privacy and security characteristics, and their worldwide performance. Some of these services offer basic DNS-level blocking of malware or trackers depending on the server you choose, but if you want to be able to see and customize what is blocked you should use a dedicated DNS filtering product instead.

| الموفِّر                                                                 | سياسة الخصوصية                                                                                       | الموافيق                                 | تسجيل الأنشطة                                                              | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | التصفية                                                                                                                                      | Signed Apple Profile                                                                                                     |
| ------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------- | ---------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| [**AdGuard Public DNS**](https://adguard-dns.io/en/public-dns.html)      | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                               | Cleartext   DoH/3   DoT   DoQ   DNSCrypt | بعض منه <sup id="fnref:1"><a href="#fn:1" class="footnote-ref">١</a></sup> | Anonymized                                                     | Based on server choice. لك العثور على قائمة التصفيات المستخدمة هنا. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) | Yes [:octicons-link-external-24:](https://adguard.com/en/blog/encrypted-dns-ios-14.html)                                 |
| [**كلاودفلير**](https://developers.cloudflare.com/1.1.1.1/setup)         | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) | Cleartext   DoH/3   DoT                  | بعض منه <sup id="fnref:2"><a href="#fn:2" class="footnote-ref">٢</a></sup> | لا يوجد                                                        | Based on server choice.                                                                                                                      | No [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846) |
| [**Control D Free DNS**](https://controld.com/free-dns)                  | [:octicons-link-external-24:](https://controld.com/privacy)                                          | Cleartext   DoH/3   DoT   DoQ            | اختياري<sup id="fnref:3"><a href="#fn:3" class="footnote-ref">٣</a></sup>  | لا يوجد                                                        | Based on server choice.                                                                                                                      | Yes [:octicons-link-external-24:](https://docs.controld.com/docs/macos-platform)                                         |
| [**dns0.eu**](https://dns0.eu)                                           | [:octicons-link-external-24:](https://dns0.eu/privacy)                                               | Cleartext   DoH/3   DoH   DoT   DoQ      | لا يوجد                                                                    | Anonymized                                                     | Based on server choice.                                                                                                                      | Yes [:octicons-link-external-24:](https://dns0.eu/zero.dns0.eu.mobileconfig)                                             |
| [**ملفاد**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy)                    | DoH   DoT                                | لا يوجد<sup id="fnref:4"><a href="#fn:4" class="footnote-ref">٤</a></sup>  | لا يوجد                                                        | Based on server choice. لك العثور على قائمة التصفيات المستخدمة هنا. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    | Yes [:octicons-link-external-24:](https://mullvad.net/en/blog/profiles-to-configure-our-encrypted-dns-on-apple-devices)  |
| [**كواد٩**](https://quad9.net)                                           | [:octicons-link-external-24:](https://quad9.net/privacy/policy)                                      | Cleartext   DoH   DoT   DNSCrypt         | Some[^5]                                                                   | اختياري                                                        | Based on server choice, malware blocking by default.                                                                                         | Yes [:octicons-link-external-24:](https://quad9.net/news/blog/ios-mobile-provisioning-profiles)                          |

## Self-Hosted DNS Filtering

تتيح الاستضافة الذاتية لنظام تسمية نطاقات التصفية في المنصَّات المتحكَّم بها، مثل أجهزة التلفاز الذكية وغيرها من أجهزة إنترنت الأشياء، وذلك لأن جهة العميل لا تحتاج لأي برمجيات.

### Pi-hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](assets/img/dns/pi-hole.svg){ align=right }

**Pi-hole** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

صُمِّم باي-هول ليستضاف في جهاز راسبيري باي، ولكنَّه ليس محدودًا به. لهذه البرمجية واجهة وِب سهلة الاستخدام ترى فيها المعلومات وتدير ما حُظر.

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

لدى آدجارد هوم واجهة وِب متقنة الصنع ترى فيها المعلومات وتدير ما حُظر.

[:octicons-home-16: الصفحة الرئيسة](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="سياسة الخصوصية" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=التوثيق}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="رمز المصدر" }

</details>

</div>

## Cloud-Based DNS Filtering

These DNS filtering solutions offer a web dashboard where you can customize the blocklists to your exact needs, similarly to a Pi-hole. These services are usually easier to set up and configure than self-hosted services like the ones above, and can be used more easily across multiple networks (self-hosted solutions are typically restricted to your home/local network unless you set up a more advanced configuration).

### كنترول دي

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

### نكست‌دي‌إن‌إس

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

توفِّر برمجيات التوسُّط بين أنظمة تسمية النطاقات وسيطًا محليًّا [لمحلِّل نظام التسمية غير المعمَّى](advanced/dns-overview.md#unencrypted-dns) لتوجِّه الطلبات له. Typically, it is used on platforms that don't natively support [encrypted DNS](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ align=left }
![RethinkDNS logo](assets/img/android/rethinkdns-dark.svg#only-dark){ align=left }

**ريثنك‌دي‌إن‌إس** هو عميل أندرويد مفتوح المصدر يدعم [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh) و [DNS-over-TLS](advanced/dns-overview.md#dns-over-tls-dot) و [DNSCrypt](advanced/dns-overview.md#dnscrypt) والتوسُّط لأنظمة تسمية النطاقات وتخزين استجاباتها مؤقَّتًا وتسجيل استعلاماتها محليًّا، ويُستخدم جدارًا ناريًّا أيضًا.

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

![dnscrypt-proxy logo](assets/img/dns/dnscrypt-proxy.svg){ align=left }

**دي‌إن‌إس‌كربت-بروكسي** هو وسيط أنظمة تسمية نطاقات يدعم [DNSCrypt](advanced/dns-overview.md#dnscrypt) و [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh) [وأنظمة تسمية النطاقات المُجَهَّلة](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

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

**عليك التنبُّه لأننا لسنا ذوي صلة بأيٍّ من المشاريع التي نوصي بها**، وزيادةً على [معاييرنا القياسية](about/criteria.md) فقد طوَّرنا مجموعة متطلَّبات تتيح لنا توصية توصيات موضوعية. ينبغي لك الاطِّلاع على هذه القائمة قبل الاختيار منها، وابحث بنفسك لتتيقَّن من أن ما اخترت يناسبك.

### Minimum Requirements

- [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- [تدنية الأسماء المؤهَّلة](advanced/dns-overview.md#what-is-qname-minimization).
- Anonymize [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) or disable it by default.
- يفضِّل دعم [anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) أو دعم geo-steering.

[^1]: تخزِّن آدجارد قياسات الأداء المجمَّعة من خوادم أنظمة تسمية نطاقاتهم، وتتضمَّن عدد الطلبات المكتملة لكلِّ خادم، وعدد الطلبات المحظورة، وسرعة معالجة الطلبات. وتخزِّن أيضًا قاعدة بيانات بها النطاقات المطلوبة خلال آخر ٢٤ ساعة. «نحتاج هذه المعلومات لنتحرَّى ونحظر المتتبِّعات والمخاطر الجديدة.» «وكذلك نسجِّل عدد المرات التي تُحظر فيها المتتبِّعات. نحتاج هذه المعلومات لنزيل القواعد القديمة من تصفياتنا.» [https://adguard.com/en/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: تجمِّع وتخزِّن كلاودفلير عددًا قليلًا من استعلامات أنظمة تسمية النطاقات المرسلة للمحلِّل ١٫١٫١٫١. لا تسجِّل خدمة المحلِّل ١٫١٫١٫١ بيانات شخصيةً، وغالب ما تسِّجل من بيانات لا تعرِّف الأشخاص تخزَّن مدَّة ٢٥ ساعةً لا أكثر. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: تسجِّل كنترول دي البيانات من المحلِّلات المدفوعة التي لها ملفَّات تعريف مخصَّصة فقط. المحلِّلات المجَّانية لا تسجِّل بيانات. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: خدمة أنظمة تسمية النطاقات من ملفاد متاحة للمشتركين في خدمة الشبكة الخاصة الافتراضية ولغير المشتركين كذلك. تزعم سياسة خصوصيتهم صريحًا أنهم لا يسجِّلون طلبات أنظمة تسمية النطاقات أبدًا. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^5]: تجمع كواد٩ بعض البيانات لمراقبة المخاطر والاستجابات. ويمكن لتلك البيانات أن تُخلط وتُشارك، وغرض ذلك قد يكون لأبحاث الأمن. لا تجمع كواد٩ ولا تسجِّل عناوين IP أو أيَّ بيانات تصنِّفها معرِّفةً شخصيًّا. [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
