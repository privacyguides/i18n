---
meta_title: "비공개 암호화 이메일 서비스 권장 목록 - Privacy Guides"
title: "이메일 서비스"
icon: material/email
description: These email providers offer a great place to store your emails securely, and many offer interoperable OpenPGP encryption with other providers.
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

Proton Unlimited, Businiess, Visionary 플랜을 이용 중이라면 [SimpleLogin](#simplelogin) 프리미엄도 무료로 제공됩니다.

Proton Mail에는 내부 충돌 보고서가 존재하며, 이는 제3자와 공유되지 **않습니다**. 충돌 보고서는 비활성화 가능합니다: **Settings** > **Go to Settings** > **Account** > **Security and privacy** > **Send crash reports**.

#### :material-check:{ .pg-green } 사용자 지정 도메인 및 별칭

Proton Mail 유료 이용자는 서비스에서 자신의 도메인을 사용하거나 [Catch-all](https://proton.me/support/catch-all) 주소를 사용할 수 있습니다. 도메인을 자신이 직접 구매하지 않더라도, Proton Mail이 지원하는 [보조 주소](https://proton.me/support/creating-aliases)를 유용하게 사용할 수 있습니다.

#### :material-check:{ .pg-green } 비공개 결제 수단

Proton Mail은 일반 신용/직불 카드, [비트코인](advanced/payments.md#other-coins-bitcoin-ethereum-etc), Paypal, 현금 우편 결제를 [지원합니다](https://proton.me/support/payment-options).

#### :material-check:{ .pg-green } 계정 보안

Proton Mail은 TOTP [이중 인증](https://proton.me/support/two-factor-authentication-2fa), FIDO2/U2F 표준 [하드웨어 보안 키](https://proton.me/support/2fa-security-key)를 지원합니다. 하드웨어 보안 키를 사용하려면 먼저 TOTP 이중 인증을 설정해야 합니다.

#### :material-check:{ .pg-green } 데이터 보안

Proton Mail has [zero-access encryption](https://proton.me/blog/zero-access-encryption) at rest for your emails and [calendars](https://proton.me/news/protoncalendar-security-model). Data secured with zero-access encryption is only accessible by you.

Certain information stored in [Proton Contacts](https://proton.me/support/proton-contacts), such as display names and email addresses, are not secured with zero-access encryption. Contact fields that support zero-access encryption, such as phone numbers, are indicated with a padlock icon.

#### :material-check:{ .pg-green } 이메일 암호화

Proton Mail has [integrated OpenPGP encryption](https://proton.me/support/how-to-use-pgp) in their webmail. Emails to other Proton Mail accounts are encrypted automatically, and encryption to non-Proton Mail addresses with an OpenPGP key can be enabled easily in your account settings. They also allow you to [encrypt messages to non-Proton Mail addresses](https://proton.me/support/password-protected-emails) without the need for them to sign up for a Proton Mail account or use software like OpenPGP.

Proton Mail also supports the discovery of public keys via HTTP from their [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This allows people who don't use Proton Mail to find the OpenPGP keys of Proton Mail accounts easily, for cross-provider E2EE.


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

StartMail has [zero access encryption at rest](https://www.startmail.com/en/whitepaper/#_Toc458527835), using their "user vault" system. When you log in, the vault is opened, and the email is then moved to the vault out of the queue where it is decrypted by the corresponding private key.

StartMail supports importing [contacts](https://support.startmail.com/hc/en-us/articles/360006495557-Import-contacts) however, they are only accessible in the webmail and not through protocols such as [CalDAV](https://en.wikipedia.org/wiki/CalDAV). Contacts are also not stored using zero knowledge encryption.

#### :material-check:{ .pg-green } 이메일 암호화

StartMail has [integrated encryption](https://support.startmail.com/hc/en-us/sections/360001889078-Encryption) in their webmail, which simplifies sending encrypted messages with public OpenPGP keys. However, they do not support the Web Key Directory standard, making the discovery of a Startmail mailbox's public key more challenging for other email providers or clients.

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

Tutanota는 신용카드, Paypal만 직접 결제할 수 있으나, Tutanota와 Proxystore의 [파트너십](https://tutanota.com/faq/#cryptocurrency)을 이용해 [암호화폐](cryptocurrency.md)로 기프트카드 구입이 가능합니다.

#### :material-check:{ .pg-green } 계정 보안

Tutanota는 TOTP/U2F [이중 인증](https://tutanota.com/faq#2fa)을 지원합니다.

#### :material-check:{ .pg-green } 데이터 보안

Tutanota has [zero access encryption at rest](https://tutanota.com/faq#what-encrypted) for your emails, [address book contacts](https://tutanota.com/faq#encrypted-address-book), and [calendars](https://tutanota.com/faq#calendar). This means the messages and other data stored in your account are only readable by you.

#### :material-information-outline:{ .pg-blue } 이메일 암호화

Tutanota는 [OpenPGP를 사용하지 않습니다](https://www.tutanota.com/faq/#pgp). Tutanota 계정이 Tutanota 외의 이메일 계정으로부터 암호화된 이메일을 받는 것은 [임시 Tutanota 메일함](https://www.tutanota.com/howto/#encrypted-email-external)을 통해 전송된 경우에만 가능합니다.

#### :material-information-outline:{ .pg-blue } 계정 삭제

Tutanota는 6개월동안 [아무 활동이 없는 무료 계정들을 삭제](https://tutanota.com/faq#inactive-accounts)합니다. 돈을 지불하면 비활성화된 계정을 재사용할 수 있습니다.

#### :material-information-outline:{ .pg-blue } 추가 기능

Tutanota는 [비영리 단체에게 Tutanota 비즈니스 버전을](https://tutanota.com/blog/posts/secure-email-for-non-profit) 무료 혹은 대폭 할인된 가격으로 제공합니다.

Tutanota에는 [Secure Connect](https://tutanota.com/secure-connect/)라는 비즈니스 기능 또한 존재합니다. 이는 고객의 비즈니스 연락에 E2EE 적용을 보장합니다. 해당 기능의 가격은 연간 240유로입니다.

Tutanota는 디지털 유산 상속 기능을 제공하지 않습니다.

## 이메일 별칭 서비스

An email aliasing service allows you to easily generate a new email address for every website you register for. The email aliases you generate are then forwarded to an email address of your choosing, hiding both your "main" email address and the identity of your email provider. True email aliasing is better than plus addressing commonly used and supported by many providers, which allows you to create aliases like yourname+[anythinghere]@example.com, because websites, advertisers, and tracking networks can trivially remove anything after the + sign to know your true email address.

<div class="grid cards" markdown>

- ![AnonAddy logo](assets/img/email/anonaddy.svg#only-light){ .twemoji }![AnonAddy logo](assets/img/email/anonaddy-dark.svg#only-dark){ .twemoji } [AnonAddy](email.md#anonaddy)
- ![SimpleLogin logo](assets/img/email/simplelogin.svg){ .twemoji } [SimpleLogin](email.md#simplelogin)

</div>

Email aliasing can act as a safeguard in case your email provider ever ceases operation. In that scenario, you can easily re-route your aliases to a new email address. In turn, however, you are placing trust in the aliasing service to continue functioning.

Using a dedicated email aliasing service also has a number of benefits over a catch-all alias on a custom domain:

- Aliases can be turned on and off individually when you need them, preventing websites from emailing you randomly.
- Replies are sent from the alias address, shielding your real email address.

They also have a number of benefits over "temporary email" services:

- Aliases are permanent and can be turned on again if you need to receive something like a password reset.
- Emails are sent to your trusted mailbox rather than stored by the alias provider.
- Temporary email services typically have public mailboxes which can be accessed by anyone who knows the address, aliases are private to you.

Our email aliasing recommendations are providers that allow you to create aliases on domains they control, as well as your own custom domain(s) for a modest yearly fee. They can also be self-hosted if you want maximum control. However, using a custom domain can have privacy-related drawbacks: If you are the only person using your custom domain, your actions can be easily tracked across websites simply by looking at the domain name in the email address and ignoring everything before the at (@) sign.

Using an aliasing service requires trusting both your email provider and your aliasing provider with your unencrypted messages. Some providers mitigate this slightly with automatic PGP encryption, which reduces the number of parties you need to trust from two to one by encrypting incoming emails before they are delivered to your final mailbox provider.

### AnonAddy

!!! recommendation

    ![AnonAddy logo](assets/img/email/anonaddy.svg#only-light){ align=right }
    ![AnonAddy logo](assets/img/email/anonaddy-dark.svg#only-dark){ align=right }
    **AnonAddy**에서는 무료로 공유 도메인을 사용하면 최대 20개의 별칭을, 익명성이 떨어지는 "기본" 별칭을 사용하면 별칭을 무제한으로 생성할 수 있습니다.
    
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

The number of shared aliases (which end in a shared domain like @anonaddy.me) that you can create is limited to 20 on AnonAddy's free plan and 50 on their $12/year plan. You can create unlimited standard aliases (which end in a domain like @[username].anonaddy.com or a custom domain on paid plans), however, as previously mentioned, this can be detrimental to privacy because people can trivially tie your standard aliases together based on the domain name alone. Unlimited shared aliases are available for $36/year.

주요 무료 기능:

- [x] 20개의 공유 별칭
- [x] 무제한 기본 별칭
- [] 발신 답장 불가
- [x] 2개의 수신자 메일함
- [x] 자동 PGP 암호화

### SimpleLogin

!!! recommendation

    ![Simplelogin logo](assets/img/email/simplelogin.svg){ align=right }
    
    **SimpleLogin** is a free service which provides email aliases on a variety of shared domain names, and optionally provides paid features like unlimited aliases and custom domains.
    
    [:octicons-home-16: Homepage](https://simplelogin.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://simplelogin.io/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://simplelogin.io/docs/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/simple-login){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
        - [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/en-US/firefox/addon/simplelogin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
        - [:simple-safari: Safari](https://apps.apple.com/app/id1494051017)

SimpleLogin was [acquired by Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) as of April 8, 2022. If you use Proton Mail for your primary mailbox, SimpleLogin is a great choice. As both products are now owned by the same company you now only have to trust a single entity. We also expect that SimpleLogin will be more tightly integrated with Proton's offerings in the future. SimpleLogin continues to support forwarding to any email provider of your choosing. Securitum [audited](https://simplelogin.io/blog/security-audit/) SimpleLogin in early 2022 and all issues [were addressed](https://simplelogin.io/audit2022/web.pdf).

You can link your SimpleLogin account in the settings with your Proton account. If you have the Proton Unlimited, Business, or Visionary Plan, you will have SimpleLogin Premium for free.

Notable free features:

- [x] 10 Shared Aliases
- [x] Unlimited Replies
- [x] 1 Recipient Mailbox

## Self-Hosting Email

Advanced system administrators may consider setting up their own email server. Mail servers require attention and continuous maintenance in order to keep things secure and mail delivery reliable.

### Combined software solutions

!!! recommendation

    ![Mailcow logo](assets/img/email/mailcow.svg){ align=right }
    
    **Mailcow** is a more advanced mail server perfect for those with a bit more Linux experience. It has everything you need in a Docker container: A mail server with DKIM support, antivirus and spam monitoring, webmail and ActiveSync with SOGo, and web-based administration with 2FA support.
    
    [:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailcow.github.io/mailcow-dockerized-docs/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

!!! recommendation

    ![Mail-in-a-Box logo](assets/img/email/mail-in-a-box.svg){ align=right }
    
    **Mail-in-a-Box** is an automated setup script for deploying a mail server on Ubuntu. Its goal is to make it easier for people to set up their own mail server.
    
    [:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }

For a more manual approach we've picked out these two articles:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd/) (2019)
- [How To Run Your Own Mail Server](https://www.c0ffee.net/blog/mail-server-guide/) (August 2017)

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 제공 업체와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 이메일 제공 업체 평가 기준에는 업계 모범 사례, 최신 기술 사용 여부 등이 포함됩니다. 특정 이메일 제공 업체를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

### 기술

We regard these features as important in order to provide a safe and optimal service. 제공 업체가 여러분에게 필요한 기능을 갖추고 있는지 살펴봐야 합니다.

**최소 요구 사항:**

- Encrypts email account data at rest with zero-access encryption.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322/) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Custom domain names are important to users because it allows them to maintain their agency from the service, should it turn bad or be acquired by another company which doesn't prioritize privacy.
- Operates on owned infrastructure, i.e. not built upon third-party email service providers.

**우대 사항:**

- Encrypts all account data (Contacts, Calendars, etc.) at rest with zero-access encryption.
- Integrated webmail E2EE/PGP encryption provided as a convenience.
- Support for [WKD](https://wiki.gnupg.org/WKD) to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key by typing: `gpg --locate-key example_user@example.com`
- Support for a temporary mailbox for external users. This is useful when you want to send an encrypted email, without sending an actual copy to your recipient. These emails usually have a limited lifespan and then are automatically deleted. They also don't require the recipient to configure any cryptography like OpenPGP.
- Availability of the email provider's services via an [onion service](https://en.wikipedia.org/wiki/.onion).
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
