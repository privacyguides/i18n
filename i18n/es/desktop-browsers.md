---
meta_title: "Navegadores Web para PC y Mac que Respetan la Privacidad - Privacy Guides"
title: "Navegadores de Escritorio"
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

Like [Tor Browser](tor.md), Mullvad Browser is designed to prevent fingerprinting by making your browser fingerprint identical to all other Mullvad Browser users, and it includes default settings and extensions that are automatically configured by the default security levels: *Standard*, *Safer* and *Safest*.

Therefore, it is imperative that you do not modify the browser at all outside adjusting the default [security levels](https://tb-manual.torproject.org/security-settings). When adjusting the security level, you **must** always restart the browser before continuing to use it. Otherwise, [the security settings may not be fully applied](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), putting you at a higher risk of fingerprinting and exploits than you may expect based on the setting chosen.

Modifications other than adjusting this setting would make your fingerprint unique, defeating the purpose of using this browser. Si deseas configurar tu navegador de forma más exhaustiva y la huella digital no te preocupa, te recomendamos [Firefox](#firefox) en su lugar.

### Anti Huella Digital

**Sin** utilizar una VPN [](vpn.md), Mullvad Browser proporciona las mismas protecciones contra [scripts primitivos de huellas digitales](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) que otros navegadores privados como Firefox+[Arkenfox](#arkenfox-advanced) o [Brave](#brave). Mullvad Browser proporciona estas protecciones desde el principio, a expensas de cierta flexibilidad y comodidad que otros navegadores privados pueden proporcionar.

==Para obtener la mayor protección contra las huellas dactilares, recomendamos usar el navegador Mullvad en conjunción **con** una VPN==, ya sea de Mullvad o de otro proveedor de VPN recomendado. Al utilizar una VPN con Mullvad Browser, compartirás una huella digital y un conjunto de direcciones IP con muchos otros usuarios, lo que le proporcionará una "multitud" con la que mezclarse. Esta estrategia es la única manera de frustrar los scripts de rastreo avanzados, y es la misma técnica contra las huellas digitales utilizada por Tor Browser.

Ten en cuenta que aunque puedes usar Mullvad Browser con cualquier proveedor de VPN, otras personas en esa VPN también deben estar usando Mullvad Browser para que exista esta "multitud", algo que es más probable en Mullvad VPN en comparación con otros proveedores, especialmente tan cerca del lanzamiento de Mullvad Browser. Mullvad Browser no tiene conectividad VPN integrada, ni comprueba si estás usando una VPN antes de navegar; tu conexión VPN tiene que ser configurada y gestionada por separado.

Mullvad Browser viene con las extensiones de navegador *uBlock Origin* y *NoScript* preinstaladas. Aunque normalmente desaconsejamos añadir [extensiones](browser-extensions.md) *adicionales* al navegador, estas extensiones que vienen preinstaladas con el navegador **no** deberían ser eliminadas o configuradas fuera de sus valores por defecto, porque hacerlo haría notablemente distinta tu huella digital del navegador de otros usuarios de Mullvad Browser. También viene preinstalado con la extensión Mullvad Browser Extension, que *puede* ser eliminada de forma segura sin afectar a tu huella digital del navegador si lo deseas, pero también es seguro mantenerla incluso si no utilizas Mullvad VPN.

### Modo de Navegación Privada

Mullvad Browser funciona en modo de navegación privada permanente, lo que significa que el historial, las cookies y otros datos del sitio se borrarán siempre que se cierre el navegador. Tus marcadores y tu configuración del navegador y de las extensiones se conservarán.

Esto es necesario para evitar formas avanzadas de rastreo, pero a costa de la comodidad y de algunas funciones de Firefox, como los contenedores multicuenta. Recuerda que siempre puedes utilizar varios navegadores, por ejemplo, podrías considerar utilizar Firefox+Arkenfox para algunos sitios en los que quieras mantener la sesión iniciada o que no funcionen correctamente en Mullvad Browser, y Mullvad Browser para la navegación general.

### Mullvad Leta

Mullvad Browser comes with [**Mullvad Leta**](https://leta.mullvad.net) as the default search engine, which functions as a proxy to either Google or Brave search results (configurable on the Mullvad Leta homepage).

If you are a Mullvad VPN user, there is some risk in using services like Mullvad Leta which are offered by your VPN provider themselves. This is because Mullvad theoretically has access to your true IP address (via their VPN) and your search activity (via Leta), which is information a VPN is typically intended to separate. Even though Mullvad collects very little information about their VPN subscribers or Leta users, you should consider a different [search engine](search-engines.md) if this risk concerns you.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox logo](assets/img/browsers/firefox.svg){ align=right }

**Firefox** brinda una configuración fuerte de privacidad como la [Protección de Rastreo Mejorada](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), que puede ayudar con el bloqueo de varios [tipos de rastreadores](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).

[:octicons-home-16: Página Principal](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Politica de Privacidad" }
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

These options can be found in :material-menu: → **Settings**.

#### Buscar

- [ ] Desmarca **Mostrar sugerencias de búsqueda**

Search suggestion features may not be available in your region.

Search suggestions send everything you type in the address bar to the default search engine, regardless of whether you submit an actual search. Disabling search suggestions allows you to more precisely control what data you send to your search engine provider.

##### Firefox Suggest (solo en EE. UU.)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. We recommend disabling it for the same reason we recommend disabling search suggestions. If you don't see these options under the **Address Bar** header, you do not have the new experience and can ignore these changes.

- [ ] Desmarca **Sugerencias de Firefox**
- [ ] Desmarque **Suggestions from sponsors**

#### Privacidad y seguridad

##### Protección contra el rastreo mejorada

- [x] Selecciona **Estricto** Protección de seguimiento mejorada

This protects you by blocking social media trackers, fingerprinting scripts (note that this does not protect you from *all* fingerprinting), cryptominers, cross-site tracking cookies, and some other tracking content. ETP protects against many common threats, but it does not block all tracking avenues because it is designed to have minimal to no impact on site usability.

##### Desinfectar al cerrar

If you want to stay logged in to particular sites, you can allow exceptions in **Cookies and Site Data** → **Manage Exceptions...**

- [x] Selecciona **Eliminar cookies y datos del sitio cuando cierre Firefox**

This protects you from persistent cookies, but does not protect you against cookies acquired during any one browsing session. When this is enabled, it becomes possible to easily cleanse your browser cookies by simply restarting Firefox. You can set exceptions on a per-site basis, if you wish to stay logged in to a particular site you visit often.

##### Telemetría

- [ ] Desmarca **Permitir a Firefox enviar datos técnicos y de interacción a Mozilla**
- [ ] Desmarca **Permitir que Firefox instale y ejecute estudios**
- [ ] Desmarca **Permitir que Firefox envíe informes de fallos acumulados en su nombre**

According to Mozilla's privacy policy for Firefox,

> Firefox envía datos sobre tu versión e idioma de Firefox; sistema operativo del dispositivo y configuración del hardware; memoria, información básica sobre fallos y errores; resultado de procesos automatizados como actualizaciones, navegación segura y activación. Cuando Firefox envía datos, tu dirección IP se recoge temporalmente como parte de los registros de nuestro servidor.

Additionally, the Mozilla Accounts service collects [some technical data](https://mozilla.org/privacy/mozilla-accounts). If you use a Mozilla Account you can opt out:

1. Abre la [configuración de tu perfil en accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Desmarca **Recopilación y uso de datos** > **Ayuda a mejorar Cuentas de Firefox**

##### Preferencias de publicidad en sitios web

- [ ] Desmarque **Permitir que los sitios web realicen mediciones de anuncios respetuosas con la privacidad**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.

##### Modo Sólo HTTPS

- [x] Selecciona **Activar el modo solo-HTTPS en todas las ventanas**

This prevents you from unintentionally connecting to a website in plain-text HTTP. Sites without HTTPS are uncommon nowadays, so this should have little to no impact on your day-to-day browsing.

##### DNS sobre HTTPS

If you use a [DNS over HTTPS provider](dns.md):

- [x] Selecciona **Máxima protección** y elige un proveedor adecuado

Max Protection enforces the use of DNS over HTTPS, and a security warning will show if Firefox can’t connect to your secure DNS resolver, or if your secure DNS resolver says that records for the domain you are trying to access do not exist. This stops the network you're connected to from secretly downgrading your DNS security.

#### Sincronización

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (avanzado)

<div class="admonition tip" markdown>
<p class="admonition-title">Utiliza Mullvad Browser para una protección avanzada contra las huellas digitales</p>

[Mullvad Browser](#mullvad-browser) proporciona las mismas protecciones anti-fingerprinting que Arkenfox, y no requiere el uso de la VPN de Mullvad para beneficiarse de estas protecciones. Junto con una VPN, Mullvad Browser puede frustrar scripts de rastreo más avanzados que Arkenfox no puede. Arkenfox sigue teniendo la ventaja de ser mucho más flexible y de permitir excepciones por sitio para los sitios web en los que es necesario permanecer conectado.

</div>

The [Arkenfox project](https://github.com/arkenfox/user.js) provides a set of carefully considered options for Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly—which you can [easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. We **strongly recommend** reading through their full [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember that you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** incluye un bloqueador de contenidos integrado y [funciones de privacidad](https://brave.com/privacy-features/), muchas de las cuales están activadas por defecto.

Brave se basa en el proyecto de navegador web Chromium, por lo que debería resultar familiar y tener mínimos problemas de compatibilidad con sitios web.

[:octicons-home-16: Página Principal](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Servicio Onion" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Politica de Privacidad" }
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

These options can be found in :material-menu: → **Settings**.

#### Escudos

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

Las opciones de los escudos pueden reducirse según las necesidades de cada sitio, pero por defecto recomendamos configurar lo siguiente:

<div class="annotate" markdown>

- [x] Selecciona **Agresivo** en *Bloqueo de rastreadores y anuncios*

<details class="warning" markdown>
<summary>Usa listas de filtros predeterminadas</summary>

Brave te permite seleccionar filtros de contenido adicionales en la página interna `brave://adblock`. Te aconsejamos que no utilices esta función; en su lugar, mantén las listas de filtros predeterminadas. El uso de listas adicionales te hará destacar entre los demás usuarios de Brave y también puede aumentar la superficie de ataque si hay un exploit en Brave y se añade una regla maliciosa a una de las listas que utilizas.

</details>

- [x] Selecciona **Estricto** en *Mejorar conexiones a HTTPS*
- [x] (Opcional) Selecciona **Bloquear scripts** (1)
- [x] Marca **Bloquear huellas digitales**
- [x] Selecciona **Bloquear cookies de terceros**
- [x] Marca **Olvidarme al cerrar este sitio** (2)
- [ ] Desmarca todos los componentes de redes sociales

</div>

1. Esta opción desactiva JavaScript, lo que romperá muchos sitios. To fix them, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.
2. Si deseas permanecer conectado a un sitio concreto que visitas a menudo, puedes establecer excepciones por sitio haciendo clic en el icono del Escudo de la barra de direcciones y desmarcando esta opción en *Controles avanzados*.

#### Privacidad y seguridad

<div class="annotate" markdown>

- [x] Selecciona **No permitir que los sitios usen el optimizador de V8** en *Seguridad* → *Gestionar la seguridad de V8* (1)
- [x] Selecciona **Quitar automáticamente los permisos de los sitios que no se usan** en *Configuración del sitio y de los Escudos*
- [x] Selecciona **Desactivar el UDP sin proxy** en [*Política de gestión de IP de WebRTC*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Desmarca **Utiliza los servicios de Google para la mensajería push**
- [x] Selecciona **Redirigir automáticamente las páginas AMP**
- [x] Selecciona **URL de seguimiento de redirección automática**
- [x] Selecciona **Impedir que los sitios obtengan mis huellas digitales en función de mis preferencias de idioma**

</div>

1. Desactivar el optimizador V8 reduce tu superficie de ataque al desactivar [*algunas*](https://grapheneos.social/@GrapheneOS/112708049232710156) partes de la compilación Just-In-Time (JIT) de JavaScript.

##### Ventanas Tor

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) allows you to route your traffic through the Tor network in Private Windows and access .onion services, which may be useful in some cases. However, Brave is **not** as resistant to fingerprinting as the Tor Browser is, and far fewer people use Brave with Tor, so you will stand out. If your threat model requires strong anonymity, use the [Tor Browser](tor.md#tor-browser).

##### Recopilación de datos

- [ ] Desmarca **Permitir estadísticas del producto con preservación de la privacidad (P3A)**
- [ ] Desmarca **Enviar automáticamente el ping de uso diario a Brave**
- [ ] Desmarca **Enviar informes de diagnóstico automáticamente**

#### Web3

Brave's Web3 features can potentially add to your browser fingerprint and attack surface. Unless you use any of these features, they should be disabled.

- Selecciona **Extensiones (sin copia de seguridad)** en *Cartera predeterminada de Ethereum*
- Selecciona **Extensiones (sin copia de seguridad)** en *Cartera predeterminada de Solana*

#### Extensiones

- [ ] Desmarca todas las extensiones integradas que no utilices

#### Motor de búsqueda

We recommend disabling search suggestions in Brave for the same reason we recommend disabling this feature in [Firefox](#search).

- [ ] Desmarca **Mostrar sugerencias de búsqueda**

#### Sistema

<div class="annotate" markdown>

- [ ] Desmarca **Seguir ejecutando aplicaciones en segundo plano al cerrar Brave** para desactivar las aplicaciones en segundo plano (1)

</div>

1. Esta opción no está presente en todas las plataformas.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Recompensas y Billetera de Brave

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

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
