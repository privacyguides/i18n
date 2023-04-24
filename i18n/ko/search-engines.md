---
meta_title: "Recommended Search Engines: Anonymous Google Alternatives - Privacy Guides"
title: "검색 엔진"
icon: material/search-web
description: 프라이버시 중점 검색 엔진은 여러분의 검색 내용을 기반으로 광고 프로필을 구축하지 않습니다.
cover: search-engines.png
---

여러분의 검색 내용을 기반으로 광고 프로필을 구축하지 않는 검색 엔진을 사용하세요.

The recommendations here are based on the merits of each service's privacy policy. There is **no guarantee** that these privacy policies are honored.

여러분의 위협 모델에 따라, 검색 제공 업체에게 IP 노출을 원치 않을 경우에는 [VPN](vpn.md)이나 [Tor](https://www.torproject.org/)를 사용하세요.

## Brave Search

!!! recommendation

    ![Brave Search 로고](assets/img/search-engines/brave-search.svg){ align=right }
    
    **Brave Search**는 Brave에서 개발했으며, 주로 자체적으로 구축한 독립 색인으로 검색 결과를 제공합니다. 해당 색인은 Google 검색에 최적화되어 있으므로, 다른 대안에 비해 문맥상 더 정확한 결과를 제공할 수 있습니다.
    
    Brave Search는 포럼 게시물 같은 대화 중심 결과를 강조 표시하는 Discussions 등 독특한 기능이 존재합니다.
    
    기본 활성화된 [익명 사용량 지표](https://search.brave.com/help/usage-metrics)는 설정에서 비활성화 가능하므로, 비활성화 할 것을 추천드립니다.
    
    [:octicons-home-16: 홈페이지](https://search.brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://search.brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion 서비스" }
    [:octicons-eye-16:](https://search.brave.com/help/privacy-policy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://search.brave.com/help){ .card-link title=문서}

Brave Search 본사는 미국에 위치하고 있습니다. [프라이버시 정책](https://search.brave.com/help/privacy-policy)에 따르면, 사용 중인 운영 체제 및 브라우저를 포함한 집계된 사용량 지표는 수집하지만, 개인 식별 정보는 수집하지 않는다고 명시되어 있습니다. IP 주소는 일시적으로 처리되지만 보관되지는 않습니다.

## DuckDuckGo

!!! recommendation

    ![DuckDuckGo 로고](assets/img/search-engines/duckduckgo.svg){ align=right }
    
    **DuckDuckGo**는 대표적인 비공개 검색 엔진 중 하나입니다. 주요 검색 기능으로는 [Bang](https://duckduckgo.com/bang) 및 다양한 [즉각적 답변(Instant Answers)](https://help.duckduckgo.com/duckduckgo-help-pages/features/instant-answers-and-other-features/) 등이 있습니다. 상업용 Bing API를 이용해 대부분의 결과를 제공하지만, 즉각적 답변 및 (주요 검색 결과 외의) 기타 결과에는 [수많은 소스](https://help.duckduckgo.com/results/sources/)를 이용합니다.
    
    DuckDuckGo는 Tor 브라우저의 기본 검색 엔진이며, Apple Safari 브라우저에서 사용 가능한 몇 안되는 선택지 중 하나이기도 합니다.
    
    [:octicons-home-16: 홈페이지](https://duckduckgo.com){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion){ .card-link title="Onion 서비스" }
    [:octicons-eye-16:](https://duckduckgo.com/privacy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://help.duckduckgo.com/){ .card-link title=문서}

DuckDuckGo 본사는 미국에 위치하고 있습니다. [프라이버시 정책](https://duckduckgo.com/privacy)에 따르면 제품 개선 목적으로 검색 내용을 **기록하지만**, IP 주소 및 기타 개인 식별 정보는 기록하지 않는다고 명시되어 있습니다.

DuckDuckGo는 JavaScript 없이 사용 가능한 버전을 [두 가지](https://help.duckduckgo.com/features/non-javascript/) 제공합니다. 단, JavaScript 없이 사용 가능한 버전은 기능이 완전하지 않습니다. These versions can also be used in conjunction with their [Tor onion address](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/) by appending [/lite](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/lite) or [/html](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/html) for the respective version.

## SearXNG

!!! recommendation

    ![SearXNG 로고](assets/img/search-engines/searxng.svg){ align=right }
    
    **SearXNG**는 자체 호스팅 가능한 오픈 소스 메타 검색 엔진입니다. 메타 검색 엔진은 자체적으로 정보를 제공하지 않고 다른 검색 엔진의 결과를 종합합니다. SearXNG는 [SearX](https://github.com/searx/searx)로부터 포크된 프로젝트로, 활발하게 유지 관리되고 있습니다.
    
    [:octicons-home-16: 홈페이지](https://searxng.org){ .md-button .md-button--primary }
    [:octicons-server-16:](https://searx.space/){ .card-link title="공개 인스턴스"}
    [:octicons-code-16:](https://github.com/searxng/searxng){ .card-link title="소스 코드" }

SearXNG는 여러분과 (SearXNG가 결과를 가져오는) 검색 엔진들 사이의 프록시입니다. Your search queries will still be sent to the search engines that SearXNG gets its results from.

When self-hosting, it is important that you have other people using your instance so that the queries would blend in. You should be careful with where and how you are hosting SearXNG, as people looking up illegal content on your instance could draw unwanted attention from authorities.

When you are using a SearXNG instance, be sure to go read their privacy policy. Since SearXNG instances may be modified by their owners, they do not necessarily reflect their privacy policy. Some instances run as a Tor hidden service, which may grant some privacy as long as your search queries does not contain PII.

## Startpage

!!! recommendation

    ![Startpage 로고](assets/img/search-engines/startpage.svg#only-light){ align=right }
    ![Startpage 로고](assets/img/search-engines/startpage-dark.svg#only-dark){ align=right }
    
    **Startpage**는 Google 검색 결과를 제공하는 것으로 유명한 비공개 검색 엔진입니다.  One of Startpage's unique features is the [Anonymous View](https://www.startpage.com/en/anonymous-view/), which puts forth efforts to standardize user activity to make it more difficult to be uniquely identified. The feature can be useful for hiding [some](https://support.startpage.com/hc/en-us/articles/4455540212116-The-Anonymous-View-Proxy-technical-details) network and browser properties. Unlike the name suggests, the feature should not be relied upon for anonymity. If you are looking for anonymity, use the [Tor Browser](tor.md#tor-browser) instead.
    
    [:octicons-home-16: 홈페이지](https://www.startpage.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.startpage.com/en/privacy-policy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://support.startpage.com/hc/en-us/categories/4481917470356-Startpage-Search-Engine){ .card-link title=문서}

!!! warning "경고"

    Startpage regularly limits service access to certain IP addresses, such as IPs reserved for VPNs or Tor. [DuckDuckGo](#duckduckgo) and [Brave Search](#brave-search) are friendlier options if your threat model requires hiding your IP address from the search provider.

Startpage is based in the Netherlands. According to their [privacy policy](https://www.startpage.com/en/privacy-policy/), they log details such as: operating system, type of browser, and language. They do not log your IP address, search queries, or other personally identifying information.

Startpage's majority shareholder is System1 who is an adtech company. We don't believe that to be an issue as they have a distinctly separate [privacy policy](https://system1.com/terms/privacy-policy). The Privacy Guides team reached out to Startpage [back in 2020](https://web.archive.org/web/20210118031008/https://blog.privacytools.io/relisting-startpage/) to clear up any concerns with System1's sizeable investment into the service. We were satisfied with the answers we received.

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! example "This section is new"

    We are working on establishing defined criteria for every section of our site, and this may be subject to change. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. There are many factors considered and discussed when we recommend a project, and documenting every single one is a work-in-progress.

### Minimum Requirements

- Must not collect personally identifiable information per their privacy policy.
- Must not allow users to create an account with them.

### Best-Case

Our best-case criteria represents what we would like to see from the perfect project in this category. Our recommendations may not include any or all of this functionality, but those which do may rank higher than others on this page.

- Should be based on open-source software.
- Should not block Tor exit node IP addresses.
