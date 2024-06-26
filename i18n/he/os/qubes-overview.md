---
title: "סקירה כללית של Qubes"
icon: simple/qubesos
description: Qubes היא מערכת הפעלה הבנויה סביב בידוד אפליקציות בתוך *qubes* (לשעבר "VMs") לאבטחה מוגברת.
---

[**Qubes OS**](../desktop.md#qubes-os) היא מערכת הפעלה בקוד פתוח המשתמשת ב[Xen](https://en.wikipedia.org/wiki/Xen) היפרוויזר לספק אבטחה חזקה עבור מחשוב שולחני באמצעות *qubes* מבודדים, (אשר הם מכונות וירטואליות). אתה יכול להקצות לכל *qube* רמת אמון על סמך מטרתו. מערכת ההפעלה Qubes מספקת אבטחה באמצעות בידוד. It only permits actions on a per-case basis and therefore is the opposite of [badness enumeration](https://ranum.com/security/computer_security/editorials/dumb).

## איך עובדת מערכת ההפעלה של Qubes?

Qubes uses [compartmentalization](https://qubes-os.org/intro) to keep the system secure. Qubes נוצרים מתבניות, ברירת המחדל היא עבור Fedora, Debian ו-[Whonix](../desktop.md#whonix). Qubes OS also allows you to create once-use [disposable](https://qubes-os.org/doc/how-to-use-disposables) *qubes*.

<details class="note" markdown>
<summary>The term <em>qubes</em> is gradually being updated to avoid referring to them as "virtual machines".</summary>

חלק מהמידע כאן ובתיעוד של מערכת ההפעלה של Qubes עשוי להכיל שפה סותרת מכיוון שהמונח "appVM" משתנה בהדרגה ל-"qube". Qubes הם לא מכונות וירטואליות שלמות, אבל שומרים על פונקציונליות דומות ל-VMs.

</details>

![ארכיטקטורת Qubes](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>ארכיטקטורת Qubes, קרדיט: מהי הקדמה למערכת ההפעלה של Qubes</figcaption>

Each qube has a [colored border](https://qubes-os.org/screenshots) that can help you keep track of the domain in which it runs. אתה יכול, למשל, להשתמש בצבע ספציפי עבור הדפדפן הבנקאי שלך, תוך שימוש בצבע אחר עבור דפדפן כללי שאינו מהימן.

![גבול צבוע](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>גבולות החלונות של Qubes, קרדיט: צילומי מסך של Qubes</figcaption>

## מדוע עלי להשתמש ב-Qubes?

מערכת ההפעלה Qubes שימושית אם [מודל האיום](../basics/threat-modeling.md) שלך דורש אבטחה ובידוד חזקות, כגון אם אתה חושב שתפתח קבצים לא מהימנים ממקורות לא מהימנים. סיבה טיפוסית לשימוש ב-Qubes OS היא לפתוח מסמכים ממקורות לא ידועים, אבל הרעיון הוא שאם qube בודד ייפגע זה לא ישפיע על שאר המערכת.

Qubes OS משתמשת ב-[דום0](https://wiki.xenproject.org/wiki/Dom0)Xen VM לשליטה ב-*קיובס* אחרים במערכת ההפעלה המארח, שכולם מציגים חלונות יישומים בודדים בסביבת שולחן העבודה של dom0. ישנם שימושים רבים לסוג זה של ארכיטקטורה. הנה כמה משימות שתוכל לבצע. אתה יכול לראות עד כמה בטוחים יותר תהליכים אלה נעשים על ידי שילוב שלבים מרובים.

### העתקה והדבקה של טקסט

You can [copy and paste text](https://qubes-os.org/doc/how-to-copy-and-paste-text) using `qvm-copy-to-vm` or the below instructions:

1. הקש על **Ctrl+C** כדי לומר ל-*qube* שאתה נמצא בו שאתה רוצה להעתיק משהו.
2. הקש על **Ctrl+Shift+C** כדי לומר ל*qube* להפוך את המאגר הזה לזמין ללוח הגלובלי.
3. הקש על **Ctrl+Shift+V** ביעד *qube* כדי להפוך את הלוח הגלובלי לזמין.
4. לחץ על **Ctrl+V** ביעד *qube* כדי להדביק את התוכן במאגר.

### החלפת קבצים

כדי להעתיק ולהדביק קבצים וספריות (תיקיות) מ*qube* אחד לאחר, אתה יכול להשתמש באפשרות **העתק ל-AppVM אחר...** או **העבר ל-AppVM אחר...**. ההבדל הוא שהאפשרות ה**העבר** תמחק את הקובץ המקורי. כל אחת מהאפשרויות תגן על הלוח שלך מפני דליפה לכל *qubes* אחרים. זה מאובטח יותר מהעברת קבצים ברווח-אוויר. מחשב עם מרווח אוויר עדיין ייאלץ לנתח מחיצות או מערכות קבצים. זה לא נדרש עם מערכת ההעתקה inter-qube.

<details class="note" markdown>
<summary>Qubes do not have their own filesystems.</summary>

You can [copy and move files](https://qubes-os.org/doc/how-to-copy-and-move-files) between *qubes*. כאשר עושים זאת השינויים לא מתבצעים באופן מיידי וניתן לבטל אותם בקלות במקרה של תאונה. When you run a *qube*, it does not have a persistent filesystem. אתה יכול ליצור ולמחוק קבצים, אבל השינויים האלה הם ארעיים.

</details>

### אינטראקציות בין-VM

The [qrexec framework](https://qubes-os.org/doc/qrexec) is a core part of Qubes which allows communication between domains. It is built on top of the Xen library *vchan*, which facilitates [isolation through policies](https://qubes-os.org/news/2020/06/22/new-qrexec-policy-system).

## Connecting to Tor via a VPN

We [recommend](../advanced/tor-overview.md) connecting to the Tor network via a [VPN](../vpn.md) provider, and luckily Qubes makes this easy to do with a combination of ProxyVMs and Whonix.

After [creating a new ProxyVM](https://forum.qubes-os.org/t/configuring-a-proxyvm-vpn-gateway/19061) which connects to the VPN of your choice, you can chain your Whonix qubes to that ProxyVM **before** they connect to the Tor network, by setting the NetVM of your Whonix **Gateway** (`sys-whonix`) to the newly-created ProxyVM.

Your qubes should be configured in a manner similar to this:

| Qube name       | Qube description                                                                                    | NetVM           |
| --------------- | --------------------------------------------------------------------------------------------------- | --------------- |
| sys-net         | *Your default network qube (pre-installed)*                                                         | *n/a*           |
| sys-firewall    | *Your default firewall qube (pre-installed)*                                                        | sys-net         |
| ==sys-proxyvm== | The VPN ProxyVM you [created](https://forum.qubes-os.org/t/configuring-a-proxyvm-vpn-gateway/19061) | sys-firewall    |
| sys-whonix      | Your Whonix Gateway VM                                                                              | ==sys-proxyvm== |
| anon-whonix     | Your Whonix Workstation VM                                                                          | sys-whonix      |

## מקורות נוספים

For additional information we encourage you to consult the extensive Qubes OS documentation pages located on the [Qubes OS Website](https://qubes-os.org/doc). ניתן להוריד עותקים לא מקוונים מ[מאגר התיעוד](https://github.com/QubesOS/qubes-doc) של Qubes OS.

- [Arguably the world's most secure operating system](https://opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard) (Open Technology Fund)
- [מידור תוכנה לעומת הפרדה פיזית](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf) (J. Rutkowska)
- [חלוקת החיים הדיגיטליים שלי לתחומי אבטחה](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html) (J. Rutkowska)
- [Related Articles](https://qubes-os.org/news/categories/#articles) (Qubes OS)
