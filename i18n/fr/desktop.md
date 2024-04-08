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

![Logo Fedora](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Workstation** est la distribution que nous recommandons aux personnes qui découvrent Linux. Fedora generally adopts newer technologies before other distributions e.g., [Wayland](https://wayland.freedesktop.org), [PipeWire](https://pipewire.org). Ces nouvelles technologies s'accompagnent souvent d'améliorations générales en matière de sécurité, de vie privée et d'ergonomie.

[:octicons-home-16: Homepage](https://fedoraproject.org/workstation){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs){ .card-link title=Documentation}
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title=Contribute }

</details>

</div>

Fedora a un cycle de publication semi-continu. While some packages like [GNOME](https://gnome.org) are frozen until the next Fedora release, most packages (including the kernel) are updated frequently throughout the lifespan of the release. Chaque version de Fedora est supportée pendant un an, avec une nouvelle version publiée tous les 6 mois.

### openSUSE Tumbleweed

<div class="admonition recommendation" markdown>

![logo openSUSE Tumbleweed](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }

**openSUSE Tumbleweed** est une distribution stable à publication continue.

openSUSE Tumbleweed has a [transactional update](https://kubic.opensuse.org/blog/2018-04-04-transactionalupdates) system that uses [Btrfs](https://en.wikipedia.org/wiki/Btrfs) and [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) to ensure that snapshots can be rolled back should there be a problem.

[:octicons-home-16: Homepage](https://get.opensuse.org/tumbleweed){ .md-button .md-button--primary }
[:octicons-info-16:](https://doc.opensuse.org){ .card-link title=Documentation}
[:octicons-heart-16:](https://shop.opensuse.org){ .card-link title=Contribute }

</details>

</div>

Tumbleweed suit un modèle de publication continu où chaque mise à jour est publiée comme un instantané de la distribution. Lorsque vous mettez votre système à niveau, un nouvel instantané est téléchargé. Chaque livraison est soumise à une série de tests automatisés par [openQA](https://openqa.opensuse.org) afin de garantir sa qualité.

### Arch Linux

<div class="admonition recommendation" markdown>

![Logo Arch](assets/img/linux-desktop/archlinux.svg){ align=right }

**Arch Linux** est une distribution légère, de type do-it-yourself (DIY), ce qui signifie que vous n'obtenez que ce que vous installez. Pour plus d'informations, voir leur [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions_(Fran%C3%A7ais)).

[:octicons-home-16: Homepage](https://archlinux.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.archlinux.org){ .card-link title=Documentation}
[:octicons-heart-16:](https://archlinux.org/donate){ .card-link title=Contribute }

</details>

</div>

Arch Linux a un cycle de publication continue. Il n'y a pas de calendrier de publication fixe et les paquets sont mis à jour très fréquemment.

S'agissant d'une distribution DIY, vous êtes [censé mettre en place et maintenir](os/linux-overview.md#arch-based-distributions) votre système par vous-même. Arch a un [installateur officiel](https://wiki.archlinux.org/title/Archinstall_(Fran%C3%A7ais)) pour rendre le processus d'installation un peu plus facile.

Une grande partie des [paquets d'Arch Linux](https://reproducible.archlinux.org) sont [reproductibles](https://reproducible-builds.org).

## Distributions atomiques

**Les distributions atomiques** (parfois également appelées **distributions immuables**) sont des systèmes d'exploitation qui gèrent l'installation et la mise à jour des paquets en superposant les changements à l'image de base du système, plutôt qu'en modifiant directement le système. Cela présente des avantages, notamment une plus grande stabilité et la possibilité de revenir facilement en arrière sur les mises à jour. Voir [*Mises à jour traditionnelles vs. atomiques*](os/linux-overview.md#traditional-vs-atomic-updates) pour plus d'informations.

### Fedora Atomic Desktops

<div class="admonition recommendation" markdown>

![Logo Fedora](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Atomic Desktops** sont des variantes de Fedora qui utilisent le gestionnaire de paquets `rpm-ostree` et qui sont fortement axées sur les flux de travail conteneurisés et Flatpak pour les applications de bureau. Toutes ces variantes suivent le même calendrier de publication que Fedora Workstation, bénéficiant des mêmes mises à jour rapides et restant très proches de l'original.

[:octicons-home-16: Homepage](https://fedoraproject.org/atomic-desktops){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/emerging){ .card-link title=Documentation}
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title=Contribute }

</details>

</div>

The [Fedora Atomic Desktops](https://fedoramagazine.org/introducing-fedora-atomic-desktops) come in a variety of flavors depending on the desktop environment you prefer, such as **Fedora Silverblue** (which comes with [GNOME](https://gnome.org)), **Fedora Kinoite**, (which comes with [KDE](https://kde.org)), **Fedora Sway Atomic**, or **Fedora Budgie Atomic**. Cependant, nous ne recommandons pas la dernière solution car l'environnement de bureau Budgie [nécessite toujours X11](https://buddiesofbudgie.org/blog/wayland).

These operating systems differ from Fedora Workstation as they replace the [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf) package manager with a much more advanced alternative called [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/package-management/rpm-ostree). Le gestionnaire de paquets `rpm-ostree` fonctionne en téléchargeant une image de base pour le système, puis en superposant des paquets par-dessus dans une arborescence de commits semblable à [git](https://en.wikipedia.org/wiki/Git). Lorsque le système est mis à jour, une nouvelle image de base est téléchargée et les surcouches seront appliquées à cette nouvelle image.

Une fois la mise à jour terminée, vous redémarrerez le système sur le nouveau déploiement. `rpm-ostree` conserve deux déploiements du système afin que vous puissiez facilement revenir en arrière si quelque chose se casse dans le nouveau déploiement. Il est également possible d'épingler plus de déploiements selon les besoins.

[Flatpak](https://flatpak.org) is the primary package installation method on these distributions, as `rpm-ostree` is only meant to overlay packages that cannot stay inside of a container on top of the base image.

As an alternative to Flatpaks, there is the option of [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox) to create [Podman](https://podman.io) containers with a shared home directory with the host operating system and mimic a traditional Fedora environment, which is a [useful feature](https://containertoolbx.org) for the discerning developer.

### NixOS

<div class="admonition recommendation" markdown>

![Logo NixOS](assets/img/linux-desktop/nixos.svg){ align=right }

NixOS est une distribution indépendante basée sur le gestionnaire de paquets Nix avec un accent sur la reproductibilité et la fiabilité.

[:octicons-home-16: Homepage](https://nixos.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=Documentation}
[:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=Contribute }

</details>

</div>

Le gestionnaire de paquets de NixOS conserve chaque version de chaque paquet dans un dossier différent dans le **magasin Nix**. De ce fait, vous pouvez avoir différentes versions d'un même paquet installé sur votre système. Une fois que le contenu du paquet a été écrit dans le dossier, ce dernier est mis en lecture seule.

NixOS fournit également des mises à jour atomiques ; il télécharge d'abord (ou construit) les paquets et les fichiers pour la nouvelle génération de système et ensuite bascule dessus. Il y a différentes façons de passer à une nouvelle génération ; vous pouvez dire à NixOS de l'activer après le redémarrage ou vous pouvez basculer sur celle-ci pendant l'exécution. Vous pouvez également *tester* la nouvelle génération en basculant sur celle-ci pendant l'exécution, mais sans la définir comme la génération actuelle du système. Si quelque chose se casse pendant le processus de mise à jour, vous pouvez simplement redémarrer et revenir automatiquement à une version fonctionnelle de votre système.

Nix, le gestionnaire de paquets, utilise un langage purement fonctionnel - qui s'appelle aussi Nix - pour définir les paquets.

[Nixpkgs](https://github.com/nixos/nixpkgs) (la source principale des paquets) sont contenus dans un seul dépôt GitHub. Vous pouvez également définir vos propres paquets dans le même langage, puis les inclure facilement dans votre configuration.

Nix est un gestionnaire de paquets basé sur les sources ; s'il n'y a pas de paquet pré-construit disponible dans le cache binaire, Nix construira simplement le paquet à partir des sources en utilisant sa définition. Il construit chaque paquet dans un environnement *pur* en bac à sable, qui est aussi indépendant que possible du système hôte, ce qui rend les binaires reproductibles.

## Distributions axées sur l'anonymat

### Whonix

<div class="admonition recommendation" markdown>

![logo Whonix](assets/img/linux-desktop/whonix.svg){ align=right }

**Whonix** est basée sur [Kicksecure](#kicksecure), une version de Debian axée sur la sécurité. Il vise à assurer la vie privée, la sécurité et l'anonymat sur Internet. Whonix est utilisé de préférence en conjonction avec [Qubes OS](#qubes-os).

[:octicons-home-16: Homepage](https://whonix.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://whonix.org/wiki/Documentation){ .card-link title=Documentation}
[:octicons-heart-16:](https://whonix.org/wiki/Donate){ .card-link title=Contribute }

</details>

</div>

Whonix est conçu pour fonctionner sous la forme de deux machines virtuelles : une "Station de travail" et une "Passerelle" Tor. Toutes les communications de la Station de travail doivent passer par la passerelle Tor. Cela signifie que même si la Station de travail est compromise par un logiciel malveillant quelconque, la véritable adresse IP reste cachée.

Some of its features include Tor Stream Isolation, [keystroke anonymization](https://whonix.org/wiki/Keystroke_Deanonymization#Kloak), [encrypted swap](https://github.com/Whonix/swap-file-creator), and a hardened memory allocator. Future versions of Whonix will likely include [full system AppArmor policies](https://github.com/Whonix/apparmor-profile-everything) and a [sandbox app launcher](https://whonix.org/wiki/Sandbox-app-launcher) to fully confine all processes on the system.

Whonix is best used [in conjunction with Qubes](https://whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers). Nous avons un [guide recommandé](os/qubes-overview.md#connecting-to-tor-via-a-vpn) sur la configuration de Whonix en conjonction avec un VPN ProxyVM dans Qubes pour cacher vos activités Tor à votre FAI.

### Tails

<div class="admonition recommendation" markdown>

![Logo de Tails](assets/img/linux-desktop/tails.svg){ align=right }

**Tails** est un système d'exploitation autonome basé sur Debian qui fait passer toutes les communications par Tor, et qui peut démarrer sur presque n'importe quel ordinateur à partir d'un DVD, d'une clé USB ou d'une installation sur carte SD. Il utilise [Tor](tor.md) pour préserver la vie privée et l'anonymat tout en contournant la censure, et il ne laisse aucune trace de son passage sur l'ordinateur sur lequel il est utilisé après avoir été éteint.

[:octicons-home-16: Homepage](https://tails.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://tails.net/doc/index.en.html){ .card-link title=Documentation}
[:octicons-heart-16:](https://tails.net/donate){ .card-link title=Contribute }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Tails [n'efface pas](https://gitlab.tails.boum.org/tails/tails/-/issues/5356) la [mémoire vidéo](https://en.wikipedia.org/wiki/Dual-ported_video_RAM) lors de l'arrêt. Lorsque vous redémarrez votre ordinateur après avoir utilisé Tails, il se peut qu'il affiche brièvement le dernier écran affiché dans Tails. Si vous éteignez votre ordinateur au lieu de le redémarrer, la mémoire vidéo s'effacera automatiquement après un certain temps d'inactivité.

</div>

Tails est excellent pour la contre-analyse en raison de son amnésie (ce qui signifie que rien n'est écrit sur le disque) ; cependant, ce n'est pas une distribution renforcée comme Whonix. Elle ne dispose pas de nombreuses fonctions d'anonymat et de sécurité comme Whonix et est mise à jour beaucoup moins souvent (seulement une fois toutes les six semaines). Un système Tails compromis par un logiciel malveillant peut potentiellement contourner le proxy transparent et permettre à l'utilisateur d'être désanonymisé.

Tails includes [uBlock Origin](browser-extensions.md#ublock-origin) in Tor Browser by default, which may potentially make it easier for adversaries to fingerprint Tails users. Les machines virtuelles [Whonix](desktop.md#whonix) sont peut-être plus étanches, mais elles ne sont pas amnésiques, ce qui signifie que les données peuvent être récupérées sur votre périphérique de stockage.

De par sa conception, Tails est censé se réinitialiser complètement après chaque redémarrage. Encrypted [persistent storage](https://tails.net/doc/persistent_storage/index.en.html) can be configured to store some data between reboots.

## Distributions axées sur la sécurité

### Qubes OS

<div class="admonition recommendation" markdown>

![logo Qubes OS](assets/img/qubes/qubes_os.svg){ align=right }

**Qubes OS** est un système d'exploitation open-source conçu pour fournir une sécurité forte pour l'informatique de bureau à travers des machines virtuelles sécurisées (ou "qubes"). Qubes est basé sur Xen, le système de fenêtre X, et Linux. Il peut exécuter la plupart des applications Linux et utiliser la plupart des pilotes Linux.

[:octicons-home-16: Homepage](https://qubes-os.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://qubes-os.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://qubes-os.org/doc){ .card-link title=Documentation }
[:octicons-code-16:](https://github.com/QubesOS){ .card-link title="Source Code" }
[:octicons-heart-16:](https://qubes-os.org/donate){ .card-link title=Contribute }

</details>

</div>

Qubes OS sécurise l'ordinateur en isolant les sous-systèmes (par exemple, le réseau, l'USB, etc.) et les applications dans des *qubes* distincts. Si une partie du système est compromise, l'isolation supplémentaire est susceptible de protéger le reste des *qubes* et le système central.

Pour plus d'informations sur le fonctionnement de Qubes, lisez notre page [Introduction à Qubes](os/qubes-overview.md).

### Kicksecure

Bien que nous [déconseillions](os/linux-overview.md#release-cycle) d'utiliser des distributions "perpétuellement obsolètes" comme Debian pour un usage bureautique dans la plupart des cas, Kicksecure est un système d'exploitation basé sur Debian qui a été renforcé pour être bien plus qu'une installation Linux classique.

<div class="admonition recommendation" markdown>

![Logo Kicksecure](assets/img/linux-desktop/kicksecure.svg){ align=right }

**Kicksecure** - en termes simplifiés à l'extrême - est un ensemble de scripts, de configurations et de paquets qui réduisent considérablement la surface d'attaque de Debian. Il couvre par défaut un grand nombre de recommandations en matière de confidentialité et de durcissement. Il sert également de système d'exploitation de base pour [Whonix](#whonix).

[:octicons-home-16: Homepage](https://kicksecure.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kicksecure.com/wiki/Privacy_Policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kicksecure.com/wiki/Documentation){ .card-link title=Documentation }
[:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Source Code" }
[:octicons-heart-16:](https://kicksecure.com/wiki/Donate){ .card-link title=Contribute }

</details>

</div>

## Critères

Le choix d'une distribution Linux qui vous convient dépend d'une grande variété de préférences personnelles, et cette page n'est **pas** une liste exhaustive de toutes les distributions viables. Notre page d'introduction à Linux contient des conseils plus détaillés sur [le choix d'une distribution](os/linux-overview.md#choosing-your-distribution). Les distributions sur *cette* page suivent généralement les lignes directrices que nous avons abordées là-bas, et respectent toutes ces normes :

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

En outre, [nos critères standards](about/criteria.md) pour les projets recommandés s'appliquent toujours. **Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.**
