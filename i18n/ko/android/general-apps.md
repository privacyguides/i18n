---
title: "일반 앱"
description: 여기에 나열된 앱은 안드로이드 전용으로, 핵심 시스템 기능을 강화하거나 대체하는 데 특화되어 있습니다.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: 일반 안드로이드 앱
    url: "./"
  - "@context": http://schema.org
    "@type": MobileApplication
    name: 셸터
    applicationCategory: Utilities
    operatingSystem: Android
  - "@context": http://schema.org
    "@type": MobileApplication
    name: 시큐어 카메라
    applicationCategory: Utilities
    operatingSystem: Android
  - "@context": http://schema.org
    "@type": MobileApplication
    name: 시큐어 PDF 뷰어
    applicationCategory: Utilities
    operatingSystem: Android
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-bug-outline: 수동적 공격](../basics/common-threats.md#security-and-privacy){ .pg-orange }

프라이버시 가이드는 이 사이트 곳곳에서 다양한 안드로이드 앱을 추천하고 있습니다. 여기에 나열된 앱은 안드로이드 전용으로, 핵심 시스템 기능을 강화하거나 대체하는 데 특화되어 있습니다.

## 셸터 { #shelter }

기기가 안드로이드 15 이상이라면 대신 기본 제공되는 [비공개 스페이스](../os/android-overview.md#private-space) 기능을 사용할 것을 권장합니다. 비공개 스페이스는 서드파티 앱을 신뢰하거나 강력한 권한을 부여할 필요 없이 거의 동일한 기능을 제공합니다.

<div class="admonition recommendation" markdown>

![셸터 로고](../assets/img/android/shelter.svg){ align=right }

**셸터**는 안드로이드의 직장 프로필 기능을 활용하여 기기의 앱을 격리하거나 복제할 수 있도록 도와주는 앱입니다.

셸터는 프로필 간 연락처 검색 차단과 기본 파일 관리자([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui))를 통한 프로필 간 파일 공유를 지원합니다.

[:octicons-repo-16: 저장소](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://patreon.com/PeterCxy){ .card-link title="후원하기" }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

셸터는 직장 프로필을 생성하기 위해 [기기 관리자](https://developer.android.com/guide/topics/admin/device-admin) 역할을 하며 직장 프로필에 저장된 데이터에 광범위하게 접근할 수 있으므로, 셸터를 사용하면 개발자를 전적으로 신뢰하게 됩니다.

</div>

셸터는 [연락처 검색 차단](https://secure-system.gitlab.io/Insular/faq.html)을 지원하므로 [인슐러](https://secure-system.gitlab.io/Insular)나 [아일랜드](https://github.com/oasisfeng/island)보다 셸터를 권장합니다.

## 시큐어 카메라 { #secure-camera }

<small>다음 위협으로부터 보호합니다:</small>

- [:material-account-search: 공개 노출](../basics/common-threats.md#limiting-public-information){ .pg-green }

<div class="admonition recommendation" markdown>

![시큐어 카메라 로고](../assets/img/android/secure_camera.svg#only-light){ align=right }
![시큐어 카메라 로고](../assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

**시큐어 카메라**는 프라이버시와 보안에 중점을 둔 카메라 앱으로, 사진과 동영상을 촬영하고 QR 코드를 스캔할 수 있습니다. 지원되는 기기에서는 CameraX 제조사 확장 기능(인물 사진, HDR, 야간 모드, 얼굴 보정, 자동)도 사용할 수 있습니다.

[:octicons-repo-16: 저장소](https://github.com/GrapheneOS/Camera#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: 깃허브](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: 그래핀OS 앱 스토어](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

주요 프라이버시 기능은 다음과 같습니다:

- [Exif](https://en.wikipedia.org/wiki/Exif) 메타데이터 자동 제거(기본적으로 활성화됨)
- 새로운 [미디어](https://developer.android.com/training/data-storage/shared/media) API를 사용하므로 [저장소 권한](https://developer.android.com/training/data-storage)이 필요하지 않음
- 소리를 녹음하려는 경우가 아니라면 마이크 권한이 필요하지 않음

<div class="admonition note" markdown>
<p class="admonition-title">참고</p>

현재 동영상 파일의 메타데이터는 삭제되지 않지만, 향후 지원될 예정입니다.

이미지 방향 메타데이터는 삭제되지 않습니다. (시큐어 카메라에서) 위치 정보를 활성화한 경우, 위치 정보도 삭제되지 **않습니다**. 나중에 이를 삭제하려면 [ExifEraser](../data-redaction.md#exiferaser-android) 같은 외부 앱을 사용해야 합니다.

</div>

## 시큐어 PDF 뷰어 { #secure-pdf-viewer }

<small>다음 위협으로부터 보호합니다:</small>

- [:material-target-account: 표적 공격](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }

<div class="admonition recommendation" markdown>

![시큐어 PDF 뷰어 로고](../assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![시큐어 PDF 뷰어 로고](../assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

**시큐어 PDF 뷰어**는 [pdf.js](https://en.wikipedia.org/wiki/PDF.js) 기반의 PDF 뷰어로, 어떠한 권한도 필요하지 않습니다. PDF는 [샌드박스](https://en.wikipedia.org/wiki/Sandbox_(software_development))가 적용된 [웹뷰](https://developer.android.com/guide/webapps/webview)에 로드됩니다. 따라서 콘텐츠나 파일에 접근하기 위한 권한을 직접 요구하지 않습니다.

[Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy)를 사용하여 웹뷰 내의 자바스크립트와 스타일 속성이 완전히 정적인 콘텐츠로만 구성되도록 강제합니다.

[:octicons-repo-16: 저장소](https://github.com/GrapheneOS/PdfViewer#readme){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: 깃허브](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: 그래핀OS 앱 스토어](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](../about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

- 이 페이지의 애플리케이션은 사이트 내 다른 소프트웨어 카테고리에 해당하지 않아야 합니다.
- 일반 애플리케이션은 핵심 시스템 기능을 확장하거나 대체해야 합니다.
- 애플리케이션은 정기적인 업데이트와 유지 관리가 이루어져야 합니다.
