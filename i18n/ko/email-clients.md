---
title: "이메일 클라이언트"
icon: material/email-open
description: 이 이메일 클라이언트는 프라이버시를 존중하며 OpenPGP 이메일 암호화를 지원합니다.
cover: email-clients.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-server-network: 서비스 제공업체](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-target-account: 표적 공격](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

프라이버시 가이드가 추천하는 **이메일 클라이언트**는 [OpenPGP](encryption.md#openpgp)와 [개방형 인증(OAuth)](basics/account-creation.md#sign-in-with-oauth) 같은 강력한 인증 방식을 모두 지원합니다. OAuth를 사용하면 [다중 인증](basics/multi-factor-authentication.md)으로 계정 탈취를 막을 수 있습니다.

<details class="warning" markdown>
<summary>이메일은 순방향 비밀성을 제공하지 않습니다</summary>

OpenPGP 같은 종단 간 암호화(E2EE) 기술을 사용하더라도 이메일 헤더에는 암호화되지 않은 [일부 메타데이터](basics/email-security.md#email-metadata-overview)가 남습니다.

또한 OpenPGP는 [순방향 비밀성](https://en.wikipedia.org/wiki/Forward_secrecy)을 지원하지 않으므로, 여러분이나 수신자의 개인 키가 도난당하면 그 키로 암호화된 이전 메시지가 모두 노출됩니다: [개인 키는 어떻게 보호하나요?](basics/email-security.md) 순방향 비밀성을 제공하는 수단을 사용하는 것을 고려해 보세요:

[실시간 통신](real-time-communication.md ""){.md-button}

</details>

## 크로스 플랫폼 { #cross-platform }

### 썬더버드 { #thunderbird }

<div class="admonition recommendation" markdown>

![썬더버드 로고](assets/img/email-clients/thunderbird.svg){ align=right }

**썬더버드**는 썬더버드 커뮤니티가 (과거에는 모질라 재단이) 개발한 자유 오픈 소스 크로스 플랫폼 이메일, 뉴스그룹, 뉴스 피드, 채팅(XMPP, IRC, 매트릭스) 클라이언트입니다.

[:octicons-home-16: 홈페이지](https://thunderbird.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/thunderbird){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://support.mozilla.org/products/thunderbird){ .card-link title="문서" }
[:octicons-code-16:](https://hg.mozilla.org/comm-central){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=net.thunderbird.android)
- [:simple-github: 깃허브](https://github.com/thunderbird/thunderbird-android/releases)
- [:fontawesome-brands-windows: 윈도우](https://thunderbird.net)
- [:simple-apple: macOS](https://thunderbird.net)
- [:simple-linux: 리눅스](https://thunderbird.net)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.Thunderbird)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

썬더버드 모바일에서 메일링 리스트의 누군가에게 답장할 때, "답장" 옵션에 메일링 리스트가 함께 포함될 수 있습니다. 자세한 내용은 [thunderbird/thunderbird-android #3738](https://github.com/thunderbird/thunderbird-android/issues/3738)을 참고하세요.

</div>

#### 권장 설정 { #recommended-configuration }

<div class="annotate" markdown>

썬더버드 데스크톱의 프라이버시를 조금 더 높이려면 다음 설정 중 일부를 변경할 것을 권장합니다.

이 옵션은 :material-menu: → **설정** → **개인 정보 및 보안**에서 찾을 수 있습니다.

##### 웹 콘텐츠 { #web-content }

- [ ] **방문한 웹 사이트와 링크 기억하기** 선택 해제
- [ ] **사이트의 쿠키 허용** 선택 해제 (1)

</div>

1. 지메일 같은 일부 제공업체에 로그인하거나 기관의 SSO를 통해 로그인할 때는 이 설정을 선택한 상태로 두어야 할 수도 있습니다. 로그인에 성공하면 선택을 해제하세요.

##### 원격 측정 { #telemetry }

- [ ] **Thunderbird가 기술 및 상호 작용 데이터를 Mozilla에 보내도록 허용** 선택 해제

#### Thunderbird-user.js(고급) { #thunderbird-userjs-advanced }

[`thunderbird-user.js`](https://github.com/HorlogeSkynet/thunderbird-user.js)는 공격 표면을 줄이고 프라이버시를 지키기 위해 썬더버드 데스크톱의 웹 브라우징 기능을 최대한 비활성화하는 것을 목표로 하는 구성 옵션 모음입니다. 일부 변경 사항은 [아켄폭스 프로젝트](desktop-browsers.md#arkenfox-advanced)에서 백포트되었습니다.

## 플랫폼별 { #platform-specific }

### 애플 메일(macOS) { #apple-mail-macos }

<div class="admonition recommendation" markdown>

![애플 메일 로고](assets/img/email-clients/applemail.png){ align=right }

**애플 메일**은 macOS에 포함되어 있으며, [GPG 스위트](encryption.md#gpg-suite)로 확장하면 OpenPGP를 지원하여 PGP로 암호화된 이메일을 보낼 수 있습니다.

[:octicons-home-16: 홈페이지](https://support.apple.com/guide/mail/welcome/mac){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/en-ww){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://support.apple.com/mail){ .card-link title="문서"}

</details>

</div>

<div class="admonition info" markdown>
<p class="admonition-title">macOS 소노마를 사용하는 경우</p>

현재 GPG 스위트는 macOS 소노마용 안정 릴리스가 [아직](https://gpgtools.com/sonoma) 없습니다.

</div>

애플 메일은 [macOS](https://support.apple.com/guide/mail/mlhl03be2866/mac)와 [iOS](https://support.apple.com/guide/iphone/iphf084865c7/ios)에서 원격 콘텐츠를 백그라운드에서 불러오거나 완전히 차단하고, 발신자로부터 IP 주소를 숨기는 기능을 제공합니다.

### 페어이메일(안드로이드) { #fairemail-android }

<div class="admonition recommendation" markdown>

![페어이메일 로고](assets/img/email-clients/fairemail.svg){ align=right }

**페어이메일**은 개방형 표준(IMAP, SMTP, OpenPGP)을 사용하며 데이터와 배터리 사용량을 최소화하는 미니멀한 오픈 소스 이메일 앱입니다.

[:octicons-home-16: 홈페이지](https://email.faircode.eu){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/M66B/FairEmail/blob/master/PRIVACY.md){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://github.com/M66B/FairEmail/blob/master/FAQ.md){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/M66B/FairEmail){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://email.faircode.eu/donate){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=eu.faircode.email)
- [:simple-github: 깃허브](https://github.com/M66B/FairEmail/releases)

</details>

</div>

### 그놈 에볼루션(그놈) { #gnome-evolution-gnome }

<div class="admonition recommendation" markdown>

![에볼루션 로고](assets/img/email-clients/evolution.svg){ align=right }

**에볼루션**은 메일, 캘린더, 주소록 기능을 통합해 제공하는 개인 정보 관리 애플리케이션입니다. 에볼루션에는 시작하는 데 도움이 되는 방대한 [문서](https://gnome.pages.gitlab.gnome.org/evolution/help)가 있습니다.

[:octicons-home-16: 홈페이지](https://gitlab.gnome.org/GNOME/evolution/-/wikis/home){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.gnome.org/GNOME/evolution/-/wikis/Privacy-Policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://gnome.pages.gitlab.gnome.org/evolution/help){ .card-link title="문서" }
[:octicons-code-16:](https://gitlab.gnome.org/GNOME/evolution){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://gnome.org/donate){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.gnome.Evolution)

</details>

</div>

### 콘택트(KDE) { #kontact-kde }

<div class="admonition recommendation" markdown>

![콘택트 로고](assets/img/email-clients/kontact.svg){ align=right }

**콘택트**는 [KDE](https://kde.org) 프로젝트의 개인 정보 관리자(PIM) 애플리케이션입니다. 메일 클라이언트, 주소록, RSS 클라이언트, 일정 관리 도구를 제공합니다.

[:octicons-home-16: 홈페이지](https://kontact.kde.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kde.org/privacypolicy-apps){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://kontact.kde.org/users){ .card-link title="문서" }
[:octicons-code-16:](https://invent.kde.org/pim/kmail){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://kde.org/community/donations){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-linux: 리눅스](https://kontact.kde.org/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.kde.kontact)

</details>

</div>

### 메일벨로프(브라우저) { #mailvelope-browser }

<div class="admonition recommendation" markdown>

![메일벨로프 로고](assets/img/email-clients/mailvelope.svg){ align=right }

**메일벨로프**는 OpenPGP 암호화 표준에 따라 암호화된 이메일을 주고받을 수 있게 해 주는 브라우저 확장 프로그램입니다.

[:octicons-home-16: 홈페이지](https://mailvelope.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailvelope.com/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://mailvelope.com/faq){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/mailvelope/mailvelope){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-firefoxbrowser: 파이어폭스](https://addons.mozilla.org/firefox/addon/mailvelope)
- [:simple-googlechrome: 크롬](https://chrome.google.com/webstore/detail/mailvelope/kajibbejlbohfaggdiogboambcijhkke)
- [:fontawesome-brands-edge: 엣지](https://microsoftedge.microsoft.com/addons/detail/mailvelope/dgcbddhdhjppfdfjpciagmmibadmoapc)

</details>

</div>

### 네오머트(CLI) { #neomutt-cli }

<div class="admonition recommendation" markdown>

![네오머트 로고](assets/img/email-clients/mutt.svg){ align=right }

**네오머트**는 리눅스와 BSD용 오픈 소스 명령줄 이메일 리더입니다. [머트](https://en.wikipedia.org/wiki/Mutt_(email_client))에 기능을 추가한 포크입니다.

네오머트는 텍스트 기반 클라이언트로 학습 곡선이 가파릅니다. 하지만 사용자 지정의 폭이 매우 넓습니다.

[:octicons-home-16: 홈페이지](https://neomutt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://neomutt.org/guide){ .card-link title="문서"}
[:octicons-code-16:](https://github.com/neomutt/neomutt){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://paypal.com/paypalme/russon){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-apple: macOS](https://neomutt.org/distro)
- [:simple-linux: 리눅스](https://neomutt.org/distro)

</details>

</div>

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

### 최소 요구 사항 { #minimum-qualifications }

- 오픈 소스 운영 체제용으로 개발된 앱은 오픈 소스여야 합니다.
- 원격 측정을 수집하지 않거나, 모든 원격 측정을 쉽게 비활성화하는 방법이 있어야 합니다.
- OpenPGP 메시지 암호화를 지원해야 합니다.

### 우대 사항 { #best-case }

우대 사항은 이 카테고리에서 완벽한 프로젝트라면 갖추었으면 하는 사항을 나타냅니다. 추천 항목에 이 기능 중 일부 또는 전부가 없을 수도 있지만, 이러한 기능을 갖춘 항목은 이 페이지에서 다른 항목보다 높은 순위에 오를 수 있습니다.

- 오픈 소스인 것이 좋습니다.
- 크로스 플랫폼을 지원하는 것이 좋습니다.
- 기본적으로 어떠한 원격 측정도 수집하지 않는 것이 좋습니다.
- 확장 프로그램 없이 OpenPGP를 기본 지원하는 것이 좋습니다.
- OpenPGP로 암호화된 이메일을 로컬에 저장하는 기능을 지원하는 것이 좋습니다.
