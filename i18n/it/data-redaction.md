---
meta_title: "Rimuovi PII con Scrubber di Metadati e Strumenti di riduzione dei dati - Privacy Guides"
title: "Rimozione di dati e metadati"
icon: material/tag-remove
description: Utilizza questi strumenti per rimuovere metadati come la posizione GPS e altre informazioni identificative dalle foto e dai file che condividi.
cover: data-redaction.webp
---

Condividendo dei file, assicurati di rimuovere i metadati associati. I file immagine includono comunemente dati [Exif](https://en.wikipedia.org/wiki/Exif). Talvolta, le foto, includono persino le coordinate GPS nei metadati del file.

## Desktop

### MAT2

<div class="admonition recommendation" markdown>

![Logo di MAT2](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2** è un software gratuito che consente la rimozione dei metadati da file immagine, audio, torrent e documenti. Fornisce sia uno strumento a riga di comando che un'interfaccia utente grafica tramite un'estensione per [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin), il gestore file predefinito di [KDE](https://kde.org/it/).

Su Linux, esiste uno strumento grafico di terze parti [Metadata Cleaner](https://gitlab.com/rmnvgr/metadata-cleaner) basato su MAT2 ed è [disponibile su Flathub](https://flathub.org/apps/details/fr.romainvigier.MetadataCleaner).

[:octicons-repo-16: Repository](https://0xacab.org/jvoisin/mat2){ .md-button .md-button--primary }
[:octicons-info-16:](https://0xacab.org/jvoisin/mat2/-/blob/master/README.md){ .card-link title=Documentazione}
[:octicons-code-16:](https://0xacab.org/jvoisin/mat2){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-windows11: Windows](https://pypi.org/project/mat2)
- [:simple-apple: macOS](https://0xacab.org/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: Linux](https://pypi.org/project/mat2)
- [:octicons-globe-16: Web](https://0xacab.org/jvoisin/mat2#web-interface)

</details>

</div>

## Mobile

### ExifEraser (Android)

<div class="admonition recommendation" markdown>

![Logo ExifEraser](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser** è un'applicazione moderna e senza permessi per la cancellazione dei metadati delle immagini per Android.

Attualmente supporta file JPEG, PNG e WebP.

[:octicons-repo-16: Repository](https://github.com/Tommy-Geenexus/exif-eraser){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/Tommy-Geenexus/exif-eraser){ .card-link title="Codice sorgente" }

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
- Attraverso l'applicazione stessa, è possibile selezionare una singola immagine, più immagini contemporaneamente o persino un'intera directory.
- È dotata di un'opzione "Fotocamera" che utilizza l'app fotocamera del sistema operativo per scattare una foto e poi ne rimuove i metadati.
- Consente di trascinare le foto da un'altra applicazione in ExifEraser quando entrambe sono aperte in modalità split-screen.
- Infine, consente di incollare un'immagine dagli appunti.

### Metapho (iOS)

<div class="admonition recommendation" markdown>

![Logo di Metapho](assets/img/data-redaction/metapho.jpg){ align=right }

**Metapho** è un visualizzatore semplice e pulito per i metadati delle foto, quali data, nome del file, dimensioni, modello della fotocamera, velocità dell'otturatore e posizione.

[:octicons-home-16: Homepage](https://zininworks.com/metapho){ .md-button .md-button--primary }
[:octicons-eye-16:](https://zininworks.com/privacy/){ .card-link title="Informativa sulla Privacy" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-appstore: App Store](https://apps.apple.com/us/app/metapho/id914457352)

</details>

</div>

### PrivacyBlur

<div class="admonition recommendation" markdown>

![Logo di PrivacyBlur](assets/img/data-redaction/privacyblur.svg){ align=right }

**PrivacyBlur** è un'app gratuita che consente di sfocare le parti sensibili delle immagini, prima di condividerle online.

[:octicons-home-16: Homepage](https://privacyblur.app/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://privacyblur.app/privacy.html){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://github.com/MATHEMA-GmbH/privacyblur#readme){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/MATHEMA-GmbH/privacyblur){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.mathema.privacyblur)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/privacyblur/id1536274106)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Non dovresti **mai** utilizzare la sfocatura per nascondere [il testo nelle immagini] (https://bishopfox.com/blog/unredacter-tool-never-pixelation). Se desideri censurare il testo di un'immagine, disegna un riquadro sopra di esso. A questo scopo, suggeriamo applicazioni come [Pocket Paint](https://github.com/Catrobat/Paintroid).

</div>

## Linea di comando

### ExifTool

<div class="admonition recommendation" markdown>

![Logo di ExifTool](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool** è la libreria perl originale e appliczione di riga di comando per leggere, scrivere e modificare le meta-informazioni (Exif, IPTC, XMP e altre) in un'ampia gamma di formati di file (JPEG, TIFF, PNG, PDF, RAW e altri).

Spesso è usato come un componente di altre applicazioni di rimozione Exif ed è presente nei repository della maggior parte delle distribuzioni Linux.

[:octicons-home-16: Homepage](https://exiftool.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://exiftool.org/faq.html){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/exiftool/exiftool){ .card-link title="Codice sorgente" }
[:octicons-heart-16:](https://exiftool.org/#donate){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-windows11: Windows](https://exiftool.org)
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

<div class="admonition example" markdown>
<p class="admonition-title">Questa sezione è nuova</p>

Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

</div>

- Le applicazioni sviluppate per sistemi operativi open source devono essere open source.
- Le applicazioni devono essere gratuite e non devono includere pubblicità o altre limitazioni.
