---
title: Обзор Linux
icon: simple/linux
description: Linux - это альтернативная настольная операционная система с открытым исходным кодом, ориентированная на конфиденциальность, но не все дистрибутивы созданы одинаково.
---

**Linux** is an open-source, privacy-focused desktop operating system alternative. In the face of pervasive telemetry and other privacy-encroaching technologies in mainstream operating systems, desktop Linux has remained the clear choice for people looking for total control over their computers from the ground up.

Our website generally uses the term “Linux” to describe **desktop** Linux distributions. Other operating systems which also use the Linux kernel such as ChromeOS, Android, and Qubes OS are not discussed on this page.

[Наши рекомендации Linux :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Privacy Notes

There are some notable privacy concerns with Linux which you should be aware of. Despite these drawbacks, desktop Linux distributions are still great for most people who want to:

- Избежать телеметрии, которая часто поставляется с проприетарными операционными системами
- Maintain [software freedom](https://gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Use privacy-focused systems such as [Whonix](../desktop.md#whonix) or [Tails](../desktop.md#tails)

### Open-Source Security

It is a [common misconception](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) that Linux and other open-source software is inherently secure simply because the source code is available. There is an expectation that community verification occurs regularly, but this isn’t always [the case](https://seirdy.one/posts/2022/02/02/floss-security).

In reality, distro security depends on a number of factors, such as project activity, developer experience, the level of rigor applied to code reviews, and how often attention is given to specific parts of the codebase that may go untouched for years.

### Missing Security Features

At the moment, desktop Linux [falls behind alternatives](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) like macOS or Android when it comes to certain security features. We hope to see improvements in these areas in the future.

- **Verified boot** on Linux is not as robust as alternatives such as Apple’s [Secure Boot](https://support.apple.com/guide/security/secac71d5623/web) or Android’s [Verified Boot](https://source.android.com/security/verifiedboot). Verified boot prevents persistent tampering by malware and [evil maid attacks](https://en.wikipedia.org/wiki/Evil_Maid_attack), but is still largely [unavailable on even the most advanced distributions](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- **Strong sandboxing** for apps on Linux is severely lacking, even with containerized apps like Flatpaks or sandboxing solutions like Firejail. Flatpak is the most promising sandboxing utility for Linux thus far, but is still deficient in many areas and allows for [unsafe defaults](https://flatkill.org/2020) which allow most apps to trivially bypass their sandbox.

Additionally, Linux falls behind in implementing [exploit mitigations](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) which are now standard on other operating systems, such as Arbitrary Code Guard on Windows or Hardened Runtime on macOS. Also, most Linux programs and Linux itself are coded in memory-unsafe languages. Memory corruption bugs are responsible for the [majority of vulnerabilities](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code) fixed and assigned a CVE. While this is also true for Windows and macOS, they are quickly making progress on adopting memory-safe languages—such as Rust and Swift, respectively—while there is no similar effort to rewrite Linux in a memory-safe language like Rust.

## Выбор дистрибутива

Не все дистрибутивы Linux созданы одинаковыми. Our [Linux recommendation page](../desktop.md) is not meant to be an authoritative source on which distribution you should use, but our recommendations *are* aligned with the following guidelines. These are a few things you should keep in mind when choosing a distribution:

### Цикл релиза

Мы настоятельно рекомендуем вам выбирать дистрибутивы, которые близки к стабильным релизам программного обеспечения, часто называемые дистрибутивами с плавающим релизом. Это связано с тем, что дистрибутивы с замороженным циклом выпуска часто не обновляют версии пакетов и не получают обновлений безопасности.

For frozen distributions such as [Debian](https://debian.org/security/faq#handling), package maintainers are expected to backport patches to fix vulnerabilities rather than bump the software to the “next version” released by the upstream developer. Some security fixes [do not](https://arxiv.org/abs/2105.14565) receive a [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) (particularly less popular software) at all and therefore do not make it into the distribution with this patching model. As a result, minor security fixes are sometimes held back until the next major release.

Мы не считаем, что задержка пакетов и применение промежуточных исправлений является хорошей идеей, так как это расходится с тем, как разработчик мог задумать работу программного обеспечения. [Richard Brown](https://rootco.de/aboutme) has a presentation about this:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/i8c0mg_mS7U?local=true" title="Regular Releases are Wrong, Roll for your life" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Традиционные vs атомарные обновления

Традиционно дистрибутивы Linux обновляются путем последовательного обновления нужных пакетов. Традиционные обновления, например, используемые в дистрибутивах Fedora, Arch Linux и Debian, могут быть менее надежными, если в процессе обновления возникает ошибка.

Дистрибутивы с отомарными обновлениями применяют обновления полностью или не применяют вообще. Как правило, транзакционные системы обновления также являются атомарными.

Система транзакционного обновления создает снимок, который делается до и после применения обновления. Если обновление ломается в любой момент времени (например из-за сбоя питания), обновление можно легко откатить до "последнего известного хорошего состояния."

The Atomic update method is used for [distributions](../desktop.md#atomic-distributions) like Silverblue, Tumbleweed, and NixOS and can achieve reliability with this model. [Adam Šamalík](https://twitter.com/adsamalik) предоставил презентацию о том, как `rpm-ostree` работает с Silverblue:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/-hpV5l-gJnQ?local=true" title="Let's try Fedora Silverblue — an immutable desktop OS! - Adam Šamalik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Дистрибутивы "ориентированные на безопасность"

Часто возникает путаница между дистрибутивами "ориентированными на безопасность" и дистрибутивами для "тестов на проникновение". A quick search for “the most secure Linux distribution” will often give results like Kali Linux, Black Arch, or Parrot OS. Эти дистрибутивы представляют собой дистрибутивы для тестирования на проникновение, в которых собраны инструменты для тестирования других систем. Они не включают никаких "дополнительных мер безопасности" или защитных механизмов, предназначенных для регулярного использования.

### Дистрибутивы на базе Arch

Arch and Arch-based distributions are not recommended for those new to Linux (regardless of distribution) as they require regular [system maintenance](https://wiki.archlinux.org/title/System_maintenance). Arch does not have a distribution update mechanism for the underlying software choices. В результате вы должны быть в курсе современных тенденций и самостоятельно внедрять технологии по мере того, как они вытесняют старые методы.

Для поддержания безопасности системы от вас ожидается, что вы обладаете достаточными знаниями Linux, чтобы правильно настроить безопасность своей системы, например, принять систему [обязательного контроля доступа](https://en.wikipedia.org/wiki/Mandatory_access_control), настроить черные списки [модулей ядра](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security), усилить параметры загрузки, манипулировать параметрами [sysctl](https://en.wikipedia.org/wiki/Sysctl) и знать, какие компоненты им необходимы, например, [Polkit](https://en.wikipedia.org/wiki/Polkit).

Anyone using the [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **must** be comfortable auditing PKGBUILDs that they download from that service. AUR packages are community-produced content and are not vetted in any way, and therefore are vulnerable to software supply chain attacks, which has in fact happened [in the past](https://bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository).

The AUR should always be used sparingly, and often there is a lot of bad advice on various pages which direct people to blindly use [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) without sufficient warning. Аналогичные предупреждения относятся к использованию сторонних персональных архивов пакетов (PPA) в дистрибутивах на базе Debian или проектов сообщества (COPR) в Fedora.

If you are experienced with Linux and wish to use an Arch-based distribution, we generally recommend mainline Arch Linux over any of its derivatives.

Additionally, we recommend **against** these two Arch derivatives specifically:

- **Manjaro**: Этот дистрибутив задерживает пакеты на 2 недели, чтобы убедиться, что их собственные изменения не сломаются, а не для того, чтобы убедиться в стабильности upstream. Когда используются пакеты AUR, они часто собираются на основе последних [библиотек](https://en.wikipedia.org/wiki/Library_(computing)) из репозиториев Arch.
- **Garuda**: They use [Chaotic-AUR](https://aur.chaotic.cx) which automatically and blindly compiles packages from the AUR. Не существует процесса проверки, чтобы убедиться, что пакеты AUR не страдают от атак в цепи поставок.

### Ядро Linux-libre и дистрибутивы "Libre"

We recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://phoronix.com/news/GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode.

## Общие рекомендации

### Шифрование диска

Большинство дистрибутивов Linux имеют опцию в программе установки для включения [LUKS](../encryption.md#linux-unified-key-setup) FDE. Если этот параметр небыл выбран во время установки, вам придется создать резервную копию данных и выполнить повторную установку, поскольку шифрование применяется после [разметки диска](https://ru.wikipedia.org/wiki/%D0%A0%D0%B0%D0%B7%D0%B4%D0%B5%D0%BB_%D0%B4%D0%B8%D1%81%D0%BA%D0%B0), но до [форматирования файловых систем](https://ru.wikipedia.org/wiki/%D0%A4%D0%B0%D0%B9%D0%BB%D0%BE%D0%B2%D0%B0%D1%8F_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B0). Мы также рекомендуем безопасно удалять файлы на вашем накопителе:

- [Безопасное удаление данных :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure)

### Swap

Consider using [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) instead of a traditional swap file or partition to avoid writing potentially sensitive memory data to persistent storage (and improve performance). Fedora-based distributions [use ZRAM by default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

If you require suspend-to-disk (hibernation) functionality, you will still need to use a traditional swap file or partition. Make sure that any swap space you do have on a persistent storage device is [encrypted](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) at a minimum to mitigate some of these threats.

### Wayland

We recommend using a desktop environment that supports the [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)) display protocol, as it was developed with security [in mind](https://lwn.net/Articles/589147). Its predecessor ([X11](https://en.wikipedia.org/wiki/X_Window_System)) does not support GUI isolation, which allows any window to [record, log, and inject inputs in other windows](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), making any attempt at sandboxing futile. While there are options to do nested X11 such as [Xpra](https://en.wikipedia.org/wiki/Xpra) or [Xephyr](https://en.wikipedia.org/wiki/Xephyr), they often come with negative performance consequences, and are neither convenient to set up nor preferable over Wayland.

Fortunately, [Wayland compositors](https://en.wikipedia.org/wiki/Wayland_(protocol)#Wayland_compositors) such as those included with [GNOME](https://gnome.org) and [KDE Plasma](https://kde.org) now have good support for Wayland along with some other compositors that use [wlroots](https://gitlab.freedesktop.org/wlroots/wlroots/-/wikis/Projects-which-use-wlroots), (e.g. [Sway](https://swaywm.org)). Some distributions like Fedora and Tumbleweed use it by default, and some others may do so in the future as X11 is in [hard maintenance mode](https://phoronix.com/news/X.Org-Maintenance-Mode-Quickly). Если вы используете одну из этих сред, можно просто выбрать сессию "Wayland" в менеджере отображения рабочего стола ([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)).

Мы рекомендуем **не использовать** окружения рабочего стола или оконные менеджеры, которые не имеют поддержки Wayland, например Cinnamon (по умолчанию в Linux Mint), Pantheon (стандартный в Elementary OS), MATE, Xfce и i3.

### Проприетарная прошивка (обновления микрокода)

Some Linux distributions (such as [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)-based or DIY distros) don’t come with the proprietary [microcode](https://en.wikipedia.org/wiki/Microcode) updates which patch critical security vulnerabilities. Some notable examples of these vulnerabilities include [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), and other [hardware vulnerabilities](https://kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

We **highly recommend** that you install microcode updates, as they contain important security patches for the CPU which can not be fully mitigated in software alone. В Fedora и openSUSE обновления микрокода применяются по умолчанию.

### Обновления

Большинство дистрибутивов Linux автоматически устанавливают обновления или напоминают вам сделать это. Важно поддерживать ОС в актуальном состоянии, чтобы при обнаружении уязвимости программное обеспечение было исправлено.

Some distributions (particularly those aimed at advanced users) are more bare bones and expect you to do things yourself (e.g. Arch or Debian). Для получения важных обновлений безопасности потребуется вручную запустить "менеджер пакетов" (`apt`, `pacman`, `dnf` и т.д.).

Кроме того, некоторые дистрибутивы не будут автоматически загружать обновления прошивки. For that, you will need to install [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

## Твики конфиденциальности

### Рандомизация MAC-адресов

Many desktop Linux distributions (Fedora, openSUSE, etc.) come with [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) to configure Ethernet and Wi-Fi settings.

It is possible to [randomize](https://fedoramagazine.org/randomize-mac-address-nm) the [MAC address](https://en.wikipedia.org/wiki/MAC_address) when using NetworkManager. Это обеспечивает большую конфиденциальность в сетях Wi-Fi, так как затрудняет отслеживание конкретных устройств в сети, к которой вы подключены. Это [**не**](https://papers.mathyvanhoef.com/wisec2016.pdf) делает вас анонимным.

We recommend changing the setting to **random** instead of **stable**, as suggested in the [article](https://fedoramagazine.org/randomize-mac-address-nm).

If you are using [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), you will need to set [`MACAddressPolicy=random`](https://freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) which will enable [RFC 7844 (Anonymity Profiles for DHCP Clients)](https://freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

MAC address randomization is primarily beneficial for Wi-Fi connections. For Ethernet connections, randomizing your MAC address provides little (if any) benefit, because a network administrator can trivially identify your device by other means (such as inspecting the port you are connected to on the network switch). Рандомизация MAC-адресов Wi-Fi зависит от поддержки встроенного программного обеспечения Wi-Fi.

### Другие идентификаторы

Существуют и другие системные идентификаторы, с которыми следует быть осторожными. Вам следует подумать, применимо ли это к вашей [модели угрозы](../basics/threat-modeling.md):

- **Хост-имена:** Имя хоста вашей системы является общим для сетей, к которым вы подключаетесь. Вам следует избегать включения в имя хоста идентифицирующих терминов, таких как ваше имя или операционная система, вместо этого следует использовать общие термины или случайные строки.
- **Имена пользователей:** Аналогично, ваше имя пользователя используется различными способами в вашей системе. Рассмотрите возможность использования общих терминов, таких как "пользователь", вместо вашего настоящего имени.
- **Machine ID:** During installation, a unique machine ID is generated and stored on your device. Рассмотрите возможность [установки случайного идентификатора](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### Подсчёт систем

Проект Fedora [подсчитывает](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting), сколько уникальных систем обращаются к его зеркалам, используя переменную [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) вместо уникального ID. Fedora делает это для определения нагрузки и предоставления лучших серверов для обновлений, где это необходимо.

Эта [опция](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) в настоящее время по умолчанию выключена. Мы рекомендуем добавить `countme=false` в `/etc/dnf/dnf.conf` на случай, если она будет включена в будущем. On systems that use `rpm-ostree` such as Silverblue, the countme option is disabled by masking the [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems) timer.

openSUSE also uses a [unique ID](https://en.opensuse.org/openSUSE:Statistics) to count systems, which can be disabled by emptying the `/var/lib/zypp/AnonymousUniqueId` file.
