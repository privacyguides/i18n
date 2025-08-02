---
meta_title: "Recommended Search Engines: Anonymous Alternatives to Google - Privacy Guides"
title: Motori di ricerca
icon: material/search-web
description: Use privacy-respecting search engines which don't build an advertising profile based on your searches.
cover: search-engines.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protezione dalle seguenti minacce:</small>

- [:material-account-cash: Capitalismo di sorveglianza](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Utilizza un **motore di ricerca** che non crei un profilo pubblicitario basato sulle tue ricerche.

## Fornitori consigliati

Queste raccomandazioni non raccolgono informazioni d'identificazione personale (PII) sulla base dell'informativa sulla privacy di ciascun servizio. Non esiste **alcuna garanzia** che tali politiche sulle privacy siano rispettate.

Considera l'utilizzo di una [VPN](vpn.md) o di [Tor](tor.md), se il tuo modello di minaccia richiede l'occultamento del tuo indirizzo IP dal fornitore di ricerca.

| Provider                      | Indice di Ricerca                                                                                                                                                           | Servizio Nascosto Tor         | Logging / Informativa sulla privacy | Paese di Esercizio    |
| ----------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- | ----------------------------------- | --------------------- |
| [Brave Search](#brave-search) | [Indipendente](https://brave.com/search-independence)                                                                                                                       | :material-check:{ .pg-green } | Anonimizzato[^1]                    | Stati Uniti d'America |
| [DuckDuckGo](#duckduckgo)     | [Bing](https://help.duckduckgo.com/results/sources)                                                                                                                         | :material-check:{ .pg-green } | Anonymized[^2]                      | Stati Uniti d'America |
| [Mullvad Leta](#mullvad-leta) | [Brave and Google](https://leta.mullvad.net/faq#what-can-leta-do)                                                                                                           | :material-check:{ .pg-green } | Anonymized[^3]                      | Sweden                |
| [Startpage](#startpage)       | [Google e Bing](https://support.startpage.com/hc/articles/4522435533844-What-is-the-relationship-between-Startpage-and-your-search-partners-like-Google-and-Microsoft-Bing) | :material-check:{ .pg-green } | Anonymized[^4]                      | Paesi Bassi           |

### Brave Search

<div class="admonition recommendation" markdown>

![Logo di Brave Search](assets/img/search-engines/brave-search.svg){ align=right }

**Brave Search** è un motore di ricerca sviluppato da Brave. It includes unique features such as [Discussions](https://search.brave.com/help/discussions), which highlights conversation-focused results such as forum posts.

Brave Search is the default search engine for the [Brave Browser](desktop-browsers.md#brave).

[:octicons-home-16: Homepage](https://search.brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://search.brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://search.brave.com/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://search.brave.com/help){ .card-link title="Documentation" }

</div>

If you use Brave Search while logged in to a Premium account, there is a risk of Brave correlating search queries with your account.

Ti consigliamo di disabilitare le [Statistiche di utilizzo anonime](https://search.brave.com/help/usage-metrics), in quanto sono abilitate per impostazione predefinita e possono essere disabilitate nelle impostazioni.

### DuckDuckGo

<div class="admonition recommendation" markdown>

![Logo di DuckDuckGo](assets/img/search-engines/duckduckgo.svg){ align=right }

**DuckDuckGo** è uno dei motori di ricerca privati più popolari. Notable DuckDuckGo search features include [bangs](https://duckduckgo.com/bang) and a variety of [instant answers](https://help.duckduckgo.com/duckduckgo-help-pages/features/instant-answers-and-other-features). The search engine uses numerous [sources](https://help.duckduckgo.com/results/sources) other than Bing for instant answers and other non-primary results.

DuckDuckGo is the default search engine for the [Tor Browser](tor.md#tor-browser) and is one of the few available options on Apple’s [Safari](mobile-browsers.md#safari-ios) browser.

[:octicons-home-16: Homepage](https://duckduckgo.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://duckduckgo.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.duckduckgo.com){ .card-link title="Documentation" }

</div>

DuckDuckGo offers two [other versions](https://help.duckduckgo.com/features/non-javascript) of their search engine, both of which do not require JavaScript. Tuttavia, queste versioni mancano di funzionalità. These versions can also be used in conjunction with their Tor hidden address by appending [/lite](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/lite) or [/html](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/html) for the respective version.

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
<p class="admonition-title">Suggerimento</p>

Mullvad Leta is useful if you want to disable JavaScript in your browser, such as [Mullvad Browser](desktop-browsers.md#mullvad-browser) on the Safest security level.

</div>

Mullvad Leta was [audited](https://mullvad.net/en/blog/security-audit-of-our-letamullvadnet-search-service) by Assured AB in March 2023. All issues were addressed and fixed shortly after the [report](https://assured.se/publications/Assured_Mullvad_Leta_pentest_report_2023.pdf).

### Startpage

<div class="admonition recommendation" markdown>

![Startpage logo](assets/img/search-engines/startpage.svg#only-light){ align=right }
![Startpage logo](assets/img/search-engines/startpage-dark.svg#only-dark){ align=right }

**Startpage** is a private search engine. One of Startpage's unique features is the [Anonymous View](https://startpage.com/en/anonymous-view), which puts forth efforts to standardize user activity to make it more difficult to be uniquely identified. The feature can be useful for hiding [some](https://support.startpage.com/hc/articles/4455540212116-The-Anonymous-View-Proxy-technical-details) network and browser properties. A differenza di quanto suggerito dal nome, non ci si dovrebbe affidare a tale funzionalità per l'anonimato. Se cerchi l'anonimato, piuttosto, utilizza il [Tor Browser](tor.md#tor-browser).

[:octicons-home-16: Homepage](https://startpage.com){ .md-button .md-button--primary }
[:simple-torbrowser:](http://startpagel6srwcjlue4zgq3zevrujfaow726kjytqbbjyrswwmjzcqd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://startpage.com/en/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.startpage.com/hc/categories/4481917470356-Startpage-Search-Engine){ .card-link title="Documentation" }

</div>

L'azionista di maggioranza di Startpage è System1, un'azienda di tecnologie inserzionistiche. Non crediamo che ciò sia un problema, dato che seguono una [politica sull privacy](https://system1.com/terms/privacy-policy) distintamente separata. The Privacy Guides team reached out to Startpage [back in 2020](https://blog.privacyguides.org/2020/05/03/relisting-startpage) to clear up any concerns with System1's sizeable investment into the service, and we were satisfied with the answers we received.

Startpage previously placed limitations on VPN and [Tor](tor.md) users, but they recently created an [official](https://support.startpage.com/hc/en-us/articles/24786602537364-Startpage-s-Tor-onion-service) Tor hidden service, and as of April 2024 we have no longer noticed extra roadblocks for Tor or [VPN](vpn.md) users.

## Metasearch Engines

A [metasearch engine](https://en.wikipedia.org/wiki/Metasearch_engine) aggregates the results of other search engines, such as the ones recommended above, while not storing any information itself.

### SearXNG

<div class="admonition recommendation" markdown>

![SearXNG logo](assets/img/search-engines/searxng.svg){ align=right }

**SearXNG** is an open-source, self-hostable, metasearch engine. È un fork attivamente mantenuto di [SearX](https://github.com/searx/searx).

[:octicons-home-16: Homepage](https://searxng.org){ .md-button .md-button--primary }
[:octicons-server-16:](https://searx.space){ .card-link title="Public Instances" }
[:octicons-code-16:](https://github.com/searxng/searxng){ .card-link title="Source Code" }

</div>

SearXNG è un proxy tra te e i motori di ricerca da cui aggrega. Le tue richieste di ricerca saranno comunque inviate ai motori di ricerca da cui SearXNG ottiene i propri risultati.

Quando ospitato autonomamente, è importante che ci siano altre persone che utilizzino la tua istanza, così che le richieste si confondano tra loro. Dovresti prestare attenzione a dove e come stai ospitando SearXNG, in quanto gli utenti alla ricerca di contenuti illegali sulla tua istanza, potrebbero attirare attenzioni indesiderate da parte delle autorità.

Utilizzando un'istanza di SearXNG, assicurati di leggere la loro politica sulla privacy. Poiché le istanze di SearXNG potrebbero essere modificate dai rispettivi proprietari, non riflettono necessariamente la loro politica sulla privacy. Alcune istanze sono eseguite come un servizio nascosto di Tor, che potrebbe garantire una maggiore privacy, a patto che le tue richieste di ricerca non contengano PII.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questi elenchi, prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta migliore per te.

### Requisiti minimi

- Must not collect PII per their privacy policy.
- Must not require users to create an account with them.

### Miglior Caso

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- Dovrebbe basarsi su software open source.
- Non dovrebbe bloccare gli indirizzi IP del nodo d'uscita di Tor.

[^1]: Brave Search collects aggregated usage metrics, which includes the OS and the user agent. However, they do not collect PII. To serve [anonymous local results](https://search.brave.com/help/anonymous-local-results), IP addresses are temporarily processed, but are not retained.

    Brave Search: [*Brave Search privacy notice*](https://search.brave.com/help/privacy-policy) [^2]: DuckDuckGo **does** log your searches for product improvement purposes, but not your IP address or any other PII.

    DuckDuckGo Privacy Policy: [*We don't track you.*](https://duckduckgo.com/privacy) [^3]: Mullvad Leta logs your searches and stores them hashed with a secret in a RAM-based cache. The cache is removed after it reaches 30 days in age, or when the server-side Leta application is restarted. They do not collect any PII.

    Terms of Service: [*Service Usage*](https://leta.mullvad.net/terms-of-service) [^4]: Startpage logs details such as operating system, user agent, and language. They do not log your IP address, search queries, or other PII.

    Our Privacy Policy: [*How we have implemented truly anonymous analytics*](https://startpage.com/en/privacy-policy#section-4)
