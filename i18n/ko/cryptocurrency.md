---
meta_title: "Private Cryptocurrency Blockchains - Privacy Guides"
description: Unlike most cryptocurrencies, these ones provide transaction privacy by default. Monero is our top choice for obfuscating transaction information.
title: 암호화폐
icon: material/bank-circle
cover: cryptocurrency.webp
---

<small>Protects against the following threat(s):</small>

- [:material-eye-outline: 대중 감시(Mass Surveillance)](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: 검열(Censorship)](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

온라인 결제는 프라이버시에 있어서 매우 큰 문제입니다. 다음과 같은 암호화폐는 여러분이 프라이버시를 보호하면서 결제를 하는 방법에 대해 충분한 이해를 갖춘 경우, 거래 프라이버시를 기본적으로 제공합니다.(대부분의 암호화폐는 거래 프라이버시를 보장하지 **않습니다**.) 무엇인가를 구매하기에 앞서, Privacy Guides에서 결제 개요 문서를 읽어보실 것을 강력히 권장드립니다:

[Making Private Payments :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

전부는 아니지만, 대부분의 암호화폐 프로젝트는 사기입니다. 신뢰할 수 있는 프로젝트로만 신중하게 거래하세요.

</div>

## Monero

<div class="admonition recommendation" markdown>

![Monero logo](assets/img/cryptocurrency/monero.svg){ align=right }

**Monero** uses a blockchain with privacy-enhancing technologies that obfuscate transactions to achieve [:material-incognito: Anonymity](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }. 모든 Monero 거래는 거래 금액, 송수신 주소, 자금 출처가 숨겨지므로 암호화폐 초심자에게 이상적인 선택입니다.

[:octicons-home-16: Homepage](https://getmonero.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://getmonero.org/resources/user-guides){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Source Code" }
[:octicons-heart-16:](https://getmonero.org/get-started/contributing){ .card-link title=Contribute }

</details>

</div>

Monero를 사용할 경우, Monero를 거래하는 주소, 거래 금액, 주소 잔액, 거래 내역을 외부 관찰자가 해독할 수 없습니다.

<details class="info" markdown>
<summary>Monero's resilience to mass surveillance</summary>

In August 2021, CipherTrace [announced](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) enhanced Monero tracing capabilities for government agencies. 공개 포스트에 따르면, 미국 재무부의 금융 범죄 단속 네트워크(Financial Crimes Enforcement Network)는 2022년 말 CipherTrace의 'Monero 모듈'에 라이선스 자격을 [부여했습니다](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view).

Monero 트랜잭션 그래프는 프라이버시 면에서 제한적입니다. 상대적으로 작은 링 서명(Ring Signature)으로 인해, 표적 공격에 취약합니다. Monero's privacy features have also been [called into question](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) by some security researchers, and a number of severe vulnerabilities have been found and patched in the past, so the claims made by organizations like CipherTrace are not out of the question. 비트코인이나 다른 암호화폐처럼 대규모 감시 도구가 Monero에도 존재할 가능성은 낮지만, 추적 툴이 표적 수사에 효과가 있을 것은 확실합니다.

종합적으로, Monero는 가장 뛰어난 프라이버시 친화 암호화폐라고 충분히 말할 수 있지만, 프라이버시 주장은 (좋은 쪽으로든 나쁜 쪽으로든) 확실하게 입증된 바 **없습니다**. Monero가 항상 적절한 프라이버시를 보장할 수 있을 만큼 공격에 대한 복원력이 충분한지를 평가하기 위해서는 더 많은 시간과 연구가 필요합니다.

</details>

### Monero wallets

For optimal privacy, make sure to use a self-custody wallet where the [view key](https://getmonero.org/resources/moneropedia/viewkey.html) stays on the device. 비수탁형 지갑은 사용자 본인 외에는 자금 지출은 물론이고, 들어오고 나가는 트랜잭션을 볼 수 없습니다. If you use a custodial wallet, the provider can see **everything** you do; if you use a “lightweight” wallet where the provider retains your view key, the provider can see almost everything you do (but not spend your funds). Some self-custody wallets where the view key does not leave your device include:

- [공식 Monero 클라이언트](https://getmonero.org/downloads) (데스크톱)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, Desktop)
    - Cake Wallet은 여러 암호화폐를 지원합니다. A Monero-only version of Cake Wallet for iOS and Android is available at [Monero.com](https://monero.com).
- [Feather Wallet](https://featherwallet.org) (Desktop)
- [Monerujo](https://monerujo.io) (Android)

### Monero nodes

For maximum privacy (even with a self-custody wallet), you should run your own Monero node called the [Monero daemon](https://docs.getmonero.org/interacting/monerod-reference), which is included in the [CLI wallet](https://getmonero.org/downloads/#cli). 다른 사람의 노드를 사용할 경우 해당 노드에 연결할 때 사용한 IP 주소, 지갑을 동기화한 시각, 지갑에서 전송된 트랜잭션(해당 트랜잭션에 대한 자세한 정보는 알 수 없음) 등 일부 정보가 해당 노드에 노출됩니다. Alternatively, you can connect to someone else’s Monero node over [Tor](alternative-networks.md#tor), [I2P](alternative-networks.md#i2p-the-invisible-internet-project), or a [VPN](vpn.md).

### Buying Monero

[General tips for acquiring Monero](advanced/payments.md#acquisition ""){.md-button}

There are numerous centralized exchanges (CEX) as well as P2P marketplaces where you can buy and sell Monero. Some of them require identifying yourself (KYC) to comply with anti-money laundering regulations. However, due to Monero's privacy features, the only thing known to the seller is *that* you bought Monero, but not how much you own or where you spend it (after it leaves the exchange). Some reputable places to buy Monero include:

- [Kraken](https://kraken.com): A well-known CEX. Registration and KYC are mandatory. Card payments and bank transfers accepted. Make sure not to leave your newly purchased Monero on Kraken's platform after the purchase; withdraw them to a self-custody wallet. Monero is not available in all jurisdictions that Kraken operates in.[^1]
- [Cake Wallet](https://cakewallet.com): A self-custody cross-platform wallet for Monero and other cryptocurrencies. You can buy Monero directly in the app using card payments or bank transfers (through third-party providers such as [Guardarian](https://guardarian.com) or [DFX](https://dfx.swiss)).[^2] KYC is usually not required, but it depends on your country and the amount you are purchasing. In countries where directly purchasing Monero is not possible, you can also use a provider within Cake Wallet to first buy another cryptocurrency such as Bitcoin, Bitcoin Cash, or Litecoin and then exchange it to Monero in-app.
    - [Monero.com](https://monero.com) is an associated website where you can buy Monero and other cryptocurrencies without having to download an app. The funds will simply be sent to the wallet address of your choice.
- [RetoSwap](https://retoswap.com) (formerly known as Haveno-Reto) is a self-custody, decentralized P2P exchange platform based on the [Haveno](https://haveno.exchange) project which is available for Linux, Windows, and macOS. Monero can be bought and sold with maximum privacy, since most trading counterparties do not require KYC, trades are made directly between users (P2P), and all connections run through the Tor network. It is possible to buy Monero via bank transfer, Paypal, or even by paying in cash (meeting in person or sending by mail). Arbitrators can step in to resolve disputes between buyer and seller, but be careful when sharing your bank account or other sensitive information with your trading counterparty. Trading with some accounts may be against those accounts' terms of service.

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

- 암호화페는 기본적으로 비공개/추적 불가능한 트랜잭션을 제공해야 합니다.

<div class="admonition tip" markdown>
<p class="admonition-title">Important notices</p>

The content here is not legal or financial advice. We do not endorse or encourage illicit activities, and we do not endorse or encourage anything which violates a company's terms of service. Check with a professional to confirm that these recommendations are legal and available in your jurisdiction. [See all notices](about/notices.md).

</div>

[^1]: You may refer to the following pages for up-to-date information on countries in which Kraken does **not** allow the purchase of Monero: [Where is Kraken licensed or regulated?](https://support.kraken.com/hc/en-us/articles/where-is-kraken-licensed-or-regulated) and [Support for Monero (XMR) in Europe](https://support.kraken.com/hc/en-us/articles/support-for-monero-xmr-in-europe).
[^2]: You may refer to the following pages for up-to-date information on countries in which Cake Wallet and Monero.com **only** allow the direct purchase of Monero (through third-party providers): [Which countries are served by DFX?](https://docs.dfx.swiss/en/faq.html#which-countries-are-served-by-dfx) and [What are the supported countries/regions? (Guardarian)](https://guardarian.freshdesk.com/support/solutions/articles/80001151826-what-are-the-supported-countries-regions).
