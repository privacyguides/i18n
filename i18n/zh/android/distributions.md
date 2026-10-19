---
meta_title: "最佳 Android 操作系统 - Privacy Guides"
title: 替代发行版
description: 您可以使用这些安全且尊重隐私的替代品，替换掉您 Android 手机上的操作系统。
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: 注重隐私的 Android 操作系统
    url: "./"
  - "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>防范以下威胁：</small>

- [:material-target-account: 针对性攻击](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: 被动攻击](../basics/common-threats.md#security-and-privacy){ .pg-orange }

**基于 Android 的定制操作系统**（有时被称为**第三方 ROM**）能够为您在设备上实现更高层次的隐私和安全。这有别于手机出厂时自带的“原生”版本 Android，后者通常会与 Google Play 服务以及其他厂商软件深度集成。

如果您有一台 Google Pixel，我们推荐安装 GrapheneOS，因为它提供了强化的安全性和额外的隐私功能。我们不列出其他操作系统或设备的原因如下：

- 它们通常拥有[较弱的安全性](index.md#install-a-custom-distribution)。
- 当维护者失去兴趣或更换他们的设备时，通常会放弃提供支持。这与 GrapheneOS 所遵循的可预测的[支持周期](https://grapheneos.org/faq#device-lifetime)形成了对比。
- 它们通常很少或几乎没有显著的隐私或安全性改进，因此不值得安装。

## GrapheneOS

<div class="admonition recommendation" markdown>

![GrapheneOS logo](../assets/img/android/grapheneos.svg#only-light){ align=right }
![GrapheneOS logo](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

谈及隐私和安全性，**GrapheneOS** 是最佳选择。

GrapheneOS 提供了额外的[安全加固](https://en.wikipedia.org/wiki/Hardening_(computing))和隐私改进。它拥有一个[加固的内存分配器](https://github.com/GrapheneOS/hardened_malloc)、网络和传感器权限，以及各种其他[安全功能](https://grapheneos.org/features)。 GrapheneOS 还提供完整的固件更新和已签名的系统构建，因此完全支持验证启动（Verified Boot）。

[:octicons-home-16: 主页](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="隐私政策" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title="文档" }
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="源代码" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title="贡献" }

</div>

GrapheneOS 支持[沙盒化的 Google Play](https://grapheneos.org/usage#sandboxed-google-play)，它能像运行其他常规应用一样，将 Google Play 服务完全运行在沙盒中。这意味着您可以利用大多数 Google Play 服务（例如推送通知），同时拥有对其权限和访问的完全控制，并且能将它们限制在您选择的特定[工作配置文件](../os/android-overview.md#work-profile)或[用户配置文件](../os/android-overview.md#user-profiles)中。

[Google Pixel 手机](../mobile-phones.md#google-pixel)是目前唯一符合 GrapheneOS [硬件安全要求](https://grapheneos.org/faq#future-devices)的设备。 Pixel 8 及更新机型支持 ARM 的内存标记扩展（MTE），这项硬件安全增强功能可大幅降低通过内存破坏错误（memory corruption bugs）发生漏洞利用的几率。 GrapheneOS 极大地扩展了所支持设备上 MTE 的覆盖范围。与原厂系统仅允许通过开发者选项或 Google 高级保护计划启用有限的 MTE 实现不同，GrapheneOS 默认在系统内核、默认系统组件，以及其 Vanadium 网络浏览器和其 WebView 中提供更稳健的 MTE 实现。

GrapheneOS 还提供了一个全局开关，可为所有用户安装的应用启用 MTE，路径位于 :gear: **设置** → **安全与隐私** → **漏洞利用保护** → **内存标记** → **默认启用**。该操作系统还提供了针对单个应用的开关，以便在应用因兼容性问题崩溃时禁用 MTE。

### 连接检查

默认情况下，Android 会与 Google 建立大量网络连接，用于执行 DNS 连接检查、与当前网络时间同步、检查您的网络连通性，以及许多其他后台任务。 GrapheneOS 将这些操作替换为连接由 GrapheneOS 运营并受其隐私政策约束的服务器。此举虽然[向 Google 隐藏了](../basics/common-threats.md#privacy-from-service-providers)您的 IP 地址等信息，但这意味着您网络中的管理员或 ISP 很容易就能看到您正在连接到 `grapheneos.network`、`grapheneos.org` 等服务器，进而推断出您使用的是哪种操作系统。

如果您想向您所在网络或 ISP 上的对手隐藏此类信息，除了将连接检查设置更改为 **Standard (Google)** 外，您**必须**使用一款[受信任的 VPN](../vpn.md)。该选项位于 :gear: **设置** → **网络和互联网** → **Internet connectivity checks**。此选项允许您连接到 Google 的服务器以进行连接检查，这与使用 VPN 一起，可帮助您混入更庞大的 Android 设备群体中以隐藏自己。

## 建议标准

**请注意，我们与我们推荐的任何项目均无从属关联。** 除了[我们的通用标准](../about/criteria.md)外，我们还制定了一套明确的要求，以便能够提供客观的建议。我们建议您在选择使用某个项目之前熟悉此列表，并自行进行研究以确保其是您的正确选择。

- 它必须是开源软件。
- 必须支持锁定引导加载程序（Bootloader）并支持自定义 AVB 密钥。
- 必须在主要 Android 版本发布后的 0-1 个月内获得更新。
- 必须在 Android 功能更新（次要版本）发布后的 0-14 天内获得更新。
- 必须在定期安全补丁发布后的 0-5 天内获得更新。
- 必须**非**开箱即“Root”。
- 必须**默认未**启用 Google Play 服务。
- 必须**不**需要修改系统即可支持 Google Play 服务。
