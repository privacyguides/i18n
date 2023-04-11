---
title: "אנדרואיד"
icon: 'simple/android'
description: אתה יכול להחליף את מערכת ההפעלה בטלפון האנדרואיד שלך בחלופות מאובטחות ומכבדות פרטיות אלה.
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: מערכות הפעלה פרטיות לאנדרואיד
    url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: אנדרואיד
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://en.wikipedia.org/wiki/Android_(operating_system)
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: Divest
    image: /assets/img/android/divestos.svg
    url: https://divestos.org/
    sameAs: https://en.wikipedia.org/wiki/DivestOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": Product
    name: Pixel
    brand:
      "@type": Brand
      name: גוגל
    image: /assets/img/android/google-pixel.png
    sameAs: https://en.wikipedia.org/wiki/Google_Pixel
    review:
      "@type": Review
      author:
        "@type": Organization
        name: Privacy Guides
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Shelter
    applicationCategory: Utilities
    operatingSystem: אנדרואיד
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Auditor
    applicationCategory: Utilities
    operatingSystem: אנדרואיד
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Secure Camera
    applicationCategory: Utilities
    operatingSystem: אנדרואיד
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Secure PDF Viewer
    applicationCategory: Utilities
    operatingSystem: אנדרואיד
---

![לוגו אנדרואיד](assets/img/android/android.svg){ align=right }

**פרויקט הקוד הפתוח של אנדרואיד** היא מערכת הפעלה ניידת בקוד פתוח בהובלת גוגל, המניעה את רוב המכשירים הניידים בעולם. רוב הטלפונים הנמכרים עם אנדרואיד שונו כך שיכללו אינטגרציות פולשניות ואפליקציות כגון שירותי Google Play, כך שתוכל לשפר משמעותית את הפרטיות שלך במכשיר הנייד שלך על ידי החלפת התקנת ברירת המחדל של הטלפון שלך בגרסת אנדרואיד ללא תכונות פולשניות אלו.

