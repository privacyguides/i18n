---
title: "Desktop/PC"
icon: simple/linux
description: Le distribuzioni di Linux sono consigliate per la protezione della privcy e la libertà dei software.
cover: desktop.png
---

Le distribuzioni di Linux sono comunemente consigliate per la protezione della privacy e la libertà dei software. Se non utilizzi già Linux, seguono alcune distribuzioni che suggeriamo di provare, nonché consigli generali sul miglioramento della privacy e della sicurezza, applicabili a molte distribuzioni di Linux.

- [Panoramica generale di Linux :material-arrow-right-drop-circle:](os/linux-overview.md)

## Distribuzioni tradizionali

### Fedora Workstation

!!! recommendation

    ![Logo di Fedora](/assets/img/linux-desktop/fedora-workstation.svg){ align=right }
    
    **Fedora Workstation** è la distribuzione che consiigliamo per le persone nuove a Linux. Generalmente, Fedora, adotta le tecnologie più recenti prima delle altre distribuzioni, ad esempio, [Wayland](https://wayland.freedesktop.org/) e [PipeWire](https://pipewire.org). Queste, spesso, comportano miglioramenti alla sicurezza, privacy e utilizzabilità, in generale.
    
    [:octicons-home-16: Home](https://getfedora.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=Documentazione}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribuisci }

Fedora ha un ciclo di rilascio semi continuo. Mentre alcuni pacchetti come [GNOME](https://www.gnome.org) sono congelati fino alla prossima versione di Fedora, la maggior parte dei pacchetti (incluso il kernel) sono aggiornati frequentemente durante il ciclo di vita della versione.  Ogni versione di Fedora è supportata per un anno, con una nuova versione rilasciata ogni 6 mesi.

### openSUSE Tumbleweed

!!! recommendation

    ![Logo di openSUSE Tumbleweed](/assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }
    
    **openSUSE Tumbleweed** è una distribuzione stabile a rilascio continuo.
    
    openSUSE Tumbleweed dispone di un sistema di [aggiornamenti "transazionali"](https://kubic.opensuse.org/blog/2018-04-04-transactionalupdates/) che utilizza [Btrfs](https://it.wikipedia.org/wiki/Btrfs) e [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) per garantire che le istantanee possano essere ripristinate in caso di problemi.
    
    [:octicons-home-16: Home](https://get.opensuse.org/tumbleweed/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://doc.opensuse.org/){ .card-link title=Documentazione}
    [:octicons-heart-16:](https://shop.opensuse.org/){ .card-link title=Contribuisci }

Tumbleweed segue un modello di rilascio continuo in cui ogni aggiornamento è rilasciato come un'istantanea della distribuzione. Quando l'utente aggiorna il proprio sistema, viene scaricata una nuova istantanea. Ogni istantanea viene sottoposta a una serie di test automatizzati da [openQA](https://openqa.opensuse.org) per garantirne la qualità.

### Arch Linux

!!! recommendation

    ![Logo di Arch](/assets/img/linux-desktop/archlinux.svg){ align=right }
    
    **Arch Linux** è una distribuzione leggera e fai-da-te, il che significa che ottieni soltanto ciò che installi. Per ulteriori informazioni visita le loro [Domande Frequenti](https://wiki.archlinux.org/title/Frequently_asked_questions).
    
    [:octicons-home-16: Home](https://archlinux.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://wiki.archlinux.org/){ .card-link title=Documentazione}
    [:octicons-heart-16:](https://archlinux.org/donate/){ .card-link title=Contribuisci }

Arch Linux ha un ciclo di rilascio continuo. Non esiste un piano di rilascio fisso e i pacchetti sono aggiornati molto frequentemente.

Essendo una distribuzione fai da te, [dovresti configurare e mantenere](#arch-based-distributions) il tuo sistema per conto tuo. Arch dispone di un [installatore ufficiale](https://wiki.archlinux.org/title/Archinstall) per semplificare il processo di installazione.

Gran parte dei [pacchetti di Arch Linux](https://reproducible.archlinux.org) sono [riproducibili](https://reproducible-builds.org).

## Distribuzioni immutabili

### Fedora Silverblue

!!! recommendation

    ![Logo di Fedora Silverblue](/assets/img/linux-desktop/fedora-silverblue.svg){ align=right }
    
    **Fedora Silverblue** e **Fedora Kinoite** sono varianti immutabili di Fedora con una forte attenzione al flussi di lavoro dei contenitori. Silverblue è fornito con l'ambiente desktop [GNOME](https://www.gnome.org/), mentre Kinoite è fornito con [KDE](https://kde.org/). Silverblue e Kinoite seguono lo stesso piano di rilascio di Fedora Workstation, beneficiando dagli stessi aggiornamenti veloci e rimanendo molto vicini alla versione a monte.
    
    [:octicons-home-16: Home](https://silverblue.fedoraproject.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/it/fedora-silverblue//){ .card-link title=Documentazione}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribuisci }

Silverblue (e Kinoite) differiscono da Fedora Workstation poiché sostituiscono il gestore di pacchetti [DNF](https://fedoraproject.org/wiki/DNF) con un'alternativa molto più avanzata, detta [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/rawhide/system-administrators-guide/package-management/rpm-ostree/). Il gestore di pacchetti `rpm-ostree` opera scaricando un'immagine di base per il sistema, quindi sovrapponendo i pacchetti in un albero di commit simile a [git](https://en.wikipedia.org/wiki/Git). Quando il sistema viene aggiornato, viene scaricata una nuova immagine di base e le sovrapposizioni sono applicate a questa nuova immagine.

Al termine dell'aggiornamento, il sistema sarà riavviato nella nuova distribuzione. `rpm-ostree` mantiene due distribuzioni del sistema, così da poter facilmente essere ripristinato, se qualcosa si rompe nella nuova distribuzione. Inoltre, esiste l'opzione di aggiungere altre distribuzioni, se necessario.

[Flatpak](https://www.flatpak.org) è il metodo d'installazione principale dei pacchetti su queste distribuzioni, in quanto `rpm-ostree` è pensato soltanto per sovrapporre all'immagine di base i pacchetti che non possono rimanere all'interno di un contenitore.

Come alternativa a Flatpaks, esiste l'opzione di [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox/) per creare contenitori [Podman](https://podman.io) con una cartella home condivisa con il sistema operativo del host che imita un ambiente tradizionale di Fedora, un [caratteristica utile](https://containertoolbx.org) per gli sviluppatori esigenti.

### NixOS

!!! recommendation

    ![Logo di NixOS](assets/img/linux-desktop/nixos.svg){ align=right }
    
    NixOS è una distribuzione indipendente basata sul gestore di pacchetti Nix, incentrata sulla riproducibilità e l'affidabilità.
    
    [:octicons-home-16: Home](https://nixos.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=Documentazione}
    [:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=Contribuisci }

Il gestore di pacchetti di NixOS conserva ogni versione di ogni pacchetto in una cartella diversa del **negozio di Nix**. A causa di ciò puoi avere versioni differenti dello stesso pacchetto installate sul tuo sistema. Dopo la scrittura dei contenuti del pacchetto alla cartella, questa è resa di sola lettura.

NixOS fornisce anche aggiornamenti atomici; prima scarica (o crea) i pacchetti e i file per la nuova generazione di sistema, poi passa ad essi. Esistono svariati modi per passare a una nuova generazione; puoi chiedere a NixOS di attivarla dopo il riavvio, o passarci mentre è in esecuzione. Puoi anche *testare* la nuova generazione passandovi durante l'esecuzione, ma non impostarla come quella corrente di sistema. Se qualcosa nel processo d'aggiornamento si corrompe, basta riavviare e tornare automaticamente a una versione funzionante del sistema.

Nix, il gestore di pacchetti, utilizza un linguaggio puramente funzionale, anch'ess detto Nix, per definire i pacchetti.

[Nixpkgs](https://github.com/nixos/nixpkgs) (la fonte principale dei pacchetti) è contenuto in un'unica repository di GitHub. Inoltre, puoi definire i tuoi pacchetti nello stesso linguaggio, quindi, includerli facilmente nella tua configurazione.

Nix è un gestore di pacchetti basato sul codice sorgente; se non ne esiste alcuno di predefinito nella cache binaria, Nix creerà semplicemente il pacchetto dalla sorgente, utilizzandone la definizione. Crea ogni pacchetto in un ambiente sandbox *puro*, il più indipendente possibile dal sistema di host, rendendo riproducibili i binari.

## Distribuzioni incentrate sull'anonimato

### Whonix

!!! recommendation

    ![Logo di Whonix](assets/img/linux-desktop/whonix.svg){ align=right }
    
    **Whonix** è basato su [Kicksecure](https://www.whonix.org/wiki/Kicksecure), una biforcazione di Debian, focalizzata sulla sicurezza. Mira a fornire privacy, sicurezza e anonimato su Internet. Whonix è meglio utilizzato insieme a [Qubes OS](#qubes-os).
    
    [:octicons-home-16: Home](https://www.whonix.org/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://www.dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Servizio Onion" }
    [:octicons-info-16:](https://www.whonix.org/wiki/Documentation){ .card-link title=Documentazione}
    [:octicons-heart-16:](https://www.whonix.org/wiki/Donate){ .card-link title=Contribuisci }

Whonix è pensato per operare come due macchine virtuali: una "Workstation" e un "Gateway" di Tor. Tutte le comunicazioni dalla Workstation devono passare per il gateway di Tor. Ciò significa che, anche se la Workstation fosse compromessa da un malware di qualche tipo, il vero indirizzo IP rimarrebbe nascosto.

Alcune delle sue funzionalità includono l'Isolamento del Flusso di Tor, l'[anonimato di battitura](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak), lo [swap crittografato](https://github.com/Whonix/swap-file-creator) e un allocatore di memoria rafforzato.

Le versioni future di Whonix potrebbero includere [politiche di sistema complete di AppArmor](https://github.com/Whonix/apparmor-profile-everything) e un [launcher di app sandbox](https://www.whonix.org/wiki/Sandbox-app-launcher), per confinare completamente tutti i processi sul sistema.

Whonix è meglio utilizzato [insieme a Qubes](https://www.whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers), Qubes-Whonix presenta svariati [svantaggi](https://forums.whonix.org/t/qubes-whonix-security-disadvantages-help-wanted/8581) rispetto ad altri hypervisor.

### Tails

!!! recommendation

    ![Logo di Tails](assets/img/linux-desktop/tails.svg){ align=right }
    
    **Tails** è un sistema operativo live basato su Debian che instrada tutte le comunicazioni attraverso Tor, che può essere avviato su quasi tutti i computer da un'installazione su DVD, chiavetta USB o scheda SD. Utilizza [Tor](tor.md) per preservare la privacy e l'anonimato, aggirando la censura e non lasciando traccia di sé sul computer utilizzato, una volta spento.
    
    [:octicons-home-16: Home](https://tails.boum.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://tails.boum.org/doc/index.en.html){ .card-link title=Documentazione}
    [:octicons-heart-16:](https://tails.boum.org/donate/){ .card-link title=Contribuisci }

Tail è ottimo per le controperizie grazie all'amnesia (a significare che nulla viene scritto sul disco); tuttavia, non è una distribuzione rafforzata come Whonix. Manca di molte funzionalità per l'anonimato e la sicurezza possedute da Whonix e viene aggiornato molto meno spesso (soltanto una volta ogni sei settimane). Un sistema Tails compromesso da un malware potrebbe aggirare il proxy trasparente, consentendo all'utente di essere deanonimizzato.

Tails include di default [uBlock Origin](desktop-browsers.md#ublock-origin) nel Tor Browser, il che potrebbe semplificare, per gli avversari, il fingerprinting dei suoi utenti. Le macchine virtuali di [Whonix](desktop.md#whonix) potrebbero essere maggiormente a prova di fuga, tuttavia, non sono amnesiche, a significare che i dati potrebbero essere recuperati dal tuo dispositivo d'archiviazione.

Di design, Tails dovrebbe ripristinarsi completamente dopo ogni riavvio. L'[archiviazione persistente](https://tails.boum.org/doc/persistent_storage/index.en.html) è configurabile per memorizzare alcuni dati tra i riavvii.

## Distribuzioni incentrate sulla sicurezza

### Qubes OS

!!! recommendation

    ![Logo di Qubes OS](assets/img/qubes/qubes_os.svg){ align=right }
    
    **Qubes OS** è un sistema operativo open source progettato per fornire una forte sicurezza per l'informatica desktop. Si basa su Xen, il Sistema X Window, e su Linux, e può eseguire gran parte delle applicazioni di Linux, e utilizzare molti dei suoi driver.
    
    [:octicons-home-16: Home](https://www.qubes-os.org/){ .md-button .md-button--primary }
    [:material-arrow-right-drop-circle: Panoramica](os/qubes-overview.md){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Servizio Onion" }
    [:octicons-eye-16:](https://www.qubes-os.org/privacy/){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://www.qubes-os.org/doc/){ .card-link title=Documentazione }
    [:octicons-code-16:](https://github.com/QubesOS/){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://www.qubes-os.org/donate/){ .card-link title=Contribuisci }

Qubes OS è un sistema operativo basato su Xen, pensato per fornire una forte sicurezza per l'informatica desktop, tramite le macchine virtuali sicure (VM), anche note come *Qubes*.

Il sistema operativo Qubes OS protegge il computer isolando i sottosistemi (ad esempio, rete, USB, ecc.) e le applicazioni, in VM separate. Se una parte del sistema dovesse essere compromessa, l'isolamento aggiuntivo potrebbe proteggere il resto del sistema. Per ulteriori dettagli, consulta le [Domande Frequenti](https://www.qubes-os.org/faq/) di Qubes.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

!!! esempio "Questa sezione è nuova"

    Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

I nostri sistemi operativi consigliati:

- Devono essere open source.
- Devono ricevere regolarmente aggiornamenti del software e del kernel di Linux.
- Le distribuzioni Linux devono supportare [Wayland](os/linux-overview.md#wayland).
- Devono supportare la crittografia dell'intero disco durante l'installazione.
- Non devono interrompere i rilasci regolari per più di 1 anno. [Sconsigliamo](os/linux-overview.md#release-cycle) le versioni di distribuzioni con "Supporto a Lungo Termine" o "stabili", per l'utilizzo da desktop.
- Devono supportare un'ampia varietà di hardware.
