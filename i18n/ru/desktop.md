---
title: "Персональный компьютер"
icon: simple/linux
description: Дистрибутивы Linux часто рекомендуются для защиты конфиденциальности и свободы пользователей.
cover: desktop.webp
---

<small>Защищает от следующих угроз:</small>

- [:material-account-cash: Капитализм слежки](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Дистрибутивы Linux часто рекомендуются для защиты конфиденциальности и свободы пользователей. Если вы еще не используете Linux, ниже приведены некоторые дистрибутивы, которые мы рекомендуем попробовать, а также несколько общих советов по улучшению конфиденциальности и безопасности, которые применимы ко многим дистрибутивам Linux.

- [Общий обзор Linux :material-arrow-right-drop-circle:](os/linux-overview.md)

## Традиционные дистрибутивы

### Fedora Linux

<div class="admonition recommendation" markdown>

![Логотип Fedora](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Linux** — это настольный дистрибутив, который мы рекомендуем людям, не знакомым с Linux. Fedora обычно внедряет новые технологии (например, [Wayland](https://wayland.freedesktop.org) и [PipeWire](https://pipewire.org)) раньше других дистрибутивов. Эти новые технологии часто улучшают безопасность, конфиденциальность и удобство использования в целом.

[:octicons-home-16: Домашняя страница](https://fedoraproject.org/ru/){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/ru/docs/){ .card-link title="Документация" }
[:octicons-heart-16:](https://whatcanidoforfedora.org/ru){ .card-link title="Поддержать" }

</details>

</div>

Fedora поставляется в двух основных настольных редакциях, [Fedora Workstation](https://fedoraproject.org/workstation), использующей рабочий стол GNOME, и [Fedora KDE Plasma Desktop](https://fedoraproject.org/kde), использующей KDE. Исторически Fedora Workstation была более популярна и широко рекомендовалась, но KDE набирает популярность и предлагает более похожий на Windows опыт использования, что может помочь некоторым людям перейти на Linux. Преимущества обеих редакций в плане безопасности и приватности очень схожи, так что выбор сводится в основном к личным предпочтениям.

Fedora имеет \[полуплавающий\](https://ru.wikipedia.org/wiki/Rolling_release) цикл выпуска. Несмотря на то, что некоторые пакеты, такие как оболочка рабочего стола, замораживаются до следующего выпуска Fedora, большинство пакетов (включая ядро) обновляются часто в течение всего срока жизни релиза. Каждый выпуск Fedora поддерживается в течение одного года, а новая версия выходит каждые 6 месяцев.

### openSUSE Tumbleweed

<div class="admonition recommendation" markdown>

![Логотип openSUSE Tumbleweed](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }

**openSUSE Tumbleweed** — стабильный дистрибутив с [плавающей системой релизов](https://ru.wikipedia.org/wiki/Rolling_release).

openSUSE Tumbleweed использует [Btrfs](https://ru.wikipedia.org/wiki/Btrfs) и [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial), чтобы обеспечить возможность откатить снимки системы в случае возникновения проблем.

[:octicons-home-16: Домашняя страница](https://get.opensuse.org/tumbleweed){ .md-button .md-button--primary }
[:octicons-info-16:](https://doc.opensuse.org){ .card-link title="Документация" }
[:octicons-heart-16:](https://shop.opensuse.org){ .card-link title="Поддержать" }

</details>

</div>

Tumbleweed следует модели плавающего релиза, когда каждое обновление выпускается как снимок дистрибутива. При обновлении системы скачивается новый снимок. Каждый снимок проходит через серию автоматизированных тестов [openQA](https://openqa.opensuse.org) для обеспечения его качества.

### Arch Linux

<div class="admonition recommendation" markdown>

![Логотип Arch](assets/img/linux-desktop/archlinux.svg){ align=right }

**Arch Linux** — это легковесный дистрибутив «собери сам» (DIY): вы получаете только то, что устанавливаете. Более подробную информацию можно найти на их сайте [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions).

[:octicons-home-16: Домашняя страница](https://archlinux.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.archlinux.org){ .card-link title="Документация"}
[:octicons-heart-16:](https://archlinux.org/donate){ .card-link title="Поддержать" }

</details>

</div>

Arch Linux имеет плавающий цикл релиза. Не существует фиксированного графика релиза, пакеты обновляются очень часто.

Так как это DIY-дистрибутив, вы [должны самостоятельно настравивать и обслуживать](os/linux-overview.md#arch-based-distributions) свою систему. Arch имеет [официальный установщик](https://wiki.archlinux.org/title/Archinstall), чтобы немного облегчить процесс установки.

Значительная часть [пакетов Arch Linux](https://reproducible.archlinux.org) [воспроизводимы](https://reproducible-builds.org)[^1].

## Атомарные дистрибутивы

**Атомарные дистрибутивы** (также называемые **неизменяемыми**) — это операционные системы, в которых установка и обновление пакетов происходит путем наложения изменений на основной образ системы, а не внесения изменений напрямую в систему. Преимущества атомарных дистрибутивов — повышенная стабильность и возможность легко откатывать обновления. См. [*разницу между традиционными и атомарными обновлениями*](os/linux-overview.md#traditional-vs-atomic-updates), чтобы получить больше информации.

### Fedora Atomic

<div class="admonition recommendation" markdown>

![Логотип Fedora](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Atomic** — это варианты Fedora, которые используют пакетный менеджер `rpm-ostree` и ориентированы на контейнеризацию и использование Flatpak для настольных приложений. Эти редакции следуют тому же графику релизов, что и Fedora Workstation, получая те же преимущества быстрых обновлений и оставаясь очень близкими к основной версии системы.

[:octicons-home-16: Домашняя страница](https://fedoraproject.org/ru/atomic-desktops/){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/emerging){ .card-link title="Документация" }
[:octicons-heart-16:](https://whatcanidoforfedora.org/ru){ .card-link title="Поддержать" }

</details>

</div>

[Fedora Atomic](https://fedoramagazine.org/introducing-fedora-atomic-desktops) поставляется в нескольких различных вариантах в зависимости от того, какую среду рабочего стола вы предпочитаете. Как и в случае с рекомендацией избегать X11 в наших [критериях](#criteria) для дистрибутивов Linux, мы рекомендуем избегать версии, которые поддерживают только устаревшую оконную систему X11.

These operating systems differ from Fedora Workstation as they replace the [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf) package manager with a much more advanced alternative called [`rpm-ostree`](https://coreos.github.io/rpm-ostree). The `rpm-ostree` package manager works by downloading a base image for the system, then overlaying packages over it in a [git](https://en.wikipedia.org/wiki/Git)-like commit tree. When the system is updated, a new base image is downloaded and the overlays will be applied to that new image.

After the update is complete, you will reboot the system into the new deployment. `rpm-ostree` keeps two deployments of the system so that you can easily roll back if something breaks in the new deployment. There is also the option to pin more deployments as needed.

[Flatpak](https://flatpak.org) is the primary package installation method on these distributions, as `rpm-ostree` is only meant to overlay packages that cannot stay inside a container on top of the base image.

As an alternative to Flatpaks, there is the option of [Toolbx](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox) to create [Podman](https://podman.io) containers which mimic a traditional Fedora environment, a [useful feature](https://containertoolbx.org) for the discerning developer. These containers share a home directory with the host operating system.

### NixOS

<div class="admonition recommendation" markdown>

![Логотип NixOS](assets/img/linux-desktop/nixos.svg){ align=right }

NixOS - это независимый дистрибутив, основанный на пакетном менеджере Nix с акцентом на воспроизводимость и надежность.

[:octicons-home-16: Homepage](https://nixos.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://nixos.org/learn.html){ .card-link title="Documentation" }
[:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title="Contribute" }

</details>

</div>

NixOS’s package manager keeps every version of every package in a different folder in the **Nix store**. Due to this you can have different versions of the same package installed on your system. After the package contents have been written to the folder, the folder is made read-only.

NixOS also provides atomic updates. It first downloads (or builds) the packages and files for the new system generation and then switches to it. There are different ways to switch to a new generation: you can tell NixOS to activate it after reboot, or you can switch to it at runtime. You can also *test* the new generation by switching to it at runtime, but not setting it as the current system generation. If something in the update process breaks, you can just reboot and automatically and return to a working version of your system.

The Nix package manager uses a purely functional language—which is also called Nix—to define packages.

[Nixpkgs](https://github.com/nixos/nixpkgs) (the main source of packages) are contained in a single GitHub repository. You can also define your own packages in the same language and then easily include them in your config.

Nix is a source-based package manager; if there’s no pre-built available in the binary cache, Nix will just build the package from source using its definition. It builds each package in a sandboxed *pure* environment, which is as independent of the host system as possible. Binaries built with this method are reproducible[^1].

## Дистрибутивы для анонимности

### Whonix

<div class="admonition recommendation" markdown>

![Whonix logo](assets/img/linux-desktop/whonix.svg){ align=right }

**Whonix** is based on [Kicksecure](#kicksecure), a security-focused fork of Debian. It aims to provide privacy, security, and [:material-incognito: Anonymity](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } on the internet. Whonix лучше всего использовать в сочетании с [Qubes OS](#qubes-os).

[:octicons-home-16: Homepage](https://whonix.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://whonix.org/wiki/Documentation){ .card-link title="Documentation" }
[:octicons-heart-16:](https://whonix.org/wiki/Donate){ .card-link title="Contribute" }

</details>

</div>

Whonix is meant to run as two virtual machines: a “Workstation” and a Tor “Gateway.” All communications from the Workstation must go through the Tor gateway. This means that even if the Workstation is compromised by malware of some kind, the true IP address remains hidden.

Some of its features include Tor Stream Isolation, [keystroke anonymization](https://whonix.org/wiki/Keystroke_Deanonymization#Kloak), [encrypted swap](https://github.com/Whonix/swap-file-creator), and a hardened memory allocator. Future versions of Whonix will likely include [full system AppArmor policies](https://github.com/roddhjav/apparmor.d) and a [sandboxed app launcher](https://whonix.org/wiki/Sandbox-app-launcher) to fully confine all processes on the system.

Whonix is best used [in conjunction with Qubes](https://whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers). We have a [recommended guide](os/qubes-overview.md#connecting-to-tor-via-a-vpn) on configuring Whonix in conjunction with a VPN ProxyVM in Qubes to hide your Tor activities from your ISP.

### Tails

<div class="admonition recommendation" markdown>

![Логотип Tails](assets/img/linux-desktop/tails.svg){ align=right }

**Tails** - это операционная система, основанная на Debian и направляющая все коммуникации через Tor, которая может загружаться практически на любом компьютере с DVD или USB-накопителя или SD-карты. It uses [Tor](tor.md) to preserve privacy and [:material-incognito: Anonymity](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } while circumventing censorship, and it leaves no trace of itself on the computer it is used on after it is powered off.

[:octicons-home-16: Homepage](https://tails.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://tails.net/doc/index.en.html){ .card-link title="Documentation" }
[:octicons-heart-16:](https://tails.net/donate){ .card-link title="Contribute" }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

Tails [doesn't erase](https://gitlab.tails.boum.org/tails/tails/-/issues/5356) the [video memory](https://en.wikipedia.org/wiki/Dual-ported_video_RAM) when shutting down. When you restart your computer after using Tails, it might briefly display the last screen that was displayed in Tails. If you shut down your computer instead of restarting it, the video memory will erase itself automatically after being unpowered for some time.

</div>

Tails is great for counter forensics due to amnesia (meaning nothing is written to the disk); however, it is not a hardened distribution like Whonix. It lacks many anonymity and security features that Whonix has and gets updated much less often (only once every six weeks). A Tails system that is compromised by malware may potentially bypass the transparent proxy, allowing for the user to be deanonymized.

Tails includes [uBlock Origin](browser-extensions.md#ublock-origin) in Tor Browser by default, which may potentially make it easier for adversaries to fingerprint Tails users. [Whonix](desktop.md#whonix) virtual machines may be more leak-proof, however they are not amnesic, meaning data may be recovered from your storage device.

By design, Tails is meant to completely reset itself after each reboot. Encrypted [persistent storage](https://tails.net/doc/persistent_storage/index.en.html) can be configured to store some data between reboots.

## Дистрибутивы для безопасности

<small>Защищает от следующих угроз:</small>

- [:material-bug-outline: Пассивные атаки](basics/common-threats.md#security-and-privacy ""){.pg-orange}

### Qubes OS

<div class="admonition recommendation" markdown>

![Qubes OS logo](assets/img/qubes/qubes_os.svg){ align=right }

**Qubes OS** is an open-source operating system designed to provide strong security for desktop computing through secure virtual machines (or "qubes"). Qubes is based on Xen, the X Window System, and Linux. It can run most Linux applications and use most of the Linux drivers.

[:octicons-home-16: Homepage](https://qubes-os.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://qubes-os.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://qubes-os.org/doc){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/QubesOS){ .card-link title="Source Code" }
[:octicons-heart-16:](https://qubes-os.org/donate){ .card-link title="Contribute" }

</details>

</div>

Qubes OS secures the computer by isolating subsystems (e.g., networking, USB, etc.) and applications in separate *qubes*. Should one part of the system be compromised via an exploit in a [:material-target-account: Targeted Attack](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}, the extra isolation is likely to protect the rest of the *qubes* and the core system.

For further information about how Qubes works, read our full [Qubes OS overview](os/qubes-overview.md) page.

### Secureblue

<div class="admonition recommendation" markdown>

![Secureblue logo](assets/img/linux-desktop/secureblue.svg){ align=right }

**Secureblue** is a security-focused operating system based on [Fedora Atomic Desktops](#fedora-atomic-desktops). It includes a number of [security features](https://secureblue.dev/features) intended to proactively defend against the exploitation of both known and unknown vulnerabilities, and ships with [Trivalent](https://github.com/secureblue/Trivalent), their hardened, Chromium-based web browser.

[:octicons-home-16: Homepage](https://secureblue.dev){ .md-button .md-button--primary }
[:octicons-info-16:](https://secureblue.dev/install){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/secureblue/secureblue){ .card-link title="Source Code" }
[:octicons-heart-16:](https://secureblue.dev/donate){ .card-link title="Contribute" }

</div>

**Trivalent** is Secureblue's hardened Chromium for desktop Linux inspired by [GrapheneOS](android/distributions.md#grapheneos)'s Vanadium browser.

Secureblue also provides GrapheneOS's [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc) and enables it globally (including for Flatpaks).

### Kicksecure

While we [recommend against](os/linux-overview.md#release-cycle) "perpetually outdated" distributions like Debian for desktop use in most cases, Kicksecure is a Debian-based operating system which has been hardened to be much more than a typical Linux install.

<div class="admonition recommendation" markdown>

![Kicksecure logo](assets/img/linux-desktop/kicksecure.svg){ align=right }

**Kicksecure**—in oversimplified terms—is a set of scripts, configurations, and packages that substantially reduce the attack surface of Debian. Он охватывает множество рекомендаций по обеспечению конфиденциальности и усилению защиты, без необходимости дополнительной настройки. It also serves as the base OS for [Whonix](#whonix).

[:octicons-home-16: Homepage](https://kicksecure.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kicksecure.com/wiki/Privacy_Policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kicksecure.com/wiki/Documentation){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Source Code" }
[:octicons-heart-16:](https://kicksecure.com/wiki/Donate){ .card-link title="Contribute" }

</details>

</div>

## Критерии

Choosing a Linux distro that is right for you will come down to a huge variety of personal preferences, and this page is **not** meant to be an exhaustive list of every viable distribution. Our Linux overview page has some advice on [choosing a distro](os/linux-overview.md#choosing-your-distribution) in more detail. The distros on *this* page do all generally follow the guidelines we covered there, and all meet these standards:

- Free and open source.
- Receives regular software and kernel updates.
- Avoids X11, as its last major release was [more than a decade](https://x.org/wiki/Releases) ago.
    - The notable exception here is Qubes, but the [isolation issues](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation) which X11 typically has are avoided by virtualization. This isolation only applies to apps *running in different qubes* (virtual machines); apps running in the *same* qube are not protected from each other.
- Supports full-disk encryption during installation.
- Doesn't freeze regular releases for more than 1 year.
    - We [recommend against](os/linux-overview.md#release-cycle) "Long Term Support" or "stable" distro releases for desktop usage.
- Supports a wide variety of hardware.
- Preference towards larger projects.
    - Maintaining an operating system is a major challenge, and smaller projects have a tendency to make more avoidable mistakes, or delay critical updates (or worse, disappear entirely). We lean towards projects which will likely be around 10 years from now (whether that's due to corporate backing or very significant community support), and away from projects which are hand-built or have a small number of maintainers.

In addition, [our standard criteria](about/criteria.md) for recommended projects still applies. **Please note we are not affiliated with any of the projects we recommend.**

[^1]: Reproducibility entails the ability to verify that packages and binaries made available to the end user match the source code, which can be useful against potential [:material-package-variant-closed-remove: Supply Chain Attacks](basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}.
