---
title: "Desktop/PC"
icon: simple/linux
description: Le distribuzioni di Linux sono comunemente consigliate per la protezione della privacy e la libertà dei software.
cover: desktop.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Capitalismo di sorveglianza](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Le distribuzioni di Linux sono comunemente consigliate per la protezione della privacy e la libertà dei software. Se non utilizzi già Linux, seguono alcune distribuzioni che suggeriamo di provare, nonché consigli generali sul miglioramento della privacy e della sicurezza, applicabili a molte distribuzioni di Linux.

- [Panoramica generale di Linux :material-arrow-right-drop-circle:](os/linux-overview.md)

## Distribuzioni tradizionali

### Fedora Workstation

<div class="admonition recommendation" markdown>

![Logo Fedora](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Workstation** è la nostra distribuzione consigliata per chi si avvicina per la prima volta a Linux. Fedora generally adopts newer technologies (e.g., [Wayland](https://wayland.freedesktop.org) and [PipeWire](https://pipewire.org)) before other distributions. Queste, spesso, comportano miglioramenti alla sicurezza, privacy e utilizzabilità, in generale.

[:octicons-home-16: Homepage](https://fedoraproject.org/workstation){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs){ .card-link title=Documentation}
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title=Contribute }

</details>

</div>

Fedora ha un ciclo di rilascio semi continuo. While some packages like [GNOME](https://gnome.org) are frozen until the next Fedora release, most packages (including the kernel) are updated frequently throughout the lifespan of the release. Ogni versione di Fedora è supportata per un anno, con una nuova versione rilasciata ogni 6 mesi.

### openSUSE Tumbleweed

<div class="admonition recommendation" markdown>

![Logo di openSUSE Tumbleweed](/assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }

**openSUSE Tumbleweed** è una distribuzione stabile a rilascio continuo.

openSUSE Tumbleweed uses [Btrfs](https://en.wikipedia.org/wiki/Btrfs) and [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) to ensure that snapshots can be rolled back should there be a problem.

[:octicons-home-16: Homepage](https://get.opensuse.org/tumbleweed){ .md-button .md-button--primary }
[:octicons-info-16:](https://doc.opensuse.org){ .card-link title=Documentation}
[:octicons-heart-16:](https://shop.opensuse.org){ .card-link title=Contribute }

</details>

</div>

Tumbleweed segue un modello di rilascio continuo in cui ogni aggiornamento è rilasciato come un'istantanea della distribuzione. Quando l'utente aggiorna il proprio sistema, viene scaricata una nuova istantanea. Ogni istantanea viene sottoposta a una serie di test automatizzati da [openQA](https://openqa.opensuse.org) per garantirne la qualità.

### Arch Linux

<div class="admonition recommendation" markdown>

![Arch logo](assets/img/linux-desktop/archlinux.svg){ align=right }

**Arch Linux** is a lightweight, do-it-yourself (DIY) distribution, meaning that you only get what you install. Per ulteriori informazioni visita le loro [Domande Frequenti](https://wiki.archlinux.org/title/Frequently_asked_questions).

[:octicons-home-16: Homepage](https://archlinux.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.archlinux.org){ .card-link title=Documentation}
[:octicons-heart-16:](https://archlinux.org/donate){ .card-link title=Contribute }

</details>

</div>

Arch Linux ha un ciclo di rilascio continuo. Non esiste un piano di rilascio fisso e i pacchetti sono aggiornati molto frequentemente.

Essendo una distribuzione fai da te, [dovresti configurare e mantenere](#arch-based-distributions) il tuo sistema per conto tuo. Arch dispone di un [installatore ufficiale](https://wiki.archlinux.org/title/Archinstall) per semplificare il processo di installazione.

A large portion of [Arch Linux’s packages](https://reproducible.archlinux.org) are [reproducible](https://reproducible-builds.org)[^1].

## Distribuzioni atomiche

**Le distribuzioni atomiche** (talvolta indicate anche come **distribuzioni immutabili**) sono sistemi operativi che gestiscono l'installazione e gli aggiornamenti dei pacchetti stratificando le modifiche sull'immagine del sistema centrale, piuttosto che modificando direttamente il sistema. Advantages of atomic distros include increased stability and the ability to easily roll back updates. Per ulteriori informazioni, dai uno sguardo a [*Aggiornamenti tradizionali vs. Atomici*](os/linux-overview.md#traditional-vs-atomic-updates).

### Fedora Atomic Desktops

<div class="admonition recommendation" markdown>

![Logo Fedora](assets/img/linux-desktop/fedora.svg){ align=right }

I **Fedora Atomic Desktops** sono varianti di Fedora che utilizzano il gestore di pacchetti `rpm-ostree` e sono fortemente incentrati sui flussi di lavoro containerizzati e su Flatpak per le applicazioni desktop. Tutte queste varianti seguono lo stesso programma di rilascio di Fedora Workstation, beneficiando degli stessi aggiornamenti veloci e restando molto vicine alla versione a monte.

[:octicons-home-16: Homepage](https://fedoraproject.org/atomic-desktops){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/emerging){ .card-link title=Documentation}
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title=Contribute }

</details>

</div>

[Fedora Atomic Desktops](https://fedoramagazine.org/introducing-fedora-atomic-desktops) come in a variety of flavors depending on the desktop environment you prefer. As with the recommendation to avoid X11 in our [criteria](#criteria) for Linux distributions, we recommend avoiding flavors that support only the legacy X11 window system.

These operating systems differ from Fedora Workstation as they replace the [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf) package manager with a much more advanced alternative called [`rpm-ostree`](https://coreos.github.io/rpm-ostree). Il gestore dei pacchetti `rpm-ostree` funziona scaricando un'immagine di base per il sistema, poi sovrapponendo i pacchetti su di esso in un [git](https://en.wikipedia.org/wiki/Git)-come albero di commit. Quando il sistema viene aggiornato, viene scaricata una nuova immagine di base e le sovrapposizioni sono applicate a questa nuova immagine.

After the update is complete, you will reboot the system into the new deployment. `rpm-ostree` keeps two deployments of the system so that you can easily roll back if something breaks in the new deployment. È inoltre possibile aggiungere più versioni in base alle necessità.

[Flatpak](https://flatpak.org) is the primary package installation method on these distributions, as `rpm-ostree` is only meant to overlay packages that cannot stay inside of a container on top of the base image.

As an alternative to Flatpaks, there is the option of [Toolbx](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox) to create [Podman](https://podman.io) containers which mimic a traditional Fedora environment, a [useful feature](https://containertoolbx.org) for the discerning developer. These containers share a home directory with the host operating system.

### NixOS

<div class="admonition recommendation" markdown>

![Logo di NixOS](assets/img/linux-desktop/nixos.svg){ align=right }

NixOS è una distribuzione indipendente basata sul gestore di pacchetti Nix, incentrata sulla riproducibilità e l'affidabilità.

[:octicons-home-16: Homepage](https://nixos.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=Documentation}
[:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=Contribute }

</details>

</div>

Il gestore di pacchetti di NixOS conserva ogni versione di ogni pacchetto in una cartella diversa del **Nix Store**. A causa di ciò puoi avere versioni differenti dello stesso pacchetto installate sul tuo sistema. Dopo che il contenuto del pacchetto è stato scritto nella cartella, questa viene resa di sola lettura.

NixOS also provides atomic updates. It first downloads (or builds) the packages and files for the new system generation and then switches to it. There are different ways to switch to a new generation: you can tell NixOS to activate it after reboot or you can switch to it at runtime. Puoi anche *testare* la nuova generazione passandovi durante l'esecuzione, ma non impostarla come quella corrente di sistema. Se qualcosa nel processo d'aggiornamento si corrompe, basta riavviare e tornare automaticamente a una versione funzionante del sistema.

The Nix package manager uses a purely functional language—which is also called Nix—to define packages.

[Nixpkgs](https://github.com/nixos/nixpkgs) (la fonte principale dei pacchetti) è contenuto in un unico repository di GitHub. Inoltre, puoi definire i tuoi pacchetti nello stesso linguaggio, quindi, includerli facilmente nella tua configurazione.

Nix è un gestore di pacchetti basato sul codice sorgente; se non ne esiste alcuna binary-cache pre-buildata, Nix creerà semplicemente il pacchetto dal sorgente, utilizzando le istruzioni di build. It builds each package in a sandboxed *pure* environment, which is as independent of the host system as possible. Binaries built with this method are reproducible[^1].

## Distribuzioni incentrate sull'anonimato

### Whonix

<div class="admonition recommendation" markdown>

![Logo di Whonix](assets/img/linux-desktop/whonix.svg){ align=right }

**Whonix** si basa su [Kicksecure](#kicksecure), una biforcazione incentrata sulla sicurezza di Debian. It aims to provide privacy, security, and [:material-incognito: Anonymity](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } on the internet. Whonix è meglio utilizzato insieme a [Qubes OS](#qubes-os).

[:octicons-home-16: Homepage](https://whonix.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://whonix.org/wiki/Documentation){ .card-link title=Documentation}
[:octicons-heart-16:](https://whonix.org/wiki/Donate){ .card-link title=Contribute }

</details>

</div>

Whonix è pensato per operare come due macchine virtuali: una "Workstation" e un "Gateway" di Tor Tutte le comunicazioni dalla Workstation devono passare per il gateway di Tor. Ciò significa che, anche se la Workstation fosse compromessa da un malware di qualche tipo, il vero indirizzo IP rimarrebbe nascosto.

Some of its features include Tor Stream Isolation, [keystroke anonymization](https://whonix.org/wiki/Keystroke_Deanonymization#Kloak), [encrypted swap](https://github.com/Whonix/swap-file-creator), and a hardened memory allocator. Future versions of Whonix will likely include [full system AppArmor policies](https://github.com/roddhjav/apparmor.d) and a [sandboxed app launcher](https://whonix.org/wiki/Sandbox-app-launcher) to fully confine all processes on the system.

Whonix is best used [in conjunction with Qubes](https://whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers). Abbiamo una [guida di consigli](os/qubes-overview.md#connecting-to-tor-via-a-vpn) sulla configurazione di Whonix in combinazione con un ProxyVM della VPN su Qubes, per nascondere le tue attività di Tor dal tuo ISP.

### Tails

<div class="admonition recommendation" markdown>

![Logo di Tails](assets/img/linux-desktop/tails.svg){ align=right }

**Tails** è un sistema operativo live basato su Debian che instrada tutte le comunicazioni attraverso Tor, che può essere avviato su quasi tutti i computer da un'installazione su DVD, chiavetta USB o scheda SD. It uses [Tor](tor.md) to preserve privacy and [:material-incognito: Anonymity](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } while circumventing censorship, and it leaves no trace of itself on the computer it is used on after it is powered off.

[:octicons-home-16: Homepage](https://tails.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://tails.net/doc/index.en.html){ .card-link title=Documentation}
[:octicons-heart-16:](https://tails.net/donate){ .card-link title=Contribute }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Tails [non cancella](https://gitlab.tails.boum.org/tails/tails/-/issues/5356) la [memoria video](https://en.wikipedia.org/wiki/Dual-ported_video_RAM) allo spegnimento. Quando riavvii il computer dopo aver utilizzato Tails, è possibile che venga visualizzata brevemente l'ultima schermata visualizzata in Tails. Se spegni il computer invece di riavviarlo, la memoria video si cancellerà automaticamente dopo essere rimasta per qualche tempo senza alimentazione.

</div>

Tails è ottimo per contrastare le "ricerche forensi" grazie "all'amnesia" (nel senso che nulla viene scritto sul disco); tuttavia, non è una distribuzione rafforzata come Whonix. Manca di molte funzionalità per l'anonimato e la sicurezza possedute da Whonix e viene aggiornato molto meno spesso (soltanto una volta ogni sei settimane). A Tails system that is compromised by malware may potentially bypass the transparent proxy, allowing for the user to be deanonymized.

Tails includes [uBlock Origin](browser-extensions.md#ublock-origin) in Tor Browser by default, which may potentially make it easier for adversaries to fingerprint Tails users. Le macchine virtuali di [Whonix](desktop.md#whonix) potrebbero essere maggiormente a prova di fuga, tuttavia, non sono amnesiche, il che significa che i dati potrebbero essere recuperati dal tuo dispositivo d'archiviazione.

Di design, Tails dovrebbe resettarsi completamente dopo ogni riavvio. Encrypted [persistent storage](https://tails.net/doc/persistent_storage/index.en.html) can be configured to store some data between reboots.

## Distribuzioni incentrate sulla sicurezza

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: Attacchi Passivi](basics/common-threats.md#security-and-privacy ""){.pg-orange}

### Qubes OS

<div class="admonition recommendation" markdown>

![Logo di Qubes OS](assets/img/qubes/qubes_os.svg){ align=right }

**Qubes OS** è un sistema operativo open-source progettato per fornire una forte sicurezza per i computer desktop attraverso macchine virtuali sicure (o "qube"). Qubes si basa su Xen, X Window System e Linux. Può eseguire la maggior parte delle applicazioni Linux e utilizzare la maggior parte dei driver Linux.

[:octicons-home-16: Pagina Principale](https://qubes-os.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Servizio Onion" }
[:octicons-eye-16:](https://qubes-os.org/privacy){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://qubes-os.org/doc){ .card-link title=Documentazione }
[:octicons-code-16:](https://github.com/QubesOS){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://qubes-os.org/donate){ .card-link title=Contribuisci }

</details>

</div>

Qubes OS protegge il computer isolando i sottosistemi (ad esempio, rete, USB, ecc.) e applicazioni in *qubes* separati. Should one part of the system be compromised via an exploit in a [:material-target-account: Targeted Attack](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}, the extra isolation is likely to protect the rest of the *qubes* and the core system.

Per ulteriori informazioni sul funzionamento di Qubes, leggi la nostra pagina [Panoramica su Qubes OS](os/qubes-overview.md).

### Kicksecure

While we [recommend against](os/linux-overview.md#release-cycle) "perpetually outdated" distributions like Debian for desktop use in most cases, Kicksecure is a Debian-based operating system which has been hardened to be much more than a typical Linux install.

<div class="admonition recommendation" markdown>

![Logo di Kicksecure](assets/img/linux-desktop/kicksecure.svg){ align=right }

**Kicksecure**, in breve, consiste in una serie di script, configurazioni e pacchetti che riducono sostanzialmente la superficie di attacco di Debian. Copre di default molti dei consigli sulla privacy e la sicurezza. Inoltre, serve da OS di base per [Whonix](#whonix).

[:octicons-home-16: Pagina Principale](https://kicksecure.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kicksecure.com/wiki/Privacy_Policy){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://kicksecure.com/wiki/Documentation){ .card-link title=Documentazione }
[:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://kicksecure.com/wiki/Donate){ .card-link title=Contribuisci }

</details>

</div>

## Criteri

La scelta di una distro Linux adatta a te dipende da una grande varietà di preferenze personali e questa pagina **non** vuole essere un elenco esaustivo di tutte le distribuzioni possibili. La nostra pagina di panoramica su Linux contiene alcuni consigli sulla [scelta di una distro](os/linux-overview.md#choosing-your-distribution) in modo più dettagliato. Le distro presenti su *questa* pagina seguono tutte, in generale, le linee guida che abbiamo illustrato in quella pagina e soddisfano tutte questi standard:

- Gratuito e open source.
- Ricevono aggiornamenti regolari del software e del kernel.
- Avoids X11, as its last major release was [more than a decade](https://x.org/wiki/Releases) ago.
    - The notable exception here is Qubes, but the [isolation issues](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation) which X11 typically has are avoided by virtualization. This isolation only applies to apps *running in different qubes* (virtual machines); apps running in the *same* qube are not protected from each other.
- Supportano la crittografia del disco completo durante l'installazione.
- Non interrompono le versioni regolari per più di 1 anno.
    - [Sconsigliamo](os/linux-overview.md#release-cycle) le versioni di distribuzioni con "Supporto a Lungo Termine" o "stabile", per l'utilizzo da desktop.
- Supportano una vasta gamma di hardware.
- Preferiscono i progetti più grandi.
    - Mantenere un sistema operativo è un sfida importante e, i progetti più piccoli, tendono a compiere errori evitabili o a ritardare gli aggiornamenti critici (o peggio, scomparire interamente). Ci orientiamo verso progetti che, tra 10 anni, potrebbero essere ancora presenti (che sia grazie a supporto aziendale o supporto della community molto significativo), e ci allontaniamo da progetti costruiti a mano o aventi un numero ridotto di manutentori.

Inoltre, [i nostri criteri standard](about/criteria.md) per i progetti raccomandati sono ancora validi. **Si prega di notare che non siamo affiliati a nessuno dei progetti che raccomandiamo.**

[^1]: Reproducibility entails the ability to verify that packages and binaries made available to the end user match the source code, which can be useful against potential [:material-package-variant-closed-remove: Supply Chain Attacks](basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}.
