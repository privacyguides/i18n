---
meta_title: "최고의 프라이버시 보호 및 보안 클라우드 스토리지 제공업체 - 프라이버시 가이드"
title: 클라우드 스토리지
icon: material/file-cloud
description: 많은 클라우드 스토리지 제공업체는 여러분의 파일을 들여다보지 않을 것이라는 신뢰를 요구합니다. 다음은 프라이버시를 보호하는 대안입니다!
cover: cloud.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-bug-outline: 수동적 공격](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: 서비스 제공업체](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

많은 **클라우드 스토리지 제공업체**는 여러분의 파일을 들여다보지 않을 것이라는 전적인 신뢰를 요구합니다. 아래 대안은 안전한 종단 간 암호화를 구현하여 신뢰할 필요 자체를 없앱니다.

이러한 대안이 요구에 맞지 않는다면, 다른 클라우드 제공업체와 함께 [크립토메이터](encryption.md#cryptomator-cloud) 같은 암호화 소프트웨어를 사용하는 것을 고려해 보세요. (이 목록의 제공업체를 포함해) **어떤** 클라우드 제공업체든 크립토메이터를 함께 사용하면 제공업체 네이티브 클라이언트의 암호화 결함 위험을 줄일 수 있습니다.

<details class="admonition info" markdown>
<summary>넥스트클라우드를 찾고 계신가요?</summary>

기술적인 지식이 있는 독자라면 넥스트클라우드는 파일 관리 제품군을 자체 호스팅하는 용도로 [여전히 추천하는 도구](self-hosting/file-management.md#nextcloud)입니다. 하지만 일반 가정 사용자에게는 넥스트클라우드의 내장 E2EE 기능을 [권장하지 않기](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) 때문에, 현재 제3자 넥스트클라우드 스토리지 제공업체는 추천하지 않습니다.

</details>

## 프로톤 드라이브 { #proton-drive }

<div class="admonition recommendation" markdown>

![프로톤 드라이브 로고](assets/img/cloud/protondrive.svg){ align=right }

**프로톤 드라이브**는 인기 있는 암호화 이메일 제공업체인 [프로톤 메일](email.md#proton-mail)이 제공하는 암호화 클라우드 스토리지 서비스입니다.

처음 제공되는 무료 저장 공간은 2GB이지만, [특정 단계](https://proton.me/support/more-free-storage-existing-users)를 완료하면 최대 5GB까지 추가 저장 공간을 받을 수 있습니다.

[:octicons-home-16: 홈페이지](https://proton.me/drive){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/drive/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id1509667851)
- [:fontawesome-brands-windows: 윈도우](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

프로톤 드라이브 웹 애플리케이션은 [2021년](https://proton.me/community/open-source)에 시큐리텀의 독립적인 감사를 받았지만, 새로 출시된 모바일 클라이언트는 아직 제3자의 공개 감사를 받지 않았습니다.

## 트레소릿 { #tresorit }

<div class="admonition recommendation" markdown>

![트레소릿 로고](assets/img/cloud/tresorit.svg){ align=right }

**트레소릿**은 2011년에 설립된 스위스-헝가리 암호화 클라우드 스토리지 제공업체입니다. 트레소릿은 스위스 국영 우편 서비스인 스위스 포스트가 소유하고 있습니다.

[:octicons-home-16: 홈페이지](https://tresorit.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tresorit.com/legal/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://support.tresorit.com){ .card-link title="문서" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=com.tresorit.mobile)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id722163232)
- [:fontawesome-brands-windows: 윈도우](https://tresorit.com/download)
- [:simple-apple: macOS](https://tresorit.com/download)
- [:simple-linux: 리눅스](https://tresorit.com/download)

</details>

</div>

트레소릿은 여러 차례 독립적인 보안 감사를 받았습니다:

- [2022년](https://tresorit.com/blog/tresorit-receives-iso-27001-certification): TÜV Rheinland InterCert Kft의 ISO/IEC 27001:2013[^1] 준수 [인증](https://certipedia.com/quality_marks/9108644476)
- [2021년](https://tresorit.com/blog/fresh-penetration-testing-confirms-tresorit-security): 컴퓨테스트의 침투 테스트
    - 이 검토에서는 트레소릿 웹 클라이언트, 안드로이드 앱, 윈도우 앱 및 관련 인프라의 보안을 평가했습니다.
    - 컴퓨테스트는 취약점 두 개를 발견했으며, 이 취약점은 해결되었습니다.
- [2019년](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): 언스트앤영의 침투 테스트.
    - 이 검토에서는 트레소릿의 전체 소스 코드를 분석하여, 구현이 트레소릿 [백서](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf)에서 설명한 개념과 일치하는지 검증했습니다.
    - 언스트앤영은 웹, 모바일, 데스크톱 클라이언트도 추가로 테스트했습니다. 그 결론은 다음과 같습니다:

        > 테스트 결과, 트레소릿의 데이터 기밀성 주장에서 벗어나는 사항은 발견되지 않았습니다.

## 피어고스 { #peergos }

<div class="admonition recommendation" markdown>

![피어고스 로고](assets/img/cloud/peergos.svg){ align=right }

**피어고스**는 저장소, 소셜 미디어, 애플리케이션을 위한 탈중앙화 프로토콜이자 오픈 소스 플랫폼입니다. 사용자가 사진, 동영상, 문서 등을 저장, 공유, 열람, 편집할 수 있는 안전하고 사적인 공간을 제공합니다.

피어고스는 양자 내성 E2EE로 파일을 보호하며, 파일에 관한 모든 데이터를 비공개로 유지합니다. [자체 호스팅](https://book.peergos.org/features/self)도 가능합니다.

[:octicons-home-16: 홈페이지](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://book.peergos.org){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://github.com/peergos/peergos#support){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=peergos.android)
- [:simple-github: 깃허브](https://github.com/Peergos/web-ui/releases)
- [:fontawesome-brands-windows: 윈도우](https://peergos.org/download#windows)
- [:simple-apple: macOS](https://peergos.org/download#macos)
- [:simple-linux: 리눅스](https://peergos.org/download#linux)
- [:octicons-browser-16: 웹](https://peergos.net)

</details>

</div>

피어고스는 [:material-close-outline: 검열](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}을 방지하는 P2P 아키텍처인 [행성 간 파일 시스템(IPFS)](https://ipfs.tech)을 기반으로 구축되었습니다.

피어고스의 클라이언트, 서버, 명령줄 인터페이스는 모두 같은 바이너리에서 실행됩니다. 또한 피어고스에는 로컬 폴더와 피어고스 폴더를 양방향으로 동기화하는 (네이티브 앱에서 사용 가능한) [동기화 엔진](https://book.peergos.org/features/sync)과, 다른 애플리케이션이 피어고스 저장소에 접근할 수 있게 해 주는 [WebDAV 브리지](https://book.peergos.org/features/webdav)가 포함되어 있습니다. 피어고스의 다양한 기능에 대한 전체 개요는 피어고스 문서를 참고하세요.

피어고스는 2024년 11월 래디컬리 오픈 시큐리티의 [감사](https://peergos.org/posts/security-audit-2024)를 받았으며, 발견된 모든 문제가 수정되었습니다. 이전에는 2019년 6월 Cure53의 [감사](https://cure53.de/pentest-report_peergos.pdf)를 받았으며, 발견된 모든 문제가 이후 수정되었습니다.

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

### 최소 요구 사항 { #minimum-requirements }

- E2EE를 강제해야 합니다.
- 테스트를 위한 무료 요금제나 체험 기간을 제공해야 합니다.
- TOTP 또는 FIDO2 다중 인증이나 패스키 로그인을 지원해야 합니다.
- 기본적인 파일 관리 기능을 지원하는 웹 인터페이스를 제공해야 합니다.
- 모든 파일/문서를 쉽게 내보낼 수 있어야 합니다.

### 우대 사항 { #best-case }

우대 사항은 이 카테고리에서 완벽한 프로젝트라면 갖추었으면 하는 사항을 나타냅니다. 추천 항목에 이 기능 중 일부 또는 전부가 없을 수도 있지만, 이러한 기능을 갖춘 항목은 이 페이지에서 다른 항목보다 높은 순위에 오를 수 있습니다.

- 클라이언트는 오픈 소스인 것이 좋습니다.
- 클라이언트 전체가 독립적인 제3자의 감사를 받는 것이 좋습니다.
- 리눅스, 안드로이드, 윈도우, macOS, iOS용 네이티브 클라이언트를 제공하는 것이 좋습니다.
    - 이러한 클라이언트는 iOS의 파일 앱 연동이나 안드로이드의 DocumentsProvider 기능처럼 클라우드 스토리지 제공업체를 위한 OS 기본 도구와 통합되는 것이 좋습니다.
- 다른 사용자와 파일을 쉽게 공유할 수 있는 것이 좋습니다.
- 웹 인터페이스에서 최소한 기본적인 파일 미리 보기 및 편집 기능을 제공하는 것이 좋습니다.

[^1]: [ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001):2013 준수는 회사의 [정보 보안 관리 시스템](https://en.wikipedia.org/wiki/Information_security_management)과 관련된 것으로, 클라우드 서비스의 판매, 개발, 유지 관리 및 지원을 다룹니다.
