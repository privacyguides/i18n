---
meta_title: "Recommended Search Engines: Anonymous Google Alternatives - Privacy Guides"
title: "Поисковые системы"
icon: material/search-web
description: These privacy-respecting search engines don't build an advertising profile based on your searches.
cover: search-engines.webp
---

Используйте поисковую систему, которая не строит рекламный профиль на основе ваших запросов.

Приведенные здесь рекомендации основаны на политиках конфиденциальности этих сервисов. Не существует **никакой гарантии** того, что эти политики конфиденциальности будут соблюдены.

Consider using a [VPN](vpn.md) or [Tor](tor.md) if your threat model requires hiding your IP address from the search provider.

## Brave Search

<div class="admonition recommendation" markdown>

![Логотип Brave Search](assets/img/search-engines/brave-search.svg){ align=right }

**Brave Search** разработана компанией Brave и предоставляет результаты в основном из своего собственного, независимого индекса. Индекс оптимизирован под Google Search и поэтому может предоставлять более контекстно точные результаты по сравнению с другими альтернативами.

Brave Search включает такие уникальные функции, как Discussions, которая выделяет результаты, ориентированные на общение, например, сообщения на форумах.

Мы рекомендуем вам отключить [Анонимные метрики использования](https://search.brave.com/help/usage-metrics), поскольку они включены по умолчанию и могут быть отключены в настройках.

[:octicons-home-16: Homepage](https://search.brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://search.brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://search.brave.com/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://search.brave.com/help){ .card-link title=Documentation}

</details>

</div>

Компания Brave Search базируется в США. В их [политике конфиденциальности](https://search.brave.com/help/privacy-policy) говорится, что они собирают агрегированные метрики использования, которые включают используемые операционную систему и браузер, однако никакой персонально идентифицируемой информации не собирается. IP-адреса временно обрабатываются, но не сохраняются.

## DuckDuckGo

<div class="admonition recommendation" markdown>

![Логотип DuckDuckGo](assets/img/search-engines/duckduckgo.svg){ align=right }

**DuckDuckGo** - одна из наиболее распространенных приватных поисковых систем. Notable DuckDuckGo search features include [bangs](https://duckduckgo.com/bang) and many [instant answers](https://help.duckduckgo.com/duckduckgo-help-pages/features/instant-answers-and-other-features). The search engine relies on a commercial Bing API to serve most results, but it does use numerous [other sources](https://help.duckduckgo.com/results/sources) for instant answers and other non-primary results.

DuckDuckGo является поисковой системой по умолчанию для браузера Tor и одним из немногих доступных вариантов в браузере Safari от Apple.

[:octicons-home-16: Homepage](https://duckduckgo.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://duckduckgo.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.duckduckgo.com){ .card-link title=Documentation}

</details>

</div>

Компания DuckDuckGo базируется в США. В их [политике конфиденциальности](https://duckduckgo.com/privacy) говорится, что они **ведут логи** ваших поисковых запросов в целях улучшения качества продукции, но не записывают IP-адреса или любую другую личную информацию.

DuckDuckGo offers two [other versions](https://help.duckduckgo.com/features/non-javascript) of their search engine, both of which do not require JavaScript. Однако в этих версиях меньше функций. These versions can also be used in conjunction with their [Tor onion address](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion) by appending [/lite](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/lite) or [/html](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/html) for the respective version.

## SearXNG

<div class="admonition recommendation" markdown>

![Логотип SearXNG](assets/img/search-engines/searxng.svg){ align=right }

**SearXNG** - это мета-поисковая система с открытым исходным кодом и возможностью самостоятельного хостинга, агрегирующая результаты других поисковых систем и не хранящая никакой информации сама. Это активно поддерживаемый форк [SearX](https://github.com/searx/searx).

[:octicons-home-16: Homepage](https://searxng.org){ .md-button .md-button--primary }
[:octicons-server-16:](https://searx.space){ .card-link title="Public Instances"}
[:octicons-code-16:](https://github.com/searxng/searxng){ .card-link title="Source Code" }

</details>

</div>

SearXNG — это прокси между пользователями и поисковыми системами, которые они используют. Ваши поисковые запросы все равно будут отправляться в поисковые системы, из которых SearXNG получает результаты.

При самостоятельном хостинге важно, чтобы ваш экземпляр использовали другие люди, чтобы запросы от нескольких пользователей сливались в один поток запросов. Вы должны быть осторожны с тем, где и как вы размещаете SearXNG, поскольку другие люди, ищущие незаконный контент через ваш экземпляр, могут привлечь нежелательное внимание властей.

Если вы используете экземпляр SearXNG, обязательно ознакомьтесь с его политикой конфиденциальности. Поскольку экземпляры SearXNG могут быть изменены их владельцами, они могут не отражать их политику конфиденциальности. Некоторые экземпляры работают как скрытая служба Tor, что может обеспечить некоторую конфиденциальность, если ваши поисковые запросы не содержат ПД.

## Startpage

<div class="admonition recommendation" markdown>

![Startpage logo](assets/img/search-engines/startpage.svg#only-light){ align=right }
![Startpage logo](assets/img/search-engines/startpage-dark.svg#only-dark){ align=right }

**Startpage** is a private search engine known for serving [Google and Bing](https://support.startpage.com/hc/articles/4522435533844-What-is-the-relationship-between-Startpage-and-your-search-partners-like-Google-and-Microsoft-Bing) search results.  One of Startpage's unique features is the [Anonymous View](https://startpage.com/en/anonymous-view), which puts forth efforts to standardize user activity to make it more difficult to be uniquely identified. The feature can be useful for hiding [some](https://support.startpage.com/hc/articles/4455540212116-The-Anonymous-View-Proxy-technical-details) network and browser properties. Несмотря на название, на эту функцию не следует полагаться для обеспечения анонимности. Если вам нужна анонимность, используйте [Tor Browser](tor.md#tor-browser).

[:octicons-home-16: Homepage](https://startpage.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://startpage.com/en/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.startpage.com/hc/categories/4481917470356-Startpage-Search-Engine){ .card-link title=Documentation}

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

Startpage регулярно ограничивает доступ к сервису для определенных IP-адресов, например, IP-адресов, зарезервированных для VPN или Tor. [DuckDuckGo](#duckduckgo) и [Brave Search](#brave-search) являются более дружественными вариантами, если ваша модель угроз требует скрытия вашего IP-адреса от поставщика поиска.

</div>

Startpage базируется в Нидерландах. According to their [privacy policy](https://startpage.com/en/privacy-policy), they log details such as: operating system, type of browser, and language. Они не хранят ваш IP-адрес, поисковые запросы или другую идентифицирующую вас информацию.

Основным акционером Startpage является компания System1, занимающаяся рекламными технологиями. Мы не считаем это проблемой, поскольку у них есть отдельная [политика конфиденциальности](https://system1.com/terms/privacy-policy). The Privacy Guides team reached out to Startpage [back in 2020](https://web.archive.org/web/20210118031008/https://blog.privacytools.io/relisting-startpage) to clear up any concerns with System1's sizeable investment into the service. Мы были удовлетворены полученными ответами.

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

### Минимальные требования к сервисам

- Не должны собирать информацию, позволяющую установить личность, согласно их политике конфиденциальности.
- Не должны позволять пользователям создавать учетную запись у них.

### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Должны быть основаны на ПО с открытым исходным кодом.
- Не должны блокировать IP-адреса выходящих узлов Tor.
