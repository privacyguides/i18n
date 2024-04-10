---
meta_title: "Moteurs de recherche recommandés : alternatives anonymes à Google - Privacy Guides"
title: "Moteurs de recherche"
icon: material/search-web
description: Ces moteurs de recherche respectueux de la vie privée n'établissent pas de profil publicitaire sur la base de vos recherches.
cover: search-engines.webp
---

Utilisez un moteur de recherche qui ne construit pas un profil publicitaire en fonction de vos recherches.

Les recommandations formulées ici sont fondées sur les mérites de la politique de confidentialité de chaque service. Il n'y a **aucune garantie** que ces politiques de confidentialité soient respectées.

Consider using a [VPN](vpn.md) or [Tor](tor.md) if your threat model requires hiding your IP address from the search provider.

## Brave Search

<div class="admonition recommendation" markdown>

![Logo de Brave Search](assets/img/search-engines/brave-search.svg){ align=right }

**Brave Search** est développé par Brave et fournit des résultats provenant principalement de son propre index indépendant. L'index est optimisé en se basant sur Google Search et peut donc fournir des résultats contextuellement plus précis que d'autres solutions.

Brave Search comprend des fonctionnalités uniques telles que Discussions, qui met en évidence les résultats axés sur la conversation, comme les messages des forums.

