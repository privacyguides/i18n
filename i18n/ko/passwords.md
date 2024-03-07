---
meta_title: "The Best Password Managers to Protect Your Privacy and Security - Privacy Guides"
title: "비밀번호 관리자"
icon: material/form-textbox-password
description: Password managers allow you to securely store and manage passwords and other credentials.
cover: passwords.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Password Manager Recommendations
    url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Bitwarden
    image: /assets/img/password-management/bitwarden.svg
    url: https://bitwarden.com
    sameAs: https://en.wikipedia.org/wiki/Bitwarden
    applicationCategory: 비밀번호 관리자
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
    applicationCategory: 비밀번호 관리자
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
    name: Psono
    image: /assets/img/password-management/psono.svg
    url: https://psono.com
    applicationCategory: 비밀번호 관리자
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
    url: https://keepassxc.org/
    sameAs: https://en.wikipedia.org/wiki/KeePassXC
    applicationCategory: 비밀번호 관리자
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
    url: https://www.keepassdx.com/
    applicationCategory: 비밀번호 관리자
    operatingSystem: Android
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Strongbox
    image: /assets/img/password-management/strongbox.svg
    url: https://strongboxsafe.com/
    applicationCategory: 비밀번호 관리자
    operatingSystem: iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: gopass
    image: /assets/img/password-management/gopass.svg
    url: https://www.gopass.pw/
    applicationCategory: 비밀번호 관리자
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

비밀번호 관리자를 사용하여, 비밀번호를 비롯한 기타 자격 증명을 마스터 비밀번호로 안전하게 저장 및 관리할 수 있습니다.

[비밀번호 입문 :material-arrow-right-drop-circle:](./basics/passwords-overview.md)

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

브라우저나 운영 체제 등에 내장된 비밀번호 관리자는 전용 비밀번호 관리자 소프트웨어에 비해 부족한 경우가 있습니다. 내장된 비밀번호 관리자는 본체 소프트웨어와 잘 통합되어 있다는 장점이 있지만, 기능이 매우 단조롭고 프라이버시 및 보안 기능이 부족한 경우가 많습니다.

