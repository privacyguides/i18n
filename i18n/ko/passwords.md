---
meta_title: "프라이버시와 보안을 지켜 주는 최고의 비밀번호 관리자 - 프라이버시 가이드"
title: 비밀번호 관리자
icon: material/form-textbox-password
description: 비밀번호 관리자를 사용하면 비밀번호와 기타 자격 증명을 안전하게 저장하고 관리할 수 있습니다.
cover: passwords.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: 비밀번호 관리자 추천
    url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Bitwarden
    image: /assets/img/password-management/bitwarden.svg
    url: https://bitwarden.com
    sameAs: https://en.wikipedia.org/wiki/Bitwarden
    applicationCategory: Password Manager
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: 1Password
    image: /assets/img/password-management/1password.svg
    url: https://1password.com
    sameAs: https://en.wikipedia.org/wiki/1Password
    applicationCategory: Password Manager
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Proton Pass
    image: /assets/img/password-management/protonpass.svg
    url: https://proton.me/pass
    applicationCategory: Password Manager
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Psono
    image: /assets/img/password-management/psono.svg
    url: https://psono.com
    applicationCategory: Password Manager
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: KeePassXC
    image: /assets/img/password-management/keepassxc.svg
    url: https://keepassxc.org
    sameAs: https://en.wikipedia.org/wiki/KeePassXC
    applicationCategory: Password Manager
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: KeePassDX
    image: /assets/img/password-management/keepassdx.svg
    url: https://keepassdx.com
    applicationCategory: Password Manager
    operatingSystem: Android
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Gopass
    image: /assets/img/password-management/gopass.svg
    url: https://gopass.pw
    applicationCategory: Password Manager
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - FreeBSD
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-target-account: 표적 공격](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: 수동적 공격](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: 서비스 제공업체](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

**비밀번호 관리자**를 사용하면 마스터 비밀번호 하나로 비밀번호와 기타 자격 증명을 안전하게 저장하고 관리할 수 있습니다.

[비밀번호 소개 :material-arrow-right-drop-circle:](basics/passwords-overview.md)

<div class="admonition info" markdown>
<p class="admonition-title">정보</p>

브라우저나 운영 체제 같은 소프트웨어에 내장된 비밀번호 관리자는 전용 비밀번호 관리자 소프트웨어만큼 좋지 않은 경우가 있습니다. 내장 비밀번호 관리자는 소프트웨어와 잘 통합된다는 장점이 있지만, 기능이 매우 단순한 경우가 많고 독립형 제품이 갖춘 프라이버시 및 보안 기능이 부족할 수 있습니다.

예를 들어 마이크로소프트 엣지의 비밀번호 관리자는 종단 간 암호화를 전혀 제공하지 않습니다. 구글의 비밀번호 관리자는 E2EE를 [선택적으로](https://support.google.com/accounts/answer/11350823) 제공하며, [애플의 비밀번호 관리자](https://support.apple.com/HT202303)는 기본적으로 E2EE를 제공합니다.

</div>

## 클라우드 기반 { #cloud-based }

이 비밀번호 관리자는 비밀번호를 클라우드 서버에 동기화하므로 모든 기기에서 쉽게 접근할 수 있고, 기기를 분실해도 안전합니다.

### 비트워든 { #bitwarden }

<div class="admonition recommendation" markdown>

![비트워든 로고](assets/img/password-management/bitwarden.svg){ align=right }

**비트워든**은 자유 오픈 소스 비밀번호 및 패스키 관리자입니다. 개인, 팀, 비즈니스 조직의 비밀번호 관리 문제를 해결하는 것을 목표로 합니다. 비트워든은 모든 로그인 정보와 비밀번호를 저장하면서 모든 기기 간에 편리하게 동기화할 수 있는, 가장 뛰어나고 안전한 솔루션 중 하나입니다.

[:octicons-home-16: 홈페이지](https://bitwarden.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://bitwarden.com/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://bitwarden.com/help){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/bitwarden){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=com.x8bit.bitwarden)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id1137397744)
- [:simple-github: 깃허브](https://github.com/bitwarden/android/releases)
- [:fontawesome-brands-windows: 윈도우](https://bitwarden.com/download)
- [:simple-apple: macOS](https://bitwarden.com/download)
- [:simple-linux: 리눅스](https://bitwarden.com/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/com.bitwarden.desktop)
- [:simple-firefoxbrowser: 파이어폭스](https://addons.mozilla.org/firefox/addon/bitwarden-password-manager)
- [:simple-googlechrome: 크롬](https://chrome.google.com/webstore/detail/nngceckbapebfimnlniiiahkandclblb)
- [:fontawesome-brands-edge: 엣지](https://microsoftedge.microsoft.com/addons/detail/jbkfoedolllekgbhcbcoahefnbanhhlh)
- [:simple-safari: 사파리](https://apps.apple.com/app/id1352778147)

</details>

</div>

비트워든은 기본적으로 키 유도 함수(KDF) 알고리즘으로 [PBKDF2](https://bitwarden.com/help/kdf-algorithms/#pbkdf2)를 사용합니다. 대안으로 더 안전한 [Argon2](https://bitwarden.com/help/kdf-algorithms/#argon2id)도 제공합니다. 웹 보관함에서 계정의 KDF 알고리즘을 변경할 수 있습니다:

- [x] **설정 → 보안 → 키 → KDF 알고리즘 → Argon2id** 선택

비트워든의 서버 측 코드는 [오픈 소스](https://github.com/bitwarden/server)이므로, 비트워든 클라우드를 사용하고 싶지 않다면 자신만의 비트워든 동기화 서버를 쉽게 호스팅할 수 있습니다.

### 프로톤 패스 { #proton-pass }

<div class="admonition recommendation" markdown>

![프로톤 패스 로고](assets/img/password-management/protonpass.svg){ align=right }

**프로톤 패스**는 [프로톤 메일](email.md#proton-mail)을 만든 팀인 프로톤이 개발한 오픈 소스 종단 간 암호화 비밀번호 관리자입니다. 로그인 자격 증명을 안전하게 저장하고, 고유한 이메일 별칭을 생성하며, 패스키를 지원하고 저장합니다.

[:octicons-home-16: 홈페이지](https://proton.me/pass){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/pass/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://proton.me/support/pass){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/protonpass){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=proton.android.pass)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id6443490629)
- [:fontawesome-brands-windows: 윈도우](https://proton.me/pass/download)
- [:simple-firefoxbrowser: 파이어폭스](https://addons.mozilla.org/firefox/addon/proton-pass)
- [:simple-googlechrome: 크롬](https://chromewebstore.google.com/detail/ghmbeldphafepmbegfdlkpapadhbakde)
- [:fontawesome-brands-edge: 엣지](https://microsoftedge.microsoft.com/addons/detail/gcllgfdnfnllodcaambdaknbipemelie)
- [:octicons-browser-16: 웹](https://pass.proton.me)

</details>

</div>

2022년 4월 심플로그인을 인수한 이후, 프로톤은 별칭을 10개(무료 요금제) 또는 무제한(유료 요금제)으로 만들 수 있는 "이메일 가리기(hide-my-email)" 기능을 제공하고 있습니다.

프로톤 패스 모바일 앱과 브라우저 확장 프로그램은 2023년 5월부터 6월까지 Cure53의 감사를 받았습니다. 이 보안 분석 회사는 다음과 같이 결론지었습니다:

> 프로톤 패스 앱과 구성 요소는 보안 측면에서 상당히 긍정적인 인상을 남깁니다.

모든 문제는 [보고서](https://res.cloudinary.com/dbulfrlrz/images/v1707561557/wp-pme/Cure53-proton-pass-20230717/Cure53-proton-pass-20230717.pdf) 발표 직후 해결 및 수정되었습니다.

### 1Password

<div class="admonition recommendation" markdown>

![1Password 로고](assets/img/password-management/1password.svg){ align=right }

**1Password**는 보안과 사용 편의성에 크게 중점을 둔 비밀번호 관리자로, 비밀번호, 패스키, 신용카드, 소프트웨어 라이선스 및 기타 민감한 정보를 안전한 디지털 보관함에 저장할 수 있습니다. 보관함은 [월 요금](https://1password.com/sign-up)을 내고 1Password 서버에 호스팅됩니다.

1Password는 정기적으로 [감사](https://support.1password.com/security-assessments)를 받으며, 뛰어난 고객 지원을 제공합니다. 1Password는 비공개 소스이지만, 제품의 보안은 [보안 백서](https://1passwordstatic.com/files/security/1password-white-paper.pdf)에 철저하게 문서화되어 있습니다.

[:octicons-home-16: 홈페이지](https://1password.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://1password.com/legal/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://support.1password.com){ .card-link title="문서" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=com.onepassword.android)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id1511601750)
- [:fontawesome-brands-windows: 윈도우](https://1password.com/downloads/windows)
- [:simple-apple: macOS](https://1password.com/downloads/mac)
- [:simple-linux: 리눅스](https://1password.com/downloads/linux)
- [:simple-firefoxbrowser: 파이어폭스](https://addons.mozilla.org/firefox/addon/1password-x-password-manager)
- [:simple-googlechrome: 크롬](https://chrome.google.com/webstore/detail/aeblfdkhhhdcdjpifhhbdiojplfjncoa)
- [:fontawesome-brands-edge: 엣지](https://microsoftedge.microsoft.com/addons/detail/dppgmdbiimibapkepcbdbmkaabgiofem)
- [:simple-safari: 사파리](https://apps.apple.com/app/id1569813296)
- [:octicons-browser-16: 웹](https://my.1password.com/signin)

</details>

</div>

지금까지 1Password는 macOS와 iOS 사용자에게 최고의 비밀번호 관리자 사용 경험을 제공해 왔으며, 이제는 모든 플랫폼에서 동등한 기능을 갖추었습니다. 1Password 클라이언트는 사용하기 쉽고 탐색이 편한 직관적인 UI와 고급 기능 등, 가족이나 기술에 익숙하지 않은 사람들을 위한 많은 기능을 갖추고 있습니다. 특히 1Password의 거의 모든 기능을 네이티브 모바일 또는 데스크톱 클라이언트에서 사용할 수 있습니다.

1Password 보관함은 마스터 비밀번호와 무작위로 생성된 34자리 보안 키, 두 가지로 보호되며 이를 사용해 서버에 저장된 데이터를 암호화합니다. 이 보안 키 덕분에 마스터 비밀번호와 관계없이 데이터가 높은 엔트로피로 보호되므로, 데이터에 보호 계층이 하나 더해집니다. 다른 많은 비밀번호 관리자 솔루션은 데이터 보호를 전적으로 마스터 비밀번호의 강도에 의존합니다.

### Psono

<div class="admonition recommendation" markdown>

![Psono 로고](assets/img/password-management/psono.svg){ align=right }

**Psono**는 팀용 비밀번호 관리에 중점을 둔 독일의 자유 오픈 소스 비밀번호 관리자입니다. Psono는 비밀번호, 파일, 북마크, 이메일의 안전한 공유를 지원합니다. 모든 비밀 정보는 마스터 비밀번호로 보호됩니다.

[:octicons-home-16: 홈페이지](https://psono.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://psono.com/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://doc.psono.com){ .card-link title="문서" }
[:octicons-code-16:](https://gitlab.com/psono){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=com.psono.psono)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id1545581224)
- [:simple-firefoxbrowser: 파이어폭스](https://addons.mozilla.org/firefox/addon/psono-pw-password-manager)
- [:simple-googlechrome: 크롬](https://chrome.google.com/webstore/detail/eljmjmgjkbmpmfljlmklcfineebidmlo)
- [:simple-docker: Docker Hub](https://hub.docker.com/r/psono/psono-client)

</details>

</div>

Psono는 제품에 대한 방대한 문서를 제공합니다. Psono의 웹 클라이언트는 자체 호스팅할 수 있으며, 전체 기능의 커뮤니티 에디션이나 추가 기능이 있는 엔터프라이즈 에디션을 선택할 수도 있습니다.

2024년 4월 Psono는 브라우저 확장 프로그램에 한해 [패스키 지원](https://psono.com/blog/psono-introduces-passkeys)을 추가했습니다.

### 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

#### 최소 요구 사항 { #minimum-requirements }

- 강력한 표준 기반/최신 E2EE를 사용해야 합니다.
- 암호화 및 보안 관행이 철저하게 문서화되어 있어야 합니다.
- 평판이 좋은 독립적인 제3자의 감사 결과가 공개되어 있어야 합니다.
- 필수적이지 않은 모든 원격 측정은 선택 사항이어야 합니다.
- 요금 청구에 필요한 것 이상의 PII를 수집해서는 안 됩니다.

#### 우대 사항 { #best-case }

우대 사항은 이 카테고리에서 완벽한 프로젝트라면 갖추었으면 하는 사항을 나타냅니다. 추천 항목에 이 기능 중 일부 또는 전부가 없을 수도 있지만, 이러한 기능을 갖춘 항목은 이 페이지에서 다른 항목보다 높은 순위에 오를 수 있습니다.

- 원격 측정은 옵트인(기본적으로 비활성화) 방식이거나 아예 수집하지 않는 것이 좋습니다.
- 오픈 소스이며 합리적인 수준으로 자체 호스팅할 수 있는 것이 좋습니다.

## 로컬 저장 { #local-storage }

다음 선택지를 사용하면 암호화된 비밀번호 데이터베이스를 로컬에서 관리할 수 있습니다.

### 키패스XC { #keepassxc }

<div class="admonition recommendation" markdown>

![키패스XC 로고](assets/img/password-management/keepassxc.svg){ align=right }

**키패스XC**는 키패스 패스워드 세이프의 네이티브 크로스 플랫폼 포트인 키패스X의 커뮤니티 포크로, 새로운 기능과 버그 수정으로 키패스X를 확장하고 개선하여 기능이 풍부한 최신 크로스 플랫폼 오픈 소스 비밀번호 관리자를 제공하는 것을 목표로 합니다.

[:octicons-home-16: 홈페이지](https://keepassxc.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://keepassxc.org/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://keepassxc.org/docs){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/keepassxreboot/keepassxc){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://keepassxc.org/donate){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: 윈도우](https://keepassxc.org/download/#windows)
- [:simple-apple: macOS](https://keepassxc.org/download/#mac)
- [:simple-linux: 리눅스](https://keepassxc.org/download/#linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.keepassxc.KeePassXC)
- [:simple-firefoxbrowser: 파이어폭스](https://addons.mozilla.org/firefox/addon/keepassxc-browser)
- [:simple-googlechrome: 크롬](https://chrome.google.com/webstore/detail/oboonakemofpalcgghocfoadofidjkkk)

</details>

</div>

키패스XC는 내보내기 데이터를 [CSV](https://en.wikipedia.org/wiki/Comma-separated_values) 파일로 저장합니다. 이 파일을 다른 비밀번호 관리자로 가져오면 데이터가 손실될 수 있습니다. 각 항목을 직접 확인해 볼 것을 권장합니다.

### 키패스DX(안드로이드) { #keepassdx-android }

<div class="admonition recommendation" markdown>

![키패스DX 로고](assets/img/password-management/keepassdx.svg){ align=right }

**키패스DX**는 안드로이드용 경량 비밀번호 관리자로, 키패스 형식의 단일 파일에 담긴 암호화된 데이터를 편집할 수 있으며 양식을 안전하게 자동 입력할 수 있습니다.

[:octicons-home-16: 홈페이지](https://keepassdx.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Kunzisoft/KeePassDX/wiki){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/Kunzisoft/KeePassDX){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://keepassdx.com/#donation){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.free)
- [:simple-github: 깃허브](https://github.com/Kunzisoft/KeePassDX/releases)

</details>

</div>

이 앱의 [프로 버전](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.pro)에서는 외형 관련 콘텐츠와 비표준 프로토콜 기능을 사용할 수 있으며, 무엇보다 개발을 지원하고 장려하는 데 도움이 됩니다.

### 키패시움(iOS 및 macOS) { #keepassium-ios-macos }

<div class="admonition recommendation" markdown>

![키패시움 로고](assets/img/password-management/keepassium.svg){ align=right }

키패시움은 키패시움 랩스가 만든 상용 오픈 소스 비밀번호 관리자로, 다른 키패스 애플리케이션과 호환됩니다. 자동 완성 지원, 패스키 관리, [대부분의 클라우드 스토리지 제공업체](https://support.keepassium.com/kb/sync)를 통한 자동 양방향 동기화 등을 제공합니다.

[:material-star-box: 키패시움에 대한 최신 리뷰를 읽어 보세요.](https://www.privacyguides.org/articles/2025/05/13/keepassium-review)

[:octicons-home-16: 홈페이지](https://keepassium.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://keepassium.com/privacy/app){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://support.keepassium.com){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/keepassium/KeePassium){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://keepassium.com/donate){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-appstore: 앱 스토어](https://apps.apple.com/us/app/id1435127111)

</details>

</div>

키패시움은 여러 데이터베이스 지원, 유비키 지원, 비밀번호 점검 도구 같은 추가 기능을 갖춘 [프리미엄 버전](https://keepassium.com/pricing)을 제공합니다.

키패시움의 iOS 앱은 2024년 10월 Cure53의 [감사](https://cure53.de/pentest-report_keepassium.pdf)를 받았으며, 감사에서 발견된 모든 [문제](https://keepassium.com/blog/2024/11/independent-security-audit-complete)가 이후 수정되었습니다.

### 고패스(CLI) { #gopass-cli }

<div class="admonition recommendation" markdown>

![고패스 로고](assets/img/password-management/gopass.svg){ align=right }

**고패스**는 Go로 작성된 명령줄용 미니멀 비밀번호 관리자입니다. 스크립트 애플리케이션 안에서 사용할 수 있으며, 모든 주요 데스크톱 및 서버 운영 체제에서 작동합니다.

[:octicons-home-16: 홈페이지](https://gopass.pw){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/gopasspw/gopass/tree/master/docs){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/gopasspw/gopass){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://github.com/sponsors/dominikschulz){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: 윈도우](https://gopass.pw/#install-windows)
- [:simple-apple: macOS](https://gopass.pw/#install-macos)
- [:simple-linux: 리눅스](https://gopass.pw/#install-linux)
- [:simple-freebsd: FreeBSD](https://gopass.pw/#install-bsd)

</details>

</div>

### 평가 기준 { #criteria_1 }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

- 크로스 플랫폼을 지원해야 합니다.
