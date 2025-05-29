---
title: "Resumen de Tor"
icon: 'simple/torproject'
description: Tor es una red descentralizada y gratuita diseñada para utilizar Internet con la mayor privacidad posible.
---

![Logotipo de Tor](../assets/img/self-contained-networks/tor.svg){ align=right }

[**Tor**](../alternative-networks.md#tor) es una red gratuita y descentralizada diseñada para usar el Internet con la mayor privacidad posible. Si se utiliza correctamente, la red permite la navegación y las comunicaciones privadas y anónimas. Debido a que el tráfico de Tor es difícil de bloquear y rastrear, Tor es una herramienta eficaz para eludir la censura.

[:material-movie-open-play-outline: Por qué necesitas Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

Tor funciona enrutando tu tráfico de Internet a través de servidores operados por voluntarios en lugar de establecer una conexión directa con el sitio que intentas visitar. Esto ofusca de dónde viene el tráfico, y ningún servidor en la ruta de conexión es capaz de ver la ruta completa de dónde viene y a dónde va el tráfico, lo que significa que incluso los servidores a los que te estás conectando no pueden romper tu anonimato.

[:octicons-home-16:](https://torproject.org){ .card-link title=Página Principal }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Servicio Onion" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentación}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribuir }

## Conectarse a Tor de Forma Segura

Antes de conectarte a Tor, deberías considerar cuidadosamente lo que buscas lograr con Tor en primer lugar, además de quién estás intentando ocultar tu actividad en la red.

If you live in a free country, are accessing mundane content via Tor, aren't worried about your ISP or local network administrators having the knowledge that you're using Tor, and want to help [destigmatize](https://2019.www.torproject.org/about/torusers.html.en) Tor usage, you can likely connect to Tor directly via standard means like [Tor Browser](../tor.md) without worry.

Si tienes la posibilidad de acceder a un proveedor VPN de confianza y **cualquiera** de los siguientes es cierto, casi seguro que deberías conectarte a Tor a través de una VPN:

- Ya utilizas un [proveedor VPN de confianza](../vpn.md)
- Tu modelo de amenaza incluye un adversario capaz de extraer información de tu ISP
- Tu modelo de amenaza incluye al propio ISP como adversario
- Tu modelo de amenaza incluye a los administradores de la red local antes que a tu ISP como adversario

Como ya [generalmente recomendamos](../basics/vpn-overview.md) que la gran mayoría de la gente use un proveedor VPN de confianza por una variedad de razones, la siguiente recomendación sobre conectarse a Tor a través de una VPN probablemente se aplique a ti. <mark>No hay necesidad de desactivar tu VPN antes de conectarte a Tor</mark>, como algunos recursos en línea te hacen creer.

Conectarse directamente a Tor hará que tu conexión destaque ante cualquier administrador de red local o tu ISP. Detectar y correlacionar este tráfico [se ha hecho](https://edition.cnn.com/2013/12/17/justice/massachusetts-harvard-hoax) en el pasado por administradores de red para identificar y desanonimizar usuarios Tor específicos en su red. Por otra parte, conectarse a una VPN es casi siempre menos sospechoso, porque los proveedores comerciales de VPN son utilizados por los consumidores cotidianos para una variedad de tareas mundanas como eludir las restricciones geográficas, incluso en países con fuertes restricciones de Internet.

Por lo tanto, debes hacer un esfuerzo para ocultar tu dirección IP **antes de** conectarte a la red Tor. You can do this by simply connecting to a VPN (through a client installed on your computer) and then accessing [Tor](../tor.md) as normal (e.g., through Tor Browser). This creates a connection chain like so:

- [x] Tú → VPN → Tor → Internet

Desde la perspectiva de tu ISP, parece que estás accediendo normalmente a una VPN (con la cobertura asociada que te proporciona). Desde la perspectiva de tu VPN, pueden ver que te estás conectando a la red Tor, pero nada sobre a qué sitios web estás accediendo. Desde la perspectiva de Tor, te estás conectando normalmente, pero en el improbable caso de algún tipo de compromiso de la red Tor, sólo la IP de tu VPN estaría expuesta, y tu VPN *adicionalmente* tendría que ser comprometida para desanonimizarte.

This is **not** censorship circumvention advice because if Tor is blocked entirely by your ISP, your VPN likely is as well. Más bien, esta recomendación tiene como objetivo hacer que tu tráfico se mezcle mejor con el tráfico común de usuarios VPN, y proporcionarte un cierto nivel de negación plausible ocultando el hecho de que se está conectando a Tor a tu ISP.

---

Nosotros **desaconsejamos encarecidamente** combinar Tor con una VPN de cualquier otra manera. No configures tu conexión de forma que se parezca a ninguna de las siguientes:

- Tú → Tor → VPN → Internet
- Tú → VPN → Tor → VPN → Internet
- Cualquier otra configuración

Some VPN providers and other publications will occasionally recommend these **bad** configurations to evade Tor bans (i.e., exit nodes being blocked by websites) in some places. [Normalmente](https://support.torproject.org/#about_change-paths), Tor cambia frecuentemente la ruta de tu circuito a través de la red. Cuando eliges una VPN de *destino* permanente (conectándote a un servidor VPN *después de* Tor), estás eliminando esta ventaja y perjudicando drásticamente tu anonimato.

Es difícil establecer malas configuraciones como estas accidentalmente, porque normalmente implica establecer configuraciones proxy personalizadas dentro del Navegador Tor, o establecer configuraciones proxy personalizadas dentro de tu cliente VPN que enruta tu tráfico VPN a través de Tor Browser. Mientras evites estas configuraciones no predeterminadas, probablemente estarás bien.

---

<div class="admonition info" markdown>
<p class="admonition-title">Huella Digital VPN/SSH</p>

El Proyecto Tor [notes](https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN#vpnssh-fingerprinting) que *teóricamente* usar una VPN para ocultar las actividades Tor de tu ISP puede no ser infalible. VPNs have been found to be vulnerable to website traffic fingerprinting, where an adversary can still guess what website is being visited because all websites have specific traffic patterns.

Por lo tanto, no es descabellado creer que el tráfico Tor encriptado oculto por una VPN también podría ser detectado mediante métodos similares. No existen trabajos de investigación sobre este tema, y seguimos considerando que las ventajas de utilizar una VPN superan con creces estos riesgos, pero es algo a tener en cuenta.

Si todavía crees que los "pluggable transports" (puentes) proporcionan una protección adicional contra la huella digital del tráfico del sitio web que una VPN no proporciona, siempre tienes la opción de utilizar un puente **y** una VPN conjuntamente.

</div>

Determinar si deberías usar primero una VPN para conectarte a la red Tor requerirá algo de sentido común y conocimiento de las políticas de tu propio gobierno e ISP en relación a lo que te estás conectando. To reiterate, though, you will be better off being seen as connecting to a commercial VPN network than directly to the Tor network in most cases. If VPN providers are censored in your area, then you can also consider using Tor pluggable transports (e.g., Snowflake or meek bridges) as an alternative, but using these bridges may arouse more suspicion than standard WireGuard/OpenVPN tunnels.

## Qué No es Tor

The Tor network is not the perfect privacy protection tool in all cases and has a number of drawbacks which should be carefully considered. Estas cosas no deberían disuadirte de usar Tor si es apropiado para tus necesidades, pero siguen siendo cosas en las que pensar cuando decidas qué solución es la más apropiada para ti.

### Tor no es una VPN gratuita

El lanzamiento de la aplicación móvil *Orbot* ha llevado a mucha gente a describir Tor como una "VPN gratuita" para todo el tráfico de su dispositivo. Sin embargo, tratar Tor de esta manera plantea algunos peligros en comparación con una VPN típica.

A diferencia de los nodos de salida de Tor, los proveedores de VPN no suelen ser *activamente* [maliciosos](#caveats). Dado que los nodos de salida de Tor pueden ser creados por cualquiera, son puntos calientes para el registro y modificación de la red. En 2020, se documentó que muchos nodos de salida de Tor degradaban el tráfico HTTPS a HTTP para [secuestrar transacciones de criptomonedas](https://therecord.media/thousands-of-tor-exit-nodes-attacked-cryptocurrency-users-over-the-past-year). También se han observado otros ataques a nodos de salida, como la sustitución de descargas a través de canales no cifrados por malware. HTTPS mitiga estas amenazas hasta cierto punto.

Como ya hemos aludido, Tor también es fácilmente identificable en la red. A diferencia de un proveedor VPN real, usar Tor te hará destacar como una persona que probablemente intenta evadir a las autoridades. In a perfect world, Tor would be seen by network administrators and authorities as a tool with many uses (like how VPNs are viewed), but in reality the perception of Tor is still far less legitimate than the perception of commercial VPNs. As such, using a real VPN provides you with plausible deniability, e.g. "I was just using it to watch Netflix," etc.

### El uso de Tor no es indetectable

**Even if you use bridges and pluggable transports,** the Tor Project doesn't provide any tools to hide the fact that you are using Tor from your ISP. Ni siquiera el uso de "transportes conectables" ofuscados o puentes no públicos ocultan el hecho de que se está utilizando un canal de comunicaciones privado. Los transportes conectables más populares como obfs4 (que ofusca tu tráfico para que "parezca nada") y meek (que utiliza "domain fronting" para camuflar tu tráfico) pueden ser [detectados](https://hackerfactor.com/blog/index.php?/archives/889-Tor-0day-Burning-Bridges.html) con técnicas de análisis de tráfico bastante estándar. Snowflake tiene problemas similares, y puede [detectarse fácilmente](https://hackerfactor.com/blog/index.php?/archives/944-Tor-0day-Snowflake.html) incluso *antes de* que se establezca una conexión Tor.

Existen transportes conectables distintos de estos tres, pero normalmente se basan en la seguridad a través de la oscuridad para eludir la detección. They aren't impossible to detect—they are just used by so few people that it's not worth the effort building detectors for them. No se debe confiar en ellos si te están vigilando específicamente.

Es fundamental comprender la diferencia entre eludir la censura y eludir la detección. Es más fácil lograr lo primero debido a las muchas limitaciones del mundo real sobre lo que los censores de red pueden hacer en masa, pero estas técnicas no ocultan el hecho de que tú-*específicamente* tú-estás usando Tor de una parte interesada que monitoriza tu red.

### Tor Browser no es el navegador más *seguro*

Anonymity can often be at odds with security: Tor's anonymity requires every user to be identical, which creates a monoculture (e.g., the same bugs are present across all Tor Browser users). Como regla general de ciberseguridad, las monoculturas suelen considerarse malas: La seguridad a través de la diversidad (de la que carece Tor) proporciona una segmentación natural al limitar las vulnerabilidades a grupos más pequeños, y por lo tanto suele ser deseable, pero esta diversidad también es menos buena para el anonimato.

Adicionalmente, Tor Browser está basado en la versión de Soporte Extendido de Firefox, que solo recibe parches para vulnerabilidades consideradas *Críticas* y *Altas* (no *Medias* y *Bajas*). Esto significa que los atacantes podrían (por ejemplo):

1. Buscar nuevas vulnerabilidades Críticas/Altas en las versiones nightly o beta de Firefox, luego comprobar si son explotables en Tor Browser (este periodo de vulnerabilidad puede durar semanas).
2. Encadenar *múltiples* vulnerabilidades Medias/Bajas hasta conseguir el nivel de acceso que buscan (este periodo de vulnerabilidad puede durar meses o más).

Those at risk of browser vulnerabilities should consider additional protections to defend against Tor Browser exploits, such as using Whonix in [Qubes](../os/qubes-overview.md) to contain your Tor browsing in a secure virtual machine and protect against leaks.

## Creación de Rutas a los Servicios Clearnet

Los "servicios Clearnet" son sitios web a los que puedes acceder con cualquier navegador, como [privacyguides.org](https://www.privacyguides.org). Tor te permite conectarte a estos sitios web de forma anónima enrutando tu tráfico a través de una red compuesta por miles de servidores gestionados por voluntarios llamados nodos (o repetidores).

Cada vez que [te conectes a Tor](../tor.md), este elegirá tres nodos para construir una ruta a Internet-esta ruta se llama "circuito"

<figure markdown>
  ![Ruta de Tor que muestra tu dispositivo conectándose a un nodo de entrada, un nodo medio y un nodo de salida antes de llegar al sitio web de destino](../assets/img/how-tor-works/tor-path.svg#only-light)
  ![Ruta de Tor que muestra tu dispositivo conectándose a un nodo de entrada, un nodo medio y un nodo de salida antes de llegar al sitio web de destino](../assets/img/how-tor-works/tor-path-dark.svg#only-dark)
  <figcaption>Ruta del circuito de Tor</figcaption>
</figure>

Cada uno de estos nodos tiene su propia función:

### El nodo de entrada

El nodo de entrada, a menudo llamado nodo de guardia, es el primer nodo al que se conecta tu cliente Tor. El nodo de entrada puede ver tu dirección IP, pero no puede ver a qué te estás conectando.

A diferencia de los otros nodos, el cliente Tor seleccionará aleatoriamente un nodo de entrada y se quedará con él durante dos o tres meses para protegerte de ciertos ataques.[^1]

### El nodo medio

El nodo del medio es el segundo nodo al que se conecta tu cliente Tor. Puede ver de qué nodo procede el tráfico -el nodo de entrada- y a qué nodo se dirige a continuación. El nodo intermedio no puede, ver tu dirección IP o el dominio al que te estás conectando.

Para cada nuevo circuito, el nodo central se selecciona aleatoriamente de entre todos los nodos Tor disponibles.

### El nodo de salida

El nodo de salida es el punto en el que tu tráfico web abandona la red Tor y es reenviado a su destino deseado. El nodo de salida no puede ver tu dirección IP, pero sí sabe a qué sitio te estás conectando.

El nodo de salida será elegido al azar de entre todos los nodos Tor disponibles ejecutados con una bandera de retransmisión de salida.[^2]

## Creación de Rutas a los Servicios Onion

Los "Servicios Onion" (también conocidos comúnmente como "servicios ocultos") son sitios web a los que solo se puede acceder mediante el navegador Tor. Estos sitios web tienen un nombre de dominio largo generado aleatoriamente que termina en `.onion`.

Conectarse a un Servicio Onion en Tor funciona de forma muy similar a conectarse a un servicio clearnet, pero tu tráfico se enruta a través de un total de **seis nodos** antes de llegar al servidor de destino. Just like before, however, only three of these nodes are contributing to *your* anonymity, the other three nodes protect *the Onion Service's* anonymity, hiding the website's true IP and location in the same manner that Tor Browser is hiding yours.

<figure style="width:100%" markdown>
  ![Ruta de Tor que muestra tu tráfico siendo enrutado a través de tus tres nodos Tor más tres nodos Tor adicionales que ocultan la identidad del sitio web](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![Ruta de Tor que muestra tu tráfico siendo enrutado a través de tus tres nodos Tor más tres nodos Tor adicionales que ocultan la identidad del sitio web](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Ruta del circuito de Tor con Servicios Onion. Los nodos de la valla <span class="pg-blue">azul</span> pertenecen a tu navegador, mientras que los nodos de la valla <span class="pg-red">roja</span> pertenecen al servidor, por lo que su identidad está oculta para ti.</figcaption>
</figure>

## Cifrado

Tor encrypts each packet (a block of transmitted data) three times with the keys from the exit, middle, and entry node in that order.

Una vez que Tor ha construido un circuito, la transmisión de datos se realiza de la siguiente manera:

1. Firstly: When the packet arrives at the entry node, the first layer of encryption is removed. En este paquete encriptado, el nodo de entrada encontrará otro paquete encriptado con la dirección del nodo intermedio. El nodo de entrada reenviará entonces el paquete al nodo intermedio.

2. Secondly: When the middle node receives the packet from the entry node, it too will remove a layer of encryption with its key, and this time finds an encrypted packet with the exit node's address. El nodo intermedio reenviará entonces el paquete al nodo de salida.

3. Lastly: When the exit node receives its packet, it will remove the last layer of encryption with its key. El nodo de salida verá la dirección de destino y reenviará el paquete a esa dirección.

A continuación se presenta un diagrama alternativo que muestra el proceso. Cada nodo elimina su propia capa de encriptación, y cuando el servidor de destino devuelve los datos, el mismo proceso ocurre completamente a la inversa. Por ejemplo, el nodo de salida no sabe quién eres, pero sí sabe de qué nodo procede, por lo que añade su propia capa de encriptación y lo envía de vuelta.

<figure markdown>
  ![Tor encryption](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![Tor encryption](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>Envío y recepción de datos a través de la red Tor</figcaption>
</figure>

Tor nos permite conectarnos a un servidor sin que nadie conozca la ruta completa. El nodo de entrada sabe quién eres, pero no a dónde vas; el nodo intermedio no sabe quién eres ni a dónde vas; y el nodo de salida sabe a dónde vas, pero no quién eres. Como el nodo de salida es el que realiza la conexión final, el servidor de destino nunca conocerá tu dirección IP.

## Advertencias

Aunque Tor proporciona fuertes garantías de privacidad, uno debe ser consciente de que Tor no es perfecto:

- Tor nunca te protege de exponerte por error, como por ejemplo si compartes demasiada información sobre tu identidad real.
- Los nodos de salida de Tor pueden **modificar** el tráfico no encriptado que pasa a través de ellos. Esto significa que el tráfico que no está cifrado, como el tráfico HTTP plano, puede ser modificado por un nodo de salida malicioso. **Nunca** descargues archivos de un sitio web sin cifrar `http://` a través de Tor, y asegúrate de que tu navegador está configurado para actualizar siempre el tráfico HTTP a HTTPS.
- Los nodos de salida de Tor también pueden monitorear el tráfico que pasa a través de ellos. El tráfico no cifrado que contenga información personal identificable puede desanonimizarte hasta ese nodo de salida. De nuevo, recomendamos usar solo HTTPS sobre Tor.
- Poderosos adversarios con la capacidad de vigilar pasivamente *todo* el tráfico de red alrededor del globo ("Adversarios Pasivos Globales") **no** son algo contra lo que Tor te proteja (y usar Tor [con una VPN](#safely-connecting-to-tor) no cambia este hecho).
- Los adversarios bien financiados con la capacidad de observar pasivamente la *mayoría* del tráfico de red en todo el mundo todavía tienen una *oportunidad* de desanonimizar a los usuarios de Tor mediante el análisis avanzado del tráfico.

Si deseas utilizar Tor para navegar por la web, sólo recomendamos el navegador Tor Browser **oficial**-está diseñado para evitar las huellas digitales.

- [Tor Browser :material-arrow-right-drop-circle:](../tor.md#tor-browser)

### Protecciones que ofrecen los puentes

Los puentes Tor se promocionan comúnmente como un método alternativo para ocultar el uso de Tor a un ISP, en lugar de una VPN (como sugerimos usar si es posible). Algo a tener en cuenta es que aunque los puentes pueden proporcionar una adecuada elusión de la censura, esto es solo un beneficio *transitorio*. No te protegen adecuadamente de que tu ISP descubra que te conectaste a Tor en el *pasado* con análisis de registros históricos de tráfico.

Para ilustrar este punto, considera el siguiente escenario: Te conectas a Tor a través de un puente, y tu ISP no lo detecta porque no están haciendo un análisis sofisticado de tu tráfico, por lo que las cosas están funcionando como estaba previsto. Ahora, pasan 4 meses, y la IP de tu puente se ha hecho pública. This is a very common occurrence with bridges; they are discovered and blocked relatively frequently, just not immediately.

Tu ISP quiere identificar a los usuarios de Tor de hace 4 meses, y con su limitado registro de metadatos pueden ver que te conectaste a una dirección IP que más tarde se reveló que era un puente Tor. Prácticamente no tienes otra excusa para estar haciendo esa conexión, así que el ISP puede decir con mucha confianza que eras un usuario de Tor en ese momento.

Contrasta esto con nuestro escenario recomendado, donde te conectas a Tor a través de una VPN. Digamos que 4 meses más tarde tu ISP de nuevo quiere identificar a cualquiera que usó Tor hace 4 meses. Es casi seguro que sus registros puedan identificar tu tráfico de hace 4 meses, pero lo único que podrían ver es que te conectaste a la dirección IP de una VPN. Esto se debe a que la mayoría de los ISP solo conservan los metadatos durante largos periodos de tiempo, no el contenido completo del tráfico solicitado. Almacenar la totalidad de tus datos de tráfico requeriría una cantidad masiva de almacenamiento que casi todos los actores de amenazas no poseerían.

Como es casi seguro que tu ISP no está capturando todos los datos a nivel de paquete y almacenándolos para siempre, no tienen forma de determinar a qué te has conectado con esa VPN *después de* haberlo hecho con una técnica avanzada como la inspección profunda de paquetes, y por lo tanto tienes una negación plausible.

Por lo tanto, los puentes proporcionan el mayor beneficio a la hora de eludir la censura en Internet *en el momento*, pero no son un sustituto adecuado para **todos** los beneficios que puede proporcionar el uso de una VPN junto con Tor. Again, this is not advice *against* using Tor bridges—you should just be aware of these limitations while making your decision. En algunos casos, los puentes pueden ser la*única * opción (si todos los proveedores de VPN están bloqueados, por ejemplo), así que puedes seguir utilizándolos en esas circunstancias teniendo en cuenta esta limitación.

Si crees que un puente puede ayudarte a defenderte contra el fingerprinting (huella digital) u otros análisis avanzados de red más de lo que ya lo hace el túnel encriptado de una VPN, siempre tienes la opción de utilizar también un puente junto con una VPN. De este modo, seguirás protegido por las técnicas de ofuscación del transporte conectable, incluso si un adversario consigue algún nivel de visibilidad en tu túnel VPN. Si decides seguir este camino, te recomendamos que te conectes a un puente obfs4 detrás de tu VPN para obtener una protección óptima contra huellas digitales, en lugar de meek o Snowflake.

Es [posible](https://discuss.privacyguides.net/t/clarify-tors-weaknesses-with-respect-to-observability/3676/16) que el transporte conectable [WebTunnel](https://forum.torproject.org/t/tor-relays-announcement-webtunnel-a-new-pluggable-transport-for-bridges-now-available-for-deployment/8180) que se está probando actualmente pueda mitigar algunas de estas preocupaciones. Seguiremos atentos a la evolución de esta tecnología.

## Recursos Adicionales

- [Manual del usuario del navegador Tor](https://tb-manual.torproject.org)
- [Cómo Funciona Tor - Computerphile](https://youtube.com/watch?v=QRYzre4bf7I) <small>(YouTube)</small>
- [Servicios Tor Onion - Computerphile](https://youtube.com/watch?v=lVcbq_a5N9I) <small>(YouTube)</small>

[^1]: El primer repetidor en tu circuito se llama "guardia de entrada" o "guardia". Es un repetidor rápido y estable que se mantiene como el primero en tu circuito durante 2-3 meses para protegerse de un ataque conocido de ruptura del anonimato. El resto de tu circuito cambia con cada nuevo sitio web que visitas, y todos juntos estos repetidores proporcionan las protecciones de privacidad completas de Tor. Para obtener más información sobre el funcionamiento de los repetidores de protección, consulta esta [entrada del blog](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) y el [documento](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf) sobre los guardias de entrada. ([https://support.torproject.org/tbb/tbb-2](https://support.torproject.org/tbb/tbb-2))

[^2]: Bandera de repetidor: una (des)calificación de los repetidores para las posiciones de los circuitos (por ejemplo, "Guardia", "Salida", "MalaSalida"), las propiedades de los circuitos (por ejemplo, "Rápido", "Estable"), o los roles (por ejemplo, "Autoridad", "HSDir"), tal y como los asignan las autoridades de los directorios y se definen con más detalle en la especificación del protocolo del directorio. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html#relay-flag))