예를 들어, Microsoft Edge 내의 비밀번호 관리자는 E2EE를 전혀 제공하지 않습니다. Google 비밀번호 관리자는 [선택적](https://support.google.com/accounts/answer/11350823) E2EE를 제공하며, Apple은 [기본적으로](https://support.apple.com/ko-kr/HT202303) E2EE를 제공합니다.

</div>

## 클라우드 기반

클라우드 기반 비밀번호 관리자는 여러분의 비밀번호를 클라우드 서버에 동기화하므로, 여러분이 가진 모든 기기에서 간편하게 접근할 수 있고 기기를 분실하더라도 데이터 손실 위험이 없습니다.

### Bitwarden

<div class="admonition recommendation" markdown>

![Bitwarden 로고](assets/img/password-management/bitwarden.svg){ align=right }

**Bitwarden**은 무료 오픈 소스 비밀번호 관리자입니다. 개인, 팀, 비즈니스 조직의 비밀번호 관리 문제를 해결하는 것을 목표로 합니다. Bitwarden은 모든 로그인 및 비밀번호를 저장하는 동시에 간편하게 모든 기기 간 동기화가 가능한, 가장 안전하고 뛰어난 서비스로 꼽히는 솔루션입니다.

[:octicons-home-16: Homepage](https://bitwarden.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://bitwarden.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://bitwarden.com/help/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/bitwarden){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.x8bit.bitwarden)
- [:simple-appstore: App Store](https://apps.apple.com/app/bitwarden-password-manager/id1137397744)
- [:simple-github: GitHub](https://github.com/bitwarden/mobile/releases)
- [:simple-windows11: Windows](https://bitwarden.com/download)
- [:simple-linux: Linux](https://bitwarden.com/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/com.bitwarden.desktop)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/bitwarden-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/bitwarden-free-password-m/nngceckbapebfimnlniiiahkandclblb)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/jbkfoedolllekgbhcbcoahefnbanhhlh)

</details>

</div>

Bitwarden은 [종단 간 암호화를 적용해](https://bitwarden.com/help/send-encryption) 텍스트 및 파일을 안전하게 공유할 수 있는 [Bitwarden Send](https://bitwarden.com/products/send/) 기능도 제공합니다. Send 링크에 [비밀번호를 설정](https://bitwarden.com/help/send-privacy/#send-passwords)할 수도 있습니다. [자동 삭제](https://bitwarden.com/help/send-lifespan) 기능 또한 지원합니다.

파일 공유 기능은 [프리미엄 요금제](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans)에만 제공됩니다. 무료 플랜은 텍스트 공유만 가능합니다.

Bitwarden's server-side code is [open source](https://github.com/bitwarden/server), so if you don't want to use the Bitwarden cloud, you can easily host your own Bitwarden sync server.

**Vaultwarden**은 Bitwarden 동기화 서버를 Rust 언어로 구현한 것으로, Bitwarden 공식 클라이언트와 호환됩니다. 공식 서비스에 비해 리소스 사용량이 적으므로 자체 호스팅 용도로 적합합니다. Vaultwarden은 개인 서버에서 Bitwarden을 자체 호스팅하는 경우 공식 Bitwarden 서버 코드보다 선호됩니다.

[:octicons-repo-16: Vaultwarden 저장소](https://github.com/dani-garcia/vaultwarden ""){.md-button} [:octicons-info-16:](https://github.com/dani-garcia/vaultwarden/wiki){ .card-link title=문서}
[:octicons-code-16:](https://github.com/dani-garcia/vaultwarden){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://github.com/sponsors/dani-garcia){ .card-link title=기부 }

### 1Password

<div class="admonition recommendation" markdown>

![1Password 로고](assets/img/password-management/1password.svg){ align=right }

**1Password**는 보안과 사용 편의성에 중점을 둔 비밀번호 관리자입니다. 비밀번호, 카드, 소프트웨어 라이선스를 비롯한 민감한 정보를 안전한 디지털 보관함에 저장 가능합니다. 보관함은 [월 사용료](https://1password.com/sign-up/)를 지불하여 1Password 서버에서 호스팅됩니다. 1Password는 정기적으로 [보안 감사](https://support.1password.com/security-assessments/)를 받고 있으며, 우수한 고객 지원을 제공합니다. 1Password는 오픈 소스가 아니지만, 제품의 보안은 [보안 백서](https://1passwordstatic.com/files/security/1password-white-paper.pdf)에 철저하게 문서화되어 있습니다.

[:octicons-home-16: Homepage](https://1password.com/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://1password.com/legal/privacy/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.1password.com/){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onepassword.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1511601750?mt=8)
- [:simple-windows11: Windows](https://1password.com/downloads/windows/)
- [:simple-apple: macOS](https://1password.com/downloads/mac/)
- [:simple-linux: Linux](https://1password.com/downloads/linux/)

</details>

</div>

**1Passsword**는 이전부터 macOS 및 iOS 사용자에게 가장 뛰어난 비밀번호 관리자 사용 경험을 제공해왔습니다. 오늘날에는 모든 플랫폼에서 동일한 기능성을 제공합니다. 고급 기능뿐만 아니라, 기술 이해도가 낮은 사용자 및 가족을 위한 다양한 기능을 자랑합니다.

1Password 보관함은 마스터 비밀번호와 무작위 생성 34자 보안 키로 보호되어 여러분의 데이터를 서버에서 암호화합니다. 이 보안 키의 존재로 인해, 여러분은 마스터 비밀번호 강도에 관계없이 여러분의 데이터를 높은 엔트로피로 보호할 수 있습니다. 대부분의 다른 비밀번호 관리자는 사용자 데이터 보호를 사용자의 마스터 비밀번호 강도에만 전적으로 의존합니다.

Bitwarden 대비 1Password 장점 중 하나는 네이티브 클라이언트 지원이 매우 뛰어나다는 점입니다. Bitwarden은 상당수의 기능을(특히 계정 관리 기능) 웹 보관함 인터페이스에서만 제공합니다. 반면, 1Password는 거의 모든 기능을 모바일/데스크톱 네이티브 클라이언트에서 이용할 수 있습니다. 또한 1Password 클라이언트는 보다 직관적인 UI를 제공하여 더욱 쉬운 사용 및 탐색이 가능합니다.

### Psono

<div class="admonition recommendation" markdown>

![Psono 로고](assets/img/password-management/psono.svg){ align=right }

**Psono**는 팀 비밀번호 관리 서비스에 중점을 둔 독일의 무료 오픈 소스 비밀번호 관리자입니다. Psono는 비밀번호, 파일, 북마크, 이메일의 안전한 공유를 지원합니다. 모든 비밀 정보는 마스터 비밀번호로 보호됩니다.

[:octicons-home-16: Homepage](https://psono.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://psono.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://doc.psono.com){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.com/psono){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.psono.psono)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/psono-password-manager/id1545581224)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/psono-pw-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/psonopw-password-manager/eljmjmgjkbmpmfljlmklcfineebidmlo)
- [:simple-docker: Docker Hub](https://hub.docker.com/r/psono/psono-client)

</details>

</div>

Psono는 제품에 관련된 문서를 매우 폭넓게 제공합니다. Psono 웹 클라이언트는 자체 호스팅 가능합니다. Community Edition 혹은 추가 기능이 포함된 Enterprise Edition을 선택할 수 있습니다.

### 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

</div>

#### 최소 요구 사항

- 강력한 표준 기반/최신 E2EE를 활용해야 합니다.
- 암호화 및 보안 사례를 철저히 문서화해야 합니다.
- 평한이 좋은 독립적인 제3자로부터 공개 감사를 받아야 합니다.
- 필수적이지 않은 원격 분석 데이터 수집은 모두 선택 사항이어야 합니다.
- 요금 청구 용도로 필요한 것 이상으로 PII를 수집해서는 안 됩니다.

#### 우대 사항

평가 기준에서 '우대 사항'은 해당 부문에서 완벽한 프로젝트에 기대하는 바를 나타냅니다. 다음의 우대 사항에 해당하지 않더라도 권장 목록에 포함될 수 있습니다. 단, 우대 사항에 해당할수록 이 페이지의 다른 항목보다 높은 순위를 갖습니다.

- 원격 분석 데이터 수집 기능은 아예 존재하지 않거나, 기본적으로 비활성화되어 있어야 합니다.
- Should be open source and reasonably self-hostable.

## 로컬 저장

로컬 저장 비밀번호 관리자는 암호화된 비밀번호 데이터베이스를 로컬에서 관리합니다.

### KeePassXC

<div class="admonition recommendation" markdown>

![KeePassXC 로고](assets/img/password-management/keepassxc.svg){ align=right }

**KeePassXC**는 KeePassX(KeePass Password Safe를 네이티브 크로스 플랫폼으로 포팅한 프로젝트)를 커뮤니티에서 포크한 프로젝트입니다. 새로운 기능 추가와 버그 수정을 통해 확장 및 개선하여, 풍부한 기능을 갖추고 크로스 플랫폼을 지원하는 최신 오픈 소스 비밀번호 관리자를 제공하는 것이 목표입니다.

[:octicons-home-16: Homepage](https://keepassxc.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://keepassxc.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://keepassxc.org/docs/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/keepassxreboot/keepassxc){ .card-link title="Source Code" }
[:octicons-heart-16:](https://keepassxc.org/donate/){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://keepassxc.org/download/#windows)
- [:simple-apple: macOS](https://keepassxc.org/download/#mac)
- [:simple-linux: Linux](https://keepassxc.org/download/#linux)
- [:simple-flathub: Flatpak](https://flathub.org/apps/details/org.keepassxc.KeePassXC)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/keepassxc-browser)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/keepassxc-browser/oboonakemofpalcgghocfoadofidjkkk)

</details>

</div>

KeePassXC는 데이터 내보내기 시 [CSV](https://en.wikipedia.org/wiki/Comma-separated_values) 파일로 저장합니다. 즉, 해당 파일을 다른 비밀번호 관리자로 불러올 경우 데이터 손실이 발생할 수 있습니다. 각 데이터 항목을 수동으로 확인해보는 것이 좋습니다.

### KeePassDX (Android)

<div class="admonition recommendation" markdown>

![KeePassDX 로고](assets/img/password-management/keepassdx.svg){ align=right }

**KeePassDX**는 Android용 가벼운 비밀번호 관리자입니다. 암호화된 데이터를 KeePass 형식 단일 파일로 편집할 수 있으며, 안전한 방식으로 입력 항목을 채울 수 있습니다. [Contributor Pro](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.pro)를 결제하면 프로젝트 개발에 큰 도움을 주는 동시에, 추가 디자인 테마 및 비표준 프로토콜 기능을 사용할 수 있습니다.

[:octicons-home-16: Homepage](https://www.keepassdx.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Kunzisoft/KeePassDX/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/Kunzisoft/KeePassDX){ .card-link title="Source Code" }
[:octicons-heart-16:](https://www.keepassdx.com/#donation){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.free)
- [:simple-github: GitHub](https://github.com/Kunzisoft/KeePassDX/releases)

</details>

</div>

### Strongbox (iOS & macOS)

<div class="admonition recommendation" markdown>

![Strongbox 로고](assets/img/password-management/strongbox.svg){ align=right }

**Strongbox**는 iOS, macOS용 네이티브 오픈 소스 비밀번호 관리자입니다. KeePass, Password Safe 형식을 지원하므로, Apple 외 플랫폼에서는 KeePassXC 등의 다른 비밀번호 관리자와 함께 사용할 수 있습니다. Strongbox는 [부분 유료화](https://strongboxsafe.com/pricing/) 모델을 채택하고 있습니다. 무료 플랜에서도 대부분의 기능을 제공하나, 생체 인증 등 [편의 기능](https://strongboxsafe.com/comparison/)은 구독/영구 플랜에만 제공됩니다.

[:octicons-home-16: Homepage](https://strongboxsafe.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://strongboxsafe.com/privacy/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://strongboxsafe.com/getting-started/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/strongbox-password-safe/Strongbox){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/strongbox-password-safe/Strongbox#supporting-development){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/strongbox-keepass-pwsafe/id897283731)

</details>

</div>

[Strongbox Zero](https://apps.apple.com/app/strongbox-keepass-pwsafe/id1581589638)라는 오프라인 전용 버전 또한 제공됩니다. 해당 버전은 공격 표면을 최소화하기 위해 만들어졌습니다.

### 커맨드라인

커맨드라인 비밀번호 관리자는 스크립트 애플리케이션 내에서 사용할 수 있는 미니멀한 비밀번호 관리자입니다.

#### gopass

<div class="admonition recommendation" markdown>

![gopass 로고](assets/img/password-management/gopass.svg){ align=right }

**gopass**는 Go 언어로 작성된 커맨드라인용 비밀번호 관리자입니다. 모든 주요 데스크톱 및 서버 운영 체제(Linux, macOS, BSD, Windows)에서 작동합니다.

[:octicons-home-16: Homepage](https://www.gopass.pw){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/gopasspw/gopass/tree/master/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/gopasspw/gopass){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/dominikschulz){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://www.gopass.pw/#install-windows)
- [:simple-apple: macOS](https://www.gopass.pw/#install-macos)
- [:simple-linux: Linux](https://www.gopass.pw/#install-linux)
- [:simple-freebsd: FreeBSD](https://www.gopass.pw/#install-bsd)

</details>

</div>

### 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

</div>

- 크로스 플랫폼을 지원해야 합니다.
