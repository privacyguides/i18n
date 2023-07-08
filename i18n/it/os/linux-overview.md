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
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/i8c0mg_mS7U?local=true" title="I rilasci regolari sono sbagliati, quelli continui sono superiori" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Aggiornamenti tradizionali vs Atomici

Tradizionalmente, le distribuzioni Linux si aggiornano con l'aggiornamento in sequenza dei pacchetti desiderati. Gli aggiornamenti tradizionali, come quelli utilizzati nelle distribuzioni basate su Fedora, Arch Linux e Debian possono essere meno affidabili se si dovesse verificare un errore durante l'aggiornamento.

Le distribuzioni che utilizzano aggiornamenti atomici applicano gli aggiornamenti per intero o non li applicano affatto. Di solito, i sistemi ad aggiornamento transazionali sono anche atomici.

Un sistema ad aggiornamento transazionale crea un'istantanea prima e dopo l'applicazione di un aggiornamento. Se un aggiornamento dovesse fallire per un qualsiasi motivo (magari per un'interruzione di corrente), è possibile ripristinare facilmente l'aggiornamento "all'ultimo stato valido."

Il metodo di aggiornamento Atomico viene utilizzato su distribuzioni immutabili come Silverblue, Tumbleweed, e NixOS e possono raggiungere l'affidabilità con questo modello. [Adam Šamalík](https://twitter.com/adsamalik) ha fornito una presentazione su come funziona `rpm-ostree` con Silverblue:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/-hpV5l-gJnQ?local=true" title="Proviamo Fedora Silverblue — Un sistema operativo desktop immutabile! - Adam Šamalik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Distribuzioni "Incentrate sulla sicurezza"

Spesso si fa confusione tra distribuzioni "incentrate sulla sicurezza" e distribuzioni "pentesting". Una rapida ricerca per "la distribuzione Linux più sicura" darà spesso risultati come Kali Linux, Black Arch e Parrot OS. Queste distribuzioni sono distribuzioni per effettuare test di penetrazione offensivi che offrono strumenti per testare altri sistemi. Non includono nessuna "sicurezza aggiuntiva" o misure di sicurezza destinate ad un utilizzo regolare.

### Distribuzioni basate su Arch

Le distribuzioni basate su Arch sono sconsigliate per chi è alle prime armi con Linux, (indipendentemente dalla distribuzione) poiché richiedono una regolare [manuntenzione del sistema](https://wiki.archlinux.org/title/System_maintenance). Arch non dispone di un meccanismo di aggiornamento della distribuzione per le scelte software sottostanti. Di conseguenza, devi tenerti aggiornato circa le tendenze attuali e adottare nuove tecnologie man mano che sostituiscono le vecchie pratiche.

Per avere un sistema sicuro, ci si aspetta che tu abbia una sufficiente conoscenza di Linux per configurare correttamente la sicurezza del proprio sistema, come ad esempio l'adozione di un [sistema di controllo degli accessi obbligatorio](https://en.wikipedia.org/wiki/Mandatory_access_control), l'impostazione di [blacklist dei moduli del kernel](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security), rendere più efficaci i parametri di avvio, la manipolazione dei parametri [sysctl](https://en.wikipedia.org/wiki/Sysctl) e la conoscenza dei componenti necessari, come [Polkit](https://en.wikipedia.org/wiki/Polkit).

Chiunque utilizzi la [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository), **deve** essere a proprio agio nel verificare i PKGBUILDs che installano da quel servizio. I pacchetti AUR sono contenuti sviluppati dalla community e non sono controllati in alcun modo, e quindi sono vulnerabili ad attacchi alla catena del valore del software, cosa che in effetti è accaduta [in passato](https://www.bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository/). AUR dovrebbe essere sempre usato con parsimonia e spesso ci sono molti consigli pessimi su varie pagine che indirizzano le persone ad usare ciecamente gli [ helper AUR ](https://wiki.archlinux.org/title/AUR_helpers) senza sufficienti avvertimenti. Avvertenze simili si applicano all'utilizzo di archivi di pacchetti personali (PPA) di terze parti su distribuzioni basate su Debian o di progetti comunitari (COPR) su Fedora.

Se hai esperienza con Linux e vuoi usare una distribuzione basata su Arch, ti consigliamo soltanto la mainline di Arch Linux e non qualsiasi sua derivata. Sconsigliamo in particolare queste due derivate di Arch:

- **Manjaro**: Questa distribuzione trattiene i pacchetti per 2 settimane per assicurarsi che le proprie modifiche non diano errori, non per assicurarsi che l'upstream sia stabile. Quando si usano i pacchetti AUR, spesso vengono compilati con le ultime [librerie](https://en.wikipedia.org/wiki/Library_(computing)) dalle repository di Arch.
- **Garuda**: Utilizza [Chaotic-AUR](https://aur.chaotic.cx/) che compila automaticamente e alla cieca i pacchetti di AUR. Non c'è alcun processo di verifica per assicurarsi che i pacchetti AUR non subiscano attacchi alla catena del valore del software.

### Kicksecure

Sebbene sconsigliamo vivamente di utilizzare distribuzioni obsolete come Debian, esiste un sistema operativo basato su Debian reso molto più sicuro delle tipiche distribuzioni Linux: [Kicksecure](https://www.kicksecure.com/). Kicksecure, in termini molto semplici, è un insieme di script, configurazioni e pacchetti che riducono sostanzialmente la superficie di attacco di Debian. Copre molte delle raccomandazioni sulla privacy e sicurezza di default.

### Distribuzioni kernel linux-libre e "Libre"

**Sconsigliamo** vivamente di utilizzare il kernel Linux-libre, in quanto[rimuove parametri di sicurezza](https://www.phoronix.com/news/GNU-Linux-Libre-5.7-Released) e [sopprime gli avvisi del kernel](https://news.ycombinator.com/item?id=29674846) sul microcodice vulnerabile per motivi ideologici.

## Consigli generali

### Crittografia delle unità

Molte delle distribuzioni Linux hanno un opzione nel proprio programma d'installazione per abilitare [LUKS](../encryption.md#linux-unified-key-setup) FDE. Se questa opzione non viene impostata durante l'installazione, dovrai fare il backup dei tuoi dati e reinstallare, in quanto la crittografia viene applicata dopo [la partizione del disco](https://en.wikipedia.org/wiki/Disk_partitioning), ma prima della formattazione dei [file di sistema](https://en.wikipedia.org/wiki/File_system). Ti consigliamo inoltre di cancellare in modo sicuro il tuo dispositivo di archiviazione:

- [Cancellazione sicura dei dati :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure/)

### Swap

Consida l'utilizzo di [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) o [swap criptato](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) invece di swap non criptato per evitare potenziali problemi di sicurezza dovuti al trasferimento di dati sensibili nello [spazio di swap](https://en.wikipedia.org/wiki/Memory_paging). Le distribuzioni basate su Fedora [utilizzano ZRAM di default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

### Wayland

Consigliamo di utilizzare un ambiente desktop che supporti il protocollo grafico [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)) in quanto è stato sviluppato [tenendo conto](https://lwn.net/Articles/589147/) della sicurezza. Il suo predecessore, [X11](https://en.wikipedia.org/wiki/X_Window_System), non supporta l'isolamento della GUI, permettendo a tutte le finestre di [registrare lo schermo, registrare e dare input ad altre finestre](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), rendendo vano qualsiasi tentativo di fare sandboxing. Sebbene esistano opzioni per eseguire X11 annidato, come[Xpra](https://en.wikipedia.org/wiki/Xpra) o [Xephyr](https://en.wikipedia.org/wiki/Xephyr), spesso hanno un impatto negativo sulle prestazioni, non sono facili da configurare e non sono preferibili a Wayland.

Fortunatamente, ambienti comuni come [GNOME](https://www.gnome.org), [KDE](https://kde.org), e il gestore di finestre [Sway](https://swaywm.org) supportano Wayland. Alcune distribuzioni come Fedora e Tumbleweed lo usano di default e altre potrebbero farlo in futuro, dato che X11 è in [modalità di manutenzione](https://www.phoronix.com/news/X.Org-Maintenance-Mode-Quickly). Se stai utilizzando uno di questi ambienti è molto facile, basta selezionare la sessione “Wayland” nel display manager del desktop([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)).

**Sconsigliamo** di usare ambienti desktop o gestori di finestre che non hanno il supporto per Wayland, come Cinnamon (è di default su Linux Mint), Pantheon (è di default su Elementary OS), MATE, Xfce, e i3.

### Firmware Proprietario (Aggiornamenti microcodice)

Le distribuzioni Linux come queste, ovvero [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre) o DIY (Arch Linux) non vengono forniti con gli aggiornamenti del [microcodice](https://en.wikipedia.org/wiki/Microcode) proprietario che spesso patchano le vulnerabilità. Alcuni esempi significativi di queste vulnerabilità sono [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), e altre [vulnerabilità hardware](https://www.kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

Ti **consigliamo vivamente** di installare gli aggiornamenti del microcodice, poiché la tua CPU utilizza già il microcodice proprietario dalla fabbrica. Sia Fedora e openSUSE hanno gli aggiornamenti del microcodice applicati di default.

### Aggiornamenti

Molte distribuzioni Linux installano in automatico gli aggiornamenti o ti ricordano di farlo. È importante mantenere aggiornato il sistema operativo in modo che il tuo software venga subito patchato quando viene individuata una vulnerabilità.

Alcune distribuzioni (in particolare quelle rivolte ad utenti esperti) sono più scarne e si aspettano che tu faccia le cose da solo (ad esempio Arch o Debian). Per ricevere aggiornamenti di sicurezza importanti su queste distribuzioni è necessario eseguire manualmente il "gestore di pacchetti" (`apt`, `pacman`, `dnf`, ecc.).

Inoltre, alcune distribuzioni non scaricano in automatico gli aggiornamenti del firmware. Per questo dovrai installare [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

## Modifiche alla privacy

### Randomizzazione dell'indirizzo MAC

Molte distribuzioni Linux per desktop (Fedora, openSUSE, ecc.) sono dotate di [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager), per configurare le impostazioni Ethernet e Wi-Fi.

È possibile [randomizzare](https://fedoramagazine.org/randomize-mac-address-nm/) [l'indirizzo MAC](https://en.wikipedia.org/wiki/MAC_address) quando si utilizza NetworkManager. Questo fornisce una maggiore privacy sulle reti Wi-Fi, in quanto rende più difficile tracciare dispositivi specifici sulla rete a cui si è connessi. [**Non**](https://papers.mathyvanhoef.com/wisec2016.pdf) ti rende anonimo.

Ti consigliamo di cambiare l'impostazione in **random** anziché **stable**, come suggerito nell'[articolo](https://fedoramagazine.org/randomize-mac-address-nm/).

Se stai utilizzando [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), dovrai impostare [`MACAddressPolicy=random`](https://www.freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) che abiliterà [RFC 7844 (Profili anonimi per client DHCP)](https://www.freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

Non ha molto senso randomizzare l'indirizzo MAC per le connessioni Ethernet, poiché un amministratore di sistema può trovarti guardando la porta che stai utilizzando sullo [switch di rete](https://en.wikipedia.org/wiki/Network_switch). La randomizzazione degli indirizzi MAC del Wi-Fi dipende dal supporto del firmware del Wi-Fi.

### Altri identificatori

Esistono altri identificatori di sistema a cui dovresti fare attenzione. Dovresti riflettere su questo aspetto per vedere se si applica al tuo [modello di minaccia ](../basics/threat-modeling.md):

- **Nomi host:** Il nome host del tuo sistema è condiviso con la rete a cui sei connesso. Dovresti evitare di includere termini identificativi come il tuo nome o il sistema operativo nel tuo nome host, cerca invece di utilizzare termini generici o stringhe random.
- **Nomi utente:** Allo stesso modo, il tuo nome utente viene usato in vari modi nel tuo sistema. Cerca di usare termini generici come "utente" anziché il tuo vero nome.
- **ID Macchina:**: Durante l'installazione viene generato un ID macchina che viene memorizzato sul tuo dispositivo. Cerca di [impostarlo su un ID generico](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### Contatore del sistema

Il Fedora Project [conta](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) quanti sistemi unici accedono ai suoi mirrors utilizzando una variabile [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) anziché un ID unico. Fedora fa questo per determinare il carico e fornire server migliori per gli aggiornamenti, se necessario.

Questa [opzione](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) è disabilitata di default. Consigliamo di aggiungere `countme=false` a `/etc/dnf/dnf.conf` nel caso in cui venga abilitato in futuro. Sui sistemi che utilizzano `rpm-ostree` come Silverblue, l'opzione countme è disabilitata mascherando il timer [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems/).

anche openSUSE utilizza un [ID unico](https://en.opensuse.org/openSUSE:Statistics) per contare i sistemi, che può essere disabilitato cancellando il file `/var/lib/zypp/AnonymousUniqueId`.
