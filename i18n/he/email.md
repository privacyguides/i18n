---
meta_title: "המלצות אימייל פרטי מוצפן - Privacy Guides"
title: "שירותי אימייל"
icon: material/email
description: ספקי אימייל אלה מציעים מקום מצוין לאחסן את המיילים שלך בצורה מאובטחת, ורבים מציעים הצפנת OpenPGP הניתנת להפעלה הדדית עם ספקים אחרים.
cover: email.webp
---

אימייל הוא למעשה הכרח לשימוש בכל שירות מקוון, אולם איננו ממליצים עליו לשיחות מאדם לאדם. דואר אלקטרוני הוא למעשה הכרח שימוש בכל שירות מקוון, אולם איננו ממליצים עליו לשיחות מאדם לאדם.

[מסנג'רים (הודעות מיידיות) מומלצות](real-time-communication.md ""){.md-button}

לכל השאר, אנו ממליצים על מגוון ספק אימייל המבוססים על מודלים עסקיים ברי קיימא ותכונות אבטחה ופרטיות מובנות.

- [ספקי דוא"ל תואמי OpenPGP :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [ספקים מוצפנים אחרים :material-arrow-right-drop-circle:](#more-providers)
- [שירותי כינוי אימייל :material-arrow-right-drop-circle:](#email-aliasing-services)
- [אפשרויות אירוח עצמי :material-arrow-right-drop-circle:](#self-hosting-email)

## ספקי אימייל מומלצים

ספקים אלה תומכים באופן מקורי בהצפנה/פענוח של OpenPGP וב[תקן מדריך מפתחות אינטרנט](basics/email-security.md#what-is-the-web-key-directory-standard), המאפשר לספק -אימיילים אגנוסטיים של E2EE. לדוגמה, משתמש Proton Mail יכול לשלוח הודעת E2EE למשתמש Mailbox.org, או שאתה יכול לקבל התראות מוצפנות OpenPGP משירותי אינטרנט התומכים בכך.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

When using E2EE technology like OpenPGP your email will still have some metadata that is not encrypted in the header of the email, generally including the subject line! Read more about [email metadata](basics/email-security.md#email-metadata-overview).

OpenPGP also does not support Forward secrecy, which means if either your or the recipient's private key is ever stolen, all previous messages encrypted with it will be exposed. [How do I protect my private keys?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail לוגו](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** הוא שירות דואר אלקטרוני עם התמקדות בפרטיות, הצפנה, אבטחה וקלות שימוש. הם פועלים מאז **2013**. Proton AG מבוססת בז'נב, שוויץ. חשבונות מתחילים עם 500 MB אחסון עם התוכנית החינמית שלהם.

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

לחשבונות חינמיים יש מגבלות מסוימות, כגון חוסר היכולת לחפש גוף טקסט ואי גישה ל[Proton Mail Bridge](https://proton.me/mail/bridge), אשר נדרש כדי השתמש ב[לקוח אימייל שולחן העבודה המומלץ](email-clients.md) (למשל Thunderbird). חשבונות בתשלום כוללים תכונות כגון Proton Mail Bridge, אחסון נוסף ותמיכה בתחומים מותאמים אישית. [מכתב אישור](https://proton.me/blog/security-audit-all-proton-apps) סופק עבור האפליקציות של Proton Mail ב-9 בנובמבר 2021 על ידי [Securitum](https://research.securitum.com).

אם יש לך תוכנית Proton Unlimited, Business או Visionary, אתה גם מקבל [SimpleLogin](#simplelogin) פרימיום בחינם.

ל-Proton Mail יש דוחות קריסה פנימיים שהם **לא** חולקים עם צדדים שלישיים. ניתן להשבית אפשרות זו ב: **הגדרות** > **עבור אל הגדרות** > **חשבון** > **אבטחה ופרטיות** > **שלח דוחות קריסה**.

#### :material-check:{ .pg-green } דומיינים וכינויים מותאמים אישית

מנויי Proton Mail בתשלום יכולים להשתמש בדומיין משלהם עם השירות או בכתובת [תפוס-הכל](https://proton.me/support/catch-all). Proton Mail also supports [sub-addressing](https://proton.me/support/creating-aliases), which is useful for people who don't want to purchase a domain.

#### :material-check:{ .pg-green } שיטות תשלום פרטיות

Proton Mail [מקבל](https://proton.me/support/payment-options) מזומן בדואר בנוסף לתשלומי אשראי/חיוב רגילים, [ביטקוין](advanced/payments.md#other-coins-bitcoin-ethereum-etc) ופייפאל.

#### :material-check:{ .pg-green } אבטחת חשבון

Proton Mail תומך באימות TOTP ב[שני גורמים](https://proton.me/support/two-factor-authentication-2fa) וב[מפתחות אבטחת חומרה](https://proton.me/support/2fa-security-key) באמצעות תקני FIDO2 או U2F. השימוש במפתח אבטחת חומרה מחייב הגדרת אימות דו - שלבי של TOTP תחילה.

#### :material-check:{ .pg-green } אבטחת מידע

ל-Proton Mail יש [הצפנה עם אפס-גישה](https://proton.me/blog/zero-access-encryption) במצב מנוחה עבור המיילים ו[היומנים](https://proton.me/news/protoncalendar-security-model) שלך. נתונים המאובטחים באמצעות הצפנת אפס גישה נגישים רק לך.

מידע מסוים המאוחסן ב-[Proton Contacts](https://proton.me/support/proton-contacts), כגון שמות תצוגה וכתובות אימייל, אינו מאובטח בהצפנה ללא גישה. שדות אנשי קשר התומכים בהצפנה ללא גישה, כגון מספרי טלפון, מסומנים בסמל מנעול.

#### :material-check:{ .pg-green } הצפנת אימייל

Proton Mail [שילבה הצפנת OpenPGP](https://proton.me/support/how-to-use-pgp) בדואר האינטרנט שלהם. אימיילים לחשבונות Proton Mail אחרים מוצפנים באופן אוטומטי, וניתן להפעיל הצפנה לכתובות שאינן פרוטון מייל עם מפתח OpenPGP בקלות בהגדרות החשבון שלך. Proton also supports automatic external key discovery with [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This means that emails sent to other providers which use WKD will be automatically encrypted with OpenPGP as well, without the need to manually exchange public PGP keys with your contacts. They also allow you to [encrypt messages to non-Proton Mail addresses without OpenPGP](https://proton.me/support/password-protected-emails), without the need for them to sign up for a Proton Mail account.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. זה מאפשר לאנשים שאינם משתמשים ב-Proton Mail למצוא בקלות את מפתחות OpenPGP של חשבונות Proton Mail, עבור E2EE חוצה ספקים. זה חל רק על כתובות אימיילים המסתיימות באחד מהדומיינים של פרוטון עצמו, כמו proton.me@. אם אתה משתמש בדומיין מותאם אישית, עליך [להגדיר את WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) בנפרד.

#### :material-information-outline:{ .pg-blue } סגירת חשבון

אם יש לך חשבון בתשלום והחשבון שלך [לא שולם](https://proton.me/support/delinquency) לאחר 14 יום, לא תוכל לגשת לנתונים שלך. לאחר 30 יום, החשבון שלך יהפוך לבלתי פעיל ולא יקבל דואר נכנס. אתה תמשיך להיות מחויב במהלך תקופה זו.

#### :material-information-outline:{ .pg-blue } פונקציונליות נוספת

Proton Mail מציע חשבון "ללא הגבלה" במחיר של €9.99/חודש, המאפשר גם גישה ל-Proton VPN בנוסף לאספקת מספר חשבונות, דומיינים, כינויים ושטח אחסון של 500GB.

Proton Mail אינו מציע תכונה מורשת דיגיטלית.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org לוגו](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** הוא שירות דוא"ל עם התמקדות בלהיות מאובטח, ללא פרסומות ומופעל באופן פרטי על ידי 100% אנרגיה ידידותית לסביבה. הם פועלים מאז 2014. Mailbox.org ממוקם בברלין, גרמניה. חשבונות מתחילים בנפח אחסון של 2 ג'יגה-בייט, שניתן לשדרג לפי הצורך.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } דומיינים וכינויים מותאמים אישית

Mailbox.org lets you use your own domain, and they support [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) addresses. Mailbox.org also supports [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green } שיטות תשלום פרטיות

Mailbox.org אינו מקבל מטבעות קריפטוגרפיים כלשהם כתוצאה מכך שמעבד התשלומים BitPay השהה את הפעולות בגרמניה. עם זאת, הם מקבלים מזומן בדואר, תשלום במזומן לחשבון בנק, העברה בנקאית, כרטיס אשראי, PayPal ועוד כמה מעבדים ספציפיים לגרמניה: paydirekt ו-Sofortüberweisung.

#### :material-check:{ .pg-green } אבטחת חשבון

Mailbox.org supports [two factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. You can use either TOTP or a [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via the [YubiCloud](https://yubico.com/products/services-software/yubicloud). תקני אינטרנט כגון [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) אינם נתמכים עדיין.

#### :material-information-outline:{ .pg-blue } אבטחת מידע

Mailbox.org allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). הודעות חדשות שתקבל יוצפנו באופן מיידי באמצעות המפתח הציבורי שלך.

However, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. [אפשרות עצמאית](calendar.md) עשויה להתאים יותר למידע זה.

#### :material-check:{ .pg-green } הצפנת אימייל

Mailbox.org has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox.org's servers. תכונה זו שימושית כאשר לנמען המרוחק אין OpenPGP ואין באפשרותו לפענח עותק של הדואר האלקטרוני בתיבת הדואר שלו.

Mailbox.org תומך גם בגילוי מפתחות ציבוריים באמצעות HTTP מ-[Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) שלהם. זה מאפשר לאנשים מחוץ Mailbox.org למצוא את מפתחות OpenPGP של חשבונות Mailbox.org בקלות, עבור E2EE חוצה ספקים. זה חל רק על כתובות אימיילים המסתיימות באחד מהדומיינים של Mailbox.org עצמו, כמו mailbox.org@. אם אתה משתמש בדומיין מותאם אישית, עליך [להגדיר את WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) בנפרד.

#### :material-information-outline:{ .pg-blue } סגירת חשבון

החשבון שלך יוגדר לחשבון משתמש מוגבל כאשר החוזה שלך יסתיים, לאחר [30 יום הוא יימחק באופן בלתי הפיך](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } פונקציונליות נוספת

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). עם זאת, לא ניתן לגשת לממשק דואר האינטרנט שלהם באמצעות שירות.onion שלהם ואתה עלול להיתקל בשגיאות אישור TLS.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox.org תומך גם ב-[Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) בנוסף לפרוטוקולי גישה סטנדרטיים כמו IMAP ו-POP3.

Mailbox.org כולל תכונת מורשת דיגיטלית לכל התוכניות. אתה יכול לבחור אם אתה רוצה שכל הנתונים שלך יועברו ליורשים בתנאי שהם חלים ומספקים את הצוואה שלך. לחלופין, ניתן למנות אדם לפי שם וכתובת.

## עוד ספקים

ספקים אלה מאחסנים את המיילים שלך עם הצפנת אפס ידע, מה שהופך אותם לאפשרויות נהדרות לשמירה על אבטחת המיילים המאוחסנים שלך. עם זאת, הם אינם תומכים בתקני הצפנה הדדיים עבור תקשורת E2EE בין ספקים שונים.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg){ .twemoji } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta לוגו](assets/img/email/tuta.svg){ align=right }

**Tuta** הוא שירות דואר אלקטרוני עם התמקדות באבטחה ופרטיות באמצעות שימוש בהצפנה. Tuta פועלת מאז **2011** ובסיסה בהאנובר, גרמניה. חשבונות מתחילים עם שטח אחסון של 1GB עם התוכנית החינמית שלהם.

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/faq){ .card-link title=Documentation}
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

Tuta אינו תומך ב[פרוטוקול IMAP](https://tuta.com/faq/#imap) או בשימוש ב[ של צד שלישי לקוחות אימייל](email-clients.md), וגם לא תוכל להוסיף [חשבונות אימייל חיצוניים](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) לאפליקציית Tuta. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/posts/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/howto#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } דומיינים וכינויים מותאמים אישית

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/faq#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/faq#plus), but you can use a [catch-all](https://tuta.com/howto#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } שיטות תשלום פרטיות

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/faq/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green } אבטחת חשבון

Tuta supports [two factor authentication](https://tuta.com/faq#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } אבטחת מידע

Tuta has [zero access encryption at rest](https://tuta.com/faq#what-encrypted) for your emails, [address book contacts](https://tuta.com/faq#encrypted-address-book), and [calendars](https://tuta.com/faq#calendar). משמעות הדבר היא שההודעות ונתונים אחרים המאוחסנים בחשבונך ניתנים לקריאה רק על ידך.

#### :material-information-outline:{ .pg-blue } הצפנת אימייל

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } סגירת חשבון

Tuta [ימחק חשבונות בחינם לא פעילים](https://tuta.com/faq#inactive-accounts) לאחר שישה חודשים. אם ברצונך לשלם, באפשרותך להשתמש שוב בחשבון חינמי שהושבת.

#### :material-information-outline:{ .pg-blue } פונקציונליות נוספת

Tuta מציעה את הגרסה העסקית של [Tuta לארגונים ללא מטרות רווח](https://tuta.com/blog/posts/secure-email-for-non-profit) בחינם או בהנחה כבדה.

Tuta also has a business feature called [Secure Connect](https://tuta.com/secure-connect). זה מבטיח שיצירת קשר עם הלקוח לעסק משתמשת ב- E2EE. התכונה עולה 240 אירו לשנה.

Tuta אינו מציע תכונה מורשת דיגיטלית.

## שירותי כינוי דוא"ל

שירות כינוי דוא"ל מאפשר לך ליצור בקלות כתובת דוא"ל חדשה עבור כל אתר שאתה נרשם אליו. כינויי הדואר האלקטרוני שאתה יוצר מועברים לאחר מכן לכתובת דוא"ל שתבחר, תוך הסתרת כתובת הדוא"ל "הראשית" שלך וגם זהות ספק הדוא"ל שלך. כינוי דוא"ל אמיתי טוב יותר מאשר כתובת פלוס הנפוצה בשימוש ונתמך על ידי ספקים רבים, מה שמאפשר לך ליצור כינויים כמו yourname+[anythinghere]@example.com, מכיוון שאתרים, מפרסמים ורשתות מעקב יכולים להסיר כל דבר לאחר סימן + כדי לדעת את כתובת הדוא"ל האמיתית שלך.

<div class="grid cards" markdown>

- ![addy.io לוגו](assets/img/email/mini/addy.svg){ .twemoji } [addy.io](email.md#addyio)
- ![SimpleLogin לוגו](assets/img/email/simplelogin.svg){ .twemoji } [SimpleLogin](email.md#simplelogin)

</div>

כינוי דוא"ל יכול לשמש כהגנה למקרה שספק הדוא"ל שלך יפסיק לפעול. בתרחיש זה, באפשרותך לנתב מחדש בקלות את הכינויים שלך לכתובת דואר אלקטרוני חדשה. עם זאת, אתה נותן אמון בשירות הכינוי כדי להמשיך לתפקד.

שימוש בשירות ייעודי של כינוי דואר אלקטרוני יש גם מספר יתרונות על פני כינוי 'לתפוס-הכל' על תחום מותאם אישית:

- ניתן להפעיל ולכבות כינויים באופן אישי בעת הצורך, וכך למנוע מאתרי אינטרנט לשלוח לך דוא"ל באופן אקראי.
- התגובות נשלחות מכתובת הכינוי, ומגינות על כתובת הדוא"ל האמיתית שלך.

תכונות חינמיות בולטות:

- כינויים הם קבועים וניתן להפעיל אותם שוב אם אתה צריך לקבל משהו כמו איפוס סיסמה.
- הודעות דוא"ל נשלחות לתיבת הדואר המהימנה שלך ולא מאוחסנות על ידי ספק הכינויים.
- שירותי דואר אלקטרוני זמניים בדרך כלל יש תיבות דואר ציבוריות אשר ניתן לגשת על ידי כל מי שמכיר את הכתובת, כינויים פרטיים שלך.

ההמלצות שלנו לכינוי דוא"ל הן ספקים המאפשרים לך ליצור כינויים בדומיינים שהם שולטים בהם, כמו גם דומיינ(ים) מותאמים אישית משלך תמורת תשלום שנתי צנוע. ניתן גם לארח אותם בעצמך אם אתה רוצה שליטה מקסימלית. עם זאת, שימוש בדומיין מותאם אישית יכול להיות בעל חסרונות הקשורים לפרטיות: אם אתה האדם היחיד המשתמש בדומיין המותאם אישית שלך, ניתן לעקוב בקלות אחר הפעולות שלך באתרי אינטרנט פשוט על ידי הסתכלות על שם הדומיין בכתובת הדוא"ל והתעלמות מכל מה שלפני ה-(@) סימן.

שימוש בשירות כינויים מחייב לתת אמון הן בספק הדואר האלקטרוני שלך והן בספק הכתובות שלך בהודעות הלא מוצפנות שלך. חלק מהספקים מפחיתים זאת מעט עם הצפנת PGP אוטומטית, שמפחיתה את מספר הצדדים שאתה צריך לסמוך עליהם משניים לאחד על ידי הצפנת הודעות דוא"ל נכנסות לפני שהן נמסרות לספק תיבת הדואר הסופי שלך.

### addy.io

<div class="admonition recommendation" markdown>

![addy.io לוגו](assets/img/email/addy.svg#only-light){ align=right }
![addy.io לוגו](assets/img/email/addy-dark.svg#only-dark){ align=right }

**addy.io** מאפשר לך ליצור 10 כינויים של דומיין בדומיין משותף בחינם, או כינויים "סטנדרטיים" ללא הגבלה שהם פחות אנונימיים.

[:octicons-home-16: Homepage](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://app.addy.io/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://addy.io/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: Android](https://addy.io/faq/#is-there-an-android-app)
- [:material-apple-ios: iOS](https://addy.io/faq/#is-there-an-ios-app)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/addy_io)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/addyio-anonymous-email-fo/iadbdpnoknmbdeolbapdackdcogdmjpe)

</details>

</div>

מספר הכינויים המשותפים (שמסתיימים בדומיין משותף כמו @addy.io) שאתה יכול ליצור מוגבל ל-10 בתוכנית החינמית של addy.io, 50 בתוכנית של $1 לחודש וללא הגבלה בתוכנית של $4 לחודש (החיוב 3 דולר לשנה). אתה יכול ליצור כינויים סטנדרטיים ללא הגבלה (שמסתיימים בדומיין כמו @[username].addy.io או דומיין מותאם אישית בתוכניות בתשלום), עם זאת, כפי שצוין קודם לכן, זה יכול להזיק לפרטיות מכיוון שאנשים יכולים לקשור באופן טריוויאלי את הכינויים הסטנדרטיים שלך יחד על סמך שם הדומיין בלבד. הם שימושיים כאשר דומיין משותף עשוי להיות חסום על ידי שירות. Securitum [audited](https://addy.io/blog/addy-io-passes-independent-security-audit) addy.io in September 2023 and no significant vulnerabilities [were identified](https://addy.io/addy-io-security-audit.pdf).

תכונות חינמיות בולטות:

- [x] 10 כינויים משותפים
- [x] כינויים סטנדרטיים ללא הגבלה
- [ ] אין תגובות יוצאות
- [x] 1 תיבות דואר של נמען
- [x] הצפנת PGP אוטומטית

### SimpleLogin

<div class="admonition recommendation" markdown>

![Simplelogin לוגו](assets/img/email/simplelogin.svg){ align=right }

**SimpleLogin** הוא שירות חינמי המספק כינויי דוא"ל על מגוון שמות דומיין משותפים, ובאופן אופציונלי מספק תכונות בתשלום כמו כינויים בלתי מוגבלים ודומיינים מותאמים אישית.

[:octicons-home-16: Homepage](https://simplelogin.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplelogin.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://simplelogin.io/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simple-login){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
- [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/simplelogin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
- [:simple-safari: Safari](https://apps.apple.com/app/id6475835429)

</details>

</div>

SimpleLogin [נרכשה על ידי Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) נכון ל-8 באפריל 2022. אם אתה משתמש ב-Proton Mail עבור תיבת הדואר הראשית שלך, SimpleLogin היא בחירה מצוינת. מכיוון ששני המוצרים נמצאים כעת בבעלות אותה חברה, כעת עליך לסמוך רק על ישות אחת. אנו גם מצפים ש-SimpleLogin תשתלב בצורה הדוקה יותר עם ההיצע של Proton בעתיד. SimpleLogin ממשיכה לתמוך בהעברה לכל ספק דוא"ל שתבחרו. Securitum [audited](https://simplelogin.io/blog/security-audit) SimpleLogin in early 2022 and all issues [were addressed](https://simplelogin.io/audit2022/web.pdf).

תוכל לקשר את חשבון SimpleLogin שלך בהגדרות עם חשבון Proton שלך. אם יש לך את הפרוטון ללא הגבלה, עסקים, או תוכנית חזון, יהיה לך SimpleLogin פרימיום בחינם.

תכונות חינמיות בולטות:

- [x] 10 כינויים משותפים
- [x] תשובות ללא הגבלה
- [x] 1 תיבת דואר נמען

## אימייל לאירוח עצמי

מנהלי מערכת מתקדמים עשויים לשקול הגדרת שרת דואר אלקטרוני משלהם. שרתי דואר דורשים תשומת לב ותחזוקה שוטפת על מנת לשמור על דברים מאובטחים ועל משלוח דואר אמין.

### פתרונות תוכנה משולבים

<div class="admonition recommendation" markdown>

![Mailcow לוגו](assets/img/email/mailcow.svg){ align=right }

**Mailcow** הוא שרת דואר מתקדם יותר המושלם עבור אלה עם קצת יותר ניסיון בלינוקס. יש לו את כל מה שאתה צריך במיכל Docker: שרת דואר עם תמיכה ב- DKIM, ניטור אנטי וירוס וספאם, דואר אינטרנט ו- ActiveSync עם SOGo, וניהול מבוסס אינטרנט עם תמיכה ב- 2FA.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

</div>

<div class="admonition recommendation" markdown>

![Mail-in-a-Box לוגו](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** הוא סקריפט התקנה אוטומטי לפריסת שרת דואר באובונטו. מטרתו היא להקל על אנשים להגדיר שרת דואר משלהם.

[:octicons-home-16: דף הבית](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=תיעוד}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="קוד מקור" }

</div>

לגישה ידנית יותר בחרנו את שני המאמרים הבאים:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://c0ffee.net/blog/mail-server-guide) (August 2017)

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף [לקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה לפני שתבחר ספק דוא"ל, ולערוך מחקר משלך כדי להבטיח שספק הדוא"ל שבחרת הוא הבחירה הנכונה עבורך.

### טכנולוגיה

אנו רואים בתכונות אלה חשיבות על מנת לספק שירות בטוח ומיטבי. אתה צריך לשקול אם לספק יש לו את התכונות שאתה צריך.

**מינימום כדי לעמוד בדרישות:**

- מצפין נתוני חשבון אימייל במצב מנוחה עם הצפנה ללא גישה.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- מאפשר למשתמשים להשתמש ב[שם דומיין](https://en.wikipedia.org/wiki/Domain_name) משלהם. שמות דומיין מותאמים אישית חשובים למשתמשים מכיוון שהם מאפשרים להם לתחזק את הסוכנות שלהם מהשירות, אם היא תהפוך לגרועה או תירכש על ידי חברה אחרת שאינה מתעדפת פרטיות.
- פועל על תשתית בבעלות, כלומר לא בנוי על ספקי שירותי דואר אלקטרוני של צד שלישי.

**המקרה הטוב ביותר:**

- מצפין את כל נתוני החשבון (אנשי קשר, יומנים וכו') במצב מנוחה עם הצפנה ללא גישה.
- הצפנת דואר אינטרנט משולבת E2EE/PGP מסופקת לנוחיותך.
- תמיכה עבור [WKD](https://wiki.gnupg.org/WKD) כדי לאפשר גילוי משופר של מפתחות OpenPGP ציבוריים באמצעות HTTP. משתמשי GnuPG יכולים לקבל מפתח על ידי הקלדה `gpg --locate-key example_user@example.com`
- תמיכה בתיבת דואר זמנית למשתמשים חיצוניים. פעולה זו שימושית כאשר ברצונך לשלוח דוא"ל מוצפן, מבלי לשלוח עותק בפועל לנמען שלך. למיילים אלה יש בדרך כלל תוחלת חיים מוגבלת ולאחר מכן נמחקות אוטומטית. הם גם לא דורשים מהנמען להגדיר שום קריפטוגרפיה כמו OpenPGP.
- זמינות שירותי ספק הדואר האלקטרוני באמצעות [שירות onion](https://en.wikipedia.org/wiki/.onion).
- [Sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing) support.
- פונקציונליות של תפוס - הכל או כינוי עבור בעלי דומיינים משלהם.
- שימוש בפרוטוקולי גישה סטנדרטיים למייל כגון IMAP, SMTP או [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). פרוטוקולי גישה סטנדרטיים מבטיחים שלקוחות יכולים להוריד בקלות את כל האימייל שלהם, אם הם רוצים לעבור לספק אחר.

### פרטיות

אנו מעדיפים שהספקים המומלצים שלנו יאספו כמה שפחות נתונים.

**מינימום כדי לעמוד בדרישות:**

- להגן על כתובת ה - IP של השולח. מסנן אותו כך שלא יוצג בשדה `השולח` header.
- אין צורך במידע המאפשר זיהוי אישי (PII) מלבד שם משתמש וסיסמה.
- מדיניות פרטיות העומדת בדרישות שהוגדרו ב-GDPR.

**המקרה הטוב ביותר:**

- מקבל [אפשרויות תשלום אנונימיות](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), מזומן, כרטיסי מתנה וכו')
- מתארח באזור שיפוט עם חוקים חזקים להגנה על פרטיות האימייל.

### אבטחה

שרתי דואר אלקטרוני עוסקים בהרבה מאוד נתונים רגישים. אנו מצפים שהספקים יאמצו שיטות עבודה מומלצות בתעשייה כדי להגן על חבריהם.

**מינימום כדי לעמוד בדרישות:**

- הגנה על דואר אינטרנט עם 2FA, כגון TOTP.
- הצפנת אפס גישה, מתבססת על הצפנה במנוחה. לספק אין את מפתחות הפענוח של הנתונים שברשותו. פעולה זו מונעת מעובד שסרח להדליף נתונים שיש לו גישה אליהם או מיריב מרחוק לשחרר נתונים שגנב על ידי השגת גישה בלתי מורשית לשרת.
- תמיכה ב [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions).
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- העדפת חבילת שרתים (אופציונלית ב-TLSv1.3) עבור חבילות צופן חזקות התומכות בסודיות קדימה ובהצפנה מאומתת.
- [MTA-STS](https://tools.ietf.org/html/rfc8461) בתוקף וגם מדיניות [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- בתוקף [רשומות DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities).
- בתוקף [רשומות SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) ו - [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail).
- שיהיה לך מתאים [DMARC](https://en.wikipedia.org/wiki/DMARC) עבר ומדיניות או שימוש ב [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) לאימות. אם נעשה שימוש באימות DMARC, יש להגדיר את המדיניות ל- `דוחה` או `הסגר`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [שליחת SMTPS](https://en.wikipedia.org/wiki/SMTPS), בהנחה שנעשה שימוש ב - SMTP.
- תקני אבטחת אתר אינטרנט כגון:
    - [אבטחת תעבורה קפדנית של HTTP](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - שלמות [תת - מקור](https://en.wikipedia.org/wiki/Subresource_Integrity) אם מעמיסים דברים מדומיינים חיצוניים.
- חייב לתמוך בהצגה של [כותרות הודעות](https://en.wikipedia.org/wiki/Email#Message_header), מכיוון שזוהי תכונה משפטית חיונית כדי לקבוע אם הודעת דואר אלקטרוני היא ניסיון דיוג.

**המקרה הטוב ביותר:**

- תמיכה באימות חומרה, כלומר. U2F ו - [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn). U2F ו - WebAuthn מאובטחים יותר כאשר הם משתמשים במפתח פרטי המאוחסן בהתקן חומרה בצד הלקוח כדי לאמת אנשים, בניגוד לסוד משותף המאוחסן בשרת האינטרנט ובצד הלקוח בעת שימוש ב - TOTP. יתר על כן, U2F ו- WebAuthn עמידים יותר בפני דיוג מכיוון שתגובת האימות שלהם מבוססת על האימות [שם הדומיין](https://en.wikipedia.org/wiki/Domain_name).
- [אישור רשות ההסמכה של DNS (CAA) רשומת משאבים](https://tools.ietf.org/html/rfc6844) בנוסף לתמיכת DANE.
- יישום של [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), זה שימושי עבור אנשים שמפרסמים לרשימות דיוור [RFC8617](https://tools.ietf.org/html/rfc8617).
- תוכניות לחיפוש באגים ו/או תהליך גילוי - פגיעות מתואם.
- תקני אבטחת אתר אינטרנט כגון:
    - [מדיניות אבטחת תוכן (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### אמון

לא הייתם סומכים על הכספים שלכם למישהו שיש זהות מזויפת, אז למה לסמוך עליו עם הדוא"ל שלכם? אנו דורשים מהספקים המומלצים שלנו להיות פומביים לגבי הבעלות או המנהיגות שלהם. כמו כן, היינו רוצים לראות דיווחי שקיפות תכופים, במיוחד בכל הנוגע לאופן הטיפול בבקשות ממשלתיות.

**מינימום כדי לעמוד בדרישות:**

- מנהיגות ציבורית או בעלות.

**המקרה הטוב ביותר:**

- מנהיגות מול הציבור.
- דוחות שקיפות תכופים.

### שיווק

עם ספקי הדוא"ל אנו ממליצים לראות שיווק אחראי.

**מינימום כדי לעמוד בדרישות:**

- חייב לארח ניתוח עצמי (ללא Google Analytics, Adobe Analytics וכו'). האתר של הספק חייב גם לציית ל [DNT (לא לעקוב)](https://en.wikipedia.org/wiki/Do_Not_Track) למי שרוצה לבטל את הסכמתו.

אסור שיהיה שיווק שהוא חסר אחריות:

- טענות של "הצפנה בלתי שבירה " יש להשתמש בהצפנה מתוך כוונה שהיא לא תהיה סודית בעתיד כאשר הטכנולוגיה קיימת כדי לפצח אותה.
- ביצוע ערבויות של הגנה על 100% אנונימיות. כשמישהו טוען שמשהו הוא 100% זה אומר שאין ודאות לכישלון. אנחנו יודעים שאנשים יכולים בקלות להפוך את עצמם לאיאנונימיים במספר דרכים, למשל.:

    - שימוש חוזר במידע אישי, למשל. (חשבונות אימיילים, שמות בדויים ייחודיים וכו') שאליהם הם ניגשו ללא תוכנת אנונימיות (Tor, VPN וכו')
    - [טביעת אצבע של דפדפן](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**המקרה הטוב ביותר:**

- ברור וקל לקריאה. זה כולל דברים כמו, הגדרת 2FA, קליינט דוא"ל, OpenPGP וכו '.

### פונקציונליות נוספת

אמנם לא דרישות קפדניות, יש כמה גורמי נוחות או פרטיות אחרים שבדקנו בעת קביעת אילו ספקים להמליץ.
