---
title: "Compartir y sincronizar archivos"
icon: material/share-variant
description: Descubra cómo puede compartir de manera privada sus archivos entre sus dispositivos, con sus amigos y familia, o de manera anónima en línea.
cover: file-sharing.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-server-network: Proveedores de servicios](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Descubra cómo puede compartir de manera privada sus archivos entre sus dispositivos, con sus amigos y familia, o de manera anónima en línea.

## Programas para compartir archivos

Si ya utiliza [Proton Drive](cloud.md#proton-drive)[^1] o tiene una suscripción a [Bitwarden](passwords.md#bitwarden) Premium[^2] considere la posibilidad de utilizar las funciones de compartición de archivos que ofrecen, ambas con cifrado de extremo a extremo. De lo contrario, las opciones independientes enumeradas aquí garantizan que los archivos compartidos no sean leídos por un servidor remoto.

### Send

<div class="admonition recommendation" markdown>

![Send logo](assets/img/file-sharing-sync/send.svg){ align=right }

**Send** es una bifurcación del descontinuado servicio Firefox Send de Mozilla que le permite enviar archivos a otros con un enlace. Los archivos son encriptados en su dispositivo, lo que no permite que sean leídos por el servidor y, opcionalmente, también pueden protegerse por una contraseña. El responsable de mantener Send alberga una [instancia pública](https://send.vis.ee). Puede utilizar otras instancias públicas o puede alojar Send usted mismo.

[:octicons-home-16: Página principal](https://send.vis.ee){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="Public Instances"}
[:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title=Contribute }

</details>

</div>

Send puede utilizarse a través de su interfaz web o mediante la herremienta de comandos [ffsend](https://github.com/timvisee/ffsend). Si usted es familiar con la línea de comandos y envía archivos frecuentemente, recomendamos utilizar el cliente CLI para evitar la encriptación basada en JavaScript. Usted puede especificar la bandera `--host` para utilizar un servidor en específico:

```bash
ffsend upload --host https://send.vis.ee/ FILE
```

### OnionShare

<div class="admonition recommendation" markdown>

![OnionShare logo](assets/img/file-sharing-sync/onionshare.svg){ align=right }

**OnionShare** es una herramienta de código abierto que permite compartir de forma segura y [:material-incognito: anónima](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } archivos de cualquier tamaño. Funciona iniciando un servidor web accesible como un servicio onion de Tor, con un enlace indescifrable que se puede compartir con los receptores para descargar o enviar archivos.

[:octicons-home-16: Página Principal](https://onionshare.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="Servicio Onion" }
[:octicons-info-16:](https://docs.onionshare.org){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:fontawesome-brands-windows: Windows](https://onionshare.org/#download)
- [:simple-apple: macOS](https://onionshare.org/#download)
- [:simple-linux: Linux](https://onionshare.org/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/org.onionshare.OnionShare)

</details>

</div>

OnionShare ofrece la opción de conectarse a través de [puentes tor](https://docs.onionshare.org/2.6.2/en/tor.html#automatic-censorship-circumvention) para eludir la [:material-close-outline: Censura](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}.

### Criterios

**Por favor, tome en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** En adición a [nuestros criterios estándares](about/criteria.md), hemos desarrollado un claro conjunto de requisitos para permitirnos brindar recomendaciones objetivas. Sugerimos que usted se familiarice con esta lista antes de optar por utilizar un proyecto, y realizar su propia investigación para asegurarse que es la elección adecuada.

- No debe almacenar información sin encriptar en un servidor remoto.
- Debe ser un programa de código abierto.
- Debe tener clientes para Linux, macOS y Winwos; o tener una interfaz web.

## FreedomBox

<div class="admonition recommendation" markdown>

![FreedomBox logo](assets/img/file-sharing-sync/freedombox.svg){ align=right }

**FreedomBox** es un sistema operativo diseñado para correr en una [computadora de placa única (SBC, por sus siglas en inglés)](https://en.wikipedia.org/wiki/Single-board_computer). El propósito es facilitar la configuración de aplicaciones que requieran un servidor y se puedan alojar por usted mismo.

[:octicons-home-16: Página Principal](https://freedombox.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title=Documentación}
[:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://freedomboxfoundation.org/donate){ .card-link title=Contribuir }

</details>

</div>

## Sincronización de archivos

### Nextcloud (Cliente-Servidor)

<div class="admonition recommendation" markdown>

![Nextcloud logo](assets/img/document-collaboration/nextcloud.svg){ align=right }

**Nextcloud** es un conjunto de programas cliente-servidor gratuitos y de código abierto para crear sus propios servicios de alojamiento de archivos en un servidor privado que usted controla.

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

No recomendamos utilizar la [aplicación con cifrado de extremo a extremo](https://apps.nextcloud.com/apps/end_to_end_encryption) para Nextcloud, porque puede causar la pérdida de datos; esta es considerada como altamente experimental y no debe utilizarse en entornos de producción.

</div>

### Syncthing (P2P)

<div class="admonition recommendation" markdown>

![Syncthing logo](assets/img/file-sharing-sync/syncthing.svg){ align=right }

**Syncthing** es una herramienta de sincronización continua de archivos peer-to-peer de código abierto. Es utilizada para sincronizar archivos entre dos o más dispositivos sobre la red local o el Internet. Syncthing no utiliza un servidor centralizado, este utiliza el [Protocolo de Intercambio de Bloques](https://docs.syncthing.net/specs/bep-v1.html#bep-v1) para transferir los datos entre dispositivos. Todos los datos son encriptados utilizando TLS.

[:octicons-home-16: Página Principal](https://syncthing.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.syncthing.net){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/syncthing){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://syncthing.net/donations){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:fontawesome-brands-windows: Windows](https://syncthing.net/downloads)
- [:simple-apple: macOS](https://syncthing.net/downloads)
- [:simple-linux: Linux](https://syncthing.net/downloads)
- [:simple-freebsd: FreeBSD](https://syncthing.net/downloads)

</details>

</div>

### Criterios

**Por favor, tome en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** En adición a [nuestros criterios estándares](about/criteria.md), hemos desarrollado un claro conjunto de requisitos para permitirnos brindar recomendaciones objetivas. Sugerimos que usted se familiarice con esta lista antes de optar por utilizar un proyecto, y realizar su propia investigación para asegurarse que es la elección adecuada.

#### Requisitos Mínimos

- No debe requerir un servidor de terceros remoto o en la nube.
- Debe ser software de código abierto.
- Debe tener clientes para Linux, macOS y Winwos; o tener una interfaz web.

#### Mejor Caso

Nuestro criterio del mejor caso representa lo que nos gustaría ver del proyecto perfecto en esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Debe tener clientes móviles para iOS y Android que, al menos, admitan la vista previa de documentos.
- Debe soportar copias de seguridad de fotos desde iOS y Android, y opcionalmente soportar la sincronización de archivos/carpetas en Android.

[^1]: Proton Drive le permite [compartir archivos o carpetas](https://proton.me/support/drive-shareable-link) generando un enlace público compartible o enviando un enlace único a una dirección de correo electrónico designada. Los enlaces públicos pueden protegerse con una contraseña, configurarse para que caduquen y revocarse por completo, mientras que los enlaces compartidos por correo electrónico pueden tener permisos personalizados y revocarse de forma similar. Según [la política de privacidad](https://proton.me/drive/privacy-policy) de Proton Drive, el contenido de los archivos, los nombres de archivos y carpetas y las vistas previas en miniatura se cifran de extremo a extremo.
[^2]: Con una suscripción [premium](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans), [Bitwarden Send](https://bitwarden.com/products/send) le permite compartir archivos y texto de forma segura con [cifrado de extremo a extremo](https://bitwarden.com/help/send-encryption). Se puede solicitar una [contraseña](https://bitwarden.com/help/send-privacy/#send-passwords) junto con el enlace Send. Bitwarden Send también dispone de [borrado automático](https://bitwarden.com/help/send-lifespan).
