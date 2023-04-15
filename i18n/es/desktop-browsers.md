---
meta_title: "Privacy Respecting Web Browsers for PC and Mac - Privacy Guides"
title: "Navegadores de Escritorio"
icon: material/laptop
description: Estos navegadores web ofrecen protecciones de privacidad más sólidas que Google Chrome.
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

!!! recommendation

    ![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    **Mullvad Browser** es una versión de [Tor Browser](tor.md#tor-browser) con las integraciones de la red Tor eliminadas, con el objetivo de proporcionar las tecnologías de navegación anti huella digital de Tor Browser a los usuarios de VPN. Es desarrollado por el Proyecto Tor y distribuido por [Mullvad](vpn.md#mullvad), y **no** requiere el uso de la VPN de Mullvad.
    
    [:octicons-home-16: Página Principal](https://mullvad.net/en/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Política de Privacidad }
    [:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=Documentación}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Código Fuente" }
    
    ??? downloads "Descargas"
    
        - [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

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

!!! recommendation

    ![Firefox logo](assets/img/browsers/firefox.svg){ align=right }
    
    **Firefox** brinda una configuración fuerte de privacidad como la [Protección de Rastreo Mejorada](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), que puede ayudar con el bloqueo de varios [tipos de rastreadores](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).
    
    [:octicons-home-16: Página Principal](https://firefox.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mozilla.org/privacy/firefox/){ .card-link title="Politica de Privacidad" }
    [:octicons-info-16:](https://firefox-source-docs.mozilla.org/){ .card-link title=Documentación}
    [:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Código Fuente" }
    [:octicons-heart-16:](https://donate.mozilla.org/){ .card-link title=Contribuir }
    
    ??? downloads "Descargas"
    
        - [:simple-windows11: Windows](https://www.mozilla.org/firefox/windows)
        - [:simple-apple: macOS](https://www.mozilla.org/firefox/mac)
        - [:simple-linux: Linux](https://www.mozilla.org/firefox/linux)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

!!! warning "Advertencia"
    Firefox incluye un [token de descarga](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) único en las descargas del sitio web de Mozilla y utiliza la telemetría de Firefox para enviar el token. El token **no** se incluye en las versiones de [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

### Configuración Recomendada

Estas opciones se encuentran en :material-menu: → **Ajustes**

#### Buscar

- [ ] Desmarca **Proporcionar sugerencias de búsqueda**

Es posible que las funciones de sugerencia de búsqueda no estén disponibles en tu región.

Las sugerencias de búsqueda envían todo lo que escribes en la barra de direcciones al motor de búsqueda predeterminado, independientemente de si realizas una búsqueda real. Desactivar las sugerencias de búsqueda te permite controlar con mayor precisión los datos que envías al proveedor de tu motor de búsqueda.

#### Privacidad & Seguridad

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

#### Sincronización

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) permite que tus datos de navegación (historial, marcadores, etc.) sean accesibles desde todos tus dispositivos y los protege con E2EE.

### Arkenfox (avanzado)

!!! tip "Consejo" "Utiliza Mullvad Browser para la protección avanzada contra huella digital"

    [Mullvad Browser](#mullvad-browser) proporciona las mismas protecciones anti-fingerprinting que Arkenfox, y no requiere el uso de la VPN de Mullvad para beneficiarse de estas protecciones. Junto con una VPN, Mullvad Browser puede frustrar scripts de rastreo más avanzados que Arkenfox no puede. Arkenfox sigue teniendo la ventaja de ser mucho más flexible y de permitir excepciones por sitio para los sitios web en los que es necesario permanecer conectado.

El [proyecto Arkenfox](https://github.com/arkenfox/user.js) proporciona un conjunto de opciones cuidadosamente consideradas para Firefox. Si [decides](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) utilizar Arkenfox, unas [pocas opciones](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) son subjetivamente estrictas y/o pueden hacer que algunos sitios web no funcionen correctamente - [que puede cambiar fácilmente](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) para adaptarse a tus necesidades. Nosotros **recomendamos encarecidamente** que leas su [wiki ](https://github.com/arkenfox/user.js/wiki)(lamentablemente solo en inglés). Arkenfox también permite el soporte de [contenedores](https://support.mozilla.org/en-US/kb/containers#w_for-advanced-users).

Arkenfox sólo pretende frustrar los scripts de rastreo básicos o primitivos mediante la aleatorización del lienzo (canvas randomization) y los ajustes de configuración de resistencia a las huellas digitales incorporados en Firefox. No pretende hacer que tu navegador se mezcle con una gran multitud de otros usuarios de Arkenfox de la misma manera que lo hacen Mullvad Browser o Tor Browser, que es la única manera de frustrar los scripts avanzados de rastreo de huellas dactilares. Recuerda que siempre puedes utilizar varios navegadores, por ejemplo, podrías considerar utilizar Firefox+Arkenfox para algunos sitios en los que quieras mantener la sesión iniciada o en los que confíes, y Mullvad Browser para la navegación general.

## Brave

!!! recommendation

    ![Logo de Brave](assets/img/browsers/brave.svg){ align=right }
    
    **Brave Browser** incluye un bloqueador de contenidos integrado y [funciones de privacidad](https://brave.com/privacy-features/), muchas de las cuales están activadas por defecto.
    
    Brave se basa en el proyecto de navegador web Chromium, por lo que debería resultar familiar y tener mínimos problemas de compatibilidad con sitios web.
    
    [:octicons-home-16: Página Principal](https://brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Servicio Onion" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Politica de Privacidad" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=Documentación}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Código Fuente" }
    
    ??? downloads "Descargas"
    
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
        - [:simple-windows11: Windows](https://brave.com/download/)
        - [:simple-apple: macOS](https://brave.com/download/)
        - [:simple-linux: Linux](https://brave.com/linux/) (1)

    1. Desaconsejamos el uso de la versión Flatpak de Brave, ya que sustituye el sandbox de Chromium por el de Flatpak, que es menos efectivo. Además, el paquete no es mantenido por Brave Software, Inc.

### Configuración Recomendada

Estas opciones se encuentran en :material-menu: → **Configuración**.

#### Configuración

##### Escudos

Brave incluye algunas medidas anti-fingerprinting en su función de [Escudos](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-). Sugerimos configurar estas opciones [globalmente](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) en todas las páginas que visite.

Las opciones de los escudos pueden reducirse según las necesidades de cada sitio, pero por defecto recomendamos configurar lo siguiente:

<div class="annotate" markdown>

- [x] Selecciona **Impedir que los sitios obtengan mis huellas digitales en función de mis preferencias de idioma**
- [x] Selecciona **Agresivo** en Bloqueo de rastreadores y anuncios

    ??? advertencia "Usa listas de filtros predeterminadas"
        Brave te permite seleccionar filtros de contenido adicionales dentro de la página interna `brave://adblock`. Te aconsejamos que no utilices esta función; en su lugar, mantén las listas de filtros predeterminadas. El uso de listas adicionales te hará destacar entre los demás usuarios de Brave y también puede aumentar la superficie de ataque si hay un exploit en Brave y se añade una regla maliciosa a una de las listas que utilizas.

- [x] (Opcional) Selecciona **Bloquear Scripts** (1)
- [x] Selecciona **Estricto, puede dañar los sitios** en Bloquear huellas digitales

</div>

1. Esta opción proporciona una funcionalidad similar a los [modos de bloqueo ](https://github.com/gorhill/uBlock/wiki/Blocking-mode)avanzados de uBlock Origin o la extensión [NoScript](https://noscript.net/).

##### Bloqueo de RRSS

- [ ] Desmarca todos los componentes de redes sociales

##### Privacidad y seguridad

<div class="annotate" markdown>

- [x] Selecciona **Desactivar el UDP sin proxy** en [Política de gestión de IP de WebRTC](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Desmarca **Utiliza los servicios de Google para la mensajería push**
- [ ] Desmarca **Permitir estadísticas del producto con preservación de la privacidad (P3A)**
- [ ] Desmarca **Enviar automáticamente el ping de uso diario a Brave**
- [ ] Desmarca **Enviar informes de diagnóstico automáticamente**
- [x] Selecciona **Usar siempre conexiones seguras** en el menú **Seguridad**
- [ ] Desmarca **Ventana privada con Tor** (1)

    !!! tip "Desinfectar al cerrar"

        - [x] Selecciona **Borrar cookies y datos de sitios al cerrar todas las ventanas** en el menú *Cookies y otros datos de sitios*

        Si deseas permanecer conectado a un sitio concreto que visitas con frecuencia, puedes establecer excepciones por sitio en la sección *Comportamientos personalizados*.

</div>

1. Brave **no** es tan resistente a las huellas digitales como Tor Browser y mucha menos gente usa Brave con Tor, así que destacarás. Cuando necesites un [fuerte anonimato](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-) utiliza [Tor Browser ](tor.md#tor-browser).

##### Extensiones

Desactiva las extensiones integradas que no utilice en **Extensiones**

- [ ] Desmarca **Hangouts**
- [ ] Desmarca **WebTorrent**

##### Web3

Las funciones Web3 de Brave pueden aumentar potencialmente la huella digital de tu navegador y la superficie de ataque. A menos que utilices alguna de las funciones, deberían estar desactivadas.

- [ ] Establece **Cartera predeterminada de Ethereum** como **Ninguno**
- [ ] Establece **Cartera predeterminada de Solana** como **Ninguno**
- [ ] Establece **Método para resolver los recursos IPFS** como **Deshabilitado

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

!!! recommendation

    ![logo de uBlock Origin](assets/img/browsers/ublock_origin.svg){ align=right }
    
    **uBlock Origin** es un popular bloqueador de contenidos que puede ayudarte a bloquear anuncios, rastreadores y scripts de huellas digitales.
    
    [:octicons-repo-16: Repositorio](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Política de Privacidad" }
    [:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Documentación}
    [:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Código Fuente" }
    
    ??? downloads "Descargas"
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

Te sugerimos que sigas la [documentación del desarrollador](https://github.com/gorhill/uBlock/wiki/Blocking-mode) y elijas uno de los "modos". Las listas de filtros adicionales pueden afectar al rendimiento y [pueden aumentar la superficie de ataque](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

##### Otras listas

Estas son algunas otras [listas de filtros](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) que puedes considerar añadir:

- [x] Selecciona **Privacidad** > **AdGuard URL Tracking Protection**
- Añade [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

## Criterios

**Por favor, ten en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

!!! example "Esta sección es nueva"

    Estamos trabajando en establecer criterios definidos para cada sección de nuestra página, y esto puede estar sujeto a cambios. Si tienes alguna duda sobre nuestros criterios, por favor [pregunta en nuestro foro](https://discuss.privacyguides.net/latest) y no asumas que no hemos tenido en cuenta algo a la hora de hacer nuestras recomendaciones si no aparece aquí. Son muchos los factores que se tienen en cuenta y se debaten cuando recomendamos un proyecto, y documentar cada uno de ellos es un trabajo en curso.

### Requisitos Mínimos

- Debe ser software de código abierto.
- Admite actualizaciones automáticas.
- Recibe actualizaciones del motor en 0-1 días desde la publicación de la versión anterior.
- Disponible para iOS, macOS y Windows.
- Cualquier cambio necesario para que el navegador respete más la privacidad no debería afectar negativamente a la experiencia del usuario.
- Bloquea las cookies de terceros por defecto.
- Admite la [partición de estados](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) para mitigar el rastreo entre sitios.[^1]

### Mejor Caso

Nuestro criterio del mejor caso representa lo que nos gustaría ver del proyecto perfecto en esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Incluye funciones integradas de bloqueo de contenidos.
- Admite la compartimentación de cookies (como [Multi-Account Containers](https://support.mozilla.org/en-US/kb/containers)).
- Soporta Progressive Web Apps.  
  Las PWA permiten instalar determinados sitios web como si fueran apps nativas en su ordenador. Esto puede tener ventajas sobre la instalación de aplicaciones basadas en Electron, porque usted se beneficia de las actualizaciones de seguridad periódicas de su navegador.
- No incluye funciones adicionales (bloatware) que no afectan a la privacidad del usuario.
- No recopila telemetría por defecto.
- Ofrece la implementación de un servidor de sincronización de código abierto.
- Por defecto usa un [motor de búsqueda privado](search-engines.md).

### Extensión de Criterios

- No debe replicar la funcionalidad integrada del navegador o del sistema operativo.
- Debe afectar directamente a la privacidad del usuario, es decir, no debe limitarse a proporcionar información.

[^1]: La implementación de Brave se detalla en [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state/).
