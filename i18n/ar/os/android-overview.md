---
title: نظرة عامة على Android
icon: simple/android
description: نظام Android هو نظام تشغيل مفتوح المصدر، ويوفر حماية أمنية قوية، مما يجعله خيارنا الأول للهواتف.
robots: nofollow, max-snippet:-1, max-image-preview:large
---

![Android logo](../assets/img/android/android.svg){ align=right }

يُعد **Android Open Source Project** نظام تشغيل آمنًا للهواتف، ويتميز بنظام قوي لعزل التطبيقات ([sandboxing](https://source.android.com/security/app-sandbox))، وميزة [Verified Boot (AVB)](https://source.android.com/security/verifiedboot)، ونظام محكم للتحكم في[ الأذونات (permissions)](https://developer.android.com/guide/topics/permissions/overview).

[:octicons-home-16:](https://source.android.com){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/main){ .card-link title="Source Code" }

[نصائحنا لنظام Android :material-arrow-right-drop-circle:](../android/index.md ""){.md-button.md-button--primary}

## وسائل الحماية الأمنية

تشمل أهم عناصر نظام الحماية في Android التحقق من[ سلامة الإقلاع (verified boot)](#verified-boot)، [وتحديثات البرامج الثابتة (Firmware)](#firmware-updates)، [ونظامًا قويًا للتحكم في الأذونات](#android-permissions). تُشكّل ميزات الأمان المهمة هذه الأساس الذي نعتمد عليه في تحديد الحد الأدنى من المعايير لاختيار [الهواتف](../mobile-phones.md) و[أنظمة Android المعدّلة](../android/distributions.md) التي نوصي بها.

### التحقق من سلامة الإقلاع (Verified Boot)

يُعد الـ[**Verified Boot**](https://source.android.com/security/verifiedboot) جزءا مهما من نظام الأمان في Android. From the documentation:
> Verified Boot strives to ensure all executed code comes from a trusted source (usually device OEMs), rather than from an attacker or corruption. It establishes a full chain of trust, starting from a hardware-protected root of trust to the bootloader, to the boot partition and other verified partitions including system, vendor, and optionally oem partitions. During device boot up, each stage verifies the integrity and authenticity of the next stage before handing over execution.

It provides protection against malware persistence and ensures security updates cannot be downgraded with [rollback protection](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection).

بدءًا من Android 10، انتقل النظام من تشفير القرص بالكامل إلى [تشفير الملفات](https://source.android.com/security/encryption/file-based)، الذي يوفر مرونة أكبر.

يضمن الـVerified Boot سلامة ملفات نظام التشغيل وعدم التلاعب بها، مما يمنع أي مهاجم لديه وصول فعلي إلى الجهاز من تعديل هذه الملفات أو تثبيت برمجيات خبيثة عليه. في حال تمكنت برمجية خبيثة، رغم ندرة حدوث ذلك، من استغلال أجزاء أخرى من النظام والحصول على صلاحيات أعلى، فإن الـ Verified Boot سيمنع استمرار أي تغييرات أُجريت على النظام، ويعيده إلى حالته الأصلية عند إعادة تشغيل الجهاز.

للأسف، لا يُلزم مصنعو الأجهزة (OEMs) بدعم الـVerified Boot إلا في نسخة Android الأصلية التي يوفرونها مع أجهزتهم. لا يدعم تسجيل مفاتيح AVB مخصصة على أجهزته سوى عدد قليل من الشركات المصنعة، مثل Google. بالإضافة إلى ذلك، لا تدعم بعض الأنظمة المشتقة من AOSP، مثل LineageOS و/e/ OS، ميزة الـVerified Boot، حتى على الأجهزة التي تدعم هذه الميزة مع أنظمة تشغيل خارجية. ننصحك بالتأكد من دعم هذه الميزة **قبل** شراء جهاز جديد. لا ننصح باستخدام الأنظمة المشتقة من AOSP التي **لا** تدعم Verified Boot.

كذلك، تطبّق العديد من الشركات المصنعة ميزة الـVerified Boot بشكل غير صحيح، لذا عليك الانتباه إلى هذه المشكلات وعدم الاعتماد على ما تروج له الشركات. على سبيل المثال، لا يتمتع جهازا Fairphone 3 وFairphone 4 بالأمان الكافي بإعداداتهما الافتراضية، لأن [ الـ (bootloader) الأصلي يثق بمفتاح AVB العام المستخدم للتوقيع.](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11) هذا يضعف حماية الـVerified Boot على أجهزة Fairphone التي تعمل بنظامها الأصلي، إذ يمكن للجهاز تشغيل أنظمة Android بديلة (مثل /e/) دون عرض[ أي تحذير](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) بشأن استخدام نظام تشغيل مخصّص.

### تحديثات الـ Firmware

**تحديثات الـ (Firmware) **ضرورية للحفاظ على أمان جهازك، وبدونها لا يمكن أن يكون جهازك آمنا. لدى الشركات المصنعة للأجهزة (OEMs) اتفاقيات مع شركائها لتوفير المكونات مغلقة المصدر لفترة دعم محدودة. تُوضح تفاصيل هذه المكونات في [نشرات أمان Android الشهرية.](https://source.android.com/security/bulletin)

نظرا لأن بعض مكونات الهاتف، مثل المعالج وتقنيات الاتصال اللاسلكي، تعتمد على مكونات مغلقة المصدر، فلا بد أن توفر الشركات المصنعة لهذه المكوّنات التحديثات اللازمة. لذلك، من المهم أن تشتري جهازا لا يزال يحصل على تحديثات ودعم من الشركة المصنعة. توفّر شركتا [Qualcomm](https://qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) و[Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox) الدعم لأجهزتهما لمدة 4 سنوات، بينما غالبا ما تكون فترة الدعم للمنتجات الأقل سعرا أقصر. مع إطلاق [Pixel 6](https://support.google.com/pixelphone/answer/4457705)، بدأت Google بتصنيع نظامها الخاص على شريحة (SoC)، وستوفر الدعم لأجهزتها لمدة لا تقل عن 5 سنوات. مع إطلاق سلسلة Pixel 8، رفعت Google فترة الدعم إلى 7 سنوات.

الأجهزة التي انتهت فترة دعمها (EOL) من الشركة المصنعة للمعالج (SoC) لا يمكنها تلقي تحديثات الـ (Firmware)، سواء من الشركات المصنعة للأجهزة (OEMs) أو من مطوّري إصدارات Android البديلة. هذا يعني أن الثغرات الأمنية في هذه الأجهزة ستظل دون إصلاح.

على سبيل المثال، تروج شركة Fairphone لجهاز Fairphone 4 على أنه سيحصل على الدعم لمدة 6 سنوات. لكن المعالج (SoC) المستخدم في Fairphone 4، وهو Qualcomm Snapdragon 750G، تنتهي فترة دعمه قبل ذلك بوقت طويل. هذا يعني أن تحديثات الـ (Firmware) التي توفرها Qualcomm لجهاز Fairphone 4 ستتوقف في سبتمبر 2023، حتى لو استمرت Fairphone في إصدار تحديثات أمنية للنظام.

### أذونات الـ Android

تتيح لك [**الأذونات في Android **](https://developer.android.com/guide/topics/permissions/overview)التحكم فيما يُسمح للتطبيقات بالوصول إليه. تُجري Google [تحسينات](https://developer.android.com/about/versions/11/privacy/permissions) مستمرة على نظام الأذونات مع كل إصدار جديد. تعمل جميع التطبيقات التي تثبتها داخل بيئات معزولة [(sandboxing)](https://source.android.com/security/app-sandbox) تفرض قيودا صارمة عليها، لذلك لا حاجة لتثبيت أي تطبيق لمكافحة الفيروسات.

الهاتف الذي يعمل بأحدث إصدار من Android سيكون دائما أكثر أمانا من هاتف قديم ثبت عليه تطبيقا مدفوعا لمكافحة الفيروسات. من الأفضل ألا تنفق أموالك على برامج مكافحة الفيروسات، وأن تدّخرها لشراء هاتف جديد مثل [Google Pixel](../mobile-phones.md#google-pixel).

أندرويد 10:

- تمنحك ميزة [Scoped Storage](https://developer.android.com/about/versions/10/privacy/changes#scoped-storage) تحكما أكبر في ملفاتك، وتتيح لك تقييد وصول التطبيقات إلى [وحدة التخزين الخارجية](https://developer.android.com/training/data-storage#permissions). يمكن أن يكون لكل تطبيق مجلد خاص به في وحدة التخزين الخارجية، كما يمكنه تخزين أنواع معينة من ملفات الوسائط فيها.
- فرض قيود أكثر صرامة على الوصول إلى [موقع الجهاز](https://developer.android.com/about/versions/10/privacy/changes#app-access-device-location)، من خلال إضافة إذن `ACCESS_BACKGROUND_LOCATION`. هذا يمنع التطبيقات من معرفة موقعك أثناء عملها في الخلفية، إلا إذا سمحت لها بذلك بشكل واضح.

أندرويد 11:

- أذونات تُستخدم [لمرة واحدة](https://developer.android.com/about/versions/11/privacy/permissions#one-time)، تتيح لك منح التطبيق إذنا لمرة واحدة فقط.
- [إعادة ضبط الأذونات تلقائيا](https://developer.android.com/about/versions/11/privacy/permissions#auto-reset)، حيث تُلغى الأذونات التي مُنحت للتطبيق [أثناء استخدامه](https://developer.android.com/guide/topics/permissions/overview#runtime).
- أذونات منفصلة للتحكم في الوصول إلى الميزات المتعلقة[برقم الهاتف.](https://developer.android.com/about/versions/11/privacy/permissions#phone-numbers)

أندرويد 12:

- إذن يتيح لك مشاركة موقعك [التقريبي فقط](https://developer.android.com/about/versions/12/behavior-changes-12#approximate-location).
- إعادة ضبط أذونات [التطبيقات غير المستخدمة](https://developer.android.com/about/versions/12/behavior-changes-12#app-hibernation) تلقائيًا.
- [تتبّع وصول](https://developer.android.com/about/versions/12/behavior-changes-12#data-access-auditing) التطبيقات إلى البيانات، مما يسهّل معرفة أي جزء من التطبيق يصل إلى نوع معيّن من البيانات.

أندرويد 13:

- إذن للوصول إلى [أجهزة Wi-Fi القريبة](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). كانت التطبيقات تستخدم عناوين MAC الخاصة بنقاط اتصال Wi-Fi القريبة بشكل شائع لتتبع موقع المستخدم.
- [أذونات أكثر دقة](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions) للوصول إلى الوسائط، بحيث يمكنك السماح بالوصول إلى الصور أو الفيديوهات أو الملفات الصوتية فقط.
- أصبح استخدام المستشعرات في الخلفية يتطلب إذن الـ [BODY_SENSORS``](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission).

قد يطلب التطبيق إذنا لاستخدام ميزة معينة فيه. على سبيل المثال، أي تطبيق يمكنه مسح رموز QR سيحتاج إلى إذن الوصول إلى الكاميرا. قد تطلب بعض التطبيقات أذونات أكثر مما تحتاج إليه.

يمكن أن يكون [Exodus](https://exodus-privacy.eu.org) مفيدا عند مقارنة التطبيقات التي تؤدي وظائف متشابهة. إذا كان التطبيق يطلب الكثير من الأذونات ويحتوي على الكثير من الإعلانات وأدوات التحليل، فغالبا ما تكون هذه علامة سيئة. ننصحك **بمراجعة** أدوات التتبّع الموجودة في التطبيق وقراءة وظيفة كل أداة، بدلا من الحكم عليها بناء على عددها فقط، لأن أدوات التتبّع تختلف في طريقة عملها ومدى تأثيرها على خصوصيتك.

<div class="admonition warning" markdown>
<p class="admonition-title">تنوية</p>

إذا كان التطبيق يعتمد بشكل أساسي على خدمة عبر الويب، فقد يحدث التتبع على الخادم نفسه. يظهر أن [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest) لا يحتوي على «أي أدوات تتبع»، لكنه بالتأكيد يتتبع اهتمامات المستخدمين وسلوكهم على الموقع. قد تتمكن بعض التطبيقات من تجنب اكتشاف أدوات التتبع فيها إذا لم تستخدم مكتبات البرمجة المعتادة التي توفرها شركات الإعلانات، لكن هذا غير شائع.

</div>

<div class="admonition note" markdown>
<p class="admonition-title">ملحوظة</p>

قد تظهر بعض أدوات التتبّع مثل [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49) في التطبيقات التي تحترم خصوصيتك، مثل [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest). تتضمن هذه المكتبة [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging)، التي يمكن استخدامها لإرسال [إشعارات فورية](https://en.wikipedia.org/wiki/Push_technology) داخل التطبيقات. وهذا [هو الحال](https://fosstodon.org/@bitwarden/109636825700482007) مع Bitwarden. هذا لا يعني أن Bitwarden يستخدم جميع ميزات تحليل البيانات التي توفرها Google Firebase Analytics.

</div>

## ميزات الخصوصية

### ملفات تعريف المستخدمين

يمكنك العثور على ميزة** ملفات تعريف المستخدمين** المتعددة في **Settings** → **System** → **Users**، وهي أبسط طريقة لعزل التطبيقات والبيانات على Android.

تتيح لك ملفات تعريف المستخدمين فرض قيود على ملف تعريف معين، مثل منع إجراء المكالمات أو استخدام الرسائل النصية SMS أو تثبيت التطبيقات. يُشفر كل ملف تعريف بمفتاح تشفير خاص به، ولا يمكنه الوصول إلى بيانات أي ملف تعريف آخر. حتى صاحب الهاتف لا يمكنه الاطلاع على بيانات ملفات التعريف الأخرى دون معرفة كلمات المرور الخاصة بها. استخدام ملفات تعريف متعددة للمستخدمين هو طريقة أكثر أمانا لعزل بيانات كل مستخدم عن الآخرين.

### الملف الشخصي للعمل

تُعد ملفات تعريف العمل[ (Work Profiles)****](https://support.google.com/work/android/answer/6191949) طريقة أخرى لعزل التطبيقات عن بعضها، وقد تكون أسهل في الاستخدام من إنشاء ملفات تعريف منفصلة للمستخدمين.

لإنشاء ملف تعريف عمل (Work Profile) دون استخدام نظام إدارة أجهزة تابع لشركة (MDM)، ستحتاج إلى تطبيق **لإدارة الجهاز** مثل [Shelter](../android/general-apps.md#shelter)، إلا إذا كنت تستخدم نسخة معدّلة من Android تتضمن هذه الميزة بالفعل.

يعتمد ملف تعريف العمل (Work Profile) على تطبيق لإدارة الجهاز حتى يعمل. يجب أن يدعم تطبيق إدارة الجهاز ميزات مثل* نقل الملفات (File Shuttle)*، و*منع البحث في جهات الاتصال*، وأي ميزات أخرى لعزل التطبيقات والبيانات عن بعضها. يجب أيضا أن تثق تماما في تطبيق إدارة الجهاز، لأنه يستطيع الوصول إلى جميع بياناتك داخل ملف تعريف العمل (Work Profile).

هذه الطريقة عموما أقل أمانًا من استخدام ملف تعريف منفصل للمستخدم، لكنها تتيح لك تشغيل التطبيقات في ملفك الشخصي الأساسي وملف تعريف العمل (Work Profile) في الوقت نفسه.

### المساحة الخاصة

**المساحة الخاصة (Private Space)** هي ميزة أُضيفت في Android 15، وتوفّر طريقة أخرى لعزل التطبيقات عن بعضها. يمكنك إعداد مساحة خاصة (Private Space) في ملف تعريف المستخدم الأساسي من خلال الانتقال إلى **Settings** → **Security & privacy** → **Private space**. بعد إعداد المساحة الخاصة، ستجدها في أسفل قائمة التطبيقات.

مثل ملفات تعريف المستخدمين، تُشفر المساحة الخاصة (Private Space) بمفتاح تشفير خاص بها، ويمكنك اختيار طريقة مختلفة لفتح قفلها. مثل ملفات تعريف العمل (Work Profiles)، يمكنك تشغيل التطبيقات الموجودة في ملفك الشخصي الأساسي والمساحة الخاصة (Private Space) في الوقت نفسه. يمكنك تمييز التطبيقات التي تُشغلها من المساحة الخاصة (Private Space) من خلال أيقونة على شكل مفتاح داخل درع.

على عكس ملفات تعريف العمل (Work Profiles)، فإن المساحة الخاصة (Private Space) ميزة مدمجة في Android، ولا تحتاج إلى تطبيق خارجي لإدارتها. لهذا السبب، ننصح عموما باستخدام المساحة الخاصة (Private Space) بدلا من ملف تعريف العمل (Work Profile)، لكن يمكنك استخدامهما معا في الوقت نفسه.

### VPN kill switch

يدعم Android 7 والإصدارات الأحدث ميزة Kill Switch للـ VPN، ويمكنك استخدامها دون الحاجة إلى تثبيت تطبيقات خارجية. تساعد هذه الميزة على منع تسرب بياناتك إذا انقطع اتصال الـ VPN. يمكنك العثور على هذه الميزة من خلال الانتقال إلى :gear:**Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

### إعدادات التحكم العامة

توفر أجهزة Android الحديثة خيارات لإيقاف Bluetooth وخدمات الموقع على مستوى الجهاز بالكامل. أضاف Android 12 خيارات لتعطيل الكاميرا والميكروفون. ننصحك بإيقاف هذه الميزات عندما لا تحتاج إلى استخدامها. لا يمكن للتطبيقات استخدام هذه الميزات بعد إيقافها، حتى لو سبق أن منحتها الأذونات اللازمة، إلا بعد إعادة تفعيلها.

## خدمات جوجل

إذا كنت تستخدم جهازا يحتوي على خدمات Google، سواء بنظام التشغيل الأصلي أو بنظام يعزل Google Play Services بطريقة آمنة مثل GrapheneOS، فهناك بعض الإعدادات الإضافية التي يمكنك تغييرها لتحسين خصوصيتك. ما زلنا ننصح بتجنّب خدمات Google تمامًا، أو حصر استخدامها في ملف تعريف مستخدم أو ملف تعريف عمل (Work Profile) محدّد، من خلال الجمع بين تطبيق لإدارة الجهاز مثل *Shelter* وميزة Sandboxed Google Play في GrapheneOS.

### برنامج الحماية المتقدمة

إذا كان لديك حساب Google، فننصحك بالاشتراك في برنامج الحماية المتقدّمة [ (Advanced Protection Program)](https://landing.google.com/advancedprotection). البرنامج مجاني ومتاح لأي شخص لديه مفتاحا أمان فعليان أو أكثر يدعمان [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online). يمكنك أيضًا استخدام [مفاتيح المرور (Passkeys)](https://fidoalliance.org/passkeys) بدلًا من ذلك.

يوفر برنامج الحماية المتقدمة مراقبة أفضل للتهديدات الأمنية، ويتيح الميزات التالية:

- مصادقة ثنائية أكثر صرامة، حيث **يُشترط** استخدام [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online)، ولا يُسمح باستخدام [رموز التحقق عبر SMS](../basics/multi-factor-authentication.md#sms-or-email-mfa) أو [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) أو [OAuth](../basics/account-creation.md#sign-in-with-oauth)
- لا يمكن الوصول إلى بيانات الحساب إلا من خلال Google والتطبيقات الخارجية التي تم التحقق منها
- فحص الرسائل الواردة إلى حسابات Gmail للكشف عن محاولات [التصيد الاحتيالي (Phising)](https://en.wikipedia.org/wiki/Phishing#Email_phishing)
- [فحص أكثر صرامة](https://google.com/chrome/privacy/whitepaper.html#malware) للمواقع الخطيرة أثناء التصفح باستخدام Google Chrome
- إجراءات أكثر صرامة لاستعادة الحسابات عند فقدان بيانات تسجيل الدخول

 إذا كنت تستخدم Google Play Services دون عزلها عن بقية النظام (كما هو شائع في أنظمة التشغيل الأصلية)، فإن برنامج الحماية المتقدمة يوفّر لك أيضا [مزايا إضافية](https://support.google.com/accounts/answer/9764949)، مثل:

- منع تثبيت التطبيقات من خارج Google Play Store أو متجر التطبيقات التابع للشركة المصنعة للجهاز، إلا عند تثبيتها باستخدام [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- فحص الجهاز تلقائيًا وبشكل إلزامي باستخدام [Play Protect](https://support.google.com/googleplay/answer/2812853?#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- تحذيرك من التطبيقات التي لم يتم التحقق منها
- تفعيل ميزة [Memory Tagging Extension (MTE)](https://developer.arm.com/documentation/108035/0100/Introduction-to-the-Memory-Tagging-Extension) من ARM، التي تعتمد على مكونات الجهاز وتعمل مع التطبيقات التي تدعمها، مما يقلّل من احتمال استغلال الثغرات الناتجة عن أخطاء في الذاكرة لاختراق الجهاز.

### تحديثات نظام Google Play

في السابق، كانت تحديثات الأمان لنظام Android تصل إلى المستخدمين عن طريق الشركة المطوّرة لنظام التشغيل. بدءا من Android 10، أصبح النظام مقسّما إلى مكوّنات مستقلة بشكل أكبر، مما يتيح لـ Google إرسال تحديثات أمنية **لبعض** هذه المكوّنات مباشرة عبر Play Services، التي تمتلك صلاحيات خاصة داخل النظام.

إذا كان جهازك قد انتهى دعمه (EOL)، وكان يعمل بنظام Android 10 أو أحدث، ولا يمكنك تثبيت أي من أنظمة التشغيل التي نوصي بها، فمن الأفضل غالبا الاستمرار في استخدام نظام Android الأصلي من الشركة المصنعة لجهازك، بدلًا من تثبيت نظام آخر لا نوصي به هنا، مثل LineageOS أو /e/ OS. بهذه الطريقة، ستظل تتلقى **بعض** الإصلاحات الأمنية من Google، دون الإخلال بنظام الحماية في Android باستخدام نسخة معدلة وغير آمنة منه، أو زيادة فرص تعرض جهازك للهجمات. ومع ذلك، ما زلنا ننصحك بالانتقال إلى جهاز لا يزال يتلقى التحديثات الأمنية في أقرب وقت ممكن.

### معرف الإعلانات

تُنشئ جميع الأجهزة التي تحتوي على Google Play Services [معرفا إعلانيا](https://support.google.com/googleplay/android-developer/answer/6048248) تلقائيا، يُستخدم لعرض إعلانات تستهدف المستخدم حسب اهتماماته. عطل هذه الميزة لتقليل كمية البيانات التي تُجمع عنك.

في إصدارات Android التي تستخدم Google Play المعزول [(Sandboxed Google Play)](https://grapheneos.org/usage#sandboxed-google-play)، انتقل إلى :gear: **Settings** → **Apps** →** Sandboxed Google Play** → **Google Settings** → **All services** → **Ads**.

- [x] اختر **Delete advertising ID**

في إصدارات Android التي تعمل فيها Google Play Services بصلاحيات خاصة داخل النظام (مثل النظام الأصلي في معظم الأجهزة)، قد تجد هذا الإعداد في أكثر من مكان. تحقق

- :gear: **Settings** → **Google** → **Ads**
- :gear: **Settings** → **Privacy** → **Ads**

ستجد خيارا لحذف معرفك الإعلاني أو إيقاف الإعلانات التي* تستهدفك حسب اهتماماتك*، ويختلف الخيار المتاح حسب إصدار Android والشركة المصنعة للجهاز. إذا كان خيار حذف المعرف الإعلاني متاحا، فننصحك باختياره. إذا لم يكن متاحا، فتأكد من إيقاف الإعلانات التي تستهدفك حسب اهتماماتك، ثم إعادة تعيين معرفك الإعلاني.

### SafetyNet وPlay Integrity API

تُستخدم [SafetyNet](https://developer.android.com/training/safetynet/attestation) وواجهات [Play Integrity API](https://developer.android.com/google/play/integrity) عادةً في [التطبيقات البنكية](https://grapheneos.org/usage#banking-apps). تعمل الكثير من التطبيقات البنكية بشكل طبيعي على GrapheneOS مع خدمات Google Play المعزولة، لكن بعض التطبيقات غير المالية تستخدم وسائل بدائية خاصة بها للكشف عن التلاعب بالتطبيق أو النظام، وقد لا تعمل هذه الوسائل بشكل صحيح. يجتاز GrapheneOS فحص السلامة الأساسي` (basicIntegrity)`، لكنه لا يجتاز فحص اعتماد الجهاز `(ctsProfileMatch).` تدعم الأجهزة التي تعمل بنظام Android 8 أو أحدث ميزة التحقق من سلامة الجهاز باستخدام مكوّناته الفعلية (Hardware Attestation)، ولا يمكن تجاوز هذا التحقق إلا إذا تسربت مفاتيح الأمان أو وُجدت ثغرات أمنية خطيرة.

أما بالنسبة إلى Google Wallet، فلا ننصح باستخدامه بسبب[ سياسة الخصوصية](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en) الخاصة به، التي تنص على أنه يجب عليك إلغاء الاشتراك في مشاركة البيانات إذا كنت لا تريد مشاركة تصنيفك الائتماني ومعلوماتك الشخصية مع خدمات التسويق التابعة لشركات مرتبطة بـ Google.
