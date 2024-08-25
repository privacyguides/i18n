---
title: "שיתוף וסנכרון קבצים"
icon: material/share-variant
description: גלה כיצד לשתף את הקבצים שלך באופן פרטי בין המכשירים שלך, עם החברים והמשפחה שלך, או באופן אנונימי באינטרנט.
cover: file-sharing.webp
---

<small>Protects against the following threat(s):</small>

- [:material-server-network: ספקי שירות](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

גלה כיצד לשתף את הקבצים שלך באופן פרטי בין המכשירים שלך, עם החברים והמשפחה שלך, או באופן אנונימי באינטרנט.

## שיתוף קבצים

If you have already use [Proton Drive](cloud.md#proton-drive)[^1] or have a [Bitwarden](passwords.md#bitwarden) Premium[^2] subscription, consider using the file sharing capabilities that they each offer, both of which use end-to-end encryption. Otherwise, the standalone options listed here ensure that the files you share are not read by a remote server.

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

![OnionShare logo](assets/img/file-sharing-sync/onionshare.svg){ align=right }

**OnionShare** is an open-source tool that lets you securely and [:material-incognito: anonymously](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } share a file of any size. זה עובד על ידי הפעלת שרת אינטרנט נגיש כשירות Tor onion, עם כתובת URL בלתי ניתנת לניחוש שתוכל לשתף עם הנמענים כדי להוריד או לשלוח קבצים.

[:octicons-home-16: Homepage](https://onionshare.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://docs.onionshare.org){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://onionshare.org/#download)
- [:simple-apple: macOS](https://onionshare.org/#download)
- [:simple-linux: Linux](https://onionshare.org/#download)

</details>

</div>

OnionShare provides the option to connect via [Tor bridges](https://docs.onionshare.org/2.6.2/en/tor.html#automatic-censorship-circumvention) to circumvent [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}.

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

![Nextcloud logo](assets/img/document-collaboration/nextcloud.svg){ align=right }

**Nextcloud** is a suite of free and open-source client-server software for creating your own file hosting services on a private server you control.

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
- [:fontawesome-brands-windows: Windows](https://nextcloud.com/install/#install-clients)
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
- [:fontawesome-brands-windows: Windows](https://syncthing.net/downloads)
- [:simple-apple: macOS](https://syncthing.net/downloads)
- [:simple-linux: Linux](https://syncthing.net/downloads)
- [:simple-freebsd: FreeBSD](https://syncthing.net/downloads)

</details>

</div>

### קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

#### דרישות מינימליות

- חייב לא לדרוש שרת מרוחק/ענן של צד שלישי.
- חייבת להיות תוכנת קוד פתוח.
- חייב להיות לקוחות עבור Linux, macOS ו-Windows; או בעלי ממשק אינטרנט.

#### המקרה הטוב ביותר

הקריטריונים הטובים ביותר שלנו מייצגים את מה שהיינו רוצים לראות מהפרויקט המושלם בקטגוריה זו. ייתכן שההמלצות שלנו לא יכללו חלק מהפונקציונליות הזו או את כולה, אך אלו שכן כן עשויות לדרג גבוה יותר מאחרות בדף זה.

- Should have mobile clients for iOS and Android which at least support document previews.
- Should support photo backups from iOS and Android, and optionally support file/folder sync on Android.

[^1]: Proton Drive allows you to [share files or folders](https://proton.me/support/drive-shareable-link) by generating a shareable public link or sending a unique link to a designated email address. Public links can be protected with a password, set to expire, and completely revoked, while links shared via email can have custom permissions and be similarly revoked. Per Proton Drive's [privacy policy](https://proton.me/drive/privacy-policy), file contents, file and folder names, and thumbnail previews are end-to-end encrypted.
[^2]: With a [premium](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans) subscription, [Bitwarden Send](https://bitwarden.com/products/send) allows you to share files and text securely with [end-to-end encryption](https://bitwarden.com/help/send-encryption). A [password](https://bitwarden.com/help/send-privacy/#send-passwords) can be required along with the Send link. Bitwarden Send also features [automatic deletion](https://bitwarden.com/help/send-lifespan).
