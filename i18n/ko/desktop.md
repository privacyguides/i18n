---
title: "데스크톱/PC"
icon: simple/linux
description: 프라이버시 보호와 자유 소프트웨어를 이유로, 일반적으로 Linux 배포판이 권장됩니다.
cover: desktop.webp
---

프라이버시 보호와 자유 소프트웨어를 이유로, 일반적으로 Linux 배포판이 권장됩니다. 아직 Linux를 사용하지 않는 분을 위해, 사용해볼 만한 몇 가지 배포판을 추천드립니다. 대부분의 Linux 배포판에 적용 가능한 기본 프라이버시 및 보안 개선 안내도 찾아보실 수 있습니다.

- [Linux 기본 개요 :material-arrow-right-drop-circle:](os/linux-overview.md)

## 일반적인 배포판

### Fedora Workstation

!!! recommendation

    ![Fedora 로고](assets/img/linux-desktop/fedora-workstation.svg){ align=right }
    
    **Fedora Workstation**는 리눅스를 처음 사용하시는 분들에게 추천드리는 배포판입니다. Fedora는 보통 다른 배포판보다 먼저 최신 기술([Wayland](https://wayland.freedesktop.org/), [PipeWire](https://pipewire.org) 등)을 채택합니다. 최신 기술은 대개 보안, 프라이버시, 사용성을 개선하는 효과를 가져옵니다.
    
    [:octicons-home-16: Homepage](https://fedoraproject.org/workstation/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=Documentation}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribute }

Fedora는 반-롤링 릴리스 방식입니다. [GNOME](https://www.gnome.org) 등 일부 패키지는 다음 Fedora 릴리스 전까지 고정되지만, 커널을 포함한 대부분의 패키지는 릴리스 수명 기간 동안 자주 업데이트됩니다. 각각의 Fedora 릴리스는 1년간 지원되며, 6개월마다 새 버전이 출시됩니다.

### openSUSE Tumbleweed

!!! recommendation

    ![openSUSE Tumbleweed 로고](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }
    
    **openSUSE Tumbleweed**는 안정적인 롤링 릴리스 배포판입니다.
    
    openSUSE Tumbleweed에는 [Btrfs](https://en.wikipedia.org/wiki/Btrfs), [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial)를 사용한 [트랜잭션 업데이트](https://kubic.opensuse.org/blog/2018-04-04-transactionalupdates/) 시스템이 존재하기 때문에 문제가 발생할 경우 스냅샷 롤백이 가능합니다.
    
    [:octicons-home-16: 홈페이지](https://get.opensuse.org/tumbleweed/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://doc.opensuse.org/){ .card-link title=문서}
    [:octicons-heart-16:](https://shop.opensuse.org/){ .card-link title=기여 }

Tumbleweed는 각 업데이트가 배포판 스냅샷으로 릴리스되는 롤링 릴리스 방식입니다. 시스템을 업그레이드 할 경우, 새 스냅샷이 다운로드됩니다. 각각의 스냅샷은 [openQA](https://openqa.opensuse.org)에서 일련의 자동화된 테스트를 거쳐 품질이 보장됩니다.

### Arch Linux

!!! recommendation

    ![Arch 로고](assets/img/linux-desktop/archlinux.svg){ align=right }
    
    **Arch Linux**는 여러분이 원하는 것만 설치해서 사용할 수 있는, 간결함과 DIY(Do It Yourself) 특성을 지닌 배포판입니다. 자세한 내용은 Arch Linux [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions)를 참고해 주세요.
    
    [:octicons-home-16: 홈페이지](https://archlinux.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://wiki.archlinux.org/){ .card-link title=문서}
    [:octicons-heart-16:](https://archlinux.org/donate/){ .card-link title=기부 }

Arch Linux는 롤링 릴리스 방식입니다. 정해진 릴리스가 존재하지 않으며, 패키지는 매우 자주 업데이트됩니다.

DIY 배포판이므로 여러분은 자신의 시스템을 여러분 자신이 [직접 구성하고 관리](os/linux-overview.md#arch-based-distributions)해야 합니다. Arch Linux에는 설치 과정을 보다 쉽게 만들어주는 [공식 설치 프로그램](https://wiki.archlinux.org/title/Archinstall)이 존재합니다.

[Arch Linux의 패키지](https://reproducible.archlinux.org)는 대부분 [재현성](https://reproducible-builds.org)을 제공합니다.

## 변경 불가능한 배포판

### Fedora Silverblue

!!! recommendation

    ![Fedora Silverblue logo](assets/img/linux-desktop/fedora-silverblue.svg){ align=right }
    
    **Fedora Silverblue** is an immutable variant of Fedora with a strong focus on container workflows and the [GNOME](https://www.gnome.org/) desktop environment. If you prefer an environment other than GNOME, there are also other variants including [Kinoite](https://fedoraproject.org/kinoite/) (which comes with [KDE](https://kde.org/)) and [Sericea](https://fedoraproject.org/sericea/) (which comes with [Sway](https://swaywm.org/), a [Wayland](https://wayland.freedesktop.org)-only tiling window manager). We don't recommend [Onyx](https://fedoraproject.org/onyx/) at this time as it still [requires X11](https://buddiesofbudgie.org/blog/wayland). All of these variants follow the same release schedule as Fedora Workstation, benefiting from the same fast updates and staying very close to upstream.
    
    [:octicons-home-16: Homepage](https://fedoraproject.org/silverblue/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/fedora-silverblue/){ .card-link title=Documentation}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribute }

Silverblue and its variants differ from Fedora Workstation as they replace the [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf/) package manager with a much more advanced alternative called [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/package-management/rpm-ostree/). `rpm-ostree` 패키지 관리자는 시스템의 베이스 이미지를 다운로드한 이후 [git](https://en.wikipedia.org/wiki/Git)과 유사한 커밋 트리에서 패키지를 오버레이하는 방식으로 작동합니다. 시스템을 업데이트하는 경우, 새로운 베이스 이미지를 다운로드하고 해당 이미지에 오버레이합니다.

업데이트가 완료되면 새로 만들어진 시스템으로 재부팅합니다. `rpm-ostree`는 두 개의 시스템을 모두 유지하므로, 새로 배포된 시스템에서 문제가 발생하는 경우 간단히 롤백할 수 있습니다. 필요에 따라 유지할 시스템 수를 더 늘리는 옵션도 존재합니다.

[Flatpak](https://www.flatpak.org) is the primary package installation method on these distributions, as `rpm-ostree` is only meant to overlay packages that cannot stay inside of a container on top of the base image.

As an alternative to Flatpaks, there is the option of [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox/) to create [Podman](https://podman.io) containers with a shared home directory with the host operating system and mimic a traditional Fedora environment, which is a [useful feature](https://containertoolbx.org) for the discerning developer.

### NixOS

!!! recommendation

    ![NixOS 로고](assets/img/linux-desktop/nixos.svg){ align=right }
    
    NixOS는 재현성과 안전성에 중점을 둔 Nix 패키지 관리자를 기반으로 하는 독립 배포판입니다.
    
    [:octicons-home-16: 홈페이지](https://nixos.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=문서}
    [:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=기부 }

NixOS 패키지 매니저는 모든 패키지의 모든 버전을 **Nix Store**의 폴더에 따로 보관합니다. 따라서, 동일한 하나의 패키지를 시스템에 여러 버전으로 설치할 수 있습니다. 패키지 내용이 폴더에 작성되면 해당 폴더는 읽기 전용으로 설정됩니다.

NixOS also provides atomic updates; first it downloads (or builds) the packages and files for the new system generation and then switches to it. There are different ways to switch to a new generation; you can tell NixOS to activate it after reboot or you can switch to it at runtime. You can also *test* the new generation by switching to it at runtime, but not setting it as the current system generation. If something in the update process breaks, you can just reboot and automatically and return to a working version of your system.

Nix the package manager uses a purely functional language - which is also called Nix - to define packages.

[Nixpkgs](https://github.com/nixos/nixpkgs) (the main source of packages) are contained in a single GitHub repository. You can also define your own packages in the same language and then easily include them in your config.

Nix is a source-based package manager; if there’s no pre-built available in the binary cache, Nix will just build the package from source using its definition. It builds each package in a sandboxed *pure* environment, which is as independent of the host system as possible, thus making binaries reproducible.

## 익명성 중점 배포판

### Whonix

!!! recommendation

    ![Whonix logo](assets/img/linux-desktop/whonix.svg){ align=right }
    
    **Whonix** is based on [Kicksecure](#kicksecure), a security-focused fork of Debian. It aims to provide privacy, security, and anonymity on the internet. Whonix is best used in conjunction with [Qubes OS](#qubes-os).
    
    [:octicons-home-16: 홈페이지](https://www.whonix.org/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://www.dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Onion 서비스" }
    [:octicons-info-16:](https://www.whonix.org/wiki/Documentation){ .card-link title=문서}
    [:octicons-heart-16:](https://www.whonix.org/wiki/Donate){ .card-link title=기부 }

Whonix는 'Workstation'과 Tor 'Gateway'라는 두 개의 가상 머신으로 구성되어 실행됩니다. Workstation 에서 발생하는 모든 통신은 반드시 Tor Gateway를 통과합니다. 즉, Workstation이 만약 멀웨어에 의해 손상된다 할지라도, 실제 IP 주소는 노출되지 않습니다.

Some of its features include Tor Stream Isolation, [keystroke anonymization](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak), [encrypted swap](https://github.com/Whonix/swap-file-creator), and a hardened memory allocator. Future versions of Whonix will likely include [full system AppArmor policies](https://github.com/Whonix/apparmor-profile-everything) and a [sandbox app launcher](https://www.whonix.org/wiki/Sandbox-app-launcher) to fully confine all processes on the system.

Whonix is best used [in conjunction with Qubes](https://www.whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers). We have a [recommended guide](os/qubes-overview.md#connecting-to-tor-via-a-vpn) on configuring Whonix in conjunction with a VPN ProxyVM in Qubes to hide your Tor activities from your ISP.

### Tails

!!! recommendation

    ![Tails logo](assets/img/linux-desktop/tails.svg){ align=right }
    
    **Tails** is a live operating system based on Debian that routes all communications through Tor, which can boot on on almost any computer from a DVD, USB stick, or SD card installation. It uses [Tor](tor.md) to preserve privacy and anonymity while circumventing censorship, and it leaves no trace of itself on the computer it is used on after it is powered off.
    
    [:octicons-home-16: 홈페이지](https://tails.boum.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://tails.boum.org/doc/index.en.html){ .card-link title=문서}
    [:octicons-heart-16:](https://tails.boum.org/donate/){ .card-link title=기부 }

Tails는 휘발성(디스크에 아무것도 기록되지 않음) 특성으로 인해 포렌식 방어에 적합하지만, Whonix 처럼 특별히 보안이 강화된 배포판은 아닙니다. Whonix에 비해 많은 익명성, 보안 기능이 부족하며, 업데이트 빈도 또한 훨씬 낮습니다(Tails는 6주에 한 번 업데이트가 제공됩니다). A Tails system that is compromised by malware may potentially bypass the transparent proxy allowing for the user to be deanonymized.

Tails는 Tor 브라우저에 [uBlock Origin](desktop-browsers.md#ublock-origin)을 기본 탑재하고 있습니다. 이는 공격자가 Tails 사용자를 핑거프린팅하는 용도로 쓰일 수 있습니다. [Whonix](desktop.md#whonix) 가상 머신은 유출 방지 면에서는 더 뛰어나지만, 휘발성 특성이 없으므로 저장 장치에서 데이터를 복구하는 것이 가능할 수도 있습니다.

Tails는 재부팅 시마다 완전히 초기화되도록 설계되었습니다. 재부팅 시에도 특정 데이터를 유지하려면 암호화 [영구 저장소](https://tails.boum.org/doc/persistent_storage/index.en.html)를 설정해야 합니다.

## 보안성 중점 배포판

### Qubes OS

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
    
    **Kicksecure**—in oversimplified terms—is a set of scripts, configurations, and packages that substantially reduce the attack surface of Debian. It covers a lot of privacy and hardening recommendations by default. It also serves as the base OS for [Whonix](#whonix).
    
    [:octicons-home-16: Homepage](https://www.kicksecure.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.kicksecure.com/wiki/Privacy_Policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://www.kicksecure.com/wiki/Documentation){ .card-link title=Documentation }
    [:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.kicksecure.com/wiki/Donate){ .card-link title=Contribute }

## 평가 기준

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
