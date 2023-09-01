---
title: "סקירה כללית של Qubes"
icon: simple/qubesos
description: Qubes היא מערכת הפעלה הבנויה סביב בידוד אפליקציות בתוך *qubes* (לשעבר "VMs") לאבטחה מוגברת.
---

[**Qubes OS**](../desktop.md#qubes-os) היא מערכת הפעלה בקוד פתוח המשתמשת ב[Xen](https://en.wikipedia.org/wiki/Xen) היפרוויזר לספק אבטחה חזקה עבור מחשוב שולחני באמצעות *qubes* מבודדים, (אשר הם מכונות וירטואליות). אתה יכול להקצות לכל *qube* רמת אמון על סמך מטרתו. מערכת ההפעלה Qubes מספקת אבטחה באמצעות בידוד. הוא מתיר פעולות רק על בסיס כל מקרה ומקרה ולכן הוא ההפך מ[badness enumeration](https://www.ranum.com/security/computer_security/editorials/dumb/).

## איך עובדת מערכת ההפעלה של Qubes?

Qubes משתמשת ב[מידור](https://www.qubes-os.org/intro/) כדי לשמור על אבטחת המערכת. Qubes נוצרים מתבניות, ברירת המחדל היא עבור Fedora, Debian ו-[Whonix](../desktop.md#whonix). מערכת ההפעלה Qubes מאפשרת לך גם ליצור [חד פעמי](https://www.qubes-os.org/doc/how-to-use-disposables/) *qubes* לשימוש חד פעמי.

??? "המונח *qubes* מתעדכן בהדרגה כדי להימנע מהתייחסות אליהם כ"מכונות וירטואליות"."

    חלק מהמידע כאן ובתיעוד של מערכת ההפעלה של Qubes עשוי להכיל שפה סותרת מכיוון שהמונח "appVM" משתנה בהדרגה ל-"qube". Qubes הם לא מכונות וירטואליות שלמות, אבל שומרים על פונקציונליות דומות ל-VMs.

![ארכיטקטורת Qubes](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>ארכיטקטורת Qubes, קרדיט: מהי הקדמה למערכת ההפעלה של Qubes</figcaption>

לכל qube יש [גבול צבעוני](https://www.qubes-os.org/screenshots/) שיכול לעזור לך לעקוב אחר התחום שבו היא פועלת. אתה יכול, למשל, להשתמש בצבע ספציפי עבור הדפדפן הבנקאי שלך, תוך שימוש בצבע אחר עבור דפדפן כללי שאינו מהימן.

![גבול צבוע](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>גבולות החלונות של Qubes, קרדיט: צילומי מסך של Qubes</figcaption>

## מדוע עלי להשתמש ב-Qubes?

מערכת ההפעלה Qubes שימושית אם [מודל האיום](../basics/threat-modeling.md) שלך דורש אבטחה ובידוד חזקות, כגון אם אתה חושב שתפתח קבצים לא מהימנים ממקורות לא מהימנים. סיבה טיפוסית לשימוש ב-Qubes OS היא לפתוח מסמכים ממקורות לא ידועים, אבל הרעיון הוא שאם qube בודד ייפגע זה לא ישפיע על שאר המערכת.

Qubes OS משתמשת ב-[דום0](https://wiki.xenproject.org/wiki/Dom0)Xen VM לשליטה ב-*קיובס* אחרים במערכת ההפעלה המארח, שכולם מציגים חלונות יישומים בודדים בסביבת שולחן העבודה של dom0. ישנם שימושים רבים לסוג זה של ארכיטקטורה. הנה כמה משימות שתוכל לבצע. אתה יכול לראות עד כמה בטוחים יותר תהליכים אלה נעשים על ידי שילוב שלבים מרובים.

### העתקה והדבקה של טקסט

אתה יכול [להעתיק ולהדביק טקסט](https://www.qubes-os.org/doc/how-to-copy-and-paste-text/) באמצעות `qvm-copy -to-vm` או ההוראות שלהלן:

1. הקש על **Ctrl+C** כדי לומר ל-*qube* שאתה נמצא בו שאתה רוצה להעתיק משהו.
2. הקש על **Ctrl+Shift+C** כדי לומר ל*qube* להפוך את המאגר הזה לזמין ללוח הגלובלי.
3. הקש על **Ctrl+Shift+V** ביעד *qube* כדי להפוך את הלוח הגלובלי לזמין.
4. לחץ על **Ctrl+V** ביעד *qube* כדי להדביק את התוכן במאגר.

### החלפת קבצים

כדי להעתיק ולהדביק קבצים וספריות (תיקיות) מ*qube* אחד לאחר, אתה יכול להשתמש באפשרות **העתק ל-AppVM אחר...** או **העבר ל-AppVM אחר...**. ההבדל הוא שהאפשרות ה**העבר** תמחק את הקובץ המקורי. כל אחת מהאפשרויות תגן על הלוח שלך מפני דליפה לכל *qubes* אחרים. זה מאובטח יותר מהעברת קבצים ברווח-אוויר. מחשב עם מרווח אוויר עדיין ייאלץ לנתח מחיצות או מערכות קבצים. זה לא נדרש עם מערכת ההעתקה inter-qube.

??? "ל-Qubes אין מערכות קבצים משלהם."

    אתה יכול [להעתיק ולהעביר קבצים](https://www.qubes-os.org/doc/how-to-copy-and-move-files/) בין *qubes*. כאשר עושים זאת השינויים לא מתבצעים באופן מיידי וניתן לבטל אותם בקלות במקרה של תאונה. כאשר אתה מפעיל *qube*, אין לו מערכת קבצים מתמשכת. אתה יכול ליצור ולמחוק קבצים, אבל השינויים האלה הם ארעיים.

### אינטראקציות בין-VM

[מסגרת qrexec](https://www.qubes-os.org/doc/qrexec/) היא חלק מרכזי ב-Qubes המאפשר תקשורת בין דומיינים. הוא בנוי על גבי ספריית Xen *vchan*, המאפשרת [בידוד באמצעות מדיניות](https://www.qubes-os.org/news/2020/06/22/new-qrexec-policy-system/).

## מקורות נוספים

למידע נוסף, אנו ממליצים לך לעיין בדפי התיעוד הנרחבים של Qubes OS הממוקמים ב[אתר האינטרנט של Qubes OS](https://www.qubes-os.org/doc/). ניתן להוריד עותקים לא מקוונים מ[מאגר התיעוד](https://github.com/QubesOS/qubes-doc) של Qubes OS.

- [ללא ספק מערכת ההפעלה המאובטחת ביותר בעולם](https://www.opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard/) (Open Technology Fund)
- [מידור תוכנה לעומת הפרדה פיזית](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf) (J. Rutkowska)
- [חלוקת החיים הדיגיטליים שלי לתחומי אבטחה](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html) (J. Rutkowska)
- [מאמרים קשורים](https://www.qubes-os.org/news/categories/#articles) (Qubes OS)
