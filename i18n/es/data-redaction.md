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

**MAT2** es un software gratuito y multiplataforma que permite eliminar metadatos de archivos de imagen, audio, torrent y documentos. Proporciona tanto una herramienta de línea de comandos como una interfaz gráfica de usuario a través de una extensión para [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin), el gestor de archivos por defecto de [KDE](https://kde.org).

[:octicons-repo-16: Repositorio](https://0xacab.org/jvoisin/mat2){ .md-button .md-button--primary }
[:octicons-info-16:](https://0xacab.org/jvoisin/mat2/-/blob/master/README.md){ .card-link title="Documentación" }
[:octicons-code-16:](https://0xacab.org/jvoisin/mat2){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:fontawesome-brands-windows: Windows](https://pypi.org/project/mat2#metadata-and-privacy)
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

[:octicons-repo-16: Repositorio](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#description){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/Tommy-Geenexus/exif-eraser){ .card-link title="Código Fuente" }

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

## Atajos (iOS y macOS)

En iOS y macOS, puedes eliminar los metadatos de las imágenes sin utilizar ninguna aplicación de terceros creando un [**atajo**](https://apps.apple.com/app/id915249334) para este fin. Aquí tienes un atajo de ejemplo que puedes descargar para usarlo tal cual:

[:material-tag-minus: Eliminar Metadatos de Imagen](https://icloud.com/shortcuts/fb774ddb7b5b4296871776c67ac0fff9 ""){.md-button}

También puedes utilizarlo como modelo para tu propio atajo; solo tienes que asegurarte de que la opción **Conservar Metadatos** de la acción **Convertir** no esté marcada. Una vez añadido, puedes acceder al atajo en la hoja de compartir que aparece al seleccionar el botón :octicons-share-24: Compartir. Puedes seleccionar varias imágenes e invocar el atajo para eliminar sus metadatos a la vez.

Este atajo elimina metadatos como la ubicación, el modelo de dispositivo, el modelo de objetivo y otra información de la cámara. También establece la fecha de creación de la imagen en el momento en que se utilizó el acceso directo.

## ExifTool (CLI)

<div class="admonition recommendation" markdown>

![ExifTool logo](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool** es la biblioteca original de Perl y la aplicación de línea de comandos para leer, escribir y editar metainformación (Exif, IPTC, XMP, y más) en una amplia variedad de formatos de archivo (JPEG, TIFF, PNG, PDF, RAW, y más).

A menudo es un componente de otras aplicaciones de eliminación de Exif y se encuentra en la mayoría de los repositorios de distribución de Linux.

[:octicons-home-16: Página Principal](https://exiftool.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://exiftool.org/faq.html){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/exiftool/exiftool){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://exiftool.org/#donate){ .card-link title="Contribuir" }

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
