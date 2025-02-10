---
title: iOS Overview
icon: simple/apple
description: iOS is a mobile operating system developed by Apple for the iPhone.
---

**iOS** ו-**iPadOS** הן מערכות הפעלה קנייניות לנייד שפותחו על ידי אפל עבור מוצרי האייפון והאייפד שלהם, בהתאמה. אם יש לך מכשיר נייד של אפל, תוכל להגביר את הפרטיות שלך על ידי השבתת כמה תכונות טלמטריה מובנות, והקשחת הגדרות פרטיות ואבטחה המובנות במערכת.

## הערות פרטיות

iOS devices are frequently praised by security experts for their robust data protection and adherence to modern best practices. עם זאת, ההגבלה של המערכת האקולוגית של אפל - במיוחד עם המכשירים הניידים שלה - עדיין פוגעת בפרטיות במספר דרכים.

בדרך כלל אנו מחשיבים את iOS כמספקת הגנות פרטיות ואבטחה טובות מהממוצע עבור רוב האנשים, בהשוואה למכשירי אנדרואיד במלאי מכל יצרן. However, you can achieve even higher standards of privacy with a [custom Android operating system](../android/distributions.md) like GrapheneOS, if you want or need to be completely independent of Apple or Google's cloud services.

### נעילת הפעלה

כל מכשירי iOS חייבים להיבדק מול שרתי Activation Lock של אפל כאשר הם מוגדרים או מאפסים לראשונה, כלומר חיבור לאינטרנט **נדרש** כדי להשתמש במכשיר iOS.

### חנות אפליקציות חובה

The only source for apps on iOS is Apple's App Store, which requires an Apple Account to access. משמעות הדבר היא כי לאפל יש תיעוד של כל אפליקציה שאתה מתקין במכשיר שלך, וסביר להניח שהיא יכולה לקשור את המידע הזה לזהותך האמיתית אם תספק ל-App Store אמצעי תשלום.

### טלמטריה פולשנית

