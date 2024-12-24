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

<details class="info" markdown>
<summary>Monero's resilience to mass surveillance</summary>

2021 年 8 月，CipherTrace [宣佈](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) 為政府機構提供更強的Monero 追蹤能力。 公開貼文顯示，美國財政部金融犯罪執法網路於 2022 年底 [授權](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) CipherTrace 的「Monero 模塊」。

Monero 交易圖隱私受到其相對較小的環形簽名的限制，特別是抵抗針對性的攻擊。 Monero 的隱私功能也曾被某些資安研究人員 [質疑](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) ，過去也曾發現一些嚴重的漏洞（已被修補），因此如 CipherTrace 的宣稱並非不可能。 雖然 Monero 大規模監控工具不太可能像比特幣和其他工具一樣存在，但可以肯定的是，追蹤工具有助於進行針對性的調查。

Monero 是隱私友好的加密貨幣中最強大的競爭者，但它的隱私聲稱**尚未**被任何方式證明 。 需要更多的時間和研究來評估 Monero 是否足夠抵禦攻擊來提供足夠的隱私。

</details>

### Monero wallets

For optimal privacy, make sure to use a self-custody wallet where the [view key](https://www.getmonero.org/resources/moneropedia/viewkey.html) stays on the device. 這意味著只有您能夠花費資金並查看交易進出。 If you use a custodial wallet, the provider can see **everything** you do; if you use a “lightweight” wallet where the provider retains your view key, the provider can see almost everything you do (but not spend your funds). Some self-custody wallets where the view key does not leave your device include:

- [官方Monero客戶端](https://getmonero.org/downloads) （桌面）
- [Cake Wallet](https://cakewallet.com) (iOS, Android, Desktop)
    - Cake Wallet 支援多種加密貨幣。 適用於 iOS 和 Android 的 Monero專用版 Cake Wallet 可在 [Monero.com](https://monero.com) 網站下載。
- [Feather Wallet](https://featherwallet.org) (桌面版)
- [Monerujo](https://monerujo.io) (Android)

### Monero nodes

For maximum privacy (even with a self-custody wallet), you should run your own Monero node called the [Monero daemon](https://getmonero.org/downloads/#cli). 使用別人的節點會暴露一些信息，例如您從中連接到它的IP位址，同步錢包的時間戳記以及您從錢包發送的交易（儘管沒有關於這些交易的其他細節）。 Alternatively, you can connect to someone else’s Monero node over Tor, [I2P](alternative-networks.md#i2p-the-invisible-internet-project), or a VPN.

### Buying Monero

[General tips for acquiring Monero](advanced/payments.md#acquisition ""){.md-button}

There are numerous centralized exchanges (CEX) as well as P2P marketplaces where you can buy and sell Monero. Some of them require identifying yourself (KYC) to comply with anti-money laundering regulations. However, due to Monero's privacy features, the only thing known to the seller is _that_ you bought Monero, but not how much you own or where you spend it (after it leaves the exchange). Some reputable places to buy Monero include:

- [Kraken](https://kraken.com): A well-known CEX. Registration and KYC are mandatory. Card payments and bank transfers accepted. Make sure not to leave your newly purchased Monero on Kraken's platform after the purchase; withdraw them to a self-custody wallet. Monero is not available in all jurisdictions that Kraken operates in.[^1]
- [Cake Wallet](https://cakewallet.com): A self-custody cross-platform wallet for Monero and other cryptocurrencies. You can buy Monero directly in the app using card payments or bank transfers (through third-party providers such as [Guardarian](https://guardarian.com) or [DFX](https://dfx.swiss)).[^2] KYC is usually not required, but it depends on your country and the amount you are purchasing. In countries where directly purchasing Monero is not possible, you can also use a provider within Cake Wallet to first buy another cryptocurrency such as Bitcoin, Bitcoin Cash, or Litecoin and then exchange it to Monero in-app.
    - [Monero.com](https://monero.com) is an associated website where you can buy Monero and other cryptocurrencies without having to download an app. The funds will simply be sent to the wallet address of your choice.
- [RetoSwap](https://retoswap.com) (formerly known as Haveno-Reto) is a self-custody, decentralized P2P exchange platform based on the [Haveno](https://haveno.exchange) project which is available for Linux, Windows, and macOS. Monero can be bought and sold with maximum privacy, since most trading counterparties do not require KYC, trades are made directly between users (P2P), and all connections run through the Tor network. It is possible to buy Monero via bank transfer, Paypal, or even by paying in cash (meeting in person or sending by mail). Arbitrators can step in to resolve disputes between buyer and seller, but be careful when sharing your bank account or other sensitive information with your trading counterparty. Trading with some accounts may be against those accounts' terms of service. Please note that you can only buy Monero on RetoSwap if you already own a small amount of Monero (currently a minimum of 0.11 XMR) in order to fund security deposits, although there are ongoing efforts to drop this requirement in the future.

## 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- 預設情況下，加密貨幣必須提供私密/無法追蹤的交易。

<div class="admonition tip" markdown>
<p class="admonition-title">Important notices</p>

The content here is not legal or financial advice. We do not endorse or encourage illicit activities, and we do not endorse or encourage anything which violates a company's terms of service. Check with a professional to confirm that these recommendations are legal and available in your jurisdiction. [See all notices](about/notices.md).

</div>

[^1]: You may refer to the following pages for up-to-date information on countries in which Kraken does **not** allow the purchase of Monero: [Where is Kraken licensed or regulated?](https://support.kraken.com/hc/en-us/articles/where-is-kraken-licensed-or-regulated) and [Support for Monero (XMR) in Europe](https://support.kraken.com/hc/en-us/articles/support-for-monero-xmr-in-europe).
[^2]: You may refer to the following pages for up-to-date information on countries in which Cake Wallet and Monero.com **only** allow the direct purchase of Monero (through third-party providers): [Which countries are served by DFX?](https://docs.dfx.swiss/en/faq.html#which-countries-are-served-by-dfx) and [What are the supported countries/regions? (Guardarian)](https://guardarian.freshdesk.com/support/solutions/articles/80001151826-what-are-the-supported-countries-regions).
