---
meta_title: "Private Cryptocurrency Blockchains - Privacy Guides"
description: Unlike most cryptocurrencies, these ones provide transaction privacy by default. Monero is our top choice for obfuscating transaction information.
title: Cryptocurrency
icon: material/bank-circle
cover: cryptocurrency.webp
---

<small>Protects against the following threat(s):</small>

- [:material-eye-outline: Massabewaking](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Censuur](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

Online betalen is een van de grootste uitdagingen voor privacy. Deze cryptocurrencies bieden standaard transactieprivacy (iets wat door de meeste cryptocurrencies **niet** wordt gegarandeerd), mits je goed begrijpt hoe je private betalingen effectief kunt uitvoeren. Wij raden je sterk aan eerst ons overzichtsartikel over betalingen te lezen voordat je aankopen doet:

[Privébetalingen maken :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Veel zo niet de meeste cryptocurrency projecten zijn zwendel. Voer transacties zorgvuldig uit met alleen projecten die je vertrouwt.

</div>

## Monero

<div class="admonition recommendation" markdown>

![Monero logo](assets/img/cryptocurrency/monero.svg){ align=right }

**Monero** uses a blockchain with privacy-enhancing technologies that obfuscate transactions to achieve [:material-incognito: Anonymity](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }. Elke Monero-transactie verbergt het transactiebedrag, het verzenden en ontvangen van adressen en de bron van fondsen zonder hoepels om doorheen te springen, waardoor het een ideale keuze is voor beginners met cryptocurrency.

[:octicons-home-16: Homepage](https://getmonero.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://getmonero.org/resources/user-guides){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Source Code" }
[:octicons-heart-16:](https://getmonero.org/get-started/contributing){ .card-link title=Contribute }

</details>

</div>

Met Monero kunnen externe waarnemers geen adressen ontcijferen die handelen in Monero, transactiebedragen, adresbalansen of transactiegeschiedenissen.

<details class="info" markdown>
<summary>Monero's resilience to mass surveillance</summary>

In August 2021, CipherTrace [announced](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) enhanced Monero tracing capabilities for government agencies. Uit openbare berichten blijkt dat het Financial Crimes Enforcement Network van het Amerikaanse ministerie van Financiën [eind 2022 een licentie heeft verleend aan](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) CipherTrace's "Monero Module".

De privacy van de Monero-transactiegrafiek wordt beperkt door de relatief kleine ringhandtekeningen, vooral tegen gerichte aanvallen. Monero's privacy features have also been [called into question](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) by some security researchers, and a number of severe vulnerabilities have been found and patched in the past, so the claims made by organizations like CipherTrace are not out of the question. Hoewel het onwaarschijnlijk is dat er voor Monero massa surveillance instrumenten bestaan zoals voor Bitcoin en andere, is het zeker dat opsporingstools helpen bij gerichte onderzoeken.

Uiteindelijk is Monero de sterkste mededinger voor een privacyvriendelijke cryptocurrency, maar zijn privacyclaims zijn **niet** definitief bewezen. Er is meer tijd en onderzoek nodig om te beoordelen of Monero weerbaar genoeg is tegen aanvallen om altijd voldoende privacy te bieden.

</details>

### Monero wallets

For optimal privacy, make sure to use a self-custody wallet where the [view key](https://getmonero.org/resources/moneropedia/viewkey.html) stays on the device. Dit betekent dat alleen jij je geld kunt uitgeven en de inkomende en uitgaande transacties kunt zien. If you use a custodial wallet, the provider can see **everything** you do; if you use a “lightweight” wallet where the provider retains your view key, the provider can see almost everything you do (but not spend your funds). Some self-custody wallets where the view key does not leave your device include:

- [Officiële Monero-client](https://getmonero.org/downloads) (Desktop)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, Desktop)
    - Cake Wallet ondersteunt meerdere cryptocurrencies. A Monero-only version of Cake Wallet for iOS and Android is available at [Monero.com](https://monero.com).
- [Feather Wallet](https://featherwallet.org) (Desktop)
- [Monerujo](https://monerujo.io) (Android)

### Monero nodes

For maximum privacy (even with a self-custody wallet), you should run your own Monero node called the [Monero daemon](https://docs.getmonero.org/interacting/monerod-reference), which is included in the [CLI wallet](https://getmonero.org/downloads/#cli). Als je een knooppunt van een ander gebruikt, krijgt hij enige informatie, zoals het IP-adres van waaruit je verbinding maakt, de tijdstempels waarmee je jouw portemonnee synchroniseert, en de transacties die je vanuit jouw portemonnee verstuurt (maar geen andere details over die transacties). Alternatively, you can connect to someone else’s Monero node over [Tor](alternative-networks.md#tor), [I2P](alternative-networks.md#i2p-the-invisible-internet-project), or a [VPN](vpn.md).

### Buying Monero

[General tips for acquiring Monero](advanced/payments.md#acquisition ""){.md-button}

There are numerous centralized exchanges (CEX) as well as P2P marketplaces where you can buy and sell Monero. Some of them require identifying yourself (KYC) to comply with anti-money laundering regulations. However, due to Monero's privacy features, the only thing known to the seller is *that* you bought Monero, but not how much you own or where you spend it (after it leaves the exchange). Some reputable places to buy Monero include:

- [Kraken](https://kraken.com): A well-known CEX. Registration and KYC are mandatory. Card payments and bank transfers accepted. Make sure not to leave your newly purchased Monero on Kraken's platform after the purchase; withdraw them to a self-custody wallet. Monero is not available in all jurisdictions that Kraken operates in.[^1]
- [Cake Wallet](https://cakewallet.com): A self-custody cross-platform wallet for Monero and other cryptocurrencies. You can buy Monero directly in the app using card payments or bank transfers (through third-party providers such as [Guardarian](https://guardarian.com) or [DFX](https://dfx.swiss)).[^2] KYC is usually not required, but it depends on your country and the amount you are purchasing. In countries where directly purchasing Monero is not possible, you can also use a provider within Cake Wallet to first buy another cryptocurrency such as Bitcoin, Bitcoin Cash, or Litecoin and then exchange it to Monero in-app.
    - [Monero.com](https://monero.com) is an associated website where you can buy Monero and other cryptocurrencies without having to download an app. The funds will simply be sent to the wallet address of your choice.
- [RetoSwap](https://retoswap.com) (formerly known as Haveno-Reto) is a self-custody, decentralized P2P exchange platform based on the [Haveno](https://haveno.exchange) project which is available for Linux, Windows, and macOS. Monero can be bought and sold with maximum privacy, since most trading counterparties do not require KYC, trades are made directly between users (P2P), and all connections run through the Tor network. It is possible to buy Monero via bank transfer, PayPal, or even by paying in cash (meeting in person or sending by mail). Arbitrators can step in to resolve disputes between buyer and seller, but be careful when sharing your bank account or other sensitive information with your trading counterparty. Trading with some accounts may be against those accounts' terms of service.

## Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

- Cryptocurrency moet standaard private/ontraceerbare transacties bieden.

<div class="admonition tip" markdown>
<p class="admonition-title">Important notices</p>

The content here is not legal or financial advice. We do not endorse or encourage illicit activities, and we do not endorse or encourage anything which violates a company's terms of service. Check with a professional to confirm that these recommendations are legal and available in your jurisdiction. [See all notices](about/notices.md).

</div>

[^1]: You may refer to the following pages for up-to-date information on countries in which Kraken does **not** allow the purchase of Monero: [Where is Kraken licensed or regulated?](https://support.kraken.com/hc/en-us/articles/where-is-kraken-licensed-or-regulated) and [Support for Monero (XMR) in Europe](https://support.kraken.com/hc/en-us/articles/support-for-monero-xmr-in-europe).
[^2]: You may refer to the following pages for up-to-date information on countries in which Cake Wallet and Monero.com **only** allow the direct purchase of Monero (through third-party providers): [Which countries are served by DFX?](https://docs.dfx.swiss/en/faq.html#which-countries-are-served-by-dfx) and [What are the supported countries/regions? (Guardarian)](https://guardarian.freshdesk.com/support/solutions/articles/80001151826-what-are-the-supported-countries-regions).
