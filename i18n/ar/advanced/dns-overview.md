---
title: "نظرة عامة على DNS"
icon: material/dns
description: نظام أسماء النطاقات DNS يشبه دليل الهاتف للإنترنت؛ فهو يساعد المتصفح على العثور على الموقع الذي تريد زيارته.
---

يُعد [نظام أسماء النطاقات (DNS)](https://en.wikipedia.org/wiki/Domain_Name_System) بمثابة “دليل الهاتف للإنترنت”. عندما تكتب اسم موقع، يحوله DNS إلى عنوان IP، حتى يعرف المتصفح أين يجد الموقع، وذلك عبر شبكة من الخوادم المنتشرة.

## ما هو الـ DNS؟

عندما تفتح موقعا، يحصل المتصفح على عنوان رقمي يساعده في الوصول إليه. مثلا، عند فتح `privacyguides.org`، يحصل المتصفح على العنوان `192.98.54.105`.

ظهر DNS منذ [البدايات الأولى](https://en.wikipedia.org/wiki/Domain_Name_System#History) للإنترنت. غالبًا ما تكون طلبات الـ DNS بين جهازك وخوادم الـ DNS **غير** مشفرة. عادةً في المنزل، يعطي مزود خدمة الإنترنت (ISP) جهازك خوادم DNS باستخدام [DHCP](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol).

طلبات DNS غير المشفرة يمكن أن **تُراقَب** و**تُعدل** بسهولة وهي في طريقها بين جهازك والخادم. في بعض البلدان، يُطلب من مزودي خدمة الإنترنت استخدام طريقة بسيطة في [تصفية DNS (DNS filtering)](https://en.wikipedia.org/wiki/DNS_blocking) لحجب بعض المواقع. إذا طلبت عنوان IP لموقع محجوب، فقد لا يستجيب الخادم، أو قد يعطيك عنوان IP مختلفا. لأن DNS غير مشفر، يستطيع مزود خدمة الإنترنت أو مشغل الشبكة استخدام [DPI](https://en.wikipedia.org/wiki/Deep_packet_inspection) لرؤية الطلبات التي ترسلها. قد يحجب مزود خدمة الإنترنت بعض الطلبات لأنها تشبه طلبات معينة، حتى لو كنت تستخدم خادم DNS مختلفا.

في القسم التالي، نوضح بتجربة بسيطة ما الذي قد يراه شخص يراقب من الخارج عند استخدام DNS عادي غير مشفر و[DNS مشفر](#what-is-encrypted-dns).

### الـ DNS غير المشفر

1. من خلال [`tshark`](https://wireshark.org/docs/man-pages/tshark.html)، وهو جزء من [Wireshark](https://en.wikipedia.org/wiki/Wireshark)، نستطيع رؤية حزم الإنترنت (الـ internet packets) أثناء انتقالها وتسجيلها. هذا الأمر يسجل حزم البيانات (الـ packets) التي توافق الشروط المحددة:

    ```bash
    tshark -w /tmp/dns.pcap udp port 53 and host 1.1.1.1 or host 8.8.8.8
    ```

2. بعدها، نستخدم [`dig`](https://en.wikipedia.org/wiki/Dig_(command)) على Linux وmacOS، أو [`nslookup`](https://en.wikipedia.org/wiki/Nslookup) على Windows، لنسأل كلا الخادمين عن عنوان DNS. البرامج، مثل المتصفحات، تسأل عن عناوين الـ DNS تلقائيا، إلا إذا تم ضبطها على استخدام DNS مشفر.

    === "Linux, macOS"

        ```
        dig +noall +answer privacyguides.org @1.1.1.1
        dig +noall +answer privacyguides.org @8.8.8.8
        ```
    === "Linux, macOS"

        ```
        nslookup privacyguides.org 1.1.1.1
        nslookup privacyguides.org 8.8.8.8
        ```

3. بعد ذلك، نريد [تحليل](https://wireshark.org/docs/wsug_html_chunked/ChapterIntroduction.html#ChIntroWhatIs) النتائج:

    === "Wireshark"

        ```
        wireshark -r /tmp/dns.pcap
        ```

    === "tshark"

        ```
        tshark -r /tmp/dns.pcap
        ```

عند تشغيل أمر Wireshark السابق، سترى في الجزء العلوي “[الإطارات (الـ frames)](https://en.wikipedia.org/wiki/Ethernet_frame)”، وفي الجزء السفلي ستظهر جميع المعلومات عن الإطار (الـ frame) الذي اخترته. تستطيع أنظمة التصفية والمراقبة الخاصة (الـ filtering and monitoring) بالمؤسسات، مثل الأنظمة التي تشتريها الحكومات، القيام بهذه العملية تلقائيا من دون أي تدخل من الإنسان، ثم جمع هذه الإطارات (الـ frames) لاستخراج بيانات إحصائية يستفيد منها مراقب الشبكة.

| No. | Time     | Source    | Destination | Protocol | Length | Info                                                                   |
| --- | -------- | --------- | ----------- | -------- | ------ | ---------------------------------------------------------------------- |
| 1   | 0.000000 | 192.0.2.1 | 1.1.1.1     | DNS      | 104    | Standard query 0x58ba A privacyguides.org OPT                          |
| 2   | 0.293395 | 1.1.1.1   | 192.0.2.1   | DNS      | 108    | Standard query response 0x58ba A privacyguides.org A 198.98.54.105 OPT |
| 3   | 1.682109 | 192.0.2.1 | 8.8.8.8     | DNS      | 104    | Standard query 0xf1a9 A privacyguides.org OPT                          |
| 4   | 2.154698 | 8.8.8.8   | 192.0.2.1   | DNS      | 108    | Standard query response 0xf1a9 A privacyguides.org A 198.98.54.105 OPT |

يمكن للمراقب تعديل أي من هذه الحزم (الـ packets).

## ما هو "الـ DNS المشفر"؟

عند الحديث عن الـ DNS المشفر، فقد نقصد واحدا من عدة طرق لحماية طلبات الـ DNS، مثل [DNSCrypt](#dnscrypt) و[DNS over TLS](#dns-over-tls-dot) و[DNS over HTTPS](#dns-over-https-doh).

### DNSCrypt

كان [**DNSCrypt**](https://en.wikipedia.org/wiki/DNSCrypt) من أوائل الطرق التي جعلت طلبات الـ DNS محمية بالتشفير. يستخدم DNSCrypt المنفذ (الـ port) 443، ويمكنه إرسال البيانات باستخدام TCP أو UDP. لم يُقدم DNSCrypt رسميا إلى [فريق هندسة الإنترنت IETF](https://en.wikipedia.org/wiki/Internet_Engineering_Task_Force)، ولم يمر بخطوات [طلب التعليقات RFC](https://en.wikipedia.org/wiki/Request_for_Comments)، لذلك لم ينتشر كثيرا، وبقي مستخدما فقط في بعض [التطبيقات](https://dnscrypt.info/implementations). لذلك، أصبح الناس يستخدمون [DNS over HTTPS](#dns-over-https-doh) الأكثر انتشارا بدلا منه في أغلب الأحيان.

### DNS over TLS (DoT)

هناك طريقة أخرى لحماية اتصال DNS بالتشفير، وهي [**DNS over TLS**](https://en.wikipedia.org/wiki/DNS_over_TLS)، وقد شرحت في [RFC 7858](https://datatracker.ietf.org/doc/html/rfc7858). بدأت الأنظمة في دعم هذه الميزة مع Android 9 وiOS 14، وعلى Linux من خلال [systemd-resolved](https://freedesktop.org/software/systemd/man/resolved.conf.html#DNSOverTLS=) بدءً من الإصدار 237. في السنوات الأخيرة، صار المجال التقني يفضل DoH أكثر من DoT، لأن DoT [بروتوكول معقد](https://dnscrypt.info/faq)، ولأن تطبيقاته لا تتبع معيار RFC دائما بالطريقة نفسها. يعمل DoT على منفذ (port) خاص اسمه 853، لذلك يمكن للجدران النارية (الـ firewalls) الصارمة أن تحجبه بسهولة.

### DNS over TLS (DoT)

يعمل [**DNS over HTTPS**](https://en.wikipedia.org/wiki/DNS_over_HTTPS)، كما يشرحه [RFC 8484](https://datatracker.ietf.org/doc/html/rfc8484)، على إرسال طلبات DNS داخل [HTTP/2](https://en.wikipedia.org/wiki/HTTP/2)، ثم يحميها باستخدام HTTPS. بدأت بعض متصفحات الويب بدعم هذه الميزة، مثل Firefox 60 وChrome 83.

بدأت الأنظمة مثل iOS 14 وmacOS 11 وMicrosoft Windows وAndroid 13 بدعم DoH بشكل مدمج، ولكن هذا الدعم لا يكون [مفعلا تلقائيا](https://android-review.googlesource.com/c/platform/packages/modules/DnsResolver/+/1833144). على أجهزة Linux، ما زال الدعم العام ينتظر أن يوفر systemd هذه [الميزة](https://github.com/systemd/systemd/issues/8639)، لذلك تحتاج حاليًا إلى [تثبيت برنامج خارجي](../dns.md#encrypted-dns-proxies).

### دعم أنظمة التشغيل دون برامج إضافية

#### Android

يدعم أندرويد ٩ وما بعده أنظمة أسماء النطاقات عبر أمن طبقة النقل (DNS over TLS). تجد هذا الإعداد في: **الإعدادات** ← ** الشبكة والإنترنت ** ← **نظام أسماء نطاقات خاص**.

#### أجهزة أبل

تدعم آخر إصدارات آي‌أو‌إس و آيباد‌أو‌إس و تي‌في‌أو‌إس و ماك‌أو‌إس أنظمة DoT و DoH. يوجد دعم أصيل لهذه الموافيق باستخدام [ملفَّات تعريف الضبط](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) أو باستخدام [واجهة برمجة إعدادات نظام تسمية النطاقات](https://developer.apple.com/documentation/networkextension/dns_settings).

لك اختيار ضبط نظام تسمية النطاقات بعد تثبيت ملفِّ تعريف ضبط أو تثبيت تطبيق يستخدم واجهة برمجة إعدادات نظام تسمية النطاقات. إن كانت شبكة خاصَّة افتراضية (VPN) مفعَّلةً فسوف تُحلَّل الاتصالات داخلها باستخدام نظام تسمية نطاقاتها وليس باستخدام إعدادات نظامك.

لا تتيح أبل واجهةً أصيلةً لإنشاء ملفَّات تعريف معمَّاة. [مُنشئ ملفَّات تعريف نظام تسمية النطاقات الآمن](https://dns.notjakob.com/tool.html) هو أداة غير رسمية تتيح لك إنشاء ملفَّات تعريف نظام تسمية النطاقات معمَّاة، ولكن ضع في حسبانك أنها لن توقَّع. تفضَّل ملفَّات التعريف الموقَّعة على غيرها، وذلك ﻷن التوقيع يؤكِّد أصلها وصحَّتها. تعلَّم ملفَّات التعريف الموقَّعة بعلامة «مؤكَّد» خضراء. لتستزيد علمًا عن توقيع الرموز عليك مطالعة [عن توقيع الرموز](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html).

#### لينكس

تعتمد كثير من توزيعات Linux على `systemd-resolved` لإجراء طلبات الـ DNS، لكن هذه الأداة لا [تدعم DoH](https://github.com/systemd/systemd/issues/8639) بعد. إذا كنت تريد استخدام DoH، فعليك تثبيت وسيط مثل [dnscrypt-proxy](../dns.md#dnscrypt-proxy) و[ضبطه](https://wiki.archlinux.org/title/Dnscrypt-proxy) لكي يأخذ طلبات الـ DNS من النظام ويمررها عبر HTTPS.

## ما الذي يستطيع طرف خارجي رؤيته؟

في هذا المثال، سنسجل ما يحدث عندما نرسل طلب الـ DoH:

1. أولا، قم بتشغيل أداة `tshark`:

    ```bash
    tshark -w /tmp/dns_doh.pcap -f "tcp port https and host 1.1.1.1"
    ```

2. ثانيا، قم بإرسال طلب باستخدام `curl`:

    ```bash
    curl -vI --doh-url https://1.1.1.1/dns-query https://privacyguides.org
    ```

3. بعد إرسال الطلب، يمكنك إيقاف عملية التقاط الحزم بالضغط (packet capture) على <kbd>CTRL</kbd>+ <kbd>C</kbd>.

4. والآن، دعنا نُحلل البيانات التي حصلنا عليها في Wireshark:

    ```bash
    wireshark -r /tmp/dns_doh.pcap
    ```

يمكننا رؤية عملية [إنشاء الاتصال](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#Connection_establishment) و [TLS handshake](https://cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake) التي تحدث مع أي اتصال مشفر. إذا تصفحت حزم البيانات التالية الخاصة بالتطبيق، ستلاحظ أنها لا تُظهر اسم النطاق الذي طلبته ولا عنوان الـ IP الذي رجع إلينا، فالبيانات أصبحت مخفية تماما.

## لماذا **لا ينبغي** لي استخدام DNS مشفر؟

في الأماكن التي تفرض رقابة أو تصفية للإنترنت، قد تترتب على زيارة المصادر المحظورة عواقب خاصة بها، وهو أمر يجب عليك مراعاته في [نموذج التهديد ](../basics/threat-modeling.md)الخاص بك. **لا** نقترح استخدام DNS المشفر لهذا الغرض. استخدم [Tor](../advanced/tor-overview.md) أو [VPN](../vpn.md) بدلا من ذلك. إذا كنت تستخدم شبكة الـ VPN، فمن الضروري الاعتماد على خوادم الـ DNS الخاصة بمزود الخدمة نفسه. عند استخدام الـ VPN، فإنك تضع ثقتك الكاملة في مزود الخدمة بالفعل، وتأتمنه على كافة أنشطتك وتحركاتك عبر الشبكة.

عندما نقوم بإجراء استعلام من خلال الـ DNS، فغالبا ما يكون ذلك بسبب رغبتنا في الوصول إلى مصدر معين على الشبكة. في السطور التالية، سنناقش بعض الطرق التي قد تتسبب في كشف أنشطة تصفحك، حتى عند استخدامك لبروتوكول الـ DNS المشفّر:

### الـ IP Address

قد تكون أسهل طريقة لمعرفة نشاط تصفحك هي النظر إلى عناوين الـ IP التي تتصل بها أجهزتك. ببساطة، إذا كان من يراقب الشبكة يعلم مسبقا أن عنوان `privacyguides.org` هو `198.98.54.105`، ولاحظ أن جهازك يتصل بهذا العنوان تحديداً، فسوف يستنتج بسهولة أنك تتصفح موقع Privacy Guides.

تكون هذه الطريقة مفيدة فقط عندما ينتمي عنوان الـ IP إلى خادم (Server) يستضيف عددا قليلا من المواقع. كما أنها لا تكون مفيدة جدا إذا كان الموقع مستضافا على منصة مشتركة (مثل: GitHub Pages، و Cloudflare Pages، و Netlify، و WordPress، و Blogger، وغيرها). علاوة على ذلك، فإنه يفقد الكثير من فائدته إذا كانت استضافة الخادم تتم خلف [reverse proxy](https://en.wikipedia.org/wiki/Reverse_proxy).

### Server Name Indication (SNI)

يُستخدم الـ Server Name Indication عادة عندما يستضيف عنوان IP العديد من مواقع الويب. قد يتمثل ذلك في خدمة مثل Cloudflare، أو أي نظام آخر للحماية من هجمات الـ [(Denial-of-service attack)](https://en.wikipedia.org/wiki/Denial-of-service_attack).

1. ابدأ التتبع مرة أخرى باستخدام `tshark`. لقد أضفنا عامل تصفية بناءً على عنوان IP الخاص بنا، لكي تتجنب التقاط الكثير من الـ packets:

    ```bash
    tshark -w /tmp/pg.pcap port 443 and host 198.98.54.105
    ```

2. بعد ذلك، نقوم بزيارة [https://privacyguides.org](https://privacyguides.org).

3. بعد زيارة الموقع، نريد إيقاف تسجيل الـ packets بالضغط على <kbd>CTRL</kbd> + <kbd>C</kbd>.

4. بعد ذلك، نريد تحليل النتائج:

    ```bash
    wireshark -r /tmp/pg.pcap
    ```

    سنرى بدء الاتصال، وبعده الـ TLS handshake لموقع Privacy Guides. حوالي الـ frame رقم 5. سترى رسالة «Client Hello».

5. افتح رمز المثلث &#9656; بجوار كل حقل:

    ```text
    ▸ Transport Layer Security
      ▸ TLSv1.3 Record Layer: Handshake Protocol: Client Hello
        ▸ Handshake Protocol: Client Hello
          ▸ Extension: server_name (len=22)
            ▸ Server Name Indication extension
    ```

6. يمكننا ملاحظة قيمة SNI، وهي التي تفصح عن هوية موقع الويب الذي نقوم بزيارته. يمكن لأمر `tshark` أن يعطيك القيمة مباشرة لجميع الـ packets التي تحتوي على قيمة SNI:

    ```bash
    tshark -r /tmp/pg.pcap -Tfields -Y tls.handshake.extensions_server_name -e tls.handshake.extensions_server_name
    ```

وهذا يعني أنه حتى وإن استخدمنا خوادم الـ "Encrypted DNS"، فمن المرجح أن يُفصح عن النطاق عبر SNI. يجلب بروتوكول [TLS v1.3](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_1.3) معه تقنية [Encrypted Client Hello](https://blog.cloudflare.com/encrypted-client-hello)، مما يمنع حدوث هذا النوع من التسريبات.

الحكومات، وخاصة [الصين](https://zdnet.com/article/china-is-now-blocking-all-encrypted-https-traffic-using-tls-1-3-and-esni) [وروسيا](https://zdnet.com/article/russia-wants-to-ban-the-use-of-secure-protocols-such-as-tls-1-3-doh-dot-esni)، إما أنها بدأت بالفعل في [حظره](https://en.wikipedia.org/wiki/Server_Name_Indication#Encrypted_Client_Hello) أو أعربت عن رغبتها في القيام بذلك. مؤخرًا، روسيا بدأت في [حظر المواقع الأجنبية](https://github.com/net4people/bbs/issues/108) التي تعتمد على الـ [HTTP/3](https://en.wikipedia.org/wiki/HTTP/3). وهذا لأن بروتوكول [QUIC](https://en.wikipedia.org/wiki/QUIC) الذي يعتبر جزءًا من HTTP/3 يتطلب أن يكون `ClientHello` مشفرا أيضا.

### Online Certificate Status Protocol (OCSP)

هناك طريقة أخرى قد تجعل متصفحك يكشف المواقع التي تزورها، وهي عبر [الـ Online Certificate Status Protocol](https://en.wikipedia.org/wiki/Online_Certificate_Status_Protocol). عند دخولك إلى موقع يستخدم HTTPS، قد يتحقق المتصفح من [شهادة](https://en.wikipedia.org/wiki/Public_key_certificate) الموقع ليرى هل ما زالت صالحة أم تم إلغاؤها. عادة يستخدم المتصفح HTTP لفعل ذلك، وهذا يعني أن الطلب **غير** مشفر.

يحتوي طلب OCSP على["الرقم التسلسلي (serial number)](https://en.wikipedia.org/wiki/Public_key_certificate#Common_fields)" للشهادة، وهو[رقم](https://en.wikipedia.org/wiki/Public_key_certificate#Common_fields) فريد من نوعه. يرسل المتصفح هذا الطلب إلى “الـ OCSP responder” حتى يتأكد من حالة الشهادة.

نستطيع تقليد ما يقوم به المتصفح باستخدام أمر [`openssl`](https://en.wikipedia.org/wiki/OpenSSL).

1. احصل على شهادة الخادم، ثم استخدم [`sed`](https://en.wikipedia.org/wiki/Sed) حتى تحفظ الجزء المهم فقط في ملف:

    ```bash
    openssl s_client -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_server.cert
    ```

2. احصل على الشهادة الوسيطة. عادةً لا توقّع [الـ CA](https://en.wikipedia.org/wiki/Certificate_authority) الشهادة مباشرةً، بل تستخدم شهادة أخرى في المنتصف تُسمّى “الشهادة الوسيطة (intermediate" certificate)”.

    ```bash
    openssl s_client -showcerts -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_and_intermediate.cert
    ```

3. أول شهادة داخل `pg_and_intermediate.cert` هي في الحقيقة شهادة الخادم من الخطوة الأولى. نستطيع استخدام `sed` مجددا لحذف كل ما يسبق أول ظهور لـ END:

    ```bash
    sed -n '/^-*END CERTIFICATE-*$/!d;:a n;p;ba' \
        /tmp/pg_and_intermediate.cert > /tmp/intermediate_chain.cert
    ```

4. استخرج OCSP responder من شهادة الخادم:

    ```bash
    openssl x509 -noout -ocsp_uri -in /tmp/pg_server.cert
    ```

    تبين الشهادة لدينا الـ Lets Encrypt certificate responder. إذا أردنا رؤية كل تفاصيل الشهادة، يمكننا استخدام الأمر التالي:

    ```bash
    openssl x509 -text -noout -in /tmp/pg_server.cert
    ```

5. ابدأ التقاط حزم البيانات (الـ packet):

    ```bash
    tshark -w /tmp/pg_ocsp.pcap -f "tcp port http"
    ```

6. قم بإرسال طلب الـ OCSP:

    ```bash
    openssl ocsp -issuer /tmp/intermediate_chain.cert \
                 -cert /tmp/pg_server.cert \
                 -text \
                 -url http://r3.o.lencr.org
    ```

7. Open the capture:

    ```bash
    wireshark -r /tmp/pg_ocsp.pcap
    ```

    سترى حزمتين مرتبطتين ببروتوكول “OCSP”: واحدة ترسل الطلب “Request”، والأخرى تحمل الرد “Response”. في طلب “Request”، يمكنك إظهار “الرقم التسلسلي (الـ serial number)” عن طريق فتح المثلث &#9656; الموجود بجانب كل خانة:

    ```bash
    ▸ Online Certificate Status Protocol
      ▸ tbsRequest
        ▸ requestList: 1 item
          ▸ Request
            ▸ reqCert
              serialNumber
    ```

    في الاستجابة “Response”، يظهر “الرقم التسلسلي (الـ serial number)” أيضا:

    ```bash
    ▸ Online Certificate Status Protocol
      ▸ responseBytes
        ▸ BasicOCSPResponse
          ▸ tbsResponseData
            ▸ responses: 1 item
              ▸ SingleResponse
                ▸ certID
                  serialNumber
    ```

8. أو استخدم `tshark` للبحث داخل الحزم (الـ packets) عن الرقم التسلسلي (الـ serial number):

    ```bash
    tshark -r /tmp/pg_ocsp.pcap -Tfields -Y ocsp.serialNumber -e ocsp.serialNumber
    ```

بما أن الشهادة العامة (public certificate) متاحة للجميع، يمكن لمراقب الشبكة مقارنة الرقم التسلسلي (الـ serial number) بها، ثم يعرف من ذلك الموقع الذي تزوره. يمكن جعل هذه العملية تعمل تلقائيا، فتربط بين عناوين IP والأرقام التسلسلية (الـ serial numbers). يمكن أيضا البحث داخل سجلات الـ [Certificate Transparency](https://en.wikipedia.org/wiki/Certificate_Transparency) عن هذا الرقم التسلسلي (serial number).

## هل ينبغي أن أستخدم DNS مشفرا؟

صممنا هذا المخطط الانسيابي لمساعدتك على معرفة متى *ينبغي* استخدام DNS مشفر:

``` mermaid
Start[البداية] --> anonymous{هل تحاول أن تكون<br> مجهول الهوية؟}
    anonymous --> | نعم | tor(استخدم Tor)
anonymous --> | لا | censorship{هل تحاول تجنب<br> الرقابة؟}
    censorship --> | نعم | vpnOrTor(استخدم<br> VPN أو Tor)
censorship --> | لا | privacy{هل تريد حماية خصوصيتك<br> من مزوّد خدمة الإنترنت؟}
    privacy --> | نعم | vpnOrTor
privacy --> | لا | obnoxious{هل يقوم مزوّد خدمة الإنترنت<br> بإعادة توجيه مزعجة؟<br>}
    obnoxious --> | نعم | encryptedDNS(استخدم<br> DNS مشفرا<br> من مزود آخر)
obnoxious --> | لا | ispDNS{هل يوفر مزوّد خدمة الإنترنت<br> DNS مشفرا؟}
    ispDNS --> | نعم | useISP(استخدم<br> DNS مشفرا<br> من مزود خدمة الإنترنت)
ispDNS --> | لا | nothing(لا تحتاج إلى فعل شيء)
```

لا تستخدم DNS مشفرا من مزود آخر إلا إذا كنت تريد تجاوز إعادة التوجيه أو [ الـ DNS blocking ](https://en.wikipedia.org/wiki/DNS_blocking)، وكنت متأكدا من أن ذلك لن يسبب لك مشكلة، أو إذا كنت تريد مزودا يوفر بعض التصفية البسيطة.

[قائمة خوادم الـ DNS الموصى بها](../dns.md ""){.md-button}

## ما هو الـ DNSSEC؟

[](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) (DNSSEC) هي ميزة في DNS تساعد على التأكد من أن الردود على طلبات أسماء النطاقات صحيحة. هي لا تحمي خصوصية هذه الطلبات، بل تمنع المهاجمين من تغيير ردود الـ DNS أو إفسادها.

بمعنى أبسط، يضيف DNSSEC توقيعا رقميا إلى البيانات حتى يساعد على التأكد من أنها صحيحة. حتى يكون استعلام الـ DNS آمنا، يحدث التوقيع في كل مرحلة من مراحل عملية البحث. ونتيجة لذلك، يمكن الوثوق بجميع الردود القادمة من DNS.

يمكن تشبيه توقيع DNSSEC بتوقيع شخص على ورقة قانونية بقلم؛ فلكل شخص توقيع مميز لا يستطيع الآخرون تقليده، ويمكن للخبير أن يفحصه ويتأكد من أن الشخص نفسه هو من وقع الوثيقة. تساعد هذه التوقيعات الرقمية على التأكد من أن البيانات لم يتم تغييرها أو العبث بها.

يطبق DNSSEC سياسة توقيع رقمي هرمية عبر جميع طبقات DNS. على سبيل المثال، عند البحث عن `privacyguides.org`، سيقوم خادم الـ root بتوقيع مفتاح لخادم أسماء `.org`، وبعدها سيقوم خادم أسماء `.org` بتوقيع مفتاح للخادم الرئيسي الخاص بـ `privacyguides.org`.

<small>مقتبس من [نظرة عامة على ملحقات أمان DNS (DNSSEC)](https://docs.cloud.google.com/dns/docs/dnssec) بواسطة Google و[DNSSEC: مقدمة](https://blog.cloudflare.com/dnssec-an-introduction) بواسطة Cloudflare، وكلاهما مرخص بموجب [CC BY 4.0](https://creativecommons.org/licenses/by/4.0).</small>

## ما هو الـ QNAME minimization؟

يشير QNAME إلى "qualified name" (Qualified Name)، مثل `discuss.privacyguides.net`. سابقًا، عند البحث عن أي دومين، كان الـ DNS resolver الخاص بك يسأل كل سيرفر في الشبكة لتقديم أي معلومات يملكها عن طلبك بالكامل. في المثال أدناه، يتم توجيه طلبك للعثور على عنوان IP الخاص بـ `discuss.privacyguides.net` إلى كل مزود لخوادم DNS:

| خادم                  | الأسئلة المطروحة                                | الرد                                   |
| --------------------- | ----------------------------------------------- | -------------------------------------- |
| الخادم الأساسي        | ما هو عنوان IP لموقع discuss.privacyguides.net؟ | لا أعرف، اسأل خادم .net...             |
| خادم .net             | ما هو عنوان IP لموقع discuss.privacyguides.net؟ | لا أعرف، اسأل خادم «Privacy Guides»... |
| خادم «Privacy Guides» | ما هو عنوان IP لموقع discuss.privacyguides.net؟ | 5.161.195.190!                         |

باستخدام "QNAME minimization"، لا يطلب الـ DNS resolver الخاص بك الآن سوى المعلومات الضرورية فقط لإيجاد الخادم التالي في الشبكة. في هذا المثال، يُسأل الخادم الأساسي فقط عن معلومات كافية لإيجاد خادم الـ nameserver الملائم لامتداد .net (TLD)، وهكذا، من دون أن يعرف أبدًا الدومين بالكامل الذي تحاول زيارته:

| خادم                  | الأسئلة المطروحة                                                     | الرد                                  |
| --------------------- | -------------------------------------------------------------------- | ------------------------------------- |
| الخادم الأساسي        | ما هو خادم الـ nameserver الخاص بنطاق .net؟                          | *يقوم بتوفير خادم الـ .net*           |
| خادم .net             | ما هو خادم الـ nameserver الخاص بنطاق الـ privacyguides.net؟         | *يوفر الخادم الخاص بـ Privacy Guides* |
| خادم «Privacy Guides» | ما هو خادم الـ nameserver الخاص بنطاق الـ discuss.privacyguides.net؟ | هذا الخادم!                           |
| خادم «Privacy Guides» | ما هو عنوان IP لموقع discuss.privacyguides.net؟                      | 5.161.195.190                         |

مع أن هذه الطريقة قد تكون أبطأ قليلًا، ففي هذا المثال لا تستلم خوادم الـ root المركزية ولا خوادم الـ TLD أي معلومات أبدًا عن طلبك *بالكامل*، وبالتالي يقل حجم البيانات التي يتم نقلها عن عادات التصفح الخاصة بك. توجد تفاصيل تقنية إضافية في [RFC 7816](https://datatracker.ietf.org/doc/html/rfc7816).

## ما هي الـ EDNS Client Subnet (ECS)؟

تُعد تقنية [EDNS Client Subnet](https://en.wikipedia.org/wiki/EDNS_Client_Subnet) طريقة تتيح للـ recursive DNS resolver تحديد[ شبكة فرعية](https://en.wikipedia.org/wiki/Subnetwork) لـالمضيف أو العميل الذي يقوم بإجراء استعلام DNS.</p> 

الهدف منها هو "تسريع" توصيل البيانات عن طريق تزويد العميل بإجابة من خادم قريب منه، مثل [شبكة توصيل المحتوى (CDN)](https://en.wikipedia.org/wiki/Content_delivery_network)، والتي تُستخدم غالبًا في بث الفيديو وتقديم تطبيقات الـ javascript.

إلا أن هذه الميزة لها سلبيتها على الخصوصية؛ فهي تخبر خادم الـ DNS ببعض المعلومات عن الموقع الجغرافي للعميل، وبشكل عام الـ IP الخاصة بك. على سبيل المثال، في حال كان عنوان IP لديك هو `198.51.100.32`، فإن مزود خدمة الـ DNS قد يشارك النطاق `198.51.100.0/24` مع الخادم المعتمد. يقوم بعض مزودي خدمة الـ DNS بإخفاء هوية هذه البيانات من خلال تقديم عنوان IP آخر قريب تقريبًا من موقعك.

إذا كان لديك `dig` مثبتًا، يمكنك فحص ما إذا كان مزود الـ DNS الخاص بك يشارك معلومات EDNS مع سيرفرات الـ DNS nameservers عبر هذا الأمر:



```bash
dig +nocmd -t txt o-o.myaddr.l.google.com +nocomments +noall +answer +stats
```


يرجى ملاحظة أن هذا الأمر سيتصل بـ Google لإجراء الاختبار، وسيعرض عنوان IP الخاص بك بالإضافة إلى معلومات الـ EDNS client subnet. إذا كنت ترغب في اختبار DNS resolver آخر، يمكنك تحديد عنوان IP الخاص به، لاختبار` 9.9.9.11` على سبيل المثال:



```bash
dig +nocmd @9.9.9.11 -t txt o-o.myaddr.l.google.com +nocomments +noall +answer +stats
```


إذا تضمنت النتائج سجل الـ edns0-client-subnet TXT ثان (كما هو موضح أدناه)، فهذا يعني أن خادم DNS الخاص بك يمرر معلومات الـ EDNS. الـ IP أو الشبكة التي تظهر بعد ذلك هي بالضبط المعلومات التي تمت مشاركتها مع Google بواسطة مزود الـ DNS الخاص بك.



```text
o-o.myaddr.l.google.com. 60 IN TXT "198.51.100.32"
o-o.myaddr.l.google.com. 60 IN TXT "edns0-client-subnet 198.51.100.0/24"
;; Query time: 64 msec
;; SERVER: 9.9.9.11#53(9.9.9.11)
;; WHEN: Wed Mar 13 10:23:08 CDT 2024
;; MSG SIZE  rcvd: 130
```
