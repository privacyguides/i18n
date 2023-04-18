---
title: "Desktop/PC"
icon: simple/linux
description: Le distribuzioni Linux sono comunemente consigliate per la protezione della privacy e la libertà del software.
cover: desktop.png
---

Le distribuzioni Linux sono comunemente consigliate per la protezione della privacy e la libertà del software. Se non utilizzi già Linux, di seguito ti suggeriamo alcune distribuzioni da provare, oltre ad alcuni consigli generali per migliorare la privacy e la sicurezza applicabili a molte distribuzioni Linux.

- [Panoramica generale di Linux :material-arrow-right-drop-circle:](os/linux-overview.md)

## Distribuzioni tradizionali

### Fedora Workstation

!!! recommendation

    ![Fedora logo](/assets/img/linux-desktop/fedora-workstation.svg){ align=right }
    
    **Fedora Workstation** è la distribuzione che raccomandiamo per utenti nuovi a Linux. Fedora generalmente adotta tecnologie più recenti prima di altre distribuzioni, ad esempio [Wayland](https://wayland.freedesktop.org/), [PipeWire](https://pipewire.org), e presto, [FS-Verity](https://fedoraproject.org/wiki/Changes/FsVerityRPM). Queste nuove tecnologie spesso comportano miglioramenti alla sicurezza, privacy e usabilità in generale.
    
    [:octicons-home-16: Pagina principale](https://getfedora.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=Documentazione}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribuisci }

Fedora ha un ciclo di rilascio semi-rolling. Mentre alcuni pacchetti come [GNOME](https://www.gnome.org) sono congelati fino alla prossima versione di Fedora, la maggior parte dei pacchetti (incluso il kernel) sono aggiornati frequentemente durante il ciclo di vita della versione.  Ogni versione di Fedora è supportata per un anno, con una nuova versione rilasciata ogni 6 mesi.

### openSUSE Tumbleweed

!!! recommendation

    ![openSUSE Tumbleweed logo](/assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }
    
    **openSUSE Tumbleweed** è una distribuzione [a rilascio continuo](https://it.wikipedia.org/wiki/Rolling_release) stabile.
    
    openSUSE Tumbleweed ha un sistema di [aggiornamenti "transazionali"](https://kubic.opensuse.org/blog/2018-04-04-transactionalupdates/) che usa [Btrfs](https://it.wikipedia.org/wiki/Btrfs) e [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) per assicurare che le istantanee possano essere ripristinate in caso di problemi.
    
    [:octicons-home-16: Pagina principale](https://get.opensuse.org/tumbleweed/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://doc.opensuse.org/){ .card-link title=Documentazione}
    [:octicons-heart-16:](https://shop.opensuse.org/){ .card-link title=Contribuisci }

Tumbleweed segue un modello di rilascio continuo in cui ogni aggiornamento viene rilasciato come un'istantanea della distribuzione. Quando l'utente aggiorna il suo sistema, viene scaricata una nuova istantanea. Ogni istantanea viene sottoposta a una serie di test automatizzati da [openQA](https://openqa.opensuse.org) per garantirne la qualità.

### Arch Linux

!!! recommendation

    ![Arch logo](/assets/img/linux-desktop/archlinux.svg){ align=right }
    
    **Arch Linux** è una distribuzione leggera, fai-da-te (DIY) che significa che ottieni solo ciò che installi. Per maggiori informazioni visita le loro [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions).
    
    [:octicons-home-16: Pagina principale](https://archlinux.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://wiki.archlinux.org/){ .card-link title=Documentazione}
    [:octicons-heart-16:](https://archlinux.org/donate/){ .card-link title=Contribuisci }

Arch Linux ha un ciclo di rilascio continuo. Non c'è un programma di rilascio fisso e i pacchetti vengono aggiornati molto frequentemente.

Essendo una distribuzione DIY, ci si aspetta che l'utente [imposti e mantenga](#arch-based-distributions) il proprio sistema. Arch ha un [installatore ufficiale](https://wiki.archlinux.org/title/Archinstall) per rendere il processo di installazione un po' più facile.

Gran parte dei [pacchetti di Arch Linux](https://reproducible.archlinux.org) sono [riproducibili](https://reproducible-builds.org).

## Distribuzioni immutabili

### Fedora Silverblue

!!! recommendation

    ![Fedora Silverblue logo](/assets/img/linux-desktop/fedora-silverblue.svg){ align=right }
    
    **Fedora Silverblue** e **Fedora Kinoite** sono varianti immutabili di Fedora con una forte attenzione al flussi di lavoro basato su contenitori. Silverblue viene fornito con l'ambiente desktop [GNOME](https://www.gnome.org/) mentre Kinoite viene fornito con [KDE](https://kde.org/). Silverblue e Kinoite seguono lo stesso programma di rilascio di Fedora Workstation, beneficiando degli stessi aggiornamenti veloci e rimanendo molto vicini all'upstream.
    
    [Visita silverblue.fedoraproject.org](https://silverblue.fedoraproject.org/){ .md-button .md-button--primary }

Silverblue (e Kinoite) differiscono da Fedora Workstation perché sostituiscono il gestore di pacchetti [DNF](https://fedoraproject.org/wiki/DNF) con un'alternativa molto più avanzata chiamata [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/rawhide/system-administrators-guide/package-management/rpm-ostree/).  Il gestore di pacchetti `rpm-ostree` funziona scaricando un'immagine di base per il sistema, quindi sovrapponendo i pacchetti in un albero di commit simile a [git](https://en.wikipedia.org/wiki/Git). Quando il sistema viene aggiornato, viene scaricata una nuova immagine di base e le sovrapposizioni vengono applicate a questa nuova immagine.

Al termine dell'aggiornamento, il sistema verrà riavviato nella nuova distribuzione. `rpm-ostree` mantiene due distribuzioni del sistema in modo da poter effettuare facilmente il rollback se qualcosa si rompe nella nuova distribuzione. È inoltre possibile aggiungere altre distribuzioni in base alle necessità.

[Flatpak](https://www.flatpak.org) è il metodo principale di installazione dei pacchetti su queste distribuzioni, in quanto `rpm-ostree` è pensato solo per sovrapporre all'immagine di base i pacchetti che non possono stare all'interno di un contenitore.

Come alternativa a Flatpaks, c'è l'opzione di [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox/) per creare contenitori [Podman](https://podman.io) con una cartella home condivisa con il sistema operativo host e imitare un ambiente Fedora tradizionale, che è una [caratteristica utile](https://containertoolbx.org) per lo sviluppatore esigente.

### NixOS

!!! recommendation

    ![NixOS logo](assets/img/linux-desktop/nixos.svg){ align=right }
    
    NixOS è una distribuzione indipendente basata sul gestore di pacchetti Nix con una particolare attenzione alla riproducibilità e all'affidabilità.
    
    [:octicons-home-16: Pagina principale](https://nixos.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=Documentazione}
    [:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=Contribuisci }

Il gestore di pacchetti di NixOS conserva ogni versione di ogni pacchetto in una cartella diversa del **negozio Nix**. Per questo motivo è possibile avere diverse versioni dello stesso pacchetto installate sul sistema. Dopo che il contenuto del pacchetto è stato scritto nella cartella, questa viene resa di sola lettura.

NixOS fornisce anche aggiornamenti atomici; prima scarica (o costruisce) i pacchetti e i file per la nuova generazione di sistema e poi passa ad essi. Ci sono diversi modi per passare a una nuova generazione: si può dire a NixOS di attivarla dopo il riavvio o si può passare ad essa in fase di esecuzione. È anche possibile *testare* la nuova generazione passando ad essa in fase di esecuzione, ma senza impostarla come generazione corrente del sistema. Se qualcosa nel processo di aggiornamento si interrompe, è possibile riavviare automaticamente e tornare a una versione funzionante del sistema.

Nix, il gestore di pacchetti, utilizza un linguaggio puramente funzionale, chiamato anch'esso Nix, per definire i pacchetti.

[Nixpkgs](https://github.com/nixos/nixpkgs) (la fonte principale dei pacchetti) è contenuto in un unico repository GitHub. È anche possibile definire i propri pacchetti nella stesso linguaggio e quindi includerli facilmente nella configurazione.

Nix è un gestore di pacchetti basato sul codice sorgente; se non c'è nessun pacchetto precostruito disponibile nella cache binaria, Nix genererà il pacchetto da zero usando la sua definizione. Costruisce ogni pacchetto in un ambiente sandbox *puro* , che è il più indipendente possibile dal sistema ospite, rendendo così i binari riproducibili.

## Distribuzioni incentrate sull'anonimato

### Whonix

!!! recommendation

    ![Logo Whonix](assets/img/linux-desktop/whonix.svg){ align=right }
    
    **Whonix** è basato su [Kicksecure](https://www.whonix.org/wiki/Kicksecure), un fork di Debian focalizzato sulla sicurezza. Mira a fornire privacy, sicurezza e anonimato su internet. Whonix è meglio utilizzato insieme a [Qubes OS](#qubes-os).
    
    [:octicons-home-16: Pagina principale](https://www.whonix.org/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://www.dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Servizio onion" }
    [:octicons-info-16:](https://www.whonix.org/wiki/Documentation){ .card-link title=Documentazione}
    [:octicons-heart-16:](https://www.whonix.org/wiki/Donate){ .card-link title=Contribuisci }

Whonix è pensato per essere eseguito come due macchine virtuali: una "Workstation" e un "Gateway" Tor. Tutte le comunicazioni dalla Workstation devono passare attraverso il gateway Tor, e saranno instradate attraverso la rete Tor. Ciò significa che anche se la Workstation venisse compromessa da un malware di qualche tipo, il vero indirizzo IP rimarrebbe nascosto.

Alcune delle sue caratteristiche includono Tor Stream Isolation, [keystroke anonymization](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak), [swap crittografato](https://github.com/Whonix/swap-file-creator), e un allocatore di memoria rinforzato.

Le versioni future di Whonix probabilmente includeranno [criteri AppArmor di sistema completi](https://github.com/Whonix/apparmor-profile-everything) e un [lanciatore di app sandbox](https://www.whonix.org/wiki/Sandbox-app-launcher) per confinare completamente tutti i processi sul sistema.

Whonix è utilizzato al meglio [in combinazione con Qubes](https://www.whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers).

### Tails

!!! recommendation

    ![Tails logo](assets/img/linux-desktop/tails.svg){ align=right }
    
    **Tails** è un sistema operativo live basato su Debian che instrada tutte le comunicazioni attraverso Tor, che può essere avviato su quasi tutti i computer da un'installazione su DVD, chiavetta USB o scheda SD. Utilizza [Tor](tor.md) per preservare la privacy e l'anonimato aggirando la censura e non lascia traccia di sé sul computer su cui viene utilizzato una volta spento.
    
    [:octicons-home-16: Pagina principale](https://tails.boum.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://tails.boum.org/doc/index.en.html){ .card-link title=Documentazione}
    [:octicons-heart-16:](https://tails.boum.org/donate/){ .card-link title=Contribuisci }

Tails è ottimo per la contro-analisi forense grazie all'amnesia (il che significa che non viene scritto nulla sul disco); tuttavia, non è una distribuzione rafforzata come Whonix. Manca di molte funzioni di anonimato e sicurezza che Whonix possiede e viene aggiornato molto meno spesso (solo una volta ogni sei settimane). Un sistema Tails compromesso da malware può potenzialmente aggirare il proxy trasparente, consentendo all'utente di essere deanonimizzato.

Tails include [uBlock Origin](desktop-browsers.md#ublock-origin) nel Tor Browser per impostazione predefinita, il che può potenzialmente rendere più facile per gli avversari effettuare il fingerprinting degli utenti di Tails. [Le macchine virtuali Whonix](desktop.md#whonix) possono essere più a prova di perdite, ma non sono amnesiche, il che significa che i dati possono essere recuperati dal dispositivo di archiviazione.

Da progettazione, Tails è previsto che si ripristini completamente dopo ogni riavvio. L'archiviazione [cifrata persistente](https://tails.boum.org/doc/first_steps/persistence/index.en.html) può essere configurata per memorizzare alcuni dati tra un ravvio e l'altro.

## Distribuzioni incentrate sulla sicurezza

### Qubes OS

!!! recommendation

    ![Qubes OS logo](assets/img/qubes/qubes_os.svg){ align=right }
    
    **Qubes OS** è un sistema operativo open-source progettato per fornire una forte sicurezza per i computer desktop. È basato su Xen, sul sistema X Window e su Linux, e può eseguire/utilizzare la maggior parte delle applicazioni/driver di Linux.
    
    [:octicons-home-16: Pagina principale](https://www.qubes-os.org/){ .md-button .md-button--primary }
    [:material-arrow-right-drop-circle: Panoramica](os/qubes-overview.md){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Servizio Onion" }
    [:octicons-eye-16:](https://www.qubes-os.org/privacy/){ .card-link title="Informativa sulla privacy" }
    [:octicons-info-16:](https://www.qubes-os.org/doc/){ .card-link title=Documentazione }
    [:octicons-code-16:](https://github.com/QubesOS/){ .card-link title="Codice sorgente" }
    [:octicons-heart-16:](https://www.qubes-os.org/donate/){ .card-link title=Contribuisci }

Qubes OS è un sistema operativo basato su Xen che mira a fornire una forte sicurezza per il desktop computing attraverso macchine virtuali (VM) sicure, note anche come *Qubes*.

Il sistema operativo Qubes OS protegge il computer isolando i sottosistemi (ad esempio, rete, USB, ecc.) e le applicazioni in macchine virtuali separate. Se una parte del sistema viene compromessa, è probabile che l'isolamento supplementare protegga il resto del sistema. Per ulteriori dettagli, consulta le [FAQ](https://www.qubes-os.org/faq/) di Qubes.

## Criteri

**Si noti che non siamo affiliati a nessuno dei progetti che raccomandiamo.** Oltre ai [ nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie di requisiti chiari che ci consentono di fornire raccomandazioni obiettive. Ti consigliamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le vostre ricerche per assicurarvi che sia la scelta giusta per voi.

!!! esempio "Questa sezione è nuova"

    Stiamo lavorando per stabilire criteri ben definiti per ogni sezione del nostro sito, e questo potrebbe essere soggetto a modifiche. Se avete domande sui nostri criteri, vi preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e non date per scontato che non abbiamo preso in considerazione qualcosa nel formulare le nostre raccomandazioni se non è elencato qui. Sono molti i fattori presi in considerazione e discussi quando consigliamo un progetto, e stiamo lavorando per documentare ogni singolo fattore.

I nostri sistemi operativi consigliati:

- Devono essere open-source.
- Devono ricevere regolarmente aggiornamenti del software e del kernel Linux.
- Le distribuzioni Linux devono supportare [Wayland](os/linux-overview.md#Wayland).
- Devono supportare la crittografia dell'intero disco durante l'installazione.
- Non devono fermare i rilasci regolari per più di 1 anno. Noi [non consigliamo](os/linux-overview.md#release-cycle) le distribuzioni "Long Term Support" o "stable" per utilizzo desktop.
- Devono supportare un'ampia varietà di hardware.
