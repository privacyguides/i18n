---
title: Aperçu de Linux
icon: simple/linux
description: Linux est un système d'exploitation de bureau alternatif open-source, axé sur la protection de la vie privée, mais toutes les distributions ne sont pas égales.
---

**Linux** est un système d'exploitation de bureau alternatif, open-source et axé sur la protection de la vie privée. Face à l'omniprésence de la télémétrie et d'autres technologies portant atteinte à la vie privée dans les systèmes d'exploitation grand public, Linux est resté le choix le plus évident pour les personnes désireuses de contrôler totalement leur ordinateur de zéro.

Notre site web utilise généralement le terme "Linux" pour décrire les distributions Linux de **bureau**. Les autres systèmes d'exploitation qui utilisent également le noyau Linux, tels que ChromeOS, Android et Qubes OS, ne sont pas abordés sur cette page.

[Nos recommandations Linux :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Remarque de sécurité

Il y a quelques problèmes de sécurité avec Linux dont vous devriez être conscient. Malgré ces inconvénients, les distributions Linux de bureau restent excellentes pour la plupart des personnes qui souhaitent :

- Éviter la télémétrie qui accompagne souvent les systèmes d'exploitation propriétaires
- Maintenir la [liberté des logiciels](https://gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Utiliser des systèmes axés sur la protection de la vie privée tels que [Whonix](../desktop.md#whonix) ou [Tails](../desktop.md#tails)

### Sécurité de l'open source

It is a [common misconception](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) that Linux and other open-source software are inherently secure simply because the source code is available. On s'attend à ce que la communauté effectue des vérifications régulièrement, mais ce n'est pas toujours [le cas](https://seirdy.one/posts/2022/02/02/floss-security).

En réalité, la sécurité d'une distribution dépend d'un certain nombre de facteurs, tels que l'activité du projet, l'expérience des développeurs, le niveau de rigueur appliqué aux révisions de code et l'attention portée à des parties spécifiques de la base de code qui peuvent rester non touchées pendant des années.

### Fonctionnalités de sécurité manquantes

À l'heure actuelle, le système d'exploitation Linux de bureau [n'est pas à la hauteur des alternatives](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) telles que macOS ou Android en ce qui concerne certaines fonctions de sécurité. Nous espérons voir des améliorations dans ces domaines à l'avenir.

- Le **démarrage vérifié** sur Linux n'est pas aussi robuste que les alternatives telles que le [démarrage sécurisé](https://support.apple.com/guide/security/secac71d5623/web) d'Apple ou le [démarrage vérrifié](https://source.android.com/security/verifiedboot) d'Android. Le démarrage vérifié prévient les altérations persistantes par les logiciels malveillants et les [attaques evil maid](https://en.wikipedia.org/wiki/Evil_Maid_attack), mais il est encore largement [non présent, même sur les distributions les plus avancées](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- Un **sandboxing solide** pour les applications sous Linux fait cruellement défaut, même avec des applications conteneurisées comme Flatpaks ou des solutions de sandboxing comme Firejail. Flatpak is the most promising sandboxing utility for Linux thus far, but is still deficient in many areas and allows for [unsafe defaults](https://flatkill.org/2020) which permit most apps to trivially bypass their sandbox.

En outre, Linux est en retard dans la mise en œuvre de [mesures d'atténuation des exploits](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) qui sont désormais standard sur d'autres systèmes d'exploitation, tels que Arbitrary Code Guard sur Windows ou Hardened Runtime sur macOS. De plus, la plupart des programmes Linux et Linux lui-même sont codés dans des langages peu sûrs pour la mémoire. Les bugs de corruption de la mémoire sont responsables de la [majorité des vulnérabilités](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code) corrigées et affectées d'un CVE. While this is also true for Windows and macOS, they are quickly making progress on adopting memory-safe languages such as Rust and Swift, respectively.

## Choisir sa distribution

Toutes les distributions Linux ne sont pas créées égales. Notre [page de recommandation Linux](../desktop.md) n'est pas censée faire autorité quant au choix de la distribution à utiliser, mais nos recommandations *sont* alignées sur les lignes directrices suivantes. Voici quelques éléments à prendre en compte lors du choix d'une distribution :

### Cycle de mises à jour

Nous vous recommandons vivement de choisir des distributions qui restent proches des versions stables des logiciels en amont, souvent appelées distributions à publications continues. En effet, les distributions à cycle de publication gelé ne mettent souvent pas à jour les versions des paquets et prennent du retard sur les mises à jour de sécurité.

Pour les distributions gelées telles que [Debian](https://debian.org/security/faq#handling), les responsables de paquets sont censés importer les correctifs pour corriger les vulnérabilités plutôt que de faire passer le logiciel à la "prochaine version" publiée par le développeur en amont. Some security fixes (particularly for less popular software) [do not](https://arxiv.org/abs/2105.14565) receive a [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) at all and therefore do not make it into the distribution with this patching model. Par conséquent, les correctifs de sécurité mineurs sont parfois reportés à la prochaine version majeure.

Nous ne pensons pas que retenir les paquets et appliquer des correctifs provisoires soit une bonne idée, car cela s'écarte de la manière dont le développeur aurait pu vouloir que le logiciel fonctionne. [Richard Brown](https://rootco.de/aboutme) propose une présentation à ce sujet :

- [Regular Releases are Wrong, Roll for your life](https://youtu.be/i8c0mg_mS7U) <small>(YouTube)</small>

### Traditional vs Atomic Updates

Traditionnellement, les distributions Linux se mettent à jour en mettant séquentiellement à jour les paquets souhaités. Traditional updates such as those used in Fedora, Arch Linux, and Debian-based distributions can be less reliable if an error occurs while updating.

Distros which use atomic updates, on the other hand, apply updates in full or not at all. On an atomic distribution, if an error occurs while updating (perhaps due to a power failure), nothing is changed on the system.

The atomic update method can achieve reliability with this model and is used for [distributions](../desktop.md#atomic-distributions) like Silverblue and NixOS. [Adam Šamalík](https://twitter.com/adsamalik) provides a presentation on how `rpm-ostree` works with Silverblue:

- [Let's try Fedora Silverblue — an immutable desktop OS! - Adam Šamalík](https://youtu.be/-hpV5l-gJnQ) <small>(YouTube)</small>

### "Distributions "axées sur la sécurité

Il y a souvent une certaine confusion entre les distributions "axées sur la sécurité" et les distributions pour les "tests de pénétration". Une recherche rapide sur "la distribution Linux la plus sûre" donne souvent des résultats tels que Kali Linux, Black Arch ou Parrot OS. Ces distributions sont des distributions de tests de pénétration offensifs qui regroupent des outils pour tester d'autres systèmes. Elles n'incluent pas de "sécurité supplémentaire" ni de mesures d'atténuation défensives destinées à une utilisation régulière.

### Distributions basées sur Arch Linux

Arch et les distributions basées sur Arch ne sont pas recommandées pour ceux qui débutent avec Linux (quelle que soit la distribution) car elles nécessitent [une maintenance régulière du système](https://wiki.archlinux.org/title/System_maintenance). Arch n'a pas de mécanisme de mise à jour de la distribution pour les choix logiciels sous-jacents. As a result you have to stay aware with current trends and adopt technologies on your own as they supersede older practices.

For a secure system, you are also expected to have sufficient Linux knowledge to properly set up security for their system such as adopting a [mandatory access control](#mandatory-access-control) system, setting up [kernel module](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) blacklists, hardening boot parameters, manipulating [sysctl](https://en.wikipedia.org/wiki/Sysctl) parameters, and knowing what components they need such as [Polkit](https://en.wikipedia.org/wiki/Polkit).

Toute personne utilisant le [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **doit** être à l'aise avec l'audit des PKGBUILDs qu'elle télécharge depuis ce service. AUR packages are community-produced content and are not vetted in any way, and therefore are vulnerable to software [:material-package-variant-closed-remove: Supply Chain Attacks](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}, which has in fact happened [in the past](https://bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository).

Le AUR doit toujours être utilisé avec parcimonie, et l'on trouve souvent de nombreux mauvais conseils sur diverses pages qui incitent les gens à utiliser aveuglément [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) sans avertissement suffisant. Similar warnings apply to the use of third-party Personal Package Archives (PPAs) on Debian-based distributions or Community Projects (COPR) on Fedora.

Si vous avez de l'expérience avec Linux et que vous souhaitez utiliser une distribution basée sur Arch, nous recommandons généralement la version principale d'Arch Linux plutôt que l'un de ses dérivés.

En outre, nous ne recommandons particulièrement **pas** ces deux dérivés d'Arch :

- **Manjaro**: cette distribution bloque les mises à jour des paquets pendant 2 semaines pour s'assurer que leurs propres changements ne cassent pas, et non pas pour s'assurer que l'amont est stable. Lorsque des paquets AUR sont utilisés, ils sont souvent construits avec les dernières [bibliothèques](https://en.wikipedia.org/wiki/Library_(computing)) des dépôts d'Arch.
- **Garuda**: ils utilisent [Chaotic-AUR](https://aur.chaotic.cx) qui compile automatiquement et aveuglément les paquets de l'AUR. Il n'existe aucun processus de vérification pour s'assurer que les paquets AUR ne souffrent pas d'attaques de la chaîne d'approvisionnement.

### Le noyau Linux-libre et les distributions "libres"

Nous vous **déconseillons d'**utiliser le noyau Linux-libre, car il [supprime les mesures d'atténuation de la sécurité](https://phoronix.com/news/GNU-Linux-Libre-5.7-Released) et les [avertissements du noyau](https://news.ycombinator.com/item?id=29674846) concernant le microcode vulnérable.

### Mandatory access control

Mandatory access control is a set of additional security controls which help to confine parts of the system such as apps and system services. The two common forms of mandatory access control found in Linux distributions are [SELinux](https://github.com/SELinuxProject) and [AppArmor](https://apparmor.net). Fedora and Tumbleweed use SELinux by default, with Tumbleweed offering an option in its installer to choose AppArmor instead.

SELinux on [Fedora](https://docs.fedoraproject.org/en-US/quick-docs/selinux-getting-started) confines Linux containers, virtual machines, and service daemons by default. AppArmor is used by the snap daemon for [sandboxing](https://snapcraft.io/docs/security-sandboxing) snaps which have [strict](https://snapcraft.io/docs/snap-confinement) confinement such as [Firefox](https://snapcraft.io/firefox). There is a community effort to confine more parts of the system in Fedora with the [ConfinedUsers](https://fedoraproject.org/wiki/SIGs/ConfinedUsers) special interest group.

## Recommandations générales

### Chiffrement de disque

La plupart des distributions Linux ont une option dans leur installateur pour activer [LUKS](../encryption.md#linux-unified-key-setup) FDE. If this option isn’t set at installation time, you will have to back up your data and re-install, as encryption is applied after [disk partitioning](https://en.wikipedia.org/wiki/Disk_partitioning), but before [file systems](https://en.wikipedia.org/wiki/File_system) are formatted. Nous vous suggérons également d'effacer de façon sécurisée votre dispositif de stockage :

- [Effacement sécurisé des données :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure)

### Swap

Envisagez d'utiliser [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) au lieu d'un fichier swap traditionnel ou d'une partition afin d'éviter d'écrire des données de mémoire potentiellement sensibles sur un stockage permanent (et d'améliorer les performances). Les distributions basées sur Fedora [utilisent ZRAM par défaut](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

Si vous avez besoin d'une fonctionnalité de suspension sur disque (hibernation), vous devrez toujours utiliser un fichier ou une partition swap. Veillez à ce que l'espace swap que vous avez sur un périphérique de stockage persistant soit au minimum [chiffré](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) afin d'atténuer certaines de ces menaces.

### Micrologiciel propriétaire (mises à jour du microcode)

Certaines distributions Linux (telles que les distributions basées sur [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)ou les distributions DIY) ne sont pas livrées avec les mises à jour propriétaires du [microcode](https://en.wikipedia.org/wiki/Microcode) qui corrigent les failles de sécurité critiques. Parmi les exemples notables de ces vulnérabilités figurent [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)) et d'autres [vulnérabilités matérielles](https://kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

Nous **recommandons vivement** d'installer les mises à jour du microcode, car elles contiennent d'importants correctifs de sécurité pour l'unité centrale qui ne peuvent pas être entièrement atténués par le logiciel seul. Fedora and openSUSE both apply microcode updates by default.

### Mises à jour

La plupart des distributions Linux installent automatiquement les mises à jour ou vous rappellent de le faire. Il est important de maintenir votre système d'exploitation à jour afin que votre logiciel soit corrigé lorsqu'une vulnérabilité est découverte.

Certaines distributions (en particulier celles destinées aux utilisateurs avancés) sont plus dépouillées et attendent de vous que vous fassiez les choses vous-même (par exemple Arch ou Debian). Il faudra manuellement exécuter le "gestionnaire de paquets" (`apt`, `pacman`, `dnf`, etc.) afin de recevoir les mises à jour de sécurité importantes.

En outre, certaines distributions ne téléchargent pas automatiquement les mises à jour du micrologiciel. Pour cela, vous devez installer [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

### Permission Controls

Desktop environments (DEs) that support the [Wayland](https://wayland.freedesktop.org) display protocol are [more secure](https://lwn.net/Articles/589147) than those that only support X11. However, not all DEs take full advantage of Wayland's architectural security improvements.

For example, GNOME has a notable edge in security compared to other DEs by implementing permission controls for third-party software that tries to [capture your screen](https://gitlab.gnome.org/GNOME/gnome-shell/-/issues/3943). That is, when a third-party application attempts to capture your screen, you are prompted for your permission to share your screen with the app.

<figure markdown>
  ![Screenshot permissions](../assets/img/linux/screenshot_permission.png){ width="450" }
  <figcaption>GNOME's screenshot permission dialog</figcaption>
</figure>

Many alternatives don't provide these same permission controls yet,[^1] while some are waiting for Wayland to implement these controls upstream.[^2]

## Ajustements de confidentialité

### Adresse MAC aléatoire

De nombreuses distributions Linux de bureau (Fedora, openSUSE, etc.) sont livrées avec [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) pour configurer les paramètres Ethernet et Wi-Fi.

Il est possible de [rendre aléatoire](https://fedoramagazine.org/randomize-mac-address-nm) l'[adresse MAC](https://en.wikipedia.org/wiki/MAC_address) lors de l'utilisation de NetworkManager. Cela permet de protéger un peu plus la vie privée sur les réseaux Wi-Fi, car il est plus difficile de suivre des appareils spécifiques sur le réseau auquel vous êtes connecté. Cela ne vous rend [**pas**](https://papers.mathyvanhoef.com/wisec2016.pdf) anonyme.

Nous vous recommandons de changer le paramètre en **aléatoire** au lieu de **stable**, comme suggéré dans l'[article](https://fedoramagazine.org/randomize-mac-address-nm).

Si vous utilisez [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), vous devrez définir [`MACAddressPolicy=random`](https://freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) ce qui activera la [RFC 7844 (Profils d'anonymat pour les clients DHCP)](https://freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

La randomisation des adresses MAC est principalement bénéfique pour les connexions Wi-Fi. Pour les connexions Ethernet, la randomisation de l'adresse MAC ne présente que peu d'avantages (voire aucun), car un administrateur de réseau peut trivialement identifier votre appareil par d'autres moyens (par exemple en inspectant le port auquel vous êtes connecté sur le commutateur du réseau). Rendre aléatoire les adresses MAC Wi-Fi dépend de la prise en charge par le micrologiciel du Wi-Fi.

### Autres identifiants

Il existe d'autres identifiants de système auxquels vous devez faire attention. Vous devriez y réfléchir pour voir si cela s'applique à votre [modèle de menace](../basics/threat-modeling.md) :

- **Noms d'hôte :** Le nom d'hôte de votre système est partagé avec les réseaux auxquels vous vous connectez. Vous devriez éviter d'inclure des termes d'identification comme votre nom ou votre système d'exploitation dans votre nom d'hôte, et vous en tenir plutôt à des termes génériques ou à des chaînes aléatoires.
- **Noms d'utilisateur :** De même, votre nom d'utilisateur est utilisé de diverses manières dans votre système. Envisagez d'utiliser des termes génériques comme "utilisateur" plutôt que votre nom réel.
- **Identifiant machine :** Pendant l'installation, un identifiant machine unique est généré et stocké sur votre appareil. Envisagez de [le régler sur un identifiant générique](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### Comptage des systèmes

Le projet Fedora [compte](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) le nombre de systèmes uniques qui accèdent à ses miroirs en utilisant une variable [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) au lieu d'un identifiant unique. Fedora fait cela pour déterminer la charge et fournir de meilleurs serveurs pour les mises à jour si nécessaire.

Cette [option](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) est actuellement désactivée par défaut. Nous recommandons d'ajouter `countme=false` à `/etc/dnf/dnf.conf` juste au cas où il serait activé dans le futur. On systems that use `rpm-ostree` such as Silverblue, the `countme` option is disabled by masking the [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems) timer.

openSUSE utilise également un [identifiant unique](https://en.opensuse.org/openSUSE:Statistics) pour compter les systèmes, qui peut être désactivé en vidant le fichier `/var/lib/zypp/AnonymousUniqueId`.

[^1]: KDE currently has an open proposal to add controls for screen captures: <https://invent.kde.org/plasma/xdg-desktop-portal-kde/-/issues/7>
[^2]: Sway is waiting to add specific security controls until they "know how security as a whole is going to play out" in Wayland: <https://github.com/swaywm/sway/issues/5118#issuecomment-600054496>
