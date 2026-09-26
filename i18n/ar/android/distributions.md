---
meta_title: "أفضل أنظمة تشغيل أندرويد — دليل الخصوصية"
title: توزيعات أندرويد البديلة
description: يمكنك استبدال نظام التشغيل على هاتف أندرويد بأحد هذه البدائل الآمنة والتي تحترم خصوصيتك.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Private Android Operating Systems
    url: "./"
  - "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>يحمي من التهديدات التالية:</small>

- [:material-target-account: الهجمات الموجّهة **Targeted Attacks**](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: الهجمات السلبية **Passive Attacks**](../basics/common-threats.md#security-and-privacy){ .pg-orange }

يمكن أن يكون استخدام custom Android-based operating system (والذي يُشار إليه أحيانًا باسم custom ROM) وسيلة لتحقيق مستوى أعلى من الخصوصية والأمان على جهازك. وهذا يختلف عن إصدار Android الـ "stock" الذي يأتي مثبتا على هاتفك من المصنع، والذي غالبًا ما يكون مدمجًا بشكل كبير مع Google Play Services بالإضافة إلى برمجيات أخرى خاصة بالشركة المصنعة.

نوصي بتثبيت GrapheneOS إذا كان لديك هاتف Google Pixel، لأنه يوفر تقوية أمنية (Security Hardening) محسنة وميزات إضافية للخصوصية. الأسباب التي تجعلنا لا ندرج أنظمة تشغيل أو أجهزة أخرى هي كما يلي:

- غالبًا ما تكون لديهم حماية [ أمنية أضعف](index.md#install-a-custom-distribution).
- غالبا ما يتوقف الدعم عندما يفقد المطور المسؤول اهتمامه بالمشروع أو يغير جهازه إلى جهاز أحدث، وهذا على عكس [دورة الدعم](https://grapheneos.org/faq#device-lifetime) المتوقعة والواضحة التي يتبعها GrapheneOS.
- بشكل عام، لا تقدم هذه الأنظمة تحسينات ملحوظة في الخصوصية أو الأمان، أو تقدم تحسينات قليلة جدا، بحيث لا يكون تثبيتها مستحقا للعناء.

## GrapheneOS

<div class="admonition recommendation" markdown>

![GrapheneOS logo](../assets/img/android/grapheneos.svg#only-light){ align=right }
![GrapheneOS logo](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

يُعد **GrapheneOS** الخيار الأفضل عندما يتعلق الأمر بالخصوصية والأمان.

يوفر GrapheneOS المزيد من تحسينات [التقوية الأمنية](https://en.wikipedia.org/wiki/Hardening_(computing) (Security Hardening) وميزات إضافية لتعزيز الخصوصية. يحتوي على [مُخصص ذاكرة مُعزز](https://github.com/GrapheneOS/hardened_malloc) (Hardened Memory Allocator)، وأذونات للتحكم في الوصول إلى الشبكة والمستشعرات، إلى جانب العديد من [ميزات الأمان الأخرى](https://grapheneos.org/features). يأتي GrapheneOS أيضا مع تحديثات كاملة للبرامج الثابتة (Firmware) وإصدارات موقعة (Signed Builds)، لذلك فهو يدعم الإقلاع الموثق (Verified Boot) بشكل كامل.

[:octicons-home-16: Homepage](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title="Contribute" }

</div>

يدعم GrapheneOS تشغيل Google Play داخل [بيئة معزولة](https://grapheneos.org/usage#sandboxed-google-play) (Sandboxed Google Play)، حيث تعمل خدمات Google Play داخل Sandbox بالكامل مثل أي تطبيق عادي آخر. هذا يعني أنه يمكنك الاستفادة من معظم خدمات Google Play، مثل الإشعارات الفورية (Push Notifications)، مع الاحتفاظ بالتحكم الكامل في أذوناتها وما يمكنها الوصول إليه، بالإضافة إلى إمكانية حصرها داخل [ملف عمل](../os/android-overview.md#work-profile) (Work Profile) أو [ملف مستخدم](../os/android-overview.md#user-profiles) (User Profile) محدد من اختيارك.

تُعد هواتف Google Pixel الأجهزة الوحيدة التي تستوفي حاليا الـ [متطلبات أمان العتاد (Hardware Security Requirements)](https://grapheneos.org/faq#future-devices) الخاصة بـ GrapheneOS. يدعم Pixel 8 والإصدارات الأحدث ميزة Memory Tagging Extension (MTE) من ARM، وهي ميزة أمان على مستوى الـ Hardware تقلل بشكل كبير من احتمال استغلال الثغرات الناتجة عن أخطاء تلف الذاكرة (Memory Corruption Bugs). يوسّع GrapheneOS بشكل كبير نطاق استخدام MTE على الأجهزة التي تدعمها. بينما لا يسمح لك نظام التشغيل الافتراضي (Stock OS) إلا بتفعيل تطبيق محدود لميزة MTE من خلال أحد خيارات المطوّرين أو برنامج الحماية المتقدمة من Google (Advanced Protection Program)، يوفر GrapheneOS تطبيقا أقوى وأكثر شمولًا لميزة MTE بشكل افتراضي في نواة النظام (System Kernel)، ومكونات النظام الافتراضية، ومتصفح Vanadium الخاص به وميزة الـ WebView.

يوفر GrapheneOS أيضًا مفتاحًا عامًا (Global Toggle) لتفعيل MTE على جميع التطبيقات التي يثبتها المستخدم، وذلك من خلال: :gear: **الإعدادات** (Settings) ← **الأمان والخصوصية** (Security & privacy) ← **الحماية من الاستغلال** (Exploit protection) ← **وسم الذاكرة** (Memory tagging) ← **التفعيل افتراضيا** (Enable by default). يوفر نظام التشغيل أيضًا خيارات منفصلة لكل تطبيق لتعطيل MTE للتطبيقات التي قد تتعطل بسبب مشاكل التوافق (Compatibility Issues).

### فحوصات الاتصال (Connectivity Checks)

افتراضيا، يجري Android العديد من الاتصالات عبر الشبكة مع Google لإجراء الـ (DNS Connectivity Checks)، ومزامنة الوقت الحالي عبر الشبكة، والتحقق من اتصال جهازك بالشبكة، بالإضافة إلى العديد من المهام الأخرى التي تعمل في الخلفية. يستبدل GrapheneOS هذه الاتصالات باتصالات إلى خوادم تديرها GrapheneOS وتخضع لسياسة الخصوصية الخاصة بها. يؤدي ذلك إلى إخفاء معلومات مثل عنوان الـ (IP Address) الخاص بك عن Google، لكنه يعني أيضًا أنه سيكون من السهل جدًا على مسؤول الشبكة لديك أو مزود خدمة الإنترنت (ISP) ملاحظة أنك تتصل بعناوين مثل grapheneos.network وgrapheneos.org وغيرها، ومن ثم استنتاج نظام التشغيل الذي تستخدمه.

إذا كنت تريد إخفاء معلومات كهذه عن جهة معادية على شبكتك أو عن مزود خدمة الإنترنت (ISP)، فيجب عليك استخدام VPN موثوق، بالإضافة إلى تغيير إعداد فحص الاتصال (Connectivity Check) إلى Standard (Google). يمكن العثور على هذا الإعداد من خلال: :gear: **الإعدادات** (Settings) ← **الشبكة والإنترنت** (Network & internet) ← **فحوصات اتصال الإنترنت** (Internet connectivity checks). يتيح لك هذا الخيار الاتصال بخوادم Google لإجراء فحوصات الاتصال (Connectivity Checks)، ومع استخدام VPN يساعد ذلك على جعلك أقل تميزا ضمن مجموعة أكبر من أجهزة Android.

## المعايير

يرجى ملاحظة أننا غير مرتبطين بأي من المشاريع التي نوصي بها. بالإضافة إلى [معاييرنا العامة](../about/criteria.md)، وضعنا مجموعة واضحة من المتطلبات التي تساعدنا على تقديم توصيات موضوعية. ننصحك بالاطلاع على هذه القائمة وفهمها قبل اختيار أي مشروع، وإجراء بحثك الخاص للتأكد من أنه الخيار المناسب لك.

- يجب أن يكون البرنامج مفتوح المصدر (open-source software).
- يجب أن يدعم الـ (Bootloader Locking) مع دعم مفتاح AVB مخصّص (Custom AVB Key).
- يجب أن يتلقى تحديثات Android الرئيسية (Major Android Updates) خلال مدة تتراوح بين 0 و1 شهر من تاريخ إصدارها.
- يجب أن يحصل على تحديثات ميزات  (Android Feature Updates) خلال 14 يوما كحد أقصى من إصدارها.
- يجب أن يحصل على تحديثات الأمان (Security Patches) بشكل منتظم خلال 5 أيام كحد أقصى من إصدارها.
- يجب **ألا** يأتي بصلاحيات **الروت** (Rooted) بشكل افتراضي.
- يجب ألا تكون خدمات Google Play مفعلة بشكل افتراضي.
- يجب **ألا** يتطلب تعديل النظام حتى يدعم خدمات Google Play.
