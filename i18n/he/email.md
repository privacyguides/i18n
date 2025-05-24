---
meta_title: "המלצות אימייל פרטי מוצפן - Privacy Guides"
title: "שירותי אימייל"
icon: material/email
description: ספקי אימייל אלה מציעים מקום מצוין לאחסן את המיילים שלך בצורה מאובטחת, ורבים מציעים הצפנת OpenPGP הניתנת להפעלה הדדית עם ספקים אחרים.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protects against the following threat(s):</small>

- [:material-server-network: ספקי שירות](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

אימייל הוא למעשה הכרח לשימוש בכל שירות מקוון, אולם איננו ממליצים עליו לשיחות מאדם לאדם. דואר אלקטרוני הוא למעשה הכרח שימוש בכל שירות מקוון, אולם איננו ממליצים עליו לשיחות מאדם לאדם.

[מסנג'רים (הודעות מיידיות) מומלצות](real-time-communication.md ""){.md-button}

## ספקים מומלצים

לכל השאר, אנו ממליצים על מגוון ספק אימייל המבוססים על מודלים עסקיים ברי קיימא ותכונות אבטחה ופרטיות מובנות. קרא את \[רשימת הקריטריונים המלאה\](#_20) שלנו למידע נוסף.

| Provider                    | OpenPGP / WKD                          | IMAP / SMTP                                                | Zero-Access Encryption                               | Anonymous Payment Methods             |
| --------------------------- | -------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------- | ------------------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Paid plans only | :material-check:{ .pg-green }                        | מזומן                                 |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                              | :material-information-outline:{ .pg-blue } Mail only | מזומן                                 |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                        | Monero <br>Cash via third party |

In addition to (or instead of) an email provider recommended here, you may wish to consider a dedicated [email aliasing service](email-aliasing.md#recommended-providers) to protect your privacy. Among other things, these services can help protect your real inbox from spam, prevent marketers from correlating your accounts, and encrypt all incoming messages with PGP.

- [More Information :material-arrow-right-drop-circle:](email-aliasing.md)

## ספקי אימייל מומלצים

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory (WKD) standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic end-to-end encrypted emails. לדוגמה, משתמש Proton Mail יכול לשלוח הודעת E2EE למשתמש Mailbox.org, או שאתה יכול לקבל התראות מוצפנות OpenPGP משירותי אינטרנט התומכים בכך.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

When using E2EE technology like OpenPGP your email will still have some metadata that is not encrypted in the header of the email, generally including the subject line! Read more about [email metadata](basics/email-security.md#email-metadata-overview).

OpenPGP also does not support forward secrecy, which means if the private key of either you or the message recipient is ever stolen, all previous messages encrypted with it will be exposed.

- [How do I protect my private keys?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail לוגו](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** הוא שירות דואר אלקטרוני עם התמקדות בפרטיות, הצפנה, אבטחה וקלות שימוש. They have been in operation since 2013. Proton AG is based in Geneva, Switzerland.

The Proton Free plan comes with 500 MB of Mail storage, which you can increase up to 1 GB for free.

[:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/mail/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }

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

Free accounts have some limitations, such as not being able to search body text and not having access to [Proton Mail Bridge](https://proton.me/mail/bridge), which is required to use a [recommended desktop email client](email-clients.md) (e.g., Thunderbird). חשבונות בתשלום כוללים תכונות כגון Proton Mail Bridge, אחסון נוסף ותמיכה בתחומים מותאמים אישית. If you have the Proton Unlimited plan or any multi-user Proton plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

[מכתב אישור](https://proton.me/blog/security-audit-all-proton-apps) סופק עבור האפליקציות של Proton Mail ב-9 בנובמבר 2021 על ידי [Securitum](https://research.securitum.com).

Proton Mail has internal crash reports that are **not** shared with third parties. This can be disabled in the web app: :gear: → **All Settings** → **Account** → **Security and privacy** → **Privacy and data collection**.

#### :material-check:{ .pg-green } דומיינים וכינויים מותאמים אישית

מנויי Proton Mail בתשלום יכולים להשתמש בדומיין משלהם עם השירות או בכתובת [תפוס-הכל](https://proton.me/support/catch-all). Proton Mail also supports [sub-addressing](https://proton.me/support/creating-aliases), which is useful for people who don't want to purchase a domain.

#### :material-check:{ .pg-green } שיטות תשלום פרטיות

Proton Mail [accepts](https://proton.me/support/payment-options) **cash** by mail in addition to standard credit/debit card, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), and PayPal payments.

#### :material-check:{ .pg-green } אבטחת חשבון

Proton Mail supports TOTP [two-factor authentication](https://proton.me/support/two-factor-authentication-2fa) and [hardware security keys](https://proton.me/support/2fa-security-key) using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two-factor authentication first.

#### :material-check:{ .pg-green } אבטחת מידע

ל-Proton Mail יש [הצפנה עם אפס-גישה](https://proton.me/blog/zero-access-encryption) במצב מנוחה עבור המיילים ו[היומנים](https://proton.me/news/protoncalendar-security-model) שלך. נתונים המאובטחים באמצעות הצפנת אפס גישה נגישים רק לך.

מידע מסוים המאוחסן ב-[Proton Contacts](https://proton.me/support/proton-contacts), כגון שמות תצוגה וכתובות אימייל, אינו מאובטח בהצפנה ללא גישה. שדות אנשי קשר התומכים בהצפנה ללא גישה, כגון מספרי טלפון, מסומנים בסמל מנעול.

#### :material-check:{ .pg-green } הצפנת אימייל

Proton Mail [שילבה הצפנת OpenPGP](https://proton.me/support/how-to-use-pgp) בדואר האינטרנט שלהם. אימיילים לחשבונות Proton Mail אחרים מוצפנים באופן אוטומטי, וניתן להפעיל הצפנה לכתובות שאינן פרוטון מייל עם מפתח OpenPGP בקלות בהגדרות החשבון שלך. Proton also supports automatic external key discovery with WKD. This means that emails sent to other providers which use WKD will be automatically encrypted with OpenPGP as well, without the need to manually exchange public PGP keys with your contacts. They also allow you to [encrypt messages to non-Proton Mail addresses without OpenPGP](https://proton.me/support/password-protected-emails), without the need for them to sign up for a Proton Mail account.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. This allows people who don't use Proton Mail to find the OpenPGP keys of Proton Mail accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Proton's own domains, like `@proton.me`. If you use a custom domain, you must [configure WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } סגירת חשבון

אם יש לך חשבון בתשלום והחשבון שלך [לא שולם](https://proton.me/support/delinquency) לאחר 14 יום, לא תוכל לגשת לנתונים שלך. לאחר 30 יום, החשבון שלך יהפוך לבלתי פעיל ולא יקבל דואר נכנס. אתה תמשיך להיות מחויב במהלך תקופה זו. Proton will [delete inactive free accounts](https://proton.me/support/inactive-accounts) after one year. You **cannot** reuse the email address of a deactivated account.

#### :material-information-outline:{ .pg-blue } פונקציונליות נוספת

Proton Mail's [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) plan also enables access to other Proton services in addition to providing multiple custom domains, unlimited hide-my-email aliases, and 500 GB of storage.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** is an email service with a focus on being secure, ad-free, and powered by 100% eco-friendly energy. הם פועלים מאז 2014. Mailbox.org ממוקם בברלין, גרמניה.

Accounts start with up to 2 GB storage, which can be upgraded as needed.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } דומיינים וכינויים מותאמים אישית

Mailbox.org lets you use your own domain, and they support [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) addresses. Mailbox.org also supports [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green } שיטות תשלום פרטיות

Mailbox.org אינו מקבל מטבעות קריפטוגרפיים כלשהם כתוצאה מכך שמעבד התשלומים BitPay השהה את הפעולות בגרמניה. However, they do accept **cash** by mail, **cash** payment to bank account, bank transfer, credit card, PayPal, and a couple of German-specific processors: Paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } אבטחת חשבון

Mailbox.org supports [two-factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. You can use either TOTP or a [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via the [YubiCloud](https://yubico.com/products/services-software/yubicloud). Web standards such as [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) are not yet supported.

#### :material-information-outline:{ .pg-blue } אבטחת מידע

Mailbox.org allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). הודעות חדשות שתקבל יוצפנו באופן מיידי באמצעות המפתח הציבורי שלך.

However, [Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. A [standalone option](calendar.md) may be more appropriate for that data.

#### :material-check:{ .pg-green } הצפנת אימייל

Mailbox.org has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox.org's servers. תכונה זו שימושית כאשר לנמען המרוחק אין OpenPGP ואין באפשרותו לפענח עותק של הדואר האלקטרוני בתיבת הדואר שלו.

Mailbox.org also supports the discovery of public keys via HTTP from their WKD. This allows people outside of Mailbox.org to find the OpenPGP keys of Mailbox.org accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Mailbox.org's own domains, like `@mailbox.org`. If you use a custom domain, you must [configure WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } סגירת חשבון

Your account will be set to a restricted user account when your contract ends. It will be irrevocably deleted after [30 days](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } פונקציונליות נוספת

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). However, their webmail interface cannot be accessed via their .onion service, and you may experience TLS certificate errors.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox.org תומך גם ב-[Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) בנוסף לפרוטוקולי גישה סטנדרטיים כמו IMAP ו-POP3.

Mailbox.org כולל תכונת מורשת דיגיטלית לכל התוכניות. You can choose whether you want any of your data to be passed to heirs, providing that they apply and provide your testament. לחלופין, ניתן למנות אדם לפי שם וכתובת.

## עוד ספקים

ספקים אלה מאחסנים את המיילים שלך עם הצפנת אפס ידע, מה שהופך אותם לאפשרויות נהדרות לשמירה על אבטחת המיילים המאוחסנים שלך. עם זאת, הם אינם תומכים בתקני הצפנה הדדיים עבור תקשורת E2EE בין ספקים שונים.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (formerly *Tutanota*) is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since 2011 and is based in Hanover, Germany.

Free accounts start with 1 GB of storage.

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:fontawesome-brands-windows: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta doesn't support the [IMAP protocol](https://tuta.com/support#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/support#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } דומיינים וכינויים מותאמים אישית

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/support#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/support#plus), but you can use a [catch-all](https://tuta.com/support#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } שיטות תשלום פרטיות

Tuta only directly accepts credit cards and PayPal, however [**cryptocurrency**](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with ProxyStore.

#### :material-check:{ .pg-green } אבטחת חשבון

Tuta supports [two-factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } אבטחת מידע

Tuta has [zero-access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). משמעות הדבר היא שההודעות ונתונים אחרים המאוחסנים בחשבונך ניתנים לקריאה רק על ידך.

#### :material-information-outline:{ .pg-blue } הצפנת אימייל

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } סגירת חשבון

Tuta will [delete inactive free accounts](https://tuta.com/support#inactive-accounts) after six months. אם ברצונך לשלם, באפשרותך להשתמש שוב בחשבון חינמי שהושבת.

#### :material-information-outline:{ .pg-blue } פונקציונליות נוספת

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/secure-email-for-non-profit) for free or with a heavy discount.

## קריטריונים

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an email provider, and conduct your own research to ensure the email provider you choose is the right choice for you.

### טכנולוגיה

אנו רואים בתכונות אלה חשיבות על מנת לספק שירות בטוח ומיטבי. אתה צריך לשקול אם לספק יש לו את התכונות שאתה צריך.

**מינימום כדי לעמוד בדרישות:**

- Must encrypt email account data at rest with zero-access encryption.
- Must be capable of exporting emails as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .EML with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). שמות דומיין מותאמים אישית חשובים למשתמשים מכיוון שהם מאפשרים להם לתחזק את הסוכנות שלהם מהשירות, אם היא תהפוך לגרועה או תירכש על ידי חברה אחרת שאינה מתעדפת פרטיות.
- Must operate on owned infrastructure, i.e. not built upon third-party email service providers.

**המקרה הטוב ביותר:**

- Should encrypt all account data (contacts, calendars, etc.) at rest with zero-access encryption.
- Should provide integrated webmail E2EE/PGP encryption as a convenience.
- Should support WKD to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key with this command: `gpg --locate-key example_user@example.com`.
- תמיכה בתיבת דואר זמנית למשתמשים חיצוניים. This is useful when you want to send an encrypted email without sending an actual copy to your recipient. למיילים אלה יש בדרך כלל תוחלת חיים מוגבלת ולאחר מכן נמחקות אוטומטית. הם גם לא דורשים מהנמען להגדיר שום קריפטוגרפיה כמו OpenPGP.
- Should support [sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Should allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). שמות דומיין מותאמים אישית חשובים למשתמשים מכיוון שהם מאפשרים להם לתחזק את הסוכנות שלהם מהשירות, אם היא תהפוך לגרועה או תירכש על ידי חברה אחרת שאינה מתעדפת פרטיות.
- Catch-all or alias functionality for those who use their own domains.
- Should use standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.
- Email provider's services should be available via an [onion service](https://en.wikipedia.org/wiki/.onion).

### פרטיות

אנו מעדיפים שהספקים המומלצים שלנו יאספו כמה שפחות נתונים.

**מינימום כדי לעמוד בדרישות:**

- Must protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Must not require personally identifiable information (PII) besides a username and a password.
- Privacy policy must meet the requirements defined by the GDPR.

**המקרה הטוב ביותר:**

- Should accept [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Should be hosted in a jurisdiction with strong email privacy protection laws.

### אבטחה

Email servers deal with a lot of very sensitive data. We expect that providers will adopt industry best practices in order to protect their customers.

**מינימום כדי לעמוד בדרישות:**

- Protection of webmail with 2FA, such as [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Zero-access encryption, which builds on encryption at rest. לספק אין את מפתחות הפענוח של הנתונים שברשותו. פעולה זו מונעת מעובד שסרח להדליף נתונים שיש לו גישה אליהם או מיריב מרחוק לשחרר נתונים שגנב על ידי השגת גישה בלתי מורשית לשרת.
- תמיכה ב [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions).
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLS 1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- [MTA-STS](https://tools.ietf.org/html/rfc8461) בתוקף וגם מדיניות [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- בתוקף [רשומות DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities).
- בתוקף [רשומות SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) ו - [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail).
- Must have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. אם נעשה שימוש באימות DMARC, יש להגדיר את המדיניות ל- `דוחה` או `הסגר`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [שליחת SMTPS](https://en.wikipedia.org/wiki/SMTPS), בהנחה שנעשה שימוש ב - SMTP.
- תקני אבטחת אתר אינטרנט כגון:
    - [אבטחת תעבורה קפדנית של HTTP](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - שלמות [תת - מקור](https://en.wikipedia.org/wiki/Subresource_Integrity) אם מעמיסים דברים מדומיינים חיצוניים.
- Must support viewing of [message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**המקרה הטוב ביותר:**

- Should support hardware authentication, i.e. U2F and [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [אישור רשות ההסמכה של DNS (CAA) רשומת משאבים](https://tools.ietf.org/html/rfc6844) בנוסף לתמיכת DANE.
- Should implement [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Published security audits from a reputable, third-party firm.
- תוכניות לחיפוש באגים ו/או תהליך גילוי - פגיעות מתואם.
- תקני אבטחת אתר אינטרנט כגון:
    - [מדיניות אבטחת תוכן (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### אמון

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? אנו דורשים מהספקים המומלצים שלנו להיות פומביים לגבי הבעלות או המנהיגות שלהם. כמו כן, היינו רוצים לראות דיווחי שקיפות תכופים, במיוחד בכל הנוגע לאופן הטיפול בבקשות ממשלתיות.

**מינימום כדי לעמוד בדרישות:**

- מנהיגות ציבורית או בעלות.

**המקרה הטוב ביותר:**

- דוחות שקיפות תכופים.

### שיווק

With the email providers we recommend, we like to see responsible marketing.

**מינימום כדי לעמוד בדרישות:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.).
- Must not have any irresponsible marketing, which can include the following:
    - Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
    - Guarantees of protecting anonymity 100%. When someone makes a claim that something is 100%, it means there is no certainty for failure. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:
        - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software such as Tor
        - [טביעת אצבע של דפדפן](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**המקרה הטוב ביותר:**

- Clear and easy-to-read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### פונקציונליות נוספת

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
