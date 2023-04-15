---
meta_title: "Why Email Isn't the Best Choice for Privacy and Security - Privacy Guides"
title: 이메일 보안
icon: material/email
description: 이메일은 태생적으로 여러 가지 면에서 안전하지 않습니다. 따라서 안전한 통신을 위한 최선의 선택은 아닙니다.
---

기본적으로, 이메일은 안전하지 않은 통신 형식입니다. OpenPGP(메시지에 종단 간 암호화 적용) 등을 이용해 이메일 보안을 개선할 수는 있지만, OpenPGP 또한 다른 메신저 애플리케이션의 암호화에 비교하면 여러 문제점이 있으며, 이메일 시스템 설계상 암호화가 불가능한 일부 이메일 데이터도 존재합니다.

따라서, 이메일은 다른 사람과 통신하는 용도로는 사용하지 않고, 가입한 온라인 서비스에서 보내는 사무 관련 이메일(알림, 인증 메일, 비밀번호 초기화 등) 수신 용도로 사용하는 것이 가장 좋습니다.

## 이메일 암호화 개요

서로 다른 이메일 제공 업체 간의 이메일에 E2EE를 적용하는 표준 방법은 OpenPGP를 사용하는 것입니다. OpenPGP 표준에는 여러 구현체가 존재하며, [GnuPG](https://en.wikipedia.org/wiki/GNU_Privacy_Guard)와 [OpenPGP.js](https://openpgpjs.org)가 보편적입니다.

비즈니스에서 널리 사용되는 [S/MIME](https://en.wikipedia.org/wiki/S/MIME) 표준도 있으나, S/MIME는 [인증 기관](https://en.wikipedia.org/wiki/Certificate_authority)(모든 인증 기관이 S/MIME 인증서를 발급하지는 않습니다)에서 발급한 인증서가 필요합니다. S/MIME는 [Google Workplace](https://support.google.com/a/topic/9061730?hl=en&ref_topic=9061731), [웹용 Outlook 또는 Exchange Server 2016, 2019](https://support.office.com/en-us/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480)에서 지원됩니다.

OpenPGP를 사용하더라도 [순방향 비밀성(Forward secrecy)](https://en.wikipedia.org/wiki/Forward_secrecy)을 지원하지 않으므로, 본인 혹은 수신자의 개인 키가 도난당할 경우 해당 키로 암호화된 이전 메시지가 전부 노출됩니다. 따라서, 개인 간 의사소통에는 이메일보다는 순방향 비밀성이 구현된 [인스턴트 메신저](../real-time-communication.md) 이용을 권장합니다.

### What Email Clients Support E2EE?

Email providers which allow you to use standard access protocols like IMAP and SMTP can be used with any of the [email clients we recommend](../email-clients.md). Depending on the authentication method, this may lead to the decrease security if either the provider or the email client does not support OATH or a bridge application as [multi-factor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### How Do I Protect My Private Keys?

A smartcard (such as a [YubiKey](https://support.yubico.com/hc/en-us/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](https://www.nitrokey.com)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smartcard and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smartcard so as to avoid possibly exposing your private key to a compromised device.

## 이메일 메타데이터 개요

이메일 메타데이터는 이메일 메시지의 [메시지 헤더](https://en.wikipedia.org/wiki/Email#Message_header)에 저장됩니다. 이메일 메타데이터에는 여러분이 봐왔을 `To`(받는사람), `From`(보낸사람), `Cc`(참조), `Date`(보낸 날짜), `Subject`(제목) 등이 포함됩니다. 이외에도 여러 숨겨진 헤더가 이메일 클라이언트 및 제공 업체로부터 추가되며, 이러한 정보는 여러분의 계정에 대한 정보를 노출시킬 수 있습니다.

Client software may use email metadata to show who a message is from and what time it was received. Servers may use it to determine where an email message must be sent, among [other purposes](https://en.wikipedia.org/wiki/Email#Message_header) which are not always transparent.

### Who Can View Email Metadata?

Email metadata is protected from outside observers with [Opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS) protecting it from outside observers, but it is still able to be seen by your email client software (or webmail) and any servers relaying the message from you to any recipients including your email provider. Sometimes email servers will also use third-party services to protect against spam, which generally also have access to your messages.

### Why Can't Metadata be E2EE?

Email metadata is crucial to the most basic functionality of email (where it came from, and where it has to go). E2EE was not built into the email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt email metadata, only the message body itself. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as who you're emailing, the subject lines, when you're emailing, etc.
