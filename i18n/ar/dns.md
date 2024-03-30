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

| الموفِّر                                                                 | سياسة الخصوصية                                                                                       | الموافيق                                                                     | تسجيل الأنشطة                                                              | ECS     | التصفية                                                                                                                                               |
| ------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | -------------------------------------------------------------------------- | ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**آدجارد**](https://adguard.com/en/adguard-dns/overview.html)           | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                               | Cleartext <br> DoH/3 <br> DoT <br> DoQ <br> DNSCrypt | بعض منه <sup id="fnref:1"><a href="#fn:1" class="footnote-ref">١</a></sup> | Yes     | Based on personal configuration. لك العثور على قائمة التصفيات المستخدمة هنا. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) |
| [**كلاودفلير**](https://developers.cloudflare.com/1.1.1.1/setup)         | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) | Cleartext <br> DoH/3 <br> DoT                                    | بعض منه <sup id="fnref:2"><a href="#fn:2" class="footnote-ref">٢</a></sup> | لا يوجد | Based on personal configuration.                                                                                                                      |
| [**كنترول دي**](https://controld.com/free-dns)                           | [:octicons-link-external-24:](https://controld.com/privacy)                                          | Cleartext <br> DoH/3 <br> DoT <br> DoQ                     | اختياري<sup id="fnref:3"><a href="#fn:3" class="footnote-ref">٣</a></sup>  | لا يوجد | Based on personal configuration.                                                                                                                      |
| [**ملفاد**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy)                    | DoH <br> DoT                                                           | لا يوجد<sup id="fnref:4"><a href="#fn:4" class="footnote-ref">٤</a></sup>  | لا يوجد | Based on personal configuration. لك العثور على قائمة التصفيات المستخدمة هنا. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    |
| [**نكست‌دي‌إن‌إس**](https://nextdns.io)                                  | [:octicons-link-external-24:](https://nextdns.io/privacy)                                            | Cleartext <br> DoH/3 <br> DoT <br> DoQ                     | اختياري<sup id="fnref:5"><a href="#fn:5" class="footnote-ref">٥</a></sup>  | اختياري | Based on personal configuration.                                                                                                                      |
| [**كواد٩**](https://quad9.net)                                           | [:octicons-link-external-24:](https://quad9.net/privacy/policy)                                      | Cleartext <br> DoH <br> DoT <br> DNSCrypt                  | بعض منه<sup id="fnref:6"><a href="#fn:6" class="footnote-ref">٦</a></sup>  | اختياري | Based on personal configuration, Malware blocking by default.                                                                                         |

### Criteria

**عليك التنبُّه لأننا لسنا ذوي صلة بأيٍّ من المشاريع التي نوصي بها**، وزيادةً على [معاييرنا القياسية](about/criteria.md) فقد طوَّرنا مجموعة متطلَّبات تتيح لنا توصية توصيات موضوعية. ينبغي لك الاطِّلاع على هذه القائمة قبل الاختيار منها، وابحث بنفسك لتتيقَّن من أن ما اخترت يناسبك.

- يجب أن يدعم [إضافات الأمان لأنظمة أسماء النطاقات](advanced/dns-overview.md#what-is-dnssec).
- [تدنية الأسماء المؤهَّلة](advanced/dns-overview.md#what-is-qname-minimization).
- يسمح بتعطيل [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs).
- يفضِّل دعم [anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) أو دعم geo-steering.

## Native Operating System Support

### Android

يدعم أندرويد ٩ وما بعده أنظمة أسماء النطاقات عبر أمن طبقة النقل (DNS over TLS). تجد هذا الإعداد في: **الإعدادات** ← ** الشبكة والإنترنت ** ← **نظام أسماء نطاقات خاص**.

### Apple Devices

تدعم آخر إصدارات آي‌أو‌إس و آيباد‌أو‌إس و تي‌في‌أو‌إس و ماك‌أو‌إس أنظمة DoT و DoH. يوجد دعم أصيل لهذه الموافيق باستخدام [ملفَّات تعريف الضبط](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) أو باستخدام [واجهة برمجة إعدادات نظام تسمية النطاقات](https://developer.apple.com/documentation/networkextension/dns_settings).

لك اختيار ضبط نظام تسمية النطاقات بعد تثبيت ملفِّ تعريف ضبط أو تثبيت تطبيق يستخدم واجهة برمجة إعدادات نظام تسمية النطاقات. إن كانت شبكة خاصَّة افتراضية (VPN) مفعَّلةً فسوف تُحلَّل الاتصالات داخلها باستخدام نظام تسمية نطاقاتها وليس باستخدام إعدادات نظامك.

#### ملفَّات التعريف الموقَّعة

لا تتيح أبل واجهةً أصيلةً لإنشاء ملفَّات تعريف معمَّاة. [مُنشئ ملفَّات تعريف نظام تسمية النطاقات الآمن](https://dns.notjakob.com/tool.html) هو أداة غير رسمية تتيح لك إنشاء ملفَّات تعريف نظام تسمية النطاقات معمَّاة، ولكن ضع في حسبانك أنها لن توقَّع. تفضَّل ملفَّات التعريف الموقَّعة على غيرها، وذلك ﻷن التوقيع يؤكِّد أصلها وصحَّتها. تعلَّم ملفَّات التعريف الموقَّعة بعلامة «مؤكَّد» خضراء. لتستزيد علمًا عن توقيع الرموز عليك مطالعة [عن توقيع الرموز](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html). **Signed profiles** are offered by [AdGuard](https://adguard.com/en/blog/encrypted-dns-ios-14.html), [NextDNS](https://apple.nextdns.io), and [Quad9](https://quad9.net/news/blog/ios-mobile-provisioning-profiles).

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

[لا يدعم](https://github.com/systemd/systemd/issues/8639) ‹systemd-resolved› ميفاق DoH بعد، وهو ما تستخدمه الكثير من توزيعات لينكس لتبحث في أنظمة تسمية النطاقات. إن أردت استخدام DoH فعليك تثبيت وسيط مثل [dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy) [وضبطه](https://wiki.archlinux.org/title/Dnscrypt-proxy) ليستلم كلَّ استعلامات أنظمة تسمية النطاقات من محلِّل نظامك ويوجِّههم عبر HTTPS.

</div>

## Encrypted DNS Proxies

توفِّر برمجيات التوسُّط بين أنظمة تسمية النطاقات وسيطًا محليًّا [لمحلِّل نظام التسمية غير المعمَّى](advanced/dns-overview.md#unencrypted-dns) لتوجِّه الطلبات له. ويشيع استخدامه في المنصَّات التي لا تدعم [أنظمة تسمية النطاقات المعمَّاة](advanced/dns-overview.md#what-is-encrypted-dns) أصلًا.

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

## Self-hosted Solutions

تتيح الاستضافة الذاتية لنظام تسمية نطاقات التصفية في المنصَّات المتحكَّم بها، مثل أجهزة التلفاز الذكية وغيرها من أجهزة إنترنت الأشياء، وذلك لأن جهة العميل لا تحتاج لأي برمجيات.

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

[^1]: تخزِّن آدجارد قياسات الأداء المجمَّعة من خوادم أنظمة تسمية نطاقاتهم، وتتضمَّن عدد الطلبات المكتملة لكلِّ خادم، وعدد الطلبات المحظورة، وسرعة معالجة الطلبات. وتخزِّن أيضًا قاعدة بيانات بها النطاقات المطلوبة خلال آخر ٢٤ ساعة. «نحتاج هذه المعلومات لنتحرَّى ونحظر المتتبِّعات والمخاطر الجديدة.» «وكذلك نسجِّل عدد المرات التي تُحظر فيها المتتبِّعات. نحتاج هذه المعلومات لنزيل القواعد القديمة من تصفياتنا.» [https://adguard.com/en/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: تجمِّع وتخزِّن كلاودفلير عددًا قليلًا من استعلامات أنظمة تسمية النطاقات المرسلة للمحلِّل ١٫١٫١٫١. لا تسجِّل خدمة المحلِّل ١٫١٫١٫١ بيانات شخصيةً، وغالب ما تسِّجل من بيانات لا تعرِّف الأشخاص تخزَّن مدَّة ٢٥ ساعةً لا أكثر. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: تسجِّل كنترول دي البيانات من المحلِّلات المدفوعة التي لها ملفَّات تعريف مخصَّصة فقط. المحلِّلات المجَّانية لا تسجِّل بيانات. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: خدمة أنظمة تسمية النطاقات من ملفاد متاحة للمشتركين في خدمة الشبكة الخاصة الافتراضية ولغير المشتركين كذلك. تزعم سياسة خصوصيتهم صريحًا أنهم لا يسجِّلون طلبات أنظمة تسمية النطاقات أبدًا. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^5]: When used with an account, NextDNS will enable insights and logging features by default (as some features require it). You can choose retention time and log storage location for any logs you choose to keep, or disable logs altogether. If used without an account, no data is logged. [https://nextdns.io/privacy](https://nextdns.io/privacy)
[^6]: تجمع كواد٩ بعض البيانات لمراقبة المخاطر والاستجابات. ويمكن لتلك البيانات أن تُخلط وتُشارك، وغرض ذلك قد يكون لأبحاث الأمن. لا تجمع كواد٩ ولا تسجِّل عناوين IP أو أيَّ بيانات تصنِّفها معرِّفةً شخصيًّا. [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
