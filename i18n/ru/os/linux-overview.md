---
title: Обзор Linux
icon: fontawesome/brands/linux
description: Linux - это альтернативная настольная операционная система с открытым исходным кодом, ориентированная на конфиденциальность, но не все дистрибутивы созданы одинаково.
---

Часто считается, что программное обеспечение с [открытым исходным кодом](https://en.wikipedia.org/wiki/Open-source_software) по своей сути безопасно, поскольку исходный код доступен. Существует ожидание, что проверка сообщества происходит регулярно; однако это [не всегда так](https://seirdy.one/posts/2022/02/02/floss-security/). Это зависит от ряда факторов, таких как активность проекта, опыт разработчиков, уровень строгости, применяемый в [обзорах кода](https://en.wikipedia.org/wiki/Code_review), и как часто уделяется внимание определенным частям [кодовой базы](https://en.wikipedia.org/wiki/Codebase), которые могут оставаться нетронутыми годами.

На данный момент в настольном Linux есть некоторые области, которые можно улучшить при сравнении с проприетарными аналогами, например:

- Проверенная загрузка, например, [безопасная загрузка](https://support.apple.com/ru-ru/guide/security/secc7b34e5b5/web) от Apple (с [Secure Enclave](https://support.apple.com/ru-ru/guide/security/sec59b0b31ff/1/web/1)), [проверенная загрузка](https://source.android.com/security/verifiedboot) в Android, [Verified boot](https://www.chromium.org/chromium-os/chromiumos-design-docs/security-overview/#verified-boot) в ChromeOS или [защита процесса загрузки](https://learn.microsoft.com/ru-ru/windows/security/operating-system-security/system-security/secure-the-windows-10-boot-process) с [TPM](https://learn.microsoft.com/ru-ru/windows/security/information-protection/tpm/how-windows-uses-the-tpm) в Microsoft Windows. Все эти функции и аппаратные технологии могут помочь предотвратить постоянное вмешательство вредоносных программ или предотвратить [атаки злой горничной](https://encyclopedia.kaspersky.ru/glossary/evil-maid/)
- Сильная "песочница", такая как в [macOS](https://developer.apple.com/library/archive/documentation/Security/Conceptual/AppSandboxDesignGuide/AboutAppSandbox/AboutAppSandbox.html), [ChromeOS](https://chromium.googlesource.com/chromiumos/docs/+/HEAD/sandboxing.md), и [Android](https://source.android.com/security/app-sandbox). Широко используемые решения для создания песочниц в Linux, например [Flatpak](https://docs.flatpak.org/en/latest/sandbox-permissions.html) и [Firejail](https://firejail.wordpress.com/), все еще требуют много улучшений
- Сильные [средства защиты от эксплойтов](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations)

Несмотря на эти недостатки, настольные дистрибутивы Linux отлично вам подойдут, если вы хотите:

- Избежать телеметрии, которая часто поставляется с проприетарными операционными системами
- Поддержать [свободу программного обеспечения](https://www.gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Использовать системы, ориентированные на конфиденциальность, такие как [Whonix](https://www.whonix.org) или [Tails](https://tails.boum.org/index.ru.html)

На нашем сайте термин "Linux" обычно используется для описания дистрибутивов Linux для настольных компьютеров. Другие операционные системы, которые также используют ядро Linux (ChromeOS, Android и Qubes OS) здесь не рассматриваются.

[Наши рекомендации Linux :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Выбор дистрибутива

Не все дистрибутивы Linux созданы одинаковыми. Хотя наша страница рекомендаций по Linux не является авторитетным источником информации о том, какой дистрибутив вам следует использовать, есть несколько моментов, на которые следует обращать внимание при выборе дистрибутива.

### Цикл релиза

Мы настоятельно рекомендуем вам выбирать дистрибутивы, которые близки к стабильным релизам программного обеспечения, часто называемые дистрибутивами с плавающим релизом. Это связано с тем, что дистрибутивы с замороженным циклом выпуска часто не обновляют версии пакетов и не получают обновлений безопасности.

В замороженных дистрибутивах, таких как [Debian](https://www.debian.org/security/faq#handling), ожидается, что сопровождающие пакетов будут вносить исправления из новых релизов для устранения уязвимостей, а не переводить программное обеспечение на новый релиз, выпущенный вышестоящим разработчиком. Некоторые исправления безопасности [вообще не](https://arxiv.org/abs/2105.14565) получают [CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) (особенно менее популярные программы) и поэтому не попадают в дистрибутив при такой модели исправлений. В результате незначительные исправления безопасности иногда задерживаются до следующего крупного релиза.

Мы не считаем, что задержка пакетов и применение промежуточных исправлений является хорошей идеей, так как это расходится с тем, как разработчик мог задумать работу программного обеспечения. [Ричард Браун](https://rootco.de/aboutme/) подготовил презентацию об этом:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/i8c0mg_mS7U?local=true" title="Regular Releases are Wrong, Roll for your life" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Традиционные vs атомарные обновления

Традиционно дистрибутивы Linux обновляются путем последовательного обновления нужных пакетов. Традиционные обновления, например, используемые в дистрибутивах Fedora, Arch Linux и Debian, могут быть менее надежными, если в процессе обновления возникает ошибка.

Дистрибутивы с отомарными обновлениями применяют обновления полностью или не применяют вообще. Как правило, транзакционные системы обновления также являются атомарными.

Система транзакционного обновления создает снимок, который делается до и после применения обновления. Если обновление ломается в любой момент времени (например из-за сбоя питания), обновление можно легко откатить до "последнего известного хорошего состояния."

Метод атомарного обновления используется для таких неизменяемых дистрибутивов, как Silverblue, Tumbleweed и NixOS и может повысить надежность с помощью этой модели. [Adam Šamalík](https://twitter.com/adsamalik) предоставил презентацию о том, как `rpm-ostree` работает с Silverblue:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/-hpV5l-gJnQ?local=true" title="Let's try Fedora Silverblue — an immutable desktop OS! - Adam Šamalik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Дистрибутивы "ориентированные на безопасность"

Часто возникает путаница между дистрибутивами "ориентированными на безопасность" и дистрибутивами для "тестов на проникновение". Быстрый поиск "самый безопасный дистрибутив Linux" часто дает такие результаты, как Kali Linux, Black Arch и Parrot OS. Эти дистрибутивы представляют собой дистрибутивы для тестирования на проникновение, в которых собраны инструменты для тестирования других систем. Они не включают никаких "дополнительных мер безопасности" или защитных механизмов, предназначенных для регулярного использования.

### Дистрибутивы на базе Arch

Дистрибутивы на базе Arch не рекомендуется использовать новичкам в Linux (независимо от дистрибутива), так как они требуют регулярного [обслуживания системы](https://wiki.archlinux.org/title/System_maintenance). Arch не имеет механизма обновления дистрибутива для выбора основного программного обеспечения. В результате вы должны быть в курсе современных тенденций и самостоятельно внедрять технологии по мере того, как они вытесняют старые методы.

Для поддержания безопасности системы от вас ожидается, что вы обладаете достаточными знаниями Linux, чтобы правильно настроить безопасность своей системы, например, принять систему [обязательного контроля доступа](https://en.wikipedia.org/wiki/Mandatory_access_control), настроить черные списки [модулей ядра](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security), усилить параметры загрузки, манипулировать параметрами [sysctl](https://en.wikipedia.org/wiki/Sysctl) и знать, какие компоненты им необходимы, например, [Polkit](https://en.wikipedia.org/wiki/Polkit).

Тот, кто использует [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository), **, должен** быть уверен в том, что он сможет провести аудит PKGBUILD, которые он устанавливает из этой службы. Пакеты AUR - это контент, созданный сообществом, он никак не проверяется и поэтому уязвим для атак на цепочки поставок программного обеспечения, что, собственно, и произошло [в прошлом](https://www.bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository/). AUR всегда следует использовать осторожно, и часто на различных страницах можно встретить множество плохих советов, которые направляют людей на слепое использование [помощников AUR](https://wiki.archlinux.org/title/AUR_helpers) без достаточного предупреждения. Аналогичные предупреждения относятся к использованию сторонних персональных архивов пакетов (PPA) в дистрибутивах на базе Debian или проектов сообщества (COPR) в Fedora.

Если у вас есть опыт работы с Linux и вы хотите использовать дистрибутив на базе Arch, мы рекомендуем только основной Arch Linux, а не его варианты. Мы особенно не рекомендуем использовать эти два варианта Arch:

- **Manjaro**: Этот дистрибутив задерживает пакеты на 2 недели, чтобы убедиться, что их собственные изменения не сломаются, а не для того, чтобы убедиться в стабильности upstream. Когда используются пакеты AUR, они часто собираются на основе последних [библиотек](https://en.wikipedia.org/wiki/Library_(computing)) из репозиториев Arch.
- **Garuda**: Они используют [Chaotic-AUR](https://aur.chaotic.cx/), который автоматически и вслепую компилирует пакеты из AUR. Не существует процесса проверки, чтобы убедиться, что пакеты AUR не страдают от атак в цепи поставок.

### Kicksecure

Хотя мы настоятельно рекомендуем не использовать устаревшие дистрибутивы, такие как Debian, существует операционная система на базе Debian, которая была усилена, чтобы быть намного более безопасной, чем обычные дистрибутивы Linux: [Kicksecure](https://www.kicksecure.com/). Kicksecure, если говорить упрощенно, это набор скриптов, конфигураций и пакетов, которые значительно уменьшают поверхность атаки Debian. Он охватывает множество рекомендаций по обеспечению конфиденциальности и усилению защиты, без необходимости дополнительной настройки.

### Ядро Linux-libre и дистрибутивы "Libre"

Мы настоятельно рекомендуем **не** использовать ядро Linux-libre, поскольку оно [удаляет некоторые компоненты безопасности](https://www.phoronix.com/scan.php?page=news_item&px=GNU-Linux-Libre-5.7-Released) и [подавляет предупреждения ядра](https://news.ycombinator.com/item?id=29674846) об уязвимом микрокоде (по идеологическим причинам).

## Общие рекомендации

### Шифрование диска

Большинство дистрибутивов Linux имеют опцию в программе установки для включения [LUKS](../encryption.md#linux-unified-key-setup) FDE. Если этот параметр небыл выбран во время установки, вам придется создать резервную копию данных и выполнить повторную установку, поскольку шифрование применяется после [разметки диска](https://ru.wikipedia.org/wiki/%D0%A0%D0%B0%D0%B7%D0%B4%D0%B5%D0%BB_%D0%B4%D0%B8%D1%81%D0%BA%D0%B0), но до [форматирования файловых систем](https://ru.wikipedia.org/wiki/%D0%A4%D0%B0%D0%B9%D0%BB%D0%BE%D0%B2%D0%B0%D1%8F_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B0). Мы также рекомендуем безопасно удалять файлы на вашем накопителе:

- [Безопасное удаление данных :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure/)

### Swap

Consider using [ZRAM](https://wiki.archlinux.org/title/Swap#zram-generator) or [encrypted swap](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) instead of unencrypted swap to avoid potential security issues with sensitive data being pushed to [swap space](https://en.wikipedia.org/wiki/Memory_paging). Дистрибутивы на базе Fedora [по умолчанию используют ZRAM](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

### Wayland

Мы рекомендуем использовать среду рабочего стола, которая поддерживает графический протокол [Wayland](https://ru.wikipedia.org/wiki/Wayland), поскольку он был разработан [с учетом](https://lwn.net/Articles/589147/) требований безопасности. Его предшественник, [X11](https://en.wikipedia.org/wiki/X_Window_System), не поддерживает изоляцию графического интерфейса, позволяя всем окнам [записывать экран, логи и вводить данные в другие окна](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), что делает любые попытки создания "песочницы" бесполезными. Хотя существуют варианты вложенных X11, например [Xpra](https://en.wikipedia.org/wiki/Xpra) или [Xephyr](https://en.wikipedia.org/wiki/Xephyr), они часто имеют негативные последствия для производительности, не удобны в настройке и всё равно хуже Wayland.

К счастью, такие распространенные среды, как [GNOME](https://www.gnome.org), [KDE](https://kde.org) и оконный менеджер [Sway](https://swaywm.org) имеют поддержку Wayland. Some distributions like Fedora and Tumbleweed use it by default, and some others may do so in the future as X11 is in [hard maintenance mode](https://www.phoronix.com/scan.php?page=news_item&px=X.Org-Maintenance-Mode-Quickly). Если вы используете одну из этих сред, можно просто выбрать сессию "Wayland" в менеджере отображения рабочего стола ([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)).

Мы рекомендуем **не использовать** окружения рабочего стола или оконные менеджеры, которые не имеют поддержки Wayland, например Cinnamon (по умолчанию в Linux Mint), Pantheon (стандартный в Elementary OS), MATE, Xfce и i3.

### Проприетарная прошивка (обновления микрокода)

Linux distributions such as those which are [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre) or DIY (Arch Linux) don’t come with the proprietary [microcode](https://en.wikipedia.org/wiki/Microcode) updates that often patch vulnerabilities. Some notable examples of these vulnerabilities include [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), and other [hardware vulnerabilities](https://www.kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

We **highly recommend** that you install the microcode updates, as your CPU is already running the proprietary microcode from the factory. Fedora and openSUSE both have the microcode updates applied by default.

### Обновления

Most Linux distributions will automatically install updates or remind you to do so. It is important to keep your OS up to date so that your software is patched when a vulnerability is found.

Some distributions (particularly those aimed at advanced users) are more barebones and expect you to do things yourself (e.g. Arch or Debian). These will require running the "package manager" (`apt`, `pacman`, `dnf`, etc.) manually in order to receive important security updates.

Additionally, some distributions will not download firmware updates automatically. For that you will need to install [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

## Твики конфиденциальности

### Рандомизация MAC-адресов

Many desktop Linux distributions (Fedora, openSUSE, etc.) will come with [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager), to configure Ethernet and Wi-Fi settings.

It is possible to [randomize](https://fedoramagazine.org/randomize-mac-address-nm/) the [MAC address](https://en.wikipedia.org/wiki/MAC_address) when using NetworkManager. This provides a bit more privacy on Wi-Fi networks as it makes it harder to track specific devices on the network you’re connected to. It does [**not**](https://papers.mathyvanhoef.com/wisec2016.pdf) make you anonymous.

We recommend changing the setting to **random** instead of **stable**, as suggested in the [article](https://fedoramagazine.org/randomize-mac-address-nm/).

If you are using [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), you will need to set [`MACAddressPolicy=random`](https://www.freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) which will enable [RFC 7844 (Anonymity Profiles for DHCP Clients)](https://www.freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

There isn’t many points in randomizing the MAC address for Ethernet connections as a system administrator can find you by looking at the port you are using on the [network switch](https://en.wikipedia.org/wiki/Network_switch). Randomizing Wi-Fi MAC addresses depends on support from the Wi-Fi’s firmware.

### Другие идентификаторы

There are other system identifiers which you may wish to be careful about. You should give this some thought to see if it applies to your [threat model](../basics/threat-modeling.md):

- **Hostnames:** Your system's hostname is shared with the networks you connect to. You should avoid including identifying terms like your name or operating system in your hostname, instead sticking to generic terms or random strings.
- **Usernames:** Similarly, your username is used in a variety of ways across your system. Consider using generic terms like "user" rather than your actual name.
- **Machine ID:**: During installation a unique machine ID is generated and stored on your device. Consider [setting it to a generic ID](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### Подсчёт систем

The Fedora Project [counts](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) how many unique systems access its mirrors by using a [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) variable instead of a unique ID. Fedora does this to determine load and provision better servers for updates where necessary.

This [option](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) is currently off by default. We recommend adding `countme=false` to `/etc/dnf/dnf.conf` just in case it is enabled in the future. On systems that use `rpm-ostree` such as Silverblue, the countme option is disabled by masking the [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems/) timer.

openSUSE also uses a [unique ID](https://en.opensuse.org/openSUSE:Statistics) to count systems, which can be disabled by deleting the `/var/lib/zypp/AnonymousUniqueId` file.