Nous vous recommandons de désactiver [Mesures d'utilisation anonymes](https://search.brave.com/help/usage-metrics) car ells sont activées par défaut et peuvent être désactivées dans les paramètres.

[:octicons-home-16: Homepage](https://search.brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://search.brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://search.brave.com/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://search.brave.com/help){ .card-link title=Documentation}

</details>

</div>

Brave Search est basé aux États-Unis. Leur [politique de confidentialité](https://search.brave.com/help/privacy-policy) indique qu'ils collectent des données d'utilisation agrégées, notamment le système d'exploitation et le navigateur utilisés, mais qu'aucune information permettant d'identifier une personne n'est collectée. Les adresses IP sont traitées temporairement, mais ne sont pas conservées.

## DuckDuckGo

<div class="admonition recommendation" markdown>

![Logo DuckDuckGo](assets/img/search-engines/duckduckgo.svg){ align=right }

**DuckDuckGo** est l'un des moteurs de recherche privés les plus populaires. Notable DuckDuckGo search features include [bangs](https://duckduckgo.com/bang) and many [instant answers](https://help.duckduckgo.com/duckduckgo-help-pages/features/instant-answers-and-other-features). The search engine relies on a commercial Bing API to serve most results, but it does use numerous [other sources](https://help.duckduckgo.com/results/sources) for instant answers and other non-primary results.

DuckDuckGo est le moteur de recherche par défaut du navigateur Tor et l'une des rares options disponibles sur le navigateur Safari d'Apple.

[:octicons-home-16: Homepage](https://duckduckgo.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://duckduckgo.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.duckduckgo.com){ .card-link title=Documentation}

</details>

</div>

DuckDuckGo est basé aux États-Unis. Leur [politique de confidentialité](https://duckduckgo.com/privacy) indique qu'ils **font** enregistrer vos recherches à des fins d'amélioration des produits, mais pas votre adresse IP ou toute autre information d'identification personnelle.

DuckDuckGo offers two [other versions](https://help.duckduckgo.com/features/non-javascript) of their search engine, both of which do not require JavaScript. Ces versions manquent toutefois de fonctionnalités. These versions can also be used in conjunction with their [Tor onion address](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion) by appending [/lite](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/lite) or [/html](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/html) for the respective version.

## SearXNG

<div class="admonition recommendation" markdown>

![Logo SearXNG](assets/img/search-engines/searxng.svg){ align=right }

**SearXNG** est un métamoteur de recherche open-source, auto-hébergeable, qui agrège les résultats d'autres moteurs de recherche sans stocker lui-même d'informations. C'est un fork activement maintenu de [SearX](https://github.com/searx/searx).

[:octicons-home-16: Homepage](https://searxng.org){ .md-button .md-button--primary }
[:octicons-server-16:](https://searx.space){ .card-link title="Public Instances"}
[:octicons-code-16:](https://github.com/searxng/searxng){ .card-link title="Source Code" }

</details>

</div>

SearXNG est un proxy entre vous et les moteurs de recherche qu'il agrège. Vos requêtes de recherche seront toujours envoyées aux moteurs de recherche dont SearXNG tire ses résultats.

Lorsque vous auto-hébergez, il est important que d'autres personnes utilisent également votre instance pour que vous puissiez vous fondre dans la masse. Vous devriez faire attention à l'endroit et à la manière dont vous hébergez SearXNG, car les personnes qui recherchent du contenu illégal sur votre instance pourraient attirer l'attention des autorités.

Lorsque vous utilisez une instance SearXNG, assurez-vous d'aller lire sa politique de confidentialité. Les instances SearXNG pouvant être modifiées par leurs propriétaires, elles ne reflètent pas nécessairement leur politique de confidentialité. Certaines instances fonctionnent en tant que service caché Tor, ce qui peut garantir une certaine confidentialité tant que vos requêtes de recherche ne contiennent pas de DCP (données à caractère personnelles).

## Startpage

<div class="admonition recommendation" markdown>

![Startpage logo](assets/img/search-engines/startpage.svg#only-light){ align=right }
![Startpage logo](assets/img/search-engines/startpage-dark.svg#only-dark){ align=right }

**Startpage** is a private search engine known for serving [Google and Bing](https://support.startpage.com/hc/articles/4522435533844-What-is-the-relationship-between-Startpage-and-your-search-partners-like-Google-and-Microsoft-Bing) search results.  One of Startpage's unique features is the [Anonymous View](https://startpage.com/en/anonymous-view), which puts forth efforts to standardize user activity to make it more difficult to be uniquely identified. The feature can be useful for hiding [some](https://support.startpage.com/hc/articles/4455540212116-The-Anonymous-View-Proxy-technical-details) network and browser properties. Contrairement à ce que son nom suggère, il ne faut pas compter sur cette fonction pour assurer l'anonymat. Si vous recherchez l'anonymat, utilisez plutôt le [Navigateur Tor](tor.md#tor-browser).

[:octicons-home-16: Homepage](https://startpage.com){ .md-button .md-button--primary }
[:simple-torbrowser:](http://startpagel6srwcjlue4zgq3zevrujfaow726kjytqbbjyrswwmjzcqd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://startpage.com/en/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.startpage.com/hc/categories/4481917470356-Startpage-Search-Engine){ .card-link title=Documentation}

</details>

</div>

Startpage est basée aux Pays-Bas. According to their [privacy policy](https://startpage.com/en/privacy-policy), they log details such as: operating system, type of browser, and language. Ils n'enregistrent pas votre adresse IP, vos requêtes de recherche ou d'autres informations à caractère personnel.

L'actionnaire majoritaire de Startpage est System1 qui est une société de technologie publicitaire. Nous ne pensons pas que ce soit un problème car ils ont une [politique de confidentialité](https://system1.com/terms/privacy-policy)distincte. The Privacy Guides team reached out to Startpage [back in 2020](https://blog.privacyguides.org/2020/05/03/relisting-startpage) to clear up any concerns with System1's sizeable investment into the service, and we were satisfied with the answers we received.

Startpage previously placed limitations on VPN and [Tor](tor.md) users, but they recently created an [official](https://support.startpage.com/hc/en-us/articles/24786602537364-Startpage-s-Tor-onion-service) Tor hidden service, and as of April 2024 we have no longer noticed extra roadblocks for Tor or [VPN](vpn.md) users.

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Ne doit pas collecter d'informations permettant d'identifier une personne, conformément à sa politique de confidentialité.
- Ne doit pas permettre aux utilisateurs de créer un compte chez eux.

### Dans le meilleur des cas

Nos critères de cas idéal représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de cette fonctionnalité, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Doit être basé sur des logiciels open-source.
- Ne doit pas bloquer les adresses IP des nœuds de sortie Tor.
