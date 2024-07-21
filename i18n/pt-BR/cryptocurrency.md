---
meta_title: "Blockchains de criptomoedas privadas - Privacy Guides"
title: Criptomoedas
icon: material/bank-circle
cover: cryptocurrency.webp
---

Fazer pagamentos “on-line” é um dos maiores desafios à privacidade. Essas criptomoedas oferecem privacidade nas transações por padrão (algo que **não** é garantido pela maioria das criptomoedas), desde que você tenha um bom conhecimento de como fazer pagamentos privados de forma eficaz. Recomendamos fortemente que você leia primeiro nosso artigo de visão geral sobre pagamentos antes de fazer qualquer compra:

[Fazendo Pagamentos Privados :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

<div class="admonition danger" markdown>
<p class="admonition-title">Aviso</p>

Many if not most cryptocurrency projects are scams. Make transactions carefully with only projects you trust.

</div>

## Monero

<div class="admonition recommendation" markdown>

![Monero logo](assets/img/cryptocurrency/monero.svg){ align=right }

**Monero** uses a blockchain with privacy-enhancing technologies that obfuscate transactions to achieve anonymity. Every Monero transaction hides the transaction amount, sending and receiving addresses, and source of funds without any hoops to jump through, making it an ideal choice for cryptocurrency novices.

[:octicons-home-16: Homepage](https://getmonero.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://getmonero.org/resources/user-guides){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Source Code" }
[:octicons-heart-16:](https://getmonero.org/get-started/contributing){ .card-link title=Contribute }

</details>

</div>

Com o Monero, observadores externos não podem decifrar endereços que negociam Monero, valores de transações, saldos de endereços ou históricos de transações.

Para otimizar a privacidade, certifique-se de usar uma carteira sem custódia em que a chave de visualização permaneça no dispositivo. Isso significa que somente você poderá gastar seus fundos e ver as transações de entrada e saída. Se você usar uma carteira de custódia, o provedor poderá ver **tudo o que** você faz; se você usar uma carteira "leve", em que o provedor retém sua chave de visualização privada, o provedor poderá ver quase tudo o que você faz. Algumas carteiras sem custódia incluem:

- [Cliente oficial do Monero](https://getmonero.org/downloads) (Desktop)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, macOS)
    - Cake Wallet supports multiple cryptocurrencies. A Monero-only version of Cake Wallet for iOS and Android is available at [Monero.com](https://monero.com).
- [Carteira Feather](https://featherwallet.org) (Desktop)
- [Monerujo](https://monerujo.io) (Android)

Para obter o máximo de privacidade (mesmo com uma carteira sem custódia), você deve executar seu próprio nó Monero. O uso do nó de outra pessoa exporá algumas informações a ela, como o endereço IP a partir do qual você se conecta a ele, os carimbos de data e hora em que você sincroniza sua carteira e as transações que você envia de sua carteira (embora não haja outros detalhes sobre essas transações). Alternatively, you can connect to someone else’s Monero node over Tor or [I2P](alternative-networks.md#i2p-the-invisible-internet-project).

In August 2021, CipherTrace [announced](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) enhanced Monero tracing capabilities for government agencies. Postagens públicas mostram que o Departamento da Rede de Execução de Crimes Financeiros do Tesouro dos EUA [licenciou](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) Módulo "Monero Trace" da CipherTrace no final de 2022.

A privacidade do gráfico de transações do Monero é limitada por suas assinaturas de anel relativamente pequenas, especialmente contra ataques direcionados. Os recursos de privacidade do Monero também foram [questionados](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) por alguns pesquisadores de segurança, e várias vulnerabilidades graves foram encontradas e corrigidas no passado, de modo que as alegações feitas por organizações como a CipherTrace não estão fora de questão. Embora seja improvável que existam ferramentas de vigilância em massa do Monero como existem para o Bitcoin e outros, é certo que as ferramentas de rastreamento ajudam nas investigações direcionadas.

Em última análise, o Monero é o mais forte candidato a uma criptomoeda favorável à privacidade, mas suas alegações de privacidade **não** foram definitivamente comprovadas de uma forma ou de outra. É necessário mais tempo e pesquisa para avaliar se o Monero é suficientemente resistente a ataques para sempre proporcionar a privacidade adequada.

## Critérios

**Por favor, note que não somos parceiros de nenhum dos produtos que recomendamos.**Em adição aos[nossos critérios básicos](about/criteria.md), desenvolvemos um conjunto claro de requisitos para nos permitir fornecer recomendações objetivas. Recomendamos que você se familiarize com esta lista antes de escolher usar um produto, e que faça sua própria pesquisa para garantir que o produto escolhido é o ideal para você.

- A criptomoeda deve fornecer transações privadas/não rastreáveis por padrão.
