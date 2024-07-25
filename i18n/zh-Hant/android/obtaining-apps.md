---
title: 應用程式獲取途徑
---

有許多途徑可用於獲取 Android 應用程式而不必犧牲您的隱私，您甚至可以不使用 Google Play 服務 即可從 Play 商店下載應用程式。 我們推薦以下獲取 Android 應用程式的途徑（按優先順序列出）。

## Obtainium

<div class="admonition recommendation" markdown>

![Obtainium logo](../assets/img/android/obtainium.svg){ align=right }

**Obtainium** 是一個應用程式管理器，可讓您直接從開發人員自己的版本發布頁面下載及更新應用程式（即 Github、GitLab、開發人員自己的網站 等等。），而不是使用集中式的應用程式商店或儲存庫。 在 Android 12 及以上版本，其支援背景自動更新。

[:octicons-repo-16: 儲存庫](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ImranR98/Obtainium/wiki){ .card-link title=文檔}
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="原始碼" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=捐款 }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

Obtainium 允許您從各種來源下載 APK 安裝檔案，但您需要確認這些來源及應用程式是可以信任且可靠的。 舉例來說，使用 Obtainium 從 [Signal APK 下載頁面](https://signal.org/android/apk) 下載並安裝 Signal 應該是安全的；但如果將第三方儲存庫如：Aptoide 或 APKPure 作為來源則可能會帶來額外的風險。 至於惡意 _更新_ ，其較不可能對您構成威脅；因為 Android 本身會在安裝更新之前驗證應用程式更新是否與手機上現有應用程式為相同的開發人員所簽署的。

## GrapheneOS App Store

GrapheneOS 的 應用程式商店 可在 [GitHub](https://github.com/GrapheneOS/Apps/releases) 找到。 它支持 Android 12 及以上版本，並且能夠自我更新。 這個 應用程式商店 中有由 GrapheneOS 專案建立的獨立應用程式，例如：[Auditor](../device-integrity.md#auditor-android)、[Camera](general-apps.md#secure-camera)、[PDF Viewer](general-apps.md#secure-pdf-viewer)。 如果您正在尋找這些應用程式，強烈建議從 GrapheneOS 應用程式商店 獲得而不是從 Play 商店獲得，因為其商店中的應用程式是用 GrapheneOS 項目自己的簽名來簽署的，而 Google 無權訪問。

## Aurora Store

Google Play商店 需要登錄 Google帳戶 才能使用，這不利於隱私。 您可以使用替代客戶端，如：Aurora Store；來解決這個問題。

<div class="admonition recommendation" markdown>

![Aurora Store logo](../assets/img/android/aurora-store.webp){ align=right }

**Aurora Store** 是一個 Google Play商店 客戶端，其無須 Google帳戶、Google Play服務 或 microG 便可下載應用程式

[:octicons-home-16: 首頁](https://auroraoss.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="隱私權政策" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

Aurora Store 不允許其匿名帳戶下載付費應用程式。 您可以選擇在 Aurora Store 上登錄 Google帳戶 來下載已購買的應用程式，這確實將給予 Google 能力用於了解並存取您已安裝的應用程式。 即便如此，您仍然受益於不需要在裝置上擁有完整的 Google Play 客戶端 和 Google Play 服務 抑或是 microG。

## 手動添加 RSS 以追蹤應用程式更新

對於在 GitHub 和 GitLab 等平台上發布的應用程序，您可以將其 RSS 摘要添加到您的 [新聞聚合器](../news-aggregators.md) ，這將幫助您追蹤新版本。

![RSS APK](../assets/img/android/rss-apk-light.png#only-light) ![RSS APK](../assets/img/android/rss-apk-dark.png#only-dark) ![APK Changes](../assets/img/android/rss-changes-light.png#only-light) ![APK Changes](../assets/img/android/rss-changes-dark.png#only-dark)

### GitHub

在 GitHub 上，此處以 [Secure Camera](general-apps.md#secure-camera) 作為例子，您需要先獲取其 [版本發布頁面](https://github.com/GrapheneOS/Camera/releases) 的網址，並在最後加上 ` .atom` ：

`https://github.com/GrapheneOS/Camera/releases.atom`

### GitLab

在 GitLab 上，此處以 [Aurora Store](#aurora-store) 作為例子，您需要先獲取其 [專案儲存庫](https://gitlab.com/AuroraOSS/AuroraStore) 的網址，並在最後加上 `/-/tags?format=atom` ：

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

### 驗證 APK Fingerprints

如果你打算下載 APK 並手動安裝，則可以使用 [`apksigner`](https://developer.android.com/studio/command-line/apksigner) 工具來驗證其簽章，該工具是 Android [build-tools](https://developer.android.com/studio/releases/build-tools) 的一部分。

1. 安裝 [Java JDK](https://oracle.com/java/technologies/downloads) 。

2. 下載 [Android Studio 指令列工具](https://developer.android.com/studio#command-tools) 。

3. 解壓縮下載的檔案：

   ```bash
   unzip commandlinetools-*.zip
   cd cmdline-tools
   ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
   ```

4. 執行簽章驗證指令：

   ```bash
   ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
   ```

5. 然後可以將產生的雜湊值與另一個來源的相同應用程式進行比對。 一些開發人員（例如 Signal）也會在其網站上 [展示 fingerprints](https://signal.org/android/apk)，您可以用先前產生的雜湊值與其比對。

   ```bash
   Signer #1 certificate DN: CN=GrapheneOS
   Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
   Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
   Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
   ```

## F-Droid

![F-Droid logo](../assets/img/android/f-droid.svg){ align=right width=120px }

\==我們只建議用 F-Droid 來獲取無法從上述管道取得的應用程式== 。F-Droid 經常被推薦為 Google Play 替代品，特別是在隱私社群內。 能新增第三方儲存庫且不被局限於 Google 圍牆花園使其廣受歡迎。 F-Droid 也為某些應用程式提供了 [可重現構建](https://f-droid.org/en/docs/Reproducible_Builds) ，並致力於自由和開放原始碼軟體。 然而，F-Droid 構建、簽署和交付軟體包的方式存在一些與安全缺失：

由於其構建應用程式的過程，「官方」F-Droid 儲存庫中的應用程式在更新上經常存在延遲。 F-Droid 維護人員在使用自己的金鑰簽署應用程式時也常會重複使用 package ID，這並不理想，因為這給了 F-Droid 團隊終極信任。 此外，將應用程式納入官方 F-Droid 儲存庫中的要求不如 Google Play 等其他應用程式商店嚴格，這意味著 F-Droid 往往會託管更多較舊、未維護或不符合 [現代安全標準](https://developer.android.com/google/play/requirements/target-sdk) 的應用程式。

其他流行的 F-Droid 第三方儲存庫（例如：[IzzyOnDroid](https://apt.izzysoft.de/fdroid)）緩解了其中的一些問題。 IzzyOnDroid 存儲庫直接從 GitHub 拉取構建，是開發者自己存儲庫的下一個最好的東西。 However, it is not something that we can fully recommend, as apps are typically [removed](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446) from that repository if they are later added to the main F-Droid repository. While that makes sense (since the goal of that particular repository is to host apps before they're accepted into the main F-Droid repository), it can leave you with installed apps which no longer receive updates.

That said, the [F-Droid](https://f-droid.org/en/packages) and [IzzyOnDroid](https://apt.izzysoft.de/fdroid) repositories are home to countless apps, so they can be a useful tool to search for and discover open-source apps that you can then download through other means such as the Play Store, Aurora Store, or by getting the APK directly from the developer. You should use your best judgement when looking for new apps via this method, and keep an eye on how frequently the app is updated. Outdated apps may rely on unsupported libraries, among other things, posing a potential security risk.

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

In some rare cases, the developer of an app will only distribute it through F-Droid ([Gadgetbridge](https://gadgetbridge.org) is one example of this). If you really need an app like that, we recommend using the newer [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) client instead of the original F-Droid app to obtain it. F-Droid Basic supports automatic background updates without privileged extension or root, and has a reduced feature set (limiting attack surface).

</div>
