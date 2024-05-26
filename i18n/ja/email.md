---
meta_title: "暗号化プライベートメールのおすすめ - Privacy Guides"
title: "メールサービス"
icon: material/email
description: これらの電子メールプロバイダはメールを安全に保存するのに最適な場所で、多くは他のプロバイダと相互運用可能なOpenPGP暗号化を提供しています。
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<!-- markdownlint-disable MD024 -->
実質的に、電子メールはどんなオンラインサービスを使うにも必要ですが、個人間での会話にはお勧めしません。 他人との連絡には電子メールを使うよりも、前方秘匿性のあるインスタントメッセンジャの使用を検討してください。

[おすすめのインスタントメッセンジャー](real-time-communication.md ""){.md-button}

## 推奨するサービスプロバイダー

それ以外にも、持続可能なビジネスモデル、組み込まれたセキュリティーとプライバシー機能に基づき、様々な電子メールプロバイダーを推奨します。 詳細については、[基準の完全なリスト](#criteria)をお読みください。

| Provider                    | OpenPGP / WKD                          | IMAP / SMTP                                                | Zero Access Encryption                               | Anonymous Payments            |
| --------------------------- | -------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------- | ----------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Paid plans only | :material-check:{ .pg-green }                        | 現金                            |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                              | :material-information-outline:{ .pg-blue } Mail only | 現金                            |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                        | Monero & Cash via third-party |

In addition to (or instead of) an email provider recommended here, you may wish to consider a dedicated [email aliasing service](email-aliasing.md) to protect your privacy. Among other things, these services can help protect your real inbox from spam, prevent marketers from correlating your accounts, and encrypt all incoming messages with PGP.

- [More Information :material-arrow-right-drop-circle:](email-aliasing.md)

## OpenPGP対応サービス

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic E2EE emails. 例えば、Proton MailのユーザはMailbox.orgのユーザにE2EEメッセージを送れますし、OpenPGPで暗号化された通知を、それをサポートするインターネットサービスから受け取ることができます。

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

![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** は、プライバシー、暗号化、セキュリティ、使いやすさを重視したメールサービスです。 2013年から運営をされています。 Proton AGはスイスのジュネーブに拠点を置いています。 The Proton Mail Free plan comes with 500MB of Mail storage, which you can increase up to 1GB for free.

[:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

無料アカウントには本文の検索ができないことや、 [推奨されるデスクトップメールクライアント](email-clients.md) (Thunderbirdなど)を使用するために必要な [Proton Mail Bridge](https://proton.me/mail/bridge) を利用できないといった制限があります。 有料アカウントにはProton Mail Bridge、追加ストレージ、カスタムドメインのサポートなどの機能が含まれています。 [Securitum](https://research.securitum.com)により2021年11月9日 [監査証明書](https://proton.me/blog/security-audit-all-proton-apps) がProton Mailアプリにおくられました。

If you have the Proton Unlimited, Business, Family, or Visionary plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

Proton Mail has internal crash reports that are **not** shared with third parties. This can be disabled in the web app: :gear: → **All Settings** → **Account** → **Security and privacy** → **Privacy and data collection**.

#### :material-check:{ .pg-green } カスタムドメインとエイリアス

Proton Mailの有料会員は独自ドメインでサービスや [キャッチオール](https://proton.me/support/catch-all) アドレスを使うことができます。 Proton Mail also supports [sub-addressing](https://proton.me/support/creating-aliases), which is useful for people who don't want to purchase a domain.

#### :material-check:{ .pg-green } プライベートな支払い方法

Proton Mailは標準的なクレジット・デビットカード、 [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) 、またPayPalでの支払いに加え、現金の郵送も [受け付けています](https://proton.me/support/payment-options) 。

#### :material-check:{ .pg-green } アカウントのセキュリティ

Proton Mailは TOTP [二要素認証](https://proton.me/support/two-factor-authentication-2fa) およびFIDO2またはU2F規格を使用した [ハードウェアセキュリティキー](https://proton.me/support/2fa-security-key) をサポートしています。 ハードウェアセキュリティキーを使用するには、先にTOTP二要素認証の設定が必要です。

#### :material-check:{ .pg-green } データのセキュリティ

Proton Mailはメールと [カレンダー](https://proton.me/news/protoncalendar-security-model) を [ゼロアクセス暗号化](https://proton.me/blog/zero-access-encryption) します。 ゼロアクセス暗号化で保護されたデータにアクセスできるのはあなただけです。

ディスプレイネームやメールアドレスなど、 [Proton Contacts](https://proton.me/support/proton-contacts) に保存される一部の情報はゼロアクセス暗号化によって保護されていません。 電話番号など、ゼロアクセス暗号化をサポートするContactフィールドには南京錠のアイコンが表示されます。

#### :material-check:{ .pg-green } メールの暗号化

Proton Mailはwebメールに [OpenPGP暗号化を組み込んでいます。](https://proton.me/support/how-to-use-pgp) 他のProton Mailアカウントへのメールは自動的に暗号化され、OpenPGPキーによる非Proton Mailアドレスへの暗号化はアカウント設定から簡単に有効化できます。 Proton also supports automatic external key discovery with [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This means that emails sent to other providers which use WKD will be automatically encrypted with OpenPGP as well, without the need to manually exchange public PGP keys with your contacts. They also allow you to [encrypt messages to non-Proton Mail addresses without OpenPGP](https://proton.me/support/password-protected-emails), without the need for them to sign up for a Proton Mail account.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. これにより、Proton Mailを使っていない人でも、Proton MailアカウントのOpenPGPキーを簡単に見つけることができ、プロバイダをまたいだE2EEが可能になります。 This only applies to email addresses ending in one of Proton's own domains, like @proton.me. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } アカウントの停止

有料アカウントを持っており、しかし14日を過ぎても [請求への支払いが無い](https://proton.me/support/delinquency) 場合、データにアクセスできなくなります。 30日を過ぎるとアカウントは滞納者となり、受信メールは届かなくなります。 この期間も請求は継続されます。 Proton will [delete inactive free accounts](https://proton.me/support/inactive-accounts) after one year. You **cannot** reuse the email address of a deactivated account.

#### :material-information-outline:{ .pg-blue } 追加機能

Proton Mail's [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) plan also enables access to other Proton services in addition to providing multiple custom domains, unlimited hide-my-email aliases, and 500GB of storage.

Proton Mailにはデジタル遺産の機能はありません。

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** は安全、広告なし、プライベートでいることを重視した、100%エコエネルギーで運営されているメールサービスです。 2014年から運営をされています。 Mailbox.orgはドイツのベルリンに拠点を置いています。 Accounts start with up to 2GB storage, which can be upgraded as needed.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } カスタムドメインとエイリアス

Mailbox.org lets you use your own domain, and they support [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) addresses. Mailbox.org also supports [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green } プライベートな支払い方法

Mailbox.orgは決済プロセッサBitPayがドイツでの業務を停止したために暗号通貨を受け付けていません。 However, they do accept cash by mail, cash payment to bank account, bank transfer, credit card, PayPal and couple of German-specific processors: paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } アカウントのセキュリティ

Mailbox.org supports [two factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. You can use either TOTP or a [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via the [YubiCloud](https://yubico.com/products/services-software/yubicloud). [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) などのウェブ標準はまだサポートされていません。

#### :material-information-outline:{ .pg-blue } データのセキュリティ

Mailbox.org allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). 新しいメッセージを受信するとすぐにあなたの公開鍵で暗号化されます。

However, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. その情報については、 [スタンドアロンオプション](calendar.md) の方が適切であるかもしれません。

#### :material-check:{ .pg-green } メールの暗号化

Mailbox.org has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox.org's servers. この機能はリモートの受信者がOpenPGPを持っておらず、自分のメールボックスにあるメールのコピーを複合できない場合に便利です。

Mailbox.orgは [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) からHTTP経由で公開鍵を発見することもサポートしています。 これにより、Mailbox.orgを使っていない人でも、Mailbox.orgアカウントのOpenPGPキーを簡単に見つけることができ、プロバイダをまたいだE2EEが可能になります。 This only applies to email addresses ending in one of Mailbox.org's own domains, like @mailbox.org. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } アカウントの停止

Your account will be set to a restricted user account when your contract ends. It will be irrevocably deleted after [30 days](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } 追加機能

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). ただし .onionサービスからwebメールのインターフェイスにアクセスすることはできず、TLS証明書のエラーが発生する可能性があります。

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox.orgはIMAPやPOP3のような標準的なアクセスプロトコルに加え、 [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) もサポートしています。

Mailbox.orgの全てのプランにはデジタル遺産機能があります。 相続人が申請し、遺言書を提出することを条件に、自分のデータを相続人に渡すかどうかを選択することができます。 または、名前と住所で人を指名することもできます。

## その他のプロバイダ

これらのプロバイダーは、あなたの電子メールをゼロ知識暗号化で保存するため、電子メールを安全に保つのに最適なオプションです。 ただし、異なるプロバイダー間のE2EE通信では、相互運用可能な暗号化規格がサポートされていません。

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since **2011** and is based in Hanover, Germany. Free accounts start with 1GB of storage.

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:simple-windows11: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta doesn't support the [IMAP protocol](https://tuta.com/support#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/support#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } カスタムドメインとエイリアス

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/support#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/support#plus), but you can use a [catch-all](https://tuta.com/support#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } プライベートな支払い方法

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green } アカウントのセキュリティ

Tuta supports [two factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } データのセキュリティ

Tuta has [zero access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). This means the messages and other data stored in your account are only readable by you.

#### :material-information-outline:{ .pg-blue } メールの暗号化

Tutaは[OpenPGPを使用していません](https://tuta.com/support/#pgp)。 Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } アカウントの停止

Tuta will [delete inactive free accounts](https://tuta.com/support#inactive-accounts) after six months. 料金を払えば、停止された無料アカウントを再利用できます。

#### :material-information-outline:{ .pg-blue } 追加機能

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/secure-email-for-non-profit) for free or with a heavy discount.

Tutaにはデジタルレガシー機能はありません。

## セルフホストメール

Advanced system administrators may consider setting up their own email server. Mail servers require attention and continuous maintenance in order to keep things secure and mail delivery reliable.

### Combined software solutions

<div class="admonition recommendation" markdown>

![Mailcow logo](assets/img/email/mailcow.svg){ align=right }

**Mailcow** is a more advanced mail server perfect for those with a bit more Linux experience. It has everything you need in a Docker container: A mail server with DKIM support, antivirus and spam monitoring, webmail and ActiveSync with SOGo, and web-based administration with 2FA support.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

</div>

<div class="admonition recommendation" markdown>

![Mail-in-a-Box logo](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** is an automated setup script for deploying a mail server on Ubuntu. Its goal is to make it easier for people to set up their own mail server.

[:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }

</div>

For a more manual approach we've picked out these two articles:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://c0ffee.net/blog/mail-server-guide) (August 2017)

## 規準

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an email provider, and conduct your own research to ensure the email provider you choose is the right choice for you.

### テクノロジー

We regard these features as important in order to provide a safe and optimal service. You should consider whether the provider which has the features you require.

**最低条件：**

- Encrypts email account data at rest with zero-access encryption.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Custom domain names are important to users because it allows them to maintain their agency from the service, should it turn bad or be acquired by another company which doesn't prioritize privacy.
- Operates on owned infrastructure, i.e. not built upon third-party email service providers.

**満たされることが望ましい基準：**

- Encrypts all account data (Contacts, Calendars, etc.) at rest with zero-access encryption.
- Integrated webmail E2EE/PGP encryption provided as a convenience.
- Support for [WKD](https://wiki.gnupg.org/WKD) to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key by typing: `gpg --locate-key example_user@example.com`
- Support for a temporary mailbox for external users. This is useful when you want to send an encrypted email, without sending an actual copy to your recipient. These emails usually have a limited lifespan and then are automatically deleted. They also don't require the recipient to configure any cryptography like OpenPGP.
- Availability of the email provider's services via an [onion service](https://en.wikipedia.org/wiki/.onion).
- [Sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing) support.
- Catch-all or alias functionality for those who own their own domains.
- Use of standard email access protocols such as IMAP, SMTP or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.

### プライバシー

私たちは、推奨するサービスプロバイダーができるだけデータを収集しないことを望んでいます。

**最低条件：**

- 送信者IPアドレスを保護している。 `Received`ヘッダーフィールドに表示されないようフィルターしている。
- ユーザー名とパスワード以外に、個人情報(PII)を必要としない。
- プライバシーポリシーがGDPRの要件を満たしている。

**満たされることが望ましい基準：**

- [匿名の支払い方法](advanced/payments.md)（[暗号通貨](cryptocurrency.md)、現金、ギフトカードなど）を受け入れること
- 強固な電子メールのプライバシー保護法の管轄区域でホストされていること

### セキュリティー

メールサーバーは、非常に機密性の高いデータを大量に扱います。 私たちは、プロバイダーがユーザーを保護するために最も優れた業界の慣行を採用することを期待します。

**最低条件：**

- TOTPなどの二要素認証によるウェブメールの保護。
- Zero access encryption, builds on encryption at rest. The provider does not have the decryption keys to the data they hold. This prevents a rogue employee leaking data they have access to or remote adversary from releasing data they have stolen by gaining unauthorized access to the server.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions)のサポート。
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLSv1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- 有効な [MTA-STS](https://tools.ietf.org/html/rfc8461) および [TLS-RPT](https://tools.ietf.org/html/rfc8460) ポリシー。
- 有効な[DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities)レコード。
- 有効な[SPF](https://ja.wikipedia.org/wiki/Sender_Policy_Framework)および[DKIM](https://ja.wikipedia.org/wiki/DKIM)レコード。
- Have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. If DMARC authentication is being used, the policy must be set to `reject` or `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) submission, assuming SMTP is used.
- 以下のようなウェブサイトのセキュリティ基準：
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subresource Integrity](https://en.wikipedia.org/wiki/Subresource_Integrity) if loading things from external domains.
- Must support viewing of [Message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**満たされることが望ましい基準：**

- ハードウェア認証のサポート、つまり U2Fと[WebAuthn](https://en.wikipedia.org/wiki/WebAuthn)。 U2F and WebAuthn are more secure as they use a private key stored on a client-side hardware device to authenticate people, as opposed to a shared secret that is stored on the web server and on the client side when using TOTP. Furthermore, U2F and WebAuthn are more resistant to phishing as their authentication response is based on the authenticated [domain name](https://en.wikipedia.org/wiki/Domain_name).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in addition to DANE support.
- Implementation of [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), this is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- バグ報奨金プログラム、協調的な脆弱性開示プロセス。
- 以下のようなウェブサイトのセキュリティ基準：
    - [コンテンツセキュリティポリシー（CSP）](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### 信頼

あなたは偽の身分証を持つ人物に自分の財政を託すことはないでしょう。電子メールに関しても、同じことが言えるはずです。 推奨されるサービスプロバイダーには、自社の所有権やリーダーシップについて公表することが求められます。 また、特に政府からの要請がどのように処理されるかについて、透明性の高い報告が頻繁に行われることを望んでいます。

**最低条件：**

- 公的なリーダーシップまたはオーナーシップ。

**満たされることが望ましい基準：**

- 公的なリーダーシップ。
- 頻繁な透明性レポート。

### マーケティング

私たちが推奨する電子メールプロバイダーには、責任あるマーケティングを求めます。

**最低条件：**

- アナリティクスを自己でホストすること（つまり、GoogleアナリティクスやAdobe Analyticsなどは不可）。 プロバイダーのサイトは、オプトアウトを希望するユーザーのために[DNT（Do Not Track）](https://en.wikipedia.org/wiki/Do_Not_Track)に準拠しなければなりません。

無責任なマーケティングを行わないこと。

- 「破れない暗号化」という主張。 暗号化は、その暗号化を破る技術が将来になって現れた際には、それがもはや秘密ではなくなってしまうかもしれないということを念頭に置いて使用されるべきものです。
- 匿名性を100％保証するという主張。 誰かが何かを100％だと主張するとき、それは失敗の確実性が全く存在しないということを意味します。 私たちは、人々が以下のような多くの方法で簡単に匿名化を解除できることを知っています。

    - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
    - [ブラウザーのフィンガープリンティングを行うこと。](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**満たされることが望ましい基準：**

- 明確で読みやすいドキュメント。 これには、2FAの設定、電子メールクライアント、OpenPGPなどが含まれます。

### 追加機能

厳密な要件ではありませんが、推奨するサービスプロバイダーを決定する際に考慮した利便性やプライバシーの要素が他にもいくつかあります。
