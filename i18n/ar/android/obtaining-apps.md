---
title: "نزيل التطبيقات"
description: نوصي بهذه الطرق للحصول على التطبيقات على Android دون الحاجة إلى التعامل مع خدمات Google Play.
---

هناك طرق عديدة للحصول على تطبيقات Android بخصوصية، حتى من Play Store، دون الحاجة إلى التعامل مع خدمات Google Play. نوصي بالطرق التالية للحصول على التطبيقات على Android، مرتبة حسب الأفضلية.

## Obtainium

<div class="admonition recommendation" markdown>

![Obtainium logo](../assets/img/android/obtainium.svg){ align=right }

تطبيق Obtainium هو مدير تطبيقات (App Manager) يتيح لك تثبيت التطبيقات وتحديثها مباشرةً من صفحة الإصدارات الخاصة بالمطور نفسه. مثل GitHub أو GitLab أو موقع المطور نفسه، بدلا من الاعتماد على متجر تطبيقات أو مستودع مركزي (Centralized App Store/Repository). يدعم التحديثات التلقائية في الخلفية على Android 12 والإصدارات الأحدث.

[:octicons-repo-16: Repository](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ImranR98/Obtainium/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

يتيح لك Obtainium تنزيل ملفات تثبيت APK من مجموعة كبيرة من المصادر، وتقع عليك مسؤولية التأكد من أن هذه المصادر والتطبيقات موثوقة وشرعية. على سبيل المثال، يُفترض أن يكون استخدام Obtainium لتثبيت Signal من صفحة APK الرسمية الخاصة بـ [Signal](https://signal.org/android/apk) آمنًا، لكن تثبيت التطبيقات من مستودعات APK تابعة لجهات خارجية مثل Aptoide أو APKPure قد ينطوي على مخاطر إضافية. خطر تثبيت تحديث ضار أقل، لأن Android يتأكد قبل التثبيت أن التحديث صادر من نفس مطور التطبيق الموجود على هاتفك.

## متجر تطبيقات GrapheneOS

يتوفر متجر تطبيقات لـ GrapheneOS على GitHub. يدعم Android 12 والإصدارات الأحدث، ويمكنه تحديث نفسه تلقائيًا. يضم متجر التطبيقات، تطبيقات مستقلة طوّرها مشروع GrapheneOS، مثل [Auditor](../device-integrity.md#auditor-android) و[Camera](general-apps.md#secure-camera) و[PDF Viewer](general-apps.md#secure-pdf-viewer). إذا كنت تبحث عن هذه التطبيقات، فننصح بشدة بتنزيلها من متجر GrapheneOS بدلا من Play Store، لأن التطبيقات الموجودة في متجر GrapheneOS موقعة بتوقيع خاص بالمشروع نفسه، ولا تملك Google إمكانية الوصول إليه.

## متجر أورورا

يتطلب Google Play Store تسجيل الدخول باستخدام حساب Google، وهذا ليس جيدا للخصوصية. يمكنك تجنب ذلك باستخدام تطبيق بديل، مثل Aurora Store.

<div class="admonition recommendation" markdown>

![Aurora Store logo](../assets/img/android/aurora-store.webp){ align=right }

تطبيق **Aurora Store** هو تطبيق بديل لـ Google Play Store، ولا يحتاج إلى حساب Google أو Google Play Services أو microG لتنزيل التطبيقات.

[:octicons-home-16: Homepage](https://auroraoss.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

لا يتيح لك Aurora Store تنزيل التطبيقات المدفوعة عند استخدام ميزة الحساب المجهول. يمكنك أيضا تسجيل الدخول إلى Aurora Store باستخدام حساب Google لتنزيل التطبيقات التي اشتريتها، لكن هذا سيتيح لـ Google معرفة قائمة التطبيقات التي ثبتها. ومع ذلك، ستظل تستفيد من عدم الحاجة إلى تثبيت Google Play Store الكامل أو Google Play Services أو microG على جهازك.

## يدويًا باستخدام إشعارات RSS

بالنسبة للتطبيقات التي تُنشر على منصات مثل GitHub وGitLab، يمكنك إضافة RSS feed إلى [قارئ الأخبار](../news-aggregators.md) لمتابعة الإصدارات الجديدة.

![RSS APK](../assets/img/android/rss-apk-light.png#only-light) ![RSS APK](../assets/img/android/rss-apk-dark.png#only-dark) ![APK Changes](../assets/img/android/rss-changes-light.png#only-light) ![APK Changes](../assets/img/android/rss-changes-dark.png#only-dark)

### GitHub

على GitHub، وباستخدام [Secure Camera](general-apps.md#secure-camera) كمثال، انتقل إلى [صفحة الإصدارات (releases page)](https://github.com/GrapheneOS/Camera/releases)، ثم أضف .atom إلى نهاية الرابط:

`https://github.com/GrapheneOS/Camera/releases.atom`

### GitLab

على GitLab، وباستخدام [Aurora Store](#aurora-store) كمثال، انتقل إلى [مستودع المشروع (project repository)](https://gitlab.com/AuroraOSS/AuroraStore)، ثم أضف `/-/tags?format=atom` إلى نهاية الرابط:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

### التحقق من بصمات (Fingerprints) ملفات APK

إذا نزلت ملفات APK لتثبيتها يدويا، يمكنك التحقق من توقيعها باستخدام أداة [`apksigner`](https://developer.android.com/studio/command-line/apksigner)، وهي جزء من [Android build-tools](https://developer.android.com/studio/releases/build-tools).

1. قم بتثبيت [Java JDK](https://oracle.com/java/technologies/downloads).

2. نزّل [Android Studio command line tools](https://developer.android.com/studio#command-tools).

3. فك ضغط الأرشيف الذي نزلته:

   ```bash
   unzip commandlinetools-*.zip
   cd cmdline-tools
   ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
   ```

4. نفّذ الأمر التالي للتحقق من التوقيع (signature verification):

   ```bash
   ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
   ```

5. بعد ذلك، يمكنك مقارنة الـ hashes الناتجة بمصدر آخر. بعض المطورين مثل Signal يعرضون الـ [fingerprints](https://signal.org/android/apk) على موقعهم.

   ```bash
   Signer #1 certificate DN: CN=GrapheneOS
   Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
   Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
   Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
   ```

## F-Droid

![F-Droid logo](../assets/img/android/f-droid.svg){ align=right width=120px }

\==نوصي باستخدام F-Droid فقط للحصول على التطبيقات التي لا يمكن الحصول عليها بالطرق المذكورة أعلاه.== غالبًا ما يُنصح بـ F-Droid كبديل لـ Google Play، خصوصًا في مجتمع الخصوصية. إمكانية إضافة مستودعات من جهات خارجية، وعدم التقيد بنظام Google المغلق، ساهمت في انتشار F-Droid. يدعم F-Droid أيضا الـ [Reproducible Builds](https://f-droid.org/en/docs/Reproducible_Builds) لبعض التطبيقات، وهو مخصص للبرمجيات الحرة ومفتوحة المصدر. لكن توجد بعض العيوب الأمنية في طريقة F-Droid لبناء الحزم وتوقيعها وتوزيعها:

بسبب طريقة F-Droid في بناء التطبيقات، غالبا ما تتأخر تحديثات التطبيقات في مستودع F-Droid الرسمي. يعيد مشرفو F-Droid أيضا استخدام package IDs، ويوقعون التطبيقات بمفاتيحهم الخاصة، وهذا ليس مثاليا لأنه يمنح فريق F-Droid ثقة كاملة. بالإضافة إلى ذلك، فإن متطلبات إضافة التطبيقات إلى مستودع F-Droid الرسمي أقل صرامة من متاجر التطبيقات الأخرى مثل Google Play، ما يعني أن F-Droid يضم عددًا أكبر من التطبيقات القديمة أو التي لم تعد تحصل على تحديثات أو دعم، أو التي لم تعد تستوفي [معايير الأمان الحديثة](https://developer.android.com/google/play/requirements/target-sdk).

تخفف بعض مستودعات F-Droid الخارجية الشهيرة، مثل [IzzyOnDroid](https://apt.izzysoft.de/fdroid)، من بعض هذه المشاكل. يسحب مستودع IzzyOnDroid إصدارات التطبيقات مباشرةً من منصات استضافة الكود (code forges) (GitHub وGitLab وغيرها) ويُعد ثاني أفضل خيار بعد مستودعات المطورين أنفسهم. كما يوفر IzzyOnDroid جزء الـ [Reproducible Builds](https://android.izzysoft.de/articles/named/iod-rbs-mirrors-clients) لمئات التطبيقات، ولديه مطورون يتحققون من إمكانية إعادة إنتاج ملفات APK الموقّعة من مطوريها. بالإضافة إلى ذلك، يجري فريق IzzyOnDroid [فحوصات أمنية إضافية](https://android.izzysoft.de/articles/named/iod-scan-apkchecks) للتطبيقات الموجودة في المستودع، وغالبا ما تؤدي هذه الفحوصات إلى [نقاشات](https://github.com/gouravkhunger/QuotesApp/issues/22) مع مطوري التطبيقات لتحسين الخصوصية فيها. لاحظ أن التطبيقات قد تُحذف من مستودع IzzyOnDroid [في بعض الحالات](https://gitlab.com/IzzyOnDroid/repo#are-apps-removed-from-the-repo--and-when-does-that-happen).

تضم مستودعات [F-Droid](https://f-droid.org/en/packages) [وIzzyOnDroid](https://apt.izzysoft.de/fdroid) عددًا كبيرًا جدًا من التطبيقات، لذلك يمكن استخدامها للبحث عن التطبيقات مفتوحة المصدر واكتشافها، ثم تنزيلها بطرق أخرى مثل Play Store أو Aurora Store، أو بالحصول على ملف APK مباشرةً من المطور. استخدم تقديرك عند البحث عن تطبيقات جديدة بهذه الطريقة، وانتبه إلى مدى انتظام تحديث التطبيق. قد تعتمد التطبيقات القديمة على مكتبات لم تعد مدعومة، إلى جانب مشاكل أخرى، مما قد يشكل خطرا أمنيًا.

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

في بعض الحالات النادرة، يوزّع مطور التطبيق تطبيقه عبر F-Droid فقط، ويُعد Gadgetbridge مثالًا على ذلك. إذا كنت تحتاج فعلا إلى تطبيق كهذا، فننصح باستخدام [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) الأحدث بدلًا من تطبيق F-Droid الأصلي للحصول عليه. يدعم F-Droid Basic التحديثات التلقائية في الخلفية بدون الحاجة إلى privileged extension أو root، كما أنه يحتوي على ميزات أقل، وهذا يساعد على تقليل الـ attack surface.

</div>
