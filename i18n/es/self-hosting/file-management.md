---
title: Gestión de Archivos
meta_title: "Autoalojamiento de Herramientas de Gestión de Archivos - Privacy Guides"
icon: material/file-multiple-outline
description: Para nuestros lectores más técnicos, el autoalojamiento de las herramientas de gestión de archivos puede proporcionar garantías adicionales de privacidad al tener el máximo control sobre tus datos.
cover: cloud.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-server-network: Proveedores de Servicios](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

Autoalojar tus propias herramientas de **gestión de archivos** podría ser una buena idea para reducir el riesgo de errores de cifrado en los clientes nativos de un proveedor de nube.

## Gestión de Fotografías

### PhotoPrism

<div class="admonition recommendation" markdown>

![PhotoPrism logo](../assets/img/self-hosting/photoprism.svg){ align=right }

**PhotoPrism** es una plataforma para la gestión de fotos. Permite sincronizar y compartir álbumes y tiene otras muchas [funciones](https://photoprism.app/features). No incluye cifrado de extremo a extremo, por lo que es mejor alojarlo en un servidor en el que confíes y que esté bajo tu control.

[:octicons-home-16: Página Principal](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Código Fuente" }

</div>

## Compartir y sincronizar archivos

### FreedomBox

<div class="admonition recommendation" markdown>

![FreedomBox logo](../assets/img/self-hosting/freedombox.svg){ align=right }

**FreedomBox** es un sistema operativo diseñado para ser ejecutado en un [ordenador monoplaca (SBC)](https://en.wikipedia.org/wiki/Single-board_computer). El objetivo es facilitar la configuración de aplicaciones de servidor para casos de uso como compartir archivos.

[:octicons-home-16: Página Principal](https://freedombox.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title="Documentación" }
[:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://freedomboxfoundation.org/donate){ .card-link title="Contribuir" }

</div>

### Nextcloud

<div class="admonition recommendation" markdown>

![Nextcloud logo](../assets/img/self-hosting/nextcloud.svg){ align=right }

**Nextcloud** es un conjunto de programas cliente-servidor gratuitos y de código abierto para crear tus propios servicios de alojamiento de archivos en un servidor privado que tú controlas.

[:octicons-home-16: Página Principal](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title="Contribuir" }

<details class="downloads" markdown><summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
- [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
- [:fontawesome-brands-windows: Windows](https://nextcloud.com/install/#install-clients)
- [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
- [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Peligro</p>

No recomendamos utilizar la [aplicación con cifrado de extremo a extremo](https://apps.nextcloud.com/apps/end_to_end_encryption) para Nextcloud, porque puede causar la pérdida de datos; esta es considerada como altamente experimental y no debe utilizarse en entornos de producción. Por esta razón, no recomendamos proveedores de Nextcloud de terceros.

</div>
