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

Silverblue (и Kinoite) отличаются от Fedora Workstation тем, что заменяют пакетный менеджер [DNF](https://fedoraproject.org/wiki/DNF) гораздо более продвинутой альтернативой под названием [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/rawhide/system-administrators-guide/package-management/rpm-ostree/). Менеджер пакетов `rpm-ostree` работает путем скачивания базового образа для системы, а затем наложения пакетов на него в [git](https://en.wikipedia.org/wiki/Git)-подобном дереве коммитов. Когда система обновляется, загружается новое базовое изображение, и наложения будут применены к этому новому изображению.

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

    ![Логотип Whonix](assets/img/linux-desktop/whonix.svg){ align=right }
    
    **Whonix** основан на [Kicksecure](https://www.whonix.org/wiki/Kicksecure), форке Debian, ориентированном на безопасность. Его цель - обеспечить конфиденциальность, безопасность и анонимность в интернете. Whonix лучше всего использовать в сочетании с [Qubes OS](#qubes-os).
    
    [:octicons-home-16: Домашняя страница](https://www.whonix.org/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://www.dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Сервис Onion" }
    [:octicons-info-16:](https://www.whonix.org/wiki/Documentation){ .card-link title=Документация}
    [:octicons-heart-16:](https://www.whonix.org/wiki/Donate){ .card-link title=Поддержать }

Whonix предназначен для запуска в виде двух виртуальных машин: "Рабочая" и "Шлюз Tor." Все соединения рабочей станции должны проходить через шлюз Tor. Это означает, даже если рабочая станция будет скомпрометирована каким-либо вредоносным ПО, настоящий IP-адрес останется скрытым.

Некоторые из его возможностей включают изоляцию потока Tor, [анонимизацию нажатия клавиш](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak), [зашифрованный swap](https://github.com/Whonix/swap-file-creator), а также усиленный распределитель памяти.

Будущие версии Whonix, вероятно, будут включать [полные системные политики AppArmor](https://github.com/Whonix/apparmor-profile-everything) и [программу запуска приложений в песочнице](https://www.whonix.org/wiki/Sandbox-app-launcher) для полного ограничения всех процессов в системе.

Whonix лучше всего использовать [в сочетании с Qubes](https://www.whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers), Qubes-Whonix имеет различные [недостатки](https://forums.whonix.org/t/qubes-whonix-security-disadvantages-help-wanted/8581) по сравнению с другими гипервизорами.

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

    ![Логотип Qubes OS](assets/img/qubes/qubes_os.svg){ align=right }
    
    **Qubes OS** - это операционная система с открытым исходным кодом, разработанная для обеспечения сильной безопасности персональных компьютеров. Qubes основан на Xen, X Window System и Linux, и может запускать большинство Linux-приложений и использовать большинство драйверов для Linux.
    
    [:octicons-home-16: Домашняя страница](https://www.qubes-os.org/){ .md-button .md-button--primary }
    [:material-arrow-right-drop-circle: Обзор](os/qubes-overview.md){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Сервис Onion" }
    [:octicons-eye-16:](https://www.qubes-os.org/privacy/){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://www.qubes-os.org/doc/){ .card-link title=Документация }
    [:octicons-code-16:](https://github.com/QubesOS/){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://www.qubes-os.org/donate/){ .card-link title=Поддержать }

Qubes OS - это операционная система на базе Xen, предназначенная для обеспечения надежной защиты настольных компьютеров с помощью защищенных виртуальных машин (ВМ), также известных как *Qubes*.

Операционная система Qubes OS обеспечивает безопасность компьютера путем изоляции подсистем (например, сетевых, USB и т.д.) и приложений в отдельных виртуальных машинах. Если одна часть системы будет скомпрометирована, дополнительная изоляция, скорее всего, защитит остальную часть системы. Более подробную информацию можно найти на сайте [Qubes](https://www.qubes-os.org/faq/).

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

!!! example "Это новый раздел"

    Мы всё еще работаем над установлением критериев для каждого раздела нашего сайта, поэтому они могут поменяться в будущем. Если у вас есть вопросы по поводу наших критериев, пожалуйста, [задавайте их на нашем форуме](https://discuss.privacyguides.net/latest). Если какой-то критерий здесь не указан, это не значит, что мы его не учли. Перед тем, как рекомендовать какой-либо проект мы учитываем и обсуждаем множество факторов. Документирование этих факторов ещё не завершено.

Наши рекомендованные операционные системы:

- Должны иметь открытый исходный код.
- Должны получать регулярные обновления программного обеспечения и ядра Linux.
- Дистрибутивы Linux должны поддерживать [Wayland](os/linux-overview.md#Wayland).
- Должны предлагать шифрование всего диска во время установки.
- Не должны замораживать релизы более чем на 1 год. Мы [не рекомендуем](os/linux-overview.md#release-cycle) дистрибутивы с "Long Term Support" или "stable" релизами для персональных компьютеров.
- Должны поддерживать широкий спектр устройств.
