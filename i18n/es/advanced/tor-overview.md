---
title: "Resumen de Tor"
icon: 'simple/torproject'
description: Tor es una red descentralizada y gratuita diseñada para utilizar Internet con la mayor privacidad posible.
---

Tor es una red descentralizada y gratuita diseñada para utilizar Internet con la mayor privacidad posible. Si se utiliza correctamente, la red permite la navegación y las comunicaciones privadas y anónimas.

## Conectarse a Tor de Forma Segura

Antes de conectarte a [Tor](../tor.md), deberías considerar cuidadosamente qué estás buscando conseguir usando Tor en primer lugar, y a quién estás intentando ocultar tu actividad en la red.

Si vives en un país libre, accedes a contenido mundano a través de Tor, no te preocupa que tu ISP o los administradores de tu red local sepan que estás usando Tor, y quieres ayudar a [a desestigmatizar](https://2019.www.torproject.org/about/torusers.html.en) el uso de Tor, probablemente puedes conectarte a Tor directamente a través de medios estándar como [Tor Browser](../tor.md) sin preocuparte.

Si tienes la posibilidad de acceder a un proveedor VPN de confianza y **cualquiera** de los siguientes es cierto, casi seguro que deberías conectarte a Tor a través de una VPN:

- Ya utilizas un [proveedor VPN de confianza](../vpn.md)
- Tu modelo de amenaza incluye un adversario capaz de extraer información de tu ISP
- Tu modelo de amenaza incluye al propio ISP como adversario
- Tu modelo de amenaza incluye a los administradores de la red local antes que a tu ISP como adversario

Como ya [generalmente recomendamos](../basics/vpn-overview.md) que la gran mayoría de la gente use un proveedor VPN de confianza por una variedad de razones, la siguiente recomendación sobre conectarse a Tor a través de una VPN probablemente se aplique a ti. <mark>No hay necesidad de desactivar tu VPN antes de conectarte a Tor</mark>, como algunos recursos en línea te hacen creer.

Conectarse directamente a Tor hará que tu conexión destaque ante cualquier administrador de red local o tu ISP. Detectar y correlacionar este tráfico [se ha hecho](https://edition.cnn.com/2013/12/17/justice/massachusetts-harvard-hoax/) en el pasado por administradores de red para identificar y desanonimizar usuarios Tor específicos en su red. Por otra parte, conectarse a una VPN es casi siempre menos sospechoso, porque los proveedores comerciales de VPN son utilizados por los consumidores cotidianos para una variedad de tareas mundanas como eludir las restricciones geográficas, incluso en países con fuertes restricciones de Internet.

Por lo tanto, debes hacer un esfuerzo para ocultar tu dirección IP **antes de** conectarte a la red Tor. Puedes hacerlo simplemente conectándote a una VPN (a través de un cliente instalado en tu ordenador) y luego accediendo a [Tor](../tor.md) de forma normal, a través de Tor Browser, por ejemplo. Esto crea una cadena de conexión como:

- [x] Tú → VPN → Tor → Internet

Desde la perspectiva de tu ISP, parece que estás accediendo normalmente a una VPN (con la cobertura asociada que te proporciona). Desde la perspectiva de tu VPN, pueden ver que te estás conectando a la red Tor, pero nada sobre a qué sitios web estás accediendo. Desde la perspectiva de Tor, te estás conectando normalmente, pero en el improbable caso de algún tipo de compromiso de la red Tor, sólo la IP de tu VPN estaría expuesta, y tu VPN *adicionalmente* tendría que ser comprometida para desanonimizarte.

Esto **no** es un consejo para eludir la censura, porque si Tor está bloqueado completamente por tu ISP, tu VPN probablemente también lo esté. Más bien, esta recomendación tiene como objetivo hacer que tu tráfico se mezcle mejor con el tráfico común de usuarios VPN, y proporcionarte un cierto nivel de negación plausible ocultando el hecho de que se está conectando a Tor a tu ISP.

---

Nosotros **desaconsejamos encarecidamente** combinar Tor con una VPN de cualquier otra manera. No configures tu conexión de forma que se parezca a ninguna de las siguientes:

- Tú → Tor → VPN → Internet
- Tú → VPN → Tor → VPN → Internet
- Cualquier otra configuración

Algunos proveedores de VPN y otras publicaciones recomendarán ocasionalmente estas **malas** configuraciones para evadir las prohibiciones de Tor (nodos de salida bloqueados por sitios web) en algunos lugares. [Normalmente](https://support.torproject.org/#about_change-paths), Tor cambia frecuentemente la ruta de tu circuito a través de la red. Cuando eliges una VPN de *destino* permanente (conectándote a un servidor VPN *después de* Tor), estás eliminando esta ventaja y perjudicando drásticamente tu anonimato.

Es difícil establecer malas configuraciones como estas accidentalmente, porque normalmente implica establecer configuraciones proxy personalizadas dentro del Navegador Tor, o establecer configuraciones proxy personalizadas dentro de tu cliente VPN que enruta tu tráfico VPN a través de Tor Browser. Mientras evites estas configuraciones no predeterminadas, probablemente estarás bien.

---

!!! info "Huella digital VPN/SSH"

    El Proyecto Tor [notes](https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN#vpnssh-fingerprinting) que *teóricamente* usar una VPN para ocultar las actividades Tor de tu ISP puede no ser infalible. Se ha descubierto que las VPN son vulnerables a las huellas digitales de tráfico de sitios web, en las que un adversario puede adivinar qué sitio web se está visitando, ya que todos los sitios web tienen patrones de tráfico específicos.
    
    Por lo tanto, no es descabellado creer que el tráfico Tor encriptado oculto por una VPN también podría ser detectado mediante métodos similares. No existen trabajos de investigación sobre este tema, y seguimos considerando que las ventajas de utilizar una VPN superan con creces estos riesgos, pero es algo a tener en cuenta.
    
    Si todavía crees que los "pluggable transports" (puentes) proporcionan una protección adicional contra la huella digital del tráfico del sitio web que una VPN no proporciona, siempre tienes la opción de utilizar un puente **y** una VPN conjuntamente.

Determinar si deberías usar primero una VPN para conectarte a la red Tor requerirá algo de sentido común y conocimiento de las políticas de tu propio gobierno e ISP en relación a lo que te estás conectando. Sin embargo, de nuevo, en la mayoría de los casos será mejor que te vean conectándose a una red VPN comercial que directamente a la red Tor. Si los proveedores VPN están censurados en tu área, entonces también puedes considerar usar "pluggable transports" Tor (p.e. Snowflake o meek bridges) como alternativa, pero usar estos puentes puede levantar más sospechas que los túneles estándar WireGuard/OpenVPN.

## Qué No es Tor

La red Tor no es la herramienta perfecta de protección de la privacidad en todos los casos, y tiene una serie de inconvenientes que deben ser considerados cuidadosamente. Estas cosas no deberían disuadirte de usar Tor si es apropiado para tus necesidades, pero siguen siendo cosas en las que pensar cuando decidas qué solución es la más apropiada para ti.

### Tor no es una VPN gratuita

El lanzamiento de la aplicación móvil *Orbot* ha llevado a mucha gente a describir Tor como una "VPN gratuita" para todo el tráfico de su dispositivo. Sin embargo, tratar Tor de esta manera plantea algunos peligros en comparación con una VPN típica.

A diferencia de los nodos de salida de Tor, los proveedores de VPN no suelen ser *activamente* [maliciosos](#caveats). Dado que los nodos de salida de Tor pueden ser creados por cualquiera, son puntos calientes para el registro y modificación de la red. En 2020, se documentó que muchos nodos de salida de Tor degradaban el tráfico HTTPS a HTTP para [secuestrar transacciones de criptomonedas](https://therecord.media/thousands-of-tor-exit-nodes-attacked-cryptocurrency-users-over-the-past-year). También se han observado otros ataques a nodos de salida, como la sustitución de descargas a través de canales no cifrados por malware. HTTPS mitiga estas amenazas hasta cierto punto.

Como ya hemos aludido, Tor también es fácilmente identificable en la red. A diferencia de un proveedor VPN real, usar Tor te hará destacar como una persona que probablemente intenta evadir a las autoridades. En un mundo perfecto, Tor sería visto por los administradores de red y las autoridades como una herramienta con muchos usos (como se ven las VPN), pero en realidad la percepción de Tor sigue siendo mucho menos legítima que la percepción de las VPN comerciales, por lo que usar una VPN real te proporciona una negación plausible, por ejemplo, "solo la estaba usando para ver Netflix", etc.

### El uso de Tor no es indetectable

**Incluso si usas puentes y transportes conectables (pluggable transports),** el Proyecto Tor no proporciona herramientas para ocultar a tu ISP el hecho de que estás usando Tor. Ni siquiera el uso de "transportes conectables" ofuscados o puentes no públicos ocultan el hecho de que se está utilizando un canal de comunicaciones privado. Los transportes conectables más populares como obfs4 (que ofusca tu tráfico para que "parezca nada") y meek (que utiliza "domain fronting" para camuflar tu tráfico) pueden ser [detectados](https://www.hackerfactor.com/blog/index.php?/archives/889-Tor-0day-Burning-Bridges.html) con técnicas de análisis de tráfico bastante estándar. Snowflake tiene problemas similares, y puede ser [fácilmente detectado](https://www.hackerfactor.com/blog/index.php?/archives/944-Tor-0day-Snowflake.html) *antes de que* se establezca una conexión Tor.

Pluggable transports other than these three do exist, but typically rely on security through obscurity to evade detection. They aren't impossible to detect, they are just used by so few people that it's not worth the effort building detectors for them. They shouldn't be relied upon if you specifically are being monitored.

It is critical to understand the difference between bypassing censorship and evading detection. It is easier to accomplish the former because of the many real-world limitations on what network censors can realistically do en masse, but these techniques do not hide the fact that you—*specifically* you—are using Tor from an interested party monitoring your network.

### Tor Browser is not the most *secure* browser

Anonymity can often be at odds with security: Tor's anonymity requires every user to be identical, which creates a monoculture (the same bugs are present across all Tor Browser users). As a cybersecurity rule of thumb, monocultures are generally regarded as bad: Security through diversity (which Tor lacks) provides natural segmentation by limiting vulnerabilities to smaller groups, and is therefore usually desirable, but this diversity is also less good for anonymity.

Additionally, Tor Browser is based on Firefox's Extended Support Release builds, which only receives patches for vulnerabilities considered *Critical* and *High* (not *Medium* and *Low*). This means that attackers could (for example):

1. Look for new Critical/High vulnerabilities in Firefox nightly or beta builds, then check if they are exploitable in Tor Browser (this vulnerability period can last weeks).
2. Chain *multiple* Medium/Low vulnerabilities together until they get the level of access they're looking for (this vulnerability period can last months or longer).

Those at risk of browser vulnerabilities should consider additional protections to defend against Tor Browser exploits, such as using Whonix in [Qubes](../os/qubes-overview.md) to contain your Tor browsing in a secure VM and protect against leaks.

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

Conectarse a un Servicio Onion en Tor funciona de forma muy similar a conectarse a un servicio clearnet, pero tu tráfico se enruta a través de un total de **seis nodos** antes de llegar al servidor de destino. Sin embargo, al igual que antes, solo tres de estos nodos contribuyen a *tu* anonimato, los otros tres nodos protegen el anonimato del *Servicio Onion*, ocultando la verdadera IP y la ubicación del sitio web de la misma manera que Tor Browser oculta la tuya.

<figure style="width:100%" markdown>
  ![Ruta de Tor que muestra tu tráfico siendo enrutado a través de tus tres nodos Tor más tres nodos Tor adicionales que ocultan la identidad del sitio web](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![Ruta de Tor que muestra tu tráfico siendo enrutado a través de tus tres nodos Tor más tres nodos Tor adicionales que ocultan la identidad del sitio web](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Ruta del circuito de Tor con Servicios Onion. Los nodos de la valla <span class="pg-blue">azul</span> pertenecen a tu navegador, mientras que los nodos de la valla <span class="pg-red">roja</span> pertenecen al servidor, por lo que su identidad está oculta para ti.</figcaption>
</figure>

## Cifrado

Tor encripta cada paquete (un bloque de datos transmitidos) tres veces con las claves del nodo de salida, medio y de entrada, en ese orden.

Una vez que Tor ha construido un circuito, la transmisión de datos se realiza de la siguiente manera:

1. En primer lugar: cuando el paquete llega al nodo de entrada, se elimina la primera capa de cifrado. En este paquete encriptado, el nodo de entrada encontrará otro paquete encriptado con la dirección del nodo intermedio. El nodo de entrada reenviará entonces el paquete al nodo intermedio.

2. Segundo: cuando el nodo intermedio recibe el paquete del nodo de entrada, también elimina una capa de encriptación con su clave, y esta vez encuentra un paquete encriptado con la dirección del nodo de salida. El nodo intermedio reenviará entonces el paquete al nodo de salida.

3. Por último, cuando el nodo de salida reciba su paquete, eliminará la última capa de cifrado con su clave. El nodo de salida verá la dirección de destino y reenviará el paquete a esa dirección.

A continuación se presenta un diagrama alternativo que muestra el proceso. Cada nodo elimina su propia capa de encriptación, y cuando el servidor de destino devuelve los datos, el mismo proceso ocurre completamente a la inversa. Por ejemplo, el nodo de salida no sabe quién eres, pero sí sabe de qué nodo procede, por lo que añade su propia capa de encriptación y lo envía de vuelta.

<figure markdown>
  ![Tor encryption](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![Tor encryption](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>Envío y recepción de datos a través de la red Tor</figcaption>
</figure>

Tor nos permite conectarnos a un servidor sin que nadie conozca la ruta completa. El nodo de entrada sabe quién eres, pero no a dónde vas; el nodo intermedio no sabe quién eres ni a dónde vas; y el nodo de salida sabe a dónde vas, pero no quién eres. Como el nodo de salida es el que realiza la conexión final, el servidor de destino nunca conocerá tu dirección IP.

## Advertencias

Aunque Tor proporciona fuertes garantías de privacidad, uno debe ser consciente de que Tor no es perfecto:

- Tor never protects you from exposing yourself by mistake, such as if you share too much information about your real identity.
- Tor exit nodes can **modify** unencrypted traffic which passes through them. This means traffic which is not encrypted, such as plain HTTP traffic, can be changed by a malicious exit node. **Never** download files from an unencrypted `http://` website over Tor, and ensure your browser is set to always upgrade HTTP traffic to HTTPS.
- Los nodos de salida de Tor también pueden monitorear el tráfico que pasa a través de ellos. Unencrypted traffic which contains personally identifiable information can deanonymize you to that exit node. Again, we recommend only using HTTPS over Tor.
- Powerful adversaries with the capability to passively watch *all* network traffic around the globe ("Global Passive Adversaries") are **not** something that Tor protects you against (and using Tor [with a VPN](#safely-connecting-to-tor) doesn't change this fact).
- Well-funded adversaries with the capability to passively watch *most* network traffic around the globe still have a *chance* of deanonymizing Tor users by means of advanced traffic analysis.

Si deseas utilizar Tor para navegar por la web, sólo recomendamos el navegador Tor Browser **oficial**-está diseñado para evitar las huellas digitales.

- [Tor Browser :material-arrow-right-drop-circle:](../tor.md#tor-browser)

### Protections provided by bridges

Tor bridges are commonly touted as an alternative method to hiding Tor usage from an ISP, instead of a VPN (as we suggest using if possible). Something to consider is that while bridges may provide adequate censorship circumvention, this is only a *transient* benefit. They do not adequately protect you from your ISP discovering you connected to Tor in the *past* with historical traffic log analysis.

To illustrate this point, consider the following scenario: You connect to Tor via a bridge, and your ISP doesn’t detect it because they are not doing sophisticated analysis of your traffic, so things are working as intended. Now, 4 months go by, and the IP of your bridge has been made public. This is a very common occurrence with bridges, they are discovered and blocked relatively frequently, just not immediately.

Your ISP wants to identify Tor users 4 months ago, and with their limited metadata logging they can see that you connected to an IP address which was later revealed to be a Tor bridge. You have virtually no other excuse to be making such a connection, so the ISP can say with very high confidence that you were a Tor user at that time.

Contrast this with our recommended scenario, where you connect to Tor via a VPN. Say that 4 months later your ISP again wants to identify anybody who used Tor 4 months ago. Their logs almost certainly can identify your traffic 4 months ago, but all they would likely be able to see is that you connected to a VPN’s IP address. This is because most ISPs only retain metadata over long periods of time, not the full contents of the traffic you request. Storing the entirety of your traffic data would require a massive quantity of storage which nearly all threat actors wouldn't possess.

Because your ISP almost certainly is not capturing all packet-level data and storing it forever, they have no way of determining what you connected to with that VPN *after* the fact with an advanced technique like deep packet inspection, and therefore you have plausible deniability.

Therefore, bridges provide the most benefit when circumventing internet censorship *in the moment*, but they are not an adequate substitute for **all** the benefits that using a VPN alongside Tor can provide. Again, this is not advice *against* using Tor bridges, you should just be aware of these limitations while making your decision. In some cases bridges may be the *only* option (if all VPN providers are blocked, for instance), so you can still use them in those circumstances with this limitation in mind.

If you think that a bridge can aid in defending against fingerprinting or other advanced network analysis more than a VPN's encrypted tunnel already can, you always have the option to use a bridge in conjunction with a VPN as well. That way you are still protected by the pluggable transport's obfuscation techniques even if an adversary gains some level of visibility into your VPN tunnel. If you decide to go this route, we recommend connecting to an obfs4 bridge behind your VPN for optimal fingerprinting protection, rather than meek or Snowflake.

It is [possible](https://discuss.privacyguides.net/t/clarify-tors-weaknesses-with-respect-to-observability/3676/16) that the [WebTunnel](https://forum.torproject.org/t/tor-relays-announcement-webtunnel-a-new-pluggable-transport-for-bridges-now-available-for-deployment/8180) pluggable transport currently being trialed may mitigate some of these concerns. We will continue to keep an eye on that technology as it develops.

## Recursos Adicionales

- [Manual del usuario del navegador Tor](https://tb-manual.torproject.org)
- [¿Cómo funciona Tor? - Computerphile](https://invidious.privacyguides.net/embed/QRYzre4bf7I?local=true) <small>(YouTube)</small>
- [Servicios Onion de Tor - Computerphile](https://invidious.privacyguides.net/embed/lVcbq_a5N9I?local=true) <small>(YouTube)</small>

[^1]: El primer repetidor en tu circuito se llama "guardia de entrada" o "guardia". Es un repetidor rápido y estable que se mantiene como el primero en tu circuito durante 2-3 meses para protegerse de un ataque conocido de ruptura del anonimato. El resto de tu circuito cambia con cada nuevo sitio web que visitas, y todos juntos estos repetidores proporcionan las protecciones de privacidad completas de Tor. Para obtener más información sobre el funcionamiento de los repetidores de protección, consulta esta [entrada del blog](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) y el [documento](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf) sobre los guardias de entrada. ([https://support.torproject.org/tbb/tbb-2/](https://support.torproject.org/tbb/tbb-2/))

[^2]: Bandera de repetidor: una (des)calificación de los repetidores para las posiciones de los circuitos (por ejemplo, "Guardia", "Salida", "MalaSalida"), las propiedades de los circuitos (por ejemplo, "Rápido", "Estable"), o los roles (por ejemplo, "Autoridad", "HSDir"), tal y como los asignan las autoridades de los directorios y se definen con más detalle en la especificación del protocolo del directorio. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html))
