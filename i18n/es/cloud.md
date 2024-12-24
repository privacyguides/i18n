---
meta_title: "Los Mejores Proveedores de Almacenamiento en la Nube Privado y Seguro - Privacy Guides"
title: "Almacenamiento en la Nube"
icon: material/file-cloud
description: Muchos proveedores de almacenamiento en la nube exigen que confíes plenamente en que no mirarán tus archivos. Estas son alternativas privadas.
cover: cloud.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-bug-outline: Ataques pasivos](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Proveedores de servicios](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Muchos **proveedores de almacenamiento en la nube** exigen que confíes plenamente en que no mirarán tus archivos. Las alternativas enumeradas a continuación eliminan la necesidad de confianza mediante la implementación de E2EE seguros.

Si estas alternativas no se ajustan a tus necesidades, te sugerimos que busques utilizar un software de encriptación como [Cryptomator](encryption.md#cryptomator-cloud) con otro proveedor en la nube. Utilizar Cryptomator junto con **cualquier** proveedor de la nube(incluidos estos) puede ser una buena idea para reducir el riesgo de fallos de cifrado en los clientes nativos de un proveedor.

<details class="admonition info" markdown>
<summary>¿Buscando Nextcloud?</summary>

Nextcloud [sigue siendo una herramienta recomendada](document-collaboration.md#nextcloud) para el autoalojamiento de una suite de gestión de archivos, sin embargo no recomendamos proveedores de almacenamiento Nextcloud de terceros por el momento, porque [no recomendamos](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) la funcionalidad E2EE incorporada de Nextcloud para usuarios domésticos.

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Proton Drive logo](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive** es un proveedor de almacenamiento cifrado en la nube del popular proveedor de correo electrónico cifrado [Proton Mail](email.md#proton-mail). The initial free storage is limited to 2GB, but with the completion of [certain steps](https://proton.me/support/more-free-storage-existing-users), additional storage can be obtained up to 5GB.

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

La aplicación web de Proton Drive ha sido auditada de forma independiente por Securitum en [2021](https://proton.me/community/open-source).

Los nuevos clientes móviles de Proton Drive aún no han sido auditados públicamente por terceros.

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
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): Pruebas de Penetración por Ernst & Young.
    - En esta revisión se analizó el código fuente completo de Tresorit y se validó que la implementación coincide con los conceptos descritos en el [libro blanco](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf) de Tresorit.
    - Ernst & Young probó además los clientes web, móvil y de escritorio: "Los resultados de las pruebas no encontraron ninguna desviación de las afirmaciones de confidencialidad de datos de Tresorit".

También han recibido el Digital Trust Label, una certificación de la [Swiss Digital Initiative](https://efd.admin.ch/en/swiss-digital-initiative-en) que exige superar [35 criterios](https://swiss-digital-initiative.org/criteria) relacionados con la seguridad, la privacidad y la fiabilidad.

## Peergos

<div class="admonition recommendation" markdown>

![Peergos logo](assets/img/cloud/peergos.svg){ align=right }

**Peergos** es un protocolo descentralizado y una plataforma de código abierto para almacenamiento, redes sociales y aplicaciones. Proporciona un espacio seguro y privado donde los usuarios pueden almacenar, compartir y ver sus fotos, vídeos, documentos, etc. Peergos protege tus archivos con cifrado cuántico resistente de extremo a extremo y garantiza que todos los datos sobre tus archivos permanezcan privados. Está construido sobre [IPFS (InterPlanetary File System)](https://ipfs.tech), una arquitectura peer-to-peer que protege contra la [:material-close-outline: Censura](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }.

[:octicons-home-16: Página Principal](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://book.peergos.org){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:octicons-globe-16: Web](https://peergos.net)
- [:fontawesome-brands-windows: Windows](https://github.com/Peergos/web-ui/releases)
- [:simple-apple: macOS](https://github.com/Peergos/web-ui/releases)
- [:simple-linux: Linux](https://github.com/Peergos/web-ui/releases)

</details>

</div>

Peergos es principalmente una aplicación web, pero puedes alojar tú mismo el servidor, ya sea como caché local para tu cuenta Peergos remota o como servidor de almacenamiento independiente, lo que evita la necesidad de registrarte para obtener una cuenta y una suscripción remotas. El servidor Peergos es un archivo `.jar`, lo que significa que debes tener instalado en tu máquina Java 17+ Runtime Environmen ([descarga de OpenJDK](https://azul.com/downloads)) para que funcione.

Ejecutar una versión local de Peergos junto con una cuenta registrada en su servicio alojado de pago te permite acceder a tu almacenamiento Peergos sin depender de DNS o autoridades de certificación TLS, y mantener una copia de seguridad de tus datos en su nube. La experiencia del usuario debería ser la misma tanto si ejecutas su servidor de escritorio como si utilizas su interfaz web alojada.

Peergos fue [auditado](https://cure53.de/pentest-report_peergos.pdf) por Cure53 en junio de 2019, y todos los problemas encontrados se solucionaron posteriormente.

No hay disponible una aplicación para Android, pero está [en preparación](https://discuss.privacyguides.net/t/peergos-private-storage-sharing-social-media-and-application-platform/11825/25). La solución actual consiste en utilizar [la PWA](https://peergos.net) móvil en su lugar.

## Criterios

**Por favor, ten en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

### Requisitos Mínimos

- Debe aplicar el cifrado de extremo a extremo.
- Debe ofrecer un plan gratuito o un periodo de prueba.
- Debe ser compatible con la autenticación multifactor TOTP o FIDO2, o con los inicios de sesión con llave de acceso.
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
