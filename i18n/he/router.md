---
title: "קושחת הנתב"
icon: material/router-wireless
description: Alternative operating systems for securing your router or Wi-Fi access point.
cover: router.webp
---

להלן מספר מערכות הפעלה חלופיות, שניתן להשתמש בהן בנתבים, נקודות גישה ל-Wi-Fi וכו'.

## OpenWrt

<div class="admonition recommendation" markdown>

![לוגו OpenWrt](assets/img/router/openwrt.svg#only-light){ align=right }
![לוגו OpenWrt](assets/img/router/openwrt-dark.svg#only-dark){ align=right }

**OpenWrt** היא מערכת הפעלה מבוססת לינוקס; הוא משמש בעיקר במכשירים משובצים לניתוב תעבורת רשת. זה כולל util-linux, uClibc ו-BusyBox. כל הרכיבים עברו אופטימיזציה עבור נתבים ביתיים.

[:octicons-home-16: דף הבית](https://openwrt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title=תיעוד}
[:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="קוד מקור" }
[:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=לתרומה }

</details>

</div>

אתה יכול לעיין ב[טבלת החומרה](https://openwrt.org/toh/start) של OpenWrt כדי לבדוק אם המכשיר שלך נתמך.

## OPNsense

<div class="admonition recommendation" markdown>

![OPNsense לוגו](assets/img/router/opnsense.svg){ align=right }

**OPNsense** היא חומת אש ופלטפורמת ניתוב מבוססת קוד פתוח, מבוססת FreeBSD, המשלבת תכונות מתקדמות רבות כגון עיצוב תעבורה, איזון עומסים ויכולות VPN, עם תכונות רבות נוספות הזמינות בצורה של תוספים. OPNsense נפוץ כחומת אש היקפית, נתב, נקודת גישה אלחוטית, שרת DHCP, שרת DNS ונקודת קצה VPN.

[:octicons-home-16: Homepage](https://opnsense.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/opnsense){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opnsense.org/donate){ .card-link title=Contribute }

</details>

</div>

OPNsense פותחה במקור כמזלג של [pfSense](https://en.wikipedia.org/wiki/PfSense), ושני הפרויקטים ידועים לפי הפצות חומת אש חינמיות ואמינות המציעות ציוד דומה נמצא רק בחומות אש מסחריות יקרות. הושק בשנת 2015, מפתחי OPNsense [ציטטו](https://docs.opnsense.org/history/thefork.html) מספר בעיות אבטחה ואיכות ב-pfSense שלדעתם היו נחוצות חלק מהפרויקט, כמו גם חששות לגבי רכישת הרוב של Netgate של pfSense והכיוון העתידי של פרויקט pfSense.

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

- חייב להיות קוד פתוח.
- חייב לקבל עדכונים שוטפים.
- חייב לתמוך במגוון רחב של חומרה.
