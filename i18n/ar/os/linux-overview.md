---
title: نظرة عامة على Linux
icon: simple/linux
description: نظام Linux هو نظام تشغيل مفتوح المصدر لأجهزة الكمبيوتر، يركز على الخصوصية، لكن ليست كل توزيعاته على نفس المستوى.
---

نظام **Linux** هو نظام تشغيل مفتوح المصدر لأجهزة الكمبيوتر، يركز على الخصوصية. مع انتشار تقنيات الـ telemetry وغيرها من التقنيات التي تنتهك الخصوصية في أنظمة التشغيل الشائعة، ظل Linux على أجهزة الكمبيوتر الخيار الواضح لمن يريدون التحكم الكامل في أجهزتهم من الأساس.

نستخدم مصطلح «Linux» في موقعنا عادةً للإشارة إلى توزيعات Linux المخصّصة** لأجهزة الكمبيوتر**. لا تتناول هذه الصفحة أنظمة التشغيل الأخرى التي تستخدم نواة Linux أيضا، مثل ChromeOS وAndroid وQubes OS.

[توصياتنا لتوزيعات Linux :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## ملاحظات أمنية

هناك بعض المخاطر الأمنية المهمة في Linux التي ينبغي أن تكون على دراية بها. رغم هذه العيوب، تظل توزيعات Linux المخصصة لأجهزة الكمبيوتر خيارا ممتازا لمعظم الأشخاص الذين يرغبون في:

- تجنب جمع بيانات telemetry الذي غالبا ما يصاحب أنظمة التشغيل مغلقة المصدر
- الحفاظ على [حرية استخدام البرمجيات والتحكم فيها](https://gnu.org/philosophy/free-sw.en.html#four-freedoms)
- استخدام أنظمة تركز على الخصوصية، مثل [Whonix](../desktop.md#whonix) أو [Tails](../desktop.md#tails)

### أمان البرمجيات مفتوحة المصدر

من [المفاهيم الخاطئة الشائعة](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) أن Linux وغيره من البرمجيات مفتوحة المصدر آمنة بطبيعتها لمجرد أن الشيفرة المصدرية (Source Code) متاحة للجميع. يعتقد البعض أن مجتمع المطورين يراجع الشيفرة المصدرية (Source Code) بانتظام، لكن هذا لا يحدث [.دائما](https://seirdy.one/posts/2022/02/02/floss-security).

في الواقع، يعتمد أمان توزيعة Linux على عدة عوامل، مثل مدى نشاط المشروع، وخبرة المطورين، ودقة مراجعة الكود، ومدى الاهتمام بأجزاء معينة من الكود قد تمر سنوات دون مراجعتها أو تعديلها.

### ميزات الأمان المفقودة

حاليا، يتأخر Linux على [أجهزة الكمبيوتر المكتبية (Desktop)](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) عن بدائل مثل macOS وAndroid في بعض ميزات الأمان. نأمل أن نرى تحسينات في هذه الجوانب مستقبلا.

- ميزة الـ **Verified Boot** على Linux ليست بقوة البدائل مثل [Secure Boot](https://support.apple.com/guide/security/secac71d5623/web) من Apple أو [Verified Boot](https://source.android.com/security/verifiedboot) من Android. تمنع ميزة الـ Verified Boot البرمجيات الخبيثة من إجراء تعديلات دائمة على النظام، وتحمي من هجمات [Evil Maid](https://en.wikipedia.org/wiki/Evil_Maid_attack)، لكنها [لا تزال غير متاحة على نطاق واسع](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3)، حتى في أكثر توزيعات Linux تطورا.

- يفتقر Linux بشدة إلى **عزل قوي للتطبيقات (sandboxing)**، حتى مع التطبيقات التي تعمل داخل حاويات مثل Flatpaks، أو حلول العزل مثل Firejail. يُعد Flatpak حتى الآن أكثر أدوات العزل (sandboxing) الواعدة على Linux، لكنه لا يزال يعاني من أوجه قصور عديدة، ويسمح [بإعدادات افتراضية](https://flatkill.org/2020) غير آمنة تُمكّن معظم التطبيقات من تجاوز العزل بسهولة.

بالإضافة إلى ذلك، يتأخر Linux في تطبيق [وسائل الحماية من استغلال الثغرات الأمنية](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations)، التي أصبحت أساسية في أنظمة التشغيل الأخرى، مثل Arbitrary Code Guard في Windows وHardened Runtime في macOS. كذلك، فإن معظم برامج Linux ونظام Linux نفسه مكتوبة بلغات برمجة لا تضمن سلامة الذاكرة. تُعد أخطاء تلف الذاكرة (Memory Corruption) السبب وراء [معظم الثغرات الأمنية](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code) التي تم إصلاحها وتخصيص معرّف CVE لها. ورغم أن هذا ينطبق أيضا على Windows وmacOS، فإنهما يحرزان تقدمًا سريعًا في استخدام لغات برمجة تضمن سلامة الذاكرة، مثل Rust في Windows وSwift في macOS.

## اختيار توزيعة Linux المناسبة لك

ليست كل توزيعات Linux على نفس المستوى. صفحتنا التي [نوصي](../desktop.md) فيها بتوزيعات Linux ليست مرجعا نهائيا لتحديد التوزيعة التي يجب عليك استخدامها، لكن توصياتنا *تستند* إلى الإرشادات التالية. إليك بعض الأمور التي يجب مراعاتها عند اختيار توزيعة Linux:

### دورة إصدار التحديثات

نوصي بشدة باختيار توزيعات توفر الإصدارات المستقرة من البرامج الأصلية فور توفرها تقريبا، وتُعرف غالبا باسم توزيعات الإصدار المتجدد (Rolling Release). ويرجع ذلك إلى أن التوزيعات ذات دورة الإصدارات الثابتة (release cycle distribution) غالبا لا تُحدّث إصدارات حزم (package) البرامج، مما يجعلها تتأخر في توفير التحديثات الأمنية.

في التوزيعات ذات الإصدارات الثابتة مثل [Debian](https://debian.org/security/faq#handling)، يُتوقع من مسؤولي صيانة حزم البرامج (package maintainers) نقل الإصلاحات الأمنية من الإصدارات الأحدث إلى الإصدارات القديمة لإصلاح الثغرات، بدلا من تحديث البرامج إلى «الإصدار التالي» الذي يصدره المطور الأصلي. بعض الإصلاحات الأمنية (خاصة للبرامج الأقل شيوعا) [لا تحصل](https://arxiv.org/abs/2105.14565) على [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) من الأساس، ولذلك لا تصل هذه الإصلاحات إلى التوزيعة عند الاعتماد على هذا الأسلوب في تحديث البرامج. ونتيجة لذلك، قد تتأخر بعض الإصلاحات الأمنية البسيطة حتى صدور الإصدار الرئيسي التالي.

لا نرى أن الإبقاء على الإصدارات القديمة من حزم البرامج وتطبيق إصلاحات مؤقتة عليها فكرة جيدة، لأن ذلك قد يجعل البرامج تعمل بطريقة تختلف عما قصده مطوّروها. لدى [Richard Brown](https://rootco.de/aboutme) عرض تقديمي حول هذا الموضوع:

- [الإصدارات الدورية (Regular Releases) خيار خاطئ](https://youtu.be/i8c0mg_mS7U)، اعتمد على الإصدارات المتجددة <small>(YouTube)</small>

### التحديثات التقليدية مقابل التحديثات التي تُطبَّق كوحدة واحدة

تقليديا، تُحدث توزيعات Linux حزم البرامج المطلوبة واحدة تلو الأخرى. قد تكون التحديثات التقليدية، مثل تلك المستخدمة في Fedora وArch Linux والتوزيعات المبنية على Debian، أقل موثوقية إذا حدث خطأ أثناء التحديث.

أما التوزيعات التي تستخدم التحديثات التي تُطبّق كوحدة واحدة، فتُطبّق التحديثات بالكامل أو لا تُطبقها إطلاقا. في التوزيعات التي تُطبّق التحديثات كوحدة واحدة، إذا حدث خطأ أثناء التحديث (مثل انقطاع الكهرباء)، فلن يتغير أي شيء في النظام.

تساعد هذه الطريقة في تطبيق التحديثات على جعل النظام أكثر موثوقية، وتستخدمها [توزيعات](../desktop.md#atomic-distributions) مثل Silverblue وNixOS. [Adam Šamalík](https://twitter.com/adsamalik) provides a presentation on how `rpm-ostree` works with Silverblue:

- [لنجرب Fedora Silverblue — نظام تشغيل لأجهزة الكمبيوتر لا يمكن تعديل ملفاته الأساسية! - Adam Šamalík](https://youtu.be/-hpV5l-gJnQ) <small>(YouTube)</small>

### التوزيعات «التي تركز على الأمان»

غالبا ما يحدث خلط بين التوزيعات «التي تركز على الأمان» والتوزيعات المخصصة لاختبار الاختراق. غالبًا ما يُظهر البحث السريع عن «أكثر توزيعات Linux أمانًا» نتائج مثل Kali Linux وBlack Arch وParrot OS. These distributions are offensive penetration testing distributions that bundle tools for testing other systems. They don’t include any “extra security” or defensive mitigations intended for regular use.

### Arch-based distributions

Arch and Arch-based distributions are not recommended for those new to Linux (regardless of distribution) as they require regular [system maintenance](https://wiki.archlinux.org/title/System_maintenance). Arch does not have a distribution update mechanism for the underlying software choices. As a result you have to stay aware with current trends and adopt technologies on your own as they supersede older practices.

For a secure system, you are also expected to have sufficient Linux knowledge to properly set up security for their system such as adopting a [mandatory access control](#mandatory-access-control) system, setting up [kernel module](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) blacklists, hardening boot parameters, manipulating [sysctl](https://en.wikipedia.org/wiki/Sysctl) parameters, and knowing what components they need such as [Polkit](https://en.wikipedia.org/wiki/Polkit).

Arch-based derivatives designed to make Arch "easier to use" are not recommended, as they frequently encourage poor security practices while weakening the base system. These practices include bundling outdated packages in downstream repositories that are updated less frequently than Arch's official channels. Furthermore, these distributions usually fail to properly educate users on the risks associated with the Arch User Repository (AUR).

Anyone using the [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **must** be comfortable auditing PKGBUILDs (the recipes that build packages) that they download from that service. AUR packages are community-produced content and are not vetted in any way, and therefore are vulnerable to software [:material-package-variant-closed-remove: Supply Chain Attacks](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}, which has in fact happened [in the past](https://bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository) and more recently when [1500 packages](https://discuss.privacyguides.net/t/around-1-500-aur-packages-compromised-with-rootkit-like-malware/38517) were compromised.

The AUR should always be used sparingly, and often there is a lot of bad advice on various pages which direct people to blindly use [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) without sufficient warning. Similar warnings apply to the use of third-party Personal Package Archives (PPAs) on Debian-based distributions or Community Projects (COPR) on Fedora.

If you are experienced with Linux and wish to use an Arch-based distribution, mainline Arch Linux is the **only** recommended option.

### Linux-libre kernel and “Libre” distributions

We recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://phoronix.com/news/GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode.

### Mandatory access control

Mandatory access control is a set of additional security controls which help to confine parts of the system such as apps and system services. The two common forms of mandatory access control found in Linux distributions are [SELinux](https://github.com/SELinuxProject) and [AppArmor](https://apparmor.net). Fedora and Tumbleweed use SELinux by default, with Tumbleweed offering an option in its installer to choose AppArmor instead.

SELinux on [Fedora](https://docs.fedoraproject.org/en-US/quick-docs/selinux-getting-started) confines Linux containers, virtual machines, and service daemons by default. AppArmor is used by the snap daemon for [sandboxing](https://snapcraft.io/docs/security-sandboxing) snaps which have [strict](https://snapcraft.io/docs/snap-confinement) confinement such as [Firefox](https://snapcraft.io/firefox). There is a community effort to confine more parts of the system in Fedora with the [ConfinedUsers](https://fedoraproject.org/wiki/SIGs/ConfinedUsers) special interest group.

## General Recommendations

### Drive Encryption

Most Linux distributions have an option within its installer for enabling [LUKS](../encryption.md#linux-unified-key-setup) FDE. If this option isn’t set at installation time, you will have to back up your data and re-install, as encryption is applied after [disk partitioning](https://en.wikipedia.org/wiki/Disk_partitioning), but before [file systems](https://en.wikipedia.org/wiki/File_system) are formatted. We also suggest securely erasing your storage device:

- [Secure Data Erasure :material-arrow-right-drop-circle:](https://www.privacyguides.org/articles/2022/05/25/secure-data-erasure/)

### Swap

Consider using [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) instead of a traditional swap file or partition to avoid writing potentially sensitive memory data to persistent storage (and improve performance). Fedora-based distributions [use ZRAM by default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

If you require suspend-to-disk (hibernation) functionality, you will still need to use a traditional swap file or partition. Make sure that any swap space you do have on a persistent storage device is [encrypted](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) at a minimum to mitigate some of these threats.

### Proprietary Firmware (Microcode Updates)

Some Linux distributions (such as [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)-based or DIY distros) don’t come with the proprietary [microcode](https://en.wikipedia.org/wiki/Microcode) updates which patch critical security vulnerabilities. Some notable examples of these vulnerabilities include [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), and other [hardware vulnerabilities](https://kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

We **highly recommend** that you install microcode updates, as they contain important security patches for the CPU which can not be fully mitigated in software alone. Fedora and openSUSE both apply microcode updates by default.

### Updates

Most Linux distributions will automatically install updates or remind you to do so. It is important to keep your OS up to date so that your software is patched when a vulnerability is found.

Some distributions (particularly those aimed at advanced users) are more bare bones and expect you to do things yourself (e.g. Arch or Debian). These will require running the "package manager" (`apt`, `pacman`, `dnf`, etc.) manually in order to receive important security updates.

Additionally, some distributions will not download firmware updates automatically. For that, you will need to install [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

### Permission Controls

Desktop environments that support the [Wayland](https://wayland.freedesktop.org) display protocol are [more secure](https://lwn.net/Articles/589147) than those that only support X11. Moreover, we *generally* recommend installing and using applications which are sandboxed such as those obtained via **Flatpak**. Flatpak supports the [`security-context-v1`](https://github.com/flatpak/flatpak/pull/4920) protocol and the ability to filter D-Bus protocols, which allow Flatpak to properly identify apps for the purpose of sandboxing them through permission controls.[^1] Conversely, applications outside sandboxes are free to perform privileged actions such as capturing your screen, either by [overwriting the portal permission store](https://invent.kde.org/plasma/xdg-desktop-portal-kde/-/issues/7#note_1112260), or [making use of privileged Wayland protocols](https://github.com/swaywm/sway/pull/7648#issuecomment-2507730794).

## Privacy Tweaks

### MAC Address Randomization

Many desktop Linux distributions (Fedora, openSUSE, etc.) come with [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) to configure Ethernet and Wi-Fi settings.

It is possible to randomize the [MAC address](https://en.wikipedia.org/wiki/MAC_address) when using NetworkManager. This provides a bit more privacy on Wi-Fi networks as it makes it harder to track specific devices on the network you’re connected to. It does [**not**](https://papers.mathyvanhoef.com/wisec2016.pdf) make you anonymous.

In the terminal, create a new file `/etc/NetworkManager/conf.d/00-macrandomize.conf` and add the following to it:

```text
[device]
wifi.scan-rand-mac-address=yes

[connection]
wifi.cloned-mac-address=random
ethernet.cloned-mac-address=random
```

Then, restart NetworkManager:

```sh
systemctl restart NetworkManager
```

Optionally, changing the connection parameter from `random` to `stable` will give you a random MAC address *per network*, but keep it stable for that network when you reconnect to it later. Using `random` will give you a random MAC address *per connection*. This may be desirable for networks with captive portals or where you have a static DHCP assignment, at the expense of making you more identifiable by a single network operator you connect to multiple times.

If you are using [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), you will need to set [`MACAddressPolicy=random`](https://freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) which will enable [RFC 7844 (Anonymity Profiles for DHCP Clients)](https://freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

MAC address randomization is primarily beneficial for Wi-Fi connections. For Ethernet connections, randomizing your MAC address provides little (if any) benefit, because a network administrator can trivially identify your device by other means (such as inspecting the port you are connected to on the network switch). Randomizing Wi-Fi MAC addresses depends on support from the Wi-Fi’s firmware.

### Other Identifiers

There are other system identifiers which you may wish to be careful about. You should give this some thought to see if it applies to your [threat model](../basics/threat-modeling.md):

- **Hostnames:** Your system's hostname is shared with the networks you connect to. You should avoid including identifying terms like your name or operating system in your hostname, instead sticking to generic terms or random strings.
- **Usernames:** Similarly, your username is used in a variety of ways across your system. Consider using generic terms like "user" rather than your actual name.

### System Counting

The Fedora Project [counts](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) how many unique systems access its mirrors by using a [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) variable instead of a unique ID. Fedora does this to determine load and provision better servers for updates where necessary.

This [option](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) is currently off by default. We recommend adding `countme=false` to `/etc/dnf/dnf.conf` just in case it is enabled in the future. On systems that use `rpm-ostree` such as Silverblue, the `countme` option is disabled by masking the [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems) timer.

openSUSE also uses a [unique ID](https://en.opensuse.org/openSUSE:Statistics) to count systems, which can be disabled by emptying the `/var/lib/zypp/AnonymousUniqueId` file.

[^1]: This exposes a reliable way for Wayland compositors to get identifying information about a client. Compositors can then apply security policies if desirable. [https://github.com/flatpak/flatpak/commit/f0e626a4b60439f211f06d35df74b675a9ef42f4](https://github.com/flatpak/flatpak/commit/f0e626a4b60439f211f06d35df74b675a9ef42f4)
