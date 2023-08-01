---
title: "Panoramica di Qubes"
icon: simple/qubesos
description: Qubes is an operating system built around isolating apps within *qubes* (formerly "VMs") for heightened security.
---

[**Qubes OS**](../desktop.md#qubes-os) is an open-source operating system which uses the [Xen](https://en.wikipedia.org/wiki/Xen) hypervisor to provide strong security for desktop computing through isolated *qubes*, (which are Virtual Machines). You can assign each *qube* a level of trust based on its purpose. Qubes OS provides security by using isolation. It only permits actions on a per-case basis and therefore is the opposite of [badness enumeration](https://www.ranum.com/security/computer_security/editorials/dumb/).

## Come funziona Qubes OS?

Qubes utilizza la [compartimentazione](https://www.qubes-os.org/intro/) per mantenere il sistema sicuro. I Qube sono creati da modelli, predefiniti per Fedora, Debian e [Whonix](../desktop.md#whonix). Qubes OS also allows you to create once-use [disposable](https://www.qubes-os.org/doc/how-to-use-disposables/) *qubes*.

??? "The term *qubes* is gradually being updated to avoid referring to them as "virtual machines"."

    Some of the information here and on the Qubes OS documentation may contain conflicting language as the "appVM" term is gradually being changed to "qube". Qubes are not entire virtual machines, but maintain similar functionalities to VMs.

![Architettura Qubes](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Architettura di Qubes, Crediti: Introduzione a Qubes OS</figcaption>

Each qube has a [colored border](https://www.qubes-os.org/screenshots/) that can help you keep track of the domain in which it runs. Ad esempio, potresti utilizzare un colore specifico per le operazioni bancarie, utilizzandone uno differente per un browser generico non affidabile.

![Bordo colorato](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Bordi delle finestre di Qubes, Crediti: Screenshot di Qubes</figcaption>

## Perché dovrei usare Qubes?

Qubes OS is useful if your [threat model](../basics/threat-modeling.md) requires strong security and isolation, such as if you think you'll be opening untrusted files from untrusted sources. A typical reason for using Qubes OS is to open documents from unknown sources, but the idea is that if a single qube is compromised it won't affect the rest of the system.

Qubes OS utilizes [dom0](https://wiki.xenproject.org/wiki/Dom0) Xen VM for controlling other *qubes* on the host OS, all of which display individual application windows within dom0's desktop environment. There are many uses for this type of architecture. Here are some tasks you can perform. You can see just how much more secure these processes are made by incorporating multiple steps.

### Copiare e incollare il testo

Puoi [copiare e incollare il testo](https://www.qubes-os.org/doc/how-to-copy-and-paste-text/) utilizzando `qvm-copy-to-vm` o le istruzioni seguenti:

1. Press **Ctrl+C** to tell the *qube* you're in that you want to copy something.
2. Press **Ctrl+Shift+C** to tell the *qube* to make this buffer available to the global clipboard.
3. Press **Ctrl+Shift+V** in the destination *qube* to make the global clipboard available.
4. Press **Ctrl+V** in the destination *qube* to paste the contents in the buffer.

### Scambio di file

To copy and paste files and directories (folders) from one *qube* to another, you can use the option **Copy to Other AppVM...** or **Move to Other AppVM...**. La differenza è che l'opzione **Move** eliminerà il file originale. Either option will protect your clipboard from being leaked to any other *qubes*. This is more secure than air-gapped file transfer. An air-gapped computer will still be forced to parse partitions or file systems. Ciò non è necessario con il sistema di copia tra Qube.

??? "Qubes do not have their own filesystems."

    You can [copy and move files](https://www.qubes-os.org/doc/how-to-copy-and-move-files/) between *qubes*. Così facendo, le modifiche non sono effettuate immediatamente e sono facilmente annullabili, in caso di incidente. When you run a *qube*, it does not have a persistent filesystem. You can create and delete files, but these changes are ephemeral.

### Interazioni tra VM

The [qrexec framework](https://www.qubes-os.org/doc/qrexec/) is a core part of Qubes which allows communication between domains. Si basa sulla libreria di Xen *vchan*, che facilita l'[isolamento tramite politiche](https://www.qubes-os.org/news/2020/06/22/new-qrexec-policy-system/).

## Risorse aggiuntive

Per ulteriori informazioni si consiglia di consultare le ampie pagine di documentazione di Qubes OS presenti sul [sito web di Qubes OS](https://www.qubes-os.org/doc/). Le copie offline sono scaricabili dalla [repository della documentazione](https://github.com/QubesOS/qubes-doc) di Qubes OS.

- [Arguably the world's most secure operating system](https://www.opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard/) (Open Technology Fund)
- [Software compartmentalization vs. physical separation](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf) (J. Rutkowska)
- [Partitioning my digital life into security domains](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html) (J. Rutkowska)
- [Related Articles](https://www.qubes-os.org/news/categories/#articles) (Qubes OS)
