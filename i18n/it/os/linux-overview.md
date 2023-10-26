---
title: Panoramica su Linux
icon: simple/linux
description: Linux è un sistema operativo desktop, open source, incentrato sulla privacy e alternativo, ma non tutte le distribuzioni sono uguali.
---

**Linux** è un sistema operativo per desktop open-source, alternativo e incentrato sulla privacy. Di fronte alla telemetria pervasiva e altre tecnologie che violano la privacy nei sistemi operativi tradizionali, i desktop Linux sono rimasti la scelta migliore per coloro che vorrebbero il pieno controllo sui propri computer, da cima a fondo.

Il nostro sito web utilizza generalmente il termine "Linux" per descrivere le distribuzioni Linux per **desktop**. Altri sistemi operativi che utilizzano anch'essi il kernel di Linux, come ChromeOS, Android e Qubes OS non sono discussi su questa pagina.

[Consigli su Linux :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Note sulla Privacy

Esistono alcune notevoli preoccupazioni sulla privacy con Linux, di cui dovresti essere consapevole. Nonostante tali svantaggi, le distribuzioni di Linux per desktop sono comunque ottime per gran parte delle persone che desiderano:

- Evitare la telemetria fornita dai sistemi operativi proprietari
- Mantenere la [libertà del software](https://www.gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Utilizzare sistemi incentrati sulla privacy come [Whonix](https://www.whonix.org) o [Tails](https://tails.boum.org/)

### Sicurezza Open Source

È una convinzione [comunemente errata](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) che Linux e altri software open-source siano intrinsecamente sicuri semplicemente perché il codice sorgente è disponibile. Ci si aspetta che la verifica della community si verifichi regolarmente, ma ciò non è sempre [il caso](https://seirdy.one/posts/2022/02/02/floss-security/).

In realtà, la sicurezza della distribuzione dipende da numerosi fattori, come l'attività del progetto, l'esperienza dello sviluppatore, il livello di rigore applicato alle revisioni del codice e quanto spesso è data attenzione a parti specifiche della base di codice, che potrebbero non essere toccate per anni.

### Funzionalità di Sicurezza Mancanti

Al momento, il desktop Linux [è indietro rispetto alle alternative](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) come macOS o Android per quanto riguarda alcune funzionalità di sicurezza. Ci auguriamo di vedere miglioramenti in queste aree in futuro.

- L'**avvio verificato** su Linux non è robusto come le alternative, quali l'[Avvio Sicuro](https://support.apple.com/guide/security/secac71d5623/web) di Apple o l'[Avvio Verificato](https://source.android.com/security/verifiedboot) di Android. L'avvio verificato impedisce la manomissione persistente da parte di malware e da [attacchi evil maid](https://en.wikipedia.org/wiki/Evil_Maid_attack), ma è ancora in gran parte [non disponibile, anche sulle distribuzioni più avanzate](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- Il **sandboxing forte** per le app su Linux è fortemente carente, anche con app containerizzate, come Flatpaks, o le soluzioni di sandbox, come Firejail. Flatpak è l'utlità di sandboxing più promettente per Linux finora, ma è ancora carente in molte aree e consente [valori predefiniti non sicuri](https://flatkill.org/2020/), che consentono a gran parte delle app di superare banalmente tale sandbox.

Inoltre, Linux è in ritardo nell'implementazione delle [mitigazioni di exploit](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations), che sono ora lo standard sugli altri sistemi operativi, come Arbitrary Code Guard su Windows o Hardened Runtime su macOS. Inoltre, gran parte dei programmi per Linux e Linux stesso sono programmati in linguaggi non sicuri per la memoria. I bug di corruzione della memoria sono responsabili per [gran parte delle vulnerabilità](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code/) risolte e cui è stato assegnato un CVE. Sebbene ciò sia vero anche per Windows e per macOS, stanno rapidamente facendo progressi nell'adottare linguaggi sicuri per la memoria, come Rust e Swift, rispttivamente, mentre non sembra esistere un simile sforzo per la riscrittura di Linux in un linguaggo sicuro per la memoria, come Rust.

## Scegliere la tua distribuzione

Non tutte le distribuzioni Linux sono uguali. La nostra [pagina di consigli per Linux](../desktop.md) non è intesa come una fonte autorevole sulla quale distribuzione dovresti utilizzare, ma i nostri consigli *sono* allineati con le seguenti linee guida. Esistono alcune cose che dovresti tenere a mente scegliendo una distribuzione:

### Ciclo di rilascio

Ti consigliamo vivamente di scegliere le distribuzioni che restano vicine alle release stabili a monte del software, spesso note come distribuzioni a rilascio continuo. Questo perché le distribuzioni a rilascio congelato, spesso, non aggiornano le versioni dei pacchetti e restano indietro con gli aggiornamenti di sicurezza.

Per le distribuzioni congelate come [Debian](https://www.debian.org/security/faq#handling), i manutentori dei pacchetti dovrebbero effettuare il backport delle patch per correggere le vulnerabilità, piuttosto che portare il software alla "versione successiva", rilasciata dallo sviluppatore a monte. Alcune correzioni di sicurezza [non](https://arxiv.org/abs/2105.14565) ricevono affatto un [ID CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) (software particolarmente meno popolare) e, dunque, non arrivano alla distribuzione con questo modello di correzione. Di conseguenza, talvolta, le correzioni di sicurezza minori sono rimandate alla versione principale successiva.

Non crediamo che trattenere i pacchetti e applicare patch provvisorie sia una buona idea, poiché si discosta dal modo in cui lo sviluppatore avrebbe voluto che il software funzionasse. [Richard Brown](https://rootco.de/aboutme/) ha una presentazione a riguardo:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/i8c0mg_mS7U?local=true" title="Le versioni regolari sono sbagliate; rilasci continui per la vita!" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Aggiornamenti tradizionali vs Atomici

Tradizionalmente, le distribuzioni di Linux si aggiornano tramite l'aggiornamento sequenziale dei pacchetti desiderati. Gli aggiornamenti tradizionali, come quelli utilizzati sulle distribuzioni basate su Fedora, Arch Linux e Debian, possono essere meno affidabili se si verifica un errore durante l'aggiornamento.

Le distribuzioni ad aggiornamento atomico applicano gli aggiornamenti completi, o non li applicano affatto. Tipicamente, i sistemi di aggiornamento transazionali sono anch'essi atomici.

Un sistema ad aggiornamento transazionale crea un'istantanea prima e dopo l'applicazione di un aggiornamento. Se un aggiornamento fallisce in qualsiasi momento (forse a causa di un guasto elettrico), l'aggiornamento è facilmente ripristinabile a un "ultimo buono stato noto."

Il modello d'aggiornamento Atomico è utilizzato per le distribuzioni immutabili come Silverblue, Tumbleweed e NixOS e può ottenere affidabilità con tale modello. [Adam Šamalík](https://twitter.com/adsamalik) ha fornito una presentazione sul funzionamento di `rpm-ostree` con Silverblue:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/-hpV5l-gJnQ?local=true" title="Proviamo Fedora Silverblue: un OS desktop immutabile! - Adam Šamalik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Distribuzioni "Incentrate sulla sicurezza"

Spesso si fa confusione tra distribuzioni "incentrate sulla sicurezza" e distribuzioni di "pentesting". Una rapida ricerca della “distribuzione Linux più sicura” mostrerà risultati come Kali Linux, Black Arch, o Parrot OS. Queste distribuzioni sono distribuzioni testate contro la penetrazione offensiva che impacchettano strumenti per testare altri sistemi. Non includono nessuna "ulteriore sicurezza" o mitigazione difensiva intesa per l'utilizzo regolare.

### Distribuzioni basate su Arch

Arch e le distribuzioni basate su Arch sono sconsigliate per coloro che sono alle prime armi con Linux (indipendentemente dalla distribuzione), poiché richiedono una regolare [manutenzione del sistema](https://wiki.archlinux.org/title/System_maintenance). Arch non dispone di un meccanismo di aggiornamento della distribuzione, per le scelte software sottostanti. Di conseguenza, devi tenerti aggiornato con le tendenze attuali e adottare tecnologie, a mano a mano che sostituiscono le vecchie pratiche.

Per avere un sistema sicuro, si suppone che tu abbia una conoscenza sufficiente di Linux per configurarne adeguatamente la sicurezza, come adottando un sistema di [controllo obbligatorio dell'accesso](https://en.wikipedia.org/wiki/Mandatory_access_control), configurando liste nere del [modulo del kernel](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security), rafforzando la sicurezza dei parametri d'avvio, manipolando i parametri [sysctl](https://en.wikipedia.org/wiki/Sysctl) e conoscendo quali componenti necessitano, come [Polkit](https://en.wikipedia.org/wiki/Polkit).

Chiunque utilizzi il [Repository di Arch User (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository), **deve** essere a proprio agio nel controllare i PKGBUILD che scarica da tale servizio. I pacchetti AUR sono contenuti prodotti dalla community e non sono controllati in alcun modo e, dunque, sono vulnerabili agli attacchi alla catena di distribuzione dei softwre, che, difatti, si sono verificati [in passato](https://www.bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository/).

L'AUR dovrebbe sempre essere utilizzata con parsimonia e, spesso, esistono molti cattivi consigli, su varie pagine, che indirizzano le persone a utilizzare ciecamente gli [aiutanti AUR](https://wiki.archlinux.org/title/AUR_helpers), senza avvertimenti sufficienti. Simili avvertenze si applicano all'utilizzo di Archivi di Pacchetti Personali (PPA) di terze parti sulle distribuzioni basate su Debian, o dei Progetti della Community (COPR) su Fedora.

Se sei esperto con Linux e vorresti utilizzare una distribuzione basata su Arch, consigliamo generalmente la linea principale di Arch Linux, rispetto a qualsiasi suo derivato.

Inoltre, **sconsigliamo**, nello specifico, questi due derivati di Arch:

- **Manjaro**: Questa distribuzione trattiene i pacchetti per 2 settimane per assicurarsi che le proprie modifiche non si corrrompano, non per assicurarsi che, tutto sia stabile a monte. Utilizzando i pacchetti AUR, sono spesso compilati con le [librerie](https://en.wikipedia.org/wiki/Library_(computing)) più recenti dai repository di Arch.
- **Garuda**: Utilizza [Chaotic-AUR](https://aur.chaotic.cx/) che compila automaticamente e alla cieca i pacchetti da AUR. Non esiste alcun processo di verifica per assicurarsi che i pacchetti di AUR non subiscano attacchi alla catena di distribuzione del software.

### Distribuzioni del kernel libero di Linux e "Libre"

**Sconsigliamo** l'utilizzo del kernel libero di Linux, poiché [rimuove delle mitigazioni di sicurezza](https://www.phoronix.com/news/GNU-Linux-Libre-5.7-Released) e [sopprime gli avvertimenti del kernel](https://news.ycombinator.com/item?id=29674846), sul microcodice vulnerabile.

## Consigli generali

### Crittografia delle Unità

Molte delle distribuzioni Linux offrono un opzione nel proprio programma d'installazione per abilitare la FDE di [LUKS](../encryption.md#linux-unified-key-setup). Se questa opzione non viene impostata durante l'installazione, dovrai fare il backup dei tuoi dati e reinstallare, in quanto la crittografia viene applicata dopo [la partizione del disco](https://en.wikipedia.org/wiki/Disk_partitioning), ma prima della formattazione dei [file di sistema](https://en.wikipedia.org/wiki/File_system). Inoltre, suggeriamo di svuotare il tuo dispositivo di archiviazione:

- [Cancellazione sicura dei dati :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure/)

### Swap

Considera l'utilizzo della [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator), invece di un file di swap tradizionale o di una partizione, per evitare di scrvere dati della memoria potenzialmente sensibili, sull'archiviazione persistente (e migliorare le prestazioni). Le distribuzioni basate su Fedora [utilzzano la ZRAM di default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

Se richiedi la funzionalità di sospensione su disco (ibernazione), dovresti comunque utilizzare un file di swap o una partizione tradizionale. Assicurati che qualsiasi spazio di swap che possiedi disponga di un dispositivo di archiviazione persistente, come minimo [crittografato](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption), per mitigare alcune di queste minacce.

### Wayland

Consigliamo di utilizzare un ambiente desktop che supporti il protocollo di visualizzazione di [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)), sviluppato tenendo [a mente](https://lwn.net/Articles/589147/) la sicurezza. Il suo predecessore ([X11](https://en.wikipedia.org/wiki/X_Window_System)) non supporta l'isolamento della GUI, che consente a qualsiasi finestra di [registrare e iniettare input in altre finestre](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), rendendo futile qualsiasi tentativo di sandboxing. Sebbene esistano delle opzioni per eseguire X11 nidificato, quali [Xpra](https://en.wikipedia.org/wiki/Xpra) o [Xephyr](https://en.wikipedia.org/wiki/Xephyr), queste, spesso, presentano delle conseguenze negative sulle prestazioni e non sono né comode da configurare, né preferibili a Wayland.

Fortunatamente, ambienti comuni come [GNOME](https://www.gnome.org), [KDE](https://kde.org), e il gestore di finestre [Sway](https://swaywm.org), supportano Wayland. Alcune distribuzioni come Fedora e Tumbleweed lo utilizzano di default, mentre altre potrebbero farlo in futuro, dato che X11 è in [modalità di manutenzione](https://www.phoronix.com/news/X.Org-Maintenance-Mode-Quickly). Se stai utilizzando uno di questi ambienti è molto facile, basta selezionare la sessione “Wayland” nel gestore dello schermo del desktop([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)).

**Sconsigliamo** di usare ambienti desktop o gestori di finestre che non hanno il supporto per Wayland, come Cinnamon (è di default su Linux Mint), Pantheon (è di default su Elementary OS), MATE, Xfce, e i3.

### Firmware Proprietario (Aggiornamenti al Microcodice)

Alcune distribuzioni di Linux (come le distribuzioni fai da te o basate su [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)), non dispongono degli aggiornamenti proprietari al [microcodice](https://en.wikipedia.org/wiki/Microcode), che correggono le vulnerabilità di sicurezza critiche. Alcuni esempi significativi di queste vulnerabilità includono [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), e altre [vulnerabilità hardware](https://www.kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

**Consigliamo vivamente** che installi gli aggiornamenti al microcodice, poiché contengono importanti correzioni di sicurezza per la CPU, che non sono completamente mitigabili dal solo software. Sia Fedora che openSUSE hanno gli aggiornamenti del microcodice applicati di default.

### Aggiornamenti

Molte distribuzioni di Linux installano automaticamente gli aggiornamenti o ti ricordano di farlo. È importante mantenere aggiornato il sistema operativo in modo che il tuo software venga subito corretto quando viene individuata una vulnerabilità.

Alcune distribuzioni (in particolare quelle rivolte agli utenti avanzati) sono più scarne e si aspettano che tu faccia le cose da solo (ad esempio Arch o Debian). Per ricevere gli aggiornamenti di sicurezza importanti su queste distribuzioni è necessario eseguire manualmente il "gestore di pacchetti" (`apt`, `pacman`, `dnf`, ecc.).

Inoltre, alcune distribuzioni non scaricano in automatico gli aggiornamenti del firmware. Per questo, dovrai installare [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

## Miglioramenti della Privacy

### Randomizzazione dell'indirizzo MAC

Molte distribuzioni di Linux per desktop (Fedora, openSUSE, etc.), dispongono di [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) per configurare le impostazioni Ethernet e Wi-Fi.

È possibile [randomizzare](https://fedoramagazine.org/randomize-mac-address-nm/) [l'indirizzo MAC](https://en.wikipedia.org/wiki/MAC_address) quando si utilizza NetworkManager. Ciò fornisce una privacy lievemente migliore sulle reti Wi-Fi, complicando il tracciamento di dispositivi specifici sulla rete cui sei connesso. [**Non**](https://papers.mathyvanhoef.com/wisec2016.pdf) ti rende anonimo.

Consigliamo di modificare l'impostazione a **casuale**, invece che a **stabile**, come suggerito nell'[articolo](https://fedoramagazine.org/randomize-mac-address-nm/).

Se stai utilizzando [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), dovrai impostare [`MACAddressPolicy=random`](https://www.freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=), che abiliterà [RFC 7844 (Profili Anonimi per i Client DHCP)](https://www.freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

La randomizzazione dell'indirizzo MAC è utile soprattutto per le connessioni Wi-Fi. Per le connessioni Ethernet, la randomizzazione dell'indirizzo MAC offre pochi vantaggi (o addirittura nessuno), perché un amministratore di rete può facilmente identificare il tuo dispositivo con altri mezzi (ad esempio ispezionando la porta a cui sei connesso sullo switch di rete). La casualizzazione degli indirizzi MAC della Wi-Fi, dipende dal supporto dal firmware della Wi-Fi.

### Altri identificatori

Esistono altri identificatori di sistema a cui dovresti prestare attenzione. Dovresti riflettere su questo aspetto, per capire se si applica al tuo [modello di minaccia](../basics/threat-modeling.md):

- **Nomi del host:** Il nome del host del tuo sistema è condiviso con le reti cui ti connetti. Dovresti evitare di includere i termini identificativi, come il tuo nome o sistema operativo nel tuo nome del host, piuttosto utilizzando termini generici o stringhe casuali.
- **Nomi utente:** Similmente, il tuo nome utente è utilizzato in vari modi nel tuo sistema. Cerca di utilizzare termini generici come "utente", piuttosto che il tuo nome reale.
- **ID della macchina:** Durante l'installazione, viene generato un ID della macchina univoco, memorizzato sul tuo dispositivo. Considera di [impostarlo a un ID generico](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### Conteggio di Sistema

Fedora Project [conteggia](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) quanti sistemi univoci accedono ai suoi mirror, utilizzando una variabile [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description), invece di un ID univoco. Fedora lo fa per determinare il carico e fornire server migliori per gli aggiornamenti, quando necessario.

Quest'[opzione](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) è disabilitata di default. Consigliamo di aggiungere `countme=false` a `/etc/dnf/dnf.conf` nel caso in cui venga abilitato in futuro. Sui sistemi che utilizzano `rpm-ostree`, come Silverblue, l'opzione countme è disabilitata mascherando il timer [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems/).

anche openSUSE utilizza un [ID unico](https://en.opensuse.org/openSUSE:Statistics) per contare i sistemi, che può essere disabilitato cancellando il file `/var/lib/zypp/AnonymousUniqueId`.
