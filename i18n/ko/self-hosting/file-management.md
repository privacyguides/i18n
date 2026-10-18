---
title: 파일 관리
meta_title: "자체 호스팅 파일 관리 도구 - 프라이버시 가이드"
icon: material/file-multiple-outline
description: 기술적인 지식이 있는 독자라면 파일 관리 도구를 자체 호스팅하여 데이터를 최대한 통제함으로써 프라이버시를 추가로 보장받을 수 있습니다.
cover: cloud.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-server-network: 서비스 제공업체](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

**파일 관리** 도구를 직접 자체 호스팅하면 클라우드 제공업체 네이티브 클라이언트의 암호화 결함 위험을 줄일 수 있습니다.

## 사진 관리 { #photo-management }

### 포토프리즘 { #photoprism }

<div class="admonition recommendation" markdown>

![포토프리즘 로고](../assets/img/self-hosting/photoprism.svg){ align=right }

**포토프리즘**은 사진을 관리하는 플랫폼입니다. 앨범 동기화 및 공유는 물론 다양한 [기능](https://photoprism.app/features)을 지원합니다. 종단 간 암호화를 지원하지 않으므로, 신뢰할 수 있고 직접 관리하는 서버에서 호스팅하는 것이 가장 좋습니다.

[:octicons-home-16: 홈페이지](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="소스 코드" }

</div>

## 파일 공유 및 동기화 { #file-sharing-and-sync }

### 프리덤박스 { #freedombox }

<div class="admonition recommendation" markdown>

![프리덤박스 로고](../assets/img/self-hosting/freedombox.svg){ align=right }

**프리덤박스**는 [싱글 보드 컴퓨터(SBC)](https://en.wikipedia.org/wiki/Single-board_computer)에서 실행되도록 설계된 운영 체제입니다. 파일 공유 같은 용도의 서버 애플리케이션을 쉽게 설정할 수 있도록 하는 것이 목적입니다.

[:octicons-home-16: 홈페이지](https://freedombox.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title="문서" }
[:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://freedomboxfoundation.org/donate){ .card-link title="후원하기" }

</div>

### 넥스트클라우드 { #nextcloud }

<div class="admonition recommendation" markdown>

![넥스트클라우드 로고](../assets/img/self-hosting/nextcloud.svg){ align=right }

**넥스트클라우드**는 직접 관리하는 개인 서버에 자신만의 파일 호스팅 서비스를 만들 수 있는 자유 오픈 소스 클라이언트-서버 소프트웨어 모음입니다.

[:octicons-home-16: 홈페이지](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title="후원하기" }

<details class="downloads" markdown><summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=com.nextcloud.client)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id1125420102)
- [:simple-github: 깃허브](https://github.com/nextcloud/android/releases)
- [:fontawesome-brands-windows: 윈도우](https://nextcloud.com/install/#install-clients)
- [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
- [:simple-linux: 리눅스](https://nextcloud.com/install/#install-clients)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">위험</p>

넥스트클라우드용 [E2EE 앱](https://apps.nextcloud.com/apps/end_to_end_encryption)은 데이터 손실을 일으킬 수 있으므로 사용을 권장하지 않습니다. 이 앱은 매우 실험적이며 실사용할 수준의 품질이 아닙니다. 이러한 이유로 제3자 넥스트클라우드 제공업체는 권장하지 않습니다.

</div>
