---
meta_title: "Los Mejores Proveedores de Almacenamiento en la Nube Privado y Seguro - Privacy Guides"
title: Almacenamiento en la Nube
icon: material/file-cloud
description: Muchos proveedores de almacenamiento en la nube exigen que confíes plenamente en que no mirarán tus archivos. Estas son alternativas privadas.
cover: cloud.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-bug-outline: Ataques pasivos](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Proveedores de servicios](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Muchos **proveedores de almacenamiento en la nube** exigen que confíes plenamente en que no mirarán tus archivos. Las alternativas enumeradas a continuación eliminan la necesidad de confianza mediante la implementación de un cifrado de extremo a extremo seguro.

Si estas alternativas no se ajustan a tus necesidades, te sugerimos que busques utilizar un software de encriptación como [Cryptomator](encryption.md#cryptomator-cloud) con otro proveedor en la nube. Utilizar Cryptomator junto con **cualquier** proveedor de la nube(incluidos estos) puede ser una buena idea para reducir el riesgo de fallos de cifrado en los clientes nativos de un proveedor.

<details class="admonition info" markdown>
<summary>¿Buscando Nextcloud?</summary>

For more technical readers, Nextcloud is [still a recommended tool](self-hosting/file-management.md#nextcloud) for self-hosting a file management suite, however we do not recommend third-party Nextcloud storage providers at the moment, because we do [not recommend](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) Nextcloud's built-in E2EE functionality for home users.

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Proton Drive logo](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive** es un proveedor de almacenamiento cifrado en la nube del popular proveedor de correo electrónico cifrado [Proton Mail](email.md#proton-mail).

El almacenamiento gratuito inicial está limitado a 2 GB, pero al completar [ciertos pasos](https://proton.me/support/more-free-storage-existing-users), se puede obtener almacenamiento adicional de hasta 5 GB.

[:octicons-home-16: Página Principal](https://proton.me/drive){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/drive/privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)
- [:fontawesome-brands-windows: Windows](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

La aplicación web de Proton Drive ha sido auditada de forma independiente por Securitum en [2021](https://proton.me/community/open-source), pero los nuevos clientes móviles aún no han sido auditados públicamente por un tercero.

## Tresorit

<div class="admonition recommendation" markdown>

![Logo de Tresorit](assets/img/cloud/tresorit.svg){ align=right }

**Tresorit** es un proveedor suizo-húngaro de almacenamiento cifrado en la nube fundado en 2011. Tresorit es propiedad de Swiss Post, el servicio postal nacional de Suiza.

[:octicons-home-16: Página Principal](https://tresorit.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tresorit.com/legal/privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://support.tresorit.com){ .card-link title="Documentación" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.tresorit.mobile)
- [:simple-appstore: App Store](https://apps.apple.com/app/id722163232)
- [:fontawesome-brands-windows: Windows](https://tresorit.com/download)
- [:simple-apple: macOS](https://tresorit.com/download)
- [:simple-linux: Linux](https://tresorit.com/download)

</details>

</div>

Tresorit ha recibido varias auditorías de seguridad independientes:

- [2022](https://tresorit.com/blog/tresorit-receives-iso-27001-certification): ISO/IEC 27001:2013[^1][Certificación de](https://certipedia.com/quality_marks/9108644476) Conformidad por TÜV Rheinland InterCert Kft
- [2021](https://tresorit.com/blog/fresh-penetration-testing-confirms-tresorit-security): Pruebas de Penetración por Computest
    - Esta revisión evaluó la seguridad del cliente web Tresorit, la aplicación Android, la aplicación Windows y la infraestructura asociada.
    - Computest descubrió dos vulnerabilidades que ya han sido resueltas.
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): Pruebas de penetración por Ernst & Young.
    - En esta revisión se analizó el código fuente completo de Tresorit y se validó que la implementación coincide con los conceptos descritos en el [libro blanco](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf) de Tresorit.
    - Ernst & Young probó además los clientes web, móvil y de escritorio. Concluyó:

        > Los resultados de las pruebas no revelaron ninguna desviación con respecto a las afirmaciones de Tresorit sobre la confidencialidad de los datos.

También han recibido el Sello de Confianza Digital, una certificación de la [Swiss Digital Initiative](https://efd.admin.ch/en/swiss-digital-initiative-en) que exige superar [35 criterios](https://swiss-digital-initiative.org/criteria) relacionados con la seguridad, la privacidad y la fiabilidad.

## Peergos

<div class="admonition recommendation" markdown>

![Peergos logo](assets/img/cloud/peergos.svg){ align=right }

**Peergos** es un protocolo descentralizado y una plataforma de código abierto para almacenamiento, redes sociales y aplicaciones. It provides a secure and private space where users can store, share, view and edit their photos, videos, documents, etc. Peergos secures your files with quantum-resistant E2EE and ensures all data about your files remains private.

[:octicons-home-16: Página Principal](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://book.peergos.org){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://github.com/peergos/peergos#support){ .card-link title="Contribuir" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=peergos.android)
- [:simple-github: GitHub](https://github.com/Peergos/web-ui/releases)
- [:fontawesome-brands-windows: Windows](https://peergos.org/download#windows)
- [:simple-apple: macOS](https://peergos.org/download#macos)
- [:simple-linux: Linux](https://peergos.org/download#linux)
- [:octicons-browser-16: Web](https://peergos.net)

</details>

</div>

Peergos se basa en el [Sistema de Archivos Interplanetario (IPFS)](https://ipfs.tech), una arquitectura entre iguales que protege contra [:material-close-outline: la censura](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}.

Peergos has a web app, desktop apps and an Android app and you can also self-host the server. Client, server and command line interface all run from the same binary. There is a sync engine included (accessible via the desktop or android apps) for bi-directionally synchronizing a local folder with a Peergos folder, and a webdav bridge to allow other applications to access your Peergos storage.

Peergos fue [auditado](https://peergos.org/posts/security-audit-2024) en noviembre de 2024 por Radically Open Security y se solucionaron todos los problemas. Anteriormente fueron [auditados](https://cure53.de/pentest-report_peergos.pdf) por Cure53 en junio de 2019, y todos los problemas encontrados se solucionaron posteriormente.

## Criterios

**Por favor, ten en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

### Requisitos Mínimos

- Debe aplicar E2EE.
- Debe ofrecer un plan gratuito o un periodo de prueba.
- Debe ser compatible con la autenticación multifactor TOTP o FIDO2, o con los inicios de sesión con clave de acceso.
- Debe ofrecer una interfaz web que admita funciones básicas de gestión de archivos.
- Debe permitir exportar fácilmente todos los archivos/documentos.

### Mejor Caso

Nuestro criterio del mejor caso representa lo que nos gustaría ver del proyecto perfecto en esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Los clientes deberían ser de código abierto.
- Los clientes deberían ser auditados en su totalidad por un tercero independiente.
- Debería ofrecer clientes nativos para Linux, Android, Windows, macOS e iOS.
    - Estos clientes deberían integrarse con las herramientas nativas del sistema operativo para los proveedores de almacenamiento en la nube, como la integración de la aplicación Files en iOS, o la funcionalidad DocumentsProvider en Android.
- Debería permitir compartir archivos fácilmente con otros usuarios.
- Debería ofrecer al menos funciones básicas de previsualización y edición de archivos en la interfaz web.

[^1]: [El cumplimiento de la norma ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001):2013 se refiere al sistema de gestión de la seguridad de la información de la empresa [](https://en.wikipedia.org/wiki/Information_security_management) y abarca la venta, el desarrollo, el mantenimiento y la asistencia de sus servicios en la nube.
