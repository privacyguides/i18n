---
meta_title: "Aplicaciones de Mapas y Navegación Recomendadas - Privacy Guides"
title: Mapas y Navegación
icon: material/map
description: Proveedores de mapas y aplicaciones de navegación que respetan la privacidad y no crean un perfil publicitario basado en tus búsquedas y ubicaciones.
cover: maps.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

Utiliza una **aplicación de mapas y navegación** que no construya un perfil publicitario basado en tus búsquedas e historial de localización. En lugar de utilizar Google Maps, Mapas de Apple o Waze, te recomendamos estas alternativas que respetan la privacidad.

Estas recomendaciones no recogen información de identificación personal (IIP), de acuerdo con la política de privacidad de cada aplicación. No existe **ninguna garantía** de que se respeten estas políticas de privacidad.

## Organic Maps

<div class="admonition recommendation" markdown>

![Organic Maps logo](assets/img/maps/organic-maps.svg){ align=right }

**Organic Maps** es una aplicación de código abierto, desarrollada por la comunidad, que permite visualizar mapas y ofrece navegación tipo satélite para peatones, conductores y ciclistas. La aplicación ofrece mapas de todo el mundo sin conexión, basados en datos de OpenStreetMap, y navegación con privacidad: sin seguimiento de la ubicación, sin recopilación de datos y sin anuncios. La aplicación puede utilizarse sin conexión.

Entre sus funciones se incluyen rutas de ciclismo, rutas de senderismo y senderos, navegación giro a giro guiada por voz y planificación de rutas de transporte público (solo disponible en ciertas regiones y ciudades).

[:octicons-home-16: Página Principal](https://organicmaps.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://organicmaps.app/privacy){ .card-link title="Política de Privacidad" }
[:octicons-code-16:](https://git.omaps.dev/organicmaps/organicmaps){ .card-link title="Código Fuente" }

<details class="downloads" markdown><summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.organicmaps)
- [:simple-appstore: App Store](https://apps.apple.com/app/organic-maps/id1567437057)
- [:simple-forgejo: Forgejo](https://git.omaps.dev/organicmaps/organicmaps/releases)
- [:simple-linux: Linux](https://flathub.org/apps/app.organicmaps.desktop)

</details>

</div>

Por favor, ten en cuenta que Organic Maps es una aplicación simple y básica que carece de ciertas características que muchos usuarios podrían esperar, como imágenes satelitales, imágenes de la calle e información del tráfico en tiempo real.

## OsmAnd

<div class="admonition recommendation" markdown>

![OsmAnd logo](assets/img/maps/osmand.svg){ align=right }

**OsmAnd** es una aplicación de mapas y navegación sin conexión de código abierto basada en OpenStreetMap que ofrece navegación giro a giro para caminar, ir en bicicleta, conducir y utilizar el transporte público. Puedes encontrar una descripción detallada de las [características] compatibles con OsmAnd(https://wiki.openstreetmap.org/wiki/OsmAnd#Features) en la Wiki de OpenStreet Map.

[:octicons-home-16: Página Principal](https://osmand.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://osmand.net/docs/legal/privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://osmand.net/docs/intro){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/osmandapp){ .card-link title="Código Fuente" }

<details class="downloads" markdown><summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.osmand)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/id934850257)
- [:simple-android: Android](https://osmand.net/docs/versions/free-versions)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Identificador Único de Usuario</p>

OsmAnd genera un [identificador único de usuario (UUID)](https://osmand.net/docs/legal/terms-of-use/#6-unique-user-indentifier) cada vez que se instala la aplicación, que cambia cada tres meses y se utiliza para informes y estadísticas internos. El UUID también se envía a los servidores de OsmAnd cuando se descargan los mapas. En Android, hay un ajuste que controla si el UUID se envía con cada solicitud de descarga. Desde la pantalla de inicio, ve a :material-menu: → :gear: **Configuración** → :gear: **Ajustes de OsmAnd** → :material-web: **Identificadores**.

- [ ] Desmarca **Enviar identificador único de usuario (UUID)**

Esta opción no está disponible en la aplicación para iOS.

</div>

La aplicación también incluye una opción para compartir datos anónimos sobre los mapas que descargas y las funciones que utilizas. Este ajuste está desactivado por defecto en Android, pero activado por defecto en iOS. Para desactivarlo en la aplicación para iOS, toca :material-menu: en la pantalla de inicio para encontrar el menú :gear: **Configuración**. Selecciónalo y, a continuación, selecciona :gear: **Ajustes de OsmAnd**.

- [ ] Desmarca **Enviar datos anónimos**

OsmAnd te permite superponer o subyacer datos del mapa externo, como imágenes de satélite de Microsoft o [datos del tráfico](https://themm.net/public/osmand_traffic) de Google, aunque este último es ignorado por la planificación automática de rutas. OsmAnd también dispone de una integración opcional de imágenes de vista de calles proporcionadas por [Mapillary](https://mapillary.com).

## Criterios

**Por favor, ten en cuenta que no estamos afiliados a ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

### Requisitos Mínimos

- No debe recopilar IIP según su política de privacidad.
- No debe exigir a los usuarios que creen una cuenta con ellos.
- No debe exigir a los usuarios que compartan sus datos de localización. Si el usuario opta por compartir su ubicación, estos datos deben ser anónimos.
- Debe mantener la funcionalidad básica cuando no esté conectado y permitir a los usuarios descargar mapas para su uso sin conexión.

### Mejor Caso

Nuestro criterio del mejor caso representa lo que nos gustaría ver del proyecto perfecto en esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Las aplicaciones deberían ser de código abierto.
- Debería disponer de planificación de rutas para el transporte público.
- Debería disponer de información sobre el tráfico en tiempo real para planificar la ruta.
- Debería admitir funciones avanzadas, como información detallada y reseñas de tiendas/puntos de interés (POI), mapas topográficos e imágenes de satélite y vistas de calles.
