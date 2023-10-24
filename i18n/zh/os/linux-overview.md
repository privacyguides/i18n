---
title: Linux概述
icon: simple/linux
description: Linux is an open-source, privacy-focused desktop operating system alternative, but not all distribitions are created equal.
---

**Linux** is an open-source, privacy-focused desktop operating system alternative. In the face of pervasive telemetry and other privacy-encroaching technologies in mainstream operating systems, Linux desktop has remained the clear choice for people looking for total control over their computers from the ground up.

Our website generally uses the term “Linux” to describe **desktop** Linux distributions. Other operating systems which also use the Linux kernel such as ChromeOS, Android, and Qubes OS are not discussed on this page.

[我们的Linux推荐 :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Privacy Notes

There are some notable privacy concerns with Linux which you should be aware of. Despite these drawbacks, desktop Linux distributions are still great for most people who want to:

- 避免专有操作系统中经常出现的遥测现象
- 保持 [软件自由](https://www.gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Use privacy focused systems such as [Whonix](https://www.whonix.org) or [Tails](https://tails.boum.org/)

### Open-Source Security

It is a [common misconception](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) that Linux and other open-source software is inherently secure simply because the source code is available. There is an expectation that community verification occurs regularly, but this isn’t always [the case](https://seirdy.one/posts/2022/02/02/floss-security/).

In reality, distro security depends on a number of factors, such as project activity, developer experience, the level of rigor applied to code reviews, and how often attention is given to specific parts of the codebase that may go untouched for years.

### Missing Security Features

At the moment, desktop Linux [falls behind alternatives](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) like macOS or Android when it comes to certain security features. We hope to see improvements in these areas in the future.

- **Verified boot** on Linux is not as robust as alternatives such as Apple’s [Secure Boot](https://support.apple.com/guide/security/secac71d5623/web) or Android’s [Verified Boot](https://source.android.com/security/verifiedboot). Verified boot prevents persistent tampering by malware and [evil maid attacks](https://en.wikipedia.org/wiki/Evil_Maid_attack), but is still largely [unavailable on even the most advanced distributions](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- **Strong sandboxing** for apps on Linux is severely lacking, even with containerized apps like Flatpaks or sandboxing solutions like Firejail. Flatpak is the most promising sandboxing utility for Linux thus far, but is still deficient in many areas and allows for [unsafe defaults](https://flatkill.org/2020/) which allow most apps to trivially bypass their sandbox.

Additionally, Linux falls behind in implementing [exploit mitigations](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) which are now standard on other operating systems, such as Arbitrary Code Guard on Windows or Hardened Runtime on macOS. Also, most Linux programs and Linux itself are coded in memory-unsafe languages. Memory corruption bugs are responsible for the [majority of vulnerabilities](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code/) fixed and assigned a CVE. While this is also true for Windows and macOS, they are quickly making progress on adopting memory-safe languages—such as Rust and Swift, respectively—while there is no similar effort to rewrite Linux in a memory-safe language like Rust.

## 选择您的发行版

并非所有的 Linux 发行版都是相同的。 Our [Linux recommendation page](../desktop.md) is not meant to be an authoritative source on which distribution you should use, but our recommendations *are* aligned with the following guidelines. These are a few things you should keep in mind when choosing a distribution:

### 发布周期

我们强烈建议你选择与稳定的上游软件版本接近的发行版，通常被称为滚动发行版。 这是因为冻结发布周期的发行版往往不更新软件包版本，并且在安全更新方面落后。

对于冻结的发行版，如 [Debian](https://www.debian.org/security/faq#handling)，软件包维护者被要求回传补丁来修复漏洞，而不是将软件提升到上游开发者发布的 "下一个版本"。 Some security fixes [do not](https://arxiv.org/abs/2105.14565) receive a [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) (particularly less popular software) at all and therefore do not make it into the distribution with this patching model. 因此，小的安全修复有时会被推迟到下一个主要版本。

我们不认为保留软件包和应用临时补丁是一个好主意，因为它偏离了开发者可能打算让软件工作的方式。 [理查德-布朗](https://rootco.de/aboutme/) ，有一个关于这个问题的介绍。

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/i8c0mg_mS7U?local=true" title="定期发布是错误的，为你的生活而滚动" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### 传统vs原子更新

传统上，Linux发行版的更新方式是依次更新所需的软件包。 如果在更新时发生错误，传统的更新，如基于Fedora、Arch Linux和Debian的发行版中使用的更新，可能不太可靠。

原子更新发行版完全或根本不应用更新。 通常情况下，事务性更新系统也是原子性的。

事务性更新系统创建了一个快照，在应用更新之前和之后进行。 如果更新在任何时候失败（也许是由于电源故障），更新可以很容易地回滚到 "最后已知良好状态"。

原子更新法用于Silverblue、Tumbleweed和NixOS等不可变的发行版，可以通过这种模式实现可靠性。 [Adam Šamalík](https://twitter.com/adsamalik) 提供了一个关于 `rpm-ostree` 如何与Silverblue一起工作的演讲。

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/-hpV5l-gJnQ?local=true" title="让我们试试Fedora Silverblue--一个不可改变的桌面操作系统! - Adam Šamalik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### “以安全为重点”的分发

通常在“以安全为中心”的发行版和“渗透测试”发行版之间存在一些混淆。 A quick search for “the most secure Linux distribution” will often give results like Kali Linux, Black Arch, or Parrot OS. 这些发行版是攻击性的渗透测试发行版，捆绑了测试其他系统的工具。 它们不包括任何 "额外的安全 "或用于常规使用的防御性缓解措施。

### 基于Arch的发行版

Arch and Arch-based distributions are not recommended for those new to Linux (regardless of distribution) as they require regular [system maintenance](https://wiki.archlinux.org/title/System_maintenance). Arch does not have a distribution update mechanism for the underlying software choices. 因此，你必须保持对当前趋势的了解，并在技术取代旧有做法时自行采用。

对于一个安全的系统，你还应该有足够的Linux知识来为他们的系统正确设置安全，如采用 [强制性访问控制](https://en.wikipedia.org/wiki/Mandatory_access_control) 系统，设置 [内核模块](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) 黑名单，硬化启动参数，操作 [sysctl](https://en.wikipedia.org/wiki/Sysctl) 参数，并知道他们需要哪些组件，如 [Polkit](https://en.wikipedia.org/wiki/Polkit)。

Anyone using the [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **must** be comfortable auditing PKGBUILDs that they download from that service. AUR软件包是社区制作的内容，没有经过任何审查，因此很容易受到软件供应链的攻击，事实上在过去已经发生了 [](https://www.bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository/)。

The AUR should always be used sparingly, and often there is a lot of bad advice on various pages which direct people to blindly use [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) without sufficient warning. 类似的警告也适用于在基于Debian的发行版上使用第三方个人软件包档案（PPAs）或在Fedora上使用社区项目（COPR）。

If you are experienced with Linux and wish to use an Arch-based distribution, we generally recommend mainline Arch Linux over any of its derivatives.

Additionally, we recommend **against** these two Arch derivatives specifically:

- **Manjaro**: 这个发行版将软件包保留2周，以确保他们自己的修改不会破坏，而不是确保上游的稳定。 当使用AUR软件包时，它们通常是根据Arch的软件库中最新的 [库构建的](https://en.wikipedia.org/wiki/Library_(computing))。
- **Garuda**: 他们使用 [Chaotic-AUR](https://aur.chaotic.cx/) ，它自动地、盲目地从AUR编译软件包。 没有验证过程来确保AUR包不会受到供应链的攻击。

### Linux-libre内核和“Libre”发行版

We recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://www.phoronix.com/news/GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode.

## 一般建议

### 驱动器加密

大多数Linux发行版在其安装程序中都有一个选项用于启用 [LUKS](../encryption.md#linux-unified-key-setup) FDE。 如果在安装时没有设置这个选项，你将不得不备份你的数据并重新安装，因为加密是在 [磁盘分区](https://en.wikipedia.org/wiki/Disk_partitioning)，但在 [文件系统](https://en.wikipedia.org/wiki/File_system) 被格式化之前应用。 我们还建议安全地删除你的存储设备。

- [安全数据清除 :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure/)

### Swap

Consider using [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) instead of a traditional swap file or partition to avoid writing potentially sensitive memory data to persistent storage (and improve performance). Fedora-based distributions [use ZRAM by default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

If you require suspend-to-disk (hibernation) functionality, you will still need to use a traditional swap file or partition. Make sure that any swap space you do have on a persistent storage device is [encrypted](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) at a minimum to mitigate some of these threats.

### Wayland

We recommend using a desktop environment that supports the [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)) display protocol, as it was developed with security [in mind](https://lwn.net/Articles/589147/). Its predecessor ([X11](https://en.wikipedia.org/wiki/X_Window_System)) does not support GUI isolation, which allows any window to [record, log, and inject inputs in other windows](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), making any attempt at sandboxing futile. While there are options to do nested X11 such as [Xpra](https://en.wikipedia.org/wiki/Xpra) or [Xephyr](https://en.wikipedia.org/wiki/Xephyr), they often come with negative performance consequences, and are neither convenient to set up nor preferable over Wayland.

幸运的是，常见的环境，如 [GNOME](https://www.gnome.org)， [KDE](https://kde.org)，以及窗口管理器 [Sway](https://swaywm.org) 都支持 Wayland。 Some distributions like Fedora and Tumbleweed use it by default, and some others may do so in the future as X11 is in [hard maintenance mode](https://www.phoronix.com/news/X.Org-Maintenance-Mode-Quickly). 如果你使用的是这些环境之一，就像在桌面显示管理器中选择 "Wayland "会话一样简单([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)) 。

</strong> 我们建议 **，反对使用没有Wayland支持的桌面环境或窗口管理器，如Cinnamon（Linux Mint的默认）、Pantheon（Elementary OS的默认）、MATE、Xfce和i3。</p>

### 专有固件(Microcode更新)

Some Linux distributions (such as [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)-based or DIY distros) don’t come with the proprietary [microcode](https://en.wikipedia.org/wiki/Microcode) updates which patch critical security vulnerabilities. 这些漏洞的一些明显例子包括： [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), 以及其他 [硬件漏洞](https://www.kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html)。

We **highly recommend** that you install microcode updates, as they contain important security patches for the CPU which can not be fully mitigated in software alone. Fedora和openSUSE都有默认应用的微码更新。

### 更新

大多数Linux发行版会自动安装更新或提醒你这样做。 重要的是保持你的操作系统是最新的，这样当发现漏洞时，你的软件就会打上补丁。

Some distributions (particularly those aimed at advanced users) are more bare bones and expect you to do things yourself (e.g. Arch or Debian). 这些将需要手动运行 "软件包管理器" (`apt`, `pacman`, `dnf`, 等等)，以便接收重要的安全更新。

此外，一些发行版将不会自动下载固件更新。 为此，你将需要安装 [`fwupd`](https://wiki.archlinux.org/title/Fwupd)。

## 隐私调整

### MAC地址随机化

Many desktop Linux distributions (Fedora, openSUSE, etc.) come with [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) to configure Ethernet and Wi-Fi settings.

在使用NetworkManager时，可以随机化 [](https://fedoramagazine.org/randomize-mac-address-nm/) [MAC地址](https://en.wikipedia.org/wiki/MAC_address)。 这在Wi-Fi网络上提供了更多的隐私，因为它使你更难追踪你所连接的网络上的特定设备。 它并不是 [****](https://papers.mathyvanhoef.com/wisec2016.pdf) 让你匿名。

我们建议将设置改为 **随机** ，而不是 **稳定**，正如 [文章中建议的那样](https://fedoramagazine.org/randomize-mac-address-nm/)。

如果你使用 [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components)，你需要设置 [`MACAddressPolicy=random`](https://www.freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) ，这将启用 [RFC 7844 (Anonymity Profiles for DHCP Clients)](https://www.freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=)。

MAC address randomization is primarily beneficial for Wi-Fi connections. For Ethernet connections, randomizing your MAC address provides little (if any) benefit, because a network administrator can trivially identify your device by other means (such as inspecting the port you are connected to on the network switch). 随机化Wi-Fi MAC地址取决于Wi-Fi固件的支持。

### 其他标识符

还有一些其他的系统标识符，你可能要小心对待。 你应该考虑一下，看看它是否适用于你的 [威胁模型](../basics/threat-modeling.md)。

- **主机名。** 你的系统的主机名是与你所连接的网络共享的。 你应该避免在你的主机名中包括像你的名字或操作系统这样的识别术语，而是坚持使用通用术语或随机字符串。
- **用户名。** 同样地，你的用户名在你的系统中以各种方式使用。 考虑使用 "用户 "这样的通用术语，而不是你的真实姓名。
- **机器ID：**：在安装过程中，会生成一个独特的机器ID并存储在你的设备上。 考虑 [，将其设置为一个通用的ID](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id)。

### 系统计数

Fedora 项目 [通过使用一个 [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) 变量而不是唯一的 ID 来计算](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) 有多少独特的系统访问它的镜像。 Fedora这样做是为了确定负载并在必要时为更新提供更好的服务器。

这个 [选项](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) ，目前默认是关闭的。 我们建议将 `countme=false` 添加到 `/etc/dnf/dnf.conf` ，以备将来启用它。 在使用 `rpm-ostree` 的系统上，如Silverblue，通过屏蔽 [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems/) 计时器来禁用 countme 选项。

openSUSE 还使用一个 [唯一的 ID](https://en.opensuse.org/openSUSE:Statistics) 来计算系统，可以通过删除 `/var/lib/zypp/AnonymousUniqueId` 文件来禁用它。
