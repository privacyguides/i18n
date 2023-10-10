---
meta_title: "Чому електронна пошта - не найкращий вибір для забезпечення конфіденційності та безпеки - Privacy Guides"
title: Безпека електронної пошти
icon: material/email
description: Електронна пошта за своєю природою є небезпечною, і це одна з причин, чому вона не найкращий вибір для безпечного спілкування.
---

Електронна пошта за замовчуванням є незахищеною формою комунікації. Ви можете підвищити безпеку своєї електронної пошти за допомогою таких інструментів, як OpenPGP, які додають наскрізне шифрування до ваших повідомлень, але OpenPGP все ще має ряд недоліків порівняно з шифруванням в інших програмах обміну повідомленнями, а деякі дані електронної пошти ніколи не можуть бути зашифровані за своєю суттю через те, як влаштована електронна пошта.

Як наслідок, електронну пошту найкраще використовувати для отримання транзакційних повідомлень (наприклад, сповіщень, підтверджень, скидання паролів тощо) від сервісів, на які ви зареєструвалися в Інтернеті, а не для спілкування з іншими людьми.

## Огляд шифрування електронної пошти

Стандартним способом додавання E2EE до листів між різними поштовими провайдерами є використання OpenPGP. Існують різні реалізації стандарту OpenPGP, найпоширенішими з яких є [GnuPG](https://uk.wikipedia.org/wiki/GNU_Privacy_Guard) та [OpenPGP.js](https://openpgpjs.org).

Існує ще один стандарт, популярний серед бізнесу, який називається [S/MIME](https://uk.wikipedia.org/wiki/S/MIME), однак для нього потрібен сертифікат, виданий [Центром сертифікації](https://uk.wikipedia.org/wiki/%D0%90%D0%BA%D1%80%D0%B5%D0%B4%D0%B8%D1%82%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B9_%D1%86%D0%B5%D0%BD%D1%82%D1%80_%D1%81%D0%B5%D1%80%D1%82%D0%B8%D1%84%D1%96%D0%BA%D0%B0%D1%86%D1%96%D1%97_%D0%BA%D0%BB%D1%8E%D1%87%D1%96%D0%B2) (не всі вони видають сертифікати S/MIME). Має підтримку в [Google Workplace](https://support.google.com/a/topic/9061730?hl=en&ref_topic=9061731) і [Outlook for Web або Exchange Server 2016, 2019](https://support.microsoft.com/uk-ua/office/%D1%88%D0%B8%D1%84%D1%80%D1%83%D0%B2%D0%B0%D0%BD%D0%BD%D1%8F-%D0%BF%D0%BE%D0%B2%D1%96%D0%B4%D0%BE%D0%BC%D0%BB%D0%B5%D0%BD%D1%8C-%D0%B7%D0%B0-%D0%B4%D0%BE%D0%BF%D0%BE%D0%BC%D0%BE%D0%B3%D0%BE%D1%8E-%D0%BF%D1%80%D0%BE%D1%82%D0%BE%D0%BA%D0%BE%D0%BB%D1%83-s-mime-%D0%B2-%D1%96%D0%BD%D1%82%D0%B5%D1%80%D0%BD%D0%B5%D1%82-%D0%B2%D0%B5%D1%80%D1%81%D1%96%D1%97-outlook-878c79fc-7088-4b39-966f-14512658f480).

Навіть якщо ви використовуєте OpenPGP, він не підтримує [Пряму секретність](https://uk.wikipedia.org/wiki/%D0%9F%D1%80%D1%8F%D0%BC%D0%B0_%D1%81%D0%B5%D0%BA%D1%80%D0%B5%D1%82%D0%BD%D1%96%D1%81%D1%82%D1%8C), що означає, якщо закритий ключ ваш або одержувача буде викрадено, всі попередні повідомлення, зашифровані за допомогою цього ключа, будуть відкриті. Ось чому ми рекомендуємо [месенджери](../real-time-communication.md), які реалізують пряму секретність через електронну пошту для особистого спілкування, коли це можливо.

## Що таке стандарт Web Key Directory?

Стандарт Web Key Directory (WKD) дозволяє поштовим клієнтам отримувати ключ OpenPGP для інших поштових скриньок, навіть тих, що розміщені в іншого провайдера. Поштові клієнти, які підтримують WKD, запитують у сервера одержувача ключ на основі доменного імені адреси електронної пошти. Наприклад, якщо ви надішлете електронною поштою `jonah@privacyguides.org`, ваш поштовий клієнт запитає `privacyguides.org` про ключ OpenPGP Джона, і якщо `privacyguides.org` має ключ для цього облікового запису, ваше повідомлення буде автоматично зашифровано.

На додачу до [рекомендованих поштових клієнтів](../email-clients.md), які підтримують WKD, деякі провайдери вебпошти також підтримують WKD. Чи буде *ваш власний ключ* опублікований у WKD для використання іншими, залежить від конфігурації вашого домену. Якщо ви використовуєте [провайдера електронної пошти](../email.md#openpgp-compatible-services), який підтримує WKD, наприклад, Proton Mail або Mailbox.org, вони можуть опублікувати для вас ваш ключ OpenPGP на своєму домені.

Якщо ви використовуєте власний домен, вам потрібно буде налаштувати WKD окремо. Якщо ви контролюєте своє доменне ім'я, ви можете налаштувати WKD незалежно від провайдера електронної пошти. Один з простих способів зробити це - скористатися функцією "[WKD як сервіс](https://keys.openpgp.org/about/usage#wkd-as-a-service)" з сайту keys.openpgp.org, встановивши запис CNAME на піддомені `openpgpkey` вашого домену, що вказує на `wkd.keys.openpgp.org`, а потім завантаживши ваш ключ на [keys.openpgp.org](https://keys.openpgp.org/). Крім того, ви можете [самостійно розмістити WKD на власному веб-сервері](https://wiki.gnupg.org/WKDHosting).

Якщо ви використовуєте домен від провайдера, який не підтримує WKD, наприклад @gmail.com, ви не зможете поділитися своїм ключем OpenPGP з іншими за допомогою цього методу.

### Які поштові клієнти підтримують E2EE?

Провайдери електронної пошти, які дозволяють використовувати стандартні протоколи, такі як IMAP та SMTP, можна використовувати з будь-яким з [рекомендованими поштовими клієнтами](../email-clients.md). Залежно від методу автентифікації, це може призвести до зниження безпеки, якщо провайдер або поштовий клієнт не підтримує OATH або додаток-міст, оскільки багатофакторна автентифікація [](multi-factor-authentication.md) неможлива з автентифікацією за допомогою простого пароля.

### Як захистити свої приватні ключі?

Смарт-карта (наприклад, [YubiKey](https://support.yubico.com/hc/en-us/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) або [Nitrokey](https://www.nitrokey.com)) працює, отримуючи зашифроване електронне повідомлення з пристрою (телефона, планшета, комп'ютера тощо), на якому запущено клієнт електронної пошти/веб-пошти. Потім повідомлення розшифровується смарткартою, і розшифрований вміст надсилається назад на пристрій.

Для уникнення можливого потрапляння вашого приватного ключа на скомпрометований пристрій бажано, щоб розшифрування відбувалося на смарткарті.

## Огляд метаданих електронної пошти

Метадані електронного листа зберігаються в [заголовку](https://uk.wikipedia.org/wiki/%D0%95%D0%BB%D0%B5%D0%BA%D1%82%D1%80%D0%BE%D0%BD%D0%BD%D0%B0_%D0%BF%D0%BE%D1%88%D1%82%D0%B0#%D0%97%D0%B0%D0%B3%D0%BE%D0%BB%D0%BE%D0%B2%D0%BA%D0%B8_%D0%BB%D0%B8%D1%81%D1%82%D0%B0) повідомлення електронної пошти і включають деякі видимі поля, такі як `Кому`, `Від`, `Копія`, `Дата`, `Тема`. Існує також низка прихованих заголовків, які включаються багатьма поштовими клієнтами та провайдерами і можуть розкрити інформацію про ваш обліковий запис.

Client software may use email metadata to show who a message is from and what time it was received. Servers may use it to determine where an email message must be sent, among [other purposes](https://en.wikipedia.org/wiki/Email#Message_header) which are not always transparent.

### Who Can View Email Metadata?

Email metadata is protected from outside observers with [Opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS) protecting it from outside observers, but it is still able to be seen by your email client software (or webmail) and any servers relaying the message from you to any recipients including your email provider. Sometimes email servers will also use third-party services to protect against spam, which generally also have access to your messages.

### Why Can't Metadata be E2EE?

Email metadata is crucial to the most basic functionality of email (where it came from, and where it has to go). E2EE was not built into the email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt email metadata, only the message body itself. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as who you're emailing, the subject lines, when you're emailing, etc.
