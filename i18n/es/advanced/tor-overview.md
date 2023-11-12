---
title: "Resumen de Tor"
icon: 'simple/torproject'
description: Tor es una red descentralizada y gratuita diseñada para utilizar Internet con la mayor privacidad posible.
---

Tor es una red descentralizada y gratuita diseñada para utilizar Internet con la mayor privacidad posible. Si se utiliza correctamente, la red permite la navegación y las comunicaciones privadas y anónimas.

## Safely Connecting to Tor

Before connecting to [Tor](../tor.md), you should carefully consider what you're looking to accomplish by using Tor in the first place, and who you're trying to hide your network activity from.

If you live in a free country, are accessing mundane content via Tor, aren't worried about your ISP or local network administrators having the knowledge that you're using Tor, and want to help [de-stigmatize](https://2019.www.torproject.org/about/torusers.html.en) Tor usage, you can likely connect to Tor directly via standard means like [Tor Browser](../tor.md) without worry.

If you have the ability to access a trusted VPN provider and **any** of the following are true, you almost certainly should connect to Tor through a VPN:

- You already use a [trusted VPN provider](../vpn.md)
- Your threat model includes an adversary which is capable of extracting information from your ISP
- Your threat model includes your ISP itself as an adversary
- Your threat model includes local network administrators before your ISP as an adversary

Because we already [generally recommend](../basics/vpn-overview.md) that the vast majority of people use a trusted VPN provider for a variety of reasons, the following recommendation about connecting to Tor via a VPN likely applies to you. <mark>There is no need to disable your VPN before connecting to Tor</mark>, as some online resources would lead you to believe.

Connecting directly to Tor will make your connection stand out to any local network administrators or your ISP. Detecting and correlating this traffic [has been done](https://edition.cnn.com/2013/12/17/justice/massachusetts-harvard-hoax/) in the past by network administrators to identify and deanonymize specific Tor users on their network. On the other hand, connecting to a VPN is almost always less suspicious, because commercial VPN providers are used by everyday consumers for a variety of mundane tasks like bypassing geo-restrictions, even in countries with heavy internet restrictions.

Therefore, you should make an effort to hide your IP address **before** connecting to the Tor network. You can do this by simply connecting to a VPN (through a client installed on your computer) and then accessing [Tor](../tor.md) as normal, through Tor Browser for example. This creates a connection chain like:

- [x] You → VPN → Tor → Internet

From your ISP's perspective, it looks like you're accessing a VPN normally (with the associated cover that provides you). From your VPN's perspective, they can see that you are connecting to the Tor network, but nothing about what websites you're accessing. From Tor's perspective, you're connecting normally, but in the unlikely event of some sort of Tor network compromise, only your VPN's IP would be exposed, and your VPN would *additionally* have to be compromised to deanonymize you.

This is **not** censorship circumvention advice, because if Tor is blocked entirely by your ISP, your VPN likely is as well. Rather, this recommendation aims to make your traffic blend in better with commonplace VPN user traffic, and provide you with some level of plausible deniability by obscuring the fact that you're connecting to Tor from your ISP.

---

We **very strongly discourage** combining Tor with a VPN in any other manner. Do not configure your connection in a way which resembles any of the following:

- You → Tor → VPN → Internet
- You → VPN → Tor → VPN → Internet
- Any other configuration

Some VPN providers and other publications will occasionally recommend these **bad** configurations to evade Tor bans (exit nodes being blocked by websites) in some places. [Normally](https://support.torproject.org/#about_change-paths), Tor frequently changes your circuit path through the network. When you choose a permanent *destination* VPN (connecting to a VPN server *after* Tor), you're eliminating this advantage and drastically harming your anonymity.

Setting up bad configurations like these is difficult to do accidentally, because it usually involves either setting up custom proxy settings inside Tor Browser, or setting up custom proxy settings inside your VPN client which routes your VPN traffic through the Tor Browser. As long as you avoid these non-default configurations, you're probably fine.

---

!!! info "VPN/SSH Fingerprinting"

    The Tor Project [notes](https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN#vpnssh-fingerprinting) that *theoretically* using a VPN to hide Tor activities from your ISP may not be foolproof. VPNs have been found to be vulnerable to website traffic fingerprinting, where an adversary can still guess what website is being visited, because all websites have specific traffic patterns.
    
    Therefore, it's not unreasonable to believe that encrypted Tor traffic hidden by a VPN could also be detected via similar methods. There are no research papers on this subject, and we still consider the benefits of using a VPN to far outweigh these risks, but it is something to keep in mind.
    
    If you still believe that pluggable transports (bridges) provide additional protection against website traffic fingerprinting that a VPN does not, you always have the option to use a bridge **and** a VPN in conjunction.

Determining whether you should first use a VPN to connect to the Tor network will require some common sense and knowledge of your own government's and ISP's policies relating to what you're connecting to. However, again in most cases you will be better off being seen as connecting to a commercial VPN network than directly to the Tor network. If VPN providers are censored in your area, then you can also consider using Tor pluggable transports (e.g. Snowflake or meek bridges) as an alternative, but using these bridges may arouse more suspicion than standard WireGuard/OpenVPN tunnels.

## What Tor is Not

The Tor network is not the perfect privacy protection tool in all cases, and has a number of drawbacks which should be carefully considered. These things should not discourage you from using Tor if it is appropriate for your needs, but they are still things to think about when deciding which solution is most appropriate for you.

### Tor is not a free VPN

The release of the *Orbot* mobile app has lead many people to describe Tor as a "free VPN" for all of your device traffic. However, treating Tor like this poses some dangers compared to a typical VPN.

Unlike Tor exit nodes, VPN providers are usually not *actively* [malicious](#caveats). Because Tor exit nodes can be created by anybody, they are hotspots for network logging and modification. In 2020, many Tor exit nodes were documented to be downgrading HTTPS traffic to HTTP in order to [hijack cryptocurrency transactions](https://therecord.media/thousands-of-tor-exit-nodes-attacked-cryptocurrency-users-over-the-past-year). Other exit node attacks such as replacing downloads via unencrypted channels with malware have also been observed. HTTPS does mitigate these threats to an extent.

As we've alluded to already, Tor is also easily identifiable on the network. Unlike an actual VPN provider, using Tor will make you stick out as a person likely attempting to evade authorities. In a perfect world, Tor would be seen by network administrators and authorities as a tool with many uses (like how VPNs are viewed), but in reality the perception of Tor is still far less legitimate than the perception of commercial VPNs, so using a real VPN provides you with plausible deniability, e.g. "I was just using it to watch Netflix," etc.

### Tor usage is not undetectable

**Even if you use bridges and pluggable transports,** the Tor Project provides no tools to hide the fact that you are using Tor from your ISP. Even using obfuscated "pluggable transports" or non-public bridges do not hide the fact that you are using a private communications channel. The most popular pluggable transports like obfs4 (which obfuscates your traffic to "look like nothing") and meek (which uses domain fronting to camouflage your traffic) can be [detected](https://www.hackerfactor.com/blog/index.php?/archives/889-Tor-0day-Burning-Bridges.html) with fairly standard traffic analysis techniques. Snowflake has similar issues, and can be [easily detected](https://www.hackerfactor.com/blog/index.php?/archives/944-Tor-0day-Snowflake.html) *before* a Tor connection is even established.

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
