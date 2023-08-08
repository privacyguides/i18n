---
title: "Ikhtisar Qubes"
icon: simple/qubesos
description: Qubes adalah sistem operasi yang dibangun dengan mengisolasi aplikasi di dalam *qubes* (sebelumnya disebut "VM") untuk meningkatkan keamanan.
---

[**Qubes OS**](../desktop.md#qubes-os) adalah sistem operasi sumber terbuka yang menggunakan hypervisor [Xen](https://en.wikipedia.org/wiki/Xen) untuk memberikan keamanan yang kuat untuk komputasi desktop melalui *qubes*yang terisolasi, (yang merupakan Mesin Virtual). Anda dapat menetapkan setiap *qube* tingkat kepercayaan berdasarkan tujuannya. Qubes OS menyediakan keamanan dengan menggunakan isolasi. Ini hanya mengizinkan tindakan berdasarkan basis per kasus dan oleh karena itu merupakan kebalikan dari [enumerasi keburukan](https://www.ranum.com/security/computer_security/editorials/dumb/).

## Bagaimana cara kerja Qubes OS?

Qubes menggunakan kompartementalisasi [](https://www.qubes-os.org/intro/) untuk menjaga sistem tetap aman. Qubes dibuat dari beberapa template, umumnya untuk Fedora, Debian dan [Whonix](../desktop.md#whonix). Qubes OS juga memungkinkan Anda untuk membuat [sekali pakai](https://www.qubes-os.org/doc/how-to-use-disposables/) *qubes sekali pakai*.

??? "Istilah *qubes* secara bertahap diperbarui untuk menghindari penyebutan sebagai "mesin virtual"."

    Beberapa informasi di sini dan di dokumentasi Qubes OS mungkin mengandung bahasa yang bertentangan karena istilah "appVM" secara bertahap diubah menjadi "qube". Qubes bukanlah mesin virtual secara keseluruhan, tetapi memiliki fungsi yang serupa dengan VM.

![Arsitektur Qubes](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Arsitektur Qubes, Kredit: Apa itu Qubes OS Intro</figcaption>

Setiap aplikasi Qubes memiliki [batas berwarna](https://www.qubes-os.org/screenshots/) yang dapat membantu Anda melacak mesin virtual yang sedang berjalan. Anda dapat menggunakan warna tertentu di peramban khusus untuk perbankan, sementara menggunakan warna yang berbeda untuk peramban umum yang tidak terpercaya.

![Pembatas berwarna](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Batas jendela Qubes, Kredit: Tangkapan Layar Qubes</figcaption>

## Mengapa saya harus menggunakan Qubes?

Qubes OS berguna jika [ancaman model](../basics/threat-modeling.md) Anda membutuhkan kompartementalisasi dan keamanan yang kuat, misalnya jika Anda merasa akan membuka file yang tidak terpercaya dari sumber yang tidak terpercaya. Alasan umum untuk menggunakan Qubes OS adalah untuk membuka dokumen dari sumber yang tidak dikenal, tetapi idenya adalah bahwa jika satu qubes disusupi, hal itu tidak akan memengaruhi seluruh sistem.

Qubes OS menggunakan [dom0](https://wiki.xenproject.org/wiki/Dom0) Xen VM untuk mengendalikan *qubes* lainnya pada OS host, yang semuanya menampilkan jendela aplikasi individual dalam lingkungan desktop dom0. Ada banyak kegunaan untuk jenis arsitektur ini. Berikut ini beberapa tugas yang dapat Anda lakukan. Anda dapat melihat betapa proses ini jauh lebih aman dengan menggabungkan beberapa langkah.

### Menyalin dan Menempel Teks

Anda dapat [menyalin dan menempelkan teks](https://www.qubes-os.org/doc/how-to-copy-and-paste-text/) menggunakan `qvm-copy-to-vm` atau dengan petunjuk di bawah ini:

1. Tekan **Ctrl+C** untuk memberi tahu *qube* yang Anda masuki bahwa Anda ingin menyalin sesuatu.
2. Tekan **Ctrl+Shift+C** untuk memberi tahu qube ** agar buffer ini tersedia di papan klip global.
3. Tekan **Ctrl+Shift+V** di tujuan *qube* untuk membuat papan klip global tersedia.
4. Tekan **Ctrl+V** di *qube* yang dituju untuk menempelkan konten di buffer.

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
