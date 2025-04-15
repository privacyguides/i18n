---
title: Linux Overview
icon: simple/linux
description: Linux is an open-source, privacy-focused desktop operating system alternative, but not all distribitions are created equal.
---

**Linux** היא חלופה למערכת הפעלה שולחנית בקוד פתוח, ממוקדת פרטיות. In the face of pervasive telemetry and other privacy-encroaching technologies in mainstream operating systems, desktop Linux has remained the clear choice for people looking for total control over their computers from the ground up.

האתר שלנו משתמש בדרך כלל במונח "Linux" כדי לתאר הפצות לינוקס של **שולחן העבודה**. מערכות הפעלה אחרות המשתמשות גם בליבת לינוקס כגון ChromeOS, Android ו-Qubes OS אינן נדונות בדף זה.

[המלצות לינוקס שלנו :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Security Notes

There are some notable security concerns with Linux which you should be aware of. למרות החסרונות הללו, הפצות לינוקס לשולחן העבודה עדיין נהדרות עבור רוב האנשים שרוצים:

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

בנוסף, לינוקס מפגרת בהטמעת [הפחתות ניצול](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) אשר כעת סטנדרטיות במערכות הפעלה אחרות, כגון Code Guard שרירותי ב-Windows או Hardened Runtime ב-macOS. כמו כן, רוב תוכניות הלינוקס ולינוקס עצמה מקודדות בשפות שאינן בטוחות בזיכרון. Memory corruption bugs are responsible for the [majority of vulnerabilities](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code) fixed and assigned a CVE. While this is also true for Windows and macOS, they are quickly making progress on adopting memory-safe languages such as Rust and Swift, respectively.

## בחירת ההפצה שלך

לא כל ההפצות של לינוקס נוצרו שוות. [דף ההמלצות שלנו ללינוקס](../desktop.md) לא נועד להיות מקור סמכותי באיזו הפצה כדאי להשתמש, אבל ההמלצות שלנו *הן * בהתאם להנחיות הבאות. אלה כמה דברים שכדאי לזכור בעת בחירת הפצה:

### מחזור שחרור

אנו ממליצים בחום לבחור בהפצות שנשארות קרובות למהדורות התוכנה היציבות במעלה הזרם, המכונה לעתים קרובות הפצות מהדורות מתגלגלות. הסיבה לכך היא שהפצות מחזור שחרור קפוא לרוב אינן מעדכנות גרסאות חבילה ונגררות לפי עדכוני אבטחה.

For frozen distributions such as [Debian](https://debian.org/security/faq#handling), package maintainers are expected to backport patches to fix vulnerabilities rather than bump the software to the “next version” released by the upstream developer. Some security fixes (particularly for less popular software) [do not](https://arxiv.org/abs/2105.14565) receive a [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) at all and therefore do not make it into the distribution with this patching model. As a result, minor security fixes are sometimes held back until the next major release.

אנחנו לא מאמינים שהחזקת חבילות והחלת תיקוני ביניים הם רעיון טוב, מכיוון שהוא שונה מהדרך שבה המפתח התכוון שהתוכנה תעבוד. [Richard Brown](https://rootco.de/aboutme) has a presentation about this:

- [Regular Releases are Wrong, Roll for your life](https://youtu.be/i8c0mg_mS7U) <small>(YouTube)</small>

### Traditional vs Atomic Updates

באופן מסורתי, הפצות לינוקס מתעדכנות על ידי עדכון רציף של החבילות הרצויות. Traditional updates such as those used in Fedora, Arch Linux, and Debian-based distributions can be less reliable if an error occurs while updating.

Distros which use atomic updates, on the other hand, apply updates in full or not at all. On an atomic distribution, if an error occurs while updating (perhaps due to a power failure), nothing is changed on the system.

The atomic update method can achieve reliability with this model and is used for [distributions](../desktop.md#atomic-distributions) like Silverblue and NixOS. [Adam Šamalík](https://twitter.com/adsamalik) provides a presentation on how `rpm-ostree` works with Silverblue:

- [Let's try Fedora Silverblue — an immutable desktop OS! - Adam Šamalík](https://youtu.be/-hpV5l-gJnQ) <small>(YouTube)</small>

### הפצות "ממוקדות אבטחה"

לעתים קרובות קיים בלבול מסוים בין הפצות "ממוקדות אבטחה" והפצות "לבדיקת חדירות". חיפוש מהיר של "הפצת לינוקס המאובטחת ביותר" ייתן לרוב תוצאות כמו Kali Linux, Black Arch או Parrot OS. הפצות אלו הן הפצות בדיקות חדירה פוגעניות המאגדות כלים לבדיקת מערכות אחרות. הם אינם כוללים "אבטחה נוספת" או הקלות הגנתיות המיועדות לשימוש קבוע.

### הפצות מבוססות Arch

הפצות מבוססות Arch ו-Arch אינן מומלצות למשתמשים חדשים ב-Linux (ללא קשר להפצה) מכיוון שהן דורשות [תחזוקת מערכת](https://wiki.archlinux.org/title/System_maintenance) רגילה. ל- Arch אין מנגנון עדכון הפצה עבור אפשרויות התוכנה הבסיסיות. As a result you have to stay aware with current trends and adopt technologies on your own as they supersede older practices.

For a secure system, you are also expected to have sufficient Linux knowledge to properly set up security for their system such as adopting a [mandatory access control](#mandatory-access-control) system, setting up [kernel module](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) blacklists, hardening boot parameters, manipulating [sysctl](https://en.wikipedia.org/wiki/Sysctl) parameters, and knowing what components they need such as [Polkit](https://en.wikipedia.org/wiki/Polkit).

כל מי שמשתמש ב[Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **חייב** להרגיש בנוח ביקורת PKGBUILD שהם מורידים מהשירות הזה. AUR packages are community-produced content and are not vetted in any way, and therefore are vulnerable to software [:material-package-variant-closed-remove: Supply Chain Attacks](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}, which has in fact happened [in the past](https://bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository).

תמיד יש להשתמש ב-AUR במשורה, ולעתים קרובות יש הרבה עצות רעות בדפים שונים שמפנים אנשים להשתמש באופן עיוור ב[עוזרים של AUR](https://wiki.archlinux.org/title/AUR_helpers) ללא אזהרה מספקת. Similar warnings apply to the use of third-party Personal Package Archives (PPAs) on Debian-based distributions or Community Projects (COPR) on Fedora.

אם אתה מנוסה עם לינוקס וברצונך להשתמש בהפצה מבוססת Arch, אנו ממליצים בדרך כלל על Arch Linux על פני כל אחת מהנגזרות שלו.

בנוסף, אנו ממליצים על **נגד** שתי נגזרות Arch אלו במיוחד:

- **Manjaro**: הפצה זו מעכבת חבילות למשך שבועיים כדי לוודא שהשינויים שלהן לא יישברו, לא כדי לוודא שהמעלה הזרם יציב. כאשר נעשה שימוש בחבילות AUR, הן בנויות לרוב על פי [ספריות](https://en.wikipedia.org/wiki/Library_(computing)) העדכניות ביותר מהמאגרים של Arch.
- **Garuda**: They use [Chaotic-AUR](https://aur.chaotic.cx) which automatically and blindly compiles packages from the AUR. אין תהליך אימות כדי לוודא שחבילות AUR אינן סובלות מהתקפות שרשרת האספקה.

### הפצות ליבה של לינוקס ו-"Libre"

We recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://phoronix.com/news/GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode.

### Mandatory access control

Mandatory access control is a set of additional security controls which help to confine parts of the system such as apps and system services. The two common forms of mandatory access control found in Linux distributions are [SELinux](https://github.com/SELinuxProject) and [AppArmor](https://apparmor.net). Fedora and Tumbleweed use SELinux by default, with Tumbleweed offering an option in its installer to choose AppArmor instead.

SELinux on [Fedora](https://docs.fedoraproject.org/en-US/quick-docs/selinux-getting-started) confines Linux containers, virtual machines, and service daemons by default. AppArmor is used by the snap daemon for [sandboxing](https://snapcraft.io/docs/security-sandboxing) snaps which have [strict](https://snapcraft.io/docs/snap-confinement) confinement such as [Firefox](https://snapcraft.io/firefox). There is a community effort to confine more parts of the system in Fedora with the [ConfinedUsers](https://fedoraproject.org/wiki/SIGs/ConfinedUsers) special interest group.

## המלצות כלליות

### הצפנת כונן

לרוב ההפצות של לינוקס יש אפשרות בתוך תוכנית ההתקנה שלה להפעלת [LUKS](../encryption.md#linux-unified-key-setup) FDE. If this option isn’t set at installation time, you will have to back up your data and re-install, as encryption is applied after [disk partitioning](https://en.wikipedia.org/wiki/Disk_partitioning), but before [file systems](https://en.wikipedia.org/wiki/File_system) are formatted. אנו מציעים גם למחוק בצורה מאובטחת את מכשיר האחסון שלך:

- [מחיקת נתונים מאובטחת :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure)

### החלף

שקול להשתמש ב-[ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) במקום קובץ החלפה או מחיצה מסורתיים כדי להימנע מכתיבת נתוני זיכרון שעלולים להיות רגישים לאחסון מתמשך ( ולשפר ביצועים). הפצות מבוססות פדורה [משתמשות ב-ZRAM כברירת מחדל](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

אם אתה זקוק לפונקציונליות של השהייה לדיסק (תרדמה), עדיין תצטרך להשתמש בקובץ החלפה או מחיצה מסורתיים. ודא שכל שטח החלפה שיש לך בהתקן אחסון קבוע [מוצפן](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) לכל הפחות כדי להפחית חלק מהאיומים הללו.

### קושחה קניינית (עדכוני מיקרוקוד)

חלק מההפצות של לינוקס (כגון [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre) מבוססות או הפצות עשה זאת בעצמך) אינן מגיעות עם קנייני [microcode](https://en.wikipedia.org/wiki/Microcode) עדכוני המתקן פרצות אבטחה קריטיות. Some notable examples of these vulnerabilities include [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), and other [hardware vulnerabilities](https://kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

אנו **ממליצים בחום** להתקין עדכוני מיקרוקוד, מכיוון שהם מכילים תיקוני אבטחה חשובים עבור ה-CPU אשר לא ניתן להפחית באופן מלא בתוכנה בלבד. Fedora and openSUSE both apply microcode updates by default.

### עדכונים

רוב ההפצות של לינוקס יתקינו עדכונים אוטומטית או יזכירו לך לעשות זאת. חשוב לשמור על מערכת ההפעלה שלך מעודכנת כדי שהתוכנה שלך תתוקן כאשר מתגלה פגיעות.

חלק מההפצות (במיוחד אלו המיועדות למשתמשים מתקדמים) הן עצמות יותר ומצפות ממך לעשות דברים בעצמך (למשל Arch או Debian). אלה ידרשו להפעיל את "מנהל החבילות" (`apt`, `pacman`, `dnf` וכו') באופן ידני על מנת לקבל עדכוני אבטחה חשובים.

בנוסף, הפצות מסוימות לא יוריד עדכוני קושחה באופן אוטומטי. For that, you will need to install [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

### Permission Controls

Desktop environments (DEs) that support the [Wayland](https://wayland.freedesktop.org) display protocol are [more secure](https://lwn.net/Articles/589147) than those that only support X11. However, not all DEs take full advantage of Wayland's architectural security improvements.

For example, GNOME has a notable edge in security compared to other DEs by implementing permission controls for third-party software that tries to [capture your screen](https://gitlab.gnome.org/GNOME/gnome-shell/-/issues/3943). That is, when a third-party application attempts to capture your screen, you are prompted for your permission to share your screen with the app.

<figure markdown>
  ![Screenshot permissions](../assets/img/linux/screenshot_permission.png){ width="450" }
  <figcaption>GNOME's screenshot permission dialog</figcaption>
</figure>

Many alternatives don't provide these same permission controls yet,[^1] while some are waiting for Wayland to implement these controls upstream.[^2]

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

[אפשרות](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) זו כבויה כעת כברירת מחדל. אנו ממליצים להוסיף את `countme=false` ל-`/etc/dnf/dnf.conf` למקרה שהוא יופעל בעתיד. On systems that use `rpm-ostree` such as Silverblue, the `countme` option is disabled by masking the [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems) timer.

openSUSE also uses a [unique ID](https://en.opensuse.org/openSUSE:Statistics) to count systems, which can be disabled by emptying the `/var/lib/zypp/AnonymousUniqueId` file.

[^1]: KDE currently has an open proposal to add controls for screen captures: <https://invent.kde.org/plasma/xdg-desktop-portal-kde/-/issues/7>
[^2]: Sway is waiting to add specific security controls until they "know how security as a whole is going to play out" in Wayland: <https://github.com/swaywm/sway/issues/5118#issuecomment-600054496>
