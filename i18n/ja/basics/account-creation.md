---
meta_title: "プライベートなアカウントを作成する方法 - Privacy Guides"
title: "アカウントの作成"
icon: 'material/account-plus'
description: オンラインでアカウントを作成することは実際のインターネットでは必須であり、プライベートなものであることを確認するために以下のステップに従ってください。
---

多くの場合、何も考えずにサービスへユーザー登録することがあります。 多くの人が話題にしている新番組を見るためのストリーミングサービスかもしれませんし、お気に入りのファーストフード店の割引を受けるためのアカウントかもしれません。 どのような場合でも、データが現在および将来及ぼす影響を考える必要があります。

新しいサービスを利用することにはリスクがあります。 データ漏洩、第三者への顧客情報の開示や不正に従業員がデータにアクセスすることの可能性については、自分の情報を提供する際に考える必要があります。 サービスを信用できるという確信が必要であり、そのため最も成熟し、実践レベルで使われている製品以外に貴重なデータを保存することは推奨しません。 多くの場合、エンドツーエンド暗号化が行われ、暗号化の監査を受けているサービスが該当します。 検査を受けることで、経験の浅い開発者によって引き起こされるセキュリティ上のひどい問題がなく製品が設計されているという保証が高まります。

サービスによってはアカウントの削除が難しい場合もあります。 アカウントに関連する[データの上書き](account-deletion.md#overwriting-account-information)ができる場合もありますが、アカウントの変更履歴をすべて保持するサービスもあります。

## 利用規約 & プライバシーポリシー

利用規約はサービスを利用する際に従うことに同意するルールです。 大規模なサービスにおいては、自動化されたシステムによって実施されることが多いです。 自動化されたシステムは間違えることもあります。 例えばVPNやVoIP番号を利用すると、アカウントが停止されたり、ロックアウトされたりしまうサービスもあります。 アカウント停止に対する申請も自動化されていることがあり、難しいことが多く必ずしも成功するとは限りません。 これは例えばGmailの利用を推奨しない理由の一つです。 メールは登録している他のサービスへアクセスするために非常に重要だからです。

プライバシーポリシーはサービスでデータをどのように使用するかを示したものであり、データがどのように使われるかを理解するために読む価値があります。 企業や組織はポリシーに書かれたすべての内容に従う法的義務を負わないかもしれません（司法管轄によります）。 住んでいる地域の法律やプロバイダーが何の収集を許可されているかをある程度知っておくことを推奨します。

「データ収集」、「データ分析」、「クッキー」、「広告」や「サードパーティ」など特定の用語を探すことを推奨します。 データ収集やデータ共有をオプトアウトすることができる場合もありますが、最初からプライバシーが尊重されているサービスを選ぶことが最も良いです。

企業や組織そのものだけではなく、企業や組織がプライバシーポリシーを遵守することも信用することになることに留意ください。

## 認証方法

アカウントの登録には複数の方法があり、それぞれ利点と欠点があります。

### メールアドレスとパスワード

アカウント作成の最も一般的な方法はメールアドレスとパスワードによるものです。 この方法の場合、パスワードマネージャーを使い、パスワードに関する[ベストプラクティス](passwords-overview.md)に従ってください。

<div class="admonition tip" markdown>
<p class="admonition-title">ヒント</p>

パスワードマネージャーで他の認証方法をまとめることもできます！ 新しいエントリーを追加し、適切な項目を入力し、セキュリティの質問やバックアップキーなどのメモを追加することもできます。

</div>

ログイン認証情報は自分で管理する必要があります。 セキュリティを強化するために、アカウントに[他要素認証](multi-factor-authentication.md)を設定することもできます。

[推奨のパスワードマネージャー](../passwords.md ""){.md-button}

#### 電子メールのエイリアス

本当のメールアドレスをサービスに登録したくない場合、メールエイリアスを使う選択肢もあります。 詳細はメールサービスのページに記載しています。 基本的に、エイリアスサービスではメインのメールアドレスにすべてのメールを転送する新しいメールアドレスを作ることができます。 サービス間でのトラッキングを防ぎ、登録に伴ってついてくるマーケティングメールを処理するのに役立ちます。 送信先のエイリアスに基づいて自動的にフィルタリングすることができます。

サービスがハッキングされた場合、登録したアドレスにフィッシングメールやスパムメールが届くかもしれません。 サービスごとに個別のエイリアスを使うことで、どのサービスがハッキングされたかを正確に特定することができます。

[推奨されるメールエイリアスサービス](../email-aliasing.md ""){.md-button}

### 「他のサービスでサインイン」 (OAuth)

[Open Authorization(OAuth)](https://en.wikipedia.org/wiki/OAuth)はサービスプロバイダーに多くの情報を共有せずに登録できる認証プロトコルで、他のサービスの既存のアカウントを代わりに使うことができます。 登録フォームに「*プロバイダー名*でサインイン」のような表示がある場合、たいていはOAuthを使っています。

OAuthでサインインすると、選択したプロバイダーのログインページが開かれ、既存のアカウントと新しいアカウントが接続されます。 パスワードは共有されませんが、基本的な情報は共有されます（ログイン要求の際に確認できます）。 このプロセスは同じアカウントにログインするたびに必要です。

主な利点は以下の通りです。

- **Security**: You don't have to trust the security practices of the service you're logging into when it comes to storing your login credentials because they are stored with the external OAuth provider. Common OAuth providers like Apple and Google typically follow the best security practices, continuously audit their authentication systems, and don't store credentials inappropriately (such as in plain text).
- **Ease-of-use**: Multiple accounts are managed by a single login.

しかし、以下のデメリットもあります。

- **Privacy**: The OAuth provider you log in with will know the services you use.
- **Centralization**: If the account you use for OAuth is compromised, or you aren't able to log in to it, all other accounts connected to it are affected.

OAuth can be especially useful in those situations where you could benefit from deeper integration between services. Our recommendation is to limit using OAuth to only where you need it, and always protect the main account with [MFA](multi-factor-authentication.md).

All the services that use OAuth will be as secure as your underlying OAuth provider's account. For example, if you want to secure an account with a hardware key, but that service doesn't support hardware keys, you can secure the account you use with OAuth with a hardware key instead, and now you essentially have hardware MFA on all your accounts. It is worth noting though that weak authentication on your OAuth provider account means that any account tied to that login will also be weak.

There is an additional danger when using *Sign in with Google*, *Facebook*, or another service, which is that typically the OAuth process allows for *bidirectional* data sharing. For example, logging in to a forum with your Twitter account could grant that forum access to do things on your Twitter account such as post, read your messages, or access other personal data. OAuth providers will typically present you with a list of things you are granting the external service access to, and you should always ensure that you read through that list and don't inadvertently grant the external service access to anything it doesn't require.

Malicious applications, particularly on mobile devices where the application has access to the WebView session used for logging in to the OAuth provider, can also abuse this process by hijacking your session with the OAuth provider and gaining access to your OAuth account through those means. Using the *Sign in with* option with any provider should usually be considered a matter of convenience that you only use with services you trust to not be actively malicious.

### 電話番号

We recommend avoiding services that require a phone number for sign up. A phone number can identify you across multiple services and depending on data sharing agreements this will make your usage easier to track, particularly if one of those services is breached as the phone number is often **not** encrypted.

You should avoid giving out your real phone number if you can. Some services will allow the use of VoIP numbers, however these often trigger fraud detection systems, causing an account to be locked down, so we don't recommend that for important accounts.

In many cases you will need to provide a number that you can receive SMS or calls from, particularly when shopping internationally, in case there is a problem with your order at border screening. It's common for services to use your number as a verification method; don't let yourself get locked out of an important account because you wanted to be clever and give a fake number!

### ユーザー名とパスワード

Some services allow you to register without using an email address and only require you to set a username and password. These services may provide increased anonymity when combined with a VPN or Tor. Keep in mind that for these accounts there will most likely be **no way to recover your account** in the event you forget your username or password.
