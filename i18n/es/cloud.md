---
meta_title: "Los Mejores Proveedores de Almacenamiento en la Nube Privado y Seguro - Privacy Guides"
title: "Almacenamiento en la Nube"
icon: material/file-cloud
description: Muchos proveedores de almacenamiento en la nube exigen que confíes plenamente en que no mirarán tus archivos. Estas son alternativas privadas.
cover: cloud.webp
---

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: Ataques pasivos](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Proveedores de servicios](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Many **cloud storage providers** require your full trust that they will not look at your files. Las alternativas enumeradas a continuación eliminan la necesidad de confianza mediante la implementación de E2EE seguros.

Si estas alternativas no se ajustan a tus necesidades, te sugerimos que busques utilizar un software de encriptación como [Cryptomator](encryption.md#cryptomator-cloud) con otro proveedor en la nube. Utilizar Cryptomator junto con **cualquier** proveedor de la nube(incluidos estos) puede ser una buena idea para reducir el riesgo de fallos de cifrado en los clientes nativos de un proveedor.

<details class="admonition info" markdown>
<summary>¿Buscando Nextcloud?</summary>

Nextcloud is [still a recommended tool](document-collaboration.md#nextcloud) for self-hosting a file management suite, however we do not recommend third-party Nextcloud storage providers at the moment, because we do [not recommend](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) Nextcloud's built-in E2EE functionality for home users.

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Proton Drive logo](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive** is an encrypted cloud storage provider from the popular encrypted email provider [Proton Mail](email.md#proton-mail). The initial free storage is limited to 2GB, but with the completion of certain steps, additional storage can be obtained up to 5GB.

[:octicons-home-16: Homepage](https://proton.me/drive){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/drive/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)
- [:fontawesome-brands-windows: Windows](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

The Proton Drive web application has been independently audited by Securitum in [2021](https://proton.me/community/open-source).

Los nuevos clientes móviles de Proton Drive aún no han sido auditados públicamente por terceros.

## Tresorit

<div class="admonition recommendation" markdown>

![Logo de Tresorit](assets/img/cloud/tresorit.svg){ align=right }

**Tresorit** es un proveedor suizo-húngaro de almacenamiento cifrado en la nube fundado en 2011. Tresorit es propiedad de Swiss Post, el servicio postal nacional de Suiza.

[:octicons-home-16: Homepage](https://tresorit.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tresorit.com/legal/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.tresorit.com){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Downloads</summary>

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
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): Pruebas de Penetración por Ernst & Young.
    - En esta revisión se analizó el código fuente completo de Tresorit y se validó que la implementación coincide con los conceptos descritos en el [libro blanco](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf) de Tresorit.
    - Ernst & Young probó además los clientes web, móvil y de escritorio: "Los resultados de las pruebas no encontraron ninguna desviación de las afirmaciones de confidencialidad de datos de Tresorit".

They have also received the Digital Trust Label, a certification from the [Swiss Digital Initiative](https://efd.admin.ch/en/swiss-digital-initiative-en) which requires passing [35 criteria](https://swiss-digital-initiative.org/criteria) related to security, privacy, and reliability.

## Peergos

<div class="admonition recommendation" markdown>

![Peergos logo](assets/img/cloud/peergos.svg){ align=right }

**Peergos** es un protocolo descentralizado y una plataforma de código abierto para almacenamiento, redes sociales y aplicaciones. Proporciona un espacio seguro y privado donde los usuarios pueden almacenar, compartir y ver sus fotos, vídeos, documentos, etc. Peergos protege tus archivos con cifrado cuántico resistente de extremo a extremo y garantiza que todos los datos sobre tus archivos permanezcan privados. It is built on top of [IPFS (InterPlanetary File System)](https://ipfs.tech), a peer-to-peer architecture that protects against [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }.

[:octicons-home-16: Homepage](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://book.peergos.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-globe-16: Web](https://peergos.net)
- [:fontawesome-brands-windows: Windows](https://github.com/Peergos/web-ui/releases)
- [:simple-apple: macOS](https://github.com/Peergos/web-ui/releases)
- [:simple-linux: Linux](https://github.com/Peergos/web-ui/releases)

</details>

</div>

Peergos is primarily a web app, but you can self-host the server either as a local cache for your remote Peergos account, or as a standalone storage server which negates the need to register for a remote account and subscription. El servidor Peergos es un archivo `.jar`, lo que significa que debes tener instalado en tu máquina Java 17+ Runtime Environmen ([descarga de OpenJDK](https://azul.com/downloads)) para que funcione.

Ejecutar una versión local de Peergos junto con una cuenta registrada en su servicio alojado de pago te permite acceder a tu almacenamiento Peergos sin depender de DNS o autoridades de certificación TLS, y mantener una copia de seguridad de tus datos en su nube. La experiencia del usuario debería ser la misma tanto si ejecutas su servidor de escritorio como si utilizas su interfaz web alojada.

Peergos fue [auditado](https://cure53.de/pentest-report_peergos.pdf) por Cure53 en septiembre de 2019, y todos los problemas encontrados se solucionaron posteriormente.

An Android app is not available but it is [in the works](https://discuss.privacyguides.net/t/peergos-private-storage-sharing-social-media-and-application-platform/11825/25). La solución actual consiste en utilizar [la PWA](https://peergos.net) móvil en su lugar.

## Criterios

**Por favor, ten en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

### Requisitos Mínimos

- Debe aplicar el cifrado de extremo a extremo.
- Debe ofrecer un plan gratuito o un periodo de prueba.
- Must support TOTP or FIDO2 multi-factor authentication, or passkey logins.
- Debe ofrecer una interfaz web que admita funciones básicas de gestión de archivos.
- Debe permitir exportar fácilmente todos los archivos/documentos.

### Mejor Caso

Nuestro criterio del mejor caso representa lo que nos gustaría ver del proyecto perfecto en esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Los clientes deben ser de código abierto.
- Los clientes deben ser auditados en su totalidad por un tercero independiente.
- Debe ofrecer clientes nativos para Linux, Android, Windows, macOS e iOS.
    - Estos clientes deben integrarse con las herramientas nativas del sistema operativo para los proveedores de almacenamiento en la nube, como la integración de la aplicación Files en iOS, o la funcionalidad DocumentsProvider en Android.
- Debe permitir compartir archivos fácilmente con otros usuarios.
- Debe ofrecer al menos funciones básicas de previsualización y edición de archivos en la interfaz web.

[^1]: [El cumplimiento de la norma ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001):2013 se refiere al sistema de gestión de la seguridad de la información de la empresa [](https://en.wikipedia.org/wiki/Information_security_management) y abarca la venta, el desarrollo, el mantenimiento y la asistencia de sus servicios en la nube.
