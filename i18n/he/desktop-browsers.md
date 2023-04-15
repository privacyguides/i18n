---
meta_title: "Privacy Respecting Web Browsers for PC and Mac - Privacy Guides"
title: "דפדפנים שולחניים"
icon: material/laptop
description: These web browsers provide stronger privacy protections than Google Chrome.
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
      - Windows
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
    sameAs: https://en.wikipedia.org/wiki/Firefox
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
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
      - Windows
      - macOS
      - לינוקס
    subjectOf:
      "@type": WebPage
      url: "./"
---

אלה הדפדפנים והתצורות המומלצים כרגע לגלישה רגילה/לא אנונימית. We recommend [Mullvad Browser](#mullvad-browser) if you are focused on strong privacy protections and anti-fingerprinting out of the box, [Firefox](#firefox) for casual internet browsers looking for a good alternative to Google Chrome, and [Brave](#brave) if you need Chromium browser compatibility.

אם אתה צריך לגלוש באינטרנט באופן אנונימי, אתה צריך להשתמש [Tor](tor.md) במקום. We make some configuration recommendations on this page, but all browsers other than Tor Browser will be traceable by *somebody* in some manner or another.

## Mullvad Browser

!!! recommendation

    ![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    **Mullvad Browser** is a version of [Tor Browser](tor.md#tor-browser) with Tor network integrations removed, aimed at providing Tor Browser's anti-fingerprinting browser technologies to VPN users. It is developed by the Tor Project and distributed by [Mullvad](vpn.md#mullvad), and does **not** require the use of Mullvad's VPN.
    
    [:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

Like [Tor Browser](tor.md), Mullvad Browser is designed to prevent fingerprinting by making your browser fingerprint identical to all other Mullvad Browser users, and it includes default settings and extensions that are automatically configured by the default security levels: *Standard*, *Safer* and *Safest*. Therefore, it is imperative that you do not modify the browser at all outside adjusting the default [security levels](https://tb-manual.torproject.org/security-settings/). Other modifications would make your fingerprint unique, defeating the purpose of using this browser. If you want to configure your browser more heavily and fingerprinting is not a concern for you, we recommend [Firefox](#firefox) instead.

### Anti-Fingerprinting

**Without** using a [VPN](vpn.md), Mullvad Browser provides the same protections against [naive fingerprinting scripts](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) as other private browsers like Firefox+[Arkenfox](#arkenfox-advanced) or [Brave](#brave). Mullvad Browser provides these protections out of the box, at the expense of some flexibility and convenience that other private browsers can provide.

==For the strongest anti-fingerprinting protection, we recommend using Mullvad Browser in conjunction **with** a VPN==, whether that is Mullvad or another recommended VPN provider. When using a VPN with Mullvad Browser, you will share a fingerprint and a pool of IP addresses with many other users, giving you a "crowd" to blend in with. This strategy is the only way to thwart advanced tracking scripts, and is the same anti-fingerprinting technique used by Tor Browser.

Note that while you can use Mullvad Browser with any VPN provider, other people on that VPN must also be using Mullvad Browser for this "crowd" to exist, something which is more likely on Mullvad VPN compared to other providers, particularly this close to the launch of Mullvad Browser. Mullvad Browser does not have built-in VPN connectivity, nor does it check whether you are using a VPN before browsing; your VPN connection has to be configured and managed separately.

Mullvad Browser comes with the *uBlock Origin* and *NoScript* browser extensions pre-installed. While we typically [don't recommend](#extensions) adding *additional* browser extensions, these extensions that come pre-installed with the browser should **not** be removed or configured outside their default values, because doing so would noticeably make your browser fingerprint distinct from other Mullvad Browser users. It also comes pre-installed with the Mullvad Browser Extension, which *can* be safely removed without impacting your browser fingerprint if you would like, but is also safe to keep even if you don't use Mullvad VPN.

### Private Browsing Mode

Mullvad Browser operates in permanent private browsing mode, meaning your history, cookies, and other site data will always be cleared every time the browser is closed. Your bookmarks, browser settings, and extension settings will still be preserved.

This is required to prevent advanced forms of tracking, but does come at the cost of convenience and some Firefox features, such as Multi-Account Containers. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise don't work properly in Mullvad Browser, and Mullvad Browser for general browsing.

### Mullvad Leta

Mullvad Browser comes with DuckDuckGo set as the default [search engine](search-engines.md), but it also comes preinstalled with **Mullvad Leta**, a search engine which requires an active Mullvad VPN subscription to access. Mullvad Leta queries Google's paid search API directly (which is why it is limited to paying subscribers), however because of this limitation it is possible for Mullvad to correlate search queries and Mullvad VPN accounts. For this reason we discourage the use of Mullvad Leta, even though Mullvad collects very little information about their VPN subscribers.

## Firefox

!!! recommendation

    ![לוגו Firefox](assets/img/browsers/firefox.svg){ align=right }
    
    **Firefox** מספק הגדרות פרטיות חזקות כגון [Enhanced Tracking Protection](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), שיכול לעזור לחסום שונים [סוגי מעקב](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-protection-blocks).
    
    [:octicons-home-16: דף הבית](https://firefox.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mozilla.org/privacy/firefox/){ .card-link title="מדיניות פרטיות" }
    [:octicons-info-16:](https://firefox-source-docs.mozilla.org/){ .card-link title=תיעוד}
    [:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="קוד מקור" }
    [:octicons-heart-16:](https://donate.mozilla.org/){ .card-link title=לתרומה }
    
    ??? downloads "הורדות"
    
        - [:simple-windows11: Windows](https://www.mozilla.org/firefox/windows)
        - [:simple-apple: macOS](https://www.mozilla.org/firefox/mac)
        - [:simple-linux: Linux](https://www.mozilla.org/firefox/linux)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

!!! warning "אזהרה"
    Firefox כולל [אסימון הורדה](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) ייחודי בהורדות מאתר האינטרנט של מוזילה ומשתמש בטלמטריה ב-Firefox כדי לשלוח את האסימון. האסימון **לא** כלול במהדורות מ-[Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

### תצורה מומלצת

These options can be found in :material-menu: → **Settings**

#### Search

- [ ] בטל את הסימון **הצגת המלצות חיפוש**

ייתכן שתכונות הצעות חיפוש לא יהיו זמינות באזור שלך.

הצעות חיפוש שולחות את כל מה שאתה מקליד בסרגל הכתובות למנוע החיפוש המוגדר כברירת מחדל, ללא קשר אם אתה שולח חיפוש בפועל. השבתת הצעות חיפוש מאפשרת לך לשלוט בצורה מדויקת יותר באילו נתונים אתה שולח לספק מנועי החיפוש שלך.

#### Privacy & Security

##### הגנה מוגברת מפני מעקב

- [x] בחר ** מחמיר** הגנת מעקב מתקדמת

זה מגן עליך על ידי חסימת מעקבי מדיה חברתית, סקריפטים של טביעת אצבע (שים לב שזה לא מגן עליך מפני *כל* טביעות האצבע), קריפטומינרים, עוגיות מעקב חוצות- אתרים ותוכן מעקב אחר. ETP מגן מפני איומים נפוצים רבים, אך הוא אינו חוסם את כל אפיקי המעקב מכיוון שהוא נועד להשפיע באופן מינימלי עד ללא השפעה על השימושיות באתר.

##### Firefox Suggest (US only)

[Firefox Suggest](https://support.mozilla.org/en-US/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. We recommend disabling it for the same reason we recommend disabling search suggestions. If you don't see these options under the **Address Bar** header, you do not have the new experience and can ignore these changes.

- [ ] Uncheck **Suggestions from the web**
- [ ] Uncheck **Suggestions from sponsors**

##### חיטוי בעת סגירה

אם אתה רוצה להישאר מחובר לאתרים מסוימים, אתה יכול לאפשר חריגים ב**עוגיות ונתוני אתר** ← **נהל חריגים... **

- [x] סמן **מחיקת עוגיות ונתוני אתרים עם סגירת Firefox**

זה מגן עליך מפני עוגיות מתמשכות, אך אינו מגן עליך מפני עוגיות שנרכשו במהלך כל הפעלת גלישה אחת. כאשר זה מופעל, אפשר לנקות בקלות את קובצי העוגיות של הדפדפן שלך פשוט על ידי הפעלה מחדש של Firefox. אתה יכול להגדיר חריגים על בסיס אתר, אם אתה רוצה להישאר מחובר לאתר מסוים שאתה מבקר בו לעתים קרובות.

##### טלמטריה

- [ ] בטל את הסימון **לאפשר ל-Firefox לשלוח אל Mozilla מידע טכני ופעולות שבוצעו בדפדפן**
- [ ] בטל את הסימון **לאפשר ל-Firefox להתקין ולהריץ מחקרים**
- [ ] בטל את הסימון **לאפשר ל-Firefox דיווחי קריסות שנשמרו בשמך**

> Firefox שולח נתונים על הגרסה והשפה של Firefox שלך; תצורת מערכת ההפעלה והחומרה של המכשיר; זיכרון, מידע בסיסי על קריסות ושגיאות; תוצאה של תהליכים אוטומטיים כמו עדכונים, גלישה בטוחה והפעלה אלינו. כאשר Firefox שולח לנו נתונים, כתובת ה-IP שלך נאספת זמנית כחלק מיומני השרת שלנו.

בנוסף, שירות חשבונות Firefox אוסף [כמה נתונים טכניים](https://www.mozilla.org/en-US/privacy/firefox/#firefox-accounts). אם אתה משתמש בחשבון Firefox אתה יכול לבטל את הסכמתך:

1. פתח את [הגדרות הפרופיל שלך ב ](https://accounts.firefox.com/settings#data-collection)accounts.firefox.com
2. ביטול סימון **איסוף נתונים ושימוש** > **עזרה בשיפור חשבונות Firefox**

##### מצב HTTPS בלבד

- [x] בחר **הפעלת מצב HTTPS בלבד בכל החלונות**

זה מונע ממך להתחבר ללא כוונה לאתר אינטרנט ב-HTTP בטקסט רגיל. אתרים ללא HTTPS אינם נפוצים כיום, לכן לא אמורה להיות לכך השפעה רבה על הגלישה היומיומית שלך.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) מאפשר לנתוני הגלישה שלך (היסטוריה, סימניות וכו') להיות נגישים בכל המכשירים שלך ומגן עליהם באמצעות E2EE.

### Arkenfox (מתקדם)

!!! tip "Use Mullvad Browser for advanced anti-fingerprinting"

    [Mullvad Browser](#mullvad-browser) provides the same anti-fingerprinting protections as Arkenfox out of the box, and does not require the use of Mullvad's VPN to benefit from these protections. Coupled with a VPN, Mullvad Browser can thwart more advanced tracking scripts which Arkenfox cannot. Arkenfox still has the advantage of being much more flexible, and allowing per-site exceptions for websites which you need to stay logged in to.

פרויקט [Arkenfox](https://github.com/arkenfox/user.js) מספק קבוצה של אפשרויות שנשקלו בקפידה עבור Firefox. אם אתה [מחליט](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) להשתמש ב-Arkenfox, [כמה אפשרויות](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) הן קפדניות סובייקטיבית ו/או עלולות לגרום לאתרים מסוימים לא לעבוד כראוי [שאותן תוכל לשנות בקלות](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) כדי להתאים לצרכים שלך. אנו **ממליצים בחום** לקרוא את [הויקי](https://github.com/arkenfox/user.js/wiki) המלא שלהם. Arkenfox גם מאפשר תמיכה ב[מכולות](https://support.mozilla.org/en-US/kb/containers#w_for-advanced-users).

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

## Brave

!!! recommendation

    ![Brave לוגו](assets/img/browsers/brave.svg){ align=right }
    
    **דפדפן Brave** כולל חוסם תוכן מובנה ו [תכונות פרטיות ]( https://brave.com/privacy-features/), רבים מהם מופעלים כברירת מחדל.
    
    Brave בנוי על פרויקט דפדפן Chromium, כך שהוא אמור להרגיש מוכר ושיהיו לו בעיות תאימות מינימליות לאתר.
    
    [:octicons-home-16: דף הבית](https://brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="שירות בצל" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="מדיניות פרטיות" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=תיעוד}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="קוד פתוח" }
    
    ??? downloads annotate "הורדות"
    
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
        - [:simple-windows11: Windows](https://brave.com/download/)
        - [:simple-apple: macOS](https://brave.com/download/)
        - [:simple-linux: Linux](https://brave.com/linux/) (1)

    1. אנו ממליצים לא להשתמש בגרסת Flatpak של Brave, מכיוון שהיא מחליפה את ארגז החול של Chromium ב-Flatpak, שהוא פחות יעיל. בנוסף, החבילה אינה מתוחזקת על ידי Brave Software, Inc.

### תצורה מומלצת

ניתן למצוא אפשרויות אלה ב - :material-menu: ← **הגדרות**.

#### Settings

##### Shields

Brave כולל כמה אמצעים נגד טביעת אצבע בתכונת [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-) שלו. אנו מציעים להגדיר את האפשרויות האלה [גלובלי](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) בכל הדפים שבהם אתה מבקר.

ניתן לשדרג לאחור את האפשרויות של Shields על בסיס אתר לפי הצורך, אך כברירת מחדל אנו ממליצים להגדיר את האפשרויות הבאות:

<div class="annotate" markdown>

- [x] בחר **מנע מאתרים לקחת ממני טביעות אצבע בהתבסס על העדפות השפה שלי**
- [x] בחר **אגרסיבי** תחת חסימת עוקבים ומודעות

    ??? warning "השתמש ברשימות סינון ברירת מחדל"
         Brave מאפשר לך לבחור מסנני תוכן נוספים בדף הפנימי `brave://adblock`. אנו ממליצים לא להשתמש בתכונה זו; במקום זאת, שמור על רשימות הסינון המוגדרות כברירת מחדל. שימוש ברשימות נוספות יגרום לך להתבלט ממשתמשי Brave אחרים ועלול גם להגדיל את שטח ההתקפה אם יש ניצול ב-Brave וכלל זדוני יתווסף לאחת הרשימות שבהן אתה משתמש.

- [x] (אופציונלי) בחר **בלוק סקריפטים** (1)
- [x] בחר **מחמיר, עלול לשבור אתרים** תחת בלוק טביעת אצבע

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net/) extension.

##### חסימת מדיה חברתית

- [ ] בטל את הסימון של כל רכיבי המדיה החברתית

##### פרטיות ואבטחה

<div class="annotate" markdown>

- [x] בחר **Disable Non-Proxied UDP** מתחת [WebRTC IP Handling Policy](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] בטל **שימוש בשירותי Google להעברת הודעות בדחיפה**
- [ ] בטל **אפשר ניתוח מוצרים ששומר על הפרטיות (P3A)**
- [ ] בטל **שליחה אוטומטית של פינג שימוש יומי ל-Brave**
- [x] בחר **השתמש תמיד בחיבורים מאובטחים** בתוך **אבטחה** תפריט
- [ ] בטל **חלון פרטי עם טור** (1)

    !!! tip "Sanitizing on Close"

        - [x] Select **Clear cookies and site data when you close all windows** in the *Cookies and other site data* menu

        If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

1. Brave הוא **לא** עמיד בפני טביעת אצבע כמו דפדפן Tor והרבה פחות אנשים משתמשים אמיץ עם Tor, כך תוכל להתבלט. כאשר [נדרשת אנונימיות חזקה](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-) השתמש בדפדפן [Tor](tor.md#tor-browser).

##### הרחבות

השבת הרחבות מובנות שאינך משתמש בהן ב**הרחבות**

- [ ] בטל את הסימון **Hangouts**
- [ ] בטל את הסימון **WebTorrent**

##### Web3

Brave's Web3 features can potentially add to your browser fingerprint and attack surface. Unless you use any of features, they should be disabled.

- [ ] Set **Default Ethereum Wallet** to **None**
- [ ] Set **Default Solana Wallet** to **None**
- [ ] Set **Method to resolve IPFS resources** to **Disabled

##### System

<div class="annotate" markdown>

- [ ] Uncheck **Continue running apps when Brave is closed** to disable background apps (1)

</div>

1. This option is not present on all platforms.

#### Sync

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) מאפשר לנתוני הגלישה שלך (היסטוריה, סימניות וכו ') להיות נגישים בכל המכשירים שלך ללא צורך בחשבון ומגן עליהם באמצעות E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you recieve Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#other-coins-bitcoin-ethereum-etc), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

## מקורות נוספים

In general, we recommend keeping your browser extensions to a minimum to decrease your attack surface; they have privileged access within your browser, require you to trust the developer, can make you [stand out](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), and [weaken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) site isolation. However, uBlock Origin may prove useful if you value content blocking functionality.

### uBlock Origin

!!! recommendation

    ![הלוגו של uBlock Origin](assets/img/browsers/ublock_origin.svg){ align=right }
    
    **uBlock Origin** הוא חוסם תוכן פופולרי שיכול לעזור לך לחסום מודעות, עוקבים וסקריפטים של טביעות אצבע.
    
    [:octicons-repo-16: מאגר](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="מדיניות פרטיות" }
    [:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=תיעוד}
    [:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="קוד מקור" }
    
    ??? הורדות
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

We suggest following the [developer's documentation](https://github.com/gorhill/uBlock/wiki/Blocking-mode) and picking one of the "modes". Additional filter lists can impact performance and [may increase attack surface](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

##### רשימות אחרות

These are some other [filter lists](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) that you may want to consider adding:

- [x] Check **Privacy** > **AdGuard URL Tracking Protection**
- Add [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

!!! example "חלק זה הוא חדש"

    אנו עובדים על קביעת קריטריונים מוגדרים לכל קטע באתר שלנו, והדבר עשוי להשתנות. אם יש לך שאלות כלשהן לגבי הקריטריונים שלנו, אנא [שאל בפורום שלנו](https://discuss.privacyguides.net/latest) ואל תניח שלא שקלנו משהו כשהצענו את ההמלצות שלנו אם הוא לא רשום כאן. ישנם גורמים רבים שנחשבים ונדונים כאשר אנו ממליצים על פרויקט, ותיעוד כל אחד מהם הוא עבודה בתהליך.

### דרישות מינימליות

- חייבת להיות תוכנת קוד פתוח.
- Supports automatic updates.
- Receives engine updates in 0-1 days from upstream release.
- Available on Linux, macOS, and Windows.
- כל שינוי שיידרש כדי להפוך את הדפדפן ליותר מכבד פרטיות לא צריך להשפיע לרעה על חוויית המשתמש.
- Blocks third-party cookies by default.
- Supports [state partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### המקרה הטוב ביותר

הקריטריונים הטובים ביותר שלנו מייצגים את מה שהיינו רוצים לראות מהפרויקט המושלם בקטגוריה זו. ייתכן שההמלצות שלנו לא יכללו חלק מהפונקציונליות הזו או את כולה, אך אלו שכן כן עשויות לדרג גבוה יותר מאחרות בדף זה.

- Includes built-in content blocking functionality.
- Supports cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/en-US/kb/containers)).
- Supports Progressive Web Apps.  
  PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps, because you benefit from your browser's regular security updates.
- Does not include add-on functionality (bloatware) that does not impact user privacy.
- Does not collect telemetry by default.
- Provides open-source sync server implementation.
- Defaults to a [private search engine](search-engines.md).

### קריטריונים להרחבה

- אסור לשכפל דפדפן מובנה או פונקציונליות מערכת הפעלה.
- חייב להשפיע ישירות על פרטיות המשתמש, כלומר לא חייב פשוט לספק מידע.

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state/).
