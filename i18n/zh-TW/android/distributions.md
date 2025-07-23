---
meta_title: "最佳 Android 作業系統 - Privacy Guides"
title: "替代作業系統"
description: 您可以使用這些安全且尊重隱私的替代方案來取代 Android 手機上的作業系統。
schema:
  - "@context": http://schema.org
    "@type": 網頁
    name: 尊重隱私的 Android 作業系統
    url: "./"
  - "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": 網頁
      url: "./"
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>防護下列威脅：</small>

- [:material-target-account: 針對性攻擊](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: 被動攻擊](../basics/common-threats.md#security-and-privacy){ .pg-orange }

**基於 Android 的自訂作業系統** (有時也稱為 **自訂 ROM**)，可以讓您的裝置擁有更高層級的隱私與安全性。 這與出廠時隨手機附送的「原廠 (stock)」Android 形成對比，「原廠」Android 通常與 Google Play 服務及其他供應商軟體深度整合。

如果您擁有 Google Pixel，我們建議您安裝 GrapheneOS，因為它提供了更高的安全性和額外的隱私功能。 我們不列出其他作業系統或裝置的原因如下：

- 它們通常具有 [較弱的安全性](index.md#install-a-custom-distribution)。
- 當維護者失去興趣或升級他們的裝置時，經常會導致支援中止，這與 GrapheneOS 所遵循的可預測 [支援週期](https://grapheneos.org/faq#device-lifetime) 形成對比。
- 它們通常在隱私或安全性改善方面少有建樹，因此不值得安裝。

## GrapheneOS

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

預設情況下，Android 會與 Google 進行許多網路連線，以執行 DNS 連線檢查、同步目前的網路時間、檢查您的網路連線，以及其他許多背景工作。 GrapheneOS 不這麼做，他們通過讓作業系統與由其團隊所擁有的伺服器通訊來完成上述工作，這些伺服器遵守他們的隱私權政策 這能向 [Google](.../basics/common-threats.md#privacy-from-service-providers) 隱藏您的資訊（例如：IP位置），但這意味著您的網路管理員或 ISP 的很容易看到您正在連線到 `grapheneos.network`、`grapheneos.org` 等，並推斷出您使用的作業系統。

如果您想要隱藏類似此類的資訊，以避免被您網路上或 ISP 上的對手發現，除了將連線檢查設定變更為 **Standard (Google)** 之外，您還 **必須** 使用 [可信賴的 VPN](../vpn.md)。 連線檢查設定可以在 :gear: **設定** → **網路與網際網路** → **Internet connectivity checks** 中找到。 此選項可讓您連線至 Google 伺服器進行連線檢查，加上 VPN 的使用，可協助您混入更多的 Android 裝置中。

## 標準

**請注意，我們與推薦的任何項目均無關。** 除了 [我們的通用標準](../about/criteria.md) 外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- 必須是開源軟體。
- 必須支援引導裝載程式鎖定且其必須允許使用自訂 AVB 金鑰簽名。
- 必須在 主要 Android 更新 發布後 0-1 個月內收到更新。
- 必須在 Android 功能更新（小版本）發布後 0-14 天內收到更新。
- 必須在定期安全修補補丁發布後 0-5 天內收到更新。
- **不可** 在預設情況下 "rooted" 。
- **不可** 在預設情況下安裝 Google Play 服務 。
- **不可** 透過修改系統支援 Google Play 服務 。
