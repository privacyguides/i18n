---
meta_title: "如何创建私密互联网账户 - 隐私指南"
title: "账户创建"
icon: 'material/account-plus'
description: 在网上创建账户几乎是网络生活的必需品，采取这些步骤来保障您的隐私安全。
---

人们经常不假思索地注册服务。 Maybe it's a streaming service to watch that new show everyone's talking about, or an account that gives you a discount for your favorite fast food place. 无论情况如何，你应该考虑现在和以后对你的数据的影响。

你所使用的每一项新服务都有风险。 数据泄露；向第三方披露客户信息；流氓雇员访问数据；所有这些都是在提供你的信息时必须考虑的可能性。 你需要确信你可以信任该服务，这就是为什么我们不建议将有价值的数据存储在任何东西上，除了最成熟和经过战斗考验的产品。 这通常意味着提供E2EE并经过加密审计的服务。 审计增加了对产品的保证，即产品的设计没有由缺乏经验的开发者造成的明显的安全问题。

在一些服务上删除账户也可能很困难。 有时 [覆盖与一个账户相关的数据](account-deletion.md#overwriting-account-information) ，但在其他情况下，该服务将保留整个账户的变化历史。

## 用户协议和隐私政策

服务条款是你在使用服务时同意遵守的规则。 对于较大的服务，这些规则通常由自动系统执行。 有时这些自动系统会犯错误。 For example, you may be banned or locked out of your account on some services for using a VPN or VoIP number. 对这种禁令提出上诉往往很困难，而且也涉及到一个自动程序，并不总是成功。 这将是我们不建议使用Gmail的电子邮件作为例子的原因之一。 电子邮件对于访问你可能已经注册的其他服务至关重要。

The Privacy Policy is how the service says they will use your data, and it is worth reading so that you understand how your data will be used. 一个公司或组织可能在法律上没有义务遵守政策中的所有内容（这取决于司法管辖区）。 我们建议对你当地的法律有一些了解，以及他们允许供应商收集什么。

我们建议寻找特定的术语，如 "数据收集"、"数据分析"、"cookies"、"广告 "或 "第三方 "服务。 Sometimes you will be able to opt out from data collection or from sharing your data, but it is best to choose a service that respects your privacy from the start.

请记住，你也将你的信任寄托在该公司或组织身上，他们会遵守自己的隐私政策。

## 身份验证方法

通常有多种注册账户的方式，每种方式都有各自的好处和缺点。

### 电子邮件和密码

创建新账户最常见的方式是通过电子邮件地址和密码。 当使用这种方法时，你应该使用一个密码管理器，并遵循 [有关密码的最佳实践](passwords-overview.md)。

<div class="admonition tip" markdown>
<p class="admonition-title">小提示</p>

你还可以使用密码管理器来组织其他验证方法！ 只需添加新条目并填写相应字段，你可以为诸如安全问题或备用密钥之类的事物添加注释。

</div>

你将负责管理你的登录凭证。 为了增加安全性，你可以在你的账户上设置 [MFA](multi-factor-authentication.md)。

[推荐的密码管理器](../passwords.md ""){.md-button}

#### 邮箱别名

如果你不想把你的真实电子邮件地址提供给一个服务，你可以选择使用一个别名。 We describe them in more detail on our email services recommendation page. 本质上，别名服务允许你生成新的电子邮件地址，将所有电子邮件转发到你的主地址。 This can help prevent tracking across services and help you manage the marketing emails that sometimes come with the sign-up process. 这些可以根据它们被发送到的别名自动过滤。

如果一项服务被黑客攻击，你可能会开始收到钓鱼或垃圾邮件到你用来注册的地址。 为每项服务使用独特的别名，可以帮助准确识别什么服务被黑。

[推荐的电子邮件别名服务](../email-aliasing.md ""){.md-button}

### “通过……登录” (OAuth)

[Open Authorization (OAuth)](https://en.wikipedia.org/wiki/OAuth) is an authentication protocol that allows you to register for a service without sharing much information with the service provider, if any, by using an existing account you have with another service instead. 每当你在注册表单上看到类似“通过*提供商名称*登录”的内容时，通常就是在使用OAuth。

当你通过OAuth登录时，它会打开一个登录页面，你选择的提供商和你现有的账户以及新账户将会被连接起来。 你的密码不会共享，但一些基本信息通常会共享（你可以在登录请求期间审查它） 每次你想登录同一个账户时，都需要这个过程。

主要的优点是:

- **Security**: You don't have to trust the security practices of the service you're logging into when it comes to storing your login credentials because they are stored with the external OAuth provider. Common OAuth providers like Apple and Google typically follow the best security practices, continuously audit their authentication systems, and don't store credentials inappropriately (such as in plain text).
- **Ease-of-use**: Multiple accounts are managed by a single login.

但也有弊端:

- **Privacy**: The OAuth provider you log in with will know the services you use.
- **Centralization**: If the account you use for OAuth is compromised, or you aren't able to log in to it, all other accounts connected to it are affected.

OAuth在需要服务之间更深入整合的情况下特别有用。 我们的建议是仅在需要时使用OAuth，并始终使用多因素认证 [MFA](multi-factor-authentication.md) 保护主账户。

使用OAuth的所有服务的安全性将与你的底层OAuth提供商账户的安全性一样。 例如，如果你想用硬件密钥保护一个账户，但该服务不支持硬件密钥，你可以改用硬件密钥保护你用于OAuth的账户，现在你基本上在所有账户上都有硬件MFA。 不过，值得注意的是，如果你的OAuth提供商账户的认证较弱，那么与该登录绑定的任何账户也将是脆弱的。

使用 *Google登录*、*Facebook登录* 或其他服务时还有一个额外的危险，那就是通常OAuth过程允许 *双向* 数据共享。 例如，使用你的Twitter账户登录论坛可能会授权该论坛在你的Twitter账户上进行操作，如发布、阅读你的消息或访问其他个人数据。 OAuth提供商通常会向你展示一个列表，列出你授权外部服务访问的内容，你应该始终确保阅读该列表，并且不要无意中授权外部服务访问它不需要的任何内容。

恶意应用程序，尤其是在移动设备上，这些应用程序可以访问用于登录OAuth提供商的WebView会话，也可以通过劫持你与OAuth提供商的会话并通过这些方式获得对你的OAuth账户的访问来滥用这个过程。 使用任何提供商的 *通过……登录* 选项通常应该被视为一种便利性选择，你只会在信任不会主动恶意行为的服务时使用。

### 手机号

我们建议避免使用那些需要电话号码才能注册的服务。 A phone number can identify you across multiple services and depending on data sharing agreements this will make your usage easier to track, particularly if one of those services is breached as the phone number is often **not** encrypted.

如果可以的话，你应该避免提供你的真实电话号码。 Some services will allow the use of VoIP numbers, however these often trigger fraud detection systems, causing an account to be locked down, so we don't recommend that for important accounts.

在许多情况下，你将需要提供一个可以接收短信或电话的号码，特别是在国际购物时，以防你的订单在边境检查时出现问题。 服务机构使用你的号码作为验证方法是很常见的；不要因为你想耍小聪明，给了一个假的号码，而让自己被锁定在一个重要的账户之外。

### 用户名和密码

有些服务允许你不使用电子邮件地址进行注册，只要求你设置一个用户名和密码。 这些服务在与VPN或Tor结合使用时，可以提供更多的匿名性。 **请记住，对于这些账户，如果你忘记了你的用户名或密码，很可能没有办法恢复你的账户**。
