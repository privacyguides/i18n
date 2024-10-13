---
meta_title: "Privacy Respecting Web Browsers for Android and iOS - Privacy Guides"
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

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our currently recommended **mobile web browsers** and configurations for standard/non-anonymous internet browsing. Si necesitas navegar por Internet de forma anónima, deberías utilizar [Tor](tor.md) .

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
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)

</details>

</div>

### Configuración Recomendada de Brave

Tor Browser es la única manera de navegar por Internet de forma verdaderamente anónima. Cuando use Brave, Le recomendamos cambiar los siguiente ajustes para proteger su privacidad de ciertas partes, pero todos los navegadores que no sean [Tor Browser](tor.md#tor-browser) serán rastreables por *alguien* en un sentido u otro.

Estas opciones se pueden encontrar en :material-menu: → **Configuración** → **Protecciones y privacidad de Brave**

#### Shields

Brave incluye algunas medidas antihuellas en su función [Escudos](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Te sugerimos configurar estas opciones [globalmente](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) en todas las páginas que visites.

#### Brave shields global defaults

Las opciones de los escudos pueden reducirse según las necesidades de cada sitio, pero por defecto recomendamos configurar lo siguiente:

<div class="annotate" markdown>

- [x] Seleccione **Agresivo** en **Bloquear rastreadores y anuncios**

<details class="warning" markdown>
<summary>Usa listas de filtros predeterminadas</summary>

Brave te permite seleccionar filtros de contenido adicionales en la página interna `brave://adblock`. Desaconsejamos el uso de esta función; en su lugar, mantenga las listas de filtros por defecto. El uso de listas adicionales le hará destacar entre los demás usuarios de Brave y también puede aumentar la superficie de ataque si hay un exploit en Brave y se añade una regla maliciosa a una de las listas que utiliza.

</details>

- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **strict** under **Upgrade connections to HTTPS**
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Block third-party cookies** under **Block Cookies**
- [x] Select **Block fingerprinting**
- [x] Select **Prevent fingerprinting via language settings**

</div>

1. Esta opción proporciona una funcionalidad similar a los [modos de bloqueo](https://github.com/gorhill/uBlock/wiki/Blocking-mode) avanzados de uBlock Origin o la extensión [NoScript](https://noscript.net).

#### Clear browsing data

- [x] Seleccione **Borrar datos al salir**

#### Social Media Blocking

- [ ] Desmarque todos los componentes de redes sociales

#### Other privacy settings

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP handling policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [x] (Optional) Select **No protection** under **Safe Browsing** (1)
- [ ] Uncheck **Allow sites to check if you have payment methods saved**
- [ ] Uncheck **IPFS Gateway** (2)
- [x] Select **Close tabs on exit**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Automatically send daily usage ping to Brave**

</div>

1. Brave's [implementation of Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) on Android **does not** proxy [Safe Browsing network requests](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) like its desktop counterpart. This means that your IP address may be seen (and logged) by Google. Note that Safe Browsing is not available for Android devices without Google Play Services.
2. El Sistema de Archivos InterPlanetario (IPFS) es una red descentralizada, de igual a igual, para almacenar y compartir datos en un sistema de archivos distribuido. A menos que utilice la función, desactívela.

### Leo

These options can be found in :material-menu: → **Settings** → **Leo**

- [ ] Uncheck **Show autocomplete suggestions in address bar**

### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) permite que tus datos de navegación (historial, favoritos, etc.) sean accesibles en todos tus dispositivos sin necesidad de tener una cuenta y los protege con E2EE.

## Mull (Android)

<div class="admonition recommendation" markdown>

![Mull logo](assets/img/browsers/mull.svg){ align=right }

**Mull** es un navegador orientado y depurado a la privacidad basado en Firefox. A comparación con Firefox, este ofrece una protección mayor contra las huellas digitales y desactiva la compilación Just-In-Time (JIT) de JavaScript para mejorar la seguridad. Este también elimina todos los elementos propietarios de Firefox, como el reemplazo de las referencias a los Servicios de Google Play.

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

Enable DivestOS's [F-Droid repository](https://divestos.org/fdroid/official) to receive updates directly from the developer. La descarga de Mull desde el repositorio oficial de F-Droid puede significar que las actualizaciones se atrasen por algunos días o incluso más.

Mull activa varias características del [proyecto Tor uplift](https://wiki.mozilla.org/Security/Tor_Uplift) usando las preferencias de [Arkenfox](desktop-browsers.md#arkenfox-advanced). Los blobs propietarios son eliminados desde el código de Mozilla usando script desarrollador para Fennec F-Droid.

### Recommended Mull Configuration

Sugerimos instalar [uBlock Origin](browser-extensions.md#ublock-origin) como bloqueador de contenido si quieres bloquear los rastreadores en Mull.

Mull viene con ajustes para la protección de la privacidad activados por defecto. Puedes considerar configurar las opciones para **Eliminar los datos de navegación al salir** en los ajustes de Mull si quieres cerrar automáticamente todas las pestañas abiertas al salir de la aplicación, o eliminar otros datos como el historial de navegación y las cookies de manera automática.

Debido a que Mull tiene protecciones más avanzadas y estrictas activadas por defecto a comparación de otros navegadores, algunos sitios web podrían no cargar o dejar de funcionar correctamente, a menos que se ajusten esas configuraciones. Puedes consultar esta [lista de problemas conocidos y soluciones](https://divestos.org/pages/broken#mull) para obtener consejos sobre una posible solución si encuentras un sitio roto. Ajustar una configuración para el correcto funcionamiento de un sitio web podría impactar tu privacidad y/o seguridad, por lo que debes asegurarte de comprender totalmente cualquier instrucción que sigues.

## Safari (iOS)

En iOS, cualquier aplicación que puede navegar en internet está [limitada](https://developer.apple.com/app-store/review/guidelines) a utilizar un sistema que provee Apple, [llamado WebKit](https://developer.apple.com/documentation/webkit), por lo que hay pocos motivos para utilizar un navegador de terceros.

<div class="admonition recommendation" markdown>

![Safari logo](assets/img/browsers/safari.svg){ align=right }

**Safari** es el navegador predeterminado en iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Privacy Report, isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites so more devices look identical) as well as fingerprint randomization, and Private Relay for those with a paid iCloud+ subscription. It also allows you to separate your browsing with different profiles and lock private tabs with your biometrics/PIN.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title=Documentation}

</details>

</div>

### Configuración recomendada de Safari

We would suggest installing [AdGuard](browser-extensions.md#adguard) if you want a content blocker in Safari.

Las siguientes opciones relacionadas con la privacidad/seguridad pueden encontrarse en :gear: aplicación de **Ajustes** → **Safari**

#### Perfiles

Todas tus cookies, historial y datos del sitio web estarán separados para cada perfil. Deberías utilizar diferentes perfiles para diferentes propósitos, por ejemplo, ir de compras, trabajar o uso escolar.

#### Privacidad y seguridad

- [x] Activa **Evitar el seguimiento cruzado de sitios**

    Esto habilita la [Protección de Seguimiento Inteligente (ITP)](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp) de WebKit. La función ayuda a proteger contra el rastreo no deseado utilizando el aprendizaje automático en el dispositivo para detener a los rastreadores. La ITP protege contra muchas amenazas comunes, pero no bloquea todas las vías de rastreo porque está diseñada para no interferir con la usabilidad del sitio web.

- [x] Activa **Requerir Face ID para desbloquear la navegación privada**

    Este ajuste te permite bloquear tus pestañas privadas detrás de los datos biométricos/PIN cuando no las estés utilizando.

#### Avanzado → Privacidad

La configuración de **Protección Avanzada Antirrastreo y de la Huella Digital** aleatorizará ciertos valores para que sea más difícil tomarte las huellas dactilares:

- [x] Seleccione **Toda la Navegación** o **Navegación Privada**

#### Informe de privacidad

El Informe de privacidad proporciona una instantánea de los rastreadores de sitios cruzados a los que actualmente se les impide elaborar perfiles en el sitio web que está visitando. También puede mostrar un informe semanal para mostrar qué rastreadores se han bloqueado a lo largo del tiempo.

Se puede acceder al Informe de privacidad a través del menú Configuración de la página.

#### Medición de anuncios para preservar la privacidad

- [ ] Desactiva **Medición de anuncios para preservar la privacidad**

La medición de los clics en los anuncios ha utilizado tradicionalmente una tecnología de seguimiento que vulnera la intimidad del usuario. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) es una función de WebKit y un estándar web propuesto para permitir a los anunciantes medir la eficacia de las campañas web sin comprometer la privacidad del usuario.

La función tiene pocos problemas de privacidad por sí misma, así que aunque puede optar por dejarla activada, consideramos que el hecho de que se desactive automáticamente en Navegación Privada es un indicador para desactivar la función.

#### Navegación privada siempre activa

Abre Safari y pulsa el botón Pestañas, situado en la parte inferior derecha. A continuación, despliegua la lista Grupos de pestañas.

- [x] Selecciona **Privado**

El modo de Navegación Privada de Safari ofrece protecciones de privacidad adicionales. La Navegación Privada utiliza una nueva sesión [efímera](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) para cada pestaña, lo que significa que las pestañas están aisladas unas de otras. La Navegación Privada también ofrece otras pequeñas ventajas de privacidad, como no enviar la dirección de una página web a Apple cuando se utiliza la función de traducción de Safari.

Ten en cuenta que la Navegación Privada no guarda cookies ni datos de sitios web, por lo que no podrás permanecer conectado a los sitios. Esto puede ser un inconveniente.

#### iCloud Sync

La sincronización del historial de Safari, los grupos de pestañas, las pestañas de iCloud y las contraseñas guardadas son E2EE. Sin embargo, por defecto, los marcadores [no](https://support.apple.com/HT202303) lo son. Apple puede descifrarlos y acceder a ellos de acuerdo con su [política de privacidad](https://apple.com/legal/privacy/en-ww).

Puedes activar E2EE para tus favoritos y tus descargas de Safari activando [Protección de Datos Avanzada](https://support.apple.com/HT212520). Vaya a su **Nombre de ID de Apple → iCloud → Protección de datos avanzada**.

- [x] Activa **Protección de datos avanzada**

Si utilizas iCloud con la Protección de Datos Avanzada desactivada, también te recomendamos que compruebes que la ubicación de descarga predeterminada de Safari está configurada como local en tu dispositivo. Esta opción se encuentra en :gear: **Ajustes** → **Safari** → **General** → **Descargas**.

## Criterios

**Por favor, tenga en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que usted se familiarice con esta lista, antes de decidir utilizar un proyecto y realizar su propia investigación para asegurarse de que es la elección ideal para usted.

### Requisitos Mínimos

- Debe admitir actualizaciones automáticas.
- Debe recibir las actualizaciones del motor con rapidez.
- Debe soportar el bloqueo de contenido.
- Cualquier cambio necesario para que el navegador respete más la privacidad no debería afectar negativamente a la experiencia del usuario.
