---
meta_title: "Navegadores Web para PC y Mac que Respetan la Privacidad - Privacy Guides"
title: Navegadores de Escritorio
icon: material/laptop
description: Estos navegadores que protegen la privacidad son los que recomendamos actualmente para la navegación estándar/no anónima por Internet en computadoras de escritorio.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Recomendaciones de Navegadores de Escritorio Privados
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/es/browser
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Firefox
    image: /assets/img/browsers/firefox.svg
    url: https://firefox.com
    sameAs: https://es.wikipedia.org/wiki/Firefox
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    sameAs: https://es.wikipedia.org/wiki/Brave_(web_browser)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Estos son nuestros **navegadores** recomendados y las configuraciones para la navegación estándar/no anónima por Internet. Recomendamos [Mullvad Browser](#mullvad-browser) si estás centrado en fuertes protecciones de privacidad y contra huellas digitales desde el primer momento, [Firefox](#firefox) para navegantes ocasionales que buscan una buena alternativa a Google Chrome, y [Brave](#brave) si necesitas compatibilidad con el navegador Chromium.

Si necesitas navegar por Internet de forma anónima, deberías utilizar [Tor](tor.md). Hacemos algunas recomendaciones de configuración en esta página, pero todos los navegadores que no sean Tor Browser serán rastreables por *alguien* de una forma u otra.

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** es una versión de [Tor Browser](tor.md#tor-browser) con las integraciones de la red Tor eliminadas. Su objetivo es proporcionar a los usuarios de VPN las tecnologías de navegador contra la huella digital de Tor Browser, que son protecciones clave contra la [:material-eye-outline: Vigilancia Masiva](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. Es desarrollado por el Proyecto Tor y distribuido por [Mullvad](vpn.md#mullvad), y **no** requiere el uso de la VPN de Mullvad.

[:octicons-home-16: Página Principal](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="Documentación" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Al igual que [Tor Browser](tor.md), Mullvad Browser está diseñado para evitar el fingerprinting haciendo que la huella digital de tu navegador sea idéntica a la de todos los demás usuarios de Mullvad Browser, e incluye ajustes predeterminados y extensiones que se configuran automáticamente según los niveles de seguridad por defecto: *Estándar*, *Más seguro* y *El más seguro*.

Por lo tanto, es fundamental que no modifiques el navegador en absoluto, más allá de ajustar los [niveles de seguridad](https://tb-manual.torproject.org/security-settings) por defecto. Cuando ajustes el nivel de seguridad, **deberás** reiniciar siempre el navegador antes de seguir utilizándolo. De lo contrario, [es posible que la configuración de seguridad no se aplique en su totalidad](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), exponiéndote a un riesgo de fingerprinting y exploits mayor de lo que cabría esperar en función de la configuración elegida.

Cualquier otra modificación que no sea el ajuste de esta configuración haría que tu huella digital fuera única, anulando el propósito de utilizar este navegador. Si deseas configurar tu navegador de forma más exhaustiva y la huella digital no te preocupa, te recomendamos [Firefox](#firefox) en su lugar.

### Anti Huella Digital

**Sin** usar una [VPN](vpn.md), Mullvad Browser proporciona protecciones contra [scripts de huellas digitales ingenuos ](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) similares a otros navegadores privados como Firefox+[Arkenfox](#arkenfox-advanced) o [Brave](#brave). Mullvad Browser proporciona estas protecciones desde el principio, a expensas de cierta flexibilidad y comodidad que otros navegadores privados pueden proporcionar.

==Para obtener la mayor protección contra las huellas dactilares, recomendamos usar el navegador Mullvad en conjunción **con** una VPN==, ya sea de Mullvad o de otro proveedor de VPN recomendado. Al utilizar una VPN con Mullvad Browser, compartirás una huella digital y un conjunto de direcciones IP con muchos otros usuarios, lo que le proporcionará una "multitud" con la que mezclarse. Esta estrategia es la única manera de frustrar los scripts de rastreo avanzados, y es la misma técnica contra las huellas digitales utilizada por Tor Browser.

Ten en cuenta que aunque puedes usar Mullvad Browser con cualquier proveedor de VPN, otras personas en esa VPN también deben estar usando Mullvad Browser para que exista esta «multitud», algo que es más probable con Mullvad VPN que con otros proveedores. Mullvad Browser no tiene conectividad VPN integrada, ni comprueba si estás usando una VPN antes de navegar; tu conexión VPN tiene que ser configurada y gestionada por separado.

Mullvad Browser viene con las extensiones de navegador *uBlock Origin* y *NoScript* preinstaladas. Aunque normalmente desaconsejamos añadir [extensiones](browser-extensions.md) *adicionales* al navegador, estas extensiones que vienen preinstaladas con el navegador **no** deberían ser eliminadas o configuradas fuera de sus valores por defecto, porque hacerlo haría notablemente distinta tu huella digital del navegador de otros usuarios de Mullvad Browser. También viene preinstalado con la extensión Mullvad Browser Extension, que *puede* ser eliminada de forma segura sin afectar a tu huella digital del navegador si lo deseas, pero también es seguro mantenerla incluso si no utilizas Mullvad VPN.

### Modo de Navegación Privada

Mullvad Browser funciona en modo de navegación privada permanente, lo que significa que el historial, las cookies y otros datos del sitio se borrarán siempre que se cierre el navegador. Tus marcadores y tu configuración del navegador y de las extensiones se conservarán.

Esto es necesario para evitar formas avanzadas de rastreo, pero a costa de la comodidad y de algunas funciones de Firefox, como los contenedores multicuenta. Recuerda que siempre puedes utilizar varios navegadores, por ejemplo, podrías considerar utilizar Firefox+Arkenfox para algunos sitios en los que quieras mantener la sesión iniciada o que no funcionen correctamente en Mullvad Browser, y Mullvad Browser para la navegación general.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox logo](assets/img/browsers/firefox.svg){ align=right }

**Firefox** brinda una configuración fuerte de privacidad como la [Protección de Rastreo Mejorada](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), que puede ayudar con el bloqueo de varios [tipos de rastreadores](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).

[:octicons-home-16: Página Principal](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="Documentación" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Contribuir" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Firefox incluye un [token de descarga] único (https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) en las descargas del sitio web de Mozilla y utiliza la telemetría de Firefox para enviar el token. El token **no** está incluido en las versiones de [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Configuración Recomendada de Firefox

Estas opciones se encuentran en :material-menu: → **Ajustes**.

#### Buscar

- [ ] Desmarca **Mostrar sugerencias de búsqueda**

Es posible que las funciones de sugerencia de búsqueda no estén disponibles en tu región.

Las sugerencias de búsqueda envían todo lo que escribes en la barra de direcciones al motor de búsqueda predeterminado, independientemente de si realizas una búsqueda real. Desactivar las sugerencias de búsqueda te permite controlar con mayor precisión qué datos envías al proveedor de tu motor de búsqueda.

##### Firefox Suggest (solo en EE. UU.)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) es una función similar a las sugerencias de búsqueda que solo está disponible en Estados Unidos. Recomendamos desactivarlo por la misma razón que recomendamos desactivar las sugerencias de búsqueda. Si no ves estas opciones en el encabezado de la **Barra de Direcciones**, no tienes la nueva experiencia y puedes ignorar estos cambios.

- [ ] Desmarca **Sugerencias de Firefox**
- [ ] Desmarca **Sugerencias de los patrocinadores**

#### Privacidad & Seguridad

##### Protección contra el rastreo mejorada

- [x] Selecciona **Estricto** Protección de seguimiento mejorada

Esto te protege bloqueando los rastreadores de redes sociales, los scripts de fingerprinting (ten en cuenta que esto no te protege de *todos* los fingerprinting), los criptomineros, las cookies de rastreo de sitios cruzados y algunos otros contenidos de rastreo. La ETP protege contra muchas amenazas comunes, pero no bloquea todas las vías de rastreo porque está diseñada para tener un impacto mínimo o nulo en la usabilidad del sitio.

##### Desinfectar al cerrar

Si deseas seguir conectado a determinados sitios, puedes permitir excepciones en **Cookies y datos del sitio** → **Gestionar excepciones....**

- [x] Selecciona **Eliminar cookies y datos del sitio cuando cierre Firefox**

Esto te protege de las cookies persistentes, pero no te protege de las cookies adquiridas durante una sesión de navegación. Cuando esta opción está activada, es posible limpiar fácilmente las cookies del navegador simplemente reiniciando Firefox. Puedes establecer excepciones por sitio, si deseas permanecer conectado a un sitio concreto que visites con frecuencia.

##### Telemetría

- [ ] Desmarca **Enviar datos técnicos y de interacción a Mozilla**
- [ ] Desmarca **Instalar y ejecutar estudios**
- [ ] Desmarca **Enviar automáticamente informes de fallos**

Según la política de privacidad de Mozilla para Firefox,

> Firefox envía datos sobre tu versión e idioma de Firefox; sistema operativo del dispositivo y configuración del hardware; memoria, información básica sobre fallos y errores; resultado de procesos automatizados como actualizaciones, navegación segura y activación. Cuando Firefox envía datos, tu dirección IP se recoge temporalmente como parte de los registros de nuestro servidor.

Además, el servicio de Cuentas de Mozilla recopila [algunos datos técnicos](https://mozilla.org/privacy/mozilla-accounts). Si usas una cuenta de Mozilla, puedes optar por salir:

1. Abre la [configuración de tu perfil en accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Desmarca **Recopilación y uso de datos** > **Ayuda a mejorar Cuentas de Firefox**

##### Preferencias de publicidad en sitios web

- [ ] Desmarca **Permitir que los sitios web realicen mediciones de anuncios con respeto a la privacidad**

Con el lanzamiento de Firefox 128, un nuevo ajuste para la [atribución de respeto a la privacidad](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) se ha agregado y [activado por defecto](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA permite a los anunciantes utilizar tu navegador web para medir la eficacia de las campañas web, en vez de utilizar el rastreo tradicional con JavaScript. Consideramos este comportamiento como fuera del alcance de las responsabilidades del agente de usuario y el hecho de que se encuentre desactivado por defecto en Arkenfox es una señal adicional para desactivar esta característica.

##### Modo solo-HTTPS

- [x] Selecciona **Activar el modo solo-HTTPS en todas las ventanas**

Esto evita que te conectes involuntariamente a un sitio web en texto plano HTTP. Los sitios sin HTTPS son poco comunes hoy en día, por lo que esto debería tener poco o ningún impacto en tu navegación diaria.

##### DNS sobre HTTPS

Si utilizas un [proveedor de DNS sobre HTTPS](dns.md):

- [x] Selecciona **Protección máxima** y elige un proveedor adecuado

La Protección Máxima impone el uso de DNS sobre HTTPS y una advertencia de seguridad se mostrará si Firefox no se puede conectar a un solucionador seguro de DNS, o si tu solucionador seguro de DNS dice que los registros para el dominio al que te estás intentando conectar no existe. Esto impide que la red a la que estás conectado degrade secretamente tu seguridad DNS.

#### Sincronización

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) permite que tus datos de navegación (historial, marcadores, etc.) sean accesibles desde todos tus dispositivos y los protege con E2EE.

### Arkenfox (avanzado)

<div class="admonition tip" markdown>
<p class="admonition-title">Utiliza Mullvad Browser para una protección avanzada contra las huellas digitales</p>

[Mullvad Browser](#mullvad-browser) ofrece desde el primer momento una protección contra las huellas digitales más fuerte que Firefox y no requiere el uso de la VPN de Mullvad para beneficiarse de estas protecciones. Junto con una VPN, Mullvad Browser puede frustrar scripts de rastreo más avanzados que Arkenfox no puede. Firefox sigue teniendo la ventaja de ser mucho más flexible y de permitir excepciones por sitio para los sitios web en los que es necesario permanecer conectado.

</div>

El [proyecto Arkenfox](https://github.com/arkenfox/user.js) proporciona un conjunto de opciones cuidadosamente consideradas para Firefox. Si [decides](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) utilizar Arkenfox, unas [pocas opciones](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) son subjetivamente estrictas y/o pueden hacer que algunos sitios web no funcionen correctamente ―lo cual puedes [cambiar fácilmente](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) para adaptarlo a tus necesidades―. **Recomendamos encarecidamente** leer su [wiki](https://github.com/arkenfox/user.js/wiki) completa. Arkenfox también es compatible con [contenedores](https://support.mozilla.org/kb/containers#w_for-advanced-users).

Arkenfox solo pretende neutralizar los scripts de rastreo básicos o ingenuos mediante la aleatorización del lienzo y los ajustes de configuración de resistencia al fingerprint incorporados en Firefox. No pretende hacer que tu navegador se mezcle con una gran multitud de otros usuarios de Arkenfox de la misma manera que lo hacen Mullvad Browser o Tor Browser, que es la única manera de neutralizar los scripts avanzados de rastreo de huellas digitales. Recuerda que siempre puedes utilizar varios navegadores, por ejemplo, podrías considerar utilizar Firefox+Arkenfox para algunos sitios en los que quieras mantener la sesión iniciada o en los que confíes, y Mullvad Browser para la navegación general.

## Brave

<div class="admonition recommendation annotate" markdown>

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

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Brave añade un "[código de referido](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" al nombre del archivo en las descargas desde el sitio web de Brave, que se utiliza para rastrear de qué fuente se descargó el navegador, por ejemplo `BRV002` en una descarga llamada `Brave-Browser-BRV002.pkg`. El instalador hará un ping al servidor de Brave con el código de referido al final del proceso de instalación. Si esto te preocupa, puedes cambiar el nombre del archivo de instalación antes de abrirlo.

</div>

### Configuración Recomendada de Brave

Estas opciones se encuentran en :material-menu: → **Ajustes**.

#### Escudos

Brave incluye algunas medidas contra el fingerprinting en su función [Escudos](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Te sugerimos configurar estas opciones [globalmente](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) en todas las páginas que visites.

Las opciones de los escudos pueden reducirse según las necesidades de cada sitio, pero por defecto recomendamos configurar lo siguiente:

<div class="annotate" markdown>

- [x] Selecciona **Agresivo** en *Bloqueo de rastreadores y anuncios*

<details class="warning" markdown>
<summary>Usar listas de filtros predeterminadas</summary>

Brave te permite seleccionar filtros de contenido adicionales en la página interna `brave://adblock`. Te aconsejamos que no utilices esta función; en su lugar, mantén las listas de filtros predeterminadas. El uso de listas adicionales te hará destacar entre los demás usuarios de Brave y también puede aumentar la superficie de ataque si hay un exploit en Brave y se añade una regla maliciosa a una de las listas que utilizas.

</details>

- [x] Selecciona **Estricto** en *Mejorar conexiones a HTTPS*
- [x] (Opcional) Selecciona **Bloquear scripts** (1)
- [x] Marca **Bloquear huellas digitales**
- [x] Selecciona **Bloquear cookies de terceros**
- [x] Marca **Olvidarme al cerrar este sitio** (2)
- [ ] Desmarca todos los componentes de redes sociales

</div>

1. Esta opción desactiva JavaScript, lo que romperá muchos sitios. Para arreglarlos, puedes establecer excepciones por sitio haciendo clic en el icono Escudo de la barra de direcciones y desmarcando esta opción en *Controles avanzados*.
2. Si deseas permanecer conectado a un sitio concreto que visitas a menudo, puedes establecer excepciones por sitio haciendo clic en el icono del Escudo de la barra de direcciones y desmarcando esta opción en *Controles avanzados*.

#### Privacidad y seguridad

<div class="annotate" markdown>

- [x] Selecciona **No permitir que los sitios usen la optimización de JavaScript** en *Seguridad* → *Gestionar optimización y seguridad de JavaScript* (1)
- [x] Selecciona **Quitar automáticamente los permisos de los sitios que no se usan** en *Configuración del sitio y de los Escudos*
- [x] Selecciona **Desactivar el UDP sin proxy** en [*Política de gestión de IP de WebRTC*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Desmarca **Utiliza los servicios de Google para la mensajería push**
- [x] Selecciona **Redirigir automáticamente las páginas AMP**
- [x] Selecciona **URL de seguimiento de redirección automática**
- [x] Selecciona **Impedir que los sitios obtengan mis huellas digitales en función de mis preferencias de idioma**

</div>

1. Desactivar el optimizador V8 reduce tu superficie de ataque al desactivar [*algunas*](https://grapheneos.social/@GrapheneOS/112708049232710156) partes de la compilación Just-In-Time (JIT) de JavaScript.

##### Ventanas Tor

[**Ventana privada con Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) te permite enrutar tu tráfico a través de la red Tor en Ventanas Privadas y acceder a servicios .onion, lo que puede ser útil en algunos casos. Sin embargo, Brave **no** es tan resistente al fingerprinting como Tor Browser, y mucha menos gente usa Brave con Tor, por lo que destacarás. Si tu modelo de amenaza requiere un fuerte anonimato, utiliza [Tor Browser](tor.md#tor-browser).

##### Recopilación de datos

- [ ] Desmarca **Permitir estadísticas del producto con preservación de la privacidad (P3A)**
- [ ] Desmarca **Enviar automáticamente el ping de uso diario a Brave**
- [ ] Desmarca **Enviar informes de diagnóstico automáticamente**

#### Web3

Las funciones Web3 de Brave pueden aumentar potencialmente la huella digital de tu navegador y la superficie de ataque. A menos que uses alguna de estas funciones, deberían ser desactivadas.

- Selecciona **Extensiones (sin copia de seguridad)** en *Cartera predeterminada de Ethereum*
- Selecciona **Extensiones (sin copia de seguridad)** en *Cartera predeterminada de Solana*

#### Extensiones

- [ ] Desmarca todas las extensiones integradas que no utilices

#### Motor de búsqueda

Recomendamos desactivar las sugerencias de búsqueda en Brave por la misma razón que recomendamos desactivar esta función en [Firefox](#search).

- [ ] Desmarca **Mostrar sugerencias de búsqueda**

#### Sistema

<div class="annotate" markdown>

- [ ] Desmarca **Seguir ejecutando aplicaciones en segundo plano al cerrar Brave** para desactivar las aplicaciones en segundo plano (1)

</div>

1. Esta opción no está presente en todas las plataformas.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) permite que tus datos de navegación (historial, marcadores, etc.) sean accesibles en todos tus dispositivos sin necesidad de tener una cuenta y los protege con E2EE.

#### Recompensas y Billetera de Brave

**Brave Rewards** te permite recibir la criptomoneda Basic Attention Token (BAT) por realizar ciertas acciones dentro de Brave. Depende de una cuenta de custodia y de un número selecto de proveedores. No recomendamos utilizar BAT como una [criptomoneda privada](cryptocurrency.md), ni recomendamos el uso de una [billetera de custodia](advanced/payments.md#wallet-custody), por lo que no recomendamos usar esta función.

**Brave Wallet** funciona localmente en tu ordenador, pero no admite ninguna criptomoneda privada, por lo que desaconsejamos utilizar esta función también.

## Criterios

**Por favor, ten en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

### Requisitos Mínimos

- Debe ser software de código abierto.
- Debe admitir actualizaciones automáticas.
- Debe recibir actualizaciones del motor en 0-1 días desde el lanzamiento principal.
- Debe estar disponible en Linux, macOS y Windows.
- Cualquier cambio requerido para que el navegador sea más respetuoso con la privacidad, no debe impactar negativamente la experiencia del usuario.
- Debe bloquear las cookies de terceros por defecto.
- Debe permitir la [partición de estados](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) para mitigar el rastreo entre sitios.[^1]

### Mejor Caso

Nuestro criterio del mejor caso representa lo que nos gustaría ver del proyecto perfecto en esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Incluye un bloqueador de contenido.
- Permite la compartimentación de cookies (como los [Contenedores Multicuenta](https://support.mozilla.org/kb/containers)).
- Soporta las Aplicaciones Web Progresivas (PWA). Las PWA permiten instalar determinados sitios web como si fueran aplicaciones nativas en el ordenador. Esto puede tener ventajas sobre la instalación de aplicaciones basadas en Electron porque las PWA se benefician de las actualizaciones de seguridad periódicas de tu navegador.
- No incluye complementos (bloatware) que impactan la privacidad del usuario.
- No recolecta telemetría por defecto.
- Proporciona la implementación de un servidor de sincronización de código abierto.
- Utiliza un [motor de búsqueda privado](search-engines.md) por defecto.

[^1]: La implementación de Brave se detalla en [Brave Privacy Updates: Partitioning network-state for](https://brave.com/privacy-updates/14-partitioning-network-state) privacy.
