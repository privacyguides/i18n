---
meta_title: "Чому електронна пошта - не найкращий вибір для забезпечення конфіденційності та безпеки - Privacy Guides"
title: Безпека електронної пошти
icon: material/email
description: Email is insecure in many ways, and these are some of the reasons it isn't our top choice for secure communications.
---

Електронна пошта за замовчуванням є незахищеною формою комунікації. You can improve your email security with tools such as OpenPGP, which add end-to-end encryption to your messages, but OpenPGP still has a number of drawbacks compared to encryption in other messaging applications.

Як наслідок, електронну пошту найкраще використовувати для отримання транзакційних повідомлень (наприклад, сповіщень, підтверджень, скидання паролів тощо) від сервісів, на які ви зареєструвалися в Інтернеті, а не для спілкування з іншими людьми.

## Огляд шифрування електронної пошти

Стандартним способом додавання E2EE до листів між різними поштовими провайдерами є використання OpenPGP. There are different implementations of the OpenPGP standard, the most common being [GnuPG](../encryption.md#gnu-privacy-guard) and [OpenPGP.js](https://openpgpjs.org).

Even if you use OpenPGP, it does not support [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), which means if the private key of either you or the message recipient is ever stolen, all previous messages encrypted with it will be exposed. Ось чому ми рекомендуємо [месенджери](../real-time-communication.md), які реалізують пряму секретність через електронну пошту для особистого спілкування, коли це можливо.

There is another standard which is popular with business called [S/MIME](https://en.wikipedia.org/wiki/S/MIME), however it requires a certificate issued from a [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (not all of them issue S/MIME certificates, and often a yearly payment is required). In some cases it is more usable than PGP because it has support in popular/mainstream email applications like Apple Mail, [Google Workplace](https://support.google.com/a/topic/9061730), and [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). However, S/MIME does not solve the issue of lack of forward secrecy, and isn't particularly more secure than PGP.

## Що таке стандарт Web Key Directory?

The [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. Поштові клієнти, які підтримують WKD, запитують у сервера одержувача ключ на основі доменного імені адреси електронної пошти. Наприклад, якщо ви надішлете електронною поштою `jonah@privacyguides.org`, ваш поштовий клієнт запитає `privacyguides.org` про ключ OpenPGP Джона, і якщо `privacyguides.org` має ключ для цього облікового запису, ваше повідомлення буде автоматично зашифровано.

На додачу до [рекомендованих поштових клієнтів](../email-clients.md), які підтримують WKD, деякі провайдери вебпошти також підтримують WKD. Чи буде *ваш власний ключ* опублікований у WKD для використання іншими, залежить від конфігурації вашого домену. If you use an [email provider](../email.md#openpgp-compatible-services) which supports WKD, such as Proton Mail or Mailbox Mail, they can publish your OpenPGP key on their domain for you.

Якщо ви використовуєте власний домен, вам потрібно буде налаштувати WKD окремо. Якщо ви контролюєте своє доменне ім'я, ви можете налаштувати WKD незалежно від провайдера електронної пошти. One easy way to do this is to use the "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" feature from the `keys.openpgp.org` server: Set a CNAME record on the `openpgpkey` subdomain of your domain pointed to `wkd.keys.openpgp.org`, then upload your key to [keys.openpgp.org](https://keys.openpgp.org). Крім того, ви можете [самостійно розмістити WKD на власному веб-сервері](https://wiki.gnupg.org/WKDHosting).

If you use a shared domain from a provider which doesn't support WKD, like `@gmail.com`, you won't be able to share your OpenPGP key with others via this method.

### Які поштові клієнти підтримують E2EE?

Провайдери електронної пошти, які дозволяють використовувати стандартні протоколи, такі як IMAP та SMTP, можна використовувати з будь-яким з [рекомендованими поштовими клієнтами](../email-clients.md). Depending on the authentication method, this may lead to decreased security if either the provider or the email client does not support [OAuth](account-creation.md#sign-in-with-oauth) or a bridge application as [multifactor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### Як захистити свої приватні ключі?

A smart card (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smart card and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smart card to avoid possibly exposing your private key to a compromised device.

## Огляд метаданих електронної пошти

Email metadata is stored in the [message header](https://en.wikipedia.org/wiki/Email#Message_header) of the email message and includes some visible headers that you may have seen such as `To`, `From`, `Cc`, `Date`, and `Subject`. Існує також низка прихованих заголовків, які включаються багатьма поштовими клієнтами та провайдерами і можуть розкрити інформацію про ваш обліковий запис.

Клієнтське програмне забезпечення може використовувати метадані електронної пошти, щоб показати, від кого надійшло повідомлення і в який час воно було отримано. Сервери можуть використовувати їх, щоб визначити, куди потрібно відправити електронне повідомлення, серед [інших цілей](https://uk.wikipedia.org/wiki/%D0%95%D0%BB%D0%B5%D0%BA%D1%82%D1%80%D0%BE%D0%BD%D0%BD%D0%B0_%D0%BF%D0%BE%D1%88%D1%82%D0%B0#%D0%97%D0%B0%D0%B3%D0%BE%D0%BB%D0%BE%D0%B2%D0%BA%D0%B8_%D0%BB%D0%B8%D1%81%D1%82%D0%B0), які не завжди є прозорими.

### Хто може переглядати метадані електронної пошти?

Email metadata is protected from outside observers with [opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS), but it is still able to be seen by your email client software (or webmail) and any servers relaying the message from you to any recipients including your email provider. Іноді поштові сервери також використовують сторонні сервіси для захисту від спаму, які, як правило, також мають доступ до ваших повідомлень.

### Чому метадані не можуть бути E2EE?

Метадані електронної пошти мають вирішальне значення для базової функціональності електронної пошти (звідки вона прийшла і куди має надійти). E2EE was not built into standard email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
