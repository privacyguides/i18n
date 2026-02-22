---
title: Extensiones de Navegador
icon: material/puzzle-outline
description: Estas extensiones de navegador pueden mejorar tu experiencia de navegación y proteger tu privacidad.
cover: browser-extensions.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

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
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

</details>

</div>

Sugerimos seguir la [documentación del desarrollador](https://github.com/gorhill/uBlock/wiki/Blocking-mode) y elegir uno de los "modos". Las listas de filtros adicionales pueden afectar al rendimiento y [pueden aumentar la superficie de ataque](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

Estas son algunas otras [listas de filtros](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) que puedes considerar añadir:

- [x] Marca **Privacidad** > **Protección de Rastreo de URL de AdGuard**
- Añade [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

### uBlock Origin Lite

uBlock Origin también tiene una versión «Lite» de su extensión, que ofrece un conjunto de características limitado en comparación con la extensión original. Sin embargo, tiene algunas ventajas distintas sobre su hermana de pleno derecho, así que puede que quieras considerarlo si...

- ...no quieres conceder permisos completos para "leer/modificar datos del sitio web" a ninguna extensión (incluso una de confianza como uBlock Origin)
- ...quieres un bloqueador de contenidos[^1] más eficiente en cuanto a recursos (memoria/CPU)
- ...tu navegador solo admite extensiones Manifest V3. Este es el caso de Chrome [^2] , Edge y la mayoría de los navegadores Chromium.

<div class="admonition recommendation" markdown>

![uBlock Origin Lite logo](assets/img/browsers/ublock_origin_lite.svg){ align=right }

**uBlock Origin Lite** es un bloqueador de contenidos compatible con Manifest V3. En comparación con el _uBlock Origin_ original, esta extensión no requiere amplios permisos de "lectura/modificación de datos" para funcionar, lo que reduce el riesgo de [:material-bug-outline: Ataques Pasivos](basics/common-threats.md#security-and-privacy){ .pg-orange } en tu navegador si se añade una regla maliciosa a una lista de filtros.

[:octicons-repo-16: Repositorio](https://github.com/uBlockOrigin/uBOL-home#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uBlockOrigin/uBOL-home/wiki/Privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://github.com/uBlockOrigin/uBOL-home/wiki){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/gorhill/uBlock/tree/master/platform/mv3){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin-lite/ddkjiahejlhfcafbddmgiahcphecmpfh)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/cimighlppcgcoapaliogpjjdehbnofhn)
- [:simple-safari: Safari](https://apps.apple.com/app/id6745342698)

</details>

</div>

Solo recomendamos esta versión de uBlock Origin si no quieres añadir ninguna lista de filtros que no esté incluida por defecto ni necesitas opciones avanzadas como el [filtrado dinámico](https://github.com/gorhill/ublock/wiki/dynamic-filtering:-quick-guide) o el registrador de red. Estas restricciones se deben a limitaciones en el diseño de Manifest V3, en particular el estricto límite en el número de reglas de filtrado y el hecho de que las extensiones generalmente no pueden obtener recursos remotos.[^3]

Esta versión ofrece tres niveles de bloqueo: "Básico" funciona sin requerir ningún privilegio especial para ver y modificar el contenido del sitio, mientras que los niveles "Óptimo" y "Completo" sí requieren ese amplio permiso, pero ofrecen una mejor experiencia de filtrado con reglas cosméticas adicionales e inyecciones de scriptlet.

Si estableces el modo de filtrado predeterminado en "Óptimo" o "Completo", la extensión solicitará acceso de lectura/modificación a **todos** los sitios web que visites. Sin embargo, también tienes la opción de cambiar la configuración a "Óptima" o "Completa" **por sitio** ajustando el control deslizante en el panel emergente de la extensión en un sitio determinado. Al hacerlo, la extensión solicitará acceso de lectura/modificación únicamente a ese sitio. Por lo tanto, si deseas aprovechar la configuración "sin permisos" de uBlock Origin Lite, probablemente deberías dejar la configuración predeterminada como "Básica" y solo ajustarla a un nivel superior en los sitios en los que ese nivel no sea adecuado.

uBlock Origin Lite solo recibe actualizaciones de la lista de bloqueos cada vez que se actualiza la extensión desde el mercado de extensiones de tu navegador, en lugar de bajo demanda. Google cuenta con un [proceso de revisión acelerado](https://developer.chrome.com/docs/webstore/skip-review) para las actualizaciones de filtros, lo que significa que, por lo general, recibirás las actualizaciones de la lista de filtros con la misma frecuencia con la que uBlock Origin Lite decida publicar una versión (históricamente, cada 2-7 días). Sin embargo, solo pueden actualizarse las llamadas «[reglas seguras](https://developer.chrome.com/docs/extensions/reference/api/declarativeNetRequest#safe_rules)» lo que puede limitar la frecuencia de actualización de las listas que utilizan técnicas avanzadas.

### AdGuard

We recommend [Safari](mobile-browsers.md#safari-ios) for iOS users, which unfortunately is only supported by uBlock Origin **Lite**. Por suerte, AdGuard ofrece una alternativa adecuada:

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

[^2]: A [workaround](https://github.com/uBlockOrigin/uBlock-issues/discussions/3690#discussioncomment-14548779) stil exists as of early December 2025.

[^3]: This is starting to change, as MV3 extensions can now request to use scripts. This has enabled [AdGuard](https://adguard.com/en/blog/adguard-browser-extension-v5-2.html) to propose to import custom filters list by the url, as opposed to having to manually paste the rules, as is the case with uBOL.
