---
meta_title: "Рекомендации по шифрованной конфиденциальной электронной почте - Privacy Guides"
title: "Электронная почта"
icon: material/email
description: Эти провайдеры электронной почты предлагают отличное место для безопасного хранения твоих писем. Многие из них предлагают еще и совместимое с другими провайдерами шифрование OpenPGP.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Защищает от следующих угроз:</small>

- [:material-server-network: Поставщики услуг](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Электронная почта практически всегда необходима для использования любого онлайн-сервиса, однако мы не рекомендуем использовать её для общения с людьми. Вместо того, чтобы использовать электронную почту для связи с другими людьми, мы советуем использовать мессенджеры, которые поддерживают прямую секретность.

[Рекомендуемые мессенджеры](real-time-communication.md ""){.md-button}

## Рекомендованные провайдеры

Для всего остального мы рекомендуем различных провайдеров электронной почты, которые базируются на устойчивых бизнес-моделях и встроенных функциях безопасности и конфиденциальности. Для получения дополнительной информации, ознакомьтесь с [полным списком критериев](#criteria).

| Провайдер                   | OpenPGP / WKD                          | IMAP / SMTP                                                      | Шифрование с нулевым доступом                           | Анонимные способы оплаты                    |
| --------------------------- | -------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue }  Только платные планы | :material-check:{ .pg-green }                           | Наличные                                    |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                                    | :material-information-outline:{ .pg-blue } Только почта | Наличные                                    |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                           | :material-check:{ .pg-green }                           | Monero <br>Наличные через третьих лиц |

В дополнение к (или вместо) рекомендованному здесь провайдеру электронной почты, вы можете рассмотреть специализированный [сервис создания псевдонимов электронной почты](email-aliasing.md#recommended-providers) для защиты вашей конфиденциальности. Помимо прочего, эти сервисы могут помочь защитить ваш настоящий почтовый ящик от спама, предотвратить корреляцию ваших аккаунтов маркетологами и шифровать все входящие сообщения с помощью PGP.

- [Больше информации :material-arrow-right-drop-circle:](email-aliasing.md)

## Сервисы, поддерживающие OpenPGP

Эти провайдеры изначально поддерживают шифрование/дешифрование OpenPGP и [стандарт Web Key Directory (WKD)](basics/email-security.md#what-is-the-web-key-directory-standard), что позволяет осуществлять сквозное шифрование электронной почты независимо от провайдера. Например, пользователь Proton Mail может отправлять E2EE-зашифрованное сообщение пользователю Mailbox.org, или ты можешь получить OpenPGP-зашифрованное уведомление от интернет-сервисов, поддерживающих такую функцию.

<div class="grid cards" markdown>

- ![Логотип Proton Mail](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Логотип Mailbox.org](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

Когда вы используете технологию E2EE вроде OpenPGP, электронные письма все равно содержат некоторые незашифрованные метаданные в заголовках письма, в том числе тему! Узнайте больше о [метаданных электронной почты](basics/email-security.md#email-metadata-overview).

OpenPGP также не поддерживает прямую секретность, поэтому если твой приватный ключ или ключ адресата будет украден, все предыдущие сообщения, зашифрованные с его помощью, будут раскрыты.

- [Как я могу защитить свои приватные ключи?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Логотип Proton Mail](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** — это сервис электронной почты, фокусирующийся на приватности, шифровании, безопасности и простоте использования. Они работают с 2013 года. Компания Proton AG базируется в Женеве, Швейцария.

Бесплатный план Proton включает 500 МБ хранилища для почты, которое вы можете бесплатно увеличить до 1 ГБ.

[:octicons-home-16: Главная](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/mail/privacy-policy){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title="Документация" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Исходный код" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Бесплатные аккаунты имеют некоторые ограничения, такие как невозможность поиска писем по седержимому и отсутствие доступа к [Proton Mail Bridge](https://proton.me/mail/bridge), который необходим для использования [рекомендуемого настольного почтового клиента](email-clients.md) (например, Thunderbird). Платные аккаунты включают такие функции, как Proton Mail Bridge, дополнительное хранилище и поддержку пользовательских доменов. Если у тебя есть план Proton Unlimited или любой многопользовательский план Proton, ты также получаешь [SimpleLogin](email-aliasing.md#simplelogin) Premium бесплатно.

[Аттестационное письмо](https://proton.me/blog/security-audit-all-proton-apps) было предоставлено для приложений Proton Mail 9 ноября 2021 года компанией [Securitum](https://research.securitum.com).

У Proton Mail есть внутренние отчеты о сбоях, которые **не** передаются третьим сторонам. Это можно отключить в веб-приложении: :gear: → **Все настройки** → **Аккаунт** → **Безопасность и конфиденциальность** → **Конфиденциальность и сбор данных**.

#### :material-check:{ .pg-green } Пользовательские домены и псевдонимы

Платные подписчики Proton Mail могут использовать свой собственный домен или [универсальный адрес](https://proton.me/support/catch-all). Proton Mail также поддерживает [субадресацию](https://proton.me/support/creating-aliases), что полезно для тех, кто не хочет покупать домен.

#### :material-check:{ .pg-green } Конфиденциальные способы оплаты

Proton Mail [принимает](https://proton.me/support/payment-options) **наличные** по почте в дополнение к стандартным платежам кредитными/дебетовыми картами, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) и PayPal.

#### :material-check:{ .pg-green } Безопасность аккаунта

Proton Mail поддерживает [двухфакторную аутентификацию](https://proton.me/support/two-factor-authentication-2fa) TOTP и [аппаратные ключи безопасности](https://proton.me/support/2fa-security-key) с использованием стандартов FIDO2 или U2F. Использование аппаратного ключа безопасности требует предварительной настройки двухфакторной аутентификации TOTP.

#### :material-check:{ .pg-green } Безопасность данных

Proton Mail использует [шифрование с нулевым доступом](https://proton.me/blog/zero-access-encryption) в состоянии покоя для твоих писем и [календарей](https://proton.me/news/protoncalendar-security-model). Данные, защищенные с помощью шифрования с нулевым доступом, доступны только тебе.

Определенная информация, хранящаяся в [Proton Contacts](https://proton.me/support/proton-contacts), такая, как имена пользователей и адреса электронной почты, не защищена шифрованием с нулевым доступом. Поля контактов, поддерживающие шифрование с нулевым доступом, например номера телефонов, обозначаются значком замка.

#### :material-check:{ .pg-green } Шифрование электронной почты

Proton Mail [интегрировал шифрование OpenPGP](https://proton.me/support/how-to-use-pgp) в свою веб-почту. Письма, отправленные на другие аккаунты Proton Mail шифруются автоматически. Шифрование писем с помощью ключа OpenPGP на адреса, не принадлежащие Proton Mail, можно легко включить в настройках аккаунта. Proton также поддерживает автоматическое обнаружение внешних ключей с помощью WKD. Это означает, что письма, отправляемые другим провайдерам, использующим WKD, также будут автоматически шифроваться с помощью OpenPGP без необходимости вручную обмениваться публичными PGP-ключами с твоими контактами. Они также позволяют тебе [шифровать сообщения для адресов, не принадлежащих Proton Mail, без использования OpenPGP](https://proton.me/support/password-protected-emails), причем получателям не нужно регистрировать учетную запись Proton Mail.

Proton Mail также публикует открытые ключи аккаунтов Proton через HTTP из их WKD. Это позволяет людям, не использующим Proton Mail, легко находить OpenPGP-ключи аккаунтов Proton Mail для межпровайдерного сквозного шифрования (E2EE). Это относится только к адресам электронной почты, заканчивающимся на один из собственных доменов Proton, таких, как `@proton.me`. Если ты используешь собственный домен, тебе необходимо [настроить WKD](basics/email-security.md#what-is-the-web-key-directory-standard) отдельно.

#### :material-information-outline:{ .pg-blue } Блокировка аккаунта

Если у тебя платный аккаунт, и твой [счёт не оплачен](https://proton.me/support/delinquency) в течение 14 дней, то ты не сможешь получить доступ к своим данным. Через 30 дней твой аккаунт станет просроченным и не будет получать входящую почту. В течение этого периода тебе будет по-прежнему выставляться счет. Proton [удаляет неактивные бесплатные аккаунты](https://proton.me/support/inactive-accounts) через один год. Ты **не можешь** повторно использовать адрес электронной почты деактивированного аккаунта.

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

План Proton Mail [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) также обеспечивает доступ к другим сервисам Proton в дополнение к предоставлению нескольких пользовательских доменов, неограниченного количества скрытых адресов электронной почты и 500 ГБ хранилища.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Логотип Mailbox.org](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** — это сервис электронной почты, ориентированный на безопасность, отсутствие рекламы и работающий на 100% экологически чистой энергии.

 Они работают с 2014 года. Mailbox.org базируется в Берлине, Германия.

Аккаунты начинаются с объемом хранилища до 2 ГБ, который при необходимости можно увеличить.

[:octicons-home-16: Главная](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="Документация" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Пользовательские домены и псевдонимы

Mailbox.org позволяет тебе использовать собственный домен, и они поддерживают [универсальные](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) адреса. Mailbox.org также поддерживает [субадресацию](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), что полезно, если ты не хочешь покупать домен.

#### :material-check:{ .pg-green } Конфиденциальные способы оплаты

Mailbox.org не принимает криптовалюты в связи с тем, что их платежная система BitPay приостановила работу в Германии. Однако они принимают **наличные** по почте, **наличные** платежи на банковский счет, банковские переводы, кредитные карты, PayPal и несколько специфичных для Германии платежных систем: Paydirekt и Sofortüberweisung.

#### :material-check:{ .pg-green } Безопасность аккаунта

Mailbox.org поддерживает [двухфакторную аутентификацию](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa)только для своего веб клиента. Ты можешь использовать либо TOTP, либо [YubiKey](https://en.wikipedia.org/wiki/YubiKey) через [YubiCloud](https://yubico.com/products/services-software/yubicloud). Веб-стандарты, такие как [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), пока не поддерживаются.

#### :material-information-outline:{ .pg-blue } Безопасность данных

Mailbox.org позволяет шифровать входящую почту с помощью их [зашифрованного почтового ящика](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Новые сообщения, которые ты получаешь, будут немедленно зашифрованы твоим открытым ключом.

Однако [Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange), программная платформа, используемая Mailbox.org, [не поддерживает](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) шифрование твоей адресной книги и календаря. Для таких данных может быть более подходящим [отдельное решение](calendar.md).

#### :material-check:{ .pg-green } Шифрование электронной почты

Mailbox.org имеет [встроенное шифрование](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) в своем веб-интерфейсе, что упрощает отправку сообщений людям с публичными ключами OpenPGP. Они также позволяют [удаленным получателям расшифровывать электронное письмо](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp)на серверах Mailbox.org. Эта функция полезна, когда получатель не имеет OpenPGP и не может расшифровать копию письма в собственном почтовом ящике.

Mailbox.org также поддерживает обнаружение публичных ключей через HTTP из своего WKD. Это позволяет людям за пределами Mailbox.org легко находить OpenPGP-ключи аккаунтов Mailbox.org для межпровайдерного сквозного шифрования (E2EE). Это относится только к адресам электронной почты, заканчивающимся на один из собственных доменов Mailbox.org, таких как `@mailbox.org`. Если ты используешь собственный домен, тебе необходимо [настроить WKD](basics/email-security.md#what-is-the-web-key-directory-standard) отдельно.

#### :material-information-outline:{ .pg-blue } Блокировка аккаунта

Твой аккаунт будет переведен в ограниченный режим пользователя по окончании срока контракта. Он будет безвозвратно удален через [30 дней](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

Ты можешь получить доступ к своему аккаунту Mailbox.org через IMAP/SMTP, используя их [.onion сервис](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). Однако веб клиент нельзя открыть через их .onion сервис, и ты можешь столкнуться с ошибками TLS-сертификата.

Все аккаунты поставляются с ограниченным облачным хранилищем, которое [можно зашифровать](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org также предлагает псевдоним [secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), который обеспечивает TLS-шифрование соединения между почтовыми серверами — в противном случае сообщение вообще не будет отправлено. Mailbox.org также поддерживает [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) в дополнение к стандартным протоколам доступа, таким как IMAP и POP3.

Mailbox.org имеет функцию цифрового наследия для всех тарифных планов. Ты можешь выбрать, хочешь ли ты, чтобы какие-либо из твоих данных были переданы твоим наследникам, при условии, что они подадут заявление и предоставят твоё завещание. Кроме того, ты можешь назначить наследника по имени и адресу.

## Дополнительные провайдеры

Эти провайдеры хранят твою электронную почту с помощью шифрования с нулевым знанием, что делает их отличными вариантами для безопасного хранения твоей электронной почты. Однако они не поддерживают совместимые между различными провайдерами стандарты шифрования для E2EE коммуникаций.

<div class="grid cards" markdown>

- ![Логотип Tuta](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Логотип Tuta](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Логотип Tuta](assets/img/email/tuta.svg#only-light){ align=right }
![Логотип Tuta](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (ранее *Tutanota*) - это сервис электронной почты, в котором особое внимание уделяется безопасности и конфиденциальности благодаря использованию шифрования. Tuta работает с 2011 года и базируется в Ганновере, Германия.

Бесплатные аккаунты начинаются с 1 ГБ хранилища.

[:octicons-home-16: Главная](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Политики конфиденциальности" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="Документация" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link 

<details class="downloads" markdown>
<summary>Скачать</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:fontawesome-brands-windows: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta не поддерживает [протокол IMAP](https://tuta.com/support#imap) или использование сторонних [почтовых клиентов](email-clients.md), а также ты не сможешь добавить [внешние учетные записи электронной почты](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) в приложение Tuta. [Импорт электронных писем](https://github.com/tutao/tutanota/issues/630) в настоящее время также не поддерживается, хотя это [планируется изменить](https://tuta.com/blog/kickoff-import). Письма можно экспортировать [по отдельности или путем массового выбора](https://tuta.com/support#generalMail) для каждой папки, что может быть неудобно, если у тебя много папок.

#### :material-check:{ .pg-green } Пользовательские домены и псевдонимы

Платные аккаунты Tuta могут использовать либо 15, либо 30 псевдонимов в зависимости от плана и неограниченное количество псевдонимов на [собственных доменах](https://tuta.com/support#custom-domain). Tuta не позволяет использовать [субадресацию (плюс-адреса)](https://tuta.com/support#plus), но ты можешь использовать [универсальный адрес](https://tuta.com/support#settings-global) с собственным доменом.

#### :material-information-outline:{ .pg-blue } Конфиденциальные способы оплаты

Tuta напрямую принимает только кредитные карты и PayPal, однако [**криптовалюта**](cryptocurrency.md) может быть использована для покупки подарочных карт через их [партнерство](https://tuta.com/support/#cryptocurrency) с ProxyStore.

#### :material-check:{ .pg-green } Безопасность аккаунта

Tuta supports [two-factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Безопасность данных

Tuta has [zero-access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). Это означает, что сообщения и другие данные, хранящиеся на твоём аккаунте, доступны для чтения только тебе.

#### :material-information-outline:{ .pg-blue } Шифрование электронной почты

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Блокировка аккаунта

Tuta will [delete inactive free accounts](https://tuta.com/support#inactive-accounts) after six months. Ты можешь повторно использовать деактивированный бесплатный аккаунт, если заплатишь.

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/secure-email-for-non-profit) for free or with a heavy discount.

## Критерии

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an email provider, and conduct your own research to ensure the email provider you choose is the right choice for you.

### Технология

Мы считаем эти особенности важными для обеспечения безопасного и оптимального обслуживания. You should consider whether the provider has the features you require.

**Минимальные требования:**

- Must encrypt email account data at rest with zero-access encryption.
- Must be capable of exporting emails as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .EML with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Пользовательские доменные имена важны для пользователей, поскольку позволяют им сохранить свое агентство от сервиса, если он окажется плохим или будет приобретен другой компанией, которая не уделяет приоритетного внимания конфиденциальности.
- Must operate on owned infrastructure, i.e. not built upon third-party email service providers.

**В лучшем случае:**

- Should encrypt all account data (contacts, calendars, etc.) at rest with zero-access encryption.
- Should provide integrated webmail E2EE/PGP encryption as a convenience.
- Should support WKD to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key with this command: `gpg --locate-key example_user@example.com`.
- Поддержка временного почтового ящика для внешних пользователей. This is useful when you want to send an encrypted email without sending an actual copy to your recipient. Такие письма обычно имеют ограниченный срок действия, а затем автоматически удаляются. Они также не требуют от получателя настройки какой-либо криптографии, как OpenPGP.
- Should support [sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Should allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Пользовательские доменные имена важны для пользователей, поскольку позволяют им сохранить свое агентство от сервиса, если он окажется плохим или будет приобретен другой компанией, которая не уделяет приоритетного внимания конфиденциальности.
- Catch-all or alias functionality for those who use their own domains.
- Should use standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.
- Email provider's services should be available via an [onion service](https://en.wikipedia.org/wiki/.onion).

### Конфиденциальность

Мы предпочитаем, чтобы рекомендуемые нами поставщики собирали как можно меньше данных.

**Минимальные требования:**

- Must protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Must not require personally identifiable information (PII) besides a username and a password.
- Privacy policy must meet the requirements defined by the GDPR.

**В лучшем случае:**

- Should accept [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Should be hosted in a jurisdiction with strong email privacy protection laws.

### Безопасность

Email servers deal with a lot of very sensitive data. We expect that providers will adopt industry best practices in order to protect their customers.

**Минимальные требования:**

- Protection of webmail with 2FA, such as [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Zero-access encryption, which builds on encryption at rest. Провайдер не имеет ключей расшифровки для хранящихся у него данных. Это предотвращает утечку данных, к которым имеет доступ недобросовестный сотрудник. Или утечку данных, которые злоумышленник украл, получив несанкционированный доступ к серверу.
- Поддержка [DNSSEC](https://ru.wikipedia.org/wiki/DNSSEC).
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLS 1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- Действующая политика [MTA-STS](https://tools.ietf.org/html/rfc8461) и [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Действительные записи [DANE](https://ru.wikipedia.org/wiki/DANE).
- Действительные записи [SPF](https://ru.wikipedia.org/wiki/Sender_Policy_Framework) и [DKIM](https://ru.wikipedia.org/wiki/DomainKeys_Identified_Mail).
- Must have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. Если используется DMARC-аутентификация, политика должна быть установлена на `reject` или `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) отправка, при условии использования SMTP.
- Стандарты безопасности веб-сайта, такие как:
    - [Строгая транспортная безопасность HTTP](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Целостность субресурса](https://en.wikipedia.org/wiki/Subresource_Integrity) при загрузке вещей из внешних доменов.
- Must support viewing of [message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**В лучшем случае:**

- Should support hardware authentication, i.e. U2F and [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [Запись ресурса DNS Certification Authority Authorization (CAA)](https://tools.ietf.org/html/rfc6844) в дополнение к поддержке DANE.
- Should implement [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Published security audits from a reputable, third-party firm.
- Программы "bug-bounty" и/или скоординированный процесс раскрытия информации об уязвимостях.
- Стандарты безопасности веб-сайта, такие как:
    - [Политика безопасности контента (CSP, Content-Security-Policy)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Доверие

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? Мы требуем, чтобы рекомендованные нами поставщики услуг открыто заявляли о своих владельцах или своём руководстве. Мы также хотели бы видеть частые отчеты о прозрачности, особенно в отношении того, как обрабатываются правительственные запросы.

**Минимальные требования:**

- Руководство или владение, ориентированное на общественность.

**В лучшем случае:**

- Частые отчеты о прозрачности.

### Маркетинг

With the email providers we recommend, we like to see responsible marketing.

**Минимальные требования:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.).
- Must not have any irresponsible marketing, which can include the following:
    - Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
    - Guarantees of protecting anonymity 100%. When someone makes a claim that something is 100%, it means there is no certainty for failure. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:
        - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software such as Tor
        - [Цифровые отпечатки браузера](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**В лучшем случае:**

- Clear and easy-to-read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### Дополнительная функциональность

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
