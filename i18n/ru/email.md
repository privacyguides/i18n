---
meta_title: "Рекомендации по шифрованной конфиденциальной электронной почте - Privacy Guides"
title: "Электронная почта"
icon: material/email
description: Эти провайдеры электронной почты предлагают отличное место для безопасного хранения ваших писем, а многие из них предлагают еще и совместимое шифрование OpenPGP с другими провайдерами.
cover: email.png
---

Электронная почта практически всегда необходима для использования любого онлайн-сервиса, однако мы не рекомендуем использовать её для общения с людьми. Вместо того, чтобы использовать электронную почту для связи с другими людьми, мы советуем использовать мессенджеры, которые поддерживают прямую секретность.

[Рекомендуемые мессенджеры](real-time-communication.md ""){.md-button}

Для всего остального мы рекомендуем различных провайдеров электронной почты, которые базируются на устойчивых бизнес-моделях и встроенных функциях безопасности и конфиденциальности.

- [Провайдеры электронной почты, поддерживающие OpenPGP :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [Другие провайдеры, поддерживающие шифрование :material-arrow-right-drop-circle:](#more-providers)
- [Сервисы псевдонимов электронной почты :material-arrow-right-drop-circle:](#email-aliasing-services)
- [Варианты самостоятельного хостинга :material-arrow-right-drop-circle:](#self-hosting-email)

## Сервисы, поддерживающие OpenPGP

Эти провайдеры поддерживают OpenPGP шифрование/дешифрование и стандарт Web Key Directory (WKD), позволяя обмениваться E2EE-сообщениями вне зависимости от провайдера. Например, пользователь Proton Mail может отправлять E2EE-зашифрованное сообщение пользователю Mailbox.org, или вы можете получить OpenPGP-зашифрованное уведомление от интернет-сервисов, поддерживающих такую функцию.

<div class="grid cards" markdown>

- ![Логотип Proton Mail](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Логотип Mailbox.org](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

!!! предупреждение

    При использовании технологии E2EE, такой, как OpenPGP, сообщения все равно будут содержать некоторые незашифрованные метаданные в заголовках письма. Узнайте больше о [метаданных электронной почты](basics/email-security.md#email-metadata-overview).
    
    OpenPGP также не поддерживает прямую секретность: если ваш закрытый ключ или закрытый ключ получателя окажется украден, все предыдущие сообщения, зашифрованные с его помощью, будут раскрыты. [Как я могу защитить свои закрытые ключи?](basics/email-security.md#how-do-i-protect-my-private-keys)

### Proton Mail

!!! recommendation

    ![Логотип Proton Mail](assets/img/email/protonmail.svg){ align=right }
    
    **Proton Mail** — это сервис электронной почты, фокусирующийся на приватности, шифровании, безопасности и простоте использования. Они работают с **2013** года. Компания Proton AG базируется в Женеве, Швейцария. Аккаунты получают от 500 МБ хранилища на бесплатном тарифе.
    
    [:octicons-home-16: Домашняя страница](https://proton.me/mail){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion-сервис" }
    [:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Исходный код" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id979659905)
        - [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
        - [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
        - [:simple-apple: macOS](https://proton.me/mail/bridge#download)
        - [:simple-linux: Linux](https://proton.me/mail/bridge#download)
        - [:octicons-browser-16: Веб-версия](https://mail.proton.me)

Бесплатные аккаунты имеют некоторые ограничения, такие как невозможность поиска писем по седержимому и отсутствие доступа к [Proton Mail Bridge](https://proton.me/mail/bridge), который необходим для использования [рекомендуемого настольного почтового клиента](email-clients.md) (например, Thunderbird). Платные аккаунты включают такие функции, как Proton Mail Bridge, дополнительное хранилище и поддержку пользовательских доменов. [Аттестационное письмо](https://proton.me/blog/security-audit-all-proton-apps) было предоставлено для приложений Proton Mail 9 ноября 2021 года компанией [Securitum](https://research.securitum.com).

Если у вас есть план Proton Unlimited, Business или Visionary, вы также получаете [SimpleLogin](#simplelogin) Premium бесплатно.

У компании Proton Mail есть внутренние отчеты об ошибках, которые они **не передают** третьим лицам. Это можно отключить в: **Настройки** > **Перейти в Настройки** > **Учетная запись** > **Безопасность и конфиденциальность** > **Отправка отчетов об ошибках**.

#### :material-check:{ .pg-green } Пользовательские домены и псевдонимы

Платные подписчики Proton Mail могут использовать свой собственный домен или [универсальный адрес](https://proton.me/support/catch-all). Proton Mail также поддерживает [субадресацию](https://proton.me/support/creating-aliases), что полезно для тех, кто не хочет покупать домен.

#### :material-check:{ .pg-green } Конфиденциальные способы оплаты

Proton Mail [принимает](https://proton.me/support/payment-options) наличные по почте в дополнение к стандартным платежам кредитными/дебетовыми картами, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), и PayPal.

#### :material-check:{ .pg-green } Безопасность аккаунта

Proton Mail поддерживает [двухфакторную аутентификацию](https://proton.me/support/two-factor-authentication-2fa) TOTP и [аппаратные ключи безопасности](https://proton.me/support/2fa-security-key) с использованием стандартов FIDO2 или U2F. Использование аппаратного ключа безопасности сначала требует настройки двухфакторной аутентификации TOTP.

#### :material-check:{ .pg-green } Безопасность данных

Proton Mail имеет [шифрование с нулевым доступом](https://proton.me/blog/zero-access-encryption) в состоянии покоя для ваших писем и [календарей](https://proton.me/news/protoncalendar-security-model). Данные, защищенные с помощью шифрования с нулевым доступом, доступны только вам.

Определенная информация, хранящаяся в [Proton Contacts](https://proton.me/support/proton-contacts), такая, как имена пользователей и адреса электронной почты, не защищена шифрованием с нулевым доступом. Поля контактов, поддерживающие шифрование с нулевым доступом, например номера телефонов, обозначаются значком замка.

#### :material-check:{ .pg-green } Шифрование электронной почты

Proton Mail [интегрировал шифрование OpenPGP](https://proton.me/support/how-to-use-pgp) в свою веб-почту. Письма, отправленные на другие аккаунты Proton Mail шифруются автоматически. Шифрование писем с помощью ключа OpenPGP на адреса, не принадлежащие Proton Mail, можно легко включить в настройках аккаунта. Они также позволяют вам [шифровать сообщения на адреса, не относящиеся к Proton Mail](https://proton.me/support/password-protected-emails), без необходимости регистрировать учетную запись Proton Mail или использовать программное обеспечение типа OpenPGP.

Proton Mail также поддерживает обнаружение открытых ключей через HTTP с их [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Это позволяет людям, не использующим Proton Mail, легко находить OpenPGP-ключи учетных записей Proton Mail для кросс-провайдерского E2EE.


#### :material-information-outline:{ .pg-blue } Блокировка аккаунта

Если у вас платный аккаунт, и ваш [счет не оплачен](https://proton.me/support/delinquency) в течение 14 дней, вы не сможете получить доступ к своим данным. Через 30 дней ваш аккаунт станет просроченным и не будет получать входящую почту. В течение этого периода вам будет по-прежнему выставляться счет.

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

Proton Mail предлагает "Proton Unlimited" аккаунт за €9,99/месяц, который также позволяет получить доступ к Proton VPN в дополнение к предоставлению нескольких аккаунтов, доменов, псевдонимов и 500 ГБ хранилища.

Proton Mail не предлагает функцию цифрового наследия.

### Mailbox.org

!!! recommendation

    ![Логотип Mailbox.org](assets/img/email/mailboxorg.svg){ align=right }
    
    **Mailbox.org** - это сервис электронной почты, ориентированный на безопасность, отсутствие рекламы и приватное электроснабжение от 100% экологически чистой энергии. They have been in operation since 2014. Mailbox.org is based in Berlin, Germany. Accounts start with 2 GB of storage, which can be upgraded as needed.
    
    [:octicons-home-16: Домашняя страница](https://mailbox.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Политика конфеденциальности" }
    [:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Документация}
    
    ??? скачать
    
        - [:octicons-browser-16: Сайт](https://login.mailbox.org)

#### :material-check:{ .pg-green } Пользовательские домены и псевдонимы

Mailbox.org позволяет вам использовать собственный домен, и поддерживает [универсальные](https://kb.mailbox.org/display/MBOKBEN/Using+catch-all+alias+with+own+domain) адреса. Mailbox.org также поддерживает [субадресацию](https://kb.mailbox.org/display/BMBOKBEN/What+is+an+alias+and+how+do+I+use+it), что полезно для тех, кто не хочет покупать домен.

#### :material-check:{ .pg-green } Конфиденциальные способы оплаты

Mailbox.org не принимает криптовалюты в связи с тем, что их платежная система BitPay приостановила работу в Германии. Однако, они принимают наличные по почте, оплату наличными на банковский счет, банковский перевод, кредитные карты, PayPal и несколько немецких платёжных систем: paydirekt и Sofortüberweisung.

#### :material-check:{ .pg-green } Безопасность аккаунта

Mailbox.org поддерживает [двухфакторную аутентификацию](https://kb.mailbox.org/display/MBOKBEN/How+to+use+two-factor+authentication+-+2FA) только для своей веб-почты. Вы можете использовать либо TOTP, либо [YubiKey](https://en.wikipedia.org/wiki/YubiKey) с помощью [YubiCloud](https://www.yubico.com/products/services-software/yubicloud). Веб-стандарты, такие, как [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn), пока не поддерживаются.

#### :material-information-outline:{ .pg-blue } Безопасность данных

Mailbox.org позволяет шифровать входящую почту с помощью своего [зашифрованного почтового ящика](https://kb.mailbox.org/display/MBOKBEN/The+Encrypted+Mailbox). Новые сообщения, которые вы получаете, будут немедленно зашифрованы вашим открытым ключом.

Однако [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), программная платформа, используемая Mailbox.org, [не поддерживает](https://kb.mailbox.org/display/BMBOKBEN/Encryption+of+calendar+and+address+book) шифрование вашей адресной книги и календаря. A [standalone option](calendar.md) may be more appropriate for that information.

#### :material-check:{ .pg-green } Шифрование электронной почты

Mailbox.org использует [встроенное шифрование](https://kb.mailbox.org/display/MBOKBEN/Send+encrypted+e-mails+with+Guard) в свою веб-почту, что упрощает отправку сообщений людям с открытыми ключами OpenPGP. Они также позволяют [пользователям без Mailbox.org расшифровывать электронные письма](https://kb.mailbox.org/display/MBOKBEN/My+recipient+does+not+use+PGP) на серверах Mailbox.org. Эта функция полезна, когда получатель не имеет OpenPGP и не может расшифровать копию письма в собственном почтовом ящике.

Mailbox.org также поддерживает обнаружение открытых ключей через HTTP с их [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Это позволяет людям, не использующим Mailbox.org, легко находить OpenPGP-ключи учетных записей Proton Mail для кросс-провайдерского E2EE.

#### :material-information-outline:{ .pg-blue } Блокировка аккаунта

По окончании срока действия подписки ваша учетная запись будет переведена в ограниченный режим, по истечении [30 дней она будет безвозвратно удалена](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

Вы можете получить доступ к вашему аккаунту Mailbox.org через IMAP/SMTP, используя их сервис [.onion](https://kb.mailbox.org/display/MBOKBEN/The+Tor+exit+node+of+mailbox.org). Однако доступ к интерфейсу веб-почты через службу .onion невозможен, и вы можете столкнуться с ошибками сертификата TLS.

Все учетные записи имеют ограниченное облачное хранилище, которое [может быть зашифровано](https://kb.mailbox.org/display/MBOKBEN/Encrypt+files+on+your+Drive). Mailbox.org также предлагает псевдоним [@secure.mailbox.org](https://kb.mailbox.org/display/MBOKBEN/Ensuring+E-Mails+are+Sent+Securely), который требует шифрование TLS от соединения между почтовыми серверами, в противном случае сообщение вообще не будет отправлено. Mailbox.org также поддерживает [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) в дополнение к стандартным протоколам доступа, таким как IMAP и POP3.

Mailbox.org имеет функцию цифрового наследия для всех тарифных планов. Вы можете выбрать, хотите ли вы, чтобы какие-либо из ваших данных были переданы наследникам, при условии, что они подадут заявление и предоставят ваше завещание. Кроме того, вы можете назначить человека по имени и адресу.

## Дополнительные провайдеры

Эти провайдеры хранят вашу электронную почту с помощью шифрования с нулевым знанием, что делает их отличными вариантами для безопасного хранения вашей электронной почты. Однако они не поддерживают совместимые стандарты шифрования для коммуникаций E2EE между провайдерами.

<div class="grid cards" markdown>

- ![Логотип StartMail](assets/img/email/startmail.svg#only-light){ .twemoji }![Логотип StartMail](assets/img/email/startmail-dark.svg#only-dark){ .twemoji } [StartMail](email.md#startmail)
- ![Логотип Tutanota](assets/img/email/tutanota.svg){ .twemoji } [Tutanota](email.md#tutanota)

</div>

### StartMail

!!! recommendation

    ![Логотип StartMail](assets/img/email/startmail.svg#only-light){ align=right }
    ![Логотип StartMail](assets/img/email/startmail-dark.svg#only-dark){ align=right }
    
    **StartMail** - это сервис электронной почты, в котором особое внимание уделяется безопасности и конфиденциальности благодаря использованию стандартного шифрования OpenPGP. StartMail has been in operation since 2014 and is based in Boulevard 11, Zeist Netherlands. Accounts start with 10GB. They offer a 30-day trial.
    
    [:octicons-home-16: Домашняя страница](https://www.startmail.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.startmail.com/en/privacy/){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://support.startmail.com){ .card-link title=Документация}
    
    ??? скачать
    
        - [:octicons-browser-16: Web](https://mail.startmail.com/login)

#### :material-check:{ .pg-green } Пользовательские домены и псевдонимы

Личные аккаунты могут использовать псевдонимы [Custom или Quick](https://support.startmail.com/hc/en-us/articles/360007297457-Aliases). [Пользовательские домены](https://support.startmail.com/hc/en-us/articles/4403911432209-Setup-a-custom-domain) также доступны.

#### :material-alert-outline:{ .pg-orange } Конфиденциальные способы оплаты

StartMail принимает к оплате Visa, MasterCard, American Express и Paypal. StartMail также имеет другие [варианты оплаты](https://support.startmail.com/hc/en-us/articles/360006620637-Payment-methods), такие как [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) (в настоящее время только для личных счетов) и SEPA Direct Debit для счетов старше года.

#### :material-check:{ .pg-green } Безопасность аккаунта

StartMail поддерживает двухфакторную аутентификацию TOTP [только для веб-почты](https://support.startmail.com/hc/en-us/articles/360006682158-Two-factor-authentication-2FA). Он не поддерживает аутентификацию с помощью ключа безопасности U2F.

#### :material-information-outline:{ .pg-blue } Безопасность данных

StartMail имеет [шифрование с нулевым доступом в состоянии покоя](https://www.startmail.com/en/whitepaper/#_Toc458527835), используя свою систему "хранилище пользователя". Когда вы входите в систему, хранилище открывается, и электронное письмо перемещается в хранилище из очереди, где оно расшифровывается соответствующим закрытым ключом.

StartMail поддерживает импорт [контактов](https://support.startmail.com/hc/en-us/articles/360006495557-Import-contacts), однако они доступны только в веб-почте, и не доступны через другие протоколы, такие как [CalDAV](https://en.wikipedia.org/wiki/CalDAV). Контакты не хранятся с использованием шифрования с нулевым знанием.

#### :material-check:{ .pg-green } Шифрование электронной почты

StartMail использует [встроенное шифрование](https://support.startmail.com/hc/en-us/sections/360001889078-Encryption) в своей веб-почте, что упрощает отправку сообщений людям с открытыми ключами OpenPGP. Однако они не поддерживают стандарт Web Key Directory, что делает обнаружение открытого ключа почтового ящика Startmail более сложной задачей для других поставщиков услуг электронной почты или клиентов.

#### :material-information-outline:{ .pg-blue } Блокировка аккаунта

По истечении срока действия аккаунта StartMail удалит вашу учетную запись навсегда после [6 месяцев в 3 этапа](https://support.startmail.com/hc/en-us/articles/360006794398-Account-expiration).

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

StartMail позволяет проксировать изображения в электронных письмах. Если вы разрешите загрузку изображений, отправитель не будет знать, какой у вас IP-адрес.

StartMail не предлагает функцию цифрового наследия.

### Tutanota

!!! recommendation

    ![Логотип Tutanota](assets/img/email/tutanota.svg){ align=right }
    
    **Tutanota** - это сервис электронной почты, в котором особое внимание уделяется безопасности и конфиденциальности благодаря использованию шифрования. Tutanota has been in operation since **2011** and is based in Hanover, Germany. Accounts start with 1GB storage with their free plan.
    
    [:octicons-home-16: Домашняя страница](https://tutanota.com/ru/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://tutanota.com/ru/privacy){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://tutanota.com/ru/faq){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://tutanota.com/community/){ .card-link title=Поддержать }
    
    ??? скачать
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
        - [:simple-appstore: App Store](https://apps.apple.com/app/tutanota/id922429609)
        - [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
        - [:simple-windows11: Windows](https://tutanota.com/ru/#download)
        - [:simple-apple: macOS](https://tutanota.com/ru/#download)
        - [:simple-linux: Linux](https://tutanota.com/ru/#download)
        - [:octicons-browser-16: Web](https://mail.tutanota.com/)

Tutanota не поддерживает [протокол IMAP](https://tutanota.com/faq/#imap) или использование сторонних [почтовых клиентов](email-clients.md). Вы также не сможете добавить [внешние почтовые аккаунты](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) в приложение Tutanota. В настоящее время ни [импорт электронной почты](https://github.com/tutao/tutanota/issues/630), ни [вложенные папки](https://github.com/tutao/tutanota/issues/927) не поддерживаются, однако эти функции [находится в разработке](https://tutanota.com/blog/posts/kickoff-import). Письма можно экспортировать [по отдельности или массовым выбором](https://tutanota.com/howto#generalMail) в каждую папку, что может быть неудобно, если у вас много папок.

#### :material-check:{ .pg-green } Пользовательские домены и псевдонимы

Платные аккаунты Tutanota могут использовать до 5 [псевдонимов](https://tutanota.com/faq#alias) и [пользовательских доменов](https://tutanota.com/faq#custom-domain). Tutanota не позволяет использовать [субадресацию (адреса с плюсом)](https://tutanota.com/faq#plus), но с пользовательским доменом вы можете использовать [универсальный адрес](https://tutanota.com/howto#settings-global).

#### :material-information-outline:{ .pg-blue } Конфиденциальные способы оплаты

Tutanota напрямую принимает только кредитные карты и PayPal, однако [криптовалюта](cryptocurrency.md) может быть использована для покупки подарочных карт через их [партнерство](https://tutanota.com/faq/#cryptocurrency) с Proxystore.

#### :material-check:{ .pg-green } Безопасность аккаунта

Tutanota поддерживает [двухфакторную аутентификацию](https://tutanota.com/faq#2fa) с помощью TOTP или U2F.

#### :material-check:{ .pg-green } Безопасность данных

Tutanota использует [шифрование с нулевым доступом в состоянии покоя](https://tutanota.com/faq#what-encrypted) для вашей электронной почты, [записей контактов](https://tutanota.com/faq#encrypted-address-book), и [календарей](https://tutanota.com/faq#calendar). Это означает, что сообщения и другие данные, хранящиеся на вашем аккаунте, доступны для чтения только вам.

#### :material-information-outline:{ .pg-blue } Шифрование электронной почты

Tutanota [не использует OpenPGP](https://www.tutanota.com/faq/#pgp). Учетные записи Tutanota могут получать зашифрованные электронные письма от учетных записей электронной почты, не принадлежащих Tutanota, только при отправке через [временный почтовый ящик Tutanota](https://www.tutanota.com/howto/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Блокировка аккаунта

Tutanota будет [удалять неактивные бесплатные аккаунты](https://tutanota.com/faq#inactive-accounts) по истечении шести месяцев. Вы можете повторно использовать деактивированный бесплатный аккаунт, если заплатите.

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

Tutanota предлагает бизнес-версию [Tutanota для некоммерческих организаций](https://tutanota.com/blog/posts/secure-email-for-non-profit) бесплатно или с большой скидкой.

Tutanota также имеет функцию для бизнеса под названием [Secure Connect](https://tutanota.com/secure-connect/). Это гарантирует, что контакт клиента с бизнесом использует E2EE. Стоимость функции составляет €240/год.

Tutanota не предлагает функцию цифрового наследия.

## Сервисы псевдонимов электронной почты

Служба псевдонимов электронной почты позволяет легко генерировать новый адрес электронной почты для каждого сайта, на котором вы зарегистрированы. Созданные вами псевдонимы электронной почты затем пересылаются на выбранный вами адрес электронной почты, скрывая как ваш "основной" адрес электронной почты, так и личность вашего поставщика услуг электронной почты. Истинная адресация электронной почты лучше, чем плюсовая адресация, обычно используемая и поддерживаемая многими провайдерами, которая позволяет создавать псевдонимы типа ваше_имя+[что-то_ещё]@example.com, поскольку веб-сайты, рекламодатели и сети отслеживания могут тривиально удалить все, что идет после знака +, чтобы узнать ваш истинный адрес электронной почты.

<div class="grid cards" markdown>

- ![Логотип Proton VPN](assets/img/vpn/protonvpn.svg){ .twemoji } [Proton VPN](vpn.md#protonvpn)
- ![Логотип IVPN](assets/img/vpn/mini/ivpn.svg){ .twemoji } [IVPN](vpn.md#ivpn)
- ![Логотип Mullvad](assets/img/vpn/mullvad.svg){ .twemoji } [Mullvad](vpn.md#mullvad)

</div>

Псевдоним электронной почты может служить защитой на случай, если ваш поставщик услуг электронной почты прекратит свою работу. В этом случае вы можете легко перенаправить свои псевдонимы на новый адрес электронной почты. Однако, в этом случае, вы доверяете службе псевдонимов продолжать функционировать.

Использование специализированной службы псевдонимов электронной почты также имеет ряд преимуществ по сравнению с универсальным псевдонимом на пользовательском домене:

- Псевдонимы можно включать и выключать по отдельности, когда это необходимо, что предотвращает случайную рассылку электронной почты веб-сайтами.
- Ответы отправляются с псевдонимного адреса, скрывая ваш настоящий адрес электронной почты.

Они также имеют ряд преимуществ по сравнению с услугами "временной электронной почты":

- Псевдонимы являются постоянными и могут быть включены снова, если вам нужно получить что-то вроде сброса пароля.
- Письма отправляются на ваш доверенный почтовый ящик, а не хранятся у поставщика псевдонимов.
- Временные почтовые службы обычно имеют публичные почтовые ящики, доступ к которым может получить любой, кто знает адрес, псевдонимы же доступны только вам.

Наши рекомендованные поставщики псевдонимов электронной почты позволяют вам создавать псевдонимы на доменах, которые они контролируют, а также на ваших собственных доменах за умеренную годовую плату. Вы так же можете разместить их на своем сервере, если вы хотите получить максимальный контроль. Однако использование пользовательского домена может иметь недостатки, связанные с конфиденциальностью: если вы единственный человек, использующий пользовательский домен, ваши действия можно легко отследить на всех сайтах, просто посмотрев на доменное имя в адресе электронной почты и проигнорировав все, что находится перед знаком "эт" (@).

Отправка/получение незашифрованных писем через службу псевдонимов требует доверия как к вашему почтовому провайдеру, так и к провайдеру псевдонимов. Некоторые провайдеры смягчают эту проблему с помощью автоматического шифрования PGP, которое уменьшает требующих доверия сторон, с двух до одной, шифруя входящие электронные письма до их доставки к вашему конечному почтовому провайдеру.

### AnonAddy

!!! recommendation

    ![Логотип AnonAddy](assets/img/email/anonaddy.svg#only-light){ align=right }
    ![Логотип AnonAddy](assets/img/email/anonaddy-dark.svg#only-dark){ align=right }
    
    **AnonAddy** позволяет вам бесплатно создать 20 доменных псевдонимов на общем домене или неограниченное количество "стандартных" псевдонимов, которые менее анонимны.
    
    [:octicons-home-16: Домашняя страница](https://anonaddy.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://anonaddy.com/privacy/){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://app.anonaddy.com/docs/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://anonaddy.com/donate/){ .card-link title=Поддержать }
    
    ??? скачать
    
        - [:simple-android: Android](https://anonaddy.com/faq/#is-there-an-android-app)
        - [:material-apple-ios: iOS](https://anonaddy.com/faq/#is-there-an-ios-app)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/en-GB/firefox/addon/anonaddy/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/anonaddy-anonymous-email/iadbdpnoknmbdeolbapdackdcogdmjpe)

Доступное вам количество общих псевдонимов (которые заканчиваются на общий домен, например @anonaddy.me), ограничено 20 на бесплатном плане AnonAddy и 50 на их плане за $12/год. Вы можете создавать неограниченное количество стандартных псевдонимов (которые заканчиваются на домен типа @[username].anonaddy.com или пользовательский домен в платных тарифных планах), однако, как уже говорилось ранее, это может нанести ущерб конфиденциальности, поскольку люди могут банально связать ваши стандартные псевдонимы вместе на основе одного только доменного имени. Неограниченное количество общих псевдонимов доступно за $36/год.

Примечательные бесплатные функции:

- [x] 20 общих псевдонимов
- [x] Неограниченное количество стандартных псевдонимов
- [ ] Нет исходящих ответов
- [x] 2 почтовых ящика получателя
- [x] Автоматическое шифрование PGP

### SimpleLogin

!!! recommendation

    ![Логотип Simplelogin](assets/img/email/simplelogin.svg){ align=right }
    
    **SimpleLogin** - это бесплатный сервис, который предоставляет псевдонимы электронной почты на различных общих доменных именах, и опционально платные возможности, такие как неограниченное количество псевдонимов и пользовательские домены.
    
    [:octicons-home-16: Домашняя страница](https://simplelogin.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://simplelogin.io/privacy/){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://simplelogin.io/docs/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/simple-login){ .card-link title="Исходный код" }
    
    ??? скачать
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
        - [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/en-US/firefox/addon/simplelogin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
        - [:simple-safari: Safari](https://apps.apple.com/app/id1494051017)

SimpleLogin was [acquired by Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) as of April 8, 2022. If you use Proton Mail for your primary mailbox, SimpleLogin is a great choice. As both products are now owned by the same company you now only have to trust a single entity. We also expect that SimpleLogin will be more tightly integrated with Proton's offerings in the future. SimpleLogin continues to support forwarding to any email provider of your choosing. Securitum [audited](https://simplelogin.io/blog/security-audit/) SimpleLogin in early 2022 and all issues [were addressed](https://simplelogin.io/audit2022/web.pdf).

You can link your SimpleLogin account in the settings with your Proton account. If you have the Proton Unlimited, Business, or Visionary Plan, you will have SimpleLogin Premium for free.

Notable free features:

- [x] 10 Shared Aliases
- [x] Unlimited Replies
- [x] 1 Recipient Mailbox

## Self-Hosting Email

Advanced system administrators may consider setting up their own email server. Mail servers require attention and continuous maintenance in order to keep things secure and mail delivery reliable.

### Combined software solutions

!!! recommendation

    ![Mailcow logo](assets/img/email/mailcow.svg){ align=right }
    
    **Mailcow** is a more advanced mail server perfect for those with a bit more Linux experience. It has everything you need in a Docker container: A mail server with DKIM support, antivirus and spam monitoring, webmail and ActiveSync with SOGo, and web-based administration with 2FA support.
    
    [:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailcow.github.io/mailcow-dockerized-docs/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

!!! recommendation

    ![Mail-in-a-Box logo](assets/img/email/mail-in-a-box.svg){ align=right }
    
    **Mail-in-a-Box** is an automated setup script for deploying a mail server on Ubuntu. Its goal is to make it easier for people to set up their own mail server.
    
    [:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }

For a more manual approach we've picked out these two articles:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd/) (2019)
- [How To Run Your Own Mail Server](https://www.c0ffee.net/blog/mail-server-guide/) (August 2017)

## Критерии

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any Email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an Email provider, and conduct your own research to ensure the Email provider you choose is the right choice for you.

### Technology

We regard these features as important in order to provide a safe and optimal service. You should consider whether the provider which has the features you require.

**Minimum to Qualify:**

- Encrypts email account data at rest with zero-access encryption.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322/) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Custom domain names are important to users because it allows them to maintain their agency from the service, should it turn bad or be acquired by another company which doesn't prioritize privacy.
- Operates on owned infrastructure, i.e. not built upon third-party email service providers.

**Best Case:**

- Encrypts all account data (Contacts, Calendars, etc.) at rest with zero-access encryption.
- Integrated webmail E2EE/PGP encryption provided as a convenience.
- Support for [WKD](https://wiki.gnupg.org/WKD) to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key by typing: `gpg --locate-key example_user@example.com`
- Support for a temporary mailbox for external users. This is useful when you want to send an encrypted email, without sending an actual copy to your recipient. These emails usually have a limited lifespan and then are automatically deleted. They also don't require the recipient to configure any cryptography like OpenPGP.
- Availability of the email provider's services via an [onion service](https://en.wikipedia.org/wiki/.onion).
- [Subaddressing](https://en.wikipedia.org/wiki/Email_address#Subaddressing) support.
- Catch-all or alias functionality for those who own their own domains.
- Use of standard email access protocols such as IMAP, SMTP or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.

### Конфиденциальность

We prefer our recommended providers to collect as little data as possible.

**Minimum to Qualify:**

- Protect sender's IP address. Filter it from showing in the `Received` header field.
- Don't require personally identifiable information (PII) besides a username and a password.
- Privacy policy that meets the requirements defined by the GDPR
- Must not be hosted in the US due to [ECPA](https://en.wikipedia.org/wiki/Electronic_Communications_Privacy_Act#Criticism) which has [yet to be reformed](https://epic.org/ecpa/).

**Best Case:**

- Accepts [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)

### Безопасность

Email servers deal with a lot of very sensitive data. We expect that providers will adopt best industry practices in order to protect their members.

**Minimum to Qualify:**

- Protection of webmail with 2FA, such as TOTP.
- Zero access encryption, builds on encryption at rest. The provider does not have the decryption keys to the data they hold. This prevents a rogue employee leaking data they have access to or remote adversary from releasing data they have stolen by gaining unauthorized access to the server.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) support.
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://www.hardenize.com/), [testssl.sh](https://testssl.sh/), or [Qualys SSL Labs](https://www.ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLSv1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- A valid [MTA-STS](https://tools.ietf.org/html/rfc8461) and [TLS-RPT](https://tools.ietf.org/html/rfc8460) policy.
- Valid [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) records.
- Valid [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) and [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) records.
- Have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. If DMARC authentication is being used, the policy must be set to `reject` or `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996/).
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) submission, assuming SMTP is used.
- Website security standards such as:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subresource Integrity](https://en.wikipedia.org/wiki/Subresource_Integrity) if loading things from external domains.
- Must support viewing of [Message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**Best Case:**

- Support for hardware authentication, i.e. U2F and [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn). U2F and WebAuthn are more secure as they use a private key stored on a client-side hardware device to authenticate people, as opposed to a shared secret that is stored on the web server and on the client side when using TOTP. Furthermore, U2F and WebAuthn are more resistant to phishing as their authentication response is based on the authenticated [domain name](https://en.wikipedia.org/wiki/Domain_name).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in addition to DANE support.
- Implementation of [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), this is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Bug-bounty programs and/or a coordinated vulnerability-disclosure process.
- Website security standards such as:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163/)

### Доверие

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? We require our recommended providers to be public about their ownership or leadership. We also would like to see frequent transparency reports, especially in regard to how government requests are handled.

**Minimum to Qualify:**

- Public-facing leadership or ownership.

**Best Case:**

- Public-facing leadership.
- Frequent transparency reports.

### Маркетинг

With the email providers we recommend we like to see responsible marketing.

**Minimum to Qualify:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.). The provider's site must also comply with [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) for those who wish to opt-out.

Must not have any marketing which is irresponsible:

- Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
- Making guarantees of protecting anonymity 100%. When someone makes a claim that something is 100% it means there is no certainty for failure. We know people can quite easily deanonymize themselves in a number of ways, e.g.:

- Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
- [Browser fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Best Case:**

- Clear and easy to read documentation. This includes things like, setting up 2FA, email clients, OpenPGP, etc.

### Дополнительная функциональность

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
