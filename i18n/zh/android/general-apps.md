---
title: "常规App"
description: 此处列出的App为Android专属，专门用于增强或替换关键的系统功能。
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: 常规Android App
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

<small>防范以下威胁：</small>

- [:material-bug-outline: 被动攻击](../basics/common-threats.md#security-and-privacy){ .pg-orange }

我们在整个网站中推荐了各种各样的Android App。此处列出的App为Android专属，专门用于增强或替换关键的系统功能。

## Shelter

如果您的设备运行的是Android 15或更高版本，我们建议改用原生的[私密空间](../os/android-overview.md#private-space)功能，该功能提供几乎相同的功能，而无需信任并向第三方App授予强大的权限。

<div class="admonition recommendation" markdown>

![Shelter logo](../assets/img/android/shelter.svg){ align=right }

**Shelter** 是一款帮助您利用Android工作配置文件功能在设备上隔离或复制App的应用程序。

Shelter支持阻止跨配置文件的联系人搜索，并通过默认文件管理器（[DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)）跨配置文件共享文件。

[:octicons-repo-16: 仓库](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="源代码" }
[:octicons-heart-16:](https://patreon.com/PeterCxy){ .card-link title=贡献 }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

使用Shelter时，您对其开发者寄予了完全的信任，因为Shelter充当[设备管理员](https://developer.android.com/guide/topics/admin/device-admin)来创建工作配置文件，并且它对存储在工作配置文件中的数据具有广泛的访问权限。

</div>

相比于[Insular](https://secure-system.gitlab.io/Insular)和[Island](https://github.com/oasisfeng/island)，我们更推荐Shelter，因为它支持[联系人搜索拦截](https://secure-system.gitlab.io/Insular/faq.html)。

## Secure Camera

<small>防范以下威胁：</small>

- [:material-account-search: 公开暴露](../basics/common-threats.md#limiting-public-information){ .pg-green }

<div class="admonition recommendation" markdown>

![Secure Camera logo](../assets/img/android/secure_camera.svg#only-light){ align=right }
![Secure Camera logo](../assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

**Secure Camera** 是一款专注于隐私和安全的相机App，可以拍摄图像、视频和扫描二维码。在支持的设备上，它还支持CameraX供应商扩展（人像、HDR、夜视、面部修饰和自动）。

[:octicons-repo-16: 仓库](https://github.com/GrapheneOS/Camera#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=文档}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="源代码" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=贡献 }

<details class="downloads" markdown>
<summary>下载</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

主要的隐私功能包括：

- 自动移除[Exif](https://en.wikipedia.org/wiki/Exif)元数据（默认启用）
- 使用新的[Media](https://developer.android.com/training/data-storage/shared/media) API，因此不需要[存储权限](https://developer.android.com/training/data-storage)
- 除非您想录音，否则不需要麦克风权限

<div class="admonition note" markdown>
<p class="admonition-title">注意</p>

目前尚未从视频文件中删除元数据，但这已在计划中。

图像方向元数据不会被删除。如果您（在Secure Camera中）启用了位置信息，它也**不会**被删除。如果您想在以后删除它，则需要使用外部App，例如[ExifEraser](../data-redaction.md#exiferaser-android)。

</div>

## Secure PDF Viewer

<small>防范以下威胁：</small>

- [:material-target-account: 针对性攻击](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }

<div class="admonition recommendation" markdown>

![Secure PDF Viewer logo](../assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Secure PDF Viewer logo](../assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

**Secure PDF Viewer** 是一个基于[pdf.js](https://en.wikipedia.org/wiki/PDF.js)的PDF查看器，不需要任何权限。 PDF被送入一个[沙盒化](https://en.wikipedia.org/wiki/Sandbox_(software_development))的[WebView](https://developer.android.com/guide/webapps/webview)中。这意味着它不需要直接访问内容或文件的权限。

[内容安全策略 (Content-Security-Policy)](https://en.wikipedia.org/wiki/Content_Security_Policy) 用于强制WebView中的JavaScript和样式属性完全是静态内容。

[:octicons-repo-16: 仓库](https://github.com/GrapheneOS/PdfViewer#readme){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="源代码" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=贡献 }

<details class="downloads" markdown>
<summary>下载</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## 标准

**请注意，我们与我们推荐的任何项目均无附属关系。** 除了[我们的标准](../about/criteria.md)之外，我们还制定了一套明确的要求，使我们能够提供客观的建议。我们建议您在选择使用某个项目之前熟悉此列表，并进行自己的研究以确保它是您的正确选择。

- 此页面上的App不得适用于本网站上的任何其他软件类别。
- 常规应用程序应扩展或替换核心系统功能。
- 应用程序应定期接收更新和维护。
