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

Рассмотрите возможность использования [ZRAM](https://wiki.archlinux.org/title/Swap#zram-generator) или [зашифрованного свопа](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) вместо незашифрованного свопа, чтобы избежать потенциальных проблем безопасности, связанных с перемещением конфиденциальных данных в [пространство свопа](https://en.wikipedia.org/wiki/Memory_paging). Дистрибутивы на базе Fedora [по умолчанию используют ZRAM](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

### Wayland

Мы рекомендуем использовать среду рабочего стола, которая поддерживает графический протокол [Wayland](https://ru.wikipedia.org/wiki/Wayland), поскольку он был разработан [с учетом](https://lwn.net/Articles/589147/) требований безопасности. Его предшественник, [X11](https://en.wikipedia.org/wiki/X_Window_System), не поддерживает изоляцию графического интерфейса, позволяя всем окнам [записывать экран, логи и вводить данные в другие окна](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), что делает любые попытки создания "песочницы" бесполезными. Хотя существуют варианты вложенных X11, например [Xpra](https://en.wikipedia.org/wiki/Xpra) или [Xephyr](https://en.wikipedia.org/wiki/Xephyr), они часто имеют негативные последствия для производительности, не удобны в настройке и всё равно хуже Wayland.

К счастью, такие распространенные среды, как [GNOME](https://www.gnome.org), [KDE](https://kde.org) и оконный менеджер [Sway](https://swaywm.org) имеют поддержку Wayland. Некоторые дистрибутивы, такие как Fedora и Tumbleweed, используют его по умолчанию, а некоторые другие могут сделать это в будущем, поскольку X11 находится в [режиме жесткого обслуживания](https://www.phoronix.com/scan.php?page=news_item&px=X.Org-Maintenance-Mode-Quickly). Если вы используете одну из этих сред, можно просто выбрать сессию "Wayland" в менеджере отображения рабочего стола ([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)).

Мы рекомендуем **не использовать** окружения рабочего стола или оконные менеджеры, которые не имеют поддержки Wayland, например Cinnamon (по умолчанию в Linux Mint), Pantheon (стандартный в Elementary OS), MATE, Xfce и i3.

### Проприетарная прошивка (обновления микрокода)

Такие дистрибутивы Linux, как [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre) или DIY (Arch Linux), не поставляются с собственными обновлениями [микрокода](https://en.wikipedia.org/wiki/Microcode), которые часто исправляют уязвимости. Некоторыми яркими примерами таких уязвимостей являются [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), и других [аппаратные уязвимости](https://www.kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

Мы **настоятельно рекомендуем** устанавливать обновления микрокода, поскольку ваш процессор уже работает под управлением фирменного микрокода с завода. В Fedora и openSUSE обновления микрокода применяются по умолчанию.

### Обновления

Большинство дистрибутивов Linux автоматически устанавливают обновления или напоминают вам сделать это. Важно поддерживать ОС в актуальном состоянии, чтобы при обнаружении уязвимости программное обеспечение было исправлено.

Некоторые дистрибутивы (особенно предназначенные для опытных пользователей) более "голые" и предполагают, что вы все сделаете сами (например, Arch или Debian). Для получения важных обновлений безопасности потребуется вручную запустить "менеджер пакетов" (`apt`, `pacman`, `dnf` и т.д.).

Кроме того, некоторые дистрибутивы не будут автоматически загружать обновления прошивки. Для этого вам нужно установить [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

## Твики конфиденциальности

### Рандомизация MAC-адресов

Многие настольные дистрибутивы Linux (Fedora, openSUSE и т.д.) поставляются с [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager), для настройки параметров Ethernet и Wi-Fi.

Можно [рандомизировать](https://fedoramagazine.org/randomize-mac-address-nm/) [MAC-адрес](https://ru.wikipedia.org/wiki/MAC-%D0%B0%D0%B4%D1%80%D0%B5%D1%81) при использовании NetworkManager. Это обеспечивает большую конфиденциальность в сетях Wi-Fi, так как затрудняет отслеживание конкретных устройств в сети, к которой вы подключены. Это [**не**](https://papers.mathyvanhoef.com/wisec2016.pdf) делает вас анонимным.

Мы рекомендуем изменить настройки на **random** вместо **stable**, как предлагается в [статье](https://fedoramagazine.org/randomize-mac-address-nm/).

Если вы используете [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), вам необходимо установить [`MACAddressPolicy=random`](https://www.freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=), что позволит включить [RFC 7844 (профили анонимности для клиентов DHCP)](https://www.freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

Нет особого смысла в рандомизации MAC-адресов для Ethernet-подключений, поскольку системный администратор может найти вас, посмотрев на порт, который вы используете на [сетевом коммутаторе](https://en.wikipedia.org/wiki/Network_switch). Рандомизация MAC-адресов Wi-Fi зависит от поддержки встроенного программного обеспечения Wi-Fi.

### Другие идентификаторы

Существуют и другие системные идентификаторы, с которыми следует быть осторожными. Вам следует подумать, применимо ли это к вашей [модели угрозы](../basics/threat-modeling.md):

- **Хост-имена:** Имя хоста вашей системы является общим для сетей, к которым вы подключаетесь. Вам следует избегать включения в имя хоста идентифицирующих терминов, таких как ваше имя или операционная система, вместо этого следует использовать общие термины или случайные строки.
- **Имена пользователей:** Аналогично, ваше имя пользователя используется различными способами в вашей системе. Рассмотрите возможность использования общих терминов, таких как "пользователь", вместо вашего настоящего имени.
- **Идентификатор устройства:**: Во время установки генерируется уникальный идентификатор устройства, который сохраняется на вашем устройстве. Рассмотрите возможность [установки случайного идентификатора](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### Подсчёт систем

Проект Fedora [подсчитывает](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting), сколько уникальных систем обращаются к его зеркалам, используя переменную [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) вместо уникального ID. Fedora делает это для определения нагрузки и предоставления лучших серверов для обновлений, где это необходимо.

Эта [опция](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) в настоящее время по умолчанию выключена. Мы рекомендуем добавить `countme=false` в `/etc/dnf/dnf.conf` на случай, если она будет включена в будущем. В системах, использующих `rpm-ostree`, например Silverblue, опция countme отключается путем маскировки таймера [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems/).

openSUSE также использует [уникальный идентификатор](https://en.opensuse.org/openSUSE:Statistics) для подсчета систем, который можно отключить, удалив файл `/var/lib/zypp/AnonymousUniqueId`.
