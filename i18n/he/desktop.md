---
title: "שולחן עבודה/מחשב אישי"
icon: simple/linux
description: הפצות לינוקס מומלצות בדרך כלל להגנה על פרטיות וחופש תוכנה.
cover: desktop.webp
---

הפצות לינוקס מומלצות בדרך כלל להגנה על פרטיות וחופש תוכנה. אם אינך משתמש עדיין בלינוקס, להלן כמה הפצות שאנו מציעים לנסות, כמו גם כמה טיפים כלליים לשיפור פרטיות ואבטחה החלים על הפצות לינוקס רבות.

- [סקירה כללית של לינוקס :material-arrow-right-drop-circle:](os/linux-overview.md)

## הפצות מסורתיות

### Fedora Workstation

<div class="admonition recommendation" markdown>

![Fedora לוגו](assets/img/linux-desktop/fedora-workstation.svg){ align=right }

**תחנת העבודה של פדורה** היא ההפצה המומלצת שלנו לאנשים חדשים ללינוקס. Fedora בדרך כלל מאמצת טכנולוגיות חדשות יותר לפני הפצות אחרות, למשל [Wayland](https://wayland.freedesktop.org/), [PipeWire](https://pipewire.org), ובקרוב [FS-Verity](https://fedoraproject.org/wiki/Changes/FsVerityRPM). טכנולוגיות חדשות אלה מגיעות לעתים קרובות עם שיפורים באבטחה, בפרטיות ובשימושיות באופן כללי.

[:octicons-home-16: דף הבית](https://fedoraproject.org/workstation/){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=תיעוד}
[:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=לתרומה }

</details>

</div>

לFedora יש מהדורת שחרור מתגלגל-למחצה. בעוד כמה חבילות כמו [GNOME](https://www.gnome.org) מוקפאות עד לשחרור הבא של פדורה, רוב החבילות (כולל הקרנל) מתעדכנות לעתים קרובות לאורך תוחלת החיים של השחרור. כל גרסה של פדורה נתמכת למשך שנה אחת, עם גרסה חדשה ששוחררה כל שישה חודשים.

### openSUSE Tumbleweed

<div class="admonition recommendation" markdown>

![openSUSE Tumbleweed לוגו](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }

**openSUSE Tumbleweed** היא הפצת שחרור מתגלגלת יציבה.

ל-openSUSE Tumblewee יש a [transactional update](https://kubic.opensuse.org/blog/2018-04-04-transactionalupdates/) יש מערכת המשתמשת [Btrfs](https://en.wikipedia.org/wiki/Btrfs) ו [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) כדי להבטיח שניתן יהיה להחזיר תמונות אם תהיה בעיה.

[:octicons-home-16: Homepage](https://get.opensuse.org/tumbleweed/){ .md-button .md-button--primary }
[:octicons-info-16:](https://doc.opensuse.org/){ .card-link title=Documentation}
[:octicons-heart-16:](https://shop.opensuse.org/){ .card-link title=Contribute }

</details>

</div>

Tumbleweed עוקב אחר מודל מהדורה מתגלגל שבו כל עדכון משוחרר כתמונת מצב של ההפצה. בעת שדרוג המערכת, מתבצעת הורדה של תמונת מצב חדשה. כל תמונת מצב מנוהלת באמצעות סדרה של בדיקות אוטומטיות על ידי [openQA](https://openqa.opensuse.org) כדי להבטיח את איכותה.

### Arch Linux

<div class="admonition recommendation" markdown>

![Arch לוגו](assets/img/linux-desktop/archlinux.svg){ align=right }

**Arch Linux** הוא הפצה קלה של עשה זאת בעצמך (DIY) שמשמעותה שאתה מקבל רק את מה שאתה מתקין. לקבלת מידע נוסף, עיין ב[FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions).

[:octicons-home-16: Homepage](https://archlinux.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.archlinux.org/){ .card-link title=Documentation}
[:octicons-heart-16:](https://archlinux.org/donate/){ .card-link title=Contribute }

</details>

</div>

ל - Arch Linux יש מחזור שחרור מתגלגל. אין לוח זמנים שחרור קבוע וחבילות מתעדכנות לעתים קרובות מאוד.

להיות התפלגות DIY, אתה [צפוי להגדיר ולתחזק](os/linux-overview.md#arch-based-distributions) המערכת שלך בעצמך. יש Arch [מתקין רשמי](https://wiki.archlinux.org/title/Archinstall) כדי להפוך את תהליך ההתקנה קצת יותר קל.

חלק גדול מהחבילות של [ארץ' לינוקס](https://reproducible.archlinux.org) הן [לשחזור](https://reproducible-builds.org).

## הפצות בלתי ניתנות לשינוי

### Fedora Atomic Desktops

<div class="admonition recommendation" markdown>

![Fedora logo](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Atomic Desktops** are the immutable variants of Fedora with a strong focus on containerized workflows and Flatpak for desktop applications. All of these variants follow the same release schedule as Fedora Workstation, benefiting from the same fast updates and staying very close to upstream.

[:octicons-home-16: Homepage](https://fedoraproject.org/atomic-desktops/){ .md-button .md-button--primary }
[:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribute }

</details>

</div>

The [Fedora Atomic Desktops](https://fedoramagazine.org/introducing-fedora-atomic-desktops/) come in a variety of flavors depending on the desktop environment you prefer, such as **Fedora Silverblue** (which comes with [GNOME](https://www.gnome.org/)), **Fedora Kinoite**, (which comes with [KDE](https://kde.org/)), **Fedora Sway Atomic**, or **Fedora Budgie Atomic**. However, we don't recommend the last of these as the Budgie desktop environment [still requires X11](https://buddiesofbudgie.org/blog/wayland).

These operating systems differ from Fedora Workstation as they replace the [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf/) package manager with a much more advanced alternative called [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/package-management/rpm-ostree/). The `rpm-ostree` package manager works by downloading a base image for the system, then overlaying packages over it in a [git](https://en.wikipedia.org/wiki/Git)-like commit tree. When the system is updated, a new base image is downloaded and the overlays will be applied to that new image.

After the update is complete you will reboot the system into the new deployment. `rpm-ostree` keeps two deployments of the system so that you can easily rollback if something breaks in the new deployment. There is also the option to pin more deployments as needed.

[Flatpak](https://www.flatpak.org) is the primary package installation method on these distributions, as `rpm-ostree` is only meant to overlay packages that cannot stay inside of a container on top of the base image.

As an alternative to Flatpaks, there is the option of [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox/) to create [Podman](https://podman.io) containers with a shared home directory with the host operating system and mimic a traditional Fedora environment, which is a [useful feature](https://containertoolbx.org) for the discerning developer.

### NixOS

<div class="admonition recommendation" markdown>

![NixOS logo](assets/img/linux-desktop/nixos.svg){ align=right }

NixOS היא הפצה עצמאית המבוססת על מנהל החבילות של Nix ומתמקדת בשחזור ואמינות.

[:octicons-home-16: Homepage](https://nixos.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=Documentation}
[:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=Contribute }

</details>

</div>

NixOS’s package manager keeps every version of every package in a different folder in the **Nix store**. Due to this you can have different versions of the same package installed on your system. After the package contents have been written to the folder, the folder is made read-only.

NixOS also provides atomic updates; first it downloads (or builds) the packages and files for the new system generation and then switches to it. There are different ways to switch to a new generation; you can tell NixOS to activate it after reboot or you can switch to it at runtime. You can also *test* the new generation by switching to it at runtime, but not setting it as the current system generation. If something in the update process breaks, you can just reboot and automatically and return to a working version of your system.

Nix the package manager uses a purely functional language - which is also called Nix - to define packages.

[Nixpkgs](https://github.com/nixos/nixpkgs) (the main source of packages) are contained in a single GitHub repository. You can also define your own packages in the same language and then easily include them in your config.

Nix is a source-based package manager; if there’s no pre-built available in the binary cache, Nix will just build the package from source using its definition. It builds each package in a sandboxed *pure* environment, which is as independent of the host system as possible, thus making binaries reproducible.

## הפצות ממוקדות אנונימיות

### Whonix

<div class="admonition recommendation" markdown>

![Whonix לוגו](assets/img/linux-desktop/whonix.svg){ align=right }

**Whonix** מבוסס על [Kicksecure](#kicksecure), נגזר ממוקד אבטחה של דביאן. מטרתו לספק פרטיות, אבטחה ואנונימיות באינטרנט. כדאי להשתמש ב - Whonix בשילוב עם [Qubes OS](# qubes- os).

[:octicons-home-16: Homepage](https://www.whonix.org/){ .md-button .md-button--primary }
[:simple-torbrowser:](http://www.dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://www.whonix.org/wiki/Documentation){ .card-link title=Documentation}
[:octicons-heart-16:](https://www.whonix.org/wiki/Donate){ .card-link title=Contribute }

</details>

</div>

Whonix is meant to run as two virtual machines: a “Workstation” and a Tor “Gateway.” All communications from the Workstation must go through the Tor gateway. This means that even if the Workstation is compromised by malware of some kind, the true IP address remains hidden.

Some of its features include Tor Stream Isolation, [keystroke anonymization](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak), [encrypted swap](https://github.com/Whonix/swap-file-creator), and a hardened memory allocator. Future versions of Whonix will likely include [full system AppArmor policies](https://github.com/Whonix/apparmor-profile-everything) and a [sandbox app launcher](https://www.whonix.org/wiki/Sandbox-app-launcher) to fully confine all processes on the system.

Whonix is best used [in conjunction with Qubes](https://www.whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers). We have a [recommended guide](os/qubes-overview.md#connecting-to-tor-via-a-vpn) on configuring Whonix in conjunction with a VPN ProxyVM in Qubes to hide your Tor activities from your ISP.

### Tails

<div class="admonition recommendation" markdown>

![Tails לוגו](assets/img/linux-desktop/tails.svg){ align=right }

**Tails** היא מערכת הפעלה חיה המבוססת על דביאן המנתבת את כל התקשורת דרך Tor, שיכולה לאתחל כמעט כל מחשב מ - DVD, מקל USB או התקנת כרטיס SD. הוא משתמש ב - [Tor](tor.md) כדי לשמור על פרטיות ואנונימיות תוך עקיפת הצנזורה, והוא אינו מותיר עקבות של עצמו במחשב שבו הוא נמצא בשימוש לאחר שהוא כבוי.

[:octicons-home-16: Homepage](https://tails.boum.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://tails.boum.org/doc/index.en.html){ .card-link title=Documentation}
[:octicons-heart-16:](https://tails.boum.org/donate/){ .card-link title=Contribute }

</details>

</div>

Tails is great for counter forensics due to amnesia (meaning nothing is written to the disk); however, it is not a hardened distribution like Whonix. It lacks many anonymity and security features that Whonix has and gets updated much less often (only once every six weeks). A Tails system that is compromised by malware may potentially bypass the transparent proxy allowing for the user to be deanonymized.

Tails includes [uBlock Origin](desktop-browsers.md#ublock-origin) in Tor Browser by default, which may potentially make it easier for adversaries to fingerprint Tails users. [Whonix](desktop.md#whonix) virtual machines may be more leak-proof, however they are not amnesic, meaning data may be recovered from your storage device.

By design, Tails is meant to completely reset itself after each reboot. Encrypted [persistent storage](https://tails.boum.org/doc/persistent_storage/index.en.html) can be configured to store some data between reboots.

## הפצות ממוקדות אבטחה

### Qubes OS

<div class="admonition recommendation" markdown>

![Qubes OS לוגו](assets/img/qubes/qubes_os.svg){ align=right }

**Qubes OS** היא מערכת הפעלה בקוד פתוח שנועדה לספק אבטחה חזקה עבור מחשוב שולחני באמצעות מכונות וירטואליות מאובטחות (או "qubes"). Qubes מבוסס על Xen, מערכת חלונות X ו- Linux. זה יכול להריץ את רוב יישומי לינוקס ולהשתמש ברוב מנהלי ההתקנים של לינוקס.

[:octicons-home-16: דף הבית](https://www.qubes-os.org/){ .md-button .md-button--primary }
[:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://www.qubes-os.org/privacy/){ .card-link title="מדיניות פרטיות" }
[:octicons-info-16:](https://www.qubes-os.org/doc/){ .card-link title=תיעוד }
[:octicons-code-16:](https://github.com/QubesOS/){ .card-link title="קוד מקור" }
[:octicons-heart-16:](https://www.qubes-os.org/donate/){ .card-link title=לתרומה }

</details>

</div>

Qubes OS secures the computer by isolating subsystems (e.g., networking, USB, etc.) and applications in separate *qubes*. Should one part of the system be compromised, the extra isolation is likely to protect the rest of the *qubes* and the core system.

For further information about how Qubes works, read our full [Qubes OS overview](os/qubes-overview.md) page.

### Kicksecure

While we [recommend against](os/linux-overview.md#release-cycle) "perpetually outdated" distributions like Debian for Desktop use in most cases, Kicksecure is a Debian-based operating system which has been hardened to be much more than a typical Linux install.

<div class="admonition recommendation" markdown>

![Kicksecure לוגו](assets/img/linux-desktop/kicksecure.svg){ align=right }

**Kicksecure** - במונחים פשוטים מדי - היא קבוצה של סקריפטים, תצורות וחבילות שמצמצמות באופן משמעותי את משטח ההתקפה של דביאן. זה מכסה הרבה המלצות לפרטיות והקשחה כברירת מחדל. הוא משמש גם כמערכת ההפעלה הבסיסית עבור [Whonix](#whonix).

[:octicons-home-16: דף הבית](https://www.kicksecure.com/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.kicksecure.com/wiki/Privacy_Policy){ .card-link title="מדיניות פרטיות" }
[:octicons-info-16:](https://www.kicksecure.com/wiki/Documentation){ .card-link title=תיעוד }
[:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="קוד מקור" }
[:octicons-heart-16:](https://www.kicksecure.com/wiki/Donate){ .card-link title=לתרומה }

</details>

</div>

## קריטריונים

Choosing a Linux distro that is right for you will come down to a huge variety of personal preferences, and this page is **not** meant to be an exhaustive list of every viable distribution. Our Linux overview page has some advice on [choosing a distro](os/linux-overview.md#choosing-your-distribution) in more detail. The distros on *this* page do all generally follow the guidelines we covered there, and all meet these standards:

- Free and open source.
- מקבל עדכוני תוכנה וליבה קבועים.
- [נמנע מ-X11](os/linux-overview.md#wayland).
    - החריג הבולט כאן הוא Qubes, אבל בעיות הבידוד שיש ל-X11 בדרך כלל נמנעות על ידי וירטואליזציה. בידוד זה חל רק על אפליקציות * פועל ב- qubes שונים * (מכונות וירטואליות), אפליקציות הפועלות ב- * אותם * qube הם לא מוגנים זה מזה.
- תומך בהצפנת דיסק מלא במהלך ההתקנה.
- לא מקפיא מהדורות רגילות במשך יותר משנה.
    - אנו [ממליצים נגד](os/linux-overview.md#release-cycle) הפצות "תמיכה לטווח ארוך" או "יציבות" לשימוש בשולחן העבודה.
- תומך במגוון רחב של חומרה.
- העדפה לפרויקטים גדולים יותר.
    - שמירה על מערכת הפעלה היא אתגר מרכזי, ולפרויקטים קטנים יותר יש נטייה לטעויות נמנעות יותר, או לעכב עדכונים קריטיים (או גרוע מכך, להיעלם לחלוטין). אנו נשענים לעבר פרויקטים אשר ככל הנראה יהיו בערך 10 שנים מהיום (בין אם זה נובע מגיבוי תאגידי או תמיכה קהילתית משמעותית מאוד), והרחק מפרויקטים שנבנו בעבודת יד או שיש להם מספר מצומצם של מתחזקים.

In addition, [our standard criteria](about/criteria.md) for recommended projects still applies. **Please note we are not affiliated with any of the projects we recommend.**
