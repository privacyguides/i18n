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

DivestOS 具有自動核心漏洞 ([CVE](https://zh.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [修補](https://gitlab.com/divested-mobile/cve_checker)，更少的專有設備驅動程式，和自訂的 [hosts](https://divested.dev/index.php?page=dnsbl) 文件。 Its hardened WebView, [Mulch](https://gitlab.com/divested-mobile/mulch), enables [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) for all architectures and [network state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning), and receives out-of-band updates.
DivestOS also includes kernel patches from GrapheneOS and enables all available kernel security features via [defconfig hardening](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). All kernels newer than version 3.4 include full page [sanitization](https://lwn.net/Articles/334747) and all ~22 Clang-compiled kernels have [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) enabled.

DivestOS implements some system hardening patches originally developed for GrapheneOS. DivestOS 16.0 and higher implements GrapheneOS's [`INTERNET`](https://developer.android.com/training/basics/network-ops/connecting) and SENSORS permission toggle, [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](https://grapheneos.org/usage#exec-spawning), [JNI](https://en.wikipedia.org/wiki/Java_Native_Interface) [constification](https://en.wikipedia.org/wiki/Const_\(computer_programming\)), and partial [bionic](https://en.wikipedia.org/wiki/Bionic_\(software\)) hardening patchsets. 17.1 and higher features GrapheneOS's per-network full [MAC randomization](https://en.wikipedia.org/wiki/MAC_address#Randomization) option, [`ptrace_scope`](https://kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) control, [automatic reboot](https://grapheneos.org/features#auto-reboot), and Wi-Fi/Bluetooth [timeout options](https://grapheneos.org/features#attack-surface-reduction).

DivestOS uses F-Droid as its default app store. We normally [recommend avoiding F-Droid](obtaining-apps.md#f-droid), but doing so on DivestOS isn't viable; the developers update their apps via their own F-Droid repositories ([DivestOS Official](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) and [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2)). We recommend disabling the official F-Droid app and using [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) **with the DivestOS repositories enabled** to keep those components up to date. For other apps, our recommended methods of obtaining them still apply.

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

DivestOS firmware update [status](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) and quality control varies across the devices it supports. We still recommend GrapheneOS depending on your device's compatibility. For other devices, DivestOS is a good alternative.

Not all of the supported devices have verified boot, and some perform it better than others.

</div>

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
