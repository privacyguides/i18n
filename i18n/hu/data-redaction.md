---
meta_title: "Remove PII with Metadata Scrubbers and Data Redaction Tools - Privacy Guides"
title: "Data and Metadata Redaction"
icon: material/tag-remove
description: Use these tools to remove metadata like GPS location and other identifying information from photos and files you share.
cover: data-redaction.webp
---

Fájlok megosztásakor ügyelj a kapcsolódó metaadatok eltávolítsára. A képfájlok gyakran tartalmaznak [Exif](https://en.wikipedia.org/wiki/Exif) adatokat. A fényképek időnként még GPS-koordinátákat is tartalmaznak a fájl metaadataiban.

## Asztal

### MAT2

<div class="admonition recommendation" markdown>

![MAT2 logo](assets/img/data-redaction/mat2.svg){ align=right }

A **MAT2** szabad szoftver, amely lehetővé teszi a metaadatok eltávolítását kép, hang, torrent és dokumentum fájltípusokból. It provides both a command line tool and a graphical user interface via an extension for [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin), the default file manager of [KDE](https://kde.org).

Linuxon létezik egy harmadik féltől származó grafikus eszköz, a [Metadata Cleaner](https://gitlab.com/rmnvgr/metadata-cleaner), amely alapját a MAT2 adja, és ez [el is érhető a Flathubon](https://flathub.org/apps/details/fr.romainvigier.MetadataCleaner).

[:octicons-repo-16: Repository](https://0xacab.org/jvoisin/mat2){ .md-button .md-button--primary }
[:octicons-info-16:](https://0xacab.org/jvoisin/mat2/-/blob/master/README.md){ .card-link title=Documentation}
[:octicons-code-16:](https://0xacab.org/jvoisin/mat2){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://pypi.org/project/mat2)
- [:simple-apple: macOS](https://0xacab.org/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: Linux](https://pypi.org/project/mat2)
- [:octicons-globe-16: Web](https://0xacab.org/jvoisin/mat2#web-interface)

</details>

</div>

## Mobil

### ExifEraser (Android)

<div class="admonition recommendation" markdown>

![ExifEraser logo](assets/img/data-redaction/exiferaser.svg){ align=right }

Az **ExifEraser** egy modern, engedély nélküli képmetaadat-törlő alkalmazás Androidra.

Jelenleg támogatja a JPEG, PNG és WebP fájlokat.

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

### Metapho (iOS)

<div class="admonition recommendation" markdown>

![Metapho logo](assets/img/data-redaction/metapho.jpg){ align=right }

A **Metapho** egy egyszerű és letisztult megjelenítője fényképek metaadatainak, mint például dátum, fájlnév, méret, fényképező modell, zársebesség és helyszín.

[:octicons-home-16: Homepage](https://zininworks.com/metapho){ .md-button .md-button--primary }
[:octicons-eye-16:](https://zininworks.com/privacy){ .card-link title="Privacy Policy" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id914457352)

</details>

</div>

### PrivacyBlur

<div class="admonition recommendation" markdown>

![PrivacyBlur logo](assets/img/data-redaction/privacyblur.svg){ align=right }

A **PrivacyBlur** egy ingyenes alkalmazás, amely képes elmosni képek érzékeny részeit, mielőtt online megosztanád azokat.

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
<p class="admonition-title">Figyelmeztetés</p>

**Soha** ne használd a homályosítást [képekben lévő szöveg](https://bishopfox.com/blog/unredacter-tool-never-pixelation) szerkesztésére. Ha egy képen lévő szöveget szeretnél visszatartani, rajzolj egy négyzetet a szöveg fölé. Ehhez olyan alkalmazásokat ajánlunk, mint a [Pocket Paint](https://github.com/Catrobat/Paintroid).

</div>

## Parancssor

### ExifTool

<div class="admonition recommendation" markdown>

![ExifTool logo](assets/img/data-redaction/exiftool.png){ align=right }

Az **ExifTool** az eredeti perl könyvtár és parancssor alkalmazás a metainformációk (Exif, IPTC, XMP, stb.) olvasására, írására és szerkesztésére a legkülönbözőbb fájlformátumok (JPEG, TIFF, PNG, PDF, RAW, stb.) esetében.

Gyakran más Exif eltávolító alkalmazások része, és megtalálható a legtöbb Linux disztribúció addattáraiban.

[:octicons-home-16: Homepage](https://exiftool.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://exiftool.org/faq.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/exiftool/exiftool){ .card-link title="Source Code" }
[:octicons-heart-16:](https://exiftool.org/#donate){ .card-link title=Contribute }

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
