---
meta_title: "Remove PII with Metadata Scrubbers and Data Redaction Tools - Privacy Guides"
title: "Data and Metadata Redaction"
icon: material/tag-remove
description: Use these tools to remove metadata like GPS location and other identifying information from photos and files you share.
cover: data-redaction.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-search: 公开曝光](basics/common-threats.md#limiting-public-information ""){.pg-green}

共享文件时，请务必删除关联的元数据。 图像文件通常包括 [Exif](https://en.wikipedia.org/wiki/Exif) 数据。 照片有时甚至包括文件元数据中的GPS坐标。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

您应该* *从不* *使用模糊来编辑[图片中的文本](https://bishopfox.com/blog/unredacter-tool-never-pixelation)。 If you want to redact text in an image, you should draw a box over the text.

</div>

## 电脑版

### MAT2

<div class="admonition recommendation" markdown>

![MAT2标志](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2**是免费软件，它允许从图像、音频、洪流和文件类型中删除元数据。 It provides both a command line tool and a graphical user interface via an extension for [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin), the default file manager of [KDE](https://kde.org).

在Linux上，存在一个由MAT2驱动的第三方图形工具[Metadata Cleaner](https://gitlab.com/rmnvgr/metadata-cleaner)，并[在Flathub上提供](https://flathub.org/apps/details/fr.romainvigier.MetadataCleaner)。

[:octicons-repo-16: Repository](https://0xacab.org/jvoisin/mat2){ .md-button .md-button--primary }
[:octicons-info-16:](https://0xacab.org/jvoisin/mat2/-/blob/master/README.md){ .card-link title=Documentation}
[:octicons-code-16:](https://0xacab.org/jvoisin/mat2){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://pypi.org/project/mat2)
- [:simple-apple: macOS](https://0xacab.org/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: Linux](https://pypi.org/project/mat2)
- [:octicons-globe-16: Web](https://0xacab.org/jvoisin/mat2#web-interface)

</details>

</div>

## Android

### ExifEraser (安卓系统)

<div class="admonition recommendation" markdown>

![ExifEraser标志](assets/img/data-redaction/exiferaser.svg) { align=right }

**ExifEraser**是一个现代的、无权限的图像元数据删除应用程序，适用于Android。

它目前支持JPEG、PNG和WebP文件。

[:octicons-repo-16: Repository](https://github.com/Tommy-Geenexus/exif-eraser){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/Tommy-Geenexus/exif-eraser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.none.tom.exiferaser)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/com.none.tom.exiferaser)
- [:simple-github: GitHub](https://github.com/Tommy-Geenexus/exif-eraser/releases)

</details>

</div>

被删除的元数据取决于图像的文件类型。

- **JPEG**: ICC Profile、Exif、Photoshop Image Resources和XMP/ExtendedXMP元数据如果存在，将被删除。
- **PNG**：ICC Profile、Exif和XMP元数据如果存在，将被删除。
- **WebP**：ICC Profile、Exif和XMP元数据如果存在，将被删除。

在处理完图像后，ExifEraser会向你提供一份完整的报告，说明每张图像中到底有哪些被删除。

该应用程序提供多种方法来消除图像中的元数据。 名称：

- 你可以用ExifEraser分享另一个应用程序的图像。
- 通过应用程序本身，你可以选择一张图片，一次选择多张图片，甚至是整个目录。
- 它有一个 "相机 "选项，它使用你的操作系统的相机应用程序来拍摄照片，然后它将元数据从照片中删除。
- 它允许你将照片从另一个应用程序拖入ExifEraser，当它们都以分屏模式打开时。
- 最后，它允许你从剪贴板上粘贴图片。

### Metapho (iOS)

<div class="admonition recommendation" markdown>

![Metapho标志](assets/img/data-redaction/metapho.jpg){ align=right }

**Metapho**是一个简单而干净的照片元数据查看器，如日期、文件名、大小、相机型号、快门速度和位置。

[:octicons-home-16: Homepage](https://zininworks.com/metapho){ .md-button .md-button--primary }
[:octicons-eye-16:](https://zininworks.com/privacy){ .card-link title="Privacy Policy" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id914457352)

</details>

</div>

## Command-line

### ExifTool

<div class="admonition recommendation" markdown>

![ExifTool标志](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool**是原始的perl库和命令行应用程序，用于读取、写入和编辑各种文件格式（JPEG、TIFF、PNG、PDF、RAW等）的元信息（Exif、IPTC、XMP等）。

它通常是其他Exif删除应用程序的一个组成部分，并且在大多数Linux发行库中。

[:octicons-home-16: Homepage](https://exiftool.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://exiftool.org/faq.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/exiftool/exiftool){ .card-link title="Source Code" }
[:octicons-heart-16:](https://exiftool.org/#donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://exiftool.org)
- [:simple-apple: macOS](https://exiftool.org)
- [:simple-linux: Linux](https://exiftool.org)

</details>

</div>

<div class="admonition example" markdown>
<p class="admonition-title">Deleting data from a directory of files</p>

```bash
exiftool -all= *.file_extension
```

</div>

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

- Apps developed for open-source operating systems must be open source.
- 应用程序必须是免费的，不应包括广告或其他限制。
