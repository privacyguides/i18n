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

Qubes OS utilizes [dom0](https://wiki.xenproject.org/wiki/Dom0) Xen VM for controlling other *qubes* on the host OS, all of which display individual application windows within dom0's desktop environment. There are many uses for this type of architecture. Here are some tasks you can perform. You can see just how much more secure these processes are made by incorporating multiple steps.

### Copier et coller du texte

Vous pouvez [copier et coller du texte](https://www.qubes-os.org/doc/how-to-copy-and-paste-text/) en utilisant `qvm-copy-to-vm` ou les instructions ci-dessous :

1. Press **Ctrl+C** to tell the *qube* you're in that you want to copy something.
2. Press **Ctrl+Shift+C** to tell the *qube* to make this buffer available to the global clipboard.
3. Press **Ctrl+Shift+V** in the destination *qube* to make the global clipboard available.
4. Press **Ctrl+V** in the destination *qube* to paste the contents in the buffer.

### Échange de fichiers

To copy and paste files and directories (folders) from one *qube* to another, you can use the option **Copy to Other AppVM...** or **Move to Other AppVM...**. La différence est que l'option **Déplacer** supprime le fichier d'origine. Either option will protect your clipboard from being leaked to any other *qubes*. This is more secure than air-gapped file transfer. An air-gapped computer will still be forced to parse partitions or file systems. Cela n'est pas nécessaire avec le système de copie inter-qube.

??? "Qubes do not have their own filesystems."

    You can [copy and move files](https://www.qubes-os.org/doc/how-to-copy-and-move-files/) between *qubes*. Ce faisant, les changements ne sont pas immédiats et peuvent être facilement annulés en cas d'accident. When you run a *qube*, it does not have a persistent filesystem. You can create and delete files, but these changes are ephemeral.

### Interactions inter-VM

The [qrexec framework](https://www.qubes-os.org/doc/qrexec/) is a core part of Qubes which allows communication between domains. Il est construit sur la bibliothèque Xen *vchan*, qui facilite [l'isolation de par le biais de politiques](https://www.qubes-os.org/news/2020/06/22/new-qrexec-policy-system/).

## Ressources supplémentaires

Pour de plus amples informations, nous vous encourageons à consulter les pages de documentation complètes de Qubes OS, situées sur le [site web de Qubes OS](https://www.qubes-os.org/doc/). Des copies hors ligne peuvent être téléchargées à partir du [dépôt de documentationde](https://github.com/QubesOS/qubes-doc) Qubes OS.

- [Arguably the world's most secure operating system](https://www.opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard/) (Open Technology Fund)
- [Software compartmentalization vs. physical separation](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf) (J. Rutkowska)
- [Partitioning my digital life into security domains](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html) (J. Rutkowska)
- [Related Articles](https://www.qubes-os.org/news/categories/#articles) (Qubes OS)