Apple has historically had problems with properly disassociating their telemetry from Apple Accounts on iOS. In [2019](https://theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings), Apple was found to transmit Siri recordings—some containing highly confidential information—to their servers for manual review by third-party contractors. Though Apple temporarily stopped that program after that practice was [widely reported on](https://theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana), the company rolled out a switch to [**opt out** of uploading conversations with Siri](https://theguardian.com/technology/2019/oct/30/apple-lets-users-opt-out-of-having-siri-conversations-recorded) a few months later in the succeeding iOS update. Moreover, in 2021, [Apple reworked Siri](https://theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance) so that it processes voice recordings locally rather than sending it to their servers.

More recently, Apple has been found to transmit analytics [even when analytics sharing is disabled](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) on iOS, and this data [appears](https://twitter.com/mysk_co/status/1594515229915979776) to be easily linked to unique iCloud account identifiers despite supposedly being decoupled from Apple Accounts.

### Traffic Outside Active VPN Connections

Apple's [privacy policy regarding VPNs](https://apple.com/legal/privacy/data/en/vpns) states:

> Even when a VPN is active, some traffic that is necessary for essential system services will take place outside the VPN so that your device can function properly.

## תצורה מומלצת

**Note:** This guide assumes that you're running the latest version of iOS.

### iCloud

רוב דאגות הפרטיות והאבטחה של מוצרי Apple קשורות לשירותי הענן שלהם, לא לחומרה או לתוכנה שלהם. כאשר אתה משתמש בשירותי אפל כמו iCloud, רוב המידע שלך מאוחסן בשרתים שלהם ומאובטח באמצעות מפתחות שאליהם יש לאפל גישה כברירת מחדל. תוכל לעיין ב[תיעוד של אפל](https://support.apple.com/HT202303) לקבלת מידע על השירותים המוצפנים מקצה לקצה. כל דבר המופיע כ"מעבר "או" בשרת "פירושו שאפל ניתן לגשת לנתונים אלה ללא רשותך. מדי פעם נוצלה רמת גישה זו על ידי אכיפת החוק כדי לעקוף את העובדה שהנתונים שלך מוצפנים באופן מאובטח במכשיר שלך, וכמובן שאפל חשופה להפרות נתונים כמו כל חברה אחרת.

לכן, אם אתה משתמש ב- iCloud עליך ל [ אפשר ** הגנה על נתונים מתקדמת ** ](https://support.apple.com/ht212520). זה מצפן כמעט את כל נתוני ה- iCloud שלך עם מפתחות המאוחסנים במכשירים שלך (הצפנה מקצה לקצה), ולא בשרתים של אפל, כך שנתוני ה- iCloud שלך יאובטחו במקרה של הפרת נתונים, ובאופן אחר מוסתר מאפל.

ההצפנה המשמשת את הגנת הנתונים המתקדמת, למרות שהיא חזקה, [אינה *ממש* חזקה](https://discuss.privacyguides.net/t/apple-advances-user-security-with-powerful-new-data-protections/10778/4) כמו ההצפנה המוצעת על ידי [שירותי ענן](../cloud.md) אחרים, במיוחד כשמדובר ב-iCloud Drive. למרות שאנו ממליצים בחום להשתמש בהגנה על נתונים מתקדמת אם אתה משתמש ב-iCloud, אנו מציעים גם לשקול למצוא חלופה ל-iCloud מ[ספק שירות ממוקד יותר בפרטיות](../tools.md), אם כי לא סביר שרוב האנשים יושפעו ממוזרויות ההצפנה הללו.

אתה יכול גם להגן על הנתונים שלך על ידי הגבלת מה שאתה מסנכרן עם iCloud מלכתחילה. בחלק העליון של האפליקציה **הגדרות**, תראה את שמך ותמונת הפרופיל שלך אם אתה מחובר ל-iCloud. בחר את זה, ולאחר מכן **iCloud**, וכבה את המתגים עבור כל השירותים שאתה לא רוצה לסנכרן עם iCloud. ייתכן שתראה יישומי צד שלישי ברשימה תחת **הצג הכל**אם הם מסתנכרנים עם iCloud, אותו תוכל להשבית כאן.

#### iCloud+

מנוי **iCloud+** בתשלום (עם כל תוכנית אחסון של iCloud) מגיע עם פונקציונליות מסוימת להגנה על הפרטיות. While these may provide adequate service for current iCloud customers, we wouldn't recommend purchasing an iCloud+ plan over a [VPN](../vpn.md) and [standalone email aliasing service](../email-aliasing.md) just for these features alone.

[**Private Relay**](https://apple.com/legal/privacy/data/en/icloud-relay) is a proxy service which relays all of your Safari traffic, your DNS queries, and unencrypted traffic on your device through two servers: one owned by Apple and one owned by a third-party provider (including Akamai, Cloudflare, and Fastly). בתיאוריה זה אמור למנוע מכל ספק בודד בשרשרת - כולל אפל - לקבל ראות מלאה באילו אתרים אתה מבקר בזמן שאתה מחובר. Unlike a VPN, Private Relay does not protect traffic that's already encrypted.

**הסתר את האימייל שלי** הוא שירות כינוי האימייל של אפל. אתה יכול ליצור כינוי אימייל בחינם כשאתה *נכנס עם Apple* באתר או באפליקציה, או יוצר כינויים ללא הגבלה לפי דרישה עם תוכנית iCloud+ בתשלום. Hide My Email יש את היתרון בשימוש בדומיין `@icloud.com` עבור הכינויים שלו, אשר עשוי להיות פחות סביר שייחסם בהשוואה לשירותי כינוי דוא"ל אחרים, אך אינו מציע פונקציונליות המוצעת על ידי שירותים עצמאיים כגון כהצפנת PGP אוטומטית או תמיכה במספר תיבות דואר.

#### מדיה & רכישות

At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to an Apple Account. Select that, then select **Media & Purchases** → **View Account**.

- [ ] כבה **המלצות מותאמות אישית**

#### מצא את שלי - Find My

**Find My** הוא שירות המאפשר לך לעקוב אחר מכשירי ה אפל שלך ולשתף את המיקום שלך עם חברים ובני משפחה. הוא גם מאפשר לך למחוק את המכשיר שלך מרחוק במקרה שהוא נגנב, ומונע מגנב לגשת לנתונים שלך. Your Find My [location data is E2EE](https://apple.com/legal/privacy/data/en/find-my) when:

- Your location is shared with a family member or friend, and you both use iOS 17 or greater.
- המכשיר שלך לא מחובר וממוקם על ידי 'מצא את הרשת שלי '.

נתוני המיקום שלך אינם E2EE כאשר המכשיר שלך מחובר ואתה משתמש ב - Find My iPhone מרחוק כדי לאתר את המכשיר שלך. תצטרך לקבל את ההחלטה אם תמורות אלה שוות את היתרונות נגד גניבה של נעילת הפעלה.

At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to an Apple Account. בחר באפשרות זו, ולאחר מכן בחר **איתור**. כאן באפשרותך לבחור אם להפעיל או להשבית את תכונות המיקום שלי.

### Settings

ניתן למצוא הגדרות רבות אחרות הקשורות לפרטיות באפליקציית **הגדרות**.

#### מצב טיסה

הפעלת **מצב טיסה** מונעת מהטלפון ליצור קשר עם אנטנות סלולריות. עדיין תוכלו להתחבר ל - Wi - Fi ול - Bluetooth, כך שבכל פעם שאתם מחוברים ל - Wi - Fi תוכלו להפעיל הגדרה זו.

#### רשת אלחוטית

You can enable [hardware address randomization](https://support.apple.com/en-us/102509#triswitch) to protect you from tracking across Wi-Fi networks, and on the same network over time. On the network you are currently connected to, tap the :material-information: button:

- [x] Set **Private Wi-Fi Address** to **Fixed** or **Rotating**

יש לך גם אפשרות **להגביל מעקב אחר כתובות IP**. זה דומה ל - iCloud Private Relay אבל משפיע רק על חיבורים ל"מעקבים ידועים." מכיוון שהיא משפיעה רק על חיבורים לשרתים שעלולים להיות זדוניים, סביר להניח שהגדרה זו תשאיר אותה מופעלת, אך אם אינך מעוניין בכך * כל * תעבורה שתנותב דרך השרתים של אפל, מומלץ לכבות אותה.

#### Bluetooth

**Bluetooth** אמור להיות מושבת כאשר אינך משתמש בו מכיוון שהוא מגדיל את שטח ההתקפה שלך. השבתת Bluetooth (או Wi - Fi) באמצעות מרכז הבקרה מבטלת אותו באופן זמני בלבד: עליך לכבות אותו בהגדרות כדי להשבית אותו כדי להישאר יעיל.

- [ ] כבה את **Bluetooth**

Note that Bluetooth is automatically turned on after every system update.

#### כללי

שם המכשיר של האייפון שלך יכיל כברירת מחדל את שמך הפרטי, וזה יהיה גלוי לכל מי ברשתות שאתה מתחבר אליהן. אתה צריך לשנות את זה למשהו יותר גנרי, כמו "אייפון" Select **About** → **Name** and enter the device name you prefer.

חשוב להתקין **עדכוני תוכנה** לעיתים קרובות כדי לקבל את תיקוני האבטחה האחרונים. אתה יכול להפעיל את **עדכונים אוטומטיים** כדי לשמור על הטלפון שלך מעודכן מבלי שתצטרך לחפש כל הזמן עדכונים. Select **Software Update** → **Automatic Updates**:

- [x] הפעל את **הורד עדכוני iOS**
- [x] הפעל את **התקן עדכוני iOS**
- [x] הפעל את **תגובות אבטחה & קבצי מערכת**

**AirDrop** is commonly used to easily share files, but it represents a significant privacy risk. The AirDrop protocol constantly broadcasts your personal information to your surroundings, with [very weak](https://usenix.org/system/files/sec21-heinrich.pdf) security protections. Your identity can easily be discovered by attackers even with limited resources, and the Chinese government has [openly acknowledged](https://arstechnica.com/security/2024/01/hackers-can-id-unique-apple-airdrop-users-chinese-authorities-claim-to-do-just-that) using such techniques to identify AirDrop users in public since 2022.

- [x] Select **AirDrop** → **Receiving Off**

**AirPlay** מאפשר לך להזרים בצורה חלקה תוכן מה-iPhone שלך לטלוויזיה; עם זאת, ייתכן שלא תמיד תרצה בכך. Select **AirPlay & Continuity** → **Automatically AirPlay**:

- [x] בחר **לעולם לא** או **שאל**

**רענון אפליקציות ברקע** מאפשר ליישומים שלך לרענן את התוכן שלהם בזמן שאינך משתמש בהם. זה עלול לגרום להם ליצור קשרים לא רצויים. Turning this off can also save battery life, but may affect an app's ability to receive updated information, particularly weather and messaging apps.

בחר **רענון אפליקציות ברקע** וכבה את כל האפליקציות שאינך רוצה להמשיך לרענן ברקע. אם אינך רוצה שאפליקציות כלשהן ירעננו ברקע, תוכל לבחור שוב ב**רענון אפליקציה ברקע** ולכבות **אותה**.

#### סירי & חיפוש

אם אתה לא רוצה שאף אחד יוכל לשלוט בטלפון שלך עם Siri כשהוא נעול, אתה יכול לכבות את זה כאן.

- [ ] כבה את **אפשר את Siri כאשר נעולה**

#### מזהה פנים/זיהוי מגע & קוד סיסמה

הגדרת סיסמה חזקה בטלפון שלך היא הצעד החשוב ביותר שאתה יכול לנקוט לאבטחת המכשיר הפיזי. תצטרך לעשות כאן פשרה בין אבטחה לנוחות: סיסמה ארוכה יותר תהיה מעצבנת להזין בכל פעם, אבל סיסמה קצרה יותר או PIN יהיה קל יותר לנחש. הגדרת Face ID או Touch ID יחד עם סיסמה חזקה יכולה להיות פשרה טובה בין שימושיות ואבטחה.

Select **Turn Passcode On** or **Change Passcode** → **Passcode Options** → **Custom Alphanumeric Code**. Make sure that you create a [secure password](../basics/passwords-overview.md).

אם ברצונך להשתמש ב-Face ID או Touch ID, תוכל להמשיך ולהגדיר זאת כעת. הטלפון שלך ישתמש בסיסמה שהגדרת קודם לכן כחלופה למקרה שהאימות הביומטרי שלך ייכשל. שיטות פתיחה ביומטריות הן בעיקר נוחות, אם כי הן עוצרות מצלמות מעקב או אנשים מעבר לכתף שלך מלצפות בך מזין את קוד הסיסמה שלך.

אם אתה משתמש ביומטרי, אתה צריך לדעת איך לכבות אותם במהירות במקרה חירום. לחיצה ממושכת על לחצן הצד או ההפעלה ו*כל אחד* כפתור עוצמת הקול עד שתראה את המחוון Slide to Power Off תשבית את הביומטרי, ותחייב את קוד הגישה שלך כדי לפתוח. קוד הגישה שלך יידרש גם לאחר הפעלה מחדש של המכשיר.

On some older devices, you may have to press the power button five times to disable biometrics instead, or for devices with Touch ID, you may just have to hold down the power button and nothing else. הקפד לנסות זאת מראש כדי שתדע איזו שיטה עובדת עבור המכשיר שלך.

**Stolen Device Protection** adds additional security intended to protect your personal data if your device is stolen while unlocked. If you use biometrics and the Find My Device feature in your Apple Account settings, we recommend enabling this new protection:

- [x] Select **Turn On Protection**

After enabling Stolen Device Protection, [certain actions](https://support.apple.com/HT212510) will require biometric authentication without a password fallback (in the event that a shoulder surfer has obtained your PIN), such as using password autofill, accessing payment information, and disabling Lost Mode. It also adds a security delay to certain actions performed away from your home or another "familiar location," such as requiring a 1-hour timer to reset your Apple Account password or sign out of your Apple Account. This delay is intended to give you time to enable Lost Mode and secure your account before a thief can reset your device.

**אפשר גישה כאשר הוא נעול** נותן לך אפשרויות למה שאתה יכול לאפשר כשהטלפון שלך נעול. ככל שתבטל יותר מהאפשרויות האלה, כך מישהו ללא הסיסמה שלך יכול לעשות פחות, אבל זה יהיה פחות נוח עבורך. תברר ובחר לאילו מבין אלה אינך רוצה שלמישהו תהיה גישה אם הוא ישים את ידו על הטלפון שלך.

- [ ] כבה את **היום הצג וחיפוש**
- [ ] כבה את **מרכז ההודעות**
- [ ] כבה את **מרכז הבקרה**
- [ ] כבה את **יישומוני מסך נעילה**
- [ ] כבה את **Siri**
- [ ] כבה את **השב עם הודעה**
- [ ] כבה את **בקרת הבית**
- [ ] כבה את **ארנק**
- [ ] כבה את **החזרת שיחות שלא נענו**
- [ ] כבה את **אביזרי USB**

מכשירי אייפון כבר עמידים בפני התקפות בכוח גס בכך שהם גורמים לך להמתין פרקי זמן ארוכים לאחר ניסיונות כושלים מרובים; עם זאת, היסטורית היו מעללים כדי לעקוף את זה. ליתר ביטחון, אתה יכול להגדיר את הטלפון שלך לנגב את עצמו לאחר 10 ניסיונות כושלים של קוד סיסמה.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

כאשר הגדרה זו מופעלת, מישהו יכול למחוק את הטלפון שלך בכוונה על ידי הזנת הסיסמה השגויה פעמים רבות. ודא שיש לך גיבויים מתאימים והפעל את ההגדרה הזו רק אם אתה מרגיש בנוח איתה.

</div>

- [x] הפעל את **מחק נתונים**

#### פרטיות& אבטחה

**שירותי מיקום** מאפשרים לך להשתמש בתכונות כמו מצא את שלי ומפות. אם אינך זקוק לתכונות אלו, תוכל להשבית את שירותי המיקום. לחלופין, תוכל לסקור ולבחור אילו אפליקציות יכולות להשתמש במיקום שלך כאן. בחר **שירותי מיקום**:

- [ ] כבה את **שירותי מיקום**

A purple arrow will appear next to an app in these settings that has used your location recently, while a gray arrow indicates that your location has been accessed within the last 24 hours. If you decide to leave Location Services on, Apple will use it for System Services by default. You can review and pick which services can use your location here. However, if you don't want to submit location analytics to Apple, which they use to improve Apple Maps, you can disable this here as well. Select **System Services**:

- [ ] Turn off **iPhone Analytics**
- [ ] Turn off **Routing & Traffic**
- [ ] Turn off **Improve Maps**

אתה יכול להחליט לאפשר לאפליקציות לבקש **לעקוב ** אחריך כאן. השבתה זו לא מאפשרת לכל האפליקציות לעקוב אחריך עם מזהה הפרסום של הטלפון שלך. בחר **מעקב**:

- [ ] כבה את **אפשר לאפליקציות לבקש מעקב**

This is disabled by default and cannot be changed for users under 18.

עליך לכבות את **חיישן מחקר & נתוני שימוש**אם אינך מעוניין להשתתף במחקרים. בחר **חיישן מחקר & נתוני שימוש**:

- [ ] כבה את **חיישן & איסוף נתוני שימוש**

**בדיקת בטיחות** מאפשרת לך להציג ולבטל במהירות אנשים ואפליקציות מסוימים שעשויים לקבל הרשאה לגשת לנתונים שלך. Here you can perform an **Emergency Reset**, immediately resetting permissions for all people and apps which might have access to device resources. You can also **Manage Sharing & Access** which allows you to go through and customize who and what has access to your device and account resources.

עליך להשבית את הניתוח אם אינך רוצה לשלוח נתוני שימוש לאפל. בחר **אנליטיקס& שיפורים**:

- [ ] כבה את **שתף iPhone Analytics** או **שתף iPhone & צפה ב-Analytics**
- [ ] כבה את **שתף iCloud Analytics**
- [ ] כבה את **שיפור כושר+**
- [ ] כבה את **שפר את הבטיחות**
- [ ] כבה את **שפר את Siri & הכתבה**
- [ ] Turn off **Improve Assistive Voice Features**
- [ ] Turn off **Improve AR Location Accuracy**

השבת את **מודעות מותאמות אישית** אם אינך מעוניין במודעות ממוקדות. Select **Apple Advertising**:

- [ ] כבה את **מודעות מותאמות אישית**

**דוח פרטיות האפליקציה** הוא כלי מובנה המאפשר לך לראות באילו הרשאות האפליקציות שלך משתמשות. בחר **דוח פרטיות האפליקציה**:

- [x] בחר **הפעל דוח פרטיות של אפליקציה**

[מצב נעילה](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) הוא הגדרת אבטחה שתוכל להפעיל כדי להפוך את הטלפון שלך עמיד יותר בפני התקפות. Be aware that certain apps and features [won't work](https://support.apple.com/HT212650) as they do normally.

- [x] בחר **הפעל מצב נעילה**

## עצה נוספת

### שיחות E2EE

שיחות טלפון רגילות שנעשות באמצעות אפליקציית הטלפון דרך הספק שלך אינן E2EE. Both FaceTime Video and FaceTime Audio calls are E2EE. Alternatively, you can use [another app](../real-time-communication.md) like Signal for E2EE calls.

### Imessage מוצפן

The [color of the message bubble](https://support.apple.com/en-us/104972) in the Messages app indicates whether your messages are E2EE or not. A blue bubble indicates that you're using iMessage with E2EE, while a green bubble indicates the other party is using either the outdated SMS and MMS protocols or RCS. RCS on iOS is **not** E2EE. Currently, the only way to have E2EE in Messages is for both parties to be using iMessage on Apple devices.

אם אתה או שותף ההודעות שלך הפעלת גיבוי iCloud ללא הגנת נתונים מתקדמת, מפתח ההצפנה יאוחסן בשרתים של אפל, כלומר הם יכולים לגשת להודעות שלך. Additionally, iMessage's key exchange is not as secure as alternative implementations like Signal's (which allows you to view the recipients key and verify by QR code), so it shouldn't be relied on for particularly sensitive communications.

### Photo Permissions

When an app prompts you for access to your device's photo library, iOS provides you with options to limit what an app can access.

Rather than allow an app to access all the photos on your device, you can allow it to only access whichever photos you choose by tapping the "Select Photos..." option in the permission dialog. You can change photo access permissions at any time by navigating to **Settings** → **Privacy & Security** → **Photos**.

![Photo Permissions](../assets/img/ios/photo-permissions-light.png#only-light) ![Photo Permissions](../assets/img/ios/photo-permissions-dark.png#only-dark)

**Add Photos Only** is a permission that only gives an app the ability to download photos to the photo library. Not all apps which request photo library access provide this option.

![Private Access](../assets/img/ios/private-access-light.png#only-light) ![Private Access](../assets/img/ios/private-access-dark.png#only-dark)

Some apps also support **Private Access**, which functions similarly to the **Limited Access** permission. However, photos shared to apps using Private Access include their location by default. We recommend unchecking this setting if you do not [remove photo metadata](../data-redaction.md) beforehand.

### Contact Permissions

Similarly, rather than allow an app to access all the contacts saved on your device, you can allow it to only access whichever contacts you choose. You can change contact access permissions at any time by navigating to **Settings** → **Privacy & Security** → **Contacts**.

![Contact Permissions](../assets/img/ios/contact-permissions-light.png#only-light) ![Contact Permissions](../assets/img/ios/contact-permissions-dark.png#only-dark)

### Require Biometrics and Hide Apps

iOS offers the ability to lock most apps behind Touch ID/Face ID or your passcode, which can be useful for protecting sensitive content in apps which do not provide the option themselves. You can lock an app by long-pressing on it and selecting **Require Face ID/Touch ID**. Any app locked in this way requires biometric authentication whenever opening it or accessing its contents in other apps. Also, notification previews for locked apps will not be shown.

In addition to locking apps behind biometrics, you can also hide apps so that they don't appear on the Home Screen, App Library, the app list in **Settings**, etc. While hiding apps may be useful in situations where you have to hand your unlocked phone to someone else, the concealment provided by the feature is not absolute, as a hidden app is still visible in some places such as the battery usage list. Moreover, one notable tradeoff of hiding an app is that you will not receive any of its notifications.

You can hide an app by long-pressing on it and selecting **Require Face ID/Touch ID** → **Hide and Require Face ID/Touch ID**. Note that pre-installed Apple apps, as well as the default web browser and email app, cannot be hidden. Hidden apps reside in a **Hidden** folder at the bottom of the App Library, which can be unlocked using biometrics. This folder appears in the App Library whether you hid any apps or not, which provides you a degree of plausible deniability.

### Redacting Elements in Images

If you need to hide information in a photo, you can use Apple's built-in editing tools to do so.

If your device supports it, you can use the [Clean Up](https://support.apple.com/en-us/121429) feature to pixelate faces or remove objects from images.

- Open the **Photos** app and tap the photo you have selected for redaction
- Tap the :material-tune: (at the bottom of the screen)
- Tap the button labeled **Clean Up**
- Draw a circle around whatever you want to redact. Faces will be pixelated and it will attempt to delete anything else.

Our warning [against blurring text](../data-redaction.md) also applies here, so we recommend to instead add a black shape with 100% opacity over it. In addition to redacting text, you can also black out any face or object using the **Photos** app.

- Tap the image you have selected for redaction
- Tap the :material-tune: (at the bottom of the screen) → markup symbol (top right) → plus icon at the bottom right
- Select **Add Shape** and choose the square or circle
- On the toolbar, tap the circle (left-most option) and choose black as the color for filling in the shape. You can also move the shape and increase its size as you see fit.

**Don't** use the highlighter to obfuscate information, as its opacity is not quite 100%.

### הימנע מפריצת Jailbreak

פריצת Jailbreaking של אייפון מערערת את האבטחה שלו והופכת אותך לפגיע. הפעלת תוכנת צד שלישי לא מהימנה עלולה לגרום למכשיר שלך להידבק בתוכנה זדונית.

### iOS בטא

אפל תמיד הופכת גרסאות בטא של iOS לזמינות מוקדם עבור אלה שרוצים לעזור למצוא ולדווח על באגים. אנו לא ממליצים להתקין תוכנת בטא בטלפון שלך. גרסאות בטא עלולות להיות לא יציבות ויכולות להכיל פרצות אבטחה שלא התגלו.

## דגשים באבטחה

### לפני הפתיחה הראשונה

If your threat model includes [:material-target-account: Targeted Attacks](../basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} that involve forensic tools, and you want to minimize the chance of exploits being used to access your phone, you should restart your device frequently. המצב *אחרי* אתחול מחדש אך *לפני* ביטול נעילת המכשיר שלך מכונה "לפני ביטול נעילה ראשון" (BFU), וכאשר המכשיר שלך נמצא במצב זה, זה מקשה [באופן משמעותי](https://belkasoft.com/checkm8_glossary) עבור כלים משפטיים לנצל נקודות תורפה כדי לגשת לנתונים שלך. מצב BFU זה מאפשר לך לקבל התראות על שיחות, הודעות טקסט והתראות, אך רוב הנתונים במכשיר שלך עדיין מוצפנים ואינם נגישים. זה יכול להיות לא מעשי, אז שקול אם הפשרות האלה הגיוניות למצב שלך.
