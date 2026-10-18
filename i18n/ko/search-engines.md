---
meta_title: "추천 검색 엔진: 구글을 대체하는 익명 검색 엔진 - 프라이버시 가이드"
title: 검색 엔진
icon: material/search-web
description: 검색 기록을 바탕으로 광고 프로필을 만들지 않는, 프라이버시를 존중하는 검색 엔진을 사용하세요.
cover: search-engines.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-account-cash: 감시 자본주의](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

검색 기록을 바탕으로 광고 프로필을 만들지 않는 **검색 엔진**을 사용하세요.

## 추천 제공업체 { #recommended-providers }

각 서비스의 개인정보 처리방침에 따르면 여기서 추천하는 서비스는 개인 식별 정보(PII)를 수집하지 않습니다. 이러한 개인정보 처리방침이 지켜진다는 **보장은 없습니다**.

위협 모델상 검색 제공업체로부터 IP 주소를 숨겨야 한다면 [VPN](vpn.md)이나 [토르](tor.md) 사용을 고려해 보세요.

| 제공업체                     | 검색 인덱스                                                                                                                                                               | 토르 히든 서비스                     | 로깅 / 개인정보 처리방침 | 운영 국가 |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- | -------------- | ----- |
| [브레이브 서치](#brave-search) | [자체 인덱스](https://brave.com/search-independence)                                                                                                                      | :material-check:{ .pg-green } | 익명화[^1]        | 미국    |
| [덕덕고](#duckduckgo)       | [빙](https://help.duckduckgo.com/results/sources)                                                                                                                     | :material-check:{ .pg-green } | 익명화[^2]        | 미국    |
| [스타트페이지](#startpage)     | [구글 및 빙](https://support.startpage.com/hc/articles/4522435533844-What-is-the-relationship-between-Startpage-and-your-search-partners-like-Google-and-Microsoft-Bing) | :material-check:{ .pg-green } | 익명화[^3]        | 네덜란드  |

### 브레이브 서치 { #brave-search }

<div class="admonition recommendation" markdown>

![브레이브 서치 로고](assets/img/search-engines/brave-search.svg){ align=right }

**브레이브 서치**는 브레이브가 개발한 검색 엔진입니다. 포럼 게시물처럼 대화 중심의 결과를 강조해 보여 주는 [토론(Discussions)](https://search.brave.com/help/discussions) 같은 고유한 기능이 있습니다.

브레이브 서치는 [브레이브 브라우저](desktop-browsers.md#brave)의 기본 검색 엔진입니다.

[:octicons-home-16: 홈페이지](https://search.brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://search.brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="어니언 서비스" }
[:octicons-eye-16:](https://search.brave.com/help/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://search.brave.com/help){ .card-link title="문서" }

</div>

[익명 사용 지표](https://search.brave.com/help/usage-metrics)는 기본적으로 활성화되어 있으므로, 설정에서 비활성화할 것을 권장합니다.

### 덕덕고 { #duckduckgo }

<div class="admonition recommendation" markdown>

![덕덕고 로고](assets/img/search-engines/duckduckgo.svg){ align=right }

**덕덕고**는 비교적 대중적인 프라이버시 검색 엔진 중 하나입니다. 덕덕고의 주목할 만한 검색 기능으로는 [뱅(bang)](https://duckduckgo.com/bang)과 다양한 [즉답(instant answer)](https://help.duckduckgo.com/duckduckgo-help-pages/features/instant-answers-and-other-features) 기능이 있습니다. 이 검색 엔진은 즉답과 기타 부가 결과를 위해 빙 이외의 다양한 [소스](https://help.duckduckgo.com/results/sources)도 사용합니다.

덕덕고는 [토르 브라우저](tor.md#tor-browser)의 기본 검색 엔진이며, 애플 [사파리](mobile-browsers.md#safari-ios) 브라우저에서 선택할 수 있는 몇 안 되는 검색 엔진 중 하나입니다.

[:octicons-home-16: 홈페이지](https://duckduckgo.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion){ .card-link title="어니언 서비스" }
[:octicons-eye-16:](https://duckduckgo.com/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://help.duckduckgo.com){ .card-link title="문서" }

</div>

덕덕고는 자바스크립트가 필요하지 않은 두 가지 [다른 버전](https://help.duckduckgo.com/features/non-javascript)의 검색 엔진을 제공합니다. 하지만 이 버전들은 일부 기능이 빠져 있습니다. 이 버전들은 토르 히든 주소 뒤에 각각 [/lite](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/lite)나 [/html](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/html)을 붙여 함께 사용할 수도 있습니다.

### 스타트페이지 { #startpage }

<div class="admonition recommendation" markdown>

![스타트페이지 로고](assets/img/search-engines/startpage.svg#only-light){ align=right }
![스타트페이지 로고](assets/img/search-engines/startpage-dark.svg#only-dark){ align=right }

**스타트페이지**는 프라이버시를 보호하는 검색 엔진입니다. 스타트페이지의 고유한 기능 중 하나는 [익명 보기(Anonymous View)](https://startpage.com/en/anonymous-view)로, 사용자 활동을 표준화하여 개인을 고유하게 식별하기 어렵게 만듭니다. 이 기능은 [일부](https://support.startpage.com/hc/articles/4455540212116-The-Anonymous-View-Proxy-technical-details) 네트워크 및 브라우저 속성을 숨기는 데 유용할 수 있습니다. 이름과 달리 익명성을 위해 이 기능에 의존해서는 안 됩니다. 익명성이 필요하다면 대신 [토르 브라우저](tor.md#tor-browser)를 사용하세요.

[:octicons-home-16: 홈페이지](https://startpage.com){ .md-button .md-button--primary }
[:simple-torbrowser:](http://startpagel6srwcjlue4zgq3zevrujfaow726kjytqbbjyrswwmjzcqd.onion){ .card-link title="어니언 서비스" }
[:octicons-eye-16:](https://startpage.com/en/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://support.startpage.com/hc/categories/4481917470356-Startpage-Search-Engine){ .card-link title="문서" }

</div>

스타트페이지의 최대 주주는 애드테크 기업인 System1입니다. System1은 별도의 [개인정보 처리방침](https://system1.com/terms/privacy-policy)을 두고 있으므로 문제가 되지 않는다고 판단합니다. 프라이버시 가이드 팀은 System1의 대규모 투자에 관한 우려를 해소하기 위해 [2020년](https://blog.privacyguides.org/2020/05/03/relisting-startpage) 스타트페이지에 연락했으며, 받은 답변에 만족했습니다.

스타트페이지는 이전에 VPN과 [토르](tor.md) 사용자에게 제한을 두었지만, 최근 [공식](https://support.startpage.com/hc/en-us/articles/24786602537364-Startpage-s-Tor-onion-service) 토르 히든 서비스를 만들었으며, 2024년 4월 기준으로 토르나 [VPN](vpn.md) 사용자에 대한 추가 제약은 더 이상 확인되지 않았습니다.

## 메타 검색 엔진 { #metasearch-engines }

[메타 검색 엔진](https://en.wikipedia.org/wiki/Metasearch_engine)은 위에서 추천한 검색 엔진 같은 다른 검색 엔진의 결과를 모아 보여 주며, 자체적으로는 어떠한 정보도 저장하지 않습니다.

### SearXNG

<div class="admonition recommendation" markdown>

![SearXNG 로고](assets/img/search-engines/searxng.svg){ align=right }

**SearXNG**는 자체 호스팅이 가능한 오픈 소스 메타 검색 엔진입니다. [SearX](https://github.com/searx/searx)에서 포크되어 활발하게 유지 관리되고 있는 프로젝트입니다.

[:octicons-home-16: 홈페이지](https://searxng.org){ .md-button .md-button--primary }
[:octicons-server-16:](https://searx.space){ .card-link title="공개 인스턴스" }
[:octicons-code-16:](https://github.com/searxng/searxng){ .card-link title="소스 코드" }

</div>

SearXNG는 여러분과 SearXNG가 결과를 모으는 검색 엔진 사이에 있는 프록시입니다. 여러분의 검색 쿼리는 여전히 SearXNG가 결과를 가져오는 검색 엔진으로 전송됩니다.

자체 호스팅한다면, 검색 쿼리가 다른 쿼리 사이에 섞일 수 있도록 다른 사람들도 여러분의 인스턴스를 사용하는 것이 중요합니다. 여러분의 인스턴스에서 불법 콘텐츠를 검색하는 사람이 있으면 당국의 원치 않는 관심을 받을 수 있으므로, SearXNG를 어디서 어떻게 호스팅할지 주의해야 합니다.

SearXNG 인스턴스를 사용할 때는 해당 인스턴스의 개인정보 처리방침을 꼭 읽어 보세요. SearXNG 인스턴스는 운영자가 수정할 수 있으므로, 개인정보 처리방침이 실제 운영을 반영하지 않을 수도 있습니다. 일부 인스턴스는 토르 히든 서비스로 운영되므로, 검색 쿼리에 PII가 포함되지 않는 한 어느 정도 프라이버시를 제공할 수 있습니다.

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

### 최소 요구 사항 { #minimum-requirements }

- 개인정보 처리방침에 따라 PII를 수집하지 않아야 합니다.
- 사용자에게 계정 생성을 요구해서는 안 됩니다.

### 우대 사항 { #best-case }

우대 사항은 이 카테고리에서 완벽한 프로젝트라면 갖추었으면 하는 사항을 나타냅니다. 추천 항목에 이 기능 중 일부 또는 전부가 없을 수도 있지만, 이러한 기능을 갖춘 항목은 이 페이지에서 다른 항목보다 높은 순위에 오를 수 있습니다.

- 오픈 소스 소프트웨어를 기반으로 하는 것이 좋습니다.
- 토르 출구 노드의 IP 주소를 차단하지 않는 것이 좋습니다.

[^1]: 브레이브 서치는 운영 체제와 사용자 에이전트를 포함한 집계된 사용 지표를 수집합니다. 하지만 PII는 수집하지 않습니다. [익명 지역 검색 결과](https://search.brave.com/help/anonymous-local-results)를 제공하기 위해 IP 주소를 일시적으로 처리하지만, 보관하지는 않습니다.

    브레이브 서치: [*브레이브 서치 개인정보 처리방침*](https://search.brave.com/help/privacy-policy) [^2]: 덕덕고는 제품 개선을 위해 검색 기록을 기록**하지만**, IP 주소나 기타 PII는 기록하지 않습니다.

    덕덕고 개인정보 처리방침: [*저희는 여러분을 추적하지 않습니다.*](https://duckduckgo.com/privacy) [^3]: 스타트페이지는 운영 체제, 사용자 에이전트, 언어 같은 세부 정보를 기록합니다. IP 주소, 검색 쿼리, 기타 PII는 기록하지 않습니다.

    스타트페이지 개인정보 처리방침: [*진정한 익명 분석을 구현한 방법*](https://startpage.com/en/privacy-policy#section-4)
