---
title: "Navegadores de Escritorio"
icon: material/laptop
description: These web browsers provide stronger privacy protections than Google Chrome.
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

Estas son nuestras recomendaciones de navegadores web para computadoras y las configuraciones para la navegación estándar/no anónima por Internet. We recommend [Mullvad Browser](#mullvad-browser) if you are focused on strong privacy protections and anti-fingerprinting out of the box, [Firefox](#firefox) for casual internet browsers looking for a good alternative to Google Chrome, and [Brave](#brave) if you need Chromium browser compatibility.

Si necesita navegar por Internet de forma anónima, debería utilizar [Tor](tor.md). We make some configuration recommendations on this page, but all browsers other than Tor Browser will be traceable by *somebody* in some manner or another.

## Mullvad Browser

!!! recommendation

    ![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    **Mullvad Browser** is a version of [Tor Browser](tor.md#tor-browser) with Tor network integrations removed, aimed at providing Tor Browser's anti-fingerprinting browser technologies to VPN users. It is developed by the Tor Project and distributed by [Mullvad](vpn.md#mullvad), and does **not** require the use of Mullvad's VPN.
    
    [:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }
    
    ??? downloads "Descargas"
    
        - [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

Like [Tor Browser](tor.md), Mullvad Browser is designed to prevent fingerprinting by making your browser fingerprint identical to all other Mullvad Browser users, and it includes default settings and extensions that are automatically configured by the default security levels: *Standard*, *Safer* and *Safest*. Therefore, it is imperative that you do not modify the browser at all outside adjusting the default [security levels](https://tb-manual.torproject.org/security-settings/). Other modifications would make your fingerprint unique, defeating the purpose of using this browser. If you want to configure your browser more heavily and fingerprinting is not a concern for you, we recommend [Firefox](#firefox) instead.

### Anti-Fingerprinting

**Without** using a [VPN](vpn.md), Mullvad Browser provides the same protections against [naive fingerprinting scripts](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) as other private browsers like Firefox+[Arkenfox](#arkenfox-advanced) or [Brave](#brave). Mullvad Browser provides these protections out of the box, at the expense of some flexibility and convenience that other private browsers can provide.

==For the strongest anti-fingerprinting protection, we recommend using Mullvad Browser in conjunction **with** a VPN==, whether that is Mullvad or another recommended VPN provider. When using a VPN with Mullvad Browser, you will share a fingerprint and a pool of IP addresses with many other users, giving you a "crowd" to blend in with. This strategy is the only way to thwart advanced tracking scripts, and is the same anti-fingerprinting technique used by Tor Browser.

Note that while you can use Mullvad Browser with any VPN provider, other people on that VPN must also be using Mullvad Browser for this "crowd" to exist, something which is more likely on Mullvad VPN compared to other providers, particularly this close to the launch of Mullvad Browser. Mullvad Browser does not have built-in VPN connectivity, nor does it check whether you are using a VPN before browsing; your VPN connection has to be configured and managed separately.

Mullvad Browser comes with the *uBlock Origin* and *NoScript* browser extensions pre-installed. While we typically [don't recommend](#extensions) adding *additional* browser extensions, these extensions that come pre-installed with the browser should **not** be removed or configured outside their default values, because doing so would noticeably make your browser fingerprint distinct from other Mullvad Browser users. It also comes pre-installed with the Mullvad Browser Extension, which *can* be safely removed without impacting your browser fingerprint if you would like, but is also safe to keep even if you don't use Mullvad VPN.

### Private Browsing Mode

Mullvad Browser operates in permanent private browsing mode, meaning your history, cookies, and other site data will always be cleared every time the browser is closed. Your bookmarks, browser settings, and extension settings will still be preserved.

This is required to prevent advanced forms of tracking, but does come at the cost of convenience and some Firefox features, such as Multi-Account Containers. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise don't work properly in Mullvad Browser, and Mullvad Browser for general browsing.

### Mullvad Leta

Mullvad Browser comes with DuckDuckGo set as the default [search engine](search-engines.md), but it also comes preinstalled with **Mullvad Leta**, a search engine which requires an active Mullvad VPN subscription to access. Mullvad Leta queries Google's paid search API directly (which is why it is limited to paying subscribers), however because of this limitation it is possible for Mullvad to correlate search queries and Mullvad VPN accounts. For this reason we discourage the use of Mullvad Leta, even though Mullvad collects very little information about their VPN subscribers.

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

Estas opciones se encuentran en :material-menu: → **Ajustes** → **Privacidad y seguridad**.

##### Protección antirrastreo mejorada

- [x] Seleccione **Estricto** Protección de seguimiento mejorada

Esto le protege bloqueando los rastreadores de redes sociales, las secuencias de comandos de huellas digitales (ten en cuenta que esto no le protege de *todas* las huellas digitales), los criptomineros, las cookies de rastreo de sitios cruzados y algunos otros contenidos de rastreo. ETP protege contra muchas amenazas comunes, pero no bloquea todas las vías de rastreo porque está diseñado para tener un impacto mínimo o nulo en la usabilidad del sitio.

##### Desinfectar al cerrar

Si deseas seguir conectado a determinados sitios, puede permitir excepciones en **Cookies y datos del sitio** → **Administrar excepciones....**

- [x] Marque **Eliminar cookies y datos del sitio cuando se cierra Firefox**

Esto le protege de las cookies persistentes, pero no le protege de las cookies adquiridas durante una sesión de navegación. Cuando esta opción está activada, es posible limpiar fácilmente las cookies del navegador simplemente reiniciando Firefox. Puedes establece excepciones por sitio, si desea permanecer conectado a un sitio concreto que visite con frecuencia.

##### Buscar sugerencias

- [ ] Desmarque **Proporcionar sugerencias de búsqueda**

Es posible que las funciones de sugerencia de búsqueda no estén disponibles en su región.

Las sugerencias de búsqueda envían todo lo que escribe en la barra de direcciones al motor de búsqueda predeterminado, independientemente de si realiza una búsqueda real. Desactivar las sugerencias de búsqueda le permite controlar con mayor precisión los datos que envía al proveedor de su motor de búsqueda.

##### Telemetría

- [ ] Desmarque **Permitir que Firefox envíe infromación técnica y de interacción a Mozilla**
- [ ] Desmarque **Permitir Firefox para instalar y ejecutar estudios**
- [ ] Desmarque **Permitir que Firefox envié informes de fallos acumulados en tu nombre**

> Firefox envía datos sobre su versión e idioma de Firefox; sistema operativo del dispositivo y configuración del hardware; memoria, información básica sobre fallos y errores; resultado de procesos automatizados como actualizaciones, navegación segura y activación. Cuando Firefox envía datos, su dirección IP se recoge temporalmente como parte de los registros de nuestro servidor.

Además, el servicio Firefox Accounts recoge [algunos datos técnicos](https://www.mozilla.org/en-US/privacy/firefox/#firefox-accounts). Si usa una cuenta de Firefox, puede excluir:

1. Abra la [configuración de su perfil en accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Desmarque **Recopilación y uso de datos** > **Ayuda a mejorar Cuentas de Firefox**

##### Modo solo HTTPS

- [x] Seleccione **Habilitar el modo solo HTTPS en todas las ventanas**

Esto evita que se conecte involuntariamente a un sitio web en texto plano HTTP. Los sitios sin HTTPS son poco comunes hoy en día, por lo que esto debería tener poco o ningún impacto en su navegación diaria.

### Firefox Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) permite que sus datos de navegación (historial, marcadores, etc.) sean accesibles en todos sus dispositivos y los protege con E2EE.

### Arkenfox (avanzado)

!!! tip "Use Mullvad Browser for advanced anti-fingerprinting"

    [Mullvad Browser](#mullvad-browser) provides the same anti-fingerprinting protections as Arkenfox out of the box, and does not require the use of Mullvad's VPN to benefit from these protections. Coupled with a VPN, Mullvad Browser can thwart more advanced tracking scripts which Arkenfox cannot. Arkenfox still has the advantage of being much more flexible, and allowing per-site exceptions for websites which you need to stay logged in to.

El [proyecto Arkenfox](https://github.com/arkenfox/user.js) proporciona un conjunto de opciones cuidadosamente consideradas para Firefox. Si [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) utilizar Arkenfox, unas [pocas opciones](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) son subjetivamente estrictas y/o pueden hacer que algunos sitios web no funcionen correctamente - [lo que puede cambiar fácilmente](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) para adaptarse a sus necesidades. Nosotros **recomendamos encarecidamente** que lea su [wiki ](https://github.com/arkenfox/user.js/wiki)(lamentablemente solo en inglés). Arkenfox también permite el soporte de [contenedores](https://support.mozilla.org/en-US/kb/containers#w_for-advanced-users).

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

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

##### Protecciones

Brave incluye algunas medidas anti-fingerprinting en su función de [Escudos](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-). Sugerimos configurar estas opciones [globalmente](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) en todas las páginas que visite.

Las opciones de los escudos pueden reducirse según las necesidades de cada sitio, pero por defecto recomendamos configurar lo siguiente:

<div class="annotate" markdown>

- [x] Seleccione **Impedir que los sitios obtengan mis huellas digitales en función de mis preferencias de idioma**
- [x] Selecciona * * Agresivo * * en Bloqueo de rastreadores y anuncios

    ??? advertencia "Use listas de filtros predeterminadas"
        Brave le permite seleccionar filtros de contenido adicionales dentro de la página interna `brave://adblock`. Le aconsejamos que no utilice esta función; en su lugar, mantenga las listas de filtros predeterminadas. El uso de listas adicionales le hará destacar entre los demás usuarios de Brave y también puede aumentar la superficie de ataque si hay un exploit en Brave y se añade una regla maliciosa a una de las listas que utiliza.

- [x] (Opcional) Seleccione **Bloquear Scripts** (1)
- [x] Seleccione **Estricto, puede dañar los sitios** en Bloquear huellas digitales

</div>

1. Esta opción proporciona una funcionalidad similar a los [modos de bloqueo ](https://github.com/gorhill/uBlock/wiki/Blocking-mode)avanzados de uBlock Origin o la extensión [NoScript](https://noscript.net/).

##### Bloqueo de RRSS

- [ ] Desmarque todos los componentes de redes sociales

##### Privacidad y seguridad

<div class="annotate" markdown>

- [x] Selecciona **Desactivar UDP no proxy** en [Política de gestión de IP de WebRTC](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Desmarca **Utilizar los servicios de Google para la mensajería push**
- [ ] Desmarca **Permitir análisis de productos que preservan la privacidad (P3A)**
- ¡[ ] Desmarcar **Enviar automáticamente ping de uso diario a Brave**
- [ ] Desmarca **Enviar automáticamente informes de diagnóstico**
- [x] Selecciona **Usar siempre conexiones seguras** en el menú **Seguridad**
- [ ] Desmarca **Ventana privada con Tor** (1)

    !!! consejo "Desinfectar al cerrar"
        - [x] Selecciona **Borrar cookies y datos de sitios al cerrar todas las ventanas** en el menú *Cookies y otros datos de sitios*

        Si deseas permanecer conectado a un sitio concreto que visitas con frecuencia, puedes establecer excepciones por sitio en la sección *Comportamientos personalizados*.

</div>

1. Brave **no** es tan resistente a las huellas dactilares como Tor Browser y mucha menos gente usa Brave con Tor, así que usted destacará. Cuando se requiera un [fuerte anonimato](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-) utilice [Tor Browser ](tor.md#tor-browser).

##### Extensiones

Desactive las extensiones integradas que no utilice en **Extensiones**

- [ ] Desmarca **Hangouts**
- [ ] Desmarca **WebTorrent**

##### Web3

<div class="annotate" markdown>

- [x] Selecciona Deshabilitado en Método para resolver los recursos IPFS (1)

</div>

1. El Sistema de Archivos InterPlanetario (IPFS) es una red descentralizada, de igual a igual, para almacenar y compartir datos en un sistema de archivos distribuido. A menos que utilice la función, desactívela.

##### Ajustes Adicionales

En el menú *Sistema*

<div class="annotate" markdown>

- [ ] Desmarca **Seguir ejecutando aplicaciones en segundo plano al cerrar Brave** para desactivar las aplicaciones en segundo plano (1)

</div>

1. Esta opción no está presente en todas las plataformas.

### Brave Sync

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) permite que sus datos de navegación (historial, marcadores, etc.) sean accesibles en todos sus dispositivos sin necesidad de una cuenta y los protege con E2EE.

## Recursos Adicionales

In general, we recommend keeping your browser extensions to a minimum to decrease your attack surface; they have privileged access within your browser, require you to trust the developer, can make you [stand out](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), and [weaken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) site isolation. Sin embargo, uBlock Origin puede resultarte útil si valoras la funcionalidad de bloqueo de contenidos.

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

    Estamos trabajando en establecer criterios definidos para cada sección de nuestra página, y esto puede estar sujeto a cambios. Si tiene alguna duda sobre nuestros criterios, por favor [pregunte en nuestro foro](https://discuss.privacyguides.net/latest) y no asuma que no hemos tenido en cuenta algo a la hora de hacer nuestras recomendaciones si no aparece aquí. Son muchos los factores que se tienen en cuenta y se debaten cuando recomendamos un proyecto, y documentar cada uno de ellos es un trabajo en curso.

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
