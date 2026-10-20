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

تساعد هذه الطريقة في تطبيق التحديثات على جعل النظام أكثر موثوقية، وتستخدمها [توزيعات](../desktop.md#atomic-distributions) مثل Silverblue وNixOS. يقدّم [Adam Šamalík](https://www.linkedin.com/in/adamsamalik/) عرضًا يشرح فيه كيفية عمل `rpm-ostree` مع Silverblue:

- [لنجرب Fedora Silverblue — نظام تشغيل لأجهزة الكمبيوتر لا يمكن تعديل ملفاته الأساسية! - Adam Šamalík](https://youtu.be/-hpV5l-gJnQ) <small>(YouTube)</small>

### التوزيعات «التي تركز على الأمان»

غالبا ما يحدث خلط بين التوزيعات «التي تركز على الأمان» والتوزيعات المخصصة لاختبار الاختراق. غالبًا ما يُظهر البحث السريع عن «أكثر توزيعات Linux أمانًا» نتائج مثل Kali Linux وBlack Arch وParrot OS. هذه التوزيعات مخصصة لاختبار الاختراق الهجومي، وتأتي مع مجموعة من الأدوات لاختبار أمان الأنظمة الأخرى. لا توفر هذه التوزيعات أي ميزات أمان إضافية أو وسائل حماية مخصصة للاستخدام اليومي.

### التوزيعات المبنية على Arch

لا نوصي بتوزيعة Arch أو التوزيعات المبنية عليها للمستخدمين الجدد في Linux، مهما كانت التوزيعة التي استخدموها سابقًا، لأنها تتطلب [صيانة دورية للنظام](https://wiki.archlinux.org/title/System_maintenance). لا توفر Arch آلية لتحديث البرامج الأساسية التي تعتمد عليها التوزيعة. ونتيجة لذلك، عليك متابعة أحدث التطورات بنفسك واستخدام التقنيات الجديدة عندما تحل محل الطرق القديمة.

وللحصول على نظام آمن، يُتوقع منك أيضا أن تكون لديك معرفة كافية بنظام Linux لضبط إعدادات الأمان بشكل صحيح، مثل استخدام نظام [للتحكم الإلزامي في الوصول (Mandatory Access Control)](#mandatory-access-control)، وإعداد قوائم لحظر بعض [وحدات النواة (Kernel Modules)](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security)، وتعزيز أمان إعدادات الإقلاع، وتعديل إعدادات [sysctl](https://en.wikipedia.org/wiki/Sysctl)، ومعرفة المكونات التي يحتاجها نظامك، مثل [Polkit](https://en.wikipedia.org/wiki/Polkit).

لا نوصي بالتوزيعات المبنية على Arch والمصممة لجعلها «أسهل في الاستخدام»، لأنها غالبًا ما تشجع على اتباع ممارسات أمنية غير جيدة، وتُضعف أمان النظام الأساسي. تشمل هذه الممارسات توفير حزم برامج قديمة في مستودعات (repositories) تابعة لهذه التوزيعات، لا تُحدث بنفس وتيرة مستودعات Arch الرسمية. بالإضافة إلى ذلك، غالبا ما لا توضح هذه التوزيعات للمستخدمين بشكل كاف المخاطر المرتبطة بمستودع مستخدمي Arch (AUR).

يجب أن يكون أي شخص يستخدم مستودع مستخدمي [Arch (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **قادرًا** على مراجعة ملفات PKGBUILD (وهي الملفات التي تحتوي على تعليمات بناء حزم البرامج) التي ينزّلها من هذا المستودع. حزم AUR يُنشئها أفراد المجتمع، ولا تخضع لأي مراجعة أو تدقيق، ولذلك فهي عرضة لهجمات [سلسلة توريد البرمجيات (Supply Chain Attacks):material-package-variant-closed-remove:](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}، وقد حدثت هذه الهجمات بالفعل في [الماضي](https://bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository)، ومؤخرًا عندما [تعرضت 1500 حزمة للاختراق](https://discuss.privacyguides.net/t/around-1-500-aur-packages-compromised-with-rootkit-like-malware/38517).

يجب دائمًا استخدام AUR عند الضرورة فقط، فكثيرًا ما تنشر مواقع مختلفة نصائح سيئة تشجع المستخدمين على استخدام أدوات [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) دون التحقق منها، ودون تحذيرهم بشكل كافٍ من المخاطر. تنطبق التحذيرات نفسها على استخدام مستودعات PPA التابعة لجهات خارجية في التوزيعات المبنية على Debian، أو مستودعات المشاريع المجتمعية (COPR) في Fedora.

إذا كانت لديك خبرة في استخدام Linux وترغب في استخدام توزيعة مبنية على Arch، فإن توزيعة Arch Linux الأصلية هي الخيار **الوحيد** الذي نوصي به.

### نواة Linux-libre وتوزيعات «Libre» الحرة

لا **نوصي** باستخدام نواة Linux-libre، لأنها تزيل بعض وسائل الحماية من [استغلال الثغرات الأمنية](https://phoronix.com/news/GNU-Linux-Libre-5.7-Released)، وتمنع ظهور [تحذيرات النواة](https://news.ycombinator.com/item?id=29674846) بشأن وجود ثغرات أمنية في التعليمات البرمجية الدقيقة (microcode).

### التحكم الإلزامي في الوصول

التحكم الإلزامي في الوصول هو مجموعة من وسائل الحماية الإضافية التي تساعد على تقييد صلاحيات أجزاء من النظام، مثل التطبيقات وخدمات النظام. أشهر نظامين للتحكم الإلزامي (mandatory access control) في الوصول في توزيعات Linux هما [SELinux](https://github.com/SELinuxProject) [وAppArmor](https://apparmor.net). تستخدم توزيعتا Fedora وTumbleweed نظام SELinux افتراضيا، لكن Tumbleweed تتيح لك اختيار AppArmor بدلا منه أثناء التثبيت.

يفرض SELinux في [Fedora](https://docs.fedoraproject.org/en-US/quick-docs/selinux-getting-started) قيودا على الـ Linux Containers والأجهزة الافتراضية (virtual machines) والـ service daemons التي تعمل في الخلفية بشكل افتراضي. تستخدم خدمة snap نظام AppArmor [لعزل](https://snapcraft.io/docs/security-sandboxing) حزم snap التي تخضع لقيود [صارمة](https://snapcraft.io/docs/snap-confinement)، مثل [Firefox](https://snapcraft.io/firefox). تعمل مجموعة [ConfinedUsers](https://fedoraproject.org/wiki/SIGs/ConfinedUsers) في مجتمع Fedora على وضع قيود أمنية على أجزاء أكثر من النظام.

## توصيات عامة

### تشفير القرص

تتيح معظم توزيعات Linux خيار تفعيل تشفير القرص بالكامل [(LUKS FDE)](../encryption.md#linux-unified-key-setup) أثناء التثبيت. إذا لم تفعل هذا الخيار أثناء التثبيت، فستحتاج إلى حفظ نسخة احتياطية من بياناتك وإعادة تثبيت النظام، لأن التشفير يتم بعد [تقسيم القرص](https://en.wikipedia.org/wiki/Disk_partitioning) وقبل [تهيئته](https://en.wikipedia.org/wiki/File_system). ننصحك أيضا بمسح بيانات وحدة التخزين بشكل آمن:

- [مسح البيانات بشكل آمن :material-arrow-right-drop-circle:](https://www.privacyguides.org/articles/2022/05/25/secure-data-erasure/)

### مساحة التبديل (swap)

فكّر في استخدام [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) بدلًا من ملف أو partition عادي، لتجنب حفظ بيانات قد تكون حساسة من الذاكرة على القرص بشكل دائم (ولتحسين الأداء أيضا). تستخدم التوزيعات المبنية على Fedora [تقنية ZRAM افتراضيا](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

إذا كنت تحتاج إلى ميزة السبات (hibernation) (حفظ حالة النظام على القرص)، فستظل بحاجة إلى ملف أو partition عادي. تأكّد على الأقل من [تشفير](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) أي مساحة تبديل (swap space) موجودة على القرص، لتقليل بعض هذه المخاطر.

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
