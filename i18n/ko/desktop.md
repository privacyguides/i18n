---
title: "데스크톱/PC"
icon: simple/linux
description: Linux distributions are commonly recommended for privacy protection and software freedom.
cover: desktop.png
---

Linux distributions are commonly recommended for privacy protection and software freedom. If you don't already use Linux, below are some distributions we suggest trying out, as well as some general privacy and security improvement tips that are applicable to many Linux distributions.

- [General Linux Overview :material-arrow-right-drop-circle:](os/linux-overview.md)

## Traditional Distributions

### Fedora Workstation

!!! recommendation

    ![Fedora 로고](assets/img/linux-desktop/fedora-workstation.svg){ align=right }
    
    **Fedora Workstation**는 리눅스를 처음 사용하시는 분들에게 추천드리는 배포판입니다. Fedora는 보통 다른 배포판보다 먼저 최신 기술([Wayland](https://wayland.freedesktop.org/), [PipeWire](https://pipewire.org) 등)을 채택합니다. 최신 기술은 대개 보안, 프라이버시, 사용성을 개선하는 효과를 가져옵니다.
    
    [:octicons-home-16: 홈페이지](https://getfedora.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=문서}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=기여 }

Fedora는 반-롤링 릴리스 방식입니다. [GNOME](https://www.gnome.org) 등 일부 패키지는 다음 Fedora 릴리스 전까지 고정되지만, 커널을 포함한 대부분의 패키지는 릴리스 수명 기간 동안 자주 업데이트됩니다. 각각의 Fedora 릴리스는 1년간 지원되며, 6개월마다 새 버전이 출시됩니다.

### openSUSE Tumbleweed

!!! recommendation

    ![openSUSE Tumbleweed 로고](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }
    
    **openSUSE Tumbleweed**는 안정적인 롤링 릴리스 배포판입니다.
    
    openSUSE Tumbleweed has a [transactional update](https://kubic.opensuse.org/blog/2018-04-04-transactionalupdates/) system that uses [Btrfs](https://en.wikipedia.org/wiki/Btrfs) and [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) to ensure that snapshots can be rolled back should there be a problem.
    
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
    
    **Fedora Silverblue** and **Fedora Kinoite** are immutable variants of Fedora with a strong focus on container workflows. Silverblue comes with the [GNOME](https://www.gnome.org/) desktop environment while Kinoite comes with [KDE](https://kde.org/). Silverblue and Kinoite follow the same release schedule as Fedora Workstation, benefiting from the same fast updates and staying very close to upstream.
    
    [:octicons-home-16: 홈페이지](https://silverblue.fedoraproject.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/fedora-silverblue/){ .card-link title=문서}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=기여 }

Fedora Workstation과의 차이점은, Silverblue, Kinoite는 [DNF](https://fedoraproject.org/wiki/DNF) 패키지 관리자를 사용하는 것이 아닌, [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/rawhide/system-administrators-guide/package-management/rpm-ostree/)라는 발전된 대체제를 사용합니다. The `rpm-ostree` package manager works by downloading a base image for the system, then overlaying packages over it in a [git](https://en.wikipedia.org/wiki/Git)-like commit tree. When the system is updated, a new base image is downloaded and the overlays will be applied to that new image.

After the update is complete you will reboot the system into the new deployment. `rpm-ostree` keeps two deployments of the system so that you can easily rollback if something breaks in the new deployment. There is also the option to pin more deployments as needed.

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
    
    **Whonix** is based on [Kicksecure](https://www.whonix.org/wiki/Kicksecure), a security-focused fork of Debian. It aims to provide privacy, security, and anonymity on the internet. Whonix is best used in conjunction with [Qubes OS](#qubes-os).
    
    [:octicons-home-16: 홈페이지](https://www.whonix.org/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://www.dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Onion 서비스" }
    [:octicons-info-16:](https://www.whonix.org/wiki/Documentation){ .card-link title=문서}
    [:octicons-heart-16:](https://www.whonix.org/wiki/Donate){ .card-link title=기부 }

Whonix는 'Workstation'과 Tor 'Gateway'라는 두 개의 가상 머신으로 구성되어 실행됩니다. Workstation 에서 발생하는 모든 통신은 반드시 Tor Gateway를 통과합니다. 즉, Workstation이 만약 멀웨어에 의해 손상된다 할지라도, 실제 IP 주소는 노출되지 않습니다.

Whonix는 다양한 기능을 제공합니다. 예시로는 Tor 스트림 격리, [키 입력 익명화](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak), [암호화 Swap](https://github.com/Whonix/swap-file-creator), 메모리 할당 보안 강화 등이 있습니다.

Whonix 향후 버전에서는 [전체 시스템 AppArmor 정책](https://github.com/Whonix/apparmor-profile-everything), [샌드박스 앱 런처](https://www.whonix.org/wiki/Sandbox-app-launcher) 등 시스템 내 모든 프로세스의 완전한 격리가 추가될 예정입니다.

Whonix는 [Qubes와 결합해 사용하는 것이 가장 뛰어납니다](https://www.whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers). 하지만, Qubes-Whonix는 다른 하이퍼바이저와 비교했을 때 [여러 단점](https://forums.whonix.org/t/qubes-whonix-security-disadvantages-help-wanted/8581) 또한 가지고 있습니다.

### Tails

!!! recommendation

    ![Tails logo](assets/img/linux-desktop/tails.svg){ align=right }
    
    **Tails** is a live operating system based on Debian that routes all communications through Tor, which can boot on on almost any computer from a DVD, USB stick, or SD card installation. It uses [Tor](tor.md) to preserve privacy and anonymity while circumventing censorship, and it leaves no trace of itself on the computer it is used on after it is powered off.
    
    [:octicons-home-16: 홈페이지](https://tails.boum.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://tails.boum.org/doc/index.en.html){ .card-link title=문서}
    [:octicons-heart-16:](https://tails.boum.org/donate/){ .card-link title=기부 }

Tails is great for counter forensics due to amnesia (meaning nothing is written to the disk); however, it is not a hardened distribution like Whonix. It lacks many anonymity and security features that Whonix has and gets updated much less often (only once every six weeks). A Tails system that is compromised by malware may potentially bypass the transparent proxy allowing for the user to be deanonymized.

Tails includes [uBlock Origin](desktop-browsers.md#ublock-origin) in Tor Browser by default, which may potentially make it easier for adversaries to fingerprint Tails users. [Whonix](desktop.md#whonix) virtual machines may be more leak-proof, however they are not amnesic, meaning data may be recovered from your storage device.

By design, Tails is meant to completely reset itself after each reboot. Encrypted [persistent storage](https://tails.boum.org/doc/persistent_storage/index.en.html) can be configured to store some data between reboots.

## 보안성 중점 배포판

### Qubes OS

!!! recommendation

    ![Qubes OS logo](assets/img/qubes/qubes_os.svg){ align=right }
    
    **Qubes OS** is an open-source operating system designed to provide strong security for desktop computing. Qubes is based on Xen, the X Window System, and Linux, and can run most Linux applications and use most of the Linux drivers.
    
    [:octicons-home-16: 홈페이지](https://www.qubes-os.org/){ .md-button .md-button--primary }
    [:material-arrow-right-drop-circle: 개요](os/qubes-overview.md){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://www.qubes-os.org/privacy/){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://www.qubes-os.org/doc/){ .card-link title=문서 }
    [:octicons-code-16:](https://github.com/QubesOS/){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://www.qubes-os.org/donate/){ .card-link title=기부 }

Qubes OS is a Xen-based operating system meant to provide strong security for desktop computing through secure virtual machines (VMs), also known as *Qubes*.

The Qubes OS operating system secures the computer by isolating subsystems (e.g., networking, USB, etc.) and applications in separate VMs. Should one part of the system be compromised, the extra isolation is likely to protect the rest of the system. For further details see the Qubes [FAQ](https://www.qubes-os.org/faq/).

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

!!! example "이 단락은 최근에 만들어졌습니다"

    Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

Privacy Guides 권장 운영 체제는 다음 조건을 만족해야 합니다:

- 오픈 소스여야 합니다.
- 소프트웨어 및 Linux 커널 업데이트를 정기적으로 받아야 합니다.
- Linux 배포판은 [Wayland](os/linux-overview.md#Wayland)를 지원해야 합니다.
- 설치 과정에서 전체 디스크 암호화를 지원해야 합니다.
- 정기 릴리스가 1년 이상 고정되어선 안됩니다. Privacy Guides 데스크톱 사용에 있어서 'LTS(Long Term Support, 장기 지원)'이나 'Stable(안정적인)' 릴리스 배포판을 [권장하지 않습니다](os/linux-overview.md#release-cycle).
- 다양한 하드웨어를 지원해야 합니다.
