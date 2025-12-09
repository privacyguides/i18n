---
meta_title: "Usuwanie informacji osobistych za pomocą narzędzi do usuwania metadanych i redagowania danych - Privacy Guides"
title: "Redukcja danych i metadanych"
icon: material/tag-remove
description: Użyj tych narzędzi, aby usunąć metadane, takie jak lokalizacja GPS i inne informacje identyfikujące ze zdjęć i udostępnianych plików.
cover: data-redaction.webp
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-account-search: Ekspozycja publiczna](basics/common-threats.md#limiting-public-information ""){.pg-green}

Podczas udostępniania plików należy pamiętać o usunięciu powiązanych metadanych. Pliki obrazów zazwyczaj zawierają dane [Exif](https://en.wikipedia.org/wiki/Exif). Zdjęcia czasami zawierają nawet współrzędne GPS w metadanych pliku.

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

Nie powinieneś **nigdy** używać rozmycia do ukrycia [tekstu na obrazach](https://bishopfox.com/blog/unredacter-tool-never-pixelation). Jeśli chcesz ukryć tekst na obrazie, powinieneś narysować ramkę nad tekstem.

</div>

## MAT2

<div class="admonition recommendation" markdown>

![MAT2 logo](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2** to darmowe, wieloplatformowe oprogramowanie, które umożliwia usuwanie metadanych z plików graficznych, audio, torrent i dokumentów. It provides both a command line tool and a graphical user interface via an extension for [Dolphin](https://github.com/jvoisin/mat2/tree/master/dolphin), the default file manager of [KDE](https://kde.org).

[:octicons-repo-16: Repository](https://github.com/jvoisin/mat2#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/jvoisin/mat2#how-to-use-mat2){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/jvoisin/mat2){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://pypi.org/project/mat2)
- [:simple-apple: macOS](https://github.com/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: Linux](https://pypi.org/project/mat2)
- [:octicons-browser-16: Web](https://github.com/jvoisin/mat2#web-interface)

</details>

</div>

## ExifEraser (Android)

<div class="admonition recommendation" markdown>

![ExifEraser logo](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser** to nowoczesna, niewymagająca uprawnień aplikacja do usuwania metadanych obrazu dla systemu Android.

Obecnie obsługuje pliki JPEG, PNG i WebP.

[:octicons-repo-16: Repository](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#description){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Tommy-Geenexus/exif-eraser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Pliki do pobrania</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.none.tom.exiferaser)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/com.none.tom.exiferaser)
- [:simple-github: GitHub](https://github.com/Tommy-Geenexus/exif-eraser/releases)

</details>

</div>

The metadata that is erased depends on the image's file type:

- **JPEG**: ICC Profile, Exif, Photoshop Image Resources and XMP/ExtendedXMP metadata will be erased if it exists.
- **PNG**: ICC Profile, Exif and XMP metadata will be erased if it exists.
- **WebP**: ICC Profile, Exif and XMP metadata will be erased if it exists.

After processing the images, ExifEraser provides you with a full report about what exactly was removed from each image.

The app offers multiple ways to erase metadata from images. Namely:

- You can share an image from another application with ExifEraser.
- Through the app itself, you can select a single image, multiple images at once, or even an entire directory.
- It features a "Camera" option, which uses your operating system's camera app to take a photo, and then it removes the metadata from it.
- It allows you to drag photos from another app into ExifEraser when they are both open in split-screen mode.
- Lastly, it allows you to paste an image from your clipboard.

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

## Kryteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

- Apps developed for open-source operating systems must be open source.
- Apps must be free and should not include ads or other limitations.
