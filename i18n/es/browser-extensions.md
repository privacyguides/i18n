---
title: Extensiones de Navegador
icon: material/puzzle-outline
description: Estas extensiones de navegador pueden mejorar tu experiencia de navegación y proteger tu privacidad.
cover: browser-extensions.webp
---

En general, recomendamos mantener las extensiones del navegador al mínimo para reducir la superficie de ataque. Tienen acceso privilegiado dentro de tu navegador, requieren que confíes en el desarrollador, pueden hacerte [destacar](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), y [debilitar](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) el aislamiento del sitio.

Sin embargo, algunas ofrecen funcionalidades que pueden compensar estos inconvenientes en determinadas situaciones, especialmente cuando se trata de [bloqueo de contenidos](basics/common-threats.md#mass-surveillance-programs).

No instales extensiones que no necesites de inmediato o que dupliquen la funcionalidad de tu navegador. Por ejemplo, los usuarios de [Brave](desktop-browsers.md#brave) no necesitan instalar uBlock Origin, porquel los Escudos de Brave ya ofrece la misma funcionalidad.

## Bloqueadores de Contenidos

### uBlock Origin

<div class="admonition recommendation" markdown>

![uBlock Origin logo](assets/img/browsers/ublock_origin.svg){ align=right }

**uBlock Origin** es un popular bloqueador de contenidos que puede ayudarte a bloquear anuncios, rastreadores y scripts de huellas digitales.

[:octicons-repo-16: Repositorio](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

</details>

</div>

Sugerimos seguir la [documentación del desarrollador](https://github.com/gorhill/uBlock/wiki/Blocking-mode) y elegir uno de los "modos". Las listas de filtros adicionales pueden afectar al rendimiento y [pueden aumentar la superficie de ataque](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

Estas son algunas otras [listas de filtros](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) que puedes considerar añadir:

- [x] Marca **Privacidad** > **Protección de Rastreo de URL de AdGuard**
- Añade [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

### uBlock Origin Lite

uBlock Origin también tiene una versión "Lite" de su extensión, que ofrece un conjunto de características muy limitado en comparación con la extensión original. Sin embargo, tiene algunas ventajas distintas sobre su hermana de pleno derecho, así que puede que quieras considerarlo si...

- ...no quieres conceder permisos completos para "leer/modificar datos del sitio web" a ninguna extensión (incluso una de confianza como uBlock Origin)
- ...quieres un bloqueador de contenidos[^1] más eficiente en cuanto a recursos (memoria/CPU)
- ...tu navegador solo soporta extensiones Manifest V3

<div class="admonition recommendation" markdown>

![uBlock Origin Lite logo](assets/img/browsers/ublock_origin_lite.svg){ align=right }

**uBlock Origin Lite** es un bloqueador de contenidos compatible con Manifest V3. En comparación con el _uBlock Origin_ original, esta extensión no requiere amplios permisos de "lectura/modificación de datos" para funcionar.

[:octicons-repo-16: Repository](https://github.com/uBlockOrigin/uBOL-home#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uBlockOrigin/uBOL-home/wiki/Privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/uBlockOrigin/uBOL-home/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/gorhill/uBlock/tree/master/platform/mv3){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/addon/ublock-origin-lite)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin-lite/ddkjiahejlhfcafbddmgiahcphecmpfh)

</details>

</div>

Solo recomendamos esta versión de uBlock Origin si nunca quieres hacer cambios en tus listas de filtros, porque solo soporta unas pocas listas preseleccionadas y no ofrece opciones de personalización adicionales, incluyendo la capacidad de seleccionar elementos para bloquear manualmente. Estas restricciones se deben a limitaciones en el diseño de Manifest V3.

Esta versión ofrece tres niveles de bloqueo: "Básico" funciona sin requerir ningún privilegio especial para ver y modificar el contenido del sitio, mientras que los niveles "Óptimo" y "Completo" sí requieren ese amplio permiso, pero ofrecen una mejor experiencia de filtrado con reglas cosméticas adicionales e inyecciones de scriptlet.

Si estableces el modo de filtrado predeterminado en "Óptimo" o "Completo", la extensión solicitará acceso de lectura/modificación a **todos** los sitios web que visites. Sin embargo, también tienes la opción de cambiar la configuración a "Óptima" o "Completa" **por sitio** ajustando el control deslizante en el panel emergente de la extensión en un sitio determinado. Al hacerlo, la extensión solicitará acceso de lectura/modificación únicamente a ese sitio. Por lo tanto, si deseas aprovechar la configuración "sin permisos" de uBlock Origin Lite, probablemente deberías dejar la configuración predeterminada como "Básica" y solo ajustarla a un nivel superior en los sitios en los que ese nivel no sea adecuado.

uBlock Origin Lite solo recibe actualizaciones de la lista de bloqueos cada vez que se actualiza la extensión desde el mercado de extensiones de tu navegador, en lugar de bajo demanda. Esto significa que puedes perderte el bloqueo de nuevas amenazas durante semanas hasta que se publique una extensión completa.

### AdGuard

Recomendamos [Safari](mobile-browsers.md#safari) para los usuarios de iOS, que lamentablemente no es compatible con uBlock Origin. Por suerte, Adguard ofrece una alternativa adecuada:

<div class="admonition recommendation" markdown>

![AdGuard logo](assets/img/browsers/adguard.svg){ align=right }

**AdGuard for iOS** es una extensión de bloqueo de contenidos gratuita y de código abierto para Safari que utiliza la [Content Blocker API] nativa (https://developer.apple.com/documentation/safariservices/creating_a_content_blocker).

[:octicons-home-16: Página Principal](https://adguard.com/en/adguard-ios/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/ios.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1047223162)

</details>

</div>

Las listas de filtros adicionales ralentizan las cosas y pueden aumentar su superficie de ataque, así que aplique sólo lo que necesite. AdGuard para iOS tiene algunas funciones premium; sin embargo, el bloqueo de contenidos estándar de Safari es gratuito.

## Criterios

- No debe replicar la funcionalidad integrada del navegador o del sistema operativo.
- Debe afectar directamente a la privacidad del usuario, es decir, no debe limitarse a proporcionar información.

[^1]: uBlock Origin Lite _en sí mismo_ no consumirá recursos, ya que utiliza API más recientes que hacen que el navegador procese las listas de filtros de forma nativa, en lugar de ejecutar código JavaScript dentro de la extensión para gestionar el filtrado. Sin embargo, esta ventaja de recursos es solo [teórica](https://github.com/uBlockOrigin/uBOL-home/wiki/Frequently-asked-questions-\(FAQ\)#is-ubol-more-efficient-cpu--and-memory-wise-than-ubo), porque es posible que el código de filtrado estándar de uBlock Origin sea más eficiente que el código de filtrado nativo de tu navegador. Aún no se ha realizado una evaluación comparativa de esto.
