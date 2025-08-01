---
meta_title: "Navegadores Web que Respetan la Privacidad para Android e iOS - Privacy Guides"
title: Navegadores Móviles
icon: material/cellphone-information
description: Estos navegadores son los que recomendamos actualmente para la navegación estándar/no anónima por Internet en su teléfono.
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Recomendaciones de Navegadores de Escritorio Privados
    url: "./"
    relatedLink: "../desktop-browsers/"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    applicationCategory: Web Browser
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Cromite
    image: /assets/img/browsers/cromite.svg
    url: https://cromite.org
    applicationCategory: Web Browser
    operatingSystem:
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://apple.com/safari
    applicationCategory: Navegador Web
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Estos son nuestros **navegadores web para móviles** y configuraciones recomendados actualmente para la navegación estándar/no anónima por Internet. Si necesitas navegar por Internet de forma anónima, deberías utilizar [Tor](tor.md) .

## Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** incluye un bloqueador de contenidos integrado y [funciones de privacidad](https://brave.com/privacy-features/), muchas de las cuales están activadas por defecto.

Brave se basa en el proyecto de navegador web Chromium, por lo que debería resultar familiar y tener mínimos problemas de compatibilidad con sitios web.

[:octicons-home-16: Página Principal](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Servicio Onion" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-fdroid: F-Droid](https://brave-browser-apk-release.s3.brave.com/fdroid/repo/index.html)

</details>

</div>

### Configuración Recomendada de Brave

Tor Browser es la única manera de navegar por Internet de forma verdaderamente anónima. Cuando uses Brave, te recomendamos cambiar los siguiente ajustes para proteger tu privacidad de ciertas partes, pero todos los navegadores que no sean [Tor Browser](tor.md#tor-browser) serán rastreables por *alguien* en un sentido u otro.

=== "Android"

    Estas opciones se encuentran en :material-menu: → **Configuración** → **Protecciones y privacidad de Brave**.

=== "iOS"

    Estas opciones se encuentran en :fontawesome-solid-ellipsis: → **Configuración** → **Protecciones y privacidad**.

#### Valores generales predeterminados de los escudos de Brave

Brave incluye algunas medidas contra el fingerprinting en su función [Escudos](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Te sugerimos configurar estas opciones [globalmente](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) en todas las páginas que visites.

Las opciones de los escudos pueden reducirse según las necesidades de cada sitio, pero por defecto recomendamos configurar lo siguiente:

=== "Android"

    <div class="annotate" markdown>

    - [x] Selecciona **Agresivo** en *Bloquear rastreadores y anuncios*
    - [x] Selecciona **Redirigir automáticamente las páginas AMP**
    - [x] Selecciona **URL de seguimiento de redirección automática**
    - [x] Selecciona **Exigir que todas las conexiones utilicen HTTPS (estricto)** en *Mejorar conexiones a HTTPS*
    - \[x\] (Opcional) Selecciona **Bloquear Scripts** (1)
    - [x] Selecciona **Bloquear cookies de terceros** en *Bloquear cookies*
    - [x] Selecciona **Bloquear Fingerprinting**
    - [x] Selecciona **Evita la toma de huellas dactilares mediante los ajustes de idioma**

    <details class="warning" markdown>
    <summary>Utiliza listas de filtros predeterminadas</summary>

    Brave te permite seleccionar filtros de contenido adicionales dentro del menú **Filtros de contenido** o de la página interna `brave://adblock`. Desaconsejamos el uso de esta función; en su lugar, mantenga las listas de filtros por defecto. El uso de listas adicionales le hará destacar entre los demás usuarios de Brave y también puede aumentar la superficie de ataque si hay un exploit en Brave y se añade una regla maliciosa a una de las listas que utiliza.

    </details>

    - [x] Selecciona **Olvidarme al cerrar este sitio**

    </div>

    1. Esta opción desactiva JavaScript, lo que romperá muchos sitios. Para no romperlos, puedes establecer excepciones para cada sitio pulsando sobre el icono del Escudo en la barra de direcciones y desmarcando esta opción en *Controles avanzados*.

=== "iOS"

    <div class="annotate" markdown>

    - [x] Selecciona **Agresivo** en *Bloquear rastreadores y anuncios*
    - [x] Selecciona **Estricto** en *Mejorar conexiones a HTTPS*
    - [x] Selecciona **Redirigir automáticamente las páginas AMP**
    - [x] Selecciona **URL de seguimiento de redirección automática**
    - \[x\] (Opcional) Selecciona **Bloquear Scripts** (1)
    - [x] Selecciona **Bloquear Fingerprinting**
    - [x] Selecciona **Pestañas Cerradas** en *Destrucción Automática*

    <details class="warning" markdown>
    <summary>Utiliza listas de filtros predeterminadas</summary>

    Brave te permite seleccionar filtros de contenido adicionales dentro del menú **Filtros de contenido**. Desaconsejamos el uso de esta función; en su lugar, mantenga las listas de filtros por defecto. El uso de listas adicionales le hará destacar entre los demás usuarios de Brave y también puede aumentar la superficie de ataque si hay un exploit en Brave y se añade una regla maliciosa a una de las listas que utiliza.

    </details>

    </div>

    1. Esta opción desactiva JavaScript, lo que romperá muchos sitios. Para no romperlos, puedes establecer excepciones para cada sitio pulsando sobre el icono del Escudo en la barra de direcciones y desmarcando esta opción en *Controles avanzados*.

##### Borrar datos de navegación (solo Android)

- [x] Selecciona **Borrar datos al salir**

##### Bloqueo de redes sociales (solo Android)

- [ ] Desmarca todos los componentes de redes sociales

#### Otros ajustes de privacidad

=== "Android"

    <div class="annotate" markdown>

    - [x] Selecciona **Desactivar UDP sin proxy** en [*Política de gestión de IP de WebRTC*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
    - \[x\] (Opcional) Selecciona **Sin protección** en *Navegación segura* (1)
    - [ ] Desmarca **Permite a los sitios comprobar si tienes métodos de pago guardados**
    - [ ] Desmarca **Optimización y seguridad de Javascript** en la opción con el mismo nombre
    - [x] Selecciona **Cerrar pestañas al salir**
    - [ ] Desmarca **Permitir estadísticas del producto con preservación de la privacidad (P3A)**
    - [ ] Desmarca **Enviar informes de diagnóstico automáticamente**
    - [ ] Desmarca **Enviar automáticamente el ping de uso diario a Brave**

    </div>

    1. La [implementación de la Navegación Segura](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) de Brave en Android **no** delega [las solicitudes de red de la Navegación Segura](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) como su homólogo de escritorio. Esto significa que tu dirección IP puede ser vista (y registrada) por Google. Ten en cuenta que la Navegación Segura no está disponible para dispositivos Android sin Google Play Services.

=== "iOS"

    - [ ] Desmarca **Permitir estadísticas de productos que preservan la privacidad (P3A)**
    - [ ] Desmarca **Enviar automáticamente el ping de uso diario a Brave**

#### Leo

Estas opciones se encuentran en :material-menu: → **Configuración** → **Leo**.

<div class="annotate" markdown>

- [ ] Desmarca **Mostrar sugerencias autocompletadas en la barra de direcciones** (1)

</div>

1. Esta opción no está presente en la aplicación de Brave para iOS.

#### Motores de búsqueda

Estas opciones se encuentran en :material-menu:/:fontawesome-solid-ellipsis: → **Configuración** → **Motores de búsqueda**.

- [ ] Desmarca **Mostrar sugerencias de búsqueda**

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) permite que tus datos de navegación (historial, marcadores, etc.) sean accesibles en todos tus dispositivos sin necesidad de tener una cuenta y los protege con E2EE.

## Cromite (Android)

<div class="admonition recommendation" markdown>

![Cromite logo](assets/img/browsers/cromite.svg){ align=right }

**Cromite** es un navegador basado en Chromium con bloqueo de anuncios integrado, protección de huellas digitales y otras [mejoras de privacidad y seguridad](https://github.com/uazo/cromite/blob/master/docs/FEATURES.md). Es una bifurcación del navegador descatalogado **Bromite**.

[:octicons-home-16: Página Principal](https://cromite.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uazo/cromite/blob/master/docs/PRIVACY_POLICY.md){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://github.com/uazo/cromite?tab=readme-ov-file#docs){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/uazo/cromite){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-android: F-Droid](https://cromite.org/fdroid/repo/?fingerprint=49F37E74DEE483DCA2B991334FB5A0200787430D0B5F9A783DD5F13695E9517B)
- [:simple-github: GitHub](https://github.com/uazo/cromite/releases/latest)

</details>

</div>

### Configuración Recomendada

Estas opciones se encuentran en :material-menu: → :gear: **Configuración** → **Privacidad y seguridad**.

#### Browsing data

- [x] Selecciona **Close all open tabs on exit**

#### Modo Incógnito

- [x] Selecciona **Open external links in incognito**

#### Seguridad

- [x] Selecciona **Usar siempre conexiones seguras**

Esto evita que te conectes involuntariamente a un sitio web en texto plano HTTP. HTTP es muy poco común hoy en día, por lo que esto debería tener poco o ningún impacto en tu navegación diaria.

#### Adblock Plus settings

Estas opciones se encuentran en :material-menu: → :gear: **Configuración** → **Adblock Plus settings**.

Cromite contiene una versión personalizada de Adblock Plus con EasyList activado por defecto, así como opciones para seleccionar más listas de filtros dentro del menú **Filter lists**.

Usar listas adicionales te hará destacar de otros usuarios de Cromite y también puede aumentar la superficie de ataque si una regla maliciosa es añadida a una de las listas que usas.

- \[x\] (Opcional) Selecciona **Enable anti-circumvention and snippets**

Esta opción añade una lista adicional de Adblock Plus que puede aumentar la efectividad del bloqueo de contenido de Cromite. Se aplican las advertencias sobre destacar y aumentar potencialmente la superficie de ataque.

#### Legacy Adblock settings

Estas opciones se encuentran en :material-menu: → :gear: **Configuración** → **Legacy Adblock settings**.

- [ ] Desmarca la opción de actualización automática (Autoupdate)

Esto desactiva las comprobaciones de actualización para el filtro adblock Bromite, que no recibe mantenimiento.

## Safari (iOS)

On iOS, any app that can browse the web is [restricted](https://developer.apple.com/app-store/review/guidelines) to using an Apple-provided [WebKit framework](https://developer.apple.com/documentation/webkit), so a browser like [Brave](#brave) does not use the Blink engine (the core component of Chromium) like its counterparts on other operating systems.

<div class="admonition recommendation" markdown>

![Safari logo](assets/img/browsers/safari.svg){ align=right }

**Safari** es el navegador predeterminado en iOS. Incluye [funciones de privacidad](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) como [Prevención Inteligente de Rastreo](https://webkit.org/blog/7675/intelligent-tracking-prevention), pestañas aisladas y efímeras de Navegación Privada, protección de huellas digitales (presentando una versión simplificada de la configuración del sistema a los sitios web para que más dispositivos parezcan idénticos) y aleatorización de huellas digitales, así como Relay Privado para quienes tengan una suscripción de pago a iCloud+.

[:octicons-home-16: Página Principal](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title="Documentación" }

</details>

</div>

### Configuración Recomendada de Safari

Te sugerimos instalar [AdGuard](browser-extensions.md#adguard) si quieres un bloqueador de contenido en Safari.

Las siguientes opciones relacionadas con la privacidad y la seguridad se encuentran en :gear: **Ajustes** → **Aplicaciones** → **Safari**.

#### Permitir a Safari Acceder

En **Siri**:

- [ ] Desactiva **Aprender de esta App**
- [ ] Desactiva **Mostrar en App**
- [ ] Desactiva **Mostrar en Pantalla de Inicio**
- [ ] Desactiva **Sugerir App**

Esto evita que Siri utilice el contenido de Safari para las sugerencias de Siri.

#### Buscar

- [ ] Desactiva **Sugerencias del Motor de Búsqueda**

Este ajuste envía todo lo que escribas en la barra de direcciones al motor de búsqueda configurado en Safari. Desactivar las sugerencias de búsqueda te permite controlar con mayor precisión qué datos envías al proveedor de tu motor de búsqueda.

#### Perfiles

Safari te permite separar tu navegación con diferentes perfiles. Todas tus cookies, historial y datos del sitio web están separados para cada perfil. Deberías utilizar diferentes perfiles para diferentes propósitos, por ejemplo, ir de compras, trabajar o uso escolar.

#### Privacidad & Seguridad

- [x] Activa **Evitar el seguimiento cruzado de sitios**

Esto habilita la [Protección de Seguimiento Inteligente](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp) de WebKit. La función ayuda a proteger contra el rastreo no deseado utilizando el aprendizaje automático en el dispositivo para detener a los rastreadores. La ITP protege contra muchas amenazas comunes, pero no bloquea todas las vías de rastreo porque está diseñada para no interferir con la usabilidad del sitio web.

- [x] Activa **Requerir Face ID/Touch ID para desbloquear la navegación privada**

Este ajuste te permite bloquear tus pestañas privadas detrás de los datos biométricos/PIN cuando no las estés utilizando.

- [ ] Desactiva **Aviso de Sitio Web Fraudulento**

Esta configuración utiliza Google Safe Browsing (o Tencent Safe Browsing para usuarios de China continental o Hong Kong) para protegerte mientras navegas. Por ello, es posible que tu proveedor de navegación segura registre tu dirección IP. Si desactivas esta opción, se desactivará el registro, pero podrías ser más vulnerable a los sitios de phishing conocidos.

- [x] Activar **Aviso de Conexión No Segura**

Esta configuración muestra una pantalla de advertencia si tu conexión a un sitio web no utiliza HTTPS. Safari intentará automáticamente actualizar el sitio a HTTPS, por lo que solo deberías ver esto cuando no haya una conexión HTTPS disponible.

- [ ] Desactiva **Destacados**

La política de privacidad de Apple para Safari establece:

> Al visitar una página web, Safari puede enviar información calculada a partir de la dirección de la página web a Apple a través de HTTP para determinar si hay disponibles elementos destacados relevantes.

#### Configuración de Sitios Web

En **Cámara**

- [x] Selecciona **Preguntar**

En **Micrófono**

- [x] Selecciona **Preguntar**

En**Ubicación**

- [x] Selecciona **Preguntar**

Estos ajustes garantizan que los sitios web solo puedan acceder a tu cámara, micrófono o ubicación después de que les concedas explícitamente el acceso.

#### Otros Ajustes de Privacidad

Estas opciones se encuentran en :gear: **Ajustes** → **Aplicaciones** → **Safari** → **Avanzado**.

##### Mitigación de Huella Digital

La configuración de **Protección Avanzada Antirrastreo y de la Huella Digital** aleatorizará ciertos valores para que sea más difícil tomarte las huellas dactilares:

- [x] Seleccione **Toda la Navegación** o **Navegación Privada**

##### Medición de anuncios para preservar la privacidad

- [ ] Desactiva **Medición de anuncios para preservar la privacidad**

La medición de los clics en los anuncios ha utilizado tradicionalmente una tecnología de seguimiento que vulnera la intimidad del usuario. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) es una función de WebKit y un estándar web propuesto para permitir a los anunciantes medir la eficacia de las campañas web sin comprometer la privacidad del usuario.

La función tiene pocos problemas de privacidad por sí misma, así que aunque puede optar por dejarla activada, consideramos que el hecho de que se desactive automáticamente en Navegación Privada es un indicador para desactivar la función.

#### Navegación privada siempre activa

Abre Safari y pulsa el botón Pestañas, situado en la parte inferior derecha. A continuación, amplíe la :material-format-list-bulleted: lista Grupos de Pestañas.

- [x] Selecciona **Privado**

El modo de Navegación Privada de Safari ofrece protecciones de privacidad adicionales. La Navegación Privada utiliza una nueva sesión [efímera](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) para cada pestaña, lo que significa que las pestañas están aisladas unas de otras. La Navegación Privada también ofrece otras pequeñas ventajas de privacidad, como no enviar la dirección de una página web a Apple cuando se utiliza la función de traducción de Safari.

Ten en cuenta que la Navegación Privada no guarda cookies ni datos de sitios web, por lo que no podrás seguir conectado a ellos. Esto puede ser un inconveniente.

#### iCloud Sync

La sincronización del historial de Safari, los grupos de pestañas, las pestañas de iCloud y las contraseñas guardadas son E2EE. Sin embargo, por defecto, los marcadores [no](https://support.apple.com/HT202303) lo son. Apple puede descifrarlos y acceder a ellos de acuerdo con su [política de privacidad](https://apple.com/legal/privacy/en-ww).

Puedes activar E2EE para tus favoritos y tus descargas de Safari activando [Protección de Datos Avanzada](https://support.apple.com/HT212520). Vaya a :gear: **Ajustes** → **iCloud** → **Protección de Datos Avanzada**.

- [x] Activa **Protección de Datos Avanzada**

Si utilizas iCloud con la Protección de Datos Avanzada desactivada, también te recomendamos que configures la ubicación de descarga predeterminada de Safari en una carpeta local de tu dispositivo. Esta opción se encuentra en :gear: **Ajustes** → **Aplicaciones** → **Safari** → **General** → **Descargas**.

## Criterios

**Por favor, tenga en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que usted se familiarice con esta lista, antes de decidir utilizar un proyecto y realizar su propia investigación para asegurarse de que es la elección ideal para usted.

### Requisitos Mínimos

- Debe admitir actualizaciones automáticas.
- Debe recibir las actualizaciones del motor con rapidez.
- Debe soportar el bloqueo de contenido.
- Cualquier cambio necesario para que el navegador respete más la privacidad no debería afectar negativamente a la experiencia del usuario.
