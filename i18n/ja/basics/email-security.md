---
meta_title: "Eメールがプライバシーやセキュリティの観点で最良でない理由 - Privacy Guides"
title: Eメールのセキュリティー
icon: material/email
description: Eメールは安全でない点がいくつもあります。本記事では、安全な連絡手段としてEメールを推奨しない理由を紹介します。
---

Eメールは、普通に使用すると、コミュニケーション手段として安全ではありません。 Eメールにエンドツーエンド暗号化を施すOpenPGPのようなツールを使用することで、Eメールのセキュリティを向上させることはできますが、他のメッセージアプリケーションにおける暗号化と比較すると、OpenPGPには様々な欠点があります。

そのため、Eメールは、人とのコミュニケーション手段ではなく、登録したオンラインサービスからのトランザクションメール（通知メールや確認メール、パスワードリセットなど）を受け取る手段として使うのが最適です。

## 電子メールの暗号化の概要

２つの異なるEメールプロバイダー間で送られるEメールをE2E暗号化する標準的な方法はOpenPGPです。 OpenPGPの標準を実装したものにはいろいろなものがありますが、一番一般的なのが[GnuPG](../encryption.md#gnu-privacy-guard)と[OpenPGP.js](https://openpgpjs.org)です。

OpenPGPを使ったとしても、[前方秘匿性](https://ja.wikipedia.org/wiki/Forward_secrecy)がないため、もし送受信者のどちらかの秘密鍵が盗まれると、その鍵で暗号化された過去のメッセージがすべて復号できてしまいます。 このため、人対人の連絡手段としては、Eメールよりも、前方秘匿性のある[インスタントメッセンジャー](../real-time-communication.md)を推奨します。

他にも、ビジネスでよく使われている規格として[S/MIME](https://ja.wikipedia.org/wiki/S/MIME)がありますが、使用するには[認証局](https://ja.wikipedia.org/wiki/%E8%AA%8D%E8%A8%BC%E5%B1%80)から発行された証明書が必要です（すべての認証局がS/MIME証明書を発行しているわけではないですし、発行のため年会費を払う必要がある場合が多いです）。 S/MIMEの方がPGPよりも使い勝手いい場合もあります。Appleのメールアプリ、[Google Workplace](https://support.google.com/a/topic/9061730)、[Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480)などの広く使われているEメールアプリケーションが、S/MIMEに対応しています。 しかし、PGPと同じくS/MIMEは前方秘匿性がなく、PGPと比較しても安全性が特に高いわけではありません。

## Web Key Directory規格とは？

[Web Key Directory (WKD)](https://wiki.gnupg.org/WKD)規格とは、異なるプロバイダーでホストされている他のメールボックスのOpenPGP鍵をEメールクライアントから取得できるようにする仕組みです。 EメールクライアントがWKDに対応していれば、宛先のアドレスのドメインに基づいて、宛先のサーバーに鍵を要求します。 例えば、`jonah@privacyguides.org`にメールを送る場合、クライアントが`privacyguides.org`に対してJonahのOpenPGP鍵を要求し、もし`privacyguides.org`がそのアカウントの鍵を持っていれば、自動的にメールが暗号化されます。

[推奨Eメールクライアント](../email-clients.md)はWKDに対応していますが、他にも、一部のWebメールプロバイダーがWKDに対応しています。 *自分の*鍵がWKDで公開されているかどうかは、ドメインの設定に依存します。 If you use an [email provider](../email.md#openpgp-compatible-services) which supports WKD, such as Proton Mail or Mailbox Mail, they can publish your OpenPGP key on their domain for you.

カスタムドメインを使用している場合は、WKDを別途設定する必要があります。 自分が管理しているドメインであれば、Eメールプロバイダーに関わらずWKDを設定できます。 簡単に設定するには、`keys.openpgp.org`サーバーの「[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)」機能を使うという手があります。具体的には、自分のドメインの`openpgpkey`サブドメインのCNAMEレコードを`wkd.keys.openpgp.org`に向けて、 [keys.openpgp.org](https://keys.openpgp.org)に自分の鍵をアップロードすればOKです。 もしくは、[WKDを自分のウェブサーバーでホストする](https://wiki.gnupg.org/WKDHosting)こともできます。

もしWKDに非対応、かつドメイン共有型のプロバイダーを使っている場合(`@gmail.com`など)は、上記の方法ではOpenPGP鍵を共有することはできません。

### E2E暗号化に対応しているEメールクライアントは？

IMAPやSMPTなどの標準的なプロトコルに対応しているEメールプロバイダーであれば、[推奨Eメールクライアント](../email-clients.md)のどれを使用しても問題ありません。 認証方式によっては、セキュリティの低下に繋がってしまいます。プロバイダーもしくはクライアントが[OAuth](account-creation.md#sign-in-with-oauth)やブリッジアプリケーションに対応していない場合、通常のパスワード認証となるため、[多段階認証](multi-factor-authentication.md)が使用できません。

### 秘密鍵を保護するには？

スマートカード（[YubiKeyや](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) [Nitrokey](../security-keys.md#nitrokey)など）は、以下のように動作します。まず、EメールクライアントもしくはWebメールクライアントを実行しているデバイス（スマホ、タブレット、コンピュータなど）が、暗号化されたメールをスマートカードに送ります。 そしてスマートカードがメールを復号化し、デバイスに送り返します。

復号化をスマートカード上で行うことで、デバイスが感染したとしても秘密鍵が漏れるのを防ぐことができるという利点があります。

## 電子メールのメタデータの概要

メールのメタデータは[ヘッダー](https://ja.wikipedia.org/wiki/%E9%9B%BB%E5%AD%90%E3%83%A1%E3%83%BC%E3%83%AB#%E3%83%98%E3%83%83%E3%83%80%E3%83%BC%E6%83%85%E5%A0%B1)に含まれています。`To`、`From`、`Cc`、`Date`、`Subject`のようなヘッダーは表示されるので、あなたも見たことがあるかもしれません。 他にも、Eメールクライアントやプロバイダーによって付加される隠れたヘッダーがあり、これがあなたのアカウントに関する情報を漏らしてしまう可能性があります。

クライアントはメールのメタデータに基づいて送信者や受信日時を表示することがあります。 サーバーは、メタデータを使ってメールの送信先を判定したり、[他の用途](https://en.wikipedia.org/wiki/Email#Message_header)にも使用することがあります。

### メールのメタデータは誰から見える？

メールのメタデータは、[STARTTLS](https://ja.wikipedia.org/wiki/STARTTLS)によって外部から見えないように保護されますが、クライアントソフトウェア（またはウェブメール）や、メールプロバイダ、メッセージを中継するサーバーからは、見ることができます。 メールサーバーは、スパム防止のために外部のサービスを利用することもあり、そのサービスにもメールの内容が通常見えます。

### メタデータをE2E暗号化できないのはなぜ？

Email metadata is crucial to the most basic functionality of email (where it came from, and where it has to go). E2EE was not built into standard email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
