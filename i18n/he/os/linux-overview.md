---
title: סקירה כללית של לינוקס
icon: simple/linux
description: לינוקס היא חלופה למערכת הפעלה שולחנית ממוקדת פרטיות בקוד פתוח, אך לא כל ההפצות נוצרות שווה.
---

**Linux** היא חלופה למערכת הפעלה שולחנית בקוד פתוח, ממוקדת פרטיות. In the face of pervasive telemetry and other privacy-encroaching technologies in mainstream operating systems, desktop Linux has remained the clear choice for people looking for total control over their computers from the ground up.

האתר שלנו משתמש בדרך כלל במונח "Linux" כדי לתאר הפצות לינוקס של **שולחן העבודה**. מערכות הפעלה אחרות המשתמשות גם בליבת לינוקס כגון ChromeOS, Android ו-Qubes OS אינן נדונות בדף זה.

[המלצות לינוקס שלנו :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## הערות פרטיות

יש כמה חששות בולטים של פרטיות עם לינוקס שכדאי להיות מודעים אליהם. למרות החסרונות הללו, הפצות לינוקס לשולחן העבודה עדיין נהדרות עבור רוב האנשים שרוצים:

- הימנע מטלמטריה שמגיעה לרוב עם מערכות הפעלה קנייניות
- Maintain [software freedom](https://gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Use privacy-focused systems such as [Whonix](../desktop.md#whonix) or [Tails](../desktop.md#tails)

### Open-Source Security

It is a [common misconception](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) that Linux and other open-source software are inherently secure simply because the source code is available. There is an expectation that community verification occurs regularly, but this isn’t always [the case](https://seirdy.one/posts/2022/02/02/floss-security).

במציאות, אבטחת הפצה תלויה במספר גורמים, כגון פעילות הפרויקט, חווית מפתח, רמת הקפדנות המופעלת על ביקורות קוד, וכמה פעמים ניתנת תשומת לב לחלקים ספציפיים של בסיס הקוד שעלולים להישאר ללא נגיעה במשך שנים.

### תכונות אבטחה חסרות

כרגע, Linux [ נופל מאחורי חלופות](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) כמו macOS או Android כשמדובר בתכונות אבטחה מסוימות. אנו מקווים לראות שיפורים בתחומים אלו בעתיד.

- **אתחול מאומת** בלינוקס אינו חזק כמו חלופות כגון [אתחול מאובטח של אפל](https://support.apple.com/guide/security/secac71d5623/web) או [אתחול מאומת](https://source.android.com/security/verifiedboot) של אנדרואיד. אתחול מאומת מונע התעסקות מתמשכת על ידי תוכנות זדוניות ו[התקפות עוזרות מרושעות](https://en.wikipedia.org/wiki/Evil_Maid_attack), אך הוא עדיין ברובו [לא זמין אפילו בהפצות המתקדמות ביותר](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- **ארגז חול חזק** עבור אפליקציות בלינוקס חסר מאוד, אפילו עם אפליקציות מכולות כמו Flatpaks או פתרונות ארגז חול כמו Firejail. Flatpak is the most promising sandboxing utility for Linux thus far, but is still deficient in many areas and allows for [unsafe defaults](https://flatkill.org/2020) which permit most apps to trivially bypass their sandbox.

בנוסף, לינוקס מפגרת בהטמעת [הפחתות ניצול](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) אשר כעת סטנדרטיות במערכות הפעלה אחרות, כגון Code Guard שרירותי ב-Windows או Hardened Runtime ב-macOS. כמו כן, רוב תוכניות הלינוקס ולינוקס עצמה מקודדות בשפות שאינן בטוחות בזיכרון. Memory corruption bugs are responsible for the [majority of vulnerabilities](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code) fixed and assigned a CVE. למרות שזה נכון גם עבור Windows ו-macOS, הם מתקדמים במהירות באימוץ שפות בטוחות לזיכרון - כמו Rust ו- Swift, בהתאמה - בעוד שאין מאמץ דומה לשכתב את לינוקס בשפה בטוחה לזיכרון כמו Rust.

## בחירת ההפצה שלך

לא כל ההפצות של לינוקס נוצרו שוות. [דף ההמלצות שלנו ללינוקס](../desktop.md) לא נועד להיות מקור סמכותי באיזו הפצה כדאי להשתמש, אבל ההמלצות שלנו *הן * בהתאם להנחיות הבאות. אלה כמה דברים שכדאי לזכור בעת בחירת הפצה:

### מחזור שחרור

אנו ממליצים בחום לבחור בהפצות שנשארות קרובות למהדורות התוכנה היציבות במעלה הזרם, המכונה לעתים קרובות הפצות מהדורות מתגלגלות. הסיבה לכך היא שהפצות מחזור שחרור קפוא לרוב אינן מעדכנות גרסאות חבילה ונגררות לפי עדכוני אבטחה.

For frozen distributions such as [Debian](https://debian.org/security/faq#handling), package maintainers are expected to backport patches to fix vulnerabilities rather than bump the software to the “next version” released by the upstream developer. Some security fixes (particularly for less popular software) [do not](https://arxiv.org/abs/2105.14565) receive a [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) at all and therefore do not make it into the distribution with this patching model. As a result, minor security fixes are sometimes held back until the next major release.

אנחנו לא מאמינים שהחזקת חבילות והחלת תיקוני ביניים הם רעיון טוב, מכיוון שהוא שונה מהדרך שבה המפתח התכוון שהתוכנה תעבוד. [Richard Brown](https://rootco.de/aboutme) has a presentation about this:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/i8c0mg_mS7U?local=true" title="מהדורות רגילות הן שגויות, גלגלו על החיים שלכם" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Traditional vs Atomic Updates

באופן מסורתי, הפצות לינוקס מתעדכנות על ידי עדכון רציף של החבילות הרצויות. Traditional updates such as those used in Fedora, Arch Linux, and Debian-based distributions can be less reliable if an error occurs while updating.

Atomic updating distributions, on the other hand, apply updates in full or not at all. On an atomic distribution, if an error occurs while updating (perhaps due to a power failure), nothing is changed on the system.

The atomic update method can achieve reliability with this model and is used for [distributions](../desktop.md#atomic-distributions) like Silverblue and NixOS. [Adam Šamalík](https://twitter.com/adsamalik) סיפק מצגת על האופן שבו `rpm-ostree` עובד עם Silverblue:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/-hpV5l-gJnQ?local=true" title="בואו ננסה את Fedora Silverblue - מערכת הפעלה שולחנית בלתי ניתנת לשינוי! - Adam Šamalik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### הפצות "ממוקדות אבטחה"

לעתים קרובות קיים בלבול מסוים בין הפצות "ממוקדות אבטחה" והפצות "לבדיקת חדירות". חיפוש מהיר של "הפצת לינוקס המאובטחת ביותר" ייתן לרוב תוצאות כמו Kali Linux, Black Arch או Parrot OS. הפצות אלו הן הפצות בדיקות חדירה פוגעניות המאגדות כלים לבדיקת מערכות אחרות. הם אינם כוללים "אבטחה נוספת" או הקלות הגנתיות המיועדות לשימוש קבוע.

### הפצות מבוססות Arch

הפצות מבוססות Arch ו-Arch אינן מומלצות למשתמשים חדשים ב-Linux (ללא קשר להפצה) מכיוון שהן דורשות [תחזוקת מערכת](https://wiki.archlinux.org/title/System_maintenance) רגילה. ל- Arch אין מנגנון עדכון הפצה עבור אפשרויות התוכנה הבסיסיות. As a result you have to stay aware with current trends and adopt technologies on your own as they supersede older practices.

עבור מערכת מאובטחת, מצפים ממך גם שיהיה לך מספיק ידע בלינוקס כדי להגדיר כראוי אבטחה עבור המערכת שלהם, כגון אימוץ מערכת [בקרת כניסה חובה](https://en.wikipedia.org/wiki/Mandatory_access_control), הגדרת רשימות שחורות של [מודול ליבה](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) רשימות שחורות, הקשחת פרמטרי אתחול, מניפולציה של [סיסקטל](https://en.wikipedia.org/wiki/Sysctl) פרמטרים, ולדעת אילו רכיבים הם צריכים כמו [Polkit](https://en.wikipedia.org/wiki/Polkit).

כל מי שמשתמש ב[Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **חייב** להרגיש בנוח ביקורת PKGBUILD שהם מורידים מהשירות הזה. AUR packages are community-produced content and are not vetted in any way, and therefore are vulnerable to software supply chain attacks, which has in fact happened [in the past](https://bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository).

תמיד יש להשתמש ב-AUR במשורה, ולעתים קרובות יש הרבה עצות רעות בדפים שונים שמפנים אנשים להשתמש באופן עיוור ב[עוזרים של AUR](https://wiki.archlinux.org/title/AUR_helpers) ללא אזהרה מספקת. Similar warnings apply to the use of third-party Personal Package Archives (PPAs) on Debian-based distributions or Community Projects (COPR) on Fedora.

אם אתה מנוסה עם לינוקס וברצונך להשתמש בהפצה מבוססת Arch, אנו ממליצים בדרך כלל על Arch Linux על פני כל אחת מהנגזרות שלו.

בנוסף, אנו ממליצים על **נגד** שתי נגזרות Arch אלו במיוחד:

- **Manjaro**: הפצה זו מעכבת חבילות למשך שבועיים כדי לוודא שהשינויים שלהן לא יישברו, לא כדי לוודא שהמעלה הזרם יציב. כאשר נעשה שימוש בחבילות AUR, הן בנויות לרוב על פי [ספריות](https://en.wikipedia.org/wiki/Library_(computing)) העדכניות ביותר מהמאגרים של Arch.
- **Garuda**: They use [Chaotic-AUR](https://aur.chaotic.cx) which automatically and blindly compiles packages from the AUR. אין תהליך אימות כדי לוודא שחבילות AUR אינן סובלות מהתקפות שרשרת האספקה.

### הפצות ליבה של לינוקס ו-"Libre"

We recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://phoronix.com/news/GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode.

## המלצות כלליות

### הצפנת כונן

לרוב ההפצות של לינוקס יש אפשרות בתוך תוכנית ההתקנה שלה להפעלת [LUKS](../encryption.md#linux-unified-key-setup) FDE. אם אפשרות זו לא מוגדרת בזמן ההתקנה, תצטרך לגבות את הנתונים שלך ולהתקין מחדש, מכיוון שההצפנה מוחלת לאחר [חלוקת דיסקים ](https://en.wikipedia.org/wiki/Disk_partitioning), אבל לפני ש[מערכות הקבצים](https://en.wikipedia.org/wiki/File_system) מתעצבות. אנו מציעים גם למחוק בצורה מאובטחת את מכשיר האחסון שלך:

- [מחיקת נתונים מאובטחת :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure)

### החלף

שקול להשתמש ב-[ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) במקום קובץ החלפה או מחיצה מסורתיים כדי להימנע מכתיבת נתוני זיכרון שעלולים להיות רגישים לאחסון מתמשך ( ולשפר ביצועים). הפצות מבוססות פדורה [משתמשות ב-ZRAM כברירת מחדל](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

אם אתה זקוק לפונקציונליות של השהייה לדיסק (תרדמה), עדיין תצטרך להשתמש בקובץ החלפה או מחיצה מסורתיים. ודא שכל שטח החלפה שיש לך בהתקן אחסון קבוע [מוצפן](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) לכל הפחות כדי להפחית חלק מהאיומים הללו.

### Wayland

We recommend using a desktop environment that supports the [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)) display protocol, as it was developed with security [in mind](https://lwn.net/Articles/589147). קודמו ([X11](https://en.wikipedia.org/wiki/X_Window_System)) אינו תומך בבידוד GUI, המאפשר לכל חלון [תיעדו, רשמו והזריקו קלט בחלונות אחרים](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), מה שהופך כל ניסיון לארגז חול חסר תועלת.

Fortunately, [Wayland compositors](https://en.wikipedia.org/wiki/Wayland_(protocol)#Wayland_compositors) such as those included with [GNOME](https://gnome.org) and [KDE Plasma](https://kde.org) now have good support for Wayland along with some other compositors that use [wlroots](https://gitlab.freedesktop.org/wlroots/wlroots/-/wikis/Projects-which-use-wlroots), (e.g. [Sway](https://swaywm.org)). Some distributions like Fedora and Tumbleweed use it by default, and some others may do so in the future as X11 is in [hard maintenance mode](https://phoronix.com/news/X.Org-Maintenance-Mode-Quickly). If you’re using one of those environments, it is as easy as selecting the “Wayland” session at the desktop display manager ([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)).

אנו ממליצים **נגד** להשתמש בסביבות שולחן עבודה או במנהלי חלונות שאין להם תמיכה ב-Wayland, כגון Cinnamon (ברירת מחדל ב-Linux Mint), Pantheon (ברירת מחדל במערכת ההפעלה היסודית), MATE, Xfce, ו-i3.

### קושחה קניינית (עדכוני מיקרוקוד)

חלק מההפצות של לינוקס (כגון [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre) מבוססות או הפצות עשה זאת בעצמך) אינן מגיעות עם קנייני [microcode](https://en.wikipedia.org/wiki/Microcode) עדכוני המתקן פרצות אבטחה קריטיות. Some notable examples of these vulnerabilities include [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), and other [hardware vulnerabilities](https://kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

אנו **ממליצים בחום** להתקין עדכוני מיקרוקוד, מכיוון שהם מכילים תיקוני אבטחה חשובים עבור ה-CPU אשר לא ניתן להפחית באופן מלא בתוכנה בלבד. Fedora and openSUSE both apply microcode updates by default.

### עדכונים

רוב ההפצות של לינוקס יתקינו עדכונים אוטומטית או יזכירו לך לעשות זאת. חשוב לשמור על מערכת ההפעלה שלך מעודכנת כדי שהתוכנה שלך תתוקן כאשר מתגלה פגיעות.

חלק מההפצות (במיוחד אלו המיועדות למשתמשים מתקדמים) הן עצמות יותר ומצפות ממך לעשות דברים בעצמך (למשל Arch או Debian). אלה ידרשו להפעיל את "מנהל החבילות" (`apt`, `pacman`, `dnf` וכו') באופן ידני על מנת לקבל עדכוני אבטחה חשובים.

בנוסף, הפצות מסוימות לא יוריד עדכוני קושחה באופן אוטומטי. For that, you will need to install [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

## תיקוני פרטיות

### כתובת MAC אקראית

הפצות רבות של לינוקס לשולחן העבודה (Fedora, openSUSE וכו') מגיעות עם [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) כדי להגדיר הגדרות Ethernet ו-Wi-Fi.

It is possible to [randomize](https://fedoramagazine.org/randomize-mac-address-nm) the [MAC address](https://en.wikipedia.org/wiki/MAC_address) when using NetworkManager. זה מספק קצת יותר פרטיות ברשתות Wi-Fi מכיוון שהוא מקשה על מעקב אחר מכשירים ספציפיים ברשת שאליה אתה מחובר. זה [**לא**](https://papers.mathyvanhoef.com/wisec2016.pdf) הופך אותך לאנונימי.

We recommend changing the setting to **random** instead of **stable**, as suggested in the [article](https://fedoramagazine.org/randomize-mac-address-nm).

If you are using [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), you will need to set [`MACAddressPolicy=random`](https://freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) which will enable [RFC 7844 (Anonymity Profiles for DHCP Clients)](https://freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

כתובות MAC אקראית מועילה בעיקר עבור חיבורי Wi-Fi. עבור חיבורי אינטרנט, כתובת אקראית של ה-MAC שלך מספקת תועלת מועטה (אם בכלל), מכיוון שמנהל רשת יכול לזהות את המכשיר שלך באופן טריוויאלי באמצעים אחרים (כגון בדיקת היציאה אליה אתה מחובר במתג הרשת). הקצאה אקראית של כתובות Wi-Fi MAC תלויה בתמיכה מהקושחה של ה-Wi-Fi.

### מזהים אחרים

ישנם מזהי מערכת נוספים שתרצו להיזהר מהם. עליך להקדיש לכך מחשבה כדי לראות אם הוא חל על [מצב האיום ](../basics/threat-modeling.md)שלך:

- **שמות מארח:** שם המארח של המערכת שלך משותף עם הרשתות שאליהן אתה מתחבר. עליך להימנע מלכלול מונחים מזהים כמו השם או מערכת ההפעלה שלך בשם המארח שלך, במקום להיצמד למונחים גנריים או מחרוזות אקראיות.
- **שמות משתמש:** באופן דומה, שם המשתמש שלך משמש במגוון דרכים במערכת שלך. שקול להשתמש במונחים גנריים כמו "משתמש" ולא בשמך האמיתי.
- **Machine ID:** During installation, a unique machine ID is generated and stored on your device. שקול [להגדיר אותו למזהה גנרי](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### ספירת מערכת

פרויקט Fedora [סופר](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) כמה מערכות ייחודיות ניגשים למראות שלו באמצעות [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) משתנה במקום מזהה ייחודי. פדורה עושה זאת כדי לקבוע עומס והספקת שרתים טובים יותר עבור עדכונים במידת הצורך.

[אפשרות](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) זו כבויה כעת כברירת מחדל. אנו ממליצים להוסיף את `countme=false` ל-`/etc/dnf/dnf.conf` למקרה שהוא יופעל בעתיד. On systems that use `rpm-ostree` such as Silverblue, the countme option is disabled by masking the [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems) timer.

openSUSE also uses a [unique ID](https://en.opensuse.org/openSUSE:Statistics) to count systems, which can be disabled by emptying the `/var/lib/zypp/AnonymousUniqueId` file.
