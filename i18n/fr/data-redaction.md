---
meta_title: "Supprimer les DCP à l'aide de nettoyeurs de métadonnées et d'outils de suppression des données - Privacy Guides"
title: "Rédaction de données et de métadonnées"
icon: material/tag-remove
description: Utilisez ces outils pour supprimer les métadonnées telles que la localisation GPS et d'autres informations d'identification des photos et des fichiers que vous partagez.
cover: data-redaction.webp
---

<small>Protège contre la (les) menace(s) suivante(s) :</small>

- [:material-account-search: Exposition publique](basics/common-threats.md#limiting-public-information ""){.pg-green}

Lorsque vous partagez des fichiers, veillez à supprimer les métadonnées associées. Les fichiers d'image comprennent généralement des données [Exif](https://en.wikipedia.org/wiki/Exif) . Les photos comportent parfois même des coordonnées GPS dans les métadonnées du fichier.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Vous ne devez **jamais** utiliser le flou pour expurger [du texte dans les images](https://bishopfox.com/blog/unredacter-tool-never-pixelation). Si vous voulez expurger du texte dans une image, vous devriez dessiner une case sur le texte.

</div>

## MAT2

<div class="admonition recommendation" markdown>

![MAT2 logo](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2** est gratuit, logiciel multi-plateforme qui vous permet de supprimer les métadonnées des types d'image, d'audio, de torrent et de fichiers de documents. Il fournit à la fois un outil en ligne de commande et une interface utilisateur graphique via une extension pour [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin), le gestionnaire de fichiers par défaut de [KDE](https://kde.org).

[:octicons-repo-16: Dépôt](https://0xacab.org/jvoisin/mat2){ .md-button .md-button--primary }
[:octicons-info-16:](https://0xacab.org/jvoisin/mat2/-/blob/master/README.md){ .card-link title=Documentation}
[:octicons-code-16:](https://0xacab.org/jvoisin/mat2){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:fontawesome-brands-windows: Windows](https://pypi.org/project/mat2#metadata-and-privacy)
- [:simple-apple: macOS](https://0xacab.org/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: Linux](https://pypi.org/project/mat2)
- [:octicons-globe-16: Web](https://0xacab.org/jvoisin/mat2#web-interface)

</details>

</div>

## ExifEraser (Android)

<div class="admonition recommendation" markdown>

![Logo ExifEraser](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser** est une application moderne d'effacement des métadonnées d'image sans autorisation pour Android.

Il supporte actuellement les fichiers JPEG, PNG, et WebP.

[:octicons-repo-16: Dépôt](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#description){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/Tommy-Geenexus/exif-eraser){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

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

## Raccourcis (iOS & macOS)

Sur iOS et macOS, vous pouvez supprimer les métadonnées des images sans utiliser d'application tierce en créant un [**raccourci**](https://apps.apple.com/app/id915249334) à cet effet. Voici un exemple de raccourci que vous pouvez télécharger pour l'utiliser comme suit :

[:material-tag-minus: Nettoyer les métadonnées de l'image](https://icloud.com/shortcuts/fb774ddb7b5b4296871776c67ac0fff9 ""){.md-button}

Vous pouvez également l'utiliser comme modèle pour votre propre raccourci ; assurez-vous simplement que l'option **Préserver les métadonnées** sous l'action **Convertir** n'est pas cochée. Une fois ajouté, vous pouvez accéder au raccourci dans la feuille de partage qui apparaît lorsque vous sélectionnez le bouton :octicons-share-24: Partage. Vous pouvez sélectionner plusieurs images et appeler le raccourci pour supprimer leurs métadonnées en même temps.

Ce raccourci supprime les métadonnées telles que l'emplacement, le modèle de l'appareil, le modèle de l'objectif et d'autres informations sur la caméra. Il définit également la date de création de l'image à l'heure où le raccourci a été utilisé.

## ExifTool (CLI)

<div class="admonition recommendation" markdown>

![ExifTool logo](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool** est la bibliothèque Perl originale et l'application en ligne de commande pour la lecture, écrire et éditer des méta-informations (Exif, IPTC, XMP et plus) dans une grande variété de formats de fichiers (JPEG, TIFF, PNG, PDF, RAW et plus).

Il fait souvent partie d'autres applications de suppression d'Exif et se trouve dans les dépôts de la plupart des distributions Linux.

[:octicons-home-16: Page d'accueil](https://exiftool.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://exiftool.org/faq.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/exiftool/exiftool){ .card-link title="Code source" }
[:octicons-heart-16:](https://exiftool.org/#donate){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:fontawesome-brands-windows: Windows](https://exiftool.org)
- [:simple-apple: macOS](https://exiftool.org)
- [:simple-linux: Linux](https://exiftool.org)

</details>

</div>

<div class="admonition example" markdown>
<p class="admonition-title">Suppression des données d'un répertoire de fichiers</p>

```bash
exiftool -all= *.file_extension
```

</div>

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

- Les applications développées pour des systèmes d'exploitation open source doivent être open source.
- Les applications doivent être gratuites et ne doivent pas comporter de publicités ou d'autres limitations.
