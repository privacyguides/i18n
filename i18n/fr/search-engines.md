---
meta_title: "Moteurs de recherche recommandés : alternatives anonymes à Google - Privacy Guides"
title: Moteurs de recherche
icon: material/search-web
description: Utilisez un moteur de recherche respectueux de la vie privée qui n'établi pas de profil publicitaire basé sur vos recherches.
cover: search-engines.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protège contre les menaces suivantes :</small>

- [:material-account-cash: Capitalisme de surveillance](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Utilisez un **moteur de recherche** qui n'établi pas de profil publicitaire basé sur vos recherches.

## Fournisseurs recommandés

Les recommandations ci-dessous ne collectent pas d'Informations Personnellement Identifiables (IPI) selon leurs politiques de confidetialité. Il n'y a **aucune garantie** que ces politiques de confidentialité soient respectées.

Vous pouvez utiliser un [VPN](vpn.md) ou [Tor](tor.md) si votre modèle de menace nécessite que vous cachiez votre adresse IP au moteur de recherche.

| Fournisseur                   | Index de recherche                                                                                                                                                           | Service caché Tor             | Journalisation / Politique de confidentialité | Pays d'activité |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- | --------------------------------------------- | --------------- |
| [Brave Search](#brave-search) | [Indépendant](https://brave.com/search-independence)                                                                                                                         | :material-check:{ .pg-green } | Anonymisé[^1]                                 | États-Unis      |
| [DuckDuckGo](#duckduckgo)     | [Bing](https://help.duckduckgo.com/results/sources)                                                                                                                          | :material-check:{ .pg-green } | Anonymisé[^2]                                 | États-Unis      |
| [Mullvad Leta](#mullvad-leta) | [Brave et Google](https://leta.mullvad.net/faq#what-can-leta-do)                                                                                                             | :material-check:{ .pg-green } | Anonymisé[^3]                                 | Suède           |
| [Startpage](#startpage)       | [Google et Bing](https://support.startpage.com/hc/articles/4522435533844-What-is-the-relationship-between-Startpage-and-your-search-partners-like-Google-and-Microsoft-Bing) | :material-check:{ .pg-green } | Anonymisé[^4]                                 | Pays-Bas        |

### Brave Search

<div class="admonition recommendation" markdown>

![Logo de Brave Search](assets/img/search-engines/brave-search.svg){ align=right }

**Brave Search** est un moteur de recherche développé par Brave. Il propose des fonctionnalités uniques comme [Discussions](https://search.brave.com/help/discussions), qui permet de mettre en évidence des résultats axés sur les conversations comme des posts de forum.

Brave Search est le moteur de recherche par défaut du [navigateur Brave](desktop-browsers.md#brave).

[:octicons-home-16: Page d'Accueil](https://search.brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://search.brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Service Onion" }
[:octicons-eye-16:](https://search.brave.com/help/privacy-policy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://search.brave.com/help){ .card-link title="Documentation" }

</div>

Si vous utilisez Brave Search en étant connecté à un compte Premium, il y a un risque que Brave associe vos recherches à votre compte.

Nous vous recommandons de désactiver [La télémétrie d'usage anonyme](https://search.brave.com/help/usage-metrics), car elle est activée par défaut et peut se paramètrer depuis les règlages.

### DuckDuckGo

<div class="admonition recommendation" markdown>

![Logo DuckDuckGo](assets/img/search-engines/duckduckgo.svg){ align=right }

**DuckDuckGo** est l'un des moteurs de recherche privés les plus populaires. Les principales fonctionnalités de recherche de DuckDuckGo incluent les [bangs](https://duckduckgo.com/bang) et de nombreuse [réponses instantanées](https://help.duckduckgo.com/duckduckgo-help-pages/features/instant-answers-and-other-features). Le moteur de recherche utilise beaucoup d'autres [sources](https://help.duckduckgo.com/results/sources) que Bing pour les réponses instantanées et autres résultats non principaux.

DuckDuckGo est le moteur de recherche par défaut sur le [navigateur Tor](tor.md#tor-browser) et est l'une des rares options disponibles sur [Safari](mobile-browsers.md#safari-ios).

[:octicons-home-16: Page d'Accueil](https://duckduckgo.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion){ .card-link title="Service Onion" }
[:octicons-eye-16:](https://duckduckgo.com/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://help.duckduckgo.com){ .card-link title="Documentation" }

</div>

DuckDuckGo propose deux [autres versions](https://help.duckduckgo.com/features/non-javascript) de leur moteur de recherche, lesquels peuvent fonctionner sans JavaScript. Ces versions manquent toutefois de fonctionnalités. Ces versions peuvent être utilisées en complément de leur adresse cachée Tor en ajoutant [/lite](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/lite) ou [/html](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/html) à leur version respective.

### Mullvad Leta

<div class="admonition recommendation" markdown>

![Logo de Mullvad](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad Leta** est un moteur de recherche développé par Mullvad. Il utilise un [cache partagé](https://leta.mullvad.net/faq#what-is-cached-search) pour récupérer les résultats de recherche et limite les appels aux APIs de recherche qu'il utilise.

Mullvad Leta ne propose que des résultats de recherche textuels pour le moment. C'est le moteur de recherche par défaut du [navigateur Mullvad](desktop-browsers.md#mullvad-browser).

[:octicons-home-16: Page d'Accueil](https://leta.mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://uxngojcovdcyrmwkmkltyy2q7enzzvgv7vlqac64f2vl6hcrrqtlskqd.onion){ .card-link title="Service Onion" }
[:octicons-eye-16:](https://leta.mullvad.net/terms-of-service){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://leta.mullvad.net/faq){ .card-link title="Documentation" }

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Mullvad Leta vous permet également de désactiver JavaScript dans votre navigateur, comme le fait [le navigateur Mullvad](desktop-browsers.md#mullvad-browser) lorsqu'il est paramétré sur le niveau de sécurité le plus élevé.

</div>

Mullvad Leta a été [audité](https://mullvad.net/en/blog/security-audit-of-our-letamullvadnet-search-service) par Assured AB en mars 2023. Toutes les failles trouvées ont été résolues rapidement après la publication du [rapport](https://assured.se/publications/Assured_Mullvad_Leta_pentest_report_2023.pdf).

### Startpage

<div class="admonition recommendation" markdown>

![Logo de Startpage](assets/img/search-engines/startpage.svg#only-light){ align=right }
![Startpage logo](assets/img/search-engines/startpage-dark.svg#only-dark){ align=right }

**Startpage** est un moteur de recherche privé. One of Startpage's unique features is the [Anonymous View](https://startpage.com/en/anonymous-view), which puts forth efforts to standardize user activity to make it more difficult to be uniquely identified. The feature can be useful for hiding [some](https://support.startpage.com/hc/articles/4455540212116-The-Anonymous-View-Proxy-technical-details) network and browser properties. Contrairement à ce que son nom suggère, il ne faut pas compter sur cette fonction pour assurer l'anonymat. Si vous recherchez l'anonymat, utilisez plutôt le [Navigateur Tor](tor.md#tor-browser).

[:octicons-home-16: Homepage](https://startpage.com){ .md-button .md-button--primary }
[:simple-torbrowser:](http://startpagel6srwcjlue4zgq3zevrujfaow726kjytqbbjyrswwmjzcqd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://startpage.com/en/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.startpage.com/hc/categories/4481917470356-Startpage-Search-Engine){ .card-link title="Documentation" }

</div>

L'actionnaire majoritaire de Startpage est System1 qui est une société de technologie publicitaire. Nous ne pensons pas que ce soit un problème car ils ont une [politique de confidentialité](https://system1.com/terms/privacy-policy)distincte. The Privacy Guides team reached out to Startpage [back in 2020](https://blog.privacyguides.org/2020/05/03/relisting-startpage) to clear up any concerns with System1's sizeable investment into the service, and we were satisfied with the answers we received.

Startpage previously placed limitations on VPN and [Tor](tor.md) users, but they recently created an [official](https://support.startpage.com/hc/en-us/articles/24786602537364-Startpage-s-Tor-onion-service) Tor hidden service, and as of April 2024 we have no longer noticed extra roadblocks for Tor or [VPN](vpn.md) users.

## Metasearch Engines

A [metasearch engine](https://en.wikipedia.org/wiki/Metasearch_engine) aggregates the results of other search engines, such as the ones recommended above, while not storing any information itself.

### SearXNG

<div class="admonition recommendation" markdown>

![SearXNG logo](assets/img/search-engines/searxng.svg){ align=right }

**SearXNG** is an open-source, self-hostable, metasearch engine. C'est un fork activement maintenu de [SearX](https://github.com/searx/searx).

[:octicons-home-16: Homepage](https://searxng.org){ .md-button .md-button--primary }
[:octicons-server-16:](https://searx.space){ .card-link title="Public Instances" }
[:octicons-code-16:](https://github.com/searxng/searxng){ .card-link title="Source Code" }

</div>

SearXNG est un proxy entre vous et les moteurs de recherche qu'il agrège. Vos requêtes de recherche seront toujours envoyées aux moteurs de recherche dont SearXNG tire ses résultats.

Lorsque vous auto-hébergez, il est important que d'autres personnes utilisent également votre instance pour que vous puissiez vous fondre dans la masse. Vous devriez faire attention à l'endroit et à la manière dont vous hébergez SearXNG, car les personnes qui recherchent du contenu illégal sur votre instance pourraient attirer l'attention des autorités.

Lorsque vous utilisez une instance SearXNG, assurez-vous d'aller lire sa politique de confidentialité. Les instances SearXNG pouvant être modifiées par leurs propriétaires, elles ne reflètent pas nécessairement leur politique de confidentialité. Certaines instances fonctionnent en tant que service caché Tor, ce qui peut garantir une certaine confidentialité tant que vos requêtes de recherche ne contiennent pas de DCP (données à caractère personnelles).

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Must not collect PII per their privacy policy.
- Must not require users to create an account with them.

### Critères optimaux

Nos critères optimaux représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de ces fonctionnalités, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Doit être basé sur des logiciels open-source.
- Ne doit pas bloquer les adresses IP des nœuds de sortie Tor.

[^1]: Brave Search collects aggregated usage metrics, which includes the OS and the user agent. However, they do not collect PII. To serve [anonymous local results](https://search.brave.com/help/anonymous-local-results), IP addresses are temporarily processed, but are not retained.

    Brave Search: [*Brave Search privacy notice*](https://search.brave.com/help/privacy-policy) [^2]: DuckDuckGo **does** log your searches for product improvement purposes, but not your IP address or any other PII.

    DuckDuckGo Privacy Policy: [*We don't track you.*](https://duckduckgo.com/privacy) [^3]: Mullvad Leta logs your searches and stores them hashed with a secret in a RAM-based cache. The cache is removed after it reaches 30 days in age, or when the server-side Leta application is restarted. They do not collect any PII.

    Terms of Service: [*Service Usage*](https://leta.mullvad.net/terms-of-service) [^4]: Startpage logs details such as operating system, user agent, and language. They do not log your IP address, search queries, or other PII.

    Our Privacy Policy: [*How we have implemented truly anonymous analytics*](https://startpage.com/en/privacy-policy#section-4)
