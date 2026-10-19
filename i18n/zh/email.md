---
meta_title: "加密私人电子邮箱推荐- Privacy Guides"
title: 电子邮件服务
icon: material/email
description: 这些电子邮件服务商为您提供了一个安全存储邮件的绝佳场所，其中许多还支持与其他服务商互操作的 OpenPGP 加密功能。
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>可防御以下威胁：</small>

- [:material-server-network: 服务提供商](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

电子邮件实际上是使用任何在线服务的必需品，但我们不建议使用它进行人与人之间的对话。与其使用电子邮件与他人联系，不如考虑使用支持前向保密的即时通讯媒介。

[推荐的即时通讯工具](real-time-communication.md ""){.md-button}

## 推荐的供应商

对于其他一切，我们根据可持续的商业模式和内置的安全和隐私功能，推荐各种电子邮件供应商。阅读我们的[完整标准列表](#criteria)了解更多信息。

| 提供商                           | OpenPGP / WKD                          | IMAP / SMTP                                      | 加密存储                                             | 匿名支付方式                        |
| ----------------------------- | -------------------------------------- | ------------------------------------------------ | ------------------------------------------------ | ----------------------------- |
| [Proton Mail](#proton-mail)   | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } 仅付费方案 | :material-check:{ .pg-green }                    | 现金、<br>通过第三方支付门罗币       |
| [Mailbox Mail](#mailbox-mail) | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                    | :material-information-outline:{ .pg-blue } 仅邮件加密 | 现金                            |
| [Tuta](#tuta)                 | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }           | :material-check:{ .pg-green }                    | 通过第三方使用门罗币<br>通过第三方使用现金 |

除了（或代替）本文推荐的电子邮件服务商外，您不妨考虑使用专门的[邮件别名服务](email-aliasing.md#recommended-providers)来保护您的隐私。这些服务除其他作用外，还能帮助保护您的真实收件箱免受垃圾邮件侵扰，防止营销人员将您的账户关联起来，并使用PGP对所有收到的邮件进行加密。

- [更多信息 :material-arrow-right-drop-circle:](email-aliasing.md)

## OpenPGP 兼容服务

这些服务商原生支持 OpenPGP 加密/解密以及[Web Key Directory（WKD）标准](basics/email-security.md#what-is-the-web-key-directory-standard)，从而能够实现与服务商无关的端到端加密电子邮件。例如，Proton Mail 用户可以向 Mailbox Mail 用户发送一条端到端加密消息，或者您可以从支持该功能的互联网服务中接收经过 OpenPGP 加密的通知。

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](#proton-mail)
- ![Mailbox Mail logo](assets/img/email/mailbox-mail.svg){ .twemoji } [Mailbox Mail](#mailbox-mail)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

当使用像OpenPGP这样的E2EE技术时，电子邮件仍然会有一些元数据没有在电子邮件的标题中进行加密。了解更多关于[电子邮件元数据](basics/email-security.md#email-metadata-overview)的信息。

此外，OpenPGP 不支持前向保密，这就意味着一旦您的私钥或消息接收方的私钥被盗，所有此前使用这些私钥加密的消息都会泄露。

- [如何保护我的私钥？](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

! [Proton Mail徽标] (assets/img/email/protonmail.svg) {align = right}

* * Proton Mail * *是一项专注于隐私、加密、安全性和易用性的电子邮件服务。它们自2013年以来一直处于运营状态。 Proton AG 总部位于瑞士日内瓦。

“Proton Free”套餐提供 500 MB 的邮件存储空间，您可以免费将其扩容至 1 GB。

[:octicons-home-16: 首页](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion服务" }
[:octicons-eye-16:](https://proton.me/mail/privacy-policy){ .card-link title="隐私政策" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title="文档"}
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="源代码" }

<details class="downloads" markdown>
<summary>下载</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

其免费账户存在一些限制，比如不能搜索正文，不能访问 [Proton Mail Bridge](https://proton.me/mail/bridge)，这是使用 [推荐的桌面邮件客户端](email-clients.md) 所必需的，如Thunderbird等客户端。付费账户包含 Proton Mail Bridge、额外存储空间和自定义域名支持等功能。 “Proton Unlimited”套餐或任何多用户版 Proton 套餐均包含[SimpleLogin](email-aliasing.md#simplelogin)Premium 的使用权限。

这是2021年11月[Securitum](https://research.securitum.com)为Proton Mail的应用提供的[认证函](https://res.cloudinary.com/dbulfrlrz/images/v1714639878/wp-pme/letter-of-attestation-proton-mail-20211109_3138714c61/letter-of-attestation-proton-mail-20211109_3138714c61.pdf)。

Proton Mail 自带内部崩溃报告，这些报告**不会**与第三方共享，并且可以关闭。

=== “网页端” ===

    在您的收件箱中，选择 :gear: → **所有设置** → **账户** → **安全与隐私** → **隐私与数据收集**。

    - [ ] 禁用**收集使用情况诊断信息**
    - [ ] 禁用**“发送崩溃报告**”功能

=== “移动端” ===

    在收件箱中，选择 :material-menu: → :gear: **设置** → 选择您的用户名。

    - [ ] 禁用**“发送崩溃报告**”功能
    - [ ] 禁用**收集使用情况诊断信息**

#### :material-check:{ .pg-green } 自定义域名和别名

Proton Mail的付费用户可以在该服务中使用自己的域名或[通配符邮箱](https://proton.me/support/catch-all)地址。 Proton Mail 还支持[邮件别名功能](https://proton.me/support/creating-aliases)，这对不想购买域名的人来说非常有用。

#### :material-check:{ .pg-green } 保护隐私的支付方式

除了标准的信用卡/借记卡、[比特币](advanced/payments.md#other-coins-bitcoin-ethereum-etc)和PayPal支付方式外，Proton Mail还[接受](https://proton.me/support/payment-options)邮寄**现金**。此外，您还可以使用 [**门罗币**](cryptocurrency.md#monero) 通过其[官方](https://discuss.privacyguides.net/t/add-monero-as-an-anonymous-payment-method-for-proton-services/31058/15)经销商[ProxyStore](https://dys2p.com/en/2025-09-09-proton.html)购买Proton Mail Plus或Proton Unlimited的代金券。

#### :material-check:{ .pg-green } 账户安全

Proton Mail 支持基于 FIDO2 或 U2F 标准的 TOTP[双因素认证](https://proton.me/support/two-factor-authentication-2fa)以及[硬件安全密钥](https://proton.me/support/2fa-security-key)。要使用硬件安全密钥，需要先设置TOTP双因素认证。

#### :material-check:{ .pg-green } 数据安全

Proton Mail 采用基于 PGP 的加密技术存储您的[邮件](https://proton.me/blog/zero-access-encryption)和[日历](https://proton.me/news/protoncalendar-security-model)，只有您本人拥有解密密钥，才能在以后访问这些内容。

存储在[Proton 联系人](https://proton.me/support/proton-contacts)中的某些信息（例如显示名称和电子邮件地址）**并未**使用您自己的加密密钥进行加密，因此 Proton 可以读取这些信息。使用您自己的加密密钥进行保护的联系字段（例如电话号码）会显示一个挂锁图标。

#### :material-check:{ .pg-green } 邮件加密

Proton Mail 已在网页版邮箱中[集成了 OpenPGP 加密功能](https://proton.me/support/how-to-use-pgp)。给其他Proton Mail账户的邮件是自动加密的，用OpenPGP密钥给非Proton Mail地址加密可以在账户设置中轻松启用。 Proton 还支持通过 WKD 进行自动外部密钥发现。这意味着发送给其他使用WKD的提供商的电子邮件也将自动使用OpenPGP加密，而无需与您的联系人手动交换公共PGP密钥。此外，它们还允许您[对发送到Proton Mail之外地址的消息进行加密](https://proton.me/support/password-protected-emails)，不需要使用OpenPGP，收件人也不需要注册Proton Mail账户。

Proton Mail还通过HTTP从其WKD发布Proton帐户的公钥。这个做法可以让不使用 Proton Mail 的用户也能轻松找到 Proton Mail 账户的 OpenPGP 密钥，从而实现跨服务商的端到端加密。这项功能只能用于以 Proton 自有域名结尾的邮件地址，比如`@proton.me`。如果您使用自定义域名，您必须单独[配置WKD](basics/email-security.md#what-is-the-web-key-directory-standard)。

#### :material-information-outline:{ .pg-blue } 账户停用

如果您拥有付费账户，而且14天后[账单仍然没有支付](https://proton.me/support/delinquency)，您将无法访问您的数据。 30天后，你的账户将成为欠费账户，不会收到来信。在此期间，您将继续收到账单。 Proton 将在一年后[删除处于非活跃状态的免费账户](https://proton.me/support/inactive-accounts)。而且已经停用账户的邮件地址是**不能**再次使用的。

#### :material-information-outline:{ .pg-blue } 附加功能

Proton Mail[的“无限”](https://proton.me/support/proton-plans#proton-unlimited)套餐除了提供多个自定义域名、无限量的马甲邮箱以及 500 GB 存储空间外，还可使用其他 Proton 服务。

### Mailbox Mail

<div class="admonition recommendation" markdown>

![Mailbox Mail 标志](assets/img/email/mailbox-mail.svg){ align=right }

**Mailbox Mail**（前身为 *Mailbox.org*）是一款以安全、无广告为重点，且100%采用环保能源的邮件服务。他们自2014年以来一直在运作。 Mailbox Mail 总部位于德国柏林。

账户创建后自带高达2GB存储，可以根据需要进行升级。

[:octicons-home-16: 主页](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="隐私政策" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="文档" }

<details class="downloads" markdown>
<summary>下载</summary>

- [:octicons-browser-16: 网页端](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } 自定义域名和别名

Mailbox Mail 允许您使用自己的域名，并且支持[“通配”](https://kb.mailbox.org/en/private/custom-domains/use-your-own-domain-with-catch-all/)邮箱地址。 Mailbox Mail 还支持[子邮箱功能](https://kb.mailbox.org/en/private/e-mail/what-is-an-alias-and-how-do-i-use-it/)，如果您不想购买域名，这会非常有用。

#### :material-check:{ .pg-green } 保护隐私的支付方式

由于其支付服务商BitPay暂停了在德国的业务，Mailbox Mail不再接受任何加密货币支付。不过，他们确实接受邮寄**现金**、银行账户**现金**支付、银行转账、信用卡、PayPal，以及两种德国特有的支付渠道：Paydirekt 和 Sofortüberweisung。

#### :material-check:{ .pg-green } 账户安全

Mailbox Mail 仅对其网页版邮箱支持[双因素认证](https://kb.mailbox.org/en/private/security-and-privacy/how-to-use-two-factor-authentication-2fa/)。您可以通过[YubiCloud](https://yubico.com/products/services-software/yubicloud) 使用 TOTP 或[YubiKey](security-keys.md#yubikey)。目前尚不支持[WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online)等 Web 标准。

#### :material-information-outline:{ .pg-blue } 数据安全

Mailbox Mail 支持通过其[加密邮箱](https://kb.mailbox.org/en/private/encryption/your-encrypted-mailbox/)对收到的邮件进行加密。您收到的新消息后将立即使用您的公钥进行加密。

然而，Mailbox Mail 所使用的软件平台[Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange) [不支持](https://kb.mailbox.org/en/business/security-privacy-article/encryption-of-calendar-and-address-book/)对您的通讯录和日历进行加密。[独立选项](calendar.md)可能更适合该数据。

#### :material-check:{ .pg-green } 邮件加密

Mailbox Mail 在其网页邮箱中[集成了加密功能](https://kb.mailbox.org/en/private/encryption/how-can-e-mails-be-encrypted-with-pgp/)，这使得向拥有公开 OpenPGP 密钥的用户发送邮件变得更加简单。该功能还允许[远程收件人解密](https://kb.mailbox.org/en/private/encryption/my-recipient-does-not-use-pgp/)在Mailbox Mail 服务器上的邮件。当远程收件人没有 OpenPGP 且无法对其邮箱中的邮件副本进行解密时，此功能非常有用。

Mailbox Mail也支持通过HTTP从其WKD发现公钥。这使得 Mailbox Mail 平台外的用户能够轻松找到 Mailbox Mail 账户的 OpenPGP 密钥，从而实现跨提供商的端到端加密E2EE。这项功能只能用于以Mailbox Mail自有域名结尾的邮件地址，比如`@mailbox.org`。如果您使用自定义域名，您必须单独[配置WKD](basics/email-security.md#what-is-the-web-key-directory-standard)。

#### :material-information-outline:{ .pg-blue } 账户停用

合约到期后，您的账户将被设为受限用户账户。 [30天](https://kb.mailbox.org/en/en/private/account/reactivate-a-deleted-account/)后，该内容将被永久删除。

#### :material-information-outline:{ .pg-blue } 附加功能

您可以通过其[.onion 服务](https://kb.mailbox.org/en/en/private/security-privacy/using-the-tor-exit-node-from-mailbox/)，使用 IMAP/SMTP 访问您的 Mailbox Mail 账户。不过，无法通过其 .onion 服务访问他们的网页邮件界面，而且您可能会遇到 TLS 证书错误。

所有账户都自带[可加密](https://kb.mailbox.org/en/private/drive/encrypt-files-on-your-drive/)的有限云空间。 Mailbox Mail 还提供了一个别名[@secure.mailbox.org，](https://kb.mailbox.org/en/business/e-mail-article/ensuring-e-mails-are-sent-securely/)该别名会强制在邮件服务器之间的连接中启用 TLS 加密，否则邮件将无法发送。除了 IMAP 和 POP3 等标准访问协议外，Mailbox Mail 还支持[Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync)。

Mailbox Mail 的所有套餐均提供“数字遗产”功能。您可以选择是否将您的任何数据传递给继承人，前提是他们提出申请并出示您的遗嘱。或者，您可以通过姓名和地址指定一个人。

## 更多服务提供商

这些提供商对您的邮件进行加密，只有您可以稍后阅读它们，使它们更能保证您存储的邮件的安全。然而，它们并不支持不同服务提供商之间端到端加密通信的互操作性加密标准。

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta 标志](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta 标志](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta**（原名 *Tutanota*）是一项通过加密技术专注于安全与隐私的邮件服务。 Tuta自2011年起开始运营，总部位于德国汉诺威。

免费账户自带 1 GB储存空间。

[:octicons-home-16: 主页](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="隐私政策" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="文档" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="源代码" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title="贡献" }

<details class="downloads" markdown>
<summary>下载</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:fontawesome-brands-windows: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta 不支持[IMAP 协议](https://tuta.com/support#imap)，也不支持使用[第三方邮件客户端](email-clients.md)，此外，您也无法在 Tuta 应用中添加[外部邮箱账户](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647)。目前也不支持[邮件导入](https://github.com/tutao/tutanota/issues/630)，不过这一情况[预计将有所改变](https://tuta.com/blog/kickoff-import)。邮件可以[逐封导出，或者按文件夹批量选择导出](https://tuta.com/support#generalMail)，但如果文件夹数量较多，这种操作可能会不方便。

#### :material-check:{ .pg-green } 自定义域名和别名

付费版 Tuta 账户可根据其套餐使用 15 个或 30 个别名，并在[自定义域名](https://tuta.com/support#custom-domain)上使用不限数量的别名。 Tuta 不支持[子地址（加号地址）](https://tuta.com/support#plus)，但您可以使用自定义域名的[“通配地址”](https://tuta.com/support#settings-global)。

#### :material-information-outline:{ .pg-blue } 保护隐私的支付方式

Tuta 仅直接接受信用卡和 PayPal 支付，但您可以使用 [**加密货币**](cryptocurrency.md) 通过其与ProxyStore[的合作关系](https://tuta.com/support/#cryptocurrency)购买礼品卡。

#### :material-check:{ .pg-green } 账户安全

Tuta 支持使用 TOTP 或 U2F[进行双因素认证](https://tuta.com/support#2fa)。

#### :material-check:{ .pg-green } 数据安全

Tuta 会将您的[电子邮件](https://tuta.com/support#what-encrypted)、[通讯录联系人](https://tuta.com/support#encrypted-address-book)以及[日历](https://tuta.com/support#calendar)通过强加密技术进行存储，只有您拥有解密密钥。这意味着，一旦消息和其他数据存储到您的账户中，除您本人外，任何人都无法读取这些内容。

#### :material-information-outline:{ .pg-blue } 邮件加密

Tuta[不使用 OpenPGP](https://tuta.com/support/#pgp)。 Tuta帐户只有在通过[临时Tuta邮箱](https://tuta.com/support/#encrypted-email-external)发送时，才能接收来自非Tuta电子邮件帐户的加密电子邮件。

#### :material-information-outline:{ .pg-blue } 账户停用

Tuta 将在六个月后[删除处于非活跃状态的免费账户](https://tuta.com/support#inactive-accounts)。只要付费，您就可以重新使用已被停用的免费账户。

#### :material-information-outline:{ .pg-blue } 附加功能

Tuta免费或以极大的折扣向[非营利组织提供Tuta](https://tuta.com/blog/secure-email-for-non-profit)商业版本。

## 标准

**请注意，我们与所推荐的任何服务提供商均无关联。**除[标准评选标准](about/criteria.md)外，我们还针对希望获得推荐的邮件服务提供商制定了一套明确的要求，包括实施行业最佳实践、采用现代技术等。我们建议您在选择电子邮件提供商之前熟悉此列表，并进行自己的研究以确保您选择的电子邮件提供商适合您。

### 技术

为了提供安全和最佳的服务，我们认为这些功能非常重要。您应该考虑提供商是否具备您所需的功能。

**符合条件的最低要求。**

- 必须使用非对称加密对静态的电子邮件帐户数据进行加密，且只有用户才拥有解密所需的私钥。
- 必须能够将电子邮件导出为[Mbox](https://en.wikipedia.org/wiki/Mbox)或符合[RFC5322](https://datatracker.ietf.org/doc/rfc5322)标准的独立.EML文件。
- 必须在自有基础设施上运行，即不建立在第三方电子邮件服务提供商之上。

**最佳情况：**

- 应该使用非对称加密对所有静态的帐户数据（联系人、日历等）进行加密，且只有用户拥有解密所需的私钥。
- 应该为方便起见提供集成的网页邮箱端到端加密/PGP加密。
- 应支持WKD，以改善通过HTTP发现公开OpenPGP密钥的过程。 GnuPG用户可以使用此命令获取密钥：`gpg --locate-key example_user@example.com`。
- 支持为外部用户提供临时邮箱。当您想发送加密电子邮件而不向收件人发送实际副本时，这非常有用。这些电子邮件通常寿命有限，随后会被自动删除。它们也不需要收件人配置任何诸如OpenPGP之类的密码学技术。
- 应支持[子寻址](https://en.wikipedia.org/wiki/Email_address#Sub-addressing)。
- 应允许用户使用自己的[域名](https://en.wikipedia.org/wiki/Domain_name)。自定义域名对用户来说很重要，因为如果服务变差或被另一家不优先考虑隐私的公司收购，它允许用户保留对其服务的控制权。
- 为那些使用自己域名的用户提供统配（Catch-all）或别名功能。
- 应使用标准电子邮件访问协议，如IMAP、SMTP或[JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol)。标准访问协议可确保客户能够轻松下载其所有电子邮件，以便他们切换到另一家提供商。
- 电子邮件提供商的服务应该可以通过[洋葱服务](https://en.wikipedia.org/wiki/.onion)访问。

### 隐私

我们希望我们推荐的提供商尽可能少地收集数据。

**符合条件的最低要求：**

- 必须保护发件人的IP地址，包括过滤该地址以防其在`Received`标头字段中显示。
- 除用户名和密码外，不得要求提供个人身份信息（PII）。
- 隐私政策必须符合GDPR规定的要求。

**最佳情况：**

- 应接受[匿名付款选项](advanced/payments.md)（[加密货币](cryptocurrency.md)、现金、礼品卡等）
- 应托管在具有强效电子邮件隐私保护法律的司法管辖区。

### 安全性

电子邮件服务器处理大量非常敏感的数据。我们期望提供商采用行业最佳实践来保护他们的客户。

**符合条件的最低要求：**

- 使用双因素身份验证（如[TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp)）保护网页邮箱。
- 静态加密，使用非对称加密，其中服务提供商没有其所持数据的解密密钥。这可以防止流氓员工泄漏他们有权访问的数据，或远程对手释出其通过未经授权访问服务器窃取的数据。
- 支持[DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions)。
- 在使用[Hardenize](https://hardenize.com)、[testssl.sh](https://testssl.sh)或[Qualys SSL Labs](https://ssllabs.com/ssltest)等工具进行评估时，没有TLS错误或漏洞；这包括与证书相关的错误和弱DH参数（例如导致[Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security))的参数）。
- 支持前向保密和经过身份验证的加密的强密码套件的服务器套件偏好（在TLS 1.3上为可选）。
- 有效的[MTA-STS](https://tools.ietf.org/html/rfc8461)和[TLS-RPT](https://tools.ietf.org/html/rfc8460)策略。
- 有效的[DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities)记录。
- 有效的[SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework)和[DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail)记录。
- 必须有适当的[DMARC](https://en.wikipedia.org/wiki/DMARC)记录和策略，或者使用[ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain)进行身份验证。如果使用DMARC身份验证，则策略必须设置为`reject`（拒绝）或`quarantine`（隔离）。
- 偏好TLS 1.2或更高版本的服务器套件，并具有支持[RFC8996](https://datatracker.ietf.org/doc/rfc8996)的计划。
- 如果使用SMTP，则应进行[SMTPS](https://en.wikipedia.org/wiki/SMTPS)提交。
- 网站安全标准，例如：
    - [HTTP严格传输安全协议（HSTS）](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - 如果从外部域加载内容，则使用[子资源完整性（SRI）](https://en.wikipedia.org/wiki/Subresource_Integrity)。
- 必须支持查看[邮件标头](https://en.wikipedia.org/wiki/Email#Message_header)，因为这是确定电子邮件是否为网络钓鱼尝试的关键取证功能。

**最佳情况：**

- 应支持硬件身份验证，即 U2F和[WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online)。
- 除了DANE支持外，还有[DNS证书颁发机构授权（CAA）资源记录](https://tools.ietf.org/html/rfc6844)。
- 应实施[经过身份验证的接收链（ARC）](https://en.wikipedia.org/wiki/Authenticated_Received_Chain)，这对于向邮件列表发帖的人（[RFC8617](https://tools.ietf.org/html/rfc8617)）非常有用。
- 由知名的第三方公司发布的公开安全审计。
- 漏洞悬赏计划和/或协调一致的漏洞披露流程。
- 网站安全标准，例如：
    - [内容安全策略（CSP）](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### 信任

您不会将财务委托给使用虚假身份的人，那为什么要将电子邮件托付给他们呢？我们要求我们推荐的提供商公开其所有权或领导层。我们还希望看到频繁的透明度报告，特别是关于如何处理政府请求的报告。

**符合条件的最低要求：**

- 面向公众的领导层或所有权。

**最佳情况：**

- 频繁的透明度报告。

### 营销

对于我们推荐的电子邮件提供商，我们希望看到负责任的营销。

**符合条件的最低要求：**

- 必须自托管分析服务（不使用Google Analytics、Adobe Analytics等）。
- 不得进行任何不负责任的营销，这可能包括以下内容：
    - 声称拥有“牢不可破的加密”。使用加密时应考虑到，未来当出现破解它的技术时，它可能不再是秘密。
    - 保证100%保护匿名性。当有人声称某事是100%时，这意味着绝不承认存在失败的可能性。我们知道人们很容易通过多种方式解除自己的匿名化，例如：
        - 重复使用他们未使用Tor等匿名软件就访问过的个人信息（如电子邮件帐户、唯一的化名等）
        - [浏览器指纹识别](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**最佳情况：**

- 有关设置双因素身份验证、电子邮件客户端、OpenPGP等任务的清晰易读的文档。

### 附加功能

虽然不是严格的要求，但我们在确定推荐哪些提供商时还会考虑其他一些便利性或隐私因素。
