---
title: "Ikhtisar Qubes"
icon: simple/qubesos
description: Qubes is an operating system built around isolating apps within *qubes* (formerly "VMs") for heightened security.
---

[**Qubes OS**](../desktop.md#qubes-os) is an open-source operating system which uses the [Xen](https://en.wikipedia.org/wiki/Xen) hypervisor to provide strong security for desktop computing through isolated *qubes*, (which are Virtual Machines). You can assign each *qube* a level of trust based on its purpose. Qubes OS provides security by using isolation. It only permits actions on a per-case basis and therefore is the opposite of [badness enumeration](https://www.ranum.com/security/computer_security/editorials/dumb/).

## Bagaimana cara kerja Qubes OS?

Qubes menggunakan kompartementalisasi [](https://www.qubes-os.org/intro/) untuk menjaga sistem tetap aman. Qubes dibuat dari beberapa template, umumnya untuk Fedora, Debian dan [Whonix](../desktop.md#whonix). Qubes OS also allows you to create once-use [disposable](https://www.qubes-os.org/doc/how-to-use-disposables/) *qubes*.

??? "The term *qubes* is gradually being updated to avoid referring to them as "virtual machines"."

    Some of the information here and on the Qubes OS documentation may contain conflicting language as the "appVM" term is gradually being changed to "qube". Qubes are not entire virtual machines, but maintain similar functionalities to VMs.

![Arsitektur Qubes](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Arsitektur Qubes, Kredit: Apa itu Qubes OS Intro</figcaption>

Each qube has a [colored border](https://www.qubes-os.org/screenshots/) that can help you keep track of the domain in which it runs. Anda dapat menggunakan warna tertentu di peramban khusus untuk perbankan, sementara menggunakan warna yang berbeda untuk peramban umum yang tidak terpercaya.

![Pembatas berwarna](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Batas jendela Qubes, Kredit: Tangkapan Layar Qubes</figcaption>

## Mengapa saya harus menggunakan Qubes?

Qubes OS is useful if your [threat model](../basics/threat-modeling.md) requires strong security and isolation, such as if you think you'll be opening untrusted files from untrusted sources. A typical reason for using Qubes OS is to open documents from unknown sources, but the idea is that if a single qube is compromised it won't affect the rest of the system.

Qubes OS utilizes [dom0](https://wiki.xenproject.org/wiki/Dom0) Xen VM for controlling other *qubes* on the host OS, all of which display individual application windows within dom0's desktop environment. There are many uses for this type of architecture. Here are some tasks you can perform. You can see just how much more secure these processes are made by incorporating multiple steps.

### Menyalin dan Menempel Teks

Anda dapat [menyalin dan menempelkan teks](https://www.qubes-os.org/doc/how-to-copy-and-paste-text/) menggunakan `qvm-copy-to-vm` atau dengan petunjuk di bawah ini:

1. Press **Ctrl+C** to tell the *qube* you're in that you want to copy something.
2. Press **Ctrl+Shift+C** to tell the *qube* to make this buffer available to the global clipboard.
3. Press **Ctrl+Shift+V** in the destination *qube* to make the global clipboard available.
4. Press **Ctrl+V** in the destination *qube* to paste the contents in the buffer.

### Pertukaran File

To copy and paste files and directories (folders) from one *qube* to another, you can use the option **Copy to Other AppVM...** or **Move to Other AppVM...**. Perbedaannya adalah bahwa opsi **Pindahkan** akan menghapus file asli. Either option will protect your clipboard from being leaked to any other *qubes*. This is more secure than air-gapped file transfer. An air-gapped computer will still be forced to parse partitions or file systems. Hal itu tidak diperlukan dengan sistem penyalinan antar-qube.

??? "Qubes do not have their own filesystems."

    You can [copy and move files](https://www.qubes-os.org/doc/how-to-copy-and-move-files/) between *qubes*. Ketika melakukan hal tersebut, perubahan tidak langsung dilakukan dan dapat dengan mudah dibatalkan jika terjadi kecelakaan. When you run a *qube*, it does not have a persistent filesystem. You can create and delete files, but these changes are ephemeral.

### Interaksi Antar-VM

The [qrexec framework](https://www.qubes-os.org/doc/qrexec/) is a core part of Qubes which allows communication between domains. Ini dibangun di atas pustaka Xen *vchan*, yang memfasilitasi [isolasi melalui kebijakan](https://www.qubes-os.org/news/2020/06/22/new-qrexec-policy-system/).

## Sumber Daya Tambahan

Untuk informasi tambahan, kami menganjurkan Anda untuk membaca halaman dokumentasi Qubes OS yang luas yang terletak di [Situs Web Qubes OS](https://www.qubes-os.org/doc/). Salinan offline dapat diunduh dari [repositori dokumentasi](https://github.com/QubesOS/qubes-doc) Qubes OS.

- [Arguably the world's most secure operating system](https://www.opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard/) (Open Technology Fund)
- [Software compartmentalization vs. physical separation](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf) (J. Rutkowska)
- [Partitioning my digital life into security domains](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html) (J. Rutkowska)
- [Related Articles](https://www.qubes-os.org/news/categories/#articles) (Qubes OS)
