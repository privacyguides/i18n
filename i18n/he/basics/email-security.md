---
meta_title: "מדוע אימייל אינו הבחירה הטובה ביותר לפרטיות ואבטחה - Privacy Guides"
title: אבטחת אימייל
icon: material/email
description: Email is insecure in many ways, and these are some of the reasons it isn't our top choice for secure communications.
---

אימייל הוא צורת תקשורת לא מאובטחת כברירת מחדל. You can improve your email security with tools such as OpenPGP, which add end-to-end encryption to your messages, but OpenPGP still has a number of drawbacks compared to encryption in other messaging applications.

כתוצאה מכך, האימייל משמש בצורה הטובה ביותר לקבלת הודעות אימייל עסקאות (כמו התראות, אימייל אימות, איפוסי סיסמה וכו') מהשירותים שאליהם אתה נרשם באופן מקוון, לא לתקשורת עם אחרים.

## סקירת הצפנת אימייל

הדרך הסטנדרטית להוסיף E2EE למיילים בין ספקי אימייל שונים היא באמצעות OpenPGP. There are different implementations of the OpenPGP standard, the most common being [GnuPG](../encryption.md#gnu-privacy-guard) and [OpenPGP.js](https://openpgpjs.org).

Even if you use OpenPGP, it does not support [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), which means if the private key of either you or the message recipient is ever stolen, all previous messages encrypted with it will be exposed. זו הסיבה שאנו ממליצים על [מסנג'רים מיידיים](../real-time-communication.md) אשר מיישמים סודיות קדימה על פני דואר אלקטרוני עבור הודעות פנים אל פנים במידת האפשר.

There is another standard which is popular with business called [S/MIME](https://en.wikipedia.org/wiki/S/MIME), however it requires a certificate issued from a [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (not all of them issue S/MIME certificates, and often a yearly payment is required). In some cases it is more usable than PGP because it has support in popular/mainstream email applications like Apple Mail, [Google Workplace](https://support.google.com/a/topic/9061730), and [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). However, S/MIME does not solve the issue of lack of forward secrecy, and isn't particularly more secure than PGP.

## What is the Web Key Directory standard?

The [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. Email clients which support WKD will ask the recipient's server for a key based on the email address' domain name. For example, if you emailed `jonah@privacyguides.org`, your email client would ask `privacyguides.org` for Jonah's OpenPGP key, and if `privacyguides.org` has a key for that account, your message would be automatically encrypted.

In addition to the [email clients we recommend](../email-clients.md) which support WKD, some webmail providers also support WKD. Whether *your own* key is published to WKD for others to use depends on your domain configuration. If you use an [email provider](../email.md#openpgp-compatible-services) which supports WKD, such as Proton Mail or Mailbox Mail, they can publish your OpenPGP key on their domain for you.

If you use your own custom domain, you will need to configure WKD separately. If you control your domain name, you can set up WKD regardless of your email provider. One easy way to do this is to use the "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" feature from the `keys.openpgp.org` server: Set a CNAME record on the `openpgpkey` subdomain of your domain pointed to `wkd.keys.openpgp.org`, then upload your key to [keys.openpgp.org](https://keys.openpgp.org). Alternatively, you can [self-host WKD on your own web server](https://wiki.gnupg.org/WKDHosting).

If you use a shared domain from a provider which doesn't support WKD, like `@gmail.com`, you won't be able to share your OpenPGP key with others via this method.

### אילו לקוחות אימייל תומכים ב - E2EE?

ספקי אימייל המאפשרים לך להשתמש בפרוטוקולי גישה סטנדרטיים כגון IMAP ו- SMTP יכולים לשמש עם כל אחד מ[קליינטי הדואר האלקטרוני שאנו ממליצים עליהם](../email-clients.md). Depending on the authentication method, this may lead to decreased security if either the provider or the email client does not support [OAuth](account-creation.md#sign-in-with-oauth) or a bridge application as [multifactor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### כיצד אוכל להגן על המפתחות הפרטיים שלי?

A smart card (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smart card and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smart card to avoid possibly exposing your private key to a compromised device.

## סקירה כללית של מטא נתונים בדוא"ל

Email metadata is stored in the [message header](https://en.wikipedia.org/wiki/Email#Message_header) of the email message and includes some visible headers that you may have seen such as `To`, `From`, `Cc`, `Date`, and `Subject`. יש גם מספר כותרות נסתרות שנכללות על ידי לקוחות דוא"ל וספקים רבים שיכולים לחשוף מידע על החשבון שלך.

תוכנת הלקוח עשויה להשתמש במטא נתונים של דוא"ל כדי להראות מי ההודעה ומאיזו שעה היא התקבלה. השרתים רשאים להשתמש בו כדי לקבוע לאן תישלח הודעת דוא"ל, בין [מטרות אחרות](https://en.wikipedia.org/wiki/Email#Message_header) שאינן תמיד שקופות.

### מי יכול לצפות במטא נתונים של דוא"ל?

Email metadata is protected from outside observers with [opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS), but it is still able to be seen by your email client software (or webmail) and any servers relaying the message from you to any recipients including your email provider. לפעמים שרתי דוא"ל ישתמשו גם בשירותי צד שלישי כדי להגן מפני תגובות זבל, שבדרך כלל יש להם גם גישה להודעות שלך.

### למה מטא נתונים לא יכולים להיות E2EE?

מטא נתונים של דואר אלקטרוני חיוניים לפונקציונליות הבסיסית ביותר של דואר אלקטרוני (מהיכן הוא הגיע ולאן הוא צריך ללכת). E2EE was not built into standard email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
