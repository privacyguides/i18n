---
title: "שיתוף וסנכרון קבצים"
icon: material/share-variant
description: גלה כיצד לשתף את הקבצים שלך באופן פרטי בין המכשירים שלך, עם החברים והמשפחה שלך, או באופן אנונימי באינטרנט.
cover: file-sharing.webp
---

גלה כיצד לשתף את הקבצים שלך באופן פרטי בין המכשירים שלך, עם החברים והמשפחה שלך, או באופן אנונימי באינטרנט.

## שיתוף קבצים

### Send

<div class="admonition recommendation" markdown>

![Send logo](assets/img/file-sharing-sync/send.svg){ align=right }

**Send** is a fork of Mozilla's discontinued Firefox Send service which allows you to send files to others with a link. קבצים מוצפנים במכשיר שלך כך שלא ניתן לקרוא אותם על ידי השרת, והם יכולים להיות מוגנים באמצעות סיסמה. The maintainer of Send hosts a [public instance](https://send.vis.ee). אפשר להשתמש במועדים ציבוריים אחרים, או לארח לשלוח את עצמכם.

[:octicons-home-16: דף הבית](https://send.vis.ee){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="מופעים ציבוריים"}
[:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title=תיעוד}
[:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="קוד מקור" }
[:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title=לתרומה }

</details>

</div>

ניתן להשתמש ב- Send דרך ממשק האינטרנט שלו או דרך [ffsend](https://github.com/timvisee/ffsend) CLI. אם אתה מכיר את שורת הפקודה ושולח קבצים לעתים קרובות, אנו ממליצים להשתמש בלקוח ה-CLI כדי להימנע מהצפנה מבוססת JavaScript. אתה יכול לציין את הדגל `--host` כדי להשתמש בשרת ספציפי:

```bash
ffsend upload -- host https://send.vis.ee/ FILE
```

### OnionShare

<div class="admonition recommendation" markdown>

![OnionShare לוגו](assets/img/file-sharing-sync/onionshare.svg){ align=right }

**OnionShare** הוא כלי קוד פתוח המאפשר לך לשתף בצורה מאובטחת ואנונימית קובץ בכל גודל. זה עובד על ידי הפעלת שרת אינטרנט נגיש כשירות Tor onion, עם כתובת URL בלתי ניתנת לניחוש שתוכל לשתף עם הנמענים כדי להוריד או לשלוח קבצים.

[:octicons-home-16: Homepage](https://onionshare.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://docs.onionshare.org){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://onionshare.org/#download)
- [:simple-apple: macOS](https://onionshare.org/#download)
- [:simple-linux: Linux](https://onionshare.org/#download)

</details>

</div>

### קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

- אסור לאחסן נתונים מפוענחים בשרת מרוחק.
- חייבת להיות תוכנת קוד פתוח.
- חייב להיות לקוחות עבור Linux, macOS ו-Windows; או בעלי ממשק אינטרנט.

## FreedomBox

<div class="admonition recommendation" markdown>

![FreedomBox לוגו](assets/img/file-sharing-sync/freedombox.svg){ align=right }

**FreedomBox** היא מערכת הפעלה המיועדת להפעלה על [מחשב עם לוח יחיד (SBC)](https://en.wikipedia.org/wiki/Single-board_computer). המטרה היא להקל על הגדרת יישומי שרת שאולי תרצה לארח בעצמך.

[:octicons-home-16: Homepage](https://freedombox.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title=Documentation}
[:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="Source Code" }
[:octicons-heart-16:](https://freedomboxfoundation.org/donate){ .card-link title=Contribute }

</details>

</div>

## סנכרון קבצים

### Nextcloud (שרת-לקוח)

<div class="admonition recommendation" markdown>

![Nextcloud לוגו](assets/img/productivity/nextcloud.svg){ align=right }

**Nextcloud** היא חבילה של תוכנות שרת-לקוח חינמיות וקוד פתוח ליצירת שירותי אירוח קבצים משלך בשרת פרטי שאתה שולט בו.

[:octicons-home-16: Homepage](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Source Code" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
- [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
- [:simple-windows11: Windows](https://nextcloud.com/install/#install-clients)
- [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
- [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

אנו לא ממליצים להשתמש ב-[E2EE App](https://apps.nextcloud.com/apps/end_to_end_encryption) עבור Nextcloud מכיוון שהיא עלולה להוביל לאובדן נתונים; זה מאוד ניסיוני ולא איכות ייצור.

</div>

### Syncthing (P2P)

<div class="admonition recommendation" markdown>

![Syncthing לוגו](assets/img/file-sharing-sync/syncthing.svg){ align=right }

**Syncthing** הוא כלי עזר רציף לסנכרון קבצים עמית לעמית בקוד פתוח. הוא משמש לסנכרון קבצים בין שני מכשירים או יותר ברשת המקומית או באינטרנט. Syncthing אינו משתמש בשרת מרכזי; הוא משתמש ב-[Block Exchange Protocol](https://docs.syncthing.net/specs/bep-v1.html#bep-v1) כדי להעביר נתונים בין מכשירים. כל הנתונים מוצפנים באמצעות TLS.

[:octicons-home-16: Homepage](https://syncthing.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.syncthing.net){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/syncthing){ .card-link title="Source Code" }
[:octicons-heart-16:](https://syncthing.net/donations){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nutomic.syncthingandroid)
- [:simple-windows11: Windows](https://syncthing.net/downloads)
- [:simple-apple: macOS](https://syncthing.net/downloads)
- [:simple-linux: Linux](https://syncthing.net/downloads)
- [:simple-freebsd: FreeBSD](https://syncthing.net/downloads)

</details>

</div>

<!-- markdownlint-disable-next-line -->
### קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

#### דרישות מינימליות

- חייב לא לדרוש שרת מרוחק/ענן של צד שלישי.
- חייבת להיות תוכנת קוד פתוח.
- חייב להיות לקוחות עבור Linux, macOS ו-Windows; או בעלי ממשק אינטרנט.

#### המקרה הטוב ביותר

הקריטריונים הטובים ביותר שלנו מייצגים את מה שהיינו רוצים לראות מהפרויקט המושלם בקטגוריה זו. ייתכן שההמלצות שלנו לא יכללו חלק מהפונקציונליות הזו או את כולה, אך אלו שכן כן עשויות לדרג גבוה יותר מאחרות בדף זה.

- יש לו לקוחות ניידים עבור iOS ואנדרואיד, שלפחות תומכים בתצוגה מקדימה של מסמכים.
- תומך בגיבוי תמונות מ-iOS ואנדרואיד, ותומך באופן אופציונלי בסנכרון קבצים/תיקיות באנדרואיד.
