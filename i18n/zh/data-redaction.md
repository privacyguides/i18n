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

## MAT2

<div class="admonition recommendation" markdown>

![MAT2 logo](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2** is free, cross-platform software which allows you to remove metadata from image, audio, torrent, and document file types. It provides both a command line tool and a graphical user interface via an extension for [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin), the default file manager of [KDE](https://kde.org).

[:octicons-repo-16: Repository](https://0xacab.org/jvoisin/mat2){ .md-button .md-button--primary }
[:octicons-info-16:](https://0xacab.org/jvoisin/mat2/-/blob/master/README.md){ .card-link title="Documentation" }
[:octicons-code-16:](https://0xacab.org/jvoisin/mat2){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://pypi.org/project/mat2)
- [:simple-apple: macOS](https://0xacab.org/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: Linux](https://pypi.org/project/mat2)
- [:octicons-globe-16: Web](https://0xacab.org/jvoisin/mat2#web-interface)

</details>

</div>

## ExifEraser (安卓系统)

<div class="admonition recommendation" markdown>

![ExifEraser标志](assets/img/data-redaction/exiferaser.svg) { align=right }

**ExifEraser**是一个现代的、无权限的图像元数据删除应用程序，适用于Android。

它目前支持JPEG、PNG和WebP文件。

[:octicons-repo-16: Repository](https://github.com/Tommy-Geenexus/exif-eraser){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .card-link title="Documentation" }
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

## Shortcuts (iOS & macOS)

On iOS and macOS, you can remove image metadata without using any third-party apps by creating a [**shortcut**](https://apps.apple.com/app/id915249334) for this purpose. Here is an example shortcut you can download to use as is:

[:material-tag-minus: Clean Image Metadata](https://icloud.com/shortcuts/fb774ddb7b5b4296871776c67ac0fff9 ""){.md-button}

You can also use it as a model for your own shortcut; just make sure that the **Preserve Metadata** option under the **Convert** action is unchecked. Once added, you can access the shortcut in the share sheet that appears when you select the :octicons-share-24: Share button. You can select multiple images and invoke the shortcut to remove their metadata all at once.

This shortcut removes metadata such as location, device model, lens model, and other camera information. It also sets the image creation date to the time the shortcut was used.

## ExifTool (CLI)

<div class="admonition recommendation" markdown>

![ExifTool logo](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool** is the original Perl library and command-line application for reading, writing, and editing meta information (Exif, IPTC, XMP, and more) in a wide variety of file formats (JPEG, TIFF, PNG, PDF, RAW, and more).

It is often a component of other Exif removal applications and in most Linux distribution repositories.

[:octicons-home-16: Homepage](https://exiftool.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://exiftool.org/faq.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/exiftool/exiftool){ .card-link title="Source Code" }
[:octicons-heart-16:](https://exiftool.org/#donate){ .card-link title="Contribute" }

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
