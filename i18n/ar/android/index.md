---
title: "Android"
description: نصائحنا لاستبدال ميزات Android الافتراضية التي تنتهك الخصوصية ببدائل أكثر خصوصية وأمانا.
icon: 'simple/android'
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Android Recommendations
    url: ""
  - "@context": ""
    "@type": ""
    name: Android
    image: ""
    url: ""
    sameAs: ""
---



يُعد Android Open Source Project (AOSP) نظام تشغيل مفتوح المصدر للأجهزة المحمولة تقوده Google، وهو الأساس الذي تعمل عليه أغلب أجهزة الهواتف المحمولة حول العالم. معظم الهواتف التي تُباع بنظام Android تأتي بنسخة معدلة منه تتضمن خدمات وتطبيقات قد تنتهك الخصوصية، مثل Google Play Services. لذلك يمكنك تحسين خصوصيتك بشكل كبير عبر استبدال نسخة Android الافتراضية على هاتفك بإصدار لا يحتوي على هذه الميزات المتطفلة.

[نظرة عامة على Android :material-arrow-right-drop-circle:](../os/android-overview.md){ .md-button .md-button--primary }

## نصائحنا

### استبدال خدمات Google

توجد طرق عديدة للحصول على التطبيقات على Android دون استخدام Google Play. كلما أمكن، حاول استخدام إحدى هذه الطرق أولًا قبل الحصول على تطبيقاتك من مصادر لا تحترم الخصوصية:

[الحصول على التطبيقات :material-arrow-right-drop-circle:](obtaining-apps.md){ .md-button }

توجد أيضا بدائل عديدة تحترم الخصوصية للتطبيقات التي تأتي مثبتة مسبقا على هاتفك، مثل تطبيق الكاميرا. إلى جانب تطبيقات Android التي نوصي بها بشكل عام في هذا الموقع، أعددنا أيضا قائمة بأدوات النظام system utilities الخاصة بـ Android والتي قد تجدها مفيدة.

[توصيات عامة للتطبيقات :material-arrow-right-drop-circle:](general-apps.md){ .md-button }

### تثبيت توزيعة Android مخصصة

عند شراء هاتف Android، يأتي نظام التشغيل الافتراضي مرفقا بتطبيقات وميزات لا تعد جزءا من Android Open Source Project (AOSP). تتطلب العديد من هذه التطبيقات — حتى تطبيقات مثل dialer التي توفر وظائف أساسية في النظام — تكاملات متطفلة مع Google Play Services. وهذه الخدمات بدورها تطلب privileges للوصول إلى ملفاتك، وجهات الاتصال، وسجل المكالمات، ورسائل SMS، والموقع، والكاميرا، والميكروفون، والعديد من الأشياء الأخرى على جهازك، وذلك حتى تتمكن تطبيقات النظام الأساسية هذه والعديد من التطبيقات الأخرى من العمل من الأساس. تزيد أُطر العمل مثل Google Play Services من الـ attack surface على جهازك، كما أنها تُعد مصدرا للعديد من المخاوف المتعلقة بالخصوصية في Android.

