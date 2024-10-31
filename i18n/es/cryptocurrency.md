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

Para una mejor privacidad, se debe asegurar de utilizar una billetera no monitorizada donde la clave de visualización permanece en el dispositivo. Esto significa que solo usted tiene la capacidad de gastar sus fondos, además de ver las transacciones entrantes y salientes. Si usted utiliza una billetera monitoreada, el proveedor puede ver **todo** lo que hace; si utiliza una billetera "ligera" donde el proveedor retiene su clave privada de visualización, el proveedor puede ver casi todo lo que hace. Algunas billeteras no monitoreadas son:

- [Cliente oficial de Monero](https://getmonero.org/downloads) (Escritorio)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, macOS)
    - Cake Wallet soporta múltiples criptomonedas. En [Monero.com](https://monero.com) está disponible una versión de Cake Wallet exclusiva para Monero para iOS y Android.
- [Feather Wallet](https://featherwallet.org) (Desktop)
- [Monerujo](https://monerujo.io) (Android)

Para obtener un nivel máximo de privacidad (incluso con una billetera monitoreada), usted debe ejecutar su propio nodo de Monero. Al utilizar el nodo de otra persona, usted expondrá alguna información a dicha persona, como la dirección IP que utiliza para conectarse, las marcas de tiempo que sincroniza su billetera, y las transacciones que realiza desde su billetera (aunque no hay otros detalles sobre esas transacciones). Alternativamente, puede conectarse al nodo Monero de otra persona sobre Tor o [I2P](alternative-networks.md#i2p-the-invisible-internet-project).

En agosto de 2021, CipherTrace [anunció](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) capacidades mejoradas de rastreo de Monero para agencias gubernamentales. Publicaciones públicas muestran cómo la Red de Ejecución de Delitos Financieros del Departamento de Tesorería del Gobierno de los Estados Unidos [licenció](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) el módulo CipherTrace de Monero a finales de 2022.

La privacidad del gráfico transaccional de Monero está limitada por sus firmas de anillo relativamente pequeñas, especialmente contra ataques dirigidos. Las características de privacidad de Monero también han sido [cuestionadas](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) por algunos investigadores de seguridad, y una serie de vulnerabilidades graves han sido encontradas y corregidas en el pasado, haciendo que las reclamaciones de organizaciones como CipherTrace no están descartadas. Mientras es poco probable que las herramientas de vigilancia masiva de Monero existan como lo hacen para Bitcoin y otras, es seguro que las herramientas de rastreo ayudan en las investigaciones dirigidas.

En última instancia, Monero es el principal candidato para una criptomoneda amigable con la privacidad, pero sus argumentos de privacidad **no** han sido definitivamente comprobados de una manera u otra. Más tiempo e investigación es requerida para encontrar los puntos donde Monero es lo suficientemente resistente a los ataques como para proporcionar la privacidad adecuada.

## Criterios

**Por favor, tome en cuenta que no estamos asociados con ninguno de los proyectos que recomendamos. ** En adición a [nuestros criterios base](about/criteria.md), hemos desarrollado un claro conjunto de requisitos que nos permiten brindar recomendaciones objetivas. Sugerimos que usted se familiarice con esta lista, antes de elegir utilizar un proyecto y realizar su propia investigación para asegurarse que es la elección ideal para usted.

- Las criptomonedas deben brindar transacciones privadas o imposibles de rastrear por defecto.
