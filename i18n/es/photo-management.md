---
title: Gestión de Fotografías
icon: material/image
description: Herramientas de gestión de fotos para mantener tus fotos personales a salvo de las miradas indiscretas de los proveedores de almacenamiento en la nube y de otros accesos no autorizados.
cover: photo-management.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-bug-outline: Ataques pasivos](basics/common-threats.md#security-and-privacy){ .pg-orange }
- [:material-server-network: Proveedores de Servicios](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

La mayoría de las soluciones de **gestión de fotografías en la nube**, como Google Photos, Flickr y Amazon Photos, no protegen tus fotos contra el acceso del propio proveedor de almacenamiento en la nube. Estas opciones mantienen la privacidad de tus fotos personales y te permiten compartirlas solo con familiares y personas de confianza.

## Ente Photos

<div class="admonition recommendation" markdown>

![Ente logo](assets/img/photo-management/ente.svg#only-light){ align=right }
![Ente logo](assets/img/photo-management/ente-dark.svg#only-dark){ align=right }

**Ente Photos** es un servicio de copia de seguridad cifrada de fotos de extremo a extremo que admite copias de seguridad automáticas en iOS y Android. Su código es totalmente abierto, tanto en el lado del cliente como en el del servidor. También es [autoalojable](https://github.com/ente-io/ente/tree/main/server#self-hosting). The free plan offers 10 GB of storage as long as you use the service at least once a year.

[:octicons-home-16: Página Principal](https://ente.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://ente.io/faq){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/ente-io/ente){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.photos)
- [:simple-android: Android](https://ente.io/download)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1542026904)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=photos)
- [:fontawesome-brands-windows: Windows](https://ente.io/download)
- [:simple-apple: macOS](https://ente.io/download)
- [:simple-linux: Linux](https://ente.io/download)
- [:octicons-globe-16: Web](https://web.ente.io)

</details>

</div>

Ente Photos se sometió a una [auditoría por Cure53](https://ente.io/blog/cryptography-audit) en marzo de 2023 y por [Fallible](https://ente.io/reports/Fallible-Audit-Report-19-04-2023.pdf) en abril de 2023.

## Stingle

<div class="admonition recommendation" markdown>

![Stingle logo](assets/img/photo-management/stingle.png#only-light){ align=right }
![Stingle logo](assets/img/photo-management/stingle-dark.png#only-dark){ align=right }

**Stingle** es una aplicación de galería y cámara con funciones integradas de copia de seguridad cifrada de extremo a extremo y de sincronización para tus fotos y vídeos. Storage starts at 1 GB for free accounts on their cloud, or you can host your own Stingle API server for total independence.

[:octicons-home-16: Página Principal](https://stingle.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://stingle.org/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://stingle.org/faq){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/stingle){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.stingle.photos)
- [:simple-android: Android](https://f-droid.org/en/packages/org.stingle.photos)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1582535448)
- [:simple-github: GitHub](https://github.com/stingle/stingle-photos-android/releases)

</details>

</div>

## PhotoPrism

<div class="admonition recommendation" markdown>

![PhotoPrism logo](assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** es una plataforma autoalojable para la gestión de fotos. Permite sincronizar y compartir álbumes y tiene otras muchas [funciones](https://photoprism.app/features). No incluye E2EE, por lo que es mejor alojarlo en un servidor en el que confíes y que esté bajo tu control.

[:octicons-home-16: Página Principal](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>

## Criterios

**Por favor, ten en cuenta que no estamos afiliados a ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

### Requisitos Mínimos

- Los proveedores alojados en la nube deben aplicar cifrado de extremo a extremo.
- Debe ofrecer un plan gratuito o un periodo de prueba.
- Must support TOTP or FIDO2 multifactor authentication, or passkey logins.
- Debe ofrecer una interfaz web que admita funciones básicas de gestión de archivos.
- Debe permitir exportar fácilmente todos los archivos/documentos.
- Debe ser de código abierto.

### Mejor Caso

- Debe tener una auditoría publicada por una tercera parte independiente y de buena reputación.
