---
meta_title: "How Do VPNs Protect Your Privacy? Our VPN Overview - Privacy Guides"
title: VPN Overview
icon: material/vpn
description: Virtual Private Networks shift risk away from your ISP to a third-party you trust. You should keep these things in mind.
---

Las Redes Privadas Virtuales son una forma de ampliar el extremo de tu red para que salga por otro lugar en el mundo.

Normalmente, un ISP puede ver el flujo de tráfico de Internet que entra y sale de Tu dispositivo de terminación de red (es decir, el módem). Los protocolos de cifrado como HTTPS se utilizan habitualmente en Internet, por lo que es posible que no puedan ver exactamente lo que publicas o lees, pero pueden hacerse una idea de los [dominios que solicitas](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns).

El uso de una VPN oculta incluso esta información a tu ISP, al trasladar la confianza que depositas en tu red a un servidor situado en otro lugar del mundo. Como resultado, el ISP solo ve que estás conectado a una VPN y nada sobre la actividad que estás pasando a través de ella.

<div class="admonition note" markdown>
<p class="admonition-title">Nota</p>

Cuando hablamos de "Redes Privadas Virtuales" en este sitio web, normalmente nos referimos a [proveedores de VPN](../vpn.md) **comerciales**, a los que usted paga una cuota mensual a cambio de enrutar tu tráfico de Internet de forma segura a través de sus servidores públicos. Existen muchas otras formas de VPN, como las que alojas tú mismo o las que gestionan los centros de trabajo, que te permiten conectarte de forma segura a los recursos de red internos o de los empleados; sin embargo, estas VPN suelen estar diseñadas para acceder de forma segura a redes remotas, en lugar de para proteger la privacidad de tu conexión a Internet.

</div>

## ¿Cómo funciona una VPN?

Las VPN cifran el tráfico entre tu dispositivo y un servidor propiedad de tu proveedor de VPN. Desde la perspectiva de cualquiera que se encuentre entre ti y el servidor VPN, parece que te estás conectando al servidor VPN. Desde la perspectiva de cualquier persona que se encuentre entre el servidor VPN y tu sitio de destino, todo lo que pueden ver es el servidor VPN conectándose al sitio web.

``` mermaid
diagrama de flujo LR
 763931["Tu Dispositivo<div>(con Cliente VPN)</div>"] ===|"Cifrado VPN"| 404512{"Servidor VPN"}
 404512 -.-|"Sin Cifrado VPN "| 593753((("Internet\n(Tu Destino)")))
 subgraph 763931["Tu Dispositivo<div>(con Cliente VPN)</div>"]
 end
```

Ten en cuenta que una VPN no añade ningún tipo de seguridad o cifrado a tu tráfico entre el servidor VPN y tu destino en Internet. Para acceder a un sitio web de forma segura **debes** asegurarte de que HTTPS está en uso, independientemente de si utilizas una VPN.

## ¿Yo debería usar una VPN?

**Sí**, casi seguro. Una VPN tiene muchas ventajas, entre ellas:

1. Oculta tu tráfico **solo** de tu proveedor de servicios de Internet.
1. Oculta tus descargas (como los torrents) de tu ISP y las organizaciones antipiratería.
1. Oculta tu IP de sitios web y servicios de terceros, ayudándote a pasar desapercibido y evitando el rastreo basado en la IP.
1. Te permite saltarte las restricciones geográficas de determinados contenidos.

Las VPN pueden proporcionar a *algunos* de los mismos beneficios que proporciona Tor, como ocultar tu IP de los sitios web que visitas y desplazar geográficamente tu tráfico de red, y los buenos proveedores de VPN no cooperarán con, por ejemplo, las autoridades legales de regímenes opresivos, especialmente si eliges un proveedor de VPN fuera de tu propia jurisdicción.

Las VPN no pueden cifrar datos fuera de la conexión entre tu dispositivo y el servidor VPN. Los proveedores de VPN también pueden ver y modificar tu tráfico del mismo modo que tu ISP, por lo que sigue habiendo un nivel de confianza que depositas en ellos. Y no hay forma en absoluto de verificar las políticas de "no registro" de un proveedor de VPN.

## ¿Cuándo no es adecuada una VPN?

