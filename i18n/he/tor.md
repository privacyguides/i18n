---
meta_title: "דפדפן ורשת Tor: גלישה אנונימית באינטרנט - Privacy Guides"
title: "רשת טור (Tor Network)"
icon: simple/torproject
description: הגן על הגלישה שלך באינטרנט מעיניים סקרניות על ידי שימוש ברשת Tor, רשת מאובטחת שעוקפת צנזורה.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": יישום תוכנה
    name: דפדפן Tor
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
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

[:octicons-home-16:](https://torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

Tor פועלת על ידי ניתוב תעבורת האינטרנט שלך דרך אותם שרתים המופעלים על ידי מתנדבים, במקום ליצור חיבור ישיר לאתר שבו אתה מנסה לבקר. זה מטשטש מהיכן מגיעה התעבורה, ואף שרת בנתיב החיבור לא מסוגל לראות את הנתיב המלא של המקום ממנו מגיעה התנועה והולכת, כלומר אפילו השרתים שבהם אתה משתמש כדי להתחבר לא יכולים לשבור את האנונימיות שלך.

[סקירת Tor מפורטת :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## התחברות ל - Tor

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Before connecting to Tor, please ensure you've read our [overview](advanced/tor-overview.md) on what Tor is and how to connect to it safely. We often recommend connecting to Tor through a trusted [VPN provider](vpn.md), but you have to do so **properly** to avoid decreasing your anonymity.

</div>

ישנן מגוון דרכים שלך להתחבר לרשת Tor מהמכשיר, הנפוץ ביותר הוא דפדפן **Tor**, נגזרת של Firefox המיועד לגלישה אנונימית למחשבים שולחניים ואנדרואיד.

Some of these apps are better than others, and again making a determination comes down to your threat model. If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using apps like [Orbot](#orbot) or mobile browser apps to access the Tor network is probably fine. Increasing the number of people who use Tor on an everyday basis helps reduce the bad stigma of Tor, and lowers the quality of "lists of Tor users" that ISPs and governments may compile.

If more complete anonymity is paramount to your situation, you should **only** be using the desktop Tor Browser client, ideally in a [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os) configuration. Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

### דפדפן Tor

<div class="admonition recommendation" markdown>

![Tor Browser לוגו](assets/img/browsers/tor.svg){ align=right }

**דפדפן Tor** הוא הבחירה אם אתה זקוק לאנונימיות, מכיוון שהוא מספק לך גישה לרשת Tor ולגשרים, והוא כולל הגדרות ברירת מחדל והרחבות המוגדרות אוטומטית לפי רמות האבטחה המוגדרות כברירת מחדל: *סטנדרטי*, *בטוח יותר * ו*הבטוח ביותר*.

[:octicons-home-16: Homepage](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:simple-windows11: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

אתה צריך **לעולם לא** להתקין הרחבות נוספות בדפדפן Tor או לערוך את הגדרות `about:config`, כולל אלו שאנו מציעים עבור Firefox. הרחבות דפדפן והגדרות לא סטנדרטיות גורמים לך להתבלט על פני אחרים ברשת Tor, ובכך להקל על [טביעת אצבע](https://support.torproject.org/glossary/browser-fingerprinting) של הדפדפן שלך.

</div>

דפדפן Tor נועד למנוע טביעת אצבע, או לזהות אותך על סמך תצורת הדפדפן שלך. Therefore, it is imperative that you do **not** modify the browser beyond the default [security levels](https://tb-manual.torproject.org/security-settings).

In addition to installing Tor Browser on your computer directly, there are also operating systems designed specifically to connect to the Tor network such as [Whonix](desktop.md#whonix) on [Qubes OS](desktop.md#qubes-os), which provide even greater security and protections than the standard Tor Browser alone.

### Orbot

<div class="admonition recommendation" markdown>

![Orbot לוגו](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** הוא Tor VPN בחינם לסמארטפונים שמנתב תעבורה מכל אפליקציה במכשיר שלך דרך רשת Tor.

[:octicons-home-16: Homepage](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

</details>

</div>

המלצנו בעבר להפעיל את העדפת *בודד כתובת יעד* בהגדרות Orbot. בעוד שהגדרה זו יכולה לשפר באופן תיאורטי את הפרטיות על ידי אכיפת השימוש במעגל אחר עבור כל כתובת IP שאתה מתחבר אליה, היא אינה מספקת יתרון מעשי לרוב היישומים (במיוחד גלישה באינטרנט), עלולה לבוא עם עונש משמעותי בביצועים ומגבירה העומס על רשת Tor. אנחנו לא ממליצים עוד לשנות הגדרה זו מערך ברירת המחדל שלה, אלא אם כן אתה יודע שצריך.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Tips for Android</p>

Orbot יכול לבצע שרת proxy של אפליקציות בודדות אם הם תומכים ב-SOCKS או HTTP proxy. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN killswitch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

Orbot מיושן לעתים קרובות ב[מאגר F-Droid](https://guardianproject.info/fdroid) ו- [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android), אז שקול להוריד ישירות מ[מאגר GitHub](https://github.com/guardianproject/orbot/releases) במקום זאת.

כל הגרסאות חתומות באמצעות אותה חתימה ולכן הן צריכות להיות תואמות זו לזו.

</div>

### Onion Browser

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** is an open-source browser that lets you browse the web anonymously over the Tor network on iOS devices and is endorsed by the [Tor Project](https://support.torproject.org/glossary/onion-browser).

[:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

## ממסרים וגשרים

### Snowflake

<div class="admonition recommendation" markdown>

![Snowflake לוגו](assets/img/browsers/snowflake.svg#only-light){ align=right }
![Snowflake לוגו](assets/img/browsers/snowflake-dark.svg#only-dark){ align=right }

**Snowflake** מאפשר לך לתרום רוחב פס לפרויקט Tor על ידי הפעלת "Snowflake proxy" בתוך הדפדפן שלך.

אנשים שמצונזרים יכולים להשתמש בפרוקסי של Snowflake כדי להתחבר לרשת Tor. Snowflake היא דרך מצוינת לתרום לרשת גם אם אין לך את הידע הטכני להפעיל ממסר Tor או גשר.

[:octicons-home-16: Homepage](https://snowflake.torproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

</details>

</div>

אתה יכול לאפשר Snowflake בדפדפן שלך על ידי פתיחתו בכרטיסייה אחרת והפעלת המתג. אתה יכול להשאיר אותו פועל ברקע בזמן שאתה גולש כדי לתרום את החיבור שלך. אנו לא ממליצים להתקין Snowflake כהרחבה של דפדפן; הוספת הרחבות של צד שלישי יכולה להגדיל את משטח ההתקפה שלך.

[הפעל Snowflake בדפדפן שלך :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html ""){.md-button}

Snowflake אינו מגדיל את פרטיותך בשום צורה, ואינו משמש לחיבור לרשת Tor בתוך הדפדפן האישי שלך. עם זאת, אם חיבור האינטרנט שלך אינו מצונזר, עליך לשקול להפעיל אותו כדי לעזור לאנשים ברשתות מצונזרות להשיג פרטיות טובה יותר בעצמם. אין צורך לדאוג לאילו אתרים אנשים ניגשים דרך ה-proxy שלך - כתובת ה-IP הגלויה של הגלישה שלהם תתאים לצומת היציאה של Tor, לא שלך.

הפעלת פרוקסי של Snowflake היא בסיכון נמוך, אפילו יותר מהפעלת ממסר Tor או גשר שהם כבר מאמצים לא מסוכנים במיוחד. עם זאת, היא עדיין עושה תעבורת פרוקסי דרך הרשת שלך, מה שיכול להשפיע במובנים מסוימים, במיוחד אם הרשת שלך מוגבלת ברוחב הפס. ודא שאתה מבין [איך Snowflake עובד](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) לפני שתחליט אם להפעיל פרוקסי.

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) and [Whonix's Stream Isolation documentation](https://whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
