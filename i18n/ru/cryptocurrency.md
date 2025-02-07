---
meta_title: "Private Cryptocurrency Blockchains - Privacy Guides"
description: Unlike most cryptocurrencies, these ones provide transaction privacy by default. Monero is our top choice for obfuscating transaction information.
title: Криптовалюта
icon: material/bank-circle
cover: cryptocurrency.webp
---

<small>Protects against the following threat(s):</small>

- [:material-eye-outline: Массовое наблюдение](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Цензура](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

Платежи в интернете - одна из самых серьезных проблем, связанных с конфиденциальностью. Эти криптовалюты по умолчанию обеспечивают конфиденциальность транзакций (что **не** гарантируется большинством криптовалют), при условии, что вы хорошо понимаете, как эффективно осуществлять приватные платежи. Мы настоятельно рекомендуем вам сначала прочитать нашу обзорную статью о платежах, прежде чем совершать какие-либо покупки:

[Совершение приватных платежей :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Многие, если не большинство, криптовалютных проектов - это мошеннические схемы. Осуществляйте транзакции осторожно, используя только те проекты, которым вы доверяете.

</div>

## Monero

<div class="admonition recommendation" markdown>

![Monero logo](assets/img/cryptocurrency/monero.svg){ align=right }

**Monero** uses a blockchain with privacy-enhancing technologies that obfuscate transactions to achieve [:material-incognito: Anonymity](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }. Каждая транзакция в Monero скрывает сумму транзакции, адреса отправителя и получателя и источник средств, не требуя при этом дополнительных действий, что делает её идеальным выбором для новичков в области криптовалют.

[:octicons-home-16: Homepage](https://getmonero.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://getmonero.org/resources/user-guides){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Source Code" }
[:octicons-heart-16:](https://getmonero.org/get-started/contributing){ .card-link title=Contribute }

</details>

</div>

С помощью Monero сторонние наблюдатели не могут расшифровать адреса, которые обмениваются Monero, суммы транзакций, балансы адресов или историю транзакций.

<details class="info" markdown>
<summary>Monero's resilience to mass surveillance</summary>

In August 2021, CipherTrace [announced](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) enhanced Monero tracing capabilities for government agencies. Публичные сообщения показывают, что сеть по борьбе с финансовыми преступлениями министерства финансов США [лицензировала](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) "модуль Monero" CipherTrace в конце 2022 года.

Конфиденциальность графа транзакций Monero ограничена его относительно небольшими кольцевыми подписями, особенно против персональных атак. Monero's privacy features have also been [called into question](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) by some security researchers, and a number of severe vulnerabilities have been found and patched in the past, so the claims made by organizations like CipherTrace are not out of the question. Хотя маловероятно, что существуют инструменты массового наблюдения за Monero, как это происходит с Bitcoin и другими криптовалютами, несомненно инструменты отслеживания помогают проводить персональные расследования.

В конечном итоге Monero является самым сильным претендентом на звание криптовалюты, обеспечивающей конфиденциальность, но ее заявления о конфиденциальности **не** были окончательно доказаны тем или иным способом. Необходимо больше времени и исследований, чтобы оценить, достаточно ли устойчива Monero к атакам, чтобы всегда обеспечивать достаточную конфиденциальность.

</details>

### Monero wallets

For optimal privacy, make sure to use a self-custody wallet where the [view key](https://www.getmonero.org/resources/moneropedia/viewkey.html) stays on the device. Это означает то, что только вы будете иметь возможность расходовать свои средства и видеть входящие и исходящие транзакции. If you use a custodial wallet, the provider can see **everything** you do; if you use a “lightweight” wallet where the provider retains your view key, the provider can see almost everything you do (but not spend your funds). Some self-custody wallets where the view key does not leave your device include:

- [Официальный клиент Monero](https://getmonero.org/ru/downloads/) (для ПК)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, Desktop)
    - Cake Wallet поддерживает множество криптовалют. A Monero-only version of Cake Wallet for iOS and Android is available at [Monero.com](https://monero.com).
- [Feather Wallet](https://featherwallet.org) (Desktop)
- [Monerujo](https://monerujo.io) (Android)

### Monero nodes

For maximum privacy (even with a self-custody wallet), you should run your own Monero node called the [Monero daemon](https://docs.getmonero.org/interacting/monerod-reference), which is included in the [CLI wallet](https://getmonero.org/downloads/#cli). Использование чьего-то узла раскрывает ему некоторую информацию, например: IP-адрес, с которого вы к нему подключаетесь, временные метки, по которым вы синхронизируете свой кошелек, и транзакции, которые вы отправляете из своего кошелька (хотя никакой другой информации об этих транзакциях нет). Alternatively, you can connect to someone else’s Monero node over [Tor](alternative-networks.md#tor), [I2P](alternative-networks.md#i2p-the-invisible-internet-project), or a [VPN](vpn.md).

### Buying Monero

[General tips for acquiring Monero](advanced/payments.md#acquisition ""){.md-button}

There are numerous centralized exchanges (CEX) as well as P2P marketplaces where you can buy and sell Monero. Some of them require identifying yourself (KYC) to comply with anti-money laundering regulations. However, due to Monero's privacy features, the only thing known to the seller is *that* you bought Monero, but not how much you own or where you spend it (after it leaves the exchange). Some reputable places to buy Monero include:

- [Kraken](https://kraken.com): A well-known CEX. Registration and KYC are mandatory. Card payments and bank transfers accepted. Make sure not to leave your newly purchased Monero on Kraken's platform after the purchase; withdraw them to a self-custody wallet. Monero is not available in all jurisdictions that Kraken operates in.[^1]
- [Cake Wallet](https://cakewallet.com): A self-custody cross-platform wallet for Monero and other cryptocurrencies. You can buy Monero directly in the app using card payments or bank transfers (through third-party providers such as [Guardarian](https://guardarian.com) or [DFX](https://dfx.swiss)).[^2] KYC is usually not required, but it depends on your country and the amount you are purchasing. In countries where directly purchasing Monero is not possible, you can also use a provider within Cake Wallet to first buy another cryptocurrency such as Bitcoin, Bitcoin Cash, or Litecoin and then exchange it to Monero in-app.
    - [Monero.com](https://monero.com) is an associated website where you can buy Monero and other cryptocurrencies without having to download an app. The funds will simply be sent to the wallet address of your choice.
- [RetoSwap](https://retoswap.com) (formerly known as Haveno-Reto) is a self-custody, decentralized P2P exchange platform based on the [Haveno](https://haveno.exchange) project which is available for Linux, Windows, and macOS. Monero can be bought and sold with maximum privacy, since most trading counterparties do not require KYC, trades are made directly between users (P2P), and all connections run through the Tor network. It is possible to buy Monero via bank transfer, Paypal, or even by paying in cash (meeting in person or sending by mail). Arbitrators can step in to resolve disputes between buyer and seller, but be careful when sharing your bank account or other sensitive information with your trading counterparty. Trading with some accounts may be against those accounts' terms of service.

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

- Криптовалюта должна по умолчанию обеспечивать приватные/неотслеживаемые транзакции.

<div class="admonition tip" markdown>
<p class="admonition-title">Important notices</p>

The content here is not legal or financial advice. We do not endorse or encourage illicit activities, and we do not endorse or encourage anything which violates a company's terms of service. Check with a professional to confirm that these recommendations are legal and available in your jurisdiction. [See all notices](about/notices.md).

</div>

[^1]: You may refer to the following pages for up-to-date information on countries in which Kraken does **not** allow the purchase of Monero: [Where is Kraken licensed or regulated?](https://support.kraken.com/hc/en-us/articles/where-is-kraken-licensed-or-regulated) and [Support for Monero (XMR) in Europe](https://support.kraken.com/hc/en-us/articles/support-for-monero-xmr-in-europe).
[^2]: You may refer to the following pages for up-to-date information on countries in which Cake Wallet and Monero.com **only** allow the direct purchase of Monero (through third-party providers): [Which countries are served by DFX?](https://docs.dfx.swiss/en/faq.html#which-countries-are-served-by-dfx) and [What are the supported countries/regions? (Guardarian)](https://guardarian.freshdesk.com/support/solutions/articles/80001151826-what-are-the-supported-countries-regions).
