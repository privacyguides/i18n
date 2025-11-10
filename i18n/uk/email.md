---
meta_title: "Рекомендації щодо зашифрованої приватної електронної пошти"
title: Сервіси електронної пошти
icon: material/email
description: Ці сервіси електронної пошти пропонують чудове місце для безпечного зберігання ваших листів, а багато з них пропонують сумісне з іншими сервісами шифрування OpenPGP.
cover: email.webp
global:
  - 
    - випадковий елемент
    - "таблиця tbody"
---

<small>Захищає від наступних загроз:</small>

- [:material-server-network: Сервіси](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Електронна пошта це практично необхідність для користування будь-яким онлайн-сервісом, проте ми не рекомендуємо використовувати її для особистого спілкування. Замість того, щоб використовувати електронну пошту для зв'язку, розгляньте можливість використання засобів обміну миттєвими повідомленнями, які підтримують секретність.

[Рекомендовані месенджери](real-time-communication.md ""){.md-button}

## Рекомендовані сервіси

Для всього іншого ми рекомендуємо різноманітні поштові сервіси, що базуються на стійких бізнес-моделях і мають вбудовані функції безпеки та конфіденційності. Ознайомтеся з нашим [повним списком критеріїв](#criteria) для отримання додаткової інформації.

| Сервіс                        | OpenPGP / WKD                          | IMAP / SMTP                                                                 | Шифрування з нульовим доступом                          | Анонімні способи оплати                               |
| ----------------------------- | -------------------------------------- | --------------------------------------------------------------------------- | ------------------------------------------------------- | ----------------------------------------------------- |
| [Proton Mail](#proton-mail)   | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Тільки в платних тарифних планах | :material-check:{ .pg-green }                           | Cash <br>Monero via third party                 |
| [Mailbox Mail](#mailbox-mail) | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                                               | :material-information-outline:{ .pg-blue } Тільки пошта | Готівка                                               |
| [Tuta](#tuta)                 | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                                      | :material-check:{ .pg-green }                           | Monero via third party <br>Cash via third party |

На додаток до (або замість) рекомендованого тут сервісу електронної пошти, ви можете розглянути можливість використання спеціального [сервісу псевдонімів](email-aliasing.md#recommended-providers) для захисту вашої приватності. Серед іншого, ці сервіси можуть допомогти захистити вашу реальну поштову скриньку від спаму, не дати маркетологам зв'язати ваші акаунти, а також зашифрувати всі вхідні повідомлення за допомогою PGP.

- [Більше інформації :material-arrow-right-drop-circle:](email-aliasing.md)

## Сервіси, сумісні з OpenPGP

Ці сервіси одразу підтримують шифрування/дешифрування OpenPGP і [стандарт Web Key Directory (WKD)](basics/email-security.md#what-is-the-web-key-directory-standard), що дозволяє наскрізне шифрування електронних листів незалежно від сервісу. Наприклад, користувач Proton Mail може надіслати повідомлення E2EE користувачеві Mailbox Mail, або ви можете отримувати сповіщення, зашифровані за допомогою OpenPGP, від інтернет-сервісів, які його підтримують.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](#proton-mail)
- ![Mailbox Mail logo](assets/img/email/mailbox-mail.svg){ .twemoji } [Mailbox Mail](#mailbox-mail)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Попередження</p>

При використанні наскрізного шифрування (E2EE), такого як OpenPGP, ваш лист все одно буде містити деякі метадані, які не зашифровані в заголовку листа, в тому числі і рядок теми! Дізнайтеся більше про [метадані електронної пошти] (basics/email-security.md#email-metadata-overview).

OpenPGP також не підтримує пряму секретність, що означає, що якщо приватний ключ вас або одержувача повідомлення буде викрадено, всі попередні повідомлення, зашифровані за допомогою цього ключа, будуть відкриті.

- [Як захистити свої приватні ключі?] (basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Логотип Proton Mail](assets/img/email/protonmail.svg){align=right}

**Proton Mail — це поштовий сервіс з акцентом на конфіденційності, шифруванні, безпеці та простоті використання. Він працює з 2013 року. Компанія Proton AG базується в Женеві, Швейцарія.

План Proton Free надає 500 МБ поштового сховища, яке ви можете безплатно збільшити до 1 ГБ.

[:octicons-home-16: Домашня сторінка ](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/mail/privacy-policy){ .card-link title="Політика конфіденційності" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title="Документація" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Вихідний код" }

<details class="downloads" markdown>
<summary>Завантаження</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Free accounts have some limitations, such as not being able to search body text and not having access to [Proton Mail Bridge](https://proton.me/mail/bridge), which is required to use a [recommended desktop email client](email-clients.md) such as Thunderbird. Платні акаунти включають такі функції, як Proton Mail Bridge, додаткове сховище та підтримку власних доменів. The Proton Unlimited plan or any multi-user Proton plan includes access to [SimpleLogin](email-aliasing.md#simplelogin) Premium.

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

#### :material-check:{ .pg-green } Користувацькі домени та псевдоніми

Платні абоненти Proton Mail можуть використовувати власний домен з сервісом або [загальну](https://proton.me/support/catch-all) адресу. Proton Mail також підтримує [субадресацію](https://proton.me/support/creating-aliases), що корисно для людей, які не хочуть купувати домен.

#### :material-check:{ .pg-green } Приватні способи оплати

Proton Mail [приймає](https://proton.me/support/payment-options) **готівку** поштою на додаток до стандартних платежів кредитною/дебетовою карткою, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) та PayPal. Additionally, you can use [**Monero**](cryptocurrency.md#monero) to purchase vouchers for Proton Mail Plus or Proton Unlimited via their [official](https://discuss.privacyguides.net/t/add-monero-as-an-anonymous-payment-method-for-proton-services/31058/15) reseller [ProxyStore](https://dys2p.com/en/2025-09-09-proton.html).

#### :material-check:{ .pg-green } Безпека облікового запису

Proton Mail підтримує [двофакторну автентифікацію](https://proton.me/support/two-factor-authentication-2fa) TOTP та [апаратні ключі безпеки](https://proton.me/support/2fa-security-key) за стандартами FIDO2 або U2F. Використання апаратного ключа безпеки вимагає попереднього налаштування двофакторної автентифікації TOTP.

#### :material-check:{ .pg-green } Безпека даних

Proton Mail має [шифрування з нульовим доступом](https://proton.me/blog/zero-access-encryption) для ваших електронних листів та [календарів](https://proton.me/news/protoncalendar-security-model). Дані, захищені шифруванням з нульовим доступом, доступні лише вам.

Певна інформація, що зберігається в [Proton Contacts](https://proton.me/support/proton-contacts), наприклад, імена користувачів та адреси електронної пошти, не захищена шифруванням з нульовим доступом. Поля контактів, які підтримують шифрування з нульовим доступом, наприклад, номери телефонів, позначені значком замка.

#### :material-check:{ .pg-green } Шифрування електронної пошти

Proton Mail має [інтегроване OpenPGP шифрування](https://proton.me/support/how-to-use-pgp) у своїй електронній пошті. Електронні листи на інші акаунти Proton Mail шифруються автоматично, а шифрування на адреси, що не належать до Proton Mail, за допомогою ключа OpenPGP можна легко ввімкнути в налаштуваннях вашого акаунта. Proton також підтримує автоматичне виявлення зовнішніх ключів за допомогою WKD. Це означає, що електронні листи, надіслані іншим сервісам, які використовують WKD, також будуть автоматично зашифровані за допомогою OpenPGP, без необхідності вручну обмінюватися відкритими ключами PGP з вашими контактами. Сервіс також дозволяє [шифрувати повідомлення на адреси, що не належать до Proton Mail, без використання OpenPGP](https://proton.me/support/password-protected-emails), та без необхідності реєструвати обліковий запис Proton Mail.

Proton Mail також публікує відкриті ключі акаунтів Proton через HTTP з їхніх WKD. Це дозволяє людям, які не використовують Proton Mail, легко знайти ключі OpenPGP акаунтів Proton Mail для сервісів E2EE. Це стосується лише адрес електронної пошти, що закінчуються на один із власних доменів Proton, наприклад `@proton.me`. Якщо ви використовуєте власний домен, вам потрібно [налаштувати WKD](basics/email-security.md#what-is-the-web-key-directory-standard) окремо.

#### :material-information-outline:{ .pg-blue } Видалення облікового запису

Якщо у вас платний акаунт і ваш рахунок [не сплачений](https://proton.me/support/delinquency) протягом 14 днів, ви не зможете отримати доступ до своїх даних. Через 30 днів ваш акаунт стане простроченим і не буде отримувати вхідну пошту. Протягом цього періоду ви продовжуватимете отримувати рахунки. Proton [видаляє неактивні безплатні акаунти](https://proton.me/support/inactive-accounts) через один рік. Ви **не можете** повторно використовувати адресу електронної пошти деактивованого акаунта.

#### :material-information-outline:{ .pg-blue } Додатковий функціонал

[Безлімітний](https://proton.me/support/proton-plans#proton-unlimited) тарифний план Proton Mail також надає доступ до інших сервісів Proton на додаток до кількох власних доменів, необмежену кількість псевдонімів для приховування електронної пошти та 500 ГБ дискового простору.

### Mailbox Mail

<div class="admonition recommendation" markdown>

![Mailbox Mail logo](assets/img/email/mailbox-mail.svg){ align=right }

**Mailbox Mail** (formerly *Mailbox.org*) is an email service with a focus on being secure, ad-free, and powered by 100% eco-friendly energy. Він працює з 2014 року. Mailbox Mail базується в Берліні, Німеччина.

Облікові записи починаються з 2 ГБ пам'яті, яку можна збільшити за потреби.

[:octicons-home-16: Домашня сторінка ](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Політика конфіденційності" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="Документація" }

<details class="downloads" markdown>
<summary>Завантаження</summary>

- [:octicons-browser-16: Web] (https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Користувацькі домени та псевдоніми

Mailbox Mail дозволяє використовувати власний домен і підтримує [catch-al](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) адреси. Mailbox Mail також підтримує [субадресацію](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), що корисно, якщо ви не хочете купувати домен.

#### :material-check:{ .pg-green } Приватні способи оплати

Mailbox Mail не приймає жодних криптовалют, оскільки їхній платіжний процесор BitPay призупинив роботу в Німеччині. Однак вони приймають **готівку поштою**, **готівку на банківський рахунок**, банківські перекази, кредитні картки, PayPal і кілька німецьких платіжних систем: Paydirekt та Sofortüberweisung.

#### :material-check:{ .pg-green } Безпека облікового запису

Mailbox Mail підтримує [двофакторну автентифікацію](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) лише для своєї вебпошти. Ви можете використовувати TOTP або [YubiKey](security-keys.md#yubikey) через [YubiCloud](https://yubico.com/products/services-software/yubicloud). Вебстандарти, такі як [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), поки що не підтримуються.

#### :material-information-outline:{ .pg-blue } Безпека даних

Mailbox Mail дозволяє шифрувати вхідну пошту, використовуючи свою [зашифровану поштову скриньку](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Нові повідомлення, які ви отримуєте, будуть негайно зашифровані вашим публічним ключем.

Однак [Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange), програмна платформа, яку використовує Mailbox Mail, [не підтримує](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) шифрування вашої адресної книги та календаря. Для цих даних може бути більш доречною [окрема опція](calendar.md).

#### :material-check:{ .pg-green } Шифрування електронної пошти

Mailbox Mail [інтегрував шифрування](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) у свою вебпошту, що спрощує надсилання повідомлень людям з відкритими ключами OpenPGP. Сервіс також дозволяє [віддаленим одержувачам розшифровувати електронні](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) листи на серверах Mailbox. Ця функція корисна, коли віддалений одержувач не має OpenPGP і не може розшифрувати копію листа у власній поштовій скриньці.

Mailbox Mail також підтримує отримання відкритих ключів через HTTP з їх WKD. Це дозволяє людям за межами Mailbox Mail легко знаходити ключі OpenPGP облікових записів Mailbox Mail для інших сервісів E2EE. Це стосується лише адрес електронної пошти, які закінчуються на один із власних доменів Mailbox, наприклад `@mailbox.org`. Якщо ви використовуєте власний домен, вам потрібно [налаштувати WKD](basics/email-security.md#what-is-the-web-key-directory-standard) окремо.

#### :material-information-outline:{ .pg-blue } Видалення облікового запису

Після закінчення терміну дії контракту ваш обліковий запис буде переведено в режим обмеженого користувача. Він буде безповоротно видалений через [30 днів](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Додатковий функціонал

Ви можете отримати доступ до свого облікового запису Mailbox через IMAP/SMTP за допомогою їхнього [ сервісу .onion](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). Однак їхній інтерфейс вебпошти не може бути доступний через службу .onion, і у вас можуть виникати помилки TLS сертифіката.

Усі акаунти мають обмежений обсяг хмарного сховища, який [можна зашифрувати](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox Mail також пропонує псевдонім [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), який забезпечує шифрування TLS на з'єднанні між поштовими серверами, інакше повідомлення не буде надіслано взагалі. Mailbox Mail також підтримує [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) на додаток до стандартних протоколів доступу, таких як IMAP і POP3.

Mailbox Mail має функцію цифрової спадщини для всіх тарифних планів. Ви можете вибрати, чи хочете ви, щоб будь-які ваші дані були передані спадкоємцям, за умови, що вони подадуть заяву та нададуть ваш заповіт. Крім того, ви можете призначити особу, вказавши її ім'я та адресу.

## Інші сервіси

Ці сервіси зберігають ваші електронні листи за допомогою шифрування з нульовим рівнем доступу, що робить їх чудовими варіантами для захисту ваших збережених електронних листів. Однак вони не підтримують сумісні стандарти шифрування для комунікацій E2EE між різними сервісами.

<div class="grid cards" markdown>

- [Tuta logo](assets/img/email/tuta.svg#only-light){.twemoji loading=lazy}! [Tuta logo](assets/img/email/tuta-dark.svg#only-dark){.twemoji loading=lazy} [Tuta](#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){align=right}
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){align=right}

**Tuta** (раніше *Tutanota*) - це поштовий сервіс, що фокусується на безпеці та конфіденційності завдяки використанню шифрування. Tuta працює з 2011 року і базується в Ганновері, Німеччина.

Безплатні акаунти починаються з 1 ГБ сховища.

[:octicons-home-16: Домашня сторінка ](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Політика конфіденційності" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="Документація" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Вихідний код" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Завантаження</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:fontawesome-brands-windows: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta не підтримує [протокол IMAP](https://tuta.com/support#imap) або використання сторонніх [поштових клієнтів](email-clients.md), а також ви не зможете додавати [зовнішні](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) поштові скриньки до додатка Tuta. [Імпорт електронної пошти](https://github.com/tutao/tutanota/issues/630) наразі також не підтримується, але це має бути [змінено](https://tuta.com/blog/kickoff-import). Листи можна експортувати [як окремо, так і масовим вибором](https://tuta.com/support#generalMail) за текою, що може бути незручно, якщо у вас багато тек.

#### :material-check:{ .pg-green } Користувацькі домени та псевдоніми

Платні акаунти Tuta можуть використовувати 15 або 30 псевдонімів залежно від тарифного плану та необмежену кількість псевдонімів на [власних доменах](https://tuta.com/support#custom-domain). Tuta не підтримує [субадресацію (плюс адреси)](https://tuta.com/support#plus), але ви можете використовувати [загальну](https://tuta.com/support#settings-global) адресу з користувацьким доменом.

#### :material-information-outline:{ .pg-blue } Приватні способи оплати

Tuta only directly accepts credit cards and PayPal, however you can use [**cryptocurrency**](cryptocurrency.md) to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with ProxyStore.

#### :material-check:{ .pg-green } Безпека облікового запису

Tuta підтримує [двофакторну автентифікацію](https://tuta.com/support#2fa) за допомогою TOTP або U2F.

#### :material-check:{ .pg-green } Безпека даних

Tuta має [шифрування з нульовим доступом](https://tuta.com/support#what-encrypted) для ваших електронних листів, [контактів адресної книги](https://tuta.com/support#encrypted-address-book) та [календарів](https://tuta.com/support#calendar). Це означає, що повідомлення та інші дані, які зберігаються у вашому акаунті, можете читати тільки ви.

#### :material-information-outline:{ .pg-blue } Шифрування електронної пошти

Tuta [не використовує OpenPGP](https://tuta.com/support/#pgp). Акаунти Tuta можуть отримувати зашифровані листи від акаунтів, що не належать до Tuta, лише якщо вони надіслані через [тимчасову поштову скриньку Tuta](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Видалення облікового запису

Tuta [видаляє неактивні безплатні акаунти](https://tuta.com/support#inactive-accounts) через шість місяців. Ви можете повторно використовувати деактивований безплатний акаунт, якщо заплатите.

#### :material-information-outline:{ .pg-blue } Додатковий функціонал

Tuta пропонує бізнес-версію [неприбутковим організаціям](https://tuta.com/blog/secure-email-for-non-profit) безкоштовно або зі значною знижкою.

## Критерії

**Зверніть увагу, що ми не пов'язані з жодним із рекомендованих нами сервісів.** На додаток до [наших стандартних критеріїв](about/criteria.md), ми розробили чіткий набір вимог до будь-якого постачальника послуг електронної пошти, який може бути рекомендованим, включаючи впровадження найкращих практик, сучасних технологій тощо. Ми радимо вам ознайомитися з цим списком перед тим, як обирати постачальника послуг електронної пошти, і провести власне дослідження, щоб переконатися, що обраний вами сервіс є правильним вибором для вас.

### Технологія

Ми вважаємо ці функції важливими для надання безпечного та оптимального сервісу. Вам слід подумати, чи має він ті функції, які вам потрібні.

**Мінімальний функціонал:**

- Має шифрувати дані поштового акаунта за допомогою шифрування з нульовим доступом.
- Повинен мати можливість експортувати листи у форматі [Mbox](https://en.wikipedia.org/wiki/Mbox) або окремі файли .EML за стандартом [RFC5322](https://datatracker.ietf.org/doc/rfc5322).
- Дозволяти користувачам використовувати власне [доменне ім'я](https://en.wikipedia.org/wiki/Domain_name). Користувацькі доменні імена важливі для користувачів, оскільки вони дозволяють їм зберегти свою суб'єктність від сервісу, якщо він стане поганим або буде придбаний іншою компанією, для якої конфіденційність не є пріоритетом.
- Має працювати на власній інфраструктурі, тобто не на базі сторонніх постачальників послуг електронної пошти.

**Найкращі практики:**

- Шифрувати всі дані акаунта (контакти, календарі тощо) за допомогою шифрування з нульовим доступом.
- Забезпечувати інтегроване шифрування вебпошти E2EE/PGP для зручності.
- Має підтримувати WKD для покращення знаходження відкритих ключів OpenPGP через HTTP. Користувачі GnuPG можуть отримати ключ за допомогою цієї команди: `gpg --locate-key example_user@example.com`.
- Підтримувати тимчасову поштову скриньку для зовнішніх користувачів. Це корисно, коли ви хочете надіслати зашифрований електронний лист, не надсилаючи його копію одержувачу. Ці листи зазвичай мають обмежений термін зберігання, після чого автоматично видаляються. Вони також не вимагають від одержувача налаштування криптографії, як OpenPGP.
- Має підтримувати [субадресацію](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Дозволяти користувачам використовувати власне [доменне ім'я](https://en.wikipedia.org/wiki/Domain_name). Користувацькі доменні імена важливі для користувачів, оскільки вони дозволяють їм зберегти свою суб'єктність від сервісу, якщо він стане поганим або буде придбаний іншою компанією, для якої конфіденційність не є пріоритетом.
- Функціональність псевдоніму для тих, хто використовує власні домени.
- Слід використовувати стандартні протоколи доступу до електронної пошти, такі як IMAP, SMTP або [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Стандартні протоколи доступу гарантують, що клієнти зможуть легко завантажити всю свою електронну пошту, якщо захочуть перейти до іншого сервісу.
- Послуги поштового сервісу повинні бути доступні через [onion сервіс](https://en.wikipedia.org/wiki/.onion).

### Приватність

Ми вважаємо за краще, щоб рекомендовані нами сервіси збирали якомога менше даних.

**Мінімальний функціонал:**

- Має захищати IP-адресу відправника, що може включати фільтрацію її відображення в полі заголовка `Received`.
- Не повинен вимагати особисту ідентифікаційну інформацію (PII), окрім імені користувача та пароля.
- Політика конфіденційності повинна відповідати вимогам, визначеним GDPR.

**Найкращі практики:**

- Має приймати [анонімні варіанти оплати](advanced/payments.md)[ (криптовалюта](cryptocurrency.md), готівка, подарункові картки тощо)
- Має бути розміщений в юрисдикції з суворими законами про захист конфіденційності електронної пошти.

### Безпека

Сервери електронної пошти мають справу з великою кількістю дуже чутливих даних. Ми очікуємо, що сервіси перейматимуть найкращі галузеві практики, щоб захистити своїх клієнтів.

**Мінімальний функціонал:**

- Захист вебпошти за допомогою 2FA, наприклад, [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Шифрування з нульовим доступом. Сервіс не має ключів для розшифрування даних, які він зберігає. Це запобігає витоку даних, до яких має доступ недобросовісний працівник, або витоку даних, які вкрав віддалений зловмисник, отримавши несанкціонований доступ до сервера.
- Підтримка [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions).
- Відсутність помилок або вразливостей TLS при аналізі такими інструментами, як [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh) або [Qualys SSL Labs](https://ssllabs.com/ssltest); це включає помилки, пов'язані з сертифікатом, і слабкі параметри DH, такі як ті, що призвели до [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Налаштування серверного набору (необов'язкове для TLS 1.3) для стійких наборів шифрів, які підтримують пряме шифрування та шифрування з автентифікацією.
- Правильні політики [MTA-STS](https://tools.ietf.org/html/rfc8461) та [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Дійсні записи [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities).
- Дійсні записи [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) та [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail).
- Повинні мати належний запис і політику [DMARC](https://en.wikipedia.org/wiki/DMARC) або використовувати [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) для автентифікації. Якщо використовується автентифікація DMARC, політика повинна бути налаштована на `відхилення` або `карантин`.
- Налаштування серверного набору TLS 1.2 або новішої версії та план для [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- Надсилання [SMTPS](https://en.wikipedia.org/wiki/SMTPS), якщо використовується SMTP.
- Стандарти безпеки вебсайтів, такі як:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subresource Integrity](https://en.wikipedia.org/wiki/Subresource_Integrity) при завантаженні із зовнішніх доменів.
- Повинен підтримувати перегляд [заголовків повідомлень](https://en.wikipedia.org/wiki/Email#Message_header), оскільки це важлива функція для визначення того, чи є лист спробою фішингу.

**Найкращі практики:**

- Має підтримувати апаратну автентифікацію, тобто. U2F та [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [Ресурсний запис DNS Certification Authority Authorization (CAA)](https://tools.ietf.org/html/rfc6844) на додачу до підтримки DANE.
- Має бути реалізовано [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), що стане в пригоді людям, які пишуть до списків розсилки [RFC8617](https://tools.ietf.org/html/rfc8617).
- Опубліковані аудити безпеки від авторитетної сторонньої фірми.
- Програми винагород за виправлення помилок та/або скоординований процес розкриття вразливостей.
- Стандарти безпеки вебсайтів, такі як:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Довіра

Ви б не довірили свої фінанси людині з підробленою ідентичністю, тож навіщо довіряти їй свою електронну пошту? Ми вимагаємо, щоб рекомендовані нами сервіси публічно заявляли про свою приналежність або керівництво. Ми також хотіли б бачити часті звіти про прозорість, особливо щодо того, як обробляються урядові запити.

**Мінімальний функціонал:**

- Відповідальне управління чи володіння.

**Найкращі практики:**

- Часті звіти про прозорість.

### Маркетинг

Сервіси електронної пошти, яких ми рекомендуємо, дотримуються принципів відповідального маркетингу.

**Мінімальний функціонал:**

- Повинні самостійно розміщувати аналітику (ніяких Google Analytics, Adobe Analytics і т. д.).
- Не повинно бути безвідповідального маркетингу, який може містити наступне:
    - Заяви про "незламне шифрування". Не можна приховувати вади шифрування якщо з'явиться технологія для його розкриття.
    - Гарантії захисту анонімності 100%. Коли хтось заявляє, що щось працює на 100%, це означає, що немає жодних шансів на невдачу. Ми знаємо, що люди можуть досить легко деанонімізувати себе різними способами, наприклад.:
        - Повторне використання особистої інформації, наприклад, електронної пошти, унікальних псевдонімів тощо, до якої вони отримали доступ без програмного забезпечення для забезпечення анонімності, як Tor
        - [Цифровий відбиток браузера](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Найкращі практики:**

- Чітка і легка для читання документація для таких завдань, як налаштування 2FA, поштових клієнтів, OpenPGP тощо.

### Додатковий функціонал

Хоча це не є суворими вимогами, є деякі інші фактори зручності та конфіденційності, які ми враховували при виборі сервісів, яких рекомендуємо.
