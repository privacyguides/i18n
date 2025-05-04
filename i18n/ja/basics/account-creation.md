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

There are usually multiple ways to sign up for an account, each with their own benefits and drawbacks.

### メールアドレスとパスワード

The most common way to create a new account is by an email address and password. When using this method, you should use a password manager and follow [best practices](passwords-overview.md) regarding passwords.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

You can use your password manager to organize other authentication methods too! Just add the new entry and fill the appropriate fields, you can add notes for things like security questions or a backup key.

</div>

You will be responsible for managing your login credentials. For added security, you can set up [MFA](multi-factor-authentication.md) on your accounts.

[推奨のパスワードマネージャー](../passwords.md ""){.md-button}

#### 電子メールのエイリアス

If you don't want to give your real email address to a service, you have the option to use an alias. We describe them in more detail on our email services recommendation page. Essentially, alias services allow you to generate new email addresses that forward all emails to your main address. This can help prevent tracking across services and help you manage the marketing emails that sometimes come with the sign-up process. Those can be filtered automatically based on the alias they are sent to.

Should a service get hacked, you might start receiving phishing or spam emails to the address you used to sign up. Using unique aliases for each service can assist in identifying exactly what service was hacked.

[Recommended email aliasing services](../email-aliasing.md ""){.md-button}

### "Sign in with..." (OAuth)

[Open Authorization (OAuth)](https://en.wikipedia.org/wiki/OAuth) is an authentication protocol that allows you to register for a service without sharing much information with the service provider, if any, by using an existing account you have with another service instead. Whenever you see something along the lines of "Sign in with *provider name*" on a registration form, it's typically using OAuth.

When you sign in with OAuth, it will open a login page with the provider you choose, and your existing account and new account will be connected. Your password won't be shared, but some basic information typically will (you can review it during the login request). This process is needed every time you want to log in to the same account.

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
