---
meta_title: "비공개 암호화 이메일 서비스 권장 목록 - Privacy Guides"
title: "이메일 서비스"
icon: material/email
description: 이러한 이메일 제공 업체는 여러분의 이메일을 안전하게 보관하기에 적합합니다. 대부분이 OpenPGP 암호화를 제공하여 다른 이메일 서비스와도 호환됩니다.
cover: email.png
---

이메일은 모든 온라인 서비스 이용에 사실상 필수적이지만, 개인 간 대화에는 권장드리지 않습니다. 다른 사람에게 연락할 때는 이메일보다는 순방향 비밀성을 지원하는 인스턴트 메신저를 사용하는 것이 좋습니다.

[권장 인스턴트 메신저](real-time-communication.md ""){.md-button}

그 외 용도로 이메일을 사용한다면, 지속 가능한 비즈니스 모델을 갖추고 보안 및 프라이버시 기능을 기본 제공하는 이메일 제공 업체를 권장합니다.

- [OpenPGP 호환 이메일 제공 업체 :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [기타 암호화 이메일 제공 업체 :material-arrow-right-drop-circle:](#more-providers)
- [이메일 별칭 서비스 :material-arrow-right-drop-circle:](#email-aliasing-services)
- [자체 호스팅 솔루션 :material-arrow-right-drop-circle:](#self-hosting-email)

## OpenPGP 호환 서비스

다음 제공 업체는 Open PGP 암호화/복호화 및 Web Key Directory(WKD) 표준을 기본적으로 지원하므로, 제공 업체를 가리지 않고 E2EE 이메일 이용이 가능합니다. 예를 들어, Proton Mail 사용자는 Mailbox.org 사용자에게 E2EE 메시지를 보내거나, OpenPGP 지원 인터넷 서비스에서 OpenPGP로 암호화된 알림을 받을 수 있습니다.

<div class="grid cards" markdown>

- ![Proton Mail 로고](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org 로고](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

!!! warning "경고"

    OpenPGP 등 E2EE 기술을 사용하더라도, 이메일 헤더의 일부 메타데이터는 암호화되지 않은 채로 존재합니다. [이메일 메타데이터 개요](basics/email-security.md#email-metadata-overview)를 살펴보세요.
    
    또한, OpenPGP는 순방향 비밀성을 지원하지 않습니다. 따라서 본인 혹은 수신자의 개인 키가 유출될 경우, 해당 키로 암호화된 이전 메시지가 전부 노출됩니다. [개인 키를 어떻게 보호해야 하나요?](basics/email-security.md#how-do-i-protect-my-private-keys)

### Proton Mail

!!! recommendation

    ![Proton Mail 로고](assets/img/email/protonmail.svg){ align=right }
    
    **Proton Mail**은 프라이버시, 암호화, 보안, 사용 편의성에 중점을 둔 이메일 서비스입니다. **2013년**부터 운영되었습니다. Proton AG 본사는 스위스 제네바에 위치하고 있습니다. 무료 플랜 계정은 500MB 저장 공간으로 시작합니다.
    
    [:octicons-home-16: 홈페이지](https://proton.me/mail){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion 서비스" }
    [:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://proton.me/support/mail){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="소스 코드" }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id979659905)
        - [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
        - [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
        - [:simple-apple: macOS](https://proton.me/mail/bridge#download)
        - [:simple-linux: Linux](https://proton.me/mail/bridge#download)
        - [:octicons-browser-16: Web](https://mail.proton.me)

무료 계정은 본문 텍스트 검색이 불가능하고 [Proton Mail Bridge](https://proton.me/mail/bridge)(Thunderbird 등 [권장 데스크톱 이메일 클라이언트](email-clients.md)를 사용하려면 필수적인 기능)를 사용할 수 없습니다. 유료 계정에는 Proton Mail Bridge, 추가 저장 공간, 사용자 지정 도메인 지원 등의 기능이 제공됩니다. Proton Mail 앱 [감사 증명서](https://proton.me/blog/security-audit-all-proton-apps)는 2021년 11월 9일에 [Securitum](https://research.securitum.com)에서 발급하였습니다.

Proton Unlimited, Business, Visionary 플랜을 이용 중이라면 [SimpleLogin](#simplelogin) 프리미엄도 무료로 제공됩니다.

Proton Mail에는 내부 충돌 보고서가 존재하며, 이는 제3자와 공유되지 **않습니다**. 충돌 보고서는 비활성화 가능합니다: **Settings** > **Go to Settings** > **Account** > **Security and privacy** > **Send crash reports**.

#### :material-check:{ .pg-green } 사용자 지정 도메인 및 별칭

Proton Mail 유료 이용자는 서비스에서 자신의 도메인을 사용하거나 [Catch-all](https://proton.me/support/catch-all) 주소를 사용할 수 있습니다. 도메인을 자신이 직접 구매하지 않더라도, Proton Mail이 지원하는 [보조 주소](https://proton.me/support/creating-aliases)를 유용하게 사용할 수 있습니다.

#### :material-check:{ .pg-green } 비공개 결제 수단

Proton Mail은 일반 신용/직불 카드, [비트코인](advanced/payments.md#other-coins-bitcoin-ethereum-etc), Paypal, 현금 우편 결제를 [지원합니다](https://proton.me/support/payment-options).

#### :material-check:{ .pg-green } 계정 보안

Proton Mail은 TOTP [이중 인증](https://proton.me/support/two-factor-authentication-2fa), FIDO2/U2F 표준 [하드웨어 보안 키](https://proton.me/support/2fa-security-key)를 지원합니다. 하드웨어 보안 키를 사용하려면 먼저 TOTP 이중 인증을 설정해야 합니다.

#### :material-check:{ .pg-green } 데이터 보안

Proton Mail은 이메일 및 [캘린더](https://proton.me/news/protoncalendar-security-model)에 [Zero Access Encryption](https://proton.me/blog/zero-access-encryption)을 적용하고 있습니다. Zero Access Encryption으로 보호된 데이터는 여러분 본인만 접근 가능합니다.

[Proton Contacts](https://proton.me/support/proton-contacts) 연락처에 저장된 특정 정보(표시된 이름, 이메일 주소 등)는 Zero Access Encryption으로 보호되지 않습니다. 전화번호 등, Zero Access Encrpytion이 적용된 연락처 필드는 자물쇠 아이콘으로 표시됩니다.

#### :material-check:{ .pg-green } 이메일 암호화

Proton Mail은 웹메일에 [OpenPGP 암호화 기능을 내장](https://proton.me/support/how-to-use-pgp)하고 있습니다. 다른 Proton Mail 계정으로 보내는 이메일은 자동으로 암호화되며, Proton Mail 외 주소로 보내는 이메일에 대한 OpenPGP 암호화는 계정 설정에서 간편하게 활성화할 수 있습니다. Proton Mail 계정도 없고 OpenPGP 등의 소프트웨어도 사용하지 않는 사람에게도 [암호화된 메시지를 보낼 수 있는 기능](https://proton.me/support/password-protected-emails) 또한 제공합니다.

Proton Mail은 자체 [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD)에서 HTTP로 공개 키를 검색할 수 있는 기능을 지원합니다. 이로써 Proton Mail을 사용하지 않는 사람도 Proton Mail OpenPGP 키를 쉽게 찾아 서로 다른 제공 업체 간 E2EE 적용이 가능합니다.


#### :material-information-outline:{ .pg-blue } Account Termination

If you have a paid account and your [bill is unpaid](https://proton.me/support/delinquency) after 14 days, you won't be able to access your data. 30일이 지나면 계정이 연체 상태가 되고, 메일을 수신할 수 없게 됩니다. 이 기간에 대해서도 계속 요금이 청구됩니다.

#### :material-information-outline:{ .pg-blue } 추가 기능

Proton Mail은 'Unlimited' 계정 요금제를 월 9.99유로에 제공합니다. Unlimited 계정은 Proton VPN 접근이 제공되며, 다중 계정, 도메인, 별칭을 비롯해 500GB 저장 공간이 제공됩니다.

Proton Mail은 디지털 유산 상속 기능을 제공하지 않습니다.

### Mailbox.org

!!! recommendation

    ![Mailbox.org 로고](assets/img/email/mailboxorg.svg){ align=right }
    
    **Mailbox.org**는 100% 친환경 에너지로 작동되는 안전하고, 광고가 없는 비공개 중점 이메일 서비스입니다. 2014년부터 운영되었습니다. Mailbox.org 본사는 독일 베를린에 위치하고 있습니다. 계정은 2GB 저장 공간으로 시작하며, 필요에 따라 업그레이드 가능합니다.
    
    [:octicons-home-16: 홈페이지](https://mailbox.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=문서}
    
    ??? downloads "다운로드"
    
        - [:octicons-browser-16: Web](https://login.mailbox.org)

#### :material-check:{ .pg-green } 사용자 지정 도메인 및 별칭

Mailbox.org는 자신의 도메인을 사용할 수 있으며, [Catch-all](https://kb.mailbox.org/display/MBOKBEN/Using+catch-all+alias+with+own+domain) 주소를 지원합니다. 도메인을 자신이 직접 구매하지 않더라도, Mailbox.org가 지원하는 [보조 주소](https://kb.mailbox.org/display/BMBOKBEN/What+is+an+alias+and+how+do+I+use+it)를 유용하게 사용할 수 있습니다.

#### :material-check:{ .pg-green } 비공개 결제 수단

Mailbox.org는 BitPay 결제 처리업체가 독일에서 운영을 중단함에 따라 어떠한 암호화폐도 받지 않습니다. 단, 몇 가지 독일 전용 결제 수단(paydirekt, Sofortüberweisung)을 비롯해 현금 우편, 은행 계좌 현금 입금, 은행 송금, 신용 카드, PayPal을 지원합니다.

#### :material-check:{ .pg-green } 계정 보안

Mailbox.org는 웹메일에 한해 [이중 인증](https://kb.mailbox.org/display/MBOKBEN/How+to+use+two-factor+authentication+-+2FA)을 지원합니다. TOTP 혹은 ([YubiCloud](https://www.yubico.com/products/services-software/yubicloud)를 통한) [YubiKey](https://en.wikipedia.org/wiki/YubiKey)를 사용할 수 있습니다. [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) 등의 웹 표준은 아직 지원되지 않습니다.

#### :material-information-outline:{ .pg-blue } 데이터 보안

Mailbox.org는 [암호화된 메일함](https://kb.mailbox.org/display/MBOKBEN/The+Encrypted+Mailbox)을 이용하여 수신 메일을 암호화할 수 있습니다. 새로 받은 메일들은 즉시 공개키로 암호화됩니다.

하지만 Mailbox.org에서 사용하는 소프트웨어 플랫폼인 [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange)는 주소록 및 캘린더 암호화를 [지원하지 않습니다.](https://kb.mailbox.org/display/BMBOKBEN/Encryption+of+calendar+and+address+book) 해당 데이터에 대해서는 [다른 솔루션](calendar.md)을 찾는것이 적합할 수 있습니다.

#### :material-check:{ .pg-green } 이메일 암호화

Mailbox.org의 웹메일에는 [암호화 기능이 내장](https://kb.mailbox.org/display/MBOKBEN/Send+encrypted+e-mails+with+Guard)되어 있어 공개 OpenPGP키를 가진 사람들에게 메일을 간편하게 보낼 수 있습니다. 또한, [수신자가 직접 Mailbox.org에 있는 메일을 복호화](https://kb.mailbox.org/display/MBOKBEN/My+recipient+does+not+use+PGP)하게 하는 기능도 있습니다. OpenPGP가 없어 수신자가 자신의 메일함에서 직접 복호화할 수 없을 경우에 이 기능을 사용할 수 있습니다.

또한, Mailbox.org는 [웹 키 디렉터리(WKD)](https://wiki.gnupg.org/WKD)에서 HTTP를 통한 공개 키 검색을 지원합니다. Mailbox.org를 사용하지 않는 사람들은 Mailbox.org 계정의 OpenPGP 공개키를 쉽게 찾을 수 있고, 플랫폼과 무관하게 종단간 암호화를 할 수 있습니다.

#### :material-information-outline:{ .pg-blue } 계정 삭제

계약이 끝나면 해당 계정은 제한된 상태로 변경되며, [30일이 지나면 영구적으로 삭제됩니다](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } 추가 기능

[.onion을 이용하여](https://kb.mailbox.org/display/MBOKBEN/The+Tor+exit+node+of+mailbox.org) Mailbox.org 계정을 IMAP/SMTP로 접근할 수 있습니다. 하지만 웹메일 인터페이스는 .onion 서비스로 접근할 수 없고, TLS 인증서 에러가 뜰 수 있습니다.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/display/MBOKBEN/Encrypt+files+on+your+Drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/display/MBOKBEN/Ensuring+E-Mails+are+Sent+Securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox.org also supports [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) in addition to standard access protocols like IMAP and POP3.

Mailbox.org has a digital legacy feature for all plans. You can choose whether you want any of your data to be passed to heirs providing that they apply and provide your testament. Alternatively, you can nominate a person by name and address.

## 그외 제공자

이 제공자들은 영지식 암호화를 사용하기에 메일을 안전하게 보관하는 용도로 좋습니다. However, they don't support interoperable encryption standards for E2EE communications between providers.

<div class="grid cards" markdown>

- ![StartMail 로고](assets/img/email/startmail.svg#only-light){ .twemoji }![StartMail 로고](assets/img/email/startmail-dark.svg#only-dark){ .twemoji } [StartMail](email.md#startmail)
- ![Tutanota 로고](assets/img/email/tutanota.svg){ .twemoji } [Tutanota](email.md#tutanota)

</div>

### StartMail

!!! recommendation

    ![StartMail 로고](assets/img/email/startmail.svg#only-light){ align=right }
    ![StartMail 로고](assets/img/email/startmail-dark.svg#only-dark){ align=right }
    
    **StartMail**은 표준 OpenPGP 암호화를 사용하여 보안 및 프라이버시에 중점을 둔 이메일 서비스입니다. StartMail은 2014년부터 운영되었으며 본사는 네덜란드 제이스트 Boulevard 11에 위치하고 있습니다. 계정은 10GB부터 시작합니다. 30일 체험 기간을 제공합니다.
    
    [:octicons-home-16: 홈페이지](https://www.startmail.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.startmail.com/en/privacy/){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://support.startmail.com){ .card-link title=문서}
    
    ??? downloads "다운로드"
    
        - [:octicons-browser-16: Web](https://mail.startmail.com/login)

#### :material-check:{ .pg-green } 사용자 지정 도메인 및 별칭

개인 계정은 [사용자 지정](https://support.startmail.com/hc/en-us/articles/360007297457-Aliases) 별칭을 사용할 수 있습니다. [사용자 지정 도메인](https://support.startmail.com/hc/en-us/articles/4403911432209-Setup-a-custom-domain)도 사용 가능합니다.

#### :material-alert-outline:{ .pg-orange } 비공개 결제 수단

StartMail은 Visa, MasterCard, American Express, Paypal 결제를 지원합니다. [비트코인](advanced/payments.md#other-coins-bitcoin-ethereum-etc)(개인 계정 한정)이나 1년 이상 지난 계정의 SPEA 자동 이체 등 [추가 결제 옵션](https://support.startmail.com/hc/en-us/articles/360006620637-Payment-methods) 또한 지원합니다.

#### :material-check:{ .pg-green } 계정 보안

StartMail은 [웹메일에 한해](https://support.startmail.com/hc/en-us/articles/360006682158-Two-factor-authentication-2FA) TOTP 이중 인증을 지원합니다. U2F 보안 키 인증은 허용하지 않습니다.

#### :material-information-outline:{ .pg-blue } 데이터 보안

StartMail에서는 '사용자 보관함' 시스템으로 [Zero Access Encryption을 적용](https://www.startmail.com/en/whitepaper/#_Toc458527835)합니다. 사용자가 로그인할 경우 먼저 보관함이 열리고, 이메일이 보관함으로 이동하여, 보관함에서 이메일을 개인 키로 해독합니다.

StartMail은 [연락처 가져오기](https://support.startmail.com/hc/en-us/articles/360006495557-Import-contacts)를 지원합니다. 하지만 연락처는 웹메일에서만 접근 가능하며, [CalDAV](https://en.wikipedia.org/wiki/CalDAV) 등의 프로토콜로는 접근할 수 없습니다. 연락처는 Zero Knowledge Encryption이 적용되지 않고 저장됩니다.

#### :material-check:{ .pg-green } 이메일 암호화

StartMail은 웹메일에 [암호화 기능을 내장](https://support.startmail.com/hc/en-us/sections/360001889078-Encryption)하고 있으므로, OpenPGP 공개 키로 간편하게 암호화 메시지를 전송할 수 있습니다. 하지만 Web Key Directory 표준을 지원하지 않기 때문에 StartMail 메일함의 공개 키 검색은 쉽지 않습니다.

#### :material-information-outline:{ .pg-blue } 계정 삭제

계정이 만료되면 StartMail은 [6개월동안 3개의 단계를 걸쳐서](https://support.startmail.com/hc/en-us/articles/360006794398-Account-expiration) 계정을 영구적으로 삭제합니다.

#### :material-information-outline:{ .pg-blue } 추가 기능

StartMail은 메일 내 사진을 프록시를 통하여 가져올 수 있습니다. 원격 이미지를 허용할 경우, 메일 발신자는 당신의 IP 주소를 알 수 없습니다.

StartMail은 디지털 유산 상속 기능을 제공하지 않습니다.

### Tutanota

!!! recommendation

    ![Tutanota 로고](assets/img/email/tutanota.svg){ align=right }
    
    **Tutanota**는 암호화 적용을 통한 보안 및 프라이버시 보호에 중점을 둔 이메일 서비스입니다. Tutanota는 2011년부터 운영되고 있으며 본사는 독일 하노버에 위치하고 있습니다. 무료 플랜 계정은 1GB 저장 공간으로 시작합니다.
    
    [:octicons-home-16: 홈페이지](https://tutanota.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://tutanota.com/privacy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://tutanota.com/faq){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://tutanota.com/community/){ .card-link title=기여 }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
        - [:simple-appstore: App Store](https://apps.apple.com/app/tutanota/id922429609)
        - [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
        - [:simple-windows11: Windows](https://tutanota.com/#download)
        - [:simple-apple: macOS](https://tutanota.com/#download)
        - [:simple-linux: Linux](https://tutanota.com/#download)
        - [:octicons-browser-16: Web](https://mail.tutanota.com/)

Tutanota는 [IMAP 프로토콜](https://tutanota.com/faq/#imap)이나 외부 [이메일 클라이언트](email-clients.md)를 지원하지 않으며, Tutanota 앱에 [외부 이메일 계정](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647)을 추가하는 것도 불가능합니다. [이메일 가져오기](https://github.com/tutao/tutanota/issues/630)나 [하위 폴더](https://github.com/tutao/tutanota/issues/927)는 현재 지원되지 않지만, [개선 예정입니다](https://tutanota.com/blog/posts/kickoff-import). 이메일은 [개별적으로 혹은 폴더별로 일괄 선택](https://tutanota.com/howto#generalMail)하여 내보낼 수 있으나, 폴더가 많은 경우 불편할 수 있습니다.

#### :material-check:{ .pg-green } 사용자 지정 도메인 및 별칭

Tutanota 유료 계정은 최대 5개의 [별칭](https://tutanota.com/faq#alias) 및 사용자 지정 [도메인](https://tutanota.com/faq#custom-domain)을 사용할 수 있습니다. Tutanota는 [보조 주소(Plus 주소)](https://tutanota.com/faq#plus)를 허용하지 않지만, 사용자 지정 도메인 [Catch-all](https://tutanota.com/howto#settings-global) 기능은 지원합니다.

#### :material-information-outline:{ .pg-blue } 비공개 결제 수단

Tutanota는 신용카드, Paypal만 직접 결제할 수 있으나, Tutanota와 Proxystore의 [파트너십](https://tutanota.com/faq/#cryptocurrency)을 이용해 [암호화폐](cryptocurrency.md)로 기프트 카드 구입이 가능합니다.

#### :material-check:{ .pg-green } 계정 보안

Tutanota는 TOTP/U2F [이중 인증](https://tutanota.com/faq#2fa)을 지원합니다.

#### :material-check:{ .pg-green } 데이터 보안

Tutanota는 이메일, [주소록 연락처](https://tutanota.com/faq#encrypted-address-book), [캘린더](https://tutanota.com/faq#calendar)에 [Zero Access Encryption을 적용하고 있습니다](https://tutanota.com/faq#what-encrypted). 즉, 계정에 저장된 메시지 및 기타 데이터는 사용자 본인만 읽을 수 있습니다.

#### :material-information-outline:{ .pg-blue } 이메일 암호화

Tutanota는 [OpenPGP를 사용하지 않습니다](https://www.tutanota.com/faq/#pgp). Tutanota 계정이 Tutanota 외의 이메일 계정으로부터 암호화된 이메일을 받는 것은 [임시 Tutanota 메일함](https://www.tutanota.com/howto/#encrypted-email-external)을 통해 전송된 경우에만 가능합니다.

#### :material-information-outline:{ .pg-blue } 계정 삭제

Tutanota는 6개월동안 [아무 활동이 없는 무료 계정들을 삭제](https://tutanota.com/faq#inactive-accounts)합니다. 돈을 지불하면 비활성화된 계정을 재사용할 수 있습니다.

#### :material-information-outline:{ .pg-blue } 추가 기능

Tutanota는 [비영리 단체에게 Tutanota 비즈니스 버전을](https://tutanota.com/blog/posts/secure-email-for-non-profit) 무료 혹은 대폭 할인된 가격으로 제공합니다.

Tutanota에는 [Secure Connect](https://tutanota.com/secure-connect/)라는 비즈니스 기능 또한 존재합니다. 이는 고객의 비즈니스 연락에 E2EE 적용을 보장합니다. 해당 기능의 가격은 연간 240유로입니다.

Tutanota는 디지털 유산 상속 기능을 제공하지 않습니다.

## 이메일 별칭 서비스

이메일 별칭 서비스를 이용하면 가입하는 모든 웹사이트마다 새로운 이메일 주소를 생성해 사용하는 것이 가능합니다. 생성한 이메일 별칭으로 오는 메시지는 모두 여러분이 선택한 이메일 주소로 전달됩니다. 따라서 여러분이 "주로" 사용하는 이메일 주소를 드러내지 않을 수 있고, 여러분이 사용하는 이메일 제공 업체가 무엇인지도 숨길 수 있습니다. 사용자명+[어떤 문자열]@example.com 형태로 이메일 별칭을 생성하는 서비스가 대다수지만, 이 경우 웹사이트나 광고 업체 혹은 추적 네트워크에서 + 기호 뒤의 문자열을 지우기만 하면 여러분의 실제 이메일 주소를 알아낼 수 있으므로, 이런 형태 대신 완전한 이메일 별칭을 만드는 것이 훨씬 낫습니다.

<div class="grid cards" markdown>

- ![AnonAddy 로고](assets/img/email/anonaddy.svg#only-light){ .twemoji }![AnonAddy logo](assets/img/email/anonaddy-dark.svg#only-dark){ .twemoji } [AnonAddy](email.md#anonaddy)
- ![SimpleLogin 로고](assets/img/email/simplelogin.svg){ .twemoji } [SimpleLogin](email.md#simplelogin)

</div>

이메일 별칭은 이메일 제공 업체가 운영을 중단하는 경우를 대비한 안전장치 역할을 할 수도 있습니다. 이메일 제공 업체가 운영을 중단한 경우, 이메일 별칭의 전달 주소를 새로운 이메일 주소로 바꾸기만 하면 됩니다. 단, 이는 이메일 별칭 서비스가 계속 운영될 것이라는 신뢰 또한 필요로 합니다.

이메일 별칭 전용 서비스를 사용할 경우 사용자 정의 도메인에서 Catch-all 별칭보다 유리한 점이 있습니다:

- 별칭은 필요할 때 개별적으로 켜고 끌 수 있어 웹사이트가 무차별적으로 이메일을 보내는 걸 방지할 수 있습니다.
- 답장 시 실제 이메일 주소가 드러내지 않고 별칭 주소에서 전송됩니다.

'임시 이메일' 서비스에 비해서도 여러 이점이 있습니다.

- 이메일 별칭은 영구적이며, 비밀번호 재설정 등의 이메일을 받아야 하는 경우 다시 활성화할 수 있습니다.
- 이메일을 이메일 별칭 서비스 제공 업체에서 저장하는 것이 아닌, 여러분이 신뢰하는 메일함으로 전송됩니다.
- 임시 이메일 서비스는 일반적으로 누군가 주소를 알고만 있다면 접근 가능한 공개 메일함이 존재합니다. 반면 이메일 별칭은 비공개로, 여러분만 볼 수 있습니다.

Privacy Guides 권장 이메일 별칭 제공 업체는 해당 업체에서 관리하는 도메인을 이용한 이메일 별칭 생성 서비스를 제공하며, 소정의 연간 요금으로 여러분이 보유한 도메인을 이용할 수도 있습니다. 가능한 한 많은 통제권을 원하는 경우 자체 호스팅할 수도 있습니다. 단, 사용자 정의 도메인을 사용할 경우에는 프라이버시 면에서 단점이 생길 수 있습니다. 해당 사용자 정의 도메인을 사용하는 사람이 한 명뿐일 경우, 이메일 주소에서 @ 기호 앞부분을 무시하고 도메인 이름만으로도 해당 사람을 특정 웹사이트의 경계 밖에서도 쉽게 추적 가능해집니다.

'이메일 별칭 서비스를 사용한다'라는 것은, 암호화되지 않은 메시지를 다룰 땐 이메일 제공 업체와 이메일 별칭 서비스 제공 업체를 모두 신뢰해야 함을 의미합니다. 일부 제공 업체는 수신 이메일을 최종 메일함 제공 업체에 도달하기 전에 자동으로 PGP 암호화는 방식을 통해 신뢰해야 할 개체의 수를 둘에서 하나로 줄이는 식으로 해당 문제를 어느 정도 완화하기도 합니다.

### AnonAddy

!!! recommendation

    ![AnonAddy 로고](assets/img/email/anonaddy.svg#only-light){ align=right }
    ![AnonAddy 로고](assets/img/email/anonaddy-dark.svg#only-dark){ align=right }
    
    **AnonAddy**는 공통 도메인에 20개까지 도메인 별칭 생성을 무료로 제공하며, 익명성이 떨어지는 'Standard' 별칭은 무제한으로 생성 가능합니다.
    
    [:octicons-home-16: 홈페이지](https://anonaddy.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://anonaddy.com/privacy/){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://app.anonaddy.com/docs/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/anonaddy){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://anonaddy.com/donate/){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-android: Android](https://anonaddy.com/faq/#is-there-an-android-app)
        - [:material-apple-ios: iOS](https://anonaddy.com/faq/#is-there-an-ios-app)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/en-GB/firefox/addon/anonaddy/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/anonaddy-anonymous-email/iadbdpnoknmbdeolbapdackdcogdmjpe)

AnonAddy에서 생성 가능한 공통 도메인 별칭(공통 도메인은 @anonaddy.me 으로 끝나는 형태입니다) 개수는 무료 플랜의 경우 20개, 연간 $12 플랜의 경우 50개입니다. Standard 별칭(@[사용자명].anonaddy.com으로 끝나는 형태이거나, 유료 플랜은 사용자 정의 도메인)은 무제한으로 만들 수 있습니다. 하지만 앞서 언급했듯, 도메인 이름만 보고도 해당 Standard 별칭 사용자를 연결 지을 수 있기 때문에 프라이버시 면에서는 해로울 수 있습니다. 무제한 공통 도메인 별칭은 연간 $36로 이용할 수 있습니다.

주요 무료 기능:

- [x] 20개의 공통 도메인 별칭
- [x] 무제한 Standard 별칭
- [ ] 발신 답장 불가능
- [x] 2개의 수신자 메일함
- [x] 자동 PGP 암호화

### SimpleLogin

!!! recommendation

    ![Simplelogin 로고](assets/img/email/simplelogin.svg){ align=right }
    
    **SimpleLogin**는 여러 공통 도메인 이름에 이메일 별칭을 제공하는 무료 서비스입니다. 유료 기능으로는 무제한 별칭 및 사용자 지정 도메인을 사용할 수 있습니다.
    
    [:octicons-home-16: 홈페이지](https://simplelogin.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://simplelogin.io/privacy/){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://simplelogin.io/docs/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/simple-login){ .card-link title="소스 코드" }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
        - [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/en-US/firefox/addon/simplelogin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
        - [:simple-safari: Safari](https://apps.apple.com/app/id1494051017)

SimpleLogin은 [2022년 4월 8일자로 Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces)에 인수되었습니다. Proton Mail을 주로 사용하고 계신다면 SimpleLogin은 훌륭한 선택입니다. 이제 두 제품 모두 동일한 회사에서 소유하고 있으므로, 신뢰해야 할 업체의 개수가 하나로 줄어듭니다. SimpleLogin은 향후 Proton 제품과 더욱 긴밀하게 통합될 것으로 기대하고 있습니다. SimpleLogin은 사용자가 선택한 어떤 이메일 제공업체든 계속 전달을 지원합니다. SimpleLogin은 2022년 초 Securitum으로부터 [감사받았으며](https://simplelogin.io/blog/security-audit/), 제기된 모든 문제는 [해결되었습니다](https://simplelogin.io/audit2022/web.pdf).

Proton 계정과 SimpleLogin 계정 연결은 설정에서 가능합니다. Proton Unlimited, Business, Visionary 플랜을 이용 중이라면 SimpleLogin 프리미엄도 무료로 제공됩니다.

주요 무료 기능:

- [x] 10개의 공통 도메인 별칭
- [x] 무제한 답장
- [x] 1개의 수신자 메일함

## 자체 호스팅 이메일

고급 시스템 관리자는 자체 이메일 서버를 구축하는 것도 고려할 수 있습니다. 메일 서버는 보안과 메일 전달 역할을 신뢰성 있고 안정적으로 유지하기 위해 지속적인 주의 및 유지 관리가 필요합니다.

### 통합 소프트웨어 솔루션

!!! recommendation

    ![Mailcow 로고](assets/img/email/mailcow.svg){ align=right }
    
    **Mailcow**는 Linux 사용 경험이 많은 분에게 적합한 고급 메일 서버입니다. DKIM 지원 메일 서버, 안티바이러스, 스팸 모니터링, SOGo 웹메일 및 ActiveSync, 이중 인증 지원 웹 기반 관리 등 필요한 모든 것을 Docker 컨테이너에 갖추고 있습니다.
    
    [:octicons-home-16: 홈페이지](https://mailcow.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailcow.github.io/mailcow-dockerized-docs/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://www.servercow.de/mailcow?lang=en#sal){ .card-link title=기여 }

!!! recommendation

    ![Mail-in-a-Box 로고](assets/img/email/mail-in-a-box.svg){ align=right }
    
    **Mail-in-a-Box**는 Ubuntu 위에 메일 서버를 배포하는 자동화 설정 스크립트입니다. 사람들이 자신만의 메일 서버를 쉽게 구축할 수 있도록 만드는 것을 목표로 하는 프로젝트입니다.
    
    [:octicons-home-16: 홈페이지](https://mailinabox.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="소스 코드" }

보다 수동적인 접근 방식을 찾으신다면 다음 두 아티클을 추천드립니다:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd/) (2019)
- [How To Run Your Own Mail Server](https://www.c0ffee.net/blog/mail-server-guide/) (August 2017)

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 제공 업체와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 이메일 제공 업체 평가 기준에는 업계 모범 사례, 최신 기술 사용 여부 등이 포함됩니다. 특정 이메일 제공 업체를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

### 기술

안전하고 최적화된 서비스를 제공하기 위해서는 이러한 기능이 중요하다고 판단했습니다. 제공 업체가 여러분에게 필요한 기능을 갖추고 있는지 살펴봐야 합니다.

**최소 요구 사항:**

- Zero Access Encryption을 통해 이메일 계정 데이터를 암호화해야 합니다.
- [RFC5322](https://datatracker.ietf.org/doc/rfc5322/) 표준을 사용해 [Mbox](https://en.wikipedia.org/wiki/Mbox) 혹은 개별 .eml 내보내기 기능을 지원해야 합니다.
- 사용자가 자신의 [도메인 이름](https://en.wikipedia.org/wiki/Domain_name)을 사용할 수 있어야 합니다. Custom domain names are important to users because it allows them to maintain their agency from the service, should it turn bad or be acquired by another company which doesn't prioritize privacy.
- 자체 인프라에서 운영되어야 합니다. 다른 이메일 서비스 제공 업체의 인프라를 기반으로 만들어진 서비스여선 안 됩니다.

**우대 사항:**

- Zero Access Encryption을 통해 모든 계정 데이터(연락처, 캘린더 등)를 암호화해야 합니다.
- 웹메일에 E2EE/PGP 암호화가 통합되어 있어서 편리하게 사용할 수 있어야 합니다.
- Support for [WKD](https://wiki.gnupg.org/WKD) to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key by typing: `gpg --locate-key example_user@example.com`
- 외부 사용자를 위해 임시 메일함을 지원해야 합니다. 수신자에게 실제 사본을 보내지 않고 암호화된 이메일을 보내고자 할 때 유용합니다. 이러한 이메일은 보통 수명이 제한돼 있으며 이후 자동으로 삭제됩니다. 수신자가 OpenPGP 등의 암호화를 설정할 필요가 없습니다.
- [Onion 서비스](https://en.wikipedia.org/wiki/.onion)를 통해 이메일 서비스를 이용할 수 있어야 합니다.
- [Subaddressing](https://en.wikipedia.org/wiki/Email_address#Subaddressing) support.
- Catch-all or alias functionality for those who own their own domains.
- Use of standard email access protocols such as IMAP, SMTP or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.

### 프라이버시

We prefer our recommended providers to collect as little data as possible.

**최소 요구 사항:**

- 발신자의 IP 주소를 보호해야 합니다. `Received` 헤더 필드에 표시되지 않도록 필터링해야 합니다.
- 사용자 이름과 비밀번호 외에 개인 식별 정보(PII, Personally Identifiable Information)를 요구하지 않아야 합니다.
- 프라이버시 정책은 GDPR에서 정의한 요구 사항을 충족해야 합니다.
- [ECPA](https://en.wikipedia.org/wiki/Electronic_Communications_Privacy_Act#Criticism)가 [아직 개정되지 않았기 때문에](https://epic.org/ecpa/), 미국에서 호스트되어서는 안 됩니다.

**우대 사항:**

- [익명 결제 수단](advanced/payments.md)([암호 화폐](cryptocurrency.md), 현금, 기프트 카드 등)을 지원해야 합니다.

### 보안

Email servers deal with a lot of very sensitive data. We expect that providers will adopt best industry practices in order to protect their members.

**최소 요구 사항:**

- 웹메일은 2FA(TOTP 등)로 보호되어야 합니다.
- Zero access encryption, builds on encryption at rest. The provider does not have the decryption keys to the data they hold. This prevents a rogue employee leaking data they have access to or remote adversary from releasing data they have stolen by gaining unauthorized access to the server.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions)를 지원해야 합니다.
- [Hardenize](https://www.hardenize.com/), [testssl.sh](https://testssl.sh/), [Qualys SSL Labs](https://www.ssllabs.com/ssltest) 등의 툴로 분석했을 때 TLS 에러나 취약점이 없어야 합니다. 여기에는 [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security))으로 이어진 것과 같은 인증서 관련 오류 및 DH 파라미터도 포함됩니다.
- A server suite preference (optional on TLSv1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- A valid [MTA-STS](https://tools.ietf.org/html/rfc8461) and [TLS-RPT](https://tools.ietf.org/html/rfc8460) policy.
- Valid [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) records.
- Valid [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) and [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) records.
- Have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. If DMARC authentication is being used, the policy must be set to `reject` or `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996/).
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) submission, assuming SMTP is used.
- Website security standards such as:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subresource Integrity](https://en.wikipedia.org/wiki/Subresource_Integrity) if loading things from external domains.
- Must support viewing of [Message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**우대 사항:**

- Support for hardware authentication, i.e. U2F and [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn). U2F and WebAuthn are more secure as they use a private key stored on a client-side hardware device to authenticate people, as opposed to a shared secret that is stored on the web server and on the client side when using TOTP. Furthermore, U2F and WebAuthn are more resistant to phishing as their authentication response is based on the authenticated [domain name](https://en.wikipedia.org/wiki/Domain_name).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in addition to DANE support.
- Implementation of [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), this is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Bug-bounty programs and/or a coordinated vulnerability-disclosure process.
- Website security standards such as:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163/)

### 신뢰

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? We require our recommended providers to be public about their ownership or leadership. We also would like to see frequent transparency reports, especially in regard to how government requests are handled.

**최소 요구 사항:**

- Public-facing leadership or ownership.

**우대 사항:**

- Public-facing leadership.
- 투명성 보고서를 자주 발간해야 합니다.

### 마케팅

Privacy Guides는 권장 이메일 제공 업체가 책임감 있는 마케팅을 할 것을 기대하고 있습니다.

**최소 요구 사항:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.). The provider's site must also comply with [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) for those who wish to opt-out.

다음과 같은 무책임한 마케팅은 일절 없어야 합니다:

- "절대 뚫리지 않는 암호화" 등의 주장을 해선 안 됩니다. 암호화는 미래에 해당 암호화를 무력화할 수 있는 기술이 등장할 수 있다는 것을 항상 염두에 두고 사용해야 합니다.
- "100% 익명성 보장" When someone makes a claim that something is 100% it means there is no certainty for failure. We know people can quite easily deanonymize themselves in a number of ways, e.g.:

- Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
- [브라우저 핑거프린팅 시도](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**우대 사항:**

- 명확하고 읽기 쉬운 문서를 제공해야 합니다. 2FA/이메일 클라이언트/OpenPGP 설정 방법 안내 등을 포함합니다.

### 추가 기능

엄격하게 적용한 요구 사항은 아니지만, 이 외의 편의성/프라이버시 요소 일부 또한 고려하여 권장 제공 업체를 결정했습니다.
