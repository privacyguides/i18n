---
meta_title: "Remove PII with Metadata Scrubbers and Data Redaction Tools - Privacy Guides"
title: "Data and Metadata Redaction"
icon: material/tag-remove
description: Use these tools to remove metadata like GPS location and other identifying information from photos and files you share.
cover: data-redaction.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-search: Paparan Publik](basics/common-threats.md#limiting-public-information ""){.pg-green}

Saat berbagi file, pastikan untuk menghapus metadata terkait. File gambar biasanya menyertakan data [Exif](https://en.wikipedia.org/wiki/Exif). Foto terkadang bahkan menyertakan koordinat GPS dalam metadata file.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Anda *"tidak boleh** menggunakan teknik blur untuk menyamarkan [teks dalam gambar](https://bishopfox.com/blog/unredacter-tool-never-pixelation). If you want to redact text in an image, you should draw a box over the text.

</div>

## MAT2

<div class="admonition recommendation" markdown>

![MAT2 logo](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2** is free, cross-platform software which allows you to remove metadata from image, audio, torrent, and document file types. It provides both a command line tool and a graphical user interface via an extension for [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin), the default file manager of [KDE](https://kde.org).

[:octicons-repo-16: Repository](https://0xacab.org/jvoisin/mat2){ .md-button .md-button--primary }
[:octicons-info-16:](https://0xacab.org/jvoisin/mat2/-/blob/master/README.md){ .card-link title="Documentation" }
[:octicons-code-16:](https://0xacab.org/jvoisin/mat2){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://pypi.org/project/mat2)
- [:simple-apple: macOS](https://0xacab.org/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: Linux](https://pypi.org/project/mat2)
- [:octicons-globe-16: Web](https://0xacab.org/jvoisin/mat2#web-interface)

</details>

</div>

## ExifEraser (Android)

<div class="admonition recommendation" markdown>

![Logo ExifEraser](assets/img/data-redaksi/exiferaser.svg){ align=right }

**ExifEraser** adalah aplikasi penghapus metadata gambar modern tanpa izin untuk Android.

Saat ini mendukung file JPEG, PNG dan WebP.

[:octicons-repo-16: Repository](https://github.com/Tommy-Geenexus/exif-eraser){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .card-link title="Documentation" }
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

## Shortcuts (iOS & macOS)

On iOS and macOS, you can remove image metadata without using any third-party apps by creating a [**shortcut**](https://apps.apple.com/app/id915249334) for this purpose. Here is an example shortcut you can download to use as is:

[:material-tag-minus: Clean Image Metadata](https://icloud.com/shortcuts/fb774ddb7b5b4296871776c67ac0fff9 ""){.md-button}

You can also use it as a model for your own shortcut; just make sure that the **Preserve Metadata** option under the **Convert** action is unchecked. Once added, you can access the shortcut in the share sheet that appears when you select the :octicons-share-24: Share button. You can select multiple images and invoke the shortcut to remove their metadata all at once.

This shortcut removes metadata such as location, device model, lens model, and other camera information. It also sets the image creation date to the time the shortcut was used.

## ExifTool (CLI)

<div class="admonition recommendation" markdown>

![ExifTool logo](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool** is the original Perl library and command-line application for reading, writing, and editing meta information (Exif, IPTC, XMP, and more) in a wide variety of file formats (JPEG, TIFF, PNG, PDF, RAW, and more).

It is often a component of other Exif removal applications and in most Linux distribution repositories.

[:octicons-home-16: Homepage](https://exiftool.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://exiftool.org/faq.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/exiftool/exiftool){ .card-link title="Source Code" }
[:octicons-heart-16:](https://exiftool.org/#donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://exiftool.org)
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

- Aplikasi yang dikembangkan untuk sistem operasi sumber terbuka haruslah bersumber terbuka.
- Aplikasi harus gratis dan tidak boleh menyertakan iklan atau batasan lainnya.
