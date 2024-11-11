---
meta_title: "דפדפני אינטרנט המכבדים פרטיות עבור מחשב ו-מק - Privacy Guides"
title: "דפדפנים שולחניים"
icon: material/laptop
description: These privacy-protecting browsers are what we currently recommend for standard/non-anonymous internet browsing on desktop systems.
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

<small>Protects against the following threat(s):</small>

- [:material-account-cash: קפיטליזם מעקב](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our currently recommended **desktop web browsers** and configurations for standard/non-anonymous browsing. אנו ממליצים על [Mullvad Browser](#mullvad-browser) אם אתה מתמקד בהגנת פרטיות חזקה ואנטי-טביעת אצבע מהקופסה, [Firefox](#firefox) עבור דפדפני אינטרנט מזדמנים המחפשים אלטרנטיבה טובה ל-Google Chrome, ו-[Brave](#brave) אם אתה צריך תאימות לדפדפן Chromium.

אם אתה צריך לגלוש באינטרנט באופן אנונימי, אתה צריך להשתמש [Tor](tor.md) במקום. אנו מציעים כמה המלצות תצורה בדף זה, אך כל הדפדפנים מלבד דפדפן Tor יהיו ניתנים למעקב על ידי *מישהו* בצורה כזו או אחרת.

## דפדפן Mullvad

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** is a version of [Tor Browser](tor.md#tor-browser) with Tor network integrations removed. It aims to provide to VPN users Tor Browser's anti-fingerprinting browser technologies, which are key protections against [:material-eye-outline: Mass Surveillance](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. הוא פותח על ידי Tor Project ומופץ על ידי [Mullvad](vpn.md#mullvad), ו**לא** דורש שימוש ב-VPN של Mullvad.

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

בדומה ל[דפדפן תור](tor.md), Mullvad Browser נועד למנוע טביעת אצבע על ידי הפיכת טביעת האצבע של הדפדפן שלך לזהות לכל שאר משתמשי Mullvad Browser, והוא כולל הגדרות ברירת מחדל והרחבות המוגדרות אוטומטית לפי רמות האבטחה המוגדרות כברירת מחדל: *Standard*, *Safer* ו- *Safest*. Therefore, it is imperative that you do not modify the browser at all outside adjusting the default [security levels](https://tb-manual.torproject.org/security-settings). שינויים אחרים יהפכו את טביעת האצבע שלך לייחודית, ויביסו את מטרת השימוש בדפדפן זה. אם אתה רוצה להגדיר את הדפדפן שלך בצורה כבדה יותר וטביעת אצבע אינה מדאיגה אותך, אנו ממליצים במקום זאת על [Firefox](#firefox).

### נגד טביעת אצבע

**ללא** שימוש ב [VPN](vpn.md), דפדפן Mullvad מספק את אותן הגנות נגד [סקריפטים תמימים של טביעת אצבע](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) כמו דפדפנים פרטיים אחרים כמו Firefox+[Arkenfox](#arkenfox-advanced) או [Brave](#brave). Mullvad Browser מספק הגנות אלה מחוץ לקופסה, על חשבון גמישות ונוחות מסוימת שדפדפנים פרטיים אחרים יכולים לספק.

==להגנה החזקה ביותר נגד טביעות אצבע, אנו ממליצים להשתמש בדפדפן Mullvad **בשילוב**עם VPN==, בין אם זה Mullvad או ספק VPN מומלץ אחר. בעת שימוש ב-VPN עם דפדפן Mullvad, אתה תשתף טביעת אצבע ומאגר של כתובות IP עם משתמשים רבים אחרים, מה שייתן לך "קהל" להתמזג איתו. אסטרטגיה זו היא הדרך היחידה לסכל תסריטי מעקב מתקדמים, והיא אותה טכניקה נגד טביעת אצבע המשמשת את Tor Browser.

שים לב שבעוד שאתה יכול להשתמש בדפדפן Mullvad עם כל ספק VPN, אנשים אחרים ב-VPN חייבים להשתמש גם הם בדפדפן Mullvad כדי ש"הקהל" הזה יתקיים, משהו שסביר יותר ב-Mullvad VPN בהשוואה לספקים אחרים, במיוחד זה קרוב לזה השקת דפדפן Mullvad. לדפדפן Mullvad אין קישוריות VPN מובנית, והוא גם לא בודק אם אתה משתמש ב-VPN לפני הגלישה; יש להגדיר ולנהל את חיבור ה-VPN שלך בנפרד.

Mullvad Browser מגיע עם *uBlock Origin* ו*NoScript* הרחבות דפדפן מותקנות מראש. While we typically discourage adding *additional* [browser extensions](browser-extensions.md), these extensions that come pre-installed with the browser should **not** be removed or configured outside their default values, because doing so would noticeably make your browser fingerprint distinct from other Mullvad Browser users. הוא גם מגיע מותקן מראש עם הרחבת דפדפן Mullvad, *אותה* ניתן להסיר בבטחה מבלי להשפיע על טביעת האצבע של הדפדפן שלך אם תרצה, אך היא גם בטוחה לשמור גם אם אינך משתמש ב-Mullvad VPN.

### מצב גלישה פרטית

דפדפן Mullvad פועל במצב גלישה פרטית קבועה, כלומר ההיסטוריה, העוגיות ונתוני האתר האחרים שלך יימחקו תמיד בכל פעם שהדפדפן ייסגר. הסימניות, הגדרות הדפדפן והגדרות התוסף שלך עדיין יישמרו.

זה נדרש כדי למנוע צורות מתקדמות של מעקב, אבל זה כרוך במחיר של נוחות וכמה תכונות של Firefox, כגון Multi-Account Containers. זכור שאתה תמיד יכול להשתמש במספר דפדפנים, לדוגמה, אתה יכול לשקול להשתמש ב-Firefox+Arkenfox עבור כמה אתרים שאתה רוצה להישאר מחובר אליהם או שלא יפעלו כראוי בדפדפן Mullvad, ובדפדפן Mullvad לגלישה כללית.

### Mullvad Leta

Mullvad Browser מגיע עם DuckDuckGo מוגדר כ[מנוע החיפוש](search-engines.md) המוגדר כברירת מחדל, אך הוא מגיע גם מותקן מראש עם **Mullvad Leta**, מנוע חיפוש שדורש מנוי Mullvad VPN פעיל כדי לגשת אליו. Mullvad Leta queries Google's paid search API directly, which is why it is limited to paying subscribers. However, it is possible for Mullvad to correlate search queries and Mullvad VPN accounts because of this limitation. מסיבה זו אנו מונעים את השימוש ב-Mullvad Leta, למרות ש-Mullvad אוספת מעט מאוד מידע על מנויי ה-VPN שלהם.

## Firefox

<div class="admonition recommendation" markdown>

![לוגו Firefox](assets/img/browsers/firefox.svg){ align=right }

**Firefox** מספק הגדרות פרטיות חזקות כגון [Enhanced Tracking Protection](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), שיכול לעזור לחסום שונים [סוגי מעקב](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-protection-blocks).

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="Documentation" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Firefox includes a unique [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) in downloads from Mozilla's website and uses telemetry in Firefox to send the token. The token is **not** included in releases from the [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Recommended Firefox Configuration

ניתן למצוא אפשרויות אלה ב - :material-menu: ← **הגדרות**.

#### חיפוש

- [ ] Uncheck **Show search suggestions**

ייתכן שתכונות הצעות חיפוש לא יהיו זמינות באזור שלך.

הצעות חיפוש שולחות את כל מה שאתה מקליד בסרגל הכתובות למנוע החיפוש המוגדר כברירת מחדל, ללא קשר אם אתה שולח חיפוש בפועל. השבתת הצעות חיפוש מאפשרת לך לשלוט בצורה מדויקת יותר באילו נתונים אתה שולח לספק מנועי החיפוש שלך.

##### Firefox Suggest (ארה"ב בלבד)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. אנו ממליצים להשבית אותו מאותה סיבה שאנו ממליצים להשבית את הצעות החיפוש. אם אינך רואה את האפשרויות הללו תחת הכותרת **סרגל הכתובות**, אין לך את החוויה החדשה ואתה יכול להתעלם משינויים אלה.

- [ ] Uncheck **Suggestions from Firefox**
- [ ] בטל את הסימון **הצעות מנותני חסות**

#### פרטיות& אבטחה

##### הגנה מוגברת מפני מעקב

- [x] בחר ** מחמיר** הגנת מעקב מתקדמת

זה מגן עליך על ידי חסימת מעקבי מדיה חברתית, סקריפטים של טביעת אצבע (שים לב שזה לא מגן עליך מפני *כל* טביעות האצבע), קריפטומינרים, עוגיות מעקב חוצות- אתרים ותוכן מעקב אחר. ETP מגן מפני איומים נפוצים רבים, אך הוא אינו חוסם את כל אפיקי המעקב מכיוון שהוא נועד להשפיע באופן מינימלי עד ללא השפעה על השימושיות באתר.

##### חיטוי בעת סגירה

אם אתה רוצה להישאר מחובר לאתרים מסוימים, אתה יכול לאפשר חריגים ב**עוגיות ונתוני אתר** ← **נהל חריגים... **

- [x] סמן **מחיקת עוגיות ונתוני אתרים עם סגירת Firefox**

זה מגן עליך מפני עוגיות מתמשכות, אך אינו מגן עליך מפני עוגיות שנרכשו במהלך כל הפעלת גלישה אחת. כאשר זה מופעל, אפשר לנקות בקלות את קובצי העוגיות של הדפדפן שלך פשוט על ידי הפעלה מחדש של Firefox. אתה יכול להגדיר חריגים על בסיס אתר, אם אתה רוצה להישאר מחובר לאתר מסוים שאתה מבקר בו לעתים קרובות.

##### Telemetry

- [ ] בטל את הסימון **לאפשר ל-Firefox לשלוח אל Mozilla מידע טכני ופעולות שבוצעו בדפדפן**
- [ ] בטל את הסימון **לאפשר ל-Firefox להתקין ולהריץ מחקרים**
- [ ] בטל את הסימון **לאפשר ל-Firefox דיווחי קריסות שנשמרו בשמך**

According to Mozilla's privacy policy for Firefox,

> Firefox שולח נתונים על הגרסה והשפה של Firefox שלך; תצורת מערכת ההפעלה והחומרה של המכשיר; זיכרון, מידע בסיסי על קריסות ושגיאות; תוצאה של תהליכים אוטומטיים כמו עדכונים, גלישה בטוחה והפעלה אלינו. כאשר Firefox שולח לנו נתונים, כתובת ה-IP שלך נאספת זמנית כחלק מיומני השרת שלנו.

Additionally, the Mozilla Accounts service collects [some technical data](https://mozilla.org/privacy/mozilla-accounts). If you use a Mozilla Account you can opt-out:

1. פתח את [הגדרות הפרופיל שלך ב ](https://accounts.firefox.com/settings#data-collection)accounts.firefox.com
2. ביטול סימון **איסוף נתונים ושימוש** > **עזרה בשיפור חשבונות Firefox**

##### Website Advertising Preferences

- [ ] Uncheck **Allow websites to perform privacy-preserving ad measurement**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.

##### HTTPS-Only Mode

- [x] בחר **הפעלת מצב HTTPS בלבד בכל החלונות**

זה מונע ממך להתחבר ללא כוונה לאתר אינטרנט ב-HTTP בטקסט רגיל. אתרים ללא HTTPS אינם נפוצים כיום, לכן לא אמורה להיות לכך השפעה רבה על הגלישה היומיומית שלך.

##### DNS דרך HTTPS

אם אתה משתמש ב[ספק DNS דרך HTTPS](dns.md):

- [x] בחר **Max Protection** ובחר ספק מתאים

Max Protection אוכפת את השימוש ב-DNS על HTTPS, ואזהרת אבטחה תראה אם Firefox לא יכול להתחבר לפותר ה-DNS המאובטח שלך, או אם פותר ה-DNS המאובטח שלך אומר שרשומות עבור הדומיין שאליו אתה מנסה לגשת אינן קיימות. זה מונע מהרשת שאליה אתה מחובר לשדרג לאחור בסתר את אבטחת ה-DNS שלך.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (מתקדם)

<div class="admonition tip" markdown>
<p class="admonition-title">Use Mullvad Browser for advanced anti-fingerprinting</p>

[דפדפן Mullvad](#mullvad-browser) מספק את אותן הגנות נגד טביעת אצבע כמו Arkenfox מחוץ לקופסה, ואינו מצריך שימוש ב-VPN של Mullvad כדי ליהנות מההגנות הללו. יחד עם VPN, דפדפן Mullvad יכול לסכל סקריפטים מתקדמים יותר למעקב ש-Arkenfox לא יכול. ל-Arkenfox עדיין יש את היתרון להיות הרבה יותר גמיש, ולאפשר חריגים לכל אתר עבור אתרים שאתה צריך להישאר מחובר אליהם.

</div>

פרויקט [Arkenfox](https://github.com/arkenfox/user.js) מספק קבוצה של אפשרויות שנשקלו בקפידה עבור Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly—which you can [easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. אנו **ממליצים בחום** לקרוא את [הויקי](https://github.com/arkenfox/user.js/wiki) המלא שלהם. Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox שואפת רק לסכל תסריטי מעקב בסיסיים או נאיביים באמצעות קנבס אקראי והגדרות תצורת התנגדות טביעות האצבע המובנות של Firefox. זה לא מכוון לגרום לדפדפן שלך להשתלב עם קהל גדול של משתמשי Arkenfox אחרים באותו אופן שבו Mullvad Browser או Tor Browser עושים, וזו הדרך היחידה לסכל סקריפטים מתקדמים למעקב אחר טביעות אצבע. Remember that you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave בנוי על פרויקט דפדפן Chromium, כך שהוא אמור להרגיש מוכר ושיהיו לו בעיות תאימות מינימליות לאתר.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Brave מוסיף "[קוד הפניה](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" לשם הקובץ בהורדות מהאתר Brave, המשמש למעקב מאיזה מקור הורדת הדפדפן, למשל `BRV002` בהורדה בשם `Brave-Browser-BRV002.pkg`. לאחר מכן, המתקין יבצע פינג לשרת של Brave עם קוד ההפניה בסוף תהליך ההתקנה. אם אתה מודאג מכך, אתה יכול לשנות את שם קובץ ההתקנה לפני פתיחתו.

</div>

### Recommended Brave Configuration

ניתן למצוא אפשרויות אלה ב - :material-menu: ← **הגדרות**.

#### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

ניתן לשדרג לאחור את האפשרויות של Shields על בסיס אתר לפי הצורך, אך כברירת מחדל אנו ממליצים להגדיר את האפשרויות הבאות:

<div class="annotate" markdown>

- [x] Select **Aggressive** under *Trackers & ads blocking*

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. אנו ממליצים לא להשתמש בתכונה זו; במקום זאת, שמור על רשימות הסינון המוגדרות כברירת מחדל. שימוש ברשימות נוספות יגרום לך להתבלט ממשתמשי Brave אחרים ועלול גם להגדיל את שטח ההתקפה אם יש ניצול ב-Brave וכלל זדוני יתווסף לאחת הרשימות שבהן אתה משתמש.

</details>

- [x] Select **Strict** under *Upgrade connections to HTTPS*
- [x] (Optional) Select **Block Scripts** (1)
- [x] Check **Block fingerprinting**
- [x] Select **Block third-party cookies**
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option disables JavaScript, which will break a lot of sites. To unbreak them, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

#### Privacy and security

<div class="annotate" markdown>

- [x] Select **Don't allow sites to use the V8 optimizer** under *Security* → *Manage V8 security* (1)
- [x] Select **Automatically remove permissions from unused sites** under *Sites and Shields Settings*
- [x] Select **Disable non-proxied UDP** under [*WebRTC IP Handling Policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **Prevent sites from fingerprinting me based on my language preferences**

</div>

1. Disabling the V8 optimizer reduces your attack surface by disabling [*some*](https://grapheneos.social/@GrapheneOS/112708049232710156) parts of JavaScript Just-In-Time (JIT) compilation.

<div class="admonition tip" markdown>
<p class="admonition-title">Sanitizing on close</p>

- [x] Select **Delete data sites have saved to your device when you close all windows** under *Sites and Shields Settings* → *Content* → *Additional content settings* → *On-device site data*.

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

##### Tor windows

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) allows you to route your traffic through the Tor network in Private Windows and access .onion services, which may be useful in some cases. However, Brave is **not** as resistant to fingerprinting as the Tor Browser is, and far fewer people use Brave with Tor, so you will stand out. If your threat model requires strong anonymity, use the [Tor Browser](tor.md#tor-browser).

##### Data Collection

- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**

#### Web3

תכונות ה-Web3 של Brave עשויות להוסיף לטביעת האצבע של הדפדפן ולשטח ההתקפה שלך. Unless you use any of these features, they should be disabled.

- Select **Extensions (no fallback)** under *Default Ethereum wallet*
- Select **Extensions (no fallback)** under *Default Solana wallet*

#### Extensions

- [ ] Uncheck all built-in extensions you don't use

#### Search engine

We recommend disabling search suggestions in Brave for the same reason we recommend disabling this feature in [Firefox](#search).

- [ ] Uncheck **Show search suggestions**

#### System

<div class="annotate" markdown>

- [] בטל את הסימון **המשך להפעיל אפליקציות כאשר Brave סגור** כדי להשבית אפליקציות רקע (1)

</div>

1. אפשרות זו אינה קיימת בכל הפלטפורמות.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. זה מסתמך על חשבון משמורת ו-KYC ממספר נבחר של ספקים. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Brave Wallet** פועל באופן מקומי במחשב שלך, אך אינו תומך במטבעות קריפטוגרפיים פרטיים כלשהם, ולכן אנו נמנע משימוש גם בתכונה זו.

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

### דרישות מינימליות

- חייבת להיות תוכנת קוד פתוח.
- חייב לתמוך בעדכונים אוטומטיים.
- Must receive engine updates in 0-1 days from upstream release.
- Must be available on Linux, macOS, and Windows.
- Any changes required to make the browser more privacy-respecting must not negatively impact user experience.
- Must block third-party cookies by default.
- Must support [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### המקרה הטוב ביותר

הקריטריונים הטובים ביותר שלנו מייצגים את מה שהיינו רוצים לראות מהפרויקט המושלם בקטגוריה זו. ייתכן שההמלצות שלנו לא יכללו חלק מהפונקציונליות הזו או את כולה, אך אלו שכן כן עשויות לדרג גבוה יותר מאחרות בדף זה.

- Should include built-in content blocking functionality.
- Should support cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Should support Progressive Web Apps (PWAs). PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps because PWAs benefit from your browser's regular security updates.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Should not collect telemetry by default.
- Should provide an open-source sync server implementation.
- Should default to a [private search engine](search-engines.md).

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
