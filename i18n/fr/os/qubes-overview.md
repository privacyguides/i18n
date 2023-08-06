---
title: "Introduction à Qubes"
icon: simple/qubesos
description: Qubes est un système d'exploitation conçu pour isoler les applications au sein de *qubes* (anciennement "VMs") afin d'améliorer la sécurité.
---

[**Qubes OS**](../desktop.md#qubes-os) est un système d'exploitation open source qui utilise l'hyperviseur [Xen](https://fr.wikipedia.org/wiki/Xen) pour fournir une sécurité forte pour l'informatique de bureau par le biais de *qubes* isolés (qui sont des machines virtuelles). Vous pouvez attribuer à chaque *qube* un niveau de confiance en fonction de son objectif. Qubes OS assure la sécurité en utilisant l'isolation. Il n'autorise les actions qu'au cas par cas et est donc à l'opposé de [l'énumération de méchanceté](https://www.ranum.com/security/computer_security/editorials/dumb/).

## Comment fonctionne Qubes OS ?

Les qubes utilisent la [compartimentation](https://www.qubes-os.org/intro/) pour assurer la sécurité du système. Les Qubes sont créés à partir de modèles, ceux par défaut étant pour Fedora, Debian et [Whonix](../desktop.md#whonix). Qubes OS vous permet également de créer des *qubes* à usage unique [jetables](https://www.qubes-os.org/doc/how-to-use-disposables/).

??? "Le terme *qubes* est progressivement mis à jour pour éviter d'y faire référence en tant que "machines virtuelles"."

    Certaines des informations présentées ici et dans la documentation du système d'exploitation Qubes OS peuvent être contradictoires, car le terme "appVM" est progressivement remplacé par "qube". Les qubes ne sont pas des machines virtuelles à part entière, mais ils conservent des fonctionnalités similaires à celles des VMs.

![Architecture de Qubes](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Architecture de Qubes, Crédit : Intro de Qu'est-ce que Qubes OS</figcaption>

Chaque qube a une [bordure colorée](https://www.qubes-os.org/screenshots/) qui peut vous aider à repérer le domaine dans lequel il s'exécute. Vous pouvez, par exemple, utiliser une couleur spécifique pour votre navigateur bancaire, tout en utilisant une couleur différente pour un navigateur général non fiable.

![Bordure colorée](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Bordures de fenêtres de Qubes, Crédit : Captures d'écran Qubes</figcaption>

## Pourquoi devrais-je utiliser Qubes ?

Qubes OS est utile si votre [modèle de menace](../basics/threat-modeling.md) exige une sécurité et une isolation fortes, par exemple si vous pensez ouvrir des fichiers non fiables provenant de sources non fiables. Une raison typique d'utiliser Qubes OS est d'ouvrir des documents provenant de sources inconnues, mais l'idée est que si un seul qube est compromis, cela n'affectera pas le reste du système.

Qubes OS utilise une VM Web [dom0](https://wiki.xenproject.org/wiki/Dom0) pour contrôler d'autres *qubes* sur l'OS hôte, qui affichent tous des fenêtres d'application individuelles dans l'environnement de bureau de dom0. Les utilisations de ce type d'architecture sont multiples. Voici quelques tâches que vous pouvez effectuer. Vous pouvez constater à quel point ces processus sont sécurisés par l'incorporation de plusieurs étapes.

### Copier et coller du texte

Vous pouvez [copier et coller du texte](https://www.qubes-os.org/doc/how-to-copy-and-paste-text/) en utilisant `qvm-copy-to-vm` ou les instructions ci-dessous :

1. Appuyez sur **Ctrl+C** pour indiquer au *qube* dans lequel vous vous trouvez que vous souhaitez copier quelque chose.
2. Appuyez sur **Ctrl+Maj+C** pour demander au *qube* de mettre ce tampon à la disposition du presse-papiers global.
3. Appuyez sur **Ctrl+Maj+V** dans le *qube* de destination pour rendre le presse-papiers global disponible.
4. Appuyez sur **Ctrl+V** dans lr *qube* de destination pour coller le contenu dans le tampon.

### Échange de fichiers

Pour copier et coller des fichiers et des répertoires (dossiers) d'un *qube* à un autre, vous pouvez utiliser l'option **Copier vers une autre AppVM...** ou **Déplacer vers une autre AppVM...**. La différence est que l'option **Déplacer** supprime le fichier d'origine. L'une ou l'autre option protégera votre presse-papiers contre les fuites vers d'autres *qubes*. Cette méthode est plus sûre que le transfert de fichiers air-gap. Un ordinateur air-gap sera toujours obligé d'analyser les partitions ou les systèmes de fichiers. Cela n'est pas nécessaire avec le système de copie inter-qube.

??? "Les Qubes n'ont pas leur propre système de fichiers."

    Vous pouvez [copier et déplacer des fichiers] (https://www.qubes-os.org/doc/how-to-copy-and-move-files/) entre *qubes*. Ce faisant, les changements ne sont pas immédiats et peuvent être facilement annulés en cas d'accident. When you run a *qube*, it does not have a persistent filesystem. You can create and delete files, but these changes are ephemeral.

### Interactions inter-VM

The [qrexec framework](https://www.qubes-os.org/doc/qrexec/) is a core part of Qubes which allows communication between domains. Il est construit sur la bibliothèque Xen *vchan*, qui facilite [l'isolation de par le biais de politiques](https://www.qubes-os.org/news/2020/06/22/new-qrexec-policy-system/).

## Ressources supplémentaires

Pour de plus amples informations, nous vous encourageons à consulter les pages de documentation complètes de Qubes OS, situées sur le [site web de Qubes OS](https://www.qubes-os.org/doc/). Des copies hors ligne peuvent être téléchargées à partir du [dépôt de documentationde](https://github.com/QubesOS/qubes-doc) Qubes OS.

- [Sans doute le système d'exploitation le plus sûr au monde](https://www.opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard/) (Open Technology Fund)
- [Comparaison entre le cloisonnement des logiciels et la séparation physique](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf) (J. Rutkowska)
- [Partitionner ma vie numérique en domaines de sécurité](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html) (J. Rutkowska)
- [Related Articles](https://www.qubes-os.org/news/categories/#articles) (Qubes OS)
