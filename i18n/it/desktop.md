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

These operating systems differ from Fedora Workstation as they replace the [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf/) package manager with a much more advanced alternative called [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/package-management/rpm-ostree/). The `rpm-ostree` package manager works by downloading a base image for the system, then overlaying packages over it in a [git](https://en.wikipedia.org/wiki/Git)-like commit tree. When the system is updated, a new base image is downloaded and the overlays will be applied to that new image.

After the update is complete you will reboot the system into the new deployment. `rpm-ostree` keeps two deployments of the system so that you can easily rollback if something breaks in the new deployment. There is also the option to pin more deployments as needed.

[Flatpak](https://www.flatpak.org) is the primary package installation method on these distributions, as `rpm-ostree` is only meant to overlay packages that cannot stay inside of a container on top of the base image.

As an alternative to Flatpaks, there is the option of [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox/) to create [Podman](https://podman.io) containers with a shared home directory with the host operating system and mimic a traditional Fedora environment, which is a [useful feature](https://containertoolbx.org) for the discerning developer.

### NixOS

<div class="admonition recommendation" markdown>

![Logo di NixOS](assets/img/linux-desktop/nixos.svg){ align=right }

NixOS è una distribuzione indipendente basata sul gestore di pacchetti Nix, incentrata sulla riproducibilità e l'affidabilità.

[:octicons-home-16: Home](https://nixos.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=Documentazione}
[:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=Contribuisci }

</details>

</div>

NixOS’s package manager keeps every version of every package in a different folder in the **Nix store**. Due to this you can have different versions of the same package installed on your system. After the package contents have been written to the folder, the folder is made read-only.

NixOS also provides atomic updates; first it downloads (or builds) the packages and files for the new system generation and then switches to it. There are different ways to switch to a new generation; you can tell NixOS to activate it after reboot or you can switch to it at runtime. You can also *test* the new generation by switching to it at runtime, but not setting it as the current system generation. If something in the update process breaks, you can just reboot and automatically and return to a working version of your system.

Nix the package manager uses a purely functional language - which is also called Nix - to define packages.

[Nixpkgs](https://github.com/nixos/nixpkgs) (the main source of packages) are contained in a single GitHub repository. You can also define your own packages in the same language and then easily include them in your config.

Nix is a source-based package manager; if there’s no pre-built available in the binary cache, Nix will just build the package from source using its definition. It builds each package in a sandboxed *pure* environment, which is as independent of the host system as possible, thus making binaries reproducible.

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

Whonix is meant to run as two virtual machines: a “Workstation” and a Tor “Gateway.” All communications from the Workstation must go through the Tor gateway. This means that even if the Workstation is compromised by malware of some kind, the true IP address remains hidden.

Some of its features include Tor Stream Isolation, [keystroke anonymization](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak), [encrypted swap](https://github.com/Whonix/swap-file-creator), and a hardened memory allocator. Future versions of Whonix will likely include [full system AppArmor policies](https://github.com/Whonix/apparmor-profile-everything) and a [sandbox app launcher](https://www.whonix.org/wiki/Sandbox-app-launcher) to fully confine all processes on the system.

Whonix is best used [in conjunction with Qubes](https://www.whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers). We have a [recommended guide](os/qubes-overview.md#connecting-to-tor-via-a-vpn) on configuring Whonix in conjunction with a VPN ProxyVM in Qubes to hide your Tor activities from your ISP.

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

Tails [doesn't erase](https://gitlab.tails.boum.org/tails/tails/-/issues/5356) the [video memory](https://en.wikipedia.org/wiki/Dual-ported_video_RAM) when shutting down. When you restart your computer after using Tails, it might briefly display the last screen that was displayed in Tails. If you shut down your computer instead of restarting it, the video memory will erase itself automatically after being unpowered for some time.

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

Choosing a Linux distro that is right for you will come down to a huge variety of personal preferences, and this page is **not** meant to be an exhaustive list of every viable distribution. Our Linux overview page has some advice on [choosing a distro](os/linux-overview.md#choosing-your-distribution) in more detail. The distros on *this* page do all generally follow the guidelines we covered there, and all meet these standards:

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

In addition, [our standard criteria](about/criteria.md) for recommended projects still applies. **Please note we are not affiliated with any of the projects we recommend.**
