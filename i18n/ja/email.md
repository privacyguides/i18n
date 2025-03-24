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

| プロバイダー                      | OpenPGP / WKD                          | IMAP / SMTP                                        | ゼロアクセス暗号化                                        | 匿名での支払い                |
| --------------------------- | -------------------------------------- | -------------------------------------------------- | ------------------------------------------------ | ---------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } 有料プランのみ | :material-check:{ .pg-green }                    | 現金                     |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                      | :material-information-outline:{ .pg-blue } メールのみ | 現金                     |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }             | :material-check:{ .pg-green }                    | サードバーティ経由でのMonero & 現金 |

上記の推奨するEメールプロバイダーに加え（もしくは代わりに）、プライバシー保護のために[Eメールエイリアスサービス](email-aliasing.md)を検討してください。 特に、スパムから実際の受信トレイを保護し、企業のマーケティング活動によるアカウントの関連付けを防ぎ、すべての受信メールをPGPで暗号化することができます。

- [詳細 :material-arrow-right-drop-circle:](email-aliasing.md)

## OpenPGP対応サービス

OpenPGPによる暗号化・復号化や[Web Key Directory規格](basics/email-security.md#what-is-the-web-key-directory-standard)をネイティブサポートしているプロバイダーでは、プロバイダーに依存しないE2EE（エンドツーエンド暗号化）メールが利用可能です。 例えば、Proton MailのユーザはMailbox.orgのユーザにE2EEメッセージを送れますし、OpenPGPで暗号化された通知を、それをサポートするインターネットサービスから受け取ることができます。

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">注意</p>

OpenPGPのようなE2EE（エンドツーエンド暗号化）を利用しても、件名などを含むメールのヘッダーには暗号化されていないメタデータが残ります！ 詳細は [電子メールのメタデータ](basics/email-security.md#email-metadata-overview)のページにあります。

OpenPGPは前方秘匿性に対応していないため、送信者であるあなたか受信者の秘密鍵が盗まれた場合、その秘密鍵で暗号化した過去を含めたすべてのメッセージが暗号化解除可能な状態となります。 [秘密鍵を保護するには？](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** は、プライバシー、暗号化、セキュリティ、使いやすさを重視したメールサービスです。 2013年からサービスが稼働しました。 Proton AGはスイスのジュネーブを拠点としています。 Proton Mailの無料プランのメールストレージは500MBから始まり、無料で1GBまで増やすことができます。

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

無料アカウントには本文の検索ができないことや、 [推奨されるデスクトップメールクライアント](email-clients.md) (Thunderbirdなど)を使用するために必要な [Proton Mail Bridge](https://proton.me/mail/bridge) を利用できないといった制限があります。 有料アカウントにはProton Mail Bridge、追加ストレージ、カスタムドメインのサポートなどの機能が含まれています。 [Securitum](https://research.securitum.com)により2021年11月9日 [監査証明書](https://proton.me/blog/security-audit-all-proton-apps) がProton Mailアプリにおくられました。

Proton Unlimitedプランや複数ユーザープランの場合、[SimpleLogin](email-aliasing.md#simplelogin)も無料で利用できます。

Proton Mailのクラッシュレポートは第三者に共有**されません**。 これはウェブアプリで無効にすることができます：:gear: → **すべての設定** → **アカウント** → **セキュリティとプライバシー** → **プライバシーとデータ収集**。

#### :material-check:{ .pg-green } カスタムドメインとエイリアス

Proton Mailの有料会員は独自ドメインでサービスや [キャッチオール](https://proton.me/support/catch-all) アドレスを使うことができます。 Proton Mailはドメインを購入したくない場合に有用な[サブアドレス](https://proton.me/support/creating-aliases)に対応しています。

#### :material-check:{ .pg-green } プライベートな支払い方法

Proton Mailは標準的なクレジット・デビットカード、 [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) 、またPayPalでの支払いに加え、現金の郵送も [受け付けています](https://proton.me/support/payment-options) 。

#### :material-check:{ .pg-green } アカウントのセキュリティ

Proton MailはFIDO2やU2Fを用いたTOTP[二要素認証](https://proton.me/support/two-factor-authentication-2fa)や[ハードウェアセキュリティキー](https://proton.me/support/2fa-security-key)に対応しています。 ハードウェアセキュリティキーを使用するには、先にTOTP二要素認証の設定が必要です。

#### :material-check:{ .pg-green } データのセキュリティ

Proton Mailはメールと [カレンダー](https://proton.me/news/protoncalendar-security-model) を [ゼロアクセス暗号化](https://proton.me/blog/zero-access-encryption) します。 ゼロアクセス暗号化で保護されたデータにアクセスできるのはあなただけです。

ディスプレイネームやメールアドレスなど、 [Proton Contacts](https://proton.me/support/proton-contacts) に保存される一部の情報はゼロアクセス暗号化によって保護されていません。 電話番号など、ゼロアクセス暗号化をサポートするContactフィールドには南京錠のアイコンが表示されます。

#### :material-check:{ .pg-green } メールの暗号化

Proton Mailはwebメールに [OpenPGP暗号化を組み込んでいます。](https://proton.me/support/how-to-use-pgp) 他のProton Mailアカウントへのメールは自動的に暗号化され、OpenPGPキーによる非Proton Mailアドレスへの暗号化はアカウント設定から簡単に有効化できます。 Protonは[Web Key Directory(WKD)](https://wiki.gnupg.org/WKD)による外部の鍵の自動探索にも対応しています。 WKDを使った他のプロバイダーに送信されるEメールは自動的にOpenPGPで暗号化され、PGP公開鍵と連絡先を手動で交換する必要はありません。 また、[Proton Mailではないアドレスに送るメッセージをOpenPGPを使わずに暗号化する](https://proton.me/support/password-protected-emails)こともでき、受信者はProton Mailアカウントへのサインアップが必要ありません。

Proton MailではProtonアカウントの公開鍵をWKDからHTTP経由で公開します。 これにより、Proton Mailを使っていない人でも、Proton MailアカウントのOpenPGPキーを簡単に見つけることができ、プロバイダをまたいだE2EEが可能になります。 @proton.meのようなProtonが所有するドメインのEメールアドレスのみ対象です。 カスタムドメインを使用する場合、[WKDの設定](./basics/email-security.md#what-is-the-web-key-directory-standard)が必要になります。

#### :material-information-outline:{ .pg-blue } アカウントの停止

有料アカウントを持っており、しかし14日を過ぎても [請求への支払いが無い](https://proton.me/support/delinquency) 場合、データにアクセスできなくなります。 30日を過ぎるとアカウントは滞納者となり、受信メールは届かなくなります。 この期間も請求は継続されます。 Protonは1年間[アクティブではないフリープランのアカウントを削除します](https://proton.me/support/inactive-accounts)。 削除されたアカウントのメールアドレスは再利用**できません**。

#### :material-information-outline:{ .pg-blue } 追加機能

Proton Mailの[Unlimited](https://proton.me/support/proton-plans#proton-unlimited)プランでは複数のカスタムドメイン、無制限のEメールエイリアスや500GBのストレージに加え、その他のProtonサービスを利用することができます。

Proton Mailにはデジタル遺産の機能はありません。

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** は安全、広告なし、プライベートでいることを重視した、100%エコエネルギーで運営されているメールサービスです。 2014年から運営をされています。 Mailbox.orgはドイツのベルリンに拠点を置いています。 各アカウントには最大2GBのストレージが割当てられ、必要に応じてアップグレードできます。

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

Mailbox.orgは決済プロセッサBitPayがドイツでの業務を停止したために暗号通貨を受け付けていません。 郵送による現金払い、銀行口座への銀金払い、銀行振込、クレジットカード、Paypalとドイツの支払いサービスであるpaydirektとSofortüberweisungに対応しています。

#### :material-check:{ .pg-green } アカウントのセキュリティ

Mailbox.orgはウェブメールに限り、[二要素認証](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa)に対応しています。 TOTPもしくは[YubiCloud](https://yubico.com/products/services-software/yubicloud)経由の[YubiKey](https://en.wikipedia.org/wiki/YubiKey)を利用できます。 [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) などのウェブ標準はまだサポートされていません。

#### :material-information-outline:{ .pg-blue } データのセキュリティ

Mailbox.orgでは[暗号化されたメールボックス](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox)により受信メールを暗号化することができます。 新しいメッセージを受信するとすぐにあなたの公開鍵で暗号化されます。

ただし、Mailbox.orgが利用している[Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange)はアドレス帳やカレンダーの暗号化は[対応していません](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book)。 その情報については、 [スタンドアロンオプション](calendar.md) の方が適切であるかもしれません。

#### :material-check:{ .pg-green } メールの暗号化

Mailbox.orgのウェブメールは[暗号化機能が組みこまれており](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard)、OpenPGP公開鍵を持つ人へのメッセージの送信が簡単にできます。 Mailbox.orgのサーバー上で[受信者がEメールの復号化をすることもできます](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp)。 この機能はリモートの受信者がOpenPGPを持っておらず、自分のメールボックスにあるメールのコピーを複合できない場合に便利です。

Mailbox.orgは [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) からHTTP経由で公開鍵を発見することもサポートしています。 これにより、Mailbox.orgを使っていない人でも、Mailbox.orgアカウントのOpenPGPキーを簡単に見つけることができ、プロバイダをまたいだE2EEが可能になります。 @mailbox.orgのようなMailbox.orgが所有するドメインのEメールアドレスのみ対象です。 カスタムドメインを使用する場合、[WKDの設定](./basics/email-security.md#what-is-the-web-key-directory-standard)が必要になります。

#### :material-information-outline:{ .pg-blue } アカウントの停止

契約が終了すると、アカウントは制限付きユーザーアカウントになります。 [30日後](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract)に取消不可能な形で削除されます。

#### :material-information-outline:{ .pg-blue } 追加機能

Mailbox.orgの[.onionサービス](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org)を利用し、IMAP/SMTP経由でMailbox.orgのアカウントにアクセスできます。 ただし、.onionサービスからウェブメールにはアクセスできず、TLS証明書エラーが発生する可能性があります。

すべてのアカウントで[暗号化可能な](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive)制限付きクラウドストレージが利用できます。 Mailbox.orgには[@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely)というメールサーバー間の接続にTLS暗号化が必須であるエイリアスもあり、TLS暗号化がなければメッセージは全く送信できません。 Mailbox.orgはIMAPやPOP3のような標準的なアクセスプロトコルに加え、 [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) もサポートしています。

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

**Tuta** （旧 *Tutanota*）は暗号化によるセキュリティとプライバシーを重視したメールサービスです。 Tutaは2011年に設立され、ドイツのハノーバーに拠点を置いています。 無料アカウントは1GBのストレージが利用できます。

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

TutaはクレジットカードもしくはPaypalのみ受け付けていますが、ProxyStoreとの[提携](https://tuta.com/support/#cryptocurrency)により、[暗号通貨](cryptocurrency.md)でギフトカードを購入することができます。

#### :material-check:{ .pg-green } アカウントのセキュリティ

TutaはTOTPもしくはU2Fによる[二要素認証](https://tuta.com/support#2fa)に対応しています。

#### :material-check:{ .pg-green } データのセキュリティ

TutaはEメールや[アドレス帳の連絡先](https://tuta.com/support#encrypted-address-book)、[カレンダー](https://tuta.com/support#calendar)の[ゼロアクセス暗号化](https://tuta.com/support#what-encrypted)に対応しています。 アカウントに保存されたメッセージやその他データはあなたにしか読むことができません。

#### :material-information-outline:{ .pg-blue } メールの暗号化

Tutaは[OpenPGPを使用していません](https://tuta.com/support/#pgp)。 TutaではTuta以外からの暗号化されたEメールを受信するには[一時的なTutaメールボックス](https://tuta.com/support/#encrypted-email-external)を経由する必要があります。

#### :material-information-outline:{ .pg-blue } アカウントの停止

Tutaは6ヶ月間[アクティブではないフリープランのアカウント](https://tuta.com/support#inactive-accounts)を削除します。 料金を払えば、停止された無料アカウントを再利用できます。

#### :material-information-outline:{ .pg-blue } 追加機能

Tutaは[非営利団体](https://tuta.com/blog/secure-email-for-non-profit)向けに無料もしくは大幅な割引価格でビジネス版Tutaを提供しています。

Tutaにはデジタルレガシー機能はありません。

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

- ゼロアクセス暗号化によりEメールアカウントのデータを暗号化していること。
- [Mbox](https://en.wikipedia.org/wiki/Mbox)もしくは[RFC5322](https://datatracker.ietf.org/doc/rfc5322)に基づいた個別の.EMLファイルとしてエクスポートできること。
- ユーザーの独自[ドメイン名](https://en.wikipedia.org/wiki/Domain_name)が利用できること。 プロバイダーが悪化したり、プライバシーを重視しない他の会社に買収されたりした場合に備えることができるため、カスタムドメイン名はユーザーにとって非常に重要である。
- 自社所有のインフラで運用されていること。第三者のEメールサービスプロバイダーによるサービス提供ではないこと。

**満たされることが望ましい基準：**

- ゼロアクセス暗号化により、すべてのアカウントのデータ（連絡先、カレンダーなど）が暗号化されていること。
- 利便性のため、E2EE/PGP暗号化できるウェブメールがあること。
- HTTP経由でのOpenPGP公開鍵の探索を改善するため、[WKD](https://wiki.gnupg.org/WKD)へ対応していること。 GnuPGでは次のスクリプトで鍵を取得できます： `gpg --locate-key example_user@example.com`
- 外部ユーザー用の一時的なメールボックスがあること。 受信者に実際のメールのコピーを送るのではなく、暗号化されたメールを送る際に役立ちます。 通常の場合、一時的なメールボックスのメールには期限があり、自動的に削除されます。 また、受信者はOpenPGPのような暗号化を設定する必要がありません。
- [.onionサービス](https://en.wikipedia.org/wiki/.onion)経由でEメールプロバイダーのサービスが利用できること。
- [サブアドレス](https://en.wikipedia.org/wiki/Email_address#Sub-addressing)に対応していること。
- 独自ドメインを利用した際、キャッチオール機能もしくはエイリアス機能があること。
- IMAP、SMTPや[JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol)などの標準的なEメールプロトコルを使用していること。 標準的なプロトコルを採用していることで、他のプロバイダーへ変更する際にすべてのメールを簡単にダウンロードすることができます。

### プライバシー

私たちは、推奨するサービスプロバイダーができるだけデータを収集しないことを望んでいます。

**最低条件：**

- 送信者のIPアドレスが保護されていること。`Received`ヘッダーフィールドに表示されないようフィルタリングすることを含む。
- ユーザー名とパスワード以外に、個人情報(PII)を必要としない。
- プライバシーポリシーがGDPRの要件を満たしている。

**満たされることが望ましい基準：**

- [匿名の支払い方法](advanced/payments.md)（[暗号通貨](cryptocurrency.md)、現金、ギフトカードなど）を受け入れること
- 強固な電子メールのプライバシー保護法の管轄区域でホストされていること

### セキュリティー

メールサーバーは、非常に機密性の高いデータを大量に扱います。 プロバイダーが顧客を保護するために業界のベストプラクティスを採用することを期待している。

**最低条件：**

- TOTPなどの二要素認証によるウェブメールの保護。
- 保存データの暗号化に基づく、ゼロアクセス暗号化。 プロバイダーは保有するデータの復号鍵を持たないこと。 不正を働く従業員がアクセスしたデータを流出させたり、遠隔地の敵対者がサーバーに不正アクセスして盗んだデータを公開したりすることを防ぐことができます。
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions)のサポート。
- [Hardenize](https://hardenize.com)や[testssl.sh](https://testssl.sh)、[Qualys SSL Labs](https://ssllabs.com/ssltest)などのツールでプロファイリングした際にTLSエラーや脆弱性がないこと。証明書関連のエラーや[Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security))の原因となった弱いDHパラメーターを含みます。
- サーバーの暗号スイート設定が（TLSv1.3では任意となっている）前方秘匿性と認証付き暗号に対応する強力な暗号スイートを優先していること。
- 有効な [MTA-STS](https://tools.ietf.org/html/rfc8461) および [TLS-RPT](https://tools.ietf.org/html/rfc8460) ポリシー。
- 有効な[DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities)レコード。
- 有効な[SPF](https://ja.wikipedia.org/wiki/Sender_Policy_Framework)および[DKIM](https://ja.wikipedia.org/wiki/DKIM)レコード。
- 適切な[DMARC](https://en.wikipedia.org/wiki/DMARC)レコード及びポリシーを設定している、もしくは認証に[ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain)を使用していること。 DMARC認証を使用している場合、ポリシーは`reject`か`quarantine`に設定していること。
- サーバーの暗号スイートがTLS1.2以降であること、及び[RFC8996](https://datatracker.ietf.org/doc/rfc8996)への対応計画があること。
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS)によるメール送信。
- 以下のようなウェブサイトのセキュリティ基準：
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - 外部のドメインから読み込む場合、[サブリソース完全性](https://en.wikipedia.org/wiki/Subresource_Integrity)があること。
- [ヘッダー情報](https://en.wikipedia.org/wiki/Email#Message_header)の表示に対応していること。ヘッダー情報はメールがフィッシングであるか判断する重要なフォレンジック上の特徴である。

**満たされることが望ましい基準：**

- ハードウェア認証のサポート、つまり U2Fおよび[WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online)。
- DANEへの対応と[DNS Certification Authority Authorization（CAA）リソースレコード](https://tools.ietf.org/html/rfc6844)の設定。
- メーリングリストに投稿する際に役立つ[RFC8617](https://tools.ietf.org/html/rfc8617) [Authenticated Received Chain（ARC）](https://en.wikipedia.org/wiki/Authenticated_Received_Chain)が実装されていること。
- 信頼できる第三者機関によるセキュリティ監査を公表
- バグ報奨金プログラム、協調的な脆弱性開示プロセス。
- 以下のようなウェブサイトのセキュリティ基準：
    - [コンテンツセキュリティポリシー（CSP）](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### 信頼

あなたは偽の身分証を持つ人物に自分の財政を託すことはないでしょう。電子メールに関しても、同じことが言えるはずです。 推奨されるサービスプロバイダーには、自社の所有権やリーダーシップについて公表することが求められます。 また、特に政府からの要請がどのように処理されるかについて、透明性の高い報告が頻繁に行われることを望んでいます。

**最低条件：**

- 公的なリーダーシップまたはオーナーシップ。

**満たされることが望ましい基準：**

- 頻繁な透明性レポート。

### マーケティング

推奨するEメールプロバイダーには責任あるマーケティングを求めます。

**最低条件：**

- アナリティクスをセルフホスティングしていること（Google AnalyticsやAdobe Analyticsを使用していないこと）。

以下のような無責任なマーケティングは行ってはなりません：

- 「破れない暗号化」という主張。 暗号化は、その暗号化を破る技術が将来になって現れた際には、それがもはや秘密ではなくなってしまうかもしれないということを念頭に置いて使用されるべきものです。
- 匿名性を100％保証するという主張。 誰かが何かを100％だと主張するとき、それは失敗の確実性が全く存在しないということを意味します。 例えば、以下のような匿名化を簡単に解除する様々な方法があります。

    - 匿名化ソフトウェア（Tor、VPNなど）を使わずにアクセスした個人情報（メールアカウント、ハンドルネームなど）を再利用する
    - [ブラウザーのフィンガープリンティングを行うこと。](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**満たされることが望ましい基準：**

- 二要素認証、メールクライアント、OpenPGPなどの設定に関する明確で読みやすいドキュメント。

### 追加機能

厳密な要件ではありませんが、推奨するサービスプロバイダーを決定する際に考慮した利便性やプライバシーの要素が他にもいくつかあります。
