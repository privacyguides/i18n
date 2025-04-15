---
title: Linux Overview
icon: simple/linux
description: Linux is an open-source, privacy-focused desktop operating system alternative, but not all distribitions are created equal.
---

**Linux** è un sistema operativo per desktop open source, alternativo e incentrato sulla privacy. In the face of pervasive telemetry and other privacy-encroaching technologies in mainstream operating systems, desktop Linux has remained the clear choice for people looking for total control over their computers from the ground up.

Il nostro sito web utilizza generalmente il termine "Linux" per descrivere le distribuzioni Linux per **desktop**. Altri sistemi operativi che utilizzano anch'essi il kernel di Linux, come ChromeOS, Android e Qubes OS non sono discussi su questa pagina.

[Consigli su Linux :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Security Notes

There are some notable security concerns with Linux which you should be aware of. Nonostante tali svantaggi, le distribuzioni di Linux per desktop sono comunque ottime per gran parte delle persone che desiderano:

- Evitare la telemetria fornita dai sistemi operativi proprietari
- Maintain [software freedom](https://gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Use privacy-focused systems such as [Whonix](../desktop.md#whonix) or [Tails](../desktop.md#tails)

### Sicurezza Open Source

It is a [common misconception](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) that Linux and other open-source software are inherently secure simply because the source code is available. There is an expectation that community verification occurs regularly, but this isn’t always [the case](https://seirdy.one/posts/2022/02/02/floss-security).

In realtà, la sicurezza della distribuzione dipende da numerosi fattori, come l'attività del progetto, l'esperienza dello sviluppatore, il livello di rigore applicato alle revisioni del codice e quanto spesso è data attenzione a parti specifiche della base di codice, che potrebbero non essere toccate per anni.

### Funzionalità di Sicurezza Mancanti

Al momento, il desktop Linux [è indietro rispetto alle alternative](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) come macOS o Android per quanto riguarda alcune funzionalità di sicurezza. Ci auguriamo di vedere miglioramenti in queste aree in futuro.

- L'**avvio verificato** su Linux non è robusto come le alternative, quali l'[Avvio Sicuro](https://support.apple.com/guide/security/secac71d5623/web) di Apple o l'[Avvio Verificato](https://source.android.com/security/verifiedboot) di Android. L'avvio verificato impedisce la manomissione persistente da parte di malware e da [attacchi evil maid](https://en.wikipedia.org/wiki/Evil_Maid_attack), ma è ancora in gran parte [non disponibile, anche sulle distribuzioni più avanzate](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- Il **sandboxing forte** per le app su Linux è fortemente carente, anche con app containerizzate, come Flatpaks, o le soluzioni di sandbox, come Firejail. Flatpak is the most promising sandboxing utility for Linux thus far, but is still deficient in many areas and allows for [unsafe defaults](https://flatkill.org/2020) which permit most apps to trivially bypass their sandbox.

Inoltre, Linux è in ritardo nell'implementazione delle [mitigazioni di exploit](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations), che sono ora lo standard sugli altri sistemi operativi, come Arbitrary Code Guard su Windows o Hardened Runtime su macOS. Inoltre, gran parte dei programmi per Linux e Linux stesso sono programmati in linguaggi non sicuri per la memoria. Memory corruption bugs are responsible for the [majority of vulnerabilities](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code) fixed and assigned a CVE. While this is also true for Windows and macOS, they are quickly making progress on adopting memory-safe languages such as Rust and Swift, respectively.

## Scegliere la tua distribuzione

Non tutte le distribuzioni Linux sono uguali. La nostra [pagina di consigli per Linux](../desktop.md) non è intesa come una fonte autorevole sulla quale distribuzione dovresti utilizzare, ma i nostri consigli *sono* allineati con le seguenti linee guida. Esistono alcune cose che dovresti tenere a mente scegliendo una distribuzione:

### Ciclo di rilascio

Ti consigliamo vivamente di scegliere le distribuzioni che restano vicine alle release stabili a monte del software, spesso note come distribuzioni a rilascio continuo. Questo perché le distribuzioni a rilascio congelato, spesso, non aggiornano le versioni dei pacchetti e restano indietro con gli aggiornamenti di sicurezza.

For frozen distributions such as [Debian](https://debian.org/security/faq#handling), package maintainers are expected to backport patches to fix vulnerabilities rather than bump the software to the “next version” released by the upstream developer. Some security fixes (particularly for less popular software) [do not](https://arxiv.org/abs/2105.14565) receive a [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) at all and therefore do not make it into the distribution with this patching model. As a result, minor security fixes are sometimes held back until the next major release.

Non crediamo che trattenere i pacchetti e applicare patch provvisorie sia una buona idea, poiché si discosta dal modo in cui lo sviluppatore avrebbe voluto che il software funzionasse. [Richard Brown](https://rootco.de/aboutme) has a presentation about this:

- [Regular Releases are Wrong, Roll for your life](https://youtu.be/i8c0mg_mS7U) <small>(YouTube)</small>

### Traditional vs Atomic Updates

Tradizionalmente, le distribuzioni di Linux si aggiornano tramite l'aggiornamento sequenziale dei pacchetti desiderati. Traditional updates such as those used in Fedora, Arch Linux, and Debian-based distributions can be less reliable if an error occurs while updating.

Distros which use atomic updates, on the other hand, apply updates in full or not at all. On an atomic distribution, if an error occurs while updating (perhaps due to a power failure), nothing is changed on the system.

The atomic update method can achieve reliability with this model and is used for [distributions](../desktop.md#atomic-distributions) like Silverblue and NixOS. [Adam Šamalík](https://twitter.com/adsamalik) provides a presentation on how `rpm-ostree` works with Silverblue:

- [Let's try Fedora Silverblue — an immutable desktop OS! - Adam Šamalík](https://youtu.be/-hpV5l-gJnQ) <small>(YouTube)</small>

### Distribuzioni "Incentrate sulla sicurezza"

Spesso si fa confusione tra distribuzioni "incentrate sulla sicurezza" e distribuzioni di "pentesting". Una rapida ricerca della “distribuzione Linux più sicura” mostrerà risultati come Kali Linux, Black Arch, o Parrot OS. Queste distribuzioni sono distribuzioni testate contro la penetrazione offensiva che impacchettano strumenti per testare altri sistemi. Non includono nessuna "ulteriore sicurezza" o mitigazione difensiva intesa per l'utilizzo regolare.

### Distribuzioni basate su Arch

Arch e le distribuzioni basate su Arch sono sconsigliate per coloro che sono alle prime armi con Linux (indipendentemente dalla distribuzione), poiché richiedono una regolare [manutenzione del sistema](https://wiki.archlinux.org/title/System_maintenance). Arch non dispone di un meccanismo di aggiornamento della distribuzione, per le scelte software sottostanti. As a result you have to stay aware with current trends and adopt technologies on your own as they supersede older practices.

For a secure system, you are also expected to have sufficient Linux knowledge to properly set up security for their system such as adopting a [mandatory access control](#mandatory-access-control) system, setting up [kernel module](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) blacklists, hardening boot parameters, manipulating [sysctl](https://en.wikipedia.org/wiki/Sysctl) parameters, and knowing what components they need such as [Polkit](https://en.wikipedia.org/wiki/Polkit).

Chiunque utilizzi il [Repository di Arch User (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository), **deve** essere a proprio agio nel controllare i PKGBUILD che scarica da tale servizio. AUR packages are community-produced content and are not vetted in any way, and therefore are vulnerable to software [:material-package-variant-closed-remove: Supply Chain Attacks](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}, which has in fact happened [in the past](https://bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository).

L'AUR dovrebbe sempre essere utilizzata con parsimonia e, spesso, esistono molti cattivi consigli, su varie pagine, che indirizzano le persone a utilizzare ciecamente gli [aiutanti AUR](https://wiki.archlinux.org/title/AUR_helpers), senza avvertimenti sufficienti. Similar warnings apply to the use of third-party Personal Package Archives (PPAs) on Debian-based distributions or Community Projects (COPR) on Fedora.

Se sei esperto con Linux e vorresti utilizzare una distribuzione basata su Arch, consigliamo generalmente la linea principale di Arch Linux, rispetto a qualsiasi suo derivato.

Inoltre, **sconsigliamo**, nello specifico, questi due derivati di Arch:

- **Manjaro**: Questa distribuzione trattiene i pacchetti per 2 settimane per assicurarsi che le proprie modifiche non si corrompano, non per assicurarsi che, tutto sia stabile a monte. Utilizzando i pacchetti AUR, sono spesso compilati con le [librerie](https://en.wikipedia.org/wiki/Library_(computing)) più recenti dai repository di Arch.
- **Garuda**: They use [Chaotic-AUR](https://aur.chaotic.cx) which automatically and blindly compiles packages from the AUR. Non esiste alcun processo di verifica per assicurarsi che i pacchetti di AUR non subiscano attacchi alla catena di distribuzione del software.

### Distribuzioni del kernel libero di Linux e "Libre"

We recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://phoronix.com/news/GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode.

### Mandatory access control

Mandatory access control is a set of additional security controls which help to confine parts of the system such as apps and system services. The two common forms of mandatory access control found in Linux distributions are [SELinux](https://github.com/SELinuxProject) and [AppArmor](https://apparmor.net). Fedora and Tumbleweed use SELinux by default, with Tumbleweed offering an option in its installer to choose AppArmor instead.

SELinux on [Fedora](https://docs.fedoraproject.org/en-US/quick-docs/selinux-getting-started) confines Linux containers, virtual machines, and service daemons by default. AppArmor is used by the snap daemon for [sandboxing](https://snapcraft.io/docs/security-sandboxing) snaps which have [strict](https://snapcraft.io/docs/snap-confinement) confinement such as [Firefox](https://snapcraft.io/firefox). There is a community effort to confine more parts of the system in Fedora with the [ConfinedUsers](https://fedoraproject.org/wiki/SIGs/ConfinedUsers) special interest group.

## Consigli generali

### Crittografia delle Unità

Molte delle distribuzioni Linux offrono un opzione nel proprio programma d'installazione per abilitare la FDE di [LUKS](../encryption.md#linux-unified-key-setup). If this option isn’t set at installation time, you will have to back up your data and re-install, as encryption is applied after [disk partitioning](https://en.wikipedia.org/wiki/Disk_partitioning), but before [file systems](https://en.wikipedia.org/wiki/File_system) are formatted. Inoltre, suggeriamo di svuotare il tuo dispositivo di archiviazione:

- [Cancellazione sicura dei dati :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure)

### Swap

Considera l'utilizzo della [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator), invece di un file di swap tradizionale o di una partizione, per evitare di scrivere dati della memoria potenzialmente sensibili, sull'archiviazione persistente (e migliorare le prestazioni). Le distribuzioni basate su Fedora [utilzzano la ZRAM di default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

Se richiedi la funzionalità di sospensione su disco (ibernazione), dovresti comunque utilizzare un file di swap o una partizione tradizionale. Assicurati che qualsiasi spazio di swap che possiedi disponga di un dispositivo di archiviazione persistente, come minimo [crittografato](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption), per mitigare alcune di queste minacce.

### Firmware Proprietario (Aggiornamenti al Microcodice)

Alcune distribuzioni di Linux (come le distribuzioni fai da te o basate su [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)), non dispongono degli aggiornamenti proprietari al [microcodice](https://en.wikipedia.org/wiki/Microcode), che correggono le vulnerabilità di sicurezza critiche. Some notable examples of these vulnerabilities include [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), and other [hardware vulnerabilities](https://kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

**Consigliamo vivamente** che installi gli aggiornamenti al microcodice, poiché contengono importanti correzioni di sicurezza per la CPU, che non sono completamente mitigabili dal solo software. Fedora and openSUSE both apply microcode updates by default.

### Aggiornamenti

Molte distribuzioni di Linux installano automaticamente gli aggiornamenti o ti ricordano di farlo. È importante mantenere aggiornato il sistema operativo, così che il tuo software sia subito corretto, all'individuazione di una vulnerabilità.

Alcune distribuzioni (in particolare quelle rivolte agli utenti avanzati) sono più scarne e si aspettano che tu faccia le cose da solo (ad esempio Arch o Debian). Per ricevere gli aggiornamenti di sicurezza importanti su queste distribuzioni è necessario eseguire manualmente il "gestore di pacchetti" (`apt`, `pacman`, `dnf`, ecc.).

Inoltre, alcune distribuzioni non scaricano in automatico gli aggiornamenti del firmware. For that, you will need to install [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

### Permission Controls

Desktop environments (DEs) that support the [Wayland](https://wayland.freedesktop.org) display protocol are [more secure](https://lwn.net/Articles/589147) than those that only support X11. However, not all DEs take full advantage of Wayland's architectural security improvements.

For example, GNOME has a notable edge in security compared to other DEs by implementing permission controls for third-party software that tries to [capture your screen](https://gitlab.gnome.org/GNOME/gnome-shell/-/issues/3943). That is, when a third-party application attempts to capture your screen, you are prompted for your permission to share your screen with the app.

<figure markdown>
  ![Screenshot permissions](../assets/img/linux/screenshot_permission.png){ width="450" }
  <figcaption>GNOME's screenshot permission dialog</figcaption>
</figure>

Many alternatives don't provide these same permission controls yet,[^1] while some are waiting for Wayland to implement these controls upstream.[^2]

## Miglioramenti della Privacy

### Randomizzazione dell'indirizzo MAC

Molte distribuzioni di Linux per desktop (Fedora, openSUSE, etc.), dispongono di [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) per configurare le impostazioni Ethernet e Wi-Fi.

It is possible to [randomize](https://fedoramagazine.org/randomize-mac-address-nm) the [MAC address](https://en.wikipedia.org/wiki/MAC_address) when using NetworkManager. Ciò fornisce una privacy lievemente migliore sulle reti Wi-Fi, complicando il tracciamento di dispositivi specifici sulla rete cui sei connesso. [**Non**](https://papers.mathyvanhoef.com/wisec2016.pdf) ti rende anonimo.

We recommend changing the setting to **random** instead of **stable**, as suggested in the [article](https://fedoramagazine.org/randomize-mac-address-nm).

Se stai utilizzando [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), dovrai impostare [`MACAddressPolicy=random`](https://freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) che abiliterà [RFC 7844 (Profili di Anonimato per i Client DHCP)](https://freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

La randomizzazione dell'indirizzo MAC è utile soprattutto per le connessioni Wi-Fi. Per le connessioni Ethernet, la randomizzazione dell'indirizzo MAC offre pochi vantaggi (o addirittura nessuno), perché un amministratore di rete può facilmente identificare il tuo dispositivo con altri mezzi (ad esempio ispezionando la porta a cui sei connesso sullo switch di rete). La randomizzazione degli indirizzi MAC del Wi-Fi dipende dal supporto del firmware del Wi-Fi.

### Altri identificatori

Esistono altri identificatori di sistema a cui dovresti prestare attenzione. Dovresti riflettere su questo aspetto, per capire se si applica al tuo [modello di minaccia](../basics/threat-modeling.md):

- **Nomi del host:** Il nome del host del tuo sistema è condiviso con le reti cui ti connetti. Dovresti evitare di includere i termini identificativi, come il tuo nome o sistema operativo nel tuo nome del host, piuttosto utilizzando termini generici o stringhe casuali.
- **Nomi utente:** Similmente, il tuo nome utente è utilizzato in vari modi nel tuo sistema. Cerca di utilizzare termini generici come "utente", piuttosto che il tuo nome reale.
- **Machine ID:** During installation, a unique machine ID is generated and stored on your device. Considera di [impostarlo a un ID generico](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### Conteggio di Sistema

Fedora Project [conteggia](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) quanti sistemi univoci accedono ai suoi mirror, utilizzando una variabile [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description), invece di un ID univoco. Fedora lo fa per determinare il carico e fornire server migliori per gli aggiornamenti, quando necessario.

Quest'[opzione](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) è disabilitata di default. Consigliamo di aggiungere `countme=false` a `/etc/dnf/dnf.conf` nel caso in cui venga abilitato in futuro. On systems that use `rpm-ostree` such as Silverblue, the `countme` option is disabled by masking the [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems) timer.

openSUSE also uses a [unique ID](https://en.opensuse.org/openSUSE:Statistics) to count systems, which can be disabled by emptying the `/var/lib/zypp/AnonymousUniqueId` file.

[^1]: KDE currently has an open proposal to add controls for screen captures: <https://invent.kde.org/plasma/xdg-desktop-portal-kde/-/issues/7>
[^2]: Sway is waiting to add specific security controls until they "know how security as a whole is going to play out" in Wayland: <https://github.com/swaywm/sway/issues/5118#issuecomment-600054496>
