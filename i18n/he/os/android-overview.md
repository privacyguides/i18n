---
title: סקירה כללית של אנדרואיד
icon: simple/android
description: אנדרואיד היא מערכת הפעלה בקוד פתוח עם הגנות אבטחה חזקות, מה שהופך אותה לבחירה המובילה שלנו עבור טלפונים.
---

![לוגו אנדרואיד](../assets/img/android/android.svg){ align=right }

ה**פרויקט הקוד הפתוח של אנדרואיד** הוא מערכת הפעלה מאובטחת לנייד הכוללת [אפליקצית ארגז חול](https://source.android.com/security/app-sandbox), [אתחול מאומת](https://source.android.com/security/verifiedboot) (AVB), ו- [הרשאות](https://developer.android.com/guide/topics/permissions/overview) מערכת בקרת חזקה.

## העצה שלנו

### בחירת הפצת אנדרואיד

When you buy an Android phone, the default operating system comes bundled with apps and functionality that are not part of the Android Open Source Project. Many of these apps—even apps like the dialer which provide basic system functionality—require invasive integrations with Google Play Services, which in turn asks for privileges to access your files, contacts storage, call logs, SMS messages, location, camera, microphone, and numerous other things on your device in order for those basic system apps and many other apps to function in the first place. Frameworks like Google Play Services increase the attack surface of your device and are the source of various privacy concerns with Android.

ניתן לפתור בעיה זו באמצעות הפצת אנדרואיד מותאמת אישית שאינה מגיעה עם אינטגרציה פולשנית כזו. לרוע המזל, הפצות רבות של אנדרואיד מותאמות אישית מפרות לעתים קרובות את מודל האבטחה של אנדרואיד בכך שאינן תומכות בתכונות אבטחה קריטיות כגון AVB, הגנה לאחור, עדכוני קושחה וכן הלאה. חלק מההפצות מספקות גם רכיבי [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) אשר חושפים שורש באמצעות [ADB](https://developer.android.com/studio/command-line/adb) ודורשים [מדיניות](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) SELinux מתירנית יותר כדי להתאים לתכונות ניפוי באגים, וכתוצאה מכך משטח התקפה מוגדל נוסף ומודל אבטחה מוחלש.

באופן אידיאלי, בעת בחירת הפצת אנדרואיד מותאמת אישית, עליך לוודא שהיא מקיימת את מודל האבטחה של אנדרואיד. לכל הפחות, להפצה צריכה להיות בניית ייצור, תמיכה ב-AVB, הגנה על חזרה, עדכוני קושחה ומערכת הפעלה בזמן, ו-SELinux ב[מצב אכיפה](https://source.android.com/security/selinux/concepts#enforcement_levels). כל הפצות האנדרואיד המומלצות שלנו עומדות בקריטריונים האלה.

[המלצות מערכת אנדרואיד שלנו :material-arrow-right-drop-circle:](../android.md ""){.md-button}

### הימנע מהשתרשות

[השרשת](https://en.wikipedia.org/wiki/Rooting_(Android)) טלפונים אנדרואיד יכולים להפחית את האבטחה באופן משמעותי מכיוון שהוא מחליש את [מודל האבטחה של אנדרואיד](https://en.wikipedia.org/wiki/Android_(operating_system)#Security_and_privacy). זה יכול להפחית את הפרטיות אם יש ניצול הנעזר בירידה באבטחה. שיטות השתרשות נפוצות כוללות התעסקות ישירה במחיצת האתחול, מה שהופך את זה לבלתי אפשרי לבצע אתחול מאומת בהצלחה. אפליקציות הדורשות שורש ישנו גם את מחיצת המערכת, כלומר אתחול מאומת יצטרך להישאר מושבת. חשיפת השורש ישירות בממשק המשתמש גם מגדילה את [משטח ההתקפה](https://en.wikipedia.org/wiki/Attack_surface) של המכשיר שלך ועשויה לסייע ב[הסלמה של הרשאות](https://en.wikipedia.org/wiki/Privilege_escalation) פגיעויות ועקיפות מדיניות SELinux.

Content blockers which modify the [hosts file](https://en.wikipedia.org/wiki/Hosts_(file)) (AdAway) and firewalls (AFWall+) which require root access persistently are dangerous and should not be used. הם גם לא הדרך הנכונה לפתור את מטרותיהם המיועדות. For content blocking we suggest encrypted [DNS](../dns.md) or [VPN](../vpn.md) server blocking solutions instead. RethinkDNS, TrackerControl ו-AdAway במצב ללא-שורש יתפסו את חריץ ה-VPN (על ידי שימוש ב-VPN עם לולאה מקומית) וימנעו ממך להשתמש בשירותים לשיפור הפרטיות כגון Orbot או שרת VPN אמיתי.

AFWall+ פועל על בסיס גישת [סינון חבילות](https://en.wikipedia.org/wiki/Firewall_(computing)#Packet_filter) וייתכן שניתן לעקוף אותו במצבים מסוימים.

אנחנו לא מאמינים שקורבנות האבטחה שנעשו על ידי השתרשות טלפון שווים את יתרונות הפרטיות המפוקפקים של אפליקציות אלה.

### התקן עדכונים

חשוב לא להשתמש בגרסת [סוף החיים](https://endoflife.date/android) של אנדרואיד. גרסאות חדשות יותר של אנדרואיד לא רק מקבלות עדכוני אבטחה עבור מערכת ההפעלה אלא גם עדכונים חשובים לשיפור הפרטיות.

לדוגמה, [לפני אנדרואיד 10](https://developer.android.com/about/versions/10/privacy/changes) כל אפליקציה עם הרשאת [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) יכלו לגשת למספרים סידוריים רגישים וייחודיים של הטלפון שלך כגון [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), כרטיס ה-SIM שלך;[IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity), בעוד שכעת הם חייבים להיות אפליקציות מערכת כדי לעשות זאת. אפליקציות מערכת מסופקות רק על ידי הפצת OEM או אנדרואיד.

### שיתוף מדיה

אתה יכול להימנע ממתן הרשאות לאפליקציות רבות לגשת למדיה שלך עם תכונות השיתוף המובנות של אנדרואיד. יישומים רבים מאפשרים לך "לשתף" איתם קובץ להעלאת מדיה.

לדוגמה, אם אתה רוצה לפרסם תמונה ל-Discord אתה יכול לפתוח את מנהל הקבצים או הגלריה שלך ולשתף את התמונה עם אפליקציית Discord, במקום להעניק ל-Discord גישה מלאה למדיה ולתמונות שלך.

## הגנות אבטחה

### אתחול מאומת

[אתחול מאומת](https://source.android.com/security/verifiedboot) הוא חלק חשוב ממודל האבטחה של אנדרואיד. הוא מספק הגנה מפני התקפות [משרתת רעה](https://en.wikipedia.org/wiki/Evil_maid_attack), התמדה של תוכנות זדוניות, ומבטיח שלא ניתן לשדרג לאחור עדכוני אבטחה עם [הגנה לאחור](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection).

אנדרואיד 10 ומעלה עברה מהצפנה בדיסק מלא ל[הצפנה מבוססת קבצים](https://source.android.com/security/encryption/file-based) גמישה יותר. הנתונים שלך מוצפנים באמצעות מפתחות הצפנה ייחודיים, וקבצי מערכת ההפעלה נותרים לא מוצפנים.

אתחול מאומת מבטיח את שלמות קבצי מערכת ההפעלה, ובכך מונע מיריב בעל גישה פיזית לחבל או להתקין תוכנה זדונית במכשיר. במקרה הבלתי סביר שתוכנות זדוניות מסוגלות לנצל חלקים אחרים של המערכת ולהשיג גישה מוסמכת יותר, אתחול מאומת ימנע ותחזיר שינויים במחיצת המערכת עם אתחול המכשיר מחדש.

למרבה הצער, יצרני ציוד מקורי מחויבים לתמוך באתחול מאומת רק בהפצת אנדרואיד בברירת מחדל שלהם. רק כמה יצרני OEM כגון גוגל תומכים ברישום מפתח AVB מותאם אישית במכשירים שלהם. בנוסף, חלק מנגזרות AOSP כגון LineageOS או /e/ OS אינן תומכות ב-Verified Boot אפילו בחומרה עם תמיכה ב-Verified Boot עבור מערכות הפעלה של צד שלישי. אנו ממליצים לבדוק אם יש תמיכה **לפני** רכישת מכשיר חדש. נגזרות AOSP שאינן תומכות באתחול מאומת **לא** מומלצות.

יצרני OEM רבים גם עשו יישום שבור של אתחול מאומת שעליך להיות מודע אליו מעבר לשיווק שלהם. לדוגמה, ה-Fairphone 3 ו-4 אינם מאובטחים כברירת מחדל, מכיוון ש[מטען האתחול של הברירת מחדל סומך על מפתח החתימה הציבורי של ](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11)AVB. זה שובר אתחול מאומת במכשיר Fairphone ברירת מחדל, מכיוון שהמערכת תאתחל מערכות הפעלה חלופיות של אנדרואיד כגון (כגון /e/) [ללא כל אזהרה](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) לגבי שימוש מותאם אישית במערכת ההפעלה.

### עדכוני קושחה

עדכוני קושחה הם קריטיים לשמירה על האבטחה ובלעדיהם המכשיר שלך לא יכול להיות מאובטח. ליצרני ציוד מקורי יש הסכמי תמיכה עם השותפים שלהם כדי לספק את רכיבי הקוד הסגור לתקופת תמיכה מוגבלת. אלה מפורטים ב[עלוני האבטחה של אנדרואיד](https://source.android.com/security/bulletin) החודשיים.

מכיוון שרכיבי הטלפון, כגון טכנולוגיות המעבד והרדיו, מסתמכים על רכיבי קוד סגור, העדכונים חייבים להיות מסופקים על ידי היצרנים המתאימים. לכן, חשוב שתרכוש מכשיר בתוך מחזור תמיכה פעיל. [קוואלקום](https://www.qualcomm.com/news/releases/2020/12/16/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) ו[סמסונג](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox/) תומכות במכשירים שלהן במשך 4 שנים, בעוד שלמוצרים זולים יותר יש לרוב מחזורי תמיכה קצרים יותר. With the introduction of the [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google now makes their own SoC, and they will provide a minimum of 5 years of support. With the introduction of the Pixel 8 series, Google increased that support window to 7 years.

מכשירי EOL שאינם נתמכים עוד על ידי יצרן ה-SoC אינם יכולים לקבל עדכוני קושחה מספקי OEM או מפיצי אנדרואיד לאחר השוק. משמעות הדבר היא שבעיות אבטחה במכשירים אלה יישארו ללא תיקון.

Fairphone, for example, markets their Fairphone 4 device as receiving 6 years of support. עם זאת, ל-SoC (Qualcomm Snapdragon 750G ב-Fairphone 4) יש תאריך EOL קצר בהרבה. המשמעות היא שעדכוני אבטחת קושחה מ-Qualcomm עבור Fairphone 4 יסתיימו בספטמבר 2023, ללא קשר לשאלה אם Fairphone תמשיך לשחרר עדכוני אבטחה תוכנה.

### הרשאות אנדרואיד

[הרשאות ב-אנדרואיד](https://developer.android.com/guide/topics/permissions/overview) מעניקות לך שליטה על האפליקציות המורשות לגשת. גוגל מבצעת בקביעות [שיפורים](https://developer.android.com/about/versions/11/privacy/permissions) במערכת ההרשאות בכל גרסה עוקבת. כל האפליקציות שאתה מתקין הן אך ורק [ארגז חול](https://source.android.com/security/app-sandbox), לכן, אין צורך להתקין אפליקציות אנטי וירוס.

סמארטפון עם הגרסה העדכנית ביותר של אנדרואיד תמיד יהיה מאובטח יותר מסמארטפון ישן עם אנטי וירוס ששילמת עליו. עדיף לא לשלם על תוכנת אנטי וירוס ולחסוך כסף בקניית סמארטפון חדש כמו גוגל פיקסל.

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

- A permission for [nearby Wi-Fi access](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). The MAC addresses of nearby Wi-Fi access points was a popular way for apps to track a user's location.
- [הרשאות מדיה מפורטות](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions) יותר, כלומר אתה יכול להעניק גישה לתמונות, סרטונים או קבצי אודיו בלבד.
- שימוש ברקע בחיישנים מחייב כעת את הרשאת [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission).

אפליקציה עשויה לבקש הרשאה עבור תכונה ספציפית שיש לה. לדוגמה, כל אפליקציה שיכולה לסרוק קודי QR תדרוש את אישור המצלמה. אפליקציות מסוימות יכולות לבקש יותר הרשאות ממה שהן צריכות.

[Exodus](https://exodus-privacy.eu.org/) יכול להיות שימושי כאשר משווים אפליקציות שיש להן מטרות דומות. אם אפליקציה דורשת הרבה הרשאות ויש לה הרבה פרסום וניתוח זה כנראה סימן רע. אנו ממליצים להסתכל על העוקבים הבודדים ולקרוא את התיאורים שלהם במקום פשוט **לספור את הסכום הכולל** ולהנחה שכל הפריטים הרשומים שווים.

!!! warning "אזהרה"

    אם אפליקציה היא ברובה שירות מבוסס אינטרנט, המעקב עשוי להתרחש בצד השרת. [פייסבוק](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest/) מציג "ללא עוקבים" אבל בהחלט עוקב אחר תחומי העניין וההתנהגות של המשתמשים ברחבי האתר. אפליקציות עשויות להתחמק מזיהוי על ידי אי שימוש בספריות קוד סטנדרטיות המיוצרות על ידי תעשיית הפרסום, אם כי זה לא סביר.

!!! note "הערה"

    אפליקציות ידידותיות לפרטיות כגון [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest/) עשויות להציג עוקבים מסוימים כגון [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49/). ספרייה זו כוללת את [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) שיכולה לספק [הודעות דחיפה](https://en.wikipedia.org/wiki/Push_technology) באפליקציות. זה [המקרה](https://fosstodon.org/@bitwarden/109636825700482007) עם Bitwarden. זה לא אומר ש-Bitwarden משתמש בכל תכונות הניתוח שמסופקות על ידי Google Firebase Analytics.

## תכונות פרטיות

### פרופילי משתמשים

ניתן למצוא פרופילי משתמש מרובים ב**הגדרות** ← **מערכת** ← **משתמש מרובים** והם הדרך הפשוטה ביותר לבודד באנדרואיד.

עם פרופילי משתמש, אתה יכול להטיל הגבלות על פרופיל ספציפי, כגון: ביצוע שיחות, שימוש ב-SMS או התקנת אפליקציות במכשיר. כל פרופיל מוצפן באמצעות מפתח הצפנה משלו ואינו יכול לגשת לנתונים של אף פרופיל אחר. אפילו בעל המכשיר לא יכול לראות את הנתונים של פרופילים אחרים מבלי לדעת את הסיסמה שלהם. פרופילי משתמשים מרובים הם שיטה בטוחה יותר לבידוד.

### פרופיל עבודה

[פרופילי עבודה](https://support.google.com/work/android/answer/6191949) הם דרך נוספת לבודד אפליקציות בודדות ועשויה להיות נוחה יותר מפרופילי משתמשים נפרדים.

יישום **בקר מכשיר** כגון [Shelter](../android.md#shelter) נדרש ליצירת פרופיל עבודה ללא ארגון MDM, אלא אם אתה משתמש במערכת הפעלה אנדרואיד מותאמת אישית הכוללת אחת.

פרופיל העבודה תלוי בבקר התקן כדי לתפקד. תכונות כגון *מעבורת קבצים* ו*חסימת חיפוש אנשי קשר* או כל סוג של תכונות בידוד חייבות להיות מיושמות על ידי הבקר. You must also fully trust the device controller app, as it has full access to your data inside the work profile.

שיטה זו בדרך כלל פחות מאובטחת מפרופיל משתמש משני; עם זאת, זה כן מאפשר לך את הנוחות של הפעלת אפליקציות בפרופיל העבודה וגם בפרופיל האישי בו-זמנית.

### מתג הרג VPN

Android 7 and above supports a VPN kill switch, and it is available without the need to install third-party apps. תכונה זו יכולה למנוע דליפות אם ה-VPN מנותק. ניתן למצוא אותו ב:gear: **הגדרות** ← **רשת & אינטרנט** ← **VPN** ← :gear: ← **חסום חיבורים ללא VPN**.

### בוררים גלובליים

למכשירי אנדרואיד מודרניים יש בוררים גלובליים לביטול Bluetooth ושירותי מיקום. אנדרואיד 12 הציגה מתגים למצלמה ולמיקרופון. כאשר אינו בשימוש, אנו ממליצים להשבית את התכונות הללו. אפליקציות לא יכולות להשתמש בתכונות מושבתות (גם אם ניתנה הרשאה אישית) עד להפעלה מחדש.

## שירותי גוגל

אם אתה משתמש במכשיר עם שירותי Google, בין אם מערכת ההפעלה ברירת מחדל שלך או מערכת הפעלה המארחת בבטחה את שירותי Google Play כמו GrapheneOS, ישנם מספר שינויים נוספים שתוכל לבצע כדי לשפר את הפרטיות שלך. אנו עדיין ממליצים להימנע לחלוטין משירותי Google, או להגביל את שירותי Google Play לפרופיל משתמש/עבודה ספציפי על ידי שילוב של בקר מכשיר כמו *Shelter* עם Google Play Sandboxed של GrapheneOS.

### תוכנית הגנה מתקדמת

אם יש לך חשבון Google, אנו מציעים להירשם ל[תוכנית ההגנה המתקדמת](https://landing.google.com/advancedprotection/). הוא זמין ללא עלות לכל מי שיש לו שני מפתחות אבטחה חומרה או יותר עם תמיכה ב-[FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online).

תוכנית ההגנה המתקדמת מספקת ניטור איומים משופר ומאפשרת:

- Stricter two-factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](https://en.wikipedia.org/wiki/OAuth)
- רק גוגל ואפליקציות צד שלישי מאומתות יכולות לגשת לנתוני החשבון
- סריקה של הודעות אימייל נכנסות בחשבונות Gmail עבור ניסיונות [דיוג](https://en.wikipedia.org/wiki/Phishing#Email_phishing)
- [סריקת דפדפן בטוחה](https://www.google.com/chrome/privacy/whitepaper.html#malware) מחמירה יותר עם Google Chrome
- תהליך שחזור מחמיר עבור חשבונות עם אישורים שאבדו

 אם אתה משתמש בשירותי Google Play שאינם בארגז חול (נפוצים במערכות הפעלה במלאי), תוכנית ההגנה המתקדמת מגיעה גם עם [הטבות נוספות](https://support.google.com/accounts/answer/9764949?hl=en) כגון:

- Not allowing app installation outside the Google Play Store, the OS vendor's app store, or via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- סריקת מכשיר אוטומטי חובה עם [Play Protect](https://support.google.com/googleplay/answer/2812853?hl=en#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- מזהיר אותך לגבי יישומים לא מאומתים

### עדכוני מערכת Google Play

בעבר, עדכוני אבטחה אנדרואיד היו צריכים להישלח על ידי ספק מערכת ההפעלה. אנדרואיד הפכה מודולרית יותר החל מאנדרואיד 10, וגוגל יכולה לדחוף עדכוני אבטחה עבור **חלק** רכיבי מערכת באמצעות שירותי Play המועדפים.

אם יש לך מכשיר EOL שנשלח עם אנדרואיד 10 ומעלה ואינך יכול להריץ אף אחת ממערכות ההפעלה המומלצות שלנו במכשיר שלך, סביר להניח שעדיף לך להישאר עם התקנת האנדרואיד של היצרן ציוד המקורי (בניגוד למערכת הפעלה שאינה מופיעה ברשימה כאן כגון LineageOS או /e/ OS). זה יאפשר לך לקבל **כמה** תיקוני אבטחה מגוגל, מבלי להפר את מודל האבטחה של אנדרואיד על ידי שימוש בנגזרת אנדרואיד לא מאובטחת והגדלת משטח ההתקפה שלך. אנו עדיין ממליצים לשדרג למכשיר נתמך בהקדם האפשרי.

### מזהה פרסום

כל המכשירים עם שירותי Google Play מותקנים באופן אוטומטי מייצרים [מזהה פרסום](https://support.google.com/googleplay/android-developer/answer/6048248?hl=en) המשמש לפרסום ממוקד. השבת תכונה זו כדי להגביל את הנתונים שנאספו עליך.

בהפצות אנדרואיד עם [Google Play בארגז חול](https://grapheneos.org/usage#sandboxed-google-play), עבור אל :gear: **הגדרות** ← **אפליקציות** ← **Google Play בארגז חול** ← **הגדרות גוגל** ← **מודעות**, ותבחר *מחק מזהה פרסום*.

בהפצות אנדרואיד עם שירותי Google Play מורשים (כגון מערכת הפעלה ברירת מחדל), ההגדרה עשויה להיות באחד מכמה מיקומים. בדיקה

- :gear: **הגדרות** ← **גוגל** ← **מודעות**
- :gear: **הגדרות** ← **פרטיות** ← **מודעות**

תינתן לך האפשרות למחוק את מזהה הפרסום שלך או *לבטל את הסכמתך למודעות מבוססות עניין*, זה משתנה בין הפצות OEM של אנדרואיד. אם מוצגת האפשרות למחוק את מזהה הפרסום המועדף. אם לא, הקפד לבטל את הסכמתך ולאפס את מזהה הפרסום שלך.

### SafetyNet ו-Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) וה[ממשק API של Play Integrity](https://developer.android.com/google/play/integrity) משמשים בדרך כלל עבור [אפליקציות בנקאיות](https://grapheneos.org/usage#banking-apps). אפליקציות בנקאות רבות יעבדו מצוין ב-GrapheneOS עם שירותי Play בארגז חול, אולם לחלק מהאפליקציות הלא פיננסיות יש מנגנוני אנטי-שיבוש גולמיים משלהם שעלולים להיכשל. GrapheneOS עובר את בדיקת `basicIntegrity`, אך לא את בדיקת האישור `ctsProfileMatch`. למכשירים עם אנדרואיד 8 ואילך יש תמיכה באישורי חומרה שלא ניתן לעקוף ללא מפתחות דלופים או פגיעויות חמורות.

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt out if you don't want your credit rating and personal information shared with affiliate marketing services.
