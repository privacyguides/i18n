---
title: "Персональный компьютер"
icon: fontawesome/brands/linux
description: Дистрибутивы Linux часто рекомендуются для защиты конфиденциальности и свободы пользователей.
cover: desktop.png
---

Дистрибутивы Linux часто рекомендуются для защиты конфиденциальности и свободы пользователей. Если вы еще не используете Linux, ниже приведены некоторые дистрибутивы, которые мы рекомендуем попробовать, а также несколько общих советов по улучшению конфиденциальности и безопасности, которые применимы ко многим дистрибутивам Linux.

- [Общий обзор Linux :material-arrow-right-drop-circle:](os/linux-overview.md)

## Традиционные дистрибутивы

### Fedora Workstation

!!! recommendation

    ![Логотип Fedora](assets/img/linux-desktop/fedora-workstation.svg){ align=right }
    
    **Fedora Workstation** - наш рекомендуемый дистрибутив для начинающих пользователей Linux. Fedora обычно внедряет новые технологии раньше других дистрибутивов, например [Wayland](https://wayland.freedesktop.org/), [PipeWire](https://pipewire.org). Эти новые технологии часто улучшают безопасность, конфиденциальность и удобство использования в целом.
    
    [:octicons-home-16: Домашняя страница](https://getfedora.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=Документация}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Поддержать }

Fedora имеет \[полу-плавающий\](https://ru.wikipedia.org/wiki/Rolling_release) цикл релиза. В то время как некоторые пакеты, такие как [GNOME](https://www.gnome.org), замораживаются до следующего выпуска Fedora, большинство пакетов (включая ядро) часто обновляются в течение всего срока жизни релиза. Каждый выпуск Fedora поддерживается в течение одного года, а новая версия выходит каждые 6 месяцев.

### openSUSE Tumbleweed

!!! recommendation

    ![Логотип openSUSE Tumbleweed](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }
    
    **openSUSE Tumbleweed** - стабильный дистрибутив с [плавающей системой релизов](https://ru.wikipedia.org/wiki/Rolling_release).
    
    openSUSE Tumbleweed имеет систему [транзакционного обновления](https://kubic.opensuse.org/blog/2018-04-04-transactionalupdates/), которая использует [Btrfs](https://en.wikipedia.org/wiki/Btrfs) и [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) для обеспечения возможности отката моментальных снимков системы в случае возникновения проблем.
    
    [:octicons-home-16: Домашняя страница](https://get.opensuse.org/tumbleweed/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://doc.opensuse.org/){ .card-link title=Документация}
    [:octicons-heart-16:](https://shop.opensuse.org/){ .card-link title=Поддержать }

Tumbleweed следует модели плавающего релиза, когда каждое обновление выпускается как снимок дистрибутива. При обновлении системы скачивается новый снимок. Каждый снимок проходит через серию автоматизированных тестов [openQA](https://openqa.opensuse.org) для обеспечения его качества.

### Arch Linux

!!! recommendation

    ![Логотип Arch](assets/img/linux-desktop/archlinux.svg){ align=right }
    
    **Arch Linux** - это легкий, "сделай сам" (DIY) дистрибутив, означающий, что вы получаете только то, что устанавливаете. Более подробную информацию можно найти на их сайте [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions).
    
    [:octicons-home-16: Домашняя страница](https://archlinux.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://wiki.archlinux.org/){ .card-link title=Документация}
    [:octicons-heart-16:](https://archlinux.org/donate/){ .card-link title=Поддержать }

Arch Linux имеет плавающий цикл релиза. Не существует фиксированного графика релиза, пакеты обновляются очень часто.

Будучи DIY дистрибутивом, вы [должны самостоятельно установить и поддерживать](os/linux-overview.md#arch-based-distributions) свою систему. Arch имеет [официальный установщик](https://wiki.archlinux.org/title/Archinstall), чтобы немного облегчить процесс установки.

Большая часть пакетов [Arch Linux](https://reproducible.archlinux.org) является [воспроизводимой](https://reproducible-builds.org).

## Неизменяемые дистрибутивы

### Fedora Silverblue

!!! recommendation

    ![Логотип Fedora Silverblue](assets/img/linux-desktop/fedora-silverblue.svg){ align=right }
    
    **Fedora Silverblue** и **Fedora Kinoite** - это неизменяемые варианты Fedora с сильным фокусом на контейнерные рабочие процессы. Silverblue поставляется с окружением рабочего стола [GNOME](https://www.gnome.org/), а Kinoite - с [KDE](https://kde.org/). Silverblue и Kinoite следуют тому же графику релиза, что и Fedora Workstation, получая преимущества от таких же быстрых обновлений и оставаясь очень близкими к upstream.
    
    [:octicons-home-16: Домашняя страница](https://silverblue.fedoraproject.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/fedora-silverblue/){ .card-link title=Документация}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Поддержать }

Silverblue (and Kinoite) differ from Fedora Workstation as they replace the [DNF](https://fedoraproject.org/wiki/DNF) package manager with a much more advanced alternative called [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/rawhide/system-administrators-guide/package-management/rpm-ostree/). The `rpm-ostree` package manager works by downloading a base image for the system, then overlaying packages over it in a [git](https://en.wikipedia.org/wiki/Git)-like commit tree. When the system is updated, a new base image is downloaded and the overlays will be applied to that new image.

After the update is complete you will reboot the system into the new deployment. `rpm-ostree` keeps two deployments of the system so that you can easily rollback if something breaks in the new deployment. There is also the option to pin more deployments as needed.

[Flatpak](https://www.flatpak.org) is the primary package installation method on these distributions, as `rpm-ostree` is only meant to overlay packages that cannot stay inside of a container on top of the base image.

As an alternative to Flatpaks, there is the option of [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox/) to create [Podman](https://podman.io) containers with a shared home directory with the host operating system and mimic a traditional Fedora environment, which is a [useful feature](https://containertoolbx.org) for the discerning developer.

### NixOS

!!! recommendation

    ![Логотип NixOS](assets/img/linux-desktop/nixos.svg){ align=right }
    
    NixOS - это независимый дистрибутив, основанный на пакетном менеджере Nix с акцентом на воспроизводимость и надежность.
    
    [:octicons-home-16: Домашняя страница](https://nixos.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=Документация}
    [:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=Поддержать }

NixOS’s package manager keeps every version of every package in a different folder in the **Nix store**. Due to this you can have different versions of the same package installed on your system. After the package contents have been written to the folder, the folder is made read-only.

NixOS also provides atomic updates; first it downloads (or builds) the packages and files for the new system generation and then switches to it. There are different ways to switch to a new generation; you can tell NixOS to activate it after reboot or you can switch to it at runtime. You can also *test* the new generation by switching to it at runtime, but not setting it as the current system generation. If something in the update process breaks, you can just reboot and automatically and return to a working version of your system.

Nix the package manager uses a purely functional language - which is also called Nix - to define packages.

[Nixpkgs](https://github.com/nixos/nixpkgs) (the main source of packages) are contained in a single GitHub repository. You can also define your own packages in the same language and then easily include them in your config.

Nix is a source-based package manager; if there’s no pre-built available in the binary cache, Nix will just build the package from source using its definition. It builds each package in a sandboxed *pure* environment, which is as independent of the host system as possible, thus making binaries reproducible.

## Дистрибутивы для анонимности

### Whonix

!!! recommendation

    ![Логотип Whonix](assets/img/linux-desktop/whonix.svg){ align=right }
    
    **Whonix** основан на [Kicksecure](https://www.whonix.org/wiki/Kicksecure), форке Debian, ориентированном на безопасность. Его цель - обеспечить конфиденциальность, безопасность и анонимность в интернете. Whonix лучше всего использовать в сочетании с [Qubes OS](#qubes-os).
    
    [:octicons-home-16: Домашняя страница](https://www.whonix.org/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://www.dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Сервис Onion" }
    [:octicons-info-16:](https://www.whonix.org/wiki/Documentation){ .card-link title=Документация}
    [:octicons-heart-16:](https://www.whonix.org/wiki/Donate){ .card-link title=Поддержать }

Whonix is meant to run as two virtual machines: a “Workstation” and a Tor “Gateway.” All communications from the Workstation must go through the Tor gateway. This means that even if the Workstation is compromised by malware of some kind, the true IP address remains hidden.

Some of its features include Tor Stream Isolation, [keystroke anonymization](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak), [encrypted swap](https://github.com/Whonix/swap-file-creator), and a hardened memory allocator.

Future versions of Whonix will likely include [full system AppArmor policies](https://github.com/Whonix/apparmor-profile-everything) and a [sandbox app launcher](https://www.whonix.org/wiki/Sandbox-app-launcher) to fully confine all processes on the system.

Whonix is best used [in conjunction with Qubes](https://www.whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers), Qubes-Whonix has various [disadvantages](https://forums.whonix.org/t/qubes-whonix-security-disadvantages-help-wanted/8581) when compared to other hypervisors.

### Tails

!!! recommendation

    ![Логотип Tails](assets/img/linux-desktop/tails.svg){ align=right }
    
    **Tails** - это операционная система, основанная на Debian и направляющая все коммуникации через Tor, которая может загружаться практически на любом компьютере с DVD или USB-накопителя или SD-карты. Она использует [Tor](tor.md) для сохранения конфиденциальности и анонимности, обходя цензуру и не оставляет следов на используемом компьютере после выключения.
    
    [:octicons-home-16: Домашняя страница](https://tails.boum.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://tails.boum.org/doc/index.en.html){ .card-link title=Документация}
    [:octicons-heart-16:](https://tails.boum.org/donate/){ .card-link title=Поддержать }

Tails is great for counter forensics due to amnesia (meaning nothing is written to the disk); however, it is not a hardened distribution like Whonix. It lacks many anonymity and security features that Whonix has and gets updated much less often (only once every six weeks). A Tails system that is compromised by malware may potentially bypass the transparent proxy allowing for the user to be deanonymized.

Tails includes [uBlock Origin](desktop-browsers.md#ublock-origin) in Tor Browser by default, which may potentially make it easier for adversaries to fingerprint Tails users. [Whonix](desktop.md#whonix) virtual machines may be more leak-proof, however they are not amnesic, meaning data may be recovered from your storage device.

By design, Tails is meant to completely reset itself after each reboot. Encrypted [persistent storage](https://tails.boum.org/doc/persistent_storage/index.en.html) can be configured to store some data between reboots.

## Дистрибутивы для безопасности

### Qubes OS

!!! recommendation

    ![Логотип Qubes OS](assets/img/qubes/qubes_os.svg){ align=right }
    
    **Qubes OS** - это операционная система с открытым исходным кодом, разработанная для обеспечения сильной безопасности персональных компьютеров. Qubes основан на Xen, X Window System и Linux, и может запускать большинство Linux-приложений и использовать большинство драйверов для Linux.
    
    [:octicons-home-16: Домашняя страница](https://www.qubes-os.org/){ .md-button .md-button--primary }
    [:material-arrow-right-drop-circle: Обзор](os/qubes-overview.md){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Сервис Onion" }
    [:octicons-eye-16:](https://www.qubes-os.org/privacy/){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://www.qubes-os.org/doc/){ .card-link title=Документация }
    [:octicons-code-16:](https://github.com/QubesOS/){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://www.qubes-os.org/donate/){ .card-link title=Поддержать }

Qubes OS is a Xen-based operating system meant to provide strong security for desktop computing through secure virtual machines (VMs), also known as *Qubes*.

The Qubes OS operating system secures the computer by isolating subsystems (e.g., networking, USB, etc.) and applications in separate VMs. Should one part of the system be compromised, the extra isolation is likely to protect the rest of the system. For further details see the Qubes [FAQ](https://www.qubes-os.org/faq/).

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

!!! example "Это новый раздел"

    Мы всё еще работаем над установлением критериев для каждого раздела нашего сайта, поэтому они могут поменяться в будущем. Если у вас есть вопросы по поводу наших критериев, пожалуйста, [задавайте их на нашем форуме](https://discuss.privacyguides.net/latest). Если какой-то критерий здесь не указан, это не значит, что мы его не учли. Перед тем, как рекомендовать какой-либо проект мы учитываем и обсуждаем множество факторов. Документирование этих факторов ещё не завершено.

Our recommended operating systems:

- Must be open-source.
- Must receive regular software and Linux kernel updates.
- Linux distributions must support [Wayland](os/linux-overview.md#Wayland).
- Must support full-disk encryption during installation.
- Must not freeze regular releases for more than 1 year. We [do not recommend](os/linux-overview.md#release-cycle) "Long Term Support" or "stable" distro releases for desktop usage.
- Must support a wide variety of hardware.
