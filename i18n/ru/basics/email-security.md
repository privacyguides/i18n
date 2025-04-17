---
meta_title: "Почему электронная почта не является лучшим выбором для конфиденциальности и безопасности - Privacy Guides"
title: Безопасность электронной почты
icon: material/email
description: Email is insecure in many ways, and these are some of the reasons it isn't our top choice for secure communications.
---

Электронная почта по умолчанию является небезопасной формой коммуникации. You can improve your email security with tools such as OpenPGP, which add end-to-end encryption to your messages, but OpenPGP still has a number of drawbacks compared to encryption in other messaging applications.

Таким образом, электронную почту лучше всего использовать для получения транзакционных писем (например, уведомлений, писем для проверки, сброса пароля и т.д.) от сайтов, в которых у вас есть аккаунт, а не для общения с другими людьми.

## Обзор шифрования электронной почты

Стандартным способом добавления E2EE в электронные письма между различными поставщиками услуг электронной почты является использование OpenPGP. There are different implementations of the OpenPGP standard, the most common being [GnuPG](../encryption.md#gnu-privacy-guard) and [OpenPGP.js](https://openpgpjs.org).

Even if you use OpenPGP, it does not support [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), which means if the private key of either you or the message recipient is ever stolen, all previous messages encrypted with it will be exposed. Именно поэтому мы рекомендуем использовать для общения между людьми [мессенджеры](../real-time-communication.md), которые обеспечивают прямую секретность, а не электронную почту.

There is another standard which is popular with business called [S/MIME](https://en.wikipedia.org/wiki/S/MIME), however it requires a certificate issued from a [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (not all of them issue S/MIME certificates, and often a yearly payment is required). In some cases it is more usable than PGP because it has support in popular/mainstream email applications like Apple Mail, [Google Workplace](https://support.google.com/a/topic/9061730), and [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). However, S/MIME does not solve the issue of lack of forward secrecy, and isn't particularly more secure than PGP.

## Что такое стандарт Web Key Directory?

The [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. Почтовые клиенты, поддерживающие WKD, запрашивают ключ у сервера получателя, основываясь на доменном имени его адреса. Например, когда вы пишете на `jonah@privacyguides.org`, ваш почтовый клиент запрашивает у `privacyguides.org` OpenPGP-ключ Джона, и если `privacyguides.org` имеет соответствующий ключ, ваше сообщение будет автоматически зашифровано.

В дополнение к [рекомендованным почтовым клиентам](../email-clients.md), поддерживающим WKD, некоторые браузерные почтовые интерфейсы также поддерживают WKD. Будет ли *ваш личный* ключ опубликован в WKD для других пользователей, зависит от конфигурации вашего домена. Если вы пользуетесь [почтовым провайдером](../email.md#openpgp-compatible-services), поддерживающим WKD, таким как Proton Mail или Mailbox.org, они опубликуют ваш OpenPGP-ключ на своем домене.

Если же вы используете свой собственный домен, вам потребуется настроить WKD отдельно. Если вы контролируете доменное имя, вы можете настроить WKD независимо от почтового провайдера. One easy way to do this is to use the "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" feature from the `keys.openpgp.org` server: Set a CNAME record on the `openpgpkey` subdomain of your domain pointed to `wkd.keys.openpgp.org`, then upload your key to [keys.openpgp.org](https://keys.openpgp.org). Кроме того, можно [запустить WKD на собственном сервере](https://wiki.gnupg.org/WKDHosting).

If you use a shared domain from a provider which doesn't support WKD, like `@gmail.com`, you won't be able to share your OpenPGP key with others via this method.

### Какие почтовые клиенты поддерживают E2EE?

Провайдеры электронной почты, позволяющие использовать стандартные протоколы доступа, такие как IMAP и SMTP, можно использовать с любым [ почтовым клиентом, которые мы рекомендуем](../email-clients.md). Depending on the authentication method, this may lead to decreased security if either the provider or the email client does not support [OAuth](account-creation.md#sign-in-with-oauth) or a bridge application as [multifactor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### Как я могу защитить свои приватные ключи?

A smart card (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smart card and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smart card to avoid possibly exposing your private key to a compromised device.

## Обзор метаданных электронной почты

Email metadata is stored in the [message header](https://en.wikipedia.org/wiki/Email#Message_header) of the email message and includes some visible headers that you may have seen such as `To`, `From`, `Cc`, `Date`, and `Subject`. Существует также ряд скрытых заголовков, включаемых многими почтовыми клиентами и провайдерами, которые могут раскрыть информацию о вашем аккаунте.

Клиентское программное обеспечение может использовать метаданные электронной почты, чтобы показать, от кого пришло сообщение и в какое время оно было получено. Серверы могут использовать его для определения места отправки сообщения электронной почты, а также для [других целей](https://ru.wikipedia.org/wiki/%D0%AD%D0%BB%D0%B5%D0%BA%D1%82%D1%80%D0%BE%D0%BD%D0%BD%D0%B0%D1%8F_%D0%BF%D0%BE%D1%87%D1%82%D0%B0#%D0%97%D0%B0%D0%B3%D0%BE%D0%BB%D0%BE%D0%B2%D0%BA%D0%B8_%D0%BF%D0%B8%D1%81%D1%8C%D0%BC%D0%B0), которые не всегда прозрачны.

### Кто может просматривать метаданные электронной почты?

Email metadata is protected from outside observers with [opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS), but it is still able to be seen by your email client software (or webmail) and any servers relaying the message from you to any recipients including your email provider. Иногда почтовые серверы для защиты от спама используют сторонние службы, которые, как правило, также имеют доступ к вашим сообщениям.

### Почему метаданные не могут быть E2EE?

Метаданные электронной почты имеют решающее значение для самой базовой функциональности электронной почты (откуда она пришла и куда должна отправиться). E2EE was not built into standard email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
