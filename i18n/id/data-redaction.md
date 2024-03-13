---
meta_title: "Remove PII with Metadata Scrubbers and Data Redaction Tools - Privacy Guides"
title: "Data and Metadata Redaction"
icon: material/tag-remove
description: Use these tools to remove metadata like GPS location and other identifying information from photos and files you share.
cover: data-redaction.webp
---

Saat berbagi file, pastikan untuk menghapus metadata terkait. File gambar biasanya menyertakan data [Exif](https://en.wikipedia.org/wiki/Exif). Foto terkadang bahkan menyertakan koordinat GPS dalam metadata file.

## Desktop

### MAT2

<div class="admonition recommendation" markdown>

![Logo MAT2](assets/img/data-redaksi/mat2.svg){ align=right }

**MAT2** adalah perangkat lunak gratis, yang memungkinkan metadata dihapus dari jenis file gambar, audio, torrent, dan dokumen. It provides both a command line tool and a graphical user interface via an extension for [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin), the default file manager of [KDE](https://kde.org).

Di Linux, alat grafis pihak ketiga [Metadata Cleaner] (https://gitlab.com/rmnvgr/metadata-cleaner) yang didukung oleh MAT2 ada dan [tersedia di Flathub] (https://flathub.org/apps/details/fr.romainvigier.MetadataCleaner).

[:octicons-repo-16: Repository](https://0xacab.org/jvoisin/mat2){ .md-button .md-button--primary }
[:octicons-info-16:](https://0xacab.org/jvoisin/mat2/-/blob/master/README.md){ .card-link title=Documentation}
[:octicons-code-16:](https://0xacab.org/jvoisin/mat2){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://pypi.org/project/mat2)
- [:simple-apple: macOS](https://0xacab.org/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: Linux](https://pypi.org/project/mat2)
- [:octicons-globe-16: Web](https://0xacab.org/jvoisin/mat2#web-interface)

</details>

</div>

## Handphone

### ExifEraser (Android)

<div class="admonition recommendation" markdown>

![Logo ExifEraser](assets/img/data-redaksi/exiferaser.svg){ align=right }

**ExifEraser** adalah aplikasi penghapus metadata gambar modern tanpa izin untuk Android.

Saat ini mendukung file JPEG, PNG dan WebP.

[:octicons-repo-16: Repository](https://github.com/Tommy-Geenexus/exif-eraser){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/Tommy-Geenexus/exif-eraser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.none.tom.exiferaser)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/com.none.tom.exiferaser)
- [:simple-github: GitHub](https://github.com/Tommy-Geenexus/exif-eraser/releases)

</details>

</div>

Metadata yang dihapus, bergantung pada jenis file gambar:

- **JPEG**: Profil ICC, Exif, Sumber Daya Gambar Photoshop, dan metadata XMP/ExtendedXMP akan dihapus jika ada.
- **PNG**: Profil ICC, metadata Exif dan XMP akan dihapus jika ada.
- **WebP**: Profil ICC, Exif dan metadata XMP akan dihapus jika ada.

Setelah memproses gambar, ExifEraser memberi Anda laporan lengkap mengenai apa yang sesungguhnya dihapus dari tiap gambar.

Aplikasi ini menawarkan beberapa cara untuk menghapus metadata dari gambar. Yaitu:

- Anda dapat berbagi gambar dari aplikasi lain dengan ExifEraser.
- Melalui aplikasi itu sendiri, Anda dapat memilih satu gambar, beberapa gambar sekaligus, atau bahkan seluruh direktori.
- Aplikasi ini memiliki opsi "Kamera", yang menggunakan aplikasi kamera sistem operasi Anda untuk mengambil foto, dan kemudian menghapus metadata dari foto tersebut.
- Anda dapat menyeret foto dari aplikasi lain ke ExifEraser apabila keduanya terbuka dalam mode layar terbagi.
- Terakhir, Anda dapat menempelkan gambar dari clipboard Anda.

### Metapho (iOS)

<div class="admonition recommendation" markdown>

![Metapho logo](assets/img/data-redaksi/metapho.jpg){ align=right }

**Metapho** adalah penampil yang sederhana dan bersih untuk metadata foto seperti tanggal, nama file, ukuran, model kamera, kecepatan rana, dan lokasi.

[:octicons-home-16: Homepage](https://zininworks.com/metapho){ .md-button .md-button--primary }
[:octicons-eye-16:](https://zininworks.com/privacy){ .card-link title="Privacy Policy" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id914457352)

</details>

</div>

### PrivacyBlur

<div class="admonition recommendation" markdown>

![Logo PrivacyBlur](assets/img/data-redaksi/privacyblur.svg){ align=right }

**PrivacyBlur** adalah aplikasi gratis yang dapat memburamkan bagian gambar yang sensitif sebelum membagikannya secara online.

[:octicons-home-16: Homepage](https://privacyblur.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://privacyblur.app/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/MATHEMA-GmbH/privacyblur#readme){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/MATHEMA-GmbH/privacyblur){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.mathema.privacyblur)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1536274106)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Anda *"tidak boleh** menggunakan teknik blur untuk menyamarkan [teks dalam gambar](https://bishopfox.com/blog/unredacter-tool-never-pixelation). Jika Anda ingin menyamarkan teks dalam gambar, gambarlah sebuah kotak di atas teks. Untuk ini, kami menyarankan aplikasi seperti [Pocket Paint](https://github.com/Catrobat/Paintroid).

</div>

## Baris perintah

### ExifTool

<div class="admonition recommendation" markdown>

![Logo ExifTool](assets/img/data-redaksi/exiftool.png){ align=right }

**ExifTool** adalah library dari perl dan sebuah aplikasi baris perintah untuk membaca, menulis, dan mengedit informasi meta (Exif, IPTC, XMP, dan banyak lagi) dalam berbagai macam format file (JPEG, TIFF, PNG, PDF, RAW, dan banyak lagi).

Aplikasi ini sering kali merupakan komponen dari aplikasi penghapus Exif lainnya dan ada di sebagian besar repositori distribusi Linux.

[:octicons-home-16: Homepage](https://exiftool.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://exiftool.org/faq.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/exiftool/exiftool){ .card-link title="Source Code" }
[:octicons-heart-16:](https://exiftool.org/#donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://exiftool.org)
- [:simple-apple: macOS](https://exiftool.org)
- [:simple-linux: Linux](https://exiftool.org)

</details>

</div>

<div class="admonition example" markdown>
<p class="admonition-title">Deleting data from a directory of files</p>

```bash
exiftool -all= *.file_extension
```

</div>

## Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih untuk menggunakan sebuah proyek, dan melakukan penelitian sendiri untuk memastikan bahwa itu adalah pilihan yang tepat untuk Anda.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Kami sedang berupaya menetapkan kriteria yang jelas untuk setiap bagian dari situs kami, dan hal ini dapat berubah sewaktu-waktu. Jika Anda memiliki pertanyaan mengenai kriteria kami, silakan [tanyakan di forum](https://discuss.privacyguides.net/latest) dan jangan berasumsi bahwa kami tidak mempertimbangkan sesuatu saat membuat rekomendasi jika tidak tercantum di sini. Ada banyak faktor yang dipertimbangkan dan didiskusikan saat kami merekomendasikan sebuah proyek, dan mendokumentasikan setiap faktor tersebut merupakan sebuah pekerjaan yang sedang berjalan.

</div>

- Aplikasi yang dikembangkan untuk sistem operasi sumber terbuka haruslah bersumber terbuka.
- Aplikasi harus gratis dan tidak boleh menyertakan iklan atau batasan lainnya.
