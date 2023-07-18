---
title: Panoramica su Linux
icon: simple/linux
description: Linux è un sistema operativo desktop, open source, incentrato sulla privacy e alternativo, ma non tutte le distribuzioni sono uguali.
---

Spesso si ritiene che un software [open source](https://en.wikipedia.org/wiki/Open-source_software) sia intrinsecamente sicuro, poiché il codice sorgente è disponibile. Ci si aspeetta che la verifica dalla community si verifichi regolarmente; tuttavia, questo non è sempre [il caso](https://seirdy.one/posts/2022/02/02/floss-security/). Dipende da numerosi fattori, come l'attività del progetto, l'esperienza degli sviluppatori, il livello di rigore applicato alle [revisioni del codice](https://en.wikipedia.org/wiki/Code_review) e a quanto spesso l'attenzione è prestata a parti specifiche della [base di codice](https://en.wikipedia.org/wiki/Codebase), che potrebbe rimanere inalterata per anni.

Al momento, Linux presenta delle aree che potrebbero essere migliorate, rispetto aalle sue controparti proprietarie, es.:

- Una catena d'avvio verificata, come l'[Avvio Sicuro](https://support.apple.com/guide/security/startup-security-utility-secc7b34e5b5/web) di Apple (con [Secure Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1)), l'[Avvio Verificato](https://source.android.com/security/verifiedboot) di Android, l'[Avvio verificato](https://www.chromium.org/chromium-os/chromiumos-design-docs/security-overview/#verified-boot) di ChromeOS, o il [processo d'avvio](https://docs.microsoft.com/en-us/windows/security/information-protection/secure-the-windows-10-boot-process) di Microsoft Windows, con [TPM](https://docs.microsoft.com/en-us/windows/security/information-protection/tpm/how-windows-uses-the-tpm). Queste funzionalità e tecnologie hardware possono aiutare a prevenire la manomissione persistente da parte di malware o [attacchi di evil maid](https://en.wikipedia.org/wiki/Evil_Maid_attack)
- Una forte soluzione di sandboxing, come quella di [macOS](https://developer.apple.com/library/archive/documentation/Security/Conceptual/AppSandboxDesignGuide/AboutAppSandbox/AboutAppSandbox.html), [ChromeOS](https://chromium.googlesource.com/chromiumos/docs/+/HEAD/sandboxing.md) e [Android](https://source.android.com/security/app-sandbox). Le soluzioni di sandboxing di Linux utilizzate comunemente, come [Flatpak](https://docs.flatpak.org/en/latest/sandbox-permissions.html) e [Firejail](https://firejail.wordpress.com/), hanno ancora molta strada da fare
- Forte [mitigazione degli exploit](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations)

Nonostante questi svantaggi, le distribuzioni di Linux per desktop sono ottime se desideri:

- Evitare la telemetria fornita dai sistemi operativi proprietari
- Mantenere la [libertà del software](https://www.gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Avere sistemi orientati alla password, come [Whonix](https://www.whonix.org) o [Tails](https://tails.boum.org/)

Questa pagina utilizza il termine "Linux" per descrivere le distribuzioni di Linux per desktop. Altri sistemi operativi che utilizzano anch'essi il kernel di Linux, come ChromeOS, Android e Qubes OS non sono discussi qui.

[Consigli su Linux :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Scegliere la tua distribuzione

Non tutte le distribuzioni Linux sono uguali. Sebbene la nostra pagina di consigli su Linux non sia intesa come una fonte autorevole sulla distribuzione che dovresti utilizzare, esistono delle cose che dovresti tenere a mente scegliendo quale distribuzione utilizzare.

### Ciclo di rilascio

Ti consigliamo vivamente di scegliere le distribuzioni che restano vicine alle release stabili a monte del software, spesso note come distribuzioni a rilascio continuo. Questo perché le distribuzioni a rilascio congelato, spesso, non aggiornano le versioni dei pacchetti e restano indietro con gli aggiornamenti di sicurezza.

Per le distribuzioni congelate come [Debian](https://www.debian.org/security/faq#handling), i manutentori dei pacchetti dovrebbero effettuare il backport delle patch per correggere le vulnerabilità, piuttosto che portare il software alla "versione successiva", rilasciata dallo sviluppatore a monte. Alcune correzioni di sicurezza [non](https://arxiv.org/abs/2105.14565) ricevono affatto un [CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) (software particolarmente meno diffuso) e, dunque, non arrivano alla distribuzione con questo modello di patch. Di conseguenza, talvolta, le correzioni di sicurezza minori sono rimandate alla versione principale successiva.

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

Spesso si fa confusione tra distribuzioni "incentrate sulla sicurezza" e distribuzioni di "pentesting". Una rapida ricerca per la "distribuzione Linux più sicura", restituirà spesso risultati come Kali Linux, Black Arch e Parrot OS. Queste distribuzioni sono distribuzioni testate contro la penetrazione offensiva che impacchettano strumenti per testare altri sistemi. Non includono nessuna "ulteriore sicurezza" o mitigazione difensiva intesa per l'utilizzo regolare.

### Distribuzioni basate su Arch

Le distribuzioni basate su Arch sono sconsigliate per coloro che sono alle prime armi con Linux, (indipendentemente dalla distribuzione), poiché richiedono una regolare [manuntenzione del sistema](https://wiki.archlinux.org/title/System_maintenance). Arch non dispone di un meccanismo d'aggiornamento della distribuzione per le scelte software sottostanti. Di conseguenza, devi tenerti aggiornato con le tendenze attuali e adottare tecnologie, a mano a mano che sostituiscono le vecchie pratiche.

Per avere un sistema sicuro, si suppone che tu abbia una conoscenza sufficiente di Linux per configurarne adeguatamente la sicurezza, come adottando un sistema di [controllo obbligatorio dell'accesso](https://en.wikipedia.org/wiki/Mandatory_access_control), configurando liste nere del [modulo del kernel](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security), rafforzando la sicurezza dei parametri d'avvio, manipolando i parametri [sysctl](https://en.wikipedia.org/wiki/Sysctl) e conoscendo quali componenti necessitano, come [Polkit](https://en.wikipedia.org/wiki/Polkit).

Chiunque utilizzi la [Repository di Arch User (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository), **deve** essere a proprio agio nel controllare i PKGBUILD che installano da tale servizio. I pacchetti AUR sono contenuti prodotti dalla community e non sono controllati in alcun modo e, dunque, sono vulnerabili agli attacchi alla catena di distribuzione dei softwre, che, difatti, si sono verificati [in passato](https://www.bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository/). AUR dovrebbe sempre essere utilizzato con parsimonia e, spesso, ci sono molti cattivi consigli su varie pagine, che indirizzano le persone a utilizzare ciecamente gli [aiutanti AUR](https://wiki.archlinux.org/title/AUR_helpers), senza avvertimenti sufficienti. Simili avvertenze si applicano all'utilizzo di Archivi di Pacchetti Personali (PPA) di terze parti sulle distribuzioni basate su Debian, o dei Progetti della Community (COPR) su Fedora.

Se hai esperienza con Linux e desideri utilizzare una distribuzione basata su Arch, consigliaamo esclusivamente la linea principale di Arch Linux, non alcuno dei suoi derivati. Sconsigliamo in particolare questi due derivati di Arch:

- **Manjaro**: Questa distribuzione trattiene i pacchetti per 2 settimane per assicurarsi che le proprie modifiche non si corrrompano, non per assicurarsi che, tutto sia stabile a monte. Utilizzando i pacchetti AUR, sono spesso compilati con le [librerie](https://en.wikipedia.org/wiki/Library_(computing)) più recenti dalle repository di Arch.
- **Garuda**: Utilizza [Chaotic-AUR](https://aur.chaotic.cx/) che compila automaticamente e alla cieca i pacchetti da AUR. Non esiste alcun processo di verifica per assicurarsi che i pacchetti di AUR non subiscano attacchi alla catena di distribuzione del software.

### Kicksecure

Sebbene sconsigliamo vivamente di utilizzare distribuzioni obsolete come Debian, esiste un sistema operativo basato su Debian che è stato reso molto più sicuro delle tipiche distribuzioni Linux: [Kicksecure](https://www.kicksecure.com/). Kicksecure, in breve, è una serie di script, configurazioni e pacchetti che riducono sostanzialmente la superficie di attacco di Debian. Copre di default molti dei consigli sulla privacy e la sicurezza.

### Distribuzioni del kernel libero di Linux e "Libre"

**Sconsigliamo** vivamente di utilizzare il kernel libero di Linux, poiché [rimuove le mitigazioni di sicurezza](https://www.phoronix.com/news/GNU-Linux-Libre-5.7-Released) e [sopprime gli avvisi del kernel](https://news.ycombinator.com/item?id=29674846), sul microcodice vulnerabile, per motivi ideologici.

## Consigli generali

### Crittografia delle Unità

Molte delle distribuzioni Linux offrono un opzione nel proprio programma d'installazione per abilitare il FDE di [LUKS](../encryption.md#linux-unified-key-setup). Se quest'opzione non è impostata all'installazione, dovrai eseguire il backup dei tuoi dati e reinstallare, poiché la crittografia è applicata dopo la [partizione del disco](https://en.wikipedia.org/wiki/Disk_partitioning), ma prima della formattazione dei [file di sistema](https://en.wikipedia.org/wiki/File_system). Inoltre, suggeriamo di svuotare il tuo dispositivo di archiviazione:

- [Cancellazione sicura dei dati :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure/)

### Swap

Considera l'utilizzo della [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) o della [swap crittografata](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption), invece della swap non crittografata, per evitare potenziali problemi di sicurezza dovuti al trasferimento di dati sensibili, allo [spazio di swap](https://en.wikipedia.org/wiki/Memory_paging). Le distribuzioni basate su Fedora [utilizzano la ZRAM di default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

### Wayland

Consigliamo l'utilizzo di un ambiente desktop che supporti il protocollo grafico [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)), essendo sviluppato [tenendo a mente](https://lwn.net/Articles/589147/) la sicurezza. Il suo predecessore, [X11](https://en.wikipedia.org/wiki/X_Window_System), non supporta l'isolamento della GUI, consentendo a tutte le finestre di [registrare lo schermo, registrare e iniettare input in altre finestre](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), rendendo futile ogni tentativo di sandboxing. Sebbene esistano altre opzioni per eseguire X11 nidifcato, quali [Xpra](https://en.wikipedia.org/wiki/Xpra) o [Xephyr](https://en.wikipedia.org/wiki/Xephyr), queste, spesso presentano delle conseguenze negative sulle prestazioni e non sono facili da configurare e non sono preferibili a Wayland.

Fortunatamente, ambienti comuni come [GNOME](https://www.gnome.org), [KDE](https://kde.org), e il gestore di finestre [Sway](https://swaywm.org), supportano Wayland. Alcune distribuzioni come Fedora e Tumbleweed lo utilizzano di default, mentre altre potrebbero farlo in futuro, dato che X11 è in [modalità di manutenzione](https://www.phoronix.com/news/X.Org-Maintenance-Mode-Quickly). Se stai utilizzando uno di questi ambienti è molto facile, basta selezionare la sessione “Wayland” nel gestore dello schermo del desktop([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)).

**Sconsigliamo** di utilizzare ambienti desktop o gestori di finestre che non hanno supportano Wayland, come Cinnamon (predefinito su Linux Mint), Pantheon (predefinito su Elementary OS), MATE, Xfce e i3.

### Firmware Proprietario (Aggiornamenti al Microcodice)

Le distribuzioni di Linux come queste, ovvero [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre) o DIY (Arch Linux) non sono fornite con gli aggiornamenti proprietari al [microcodice](https://en.wikipedia.org/wiki/Microcode) che, spesso, correggono le vulnerabilità. Alcuni esempi significativi di queste vulnerabilità includono [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), e altre [vulnerabilità hardware](https://www.kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

Ti **consigliamo vivamente** di installare gli aggiornamenti al microcodice, poiché la tua CPU sta già eseguendo il microcodice proprietario dalla fabbrica. Sia Fedora che openSUSE hanno gli aggiornamenti del microcodice applicati di default.

### Aggiornamenti

Molte distribuzioni di Linux installano automaticamente gli aggiornamenti o ti ricordano di farlo. È importante mantenere aggiornato il sistema operativo, così che il tuo software sia subito corretto, all'individuazione di una vulnerabilità.

Alcune distribuzioni (in particolare quelle mirate agli utenti avanzati) sono più scarne e si aspettano che tu faccia le cose da solo (es., Arch o Debian). Per ricevere gli aggiornamenti di sicurezza importanti, queste richiederanno l'esecuzione del "gestore di pacchetti" (`apt`, `pacman`, `dnf`, etc.).

Inoltre, alcune distribuzioni non scaricano in automatico gli aggiornamenti del firmware. Per questo, dovrai installare [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

## Miglioramenti della Privacy

### Casualizzazione dell'Indirizzo MAC

Molte distribuzioni di Linux per desktop (Fedora, openSUSE, etc.), sono dotate di [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager), per configurare le impostazioni Ethernet e Wi-Fi.

È possibile [casualizzre](https://fedoramagazine.org/randomize-mac-address-nm/) l'[indirizzo MAC](https://en.wikipedia.org/wiki/MAC_address), utilizzando NetworkManager. Ciò fornisce una privacy lievemente migliore sulle reti Wi-Fi, complicando il tracciamento di dispositivi specifici sulla rete cui sei connesso. [**Non**](https://papers.mathyvanhoef.com/wisec2016.pdf) ti rende anonimo.

Consigliamo di modificare l'impostazione a **casuale**, invece che a **stabile**, come suggerito nell'[articolo](https://fedoramagazine.org/randomize-mac-address-nm/).

Se stai utilizzando [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), dovrai impostare [`MACAddressPolicy=random`](https://www.freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=), che abiliterà [RFC 7844 (Profili Anonimi per i Client DHCP)](https://www.freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

Non ha molto senso casualizzre l'indirizzo MAC per le connessioni Ethernet, poiché un amministratore di sistema può trovarti osservando la porta che stai utilizzando sul [commutatore di rete](https://en.wikipedia.org/wiki/Network_switch). La casualizzazione degli indirizzi MAC della Wi-Fi, dipende dal supporto dal firmware della Wi-Fi.

### Altri identificatori

Esistono altri identificatori di sistema a cui dovresti prestare attenzione. Dovresti riflettere su questo aspetto, per capire se si applica al tuo [modello di minaccia](../basics/threat-modeling.md):

- **Nomi del host:** Il nome del host del tuo sistema è condiviso con le reti cui ti connetti. Dovresti evitare di includere i termini identificativi, come il tuo nome o sistema operativo nel tuo nome del host, piuttosto utilizzando termini generici o stringhe casuali.
- **Nomi utente:** Similmente, il tuo nome utente è utilizzato in vari modi nel tuo sistema. Cerca di utilizzare termini generici come "utente", piuttosto che il tuo nome reale.
- **ID della macchina:** Durante l'installazione, viene generato un ID della macchina univoco, memorizzato sul tuo dispositivo. Considera di [impostarlo a un ID generico](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### Conteggio di Sistema

Fedora Project [conteggia](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) quanti sistemi univoci accedono ai suoi mirror, utilizzando una variabile [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description), invece di un ID univoco. Fedora lo fa per determinare il carico e fornire server migliori per gli aggiornamenti, quando necessario.

Quest'[opzione](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) è disabilitata di default. Consigliamo di aggiungere `countme=false` a `/etc/dnf/dnf.conf` nel caso in cui venga abilitato in futuro. Sui sistemi che utilizzano `rpm-ostree`, come Silverblue, l'opzione countme è disabilitata mascherando il timer [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems/).

Anche openSUSE utilizza un [ID univoco](https://en.opensuse.org/openSUSE:Statistics) per contare i sistemi, disabilitabili eliminando il file `/var/lib/zypp/AnonymousUniqueId`.
