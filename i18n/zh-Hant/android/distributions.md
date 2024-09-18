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

<small>防護下列威脅：</small>

- [:material-target-account: 針對性攻擊](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: 被動攻擊](../basics/common-threats.md#security-and-privacy){ .pg-orange }

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

GrapheneOS 支援 [沙盒化 Google Play](https://grapheneos.org/usage#sandboxed-google-play) ，他將 Google Play 服務 完全沙盒化，使其如同其他常規應用程式一樣運行。 這意味著可正常使用大多數 Google Play 服務 所提供的功能，像是 推送通知 ，同時讓您完全控制其存取能力和權限，並將其包含在所選的特定 [工作設定檔](../os/android-overview.md#work-profile) 或 [用戶設定檔](../os/android-overview.md#user-profiles) 。

[Google Pixel系列](../mobile-phones.md#google-pixel) 是目前唯一符合 GrapheneOS [硬體安全要求](https://grapheneos.org/faq#future-devices) 的裝置。

預設情況下，Android 會與 Google 進行許多網路連線，以執行 DNS 連線檢查、同步目前的網路時間、檢查您的網路連線，以及其他許多背景工作。 GrapheneOS 不這麼做，他們通過讓作業系統與由其團隊所擁有的伺服器通信來完成上述工作，這些伺服器遵守他們的隱私權政策 這能向 [Google] (.../basics/common-threats.md#privacy-from-service-providers) 隱藏您的資訊（例如：IP位置），但這意味著您的網路管理員或 ISP 的很容易看到您正在連線到 `grapheneos.network`、`grapheneos.org` 等，並推斷出您使用的作業系統。

如果您想要隱藏類似此類的資訊，以避免被您網路上或 ISP 上的對手發現，除了將連線檢查設定變更為 **Standard (Google)** 之外，您還 **必須** 使用 [可信賴的 VPN](../vpn.md)。 它可以在 :gear: **設定** → **網路與網際網路** → **Internet connectivity checks** 中找到. This option allows you to connect to Google's servers for connectivity checks, which, alongside the usage of a VPN, helps you blend in with a larger pool of Android devices.

### DivestOS

If GrapheneOS isn't compatible with your phone, DivestOS is a good alternative. It supports a wide variety of phones with _varying_ levels of security protections and quality control.

<div class="admonition recommendation" markdown>

![DivestOS logo](../assets/img/android/divestos.svg){ align=right }

**DivestOS** 是一個 [LineageOS](https://lineageos.org) 的軟分叉。
DivestOS 從 LineageOS 繼承了許多 [支援的裝置](https://divestos.org/index.php?page=devices\&base=LineageOS) 。 It has signed builds, making it possible to have [verified boot](../os/android-overview.md#verified-boot) on some non-Pixel devices. Not all supported devices support verified boot or other security features.

[:octicons-home-16: Homepage](https://divestos.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="Source Code" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title="Contribute" }

</div>

The [status](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) of firmware updates in particular will vary significantly depending on your phone model. While standard AOSP bugs and vulnerabilities can be fixed with standard software updates like those provided by DivestOS, some vulnerabilities cannot be patched without support from the device manufacturer, making end-of-life devices less safe even with an up-to-date alternative ROM like DivestOS.

DivestOS 具有自動核心漏洞 ([CVE](https://zh.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [修補](https://gitlab.com/divested-mobile/cve_checker)，更少的專有設備驅動程式，和自訂的 [hosts](https://divested.dev/index.php?page=dnsbl) 文件。 Its hardened WebView, [Mulch](https://gitlab.com/divested-mobile/mulch), enables [control-flow integrity](https://en.wikipedia.org/wiki/Control-flow_integrity) for all architectures and [network state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning), and receives out-of-band updates.

DivestOS 還包含來自GrapheneOS 的核心補丁，並透過 [defconfig 加固](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758) 啟用所有可用的核心安全功能。 所有高於3.4版本的核心都包含 整頁的[核心記憶體清理](https://lwn.net/Articles/334747) ，並且所有~22 Clang 編譯的核心都有啟用 [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) 。

DivestOS 也實現了一些最初專為 GrapheneOS 開發的系統加固補丁。 DivestOS 16.0 and higher implements GrapheneOS's `INTERNET` and `SENSORS` permission toggle, [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](https://grapheneos.org/usage#exec-spawning), Java Native Interface [constification](https://en.wikipedia.org/wiki/Const_\(computer_programming\)), and partial [bionic](https://en.wikipedia.org/wiki/Bionic_\(software\)) hardening patchsets. 17.1 and higher features per-network full MAC address randomization, [`ptrace_scope`](https://kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) control, automatic reboot, and Wi-Fi/Bluetooth [timeout options](https://grapheneos.org/features#attack-surface-reduction).

DivestOS 使用 F-Droid 作為其預設應用程式商店。 我們通常 [建議避免使用 F-Droid](obtaining-apps.md#f-droid) ，但在 DivestOS 上這樣做是不可行的；開發人員透過自己的 F-Droid 儲存庫：[DivestOS Official](https://divestos.org/fdroid/official) 來更新他們的應用程式。 For these apps you should continue to use F-Droid **with the DivestOS repository enabled** to keep those components up to date. 對於其他應用程式，我們推薦的 [應用程式獲取途徑](obtaining-apps.md) 仍然適用。

DivestOS replaces many of Android's background network connections to Google services with alternative services, such as using OpenEUICC for eSIM activation, NTP.org for network time, and Quad9 for DNS. These connections can be modified, but their deviation from a standard Android phone's network connections could mean it is easier for an adversary on your network to deduce what operating system you have installed on your phone. If this is a concern to you, consider using a [trusted VPN](../vpn.md) and enabling the native VPN [kill switch](../os/android-overview.md#vpn-killswitch) to hide this network traffic from your local network and ISP.

## 標準

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](../about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- 必須是開源軟體。
- Must support bootloader locking with custom AVB key support.
- Must receive major Android updates within 0-1 months of release.
- Must receive Android feature updates (minor version) within 0-14 days of release.
- Must receive regular security patches within 0-5 days of release.
- Must **not** be "rooted" out of the box.
- Must **not** enable Google Play Services by default.
- Must **not** require system modification to support Google Play Services.
