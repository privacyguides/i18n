---
title: فلترة الـ DNS
meta_title: "حلول استضافة DNS بنفسك - Privacy Guides"
icon: material/dns
description: للقرّاء الذين لديهم خبرة تقنية أكبر، يمكنهم تشغيل خدمة DNS خاصة بهم لفلترة المحتوى على الأجهزة التي لا تدعمها خدمات DNS السحابية.
cover: dns.webp
---

<small>يحمي من التهديدات التالية:</small>

- [:material-server-network: مقدّمو الخدمات](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash:رأسمالية المراقبة](../basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

استضافة DNS بنفسك مفيدة لتوفير [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) على الأجهزة التي يصعب تثبيت البرامج عليها، مثل أجهزة التلفزيون الذكية وغيرها من أجهزة الـ IoT، لأنها لا تتطلب تثبيت أي برنامج على هذه الأجهزة. ضع في اعتبارك أن حلول الـDNS التالية تعمل عادة داخل منزلك أو شبكتك المحلية (local netowrk) فقط، إلا إذا أجريت إعدادات أكثر تقدما.

## أنظمة حجب النطاقات عبر الـ DNS

تستخدم [أنظمة حجب النطاقات عبر الـDNS](https://en.wikipedia.org/wiki/DNS_sinkhole) خدمة الـ DNS filtering لحظر محتوى الويب غير المرغوب فيه، مثل الإعلانات.

### Pi-Hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](../assets/img/self-hosting/pi-hole.svg){ align=right }

أداة Pi-hole أداة مفتوحة المصدر لحجب المحتوى غير المرغوب فيه عبر الـDNS، وتوفر واجهة ويب سهلة الاستخدام لعرض الإحصائيات وإدارة المحتوى المحظور. صُمّم Pi-hole ليعمل على أجهزة الـRaspberry Pi، لكنه لا يقتصر عليها، ويمكن تشغيله على أجهزة أخرى.

[:octicons-home-16: Homepage](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Source Code" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title="Contribute" }

</div>

### AdGuard Home

<div class="admonition recommendation" markdown>

![AdGuard Home logo](../assets/img/self-hosting/adguard-home.svg){ align=right }

أداة AdGuard Home أداة مفتوحة المصدر لحجب المحتوى غير المرغوب فيه عبر الـDNS، وتوفر واجهة ويب بتصميم متقن وسهل الاستخدام لعرض الإحصائيات وإدارة المحتوى المحظور.

[:octicons-home-16: Homepage](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Source Code" }

</div>
