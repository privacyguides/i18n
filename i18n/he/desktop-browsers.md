---
meta_title: "דפדפני אינטרנט המכבדים פרטיות עבור מחשב ו-מק - Privacy Guides"
title: "דפדפנים שולחניים"
icon: material/laptop
description: דפדפני אינטרנט אלה מספקים הגנת פרטיות חזקה יותר מאשר Google Chrome.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: המלצות על דפדפן לשולחן העבודה פרטי
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/en/browser
    applicationCategory: Web Browser
    operatingSystem:
      - ווינדוס
      - macOS
      - לינוקס
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Firefox
    image: /assets/img/browsers/firefox.svg
    url: https://firefox.com
    sameAs: https://he.wikipedia.org/wiki/Firefox
    applicationCategory: Web Browser
    operatingSystem:
      - ווינדוס
      - macOS
      - לינוקס
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    sameAs: https://en.wikipedia.org/wiki/Brave_(web_browser)
    applicationCategory: Web Browser
    operatingSystem:
      - ווינדוס
      - macOS
      - לינוקס
    subjectOf:
      "@type": WebPage
      url: "./"
---

אלה הדפדפנים והתצורות המומלצים כרגע לגלישה רגילה/לא אנונימית. אנו ממליצים על [Mullvad Browser](#mullvad-browser) אם אתה מתמקד בהגנת פרטיות חזקה ואנטי-טביעת אצבע מהקופסה, [Firefox](#firefox) עבור דפדפני אינטרנט מזדמנים המחפשים אלטרנטיבה טובה ל-Google Chrome, ו-[Brave](#brave) אם אתה צריך תאימות לדפדפן Chromium.

אם אתה צריך לגלוש באינטרנט באופן אנונימי, אתה צריך להשתמש [Tor](tor.md) במקום. אנו מציעים כמה המלצות תצורה בדף זה, אך כל הדפדפנים מלבד דפדפן Tor יהיו ניתנים למעקב על ידי *מישהו* בצורה כזו או אחרת.

## דפדפן Mullvad

<div class="admonition recommendation" markdown>

![Mullvad Browser לוגו](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** הוא גרסה של [דפדפן Tor](tor.md#tor-browser) עם שילובי רשת Tor שהוסרו, שמטרתה לספק את טכנולוגיות הדפדפן נגד טביעת אצבע של Tor Browser למשתמשי VPN. הוא פותח על ידי Tor Project ומופץ על ידי [Mullvad](vpn.md#mullvad), ו**לא** דורש שימוש ב-VPN של Mullvad.

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

בדומה ל[דפדפן תור](tor.md), Mullvad Browser נועד למנוע טביעת אצבע על ידי הפיכת טביעת האצבע של הדפדפן שלך לזהות לכל שאר משתמשי Mullvad Browser, והוא כולל הגדרות ברירת מחדל והרחבות המוגדרות אוטומטית לפי רמות האבטחה המוגדרות כברירת מחדל: *Standard*, *Safer* ו- *Safest*. Therefore, it is imperative that you do not modify the browser at all outside adjusting the default [security levels](https://tb-manual.torproject.org/security-settings). שינויים אחרים יהפכו את טביעת האצבע שלך לייחודית, ויביסו את מטרת השימוש בדפדפן זה. אם אתה רוצה להגדיר את הדפדפן שלך בצורה כבדה יותר וטביעת אצבע אינה מדאיגה אותך, אנו ממליצים במקום זאת על [Firefox](#firefox).

### נגד טביעת אצבע

**ללא** שימוש ב [VPN](vpn.md), דפדפן Mullvad מספק את אותן הגנות נגד [סקריפטים תמימים של טביעת אצבע](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) כמו דפדפנים פרטיים אחרים כמו Firefox+[Arkenfox](#arkenfox-advanced) או [Brave](#brave). Mullvad Browser מספק הגנות אלה מחוץ לקופסה, על חשבון גמישות ונוחות מסוימת שדפדפנים פרטיים אחרים יכולים לספק.

==להגנה החזקה ביותר נגד טביעות אצבע, אנו ממליצים להשתמש בדפדפן Mullvad **בשילוב**עם VPN==, בין אם זה Mullvad או ספק VPN מומלץ אחר. בעת שימוש ב-VPN עם דפדפן Mullvad, אתה תשתף טביעת אצבע ומאגר של כתובות IP עם משתמשים רבים אחרים, מה שייתן לך "קהל" להתמזג איתו. אסטרטגיה זו היא הדרך היחידה לסכל תסריטי מעקב מתקדמים, והיא אותה טכניקה נגד טביעת אצבע המשמשת את Tor Browser.

שים לב שבעוד שאתה יכול להשתמש בדפדפן Mullvad עם כל ספק VPN, אנשים אחרים ב-VPN חייבים להשתמש גם הם בדפדפן Mullvad כדי ש"הקהל" הזה יתקיים, משהו שסביר יותר ב-Mullvad VPN בהשוואה לספקים אחרים, במיוחד זה קרוב לזה השקת דפדפן Mullvad. לדפדפן Mullvad אין קישוריות VPN מובנית, והוא גם לא בודק אם אתה משתמש ב-VPN לפני הגלישה; יש להגדיר ולנהל את חיבור ה-VPN שלך בנפרד.

Mullvad Browser מגיע עם *uBlock Origin* ו*NoScript* הרחבות דפדפן מותקנות מראש. בעוד שבדרך כלל [אנו לא ממליצים](#extensions) להוסיף *בנוסף* לתוספים אלו המגיעים מותקנים מראש בדפדפן צריכים**לא** יוסרו או יוגדרו מחוץ לערכי ברירת המחדל שלהם, כי פעולה זו תגרום באופן ניכר להבדיל את טביעת האצבע של הדפדפן שלך ממשתמשים אחרים בדפדפן Mullvad. הוא גם מגיע מותקן מראש עם הרחבת דפדפן Mullvad, *אותה* ניתן להסיר בבטחה מבלי להשפיע על טביעת האצבע של הדפדפן שלך אם תרצה, אך היא גם בטוחה לשמור גם אם אינך משתמש ב-Mullvad VPN.

### מצב גלישה פרטית

דפדפן Mullvad פועל במצב גלישה פרטית קבועה, כלומר ההיסטוריה, העוגיות ונתוני האתר האחרים שלך יימחקו תמיד בכל פעם שהדפדפן ייסגר. הסימניות, הגדרות הדפדפן והגדרות התוסף שלך עדיין יישמרו.

זה נדרש כדי למנוע צורות מתקדמות של מעקב, אבל זה כרוך במחיר של נוחות וכמה תכונות של Firefox, כגון Multi-Account Containers. זכור שאתה תמיד יכול להשתמש במספר דפדפנים, לדוגמה, אתה יכול לשקול להשתמש ב-Firefox+Arkenfox עבור כמה אתרים שאתה רוצה להישאר מחובר אליהם או שלא יפעלו כראוי בדפדפן Mullvad, ובדפדפן Mullvad לגלישה כללית.

### Mullvad Leta

Mullvad Browser מגיע עם DuckDuckGo מוגדר כ[מנוע החיפוש](search-engines.md) המוגדר כברירת מחדל, אך הוא מגיע גם מותקן מראש עם **Mullvad Leta**, מנוע חיפוש שדורש מנוי Mullvad VPN פעיל כדי לגשת אליו. Mullvad Leta מבצע שאילתות ישירות ב-API החיפוש בתשלום של גוגל (ולכן הוא מוגבל למנויים משלמים), אולם בגלל מגבלה זו, ניתן ל-Mullvad לתאם בין שאילתות חיפוש וחשבונות Mullvad VPN. מסיבה זו אנו מונעים את השימוש ב-Mullvad Leta, למרות ש-Mullvad אוספת מעט מאוד מידע על מנויי ה-VPN שלהם.

## Firefox

<div class="admonition recommendation" markdown>

![לוגו Firefox](assets/img/browsers/firefox.svg){ align=right }

**Firefox** מספק הגדרות פרטיות חזקות כגון [Enhanced Tracking Protection](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), שיכול לעזור לחסום שונים [סוגי מעקב](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-protection-blocks).

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://firefox-source-docs.mozilla.org){ .card-link title=Documentation}
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Firefox includes a unique [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) in downloads from Mozilla's website and uses telemetry in Firefox to send the token. The token is **not** included in releases from the [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases).

</div>

### תצורה מומלצת

ניתן למצוא אפשרויות אלה ב :material-menu: ← **הגדרות**

#### חיפוש

- [ ] בטל את הסימון **הצגת המלצות חיפוש**

ייתכן שתכונות הצעות חיפוש לא יהיו זמינות באזור שלך.

הצעות חיפוש שולחות את כל מה שאתה מקליד בסרגל הכתובות למנוע החיפוש המוגדר כברירת מחדל, ללא קשר אם אתה שולח חיפוש בפועל. השבתת הצעות חיפוש מאפשרת לך לשלוט בצורה מדויקת יותר באילו נתונים אתה שולח לספק מנועי החיפוש שלך.

#### פרטיות& אבטחה

##### הגנה מוגברת מפני מעקב

- [x] בחר ** מחמיר** הגנת מעקב מתקדמת

זה מגן עליך על ידי חסימת מעקבי מדיה חברתית, סקריפטים של טביעת אצבע (שים לב שזה לא מגן עליך מפני *כל* טביעות האצבע), קריפטומינרים, עוגיות מעקב חוצות- אתרים ותוכן מעקב אחר. ETP מגן מפני איומים נפוצים רבים, אך הוא אינו חוסם את כל אפיקי המעקב מכיוון שהוא נועד להשפיע באופן מינימלי עד ללא השפעה על השימושיות באתר.

##### Firefox Suggest (ארה"ב בלבד)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. אנו ממליצים להשבית אותו מאותה סיבה שאנו ממליצים להשבית את הצעות החיפוש. אם אינך רואה את האפשרויות הללו תחת הכותרת **סרגל הכתובות**, אין לך את החוויה החדשה ואתה יכול להתעלם משינויים אלה.

- [] בטל את הסימון **הצעות מהאינטרנט**
- [ ] בטל את הסימון **הצעות מנותני חסות**

##### חיטוי בעת סגירה

אם אתה רוצה להישאר מחובר לאתרים מסוימים, אתה יכול לאפשר חריגים ב**עוגיות ונתוני אתר** ← **נהל חריגים... **

- [x] סמן **מחיקת עוגיות ונתוני אתרים עם סגירת Firefox**

זה מגן עליך מפני עוגיות מתמשכות, אך אינו מגן עליך מפני עוגיות שנרכשו במהלך כל הפעלת גלישה אחת. כאשר זה מופעל, אפשר לנקות בקלות את קובצי העוגיות של הדפדפן שלך פשוט על ידי הפעלה מחדש של Firefox. אתה יכול להגדיר חריגים על בסיס אתר, אם אתה רוצה להישאר מחובר לאתר מסוים שאתה מבקר בו לעתים קרובות.

##### טלמטריה

- [ ] בטל את הסימון **לאפשר ל-Firefox לשלוח אל Mozilla מידע טכני ופעולות שבוצעו בדפדפן**
- [ ] בטל את הסימון **לאפשר ל-Firefox להתקין ולהריץ מחקרים**
- [ ] בטל את הסימון **לאפשר ל-Firefox דיווחי קריסות שנשמרו בשמך**

> Firefox שולח נתונים על הגרסה והשפה של Firefox שלך; תצורת מערכת ההפעלה והחומרה של המכשיר; זיכרון, מידע בסיסי על קריסות ושגיאות; תוצאה של תהליכים אוטומטיים כמו עדכונים, גלישה בטוחה והפעלה אלינו. כאשר Firefox שולח לנו נתונים, כתובת ה-IP שלך נאספת זמנית כחלק מיומני השרת שלנו.

Additionally, the Firefox Accounts service collects [some technical data](https://mozilla.org/privacy/firefox/#firefox-accounts). אם אתה משתמש בחשבון Firefox אתה יכול לבטל את הסכמתך:

1. פתח את [הגדרות הפרופיל שלך ב ](https://accounts.firefox.com/settings#data-collection)accounts.firefox.com
2. ביטול סימון **איסוף נתונים ושימוש** > **עזרה בשיפור חשבונות Firefox**

##### מצב HTTPS בלבד

- [x] בחר **הפעלת מצב HTTPS בלבד בכל החלונות**

זה מונע ממך להתחבר ללא כוונה לאתר אינטרנט ב-HTTP בטקסט רגיל. אתרים ללא HTTPS אינם נפוצים כיום, לכן לא אמורה להיות לכך השפעה רבה על הגלישה היומיומית שלך.

##### DNS דרך HTTPS

אם אתה משתמש ב[ספק DNS דרך HTTPS](dns.md):

- [x] בחר **Max Protection** ובחר ספק מתאים

Max Protection אוכפת את השימוש ב-DNS על HTTPS, ואזהרת אבטחה תראה אם Firefox לא יכול להתחבר לפותר ה-DNS המאובטח שלך, או אם פותר ה-DNS המאובטח שלך אומר שרשומות עבור הדומיין שאליו אתה מנסה לגשת אינן קיימות. זה מונע מהרשת שאליה אתה מחובר לשדרג לאחור בסתר את אבטחת ה-DNS שלך.

#### סנכרון

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (מתקדם)

<div class="admonition tip" markdown>
<p class="admonition-title">Use Mullvad Browser for advanced anti-fingerprinting</p>

[דפדפן Mullvad](#mullvad-browser) מספק את אותן הגנות נגד טביעת אצבע כמו Arkenfox מחוץ לקופסה, ואינו מצריך שימוש ב-VPN של Mullvad כדי ליהנות מההגנות הללו. יחד עם VPN, דפדפן Mullvad יכול לסכל סקריפטים מתקדמים יותר למעקב ש-Arkenfox לא יכול. ל-Arkenfox עדיין יש את היתרון להיות הרבה יותר גמיש, ולאפשר חריגים לכל אתר עבור אתרים שאתה צריך להישאר מחובר אליהם.

</div>

פרויקט [Arkenfox](https://github.com/arkenfox/user.js) מספק קבוצה של אפשרויות שנשקלו בקפידה עבור Firefox. אם אתה [מחליט](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) להשתמש ב-Arkenfox, [כמה אפשרויות](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) הן קפדניות סובייקטיבית ו/או עלולות לגרום לאתרים מסוימים לא לעבוד כראוי [שאותן תוכל לשנות בקלות](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) כדי להתאים לצרכים שלך. אנו **ממליצים בחום** לקרוא את [הויקי](https://github.com/arkenfox/user.js/wiki) המלא שלהם. Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox שואפת רק לסכל תסריטי מעקב בסיסיים או נאיביים באמצעות קנבס אקראי והגדרות תצורת התנגדות טביעות האצבע המובנות של Firefox. זה לא מכוון לגרום לדפדפן שלך להשתלב עם קהל גדול של משתמשי Arkenfox אחרים באותו אופן שבו Mullvad Browser או Tor Browser עושים, וזו הדרך היחידה לסכל סקריפטים מתקדמים למעקב אחר טביעות אצבע. זכור שאתה תמיד יכול להשתמש במספר דפדפנים, לדוגמה, אתה יכול לשקול להשתמש ב-Firefox+Arkenfox עבור כמה אתרים שאתה רוצה להישאר מחובר אליהם או לסמוך עליהם בדרך אחרת, ואת Mullvad Browser לגלישה כללית.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave בנוי על פרויקט דפדפן Chromium, כך שהוא אמור להרגיש מוכר ושיהיו לו בעיות תאימות מינימליות לאתר.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-windows11: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

**משתמשי macOS:** ההורדה של Brave Browser מהאתר הרשמי שלהם היא מתקין `.pkg` הדורש הרשאות מנהל כדי לפעול (ועשוי להפעיל סקריפטים מיותרים אחרים במחשב שלך). כחלופה, אתה יכול להוריד את הקובץ האחרון `Brave-Browser-universal.dmg` מעמוד[ההפצות גיטהאב ](https://github.com/brave/brave-browser/releases/latest)שלהם, המספק התקנה מסורתית של "גרור לתיקיית יישומים".

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Brave מוסיף "[קוד הפניה](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" לשם הקובץ בהורדות מהאתר Brave, המשמש למעקב מאיזה מקור הורדת הדפדפן, למשל `BRV002` בהורדה בשם `Brave-Browser-BRV002.pkg`. לאחר מכן, המתקין יבצע פינג לשרת של Brave עם קוד ההפניה בסוף תהליך ההתקנה. אם אתה מודאג מכך, אתה יכול לשנות את שם קובץ ההתקנה לפני פתיחתו.

</div>

### תצורה מומלצת

ניתן למצוא אפשרויות אלה ב - :material-menu: ← **הגדרות**.

#### הגדרות

##### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

ניתן לשדרג לאחור את האפשרויות של Shields על בסיס אתר לפי הצורך, אך כברירת מחדל אנו ממליצים להגדיר את האפשרויות הבאות:

<div class="annotate" markdown>

- [x] Select **Prevent sites from fingerprinting me based on my language preferences**
- [x] Select **Aggressive** under Trackers & ads blocking

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. אנו ממליצים לא להשתמש בתכונה זו; במקום זאת, שמור על רשימות הסינון המוגדרות כברירת מחדל. שימוש ברשימות נוספות יגרום לך להתבלט ממשתמשי Brave אחרים ועלול גם להגדיל את שטח ההתקפה אם יש ניצול ב-Brave וכלל זדוני יתווסף לאחת הרשימות שבהן אתה משתמש.

</details>

- [x] Select **Strict** under **Upgrade connections to HTTPS**
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Strict, may break sites** under Block fingerprinting
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net) extension.
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar.

##### פרטיות ואבטחה

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP Handling Policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Private window with Tor** (1)

</div>

1. Brave הוא **לא** עמיד בפני טביעת אצבע כמו דפדפן Tor והרבה פחות אנשים משתמשים אמיץ עם Tor, כך תוכל להתבלט. Where [strong anonymity is required](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) use the [Tor Browser](tor.md#tor-browser).

<div class="admonition tip" markdown>
<p class="admonition-title">Sanitizing on close</p>

- [x] In the *Sites and Shields Settings* menu, under Content, after clicking on the *On-device site data* menu, select **Delete data sites have saved to your device when you close all windows**

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

##### הרחבות

השבת הרחבות מובנות שאינך משתמש בהן ב**הרחבות**

- [ ] בטל את הסימון **Hangouts**
- [ ] בטל את הסימון **WebTorrent**

##### Web3

תכונות ה-Web3 של Brave עשויות להוסיף לטביעת האצבע של הדפדפן ולשטח ההתקפה שלך. אלא אם אתה משתמש באחת מהתכונות, יש להשבית אותן.

- בחר **הרחבות (ללא נפילה)** תחת ארנק Ethereum ברירת מחדל וארנק Solana ברירת מחדל
- הגדר את **שיטה לפתרון משאבי IPFS** ל**מושבת**

##### מערכת

<div class="annotate" markdown>

- [] בטל את הסימון **המשך להפעיל אפליקציות כאשר Brave סגור** כדי להשבית אפליקציות רקע (1)

</div>

1. אפשרות זו אינה קיימת בכל הפלטפורמות.

#### סנכרון

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** מאפשר לך לקבל מטבע קריפטוגרפי Basic Attention Token (BAT) עבור ביצוע פעולות מסוימות בתוך Brave. זה מסתמך על חשבון משמורת ו-KYC ממספר נבחר של ספקים. איננו ממליצים על BAT כ[מטבע קריפטוגרפי פרטי](cryptocurrency.md), וגם איננו ממליצים להשתמש ב[ארנק משמורת](advanced/payments.md#other-coins-bitcoin-ethereum-etc), לכן נמנע משימוש בתכונה זו.

**Brave Wallet** פועל באופן מקומי במחשב שלך, אך אינו תומך במטבעות קריפטוגרפיים פרטיים כלשהם, ולכן אנו נמנע משימוש גם בתכונה זו.

## מקורות נוספים

באופן כללי, אנו ממליצים לשמור על הרחבות הדפדפן שלך למינימום כדי להקטין את משטח ההתקפה שלך; יש להם גישה מוסמכת בדפדפן שלך, הם דורשים ממך לסמוך על המפתח, יכולים לגרום לך [לבלוט](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint) ו[להחליש](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) את בידוד האתרים. עם זאת, uBlock Origin עשוי להיות שימושי אם אתה מעריך פונקציונליות של חסימת תוכן.

### uBlock Origin

<div class="admonition recommendation" markdown>

![הלוגו של uBlock Origin](assets/img/browsers/ublock_origin.svg){ align=right }

**uBlock Origin** הוא חוסם תוכן פופולרי שיכול לעזור לך לחסום מודעות, עוקבים וסקריפטים של טביעות אצבע.

[:octicons-repo-16: Repository](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

</details>

</div>

אנו ממליצים לעקוב אחר התיעוד של [היזם](https://github.com/gorhill/uBlock/wiki/Blocking-mode) ולבחור אחד מה"מצבים ". רשימות מסננים נוספות [עלולות להשפיע על הביצועים ולהגדיל את שטח התקיפה](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

אלה עוד כמה [רשימות מסנן](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) ייתכן שתרצה לשקול הוספה:

- [x] בדוק **פרטיות** > **הגנה על מעקב אחר כתובות אתרים של AdGuard**
- להוסיף [למעשה כלי URL מקוצר לגיטימי ](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

### uBlock Origin Lite

uBlock Origin also has a "Lite" version of their extension, which offers a very limited feature-set compared to the original extension. However, it has a few distinct advantages over its full-fledged sibling, so you may want to consider it if...

- ...you don't want to grant full "read/modify website data" permissions to any extensions (even a trusted one like uBlock Origin)
- ...you want a more resource (memory/CPU) efficient content blocker[^1]
- ...your browser only supports Manifest V3 extensions

<div class="admonition recommendation" markdown>

![uBlock Origin Lite logo](assets/img/browsers/ublock_origin_lite.svg){ align=right }

**uBlock Origin Lite** is a Manifest V3 compatible content blocker. Compared to the original *uBlock Origin*, this extension does not require broad "read/modify data" permissions to function.

[:octicons-repo-16: Repository](https://github.com/uBlockOrigin/uBOL-home#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/uBlockOrigin/uBOL-home/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/gorhill/uBlock/tree/master/platform/mv3){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/addon/ublock-origin-lite)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin-lite/ddkjiahejlhfcafbddmgiahcphecmpfh)

</details>

</div>

We only recommend this version of uBlock Origin if you never want to make any changes to your filter lists, because it only supports a few pre-selected lists and offers no additional customization options, including the ability to select elements to block manually. These restrictions are due to limitations in Manifest V3's design.

This version offers three levels of blocking: "Basic" works without requiring any special privileges to view and modify site content, while the "Optimal" and "Complete" levels do require that broad permission, but offer a better filtering experience with additional cosmetic rules and scriptlet injections.

If you set the default filtering mode to "Optimal" or "Complete" the extension will request read/modify access to **all** websites you visit. However, you also have the option to change the setting to "Optimal" or "Complete" on a **per-site** basis by adjusting the slider in the extension's pop-up panel on any given site. When you do so, the extension will request read/modify access to that site only. Therefore, if you want to take advantage of uBlock Origin Lite's "permission-less" configuration, you should probably leave the default setting as "Basic" and only adjust it higher on sites where that level is not adequate.

uBlock Origin Lite only receives block list updates whenever the extension is updated from your browser's extension marketplace, as opposed to on demand. This means that you may miss out on new threats being blocked for weeks until a full extension release is published.

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

### דרישות מינימליות

- חייבת להיות תוכנת קוד פתוח.
- תומך בעדכונים אוטומטיים.
- מקבל עדכוני מנוע בתוך 0 -1 ימים משחרורו במעלה הזרם.
- זמין ב-Linux, macOS ו-Windows.
- כל שינוי שיידרש כדי להפוך את הדפדפן ליותר מכבד פרטיות לא צריך להשפיע לרעה על חוויית המשתמש.
- חוסם קובצי עוגיות של צד שלישי כברירת מחדל.
- Supports [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^2]

### המקרה הטוב ביותר

הקריטריונים הטובים ביותר שלנו מייצגים את מה שהיינו רוצים לראות מהפרויקט המושלם בקטגוריה זו. ייתכן שההמלצות שלנו לא יכללו חלק מהפונקציונליות הזו או את כולה, אך אלו שכן כן עשויות לדרג גבוה יותר מאחרות בדף זה.

- כולל פונקציונליות מובנית לחסימת תוכן.
- Supports cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Supports Progressive Web Apps. PWAs enable you to install certain websites as if they were native apps on your computer. זה יכול להיות בעל יתרונות על פני התקנת אפליקציות מבוססות-אלקטרון, מכיוון שאתה נהנה מעדכוני האבטחה הרגילים של הדפדפן שלך.
- לא כולל פונקציונליות הרחבה (bloatware) שאינה משפיעה על פרטיות המשתמש.
- אינו אוסף טלמטריה כברירת מחדל.
- מספק יישום שרת סינכרון בקוד פתוח.
- ברירת המחדל היא [מנוע חיפוש פרטי](search-engines.md).

### קריטריונים להרחבה

- אסור לשכפל דפדפן מובנה או פונקציונליות מערכת הפעלה.
- חייב להשפיע ישירות על פרטיות המשתמש, כלומר לא חייב פשוט לספק מידע.

[^1]: uBlock Origin Lite *itself* will consume no resources, because it uses newer APIs which make the browser process the filter lists natively, instead of running JavaScript code within the extension to handle the filtering. However, this resource advantage is only [theoretical](https://github.com/uBlockOrigin/uBOL-home/wiki/Frequently-asked-questions-(FAQ)#is-ubol-more-efficient-cpu--and-memory-wise-than-ubo), because it's possible that standard uBlock Origin's filtering code is more efficient than your browser's native filtering code. This has not yet been benchmarked.
[^2]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
