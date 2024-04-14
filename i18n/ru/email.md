---
meta_title: "Рекомендации по шифрованной конфиденциальной электронной почте - Privacy Guides"
title: "Электронная почта"
icon: material/email
description: Эти провайдеры электронной почты предлагают отличное место для безопасного хранения ваших писем. Многие из них предлагают еще и совместимое с другими провайдерами шифрование OpenPGP.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<!-- markdownlint-disable MD024 -->
Электронная почта практически всегда необходима для использования любого онлайн-сервиса, однако мы не рекомендуем использовать её для общения с людьми. Вместо того, чтобы использовать электронную почту для связи с другими людьми, мы советуем использовать мессенджеры, которые поддерживают прямую секретность.

[Рекомендуемые мессенджеры](real-time-communication.md ""){.md-button}

## Рекомендованные провайдеры

Для всего остального мы рекомендуем различных провайдеров электронной почты, которые базируются на устойчивых бизнес-моделях и встроенных функциях безопасности и конфиденциальности. Для получения дополнительной информации, ознакомьтесь с \[полным списком критериев\](#_18).

| Provider                    | OpenPGP / WKD                          | IMAP / SMTP                                                | Zero Access Encryption                               | Anonymous Payments            |
| --------------------------- | -------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------- | ----------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Paid plans only | :material-check:{ .pg-green }                        | Наличные                      |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                              | :material-information-outline:{ .pg-blue } Mail only | Наличные                      |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                        | Monero & Cash via third-party |

In addition to (or instead of) an email provider recommended here, you may wish to consider a dedicated [email aliasing service](email-aliasing.md) to protect your privacy. Among other things, these services can help protect your real inbox from spam, prevent marketers from correlating your accounts, and encrypt all incoming messages with PGP.

- [More Information :material-arrow-right-drop-circle:](email-aliasing.md)

## Сервисы, поддерживающие OpenPGP

Эти провайдеры нативно поддерживают шифрование/дешифрование с помощью OpenPGP и стандарт [Web Key Directory](basics/email-security.md#what-is-the-web-key-directory-standard), что позволяет использовать E2EE, не зависимо от провайдера. Например, пользователь Proton Mail может отправлять E2EE-зашифрованное сообщение пользователю Mailbox.org, или ты можешь получить OpenPGP-зашифрованное уведомление от интернет-сервисов, поддерживающих такую функцию.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

Когда вы используете технологию E2EE вроде OpenPGP, электронные письма все равно содержат некоторые незашифрованные метаданные в заголовках письма, в том числе тему! Узнайте больше о [метаданных электронной почты](basics/email-security.md#email-metadata-overview).

OpenPGP также не поддерживает прямую секретность, поэтому если ваш приватный ключ или ключ адресата будет украден, все предыдущие сообщения, зашифрованные с его помощью, будут раскрыты. [Как я могу защитить свои приватные ключи?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Логотип Proton Mail](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** — это сервис электронной почты, фокусирующийся на приватности, шифровании, безопасности и простоте использования. Они работают с **2013** года. Компания Proton AG базируется в Женеве, Швейцария. The Proton Mail Free plan comes with 500MB of Mail storage, which you can increase up to 1GB for free.

[:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
- [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Бесплатные аккаунты имеют некоторые ограничения, такие как невозможность поиска писем по седержимому и отсутствие доступа к [Proton Mail Bridge](https://proton.me/mail/bridge), который необходим для использования [рекомендуемого настольного почтового клиента](email-clients.md) (например, Thunderbird). Платные аккаунты включают такие функции, как Proton Mail Bridge, дополнительное хранилище и поддержку пользовательских доменов. [Аттестационное письмо](https://proton.me/blog/security-audit-all-proton-apps) было предоставлено для приложений Proton Mail 9 ноября 2021 года компанией [Securitum](https://research.securitum.com).

If you have the Proton Unlimited, Business, Family, or Visionary plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

Proton Mail has internal crash reports that are **not** shared with third parties. This can be disabled in the web app: :gear: → **All Settings** → **Account** → **Security and privacy** → **Privacy and data collection**.

#### :material-check:{ .pg-green } Пользовательские домены и псевдонимы

Платные подписчики Proton Mail могут использовать свой собственный домен или [универсальный адрес](https://proton.me/support/catch-all). Proton Mail also supports [sub-addressing](https://proton.me/support/creating-aliases), which is useful for people who don't want to purchase a domain.

#### :material-check:{ .pg-green } Конфиденциальные способы оплаты

Proton Mail [принимает](https://proton.me/support/payment-options) наличные по почте в дополнение к стандартным платежам кредитными/дебетовыми картами, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), и PayPal.

#### :material-check:{ .pg-green } Безопасность аккаунта

Proton Mail поддерживает [двухфакторную аутентификацию](https://proton.me/support/two-factor-authentication-2fa) TOTP и [аппаратные ключи безопасности](https://proton.me/support/2fa-security-key) с использованием стандартов FIDO2 или U2F. Использование аппаратного ключа безопасности сначала требует настройки двухфакторной аутентификации TOTP.

#### :material-check:{ .pg-green } Безопасность данных

Proton Mail использует [шифрование с нулевым доступом](https://proton.me/blog/zero-access-encryption) в состоянии покоя для твоих писем и [календарей](https://proton.me/news/protoncalendar-security-model). Данные, защищенные с помощью шифрования с нулевым доступом, доступны только тебе.

Определенная информация, хранящаяся в [Proton Contacts](https://proton.me/support/proton-contacts), такая, как имена пользователей и адреса электронной почты, не защищена шифрованием с нулевым доступом. Поля контактов, поддерживающие шифрование с нулевым доступом, например номера телефонов, обозначаются значком замка.

#### :material-check:{ .pg-green } Шифрование электронной почты

Proton Mail [интегрировал шифрование OpenPGP](https://proton.me/support/how-to-use-pgp) в свою веб-почту. Письма, отправленные на другие аккаунты Proton Mail шифруются автоматически. Шифрование писем с помощью ключа OpenPGP на адреса, не принадлежащие Proton Mail, можно легко включить в настройках аккаунта. Proton also supports automatic external key discovery with [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This means that emails sent to other providers which use WKD will be automatically encrypted with OpenPGP as well, without the need to manually exchange public PGP keys with your contacts. They also allow you to [encrypt messages to non-Proton Mail addresses without OpenPGP](https://proton.me/support/password-protected-emails), without the need for them to sign up for a Proton Mail account.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. Это позволяет людям, не использующим Proton Mail, легко находить OpenPGP-ключи учетных записей Proton Mail для кросс-провайдерского E2EE. Это относится только к адресам электронной почты, заканчивающимся на один из собственных доменов "Протона", например @proton.me. При использовании кастомного домена необходимо [настроить WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) отдельно.

#### :material-information-outline:{ .pg-blue } Блокировка аккаунта

Если у тебя платный аккаунт, и твой [счёт не оплачен](https://proton.me/support/delinquency) в течение 14 дней, то ты не сможешь получить доступ к своим данным. Через 30 дней твой аккаунт станет просроченным и не будет получать входящую почту. В течение этого периода тебе будет по-прежнему выставляться счет. Proton will [delete inactive free accounts](https://proton.me/support/inactive-accounts) after one year. You **cannot** reuse the email address of a deactivated account.

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

Proton Mail's [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) plan also enables access to other Proton services in addition to providing multiple custom domains, unlimited hide-my-email aliases, and 500GB of storage.

Proton Mail не предлагает функцию цифрового наследия.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Логотип Mailbox.org](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** - это сервис электронной почты, ориентированный на безопасность, отсутствие рекламы и приватное электроснабжение от 100% экологически чистой энергии. Они работают с 2014 года. Mailbox.org базируется в Берлине, Германия. Accounts start with up to 2GB storage, which can be upgraded as needed.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Пользовательские домены и псевдонимы

Mailbox.org lets you use your own domain, and they support [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) addresses. Mailbox.org also supports [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green } Конфиденциальные способы оплаты

Mailbox.org не принимает криптовалюты в связи с тем, что их платежная система BitPay приостановила работу в Германии. However, they do accept cash by mail, cash payment to bank account, bank transfer, credit card, PayPal and couple of German-specific processors: paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } Безопасность аккаунта

Mailbox.org supports [two factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. You can use either TOTP or a [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via the [YubiCloud](https://yubico.com/products/services-software/yubicloud). Веб-стандарты, такие, как [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn), пока не поддерживаются.

#### :material-information-outline:{ .pg-blue } Безопасность данных

Mailbox.org allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Новые сообщения, которые ты получаешь, будут немедленно зашифрованы твоим открытым ключом.

However, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. [Отдельное решение](calendar.md) может больше подойти для этой информации.

#### :material-check:{ .pg-green } Шифрование электронной почты

Mailbox.org has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox.org's servers. Эта функция полезна, когда получатель не имеет OpenPGP и не может расшифровать копию письма в собственном почтовом ящике.

Mailbox.org также поддерживает обнаружение открытых ключей через HTTP с их [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Это позволяет людям, не использующим Mailbox.org, легко находить OpenPGP-ключи учетных записей Mailbox.org для кросс-провайдерского E2EE. Это относится только к адресам электронной почты, заканчивающимся на один из собственных доменов "Mailbox.org", например @mailbox.org. При использовании кастомного домена необходимо [настроить WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) отдельно.

#### :material-information-outline:{ .pg-blue } Блокировка аккаунта

Your account will be set to a restricted user account when your contract ends. It will be irrevocably deleted after [30 days](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). Однако доступ к интерфейсу веб-почты через службу .onion невозможен, и ты можешь столкнуться с ошибками сертификата TLS.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox.org также поддерживает [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) в дополнение к стандартным протоколам доступа, таким как IMAP и POP3.

Mailbox.org имеет функцию цифрового наследия для всех тарифных планов. Ты можешь выбрать, хочешь ли ты, чтобы какие-либо из твоих данных были переданы твоим наследникам, при условии, что они подадут заявление и предоставят твоё завещание. Кроме того, ты можешь назначить наследника по имени и адресу.

## Дополнительные провайдеры

Эти провайдеры хранят твою электронную почту с помощью шифрования с нулевым знанием, что делает их отличными вариантами для безопасного хранения твоей электронной почты. Однако они не поддерживают совместимые между различными провайдерами стандарты шифрования для E2EE коммуникаций.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg){ .twemoji } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg){ align=right }

**Tuta** is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since **2011** and is based in Hanover, Germany. Free accounts start with 1GB of storage.

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:simple-windows11: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta doesn't support the [IMAP protocol](https://tuta.com/faq/#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/posts/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/support#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } Пользовательские домены и псевдонимы

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/support#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/support#plus), but you can use a [catch-all](https://tuta.com/support#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } Конфиденциальные способы оплаты

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/faq/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green } Безопасность аккаунта

Tuta supports [two factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Безопасность данных

Tuta has [zero access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). Это означает, что сообщения и другие данные, хранящиеся на твоём аккаунте, доступны для чтения только тебе.

#### :material-information-outline:{ .pg-blue } Шифрование электронной почты

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Блокировка аккаунта

Tuta will [delete inactive free accounts](https://tuta.com/support#inactive-accounts) after six months. Ты можешь повторно использовать деактивированный бесплатный аккаунт, если заплатишь.

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/posts/secure-email-for-non-profit) for free or with a heavy discount.

Tuta doesn't offer a digital legacy feature.

## Электронная почта для самостоятельного хостинга

Продвинутые системные администраторы могут рассмотреть возможность создания собственного сервера электронной почты. Почтовые серверы требуют внимания и постоянного обслуживания, чтобы поддерживать безопасность и надежность доставки почты.

### Комбинированные программные решения

<div class="admonition recommendation" markdown>

![Логотип Mailcow](assets/img/email/mailcow.svg){ align=right }

**Mailcow** - это более продвинутый почтовый сервер, идеально подходящий для тех, у кого есть опыт работы с Linux. В его контейнере Docker есть всё, что тебе нужно: почтовый сервер с поддержкой DKIM, антивирус и мониторинг спама, веб-почта и ActiveSync с SOGo, а также веб-администрирование с поддержкой 2FA.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

</div>

<div class="admonition recommendation" markdown>

![Логотип Mail-in-a-Box](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** - это скрипт автоматической настройки для запуска почтового сервера на Ubuntu. Его цель - облегчить людям создание собственного почтового сервера.

[:octicons-home-16: Домашняя страница](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Документация}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Исходный код" }

</div>

Для ручной настройки мы выбрали эти две статьи:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://c0ffee.net/blog/mail-server-guide) (August 2017)

## Критерии

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an email provider, and conduct your own research to ensure the email provider you choose is the right choice for you.

### Технология

Мы считаем эти особенности важными для обеспечения безопасного и оптимального обслуживания. Ты должен проверить, обладает ли провайдер необходимыми тебе функциями.

**Минимальные требования:**

- Шифрует данные аккаунта электронной почты в состоянии покоя с помощью шифрования с нулевым доступом.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Разрешает пользователям использовать собственное [доменное имя](https://en.wikipedia.org/wiki/Domain_name). Пользовательские доменные имена важны для пользователей, поскольку позволяют им сохранить свое агентство от сервиса, если он окажется плохим или будет приобретен другой компанией, которая не уделяет приоритетного внимания конфиденциальности.
- Работает на собственной инфраструктуре, т.е. не опирается на сторонних провайдеров электронной почты.

**В лучшем случае:**

- Шифрует все данные аккаунта (Контакты, Календари и т.д.) в состоянии покоя с помощью шифрования с нулевым доступом.
- Встроенное шифрование веб-почты E2EE/PGP обеспечивает удобство.
- Поддерживает [WKD](https://wiki.gnupg.org/WKD) для улучшения обнаружения открытых ключей OpenPGP через HTTP. Пользователи GnuPG могут получить ключ, набрав: `gpg --locate-key example_user@example.com`
- Поддержка временного почтового ящика для внешних пользователей. Это полезно, когда вы хотите отправить зашифрованное сообщение электронной почты, не отправляя фактическую копию получателю. Такие письма обычно имеют ограниченный срок действия, а затем автоматически удаляются. Они также не требуют от получателя настройки какой-либо криптографии, как OpenPGP.
- Доступность услуг провайдера электронной почты через [службу .onion](https://en.wikipedia.org/wiki/.onion).
- [Sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing) support.
- Функциональность поймать-все или псевдонимов для тех, кто владеет собственными доменами.
- Использование стандартных протоколов доступа к электронной почте, таких как IMAP, SMTP или [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Стандартные протоколы доступа обеспечивают клиентам возможность легко скачать всю свою электронную почту, если они захотят перейти к другому провайдеру.

### Конфиденциальность

Мы предпочитаем, чтобы рекомендуемые нами поставщики собирали как можно меньше данных.

**Минимальные требования:**

- Защищает IP-адрес отправителя. Отфильтрует его от отображения в поле заголовка `Received`.
- Не требуйте личной идентификационной информации (PII), кроме имени пользователя и пароля.
- Политика конфиденциальности, отвечающая требованиям GDPR.

**В лучшем случае:**

- Принимает [анонимные варианты оплаты](advanced/payments.md) ([криптовалюту](cryptocurrency.md), наличные, подарочные карты и т.д.)
- Хостинг в юрисдикции с сильными законами о защите конфиденциальности электронной почты.

### Безопасность

Серверы электронной почты работают с большим количеством очень конфиденциальных данных. Мы ожидаем, что поставщики услуг будут использовать лучшие отраслевые практики для защиты своих клиентов.

**Минимальные требования:**

- Защита веб-почты с помощью 2FA, например, TOTP.
- Шифрование с нулевым доступом, основанное на шифровании в состоянии покоя. Провайдер не имеет ключей расшифровки для хранящихся у него данных. Это предотвращает утечку данных, к которым имеет доступ недобросовестный сотрудник. Или утечку данных, которые злоумышленник украл, получив несанкционированный доступ к серверу.
- Поддержка [DNSSEC](https://ru.wikipedia.org/wiki/DNSSEC).
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Настройки сервера (опционально для TLSv1.3) для сильных наборов шифров, которые поддерживают прямую секретность и аутентифицированное шифрование.
- Действующая политика [MTA-STS](https://tools.ietf.org/html/rfc8461) и [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Действительные записи [DANE](https://ru.wikipedia.org/wiki/DANE).
- Действительные записи [SPF](https://ru.wikipedia.org/wiki/Sender_Policy_Framework) и [DKIM](https://ru.wikipedia.org/wiki/DomainKeys_Identified_Mail).
- Имеет надлежащую политику и запись [DMARC](https://ru.wikipedia.org/wiki/DMARC) или использует [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) для аутентификации. Если используется DMARC-аутентификация, политика должна быть установлена на `reject` или `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) отправка, при условии использования SMTP.
- Стандарты безопасности веб-сайта, такие как:
    - [Строгая транспортная безопасность HTTP](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Целостность субресурса](https://en.wikipedia.org/wiki/Subresource_Integrity) при загрузке вещей из внешних доменов.
- Должен поддерживать просмотр [заголовков сообщений](https://ru.wikipedia.org/wiki/%D0%AD%D0%BB%D0%B5%D0%BA%D1%82%D1%80%D0%BE%D0%BD%D0%BD%D0%B0%D1%8F_%D0%BF%D0%BE%D1%87%D1%82%D0%B0#%D0%97%D0%B0%D0%B3%D0%BE%D0%BB%D0%BE%D0%B2%D0%BA%D0%B8_%D0%BF%D0%B8%D1%81%D1%8C%D0%BC%D0%B0), поскольку это важнейшая криминалистическая функция, позволяющая определить, является ли письмо попыткой фишинга.

**В лучшем случае:**

- Поддержка аппаратной аутентификации, т.е. U2F и [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn). U2F и WebAuthn являются более безопасными, поскольку для аутентификации людей они используют закрытый ключ, хранящийся на аппаратном устройстве на стороне клиента, в отличие от общего секрета, который хранится на веб-сервере и на стороне клиента при использовании TOTP. Кроме того, U2F и WebAuthn более устойчивы к фишингу, поскольку их ответ аутентификации основан на аутентифицированном [доменном имени](https://ru.wikipedia.org/wiki/%D0%94%D0%BE%D0%BC%D0%B5%D0%BD%D0%BD%D0%BE%D0%B5_%D0%B8%D0%BC%D1%8F).
- [Запись ресурса DNS Certification Authority Authorization (CAA)](https://tools.ietf.org/html/rfc6844) в дополнение к поддержке DANE.
- Реализация [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), это полезно для людей, которые пишут в списки рассылки [RFC8617](https://tools.ietf.org/html/rfc8617).
- Программы "bug-bounty" и/или скоординированный процесс раскрытия информации об уязвимостях.
- Стандарты безопасности веб-сайта, такие как:
    - [Политика безопасности контента (CSP, Content-Security-Policy)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Доверие

Вы бы не доверили свои финансы человеку с фальшивой личностью, так зачем доверять ему свою электронную почту? Мы требуем, чтобы рекомендованные нами поставщики услуг открыто заявляли о своих владельцах или своём руководстве. Мы также хотели бы видеть частые отчеты о прозрачности, особенно в отношении того, как обрабатываются правительственные запросы.

**Минимальные требования:**

- Руководство или владение, ориентированное на общественность.

**В лучшем случае:**

- Лидерство, ориентированное на общественность.
- Частые отчеты о прозрачности.

### Маркетинг

Провайдеры электронной почты, которых мы рекомендуем, предпочитают ответственный маркетинг.

**Минимальные требования:**

- Должен самостоятельно хостить аналитику (без Google Analytics, Adobe Analytics и т.д.). Сайт провайдера также должен соответствовать требованиям [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) для тех, кто желает отказаться от отслеживания.

Не должно быть никакого маркетинга, который является безответственным:

- Заявления о "невзламываемом шифровании." Шифрование должно использоваться с тем расчетом, что в будущем, когда появится технология для его взлома, оно может оказаться не секретным.
- Предоставление гарантий защиты анонимности на 100%. Когда кто-то утверждает: "Это является на 100% ..." - это не означает, что кто-то не может ошибиться. Мы знаем, что люди могут довольно легко деанонимизировать себя различными способами, например:

    - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
    - [Цифровые отпечатки браузера](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**В лучшем случае:**

- Понятная и легко читаемая документация. Сюда входят такие вещи, как настройка 2FA, почтовые клиенты, OpenPGP и т.д.

### Дополнительная функциональность

Хотя это и не является строгими требованиями, существуют и другие факторы удобства или конфиденциальности, на которые мы обращали внимание при выборе рекомендуемых провайдеров.
