---
title: "Berbagi dan Sinkronisasi File"
icon: material/share-variant
description: Temukan cara berbagi file secara pribadi di antara perangkat Anda, dengan teman dan keluarga, atau secara anonim secara online.
cover: file-sharing.png
---

Temukan cara berbagi file secara pribadi di antara perangkat Anda, dengan teman dan keluarga, atau secara anonim secara online.

## Berbagi File

### Send

!!! recommendation

    ![Logo Send](assets/img/file-sharing-sync/send.svg){ align=right }
    
    **Send** adalah cabang dari layanan Firefox Send yang sudah tidak digunakan lagi oleh Mozilla yang memungkinkan Anda untuk mengirim berkas kepada orang lain dengan sebuah tautan. File dienkripsi di perangkat Anda sehingga tidak dapat dibaca oleh server, dan secara opsional juga dapat dilindungi dengan kata sandi. Pengelola Send menghosting sebuah [server publik](https://send.vis.ee/). Anda bisa menggunakan server publik lainnya, atau Anda bisa meng-host Send sendiri.
    
    [:octicons-home-16: Homepage](https://send.vis.ee){ .md-button .md-button--primary }
    [:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="Public Instances"}
    [:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title=Contribute }

Send dapat digunakan melalui antarmuka webnya atau melalui CLI [ffsend](https://github.com/timvisee/ffsend). Jika Anda terbiasa dengan baris perintah dan sering mengirim file, kami sarankan untuk menggunakan klien CLI untuk menghindari enkripsi berbasis JavaScript. Anda dapat menentukan flag `--host` untuk menggunakan server tertentu:

```bash
ffsend upload --host https://send.vis.ee/ FILE
```

### OnionShare

!!! recommendation

    ![Logo OnionShare](assets/img/file-sharing-sync/onionshare.svg){ align=right }
    
    **OnionShare** adalah alat sumber terbuka yang memungkinkan Anda berbagi file dengan aman dan anonim dalam berbagai ukuran. Ia bekerja dengan memulai server web yang dapat diakses sebagai layanan Tor onion, dengan URL yang tidak dapat dibaca yang dapat Anda bagikan dengan penerima untuk mengunduh atau mengirim berkas.
    
    [:octicons-home-16: Homepage](https://onionshare.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="Layanan Onion" }
    [:octicons-info-16:](https://docs.onionshare.org){ .card-link title=Dokumentasi}
    [:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="Kode Sumber" }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://onionshare.org/#download)
        - [:simple-apple: macOS](https://onionshare.org/#download)
        - [:simple-linux: Linux](https://onionshare.org/#download)

### Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih untuk menggunakan sebuah proyek, dan melakukan penelitian sendiri untuk memastikan bahwa itu adalah pilihan yang tepat untuk Anda.

!!! contoh "Bagian ini baru"

    Kami sedang berupaya menetapkan kriteria yang jelas untuk setiap bagian dari situs kami, dan hal ini dapat berubah sewaktu-waktu. Jika Anda memiliki pertanyaan mengenai kriteria kami, silakan [tanyakan di forum](https://discuss.privacyguides.net/latest) dan jangan berasumsi bahwa kami tidak mempertimbangkan sesuatu saat membuat rekomendasi jika tidak tercantum di sini. Ada banyak faktor yang dipertimbangkan dan didiskusikan saat kami merekomendasikan sebuah proyek, dan mendokumentasikan setiap faktor tersebut merupakan sebuah pekerjaan yang sedang berjalan.

- Tidak boleh menyimpan data yang telah didekripsi pada server jarak jauh.
- Harus berupa perangkat lunak sumber terbuka.
- Harus memiliki klien untuk Linux, macOS, dan Windows; atau memiliki antarmuka web.

## FreedomBox

!!! recommendation

    ![Logo FreedomBox](assets/img/file-sharing-sync/freedombox.svg){ align=right }
    
    **FreedomBox** adalah sistem operasi yang dirancang untuk dijalankan pada [komputer papan tunggal (SBC)] (https://en.wikipedia.org/wiki/Single-board_computer). Tujuannya adalah untuk memudahkan pengaturan aplikasi server yang mungkin ingin Anda hosting sendiri.
    
    [:octicons-home-16: Homepage](https://freedombox.org){ .md-button .md-button--primary }
    [:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title=Dokumentasi}
    [:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="Kode Sumber" }
    [:octicons-heart-16:](https://freedomboxfoundation.org/donate/){ .card-link title=Kontribusi }

## File Sync

### Nextcloud (Client-Server)

!!! recommendation

    ![Nextcloud logo](assets/img/productivity/nextcloud.svg){ align=right }
    
    **Nextcloud** is a suite of free and open-source client-server software for creating your own file hosting services on a private server you control.
    
    [:octicons-home-16: Homepage](https://nextcloud.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://nextcloud.com/support/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://nextcloud.com/contribute/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
        - [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
        - [:simple-windows11: Windows](https://nextcloud.com/install/#install-clients)
        - [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
        - [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

!!! danger

    We don't recommend using the [E2EE App](https://apps.nextcloud.com/apps/end_to_end_encryption) for Nextcloud as it may lead to data loss; it is highly experimental and not production quality.

### Syncthing (P2P)

!!! recommendation

    ![Syncthing logo](assets/img/file-sharing-sync/syncthing.svg){ align=right }
    
    **Syncthing** is an open-source peer-to-peer continuous file synchronization utility. It is used to synchronize files between two or more devices over the local network or the internet. Syncthing does not use a centralized server; it uses the [Block Exchange Protocol](https://docs.syncthing.net/specs/bep-v1.html#bep-v1) to transfer data between devices. All data is encrypted using TLS.
    
    [:octicons-home-16: Homepage](https://syncthing.net){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.syncthing.net){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/syncthing){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://syncthing.net/donations/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nutomic.syncthingandroid)
        - [:simple-windows11: Windows](https://syncthing.net/downloads/)
        - [:simple-apple: macOS](https://syncthing.net/downloads/)
        - [:simple-linux: Linux](https://syncthing.net/downloads/)
        - [:simple-freebsd: FreeBSD](https://syncthing.net/downloads/)

### Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih untuk menggunakan sebuah proyek, dan melakukan penelitian sendiri untuk memastikan bahwa itu adalah pilihan yang tepat untuk Anda.

!!! contoh "Bagian ini baru"

    Kami sedang berupaya menetapkan kriteria yang jelas untuk setiap bagian dari situs kami, dan hal ini dapat berubah sewaktu-waktu. Jika Anda memiliki pertanyaan mengenai kriteria kami, silakan [tanyakan di forum](https://discuss.privacyguides.net/latest) dan jangan berasumsi bahwa kami tidak mempertimbangkan sesuatu saat membuat rekomendasi jika tidak tercantum di sini. Ada banyak faktor yang dipertimbangkan dan didiskusikan saat kami merekomendasikan sebuah proyek, dan mendokumentasikan setiap faktor tersebut merupakan sebuah pekerjaan yang sedang berjalan.

#### Persyaratan Minimum

- Must not require a third-party remote/cloud server.
- Harus berupa perangkat lunak sumber terbuka.
- Harus memiliki klien untuk Linux, macOS, dan Windows; atau memiliki antarmuka web.

#### Kasus Terbaik

Kriteria kasus terbaik kami mewakili apa yang ingin kami lihat dari proyek yang sempurna dalam kategori ini. Rekomendasi kami mungkin tidak menyertakan salah satu atau semua fungsi ini, tetapi rekomendasi yang menyertakan fungsi ini mungkin memiliki peringkat yang lebih tinggi daripada yang lain di halaman ini.

- Has mobile clients for iOS and Android, which at least support document previews.
- Supports photo backup from iOS and Android, and optionally supports file/folder sync on Android.
