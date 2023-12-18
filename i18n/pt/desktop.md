---
title: "Desktop/PC"
icon: fontawesome/brands/linux
description: Linux distributions are commonly recommended for privacy protection and software freedom.
cover: desktop.webp
---

Linux distributions are commonly recommended for privacy protection and software freedom. If you don't already use Linux, below are some distributions we suggest trying out, as well as some general privacy and security improvement tips that are applicable to many Linux distributions.

- [General Linux Overview :material-arrow-right-drop-circle:](os/linux-overview.md)

## Distribuições Tradicionais

### Estação de Trabalho Fedora

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![logotipo Fedora](/assets/img/linux-desktop/fedora-workstation.svg){ align=right }
    
    **Fedora Workstation** é a nossa distribuição recomendada para usuários novos no Linux. A Fedora geralmente adota novas tecnologias antes de outras distribuições, por exemplo, [Wayland](https://wayland.freedesktop.org/), [PipeWire](https://pipewire.org), e em breve, [FS-Verity](https://fedoraproject.org/wiki/Changes/FsVerityRPM). Estas novas tecnologias muitas vezes vêm com melhorias na segurança, privacidade e usabilidade em geral.
    
    [:octicons-home-16: Homepage](https://fedoraproject.org/workstation/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=Documentation}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribute }

Fedora has a semi-rolling release cycle. While some packages like [GNOME](https://www.gnome.org) are frozen until the next Fedora release, most packages (including the kernel) are updated frequently throughout the lifespan of the release. Each Fedora release is supported for one year, with a new version released every 6 months.

### openSUSE Tumbleweed

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![logotipo do openSUSE Tumbleweed](/assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }
    
    **openSUSE Tumbleweed** é uma distribuição estável [lançamento rolante](https://en.wikipedia.org/wiki/Rolling_release).
    
    O openSUSE Tumbleweed tem um sistema [transactional update](https://kubic.opensuse.org/blog/2018-04-04-transactionalupdates/) que usa [Btrfs](https://en.wikipedia.org/wiki/Btrfs) e [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) para garantir que os instantâneos possam ser rolados de volta caso haja algum problema.
    
    [Visite get.opensuse.org](https://get.opensuse.org/tumbleweed/){ .md-button .md-button--primary }

Tumbleweed follows a rolling release model where each update is released as a snapshot of the distribution. When you upgrade your system, a new snapshot is downloaded. Each snapshot is run through a series of automated tests by [openQA](https://openqa.opensuse.org) to ensure its quality.

### Arco Linux

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Arch logo](/assets/img/linux-desktop/archlinux.svg){ align=right }
    
    **Arch Linux** é uma distribuição leve, faça-você-mesmo (faça você mesmo), o que significa que você só recebe o que você instala. Para mais informações consulte o seu [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions).
    
    [Visite archlinux.org](https://archlinux.org/){ .md-button .md-button--primary }

Sendo uma distribuição DIY, o usuário é [esperado para configurar e manter](/linux-desktop/#arch-based-distributions) seu sistema. Arch tem um [instalador oficial](https://wiki.archlinux.org/title/Archinstall) para tornar o processo de instalação um pouco mais fácil.

Being a DIY distribution, you are [expected to set up and maintain](os/linux-overview.md#arch-based-distributions) your system on your own. Arch has an [official installer](https://wiki.archlinux.org/title/Archinstall) to make the installation process a little easier.

A large portion of [Arch Linux’s packages](https://reproducible.archlinux.org) are [reproducible](https://reproducible-builds.org).

## Distribuições imutáveis

### Fedora Silverblue

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Fedora Silverblue logo](assets/img/linux-desktop/fedora-silverblue.svg){ align=right }
    
    **Fedora Silverblue** is an immutable variant of Fedora with a strong focus on container workflows and the [GNOME](https://www.gnome.org/) desktop environment. If you prefer an environment other than GNOME, there are also other variants including [Kinoite](https://fedoraproject.org/kinoite/) (which comes with [KDE](https://kde.org/)) and [Sericea](https://fedoraproject.org/sericea/) (which comes with [Sway](https://swaywm.org/), a [Wayland](https://wayland.freedesktop.org)-only tiling window manager). We don't recommend [Onyx](https://fedoraproject.org/onyx/) at this time as it still [requires X11](https://buddiesofbudgie.org/blog/wayland). All of these variants follow the same release schedule as Fedora Workstation, benefiting from the same fast updates and staying very close to upstream.
    
    [:octicons-home-16: Homepage](https://fedoraproject.org/silverblue/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/fedora-silverblue/){ .card-link title=Documentation}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribute }

Silverblue and its variants differ from Fedora Workstation as they replace the [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf/) package manager with a much more advanced alternative called [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/package-management/rpm-ostree/). `rpm-ostree` mantém duas implantações do sistema para que um usuário possa facilmente reverter se algo quebrar na nova implantação. Há também a opção de fixar mais implantações conforme necessário.

After the update is complete you will reboot the system into the new deployment. `rpm-ostree` keeps two deployments of the system so that you can easily rollback if something breaks in the new deployment. There is also the option to pin more deployments as needed.

Como alternativa aos Flatpaks, existe a opção de [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox/) para criar [Podman](https://podman.io) containers com um diretório home compartilhado com o sistema operacional host e imitar um ambiente Fedora tradicional, que é um [recurso útil](https://containertoolbx.org) para o desenvolvedor perspicaz.

As an alternative to Flatpaks, there is the option of [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox/) to create [Podman](https://podman.io) containers with a shared home directory with the host operating system and mimic a traditional Fedora environment, which is a [useful feature](https://containertoolbx.org) for the discerning developer.

### NixOS

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![logo NixOS](/assets/img/linux-desktop/nixos.svg){ align=right }
    
    NixOS é uma distribuição independente baseada no gerenciador de pacotes Nix com foco na reprodutibilidade e confiabilidade.
    
    [Visite nixos.org](https://nixos.org/){ .md-button .md-button--primary }

O NixOS também fornece atualizações atômicas; primeiro ele baixa (ou constrói) os pacotes e arquivos para a nova geração do sistema e depois muda para ele. Existem diferentes maneiras de mudar para uma nova geração; você pode dizer ao NixOS para ativá-lo após o reinício ou você pode mudar para ele em tempo de execução. Você também pode *testar* a nova geração mudando para ela em tempo de execução, mas não definindo-a como a geração atual do sistema.

NixOS also provides atomic updates; first it downloads (or builds) the packages and files for the new system generation and then switches to it. There are different ways to switch to a new generation; you can tell NixOS to activate it after reboot or you can switch to it at runtime. You can also *test* the new generation by switching to it at runtime, but not setting it as the current system generation. If something in the update process breaks, you can just reboot and automatically and return to a working version of your system.

Nix the package manager uses a purely functional language - which is also called Nix - to define packages.

Nix é um gerenciador de pacotes baseado no código fonte; se não houver um pré-cache binário disponível, Nix irá apenas construir o pacote a partir do código fonte usando sua definição. Ele constrói cada pacote em um ambiente sandboxed *puro* , que é o mais independente possível do sistema hospedeiro, tornando assim os binários reprodutíveis.

Nix is a source-based package manager; if there’s no pre-built available in the binary cache, Nix will just build the package from source using its definition. It builds each package in a sandboxed *pure* environment, which is as independent of the host system as possible, thus making binaries reproducible.

## Distribuições Anónimas-Focusadas

### Whonix

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Whonix logo](assets/img/linux-desktop/whonix.svg){ align=right }
    
    **Whonix** is based on [Kicksecure](#kicksecure), a security-focused fork of Debian. O seu objectivo é proporcionar privacidade, segurança e anonimato na Internet. Whonix is best used in conjunction with [Qubes OS](#qubes-os).
    
    [:octicons-home-16: Homepage](https://www.whonix.org/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://www.dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Onion Service" }
    [:octicons-info-16:](https://www.whonix.org/wiki/Documentation){ .card-link title=Documentation}
    [:octicons-heart-16:](https://www.whonix.org/wiki/Donate){ .card-link title=Contribute }

Whonix is meant to run as two virtual machines: a “Workstation” and a Tor “Gateway.” All communications from the Workstation must go through the Tor gateway. This means that even if the Workstation is compromised by malware of some kind, the true IP address remains hidden.

Some of its features include Tor Stream Isolation, [keystroke anonymization](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak), [encrypted swap](https://github.com/Whonix/swap-file-creator), and a hardened memory allocator. Future versions of Whonix will likely include [full system AppArmor policies](https://github.com/Whonix/apparmor-profile-everything) and a [sandbox app launcher](https://www.whonix.org/wiki/Sandbox-app-launcher) to fully confine all processes on the system.

Whonix is best used [in conjunction with Qubes](https://www.whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers). We have a [recommended guide](os/qubes-overview.md#connecting-to-tor-via-a-vpn) on configuring Whonix in conjunction with a VPN ProxyVM in Qubes to hide your Tor activities from your ISP.

### Caudas

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    !(/assets/img/linux-desktop/tails.svg){ align=right }
    
    **Tails** é um sistema operacional live baseado no Debian que roteia todas as comunicações através do Tor. Pode arrancar em quase qualquer computador a partir de um DVD, pen USB ou sdcard.
    
    O seu objectivo é preservar a privacidade e o anonimato, contornando a censura e não deixando qualquer vestígio de si no computador em que é utilizado.

Acredita-se frequentemente que [open source](https://en.wikipedia.org/wiki/Open-source_software) software é intrinsecamente seguro porque o código fonte está disponível. Há uma expectativa de que a verificação da comunidade ocorra regularmente; no entanto, isto nem sempre é [o caso](https://seirdy.one/2022/02/02/floss-security.html). A Tails system that is compromised by malware may potentially bypass the transparent proxy allowing for the user to be deanonymized.

Tails includes [uBlock Origin](desktop-browsers.md#ublock-origin) in Tor Browser by default, which may potentially make it easier for adversaries to fingerprint Tails users. [Whonix](desktop.md#whonix) virtual machines may be more leak-proof, however they are not amnesic, meaning data may be recovered from your storage device.

By design, Tails is meant to completely reset itself after each reboot. Encrypted [persistent storage](https://tails.boum.org/doc/persistent_storage/index.en.html) can be configured to store some data between reboots.

## Security-focused Distributions

### SO Qubes

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

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

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Kicksecure logo](assets/img/linux-desktop/kicksecure.svg){ align=right }
    
    **Kicksecure**—in oversimplified terms—is a set of scripts, configurations, and packages that substantially reduce the attack surface of Debian. It covers a lot of privacy and hardening recommendations by default. It also serves as the base OS for [Whonix](#whonix).
    
    [:octicons-home-16: Homepage](https://www.kicksecure.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.kicksecure.com/wiki/Privacy_Policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://www.kicksecure.com/wiki/Documentation){ .card-link title=Documentation }
    [:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.kicksecure.com/wiki/Donate){ .card-link title=Contribute }

## Framadate

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
