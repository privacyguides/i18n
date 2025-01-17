---
meta_title: "Blockchains de criptomoedas privadas - Privacy Guides"
description: Unlike most cryptocurrencies, these ones provide transaction privacy by default. Monero is our top choice for obfuscating transaction information.
title: Criptomoedas
icon: material/bank-circle
cover: cryptocurrency.webp
---

<small>Protects against the following threat(s):</small>

- [:material-eye-outline: Mass Surveillance](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

Fazer pagamentos “on-line” é um dos maiores desafios à privacidade. Essas criptomoedas oferecem privacidade nas transações por padrão (algo que **não** é garantido pela maioria das criptomoedas), desde que você tenha um bom conhecimento de como fazer pagamentos privados de forma eficaz. Recomendamos fortemente que você leia primeiro nosso artigo de visão geral sobre pagamentos antes de fazer qualquer compra:

[Fazendo Pagamentos Privados :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

<div class="admonition danger" markdown>
<p class="admonition-title">Aviso</p>

Many if not most cryptocurrency projects are scams. Make transactions carefully with only projects you trust.

</div>

## Monero

<div class="admonition recommendation" markdown>

![Monero logo](assets/img/cryptocurrency/monero.svg){ align=right }

**Monero** uses a blockchain with privacy-enhancing technologies that obfuscate transactions to achieve [:material-incognito: Anonymity](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }. Every Monero transaction hides the transaction amount, sending and receiving addresses, and source of funds without any hoops to jump through, making it an ideal choice for cryptocurrency novices.

[:octicons-home-16: Homepage](https://getmonero.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://getmonero.org/resources/user-guides){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Source Code" }
[:octicons-heart-16:](https://getmonero.org/get-started/contributing){ .card-link title=Contribute }

</details>

</div>

Com o Monero, observadores externos não podem decifrar endereços que negociam Monero, valores de transações, saldos de endereços ou históricos de transações.

<details class="info" markdown>
<summary>Monero's resilience to mass surveillance</summary>

In August 2021, CipherTrace [announced](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) enhanced Monero tracing capabilities for government agencies. Postagens públicas mostram que o Departamento da Rede de Execução de Crimes Financeiros do Tesouro dos EUA [licenciou](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) Módulo "Monero Trace" da CipherTrace no final de 2022.

A privacidade do gráfico de transações do Monero é limitada por suas assinaturas de anel relativamente pequenas, especialmente contra ataques direcionados. Os recursos de privacidade do Monero também foram [questionados](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) por alguns pesquisadores de segurança, e várias vulnerabilidades graves foram encontradas e corrigidas no passado, de modo que as alegações feitas por organizações como a CipherTrace não estão fora de questão. Embora seja improvável que existam ferramentas de vigilância em massa do Monero como existem para o Bitcoin e outros, é certo que as ferramentas de rastreamento ajudam nas investigações direcionadas.

Em última análise, o Monero é o mais forte candidato a uma criptomoeda favorável à privacidade, mas suas alegações de privacidade **não** foram definitivamente comprovadas de uma forma ou de outra. É necessário mais tempo e pesquisa para avaliar se o Monero é suficientemente resistente a ataques para sempre proporcionar a privacidade adequada.

</details>

### Monero wallets

For optimal privacy, make sure to use a self-custody wallet where the [view key](https://www.getmonero.org/resources/moneropedia/viewkey.html) stays on the device. Isso significa que somente você poderá gastar seus fundos e ver as transações de entrada e saída. If you use a custodial wallet, the provider can see **everything** you do; if you use a “lightweight” wallet where the provider retains your view key, the provider can see almost everything you do (but not spend your funds). Some self-custody wallets where the view key does not leave your device include:

- [Cliente oficial do Monero](https://getmonero.org/downloads) (Desktop)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, Desktop)
    - Cake Wallet supports multiple cryptocurrencies. A Monero-only version of Cake Wallet for iOS and Android is available at [Monero.com](https://monero.com).
- [Carteira Feather](https://featherwallet.org) (Desktop)
- [Monerujo](https://monerujo.io) (Android)

### Monero nodes

For maximum privacy (even with a self-custody wallet), you should run your own Monero node called the [Monero daemon](https://getmonero.org/downloads/#cli). O uso do nó de outra pessoa exporá algumas informações a ela, como o endereço IP a partir do qual você se conecta a ele, os carimbos de data e hora em que você sincroniza sua carteira e as transações que você envia de sua carteira (embora não haja outros detalhes sobre essas transações). Alternatively, you can connect to someone else’s Monero node over Tor, [I2P](alternative-networks.md#i2p-the-invisible-internet-project), or a VPN.

### Buying Monero

[General tips for acquiring Monero](advanced/payments.md#acquisition ""){.md-button}

There are numerous centralized exchanges (CEX) as well as P2P marketplaces where you can buy and sell Monero. Some of them require identifying yourself (KYC) to comply with anti-money laundering regulations. However, due to Monero's privacy features, the only thing known to the seller is _that_ you bought Monero, but not how much you own or where you spend it (after it leaves the exchange). Some reputable places to buy Monero include:

- [Kraken](https://kraken.com): A well-known CEX. Registration and KYC are mandatory. Card payments and bank transfers accepted. Make sure not to leave your newly purchased Monero on Kraken's platform after the purchase; withdraw them to a self-custody wallet. Monero is not available in all jurisdictions that Kraken operates in.[^1]
- [Cake Wallet](https://cakewallet.com): A self-custody cross-platform wallet for Monero and other cryptocurrencies. You can buy Monero directly in the app using card payments or bank transfers (through third-party providers such as [Guardarian](https://guardarian.com) or [DFX](https://dfx.swiss)).[^2] KYC is usually not required, but it depends on your country and the amount you are purchasing. In countries where directly purchasing Monero is not possible, you can also use a provider within Cake Wallet to first buy another cryptocurrency such as Bitcoin, Bitcoin Cash, or Litecoin and then exchange it to Monero in-app.
    - [Monero.com](https://monero.com) is an associated website where you can buy Monero and other cryptocurrencies without having to download an app. The funds will simply be sent to the wallet address of your choice.
- [RetoSwap](https://retoswap.com) (formerly known as Haveno-Reto) is a self-custody, decentralized P2P exchange platform based on the [Haveno](https://haveno.exchange) project which is available for Linux, Windows, and macOS. Monero can be bought and sold with maximum privacy, since most trading counterparties do not require KYC, trades are made directly between users (P2P), and all connections run through the Tor network. It is possible to buy Monero via bank transfer, Paypal, or even by paying in cash (meeting in person or sending by mail). Arbitrators can step in to resolve disputes between buyer and seller, but be careful when sharing your bank account or other sensitive information with your trading counterparty. Trading with some accounts may be against those accounts' terms of service.

## Critérios

**Por favor, note que não somos parceiros de nenhum dos produtos que recomendamos.**Em adição aos[nossos critérios básicos](about/criteria.md), desenvolvemos um conjunto claro de requisitos para nos permitir fornecer recomendações objetivas. Recomendamos que você se familiarize com esta lista antes de escolher usar um produto, e que faça sua própria pesquisa para garantir que o produto escolhido é o ideal para você.

- A criptomoeda deve fornecer transações privadas/não rastreáveis por padrão.

<div class="admonition tip" markdown>
<p class="admonition-title">Important notices</p>

The content here is not legal or financial advice. We do not endorse or encourage illicit activities, and we do not endorse or encourage anything which violates a company's terms of service. Check with a professional to confirm that these recommendations are legal and available in your jurisdiction. [See all notices](about/notices.md).

</div>

[^1]: You may refer to the following pages for up-to-date information on countries in which Kraken does **not** allow the purchase of Monero: [Where is Kraken licensed or regulated?](https://support.kraken.com/hc/en-us/articles/where-is-kraken-licensed-or-regulated) and [Support for Monero (XMR) in Europe](https://support.kraken.com/hc/en-us/articles/support-for-monero-xmr-in-europe).
[^2]: You may refer to the following pages for up-to-date information on countries in which Cake Wallet and Monero.com **only** allow the direct purchase of Monero (through third-party providers): [Which countries are served by DFX?](https://docs.dfx.swiss/en/faq.html#which-countries-are-served-by-dfx) and [What are the supported countries/regions? (Guardarian)](https://guardarian.freshdesk.com/support/solutions/articles/80001151826-what-are-the-supported-countries-regions).
