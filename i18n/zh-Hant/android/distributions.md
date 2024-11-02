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

GrapheneOS 支援 [沙盒化 Google Play](https://grapheneos.org/usage#sandboxed-google-play) ，他將 Google Play 服務 完全沙盒化，使其如同其他常規應用程式一樣運行。 這意味著可正常使用大多數 Google Play 服務 所提供的功能，像是 推送通知 ，同時讓您完全控制其存取能力和權限，並將其包含在所選的特定 [工作設定檔](../os/android-overview.md#work-profile) 或 [使用者設定檔](../os/android-overview.md#user-profiles) 。

[Google Pixel系列](../mobile-phones.md#google-pixel) 是目前唯一符合 GrapheneOS [硬體安全要求](https://grapheneos.org/faq#future-devices) 的裝置。

預設情況下，Android 會與 Google 進行許多網路連線，以執行 DNS 連線檢查、同步目前的網路時間、檢查您的網路連線，以及其他許多背景工作。 GrapheneOS 不這麼做，他們通過讓作業系統與由其團隊所擁有的伺服器通信來完成上述工作，這些伺服器遵守他們的隱私權政策 這能向 [Google](.../basics/common-threats.md#privacy-from-service-providers) 隱藏您的資訊（例如：IP位置），但這意味著您的網路管理員或 ISP 的很容易看到您正在連線到 `grapheneos.network`、`grapheneos.org` 等，並推斷出您使用的作業系統。

如果您想要隱藏類似此類的資訊，以避免被您網路上或 ISP 上的對手發現，除了將連線檢查設定變更為 **Standard (Google)** 之外，您還 **必須** 使用 [可信賴的 VPN](../vpn.md)。 它可以在 :gear: **設定** → **網路與網際網路** → **Internet connectivity checks** 中找到. 此選項可讓您連線至 Google 伺服器進行連線檢查，加上 VPN 的使用，可協助您混入更多的 Android 裝置中。

### DivestOS

如果 GrapheneOS 與您的手機不相容，DivestOS 是一個很好的替代方案。 它支援各式各樣的手機，具有 _不同_ 等級的安全防護和品質控制。

<div class="admonition recommendation" markdown>

![DivestOS logo](../assets/img/android/divestos.svg){ align=right }

**DivestOS** 是一個 [LineageOS](https://lineageos.org) 的軟分叉。
DivestOS 從 LineageOS 繼承了許多 [支援的裝置](https://divestos.org/index.php?page=devices\&base=LineageOS) 。 它具有已簽名的構建，使其在某些非 Pixel 裝置上可以使用 [verified boot](../os/android-overview.md#verified-boot) 。 並非所有支援的裝置都支援驗證開機或其他安全功能。

[:octicons-home-16: 首頁](https://divestos.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="洋蔥服務" }
[:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title="文檔" }
[:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="原始碼" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title="捐款" }

</div>

特別是韌體更新的 [狀態](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) ，會因為您的手機型號不同而有很大的差異。 雖然標準的 AOSP Bug 和漏洞可以透過標準的軟體更新（例如 DivestOS 提供的更新）來修補，但有些漏洞在沒有裝置製造商支援的情況下是無法修補的，因此即使使用最新的替代 ROM（例如 DivestOS），產品壽命結束的裝置安全性也會降低。

DivestOS 具有自動核心漏洞 ([CVE](https://zh.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [修補](https://gitlab.com/divested-mobile/cve_checker)，更少的專有設備驅動程式，和自訂的 [hosts](https://divested.dev/index.php?page=dnsbl) 文件。 其加固的 WebView： [Mulch](https://gitlab.com/divested-mobile/mulch) ，可針對所有架構啟用 [控制流完整性](https://en.wikipedia.org/wiki/Control-flow_integrity) ，以及 [網路狀態分割](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) ，且接受 緊急更新 。

DivestOS 還包含來自GrapheneOS 的核心補丁，並透過 [defconfig 加固](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758) 啟用所有可用的核心安全功能。 所有高於3.4版本的核心都包含 整頁的[核心記憶體清理](https://lwn.net/Articles/334747) ，並且所有~22 Clang 編譯的核心都有啟用 [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) 。

DivestOS 也實現了一些最初專為 GrapheneOS 開發的系統加固補丁。 DivestOS 16.0 及更高版本實作了 GrapheneOS 的 `網路` 與 `傳感器` 權限切換、[加固的記憶體分配器](https://github.com/GrapheneOS/hardened_malloc)、[exec-spawning](https://grapheneos.org/usage#exec-spawning)、Java本地接口 [constification](https://zh.wikipedia.org/zh-tw/Const) 以及部分 [bionic](https://zh.wikipedia.org/zh-tw/Bionic_%28%E8%BB%9F%E9%AB%94%29) 加固補丁集。 17.1 及更高版本具備「根據每個網路完整的 MAC 位址隨機化」、[`ptrace_scope`](https://kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) 控制、自動重新開機，以及 Wi-Fi/Bluetooth [超時關閉選項](https://grapheneos.org/features#attack-surface-reduction) 。

DivestOS 使用 F-Droid 作為其預設應用程式商店。 我們通常 [建議避免使用 F-Droid](obtaining-apps.md#f-droid) ，但在 DivestOS 上這樣做是不可行的；開發人員透過自己的 F-Droid 儲存庫：[DivestOS Official](https://divestos.org/fdroid/official) 來更新他們的應用程式。 對於這些應用程式，您應該繼續使用 F-Droid ＋ **DivestOS 儲存庫** ，以保持這些元件為最新。 對於其他應用程式，我們推薦的 [應用程式獲取途徑](obtaining-apps.md) 仍然適用。

DivestOS 以替代服務取代 Android 與 Google 服務的許多背景網路連線，例如使用 OpenEUICC 來啟動 eSIM；使用 NTP.org 來設定網路時間；以及使用 Quad9 來設定 DNS。 這些連線可以修改，但它們與標準 Android 手機的網路連線不同，可能意味著您所使用的網路中的對手更容易推測出您手機上安裝的作業系統。 如果您擔心這一點，請考慮使用 [受信任的 VPN](../vpn.md) 並啟用本機 VPN [kill switch](../os/android-overview.md#vpn-killswitch) 來對您的本機網路和 ISP 隱藏此網路流量。

## 標準

**請注意，我們與所推薦專案沒有任何瓜葛。** 除了 [我們的標準準則](../about/criteria.md) 外，還有一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- 必須是開源軟體。
- 必須支援引導裝載程式鎖定且其必須允許使用自訂 AVB 金鑰簽名。
- 必須在 主要 Android 更新 發布後 0-1 個月內收到更新。
- 必須在 Android 功能更新（小版本）發布後 0-14 天內收到更新。
- 必須在定期安全修補補丁發布後 0-5 天內收到更新。
- **不可** 在預設情況下 "rooted" 。
- **不可** 在預設情況下安裝 Google Play 服務 。
- **不可** 透過修改系統支援 Google Play 服務 。
