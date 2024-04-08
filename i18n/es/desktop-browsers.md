---
meta_title: "Navegadores Web para PC y Mac que Respetan la Privacidad - Privacy Guides"
title: "Navegadores de Escritorio"
icon: material/laptop
description: Estos navegadores web ofrecen protecciones de privacidad más sólidas que Google Chrome.
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

Estas son nuestras recomendaciones de navegadores web para computadoras y las configuraciones para la navegación estándar/no anónima por Internet. Recomendamos [Mullvad Browser](#mullvad-browser) si estás centrado en fuertes protecciones de privacidad y contra huellas digitales desde el primer momento, [Firefox](#firefox) para navegantes ocasionales que buscan una buena alternativa a Google Chrome, y [Brave](#brave) si necesitas compatibilidad con el navegador Chromium.

Si necesitas navegar por Internet de forma anónima, deberías utilizar [Tor](tor.md) . Hacemos algunas recomendaciones de configuración en esta página, pero todos los navegadores que no sean Tor Browser serán rastreables por *alguien* de una forma u otra.

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** es una versión de [Tor Browser](tor.md#tor-browser) con las integraciones de la red Tor eliminadas, con el objetivo de proporcionar las tecnologías de navegación anti huella digital de Tor Browser a los usuarios de VPN. Es desarrollado por el Proyecto Tor y distribuido por [Mullvad](vpn.md#mullvad), y **no** requiere el uso de la VPN de Mullvad.

[:octicons-home-16: Página Principal](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title=Documentación}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Al igual que [Tor Browser](tor.md), Mullvad Browser está diseñado para evitar el fingerprinting haciendo que la huella digital de tu navegador sea idéntica a la de todos los demás usuarios de Mullvad Browser, e incluye ajustes por defecto y extensiones que se configuran automáticamente según los niveles de seguridad por defecto: *Standard*, *Safer* y *Safest*. Por lo tanto, es imperativo que no modifiques el navegador en absoluto, más allá de ajustar los [niveles de seguridad](https://tb-manual.torproject.org/security-settings) por defecto. Otras modificaciones harían que tu huella digital fuera única, anulando el propósito de utilizar este navegador. Si deseas configurar tu navegador de forma más exhaustiva y la huella digital no te preocupa, te recomendamos [Firefox](#firefox) en su lugar.

### Anti Huella Digital

**Sin** utilizar una VPN [](vpn.md), Mullvad Browser proporciona las mismas protecciones contra [scripts primitivos de huellas digitales](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) que otros navegadores privados como Firefox+[Arkenfox](#arkenfox-advanced) o [Brave](#brave). Mullvad Browser proporciona estas protecciones desde el principio, a expensas de cierta flexibilidad y comodidad que otros navegadores privados pueden proporcionar.

==Para obtener la mayor protección contra las huellas dactilares, recomendamos usar el navegador Mullvad en conjunción **con** una VPN==, ya sea de Mullvad o de otro proveedor de VPN recomendado. Al utilizar una VPN con Mullvad Browser, compartirás una huella digital y un conjunto de direcciones IP con muchos otros usuarios, lo que le proporcionará una "multitud" con la que mezclarse. Esta estrategia es la única manera de frustrar los scripts de rastreo avanzados, y es la misma técnica contra las huellas digitales utilizada por Tor Browser.

Ten en cuenta que aunque puedes usar Mullvad Browser con cualquier proveedor de VPN, otras personas en esa VPN también deben estar usando Mullvad Browser para que exista esta "multitud", algo que es más probable en Mullvad VPN en comparación con otros proveedores, especialmente tan cerca del lanzamiento de Mullvad Browser. Mullvad Browser no tiene conectividad VPN integrada, ni comprueba si estás usando una VPN antes de navegar; tu conexión VPN tiene que ser configurada y gestionada por separado.

Mullvad Browser viene con las extensiones de navegador *uBlock Origin* y *NoScript* preinstaladas. Aunque normalmente desaconsejamos añadir [extensiones](browser-extensions.md) *adicionales* al navegador, estas extensiones que vienen preinstaladas con el navegador **no** deberían ser eliminadas o configuradas fuera de sus valores por defecto, porque hacerlo haría notablemente distinta tu huella digital del navegador de otros usuarios de Mullvad Browser. También viene preinstalado con la extensión Mullvad Browser Extension, que *puede* ser eliminada de forma segura sin afectar a tu huella digital del navegador si lo deseas, pero también es seguro mantenerla incluso si no utilizas Mullvad VPN.

### Modo de Navegación Privada

Mullvad Browser funciona en modo de navegación privada permanente, lo que significa que el historial, las cookies y otros datos del sitio se borrarán siempre que se cierre el navegador. Tus marcadores y tu configuración del navegador y de las extensiones se conservarán.

Esto es necesario para evitar formas avanzadas de rastreo, pero a costa de la comodidad y de algunas funciones de Firefox, como los contenedores multicuenta. Recuerda que siempre puedes utilizar varios navegadores, por ejemplo, podrías considerar utilizar Firefox+Arkenfox para algunos sitios en los que quieras mantener la sesión iniciada o que no funcionen correctamente en Mullvad Browser, y Mullvad Browser para la navegación general.

### Mullvad Leta

Mullvad Browser viene con DuckDuckGo configurado como [motor de búsqueda](search-engines.md) por defecto, pero también viene preinstalado con **Mullvad Leta**, un motor de búsqueda que requiere una suscripción activa a Mullvad VPN para poder acceder. Mullvad Leta queries Google's paid search API directly, which is why it is limited to paying subscribers. However, it is possible for Mullvad to correlate search queries and Mullvad VPN accounts because of this limitation. Por este motivo, desaconsejamos el uso de Mullvad Leta, a pesar de que Mullvad recopila muy poca información sobre sus suscriptores de VPN.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox logo](assets/img/browsers/firefox.svg){ align=right }

**Firefox** brinda una configuración fuerte de privacidad como la [Protección de Rastreo Mejorada](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), que puede ayudar con el bloqueo de varios [tipos de rastreadores](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title=Documentation}
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-windows11: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Firefox incluye un [token de descarga] único (https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) en las descargas del sitio web de Mozilla y utiliza la telemetría de Firefox para enviar el token. The token is **not** included in releases from the [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Configuración Recomendada de Firefox

Estas opciones se encuentran en :material-menu: → **Ajustes**

#### Buscar

- [ ] Uncheck **Show search suggestions**

Es posible que las funciones de sugerencia de búsqueda no estén disponibles en tu región.

Las sugerencias de búsqueda envían todo lo que escribes en la barra de direcciones al motor de búsqueda predeterminado, independientemente de si realizas una búsqueda real. Desactivar las sugerencias de búsqueda te permite controlar con mayor precisión los datos que envías al proveedor de tu motor de búsqueda.

##### Firefox Suggest (solo en EE. UU.)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) es una función similar a las sugerencias de búsqueda que solo está disponible en Estados Unidos. Recomendamos desactivarlo por la misma razón que recomendamos desactivar las sugerencias de búsqueda. Si no ves estas opciones en lel encabezado de la **Barra de Direcciones**, no tienes la nueva experiencia y puedes ignorar estos cambios.

- [ ] Uncheck **Suggestions from Firefox**
- [ ] Desmarque **Suggestions from sponsors**

#### Privacidad y seguridad

##### Protección contra el rastreo mejorada

- [x] Selecciona **Estricto** Protección de seguimiento mejorada

Esto te protege bloqueando los rastreadores de redes sociales, las secuencias de comandos de huellas digitales (ten en cuenta que esto no te protege de *todas* las huellas digitales), los criptomineros, las cookies de rastreo de sitios cruzados y algunos otros contenidos de rastreo. ETP protege contra muchas amenazas comunes, pero no bloquea todas las vías de rastreo porque está diseñado para tener un impacto mínimo o nulo en la usabilidad del sitio.

##### Desinfectar al cerrar

Si deseas seguir conectado a determinados sitios, puedes permitir excepciones en **Cookies y datos del sitio** → **Gestionar excepciones....**

- [x] Selecciona **Eliminar cookies y datos del sitio cuando cierre Firefox**

Esto te protege de las cookies persistentes, pero no te protege de las cookies adquiridas durante una sesión de navegación. Cuando esta opción está activada, es posible limpiar fácilmente las cookies del navegador simplemente reiniciando Firefox. Puedes establecer excepciones por sitio, si deseas permanecer conectado a un sitio concreto que visites con frecuencia.

##### Telemetría

- [ ] Desmarca **Permitir a Firefox enviar datos técnicos y de interacción a Mozilla**
- [ ] Desmarca **Permitir que Firefox instale y ejecute estudios**
- [ ] Desmarca **Permitir que Firefox envíe informes de fallos acumulados en su nombre**

> Firefox envía datos sobre tu versión e idioma de Firefox; sistema operativo del dispositivo y configuración del hardware; memoria, información básica sobre fallos y errores; resultado de procesos automatizados como actualizaciones, navegación segura y activación. Cuando Firefox envía datos, tu dirección IP se recoge temporalmente como parte de los registros de nuestro servidor.

Additionally, the Mozilla Accounts service collects [some technical data](https://mozilla.org/privacy/mozilla-accounts). If you use a Mozilla Account you can opt-out:

1. Abre la [configuración de tu perfil en accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Desmarca **Recopilación y uso de datos** > **Ayuda a mejorar Cuentas de Firefox**

##### Modo solo HTTPS

- [x] Selecciona **Activar el modo solo-HTTPS en todas las ventanas**

Esto evita que te conectes involuntariamente a un sitio web en texto plano HTTP. Los sitios sin HTTPS son poco comunes hoy en día, por lo que esto debería tener poco o ningún impacto en tu navegación diaria.

##### DNS sobre HTTPS

Si utilizas un proveedor de [DNS sobre HTTPS](dns.md):

- [x] Selecciona **Máxima protección** y elige un proveedor adecuado

La Protección Máxima impone el uso de DNS sobre HTTPS y una advertencia de seguridad se mostrará si Firefox no se puede conectar a un solucionador seguro de DNS, o si tu solucionador seguro de DNS dice que los registros para el dominio al que se está intentando conectar no existe. Esto impide que la red a la que estás conectado degrade secretamente tu seguridad DNS.

#### Sincronización

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) permite que tus datos de navegación (historial, marcadores, etc.) sean accesibles desde todos tus dispositivos y los protege con E2EE.

### Arkenfox (avanzado)

<div class="admonition tip" markdown>
<p class="admonition-title">Utiliza Mullvad Browser para una protección avanzada contra las huellas digitales</p>

[Mullvad Browser](#mullvad-browser) proporciona las mismas protecciones anti-fingerprinting que Arkenfox, y no requiere el uso de la VPN de Mullvad para beneficiarse de estas protecciones. Junto con una VPN, Mullvad Browser puede frustrar scripts de rastreo más avanzados que Arkenfox no puede. Arkenfox sigue teniendo la ventaja de ser mucho más flexible y de permitir excepciones por sitio para los sitios web en los que es necesario permanecer conectado.

</div>

El [proyecto Arkenfox](https://github.com/arkenfox/user.js) proporciona un conjunto de opciones cuidadosamente consideradas para Firefox. Si [decides](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) utilizar Arkenfox, unas [pocas opciones](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) son subjetivamente estrictas y/o pueden hacer que algunos sitios web no funcionen correctamente - [que puede cambiar fácilmente](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) para adaptarse a tus necesidades. Nosotros **recomendamos encarecidamente** que leas su [wiki ](https://github.com/arkenfox/user.js/wiki)(lamentablemente solo en inglés). Arkenfox también es compatible con [contenedores](https://support.mozilla.org/kb/containers#w_for-advanced-users).

Arkenfox sólo pretende frustrar los scripts de rastreo básicos o primitivos mediante la aleatorización del lienzo (canvas randomization) y los ajustes de configuración de resistencia a las huellas digitales incorporados en Firefox. No pretende hacer que tu navegador se mezcle con una gran multitud de otros usuarios de Arkenfox de la misma manera que lo hacen Mullvad Browser o Tor Browser, que es la única manera de frustrar los scripts avanzados de rastreo de huellas dactilares. Recuerda que siempre puedes utilizar varios navegadores, por ejemplo, podrías considerar utilizar Firefox+Arkenfox para algunos sitios en los que quieras mantener la sesión iniciada o en los que confíes, y Mullvad Browser para la navegación general.

## Brave

<div class="admonition recommendation annotate" markdown>

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

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-windows11: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

**Usuarios de macOS:** La descarga de Brave Browser desde su web oficial es un instalador `.pkg` que requiere privilegios de administrador para ejecutarse (y puede ejecutar otros scripts innecesarios en tu máquina). Como alternativa, puedes descargar el último archivo `Brave-Browser-universal.dmg` de su página [GitHub releases](https://github.com/brave/brave-browser/releases/latest), que proporciona una instalación tradicional de "arrastrar a la carpeta Aplicaciones".

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Brave añade un "[código de referido](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" al nombre del archivo en las descargas desde el sitio web de Brave, que se utiliza para rastrear de qué fuente se descargó el navegador, por ejemplo `BRV002` en una descarga llamada `Brave-Browser-BRV002.pkg`. El instalador hará un ping al servidor de Brave con el código de referido al final del proceso de instalación. Si esto te preocupa, puedes cambiar el nombre del archivo de instalación antes de abrirlo.

</div>

### Configuración Recomendada de Brave

Estas opciones se encuentran en :material-menu: → **Configuración**.

#### Ajustes

##### Escudos

Brave incluye algunas medidas antihuellas en su función [Escudos](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Te sugerimos configurar estas opciones [globalmente](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) en todas las páginas que visites.

Las opciones de los escudos pueden reducirse según las necesidades de cada sitio, pero por defecto recomendamos configurar lo siguiente:

<div class="annotate" markdown>

- [x] Selecciona **Impedir que los sitios obtengan mis huellas digitales en función de mis preferencias de idioma**
- [x] Selecciona **Agresivo** en Bloqueo de rastreadores y anuncios

<details class="warning" markdown>
<summary>Usa listas de filtros predeterminadas</summary>

Brave te permite seleccionar filtros de contenido adicionales dentro de la página interna `brave://adblock`. Te aconsejamos que no utilices esta función; en su lugar, mantén las listas de filtros predeterminadas. El uso de listas adicionales te hará destacar entre los demás usuarios de Brave y también puede aumentar la superficie de ataque si hay un exploit en Brave y se añade una regla maliciosa a una de las listas que utilizas.

</details>

- [x] Selecciona **Estricto** en **Mejorar conexiones a HTTPS**
- [x] (Opcional) Selecciona **Bloquear Scripts** (1)
- [x] Selecciona **Estricto, puede dañar los sitios** en Bloquear huellas digitales
- [x] Marca **Olvídame cuando cierre este sitio** (2)
- [ ] Desmarca todos los componentes de redes sociales

</div>

1. Esta opción proporciona una funcionalidad similar a los [modos de bloqueo](https://github.com/gorhill/uBlock/wiki/Blocking-mode) avanzados de uBlock Origin.
2. Si deseas permanecer conectado a un sitio concreto que visitas a menudo, puedes establecer excepciones por sitio haciendo clic en el icono del Escudo de la barra de direcciones.

##### Privacidad y seguridad

<div class="annotate" markdown>

- [x] Selecciona **Desactivar el UDP sin proxy** en [Política de gestión de IP de WebRTC](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Desmarca **Utiliza los servicios de Google para la mensajería push**
- [ ] Desmarca **Permitir estadísticas del producto con preservación de la privacidad (P3A)**
- [ ] Desmarca **Enviar automáticamente el ping de uso diario a Brave**
- [ ] Desmarca **Enviar informes de diagnóstico automáticamente**
- [ ] Desmarca **Ventana privada con Tor** (1)

</div>

1. Brave **no** es tan resistente a las huellas digitales como Tor Browser y mucha menos gente usa Brave con Tor, así que destacarás. Cuando se [requiera un fuerte anonimato](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity), utiliza el [Navegador Tor](tor.md#tor-browser).

<div class="admonition tip" markdown>
<p class="admonition-title">Desinfectar al cerrar</p>

- [x] En el menú *Configuración del sitio y de los Escudos*, en Contenido, después de hacer clic en el menú *Datos de sitios en el dispositivo*, selecciona **Eliminar los datos que los sitios guardan en tu dispositivo cuando cierras todas las ventanas**

Si deseas permanecer conectado a un sitio en particular que visitas con frecuencia, puedes establecer excepciones por sitio en la sección *Comportamientos personalizados*.

</div>

##### Extensiones

Desactiva las extensiones integradas que no utilice en **Extensiones**

- [ ] Desmarca **Hangouts**
- [ ] Desmarca **WebTorrent**

##### Web3

Las funciones Web3 de Brave pueden aumentar potencialmente la huella digital de tu navegador y la superficie de ataque. A menos que utilices alguna de las funciones, deberían estar desactivadas.

- Seleccione **Extensiones (sin copia de seguridad)** en Cartera predeterminada de Ethereum y Cartera predeterminada de Solana
- Establece **Método para resolver los recursos IPFS** como **Deshabilitado**

##### Sistema

<div class="annotate" markdown>

- [ ] Desmarca **Seguir ejecutando aplicaciones en segundo plano al cerrar Brave** para desactivar las aplicaciones en segundo plano (1)

</div>

1. Esta opción no está presente en todas las plataformas.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) permite que tus datos de navegación (historial, favoritos, etc.) sean accesibles en todos tus dispositivos sin necesidad de tener una cuenta y los protege con E2EE.

#### Brave Rewards y Wallet

**Brave Rewards** te permite recibir la criptomoneda Basic Attention Token (BAT) por realizar ciertas acciones dentro de Brave. Se basa en una cuenta de custodia y KYC de un número selecto de proveedores. No recomendamos BAT como [criptomoneda privada](cryptocurrency.md), ni tampoco recomendamos utilizar un [monedero de custodia](advanced/payments.md#other-coins-bitcoin-ethereum-etc), por lo que desaconsejamos utilizar esta función.

**Brave Wallet** funciona localmente en tu ordenador, pero no admite ninguna criptomoneda privada, por lo que desaconsejamos utilizar esta función también.

## Recursos Adicionales

## Criterios

**Por favor, ten en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

### Requisitos Mínimos

- Debe ser software de código abierto.
- Admite actualizaciones automáticas.
- Recibe actualizaciones del motor en 0-1 días desde la publicación de la versión anterior.
- Disponible para iOS, macOS y Windows.
- Cualquier cambio necesario para que el navegador respete más la privacidad no debería afectar negativamente a la experiencia del usuario.
- Bloquea las cookies de terceros por defecto.
- Admite la [partición de estados](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) para mitigar el rastreo entre sitios.[^1]

### Mejor Caso

Nuestro criterio del mejor caso representa lo que nos gustaría ver del proyecto perfecto en esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Incluye funciones integradas de bloqueo de contenidos.
- Admite la compartimentación de cookies (como [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Admite Aplicaciones Web Progresivas (PWA). Las PWA permiten instalar determinados sitios web como si fueran aplicaciones nativas en el ordenador. Esto puede tener ventajas sobre la instalación de aplicaciones basadas en Electron, porque usted se beneficia de las actualizaciones de seguridad periódicas de su navegador.
- No incluye funciones adicionales (bloatware) que no afectan a la privacidad del usuario.
- No recopila telemetría por defecto.
- Ofrece la implementación de un servidor de sincronización de código abierto.
- Por defecto usa un [motor de búsqueda privado](search-engines.md).

[^1]: La implementación de Brave se detalla en [Brave Privacy Updates: Partitioning network-state for](https://brave.com/privacy-updates/14-partitioning-network-state) privacy.