El uso de una VPN en los casos en los que estés utilizando tu [identidad real o conocida](common-misconceptions.md#complicated-is-better) en línea es poco probable que sea útil. Si lo haces, puedes activar sistemas de detección de spam y fraude, por ejemplo si te conectas al sitio web de tu banco.

Es importante recordar que una VPN no te proporcionará un anonimato absoluto, ya que el propio proveedor de VPN seguirá viendo tu dirección IP real, la información del sitio web de destino y, a menudo, tiene un rastro de dinero que puede vincularse directamente contigo. No puedes confiar en las políticas de "no registro" para proteger tus datos de cualquiera que sea capaz de proteger. Si necesitas seguridad total de la propia red, considera usar [Tor](../advanced/tor-overview.md) además o en lugar de una VPN.

Tampoco deberías confiar en una VPN para asegurar tu conexión a un destino HTTP sin cifrar. Para mantener la privacidad y seguridad de lo que haces en los sitios web que visitas, debes utilizar HTTPS. Esto mantendrá tus contraseñas, tokens de sesión y consultas a salvo del proveedor de VPN y otros posibles adversarios entre el servidor VPN y tu destino. Deberías activar el modo sólo HTTPS en tu navegador (si es compatible) para mitigar los ataques que intentan degradar tu conexión de HTTPS a HTTP.

## ¿Debo utilizar DNS cifrado con una VPN?

A menos que tu proveedor de VPN aloje los propios servidores DNS cifrados, **probablemente no**. Utilizar DOH/DOT (o cualquier otra forma de DNS cifrado) con servidores de terceros simplemente añadirá más entidades en las que confiar. Tu proveedor de VPN aún puede ver qué sitios web visitas basándose en las direcciones IP y otros métodos. Dicho esto, puede tener algunas ventajas activar el DNS cifrado para activar otras funciones de seguridad en tu navegador, como ECH. Las tecnologías de navegación que dependen del DNS cifrado en el navegador son relativamente nuevas y aún no están muy extendidas, por lo que si son relevantes para ti en particular es un ejercicio que te dejamos para que lo investigues por tu cuenta.

Otra razón común por la que se recomienda el DNS cifrado es que evita la suplantación de DNS (DNS spoofing). Sin embargo, tu navegador ya debería estar buscando [certificados TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) con **HTTPS** y advertirte al respecto. Si no estás utilizando **HTTPS**, entonces un adversario todavía puede simplemente modificar cualquier cosa que no sean tus consultas DNS y el resultado final será similar.

## ¿Debería usar Tor *y* una VPN?

Tal vez, Tor no sea necesariamente adecuado para todo el mundo en primer lugar. Considera tu [modelo de amenaza](threat-modeling.md), porque si tu adversario no es capaz de extraer información de tu proveedor de VPN, el uso de una VPN por sí sola puede proporcionar suficiente protección.

Si utilizas Tor, entonces *probablemente* es mejor conectarse a la red Tor a través de un proveedor comercial de VPN. Sin embargo, este es un tema complejo sobre el que hemos escrito más en nuestra página [Resumen de Tor](../advanced/tor-overview.md).

## ¿Debería acceder a Tor a través de proveedores de VPN que proporcionen "nodos Tor"?

No deberías usar esa función: La principal ventaja de usar Tor es que no confías en tu proveedor VPN, lo que se anula cuando usas nodos Tor alojados por tu VPN en lugar de conectarte directamente a Tor desde tu ordenador.

Actualmente, Tor solo soporta el protocolo TCP. UDP (utilizado por [WebRTC](https://es.wikipedia.org/wiki/WebRTC), [HTTP3/QUIC](https://es.wikipedia.org/wiki/HTTP/3), y otros protocolos), [ICMP](https://es.wikipedia.org/wiki/Protocolo_de_control_de_mensajes_de_Internet), y otros paquetes serán descartados. Para compensar por esto, los proveedores de VPN suelen enrutar todos los paquetes no TCP a través de su servidor VPN (tu primer salto). Este es el caso con [ProtonVPN](https://protonvpn.com/support/tor-vpn/). Adicionalmente, al usar esta configuración de Tor sobre VPN, no tienes control sobre otras funciones importantes de Tor como [Dirección de Destino Aislada](https://www.whonix.org/wiki/Stream_Isolation) (usando un circuito Tor diferente para cada dominio que visitas).

La función debe verse como una *conveniente* forma de acceder a servicios ocultos en Tor, no para permanecer en el anonimato. Para un anonimato adecuado, utilice el navegador real [Tor Browser](../tor.md).

## Propiedad Comercial de VPN

La mayoría de los servicios VPN pertenecen a las mismas [pocas empresas](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies/). Estas empresas sospechosas gestionan multitud de servicios VPN más pequeños para crear la ilusión de que tienes más opciones de las que realmente tienes y para maximizar sus beneficios. Normalmente, estos proveedores que alimentan a su empresa fantasma tienen políticas de privacidad terribles y no se les debería confiar tu tráfico de Internet. Debes ser muy estricto con el proveedor que decides utilizar.

También debes tener cuidado con el hecho de que muchos sitios de reseñas de VPN no son más que vehículos publicitarios abiertos al mejor postor. ==Privacy Guides no gana dinero recomendando productos externos y nunca utiliza programas de afiliación.==

[Nuestras Recomendaciones de VPN](../vpn.md ""){.md-button}

## Alternativas VPN Modernas

Recientemente, varias organizaciones han intentado resolver algunos de los problemas que presentan las VPN centralizadas. Estas tecnologías son relativamente nuevas, pero merece la pena seguirlas de cerca.

### Repetidores Multiparte

Los repetidores multiparte (MPR) utilizan varios nodos propiedad de distintas partes, de modo que ninguna sabe quién eres y a qué te conectas. Esta es la idea básica detrás de Tor, pero ahora hay algunos servicios de pago que intentan emular este modelo.

Los MPR tratan de resolver un problema inherente a las VPN: el hecho de que hay que confiar plenamente en ellas. Logran este objetivo segmentando las responsabilidades entre dos o más empresas diferentes. Por ejemplo, Relay Privado de iCloud+ de Apple dirige tu tráfico a través de dos servidores:

1. En primer lugar, un servidor operado por Apple.

    Este servidor es capaz de ver la IP de tu dispositivo cuando te conectas a él, y tiene conocimiento de tu información de pago y de tu ID de Apple vinculada a tu suscripción a iCloud. Sin embargo, no es capaz de ver a qué sitio web te estás conectando.

2. En segundo lugar, un servidor operado por una CDN asociada, como Cloudflare o Fastly.

    Este servidor realiza la conexión con el sitio web de destino, pero no tiene conocimiento de tu dispositivo. La única dirección IP que conoce es la del servidor de Apple.

Otros MPR gestionados por empresas diferentes, como Google o INVISV, funcionan de manera muy similar. Esta protección por segmentación solo existe si confías en que las dos empresas no confabularán entre sí para desanonimizarte.

### VPN Descentralizadas

Otro intento de resolver los problemas de los servicios VPN centralizados son las dVPN. Se basan en la tecnología blockchain y pretenden eliminar la confianza en una sola parte distribuyendo los nodos entre muchas personas diferentes. Sin embargo, en muchas ocasiones una dVPN utilizará por defecto un único nodo, lo que significa que tendrás que confiar plenamente en ese nodo, al igual que en una VPN tradicional. A diferencia de una VPN tradicional, este único nodo que puede ver todo tu tráfico es una persona cualquiera en lugar de tu proveedor de VPN, que puede ser auditado y tiene responsabilidades legales para mantener su política de privacidad. Para solucionarlo se necesitan multisaltos, pero eso conlleva un coste de estabilidad y rendimiento.

Otra consideración es la responsabilidad legal. El nodo de salida tendrá que lidiar con problemas legales derivados del mal uso de la red, un problema con el que la red Tor ha lidiado durante toda su existencia. Esto disuade a la gente normal de ejecutar nodos y hace que sea más atractivo para un actor malicioso con muchos recursos alojar uno. Esto es un gran problema si el servicio es de un solo nodo, ya que el nodo de salida potencialmente malicioso puede ver quién eres y a qué te estás conectando.

Muchas dVPN se utilizan para impulsar una criptomoneda en lugar de hacer el mejor servicio. También suelen ser redes más pequeñas con menos nodos, lo que las hace más vulnerables a los [ataques de Sybil](https://en.wikipedia.org/wiki/Sybil_attack).

## Información Relacionada con las VPNs

- [El Problema con los Sitios de Revisión de VPNs y de Privacidad](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites/)
- [Investigación de Aplicaciones de VPN Gratuita](https://www.top10vpn.com/free-vpn-app-investigation/)
- [Propietarios ocultos de VPN revelados: 101 productos VPN administrados por solo 23 empresas](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies/)
- [Esta empresa china está secretamente detrás de 24 aplicaciones populares que buscan permisos peligrosos](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions/)
- [VPN - una narrativa muy precaria](https://schub.io/blog/2019/04/08/very-precarious-narrative.html) por Dennis Schubert
