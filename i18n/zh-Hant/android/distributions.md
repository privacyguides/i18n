---
meta_title: |-
  最佳自訂Android作業系統（又稱 自訂ROM ）
  Privacy Guides
title: 替代發行版
description: 您可以使用這些安全且尊重隱私的替代方案來取代 Android 手機上的作業系統。
schema:
  - "@context": http://schema.org
    "@type": 網頁
    name: 私密 Android 作業系統
    url: ./
  - "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": 網頁
      url: ./
  - "@context": http://schema.org
    "@type": CreativeWork
    name: Divest
    image: /assets/img/android/divestos.svg
    url: https://divestos.org/
    sameAs: https://en.wikipedia.org/wiki/DivestOS
    subjectOf:
      "@context": http://schema.org
      "@type": 網頁
      url: ./
---

**基於 Android 的自訂作業系統**（通常稱為 **自訂 ROM**）是在裝置上實現更高層級的隱私和安全性的流行方法。 這與 Android 的「庫存」版本形成鮮明對比，「庫存」版本是手機出廠時附帶的，並且通常與 Google Play 服務深度整合。

我們建議您在裝置上安裝這些自訂 Android 作業系統之一（按優先順序列出），具體取決於您的裝置與這些作業系統的相容性。

## AOSP 衍生品

### GrapheneOS

<div class="admonition recommendation" markdown>

![GrapheneOS logo](../assets/img/android/grapheneos.svg#only-light){ align=right }
![GrapheneOS logo](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** 是隱私與安全方面的最佳選擇。

GrapheneOS 提供了額外的 [安全強化](https://zh.m.wikipedia.org/wiki/%E5%AE%89%E5%85%A8%E5%BC%B7%E5%8C%96) 和 隱私改進。 它有 [加固的記憶體分配器](https://github.com/GrapheneOS/hardened_malloc)，網路、傳感器權限與各式[安全改進](https://grapheneos.org/features). GrapheneOS 還帶有完整的軔體更新與已簽名的構建版本，因此完全支援 驗證啟動 。

[:octicons-home-16: 首頁](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=文檔}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="原始碼" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=捐款 }

</div>

GrapheneOS 支援 [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play) ，他將 [Google Play Services](https://zh.wikipedia.org/wiki/Google_Play%E6%9C%8D%E5%8B%99) 完全沙盒化，使其如同其他常規應用程式一樣運行。 這意味著可正常使用大多數Google Play Services所提供的功能，像是 [推送通知](https://firebase.google.com/docs/cloud-messaging) ，同時讓您完全控制其存取能力和權限，並將其包含在所選的特定 [工作設定檔](../os/android-overview.md#work-profile) 或 [用戶設定檔](../os/android-overview.md#user-profiles) 。

[Google Pixel系列](../mobile-phones.md#google-pixel) 是目前唯一符合 GrapheneOS [硬體安全要求](https://grapheneos.org/faq#future-devices) 的裝置。

### DivestOS

<div class="admonition recommendation" markdown>

![DivestOS logo](../assets/img/android/divestos.svg){ align=right }

**DivestOS** 是一個 [LineageOS](https://lineageos.org) 的軟分叉。
DivestOS 從 LineageOS 繼承了許多 [支援的裝置](https://divestos.org/index.php?page=devices\&base=LineageOS)。 它具有已簽名的構建，使其在某些非 Pixel 裝置上可以使用 [驗證啟動](https://source.android.com/security/verifiedboot) 。

[:octicons-home-16: 首頁](https://divestos.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=文檔}
[:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="原始碼" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=捐款 }

</div>

DivestOS 具有自動核心漏洞 ([CVE](https://zh.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [修補](https://gitlab.com/divested-mobile/cve_checker)，更少的專有設備驅動程式，和自訂的 [hosts](https://divested.dev/index.php?page=dnsbl) 文件。 其加固的 WebView：[Mulch](https://gitlab.com/divested-mobile/mulch)，為所有架構啟用了 [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) 並引入了 [網路狀態分割](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) ，並接受 緊急更新。
DivestOS 還包含來自GrapheneOS 的核心補丁，並透過 [defconfig hardening](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758) 啟用所有可用的核心安全功能。 所有高於3.4版本的核心都包含 整頁的[核心記憶體清理](https://lwn.net/Articles/334747) ，並且所有~22 Clang 編譯的內核都有啟用 [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) 。

DivestOS 也實現了一些最初專為 GrapheneOS 開發的系統加固補丁。 DivestOS 16.0 及更高版本實現了GrapheneOS 的 [`網路`](https://developer.android.com/training/basics/network-ops/connecting) 和傳感器權限。除此之外還有： [加固的記憶體分配器](https://github.com/GrapheneOS/hardened_malloc) 、 [更安全的應用程式啟動](https://grapheneos.org/usage#exec-spawning) 、 [JNI](https://zh.wikipedia.org/wiki/Java%E6%9C%AC%E5%9C%B0%E6%8E%A5%E5%8F%A3) [聲明](https://zh.wikipedia.org/wiki/Const)，和部分 [bionic](https://zh.wikipedia.org/wiki/Bionic_\(%E8%BB%9F%E9%AB%94\)) 強化補丁集。 17.1 及更高版本有 GrapheneOS 所具有的「根據每個網路完整的 [MAC 隨機化](https://en.wikipedia.org/wiki/MAC_address#Randomization) 」選項、 [`ptrace_scope`](https://kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) 控制 、 [自動重新啟動](https://grapheneos.org/features#auto-reboot) ，和 Wi-Fi/藍牙 [逾時關閉選項](https://grapheneos.org/features#attack-surface-reduction)。

DivestOS 使用 F-Droid 作為其預設應用程式商店。 我們通常 [建議避免使用 F-Droid](obtaining-apps.md#f-droid) ，但在 DivestOS 上這樣做是不可行的；開發人員透過自己的F-Droid 儲存庫 ([DivestOS Official](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) 和 [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2)) 更新應用程式。 我們建議停用官方 F-Droid 應用程式，改為使用 [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) 並 **添加DivestOS儲存庫** 來保持這些組件處於最新狀態。 對於其他應用程式，我們推薦的獲取方法仍然適用。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

DivestOS 韌體更新 [狀態](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) 和品質管理依照所支援的設備不同而異。 我們仍然推薦 GrapheneOS，具體取決於您裝置的兼容性。 對於其他設備，DivestOS 是不錯的選擇

並非所有支援設備都可使用 驗證啟動 ；且在受支援的裝置中，某些設備的表現較好。

</div>

## 標準

**請注意，我們所推薦專案沒有任何瓜葛** 。除了 [標準準則](../about/criteria.md) 外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- 必須是開源軟體。
- 必須支援具有自訂 AVB 金鑰支援的引導裝載程式鎖定。
- 必須在主要 Android 更新發布後 0-1 個月內收到更新
- 必須在Android 功能更新（小版本）發布後 0-14 天內收到更新
- Must receive regular security patches within 0-5 days of release.
- Must **not** be "rooted" out of the box.
- Must **not** enable Google Play Services by default.
- Must **not** require system modification to support Google Play Services.
