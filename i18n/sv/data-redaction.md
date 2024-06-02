---
meta_title: "Remove PII with Metadata Scrubbers and Data Redaction Tools - Privacy Guides"
title: "Data and Metadata Redaction"
icon: material/tag-remove
description: Use these tools to remove metadata like GPS location and other identifying information from photos and files you share.
cover: data-redaction.webp
---

När du delar filer ska du se till att ta bort tillhörande metadata. Bildfiler innehåller vanligtvis [Exif](https://en.wikipedia.org/wiki/Exif) data. Foton innehåller ibland även GPS-koordinater i filmetadata.

## Skrivbord

### MAT2

<div class="admonition recommendation" markdown>

![MAT2-logotyp](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2** är en gratis programvara som gör det möjligt att ta bort metadata från bild-, ljud-, torrent- och dokumentfiler. It provides both a command line tool and a graphical user interface via an extension for [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin), the default file manager of [KDE](https://kde.org).

På Linux finns ett grafiskt verktyg från tredje part [Metadata Cleaner] (https://gitlab.com/rmnvgr/metadata-cleaner) som drivs av MAT2 och är [tillgängligt på Flathub] (https://flathub.org/apps/details/fr.romainvigier.MetadataCleaner).

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

## Mobil

### ExifEraser (Android)

<div class="admonition recommendation" markdown>

![ExifEraser logo](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser** är ett modernt program för radering av bildmetadata för Android, utan behörighet.

För närvarande stöds JPEG-, PNG- och WebP-filer.

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

Vilka metadata som raderas beror på bildens filtyp:

- **JPEG**: ICC-profil, Exif, Photoshop Image Resources och XMP/ExtendedXMP-metadata raderas om de finns.
- **PNG**: ICC-profil, Exif- och XMP-metadata raderas om de finns.
- **PNG**: ICC-profil, Exif- och XMP-metadata raderas om de finns.

Efter att ha behandlat bilderna ger ExifEraser dig en fullständig rapport om exakt vad som togs bort från varje bild.

Appen erbjuder flera sätt att radera metadata från bilder. Namn:

- Du kan dela en bild från ett annat program med ExifEraser.
- I appen kan du välja en enda bild, flera bilder samtidigt eller till och med en hel katalog.
- Den har ett "kamera"-alternativ som använder operativsystemets kameraapp för att ta ett foto och sedan tar bort metadata från det.
- Du kan dra foton från en annan app till ExifEraser när båda är öppna i delad skärm.
- Slutligen kan du klistra in en bild från klippbordet.

### Metapho (iOS)

<div class="admonition recommendation" markdown>

![Metapho logotyp](assets/img/data-redaction/metapho.jpg){ align=right }

**Metapho** är en enkel och ren visare för fotometadata som datum, filnamn, storlek, kameramodell, slutartid och plats.

[:octicons-home-16: Homepage](https://zininworks.com/metapho){ .md-button .md-button--primary }
[:octicons-eye-16:](https://zininworks.com/privacy){ .card-link title="Privacy Policy" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id914457352)

</details>

</div>

### PrivacyBlur

<div class="admonition recommendation" markdown>

![PrivacyBlur-logotyp](assets/img/data-redaction/privacyblur.svg){ align=right }

**PrivacyBlur** är en gratis app som kan sudda ut känsliga delar av bilder innan de delas på nätet.

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
<p class="admonition-title">Varning</p>

Du bör **aldrig** använda oskärpa för att redigera [text i bilder] (https://bishopfox.com/blog/unredacter-tool-never-pixelation). Om du vill redigera text i en bild ritar du en ruta över texten. För detta föreslår vi appar som [Pocket Paint] (https://github.com/Catrobat/Paintroid).

</div>

## Kommandorad

### ExifTool

<div class="admonition recommendation" markdown>

![ExifTool logo](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool** är det ursprungliga perl-biblioteket och kommandoradstillämpningen för att läsa, skriva och redigera metainformation (Exif, IPTC, XMP med mera) i en mängd olika filformat (JPEG, TIFF, PNG, PDF, RAW med mera).

Det är ofta en del av andra program för att ta bort Exif-filer och finns i de flesta Linuxdistributioners arkiv.

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

## Kriterier

**Observera att vi inte är knutna till något av de projekt som vi rekommenderar.** Förutom [våra standardkriterier](about/criteria.md)har vi utvecklat en tydlig uppsättning krav som gör det möjligt för oss att ge objektiva rekommendationer. Vi föreslår att du bekantar dig med den här listan innan du väljer att använda ett projekt, och att du gör din egen forskning för att se till att det är rätt val för dig.

- Apps developed for open-source operating systems must be open source.
- Apparna måste vara gratis och får inte innehålla annonser eller andra begränsningar.