يمكن حل هذه المشكلة باستخدام توزيعة بديلة من Android، تُعرف عادةً باسم custom ROM، ولا تأتي مدمجة بهذه التكاملات المتطفلة. للأسف، كثير من توزيعات Android المخصّصة custom Android distributions لا تلتزم بنموذج الأمان الخاص بـ Android، لأنها لا تدعم بعض ميزات الأمان المهمة مثل AVB وrollback protection وتحديثات firmware وغيرها. تأتي بعض التوزيعات أيضًا بإصدارات [userdebug](https://source.android.com/setup/build/building#choose-a-target)، والتي تتيح الوصول إلى root عبر [ADB](https://developer.android.com/studio/command-line/adb)، كما تتطلب سياسات SELinux [أكثر تساهلًا](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) لدعم ميزات debugging. ونتيجة لذلك، تزداد الـ attack surface بشكل أكبر ويصبح نموذج الأمان أضعف.

من الأفضل عند اختيار توزيعة Android مخصصة custom Android distribution أن تتأكد من أنها تحافظ على نموذج الأمان الخاص بـ Android. على أقل تقدير، يجب أن توفر التوزيعة إصدارات production builds، وأن تدعم AVB وrollback protection، وأن تحصل على تحديثات firmware ونظام التشغيل في الوقت المناسب، مع تشغيل SELinux في وضع [enforcing](https://source.android.com/security/selinux/concepts#enforcement_levels). جميع توزيعات Android التي نوصي بها تستوفي هذه المعايير:

التوزيعات الموصى بها :material-arrow-right-drop-circle:{ .md-button }

### تجنب الـ Root

يمكن أن يؤدي عمل الـ [Root](https://en.wikipedia.org/wiki/Rooting_(Android) لهواتف Android إلى تقليل مستوى الأمان بشكل كبير، لأنه يضعف [نموذج الأمان الخاص بـ Android](https://en.wikipedia.org/wiki/Android_(operating_system) ككل. وقد يؤدي ذلك أيضا إلى تقليل مستوى الخصوصية إذا وُجدت ثغرة (exploit) يمكنه الاستفادة من هذا الضعف في الأمان. تتضمن طرق الـ Root الشائعة التعديل مباشرةً على الـ boot partition، مما يجعل من المستحيل إجراء Verified Boot بشكل ناجح. كما أن التطبيقات التي تتطلب صلاحيات Root ستقوم أيضا بتعديل system partition، وهذا يعني أن Verified Boot سيحتاج إلى البقاء معطلًا. كما أن إتاحة صلاحيات الـ Root مباشرة من خلال واجهة المستخدم تزيد من الـ attack surface على جهازك، وقد تساعد في استغلال ثغرات privilege escalation وتجاوز سياسات SELinux.

أدوات حجب المحتوى التي تعدّل [ملف hosts](https://en.wikipedia.org/wiki/Hosts_(file) مثل AdAway، وكذلك تطبيقات firewall التي تحتاج إلى صلاحيات الـ Root بشكل دائم مثل AFWall+، تُعد خطرة ولا يُنصح باستخدامها. كما أنها ليست الطريقة الصحيحة لتحقيق الأهداف التي صُممت من أجلها. لحجب المحتوى، نوصي باستخدام [DNS](../dns.md) مشفر، أو استخدام ميزة حجب المحتوى التي توفرها بعض خدمات VPN بدلًا من ذلك. يستخدم كل من TrackerControl وAdAway في وضع non-root خانة الـ VPN على الجهاز، وذلك عبر إنشاء local loopback VPN. وهذا يمنعك من استخدام خدمات أخرى تعزز الخصوصية مثل [Orbot](../alternative-networks.md#orbot) أو [مزود VPN](../vpn.md) حقيقي.

يعمل AFWall+ بالاعتماد على أسلوب [packet filtering](https://en.wikipedia.org/wiki/Firewall_(computing)، وقد يكون من الممكن تجاوزه في بعض الحالات.

نرى أن المخاطر الأمنية الناتجة عن عمل الـ Root للهاتف أكبر من فوائد الخصوصية التي قد توفرها هذه التطبيقات، خصوصا أن هذه الفوائد ليست مضمونة دائما.

### ثبّت التحديثات بانتظام

من المهم ألا تستخدم إصدارا من Android وصل إلى مرحلة end-of-life، أي أنه لم يعد يحصل على تحديثات أمنية أو دعم رسمي. الإصدارات الأحدث من Android لا تحصل فقط على تحديثات أمنية لنظام التشغيل، بل تتلقى أيضا تحديثات مهمة تعمل على تحسين الخصوصية.

على سبيل المثال، قبل Android 10https://developer.android.com/about/versions/10/privacy/changes، كان بإمكان أي تطبيق لديه صلاحية [READ_PHONE_STATE](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) الوصول إلى أرقام تعريف حساسة وفريدة خاصة بهاتفك، مثل [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity) و[MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier) و[IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity) الخاص بشريحة SIM. أما الآن، فلا يمكن للتطبيق الوصول إلى هذه المعلومات إلا إذا كان system app. تطبيقات System apps لا يتم توفيرها إلا من قِبل الشركة المصنعة للجهاز OEM أو من خلال توزيعة Android نفسها.

### استخدم ميزات المشاركة المدمجة

يمكنك تجنب منح العديد من التطبيقات صلاحية الوصول إلى الصور والوسائط على جهازك، وذلك باستخدام ميزات المشاركة المدمجة في Android. تسمح لك العديد من التطبيقات باستخدام خيار "Share" لإرسال ملف إليها من أجل رفعه كوسائط.

على سبيل المثال، إذا أردت نشر صورة على Discord، يمكنك فتح file manager أو معرض الصور، ثم استخدام خيار Share لمشاركة الصورة مع تطبيق Discord مباشرة، بدلًا من منح Discord صلاحية الوصول الكامل إلى جميع الصور والوسائط على جهازك.
