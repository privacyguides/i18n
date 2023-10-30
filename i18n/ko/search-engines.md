---
meta_title: "검색 엔진 권장 목록: Google 검색 대체제 익명 서비스 - Privacy Guides"
title: "검색 엔진"
icon: material/search-web
description: 프라이버시 중점 검색 엔진은 여러분의 검색 내용을 기반으로 광고 프로필을 구축하지 않습니다.
cover: search-engines.webp
---

여러분의 검색 내용을 기반으로 광고 프로필을 구축하지 않는 검색 엔진을 사용하세요.

본 권장 목록은 각 서비스의 프라이버시 정책을 기반으로 장점을 판단하여 선정되었습니다. 실제로 해당 서비스에서 프라이버시 정책이 제대로 지켜진다는 **보장은 없습니다**.

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

DuckDuckGo는 JavaScript 없이 사용 가능한 버전을 [두 가지](https://help.duckduckgo.com/features/non-javascript/) 제공합니다. 단, JavaScript 없이 사용 가능한 버전은 기능이 완전하지 않습니다. [Tor Onion 주소](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/)에도 [/lite](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/lite)나 [/html](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/html)을 추가하여 사용할 수 있습니다.

## SearXNG

!!! recommendation

    ![SearXNG 로고](assets/img/search-engines/searxng.svg){ align=right }
    
    **SearXNG**는 자체 호스팅 가능한 오픈 소스 메타 검색 엔진입니다. 메타 검색 엔진은 자체적으로 정보를 제공하지 않고 다른 검색 엔진의 결과를 종합합니다. SearXNG는 [SearX](https://github.com/searx/searx)로부터 포크된 프로젝트로, 활발하게 유지 관리되고 있습니다.
    
    [:octicons-home-16: 홈페이지](https://searxng.org){ .md-button .md-button--primary }
    [:octicons-server-16:](https://searx.space/){ .card-link title="공개 인스턴스"}
    [:octicons-code-16:](https://github.com/searxng/searxng){ .card-link title="소스 코드" }

SearXNG는 여러분과 (SearXNG가 결과를 가져오는) 검색 엔진들 사이의 프록시입니다. 여러분의 검색 쿼리는 SearXNG가 결과를 가져오는 검색 엔진으로도 전송됩니다.

자체 호스팅을 할 경우, 다른 사람들도 해당 인스턴스를 사용하도록 하여 검색 쿼리가 뒤섞이게 해야 합니다. 단, 해당 인스턴스에서 불법 콘텐츠를 검색하는 사람들로 인해 당국의 관심을 끌게 될 수 있으므로, 호스팅하는 위치와 방식에 주의해야 합니다.

SearXNG 인스턴스를 사용하는 경우에는 해당 인스턴스의 프라이버시 정책을 반드시 읽어봐야 합니다. 동시에, SearXNG 인스턴스는 소유자가 수정 가능하므로 프라이버시 정책이 실제로는 반영되지 않을 수도 있습니다. 일부 인스턴스는 Tor Onion 서비스로 실행되어, 검색 쿼리에 여러분의 개인 식별 정보가 담겨있지 않는 한 프라이버시를 어느 정도 보장하기도 합니다.

## Startpage

!!! recommendation

    ![Startpage 로고](assets/img/search-engines/startpage.svg#only-light){ align=right }
    ![Startpage 로고](assets/img/search-engines/startpage-dark.svg#only-dark){ align=right }
    
    **Startpage**는 [Google, Bing](https://support.startpage.com/hc/en-us/articles/4522435533844-What-is-the-relationship-between-Startpage-and-your-search-partners-like-Google-and-Microsoft-Bing-) 검색 결과를 제공하는 것으로 유명한 비공개 검색 엔진입니다.  독특한 기능 중 하나로 '[익명 보기(Anonymous View)](https://www.startpage.com/en/anonymous-view/)'라는, 사용자 활동을 표준화해 고유 식별을 어렵게 만드는 기능이 있습니다. 이 기능은 네트워크, 브라우저 관련 [일부 속성](https://support.startpage.com/hc/en-us/articles/4455540212116-The-Anonymous-View-Proxy-technical-details)을 감추는 데에 유용할 수 있습니다. 단, 명칭과는 다르게 해당 기능은 익명성 면에서 의존해서는 안 됩니다. 익명성이 필요한 경우에는 [Tor 브라우저](tor.md#tor-browser)를 사용하세요.
    
    [:octicons-home-16: 홈페이지](https://www.startpage.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.startpage.com/en/privacy-policy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://support.startpage.com/hc/en-us/categories/4481917470356-Startpage-Search-Engine){ .card-link title=문서}

!!! warning "경고"

    Startpage는 VPN이나 Tor에서 쓰이는 IP 등 특정 IP 주소를 자주 차단합니다. 위협 모델상 검색 서비스 제공 업체에게 IP를 노출하지 않고자 하는 분의 경우, [DuckDuckGo](#duckduckgo), [Brave Search](#brave-search)가 더 편리한 선택입니다.

Startpage 본사는 네덜란드에 위치하고 있습니다. [프라이버시 정책](https://www.startpage.com/en/privacy-policy/)에 따르면, 운영 체제, 브라우저 유형, 언어 등 세부 정보를 기록합니다. IP 주소, 검색 쿼리 및 그 외 개인 식별 정보는 기록하지 않습니다.

Startpage 대주주는 System1이라는 애드테크 회사입니다. 별도의 [프라이버시 정책](https://system1.com/terms/privacy-policy)을 가지고 있으므로 문제가 되지는 않을 것으로 판단됩니다. Privacy Guides 팀은 Startpage가 System1으로부터 큰 투자를 받은 것에 대한 우려를 해소하기 위해, [2020년 Startpage측에 연락했습니다](https://web.archive.org/web/20210118031008/https://blog.privacytools.io/relisting-startpage/). Privacy Guides 팀은 해당 답변에 납득했습니다.

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

!!! example "이 단락은 최근에 만들어졌습니다"

    Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

### 최소 요구 사항

- 프라이버시 정책에 따라, 개인 식별 정보를 수집해서는 안 됩니다.
- 해당 서비스에서는 사용자가 계정을 만들 수 없어야 합니다.

### 우대 사항

평가 기준에서 '우대 사항'은 해당 부문에서 완벽한 프로젝트에 기대하는 바를 나타냅니다. 다음의 우대 사항에 해당하지 않더라도 권장 목록에 포함될 수 있습니다. 단, 우대 사항에 해당할수록 이 페이지의 다른 항목보다 높은 순위를 갖습니다.

- 오픈 소스 소프트웨어 기반이어야 합니다.
- Tor 출구 노드 IP 주소를 차단해서는 안 됩니다.
