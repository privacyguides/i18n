---
meta_title: "توصيات ومقارنة بين خِدْمَات الشبكات الخاصة الافتراضية، دون رعاة أو إعلانات - Privacy Guides"
title: خدمات الشبكات الخاصة الافتراضية
icon: material/vpn
description: أفضل خدمات الشبكات الخاصة الافتراضية لحماية خصوصيتك وأمانك على الإنترنت. اعثر هنا على مزود خدمة لا يريد التجسس عليك.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>يوفر الحماية من التهديدات التالية:</small>

- [:material-account-cash: رأسمالية المراقبة](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

إذا كنت تبحث عن *خصوصية* إضافية من مزود خدمة الإنترنت الخاص بك، أو على شبكة Wi-Fi عامة، أو في أثناء تحميل ملفات تورنت، فقد تكون **الشبكة الافتراضية الخاصة** هي الحل المناسب لك.

<div class="admonition danger" markdown>
<p class="admonition-title">لا تحميك الشبكات الخاصة الافتراضية من التعرف على هويتك</p>

**لن يؤدي** استخدام شبكة خاصة افتراضية إلى إبقاء عاداتك التصفحية مجهولة الهُوِيَّة، ولن يضيف حماية إلى الاتصالات التي تستخدم ميثاق نَقْل النُصوصٍ التَرابُطيَّة (HTTP) الغير آمن.

إذا كنت تبحث عن **عدم الكشف عن هويتك**، فعليك استخدام متصفح Tor. إذا كنت تبحث عن **أمان** إضافي، يجب التأكد من الاتصال بمواقع الويب باستخدام ميثاق نَقْل النُصوصٍ التَرابُطيَّة الآمن (HTTPS). الشبكات الخاصة الافتراضية ليست بديلاً للممارسات الأمنية الجيدة.

[Introduction to the Tor Browser](tor.md#tor-browser){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[نظرة عامة شاملة على الشبكات الخاصة الافتراضية: :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## موفِّرو الخدمة الموصى بهم

يستخدم مزودو الخدمات الذين نوصي بهم التشفير، ويدعمون WireGuard & OpenVPN، ولديهم سياسة عدم تسجيل الاتصالات. للمزيد من المعلومات، اطلع على [قائمة المعايير](#criteria).

| مزوّد                 | البُلدان | WireGuard                     | إعادة توجيه المنفذ (Port Forwarding)                | IPv6                                                     | المدفوعات المخفيّة           |
| --------------------- | -------- | ----------------------------- | --------------------------------------------------- | -------------------------------------------------------- | ---------------------------- |
| [Proton](#proton-vpn) | 127+     | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } الدعم الجزئي | :material-information-outline:{ .pg-blue } الدعم المحدود | Cash  Monero via third party |
| [IVPN](#ivpn)         | 41+      | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }              | :material-information-outline:{ .pg-blue } الصادر فقط    | Monero  Cash                 |
| [ملفاد](#mullvad)     | 49+      | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }              | :material-check:{ .pg-green }                            | Monero  Cash                 |

### الشبكات الخاصة الافتراضية من Proton

<div class="admonition recommendation" markdown>

![شعار الشبكات الخاصة الافتراضية من Proton] (assets/img/vpn/protonvpn.svg){ align=right }

**الشبكات الخاصة الافتراضية من Proton** هي منافس قوي في مجال الشبكات الخاصة الافتراضية، وهي تعمل منذ عام 2016. يقع مقر شركة Proton AG في سويسرا وتقدم فئة مجانية محدودة، بالإضافة إلى خِيار مميز أكثر.

[:octicons-home-16: Homepage](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://protonvpn.com/download-windows)
- [:simple-apple: macOS](https://protonvpn.com/download-macos)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 127 Countries

Proton VPN has [servers in 127 countries](https://protonvpn.com/vpn-servers)(1) or [10](https://protonvpn.com/support/how-to-create-free-vpn-account) if you use their [free plan](https://protonvpn.com/blog/product-roadmap-winter-2025-2026).(2) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. This is because of a shorter route (fewer hops) to the destination.
{ .annotate }

1. Of which at least 71 are virtual servers, meaning your IP will appear from the country but the server is in another. 12 more locations have both hardware and virtual servers. [Source](https://protonvpn.com/support/how-smart-routing-works)
2. Last checked: 2025-10-28

استخدام [خادم مخصص](https://en.wikipedia.org/wiki/Dedicated_hosting_service) يعني أن الشركة تملك الخادم وتتحكم فيه بالكامل، مما يقلل من خطر تسريب البيانات أو تعرضها للاختراق مقارنة [بخوادم مشتركة (VPS)](https://en.wikipedia.org/wiki/Virtual_private_server) تُستخدم من عدة عملاء.

#### :material-check:{ .pg-green } تمت مراجعته من جهة مستقلة

Independent security researcher Ruben Santamarta conducted audits for Proton VPN's [browser extensions](https://drive.proton.me/urls/RWDD2SHT98#v7ZrwNcafkG8) and [apps](https://drive.proton.me/urls/RVW8TXG484#uTXX5Fc9GADo) in September 2024 and January 2025, respectively. Proton VPN's infrastrcture has undergone [annual audits](https://protonvpn.com/blog/no-logs-audit) by Securitum since 2022.

Previously, Proton VPN underwent an independent audit by SEC Consult in January 2020. اكتشفت شركة SEC Consult بعض الثغرات الأمنية متوسطة ومنخفضة الخطورة في تطبيقات Proton VPN على أنظمة ويندوز وأندرويد وiOS، وقد قامت Proton VPN بـ"معالجتها بالشكل المناسب" قبل نشر تقارير التدقيق. جميع الثغرات التي تم العثور عليها كانت محدودة التأثير، ولم تُمكن أي جهة من الوصول عن بُعد إلى جهازك أو اعتراض حركة الإنترنت الخاصة بك. You can view individual reports for each platform in their dedicated [blog post](https://web.archive.org/web/20250307041036/https://protonvpn.com/blog/open-source) on the audit.

#### :material-check:{ .pg-green } العملاء الذين يستخدمون برامج مفتوحة المصدر

Proton VPN provides the source code for their desktop and mobile clients in their [GitHub organization](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } يقبل الدفع نقدا

Proton VPN, in addition to accepting credit/debit cards, PayPal, and [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), also accepts **cash/local currency** as an anonymous form of payment. You can also use [**Monero**](cryptocurrency.md#monero) to purchase vouchers for Proton VPN Plus and Proton Unlimited via their [official](https://discuss.privacyguides.net/t/add-monero-as-an-anonymous-payment-method-for-proton-services/31058/15) reseller [ProxyStore](https://dys2p.com/en/2025-09-09-proton.html).

#### :material-check:{ .pg-green } WireGuard Support

يدعم Proton VPN بروتوكول WireGuard. [WireGuard](https://wireguard.com) هو بروتوكول VPN جديد نسبيا، ويعتمد على [تشفير حديث ومتطور](https://wireguard.com/protocol) يوفّر أمانًا عاليا وكفاءة في الأداء. ويتميز WireGuard أيضا بتصميمه البسيط وأدائه العالي، مقارنة ببروتوكولات VPN التقليدية.

توصي Proton VPN بـ[استخدام بروتوكول WireGuard](https://protonvpn.com/blog/wireguard) مع خدمتها. توفّر Proton VPN أيضًا أداة لإنشاء إعدادات مخصصة لبروتوكول WireGuard، يمكن استخدامها مع [تطبيقات WireGuard الرسمية](https://wireguard.com/install). <br> **ملاحظة**: قد تحتاج إلى هذه الأداة إذا كنت تفضل استخدام تطبيق WireGuard الرسمي بدلا من تطبيق Proton VPN، أو إذا كنت تستخدم نظام تشغيل لا يتوفر عليه تطبيق Proton VPN مباشرة.

#### :material-alert-outline:{ .pg-orange } Limited IPv6 Support

تدعم Proton حاليا ب[روتوكول IPv6 ](https://protonvpn.com/support/prevent-ipv6-vpn-leaks)في إضافة المتصفح (browser extension) ونسخة Linux، ولكن يجدر الانتباه إلى أن حوالي 20٪ من خوادمها لا تزال غير متوافقة مع هذا البروتوكول. تطبيق Proton VPN يحميك من تسريب عنوان IPv6 على معظم الأنظمة عن طريق حظر هذا النوع من الاتصال. لكن نتيجة لذلك، لن تتمكن من زيارة مواقع تعتمد على IPv6 فقط، أو الاتصال بالخدمة من شبكة لا تدعم سوى IPv6.

#### :material-information-outline:{ .pg-info } Remote Port Forwarding

تدعم Proton VPN حاليا فقط [Port Forwarding ](https://protonvpn.com/support/port-forwarding)المؤقت (ephemeral) عن بعد باستخدام بروتوكول NAT-PMP، مع مدة صلاحية قصيرة تبلغ 60 ثانية لكل منفذ. تطبيقات Proton VPN الرسمية على نظامي Windows وLinux توفّر خيار Port Forwarding بطريقة سهلة ومباشرة. أما على الأنظمة الأخرى، فستحتاج إلى تشغيل [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup) يدويا — وهو برنامج صغير يُستخدم للتواصل مع جهاز الراوتر لطلب فتح منفذ بشكل مؤقت. العديد من تطبيقات التورنت تحتوي على دعم مدمج لـ NAT-PMP، مما يتيح لها طلب فتح المنافذ تلقائيا من الراوتر أو خدمة الـ VPN دون تدخل يدوي.

#### :material-information-outline:{ .pg-blue } مقاومة الرقابة

تمتلك Proton VPN بروتوكولا خاصا يُعرف باسم [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol)، والذي *قد* يساعد في تجاوز الرقابة في الحالات التي يتم فيها حظر بروتوكولات VPN التقليدية مثل OpenVPN أو WireGuard باستخدام أساليب بسيطة. بروتوكول Stealth يخفي اتصال VPN من خلال تمريره داخل TLS session (وهي نفس التقنية التي تُستخدم في تأمين مواقع الويب العادية مثل HTTPS)، مما يجعل حركة البيانات تبدو مثل أي تصفح عادي، ويساعد في تجاوز أنظمة الحجب التي تميز أو تمنع الـ VPN.

لكن للأسف، في الدول التي تعتمد تقنيات مراقبة وتحليل متطورة لاكتشاف أي نوع من الاتصالات المشفّرة (مثل الـ VPN)، فإن بروتوكول Stealth لا يكون فعالا بشكل كبير. بروتوكول Stealth متاح على أنظمة أندرويد وiOS وويندوز وmacOS، لكنه غير متوفر بعد على نظام Linux.

#### :material-check:{ .pg-green } عملاء الهاتف المحمول

توفر Proton VPN تطبيقات رسمية على متجر [App Store](https://apps.apple.com/app/id1437005085) و[Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)، بواجهة استخدام سهلة، فلا تحتاج إلى إعداد اتصال WireGuard يدويا. يتوفر تطبيق Proton VPN لأجهزة أندرويد أيضا على [GitHub](https://github.com/ProtonVPN/android-app/releases).

<div class="admonition warning" markdown>
<p class="admonition-title">كيفية إيقاف مشاركة بيانات التتبع</p>

في أندرويد، تخفي Proton إعدادات التتبع (telemetry) تحت خيار يحمل اسما مضللا وهو "**ساعدنا في مكافحة الرقابة**" داخل لوحة الإعدادات. في الأنظمة الأخرى، يمكن العثور على هذه الإعدادات تحت قائمة "**Usage statistics**".

نحن نلفت الانتباه إلى هذه النقطة لأنه، رغم أننا لا نعارض بالضرورة مشاركة إحصاءات الاستخدام المجهولة مع المطورين، من المهم أن تكون هذه الإعدادات واضحة وسهلة الوصول.

</div>

#### :material-information-outline:{ .pg-blue } ملاحظات إضافية

تدعم تطبيقات Proton VPN المصادقة الثنائية (2FA) على جميع المنصات. Proton VPN تمتلك خوادم ومراكز بيانات خاصة بها في سويسرا وآيسلندا والسويد. يوفرون خدمة حجب المحتوى والمواقع المعروفة بأنها تحتوي على برمجيات خبيثة، وذلك من خلال الـ (DNS) الخاص بهم. بالإضافة إلى ذلك، توفر Proton VPN خوادم "Tor" مخصصة، تتيح لك الاتصال بسهولة بمواقع.onion. ومع ذلك، نوصي بشدة باستخدام [متصفح Tor](tor.md#tor-browser) الرسمي لهذا الغرض لضمان أعلى مستوى من الخصوصية.

##### :material-alert-outline:{ .pg-orange }

ميزة Kill Switch [لا تعمل بشكل صحيح](https://protonvpn.com/support/macos-t2-chip-kill-switch) على أجهزة Mac المزودة بمعالجات Intel. إذا كنت تحتاج إلى هذه الميزة، وتستخدم جهاز Mac بمعالج Intel، فمن الأفضل أن تفكر في استخدام خدمة VPN أخرى تدعم ميزة Kill Switch بشكل موثوق على هذا النوع من الأجهزة.

### IVPN

<div class="admonition recommendation" markdown>

![IVPN logo](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** هو مزود VPN مميز آخر، وقد بدأ تشغيله منذ عام 2009. شركة IVPN مقرها في جبل طارق، ولا توفر فترة تجريبية مجانية لاختبار الخدمة.

[:octicons-home-16: Homepage](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

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

IVPN has [servers in 41 countries](https://ivpn.net/status).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. وذلك لأن المسار إلى الوجهة سيكون أقصر (أي عدد أقل من التمريرات أو "hops")، مما يؤدي إلى تقليل التأخير وتحسين سرعة الاتصال.
{ .annotate }

1. Last checked: 2025-10-28

استخدام [خادم مخصص](https://en.wikipedia.org/wiki/Dedicated_hosting_service) يعني أن الشركة تملك الخادم وتتحكم فيه بالكامل، مما يقلل من خطر تسريب البيانات أو تعرضها للاختراق مقارنة [بخوادم مشتركة (VPS)](https://en.wikipedia.org/wiki/Virtual_private_server) تُستخدم من عدة عملاء.

#### :material-check:{ .pg-green } تمت مراجعته من جهة مستقلة

أجرت IVPN عدة [مراجعات أمان مستقلة](https://ivpn.net/en/blog/tags/audit) منذ عام 2019، وقد أعلنت بشكل علني التزامها بإجراء م[راجعات أمنية سنوية](https://ivpn.net/blog/ivpn-apps-security-audit-concluded) لتعزيز موثوقيتها وشفافيتها.

#### :material-check:{ .pg-green } العملاء الذين يستخدمون برامج مفتوحة المصدر

بدءًا من فبراير 2020، [أصبحت تطبيقات IVPN مفتوحة المصدر](https://ivpn.net/blog/ivpn-applications-are-now-open-source)، مما يسمح لأي شخص بمراجعة الكود والتأكد من مستوى الأمان والخصوصية الذي توفره الخدمة. يمكن الحصول على الشيفرة المصدرية لتطبيقات IVPN من [منظمة GitHub](https://github.com/ivpn) الخاصة بهم، ما يتيح للمستخدمين والخبراء مراجعتها بحرية.

#### :material-check:{ .pg-green } تقبل الدفع بوسائل خاصة مثل النقود وعملة مونيرو (Monero)

بالإضافة إلى قبول بطاقات الـ credit/debit وPayPal، تقبل IVPN الدفع باستخدام البيتكوين (Bitcoin) **ومونيرو (Monero)** **والنقد (cash)** كخيارات دفع مجهولة الهوية، وذلك عند الاشتراك في الخطط السنوية. You can also purchase [prepaid cards](https://ivpn.net/knowledgebase/billing/voucher-cards-faq) with redeem codes.

#### :material-check:{ .pg-green } WireGuard Support

تدعم خدمة IVPN بروتوكول WireGuard®، وهو بروتوكول حديث يتميز بالبساطة، والأداء العالي، واستخدام تقنيات تشفير متقدمة. [WireGuard](https://wireguard.com) هو بروتوكول VPN جديد نسبيا، ويعتمد على [تشفير حديث ومتطور](https://wireguard.com/protocol) يوفّر أمانًا عاليا وكفاءة في الأداء. ويتميز WireGuard أيضا بتصميمه البسيط وأدائه العالي، مقارنة ببروتوكولات VPN التقليدية.

[توصي ](https://ivpn.net/wireguard)IVPN باستخدام بروتوكول WireGuard مع خدمتها، ولذلك فهو مفعّل بشكل افتراضي في جميع تطبيقات IVPN. كما توفر IVPN أيضا أداة لتوليد إعدادات WireGuard لاستخدامها مع ت[طبيقات WireGuard الرسمية](https://wireguard.com/install).

#### :material-information-outline:{ .pg-blue } دعم لـ IPv6

تتيح لك IVPN [الاتصال بالخدمات التي تستخدم بروتوكول IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6)، ولكنها لا تسمح بالاتصال من جهاز يستخدم عنوان IPv6.

#### :material-alert-outline:{ .pg-orange } Remote Port Forwarding

كانت IVPN تدعم ميزة الـ (Port Forwarding) سابقا، لكنها أزالت هذه الخاصية في [يونيو 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). غياب هذه الميزة قد يؤثر سلبا على بعض التطبيقات، خصوصا تلك التي تعتمد على الاتصال (P2P) مثل برامج التورنت.

#### :material-check:{ .pg-green } مقاومة الرقابة

IVPN has obfuscation modes using [V2Ray](https://v2ray.com/en/index) which helps in situations where VPN protocols like OpenVPN or WireGuard are blocked. It has two modes where it can use [VMess](https://guide.v2fly.org/en_US/basics/vmess) over QUIC or TCP connections. بروتوكول QUIC حديث ويُحسن طريقة انتقال البيانات، مما يساعد في زيادة السرعة وتقليل التأخير (latency) أثناء التصفح. في وضع TCP، يتم تغليف بياناتك لتبدو وكأنها بيانات تصفح عادية (HTTP)، مما يساعد في تجاوز الرقابة أو الحظر في بعض الشبكات.

#### :material-check:{ .pg-green } عملاء الهاتف المحمول

توفر IVPN تطبيقات رسمية على متجر [App Store](https://apps.apple.com/app/id1193122683) و[Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)، وتتميز هذه التطبيقات بواجهة استخدام سهلة، مما يُغنيك عن إعداد اتصال WireGuard يدويا. يتوفر تطبيق IVPN لأندرويد أيضا على [GitHub](https://github.com/ivpn/android-app/releases).

#### :material-information-outline:{ .pg-blue } ملاحظات إضافية

تطبيقات IVPN تدعم المصادقة الثنائية (two-factor authentication). توفر IVPN ميزة تعرف باسم "حاجب التتبع ([AntiTracker](https://ivpn.net/antitracker))"، وهي تقوم بحظر أدوات التتبع والإعلانات المزعجة مباشرة من خلال الاتصال بالإنترنت نفسه – أي أن الحظر يتم من خلال اتصال الشبكة، وليس فقط داخل المتصفح – قبل أن تصل إلى المتصفح أو التطبيقات.

### ملفاد

<div class="admonition recommendation" markdown>

![Mullvad logo](assets/img/vpn/mullvad.svg){ align=right }

Mullvad هو خدمة VPN سريعة ومنخفضة التكلفة، تركز بشكل جاد على الشفافية والأمان. تعمل Mullvad منذ عام 2009. يقع مقر Mullvad في السويد، وتقدم ضمان استرداد لمدة 14 يوما على [طرق الدفع](https://mullvad.net/en/help/refunds) التي تسمح بذلك.

[:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 49 دولة

تمتلك Mullvad [خوادم في 49 دولة](https://mullvad.net/servers).(1) اختيارك لخدمة VPN توفر خادما قريبا من موقعك الجغرافي يساعد على تقليل زمن التأخير (latency) في حركة البيانات التي ترسلها عبر الشبكة. ويعود ذلك إلى أن المسار بينك وبين الوجهة يكون أقصر، أي أن البيانات تمر عبر عدد أقل من الـ (hops).
{ .annotate }

1. Last checked: 2025-10-28

استخدام [خادم مخصص](https://en.wikipedia.org/wiki/Dedicated_hosting_service) يعني أن الشركة تملك الخادم وتتحكم فيه بالكامل، مما يقلل من خطر تسريب البيانات أو تعرضها للاختراق مقارنة [بخوادم مشتركة (VPS)](https://en.wikipedia.org/wiki/Virtual_private_server) تُستخدم من عدة عملاء.

#### :material-check:{ .pg-green } تمت مراجعته من جهة مستقلة

خضعت Mullvad لعدة [مراجعات أمنية مستقلة](https://mullvad.net/en/blog/tag/audits)، وأعلنت بشكل علني عن سعيها لإجراء [مراجعات سنوية](https://mullvad.net/en/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) لتطبيقاتها وبنيتها التحتية.

#### :material-check:{ .pg-green } العملاء الذين يستخدمون برامج مفتوحة المصدر

تُوفر Mullvad الـ (source code) لتطبيقاتها على الحاسوب والهاتف عبر [منظمتها على GitHub](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } تقبل الدفع بوسائل خاصة مثل النقود وعملة مونيرو (Monero)

بالإضافة إلى قبول بطاقات الـ credit/debit وPayPal، تقبل Mullvad أيضا البيتكوين، وبيتكوين كاش، و**Monero**، و**النقد** كطرق دفع مجهولة الهوية. You can also purchase [prepaid cards](https://mullvad.net/en/help/partnerships-and-resellers) with redeem codes. تقبل Mullvad أيضا الدفع عبر تطبيق Swish والتحويل البنكي المباشر، بالإضافة إلى بعض أنظمة الدفع الأوروبية الأخرى.

#### :material-check:{ .pg-green } WireGuard Support

تدعم Mullvad بروتوكول WireGuard®. [WireGuard](https://wireguard.com) هو بروتوكول VPN جديد نسبيا، ويعتمد على [تشفير حديث ومتطور](https://wireguard.com/protocol) يوفّر أمانًا عاليا وكفاءة في الأداء. ويتميز WireGuard أيضا بتصميمه البسيط وأدائه العالي، مقارنة ببروتوكولات VPN التقليدية.

[توصي ](https://mullvad.net/en/help/why-wireguard)Mullvad باستخدام بروتوكول WireGuard مع خدمتها. It is the only protocol supported on their mobile apps, and their desktop apps will [lose OpenVPN support](https://mullvad.net/en/blog/reminder-that-openvpn-is-being-removed) in 2025. Additionally, their servers will stop accepting OpenVPN connections by January 15, 2026. توفر Mullvad أيضا مولد إعدادات WireGuard لاستخدامه مع [تطبيقات ](https://wireguard.com/install)WireGuard الرسمية.

#### :material-check:{ .pg-green } دعم لـ IPv6

تتيح لك Mullvad الوصول إلى الخدمات التي [تعمل عبر بروتوكول IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support)، وكذلك الاتصال من جهاز يستخدم عنوان IPv6.

#### :material-alert-outline:{ .pg-orange } Remote Port Forwarding

كانت Mullvad تدعم ميزة الـ (Port Forwarding) في السابق، لكنها أزالت هذا الخيار في [مايو 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). غياب هذه الميزة قد يؤثر سلبا على بعض التطبيقات، خصوصا تلك التي تعتمد على الاتصال (P2P) مثل برامج التورنت.

#### :material-check:{ .pg-green } مقاومة الرقابة

توفر Mullvad عددا من الميزات التي تساعد على تجاوز الرقابة والوصول الحر إلى الإنترنت:

- الـ **Obfuscation modes**: توفر Mullvad وضعين مدمجين للتمويه (obfuscation): UDP-over-TCP و[WireGuard over Shadowsocks](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard). تعمل هذه الأوضاع (modes) على إخفاء حركة VPN الخاصة بك لتبدو كأنها حركة ويب عادية، مما يجعل من الصعب على أنظمة الرقابة اكتشافها أو حظرها. يُقال إن الصين أصبحت تحتاج إلى أسلوب جديد لتعطيل حركة البيانات التي تمر عبر [Shadowsocks](https://gfw.report/publications/usenixsecurity23/en).
- **الـ Advanced obfuscation (التموية المتقدم) بإستخدام Shadowsocks and v2ray**: للمستخدمين المتقدمين، توفر Mullvad دليلا لشرح كيفية استخدام إضافة Shadowsocks مع v2ray مع تطبيقات Mullvad. يوفر هذا الإعداد طبقة إضافية من التمويه والتشفير، مما يعزز القدرة على تجاوز الرقابة والحفاظ على الخصوصية.
- **Custom server IPs**: إذا كانت هناك محاولات لحجب VPN من خلال منع الوصول إلى عناوين الـ IP المعروفة، يمكنك التواصل مع دعم Mullvad وطلب عناوين خوادم مخصصة تساعدك على تجاوز هذا الحجب. بعد أن تستلم الـ custom IPs من فريق دعم Mullvad، يمكنك تحميلها في إعداد موجود داخل التطبيق يُسمى "Server IP override". هذا الإعداد يسمح لك باستخدام عناوين جديدة غير معروفة لأنظمة الحجب، بدلا من العناوين العادية التي قد تكون محجوبة.
- **الـ Bridges وProxies**: تتيح Mullvad استخدام Bridges أو Proxies للوصول إلى الـ API الخاصة بها (اللازمة لتسجيل الدخول)، مما يساعد في تجاوز محاولات الرقابة التي تحاول حجب الوصول إلى الـAPI نفسه.

#### :material-check:{ .pg-green } عملاء الهاتف المحمول

نشرت Mullvad تطبيقاتها الرسمية على [App Store ](https://apps.apple.com/app/id1488466513)و[Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)، وتوفر هذه التطبيقات واجهة سهلة الاستخدام، تغنيك عن إعداد اتصال WireGuard يدويا. يتوفر تطبيق Mullvad لأندرويد أيضا على [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } ملاحظات إضافية

تُظهر Mullvad قدرا كبيرا من الشفافية بشأن الخوادم التي [تملكها أو تستأجرها](https://mullvad.net/en/servers). كما توفر Mullvad خيار تفعيل ميزة الحماية من تحليل الحركة باستخدام الذكاء الاصطناعي ([DAITA](https://mullvad.net/en/blog/daita-defense-against-ai-guided-traffic-analysis)) داخل تطبيقاتها، وهي تهدف إلى منع أنظمة الذكاء الاصطناعي من تحليل أنماط حركة الإنترنت لتحديد نشاطك أو هويتك. تحمي ميزة DAITA من نوع متقدم من المراقبة يُعرف بتحليل حركة البيانات، والذي يمكن استخدامه لمحاولة تحديد المواقع التي تزورها من خلال مراقبة نمط استخدامك للـVPN، حتى لو لم يُعرف محتوى ما ترسله أو تستقبله.

## المعايير

<div class="admonition danger" markdown>
<p class="admonition-title">خطر</p>

من المهم أن تعلم أن استخدام خدمة VPN لا يجعلك مجهول الهوية بالكامل،
لكنه يمنحك مستوى أفضل من الخصوصية في مواقف معينة. يجب عدم استخدام خدمات VPN في أنشطة مخالفة للقانون. لا تعتمد فقط على سياسة "No Log"،
(فقد لا يمكن التأكد من التزام الخدمة بهذه السياسة ما لم تخضع لمراجعات مستقلة ومحايدة).

</div>

**يرجى ملاحظة أننا لسنا مرتبطين بأي من الخدمات التي نوصي بها. وهذا ما يتيح لنا تقديم توصيات محايدة تماما.** بالإضافة إلى[ المعايير العامة ](about/criteria.md)التي نعتمدها، قمنا بوضع مجموعة واضحة من المتطلبات لأي خدمة VPN ترغب في أن نوصي بها، وتشمل: تشفير قوي، مراجعات أمنية مستقلة، استخدام تقنيات حديثة، وغيرها من المعايير الصارمة. We suggest you familiarize yourself with this list before choosing a VPN provider, and conduct your own research to ensure the VPN provider you choose is as trustworthy as possible.

### Technology

We require all our recommended VPN providers to provide standard configuration files which can be used in a generic, open-source client. **If** a VPN provides their own custom client, we require a kill switch to block network data leaks when disconnected.

**Minimum to Qualify:**

- Support for strong protocols such as WireGuard.
- Kill switch built in to clients.
- Multi-hop support. Multi-hopping is important to keep data private in case of a single node compromise.
- If VPN clients are provided, they should be [open source](https://en.wikipedia.org/wiki/Open_source), like the VPN software they generally have built into them. We believe that [source code](https://en.wikipedia.org/wiki/Source_code) availability provides greater transparency about what the program is actually doing.
- Censorship resistance features designed to bypass firewalls without DPI.

**أحسن الاحتمالات:**

- Kill switch with highly configurable options (enable/disable on certain networks, on boot, etc.)
- Easy-to-use VPN clients
- [IPv6](https://en.wikipedia.org/wiki/IPv6) support. We expect that servers will allow incoming connections via IPv6 and allow you to access services hosted on IPv6 addresses.
- Capability of [remote port forwarding](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) assists in creating connections when using P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) file sharing software or hosting a server (e.g., Mumble).
- Obfuscation technology which camouflages the true nature of internet traffic, designed to circumvent advanced internet censorship methods like DPI.

### Privacy

We prefer our recommended providers to collect as little data as possible. Not collecting personal information on registration, and accepting anonymous forms of payment are required.

**Minimum to Qualify:**

- [Anonymous cryptocurrency](cryptocurrency.md) **or** cash payment option.
- No personal information required to register: Only username, password, and email at most.

**أحسن الاحتمالات:**

- Accepts multiple [anonymous payment options](advanced/payments.md).
- No personal information accepted (auto-generated username, no email required, etc.).

### Security

A VPN is pointless if it can't even provide adequate security. We require all our recommended providers to abide by current security standards. Ideally, they would use more future-proof encryption schemes by default. We also require an independent third-party to audit the provider's security, ideally in a very comprehensive manner and on a repeated (yearly) basis.

**Minimum to Qualify:**

- Strong Encryption Schemes: OpenVPN with SHA-256 authentication; RSA-2048 or better handshake; AES-256-GCM or AES-256-CBC data encryption.
- Forward Secrecy.
- Published security audits from a reputable third-party firm.
- VPN servers that use full-disk encryption or are RAM-only.

**أحسن الاحتمالات:**

- Strongest Encryption: RSA-4096.
- Optional quantum-resistant encryption.
- Comprehensive published security audits from a reputable third-party firm.
- Bug-bounty programs and/or a coordinated vulnerability-disclosure process.
- RAM-only VPN servers.

### Trust

You wouldn't trust your finances to someone with a fake identity, so why trust them with your internet data? We require our recommended providers to be public about their ownership or leadership. كما نفضل أن تنشر الخدمة تقارير شفافية بشكل منتظم، خصوصا فيما يتعلق بكيفية تعاملها مع طلبات الجهات الحكومية.

**الحد الأدنى لترشيح الخدمة:**

- فريق إداري أو مالك معروف ومُعلن بشكل علني.
- أن تكون الشركة مقرها في دولة لا يمكن إلزامها قانونيا بمراقبة المستخدمين أو الاحتفاظ بسجلات سرية.

**أحسن الاحتمالات:**

- إدارة معلنة.
- تقارير شفافية دورية.

### التسويق

بالنسبة لخدمات الـVPN التي نوصي بها، نُفضل أن تعتمد أسلوبا تسويقيا صادقا وواضحا. (أي أن لا تبالغ في الوعود، ولا تروج لمفاهيم مضللة مثل "الخصوصية المطلقة" أو "إخفاء الهوية بالكامل").

**الحد الأدنى لترشيح الخدمة:**

- يجب أن تُدير الخدمة أدوات التحليل الخاصة بها بنفسها، دون الاعتماد على خدمات خارجية مثل Google Analytics.

يشترط ألا تحتوي المواد التسويقية على معلومات مضللة أو وعود مبالغ فيها:

- ضمانات بحماية الهوية بشكل كامل بنسبة 100٪. عندما يدعي أحدهم أن شيئا ما مضمون بنسبة 100٪، فهذا يعني ضمنا أنه لا يمكن أن يفشل أبدا — وهو أمر غير واقعي. نعلم أن المستخدمين قد يفصحون عن هويتهم دون قصد بطرق متعددة، مثلا.:
    - إعادة استخدام بيانات شخصية (مثل البريد أو الاسم المستعار) سبق استخدامها بدون أدوات إخفاء الهوية مثل Tor، مما يسهل الربط بين الهوية الحقيقية والنشاط.)
    - [بصمة المتصفح](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- يُعتبر من التسويق المضلل أن تدعي خدمة VPN أن اتصالها العادي (الذي يمر عبر خادم واحد فقط) يمنح "مجهولية أكثر" من شبكة Tor، لأن Tor يستخدم مسارا مكوّنا من ثلاث خوادم أو أكثر، ويتغير بشكل منتظم لزيادة الخصوصية.
- استخدام لغة متزنة: من المقبول أن تقول إن اتصال الـVPN "مقطوع" أو "غير متصل"، لكن استخدام تعبيرات مثل "أنت مكشوف"، أو "في خطر"، أو "تم اختراقك" هو تهويل غير ضروري، وقد يكون غير دقيق. فمثلا، قد يكون ذلك الشخص ببساطة يستخدم خدمة VPN أخرى، أو متصلا عبر شبكة Tor.

**أحسن الاحتمالات:**

أسلوب تسويقي مسؤول يجمع بين التوعية والفائدة للمستخدم يمكن أن يتضمن:

- مقارنة دقيقة توضح متى يكون من الأفضل استخدام شبكة [Tor](tor.md) بدلا من VPN.
- توفر موقع خدمة الـVPN عبر [نطاق.onion](https://en.wikipedia.org/wiki/.onion) (لتمكين الوصول إليه من خلال شبكة Tor عند الحاجة إلى خصوصية أعلى)

### ميزات إضافية

رغم أن هذه الأمور ليست شروطا إلزامية، إلا أننا أخذناها بعين الاعتبار عند تقييم مزودي خدمات الـVPN الذين نوصي بهم. وتشمل هذه العوامل: إمكانية حظر المحتوى، ووجود إشعارات قانونية تحذيرية (Warrant Canaries)، ودعم فني ممتاز، وعدد الاتصالات المتزامنة (simultaneous connections) المسموح بها، وغيرها.
