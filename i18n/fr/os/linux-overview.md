---
title: Introduction à Linux
icon: simple/linux
description: Linux est un système d'exploitation de bureau alternatif open source, axé sur la protection de la vie privée, mais toutes les distributions ne sont pas créées égales.
---

**Linux** est un système d'exploitation de bureau alternatif, open-source et axé sur la protection de la vie privée. Face à l'omniprésence de la télémétrie et d'autres technologies portant atteinte à la vie privée dans les systèmes d'exploitation courants, Linux est resté le choix le plus évident pour les personnes désireuses de contrôler totalement leur ordinateur de zéro.

Our website generally uses the term “Linux” to describe **desktop** Linux distributions. Other operating systems which also use the Linux kernel such as ChromeOS, Android, and Qubes OS are not discussed on this page.

[Nos recommandations Linux :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Remarques concernant la vie privée

There are some notable privacy concerns with Linux which you should be aware of. Despite these drawbacks, desktop Linux distributions are still great for most people who want to:

- Évitez la télémétrie qui accompagne souvent les systèmes d'exploitation propriétaires
- Maintenir [la liberté des logiciels](https://www.gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Use privacy focused systems such as [Whonix](https://www.whonix.org) or [Tails](https://tails.boum.org/)

### Open Source Security

It is a [common misconception](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) that Linux and other open-source software is inherently secure simply because the source code is available. There is an expectation that community verification occurs regularly, but this isn’t always [the case](https://seirdy.one/posts/2022/02/02/floss-security/).

In reality, distro security depends on a number of factors, such as project activity, developer experience, the level of rigor applied to code reviews, and how often attention is given to specific parts of the codebase that may go untouched for years.

### Missing Security Features

At the moment, desktop Linux [falls behind alternatives](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) like macOS or Android when it comes to certain security features. We hope to see improvements in these areas in the future.

- **Verified boot** on Linux is not as robust as alternatives such as Apple’s [Secure Boot](https://support.apple.com/guide/security/secac71d5623/web) or Android’s [Verified Boot](https://source.android.com/security/verifiedboot). Verified boot prevents persistent tampering by malware and [evil maid attacks](https://en.wikipedia.org/wiki/Evil_Maid_attack), but is still largely [unavailable on even the most advanced distributions](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- **Strong sandboxing** for apps on Linux is severely lacking, even with containerized apps like Flatpaks or sandboxing solutions like Firejail. Flatpak is the most promising sandboxing utility for Linux thus far, but is still deficient in many areas and allows for [unsafe defaults](https://flatkill.org/2020/) which allow most apps to trivially bypass their sandbox.

Additionally, Linux falls behind in implementing [exploit mitigations](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) which are now standard on other operating systems, such as Arbitrary Code Guard on Windows or Hardened Runtime on macOS. Also, most Linux programs and Linux itself are coded in memory-unsafe languages. Memory corruption bugs are responsible for the [majority of vulnerabilities](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code/) fixed and assigned a CVE. While this is also true for Windows and macOS, they are quickly making progress on adopting memory-safe languages—such as Rust and Swift, respectively—while there is no similar effort to rewrite Linux in a memory-safe language like Rust.

## Choisir sa distribution

Toutes les distributions Linux ne sont pas créées égales. Our [Linux recommendation page](../desktop.md) is not meant to be an authoritative source on which distribution you should use, but our recommendations *are* aligned with the following guidelines. These are a few things you should keep in mind when choosing a distribution:

### Cycle de mises à jour

Nous vous recommandons vivement de choisir des distributions qui restent proches des versions stables des logiciels en amont, souvent appelées distributions à publications continues. En effet, les distributions à cycle de publication gelé ne mettent souvent pas à jour les versions des paquets et prennent du retard sur les mises à jour de sécurité.

Pour les distributions gelées telles que [Debian](https://www.debian.org/security/faq#handling), les responsables de paquets sont censés rapporter les correctifs pour corriger les vulnérabilités plutôt que de faire passer le logiciel à la "prochaine version" publiée par le développeur en amont. Some security fixes [do not](https://arxiv.org/abs/2105.14565) receive a [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) (particularly less popular software) at all and therefore do not make it into the distribution with this patching model. Par conséquent, les corrections de sécurité mineures sont parfois reportées à la prochaine version majeure.

Nous ne pensons pas que retenir les paquets et appliquer des correctifs provisoires soit une bonne idée, car cela s'écarte de la manière dont le développeur aurait pu vouloir que le logiciel fonctionne. [Richard Brown](https://rootco.de/aboutme/) propose une présentation à ce sujet :

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/i8c0mg_mS7U?local=true" title="Les publications régulières sont une erreur, les publications continues c'est la vie" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Mises à jour traditionnelles et atomiques

Traditionnellement, les distributions Linux se mettent à jour en mettant séquentiellement à jour les paquets souhaités. Les mises à jour traditionnelles, telles que celles utilisées dans les distributions basées sur Fedora, Arch Linux et Debian, peuvent être moins fiables si une erreur se produit lors de la mise à jour.

Les distributions à mises à jour atomiques appliquent les mises à jour dans leur intégralité ou pas du tout. En général, les systèmes de mise à jour transactionnelle sont également atomiques.

Un système de mise à jour transactionnelle crée un instantané qui est réalisé avant et après l'application d'une mise à jour. Si une mise à jour échoue à un moment donné (par exemple en raison d'une panne de courant), elle peut facilement être ramenée au "dernier état correct connu."

La méthode de mise à jour atomique est utilisée pour les distributions immuables comme Silverblue, Tumbleweed et NixOS et permet d'atteindre la fiabilité avec ce modèle. [Adam Šamalík](https://twitter.com/adsamalik) a fait une présentation sur le fonctionnement de `rpm-ostree` avec Silverblue :

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/-hpV5l-gJnQ?local=true" title="Essayons Fedora Silverblue — un OS de bureau immuable ! - Adam Šamalik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### "Distributions "axées sur la sécurité

Il y a souvent une certaine confusion entre les distributions "axées sur la sécurité" et les distributions pour les "tests de pénétration". A quick search for “the most secure Linux distribution” will often give results like Kali Linux, Black Arch, or Parrot OS. Ces distributions sont des distributions de tests de pénétration offensifs qui regroupent des outils pour tester d'autres systèmes. Elles n'incluent pas de "sécurité supplémentaire" ni de mesures d'atténuation défensives destinées à une utilisation régulière.

### Distributions basées sur Arch Linux

Arch and Arch-based distributions are not recommended for those new to Linux (regardless of distribution) as they require regular [system maintenance](https://wiki.archlinux.org/title/System_maintenance). Arch does not have a distribution update mechanism for the underlying software choices. Par conséquent, vous devez rester au courant des tendances actuelles et adopter les technologies au fur et à mesure qu'elles remplacent les anciennes pratiques.

Pour un système sécurisé, vous êtes également censé avoir une connaissance suffisante de Linux pour configurer correctement la sécurité de votre système, par exemple en adoptant un système de [contrôle d'accès obligatoire](https://en.wikipedia.org/wiki/Mandatory_access_control), en configurant des listes noires de [modules du noyau](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security), en renforçant les paramètres de démarrage, en manipulant les paramètres [sysctl](https://en.wikipedia.org/wiki/Sysctl), et en sachant de quels composants ils ont besoin, comme [Polkit](https://en.wikipedia.org/wiki/Polkit).

Anyone using the [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **must** be comfortable auditing PKGBUILDs that they download from that service. Les paquets AUR sont des contenus produits par la communauté et ne font l'objet d'aucune vérification. Ils sont donc vulnérables aux attaques de la chaîne d'approvisionnement des logiciels, ce qui s'est d'ailleurs produit [dans le passé](https://www.bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository/).

The AUR should always be used sparingly, and often there is a lot of bad advice on various pages which direct people to blindly use [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) without sufficient warning. Des avertissements similaires s'appliquent à l'utilisation d'Archives de Paquets Personnels (PPA) de tiers sur les distributions basées sur Debian ou de Projets Communautaires (COPR) sur Fedora.

If you are experienced with Linux and wish to use an Arch-based distribution, we generally recommend mainline Arch Linux over any of its derivatives.

Additionally, we recommend **against** these two Arch derivatives specifically:

- **Manjaro**: Cette distribution bloque les mises à jour des paquets pendant 2 semaines pour s'assurer que leurs propres changements ne cassent pas, et non pas pour s'assurer que l'amont est stable. Lorsque des paquets AUR sont utilisés, ils sont souvent construits avec les dernières [bibliothèques](https://en.wikipedia.org/wiki/Library_(computing)) des dépôts d'Arch.
- **Garuda**: Ils utilisent [Chaotic-AUR](https://aur.chaotic.cx/) qui compile automatiquement et aveuglément les paquets de l'AUR. Il n'existe aucun processus de vérification pour s'assurer que les paquets AUR ne souffrent pas d'attaques de la chaîne d'approvisionnement.

### Le noyau Linux-libre et les distributions "libres"

We recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://www.phoronix.com/news/GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode.

## Recommandations générales

### Chiffrement de disque

La plupart des distributions Linux ont une option dans leur installateur pour activer [LUKS](../encryption.md#linux-unified-key-setup) FDE. Si cette option n'est pas définie au moment de l'installation, vous devrez sauvegarder vos données et réinstaller, car le chiffrement est appliqué après le [partitionnement du disque](https://en.wikipedia.org/wiki/Disk_partitioning), mais avant le formatage des [systèmes de fichiers](https://en.wikipedia.org/wiki/File_system). Nous vous suggérons également d'effacer de façon sécurisée votre dispositif de stockage :

- [Effacement sécurisé des données :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure/)

### Swap

Consider using [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) instead of a traditional swap file or partition to avoid writing potentially sensitive memory data to persistent storage (and improve performance). Fedora-based distributions [use ZRAM by default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

If you require suspend-to-disk (hibernation) functionality, you will still need to use a traditional swap file or partition. Make sure that any swap space you do have on a persistent storage device is [encrypted](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) at a minimum to mitigate some of these threats.

### Wayland

We recommend using a desktop environment that supports the [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)) display protocol, as it was developed with security [in mind](https://lwn.net/Articles/589147/). Its predecessor ([X11](https://en.wikipedia.org/wiki/X_Window_System)) does not support GUI isolation, which allows any window to [record, log, and inject inputs in other windows](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), making any attempt at sandboxing futile. While there are options to do nested X11 such as [Xpra](https://en.wikipedia.org/wiki/Xpra) or [Xephyr](https://en.wikipedia.org/wiki/Xephyr), they often come with negative performance consequences, and are neither convenient to set up nor preferable over Wayland.

Heureusement, des environnements courants tels que [GNOME](https://www.gnome.org), [KDE](https://kde.org), et le gestionnaire de fenêtres [Sway](https://swaywm.org) prennent en charge Wayland. Certaines distributions comme Fedora et Tumbleweed l'utilisent par défaut, et d'autres pourraient le faire à l'avenir car X11 est en [mode maintenance limitée](https://www.phoronix.com/news/X.Org-Maintenance-Mode-Quickly). Si vous utilisez l'un de ces environnements, il vous suffit de sélectionner la session "Wayland" dans le gestionnaire d'affichage du bureau ([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)).

Nous recommandons **de ne pas** utiliser des environnements de bureau ou des gestionnaires de fenêtres qui ne prennent pas en charge Wayland, comme Cinnamon (par défaut sur Linux Mint), Pantheon (par défaut sur Elementary OS), MATE, Xfce et i3.

### Micrologiciel propriétaire (mises à jour du microcode)

Some Linux distributions (such as [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)-based or DIY distros) don’t come with the proprietary [microcode](https://en.wikipedia.org/wiki/Microcode) updates which patch critical security vulnerabilities. Voici quelques exemples notables de ces vulnérabilités : [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), et d'autres [vulnérabilités matérielles](https://www.kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

We **highly recommend** that you install microcode updates, as they contain important security patches for the CPU which can not be fully mitigated in software alone. Fedora et openSUSE ont tous deux les mises à jour du microcode appliquées par défaut.

### Mises à jour

La plupart des distributions Linux installent automatiquement les mises à jour ou vous rappellent de le faire. Il est important de maintenir votre système d'exploitation à jour afin que votre logiciel soit corrigé lorsqu'une vulnérabilité est découverte.

Some distributions (particularly those aimed at advanced users) are more bare bones and expect you to do things yourself (e.g. Arch or Debian). Il faudra manuellement exécuter le "gestionnaire de paquets" (`apt`, `pacman`, `dnf`, etc.) afin de recevoir les mises à jour de sécurité importantes.

En outre, certaines distributions ne téléchargent pas automatiquement les mises à jour du micrologiciel. Pour cela, vous devrez installer [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

## Ajustements de confidentialité

### Adresse MAC aléatoire

Many desktop Linux distributions (Fedora, openSUSE, etc.) come with [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) to configure Ethernet and Wi-Fi settings.

Il est possible de [changer aléatoirement](https://fedoramagazine.org/randomize-mac-address-nm/) l'[adresse MAC](https://en.wikipedia.org/wiki/MAC_address) en utilisant NetworkManager. Cela permet de protéger un peu plus la vie privée sur les réseaux Wi-Fi, car il est plus difficile de suivre des appareils spécifiques sur le réseau auquel vous êtes connecté. Cela ne vous rend [**pas**](https://papers.mathyvanhoef.com/wisec2016.pdf) anonyme.

Nous recommandons de changer le paramètre et mettre **aléatoire** plutôt que **stable**, comme suggéré dans l'[article](https://fedoramagazine.org/randomize-mac-address-nm/).

Si vous utilisez [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), vous devrez définir [`MACAddressPolicy=random`](https://www.freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) qui activera [RFC 7844 (Profils d'anonymat pour les clients DHCP)](https://www.freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

MAC address randomization is primarily beneficial for Wi-Fi connections. For Ethernet connections, randomizing your MAC address provides little (if any) benefit, because a network administrator can trivially identify your device by other means (such as inspecting the port you are connected to on the network switch). Rendre aléatoire les adresses MAC Wi-Fi dépend de la prise en charge par le micrologiciel du Wi-Fi.

### Autres identifiants

Il existe d'autres identifiants de système auxquels vous devez faire attention. Vous devriez y réfléchir pour voir si cela s'applique à votre [modèle de menace](../basics/threat-modeling.md) :

- **Noms d'hôte :** Le nom d'hôte de votre système est partagé avec les réseaux auxquels vous vous connectez. Vous devriez éviter d'inclure des termes d'identification comme votre nom ou votre système d'exploitation dans votre nom d'hôte, et vous en tenir plutôt à des termes génériques ou à des chaînes aléatoires.
- **Noms d'utilisateur :** De même, votre nom d'utilisateur est utilisé de diverses manières dans votre système. Envisagez d'utiliser des termes génériques comme "utilisateur" plutôt que votre nom réel.
- **Identifiant machine :**: Pendant l'installation, un identifiant machine unique est généré et stocké sur votre appareil. Envisagez de [le régler sur un identifiant générique](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### Comptage des systèmes

Le projet Fedora [compte](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) le nombre de systèmes uniques qui accèdent à ses miroirs en utilisant une variable [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) au lieu d'un identifiant unique. Fedora fait cela pour déterminer la charge et fournir de meilleurs serveurs pour les mises à jour si nécessaire.

Cette [option](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) est actuellement désactivée par défaut. Nous recommandons d'ajouter `countme=false` à `/etc/dnf/dnf.conf` juste au cas où il serait activé dans le futur. Sur les systèmes qui utilisent `rpm-ostree` tels que Silverblue, l'option countme est désactivée en masquant le compteur [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems/).

openSUSE utilise également un [identifiant unique](https://en.opensuse.org/openSUSE:Statistics) pour compter les systèmes, qui peut être désactivé en supprimant le fichier `/var/lib/zypp/AnonymousUniqueId`.
