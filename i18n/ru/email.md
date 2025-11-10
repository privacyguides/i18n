---
meta_title: "Рекомендации по шифрованной конфиденциальной электронной почте - Privacy Guides"
title: Электронная почта
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

| Провайдер                     | OpenPGP / WKD                          | IMAP / SMTP                                                      | Шифрование с нулевым доступом                           | Анонимные способы оплаты                              |
| ----------------------------- | -------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------- | ----------------------------------------------------- |
| [Proton Mail](#proton-mail)   | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue }  Только платные планы | :material-check:{ .pg-green }                           | Cash <br>Monero via third party                 |
| [Mailbox Mail](#mailbox-mail) | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                                    | :material-information-outline:{ .pg-blue } Только почта | Наличные                                              |
| [Tuta](#tuta)                 | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                           | :material-check:{ .pg-green }                           | Monero via third party <br>Cash via third party |

В дополнение к (или вместо) рекомендованному здесь провайдеру электронной почты, вы можете рассмотреть специализированный [сервис создания псевдонимов электронной почты](email-aliasing.md#recommended-providers) для защиты вашей конфиденциальности. Помимо прочего, эти сервисы могут помочь защитить ваш настоящий почтовый ящик от спама, предотвратить корреляцию ваших аккаунтов маркетологами и шифровать все входящие сообщения с помощью PGP.

- [Больше информации :material-arrow-right-drop-circle:](email-aliasing.md)

## Сервисы, поддерживающие OpenPGP

Эти провайдеры изначально поддерживают шифрование/дешифрование OpenPGP и [стандарт Web Key Directory (WKD)](basics/email-security.md#what-is-the-web-key-directory-standard), что позволяет осуществлять сквозное шифрование электронной почты независимо от провайдера. Например, пользователь Proton Mail может отправить сообщение с E2EE пользователю Mailbox Mail, или ты можешь получать уведомления, зашифрованные с помощью OpenPGP, от интернет-сервисов, которые поддерживают это.

<div class="grid cards" markdown>

- ![Логотип Proton Mail](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](#proton-mail)
- ![Логотип Mailbox Mail](assets/img/email/mailbox-mail.svg){ .twemoji } [Mailbox Mail](#mailbox-mail)

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

Free accounts have some limitations, such as not being able to search body text and not having access to [Proton Mail Bridge](https://proton.me/mail/bridge), which is required to use a [recommended desktop email client](email-clients.md) such as Thunderbird. Платные аккаунты включают такие функции, как Proton Mail Bridge, дополнительное хранилище и поддержку пользовательских доменов. The Proton Unlimited plan or any multi-user Proton plan includes access to [SimpleLogin](email-aliasing.md#simplelogin) Premium.

A [letter of attestation](https://res.cloudinary.com/dbulfrlrz/images/v1714639878/wp-pme/letter-of-attestation-proton-mail-20211109_3138714c61/letter-of-attestation-proton-mail-20211109_3138714c61.pdf) was provided for Proton Mail's apps in November 2021 by [Securitum](https://research.securitum.com).

Proton Mail has internal crash reports that are **not** shared with third parties and can be disabled.

=== "Web"

    From your inbox, select :gear: → **All Settings** → **Account** → **Security and privacy** → **Privacy and data collection**.

    - [ ] Disable **Collect usage dignostics**
    - [ ] Disable **Send crash reports**

=== "Mobile"

    From your inbox, select :material-menu: → :gear: **Settings** → select your username.

    - [ ] Disable **Send crash reports**
    - [ ] Disable **Collect usage dignostics**

#### :material-check:{ .pg-green } Пользовательские домены и псевдонимы

Платные подписчики Proton Mail могут использовать свой собственный домен или [универсальный адрес](https://proton.me/support/catch-all). Proton Mail также поддерживает [субадресацию](https://proton.me/support/creating-aliases), что полезно для тех, кто не хочет покупать домен.

#### :material-check:{ .pg-green } Конфиденциальные способы оплаты

Proton Mail [принимает](https://proton.me/support/payment-options) **наличные** по почте в дополнение к стандартным платежам кредитными/дебетовыми картами, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) и PayPal. Additionally, you can use [**Monero**](cryptocurrency.md#monero) to purchase vouchers for Proton Mail Plus or Proton Unlimited via their [official](https://discuss.privacyguides.net/t/add-monero-as-an-anonymous-payment-method-for-proton-services/31058/15) reseller [ProxyStore](https://dys2p.com/en/2025-09-09-proton.html).

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

### Mailbox Mail

<div class="admonition recommendation" markdown>

![Mailbox Mail logo](assets/img/email/mailbox-mail.svg){ align=right }

**Mailbox Mail** (formerly *Mailbox.org*) is an email service with a focus on being secure, ad-free, and powered by 100% eco-friendly energy. Они работают с 2014 года. Mailbox Mail базируется в Берлине, Германия.

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

Mailbox Mail позволяет тебе использовать собственный домен поддерживает [универсальные](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) адреса. Mailbox Mail также поддерживает [субадресацию](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), что полезно, если ты не хочешь покупать домен.

#### :material-check:{ .pg-green } Конфиденциальные способы оплаты

Mailbox Mail не принимает криптовалюты в связи с тем, что их платежная система BitPay приостановила работу в Германии. Однако они принимают **наличные** по почте, **наличные** платежи на банковский счет, банковские переводы, кредитные карты, PayPal и несколько специфичных для Германии платежных систем: Paydirekt и Sofortüberweisung.

#### :material-check:{ .pg-green } Безопасность аккаунта

Mailbox Mail поддерживает [двухфакторную аутентификацию](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa)только для своего веб клиента. Ты можешь использовать либо TOTP, либо [YubiKey](security-keys.md#yubikey) через [YubiCloud](https://yubico.com/products/services-software/yubicloud). Веб-стандарты, такие как [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), пока не поддерживаются.

#### :material-information-outline:{ .pg-blue } Безопасность данных

Mailbox Mail позволяет шифровать входящую почту с помощью их [зашифрованного почтового ящика](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Новые сообщения, которые ты получаешь, будут немедленно зашифрованы твоим открытым ключом.

Однако [Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange), программная платформа, используемая Mailbox Mail, [не поддерживает](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) шифрование твоей адресной книги и календаря. Для таких данных может быть более подходящим [отдельное решение](calendar.md).

#### :material-check:{ .pg-green } Шифрование электронной почты

Mailbox Mail имеет [встроенное шифрование](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) в своем веб-интерфейсе, что упрощает отправку сообщений людям с публичными ключами OpenPGP. Они также позволяют [удаленным получателям расшифровывать электронное письмо](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp)на серверах Mailbox Mail. Эта функция полезна, когда получатель не имеет OpenPGP и не может расшифровать копию письма в собственном почтовом ящике.

Mailbox Mail также поддерживает обнаружение публичных ключей через HTTP из своего WKD. Это позволяет людям за пределами Mailbox Mail легко находить OpenPGP-ключи аккаунтов Mailbox Mail для межпровайдерного сквозного шифрования (E2EE). Это относится только к адресам электронной почты, заканчивающимся на один из собственных доменов Mailbox Mail, таких как `@mailbox.org`. Если ты используешь собственный домен, тебе необходимо [настроить WKD](basics/email-security.md#what-is-the-web-key-directory-standard) отдельно.

#### :material-information-outline:{ .pg-blue } Блокировка аккаунта

Твой аккаунт будет переведен в ограниченный режим пользователя по окончании срока контракта. Он будет безвозвратно удален через [30 дней](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

Ты можешь получить доступ к своему аккаунту Mailbox Mail через IMAP/SMTP, используя их [.onion сервис](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). Однако веб клиент нельзя открыть через их .onion сервис, и ты можешь столкнуться с ошибками TLS-сертификата.

Все аккаунты поставляются с ограниченным облачным хранилищем, которое [можно зашифровать](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox Mail также предлагает псевдоним [secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), который обеспечивает TLS-шифрование соединения между почтовыми серверами — в противном случае сообщение вообще не будет отправлено. Mailbox Mail также поддерживает [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) в дополнение к стандартным протоколам доступа, таким как IMAP и POP3.

Mailbox Mail имеет функцию цифрового наследия для всех тарифных планов. Ты можешь выбрать, хочешь ли ты, чтобы какие-либо из твоих данных были переданы твоим наследникам, при условии, что они подадут заявление и предоставят твоё завещание. Кроме того, ты можешь назначить наследника по имени и адресу.

## Дополнительные провайдеры

Эти провайдеры хранят твою электронную почту с помощью шифрования с нулевым знанием, что делает их отличными вариантами для безопасного хранения твоей электронной почты. Однако они не поддерживают совместимые между различными провайдерами стандарты шифрования для E2EE коммуникаций.

<div class="grid cards" markdown>

- ![Логотип Tuta](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Логотип Tuta](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](#tuta)

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

Tuta only directly accepts credit cards and PayPal, however you can use [**cryptocurrency**](cryptocurrency.md) to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with ProxyStore.

#### :material-check:{ .pg-green } Безопасность аккаунта

Tuta поддерживает [двухфакторную аутентификацию](https://tuta.com/support#2fa) с использованием либо TOTP, либо U2F.

#### :material-check:{ .pg-green } Безопасность данных

Tuta имеет [шифрование с нулевым доступом](https://tuta.com/support#what-encrypted) для твоих электронных писем, [контактов адресной книги](https://tuta.com/support#encrypted-address-book) и [календарей](https://tuta.com/support#calendar). Это означает, что сообщения и другие данные, хранящиеся на твоём аккаунте, доступны для чтения только тебе.

#### :material-information-outline:{ .pg-blue } Шифрование электронной почты

Tuta [не использует OpenPGP](https://tuta.com/support/#pgp). Аккаунты Tuta могут получать зашифрованные электронные письма от аккаунтов, не использующих Tuta, только когда они отправляются через [временный почтовый ящик Tuta](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Блокировка аккаунта

Tuta [удаляет неактивные бесплатные аккаунты](https://tuta.com/support#inactive-accounts) через шесть месяцев. Ты можешь повторно использовать деактивированный бесплатный аккаунт, если заплатишь.

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

Tuta предлагает бизнес-версию [Tuta для некоммерческих организаций](https://tuta.com/blog/secure-email-for-non-profit) бесплатно или с существенной скидкой.

## Критерии

**Обрати внимание, что мы не связаны ни с одним из рекомендуемых провайдеров.** В дополнение к [нашим стандартным критериям](about/criteria.md), мы разработали четкий набор требований для любого провайдера электронной почты, желающего получить нашу рекомендацию, включая внедрение лучших отраслевых практик, современных технологий и многое другое. Советуем тебе ознакомиться с этим списком перед выбором провайдера электронной почты и провести собственное исследование, чтобы убедиться, что выбранный тобой провайдер электронной почты является правильным выбором для тебя.

### Технология

Мы считаем эти особенности важными для обеспечения безопасного и оптимального обслуживания. Тебе следует рассмотреть, есть ли у провайдера функции, которые тебе необходимы.

**Минимальные требования:**

- Должен шифровать данные учетных записей электронной почты в состоянии покоя с помощью шифрования с нулевым доступом.
- Должен быть способен экспортировать электронные письма в формате [Mbox](https://en.wikipedia.org/wiki/Mbox) или отдельных файлов .EML со стандартом [RFC5322](https://datatracker.ietf.org/doc/rfc5322).
- Должен позволять пользователям использовать собственное [доменное имя](https://en.wikipedia.org/wiki/Domain_name). Пользовательские доменные имена важны для пользователей, поскольку позволяют им сохранить свое агентство от сервиса, если он окажется плохим или будет приобретен другой компанией, которая не уделяет приоритетного внимания конфиденциальности.
- Должен работать на собственной инфраструктуре, т.е. не основываться на сторонних провайдерах электронной почты.

**В лучшем случае:**

- Должен шифровать все данные аккаунта (контакты, календари и т.д.) в состоянии покоя с помощью шифрования с нулевым доступом.
- Должен предоставлять встроенное сквозное E2EE/PGP шифрование в веб-интерфейсе для удобства пользователей.
- Должен поддерживать WKD для улучшенного обнаружения публичных OpenPGP-ключей через HTTP. GnuPG-пользователи могут получить ключ с помощью этой команды: `gpg --locate-key example_user@example.com`.
- Поддержка временного почтового ящика для внешних пользователей. Это полезно, когда ты хочешь отправить зашифрованное письмо без отправки реальной копии твоему получателю. Такие письма обычно имеют ограниченный срок действия, а затем автоматически удаляются. Они также не требуют от получателя настройки какой-либо криптографии, как OpenPGP.
- Должен поддерживать [субадресацию](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Должен позволять пользователям использовать собственное [доменное имя](https://en.wikipedia.org/wiki/Domain_name). Пользовательские доменные имена важны для пользователей, поскольку позволяют им сохранить свое агентство от сервиса, если он окажется плохим или будет приобретен другой компанией, которая не уделяет приоритетного внимания конфиденциальности.
- Функциональность универсального адреса или псевдонимов для тех, кто использует собственные домены.
- Должен использовать стандартные протоколы доступа к электронной почте, такие как IMAP, SMTP или [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Стандартные протоколы доступа обеспечивают клиентам возможность легко скачать всю свою электронную почту, если они захотят перейти к другому провайдеру.
- Сервисы провайдера электронной почты должны быть доступны через [onion-сервис](https://en.wikipedia.org/wiki/.onion).

### Конфиденциальность

Мы предпочитаем, чтобы рекомендуемые нами поставщики собирали как можно меньше данных.

**Минимальные требования:**

- Должен защищать IP-адрес отправителя, что может включать его фильтрацию от отображения в поле заголовка `Received`.
- Не должен требовать персональную идентифицирующую информацию (PII) помимо имени пользователя и пароля.
- Политика конфиденциальности должна соответствовать требованиям, определенным GDPR.

**В лучшем случае:**

- Должен принимать [анонимные способы оплаты](advanced/payments.md) ([криптовалюта](cryptocurrency.md), наличные, подарочные карты и т.д.)
- Должен размещаться в юрисдикции с сильными законами о защите конфиденциальности электронной почты.

### Безопасность

Почтовые серверы работают с большим количеством очень конфиденциальных данных. Мы ожидаем, что провайдеры будут применять лучшие отраслевые практики для защиты своих клиентов.

**Минимальные требования:**

- Защита веб-почты с помощью двухфакторной аутентификации, такой как [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Шифрование с нулевым доступом, которое основывается на шифровании данных в состоянии покоя. Провайдер не имеет ключей расшифровки для хранящихся у него данных. Это предотвращает утечку данных, к которым имеет доступ недобросовестный сотрудник. Или утечку данных, которые злоумышленник украл, получив несанкционированный доступ к серверу.
- Поддержка [DNSSEC](https://ru.wikipedia.org/wiki/DNSSEC).
- Отсутствие ошибок TLS или уязвимостей при профилировании такими инструментами, как [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh) или [Qualys SSL Labs](https://ssllabs.com/ssltest); это включает ошибки, связанные с сертификатами, и слабые параметры DH, такие как те, которые привели к [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security))).
- Предпочтительный набор серверных шифров (опционально для TLS 1.3) с поддержкой сильных шифронаборов, которые обеспечивают прямую секретность и аутентифицированное шифрование.
- Действующая политика [MTA-STS](https://tools.ietf.org/html/rfc8461) и [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Действительные записи [DANE](https://ru.wikipedia.org/wiki/DANE).
- Действительные записи [SPF](https://ru.wikipedia.org/wiki/Sender_Policy_Framework) и [DKIM](https://ru.wikipedia.org/wiki/DomainKeys_Identified_Mail).
- Должен иметь правильную [DMARC](https://en.wikipedia.org/wiki/DMARC) запись и политику или использовать [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) для аутентификации. Если используется DMARC-аутентификация, политика должна быть установлена на `reject` или `quarantine`.
- Предпочтительный набор серверных протоколов TLS 1.2 или новее и план для [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) отправка, при условии использования SMTP.
- Стандарты безопасности веб-сайта, такие как:
    - [Строгая транспортная безопасность HTTP](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Целостность субресурса](https://en.wikipedia.org/wiki/Subresource_Integrity) при загрузке вещей из внешних доменов.
- Должен поддерживать просмотр [заголовков сообщений](https://en.wikipedia.org/wiki/Email#Message_header), так как это важная функция для криминалистического анализа, позволяющая определить, является ли электронное письмо попыткой фишинга.

**В лучшем случае:**

- Должен поддерживать аппаратную аутентификацию, т.е. U2F и [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [Запись ресурса DNS Certification Authority Authorization (CAA)](https://tools.ietf.org/html/rfc6844) в дополнение к поддержке DANE.
- Должен реализовывать [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), что полезно для людей, публикующих сообщения в списках рассылки [RFC8617](https://tools.ietf.org/html/rfc8617).
- Опубликованные аудиты безопасности от авторитетной, сторонней компании.
- Программы "bug-bounty" и/или скоординированный процесс раскрытия информации об уязвимостях.
- Стандарты безопасности веб-сайта, такие как:
    - [Политика безопасности контента (CSP, Content-Security-Policy)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Доверие

Ты бы не доверил свои финансы человеку с поддельной личностью, так почему же ты должен доверять им свою электронную почту? Мы требуем, чтобы рекомендованные нами поставщики услуг открыто заявляли о своих владельцах или своём руководстве. Мы также хотели бы видеть частые отчеты о прозрачности, особенно в отношении того, как обрабатываются правительственные запросы.

**Минимальные требования:**

- Руководство или владение, ориентированное на общественность.

**В лучшем случае:**

- Частые отчеты о прозрачности.

### Маркетинг

С рекомендуемыми нами провайдерами электронной почты мы хотим видеть ответственный маркетинг.

**Минимальные требования:**

- Должен самостоятельно хостить аналитику (без Google Analytics, Adobe Analytics и т.д.).
- Не должен иметь безответственного маркетинга, который может включать следующее:
    - Заявления о "нерушимом шифровании". Шифрование должно использоваться с пониманием того, что оно может не остаться секретным в будущем, когда появится технология для его взлома.
    - Гарантии 100% защиты анонимности. Когда кто-то заявляет, что нечто обеспечивает 100% защиту, это означает, что не допускается возможность неудачи. Мы знаем, что люди могут довольно легко деанонимизировать себя различными способами, например:
        - Повторное использование личной информации, например (учетных записей электронной почты, уникальных псевдонимов и т.д.), к которой они получали доступ без программного обеспечения для анонимности, такого как Tor
        - [Цифровые отпечатки браузера](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**В лучшем случае:**

- Четкая и легко читаемая документация для таких задач, как настройка 2FA, почтовых клиентов, OpenPGP и т.д.

### Дополнительная функциональность

Хотя это не строгие требования, есть некоторые другие факторы удобства или конфиденциальности, которые мы рассматривали при определении того, каких провайдеров рекомендовать.
