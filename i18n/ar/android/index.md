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

Ideally, when choosing a custom Android distribution, you should make sure that it upholds the Android security model. At the very least, the distribution should have production builds, support for AVB, rollback protection, timely firmware and operating system updates, and SELinux in [enforcing mode](https://source.android.com/security/selinux/concepts#enforcement_levels). All of our recommended Android distributions satisfy these criteria:

[Recommended Distributions :material-arrow-right-drop-circle:](distributions.md){ .md-button }

### Avoid Root

[Rooting](https://en.wikipedia.org/wiki/Rooting_(Android)) Android phones can decrease security significantly as it weakens the complete [Android security model](https://en.wikipedia.org/wiki/Android_(operating_system)#Security_and_privacy). This can decrease privacy should there be an exploit that is assisted by the decreased security. Common rooting methods involve directly tampering with the boot partition, making it impossible to perform successful Verified Boot. Apps that require root will also modify the system partition, meaning that Verified Boot would have to remain disabled. Having root exposed directly in the user interface also increases the attack surface of your device and may assist in [privilege escalation](https://en.wikipedia.org/wiki/Privilege_escalation) vulnerabilities and SELinux policy bypasses.

Content blockers which modify the [hosts file](https://en.wikipedia.org/wiki/Hosts_(file)) (like AdAway) and firewalls which require root access persistently (like AFWall+) are dangerous and should not be used. They are also not the correct way to solve their intended purposes. For content blocking, we suggest encrypted [DNS](../dns.md) or content blocking functionality provided by a VPN instead. TrackerControl and AdAway in non-root mode will take up the VPN slot (by using a local loopback VPN), preventing you from using privacy-enhancing services such as [Orbot](../alternative-networks.md#orbot) or a [real VPN provider](../vpn.md).

AFWall+ works based on the [packet filtering](https://en.wikipedia.org/wiki/Firewall_(computing)#Packet_filter) approach and may be bypassable in some situations.

We do not believe that the security sacrifices made by rooting a phone are worth the questionable privacy benefits of those apps.

### Install Updates Regularly

It's important to not use an [end-of-life](https://endoflife.date/android) version of Android. Newer versions of Android receive not only security updates for the operating system but also important privacy enhancing updates too.

For example, [prior to Android 10](https://developer.android.com/about/versions/10/privacy/changes) any apps with the [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) permission could access sensitive and unique serial numbers of your phone such as [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), or your SIM card's [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity); whereas now they must be system apps to do so. System apps are only provided by the OEM or Android distribution.

### Use Built-in Sharing Features

You can avoid giving many apps permission to access your media with Android's built-in sharing features. Many applications allow you to "share" a file with them for media upload.

For example, if you want to post a picture to Discord you can open your file manager or gallery and share that picture with the Discord app, instead of granting Discord full access to your media and photos.
