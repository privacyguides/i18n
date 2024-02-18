---
title: "Bureau/PC"
icon: simple/linux
description: Les distributions Linux sont généralement recommandées pour la protection de la vie privée et la liberté logicielle.
cover: desktop.webp
---

Les distributions Linux sont généralement recommandées pour la protection de la vie privée et la liberté logicielle. Si vous n'utilisez pas encore Linux, vous trouverez ci-dessous quelques distributions que nous vous suggérons d'essayer, ainsi que des conseils généraux d'amélioration de la sécurité et de la confidentialité qui s'appliquent à de nombreuses distributions Linux.

- [Vue d'ensemble de Linux :material-arrow-right-drop-circle:](os/linux-overview.md)

## Distributions traditionnelles

### Fedora Workstation

<div class="admonition recommendation" markdown>

![Fedora logo](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Workstation** is our recommended distribution for people new to Linux. Fedora adopte généralement les nouvelles technologies avant les autres distributions, par exemple, [Wayland](https://wayland.freedesktop.org/), [PipeWire](https://pipewire.org), et bientôt. Ces nouvelles technologies s'accompagnent souvent d'améliorations générales en matière de sécurité, de vie privée et d'ergonomie.

[:octicons-home-16: Page d'accueil](https://fedoraproject.org/workstation/){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=Documentation}
[:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribuer }

</details>

</div>

Fedora a un cycle de publication semi-continu. Si certains paquets comme [GNOME](https://www.gnome.org) sont gelés jusqu'à la prochaine version de Fedora, la plupart des paquets (y compris le noyau) sont mis à jour fréquemment tout au long de la durée de vie de la version. Chaque version de Fedora est supportée pendant un an, avec une nouvelle version publiée tous les 6 mois.

### openSUSE Tumbleweed

<div class="admonition recommendation" markdown>

![logo openSUSE Tumbleweed](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }

**openSUSE Tumbleweed** est une distribution stable à publication continue.

openSUSE Tumbleweed dispose d'un système de [mise à jour transactionnelle](https://kubic.opensuse.org/blog/2018-04-04-transactionalupdates/) qui utilise [Btrfs](https://en.wikipedia.org/wiki/Btrfs) et [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) pour s'assurer que les livraisons peuvent être annulées en cas de problème.

[:octicons-home-16: Page d'accueil](https://get.opensuse.org/fr/tumbleweed/){ .md-button .md-button--primary }
[:octicons-info-16:](https://doc.opensuse.org/fr/){ .card-link title=Documentation}
[:octicons-heart-16:](https://shop.opensuse.org/){ .card-link title=Contribuer }

</details>

</div>

Tumbleweed suit un modèle de publication continu où chaque mise à jour est publiée comme un instantané de la distribution. Lorsque vous mettez votre système à niveau, un nouvel instantané est téléchargé. Chaque livraison est soumise à une série de tests automatisés par [openQA](https://openqa.opensuse.org) afin de garantir sa qualité.

### Arch Linux

<div class="admonition recommendation" markdown>

![Logo Arch](assets/img/linux-desktop/archlinux.svg){ align=right }

**Arch Linux** est une distribution légère, de type do-it-yourself (DIY), ce qui signifie que vous n'obtenez que ce que vous installez. Pour plus d'informations, voir leur [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions_(Fran%C3%A7ais)).

[:octicons-home-16: Page d'accueil](https://archlinux.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.archlinux.org/title/Main_page_(Fran%C3%A7ais)){ .card-link title=Documentation}
[:octicons-heart-16:](https://archlinux.org/donate/){ .card-link title=Contribuer }

</details>

</div>

Arch Linux a un cycle de publication continue. Il n'y a pas de calendrier de publication fixe et les paquets sont mis à jour très fréquemment.

S'agissant d'une distribution DIY, vous êtes [censé mettre en place et maintenir](os/linux-overview.md#arch-based-distributions) votre système par vous-même. Arch a un [installateur officiel](https://wiki.archlinux.org/title/Archinstall_(Fran%C3%A7ais)) pour rendre le processus d'installation un peu plus facile.

Une grande partie des [paquets d'Arch Linux](https://reproducible.archlinux.org) sont [reproductibles](https://reproducible-builds.org).

## Atomic Distributions

**Atomic distributions** (sometimes also referred to as **immutable distributions**) are operating systems which handle package installation and updates by layering changes atop your core system image, rather than by directly modifying the system. This has advantages including increased stability and the ability to easily rollback updates. See [*Traditional vs. Atomic Updates*](os/linux-overview.md#traditional-vs-atomic-updates) for more info.

### Fedora Atomic Desktops

<div class="admonition recommendation" markdown>

![Fedora logo](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Atomic Desktops** are variants of Fedora which use the `rpm-ostree` package manager and have a strong focus on containerized workflows and Flatpak for desktop applications. Toutes ces variantes suivent le même calendrier de publication que Fedora Workstation, bénéficiant des mêmes mises à jour rapides et restant très proches de l'original.

[:octicons-home-16: Homepage](https://fedoraproject.org/atomic-desktops/){ .md-button .md-button--primary }
[:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribute }

</details>

</div>

The [Fedora Atomic Desktops](https://fedoramagazine.org/introducing-fedora-atomic-desktops/) come in a variety of flavors depending on the desktop environment you prefer, such as **Fedora Silverblue** (which comes with [GNOME](https://www.gnome.org/)), **Fedora Kinoite**, (which comes with [KDE](https://kde.org/)), **Fedora Sway Atomic**, or **Fedora Budgie Atomic**. However, we don't recommend the last of these as the Budgie desktop environment [still requires X11](https://buddiesofbudgie.org/blog/wayland).

These operating systems differ from Fedora Workstation as they replace the [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf/) package manager with a much more advanced alternative called [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/package-management/rpm-ostree/). The `rpm-ostree` package manager works by downloading a base image for the system, then overlaying packages over it in a [git](https://en.wikipedia.org/wiki/Git)-like commit tree. When the system is updated, a new base image is downloaded and the overlays will be applied to that new image.

After the update is complete you will reboot the system into the new deployment. `rpm-ostree` keeps two deployments of the system so that you can easily rollback if something breaks in the new deployment. There is also the option to pin more deployments as needed.

[Flatpak](https://www.flatpak.org) is the primary package installation method on these distributions, as `rpm-ostree` is only meant to overlay packages that cannot stay inside of a container on top of the base image.

As an alternative to Flatpaks, there is the option of [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox/) to create [Podman](https://podman.io) containers with a shared home directory with the host operating system and mimic a traditional Fedora environment, which is a [useful feature](https://containertoolbx.org) for the discerning developer.

### NixOS

<div class="admonition recommendation" markdown>

![Logo NixOS](assets/img/linux-desktop/nixos.svg){ align=right }

NixOS est une distribution indépendante basée sur le gestionnaire de paquets Nix avec un accent sur la reproductibilité et la fiabilité.

[:octicons-home-16: Page d'accueil](https://nixos.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=Documentation}
[:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=Contribuer }

</details>

</div>

NixOS’s package manager keeps every version of every package in a different folder in the **Nix store**. Due to this you can have different versions of the same package installed on your system. After the package contents have been written to the folder, the folder is made read-only.

NixOS also provides atomic updates; first it downloads (or builds) the packages and files for the new system generation and then switches to it. There are different ways to switch to a new generation; you can tell NixOS to activate it after reboot or you can switch to it at runtime. You can also *test* the new generation by switching to it at runtime, but not setting it as the current system generation. If something in the update process breaks, you can just reboot and automatically and return to a working version of your system.

Nix the package manager uses a purely functional language - which is also called Nix - to define packages.

[Nixpkgs](https://github.com/nixos/nixpkgs) (the main source of packages) are contained in a single GitHub repository. You can also define your own packages in the same language and then easily include them in your config.

Nix is a source-based package manager; if there’s no pre-built available in the binary cache, Nix will just build the package from source using its definition. It builds each package in a sandboxed *pure* environment, which is as independent of the host system as possible, thus making binaries reproducible.

## Distributions axées sur l'anonymat

### Whonix

<div class="admonition recommendation" markdown>

![logo Whonix](assets/img/linux-desktop/whonix.svg){ align=right }

**Whonix** est basée sur [Kicksecure](#kicksecure), une version de Debian axée sur la sécurité. Il vise à assurer la vie privée, la sécurité et l'anonymat sur Internet. Whonix est utilisé de préférence en conjonction avec [Qubes OS](#qubes-os).

[:octicons-home-16: Page d'accueil](https://www.whonix.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://www.whonix.org/wiki/Documentation){ .card-link title=Documentation}
[:octicons-heart-16:](https://www.whonix.org/wiki/Donate){ .card-link title=Contribuer }

</details>

</div>

Whonix is meant to run as two virtual machines: a “Workstation” and a Tor “Gateway.” All communications from the Workstation must go through the Tor gateway. This means that even if the Workstation is compromised by malware of some kind, the true IP address remains hidden.

Some of its features include Tor Stream Isolation, [keystroke anonymization](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak), [encrypted swap](https://github.com/Whonix/swap-file-creator), and a hardened memory allocator. Future versions of Whonix will likely include [full system AppArmor policies](https://github.com/Whonix/apparmor-profile-everything) and a [sandbox app launcher](https://www.whonix.org/wiki/Sandbox-app-launcher) to fully confine all processes on the system.

Whonix is best used [in conjunction with Qubes](https://www.whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers). We have a [recommended guide](os/qubes-overview.md#connecting-to-tor-via-a-vpn) on configuring Whonix in conjunction with a VPN ProxyVM in Qubes to hide your Tor activities from your ISP.

### Tails

<div class="admonition recommendation" markdown>

![Logo de Tails](assets/img/linux-desktop/tails.svg){ align=right }

**Tails** est un système d'exploitation autonome basé sur Debian qui fait passer toutes les communications par Tor, et qui peut démarrer sur presque n'importe quel ordinateur à partir d'un DVD, d'une clé USB ou d'une installation sur carte SD. Il utilise [Tor](tor.md) pour préserver la vie privée et l'anonymat tout en contournant la censure, et il ne laisse aucune trace de son passage sur l'ordinateur sur lequel il est utilisé après avoir été éteint.

[:octicons-home-16: Page d'accueil](https://tails.boum.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://tails.boum.org/doc/index.en.html){ .card-link title=Documentation}
[:octicons-heart-16:](https://tails.boum.org/donate/){ .card-link title=Contribuer }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Tails [doesn't erase](https://gitlab.tails.boum.org/tails/tails/-/issues/5356) the [video memory](https://en.wikipedia.org/wiki/Dual-ported_video_RAM) when shutting down. When you restart your computer after using Tails, it might briefly display the last screen that was displayed in Tails. If you shut down your computer instead of restarting it, the video memory will erase itself automatically after being unpowered for some time.

</div>

Tails is great for counter forensics due to amnesia (meaning nothing is written to the disk); however, it is not a hardened distribution like Whonix. It lacks many anonymity and security features that Whonix has and gets updated much less often (only once every six weeks). A Tails system that is compromised by malware may potentially bypass the transparent proxy allowing for the user to be deanonymized.

Tails includes [uBlock Origin](desktop-browsers.md#ublock-origin) in Tor Browser by default, which may potentially make it easier for adversaries to fingerprint Tails users. [Whonix](desktop.md#whonix) virtual machines may be more leak-proof, however they are not amnesic, meaning data may be recovered from your storage device.

By design, Tails is meant to completely reset itself after each reboot. Encrypted [persistent storage](https://tails.boum.org/doc/persistent_storage/index.en.html) can be configured to store some data between reboots.

## Distributions axées sur la sécurité

### Qubes OS

<div class="admonition recommendation" markdown>

![logo Qubes OS](assets/img/qubes/qubes_os.svg){ align=right }

**Qubes OS** est un système d'exploitation open-source conçu pour fournir une sécurité forte pour l'informatique de bureau à travers des machines virtuelles sécurisées (ou "qubes"). Qubes est basé sur Xen, le système de fenêtre X, et Linux. Il peut exécuter la plupart des applications Linux et utiliser la plupart des pilotes Linux.

[:octicons-home-16: Page d'accueil](https://www.qubes-os.org/){ .md-button .md-button--primary }
[:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Service onion" }
[:octicons-eye-16:](https://www.qubes-os.org/privacy/){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://www.qubes-os.org/doc/){ .card-link title=Documentation }
[:octicons-code-16:](https://github.com/QubesOS/){ .card-link title="Code source" }
[:octicons-heart-16:](https://www.qubes-os.org/donate/){ .card-link title=Contribuer }

</details>

</div>

Qubes OS secures the computer by isolating subsystems (e.g., networking, USB, etc.) and applications in separate *qubes*. Should one part of the system be compromised, the extra isolation is likely to protect the rest of the *qubes* and the core system.

For further information about how Qubes works, read our full [Qubes OS overview](os/qubes-overview.md) page.

### Kicksecure

While we [recommend against](os/linux-overview.md#release-cycle) "perpetually outdated" distributions like Debian for Desktop use in most cases, Kicksecure is a Debian-based operating system which has been hardened to be much more than a typical Linux install.

<div class="admonition recommendation" markdown>

![Logo Kicksecure](assets/img/linux-desktop/kicksecure.svg){ align=right }

**Kicksecure** - en termes simplifiés à l'extrême - est un ensemble de scripts, de configurations et de paquets qui réduisent considérablement la surface d'attaque de Debian. Il couvre par défaut un grand nombre de recommandations en matière de confidentialité et de durcissement. Il sert également de système d'exploitation de base pour [Whonix](#whonix).

[:octicons-home-16: Page d'accueil](https://www.kicksecure.com/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.kicksecure.com/wiki/Privacy_Policy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://www.kicksecure.com/wiki/Documentation){ .card-link title=Documentation }
[:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Code source" }
[:octicons-heart-16:](https://www.kicksecure.com/wiki/Donate){ .card-link title=Contribuer }

</details>

</div>

## Critères

Choosing a Linux distro that is right for you will come down to a huge variety of personal preferences, and this page is **not** meant to be an exhaustive list of every viable distribution. Our Linux overview page has some advice on [choosing a distro](os/linux-overview.md#choosing-your-distribution) in more detail. The distros on *this* page do all generally follow the guidelines we covered there, and all meet these standards:

- Gratuites et open source.
- Reçoivent régulièrement des mises à jour des logiciels et du noyau.
- [Évitent X11](os/linux-overview.md#wayland).
    - L'exception notable est Qubes, mais la virtualisation permet d'éviter les problèmes d'isolation que rencontre généralement X11. Cette isolation ne s'applique qu'aux applications *fonctionnant dans différents qubes* (machines virtuelles), les applications fonctionnant dans le *même* qube ne sont pas protégées les unes des autres.
- Prennent en charge le chiffrement complet du disque pendant l'installation.
- Ne gêlent pas les mises à jour régulières pendant plus d'un an.
    - Nous [ne recommandons pas](os/linux-overview.md#release-cycle) les versions "Long Term Support" ou "stables" de distributions pour une utilisation de bureau.
- Prennent en charge une grande variété de matériel.
- Préférence pour les projets de plus grande envergure.
    - La maintenance d'un système d'exploitation est un défi majeur, et les petits projets ont tendance à faire plus d'erreurs évitables ou à retarder les mises à jour critiques (ou pire, à disparaître complètement). Nous privilégions les projets qui seront probablement toujours présents dans 10 ans (que ce soit grâce au soutien d'une entreprise ou à un soutien communautaire très important), et nous évitons les projets qui sont construits de zéro ou qui ont un petit nombre de mainteneurs.

In addition, [our standard criteria](about/criteria.md) for recommended projects still applies. **Please note we are not affiliated with any of the projects we recommend.**
