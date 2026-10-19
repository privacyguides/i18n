---
meta_title: "保护隐私的 Android 和 iOS 网页浏览器 - Privacy Guides"
title: 移动浏览器
icon: material/cellphone-information
description: 对于在手机上进行标准/非匿名互联网浏览，目前推荐这些浏览器。
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: 移动端隐私浏览器推荐
    url: "./"
    relatedLink: "../desktop-browsers/"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    applicationCategory: Web Browser
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://apple.com/safari
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>防御以下威胁：</small>

- [:material-account-cash: 监视资本主义](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

这些是我们目前推荐的适用于标准/非匿名互联网浏览的**移动端网页浏览器**及其配置。如果您需要匿名浏览互联网，则应使用 [Tor](tor.md) 。

## Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave 浏览器**包含内置的内容拦截器和[隐私功能](https://brave.com/privacy-features)，其中许多功能默认启用。

Brave 基于 Chromium 网页浏览器项目，因此使用起来应该很熟悉，且几乎不会出现网站兼容性问题。

[:octicons-home-16: 官网](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="隐私政策" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="文档" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="源代码" }

<details class="downloads" markdown>
<summary>下载</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-fdroid: F-Droid](https://brave-browser-apk-release.s3.brave.com/fdroid/repo/index.html)

</details>

</div>

### 推荐的 Brave 配置

Tor浏览器是匿名浏览互联网的唯一途径。当您使用Brave时，我们建议您更改以下设置，以保护您的隐私不受某些方的侵害，但除了 [Tor浏览器](tor.md#tor-browser) 之外的所有浏览器都可以在某些方面被 *个人* 追踪。

=== "Android"

    这些选项可以在 :material-dots-vertical: → **设置** → **Brave Shields 和隐私设置** 中找到。

=== "iOS"

    这些选项可以在 :material-dots-horizontal: → **所有设置** → **Shields 和隐私设置** 中找到。

#### Brave 护盾的全局默认设置

Brave 在其 [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) 功能中包含一些反指纹措施。我们建议在您访问的所有页面中[全局](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings)配置这些选项。

根据需要，可以针对每个站点下调 Shields 的配置级别，但默认情况下，我们的建议设置如下：

=== "Android"

    <div class="annotate" markdown>

    - [x] 在 *拦截跟踪器和广告* 下选择 **激进**
    - [x] 选择 **自动重定向 AMP 页面**
    - [x] 选择 **自动重定向跟踪 URL**
    - [x] 在 *将连接升级为 HTTPS* 下选择 **要求所有连接使用 HTTPS (严格)**
    - \[x\] (可选) 选择 **拦截脚本** (1)
    - [x] 在 *拦截 Cookie* 下选择 **拦截第三方 Cookie**
    - [x] 选择 **拦截指纹识别**
    - [x] 选择 **防止通过语言设置进行指纹识别**

    <details class="warning" markdown>
    <summary>使用默认过滤规则</summary>

    Brave 允许您在 **内容过滤** 菜单或内部的 `brave://adblock` 页面中选择附加的内容过滤器。我们建议不要使用这个功能；相反，保留默认的过滤列表。使用额外的列表会使你从其他Brave用户中脱颖而出，如果Brave中存在漏洞，恶意规则被添加到你使用的列表中，也可能增加攻击面。

    </details>

    - [x] 在 *自动清理* 下选择 **关闭站点标签页**

    </div>

    1. 此选项禁用 JavaScript，这会破坏许多网站。要恢复它们，您可以针对每个网站设置例外情况，方法是点击地址栏中的盾牌图标，并在 *高级控件* 中取消勾选此设置。

=== "iOS"

    <div class="annotate" markdown>

    - [x] 在 *拦截跟踪器和广告* 下选择 **激进**
    - [x] 在 *将连接升级为 HTTPS* 下选择 **严格**
    - [x] 选择 **自动重定向 AMP 页面**
    - [x] 选择 **自动重定向跟踪 URL**
    - \[x\] (可选) 选择 **拦截脚本** (1)
    - [x] 选择 **拦截指纹识别**
    - [x] 在 *自动清理* 下选择 **关闭站点标签页**

    <details class="warning" markdown>
    <summary>使用默认过滤规则</summary>

    Brave 允许您在 **内容过滤** 菜单中选择附加的内容过滤器。我们建议不要使用这个功能；相反，保留默认的过滤规则。使用额外的规则会使你从其他Brave用户中脱颖而出，如果Brave中存在漏洞，恶意规则被添加到你使用的列表中，也可能增加攻击面。

    </details>

    </div>

    1. 此选项禁用 JavaScript，这会破坏许多网站。要恢复它们，您可以针对每个网站设置例外情况，方法是点击地址栏中的盾牌图标，并在 *高级控件* 中取消勾选此设置。

#### 其他隐私设置

=== "Android"

    <div class="annotate" markdown>

    - \[x\] (可选) 在 *安全浏览* 下选择 **不保护** (1)
    - [x] 在 [*WebRTC IP 处理策略*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc) 下选择 **禁用非代理 UDP**
    - [ ] 取消勾选 **允许网站检查您是否保存了付款方式**
    - [x] 选择 **不使用 Brave 的 V8 引擎加速网站，但让 Brave 对攻击有更强的抵抗力**
    - [x] 选择 **退出时关闭标签页**
    - [ ] 取消选中**允许保护隐私的产品分析 (P3A)**
    - [ ] 取消选中**自动发送诊断报告**
    - [ ] 取消选中**自动向 Brave 发送每日使用情况 ping**

    </div>

    1. Brave 在 Android 上的 [安全浏览实现](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) **不会**像其桌面端那样代理 [安全浏览网络请求](https://developers.google.com/safe-browsing/v4/update-api#checking-urls)。这意味着您的 IP 地址可能会被 Google 看到（并记录）。请注意，对于没有 Google Play 服务的 Android 设备，安全浏览不可用。

=== "iOS"

    - [ ] 取消勾选 **允许保护隐私的产品分析 (P3A)**
    - [ ] 取消选中**自动向 Brave 发送每日使用情况 ping**

#### Leo AI

=== "Android"

    这些选项可以在 :material-dots-vertical: → **设置** → **Leo AI** 中找到。

    - [ ] 取消勾选 **在地址栏中显示自动完成建议**

=== "iOS"

    这些选项可以在 :material-dots-horizontal: → **所有设置** → **Leo AI** 中找到。

    - [ ] 取消勾选 **在快速搜索引擎栏中显示**

#### 搜索引擎

=== "Android"

    这些选项可以在 :material-dots-vertical: → **设置** → **搜索引擎** 中找到。

    - [ ] 取消勾选**“显示搜索建议”**

=== "iOS"

    这些选项可以在 :material-dots-horizontal: → **所有设置** → **搜索引擎** 中找到。

    - [ ] 取消勾选 **在快速搜索引擎栏中显示**

#### Brave Sync

[Brave 同步](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync)允许在您的所有设备上访问您的浏览数据（历史记录、书签等），而无需帐户，并使用端到端加密对其进行保护。

## Safari (iOS)

在 iOS 上，任何可以浏览网页的应用程序都[受到限制](https://developer.apple.com/app-store/review/guidelines)，必须使用 Apple 提供的 [WebKit 框架](https://developer.apple.com/documentation/webkit)，因此像 [Brave](#brave) 这样的浏览器不像其在其他操作系统上的版本那样使用 Blink 引擎（Chromium 的核心组件）。

<div class="admonition recommendation" markdown>

![Safari logo](assets/img/browsers/safari.svg){ align=right }

**Safari** 是 iOS 上的默认浏览器。它包含一些[隐私功能](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios)，例如[智能防跟踪](https://webkit.org/blog/7675/intelligent-tracking-prevention)、隔离且临时的无痕浏览标签页、防指纹识别（通过向网站展示简化版的系统配置，使更多设备看起来相同）、指纹随机化，以及为付费 iCloud+ 订阅用户提供的专用代理功能。

[:octicons-home-16: 官网](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="隐私政策" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title="文档" }

</details>

</div>

### 推荐 Safari 配置

以下隐私/安全相关选项可以在 :gear: **设置** → **App** → **Safari 浏览器** 中找到。

#### 允许 Safari 访问

在 **Siri 与搜索** 下：

- [ ] 禁用 **从此 App 学习**
- [ ] 禁用 **在 App 中显示**
- [ ] 禁用 **在主屏幕上显示**
- [ ] 禁用 **建议 App**

这可以防止 Siri 将 Safari 中的内容用于 Siri 建议。

#### 搜索

- [ ] 禁用 **搜索引擎建议**

此设置会将您在地址栏中输入的任何内容发送到 Safari 中设置的搜索引擎。禁用搜索建议功能可让您更精确地控制发送给搜索引擎提供商的数据。

#### 用户场景

Safari 允许您通过不同的用户场景来分隔浏览内容。您所有的 Cookie、历史记录和网站数据在每个用户场景中都是相互独立的。您应该为不同的目的使用不同的用户场景，例如购物、工作或学习。

#### 隐私与安全

- [x] 开启 **阻止跨站跟踪**

这会启用 WebKit 的[智能防跟踪功能](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp)。此功能通过使用设备端机器学习来阻止跟踪器，从而帮助防止不必要的跟踪。 ITP 可抵御许多常见威胁，但不会阻止所有跟踪途径，因为它的设计初衷是不干扰网站的可用性。

- [x] 开启 **需要面容 ID/触控 ID 解锁无痕浏览**

此设置允许您在不使用时将无痕浏览标签页锁定在生物识别/PIN 码之后。

- [ ] 禁用 **欺骗性网站警告**

此设置使用 Google 安全浏览（或针对中国大陆及香港用户的腾讯安全浏览）在您浏览时保护您。因此，您的安全浏览提供商可能会记录您的 IP 地址。禁用此设置将禁用此记录功能，但您可能更容易受到已知网络钓鱼网站的攻击。

- [x] 开启 **不安全连接警告**

如果您连接到未提供 HTTPS 的网站，此设置将显示警告屏幕。 Safari 将自动尝试把该站点升级到 HTTPS，因此只有在没有可用的 HTTPS 连接时才会看到此提示。

- [ ] 禁用 **摘要**

Apple 的 Safari 隐私政策声明：

> 在访问网页时，Safari 可能会通过 OHTTP 将基于网页地址计算出的信息发送给 Apple，以确定是否有相关的摘要可用。

#### 网站设置

在 **相机** 下

- [x] 选择 **询问**

在 **麦克风** 下

- [x] 选择 **询问**

在 **位置** 下

- [x] 选择 **询问**

这些设置确保网站只有在您明确授权后才能访问您的相机、麦克风或位置。

#### 其他隐私设置

这些选项可以在 :gear: **设置** → **App** → **Safari 浏览器** → **高级** 中找到。

##### 指纹识别缓解

**高级跟踪和指纹保护** 设置将随机化某些值，从而使指纹识别变得更加困难：

- [x] 选择 **所有浏览** 或 **无痕浏览**

##### 保护隐私的广告分析

- [ ] 禁用 **保护隐私的广告分析**

传统上，广告点击量分析使用的跟踪技术侵犯了用户隐私。[隐私点击分析](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) 是一项 WebKit 功能及建议的 Web 标准，旨在让广告商在不损害用户隐私的情况下衡量网络营销活动的效果。

该功能本身几乎没有隐私问题，因此虽然您可以选择让它保持开启，但考虑到它在无痕浏览中会自动禁用，我们认为这是禁用该功能的一个参考指标。

#### 始终开启无痕浏览

打开 Safari，点击右下角的标签页按钮。然后，展开 :material-format-list-bulleted: 标签页组列表。

- [x] 选择 **无痕浏览**

Safari 的无痕浏览模式提供了额外的隐私保护。无痕浏览会为每个标签页开启一个新的[临时](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral)会话，这意味着标签页之间彼此隔离。无痕浏览还有其他一些较小的隐私优势，例如在使用 Safari 翻译功能时，不会将网页地址发送给 Apple。

请注意，无痕浏览不会保存 Cookie 和网站数据，因此无法在网站上保持登录状态。这可能会带来不便。

#### iCloud 同步

同步 Safari 历史记录、标签页组、iCloud 标签页和保存的密码均使用端到端加密。然而默认情况下，书签[并未加密](https://support.apple.com/HT202303)。 Apple 可以根据其[隐私政策](https://apple.com/legal/privacy/en-ww)解密并访问它们。

你可以通过开启[高级数据保护](https://support.apple.com/HT212520)，为你的 Safari 书签和下载内容启用端到端加密。前往 :gear: **设置** → **iCloud** → **高级数据保护**。

- [x] 开启 **高级数据保护**

如果您使用 iCloud 时禁用了高级数据保护，我们也建议将 Safari 的默认下载位置设置为设备上的本地文件夹。此选项可以在 :gear: **设置** → **App** → **Safari 浏览器** → **通用** → **下载项** 中找到。

## 标准

**请注意，我们与我们推荐的任何项目都没有附属关系。**除了[我们的标准标准](about/criteria.md)之外，我们还制定了一套明确的要求，以便我们能够提供客观的建议。建议您在选择使用某个项目之前先熟悉此列表，并进行自己的研究，以确保它是您的正确选择。

### 最低要求

- 必须支持自动更新。
- 必须能快速接收来自上游版本的引擎更新。
- 必须支持内容拦截。
- 为使浏览器更加尊重隐私所需的任何改变都不应该对用户体验产生负面影响。
