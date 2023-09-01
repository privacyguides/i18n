---
title: "סקירה כללית של Qubes"
icon: simple/qubesos
description: Qubes היא מערכת הפעלה הבנויה סביב בידוד אפליקציות בתוך *qubes* (לשעבר "VMs") לאבטחה מוגברת.
---

[**Qubes OS**](../desktop.md#qubes-os) היא מערכת הפעלה בקוד פתוח המשתמשת ב[Xen](https://en.wikipedia.org/wiki/Xen) היפרוויזר לספק אבטחה חזקה עבור מחשוב שולחני באמצעות *qubes* מבודדים, (אשר הם מכונות וירטואליות). You can assign each *qube* a level of trust based on its purpose. Qubes OS provides security by using isolation. It only permits actions on a per-case basis and therefore is the opposite of [badness enumeration](https://www.ranum.com/security/computer_security/editorials/dumb/).

## איך עובדת מערכת ההפעלה של Qubes?

Qubes משתמשת ב[מידור](https://www.qubes-os.org/intro/) כדי לשמור על אבטחת המערכת. Qubes נוצרים מתבניות, ברירת המחדל היא עבור Fedora, Debian ו-[Whonix](../desktop.md#whonix). מערכת ההפעלה Qubes מאפשרת לך גם ליצור [חד פעמי](https://www.qubes-os.org/doc/how-to-use-disposables/) *qubes* לשימוש חד פעמי.

??? "The term *qubes* is gradually being updated to avoid referring to them as "virtual machines"."

    Some of the information here and on the Qubes OS documentation may contain conflicting language as the "appVM" term is gradually being changed to "qube". Qubes are not entire virtual machines, but maintain similar functionalities to VMs.

![ארכיטקטורת Qubes](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>ארכיטקטורת Qubes, קרדיט: מהי הקדמה למערכת ההפעלה של Qubes</figcaption>

Each qube has a [colored border](https://www.qubes-os.org/screenshots/) that can help you keep track of the domain in which it runs. אתה יכול, למשל, להשתמש בצבע ספציפי עבור הדפדפן הבנקאי שלך, תוך שימוש בצבע אחר עבור דפדפן כללי שאינו מהימן.

![גבול צבוע](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>גבולות החלונות של Qubes, קרדיט: צילומי מסך של Qubes</figcaption>

## מדוע עלי להשתמש ב-Qubes?

מערכת ההפעלה Qubes שימושית אם [מודל האיום](../basics/threat-modeling.md) שלך דורש אבטחה ובידוד חזקות, כגון אם אתה חושב שתפתח קבצים לא מהימנים ממקורות לא מהימנים. סיבה טיפוסית לשימוש ב-Qubes OS היא לפתוח מסמכים ממקורות לא ידועים, אבל הרעיון הוא שאם qube בודד ייפגע זה לא ישפיע על שאר המערכת.

Qubes OS utilizes [dom0](https://wiki.xenproject.org/wiki/Dom0) Xen VM for controlling other *qubes* on the host OS, all of which display individual application windows within dom0's desktop environment. There are many uses for this type of architecture. Here are some tasks you can perform. You can see just how much more secure these processes are made by incorporating multiple steps.

### העתקה והדבקה של טקסט

אתה יכול [להעתיק ולהדביק טקסט](https://www.qubes-os.org/doc/how-to-copy-and-paste-text/) באמצעות `qvm-copy -to-vm` או ההוראות שלהלן:

1. הקש על **Ctrl+C** כדי לומר ל-*qube* שאתה נמצא בו שאתה רוצה להעתיק משהו.
2. הקש על **Ctrl+Shift+C** כדי לומר ל*qube* להפוך את המאגר הזה לזמין ללוח הגלובלי.
3. הקש על **Ctrl+Shift+V** ביעד *qube* כדי להפוך את הלוח הגלובלי לזמין.
4. לחץ על **Ctrl+V** ביעד *qube* כדי להדביק את התוכן במאגר.

### החלפת קבצים

כדי להעתיק ולהדביק קבצים וספריות (תיקיות) מ*qube* אחד לאחר, אתה יכול להשתמש באפשרות **העתק ל-AppVM אחר...** או **העבר ל-AppVM אחר...**. ההבדל הוא שהאפשרות ה**העבר** תמחק את הקובץ המקורי. Either option will protect your clipboard from being leaked to any other *qubes*. This is more secure than air-gapped file transfer. An air-gapped computer will still be forced to parse partitions or file systems. זה לא נדרש עם מערכת ההעתקה inter-qube.

??? "Qubes do not have their own filesystems."

    You can [copy and move files](https://www.qubes-os.org/doc/how-to-copy-and-move-files/) between *qubes*. כאשר עושים זאת השינויים לא מתבצעים באופן מיידי וניתן לבטל אותם בקלות במקרה של תאונה. When you run a *qube*, it does not have a persistent filesystem. You can create and delete files, but these changes are ephemeral.

### אינטראקציות בין-VM

The [qrexec framework](https://www.qubes-os.org/doc/qrexec/) is a core part of Qubes which allows communication between domains. הוא בנוי על גבי ספריית Xen *vchan*, המאפשרת [בידוד באמצעות מדיניות](https://www.qubes-os.org/news/2020/06/22/new-qrexec-policy-system/).

## מקורות נוספים

למידע נוסף, אנו ממליצים לך לעיין בדפי התיעוד הנרחבים של Qubes OS הממוקמים ב[אתר האינטרנט של Qubes OS](https://www.qubes-os.org/doc/). ניתן להוריד עותקים לא מקוונים מ[מאגר התיעוד](https://github.com/QubesOS/qubes-doc) של Qubes OS.

- [ללא ספק מערכת ההפעלה המאובטחת ביותר בעולם](https://www.opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard/) (Open Technology Fund)
- [מידור תוכנה לעומת הפרדה פיזית](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf) (J. Rutkowska)
- [חלוקת החיים הדיגיטליים שלי לתחומי אבטחה](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html) (J. Rutkowska)
- [מאמרים קשורים](https://www.qubes-os.org/news/categories/#articles) (Qubes OS)
