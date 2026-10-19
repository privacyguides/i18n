---
title: "获取应用程序"
description: 我们推荐使用这些方法在 Android 上获取应用程序，而无需与 Google Play 服务进行交互。
---

有许多方法可以私下获取 Android 应用程序，甚至是从 Play 商店获取，而无需与 Google Play 服务交互。我们推荐以下在 Android 上获取应用程序的方法，按优先级排序。

## Obtainium

<div class="admonition recommendation" markdown>

![Obtainium logo](../assets/img/android/obtainium.svg){ align=right }

**Obtainium** 是一个应用程序管理器，允许您直接从开发者自己的发布页面（即 GitHub、GitLab、开发者网站等）安装和更新应用程序，而不是通过中心化的应用商店/存储库。它支持在 Android 12 及更高版本上自动在后台更新。

[:octicons-repo-16: 存储库](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ImranR98/Obtainium/wiki){ .card-link title=文档}
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="源代码" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=贡献 }

<details class="downloads" markdown>
<summary>下载</summary>

- [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

Obtainium 允许您从各种来源下载 APK 安装文件，您需要自行确保这些来源和应用程序是合法的。例如，使用 Obtainium 从 [Signal 的 APK 下载页面](https://signal.org/android/apk) 安装 Signal 应该没有问题，但从 Aptoide 或 APKPure 等第三方 APK 存储库安装可能会带来额外的风险。安装恶&#x610F;_&#x66F4;&#x65B0;_&#x7684;风险较低，因为在安装之前，Android 本身会验证所有应用程序更新是否与您手机上的现有应用程序由同一开发者签名。

## GrapheneOS 应用商店

GrapheneOS 的应用商店可以在 [GitHub](https://github.com/GrapheneOS/Apps/releases) 上找到。它支持 Android 12 及以上版本，并能够自行更新。该应用商店提供由 GrapheneOS 项目构建的独立应用程序，例如 [Auditor](../device-integrity.md#auditor-android)、[Camera](general-apps.md#secure-camera) 和 [PDF Viewer](general-apps.md#secure-pdf-viewer)。如果您正在寻找这些应用程序，我们强烈建议您从 GrapheneOS 的应用商店而不是 Play 商店获取它们，因为其商店上的应用程序是由 GrapheneOS 项目自己的签名签发的，Google 无法访问该签名。

## Aurora Store

Google Play 商店需要登录 Google 帐户，这对隐私不利。您可以通过使用替代客户端（例如 Aurora Store）来绕过此问题。

<div class="admonition recommendation" markdown>

![Aurora Store logo](../assets/img/android/aurora-store.webp){ align=right }

**Aurora Store** 是一个 Google Play 商店客户端，不需要 Google 帐户、Google Play 服务或 microG 即可下载应用程序。

[:octicons-home-16: 主页](https://auroraoss.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="隐私政策" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="源代码" }

<details class="downloads" markdown>
<summary>下载</summary>

- [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

Aurora Store 不允许您使用其匿名帐户功能下载付费应用程序。您可以选择在 Aurora Store 中使用 Google 帐户登录，以下载您已购买的应用程序，但这确实会让 Google 访问您已安装的应用程序列表。然而，您的设备上仍然不需要完整的 Google Play 客户端和 Google Play 服务或 microG，并从中受益。

## 使用 RSS 通知手动获取

对于在 GitHub 和 GitLab 等平台上发布的应用程序，您可以将 RSS 订阅添加到您的[新闻聚合器](../news-aggregators.md)中，以帮助您跟踪新版本。

![RSS APK](../assets/img/android/rss-apk-light.png#only-light) ![RSS APK](../assets/img/android/rss-apk-dark.png#only-dark) ![APK Changes](../assets/img/android/rss-changes-light.png#only-light) ![APK Changes](../assets/img/android/rss-changes-dark.png#only-dark)

### GitHub

在 GitHub 上，以 [Secure Camera](general-apps.md#secure-camera) 为例，您可以导航到其[发布页面](https://github.com/GrapheneOS/Camera/releases)并将 `.atom` 附加到 URL 后面：

`https://github.com/GrapheneOS/Camera/releases.atom`

### GitLab

在 GitLab 上，以 [Aurora Store](#aurora-store) 为例，您可以导航到其[项目存储库](https://gitlab.com/AuroraOSS/AuroraStore)并将 `/-/tags?format=atom` 附加到 URL 后面：

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

### 验证 APK 指纹

如果您手动下载 APK 文件进行安装，您可以使用 [`apksigner`](https://developer.android.com/studio/command-line/apksigner) 工具验证其签名，该工具是 Android [build-tools](https://developer.android.com/studio/releases/build-tools) 的一部分。

1. 安装 [Java JDK](https://oracle.com/java/technologies/downloads)。

2. 下载 [Android Studio 命令行工具](https://developer.android.com/studio#command-tools)。

3. 解压下载的压缩包：

   ```bash
   unzip commandlinetools-*.zip
   cd cmdline-tools
   ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
   ```

4. 运行签名验证命令：

   ```bash
   ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
   ```

5. 然后可以将生成的哈希值与另一个来源进行比较。一些开发者（如 Signal）会在他们的网站上[显示指纹](https://signal.org/android/apk)。

   ```bash
   Signer #1 certificate DN: CN=GrapheneOS
   Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
   Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
   Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
   ```

## F-Droid

![F-Droid logo](../assets/img/android/f-droid.svg){ align=right width=120px }

\==我们仅推荐使用 F-Droid 作为获取无法通过上述方式获取的应用程序的方法。== F-Droid 经常被推荐作为 Google Play 的替代品，特别是在隐私社区中。添加第三方存储库且不受限于 Google 围墙花园的选项，使其广受欢迎。 F-Droid 此外还为一些应用程序提供[可重复构建](https://f-droid.org/en/docs/Reproducible_Builds)，并致力于免费和开源软件。但是，F-Droid 构建、签名和交付软件包的方式存在一些与安全相关的缺点：

由于其构建应用程序的流程，_官方_ F-Droid 存储库中的应用程序经常在更新方面落后。 F-Droid 维护者在使用自己的密钥签署应用程序时也重用包 ID，这并不理想，因为这赋予了 F-Droid 团队绝对的信任。此外，包含在官方 F-Droid 存储库中的应用程序的要求不如 Google Play 等其他应用商店严格，这意味着 F-Droid 往往托管更多陈旧的、无人维护的或不再符合[现代安全标准](https://developer.android.com/google/play/requirements/target-sdk)的应用程序。

F-Droid 的其他流行第三方存储库（如 [IzzyOnDroid](https://apt.izzysoft.de/fdroid)）减轻了其中的一些担忧。 IzzyOnDroid 存储库直接从代码托管平台（GitHub、GitLab 等）获取构建版本，这是仅次于开发者自己的存储库的最佳选择。他们还为数百个应用程序提供[可重复构建](https://android.izzysoft.de/articles/named/iod-rbs-mirrors-clients)，并有开发者验证开发者签名 APK 的可重复性。此外，IzzyOnDroid 团队还会对存储库中的应用程序进行[额外的安全扫描](https://android.izzysoft.de/articles/named/iod-scan-apkchecks)，这通常会促使他们与应用程序开发者进行[讨论](https://github.com/gouravkhunger/QuotesApp/issues/22)，以改进其应用程序的隐私性。请注意，在[某些情况下](https://gitlab.com/IzzyOnDroid/repo#are-apps-removed-from-the-repo--and-when-does-that-happen)，应用程序可能会从 IzzyOnDroid 存储库中移除。

[F-Droid](https://f-droid.org/en/packages) 和 [IzzyOnDroid](https://apt.izzysoft.de/fdroid) 存储库中包含无数应用程序，因此它们是搜索和发现开源应用程序的有用场所，然后您可以通过其他方式（例如 Play 商店、Aurora Store 或直接从开发者处获取 APK）下载这些应用程序。当通过这种方法寻找新应用程序时，您应该使用最佳判断，并留意应用程序的更新频率。过时的应用程序可能会依赖不受支持的库等，从而带来潜在的安全风险。

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

在极少数情况下，某个应用程序可能只能通过 F-Droid 获取。如果您确实需要这样的应用程序，我们建议使用较新的 [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) 客户端而不是原始的 F-Droid 应用程序来获取它，因为它减少了功能集（限制了攻击面）。

</div>
