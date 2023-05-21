---
meta_title: "דפדפן ורשת Tor: גלישה אנונימית באינטרנט - Privacy Guides"
title: "רשת טור (Tor Network)"
icon: simple/torproject
description: הגן על הגלישה שלך באינטרנט מעיניים סקרניות על ידי שימוש ברשת Tor, רשת מאובטחת שעוקפת צנזורה.
cover: tor.png
schema:
  - 
    "@context": http://schema.org
    "@type": יישום תוכנה
    name: דפדפן Tor
    image: /assets/img/browsers/tor.svg
    url: https://www.torproject.org
    sameAs: https://en.wikipedia.org/wiki/Tor_(network)
    applicationCategory: דפדפן אינטרנט
    operatingSystem:
      - ווינדוס
      - macOS
      - לינוקס
      - אנדרואיד
    subjectOf:
      "@type": עמוד אינטרנט
      url: "./"
---

![Tor logo](assets/img/self-contained-networks/tor.svg){ align=right }

הרשת **Tor** היא קבוצה של שרתים המופעלים בהתנדבות המאפשרת לך להתחבר בחינם ולשפר את הפרטיות והאבטחה שלך באינטרנט. אנשים וארגונים יכולים גם לשתף מידע על גבי רשת Tor עם ".onion hidden services" מבלי לפגוע בפרטיותם. מכיוון שקשה לחסום ולעקוב אחר תעבורת Tor, Tor הוא כלי יעיל לעקוף צנזורה.

