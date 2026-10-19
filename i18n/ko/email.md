---
meta_title: "암호화된 프라이버시 이메일 서비스 추천 - 프라이버시 가이드"
title: 이메일 서비스
icon: material/email
description: 이러한 이메일 제공업체는 이메일을 안전하게 보관하기에 좋은 곳이며, 상당수가 다른 제공업체와 상호 운용되는 OpenPGP 암호화를 제공합니다.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-server-network: 서비스 제공업체](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

이메일은 거의 모든 온라인 서비스를 이용하는 데 필수적이지만, 개인 간 대화 수단으로는 권장하지 않습니다. 다른 사람에게 연락할 때는 이메일 대신 순방향 비밀성을 지원하는 인스턴트 메신저를 사용하는 것을 고려해 보세요.

[추천 인스턴트 메신저](real-time-communication.md ""){.md-button}

## 추천 제공업체

그 밖의 용도에는 지속 가능한 비즈니스 모델과 기본 제공 보안 및 프라이버시 기능을 갖춘 다양한 이메일 제공업체를 추천합니다. 자세한 사항은 [전체 평가 기준](#criteria)을 참고해 주세요.

| 제공업체                     | OpenPGP / WKD                          | IMAP / SMTP                                          | 저장 데이터 암호화                                       | 익명 결제 수단                         |
| ------------------------ | -------------------------------------- | ---------------------------------------------------- | ------------------------------------------------ | -------------------------------- |
| [프로톤 메일](#proton-mail)   | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } 유료 요금제 한정 | :material-check:{ .pg-green }                    | 현금 <br>제3자를 통한 모네로         |
| [메일박스 메일](#mailbox-mail) | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                        | :material-information-outline:{ .pg-blue } 메일 한정 | 현금                               |
| [투타](#tuta)              | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }               | :material-check:{ .pg-green }                    | 제3자를 통한 모네로 <br>제3자를 통한 현금 |

여기에서 추천하는 이메일 제공업체와 함께(또는 대신) 프라이버시를 보호하기 위해 전용 [이메일 별칭 서비스](email-aliasing.md#recommended-providers)를 고려해 볼 수 있습니다. 이러한 서비스는 무엇보다도 실제 받은편지함을 스팸으로부터 보호하고, 마케터가 여러분의 계정들을 서로 연관 짓지 못하게 하며, 수신되는 모든 메시지를 PGP로 암호화하는 데 도움이 됩니다.

- [추가 정보 :material-arrow-right-drop-circle:](email-aliasing.md)

## OpenPGP 호환 서비스

이러한 제공업체는 OpenPGP 암호화/복호화와 [웹 키 디렉터리(WKD) 표준](basics/email-security.md#what-is-the-web-key-directory-standard)을 기본으로 지원하므로, 제공업체에 관계없이 종단 간 암호화된 이메일을 주고받을 수 있습니다. 예를 들어 프로톤 메일 사용자는 메일박스 메일 사용자에게 E2EE 메시지를 보낼 수 있고, 이를 지원하는 인터넷 서비스로부터 OpenPGP로 암호화된 알림을 받을 수도 있습니다.

<div class="grid cards" markdown>

- ![프로톤 메일 로고](assets/img/email/protonmail.svg){ .twemoji } [프로톤 메일](#proton-mail)
- ![메일박스 메일 로고](assets/img/email/mailbox-mail.svg){ .twemoji } [메일박스 메일](#mailbox-mail)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

OpenPGP와 같은 E2EE 기술을 사용하더라도 이메일 헤더에는 암호화되지 않는 일부 메타데이터가 남습니다. 여기에는 일반적으로 제목도 포함됩니다! [이메일 메타데이터](basics/email-security.md#email-metadata-overview)에 관해 더 알아보세요.

또한 OpenPGP는 순방향 비밀성을 지원하지 않습니다. 따라서 여러분이나 메시지 수신자의 개인 키가 도난당하면, 그 키로 암호화된 이전 메시지가 모두 노출됩니다.

- [개인 키를 어떻게 보호할 수 있나요?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### 프로톤 메일

<div class="admonition recommendation" markdown>

![프로톤 메일 로고](assets/img/email/protonmail.svg){ align=right }

**프로톤 메일**은 프라이버시, 암호화, 보안, 사용 편의성에 중점을 둔 이메일 서비스입니다. 2013년부터 운영되어 왔습니다. 프로톤 AG는 스위스 제네바에 본사를 두고 있습니다.

프로톤 무료 요금제는 500MB의 메일 저장 공간을 제공하며, 무료로 최대 1GB까지 늘릴 수 있습니다.

[:octicons-home-16: 홈페이지](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="어니언 서비스" }
[:octicons-eye-16:](https://proton.me/mail/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id979659905)
- [:simple-github: 깃허브](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: 윈도우](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: 리눅스](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: 웹](https://mail.proton.me)

</details>

</div>

무료 계정에는 본문 검색을 할 수 없고, 썬더버드 같은 [추천 데스크톱 이메일 클라이언트](email-clients.md)를 사용하는 데 필요한 [프로톤 메일 브리지](https://proton.me/mail/bridge)를 이용할 수 없는 등 몇 가지 제한이 있습니다. 유료 계정에는 프로톤 메일 브리지, 추가 저장 공간, 사용자 지정 도메인 지원 등의 기능이 포함됩니다. 프로톤 언리미티드 요금제 또는 프로톤의 다중 사용자 요금제에는 [심플로그인](email-aliasing.md#simplelogin) 프리미엄 이용권이 포함됩니다.

2021년 11월, [시큐리텀](https://research.securitum.com)이 프로톤 메일 앱에 대한 [보안 증명서](https://res.cloudinary.com/dbulfrlrz/images/v1714639878/wp-pme/letter-of-attestation-proton-mail-20211109_3138714c61/letter-of-attestation-proton-mail-20211109_3138714c61.pdf)를 발급했습니다.

프로톤 메일에는 내부 충돌 보고 기능이 있으며, 이 보고서는 제3자와 공유되지 **않고** 비활성화할 수도 있습니다.

=== "웹"

    받은편지함에서 :gear: → **모든 설정** → **계정** → **보안 및 프라이버시** → **프라이버시 및 데이터 수집**을 선택합니다.

    - [ ] **사용 진단 정보 수집** 비활성화
    - [ ] **충돌 보고서 전송** 비활성화

=== "모바일"

    받은편지함에서 :material-menu: → :gear: **설정** → 사용자 이름을 선택합니다.

    - [ ] **충돌 보고서 전송** 비활성화
    - [ ] **사용 진단 정보 수집** 비활성화

#### :material-check:{ .pg-green } 사용자 지정 도메인 및 별칭

프로톤 메일 유료 가입자는 서비스에서 자신의 도메인을 사용하거나 [캐치올](https://proton.me/support/catch-all) 주소를 사용할 수 있습니다. 프로톤 메일은 [하위 주소 지정(sub-addressing)](https://proton.me/support/creating-aliases)도 지원하므로, 도메인을 구매하고 싶지 않은 사람에게 유용합니다.

#### :material-check:{ .pg-green } 비공개 결제 수단

프로톤 메일은 일반적인 신용카드/직불카드, [비트코인](advanced/payments.md#other-coins-bitcoin-ethereum-etc), 페이팔 결제 외에도 우편으로 보내는 **현금**을 [받습니다](https://proton.me/support/payment-options). 또한 프로톤의 [공식](https://discuss.privacyguides.net/t/add-monero-as-an-anonymous-payment-method-for-proton-services/31058/15) 재판매업체인 [프록시스토어](https://dys2p.com/en/2025-09-09-proton.html)를 통해 [**모네로**](cryptocurrency.md#monero)로 프로톤 메일 플러스 또는 프로톤 언리미티드 바우처를 구매할 수도 있습니다.

#### :material-check:{ .pg-green } 계정 보안

프로톤 메일은 TOTP [2단계 인증](https://proton.me/support/two-factor-authentication-2fa)과 FIDO2 또는 U2F 표준을 사용하는 [하드웨어 보안 키](https://proton.me/support/2fa-security-key)를 지원합니다. 하드웨어 보안 키를 사용하려면 먼저 TOTP 2단계 인증을 설정해야 합니다.

#### :material-check:{ .pg-green } 데이터 보안

프로톤 메일은 [이메일](https://proton.me/blog/zero-access-encryption)과 [캘린더](https://proton.me/news/protoncalendar-security-model)를 저장할 때 PGP 기반 저장 데이터 암호화를 적용합니다. 나중에 해당 데이터에 접근하는 데 필요한 복호화 키는 사용자만 보유합니다.

[프로톤 연락처](https://proton.me/support/proton-contacts)에 저장되는 표시 이름과 이메일 주소 등의 일부 정보는 사용자의 암호화 키로 보호되지 **않으므로**, 프로톤이 해당 정보를 읽을 수 있습니다. 전화번호처럼 사용자 본인의 암호화 키로 보호되는 연락처 항목에는 자물쇠 아이콘이 표시됩니다.

#### :material-check:{ .pg-green } 이메일 암호화

프로톤 메일은 웹메일에 [OpenPGP 암호화 기능을 내장](https://proton.me/support/how-to-use-pgp)하고 있습니다. 다른 프로톤 메일 계정으로 보내는 이메일은 자동으로 암호화되며, 프로톤 메일 외 주소로 보내는 이메일에 대한 OpenPGP 암호화는 계정 설정에서 간편하게 활성화할 수 있습니다. 프로톤은 WKD를 이용한 외부 공개 키의 자동 검색도 지원합니다. 따라서 WKD를 사용하는 다른 제공업체로 이메일을 보낼 때도 연락처와 PGP 공개 키를 수동으로 교환하지 않고 OpenPGP로 자동 암호화할 수 있습니다. 또한 상대방이 프로톤 메일 계정에 가입하지 않아도 [OpenPGP 없이 프로톤 메일 이외의 주소로 암호화된 메시지를 보낼 수 있습니다](https://proton.me/support/password-protected-emails).

프로톤 메일은 WKD를 통해 HTTP로 프로톤 계정의 공개 키도 게시합니다. 덕분에 프로톤 메일을 사용하지 않는 사람도 제공업체 간 E2EE 통신을 위해 프로톤 메일 계정의 OpenPGP 키를 쉽게 찾을 수 있습니다. 이 기능은 `@proton.me`처럼 프로톤이 소유한 도메인으로 끝나는 이메일 주소에만 적용됩니다. 사용자 지정 도메인을 사용한다면 [WKD를 별도로 설정](basics/email-security.md#what-is-the-web-key-directory-standard)해야 합니다.

#### :material-information-outline:{ .pg-blue } 계정 해지

유료 계정의 [요금이 14일 이상 미납](https://proton.me/support/delinquency)되면 데이터에 접근할 수 없게 됩니다. 30일이 지나면 계정은 연체 상태가 되며, 더 이상 메일을 수신할 수 없습니다. 이 기간 동안에도 계속해서 요금이 청구됩니다. 프로톤은 1년 동안 활동이 없는 무료 계정을 [삭제합니다](https://proton.me/support/inactive-accounts). 비활성화된 계정의 이메일 주소는 다시 사용할 수 **없습니다**.

#### :material-information-outline:{ .pg-blue } 추가 기능

프로톤 메일의 [언리미티드](https://proton.me/support/proton-plans#proton-unlimited) 요금제는 여러 개의 사용자 지정 도메인, 무제한 이메일 숨기기 별칭, 500GB 저장 공간을 제공하며 다른 프로톤 서비스도 이용할 수 있게 합니다.

### 메일박스 메일

<div class="admonition recommendation" markdown>

![메일박스 메일 로고](assets/img/email/mailbox-mail.svg){ align=right }

**메일박스 메일**(구 *Mailbox.org*)은 보안과 광고 없는 이용 환경에 중점을 두며, 에너지를 100% 친환경 방식으로 공급받는 이메일 서비스입니다. 2014년부터 운영되어 왔습니다. 메일박스 메일은 독일 베를린에 본사를 두고 있습니다.

계정은 최대 2GB의 저장 공간으로 시작하며, 필요에 따라 업그레이드할 수 있습니다.

[:octicons-home-16: 홈페이지](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="문서" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:octicons-browser-16: 웹](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } 사용자 지정 도메인 및 별칭

메일박스 메일에서는 자신의 도메인을 사용할 수 있으며, [캐치올](https://kb.mailbox.org/en/private/custom-domains/use-your-own-domain-with-catch-all/) 주소도 지원합니다. 메일박스 메일은 [하위 주소 지정(sub-addressing)](https://kb.mailbox.org/en/private/e-mail/what-is-an-alias-and-how-do-i-use-it/)도 지원하므로, 별도 도메인을 구매하지 않으려는 사용자에게 유용합니다.

#### :material-check:{ .pg-green } 비공개 결제 수단

메일박스 메일은 결제 처리 업체인 비트페이가 독일에서 운영을 중단한 이후 어떤 암호화폐도 받지 않습니다. 하지만 우편으로 보내는 **현금**, 은행 계좌로의 **현금** 입금, 은행 송금, 신용카드, 페이팔, 그리고 독일 전용 결제 서비스 두 가지(Paydirekt, Sofortüberweisung)는 받습니다.

#### :material-check:{ .pg-green } 계정 보안

메일박스 메일은 웹메일에서만 [2단계 인증](https://kb.mailbox.org/en/private/security-and-privacy/how-to-use-two-factor-authentication-2fa/)을 지원합니다. [유비클라우드](https://yubico.com/products/services-software/yubicloud)를 통해 TOTP 또는 [유비키](security-keys.md#yubikey)를 사용할 수 있습니다. [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online)과 같은 웹 표준은 아직 지원되지 않습니다.

#### :material-information-outline:{ .pg-blue } 데이터 보안

메일박스 메일은 [암호화된 사서함](https://kb.mailbox.org/en/private/encryption/your-encrypted-mailbox/) 기능으로 수신 메일을 암호화할 수 있습니다. 그러면 새로 받는 메시지는 즉시 여러분의 공개 키로 암호화됩니다.

하지만 메일박스 메일이 사용하는 소프트웨어 플랫폼인 [오픈익스체인지](https://en.wikipedia.org/wiki/Open-Xchange)는 주소록과 캘린더 암호화를 [지원하지 않습니다](https://kb.mailbox.org/en/business/security-privacy-article/encryption-of-calendar-and-address-book/). 이 데이터에는 [별도의 서비스](calendar.md)를 사용하는 편이 더 적합할 수 있습니다.

#### :material-check:{ .pg-green } 이메일 암호화

메일박스 메일은 웹메일에 [통합 암호화 기능](https://kb.mailbox.org/en/private/encryption/how-can-e-mails-be-encrypted-with-pgp/)을 제공하여 OpenPGP 공개 키를 가진 사람에게 메시지를 쉽게 보낼 수 있습니다. 또한 원격 수신자가 메일박스 메일 서버에서 [이메일을 복호화](https://kb.mailbox.org/en/private/encryption/my-recipient-does-not-use-pgp/)할 수 있도록 해 줍니다. 이 기능은 원격 수신자에게 OpenPGP가 없어 자신의 메일함에서 이메일 사본을 복호화할 수 없을 때 유용합니다.

메일박스 메일은 WKD를 통해 HTTP로 공개 키를 검색하는 기능도 지원합니다. 따라서 메일박스 메일 외부의 사용자도 제공업체 간 E2EE 통신을 위해 메일박스 메일 계정의 OpenPGP 키를 쉽게 찾을 수 있습니다. 이 기능은 `@mailbox.org`처럼 메일박스 메일이 소유한 도메인으로 끝나는 이메일 주소에만 적용됩니다. 사용자 지정 도메인을 사용한다면 [WKD를 별도로 설정](basics/email-security.md#what-is-the-web-key-directory-standard)해야 합니다.

#### :material-information-outline:{ .pg-blue } 계정 해지

계약이 종료되면 계정은 기능이 제한된 사용자 계정으로 전환됩니다. [30일](https://kb.mailbox.org/en/en/private/account/reactivate-a-deleted-account/)이 지나면 계정은 복구할 수 없도록 삭제됩니다.

#### :material-information-outline:{ .pg-blue } 추가 기능

메일박스 메일의 [.onion 서비스](https://kb.mailbox.org/en/en/private/security-privacy/using-the-tor-exit-node-from-mailbox/)를 통해 IMAP/SMTP로 계정에 접속할 수 있습니다. 하지만 웹메일 인터페이스는 .onion 서비스를 통해 이용할 수 없으며, TLS 인증서 오류가 발생할 수도 있습니다.

모든 계정에는 제한된 클라우드 저장 공간이 제공되며, 해당 공간은 [암호화할 수 있습니다](https://kb.mailbox.org/en/private/drive/encrypt-files-on-your-drive/). 메일박스 메일은 [@secure.mailbox.org](https://kb.mailbox.org/en/business/e-mail-article/ensuring-e-mails-are-sent-securely/) 별칭도 제공합니다. 이 별칭을 사용하면 메일 서버 간 연결에 TLS 암호화가 적용되며, 암호화할 수 없는 경우 메시지는 아예 전송되지 않습니다. 메일박스 메일은 IMAP, POP3 같은 표준 접속 프로토콜 외에도 [익스체인지 액티브싱크](https://en.wikipedia.org/wiki/Exchange_ActiveSync)를 지원합니다.

메일박스 메일은 모든 요금제에서 디지털 유산 기능을 제공합니다. 상속인이 신청하고 여러분의 유언장을 제출하면, 어떤 데이터를 상속인에게 넘길지 선택할 수 있습니다. 또는 특정 인물을 이름과 주소로 지정할 수도 있습니다.

## 기타 제공업체

이러한 제공업체는 나중에 사용자 본인만 읽을 수 있도록 이메일을 암호화합니다. 따라서 저장된 이메일을 안전하게 보관하기에 적합합니다. 하지만 서로 다른 제공업체 간 E2EE 통신에 사용할 수 있는 상호 운용 가능한 암호화 표준은 지원하지 않습니다.

<div class="grid cards" markdown>

- ![투타 로고](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![투타 로고](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [투타](#tuta)

</div>

### 투타

<div class="admonition recommendation" markdown>

![투타 로고](assets/img/email/tuta.svg#only-light){ align=right }
![투타 로고](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**투타**(구 *투타노타*)는 암호화를 통한 보안과 프라이버시에 중점을 둔 이메일 서비스입니다. 투타는 2011년에 서비스를 시작했으며 독일 하노버에 본사를 두고 있습니다.

무료 계정에는 1GB의 저장 공간이 제공됩니다.

[:octicons-home-16: 홈페이지](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title="기여하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id922429609)
- [:simple-github: 깃허브](https://github.com/tutao/tutanota/releases)
- [:fontawesome-brands-windows: 윈도우](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: 리눅스](https://tuta.com/#download)
- [:octicons-browser-16: 웹](https://app.tuta.com)

</details>

</div>

투타는 [IMAP 프로토콜](https://tuta.com/support#imap)이나 타사 [이메일 클라이언트](email-clients.md) 사용을 지원하지 않습니다. 또한 투타 앱에 [외부 이메일 계정](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647)을 추가할 수도 없습니다. 현재 [이메일 가져오기](https://github.com/tutao/tutanota/issues/630)도 지원하지 않습니다. 다만 이 기능은 [추후 지원될 예정](https://tuta.com/blog/kickoff-import)입니다. 이메일은 폴더별로 [개별 또는 일괄 선택](https://tuta.com/support#generalMail)으로 내보낼 수 있어, 폴더가 많다면 불편할 수 있습니다.

#### :material-check:{ .pg-green } 사용자 지정 도메인 및 별칭

유료 투타 계정은 요금제에 따라 별칭을 15개 또는 30개까지 사용할 수 있으며, [사용자 지정 도메인](https://tuta.com/support#custom-domain)에서는 별칭을 무제한으로 사용할 수 있습니다. 투타는 [하위 주소 지정(플러스 주소)](https://tuta.com/support#plus)을 지원하지 않지만, 사용자 지정 도메인에서는 [캐치올](https://tuta.com/support#settings-global)을 사용할 수 있습니다.

#### :material-information-outline:{ .pg-blue } 비공개 결제 수단

투타는 신용카드와 페이팔만 직접 받지만, 프록시스토어와의 [제휴](https://tuta.com/support/#cryptocurrency)를 통해 [**암호화폐**](cryptocurrency.md)로 기프트 카드를 구매할 수 있습니다.

#### :material-check:{ .pg-green } 계정 보안

투타는 TOTP 또는 U2F를 통한 [2단계 인증](https://tuta.com/support#2fa)을 지원합니다.

#### :material-check:{ .pg-green } 데이터 보안

투타는 [이메일](https://tuta.com/support#what-encrypted), [주소록 연락처](https://tuta.com/support#encrypted-address-book), [캘린더](https://tuta.com/support#calendar)를 강력한 암호화로 보호하며, 복호화 키는 사용자만 보유합니다. 즉, 데이터가 계정에 저장된 뒤에는 사용자 본인 외에는 누구도 메시지나 기타 데이터를 읽을 수 없습니다.

#### :material-information-outline:{ .pg-blue } 이메일 암호화

투타는 [OpenPGP를 사용하지 않습니다](https://tuta.com/support/#pgp). 투타 계정은 [임시 투타 메일함](https://tuta.com/support/#encrypted-email-external)을 통해 전송된 경우에만 투타 이외의 이메일 계정에서 암호화된 이메일을 받을 수 있습니다.

#### :material-information-outline:{ .pg-blue } 계정 해지

투타는 6개월 동안 활동이 없는 무료 계정을 [삭제합니다](https://tuta.com/support#inactive-accounts). 비활성화된 무료 계정은 요금을 지불하면 다시 사용할 수 있습니다.

#### :material-information-outline:{ .pg-blue } 추가 기능

투타는 [비영리 단체에 투타 비즈니스 버전](https://tuta.com/blog/secure-email-for-non-profit)을 무료로 제공하거나 큰 폭의 할인을 적용합니다.

## 평가 기준

**저희는 추천하는 제공업체 중 어느 곳과도 제휴 관계가 없다는 점을 알려 드립니다.** [일반 평가 기준](about/criteria.md) 외에도, 추천을 받고자 하는 이메일 제공업체를 위해 업계 모범 사례 도입, 최신 기술 등을 포함한 명확한 요구 사항을 마련했습니다. 이메일 제공업체를 선택하기 전에 이 목록을 숙지하고, 선택한 이메일 제공업체가 자신에게 맞는 선택인지 직접 조사해 보시기 바랍니다.

### 기술

저희는 안전하고 최적의 서비스를 제공하기 위해 이러한 기능이 중요하다고 생각합니다. 해당 제공업체가 여러분에게 필요한 기능을 갖추고 있는지 살펴봐야 합니다.

**최소 요구 사항:**

- 이메일 계정 데이터를 저장 시 비대칭 암호화로 암호화해야 하며, 복호화에 필요한 개인 키는 사용자만 보유해야 합니다.
- [Mbox](https://en.wikipedia.org/wiki/Mbox) 형식 또는 [RFC 5322](https://datatracker.ietf.org/doc/rfc5322) 표준을 따르는 개별 .EML 파일로 이메일을 내보낼 수 있어야 합니다.
- 자체 소유 인프라에서 운영되어야 합니다. 즉, 타사 이메일 서비스 제공업체를 기반으로 구축되어서는 안 됩니다.

**이상적인 경우:**

- 모든 계정 데이터(연락처, 캘린더 등)를 저장 시 비대칭 암호화로 암호화하고, 복호화에 필요한 개인 키는 사용자만 보유하는 것이 좋습니다.
- 편의를 위해 웹메일에 E2EE/PGP 암호화를 통합 제공하는 것이 좋습니다.
- HTTP를 통해 OpenPGP 공개 키를 더 쉽게 찾을 수 있도록 WKD를 지원하는 것이 좋습니다. GnuPG 사용자는 다음 명령으로 키를 가져올 수 있습니다: `gpg --locate-key example_user@example.com`.
- 외부 사용자를 위한 임시 메일함을 지원하는 것이 좋습니다. 수신자에게 실제 사본을 보내지 않고 암호화된 이메일을 보내려는 경우에 유용합니다. 이러한 이메일은 보통 보존 기간이 제한되어 있어 기간이 지나면 자동으로 삭제됩니다. 또한 수신자가 OpenPGP 같은 암호화를 설정할 필요가 없습니다.
- [하위 주소 지정](https://en.wikipedia.org/wiki/Email_address#Sub-addressing)을 지원하는 것이 좋습니다.
- 사용자가 자신의 [도메인 이름](https://en.wikipedia.org/wiki/Domain_name)을 사용할 수 있도록 하는 것이 좋습니다. 사용자 지정 도메인 이름은 서비스가 나빠지거나 프라이버시를 우선시하지 않는 다른 회사에 인수되더라도 사용자가 서비스에 종속되지 않고 주도권을 유지할 수 있게 해 주므로 중요합니다.
- 자체 도메인을 사용하는 사용자를 위해 캐치올 또는 별칭 기능을 제공하는 것이 좋습니다.
- IMAP, SMTP, [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol) 같은 표준 이메일 접속 프로토콜을 사용하는 것이 좋습니다. 표준 접속 프로토콜을 지원하면 사용자가 다른 제공업체로 옮기고 싶을 때 모든 이메일을 쉽게 내려받을 수 있습니다.
- 이메일 제공업체의 서비스를 [어니언 서비스](https://en.wikipedia.org/wiki/.onion)로도 이용할 수 있는 것이 좋습니다.

### 프라이버시

추천 제공업체는 데이터를 가능한 한 적게 수집하는 것이 바람직합니다.

**최소 요구 사항:**

- 발신자의 IP 주소를 보호해야 하며, 이를 위해 `Received` 헤더 필드에 IP 주소가 표시되지 않도록 필터링할 수 있습니다.
- 사용자 이름과 비밀번호 외에 개인 식별 정보(PII)를 요구해서는 안 됩니다.
- 개인정보 처리방침은 GDPR에서 정의한 요건을 충족해야 합니다.

**이상적인 경우:**

- [익명 결제 수단](advanced/payments.md)([암호화폐](cryptocurrency.md), 현금, 기프트 카드 등)을 받는 것이 좋습니다.
- 이메일 프라이버시 보호 법률이 강력한 관할권에서 호스팅되는 것이 좋습니다.

### 보안

이메일 서버는 매우 민감한 데이터를 대량으로 처리합니다. 저희는 제공업체가 고객을 보호하기 위해 업계 모범 사례를 도입하기를 기대합니다.

**최소 요구 사항:**

- [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp) 같은 2단계 인증으로 웹메일을 보호해야 합니다.
- 저장 데이터를 암호화해야 하며, 서비스 제공업체가 보유한 데이터의 복호화 키를 갖지 않는 비대칭 암호화를 사용해야 합니다. 이렇게 하면 악의적인 직원이 접근 가능한 데이터를 유출하거나, 원격 공격자가 서버에 무단으로 접근해 훔친 데이터를 공개하는 것을 막을 수 있습니다.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions)를 지원해야 합니다.
- [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), [Qualys SSL Labs](https://ssllabs.com/ssltest) 등의 도구로 검사했을 때 TLS 오류나 취약점이 없어야 합니다. 여기에는 인증서 관련 오류와 [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)) 공격의 원인이 된 취약한 DH 매개변수 등이 포함됩니다.
- 순방향 비밀성과 인증된 암호화를 지원하는 강력한 암호 스위트를 서버가 우선 사용하도록 설정해야 합니다(TLS 1.3에서는 선택 사항).
- 유효한 [MTA-STS](https://tools.ietf.org/html/rfc8461) 및 [TLS-RPT](https://tools.ietf.org/html/rfc8460) 정책이 있어야 합니다.
- 유효한 [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) 레코드가 있어야 합니다.
- 유효한 [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) 및 [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) 레코드가 있어야 합니다.
- 올바른 [DMARC](https://en.wikipedia.org/wiki/DMARC) 레코드와 정책을 설정하거나, 인증에 [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain)를 사용해야 합니다. DMARC 인증을 사용하는 경우 정책을 `reject` 또는 `quarantine`으로 설정해야 합니다.
- 서버에서 TLS 1.2 이상을 사용하도록 설정하고, [RFC 8996](https://datatracker.ietf.org/doc/rfc8996)에 대응할 계획이 있어야 합니다.
- SMTP를 사용하는 경우 [SMTPS](https://en.wikipedia.org/wiki/SMTPS) 제출을 지원해야 합니다.
- 다음과 같은 웹사이트 보안 표준을 적용해야 합니다:
    - [HTTP 엄격 전송 보안(HSTS)](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - 외부 도메인에서 리소스를 불러오는 경우 [하위 리소스 무결성(SRI)](https://en.wikipedia.org/wiki/Subresource_Integrity)을 적용해야 합니다.
- 메시지 헤더 확인은 이메일이 피싱 시도인지 판단하는 데 중요한 포렌식 기능이므로, [메시지 헤더](https://en.wikipedia.org/wiki/Email#Message_header)를 볼 수 있어야 합니다.

**이상적인 경우:**

- 하드웨어 인증을 지원하는 것이 좋습니다. 예: U2F 및 [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- DANE 지원과 더불어 [DNS 인증 기관 권한 부여(CAA) 리소스 레코드](https://tools.ietf.org/html/rfc6844)를 갖추는 것이 좋습니다.
- 메일링 리스트에 글을 보내는 사람에게 유용한 [인증 수신 체인(ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain)([RFC 8617](https://tools.ietf.org/html/rfc8617))을 구현하는 것이 좋습니다.
- 평판 있는 제3자 업체의 보안 감사 결과를 공개하는 것이 좋습니다.
- 버그 바운티 프로그램 및/또는 조율된 취약점 공개 절차를 갖추는 것이 좋습니다.
- 다음과 같은 웹사이트 보안 표준을 적용하는 것이 좋습니다:
    - [콘텐츠 보안 정책(CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC 9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### 신뢰

가짜 신원을 가진 사람에게 재정을 맡기지 않을 텐데, 이메일을 맡길 이유가 있을까요? 추천 제공업체는 소유주 또는 경영진을 공개해야 합니다. 또한 특히 정부 요청을 어떻게 처리하는지에 관한 투명성 보고서를 자주 발행하기를 바랍니다.

**최소 요구 사항:**

- 경영진 또는 소유주를 공개해야 합니다.

**이상적인 경우:**

- 투명성 보고서를 자주 발행하는 것이 좋습니다.

### 마케팅

저희가 추천하는 이메일 제공업체는 책임감 있는 마케팅을 하기를 바랍니다.

**최소 요구 사항:**

- 분석 도구를 자체 호스팅해야 합니다(구글 애널리틱스, 어도비 애널리틱스 등 사용 불가).
- 다음을 포함한 무책임한 마케팅을 해서는 안 됩니다:
    - "깨지지 않는 암호화"라는 주장. 암호화는 나중에 이를 해독할 기술이 등장하면 더 이상 비밀이 아닐 수 있다는 점을 염두에 두고 사용해야 합니다.
    - 익명성을 100% 보호한다고 보장하는 것. 무언가가 100%라고 주장한다는 것은 실패할 가능성이 전혀 없다는 뜻입니다. 사람들은 여러 방법으로 아주 쉽게 스스로 익명성을 잃을 수 있습니다. 예를 들면 다음과 같습니다:
        - 토르 같은 익명성 소프트웨어 없이 접속했던 개인정보(예: 이메일 계정, 고유한 가명 등)를 재사용하는 것
        - [브라우저 핑거프린팅](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**이상적인 경우:**

- 2단계 인증 설정, 이메일 클라이언트, OpenPGP 등의 작업에 대해 명확하고 읽기 쉬운 문서를 제공하는 것이 좋습니다.

### 추가 기능

엄격한 요구 사항은 아니지만, 추천할 제공업체를 결정할 때 고려한 몇 가지 편의성 또는 프라이버시 관련 요소가 있습니다.
