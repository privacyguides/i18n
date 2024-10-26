---
title: macOS Overview
icon: material/apple-finder
description: macOS is Apple's desktop operating system that works with their hardware to provide strong security.
---

**macOS** היא מערכת הפעלה Unix שפותחה על ידי אפל עבור מחשבי ה-Mac שלהם. כדי לשפר את הפרטיות ב-macOS, אתה יכול להשבית את תכונות הטלמטריה ולהקשיח את הגדרות הפרטיות והאבטחה הקיימות.

מחשבי Mac ו-Hackintosh ישנים יותר מבוססי אינטל אינם תומכים בכל תכונות האבטחה ש-macOS מציעה. To enhance data security, we recommend using a newer Mac with [Apple silicon](https://support.apple.com/HT211814).

## הערות פרטיות

יש כמה חששות בולטים של פרטיות עם macOS שכדאי לשקול. אלה נוגעים למערכת ההפעלה עצמה, ולא לאפליקציות ולשירותים האחרים של אפל.

### נעילת הפעלה

ניתן להגדיר מכשירי סיליקון חדשים של Apple ללא חיבור לאינטרנט. עם זאת, שחזור או איפוס ה-Mac שלך **ידרש**חיבור לאינטרנט לשרתים של אפל כדי לבדוק מול מסד הנתונים של נעילת ההפעלה של מכשירים שאבדו או נגנבו.

### בדיקות ביטול אפליקציה

macOS מבצעת בדיקות מקוונות כאשר אתה פותח אפליקציה כדי לוודא אם אפליקציה מכילה תוכנה זדונית ידועה, והאם אישור החתימה של המפתח נשלל.

Apple's OCSP service uses HTTPS encryption, so only they are able to see which apps you open. They've [posted information](https://support.apple.com/HT202491) about their logging policy for this service. They additionally [promised](http://lapcatsoftware.com/articles/2024/8/3.html) to add a mechanism for people to opt-out of this online check, but this has not been added to macOS.

While you [can](https://eclecticlight.co/2021/02/23/how-to-run-apps-in-private) manually opt out of this check relatively easily, we recommend against doing so unless you would be badly compromised by the revocation checks performed by macOS, because they serve an important role in ensuring compromised apps are blocked from running.

## תצורה מומלצת

החשבון שלך כשתגדיר לראשונה את ה-Mac שלך יהיה חשבון Administrator, בעל הרשאות גבוהות יותר מאשר חשבון משתמש רגיל. ל-macOS יש מספר הגנות שמונעות מתוכנות זדוניות ותוכניות אחרות לנצל לרעה את הרשאות המנהל שלך, כך שבדרך כלל בטוח להשתמש בחשבון זה.

However, exploits in protective utilities like `sudo` have been [discovered in the past](https://bogner.sh/2014/03/another-mac-os-x-sudo-password-bypass). אם ברצונך להימנע מהאפשרות שתוכניות שאתה מפעיל מנצלות לרעה את הרשאות המנהל שלך, תוכל לשקול ליצור חשבון משתמש שני סטנדרטי שבו אתה משתמש לפעולות יומיומיות. יש לזה יתרון נוסף בכך שהוא הופך את זה לברור יותר כאשר אפליקציה צריכה גישת מנהל, מכיוון שהיא תבקש ממך אישורים בכל פעם.

אם אתה משתמש בחשבון שני, אין צורך בהחלט להיכנס לחשבון המנהל המקורי שלך ממסך הכניסה של macOS. כאשר אתה עושה משהו כמשתמש רגיל הדורש הרשאות מנהל מערכת, המערכת אמורה לבקש ממך אימות, שם תוכל להזין את אישורי המנהל שלך כמשתמש הרגיל שלך באופן חד פעמי. אפל מספקת [הנחיות](https://support.apple.com/HT203998) להסתרת חשבון המנהל שלך אם אתה מעדיף לראות רק חשבון בודד במסך ההתחברות שלך.

### iCloud

כאשר אתה משתמש בשירותי אפל כמו iCloud, רוב המידע שלך מאוחסן בשרתים שלהם ומאובטח באמצעות מפתחות *שאלם יש לאפל גישה* כברירת מחדל. This is called [Standard Data Protection](https://support.apple.com/en-us/102651) by Apple.

לכן, אם אתה משתמש ב-iCloud, עליך [להפעיל את **הגנת נתונים מתקדמת**](https://support.apple.com/HT212520). זה מצפין כמעט את כל נתוני ה-iCloud שלך עם מפתחות המאוחסנים במכשירים שלך (הצפנה מקצה לקצה), ולא בשרתים של אפל, כך שנתוני ה-iCloud שלך מאובטחים במקרה של הפרת נתונים, ומוסתרים אחרת מאפל.

If you want to be able to install apps from the App Store but don't want to enable iCloud, you can sign in to your Apple Account from the App Store instead of **System Settings**.

### הגדרות מערכת

ישנן מספר הגדרות מובנות שאתה צריך לאשר או לשנות כדי להקשיח את המערכת שלך. פתח את אפליקציית **הגדרות**:

#### Bluetooth

- [ ] בטל את הסימון של **Bluetooth** (אלא אם כן אתה משתמש בו כעת)

#### רשת

תלוי אם אתה משתמש ב**Wi-Fi** או ב**Ethernet** (מסומן בנקודה ירוקה ובמילה "מחוברים"), לחץ על הסמל המתאים.

לחץ על כפתור "פרטים" לפי שם הרשת שלך:

- [x] Select **Rotating** under **Private Wi-Fi address**

- [x] Check **Limit IP address tracking**

##### חומת-אש

חומת האש שלך חוסמת חיבורי רשת לא רצויים. ככל שהגדרות חומת האש שלך מחמירות יותר, כך ה-Mac שלך מאובטח יותר. עם זאת, שירותים מסוימים ייחסמו. עליך להגדיר את חומת האש שלך כך שתהיה קפדנית ככל האפשר מבלי לחסום שירותים שבהם אתה משתמש.

- [x] בדוק את **חומת האש**

לחץ על הלחצן **אפשרויות**:

- [x] סמן את **חסום את כל החיבורים הנכנסים**

אם תצורה זו קפדנית מדי, אתה יכול לחזור ולבטל את הסימון. עם זאת, macOS בדרך כלל ינחה אותך לאפשר חיבורים נכנסים עבור אפליקציה אם האפליקציה מבקשת זאת.

#### כללי

כברירת מחדל, שם המכשיר שלך יהיה משהו כמו "ה-iMac של [השם שלך]". מכיוון שהשם הזה משודר בפומבי ברשת שלך, תרצה לשנות את שם המכשיר שלך למשהו כללי כמו "Mac".

לחץ על **אודות** והקלד את שם המכשיר הרצוי בשדה **שם**.

##### עדכוני תוכנה

עליך להתקין באופן אוטומטי את כל העדכונים הזמינים כדי לוודא שה-Mac שלך מכיל את תיקוני האבטחה האחרונים.

לחץ על הסמל הקטן :material-information-outline: ליד **עדכונים אוטומטיים**:

- [x] בדוק את **חפש עדכונים**

- [x] בדוק את **הורד עדכונים חדשים כאשר הם זמינים**

- [x] סמן את **התקן עדכוני macOS**

- [x] סמן את **התקן עדכוני יישומים מ-App Store**

- [x] סמן את **התקן תגובות אבטחה וקובצי מערכת**

#### פרטיות& אבטחה

בכל פעם שאפליקציה מבקשת הרשאה, היא תופיע כאן. אתה יכול להחליט אילו יישומים ברצונך לאפשר או לדחות הרשאות ספציפיות.

##### שירותי מיקום

אתה יכול לאפשר בנפרד שירותי מיקום לכל אפליקציה. אם אינך זקוק לאפליקציות כדי להשתמש במיקום שלך, כיבוי שירותי מיקום לחלוטין היא האפשרות הפרטית ביותר.

- [ ] בטל את הסימון של **שירותי מיקום**

##### ניתוח & שיפורים

החלט אם ברצונך לשתף נתוני ניתוח עם אפל ומפתחים.

- [ ] בטל את הסימון של **שתף Mac Analytics**

- [ ] בטל את הסימון של **שפר את Siri & הכתבה**

- [ ] בטל את הסימון של **שתף עם מפתחי אפליקציות**

- [ ] בטל את הסימון של **שתף iCloud Analytics** (גלוי אם אתה מחובר ל-iCloud)

##### פרסום של אפל

החלט אם אתה רוצה מודעות מותאמות אישית על סמך השימוש שלך.

- [ ] בטל את הסימון של **מודעות מותאמות אישית**

##### FileVault

במכשירים מודרניים עם מובלעת מאובטחת (Apple T2 Security Chip, Apple Silicon), הנתונים שלך תמיד מוצפנים, אך מפוענחים אוטומטית על ידי מפתח חומרה אם המכשיר שלך לא מזהה שטופלו בהם. הפעלת FileVault מחייבת בנוסף את הסיסמה שלך כדי לפענח את הנתונים שלך, מה שמשפר מאוד את האבטחה, במיוחד כאשר הוא כיבוי או לפני הכניסה הראשונה לאחר ההפעלה.

במחשבי Mac ישנים יותר מבוססי אינטל, FileVault היא הצורה היחידה של הצפנת דיסקים הזמינה כברירת מחדל, וצריכה להיות מופעלת תמיד.

- [x] לחץ על **הפעל**

##### מצב נעילה

[מצב נעילה](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) משבית תכונות מסוימות כדי לשפר בִּטָחוֹן. Some apps or features won't work the same way they do when it's off, for example, [JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers) and [WASM](https://developer.mozilla.org/docs/WebAssembly) are disabled in Safari with Lockdown Mode enabled. אנו ממליצים להפעיל את מצב הנעילה ולראות אם זה משפיע באופן משמעותי על השימוש שלך, הרבה מהשינויים שהוא עושה קלים לחיות איתם.

- [x] לחץ על **הפעל**

### כתובת MAC אקראית

macOS uses a randomized MAC address when performing Wi-Fi scans while disconnected from a network.

You can set your MAC address to be randomized per network and rotate occasionally to prevent tracking between networks and on the same network over time.

Go to **System Settings** → **Network** → **Wi-Fi** → **Details** and set **Private Wi-Fi address** to either **Fixed** if you want a fixed but unique address for the network you're connected to, or **Rotating** if you want it to change over time.

Consider changing your hostname as well, which is another device identifier that's broadcast on the network you're connected to. You may wish to set your hostname to something generic like "MacBook Air", "Laptop", "John's MacBook Pro", or "iPhone" in **System Settings** → **General** → **Sharing**. כמה [סקריפטים של פרטיות](https://github.com/sunknudsen/privacy-guides/tree/master/how-to-spoof-mac-address-and-hostname-automatically-at-boot-on-macos#guide) מאפשרים לך ליצור בקלות שמות מארח עם שמות אקראיים.

## הגנות אבטחה

macOS משתמשת בהגנה לעומק על ידי הסתמכות על שכבות מרובות של הגנות מבוססות תוכנה וחומרה, עם מאפיינים שונים. זה מבטיח שכשל בשכבה אחת לא פוגע באבטחה הכוללת של המערכת.

### אבטחת תוכנה

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

macOS מאפשר לך להתקין עדכוני בטא. אלה אינם יציבים ועשויים להגיע עם טלמטריה נוספת מכיוון שהם מיועדים למטרות בדיקה. בשל כך, אנו ממליצים להימנע מתוכנות בטא באופן כללי.

</div>

#### נפח מערכת חתומה

רכיבי המערכת של macOS מוגנים בנפח מערכת חתומה לקריאה בלבד, כלומר, לא אתה ולא תוכנות זדוניות יכולים לשנות קבצי מערכת חשובים.

הנפח של המערכת מאומתת בזמן שהיא פועלת וכל נתון שלא חתום בחתימה קריפטוגרפית תקפה מאפל יידחה.

#### הגנת שלמות המערכת

macOS מגדיר מגבלות אבטחה מסוימות שלא ניתן לעקוף. אלה נקראים בקרות גישה חובה, והם מהווים את הבסיס לארגז החול, בקרת הורים והגנה על שלמות המערכת ב-macOS.

הגנת שלמות המערכת הופכת מיקומי קבצים קריטיים לקריאה בלבד כדי להגן מפני שינויים מקוד זדוני. זה נוסף על הגנת Kernel Integrity מבוססת החומרה שמונעת מהליבה להשתנות בזיכרון.

#### אבטחת יישומים

##### ארגז חול לאפליקציה

On macOS, whether an app is sandboxed is determined by the developer when they sign it. The App Sandbox protects against vulnerabilities in the apps you run by limiting what a malicious actor can access in the event that the app is exploited. The App Sandbox *alone* can't protect against [:material-package-variant-closed-remove: Supply Chain Attacks](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian} by malicious developers. For that, sandboxing needs to be enforced by someone other than the developer themselves, as it is on the App Store.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

תוכנה שהורדה מחוץ לחנות האפליקציות הרשמית אינה חייבת להיות בארגז חול. If your threat model prioritizes defending against [:material-bug-outline: Passive Attacks](../basics/common-threats.md#security-and-privacy){ .pg-orange }, then you may want to check if the software you download outside the App Store is sandboxed, which is up to the developer to *opt in*.

</div>

You can check if an app uses the App Sandbox in a few ways:

You can check if apps that are already running are sandboxed using the [Activity Monitor](https://developer.apple.com/documentation/security/protecting-user-data-with-app-sandbox#Verify-that-your-app-uses-App-Sandbox).

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Just because one of an app's processes is sandboxed doesn't mean they all are.

</div>

Alternatively, you can check apps before you run them by running this command in the terminal:

``` zsh
% codesign -dvvv --entitlements - <path to your app>
```

If an app is sandboxed, you should see the following output:

``` zsh
    [Key] com.apple.security.app-sandbox
    [Value]
        [Bool] true
```

If you find that the app you want to run is not sandboxed, then you may employ methods of [compartmentalization](../basics/common-threats.md#security-and-privacy) such as virtual machines or separate devices, use a similar app that is sandboxed, or choose to not use the unsandboxed app altogether.

##### Hardened Runtime

The [Hardened Runtime](https://developer.apple.com/documentation/security/hardened_runtime) is an extra form of protection for apps that prevents certain classes of exploits. It improves the security of apps against exploitation by disabling certain features like JIT.

You can check if an app uses the Hardened Runtime using this command:

``` zsh
codesign --display --verbose /path/to/bundle.app
```

If Hardened Runtime is enabled, you will see `flags=0x10000(runtime)`. The `runtime` output means Hardened Runtime is enabled. There might be other flags, but the runtime flag is what we're looking for here.

You can enable a column in Activity Monitor called "Restricted" which is a flag that prevents programs from injecting code via macOS's [dynamic linker](https://pewpewthespells.com/blog/blocking_code_injection_on_ios_and_os_x.html). Ideally, this should say "Yes".

##### אנטי וירוס

macOS מגיע עם שתי צורות של הגנה מפני תוכנות זדוניות:

1. הגנה מפני הפעלת תוכנות זדוניות מלכתחילה מסופקת על ידי תהליך הבדיקה של App Store עבור יישומי App Store, או *אישור נוטריוני* (חלק מ* Gatekeeper*), תהליך שבו יישומי צד שלישי נסרקים לאיתור תוכנות זדוניות ידועות על ידי אפל לפני שהם מורשים לפעול. Apps are required to be signed by the developers using a key given to them by Apple. This ensures that you are running software from the real developers. Notarization also requires that developers enable the Hardened Runtime for their apps, which limits methods of exploitation.
2. הגנה מפני תוכנות זדוניות אחרות ותיקון מתוכנות זדוניות קיימות במערכת שלך מסופקת על ידי *XProtect*, תוכנת אנטי-וירוס מסורתית יותר המובנית ב-macOS.

אנו ממליצים לא להתקין תוכנת אנטי-וירוס של צד שלישי מכיוון שבדרך כלל אין להם את הגישה ברמת המערכת הנדרשת לתפקוד תקין בכל מקרה, בגלל המגבלות של אפל על אפליקציות של צד שלישי, ומכיוון שהענקת רמות הגישה הגבוהות שהם מבקשים מייצגת לעתים קרובות סיכון אבטחה ופרטיות גדול עוד יותר למחשב שלך.

##### גיבויים

macOS מגיע עם תוכנת גיבוי אוטומטית בשם [Time Machine](https://support.apple.com/HT201250), כך שתוכל ליצור גיבויים מוצפנים לכונן חיצוני או רשת במקרה של פגום/ קבצים שנמחקו.

### אבטחת חומרה

תכונות אבטחה מודרניות רבות ב-macOS - כמו אתחול מאובטח מודרני, הפחתת ניצול ברמת החומרה, בדיקות שלמות מערכת ההפעלה והצפנה מבוססת קבצים - מסתמכות על סיליקון של Apple, ולחומרה החדשה יותר של אפל יש תמיד את [האבטחה הטובה ביותר](https:// support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1). אנו מעודדים רק שימוש בסיליקון של Apple, ולא במחשבי Mac או Hackintosh ישנים יותר מבוססי אינטל.

חלק מתכונות האבטחה המודרניות הללו זמינות במחשבי Mac ישנים יותר מבוססי אינטל עם שבב האבטחה של Apple T2, אך השבב הזה רגיש לניצול *checkm8* שעלול לסכן את האבטחה שלו.

אם אתה משתמש באביזרי בלוטות' כגון מקלדת, אנו ממליצים להשתמש באפל הרשמיים מכיוון שהקושחה שלהם תתעדכן עבורך באופן אוטומטי על ידי macOS. שימוש באביזרים של צד שלישי זה בסדר, אך עליך לזכור להתקין עבורם עדכוני קושחה באופן קבוע.

ה-SoCs של אפל מתמקדים במזעור משטח ההתקפה על ידי העברת פונקציות האבטחה לחומרה ייעודית עם פונקציונליות מוגבלת.

#### אתחול ROM

macOS מונע התמדה של תוכנות זדוניות בכך שהוא מאפשר רק לתוכנת אפל רשמית לפעול בזמן האתחול; זה ידוע בתור אתחול מאובטח. מחשבי Mac מאמתים זאת עם מעט זיכרון לקריאה בלבד ב-SoC הנקרא אתחול ROM, אשר מונח במהלך ייצור השבב.

ROM האתחול הוא שורש האמון של החומרה. זה מבטיח שתוכנה זדונית לא יכולה לחבל בתהליך האתחול. כאשר ה-Mac שלך מאתחל, ROM האתחול הוא הדבר הראשון שפועל, ויוצר את החוליה הראשונה בשרשרת האמון.

ניתן להגדיר מחשבי Mac לאתחל בשלושה מצבי אבטחה: *אבטחה מלאה*, *אבטחה מופחתת* ו-*אבטחה מתירה*, כאשר הגדרת ברירת המחדל היא אבטחה מלאה. באופן אידיאלי אתה צריך להשתמש במצב אבטחה מלאה ולהימנע מדברים כמו **הרחבות ליבה** המאלצות אותך להוריד את מצב האבטחה שלך. הקפד [לבדוק](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac) שאתה אתה משתמש במצב אבטחה מלאה.

#### Secure Enclave

ה-Secure Enclave הוא שבב אבטחה מובנה במכשירים עם סיליקון של אפל אשר אחראי על אחסון ויצירת מפתחות הצפנה עבור נתונים במנוחה וכן נתוני Face ID ו-Touch ID. הוא מכיל ROM אתחול נפרד משלו.

אתה יכול לחשוב על ה-Secure Enclave כמרכז האבטחה של המכשיר שלך: יש לו מנוע הצפנה AES ומנגנון לאחסון מאובטח של מפתחות ההצפנה שלך, והוא מופרד משאר המערכת, כך שגם אם המעבד הראשי נפגע, הוא צריך עדיין להיות בטוח.

#### טביעת אצבע Touch ID

תכונת Touch ID של אפל מאפשרת לך לפתוח את המכשירים שלך בצורה מאובטחת באמצעות ביומטריה.

הנתונים הביומטריים שלך לעולם לא יוצאים מהמכשיר שלך; זה מאוחסן רק בSecure Enclave.

#### ניתוק מיקרופון של החומרה

כל המחשבים הניידים עם סיליקון אפל או שבב T2 כוללים ניתוק חומרה עבור המיקרופון המובנה בכל פעם שהמכסה סגור. זה אומר שאין שום דרך לתוקף להאזין למיקרופון של ה-Mac שלך גם אם מערכת ההפעלה נפגעת.

שימו לב שלמצלמה אין ניתוק חומרה, מכיוון שהנוף שלה מעורפל כאשר המכסה סגור בכל מקרה.

#### אבטחת מעבד היקפי

למחשבים יש מעבדים מובנים מלבד המעבד הראשי שמטפלים בדברים כמו רשת, גרפיקה, ניהול צריכת חשמל וכו'. למעבדים אלו יכולה להיות אבטחה לא מספקת ולהיפגע, לכן אפל מנסה למזער את הצורך במעבדים אלו בחומרה שלהם.

כאשר יש צורך להשתמש באחד מהמעבדים הללו, אפל עובדת עם הספק כדי לוודא שהמעבד

- מריץ קושחה מאומתת מהמעבד הראשי בעת האתחול
- יש לו שרשרת אתחול מאובטח משלו
- עומד בסטנדרטים קריפטוגרפיים מינימליים
- מבטיח כי קושחה פגומה ידועה מבוטלת כהלכה
- ממשקי ניפוי הבאגים שלו מושבתים
- חתום במפתחות ההצפנה של אפל

#### הגנות גישה ישירה לזיכרון

סיליקון אפל מפריד בין כל רכיב שדורש גישה ישירה לזיכרון. לדוגמה, יציאת Thunderbolt לא יכולה לגשת לזיכרון המיועד לליבה.

## מקורות

- [אבטחת פלטפורמת אפל](https://support.apple.com/guide/security/welcome/web)
