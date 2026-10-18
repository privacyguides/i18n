---
title: 사진 관리
icon: material/image
description: 이 사진 관리 도구는 클라우드 스토리지 제공업체와 기타 권한 없는 사람들의 엿보는 눈으로부터 개인 사진을 안전하게 지켜 줍니다.
cover: photo-management.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-bug-outline: 수동적 공격](basics/common-threats.md#security-and-privacy){ .pg-orange }
- [:material-server-network: 서비스 제공업체](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

구글 포토, 플리커, 아마존 포토 같은 대부분의 클라우드 **사진 관리 솔루션**은 클라우드 스토리지 제공업체 자체가 사진에 접근하는 것을 막지 못합니다. 다음 선택지는 가족이나 신뢰하는 사람들과만 사진을 공유할 수 있도록 하면서 개인 사진을 비공개로 유지해 줍니다.

## 엔테 포토 { #ente-photos }

<div class="admonition recommendation" markdown>

![엔테 로고](assets/img/photo-management/ente.svg){ align=right }

**엔테 포토**는 iOS와 안드로이드에서 자동 백업을 지원하는 종단 간 암호화 사진 백업 서비스입니다. 클라이언트와 서버 모두 코드가 완전히 오픈 소스입니다. [자체 호스팅](https://github.com/ente-io/ente/tree/main/server#self-hosting)도 가능합니다.

무료 요금제는 1년에 한 번 이상 서비스를 사용하는 한 10GB의 저장 공간을 제공합니다.

[:octicons-home-16: 홈페이지](https://ente.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.com/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://ente.com/faq){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/ente-io/ente){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=io.ente.photos)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id1542026904)
- [:simple-github: 깃허브](https://github.com/ente-io/ente/releases?q=photos)
- [:simple-android: 안드로이드](https://ente.com/download)
- [:fontawesome-brands-windows: 윈도우](https://ente.com/download)
- [:simple-apple: macOS](https://ente.com/download)
- [:simple-linux: 리눅스](https://ente.com/download)
- [:octicons-browser-16: 웹](https://web.ente.io)

</details>

</div>

엔테 포토의 기반이 되는 서버 측 소스 코드와 인프라는 2025년 10월 [Cure53](https://ente.com/blog/cern-audit)의 감사를 받았습니다. 이전에는 2023년 3월 [Cure53](https://ente.com/blog/cryptography-audit), 2023년 4월 [폴리블](https://ente.com/reports/Fallible-Audit-Report-19-04-2023.pdf)의 감사를 받았습니다.

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

### 최소 요구 사항 { #minimum-requirements }

- 클라우드 호스팅 제공업체는 E2EE를 강제해야 합니다.
- 테스트를 위한 무료 요금제나 체험 기간을 제공해야 합니다.
- TOTP 또는 FIDO2 다중 인증이나 패스키 로그인을 지원해야 합니다.
- 기본적인 파일 관리 기능을 지원하는 웹 인터페이스를 제공해야 합니다.
- 모든 파일/문서를 쉽게 내보낼 수 있어야 합니다.
- 오픈 소스여야 합니다.

### 우대 사항 { #best-case }

- 평판이 좋은 독립적인 제3자의 감사 결과가 공개되어 있는 것이 좋습니다.
