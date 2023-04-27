---
title: Panoramica di Linux
icon: simple/linux
description: Linux è un sistema operativo desktop open-source, incentrato sulla privacy, ma non tutte le distribuzioni sono uguali.
---

Si crede spesso che il software [open-source](https://it.wikipedia.org/wiki/Open_source) sia intrinsecamente sicuro perché il codice sorgente è disponibile. Ci si aspetta che la verifica da parte della comunità avvenga regolarmente; tuttavia, questo non è sempre [il caso](https://seirdy.one/posts/2022/02/02/floss-security/). Dipende da un certo numero di fattori, come l'attività del progetto, l'esperienza degli sviluppatori, il livello di rigore applicato alle [revisioni del codice](https://en.wikipedia.org/wiki/Code_review), e quanto spesso si presta attenzione a parti specifiche del [codebase](https://it.wikipedia.org/wiki/Codebase) che possono rimanere inalterate per anni.

Al momento, GNU/Linux desktop ha alcune aree che potrebbero essere migliorate rispetto alle loro controparti proprietarie, ad esempio:

- Una catena di avvio verificata, a differenza del [Secure Boot](https://support.apple.com/it-it/guide/security/secc7b34e5b5/web) di Apple (con [Secure Enclave](https://support.apple.com/it-it/guide/security/sec59b0b31ff/1/web/1)), Android [Verified Boot](https://source.android.com/security/verifiedboot) o il [processo di avvio](https://docs.microsoft.com/it-it/windows/security/information-protection/secure-the-windows-10-boot-process) di Microsoft Windows con [TPM](https://docs.microsoft.com/it-it/windows/security/information-protection/tpm/how-windows-uses-the-tpm). Queste caratteristiche e tecnologie hardware possono tutte aiutare a prevenire la manomissione persistente da parte di malware o [attacchi di malintenzionati](https://en.wikipedia.org/wiki/Evil_Maid_attack)
- Un forte utilizzo del sandboxing come quello trovato in [MacOS](https://developer.apple.com/library/archive/documentation/Security/Conceptual/AppSandboxDesignGuide/AboutAppSandbox/AboutAppSandbox.html), [ChromeOS](https://chromium.googlesource.com/chromiumos/docs/+/HEAD/sandboxing.md), e [Android](https://source.android.com/security/app-sandbox). Le soluzioni di sandboxing su Linux comunemente usate come [Flatpak](https://docs.flatpak.org/en/latest/sandbox-permissions.html) e [Firejail](https://firejail.wordpress.com/) hanno ancora molta strada da fare
- Forte [mitigazione degli exploit](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations)

Nonostante questi inconvenienti, le distribuzioni desktop GNU/Linux sono ottime se si vuole:

- Evitare la telemetria che spesso viene fornita con sistemi operativi proprietari
- Mantenere [la libertà del software](https://www.gnu.org/philosophy/free-sw.it.html#four-freedoms)
- Avere sistemi operativi orientati alla privacy come [Whonix](https://www.whonix.org) o [Tails](https://tails.boum.org/)

Questa pagina usa il termine "Linux" per descrivere le distribuzioni desktop GNU/Linux. Altri sistemi operativi che usano a loro volta il kernel Linux come ChromeOS, Android e Qubes OS non sono discussi qui.

[Raccomandazioni su Linux :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Scelta della distribuzione

Non tutte le distribuzioni Linux sono uguali. Anche se la nostra pagina di raccomandazioni su Linux non vuole essere una fonte autorevole sulla distribuzione da utilizzare, ci sono alcune cose da tenere a mente quando si sceglie la distribuzione da utilizzare.

### Ciclo di rilascio

Si consiglia vivamente di scegliere distribuzioni che si mantengono vicine alle release stabili del software upstream, spesso indicate come distribuzioni rolling release. Questo perché le distribuzioni con ciclo di rilascio congelato spesso non aggiornano le versioni dei pacchetti e rimangono indietro sugli aggiornamenti di sicurezza.

Per le distribuzioni congelate, come [Debian](https://www.debian.org/security/faq#handling), ci si aspetta che i manutentori dei pacchetti facciano il backport delle patch per correggere le vulnerabilità, piuttosto che portare il software alla "versione successiva" rilasciata dallo sviluppatore upstream. Alcune correzioni di sicurezza [non](https://arxiv.org/abs/2105.14565) ricevono affatto un [CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) (in particolare i software meno diffusi) e quindi non vengono inserite nella distribuzione con questo modello di patch. Di conseguenza, le correzioni di sicurezza minori vengono talvolta rimandate alla successiva versione principale.

Non crediamo che trattenere i pacchetti e applicare patch provvisorie sia una buona idea, in quanto si discosta dal modo in cui lo sviluppatore avrebbe voluto far funzionare il software. [Richard Brown](https://rootco.de/aboutme/) ha una presentazione al riguardo:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/i8c0mg_mS7U?local=true" title="Regular Releases are Wrong, Roll for your life" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Aggiornamenti tradizionali vs Atomici

Tradizionalmente, le distribuzioni Linux si aggiornano con l'aggiornamento in sequenza dei pacchetti desiderati. Gli aggiornamenti tradizionali, come quelli utilizzati nelle distribuzioni basate su Fedora, Arch Linux e Debian possono essere meno affidabili se si dovesse verificare un errore durante l'aggiornamento.

Le distribuzioni che utilizzano aggiornamenti atomici applicano gli aggiornamenti per intero o non li applicano affatto. Di solito, i sistemi ad aggiornamento transazionali sono anche atomici.

Un sistema ad aggiornamento transazionale crea un'istantanea prima e dopo l'applicazione di un aggiornamento. Se un aggiornamento dovesse fallire per un qualsiasi motivo (magari per un'interruzione di corrente), è possibile ripristinare facilmente l'aggiornamento "all'ultimo stato valido."

Il metodo di aggiornamento Atomico viene utilizzato su distribuzioni immutabili come Silverblue, Tumbleweed, e NixOS e possono raggiungere l'affidabilità con questo modello. [Adam Šamalík](https://twitter.com/adsamalik) ha fornito una presentazione su come funziona `rpm-ostree` con Silverblue:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/-hpV5l-gJnQ?local=true" title="Let's try Fedora Silverblue — an immutable desktop OS! - Adam Šamalik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Distribuzioni "Incentrate sulla sicurezza"

Spesso si fa confusione tra distribuzioni "incentrate sulla sicurezza" e distribuzioni "pentesting". Una rapida ricerca per "la distribuzione Linux più sicura" darà spesso risultati come Kali Linux, Black Arch e Parrot OS. Queste distribuzioni sono distribuzioni per effettuare test di penetrazione offensivi che offrono strumenti per testare altri sistemi. Non includono nessuna "sicurezza aggiuntiva" o misure di sicurezza destinate ad un utilizzo regolare.

### Distribuzioni basate su Arch

Le distribuzioni basate su Arch sono sconsigliate per chi è alle prime armi con Linux, (indipendentemente dalla distribuzione) poiché richiedono una regolare [manuntenzione del sistema](https://wiki.archlinux.org/title/System_maintenance). Arch non dispone di un meccanismo di aggiornamento della distribuzione per le scelte software sottostanti. Di conseguenza, devi tenerti aggiornato circa le tendenze attuali e adottare nuove tecnologie man mano che sostituiscono le vecchie pratiche.

For a secure system, you are also expected to have sufficient Linux knowledge to properly set up security for their system such as adopting a [mandatory access control](https://en.wikipedia.org/wiki/Mandatory_access_control) system, setting up [kernel module](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) blacklists, hardening boot parameters, manipulating [sysctl](https://en.wikipedia.org/wiki/Sysctl) parameters, and knowing what components they need such as [Polkit](https://en.wikipedia.org/wiki/Polkit).

Anyone using the [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository), **must** be comfortable in auditing PKGBUILDs that they install from that service. AUR packages are community-produced content and are not vetted in any way, and therefore are vulnerable to software supply chain attacks, which has in fact happened [in the past](https://www.bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository/). AUR should always be used sparingly and often there is a lot of bad advice on various pages which direct people to blindly use [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) without sufficient warning. Similar warnings apply to use third-party Personal Package Archives (PPAs) on Debian based distributions or Community Projects (COPR) on Fedora.

If you are experienced with Linux and wish to use an Arch-based distribution, we only recommend mainline Arch Linux, not any of its derivatives. We recommend against these two Arch derivatives specifically:

- **Manjaro**: This distribution holds packages back for 2 weeks to make sure that their own changes don’t break, not to make sure that upstream is stable. When AUR packages are used, they are often built against the latest [libraries](https://en.wikipedia.org/wiki/Library_(computing)) from Arch’s repositories.
- **Garuda**: They use [Chaotic-AUR](https://aur.chaotic.cx/) which automatically and blindly compiles packages from the AUR. There is no verification process to make sure that the AUR packages don’t suffer from supply chain attacks.

### Kicksecure

While we strongly recommend against using outdated distributions like Debian, there is a Debian based operating system that has been hardened to be much more secure than typical Linux distributions: [Kicksecure](https://www.kicksecure.com/). Kicksecure, in oversimplified terms, is a set of scripts, configurations, and packages that substantially reduce the attack surface of Debian. It covers a lot of privacy and hardening recommendations by default.

### Linux-libre kernel and “Libre” distributions

We strongly recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://www.phoronix.com/scan.php?page=news_item&px=GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode for ideological reasons.

## Consigli generali

### Drive Encryption

Most Linux distributions have an option within its installer for enabling [LUKS](../encryption.md#linux-unified-key-setup) FDE. If this option isn’t set at installation time, you will have to backup your data and re-install, as encryption is applied after [disk partitioning](https://en.wikipedia.org/wiki/Disk_partitioning), but before [file systems](https://en.wikipedia.org/wiki/File_system) are formatted. We also suggest securely erasing your storage device:

- [Secure Data Erasure :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure/)

### Swap

Consider using [ZRAM](https://wiki.archlinux.org/title/Swap#zram-generator) or [encrypted swap](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) instead of unencrypted swap to avoid potential security issues with sensitive data being pushed to [swap space](https://en.wikipedia.org/wiki/Memory_paging). Fedora based distributions [use ZRAM by default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

### Wayland

We recommend using a desktop environment that supports the [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)) display protocol as it was developed with security [in mind](https://lwn.net/Articles/589147/). Its predecessor, [X11](https://en.wikipedia.org/wiki/X_Window_System), does not support GUI isolation, allowing all windows to [record screen, log and inject inputs in other windows](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), making any attempt at sandboxing futile. While there are options to do nested X11 such as [Xpra](https://en.wikipedia.org/wiki/Xpra) or [Xephyr](https://en.wikipedia.org/wiki/Xephyr), they often come with negative performance consequences and are not convenient to set up and are not preferable over Wayland.

Fortunately, common environments such as [GNOME](https://www.gnome.org), [KDE](https://kde.org), and the window manager [Sway](https://swaywm.org) have support for Wayland. Some distributions like Fedora and Tumbleweed use it by default, and some others may do so in the future as X11 is in [hard maintenance mode](https://www.phoronix.com/scan.php?page=news_item&px=X.Org-Maintenance-Mode-Quickly). If you’re using one of those environments it is as easy as selecting the “Wayland” session at the desktop display manager ([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)).

We recommend **against** using desktop environments or window managers that do not have Wayland support, such as Cinnamon (default on Linux Mint), Pantheon (default on Elementary OS), MATE, Xfce, and i3.

### Proprietary Firmware (Microcode Updates)

Linux distributions such as those which are [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre) or DIY (Arch Linux) don’t come with the proprietary [microcode](https://en.wikipedia.org/wiki/Microcode) updates that often patch vulnerabilities. Some notable examples of these vulnerabilities include [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), and other [hardware vulnerabilities](https://www.kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

We **highly recommend** that you install the microcode updates, as your CPU is already running the proprietary microcode from the factory. Fedora and openSUSE both have the microcode updates applied by default.

### Aggiornamenti

Most Linux distributions will automatically install updates or remind you to do so. It is important to keep your OS up to date so that your software is patched when a vulnerability is found.

Some distributions (particularly those aimed at advanced users) are more barebones and expect you to do things yourself (e.g. Arch or Debian). These will require running the "package manager" (`apt`, `pacman`, `dnf`, etc.) manually in order to receive important security updates.

Additionally, some distributions will not download firmware updates automatically. For that you will need to install [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

## Modifiche alla privacy

### Randomizzazione dell'indirizzo MAC

Many desktop Linux distributions (Fedora, openSUSE, etc.) will come with [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager), to configure Ethernet and Wi-Fi settings.

It is possible to [randomize](https://fedoramagazine.org/randomize-mac-address-nm/) the [MAC address](https://en.wikipedia.org/wiki/MAC_address) when using NetworkManager. This provides a bit more privacy on Wi-Fi networks as it makes it harder to track specific devices on the network you’re connected to. It does [**not**](https://papers.mathyvanhoef.com/wisec2016.pdf) make you anonymous.

We recommend changing the setting to **random** instead of **stable**, as suggested in the [article](https://fedoramagazine.org/randomize-mac-address-nm/).

If you are using [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), you will need to set [`MACAddressPolicy=random`](https://www.freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) which will enable [RFC 7844 (Anonymity Profiles for DHCP Clients)](https://www.freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

There isn’t many points in randomizing the MAC address for Ethernet connections as a system administrator can find you by looking at the port you are using on the [network switch](https://en.wikipedia.org/wiki/Network_switch). Randomizing Wi-Fi MAC addresses depends on support from the Wi-Fi’s firmware.

### Other Identifiers

There are other system identifiers which you may wish to be careful about. You should give this some thought to see if it applies to your [threat model](../basics/threat-modeling.md):

- **Hostnames:** Your system's hostname is shared with the networks you connect to. You should avoid including identifying terms like your name or operating system in your hostname, instead sticking to generic terms or random strings.
- **Usernames:** Similarly, your username is used in a variety of ways across your system. Consider using generic terms like "user" rather than your actual name.
- **Machine ID:**: During installation a unique machine ID is generated and stored on your device. Consider [setting it to a generic ID](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### System Counting

The Fedora Project [counts](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) how many unique systems access its mirrors by using a [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) variable instead of a unique ID. Fedora does this to determine load and provision better servers for updates where necessary.

This [option](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) is currently off by default. We recommend adding `countme=false` to `/etc/dnf/dnf.conf` just in case it is enabled in the future. On systems that use `rpm-ostree` such as Silverblue, the countme option is disabled by masking the [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems/) timer.

openSUSE also uses a [unique ID](https://en.opensuse.org/openSUSE:Statistics) to count systems, which can be disabled by deleting the `/var/lib/zypp/AnonymousUniqueId` file.
