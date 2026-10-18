---
meta_title: "메타데이터 제거 및 데이터 가리기 도구로 개인 식별 정보 지우기 - 프라이버시 가이드"
title: "데이터 및 메타데이터 가리기"
icon: material/tag-remove
description: 이 도구를 사용하여 공유하는 사진과 파일에서 GPS 위치 같은 메타데이터와 기타 식별 정보를 제거하세요.
cover: data-redaction.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-account-search: 공개 노출](basics/common-threats.md#limiting-public-information ""){.pg-green}

파일을 공유할 때는 관련 메타데이터를 반드시 제거하세요. 대부분의 일반적인 파일 형식(문서, 이미지, 동영상 포함)에는 메타데이터가 포함되어 있습니다. 예를 들어 이미지 파일에는 일반적으로 Exif 데이터가 포함되어 있습니다. 사진의 파일 메타데이터에는 GPS 좌표까지 포함되는 경우도 있습니다.

윈도우에는 메타데이터 제거 기능이 내장되어 있지만, 안타깝게도 다음과 같은 여러 유형의 데이터는 제거하지 못합니다:

- 문서: 메모, 작성자 이름, 변경 내용 추적, 숨겨진 워크시트, 슬라이드 노트, 사용자 지정 XML, 문서 수정 기록.
- 이미지: 카메라 일련번호, XMP/IPTC 데이터, C2PA 메타데이터, 이미지 미리 보기 이미지(잘라내거나 지운 영역의 원본 세부 정보가 위험하게 노출될 수 있음).
- 오디오 및 동영상: XMP 메타데이터, C2PA 메타데이터, 일부 ID3v2 태그 필드.
- 포함된 파일: 문서에 포함된 이미지 안에 중첩된 숨겨진 메타데이터.

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

[이미지 속 텍스트](https://bishopfox.com/blog/unredacter-tool-never-pixelation)를 가릴 때는 **절대로** 흐림 효과를 사용해서는 안 됩니다. 이미지 속 텍스트를 가리고 싶다면 텍스트 위에 상자를 그려야 합니다.

</div>

## MAT2

<div class="admonition recommendation" markdown>

![MAT2 로고](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2**는 이미지, 오디오, 토렌트, 문서 파일에서 메타데이터를 제거할 수 있는 무료 크로스 플랫폼 소프트웨어입니다. 명령줄 도구는 물론, [KDE](https://kde.org)의 기본 파일 관리자인 [돌핀](https://github.com/jvoisin/mat2/tree/master/dolphin)용 확장 프로그램을 통해 그래픽 사용자 인터페이스도 제공합니다.

[:octicons-repo-16: 저장소](https://github.com/jvoisin/mat2#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/jvoisin/mat2#how-to-use-mat2){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/jvoisin/mat2){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: 윈도우](https://pypi.org/project/mat2)
- [:simple-apple: macOS](https://github.com/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: 리눅스](https://pypi.org/project/mat2)
- [:octicons-browser-16: 웹](https://github.com/jvoisin/mat2#web-interface)

</details>

</div>

## 메타데이터 클리너 { #metadata-cleaner }

<div class="admonition recommendation" markdown>

![메타데이터 클리너 로고](assets/img/data-redaction/metadatacleaner.svg){ align=right }

**메타데이터 클리너**는 [MAT2](https://github.com/jvoisin/mat2)를 기반으로 하는 리눅스용 그래픽 메타데이터 제거 도구입니다.

[:octicons-home-16: 홈페이지](https://metadatacleaner.gitlab.io/metadatacleaner/){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitlab.com/metadatacleaner/metadatacleaner/){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://gitlab.com/metadatacleaner/metadatacleaner/-/blob/main/CONTRIBUTING.md){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-flathub: Flathub](https://flathub.org/en/apps/io.gitlab.metadatacleaner.metadatacleaner)

</details>

</div>

## ExifEraser(안드로이드) { #exiferaser-android }

<div class="admonition recommendation" markdown>

![ExifEraser 로고](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser**는 권한이 필요 없는 안드로이드용 최신 이미지 메타데이터 제거 애플리케이션입니다.

현재 JPEG, PNG, WebP 파일을 지원합니다.

[:octicons-repo-16: 저장소](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#description){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/Tommy-Geenexus/exif-eraser){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=com.none.tom.exiferaser)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/com.none.tom.exiferaser)
- [:simple-github: 깃허브](https://github.com/Tommy-Geenexus/exif-eraser/releases)

</details>

</div>

제거되는 메타데이터는 이미지 파일 형식에 따라 다릅니다:

- **JPEG**: ICC 프로필, Exif, Photoshop Image Resources, XMP/ExtendedXMP 메타데이터가 있으면 제거됩니다.
- **PNG**: ICC 프로필, Exif, XMP 메타데이터가 있으면 제거됩니다.
- **WebP**: ICC 프로필, Exif, XMP 메타데이터가 있으면 제거됩니다.

이미지를 처리한 후 ExifEraser는 각 이미지에서 정확히 무엇이 제거되었는지에 대한 전체 보고서를 제공합니다.

이 앱은 이미지에서 메타데이터를 제거하는 여러 가지 방법을 제공합니다. 구체적으로 다음과 같습니다:

- 다른 애플리케이션에서 ExifEraser로 이미지를 공유할 수 있습니다.
- 앱 자체에서 이미지 한 장, 여러 장, 또는 디렉터리 전체를 선택할 수 있습니다.
- 운영 체제의 카메라 앱으로 사진을 촬영한 다음 메타데이터를 제거하는 "카메라" 옵션이 있습니다.
- 분할 화면 모드에서 다른 앱과 ExifEraser를 함께 열어 두고, 다른 앱의 사진을 ExifEraser로 끌어다 놓을 수 있습니다.
- 마지막으로 클립보드에 있는 이미지를 붙여넣을 수 있습니다.

## 단축어(iOS 및 macOS) { #shortcuts-ios-macos }

iOS와 macOS에서는 이를 위한 [**단축어**](https://apps.apple.com/app/id915249334)를 만들어 서드파티 앱 없이도 이미지 메타데이터를 제거할 수 있습니다. 다음은 그대로 다운로드하여 사용할 수 있는 단축어 예시입니다:

[:material-tag-minus: 이미지 메타데이터 정리](https://icloud.com/shortcuts/fb774ddb7b5b4296871776c67ac0fff9 ""){.md-button}

자신만의 단축어를 만들 때 이를 모델로 삼을 수도 있습니다. **변환** 동작의 **메타데이터 보존** 옵션이 선택 해제되어 있는지만 확인하세요. 추가한 후에는 :octicons-share-24: 공유 버튼을 선택하면 나타나는 공유 시트에서 단축어를 사용할 수 있습니다. 여러 이미지를 선택하고 단축어를 실행하여 한꺼번에 메타데이터를 제거할 수 있습니다.

이 단축어는 위치, 기기 모델, 렌즈 모델, 기타 카메라 정보 같은 메타데이터를 제거합니다. 또한 이미지 생성 날짜를 단축어를 사용한 시각으로 설정합니다.

## ExifTool(CLI) { #exiftool-cli }

<div class="admonition recommendation" markdown>

![ExifTool 로고](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool**은 다양한 파일 형식(JPEG, TIFF, PNG, PDF, RAW 등)에서 메타 정보(Exif, IPTC, XMP 등)를 읽고, 쓰고, 편집하는 원조 펄 라이브러리이자 명령줄 애플리케이션입니다.

다른 Exif 제거 애플리케이션의 구성 요소로 쓰이는 경우가 많으며, 대부분의 리눅스 배포판 저장소에 포함되어 있습니다.

[:octicons-home-16: 홈페이지](https://exiftool.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://exiftool.org/faq.html){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/exiftool/exiftool){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://exiftool.org/#donate){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: 윈도우](https://exiftool.org)
- [:simple-apple: macOS](https://exiftool.org)
- [:simple-linux: 리눅스](https://exiftool.org)

</details>

</div>

<div class="admonition example" markdown>
<p class="admonition-title">디렉터리 내 파일에서 데이터 삭제하기</p>

```bash
exiftool -all= *.file_extension
```

</div>

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

- 오픈 소스 운영 체제용으로 개발된 앱은 오픈 소스여야 합니다.
- 앱은 무료여야 하며 광고나 기타 제한이 없어야 합니다.
