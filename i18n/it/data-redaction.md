---
meta_title: "Rimuovi PII con Scrubber di Metadati e Strumenti di riduzione dei dati - Privacy Guides"
title: "Rimozione di dati e metadati"
icon: material/tag-remove
description: Utilizza questi strumenti per rimuovere metadati come la posizione GPS e altre informazioni identificative dalle foto e dai file che condividi.
cover: data-redaction.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-search: Esposizione pubblica](basics/common-threats.md#limiting-public-information ""){.pg-green}

Condividendo dei file, assicurati di rimuovere i metadati associati. I file immagine includono comunemente dati [Exif](https://en.wikipedia.org/wiki/Exif). Talvolta, le foto, includono persino le coordinate GPS nei metadati del file.

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Non dovresti **mai** utilizzare la sfocatura per nascondere [il testo nelle immagini] (https://bishopfox.com/blog/unredacter-tool-never-pixelation). If you want to redact text in an image, you should draw a box over the text.

</div>

## MAT2

<div class="admonition recommendation" markdown>

![MAT2 logo](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2** is free, cross-platform software which allows you to remove metadata from image, audio, torrent, and document file types. Fornisce sia uno strumento a riga di comando che un'interfaccia utente grafica tramite un'estensione per [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin), il gestore file predefinito di [KDE](https://kde.org/it/).

On Linux, you can use [Metadata Cleaner](https://gitlab.com/rmnvgr/metadata-cleaner), a third-party graphical tool powered by MAT2 that's [available on Flathub](https://flathub.org/apps/details/fr.romainvigier.MetadataCleaner).

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

![Logo di ExifEraser](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser** è un'applicazione moderna e priva di permessi, per cancellare i metadati delle immagini, per Android.

Attualmente supporta file JPEG, PNG e WebP.

[:octicons-repo-16: Repository](https://github.com/Tommy-Geenexus/exif-eraser){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Tommy-Geenexus/exif-eraser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.none.tom.exiferaser)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/com.none.tom.exiferaser)
- [:simple-github: GitHub](https://github.com/Tommy-Geenexus/exif-eraser/releases)

</details>

</div>

I metadati cancellati dipendono dal tipo di file dell'immagine:

- **JPEG**: i metadati del profilo ICC, Exif, Risorse dell'Immagine Photoshop e XMP/ExtendedXMP saranno cancellati se esistenti.
- **PNG**: i metadati del profilo ICC, Exif e XMP saranno cancellati se esistenti.
- **WebP**: i metadati del profilo ICC, Exif e XMP saranno cancellati se esistenti.

Dopo l'elaborazione delle immagini, ExifEraser fornisce un rapporto completo su cosa è stato rimosso esattamente da ogni immagine.

L'applicazione offre diversi modi per cancellare i metadati dalle immagini. Nello specifico:

- È possibile condividere un'immagine da un'altra applicazione con ExifEraser.
- Tramite l'app stessa, puoi selezionare un'immagine singola, più immagini o persino un'intera cartella.
- È dotata di un'opzione "Fotocamera" che utilizza l'app fotocamera del sistema operativo per scattare una foto e poi ne rimuove i metadati.
- Consente di trascinare le foto da un'altra applicazione in ExifEraser quando entrambe sono aperte in modalità split-screen.
- Infine, consente di incollare un'immagine dagli appunti.

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
<p class="admonition-title">Eliminazione di dati da una directory di file</p>

```bash
exiftool -all= *.file_extension
```

</div>

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

- Le applicazioni sviluppate per sistemi operativi open source devono essere open source.
- Le applicazioni devono essere gratuite e non devono includere pubblicità o altre limitazioni.
