---
meta_title: "Motori di ricerca consigliati: alternative anonime a Google - Privacy Guides"
title: "Motori di ricerca"
icon: material/search-web
description: Questi motori di ricerca che rispettano la privacy, non costruiscono un profilo pubblicitario secondo le tue ricerche.
cover: search-engines.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

Utilizza un motore di ricerca che non crei un profilo pubblicitario basato sulle tue ricerche.

## Fornitori consigliati

The recommendations here do not collect personally identifying information (PII) based on each service's privacy policy. Non esiste **alcuna garanzia** che tali politiche sulle privacy siano rispettate.

Considera l'utilizzo di una [VPN](vpn.md) o di [Tor](tor.md), se il tuo modello di minaccia richiede l'occultamento del tuo indirizzo IP dal fornitore di ricerca.

| Provider                      | Search Index                                                                                                                                                                  | Tor Hidden Service            | Logging / Privacy Policy | Country of Operation |
| ----------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- | ------------------------ | -------------------- |
| [Brave Search](#brave-search) | [Independent](https://brave.com/search-independence/)                                                                                                                         | :material-check:{ .pg-green } | Anonymized[^1]           | United States        |
| [DuckDuckGo](#duckduckgo)     | [Bing](https://help.duckduckgo.com/results/sources)                                                                                                                           | :material-check:{ .pg-green } | Anonymized[^2]           | United States        |
| [Startpage](#startpage)       | [Google and Bing](https://support.startpage.com/hc/articles/4522435533844-What-is-the-relationship-between-Startpage-and-your-search-partners-like-Google-and-Microsoft-Bing) | :material-check:{ .pg-green } | Anonymized[^3]           | Netherlands          |

### Brave Search

<div class="admonition recommendation" markdown>

![Brave Search logo](assets/img/search-engines/brave-search.svg){ align=right }

**Brave Search** is a search engine developed by Brave. L'indice è ottimizzato rispetto a Google Search e, dunque, potrebbe fornire risultati contestualmente più accurati, rispetto ad altre alternative.

Brave Search includes unique features such as [Discussions](https://search.brave.com/help/discussions), which highlights conversation-focused results—such as forum posts.

[:octicons-home-16: Homepage](https://search.brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://search.brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://search.brave.com/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://search.brave.com/help){ .card-link title=Documentation}

</details>

</div>

We recommend you disable [Anonymous usage metrics](https://search.brave.com/help/usage-metrics) as it is enabled by default and can be disabled within settings.

### DuckDuckGo

<div class="admonition recommendation" markdown>

![Logo di DuckDuckGo](assets/img/search-engines/duckduckgo.svg){ align=right }

**DuckDuckGo** è uno dei motori di ricerca privati più popolari. Notable DuckDuckGo search features include [bangs](https://duckduckgo.com/bang) and a variety of [instant answers](https://help.duckduckgo.com/duckduckgo-help-pages/features/instant-answers-and-other-features). The search engine uses numerous [sources](https://help.duckduckgo.com/results/sources) other than Bing for instant answers and other non-primary results.

DuckDuckGo is the default search engine for the [Tor Browser](tor.md#tor-browser) and is one of the few available options on Apple’s [Safari](mobile-browsers.md#safari) browser.

[:octicons-home-16: Homepage](https://duckduckgo.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://duckduckgo.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.duckduckgo.com){ .card-link title=Documentation}

</details>

</div>

DuckDuckGo offers two [other versions](https://help.duckduckgo.com/features/non-javascript) of their search engine, both of which do not require JavaScript. Tuttavia, queste versioni mancano di funzionalità. These versions can also be used in conjunction with their Tor hidden address by appending [/lite](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/lite) or [/html](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/html) for the respective version.

### Startpage

<div class="admonition recommendation" markdown>

![Startpage logo](assets/img/search-engines/startpage.svg#only-light){ align=right }
![Startpage logo](assets/img/search-engines/startpage-dark.svg#only-dark){ align=right }

**Startpage** is a private search engine. One of Startpage's unique features is the [Anonymous View](https://startpage.com/en/anonymous-view), which puts forth efforts to standardize user activity to make it more difficult to be uniquely identified. The feature can be useful for hiding [some](https://support.startpage.com/hc/articles/4455540212116-The-Anonymous-View-Proxy-technical-details) network and browser properties. A differenza di quanto suggerito dal nome, non ci si dovrebbe affidare a tale funzionalità per l'anonimato. Se cerchi l'anonimato, piuttosto, utilizza il [Tor Browser](tor.md#tor-browser).

[:octicons-home-16: Homepage](https://startpage.com){ .md-button .md-button--primary }
[:simple-torbrowser:](http://startpagel6srwcjlue4zgq3zevrujfaow726kjytqbbjyrswwmjzcqd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://startpage.com/en/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.startpage.com/hc/categories/4481917470356-Startpage-Search-Engine){ .card-link title=Documentation}

</details>

</div>

L'azionista di maggioranza di Startpage è System1, un'azienda di tecnologie inserzionistiche. Non crediamo che ciò sia un problema, dato che seguono una [politica sull privacy](https://system1.com/terms/privacy-policy) distintamente separata. The Privacy Guides team reached out to Startpage [back in 2020](https://blog.privacyguides.org/2020/05/03/relisting-startpage/) to clear up any concerns with System1's sizeable investment into the service, and we were satisfied with the answers we received.

Startpage previously placed limitations on VPN and [Tor](tor.md) users, but they recently created an [official](https://support.startpage.com/hc/en-us/articles/24786602537364-Startpage-s-Tor-onion-service) Tor hidden service, and as of April 2024 we have no longer noticed extra roadblocks for Tor or [VPN](vpn.md) users.

## Metasearch Engines

A [metasearch engine](https://en.wikipedia.org/wiki/Metasearch_engine) aggregates the results of other search engines, such as the ones recommended above, while not storing any information itself.

### SearXNG

<div class="admonition recommendation" markdown>

![SearXNG logo](assets/img/search-engines/searxng.svg){ align=right }

**SearXNG** is an open-source, self-hostable, metasearch engine. È un fork attivamente mantenuto di [SearX](https://github.com/searx/searx).

[:octicons-home-16: Homepage](https://searxng.org){ .md-button .md-button--primary }
[:octicons-server-16:](https://searx.space){ .card-link title="Public Instances"}
[:octicons-code-16:](https://github.com/searxng/searxng){ .card-link title="Source Code" }

</details>

</div>

SearXNG è un proxy tra te e i motori di ricerca da cui aggrega. Le tue richieste di ricerca saranno comunque inviate ai motori di ricerca da cui SearXNG ottiene i propri risultati.

Quando ospitato autonomamente, è importante che ci siano altre persone che utilizzino la tua istanza, così che le richieste si confondano tra loro. Dovresti prestare attenzione a dove e come stai ospitando SearXNG, in quanto gli utenti alla ricerca di contenuti illegali sulla tua istanza, potrebbero attirare attenzioni indesiderate da parte delle autorità.

Utilizzando un'istanza di SearXNG, assicurati di leggere la loro politica sulla privacy. Poiché le istanze di SearXNG potrebbero essere modificate dai rispettivi proprietari, non riflettono necessariamente la loro politica sulla privacy. Alcune istanze sono eseguite come un servizio nascosto di Tor, che potrebbe garantire una maggiore privacy, a patto che le tue richieste di ricerca non contengano PII.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questi elenchi, prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta migliore per te.

### Requisiti minimi

- Must not collect PII per their privacy policy.
- Non deve consentire agli utenti di creare un profilo.

### Miglior Caso

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- Dovrebbe basarsi su software open source.
- Non dovrebbe bloccare gli indirizzi IP del nodo d'uscita di Tor.

[^1]: Brave Search collects aggregated usage metrics, which includes the OS and the user agent. However, they do not collect PII. To serve [anonymous local results](https://search.brave.com/help/anonymous-local-results), IP addresses are temporarily processed, but are not retained. [https://search.brave.com/help/privacy-policy](https://search.brave.com/help/privacy-policy)
[^2]: DuckDuckGo **does** log your searches for product improvement purposes, but not your IP address or any other PII. [https://duckduckgo.com/privacy](https://duckduckgo.com/privacy)
[^3]: Startpage logs details such as operating system, user agent, and language. They do not log your IP address, search queries, or other PII. [https://startpage.com/en/privacy-policy](https://startpage.com/en/privacy-policy)
