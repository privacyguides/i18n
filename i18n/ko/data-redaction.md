---
meta_title: "Remove PII with Metadata Scrubbers and Data Redaction Tools - Privacy Guides"
title: "Data and Metadata Redaction"
icon: material/tag-remove
description: Use these tools to remove metadata like GPS location and other identifying information from photos and files you share.
cover: data-redaction.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-search: 공개 노출(Public Exposure)](basics/common-threats.md#limiting-public-information ""){.pg-green}

파일을 공유할 때에는 관련 메타데이터를 제거해야 합니다. 이미지 파일에는 보통 [Exif](https://en.wikipedia.org/wiki/Exif) 데이터가 포함되어 있습니다. 사진 파일 메타데이터에는 GPS 좌표가 포함될 때도 있습니다.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

이미지 내 텍스트를 지우는 용도로 블러 처리를 사용해서는 [**절대** 안 됩니다](https://bishopfox.com/blog/unredacter-tool-never-pixelation). If you want to redact text in an image, you should draw a box over the text.

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

## ExifEraser (Android)

<div class="admonition recommendation" markdown>

![ExifEraser 로고](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser**는 Android용 이미지 메타데이터 제거 애플리케이션으로, 최신식이며 시스템 권한을 필요로 하지 않습니다.

현재 JPEG, PNG, WebP 파일을 지원합니다.

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

지워지는 메타데이터는 이미지 파일 유형에 따라 달라집니다:

- **JPEG**: ICC 프로필, Exif, Photoshop Image Resources, XMP/ExtendedXMP 메타데이터가 제거됩니다.
- **PNG**: ICC 프로필, Exif, XMP 메타데이터가 제거됩니다.
- **WebP**: ICC 프로필, Exif, XMP 메타데이터가 제거됩니다.

이미지를 처리한 후에는 각 이미지에서 정확히 무엇이 제거됐는지 정리된 전체 기록을 볼 수 있습니다.

ExifEraser로 이미지 메타데이터를 제거하는 방법은 다양합니다. 예시는 다음과 같습니다:

- 다른 애플리케이션에서 이미지의 공유 대상으로 ExifEraser를 선택할 수 있습니다.
- 앱 내에서 단일 및 여러 이미지, 혹은 디렉터리 전체를 선택할 수 있습니다.
- 시스템 기본 카메라 앱을 사용해 사진을 촬영하고 메타데이터를 제거하는 '카메라' 옵션이 있습니다.
- 다른 앱과 ExifEraser가 분할 화면 모드로 열려 있을 때, 다른 앱에서 사진을 ExifEraser로 드래그할 수 있습니다.
- 클립보드에서 이미지를 붙여넣을 수 있습니다.

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

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

- Apps developed for open-source operating systems must be open source.
- 무료 앱이어야 하며, 광고 및 기타 제약 사항이 존재해서는 안 됩니다.
