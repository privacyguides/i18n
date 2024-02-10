---
meta_title: "尊重隐私的 PC 和 Mac 网络浏览器 - Privacy Guides"
title: "电脑浏览器"
icon: material/laptop
description: 这些浏览器比 Google Chrome 浏览器提供更强的隐私保护。
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

这些是我们目前推荐的用于标准/非匿名浏览的桌面网络浏览器和配置。 如果你需要强大的隐私保护和开箱即用的防指纹功能，我们推荐 [Mullvad 浏览器](#mullvad-browser) ；如果你需要谷歌 Chrome 浏览器的良好替代品，我们推荐 [Firefox](#firefox) ；如果你需要 Chromium 浏览器的兼容性，我们推荐 [Brave](#brave)。

如果您需要匿名浏览互联网，则应使用 [Tor](tor.md) 。 我们在本页会提出一些配置建议，但除 Tor 浏览器之外的所有浏览器都可以通过 *某种方式* 追踪到。

## Mullvad 浏览器

<div class="admonition recommendation" markdown>

![Mullvad浏览器图标](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad 浏览器** 是 [Tor 浏览器](tor.md#tor-browser) 去除了 Tor 网络的一个版本，旨在为 VPN 用户提供 Tor 浏览器的反指纹浏览器技术。 它由 Tor 项目开发，由 [Mullvad](vpn.md#mullvad) 发布，**不需要** 使用 Mullvad 的 VPN。

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

与 [Tor Browser](tor.md)一样，Mullvad Browser 的设计也是通过使您的浏览器指纹与所有其他 Mullvad Browser 用户完全相来了防止指纹识别。它自带了默认设置和扩展程序，这些会由设置的安全级别自动配置： *标准*, *更安全* 和 *最安全*。 因此，在调整自带的 [安全级别](https://tb-manual.torproject.org/security-settings/) 之外，请务必不要对浏览器进行任何修改。 其他修改会使您的指纹变得独一无二，从而失去使用该浏览器的意义。 如果你想对浏览器进行更多的配置而且不担心指纹识别，我们建议你使用 [Firefox](#firefox)。

### 防指纹

在**不使用** [VPN](vpn.md)的情况下，Mullvad 浏览器提供的对 [天真的指纹脚本](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) 的保护与其他隐私浏览器（如 Firefox+[Arkenfox](#arkenfox-advanced) 或 [Brave](#brave)）相同。 Mullvad 浏览器自带这些保护，但牺牲了其他隐私浏览器提供的一些灵活性和便利性。

==为了最完善的反指纹保护，我们建议将 Mullvad 浏览器与 **和** VPN== 结合使用，无论是 Mullvad 还是其他推荐的 VPN 提供商。 在使用 Mullvad 浏览器的 VPN 时，你将与许多其他用户共享一个指纹和一个 IP 地址池，使你混入“人群”。 这种策略是挫败进阶跟踪脚本的唯一方法，与 Tor 浏览器使用的反指纹技术相同。

请注意，虽然您可以和任何 VPN 提供商一起使用 Mullvad 浏览器，但该 VPN 上的其他人也必须使用 Mullvad 浏览器才会有“人群”存在。与其他提供商相比，Mullvad VPN 更有可能保证这种情况，尤其是在 Mullvad 浏览器刚刚发布的当下。 Mullvad 浏览器没有内置 VPN 连接，也不会在浏览前检查你是否在使用 VPN；你的 VPN 连接必须单独配置和管理。

Mullvad 浏览器预装了 *uBlock Origin* 和 *NoScript* 浏览器扩展程序。 虽然我们通常 [不建议](#extensions) 添加 *额外的* 浏览器扩展程序，但浏览器预装的这些扩展 程序**不应** 删除或配置为默认之外的设置，因为这样做会使您的浏览器指纹明显有别于其他 Mullvad 浏览器用户。 它还预装了 Mullvad 浏览器扩展程序，这个拓展程序*可以* 安全地移除，不会影响你的浏览器指纹，但即使你不使用 Mullvad VPN，保留它也不会有问题。

### 无痕模式

Mullvad 浏览器一直在无痕浏览模式下运行，这意味着每次关闭浏览器时，你的历史记录、cookies 和其他网站数据都会被清除。 您的书签、浏览器设置和扩展程序设置会被保留。

这是防止深度跟踪的必要条件，但确实牺牲了一些便利性和一些 Firefox 的功能（如多账户容器）。 当然，您可以同时使用多种浏览器，例如，您可以考虑使用 Firefox+Arkenfox 浏览一些需要保持登录状态或在 Mullvad 浏览器中无法正常运行的网站，并使用 Mullvad 浏览器进行一般浏览。

### Mullvad Leta

Mullvad 浏览器将 DuckDuckGo 设置为默认的 [搜索引擎](search-engines.md)，但它也预装了 **Mullvad Leta**，这是一个需要订阅 Mullvad VPN 才能访问的搜索引擎。 Mullvad Leta 直接查询谷歌的付费搜索 API（这是它仅限于付费用户的原因），但因为这种限制的存在，Mullvad 有可能将搜索查询与 Mullvad VPN 账户进行关联。 因此，我们不建议使用 Mullvad Leta，虽然 Mullvad 对 VPN 用户信息收集得很少。

## Firefox（火狐浏览器）

<div class="admonition recommendation" markdown>

![火狐标志](assets/img/browsers/firefox.svg){ align=right }

**火狐浏览器**提供强大的隐私设置，如[增强型跟踪保护](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop)，它可以帮助阻止各种[类型的跟踪](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks)。

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.mozilla.org/privacy/firefox/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://firefox-source-docs.mozilla.org/){ .card-link title=Documentation}
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org/){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://www.mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://www.mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://www.mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Firefox includes a unique [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) in downloads from Mozilla's website and uses telemetry in Firefox to send the token. The token is **not** included in releases from the [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### 推荐配置

这些选项可以在 :material-menu: → **设置**中找到。

#### 搜索

- [ ] 取消勾选 **提供搜索建议**

搜索建议功能可能在你的地区无法使用。

搜索建议将你在地址栏中输入的所有内容发送到默认的搜索引擎，而不管你是否提交了实际的搜索。 禁用搜索建议可以让你更精确地控制你向搜索引擎供应商发送的数据。

#### 隐私与安全

##### 增强跟踪保护

- [x] 选择 **严格的** 增强跟踪保护

这可以通过阻止社交媒体追踪器、指纹脚本（注意，这并不能保护你 *所有* 指纹）、加密器、跨网站追踪cookies和其他一些追踪内容来保护你。 ETP可以防止许多常见的威胁，但它并不阻止所有的跟踪途径，因为它的设计对网站的可用性影响最小甚至没有影响。

##### Firefox Suggest (仅限美国)

[Firefox Suggest](https://support.mozilla.org/en-US/kb/firefox-suggest) 是一项仅在美国可用的类似于搜索建议的功能。 我们建议禁用这个功能，原因与我们建议禁用搜索建议的原因相同。 如果在 **地址栏** 标题下没有看到这些选项，则表示您没有获得这个功能，可以忽略这些设置。

- [ ] 取消选中 **来自网络的建议**
- [ ] 取消选中 **来自赞助商的建议**

##### 关闭时消毒

如果你想在特定的网站上保持登录状态，你可以在 **Cookies和网站数据** → **管理例外情况中允许例外。**

- [x] 勾选 **当Firefox关闭时，删除cookies和网站数据**

这可以保护您免受持久性cookies的影响，但不能保护您免受在任何一个浏览会话中获得的cookies的影响。 启用该功能后，只需重新启动火狐浏览器，就可以轻松清理浏览器的cookies。 如果你希望在你经常访问的特定网站上保持登录状态，你可以在每个网站的基础上设置例外。

##### 遥测

- [ ] 取消勾选 **允许火狐浏览器向Mozilla发送技术和互动数据**
- [ ] 取消勾选 **允许Firefox安装和运行研究**
- [ ] 取消勾选 **允许火狐代表您发送积压的崩溃报告**

> 火狐浏览器会向我们发送有关您的火狐浏览器版本和语言、设备操作系统和硬件配置、内存、有关崩溃和错误的基本信息以及更新、安全浏览和激活等自动处理结果的数据。 当火狐浏览器向我们发送数据时，您的IP地址会被暂时收集，作为我们服务器日志的一部分。

此外，火狐账户服务还收集 [一些技术数据](https://www.mozilla.org/en-US/privacy/firefox/#firefox-accounts)。 如果你使用Firefox账户，你可以选择退出。

1. 在 accounts.firefox.com</a>上打开你的
配置文件设置。</li> 
   
   2 取消勾选 **数据收集和使用** > **帮助改进火狐账户**</ol> 



##### HTTPS-Only 模式

- [x] 选择 **启用所有窗口的纯HTTPS-Only模式**

这可以防止你无意中以纯文本的HTTP方式连接到一个网站。 现在没有HTTPS的网站已经不多见了，所以这对你的日常浏览应该没有什么影响。



##### DNS over HTTPS

如果您使用一个 [DNS over HTTPS 提供商](dns.md)：

- [x] 选择 **最强保护** 并选择一个合适的提供商

最强保护会强制使用 DoH ，如果 Firefox 无法连接到您的 DoH 服务器或者无法解析当前的域名会显示安全警告。 这将避免您所连接的网络秘密地降低您的 DNS 安全性。



#### 同步

[火狐浏览器同步](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) ，使您的浏览数据（历史记录、书签等）可以在您的所有设备上访问，并通过E2EE进行保护。



### Arkenfox (advanced)

<div class="admonition tip" markdown>
<p class="admonition-title">Use Mullvad Browser for advanced anti-fingerprinting</p>

[Mullvad Browser](#mullvad-browser) provides the same anti-fingerprinting protections as Arkenfox out of the box, and does not require the use of Mullvad's VPN to benefit from these protections. Coupled with a VPN, Mullvad Browser can thwart more advanced tracking scripts which Arkenfox cannot. Arkenfox still has the advantage of being much more flexible, and allowing per-site exceptions for websites which you need to stay logged in to.

</div>

[Arkenfox项目](https://github.com/arkenfox/user.js) ，为Firefox提供了一套精心考虑的选项。 如果你 [决定](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) 使用Arkenfox，有几个 [选项](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) 是主观严格的和/或可能导致一些网站不能正常工作-- [，你可以很容易地改变](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) 以满足你的需要。 我们 **，强烈建议** ，阅读其完整的 [wiki](https://github.com/arkenfox/user.js/wiki)。 Arkenfox还能支持 [容器](https://support.mozilla.org/en-US/kb/containers#w_for-advanced-users)。

Arkenfox 的目标只是通过 canvas 随机化和 Firefox 内置的抗指纹配置设置来挫败基本的或幼稚的跟踪脚本。 它不会像 Mullvad 浏览器或 Tor 浏览器那样，让你的浏览器与一大群其他用户融为一体，所以不会阻挡进阶的指纹跟踪脚本。 当然，您可以同时使用多种浏览器，例如，您可以考虑使用 Firefox+Arkenfox 浏览一些需要保持登录状态或着您信任的网站，并使用 Mullvad 浏览器进行一般浏览。



## Brave

<div class="admonition recommendation annotate" markdown>

![Brave标识](assets/img/browsers/brave.svg){ align=right }

**Brave浏览器**包括一个内置的内容拦截器和[隐私功能](https://brave.com/privacy-features/)，其中许多功能都是默认启用的。

Brave是建立在Chromium网络浏览器项目之上的，所以它应该有熟悉的感觉，而且网站兼容性问题最小。

[:octicons-home-16: Homepage](https://brave.com/){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-windows11: Windows](https://brave.com/download/)
- [:simple-apple: macOS](https://brave.com/download/)
- [:simple-linux: Linux](https://brave.com/linux/) (1)

</details>

</div>

1. 我们建议不要使用Flatpak版本的Brave，因为它用Flatpak的沙箱代替了Chromium的沙箱，效果较差。 此外，该软件包并非由Brave Software, Inc.维护。

**macOS users:** The download for Brave Browser from their official website is a `.pkg` installer which requires admin privileges to run (and may run other unnecessary scripts on your machine). As an alternative, you can download the latest `Brave-Browser-universal.dmg` file from their [GitHub releases](https://github.com/brave/brave-browser/releases/latest) page, which provides a traditional "drag to Applications folder" install.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Brave adds a "[referral code](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" to the file name in downloads from the Brave website, which is used to track which source the browser was downloaded from, for example `BRV002` in a download named `Brave-Browser-BRV002.pkg`. The installer will then ping Brave's server with the referral code at the end of the installation process. If you're concerned about this, you can rename the installer file before opening it.

</div>

### 推荐配置

这些选项可以在 :material-menu: → **设置**中找到。



#### Settings



##### 盾

Brave在其 [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-) 功能中包括一些防指纹的措施。 我们建议将这些选项配置为 [，在你访问的所有页面上全局](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-)。

Shields的选项可以根据需要在每个站点的基础上进行降级，但在默认情况下，我们建议设置以下内容。

<div class="annotate" markdown>

- [x] Select **Prevent sites from fingerprinting me based on my language preferences**
- [x] Select **Aggressive** under Trackers & ads blocking

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. 我们建议不要使用这个功能；相反，保留默认的过滤列表。 使用额外的列表会使你从其他Brave用户中脱颖而出，如果Brave中存在漏洞，恶意规则被添加到你使用的列表中，也可能增加攻击面。

</details>

- [x] Select **Strict** under **Upgrade connections to HTTPS**
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Strict, may break sites** under Block fingerprinting
- [x] Check **Forget me when I close this site** (2)

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net/) extension.
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar.



##### 社交媒体图标

- [ ] 取消勾选所有社交媒体组件



##### 隐私和安全

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP Handling Policy](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Private window with Tor** (1)

</div>

1. Brave 对指纹的抵抗力**不如** Tor 浏览器，而且使用 Brave 的 Tor 功能的人要少得多，所以你的指纹会突出。 在 [需要强大的匿名性的地方](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-) ，使用 [Tor 浏览器](tor.md#tor-browser)。

<div class="admonition tip" markdown>
<p class="admonition-title">Sanitizing on close</p>

- [x] Select **Clear cookies and site data when you close all windows** in the *Cookies and other site data* menu

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

##### 扩展程序

在 **Extensions**，禁用你不使用的内置扩展程序。

- [ ] 取消勾选 **Hangouts**
- [ ] 取消勾选 **WebTorrent**



##### Web3

Brave 的 Web3 功能可能会增加浏览器指纹和攻击面。 如果您不使用这些功能，应将其禁用。

- Select **Extensions (no fallback)** under Default Ethereum wallet and Default Solana wallet
- Set **Method to resolve IPFS resources** to **Disabled**



##### 系统

<div class="annotate" markdown>

- [ ] Uncheck **Continue running apps when Brave is closed** to disable background apps (1)

</div>

1. This option is not present on all platforms.



#### 同步

[Brave 同步](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) 允许你的浏览数据（历史记录、书签等）在你所有的设备上访问，而不需要账户，并以E2EE进行保护。



#### Brave Rewards and Wallet

**Brave Rewards** lets you recieve Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#other-coins-bitcoin-ethereum-etc), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.



## 其它资源

In general, we recommend keeping your browser extensions to a minimum to decrease your attack surface; they have privileged access within your browser, require you to trust the developer, can make you [stand out](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), and [weaken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) site isolation. However, uBlock Origin may prove useful if you value content blocking functionality.



### uBlock Origin

<div class="admonition recommendation" markdown>

![uBlock Origin标识](assets/img/browsers/ublock_origin.svg){ align=right }

**uBlock Origin**是一个流行的内容阻止器，可以帮助你阻止广告、跟踪器和指纹脚本。

[:octicons-repo-16: Repository](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

</details>

</div>

We suggest following the [developer's documentation](https://github.com/gorhill/uBlock/wiki/Blocking-mode) and picking one of the "modes". Additional filter lists can impact performance and [may increase attack surface](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

These are some other [filter lists](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) that you may want to consider adding:

- [x] Check **Privacy** > **AdGuard URL Tracking Protection**
- Add [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)



### uBlock Origin Lite

uBlock Origin also has a "Lite" version of their extension, which offers a very limited feature-set compared to the original extension. However, it has a few distinct advantages over its full-fledged sibling, so you may want to consider it if...

- ...you don't want to grant full "read/modify website data" permissions to any extensions (even a trusted one like uBlock Origin)
- ...you want a more resource (memory/CPU) efficient content blocker[^1]
- ...your browser only supports Manifest V3 extensions

<div class="admonition recommendation" markdown>

![uBlock Origin Lite logo](assets/img/browsers/ublock_origin_lite.svg){ align=right }

**uBlock Origin Lite** is a Manifest V3 compatible content blocker. Compared to the original *uBlock Origin*, this extension does not require broad "read/modify data" permissions to function.

[:octicons-repo-16: Repository](https://github.com/uBlockOrigin/uBOL-home#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/uBlockOrigin/uBOL-home/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/gorhill/uBlock/tree/master/platform/mv3){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/addon/ublock-origin-lite/)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin-lite/ddkjiahejlhfcafbddmgiahcphecmpfh)

</details>

</div>

We only recommend this version of uBlock Origin if you never want to make any changes to your filter lists, because it only supports a few pre-selected lists and offers no additional customization options, including the ability to select elements to block manually. These restrictions are due to limitations in Manifest V3's design.

This version offers three levels of blocking: "Basic" works without requiring any special privileges to view and modify site content, while the "Optimal" and "Complete" levels do require that broad permission, but offer a better filtering experience with additional cosmetic rules and scriptlet injections.

If you set the default filtering mode to "Optimal" or "Complete" the extension will request read/modify access to **all** websites you visit. However, you also have the option to change the setting to "Optimal" or "Complete" on a **per-site** basis by adjusting the slider in the extension's pop-up panel on any given site. When you do so, the extension will request read/modify access to that site only. Therefore, if you want to take advantage of uBlock Origin Lite's "permission-less" configuration, you should probably leave the default setting as "Basic" and only adjust it higher on sites where that level is not adequate.

uBlock Origin Lite only receives block list updates whenever the extension is updated from your browser's extension marketplace, as opposed to on demand. This means that you may miss out on new threats being blocked for weeks until a full extension release is published.



## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

We are working on establishing defined criteria for every section of our site, and this may be subject to change. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. There are many factors considered and discussed when we recommend a project, and documenting every single one is a work-in-progress.

</div>

### 最低要求

- 它必须是开源软件。
- 支持自动更新。
- 在上游发布后0-1天内收到引擎更新。
- 可用于Linux、macOS和Windows。
- 为使浏览器更加尊重隐私所需的任何改变都不应该对用户体验产生负面影响。
- 默认情况下阻止第三方的cookies。
- Supports [state partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^2]



### 最好情况

我们的最佳情况代表了我们希望从这个类别中的完美项目中看到的东西。 我们的推荐可能不包括任何或所有这些功能，但那些包含这些功能的推荐可能比本页面上的其他推荐排名更高。

- 包括内置的内容拦截功能。
- Supports cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/en-US/kb/containers)).
- Supports Progressive Web Apps. PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps, because you benefit from your browser's regular security updates.

- 不包括不增强用户隐私的累赘功能。

- 默认情况下不收集遥测数据。
- 提供开源的同步服务器实现。
- 默认为[隐私搜索引擎](search-engines.md)。



### 扩展标准

- 不得复制内置浏览器或操作系统的功能。
- 必须直接影响用户隐私，即不能简单地提供信息。



[^1]:    
    uBlock Origin Lite *itself* will consume no resources, because it uses newer APIs which make the browser process the filter lists natively, instead of running JavaScript code within the extension to handle the filtering. However, this resource advantage is only [theoretical](https://github.com/uBlockOrigin/uBOL-home/wiki/Frequently-asked-questions-(FAQ)#is-ubol-more-efficient-cpu--and-memory-wise-than-ubo), because it's possible that standard uBlock Origin's filtering code is more efficient than your browser's native filtering code. This has not yet been benchmarked.


[^2]:    
    Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state/).
