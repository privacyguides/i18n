---
meta_title: |-
  最佳自訂 Android 作業系統（又稱 自訂ROM ）-
  Privacy Guides
title: 替代作業系統
description: 您可以使用這些安全且尊重隱私的替代方案來取代 Android 手機上的作業系統。
schema:
  - "@context": http://schema.org
    "@type": 網頁
    name: 尊重隱私的 Android 作業系統
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
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Protects against the following threat(s):</small>

- [:material-target-account: Targeted Attacks](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Passive Attacks](../basics/common-threats.md#security-and-privacy){ .pg-orange }

**基於 Android 的自訂作業系統**（通常稱為 **自訂 ROM**）是在裝置上實現更高層級的隱私和安全性的流行方法。 這與 Android 的「stock」版本形成鮮明對比，「stock」版本是手機出廠時附帶的，並且通常與 Google Play 服務 深度整合。

我們建議您在裝置上安裝這些自訂 Android 作業系統之一（按優先順序列出），具體取決於您的裝置與這些作業系統的相容性。

## AOSP 衍生品

### GrapheneOS

<div class="admonition recommendation" markdown>

![GrapheneOS logo](../assets/img/android/grapheneos.svg#only-light){ align=right }
![GrapheneOS logo](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** 是隱私與安全方面的最佳選擇。

GrapheneOS 提供了額外的 [安全強化](https://zh.m.wikipedia.org/wiki/%E5%AE%89%E5%85%A8%E5%BC%B7%E5%8C%96) 和 隱私改進。 它有 [加固的記憶體分配器](https://github.com/GrapheneOS/hardened_malloc)，網路、傳感器權限與各式[安全改進](https://grapheneos.org/features). GrapheneOS 還帶有完整的軔體更新與已簽名的構建版本，因此完全支援 Verified Boot 。

[:octicons-home-16: 首頁](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=文檔}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="原始碼" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=捐款 }

</div>

GrapheneOS supports [sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), which runs Google Play Services fully sandboxed like any other regular app. This means you can take advantage of most Google Play Services, such as push notifications, while giving you full control over their permissions and access, and while containing them to a specific [work profile](../os/android-overview.md#work-profile) or [user profile](../os/android-overview.md#user-profiles) of your choice.

[Google Pixel系列](../mobile-phones.md#google-pixel) 是目前唯一符合 GrapheneOS [硬體安全要求](https://grapheneos.org/faq#future-devices) 的裝置。

By default, Android makes many network connections to Google to perform DNS connectivity checks, to sync with current network time, to check your network connectivity, and for many other background tasks. GrapheneOS replaces these with connections to servers operated by GrapheneOS and subject to their privacy policy. This hides information like your IP address [from Google](../basics/common-threats.md#privacy-from-service-providers), but means it is trivial for an admin on your network or ISP to see you are making connections to `grapheneos.network`, `grapheneos.org`, etc. and deduce what operating system you are using.

GrapheneOS provides the option to switch back to connecting to Google's servers for many of these background connections if you prefer, but it is far more robust/foolproof to use a [trusted VPN](../vpn.md) and enable Android's native VPN [kill switch](../os/android-overview.md#vpn-killswitch) to hide information like this from adversaries on your network.

### DivestOS

<div class="admonition recommendation" markdown>

![DivestOS logo](../assets/img/android/divestos.svg){ align=right }

**DivestOS** 是一個 [LineageOS](https://lineageos.org) 的軟分叉。
DivestOS 從 LineageOS 繼承了許多 [支援的裝置](https://divestos.org/index.php?page=devices\&base=LineageOS) 。 它具有已簽名的構建，使其在某些非 Pixel 裝置上可以使用 [Verified Boot](https://source.android.com/security/verifiedboot) 。

[:octicons-home-16: 首頁](https://divestos.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=文檔}
[:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="原始碼" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=捐款 }

</div>

DivestOS 具有自動核心漏洞 ([CVE](https://zh.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [修補](https://gitlab.com/divested-mobile/cve_checker)，更少的專有設備驅動程式，和自訂的 [hosts](https://divested.dev/index.php?page=dnsbl) 文件。 Its hardened WebView, [Mulch](https://gitlab.com/divested-mobile/mulch), enables [control-flow integrity](https://en.wikipedia.org/wiki/Control-flow_integrity) for all architectures and [network state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning), and receives out-of-band updates.
DivestOS 還包含來自GrapheneOS 的核心補丁，並透過 [defconfig 加固](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758) 啟用所有可用的核心安全功能。 所有高於3.4版本的核心都包含 整頁的[核心記憶體清理](https://lwn.net/Articles/334747) ，並且所有~22 Clang 編譯的核心都有啟用 [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) 。

DivestOS 也實現了一些最初專為 GrapheneOS 開發的系統加固補丁。 DivestOS 16.0 and higher implements GrapheneOS's `INTERNET` and `SENSORS` permission toggle, [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](https://grapheneos.org/usage#exec-spawning), Java Native Interface [constification](https://en.wikipedia.org/wiki/Const_\(computer_programming\)), and partial [bionic](https://en.wikipedia.org/wiki/Bionic_\(software\)) hardening patchsets. 17.1 and higher features per-network full MAC address randomization, [`ptrace_scope`](https://kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) control, automatic reboot, and Wi-Fi/Bluetooth [timeout options](https://grapheneos.org/features#attack-surface-reduction).

DivestOS 使用 F-Droid 作為其預設應用程式商店。 我們通常 [建議避免使用 F-Droid](obtaining-apps.md#f-droid) ，但在 DivestOS 上這樣做是不可行的；開發人員透過自己的 F-Droid 儲存庫：[DivestOS Official](https://divestos.org/fdroid/official) 來更新他們的應用程式。 For these apps you should continue to use F-Droid **with the DivestOS repository enabled** to keep those components up to date. 對於其他應用程式，我們推薦的 [應用程式獲取途徑](obtaining-apps.md) 仍然適用。

DivestOS replaces many of Android's background network connections to Google services with alternative services, such as using OpenEUICC for eSIM activation, NTP.org for network time, and Quad9 for DNS. These connections can be modified, but their deviation from a standard Android phone's network connections could mean it is easier for an adversary on your network to deduce what operating system you have installed on your phone. If this is a concern to you, consider using a [trusted VPN](../vpn.md) and enabling the native VPN [kill switch](../os/android-overview.md#vpn-killswitch) to hide this network traffic from your local network and ISP.

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

DivestOS 韌體更新 [狀態](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) 和品質管理依照所支援的設備不同而異。 我們仍然推薦 GrapheneOS ，具體取決於您裝置的兼容性。 對於其他設備， DivestOS 是不錯的選擇。

並非所有支援設備都可使用 verified boot；且在受支援的裝置中，某些設備的表現較好。

</div>

## 標準

**請注意，我們與所推薦專案沒有任何瓜葛** 。除了 [標準準則](../about/criteria.md) 外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- 必須是開源軟體。
- 必須支援具有自訂 AVB 金鑰支援的引導裝載程式鎖定。
- 必須在 主要 Android 更新 發布後 0-1 個月內收到更新。
- 必須在 Android 功能更新（小版本） 發布後 0-14 天內收到更新。
- 必須在定期安全修補程式發布後 0-5 天內收到更新。
- **不可** 在預設情況下 "rooted" 。
- **不可** 在預設情況下安裝 Google Play 服務 。
- **不可** 修改系統以支援 Google Play 服務 。
