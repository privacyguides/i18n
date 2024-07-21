---
meta_title: "Private Cryptocurrency Blockchains - Privacy Guides"
title: Криптовалюта
icon: material/bank-circle
cover: cryptocurrency.webp
---

Платежи в интернете - одна из самых серьезных проблем, связанных с конфиденциальностью. Эти криптовалюты по умолчанию обеспечивают конфиденциальность транзакций (что **не** гарантируется большинством криптовалют), при условии, что вы хорошо понимаете, как эффективно осуществлять приватные платежи. Мы настоятельно рекомендуем вам сначала прочитать нашу обзорную статью о платежах, прежде чем совершать какие-либо покупки:

[Совершение приватных платежей :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Многие, если не большинство, криптовалютных проектов - это мошеннические схемы. Осуществляйте транзакции осторожно, используя только те проекты, которым вы доверяете.

</div>

## Monero

<div class="admonition recommendation" markdown>

![Логотип Monero](assets/img/cryptocurrency/monero.svg){ align=right }

**Monero** использует блокчейн с технологиями повышения конфиденциальности, которые затрудняют отслеживание транзакций для достижения анонимности. Каждая транзакция в Monero скрывает сумму транзакции, адреса отправителя и получателя и источник средств, не требуя при этом дополнительных действий, что делает её идеальным выбором для новичков в области криптовалют.

[:octicons-home-16: Homepage](https://getmonero.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://getmonero.org/resources/user-guides){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Source Code" }
[:octicons-heart-16:](https://getmonero.org/get-started/contributing){ .card-link title=Contribute }

</details>

</div>

С помощью Monero сторонние наблюдатели не могут расшифровать адреса, которые обмениваются Monero, суммы транзакций, балансы адресов или историю транзакций.

Для максимальной конфиденциальности убедитесь, что вы используете некастодиальный кошелек, где ключ просмотра остается на вашем устройстве, а не на удалённом сервере. Это означает то, что только вы будете иметь возможность расходовать свои средства и видеть входящие и исходящие транзакции. Если вы используете кастодиальный кошелек, провайдер может видеть **абсолютно всё**, что вы делаете; если вы используете "лёгкий" кошелек, где провайдер хранит ваш приватный ключ, он может видеть практически всё, что вы делаете. Некоторые некастодиальные кошельки включают в себя:

- [Официальный клиент Monero](https://getmonero.org/ru/downloads/) (для ПК)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, macOS)
    - Cake Wallet поддерживает множество криптовалют. A Monero-only version of Cake Wallet for iOS and Android is available at [Monero.com](https://monero.com).
- [Feather Wallet](https://featherwallet.org) (Desktop)
- [Monerujo](https://monerujo.io) (Android)

Для обеспечения максимальной конфиденциальности (даже при использовании некастодиального кошелька) вам следует запустить собственный узел Monero. Использование чьего-то узла раскрывает ему некоторую информацию, например: IP-адрес, с которого вы к нему подключаетесь, временные метки, по которым вы синхронизируете свой кошелек, и транзакции, которые вы отправляете из своего кошелька (хотя никакой другой информации об этих транзакциях нет). Alternatively, you can connect to someone else’s Monero node over Tor or [I2P](alternative-networks.md#i2p-the-invisible-internet-project).

In August 2021, CipherTrace [announced](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) enhanced Monero tracing capabilities for government agencies. Публичные сообщения показывают, что сеть по борьбе с финансовыми преступлениями министерства финансов США [лицензировала](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) "модуль Monero" CipherTrace в конце 2022 года.

Конфиденциальность графа транзакций Monero ограничена его относительно небольшими кольцевыми подписями, особенно против персональных атак. Monero's privacy features have also been [called into question](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) by some security researchers, and a number of severe vulnerabilities have been found and patched in the past, so the claims made by organizations like CipherTrace are not out of the question. Хотя маловероятно, что существуют инструменты массового наблюдения за Monero, как это происходит с Bitcoin и другими криптовалютами, несомненно инструменты отслеживания помогают проводить персональные расследования.

В конечном итоге Monero является самым сильным претендентом на звание криптовалюты, обеспечивающей конфиденциальность, но ее заявления о конфиденциальности **не** были окончательно доказаны тем или иным способом. Необходимо больше времени и исследований, чтобы оценить, достаточно ли устойчива Monero к атакам, чтобы всегда обеспечивать достаточную конфиденциальность.

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

- Криптовалюта должна по умолчанию обеспечивать приватные/неотслеживаемые транзакции.
