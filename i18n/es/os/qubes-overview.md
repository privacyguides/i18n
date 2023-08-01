---
title: "Visión General de Qubes"
icon: simple/qubesos
description: Qubes is an operating system built around isolating apps within *qubes* (formerly "VMs") for heightened security.
---

[**Qubes OS**](../desktop.md#qubes-os) is an open-source operating system which uses the [Xen](https://en.wikipedia.org/wiki/Xen) hypervisor to provide strong security for desktop computing through isolated *qubes*, (which are Virtual Machines). You can assign each *qube* a level of trust based on its purpose. Qubes OS provides security by using isolation. It only permits actions on a per-case basis and therefore is the opposite of [badness enumeration](https://www.ranum.com/security/computer_security/editorials/dumb/).

## ¿Cómo funciona Qubes OS?

Qubes utiliza la [compartimentación](https://www.qubes-os.org/intro/) para mantener el sistema seguro. Qubes son creados de plantillas, las predeterminadas siendo para Fedora, Debian y [Whonix](../desktop.md#whonix). Qubes OS also allows you to create once-use [disposable](https://www.qubes-os.org/doc/how-to-use-disposables/) *qubes*.

??? "The term *qubes* is gradually being updated to avoid referring to them as "virtual machines"."

    Some of the information here and on the Qubes OS documentation may contain conflicting language as the "appVM" term is gradually being changed to "qube". Qubes are not entire virtual machines, but maintain similar functionalities to VMs.

![Arquitectura Qubes](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Qubes Arquitectura, Crédito: Qué es Qubes OS Introducción</figcaption>

Each qube has a [colored border](https://www.qubes-os.org/screenshots/) that can help you keep track of the domain in which it runs. Podrías, por ejemplo, usar un color específico para tu navegador bancario, mientras usas un color diferente para un navegador general no confiado.

![Borde coloreado](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Bordes de ventana de Qubes, Crédito: Capturas de pantalla de Qubes</figcaption>

## ¿Por qué utilizar Qubes?

Qubes OS is useful if your [threat model](../basics/threat-modeling.md) requires strong security and isolation, such as if you think you'll be opening untrusted files from untrusted sources. A typical reason for using Qubes OS is to open documents from unknown sources, but the idea is that if a single qube is compromised it won't affect the rest of the system.

Qubes OS utilizes [dom0](https://wiki.xenproject.org/wiki/Dom0) Xen VM for controlling other *qubes* on the host OS, all of which display individual application windows within dom0's desktop environment. There are many uses for this type of architecture. Here are some tasks you can perform. You can see just how much more secure these processes are made by incorporating multiple steps.

### Copiar y pegar texto

Puedes [copiar y pegar texto](https://www.qubes-os.org/doc/how-to-copy-and-paste-text/) utilizando `qvm-copy-to-vm` o las instrucciones siguientes:

1. Press **Ctrl+C** to tell the *qube* you're in that you want to copy something.
2. Press **Ctrl+Shift+C** to tell the *qube* to make this buffer available to the global clipboard.
3. Press **Ctrl+Shift+V** in the destination *qube* to make the global clipboard available.
4. Press **Ctrl+V** in the destination *qube* to paste the contents in the buffer.

### Intercambio de archivos

To copy and paste files and directories (folders) from one *qube* to another, you can use the option **Copy to Other AppVM...** or **Move to Other AppVM...**. La diferencia es que la opción **Mover** borrará el archivo original. Either option will protect your clipboard from being leaked to any other *qubes*. This is more secure than air-gapped file transfer. An air-gapped computer will still be forced to parse partitions or file systems. Esto no es necesario con el sistema de copia inter-qube.

??? "Qubes do not have their own filesystems."

    You can [copy and move files](https://www.qubes-os.org/doc/how-to-copy-and-move-files/) between *qubes*. Al hacerlo, los cambios no son inmediatos y pueden deshacerse fácilmente en caso de accidente. When you run a *qube*, it does not have a persistent filesystem. You can create and delete files, but these changes are ephemeral.

### Interacciones inter-VM

The [qrexec framework](https://www.qubes-os.org/doc/qrexec/) is a core part of Qubes which allows communication between domains. Está construido sobre la librería Xen *vchan*, que facilita el [aislamiento a través de políticas](https://www.qubes-os.org/news/2020/06/22/new-qrexec-policy-system/).

## Recursos Adicionales

Para obtener información adicional, te animamos a consultar las extensas páginas de documentación de Qubes OS que se encuentran en el [sitio web Qubes OS](https://www.qubes-os.org/doc/). Copias offline se pueden descargar desde el [repositorio de documentación ](https://github.com/QubesOS/qubes-doc)de Qubes OS.

- [Arguably the world's most secure operating system](https://www.opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard/) (Open Technology Fund)
- [Software compartmentalization vs. physical separation](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf) (J. Rutkowska)
- [Partitioning my digital life into security domains](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html) (J. Rutkowska)
- [Related Articles](https://www.qubes-os.org/news/categories/#articles) (Qubes OS)
