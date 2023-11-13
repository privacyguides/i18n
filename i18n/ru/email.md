---
meta_title: "Рекомендации по шифрованной конфиденциальной электронной почте - Privacy Guides"
title: "Электронная почта"
icon: material/email
description: Эти провайдеры электронной почты предлагают отличное место для безопасного хранения ваших писем. Многие из них предлагают еще и совместимое с другими провайдерами шифрование OpenPGP.
cover: email.webp
---

Электронная почта практически всегда необходима для использования любого онлайн-сервиса, однако мы не рекомендуем использовать её для общения с людьми. Вместо того, чтобы использовать электронную почту для связи с другими людьми, мы советуем использовать мессенджеры, которые поддерживают прямую секретность.

[Рекомендуемые мессенджеры](real-time-communication.md ""){.md-button}

Для всего остального мы рекомендуем различных провайдеров электронной почты, которые базируются на устойчивых бизнес-моделях и встроенных функциях безопасности и конфиденциальности.

- [Провайдеры электронной почты, поддерживающие OpenPGP :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [Другие провайдеры, поддерживающие шифрование :material-arrow-right-drop-circle:](#more-providers)
- [Сервисы псевдонимов электронной почты :material-arrow-right-drop-circle:](#email-aliasing-services)
- [Варианты самостоятельного хостинга :material-arrow-right-drop-circle:](#self-hosting-email)

## Сервисы, поддерживающие OpenPGP

Эти провайдеры нативно поддерживают шифрование/дешифрование с помощью OpenPGP и стандарт [Web Key Directory](basics/email-security.md#what-is-the-web-key-directory-standard), что позволяет использовать E2EE, не зависимо от провайдера. Например, пользователь Proton Mail может отправлять E2EE-зашифрованное сообщение пользователю Mailbox.org, или ты можешь получить OpenPGP-зашифрованное уведомление от интернет-сервисов, поддерживающих такую функцию.

<div class="grid cards" markdown>

- ![Логотип Proton Mail](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Логотип Mailbox.org](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

!!! warning "Осторожно"

    При использовании технологии E2EE, такой, как OpenPGP, сообщения все равно будут содержать некоторые незашифрованные метаданные в заголовках письма. Узнай больше о [метаданных электронной почты](basics/email-security.md#email-metadata-overview).
    
    OpenPGP также не поддерживает прямую секретность: если твой закрытый ключ или закрытый ключ получателя будет украден, то все предыдущие сообщения, зашифрованные с его помощью, будут раскрыты. [Как я могу защитить свои закрытые ключи?](basics/email-security.md#how-do-i-protect-my-private-keys)

### Proton Mail

!!! recommendation

    ![Логотип Proton Mail](assets/img/email/protonmail.svg){ align=right }
    
    **Proton Mail** — это сервис электронной почты, фокусирующийся на приватности, шифровании, безопасности и простоте использования. Они работают с **2013** года. Компания Proton AG базируется в Женеве, Швейцария. Аккаунты получают от 500 МБ хранилища на бесплатном тарифе.
    
    [:octicons-home-16: Домашняя страница](https://proton.me/mail){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion-сервис" }
    [:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Исходный код" }
    
    ??? downloads "Скачать"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id979659905)
        - [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
        - [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
        - [:simple-apple: macOS](https://proton.me/mail/bridge#download)
        - [:simple-linux: Linux](https://proton.me/mail/bridge#download)
        - [:octicons-browser-16: Web](https://mail.proton.me)

Бесплатные аккаунты имеют некоторые ограничения, такие как невозможность поиска писем по седержимому и отсутствие доступа к [Proton Mail Bridge](https://proton.me/mail/bridge), который необходим для использования [рекомендуемого настольного почтового клиента](email-clients.md) (например, Thunderbird). Платные аккаунты включают такие функции, как Proton Mail Bridge, дополнительное хранилище и поддержку пользовательских доменов. [Аттестационное письмо](https://proton.me/blog/security-audit-all-proton-apps) было предоставлено для приложений Proton Mail 9 ноября 2021 года компанией [Securitum](https://research.securitum.com).

Если у тебя есть план Proton Unlimited, Business или Visionary, то ты также получаешь [SimpleLogin](#simplelogin) Premium бесплатно.

У компании Proton Mail есть внутренние отчеты об ошибках, которые они **не передают** третьим лицам. Это можно отключить в: **Настройки** > **Перейти в Настройки** > **Учетная запись** > **Безопасность и конфиденциальность** > **Отправка отчетов об ошибках**.

#### :material-check:{ .pg-green } Пользовательские домены и псевдонимы

Платные подписчики Proton Mail могут использовать свой собственный домен или [универсальный адрес](https://proton.me/support/catch-all). Proton Mail также поддерживает [субадресацию](https://proton.me/support/creating-aliases), что полезно для тех, кто не хочет покупать домен.

#### :material-check:{ .pg-green } Конфиденциальные способы оплаты

Proton Mail [принимает](https://proton.me/support/payment-options) наличные по почте в дополнение к стандартным платежам кредитными/дебетовыми картами, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), и PayPal.

#### :material-check:{ .pg-green } Безопасность аккаунта

Proton Mail поддерживает [двухфакторную аутентификацию](https://proton.me/support/two-factor-authentication-2fa) TOTP и [аппаратные ключи безопасности](https://proton.me/support/2fa-security-key) с использованием стандартов FIDO2 или U2F. Использование аппаратного ключа безопасности сначала требует настройки двухфакторной аутентификации TOTP.

#### :material-check:{ .pg-green } Безопасность данных

Proton Mail использует [шифрование с нулевым доступом](https://proton.me/blog/zero-access-encryption) в состоянии покоя для твоих писем и [календарей](https://proton.me/news/protoncalendar-security-model). Данные, защищенные с помощью шифрования с нулевым доступом, доступны только тебе.

Определенная информация, хранящаяся в [Proton Contacts](https://proton.me/support/proton-contacts), такая, как имена пользователей и адреса электронной почты, не защищена шифрованием с нулевым доступом. Поля контактов, поддерживающие шифрование с нулевым доступом, например номера телефонов, обозначаются значком замка.

#### :material-check:{ .pg-green } Шифрование электронной почты

Proton Mail [интегрировал шифрование OpenPGP](https://proton.me/support/how-to-use-pgp) в свою веб-почту. Письма, отправленные на другие аккаунты Proton Mail шифруются автоматически. Шифрование писем с помощью ключа OpenPGP на адреса, не принадлежащие Proton Mail, можно легко включить в настройках аккаунта. Они также позволяют тебе [шифровать сообщения на адреса, не относящиеся к Proton Mail](https://proton.me/support/password-protected-emails), без необходимости регистрировать учетную запись Proton Mail или использовать программное обеспечение типа OpenPGP.

Proton Mail также поддерживает обнаружение открытых ключей через HTTP с их [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Это позволяет людям, не использующим Proton Mail, легко находить OpenPGP-ключи учетных записей Proton Mail для кросс-провайдерского E2EE. Это относится только к адресам электронной почты, заканчивающимся на один из собственных доменов "Протона", например @proton.me. При использовании кастомного домена необходимо [настроить WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) отдельно.

#### :material-information-outline:{ .pg-blue } Блокировка аккаунта

Если у тебя платный аккаунт, и твой [счёт не оплачен](https://proton.me/support/delinquency) в течение 14 дней, то ты не сможешь получить доступ к своим данным. Через 30 дней твой аккаунт станет просроченным и не будет получать входящую почту. В течение этого периода тебе будет по-прежнему выставляться счет.

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

Proton Mail предлагает "Proton Unlimited" аккаунт за €9,99/месяц, который также позволяет получить доступ к Proton VPN в дополнение к предоставлению нескольких аккаунтов, доменов, псевдонимов и 500 ГБ хранилища.

Proton Mail не предлагает функцию цифрового наследия.

### Mailbox.org

!!! recommendation

    ![Логотип Mailbox.org](assets/img/email/mailboxorg.svg){ align=right }
    
    **Mailbox.org** - это сервис электронной почты, ориентированный на безопасность, отсутствие рекламы и приватное электроснабжение от 100% экологически чистой энергии. Они работают с 2014 года. Mailbox.org базируется в Берлине, Германия. Учетные записи начинаются с 2 ГБ дискового пространства, которое может быть увеличено по мере необходимости.
    
    [:octicons-home-16: Домашняя страница](https://mailbox.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Политика конфеденциальности" }
    [:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Документация}
    
    ??? downloads "скачать"
    
        - [:octicons-browser-16: Сайт](https://login.mailbox.org)

#### :material-check:{ .pg-green } Пользовательские домены и псевдонимы

Mailbox.org позволяет тебе использовать собственный домен, и поддерживает [универсальные](https://kb.mailbox.org/display/MBOKBEN/Using+catch-all+alias+with+own+domain) адреса. Mailbox.org также поддерживает [субадресацию](https://kb.mailbox.org/display/BMBOKBEN/What+is+an+alias+and+how+do+I+use+it), что полезно для тех, кто не хочет покупать домен.

#### :material-check:{ .pg-green } Конфиденциальные способы оплаты

Mailbox.org не принимает криптовалюты в связи с тем, что их платежная система BitPay приостановила работу в Германии. Однако, они принимают наличные по почте, оплату наличными на банковский счет, банковский перевод, кредитные карты, PayPal и несколько немецких платёжных систем: paydirekt и Sofortüberweisung.

#### :material-check:{ .pg-green } Безопасность аккаунта

Mailbox.org поддерживает [двухфакторную аутентификацию](https://kb.mailbox.org/display/MBOKBEN/How+to+use+two-factor+authentication+-+2FA) только для своей веб-почты. Ты можешь использовать либо TOTP, либо [YubiKey](https://en.wikipedia.org/wiki/YubiKey) с помощью [YubiCloud](https://www.yubico.com/products/services-software/yubicloud). Веб-стандарты, такие, как [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn), пока не поддерживаются.

#### :material-information-outline:{ .pg-blue } Безопасность данных

Mailbox.org позволяет шифровать входящую почту с помощью своего [зашифрованного почтового ящика](https://kb.mailbox.org/display/MBOKBEN/The+Encrypted+Mailbox). Новые сообщения, которые ты получаешь, будут немедленно зашифрованы твоим открытым ключом.

Однако [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), программная платформа, используемая Mailbox.org, [не поддерживает](https://kb.mailbox.org/display/BMBOKBEN/Encryption+of+calendar+and+address+book) шифрование твоей адресной книги и календаря. [Отдельное решение](calendar.md) может больше подойти для этой информации.

#### :material-check:{ .pg-green } Шифрование электронной почты

Mailbox.org использует [встроенное шифрование](https://kb.mailbox.org/display/MBOKBEN/Send+encrypted+e-mails+with+Guard) в свою веб-почту, что упрощает отправку сообщений людям с открытыми ключами OpenPGP. Они также позволяют [пользователям без Mailbox.org расшифровывать электронные письма](https://kb.mailbox.org/display/MBOKBEN/My+recipient+does+not+use+PGP) на серверах Mailbox.org. Эта функция полезна, когда получатель не имеет OpenPGP и не может расшифровать копию письма в собственном почтовом ящике.

Mailbox.org также поддерживает обнаружение открытых ключей через HTTP с их [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Это позволяет людям, не использующим Mailbox.org, легко находить OpenPGP-ключи учетных записей Mailbox.org для кросс-провайдерского E2EE. Это относится только к адресам электронной почты, заканчивающимся на один из собственных доменов "Mailbox.org", например @mailbox.org. При использовании кастомного домена необходимо [настроить WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) отдельно.

#### :material-information-outline:{ .pg-blue } Блокировка аккаунта

По окончании срока действия подписки твоя учетная запись будет переведена в ограниченный режим. По истечении [30 дней она будет безвозвратно удалена](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

Ты можешь получить доступ к своему аккаунту Mailbox.org через IMAP/SMTP, используя их сервис [.onion](https://kb.mailbox.org/display/MBOKBEN/The+Tor+exit+node+of+mailbox.org). Однако доступ к интерфейсу веб-почты через службу .onion невозможен, и ты можешь столкнуться с ошибками сертификата TLS.

Все учетные записи имеют ограниченное облачное хранилище, которое [может быть зашифровано](https://kb.mailbox.org/display/MBOKBEN/Encrypt+files+on+your+Drive). Mailbox.org также предлагает псевдоним [@secure.mailbox.org](https://kb.mailbox.org/display/MBOKBEN/Ensuring+E-Mails+are+Sent+Securely), который требует шифрование TLS от соединения между почтовыми серверами, в противном случае сообщение вообще не будет отправлено. Mailbox.org также поддерживает [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) в дополнение к стандартным протоколам доступа, таким как IMAP и POP3.

Mailbox.org имеет функцию цифрового наследия для всех тарифных планов. Ты можешь выбрать, хочешь ли ты, чтобы какие-либо из твоих данных были переданы твоим наследникам, при условии, что они подадут заявление и предоставят твоё завещание. Кроме того, ты можешь назначить наследника по имени и адресу.

## Дополнительные провайдеры

Эти провайдеры хранят твою электронную почту с помощью шифрования с нулевым знанием, что делает их отличными вариантами для безопасного хранения твоей электронной почты. Однако они не поддерживают совместимые между различными провайдерами стандарты шифрования для E2EE коммуникаций.

<div class="grid cards" markdown>

- ![Skiff Mail logo](assets/img/email/skiff-mail.svg){ .twemoji } [Skiff Mail](email.md#skiff-mail)
- ![Tuta logo](assets/img/email/tuta.svg){ .twemoji } [Tuta](email.md#tuta)

</div>

### Skiff Mail

!!! recommendation

    ![Логотип Skiff Mail](assets/img/email/skiff-mail.svg){ align=right }
    
    **Skiff Mail** - это веб-сервис электронной почты с поддержкой E2EE, который основан в 2020 году, базируется в Сан-Франциско и разрабатывается людьми со всего мира. Аккаунты начинаются с 10 ГБ бесплатного хранилища.
    
    [:octicons-home-16: Домашняя страница](https://skiff.com/mail){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://app.skiff.com/docs/db93c237-84c2-4b2b-9588-19a7cd2cd45a#tyGksN9rkqbo2uGYASxsA6HVLjUoly/wTYK8tncTto8=){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://skiff.com/help){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/skiff-org/skiff-apps){ .card-link title="Исходный код" }
    
    ??? downloads "Скачать"
    
        - [:simple-android: Android](https://play.google.com/store/apps/details?id=com.skemailmobileapp&pli=1)
        - [:simple-appstore: iOS](https://apps.apple.com/us/app/skiff-mail/id1619168801)
        - [:octicons-browser-16: Web](https://app.skiff.com/mail)

Skiff прошел несколько [аудитов](https://skiff.com/transparency) во время разработки.

#### :material-check:{ .pg-green } Пользовательские домены и псевдонимы

С бесплатным тарифным планом вам доступно до 3 дополнительных псевдонимов электронной почты (с доменом @skiff.com) в дополнении к вашему главному почтовому адресу. В бесплатных учетных записях можно добавить 1 [пользовательский домен](https://skiff.com/blog/custom-domain-setup), а в платных - до 15 пользовательских доменов. С пользовательским доменом вы можете создать неограниченное количество псевдонимов или [универсальный псевдоним](https://skiff.com/blog/catch-all-email-alias).

#### :material-alert-outline:{ .pg-orange } Конфиденциальные способы оплаты

Skiff Mail принимает криптовалютные платежи с помощью Coinbase Commerce, включая Bitcoin и Ethereum, но они не принимают рекомендуемую нами [криптовалюту](cryptocurrency.md) Monero. Они также принимают платежи по кредитным картам с помощью Stripe.

#### :material-check:{ .pg-green } Безопасность аккаунта

Skiff Mail поддерживает двухфакторную аутентификацию TOTP и аппаратные ключи безопасности с использованием стандартов FIDO2 или U2F. Использование аппаратного ключа безопасности сначала требует настройки двухфакторной аутентификации TOTP.

#### :material-check:{ .pg-green } Безопасность данных

Skiff Mail предоставляет шифрование с нулевым доступом в состоянии покоя для всех ваших данных. Это означает, что сообщения и другие данные, хранящиеся на твоём аккаунте, доступны для чтения только тебе.

#### :material-information-outline:{ .pg-blue } Шифрование электронной почты

Skiff Mail не использует OpenPGP. С помощью E2EE шифруются только сообщения, отправленные другим пользователям Skiff Mail. В Skiff нет функций "временный ящик" или "письмо с паролем", как у некоторых других провайдеров, поэтому внешние пользователи не могут получать и отвечать на сообщения с помощью E2EE.

#### :material-information-outline:{ .pg-blue } Блокировка аккаунта

Срок действия аккаунтов Skiff Mail не истекает, однако неоплаченным учетным записям будет предложено удалить все включенные платные функции (например, дополнительные псевдонимы) или продлить тарифный план, прежде чем учетной записью снова можно будет пользоваться.

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

Skiff дополнительно предлагает [функции повышения производительности рабочего пространства](https://discuss.privacyguides.net/t/skiff-pages-drive-productivity-tools/11758/13), но на данный момент мы предпочитаем [альтернативные](productivity.md) варианты совместной работы и обмена файлами.

Skiff Mail не предлагает функцию цифрового наследия.

### Tuta

!!! recommendation

    ![Tuta logo](assets/img/email/tuta.svg){ align=right }
    
    **Tuta** is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since **2011** and is based in Hanover, Germany. Бесплатные аккаунты начинаются с 1 ГБ хранилища.
    
    [:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://tuta.com/faq){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://tuta.com/community/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
        - [:simple-appstore: App Store](https://apps.apple.com/app/tutanota/id922429609)
        - [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
        - [:simple-windows11: Windows](https://tuta.com/#download)
        - [:simple-apple: macOS](https://tuta.com/#download)
        - [:simple-linux: Linux](https://tuta.com/#download)
        - [:octicons-browser-16: Web](https://app.tuta.com/)

Tuta doesn't support the [IMAP protocol](https://tuta.com/faq/#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/posts/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/howto#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } Пользовательские домены и псевдонимы

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/faq#custom-domain). Tuta doesn't allow for [subaddressing (plus addresses)](https://tuta.com/faq#plus), but you can use a [catch-all](https://tuta.com/howto#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } Конфиденциальные способы оплаты

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/faq/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green } Безопасность аккаунта

Tuta supports [two factor authentication](https://tuta.com/faq#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Безопасность данных

Tuta has [zero access encryption at rest](https://tuta.com/faq#what-encrypted) for your emails, [address book contacts](https://tuta.com/faq#encrypted-address-book), and [calendars](https://tuta.com/faq#calendar). Это означает, что сообщения и другие данные, хранящиеся на твоём аккаунте, доступны для чтения только тебе.

#### :material-information-outline:{ .pg-blue } Шифрование электронной почты

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Блокировка аккаунта

Tuta will [delete inactive free accounts](https://tuta.com/faq#inactive-accounts) after six months. Ты можешь повторно использовать деактивированный бесплатный аккаунт, если заплатишь.

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/posts/secure-email-for-non-profit) for free or with a heavy discount.

Tuta also has a business feature called [Secure Connect](https://tuta.com/secure-connect/). Это гарантирует, что контакт клиента с бизнесом использует E2EE. Стоимость функции составляет €240/год.

Tuta doesn't offer a digital legacy feature.

## Сервисы псевдонимов электронной почты

Служба псевдонимов электронной почты позволяет легко генерировать новый адрес электронной почты для каждого сайта, на котором ты зарегистрирован. Созданные тобой псевдонимы электронной почты затем пересылают почту на выбранный тобой адрес электронной почты, скрывая как твой "основной" адрес электронной почты, так и название твоего провайдера электронной почты. Истинная адресация электронной почты лучше, чем плюсовая адресация, обычно используемая и поддерживаемая многими провайдерами, которая позволяет создавать псевдонимы типа ваше_имя+[что-то_ещё]@example.com, поскольку веб-сайты, рекламодатели и сети отслеживания могут просто удалить всё, что идет после знака +, чтобы узнать твой настоящий адрес электронной почты.

<div class="grid cards" markdown>

- ![Логотип addy.io](assets/img/email/mini/addy.svg){ .twemoji } [addy.io](email.md#addyio)
- ![Логотип SimpleLogin](assets/img/email/simplelogin.svg){ .twemoji } [SimpleLogin](email.md#simplelogin)

</div>

Псевдоним электронной почты может служить защитой на случай, если твой поставщик услуг электронной почты прекратит свою работу. В этом случае ты можешь легко перенаправить свои псевдонимы на новый адрес электронной почты. Однако, в этом случае, ты доверяешь службе псевдонимов продолжать функционировать.

Использование специализированной службы псевдонимов электронной почты также имеет ряд преимуществ по сравнению с универсальным псевдонимом на пользовательском домене:

- Псевдонимы можно включать и выключать по отдельности, когда это необходимо, что предотвращает случайную рассылку электронной почты веб-сайтами.
- Ответы отправляются с псевдонимного адреса, скрывая твой настоящий адрес электронной почты.

Они также имеют ряд преимуществ по сравнению с услугами "временной электронной почты":

- Псевдонимы являются постоянными и могут быть включены снова, если тебе нужно получить что-то вроде сброса пароля.
- Письма отправляются на ваш доверенный почтовый ящик, а не хранятся у поставщика псевдонимов.
- Временные почтовые службы обычно имеют публичные почтовые ящики, доступ к которым может получить любой, кто знает адрес, псевдонимы же доступны только тебе.

Наши рекомендованные провайдеры псевдонимов электронной почты позволяют тебе создавать псевдонимы на доменах, которые они контролируют, а также на твоих собственных доменах за умеренную годовую плату. Ты так же можешь разместить их на своем сервере, если ты хочешь получить максимальный контроль. Однако использование пользовательского домена может иметь недостатки, связанные с конфиденциальностью: если ты единственный человек, использующий пользовательский домен, твои действия можно легко отследить на всех сайтах, просто посмотрев на доменное имя в адресе электронной почты и проигнорировав всё, что находится перед знаком "эт" (@).

Отправка/получение незашифрованных писем через службу псевдонимов требует доверия как к твоему почтовому провайдеру, так и к провайдеру псевдонимов. Некоторые провайдеры смягчают эту проблему с помощью автоматического шифрования PGP, которое уменьшает требующих доверия сторон с двух до одной, шифруя входящие электронные письма до их доставки к твоему конечному почтовому провайдеру.

### addy.io

!!! recommendation

    ![Логотип addy.io](assets/img/email/addy.svg#only-light){ align=right }
    ![Логотип addy.io](assets/img/email/addy-dark.svg#only-dark){ align=right }
    
    **addy.io** позволяет вам создать 10 псевдонимов на общем домене или неограниченное количество "стандартных" псевдонимов, которые менее анонимны.
    
    [:octicons-home-16: Домашняя страница](https://addy.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://app.addy.io/docs){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://addy.io/donate){ .card-link title=Поддержать }
    
    ??? downloads "Скачать"
    
        - [:simple-android: Android](https://addy.io/faq/#is-there-an-android-app)
        - [:material-apple-ios: iOS](https://addy.io/faq/#is-there-an-ios-app)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/addy_io/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/addyio-anonymous-email-fo/iadbdpnoknmbdeolbapdackdcogdmjpe)

Количество общих псевдонимов (заканчивающихся на общий домен, например @addy.io), которые вы можете создать, ограничено 10 на бесплатном плане addy.io, 50 на плане стоимостью 1 доллар в месяц и неограниченно на плане стоимостью 4 доллара в месяц (счет выставляется на 3 доллара в течение года). Ты можешь создавать неограниченное количество стандартных псевдонимов (которые заканчиваются на домен типа @[username].addy.io или пользовательский домен в платных тарифных планах), однако, как уже говорилось ранее, это может нанести ущерб конфиденциальности, поскольку люди могут банально связать ваши стандартные псевдонимы вместе на основе общего доменного имени. Они полезны в тех случаях, когда общий домен может быть заблокирован какой-либо службой. Securitum [audited](https://addy.io/blog/addy-io-passes-independent-security-audit/) addy.io in September 2023 and no significant vulnerabilities [were identified](https://addy.io/addy-io-security-audit.pdf).

Примечательные бесплатные функции:

- [x] 10 общих псевдонимов
- [x] Неограниченное количество стандартных псевдонимов
- [ ] Нет исходящих ответов
- [x] 1 Почтовый ящик получателя
- [x] Автоматическое шифрование PGP

### SimpleLogin

!!! recommendation

    ![Логотип Simplelogin](assets/img/email/simplelogin.svg){ align=right }
    
    **SimpleLogin** - это бесплатный сервис, который предоставляет псевдонимы электронной почты на различных общих доменных именах, и опционально платные возможности, такие как неограниченное количество псевдонимов и пользовательские домены.
    
    [:octicons-home-16: Домашняя страница](https://simplelogin.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://simplelogin.io/privacy/){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://simplelogin.io/docs/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/simple-login){ .card-link title="Исходный код" }
    
    ??? downloads "Скачать"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
        - [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/simplelogin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
        - [:simple-safari: Safari](https://apps.apple.com/app/id1494051017)

SimpleLogin был [приобретен компанией Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) по состоянию на 8 апреля 2022 года. Если ты используешь Proton Mail в качестве основного почтового ящика, SimpleLogin - отличный выбор. Поскольку оба продукта теперь принадлежат одной компании, тебе нужно доверять только одной организации. Мы также ожидаем, что в будущем SimpleLogin будет более тесно интегрирован с приложениями Proton. SimpleLogin по-прежнему поддерживает пересылку на любого поставщика услуг электронной почты по твоему выбору. Securitum [провела аудит](https://simplelogin.io/blog/security-audit/) SimpleLogin в начале 2022 года, и все проблемы [были устранены](https://simplelogin.io/audit2022/web.pdf).

В настройках SompleLogin ты можешь связать свою учетную запись SimpleLogin с учетной записью Proton. Если у тебя есть план Proton Unlimited, Business или Visionary, то ты также получаешь SimpleLogin Premium бесплатно.

Примечательные бесплатные функции:

- [x] 10 общих псевдонимов
- [x] Неограниченные ответы
- [x] 1 Почтовый ящик получателя

## Электронная почта для самостоятельного хостинга

Продвинутые системные администраторы могут рассмотреть возможность создания собственного сервера электронной почты. Почтовые серверы требуют внимания и постоянного обслуживания, чтобы поддерживать безопасность и надежность доставки почты.

### Комбинированные программные решения

!!! recommendation

    ![Логотип Mailcow](assets/img/email/mailcow.svg){ align=right }
    
    **Mailcow** - это более продвинутый почтовый сервер, идеально подходящий для тех, у кого есть опыт работы с Linux. В его контейнере Docker есть всё, что тебе нужно: почтовый сервер с поддержкой DKIM, антивирус и мониторинг спама, веб-почта и ActiveSync с SOGo, а также веб-администрирование с поддержкой 2FA.
    
    [:octicons-home-16: Домашняя страница](https://mailcow.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailcow.github.io/mailcow-dockerized-docs/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://www.servercow.de/mailcow?lang=en#sal){ .card-link title=Поддержать }

!!! recommendation

    ![Логотип Mail-in-a-Box](assets/img/email/mail-in-a-box.svg){ align=right }
    
    **Mail-in-a-Box** - это скрипт автоматической настройки для запуска почтового сервера на Ubuntu. Его цель - облегчить людям создание собственного почтового сервера.
    
    [:octicons-home-16: Домашняя страница](https://mailinabox.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Исходный код" }

Для ручной настройки мы выбрали эти две статьи:

- [Настройка почтового сервера с OpenSMTPD, Dovecot и Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd/) (2019)
- [Как запустить собственный почтовый сервер](https://www.c0ffee.net/blog/mail-server-guide/) (август 2017)

## Критерии

**Обрати внимание, что мы не связаны ни с одним из рекомендуемых нами провайдеров.** Помимо [наших стандартных критериев](about/criteria.md), мы разработали четкий набор требований к любому провайдеру электронной почты, желающему быть рекомендованным, включая внедрение лучших отраслевых практик, современных технологий и многое другое. Мы рекомендуем тебе ознакомиться с этим списком, перед выбором провайдера электронной почты, и провести собственное исследование, чтобы убедиться, что выбранный тобой провайдер электронной почты подходит именно тебе.

### Технология

Мы считаем эти особенности важными для обеспечения безопасного и оптимального обслуживания. Ты должен проверить, обладает ли провайдер необходимыми тебе функциями.

**Минимальные требования:**

- Шифрует данные аккаунта электронной почты в состоянии покоя с помощью шифрования с нулевым доступом.
- Возможность экспорта в виде [Mbox](https://en.wikipedia.org/wiki/Mbox) или отдельных .eml со стандартом [RFC5322](https://datatracker.ietf.org/doc/rfc5322/) .
- Разрешает пользователям использовать собственное [доменное имя](https://en.wikipedia.org/wiki/Domain_name). Пользовательские доменные имена важны для пользователей, поскольку позволяют им сохранить свое агентство от сервиса, если он окажется плохим или будет приобретен другой компанией, которая не уделяет приоритетного внимания конфиденциальности.
- Работает на собственной инфраструктуре, т.е. не опирается на сторонних провайдеров электронной почты.

**В лучшем случае:**

- Шифрует все данные аккаунта (Контакты, Календари и т.д.) в состоянии покоя с помощью шифрования с нулевым доступом.
- Встроенное шифрование веб-почты E2EE/PGP обеспечивает удобство.
- Поддерживает [WKD](https://wiki.gnupg.org/WKD) для улучшения обнаружения открытых ключей OpenPGP через HTTP. Пользователи GnuPG могут получить ключ, набрав: `gpg --locate-key example_user@example.com`
- Поддержка временного почтового ящика для внешних пользователей. Это полезно, когда вы хотите отправить зашифрованное сообщение электронной почты, не отправляя фактическую копию получателю. Такие письма обычно имеют ограниченный срок действия, а затем автоматически удаляются. Они также не требуют от получателя настройки какой-либо криптографии, как OpenPGP.
- Доступность услуг провайдера электронной почты через [службу .onion](https://en.wikipedia.org/wiki/.onion).
- [Поддержка субадресации](https://en.wikipedia.org/wiki/Email_address#Subaddressing).
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
- Отсутствие ошибок или уязвимостей TLS при профилировании такими инструментами, как [Hardenize](https://www.hardenize.com/), [testssl.sh](https://testssl.sh/), или [Qualys SSL Labs](https://www.ssllabs.com/ssltest); сюда входят ошибки, связанные с сертификатами, и слабые параметры DH, например, те, которые привели к [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Настройки сервера (опционально для TLSv1.3) для сильных наборов шифров, которые поддерживают прямую секретность и аутентифицированное шифрование.
- Действующая политика [MTA-STS](https://tools.ietf.org/html/rfc8461) и [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Действительные записи [DANE](https://ru.wikipedia.org/wiki/DANE).
- Действительные записи [SPF](https://ru.wikipedia.org/wiki/Sender_Policy_Framework) и [DKIM](https://ru.wikipedia.org/wiki/DomainKeys_Identified_Mail).
- Имеет надлежащую политику и запись [DMARC](https://ru.wikipedia.org/wiki/DMARC) или использует [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) для аутентификации. Если используется DMARC-аутентификация, политика должна быть установлена на `reject` или `quarantine`.
- Предпочтение серверного пакета TLS 1.2 или более поздней версии и план [RFC8996](https://datatracker.ietf.org/doc/rfc8996/).
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
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163/)

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
