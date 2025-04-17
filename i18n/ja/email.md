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

<small>以下の脅威から保護します：</small>

- [:material-server-network: サービスプロバイダー](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

実質的に、電子メールはどんなオンラインサービスを使うにも必要ですが、個人間での会話にはお勧めしません。 他人との連絡には電子メールを使うよりも、前方秘匿性のあるインスタントメッセンジャの使用を検討してください。

[おすすめのインスタントメッセンジャー](real-time-communication.md ""){.md-button}

## 推奨するサービスプロバイダー

それ以外にも、持続可能なビジネスモデル、組み込まれたセキュリティーとプライバシー機能に基づき、様々な電子メールプロバイダーを推奨します。 詳細については、[基準の完全なリスト](#criteria)をお読みください。

| プロバイダー                      | OpenPGP / WKD                          | IMAP / SMTP                                        | Zero-Access Encryption                           | Anonymous Payment Methods             |
| --------------------------- | -------------------------------------- | -------------------------------------------------- | ------------------------------------------------ | ------------------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } 有料プランのみ | :material-check:{ .pg-green }                    | 現金                                    |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                      | :material-information-outline:{ .pg-blue } メールのみ | 現金                                    |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }             | :material-check:{ .pg-green }                    | Monero <br>Cash via third party |

In addition to (or instead of) an email provider recommended here, you may wish to consider a dedicated [email aliasing service](email-aliasing.md#recommended-providers) to protect your privacy. 特に、スパムから実際の受信トレイを保護し、企業のマーケティング活動によるアカウントの関連付けを防ぎ、すべての受信メールをPGPで暗号化することができます。

- [詳細 :material-arrow-right-drop-circle:](email-aliasing.md)

## OpenPGP対応サービス

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory (WKD) standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic end-to-end encrypted emails. 例えば、Proton MailのユーザはMailbox.orgのユーザにE2EEメッセージを送れますし、OpenPGPで暗号化された通知を、それをサポートするインターネットサービスから受け取ることができます。

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">注意</p>

OpenPGPのようなE2EE（エンドツーエンド暗号化）を利用しても、件名などを含むメールのヘッダーには暗号化されていないメタデータが残ります！ 詳細は [電子メールのメタデータ](basics/email-security.md#email-metadata-overview)のページにあります。

OpenPGP also does not support forward secrecy, which means if the private key of either you or the message recipient is ever stolen, all previous messages encrypted with it will be exposed.

- [How do I protect my private keys?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** は、プライバシー、暗号化、セキュリティ、使いやすさを重視したメールサービスです。 2013年からサービスが稼働しました。 Proton AGはスイスのジュネーブを拠点としています。

The Proton Free plan comes with 500 MB of Mail storage, which you can increase up to 1 GB for free.

[:octicons-home-16: ウェブページ](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/mail/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>ダウンロード</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Free accounts have some limitations, such as not being able to search body text and not having access to [Proton Mail Bridge](https://proton.me/mail/bridge), which is required to use a [recommended desktop email client](email-clients.md) (e.g., Thunderbird). 有料アカウントにはProton Mail Bridge、追加ストレージ、カスタムドメインのサポートなどの機能が含まれています。 Proton Unlimitedプランや複数ユーザープランの場合、[SimpleLogin](email-aliasing.md#simplelogin)も無料で利用できます。

[Securitum](https://research.securitum.com)により2021年11月9日 [監査証明書](https://proton.me/blog/security-audit-all-proton-apps) がProton Mailアプリにおくられました。

Proton Mailのクラッシュレポートは第三者に共有**されません**。 これはウェブアプリで無効にすることができます：:gear: → **すべての設定** → **アカウント** → **セキュリティとプライバシー** → **プライバシーとデータ収集**。

#### :material-check:{ .pg-green } カスタムドメインとエイリアス

Proton Mailの有料会員は独自ドメインでサービスや [キャッチオール](https://proton.me/support/catch-all) アドレスを使うことができます。 Proton Mailはドメインを購入したくない場合に有用な[サブアドレス](https://proton.me/support/creating-aliases)に対応しています。

#### :material-check:{ .pg-green } プライベートな支払い方法

Proton Mail [accepts](https://proton.me/support/payment-options) **cash** by mail in addition to standard credit/debit card, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), and PayPal payments.

#### :material-check:{ .pg-green } アカウントのセキュリティ

Proton MailはFIDO2やU2Fを用いたTOTP[二要素認証](https://proton.me/support/two-factor-authentication-2fa)や[ハードウェアセキュリティキー](https://proton.me/support/2fa-security-key)に対応しています。 ハードウェアセキュリティキーを使用するには、先にTOTP二要素認証の設定が必要です。

#### :material-check:{ .pg-green } データのセキュリティ

Proton Mailはメールと [カレンダー](https://proton.me/news/protoncalendar-security-model) を [ゼロアクセス暗号化](https://proton.me/blog/zero-access-encryption) します。 ゼロアクセス暗号化で保護されたデータにアクセスできるのはあなただけです。

ディスプレイネームやメールアドレスなど、 [Proton Contacts](https://proton.me/support/proton-contacts) に保存される一部の情報はゼロアクセス暗号化によって保護されていません。 電話番号など、ゼロアクセス暗号化をサポートするContactフィールドには南京錠のアイコンが表示されます。

#### :material-check:{ .pg-green } メールの暗号化

Proton Mailはwebメールに [OpenPGP暗号化を組み込んでいます。](https://proton.me/support/how-to-use-pgp) 他のProton Mailアカウントへのメールは自動的に暗号化され、OpenPGPキーによる非Proton Mailアドレスへの暗号化はアカウント設定から簡単に有効化できます。 ProtonはWKDによる外部の鍵の自動探索にも対応しています。 WKDを使った他のプロバイダーに送信されるEメールは自動的にOpenPGPで暗号化され、PGP公開鍵と連絡先を手動で交換する必要はありません。 また、[Proton Mailではないアドレスに送るメッセージをOpenPGPを使わずに暗号化する](https://proton.me/support/password-protected-emails)こともでき、受信者はProton Mailアカウントへのサインアップが必要ありません。

Proton MailではProtonアカウントの公開鍵をWKDからHTTP経由で公開します。 This allows people who don't use Proton Mail to find the OpenPGP keys of Proton Mail accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Proton's own domains, like `@proton.me`. If you use a custom domain, you must [configure WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } アカウントの停止

有料アカウントを持っており、しかし14日を過ぎても [請求への支払いが無い](https://proton.me/support/delinquency) 場合、データにアクセスできなくなります。 30日を過ぎるとアカウントは滞納者となり、受信メールは届かなくなります。 この期間も請求は継続されます。 Protonは1年間[アクティブではないフリープランのアカウントを削除します](https://proton.me/support/inactive-accounts)。 削除されたアカウントのメールアドレスは再利用**できません**。

#### :material-information-outline:{ .pg-blue } 追加機能

Proton Mail's [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) plan also enables access to other Proton services in addition to providing multiple custom domains, unlimited hide-my-email aliases, and 500 GB of storage.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** is an email service with a focus on being secure, ad-free, and powered by 100% eco-friendly energy. 2014年から運営をされています。 Mailbox.orgはドイツのベルリンに拠点を置いています。

Accounts start with up to 2 GB storage, which can be upgraded as needed.

[:octicons-home-16: ウェブページ](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="プライバシーポリシー" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="ドキュメント" }

<details class="downloads" markdown>
<summary>ダウンロード</summary>

- [:octicons-browser-16: ウェブ](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } カスタムドメインとエイリアス

Mailbox.orgでは独自ドメインを使うことができ、[キャッチオール](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name)アドレスにも対応している。 Mailbox.orgはドメインを購入したくない場合に有用な[サブアドレス](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it)にも対応しています。

#### :material-check:{ .pg-green } プライベートな支払い方法

Mailbox.orgは決済プロセッサBitPayがドイツでの業務を停止したために暗号通貨を受け付けていません。 However, they do accept **cash** by mail, **cash** payment to bank account, bank transfer, credit card, PayPal, and a couple of German-specific processors: Paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } アカウントのセキュリティ

Mailbox.orgはウェブメールに限り、[二要素認証](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa)に対応しています。 TOTPもしくは[YubiCloud](https://yubico.com/products/services-software/yubicloud)経由の[YubiKey](https://en.wikipedia.org/wiki/YubiKey)を利用できます。 Web standards such as [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) are not yet supported.

#### :material-information-outline:{ .pg-blue } データのセキュリティ

Mailbox.orgでは[暗号化されたメールボックス](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox)により受信メールを暗号化することができます。 新しいメッセージを受信するとすぐにあなたの公開鍵で暗号化されます。

However, [Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. A [standalone option](calendar.md) may be more appropriate for that data.

#### :material-check:{ .pg-green } メールの暗号化

Mailbox.orgのウェブメールは[暗号化機能が組みこまれており](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard)、OpenPGP公開鍵を持つ人へのメッセージの送信が簡単にできます。 Mailbox.orgのサーバー上で[受信者がEメールの復号化をすることもできます](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp)。 この機能はリモートの受信者がOpenPGPを持っておらず、自分のメールボックスにあるメールのコピーを複合できない場合に便利です。

Mailbox.orgはWKDによりHTTP経由で公開鍵を探索することにも対応しています。 This allows people outside of Mailbox.org to find the OpenPGP keys of Mailbox.org accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Mailbox.org's own domains, like `@mailbox.org`. If you use a custom domain, you must [configure WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } アカウントの停止

契約が終了すると、アカウントは制限付きユーザーアカウントになります。 [30日後](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract)に取消不可能な形で削除されます。

#### :material-information-outline:{ .pg-blue } 追加機能

Mailbox.orgの[.onionサービス](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org)を利用し、IMAP/SMTP経由でMailbox.orgのアカウントにアクセスできます。 ただし、.onionサービスからウェブメールにはアクセスできず、TLS証明書エラーが発生する可能性があります。

すべてのアカウントで[暗号化可能な](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive)制限付きクラウドストレージが利用できます。 Mailbox.orgには[@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely)というメールサーバー間の接続にTLS暗号化が必須であるエイリアスもあり、TLS暗号化がなければメッセージは全く送信できません。 Mailbox.orgはIMAPやPOP3のような標準的なアクセスプロトコルに加え、 [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) もサポートしています。

Mailbox.orgの全てのプランにはデジタル遺産機能があります。 You can choose whether you want any of your data to be passed to heirs, providing that they apply and provide your testament. または、名前と住所で人を指名することもできます。

## その他のプロバイダ

これらのプロバイダーは、あなたの電子メールをゼロ知識暗号化で保存するため、電子メールを安全に保つのに最適なオプションです。 ただし、異なるプロバイダー間のE2EE通信では、相互運用可能な暗号化規格がサポートされていません。

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** （旧 *Tutanota*）は暗号化によるセキュリティとプライバシーを重視したメールサービスです。 Tutaは2011年に設立され、ドイツのハノーバーに拠点を置いています。

Free accounts start with 1 GB of storage.

[:octicons-home-16: ウェブページ](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="プライバシーポリシー" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="ドキュメント" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="ソースコード" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>ダウンロード</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:fontawesome-brands-windows: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: ウェブ](https://app.tuta.com)

</details>

</div>

Tutaは[IMAPプロトコル](https://tuta.com/support#imap)やサードパーティの[メールクライアント](email-clients.md)に対応しておらず、Tutaアプリに[外部のメールアカウント](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647)を追加することもできません。 [Eメールのインポート](https://github.com/tutao/tutanota/issues/630)にも現状は対応していませんが、[変更される予定](https://tuta.com/blog/kickoff-import)です。 フォルダごとに[個別もしくは一括選択](https://tuta.com/support#generalMail)してエクスポートすることはできますが、複数のフォルダがある場合は不便な可能性があります。

#### :material-check:{ .pg-green } カスタムドメインとエイリアス

有料のTutaアカウントではプランに応じて15もしくは30のエイリアスを利用でき、[カスタムドメイン](https://tuta.com/support#custom-domain)では無制限のエイリアスが利用できます。 Tutaでは[サブアドレス（プラスアドレス）](https://tuta.com/support#plus)は使えませんが、カスタムドメインでの[キャッチオール](https://tuta.com/support#settings-global)機能を使うことができます。

#### :material-information-outline:{ .pg-blue } プライベートな支払い方法

Tuta only directly accepts credit cards and PayPal, however [**cryptocurrency**](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with ProxyStore.

#### :material-check:{ .pg-green } アカウントのセキュリティ

TutaはTOTPもしくはU2Fによる[二要素認証](https://tuta.com/support#2fa)に対応しています。

#### :material-check:{ .pg-green } データのセキュリティ

Tuta has [zero-access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). アカウントに保存されたメッセージやその他データはあなたにしか読むことができません。

#### :material-information-outline:{ .pg-blue } メールの暗号化

Tutaは[OpenPGPを使用していません](https://tuta.com/support/#pgp)。 TutaではTuta以外からの暗号化されたEメールを受信するには[一時的なTutaメールボックス](https://tuta.com/support/#encrypted-email-external)を経由する必要があります。

#### :material-information-outline:{ .pg-blue } アカウントの停止

Tutaは6ヶ月間[アクティブではないフリープランのアカウント](https://tuta.com/support#inactive-accounts)を削除します。 料金を払えば、停止された無料アカウントを再利用できます。

#### :material-information-outline:{ .pg-blue } 追加機能

Tutaは[非営利団体](https://tuta.com/blog/secure-email-for-non-profit)向けに無料もしくは大幅な割引価格でビジネス版Tutaを提供しています。

## セルフホストメール

システム管理に詳しいのであれば、自前のメールサーバーの構築を検討することも一つの手段です。 安全性とメール配信の信頼性を維持するには、メールサーバーへの注意と継続的なメンテンナンスが必要になります。 以下の「オールインワン」な方法に加え、手動で設定するための記事を取り上げました：

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019年)
- [How To Run Your Own Mail Server](https://www.c0ffee.net/blog/mail-server-guide) (2017年8月)

### Stalwart

<div class="admonition recommendation" markdown>

![Stalwart logo](assets/img/email/stalwart.svg){ align=right }

**Stalwart**はRustで書かれた新しいメールサーバーで、標準的なIMAP、POP3やSMTPに加え、JMAPにも対応しています。 様々な設定は用意されていますが、デフォルトでも（セキュリティと機能の両方で）適切な設定となっているため、すぐに使い始めることができます。 TOTP二要素認証に対応するウェブベースの管理機能があり、PGP公開鍵で**すべての**受信メッセージを暗号化することができます。

[:octicons-home-16: ウェブページ](https://stalw.art){ .md-button .md-button--primary }
[:octicons-info-16:](https://stalw.art/docs/get-started){ .card-link title="ドキュメント" }
[:octicons-code-16:](https://github.com/stalwartlabs){ .card-link title="ソースコード" }
[:octicons-heart-16:](https://github.com/sponsors/stalwartlabs){ .card-link title="Contribute" }

</div>

Stalwartの[PGP実装](https://stalw.art/docs/encryption/overview)は推奨するセルフホスティングEメールの中でもユニークで、前提知識なしにメッセージストレージのある自前のメールサーバーを運用することができます。 独自ドメインにWeb Key Directoryを設定し、送信メールがPGPとWeb Key Directoryに対応したクライアント（Thunderbirdなど）を使うことで、すべての[Proton Mail](#proton-mail)に対応するセルフホスティングE2EE互換性を最も簡単に得ることができます。

Stalwartにはウェブメールが**ない**ため、[専用のEメールクライアント](email-clients.md)（もしくはNextCloudのメールアプリのようなオープンソースのウェブメールをセルフホスティングする）を使う必要があります。 *Privacy Guides*ではStalwartを内部のEメールサーバーで使用しています。

### Mailcow

<div class="admonition recommendation" markdown>

![Mailcow logo](assets/img/email/mailcow.svg){ align=right }

**Mailcow** はLinuxの経験がある方に最適な、より高度なメールサーバーです。 DKIMに対応したメールサーバー、アンチウイルスやスパム監視、SOGoによるウェブメールとActiveSync、二要素認証に対応したウェブベースの管理機能など、Dockerコンテナに必要なものがすべて含まれています。

[:octicons-home-16: ウェブページ](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title="ドキュメント" }
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="ソースコード" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title="Contribute" }

</div>

### Mail-in-a-Box

<div class="admonition recommendation" markdown>

![Mail-in-a-Box logo](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** はUbuntu上にメールサーバーをデプロイするための自動セットアップスクリプトです。 自前のメールサーバーを簡単に立ち上げることを目的としています。

[:octicons-home-16: ウェブページ](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title="ドキュメント" }
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="ソースコード" }

</div>

## 規準

**推奨するプロバイダーとは提携していないことに注意してください。**[標準的な基準](about/criteria.md)に加え、業界におけるベストプラクティスの実施や新しい技術の採用などを含む、推奨するために必要なEメールプロバイダーへの明確な要件を定めています。 Eメールプロバイダーを選ぶ前に以下のリストを理解し、どのEメールプロバイダーが適切であるかを調べ、確認してください。

### テクノロジー

安全で最適なサービスのために以下の機能が重要であると考えています。 要件に合致する機能がプロバイダーにあるか検討してください。

**最低条件：**

- Must encrypt email account data at rest with zero-access encryption.
- Must be capable of exporting emails as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .EML with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). プロバイダーが悪化したり、プライバシーを重視しない他の会社に買収されたりした場合に備えることができるため、カスタムドメイン名はユーザーにとって非常に重要である。
- Must operate on owned infrastructure, i.e. not built upon third-party email service providers.

**満たされることが望ましい基準：**

- Should encrypt all account data (contacts, calendars, etc.) at rest with zero-access encryption.
- Should provide integrated webmail E2EE/PGP encryption as a convenience.
- Should support WKD to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key with this command: `gpg --locate-key example_user@example.com`.
- 外部ユーザー用の一時的なメールボックスがあること。 This is useful when you want to send an encrypted email without sending an actual copy to your recipient. 通常の場合、一時的なメールボックスのメールには期限があり、自動的に削除されます。 また、受信者はOpenPGPのような暗号化を設定する必要がありません。
- Should support [sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Should allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). プロバイダーが悪化したり、プライバシーを重視しない他の会社に買収されたりした場合に備えることができるため、カスタムドメイン名はユーザーにとって非常に重要である。
- 独自ドメインを利用した際、キャッチオール機能もしくはエイリアス機能があること。
- Should use standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). 標準的なプロトコルを採用していることで、他のプロバイダーへ変更する際にすべてのメールを簡単にダウンロードすることができます。
- Email provider's services should be available via an [onion service](https://en.wikipedia.org/wiki/.onion).

### プライバシー

私たちは、推奨するサービスプロバイダーができるだけデータを収集しないことを望んでいます。

**最低条件：**

- Must protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Must not require personally identifiable information (PII) besides a username and a password.
- Privacy policy must meet the requirements defined by the GDPR.

**満たされることが望ましい基準：**

- Should accept [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Should be hosted in a jurisdiction with strong email privacy protection laws.

### セキュリティー

Email servers deal with a lot of very sensitive data. We expect that providers will adopt industry best practices in order to protect their customers.

**最低条件：**

- Protection of webmail with 2FA, such as [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Zero-access encryption, which builds on encryption at rest. プロバイダーは保有するデータの復号鍵を持たないこと。 不正を働く従業員がアクセスしたデータを流出させたり、遠隔地の敵対者がサーバーに不正アクセスして盗んだデータを公開したりすることを防ぐことができます。
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions)のサポート。
- [Hardenize](https://hardenize.com)や[testssl.sh](https://testssl.sh)、[Qualys SSL Labs](https://ssllabs.com/ssltest)などのツールでプロファイリングした際にTLSエラーや脆弱性がないこと。証明書関連のエラーや[Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security))の原因となった弱いDHパラメーターを含みます。
- A server suite preference (optional on TLS 1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- 有効な [MTA-STS](https://tools.ietf.org/html/rfc8461) および [TLS-RPT](https://tools.ietf.org/html/rfc8460) ポリシー。
- 有効な[DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities)レコード。
- 有効な[SPF](https://ja.wikipedia.org/wiki/Sender_Policy_Framework)および[DKIM](https://ja.wikipedia.org/wiki/DKIM)レコード。
- Must have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. DMARC認証を使用している場合、ポリシーは`reject`か`quarantine`に設定していること。
- サーバーの暗号スイートがTLS1.2以降であること、及び[RFC8996](https://datatracker.ietf.org/doc/rfc8996)への対応計画があること。
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS)によるメール送信。
- 以下のようなウェブサイトのセキュリティ基準：
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - 外部のドメインから読み込む場合、[サブリソース完全性](https://en.wikipedia.org/wiki/Subresource_Integrity)があること。
- [ヘッダー情報](https://en.wikipedia.org/wiki/Email#Message_header)の表示に対応していること。ヘッダー情報はメールがフィッシングであるか判断する重要なフォレンジック上の特徴である。

**満たされることが望ましい基準：**

- Should support hardware authentication, i.e. U2Fおよび[WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online)。
- DANEへの対応と[DNS Certification Authority Authorization（CAA）リソースレコード](https://tools.ietf.org/html/rfc6844)の設定。
- Should implement [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Published security audits from a reputable, third-party firm.
- バグ報奨金プログラム、協調的な脆弱性開示プロセス。
- 以下のようなウェブサイトのセキュリティ基準：
    - [コンテンツセキュリティポリシー（CSP）](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### 信頼

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? 推奨されるサービスプロバイダーには、自社の所有権やリーダーシップについて公表することが求められます。 また、特に政府からの要請がどのように処理されるかについて、透明性の高い報告が頻繁に行われることを望んでいます。

**最低条件：**

- 公的なリーダーシップまたはオーナーシップ。

**満たされることが望ましい基準：**

- 頻繁な透明性レポート。

### マーケティング

With the email providers we recommend, we like to see responsible marketing.

**最低条件：**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.).
- Must not have any irresponsible marketing, which can include the following:
    - Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
    - Guarantees of protecting anonymity 100%. When someone makes a claim that something is 100%, it means there is no certainty for failure. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:
        - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software such as Tor
        - [ブラウザーのフィンガープリンティングを行うこと。](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**満たされることが望ましい基準：**

- Clear and easy-to-read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### 追加機能

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
