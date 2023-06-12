---
meta_title: "Private Cryptocurrency Blockchains - Privacy Guides"
title: Криптовалюта
icon: material/bank-circle
cover: cryptocurrency.png
---

Платежи в Интернете - одна из самых серьезных проблем, связанных с конфиденциальностью. These cryptocurrencies provide transaction privacy by default (something which is **not** guaranteed by the majority of cryptocurrencies), provided you have a strong understanding of how to make private payments effectively. We strongly encourage you first read our payments overview article before making any purchases:

[Совершение анонимных платежей :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

!!! recommendation

    Многие, если не большинство, криптовалютных проектов - это мошеннические схемы. Осуществляйте транзакции осторожно, используя только те проекты, которым вы доверяете.

## Monero

!!! recommendation

    ![Логотип Monero](assets/img/cryptocurrency/monero.svg){ align=right }
    
    **Монеро (Monero)** использует блокчейн с технологиями повышения конфиденциальности, которые затрудняют отслеживание транзакций и обеспечивают анонимность. Каждая транзакция в Monero скрывает сумму транзакции, адреса отправителя и получателя, и источник средств, не требуя при этом дополнительных действий, что делает его идеальным выбором для новичков в области криптовалют.
    
    [:octicons-home-16: Homepage](https://www.getmonero.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://www.getmonero.org/resources/user-guides/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.getmonero.org/get-started/contributing/){ .card-link title=Contribute }

С помощью Monero сторонние наблюдатели не могут расшифровать адреса, которые обмениваются Monero, суммы транзакций, балансы адресов или историю транзакций.

Для максимальной конфиденциальности убедитесь, что вы используете некастодиальный кошелек, где ключ просмотра остается на вашем устройстве, а не на удалённом сервере. Это означает то, что **только вы** будете иметь возможность расходовать свои средства и видеть входящие и исходящие транзакции. Если вы используете кастодиальный кошелек, провайдер может видеть **абсолютно всё**, что вы делаете; если вы используете "лёгкий" кошелек, где провайдер хранит ваш приватный ключ, он может видеть практически всё, что вы делаете. Некоторые некастодиальные кошельки включают в себя:

- [Официальный клиент Monero](https://getmonero.org/ru/downloads/) (для ПК)
- [Cake Wallet](https://cakewallet.com/) (iOS, Android)
    - Cake Wallet поддерживает множество криптовалют. Версия Cake Wallet, предназначенная только для Monero, доступна на сайте [Monero.com](https://monero.com/).
- [Feather Wallet](https://featherwallet.org/) (для ПК)
- [Monerujo](https://www.monerujo.io/) (Android)

For maximum privacy (even with a noncustodial wallet), you should run your own Monero node. Using another person’s node will expose some information to them, such as the IP address that you connect to it from, the timestamps that you sync your wallet, and the transactions that you send from your wallet (though no other details about those transactions). Alternatively, you can connect to someone else’s Monero node over Tor or i2p.

В августе 2021 года компания CipherTrace [объявила о](https://ciphertrace.com/enhanced-monero-tracing/) расширенных возможностях отслеживания Monero для государственных учреждений. Public postings show that the US Department of the Treasury's Financial Crimes Enforcement Network [licensed](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) CipherTrace's "Monero Module" in late 2022.

Monero transaction graph privacy is limited by its relatively small ring signatures, especially against targeted attacks. Monero's privacy features have also been [called into question](https://web.archive.org/web/20180331203053/https://www.wired.com/story/monero-privacy/) by some security researchers, and a number of severe vulnerabilities have been found and patched in the past, so the claims made by organizations like CipherTrace are not out of the question. While it's unlikely that Monero mass surveillance tools exist like they do for Bitcoin and others, it's certain that tracing tools assist with targeted investigations.

Ultimately, Monero is the strongest contender for a privacy-friendly cryptocurrency, but its privacy claims have **not** been definitively proven one way or the other. More time and research is needed to assess whether Monero is resilient enough to attacks to always provide adequate privacy.

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! Для уменьшения этой угрозы рассмотрите возможность самостоятельного хостинга.

    We are working on establishing defined criteria for every section of our site, and this may be subject to change. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. Мы учитываем и обсуждаем много факторов, перед тем как рекомендовать какой-то проект, и документирование каждого из них ещё не завершено.

- Cryptocurrency must provide private/untraceable transactions by default.
