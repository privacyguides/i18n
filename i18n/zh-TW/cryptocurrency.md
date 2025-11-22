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
<summary>門羅幣對大規模監控的抵抗力</summary>

2021 年 8 月，CipherTrace [宣佈](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) 為政府機構提供更強的Monero 追蹤能力。 公開貼文顯示，美國財政部金融犯罪執法網路於 2022 年底 [授權](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) CipherTrace 的「Monero 模塊」。

Monero 交易圖隱私受到其相對較小的環形簽名的限制，特別是抵抗針對性的攻擊。 Monero 的隱私功能也曾被某些資安研究人員 [質疑](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) ，過去也曾發現一些嚴重的漏洞（已被修補），因此如 CipherTrace 的宣稱並非不可能。 雖然 Monero 大規模監控工具不太可能像比特幣和其他工具一樣存在，但可以肯定的是，追蹤工具有助於進行針對性的調查。

Monero 是隱私友好的加密貨幣中最強大的競爭者，但它的隱私聲稱**尚未**被任何方式證明 。 需要更多的時間和研究來評估 Monero 是否足夠抵禦攻擊來提供足夠的隱私。

</details>

### 門羅幣錢包

為了確保最佳的隱私，請務必使用自行保管的錢包，其中[檢視金鑰](https://getmonero.org/resources/moneropedia/viewkey.html)將會保留在裝置上。 這意味著只有您能夠花費資金並查看交易進出。 若使用託管錢包，則服務提供商可看到您的**所有操作**；若使用的是「輕量」錢包，則服務提供商會儲存您的檢視金鑰，並能看到您幾乎所有的操作（但無法動用您的資金）。 一些檢視金鑰不會離開您的裝置的自行保管錢包包含了：

- [官方Monero客戶端](https://getmonero.org/downloads) （桌面）
- [Cake Wallet](https://cakewallet.com)（iOS、Android、桌面）
    - Cake Wallet 支援多種加密貨幣。 適用於 iOS 和 Android 的 Monero專用版 Cake Wallet 可在 [Monero.com](https://monero.com) 網站下載。
- [Feather Wallet](https://featherwallet.org) (桌面版)
- [Monerujo](https://monerujo.io) (Android)

### 門羅幣節點

為了確保最佳的隱私（即使使用自行保管的錢包），您應該執行自己的門羅幣節點（稱為 [Monero daemon](https://docs.getmonero.org/interacting/monerod-reference)，包含在[命令列錢包](https://getmonero.org/downloads/#cli)中）。 使用別人的節點會暴露一些信息，例如您從中連接到它的IP位址，同步錢包的時間戳記以及您從錢包發送的交易（儘管沒有關於這些交易的其他細節）。 另外，您也可以透過 [Tor](alternative-networks.md#tor)、[I2P](alternative-networks.md#tor) 或 [VPN](vpn.md) 連線到其他人的門羅幣節點。

### 購買門羅幣

[取得門羅幣的一般建議](advanced/payments.md#acquisition ""){.md-button}

有許多集中式交易所 (CEX) 以及 P2P 市場可以買賣門羅幣。 其中有些需要驗證身份 (KYC)，以符合反洗錢法規。 然而，由於門羅幣的隱私特性，賣方唯一能知曉*的*是您買了門羅幣，但不知道您擁有多少或在哪裡花掉它（在它離開交易所後）。 購買門羅幣的可靠管道包含：

- [Kraken](https://kraken.com)：知名的 CEX。 必須註冊與 KYC。 接受卡片付款與銀行轉帳。 購買後，請確保不要將您剛購買的門羅幣留在 Kraken 的平台上，請將其提款到自行保管的錢包中。 門羅幣並非在所有 Kraken 營運的所有司法管轄區均可使用。[^1]
- [Cake Wallet](https://cakewallet.com)：門羅幣與其他加密貨幣的自行保管跨平台錢包。 您可以直接在應用程式中使用卡片付款或銀行轉帳（透過 [Guardarian](https://guardarian.com) 或 [DFX](https://dfx.swiss) 等第三方供應商）購買門羅幣。[^2] 通常不需要 KYC，但這取決於您所在的國家與購買的金額。 在無法直接購買門羅幣的國家，您也可以使用 Cake Wallet 內的提供者先購買其他加密貨幣，例如比特幣、比特幣現金或萊特幣，然後在應用程式中將其兌換為門羅幣。
    - [Monero.com](https://monero.com) 是一個合作網站，您可以在該網站購買門羅幣及其他加密貨幣，無需下載應用程式。 資金將直接傳送到您指定的錢包地址。
- [RetoSwap](https://retoswap.com)（前身為 Haveno-Reto）是以 [Haveno](https://haveno.exchange) 專案為基礎開發的自行保管、去中心化 P2P 交換平台，適用於 Linux、Windows 與 macOS。 由於大多數交易對手不要求 KYC，交易直接在使用者之間進行 (P2P)，且所有連線都透過 Tor 網路處理，因此可以最大程度保障買賣門羅幣的隱私。 您可以透過銀行轉帳、PayPal，甚至是現金付款（親自會面或郵寄）的方式購買門羅幣。 仲裁人可介入解決買賣雙方之間的爭議，但與交易對手分享銀行帳號或其他敏感資訊時務必謹慎。 與某些帳號進行交易可能會違反這些帳號的服務條款。

## 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- 預設情況下，加密貨幣必須提供私密/無法追蹤的交易。

<div class="admonition tip" markdown>
<p class="admonition-title">重要聲明</p>

此處的內容並非法律或財務建議。 我們不贊同或鼓勵非法活動，也不贊同或鼓勵任何違反公司服務條款的行為。 請向專業人員查詢，確認這些建議在您的司法管轄區是否合法和可用。 [檢視所有聲明](about/notices.md)。

</div>

[^1]: 您可以參閱以下頁面，了解 Kraken **不**允許購買門羅幣的國家的最新資訊：[Kraken 在哪些地區獲得許可或受監管？](https://support.kraken.com/hc/en-us/articles/where-is-kraken-licensed-or-regulated)與[在歐洲對門羅幣 (XMR) 的支援](https://support.kraken.com/hc/en-us/articles/support-for-monero-xmr-in-europe)。
[^2]: 您可以參閱以下頁面，了解 Cake Wallet 與 Monero.com **僅**允許直接購買門羅幣（透過第三方供應商）的國家的最新資訊：[DFX 在哪些國家提供服務？](https://docs.dfx.swiss/en/faq.html#which-countries-are-served-by-dfx)與[支援哪些國家/地區？](https://guardarian.freshdesk.com/support/solutions/articles/80001151826-what-are-the-supported-countries-regions) (Guardarian)</a>.
