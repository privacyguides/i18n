---
meta_title: "Privacy Respecting Web Browsers for PC and Mac - Privacy Guides"
title: "电脑浏览器"
icon: material/laptop
description: These web browsers provide stronger privacy protections than Google Chrome.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Private Desktop Browser Recommendations
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

这些是我们目前推荐的用于标准/非匿名浏览的桌面网络浏览器和配置。 We recommend [Mullvad Browser](#mullvad-browser) if you are focused on strong privacy protections and anti-fingerprinting out of the box, [Firefox](#firefox) for casual internet browsers looking for a good alternative to Google Chrome, and [Brave](#brave) if you need Chromium browser compatibility.

如果您需要匿名浏览互联网，则应使用 [Tor](tor.md) 。 We make some configuration recommendations on this page, but all browsers other than Tor Browser will be traceable by *somebody* in some manner or another.

## Mullvad Browser

!!! recommendation

    ![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    **Mullvad Browser** is a version of [Tor Browser](tor.md#tor-browser) with Tor network integrations removed, aimed at providing Tor Browser's anti-fingerprinting browser technologies to VPN users. It is developed by the Tor Project and distributed by [Mullvad](vpn.md#mullvad), and does **not** require the use of Mullvad's VPN.
    
    [:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

Like [Tor Browser](tor.md), Mullvad Browser is designed to prevent fingerprinting by making your browser fingerprint identical to all other Mullvad Browser users, and it includes default settings and extensions that are automatically configured by the default security levels: *Standard*, *Safer* and *Safest*. Therefore, it is imperative that you do not modify the browser at all outside adjusting the default [security levels](https://tb-manual.torproject.org/security-settings/). Other modifications would make your fingerprint unique, defeating the purpose of using this browser. If you want to configure your browser more heavily and fingerprinting is not a concern for you, we recommend [Firefox](#firefox) instead.

### Anti-Fingerprinting

**Without** using a [VPN](vpn.md), Mullvad Browser provides the same protections against [naive fingerprinting scripts](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) as other private browsers like Firefox+[Arkenfox](#arkenfox-advanced) or [Brave](#brave). Mullvad Browser provides these protections out of the box, at the expense of some flexibility and convenience that other private browsers can provide.

==For the strongest anti-fingerprinting protection, we recommend using Mullvad Browser in conjunction **with** a VPN==, whether that is Mullvad or another recommended VPN provider. When using a VPN with Mullvad Browser, you will share a fingerprint and a pool of IP addresses with many other users, giving you a "crowd" to blend in with. This strategy is the only way to thwart advanced tracking scripts, and is the same anti-fingerprinting technique used by Tor Browser.

Note that while you can use Mullvad Browser with any VPN provider, other people on that VPN must also be using Mullvad Browser for this "crowd" to exist, something which is more likely on Mullvad VPN compared to other providers, particularly this close to the launch of Mullvad Browser. Mullvad Browser does not have built-in VPN connectivity, nor does it check whether you are using a VPN before browsing; your VPN connection has to be configured and managed separately.

Mullvad Browser comes with the *uBlock Origin* and *NoScript* browser extensions pre-installed. While we typically [don't recommend](#extensions) adding *additional* browser extensions, these extensions that come pre-installed with the browser should **not** be removed or configured outside their default values, because doing so would noticeably make your browser fingerprint distinct from other Mullvad Browser users. It also comes pre-installed with the Mullvad Browser Extension, which *can* be safely removed without impacting your browser fingerprint if you would like, but is also safe to keep even if you don't use Mullvad VPN.

### Private Browsing Mode

Mullvad Browser operates in permanent private browsing mode, meaning your history, cookies, and other site data will always be cleared every time the browser is closed. Your bookmarks, browser settings, and extension settings will still be preserved.

This is required to prevent advanced forms of tracking, but does come at the cost of convenience and some Firefox features, such as Multi-Account Containers. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise don't work properly in Mullvad Browser, and Mullvad Browser for general browsing.

### Mullvad Leta

Mullvad 浏览器将 DuckDuckGo 设置为默认的 [搜索引擎](search-engines.md)，但它也预装了 **Mullvad Leta**，这是一个需要订阅 Mullvad VPN 才能访问的搜索引擎。 Mullvad Leta 直接查询谷歌的付费搜索 API（这是它仅限于付费用户的原因），但因为这种限制的存在，Mullvad 有可能将搜索查询与 Mullvad VPN 账户进行关联。 因此，我们不建议使用 Mullvad Leta，虽然 Mullvad 对 VPN 用户信息收集得很少。

## Firefox（火狐浏览器）

!!! recommendation

    ![火狐标志](assets/img/browsers/firefox.svg){ align=right }
    
    **火狐浏览器**提供强大的隐私设置，如[增强型跟踪保护](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop)，它可以帮助阻止各种[类型的跟踪](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks)。
    
    [:octicons-home-16: 主页](https://firefox.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mozilla.org/privacy/firefox/){ .card-link title="隐私政策" }
    [:octicons-info-16:](https://firefox-source-docs.mozilla.org/){ .card-link title=文档}
    [:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="源代码" }
    [:octicons-heart-16:](https://donate.mozilla.org/){ .card-link title="贡献" }
    
    ??? 下载
    
        - [:simple-windows11: Windows](https://www.mozilla.org/firefox/windows)
        - [:simple-apple: macOS](https://www.mozilla.org/firefox/mac)
        - [:simple-linux: Linux](https://www.mozilla.org/firefox/linux)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

!!! 警告
    Firefox在从Mozilla网站的下载中包括一个独特的 [下载令牌](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) ，并使用Firefox中的遥测技术来发送该令牌。 </strong> 该令牌是 **，不包括在 [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/)的版本中。</p>

### 推荐配置

These options can be found in :material-menu: → **Settings**

#### Search

- [ ] 取消勾选 **提供搜索建议**

搜索建议功能可能在你的地区无法使用。

搜索建议将你在地址栏中输入的所有内容发送到默认的搜索引擎，而不管你是否提交了实际的搜索。 禁用搜索建议可以让你更精确地控制你向搜索引擎供应商发送的数据。

#### Privacy & Security

##### 增强跟踪保护

- [x] 选择 **严格的** 增强跟踪保护

这可以通过阻止社交媒体追踪器、指纹脚本（注意，这并不能保护你 *所有* 指纹）、加密器、跨网站追踪cookies和其他一些追踪内容来保护你。 ETP可以防止许多常见的威胁，但它并不阻止所有的跟踪途径，因为它的设计对网站的可用性影响最小甚至没有影响。

##### Firefox Suggest (US only)

[Firefox Suggest](https://support.mozilla.org/en-US/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. We recommend disabling it for the same reason we recommend disabling search suggestions. If you don't see these options under the **Address Bar** header, you do not have the new experience and can ignore these changes.

- [ ] Uncheck **Suggestions from the web**
- [ ] Uncheck **Suggestions from sponsors**

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

If you use a [DNS over HTTPS provider](dns.md):

- [x] Select **Max Protection** and choose a suitable provider

Max Protection enforces the use of DNS over HTTPS, and a security warning will show if Firefox can’t connect to your secure DNS resolver, or if your secure DNS resolver says that records for the domain you are trying to access do not exist. This stops the network you're connected to from secretly downgrading your DNS security.



#### Sync

[火狐浏览器同步](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) ，使您的浏览数据（历史记录、书签等）可以在您的所有设备上访问，并通过E2EE进行保护。



### Arkenfox (advanced)

!!! tip "Use Mullvad Browser for advanced anti-fingerprinting"

    [Mullvad Browser](#mullvad-browser) provides the same anti-fingerprinting protections as Arkenfox out of the box, and does not require the use of Mullvad's VPN to benefit from these protections. Coupled with a VPN, Mullvad Browser can thwart more advanced tracking scripts which Arkenfox cannot. Arkenfox still has the advantage of being much more flexible, and allowing per-site exceptions for websites which you need to stay logged in to.
    

[Arkenfox项目](https://github.com/arkenfox/user.js) ，为Firefox提供了一套精心考虑的选项。 如果你 [决定](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) 使用Arkenfox，有几个 [选项](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) 是主观严格的和/或可能导致一些网站不能正常工作-- [，你可以很容易地改变](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) 以满足你的需要。 我们 **，强烈建议** ，阅读其完整的 [wiki](https://github.com/arkenfox/user.js/wiki)。 Arkenfox还能支持 [容器](https://support.mozilla.org/en-US/kb/containers#w_for-advanced-users)。

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.



## Brave

!!! recommendation

    ![Brave标识](assets/img/browsers/brave.svg){ align=right }
    
    **Brave浏览器**包括一个内置的内容拦截器和[隐私功能](https://brave.com/privacy-features/)，其中许多功能都是默认启用的。
    
    Brave是建立在Chromium网络浏览器项目之上的，所以它应该有熟悉的感觉，而且网站兼容性问题最小。
    
    [:octicons-home-16: 首页](https://brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="洋葱服务" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="隐私政策" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title="文档"}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="源代码" }
    
    ??? 下载注释
    
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
        - [:simple-windows11: Windows](https://brave.com/download/)
        - [:simple-apple: macOS](https://brave.com/download/)
        - [:simple-linux: Linux](https://brave.com/linux/) (1)
    

    1. 我们建议不要使用Flatpak版本的Brave，因为它用Flatpak的沙箱代替了Chromium的沙箱，效果较差。 此外，该软件包并非由Brave Software, Inc.维护。



### 推荐配置

这些选项可以在 :material-menu: → **设置**中找到。



#### Settings



##### 盾

Brave在其 [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-) 功能中包括一些防指纹的措施。 我们建议将这些选项配置为 [，在你访问的所有页面上全局](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-)。

Shields的选项可以根据需要在每个站点的基础上进行降级，但在默认情况下，我们建议设置以下内容。

<div class="annotate" markdown>

- [x] 选择**防止网站根据我的语言偏好对我进行指纹识别**
- [x] 选择跟踪器和广告拦截下的**攻击性**

？? warning "Use default filter lists"
        Brave允许你在内部`brave://adblock`页面中选择额外的内容过滤器。 我们建议不要使用这个功能；相反，保留默认的过滤列表。 使用额外的列表会使你从其他Brave用户中脱颖而出，如果Brave中存在漏洞，恶意规则被添加到你使用的列表中，也可能增加攻击面。

- [x] Select **Strict** under **Upgrade connections to HTTPS**
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Strict, may break sites** under Block fingerprinting

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net/) extension.



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

    !!! tip "Sanitizing on Close"

        - [x] Select **Clear cookies and site data when you close all windows** in the *Cookies and other site data* menu

        If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

1. Brave是 **，而不是** ，对指纹的抵抗力不如Tor浏览器，而且使用Brave和Tor的人要少得多，所以你会脱颖而出。 在需要强大的匿名性的地方 [](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-) ，使用 [Tor浏览器](tor.md#tor-browser)。



##### 扩展程序

在 **Extensions**，禁用你不使用的内置扩展程序。

- [ ] 取消勾选 **Hangouts**
- [] 取消勾选 **WebTorrent**



##### Web3

Brave's Web3 features can potentially add to your browser fingerprint and attack surface. Unless you use any of features, they should be disabled.

- Select **Extensions (no fallback)** under Default Ethereum wallet and Default Solana wallet
- Set **Method to resolve IPFS resources** to **Disabled**



##### System

<div class="annotate" markdown>

- [ ] Uncheck **Continue running apps when Brave is closed** to disable background apps (1)

</div>

1. This option is not present on all platforms.



#### Sync

[Brave 同步](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) 允许你的浏览数据（历史记录、书签等）在你所有的设备上访问，而不需要账户，并以E2EE进行保护。



#### Brave Rewards and Wallet

**Brave Rewards** lets you recieve Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#other-coins-bitcoin-ethereum-etc), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.



## 其它资源

In general, we recommend keeping your browser extensions to a minimum to decrease your attack surface; they have privileged access within your browser, require you to trust the developer, can make you [stand out](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), and [weaken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) site isolation. However, uBlock Origin may prove useful if you value content blocking functionality.



### uBlock Origin

!!! recommendation

    ![uBlock Origin标识](assets/img/browsers/ublock_origin.svg){ align=right }
    
    **uBlock Origin**是一个流行的内容阻止器，可以帮助你阻止广告、跟踪器和指纹脚本。
    
    [:octicons-repo-16: Repository](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="隐私政策" }
    [:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title="文档"}
    [:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="源代码" }
    
    ??? 下载
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)
    

We suggest following the [developer's documentation](https://github.com/gorhill/uBlock/wiki/Blocking-mode) and picking one of the "modes". Additional filter lists can impact performance and [may increase attack surface](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).



##### 其它列表

These are some other [filter lists](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) that you may want to consider adding:

- [x] Check **Privacy** > **AdGuard URL Tracking Protection**
- Add [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)



## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! example "This section is new"

    We are working on establishing defined criteria for every section of our site, and this may be subject to change. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. There are many factors considered and discussed when we recommend a project, and documenting every single one is a work-in-progress.
    



### Minimum Requirements

- 它必须是开源软件。
- Supports automatic updates.
- Receives engine updates in 0-1 days from upstream release.
- Available on Linux, macOS, and Windows.
- 为使浏览器更加尊重隐私所需的任何改变都不应该对用户体验产生负面影响。
- Blocks third-party cookies by default.
- Supports [state partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]



### Best-Case

Our best-case criteria represents what we would like to see from the perfect project in this category. Our recommendations may not include any or all of this functionality, but those which do may rank higher than others on this page.

- Includes built-in content blocking functionality.
- Supports cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/en-US/kb/containers)).
- Supports Progressive Web Apps.  
  PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps, because you benefit from your browser's regular security updates.

- Does not include add-on functionality (bloatware) that does not impact user privacy.

- Does not collect telemetry by default.
- Provides open-source sync server implementation.
- Defaults to a [private search engine](search-engines.md).



### 扩展标准

- 不得复制内置浏览器或操作系统的功能。
- 必须直接影响用户隐私，即不能简单地提供信息。



[^1]:    
    Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state/).
