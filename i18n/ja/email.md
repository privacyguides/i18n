---
meta_title: "暗号化プライベートメールの推奨事項 - Privacy Guides"
title: "メールサービス"
icon: material/email
description: これらの電子メールプロバイダはメールを安全に保存するのに最適な場所で、多くは他のプロバイダと相互運用可能なOpenPGP暗号化を提供しています。
cover: email.png
---

実質的に、電子メールはどんなオンラインサービスを使うにも必要ですが、個人間での会話にはお勧めしません。 他人との連絡には電子メールを使うよりも、前方秘匿性のあるインスタントメッセンジャの使用を検討してください。

[おすすめのインスタントメッセンジャ](real-time-communication.md ""){.md-button}

それ以外のことについては、持続可能なビジネスモデル、組み込まれたセキュリティとプライバシー機能に基づいて様々な電子メールプロバイダをお勧めします。

- [OpenPGP対応電子メールプロバイダ :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [その他の暗号化プロバイダ :material-arrow-right-drop-circle:](#more-providers)
- [メールエイリアスのサービス :material-arrow-right-drop-circle:](#email-aliasing-services)
- [セルフホストのオプション :material-arrow-right-drop-circle:](#self-hosting-email)

## OpenPGP対応サービス

これらのプロバイダはOpenPGPによる暗号化、復号とWeb Key Directory (WKD) 標準をネイティブサポートしており、プロバイダに依存しないE2EEメールが可能です。 例えば、Proton MailのユーザはMailbox.orgのユーザにE2EEメッセージを送れますし、OpenPGPで暗号化された通知を、それをサポートするインターネットサービスから受け取ることができます。

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

!!! 警告

    OpenPGPのようなE2EE技術を使用しても、メールのヘッダーには暗号化されていないメタデータが残ります。 詳しくはこちらを御覧ください: [電子メールのメタデータ](basics/email-security.md#email-metadata-overview)。
    
    OpenPGPは前方秘匿性のサポートもしていません。つまり、あなたか受信者どちらかの秘密鍵が盗まれた場合、その鍵で暗号化された以前までの全てのメッセージは暴露します。 [秘密鍵を守るには?](basics/email-security.md#how-do-i-protect-my-private-keys)

### Proton Mail

!!! recommendation

    ![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }
    
    **Proton Mail** は、プライバシー、暗号化、セキュリティ、使いやすさを重視したメールサービスです。 2013年から運営をされています。 Proton AGはスイスのジュネーブに拠点を置いています。 アカウントは無料プランでストレージ500MBから始まります。
    
    [:octicons-home-16: ホームページ](https://proton.me/mail){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onionサービス" }
    [:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="プライバシーポリシー" }
    [:octicons-info-16:](https://proton.me/support/mail){ .card-link title=ドキュメンテーション}
    [:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="ソースコード" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id979659905)
        - [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
        - [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
        - [:simple-apple: macOS](https://proton.me/mail/bridge#download)
        - [:simple-linux: Linux](https://proton.me/mail/bridge#download)
        - [:octicons-browser-16: Web](https://mail.proton.me)

無料アカウントには本文の検索ができないことや、 [推奨されるデスクトップメールクライアント](email-clients.md) (Thunderbirdなど)を使用するために必要な [Proton Mail Bridge](https://proton.me/mail/bridge) を利用できないといった制限があります。 有料アカウントにはProton Mail Bridge、追加ストレージ、カスタムドメインのサポートなどの機能が含まれています。 [Securitum](https://research.securitum.com)により2021年11月9日 [監査証明書](https://proton.me/blog/security-audit-all-proton-apps) がProton Mailアプリにおくられました。

Proton Unlimitedプラン、Businessプラン、またはVisionaryプランをお持ちの場合、 [SimpleLogin](#simplelogin) Premiumも無料で利用できます。

Proton Mailには内部にクラッシュレポートがあり、これは第三者に共有 **されません** 。 クラッシュレポートは次のように無効にできます: **設定** > **設定を開く** > **アカウント** > **セキュリティとプライバシー** > **クラッシュレポートを送信**

#### :material-check:{ .pg-green } カスタムドメインとエイリアス

Proton Mailの有料会員は独自ドメインでサービスや [キャッチオール](https://proton.me/support/catch-all) アドレスを使うことができます。 Proton Mailはドメインを購入したくない人に便利な [サブアドレス](https://proton.me/support/creating-aliases) もサポートしています。

#### :material-check:{ .pg-green } プライベートな支払い方法

Proton Mailは標準的なクレジット・デビットカード、 [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) 、またPayPalでの支払いに加え、現金の郵送も [受け付けています](https://proton.me/support/payment-options) 。

#### :material-check:{ .pg-green } アカウントのセキュリティ

Proton Mailは TOTP [二要素認証](https://proton.me/support/two-factor-authentication-2fa) およびFIDO2またはU2F規格を使用した [ハードウェアセキュリティキー](https://proton.me/support/2fa-security-key) をサポートしています。 ハードウェアセキュリティキーを使用するには、先にTOTP二要素認証の設定が必要です。

#### :material-check:{ .pg-green } データのセキュリティ

Proton Mailはメールと [カレンダー](https://proton.me/news/protoncalendar-security-model) を [ゼロアクセス暗号化](https://proton.me/blog/zero-access-encryption) します。 ゼロアクセス暗号化で保護されたデータにアクセスできるのはあなただけです。

ディスプレイネームやメールアドレスなど、 [Proton Contacts](https://proton.me/support/proton-contacts) に保存される一部の情報はゼロアクセス暗号化によって保護されていません。 電話番号など、ゼロアクセス暗号化をサポートするContactフィールドには南京錠のアイコンが表示されます。

#### :material-check:{ .pg-green } メールの暗号化

Proton Mailはwebメールに [OpenPGP暗号化を組み込んでいます。](https://proton.me/support/how-to-use-pgp) 他のProton Mailアカウントへのメールは自動的に暗号化され、OpenPGPキーによる非Proton Mailアドレスへの暗号化はアカウント設定から簡単に有効化できます。 Proton Mailアカウントへのサインアップや、OpenPGPのようなソフトウェアを必要としない [非Proton Mailアドレスへの暗号化メッセージ](https://proton.me/support/password-protected-emails) も可能です。

Proton Mailは [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) からHTTP経由で公開鍵を発見することもサポートしています。 これにより、Proton Mailを使っていない人でも、Proton MailアカウントのOpenPGPキーを簡単に見つけることができ、プロバイダをまたいだE2EEが可能になります。

#### :material-information-outline:{ .pg-blue } アカウントの停止

有料アカウントを持っており、しかし14日を過ぎても [請求への支払いが無い](https://proton.me/support/delinquency) 場合、データにアクセスできなくなります。 30日を過ぎるとアカウントは滞納者となり、受信メールは届かなくなります。 この期間も請求は継続されます。

#### :material-information-outline:{ .pg-blue } 追加機能

Proton Mailは月額9.99ユーロで「Unlimited」アカウントを提供しており、複数アカウント、ドメイン、エイリアス、500GBのストレージに加えてProton VPNへのアクセスも可能になります。

Proton Mailにはデジタル遺産の機能はありません。

### Mailbox.org

!!! recommendation

    ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }
    
    **Mailbox.org** は安全、広告なし、プライベートでいることを重視した、100%エコエネルギーで運営されているメールサービスです。 2014年から運営をされています。 Mailbox.orgはドイツのベルリンに拠点を置いています。 アカウントは2GBのストレージから始まり、必要に応じてアップグレードできます。
    
    [:octicons-home-16: ホームページ](https://mailbox.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="プライバシーポリシー" }
    [:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=ドキュメンテーション}
    
    ??? downloads
    
        - [:octicons-browser-16: Web](https://login.mailbox.org)

#### :material-check:{ .pg-green } カスタムドメインとエイリアス

Mailbox.orgでは独自ドメインを使用することができ、 [キャッチオール](https://kb.mailbox.org/display/MBOKBEN/Using+catch-all+alias+with+own+domain) アドレスをサポートしています。 Mailbox.orgはドメインを購入したくない人に便利な [サブアドレス](https://kb.mailbox.org/display/BMBOKBEN/What+is+an+alias+and+how+do+I+use+it) もサポートしています。

#### :material-check:{ .pg-green } プライベートな支払い方法

Mailbox.orgは決済プロセッサBitPayがドイツでの業務を停止したために暗号通貨を受け付けていません。 しかし、郵送による現金払い、銀行口座への現金払い、銀行振込、クレジットカード、PayPal、そしてドイツ固有のプロセッサであるpaydirektとSofortüberweisungを受け付けています。

#### :material-check:{ .pg-green } アカウントのセキュリティ

Mailbox.orgはwebメールに限り [二要素認証](https://kb.mailbox.org/display/MBOKBEN/How+to+use+two-factor+authentication+-+2FA) をサポートしています。 [YubiCloud](https://www.yubico.com/products/services-software/yubicloud)を介して、TOTP または [YubiKey](https://en.wikipedia.org/wiki/YubiKey) のいずれかを使用することができます。 [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) などのウェブ標準はまだサポートされていません。

#### :material-information-outline:{ .pg-blue } データのセキュリティ

Mailbox.orgでは [encrypted mailbox](https://kb.mailbox.org/display/MBOKBEN/The+Encrypted+Mailbox) を使用して受信メールを暗号化することができます。 新しいメッセージを受信するとすぐにあなたの公開鍵で暗号化されます。

ただし、Mailbox.orgが使用しているソフトウェアプラットフォームである [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange) はアドレス帳とカレンダーの暗号化を [サポートしていません](https://kb.mailbox.org/display/BMBOKBEN/Encryption+of+calendar+and+address+book) 。 その情報については、 [スタンドアロンオプション](calendar.md) の方が適切であるかもしれません。

#### :material-check:{ .pg-green } メールの暗号化

Mailbox.orgはwebメールに [暗号化を組み込んで](https://kb.mailbox.org/display/MBOKBEN/Send+encrypted+e-mails+with+Guard) おり、OpenPGP公開鍵を持つ人へのメッセージ送信を簡素化します。 また、Mailbox.orgのサーバ上にある [メールをリモートの受信者が復号](https://kb.mailbox.org/display/MBOKBEN/My+recipient+does+not+use+PGP) することもできます。 この機能はリモートの受信者がOpenPGPを持っておらず、自分のメールボックスにあるメールのコピーを複合できない場合に便利です。

Mailbox.orgは [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) からHTTP経由で公開鍵を発見することもサポートしています。 これにより、Mailbox.orgを使っていない人でも、Mailbox.orgアカウントのOpenPGPキーを簡単に見つけることができ、プロバイダをまたいだE2EEが可能になります。

#### :material-information-outline:{ .pg-blue } アカウントの停止

アカウントは契約が終了すると制限付きユーザアカウントに設定されます。 [30日後、取り消し不能で削除されます](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract) 。

#### :material-information-outline:{ .pg-blue } 追加機能

[.onionサービス](https://kb.mailbox.org/display/MBOKBEN/The+Tor+exit+node+of+mailbox.org) を使って、IMAP/SMTP経由でMailboxl.orgアカウントにアクセスできます。 ただし .onionサービスからwebメールのインターフェイスにアクセスすることはできず、TLS証明書のエラーが発生する可能性があります。

全てのアカウントには [暗号化可能](https://kb.mailbox.org/display/MBOKBEN/Encrypt+files+on+your+Drive) な限られたクラウドストレージが付属しています。 Mailbox.orgは [@secure.mailbox.org](https://kb.mailbox.org/display/MBOKBEN/Ensuring+E-Mails+are+Sent+Securely) エイリアスも提供しており、これはメールサーバ間の接続にTLS暗号化を強制し、さもなければメッセージは全く送信されません。 Mailbox.orgはIMAPやPOP3のような標準的なアクセスプロトコルに加え、 [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) もサポートしています。

Mailbox.orgの全てのプランにはデジタル遺産機能があります。 相続人が申請し、遺言書を提出することを条件に、自分のデータを相続人に渡すかどうかを選択することができます。 または、名前と住所で人を指名することもできます。

## その他のプロバイダ

These providers store your emails with zero-knowledge encryption, making them great options for keeping your stored emails secure. However, they don't support interoperable encryption standards for E2EE communications between different providers.

<div class="grid cards" markdown>

- ![Skiff Mail logo](assets/img/email/skiff-mail.svg){ .twemoji } [Skiff Mail](email.md#skiff-mail)
- ![Tutanota logo](assets/img/email/tutanota.svg){ .twemoji } [Tutanota](email.md#tutanota)

</div>

### Skiff Mail

!!! recommendation

    ![Skiff Mail logo](assets/img/email/skiff-mail.svg){ align=right }
    
    **Skiff Mail** is a web based email service with E2EE that began in 2020 that is based in San Francisco with developers worldwide. Accounts start with 10GB of free storage.
    
    [:octicons-home-16: Homepage](https://skiff.com/mail){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://app.skiff.com/docs/db93c237-84c2-4b2b-9588-19a7cd2cd45a#tyGksN9rkqbo2uGYASxsA6HVLjUoly/wTYK8tncTto8=){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://skiff.com/help){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/skiff-org/skiff-apps){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-android: Android](https://play.google.com/store/apps/details?id=com.skemailmobileapp&pli=1)
        - [:simple-appstore: iOS](https://apps.apple.com/us/app/skiff-mail/id1619168801)
        - [:octicons-browser-16: Web](https://app.skiff.com/mail)

Skiff has undergone a few [audits](https://skiff.com/transparency) during its development.

#### :material-check:{ .pg-green } カスタムドメインとエイリアス

You can create up to 3 additional @skiff.com email aliases in addition to your primary account address on their free plan. [Custom domains](https://skiff.com/blog/custom-domain-setup) are available on their Pro or Business plan, and allow you to create unlimited aliases.

#### :material-alert-outline:{ .pg-orange } Private Payment Methods

Skiff Mail accepts cryptocurrency payments via Coinbase Commerce, including Bitcoin and Ethereum, but they do not accept our recommended [cryptocurrency](cryptocurrency.md), Monero. They also accept credit card payments via Stripe.

#### :material-check:{ .pg-green } アカウントのセキュリティ

Skiff Mail supports TOTP two-factor authentication and hardware security keys using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two-factor authentication first.

#### :material-check:{ .pg-green } データのセキュリティ

Skiff Mail has zero access encryption at rest for all of your data. This means the messages and other data stored in your account are only readable by you.

#### :material-information-outline:{ .pg-blue } Email Encryption

Skiff Mail does not use OpenPGP. Emails are only encrypted with E2EE to other Skiff Mail users. Skiff does not have a "temporary inbox" or "passworded email" feature like some other providers have, so that external users cannot receive or reply to messages with E2EE.

#### :material-information-outline:{ .pg-blue } アカウントの停止

Skiff Mail accounts do not expire, but unpaid accounts will be prompted to remove any enabled paid features (such as additional aliases) or renew their plan before the account can be used.

#### :material-information-outline:{ .pg-blue } Additional Functionality

Skiff additionally offers [workspace productivity features](https://discuss.privacyguides.net/t/skiff-pages-drive-productivity-tools/11758/13), but we still prefer [alternative](productivity.md) options for collaborating and file sharing at this time.

Skiff Mail does not offer a digital legacy feature.

### Tutanota

!!! recommendation

    ![Tutanota logo](assets/img/email/tutanota.svg){ align=right }
    
    **Tutanota** is an email service with a focus on security and privacy through the use of encryption. Tutanota has been in operation since **2011** and is based in Hanover, Germany. Accounts start with 1GB storage with their free plan.
    
    [:octicons-home-16: Homepage](https://tutanota.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://tutanota.com/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://tutanota.com/faq){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://tutanota.com/community/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
        - [:simple-appstore: App Store](https://apps.apple.com/app/tutanota/id922429609)
        - [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
        - [:simple-windows11: Windows](https://tutanota.com/#download)
        - [:simple-apple: macOS](https://tutanota.com/#download)
        - [:simple-linux: Linux](https://tutanota.com/#download)
        - [:octicons-browser-16: Web](https://mail.tutanota.com/)

Tutanota doesn't support the [IMAP protocol](https://tutanota.com/faq/#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tutanota app. Neither [Email import](https://github.com/tutao/tutanota/issues/630) or [subfolders](https://github.com/tutao/tutanota/issues/927) are currently supported, though this is [due to be changed](https://tutanota.com/blog/posts/kickoff-import). Emails can be exported [individually or by bulk selection](https://tutanota.com/howto#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } カスタムドメインとエイリアス

Paid Tutanota accounts can use up to 5 [aliases](https://tutanota.com/faq#alias) and [custom domains](https://tutanota.com/faq#custom-domain). Tutanota doesn't allow for [subaddressing (plus addresses)](https://tutanota.com/faq#plus), but you can use a [catch-all](https://tutanota.com/howto#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } Private Payment Methods

Tutanota only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tutanota.com/faq/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green } アカウントのセキュリティ

Tutanota supports [two factor authentication](https://tutanota.com/faq#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } データのセキュリティ

Tutanota has [zero access encryption at rest](https://tutanota.com/faq#what-encrypted) for your emails, [address book contacts](https://tutanota.com/faq#encrypted-address-book), and [calendars](https://tutanota.com/faq#calendar). This means the messages and other data stored in your account are only readable by you.

#### :material-information-outline:{ .pg-blue } Email Encryption

Tutanota [does not use OpenPGP](https://www.tutanota.com/faq/#pgp). Tutanota accounts can only receive encrypted emails from non-Tutanota email accounts when sent via a [temporary Tutanota mailbox](https://www.tutanota.com/howto/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } アカウントの停止

Tutanota will [delete inactive free accounts](https://tutanota.com/faq#inactive-accounts) after six months. You can reuse a deactivated free account if you pay.

#### :material-information-outline:{ .pg-blue } Additional Functionality

Tutanota offers the business version of [Tutanota to non-profit organizations](https://tutanota.com/blog/posts/secure-email-for-non-profit) for free or with a heavy discount.

Tutanota also has a business feature called [Secure Connect](https://tutanota.com/secure-connect/). This ensures customer contact to the business uses E2EE. The feature costs €240/y.

Tutanota doesn't offer a digital legacy feature.

## Email Aliasing Services

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
    
    **AnonAddy** lets you create 20 domain aliases on a shared domain for free, or unlimited "standard" aliases which are less anonymous.
    
    [:octicons-home-16: Homepage](https://anonaddy.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://anonaddy.com/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://app.anonaddy.com/docs/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://anonaddy.com/donate/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-android: Android](https://anonaddy.com/faq/#is-there-an-android-app)
        - [:material-apple-ios: iOS](https://anonaddy.com/faq/#is-there-an-ios-app)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/en-GB/firefox/addon/anonaddy/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/anonaddy-anonymous-email/iadbdpnoknmbdeolbapdackdcogdmjpe)

The number of shared aliases (which end in a shared domain like @anonaddy.me) that you can create is limited to 20 on AnonAddy's free plan and 50 on their $12/year plan. You can create unlimited standard aliases (which end in a domain like @[username].anonaddy.com or a custom domain on paid plans), however, as previously mentioned, this can be detrimental to privacy because people can trivially tie your standard aliases together based on the domain name alone. Unlimited shared aliases are available for $36/year.

Notable free features:

- [x] 20 Shared Aliases
- [x] Unlimited Standard Aliases
- [ ] No Outgoing Replies
- [x] 2 Recipient Mailboxes
- [x] Automatic PGP Encryption

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

## 基準

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any Email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an Email provider, and conduct your own research to ensure the Email provider you choose is the right choice for you.

### テクノロジー

We regard these features as important in order to provide a safe and optimal service. You should consider whether the provider which has the features you require.

**Minimum to Qualify:**

- Encrypts email account data at rest with zero-access encryption.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322/) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Custom domain names are important to users because it allows them to maintain their agency from the service, should it turn bad or be acquired by another company which doesn't prioritize privacy.
- Operates on owned infrastructure, i.e. not built upon third-party email service providers.

**最良の場合：**

- Encrypts all account data (Contacts, Calendars, etc.) at rest with zero-access encryption.
- Integrated webmail E2EE/PGP encryption provided as a convenience.
- Support for [WKD](https://wiki.gnupg.org/WKD) to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key by typing: `gpg --locate-key example_user@example.com`
- Support for a temporary mailbox for external users. This is useful when you want to send an encrypted email, without sending an actual copy to your recipient. These emails usually have a limited lifespan and then are automatically deleted. They also don't require the recipient to configure any cryptography like OpenPGP.
- Availability of the email provider's services via an [onion service](https://en.wikipedia.org/wiki/.onion).
- [Subaddressing](https://en.wikipedia.org/wiki/Email_address#Subaddressing) support.
- Catch-all or alias functionality for those who own their own domains.
- Use of standard email access protocols such as IMAP, SMTP or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.

### プライバシー

私たちは、推奨するプロバイダーができるだけデータを収集しないことを望んでいます。

**Minimum to Qualify:**

- Protect sender's IP address. Filter it from showing in the `Received` header field.
- Don't require personally identifiable information (PII) besides a username and a password.
- Privacy policy that meets the requirements defined by the GDPR.

**最良の場合：**

- Accepts [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Hosted in a jurisdiction with strong email privacy protection laws.

### セキュリティ

メール サーバーは、非常に機密性の高いデータを大量に扱います。 私たちは、プロバイダーが顧客を保護するために業界のベストプラクティスを採用することを期待しています。

**最低条件：**

- Protection of webmail with 2FA, such as TOTP.
- Zero access encryption, builds on encryption at rest. The provider does not have the decryption keys to the data they hold. This prevents a rogue employee leaking data they have access to or remote adversary from releasing data they have stolen by gaining unauthorized access to the server.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) support.
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://www.hardenize.com/), [testssl.sh](https://testssl.sh/), or [Qualys SSL Labs](https://www.ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
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

**最良の場合：**

- Support for hardware authentication, i.e. U2F and [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn). U2F and WebAuthn are more secure as they use a private key stored on a client-side hardware device to authenticate people, as opposed to a shared secret that is stored on the web server and on the client side when using TOTP. Furthermore, U2F and WebAuthn are more resistant to phishing as their authentication response is based on the authenticated [domain name](https://en.wikipedia.org/wiki/Domain_name).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in addition to DANE support.
- Implementation of [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), this is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Bug-bounty programs and/or a coordinated vulnerability-disclosure process.
- Website security standards such as:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163/)

### 信頼

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? We require our recommended providers to be public about their ownership or leadership. We also would like to see frequent transparency reports, especially in regard to how government requests are handled.

**最低条件：**

- 公の場でのリーダーシップやオーナーシップ。

**最良の場合：**

- 公の場でのリーダーシップ。
- 頻繁な透明性レポート。

### マーケティング

With the email providers we recommend we like to see responsible marketing.

**最低条件：**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.). The provider's site must also comply with [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) for those who wish to opt-out.

無責任なマーケティングをしてはいけない：

- 「破れない暗号化」という主張。 暗号化は、それを解読する技術が存在する将来に、秘密ではなくなるかもしれないという意図のもとに使用される必要があります。
- 匿名性を100％保証すること。 誰かが何かを100％だと主張するとき、それは失敗の確実性がないことを意味します。 私たちは、人々が多くの方法で簡単に匿名化を解除できることを知っています：

- 匿名化ソフトウェア（Tor、VPNなど）を使わずにアクセスした個人情報（メールアカウント、固有のペンネームなど）を再利用する。
- [ブラウザフィンガープリント](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**最良の場合：**

- 明確で読みやすいドキュメント。 これには、2FA のセットアップ、電子メールクライアント、OpenPGP などが含まれます。

### 追加機能

厳密な要件ではありませんが、推奨するプロバイダーを決定する際に考慮した利便性やプライバシーの要素が他にもいくつかあります。
