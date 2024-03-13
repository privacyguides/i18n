---
title: "לקוחות אימייל"
icon: material/email-open
description: These email clients are privacy-respecting and support OpenPGP email encryption.
cover: email-clients.webp
---

רשימת ההמלצות שלנו מכילה לקוחות אימייל התומכים הן ב[OpenPGP](encryption.md#openpgp) והן באימות חזק כגון [הרשאת פתוחה ](https://en.wikipedia.org/wiki/OAuth)(OAuth). OAuth מאפשר לך להשתמש ב - [אימות רב - גורמי](basics/multi-factor-authentication.md) ולמנוע גניבת חשבון.

<details class="warning" markdown>
<summary>Email does not provide forward secrecy</summary>

When using end-to-end encryption (E2EE) technology like OpenPGP, email will still have [some metadata](email.md#email-metadata-overview) that is not encrypted in the header of the email.

OpenPGP also does not support [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), which means if either your or the recipient's private key is ever stolen, all previous messages encrypted with it will be exposed: [How do I protect my private keys?](basics/email-security.md) Consider using a medium that provides forward secrecy:

[Real-time Communication](real-time-communication.md ""){.md-button}

</details>

## חוצה פלטפורמות

### Thunderbird

<div class="admonition recommendation" markdown>

![Thunderbird logo](assets/img/email-clients/thunderbird.svg){ align=right }

**Thunderbird** is a free, open-source, cross-platform email, newsgroup, news feed, and chat (XMPP, IRC, Matrix) client developed by the Thunderbird community, and previously by the Mozilla Foundation.

[:octicons-home-16: Homepage](https://thunderbird.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/thunderbird){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.mozilla.org/products/thunderbird){ .card-link title=Documentation}
[:octicons-code-16:](https://hg.mozilla.org/comm-central){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://thunderbird.net)
- [:simple-apple: macOS](https://thunderbird.net)
- [:simple-linux: Linux](https://thunderbird.net)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.Thunderbird)

</details>

</div>

#### תצורה מומלצת

מומלץ לשנות חלק מהגדרות אלה כדי להפוך את Thunderbird לפרטי יותר.

ניתן למצוא אפשרויות אלה ב - :material-menu: ← **הגדרות** ← **פרטיות & אבטחה**.

##### תוכן אינטרנט

- [ ] בטל את הסימון  **זכור אתרים וקישורים שביקרתי**
- [ ] בטל את הסימון של **קבל קובצי Cookie מאתרים**

##### טלמטריה

- [ ] בטל את הסימון  **אפשר ל - Thunderbird לשלוח נתונים טכניים ונתוני אינטראקציה ל - Mozilla**

#### Thunderbird-user.js (מתקדם)

[`thunderbird-user.js`](https://github.com/HorlogeSkynet/thunderbird-user.js), היא קבוצה של אפשרויות תצורה שמטרתה להשבית כמה שיותר מתכונות הגלישה באינטרנט בתוך Thunderbird על מנת להקטין את שטח הפנים ולשמור על פרטיות. חלק מהשינויים הם backported מפרויקט [Arkenfox](https://github.com/arkenfox/user.js).

## ספציפית לפלטפורמה

### Apple Mail (macOS)

<div class="admonition recommendation" markdown>

![Apple Mail לוגו](assets/img/email-clients/applemail.png){ align=right }

**Apple Mail** כלול ב-macOS וניתן להרחיב אותו כך שתהיה לו תמיכה ב-OpenPGP עם [GPG Suite](encryption.md#gpg-suite), אשר מוסיפה את היכולת לשלוח מייל מוצפן PGP.

[:octicons-home-16: Homepage](https://support.apple.com/guide/mail/welcome/mac){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/en-ww){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/mail){ .card-link title=Documentation}

</details>

</div>

ל-Apple Mail יש את היכולת לטעון תוכן מרוחק ברקע או לחסום אותו לחלוטין ולהסתיר את כתובת ה-IP שלך משולחים ב-[macOS](https://support.apple.com/guide/mail/mlhl03be2866/mac) ו-[iOS](https://support.apple.com/guide/iphone/iphf084865c7/ios).

### Canary Mail (iOS)

<div class="admonition recommendation" markdown>

![Canary Mail לוגו](assets/img/email-clients/canarymail.svg){ align=right }

**Canary Mail** הוא לקוח אימייל בתשלום שנועד להפוך את ההצפנה מקצה לקצה לחלקה עם תכונות אבטחה כגון נעילת אפליקציה ביומטרית.

[:octicons-home-16: Homepage](https://canarymail.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://canarymail.io/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://canarymail.zendesk.com){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.canarymail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1236045954)
- [:simple-windows11: Windows](https://canarymail.io/downloads.html)

</details>

</div>

<details class="warning" markdown>
<summary>Warning</summary>

Canary Mail הוציאה רק לאחרונה לקוח של Windows ואנדרואיד, אם כי אנחנו לא מאמינים שהם יציבים כמו עמיתיהם של iOS ו-Mac.

</details>

Canary Mail הוא קוד סגור. אנו ממליצים על זה בגלל האפשרויות המעטות שיש עבור לקוחות אימייל ב-iOS התומכים ב-PGP E2EE.

### FairEmail (אנדרואיד)

<div class="admonition recommendation" markdown>

![FairEmail לוגו](assets/img/email-clients/fairemail.svg){ align=right }

**FairEmail** היא אפליקציית אימייל מינימלית בקוד פתוח, המשתמשת בסטנדרטים פתוחים (IMAP, SMTP, OpenPGP) עם צריכת נתונים וסוללה נמוכה.

[:octicons-home-16: Homepage](https://email.faircode.eu){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/M66B/FairEmail/blob/master/PRIVACY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/M66B/FairEmail/blob/master/FAQ.md){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/M66B/FairEmail){ .card-link title="Source Code" }
[:octicons-heart-16:](https://email.faircode.eu/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=eu.faircode.email)
- [:simple-github: GitHub](https://github.com/M66B/FairEmail/releases)

</details>

</div>

### GNOME Evolution (GNOME)

<div class="admonition recommendation" markdown>

![Evolution לוגו](assets/img/email-clients/evolution.svg){ align=right }

**Evolution** הוא יישום לניהול מידע אישי המספק פונקציונליות משולבת של דואר, לוחות שנה ופנקס כתובות. Evolution has extensive [documentation](https://help.gnome.org/users/evolution/stable) to help you get started.

[:octicons-home-16: Homepage](https://wiki.gnome.org/Apps/Evolution){ .md-button .md-button--primary }
[:octicons-eye-16:](https://wiki.gnome.org/Apps/Evolution/PrivacyPolicy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.gnome.org/users/evolution/stable){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.gnome.org/GNOME/evolution){ .card-link title="Source Code" }
[:octicons-heart-16:](https://gnome.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.gnome.Evolution)

</details>

</div>

### K -9 Mail (אנדרואיד)

<div class="admonition recommendation" markdown>

![K-9 Mail לוגו](assets/img/email-clients/k9mail.svg){ align=right }

**K-9 Mail** היא אפליקציית מייל עצמאית התומכת גם בתיבות דואר POP3 וגם IMAP, אך תומכת רק בדואר דואר עבור IMAP.

בעתיד, K-9 Mail יהיה [המותג הרשמי](https://k9mail.app/2022/06/13/K-9-Mail-and-Thunderbird.html) לקוח Thunderbird עבור אנדרואיד.

[:octicons-home-16: Homepage](https://k9mail.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://k9mail.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.k9mail.app){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/thundernest/k-9){ .card-link title="Source Code" }
[:octicons-heart-16:](https://k9mail.app/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.fsck.k9)
- [:simple-github: GitHub](https://github.com/thundernest/k-9/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

כשמשיבים למישהו ברשימת תפוצה, אפשרות ה"תשובה" עשויה לכלול גם את רשימת התפוצה. למידע נוסף ראה [thundernest/k-9 #3738](https://github.com/thundernest/k-9/issues/3738).

</div>

### Kontact (KDE)

<div class="admonition recommendation" markdown>

![Kontact לוגו](assets/img/email-clients/kontact.svg){ align=right }

**Kontact** הוא יישום מנהל מידע אישי (PIM) מפרויקט [KDE](https://kde.org). הוא מספק לקוח מייל, פנקס כתובות, מארגן ולקוח RSS.

[:octicons-home-16: Homepage](https://kontact.kde.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kde.org/privacypolicy-apps){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kontact.kde.org/users){ .card-link title=Documentation}
[:octicons-code-16:](https://invent.kde.org/pim/kmail){ .card-link title="Source Code" }
[:octicons-heart-16:](https://kde.org/community/donations){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-linux: Linux](https://kontact.kde.org/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.kde.kontact)

</details>

</div>

### Mailvelope (דפדפן)

<div class="admonition recommendation" markdown>

![Mailvelope לוגו](assets/img/email-clients/mailvelope.svg){ align=right }

**Mailvelope** היא תוסף דפדפן המאפשר החלפת מיילים מוצפנים בהתאם לתקן ההצפנה OpenPGP.

[:octicons-home-16: Homepage](https://mailvelope.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailvelope.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mailvelope.com/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mailvelope/mailvelope){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/mailvelope)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/mailvelope/kajibbejlbohfaggdiogboambcijhkke)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/mailvelope/dgcbddhdhjppfdfjpciagmmibadmoapc)

</details>

</div>

### NeoMutt (CLI)

<div class="admonition recommendation" markdown>

![NeoMutt לוגו](assets/img/email-clients/mutt.svg){ align=right }

**NeoMutt** הוא קורא דואר שורת פקודה בקוד פתוח (או MUA) עבור לינוקס ו-BSD. זה מזלג של [Mutt](https://en.wikipedia.org/wiki/Mutt_(email_client)) עם תכונות נוספות.

NeoMutt הוא לקוח מבוסס טקסט שיש לו עקומת למידה תלולה. עם זאת, זה מאוד להתאמה אישית.

[:octicons-home-16: Homepage](https://neomutt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://neomutt.org/guide){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/neomutt/neomutt){ .card-link title="Source Code" }
[:octicons-heart-16:](https://paypal.com/paypalme/russon){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-apple: macOS](https://neomutt.org/distro)
- [:simple-linux: Linux](https://neomutt.org/distro)

</details>

</div>

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

אנו עובדים על קביעת קריטריונים מוגדרים לכל קטע באתר שלנו, והדבר עשוי להשתנות. אם יש לך שאלות כלשהן לגבי הקריטריונים שלנו, אנא [שאל בפורום שלנו](https://discuss.privacyguides.net/latest) ואל תניח שלא שקלנו משהו כשהצענו את ההמלצות שלנו אם הוא לא רשום כאן. ישנם גורמים רבים שנחשבים ונדונים כאשר אנו ממליצים על פרויקט, ותיעוד כל אחד מהם הוא עבודה בתהליך.

</div>

### כישורים מינימליים

- אפליקציות שפותחו עבור מערכות הפעלה בקוד פתוח חייבות להיות בקוד פתוח.
- לא יכול לאסוף טלמטריה, או שיש דרך קלה להפוך את כל הטלמטריה ללא זמינה.
- חייב לתמוך בהצפנת הודעות OpenPGP.

### המקרה הטוב ביותר

הקריטריונים הטובים ביותר שלנו מייצגים את מה שהיינו רוצים לראות מהפרויקט המושלם בקטגוריה זו. ייתכן שההמלצות שלנו לא יכללו חלק מהפונקציונליות הזו או את כולה, אך אלו שכן כן עשויות לדרג גבוה יותר מאחרות בדף זה.

- צריך להיות קוד פתוח.
- צריך להיות חוצה פלטפורמות.
- אינו אוסף טלמטריה כברירת מחדל.
- צריך לתמוך ב - OpenPGP באופן מקורי, כלומר ללא הרחבות.
- יש לתמוך באחסון הודעות דואר אלקטרוני מוצפנות של OpenPGP באופן מקומי.
