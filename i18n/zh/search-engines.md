---
meta_title: "推荐的搜索引擎：Google的匿名替代品 - Privacy Guides"
title: 搜索引擎
icon: material/search-web
description: 使用尊重隐私的搜索引擎，它们不会根据您的搜索构建广告档案。
cover: search-engines.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>防御以下威胁：</small>

- [:material-account-cash: 监视资本主义](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

使用不基于您的搜索记录构建广告档案的**搜索引擎**。

## 推荐的服务商

根据各服务的隐私政策，此处的推荐内容不会收集个人身份信息（PII）。**无法保证**这些隐私政策会得到遵守。

如果您的威胁模型需要向搜索提供商隐藏您的IP地址，请考虑使用 [VPN](vpn.md) 或 [Tor](tor.md)。

| 提供商                           | 搜索索引                                                                                                                                                                        | Tor隐藏服务                       | 日志/隐私政策 | 运营国家 |
| ----------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- | ------- | ---- |
| [Brave Search](#brave-search) | [独立](https://brave.com/search-independence)                                                                                                                                 | :material-check:{ .pg-green } | 匿名化[^1] | 美国   |
| [DuckDuckGo](#duckduckgo)     | [Bing](https://help.duckduckgo.com/results/sources)                                                                                                                         | :material-check:{ .pg-green } | 匿名化[^2] | 美国   |
| [Startpage](#startpage)       | [Google 和 Bing](https://support.startpage.com/hc/articles/4522435533844-What-is-the-relationship-between-Startpage-and-your-search-partners-like-Google-and-Microsoft-Bing) | :material-check:{ .pg-green } | 匿名化[^3] | 荷兰   |

### Brave Search

<div class="admonition recommendation" markdown>

![Brave Search logo](assets/img/search-engines/brave-search.svg){ align=right }

**Brave Search** 是由 Brave 开发的搜索引擎。它包含一些独特的功能，例如 [Discussions](https://search.brave.com/help/discussions)，该功能会突出显示以对话为中心的结果，例如论坛帖子。

Brave Search 是 [Brave 浏览器](desktop-browsers.md#brave) 的默认搜索引擎。

[:octicons-home-16: 主页](https://search.brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://search.brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="洋葱服务" }
[:octicons-eye-16:](https://search.brave.com/help/privacy-policy){ .card-link title="隐私政策" }
[:octicons-info-16:](https://search.brave.com/help){ .card-link title="文档" }

</div>

我们建议您禁用[“匿名使用统计”功能](https://search.brave.com/help/usage-metrics)，因为该功能默认处于启用状态，您可以在设置中将其禁用。

### DuckDuckGo

<div class="admonition recommendation" markdown>

![DuckDuckGo logo](assets/img/search-engines/duckduckgo.svg){ align=right }

**DuckDuckGo** 是更主流的隐私搜索引擎选项之一。 DuckDuckGo 著名的搜索功能包括 [bangs](https://duckduckgo.com/bang) 和各种 [即时答案](https://help.duckduckgo.com/duckduckgo-help-pages/features/instant-answers-and-other-features)。该搜索引擎除了使用 Bing 之外，还使用众多 [其他来源](https://help.duckduckgo.com/results/sources) 提供即时答案和其他非主要结果。

DuckDuckGo 是 [Tor 浏览器](tor.md#tor-browser) 的默认搜索引擎，也是 Apple 的 [Safari](mobile-browsers.md#safari-ios) 浏览器上少数可用的选项之一。

[:octicons-home-16: 主页](https://duckduckgo.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion){ .card-link title="洋葱服务" }
[:octicons-eye-16:](https://duckduckgo.com/privacy){ .card-link title="隐私政策" }
[:octicons-info-16:](https://help.duckduckgo.com){ .card-link title="文档" }

</div>

DuckDuckGo 提供其搜索引擎的另外两种 [版本](https://help.duckduckgo.com/features/non-javascript)，这两个版本都不需要 JavaScript。不过，这些版本确实缺少一些功能。这些版本还可以与它们的 Tor 隐藏地址一起使用，只需为其各自的版本附加 [/lite](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/lite) 或 [/html](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/html) 即可。

### Startpage

<div class="admonition recommendation" markdown>

![Startpage logo](assets/img/search-engines/startpage.svg#only-light){ align=right }
![Startpage logo](assets/img/search-engines/startpage-dark.svg#only-dark){ align=right }

**Startpage** 是一个隐私搜索引擎。 Startpage 的独特功能之一是 [匿名视图](https://startpage.com/en/anonymous-view)，它致力于标准化用户活动，使其更难被唯一识别。该功能可用于隐藏 [某些](https://support.startpage.com/hc/articles/4455540212116-The-Anonymous-View-Proxy-technical-details) 网络和浏览器属性。与其名称不同，不应依赖该功能来实现匿名。如果您在寻找匿名性，请使用 [Tor 浏览器](tor.md#tor-browser)。

[:octicons-home-16: 主页](https://startpage.com){ .md-button .md-button--primary }
[:simple-torbrowser:](http://startpagel6srwcjlue4zgq3zevrujfaow726kjytqbbjyrswwmjzcqd.onion){ .card-link title="洋葱服务" }
[:octicons-eye-16:](https://startpage.com/en/privacy-policy){ .card-link title="隐私政策" }
[:octicons-info-16:](https://support.startpage.com/hc/categories/4481917470356-Startpage-Search-Engine){ .card-link title="文档" }

</div>

Startpage 的多数股东是广告技术公司 System1。我们认为这不是问题，因为他们有明显独立的 [隐私政策](https://system1.com/terms/privacy-policy)。 Privacy Guides 团队 [早在 2020 年](https://blog.privacyguides.org/2020/05/03/relisting-startpage) 就联系了 Startpage，以澄清对 System1 对该服务的大量投资的任何疑虑，我们对收到的答复感到满意。

Startpage 之前对 VPN 和 [Tor](tor.md) 用户施加了限制，但他们最近创建了一个 [官方](https://support.startpage.com/hc/en-us/articles/24786602537364-Startpage-s-Tor-onion-service) Tor 隐藏服务，截至 2024 年 4 月，我们不再注意到 Tor 或 [VPN](vpn.md) 用户有额外的障碍。

## 元搜索引擎

[元搜索引擎](https://en.wikipedia.org/wiki/Metasearch_engine) 汇总其他搜索引擎（例如上面推荐的引擎）的结果，而本身不存储任何信息。

### SearXNG

<div class="admonition recommendation" markdown>

![SearXNG logo](assets/img/search-engines/searxng.svg){ align=right }

**SearXNG** 是一个开源的、可自托管的元搜索引擎。它是 [SearX](https://github.com/searx/searx) 的一个积极维护的分支。

[:octicons-home-16: 主页](https://searxng.org){ .md-button .md-button--primary }
[:octicons-server-16:](https://searx.space){ .card-link title="公共实例" }
[:octicons-code-16:](https://github.com/searxng/searxng){ .card-link title="源代码" }

</div>

SearXNG 是您和它汇总的搜索引擎之间的代理。您的搜索查询仍将发送到 SearXNG 获取其结果的搜索引擎。

当自托管时，重要的是要有其他人使用您的实例，以便查询能够混合在一起。您应该小心托管 SearXNG 的位置和方式，因为人们在您的实例上查找非法内容可能会引起当局不必要的关注。

当您使用 SearXNG 实例时，请务必阅读他们的隐私政策。由于 SearXNG 实例可能被其所有者修改，因此它们不一定反映其隐私政策。某些实例作为 Tor 隐藏服务运行，只要您的搜索查询不包含 PII，这可能会提供一些隐私。

## 标准

**请注意，我们不隶属于我们推荐的任何项目。** 除了 [我们的标准](about/criteria.md) 之外，我们还制定了一套明确的要求，以使我们能够提供客观的建议。我们建议您在选择使用某个项目之前熟悉此列表，并进行自己的研究，以确保它是适合您的选择。

### 最低要求

- 根据其隐私政策，不得收集 PII。
- 不得要求用户在他们那里创建帐户。

### 最佳情况

我们的最佳情况标准代表了我们希望在此类别中从完美项目中看到的特性。我们的建议可能不包含其中任何或所有功能，但那些具备这些功能的建议可能会在此页面上的排名高于其他建议。

- 应基于开源软件。
- 不应阻止 Tor 出口节点 IP 地址。

[^1]: Brave Search 会收集汇总的使用指标，其中包括操作系统和用户代理。但是，它们不收集 PII。为了提供 [匿名的本地结果](https://search.brave.com/help/anonymous-local-results)，IP 地址会被暂时处理，但不会保留。

    Brave Search：[*Brave Search 隐私声明*](https://search.brave.com/help/privacy-policy) [^2]: DuckDuckGo **确实** 出于改进产品的目的记录了您的搜索，但不会记录您的 IP 地址或任何其他 PII。

    DuckDuckGo 隐私政策：[*我们不跟踪您。*](https://duckduckgo.com/privacy) [^3]: Startpage 记录详细信息，例如操作系统、用户代理和语言。他们不会记录您的 IP 地址、搜索查询或其他 PII。

    我们的隐私政策：[*我们如何实施真正匿名的分析*](https://startpage.com/en/privacy-policy#section-4)
