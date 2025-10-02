---
title: "Bureau/PC"
icon: simple/linux
description: Les distributions Linux sont généralement recommandées pour la protection de la vie privée et la liberté logicielle.
cover: desktop.webp
---

<small>Protège contre la/les menaces suivantes :</small>

- [:material-account-cash: Capitalisme de surveillance](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Les distributions Linux sont généralement recommandées pour la protection de la vie privée et la liberté logicielle. Si vous n'utilisez pas encore Linux, vous trouverez ci-dessous quelques distributions que nous vous suggérons d'essayer, ainsi que des conseils généraux d'amélioration de la sécurité et de la confidentialité qui s'appliquent à de nombreuses distributions Linux.

- [Vue d'ensemble de Linux :material-arrow-right-drop-circle:](os/linux-overview.md)

## Distributions traditionnelles

### Linux Fedora

<div class="admonition recommendation" markdown>

![Logo de Fedora](assets/img/linux-desktop/fedora.svg){ align=right }

Pour les personnes débutant sur Linux, nous recommandons la distribution **Fedora**. Fedora adapte généralement les nouvelles technologies (p. ex. [Wayland](https://wayland.freedesktop.org) et [PireWire](https://pipewire.org)) avant les autres distributions. Ces nouvelles technologies s'accompagnent souvent d'améliorations générales en matière de sécurité, de vie privée et d'ergonomie.

[:octicons-home-16: Page d'accueil](https://fedoraproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs){ .card-link title="Documentation" }
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title="Contribuer" }

</details>

</div>

Les deux éditions principales de Fedora sont [Fedora Workstation](https://fedoraproject.org/workstation), qui utilise l'environnement de bureau GNOME, et [Fedora KDE Plasma Desktop](https://fedoraproject.org/kde), qui utilise KDE. Fedora Workstation est historiquement l'édition la plus populaire, mais KDE gagne de plus en plus en popularité et propose une expérience plus proche de Windows, ce qui peut faciliter la transition vers Linux pour certaines personnes. Les avantages en termes de sécurité et de confidentialité des deux éditions sont très similaires, il s'agit donc avant tout de préférence personnelle.

Fedora a un cycle de publication semi-continu. Si certains paquets comme l'environnement de bureau sont bloqués jusqu'à la prochaine version de Fedora, la majorité des paquets (y compris le kernel) sont fréquemment mis à jour. Chaque version de Fedora est supportée pendant un an, avec une nouvelle version publiée tous les 6 mois.

### openSUSE Tumbleweed

<div class="admonition recommendation" markdown>

![logo openSUSE Tumbleweed](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }

**openSUSE Tumbleweed** est une distribution stable à publication continue.

openSUSE Tumbleweed utilise [Btrfs](https://en.wikipedia.org/wiki/Btrfs) and [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) pour s'assurer que le système peut être restauré à une version précédente en cas de problème.

[:octicons-home-16: Page d'accueil](https://get.opensuse.org/tumbleweed){ .md-button .md-button--primary }
[:octicons-info-16:](https://doc.opensuse.org){ .card-link title="Documentation" }
[:octicons-heart-16:](https://shop.opensuse.org){ .card-link title="Contribuer" }

</details>

</div>

Tumbleweed suit un modèle de publication continu où chaque mise à jour est publiée comme un instantané de la distribution. Lorsque vous mettez votre système à niveau, un nouvel instantané est téléchargé. Chaque livraison est soumise à une série de tests automatisés par [openQA](https://openqa.opensuse.org) afin de garantir sa qualité.

### Arch Linux

<div class="admonition recommendation" markdown>

![Arch logo](assets/img/linux-desktop/archlinux.svg){ align=right }

**Arch Linux** est une distribution légère et do-it-yourself (DIY), ce qui veut dire que vous n'obtenez que ce que vous installez. Pour plus d'informations, voir leur [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions_(Fran%C3%A7ais)).

[:octicons-home-16: Page d'accueil](https://archlinux.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.archlinux.org){ .card-link title="Documentation" }
[:octicons-heart-16:](https://archlinux.org/donate){ .card-link title="Contribuer" }

</details>

</div>

Arch Linux a un cycle de publication continue. Il n'y a pas de calendrier de publication fixe et les paquets sont mis à jour très fréquemment.

S'agissant d'une distribution DIY, vous êtes [censé mettre en place et maintenir](os/linux-overview.md#arch-based-distributions) votre système par vous-même. Arch a un [installateur officiel](https://wiki.archlinux.org/title/Archinstall_(Fran%C3%A7ais)) pour rendre le processus d'installation un peu plus facile.

Une grande portion des [packages d'Arch Linux](https://reproducible.archlinux.org) sont [reproducibles](https://reproducible-builds.org)[^1].

## Distributions atomiques

**Les distributions atomiques** (parfois également appelées **distributions immuables**) sont des systèmes d'exploitation qui gèrent l'installation et la mise à jour des paquets en superposant les changements à l'image de base du système, plutôt qu'en modifiant directement le système. Les distributions dites "atomiques" sont plus stables et permettent plus facilement de revenir en arrière sur les mises à jour. Voir [*Mises à jour traditionnelles vs. atomiques*](os/linux-overview.md#traditional-vs-atomic-updates) pour plus d'informations.

### Fedora Atomic Desktops

<div class="admonition recommendation" markdown>

![Logo Fedora](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Atomic Desktops** sont des variantes de Fedora qui utilisent le gestionnaire de paquets `rpm-ostree` et qui sont fortement axées sur les flux de travail conteneurisés et Flatpak pour les applications de bureau. Toutes ces variantes suivent le même calendrier de publication que Fedora Workstation, bénéficiant des mêmes mises à jour rapides et restant très proches de l'original.

[:octicons-home-16: Pafe d'accueil](https://fedoraproject.org/atomic-desktops){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/emerging){ .card-link title="Documentation" }
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title="Contribuer" }

</details>

</div>

[Fedora Atomic Desktops](https://fedoramagazine.org/introducing-fedora-atomic-desktops) est disponible en plusieurs saveurs différentes, selon l'environnement de bureau que vous préférez. Comme pour notre recommandation d'éviter X11 dans nos [critères](#criteria) pour les distributions Linux, nous recommandons également d'éviter les saveurs qui ne prennent en charge que l'ancien système de fenêtre X11.

Contrairement à Fedora Workstation qui utilise le gestionnaire paquet [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf), ces systèmes d'exploitation utilisent une version alternative beaucoup plus avancée appelée [`rpm-ostree`](https://coreos.github.io/rpm-ostree). Le gestionnaire de paquets `rpm-ostree` fonctionne en téléchargeant une image de base pour le système, puis en superposant des paquets par-dessus dans une arborescence de commits semblable à [git](https://en.wikipedia.org/wiki/Git). Lorsque le système est mis à jour, une nouvelle image de base est téléchargée et les surcouches seront appliquées à cette nouvelle image.

Une fois la mise à jour terminée, le système redémarrera selon le nouveau déploiement. `rpm-ostree` conserve deux déploiements du système pour pouvoir revenir en arrière en cas de problème. Il est également possible d'épingler plus de déploiements selon les besoins.

[Flatpak](https://flatpak.org) est la méthode principale d'installation des paquets sur ces distributions, car `rpm-ostree` n'est destiné qu'à superposer les paquets qui ne peuvent pas rester à l'intérieur d'un conteneur sur l'image de base.

A la place des Flatpaks, il est possible d'utiliser [Toolbx](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox) pour créer des conteneurs [Podman](https://podman.io) qui imitent un environnement Fedora traditionnel, une [fonctionnalité intéressante](https://containertoolbx.org) pour les développeurs avertis. Ces conteneurs partagent un répertoire personnel avec le système hôte.

### NixOS

<div class="admonition recommendation" markdown>

![Logo NixOS](assets/img/linux-desktop/nixos.svg){ align=right }

NixOS est une distribution indépendante basée sur le gestionnaire de paquets Nix avec un accent sur la reproductibilité et la fiabilité.

[:octicons-home-16: Page d'accueil](https://nixos.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://nixos.org/learn.html){ .card-link title="Documentation" }
[:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title="Contribuer" }

</details>

</div>

Le gestionnaire de paquets de NixOS conserve chaque version de chaque paquet dans un dossier différent dans le **magasin Nix**. De ce fait, vous pouvez avoir différentes versions d'un même paquet installé sur votre système. Une fois que le contenu du paquet a été écrit dans le dossier, ce dernier est mis en lecture seule.

Des mises à jour atomiques sont également disponible avec NixOS. En premier lieu NixOS télécharge (ou "build") les paquets et les fichiers pour la génération du nouveau système, puis il bascule dessus. Il existe différentes manières de basculer vers une nouvelle génération : soit au redémarrage, soit au moment de l'exécution. Vous pouvez également *tester* la nouvelle génération en basculant sur celle-ci pendant l'exécution, mais sans la définir comme la génération actuelle du système. Si quelque chose se casse pendant le processus de mise à jour, vous pouvez simplement redémarrer et revenir automatiquement à une version fonctionnelle de votre système.

Le gestionnaire de paquet Nix utilise un langage purement fonctionne (lui aussi appelé Nix) pour définir les paquets.

[Nixpkgs](https://github.com/nixos/nixpkgs) (la source principale des paquets) sont contenus dans un seul dépôt GitHub. Vous pouvez également définir vos propres paquets dans le même langage, puis les inclure facilement dans votre configuration.

Nix est un gestionnaire de paquets basé sur les sources ; s'il n'y a pas de paquet pré-construit disponible dans le cache binaire, Nix construira simplement le paquet à partir des sources en utilisant sa définition. Chaque paquet est contruit dans un environnement sandboxé *pur*, qui est aussi indépendant que possible du système hôte. Les exécutables construits avec cette méthode sont reproductibles [^1].

## Distributions axées sur l'anonymat

### Whonix

<div class="admonition recommendation" markdown>

![logo Whonix](assets/img/linux-desktop/whonix.svg){ align=right }

**Whonix** est basée sur [Kicksecure](#kicksecure), une version de Debian axée sur la sécurité. Le but est d'améliorer la confidentialité, la sécurité et [:material-incognito: l'Anonymat](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } sur internet. Whonix est utilisé de préférence en conjonction avec [Qubes OS](#qubes-os).

[:octicons-home-16: Page d'accueil](https://whonix.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Service Onion" }
[:octicons-info-16:](https://whonix.org/wiki/Documentation){ .card-link title="Documentation" }
[:octicons-heart-16:](https://whonix.org/wiki/Donate){ .card-link title="Contribuer" }

</details>

</div>

Whonix est conçu pour fonctionner sous la forme de deux machines virtuelles : une "Station de travail" et une "Passerelle" Tor. Toutes les communications de la Station de travail doivent passer par la passerelle Tor. Cela signifie que même si la Station de travail est compromise par un logiciel malveillant quelconque, la véritable adresse IP reste cachée.

Parmis ses fonctionnalités, on peut retrouver Tor Stream Isolation, [l'anonymisation des dynamiques de frappe au clavier](https://whonix.org/wiki/Keystroke_Deanonymization#Kloak), [le chiffrement des fichiers swap](https://github.com/Whonix/swap-file-creator), et un allocateur de mémoire renforcé. Les futures versions de Whonix incluront probablement [des politiques système AppArmor](https://github.com/roddhjav/apparmor.d) et un [lanceur d'applications sandboxé](https://whonix.org/wiki/Sandbox-app-launcher) afin de confiner complètement tous les process du système.

Whonix est utilisé de préférence [en complément avec Qubes](https://whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers). Nous avons un [guide recommandé](os/qubes-overview.md#connecting-to-tor-via-a-vpn) sur la configuration de Whonix en conjonction avec un VPN ProxyVM dans Qubes pour cacher vos activités Tor à votre FAI.

### Tails

<div class="admonition recommendation" markdown>

![Logo de Tails](assets/img/linux-desktop/tails.svg){ align=right }

**Tails** est un système d'exploitation autonome basé sur Debian qui fait passer toutes les communications par Tor, et qui peut démarrer sur presque n'importe quel ordinateur à partir d'un DVD, d'une clé USB ou d'une installation sur carte SD. [Tor](tor.md) est utilisé pour renforcer la confidentialité et [:material-incognito: l'Anonymat](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } tout en contournant la censure. Tails ne laisse aucune trace sur l'ordinateur sur lequel il a été utilisé après avoir été éteint.

[:octicons-home-16: Page d'accueil](https://tails.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://tails.net/doc/index.en.html){ .card-link title="Documentation" }
[:octicons-heart-16:](https://tails.net/donate){ .card-link title="Contribuer" }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Tails [n'efface pas](https://gitlab.tails.boum.org/tails/tails/-/issues/5356) la [mémoire vidéo](https://en.wikipedia.org/wiki/Dual-ported_video_RAM) lors de l'arrêt. Lorsque vous redémarrez votre ordinateur après avoir utilisé Tails, il se peut qu'il affiche brièvement le dernier écran affiché dans Tails. Si vous éteignez votre ordinateur au lieu de le redémarrer, la mémoire vidéo s'effacera automatiquement après un certain temps d'inactivité.

</div>

Tails est excellent pour la contre-analyse en raison de son amnésie (ce qui signifie que rien n'est écrit sur le disque) ; cependant, ce n'est pas une distribution renforcée comme Whonix. Elle ne dispose pas de nombreuses fonctions d'anonymat et de sécurité comme Whonix et est mise à jour beaucoup moins souvent (seulement une fois toutes les six semaines). Un système Tails compromis par un logiciel malveillant peut potentiellement contourner le proxy transparent, et ainsi désanonymiser l'utilisateur.

Sur Tails, [uBlock Origin](browser-extensions.md#ublock-origin) est installé par défaut dans le navigateur Tor, ce qui peut potentiellement faciliter le fingerprinting des utilisateurs Tails Les machines virtuelles [Whonix](desktop.md#whonix) sont peut-être plus étanches, mais elles ne sont pas amnésiques, ce qui signifie que les données peuvent être récupérées sur votre périphérique de stockage.

De par sa conception, Tails est censé se réinitialiser complètement après chaque redémarrage. Un [stockage persistant](https://tails.net/doc/persistent_storage/index.en.html) chiffré peut être paramétré pour conserver certaines données entre les redémarrages.

## Distributions axées sur la sécurité

<small>Protège contre les menaces suivantes :</small>

- [:material-bug-outline: Attaques passives](basics/common-threats.md#security-and-privacy ""){.pg-orange}

### Qubes OS

<div class="admonition recommendation" markdown>

![logo Qubes OS](assets/img/qubes/qubes_os.svg){ align=right }

**Qubes OS** est un système d'exploitation open-source conçu pour fournir une sécurité forte pour l'informatique de bureau à travers des machines virtuelles sécurisées (ou "qubes"). Qubes est basé sur Xen, le système de fenêtre X, et Linux. Il peut exécuter la plupart des applications Linux et utiliser la plupart des pilotes Linux.

[:octicons-home-16: Page d'accueil](https://qubes-os.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Service Onion" }
[:octicons-eye-16:](https://qubes-os.org/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://qubes-os.org/doc){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/QubesOS){ .card-link title="Code Source" }
[:octicons-heart-16:](https://qubes-os.org/donate){ .card-link title="Contribuer" }

</details>

</div>

Qubes OS sécurise l'ordinateur en isolant les sous-systèmes (par exemple, le réseau, l'USB, etc.) et les applications dans des *qubes* distincts. Si une partie du système est compromise par une [:material-target-account: Attaque Ciblée](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}, l'isolation supplémentaire protègera probablement le reste des *qubes* et le système central.

Pour plus d'informations sur le fonctionnement de Qubes, lisez notre page [Introduction à Qubes](os/qubes-overview.md).

### Secureblue

<div class="admonition recommendation" markdown>

![Logo de Secureblue](assets/img/linux-desktop/secureblue.svg){ align=right }

**Secureblue** est un système d'exploitation orienté sur la sécurité basé sur les [Fedora Atomic Desktops](#fedora-atomic-desktops). Ses nombreuses [fonctionnalités de sécurité](https://secureblue.dev/features) ont pour but de défendre le système de façon proactive contre les menaces connues et inconnues et le système inclu également leur navigateur web renforcé basé sur Chromium, [Trivalent](https://github.com/secureblue/Trivalent).

[:octicons-home-16: Page d'accueil](https://secureblue.dev){ .md-button .md-button--primary }
[:octicons-info-16:](https://secureblue.dev/install){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/secureblue/secureblue){ .card-link title="Code Source" }
[:octicons-heart-16:](https://secureblue.dev/donate){ .card-link title="Contribuer" }

</div>

**Trivalent**, le navigateur web renforcé de Secureblue, est inspiré du navigateur Vanadium, développé par [GrapheneOS](android/distributions.md#grapheneos).

Secureblue comprend également [l'allocateur de mémoire renforcé](https://github.com/GrapheneOS/hardened_malloc) de GrapheneOS, activé au niveau global (y compris pour les Flatpaks).

### Kicksecure

Bien que nous recommandions généralement [d'éviter](os/linux-overview.md#release-cycle) les distributions Linux "perpétuellement obsolètes" comme Debian pour une utilisation de bureau, Kicksecure est un système d'exploitation basé sur Debian renforcé pour être bien plus qu'une installation Linux classique.

<div class="admonition recommendation" markdown>

![Logo Kicksecure](assets/img/linux-desktop/kicksecure.svg){ align=right }

**Kicksecure** - en termes simplifiés à l'extrême - est un ensemble de scripts, de configurations et de paquets qui réduisent considérablement la surface d'attaque de Debian. Il couvre par défaut un grand nombre de recommandations en matière de confidentialité et de durcissement. Il sert également de système d'exploitation de base pour [Whonix](#whonix).

[:octicons-home-16: Page d'accueil](https://kicksecure.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kicksecure.com/wiki/Privacy_Policy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://kicksecure.com/wiki/Documentation){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Code Source" }
[:octicons-heart-16:](https://kicksecure.com/wiki/Donate){ .card-link title="Contribuer" }

</details>

</div>

## Critères

Le choix d'une distribution Linux qui vous convient dépend d'une grande variété de préférences personnelles, et cette page n'est **pas** une liste exhaustive de toutes les distributions viables. Notre page d'introduction à Linux contient des conseils plus détaillés sur [le choix d'une distribution](os/linux-overview.md#choosing-your-distribution). Les distributions sur *cette* page suivent généralement les lignes directrices que nous avons abordées là-bas, et respectent toutes ces normes :

- Gratuites et open source.
- Reçoivent régulièrement des mises à jour des logiciels et du noyau.
- Evite X11, dont la dernière version importante date de plus de [dix ans](https://x.org/wiki/Releases).
    - Qubes est ici une exception notable, mais la virtualisation permet d'éviter les [problèmes d'isolement](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation) généralement rencontrés avec X11. Cet isolement s'applique uniquement aux applications *exécutées dans différents qubes* (machines virtuelles) ; les applications exécutées dans un *même* qube ne sont pas protégées les unes des autres.
- Prennent en charge le chiffrement complet du disque pendant l'installation.
- Ne gêlent pas les mises à jour régulières pendant plus d'un an.
    - Nous [ne recommandons pas](os/linux-overview.md#release-cycle) les versions "Long Term Support" ou "stables" de distributions pour une utilisation de bureau.
- Prennent en charge une grande variété de matériel.
- Préférence pour les projets de plus grande envergure.
    - La maintenance d'un système d'exploitation est un défi majeur, et les petits projets ont tendance à faire plus d'erreurs évitables ou à retarder les mises à jour critiques (ou pire, à disparaître complètement). Nous privilégions les projets qui seront probablement toujours présents dans 10 ans (que ce soit grâce au soutien d'une entreprise ou à un soutien communautaire très important), et nous évitons les projets qui sont construits de zéro ou qui ont un petit nombre de mainteneurs.

En outre, [nos critères standards](about/criteria.md) pour les projets recommandés s'appliquent toujours. **Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.**

[^1]: La reproductibilité permet de vérifier que les paquets et les exécutables mis à disposition de l'utilisateur correspondent au code source, ce qui peut s'avérer utile en cas d' [:material-package-variant-closed-remove: Attaque de la Chaine d'Approvisionnement](basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}.
