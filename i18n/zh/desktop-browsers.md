---
meta_title: "尊重隐私的 PC 和 Mac 网络浏览器 - Privacy Guides"
title: 电脑浏览器
icon: material/laptop
description: 我们目前推荐使用这些隐私保护型浏览器，这些浏览器可以在桌面系统上用于标准和非匿名的上网方式。
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: 隐私桌面端浏览器建议
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/en/browser
    applicationCategory: Web Browser
    operatingSystem:
      - Windows 系统
      - mac系统
      - Linux系统
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Firefox（火狐浏览器）
    image: /assets/img/browsers/firefox.svg
    url: https://firefox.com
    sameAs: https://en.wikipedia.org/wiki/Firefox
    applicationCategory: Web Browser
    operatingSystem:
      - Windows 系统
      - mac系统
      - Linux系统
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    sameAs: https://en.wikipedia.org/wiki/Brave_(web_browser)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows 系统
      - mac系统
      - Linux系统
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>可防范以下威胁：</small>

- [:material-account-cash: 监视资本主义](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

这些是我们目前推荐的用于标准及非匿名浏览的**桌面浏览器**和配置。如果你需要强大的隐私保护和开箱即用的防指纹功能，我们推荐 [Mullvad 浏览器](#mullvad-browser) ；如果你需要谷歌 Chrome 浏览器的良好替代品，我们推荐 [Firefox](#firefox) ；如果你需要 Chromium 浏览器的兼容性，我们推荐 [Brave](#brave)。

如果你需要匿名浏览互联网，你需要改用[Tor 浏览器](tor.md)。本页面提供了一些配置建议，但 Tor 浏览器能提供最佳的防网络追踪保护。

## Mullvad 浏览器

<div class="admonition recommendation" markdown>

![Mullvad 浏览器logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad 浏览器** 是 [Tor 浏览器](tor.md#tor-browser) 的一个版本，其中已移除了与 Tor 网络的集成功能。该项目旨在为VPN用户提供Tor浏览器中的反指纹识别技术，这些技术是抵御[:material-eye-outline: 大规模监控](basics/common-threats.md#mass-surveillance-programs){ .pg-blue } 的关键防护措施。该软件由Tor项目开发，由[Mullvad](vpn.md#mullvad)发行，且**无需**使用Mullvad的VPN。

[:octicons-home-16: 主页](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="隐私条款" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="文档"}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="源代码" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

与[Tor 浏览器](tor.md)类似，Mullvad 浏览器旨在通过使您的浏览器指纹与大量其他 Mullvad 浏览器用户保持相似，从而防止指纹识别；它包含默认设置和扩展程序，这些设置和扩展程序会根据默认安全级别：*标准*、*更安全*、*最安全*来自动配置。

因此，除调整默认的[安全级别](https://tb-manual.torproject.org/security-settings)外，切勿对浏览器进行任何其他修改。调整安全级别后，你**必须**先重启浏览器，然后才能继续使用。否则，[安全设置可能无法完全生效](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw)，这会使您面临比根据所选设置所预期的更高的指纹识别和漏洞利用风险。

其他修改会使您的指纹变得独一无二，从而失去使用该浏览器的意义。如果你想对浏览器进行更多的配置而且不担心指纹识别，我们建议你使用 [Firefox](#firefox)。

### 防指纹

**即使不**使用[VPN](vpn.md)，Mullvad浏览器也能像[Firefox+Arkenfox](#arkenfox-advanced)或[Brave](#brave)等其他隐私浏览器一样，抵御[简单的指纹识别脚本](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting)。 Mullvad 浏览器自带这些保护，但牺牲了其他隐私浏览器提供的一些灵活性和便利性。

==为了最完善的反指纹保护，我们建议将 Mullvad 浏览器与 **和** VPN== 结合使用，无论是 Mullvad 还是其他推荐的 VPN 提供商。在使用 Mullvad 浏览器的 VPN 时，你将与许多其他用户共享一个指纹和一个 IP 地址池，使你混入“人群”。这种策略是防御高级跟踪脚本的最佳方法，也是 Tor 浏览器使用的相同反指纹技术。

请注意，虽然您可以将 Mullvad 浏览器与任何 VPN 提供商一起使用，但该 VPN 上的其他人也必须使用 Mullvad 浏览器才能存在这种“人群”，与其他提供商相比，这在 Mullvad VPN 上更有可能发生。 Mullvad 浏览器没有内置 VPN 连接，也不会在浏览前检查你是否在使用 VPN；你的 VPN 连接必须单独配置和管理。

Mullvad 浏览器预装了 *uBlock Origin* 和 *NoScript* 浏览器扩展程序。虽然我们通常不鼓励添加*额外的*[浏览器扩展](browser-extensions.md)，但**不应**删除浏览器预装的这些扩展或将其配置为默认值以外的值，因为这样做会明显使您的浏览器指纹有别于其他 Mullvad 浏览器用户。它还预装了 Mullvad 浏览器扩展，如果您愿意，*可以*安全地将其删除，而不会[影响](https://mullvad.net/en/help/tag/mullvad-browser#112)您的浏览器指纹，但即使您不使用 Mullvad VPN，保留它也是安全的。

### 无痕模式

Mullvad 浏览器一直在无痕浏览模式下运行，这意味着每次关闭浏览器时，你的历史记录、cookies 和其他网站数据都会被清除。您的书签、浏览器设置和扩展程序设置会被保留。

这是防止深度跟踪的必要条件，但确实牺牲了一些便利性和一些 Firefox 的功能（如多账户容器）。当然，您可以同时使用多种浏览器，例如，您可以考虑使用 Firefox+Arkenfox 浏览一些需要保持登录状态或在 Mullvad 浏览器中无法正常运行的网站，并使用 Mullvad 浏览器进行一般浏览。

## Firefox（火狐浏览器）

<div class="admonition recommendation" markdown>

![火狐标志](assets/img/browsers/firefox.svg){ align=right }

**火狐浏览器**提供强大的隐私设置，如[增强型跟踪保护](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop)，它可以帮助阻止各种[跟踪类型](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks)。

[:octicons-home-16: 主页](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="隐私政策" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title=文档}
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="源代码" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="贡献" }

<details class="downloads" markdown>
<summary>下载</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Firefox 在从 Mozilla 网站下载的文件中包含一个唯一的 [下载令牌](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0)，并利用 Firefox 中的遥测功能发送该令牌。该令牌**未**包含在 [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/) 发布的版本中。

</div>

### 推荐的 Firefox 配置

这些选项可在 :material-menu: →**“设置”** 中找到。

#### 搜索

- [ ] 取消勾选**“显示搜索建议”**

您所在的地区可能无法使用搜索建议功能。

搜索建议会将您在地址栏中输入的所有内容发送至默认搜索引擎，无论您是否提交了实际的搜索请求。禁用搜索建议功能可让您更精确地控制发送给搜索引擎提供商的数据。

##### Firefox 建议

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) 是一项类似于搜索建议的功能。出于与建议禁用搜索建议相同的原因，我们建议将其禁用。如果您在**地址栏**标题下没有看到这些选项，则说明您没有新体验，可以忽略这些更改。

- [ ] 取消选中**来自 Firefox 的建议**
- [ ] 取消选中 **来自赞助商的建议**

> 根据 Mozilla 的说法，[“Firefox Suggest 的某些部分目前仅在某些地区可用。”](https://support.mozilla.org/kb/firefox-suggest)

#### 隐私与安全

##### 增强跟踪保护

- [x] 选择 **严格的** 增强跟踪保护

这通过阻止社交媒体跟踪器、指纹脚本（请注意，这并不能保护您免受*所有*指纹识别）、加密货币矿工、跨站点跟踪 cookie 和一些其他跟踪内容来保护您。 ETP 可防御许多常见威胁，但它不会阻止所有跟踪途径，因为它的设计旨在对网站可用性产生最小甚至没有影响。

##### 关闭时消毒

如果您想在特定网站上保持登录状态，可以在**Cookie 和网站数据** → **管理例外情况...**中允许例外情况。

- [x] 勾选 **当Firefox关闭时，删除cookies和网站数据**

这可以保护您免受持久性 cookie 的影响，但不能保护您免受在任何一次浏览会话期间获取的 cookie 的影响。启用此功能后，只需重新启动 Firefox 即可轻松清除浏览器 cookie。如果您希望在经常访问的特定网站上保持登录状态，则可以按网站设置例外情况。

##### 遥测

- [ ] 取消选中**允许 Firefox 向 Mozilla 发送技术与交互数据**
- [ ] 取消选中**允许 Firefox 推荐个性化扩展**
- [ ] 取消选中**允许 Firefox 安装并运行研究项目**
- [ ] 取消选中**向 Mozilla 发送每日使用情况**
- [ ] 取消选中**自动发送崩溃报告**

根据 Mozilla 的 Firefox 隐私政策，

> 火狐浏览器会向我们发送有关您的火狐浏览器版本和语言、设备操作系统和硬件配置、内存、有关崩溃和错误的基本信息以及更新、安全浏览和激活等自动处理结果的数据。当火狐浏览器向我们发送数据时，您的IP地址会被暂时收集，作为我们服务器日志的一部分。

此外，Mozilla 帐户服务会收集[一些技术数据](https://mozilla.org/privacy/mozilla-accounts)。如果您使用 Mozilla 帐户，则可以选择退出：

1. 在 accounts.firefox.com</a>上打开你的

配置文件设置。</li> 
   
   2 取消勾选 **数据收集和使用** > **帮助改进火狐账户**</ol> 



##### 仅 HTTPS 模式

- [x] 选择 **启用所有窗口的纯HTTPS-Only模式**

这可以防止您无意中以纯文本 HTTP 连接到网站。如今没有 HTTPS 的网站并不常见，因此这应该对您的日常浏览几乎没有影响。



##### DNS over HTTPS

如果您使用 [DNS over HTTPS 提供商](dns.md)：

- [x] 选择 **最强保护** 并选择一个合适的提供商

最大保护强制使用 DNS over HTTPS，如果 Firefox 无法连接到您的安全 DNS 解析器，或者如果您的安全 DNS 解析器表示您尝试访问的域的记录不存在，则会显示安全警告。这可以阻止您连接的网络秘密降低您的 DNS 安全性。



#### 同步

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) 允许在您的所有设备上访问您的浏览数据（历史记录、书签等），并使用 E2EE 对其进行保护。



### Arkenfox (advanced)

<div class="admonition tip" markdown>
<p class="admonition-title">使用 Mullvad 浏览器进行高级反指纹识别</p>

[Mullvad 浏览器](#mullvad-browser)开箱即提供比 Firefox 更强的反指纹保护，并且不需要使用 Mullvad 的 VPN 即可受益于这些保护。结合 VPN，Mullvad 浏览器可以阻止 Arkenfox 无法阻止的更高级的跟踪脚本。 Firefox 仍然具有更加灵活的优势，并允许对您需要保持登录状态的网站进行按站点例外处理。

</div>

[Arkenfox 项目](https://github.com/arkenfox/user.js)为 Firefox 提供了一组经过仔细考虑的选项。如果您[决定](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not)使用 Arkenfox，[一些选项](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-%5BCommon%5D)主观上很严格和/或可能导致某些网站无法正常工作——您可以[轻松更改](https://github.com/arkenfox/user.js/wiki/3.1-Overrides)这些选项以满足您的需求。我们**强烈建议**通读其完整的 [wiki](https://github.com/arkenfox/user.js/wiki)。 Arkenfox 还启用了[容器](https://support.mozilla.org/kb/containers#w_for-advanced-users)支持。

Arkenfox 仅旨在通过Canvas随机化和 Firefox 内置的抗指纹配置设置来阻止基本或简单的跟踪脚本。它并不像 Mullvad 浏览器或 Tor 浏览器那样使您的浏览器与大量其他 Arkenfox 用户融为一体，这是阻止高级指纹跟踪脚本的唯一方法。请记住，您始终可以使用多个浏览器，例如，您可以考虑将 Firefox+Arkenfox 用于您想要保持登录状态或以其他方式信任的少数网站，并将 Mullvad 浏览器用于一般浏览。



## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave 浏览器**包含内置的内容拦截器和[隐私功能](https://brave.com/privacy-features)，其中许多功能默认启用。

Brave是建立在Chromium网络浏览器项目之上的，所以它应该有熟悉的感觉，而且网站兼容性问题最小。

[:octicons-home-16: 官网](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="隐私政策" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="文档" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="源代码" }

<details class="downloads" markdown>
<summary>下载</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Brave 在从 Brave 网站下载的文件名中添加了“[推荐代码](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)”，用于跟踪浏览器是从哪个来源下载的，例如在名为 `Brave-Browser-BRV002.pkg` 的下载中为 `BRV002`。然后，安装程序将在安装过程结束时使用推荐代码 ping Brave 的服务器。如果您对此感到担忧，可以在打开安装程序文件之前对其进行重命名。

</div>

### 推荐的 Brave 配置

这些选项可在 :material-menu: →**“设置”** 中找到。



#### Shields

Brave 在其 [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) 功能中包含一些反指纹措施。我们建议在您访问的所有页面中[全局](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings)配置这些选项。

Shields的选项可以根据需要在每个站点的基础上进行降级，但在默认情况下，我们建议设置以下内容。

<div class="annotate" markdown>

- [x] 在 *跟踪器和广告拦截* 下选择 **激进**

<details class="warning" markdown>
<summary>使用默认过滤列表</summary>

Brave 允许您在内部 `brave://adblock` 页面中选择其他内容过滤器。我们建议不要使用这个功能；相反，保留默认的过滤列表。使用额外的列表会使你从其他Brave用户中脱颖而出，如果Brave中存在漏洞，恶意规则被添加到你使用的列表中，也可能增加攻击面。

</details>

- [x] 在 *将连接升级到 HTTPS* 下选择 **严格**
- [x] （可选）选择 **阻止脚本** (1)
- [x] 选中 **阻止指纹识别**
- [x] 选择 **阻止第三方 cookie**
- [x] 选中 **关闭此网站时忘记我** (2)
- [ ] 取消选中所有社交媒体组件

</div>

1. 此选项禁用 JavaScript，这会破坏许多网站。要修复它们，您可以通过单击地址栏中的 Shield 图标并取消选中*高级控制*下的此设置来按网站设置例外情况。
2. 如果您希望在经常访问的特定网站上保持登录状态，可以通过单击地址栏中的 Shield 图标并取消选中*高级控制*下的此设置来按网站设置例外情况。



#### 隐私和安全

<div class="annotate" markdown>

- [x] 在 *安全* → *管理 JavaScript 优化和安全* (1) 下选择 **不允许网站使用 JavaScript 优化**
- [x] 在 *网站和 Shields 设置* 下选择 **自动从不使用的网站中删除权限**
- [x] 在 [*WebRTC IP 处理策略*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc) 下选择 **禁用非代理 UDP**
- [ ] 取消选中 **使用 Google 服务进行推送消息**
- [x] 选择 **自动重定向 AMP 页面**
- [x] 选择 **自动重定向跟踪 URL**
- [x] 选择 **防止网站根据我的语言偏好对我进行指纹识别**

</div>

1. 禁用 V8 优化器可通过禁用 JavaScript 即时 (JIT) 编译的[*某些*](https://grapheneos.social/@GrapheneOS/112708049232710156)部分来减少攻击面。



##### Tor 窗口

[**带有 Tor 的隐私窗口**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity)允许您在隐私窗口中通过 Tor 网络路由您的流量并访问 .onion 服务，这在某些情况下可能很有用。但是，Brave 的抗指纹能力**不如** Tor 浏览器，而且使用带有 Tor 的 Brave 的人要少得多，因此您会很显眼。如果您的威胁模型需要强匿名性，请使用 [Tor 浏览器](tor.md#tor-browser)。



##### 数据收集

- [ ] 取消选中**允许保护隐私的产品分析 (P3A)**
- [ ] 取消选中**自动向 Brave 发送每日使用情况 ping**
- [ ] 取消选中**自动发送诊断报告**



#### Web3

Brave 的 Web3 功能可能会增加您的浏览器指纹和攻击面。除非您使用这些功能中的任何一个，否则应将其禁用。

- 在 *默认以太坊钱包* 下选择 **扩展（无后备）**
- 在 *默认 Solana 钱包* 下选择 **扩展（无后备）**
- 在 *默认 Cardano 钱包* 下选择 **扩展（无后备）**



#### 扩展

- [ ] 取消选中所有您不使用的内置扩展



#### 搜索引擎

出于与建议在 [Firefox](#search) 中禁用此功能相同的原因，我们建议在 Brave 中禁用搜索建议。

- [ ] 取消勾选**“显示搜索建议”**



#### 系统

<div class="annotate" markdown>

- [ ] 取消选中 **关闭 Brave 后继续运行后台应用** 以禁用后台应用 (1)

</div>

1. 此选项并非在所有平台上都存在。



#### Brave 同步

[Brave 同步](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync)允许在您的所有设备上访问您的浏览数据（历史记录、书签等），而无需帐户，并使用端到端加密对其进行保护。



#### Brave 奖励和钱包

**Brave 奖励**让您可以通过在 Brave 中执行某些操作来接收基本注意力代币 (BAT) 加密货币。它依赖于托管帐户和来自少数选定提供商的 KYC。我们不推荐 BAT 作为[私人加密货币](cryptocurrency.md)，也不推荐使用[托管钱包](advanced/payments.md#wallet-custody)，因此我们不鼓励使用此功能。

**Brave 钱包**在您的计算机上本地运行，但不支持任何私人加密货币，因此我们也不鼓励使用此功能。



## 标准

**请注意，我们不隶属于我们推荐的任何项目。** 除了[我们的标准评估原则](about/criteria.md)之外，我们还制定了一套明确的要求，以使我们能够提供客观的建议。我们建议您在选择使用项目之前熟悉此列表，并自行研究以确保它是适合您的选择。



### 最低要求

- 它必须是开源软件。
- 必须支持自动更新。
- 必须在上游发布后 0-1 天内收到引擎更新。
- 必须在 Linux、macOS 和 Windows 上可用。
- 使浏览器更加尊重隐私所需的任何更改都不得对用户体验产生负面影响。
- 必须默认阻止第三方 cookie。
- 必须支持[状态分区](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning)以减轻跨站点跟踪。[^1]



### 最好情况

我们的最佳情况标准代表了我们希望从该类别的完美项目中看到的内容。我们的建议可能不包括任何或所有这些功能，但那些包含这些功能的项目在此页面上的排名可能高于其他项目。

- 应包含内置的内容拦截功能。
- 应支持 cookie 隔离（如 [多帐户容器](https://support.mozilla.org/kb/containers)）。
- 应支持渐进式 Web 应用程序 (PWA)。 PWA 使您能够安装某些网站，就像它们是您计算机上的本机应用程序一样。与安装基于 Electron 的应用程序相比，这可能具有优势，因为 PWA 受益于浏览器的定期安全更新。
- 不应包含不影响用户隐私的附加功能（膨胀软件）。
- 默认情况下不应收集遥测数据。
- 应提供开源同步服务器实现。
- 应默认使用[隐私的搜索引擎](search-engines.md)。



[^1]:    
    Brave 的实现在 [Brave 隐私更新：为隐私划分网络状态](https://brave.com/privacy-updates/14-partitioning-network-state) 中有详细说明。
