---
meta_title: "How to Create Internet Accounts Privately - Privacy Guides"
title: "账户创建"
icon: 'material/account-plus'
description: Creating accounts online is practically an internet necessity, take these steps to make sure you stay private.
---

人们经常不假思索地注册服务。 也许它是一个流媒体服务，这样你就可以看到每个人都在谈论的新节目，或者一个为你最喜欢的快餐店提供折扣的账户。 无论情况如何，你应该考虑现在和以后对你的数据的影响。

你所使用的每一项新服务都有风险。 数据泄露；向第三方披露客户信息；流氓雇员访问数据；所有这些都是在提供你的信息时必须考虑的可能性。 你需要确信你可以信任该服务，这就是为什么我们不建议将有价值的数据存储在任何东西上，除了最成熟和经过战斗考验的产品。 这通常意味着提供E2EE并经过加密审计的服务。 审计增加了对产品的保证，即产品的设计没有由缺乏经验的开发者造成的明显的安全问题。

在一些服务上删除账户也可能很困难。 有时 [覆盖与一个账户相关的数据](account-deletion.md#overwriting-account-information) ，但在其他情况下，该服务将保留整个账户的变化历史。

## 用户协议和隐私政策

服务条款是你在使用服务时同意遵守的规则。 对于较大的服务，这些规则通常由自动系统执行。 有时这些自动系统会犯错误。 例如，你可能因为使用VPN或VOIP号码而被禁止或被锁定在某些服务的账户中。 对这种禁令提出上诉往往很困难，而且也涉及到一个自动程序，并不总是成功。 这将是我们不建议使用Gmail的电子邮件作为例子的原因之一。 电子邮件对于访问你可能已经注册的其他服务至关重要。

隐私政策是该服务说他们将如何使用你的数据，它值得阅读，以便你了解你的数据将如何被使用。 一个公司或组织可能在法律上没有义务遵守政策中的所有内容（这取决于司法管辖区）。 我们建议对你当地的法律有一些了解，以及他们允许供应商收集什么。

我们建议寻找特定的术语，如 "数据收集"、"数据分析"、"cookies"、"广告 "或 "第三方 "服务。 有时你可以选择不收集数据或不分享你的数据，但最好是选择一个从一开始就尊重你的隐私的服务。

请记住，你也将你的信任寄托在该公司或组织身上，他们会遵守自己的隐私政策。

## 身份验证方法

通常有多种注册账户的方式，每种方式都有各自的好处和缺点。

### 电子邮件和密码

创建新账户最常见的方式是通过电子邮件地址和密码。 当使用这种方法时，你应该使用一个密码管理器，并遵循 [有关密码的最佳实践](passwords-overview.md)。

!!! tip

    You can use your password manager to organize other authentication methods too! Just add the new entry and fill the appropriate fields, you can add notes for things like security questions or a backup key.

你将负责管理你的登录凭证。 为了增加安全性，你可以在你的账户上设置 [MFA](multi-factor-authentication.md)。

[推荐的密码管理器](../passwords.md ""){.md-button}

#### 邮箱别名

如果你不想把你的真实电子邮件地址提供给一个服务，你可以选择使用一个别名。 我们在我们的电子邮件服务推荐页面上对它们进行了更详细的描述。 本质上，别名服务允许你生成新的电子邮件地址，将所有电子邮件转发到你的主地址。 这可以帮助防止跨服务的追踪，并帮助你管理有时伴随着注册过程的营销电子邮件。 这些可以根据它们被发送到的别名自动过滤。

如果一项服务被黑客攻击，你可能会开始收到钓鱼或垃圾邮件到你用来注册的地址。 为每项服务使用独特的别名，可以帮助准确识别什么服务被黑。

[推荐的电子邮件别名服务](../email.md#email-aliasing-services ""){.md-button}

### "Sign in with..." (OAuth)

OAuth is an authentication protocol that allows you to register for a service without sharing much information with the service provider, if any, by using an existing account you have with another service instead. Whenever you see something along the lines of "Sign in with *provider name*" on a registration form, it's typically using OAuth.

When you sign in with OAuth, it will open a login page with the provider you choose, and your existing account and new account will be connected. Your password won't be shared, but some basic information typically will (you can review it during the login request). 每次你想登录同一个账户时，都需要这个过程。

主要的优点是:

- **Security**: you don't have to trust the security practices of the service you're logging into when it comes to storing your login credentials, because they are stored with the external OAuth provider, which when it comes to services like Apple and Google typically follow the best security practices, continuously audit their authentication systems, and don't store credentials inappropriately (such as in plain text).
- **易用性**：多个账户由一个登录账号管理。

但也有弊端:

- **Privacy**: the OAuth provider you log in with will know the services you use.
- **Centralization**: if the account you use for OAuth is compromised, or you aren't able to log in to it, all other accounts connected to it are affected.

OAuth can be especially useful in those situations where you could benefit from deeper integration between services. Our recommendation is to limit using OAuth to only where you need it, and always protect the main account with [MFA](multi-factor-authentication.md).

All the services that use OAuth will be as secure as your underlying OAuth provider's account. For example, if you want to secure an account with a hardware key, but that service doesn't support hardware keys, you can secure the account you use with OAuth with a hardware key instead, and now you essentially have hardware MFA on all your accounts. It is worth noting though that weak authentication on your OAuth provider account means that any account tied to that login will also be weak.

There is an additional danger when using *Sign in with Google*, *Facebook*, or another service, which is that typically the OAuth process allows for *bidirectional* data sharing. For example, logging in to a forum with your Twitter account could grant that forum access to do things on your Twitter account such as post, read your messages, or access other personal data. OAuth providers will typically present you with a list of things you are granting the external service access to, and you should always ensure that you read through that list and don't inadvertently grant the external service access to anything it doesn't require.

Malicious applications, particularly on mobile devices where the application has access to the WebView session used for logging in to the OAuth provider, can also abuse this process by hijacking your session with the OAuth provider and gaining access to your OAuth account through those means. Using the *Sign in with* option with any provider should usually be considered a matter of convenience that you only use with services you trust to not be actively malicious.

### 手机号

我们建议避免使用那些需要电话号码才能注册的服务。 一个电话号码可以在多个服务中识别你的身份，根据数据共享协议，这将使你的使用情况更容易被追踪，特别是当这些服务之一被破坏时，因为电话号码通常是 **，而不是** 加密。

如果可以的话，你应该避免提供你的真实电话号码。 有些服务会允许使用VOIP号码，但是这些号码往往会触发欺诈检测系统，导致账户被锁定，所以我们不建议重要账户使用这种号码。

在许多情况下，你将需要提供一个可以接收短信或电话的号码，特别是在国际购物时，以防你的订单在边境检查时出现问题。 服务机构使用你的号码作为验证方法是很常见的；不要因为你想耍小聪明，给了一个假的号码，而让自己被锁定在一个重要的账户之外。

### 用户名和密码

有些服务允许你不使用电子邮件地址进行注册，只要求你设置一个用户名和密码。 这些服务在与VPN或Tor结合使用时，可以提供更多的匿名性。 **请记住，对于这些账户，如果你忘记了你的用户名或密码，很可能没有办法恢复你的账户**。
