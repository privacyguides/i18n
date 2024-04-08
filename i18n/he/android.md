---
meta_title: "Android Recommendations: GrapheneOS and DivestOS - Privacy Guides"
title: "אנדרואיד"
icon: 'simple/android'
description: You can replace the operating system on your Android phone with these secure and privacy-respecting alternatives.
cover: android.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Private Android Operating Systems
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
      name: Google
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

[:octicons-home-16:](https://source.android.com){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject){ .card-link title="Source Code" }

אלו הן מערכות ההפעלה, המכשירים והאפליקציות של אנדרואיד שאנו ממליצים על מנת למקסם את האבטחה והפרטיות של המכשיר הנייד שלך. למידע נוסף על אנדרואיד:

[סקירה כללית של אנדרואיד :material-arrow-right-drop-circle:](os/android-overview.md ""){.md-button}

## נגזרות AOSP

אנו ממליצים להתקין במכשיר שלך אחת ממערכות ההפעלה המותאמות אישית של אנדרואיד, המפורטות לפי סדר העדפה, בהתאם לתאימות המכשיר שלך למערכות הפעלה אלו.

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

למכשירי סוף החיים (כגון מכשירי "תמיכה מורחבת" של GrapheneOS או CalyxOS) אין תיקוני אבטחה מלאים (עדכוני קושחה) עקב הפסקת התמיכה של OEM. מכישירים אלה אינם יכולים להיחשב מאובטחים לחלוטין ללא קשר לתוכנה המותקנת.

</div>

### GrapheneOS

<div class="admonition recommendation" markdown>

![לוגו GrapheneOS](assets/img/android/grapheneos.svg#only-light){ align=right }
![לוגו GrapheneOS](assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** היא הבחירה הטובה ביותר בכל הנוגע לפרטיות ואבטחה.

GrapheneOS מספקת [הקשחת אבטחה](https://en.wikipedia.org/wiki/Hardening_(computing)) ושיפורי פרטיות נוספים. יש לו [מקצה זיכרון מוקשה](https://github.com/GrapheneOS/hardened_malloc), הרשאות רשת וחיישנים ועוד [תכונות אבטחה](https://grapheneos.org/features) שונות. GrapheneOS מגיעה גם עם עדכוני קושחה מלאים ו-builds חתומים, כך שאתחול מאומת נתמך באופן מלא.

[:octicons-home-16: Homepage](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

</div>

GrapheneOS תומך ב-[Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), המריץ את [Google Play Services](https://en.wikipedia.org/wiki/Google_Play_Services) בארגז חול מלא כמו כל אפליקציה רגילה אחרת. This means you can take advantage of most Google Play Services, such as [push notifications](https://firebase.google.com/docs/cloud-messaging), while giving you full control over their permissions and access, and while containing them to a specific [work profile](os/android-overview.md#work-profile) or [user profile](os/android-overview.md#user-profiles) of your choice.

Google Pixel phones are the only devices that currently meet GrapheneOS's [hardware security requirements](https://grapheneos.org/faq#future-devices).

[מדוע אנו ממליצים על GrapheneOS על פני CalyxOS :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos ""){.md-button}

### DivestOS

<div class="admonition recommendation" markdown>

![DivestOS logo](assets/img/android/divestos.svg){ align=right }

**DivestOS** is a soft-fork of [LineageOS](https://lineageos.org).
DivestOS inherits many [supported devices](https://divestos.org/index.php?page=devices&base=LineageOS) from LineageOS. יש לו builds חתומים, מה שמאפשר לקבל [אתחול מאומת](https://source.android.com/security/verifiedboot) בחלק מהמכשירים שאינם Pixel.

[:octicons-home-16: דף הבית](https://divestos.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="שירות בצל" }
[:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="מדיניות פרטיות" }
[:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=תיעוד}
[:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="קוד מקור" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=לתרומה }

</div>

ל - DivestOS יש פגיעות ליבה ([CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [שמתוקן](https://gitlab.com/divested-mobile/cve_checker) אוטומטית, פחות בועות קנייניות, וקובץ [מארחים](https://divested.dev/index.php?page=dnsbl) מותאם. Its hardened WebView, [Mulch](https://gitlab.com/divested-mobile/mulch), enables [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) for all architectures and [network state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning), and receives out-of-band updates. DivestOS כוללת גם תיקוני ליבה מ-GrapheneOS ומאפשרת את כל תכונות האבטחה הזמינות של הליבה באמצעות [הקשחת defconfig](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). All kernels newer than version 3.4 include full page [sanitization](https://lwn.net/Articles/334747) and all ~22 Clang-compiled kernels have [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) enabled.

DivestOS מיישמת כמה תיקוני הקשחת מערכת שפותחו במקור עבור GrapheneOS. DivestOS 16.0 ומעלה מיישמת את החלפת הרשאות [`אינטרנט`](https://developer.android.com/training/basics/network-ops/connecting) וחיישנים של GrapheneOS, [מקצית זיכרון מוקשחת](https://github.com/GrapheneOS/hardened_malloc), [השרצת מנהלים](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/#additional-hardening), [קונסטיפיקציה](https://en.wikipedia.org/wiki/Const_(computer_programming)) של [JNI](https://en.wikipedia.org/wiki/Java_Native_Interface) ותיקוני התקשות [ביונית](https://en.wikipedia.org/wiki/Bionic_(software)) חלקית. 17.1 and higher features GrapheneOS's per-network full [MAC randomization](https://en.wikipedia.org/wiki/MAC_address#Randomization) option, [`ptrace_scope`](https://kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) control, and automatic reboot/Wi-Fi/Bluetooth [timeout options](https://grapheneos.org/features).

DivestOS משתמשת ב-F-Droid כחנות האפליקציות המוגדרת כברירת מחדל. בדרך כלל אנו [ממליצים להימנע מ-F-Droid](#f-droid), אך אין לעשות זאת ב-DivestOS; המפתחים מעדכנים את האפליקציות שלהם באמצעות מאגרי F-Droid משלהם ([DivestOS Official](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) and [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2)). We recommend disabling the official F-Droid app and using [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) **with the DivestOS repositories enabled** to keep those components up to date. לגבי אפליקציות אחרות, השיטות המומלצות שלנו להשגתן עדיין חלות.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

עדכון קושחה של DivestOS [סטטוס](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) ובקרת איכות משתנים בין המכשירים שבהם הוא תומך. אנו עדיין ממליצים על GrapheneOS בהתאם לתאימות המכשיר שלך. עבור מכשירים אחרים, DivestOS היא אלטרנטיבה טובה.

לא לכל המכשירים הנתמכים יש אתחול מאומת, וחלקם מבצעים אותו טוב יותר מאחרים.

</div>

## מכשירי אנדרואיד

בעת רכישת מכשיר, אנו ממליצים לרכוש אחד חדש ככל האפשר. התוכנה והקושחה של מכשירים ניידים נתמכות רק לזמן מוגבל, כך שקנייה חדשה מאריכה את תוחלת החיים עד כמה שניתן.

הימנע מרכישת טלפונים ממפעילי רשתות סלולריות. לאלה יש לרוב **מאתחול נעול** ואינם תומכים ב[פתיחת נעילה של OEM](https://source.android.com/devices/bootloader/locking_unlocking). גרסאות טלפון אלה ימנעו ממך להתקין כל סוג של הפצת אנדרואיד חלופית.

היה מאוד **זהיר** בקניית טלפונים יד שנייה משוק אונליין. בדוק תמיד את המוניטין של המוכר. If the device is stolen, there's a possibility of it being entered in the [IMEI database](https://gsma.com/get-involved/working-groups/terminal-steering-group/imei-database). קיים גם סיכון שכרוך בהיותך קשור לפעילות של הבעלים הקודם.

עוד כמה טיפים לגבי מכשירי אנדרואיד ותאימות מערכות הפעלה:

- אל תקנו מכשירים שהגיעו או קרובים לסוף החיים שלהם, עדכוני קושחה נוספים חייבים להיות מסופקים על ידי היצרן.
- אל תקנו טלפונים טעונים מראש של LineageOS או /e/ OS או כל טלפון אנדרואיד ללא תמיכה מתאימה של [אתחול מאומת](https://source.android.com/security/verifiedboot) ועדכוני קושחה. גם למכשירים האלה אין דרך לבדוק אם התעסקו בהם.
- בקיצור, אם לא מופיעה כאן הפצת מכשיר או אנדרואיד, כנראה שיש סיבה טובה. Check out our [forum](https://discuss.privacyguides.net) to find details!

### גוגל פיקסל

טלפונים של גוגל פיקסל הם המכשירים **היחידים** שאנו ממליצים לרכישה. לטלפונים של Pixel יש אבטחת חומרה חזקה יותר מכל מכשירי אנדרואיד אחרים הקיימים כיום בשוק, בשל תמיכת AVB נאותה עבור מערכות הפעלה של צד שלישי ושבבי האבטחה המותאמים אישית [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) של גוגל הפועלים כ-Secure Element.

<div class="admonition recommendation" markdown>

![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }

מכשירי **גוגל פיקסל** ידועים כבעלי אבטחה טובה ותומכים כראוי ב[אתחול מאומת](https://source.android.com/security/verifiedboot), גם בעת התקנת מערכות הפעלה מותאמות אישית.

החל מ-**Pixel 8** ו-**8 Pro**, מכשירי Pixel מקבלים לפחות 7 שנים של עדכוני אבטחה מובטחים, מה שמבטיח תוחלת חיים ארוכה בהרבה בהשוואה ל-2-5 שנים שמציעות בדרך כלל יצרני OEM מתחרים.

[:material-shopping: חנות](https://store.google.com/category/phones){ .md-button .md-button--primary }

</div>

רכיבים מאובטחים כמו Titan M2 מוגבלים יותר מסביבת הביצוע המהימנה של המעבד המשמשת את רוב הטלפונים האחרים מכיוון שהם משמשים רק לאחסון סודות, הוכחת חומרה והגבלת קצב, לא להפעלת תוכניות "מהימנות". טלפונים ללא Secure Element חייבים להשתמש ב-TEE עבור *כל* הפונקציות הללו, וכתוצאה מכך משטח התקפה גדול יותר.

טלפונים של Google Pixel משתמשים במערכת הפעלה TEE בשם Trusty שהיא [קוד פתוח](https://source.android.com/security/trusty#whyTrusty), בניגוד לטלפונים רבים אחרים.

ההתקנה של GrapheneOS בטלפון Pixel קלה עם [מתקין האינטרנט שלהם](https://grapheneos.org/install/web). If you don't feel comfortable doing it yourself and are willing to spend a bit of extra money, check out the [NitroPhone](https://shop.nitrokey.com/shop) as they come preloaded with GrapheneOS from the reputable [Nitrokey](https://nitrokey.com/about) company.

עוד כמה טיפים לרכישת Google Pixel:

- אם אתה מחפש מציאה על מכשיר פיקסל, אנו מציעים לקנות דגם "**a**", מיד לאחר יציאת ספינת הדגל הבאה. הנחות זמינות בדרך כלל מכיוון שגוגל תנסה לסלק את המלאי שלה.
- שקול אפשרויות מכות מחיר ומבצעים המוצעים בחנויות פיזיות.
- עיין באתרי עסקאות אןנליין של קהילתיות במדינה שלך. אלה יכולים להתריע על מכירות טובות.
- Google provides a list showing the [support cycle](https://support.google.com/nexus/answer/4457705) for each one of their devices. The price per day for a device can be calculated as: <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline" class="tml-display" style="display:inline math;"> <mfrac> <mtext>Cost</mtext> <mrow> <mtext>End of Life Date</mtext> <mo>−</mo> <mtext>Current Date</mtext> </mrow> </mfrac> </math> , meaning that the longer use of the device the lower cost per day.
- If the Pixel is unavailable in your region, the [NitroPhone](https://shop.nitrokey.com/shop) can be shipped globally.

## אפליקציות כלליות

אנו ממליצים על מגוון רחב של אפליקציות אנדרואיד ברחבי אתר זה. האפליקציות המפורטות כאן הן בלעדיות לאנדרואיד ומשפרות או מחליפות באופן ספציפי את פונקציונליות המערכת המרכזית.

### Shelter

<div class="admonition recommendation" markdown>

![Shelter לוגו](assets/img/android/shelter.svg){ align=right }

**Shelter** היא אפליקציה שעוזרת לך למנף את הפונקציונליות של פרופיל העבודה של אנדרואיד כדי לבודד או לשכפל אפליקציות במכשיר שלך.

Shelter תומך בחסימת פרופילים חוצי חיפוש אנשי קשר ושיתוף קבצים בין פרופילים באמצעות מנהל הקבצים המוגדר כברירת מחדל ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).

[:octicons-repo-16: Repository](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Source Code" }
[:octicons-heart-16:](https://patreon.com/PeterCxy){ .card-link title=Contribute }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Shelter is recommended over [Insular](https://secure-system.gitlab.io/Insular) and [Island](https://github.com/oasisfeng/island) as it supports [contact search blocking](https://secure-system.gitlab.io/Insular/faq.html).

כשאתה משתמש ב-Shelter, אתה נותן אמון מלא במפתח שלו, שכן Shelter פועל כ[מנהל מכשיר](https://developer.android.com/guide/topics/admin/device-admin) כדי ליצור את פרופיל העבודה, וכן יש לו גישה נרחבת לנתונים המאוחסנים בפרופיל העבודה.

</div>

### Secure Camera

<div class="admonition recommendation" markdown>

![Secure camera לוגו](assets/img/android/secure_camera.svg#only-light){ align=right }
![Secure camera לוגו](assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

**Secure Camera** היא אפליקציית מצלמה המתמקדת בפרטיות ואבטחה שיכולה לצלם תמונות, סרטונים וקודי QR. הרחבות של ספקי CameraX (פורטרט, HDR, ראיית לילה, ריטוש פנים ואוטומטי) נתמכות גם במכשירים זמינים.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

תכונות הפרטיות העיקריות כוללות:

- הסרה אוטומטית של מטא נתונים של [Exif](https://en.wikipedia.org/wiki/Exif) (מופעל כברירת מחדל)
- שימוש בממשק ה-API החדש של ה[מדיה](https://developer.android.com/training/data-storage/shared/media), לכן אין צורך ב[הרשאות אחסון](https://developer.android.com/training/data-storage)
- אין צורך בהרשאת מיקרופון אלא אם ברצונך להקליט קול

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

מטא נתונים אינם נמחקים כעת מקבצי וידאו אבל זה מתוכנן.

המטא נתונים של כיוון התמונה לא נמחקים. אם תפעיל מיקום ב(Secure Camera) זה גם **לא** יימחק. If you want to delete that later you will need to use an external app such as [ExifEraser](data-redaction.md#exiferaser-android).

</div>

### Secure PDF Viewer

<div class="admonition recommendation" markdown>

![Secure PDF Viewer לוגו](assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Secure PDF Viewer לוגו](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

**Secure PDF Viewer** הוא מציג PDF המבוסס על [pdf.js](https://en.wikipedia.org/wiki/PDF.js) שאינו דורש הרשאות כלשהן. ה-PDF מוזן לתוך [ארגז חול](https://en.wikipedia.org/wiki/Sandbox_(software_development))[webview](https://developer.android.com/guide/webapps/webview). המשמעות היא שזה לא דורש הרשאה ישירה כדי לגשת לתוכן או לקבצים.

[תוכן-אבטחה-מדיניות](https://en.wikipedia.org/wiki/Content_Security_Policy) משמש כדי לאכוף שמאפייני JavaScript והסגנון ב-WebView הם תוכן סטטי לחלוטין.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## קבלת בקשות

### Obtainium

<div class="admonition recommendation" markdown>

![Obtainium לוגו](assets/img/android/obtainium.svg){ align=right }

**Obtainium** הוא מנהל אפליקציות המאפשר לך להתקין ולעדכן אפליקציות ישירות מדף ההפצות של המפתח עצמו (כלומר. GitHub, GitLab, אתר האינטרנט של המפתח וכו'), במקום חנות/מאגר אפליקציות מרכזי. הוא תומך בעדכוני רקע אוטומטיים באנדרואיד 12 ומעלה.

[:octicons-repo-16: Repository](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ImranR98/Obtainium/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

Obtainium מאפשר לך להוריד קבצי התקנת APK ממגוון רחב של מקורות, וזה תלוי בך לוודא שהמקורות והאפליקציות האלה לגיטימיים. For example, using Obtainium to install Signal from [Signal's APK landing page](https://signal.org/android/apk) should be fine, but installing from third-party APK repositories like Aptoide or APKPure may pose additional risks. הסיכון של התקנת *עדכון* זדוני נמוך יותר, מכיוון שאנדרואיד עצמו מוודא שכל עדכוני האפליקציה חתומים על ידי אותו מפתח כמו האפליקציה הקיימת בטלפון שלך לפני התקנתם.

### GrapheneOS App Store

חנות האפליקציות של GrapheneOS זמינה ב-[GitHub](https://github.com/GrapheneOS/Apps/releases). הוא תומך באנדרואיד 12 ומעלה ומסוגל לעדכן את עצמו. The app store has standalone applications built by the GrapheneOS project such as the [Auditor](https://attestation.app), [Camera](https://github.com/GrapheneOS/Camera), and [PDF Viewer](https://github.com/GrapheneOS/PdfViewer). אם אתם מחפשים אפליקציות אלו, אנו ממליצים בחום להשיג אותן מחנות האפליקציות של GrapheneOS במקום מחנות Play, שכן האפליקציות בחנות שלהן חתומות על ידי חתימת הפרויקט של ה-GrapheneOS שלגוגל אין גישה אליה.

### Aurora Store

חנות Google Play דורשת חשבון Google כדי להתחבר וזה לא נהדר לפרטיות. אתה יכול לעקוף את זה על ידי שימוש בלקוח חלופי, כגון Aurora Store.

<div class="admonition recommendation" markdown>

![Aurora Store לוגו](assets/img/android/aurora-store.webp){ align=right }

**Aurora Store** היא לקוח של חנות Google Play שאינה דורשת חשבון Google, שירותי Google Play או microG כדי להוריד אפליקציות.

[:octicons-home-16: Homepage](https://auroraoss.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

Aurora Store לא מאפשרת להוריד אפליקציות בתשלום עם תכונת החשבון האנונימי שלהן. You can optionally log in with your Google account with Aurora Store to download apps you have purchased, which does give access to the list of apps you've installed to Google. However, you still benefit from not requiring the full Google Play client and Google Play Services or microG on your device.

### התראות RSS באופן ידני

For apps that are released on platforms like GitHub and GitLab, you may be able to add an RSS feed to your [news aggregator](news-aggregators.md) that will help you keep track of new releases.

![RSS APK](./assets/img/android/rss-apk-light.png#only-light) ![RSS APK](./assets/img/android/rss-apk-dark.png#only-dark) ![שינויים ב-APK](./assets/img/android/rss-changes-light.png#only-light) ![שינויים ב-APK](./assets/img/android/rss-changes-dark.png#only-dark)

#### Github

ב-GitHub, באמצעות [Secure Camera](#secure-camera) כדוגמה, תנווט ל[דף ההפצות](https://github.com/GrapheneOS/Camera/releases) שלו ותוסיף את `.atom` לכתובת האתר:

`https://github.com/GrapheneOS/Camera/releases.atom`

#### GitLab

ב-GitLab, באמצעות [Aurora Store](#aurora-store) כדוגמה, תנווט אל [מאגר הפרויקטים](https://gitlab.com/AuroraOSS/AuroraStore) שלו ותוסיף `/-/tags?format=atom` לכתובת האתר:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

#### אימות טביעות אצבע של APK

אם אתה מוריד קבצי APK להתקנה ידנית, אתה יכול לאמת את החתימה שלהם עם הכלי [`apksigner`](https://developer.android.com/studio/command-line/apksigner), שהוא חלק מ[כלי הבנייה](https://developer.android.com/studio/releases/build-tools) של אנדרואיד.

1. Install [Java JDK](https://oracle.com/java/technologies/downloads).

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

5. לאחר מכן ניתן להשוות את ה-hashes המתקבלים עם מקור אחר. Some developers such as Signal [show the fingerprints](https://signal.org/android/apk) on their website.

    ```bash
    Signer #1 certificate DN: CN=GrapheneOS
    Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
    Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
    Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
    ```

### F-Droid

![לוגו F-Droid](assets/img/android/f-droid.svg){ align=right width=120px }

==אנו ממליצים רק על F-Droid כדרך להשיג אפליקציות שלא ניתן להשיג באמצעים שלמעלה.== F-Droid מומלצת לעתים קרובות כחלופה ל-Google Play, במיוחד בקהילת הפרטיות. האפשרות להוסיף מאגרי צד שלישי ולא להיות מוגבלים לגן המוקף חומה של גוגל הובילה לפופולריות שלו. F-Droid additionally has [reproducible builds](https://f-droid.org/en/docs/Reproducible_Builds) for some applications and is dedicated to free and open-source software. עם זאת, ישנם כמה חסרונות הקשורים לאבטחה באופן שבו F-Droid בונה, חותם ומספק חבילות:

בשל תהליך בניית האפליקציות שלהם, אפליקציות במאגר ה-F-Droid הרשמי מפגרות לעתים קרובות בפיגור לגבי עדכונים. מנהלי F-Droid גם עושים שימוש חוזר במזהי חבילה בזמן חתימת אפליקציות עם המפתחות שלהם, וזה לא אידיאלי מכיוון שהוא נותן אמון אולטימטיבי לצוות F-Droid. בנוסף, הדרישות להכללת אפליקציה במאגר ה-F-Droid הרשמי הן פחות מחמירות מחנויות אפליקציות אחרות כמו Google Play, כלומר F-Droid נוטה לארח הרבה יותר אפליקציות ישנות יותר, לא מתוחזקות או לא יותר לעמוד ב[תקני אבטחה מודרניים](https://developer.android.com/google/play/requirements/target-sdk).

Other popular third-party repositories for F-Droid such as [IzzyOnDroid](https://apt.izzysoft.de/fdroid) alleviate some of these concerns. מאגר IzzyOnDroid מושך רכיבים ישירות מ-GitHub והוא הדבר הטוב הבא למאגרים של המפתחים עצמם. עם זאת, זה לא משהו שאנחנו יכולים להמליץ עליו באופן מלא, מכיוון שאפליקציות בדרך כלל [מוסרות](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446) מהמאגר הזה אם הם יתווספו מאוחר יותר למאגר F-Droid הראשי. למרות שזה הגיוני (מכיוון שהמטרה של המאגר המסוים הזה היא לארח אפליקציות לפני שהן מתקבלות למאגר ה-F-Droid הראשי), זה יכול להשאיר אותך עם אפליקציות מותקנות שכבר לא מקבלים עדכונים.

That said, the [F-Droid](https://f-droid.org/en/packages) and [IzzyOnDroid](https://apt.izzysoft.de/fdroid) repositories are home to countless apps, so they can be a useful tool to search for and discover open-source apps that you can then download through other means such as the Play Store, Aurora Store, or by getting the APK directly from the developer. כדאי להשתמש במיטב שיקול הדעת כשאתה מחפש אפליקציות חדשות בשיטה זו, ולעקוב אחר התדירות שבה האפליקציה מתעדכנת. אפליקציות מיושנות עשויות להסתמך על ספריות שאינן נתמכות, בין היתר, מהוות סיכון אבטחה פוטנציאלי.

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

In some rare cases, the developer of an app will only distribute it through F-Droid ([Gadgetbridge](https://gadgetbridge.org) is one example of this). If you really need an app like that, we recommend using the newer [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) client instead of the original F-Droid app to obtain it. F-Droid Basic supports automatic background updates without privileged extension or root, and has a reduced feature set (limiting attack surface).

</div>

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

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
