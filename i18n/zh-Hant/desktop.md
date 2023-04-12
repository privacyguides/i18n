---
title: "桌上型電腦"
icon: simple/linux
description: 因為隱私保護和軟體自由，通常建議用 Linux發行版。
---

基於隱私保護和軟體自由，通常建議用 Linux 發行版。 如果您還不曾用過 Linux ，以下是我們建議可試試的發行版，以及一些 Linux發行版的隱私和安全提升技巧。

- [一般Linux 概述 :material-arrow-right-drop-circle:](os/linux-overview.md)

## 傳統發行版

### Fedora Workstation（Fedora 工作站）

!!! recommendation

    ! [Fedora logo] (assets/img/linux-desktop/fedora-workstation.svg) {align = right}
    
    * * Fedora Workstation * *是我們推薦給Linux新手的發行版。 Fedora 通常較其他發行版更早採用較新技術，例如 [Wayland](https://wayland.freedesktop.org/) ， [PipeWire](https://pipewire.org)。 這些新技術通常會在安全性、隱私性和可用性方面有所改善。
    
    [:octicons-home-16: Homepage](https://getfedora.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=Documentation}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribute }

Fedora 有一個半滾動的發布週期。 While some packages like [GNOME](https://www.gnome.org) are frozen until the next Fedora release, most packages (including the kernel) are updated frequently throughout the lifespan of the release. 每個 Fedora 版本支持一年，每6個月發布新版本。

### openSUSE Tumbleweed

!!! recommendation

    ! [openSUSE Tumbleweed logo] (assets/img/linux-desktop/opensuse-tumbleweed.svg) {align = right}
    
    * * openSUSE Tumbleweed * *是一個穩定滾動發行版。
    
    openSUSE Tumbleweed 有一個[transactional update] (https://kubic.opensuse.org/blog/2018-04-04-transactionalupdates/)系統，使用 [Btrfs](https://en.wikipedia.org/wiki/Btrfs)和 [Snapper](https://en.opensuse.org/openSUSE: Snapper_Tutorial)來確保快照可以在出現問題時回滾。
    
    [:octicons-home-16: Homepage](https://get.opensuse.org/tumbleweed/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://doc.opensuse.org/){ .card-link title=Documentation}
    [:octicons-heart-16:](https://shop.opensuse.org/){ .card-link title=Contribute }

Tumbleweed 遵循滾動發佈模式，每個更新都是快照發布。 當您升級系統時，會下載新的快照。 每個快照都通過一系列自動化測試，由 [openQA](https://openqa.opensuse.org) 運行，以確保其質量。

### Arch Linux

!!! recommendation

    ! [Arch logo] (assets/img/linux-desktop/archlinux.svg) {align = right}
    
    * * Arch Linux * *是一個輕量級的、自己動手(DIY)的發行版，意味著只能得到你安裝的東西。 如需更多資訊，請參閱他們的 [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions)。
    
    [:octicons-home-16: Homepage](https://archlinux.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://wiki.archlinux.org/){ .card-link title=Documentation}
    [:octicons-heart-16:](https://archlinux.org/donate/){ .card-link title=Contribute }

Arch Linux有一個滾動發佈週期。 沒有固定的發布時間表，套件經常更新。

作為 DIY 發行版，用戶需要 [自行設置與維護](os/linux-overview.md#arch-based-distributions) 系統。 Arch有一個 [官方安裝程式](https://wiki.archlinux.org/title/Archinstall) ，使安裝過程更容易。

[Arch Linux ](https://reproducible.archlinux.org) 大部份軟體包是 [可復制的](https://reproducible-builds.org)。

## Immutable Distributions

### Fedora Silverblue

!!! recommendation

    ![Fedora Silverblue logo](assets/img/linux-desktop/fedora-silverblue.svg){ align=right }
    
    **Fedora Silverblue** and **Fedora Kinoite** are immutable variants of Fedora with a strong focus on container workflows. Silverblue comes with the [GNOME](https://www.gnome.org/) desktop environment while Kinoite comes with [KDE](https://kde.org/). Silverblue and Kinoite follow the same release schedule as Fedora Workstation, benefiting from the same fast updates and staying very close to upstream.
    
    [:octicons-home-16: Homepage](https://silverblue.fedoraproject.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/fedora-silverblue/){ .card-link title=Documentation}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribute }

Silverblue (and Kinoite) differ from Fedora Workstation as they replace the [DNF](https://fedoraproject.org/wiki/DNF) package manager with a much more advanced alternative called [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/rawhide/system-administrators-guide/package-management/rpm-ostree/). The `rpm-ostree` package manager works by downloading a base image for the system, then overlaying packages over it in a [git](https://en.wikipedia.org/wiki/Git)-like commit tree. When the system is updated, a new base image is downloaded and the overlays will be applied to that new image.

After the update is complete you will reboot the system into the new deployment. `rpm-ostree` keeps two deployments of the system so that you can easily rollback if something breaks in the new deployment. There is also the option to pin more deployments as needed.

[Flatpak](https://www.flatpak.org) is the primary package installation method on these distributions, as `rpm-ostree` is only meant to overlay packages that cannot stay inside of a container on top of the base image.

As an alternative to Flatpaks, there is the option of [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox/) to create [Podman](https://podman.io) containers with a shared home directory with the host operating system and mimic a traditional Fedora environment, which is a [useful feature](https://containertoolbx.org) for the discerning developer.

### NixOS

!!! recommendation

    ![NixOS logo](assets/img/linux-desktop/nixos.svg){ align=right }
    
    NixOS is an independent distribution based on the Nix package manager with a focus on reproducibility and reliability.
    
    [:octicons-home-16: Homepage](https://nixos.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=Documentation}
    [:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=Contribute }

NixOS’s package manager keeps every version of every package in a different folder in the **Nix store**. Due to this you can have different versions of the same package installed on your system. After the package contents have been written to the folder, the folder is made read-only.

NixOS also provides atomic updates; first it downloads (or builds) the packages and files for the new system generation and then switches to it. There are different ways to switch to a new generation; you can tell NixOS to activate it after reboot or you can switch to it at runtime. You can also *test* the new generation by switching to it at runtime, but not setting it as the current system generation. If something in the update process breaks, you can just reboot and automatically and return to a working version of your system.

Nix the package manager uses a purely functional language - which is also called Nix - to define packages.

[Nixpkgs](https://github.com/nixos/nixpkgs) (the main source of packages) are contained in a single GitHub repository. You can also define your own packages in the same language and then easily include them in your config.

Nix is a source-based package manager; if there’s no pre-built available in the binary cache, Nix will just build the package from source using its definition. It builds each package in a sandboxed *pure* environment, which is as independent of the host system as possible, thus making binaries reproducible.

## 以匿名爲重點的發行版

### Whonix

!!! recommendation

    ![Whonix logo](assets/img/linux-desktop/whonix.svg){ align=right }
    
    **Whonix** is based on [Kicksecure](https://www.whonix.org/wiki/Kicksecure), a security-focused fork of Debian. It aims to provide privacy, security, and anonymity on the internet. Whonix is best used in conjunction with [Qubes OS](#qubes-os).
    
    [:octicons-home-16: Homepage](https://www.whonix.org/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://www.dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Onion Service" }
    [:octicons-info-16:](https://www.whonix.org/wiki/Documentation){ .card-link title=Documentation}
    [:octicons-heart-16:](https://www.whonix.org/wiki/Donate){ .card-link title=Contribute }

Whonix is meant to run as two virtual machines: a “Workstation” and a Tor “Gateway.” All communications from the Workstation must go through the Tor gateway. This means that even if the Workstation is compromised by malware of some kind, the true IP address remains hidden.

Some of its features include Tor Stream Isolation, [keystroke anonymization](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak), [encrypted swap](https://github.com/Whonix/swap-file-creator), and a hardened memory allocator.

Future versions of Whonix will likely include [full system AppArmor policies](https://github.com/Whonix/apparmor-profile-everything) and a [sandbox app launcher](https://www.whonix.org/wiki/Sandbox-app-launcher) to fully confine all processes on the system.

Whonix is best used [in conjunction with Qubes](https://www.whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers), Qubes-Whonix has various [disadvantages](https://forums.whonix.org/t/qubes-whonix-security-disadvantages-help-wanted/8581) when compared to other hypervisors.

### Tails

!!! recommendation

    ![Tails logo](assets/img/linux-desktop/tails.svg){ align=right }
    
    **Tails** is a live operating system based on Debian that routes all communications through Tor, which can boot on on almost any computer from a DVD, USB stick, or SD card installation. It uses [Tor](tor.md) to preserve privacy and anonymity while circumventing censorship, and it leaves no trace of itself on the computer it is used on after it is powered off.
    
    [:octicons-home-16: Homepage](https://tails.boum.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://tails.boum.org/doc/index.en.html){ .card-link title=Documentation}
    [:octicons-heart-16:](https://tails.boum.org/donate/){ .card-link title=Contribute }

Tails is great for counter forensics due to amnesia (meaning nothing is written to the disk); however, it is not a hardened distribution like Whonix. It lacks many anonymity and security features that Whonix has and gets updated much less often (only once every six weeks). A Tails system that is compromised by malware may potentially bypass the transparent proxy allowing for the user to be deanonymized.

Tails includes [uBlock Origin](desktop-browsers.md#ublock-origin) in Tor Browser by default, which may potentially make it easier for adversaries to fingerprint Tails users. [Whonix](desktop.md#whonix) virtual machines may be more leak-proof, however they are not amnesic, meaning data may be recovered from your storage device.

By design, Tails is meant to completely reset itself after each reboot. Encrypted [persistent storage](https://tails.boum.org/doc/persistent_storage/index.en.html) can be configured to store some data between reboots.

## 以安全爲重點的發行版

### Qubes OS

!!! recommendation

    ! [Qubes OS logo] (assets/img/qubes/qubes_os.svg) {align = right}
    
    * * Qubes OS * *是一個開源作業系統，旨在為桌機運算提供強大的安全性。 Qubes 基於 Xen、X Window System 和 Linux ，可以運行大多數 Linux 應用程式與使用大多數 Linux 驅動程式。
    
    [:octicons-home-16: Homepage](https://www.qubes-os.org/){ .md-button .md-button--primary }
    [:material-arrow-right-drop-circle: Overview](os/qubes-overview.md){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://www.qubes-os.org/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://www.qubes-os.org/doc/){ .card-link title=Documentation }
    [:octicons-code-16:](https://github.com/QubesOS/){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.qubes-os.org/donate/){ .card-link title=Contribute }

Qubes OS 是基於Xen 的作業系統，通過安全虛擬機器為桌機提供強大的安全性，（也稱為 *Qubes*）。

Qubes OS 作業系統將子系統（例如網絡、USB等）和應用程式隔離在個別的虛擬機器中以保護電腦。 如果系統的一部分被破壞，那麼額外的隔離可以保護系統其餘部分。 詳情請參閱Qubes [FAQ](https://www.qubes-os.org/faq/)。

## 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

!!! 示例“此部分是新的”

    我們正在努力為我們網站的每個部分建立定義的標準，這可能會有所變化。 如果您對我們的標準有任何疑問，請在[論壇上提問] (https://discuss.privacyguides.net/latest) ，如果沒有列出，請不要認為我們在提出建議時沒有考慮到某些事情。 當我們推薦一個項目時，有許多因素被考慮和討論，記錄每一個項目都是正在進行式。

我們推薦的作業系統：

- 必須是開源的。
- 必須定期接收軟體和Linux內核更新。
- Linux 發行版必須支援 [Wayland](os/linux-overview.md#Wayland)。
- 安裝時必須支援全磁碟加密。
- 不可將定期更新發佈凍結超過1年。 我們 [不建議](os/linux-overview.md#release-cycle) 桌機使用“長期支援”或“穩定”發行版。
- 需要支持各種各樣的硬體。
