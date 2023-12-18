---
title: "Android 应用"
icon: simple/linux
description: 由于隐私保护和软件自由，Linux发行版被普遍推荐。
cover: desktop.webp
---

由于隐私保护和软件自由，Linux发行版被普遍推荐。 如果你还没有使用Linux，下面是我们建议尝试的一些发行版，以及一些适用于许多Linux发行版的一般隐私和安全改进提示。

- [安卓概况 :material-arrow-right-drop-circle:](os/linux-overview.md)

## 传统发行版

### Fedora Workstation（Fedora 工作站）

!!! recommendation

    ![Fedora标志](assets/img/linux-desktop/fedora-workstation.svg) { align=right }
    
    **Fedora Workstation**是我们为刚接触Linux的人推荐的发行版。 Fedora通常在其他发行版之前采用较新的技术，例如： [Wayland](https://wayland.freedesktop.org/), [PipeWire](https://pipewire.org)。 这些新技术往往伴随着安全、隐私和总体可用性的改进。
    
    [:octicons-home-16: Homepage](https://fedoraproject.org/workstation/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=Documentation}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribute }

Fedora有一个半滚动的发布周期。 虽然有些软件包如 [GNOME](https://www.gnome.org) 被冻结到下一个 Fedora 版本，但大多数软件包(包括内核)在整个发行期都会频繁更新。 每个Fedora版本都支持一年，每6个月发布一个新版本。

### openSUSE Tumbleweed

!!! recommendation

    ![openSUSE Tumbleweed logo](assets/img/linux-desktop/opensus-tumbleweed.svg){ align=right }
    
    **openSUSE Tumbleweed**是一个稳定的滚动发布版本。
    
    openSUSE Tumbleweed 有一个 [事务性更新](https://kubic.opensuse.org/blog/2018-04-04-transactionalupdates/) 系统，使用 [Btrfs](https://en.wikipedia.org/wiki/Btrfs) 和 [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) 来确保快照在出现问题时可以回滚。
    
    [:octicons-home-16: 主页](https://getfedora.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=文档}
    [:octicons-heart-16:](https://shop.opensuse.org/){ .card-link title=贡献 }

Tumbleweed采用的是滚动发布模式，每次更新都是以快照的形式发布。 当你升级你的系统时，会下载一个新的快照。 每个快照都要通过一系列的自动测试，由 [openQA](https://openqa.opensuse.org) ，以确保其质量。

### Arch Linux

!!! recommendation

    ![Arch标志](assets/img/linux-desktop/archlinux.svg){ align=right }
    
    **Arch Linux**是一个轻量级的、自己动手的（DIY）发行版，意味着你只得到你所安装的东西。 更多信息见他们的 [FAQ]（https://wiki.archlinux.org/title/Frequently_asked_questions）。
    
    [:octicons-home-16: 主页](https://getfedora.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=文档}
    [:octicons-heart-16:](https://archlinux.org/donate/){ .card-link title=贡献 }

Arch Linux有一个滚动的发布周期。 没有固定的发布时间表，软件包的更新非常频繁。

作为一个 DIY 发行版，您需要 [自行设置并维护您的](os/linux-overview.md#arch-based-distributions) 系统。 Arch有一个 [官方安装程序](https://wiki.archlinux.org/title/Archinstall) ，使安装过程更容易一些。

[Arch Linux的很大一部分软件包](https://reproducible.archlinux.org) ，都是 [，可复制的](https://reproducible-builds.org)。

## 不变的发行版

### Fedora Silverblue

!!! recommendation

    ![Fedora Silverblue logo](assets/img/linux-desktop/fedora-silverblue.svg){ align=right }
    
    **Fedora Silverblue** is an immutable variant of Fedora with a strong focus on container workflows and the [GNOME](https://www.gnome.org/) desktop environment. If you prefer an environment other than GNOME, there are also other variants including [Kinoite](https://fedoraproject.org/kinoite/) (which comes with [KDE](https://kde.org/)) and [Sericea](https://fedoraproject.org/sericea/) (which comes with [Sway](https://swaywm.org/), a [Wayland](https://wayland.freedesktop.org)-only tiling window manager). We don't recommend [Onyx](https://fedoraproject.org/onyx/) at this time as it still [requires X11](https://buddiesofbudgie.org/blog/wayland). All of these variants follow the same release schedule as Fedora Workstation, benefiting from the same fast updates and staying very close to upstream.
    
    [:octicons-home-16: Homepage](https://fedoraproject.org/silverblue/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/fedora-silverblue/){ .card-link title=Documentation}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribute }

Silverblue and its variants differ from Fedora Workstation as they replace the [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf/) package manager with a much more advanced alternative called [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/package-management/rpm-ostree/). `rpm-ostree` 软件包管理器的工作方式是为系统下载一个基本镜像，然后在一个 [git](https://en.wikipedia.org/wiki/Git)-like commit tree中叠加软件包。 当系统更新时，会下载一个新的基本图像，覆盖物将被应用于该新图像。

更新完成后，你将重新启动系统进入新的部署。 `rpm-ostree` 保持系统的两个部署，这样如果在新的部署中出现问题，你可以很容易地回滚。 还可以根据需要选择钉更多的部署。

[Flatpak](https://www.flatpak.org) 是这些发行版上的主要软件包安装方法，因为 `rpm-ostree` 只是为了在基础镜像上叠加那些不能留在容器内的软件包。

作为Flatpaks的替代方案，可以选择 [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox/) ，创建 [Podman](https://podman.io) 容器，与主机操作系统共享主目录，模仿传统的Fedora环境，这对有眼光的开发者来说是一个 [有用的功能](https://containertoolbx.org)。

### NixOS

!!! recommendation

    ![NixOS标志](assets/img/linux-desktop/nixos.svg){ align=right }
    
    NixOS是一个基于Nix软件包管理器的独立发行版，注重可重复性和可靠性。
    
    [:octicons-home-16: 主页](https://nixos.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=文档}
    [:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=贡献 }

NixOS的软件包管理器将每个软件包的每个版本保存在 **Nix商店的不同文件夹中**。 由于这个原因，你可以在你的系统上安装同一软件包的不同版本。 在包的内容被写入文件夹后，该文件夹被变成只读。

NixOS还提供了原子式更新；首先它下载（或构建）新一代系统的软件包和文件，然后切换到它。 有不同的方法来切换到新一代；你可以告诉NixOS在重启后激活它，或者你可以在运行时切换到它。 你也可以 *测试* ，在运行时切换到新的一代，但不把它设置为当前系统的一代。 如果在更新过程中出现了什么问题，你可以直接重新启动，并自动返回到你的系统的工作版本。

Nix软件包管理器使用一种纯粹的函数式语言--它也被称为Nix--来定义软件包。

[Nixpkgs](https://github.com/nixos/nixpkgs) （软件包的主要来源）包含在一个GitHub仓库中。 你也可以用同样的语言定义你自己的包，然后轻松地将它们纳入你的配置中。

Nix是一个基于源代码的软件包管理器；如果在二进制缓存中没有预置的可用软件包，Nix将直接使用其定义从源代码中构建软件包。 它在一个沙盒式的 *纯* 环境中构建每个软件包，该环境尽可能地独立于主机系统，从而使二进制文件可以重现。

## 以匿名为重点的发行版

### Whonix

!!! recommendation

    ![Whonix logo](assets/img/linux-desktop/whonix.svg){ align=right }
    
    **Whonix** is based on [Kicksecure](#kicksecure), a security-focused fork of Debian. 它的目的是在互联网上提供隐私、安全和匿名性。 Whonix最好与[Qubes OS]（#qubes-os）一起使用。
    
    [:octicons-home-16: 主页](https://www.whonix.org/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://www.dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="洋葱服务" }
    [:octicons-info-16:](https://www.whonix.org/wiki/Documentation){ .card-link title=文档}
    [:octicons-heart-16:](https://www.whonix.org/wiki/Donate){ .card-link title=贡献 }

Whonix旨在作为两个虚拟机运行：一个 "工作站 "和一个Tor "网关"。 工作站的所有通信都必须通过Tor网关。 这意味着，即使工作站被某种恶意软件入侵，真实的IP地址仍然是隐藏的。

Some of its features include Tor Stream Isolation, [keystroke anonymization](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak), [encrypted swap](https://github.com/Whonix/swap-file-creator), and a hardened memory allocator. Future versions of Whonix will likely include [full system AppArmor policies](https://github.com/Whonix/apparmor-profile-everything) and a [sandbox app launcher](https://www.whonix.org/wiki/Sandbox-app-launcher) to fully confine all processes on the system.

Whonix is best used [in conjunction with Qubes](https://www.whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers). We have a [recommended guide](os/qubes-overview.md#connecting-to-tor-via-a-vpn) on configuring Whonix in conjunction with a VPN ProxyVM in Qubes to hide your Tor activities from your ISP.

### Tails

!!! recommendation

    ![Tails标志](assets/img/linux-desktop/tails.svg){ align=right }
    
    **Tails**是一个基于Debian的实时操作系统，它通过Tor路由所有的通信，它可以从DVD、U盘或SD卡安装在几乎任何电脑上启动。 它使用 [Tor]（tor.md）来保护隐私和匿名，同时规避审查制度，而且在关闭电源后，它不会在其使用的计算机上留下任何痕迹。
    
    [:octicons-home-16: 主页](https://tails.boum.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://tails.boum.org/doc/index.en.html){ .card-link title=文档}
    [:octicons-heart-16:](https://tails.boum.org/donate/){ .card-link title=贡献 }

Tails由于具有失忆功能（意味着没有任何东西被写入磁盘），对于反取证来说是非常好的；然而，它并不是像Whonix那样的加固发行版。 它缺乏Whonix所具有的许多匿名和安全功能，而且更新频率更低（每六周才更新一次）。 被恶意软件入侵的Tails系统可能会绕过透明代理，允许用户去匿名化。

Tails默认在Tor浏览器中包括 [uBlock Origin](desktop-browsers.md#ublock-origin) ，这有可能使对手更容易对Tails用户进行指纹识别。 [Whonix](desktop.md#whonix) 虚拟机可能更加防漏，然而它们不是失忆的，这意味着数据可能会从你的存储设备中恢复。

在设计上，Tails是为了在每次重启后完全重置自己。 加密的 [持久性存储](https://tails.boum.org/doc/persistent_storage/index.en.html) ，可以配置为在重启之间存储一些数据。

## 以安全为重点的发行版

### Qubes操作系统

!!! recommendation

    ![Qubes OS logo](assets/img/qubes/qubes_os.svg){ align=right }
    
    **Qubes OS** is an open-source operating system designed to provide strong security for desktop computing through secure virtual machines (or "qubes"). Qubes is based on Xen, the X Window System, and Linux. It can run most Linux applications and use most of the Linux drivers.
    
    [:octicons-home-16: Homepage](https://www.qubes-os.org/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://www.qubes-os.org/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://www.qubes-os.org/doc/){ .card-link title=Documentation }
    [:octicons-code-16:](https://github.com/QubesOS/){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.qubes-os.org/donate/){ .card-link title=Contribute }

Qubes OS secures the computer by isolating subsystems (e.g., networking, USB, etc.) and applications in separate *qubes*. Should one part of the system be compromised, the extra isolation is likely to protect the rest of the *qubes* and the core system.

For further information about how Qubes works, read our full [Qubes OS overview](os/qubes-overview.md) page.

### Kicksecure

While we [recommend against](os/linux-overview.md#release-cycle) "perpetually outdated" distributions like Debian for Desktop use in most cases, Kicksecure is a Debian-based operating system which has been hardened to be much more than a typical Linux install.

!!! recommendation

    ![Kicksecure logo](assets/img/linux-desktop/kicksecure.svg){ align=right }
    
    **Kicksecure**—in oversimplified terms—is a set of scripts, configurations, and packages that substantially reduce the attack surface of Debian. 它默认涵盖了大量的隐私和加固建议。 It also serves as the base OS for [Whonix](#whonix).
    
    [:octicons-home-16: Homepage](https://www.kicksecure.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.kicksecure.com/wiki/Privacy_Policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://www.kicksecure.com/wiki/Documentation){ .card-link title=Documentation }
    [:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.kicksecure.com/wiki/Donate){ .card-link title=Contribute }

## Criteria

Choosing a Linux distro that is right for you will come down to a huge variety of personal preferences, and this page is **not** meant to be an exhaustive list of every viable distribution. Our Linux overview page has some advice on [choosing a distro](os/linux-overview.md#choosing-your-distribution) in more detail. The distros on *this* page do all generally follow the guidelines we covered there, and all meet these standards:

- Free and open source.
- Receives regular software and kernel updates.
- [Avoids X11](os/linux-overview.md#wayland).
    - The notable exception here is Qubes, but the isolation issues which X11 typically has are avoided by virtualization. This isolation only applies to apps *running in different qubes* (virtual machines), apps running in the *same* qube are not protected from each other.
- Supports full-disk encryption during installation.
- Doesn't freeze regular releases for more than 1 year.
    - We [recommend against](os/linux-overview.md#release-cycle) "Long Term Support" or "stable" distro releases for desktop usage.
- Supports a wide variety of hardware.
- Preference towards larger projects.
    - Maintaining an operating system is a major challenge, and smaller projects have a tendency to make more avoidable mistakes, or delay critical updates (or worse, disappear entirely). We lean towards projects which will likely be around 10 years from now (whether that's due to corporate backing or very significant community support), and away from projects which are hand-built or have a small number of maintainers.

In addition, [our standard criteria](about/criteria.md) for recommended projects still applies. **Please note we are not affiliated with any of the projects we recommend.**
