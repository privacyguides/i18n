---
meta_title: "أفضل خدمات التخزين السحابي من حيث الخصوصية والأمان - Privacy Guides"
title: التخزين السحابي
icon: material/file-cloud
description: تتطلب منك كثير من خدمات التخزين السحابي أن تثق بأنها لن تطلع على ملفاتك. إليك بدائل تحافظ على خصوصيتك!
cover: cloud.webp
---

<small>يحمي من التهديدات التالية:</small>

- [:material-bug-outline: الهجمات السلبية](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: مزودو الخدمات](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

تتطلب منك كثير من **خدمات التخزين السحابي** أن تثق بها تماما وألّا تطلع على ملفاتك. البدائل المذكورة أدناه تُغنيك عن الحاجة إلى الثقة بمزود الخدمة، لأنها تستخدم تشفير End-to-End Encryption الآمن.

إذا لم تناسبك هذه البدائل، فننصحك باستخدام برنامج تشفير مثل [Cryptomator](encryption.md#cryptomator-cloud) مع خدمة تخزين سحابي أخرى. قد يكون استخدام Cryptomator مع **أي** خدمة تخزين سحابي (بما فيها الخدمات المذكورة هنا) فكرة جيدة لتقليل مخاطر وجود ثغرات في التشفير داخل تطبيقات مزوّد الخدمة نفسها.

<details class="admonition info" markdown>
<summary>هل تبحث عن Nextcloud؟</summary>

للقراء الأكثر خبرة بالتقنية، [ما زلنا نوصي](self-hosting/file-management.md#nextcloud) باستخدام Nextcloud لاستضافة مجموعة أدوات لإدارة الملفات على خادم خاص بك. لكننا لا نوصي حاليا بخدمات التخزين التي توفرها جهات خارجية باستخدام Nextcloud، لأننا [لا ننصح](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) المستخدمين المنزليين بالاعتماد على ميزة End-to-End Encryption المدمجة فيه.

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Proton Drive logo](assets/images/cloud/protondrive.svg){ align=right }

خدمة **Proton Drive** هي خدمة تخزين سحابي مشفرة تقدمها الشركة نفسها التي توفر خدمة البريد الإلكتروني المشفر الشهيرة [Proton Mail](email.md#proton-mail).

تقتصر مساحة التخزين المجانية في البداية على 2 جيجابايت، لكن يمكنك الحصول على مساحة إضافية تصل إلى 5 جيجابايت بعد إكمال [بعض الخطوات](https://proton.me/support/more-free-storage-existing-users).

[:octicons-home-16: Homepage](https://proton.me/drive){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/drive/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)
- [:fontawesome-brands-windows: وندوز](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

The Proton Drive web application has been independently audited by Securitum in [2021](https://proton.me/community/open-source), but the brand new mobile clients have not yet been publicly audited by a third party.

## Tresorit

<div class="admonition recommendation" markdown>

![Tresorit logo](assets/images/cloud/tresorit.svg){ align=right }

خدمة **Tresorit** هي خدمة تخزين سحابي مشفّرة سويسرية مجرية، تأسست عام 2011. تملك خدمة البريد السويسري الوطنية (Swiss Post) شركة Tresorit.

[:octicons-home-16: Homepage](https://tresorit.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tresorit.com/legal/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.tresorit.com){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.tresorit.mobile)
- [:simple-appstore: App Store](https://apps.apple.com/app/id722163232)
- [:fontawesome-brands-windows: وندوز](https://tresorit.com/download)
- [:simple-apple: macOS](https://tresorit.com/download)
- [:simple-linux: لينكس](https://tresorit.com/download)

</details>

</div>

خضعت Tresorit لعدد من عمليات التدقيق الأمني المستقلة:

- [2022](https://tresorit.com/blog/tresorit-receives-iso-27001-certification): ISO/IEC 27001:2013[^1] Compliance [Certification](https://certipedia.com/quality_marks/9108644476) by TÜV Rheinland InterCert Kft
- [2021](https://tresorit.com/blog/fresh-penetration-testing-confirms-tresorit-security): اختبار اختراق أجرته شركة Computest
    - قيمت هذه المراجعة أمان تطبيق Tresorit على الويب وAndroid وWindows، بالإضافة إلى البنية التحتية المرتبطة بها.
    - اكتشفت Computest ثغرتين أمنيتين، وقد تم إصلاحهما.
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): اختبار اختراق أجرته شركة Ernst & Young.
    - حللت هذه المراجعة الـ Source Code الكاملة لـ Tresorit، وتحققت من أن طريقة تنفيذها تتوافق مع المفاهيم الموضحة في المستند التقني [(White Paper) ](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf)الخاص بها.
    - أجرت شركة Ernst & Young أيضا اختبارات على تطبيقات الويب والهواتف وأجهزة الكمبيوتر. وخلصت الشركة إلى ما يلي:

        > لم تُظهر نتائج الاختبارات أي تعارض مع ادعاءات Tresorit بشأن سرية البيانات.

## Peergos

<div class="admonition recommendation" markdown>

![Peergos logo](assets/images/cloud/peergos.svg){ align=right }

بروتوكول **Peergos** هو بروتوكول لامركزي ومنصة مفتوحة المصدر لتخزين الملفات والتواصل الاجتماعي والتطبيقات. يوفر Peergos مساحة آمنة وخاصة تتيح للمستخدمين تخزين الصور والفيديوهات والمستندات وغيرها من الملفات، ومشاركتها وعرضها وتعديلها.

يحمي Peergos ملفاتك باستخدام End-to-End Encryption المقاوم لهجمات الحوسبة الكمية، ويضمن الحفاظ على خصوصية جميع البيانات المتعلقة بملفاتك. يمكنك أيضا [استضافته على خادمك الخاص](https://book.peergos.org/features/self).

[:octicons-home-16: Homepage](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://book.peergos.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/peergos/peergos#support){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=peergos.android)
- [:simple-github: GitHub](https://github.com/Peergos/web-ui/releases)
- [:fontawesome-brands-windows: وندوز](https://peergos.org/download#windows)
- [:simple-apple: macOS](https://peergos.org/download#macos)
- [:simple-linux: لينكس](https://peergos.org/download#linux)
- [:octicons-browser-16: Web](https://peergos.net)

</details>

</div>

يعتمد Peergos على [InterPlanetary File System (IPFS)](https://ipfs.tech)، وهي بنية تعتمد على الاتصال المباشر بين الأجهزة (Peer-to-Peer) وتساعد على الحماية من [:material-close-outline: الرقابة](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}.

يعمل كل من تطبيق Peergos والخادم وواجهة سطر الأوامر (command line interface) من الملف التنفيذي نفسه. بالإضافة إلى ذلك، يتضمن Peergos [أداة مزامنة (Sync Engine)](https://book.peergos.org/features/sync) متاحة عبر تطبيقاته الأصلية، تتيح مزامنة مجلد على جهازك مع مجلد على Peergos في الاتجاهين، بحيث تنتقل التغييرات بينهما. كما يوفر [واجهة WebDAV](https://book.peergos.org/features/webdav) تتيح للتطبيقات الأخرى الوصول إلى ملفاتك المخزنة على Peergos. يمكنك الاطلاع على وثائق Peergos الرسمية للتعرف على جميع ميزاته المتعددة بالتفصيل.

خضع Peergos [لتدقيق](https://peergos.org/posts/security-audit-2024) أمني أجرته شركة Radically Open Security في نوفمبر 2024، وقد تم إصلاح جميع المشكلات التي اكتشفت. خضع Peergos أيضا [لتدقيق](https://cure53.de/pentest-report_peergos.pdf) أمني سابق أجرته شركة Cure53 في يونيو 2019، وأُصلحت جميع المشكلات التي اكتشفت لاحقا.

## المعايير

**يرجى العلم أننا لسنا تابعين لأي من المشاريع التي نوصي بها.** وإلى جانب [معاييرنا الأساسية](about/criteria.md)، وضعنا مجموعة واضحة من المتطلبات حتى نتمكن من تقديم توصيات موضوعية. ننصحك بالاطلاع على هذه القائمة قبل اختيار أي مشروع لاستخدامه، وإجراء بحثك الخاص للتأكد من أنه الخيار المناسب لك.

### الحد الأدنى من المتطلبات

- يجب أن يفرض استخدام End-to-End Encryption.
- يجب أن يوفر خطة مجانية أو فترة تجريبية لاختبار الخدمة.
- يجب أن يدعم الـ Multifactor Authentication (MFA) باستخدام TOTP أو FIDO2، أو تسجيل الدخول باستخدام Passkeys.
- يجب أن يوفر واجهة ويب تدعم الوظائف الأساسية لإدارة الملفات.
- يجب أن يتيح تصدير جميع الملفات والمستندات بسهولة.

### أحسن الاحتمالات

تمثل معاييرنا المثالية ما نود توفره في أفضل مشروع ضمن هذه الفئة. قد لا تتوفر بعض هذه الميزات أو جميعها في المشاريع التي نوصي بها، لكن المشاريع التي توفرها قد تحصل على ترتيب أعلى من غيرها في هذه الصفحة.

- يُفضل أن تكون التطبيقات مفتوحة المصدر.
- يُفضل أن تخضع التطبيقات بالكامل لتدقيق أمني من جهة خارجية مستقلة.
- يُفضل أن يوفر تطبيقات مخصصة لأنظمة Linux وAndroid وWindows وmacOS وiOS.
    - يُفضل أن تتكامل هذه التطبيقات مع الأدوات المدمجة في نظام التشغيل للتعامل مع خدمات التخزين السحابي، مثل التكامل مع تطبيق Files على iOS، أو دعم وظيفة DocumentsProvider على Android.
- يُفضل أن يتيح مشاركة الملفات بسهولة مع المستخدمين الآخرين.
- Should offer at least basic file preview and editing functionality on the web interface.

[^1]: يشير الامتثال لمعيار [ISO/IEC 27001:2013](https://en.wikipedia.org/wiki/ISO/IEC_27001) إلى [نظام إدارة أمن المعلومات](https://en.wikipedia.org/wiki/Information_security_management) في الشركة، ويشمل بيع خدماتها السحابية وتطويرها وصيانتها وتقديم الدعم الفني لها
