---
title: סקירה כללית של לינוקס
icon: simple/linux
description: לינוקס היא חלופה למערכת הפעלה שולחנית ממוקדת פרטיות בקוד פתוח, אך לא כל ההפצות נוצרות שווה.
---

**Linux** היא חלופה למערכת הפעלה שולחנית בקוד פתוח, ממוקדת פרטיות. מול טלמטריה נרחבת וטכנולוגיות אחרות שפוגעות בפרטיות במערכות הפעלה מיינסטרים, שולחן העבודה של לינוקס נשאר הבחירה הברורה עבור אנשים שמחפשים שליטה מוחלטת על המחשבים שלהם מהיסוד.

האתר שלנו משתמש בדרך כלל במונח "Linux" כדי לתאר הפצות לינוקס של **שולחן העבודה**. מערכות הפעלה אחרות המשתמשות גם בליבת לינוקס כגון ChromeOS, Android ו-Qubes OS אינן נדונות בדף זה.

[המלצות לינוקס שלנו :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Privacy Notes

There are some notable privacy concerns with Linux which you should be aware of. Despite these drawbacks, desktop Linux distributions are still great for most people who want to:

- הימנע מטלמטריה שמגיעה לרוב עם מערכות הפעלה קנייניות
- לשמור על [חופש תוכנה](https://www.gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Use privacy focused systems such as [Whonix](https://www.whonix.org) or [Tails](https://tails.boum.org/)

### Open Source Security

It is a [common misconception](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) that Linux and other open-source software is inherently secure simply because the source code is available. There is an expectation that community verification occurs regularly, but this isn’t always [the case](https://seirdy.one/posts/2022/02/02/floss-security/).

In reality, distro security depends on a number of factors, such as project activity, developer experience, the level of rigor applied to code reviews, and how often attention is given to specific parts of the codebase that may go untouched for years.

### Missing Security Features

At the moment, desktop Linux [falls behind alternatives](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) like macOS or Android when it comes to certain security features. We hope to see improvements in these areas in the future.

- **Verified boot** on Linux is not as robust as alternatives such as Apple’s [Secure Boot](https://support.apple.com/guide/security/secac71d5623/web) or Android’s [Verified Boot](https://source.android.com/security/verifiedboot). Verified boot prevents persistent tampering by malware and [evil maid attacks](https://en.wikipedia.org/wiki/Evil_Maid_attack), but is still largely [unavailable on even the most advanced distributions](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- **Strong sandboxing** for apps on Linux is severely lacking, even with containerized apps like Flatpaks or sandboxing solutions like Firejail. Flatpak is the most promising sandboxing utility for Linux thus far, but is still deficient in many areas and allows for [unsafe defaults](https://flatkill.org/2020/) which allow most apps to trivially bypass their sandbox.

Additionally, Linux falls behind in implementing [exploit mitigations](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) which are now standard on other operating systems, such as Arbitrary Code Guard on Windows or Hardened Runtime on macOS. Also, most Linux programs and Linux itself are coded in memory-unsafe languages. Memory corruption bugs are responsible for the [majority of vulnerabilities](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code/) fixed and assigned a CVE. While this is also true for Windows and macOS, they are quickly making progress on adopting memory-safe languages—such as Rust and Swift, respectively—while there is no similar effort to rewrite Linux in a memory-safe language like Rust.

## בחירת ההפצה שלך

לא כל ההפצות של לינוקס נוצרו שוות. Our [Linux recommendation page](../desktop.md) is not meant to be an authoritative source on which distribution you should use, but our recommendations *are* aligned with the following guidelines. These are a few things you should keep in mind when choosing a distribution:

### מחזור שחרור

אנו ממליצים בחום לבחור בהפצות שנשארות קרובות למהדורות התוכנה היציבות במעלה הזרם, המכונה לעתים קרובות הפצות מהדורות מתגלגלות. הסיבה לכך היא שהפצות מחזור שחרור קפוא לרוב אינן מעדכנות גרסאות חבילה ונגררות לפי עדכוני אבטחה.

עבור הפצות קפואות כגון [Debian](https://www.debian.org/security/faq#handling), מתחזקים חבילות צפויים לבצע אחורה תיקונים כדי לתקן נקודות תורפה במקום להקפיץ את התוכנה ל- "הגרסה הבאה" שפורסמה על ידי המפתח במעלה הזרם. חלק מתיקוני האבטחה [לא](https://arxiv.org/abs/2105.14565) מקבלים [מזהה CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) (במיוחד תוכנה פחות פופולרית) כלל ולכן אינם נכנסים להפצה עם מודל התיקון הזה. כתוצאה מכך תיקוני אבטחה קלים מתעכבים לפעמים עד לגרסה הגדולה הבאה.

אנחנו לא מאמינים שהחזקת חבילות והחלת תיקוני ביניים הם רעיון טוב, מכיוון שהוא שונה מהדרך שבה המפתח התכוון שהתוכנה תעבוד. ל [Richard Brown](https://rootco.de/aboutme/) יש מצגת על נושא זה:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/i8c0mg_mS7U?local=true" title="מהדורות רגילות הן שגויות, גלגלו על החיים שלכם" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### עדכונים מסורתיים לעומת עדכונים אטומיים

באופן מסורתי, הפצות לינוקס מתעדכנות על ידי עדכון רציף של החבילות הרצויות. עדכונים מסורתיים כמו אלה המשמשים בהפצות מבוססות פדורה, Arch Linux ודביאן יכולים להיות פחות אמינים אם מתרחשת שגיאה בזמן העדכון.

הפצות עדכון אטומי מיישמות עדכונים במלואם או לא בכלל. בדרך כלל, מערכות עדכון עסקאות הן גם אטומיות.

מערכת עדכון עסקה יוצרת תמונת מצב שנעשתה לפני ואחרי החלת עדכון. אם עדכון נכשל בכל עת (אולי בגלל הפסקת חשמל), ניתן להחזיר את העדכון בקלות ל"מצב התקין האחרון הידוע."

שיטת העדכון Atomic משמשת להפצות בלתי ניתנות לשינוי כמו Silverblue, Tumbleweed ו-NixOS ויכולה להשיג אמינות עם מודל זה. [Adam Šamalík](https://twitter.com/adsamalik) סיפק מצגת על האופן שבו `rpm-ostree` עובד עם Silverblue:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/-hpV5l-gJnQ?local=true" title="בואו ננסה את Fedora Silverblue - מערכת הפעלה שולחנית בלתי ניתנת לשינוי! - Adam Šamalik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### הפצות "ממוקדות אבטחה"

לעתים קרובות קיים בלבול מסוים בין הפצות "ממוקדות אבטחה" והפצות "לבדיקת חדירות". A quick search for “the most secure Linux distribution” will often give results like Kali Linux, Black Arch, or Parrot OS. הפצות אלו הן הפצות בדיקות חדירה פוגעניות המאגדות כלים לבדיקת מערכות אחרות. הם אינם כוללים "אבטחה נוספת" או הקלות הגנתיות המיועדות לשימוש קבוע.

### הפצות מבוססות Arch

Arch and Arch-based distributions are not recommended for those new to Linux (regardless of distribution) as they require regular [system maintenance](https://wiki.archlinux.org/title/System_maintenance). Arch does not have a distribution update mechanism for the underlying software choices. כתוצאה מכך, עליך להישאר מודע למגמות הנוכחיות ולאמץ טכנולוגיות מכיוון שהן מחליפות שיטות ישנות בעצמך.

עבור מערכת מאובטחת, מצפים ממך גם שיהיה לך מספיק ידע בלינוקס כדי להגדיר כראוי אבטחה עבור המערכת שלהם, כגון אימוץ מערכת [בקרת כניסה חובה](https://en.wikipedia.org/wiki/Mandatory_access_control), הגדרת רשימות שחורות של [מודול ליבה](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) רשימות שחורות, הקשחת פרמטרי אתחול, מניפולציה של [סיסקטל](https://en.wikipedia.org/wiki/Sysctl) פרמטרים, ולדעת אילו רכיבים הם צריכים כמו [Polkit](https://en.wikipedia.org/wiki/Polkit).

Anyone using the [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **must** be comfortable auditing PKGBUILDs that they download from that service. חבילות AUR הן תוכן המיוצר בקהילה ואינן נבדקות בשום צורה, ולכן הן פגיעות להתקפות שרשרת אספקת תוכנה, [מה שקרה למעשה](https://www.bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository/).

The AUR should always be used sparingly, and often there is a lot of bad advice on various pages which direct people to blindly use [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) without sufficient warning. אזהרות דומות חלות על שימוש בארכיון חבילות אישיות של צד שלישי (PPA) בהפצות מבוססות דביאן או בפרויקטים קהילתיים (COPR) בפדורה.

If you are experienced with Linux and wish to use an Arch-based distribution, we generally recommend mainline Arch Linux over any of its derivatives.

Additionally, we recommend **against** these two Arch derivatives specifically:

- **Manjaro**: הפצה זו מעכבת חבילות למשך שבועיים כדי לוודא שהשינויים שלהן לא יישברו, לא כדי לוודא שהמעלה הזרם יציב. כאשר נעשה שימוש בחבילות AUR, הן בנויות לרוב על פי [ספריות](https://en.wikipedia.org/wiki/Library_(computing)) העדכניות ביותר מהמאגרים של Arch.
- **Garuda**: הם משתמשים ב[Chaotic-AUR](https://aur.chaotic.cx/) אשר מרכיב באופן אוטומטי ועיוור חבילות מה- AUR. אין תהליך אימות כדי לוודא שחבילות AUR אינן סובלות מהתקפות שרשרת האספקה.

### הפצות ליבה של לינוקס ו-"Libre"

We recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://www.phoronix.com/news/GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode.

## המלצות כלליות

### הצפנת כונן

לרוב ההפצות של לינוקס יש אפשרות בתוך תוכנית ההתקנה שלה להפעלת [LUKS](../encryption.md#linux-unified-key-setup) FDE. אם אפשרות זו לא מוגדרת בזמן ההתקנה, תצטרך לגבות את הנתונים שלך ולהתקין מחדש, מכיוון שההצפנה מוחלת לאחר [חלוקת דיסקים ](https://en.wikipedia.org/wiki/Disk_partitioning), אבל לפני ש[מערכות הקבצים](https://en.wikipedia.org/wiki/File_system) מתעצבות. אנו מציעים גם למחוק בצורה מאובטחת את מכשיר האחסון שלך:

- [מחיקת נתונים מאובטחת :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure/)

### החלף

Consider using [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) instead of a traditional swap file or partition to avoid writing potentially sensitive memory data to persistent storage (and improve performance). Fedora-based distributions [use ZRAM by default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

If you require suspend-to-disk (hibernation) functionality, you will still need to use a traditional swap file or partition. Make sure that any swap space you do have on a persistent storage device is [encrypted](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) at a minimum to mitigate some of these threats.

### Wayland

We recommend using a desktop environment that supports the [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)) display protocol, as it was developed with security [in mind](https://lwn.net/Articles/589147/). Its predecessor ([X11](https://en.wikipedia.org/wiki/X_Window_System)) does not support GUI isolation, which allows any window to [record, log, and inject inputs in other windows](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), making any attempt at sandboxing futile. While there are options to do nested X11 such as [Xpra](https://en.wikipedia.org/wiki/Xpra) or [Xephyr](https://en.wikipedia.org/wiki/Xephyr), they often come with negative performance consequences, and are neither convenient to set up nor preferable over Wayland.

למרבה המזל, סביבות נפוצות כגון [GNOME](https://www.gnome.org), [KDE](https://kde.org) וה- למנהל החלונות [Sway](https://swaywm.org) יש תמיכה ב-Wayland. חלק מההפצות כמו Fedora ו- Tumbleweed משתמשות בו כברירת מחדל, וחלק אחרות עשויות לעשות זאת בעתיד מכיוון ש-X11 נמצא ב[מצב תחזוקה קשה](https://www.phoronix.com/news/X.Org-Maintenance-Mode-Quickly). אם אתה משתמש באחת מהסביבות האלה זה קל כמו לבחור את הפגישה "Wayland" במנהל התצוגה של שולחן העבודה ([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)).

אנו ממליצים **נגד** להשתמש בסביבות שולחן עבודה או במנהלי חלונות שאין להם תמיכה ב-Wayland, כגון Cinnamon (ברירת מחדל ב-Linux Mint), Pantheon (ברירת מחדל במערכת ההפעלה היסודית), MATE, Xfce, ו-i3.

### קושחה קניינית (עדכוני מיקרוקוד)

Some Linux distributions (such as [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)-based or DIY distros) don’t come with the proprietary [microcode](https://en.wikipedia.org/wiki/Microcode) updates which patch critical security vulnerabilities. כמה דוגמאות בולטות לפגיעויות אלה כוללות [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), ועוד [hardware vulnerabilities](https://www.kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

We **highly recommend** that you install microcode updates, as they contain important security patches for the CPU which can not be fully mitigated in software alone. לפדורה ול-openSUSE יש את עדכוני המיקרוקוד כברירת מחדל.

### עדכונים

רוב ההפצות של לינוקס יתקינו עדכונים אוטומטית או יזכירו לך לעשות זאת. חשוב לשמור על מערכת ההפעלה שלך מעודכנת כדי שהתוכנה שלך תתוקן כאשר מתגלה פגיעות.

Some distributions (particularly those aimed at advanced users) are more bare bones and expect you to do things yourself (e.g. Arch or Debian). אלה ידרשו להפעיל את "מנהל החבילות" (`apt`, `pacman`, `dnf` וכו') באופן ידני על מנת לקבל עדכוני אבטחה חשובים.

בנוסף, הפצות מסוימות לא יוריד עדכוני קושחה באופן אוטומטי. לשם כך תצטרך להתקין את [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

## תיקוני פרטיות

### כתובת MAC אקראית

Many desktop Linux distributions (Fedora, openSUSE, etc.) come with [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) to configure Ethernet and Wi-Fi settings.

אפשר [לבצע באקראי](https://fedoramagazine.org/randomize-mac-address-nm/) את [כתובת MAC](https://en.wikipedia.org/wiki/MAC_address) בעת שימוש ב-NetworkManager. זה מספק קצת יותר פרטיות ברשתות Wi-Fi מכיוון שהוא מקשה על מעקב אחר מכשירים ספציפיים ברשת שאליה אתה מחובר. זה [**לא**](https://papers.mathyvanhoef.com/wisec2016.pdf) הופך אותך לאנונימי.

אנו ממליצים לשנות את ההגדרה ל-**אקראי** </strong>במקום** יציב**, כפי שהוצע ב[מאמר](https://fedoramagazine.org/randomize-mac-address-nm/).

אם אתה משתמש ב [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), יהיה עליך להגדיר [`MACAddressPolicy=random`](https://www.freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) אשר יאפשר [RFC 7844 (פרופילי אנונימיות עבור לקוחות DHCP)](https://www.freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

MAC address randomization is primarily beneficial for Wi-Fi connections. For Ethernet connections, randomizing your MAC address provides little (if any) benefit, because a network administrator can trivially identify your device by other means (such as inspecting the port you are connected to on the network switch). הקצאה אקראית של כתובות Wi-Fi MAC תלויה בתמיכה מהקושחה של ה-Wi-Fi.

### מזהים אחרים

ישנם מזהי מערכת נוספים שתרצו להיזהר מהם. עליך להקדיש לכך מחשבה כדי לראות אם הוא חל על [מצב האיום ](../basics/threat-modeling.md)שלך:

- **שמות מארח:** שם המארח של המערכת שלך משותף עם הרשתות שאליהן אתה מתחבר. עליך להימנע מלכלול מונחים מזהים כמו השם או מערכת ההפעלה שלך בשם המארח שלך, במקום להיצמד למונחים גנריים או מחרוזות אקראיות.
- **שמות משתמש:** באופן דומה, שם המשתמש שלך משמש במגוון דרכים במערכת שלך. שקול להשתמש במונחים גנריים כמו "משתמש" ולא בשמך האמיתי.
- **מזהה מכונה:** במהלך ההתקנה נוצר מזהה מכונה ייחודי ומאוחסן במכשיר שלך. שקול [להגדיר אותו למזהה גנרי](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### ספירת מערכת

פרויקט Fedora [סופר](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) כמה מערכות ייחודיות ניגשים למראות שלו באמצעות [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) משתנה במקום מזהה ייחודי. פדורה עושה זאת כדי לקבוע עומס והספקת שרתים טובים יותר עבור עדכונים במידת הצורך.

[אפשרות](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) זו כבויה כעת כברירת מחדל. אנו ממליצים להוסיף את `countme=false` ל-`/etc/dnf/dnf.conf` למקרה שהוא יופעל בעתיד. במערכות המשתמשות ב-`rpm-ostree` כגון Silverblue, אפשרות ה-countme מושבתת על ידי מיסוך של [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems/) טיימר.

openSUSE משתמשת גם ב[מזהה ייחודי](https://en.opensuse.org/openSUSE:Statistics) כדי לספור מערכות, אותן ניתן להשבית על ידי מחיקת הקובץ `/var/lib/zypp/AnonymousUniqueId`.
