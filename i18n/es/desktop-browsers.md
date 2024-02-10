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

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Al igual que [Tor Browser](tor.md), Mullvad Browser está diseñado para evitar el fingerprinting haciendo que la huella digital de tu navegador sea idéntica a la de todos los demás usuarios de Mullvad Browser, e incluye ajustes por defecto y extensiones que se configuran automáticamente según los niveles de seguridad por defecto: *Standard*, *Safer* y *Safest*. Por lo tanto, es imperativo que no modifiques el navegador en absoluto, más allá de ajustar los [niveles de seguridad](https://tb-manual.torproject.org/security-settings/) por defecto. Otras modificaciones harían que tu huella digital fuera única, anulando el propósito de utilizar este navegador. Si deseas configurar tu navegador de forma más exhaustiva y la huella digital no te preocupa, te recomendamos [Firefox](#firefox) en su lugar.

### Anti Huella Digital

**Sin** utilizar una VPN [](vpn.md), Mullvad Browser proporciona las mismas protecciones contra [scripts primitivos de huellas digitales](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) que otros navegadores privados como Firefox+[Arkenfox](#arkenfox-advanced) o [Brave](#brave). Mullvad Browser proporciona estas protecciones desde el principio, a expensas de cierta flexibilidad y comodidad que otros navegadores privados pueden proporcionar.

==Para obtener la mayor protección contra las huellas dactilares, recomendamos usar el navegador Mullvad en conjunción **con** una VPN==, ya sea de Mullvad o de otro proveedor de VPN recomendado. Al utilizar una VPN con Mullvad Browser, compartirás una huella digital y un conjunto de direcciones IP con muchos otros usuarios, lo que le proporcionará una "multitud" con la que mezclarse. Esta estrategia es la única manera de frustrar los scripts de rastreo avanzados, y es la misma técnica contra las huellas digitales utilizada por Tor Browser.

Ten en cuenta que aunque puedes usar Mullvad Browser con cualquier proveedor de VPN, otras personas en esa VPN también deben estar usando Mullvad Browser para que exista esta "multitud", algo que es más probable en Mullvad VPN en comparación con otros proveedores, especialmente tan cerca del lanzamiento de Mullvad Browser. Mullvad Browser no tiene conectividad VPN integrada, ni comprueba si estás usando una VPN antes de navegar; tu conexión VPN tiene que ser configurada y gestionada por separado.

Mullvad Browser viene con las extensiones de navegador *uBlock Origin* y *NoScript* preinstaladas. Aunque normalmente [no recomendamos](#extensions) añadir extensiones de navegador *adicionales*, estas extensiones que vienen preinstaladas con el navegador **no** deben ser eliminadas o configuradas fuera de sus valores por defecto, ya que hacerlo haría tu huella digital del navegador notablemente distinta de la de otros usuarios de Mullvad Browser. También viene preinstalado con la extensión Mullvad Browser Extension, que *puede* ser eliminada de forma segura sin afectar a tu huella digital del navegador si lo deseas, pero también es seguro mantenerla incluso si no utilizas Mullvad VPN.

### Modo de Navegación Privada

Mullvad Browser funciona en modo de navegación privada permanente, lo que significa que el historial, las cookies y otros datos del sitio se borrarán siempre que se cierre el navegador. Tus marcadores y tu configuración del navegador y de las extensiones se conservarán.

Esto es necesario para evitar formas avanzadas de rastreo, pero a costa de la comodidad y de algunas funciones de Firefox, como los contenedores multicuenta. Recuerda que siempre puedes utilizar varios navegadores, por ejemplo, podrías considerar utilizar Firefox+Arkenfox para algunos sitios en los que quieras mantener la sesión iniciada o que no funcionen correctamente en Mullvad Browser, y Mullvad Browser para la navegación general.

### Mullvad Leta

Mullvad Browser viene con DuckDuckGo configurado como [motor de búsqueda](search-engines.md) por defecto, pero también viene preinstalado con **Mullvad Leta**, un motor de búsqueda que requiere una suscripción activa a Mullvad VPN para poder acceder. Mullvad Leta consulta directamente la API de búsqueda de pago de Google (razón por la cual está limitada a los suscriptores de pago), sin embargo, debido a esta limitación, es posible que Mullvad correlacione las consultas de búsqueda y las cuentas VPN de Mullvad. Por este motivo, desaconsejamos el uso de Mullvad Leta, a pesar de que Mullvad recopila muy poca información sobre sus suscriptores de VPN.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox logo](assets/img/browsers/firefox.svg){ align=right }

**Firefox** brinda una configuración fuerte de privacidad como la [Protección de Rastreo Mejorada](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), que puede ayudar con el bloqueo de varios [tipos de rastreadores](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.mozilla.org/privacy/firefox/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://firefox-source-docs.mozilla.org/){ .card-link title=Documentation}
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org/){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://www.mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://www.mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://www.mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Firefox includes a unique [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) in downloads from Mozilla's website and uses telemetry in Firefox to send the token. The token is **not** included in releases from the [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Configuración Recomendada

Estas opciones se encuentran en :material-menu: → **Ajustes**

#### Buscar

- [ ] Desmarca **Proporcionar sugerencias de búsqueda**

Es posible que las funciones de sugerencia de búsqueda no estén disponibles en tu región.

Las sugerencias de búsqueda envían todo lo que escribes en la barra de direcciones al motor de búsqueda predeterminado, independientemente de si realizas una búsqueda real. Desactivar las sugerencias de búsqueda te permite controlar con mayor precisión los datos que envías al proveedor de tu motor de búsqueda.

#### Privacidad y seguridad

##### Protección contra el rastreo mejorada

- [x] Selecciona **Estricto** Protección de seguimiento mejorada

Esto te protege bloqueando los rastreadores de redes sociales, las secuencias de comandos de huellas digitales (ten en cuenta que esto no te protege de *todas* las huellas digitales), los criptomineros, las cookies de rastreo de sitios cruzados y algunos otros contenidos de rastreo. ETP protege contra muchas amenazas comunes, pero no bloquea todas las vías de rastreo porque está diseñado para tener un impacto mínimo o nulo en la usabilidad del sitio.

##### Firefox Suggest (solo en EE. UU.)

[Firefox Suggest](https://support.mozilla.org/en-US/kb/firefox-suggest) es una función similar a las sugerencias de búsqueda que sólo está disponible en Estados Unidos. Recomendamos desactivarlo por la misma razón que recomendamos desactivar las sugerencias de búsqueda. Si no ves estas opciones en lel encabezado de la **Barra de Direcciones**, no tienes la nueva experiencia y puedes ignorar estos cambios.

- [ ] Desmarca **Suggestions from the web**
- [ ] Desmarque **Suggestions from sponsors**

##### Desinfectar al cerrar

Si deseas seguir conectado a determinados sitios, puedes permitir excepciones en **Cookies y datos del sitio** → **Gestionar excepciones....**

- [x] Selecciona **Eliminar cookies y datos del sitio cuando cierre Firefox**

Esto te protege de las cookies persistentes, pero no te protege de las cookies adquiridas durante una sesión de navegación. Cuando esta opción está activada, es posible limpiar fácilmente las cookies del navegador simplemente reiniciando Firefox. Puedes establecer excepciones por sitio, si deseas permanecer conectado a un sitio concreto que visites con frecuencia.

##### Telemetría

- [ ] Desmarca **Permitir a Firefox enviar datos técnicos y de interacción a Mozilla**
- [ ] Desmarca **Permitir que Firefox instale y ejecute estudios**
- [ ] Desmarca **Permitir que Firefox envíe informes de fallos acumulados en su nombre**

> Firefox envía datos sobre tu versión e idioma de Firefox; sistema operativo del dispositivo y configuración del hardware; memoria, información básica sobre fallos y errores; resultado de procesos automatizados como actualizaciones, navegación segura y activación. Cuando Firefox envía datos, tu dirección IP se recoge temporalmente como parte de los registros de nuestro servidor.

Además, el servicio Firefox Accounts recoge [algunos datos técnicos](https://www.mozilla.org/en-US/privacy/firefox/#firefox-accounts). Si usas una cuenta de Firefox, puedes excluir:

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

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) permite que tus datos de navegación (historial, marcadores, etc.) sean accesibles desde todos tus dispositivos y los protege con E2EE.

### Arkenfox (avanzado)

<div class="admonition tip" markdown>
<p class="admonition-title">Use Mullvad Browser for advanced anti-fingerprinting</p>

[Mullvad Browser](#mullvad-browser) proporciona las mismas protecciones anti-fingerprinting que Arkenfox, y no requiere el uso de la VPN de Mullvad para beneficiarse de estas protecciones. Junto con una VPN, Mullvad Browser puede frustrar scripts de rastreo más avanzados que Arkenfox no puede. Arkenfox sigue teniendo la ventaja de ser mucho más flexible y de permitir excepciones por sitio para los sitios web en los que es necesario permanecer conectado.

</div>

El [proyecto Arkenfox](https://github.com/arkenfox/user.js) proporciona un conjunto de opciones cuidadosamente consideradas para Firefox. Si [decides](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) utilizar Arkenfox, unas [pocas opciones](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) son subjetivamente estrictas y/o pueden hacer que algunos sitios web no funcionen correctamente - [que puede cambiar fácilmente](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) para adaptarse a tus necesidades. Nosotros **recomendamos encarecidamente** que leas su [wiki ](https://github.com/arkenfox/user.js/wiki)(lamentablemente solo en inglés). Arkenfox también permite el soporte de [contenedores](https://support.mozilla.org/en-US/kb/containers#w_for-advanced-users).

Arkenfox sólo pretende frustrar los scripts de rastreo básicos o primitivos mediante la aleatorización del lienzo (canvas randomization) y los ajustes de configuración de resistencia a las huellas digitales incorporados en Firefox. No pretende hacer que tu navegador se mezcle con una gran multitud de otros usuarios de Arkenfox de la misma manera que lo hacen Mullvad Browser o Tor Browser, que es la única manera de frustrar los scripts avanzados de rastreo de huellas dactilares. Recuerda que siempre puedes utilizar varios navegadores, por ejemplo, podrías considerar utilizar Firefox+Arkenfox para algunos sitios en los que quieras mantener la sesión iniciada o en los que confíes, y Mullvad Browser para la navegación general.

## Brave

<div class="admonition recommendation annotate" markdown>

![Logo de Brave](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** incluye un bloqueador de contenidos integrado y [funciones de privacidad](https://brave.com/privacy-features/), muchas de las cuales están activadas por defecto.

Brave se basa en el proyecto de navegador web Chromium, por lo que debería resultar familiar y tener mínimos problemas de compatibilidad con sitios web.

[:octicons-home-16: Homepage](https://brave.com/){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-windows11: Windows](https://brave.com/download/)
- [:simple-apple: macOS](https://brave.com/download/)
- [:simple-linux: Linux](https://brave.com/linux/) (1)

</details>

</div>

1. Desaconsejamos el uso de la versión Flatpak de Brave, ya que sustituye el sandbox de Chromium por el de Flatpak, que es menos efectivo. Además, el paquete no es mantenido por Brave Software, Inc.

**Usuarios de macOS:** La descarga de Brave Browser desde su web oficial es un instalador `.pkg` que requiere privilegios de administrador para ejecutarse (y puede ejecutar otros scripts innecesarios en tu máquina). Como alternativa, puedes descargar el último archivo `Brave-Browser-universal.dmg` de su página [GitHub releases](https://github.com/brave/brave-browser/releases/latest), que proporciona una instalación tradicional de "arrastrar a la carpeta Aplicaciones".

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Brave añade un "[código de referido](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" al nombre del archivo en las descargas desde el sitio web de Brave, que se utiliza para rastrear de qué fuente se descargó el navegador, por ejemplo `BRV002` en una descarga llamada `Brave-Browser-BRV002.pkg`. El instalador hará un ping al servidor de Brave con el código de referido al final del proceso de instalación. Si esto te preocupa, puedes cambiar el nombre del archivo de instalación antes de abrirlo.

</div>

### Configuración Recomendada

Estas opciones se encuentran en :material-menu: → **Configuración**.

#### Ajustes

##### Escudos

Brave incluye algunas medidas anti-fingerprinting en su función de [Escudos](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-). Sugerimos configurar estas opciones [globalmente](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) en todas las páginas que visite.

Las opciones de los escudos pueden reducirse según las necesidades de cada sitio, pero por defecto recomendamos configurar lo siguiente:

<div class="annotate" markdown>

- [x] Select **Prevent sites from fingerprinting me based on my language preferences**
- [x] Select **Aggressive** under Trackers & ads blocking

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. Te aconsejamos que no utilices esta función; en su lugar, mantén las listas de filtros predeterminadas. El uso de listas adicionales te hará destacar entre los demás usuarios de Brave y también puede aumentar la superficie de ataque si hay un exploit en Brave y se añade una regla maliciosa a una de las listas que utilizas.

</details>

- [x] Selecciona **Estricto** en **Mejorar conexiones a HTTPS**
- [x] (Opcional) Selecciona **Bloquear Scripts** (1)
- [x] Selecciona **Estricto, puede dañar los sitios** en Bloquear huellas digitales
- [x] Marca **Olvídame cuando cierre este sitio** (2)

</div>

1. Esta opción proporciona una funcionalidad similar a los [modos de bloqueo ](https://github.com/gorhill/uBlock/wiki/Blocking-mode)avanzados de uBlock Origin o la extensión [NoScript](https://noscript.net/).
2. Si deseas permanecer conectado a un sitio concreto que visitas a menudo, puedes establecer excepciones por sitio haciendo clic en el icono del Escudo de la barra de direcciones.

##### Bloqueo de RRSS

- [ ] Desmarca todos los componentes de redes sociales

##### Privacidad y seguridad

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP Handling Policy](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Private window with Tor** (1)

</div>

1. Brave **no** es tan resistente a las huellas digitales como Tor Browser y mucha menos gente usa Brave con Tor, así que destacarás. Cuando necesites un [fuerte anonimato](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-) utiliza [Tor Browser ](tor.md#tor-browser).

<div class="admonition tip" markdown>
<p class="admonition-title">Sanitizing on close</p>

- [x] Select **Clear cookies and site data when you close all windows** in the *Cookies and other site data* menu

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

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

#### Sincronización

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) permite que sus datos de navegación (historial, marcadores, etc.) sean accesibles en todos sus dispositivos sin necesidad de una cuenta y los protege con E2EE.

#### Brave Rewards y Wallet

**Brave Rewards** te permite recibir la criptomoneda Basic Attention Token (BAT) por realizar ciertas acciones dentro de Brave. Se basa en una cuenta de custodia y KYC de un número selecto de proveedores. No recomendamos BAT como [criptomoneda privada](cryptocurrency.md), ni tampoco recomendamos utilizar un [monedero de custodia](advanced/payments.md#other-coins-bitcoin-ethereum-etc), por lo que desaconsejamos utilizar esta función.

**Brave Wallet** funciona localmente en tu ordenador, pero no admite ninguna criptomoneda privada, por lo que desaconsejamos utilizar esta función también.

## Recursos Adicionales

En general, recomendamos mantener las extensiones al mínimo; ya que tienen acceso privilegiado dentro de su navegador y requieren que confíes en el desarrollador, pueden hacerle [destacar](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), y [debilitan](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) el aislamiento del sitio. Sin embargo, uBlock Origin puede resultarte útil si valoras la funcionalidad de bloqueo de contenidos.

### uBlock Origin

<div class="admonition recommendation" markdown>

![logo de uBlock Origin](assets/img/browsers/ublock_origin.svg){ align=right }

**uBlock Origin** es un popular bloqueador de contenidos que puede ayudarte a bloquear anuncios, rastreadores y scripts de huellas digitales.

[:octicons-repo-16: Repository](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

</details>

</div>

Te sugerimos que sigas la [documentación del desarrollador](https://github.com/gorhill/uBlock/wiki/Blocking-mode) y elijas uno de los "modos". Las listas de filtros adicionales pueden afectar al rendimiento y [pueden aumentar la superficie de ataque](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

Estas son algunas otras [listas de filtros](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) que puedes considerar añadir:

- [x] Selecciona **Privacidad** > **AdGuard URL Tracking Protection**
- Añade [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

### uBlock Origin Lite

uBlock Origin también tiene una versión "Lite" de su extensión, que ofrece un conjunto de características muy limitado en comparación con la extensión original. Sin embargo, tiene algunas ventajas distintas sobre su hermana de pleno derecho, así que puede que quieras considerarlo si...

- ...no quieres conceder permisos completos para "leer/modificar datos del sitio web" a ninguna extensión (incluso una de confianza como uBlock Origin)
- ...quieres un bloqueador de contenido más eficiente eficiente con los recursos (memoria/CPU)[^1]
- ...tu navegador solo soporta extensiones Manifest V3

<div class="admonition recommendation" markdown>

![uBlock Origin Lite logo](assets/img/browsers/ublock_origin_lite.svg){ align=right }

**uBlock Origin Lite** es un bloqueador de contenido compatible con Manifest V3. En comparación con el *uBlock Origin* original, esta extensión no requiere amplios permisos de "lectura/modificación de datos" para funcionar.

[:octicons-repo-16: Repository](https://github.com/uBlockOrigin/uBOL-home#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/uBlockOrigin/uBOL-home/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/gorhill/uBlock/tree/master/platform/mv3){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/addon/ublock-origin-lite/)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin-lite/ddkjiahejlhfcafbddmgiahcphecmpfh)

</details>

</div>

Solo recomendamos esta versión de uBlock Origin si nunca quieres hacer cambios en tus listas de filtros, porque solo soporta unas pocas listas preseleccionadas y no ofrece opciones de personalización adicionales, incluyendo la capacidad de seleccionar elementos para bloquear manualmente. Estas restricciones se deben a limitaciones en el diseño de Manifest V3.

Esta versión ofrece tres niveles de bloqueo: "Básico" funciona sin requerir ningún privilegio especial para ver y modificar el contenido del sitio, mientras que los niveles "Óptimo" y "Completo" sí requieren ese amplio permiso, pero ofrecen una mejor experiencia de filtrado con reglas cosméticas adicionales e inyecciones de scriptlet.

Si configuras el modo de filtrado predeterminado como "Óptimo" o "Completo", la extensión solicitará acceso de lectura/modificación a **todos** los sitios web que visites. Sin embargo, también tienes la opción de cambiar la configuración a "Óptima" o "Completa" en una base **por sitio** ajustando el control deslizante en el panel emergente de la extensión en cualquier sitio dado. Al hacerlo, la extensión solicitará acceso de lectura/modificación únicamente a ese sitio. Por lo tanto, si deseas aprovechar la configuración "sin permisos" de uBlock Origin Lite, probablemente deberías dejar la configuración predeterminada como "Básica" y sólo ajustarla a un nivel superior en los sitios en los que ese nivel no sea adecuado.

uBlock Origin Lite solo recibe actualizaciones de la lista de bloqueos cada vez que se actualiza la extensión desde el mercado de extensiones de su navegador, en lugar de bajo demanda. Esto significa que puedes perderte el bloqueo de nuevas amenazas durante semanas hasta que se publique una extensión completa.

## Criterios

**Por favor, ten en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

<div class="admonition example" markdown>
<p class="admonition-title">Esta sección es nueva</p>

Estamos trabajando en establecer criterios definidos para cada sección de nuestra página, y esto puede estar sujeto a cambios. Si tienes alguna duda sobre nuestros criterios, por favor [pregunta en nuestro foro](https://discuss.privacyguides.net/latest) y no asumas que no hemos tenido en cuenta algo a la hora de hacer nuestras recomendaciones si no aparece aquí. Son muchos los factores que se tienen en cuenta y se debaten cuando recomendamos un proyecto, y documentar cada uno de ellos es un trabajo en curso.

</div>

### Requisitos Mínimos

- Debe ser software de código abierto.
- Admite actualizaciones automáticas.
- Recibe actualizaciones del motor en 0-1 días desde la publicación de la versión anterior.
- Disponible para iOS, macOS y Windows.
- Cualquier cambio necesario para que el navegador respete más la privacidad no debería afectar negativamente a la experiencia del usuario.
- Bloquea las cookies de terceros por defecto.
- Admite [partición de estados](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) para mitigar el rastreo entre sitios.[^2]

### Mejor Caso

Nuestro criterio del mejor caso representa lo que nos gustaría ver del proyecto perfecto en esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Incluye funciones integradas de bloqueo de contenidos.
- Admite la compartimentación de cookies (como [Multi-Account Containers](https://support.mozilla.org/en-US/kb/containers)).
- Supports Progressive Web Apps. PWAs enable you to install certain websites as if they were native apps on your computer. Esto puede tener ventajas sobre la instalación de aplicaciones basadas en Electron, porque usted se beneficia de las actualizaciones de seguridad periódicas de su navegador.
- No incluye funciones adicionales (bloatware) que no afectan a la privacidad del usuario.
- No recopila telemetría por defecto.
- Ofrece la implementación de un servidor de sincronización de código abierto.
- Por defecto usa un [motor de búsqueda privado](search-engines.md).

### Extensión de Criterios

- No debe replicar la funcionalidad integrada del navegador o del sistema operativo.
- Debe afectar directamente a la privacidad del usuario, es decir, no debe limitarse a proporcionar información.

[^1]: uBlock Origin Lite *en sí* no consumirá recursos, ya que utiliza APIs más recientes que hacen que el navegador procese las listas de filtros de forma nativa, en lugar de ejecutar código JavaScript dentro de la extensión para gestionar el filtrado. Sin embargo, esta ventaja de recursos es solo [teórica](https://github.com/uBlockOrigin/uBOL-home/wiki/Frequently-asked-questions-(FAQ)#is-ubol-more-efficient-cpu--and-memory-wise-than-ubo), porque es posible que el código de filtrado estándar de uBlock Origin sea más eficiente que el código de filtrado nativo de tu navegador. Aún no se ha evaluado comparativamente.
[^2]: La implementación de Brave se detalla en [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state/).
