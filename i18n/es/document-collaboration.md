---
title: Colaboración en Documentos
icon: material/account-group
description: La mayoría de las paquetes de ofimática en línea no admiten E2EE, lo que significa que el proveedor de la nube tiene acceso a todo lo que haces.
cover: document-collaboration.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-server-network: Proveedores de Servicios](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

La mayoría de las paquetes de ofimática en línea no admiten E2EE, lo que significa que el proveedor de la nube tiene acceso a todo lo que haces. La política de privacidad del proveedor puede proteger legalmente tus derechos, pero no establece limitaciones técnicas de acceso.

## Plataformas de Colaboración

### Nextcloud

<div class="admonition recommendation" markdown>

![Nextcloud logo](assets/img/document-collaboration/nextcloud.svg){ align=right }

**Nextcloud** es un conjunto de programas cliente-servidor gratuitos y de código abierto para crear tus propios servicios de alojamiento de archivos en un servidor privado que tú controlas.

[:octicons-home-16: Página Principal](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

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

### CryptPad

<div class="admonition recommendation" markdown>

![CryptPad logo](assets/img/document-collaboration/cryptpad.svg){ align=right }

**CryptPad** es una alternativa privada a las herramientas ofimáticas más populares. Todos los contenidos de este servicio web están cifrados de extremo a extremo y pueden compartirse fácilmente con otros usuarios. [:material-star-box: Read our latest CryptPad review.](https://www.privacyguides.org/articles/2025/02/07/cryptpad-review)

[:octicons-home-16: Página Principal](https://cryptpad.fr){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptpad.fr/pad/#/2/pad/view/GcNjAWmK6YDB3EO2IipRZ0fUe89j43Ryqeb4fjkjehE){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://docs.cryptpad.fr){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://opencollective.com/cryptpad){ .card-link title=Contribuir }

</details>

</div>

### Criterios

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

#### Requisitos Mínimos

En general, definimos las plataformas de colaboración como paquetes completos que razonablemente podrían actuar como sustituto de Google Drive.

- Debe ser de código abierto.
- Debe hacer que los archivos sean accesibles a través de WebDAV a menos que sea imposible debido al E2EE.
- Debe tener clientes de sincronización para Linux, macOS y Windows.
- Debe soportar la edición de documentos y hojas de cálculo.
- Debe permitir la colaboración documental en tiempo real.
- Debe admitir la exportación de documentos a formatos de documento estándar (por ejemplo, ODF).

#### Mejor Caso

Nuestro criterio del mejor caso representa lo que nos gustaría ver del proyecto perfecto en esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Debe almacenar los archivos en un sistema de archivos convencional.
- Should support TOTP or FIDO2 multifactor authentication support, or passkey logins.
