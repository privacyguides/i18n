---
meta_title: "متصفح وشبكة Tor: التصفح المجهول للويب – Privacy Guides"
title: "متصفح Tor"
icon: simple/torbrowser
description: استخدم شبكة Tor لحماية نشاطك على الإنترنت من المراقبة، فهي شبكة آمنة تمكنك من تصفح الويب بحرية وتجاوز الحجب والرقابة.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: متصفِّح تور
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
    sameAs: https://en.wikipedia.org/wiki/Tor_(network)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>يُوفر الحماية من التهديدات التالية:</small>

- [:material-account-cash: رأسمالية المراقبة](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: مراقبة الجمهور](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: الرقابة](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

**Tor** عبارة عن شبكة يديرها متطوعون، تتيح لك الاتصال مجانا بالإنترنت بطريقة تحافظ على خصوصيتك وتحميك من التتبع والمراقبة. ويمكن للأفراد والمؤسسات مشاركة المعلومات عبرها باستخدام «خدمات .onion الخفية»، وذلك دون نهك خصوصيتهم. فكون اتصالات تور صعبة الحظر والتتبع يجعل تور أداةً فعَّالةً لتجاوز الرقابة.

[نظرة مفصلة على Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: فيديو: لماذا تحتاج إلى Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">نصيحة</p>

تأكد من قراءة [نظرة عامة](advanced/tor-overview.md) على Tor قبل الاتصال، لتتعرف على طريقة عملها وكيفية الاتصال بها بشكل آمن. نوصي أحيانا باستخدام [VPN موثوق](vpn.md) قبل الاتصال بـ Tor لزيادة الخصوصية، لكن يجب تنفيذ ذلك بشكل سليم، لأن الإعداد الخاطئ قد **يقلل** من مستوى الحماية التي يوفرها Tor.

</div>

توجد عدة طرق للاتصال بشبكة Tor من جهازك، وأكثرها شيوعا هو استخدام **متصفح Tor**، وهو إصدار مشتق من Firefox مُصمم خصيصا لـ[:material-incognito: التصفح المجهول](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} على أجهزة الكمبيوتر وأنظمة أندرويد.

ليست كل هذه التطبيقات متساوية في مستوى الحماية، والقرار الأفضل يعتمد على ما تريد حمايته، ومن تحاول حماية نفسك منه — وهذا ما يُعرف بـ نموذج التهديد. إذا كنت مستخدما عاديا لـ Tor ولا تقلق بشأن قيام مزود خدمة الإنترنت بجمع معلومات ضدك، فإن استخدام تطبيقات تصفح مثل [Onion Browser](#onion-browser-ios) للوصول إلى شبكة Tor سيكون مناسبا على الأرجح. استخدامك لـ Tor في حياتك اليومية لا يحميك فقط، بل يساعد في حماية الآخرين أيضا. كلما زاد عدد المستخدمين، أصبحت شبكة Tor أكثر قوة، وانخفضت قدرة مزودي الإنترنت والحكومات على تتبع الأفراد أو وصمهم باستخدامها. ساهم في كسر الصورة النمطية السلبية واجعل الخصوصية عادة طبيعية للجميع.

إذا كانت حماية هويتك بشكل كامل أمرا ضروريا مثل حال الصحفيين أو المبلغين عن الفساد أو النشطاء في بيئات خطرة فاستخدم **فقط **نسخة سطح المكتب من متصفح Tor، ويفضل أن تستخدمه داخل نظامي [Whonix](desktop.md#whonix) و[Qubes](desktop.md#qubes-os)، لأنهما يوفران طبقات إضافية من الحماية والعزل. استخدام Tor على الهاتف أقل انتشارا، وهذا يجعل المتصفح أسهل في التعرف عليه وتتبعك. كما أن الطرق الأخرى لا يتم اختبارها بنفس الدقة لحمايتك من كشف الهوية.

## متصفِّح تور

<div class="admonition recommendation" markdown>

![Tor Browser logo](assets/img/browsers/tor.svg){ align=right }

متصفح Tor هو الخيار الأفضل إذا كنت بحاجة إلى إخفاء الهوية، لأنه يتيح لك الاتصال بشبكة Tor، ويوفر إمكانية استخدام ما يُعرف بـ (Bridges) — وهي نقاط دخول خاصة تُستخدم لتجاوز الحجب والرقابة في بعض الدول.

المتصفح يأتي أيضا بإعدادات افتراضية وإضافات معدة مسبقا، مرتّبة ضمن 3 مستويات أمان يمكنك الاختيار منها حسب احتياجك، Standard (عادي) لتجربة استخدام كاملة، Safer (أكثر أمانا) لتعطيل بعض العناصر الخطرة في المواقع، Safest (الأكثر أمانا) لتعطيل معظم الوظائف غير الضرورية وتقديم أقصى حماية.

[:octicons-home-16: الصفحة الرئيسية](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title="الشروحات التفصيلية" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title="المساهمة" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:fontawesome-brands-windows: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">خطر</p>

لا تثبِّت أيَّ إضافات في متصفِّح تور **أبدًا**، ولا تحرِّر إعدادات ‹about:config›، ويشمل ذلك ما نقترحه في فيرفكس. تميِّزك الإضافات والإعدادات المختلفة عن البقية في شبكة تور، وهذه يسهِّل تبصيم [fingerprint](https://support.torproject.org/glossary/browser-fingerprinting) متصفِّحك.

</div>

صمِّم متصفِّح تور لمكافحة التبصيم، أو كشف هويَّتك حسب ضبط متصفِّحك. ولهذا السبب، من المهم جدا أن **لا تغير** إعدادات متصفح Tor خارج [المستويات الأمنية المضمنة](https://tb-manual.torproject.org/security-settings)، لأن أي تعديل قد يعرضك لخطر كشف الهوية. إذا قمت بتغيير مستوى الأمان، **من الضروري** إعادة تشغيل متصفح Tor لتطبيق التغييرات بشكل صحيح قبل مواصلة التصفح. وإلا، فقد لا تُطبَّق [إعدادات الأمان بشكل كامل](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw)، مما قد يعرّضك لخطر التتبع واستغلال الثغرات، مقارنة بما تتوقعه من مستوى الأمان الذي اخترته.

بالإضافة إلى إمكانية تثبيت متصفح Tor مباشرة على جهازك، هناك أيضا أنظمة تشغيل صُممت خصيصا لاستخدام شبكة Tor، مثل [Whonix](desktop.md#whonix) ضمن [Qubes OS](desktop.md#qubes-os)، والتي توفر مستوى أعلى من الأمان والحماية مقارنة باستخدام متصفح Tor فقط.

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** هو متصفح مفتوح المصدر يتيح لك تصفح الإنترنت بشكل مجهول عبر شبكة Tor على أجهزة iOS، وهو مدعوم رسميا من قِبل [مشروع Tor](https://support.torproject.org/glossary/onion-browser).

[:material-star-box: اطّلع على آخر مراجعة قمنا بها لمتصفح Onion Browser.](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review)

[:octicons-home-16: الصفحة الرئيسية](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="سياسة الخصوصية" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title="الشروحات التفصيلية" }
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title="المساهمة" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

رغم أن متصفح Onion Browser يتيح التصفح المجهول على أجهزة iOS، إلا أنه لا يوفر نفس مستوى حماية الخصوصية الذي يقدمه متصفح Tor على أجهزة سطح المكتب (Desktop). ويعود ذلك إلى قيود نظام iOS، مثل إجبار جميع المتصفحات على استخدام محرك WebKit من Apple، مما يُقيد بعض ميزات Tor المتقدمة، ويجعل من الصعب توفير نفس درجة العزل والتخصيص الأمني (security customization) المتاحة على أنظمة مثل Linux أو Windows. للاستخدام العادي، يعتبر Onion Browser وسيلة مناسبة تماما للوصول إلى الخدمات المخفية. لكن إذا كنت قلقا بشأن التتبع أو المراقبة من جهات متقدمة، فلا يجب الاعتماد عليه كأداة لإخفاء الهوية.

[جدير بالانتباه](https://github.com/privacyguides/privacyguides.org/issues/2929) أن Onion Browser *لا يضمن* دائما أن يتم توجيه كل حركة الاتصال (requests) عبر Tor، مما قد يشكل خطرا على الخصوصية في بعض الحالات. انتبه: عند استخدام Tor داخل Onion Browser، قد **يتم كشف عنوان IP الحقيقي** عبر ميزات مثل WebRTC أو مكالمات الصوت والفيديو، بسبب قيود WebKit في iOS، كما هو موضح في [الأسئلة الشائعة](https://onionbrowser.com/faqs). يُعتبر استخدام Onion Browser مع [Orbot](alternative-networks.md#orbot) خيارا *أكثر أمانا*، لكنه لا يزيل تماما القيود التقنية التي يفرضها نظام iOS، مثل قيود WebKit.
