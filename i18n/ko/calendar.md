---
title: 캘린더 동기화
icon: material/calendar
description: 캘린더에는 매우 민감한 데이터가 담겨 있으므로, 저장 데이터 암호화를 구현한 제품을 사용하세요.
cover: calendar.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-bug-outline: 수동적 공격](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: 서비스 제공업체](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

**캘린더**에는 매우 민감한 데이터가 담겨 있으므로, 제공업체가 데이터를 읽지 못하도록 저장 데이터에 종단 간 암호화를 적용한 제품을 사용하세요.

## 투타 { #tuta }

<div class="admonition recommendation" markdown>

![투타 로고](assets/img/email/tuta.svg#only-light){ align=right }
![투타 로고](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**투타**는 지원하는 모든 플랫폼에서 무료 암호화 캘린더를 제공합니다. 모든 데이터에 대한 자동 E2EE, 공유 기능, 가져오기/내보내기 기능, 다중 인증 등 [다양한 기능](https://tuta.com/calendar-app-comparison)을 제공합니다.

여러 캘린더와 확장된 공유 기능은 유료 구독자만 사용할 수 있습니다.

[:octicons-home-16: 홈페이지](https://tuta.com/calendar){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://tuta.com/community#donate){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=de.tutao.calendar)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id6657977811)
- [:simple-github: 깃허브](https://github.com/tutao/tutanota/releases?q=Calendar)
- [:fontawesome-brands-windows: 윈도우](https://tuta.com/blog/desktop-clients)
- [:simple-apple: macOS](https://tuta.com/blog/desktop-clients)
- [:simple-linux: 리눅스](https://tuta.com/blog/desktop-clients)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.tutanota.Tutanota)
- [:octicons-browser-16: 웹](https://app.tuta.com)

</details>

</div>

## 프로톤 캘린더 { #proton-calendar }

<div class="admonition recommendation" markdown>

![프로톤](assets/img/calendar/proton-calendar.svg){ align=right }

**프로톤 캘린더**는 웹 또는 모바일 클라이언트를 통해 프로톤 회원이 이용할 수 있는 암호화 캘린더 서비스입니다. 모든 데이터에 대한 자동 E2EE, 공유 기능, 가져오기/내보내기 기능 등 [다양한 기능](https://proton.me/support/proton-calendar-guide)을 제공합니다.

무료 요금제 사용자는 캘린더를 3개까지 사용할 수 있고, 유료 구독자는 최대 25개까지 만들 수 있습니다. 확장된 공유 기능도 유료 구독자만 사용할 수 있습니다.

[:octicons-home-16: 홈페이지](https://proton.me/calendar){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/calendar/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://proton.me/support/calendar){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/orgs/ProtonMail/repositories?q=calendar){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=me.proton.android.calendar)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id1514709943)
- [:octicons-browser-16: 웹](https://calendar.proton.me)

</details>

</div>

2021년 시큐리텀은 프로톤 캘린더의 웹 클라이언트를 [감사](https://proton.me/community/open-source#:~:text=Proton%20Calendar)했으며, 안드로이드 앱에 대해서는 [증명서](https://res.cloudinary.com/dbulfrlrz/images/v1714639870/wp-pme/letter-of-attestation-proton-calendar-20211109_3138998f9b/letter-of-attestation-proton-calendar-20211109_3138998f9b.pdf)를 제공했습니다.

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

### 최소 요구 사항 { #minimum-qualifications }

- 서비스 제공업체가 데이터를 볼 수 없도록 E2EE로 정보를 동기화하고 저장해야 합니다.

### 우대 사항 { #best-case }

우대 사항은 이 카테고리에서 완벽한 프로젝트라면 갖추었으면 하는 사항을 나타냅니다. 추천 항목에 이 기능 중 일부 또는 전부가 없을 수도 있지만, 이러한 기능을 갖춘 항목은 이 페이지에서 다른 항목보다 높은 순위에 오를 수 있습니다.

- 해당되는 경우 OS 기본 캘린더 및 연락처 관리 앱과 연동되는 것이 좋습니다.
