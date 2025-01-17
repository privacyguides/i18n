---
meta_title: "Private Kryptowährungs-Blockchains - Privacy Guides"
description: Unlike most cryptocurrencies, these ones provide transaction privacy by default. Monero is our top choice for obfuscating transaction information.
title: Kryptowährung
icon: material/bank-circle
cover: cryptocurrency.webp
---

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-eye-outline: Massenüberwachung](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Zensur](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

Online-Zahlungen sind eine der größten Herausforderungen für Privatsphäre. Diese Kryptowährungen bieten standardmäßig den Schutz der Privatsphäre bei Transaktionen (was bei den meisten Kryptowährungen **nicht** gewährleistet ist), vorausgesetzt, du weißt, wie du private Zahlungen effektiv durchführen kannst. Wir empfehlen dir dringend, zuerst unseren Artikel über Zahlungen zu lesen, bevor du einen Kauf tätigst:

[Private Zahlungsmethoden :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

<div class="admonition danger" markdown>
<p class="admonition-title">Achtung</p>

Viele, wenn nicht die meisten, Kryptowährungsprojekte sind Betrugsmaschen. Tätige Transaktionen nur mit Projekten, denen du vertraust.

</div>

## Monero

<div class="admonition recommendation" markdown>

![Monero-Logo](assets/img/cryptocurrency/monero.svg){ align=right }

**Monero** verwendet eine Blockchain mit Technologien zur Verbesserung der Privatsphäre, die Transaktionen verschleiern, um [:material-incognito: Anonymität](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } zu erreichen. Jede Monero-Transaktion verbirgt den Transaktionsbetrag, die sendende und empfangende Adresse und die Quelle des Geldes, ohne dass man irgendwelche Hürden überwinden muss, was es zu einer idealen Wahl für Kryptowährungs-Neulinge macht.

[:octicons-home-16: Homepage](https://getmonero.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://getmonero.org/resources/user-guides){ .card-link title=Dokumentation}
[:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://getmonero.org/get-started/contributing){ .card-link title=Mitwirken }

</details>

</div>

Bei Monero können außenstehende Beobachter weder Adressen, die mit Monero handeln, noch Transaktionsbeträge, Adresssalden oder Transaktionshistorien entziffern.

<details class="info" markdown>
<summary>Monero's resilience to mass surveillance</summary>

Im August 2021 [kündigte](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) CipherTrace erweiterte Monero-Verfolgungsfunktionen für Regierungsbehören an. Aus öffentlichen Veröffentlichungen geht hervor, dass das Financial Crimes Enforcement Network des US-Finanzministeriums das „Monero-Modul“ von CipherTrace Ende 2022 [lizenziert hat](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view).

Die Vertraulichkeit des Monero-Transaktionsgraphen wird durch seine relativ kleinen Ringsignaturen eingeschränkt, insbesondere gegenüber gezielten Angriffen. Die Datenschutzfunktionen von Monero wurden auch von einigen Sicherheitsforschern [in Frage gestellt](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy), und in der Vergangenheit wurde eine Reihe schwerwiegender Server-Schwachstellen gefunden und gepatcht, sodass die Behauptungen von Organisationen wie CipherTrace nicht außer Frage stehen. Es ist zwar unwahrscheinlich, dass es für Monero Massenüberwachungs-Tools gibt, wie es sie für Bitcoin und andere Währungen gibt, aber es ist sicher, dass Rückverfolgungs-Tools bei gezielten Ermittlungen helfen.

Letzten Endes ist Monero der stärkste Kandidat für eine datenschutzfreundliche Kryptowährung, aber seine Datenschutzansprüche sind **nicht** definitiv bewiesen. Es ist mehr Zeit und Forschung nötig, um zu beurteilen, ob Monero widerstandsfähig genug gegen Angriffe ist, um immer eine angemessene Privatsphäre zu bieten.

</details>

### Monero wallets

For optimal privacy, make sure to use a self-custody wallet where the [view key](https://www.getmonero.org/resources/moneropedia/viewkey.html) stays on the device. Das bedeutet, dass nur du die Möglichkeit hast, dein Geld auszugeben und ein- und ausgehende Transaktionen zu sehen. If you use a custodial wallet, the provider can see **everything** you do; if you use a “lightweight” wallet where the provider retains your view key, the provider can see almost everything you do (but not spend your funds). Some self-custody wallets where the view key does not leave your device include:

- [Offizieller Monero-Client](https://getmonero.org/downloads) (Desktop)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, Desktop)
    - Cake Wallet unterstützt mehrere Kryptowährungen. Eine reine Monero Version von Cake Wallet für iOS und Android ist auf [Monero.com](https://monero.com) verfügbar.
- [Feather Wallet](https://featherwallet.org) (Desktop)
- [Monerujo](https://monerujo.io) (Android)

### Monero nodes

For maximum privacy (even with a self-custody wallet), you should run your own Monero node called the [Monero daemon](https://getmonero.org/downloads/#cli). Wenn du den Node einer anderen Person verwendest, werden einige Informationen preisgegeben, z. B. die IP-Adresse, von der aus du dich mit dem Node verbindest, die Zeitpunkte, an denen du deine Wallet synchronisierst und der Transaktionen, die du von deiner Wallet aus sendest (allerdings keine weiteren Details über diese Transaktionen). Alternatively, you can connect to someone else’s Monero node over Tor, [I2P](alternative-networks.md#i2p-the-invisible-internet-project), or a VPN.

### Buying Monero

[General tips for acquiring Monero](advanced/payments.md#acquisition ""){.md-button}

There are numerous centralized exchanges (CEX) as well as P2P marketplaces where you can buy and sell Monero. Some of them require identifying yourself (KYC) to comply with anti-money laundering regulations. However, due to Monero's privacy features, the only thing known to the seller is _that_ you bought Monero, but not how much you own or where you spend it (after it leaves the exchange). Some reputable places to buy Monero include:

- [Kraken](https://kraken.com): A well-known CEX. Registration and KYC are mandatory. Card payments and bank transfers accepted. Make sure not to leave your newly purchased Monero on Kraken's platform after the purchase; withdraw them to a self-custody wallet. Monero is not available in all jurisdictions that Kraken operates in.[^1]
- [Cake Wallet](https://cakewallet.com): A self-custody cross-platform wallet for Monero and other cryptocurrencies. You can buy Monero directly in the app using card payments or bank transfers (through third-party providers such as [Guardarian](https://guardarian.com) or [DFX](https://dfx.swiss)).[^2] KYC is usually not required, but it depends on your country and the amount you are purchasing. In countries where directly purchasing Monero is not possible, you can also use a provider within Cake Wallet to first buy another cryptocurrency such as Bitcoin, Bitcoin Cash, or Litecoin and then exchange it to Monero in-app.
    - [Monero.com](https://monero.com) is an associated website where you can buy Monero and other cryptocurrencies without having to download an app. The funds will simply be sent to the wallet address of your choice.
- [RetoSwap](https://retoswap.com) (formerly known as Haveno-Reto) is a self-custody, decentralized P2P exchange platform based on the [Haveno](https://haveno.exchange) project which is available for Linux, Windows, and macOS. Monero can be bought and sold with maximum privacy, since most trading counterparties do not require KYC, trades are made directly between users (P2P), and all connections run through the Tor network. It is possible to buy Monero via bank transfer, Paypal, or even by paying in cash (meeting in person or sending by mail). Arbitrators can step in to resolve disputes between buyer and seller, but be careful when sharing your bank account or other sensitive information with your trading counterparty. Trading with some accounts may be against those accounts' terms of service.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, in Verbindung stehen.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen dir, dich mit der Liste vertraut zu machen, bevor du dich für ein Projekt entscheidest, und deine eigenen Recherchen anzustellen, um sicherzustellen, dass es die richtige Wahl für dich ist.

- Kryptowährungen müssen standardmäßig private/unverfolgbare Transaktionen ermöglichen.

<div class="admonition tip" markdown>
<p class="admonition-title">Important notices</p>

The content here is not legal or financial advice. We do not endorse or encourage illicit activities, and we do not endorse or encourage anything which violates a company's terms of service. Check with a professional to confirm that these recommendations are legal and available in your jurisdiction. [See all notices](about/notices.md).

</div>

[^1]: You may refer to the following pages for up-to-date information on countries in which Kraken does **not** allow the purchase of Monero: [Where is Kraken licensed or regulated?](https://support.kraken.com/hc/en-us/articles/where-is-kraken-licensed-or-regulated) and [Support for Monero (XMR) in Europe](https://support.kraken.com/hc/en-us/articles/support-for-monero-xmr-in-europe).
[^2]: You may refer to the following pages for up-to-date information on countries in which Cake Wallet and Monero.com **only** allow the direct purchase of Monero (through third-party providers): [Which countries are served by DFX?](https://docs.dfx.swiss/en/faq.html#which-countries-are-served-by-dfx) and [What are the supported countries/regions? (Guardarian)](https://guardarian.freshdesk.com/support/solutions/articles/80001151826-what-are-the-supported-countries-regions).
