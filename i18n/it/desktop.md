---
title: "Desktop/PC"
icon: simple/linux
description: Le distribuzioni di Linux sono comunemente consigliate per la protezione della privacy e la libertà dei software.
cover: desktop.webp
---

Le distribuzioni di Linux sono comunemente consigliate per la protezione della privacy e la libertà dei software. Se non utilizzi già Linux, seguono alcune distribuzioni che suggeriamo di provare, nonché consigli generali sul miglioramento della privacy e della sicurezza, applicabili a molte distribuzioni di Linux.

- [Panoramica generale di Linux :material-arrow-right-drop-circle:](os/linux-overview.md)

## Distribuzioni tradizionali

### Fedora Workstation

<div class="admonition recommendation" markdown>

![Logo Fedora](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Workstation** è la nostra distribuzione consigliata per chi si avvicina per la prima volta a Linux. Generalmente, Fedora, adotta le tecnologie più recenti prima delle altre distribuzioni, ad esempio, [Wayland](https://wayland.freedesktop.org/) e [PipeWire](https://pipewire.org). Queste, spesso, comportano miglioramenti alla sicurezza, privacy e utilizzabilità, in generale.

[:octicons-home-16: Home](https://fedoraproject.org/workstation/){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=Documentazione}
[:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribuisci }

</details>

</div>

Fedora ha un ciclo di rilascio semi continuo. Mentre alcuni pacchetti come [GNOME](https://www.gnome.org) sono ibernati fino alla versione successiva di Fedora, gran parte di essi (incluso il kernel) sono aggiornati frequentemente durante il ciclo di vita della versione. Ogni versione di Fedora è supportata per un anno, con una nuova versione rilasciata ogni 6 mesi.

### openSUSE Tumbleweed

<div class="admonition recommendation" markdown>

![Logo di openSUSE Tumbleweed](/assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }

**openSUSE Tumbleweed** è una distribuzione stabile a rilascio continuo.

openSUSE Tumbleweed dispone di un sistema di [aggiornamenti "transazionali"](https://kubic.opensuse.org/blog/2018-04-04-transactionalupdates/) che utilizza [Btrfs](https://it.wikipedia.org/wiki/Btrfs) e [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) per garantire che le istantanee possano essere ripristinate in caso di problemi.

[:octicons-home-16: Home](https://get.opensuse.org/tumbleweed/){ .md-button .md-button--primary }
[:octicons-info-16:](https://doc.opensuse.org/){ .card-link title=Documentazione}
[:octicons-heart-16:](https://shop.opensuse.org/){ .card-link title=Contribuisci }

</details>

</div>

Tumbleweed segue un modello di rilascio continuo in cui ogni aggiornamento è rilasciato come un'istantanea della distribuzione. Quando l'utente aggiorna il proprio sistema, viene scaricata una nuova istantanea. Ogni istantanea viene sottoposta a una serie di test automatizzati da [openQA](https://openqa.opensuse.org) per garantirne la qualità.

### Arch Linux

<div class="admonition recommendation" markdown>

![Logo di Arch](/assets/img/linux-desktop/archlinux.svg){ align=right }

**Arch Linux** è una distribuzione leggera e fai-da-te, il che significa che ottieni soltanto ciò che installi. Per ulteriori informazioni visita le loro [Domande Frequenti](https://wiki.archlinux.org/title/Frequently_asked_questions).

[:octicons-home-16: Home](https://archlinux.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.archlinux.org/){ .card-link title=Documentazione}
[:octicons-heart-16:](https://archlinux.org/donate/){ .card-link title=Contribuisci }

</details>

</div>

Arch Linux ha un ciclo di rilascio continuo. Non esiste un piano di rilascio fisso e i pacchetti sono aggiornati molto frequentemente.

Essendo una distribuzione fai da te, [dovresti configurare e mantenere](#arch-based-distributions) il tuo sistema per conto tuo. Arch dispone di un [installatore ufficiale](https://wiki.archlinux.org/title/Archinstall) per semplificare il processo di installazione.

Gran parte dei [pacchetti di Arch Linux](https://reproducible.archlinux.org) sono [riproducibili](https://reproducible-builds.org).

## Distribuzioni atomiche

**Le distribuzioni atomiche** (talvolta indicate anche come **distribuzioni immutabili**) sono sistemi operativi che gestiscono l'installazione e gli aggiornamenti dei pacchetti stratificando le modifiche sull'immagine del sistema centrale, piuttosto che modificando direttamente il sistema. Questo comporta dei vantaggi, tra cui una maggiore stabilità e la possibilità di eseguire facilmente il rollback degli aggiornamenti. Per ulteriori informazioni, dai uno sguardo a [*Aggiornamenti tradizionali vs. Atomici*](os/linux-overview.md#traditional-vs-atomic-updates).

### Fedora Atomic Desktops

<div class="admonition recommendation" markdown>

![Logo Fedora](assets/img/linux-desktop/fedora.svg){ align=right }

I **Fedora Atomic Desktops** sono varianti di Fedora che utilizzano il gestore di pacchetti `rpm-ostree` e sono fortemente incentrati sui flussi di lavoro containerizzati e su Flatpak per le applicazioni desktop. Tutte queste varianti seguono lo stesso programma di rilascio di Fedora Workstation, beneficiando degli stessi aggiornamenti veloci e restando molto vicine alla versione a monte.

[:octicons-home-16: Homepage](https://fedoraproject.org/atomic-desktops/){ .md-button .md-button--primary }
[:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribuisci }

</details>

</div>

I [Fedora Atomic Desktops](https://fedoramagazine.org/introducing-fedora-atomic-desktops/) sono disponibili in diverse versioni a seconda dell'ambiente desktop preferito, come **Fedora Silverblue** (che viene fornito con [GNOME](https://www.gnome.org/)), **Fedora Kinoite**, (che viene fornito con [KDE](https://kde.org/)), **Fedora Sway Atomic**, o **Fedora Budgie Atomic**. Tuttavia, non consigliamo quest'ultimo come ambiente desktop Budgie [richiede ancora X11](https://buddiesofbudgie.org/blog/wayland).

Questi sistemi operativi differiscono da Fedora Workstation perché sostituiscono il gestore di pacchetti [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf/) con un'alternativa molto più avanzata chiamata [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/package-management/rpm-ostree/). Il gestore dei pacchetti `rpm-ostree` funziona scaricando un'immagine di base per il sistema, poi sovrapponendo i pacchetti su di esso in un [git](https://en.wikipedia.org/wiki/Git)-come albero di commit. Quando il sistema viene aggiornato, viene scaricata una nuova immagine di base e le sovrapposizioni sono applicate a questa nuova immagine.

Al termine dell'aggiornamento, il sistema sarà riavviato nella nuova versione. `rpm-ostree` mantiene due versioni del sistema, così da poter facilmente essere ripristinato, se qualcosa si rompe nella nuova distribuzione. È inoltre possibile aggiungere più versioni in base alle necessità.

[Flatpak](https://www.flatpak.org) è il metodo principale di installazione dei pacchetti su queste distribuzioni, in quanto `rpm-ostree` è pensato solo per sovrapporre all'immagine di base i pacchetti che non possono stare all'interno di un contenitore.

Come alternativa ai Flatpaks, esiste l'opzione di [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox/) per creare contenitori [Podman](https://podman.io) con una cartella home condivisa con il sistema operativo dell'host che imita un ambiente tradizionale di Fedora, un [caratteristica utile](https://containertoolbx.org) per gli sviluppatori esigenti.

### NixOS

<div class="admonition recommendation" markdown>

![Logo di NixOS](assets/img/linux-desktop/nixos.svg){ align=right }

NixOS è una distribuzione indipendente basata sul gestore di pacchetti Nix, incentrata sulla riproducibilità e l'affidabilità.

[:octicons-home-16: Home](https://nixos.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=Documentazione}
[:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=Contribuisci }

</details>

</div>

Il gestore di pacchetti di NixOS conserva ogni versione di ogni pacchetto in una cartella diversa del **Nix Store**. A causa di ciò puoi avere versioni differenti dello stesso pacchetto installate sul tuo sistema. Dopo che il contenuto del pacchetto è stato scritto nella cartella, questa viene resa di sola lettura.

NixOS also provides atomic updates; first it downloads (or builds) the packages and files for the new system generation and then switches to it. Esistono svariati modi per passare a una nuova generazione; puoi chiedere a NixOS di attivarla dopo il riavvio, o passarci mentre è in esecuzione. Puoi anche *testare* la nuova generazione passandovi durante l'esecuzione, ma non impostarla come quella corrente di sistema. Se qualcosa nel processo d'aggiornamento si corrompe, basta riavviare e tornare automaticamente a una versione funzionante del sistema.

Nix, il gestore di pacchetti, utilizza un linguaggio puramente funzionale, anch'esso detto Nix, per definire i pacchetti.

[Nixpkgs](https://github.com/nixos/nixpkgs) (la fonte principale dei pacchetti) è contenuto in un unico repository di GitHub. Inoltre, puoi definire i tuoi pacchetti nello stesso linguaggio, quindi, includerli facilmente nella tua configurazione.

Nix is a source-based package manager; if there’s no pre-built available in the binary cache, Nix will just build the package from source using its definition. Builda ogni pacchetto in un ambiente sandbox *puro*, il più indipendente possibile dal sistema di host, rendendo riproducibili i binari.

## Distribuzioni incentrate sull'anonimato

### Whonix

<div class="admonition recommendation" markdown>

![Logo di Whonix](assets/img/linux-desktop/whonix.svg){ align=right }

**Whonix** si basa su [Kicksecure](#kicksecure), una biforcazione incentrata sulla sicurezza di Debian. Mira a fornire privacy, sicurezza e anonimato su Internet. Whonix è meglio utilizzato insieme a [Qubes OS](#qubes-os).

[:octicons-home-16: Home](https://www.whonix.org/){ .md-button .md-button--primary }
[:simple-torbrowser:](http://www.dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Servizio Onion" }
[:octicons-info-16:](https://www.whonix.org/wiki/Documentation){ .card-link title=Documentazione}
[:octicons-heart-16:](https://www.whonix.org/wiki/Donate){ .card-link title=Contribuisci }

</details>

</div>

Whonix è pensato per operare come due macchine virtuali: una "Workstation" e un "Gateway" di Tor Tutte le comunicazioni dalla Workstation devono passare per il gateway di Tor. Ciò significa che, anche se la Workstation fosse compromessa da un malware di qualche tipo, il vero indirizzo IP rimarrebbe nascosto.

Alcune delle sue caratteristiche includono Tor Stream Isolation, [keystroke anonymization](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak), [swap crittografato](https://github.com/Whonix/swap-file-creator)e un allocatore di memoria protetto. Le versioni future di Whonix includeranno probabilmente le [politiche di sistema complete di AppArmor](https://github.com/Whonix/apparmor-profile-everything) e un [launcher di app sandbox](https://www.whonix.org/wiki/Sandbox-app-launcher), per confinare interamente tutti i processi sul sistema.

Whonix è utilizzato al meglio [in combinazione con Qubes](https://www.whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers). Abbiamo una [guida di consigli](os/qubes-overview.md#connecting-to-tor-via-a-vpn) sulla configurazione di Whonix in combinazione con un ProxyVM della VPN su Qubes, per nascondere le tue attività di Tor dal tuo ISP.

### Tails

<div class="admonition recommendation" markdown>

![Logo di Tails](assets/img/linux-desktop/tails.svg){ align=right }

**Tails** è un sistema operativo live basato su Debian che instrada tutte le comunicazioni attraverso Tor, che può essere avviato su quasi tutti i computer da un'installazione su DVD, chiavetta USB o scheda SD. Utilizza [Tor](tor.md) per preservare la privacy e l'anonimato, aggirando la censura e non lasciando traccia di sé sul computer utilizzato, una volta spento.

[:octicons-home-16: Home](https://tails.boum.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://tails.boum.org/doc/index.en.html){ .card-link title=Documentazione}
[:octicons-heart-16:](https://tails.boum.org/donate/){ .card-link title=Contribuisci }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Tails [non cancella](https://gitlab.tails.boum.org/tails/tails/-/issues/5356) la [memoria video](https://en.wikipedia.org/wiki/Dual-ported_video_RAM) allo spegnimento. Quando si riavvia il computer dopo aver utilizzato Tails, è possibile che venga visualizzata brevemente l'ultima schermata visualizzata in Tails. Se si spegne il computer invece di riavviarlo, la memoria video si cancella automaticamente dopo essere rimasta per qualche tempo senza alimentazione.

</div>

Tails is great for counter forensics due to amnesia (meaning nothing is written to the disk); however, it is not a hardened distribution like Whonix. It lacks many anonymity and security features that Whonix has and gets updated much less often (only once every six weeks). A Tails system that is compromised by malware may potentially bypass the transparent proxy allowing for the user to be deanonymized.

Tails includes [uBlock Origin](desktop-browsers.md#ublock-origin) in Tor Browser by default, which may potentially make it easier for adversaries to fingerprint Tails users. [Whonix](desktop.md#whonix) virtual machines may be more leak-proof, however they are not amnesic, meaning data may be recovered from your storage device.

By design, Tails is meant to completely reset itself after each reboot. Encrypted [persistent storage](https://tails.boum.org/doc/persistent_storage/index.en.html) can be configured to store some data between reboots.

## Distribuzioni incentrate sulla sicurezza

### Qubes OS

<div class="admonition recommendation" markdown>

![Logo di Qubes OS](assets/img/qubes/qubes_os.svg){ align=right }

**Qubes OS** è un sistema operativo open-source progettato per fornire una forte sicurezza per i computer desktop attraverso macchine virtuali sicure (o "qube"). Qubes si basa su Xen, X Window System e Linux. Può eseguire la maggior parte delle applicazioni Linux e utilizzare la maggior parte dei driver Linux.

[:octicons-home-16: Home](https://www.qubes-os.org/){ .md-button .md-button--primary }
[:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Servizio Onion" }
[:octicons-eye-16:](https://www.qubes-os.org/privacy/){ .card-link title="Codice Sorgente" }
[:octicons-info-16:](https://www.qubes-os.org/doc/){ .card-link title=Documentazione }
[:octicons-code-16:](https://github.com/QubesOS/){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://www.qubes-os.org/donate/){ .card-link title=Contribuisci }

</details>

</div>

Qubes OS secures the computer by isolating subsystems (e.g., networking, USB, etc.) and applications in separate *qubes*. Should one part of the system be compromised, the extra isolation is likely to protect the rest of the *qubes* and the core system.

For further information about how Qubes works, read our full [Qubes OS overview](os/qubes-overview.md) page.

### Kicksecure

While we [recommend against](os/linux-overview.md#release-cycle) "perpetually outdated" distributions like Debian for Desktop use in most cases, Kicksecure is a Debian-based operating system which has been hardened to be much more than a typical Linux install.

<div class="admonition recommendation" markdown>

![Logo di Kicksecure](assets/img/linux-desktop/kicksecure.svg){ align=right }

**Kicksecure**, in breve, consiste in una serie di script, configurazioni e pacchetti che riducono sostanzialmente la superficie di attacco di Debian. Copre di default molti dei consigli sulla privacy e la sicurezza. Inoltre, serve da OS di base per [Whonix](#whonix).

[:octicons-home-16: Home](https://www.kicksecure.com/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.kicksecure.com/wiki/Privacy_Policy){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://www.kicksecure.com/wiki/Documentation){ .card-link title=Documentazione }
[:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://www.kicksecure.com/wiki/Donate){ .card-link title=Contribuisci }

</details>

</div>

## Criteri

La scelta di una distro Linux adatta a te dipende da una grande varietà di preferenze personali e questa pagina **non** vuole essere un elenco esaustivo di tutte le distribuzioni possibili. La nostra pagina di panoramica su Linux contiene alcuni consigli sulla [scelta di una distro](os/linux-overview.md#choosing-your-distribution) in modo più dettagliato. Le distro presenti su *questa* pagina seguono tutte, in generale, le linee guida che abbiamo illustrato in quella pagina e soddisfano tutte questi standard:

- Gratuito e open source.
- Ricevono aggiornamenti regolari del software e del kernel.
- [Evitano X11](os/linux-overview.md#wayland).
    - L'eccezione notevole, qui, è Qubes, ma i problemi di isolamento tipici di X11, sono evitati dalla virtualizzazione. Questo isolamento si applica esclusivamente alle app *eseguite in qube differenti* (macchine virtuali), le app eseguite nella *stessa* qube non sono protette tra loro.
- Supportano la crittografia del disco completo durante l'installazione.
- Non interrompono le versioni regolari per più di 1 anno.
    - [Sconsigliamo](os/linux-overview.md#release-cycle) le versioni di distribuzioni con "Supporto a Lungo Termine" o "stabile", per l'utilizzo da desktop.
- Supportano una vasta gamma di hardware.
- Preferiscono i progetti più grandi.
    - Mantenere un sistema operativo è un sfida importante e, i progetti più piccoli, tendono a compiere errori evitabili o a ritardare gli aggiornamenti critici (o peggio, scomparire interamente). Ci orientiamo verso progetti che, tra 10 anni, potrebbero essere ancora presenti (che sia grazie a supporto aziendale o supporto della community molto significativo), e ci allontaniamo da progetti costruiti a mano o aventi un numero ridotto di manutentori.

Inoltre, [i nostri criteri standard](about/criteria.md) per i progetti raccomandati sono ancora validi. **Si prega di notare che non siamo affiliati a nessuno dei progetti che raccomandiamo.**
