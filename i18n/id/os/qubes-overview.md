---
title: "Ikhtisar Qubes"
icon: simple/qubesos
description: Qubes adalah sistem operasi yang dibangun dengan mengisolasi aplikasi di dalam mesin virtual untuk meningkatkan keamanan.
---

[**Qubes OS**](../desktop.md#qubes-os) adalah sistem operasi yang menggunakan hypervisor [Xen](https://en.wikipedia.org/wiki/Xen) untuk memberikan keamanan yang kuat untuk komputasi desktop melalui mesin virtual yang terisolasi. Setiap VM disebut *Qube* dan Anda dapat menetapkan tingkat kepercayaan untuk setiap Qube berdasarkan tujuannya. Karena Qubes OS menyediakan keamanan dengan menggunakan isolasi, dan hanya mengizinkan tindakan berdasarkan kasus per kasus, ini merupakan kebalikan dari [badness enumeration](https://www.ranum.com/security/computer_security/editorials/dumb/).

## Bagaimana cara kerja Qubes OS?

Qubes menggunakan kompartementalisasi [](https://www.qubes-os.org/intro/) untuk menjaga sistem tetap aman. Qubes dibuat dari beberapa template, umumnya untuk Fedora, Debian dan [Whonix](../desktop.md#whonix). Qubes OS juga memungkinkan Anda untuk membuat mesin virtual [sekali pakai](https://www.qubes-os.org/doc/how-to-use-disposables/).

![Arsitektur Qubes](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Arsitektur Qubes, Kredit: Apa itu Qubes OS Intro</figcaption>

Setiap aplikasi Qubes memiliki [batas berwarna](https://www.qubes-os.org/screenshots/) yang dapat membantu Anda melacak mesin virtual yang sedang berjalan. Anda dapat menggunakan warna tertentu di peramban khusus untuk perbankan, sementara menggunakan warna yang berbeda untuk peramban umum yang tidak terpercaya.

![Pembatas berwarna](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Batas jendela Qubes, Kredit: Tangkapan Layar Qubes</figcaption>

## Mengapa saya harus menggunakan Qubes?

Qubes OS berguna jika [ancaman model](../basics/threat-modeling.md) Anda membutuhkan kompartementalisasi dan keamanan yang kuat, misalnya jika Anda merasa akan membuka file yang tidak terpercaya dari sumber yang tidak terpercaya. Alasan umum untuk menggunakan Qubes OS adalah untuk membuka dokumen dari sumber yang tidak dikenal.

Qubes OS menggunakan [Dom0](https://wiki.xenproject.org/wiki/Dom0) Xen VM (yaitu, "AdminVM") untuk mengendalikan VM tamu atau Qubes lain pada OS host. VM lain menampilkan jendela aplikasi individual dalam lingkungan desktop Dom0. Ini memungkinkan Anda untuk memberi kode warna pada jendela berdasarkan tingkat kepercayaan dan menjalankan aplikasi yang dapat berinteraksi satu sama lain dengan kontrol yang sangat terperinci.

### Menyalin dan Menempel Teks

Anda dapat [menyalin dan menempelkan teks](https://www.qubes-os.org/doc/how-to-copy-and-paste-text/) menggunakan `qvm-copy-to-vm` atau dengan petunjuk di bawah ini:

1. Tekan **Ctrl+C** untuk memberi tahu VM yang sedang Anda gunakan bahwa Anda ingin menyalin sesuatu.
2. Tekan **Ctrl+Shift+C** untuk memberi tahu VM agar buffer ini tersedia di clipboard global.
3. Tekan **Ctrl+Shift+V** di VM dengan tujuan untuk membuat papan klip global tersedia.
4. Tekan **Ctrl+V** di VM tujuan untuk menempelkan konten di buffer.

### Pertukaran File

Untuk menyalin dan menempelkan file dan direktori (folder) dari satu VM ke VM lainnya, Anda dapat menggunakan opsi **Copy to Other AppVM...** atau **Move to Other AppVM...**. Perbedaannya adalah bahwa opsi **Pindahkan** akan menghapus file asli. Opsi mana pun akan melindungi papan klip Anda agar tidak bocor ke Qubes lainnya. Ini lebih aman daripada transfer file melalui celah udara karena komputer yang memiliki celah udara masih akan dipaksa untuk mengurai partisi atau sistem file. Hal itu tidak diperlukan dengan sistem penyalinan antar-qube.

??? info "AppVM atau qubes tidak memiliki sistem file sendiri"

    Anda dapat [menyalin dan memindahkan file](https://www.qubes-os.org/doc/how-to-copy-and-move-files/) di antara Qubes. Ketika melakukan hal tersebut, perubahan tidak langsung dilakukan dan dapat dengan mudah dibatalkan jika terjadi kecelakaan.

### Interaksi Antar-VM

Kerangka kerja qrexec [](https://www.qubes-os.org/doc/qrexec/) adalah bagian inti dari Qubes yang memungkinkan komunikasi mesin virtual antar domain. Ini dibangun di atas pustaka Xen *vchan*, yang memfasilitasi [isolasi melalui kebijakan](https://www.qubes-os.org/news/2020/06/22/new-qrexec-policy-system/).

## Sumber Daya Tambahan

Untuk informasi tambahan, kami menganjurkan Anda untuk membaca halaman dokumentasi Qubes OS yang luas yang terletak di [Situs Web Qubes OS](https://www.qubes-os.org/doc/). Salinan offline dapat diunduh dari [repositori dokumentasi](https://github.com/QubesOS/qubes-doc) Qubes OS.

- Open Technology Fund: [*Arguably the world's most secure operating system*](https://www.opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard/)
- J. Rutkowska: [*Kompartementalisasi perangkat lunak vs pemisahan fisik*](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf)
- J. Rutkowska: [*Memisahkan kehidupan digital saya ke dalam domain keamanan*](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html)
- Qubes OS: [*Artikel Terkait*](https://www.qubes-os.org/news/categories/#articles)
