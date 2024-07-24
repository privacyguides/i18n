---
meta_title: "Recommended Search Engines: Anonymous Google Alternatives - Privacy Guides"
title: "Search Engines"
icon: material/search-web
description: These privacy-respecting search engines don't build an advertising profile based on your searches.
cover: search-engines.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

Use a **search engine** that doesn't build an advertising profile based on your searches.

## Empfohlene DNS-Anbieter

The recommendations here do not collect personally identifying information (PII) based on each service's privacy policy. Es gibt **keine Garantie**, dass diese Datenschutzbestimmungen auch eingehalten werden.

Consider using a [VPN](vpn.md) or [Tor](tor.md) if your threat model requires hiding your IP address from the search provider.

| Anbieter                      | Search Index                                                                                                                                                                  | Tor Hidden Service            | Logging / Privacy Policy | Country of Operation |
| ----------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- | ------------------------ | -------------------- |
| [Brave Search](#brave-search) | [Independent](https://brave.com/search-independence)                                                                                                                          | :material-check:{ .pg-green } | Anonymized[^1]           | United States        |
| [DuckDuckGo](#duckduckgo)     | [Bing](https://help.duckduckgo.com/results/sources)                                                                                                                           | :material-check:{ .pg-green } | Anonymized[^2]           | United States        |
| [Startpage](#startpage)       | [Google and Bing](https://support.startpage.com/hc/articles/4522435533844-What-is-the-relationship-between-Startpage-and-your-search-partners-like-Google-and-Microsoft-Bing) | :material-check:{ .pg-green } | Anonymized[^3]           | Netherlands          |

### Brave Search

<div class="admonition recommendation" markdown>

![Brave Search logo](assets/img/search-engines/brave-search.svg){ align=right }

**Brave Search** is a search engine developed by Brave. Der Index ist für die Google-Suche optimiert und kann daher im Vergleich zu anderen Alternativen möglicherweise kontextgenauere Ergebnisse liefern.

Brave Search includes unique features such as [Discussions](https://search.brave.com/help/discussions), which highlights conversation-focused results such as forum posts.

[:octicons-home-16: Homepage](https://search.brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://search.brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://search.brave.com/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://search.brave.com/help){ .card-link title=Documentation}

</details>

</div>

Note that if you use Brave Search while logged in to a Premium account, it may make it easier for Brave to correlate queries with specific users.

We recommend you disable [Anonymous usage metrics](https://search.brave.com/help/usage-metrics) as it is enabled by default and can be disabled within settings.

### DuckDuckGo

<div class="admonition recommendation" markdown>

![DuckDuckGo logo](assets/img/search-engines/duckduckgo.svg){ align=right }

**DuckDuckGo** ist eine der gängigeren Optionen für private Suchmaschinen. Notable DuckDuckGo search features include [bangs](https://duckduckgo.com/bang) and a variety of [instant answers](https://help.duckduckgo.com/duckduckgo-help-pages/features/instant-answers-and-other-features). The search engine uses numerous [sources](https://help.duckduckgo.com/results/sources) other than Bing for instant answers and other non-primary results.

DuckDuckGo is the default search engine for the [Tor Browser](tor.md#tor-browser) and is one of the few available options on Apple’s [Safari](mobile-browsers.md#safari) browser.

[:octicons-home-16: Homepage](https://duckduckgo.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://duckduckgo.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.duckduckgo.com){ .card-link title=Documentation}

</details>

</div>

DuckDuckGo offers two [other versions](https://help.duckduckgo.com/features/non-javascript) of their search engine, both of which do not require JavaScript. Allerdings fehlen diesen Versionen einige Funktionen. These versions can also be used in conjunction with their Tor hidden address by appending [/lite](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/lite) or [/html](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/html) for the respective version.

### Startpage

<div class="admonition recommendation" markdown>

![Startpage logo](assets/img/search-engines/startpage.svg#only-light){ align=right }
![Startpage logo](assets/img/search-engines/startpage-dark.svg#only-dark){ align=right }

**Startpage** is a private search engine. One of Startpage's unique features is the [Anonymous View](https://startpage.com/en/anonymous-view), which puts forth efforts to standardize user activity to make it more difficult to be uniquely identified. The feature can be useful for hiding [some](https://support.startpage.com/hc/articles/4455540212116-The-Anonymous-View-Proxy-technical-details) network and browser properties. Anders als der Name vermuten lässt, sollte man sich jedoch nicht auf diese Funktion verlassen, um anonym zu bleiben. Wenn du Anonymität suchst, verwende stattdessen den [Tor Browser](tor.md#tor-browser).

[:octicons-home-16: Homepage](https://startpage.com){ .md-button .md-button--primary }
[:simple-torbrowser:](http://startpagel6srwcjlue4zgq3zevrujfaow726kjytqbbjyrswwmjzcqd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://startpage.com/en/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.startpage.com/hc/categories/4481917470356-Startpage-Search-Engine){ .card-link title=Documentation}

</details>

</div>

Der Mehrheitsaktionär von Startpage ist System1, ein Werbeunternehmen. Wir glauben nicht, dass dies ein Problem ist, da sie gesonderte <a href="https://system1.com/terms/privacy-policy"]>Datenschutzbestimmungen</a> haben. The Privacy Guides team reached out to Startpage [back in 2020](https://blog.privacyguides.org/2020/05/03/relisting-startpage) to clear up any concerns with System1's sizeable investment into the service, and we were satisfied with the answers we received.

Startpage previously placed limitations on VPN and [Tor](tor.md) users, but they recently created an [official](https://support.startpage.com/hc/en-us/articles/24786602537364-Startpage-s-Tor-onion-service) Tor hidden service, and as of April 2024 we have no longer noticed extra roadblocks for Tor or [VPN](vpn.md) users.

## Metasearch Engines

A [metasearch engine](https://en.wikipedia.org/wiki/Metasearch_engine) aggregates the results of other search engines, such as the ones recommended above, while not storing any information itself.

### SearXNG

<div class="admonition recommendation" markdown>

![SearXNG logo](assets/img/search-engines/searxng.svg){ align=right }

**SearXNG** is an open-source, self-hostable, metasearch engine. Es ist ein aktiv betreuter Fork von [SearX](https://github.com/searx/searx).

[:octicons-home-16: Homepage](https://searxng.org){ .md-button .md-button--primary }
[:octicons-server-16:](https://searx.space){ .card-link title="Public Instances"}
[:octicons-code-16:](https://github.com/searxng/searxng){ .card-link title="Source Code" }

</details>

</div>

SearXNG ist ein Proxy zwischen dir und den Suchmaschinen, die es zusammenfasst. Deine Suchanfragen werden weiterhin an die Suchmaschinen gesendet, von denen SearXNG seine Ergebnisse bezieht.

Wenn du selbst hostest, ist es wichtig, dass deine Instanz auch von anderen Personen genutzt wird, damit sich die Suchanfragen vermischen können. Du solltest vorsichtig sein, wo und wie du SearXNG hostest, da Leute, die auf deiner Instanz nach illegalen Inhalten suchen, unerwünschte Aufmerksamkeit der Behörden auf sich ziehen könnten.

Wenn du eine SearXNG-Instanz verwendest, beachte unbedingt deren Datenschutzbestimmungen. Da SearXNG-Instanzen von ihren Eigentümern geändert werden können, spiegeln sie nicht unbedingt deren Datenschutzpolitik wider. Einige Instanzen laufen als versteckter Tor-Dienst, der ein gewisses Maß an Privatsphäre gewährleistet, solange deine Suchanfragen keine personenbezogenen Daten enthalten.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, in Verbindung stehen.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen dir, dich mit der Liste vertraut zu machen, bevor du dich für ein Projekt entscheidest, und deine eigenen Recherchen anzustellen, um sicherzustellen, dass es die richtige Wahl für dich ist.

### Mindestanforderungen

- Must not collect PII per their privacy policy.
- Must not require users to create an account with them.

### Im besten Fall

Unsere Best-Case-Kriterien stellen dar, was wir uns von einem perfekten Projekt in dieser Kategorie wünschen würden. Unsere Empfehlungen enthalten möglicherweise keine oder nicht alle dieser Merkmale, aber diejenigen, die sie enthalten, werden möglicherweise höher eingestuft als andere auf dieser Seite.

- Sollte auf Open-Source-Software basieren.
- Sollte keine IP-Adressen von Tor-Ausgangsknoten blockieren.

[^1]: Brave Search collects aggregated usage metrics, which includes the OS and the user agent. However, they do not collect PII. To serve [anonymous local results](https://search.brave.com/help/anonymous-local-results), IP addresses are temporarily processed, but are not retained. [https://search.brave.com/help/privacy-policy](https://search.brave.com/help/privacy-policy)
[^2]: DuckDuckGo **does** log your searches for product improvement purposes, but not your IP address or any other PII. [https://duckduckgo.com/privacy](https://duckduckgo.com/privacy)
[^3]: Startpage logs details such as operating system, user agent, and language. They do not log your IP address, search queries, or other PII. [https://startpage.com/en/privacy-policy](https://startpage.com/en/privacy-policy)
