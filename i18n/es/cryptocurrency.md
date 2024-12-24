---
meta_title: "Blockchains Privadas de Criptomonedas - Privacy Guides"
description: A diferencia de la mayoría de las criptomonedas, estas proporcionan privacidad en las transacciones por defecto. Monero es nuestra mejor opción para ocultar la información de las transacciones.
title: Criptomonedas
icon: material/bank-circle
cover: cryptocurrency.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-eye-outline: Vigilancia masiva](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Censura](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

Realizar pagos en línea es uno de los principales desafíos para la privacidad. Estas criptomonedas le brindan privacidad a sus transacciones (algo que **no** está garantizado por la mayoría de las criptomonedas), permitiéndole tener una alta comprensión de cómo hacer pagos privados correctamente. Le recomendamos encarecidamente que primero lea nuestro apartado de pagos antes de realizar cualquier compra:

[Hacer pagos privados: :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

<div class="admonition danger" markdown>
<p class="admonition-title">Peligro</p>

Muchas, si no la mayoría de los proyectos de criptomonedas son estafas. Únicamente realice transacciones con los proyectos en los que confíe.

</div>

## Monero

<div class="admonition recommendation" markdown>

![Monero logo](assets/img/cryptocurrency/monero.svg){ align=right }

**Monero** utiliza una blockchain con tecnologías de mejora de la privacidad que ofuscan las transacciones para lograr [:material-incognito: Anonimato](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }. Cada transacción realizada con Monero, oculta el monto de la transacción, las direcciones de envío y recepción, además del origen de los fondos sin ningún intermediario, convirtiéndola en una opción ideal para los novatos en las criptomonedas.

[:octicons-home-16: Página Principal](https://getmonero.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://getmonero.org/resources/user-guides){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://getmonero.org/get-started/contributing){ .card-link title=Contribuir }

</details>

</div>

Con Monero, los observadores externos no pueden descifrar las direcciones transaccionales de Monero, los montos de las transacciones, el balance de las direcciones, o el historial de transacciones.

<details class="info" markdown>
<summary>Monero's resilience to mass surveillance</summary>

En agosto de 2021, CipherTrace [anunció](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) capacidades mejoradas de rastreo de Monero para agencias gubernamentales. Publicaciones públicas muestran cómo la Red de Ejecución de Delitos Financieros del Departamento de Tesorería del Gobierno de los Estados Unidos [licenció](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) el módulo CipherTrace de Monero a finales de 2022.

La privacidad del gráfico transaccional de Monero está limitada por sus firmas de anillo relativamente pequeñas, especialmente contra ataques dirigidos. Las características de privacidad de Monero también han sido [cuestionadas](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) por algunos investigadores de seguridad, y una serie de vulnerabilidades graves han sido encontradas y corregidas en el pasado, haciendo que las reclamaciones de organizaciones como CipherTrace no están descartadas. Mientras es poco probable que las herramientas de vigilancia masiva de Monero existan como lo hacen para Bitcoin y otras, es seguro que las herramientas de rastreo ayudan en las investigaciones dirigidas.

En última instancia, Monero es el principal candidato para una criptomoneda amigable con la privacidad, pero sus argumentos de privacidad **no** han sido definitivamente comprobados de una manera u otra. Más tiempo e investigación es requerida para encontrar los puntos donde Monero es lo suficientemente resistente a los ataques como para proporcionar la privacidad adecuada.

</details>

### Monero wallets

For optimal privacy, make sure to use a self-custody wallet where the [view key](https://www.getmonero.org/resources/moneropedia/viewkey.html) stays on the device. Esto significa que solo usted tiene la capacidad de gastar sus fondos, además de ver las transacciones entrantes y salientes. If you use a custodial wallet, the provider can see **everything** you do; if you use a “lightweight” wallet where the provider retains your view key, the provider can see almost everything you do (but not spend your funds). Some self-custody wallets where the view key does not leave your device include:

- [Cliente oficial de Monero](https://getmonero.org/downloads) (Escritorio)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, Desktop)
    - Cake Wallet soporta múltiples criptomonedas. En [Monero.com](https://monero.com) está disponible una versión de Cake Wallet exclusiva para Monero para iOS y Android.
- [Feather Wallet](https://featherwallet.org) (Desktop)
- [Monerujo](https://monerujo.io) (Android)

### Monero nodes

For maximum privacy (even with a self-custody wallet), you should run your own Monero node called the [Monero daemon](https://getmonero.org/downloads/#cli). Al utilizar el nodo de otra persona, usted expondrá alguna información a dicha persona, como la dirección IP que utiliza para conectarse, las marcas de tiempo que sincroniza su billetera, y las transacciones que realiza desde su billetera (aunque no hay otros detalles sobre esas transacciones). Alternatively, you can connect to someone else’s Monero node over Tor, [I2P](alternative-networks.md#i2p-the-invisible-internet-project), or a VPN.

### Buying Monero

[General tips for acquiring Monero](advanced/payments.md#acquisition ""){.md-button}

There are numerous centralized exchanges (CEX) as well as P2P marketplaces where you can buy and sell Monero. Some of them require identifying yourself (KYC) to comply with anti-money laundering regulations. However, due to Monero's privacy features, the only thing known to the seller is _that_ you bought Monero, but not how much you own or where you spend it (after it leaves the exchange). Some reputable places to buy Monero include:

- [Kraken](https://kraken.com): A well-known CEX. Registration and KYC are mandatory. Card payments and bank transfers accepted. Make sure not to leave your newly purchased Monero on Kraken's platform after the purchase; withdraw them to a self-custody wallet. Monero is not available in all jurisdictions that Kraken operates in.[^1]
- [Cake Wallet](https://cakewallet.com): A self-custody cross-platform wallet for Monero and other cryptocurrencies. You can buy Monero directly in the app using card payments or bank transfers (through third-party providers such as [Guardarian](https://guardarian.com) or [DFX](https://dfx.swiss)).[^2] KYC is usually not required, but it depends on your country and the amount you are purchasing. In countries where directly purchasing Monero is not possible, you can also use a provider within Cake Wallet to first buy another cryptocurrency such as Bitcoin, Bitcoin Cash, or Litecoin and then exchange it to Monero in-app.
    - [Monero.com](https://monero.com) is an associated website where you can buy Monero and other cryptocurrencies without having to download an app. The funds will simply be sent to the wallet address of your choice.
- [RetoSwap](https://retoswap.com) (formerly known as Haveno-Reto) is a self-custody, decentralized P2P exchange platform based on the [Haveno](https://haveno.exchange) project which is available for Linux, Windows, and macOS. Monero can be bought and sold with maximum privacy, since most trading counterparties do not require KYC, trades are made directly between users (P2P), and all connections run through the Tor network. It is possible to buy Monero via bank transfer, Paypal, or even by paying in cash (meeting in person or sending by mail). Arbitrators can step in to resolve disputes between buyer and seller, but be careful when sharing your bank account or other sensitive information with your trading counterparty. Trading with some accounts may be against those accounts' terms of service. Please note that you can only buy Monero on RetoSwap if you already own a small amount of Monero (currently a minimum of 0.11 XMR) in order to fund security deposits, although there are ongoing efforts to drop this requirement in the future.

## Criterios

**Por favor, tome en cuenta que no estamos asociados con ninguno de los proyectos que recomendamos. ** En adición a [nuestros criterios base](about/criteria.md), hemos desarrollado un claro conjunto de requisitos que nos permiten brindar recomendaciones objetivas. Sugerimos que usted se familiarice con esta lista, antes de elegir utilizar un proyecto y realizar su propia investigación para asegurarse que es la elección ideal para usted.

- Las criptomonedas deben brindar transacciones privadas o imposibles de rastrear por defecto.

<div class="admonition tip" markdown>
<p class="admonition-title">Important notices</p>

The content here is not legal or financial advice. We do not endorse or encourage illicit activities, and we do not endorse or encourage anything which violates a company's terms of service. Check with a professional to confirm that these recommendations are legal and available in your jurisdiction. [See all notices](about/notices.md).

</div>

[^1]: You may refer to the following pages for up-to-date information on countries in which Kraken does **not** allow the purchase of Monero: [Where is Kraken licensed or regulated?](https://support.kraken.com/hc/en-us/articles/where-is-kraken-licensed-or-regulated) and [Support for Monero (XMR) in Europe](https://support.kraken.com/hc/en-us/articles/support-for-monero-xmr-in-europe).
[^2]: You may refer to the following pages for up-to-date information on countries in which Cake Wallet and Monero.com **only** allow the direct purchase of Monero (through third-party providers): [Which countries are served by DFX?](https://docs.dfx.swiss/en/faq.html#which-countries-are-served-by-dfx) and [What are the supported countries/regions? (Guardarian)](https://guardarian.freshdesk.com/support/solutions/articles/80001151826-what-are-the-supported-countries-regions).
