---
title: Berbagi dan Sinkronisasi File
icon: material/share-variant
description: Temukan cara berbagi file secara pribadi di antara perangkat Anda, dengan teman dan keluarga, atau secara anonim secara online.
cover: file-sharing.webp
---

<small>Protects against the following threat(s):</small>

- [:material-server-network: Penyedia Layanan](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Temukan cara berbagi file secara pribadi di antara perangkat Anda, dengan teman dan keluarga, atau secara anonim secara online.

## Berbagi File

If you already use [Proton Drive](cloud.md#proton-drive)[^1] or have a [Bitwarden](passwords.md#bitwarden) Premium[^2] subscription, consider using the file sharing capabilities that they each offer, both of which use end-to-end encryption. Otherwise, the standalone options listed here ensure that the files you share are not read by a remote server.

### Send

<div class="admonition recommendation" markdown>

![Send logo](assets/img/file-sharing-sync/send.svg){ align=right }

**Send** is a fork of Mozilla's discontinued Firefox Send service which allows you to send files to others with a link. File dienkripsi di perangkat Anda sehingga tidak dapat dibaca oleh server, dan secara opsional juga dapat dilindungi dengan kata sandi. The maintainer of Send hosts a [public instance](https://send.vis.ee). Anda bisa menggunakan server publik lainnya, atau Anda bisa meng-host Send sendiri.

[:octicons-home-16: Homepage](https://send.vis.ee){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="Public Instances"}
[:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title="Contribute" }

</details>

</div>

Send dapat digunakan melalui antarmuka webnya atau melalui CLI [ffsend](https://github.com/timvisee/ffsend). Jika Anda terbiasa dengan baris perintah dan sering mengirim file, kami sarankan untuk menggunakan klien CLI untuk menghindari enkripsi berbasis JavaScript. Anda dapat menentukan flag `--host` untuk menggunakan server tertentu:

```bash
ffsend upload --host https://send.vis.ee/ FILE
```

### OnionShare

<div class="admonition recommendation" markdown>

![OnionShare logo](assets/img/file-sharing-sync/onionshare.svg){ align=right }

**OnionShare** is an open-source tool that lets you securely and [:material-incognito: anonymously](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } share a file of any size. Ia bekerja dengan memulai server web yang dapat diakses sebagai layanan Tor onion, dengan URL yang tidak dapat dibaca yang dapat Anda bagikan dengan penerima untuk mengunduh atau mengirim berkas.

[:octicons-home-16: Homepage](https://onionshare.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://docs.onionshare.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://onionshare.org/#download)
- [:simple-apple: macOS](https://onionshare.org/#download)
- [:simple-linux: Linux](https://onionshare.org/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/org.onionshare.OnionShare)

</details>

</div>

OnionShare provides the option to connect via [Tor bridges](https://docs.onionshare.org/2.6.2/en/tor.html#automatic-censorship-circumvention) to circumvent [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}.

### Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih untuk menggunakan sebuah proyek, dan melakukan penelitian sendiri untuk memastikan bahwa itu adalah pilihan yang tepat untuk Anda.

- Tidak boleh menyimpan data yang telah didekripsi pada server jarak jauh.
- Harus berupa perangkat lunak sumber terbuka.
- Harus memiliki klien untuk Linux, macOS, dan Windows; atau memiliki antarmuka web.

## File Sync

### Syncthing (P2P)

<div class="admonition recommendation" markdown>

![Syncthing logo](assets/img/file-sharing-sync/syncthing.svg){ align=right }

**Syncthing** is an open-source peer-to-peer continuous file synchronization utility. It is used to synchronize files between two or more devices over the local network or the internet. Syncthing does not use a centralized server; it uses the [Block Exchange Protocol](https://docs.syncthing.net/specs/bep-v1.html#bep-v1) to transfer data between devices. All data is encrypted using TLS.

[:octicons-home-16: Homepage](https://syncthing.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.syncthing.net){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/syncthing){ .card-link title="Source Code" }
[:octicons-heart-16:](https://syncthing.net/donations){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://syncthing.net/downloads)
- [:simple-apple: macOS](https://syncthing.net/downloads)
- [:simple-linux: Linux](https://syncthing.net/downloads)
- [:simple-freebsd: FreeBSD](https://syncthing.net/downloads)

</details>

</div>

### Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih untuk menggunakan sebuah proyek, dan melakukan penelitian sendiri untuk memastikan bahwa itu adalah pilihan yang tepat untuk Anda.

#### Persyaratan Minimum

- Must not require a third-party remote/cloud server.
- Harus berupa perangkat lunak sumber terbuka.
- Harus memiliki klien untuk Linux, macOS, dan Windows; atau memiliki antarmuka web.

#### Kasus Terbaik

Kriteria kasus terbaik kami mewakili apa yang ingin kami lihat dari proyek yang sempurna dalam kategori ini. Rekomendasi kami mungkin tidak menyertakan salah satu atau semua fungsi ini, tetapi rekomendasi yang menyertakan fungsi ini mungkin memiliki peringkat yang lebih tinggi daripada yang lain di halaman ini.

- Should have mobile clients for iOS and Android which at least support document previews.
- Should support photo backups from iOS and Android, and optionally support file/folder sync on Android.

[^1]: Proton Drive allows you to [share files or folders](https://proton.me/support/drive-shareable-link) by generating a shareable public link or sending a unique link to a designated email address. Public links can be protected with a password, set to expire, and completely revoked, while links shared via email can have custom permissions and be similarly revoked. Per Proton Drive's [privacy policy](https://proton.me/drive/privacy-policy), file contents, file and folder names, and thumbnail previews are end-to-end encrypted.
[^2]: With a [premium](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans) subscription, [Bitwarden Send](https://bitwarden.com/products/send) allows you to share files and text securely with [end-to-end encryption](https://bitwarden.com/help/send-encryption). A [password](https://bitwarden.com/help/send-privacy/#send-passwords) can be required along with the Send link. Bitwarden Send also features [automatic deletion](https://bitwarden.com/help/send-lifespan).
