---
meta_title: "Encrypted Private Email Recommendations - Privacy Guides"
title: "Сервіси електронної пошти"
icon: material/email
description: Ці провайдери електронної пошти пропонують чудове місце для безпечного зберігання ваших листів, а багато з них пропонують сумісне з іншими провайдерами шифрування OpenPGP.
cover: email.webp
---

Електронна пошта це практично необхідність для користування будь-яким онлайн-сервісом, проте ми не рекомендуємо використовувати її для особистих розмов. Замість того, щоб використовувати електронну пошту для зв'язку з іншими людьми, розгляньте можливість використання засобів обміну повідомленнями, які підтримують таємницю.

[Рекомендовані месенджери](real-time-communication.md ""){.md-button}

Для всього іншого ми рекомендуємо різноманітні поштові сервіси, що базуються на стійких бізнес-моделях і мають вбудовані функції безпеки та конфіденційності.

- [OpenPGP-сумісні провайдери електронної пошти :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [Інші провайдери електронної пошти з шифруванням :material-arrow-right-drop-circle:](#more-providers)
- [Послуги аліасингу електронної пошти :material-arrow-right-drop-circle:](#email-aliasing-services)
- [Варіанти самостійного розміщення :material-arrow-right-drop-circle:](#self-hosting-email)

## Сервіси, сумісні з OpenPGP

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic E2EE emails. Наприклад, користувач Proton Mail може надіслати повідомлення E2EE користувачеві Mailbox.org, або ви можете отримувати сповіщення, зашифровані за допомогою OpenPGP, від інтернет-сервісів, які його підтримують.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Skiff Mail logo](assets/img/email/skiff-mail.svg){ .twemoji } [Skiff Mail](email.md#skiff-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

When using E2EE technology like OpenPGP your email will still have some metadata that is not encrypted in the header of the email, generally including the subject line! Read more about [email metadata](basics/email-security.md#email-metadata-overview).

OpenPGP also does not support Forward secrecy, which means if either your or the recipient's private key is ever stolen, all previous messages encrypted with it will be exposed. [How do I protect my private keys?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Логотип Proton Mail](assets/img/email/protonmail.svg){ align=right }

**Proton Mail — це поштовий сервіс з акцентом на конфіденційності, шифруванні, безпеці та простоті використання. Вони працюють з **2013 року**. Компанія Proton AG базується в Женеві, Швейцарія. Облікові записи починаються з 500 МБ пам'яті в безкоштовному тарифному плані.

[:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
- [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Безкоштовні акаунти мають деякі обмеження, такі як відсутність можливості пошуку в основному тексті та доступу до [Proton Mail Bridge](https://proton.me/mail/bridge), який необхідний для використання [рекомендованого десктопного поштового клієнта](email-clients.md) (наприклад, Thunderbird). Платні акаунти включають такі функції, як Proton Mail Bridge, додаткове сховище та підтримку власних доменів. [Атестаційний лист](https://proton.me/blog/security-audit-all-proton-apps) для додатків Proton Mail було надано 9 листопада 2021 року компанією [Securitum](https://research.securitum.com).

Якщо ви маєте тарифний план Proton Unlimited, Business або Visionary, ви також отримуєте [SimpleLogin](#simplelogin) Premium безкоштовно.

Proton Mail має внутрішні звіти про збої, які **не** передаються третім особам. Цю функцію можна вимкнути: **Налаштування** > **Перейти до налаштувань** > **Обліковий запис** > **Безпека та конфіденційність** > **Надсилати звіти про збої**.

#### :material-check:{ .pg-green } Користувацькі домени та аліаси

Абоненти оплачуваних планів Proton Mail можуть використовувати власний домен з сервісом або [всеохоплюючу](https://proton.me/support/catch-all) адресу. Proton Mail також підтримує [субадресацію](https://proton.me/support/creating-aliases), що корисно для людей, які не хочуть купувати домен.

#### :material-check:{ .pg-green } Конфіденційні способи оплати

Proton Mail [приймає](https://proton.me/support/payment-options) готівку поштою на додаток до стандартних кредитних/дебетових карток, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) та платежі через PayPal.

#### :material-check:{ .pg-green } Безпека облікового запису

Proton Mail підтримує [двофакторну автентифікацію за допомогою TOTP](https://proton.me/support/two-factor-authentication-2fa) та [апаратні ключі безпеки](https://proton.me/support/2fa-security-key) за стандартами FIDO2 або U2F. Використання апаратного ключа безпеки вимагає попереднього налаштування двофакторної автентифікації за допомогою TOTP.

#### :material-check:{ .pg-green } Безпека даних

Proton Mail має [шифрування з нульовим доступом](https://proton.me/blog/zero-access-encryption) у стані спокою для ваших електронних листів та [календарів](https://proton.me/news/protoncalendar-security-model). Дані, захищені шифруванням з нульовим доступом, доступні лише вам.

Певна інформація, що зберігається в [Proton Contacts](https://proton.me/support/proton-contacts), наприклад, імена користувачів та адреси електронної пошти, не захищена шифруванням з нульовим доступом. Поля контактів, які підтримують шифрування з нульовим доступом, наприклад, номери телефонів, позначені значком замка.

#### :material-check:{ .pg-green } Шифрування електронної пошти

Proton Mail має [інтегроване OpenPGP шифрування](https://proton.me/support/how-to-use-pgp) у своїй електронній пошті. Електронні листи на інші акаунти Proton Mail шифруються автоматично, а шифрування на адреси, що не належать до Proton Mail, за допомогою ключа OpenPGP можна легко ввімкнути в налаштуваннях вашого акаунта. Proton also supports automatic external key discovery with [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This means that emails sent to other providers which use WKD, such as Skiff Mail, will be automatically encrypted with OpenPGP as well, without the need to manually exchange public PGP keys with your contacts. They also allow you to [encrypt messages to non-Proton Mail addresses without OpenPGP](https://proton.me/support/password-protected-emails), without the need for them to sign up for a Proton Mail account.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. Це дозволяє людям, які не користуються Proton Mail, легко знайти OpenPGP ключі акаунтів Proton Mail для незалежного від провайдерів E2EE. This only applies to email addresses ending in one of Proton's own domains, like @proton.me. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Деактивація облікового запису

Якщо у вас платний акаунт і ваш рахунок [не сплачений](https://proton.me/support/delinquency) протягом 14 днів, ви не зможете отримати доступ до своїх даних. Через 30 днів ваш акаунт стане простроченим і не буде отримувати вхідну пошту. Протягом цього періоду ви продовжуватимете отримувати рахунки.

#### :material-information-outline:{ .pg-blue } Додаткова функціональність

Proton Mail пропонує "Безлімітний" акаунт за €9,99/місяць, який також надає доступ до Proton VPN на додаток до декількох облікових записів, доменів, псевдонімів та 500 ГБ сховища.

Proton Mail не пропонує функцію цифрової спадщини.

### Skiff Mail

<div class="admonition recommendation" markdown>

![Skiff Mail logo](assets/img/email/skiff-mail.svg){ align=right }

**Skiff Mail** is a web based email service with E2EE that began in 2020 that is based in San Francisco with developers worldwide. Accounts start with 10GB of free storage.

[:octicons-home-16: Homepage](https://skiff.com/mail){ .md-button .md-button--primary }
[:octicons-eye-16:](https://app.skiff.com/docs/db93c237-84c2-4b2b-9588-19a7cd2cd45a#tyGksN9rkqbo2uGYASxsA6HVLjUoly/wTYK8tncTto8=){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://skiff.com/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/skiff-org/skiff-apps){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: Android](https://play.google.com/store/apps/details?id=com.skemailmobileapp&pli=1)
- [:simple-appstore: iOS](https://apps.apple.com/us/app/skiff-mail/id1619168801)
- [:octicons-browser-16: Web](https://app.skiff.com/mail)

</details>

</div>

Skiff has undergone a few [audits](https://skiff.com/transparency) during its development.

#### :material-check:{ .pg-green } Користувацькі домени та аліаси

You can create up to 3 additional @skiff.com email aliases in addition to your primary account address on their free plan. Free accounts can add 1 [custom domain](https://skiff.com/blog/custom-domain-setup), and up to 15 custom domains on a paid plan. You can create unlimited aliases or a [catch-all](https://skiff.com/blog/catch-all-email-alias) alias on your custom domain.

#### :material-alert-outline:{ .pg-orange } Private Payment Methods

Skiff Mail accepts cryptocurrency payments via Coinbase Commerce, including Bitcoin and Ethereum, but they do not accept our recommended [cryptocurrency](cryptocurrency.md), Monero. They also accept credit card payments via Stripe.

#### :material-check:{ .pg-green } Безпека облікового запису

Skiff Mail supports TOTP two-factor authentication and hardware security keys using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two-factor authentication first.

#### :material-check:{ .pg-green } Безпека даних

Skiff Mail has zero access encryption at rest for all of your data. Це означає, що повідомлення та інші дані, які зберігаються у вашому акаунті, можете читати тільки ви.

#### :material-check:{ .pg-green } Шифрування електронної пошти

Skiff Mail encrypts messages to other Skiff mailboxes automatically with E2EE. On December 18th, 2023, Skiff added support for PGP and automatic public key discovery via Web Key Directory (WKD). This means that emails sent to other providers which use WKD, such as Proton Mail, will be automatically encrypted with OpenPGP as well without the need to exchange public PGP keys with your contacts. New Skiff Mail accounts should have a PGP key automatically generated, while accounts from before this feature was introduced need to generate a new PGP key for their address (or upload an existing private key) in the account's address settings. Skiff Mail only has support for reading messages encrypted with PGP/MIME, not the older PGP/Inline standard. Sending messages with PGP/MIME is the [recommended approach](https://www.gnupg.org/faq/gnupg-faq.html#use_pgpmime), but may pose compatibility issues in some edge cases.

Skiff Mail also publishes the public keys of Skiff Mail accounts via HTTP from their [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This allows people who don't use Skiff Mail to find the OpenPGP keys of Skiff Mail accounts easily, for cross-provider E2EE. This only applies to email addresses ending in one of Skiff's own domains, like @skiff.com. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

Skiff does not have a "temporary inbox" or "passworded email" feature like some other providers have, so that external users without OpenPGP cannot receive or reply to messages with E2EE.

#### :material-information-outline:{ .pg-blue } Деактивація облікового запису

Skiff Mail accounts do not expire, but unpaid accounts will be prompted to remove any enabled paid features (such as additional aliases) or renew their plan before the account can be used.

#### :material-information-outline:{ .pg-blue } Додаткова функціональність

Skiff additionally offers [workspace productivity features](https://discuss.privacyguides.net/t/skiff-pages-drive-productivity-tools/11758/13), but we still prefer [alternative](productivity.md) options for collaborating and file sharing at this time.

Skiff Mail does not offer a digital legacy feature.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Логотип Mailbox.org](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** — це поштовий сервіс, який прагне бути безпечним, не містить реклами та працює на 100% екологічно чистій енергії. Вони працюють з 2014 року. Mailbox.org базується в Берліні, Німеччина. Облікові записи починаються з 2 ГБ сховища, яке можна збільшити за потреби.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Користувацькі домени та аліаси

Mailbox.org дозволяє вам використовувати власний домен і підтримує [всеохоплюючі адреси](https://kb.mailbox.org/display/MBOKBEN/Using+catch-all+alias+with+own+domain). Mailbox.org також підтримує [субадресацію](https://kb.mailbox.org/display/BMBOKBEN/What+is+an+alias+and+how+do+I+use+it), що корисно, якщо ви не хочете купувати домен.

#### :material-check:{ .pg-green } Конфіденційні способи оплати

Mailbox.org не приймає жодних криптовалют, оскільки їхній платіжний процесор BitPay призупинив роботу в Німеччині. Однак вони приймають готівку поштою, готівку на банківський рахунок, банківські перекази, кредитні картки, PayPal і кілька німецьких платіжних систем: paydirekt і Sofortüberweisung.

#### :material-check:{ .pg-green } Безпека облікового запису

Mailbox.org підтримує [двофакторну аутентифікацію](https://kb.mailbox.org/display/MBOKBEN/How+to+use+two-factor+authentication+-+2FA) лише для їхньої електронної пошти. You can use either TOTP or a [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via the [YubiCloud](https://www.yubico.com/products/services-software/yubicloud). Веб-стандарти, такі як [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) на цей момент не підтримуються.

#### :material-information-outline:{ .pg-blue } Безпека даних

Mailbox.org дозволяє шифрувати вхідну пошту за допомогою їхньої [зашифрованої поштової скриньки](https://kb.mailbox.org/display/MBOKBEN/The+Encrypted+Mailbox). Нові повідомлення, які ви отримуєте, будуть негайно зашифровані вашим публічним ключем.

Однак, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), програмна платформа, що використовується Mailbox.org, [не підтримує](https://kb.mailbox.org/display/BMBOKBEN/Encryption+of+calendar+and+address+book) шифрування вашої адресної книги та календаря. Для цієї інформації може бути більш доречною [окрема опція](calendar.md).

#### :material-check:{ .pg-green } Шифрування електронної пошти

Mailbox.org має [інтегроване шифрування](https://kb.mailbox.org/display/MBOKBEN/Send+encrypted+e-mails+with+Guard) у свою електронну пошту, що спрощує надсилання повідомлень людям з публічними ключами OpenPGP. Вони також дозволяють віддаленим одержувачам [розшифровувати електронні листи](https://kb.mailbox.org/display/MBOKBEN/My+recipient+does+not+use+PGP) на серверах Mailbox.org. Ця функція корисна, коли віддалений одержувач не має OpenPGP і не може розшифрувати копію листа у власній поштовій скриньці.

Mailbox.org також підтримує виявлення публічних ключів через HTTP з їхнього [каталогу веб-ключів (WKD)](https://wiki.gnupg.org/WKD). Це дозволяє людям за межами Mailbox.org легко знаходити ключі OpenPGP акаунтів Mailbox.org для незалежного від провайдерів E2EE. This only applies to email addresses ending in one of Mailbox.org's own domains, like @mailbox.org. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Деактивація облікового запису

Після закінчення контракту ваш обліковий запис буде переведено в режим обмеженого користування, а через [30 днів він буде безповоротно видалений](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Додаткова функціональність

Ви можете отримати доступ до свого облікового запису Mailbox.org через IMAP/SMTP за допомогою їхнього сервісу [.onion](https://kb.mailbox.org/display/MBOKBEN/The+Tor+exit+node+of+mailbox.org). Однак їхній інтерфейс електронної пошти не може бути доступний через сервіс .onion, і у вас можуть виникати помилки TLS сертифіката.

Усі акаунти постачаються з обмеженим хмарним сховищем, яке [можна зашифрувати](https://kb.mailbox.org/display/MBOKBEN/Encrypt+files+on+your+Drive). Mailbox.org також пропонує аліас [@secure.mailbox.org](https://kb.mailbox.org/display/MBOKBEN/Ensuring+E-Mails+are+Sent+Securely), який забезпечує TLS шифрування на з'єднанні між поштовими серверами, інакше повідомлення не буде надіслано взагалі. Mailbox.org також підтримує [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) на додаток до стандартних протоколів доступу, таких як IMAP і POP3.

Mailbox.org має функцію цифрової спадщини для всіх тарифних планів. Ви можете вибрати, чи хочете ви, щоб будь-які ваші дані були передані спадкоємцям, за умови, що вони подадуть заяву та нададуть ваш заповіт. Крім того, ви можете номінувати людину за ім'ям та адресою.

## Більше провайдерів

Ці провайдери зберігають ваші електронні листи за допомогою шифрування з нульовим рівнем доступу, що робить їх чудовими варіантами для захисту ваших збережених електронних листів. However, they don't support interoperable encryption standards for E2EE communications between different providers.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg){ .twemoji } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg){ align=right }

**Tuta** is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since **2011** and is based in Hanover, Germany. Облікові записи починаються з 1 ГБ пам'яті в безкоштовному тарифному плані.

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
[:octicons-heart-16:](https://tuta.com/community/){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/tutanota/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:simple-windows11: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com/)

</details>

</div>

Tuta doesn't support the [IMAP protocol](https://tuta.com/faq/#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/posts/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/howto#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } Користувацькі домени та аліаси

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/faq#custom-domain). Tuta doesn't allow for [subaddressing (plus addresses)](https://tuta.com/faq#plus), but you can use a [catch-all](https://tuta.com/howto#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } Конфіденційні способи оплати

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/faq/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green } Безпека облікового запису

Tuta supports [two factor authentication](https://tuta.com/faq#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Безпека даних

Tuta has [zero access encryption at rest](https://tuta.com/faq#what-encrypted) for your emails, [address book contacts](https://tuta.com/faq#encrypted-address-book), and [calendars](https://tuta.com/faq#calendar). Це означає, що повідомлення та інші дані, які зберігаються у вашому акаунті, можете читати тільки ви.

#### :material-information-outline:{ .pg-blue } Шифрування електронної пошти

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Деактивація облікового запису

Tuta will [delete inactive free accounts](https://tuta.com/faq#inactive-accounts) after six months. Ви можете повторно використовувати деактивований безкоштовний акаунт, якщо заплатите.

#### :material-information-outline:{ .pg-blue } Additional Functionality

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/posts/secure-email-for-non-profit) for free or with a heavy discount.

Tuta also has a business feature called [Secure Connect](https://tuta.com/secure-connect/). Це забезпечує контакт клієнта з бізнесом, який використовує E2EE. Ця функція коштує 240 євро на рік.

Tuta doesn't offer a digital legacy feature.

## Служби аліасингу електронної пошти

Сервіс аліасів електронної пошти дозволяє вам легко генерувати нову адресу електронної пошти для кожного веб-сайту, на якому ви реєструєтесь. Створені вами аліаси пересилають всю пошту на обрану вами адресу електронної пошти, приховуючи як вашу "основну" електронну адресу, так і особу вашого провайдера електронної пошти. Справжній аліасінг електронної пошти краще, ніж адресація з плюсом, яка широко використовується і підтримується багатьма провайдерами, що дозволяє створювати псевдоніми на кшталт ваше ім'я +[щозавгодно]@example.com, оскільки веб-сайти, рекламодавці та мережі відстеження можуть банально видалити все, що стоїть після знака +, щоб дізнатися вашу справжню електронну адресу.

<div class="grid cards" markdown>

- ![addy.io logo](assets/img/email/mini/addy.svg){ .twemoji } [addy.io](email.md#addyio)
- ![SimpleLogin logo](assets/img/email/simplelogin.svg){ .twemoji } [SimpleLogin](email.md#simplelogin)

</div>

Псевдонімізація електронної пошти може слугувати захистом на випадок, якщо ваш поштовий провайдер припинить роботу. У цьому випадку ви можете легко перенаправити свої аліаси на нову адресу електронної пошти. Своєю чергою, однак, ви довіряєте службі аліасингу, в подальшому функціонуванні.

Використання спеціального сервісу аліасингу електронної пошти також має низку переваг у порівнянні з універсальним псевдонімом у власному домені:

- Псевдоніми можна вмикати та вимикати індивідуально, коли вам це потрібно, щоб веб-сайти не надсилали вам випадкових листів.
- Відповіді надсилаються з псевдо-адреси, яка приховує вашу справжню електронну адресу.

Вони також мають низку переваг над "тимчасовими поштовими сервісами":

- Аліаси є постійними і можуть бути ввімкнені знову, якщо вам потрібно отримати щось на кшталт скидання пароля.
- Імейли надсилаються на вашу довірену поштову скриньку, а не зберігаються у провайдера псевдонімів.
- Тимчасові поштові служби зазвичай мають загальнодоступні поштові скриньки, до яких може отримати доступ будь-хто, хто знає адресу, а аліаси є приватними для вас.

Ми рекомендуємо провайдерів, які дозволяють створювати аліаси на доменах, які вони контролюють, а також на власних доменах за помірну щорічну плату. Вони також можуть бути розміщені самостійно, якщо ви хочете отримати максимальний контроль. Однак використання власного домену може мати недоліки, пов'язані з конфіденційністю: Якщо ви єдина людина, яка використовує власний домен, ваші дії можна легко відстежити на різних веб-сайтах, просто подивившись на доменне ім'я в адресі електронної пошти та ігноруючи все, що стоїть перед знаком at (@).

Використання сервісу псевдонімів вимагає довіри до ваших незашифрованих повідомлень як з боку вашого провайдера електронної пошти, так і з боку провайдера аліасів. Деякі провайдери дещо пом'якшують цю проблему за допомогою автоматичного PGP шифрування, яке зменшує кількість сторін, яким ви повинні довіряти, з двох до однієї, шифруючи вхідні електронні листи до того, як вони будуть доставлені до вашого кінцевого провайдера поштової скриньки.

### addy.io

<div class="admonition recommendation" markdown>

![addy.io logo](assets/img/email/addy.svg#only-light){ align=right }
![addy.io logo](assets/img/email/addy-dark.svg#only-dark){ align=right }

**addy.io** lets you create 10 domain aliases on a shared domain for free, or unlimited "standard" aliases which are less anonymous.

[:octicons-home-16: Homepage](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://app.addy.io/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://addy.io/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: Android](https://addy.io/faq/#is-there-an-android-app)
- [:material-apple-ios: iOS](https://addy.io/faq/#is-there-an-ios-app)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/addy_io/)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/addyio-anonymous-email-fo/iadbdpnoknmbdeolbapdackdcogdmjpe)

</details>

</div>

The number of shared aliases (which end in a shared domain like @addy.io) that you can create is limited to 10 on addy.io's free plan, 50 on their $1/month plan and unlimited on the $4/month plan (billed $3 for a year). You can create unlimited standard aliases (which end in a domain like @[username].addy.io or a custom domain on paid plans), however, as previously mentioned, this can be detrimental to privacy because people can trivially tie your standard aliases together based on the domain name alone. They are useful where a shared domain might be blocked by a service. Securitum [audited](https://addy.io/blog/addy-io-passes-independent-security-audit/) addy.io in September 2023 and no significant vulnerabilities [were identified](https://addy.io/addy-io-security-audit.pdf).

Особливі безкоштовні можливості:

- [x] 10 спільних псевдонімів
- [x] Необмежена кількість стандартних псевдонімів
- [ ] Немає вихідних відповідей
- [x] 1 Recipient Mailboxes
- [x] Автоматичне шифрування PGP

### SimpleLogin

<div class="admonition recommendation" markdown>

![Логотип Simplelogin](assets/img/email/simplelogin.svg){ align=right }

**SimpleLogin — це безкоштовний сервіс, який надає аліаси для електронної пошти на низці загальних доменних імен, а також опціонально надає платні функції, такі як необмежена кількість псевдонімів та власні домени.

[:octicons-home-16: Homepage](https://simplelogin.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplelogin.io/privacy/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://simplelogin.io/docs/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simple-login){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
- [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/simplelogin/)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
- [:simple-safari: Safari](https://apps.apple.com/app/id1494051017)

</details>

</div>

SimpleLogin був [придбаний компанією Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) 8 квітня 2022 року. Якщо ви використовуєте Proton Mail як основну поштову скриньку, SimpleLogin — чудовий вибір. Оскільки обидва продукти тепер належать одній компанії, вам достатньо довіряти лише одному суб'єкту. Ми також очікуємо, що в майбутньому SimpleLogin буде більш тісно інтегрований з пропозиціями Proton. SimpleLogin продовжує підтримувати переадресацію до будь-якого провайдера електронної пошти на ваш вибір. Securitum [провела аудит](https://simplelogin.io/blog/security-audit/) SimpleLogin на початку 2022 року, і всі проблеми [були вирішені](https://simplelogin.io/audit2022/web.pdf).

Ви можете прив'язати свій обліковий запис SimpleLogin до свого облікового запису Proton в налаштуваннях. Якщо ви маєте тарифний план Proton Unlimited, Business або Visionary, ви отримаєте SimpleLogin Premium безкоштовно.

Особливі безкоштовні можливості:

- [x] 10 спільних псевдонімів
- [x] Необмежена кількість відповідей
- [x] 1 Поштова скринька одержувача

## Самостійний хостинг електронної пошти

Досвідчені системні адміністратори можуть розглянути можливість створення власного поштового сервера. Поштові сервери потребують уваги та постійного обслуговування, щоб забезпечити безпеку та надійність доставки пошти.

### Комбіновані програмні рішення

<div class="admonition recommendation" markdown>

![Логотип Mailcow](assets/img/email/mailcow.svg){ align=right }

**Mailcow** — це більш просунутий поштовий сервер, який ідеально підходить для тих, хто має трохи більше досвіду роботи з Linux. У ньому є все необхідне в Docker-контейнері: Поштовий сервер з підтримкою DKIM, антивірус та спам-моніторинг, електронна пошта та ActiveSync з SOGo, а також веб-адміністрування з підтримкою 2FA.

[:octicons-home-16: Домашня сторінка](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailcow.github.io/mailcow-dockerized-docs/){ .card-link title=Документація}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Вихідний код" }
[:octicons-heart-16:](https://www.servercow.de/mailcow?lang=en#sal){ .card-link title=Зробити внесок}

</div>

<div class="admonition recommendation" markdown>

![Логотип Mail-in-a-Box](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** — це автоматизований скрипт для розгортання поштового сервера на Ubuntu. Його мета — полегшити людям створення власного поштового сервера.

[:octicons-home-16: Домашня сторінка](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Документація}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Вихідний код" }

</div>

Для більш ручного підходу ми вибрали ці дві статті:

- [Налаштування поштового сервера з OpenSMTPD, Dovecot та Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd/) (2019)
- [Як запустити власний поштовий сервер](https://www.c0ffee.net/blog/mail-server-guide/) (серпень 2017)

## Критерії

**Будь ласка, зверніть увагу, що ми не пов'язані з жодним із рекомендованих нами провайдерів.** На додаток до [наших стандартних критеріїв](about/criteria.md), ми розробили чіткий набір вимог до будь-якого постачальника послуг електронної пошти, який бажає бути рекомендованим, включаючи впровадження найкращих галузевих практик, сучасних технологій тощо. Ми радимо вам ознайомитися з цим списком перед тим, як обирати постачальника послуг електронної пошти, а також провести власне дослідження, щоб переконатися, що обраний вами провайдер є правильним вибором для вас.

### Технологія

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

### Privacy

We prefer our recommended providers to collect as little data as possible.

**Minimum to Qualify:**

- Protect sender's IP address. Filter it from showing in the `Received` header field.
- Don't require personally identifiable information (PII) besides a username and a password.
- Privacy policy that meets the requirements defined by the GDPR.

**Best Case:**

- Accepts [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Hosted in a jurisdiction with strong email privacy protection laws.

### Security

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

### Trust

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? We require our recommended providers to be public about their ownership or leadership. We also would like to see frequent transparency reports, especially in regard to how government requests are handled.

**Minimum to Qualify:**

- Public-facing leadership or ownership.

**Best Case:**

- Public-facing leadership.
- Frequent transparency reports.

### Marketing

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

### Additional Functionality

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
