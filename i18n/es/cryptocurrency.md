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
<summary>La resiliencia de Monero a la vigilancia masiva</summary>

En agosto de 2021, CipherTrace [anunció](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) capacidades mejoradas de rastreo de Monero para agencias gubernamentales. Publicaciones públicas muestran cómo la Red de Ejecución de Delitos Financieros del Departamento de Tesorería del Gobierno de los Estados Unidos [licenció](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) el módulo CipherTrace de Monero a finales de 2022.

La privacidad del gráfico transaccional de Monero está limitada por sus firmas de anillo relativamente pequeñas, especialmente contra ataques dirigidos. Las características de privacidad de Monero también han sido [cuestionadas](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) por algunos investigadores de seguridad, y una serie de vulnerabilidades graves han sido encontradas y corregidas en el pasado, haciendo que las reclamaciones de organizaciones como CipherTrace no están descartadas. Mientras es poco probable que las herramientas de vigilancia masiva de Monero existan como lo hacen para Bitcoin y otras, es seguro que las herramientas de rastreo ayudan en las investigaciones dirigidas.

En última instancia, Monero es el principal candidato para una criptomoneda amigable con la privacidad, pero sus argumentos de privacidad **no** han sido definitivamente comprobados de una manera u otra. Más tiempo e investigación es requerida para encontrar los puntos donde Monero es lo suficientemente resistente a los ataques como para proporcionar la privacidad adecuada.

</details>

### Monederos Monero

