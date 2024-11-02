---
meta_title: "Navegadores Web que Respetan la Privacidad para Android e iOS - Privacy Guides"
title: "Navegadores Móviles"
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
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://apple.com/safari
    applicationCategory: Web Browser
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
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Politica de Privacidad" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

### Configuración Recomendada de Brave

Tor Browser es la única manera de navegar por Internet de forma verdaderamente anónima. Cuando uses Brave, te recomendamos cambiar los siguiente ajustes para proteger tu privacidad de ciertas partes, pero todos los navegadores que no sean [Tor Browser](tor.md#tor-browser) serán rastreables por *alguien* en un sentido u otro.

=== "Android"

    Estas opciones se encuentran en :material-menu: → **Configuración** → **Protecciones y privacidad de Brave**.

=== "iOS"

    Estas opciones se encuentran en :fontawesome-solid-ellipsis: → **Configuración** → **Protecciones y privacidad**.

#### Valores generales predeterminados de los escudos de Brave

Brave incluye algunas medidas antihuellas en su función [Escudos](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Te sugerimos configurar estas opciones [globalmente](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) en todas las páginas que visites.

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
    - [x] Selecciona **Cerrar pestañas al salir**
    - [ ] Desmarca **Permitir estadísticas del producto con preservación de la privacidad (P3A)**
    - [ ] Desmarca **Enviar informes de diagnóstico automáticamente**
    - [ ] Desmarca **Enviar automáticamente el ping de uso diario a Brave**

    </div>

    1. La [implementación de la Navegación Segura](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) de Brave en Android **no** delega [las solicitudes de red de la Navegación Segura](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) como su homólogo de escritorio. Esto significa que tu dirección IP puede ser vista (y registrada) por Google. Ten en cuenta que la Navegación Segura no está disponible para dispositivos Android sin Google Play Services.

=== "iOS"

    - [ ] Desmarca **Permitir estadísticas de productos que preservan la privacidad (P3A)**
    - [ ] Desmarca **Enviar automáticamente el ping de uso diario a Brave**

### Leo

Estas opciones se encuentran en :material-menu: → **Configuración** → **Leo**.

<div class="annotate" markdown>

- [ ] Desmarca **Mostrar sugerencias autocompletadas en la barra de direcciones** (1)

</div>

1. Esta opción no está presente en la aplicación de Brave para iOS.

### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) permite que tus datos de navegación (historial, favoritos, etc.) sean accesibles en todos tus dispositivos sin necesidad de tener una cuenta y los protege con E2EE.

## Mull (Android)

<div class="admonition recommendation" markdown>

![Mull logo](assets/img/browsers/mull.svg){ align=right }

**Mull** es un navegador para Android orientado a la privacidad y depurado, basado en Firefox. A comparación con Firefox, este ofrece una protección mayor contra las huellas digitales y desactiva la compilación Just-In-Time (JIT) de JavaScript para mejorar la seguridad. Este también elimina todos los elementos propietarios de Firefox, como el reemplazo de las referencias a los Servicios de Google Play.

[:octicons-home-16: Página principal](https://divestos.org/pages/our_apps#mull){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy){ .card-link title="Política de privacidad" }
[:octicons-info-16:](https://divestos.org/pages/browsers#tuningFenix){ .card-link title=Documentación }
[:octicons-code-16:](https://codeberg.org/divested-mobile/mull-fenix){ .card-link title="Código fuente" }

<details class="downloads" markdown>
<summary>Descargas</summary>

- [:simple-fdroid: F-Droid](https://f-droid.org/en/packages/us.spotco.fennec_dos)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Peligro</p>

Los navegadores basados en Firefox (Gecko) para Android [carecen](https://bugzilla.mozilla.org/show_bug.cgi?id=1610822) del [aislamiento de sitios](https://wiki.mozilla.org/Project_Fission),[^1] una potente función de seguridad que protege contra un sitio malicioso que realice un ataque similar a [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)) para obtener acceso a la memoria de otro sitio web que tienes abierto.[^2] Los navegadores basados en Chromium como [Brave](#brave) proporcionan una protección más robusta contra sitios maliciosos.

</div>

Habilita el [repositorio F-Droid](https://divestos.org/fdroid/official) de DivestOS para recibir actualizaciones directamente del desarrollador. La descarga de Mull desde el repositorio oficial de F-Droid puede significar que las actualizaciones se atrasen por algunos días o incluso más.

Mull activa varias características del [proyecto Tor uplift](https://wiki.mozilla.org/Security/Tor_Uplift) usando las preferencias de [Arkenfox](desktop-browsers.md#arkenfox-advanced). Los blobs propietarios son eliminados desde el código de Mozilla usando script desarrollador para Fennec F-Droid.

### Configuración Recomendada de Mull

Sugerimos instalar [uBlock Origin](browser-extensions.md#ublock-origin) como bloqueador de contenido si quieres bloquear los rastreadores en Mull.

Mull viene con ajustes para la protección de la privacidad activados por defecto. Puedes considerar configurar las opciones para **Eliminar los datos de navegación al salir** en los ajustes de Mull si quieres cerrar automáticamente todas las pestañas abiertas al salir de la aplicación, o eliminar otros datos como el historial de navegación y las cookies de manera automática.

Debido a que Mull tiene protecciones más avanzadas y estrictas activadas por defecto a comparación de otros navegadores, algunos sitios web podrían no cargar o dejar de funcionar correctamente, a menos que se ajusten esas configuraciones. Puedes consultar esta [lista de problemas conocidos y soluciones](https://divestos.org/pages/broken#mull) para obtener consejos sobre una posible solución si encuentras un sitio roto. Ajustar una configuración para el correcto funcionamiento de un sitio web podría impactar tu privacidad y/o seguridad, por lo que debes asegurarte de comprender totalmente cualquier instrucción que sigues.

## Safari (iOS)

En iOS, cualquier aplicación que puede navegar en internet está [limitada](https://developer.apple.com/app-store/review/guidelines) a utilizar un sistema que provee Apple, [llamado WebKit](https://developer.apple.com/documentation/webkit), por lo que hay pocos motivos para utilizar un navegador de terceros.

<div class="admonition recommendation" markdown>

![Safari logo](assets/img/browsers/safari.svg){ align=right }

**Safari** es el navegador predeterminado en iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites so more devices look identical), and fingerprint randomization, as well as Private Relay for those with a paid iCloud+ subscription.

[:octicons-home-16: Página Principal](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title=Documentación}

</details>

</div>

### Configuración Recomendada de Safari

Te sugerimos instalar [AdGuard](browser-extensions.md#adguard) si quieres un bloqueador de contenido en Safari.

The following privacy/security-related options can be found in :gear: **Settings** → **Apps** → **Safari**.

#### Perfiles

Safari allows you to separate your browsing with different profiles. All of your cookies, history, and website data are separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

#### Privacidad y seguridad

- [x] Enable **Prevent Cross-Site Tracking**

This enables WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). The feature helps protect against unwanted tracking by using on-device machine learning to stop trackers. ITP protects against many common threats, but does not block all tracking avenues because it is designed to not interfere with website usability.

- [x] Enable **Require Face ID/Touch ID to Unlock Private Browsing**

This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

#### Other Privacy Settings

These options can be found in :gear: **Settings** → **Apps** → **Safari** → **Advanced**.

##### Fingerprinting Mitigations

La configuración de **Protección Avanzada Antirrastreo y de la Huella Digital** aleatorizará ciertos valores para que sea más difícil tomarte las huellas dactilares:

- [x] Seleccione **Toda la Navegación** o **Navegación Privada**

##### Medición de anuncios para preservar la privacidad

- [ ] Desactiva **Medición de anuncios para preservar la privacidad**

La medición de los clics en los anuncios ha utilizado tradicionalmente una tecnología de seguimiento que vulnera la intimidad del usuario. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) es una función de WebKit y un estándar web propuesto para permitir a los anunciantes medir la eficacia de las campañas web sin comprometer la privacidad del usuario.

La función tiene pocos problemas de privacidad por sí misma, así que aunque puede optar por dejarla activada, consideramos que el hecho de que se desactive automáticamente en Navegación Privada es un indicador para desactivar la función.

#### Navegación privada siempre activa

Abre Safari y pulsa el botón Pestañas, situado en la parte inferior derecha. Then, expand the :material-format-list-bulleted: Tab Groups list.

- [x] Selecciona **Privado**

El modo de Navegación Privada de Safari ofrece protecciones de privacidad adicionales. La Navegación Privada utiliza una nueva sesión [efímera](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) para cada pestaña, lo que significa que las pestañas están aisladas unas de otras. La Navegación Privada también ofrece otras pequeñas ventajas de privacidad, como no enviar la dirección de una página web a Apple cuando se utiliza la función de traducción de Safari.

Do note that Private Browsing does not save cookies and website data, so it won't be possible to remain signed in to sites. Esto puede ser un inconveniente.

#### iCloud Sync

La sincronización del historial de Safari, los grupos de pestañas, las pestañas de iCloud y las contraseñas guardadas son E2EE. Sin embargo, por defecto, los marcadores [no](https://support.apple.com/HT202303) lo son. Apple puede descifrarlos y acceder a ellos de acuerdo con su [política de privacidad](https://apple.com/legal/privacy/en-ww).

Puedes activar E2EE para tus favoritos y tus descargas de Safari activando [Protección de Datos Avanzada](https://support.apple.com/HT212520). Go to :gear: **Settings** → **iCloud** → **Advanced Data Protection**.

- [x] Turn on **Advanced Data Protection**

If you use iCloud with Advanced Data Protection disabled, we also recommend setting Safari's default download location to a local folder on your device. This option can be found in :gear: **Settings** → **Apps** → **Safari** → **General** → **Downloads**.

## Criterios

**Por favor, tenga en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que usted se familiarice con esta lista, antes de decidir utilizar un proyecto y realizar su propia investigación para asegurarse de que es la elección ideal para usted.

### Requisitos Mínimos

- Debe admitir actualizaciones automáticas.
- Debe recibir las actualizaciones del motor con rapidez.
- Debe soportar el bloqueo de contenido.
- Cualquier cambio necesario para que el navegador respete más la privacidad no debería afectar negativamente a la experiencia del usuario.
