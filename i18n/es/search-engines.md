---
meta_title: "Recommended Search Engines: Anonymous Alternatives to Google - Privacy Guides"
title: Motores de Búsqueda
icon: material/search-web
description: Use privacy-respecting search engines which don't build an advertising profile based on your searches.
cover: search-engines.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Utilice un **motor de búsqueda** que no construya un perfil publicitario basado en sus búsquedas.

## Proveedores Recomendados

Estas recomendaciones no recogen información de identificación personal (IIP), de acuerdo con la política de privacidad de cada servicio. No hay **garantías** de que estas políticas de privacidad se respeten.

Considere usar una [VPN](vpn.md) o [Tor](tor.md) si su modelo de amenaza requiere ocultar su dirección IP al proveedor de búsquedas.

| Proveedor                     | Índice de Búsqueda                                                                                                                                                          | Servicio Oculto Tor           | Logs / Política de Privacidad | País de Operación |
| ----------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- | ----------------------------- | ----------------- |
| [Brave Search](#brave-search) | [Independiente](https://brave.com/search-independence)                                                                                                                      | :material-check:{ .pg-green } | Anónimo[^1]                   | Estados Unidos    |
| [DuckDuckGo](#duckduckgo)     | [Bing](https://help.duckduckgo.com/results/sources)                                                                                                                         | :material-check:{ .pg-green } | Anónimo[^2]                   | Estados Unidos    |
| [Mullvad Leta](#mullvad-leta) | [Brave and Google](https://leta.mullvad.net/faq#what-can-leta-do)                                                                                                           | :material-check:{ .pg-green } | Anonymized[^3]                | Sweden            |
| [Startpage](#startpage)       | [Google y Bing](https://support.startpage.com/hc/articles/4522435533844-What-is-the-relationship-between-Startpage-and-your-search-partners-like-Google-and-Microsoft-Bing) | :material-check:{ .pg-green } | Anónimo[^4]                   | Países Bajos      |

### Brave Search

<div class="admonition recommendation" markdown>

![Brave Search logo](assets/img/search-engines/brave-search.svg){ align=right }

**Brave Search** es un motor de búsqueda desarrollado por Brave. It includes unique features such as [Discussions](https://search.brave.com/help/discussions), which highlights conversation-focused results such as forum posts.

Brave Search is the default search engine for the [Brave Browser](desktop-browsers.md#brave).

[:octicons-home-16: Homepage](https://search.brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://search.brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://search.brave.com/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://search.brave.com/help){ .card-link title="Documentation" }

</div>

If you use Brave Search while logged in to a Premium account, there is a risk of Brave correlating search queries with your account.

Le recomendamos que desactive las [Estadísticas de uso anónimas](https://search.brave.com/help/usage-metrics), ya que están activadas por defecto y pueden desactivarse en la configuración.

### DuckDuckGo

<div class="admonition recommendation" markdown>

![DuckDuckGo logo](assets/img/search-engines/duckduckgo.svg){ align=right }

**DuckDuckGo** es uno de los buscadores privados más populares. Entre las funciones de búsqueda de DuckDuckGo destacan [bangs](https://duckduckgo.com/bang) y una variedad de [respuestas instantáneas](https://help.duckduckgo.com/duckduckgo-help-pages/features/instant-answers-and-other-features). El motor de búsqueda utiliza numerosas [fuentes](https://help.duckduckgo.com/results/sources) distintas de Bing para las respuestas instantáneas y otros resultados no primarios.

DuckDuckGo es el motor de búsqueda predeterminado de [Tor Browser](tor.md#tor-browser) y es una de las pocas opciones disponibles en el navegador [Safari](mobile-browsers.md#safari-ios) de Apple.

[:octicons-home-16: Homepage](https://duckduckgo.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://duckduckgo.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.duckduckgo.com){ .card-link title="Documentation" }

</div>

DuckDuckGo ofrece [otras dos versiones](https://help.duckduckgo.com/features/non-javascript) de su motor de búsqueda y ninguna de ellas requiere JavaScript. Sin embargo, estas versiones carecen de funciones. Estas versiones también pueden usarse junto con su dirección oculta Tor añadiendo [/lite](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/lite) o [/html](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/html) para la versión respectiva.

### Mullvad Leta

<div class="admonition recommendation" markdown>

![Mullvad logo](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad Leta** is a search engine developed by Mullvad. It uses a [shared cache](https://leta.mullvad.net/faq#what-is-cached-search) to fetch search results and limit calls to the search APIs it uses.

Mullvad Leta currently only provides text search results. It is the default search engine for the [Mullvad Browser](desktop-browsers.md#mullvad-browser).

[:octicons-home-16: Homepage](https://leta.mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://uxngojcovdcyrmwkmkltyy2q7enzzvgv7vlqac64f2vl6hcrrqtlskqd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://leta.mullvad.net/terms-of-service){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://leta.mullvad.net/faq){ .card-link title="Documentation" }

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Consejo</p>

Mullvad Leta is useful if you want to disable JavaScript in your browser, such as [Mullvad Browser](desktop-browsers.md#mullvad-browser) on the Safest security level.

</div>

Mullvad Leta was [audited](https://mullvad.net/en/blog/security-audit-of-our-letamullvadnet-search-service) by Assured AB in March 2023. All issues were addressed and fixed shortly after the [report](https://assured.se/publications/Assured_Mullvad_Leta_pentest_report_2023.pdf).

### Startpage

<div class="admonition recommendation" markdown>

![Startpage logo](assets/img/search-engines/startpage.svg#only-light){ align=right }
![Startpage logo](assets/img/search-engines/startpage-dark.svg#only-dark){ align=right }

**Startpage** es un motor de búsqueda privado. Una de las características exclusivas de Startpage es la [Vista Anónima](https://startpage.com/en/anonymous-view), que se esfuerza por normalizar la actividad de los usuarios para dificultar su identificación exclusiva. Esta función puede ser útil para ocultar [algunas](https://support.startpage.com/hc/articles/4455540212116-The-Anonymous-View-Proxy-technical-details) propiedades de la red y el navegador. A diferencia de lo que sugiere su nombre, no se debe confiar en esta función para mantener el anonimato. Si busca anonimato, utilice [Tor Browser](tor.md#tor-browser) en su lugar.

[:octicons-home-16: Homepage](https://startpage.com){ .md-button .md-button--primary }
[:simple-torbrowser:](http://startpagel6srwcjlue4zgq3zevrujfaow726kjytqbbjyrswwmjzcqd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://startpage.com/en/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.startpage.com/hc/categories/4481917470356-Startpage-Search-Engine){ .card-link title="Documentation" }

</div>

El accionista mayoritario de Startpage es System1, una empresa de tecnología publicitaria. No creemos que eso sea un problema, ya que tienen una [política de privacidad](https://system1.com/terms/privacy-policy) claramente separada. El equipo de Privacy Guides se puso en contacto con Startpage [en 2020](https://blog.privacyguides.org/2020/05/03/relisting-startpage) para aclarar cualquier duda sobre la considerable inversión de System1 en el servicio, y quedamos satisfechos con las respuestas que recibimos.

Startpage anteriormente ponía limitaciones a los usuarios de VPN y [Tor](tor.md), pero recientemente crearon un servicio oculto Tor [oficial](https://support.startpage.com/hc/en-us/articles/24786602537364-Startpage-s-Tor-onion-service), y desde abril de 2024 ya no hemos notado bloqueos adicionales para los usuarios de Tor o [VPN](vpn.md).

## Metabuscadores

Un [metabuscador](https://en.wikipedia.org/wiki/Metasearch_engine) agrega los resultados de otros motores de búsqueda, como los recomendados anteriormente, sin almacenar ninguna información por sí mismo.

### SearXNG

<div class="admonition recommendation" markdown>

![SearXNG logo](assets/img/search-engines/searxng.svg){ align=right }

**SearXNG** es un metabuscador autoalojable de código abierto. Es una bifurcación de [SearX](https://github.com/searx/searx) mantenida activamente.

[:octicons-home-16: Homepage](https://searxng.org){ .md-button .md-button--primary }
[:octicons-server-16:](https://searx.space){ .card-link title="Public Instances" }
[:octicons-code-16:](https://github.com/searxng/searxng){ .card-link title="Source Code" }

</div>

SearXNG es un proxy entre usted y los motores de búsqueda desde los que se agrega. Sus consultas seguirán siendo enviadas a los motores de búsqueda de los que SearXNG obtiene sus resultados.

Al autoalojarse, es importante que otras personas utilicen su instancia para que las consultas se integren. Debe tener cuidado con dónde y cómo aloja SearXNG, ya que las personas que busquen contenidos ilegales en su instancia podrían atraer la atención no deseada de las autoridades.

Cuando utilice una instancia de SearXNG, asegúrese de leer su política de privacidad. Dado que las instancias de SearXNG pueden ser modificadas por sus propietarios, no reflejan necesariamente su política de privacidad. Algunas instancias se ejecutan como un servicio oculto de Tor, lo que puede garantizar cierta privacidad siempre y cuando sus consultas de búsqueda no contengan PII.

## Criterios

**Por favor, tenga en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que usted se familiarice con esta lista, antes de decidir utilizar un proyecto y realizar su propia investigación para asegurarse de que es la elección ideal para usted.

### Requisitos Mínimos

- No debe recopilar IIP según su política de privacidad.
- No debe exigir a los usuarios que creen una cuenta con ellos.

### Mejor Caso

Nuestro criterio del mejor caso representa lo que nos gustaría ver del proyecto perfecto en esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Debe estar basado en software de código abierto.
- No debería bloquear las direcciones IP del nodo de salida de Tor.

[^1]: Brave Search recopila métricas de uso agregadas, que incluyen el sistema operativo y el agente de usuario. Sin embargo, no recopilan PII. Para servir [resultados locales anónimos](https://search.brave.com/help/anonymous-local-results), las direcciones IP se procesan temporalmente, pero no se conservan.

    Brave Search: [*Brave Search privacy notice*](https://search.brave.com/help/privacy-policy) [^2]: DuckDuckGo **does** log your searches for product improvement purposes, but not your IP address or any other PII.

    DuckDuckGo Privacy Policy: [*We don't track you.*](https://duckduckgo.com/privacy) [^3]: Mullvad Leta logs your searches and stores them hashed with a secret in a RAM-based cache. The cache is removed after it reaches 30 days in age, or when the server-side Leta application is restarted. They do not collect any PII.

    Terms of Service: [*Service Usage*](https://leta.mullvad.net/terms-of-service) [^4]: Startpage logs details such as operating system, user agent, and language. No registra su dirección IP, consultas de búsqueda u otra información personal.

    Our Privacy Policy: [*How we have implemented truly anonymous analytics*](https://startpage.com/en/privacy-policy#section-4)
