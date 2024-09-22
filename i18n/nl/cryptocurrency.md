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

Voor optimale privacy, zorg ervoor dat je een noncustodial wallet gebruikt waar de view key op het apparaat blijft. Dit betekent dat alleen jij je geld kunt uitgeven en de inkomende en uitgaande transacties kunt zien. Als je een custodial wallet gebruikt, kan de provider **alles zien wat** je doet; als je een "lichtgewicht" wallet gebruikt waarbij de provider jouw privé view key bewaard, kan de provider bijna alles zien wat u doet. Sommige niet-custodiale wallets omvatten:

- [Officiële Monero-client](https://getmonero.org/downloads) (Desktop)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, macOS)
    - Cake Wallet ondersteunt meerdere cryptocurrencies. A Monero-only version of Cake Wallet for iOS and Android is available at [Monero.com](https://monero.com).
- [Feather Wallet](https://featherwallet.org) (Desktop)
- [Monerujo](https://monerujo.io) (Android)

Voor maximale privacy (zelfs met een niet-custodiale wallet) moet je jouw eigen Monero-knooppunt beheren. Als je een knooppunt van een ander gebruikt, krijgt hij enige informatie, zoals het IP-adres van waaruit je verbinding maakt, de tijdstempels waarmee je jouw portemonnee synchroniseert, en de transacties die je vanuit jouw portemonnee verstuurt (maar geen andere details over die transacties). Alternatively, you can connect to someone else’s Monero node over Tor or [I2P](alternative-networks.md#i2p-the-invisible-internet-project).

In August 2021, CipherTrace [announced](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) enhanced Monero tracing capabilities for government agencies. Uit openbare berichten blijkt dat het Financial Crimes Enforcement Network van het Amerikaanse ministerie van Financiën [eind 2022 een licentie heeft verleend aan](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) CipherTrace's "Monero Module".

De privacy van de Monero-transactiegrafiek wordt beperkt door de relatief kleine ringhandtekeningen, vooral tegen gerichte aanvallen. Monero's privacy features have also been [called into question](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) by some security researchers, and a number of severe vulnerabilities have been found and patched in the past, so the claims made by organizations like CipherTrace are not out of the question. Hoewel het onwaarschijnlijk is dat er voor Monero massa surveillance instrumenten bestaan zoals voor Bitcoin en andere, is het zeker dat opsporingstools helpen bij gerichte onderzoeken.

Uiteindelijk is Monero de sterkste mededinger voor een privacyvriendelijke cryptocurrency, maar zijn privacyclaims zijn **niet** definitief bewezen. Er is meer tijd en onderzoek nodig om te beoordelen of Monero weerbaar genoeg is tegen aanvallen om altijd voldoende privacy te bieden.

## Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

- Cryptocurrency moet standaard private/ontraceerbare transacties bieden.
