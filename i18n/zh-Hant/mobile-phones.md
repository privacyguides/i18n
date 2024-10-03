---
title: 手機
icon: material/cellphone-check
description: 這些行動裝置為客製化 Android 作業系統提供最佳的硬體安全支援。
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": 網頁
    name: 手機推薦
    url: ./
  - "@context": http://schema.org
    "@type": 產品
    name: Pixel
    brand:
      "@type": 品牌
      name: Google
    image: /assets/img/android/google-pixel.png
    sameAs: https://zh.wikipedia.org/wiki/Google_Pixel
    review:
      "@type": 評論
      author:
        "@type": 組織
        name: Privacy Guides
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>防護下列威脅：</small>

- [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy){ .pg-orange }

大多數的**手機**都會從 OEM 收到短期或有限的安全更新；在這些裝置的支援期結束後，它們就不會再收到韌體或驅動程式的安全更新，因此**不能**被視為是安全的。

此處列出的行動裝置可提供長壽命的保證安全更新，並允許您安裝自訂作業系統，而不會違反 Android 安全模型。

[推薦的客製化作業系統 :material-arrow-right-drop-circle:](android/distributions.md){ .md-button .md-button--primary } [Android 安全性詳細資訊 :material-arrow-right-drop-circle:](os/android-overview.md#security-protections){ .md-button }

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

由於 OEM 終止支援，生命週期結束的裝置 (例如 GrapheneOS 的「延伸支援」裝置) 並沒有完整的安全修補程式 (韌體更新)。 無論是否安裝軟體，這些裝置都不能視為完全安全。

</div>

## 採購建議

購買裝置時，我們建議盡可能購買全新的裝置。 行動裝置的軟體和韌體只能支援一段有限的時間，因此購買新裝置可以儘可能延長使用期限。

避免向行動網路業者購買手機。 這些產品通常具有**鎖定的開機載入程式**，且不支援 [OEM 解鎖](https://source.android.com/devices/bootloader/locking_unlocking)。 這些有差異的手機會阻止您安裝任何類型的替代 Android 發行套件。

從線上購物購買二手手機時要非常**小心**。 務必檢查賣家的聲譽。 如果裝置被盜，就有可能被輸入 [IMEI 資料庫](https://gsma.com/get-involved/working-groups/terminal-steering-group/imei-database)。 您與前一位持有者的活動有關聯也會有風險。

更多關於 Android 裝置和作業系統相容性的提示：

- 請勿購買已達使用期限或接近使用期限的裝置；製造商必須提供額外的韌體更新。
- 請勿購買預載的 LineageOS 或 /e/ OS 手機，或任何沒有適當 [驗證開機](https://source.android.com/security/verifiedboot) 支援和韌體更新的 Android 手機。 這些裝置也無法讓您檢查它們是否被竄改過。
- 簡而言之，如果這裡沒有列出裝置，可能是有充分理由的。 查看我們的 [論壇](https://discuss.privacyguides.net) 以瞭解詳細資訊！

## Google Pixel

Google Pixel 手機是我們**唯一**推薦購買的裝置。 Pixel 手機擁有比目前市面上其他 Android 裝置更強的硬體安全性，這是由於第三方作業系統有適當的 AVB 支援，以及 Google 的客製化 [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) 安全晶片扮演安全元件的角色。

<div class="admonition recommendation" markdown>

![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }

眾所周知，**Google Pixel** 裝置具有良好的安全性，即使在安裝自訂作業系統時，也能正確支援 [驗證開機](https://source.android.com/security/verifiedboot)。

從 **Pixel 8** 和 **8 Pro** 開始，Pixel 裝置將獲得至少 7 年的保證安全更新，相較於競爭 OEM 通常提供的 2-5 年，可確保更長的使用壽命。

[:material-shopping: 商店](https://store.google.com/category/phones){ .md-button .md-button--primary }

</div>

Titan M2 之類的安全元件比其他大多數手機所使用的處理器可信執行環境更為有限，因為它們僅用於機密儲存、硬體驗證和速率限制，而非執行「可信賴」的程式。 沒有安全元件的手機必須使用 TEE 來執行**所有**這些功能，因此會產生較大的攻擊面。

Google Pixel 手機使用的 TEE OS 名為 Trusty，與許多其他手機不同，它是[開放原始碼](https://source.android.com/security/trusty#whyTrusty)的。

使用他們的 [線上安裝程式](https://grapheneos.org/install/web)，在 Pixel 手機上安裝 GrapheneOS 非常簡單。 如果您不習慣自己動手，又願意多花一點錢，可以看看 [NitroPhone](https://shop.nitrokey.com/shop)，因為它們預載了來自聲譽良好的 [Nitrokey](https://nitrokey.com/about) 公司的 GrapheneOS。

還有一些購買 Google Pixel 的小提醒：

- 如果您想以便宜的價格購買 Pixel 裝置，我們建議您購買「**a**」機型，就在下一款旗艦機發表之後。 通常都會有折扣，因為 Google 要清理庫存。
- 考慮實體商店提供的價格優惠方案和特價商品。
- 查看您所在國家或地區的線上社群特價網站。 這些都可以提醒您有好的入手價格。
- Google 提供了一份清單，顯示每部裝置的 [支援週期](https://support.google.com/nexus/answer/4457705)。 裝置的每日價格可計算為 <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline" class="tml-display" style="display:inline math;"> <mfrac> <mtext>成本</mtext> <mrow> <mtext>壽命結束日期</mtext> <mo>-</mo> <mtext>目前日期</mtext> </mrow> </mfrac> </math>
  這表示裝置使用時間越長，每天的成本就越低。
- 如果您所在的地區沒有 Pixel，[NitroPhone](https://shop.nitrokey.com/shop) 可以全球配送。

## 標準

\*\*請注意，我們與推薦的任何專案都沒有任何關係。\*\*除了 [我們的標準準則](about/criteria.md)之外，我們還制定了一套明確的要求，讓我們能夠提供客觀的推薦。 我們建議您在選擇使用專案前先熟悉此清單，並自行研究，以確保它是適合您的選擇。

- 必須支援至少一種我們推薦的客製化作業系統。
- 必須是目前店內銷售的全新產品。
- 必須接受至少 5 年的安全更新。
- 必須有專用的安全元件硬體。
