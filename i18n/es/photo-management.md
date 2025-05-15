---
title: Gestión de Fotografías
icon: material/image
description: These photo management tools keep your personal photos safe from the prying eyes of cloud storage providers and other unauthorized parties.
cover: photo-management.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-bug-outline: Ataques pasivos](basics/common-threats.md#security-and-privacy){ .pg-orange }
- [:material-server-network: Proveedores de Servicios](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

La mayoría de las soluciones de **gestión de fotografías en la nube**, como Google Photos, Flickr y Amazon Photos, no protegen tus fotos contra el acceso del propio proveedor de almacenamiento en la nube. Estas opciones mantienen la privacidad de tus fotos personales y te permiten compartirlas solo con familiares y personas de confianza.

## Ente Photos

<div class="admonition recommendation" markdown>

![Ente logo](assets/img/photo-management/ente.svg){ align=right }

**Ente Photos** es un servicio de copia de seguridad cifrada de fotos de extremo a extremo que admite copias de seguridad automáticas en iOS y Android. Their code is fully open source, both on the client side and on the server side. También es [autoalojable](https://github.com/ente-io/ente/tree/main/server#self-hosting).

The free plan offers 5 GB of storage as long as you use the service at least once a year.

[:octicons-home-16: Homepage](https://ente.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ente.io/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ente-io/ente){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.photos)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1542026904)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=photos)
- [:simple-android: Android](https://ente.io/download)
- [:fontawesome-brands-windows: Windows](https://ente.io/download)
- [:simple-apple: macOS](https://ente.io/download)
- [:simple-linux: Linux](https://ente.io/download)
- [:octicons-browser-16: Web](https://web.ente.io)

</details>

</div>

Ente Photos underwent an [audit by Cure53](https://ente.io/blog/cryptography-audit) in March 2023 and by [Fallible](https://ente.io/reports/Fallible-Audit-Report-19-04-2023.pdf) in April 2023.

## Stingle

<div class="admonition recommendation" markdown>

![Stingle logo](assets/img/photo-management/stingle.png#only-light){ align=right }
![Stingle logo](assets/img/photo-management/stingle-dark.png#only-dark){ align=right }

**Stingle** is a gallery and camera application with built-in, E2EE backup and sync functionality for your photos and videos.

Storage starts at 1 GB for free accounts on their cloud, or you can host your own Stingle API server for total independence.

[:octicons-home-16: Homepage](https://stingle.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://stingle.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://stingle.org/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/stingle){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.stingle.photos)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1582535448)
- [:simple-github: GitHub](https://github.com/stingle/stingle-photos-android/releases)

</details>

</div>

## PhotoPrism

<div class="admonition recommendation" markdown>

![PhotoPrism logo](assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** is a self-hostable platform for managing photos. It supports album syncing and sharing as well as a variety of other [features](https://photoprism.app/features). It does not include E2EE, so it's best hosted on a server that you trust and is under your control.

[:octicons-home-16: Homepage](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>

## Criterios

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

### Requisitos Mínimos

- Cloud-hosted providers must enforce E2EE.
- Debe ofrecer un plan gratuito o un periodo de prueba.
- Must support TOTP or FIDO2 multifactor authentication, or passkey logins.
- Debe ofrecer una interfaz web que admita funciones básicas de gestión de archivos.
- Debe permitir exportar fácilmente todos los archivos/documentos.
- Debe ser de código abierto.

### Mejor Caso

- Should have a published audit from a reputable, independent third party.