[:octicons-home-16:](https://www.torproject.org){ .card-link title=דף הבית }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="שירות בצל" }
[:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=תיעוד}
[:octicons-code-16:](https://gitweb.torproject.org/tor.git){ .card-link title="קוד מקור" }
[:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=לתרומה }

Tor פועלת על ידי ניתוב תעבורת האינטרנט שלך דרך אותם שרתים המופעלים על ידי מתנדבים, במקום ליצור חיבור ישיר לאתר שבו אתה מנסה לבקר. זה מטשטש מהיכן מגיעה התעבורה, ואף שרת בנתיב החיבור לא מסוגל לראות את הנתיב המלא של המקום ממנו מגיעה התנועה והולכת, כלומר אפילו השרתים שבהם אתה משתמש כדי להתחבר לא יכולים לשבור את האנונימיות שלך.

[סקירת Tor מפורטת :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## התחברות ל - Tor

ישנן מגוון דרכים שלך להתחבר לרשת Tor מהמכשיר, הנפוץ ביותר הוא דפדפן **Tor**, נגזרת של Firefox המיועד לגלישה אנונימית למחשבים שולחניים ואנדרואיד. בנוסף לאפליקציות המפורטות למטה, יש גם מערכות הפעלה שתוכננו במיוחד להתחבר לרשת Tor כגון [Whonix](desktop.md#whonix) ב-[Qubes OS](desktop.md#qubes-os), המספקות אבטחה והגנות גבוהות עוד יותר מאשר דפדפן Tor הרגיל.

### דפדפן Tor

!!! recommendation

    ![Tor Browser לוגו](assets/img/browsers/tor.svg){ align=right }
    
    **דפדפן Tor** הוא הבחירה אם אתה זקוק לאנונימיות, מכיוון שהוא מספק לך גישה לרשת Tor ולגשרים, והוא כולל הגדרות ברירת מחדל והרחבות המוגדרות אוטומטית לפי רמות האבטחה המוגדרות כברירת מחדל: *סטנדרטי*, *בטוח יותר * ו*הבטוח ביותר*.
    
    [:octicons-home-16: דף הבית](https://www.torproject.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="שירות בצל" }
    [:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=תיעוד }
    [:octicons-code-16:](https://gitweb.torproject.org/tor-browser.git/){ .card-link title="קוד מקור" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=לתרומה }
    
    ??? downloads "הורדות"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
        - [:simple-android: אנדרואיד](https://www.torproject.org/download/#android)
        - [:simple-windows11: ווינדוס](https://www.torproject.org/download/)
        - [:simple-apple: macOS](https://www.torproject.org/download/)
        - [:simple-linux: לינוקס](https://www.torproject.org/download/)

!!! danger "סַכָּנָה"

    אתה צריך **לעולם לא** להתקין הרחבות נוספות בדפדפן Tor או לערוך את הגדרות `about:config`, כולל אלו שאנו מציעים עבור Firefox. הרחבות דפדפן והגדרות לא סטנדרטיות גורמים לך להתבלט על פני אחרים ברשת Tor, ובכך להקל על [טביעת אצבע](https://support.torproject.org/glossary/browser-fingerprinting) של הדפדפן שלך.

דפדפן Tor נועד למנוע טביעת אצבע, או לזהות אותך על סמך תצורת הדפדפן שלך. לכן, זה הכרחי כי אתה עושה **לא** לשנות את הדפדפן מעבר ברירת המחדל [רמות אבטחה](https://tb-manual.torproject.org/security-settings/).

### Orbot

!!! recommendation

    ![Orbot לוגו](assets/img/self-contained-networks/orbot.svg){ align=right }
    
    **Orbot** הוא Tor VPN בחינם לסמארטפונים שמנתב תעבורה מכל אפליקציה במכשיר שלך דרך רשת Tor.
    
    [:octicons-home-16: דף הבית](https://orbot.app/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="מדיניות פרטיות" }
    [:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
    [:octicons-code-16:](https://orbot.app/code){ .card-link title="קוד מקור" }
    [:octicons-heart-16:](https://orbot.app/donate){ .card-link title=לתרומה }
    
    ??? downloads "הורדות"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/orbot/id1609461599)
        - [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

המלצנו בעבר להפעיל את העדפת *בודד כתובת יעד* בהגדרות Orbot. בעוד שהגדרה זו יכולה לשפר באופן תיאורטי את הפרטיות על ידי אכיפת השימוש במעגל אחר עבור כל כתובת IP שאתה מתחבר אליה, היא אינה מספקת יתרון מעשי לרוב היישומים (במיוחד גלישה באינטרנט), עלולה לבוא עם עונש משמעותי בביצועים ומגבירה העומס על רשת Tor. אנחנו לא ממליצים עוד לשנות הגדרה זו מערך ברירת המחדל שלה, אלא אם כן אתה יודע שצריך.[^1]

!!! tip "טיפים עבור אנדרואיד"

    Orbot יכול לבצע שרת proxy של אפליקציות בודדות אם הם תומכים ב-SOCKS או HTTP proxy. זה יכול גם לספק את כל חיבורי הרשת שלך באמצעות [VpnService](https://developer.android.com/reference/android/net/VpnService) וניתן להשתמש בו עם מתג ה-VPN ב-:gear: **הגדרות** → * *רשת & אינטרנט** → **VPN** → :gear: → **חסום חיבורים ללא VPN**.
    
    Orbot מיושן לעתים קרובות ב[מאגר F-Droid](https://guardianproject.info/fdroid) ו- [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android), אז שקול להוריד ישירות מ[מאגר GitHub](https://github.com/guardianproject/orbot/releases) במקום זאת.
    
    כל הגרסאות חתומות באמצעות אותה חתימה ולכן הן צריכות להיות תואמות זו לזו.

## ממסרים וגשרים

### Snowflake

!!! recommendation

    ![Snowflake לוגו](assets/img/browsers/snowflake.svg#only-light){ align=right }
    ![Snowflake לוגו](assets/img/browsers/snowflake-dark.svg#only-dark){ align=right }
    
    **Snowflake** מאפשר לך לתרום רוחב פס לפרויקט Tor על ידי הפעלת "Snowflake proxy" בתוך הדפדפן שלך.
    
    אנשים שמצונזרים יכולים להשתמש בפרוקסי של Snowflake כדי להתחבר לרשת Tor. Snowflake היא דרך מצוינת לתרום לרשת גם אם אין לך את הידע הטכני להפעיל ממסר Tor או גשר.
    
    [:octicons-home-16: דף הבית](https://snowflake.torproject.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=תיעוד}
    [:octicons-code-16:](https://gitweb.torproject.org/pluggable-transports/snowflake.git/){ .card-link title="קוד מקור" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=לתרומה }

אתה יכול לאפשר Snowflake בדפדפן שלך על ידי פתיחתו בכרטיסייה אחרת והפעלת המתג. אתה יכול להשאיר אותו פועל ברקע בזמן שאתה גולש כדי לתרום את החיבור שלך. אנו לא ממליצים להתקין Snowflake כהרחבה של דפדפן; הוספת הרחבות של צד שלישי יכולה להגדיל את משטח ההתקפה שלך.

[הפעל Snowflake בדפדפן שלך :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html ""){.md-button}

Snowflake אינו מגדיל את פרטיותך בשום צורה, ואינו משמש לחיבור לרשת Tor בתוך הדפדפן האישי שלך. עם זאת, אם חיבור האינטרנט שלך אינו מצונזר, עליך לשקול להפעיל אותו כדי לעזור לאנשים ברשתות מצונזרות להשיג פרטיות טובה יותר בעצמם. אין צורך לדאוג לאילו אתרים אנשים ניגשים דרך ה-proxy שלך - כתובת ה-IP הגלויה של הגלישה שלהם תתאים לצומת היציאה של Tor, לא שלך.

הפעלת פרוקסי של Snowflake היא בסיכון נמוך, אפילו יותר מהפעלת ממסר Tor או גשר שהם כבר מאמצים לא מסוכנים במיוחד. עם זאת, היא עדיין עושה תעבורת פרוקסי דרך הרשת שלך, מה שיכול להשפיע במובנים מסוימים, במיוחד אם הרשת שלך מוגבלת ברוחב הפס. ודא שאתה מבין [איך Snowflake עובד](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) לפני שתחליט אם להפעיל פרוקסי.

[^1]: ההגדרה `IsolateDestAddr` נדונה ב [רשימת התפוצה של תור](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) ו-[Whonix's Stream Isolation documentation](https://www.whonix.org/wiki/Stream_Isolation), שבו שני הפרויקטים מצביעים על כך שזו בדרך כלל לא גישה טובה עבור רוב האנשים.
