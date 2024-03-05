---
meta_title: "Remove PII with Metadata Scrubbers and Data Redaction Tools - Privacy Guides"
title: "Data and Metadata Redaction"
icon: material/tag-remove
description: Use these tools to remove metadata like GPS location and other identifying information from photos and files you share.
cover: data-redaction.webp
---

Lorsque vous partagez des fichiers, veillez à supprimer les métadonnées associées. Les fichiers d'image comprennent généralement des données [Exif](https://en.wikipedia.org/wiki/Exif) . Les photos comportent parfois même des coordonnées GPS dans les métadonnées du fichier.

## Bureau

### MAT2

<div class="admonition recommendation" markdown>

![Logo MAT2](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2** est un logiciel gratuit, qui permet de supprimer les métadonnées des types de fichiers image, audio, torrent et document. Il fournit à la fois un outil en ligne de commande et une interface utilisateur graphique via une extension pour [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin), le gestionnaire de fichiers par défaut de [KDE](https://kde.org).

Sous Linux, un outil graphique tiers [Metadata Cleaner](https://gitlab.com/rmnvgr/metadata-cleaner) fonctionnant avec MAT2 existe et est [disponible sur Flathub](https://flathub.org/apps/details/fr.romainvigier.MetadataCleaner).

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

## Mobile

### ExifEraser (Android)

<div class="admonition recommendation" markdown>

![Logo ExifEraser](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser** est une application moderne d'effacement des métadonnées d'image sans autorisation pour Android.

Il prend actuellement en charge les fichiers JPEG, PNG et WebP.

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

Les métadonnées qui sont effacées dépendent du type de fichier de l'image :

- **JPEG**: Les métadonnées ICC Profile, Exif, Photoshop Image Resources et XMP/ExtendedXMP seront effacées si elles existent.
- **PNG**: Les métadonnées ICC Profile, Exif et XMP seront effacées si elles existent.
- **WebP**: les métadonnées ICC Profile, Exif et XMP seront effacées si elles existent.

Après avoir traité les images, ExifEraser vous fournit un rapport complet sur ce qui a été exactement supprimé de chaque image.

L'application offre plusieurs façons d'effacer les métadonnées des images. À savoir :

- Vous pouvez partager une image depuis une autre application avec ExifEraser.
- Par l'intermédiaire de l'application elle-même, vous pouvez sélectionner une seule image, plusieurs images à la fois, ou même un répertoire entier.
- Elle comporte une option "Appareil photo", qui utilise l'application appareil photo de votre système d'exploitation pour prendre une photo, puis en supprime les métadonnées.
- Elle vous permet de faire glisser des photos d'une autre application dans ExifEraser lorsque les deux sont ouvertes en mode écran partagé.
- Enfin, elle vous permet de coller une image à partir de votre presse-papiers.

### Metapho (iOS)

<div class="admonition recommendation" markdown>

![Logo Metapho](assets/img/data-redaction/metapho.jpg){ align=right }

Metapho est une visionneuse simple et propre pour les métadonnées des photos telles que la date, le nom du fichier, la taille, le modèle d'appareil photo, la vitesse d'obturation et le lieu.

[:octicons-home-16: Homepage](https://zininworks.com/metapho){ .md-button .md-button--primary }
[:octicons-eye-16:](https://zininworks.com/privacy/){ .card-link title="Privacy Policy" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/us/app/metapho/id914457352)

</details>

</div>

### PrivacyBlur

<div class="admonition recommendation" markdown>

![Logo PrivacyBlur](assets/img/data-redaction/privacyblur.svg){ align=right }

**PrivacyBlur** est une application gratuite qui permet de brouiller les parties sensibles des photos avant de les partager en ligne.

[:octicons-home-16: Homepage](https://privacyblur.app/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://privacyblur.app/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/MATHEMA-GmbH/privacyblur#readme){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/MATHEMA-GmbH/privacyblur){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.mathema.privacyblur)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/privacyblur/id1536274106)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Vous ne devez **jamais** utiliser le flou pour expurger [du texte dans les images](https://bishopfox.com/blog/unredacter-tool-never-pixelation). Si vous voulez expurger du texte dans une image, dessinez une case sur le texte. Pour cela, nous vous suggérons [Pocket Paint](https://github.com/Catrobat/Paintroid) ou [Imagepipe](https://codeberg.org/Starfish/Imagepipe).

</div>

## Ligne de commande

### ExifTool

<div class="admonition recommendation" markdown>

![Logo ExifTool](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool** est la bibliothèque perl originale et l'application en ligne de commande pour lire, écrire et modifier les méta-informations (Exif, IPTC, XMP, etc.) dans une grande variété de formats de fichiers (JPEG, TIFF, PNG, PDF, RAW, etc.).

Elle est souvent un composant d'autres applications de suppression d'Exif et se trouve dans les dépôts de la plupart des distributions Linux.

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

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

<div class="admonition example" markdown>
<p class="admonition-title">Cette section est nouvelle</p>

Nous travaillons à l'établissement de critères définis pour chaque section de notre site, et celles-ci peuvent être sujet à changement. Si vous avez des questions sur nos critères, veuillez [poser la question sur notre forum](https://discuss.privacyguides.net/latest) et ne supposez pas que nous n'avons pas pris en compte un élément dans nos recommandations s'il ne figure pas dans la liste. De nombreux facteurs sont pris en compte et discutés lorsque nous recommandons un projet, et la documentation de chacun d'entre eux est en cours.

</div>

- Les applications développées pour des systèmes d'exploitation open source doivent être open source.
- Les applications doivent être gratuites et ne doivent pas comporter de publicités ou d'autres limitations.
