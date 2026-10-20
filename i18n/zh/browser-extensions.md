---
title: 浏览器扩展
icon: material/puzzle-outline
description: 这些浏览器扩展可以增强您的浏览体验并保护您的隐私。
cover: browser-extensions.webp
---

<small>防止以下威胁：</small>

- [:material-account-cash: 监视资本主义](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

通常，我们建议将浏览器扩展保持在最低限度，以减少您的攻击面。它们在您的浏览器中具有特权访问，需要您信任开发者，可能会使您[显眼（产生指纹）](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)，并[削弱](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ)站点隔离。

然而，某些扩展提供的功能在某些情况下可能胜过这些缺点，特别是在涉及[内容拦截](basics/common-threats.md#mass-surveillance-programs)时。

不要安装您目前不需要的扩展，或者与您的浏览器功能重复的扩展。例如，[Brave](desktop-browsers.md#brave) 用户不需要安装 uBlock Origin，因为 Brave Shields 已经提供了相同的功能。

## 内容拦截器

### uBlock Origin

<div class="admonition recommendation" markdown>

![uBlock Origin logo](assets/img/browsers/ublock_origin.svg){ align=right }

**uBlock Origin** 是一款受欢迎的内容拦截器，可以帮助您拦截广告、跟踪器和指纹脚本。

[:octicons-repo-16: 代码库](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="隐私政策" }
[:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=文档}
[:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="源代码" }

<details class="downloads" markdown>
<summary>下载</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)
- [:fontawesome-brands-opera: Opera](https://addons.opera.com/en/extensions/details/ublock/)

</details>

</div>

我们建议遵循[开发者文档](https://github.com/gorhill/uBlock/wiki/Blocking-mode)并选择其中一种“模式”。额外的过滤规则可能会影响性能并[可能增加攻击面](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css)。

这些是您可能考虑添加的其他一些[过滤规则](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists)：

- [x] 勾选 **Privacy** > **AdGuard URL Tracking Protection**
- 添加 [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

### uBlock Origin Lite

uBlock Origin 也有其扩展的“Lite”版本，与原始扩展相比，它提供的功能集有限。然而，与功能齐全的版本相比，它有一些明显的优势，因此如果您符合以下情况，不妨考虑一下...

- ...您不想授予任何扩展（即使像 uBlock Origin 这样受信任的扩展）完全的“读取/修改网站数据”权限
- ...您想要一个资源（内存/CPU）利用率更高的内容拦截器[^1]
- ...您的浏览器只支持 Manifest V3 扩展。 Chrome[^2] 就是这种情况。

<div class="admonition recommendation" markdown>

![uBlock Origin Lite logo](assets/img/browsers/ublock_origin_lite.svg){ align=right }

**uBlock Origin Lite** 是一个兼容 Manifest V3 的内容拦截器。与最初的 _uBlock Origin_ 相比，此扩展不需要广泛的“读取/修改数据”权限即可运行，这降低了由于过滤规则中添加了恶意规则而导致您的浏览器遭受 [:material-bug-outline: 被动攻击](basics/common-threats.md#security-and-privacy){ .pg-orange } 的风险。

[:octicons-repo-16: 代码库](https://github.com/uBlockOrigin/uBOL-home#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uBlockOrigin/uBOL-home/wiki/Privacy-policy){ .card-link title="隐私政策" }
[:octicons-info-16:](https://github.com/uBlockOrigin/uBOL-home/wiki){ .card-link title=文档}
[:octicons-code-16:](https://github.com/gorhill/uBlock/tree/master/platform/mv3){ .card-link title="源代码" }

<details class="downloads" markdown>
<summary>下载</summary>

- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin-lite/ddkjiahejlhfcafbddmgiahcphecmpfh)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/cimighlppcgcoapaliogpjjdehbnofhn)
- [:simple-safari: Safari](https://apps.apple.com/app/id6745342698)

</details>

</div>

只有在您不打算添加任何非默认包含的过滤规则，或者不需要[动态过滤](https://github.com/gorhill/ublock/wiki/dynamic-filtering:-quick-guide)和网络日志记录器等高级选项时，我们才推荐此版本的 uBlock Origin。这些限制是由于 Manifest V3 设计的局限性造成的，特别是对过滤规则数量的硬性限制，以及扩展通常无法获取远程资源的事实。[^3]

此版本提供三个级别的拦截：“基础”无需任何查看和修改站点内容的特殊权限即可工作，而“最佳”和“完整”级别确实需要这种广泛的权限，但可通过附加的外观规则和脚本注入提供更好的过滤体验。

如果您将默认过滤模式设置为“最佳”或“完整”，该扩展将请求访问以读取/修改您访问的**所有**网站。然而，您还可以选择在任意给定的站点上，通过调整扩展弹出面板中的滑块，**按站点**将设置更改为“最佳”或“完整”。当您这样做时，扩展将仅请求对该站点的读取/修改访问权限。因此，如果您想利用 uBlock Origin Lite 的“无权限”配置，您应该将默认设置保持为“基础”，仅在拦截级别不足的站点上将其调高。

uBlock Origin Lite 仅在您的浏览器扩展市场更新该扩展时才会收到拦截规则更新，而不是按需更新。谷歌对过滤更新有[加急审查流程](https://developer.chrome.com/docs/webstore/skip-review)，这意味着您通常仍能像 uBlock Origin Lite 选择发布新版本的频率（历史上每 2-7 天）一样频繁地收到过滤规则更新。然而，只有所谓的“[安全规则 (safe rules)](https://developer.chrome.com/docs/extensions/reference/api/declarativeNetRequest#safe_rules)”才能更新，这可能会限制使用高级技术的规则的更新频率。

### AdGuard

我们向 iOS 用户推荐 [Safari](mobile-browsers.md#safari-ios)，遗憾的是，它只受 uBlock Origin **Lite** 的支持。幸运的是，AdGuard 提供了一个合适的替代方案：

<div class="admonition recommendation" markdown>

![AdGuard logo](assets/img/browsers/adguard.svg){ align=right }

**AdGuard for iOS** 是一款免费且开源的 Safari 内容拦截扩展，它使用原生的 [Content Blocker API](https://developer.apple.com/documentation/safariservices/creating_a_content_blocker)。

[:octicons-home-16: 主页](https://adguard.com/en/adguard-ios/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/ios.html){ .card-link title="隐私政策" }
[:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title=文档}
[:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="源代码" }

<details class="downloads" markdown>
<summary>下载</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1047223162)

</details>

</div>

额外的过滤规则确实会减慢速度并可能增加您的攻击面，因此请仅应用您需要的内容。 AdGuard for iOS 有一些高级功能；但是，标准的 Safari 内容拦截是免费的。

## 标准

- 不得复制内置浏览器或操作系统的功能。
- 必须直接影响用户隐私，即不能简单地提供信息。

[^1]: uBlock Origin Lite _本&#x8EAB;_&#x4E0D;会消耗任何资源，因为它使用了更新的 API，使浏览器原生处理过滤规则，而不是在扩展内运行 JavaScript 代码来处理过滤。然而，这种资源优势只是[理论上的](https://github.com/uBlockOrigin/uBOL-home/wiki/Frequently-asked-questions-(FAQ)#is-ubol-more-efficient-cpu--and-memory-wise-than-ubo)，因为标准的 uBlock Origin 的过滤代码有可能比您浏览器的原生过滤代码更高效。这一结论尚未经过基准测试验证。

[^2]: [Brave](https://brave.com/blog/brave-shields-manifest-v3/) 和 [Opera](https://xcancel.com/Opera_Security/status/2066543496001888753) 已承诺在他们力所能及的范围内维持对 MV2 的支持。

[^3]: 这种情况正在开始改变，因为 MV3 扩展现在可以请求使用脚本。这使得 [AdGuard](https://adguard.com/en/blog/adguard-browser-extension-v5-2.html) 可以提出通过 URL 导入自定义过滤规则，而不是像 uBOL 那样必须手动粘贴规则。
