---
title: إدارة الملفات
meta_title: "استضافة أدوات إدارة الملفات بنفسك - Privacy Guides"
icon: material/file-multiple-outline
description: للقراء الذين لديهم خبرة تقنية أكبر، يمكن أن توفر استضافة أدوات إدارة الملفات بأنفسهم خصوصية إضافية، لأنها تمنحهم تحكما أكبر في بياناتهم.
cover: cloud.webp
---

<small>يحمي من التهديدات التالية:</small>

- [:material-server-network: مقدّمو الخدمات](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

قد تكون استضافة أدوات إدارة الملفات بنفسك فكرة جيدة لتقليل المخاطر الناتجة عن عيوب التشفير في التطبيقات الرسمية لمزوّدي الخدمات السحابية.

## إدارة الصور

### PhotoPrism

<div class="admonition recommendation" markdown>

![PhotoPrism logo](../assets/img/self-hosting/photoprism.svg){ align=right }

منصة PhotoPrism هي منصة لإدارة الصور. تدعم مزامنة ألبومات الصور ومشاركتها، بالإضافة إلى مجموعة متنوعة من [الميزات](https://photoprism.app/features) الأخرى. لا تدعم التشفير التام بين الطرفين (End-to-End Encryption)، لذلك يُفضل استضافتها على خادم تثق به ويكون تحت سيطرتك.

[:octicons-home-16: Homepage](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Source Code" }

</div>

## مشاركة الملفات ومزامنتها

### FreedomBox

<div class="admonition recommendation" markdown>

![FreedomBox logo](../assets/img/self-hosting/freedombox.svg){ align=right }

نظام **FreedomBox** هو نظام تشغيل مصمم للعمل على [كمبيوتر أحادي اللوحة (SBC)](https://en.wikipedia.org/wiki/Single-board_computer). يهدف إلى تسهيل إعداد تطبيقات الخوادم لأغراض مختلفة، مثل مشاركة الملفات.

[:octicons-home-16: Homepage](https://freedombox.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title="Documentation" }
[:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="Source Code" }
[:octicons-heart-16:](https://freedomboxfoundation.org/donate){ .card-link title="Contribute" }

</div>

### Nextcloud

<div class="admonition recommendation" markdown>

![Nextcloud logo](../assets/img/self-hosting/nextcloud.svg){ align=right }

مجموعة Nextcloud هي مجموعة من البرامج المجانية ومفتوحة المصدر، تتيح لك إنشاء خدمة خاصة لاستضافة ملفاتك على خادم تتحكم فيه بنفسك.

[:octicons-home-16: Homepage](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Source Code" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title="Contribute" }

<details class="downloads" markdown><summary>التنزيلات</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
- [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
- [:fontawesome-brands-windows: ويندوز](https://nextcloud.com/install/#install-clients)
- [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
- [:simple-linux: لينكس](https://nextcloud.com/install/#install-clients)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">تحذير</p>

لا ننصح باستخدام [تطبيق E2EE](https://apps.nextcloud.com/apps/end_to_end_encryption) في Nextcloud، لأنه قد يؤدي إلى فقدان البيانات. فهو لا يزال تجريبيا بدرجة كبيرة وغير مناسب للاستخدام الفعلي. لهذا السبب، لا ننصح باستخدام خدمات Nextcloud التي توفرها جهات خارجية.

</div>
