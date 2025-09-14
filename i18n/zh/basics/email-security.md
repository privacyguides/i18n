---
meta_title: "为什么电子邮件不是隐私和安全的最佳选择 - 隐私指南"
title: 电子邮件安全
icon: material/email
description: Email is insecure in many ways, and these are some of the reasons it isn't our top choice for secure communications.
---

电子邮件在默认情况下是一种不安全的通信形式。 You can improve your email security with tools such as OpenPGP, which add end-to-end encryption to your messages, but OpenPGP still has a number of drawbacks compared to encryption in other messaging applications.

因此，电子邮件最好用于接收来自你在线注册的服务的交易性邮件（如通知、验证邮件、密码重置等），而不是用于与他人交流。

## 电子邮件加密概述

在不同的电邮供应商之间为电子邮件添加端到端加密的标准方法是使用OpenPGP。 There are different implementations of the OpenPGP standard, the most common being [GnuPG](../encryption.md#gnu-privacy-guard) and [OpenPGP.js](https://openpgpjs.org).

Even if you use OpenPGP, it does not support [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), which means if the private key of either you or the message recipient is ever stolen, all previous messages encrypted with it will be exposed. 这就是为什么我们推荐 [即时通讯工具](../real-time-communication.md) ，比起电子邮件，它尽可能更好地在人与人之间的通信中实现前向保密性。

There is another standard which is popular with business called [S/MIME](https://en.wikipedia.org/wiki/S/MIME), however it requires a certificate issued from a [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (not all of them issue S/MIME certificates, and often a yearly payment is required). In some cases it is more usable than PGP because it has support in popular/mainstream email applications like Apple Mail, [Google Workplace](https://support.google.com/a/topic/9061730), and [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). However, S/MIME does not solve the issue of lack of forward secrecy, and isn't particularly more secure than PGP.

## 什么是网络密钥目录标准？

The [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. 支持 WKD 的电子邮件客户端会要求收件人的服务器根据电子邮件地址的域名提供密钥。 例如，如果您向 `jonah@privacyguides.org`发送电子邮件，您的电子邮件客户端会向 `privacyguides.org` 询问 Jonah 的 OpenPGP 密钥，如果 `privacyguides.org` 拥有该账户的密钥，您的邮件就会自动加密。

除了我们推荐的 [电子邮件客户端（](../email-clients.md) ）支持 WKD 外，一些网络邮件提供商也支持 WKD。 *您自己的* 密钥是否发布到 WKD 供他人使用，取决于您的域配置。 If you use an [email provider](../email.md#openpgp-compatible-services) which supports WKD, such as Proton Mail or Mailbox Mail, they can publish your OpenPGP key on their domain for you.

如果使用自己的自定义域，则需要单独配置 WKD。 如果您能控制自己的域名，那么无论您的电子邮件提供商是谁，您都可以设置 WKD。 One easy way to do this is to use the "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" feature from the `keys.openpgp.org` server: Set a CNAME record on the `openpgpkey` subdomain of your domain pointed to `wkd.keys.openpgp.org`, then upload your key to [keys.openpgp.org](https://keys.openpgp.org). 或者，您也可以 [自行将 WKD 托管在自己的网络服务器上](https://wiki.gnupg.org/WKDHosting)。

If you use a shared domain from a provider which doesn't support WKD, like `@gmail.com`, you won't be able to share your OpenPGP key with others via this method.

### 哪些电子邮件客户端支持端到端加密？

允许你使用IMAP和SMTP等标准访问协议的电子邮件提供商可以与我们推荐的任何 [电子邮件客户端一起使用](../email-clients.md)。 Depending on the authentication method, this may lead to decreased security if either the provider or the email client does not support [OAuth](account-creation.md#sign-in-with-oauth) or a bridge application as [multifactor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### 我如何保护我的私钥？

A smart card (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smart card and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smart card to avoid possibly exposing your private key to a compromised device.

## 电子邮件元数据概述

Email metadata is stored in the [message header](https://en.wikipedia.org/wiki/Email#Message_header) of the email message and includes some visible headers that you may have seen such as `To`, `From`, `Cc`, `Date`, and `Subject`. 许多电子邮件客户和供应商还包括一些隐藏的标题，可以揭示有关你的账户的信息。

客户端软件可以使用电子邮件元数据来显示信息来自谁，以及什么时间收到的。 服务器可能使用它来确定电子邮件必须发送到哪里，其中还有一些不那么透明的 [其他目的](https://en.wikipedia.org/wiki/Email#Message_header) 。

### 谁可以查看电子邮件元数据？

Email metadata is protected from outside observers with [opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS), but it is still able to be seen by your email client software (or webmail) and any servers relaying the message from you to any recipients including your email provider. 有时，电子邮件服务器也会使用第三方服务来防止垃圾邮件，这些服务一般也能接触到你的邮件。

### 为什么元数据不能被端到端加密？

电子邮件元数据对于电子邮件最基本的功能（它从哪里来，又要到哪里去）至关重要。 E2EE was not built into standard email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
