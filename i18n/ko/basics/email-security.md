---
meta_title: "이메일이 프라이버시, 보안 면에서 최선의 선택이 아닌 이유 - Privacy Guides"
title: 이메일 보안
icon: material/email
description: Email is insecure in many ways, and these are some of the reasons it isn't our top choice for secure communications.
---

기본적으로, 이메일은 안전하지 않은 통신 형식입니다. You can improve your email security with tools such as OpenPGP, which add end-to-end encryption to your messages, but OpenPGP still has a number of drawbacks compared to encryption in other messaging applications.

따라서, 이메일은 다른 사람과 통신하는 용도로는 사용하지 않고, 가입한 온라인 서비스에서 보내는 사무 관련 이메일(알림, 인증 메일, 비밀번호 초기화 등) 수신 용도로 사용하는 것이 가장 좋습니다.

## 이메일 암호화 개요

서로 다른 이메일 제공 업체 간의 이메일에 E2EE를 적용하는 표준 방법은 OpenPGP를 사용하는 것입니다. There are different implementations of the OpenPGP standard, the most common being [GnuPG](../encryption.md#gnu-privacy-guard) and [OpenPGP.js](https://openpgpjs.org).

Even if you use OpenPGP, it does not support [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), which means if the private key of either you or the message recipient is ever stolen, all previous messages encrypted with it will be exposed. 따라서, 개인 간 의사소통에는 이메일보다는 순방향 비밀성이 구현된 [메신저](../real-time-communication.md)를 이용하실 것을 권장드립니다.

There is another standard which is popular with business called [S/MIME](https://en.wikipedia.org/wiki/S/MIME), however it requires a certificate issued from a [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (not all of them issue S/MIME certificates, and often a yearly payment is required). In some cases it is more usable than PGP because it has support in popular/mainstream email applications like Apple Mail, [Google Workplace](https://support.google.com/a/topic/9061730), and [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). However, S/MIME does not solve the issue of lack of forward secrecy, and isn't particularly more secure than PGP.

## What is the Web Key Directory standard?

The [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. Email clients which support WKD will ask the recipient's server for a key based on the email address' domain name. For example, if you emailed `jonah@privacyguides.org`, your email client would ask `privacyguides.org` for Jonah's OpenPGP key, and if `privacyguides.org` has a key for that account, your message would be automatically encrypted.

In addition to the [email clients we recommend](../email-clients.md) which support WKD, some webmail providers also support WKD. Whether *your own* key is published to WKD for others to use depends on your domain configuration. If you use an [email provider](../email.md#openpgp-compatible-services) which supports WKD, such as Proton Mail or Mailbox.org, they can publish your OpenPGP key on their domain for you.

If you use your own custom domain, you will need to configure WKD separately. If you control your domain name, you can set up WKD regardless of your email provider. One easy way to do this is to use the "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" feature from the `keys.openpgp.org` server: Set a CNAME record on the `openpgpkey` subdomain of your domain pointed to `wkd.keys.openpgp.org`, then upload your key to [keys.openpgp.org](https://keys.openpgp.org). Alternatively, you can [self-host WKD on your own web server](https://wiki.gnupg.org/WKDHosting).

If you use a shared domain from a provider which doesn't support WKD, like `@gmail.com`, you won't be able to share your OpenPGP key with others via this method.

### E2EE 지원 이메일 클라이언트는 무엇인가요?

IMAP, SMTP 등 표준 접속 프로토콜을 사용할 수 있는 이메일 제공 업체는 [권장 이메일 클라이언트](../email-clients.md)와 함께 사용할 수 있습니다. Depending on the authentication method, this may lead to decreased security if either the provider or the email client does not support [OAuth](account-creation.md#sign-in-with-oauth) or a bridge application as [multifactor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### 개인 키를 어떻게 보호해야 하나요?

A smart card (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smart card and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smart card to avoid possibly exposing your private key to a compromised device.

## 이메일 메타데이터 개요

Email metadata is stored in the [message header](https://en.wikipedia.org/wiki/Email#Message_header) of the email message and includes some visible headers that you may have seen such as `To`, `From`, `Cc`, `Date`, and `Subject`. 이외에도 여러 숨겨진 헤더가 이메일 클라이언트 및 제공 업체로부터 추가되며, 이러한 정보는 여러분의 계정에 대한 정보를 노출시킬 수 있습니다.

클라이언트 소프트웨어는 이메일 메타데이터를 사용해 메시지의 발신자와 수신 시간을 표시할 수 있습니다. 서버는 항상 투명하지만은 않은 [다른 목적지](https://en.wikipedia.org/wiki/Email#Message_header) 중 어디에 이메일을 보내야 할지 결정하는 데에 메타데이터를 활용할 수 있습니다.

### 이메일 메타데이터는 누가 볼 수 있나요?

Email metadata is protected from outside observers with [opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS), but it is still able to be seen by your email client software (or webmail) and any servers relaying the message from you to any recipients including your email provider. 이메일 서버 중에는 스팸 차단 목적으로 타사 서비스를 사용하기도 하는데, 보통 이런 타사 서비스도 여러분의 메시지에 접근할 수 있습니다.

### 메타데이터는 종단 간 암호화를 적용할 수 없나요?

이메일 메타데이터는 이메일의 가장 기본적인 기능(어디에서 왔는지, 어디로 가야하는지 등)에 매우 중요한 역할을 합니다. E2EE was not built into standard email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
