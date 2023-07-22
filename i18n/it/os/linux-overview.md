---
title: Panoramica su Linux
icon: simple/linux
description: Linux è un sistema operativo desktop, open source, incentrato sulla privacy e alternativo, ma non tutte le distribuzioni sono uguali.
---

**Linux** è un sistema operativo per desktop open-source, alternativo e incentrato sulla privacy. In the face of pervasive telemetry and other privacy-encroaching technologies in mainstream operating systems, Linux desktop has remained the clear choice for people looking for total control over their computers from the ground up.

Our website generally uses the term “Linux” to describe **desktop** Linux distributions. Other operating systems which also use the Linux kernel such as ChromeOS, Android, and Qubes OS are not discussed on this page.

[Consigli su Linux :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Note sulla Privacy

There are some notable privacy concerns with Linux which you should be aware of. Despite these drawbacks, desktop Linux distributions are still great for most people who want to:

- Evitare la telemetria fornita dai sistemi operativi proprietari
- Mantenere la [libertà del software](https://www.gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Use privacy focused systems such as [Whonix](https://www.whonix.org) or [Tails](https://tails.boum.org/)

### Open Source Security

It is a [common misconception](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) that Linux and other open-source software is inherently secure simply because the source code is available. There is an expectation that community verification occurs regularly, but this isn’t always [the case](https://seirdy.one/posts/2022/02/02/floss-security/).

In reality, distro security depends on a number of factors, such as project activity, developer experience, the level of rigor applied to code reviews, and how often attention is given to specific parts of the codebase that may go untouched for years.

### Missing Security Features

At the moment, desktop Linux [falls behind alternatives](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) like macOS or Android when it comes to certain security features. We hope to see improvements in these areas in the future.

- **Verified boot** on Linux is not as robust as alternatives such as Apple’s [Secure Boot](https://support.apple.com/guide/security/secac71d5623/web) or Android’s [Verified Boot](https://source.android.com/security/verifiedboot). Verified boot prevents persistent tampering by malware and [evil maid attacks](https://en.wikipedia.org/wiki/Evil_Maid_attack), but is still largely [unavailable on even the most advanced distributions](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- **Strong sandboxing** for apps on Linux is severely lacking, even with containerized apps like Flatpaks or sandboxing solutions like Firejail. Flatpak is the most promising sandboxing utility for Linux thus far, but is still deficient in many areas and allows for [unsafe defaults](https://flatkill.org/2020/) which allow most apps to trivially bypass their sandbox.

Additionally, Linux falls behind in implementing [exploit mitigations](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) which are now standard on other operating systems, such as Arbitrary Code Guard on Windows or Hardened Runtime on macOS. Also, most Linux programs and Linux itself are coded in memory-unsafe languages. Memory corruption bugs are responsible for the [majority of vulnerabilities](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code/) fixed and assigned a CVE. While this is also true for Windows and macOS, they are quickly making progress on adopting memory-safe languages—such as Rust and Swift, respectively—while there is no similar effort to rewrite Linux in a memory-safe language like Rust.

## Scegliere la tua distribuzione

Non tutte le distribuzioni Linux sono uguali. Our [Linux recommendation page](../desktop.md) is not meant to be an authoritative source on which distribution you should use, but our recommendations *are* aligned with the following guidelines. These are a few things you should keep in mind when choosing a distribution:

### Ciclo di rilascio

Ti consigliamo vivamente di scegliere le distribuzioni che restano vicine alle release stabili a monte del software, spesso note come distribuzioni a rilascio continuo. Questo perché le distribuzioni a rilascio congelato, spesso, non aggiornano le versioni dei pacchetti e restano indietro con gli aggiornamenti di sicurezza.

Per le distribuzioni congelate come [Debian](https://www.debian.org/security/faq#handling), i manutentori dei pacchetti dovrebbero effettuare il backport delle patch per correggere le vulnerabilità, piuttosto che portare il software alla "versione successiva", rilasciata dallo sviluppatore a monte. Some security fixes [do not](https://arxiv.org/abs/2105.14565) receive a [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) (particularly less popular software) at all and therefore do not make it into the distribution with this patching model. Di conseguenza, talvolta, le correzioni di sicurezza minori sono rimandate alla versione principale successiva.

Non crediamo che trattenere i pacchetti e applicare patch provvisorie sia una buona idea, poiché si discosta dal modo in cui lo sviluppatore avrebbe voluto che il software funzionasse. [Richard Brown](https://rootco.de/aboutme/) ha una presentazione a riguardo:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/i8c0mg_mS7U?local=true" title="Le versioni regolari sono sbagliate; rilasci continui per la vita!" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Aggiornamenti tradizionali vs Atomici

Tradizionalmente, le distribuzioni di Linux si aggiornano tramite l'aggiornamento sequenziale dei pacchetti desiderati. Gli aggiornamenti tradizionali, come quelli utilizzati sulle distribuzioni basate su Fedora, Arch Linux e Debian, possono essere meno affidabili se si verifica un errore durante l'aggiornamento.

Le distribuzioni ad aggiornamento atomico applicano gli aggiornamenti completi, o non li applicano affatto. Tipicamente, i sistemi di aggiornamento transazionali sono anch'essi atomici.

Un sistema di aggiornamento transazionale crea un'istantanea prim e dopo l'applicazione di un aggiornamento. Se un aggiornamento fallisce in qualsiasi momento (forse a causa di un guasto elettrico), l'aggiornamento è facilmente ripristinabile a un "ultimo buono stato noto."

Il modello d'aggiornamento Atomico è utilizzato per le distribuzioni immutabili come Silverblue, Tumbleweed e NixOS e può ottenere affidabilità con tale modello. [Adam Šamalík](https://twitter.com/adsamalik) ha fornito una presentazione sul funzionamento di `rpm-ostree` con Silverblue:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/-hpV5l-gJnQ?local=true" title="Proviamo Fedora Silverblue: un OS desktop immutabile! - Adam Šamalik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Distribuzioni "Incentrate sulla sicurezza"

Spesso si fa confusione tra distribuzioni "incentrate sulla sicurezza" e distribuzioni di "pentesting". A quick search for “the most secure Linux distribution” will often give results like Kali Linux, Black Arch, or Parrot OS. Queste distribuzioni sono distribuzioni testate contro la penetrazione offensiva che impacchettano strumenti per testare altri sistemi. Non includono nessuna "ulteriore sicurezza" o mitigazione difensiva intesa per l'utilizzo regolare.

### Distribuzioni basate su Arch

Arch and Arch-based distributions are not recommended for those new to Linux (regardless of distribution) as they require regular [system maintenance](https://wiki.archlinux.org/title/System_maintenance). Arch does not have a distribution update mechanism for the underlying software choices. Di conseguenza, devi tenerti aggiornato con le tendenze attuali e adottare tecnologie, a mano a mano che sostituiscono le vecchie pratiche.

Per avere un sistema sicuro, si suppone che tu abbia una conoscenza sufficiente di Linux per configurarne adeguatamente la sicurezza, come adottando un sistema di [controllo obbligatorio dell'accesso](https://en.wikipedia.org/wiki/Mandatory_access_control), configurando liste nere del [modulo del kernel](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security), rafforzando la sicurezza dei parametri d'avvio, manipolando i parametri [sysctl](https://en.wikipedia.org/wiki/Sysctl) e conoscendo quali componenti necessitano, come [Polkit](https://en.wikipedia.org/wiki/Polkit).

Anyone using the [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **must** be comfortable auditing PKGBUILDs that they download from that service. I pacchetti AUR sono contenuti prodotti dalla community e non sono controllati in alcun modo e, dunque, sono vulnerabili agli attacchi alla catena di distribuzione dei softwre, che, difatti, si sono verificati [in passato](https://www.bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository/).

The AUR should always be used sparingly, and often there is a lot of bad advice on various pages which direct people to blindly use [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) without sufficient warning. Simili avvertenze si applicano all'utilizzo di Archivi di Pacchetti Personali (PPA) di terze parti sulle distribuzioni basate su Debian, o dei Progetti della Community (COPR) su Fedora.

If you are experienced with Linux and wish to use an Arch-based distribution, we generally recommend mainline Arch Linux over any of its derivatives.

Additionally, we recommend **against** these two Arch derivatives specifically:

- **Manjaro**: Questa distribuzione trattiene i pacchetti per 2 settimane per assicurarsi che le proprie modifiche non si corrrompano, non per assicurarsi che, tutto sia stabile a monte. Utilizzando i pacchetti AUR, sono spesso compilati con le [librerie](https://en.wikipedia.org/wiki/Library_(computing)) più recenti dalle repository di Arch.
- **Garuda**: Utilizza [Chaotic-AUR](https://aur.chaotic.cx/) che compila automaticamente e alla cieca i pacchetti da AUR. Non esiste alcun processo di verifica per assicurarsi che i pacchetti di AUR non subiscano attacchi alla catena di distribuzione del software.

### Distribuzioni del kernel libero di Linux e "Libre"

We recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://www.phoronix.com/news/GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode.

## Consigli generali

### Crittografia delle Unità

Molte delle distribuzioni Linux offrono un opzione nel proprio programma d'installazione per abilitare il FDE di [LUKS](../encryption.md#linux-unified-key-setup). Se quest'opzione non è impostata all'installazione, dovrai eseguire il backup dei tuoi dati e reinstallare, poiché la crittografia è applicata dopo la [partizione del disco](https://en.wikipedia.org/wiki/Disk_partitioning), ma prima della formattazione dei [file di sistema](https://en.wikipedia.org/wiki/File_system). Inoltre, suggeriamo di svuotare il tuo dispositivo di archiviazione:

- [Cancellazione sicura dei dati :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure/)

### Swap

Consider using [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) instead of a traditional swap file or partition to avoid writing potentially sensitive memory data to persistent storage (and improve performance). Fedora-based distributions [use ZRAM by default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

If you require suspend-to-disk (hibernation) functionality, you will still need to use a traditional swap file or partition. Make sure that any swap space you do have on a persistent storage device is [encrypted](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) at a minimum to mitigate some of these threats.

### Wayland

We recommend using a desktop environment that supports the [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)) display protocol, as it was developed with security [in mind](https://lwn.net/Articles/589147/). Its predecessor ([X11](https://en.wikipedia.org/wiki/X_Window_System)) does not support GUI isolation, which allows any window to [record, log, and inject inputs in other windows](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), making any attempt at sandboxing futile. While there are options to do nested X11 such as [Xpra](https://en.wikipedia.org/wiki/Xpra) or [Xephyr](https://en.wikipedia.org/wiki/Xephyr), they often come with negative performance consequences, and are neither convenient to set up nor preferable over Wayland.

Fortunatamente, ambienti comuni come [GNOME](https://www.gnome.org), [KDE](https://kde.org), e il gestore di finestre [Sway](https://swaywm.org), supportano Wayland. Alcune distribuzioni come Fedora e Tumbleweed lo utilizzano di default, mentre altre potrebbero farlo in futuro, dato che X11 è in [modalità di manutenzione](https://www.phoronix.com/news/X.Org-Maintenance-Mode-Quickly). Se stai utilizzando uno di questi ambienti è molto facile, basta selezionare la sessione “Wayland” nel gestore dello schermo del desktop([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)).

**Sconsigliamo** di utilizzare ambienti desktop o gestori di finestre che non hanno supportano Wayland, come Cinnamon (predefinito su Linux Mint), Pantheon (predefinito su Elementary OS), MATE, Xfce e i3.

### Firmware Proprietario (Aggiornamenti al Microcodice)

Some Linux distributions (such as [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)-based or DIY distros) don’t come with the proprietary [microcode](https://en.wikipedia.org/wiki/Microcode) updates which patch critical security vulnerabilities. Alcuni esempi significativi di queste vulnerabilità includono [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), e altre [vulnerabilità hardware](https://www.kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

We **highly recommend** that you install microcode updates, as they contain important security patches for the CPU which can not be fully mitigated in software alone. Sia Fedora che openSUSE hanno gli aggiornamenti del microcodice applicati di default.

### Aggiornamenti

Molte distribuzioni di Linux installano automaticamente gli aggiornamenti o ti ricordano di farlo. È importante mantenere aggiornato il sistema operativo, così che il tuo software sia subito corretto, all'individuazione di una vulnerabilità.

Some distributions (particularly those aimed at advanced users) are more bare bones and expect you to do things yourself (e.g. Arch or Debian). Per ricevere gli aggiornamenti di sicurezza importanti, queste richiederanno l'esecuzione del "gestore di pacchetti" (`apt`, `pacman`, `dnf`, etc.).

Inoltre, alcune distribuzioni non scaricano in automatico gli aggiornamenti del firmware. Per questo, dovrai installare [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

## Miglioramenti della Privacy

### Casualizzazione dell'Indirizzo MAC

Many desktop Linux distributions (Fedora, openSUSE, etc.) come with [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) to configure Ethernet and Wi-Fi settings.

È possibile [casualizzre](https://fedoramagazine.org/randomize-mac-address-nm/) l'[indirizzo MAC](https://en.wikipedia.org/wiki/MAC_address), utilizzando NetworkManager. Ciò fornisce una privacy lievemente migliore sulle reti Wi-Fi, complicando il tracciamento di dispositivi specifici sulla rete cui sei connesso. [**Non**](https://papers.mathyvanhoef.com/wisec2016.pdf) ti rende anonimo.

Consigliamo di modificare l'impostazione a **casuale**, invece che a **stabile**, come suggerito nell'[articolo](https://fedoramagazine.org/randomize-mac-address-nm/).

Se stai utilizzando [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), dovrai impostare [`MACAddressPolicy=random`](https://www.freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=), che abiliterà [RFC 7844 (Profili Anonimi per i Client DHCP)](https://www.freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

MAC address randomization is primarily beneficial for Wi-Fi connections. For Ethernet connections, randomizing your MAC address provides little (if any) benefit, because a network administrator can trivially identify your device by other means (such as inspecting the port you are connected to on the network switch). La casualizzazione degli indirizzi MAC della Wi-Fi, dipende dal supporto dal firmware della Wi-Fi.

### Altri identificatori

Esistono altri identificatori di sistema a cui dovresti prestare attenzione. Dovresti riflettere su questo aspetto, per capire se si applica al tuo [modello di minaccia](../basics/threat-modeling.md):

- **Nomi del host:** Il nome del host del tuo sistema è condiviso con le reti cui ti connetti. Dovresti evitare di includere i termini identificativi, come il tuo nome o sistema operativo nel tuo nome del host, piuttosto utilizzando termini generici o stringhe casuali.
- **Nomi utente:** Similmente, il tuo nome utente è utilizzato in vari modi nel tuo sistema. Cerca di utilizzare termini generici come "utente", piuttosto che il tuo nome reale.
- **ID della macchina:** Durante l'installazione, viene generato un ID della macchina univoco, memorizzato sul tuo dispositivo. Considera di [impostarlo a un ID generico](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### Conteggio di Sistema

Fedora Project [conteggia](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) quanti sistemi univoci accedono ai suoi mirror, utilizzando una variabile [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description), invece di un ID univoco. Fedora lo fa per determinare il carico e fornire server migliori per gli aggiornamenti, quando necessario.

Quest'[opzione](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) è disabilitata di default. Consigliamo di aggiungere `countme=false` a `/etc/dnf/dnf.conf` nel caso in cui venga abilitato in futuro. Sui sistemi che utilizzano `rpm-ostree`, come Silverblue, l'opzione countme è disabilitata mascherando il timer [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems/).

Anche openSUSE utilizza un [ID univoco](https://en.opensuse.org/openSUSE:Statistics) per contare i sistemi, disabilitabili eliminando il file `/var/lib/zypp/AnonymousUniqueId`.
