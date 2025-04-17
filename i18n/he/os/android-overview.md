---
title: Android Overview
icon: simple/android
description: Android is an open-source operating system with strong security protections, which makes it our top choice for phones.
robots: nofollow, max-snippet:-1, max-image-preview:large
---

![לוגו אנדרואיד](../assets/img/android/android.svg){ align=right }

ה**פרויקט הקוד הפתוח של אנדרואיד** הוא מערכת הפעלה מאובטחת לנייד הכוללת [אפליקצית ארגז חול](https://source.android.com/security/app-sandbox), [אתחול מאומת](https://source.android.com/security/verifiedboot) (AVB), ו- [הרשאות](https://developer.android.com/guide/topics/permissions/overview) מערכת בקרת חזקה.

[:octicons-home-16:](https://source.android.com){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/main){ .card-link title="Source Code" }

[Our Android Advice :material-arrow-right-drop-circle:](../android/index.md ""){.md-button.md-button--primary}

## הגנות אבטחה

Key components of the Android security model include [verified boot](#verified-boot), [firmware updates](#firmware-updates), and a robust [permission system](#android-permissions). These important security features form the baseline of the minimum criteria for our [mobile phone](../mobile-phones.md) and [custom Android OS](../android/distributions.md) recommendations.

### אתחול מאומת

[**Verified Boot**](https://source.android.com/security/verifiedboot) is an important part of the Android security model. הוא מספק הגנה מפני התקפות [משרתת רעה](https://en.wikipedia.org/wiki/Evil_maid_attack), התמדה של תוכנות זדוניות, ומבטיח שלא ניתן לשדרג לאחור עדכוני אבטחה עם [הגנה לאחור](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection).

אנדרואיד 10 ומעלה עברה מהצפנה בדיסק מלא ל[הצפנה מבוססת קבצים](https://source.android.com/security/encryption/file-based) גמישה יותר. הנתונים שלך מוצפנים באמצעות מפתחות הצפנה ייחודיים, וקבצי מערכת ההפעלה נותרים לא מוצפנים.

אתחול מאומת מבטיח את שלמות קבצי מערכת ההפעלה, ובכך מונע מיריב בעל גישה פיזית לחבל או להתקין תוכנה זדונית במכשיר. במקרה הבלתי סביר שתוכנות זדוניות מסוגלות לנצל חלקים אחרים של המערכת ולהשיג גישה מוסמכת יותר, אתחול מאומת ימנע ותחזיר שינויים במחיצת המערכת עם אתחול המכשיר מחדש.

למרבה הצער, יצרני ציוד מקורי מחויבים לתמוך באתחול מאומת רק בהפצת אנדרואיד בברירת מחדל שלהם. רק כמה יצרני OEM כגון גוגל תומכים ברישום מפתח AVB מותאם אישית במכשירים שלהם. בנוסף, חלק מנגזרות AOSP כגון LineageOS או /e/ OS אינן תומכות ב-Verified Boot אפילו בחומרה עם תמיכה ב-Verified Boot עבור מערכות הפעלה של צד שלישי. אנו ממליצים לבדוק אם יש תמיכה **לפני** רכישת מכשיר חדש. נגזרות AOSP שאינן תומכות באתחול מאומת **לא** מומלצות.

יצרני OEM רבים גם עשו יישום שבור של אתחול מאומת שעליך להיות מודע אליו מעבר לשיווק שלהם. לדוגמה, ה-Fairphone 3 ו-4 אינם מאובטחים כברירת מחדל, מכיוון ש[מטען האתחול של הברירת מחדל סומך על מפתח החתימה הציבורי של ](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11)AVB. This breaks verified boot on a stock Fairphone device, as the system will boot alternative Android operating systems (such as /e/) [without any warning](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) about custom operating system usage.

### עדכוני קושחה

**Firmware updates** are critical for maintaining security and without them your device cannot be secure. ליצרני ציוד מקורי יש הסכמי תמיכה עם השותפים שלהם כדי לספק את רכיבי הקוד הסגור לתקופת תמיכה מוגבלת. אלה מפורטים ב[עלוני האבטחה של אנדרואיד](https://source.android.com/security/bulletin) החודשיים.

מכיוון שרכיבי הטלפון, כגון טכנולוגיות המעבד והרדיו, מסתמכים על רכיבי קוד סגור, העדכונים חייבים להיות מסופקים על ידי היצרנים המתאימים. לכן, חשוב שתרכוש מכשיר בתוך מחזור תמיכה פעיל. [Qualcomm](https://qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) and [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox) support their devices for 4 years, while cheaper products often have shorter support cycles. With the introduction of the [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google now makes their own SoC, and they will provide a minimum of 5 years of support. With the introduction of the Pixel 8 series, Google increased that support window to 7 years.

מכשירי EOL שאינם נתמכים עוד על ידי יצרן ה-SoC אינם יכולים לקבל עדכוני קושחה מספקי OEM או מפיצי אנדרואיד לאחר השוק. משמעות הדבר היא שבעיות אבטחה במכשירים אלה יישארו ללא תיקון.

Fairphone, for example, markets their Fairphone 4 device as receiving 6 years of support. עם זאת, ל-SoC (Qualcomm Snapdragon 750G ב-Fairphone 4) יש תאריך EOL קצר בהרבה. המשמעות היא שעדכוני אבטחת קושחה מ-Qualcomm עבור Fairphone 4 יסתיימו בספטמבר 2023, ללא קשר לשאלה אם Fairphone תמשיך לשחרר עדכוני אבטחה תוכנה.

### הרשאות אנדרואיד

[**Permissions on Android**](https://developer.android.com/guide/topics/permissions/overview) grant you control over what apps are allowed to access. גוגל מבצעת בקביעות [שיפורים](https://developer.android.com/about/versions/11/privacy/permissions) במערכת ההרשאות בכל גרסה עוקבת. כל האפליקציות שאתה מתקין הן אך ורק [ארגז חול](https://source.android.com/security/app-sandbox), לכן, אין צורך להתקין אפליקציות אנטי וירוס.

סמארטפון עם הגרסה העדכנית ביותר של אנדרואיד תמיד יהיה מאובטח יותר מסמארטפון ישן עם אנטי וירוס ששילמת עליו. It's better not to pay for antivirus software and to save money to buy a new smartphone such as a [Google Pixel](../mobile-phones.md#google-pixel).

אנדרואיד 10:

- [אחסון בהיקף](https://developer.android.com/about/versions/10/privacy/changes#scoped-storage) נותן לך שליטה רבה יותר על הקבצים שלך ויכול להגביל את מה שיכול [לגשת לאחסון חיצוני](https://developer.android.com/training/data-storage#permissions). לאפליקציות יכולות להיות ספרייה ספציפית באחסון חיצוני וכן יכולת לאחסן שם סוגים ספציפיים של מדיה.
- גישה הדוקה יותר ב[מיקום המכשיר](https://developer.android.com/about/versions/10/privacy/changes#app-access-device-location) על ידי הצגת ההרשאה `ACCESS_BACKGROUND_LOCATION `. זה מונע מאפליקציות לגשת למיקום כשהן פועלות ברקע ללא אישור מפורש מהמשתמש.

אנדרואיד 11:

- [הרשאות חד פעמיות](https://developer.android.com/about/versions/11/privacy/permissions#one-time) מאפשרות לך להעניק הרשאה לאפליקציה פעם אחת בלבד.
- [הרשאות איפוס אוטומטי](https://developer.android.com/about/versions/11/privacy/permissions#auto-reset), המאפס [הרשאות זמן ריצה](https://developer.android.com/guide/topics/permissions/overview#runtime) שניתנו בעת פתיחת האפליקציה.
- הרשאות מפורטות לגישה לתכונות הקשורות ל[מספרי טלפון](https://developer.android.com/about/versions/11/privacy/permissions#phone-numbers).

אנדרואיד 12:

- הרשאה להעניק רק את ה[מיקום המשוער](https://developer.android.com/about/versions/12/behavior-changes-12#approximate-location).
- איפוס אוטומטי של [אפליקציות במצב שינה](https://developer.android.com/about/versions/12/behavior-changes-12#app-hibernation).
- [ביקורת גישה לנתונים](https://developer.android.com/about/versions/12/behavior-changes-12#data-access-auditing) שמקלה לקבוע איזה חלק באפליקציה מבצע סוג מסוים של גישה לנתונים.

אנדרואיד 13:

- A permission for [nearby Wi-Fi access](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). The MAC addresses of nearby Wi-Fi access points were a popular way for apps to track a user's location.
- [הרשאות מדיה מפורטות](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions) יותר, כלומר אתה יכול להעניק גישה לתמונות, סרטונים או קבצי אודיו בלבד.
- שימוש ברקע בחיישנים מחייב כעת את הרשאת [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission).

אפליקציה עשויה לבקש הרשאה עבור תכונה ספציפית שיש לה. לדוגמה, כל אפליקציה שיכולה לסרוק קודי QR תדרוש את אישור המצלמה. אפליקציות מסוימות יכולות לבקש יותר הרשאות ממה שהן צריכות.

[Exodus](https://exodus-privacy.eu.org) can be useful when comparing apps that have similar purposes. אם אפליקציה דורשת הרבה הרשאות ויש לה הרבה פרסום וניתוח זה כנראה סימן רע. אנו ממליצים להסתכל על העוקבים הבודדים ולקרוא את התיאורים שלהם במקום פשוט **לספור את הסכום הכולל** ולהנחה שכל הפריטים הרשומים שווים.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

אם אפליקציה היא ברובה שירות מבוסס אינטרנט, המעקב עשוי להתרחש בצד השרת. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest) shows "no trackers" but certainly does track users' interests and behavior across the site. אפליקציות עשויות להתחמק מזיהוי על ידי אי שימוש בספריות קוד סטנדרטיות המיוצרות על ידי תעשיית הפרסום, אם כי זה לא סביר.

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Privacy-friendly apps such as [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest) may show some trackers such as [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49). ספרייה זו כוללת את [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) שיכולה לספק [הודעות דחיפה](https://en.wikipedia.org/wiki/Push_technology) באפליקציות. זה [המקרה](https://fosstodon.org/@bitwarden/109636825700482007) עם Bitwarden. That doesn't mean that Bitwarden is using all the analytics features that are provided by Google Firebase Analytics.

</div>

## תכונות פרטיות

### פרופילי משתמשים

Multiple **user profiles** can be found in :gear: **Settings** → **System** → **Users** and are the simplest way to isolate in Android.

With user profiles, you can impose restrictions on a specific profile, such as: making calls, using SMS, or installing apps. כל פרופיל מוצפן באמצעות מפתח הצפנה משלו ואינו יכול לגשת לנתונים של אף פרופיל אחר. אפילו בעל המכשיר לא יכול לראות את הנתונים של פרופילים אחרים מבלי לדעת את הסיסמה שלהם. פרופילי משתמשים מרובים הם שיטה בטוחה יותר לבידוד.

### פרופיל עבודה

[**Work Profiles**](https://support.google.com/work/android/answer/6191949) are another way to isolate individual apps and may be more convenient than separate user profiles.

A **device controller** app such as [Shelter](../android/general-apps.md#shelter) is required to create a Work Profile without an enterprise MDM, unless you're using a custom Android OS which includes one.

פרופיל העבודה תלוי בבקר התקן כדי לתפקד. תכונות כגון *מעבורת קבצים* ו*חסימת חיפוש אנשי קשר* או כל סוג של תכונות בידוד חייבות להיות מיושמות על ידי הבקר. You must also fully trust the device controller app, as it has full access to your data inside the work profile.

This method is generally less secure than a secondary user profile; however, it does allow you the convenience of running apps in both the owner profile and work profile simultaneously.

### Private Space

**Private Space** is a feature introduced in Android 15 that adds another way of isolating individual apps. You can set up a private space in the owner profile by navigating to :gear: **Settings** → **Security & privacy** → **Private space**. Once set up, your private space resides at the bottom of the app drawer.

Like user profiles, a private space is encrypted using its own encryption key, and you have the option to set up a different unlock method. Like work profiles, you can use apps from both the owner profile and private space simultaneously. Apps launched from a private space are distinguished by an icon depicting a key within a shield.

Unlike work profiles, Private Space is a feature native to Android that does not require a third-party app to manage it. For this reason, we generally recommend using a private space over a work profile, though you can use a work profile alongside a private space.

### VPN kill switch

Android 7 and above supports a VPN kill switch, and it is available without the need to install third-party apps. תכונה זו יכולה למנוע דליפות אם ה-VPN מנותק. ניתן למצוא אותו ב:gear: **הגדרות** ← **רשת & אינטרנט** ← **VPN** ← :gear: ← **חסום חיבורים ללא VPN**.

### בוררים גלובליים

למכשירי אנדרואיד מודרניים יש בוררים גלובליים לביטול Bluetooth ושירותי מיקום. אנדרואיד 12 הציגה מתגים למצלמה ולמיקרופון. כאשר אינו בשימוש, אנו ממליצים להשבית את התכונות הללו. Apps cannot use disabled features (even if granted individual permissions) until re-enabled.

## שירותי גוגל

If you are using a device with Google services—whether with the stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS—there are a number of additional changes you can make to improve your privacy. We still recommend avoiding Google services entirely, or limiting Google Play Services to a specific user/work profile by combining a device controller like *Shelter* with GrapheneOS's Sandboxed Google Play.

### תוכנית הגנה מתקדמת

If you have a Google account we suggest enrolling in the [Advanced Protection Program](https://landing.google.com/advancedprotection). הוא זמין ללא עלות לכל מי שיש לו שני מפתחות אבטחה חומרה או יותר עם תמיכה ב-[FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online). Alternatively, you can use [passkeys](https://fidoalliance.org/passkeys).

תוכנית ההגנה המתקדמת מספקת ניטור איומים משופר ומאפשרת:

- Stricter two-factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](../basics/account-creation.md#sign-in-with-oauth)
- רק גוגל ואפליקציות צד שלישי מאומתות יכולות לגשת לנתוני החשבון
- סריקה של הודעות אימייל נכנסות בחשבונות Gmail עבור ניסיונות [דיוג](https://en.wikipedia.org/wiki/Phishing#Email_phishing)
- Stricter [safe browser scanning](https://google.com/chrome/privacy/whitepaper.html#malware) with Google Chrome
- תהליך שחזור מחמיר עבור חשבונות עם אישורים שאבדו

 If you use non-sandboxed Google Play Services (common on stock operating systems), the Advanced Protection Program also comes with [additional benefits](https://support.google.com/accounts/answer/9764949) such as:

- Not allowing app installation outside the Google Play Store, the OS vendor's app store, or via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Mandatory automatic device scanning with [Play Protect](https://support.google.com/googleplay/answer/2812853?#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- מזהיר אותך לגבי יישומים לא מאומתים

### עדכוני מערכת Google Play

בעבר, עדכוני אבטחה אנדרואיד היו צריכים להישלח על ידי ספק מערכת ההפעלה. אנדרואיד הפכה מודולרית יותר החל מאנדרואיד 10, וגוגל יכולה לדחוף עדכוני אבטחה עבור **חלק** רכיבי מערכת באמצעות שירותי Play המועדפים.

אם יש לך מכשיר EOL שנשלח עם אנדרואיד 10 ומעלה ואינך יכול להריץ אף אחת ממערכות ההפעלה המומלצות שלנו במכשיר שלך, סביר להניח שעדיף לך להישאר עם התקנת האנדרואיד של היצרן ציוד המקורי (בניגוד למערכת הפעלה שאינה מופיעה ברשימה כאן כגון LineageOS או /e/ OS). זה יאפשר לך לקבל **כמה** תיקוני אבטחה מגוגל, מבלי להפר את מודל האבטחה של אנדרואיד על ידי שימוש בנגזרת אנדרואיד לא מאובטחת והגדלת משטח ההתקפה שלך. אנו עדיין ממליצים לשדרג למכשיר נתמך בהקדם האפשרי.

### מזהה פרסום

All devices with Google Play Services installed automatically generate an [advertising ID](https://support.google.com/googleplay/android-developer/answer/6048248) used for targeted advertising. השבת תכונה זו כדי להגביל את הנתונים שנאספו עליך.

On Android distributions with [sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), go to :gear: **Settings** → **Apps** → **Sandboxed Google Play** → **Google Settings** → **All services** → **Ads**.

- [x] Select **Delete advertising ID**

On Android distributions with privileged Google Play Services (which includes the stock installation on most devices), the setting may be in one of several locations. בדיקה

- :gear: **הגדרות** ← **גוגל** ← **מודעות**
- :gear: **הגדרות** ← **פרטיות** ← **מודעות**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads* (this varies between OEM distributions of Android). If presented with the option to delete the advertising ID, that is preferred. אם לא, הקפד לבטל את הסכמתך ולאפס את מזהה הפרסום שלך.

### SafetyNet ו-Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) וה[ממשק API של Play Integrity](https://developer.android.com/google/play/integrity) משמשים בדרך כלל עבור [אפליקציות בנקאיות](https://grapheneos.org/usage#banking-apps). אפליקציות בנקאות רבות יעבדו מצוין ב-GrapheneOS עם שירותי Play בארגז חול, אולם לחלק מהאפליקציות הלא פיננסיות יש מנגנוני אנטי-שיבוש גולמיים משלהם שעלולים להיכשל. GrapheneOS עובר את בדיקת `basicIntegrity`, אך לא את בדיקת האישור `ctsProfileMatch`. למכשירים עם אנדרואיד 8 ואילך יש תמיכה באישורי חומרה שלא ניתן לעקוף ללא מפתחות דלופים או פגיעויות חמורות.

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt out if you don't want your credit rating and personal information shared with affiliate marketing services.
