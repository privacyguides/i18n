---
meta_title: "私密加密貨幣區塊鏈 - Privacy Guides"
description: 與大多數加密貨幣不同，這些貨幣預設提供交易隱私。 Monero 是我們混淆交易資訊的首選。
title: 加密貨幣
icon: material/bank-circle
cover: cryptocurrency.webp
---

<small>防護下列威脅：</small>

- [:material-eye-outline: 大規模監控](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: 審查](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

線上支付是隱私面臨的最大挑戰之一。 下列加密貨幣預設提供交易隱私（大多數加密貨幣**並未保證**如此 ），前提是您對如何有效地進行私人支付有深入了解。 我們強烈建議您在網路購買前先閱讀本站私密付款之介紹：

[私密付款 :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

<div class="admonition danger" markdown>
<p class="admonition-title">Danger "危險"</p>

許多（如果不是大多數）加密貨幣項目都是騙局。 只用您信任的項目小心進行交易。

</div>

## Monero

<div class="admonition recommendation" markdown>

![Monero logo](assets/img/cryptocurrency/monero.svg){ align=right }

**Monero** 使用具有隱私增強技術的區塊鏈來混淆交易，以實現 [:material-incognito: 匿名](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }。 每筆 Monero 交易都隱藏了交易金額、發送和接收地址以及資金來源，使其成為加密貨幣新手的理想選擇。

[:octicons-home-16: Homepage](https://getmonero.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://getmonero.org/resources/user-guides){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Source Code" }
[:octicons-heart-16:](https://getmonero.org/get-started/contributing){ .card-link title=Contribute }

</details>

</div>

使用 Monero ，外部觀察者無法破譯 Monero  交易地址、交易金額、地址餘額或交易歷史。

為了獲得最佳的隱私，請務必使用非保管錢包，讓查看密鑰保留在設備上。 這意味著只有您能夠花費資金並查看交易進出。 若使用託管錢包，則服務商可看到**全部活動** ；如果用的是"輕量"錢包，則服務商保存了您的私鑰並看到您全部的交易活動。 一些非保管錢包包括：

- [官方Monero客戶端](https://getmonero.org/downloads) （桌面）
- [Cake Wallet](https://cakewallet.com) (iOS, Android, macOS)
    - Cake Wallet 支援多種加密貨幣。 適用於 iOS 和 Android 的 Monero專用版 Cake Wallet 可在 [Monero.com](https://monero.com) 網站下載。
- [Feather Wallet](https://featherwallet.org) (桌面版)
- [Monerujo](https://monerujo.io) (Android)

為了獲得最大的隱私（即便使用非保管錢包），您應該運行自己的 Monero 節點。 使用別人的節點會暴露一些信息，例如您從中連接到它的IP位址，同步錢包的時間戳記以及您從錢包發送的交易（儘管沒有關於這些交易的其他細節）。 另外，您也可以透過 Tor 或 [I2P](alternative-networks.md#i2p-the-invisible-internet-project) 連接到其他人的 Monero 節點。

2021 年 8 月，CipherTrace [宣佈](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) 為政府機構提供更強的Monero 追蹤能力。 公開貼文顯示，美國財政部金融犯罪執法網路於 2022 年底 [授權](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) CipherTrace 的「Monero 模塊」。

Monero 交易圖隱私受到其相對較小的環形簽名的限制，特別是抵抗針對性的攻擊。 Monero's 隱私功能也曾被某些資安研究人員 [質疑](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) ，過去已發現一些弱點與補丁，因此如 CipherTrace 的宣稱並非不可能。 雖然 Monero 大規模監控工具不太可能像比特幣和其他工具一樣存在，但可以肯定的是，追蹤工具有助於進行針對性的調查。

Monero 是隱私友好的加密貨幣中最強大的競爭者，但它的隱私聲稱**尚未**被任何方式證明 。 需要更多的時間和研究來評估 Monero 是否足夠抵禦攻擊來提供足夠的隱私。

## 標準

**請注意，我們與所推薦專案沒有任何牽扯。 ** 除了 [我們的標準準則](about/criteria.md)外，還有一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- 預設情況下，加密貨幣必須提供私密/無法追蹤的交易。
