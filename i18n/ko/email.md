---
meta_title: "비공개 암호화 이메일 서비스 권장 목록 - Privacy Guides"
title: "이메일 서비스"
icon: material/email
description: 이러한 이메일 제공 업체는 여러분의 이메일을 안전하게 보관하기에 적합합니다. 대부분이 OpenPGP 암호화를 제공하여 다른 이메일 서비스와도 호환됩니다.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protects against the following threat(s):</small>

- [:material-server-network: 서비스 제공자/제공 업체(Service Providers)](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

이메일은 모든 온라인 서비스 이용에 사실상 필수적이지만, 개인 간 대화에는 권장드리지 않습니다. 다른 사람에게 연락할 때는 이메일보다는 순방향 비밀성을 지원하는 메신저를 사용하는 것이 좋습니다.

[권장 메신저](real-time-communication.md ""){.md-button}

## 권장 제공 업체

그 외 용도로 이메일을 사용한다면, 지속 가능한 비즈니스 모델을 갖추고 보안 및 프라이버시 기능을 기본 제공하는 이메일 제공 업체를 권장합니다. 자세한 사항은 [전체 평가 기준](#criteria)을 참고해 주세요.

| 서비스 제공자                     | OpenPGP/WKD                            | IMAP / SMTP                                        | 제로 액세스 암호화                                           | 익명 결제                         |
| --------------------------- | -------------------------------------- | -------------------------------------------------- | ---------------------------------------------------- | ----------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } 유료 요금제만 | :material-check:{ .pg-green }                        | 현금                            |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                      | :material-information-outline:{ .pg-blue } Mail only | 현금                            |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }             | :material-check:{ .pg-green }                        | Monero & Cash via third-party |

In addition to (or instead of) an email provider recommended here, you may wish to consider a dedicated [email aliasing service](email-aliasing.md) to protect your privacy. Among other things, these services can help protect your real inbox from spam, prevent marketers from correlating your accounts, and encrypt all incoming messages with PGP.

- [More Information :material-arrow-right-drop-circle:](email-aliasing.md)

## OpenPGP 호환 서비스

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic E2EE emails. 예를 들어, Proton Mail 사용자는 Mailbox.org 사용자에게 E2EE 메시지를 보내거나, OpenPGP 지원 인터넷 서비스에서 OpenPGP로 암호화된 알림을 받을 수 있습니다.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

