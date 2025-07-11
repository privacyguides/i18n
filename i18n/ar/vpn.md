---
meta_title: "توصيات ومقارنة بين خِدْمَات الشبكات الخاصة الافتراضية، دون رعاة أو إعلانات - Privacy Guides"
title: "خدمات الشبكات الخاصة الافتراضية"
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

[نزّل Tor](https://torproject.org){ .md-button .md-button--primary } [خرافات وأسئلة شائعة خاصة بـ Tor](advanced/tor-overview.md){ .md-button }

</div>

[نظرة عامة شاملة على الشبكات الخاصة الافتراضية: :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## موفِّرو الخدمة الموصى بهم

يستخدم مزودو الخدمات الذين نوصي بهم التشفير، ويدعمون WireGuard & OpenVPN، ولديهم سياسة عدم تسجيل الاتصالات. للمزيد من المعلومات، اطلع على [قائمة المعايير](#criteria).

| مزوّد                 | البُلدان | WireGuard                     | إعادة توجيه المنفذ (Port Forwarding)                | IPv6                                                     | المدفوعات المخفيّة |
| --------------------- | -------- | ----------------------------- | --------------------------------------------------- | -------------------------------------------------------- | ------------------ |
| [Proton](#proton-vpn) | 112+     | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } الدعم الجزئي | :material-information-outline:{ .pg-blue } الدعم المحدود | نقداً              |
| [IVPN](#ivpn)         | 37+      | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }              | :material-information-outline:{ .pg-blue } الصادر فقط    | Monero, نقداً      |
| [ملفاد](#mullvad)     | 49+      | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }              | :material-check:{ .pg-green }                            | Monero, نقداً      |

### الشبكات الخاصة الافتراضية من Proton

<div class="admonition recommendation" markdown>

![شعار الشبكات الخاصة الافتراضية من Proton] (assets/img/vpn/protonvpn.svg){ align=right }

**الشبكات الخاصة الافتراضية من Proton** هي منافس قوي في مجال الشبكات الخاصة الافتراضية، وهي تعمل منذ عام 2016. يقع مقر شركة Proton AG في سويسرا وتقدم فئة مجانية محدودة، بالإضافة إلى خِيار مميز أكثر.

[:octicons-home-16: صفحتهم](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="سياسة الخصوصية" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title=التوثيق}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="النص المصدري" }

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

#### :material-check:{ .pg-green } 112 دولة

لدى Proton VPN [خوادم في 112 دولة](https://protonvpn.com/vpn-servers) أو [5](https://protonvpn.com/support/how-to-create-free-vpn-account) إذا كنت تستخدم [خطتهم المجانية](https://protonvpn.com/free-vpn/server).(1) اختيار مزود VPN مع خادم أقرب خادم إليك سيقلل من زمن انتقال حركة مرور الشبكة التي ترسلها. This is because of a shorter route (fewer hops) to the destination.
{ .annotate }

1. Last checked: 2024-08-06

استخدام [خادم مخصص](https://en.wikipedia.org/wiki/Dedicated_hosting_service) يعني أن الشركة تملك الخادم وتتحكم فيه بالكامل، مما يقلل من خطر تسريب البيانات أو تعرضها للاختراق مقارنة [بخوادم مشتركة (VPS)](https://en.wikipedia.org/wiki/Virtual_private_server) تُستخدم من عدة عملاء.

#### :material-check:{ .pg-green } تمت مراجعته من جهة مستقلة

في يناير 2020، أُجري تدقيق أمني مستقل لخدمة Proton VPN من قبل شركة SEC Consult المتخصصة. اكتشفت شركة SEC Consult بعض الثغرات الأمنية متوسطة ومنخفضة الخطورة في تطبيقات Proton VPN على أنظمة ويندوز وأندرويد وiOS، وقد قامت Proton VPN بـ"معالجتها بالشكل المناسب" قبل نشر تقارير التدقيق. جميع الثغرات التي تم العثور عليها كانت محدودة التأثير، ولم تُمكن أي جهة من الوصول عن بُعد إلى جهازك أو اعتراض حركة الإنترنت الخاصة بك. لقراءة تقارير التدقيق لكل نظام تشغيل على حدة، تفضل بزيارة [protonvpn.com](https://protonvpn.com/blog/open-source). أجرت Proton VPN [تدقيقا جديدًا](https://protonvpn.com/blog/no-logs-audit) في أبريل 2022 لتعزيز الشفافية والثقة. في 9 نوفمبر 2021، أصدرت شركة [Securitum](https://research.securitum.com) [شهادة إثبات](https://research.securitum.com) تؤكد نتائج تدقيق أمني أُجري لتطبيقات Proton VPN.

#### :material-check:{ .pg-green } العملاء الذين يستخدمون برامج مفتوحة المصدر

تنشر Proton VPN الـ Source code لتطبيقاتها (على الحاسوب والهاتف) بشكل علني ضمن [منظمتها على GitHub](https://github.com/ProtonVPN)، مما يتيح للمجتمع مراجعتها والتأكد من أمانها.

#### :material-check:{ .pg-green } يقبل الدفع نقدا

إلى جانب قبول بطاقات الـ credit/debit وPayPal، و[البيتكوين](advanced/payments.md#other-coins-bitcoin-ethereum-etc)، تقبل Proton VPN أيضا **الدفع نقدًا** كوسيلة دفع مجهولة الهوية.

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

[:octicons-home-16: الصفحة الرئيسية](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="سياسة الخصوصية" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title=الشروحات التفصيلية}
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

#### :material-check:{ .pg-green } 37 دولة

تمتلك IVPN [خوادم في 37 دولة](https://ivpn.net/status).(1) اختيار مزود VPN يحتوي على خادم قريب من موقعك الجغرافي يساعد في تقليل زمن الاستجابة (Latency) لحركة البيانات التي ترسلها عبر الشبكة. وذلك لأن المسار إلى الوجهة سيكون أقصر (أي عدد أقل من التمريرات أو "hops")، مما يؤدي إلى تقليل التأخير وتحسين سرعة الاتصال.
{ .annotate }

1. تاريخ آخر تحقق: 6 أغسطس 2024

استخدام [خادم مخصص](https://en.wikipedia.org/wiki/Dedicated_hosting_service) يعني أن الشركة تملك الخادم وتتحكم فيه بالكامل، مما يقلل من خطر تسريب البيانات أو تعرضها للاختراق مقارنة [بخوادم مشتركة (VPS)](https://en.wikipedia.org/wiki/Virtual_private_server) تُستخدم من عدة عملاء.

#### :material-check:{ .pg-green } تمت مراجعته من جهة مستقلة

أجرت IVPN عدة [مراجعات أمان مستقلة](https://ivpn.net/en/blog/tags/audit) منذ عام 2019، وقد أعلنت بشكل علني التزامها بإجراء م[راجعات أمنية سنوية](https://ivpn.net/blog/ivpn-apps-security-audit-concluded) لتعزيز موثوقيتها وشفافيتها.

#### :material-check:{ .pg-green } العملاء الذين يستخدمون برامج مفتوحة المصدر

بدءًا من فبراير 2020، [أصبحت تطبيقات IVPN مفتوحة المصدر](https://ivpn.net/blog/ivpn-applications-are-now-open-source)، مما يسمح لأي شخص بمراجعة الكود والتأكد من مستوى الأمان والخصوصية الذي توفره الخدمة. يمكن الحصول على الشيفرة المصدرية لتطبيقات IVPN من [منظمة GitHub](https://github.com/ivpn) الخاصة بهم، ما يتيح للمستخدمين والخبراء مراجعتها بحرية.

#### :material-check:{ .pg-green } تقبل الدفع بوسائل خاصة مثل النقود وعملة مونيرو (Monero)

بالإضافة إلى قبول بطاقات الـ credit/debit وPayPal، تقبل IVPN الدفع باستخدام البيتكوين (Bitcoin) **ومونيرو (Monero)** **والنقد (cash)** كخيارات دفع مجهولة الهوية، وذلك عند الاشتراك في الخطط السنوية. البطاقات الـ Prepaid التي تحتوي على رموز تفعيل (redeem codes) متوفرة أيضا، [ويمكن استخدامها كوسيلة دفع](https://ivpn.net/knowledgebase/billing/voucher-cards-faq).

#### :material-check:{ .pg-green } WireGuard Support

تدعم خدمة IVPN بروتوكول WireGuard®، وهو بروتوكول حديث يتميز بالبساطة، والأداء العالي، واستخدام تقنيات تشفير متقدمة. [WireGuard](https://wireguard.com) هو بروتوكول VPN جديد نسبيا، ويعتمد على [تشفير حديث ومتطور](https://wireguard.com/protocol) يوفّر أمانًا عاليا وكفاءة في الأداء. ويتميز WireGuard أيضا بتصميمه البسيط وأدائه العالي، مقارنة ببروتوكولات VPN التقليدية.

[توصي ](https://ivpn.net/wireguard)IVPN باستخدام بروتوكول WireGuard مع خدمتها، ولذلك فهو مفعّل بشكل افتراضي في جميع تطبيقات IVPN. كما توفر IVPN أيضا أداة لتوليد إعدادات WireGuard لاستخدامها مع ت[طبيقات WireGuard الرسمية](https://wireguard.com/install).

#### :material-information-outline:{ .pg-blue } دعم لـ IPv6

تتيح لك IVPN [الاتصال بالخدمات التي تستخدم بروتوكول IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6)، ولكنها لا تسمح بالاتصال من جهاز يستخدم عنوان IPv6.

#### :material-alert-outline:{ .pg-orange } Remote Port Forwarding

كانت IVPN تدعم ميزة الـ (Port Forwarding) سابقا، لكنها أزالت هذه الخاصية في [يونيو 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). غياب هذه الميزة قد يؤثر سلبا على بعض التطبيقات، خصوصا تلك التي تعتمد على الاتصال (P2P) مثل برامج التورنت.

#### :material-check:{ .pg-green } مقاومة الرقابة

يقدم IVPN الـ (obfuscation modes) باستخدام [V2Ray](https://v2ray.com/en/index.html)، وهي مفيدة في الحالات التي يتم فيها حظر بروتوكولات VPN مثل OpenVPN أو WireGuard. حالياً، هذه الميزة متاحة فقط على أجهزة سطح المكتب (Desktop) ونظام [iOS](https://ivpn.net/knowledgebase/ios/v2ray). يوفر خيارين للتشغيل، حيث يمكنه استخدام بروتوكول [VMess ](https://guide.v2fly.org/en_US/basics/vmess.html)عبر اتصالات QUIC أو TCP. بروتوكول QUIC حديث ويُحسن طريقة انتقال البيانات، مما يساعد في زيادة السرعة وتقليل التأخير (latency) أثناء التصفح. في وضع TCP، يتم تغليف بياناتك لتبدو وكأنها بيانات تصفح عادية (HTTP)، مما يساعد في تجاوز الرقابة أو الحظر في بعض الشبكات.

#### :material-check:{ .pg-green } عملاء الهاتف المحمول

IVPN has published [App Store](https://apps.apple.com/app/id1193122683) and [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/ivpn/android-app/releases).

#### :material-information-outline:{ .pg-blue } Additional Notes

IVPN clients support two-factor authentication. IVPN also provides "[AntiTracker](https://ivpn.net/antitracker)" functionality, which blocks advertising networks and trackers from the network level.

### ملفاد

<div class="admonition recommendation" markdown>

![Mullvad logo](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** is a fast and inexpensive VPN with a serious focus on transparency and security. They have been in operation since 2009. Mullvad is based in Sweden and offers a 14-day money-back guarantee for [payment methods](https://mullvad.net/en/help/refunds) that allow it.

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

#### :material-check:{ .pg-green } 49 Countries

Mullvad has [servers in 49 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. This is because of a shorter route (fewer hops) to the destination.
{ .annotate }

1. Last checked: 2025-03-10

استخدام [خادم مخصص](https://en.wikipedia.org/wiki/Dedicated_hosting_service) يعني أن الشركة تملك الخادم وتتحكم فيه بالكامل، مما يقلل من خطر تسريب البيانات أو تعرضها للاختراق مقارنة [بخوادم مشتركة (VPS)](https://en.wikipedia.org/wiki/Virtual_private_server) تُستخدم من عدة عملاء.

#### :material-check:{ .pg-green } تمت مراجعته من جهة مستقلة

Mullvad has had multiple [independent audits](https://mullvad.net/en/blog/tag/audits) and has publicly announced their endeavors to conduct [annual audits](https://mullvad.net/en/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) of their apps and infrastructure.

#### :material-check:{ .pg-green } العملاء الذين يستخدمون برامج مفتوحة المصدر

Mullvad provides the source code for their desktop and mobile clients in their [GitHub organization](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } تقبل الدفع بوسائل خاصة مثل النقود وعملة مونيرو (Monero)

Mullvad, in addition to accepting credit/debit cards and PayPal, accepts Bitcoin, Bitcoin Cash, **Monero** and **cash/local currency** as anonymous forms of payment. Prepaid cards with redeem codes are also available. Mullvad also accepts Swish and bank wire transfers, as well as a few European payment systems.

#### :material-check:{ .pg-green } WireGuard Support

Mullvad supports the WireGuard® protocol. [WireGuard](https://wireguard.com) هو بروتوكول VPN جديد نسبيا، ويعتمد على [تشفير حديث ومتطور](https://wireguard.com/protocol) يوفّر أمانًا عاليا وكفاءة في الأداء. ويتميز WireGuard أيضا بتصميمه البسيط وأدائه العالي، مقارنة ببروتوكولات VPN التقليدية.

Mullvad [recommends](https://mullvad.net/en/help/why-wireguard) the use of WireGuard with their service. It is the default or only protocol on Mullvad's Android, iOS, macOS, and Linux apps, but on Windows you have to [manually enable](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-check:{ .pg-green } IPv6 Support

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) and connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } Remote Port Forwarding

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). غياب هذه الميزة قد يؤثر سلبا على بعض التطبيقات، خصوصا تلك التي تعتمد على الاتصال (P2P) مثل برامج التورنت.

#### :material-check:{ .pg-green } مقاومة الرقابة

Mullvad offers several features to help bypass censorship and access the internet freely:

- **Obfuscation modes**: Mullvad has two built-in obfuscation modes: "UDP-over-TCP" and ["WireGuard over Shadowsocks"](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard). These modes disguise your VPN traffic as regular web traffic, making it harder for censors to detect and block. Supposedly, China has to use a [new method to disrupt Shadowsocks-routed traffic](https://gfw.report/publications/usenixsecurity23/en).
- **Advanced obfuscation with Shadowsocks and v2ray**: For more advanced users, Mullvad provides a guide on how to use the [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) plugin with Mullvad clients. This setup provides an additional layer of obfuscation and encryption.
- **Custom server IPs**: To counter IP-blocking, you can request custom server IPs from Mullvad's support team. Once you receive the custom IPs, you can input the text file in the "Server IP override" settings, which will override the chosen server IP addresses with ones that aren't known to the censor.
- **Bridges and proxies**: Mullvad also allows you to use bridges or proxies to reach their API (needed for authentication), which can help bypass censorship attempts that block access to the API itself.

#### :material-check:{ .pg-green } عملاء الهاتف المحمول

Mullvad has published [App Store](https://apps.apple.com/app/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Additional Notes

Mullvad is very transparent about which nodes they [own or rent](https://mullvad.net/en/servers). They also provide the option to enable Defense Against AI-guided Traffic Analysis ([DAITA](https://mullvad.net/en/blog/daita-defense-against-ai-guided-traffic-analysis)) in their apps. DAITA protects against the threat of advanced traffic analysis which can be used to connect patterns in VPN traffic with specific websites.

## Criteria

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

It is important to note that using a VPN provider will not make you anonymous, but it will give you better privacy in certain situations. A VPN is not a tool for illegal activities. Don't rely on a "no log" policy.

</div>

**Please note we are not affiliated with any of the providers we recommend. This allows us to provide completely objective recommendations.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any VPN provider wishing to be recommended, including strong encryption, independent security audits, modern technology, and more. We suggest you familiarize yourself with this list before choosing a VPN provider, and conduct your own research to ensure the VPN provider you choose is as trustworthy as possible.

### Technology

We require all our recommended VPN providers to provide standard configuration files which can be used in a generic, open-source client. **If** a VPN provides their own custom client, we require a kill switch to block network data leaks when disconnected.

**Minimum to Qualify:**

- Support for strong protocols such as WireGuard.
- Kill switch built in to clients.
- Multi-hop support. Multi-hopping is important to keep data private in case of a single node compromise.
- If VPN clients are provided, they should be [open source](https://en.wikipedia.org/wiki/Open_source), like the VPN software they generally have built into them. We believe that [source code](https://en.wikipedia.org/wiki/Source_code) availability provides greater transparency about what the program is actually doing.
- Censorship resistance features designed to bypass firewalls without DPI.

**Best Case:**

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

**Best Case:**

- Accepts multiple [anonymous payment options](advanced/payments.md).
- No personal information accepted (auto-generated username, no email required, etc.).

### Security

A VPN is pointless if it can't even provide adequate security. We require all our recommended providers to abide by current security standards. Ideally, they would use more future-proof encryption schemes by default. We also require an independent third-party to audit the provider's security, ideally in a very comprehensive manner and on a repeated (yearly) basis.

**Minimum to Qualify:**

- Strong Encryption Schemes: OpenVPN with SHA-256 authentication; RSA-2048 or better handshake; AES-256-GCM or AES-256-CBC data encryption.
- Forward Secrecy.
- Published security audits from a reputable third-party firm.
- VPN servers that use full-disk encryption or are RAM-only.

**Best Case:**

- Strongest Encryption: RSA-4096.
- Optional quantum-resistant encryption.
- Forward Secrecy.
- Comprehensive published security audits from a reputable third-party firm.
- Bug-bounty programs and/or a coordinated vulnerability-disclosure process.
- RAM-only VPN servers.

### Trust

You wouldn't trust your finances to someone with a fake identity, so why trust them with your internet data? We require our recommended providers to be public about their ownership or leadership. We also would like to see frequent transparency reports, especially in regard to how government requests are handled.

**Minimum to Qualify:**

- Public-facing leadership or ownership.
- Company based in a jurisdiction where it cannot be forced to do secret logging.

**Best Case:**

- Public-facing leadership.
- Frequent transparency reports.

### Marketing

With the VPN providers we recommend we like to see responsible marketing.

**Minimum to Qualify:**

- Must self-host analytics (i.e., no Google Analytics).

Must not have any marketing which is irresponsible:

- Making guarantees of protecting anonymity 100%. When someone makes a claim that something is 100% it means there is no certainty for failure. We know people can quite easily deanonymize themselves in a number of ways, e.g.:
    - Reusing personal information (e.g., email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
    - [Browser fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Claim that a single circuit VPN is "more anonymous" than Tor, which is a circuit of three or more hops that regularly changes.
- Use responsible language: i.e., it is okay to say that a VPN is "disconnected" or "not connected", however claiming that someone is "exposed", "vulnerable" or "compromised" is needless use of alarming language that may be incorrect. For example, that person might simply be on another VPN provider's service or using Tor.

**Best Case:**

Responsible marketing that is both educational and useful to the consumer could include:

- An accurate comparison to when [Tor](tor.md) should be used instead.
- Availability of the VPN provider's website over a [.onion service](https://en.wikipedia.org/wiki/.onion)

### Additional Functionality

While not strictly requirements, there are some factors we looked into when determining which providers to recommend. These include content blocking functionality, warrant canaries, excellent customer support, the number of allowed simultaneous connections, etc.
