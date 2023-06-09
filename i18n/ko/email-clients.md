---
title: "이메일 클라이언트"
icon: material/email-open
description: 프라이버시 중점적이며 OpenPGP 이메일 암호화를 지원하는 이메일 클라이언트 목록입니다.
cover: email-clients.png
---

본 권장 목록의 이메일 클라이언트는 [OpenPGP](encryption.md#openpgp) 및 [OAuth(Open Authorization)](https://en.wikipedia.org/wiki/OAuth) 같은 강력한 인증을 모두 지원합니다. OAuth를 이용하면 [다중 인증](basics/multi-factor-authentication.md)으로 계정을 보호할 수 있습니다.

??? warning "이메일은 순방향 비밀성을 제공하지 않습니다."

    이메일은 OpenPGP 등 종단 간 암호화(E2EE) 기술을 사용하더라도, 이메일 헤더에 [일부 메타데이터](email.md#email-metadata-overview)는 암호화되지 않은 채로 존재합니다.
    
    또한 OpenPGP는 [순방향 비밀성(Forward Secrecy)](https://en.wikipedia.org/wiki/Forward_secrecy)을 지원하지 않습니다. 따라서 발신자/수신자의 개인 키가 도난당할 경우, 해당 키로 암호화된 이전 메시지가 전부 노출됩니다([개인 키를 보호하는 방법](basics/email-security.md)). 되도록이면 순방향 비밀성을 제공하는 매체를 사용하세요.
    
    [실시간 커뮤니케이션](real-time-communication.md){ .md-button }

## 크로스 플랫폼

### Thunderbird

!!! recommendation

    ![Thunderbird 로고](assets/img/email-clients/thunderbird.svg){ align=right }
    
    **Thunderbird**는 무료 오픈 소스 크로스 플랫폼 이메일 클라이언트입니다. 이메일, 뉴스그룹, 뉴스 피드, 채팅(XMPP, IRC, Twitter) 기능을 지원합니다. 이전에는 Mozilla 재단에서 개발했으며, 현재는 Thunderbird 커뮤니티에서 개발하고 있습니다.
    
    [:octicons-home-16: 홈페이지](https://www.thunderbird.net){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mozilla.org/privacy/thunderbird){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://support.mozilla.org/products/thunderbird){ .card-link title=문서}
    [:octicons-code-16:](https://hg.mozilla.org/comm-central){ .card-link title="소스 코드" }
    
    ??? downloads "다운로드"
    
        - [:simple-windows11: Windows](https://www.thunderbird.net)
        - [:simple-apple: macOS](https://www.thunderbird.net)
        - [:simple-linux: Linux](https://www.thunderbird.net)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.Thunderbird)

#### 권장 설정

다음 설정을 통해 Thunderbird에서 프라이버시를 더 강화할 것을 권장드립니다.

이러한 옵션은 :material-menu: → **설정** → **개인 정보 및 보안**에서 확인할 수 있습니다.

##### 웹 내용

- [ ] **방문한 웹 사이트와 링크 기억하기** 비활성화
- [ ] **쿠키 허용** 비활성화

##### 데이터 수집

- [ ] **Thunderbird가 기술과 상호 작용 정보를 Mozilla에 전송하도록 허용** 비활성화

#### Thunderbird-user.js (고급)

[`thunderbird-user.js`](https://github.com/HorlogeSkynet/thunderbird-user.js)는 공격 표면을 줄이고 프라이버시를 지키기 위해 Thunderbird 내 웹 탐색 기능을 최소화하는 것을 목표로 하는 구성 옵션 세트입니다. 일부분은 [Arkenfox 프로젝트](https://github.com/arkenfox/user.js)에서 백포트되었습니다.

## 개별 플랫폼

### Apple Mail (macOS)

!!! recommendation

    ![Apple Mail 로고](assets/img/email-clients/applemail.png){ align=right }
    
    **Apple Mail**은 macOS에 기본 포함되어 있으며, PGP 암호화 이메일 전송 기능을 추가하는 [GPG Suite](encryption.md#gpg-suite)를 통해 OpenPGP를 지원하도록 확장 가능합니다.
    
    [:octicons-home-16: 홈페이지](https://support.apple.com/guide/mail/welcome/mac){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.apple.com/legal/privacy/en-ww/){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://support.apple.com/mail){ .card-link title=문서}

Apple Mail은 외부 콘텐츠를 백그라운드에서 로드하거나, 완전히 차단해 발신자로부터 IP 주소를 숨길 수 있는 기능을 [macOS](https://support.apple.com/guide/mail/mlhl03be2866/mac) 및 [iOS](https://support.apple.com/guide/iphone/iphf084865c7/ios)에서 제공합니다.

### Canary Mail (iOS)

!!! recommendation

    ![Canary Mail 로고](assets/img/email-clients/canarymail.svg){ align=right }
    
    **Canary Mail**은 유료 이메일 클라이언트로, 생체 인식 앱 잠금 등의 보안 기능으로 원활한 종단 간 암호화를 지원하도록 설계되었습니다.
    
    [:octicons-home-16: 홈페이지](https://canarymail.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://canarymail.io/privacy.html){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://canarymail.zendesk.com/){ .card-link title=문서}
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.canarymail.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1236045954)
        - [:simple-windows11: Windows](https://canarymail.io/downloads.html)

!!! warning "경고"

    Canary Mail은 Windows 및 Android용 클라이언트를 최근 출시했지만, 저희는 해당 클라이언트가 iOS/Mac용 클라이언트만큼 안정적이진 않다고 판단하고 있습니다.

Canay Mail은 오픈 소스가 아닙니다. iOS에서 PGP E2EE를 지원하는 이메일 클라이언트가 몇 없기 때문에 권장 목록에 등재되었습니다.

### FairEmail (Android)

!!! recommendation

    ![FairEmail 로고](assets/img/email-clients/fairemail.svg){ align=right }
    
    **FairEmail**은 미니멀한 오픈 소스 이메일 앱으로, 개방형 표준(IMAP, SMTP, OpenPGP)을 사용하고 데이터 및 배터리 사용량이 적습니다.
    
    [:octicons-home-16: 홈페이지](https://email.faircode.eu){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/M66B/FairEmail/blob/master/PRIVACY.md){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://github.com/M66B/FairEmail/blob/master/FAQ.md){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/M66B/FairEmail){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://email.faircode.eu/donate/){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=eu.faircode.email)
        - [:simple-github: GitHub](https://github.com/M66B/FairEmail/releases)

### GNOME Evolution (GNOME)

!!! recommendation

    ![Evolution 로고](assets/img/email-clients/evolution.svg){ align=right }
    
    **Evolution** 메일, 캘린더, 연락처 기능을 통합적으로 제공하는 개인 정보 관리 애플리케이션입니다. 시작하는 데에 도움이 되는 방대한 [문서](https://help.gnome.org/users/evolution/stable/)가 존재합니다.
    
    [:octicons-home-16: 홈페이지](https://wiki.gnome.org/Apps/Evolution){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://wiki.gnome.org/Apps/Evolution/PrivacyPolicy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://help.gnome.org/users/evolution/stable/){ .card-link title=문서}
    [:octicons-code-16:](https://gitlab.gnome.org/GNOME/evolution/){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://www.gnome.org/donate/){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.gnome.Evolution)

### K-9 Mail (Android)

!!! recommendation

    ![K-9 Mail 로고](assets/img/email-clients/k9mail.svg){ align=right }
    
    **K-9 Mail**은 POP3, IMAP 메일함을 모두 지원하는 메일 애플리케이션입니다. 실시간 푸시 메일은 IMAP에서만 지원합니다.
    
    K-9 Mail은 [공식적으로 Thunderbird 브랜드에 통합되었으며](https://k9mail.app/2022/06/13/K-9-Mail-and-Thunderbird.html), 추후 Android용 Thunderbird 클라이언트가 될 예정입니다.
    
    [:octicons-home-16: 홈페이지](https://k9mail.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://k9mail.app/privacy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://docs.k9mail.app/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/k9mail/k-9){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://k9mail.app/contribute){ .card-link title=기여 }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.fsck.k9)
        - [:simple-github: GitHub](https://github.com/k9mail/k-9/releases)

!!! warning "경고"

    메일링 리스트 내 누군가에게 답장(Reply)할 때, 답장 대상에 전체 메일링 리스트가 포함될 수도 있습니다. 자세한 내용은 [thundernest/k-9 #3738](https://github.com/thundernest/k-9/issues/3738)를 참고해 주세요.

### Kontact (KDE)

!!! recommendation

    ![Kontact 로고](assets/img/email-clients/kontact.svg){ align=right }
    
    **Kontact**는 [KDE](https://kde.org) 프로젝트의 개인 정보 관리자(PIM) 애플리케이션입니다. 메일 클라이언트, 연락처, 일정 관리, RSS 클라이언트 기능을 제공합니다.
    
    [:octicons-home-16: 홈페이지](https://kontact.kde.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://kde.org/privacypolicy-apps){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://kontact.kde.org/users/){ .card-link title=문서}
    [:octicons-code-16:](https://invent.kde.org/pim/kmail){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://kde.org/community/donations/){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-linux: Linux](https://kontact.kde.org/download)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.kde.kontact)

### Mailvelope (브라우저)

!!! recommendation

    ![Mailvelope 로고](assets/img/email-clients/mailvelope.svg){ align=right }
    
    **Mailvelope**는 OpenPGP 암호화 표준에 따라 암호화된 이메일을 주고받을 수 있게 해주는 브라우저 확장 프로그램입니다.
    
    [:octicons-home-16: 홈페이지](https://www.mailvelope.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mailvelope.com/en/privacy-policy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://mailvelope.com/faq){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/mailvelope/mailvelope){ .card-link title="소스 코드" }
    
    ??? downloads "다운로드"
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/mailvelope)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/mailvelope/kajibbejlbohfaggdiogboambcijhkke)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/mailvelope/dgcbddhdhjppfdfjpciagmmibadmoapc)

### NeoMutt (CLI)

!!! recommendation

    ![NeoMutt 로고](assets/img/email-clients/mutt.svg){ align=right }
    
    **NeoMutt**은 Linux, BSD용 오픈 소스 CLI 메일 리더 프로그램(MUA)입니다. [Mutt](https://en.wikipedia.org/wiki/Mutt_(email_client))로부터 포크되어 기능이 추가된 프로젝트입니다.
    
    NeoMutt은 텍스트 기반 클라이언트로, 사용법을 익히기 매우 어렵습니다. 하지만 자유로운 커스텀이 가능합니다.
    
    [:octicons-home-16: 홈페이지](https://neomutt.org){ .md-button .md-button--primary }
    [:octicons-info-16:](https://neomutt.org/guide/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/neomutt/neomutt){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://www.paypal.com/paypalme/russon/){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-apple: macOS](https://neomutt.org/distro)
        - [:simple-linux: Linux](https://neomutt.org/distro)

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

!!! example "이 단락은 최근에 만들어졌습니다"

    Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

### 최소 요구 사항

- 오픈 소스 운영 체제용으로 개발된 앱은 반드시 오픈 소스여야 합니다.
- 원격 분석 데이터를 수집하지 않거나, 모든 원격 분석을 간단하게 비활성화할 수 있어야 합니다.
- OpenPGP 메시지 암호화를 지원해야 합니다.

### 우대 사항

평가 기준에서 '우대 사항'은 해당 부문에서 완벽한 프로젝트에 기대하는 바를 나타냅니다. 다음의 우대 사항에 해당하지 않더라도 권장 목록에 포함될 수 있습니다. 단, 우대 사항에 해당할수록 이 페이지의 다른 항목보다 높은 순위를 갖습니다.

- 오픈 소스여야 합니다.
- 크로스 플랫폼을 지원해야 합니다.
- 원격 분석 데이터를 기본적으로 수집하지 않아야 합니다.
- (확장 프로그램 등을 필요로 하지 않고) 기본적으로 OpenPGP를 지원해야 합니다.
- OpenPGP 암호화 이메일 로컬 저장을 지원해야 합니다.