[:octicons-home-16:](https://source.android.com/){ .card-link title=דף הבית }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=תיעוד}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/){ .card-link title="קוד מקור" }

אלו הן מערכות ההפעלה, המכשירים והאפליקציות של אנדרואיד שאנו ממליצים על מנת למקסם את האבטחה והפרטיות של המכשיר הנייד שלך. למידע נוסף על אנדרואיד:

[סקירה כללית של אנדרואיד :material-arrow-right-drop-circle:](os/android-overview.md ""){.md-button}

[מדוע אנו ממליצים על GrapheneOS על פני CalyxOS :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/ ""){.md-button}

## נגזרות AOSP

אנו ממליצים להתקין במכשיר שלך אחת ממערכות ההפעלה המותאמות אישית של אנדרואיד, המפורטות לפי סדר העדפה, בהתאם לתאימות המכשיר שלך למערכות הפעלה אלו.

!!! note "הערה"

    למכשירי סוף החיים (כגון מכשירי "תמיכה מורחבת" של GrapheneOS או CalyxOS) אין תיקוני אבטחה מלאים (עדכוני קושחה) עקב הפסקת התמיכה של OEM. מכישירים אלה אינם יכולים להיחשב מאובטחים לחלוטין ללא קשר לתוכנה המותקנת.

### GrapheneOS

!!! recommendation

    ![לוגו GrapheneOS](assets/img/android/grapheneos.svg#only-light){ align=right }
    ![לוגו GrapheneOS](assets/img/android/grapheneos-dark.svg#only-dark){ align=right }
    
    **GrapheneOS** היא הבחירה הטובה ביותר בכל הנוגע לפרטיות ואבטחה.
    
    GrapheneOS מספקת [הקשחת אבטחה](https://en.wikipedia.org/wiki/Hardening_(computing)) ושיפורי פרטיות נוספים. יש לו [מקצה זיכרון מוקשה](https://github.com/GrapheneOS/hardened_malloc), הרשאות רשת וחיישנים ועוד [תכונות אבטחה](https://grapheneos.org/features) שונות. GrapheneOS מגיעה גם עם עדכוני קושחה מלאים ו-builds חתומים, כך שאתחול מאומת נתמך באופן מלא.
    
    [:octicons-home-16: דף הבית](https://grapheneos.org/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="מדיניות פרטיות" }
    [:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=תיעוד}
    [:octicons-code-16:](https://grapheneos.org/source){ .card-link title="קוד מקור" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=תרומה }

GrapheneOS תומך ב-[Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), המריץ את [Google Play Services](https://en.wikipedia.org/wiki/Google_Play_Services) בארגז חול מלא כמו כל אפליקציה רגילה אחרת. משמעות הדבר היא שאתה יכול לנצל את רוב שירותי Google Play, כגון [הודעות דחיפה](https://firebase.google.com/docs/cloud-messaging/), תוך מתן שליטה מלאה על ההרשאות והגישה שלהם, ותוך כדי הכללתן ב[פרופיל עבודה](os/android-overview.md#work-profile) או [פרופיל משתמש](os/android-overview.md#user-profiles) ספציפי לבחירתך.

טלפונים של Google Pixel הם המכשירים היחידים שעומדים כרגע ב[דרישות אבטחת החומרה](https://grapheneos.org/faq#device-support) של GrapheneOS.

### DivestOS

!!! recommendation

    ![לוגו של DivestOS](assets/img/android/divestos.svg){ align=right }
    
    **DivestOS** הוא נגזרת חלקית של [LineageOS](https://lineageos.org/).
    DivestOS יורשת [מכשירים נתמכים](https://divestos.org/index.php?page=devices&base=LineageOS) רבים מ-LineageOS. יש לו builds חתומים, מה שמאפשר לקבל [אתחול מאומת](https://source.android.com/security/verifiedboot) בחלק מהמכשירים שאינם Pixel.
    
    [:octicons-home-16: דף הבית](https://divestos.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="שירות בצל" }
    [:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="מדיניות פרטיות" }
    [:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=תיעוד}
    [:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="קוד מקור" }
    [:octicons-heart-16:](https://divested.dev/index.php?page=donate){ .card-link title=לתרומה }

ל - DivestOS יש פגיעות ליבה ([CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [שמתוקן](https://gitlab.com/divested-mobile/cve_checker) אוטומטית, פחות בועות קנייניות, וקובץ [מארחים](https://divested.dev/index.php?page=dnsbl) מותאם. ה-WebView המוקשה שלו, [Mulch](https://gitlab.com/divested-mobile/mulch), מאפשר [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) עבור כל הארכיטקטורות ו[חלוקת מצבי רשת](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning), ומקבל עדכונים מחוץ לפס. DivestOS כוללת גם תיקוני ליבה מ-GrapheneOS ומאפשרת את כל תכונות האבטחה הזמינות של הליבה באמצעות [הקשחת defconfig](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). כל הליבות החדשות יותר מגרסה 3.4 כוללים עמוד מלא [חיטוי](https://lwn.net/Articles/334747/) ולכל ~22 הליבות המחוברים יש Clang [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) מופעל.

DivestOS מיישמת כמה תיקוני הקשחת מערכת שפותחו במקור עבור GrapheneOS. DivestOS 16.0 ומעלה מיישמת את החלפת הרשאות [`אינטרנט`](https://developer.android.com/training/basics/network-ops/connecting) וחיישנים של GrapheneOS, [מקצית זיכרון מוקשחת](https://github.com/GrapheneOS/hardened_malloc), [השרצת מנהלים](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/#additional-hardening), [קונסטיפיקציה](https://en.wikipedia.org/wiki/Const_(computer_programming)) של [JNI](https://en.wikipedia.org/wiki/Java_Native_Interface) ותיקוני התקשות [ביונית](https://en.wikipedia.org/wiki/Bionic_(software)) חלקית. תכונות 17.1 ומעלה של GrapheneOS לכל רשת [אפשרות אקראיות מלאה של ](https://en.wikipedia.org/wiki/MAC_address#Randomization)MAC, בקרת [`ptrace_scope`](https://www.kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) ואתחול אוטומטי/Wi-Fi/Bluetooth [אפשרויות פסק זמן](https://grapheneos.org/features).

DivestOS משתמשת ב-F-Droid כחנות האפליקציות המוגדרת כברירת מחדל. בדרך כלל, אנו ממליצים להימנע מ-F-Droid עקב [בעיות האבטחה](#f-droid) הרבות שלו. עם זאת, לעשות זאת ב-DivestOS לא כדאי; המפתחים מעדכנים את האפליקציות שלהם באמצעות מאגרי F-Droid משלהם ([DivestOS Official](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) ו- [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2)). אנו ממליצים להשבית את אפליקציית F-Droid הרשמית ולהשתמש ב-[Neo Store](https://github.com/NeoApplications/Neo-Store/) עם מאגרי DivestOS מופעלים כדי לשמור על רכיבים אלה מעודכנים. לגבי אפליקציות אחרות, השיטות המומלצות שלנו להשגתן עדיין חלות.

!!! warning "אזהרה"

    עדכון קושחה של DivestOS [סטטוס](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) ובקרת איכות משתנים בין המכשירים שבהם הוא תומך. אנו עדיין ממליצים על GrapheneOS בהתאם לתאימות המכשיר שלך. עבור מכשירים אחרים, DivestOS היא אלטרנטיבה טובה.
    
    לא לכל המכשירים הנתמכים יש אתחול מאומת, וחלקם מבצעים אותו טוב יותר מאחרים.

## מכשירי אנדרואיד

בעת רכישת מכשיר, אנו ממליצים לרכוש אחד חדש ככל האפשר. התוכנה והקושחה של מכשירים ניידים נתמכות רק לזמן מוגבל, כך שקנייה חדשה מאריכה את תוחלת החיים עד כמה שניתן.

הימנע מרכישת טלפונים ממפעילי רשתות סלולריות. לאלה יש לרוב **מאתחול נעול** ואינם תומכים ב[פתיחת נעילה של OEM](https://source.android.com/devices/bootloader/locking_unlocking). גרסאות טלפון אלה ימנעו ממך להתקין כל סוג של הפצת אנדרואיד חלופית.

היה מאוד **זהיר** בקניית טלפונים יד שנייה משוק אונליין. בדוק תמיד את המוניטין של המוכר. אם המכשיר נגנב, קיימת אפשרות ל[רשימה שחורה של IMEI](https://www.gsma.com/security/resources/imei-blacklisting/). קיים גם סיכון שכרוך בהיותך קשור לפעילות של הבעלים הקודם.

עוד כמה טיפים לגבי מכשירי אנדרואיד ותאימות מערכות הפעלה:

- אל תקנו מכשירים שהגיעו או קרובים לסוף החיים שלהם, עדכוני קושחה נוספים חייבים להיות מסופקים על ידי היצרן.
- אל תקנו טלפונים טעונים מראש של LineageOS או /e/ OS או כל טלפון אנדרואיד ללא תמיכה מתאימה של [אתחול מאומת](https://source.android.com/security/verifiedboot) ועדכוני קושחה. גם למכשירים האלה אין דרך לבדוק אם התעסקו בהם.
- בקיצור, אם לא מופיעה כאן הפצת מכשיר או אנדרואיד, כנראה שיש סיבה טובה. עיין ב[פורום](https://discuss.privacyguides.net/) שלנו כדי למצוא פרטים!

### גוגל פיקסל

טלפונים של גוגל פיקסל הם המכשירים **היחידים** שאנו ממליצים לרכישה. לטלפונים של Pixel יש אבטחת חומרה חזקה יותר מכל מכשירי אנדרואיד אחרים הקיימים כיום בשוק, בשל תמיכת AVB נאותה עבור מערכות הפעלה של צד שלישי ושבבי האבטחה המותאמים אישית [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) של גוגל הפועלים כ-Secure Element.

!!! recommendation

    ![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }
    
    מכשירי **גוגל פיקסל** ידועים כבעלי אבטחה טובה ותומכים כראוי ב[אתחול מאומת](https://source.android.com/security/verifiedboot), גם בעת התקנת מערכות הפעלה מותאמות אישית.
    
    החל מ-**Pixel 6** ו-**6 Pro**, מכשירי Pixel מקבלים לפחות 5 שנים של עדכוני אבטחה מובטחים, מה שמבטיח תוחלת חיים ארוכה בהרבה בהשוואה ל-2-4 שנים שמציעות יצרניות OEM מתחרות בדרך כלל.
    
    [:material-shopping: חנות](https://store.google.com/category/phones){ .md-button .md-button--primary }

רכיבים מאובטחים כמו Titan M2 מוגבלים יותר מסביבת הביצוע המהימנה של המעבד המשמשת את רוב הטלפונים האחרים מכיוון שהם משמשים רק לאחסון סודות, הוכחת חומרה והגבלת קצב, לא להפעלת תוכניות "מהימנות". טלפונים ללא Secure Element חייבים להשתמש ב-TEE עבור *כל* הפונקציות הללו, וכתוצאה מכך משטח התקפה גדול יותר.

טלפונים של גוגל פיקסל משתמשים ב-TEE OS בשם Trusty שהיא [קוד פתוח](https://source.android.com/security/trusty#whyTrusty), בניגוד לטלפונים רבים אחרים.

ההתקנה של GrapheneOS בטלפון Pixel קלה עם [מתקין האינטרנט שלהם](https://grapheneos.org/install/web). אם אתה לא מרגיש בנוח לעשות את זה בעצמך ומוכן להוציא קצת כסף נוסף, בדוק את ה-[NitroPhone](https://shop.nitrokey.com/shop) מכיוון שהם נטענים מראש עם GrapheneOS של חברת [Nitrokey](https://www.nitrokey.com/about) המכובדת.

עוד כמה טיפים לרכישת Google Pixel:

- אם אתה מחפש מציאה על מכשיר פיקסל, אנו מציעים לקנות דגם "**a**", מיד לאחר יציאת ספינת הדגל הבאה. הנחות זמינות בדרך כלל מכיוון שגוגל תנסה לסלק את המלאי שלה.
- שקול אפשרויות מכות מחיר ומבצעים המוצעים בחנויות פיזיות.
- עיין באתרי עסקאות אןנליין של קהילתיות במדינה שלך. אלה יכולים להתריע על מכירות טובות.
- Google מספקת רשימה המציגה את [מחזור התמיכה](https://support.google.com/nexus/answer/4457705) עבור כל אחד מהמכשירים שלהם. ניתן לחשב את המחיר ליום עבור מכשיר כך: $\text{עלות} \מעל \text {תאריך EOL}-\text{תאריך נוכחי}$, כלומר ככל שהשימוש ארוך יותר במכשיר כך העלות ליום נמוכה יותר.

## אפליקציות כלליות

אנו ממליצים על מגוון רחב של אפליקציות אנדרואיד ברחבי אתר זה. האפליקציות המפורטות כאן הן בלעדיות לאנדרואיד ומשפרות או מחליפות באופן ספציפי את פונקציונליות המערכת המרכזית.

### Shelter

!!! recommendation

    ![Shelter לוגו](assets/img/android/shelter.svg){ align=right }
    
    **Shelter** היא אפליקציה שעוזרת לך למנף את הפונקציונליות של פרופיל העבודה של אנדרואיד כדי לבודד או לשכפל אפליקציות במכשיר שלך.
    
    Shelter תומך בחסימת פרופילים חוצי חיפוש אנשי קשר ושיתוף קבצים בין פרופילים באמצעות מנהל הקבצים המוגדר כברירת מחדל ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).
    
    [:octicons-repo-16: מאגר](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
    [:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="קוד מקור" }
    [:octicons-heart-16:](https://www.patreon.com/PeterCxy){ .card-link title=לתרומה }
    
    ??? downloads "הורדות"
    
        - [simple-googleplay: Google Play:]( https://play.google.com/store/apps/details?id=net.typeblog.shelter)

!!! warning "אזהרה"

    Shelter מומלץ מעל [Insular](https://secure-system.gitlab.io/Insular/) ו-[Island](https://github.com/oasisfeng/island) מכיוון שהוא תומך ב[חסימת חיפוש אנשי קשר](https://secure-system.gitlab.io/Insular/faq.html).
    
    כשאתה משתמש ב-Shelter, אתה נותן אמון מלא במפתח שלו, שכן Shelter פועל כ[מנהל מכשיר](https://developer.android.com/guide/topics/admin/device-admin) כדי ליצור את פרופיל העבודה, וכן יש לו גישה נרחבת לנתונים המאוחסנים בפרופיל העבודה.

### Auditor

!!! recommendation

    ![Auditor לוגו](assets/img/android/auditor.svg#only-light){ align=right }
    ![Auditor לוגו](assets/img/android/auditor-dark.svg#only-dark){ align=right }
    
    **Auditor** היא אפליקציה הממנפת תכונות אבטחת חומרה כדי לספק ניטור שלמות המכשיר עבור [מכשירים נתמכים](https://attestation.app/about#device-support). נכון לעכשיו, זה עובד רק עם GrapheneOS ומערכת ההפעלה הסטוק של המכשיר.
    
    [:octicons-home-16: דף הבית](https://attestation.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="מדיניות פרטיות" }
    [:octicons-info-16:](https://attestation.app/about){ .card-link title=תיעוד}
    [:octicons-code-16:](https://attestation.app/source){ .card-link title="קוד מקור" }
    [:octicons-heart-16:](https://attestation.app/donate){ .card-link title=לתרומה }
    
    ??? downloads "הורדות"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

Auditor מבצע אישור וזיהוי חדירה על ידי:

- באמצעות מודל [Trust On First Use (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) בין *מבקר* ל*מבוקר*, הזוג יוצר מפתח פרטי ב[מאגר המפתחות המגובה בחומרה](https://source.android.com/security/keystore/) של ה*מבקר*.
- *auditor* יכול להיות מופע אחר של אפליקציית Auditor או [שירות אישור מרחוק](https://attestation.app).
- המבקר רושם את המצב הנוכחי ואת התצורה של המבוקר. ה*auditor* מתעד את המצב והתצורה הנוכחיים של ה*auditee*.
- אם התעסקות במערכת ההפעלה של ה*auditee* תתרחש לאחר השלמת ההתאמה, המבקר יהיה מודע לשינוי במצב המכשיר ובתצורות.
- תקבל התראה על השינוי.

לא נמסר מידע מזהה אישי לשירות האישורים. אנו ממליצים להירשם עם חשבון אנונימי ולאפשר אישור מרחוק לניטור רציף.

אם [מודל האיומים](basics/threat-modeling.md) שלך דורש פרטיות, תוכל לשקול להשתמש ב-[Orbot](tor.md#orbot)או ב-VPN כדי להסתיר את כתובת ה-IP שלך משירות האישורים. כדי לוודא שהחומרה ומערכת ההפעלה שלך מקוריות, [בצע אישור מקומי](https://grapheneos.org/install/web#verifying-installation) מיד לאחר התקנת המכשיר ולפני כל חיבור לאינטרנט.

### Secure Camera

!!! recommendation

    ![Secure camera לוגו](assets/img/android/secure_camera.svg#only-light){ align=right }
    ![Secure camera לוגו](assets/img/android/secure_camera-dark.svg#only-dark){ align=right }
    
    **Secure Camera** היא אפליקציית מצלמה המתמקדת בפרטיות ואבטחה שיכולה לצלם תמונות, סרטונים וקודי QR. הרחבות של ספקי CameraX (פורטרט, HDR, ראיית לילה, ריטוש פנים ואוטומטי) נתמכות גם במכשירים זמינים.
    
    [:octicons-repo-16: מאגר](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
    [:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=תיעוד}
    [:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="קוד מקור" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=לתרומה }
    
    ??? downloads "הורדות"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

תכונות הפרטיות העיקריות כוללות:

- הסרה אוטומטית של מטא נתונים של [Exif](https://en.wikipedia.org/wiki/Exif) (מופעל כברירת מחדל)
- שימוש בממשק ה-API החדש של ה[מדיה](https://developer.android.com/training/data-storage/shared/media), לכן אין צורך ב[הרשאות אחסון](https://developer.android.com/training/data-storage)
- אין צורך בהרשאת מיקרופון אלא אם ברצונך להקליט קול

!!! note "הערה"

    מטא נתונים אינם נמחקים כעת מקבצי וידאו אבל זה מתוכנן.
    
    המטא נתונים של כיוון התמונה לא נמחקים. אם תפעיל מיקום ב(Secure Camera) זה גם **לא** יימחק. אם ברצונך למחוק זאת מאוחר יותר, יהיה עליך להשתמש באפליקציה חיצונית כגון [ExifEraser](data-redaction.md#exiferaser).

### Secure PDF Viewer

!!! recommendation

    ![Secure PDF Viewer לוגו](assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
    ![Secure PDF Viewer לוגו](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }
    
    **Secure PDF Viewer** הוא מציג PDF המבוסס על [pdf.js](https://en.wikipedia.org/wiki/PDF.js) שאינו דורש הרשאות כלשהן. ה-PDF מוזן לתוך [ארגז חול](https://en.wikipedia.org/wiki/Sandbox_(software_development))[webview](https://developer.android.com/guide/webapps/webview). המשמעות היא שזה לא דורש הרשאה ישירה כדי לגשת לתוכן או לקבצים.
    
    [תוכן-אבטחה-מדיניות](https://en.wikipedia.org/wiki/Content_Security_Policy) משמש כדי לאכוף שמאפייני JavaScript והסגנון ב-WebView הם תוכן סטטי לחלוטין.
    
    [:octicons-repo-16: מאגר](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
    [:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="קוד מקור" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=לתרומה }
    
    ??? downloads "הורדות"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

## קבלת בקשות

### GrapheneOS App Store

חנות האפליקציות של GrapheneOS זמינה ב-[GitHub](https://github.com/GrapheneOS/Apps/releases). הוא תומך באנדרואיד 12 ומעלה ומסוגל לעדכן את עצמו. לחנות האפליקציות יש יישומים עצמאיים שנבנו על ידי פרויקט GrapheneOS כגון [Auditor](https://attestation.app/), [Camera](https://github.com/GrapheneOS/Camera), ו- [PDF Viewer](https://github.com/GrapheneOS/PdfViewer). אם אתם מחפשים אפליקציות אלו, אנו ממליצים בחום להשיג אותן מחנות האפליקציות של GrapheneOS במקום מחנות Play, שכן האפליקציות בחנות שלהן חתומות על ידי חתימת הפרויקט של ה-GrapheneOS שלגוגל אין גישה אליה.

### Aurora Store

חנות Google Play דורשת חשבון Google כדי להתחבר וזה לא נהדר לפרטיות. אתה יכול לעקוף את זה על ידי שימוש בלקוח חלופי, כגון Aurora Store.

!!! recommendation

    ![Aurora Store לוגו](assets/img/android/aurora-store.webp){ align=right }
    
    **Aurora Store** היא לקוח של חנות Google Play שאינה דורשת חשבון Google, שירותי Google Play או microG כדי להוריד אפליקציות.
    
    [:octicons-home-16: דף הבית](https://auroraoss.com/){ .md-button .md-button--primary }
    [:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="קוד מקור" }
    
    ??? downloads "הורדות"
    
        - [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

Aurora Store לא מאפשרת להוריד אפליקציות בתשלום עם תכונת החשבון האנונימי שלהן. אתה יכול לחלופין להתחבר עם חשבון גוגל שלך ל-Aurora Store כדי להוריד אפליקציות שרכשת, מה שאכן נותן גישה לרשימת האפליקציות שהתקנת לגוגל, אולם אתה עדיין נהנה מכך שאינך דורש את לקוח Google Play המלא ואת Google Play Services או microG במכשיר שלך.

### התראות RSS באופן ידני

עבור אפליקציות שמשוחררות בפלטפורמות כמו GitHub ו-GitLab, ייתכן שתוכל להוסיף עדכון RSS ל[צובר החדשות](/news-aggregators) שלך שיעזור לך לעקוב אחר מהדורות חדשות.

![RSS APK](./assets/img/android/rss-apk-light.png#only-light) ![RSS APK](./assets/img/android/rss-apk-dark.png#only-dark) ![שינויים ב-APK](./assets/img/android/rss-changes-light.png#only-light) ![שינויים ב-APK](./assets/img/android/rss-changes-dark.png#only-dark)

#### Github

ב-GitHub, באמצעות [Secure Camera](#secure-camera) כדוגמה, תנווט ל[דף ההפצות](https://github.com/GrapheneOS/Camera/releases) שלו ותוסיף את `.atom` לכתובת האתר:

`https://github.com/GrapheneOS/Camera/releases.atom`

#### GitLab

ב-GitLab, באמצעות [Aurora Store](#aurora-store) כדוגמה, תנווט אל [מאגר הפרויקטים](https://gitlab.com/AuroraOSS/AuroraStore) שלו ותוסיף `/-/tags?format=atom` לכתובת האתר:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

#### אימות טביעות אצבע של APK

אם אתה מוריד קבצי APK להתקנה ידנית, אתה יכול לאמת את החתימה שלהם עם הכלי [`apksigner`](https://developer.android.com/studio/command-line/apksigner), שהוא חלק מ[כלי הבנייה](https://developer.android.com/studio/releases/build-tools) של אנדרואיד.

1. התקן [Java JDK](https://www.oracle.com/java/technologies/downloads/).

2. הורד את [כלי שורת הפקודה של אנדרואיד סטודיו](https://developer.android.com/studio#command-tools).

3. חלץ את הארכיון שהורד:

    ```bash
    unzip commandlinetools-*.zip
    cd cmdline-tools
    ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
    ```

4. הפעל את פקודת אימות החתימה:

    ```bash
    ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
    ```

5. לאחר מכן ניתן להשוות את ה-hashes המתקבלים עם מקור אחר. מפתחים מסוימים כגון Signal [מראים את טביעות האצבע](https://signal.org/android/apk/) באתר האינטרנט שלהם.

    ```bash
    Signer #1 certificate DN: CN=GrapheneOS
    Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
    Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
    Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
    ```

### F-Droid

![לוגו F-Droid](assets/img/android/f-droid.svg){ align=right width=120px }

==אנחנו **לא** ממליצים כרגע על F-Droid כדרך להשיג אפליקציות.== F-Droid מומלצת לעתים קרובות כחלופה ל-Google Play, במיוחד בפרטיות קהילה. האפשרות להוסיף מאגרי צד שלישי ולא להיות מוגבלים לגן המוקף חומה של גוגל הובילה לפופולריות שלו. ל-F-Droid יש בנוסף [בנייה הניתנת לשחזור](https://f-droid.org/en/docs/Reproducible_Builds/) עבור יישומים מסוימים והוא מוקדש לתוכנות חינמיות וקוד פתוח. עם זאת, ישנן [בעיות בולטות](https://privsec.dev/posts/android/f-droid-security-issues/) עם הלקוח הרשמי של F-Droid, בקרת האיכות שלו והאופן שבו הם בונים, חותמים ומעבירים חבילות.

בשל תהליך בניית האפליקציות שלהם, אפליקציות במאגר ה-F-Droid הרשמי מפגרות לעתים קרובות בפיגור לגבי עדכונים. מנהלי F-Droid גם עושים שימוש חוזר במזהי חבילה בזמן חתימת אפליקציות עם המפתחות שלהם, וזה לא אידיאלי מכיוון שהוא נותן אמון אולטימטיבי לצוות F-Droid.

מאגרים פופולריים אחרים של צד שלישי כגון [IzzyOnDroid](https://apt.izzysoft.de/fdroid/) מקלים על חלק מהחששות הללו. מאגר IzzyOnDroid מושך רכיבים ישירות מ-GitHub והוא הדבר הטוב הבא למאגרים של המפתחים עצמם. עם זאת, זה לא משהו שאנחנו יכולים להמליץ עליו, מכיוון שבדרך כלל אפליקציות [מוסרות](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446) מהמאגר הזה כשהן מגיעות למאגר F-Droid הראשי. למרות שזה הגיוני (מכיוון שהמטרה של המאגר המסוים הזה היא לארח אפליקציות לפני שהן מתקבלות למאגר ה-F-Droid הראשי), זה יכול להשאיר אותך עם אפליקציות מותקנות שכבר לא מקבלים עדכונים.

עם זאת, מאגרי [F-Droid](https://f-droid.org/en/packages/) ו-[IzzyOnDroid](https://apt.izzysoft.de/fdroid/) הם ביתם של אינספור אפליקציות, כך שהם יכולים להיות כלי שימושי לחיפוש ולגלות אפליקציות קוד פתוח שתוכלו לאחר מכן הורד דרך Play Store, Aurora Store, או על ידי קבלת ה-APK ישירות מהמפתח. חשוב לזכור שחלק מהאפליקציות במאגרים אלו לא עודכנו במשך שנים ועשויות להסתמך על ספריות שאינן נתמכות, בין היתר, מהוות סיכון אבטחה פוטנציאלי. אתה צריך להשתמש במיטב שיקול הדעת שלך כשאתה מחפש אפליקציות חדשות בשיטה זו.

!!! note "הערה"

    במקרים נדירים מסוימים, מפתח אפליקציה יפיץ אותה רק באמצעות F-Droid ([Gadgetbridge](https://gadgetbridge.org/) היא דוגמה אחת לכך). אם אתה באמת צריך אפליקציה כזו, אנו ממליצים להשתמש ב-[Neo Store](https://github.com/NeoApplications/Neo-Store/) במקום באפליקציית F-Droid הרשמית כדי להשיג אותה.

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

!!! example "חלק זה הוא חדש"

    אנו עובדים על קביעת קריטריונים מוגדרים לכל קטע באתר שלנו, והדבר עשוי להשתנות. אם יש לך שאלות כלשהן לגבי הקריטריונים שלנו, אנא [שאל בפורום שלנו](https://discuss.privacyguides.net/latest) ואל תניח שלא שקלנו משהו כשהצענו את ההמלצות שלנו אם הוא לא רשום כאן. ישנם גורמים רבים שנחשבים ונדונים כאשר אנו ממליצים על פרויקט, ותיעוד כל אחד מהם הוא עבודה בתהליך.

### מערכות הפעלה

- חייבת להיות תוכנת קוד פתוח.
- חייב לתמוך בנעילת bootloader עם תמיכת מפתח AVB מותאמת אישית.
- חייב לקבל עדכוני אנדרואיד גדולים בתוך 0-1 חודשים מהשחרור.
- חייב לקבל עדכוני תכונות אנדרואיד (גרסה מינורית) בתוך 0-14 ימים מהשחרור.
- חייב לקבל תיקוני אבטחה רגילים בתוך 0-5 ימים מהשחרור.
- חייבים **לא** להיות "rooted" מהקופסה.
- חייב **לא** להפעיל את שירותי Google Play כברירת מחדל.
- חייב **לא** לדרוש שינוי מערכת כדי לתמוך בשירותי Google Play.

### מכשירים

- חייב לתמוך לפחות באחת ממערכות ההפעלה המומלצות שלנו.
- חייב להימכר כרגע חדש בחנויות.
- חייב לקבל לפחות 5 שנים של עדכוני אבטחה.
- חייב להיות חומרה ייעודית לרכיב מאובטח.

### יישומים

- יישומים בדף זה לא חייבים להיות ישימים לכל קטגוריית תוכנה אחרת באתר.
- יישומים כלליים צריכים להרחיב או להחליף את פונקציונליות הליבה של המערכת.
- יישומים צריכים לקבל עדכונים ותחזוקה שוטפים.
