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

Shelter is recommended over [Insular](https://secure-system.gitlab.io/Insular) and [Island](https://github.com/oasisfeng/island) as it supports [contact search blocking](https://secure-system.gitlab.io/Insular/faq.html).

## Secure Camera

<small>Protects against the following threat(s):</small>

- [:material-account-search: Public Exposure](../basics/common-threats.md#limiting-public-information){ .pg-green }

<div class="admonition recommendation" markdown>

![Secure camera logo](../assets/img/android/secure_camera.svg#only-light){ align=right }
![Secure camera logo](../assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

**Secure Camera** is a camera app focused on privacy and security which can capture images, videos, and QR codes. CameraX vendor extensions (Portrait, HDR, Night Sight, Face Retouch, and Auto) are also supported on available devices.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/Camera#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

Main privacy features include:

- Auto removal of [Exif](https://en.wikipedia.org/wiki/Exif) metadata (enabled by default)
- Use of the new [Media](https://developer.android.com/training/data-storage/shared/media) API, therefore [storage permissions](https://developer.android.com/training/data-storage) are not required
- Microphone permission not required unless you want to record sound

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Metadata is not currently deleted from video files, but that is planned.

The image orientation metadata is not deleted. If you enable location (in Secure Camera) that **won't** be deleted either. If you want to delete that later you will need to use an external app such as [ExifEraser](../data-redaction.md#exiferaser-android).

</div>

## Secure PDF Viewer

<small>Protects against the following threat(s):</small>

- [:material-target-account: Targeted Attacks](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }

<div class="admonition recommendation" markdown>

![Secure PDF Viewer logo](../assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Secure PDF Viewer logo](../assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

**Secure PDF Viewer** is a PDF viewer based on [pdf.js](https://en.wikipedia.org/wiki/PDF.js) that doesn't require any permissions. The PDF is fed into a [sandboxed](https://en.wikipedia.org/wiki/Sandbox_(software_development)) [WebView](https://developer.android.com/guide/webapps/webview). This means that it doesn't require permission directly to access content or files.

[Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) is used to enforce that the JavaScript and styling properties within the WebView are entirely static content.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer#readme){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](../about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

- Applications on this page must not be applicable to any other software category on the site.
- General applications should extend or replace core system functionality.
- Applications should receive regular updates and maintenance.
