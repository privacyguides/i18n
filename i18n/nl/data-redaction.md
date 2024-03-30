---
meta_title: "Remove PII with Metadata Scrubbers and Data Redaction Tools - Privacy Guides"
title: "Data and Metadata Redaction"
icon: material/tag-remove
description: Use these tools to remove metadata like GPS location and other identifying information from photos and files you share.
cover: data-redaction.webp
---

Wanneer je bestanden deelt, is het belangrijk om de bijbehorende metadata te verwijderen. Afbeeldingsbestanden bevatten vaak [Exif](https://en.wikipedia.org/wiki/Exif) data. Foto's bevatten soms zelfs GPS-coördinaten in de metadata van het bestand.

## Desktop

### MAT2

<div class="admonition recommendation" markdown>

![MAT2 logo](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2** is vrije software, waarmee de metadata uit beeld-, audio-, torrent- en documentbestanden kan worden verwijderd. It provides both a command line tool and a graphical user interface via an extension for [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin), the default file manager of [KDE](https://kde.org).

Voor Linux bestaat een grafisch hulpprogramma van derden [Metadata Cleaner](https://gitlab.com/rmnvgr/metadata-cleaner) op basis van MAT2, dat [beschikbaar is op Flathub](https://flathub.org/apps/details/fr.romainvigier.MetadataCleaner).

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

## Mobiel

### ExifEraser (Android)

<div class="admonition recommendation" markdown>

![ExifEraser logo](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser** is een moderne, toestemmingsvrije applicatie voor het verwijderen van metadata in afbeeldingen voor Android.

Het ondersteunt momenteel JPEG-, PNG- en WebP-bestanden.

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

De metagegevens die worden gewist, hangen af van het bestandstype van de afbeelding:

- **JPEG**: ICC Profile, Exif, Photoshop Image Resources en XMP/ExtendedXMP metadata worden gewist als ze bestaan.
- **PNG**: ICC Profile, Exif en XMP metadata worden gewist als ze bestaan.
- **WebP**: ICC Profile, Exif en XMP metadata zullen worden gewist als ze bestaan.

Na het verwerken van de afbeeldingen, geeft ExifEraser je een volledig overzicht over wat er precies uit elke afbeelding is verwijderd.

De app biedt meerdere manieren om metadata uit afbeeldingen te wissen. Namelijk:

- Je kunt een afbeelding vanuit een andere toepassing delen met ExifEraser.
- Via de app zelf kan je een enkele afbeelding, meerdere afbeeldingen tegelijk of zelfs een hele map selecteren.
- Het heeft een "Camera"-optie, die de camera-app van je besturingssysteem gebruikt om een foto te maken, en vervolgens de metadata ervan verwijdert.
- Het laat je foto's uit een ander programma naar ExifEraser slepen wanneer beide programma's in split-screen modus geopend zijn.
- Als laatste kan je een afbeelding uit het klembord plakken.

### Metapho (iOS)

<div class="admonition recommendation" markdown>

![Metapho logo](assets/img/data-redaction/metapho.jpg){ align=right }

Metapho geeft eenvoudige en nette weergave van de afbeeldingsmetadata zoals datum, bestandsnaam, grootte, camera model, sluitertijd, en locatie.

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

**PrivacyBlur** is een gratis app die gevoelige delen van foto's kan vervagen voordat je ze online deelt.

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

Je moet **nooit** vervaging gebruiken om [tekst in afbeeldingen](https://bishopfox.com/blog/unredacter-tool-never-pixelation) te redigeren. Als u tekst in een afbeelding wilt redigeren, tekent u een kader over de tekst. Hiervoor stellen wij apps voor zoals [Pocket Paint](https://github.com/Catrobat/Paintroid).

</div>

## Command-line

### ExifTool

<div class="admonition recommendation" markdown>

![ExifTool logo](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool** is de originele perl library en command-line applicatie voor het lezen, schrijven en bewerken van metadata (Exif, IPTC, XMP, en meer) in een groot aantal bestandsformaten (JPEG, TIFF, PNG, PDF, RAW, en meer).

Het is vaak een onderdeel van andere Exif verwijderingsprogramma's en staat in de repositories van de meeste Linux distributies.

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

## Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

- Apps developed for open-source operating systems must be open source.
- Apps moeten gratis zijn en mogen geen advertenties of andere beperkingen bevatten.
