---
meta_title: "Chaînes de blocs de crypto-monnaies privées - Privacy Guides"
description: Unlike most cryptocurrencies, these ones provide transaction privacy by default. Monero is our top choice for obfuscating transaction information.
title: Crypto-monnaie
icon: material/bank-circle
cover: cryptocurrency.webp
---

<small>Protects against the following threat(s):</small>

- [:material-eye-outline: Surveillance de masse](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Censure](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

Effectuer des paiements en ligne est l'un des plus grands défis en matière de protection de la vie privée. Ces crypto-monnaies garantissent par défaut la confidentialité des transactions (ce qui n'est **pas** garanti par la majorité des crypto-monnaies), à condition que vous ayez une bonne compréhension de la façon d'effectuer des paiements privés de manière efficace. Nous vous encourageons vivement à lire notre article sur les paiements avant d'effectuer tout achat :

[Effectuer des paiements privés :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

De nombreux projets de crypto-monnaies, voire la plupart, sont des escroqueries. Effectuez des transactions avec prudence, uniquement avec des projets auxquels vous faites confiance.

</div>

## Monero

<div class="admonition recommendation" markdown>

![Monero logo](assets/img/cryptocurrency/monero.svg){ align=right }

**Monero** uses a blockchain with privacy-enhancing technologies that obfuscate transactions to achieve [:material-incognito: Anonymity](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }. Chaque transaction Monero cache le montant de la transaction, les adresses d'envoi et de réception, ainsi que la source des fonds, sans aucune difficulté, ce qui en fait un choix idéal pour les novices en matière de crypto-monnaies.

[:octicons-home-16: Page d'accueil](https://getmonero.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://getmonero.org/resources/user-guides){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Code source" }
[:octicons-heart-16:](https://getmonero.org/get-started/contributing){ .card-link title=Contribuer }

</details>

</div>

Avec Monero, les observateurs extérieurs ne peuvent pas déchiffrer les adresses qui échangent des Monero, les montants des transactions, les soldes des adresses ou l'historique des transactions.

<details class="info" markdown>
<summary>Monero's resilience to mass surveillance</summary>

In August 2021, CipherTrace [announced](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) enhanced Monero tracing capabilities for government agencies. Des publications publiques montrent que le Financial Crimes Enforcement Network du département du Trésor américain [a accordé une licence à](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) CipherTrace pour son "module Monero" à la fin de l'année 2022.

La confidentialité du graphe des transactions Monero est limitée par son cercle de signatures relativement petit, en particulier contre les attaques ciblées. Les caractéristiques de confidentialité de Monero ont également été [remises en question](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) par certains chercheurs en sécurité, et un certain nombre de vulnérabilités graves ont été trouvées et corrigées dans le passé, de sorte que les affirmations faites par des organisations comme CipherTrace ne sont pas hors de question. S'il est peu probable qu'il existe des outils de surveillance de masse de Monero comme il en existe pour le Bitcoin et d'autres, il est certain que les outils de traçage facilitent les enquêtes ciblées.

En fin de compte, Monero est la crypto-monnaie la plus respectueuse de la vie privée, mais ses revendications en matière de confidentialité **n'ont pas** été prouvées de manière définitive. Plus de temps et de recherche sont nécessaires pour évaluer si le Monero est suffisamment résistant aux attaques pour toujours offrir une protection adéquate de la vie privée.

</details>

### Monero wallets

For optimal privacy, make sure to use a self-custody wallet where the [view key](https://www.getmonero.org/resources/moneropedia/viewkey.html) stays on the device. Cela signifie que vous êtes le seul à pouvoir dépenser vos fonds et à voir les transactions entrantes et sortantes. If you use a custodial wallet, the provider can see **everything** you do; if you use a “lightweight” wallet where the provider retains your view key, the provider can see almost everything you do (but not spend your funds). Some self-custody wallets where the view key does not leave your device include:

- [le client Monero officiel](https://getmonero.org/downloads) (bureau)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, Desktop)
    - Cake Wallet prend en charge plusieurs crypto-monnaies. Une version de Cake Wallet réservée aux utilisateurs de Monero est disponible pour iOS et Android sur [Monero.com](https://monero.com).
- [Feather Wallet](https://featherwallet.org) (bureau)
- [Monerujo](https://monerujo.io) (Android)

### Monero nodes

For maximum privacy (even with a self-custody wallet), you should run your own Monero node called the [Monero daemon](https://getmonero.org/downloads/#cli). L'utilisation du nœud d'une autre personne expose certaines informations, telles que l'adresse IP à partir de laquelle vous vous connectez, les heures auxquelles vous synchronisez votre portefeuille et les transactions que vous envoyez à partir de votre portefeuille (mais pas d'autres détails sur ces transactions). Alternatively, you can connect to someone else’s Monero node over Tor, [I2P](alternative-networks.md#i2p-the-invisible-internet-project), or a VPN.

### Buying Monero

[General tips for acquiring Monero](advanced/payments.md#acquisition ""){.md-button}

There are numerous centralized exchanges (CEX) as well as P2P marketplaces where you can buy and sell Monero. Some of them require identifying yourself (KYC) to comply with anti-money laundering regulations. However, due to Monero's privacy features, the only thing known to the seller is _that_ you bought Monero, but not how much you own or where you spend it (after it leaves the exchange). Some reputable places to buy Monero include:

- [Kraken](https://kraken.com): A well-known CEX. Registration and KYC are mandatory. Card payments and bank transfers accepted. Make sure not to leave your newly purchased Monero on Kraken's platform after the purchase; withdraw them to a self-custody wallet. Monero is not available in all jurisdictions that Kraken operates in.[^1]
- [Cake Wallet](https://cakewallet.com): A self-custody cross-platform wallet for Monero and other cryptocurrencies. You can buy Monero directly in the app using card payments or bank transfers (through third-party providers such as [Guardarian](https://guardarian.com) or [DFX](https://dfx.swiss)).[^2] KYC is usually not required, but it depends on your country and the amount you are purchasing. In countries where directly purchasing Monero is not possible, you can also use a provider within Cake Wallet to first buy another cryptocurrency such as Bitcoin, Bitcoin Cash, or Litecoin and then exchange it to Monero in-app.
    - [Monero.com](https://monero.com) is an associated website where you can buy Monero and other cryptocurrencies without having to download an app. The funds will simply be sent to the wallet address of your choice.
- [RetoSwap](https://retoswap.com) (formerly known as Haveno-Reto) is a self-custody, decentralized P2P exchange platform based on the [Haveno](https://haveno.exchange) project which is available for Linux, Windows, and macOS. Monero can be bought and sold with maximum privacy, since most trading counterparties do not require KYC, trades are made directly between users (P2P), and all connections run through the Tor network. It is possible to buy Monero via bank transfer, Paypal, or even by paying in cash (meeting in person or sending by mail). Arbitrators can step in to resolve disputes between buyer and seller, but be careful when sharing your bank account or other sensitive information with your trading counterparty. Trading with some accounts may be against those accounts' terms of service. Please note that you can only buy Monero on RetoSwap if you already own a small amount of Monero (currently a minimum of 0.11 XMR) in order to fund security deposits, although there are ongoing efforts to drop this requirement in the future.

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

- La crypto-monnaie doit offrir des transactions privées/intraçables par défaut.

<div class="admonition tip" markdown>
<p class="admonition-title">Important notices</p>

The content here is not legal or financial advice. We do not endorse or encourage illicit activities, and we do not endorse or encourage anything which violates a company's terms of service. Check with a professional to confirm that these recommendations are legal and available in your jurisdiction. [See all notices](about/notices.md).

</div>

[^1]: You may refer to the following pages for up-to-date information on countries in which Kraken does **not** allow the purchase of Monero: [Where is Kraken licensed or regulated?](https://support.kraken.com/hc/en-us/articles/where-is-kraken-licensed-or-regulated) and [Support for Monero (XMR) in Europe](https://support.kraken.com/hc/en-us/articles/support-for-monero-xmr-in-europe).
[^2]: You may refer to the following pages for up-to-date information on countries in which Cake Wallet and Monero.com **only** allow the direct purchase of Monero (through third-party providers): [Which countries are served by DFX?](https://docs.dfx.swiss/en/faq.html#which-countries-are-served-by-dfx) and [What are the supported countries/regions? (Guardarian)](https://guardarian.freshdesk.com/support/solutions/articles/80001151826-what-are-the-supported-countries-regions).
