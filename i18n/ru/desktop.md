---
title: "Персональный компьютер"
icon: simple/linux
description: Дистрибутивы Linux часто рекомендуются для защиты конфиденциальности и свободы пользователей.
cover: desktop.webp
---

Дистрибутивы Linux часто рекомендуются для защиты конфиденциальности и свободы пользователей. Если вы еще не используете Linux, ниже приведены некоторые дистрибутивы, которые мы рекомендуем попробовать, а также несколько общих советов по улучшению конфиденциальности и безопасности, которые применимы ко многим дистрибутивам Linux.

- [Общий обзор Linux :material-arrow-right-drop-circle:](os/linux-overview.md)

## Традиционные дистрибутивы

### Fedora Workstation

!!! recommendation

    ![Логотип Fedora](assets/img/linux-desktop/fedora-workstation.svg){ align=right }
    
    **Fedora Workstation** - наш рекомендуемый дистрибутив для начинающих пользователей Linux. Fedora обычно внедряет новые технологии раньше других дистрибутивов, например [Wayland](https://wayland.freedesktop.org/), [PipeWire](https://pipewire.org). Эти новые технологии часто улучшают безопасность, конфиденциальность и удобство использования в целом.
    
    [:octicons-home-16: Домашняя страница](https://fedoraproject.org/workstation/){ .md-button .md-button--primary }
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
    
    [:octicons-home-16: Домашняя страница](https://fedoraproject.org/silverblue/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/fedora-silverblue/){ .card-link title=Документация}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Поддержать }

Silverblue (и Kinoite) отличаются от Fedora Workstation тем, что заменяют пакетный менеджер [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf/) гораздо более продвинутой альтернативой под названием [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/package-management/rpm-ostree/). Менеджер пакетов `rpm-ostree` работает путем скачивания базового образа для системы, а затем наложения пакетов на него в [git](https://en.wikipedia.org/wiki/Git)-подобном дереве коммитов. Когда система обновляется, загружается новое базовое изображение, и наложения будут применены к этому новому изображению.

После завершения обновления вы перезагрузите систему в новую установку. `rpm-ostree` сохраняет две версии системы, чтобы вы могли легко откатиться назад, если что-то сломается в новой версии. Также есть возможность подключить большее количество версий по мере необходимости.

[Flatpak](https://www.flatpak.org) является основным методом установки пакетов в этих дистрибутивах, так как `rpm-ostree` предназначен только для наложения пакетов, которые не могут оставаться внутри контейнера, поверх базового образа.

В качестве альтернативы для Flatpak существует возможность [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox/) для создания [Podman](https://podman.io) контейнеров с общим домашним каталогом с операционной системой хоста и имитации традиционного окружения Fedora, что является [полезной функцией](https://containertoolbx.org) для взыскательных разработчиков.

### NixOS

!!! recommendation

    ![Логотип NixOS](assets/img/linux-desktop/nixos.svg){ align=right }
    
    NixOS - это независимый дистрибутив, основанный на пакетном менеджере Nix с акцентом на воспроизводимость и надежность.
    
    [:octicons-home-16: Домашняя страница](https://nixos.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=Документация}
    [:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=Поддержать }

Менеджер пакетов NixOS хранит каждую версию каждого пакета в отдельной папке в **хранилище Nix**. Из-за этого в вашей системе могут быть установлены разные версии одного и того же пакета. После записи содержимого пакета в папку, папка становится доступной только для чтения.

NixOS также предоставляет атомные обновления; сначала она загружает (или собирает) пакеты и файлы для нового поколения системы, а затем переходит на него. Есть разные способы переключения на новое поколение; вы можете указать NixOS активировать его после перезагрузки или переключиться на него во время выполнения. Вы также можете *протестировать* новое поколение, переключившись на него во время выполнения, но не устанавливая его в качестве текущего поколения системы. Если что-то в процессе обновления сломается, вы можете просто перезагрузиться и автоматически вернуться к рабочей версии системы.

Менеджер пакетов Nix использует чистый функциональный язык - который также называется Nix - для определения пакетов.

[Nixpkgs](https://github.com/nixos/nixpkgs) (основной источник пакетов) содержится в едином репозитории GitHub. Вы также можете определить свои собственные пакеты на том же языке и затем легко включить их в свою конфигурацию.

Nix - это менеджер пакетов на основе исходных файлов; если в кэше бинарных файлов нет готовой сборки, Nix просто соберет пакет из исходных файлов, используя его определение. Он собирает каждый пакет в изолированной *чистой* среде, которая максимально независима от хост-системы, что делает двоичные файлы воспроизводимыми.

## Дистрибутивы для анонимности

### Whonix

!!! recommendation

    ![Whonix logo](assets/img/linux-desktop/whonix.svg){ align=right }
    
    **Whonix** is based on [Kicksecure](#kicksecure), a security-focused fork of Debian. Его цель - обеспечить конфиденциальность, безопасность и анонимность в интернете. Whonix лучше всего использовать в сочетании с [Qubes OS](#qubes-os).
    
    [:octicons-home-16: Домашняя страница](https://www.whonix.org/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://www.dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Сервис Onion" }
    [:octicons-info-16:](https://www.whonix.org/wiki/Documentation){ .card-link title=Документация}
    [:octicons-heart-16:](https://www.whonix.org/wiki/Donate){ .card-link title=Поддержать }

Whonix предназначен для запуска в виде двух виртуальных машин: "Рабочая" и "Шлюз Tor." Все соединения рабочей станции должны проходить через шлюз Tor. Это означает, даже если рабочая станция будет скомпрометирована каким-либо вредоносным ПО, настоящий IP-адрес останется скрытым.

Some of its features include Tor Stream Isolation, [keystroke anonymization](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak), [encrypted swap](https://github.com/Whonix/swap-file-creator), and a hardened memory allocator. Future versions of Whonix will likely include [full system AppArmor policies](https://github.com/Whonix/apparmor-profile-everything) and a [sandbox app launcher](https://www.whonix.org/wiki/Sandbox-app-launcher) to fully confine all processes on the system.

Whonix is best used [in conjunction with Qubes](https://www.whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers). We have a [recommended guide](os/qubes-overview.md#connecting-to-tor-via-a-vpn) on configuring Whonix in conjunction with a VPN ProxyVM in Qubes to hide your Tor activities from your ISP.

### Tails

!!! recommendation

    ![Логотип Tails](assets/img/linux-desktop/tails.svg){ align=right }
    
    **Tails** - это операционная система, основанная на Debian и направляющая все коммуникации через Tor, которая может загружаться практически на любом компьютере с DVD или USB-накопителя или SD-карты. Она использует [Tor](tor.md) для сохранения конфиденциальности и анонимности, обходя цензуру и не оставляет следов на используемом компьютере после выключения.
    
    [:octicons-home-16: Домашняя страница](https://tails.boum.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://tails.boum.org/doc/index.en.html){ .card-link title=Документация}
    [:octicons-heart-16:](https://tails.boum.org/donate/){ .card-link title=Поддержать }

Tails отлично подходит для криминалистической экспертизы благодаря амнезии (то есть ничего не записывается на диск); однако это не такой защищенный дистрибутив, как Whonix. В нем нет многих функций анонимности и безопасности, которые есть в Whonix, и он обновляется гораздо реже (только раз в шесть недель). Система Tails, взломанная вредоносным ПО, может потенциально обойти прозрачный прокси-сервер, что позволит деанонимизировать пользователя.

Tails содержит [uBlock Origin](desktop-browsers.md#ublock-origin) в Tor Browser по умолчанию, что потенциально может облегчить злоумышленникам составить цифровые отпечатки пользователей Tails. [Виртуальные машины Whonix](desktop.md#whonix) могут быть более защищены от утечек, однако они не поддерживают амнезию, то есть данные могут быть восстановлены с вашего устройства хранения.

По замыслу разработчиков, Tails должна сама полностью сбрасываться после каждой перезагрузки. Зашифрованное [постоянное хранилище](https://tails.boum.org/doc/persistent_storage/index.en.html) может быть настроено для хранения некоторых данных между перезагрузками.

## Дистрибутивы для безопасности

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
    
    **Kicksecure**—in oversimplified terms—is a set of scripts, configurations, and packages that substantially reduce the attack surface of Debian. Он охватывает множество рекомендаций по обеспечению конфиденциальности и усилению защиты, без необходимости дополнительной настройки. It also serves as the base OS for [Whonix](#whonix).
    
    [:octicons-home-16: Homepage](https://www.kicksecure.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.kicksecure.com/wiki/Privacy_Policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://www.kicksecure.com/wiki/Documentation){ .card-link title=Documentation }
    [:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.kicksecure.com/wiki/Donate){ .card-link title=Contribute }

## Критерии

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
