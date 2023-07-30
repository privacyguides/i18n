---
title: "Desktop/PC"
icon: simple/linux
description: Linux-distributies worden algemeen aanbevolen voor privacybescherming en softwarevrijheid.
cover: desktop.png
---

Linux-distributies worden algemeen aanbevolen voor privacybescherming en softwarevrijheid. Als je nog geen Linux gebruikt, zijn hieronder enkele distributies die we aanraden om uit te proberen, evenals enkele algemene tips om je privacy en veiligheid te verbeteren die op veel Linux-distributies van toepassing zijn.

- [Algemeen Linux-overzicht :material-arrow-right-drop-circle:](os/linux-overview.md)

## Traditionele verdelingen

### Fedora Werkstation

!!! recommendation

    ![Fedora logo](assets/img/linux-desktop/fedora-workstation.svg){ align=right }
    
    **Fedora Workstation** is onze aanbevolen distributie voor mensen die nieuw zijn met Linux. Fedora adopteert over het algemeen nieuwere technologieën dan andere distributies, b.v. [Wayland](https://wayland.freedesktop.org/), [PipeWire](https://pipewire.org), en binnenkort. Deze nieuwe technologieën gaan vaak gepaard met verbeteringen op het gebied van veiligheid, privacy en bruikbaarheid in het algemeen.
    
    [:octicons-home-16: Homepage](https://fedoraproject.org/workstation/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=Documentation}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribute }

Fedora heeft een semi-rollende release cyclus. Terwijl sommige pakketten zoals [GNOME](https://www.gnome.org) bevroren worden tot de volgende Fedora uitgave, worden de meeste pakketten (inclusief de kernel) regelmatig bijgewerkt gedurende de levensduur van de uitgave. Elke Fedora release wordt een jaar lang ondersteund, met elke 6 maanden een nieuwe versie.

### openSUSE Tumbleweed

!!! recommendation

    ![openSUSE Tumbleweed logo](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }
    
    **openSUSE Tumbleweed** is een stabiele distributie met rollende release.
    
    openSUSE Tumbleweed heeft een [transactionele update](https://kubic.opensuse.org/blog/2018-04-04-transactionalupdates/) systeem dat gebruik maakt van [Btrfs](https://en.wikipedia.org/wiki/Btrfs) en [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) om ervoor te zorgen dat snapshots kunnen worden teruggerold mocht er een probleem zijn.
    
    [:octicons-home-16: Homepage](https://get.opensuse.org/tumbleweed/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://doc.opensuse.org/){ .card-link title=Documentatie}
    [:octicons-heart-16:](https://shop.opensuse.org/){ .card-link title=Bijdragen}

Tumbleweed volgt een rollend release-model waarbij elke update wordt vrijgegeven als een momentopname van de distributie. Wanneer je jouw systeem upgrade, wordt een nieuwe momentopname gedownload. Elke momentopname wordt door [openQA](https://openqa.opensuse.org) aan een reeks geautomatiseerde tests onderworpen om de kwaliteit ervan te verzekeren.

### Arch Linux

!!! recommendation

    ![Arch logo](assets/img/linux-desktop/archlinux.svg){ align=right }
    
    **Arch Linux** is een lichtgewicht, doe-het-zelf (DIY) distributie, wat betekent dat u alleen krijgt wat u installeert. Zie voor meer informatie hun [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions).
    
    [:octicons-home-16: Homepage](https://archlinux.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://wiki.archlinux.org/){ .card-link title=Documentatie}
    [:octicons-heart-16:](https://archlinux.org/donate/){ .card-link title=Bijdragen}

Arch Linux heeft een doorlopende uitgavecyclus. Er is geen vast releaseschema en pakketten worden zeer frequent bijgewerkt.

Omdat het een doe-het-zelf distributie is, wordt van je verwacht [dat je jouw systeem zelf opzet en onderhoudt](#arch-based-distributions). Arch heeft een [officiële installer](https://wiki.archlinux.org/title/Archinstall) om het installatieproces wat gemakkelijker te maken.

Een groot deel van [Arch Linux's pakketten](https://reproducible.archlinux.org) zijn [reproduceerbaar](https://reproducible-builds.org).

## Immutable distributies

### Fedora Silverblue

!!! recommendation

    ![Fedora Silverblue logo](assets/img/linux-desktop/fedora-silverblue.svg){ align=right }
    
    **Fedora Silverblue** en **Fedora Kinoite** zijn immutable varianten van Fedora met een sterke focus op container workflows. Silverblue wordt geleverd met de [GNOME](https://www.gnome.org/) desktop omgeving terwijl Kinoite wordt geleverd met [KDE](https://kde.org/). Silverblue en Kinoite volgen hetzelfde release schema als Fedora Workstation, profiteren van dezelfde snelle updates en blijven zeer dicht bij de upstream.
    
    [:octicons-home-16: Homepage](https://fedoraproject.org/silverblue/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/fedora-silverblue/){ .card-link title=Documentation}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribute }

Silverblue (and Kinoite) differ from Fedora Workstation as they replace the [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf/) package manager with a much more advanced alternative called [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/package-management/rpm-ostree/). De `rpm-ostree` pakketbeheerder werkt door een basis image voor het systeem te downloaden, en er dan pakketten overheen te leggen in een [git](https://en.wikipedia.org/wiki/Git)-achtige commit tree. Wanneer het systeem wordt bijgewerkt, wordt een nieuw basisbeeld gedownload en worden de overlays op dat nieuwe beeld toegepast.

Nadat de update is voltooid, start je het systeem opnieuw op in de nieuwe versie. `rpm-ostree` houdt twee versies van het systeem bij, zodat je gemakkelijk kunt terugdraaien als er iets kapot gaat in de nieuwe versie. Er is ook de mogelijkheid om meer versies vast te pinnen als dat nodig is.

[Flatpak](https://www.flatpak.org) is de primaire pakketinstallatiemethode op deze distributies, aangezien `rpm-ostree` alleen bedoeld is om pakketten die niet in een container kunnen blijven bovenop de basisafbeelding te plaatsen.

Als alternatief voor Flatpaks is er de optie [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox/) om [Podman](https://podman.io) containers te maken met een gedeelde home directory met het gast-besturingssysteem en een traditionele Fedora omgeving na te bootsen, wat een [nuttige eigenschap is](https://containertoolbx.org) voor de veeleisende ontwikkelaar.

### NixOS

!!! recommendation

    ![NixOS logo](assets/img/linux-desktop/nixos.svg){ align=right }
    
    NixOS is een onafhankelijke distributie gebaseerd op de Nix pakketbeheerder met een focus op reproduceerbaarheid en betrouwbaarheid.
    
    [:octicons-home-16: Homepage](https://nixos.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=Documentatie}
    [:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=Bijdragen}

De pakketbeheerder van NixOS bewaart elke versie van elk pakket in een andere map in de **Nix store**. Hierdoor kun je verschillende versies van hetzelfde pakket op jouw systeem geïnstalleerd hebben. Nadat de inhoud van het pakket naar de map is geschreven, wordt de map alleen-lezen gemaakt.

NixOS biedt ook atomaire updates; het downloadt (of bouwt) eerst de pakketten en bestanden voor de nieuwe systeemgeneratie en schakelt daar dan naar over. Er zijn verschillende manieren om over te schakelen naar een nieuwe generatie; je kunt NixOS vertellen deze te activeren na reboot of je kunt er tijdens runtime naar overschakelen. Je kunt ook *testen* de nieuwe generatie door er tijdens runtime naar over te schakelen, maar het niet in te stellen als de huidige systeemgeneratie. Als iets in het updateproces stuk gaat, kunt je gewoon opnieuw opstarten en automatisch terugkeren naar een werkende versie van jouw systeem.

Nix de pakketbeheerder gebruikt een zuiver functionele taal - die ook Nix wordt genoemd - om pakketten te definiëren.

[Nixpkgs](https://github.com/nixos/nixpkgs) (de belangrijkste bron van pakketten) zijn opgenomen in een enkele GitHub repository. Je kan ook je eigen packages definiëren in dezelfde taal en ze dan gemakkelijk opnemen in je config.

Nix is een source-based package manager; als er geen pre-built beschikbaar is in de binaire cache, zal Nix het pakket gewoon vanaf de broncode bouwen met behulp van zijn definitie. Het bouwt elk pakket in een sandboxed *pure* omgeving, die zo onafhankelijk mogelijk is van het hostsysteem, waardoor binaries reproduceerbaar zijn.

## Op anonimiteit gerichte distributies

### Whonix

!!! recommendation

    ![Whonix logo](assets/img/linux-desktop/whonix.svg){ align=right }
    
    **Whonix** is based on [Kicksecure](#kicksecure), a security-focused fork of Debian. Het is gefocust op privacy, veiligheid en anonimiteit op het internet te bieden. Whonix wordt het best gebruikt in combinatie met [Qubes OS](#qubes-os).
    
    [:octicons-home-16: Homepage](https://www.whonix.org/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://www.dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Onion Service" }
    [:octicons-info-16:](https://www.whonix.org/wiki/Documentation){ .card-link title=Documentatie}
    [:octicons-heart-16:](https://www.whonix.org/wiki/Donate){ .card-link title=Dragen bij }

Whonix is bedoeld om te draaien als twee virtuele machines: een "Workstation" en een Tor "Gateway" Alle communicatie van het werkstation moet via de Tor-gateway gaan. Dit betekent dat zelfs als het werkstation wordt gecompromitteerd door malware, het ware IP-adres verborgen blijft.

Enkele van de functies zijn Tor Stream Isolation, [keystroke anonymization](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak), [encrypted swap](https://github.com/Whonix/swap-file-creator), en een hardened memory allocator.

Toekomstige versies van Whonix zullen waarschijnlijk [full system AppArmor policies](https://github.com/Whonix/apparmor-profile-everything) en een [sandbox app launcher](https://www.whonix.org/wiki/Sandbox-app-launcher) bevatten om alle processen op het systeem volledig in te perken.

Whonix wordt het best gebruikt [in combinatie met Qubes](https://www.whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers), Qubes-Whonix heeft diverse [nadelen](https://forums.whonix.org/t/qubes-whonix-security-disadvantages-help-wanted/8581) in vergelijking met andere hypervisors.

### Tails

!!! recommendation

    ![Tails logo](assets/img/linux-desktop/tails.svg){ align=right }
    
    **Tails** is een live besturingssysteem gebaseerd op Debian dat alle communicatie via Tor laat lopen. Hij kan op bijna elke computer opstarten vanaf een DVD, USB-stick of SD-kaart.
    
    Het is bedoeld om de privacy en anonimiteit te bewaren, censuur te omzeilen en geen sporen achter te laten op de computer waarop het wordt gebruikt.

Het is de bedoeling dat Tails zichzelf reset na elke reboot. Versleutelde [persistente opslag](https://tails. boum. org/doc/first_steps/persistence/index. en. html) kan worden geconfigureerd om bepaalde gegevens op te slaan. Een Tails-systeem dat door malware is aangetast, kan de transparante proxy omzeilen, waardoor de gebruiker kan worden gedeanonimiseerd.

Tails bevat standaard [uBlock Origin](desktop-browsers.md#ublock-origin) in Tor Browser, wat het voor tegenstanders mogelijk gemakkelijker maakt om Tails-gebruikers te identificeren. [Whonix](desktop.md#whonix) virtuele machines zijn misschien lekbestendiger, maar ze zijn niet amnesisch, wat betekent dat gegevens kunnen worden teruggehaald van jouw opslagapparaat.

Het is de bedoeling dat Tails zichzelf volledig reset na elke herstart. Een versleutelde [persistente opslag](https://tails.boum.org/doc/persistent_storage/index.en.html) kan worden geconfigureerd om bepaalde gegevens tussen reboots op te slaan.

## Op veiligheid gerichte distributies

### Qubes OS

!!! recommendation

    ![Qubes OS logo](assets/img/qubes/qubes_os.svg){ align=right }
    
    **Qubes OS** is an open-source operating system designed to provide strong security for desktop computing through secure virtual machines (a.k.a. "Qubes"). Qubes is gebaseerd op Xen, het X Window System, en Linux, en kan de meeste Linux-toepassingen draaien en de meeste Linux-stuurprogramma's gebruiken.
    
    [:octicons-home-16: Homepage](https://www.qubes-os.org/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://www.qubes-os.org/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://www.qubes-os.org/doc/){ .card-link title=Documentation }
    [:octicons-code-16:](https://github.com/QubesOS/){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.qubes-os.org/donate/){ .card-link title=Contribute }

Qubes OS secures the computer by isolating subsystems (e.g., networking, USB, etc.) and applications in separate VMs. Should one part of the system be compromised, the extra isolation is likely to protect the rest of the system.

For further information about how Qubes works, read our full [Qubes OS overview](os/qubes-overview.md) page.

### Kicksecure

While we [recommend against](os/linux-overview.md#release-cycle) "perpetually outdated" distributions like Debian for Desktop use in most cases, Kicksecure is a Debian-based operating system which has been hardened to be much more than a typical Linux install.

!!! recommendation

    ![Kicksecure logo](assets/img/linux-desktop/kicksecure.svg){ align=right }
    
    **Kicksecure**—in oversimplified terms—is a set of scripts, configurations, and packages that substantially reduce the attack surface of Debian. Het dekt standaard een heleboel aanbevelingen voor privacy en hardening. It also serves as the base OS for [Whonix](#whonix).
    
    [:octicons-home-16: Homepage](https://www.kicksecure.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.kicksecure.com/wiki/Privacy_Policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://www.kicksecure.com/wiki/Documentation){ .card-link title=Documentation }
    [:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.kicksecure.com/wiki/Donate){ .card-link title=Contribute }

## Criteria

Choosing a Linux distro that is right for you will come down to a huge variety of personal preferences, and this page is **not** meant to be an exhaustive list of every viable distribution. Our Linux overview page has some advice on [choosing a distro](os/linux-overview.md#choosing-your-distribution) in more detail. The distros on *this* page do all generally follow the guidelines we covered there, and all meet these standards:

- Free and open-source.
- Receives regular software and kernel updates.
- [Avoids X11](os/linux-overview.md#wayland).
    - The notable exception here is Qubes, but the isolation issues which X11 typically has are avoided by virtualization. This isolation only applies to apps *running in different qubes* (virtual machines), apps running in the *same* qube are not protected from each other.
- Supports full-disk encryption during installation.
- Doesn't freeze regular releases for more than 1 year.
    - We [recommend against](os/linux-overview.md#release-cycle) "Long Term Support" or "stable" distro releases for desktop usage.
- Supports a wide variety of hardware.
- Preference towards larger projects.
    - Maintaining an operating system is a major challenge, and smaller projects have a tendency to make more avoidable mistakes, or delay critical updates (or worse, disappear entirely). We lean towards projects which will likely be around 10 years from now (whether that's due to corporate backing or very significant community support), and away from projects which are hand-built or have a small number of maintainers.

In addition, [our standard criteria](about/criteria.md) for recommended projects still applies. **Please note we are not affiliated with any of the projects we recommend.**
