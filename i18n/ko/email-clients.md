---
title: "이메일 클라이언트"
icon: material/email-open
description: These email clients are privacy-respecting and support OpenPGP email encryption.
cover: email-clients.webp
---

본 권장 목록의 이메일 클라이언트는 [OpenPGP](encryption.md#openpgp) 및 [OAuth(Open Authorization)](https://en.wikipedia.org/wiki/OAuth) 같은 강력한 인증을 모두 지원합니다. OAuth를 이용하면 [다중 인증](basics/multi-factor-authentication.md)으로 계정을 보호할 수 있습니다.

<details class="warning" markdown>
<summary>Email does not provide forward secrecy</summary>

When using end-to-end encryption (E2EE) technology like OpenPGP, email will still have [some metadata](basics/email-security.md#email-metadata-overview) that is not encrypted in the header of the email.

OpenPGP also does not support [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), which means if either your or the recipient's private key is ever stolen, all previous messages encrypted with it will be exposed: [How do I protect my private keys?](basics/email-security.md) Consider using a medium that provides forward secrecy:

[Real-time Communication](real-time-communication.md ""){.md-button}

</details>

## 크로스 플랫폼

### Thunderbird

<div class="admonition recommendation" markdown>

![Thunderbird logo](assets/img/email-clients/thunderbird.svg){ align=right }

**Thunderbird** is a free, open-source, cross-platform email, newsgroup, news feed, and chat (XMPP, IRC, Matrix) client developed by the Thunderbird community, and previously by the Mozilla Foundation.

[:octicons-home-16: Homepage](https://thunderbird.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/thunderbird){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.mozilla.org/products/thunderbird){ .card-link title=Documentation}
[:octicons-code-16:](https://hg.mozilla.org/comm-central){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://thunderbird.net)
- [:simple-apple: macOS](https://thunderbird.net)
- [:simple-linux: Linux](https://thunderbird.net)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.Thunderbird)

</details>

</div>

#### 권장 설정

다음 설정을 통해 Thunderbird에서 프라이버시를 더 강화할 것을 권장드립니다.

이러한 옵션은 :material-menu: → **설정** → **개인 정보 및 보안**에서 확인할 수 있습니다.

##### 웹 내용

- [ ] **방문한 웹 사이트와 링크 기억하기** 비활성화
- [ ] **쿠키 허용** 비활성화

##### 데이터 수집

- [ ] **Thunderbird가 기술과 상호 작용 정보를 Mozilla에 전송하도록 허용** 비활성화

#### Thunderbird-user.js (고급)

[`thunderbird-user.js`](https://github.com/HorlogeSkynet/thunderbird-user.js) is a set of configurations options that aims to disable as many of the web-browsing features within Thunderbird as possible in order to reduce attack surface and maintain privacy. 일부분은 [Arkenfox 프로젝트](https://github.com/arkenfox/user.js)에서 백포트되었습니다.

## 개별 플랫폼

### Apple Mail (macOS)

<div class="admonition recommendation" markdown>

![Apple Mail 로고](assets/img/email-clients/applemail.png){ align=right }

**Apple Mail**은 macOS에 기본 포함되어 있으며, PGP 암호화 이메일 전송 기능을 추가하는 [GPG Suite](encryption.md#gpg-suite)를 통해 OpenPGP를 지원하도록 확장 가능합니다.

[:octicons-home-16: Homepage](https://support.apple.com/guide/mail/welcome/mac){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/en-ww){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/mail){ .card-link title=Documentation}

</details>

</div>

Apple Mail은 외부 콘텐츠를 백그라운드에서 로드하거나, 완전히 차단해 발신자로부터 IP 주소를 숨길 수 있는 기능을 [macOS](https://support.apple.com/guide/mail/mlhl03be2866/mac) 및 [iOS](https://support.apple.com/guide/iphone/iphf084865c7/ios)에서 제공합니다.

### Canary Mail (iOS)

<div class="admonition recommendation" markdown>

![Canary Mail 로고](assets/img/email-clients/canarymail.svg){ align=right }

**Canary Mail**은 유료 이메일 클라이언트로, 생체 인식 앱 잠금 등의 보안 기능으로 원활한 종단 간 암호화를 지원하도록 설계되었습니다.

[:octicons-home-16: Homepage](https://canarymail.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://canarymail.io/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://canarymail.io/help){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.canarymail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1236045954)
- [:simple-windows11: Windows](https://canarymail.io/downloads.html)

</details>

</div>

<details class="warning" markdown>
<summary>Warning</summary>

Canary Mail은 Windows 및 Android용 클라이언트를 최근 출시했지만, 저희는 해당 클라이언트가 iOS/Mac용 클라이언트만큼 안정적이진 않다고 판단하고 있습니다.

</details>

Canay Mail은 오픈 소스가 아닙니다. iOS에서 PGP E2EE를 지원하는 이메일 클라이언트가 몇 없기 때문에 권장 목록에 등재되었습니다.

### FairEmail (Android)

<div class="admonition recommendation" markdown>

![FairEmail 로고](assets/img/email-clients/fairemail.svg){ align=right }

**FairEmail**은 미니멀한 오픈 소스 이메일 앱으로, 개방형 표준(IMAP, SMTP, OpenPGP)을 사용하고 데이터 및 배터리 사용량이 적습니다.

[:octicons-home-16: Homepage](https://email.faircode.eu){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/M66B/FairEmail/blob/master/PRIVACY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/M66B/FairEmail/blob/master/FAQ.md){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/M66B/FairEmail){ .card-link title="Source Code" }
[:octicons-heart-16:](https://email.faircode.eu/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=eu.faircode.email)
- [:simple-github: GitHub](https://github.com/M66B/FairEmail/releases)

</details>

</div>

### GNOME Evolution (GNOME)

<div class="admonition recommendation" markdown>

![Evolution 로고](assets/img/email-clients/evolution.svg){ align=right }

**Evolution** 메일, 캘린더, 연락처 기능을 통합적으로 제공하는 개인 정보 관리 애플리케이션입니다. Evolution has extensive [documentation](https://help.gnome.org/users/evolution/stable) to help you get started.

[:octicons-home-16: Homepage](https://wiki.gnome.org/Apps/Evolution){ .md-button .md-button--primary }
[:octicons-eye-16:](https://wiki.gnome.org/Apps/Evolution/PrivacyPolicy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.gnome.org/users/evolution/stable){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.gnome.org/GNOME/evolution){ .card-link title="Source Code" }
[:octicons-heart-16:](https://gnome.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.gnome.Evolution)

</details>

</div>

### K-9 Mail (Android)

<div class="admonition recommendation" markdown>

![K-9 Mail 로고](assets/img/email-clients/k9mail.svg){ align=right }

**K-9 Mail**은 POP3, IMAP 메일함을 모두 지원하는 메일 애플리케이션입니다. 실시간 푸시 메일은 IMAP에서만 지원합니다.

K-9 Mail은 [공식적으로 Thunderbird 브랜드에 통합되었으며](https://k9mail.app/2022/06/13/K-9-Mail-and-Thunderbird.html), 추후 Android용 Thunderbird 클라이언트가 될 예정입니다.

[:octicons-home-16: Homepage](https://k9mail.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://k9mail.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.k9mail.app){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/thundernest/k-9){ .card-link title="Source Code" }
[:octicons-heart-16:](https://k9mail.app/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.fsck.k9)
- [:simple-github: GitHub](https://github.com/thundernest/k-9/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

메일링 리스트 내 누군가에게 답장(Reply)할 때, 답장 대상에 전체 메일링 리스트가 포함될 수도 있습니다. 자세한 내용은 [thundernest/k-9 #3738](https://github.com/thundernest/k-9/issues/3738)를 참고해 주세요.

</div>

### Kontact (KDE)

<div class="admonition recommendation" markdown>

![Kontact 로고](assets/img/email-clients/kontact.svg){ align=right }

**Kontact**는 [KDE](https://kde.org) 프로젝트의 개인 정보 관리자(PIM) 애플리케이션입니다. 메일 클라이언트, 연락처, 일정 관리, RSS 클라이언트 기능을 제공합니다.

[:octicons-home-16: Homepage](https://kontact.kde.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kde.org/privacypolicy-apps){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kontact.kde.org/users){ .card-link title=Documentation}
[:octicons-code-16:](https://invent.kde.org/pim/kmail){ .card-link title="Source Code" }
[:octicons-heart-16:](https://kde.org/community/donations){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-linux: Linux](https://kontact.kde.org/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.kde.kontact)

</details>

</div>

### Mailvelope (브라우저)

<div class="admonition recommendation" markdown>

![Mailvelope 로고](assets/img/email-clients/mailvelope.svg){ align=right }

**Mailvelope**는 OpenPGP 암호화 표준에 따라 암호화된 이메일을 주고받을 수 있게 해주는 브라우저 확장 프로그램입니다.

[:octicons-home-16: Homepage](https://mailvelope.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailvelope.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mailvelope.com/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mailvelope/mailvelope){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/mailvelope)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/mailvelope/kajibbejlbohfaggdiogboambcijhkke)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/mailvelope/dgcbddhdhjppfdfjpciagmmibadmoapc)

</details>

</div>

### NeoMutt (CLI)

<div class="admonition recommendation" markdown>

![NeoMutt 로고](assets/img/email-clients/mutt.svg){ align=right }

**NeoMutt**은 Linux, BSD용 오픈 소스 CLI 메일 리더 프로그램(MUA)입니다. [Mutt](https://en.wikipedia.org/wiki/Mutt_(email_client))로부터 포크되어 기능이 추가된 프로젝트입니다.

NeoMutt은 텍스트 기반 클라이언트로, 사용법을 익히기 매우 어렵습니다. 하지만 자유로운 커스텀이 가능합니다.

[:octicons-home-16: Homepage](https://neomutt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://neomutt.org/guide){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/neomutt/neomutt){ .card-link title="Source Code" }
[:octicons-heart-16:](https://paypal.com/paypalme/russon){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-apple: macOS](https://neomutt.org/distro)
- [:simple-linux: Linux](https://neomutt.org/distro)

</details>

</div>

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

### 최소 요구 사항

- Apps developed for open-source operating systems must be open source.
- 원격 분석 데이터를 수집하지 않거나, 모든 원격 분석을 간단하게 비활성화할 수 있어야 합니다.
- OpenPGP 메시지 암호화를 지원해야 합니다.

### 우대 사항

평가 기준에서 '우대 사항'은 해당 부문에서 완벽한 프로젝트에 기대하는 바를 나타냅니다. 다음의 우대 사항에 해당하지 않더라도 권장 목록에 포함될 수 있습니다. 단, 우대 사항에 해당할수록 이 페이지의 다른 항목보다 높은 순위를 갖습니다.

- Should be open source.
- 크로스 플랫폼을 지원해야 합니다.
- 원격 분석 데이터를 기본적으로 수집하지 않아야 합니다.
- (확장 프로그램 등을 필요로 하지 않고) 기본적으로 OpenPGP를 지원해야 합니다.
- OpenPGP 암호화 이메일 로컬 저장을 지원해야 합니다.
