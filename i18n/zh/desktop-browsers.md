---
meta_title: "尊重隐私的 PC 和 Mac 网络浏览器 - Privacy Guides"
title: "电脑浏览器"
icon: material/laptop
description: These privacy-protecting browsers are what we currently recommend for standard/non-anonymous internet browsing on desktop systems.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: 隐私桌面浏览器建议
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

<small>Protects against the following threat(s):</small>

- [:material-account-cash: 监视资本主义](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our currently recommended **desktop web browsers** and configurations for standard/non-anonymous browsing. 如果你需要强大的隐私保护和开箱即用的防指纹功能，我们推荐 [Mullvad 浏览器](#mullvad-browser) ；如果你需要谷歌 Chrome 浏览器的良好替代品，我们推荐 [Firefox](#firefox) ；如果你需要 Chromium 浏览器的兼容性，我们推荐 [Brave](#brave)。

如果您需要匿名浏览互联网，则应使用 [Tor](tor.md) 。 我们在本页会提出一些配置建议，但除 Tor 浏览器之外的所有浏览器都可以通过 *某种方式* 追踪到。

## Mullvad 浏览器

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** is a version of [Tor Browser](tor.md#tor-browser) with Tor network integrations removed. It aims to provide to VPN users Tor Browser's anti-fingerprinting browser technologies, which are key protections against [:material-eye-outline: Mass Surveillance](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. 它由 Tor 项目开发，由 [Mullvad](vpn.md#mullvad) 发布，**不需要** 使用 Mullvad 的 VPN。

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

与 [Tor Browser](tor.md)一样，Mullvad Browser 的设计也是通过使您的浏览器指纹与所有其他 Mullvad Browser 用户完全相来了防止指纹识别。它自带了默认设置和扩展程序，这些会由设置的安全级别自动配置： *标准*, *更安全* 和 *最安全*。 Therefore, it is imperative that you do not modify the browser at all outside adjusting the default [security levels](https://tb-manual.torproject.org/security-settings). 其他修改会使您的指纹变得独一无二，从而失去使用该浏览器的意义。 如果你想对浏览器进行更多的配置而且不担心指纹识别，我们建议你使用 [Firefox](#firefox)。

### 防指纹

在**不使用** [VPN](vpn.md)的情况下，Mullvad 浏览器提供的对 [天真的指纹脚本](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) 的保护与其他隐私浏览器（如 Firefox+[Arkenfox](#arkenfox-advanced) 或 [Brave](#brave)）相同。 Mullvad 浏览器自带这些保护，但牺牲了其他隐私浏览器提供的一些灵活性和便利性。

==为了最完善的反指纹保护，我们建议将 Mullvad 浏览器与 **和** VPN== 结合使用，无论是 Mullvad 还是其他推荐的 VPN 提供商。 在使用 Mullvad 浏览器的 VPN 时，你将与许多其他用户共享一个指纹和一个 IP 地址池，使你混入“人群”。 这种策略是挫败进阶跟踪脚本的唯一方法，与 Tor 浏览器使用的反指纹技术相同。

请注意，虽然您可以和任何 VPN 提供商一起使用 Mullvad 浏览器，但该 VPN 上的其他人也必须使用 Mullvad 浏览器才会有“人群”存在。与其他提供商相比，Mullvad VPN 更有可能保证这种情况，尤其是在 Mullvad 浏览器刚刚发布的当下。 Mullvad 浏览器没有内置 VPN 连接，也不会在浏览前检查你是否在使用 VPN；你的 VPN 连接必须单独配置和管理。

Mullvad 浏览器预装了 *uBlock Origin* 和 *NoScript* 浏览器扩展程序。 While we typically discourage adding *additional* [browser extensions](browser-extensions.md), these extensions that come pre-installed with the browser should **not** be removed or configured outside their default values, because doing so would noticeably make your browser fingerprint distinct from other Mullvad Browser users. 它还预装了 Mullvad 浏览器扩展程序，这个拓展程序*可以* 安全地移除，不会影响你的浏览器指纹，但即使你不使用 Mullvad VPN，保留它也不会有问题。

### 无痕模式

Mullvad 浏览器一直在无痕浏览模式下运行，这意味着每次关闭浏览器时，你的历史记录、cookies 和其他网站数据都会被清除。 您的书签、浏览器设置和扩展程序设置会被保留。

这是防止深度跟踪的必要条件，但确实牺牲了一些便利性和一些 Firefox 的功能（如多账户容器）。 当然，您可以同时使用多种浏览器，例如，您可以考虑使用 Firefox+Arkenfox 浏览一些需要保持登录状态或在 Mullvad 浏览器中无法正常运行的网站，并使用 Mullvad 浏览器进行一般浏览。

### Mullvad Leta

Mullvad Browser comes with DuckDuckGo set as the default [search engine](search-engines.md), but it also comes pre-installed with **Mullvad Leta**, a search engine which requires an active Mullvad VPN subscription to access. Mullvad Leta queries Google's paid search API directly, which is why it is limited to paying subscribers. However, it is possible for Mullvad to correlate search queries and Mullvad VPN accounts because of this limitation. 因此，我们不建议使用 Mullvad Leta，虽然 Mullvad 对 VPN 用户信息收集得很少。

## Firefox（火狐浏览器）

<div class="admonition recommendation" markdown>

![火狐标志](assets/img/browsers/firefox.svg){ align=right }

**火狐浏览器**提供强大的隐私设置，如[增强型跟踪保护](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop)，它可以帮助阻止各种[类型的跟踪](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks)。

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="Documentation" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Firefox includes a unique [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) in downloads from Mozilla's website and uses telemetry in Firefox to send the token. The token is **not** included in releases from the [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Recommended Firefox Configuration

这些选项可以在 :material-menu: → **设置**中找到。

#### 搜索

- [ ] Uncheck **Show search suggestions**

搜索建议功能可能在你的地区无法使用。

搜索建议将你在地址栏中输入的所有内容发送到默认的搜索引擎，而不管你是否提交了实际的搜索。 禁用搜索建议可以让你更精确地控制你向搜索引擎供应商发送的数据。

##### Firefox Suggest (仅限美国)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. 我们建议禁用这个功能，原因与我们建议禁用搜索建议的原因相同。 如果在 **地址栏** 标题下没有看到这些选项，则表示您没有获得这个功能，可以忽略这些设置。

- [ ] Uncheck **Suggestions from Firefox**
- [ ] 取消选中 **来自赞助商的建议**

#### 隐私与安全

##### 增强跟踪保护

- [x] 选择 **严格的** 增强跟踪保护

这可以通过阻止社交媒体追踪器、指纹脚本（注意，这并不能保护你 *所有* 指纹）、加密器、跨网站追踪cookies和其他一些追踪内容来保护你。 ETP可以防止许多常见的威胁，但它并不阻止所有的跟踪途径，因为它的设计对网站的可用性影响最小甚至没有影响。

##### 关闭时消毒

如果你想在特定的网站上保持登录状态，你可以在 **Cookies和网站数据** → **管理例外情况中允许例外。**

- [x] 勾选 **当Firefox关闭时，删除cookies和网站数据**

这可以保护您免受持久性cookies的影响，但不能保护您免受在任何一个浏览会话中获得的cookies的影响。 启用该功能后，只需重新启动火狐浏览器，就可以轻松清理浏览器的cookies。 如果你希望在你经常访问的特定网站上保持登录状态，你可以在每个网站的基础上设置例外。

##### Telemetry

- [ ] 取消勾选 **允许火狐浏览器向Mozilla发送技术和互动数据**
- [ ] 取消勾选 **允许Firefox安装和运行研究**
- [ ] 取消勾选 **允许火狐代表您发送积压的崩溃报告**

According to Mozilla's privacy policy for Firefox,

> 火狐浏览器会向我们发送有关您的火狐浏览器版本和语言、设备操作系统和硬件配置、内存、有关崩溃和错误的基本信息以及更新、安全浏览和激活等自动处理结果的数据。 当火狐浏览器向我们发送数据时，您的IP地址会被暂时收集，作为我们服务器日志的一部分。

Additionally, the Mozilla Accounts service collects [some technical data](https://mozilla.org/privacy/mozilla-accounts). If you use a Mozilla Account you can opt out:

1. 在 accounts.firefox.com</a>上打开你的

配置文件设置。</li> 
   
   2 取消勾选 **数据收集和使用** > **帮助改进火狐账户**</ol> 



##### Website Advertising Preferences

- [ ] Uncheck **Allow websites to perform privacy-preserving ad measurement**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.



##### HTTPS-Only Mode

- [x] 选择 **启用所有窗口的纯HTTPS-Only模式**

这可以防止你无意中以纯文本的HTTP方式连接到一个网站。 Sites without HTTPS are uncommon nowadays, so this should have little to no impact on your day-to-day browsing.



##### DNS over HTTPS

如果您使用一个 [DNS over HTTPS 提供商](dns.md)：

- [x] 选择 **最强保护** 并选择一个合适的提供商

最强保护会强制使用 DoH ，如果 Firefox 无法连接到您的 DoH 服务器或者无法解析当前的域名会显示安全警告。 这将避免您所连接的网络秘密地降低您的 DNS 安全性。



#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.



### Arkenfox (advanced)

<div class="admonition tip" markdown>
<p class="admonition-title">Use Mullvad Browser for advanced anti-fingerprinting</p>

[Mullvad Browser](#mullvad-browser) provides the same anti-fingerprinting protections as Arkenfox out of the box, and does not require the use of Mullvad's VPN to benefit from these protections. Coupled with a VPN, Mullvad Browser can thwart more advanced tracking scripts which Arkenfox cannot. Arkenfox still has the advantage of being much more flexible, and allowing per-site exceptions for websites which you need to stay logged in to.

</div>

[Arkenfox项目](https://github.com/arkenfox/user.js) ，为Firefox提供了一套精心考虑的选项。 If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly—which you can [easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. 我们 **，强烈建议** ，阅读其完整的 [wiki](https://github.com/arkenfox/user.js/wiki)。 Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox 的目标只是通过 canvas 随机化和 Firefox 内置的抗指纹配置设置来挫败基本的或幼稚的跟踪脚本。 它不会像 Mullvad 浏览器或 Tor 浏览器那样，让你的浏览器与一大群其他用户融为一体，所以不会阻挡进阶的指纹跟踪脚本。 Remember that you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.



## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave是建立在Chromium网络浏览器项目之上的，所以它应该有熟悉的感觉，而且网站兼容性问题最小。

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Brave adds a "[referral code](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" to the file name in downloads from the Brave website, which is used to track which source the browser was downloaded from, for example `BRV002` in a download named `Brave-Browser-BRV002.pkg`. The installer will then ping Brave's server with the referral code at the end of the installation process. If you're concerned about this, you can rename the installer file before opening it.

</div>

### Recommended Brave Configuration

这些选项可以在 :material-menu: → **设置**中找到。



#### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

Shields的选项可以根据需要在每个站点的基础上进行降级，但在默认情况下，我们建议设置以下内容。

<div class="annotate" markdown>

- [x] Select **Aggressive** under *Trackers & ads blocking*

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. 我们建议不要使用这个功能；相反，保留默认的过滤列表。 使用额外的列表会使你从其他Brave用户中脱颖而出，如果Brave中存在漏洞，恶意规则被添加到你使用的列表中，也可能增加攻击面。

</details>

- [x] Select **Strict** under *Upgrade connections to HTTPS*
- [x] (Optional) Select **Block Scripts** (1)
- [x] Check **Block fingerprinting**
- [x] Select **Block third-party cookies**
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option disables JavaScript, which will break a lot of sites. To fix them, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.



#### Privacy and security

<div class="annotate" markdown>

- [x] Select **Don't allow sites to use the V8 optimizer** under *Security* → *Manage V8 security* (1)
- [x] Select **Automatically remove permissions from unused sites** under *Sites and Shields Settings*
- [x] Select **Disable non-proxied UDP** under [*WebRTC IP Handling Policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **Prevent sites from fingerprinting me based on my language preferences**

</div>

1. Disabling the V8 optimizer reduces your attack surface by disabling [*some*](https://grapheneos.social/@GrapheneOS/112708049232710156) parts of JavaScript Just-In-Time (JIT) compilation.

<div class="admonition tip" markdown>
<p class="admonition-title">Sanitizing on close</p>

- [x] Select **Delete data sites have saved to your device when you close all windows** under *Sites and Shields Settings* → *Content* → *Additional content settings* → *On-device site data*.

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

##### Tor windows

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) allows you to route your traffic through the Tor network in Private Windows and access .onion services, which may be useful in some cases. However, Brave is **not** as resistant to fingerprinting as the Tor Browser is, and far fewer people use Brave with Tor, so you will stand out. If your threat model requires strong anonymity, use the [Tor Browser](tor.md#tor-browser).



##### Data Collection

- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**



#### Web3

Brave 的 Web3 功能可能会增加浏览器指纹和攻击面。 Unless you use any of these features, they should be disabled.

- Select **Extensions (no fallback)** under *Default Ethereum wallet*
- Select **Extensions (no fallback)** under *Default Solana wallet*



#### Extensions

- [ ] Uncheck all built-in extensions you don't use



#### Search engine

We recommend disabling search suggestions in Brave for the same reason we recommend disabling this feature in [Firefox](#search).

- [ ] Uncheck **Show search suggestions**



#### System

<div class="annotate" markdown>

- [ ] Uncheck **Continue running apps when Brave is closed** to disable background apps (1)

</div>

1. This option is not present on all platforms.



#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.



#### Brave Rewards and Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.



## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.



### 最低要求

- 它必须是开源软件。
- Must support automatic updates.
- Must receive engine updates in 0-1 days from upstream release.
- Must be available on Linux, macOS, and Windows.
- Any changes required to make the browser more privacy-respecting must not negatively impact user experience.
- Must block third-party cookies by default.
- Must support [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]



### 最好情况

我们的最佳情况代表了我们希望从这个类别中的完美项目中看到的东西。 我们的推荐可能不包括任何或所有这些功能，但那些包含这些功能的推荐可能比本页面上的其他推荐排名更高。

- Should include built-in content blocking functionality.
- Should support cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Should support Progressive Web Apps (PWAs). PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps because PWAs benefit from your browser's regular security updates.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Should not collect telemetry by default.
- Should provide an open-source sync server implementation.
- Should default to a [private search engine](search-engines.md).



[^1]:    
    Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