When using E2EE technology like OpenPGP your email will still have some metadata that is not encrypted in the header of the email, generally including the subject line! Read more about [email metadata](basics/email-security.md#email-metadata-overview).

OpenPGP also does not support Forward secrecy, which means if either your or the recipient's private key is ever stolen, all previous messages encrypted with it will be exposed. [How do I protect my private keys?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail 로고](assets/img/email/protonmail.svg){ align=right }

**Proton Mail**은 프라이버시, 암호화, 보안, 사용 편의성에 중점을 둔 이메일 서비스입니다. They have been in operation since 2013. Proton AG 본사는 스위스 제네바에 위치하고 있습니다. Proton Mail 무료 요금제에는 500MB의 메일 저장 용량이 제공되며, 최대 1GB까지 무료로 늘릴 수 있습니다.

[:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/mail/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

무료 계정은 본문 텍스트 검색이 불가능하고 [Proton Mail Bridge](https://proton.me/mail/bridge)(Thunderbird 등 [권장 데스크톱 이메일 클라이언트](email-clients.md)를 사용하려면 필수적인 기능)를 사용할 수 없습니다. 유료 계정에는 Proton Mail Bridge, 추가 저장 공간, 사용자 지정 도메인 지원 등의 기능이 제공됩니다. Proton Mail 앱 [감사 증명서](https://proton.me/blog/security-audit-all-proton-apps)는 2021년 11월 9일에 [Securitum](https://research.securitum.com)에서 발급하였습니다.

If you have the Proton Unlimited plan or any multi-user Proton plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

Proton Mail has internal crash reports that are **not** shared with third parties. This can be disabled in the web app: :gear: → **All Settings** → **Account** → **Security and privacy** → **Privacy and data collection**.

#### :material-check:{ .pg-green } 사용자 지정 도메인 및 별칭

Proton Mail 유료 이용자는 서비스에서 자신의 도메인을 사용하거나 [Catch-all](https://proton.me/support/catch-all) 주소를 사용할 수 있습니다. Proton Mail also supports [sub-addressing](https://proton.me/support/creating-aliases), which is useful for people who don't want to purchase a domain.

#### :material-check:{ .pg-green } 비공개 결제 수단

Proton Mail은 일반 신용/직불 카드, [비트코인](advanced/payments.md#other-coins-bitcoin-ethereum-etc), Paypal, 현금 우편 결제를 [지원합니다](https://proton.me/support/payment-options).

#### :material-check:{ .pg-green } 계정 보안

Proton Mail은 TOTP [이중 인증](https://proton.me/support/two-factor-authentication-2fa), FIDO2/U2F 표준 [하드웨어 보안 키](https://proton.me/support/2fa-security-key)를 지원합니다. 하드웨어 보안 키를 사용하려면 먼저 TOTP 이중 인증을 설정해야 합니다.

#### :material-check:{ .pg-green } 데이터 보안

Proton Mail은 이메일 및 [캘린더](https://proton.me/news/protoncalendar-security-model)에 [Zero Access Encryption](https://proton.me/blog/zero-access-encryption)을 적용하고 있습니다. Zero Access Encryption으로 보호된 데이터는 여러분 본인만 접근 가능합니다.

[Proton Contacts](https://proton.me/support/proton-contacts) 연락처에 저장된 특정 정보(표시된 이름, 이메일 주소 등)는 Zero Access Encryption으로 보호되지 않습니다. 전화번호 등, Zero Access Encrpytion이 적용된 연락처 필드는 자물쇠 아이콘으로 표시됩니다.

#### :material-check:{ .pg-green } 이메일 암호화

Proton Mail은 웹메일에 [OpenPGP 암호화 기능을 내장](https://proton.me/support/how-to-use-pgp)하고 있습니다. 다른 Proton Mail 계정으로 보내는 이메일은 자동으로 암호화되며, Proton Mail 외 주소로 보내는 이메일에 대한 OpenPGP 암호화는 계정 설정에서 간편하게 활성화할 수 있습니다. Proton also supports automatic external key discovery with [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This means that emails sent to other providers which use WKD will be automatically encrypted with OpenPGP as well, without the need to manually exchange public PGP keys with your contacts. They also allow you to [encrypt messages to non-Proton Mail addresses without OpenPGP](https://proton.me/support/password-protected-emails), without the need for them to sign up for a Proton Mail account.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. 이로써 Proton Mail을 사용하지 않는 사람도 Proton Mail OpenPGP 키를 쉽게 찾아 서로 다른 제공 업체 간 E2EE 적용이 가능합니다. This only applies to email addresses ending in one of Proton's own domains, like @proton.me. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } 계정 해지

유료 계정 사용 중에 14일 이상 요금이 [미납된 경우](https://proton.me/support/delinquency), 여러분은 더 이상 자신의 데이터에 접근할 수 없습니다. 30일이 지나면 계정은 연체 상태가 되며, 더 이상 메일을 수신할 수 없습니다. 이 기간 동안에도 계속해서 요금이 청구됩니다. Proton will [delete inactive free accounts](https://proton.me/support/inactive-accounts) after one year. You **cannot** reuse the email address of a deactivated account.

#### :material-information-outline:{ .pg-blue } 추가 기능

Proton Mail's [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) plan also enables access to other Proton services in addition to providing multiple custom domains, unlimited hide-my-email aliases, and 500GB of storage.

Proton Mail은 디지털 유산 상속 기능을 제공하지 않습니다.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org 로고](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org**는 100% 친환경 에너지로 작동되는 안전하고, 광고가 없는 비공개 중점 이메일 서비스입니다. 2014년부터 운영되었습니다. Mailbox.org 본사는 독일 베를린에 위치하고 있습니다. Accounts start with up to 2GB storage, which can be upgraded as needed.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } 사용자 지정 도메인 및 별칭

Mailbox.org는 고유 도메인을 사용할 수 있으며, [캐치올](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) 주소를 지원합니다. Mailbox.org also supports [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green } 비공개 결제 수단

Mailbox.org는 BitPay 결제 처리업체가 독일에서 운영을 중단함에 따라 어떠한 암호화폐도 받지 않습니다. However, they do accept cash by mail, cash payment to bank account, bank transfer, credit card, PayPal and couple of German-specific processors: paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } 계정 보안

Mailbox.org는 웹메일에만 [2단계 인증을](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) 지원합니다. [YubiCloud](https://yubico.com/products/services-software/yubicloud)를 통해 TOTP 또는 [YubiKey](https://en.wikipedia.org/wiki/YubiKey) 를 사용할 수 있습니다. [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) 등의 웹 표준은 아직 지원되지 않습니다.

#### :material-information-outline:{ .pg-blue } 데이터 보안

Mailbox.org allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). 새로 수신하는 메시지는 즉시 공개 키로 암호화됩니다.

However, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. 해당 데이터에 대해서는 [다른 솔루션](calendar.md)을 찾는것이 적합할 수 있습니다.

#### :material-check:{ .pg-green } 이메일 암호화

Mailbox.org has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox.org's servers. OpenPGP가 없어 수신자가 자신의 메일함에서 직접 복호화할 수 없을 경우에 이 기능을 사용할 수 있습니다.

또한, Mailbox.org는 [웹 키 디렉터리(WKD)](https://wiki.gnupg.org/WKD)에서 HTTP를 통한 공개 키 검색을 지원합니다. Mailbox.org를 사용하지 않는 사람들은 Mailbox.org 계정의 OpenPGP 공개키를 쉽게 찾을 수 있고, 플랫폼과 무관하게 종단간 암호화를 할 수 있습니다. This only applies to email addresses ending in one of Mailbox.org's own domains, like @mailbox.org. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } 계정 해지

Your account will be set to a restricted user account when your contract ends. It will be irrevocably deleted after [30 days](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } 추가 기능

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). Onion 서비스를 통한 웹메일 인터페이스 접근은 불가능하며, TLS 인증서 오류가 발생할 수 있습니다.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox.org also supports [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) in addition to standard access protocols like IMAP and POP3.

Mailbox.org는 모든 플랜에 디지털 유산 상속 기능을 제공합니다. You can choose whether you want any of your data to be passed to heirs providing that they apply and provide your testament. Alternatively, you can nominate a person by name and address.

## 그외 제공자

이 제공자들은 영지식 암호화를 사용하기에 메일을 안전하게 보관하는 용도로 좋습니다. However, they don't support interoperable encryption standards for E2EE communications between different providers.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (formerly *Tutanota*) is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since 2011 and is based in Hanover, Germany. Free accounts start with 1GB of storage.

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:fontawesome-brands-windows: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta doesn't support the [IMAP protocol](https://tuta.com/support#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/support#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } 사용자 지정 도메인 및 별칭

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/support#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/support#plus), but you can use a [catch-all](https://tuta.com/support#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } 비공개 결제 수단

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green } 계정 보안

Tuta supports [two factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } 데이터 보안

Tuta has [zero access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). 즉, 계정에 저장된 메시지 및 기타 데이터는 사용자 본인만 읽을 수 있습니다.

#### :material-information-outline:{ .pg-blue } 이메일 암호화

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } 계정 삭제

Tuta will [delete inactive free accounts](https://tuta.com/support#inactive-accounts) after six months. 돈을 지불하면 비활성화된 계정을 재사용할 수 있습니다.

#### :material-information-outline:{ .pg-blue } 추가 기능

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/secure-email-for-non-profit) for free or with a heavy discount.

Tuta doesn't offer a digital legacy feature.

## 자체 호스팅 이메일

고급 시스템 관리자는 자체 이메일 서버를 구축하는 것도 고려할 수 있습니다. 메일 서버는 보안과 메일 전달 역할을 신뢰성 있고 안정적으로 유지하기 위해 지속적인 주의 및 유지 관리가 필요합니다.

### 통합 소프트웨어 솔루션

<div class="admonition recommendation" markdown>

![Mailcow 로고](assets/img/email/mailcow.svg){ align=right }

**Mailcow**는 Linux 사용 경험이 많은 분에게 적합한 고급 메일 서버입니다. It has everything you need in a Docker container: a mail server with DKIM support, antivirus and spam monitoring, webmail and ActiveSync with SOGo, and web-based administration with 2FA support.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title="Contribute" }

</div>

<div class="admonition recommendation" markdown>

![Mail-in-a-Box 로고](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box**는 Ubuntu 위에 메일 서버를 배포하는 자동화 설정 스크립트입니다. 사람들이 자신만의 메일 서버를 쉽게 구축할 수 있도록 만드는 것을 목표로 하는 프로젝트입니다.

[:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }

</div>

보다 수동적인 접근 방식을 찾으신다면 다음 두 아티클을 추천드립니다:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://c0ffee.net/blog/mail-server-guide) (August 2017)

## 평가 기준

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an email provider, and conduct your own research to ensure the email provider you choose is the right choice for you.

### 기술

안전하고 최적화된 서비스를 제공하기 위해서는 이러한 기능이 중요하다고 판단했습니다. 제공 업체가 여러분에게 필요한 기능을 갖추고 있는지 살펴봐야 합니다.

**최소 요구 사항:**

- Zero Access Encryption을 통해 이메일 계정 데이터를 암호화해야 합니다.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- 사용자가 자신의 [도메인 이름](https://en.wikipedia.org/wiki/Domain_name)을 사용할 수 있어야 합니다. 사용자 지정 도메인 이름은 서비스가 부실해지거나 프라이버시 보호를 우선시하지 않는 다른 회사에 인수되는 경우에도 에이전시를 유지할 수 있도록 해주기 때문에 사용자에게 중요합니다.
- 자체 인프라에서 운영되어야 합니다. 다른 이메일 서비스 제공 업체의 인프라를 기반으로 만들어진 서비스여선 안 됩니다.

**우대 사항:**

- Zero Access Encryption을 통해 모든 계정 데이터(연락처, 캘린더 등)를 암호화해야 합니다.
- 웹메일에 E2EE/PGP 암호화가 통합되어 있어서 편리하게 사용할 수 있어야 합니다.
- [WKD](https://wiki.gnupg.org/WKD)를 지원하여 HTTP를 통한 공개 OpenPGP 키 검색 편의를 제공해야 합니다. GnuPG 사용자는 `gpg --locate-key example_user@example.com`를 입력하여 키를 얻을 수 있습니다.
- 외부 사용자를 위해 임시 메일함을 지원해야 합니다. 수신자에게 실제 사본을 보내지 않고 암호화된 이메일을 보내고자 할 때 유용합니다. 이러한 이메일은 보통 수명이 제한돼 있으며 이후 자동으로 삭제됩니다. 수신자가 OpenPGP 등의 암호화를 설정할 필요가 없습니다.
- [Onion 서비스](https://en.wikipedia.org/wiki/.onion)를 통해 이메일 서비스를 이용할 수 있어야 합니다.
- [하위 주소](https://en.wikipedia.org/wiki/Email_address#Sub-addressing) 지원.
- Catch-all or alias functionality for those who use their own domains.
- Use of standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). 표준 액세스 프로토콜을 사용함으로써, 사용자는 다른 서비스 제공 업체로 전환하고자 할 경우 모든 이메일을 쉽게 다운로드할 수 있습니다.

### 프라이버시

Privacy Guides이 권장하는 제공자들은 최소한의 데이터만을 수집해야 합니다.

**최소 요구 사항:**

- Protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- 사용자 이름과 비밀번호 외에 개인 식별 정보(PII, Personally Identifiable Information)를 요구하지 않아야 합니다.
- 프라이버시 정책은 GDPR에서 정의한 요구 사항을 충족해야 합니다.

**우대 사항:**

- [익명 결제 수단](advanced/payments.md)([암호 화폐](cryptocurrency.md), 현금, 기프트 카드 등)을 지원해야 합니다.
- Hosted in a jurisdiction with strong email privacy protection laws.

### 보안

이메일 서버는 매우 민감한 데이터를 대량으로 처리합니다. We expect that providers will adopt best industry practices in order to protect their customers.

**최소 요구 사항:**

- 웹메일은 2FA(TOTP 등)로 보호되어야 합니다.
- Zero access encryption, which builds on encryption at rest. The provider does not have the decryption keys to the data they hold. This prevents a rogue employee leaking data they have access to or remote adversary from releasing data they have stolen by gaining unauthorized access to the server.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions)를 지원해야 합니다.
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLSv1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- A valid [MTA-STS](https://tools.ietf.org/html/rfc8461) and [TLS-RPT](https://tools.ietf.org/html/rfc8460) policy.
- Valid [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) records.
- Valid [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) and [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) records.
- Have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. If DMARC authentication is being used, the policy must be set to `reject` or `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) submission, assuming SMTP is used.
- Website security standards such as:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subresource Integrity](https://en.wikipedia.org/wiki/Subresource_Integrity) if loading things from external domains.
- Must support viewing of [message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**우대 사항:**

- Support for hardware authentication, i.e. U2F and [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in addition to DANE support.
- Implementation of [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- 검증된 제 3자로부터 보안 감사 결과가 게시됨
- 버그 바운티 프로그램 또는 체계적인 취약점 공개 프로세스가 있음
- Website security standards such as:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### 신뢰

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? We require our recommended providers to be public about their ownership or leadership. We also would like to see frequent transparency reports, especially in regard to how government requests are handled.

**최소 요구 사항:**

- Public-facing leadership or ownership.

**우대 사항:**

- 투명성 보고서를 자주 발간해야 합니다.

### 마케팅

With the email providers we recommend, we like to see responsible marketing.

**최소 요구 사항:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.). The provider's site must also comply with [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) for those who wish to opt out.

Must not have any irresponsible marketing, which can include the following:

- "절대 뚫리지 않는 암호화" 등의 주장을 해선 안 됩니다. 암호화는 미래에 해당 암호화를 무력화할 수 있는 기술이 등장할 수 있다는 것을 항상 염두에 두고 사용해야 합니다.
- "100% 익명성 보장" 만약 누군가가 100%라고 주장한다면, 이는 절대 실패할 수 없다고 하는 것과 같습니다. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:

    - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
    - [브라우저 핑거프린팅](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**우대 사항:**

- Clear and easy to read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### 추가 기능

엄격하게 적용한 요구 사항은 아니지만, 이 외의 편의성/프라이버시 요소 일부 또한 고려하여 권장 제공 업체를 결정했습니다.
