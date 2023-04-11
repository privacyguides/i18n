---
title: "קושחת הנתב"
icon: material/router-wireless
description: ניתן להשתמש במערכות הפעלה חלופיות אלה כדי לאבטח את הנתב או נקודת הגישה ל-Wi-Fi.
---

להלן מספר מערכות הפעלה חלופיות, שניתן להשתמש בהן בנתבים, נקודות גישה ל-Wi-Fi וכו'.

## OpenWrt

!!! recommendation

    ![לוגו OpenWrt](assets/img/router/openwrt.svg#only-light){ align=right }
    ![לוגו OpenWrt](assets/img/router/openwrt-dark.svg#only-dark){ align=right }
    
    **OpenWrt** היא מערכת הפעלה מבוססת לינוקס; הוא משמש בעיקר במכשירים משובצים לניתוב תעבורת רשת. זה כולל util-linux, uClibc ו-BusyBox. כל הרכיבים עברו אופטימיזציה עבור נתבים ביתיים.
    
    [:octicons-home-16: דף הבית](https://openwrt.org){ .md-button .md-button--primary }
    [:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title=תיעוד}
    [:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="קוד מקור" }
    [:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=לתרומה }

אתה יכול לעיין ב[טבלת החומרה](https://openwrt.org/toh/start) של OpenWrt כדי לבדוק אם המכשיר שלך נתמך.

## OPNsense

!!! recommendation

    ![OPNsense לוגו](assets/img/router/opnsense.svg){ align=right }
    
    **OPNsense** היא חומת אש ופלטפורמת ניתוב מבוססת קוד פתוח, מבוססת FreeBSD, המשלבת תכונות מתקדמות רבות כגון עיצוב תעבורה, איזון עומסים ויכולות VPN, עם תכונות רבות נוספות הזמינות בצורה של תוספים. OPNsense נפוץ כחומת אש היקפית, נתב, נקודת גישה אלחוטית, שרת DHCP, שרת DNS ונקודת קצה VPN.
    
    [:octicons-home-16: דף הבית](https://opnsense.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title=תיעוד}
    [:octicons-code-16:](https://github.com/opnsense){ .card-link title="קוד מקור" }
    [:octicons-heart-16:](https://opnsense.org/donate/){ .card-link title=לתרומה }

OPNsense פותחה במקור כמזלג של [pfSense](https://en.wikipedia.org/wiki/PfSense), ושני הפרויקטים ידועים לפי הפצות חומת אש חינמיות ואמינות המציעות ציוד דומה נמצא רק בחומות אש מסחריות יקרות. הושק בשנת 2015, מפתחי OPNsense [ציטטו](https://docs.opnsense.org/history/thefork.html) מספר בעיות אבטחה ואיכות ב-pfSense שלדעתם היו נחוצות חלק מהפרויקט, כמו גם חששות לגבי רכישת הרוב של Netgate של pfSense והכיוון העתידי של פרויקט pfSense.

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

!!! example "חלק זה הוא חדש"

    אנו עובדים על קביעת קריטריונים מוגדרים לכל קטע באתר שלנו, והדבר עשוי להשתנות. אם יש לך שאלות כלשהן לגבי הקריטריונים שלנו, אנא [שאל בפורום שלנו](https://discuss.privacyguides.net/latest) ואל תניח שלא שקלנו משהו כשהצענו את ההמלצות שלנו אם הוא לא רשום כאן. ישנם גורמים רבים שנחשבים ונדונים כאשר אנו ממליצים על פרויקט, ותיעוד כל אחד מהם הוא עבודה בתהליך.

- חייב להיות קוד פתוח.
- חייב לקבל עדכונים שוטפים.
- חייב לתמוך במגוון רחב של חומרה.
