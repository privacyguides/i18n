---
meta_title: "Eliminar PII con Depuradores de Metadatos y Herramientas de Edición de Datos - Privacy Guides"
title: "Edición de Datos y Metadatos"
icon: material/tag-remove
description: Utiliza estas herramientas para eliminar metadatos como la ubicación GPS y otros datos identificativos de las fotos y archivos que compartas.
cover: data-redaction.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-account-search: Exposición pública](basics/common-threats.md#limiting-public-information ""){.pg-green}

Cuando compartas archivos, asegúrate de remover los metadatos asociados. Archivos de imagen comúnmente incluyen datos [Exif](https://en.wikipedia.org/wiki/Exif). Fotos a veces incluyen hasta coordenadas GPS en los metadatos del archivo.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

No se debe **nunca** utilizar el desenfoque para eliminar [texto en imágenes](https://bishopfox.com/blog/unredacter-tool-never-pixelation). Si deseas eliminar texto en una imagen, dibuja un recuadro sobre el texto.

</div>

## MAT2

<div class="admonition recommendation" markdown>

![MAT2 logo](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2** is free, cross-platform software which allows you to remove metadata from image, audio, torrent, and document file types. Proporciona tanto una herramienta de línea de comandos como una interfaz gráfica de usuario a través de una extensión para [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin), el gestor de archivos por defecto de [KDE](https://kde.org).

[:octicons-repo-16: Repository](https://0xacab.org/jvoisin/mat2){ .md-button .md-button--primary }
[:octicons-info-16:](https://0xacab.org/jvoisin/mat2/-/blob/master/README.md){ .card-link title="Documentation" }
[:octicons-code-16:](https://0xacab.org/jvoisin/mat2){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:fontawesome-brands-windows: Windows](https://pypi.org/project/mat2)
- [:simple-apple: macOS](https://0xacab.org/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: Linux](https://pypi.org/project/mat2)
- [:octicons-globe-16: Web](https://0xacab.org/jvoisin/mat2#web-interface)

</details>

</div>

## ExifEraser (Android)

<div class="admonition recommendation" markdown>

![ExifEraser logo](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser** es una moderna aplicación de borrado de metadatos de imagen sin permisos para Android.

Actualmente admite archivos JPEG, PNG y WebP.

[:octicons-repo-16: Repository](https://github.com/Tommy-Geenexus/exif-eraser){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Tommy-Geenexus/exif-eraser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.none.tom.exiferaser)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/com.none.tom.exiferaser)
- [:simple-github: GitHub](https://github.com/Tommy-Geenexus/exif-eraser/releases)

</details>

</div>

Los metadatos que son eliminados dependen del tipo de archivo de la imagen:

- **JPEG**: Los metadatos ICC Profile, Exif, Photoshop Image Resources and XMP/ExtendedXMP serán eliminados si existen.
- **PNG**: Los metadatos ICC Profile, Exif y XMP serán eliminados si existen.
- **WebP**: Los metadatos ICC Profile, Exif y XMP serán eliminados si existen.

Tras procesar las imágenes, ExifEraser te proporciona un informe completo sobre lo que se ha eliminado exactamente de cada imagen.

La aplicación ofrece múltiples formas de borrar los metadatos de las imágenes. Estas son:

- Puede compartir una imagen de otra aplicación con ExifEraser.
- A través de la propia aplicación, puedes seleccionar una sola imagen, varias imágenes a la vez o incluso un directorio entero.
- Cuenta con una opción de "Cámara", que utiliza la aplicación de cámara de tu sistema operativo para tomar una foto, y luego elimina los metadatos de la misma.
- Te permite arrastrar fotos desde otra aplicación a ExifEraser cuando ambas están abiertas en modo de pantalla dividida.
- Por último, te permite pegar una imagen desde el portapapeles.

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
<summary>Downloads "Descargas"</summary>

- [:fontawesome-brands-windows: Windows](https://exiftool.org)
- [:simple-apple: macOS](https://exiftool.org)
- [:simple-linux: Linux](https://exiftool.org)

</details>

</div>

<div class="admonition example" markdown>
<p class="admonition-title">Borrar datos de un directorio de archivos</p>

```bash
exiftool -all= *.file_extension
```

</div>

## Criterios

**Por favor, ten en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

- Las aplicaciones desarrolladas para sistemas operativos de código abierto deben ser de código abierto.
- Las aplicaciones deben ser gratuitas y no incluir anuncios ni otras limitaciones.
