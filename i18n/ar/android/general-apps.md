---
title: "التطبيقات العامة"
description: التطبيقات المذكورة هنا متاحة حصريا على Android، وهي مصممة خصيصا لتحسين وظائف أساسية في النظام أو استبدالها.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: General Android Apps
    url: "./"
  - "@context": http://schema.org
    "@type": MobileApplication
    name: Shelter
    applicationCategory: Utilities
    operatingSystem: Android
  - "@context": http://schema.org
    "@type": MobileApplication
    name: Secure Camera
    applicationCategory: Utilities
    operatingSystem: Android
  - "@context": http://schema.org
    "@type": MobileApplication
    name: Secure PDF Viewer
    applicationCategory: Utilities
    operatingSystem: Android
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: الهجمات السلبية **Passive Attacks**](../basics/common-threats.md#security-and-privacy){ .pg-orange }

نوصي بمجموعة واسعة من تطبيقات Android في مختلف أقسام هذا الموقع. التطبيقات المذكورة هنا متاحة حصريا على Android، وهي مصممة خصيصا لتحسين وظائف أساسية في النظام أو استبدالها.

## Shelter

إذا كان جهازك يعمل بنظام Android 15 أو أحدث، فنوصي بدلًا من ذلك باستخدام ميزة [Private Space](../os/android-overview.md#private-space) المدمجة في النظام. فهي توفر تقريبًا نفس الوظائف، من دون الحاجة إلى الوثوق بتطبيق من جهة خارجية أو منحه صلاحيات واسعة.

<div class="admonition recommendation" markdown>

![Shelter logo](../assets/img/android/shelter.svg){ align=right }

تطبيق Shelter هو تطبيق يساعدك على الاستفادة من ميزة Work Profile في Android لعزل التطبيقات على جهازك أو إنشاء نسخ منفصلة منها.

يدعم Shelter منع البحث عن جهات الاتصال بين الـ profiles المختلفة، كما يتيح مشاركة الملفات بين هذه الـ profiles باستخدام مدير الملفات الافتراضي [DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui).

[:octicons-repo-16: Repository](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Source Code" }
[:octicons-heart-16:](https://patreon.com/PeterCxy){ .card-link title=Contribute }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">تنوية</p>

عند استخدام Shelter، فأنت تضع ثقة كاملة في مطوّره، لأن Shelter يعمل كـ [Device Admin](https://developer.android.com/guide/topics/admin/device-admin) لإنشاء Work Profile، كما يمتلك صلاحيات واسعة للوصول إلى البيانات المخزنة داخل هذا الـ Work Profile.

</div>

نوصي باستخدام Shelter بدلا من [Insular](https://secure-system.gitlab.io/Insular) و[Island](https://github.com/oasisfeng/island)، لأنه يدعم [ميزة حظر البحث عن جهات الاتصال](https://secure-system.gitlab.io/Insular/faq.html) بين الـ profiles.

## Secure Camera

<small>يحمي من التهديدات التالية:</small>

- [:material-account-search: الانكشاف العام **Public Exposure**](../basics/common-threats.md#limiting-public-information){ .pg-green }

<div class="admonition recommendation" markdown>

![Secure camera logo](../assets/img/android/secure_camera.svg#only-light){ align=right }
![Secure camera logo](../assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

تطبيق **Secure Camera** هو تطبيق كاميرا يركز على الخصوصية والأمان، ويمكنه التقاط الصور ومقاطع الفيديو وقراءة QR codes. كما يدعم التطبيق إضافات CameraX vendor extensions على الأجهزة المتوافقة، مثل Portrait وHDR وNight Sight وFace Retouch وAuto.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/Camera#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

تشمل أهم ميزات الخصوصية:

- الإزالة التلقائية لبيانات [Exif](https://en.wikipedia.org/wiki/Exif) الوصفية metadata (مفعّلة افتراضيًا)
- استخدام واجهة [Media](https://developer.android.com/training/data-storage/shared/media) API الجديدة، ولذلك لا يحتاج التطبيق إلى [storage permissions](https://developer.android.com/training/data-storage)
- لا يحتاج التطبيق إلى صلاحية Microphone إلا إذا كنت تريد تسجيل الصوت

<div class="admonition note" markdown>
<p class="admonition-title">ملحوظة</p>

لا يتم حاليا حذف بيانات metadata من ملفات الفيديو، لكن من المخطط إضافة هذه الميزة مستقبلًا.

لا يتم حذف بيانات metadata الخاصة باتجاه الصورة. إذا فعلت الـ Location داخل تطبيق Secure Camera، فلن يتم حذف بيانات الموقع أيضا. إذا أردت حذف هذه البيانات لاحقا، فستحتاج إلى استخدام تطبيق خارجي مثل [ExifEraser](../data-redaction.md#exiferaser-android).

</div>

## Secure PDF Viewer

<small>يحمي من التهديدات التالية:</small>

- [:material-target-account: الهجمات الموجّهة **Targeted Attacks**](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }

<div class="admonition recommendation" markdown>

![Secure PDF Viewer logo](../assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Secure PDF Viewer logo](../assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

تطبيق Secure PDF Viewer هو تطبيق لعرض ملفات PDF يعتمد على [pdf.js](https://en.wikipedia.org/wiki/PDF.js)، ولا يحتاج إلى أي صلاحيات. يتم فتح ملف PDF داخل [WebView](https://developer.android.com/guide/webapps/webview) يعمل في بيئة [sandboxed](https://en.wikipedia.org/wiki/Sandbox_(software_development) معزولة، مما يساعد على تقليل قدرة الملف على التأثير في بقية النظام. هذا يعني أن التطبيق لا يحتاج إلى صلاحية مباشرة للوصول إلى المحتوى أو الملفات على جهازك.

يتم استخدام [Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) لضمان أن أكواد JavaScript وخصائص التنسيق داخل WebView تكون محتوى ثابتًا بالكامل ولا يمكن تغييرها أو تحميلها ديناميكيا.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer#readme){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## المعايير

يرجى ملاحظة أننا غير مرتبطين بأي من المشاريع التي نوصي بها. بالإضافة إلى [معاييرنا العامة](../about/criteria.md)، وضعنا مجموعة واضحة من المتطلبات التي تساعدنا على تقديم توصيات موضوعية. ننصحك بالاطلاع على هذه القائمة وفهمها قبل اختيار أي مشروع، وإجراء بحثك الخاص للتأكد من أنه الخيار المناسب لك.

- يجب ألا تندرج التطبيقات الموجودة في هذه الصفحة تحت أي فئة برمجية أخرى موجودة في الموقع.
- يجب أن تعمل التطبيقات العامة على تحسين وظائف النظام الأساسية أو استبدالها.
- يجب أن تحصل التطبيقات على تحديثات وصيانة بشكل منتظم.
