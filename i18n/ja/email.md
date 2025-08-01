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

| プロバイダー                      | OpenPGP / WKD                          | IMAP / SMTP                                        | ゼロアクセス暗号化                                        | 匿名での支払方法                  |
| --------------------------- | -------------------------------------- | -------------------------------------------------- | ------------------------------------------------ | ------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } 有料プランのみ | :material-check:{ .pg-green }                    | 現金                        |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                      | :material-information-outline:{ .pg-blue } メールのみ | 現金                        |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }             | :material-check:{ .pg-green }                    | Monero<br>第三者経由での現金 |

推奨するEメールプロバイダーに加え（もしくは代わりに）、プライバシー保護のために[Eメールエイリアスサービス](email-aliasing.md#recommended-providers)を検討してください。 特に、スパムから実際の受信トレイを保護し、企業のマーケティング活動によるアカウントの関連付けを防ぎ、すべての受信メールをPGPで暗号化することができます。

- [詳細 :material-arrow-right-drop-circle:](email-aliasing.md)

## OpenPGP対応サービス

OpenPGPによる暗号化・復号化や[Web Key Directory(WKD)標準](basics/email-security.md#what-is-the-web-key-directory-standard)をネイティブサポートしているプロバイダーでは、プロバイダーに依存しないエンドツーエンド暗号化メールが利用可能です。 例えば、Proton MailのユーザはMailbox.orgのユーザにE2EEメッセージを送れますし、OpenPGPで暗号化された通知を、それをサポートするインターネットサービスから受け取ることができます。

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">注意</p>

OpenPGPのようなE2EE（エンドツーエンド暗号化）を利用しても、件名などを含むメールのヘッダーには暗号化されていないメタデータが残ります！ 詳細は [電子メールのメタデータ](basics/email-security.md#email-metadata-overview)のページにあります。

OpenPGPは前方秘匿性に対応していないため、送信者か受信者の秘密鍵が盗まれた場合、その秘密鍵で暗号化した過去すべてのメッセージの暗号化が解除できる状態となります。

- [秘密鍵を保護するには？](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** は、プライバシー、暗号化、セキュリティ、使いやすさを重視したメールサービスです。 2013年からサービスが稼働しました。 Proton AGはスイスのジュネーブを拠点としています。

Proton の無償プランのメールストレージは500MBから始まり、無料で1GBまで増やすことができます。

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

無償アカウントには本文の検索ができないことや、 [推奨されるデスクトップメールクライアント](email-clients.md) (Thunderbirdなど)を使用するために必要な [Proton Mail Bridge](https://proton.me/mail/bridge) を利用できないといった制限があります。 有料アカウントにはProton Mail Bridge、追加ストレージ、カスタムドメインのサポートなどの機能が含まれています。 Proton Unlimitedプランや複数ユーザープランの場合、[SimpleLogin](email-aliasing.md#simplelogin)も無料で利用できます。

[Securitum](https://research.securitum.com)により2021年11月9日 [監査証明書](https://proton.me/blog/security-audit-all-proton-apps) がProton Mailアプリにおくられました。

Proton Mailのクラッシュレポートは第三者に共有**されません**。 これはウェブアプリで無効にすることができます：:gear: → **すべての設定** → **アカウント** → **セキュリティとプライバシー** → **プライバシーとデータ収集**。

#### :material-check:{ .pg-green } カスタムドメインとエイリアス

Proton Mailの有料会員は独自ドメインでサービスや [キャッチオール](https://proton.me/support/catch-all) アドレスを使うことができます。 Proton Mailはドメインを購入したくない場合に有用な[サブアドレス](https://proton.me/support/creating-aliases)に対応しています。

#### :material-check:{ .pg-green } プライベートな支払い方法

Proton Mailは郵送による**現金**やクレジットカード・デビットカードの支払いに加え、[Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc)やPayPalでの支払いも[受け付けています](https://proton.me/support/payment-options)。

#### :material-check:{ .pg-green } アカウントのセキュリティ

Proton MailはFIDO2やU2Fを用いたTOTP[二要素認証](https://proton.me/support/two-factor-authentication-2fa)や[ハードウェアセキュリティキー](https://proton.me/support/2fa-security-key)に対応しています。 ハードウェアセキュリティキーを使用するには、先にTOTP二要素認証の設定が必要です。

#### :material-check:{ .pg-green } データのセキュリティ

Proton Mailはメールと [カレンダー](https://proton.me/news/protoncalendar-security-model) を [ゼロアクセス暗号化](https://proton.me/blog/zero-access-encryption) します。 ゼロアクセス暗号化で保護されたデータにアクセスできるのはあなただけです。

ディスプレイネームやメールアドレスなど、 [Proton Contacts](https://proton.me/support/proton-contacts) に保存される一部の情報はゼロアクセス暗号化によって保護されていません。 電話番号など、ゼロアクセス暗号化をサポートするContactフィールドには南京錠のアイコンが表示されます。

#### :material-check:{ .pg-green } メールの暗号化

Proton Mailはwebメールに [OpenPGP暗号化を組み込んでいます。](https://proton.me/support/how-to-use-pgp) 他のProton Mailアカウントへのメールは自動的に暗号化され、OpenPGPキーによる非Proton Mailアドレスへの暗号化はアカウント設定から簡単に有効化できます。 ProtonはWKDによる外部の鍵の自動探索にも対応しています。 WKDを使った他のプロバイダーに送信されるEメールは自動的にOpenPGPで暗号化され、PGP公開鍵と連絡先を手動で交換する必要はありません。 また、[Proton Mailではないアドレスに送るメッセージをOpenPGPを使わずに暗号化する](https://proton.me/support/password-protected-emails)こともでき、受信者はProton Mailアカウントへのサインアップが必要ありません。

Proton MailではProtonアカウントの公開鍵をWKDからHTTP経由で公開します。 Proton Mailを使っていない人でもProton MailのOpenPGP鍵を簡単に見つけることができ、プロバイダーをまたいだエンドツーエンド暗号化が可能になります。 `@proton.me`のようなProtonが所有するドメインで終わるEメールアドレスのみ対象です。 カスタムドメインを使用する場合、別途[WKDの設定](basics/email-security.md#what-is-the-web-key-directory-standard)が必要になります。

#### :material-information-outline:{ .pg-blue } アカウントの停止

有料アカウントを持っており、しかし14日を過ぎても [請求への支払いが無い](https://proton.me/support/delinquency) 場合、データにアクセスできなくなります。 30日を過ぎるとアカウントは滞納者となり、受信メールは届かなくなります。 この期間も請求は継続されます。 Protonは1年間[アクティブではないフリープランのアカウントを削除します](https://proton.me/support/inactive-accounts)。 削除されたアカウントのメールアドレスは再利用**できません**。

#### :material-information-outline:{ .pg-blue } 追加機能

Proton Mailの[Unlimited](https://proton.me/support/proton-plans#proton-unlimited)プランでは複数のカスタムドメイン、無制限のEメールエイリアスや500GBのストレージに加え、その他のProtonサービスを利用することができます。

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org**は安全性、広告がないこと、100%エコフレンドリーなエネルギーであることを重視したEメールサービスです。 2014年から運営をされています。 Mailbox.orgはドイツのベルリンに拠点を置いています。

各アカウントには最大2GBのストレージが割当てられ、必要に応じてアップグレードできます。

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

Mailbox.orgは決済プロセッサBitPayがドイツでの業務を停止したために暗号通貨を受け付けていません。 郵送による**現金払い**、銀行口座への**銀金払い**、銀行振込、クレジットカード、Paypalとドイツの支払いサービスであるPaydirektとSofortüberweisungに対応しています。

#### :material-check:{ .pg-green } アカウントのセキュリティ

Mailbox.orgはウェブメールに限り、[二要素認証](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa)に対応しています。 TOTPもしくは[YubiCloud](https://yubico.com/products/services-software/yubicloud)経由の[YubiKey](https://en.wikipedia.org/wiki/YubiKey)を利用できます。 [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online)などのウェブ標準にはまだ対応していません。

#### :material-information-outline:{ .pg-blue } データのセキュリティ

Mailbox.orgでは[暗号化されたメールボックス](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox)により受信メールを暗号化することができます。 新しいメッセージを受信するとすぐにあなたの公開鍵で暗号化されます。

ただし、Mailbox.orgが利用している[Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange)はアドレス帳やカレンダーの暗号化に[対応していません](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book)。 [カレンダーサービス](calendar.md)のほうが情報をより適切に扱えるかもしれません。

#### :material-check:{ .pg-green } メールの暗号化

Mailbox.orgのウェブメールは[暗号化機能が組みこまれており](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard)、OpenPGP公開鍵を持つ人へのメッセージの送信が簡単にできます。 Mailbox.orgのサーバー上で[受信者がEメールの復号化をすることもできます](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp)。 この機能はリモートの受信者がOpenPGPを持っておらず、自分のメールボックスにあるメールのコピーを複合できない場合に便利です。

Mailbox.orgはWKDによりHTTP経由で公開鍵を探索することにも対応しています。 Mailbox.orgを使っていない人でもMailbox.orgのOpenPGP鍵を簡単に見つけることができ、プロバイダーをまたいだエンドツーエンド暗号化が可能になります。 `@mailbox.org`のようなMailbox.orgが小勇するドメインで終わるメールアドレスのみ対象です。 カスタムドメインを使用する場合、別途[WKDの設定](basics/email-security.md#what-is-the-web-key-directory-standard)が必要になります。

#### :material-information-outline:{ .pg-blue } アカウントの停止

契約が終了すると、アカウントは制限付きユーザーアカウントになります。 [30日後](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract)に取消不可能な形で削除されます。

#### :material-information-outline:{ .pg-blue } 追加機能

Mailbox.orgの[.onionサービス](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org)を利用し、IMAP/SMTP経由でMailbox.orgのアカウントにアクセスできます。 ただし、.onionサービスからウェブメールにはアクセスできず、TLS証明書エラーが発生する可能性があります。

すべてのアカウントで[暗号化可能な](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive)制限付きクラウドストレージが利用できます。 Mailbox.orgには[@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely)というメールサーバー間の接続にTLS暗号化が必須であるエイリアスもあり、TLS暗号化がなければメッセージは全く送信できません。 Mailbox.orgはIMAPやPOP3のような標準的なアクセスプロトコルに加え、 [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) もサポートしています。

Mailbox.orgの全てのプランにはデジタル遺産機能があります。 相続人が申請し、遺言状が提出されることを条件に、利用者のデータを相続人に渡すこともできます。 または、名前と住所で人を指名することもできます。

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

無料アカウントは1GBのストレージが利用できます。

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

TutaはクレジットカードもしくはPaypalのみ受け付けていますが、ProxyStoreとの[提携](https://tuta.com/support/#cryptocurrency)により、[**暗号通貨**](cryptocurrency.md)でギフトカードを購入することができます。

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

## 規準

**推奨するプロバイダーとは提携していないことに注意してください。**[標準的な基準](about/criteria.md)に加え、業界におけるベストプラクティスの実施や新しい技術の採用などを含む、推奨するために必要なEメールプロバイダーへの明確な要件を定めています。 Eメールプロバイダーを選ぶ前に以下のリストを理解し、どのEメールプロバイダーが適切であるかを調べ、確認してください。

### テクノロジー

安全で最適なサービスのために以下の機能が重要であると考えています。 You should consider whether the provider has the features you require.

**最低条件：**

- ゼロアクセス暗号化によりEメールアカウントのデータを暗号化していること。
- [Mbox](https://en.wikipedia.org/wiki/Mbox)もしくは[RFC5322](https://datatracker.ietf.org/doc/rfc5322)に基づいた個別の.EMLファイルとしてエクスポートできること。
- ユーザーの独自[ドメイン名](https://en.wikipedia.org/wiki/Domain_name)が利用できること。 プロバイダーが悪化したり、プライバシーを重視しない他の会社に買収されたりした場合に備えることができるため、カスタムドメイン名はユーザーにとって非常に重要である。
- 自社所有のインフラで運用されていること。第三者のEメールサービスプロバイダーによるサービス提供ではないこと。

**満たされることが望ましい基準：**

- ゼロアクセス暗号化により、すべてのアカウントのデータ（連絡先、カレンダーなど）が暗号化されていること。
- 利便性のため、エンドツーエンド暗号化・PGP暗号化されたウェブメールサービスが提供されること。
- HTTP経由でのOpenPGP公開鍵の探索をしやすくするため、WKDへ対応していること。 GnuPGでは次のコマンドで鍵を取得できます： `gpg --locate-key example_user@example.com`。
- 外部ユーザー用の一時的なメールボックスがあること。 暗号化されたメールのコピーを送ることなく、暗号化されたメールを送る際に役立ちます。 通常の場合、一時的なメールボックスのメールには期限があり、自動的に削除されます。 また、受信者はOpenPGPのような暗号化を設定する必要がありません。
- [サブアドレス](https://en.wikipedia.org/wiki/Email_address#Sub-addressing)に対応していること。
- ユーザーの独自[ドメイン名](https://en.wikipedia.org/wiki/Domain_name)が利用できること。 プロバイダーが悪化したり、プライバシーを重視しない他の会社に買収されたりした場合に備えることができるため、カスタムドメイン名はユーザーにとって非常に重要である。
- 独自ドメインを利用した際、キャッチオール機能もしくはエイリアス機能があること。
- IMAP、SMTPや[JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol)などの標準的なEメールプロトコルを使用していること。 標準的なプロトコルを採用していることで、他のプロバイダーへ変更する際にすべてのメールを簡単にダウンロードすることができます。
- Eメールプロバイダーのサービスは[onion service](https://en.wikipedia.org/wiki/.onion)経由で利用できること。

### プライバシー

私たちは、推奨するサービスプロバイダーができるだけデータを収集しないことを望んでいます。

**最低条件：**

- 送信者のIPアドレスが保護されていること。`Received`ヘッダーフィールドに表示されないようフィルタリングすることを含む。
- ユーザー名とパスワード以外に、個人情報(PII)を必要としないこと。
- プライバシーポリシーがGDPRの要件を満たしていること。

**満たされることが望ましい基準：**

- [匿名の支払い方法](advanced/payments.md)（[暗号通貨](cryptocurrency.md)、現金、ギフトカードなど）を受け入れていること。
- 強力なEメールプライバシー保護法がある司法権区域でホスティングされていること。

### セキュリティー

メールサーバーは機密性の高いデータを大量に扱います。 プロバイダーが顧客を保護するために業界のベストプラクティスを採用することを期待しています。

**最低条件：**

- [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp)などの二要素認証によりウェブメールが保護されていること。
- 保存データの暗号化に基づく、ゼロアクセス暗号化。 プロバイダーは保有するデータの復号鍵を持たないこと。 不正を働く従業員がアクセスしたデータを流出させたり、遠隔地の敵対者がサーバーに不正アクセスして盗んだデータを公開したりすることを防ぐことができます。
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions)のサポート。
- [Hardenize](https://hardenize.com)や[testssl.sh](https://testssl.sh)、[Qualys SSL Labs](https://ssllabs.com/ssltest)などのツールでプロファイリングした際にTLSエラーや脆弱性がないこと。証明書関連のエラーや[Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security))の原因となった弱いDHパラメーターを含みます。
- サーバーの暗号スイート設定が（TLS1.3では任意となっている）前方秘匿性と認証付き暗号に対応する強力な暗号スイートを優先していること。
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

- ハードウェア認証への対応。例： U2Fおよび[WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online)。
- DANEへの対応と[DNS Certification Authority Authorization（CAA）リソースレコード](https://tools.ietf.org/html/rfc6844)の設定。
- メーリングリストに投稿するのに役立つ[RFC8617](https://tools.ietf.org/html/rfc8617) [Authenticated Received Chain（ARC）](https://en.wikipedia.org/wiki/Authenticated_Received_Chain)が実装されていること。
- 信頼できる第三者機関によるセキュリティ監査を公表していること。
- バグ報奨金プログラム、協調的な脆弱性開示プロセス。
- 以下のようなウェブサイトのセキュリティ基準：
    - [コンテンツセキュリティポリシー（CSP）](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### 信頼

偽の身分証を持つ人に資金管理を託すことはないと思いますが、メールに関しても同じことが言えます。 推奨されるサービスプロバイダーには、自社の所有権やリーダーシップについて公表することが求められます。 また、特に政府からの要請がどのように処理されるかについて、透明性の高い報告が頻繁に行われることを望んでいます。

**最低条件：**

- 公的なリーダーシップまたはオーナーシップ。

**満たされることが望ましい基準：**

- 頻繁な透明性レポート。

### マーケティング

推奨するEメールプロバイダーには責任あるマーケティングを求めます。

**最低条件：**

- アナリティクスをセルフホスティングしていること（Google AnalyticsやAdobe Analyticsを使用していないこと）。
- 以下のような無責任なマーケティングは行っていないこと：
    - 「解読不可能な暗号化」と主張すること。 暗号化は、その暗号化を解読する技術が将来に現れた際には、もはや秘密ではなくなってしまうかもしれないということを念頭に置いて使用されるべきものです。
    - 匿名性を100％保証すると主張すること。 100%であるということを主張することは、失敗する可能性が全くないことを意味します。 匿名化を無意味にしてしまう様々な方法があります。例えば：
        - Torなどの匿名化ソフトウェアを使わずにアクセスした個人情報（メールアカウント、ハンドルネームなど）を再利用する
        - [ブラウザーのフィンガープリンティングを行うこと。](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**満たされることが望ましい基準：**

- 二要素認証、メールクライアント、OpenPGPなどの設定に関する明確で読みやすいドキュメントがあること。

### 追加機能

厳密な要件ではありませんが、推奨するサービスプロバイダーを決める際には利便性やプライバシーの要素を考慮します。
