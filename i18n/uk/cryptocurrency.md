---
title: Cryptocurrency
icon: material/bank-circle
---

Making payments online is one of the biggest challenges to privacy. These cryptocurrencies provide transaction privacy by default (something which is **not** guaranteed by the majority of cryptocurrencies), provided you have a strong understanding of how to make private payments effectively. We strongly encourage you first read our payments overview article before making any purchases:

[Making Private Payments :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

!!! danger

    Many if not most cryptocurrency projects are scams. Make transactions carefully with only projects you trust.

## Monero

!!! рекомендації

    ![Monero logo](assets/img/cryptocurrency/monero.svg){ align=right }
    
    **Monero** uses a blockchain with privacy-enhancing technologies that obfuscate transactions to achieve anonymity. Every Monero transaction hides the transaction amount, sending and receiving addresses, and source of funds without any hoops to jump through, making it an ideal choice for cryptocurrency novices.
    
    [:octicons-home-16: Homepage](https://www.getmonero.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://www.getmonero.org/resources/user-guides/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.getmonero.org/get-started/contributing/){ .card-link title=Contribute }

With Monero, outside observers cannot decipher addresses trading Monero, transaction amounts, address balances, or transaction histories.

For optimal privacy, make sure to use a noncustodial wallet where the view key stays on the device. This means that only you will have the ability to spend your funds and see incoming and outgoing transactions. If you use a custodial wallet, the provider can see **everything** you do; if you use a “lightweight” wallet where the provider retains your private view key, the provider can see almost everything you do. Some noncustodial wallets include:

- [Official Monero client](https://getmonero.org/downloads) (Desktop)
- [Cake Wallet](https://cakewallet.com/) (iOS, Android)
    - Cake Wallet supports multiple cryptocurrencies. A Monero-only version of Cake Wallet is available at [Monero.com](https://monero.com/).
- [Feather Wallet](https://featherwallet.org/) (Desktop)
- [Monerujo](https://www.monerujo.io/) (Android)

For maximum privacy (even with a noncustodial wallet), you should run your own Monero node. Using another person’s node will expose some information to them, such as the IP address that you connect to it from, the timestamps that you sync your wallet, and the transactions that you send from your wallet (though no other details about those transactions). Alternatively, you can connect to someone else’s Monero node over Tor or i2p.

In August 2021, CipherTrace [announced](https://finance.yahoo.com/news/ciphertrace-announces-enhanced-monero-tracing-160000275.html) enhanced Monero tracing capabilities for government agencies. Public postings show that the US Department of the Treasury's Financial Crimes Enforcement Network [licensed](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) CipherTrace's "Monero Module" in late 2022.

Monero transaction graph privacy is limited by its relatively small ring signatures, especially against targeted attacks. Monero's privacy features have also been [called into question](https://web.archive.org/web/20180331203053/https://www.wired.com/story/monero-privacy/) by some security researchers, and a number of severe vulnerabilities have been found and patched in the past, so the claims made by organizations like CipherTrace are not out of the question. While it's unlikely that Monero mass surveillance tools exist like they do for Bitcoin and others, it's certain that tracing tools assist with targeted investigations.

Ultimately, Monero is the strongest contender for a privacy-friendly cryptocurrency, but its privacy claims have **not** been definitively proven one way or the other. More time and research is needed to assess whether Monero is resilient enough to attacks to always provide adequate privacy.

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! example "This section is new"

    We are working on establishing defined criteria for every section of our site, and this may be subject to change. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. There are many factors considered and discussed when we recommend a project, and documenting every single one is a work-in-progress.

- Cryptocurrency must provide private/untraceable transactions by default.
