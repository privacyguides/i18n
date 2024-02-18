---
title: "桌上型電腦"
icon: simple/linux
description: 基於隱私保護和軟體自由，通常建議用 Linux 發行版。
cover: desktop.webp
---

基於隱私保護和軟體自由，通常建議用 Linux 發行版。 如果您還不曾用過 Linux ，以下是我們建議可試試的發行版，以及一些 Linux發行版的隱私和安全提升技巧。

- [一般Linux 概述 :material-arrow-right-drop-circle:](os/linux-overview.md)

## 傳統發行版

### Fedora Workstation（Fedora 工作站）

<div class="admonition recommendation" markdown>

![Fedora logo](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Workstation** is our recommended distribution for people new to Linux. Fedora 通常較其他發行版更早採用較新技術，例如 [Wayland](https://wayland.freedesktop.org/) ， [PipeWire](https://pipewire.org)。 這些新技術通常會在安全性、隱私性和可用性方面有所改善。

[:octicons-home-16: Homepage](https://fedoraproject.org/workstation/){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=Documentation}
[:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribute }

</details>

</div>

Fedora 有一個半滾動的發布週期。 雖然像 [GNOME](https://www.gnome.org) 這樣的套件在下一個Fedora發布之前會被凍結，但大多數套件（包括內核）在該版的整個生命週期中都會頻繁更新。 每個 Fedora 版本支持一年，每6個月發布新版本。

### openSUSE Tumbleweed

<div class="admonition recommendation" markdown>

![openSUSE Tumbleweed logo](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }

**openSUSE Tumbleweed** 是一個穩定滾動發行版。

openSUSE Tumbleweed 有一個 [transactional update](https://kubic.opensuse.org/blog/2018-04-04-transactionalupdates/)系統，使用 [Btrfs](https://en.wikipedia.org/wiki/Btrfs)和 [Snapper](https://en.opensuse.org/openSUSE: Snapper_Tutorial)來確保快照可以在出現問題時回滾。

[:octicons-home-16: Homepage](https://get.opensuse.org/tumbleweed/){ .md-button .md-button--primary }
[:octicons-info-16:](https://doc.opensuse.org/){ .card-link title=Documentation}
[:octicons-heart-16:](https://shop.opensuse.org/){ .card-link title=Contribute }

</details>

</div>

Tumbleweed 遵循滾動發佈模式，每個更新都是快照發布。 當您升級系統時，會下載新的快照。 每個快照都通過一系列自動化測試，由 [openQA](https://openqa.opensuse.org) 運行，以確保其質量。

### Arch Linux

<div class="admonition recommendation" markdown>

![Arch logo](assets/img/linux-desktop/archlinux.svg){ align=right }

**Arch Linux** 是一個輕量級的、自己動手(DIY)的發行版，意味著只能得到你安裝的東西。 如需更多資訊，請參閱他們的 [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions)。

[:octicons-home-16: Homepage](https://archlinux.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.archlinux.org/){ .card-link title=Documentation}
[:octicons-heart-16:](https://archlinux.org/donate/){ .card-link title=Contribute }

</details>

</div>

Arch Linux有一個滾動發佈週期。 沒有固定的發布時間表，套件經常更新。

作為 DIY 發行版，用戶需要 [自行設置與維護](os/linux-overview.md#arch-based-distributions) 系統。 Arch有一個 [官方安裝程式](https://wiki.archlinux.org/title/Archinstall) ，使安裝過程更容易。

[Arch Linux ](https://reproducible.archlinux.org) 大部份軟體包是 [可復制的](https://reproducible-builds.org)。

## Atomic Distributions

**Atomic distributions** (sometimes also referred to as **immutable distributions**) are operating systems which handle package installation and updates by layering changes atop your core system image, rather than by directly modifying the system. This has advantages including increased stability and the ability to easily rollback updates. See [*Traditional vs. Atomic Updates*](os/linux-overview.md#traditional-vs-atomic-updates) for more info.

### Fedora Atomic Desktops

<div class="admonition recommendation" markdown>

![Fedora logo](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Atomic Desktops** are variants of Fedora which use the `rpm-ostree` package manager and have a strong focus on containerized workflows and Flatpak for desktop applications. 這些變體版都遵循 Fedora Workstation 同樣的發佈時間表，受益於相同的快速更新並保持非常接近上遊。

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

NixOS 是基於 Nix套件管理器的獨立發行版，專注於可重複性和可靠性。

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

## 以匿名爲重點的發行版

### Whonix

<div class="admonition recommendation" markdown>

![Whonix logo](assets/img/linux-desktop/whonix.svg){ align=right }

**Whonix** 為基於 [Kicksecure](#kicksecure) 專注在安全的 Debian 分支系統。 它旨在提供網際網路的隱私、安全和匿名性。 Whonix 最好與 [Qubes OS](# qubes-os) 配合使用。

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

![Tails logo](assets/img/linux-desktop/tails.svg){ align=right }

**Tails** 是一個基於Debian 的自生作業系統，通過 Tor 路由所有通訊，透過 DVD ， USB記憶棒或 SD卡安裝幾乎可在任何電腦上啟動。 它使用 [Tor](tor.md) 來保護隱私和匿名性，同時規避審查制度，並且使用的電腦在關閉電源後不會留下任何痕跡。

[:octicons-home-16: Homepage](https://tails.boum.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://tails.boum.org/doc/index.en.html){ .card-link title=Documentation}
[:octicons-heart-16:](https://tails.boum.org/donate/){ .card-link title=Contribute }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning "警告"</p>

Tails [doesn't erase](https://gitlab.tails.boum.org/tails/tails/-/issues/5356) the [video memory](https://en.wikipedia.org/wiki/Dual-ported_video_RAM) when shutting down. When you restart your computer after using Tails, it might briefly display the last screen that was displayed in Tails. If you shut down your computer instead of restarting it, the video memory will erase itself automatically after being unpowered for some time.

</div>

Tails is great for counter forensics due to amnesia (meaning nothing is written to the disk); however, it is not a hardened distribution like Whonix. It lacks many anonymity and security features that Whonix has and gets updated much less often (only once every six weeks). A Tails system that is compromised by malware may potentially bypass the transparent proxy allowing for the user to be deanonymized.

Tails includes [uBlock Origin](desktop-browsers.md#ublock-origin) in Tor Browser by default, which may potentially make it easier for adversaries to fingerprint Tails users. [Whonix](desktop.md#whonix) virtual machines may be more leak-proof, however they are not amnesic, meaning data may be recovered from your storage device.

By design, Tails is meant to completely reset itself after each reboot. Encrypted [persistent storage](https://tails.boum.org/doc/persistent_storage/index.en.html) can be configured to store some data between reboots.

## 以安全爲重點的發行版

### Qubes OS

<div class="admonition recommendation" markdown>

![Qubes OS logo](assets/img/qubes/qubes_os.svg){ align=right }

**Qubes OS** 是開源作業系統，利用安全的虛擬器為桌面運算提供更強的安全性 (或稱"qubes"). Qubes 基於 Xen, X Window 系統與 Linux。 大多數 Linux 應用它都可以執行且適用 Linux 驅動。

[:octicons-home-16: Homepage](https://www.qubes-os.org/){ .md-button .md-button--primary }
[:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://www.qubes-os.org/privacy/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://www.qubes-os.org/doc/){ .card-link title=Documentation }
[:octicons-code-16:](https://github.com/QubesOS/){ .card-link title="Source Code" }
[:octicons-heart-16:](https://www.qubes-os.org/donate/){ .card-link title=Contribute }

</details>

</div>

Qubes OS secures the computer by isolating subsystems (e.g., networking, USB, etc.) and applications in separate *qubes*. Should one part of the system be compromised, the extra isolation is likely to protect the rest of the *qubes* and the core system.

For further information about how Qubes works, read our full [Qubes OS overview](os/qubes-overview.md) page.

### Kicksecure

While we [recommend against](os/linux-overview.md#release-cycle) "perpetually outdated" distributions like Debian for Desktop use in most cases, Kicksecure is a Debian-based operating system which has been hardened to be much more than a typical Linux install.

<div class="admonition recommendation" markdown>

![Kicksecure logo](assets/img/linux-desktop/kicksecure.svg){ align=right }

**Kicksecure**—其簡化的介紹—可以說是一組腳本、置配與套件的組合，可大幅減少 Debian 的攻擊面。 它預設覆蓋了大量的隱私和加固建議。 它也是 [Whonix](#whonix) 的基礎作業系統。

[:octicons-home-16: Homepage](https://www.kicksecure.com/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.kicksecure.com/wiki/Privacy_Policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://www.kicksecure.com/wiki/Documentation){ .card-link title=Documentation }
[:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Source Code" }
[:octicons-heart-16:](https://www.kicksecure.com/wiki/Donate){ .card-link title=Contribute }

</details>

</div>

## 標準

Choosing a Linux distro that is right for you will come down to a huge variety of personal preferences, and this page is **not** meant to be an exhaustive list of every viable distribution. Our Linux overview page has some advice on [choosing a distro](os/linux-overview.md#choosing-your-distribution) in more detail. The distros on *this* page do all generally follow the guidelines we covered there, and all meet these standards:

- 免費且開放原始碼。
- 必須定期接收軟體和內核更新。
- [Avoids X11](os/linux-overview.md#wayland).
    - 這裡值得注意的例外是 Qubes，但虛擬化可以避免 X11 常發生的隔離問題。 其隔離僅適用於*在不同 qube*（虛擬機）中運行的應用程式，在*同一個* qube 運行的應用程式則無法保護。
- 安裝時必須支援全磁碟加密。
- 不可將定期更新發佈凍結超過1年。
    - 我們 [不建議](os/linux-overview.md#release-cycle) 桌機使用“長期支援”或“穩定”發行版。
- 需要支持各種各樣的硬體。
- 偏好較大型的專案。
    - 維護作業系統是一項大挑戰，小型專案往往會犯更多可避免的錯誤，或延遲重大更新（或更糟糕的是，很快就完全消失）。 我們傾向於至少可維持10 年的專案（無論是由於公司支持還是非常重要的社區支持），而不是手工構建或只有少數維護人員的專案。

In addition, [our standard criteria](about/criteria.md) for recommended projects still applies. **Please note we are not affiliated with any of the projects we recommend.**