Para una privacidad óptima, asegúrese de utilizar un monedero de autocustodia en el que la [clave de visualización](https://getmonero.org/resources/moneropedia/viewkey.html) permanezca en el dispositivo. Esto significa que solo usted tiene la capacidad de gastar sus fondos, además de ver las transacciones entrantes y salientes. Si utiliza un monedero de custodia, el proveedor puede ver **todo** lo que hace; si utiliza un monedero «ligero» en el que el proveedor retiene su clave de visualización, el proveedor puede ver casi todo lo que hace (pero no gastar sus fondos). Algunos monederos de autocustodia en los que la clave de visualización no sale de su dispositivo son:

- [Cliente oficial de Monero](https://getmonero.org/downloads) (Escritorio)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, Desktop)
    - Cake Wallet soporta múltiples criptomonedas. En [Monero.com](https://monero.com) está disponible una versión de Cake Wallet exclusiva para Monero para iOS y Android.
- [Feather Wallet](https://featherwallet.org) (Desktop)
- [Monerujo](https://monerujo.io) (Android)

### Nodos Monero

Para obtener la máxima privacidad (incluso con un monedero de autocustodia), debe ejecutar su propio nodo Monero llamado [Monero daemon](https://docs.getmonero.org/interacting/monerod-reference), que se incluye en el [monedero CLI](https://getmonero.org/downloads/#cli). Al utilizar el nodo de otra persona, usted expondrá alguna información a dicha persona, como la dirección IP que utiliza para conectarse, las marcas de tiempo que sincroniza su billetera, y las transacciones que realiza desde su billetera (aunque no hay otros detalles sobre esas transacciones). Alternativamente, puede conectarse al nodo Monero de otra persona a través de [Tor](alternative-networks.md#tor), [I2P](alternative-networks.md#i2p-the-invisible-internet-project) o una [VPN](vpn.md).

### Comprar Monero

[Consejos generales para adquirir Monero](advanced/payments.md#acquisition ""){.md-button}

Existen numerosos intercambios centralizados (CEX), así como mercados P2P donde se puede comprar y vender Monero. Algunas de ellas exigen identificarse (KYC) para cumplir la normativa contra el blanqueo de capitales. Sin embargo, debido a las características de privacidad de Monero, lo único que sabe el vendedor es *que* ha comprado Monero, pero no cuánto posee ni dónde lo gasta (después de que salga del intercambio). Algunos lugares de confianza para comprar Monero son:

- [Kraken](https://kraken.com): Un conocido CEX. El registro y el KYC son obligatorios. Se aceptan pagos con tarjeta y transferencias bancarias. Asegúrese de no dejar sus Monero recién adquiridos en la plataforma de Kraken tras la compra; retírelos a un monedero de autocustodia. Monero no está disponible en todas las jurisdicciones en las que opera Kraken.[^1]
- [Cake Wallet](https://cakewallet.com): Un monedero multiplataforma de autocustodia para Monero y otras criptodivisas. Puede comprar Monero directamente en la aplicación mediante pagos con tarjeta o transferencias bancarias (a través de proveedores externos como [Guardarian](https://guardarian.com) o [DFX](https://dfx.swiss)).[^2] Normalmente no se requiere KYC, pero depende de su país y de la cantidad que vaya a comprar. En los países donde no es posible comprar Monero directamente, también puede utilizar un proveedor dentro de Cake Wallet para comprar primero otra criptomoneda como Bitcoin, Bitcoin Cash o Litecoin y luego cambiarla por Monero en la aplicación.
    - [Monero.com](https://monero.com) es un sitio web asociado en el que puede comprar Monero y otras criptomonedas sin tener que descargar una aplicación. Los fondos se enviarán simplemente a la dirección del monedero que elija.
- [RetoSwap](https://retoswap.com) (antes conocido como Haveno-Reto) es una plataforma de intercambio P2P descentralizada y de autocustodia basada en el proyecto [Haveno](https://haveno.exchange) que está disponible para Linux, Windows y macOS. Monero se puede comprar y vender con la máxima privacidad, ya que la mayoría de las contrapartes comerciales no requieren KYC, las operaciones se realizan directamente entre los usuarios (P2P), y todas las conexiones se ejecutan a través de la red Tor. Es posible comprar Monero mediante transferencia bancaria, PayPal o incluso pagando en efectivo (en persona o por correo). Los árbitros pueden intervenir para resolver disputas entre comprador y vendedor, pero tenga cuidado al compartir su cuenta bancaria u otra información sensible con su contraparte comercial. Operar con algunas cuentas puede ir en contra de las condiciones de servicio de dichas cuentas.

## Criterios

**Por favor, tome en cuenta que no estamos asociados con ninguno de los proyectos que recomendamos. ** En adición a [nuestros criterios base](about/criteria.md), hemos desarrollado un claro conjunto de requisitos que nos permiten brindar recomendaciones objetivas. Sugerimos que usted se familiarice con esta lista, antes de elegir utilizar un proyecto y realizar su propia investigación para asegurarse que es la elección ideal para usted.

- Las criptomonedas deben brindar transacciones privadas o imposibles de rastrear por defecto.

<div class="admonition tip" markdown>
<p class="admonition-title">Avisos importantes</p>

El contenido aquí no constituye asesoramiento jurídico o financiero. No apoyamos ni fomentamos actividades ilícitas, ni nada que infrinja las condiciones de servicio de una empresa. Consulte a un profesional para confirmar que estas recomendaciones son legales y están disponibles en su jurisdicción. [Ver todos los avisos](about/notices.md).

</div>

[^1]: Puede consultar las siguientes páginas para obtener información actualizada sobre los países en los que Kraken **no** permite la compra de Monero: [¿Dónde está Kraken autorizado o regulado?](https://support.kraken.com/hc/en-us/articles/where-is-kraken-licensed-or-regulated) y [Soporte para Monero (XMR) en Europa](https://support.kraken.com/hc/en-us/articles/support-for-monero-xmr-in-europe).
[^2]: Puede consultar las siguientes páginas para obtener información actualizada sobre los países en los que Cake Wallet y Monero.com **solo** permiten la compra directa de Monero (a través de terceros proveedores): [¿Qué países son servidos por DFX?](https://docs.dfx.swiss/en/faq.html#which-countries-are-served-by-dfx) y [¿Cuáles son los países/regiones soportados? (Guardarian)](https://guardarian.freshdesk.com/support/solutions/articles/80001151826-what-are-the-supported-countries-regions).
