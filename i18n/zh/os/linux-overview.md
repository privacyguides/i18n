---
title: Linux Overview
icon: simple/linux
description: Linux is an open-source, privacy-focused desktop operating system alternative, but not all distribitions are created equal.
---

**Linux** is an open-source, privacy-focused desktop operating system alternative. In the face of pervasive telemetry and other privacy-encroaching technologies in mainstream operating systems, desktop Linux has remained the clear choice for people looking for total control over their computers from the ground up.

Our website generally uses the term “Linux” to describe **desktop** Linux distributions. Other operating systems which also use the Linux kernel such as ChromeOS, Android, and Qubes OS are not discussed on this page.

[我们的Linux推荐 :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Privacy Notes

There are some notable privacy concerns with Linux which you should be aware of. Despite these drawbacks, desktop Linux distributions are still great for most people who want to:

- 避免专有操作系统中经常出现的遥测现象
- Maintain [software freedom](https://gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Use privacy-focused systems such as [Whonix](../desktop.md#whonix) or [Tails](../desktop.md#tails)

### Open-Source Security

It is a [common misconception](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) that Linux and other open-source software are inherently secure simply because the source code is available. There is an expectation that community verification occurs regularly, but this isn’t always [the case](https://seirdy.one/posts/2022/02/02/floss-security).

In reality, distro security depends on a number of factors, such as project activity, developer experience, the level of rigor applied to code reviews, and how often attention is given to specific parts of the codebase that may go untouched for years.

### Missing Security Features

At the moment, desktop Linux [falls behind alternatives](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) like macOS or Android when it comes to certain security features. We hope to see improvements in these areas in the future.

- **Verified boot** on Linux is not as robust as alternatives such as Apple’s [Secure Boot](https://support.apple.com/guide/security/secac71d5623/web) or Android’s [Verified Boot](https://source.android.com/security/verifiedboot). Verified boot prevents persistent tampering by malware and [evil maid attacks](https://en.wikipedia.org/wiki/Evil_Maid_attack), but is still largely [unavailable on even the most advanced distributions](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- **Strong sandboxing** for apps on Linux is severely lacking, even with containerized apps like Flatpaks or sandboxing solutions like Firejail. Flatpak is the most promising sandboxing utility for Linux thus far, but is still deficient in many areas and allows for [unsafe defaults](https://flatkill.org/2020) which permit most apps to trivially bypass their sandbox.

Additionally, Linux falls behind in implementing [exploit mitigations](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) which are now standard on other operating systems, such as Arbitrary Code Guard on Windows or Hardened Runtime on macOS. Also, most Linux programs and Linux itself are coded in memory-unsafe languages. Memory corruption bugs are responsible for the [majority of vulnerabilities](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code) fixed and assigned a CVE. While this is also true for Windows and macOS, they are quickly making progress on adopting memory-safe languages—such as Rust and Swift, respectively—while there is no similar effort to rewrite Linux in a memory-safe language like Rust.

## 选择您的发行版

并非所有的 Linux 发行版都是相同的。 Our [Linux recommendation page](../desktop.md) is not meant to be an authoritative source on which distribution you should use, but our recommendations *are* aligned with the following guidelines. These are a few things you should keep in mind when choosing a distribution:

### 发布周期

我们强烈建议你选择与稳定的上游软件版本接近的发行版，通常被称为滚动发行版。 这是因为冻结发布周期的发行版往往不更新软件包版本，并且在安全更新方面落后。

For frozen distributions such as [Debian](https://debian.org/security/faq#handling), package maintainers are expected to backport patches to fix vulnerabilities rather than bump the software to the “next version” released by the upstream developer. Some security fixes (particularly for less popular software) [do not](https://arxiv.org/abs/2105.14565) receive a [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) at all and therefore do not make it into the distribution with this patching model. As a result, minor security fixes are sometimes held back until the next major release.

我们不认为保留软件包和应用临时补丁是一个好主意，因为它偏离了开发者可能打算让软件工作的方式。 [Richard Brown](https://rootco.de/aboutme) has a presentation about this:

- [Regular Releases are Wrong, Roll for your life](https://youtu.be/i8c0mg_mS7U) <small>(YouTube)</small>

### Traditional vs Atomic Updates

传统上，Linux发行版的更新方式是依次更新所需的软件包。 Traditional updates such as those used in Fedora, Arch Linux, and Debian-based distributions can be less reliable if an error occurs while updating.

Atomic updating distributions, on the other hand, apply updates in full or not at all. On an atomic distribution, if an error occurs while updating (perhaps due to a power failure), nothing is changed on the system.

The atomic update method can achieve reliability with this model and is used for [distributions](../desktop.md#atomic-distributions) like Silverblue and NixOS. [Adam Šamalík](https://twitter.com/adsamalik) provides a presentation on how `rpm-ostree` works with Silverblue:

- [Let's try Fedora Silverblue — an immutable desktop OS! - Adam Šamalik](https://youtu.be/aMo4ZlWznao) <small>(YouTube)</small>

### “以安全为重点”的分发

通常在“以安全为中心”的发行版和“渗透测试”发行版之间存在一些混淆。 A quick search for “the most secure Linux distribution” will often give results like Kali Linux, Black Arch, or Parrot OS. 这些发行版是攻击性的渗透测试发行版，捆绑了测试其他系统的工具。 它们不包括任何 "额外的安全 "或用于常规使用的防御性缓解措施。

### 基于Arch的发行版

Arch and Arch-based distributions are not recommended for those new to Linux (regardless of distribution) as they require regular [system maintenance](https://wiki.archlinux.org/title/System_maintenance). Arch does not have a distribution update mechanism for the underlying software choices. As a result you have to stay aware with current trends and adopt technologies on your own as they supersede older practices.

For a secure system, you are also expected to have sufficient Linux knowledge to properly set up security for their system such as adopting a [mandatory access control](#mandatory-access-control) system, setting up [kernel module](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) blacklists, hardening boot parameters, manipulating [sysctl](https://en.wikipedia.org/wiki/Sysctl) parameters, and knowing what components they need such as [Polkit](https://en.wikipedia.org/wiki/Polkit).

Anyone using the [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **must** be comfortable auditing PKGBUILDs that they download from that service. AUR packages are community-produced content and are not vetted in any way, and therefore are vulnerable to software supply chain attacks, which has in fact happened [in the past](https://bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository).

The AUR should always be used sparingly, and often there is a lot of bad advice on various pages which direct people to blindly use [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) without sufficient warning. Similar warnings apply to the use of third-party Personal Package Archives (PPAs) on Debian-based distributions or Community Projects (COPR) on Fedora.

If you are experienced with Linux and wish to use an Arch-based distribution, we generally recommend mainline Arch Linux over any of its derivatives.

Additionally, we recommend **against** these two Arch derivatives specifically:

- **Manjaro**: 这个发行版将软件包保留2周，以确保他们自己的修改不会破坏，而不是确保上游的稳定。 当使用AUR软件包时，它们通常是根据Arch的软件库中最新的 [库构建的](https://en.wikipedia.org/wiki/Library_(computing))。
- **Garuda**: They use [Chaotic-AUR](https://aur.chaotic.cx) which automatically and blindly compiles packages from the AUR. 没有验证过程来确保AUR包不会受到供应链的攻击。

### Linux-libre内核和“Libre”发行版

We recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://phoronix.com/news/GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode.

### Mandatory access control

Mandatory access control is a set of additional security controls which help to confine parts of the system such as apps and system services. The two common forms of mandatory access control found in Linux distributions are [SELinux](https://github.com/SELinuxProject) and [AppArmor](https://apparmor.net). While Fedora uses SELinux by default, Tumbleweed [defaults](https://en.opensuse.org/Portal:SELinux) to AppArmor in the installer, with an option to [choose](https://en.opensuse.org/Portal:SELinux/Setup) SELinux instead.

SELinux on [Fedora](https://docs.fedoraproject.org/en-US/quick-docs/selinux-getting-started) confines Linux containers, virtual machines, and service daemons by default. AppArmor is used by the snap daemon for [sandboxing](https://snapcraft.io/docs/security-sandboxing) snaps which have [strict](https://snapcraft.io/docs/snap-confinement) confinement such as [Firefox](https://snapcraft.io/firefox). There is a community effort to confine more parts of the system in Fedora with the [ConfinedUsers](https://fedoraproject.org/wiki/SIGs/ConfinedUsers) special interest group.

## 一般建议

### 驱动器加密

大多数Linux发行版在其安装程序中都有一个选项用于启用 [LUKS](../encryption.md#linux-unified-key-setup) FDE。 如果在安装时没有设置这个选项，你将不得不备份你的数据并重新安装，因为加密是在 [磁盘分区](https://en.wikipedia.org/wiki/Disk_partitioning)，但在 [文件系统](https://en.wikipedia.org/wiki/File_system) 被格式化之前应用。 我们还建议安全地删除你的存储设备。

- [安全数据清除 :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure)

### Swap

Consider using [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) instead of a traditional swap file or partition to avoid writing potentially sensitive memory data to persistent storage (and improve performance). Fedora-based distributions [use ZRAM by default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

If you require suspend-to-disk (hibernation) functionality, you will still need to use a traditional swap file or partition. Make sure that any swap space you do have on a persistent storage device is [encrypted](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) at a minimum to mitigate some of these threats.

### Wayland

We recommend using a desktop environment that supports the [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)) display protocol, as it was developed with security [in mind](https://lwn.net/Articles/589147). Its predecessor ([X11](https://en.wikipedia.org/wiki/X_Window_System)) does not support GUI isolation, which allows any window to [record, log, and inject inputs in other windows](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), making any attempt at sandboxing futile.

Fortunately, [Wayland compositors](https://en.wikipedia.org/wiki/Wayland_(protocol)#Wayland_compositors) such as those included with [GNOME](https://gnome.org) and [KDE Plasma](https://kde.org) now have good support for Wayland along with some other compositors that use [wlroots](https://gitlab.freedesktop.org/wlroots/wlroots/-/wikis/Projects-which-use-wlroots), (e.g. [Sway](https://swaywm.org)). Some distributions like Fedora and Tumbleweed use it by default, and some others may do so in the future as X11 is in [hard maintenance mode](https://phoronix.com/news/X.Org-Maintenance-Mode-Quickly). If you’re using one of those environments, it is as easy as selecting the “Wayland” session at the desktop display manager ([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)).

</strong> 我们建议 **，反对使用没有Wayland支持的桌面环境或窗口管理器，如Cinnamon（Linux Mint的默认）、Pantheon（Elementary OS的默认）、MATE、Xfce和i3。</p>

### 专有固件(Microcode更新)

Some Linux distributions (such as [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)-based or DIY distros) don’t come with the proprietary [microcode](https://en.wikipedia.org/wiki/Microcode) updates which patch critical security vulnerabilities. Some notable examples of these vulnerabilities include [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), and other [hardware vulnerabilities](https://kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

We **highly recommend** that you install microcode updates, as they contain important security patches for the CPU which can not be fully mitigated in software alone. Fedora and openSUSE both apply microcode updates by default.

### 更新

大多数Linux发行版会自动安装更新或提醒你这样做。 重要的是保持你的操作系统是最新的，这样当发现漏洞时，你的软件就会打上补丁。

Some distributions (particularly those aimed at advanced users) are more bare bones and expect you to do things yourself (e.g. Arch or Debian). 这些将需要手动运行 "软件包管理器" (`apt`, `pacman`, `dnf`, 等等)，以便接收重要的安全更新。

此外，一些发行版将不会自动下载固件更新。 For that, you will need to install [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

## 隐私调整

### MAC地址随机化

Many desktop Linux distributions (Fedora, openSUSE, etc.) come with [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) to configure Ethernet and Wi-Fi settings.

It is possible to [randomize](https://fedoramagazine.org/randomize-mac-address-nm) the [MAC address](https://en.wikipedia.org/wiki/MAC_address) when using NetworkManager. 这在Wi-Fi网络上提供了更多的隐私，因为它使你更难追踪你所连接的网络上的特定设备。 它并不是 [****](https://papers.mathyvanhoef.com/wisec2016.pdf) 让你匿名。

We recommend changing the setting to **random** instead of **stable**, as suggested in the [article](https://fedoramagazine.org/randomize-mac-address-nm).

If you are using [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), you will need to set [`MACAddressPolicy=random`](https://freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) which will enable [RFC 7844 (Anonymity Profiles for DHCP Clients)](https://freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

MAC address randomization is primarily beneficial for Wi-Fi connections. For Ethernet connections, randomizing your MAC address provides little (if any) benefit, because a network administrator can trivially identify your device by other means (such as inspecting the port you are connected to on the network switch). 随机化Wi-Fi MAC地址取决于Wi-Fi固件的支持。

### 其他标识符

还有一些其他的系统标识符，你可能要小心对待。 你应该考虑一下，看看它是否适用于你的 [威胁模型](../basics/threat-modeling.md)。

- **主机名。** 你的系统的主机名是与你所连接的网络共享的。 你应该避免在你的主机名中包括像你的名字或操作系统这样的识别术语，而是坚持使用通用术语或随机字符串。
- **用户名。** 同样地，你的用户名在你的系统中以各种方式使用。 考虑使用 "用户 "这样的通用术语，而不是你的真实姓名。
- **Machine ID:** During installation, a unique machine ID is generated and stored on your device. 考虑 [，将其设置为一个通用的ID](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id)。

### 系统计数

Fedora 项目 [通过使用一个 [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) 变量而不是唯一的 ID 来计算](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) 有多少独特的系统访问它的镜像。 Fedora这样做是为了确定负载并在必要时为更新提供更好的服务器。

这个 [选项](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) ，目前默认是关闭的。 我们建议将 `countme=false` 添加到 `/etc/dnf/dnf.conf` ，以备将来启用它。 On systems that use `rpm-ostree` such as Silverblue, the countme option is disabled by masking the [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems) timer.

openSUSE also uses a [unique ID](https://en.opensuse.org/openSUSE:Statistics) to count systems, which can be disabled by emptying the `/var/lib/zypp/AnonymousUniqueId` file.
