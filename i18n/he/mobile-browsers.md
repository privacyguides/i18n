---
meta_title: "פרטיות כיבוד דפדפני אינטרנט ניידים עבור אנדרואיד ו - iOS - מדריכי פרטיות"
title: "דפדפני אינטרנט לנייד"
icon: material/cellphone-information
description: דפדפנים אלו הם מה שאנו ממליצים כיום עבור גלישה רגילה/לא אנונימית באינטרנט בטלפון שלך.
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: המלצות על דפדפן פרטי לנייד
    url: "./"
    relatedLink: "../desktop-browsers/"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    applicationCategory: Web Browser
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://apple.com/safari
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: קפיטליזם מעקב](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our currently recommended **mobile web browsers** and configurations for standard/non-anonymous internet browsing. אם אתה צריך לגלוש באינטרנט באופן אנונימי, אתה צריך להשתמש [Tor](tor.md) במקום.

## Brave

<div class="admonition recommendation" markdown>

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

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)

</details>

</div>

### Recommended Brave Configuration

דפדפן Tor הוא הדרך היחידה לגלוש באמת באינטרנט באופן אנונימי. כאשר אתה משתמש ב-Brave, אנו ממליצים לשנות את ההגדרות הבאות כדי להגן על פרטיותך מפני גורמים מסוימים, אך כל הדפדפנים מלבד [Tor דפדפן](tor.md#tor-browser) יהיו ניתנים למעקב על ידי *מישהו* בהקשר זה או אחר.

ניתן למצוא אפשרויות אלו ב :material-menu: → **הגדרות** → **Brave Shields & פרטיות**

#### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

#### Brave shields global defaults

ניתן לשדרג לאחור את האפשרויות של Shields על בסיס אתר לפי הצורך, אך כברירת מחדל אנו ממליצים להגדיר את האפשרויות הבאות:

<div class="annotate" markdown>

- [x] Select **Aggressive** under **Block trackers & ads**

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. אנו ממליצים לא להשתמש בתכונה זו; במקום זאת, שמור על רשימות הסינון המוגדרות כברירת מחדל. שימוש ברשימות נוספות יגרום לך להתבלט ממשתמשי Brave אחרים ועלול גם להגדיל את שטח ההתקפה אם יש ניצול ב-Brave וכלל זדוני יתווסף לאחת הרשימות שבהן אתה משתמש.

</details>

- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **strict** under **Upgrade connections to HTTPS**
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Block third-party cookies** under **Block Cookies**
- [x] Select **Block fingerprinting**
- [x] Select **Prevent fingerprinting via language settings**

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net) extension.

#### Clear browsing data

- [x] בחר **נקה נתונים ביציאה**

#### Social Media Blocking

- [ ] בטל את הסימון של כל רכיבי המדיה החברתית

#### Other privacy settings

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP handling policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [x] (Optional) Select **No protection** under **Safe Browsing** (1)
- [ ] Uncheck **Allow sites to check if you have payment methods saved**
- [ ] Uncheck **IPFS Gateway** (2)
- [x] Select **Close tabs on exit**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Automatically send daily usage ping to Brave**

</div>

1. Brave's [implementation of Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) on Android **does not** proxy [Safe Browsing network requests](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) like its desktop counterpart. This means that your IP address may be seen (and logged) by Google. Note that Safe Browsing is not available for Android devices without Google Play Services.
2. InterPlanetary File System (IPFS) היא רשת מבוזרת, עמית לעמית לאחסון ושיתוף נתונים במערכת קבצים מבוזרת. אלא אם אתה משתמש בתכונה, השבת אותה.

### Leo

These options can be found in :material-menu: → **Settings** → **Leo**

- [ ] Uncheck **Show autocomplete suggestions in address bar**

### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

## Mull (Android)

<div class="admonition recommendation" markdown>

![Mull logo](assets/img/browsers/mull.svg){ align=right }

**Mull** is a privacy oriented and deblobbed Android browser based on Firefox. Compared to Firefox, it offers much greater fingerprinting protection out of the box, and disables JavaScript Just-in-Time (JIT) compilation for enhanced security. It also removes all proprietary elements from Firefox, such as replacing Google Play Services references.

