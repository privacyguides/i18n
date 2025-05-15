---
meta_title: "Remove PII with Metadata Scrubbers and Data Redaction Tools - Privacy Guides"
title: "Data and Metadata Redaction"
icon: material/tag-remove
description: Use these tools to remove metadata like GPS location and other identifying information from photos and files you share.
cover: data-redaction.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-search: Public Exposure](basics/common-threats.md#limiting-public-information ""){.pg-green}

Fájlok megosztásakor ügyelj a kapcsolódó metaadatok eltávolítsára. A képfájlok gyakran tartalmaznak [Exif](https://en.wikipedia.org/wiki/Exif) adatokat. A fényképek időnként még GPS-koordinátákat is tartalmaznak a fájl metaadataiban.

<div class="admonition warning" markdown>
<p class="admonition-title">Figyelmeztetés</p>

**Soha** ne használd a homályosítást [képekben lévő szöveg](https://bishopfox.com/blog/unredacter-tool-never-pixelation) szerkesztésére. If you want to redact text in an image, you should draw a box over the text.

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

- [:fontawesome-brands-windows: Windows](https://pypi.org/project/mat2#metadata-and-privacy)
- [:simple-apple: macOS](https://0xacab.org/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: Linux](https://pypi.org/project/mat2)
- [:octicons-globe-16: Web](https://0xacab.org/jvoisin/mat2#web-interface)

</details>

</div>

## ExifEraser (Android)

<div class="admonition recommendation" markdown>

![ExifEraser logo](assets/img/data-redaction/exiferaser.svg){ align=right }

Az **ExifEraser** egy modern, engedély nélküli képmetaadat-törlő alkalmazás Androidra.

It currently supports JPEG, PNG, and WebP files.

[:octicons-repo-16: Repository](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#description){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Tommy-Geenexus/exif-eraser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.none.tom.exiferaser)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/com.none.tom.exiferaser)
- [:simple-github: GitHub](https://github.com/Tommy-Geenexus/exif-eraser/releases)

</details>

</div>

A törlésre kerülő metaadat a kép fájltípusától függ:

- **JPEG**: ICC Profil, Exif, Photoshop Image Resources és XMP/ExtendedXMP metaadatok fognak törlődni, ha vannak.
- **PNG**: ICC Profil, Exif és XMP metaadatok fognak törlődni, ha vannak.
- **WebP**: ICC Profil, Exif és XMP metaadatok fognak törlődni, ha vannak.

A képek feldolgozása után ExifEraser teljes jelentést ad arról, hogy pontosan mit távolított el egyes képekről.

Az alkalmazás többféle módszert nyújt metaadatokat törléséhez a képekről. Név szerint:

- Az megoszthat egy képet egy másik alkalmazásból az ExifEraser-nek.
- Magán az alkalmazáson keresztül egyetlen képet, egyszerre több képet vagy akár egy egész könyvtárat is kiválaszthatsz.
- Rendelkezik egy "Kamera" opcióval, amely az operációs rendszer kameraalkalmazását használja egy fénykép készítéséhez, majd eltávolítja arról a metaadatokat.
- Lehetővé teszi, hogy fényképeket húzz át egy másik alkalmazásból az ExifEraser-be, ha mindkét app osztott képernyős módban van megnyitva.
- Végül, lehetővé teszi egy kép beillesztését a vágólapról.

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

## Követelmények

**Tartsd figyelemben, hogy nem állunk kapcsolatban az általunk ajánlott projektek egyikével sem.** Az [alap kritériumaink mellett](about/criteria.md), egyértelmű követelményrendszert dolgoztunk ki, hogy objektív ajánlásokat tudjunk tenni. Javasoljuk, hogy ismerkedj meg ezzel a listával, mielőtt kiválasztanál egy projektet, és végezz saját kutatásokat, hogy megbizonyosodj arról, hogy ez a megfelelő választás számodra.

- Apps developed for open-source operating systems must be open source.
- Az alkalmazásoknak ingyenesnek kell lenniük, és nem tartalmazhatnak reklámokat vagy egyéb korlátozásokat.
