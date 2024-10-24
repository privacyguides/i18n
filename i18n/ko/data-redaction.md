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

## 데스크톱

### MAT2

<div class="admonition recommendation" markdown>

![MAT2 로고](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2**는 이미지, 오디오, 토렌트, 문서 파일 형식에서 메타데이터를 제거할 수 있는 자유 소프트웨어입니다. It provides both a command line tool and a graphical user interface via an extension for [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin), the default file manager of [KDE](https://kde.org).

Linux에서는 MAT2를 기반으로 제3자가 제작한 GUI 프로그램인 [Metadata Cleaner](https://gitlab.com/rmnvgr/metadata-cleaner)를 [Flathub](https://flathub.org/apps/details/fr.romainvigier.MetadataCleaner)에서 설치할 수 있습니다.

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

## 모바일

### ExifEraser (Android)

<div class="admonition recommendation" markdown>

![ExifEraser 로고](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser**는 Android용 이미지 메타데이터 제거 애플리케이션으로, 최신식이며 시스템 권한을 필요로 하지 않습니다.

현재 JPEG, PNG, WebP 파일을 지원합니다.

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

### Metapho (iOS)

<div class="admonition recommendation" markdown>

![Metapho 로고](assets/img/data-redaction/metapho.jpg){ align=right }

**Metapho**는 날짜, 파일명, 파일 크기, 카메라 모델, 셔터 속도, 위치 등 사진 메타데이터를 간단하고 깔끔하게 볼 수 있는 애플리케이션입니다.

[:octicons-home-16: Homepage](https://zininworks.com/metapho){ .md-button .md-button--primary }
[:octicons-eye-16:](https://zininworks.com/privacy){ .card-link title="Privacy Policy" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id914457352)

</details>

</div>

### PrivacyBlur

<div class="admonition recommendation" markdown>

![PrivacyBlur 로고](assets/img/data-redaction/privacyblur.svg){ align=right }

**PrivacyBlur**는 사진을 온라인에 공유하기 전에 민감한 부분을 흐릿하게 만들 수 있는 무료 앱입니다.

[:octicons-home-16: Homepage](https://privacyblur.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://privacyblur.app/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/MATHEMA-GmbH/privacyblur#readme){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/MATHEMA-GmbH/privacyblur){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.mathema.privacyblur)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1536274106)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

이미지 내 텍스트를 지우는 용도로 블러 처리를 사용해서는 [**절대** 안 됩니다](https://bishopfox.com/blog/unredacter-tool-never-pixelation). 이미지 내 텍스트를 지울 때는 텍스트 위에 박스를 그려야 합니다. 해당 용도로는 [Pocket Paint](https://github.com/Catrobat/Paintroid) 등의 앱을 추천드립니다.

</div>

## 커맨드라인

### ExifTool

<div class="admonition recommendation" markdown>

![ExifTool 로고](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool**은 다양한 파일 형식(JPEG, TIFF, PNG, PDF, RAW 등) 메타데이터(Exif, IPTC, XMP 등)의 읽기/쓰기/편집이 가능한 오리지널 Perl 라이브러리 및 CLI 애플리케이션입니다.

다른 Exif 제거 애플리케이션에서 구성 요소로 쓰이는 경우가 많고 대부분의 Linux 배포판 패키지 저장소에 존재합니다.

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

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

- Apps developed for open-source operating systems must be open source.
- 무료 앱이어야 하며, 광고 및 기타 제약 사항이 존재해서는 안 됩니다.