[:octicons-home-16: Homepage](https://divestos.org/pages/our_apps#mull){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://divestos.org/pages/browsers#tuningFenix){ .card-link title=Documentation }
[:octicons-code-16:](https://codeberg.org/divested-mobile/mull-fenix){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-fdroid: F-Droid](https://f-droid.org/en/packages/us.spotco.fennec_dos)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Firefox (Gecko)-based browsers on Android [lack](https://bugzilla.mozilla.org/show_bug.cgi?id=1610822) [site isolation](https://wiki.mozilla.org/Project_Fission),[^1] a powerful security feature that protects against a malicious site performing a [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability))-like attack to gain access to the memory of another website you have open.[^2] Chromium-based browsers like [Brave](#brave) will provide more robust protection against malicious websites.

</div>

Enable DivestOS's [F-Droid repository](https://divestos.org/fdroid/official) to receive updates directly from the developer. Downloading Mull from the default F-Droid repo will mean your updates could be delayed by a few days or longer.

Mull enables many features upstreamed by the [Tor uplift project](https://wiki.mozilla.org/Security/Tor_Uplift) using preferences from [Arkenfox](desktop-browsers.md#arkenfox-advanced). Proprietary blobs are removed from Mozilla's code using the scripts developed for Fennec F-Droid.

### Recommended Mull Configuration

We would suggest installing [uBlock Origin](browser-extensions.md#ublock-origin) as a content blocker if you want to block trackers within Mull.

Mull comes with privacy protecting settings configured by default. You might consider configuring the **Delete browsing data on quit** options in Mull's settings if you want to close all your open tabs when quitting the app automatically, or clear other data such as browsing history and cookies automatically.

Because Mull has more advanced and strict privacy protections enabled by default compared to most browsers, some websites may not load or work properly unless you adjust those settings. You can consult this [list of known issues and workarounds](https://divestos.org/pages/broken#mull) for advice on a potential fix if you do encounter a broken site. Adjusting a setting in order to fix a website could impact your privacy/security, so make sure you fully understand any instructions you follow.

## Safari (iOS)

ב-iOS, כל אפליקציה שיכולה לגלוש באינטרנט [מוגבלת](https://developer.apple.com/app-store/review/guidelines) לשימוש ב[מסגרת WebKit](https://developer.apple.com/documentation/webkit), כך שאין סיבה קטנה להשתמש בדפדפן אינטרנט של צד שלישי.

<div class="admonition recommendation" markdown>

![Safari לוגו](assets/img/browsers/safari.svg){ align=right }

**Safari** הוא דפדפן ברירת המחדל ב - iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Privacy Report, isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites so more devices look identical), and Private Relay for those with a paid iCloud+ subscription. It also allows you to separate your browsing with different profiles and lock private tabs with your biometrics/PIN.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title=Documentation}

</details>

</div>

### Recommended Safari Configuration

We would suggest installing [AdGuard](browser-extensions.md#adguard) as a content blocker if you want to block trackers within Safari.

The following privacy/security-related options can be found in the :gear: **Settings** app → **Safari**

#### Profiles

All of your cookies, history, and website data will be separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

#### פרטיות& אבטחה

- [x] אפשר **מנע מעקב בין אתרים**

    זה מאפשר [הגנת מעקב אינטליגנטי](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp) של WebKit. התכונה מסייעת בהגנה מפני מעקב לא רצוי על ידי שימוש בלמידת מכונה במכשיר כדי לעצור עוקבים. ITP מגן מפני איומים נפוצים רבים, אך הוא אינו חוסם את כל אפיקי המעקב מכיוון שהוא נועד לא להפריע לשימושיות האתר.

- [x] Enable **Require Face ID to Unlock Private Browsing**

    This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

#### Advanced → Privacy

The **Advanced Tracking and Fingerprinting Protection** setting will randomize certain values so that it's more difficult to fingerprint you:

- [x] Select **All Browsing** or **Private Browsing**

#### דוח פרטיות

דוח הפרטיות מספק תמונה של עוקבים חוצי אתרים שכרגע מונעים ממך ליצור פרופיל באתר שבו אתה מבקר. הוא יכול גם להציג דוח שבועי כדי להראות אילו עוקבים נחסמו לאורך זמן.

ניתן לגשת לדוח הפרטיות דרך התפריט 'הגדרות דף '.

#### שמירת הפרטיות של מדידת המודעות

- [ ] השבת **פרטיות שמירה על מדידת מודעות**

מדידת קליקים על מודעה השתמשה באופן מסורתי בטכנולוגיית מעקב הפוגעת בפרטיות המשתמש. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

לתכונה יש מעט חששות פרטיות בפני עצמה, כך שבעוד שאתה יכול לבחור להשאיר אותה פועלת, אנו רואים בעובדה שהיא מושבתת אוטומטית בגלישה פרטית כאינדיקטור להשבית התכונה.

#### גלישה פרטית תמיד

פתח את Safari והקש על כפתור הכרטיסיות, הממוקם בפינה השמאלית התחתונה. לאחר מכן, הרחב את רשימת קבוצות הכרטיסיות.

- [x] בחר **פרטי**

מצב הגלישה הפרטית של Safari מציע הגנות פרטיות נוספות. גלישה פרטית משתמשת בהפעלה חדשה [>חולפת](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) עבור כל כרטיסייה, כלומר כרטיסיות מבודדות זו מזו. יש גם יתרונות פרטיות קטנים יותר עם גלישה פרטית, כגון אי שליחת כתובת של דף אינטרנט לאפל בעת שימוש בתכונת התרגום של Safari.

שימו לב שגלישה פרטית אינה שומרת קובצי עוגיות ונתוני אתר, כך שלא ניתן יהיה להישאר מחובר לאתרים. זה עשוי להיות אי נוחות.

#### iCloud Sync

סנכרון של היסטוריית ספארי, קבוצות כרטיסיות, כרטיסיות iCloud וסיסמאות שמורות הם E2EE. However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://apple.com/legal/privacy/en-ww).

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/HT212520). עבור אל **שם Apple ID שלך ← iCloud ← הגנת נתונים מתקדמת**.

- [x] הפעל **הגנת נתונים מתקדמת**

אם אתה משתמש ב-iCloud עם הגנת נתונים מתקדמת מושבתת, אנו ממליצים גם לבדוק כדי לוודא שמיקום ההורדה המוגדר כברירת מחדל של Safari מוגדר באופן מקומי במכשיר שלך. ניתן למצוא אפשרות זו ב -:gear: **הגדרות** ← **Safari** ← **כללי** ← **הורדות**.

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

### דרישות מינימליות

- חייב לתמוך בעדכונים אוטומטיים.
- Must receive engine updates from upstream releases quickly.
- Must support content blocking.
- כל שינוי שיידרש כדי להפוך את הדפדפן ליותר מכבד פרטיות לא צריך להשפיע לרעה על חוויית המשתמש.
