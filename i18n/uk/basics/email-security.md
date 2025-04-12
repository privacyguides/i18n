---
meta_title: "Чому електронна пошта - не найкращий вибір для забезпечення конфіденційності та безпеки - Privacy Guides"
title: Безпека електронної пошти
icon: material/email
description: Email is insecure in many ways, and these are some of the reasons it isn't our top choice for secure communications.
---

Електронна пошта за замовчуванням є незахищеною формою комунікації. You can improve your email security with tools such as OpenPGP, which add End-to-End Encryption to your messages, but OpenPGP still has a number of drawbacks compared to encryption in other messaging applications.

Як наслідок, електронну пошту найкраще використовувати для отримання транзакційних повідомлень (наприклад, сповіщень, підтверджень, скидання паролів тощо) від сервісів, на які ви зареєструвалися в Інтернеті, а не для спілкування з іншими людьми.

## Огляд шифрування електронної пошти

Стандартним способом додавання E2EE до листів між різними поштовими провайдерами є використання OpenPGP. Існують різні реалізації стандарту OpenPGP, найпоширенішими з яких є [GnuPG](https://uk.wikipedia.org/wiki/GNU_Privacy_Guard) та [OpenPGP.js](https://openpgpjs.org).

Навіть якщо ви використовуєте OpenPGP, він не підтримує [Пряму секретність](https://uk.wikipedia.org/wiki/%D0%9F%D1%80%D1%8F%D0%BC%D0%B0_%D1%81%D0%B5%D0%BA%D1%80%D0%B5%D1%82%D0%BD%D1%96%D1%81%D1%82%D1%8C), що означає, якщо закритий ключ ваш або одержувача буде викрадено, всі попередні повідомлення, зашифровані за допомогою цього ключа, будуть відкриті. Ось чому ми рекомендуємо [месенджери](../real-time-communication.md), які реалізують пряму секретність через електронну пошту для особистого спілкування, коли це можливо.

There is another standard which is popular with business called [S/MIME](https://en.wikipedia.org/wiki/S/MIME), however, it requires a certificate issued from a [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (not all of them issue S/MIME certificates, and often a yearly payment is required). In some cases it is more usable than PGP because it has support in popular/mainstream email applications like Apple Mail, [Google Workplace](https://support.google.com/a/topic/9061730), and [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). However, S/MIME does not solve the issue of lack of forward secrecy, and isn't particularly more secure than PGP.

## Що таке стандарт Web Key Directory?

The [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. Поштові клієнти, які підтримують WKD, запитують у сервера одержувача ключ на основі доменного імені адреси електронної пошти. Наприклад, якщо ви надішлете електронною поштою `jonah@privacyguides.org`, ваш поштовий клієнт запитає `privacyguides.org` про ключ OpenPGP Джона, і якщо `privacyguides.org` має ключ для цього облікового запису, ваше повідомлення буде автоматично зашифровано.

На додачу до [рекомендованих поштових клієнтів](../email-clients.md), які підтримують WKD, деякі провайдери вебпошти також підтримують WKD. Чи буде *ваш власний ключ* опублікований у WKD для використання іншими, залежить від конфігурації вашого домену. Якщо ви використовуєте [провайдера електронної пошти](../email.md#openpgp-compatible-services), який підтримує WKD, наприклад, Proton Mail або Mailbox.org, вони можуть опублікувати для вас ваш ключ OpenPGP на своєму домені.

Якщо ви використовуєте власний домен, вам потрібно буде налаштувати WKD окремо. Якщо ви контролюєте своє доменне ім'я, ви можете налаштувати WKD незалежно від провайдера електронної пошти. One easy way to do this is to use the "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" feature from keys.openpgp.org, by setting a CNAME record on the `openpgpkey` subdomain of your domain pointed to `wkd.keys.openpgp.org`, then uploading your key to [keys.openpgp.org](https://keys.openpgp.org). Крім того, ви можете [самостійно розмістити WKD на власному веб-сервері](https://wiki.gnupg.org/WKDHosting).

Якщо ви використовуєте домен від провайдера, який не підтримує WKD, наприклад @gmail.com, ви не зможете поділитися своїм ключем OpenPGP з іншими за допомогою цього методу.

### Які поштові клієнти підтримують E2EE?

Провайдери електронної пошти, які дозволяють використовувати стандартні протоколи, такі як IMAP та SMTP, можна використовувати з будь-яким з [рекомендованими поштовими клієнтами](../email-clients.md). Depending on the authentication method, this may lead to the decrease security if either the provider or the email client does not support OATH or a bridge application as [multifactor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### Як захистити свої приватні ключі?

A smart card (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smart card and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smart card to avoid possibly exposing your private key to a compromised device.

## Огляд метаданих електронної пошти

Метадані електронного листа зберігаються в [заголовку](https://uk.wikipedia.org/wiki/%D0%95%D0%BB%D0%B5%D0%BA%D1%82%D1%80%D0%BE%D0%BD%D0%BD%D0%B0_%D0%BF%D0%BE%D1%88%D1%82%D0%B0#%D0%97%D0%B0%D0%B3%D0%BE%D0%BB%D0%BE%D0%B2%D0%BA%D0%B8_%D0%BB%D0%B8%D1%81%D1%82%D0%B0) повідомлення електронної пошти і включають деякі видимі поля, такі як `Кому`, `Від`, `Копія`, `Дата`, `Тема`. Існує також низка прихованих заголовків, які включаються багатьма поштовими клієнтами та провайдерами і можуть розкрити інформацію про ваш обліковий запис.

Клієнтське програмне забезпечення може використовувати метадані електронної пошти, щоб показати, від кого надійшло повідомлення і в який час воно було отримано. Сервери можуть використовувати їх, щоб визначити, куди потрібно відправити електронне повідомлення, серед [інших цілей](https://uk.wikipedia.org/wiki/%D0%95%D0%BB%D0%B5%D0%BA%D1%82%D1%80%D0%BE%D0%BD%D0%BD%D0%B0_%D0%BF%D0%BE%D1%88%D1%82%D0%B0#%D0%97%D0%B0%D0%B3%D0%BE%D0%BB%D0%BE%D0%B2%D0%BA%D0%B8_%D0%BB%D0%B8%D1%81%D1%82%D0%B0), які не завжди є прозорими.

### Хто може переглядати метадані електронної пошти?

Метадані електронної пошти захищені від сторонніх спостерігачів за допомогою [Opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS), але їх все одно може бачити програмне забезпечення вашого поштового клієнта (або веб-пошти) і будь-які сервери, що передають повідомлення від вас будь-яким одержувачам, включаючи вашого провайдера електронної пошти. Іноді поштові сервери також використовують сторонні сервіси для захисту від спаму, які, як правило, також мають доступ до ваших повідомлень.

### Чому метадані не можуть бути E2EE?

Метадані електронної пошти мають вирішальне значення для базової функціональності електронної пошти (звідки вона прийшла і куди має надійти). Спочатку E2EE не був вбудований в протоколи електронної пошти, натомість вимагав додаткового програмного забезпечення, такого як OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
