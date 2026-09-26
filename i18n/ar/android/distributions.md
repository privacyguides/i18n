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
    "@type": ""
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

يوفر GrapheneOS المزيد من تحسينات [التقوية الأمنية](https://en.wikipedia.org/wiki/Hardening_(computing) (Security Hardening) وميزات إضافية لتعزيز الخصوصية. يحتوي على [مُخصص ذاكرة مُعزز](https://github.com/GrapheneOS/hardened_malloc) (Hardened Memory Allocator)، وأذونات للتحكم في الوصول إلى الشبكة والمستشعرات، إلى جانب العديد من [ميزات الأمان الأخرى](https://grapheneos.org/features). GrapheneOS also comes with full firmware updates and signed builds, so verified boot is fully supported.

[:octicons-home-16: Homepage](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title="Contribute" }

</div>

يدعم GrapheneOS تشغيل Google Play داخل [بيئة معزولة](https://grapheneos.org/usage#sandboxed-google-play) (Sandboxed Google Play)، حيث تعمل خدمات Google Play داخل Sandbox بالكامل مثل أي تطبيق عادي آخر. هذا يعني أنه يمكنك الاستفادة من معظم خدمات Google Play، مثل الإشعارات الفورية (Push Notifications)، مع الاحتفاظ بالتحكم الكامل في أذوناتها وما يمكنها الوصول إليه، بالإضافة إلى إمكانية حصرها داخل [ملف عمل](../os/android-overview.md#work-profile) (Work Profile) أو [ملف مستخدم](../os/android-overview.md#user-profiles) (User Profile) محدد من اختيارك.

تُعد هواتف Google Pixel الأجهزة الوحيدة التي تستوفي حاليا الـ [متطلبات أمان العتاد (Hardware Security Requirements)](https://grapheneos.org/faq#future-devices) الخاصة بـ GrapheneOS. يدعم Pixel 8 والإصدارات الأحدث ميزة Memory Tagging Extension (MTE) من ARM، وهي ميزة أمان على مستوى الـ Hardware تقلل بشكل كبير من احتمال استغلال الثغرات الناتجة عن أخطاء تلف الذاكرة (Memory Corruption Bugs). GrapheneOS greatly expands the coverage of MTE on supported devices. Whereas the stock OS only allows you to opt in to a limited implementation of MTE via a developer option or Google's Advanced Protection Program, GrapheneOS features a more robust implementation of MTE by default in the system kernel, default system components, and their Vanadium web browser and its WebView.

GrapheneOS also provides a global toggle for enabling MTE on all user-installed apps at :gear: **Settings** → **Security & privacy** → **Exploit protection** → **Memory tagging** → **Enable by default**. The OS also features per-app toggles to opt out of MTE for apps which may crash due to compatibility issues.

### Connectivity Checks

By default, Android makes many network connections to Google to perform DNS connectivity checks, to sync with current network time, to check your network connectivity, and for many other background tasks. GrapheneOS replaces these with connections to servers operated by GrapheneOS and subject to their privacy policy. This hides information like your IP address [from Google](../basics/common-threats.md#privacy-from-service-providers), but means it is trivial for an admin on your network or ISP to see you are making connections to `grapheneos.network`, `grapheneos.org`, etc. and deduce what operating system you are using.

If you want to hide information like this from an adversary on your network or ISP, you **must** use a [trusted VPN](../vpn.md) in addition to changing the connectivity check setting to **Standard (Google)**. It can be found in :gear: **Settings** → **Network & internet** → **Internet connectivity checks**. This option allows you to connect to Google's servers for connectivity checks, which, alongside the usage of a VPN, helps you blend in with a larger pool of Android devices.

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](../about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

- Must be open-source software.
- Must support bootloader locking with custom AVB key support.
- Must receive major Android updates within 0-1 months of release.
- Must receive Android feature updates (minor version) within 0-14 days of release.
- Must receive regular security patches within 0-5 days of release.
- Must **not** be "rooted" out of the box.
- Must **not** enable Google Play Services by default.
- Must **not** require system modification to support Google Play Services.
