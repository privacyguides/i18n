---
title: Aplicaciones Generales
description: Las aplicaciones que se encuentran listadas son exclusivas para Android y están diseñadas para mejorar o reemplazar funcionalidades clave del sistema.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Aplicaciones Generales para Android
    url: ./
  - "@context": http://schema.org
    "@type": MobileApplication
    name: Shelter
    applicationCategory: Utilidades
    operatingSystem: Android
  - "@context": http://schema.org
    "@type": MobileApplication
    name: Secure Camera
    applicationCategory: Utilidades
    operatingSystem: Android
  - "@context": http://schema.org
    "@type": MobileApplication
    name: Secure PDF Viewer
    applicationCategory: Utilidades
    operatingSystem: Android
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-bug-outline: Ataques Pasivos](../basics/common-threats.md#security-and-privacy){ .pg-orange }

En este sitio web recomendamos una amplia variedad de aplicaciones para Android. Las aplicaciones que se encuentran listadas son exclusivas para Android y están diseñadas para mejorar o reemplazar funcionalidades clave del sistema.

### Shelter

If your device is on Android 15 or greater, we recommend using the native [Private Space](../os/android-overview.md#private-space) feature instead, which provides nearly the same functionality without needing to place trust in and grant powerful permissions to a third-party app.

<div class="admonition recommendation" markdown>

![Logo de Shelter](../assets/img/android/shelter.svg){ align=right }

**Shelter** es una aplicación que ayuda con el aprovechamiento de la característica de los perfiles de trabajo para aislar o duplicar aplicaciones en tu dispositivo.

Shelter permite bloquear la búsqueda de contactos entre perfiles y compartir archivos entre los perfiles por medio del gestor de archivos por defecto [(DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).

[:octicons-repo-16: Repositorio](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Código fuente" }
[:octicons-heart-16:](https://patreon.com/PeterCxy){ .card-link title=Contribuir }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Al utilizar Shelter, estás depositando toda tu confianza en su desarrollador, ya que Shelter actúa como [Administrador del Dispositivo](https://developer.android.com/guide/topics/admin/device-admin) para crear el Perfil de Trabajo, y tiene un amplio acceso a los datos almacenados dentro del Perfil de Trabajo.

</div>

Se recomienda Shelter en lugar de [Insular](https://secure-system.gitlab.io/Insular) e [Island](https://github.com/oasisfeng/island), ya que admite [bloqueo de búsqueda de contactos](https://secure-system.gitlab.io/Insular/faq.html).

### Secure Camera

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-account-search: Public Exposure](../basics/common-threats.md#limiting-public-information){ .pg-green }

<div class="admonition recommendation" markdown>

![Secure camera logo](../assets/img/android/secure_camera.svg#only-light){ align=right }
![Secure camera logo](../assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

**Secure Camera** es una aplicación de cámara centrada en la privacidad y la seguridad que puede capturar imágenes, vídeos y códigos QR. Las extensiones del proveedor CameraX (Retrato, HDR, Vista Nocturna, Retoque Facial y Automático) también son compatibles en los dispositivos disponibles.

[:octicons-repo-16: Repositorio](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

Entre las principales características de privacidad se incluyen:

- Eliminación automática de metadatos [Exif](https://es.wikipedia.org/wiki/Exif) (activada por defecto)
- Uso de la nueva API [Media](https://developer.android.com/training/data-storage/shared/media), por lo que no se requieren [permisos de almacenamiento](https://developer.android.com/training/data-storage)
- El permiso de micrófono no es necesario a menos que quieras grabar sonido

<div class="admonition note" markdown>
<p class="admonition-title">Nota</p>

Actualmente no se eliminan los metadatos de los archivos de vídeo, pero está previsto hacerlo.

Los metadatos de orientación de la imagen no se borran. Si activas la localización (en Secure Camera) eso **tampoco** se borrará. Si quieres borrarlo más tarde tendrás que usar una aplicación externa como [ExifEraser](../data-redaction.md#exiferaser-android).

</div>

### Secure PDF Viewer

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-target-account: Ataques Dirigidos](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }

<div class="admonition recommendation" markdown>

![Secure PDF Viewer logo](../assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Secure PDF Viewer logo](../assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

**Secure PDF Viewer** es un visor de PDF basado en [pdf.js](https://en.wikipedia.org/wiki/PDF.js) que no requiere ningún permiso. El PDF se introduce en un [WebView](https://developer.android.com/guide/webapps/webview) [aislado](https://es.wikipedia.org/wiki/Entorno_de_pruebas_\(inform%C3%A1tica\)). Esto significa que no necesita permiso directamente para acceder a contenidos o archivos.

[Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) se utiliza para reforzar que las propiedades JavaScript y de estilo dentro del WebView sean enteramente contenido estático.

[:octicons-repo-16: Repositorio](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Cñodigo Fuente" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## Criterios

**Por favor, ten en cuenta que no estamos afiliados a ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](../about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

- Las aplicaciones de esta página no deben ser aplicables a ninguna otra categoría de software del sitio.
- Las aplicaciones generales deben ampliar o sustituir las funciones básicas del sistema.
- Las aplicaciones deben recibir actualizaciones y mantenimiento periódicos.
