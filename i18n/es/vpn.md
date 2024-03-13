---
meta_title: "Recomendaciones y Comparación de Servicios VPN Privados, Sin Patrocinadores Ni Anuncios - Privacy Guides"
title: "Servicios de VPN"
icon: material/vpn
description: Estos son los mejores servicios VPN para proteger tu privacidad y seguridad en línea. Encuentra un proveedor aquí que no esté para espiarte.
cover: vpn.webp
---

Si buscas **privacidad** adicional de tu proveedor de servicios de internet, en una red wifi pública o mientras descargando archivos Torrent, una VPN puede ser la solución para ti, siempre y cuando entiendas los riesgos que conlleva. Creemos que estos proveedores están por encima de los demás:

<div class="grid cards" markdown>

- ![Proton VPN logo](assets/img/vpn/protonvpn.svg){ .twemoji } [Proton VPN](#proton-vpn)
- ![IVPN logo](assets/img/vpn/mini/ivpn.svg){ .twemoji } [IVPN](#ivpn)
- ![Mullvad logo](assets/img/vpn/mullvad.svg){ .twemoji } [Mullvad](#mullvad)

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Las VPN no proporcionan anonimato</p>

El uso de una VPN **no** mantendrá sus hábitos de navegación en el anonimato, ni añadirá seguridad adicional al tráfico no seguro (HTTP).

Si buscas **anonimato**, deberías usar el navegador Tor.

Si busca mayor **seguridad**, debería asegurarse siempre de que se conecta a sitios web que utilicen HTTPS. Una VPN no sustituye las buenas prácticas de seguridad.

[Download Tor](https://torproject.org){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Resumen detallado de VPN :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Proveedores Recomendados

Nuestros proveedores recomendados usan encriptación, aceptan Monero, soportan WireGuard & OpenVPN, y tienen una política de no registro. Lee nuestra \[lista completa de criterios\](#criterios) para más información.

### Proton VPN

<div class="admonition recommendation" markdown>

![Logo de Proton VPN](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** es un fuerte contendiente en el espacio VPN, y han estado en funcionamiento desde 2016. Proton AG tiene su sede en Suiza y ofrece un nivel gratuito limitado, así como una opción premium con más funciones.

[:octicons-home-16: Homepage](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:simple-windows11: Windows](https://protonvpn.com/download-windows)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 71 Países

Proton VPN tiene [servidores en 71 países](https://protonvpn.com/vpn-servers) [o 3 si utilizas su plan gratuito](https://protonvpn.com/free-vpn).(1) Elegir un proveedor VPN con un servidor más cercano a ti reducirá la latencia del tráfico de red que envíes. Esto se debe a que es una ruta más corta (menos saltos) hasta el destino.
{ .annotate }

1. Última comprobación: 21-12-2023

También pensamos que es mejor para la seguridad de las claves privadas del proveedor de VPN si utilizan [servidores dedicados](https://en.wikipedia.org/wiki/Dedicated_hosting_service), en lugar de soluciones compartidas más baratas (con otros clientes) como los [[servidores privados virtuales](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Auditado independientemente

Los clientes VPN de Mullvad han sido auditados por Cure53 y Assured AB en un reporte de pentest \[publicado en cure53.de\](https://cure53.de/pentest-report_mullvad_v2.pdf). Los investigadores de seguridad concluyeron:

&gt; Cure53 y Assured AB están satisfechos con los resultados de la auditoría y el software deja una impresión positiva en general. Con la dedicación a la seguridad del equipo interno de Mullvad VPN, los testers no tienen dudas de que el proyecto va por buen camino desde el punto de vista de la seguridad. You can view individual reports for each platform at [protonvpn.com](https://protonvpn.com/blog/open-source). In April 2022 Proton VPN underwent [another audit](https://protonvpn.com/blog/no-logs-audit) and the report was [produced by Securitum](https://protonvpn.com/blog/wp-content/uploads/2022/04/securitum-protonvpn-nologs-20220330.pdf). El 9 de noviembre de 2021, [Securitum](https://research.securitum.com)proporcionó una carta de certificación [](https://proton.me/blog/security-audit-all-proton-apps) para las aplicaciones de Proton VPN.

#### :material-check:{ .pg-green } Clientes de código abierto

Proton VPN proporciona el código fuente para sus clientes de escritorio y móviles en su organización [GitHub](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Acepta efectivo

Proton VPN, además de aceptar tarjetas de crédito/débito, PayPal y [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), también acepta **efectivo/moneda local** como forma de pago anónima.

#### :material-check:{ .pg-green } Soporte de WireGuard

Mullvad soporta el protocolo WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Además, WireGuard aspira ser más simple y veloz.

Proton VPN [recommends](https://protonvpn.com/blog/wireguard) the use of WireGuard with their service. On Proton VPN's Windows, macOS, iOS, Android, ChromeOS, and Android TV apps, WireGuard is the default protocol; however, [support](https://protonvpn.com/support/how-to-change-vpn-protocols) for the protocol is not present in their Linux app.

#### :material-alert-outline:{ .pg-orange } Reenvío Remoto de Puertos

Proton VPN currently only supports ephemeral remote [port forwarding](https://protonvpn.com/support/port-forwarding) via NAT-PMP, with 60 second lease times. The Windows app provides an easy to access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup). Las aplicaciones de torrents suelen soportar NAT-PMP de forma nativa.

#### :material-information-outline:{ .pg-orange } Evasión de la Censura

Proton VPN has their [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) protocol which *may* help in situations where VPN protocols like OpenVPN or Wireguard are blocked with various rudimentary techniques. Stealth encapsula el túnel VPN en una sesión TLS para que parezca tráfico de Internet más genérico.

Por desgracia, no funciona muy bien en países donde se despliegan sofisticados filtros que analizan todo el tráfico saliente en un intento de descubrir túneles cifrados. Stealth tampoco está disponible aún en [Windows](https://github.com/ProtonVPN/win-app/issues/64) ni Linux.

#### :material-check:{ .pg-green } Clientes Móviles

In addition to providing standard OpenVPN configuration files, Proton VPN has mobile clients for [App Store](https://apps.apple.com/app/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android), and [GitHub](https://github.com/ProtonVPN/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } Funcionalidad Adicional

Mullvad ha publicado su cliente en la \[App Store\](https://apps.apple.com/app/mullvad-vpn/id1488466513) y en \[Google Play\](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn), ambos con una interfaz fácil de usar en lugar de requerir la configuración manual de la conexión de WireGuard. El cliente móvil en Android también está disponible en \[F-Droid\](https://f-droid.org/packages/net.mullvad.mullvadvpn), lo que garantiza que se compila con \[builds reproducibles\](https://www.f-droid.org/en/2019/05/05/trust-privacy-and-free-software.html). Ofrecen bloqueo de contenidos y bloqueo de malware conocido con su servicio DNS. Additionally, Proton VPN also offers "Tor" servers allowing you to easily connect to onion sites, but we still strongly recommend using [the official Tor Browser](https://torproject.org) for this purpose.

#### :material-alert-outline:{ .pg-orange } La función Killswitch no funciona en los Macs basados en Intel

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch) on Intel-based Macs when using the VPN killswitch. Utilizan \[ShadowSocks\](https://shadowsocks.org/en/index.html) en su configuración de ShadowSocks + OpenVPN, lo que les hace más resistentes contra los cortafuegos con \[Inspección profunda de paquete\](https://es.wikipedia.org/wiki/Deep_Packet_Inspection) que intentan bloquear las VPN.

### IVPN

<div class="admonition recommendation" markdown>

![IVPN logo](assets/img/vpn/protonvpn.svg){ align=right }

**IVPN** es un fuerte contendiente en el espacio de las VPNs, y ha estado en funcionamiento desde 2009. IVPN es basado en Gibraltar.

[:octicons-home-16: Homepage](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:simple-windows11: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 37 Países

IVPN has [servers in 37 countries](https://ivpn.net/status).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Esto se debe a que es una ruta más corta (menos saltos) hasta el destino.
{ .annotate }

1. Última comprobación: 21-12-2023

También pensamos que es mejor para la seguridad de las claves privadas del proveedor de VPN si utilizan [servidores dedicados](https://en.wikipedia.org/wiki/Dedicated_hosting_service), en lugar de soluciones compartidas más baratas (con otros clientes) como los [[servidores privados virtuales](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Auditado independientemente

IVPN se ha sometido a una auditoría de no-registrar en [por parte de Cure53](https://cure53.de/audit-report_ivpn.pdf) que concluyó de acuerdo con la afirmación de no-registrar de IVPN. IVPN también ha completado una [prueba de penetración exhaustiva Cure53](https://cure53.de/summary-report_ivpn_2019.pdf) en enero de 2020. IVPN has also said they plan to have [annual reports](https://ivpn.net/blog/independent-security-audit-concluded) in the future. A further review was conducted [in April 2022](https://ivpn.net/blog/ivpn-apps-security-audit-2022-concluded) and was produced by Cure53 [on their website](https://cure53.de/pentest-report_IVPN_2022.pdf).

#### :material-check:{ .pg-green } Clientes de Código Abierto

As of February 2020 [IVPN applications are now open source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). El código fuente puede ser obtenido en su [organización GitHub](https://github.com/ivpn).

#### :material-check:{ .pg-green } Acepta Efectivo y Monero

Además de aceptar tarjetas de crédito/débito y PayPal, IVPN acepta Bitcoin, **Monero** y **efectivo/moneda local** (en planes anuales) como formas anónimas de pago.

#### :material-check:{ .pg-green } Soporte de WireGuard

IVPN soporta el protocolo WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Además, WireGuard aspira ser más simple y veloz.

IVPN [recommends](https://ivpn.net/wireguard) the use of WireGuard with their service and, as such, the protocol is the default on all of IVPN's apps. IVPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-alert-outline:{ .pg-orange } Reenvío Remoto de Puertos

IVPN previously supported port forwarding, but removed the option in [June 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). La ausencia de esta característica podría afectar negativamente a ciertas aplicaciones, especialmente a las aplicaciones peer-to-peer como los clientes torrent.

#### :material-check:{ .pg-green } Evasión de la censura

IVPN has obfuscation modes using the [v2ray](https://v2ray.com/en/index.html) project which helps in situations where VPN protocols like OpenVPN or Wireguard are blocked. Currently this feature is only available on Desktop and [iOS](https://ivpn.net/knowledgebase/ios/v2ray). Este cuenta con dos modos donde puede usar [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) sobre QUIC o conexiones TCP. QUIC es un moderno protocolo con mejor control de la congestión y puede ser más rápido con menor latencia. El modo TCP ayuda para que tus datos aparezcan como tráfico HTTP regular.

#### :material-check:{ .pg-green } Clientes Móviles

In addition to providing standard OpenVPN configuration files, IVPN has mobile clients for [App Store](https://apps.apple.com/app/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), and [GitHub](https://github.com/ivpn/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } Funcionalidad Adicional

Proton VPN tiene sus propios servidores y centros de datos en Suiza, Islandia y Suecia. IVPN also provides "[AntiTracker](https://ivpn.net/antitracker)" functionality, which blocks advertising networks and trackers from the network level.

### Mullvad

<div class="admonition recommendation" markdown>

![Logo de Mullvad](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** es una VPN rápida y económica que se centra en la transparencia y la seguridad. Llevan en funcionamiento desde **2009**. Mullvad tiene su sede en Suecia y no tiene prueba gratuita.

[:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:simple-windows11: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 40 Países

Mullvad has [servers in 40 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Esto se debe a que es una ruta más corta (menos saltos) hasta el destino.
{ .annotate }

1. Última comprobación: 21-12-2023

También pensamos que es mejor para la seguridad de las claves privadas del proveedor de VPN si utilizan [servidores dedicados](https://en.wikipedia.org/wiki/Dedicated_hosting_service), en lugar de soluciones compartidas más baratas (con otros clientes) como los [[servidores privados virtuales](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Auditado Independientemente

Los clientes VPN de Mullvad han sido auditados por Cure53 y Assured AB en un reporte de prueba de penetración [publicado en cure53.de](https://cure53.de/pentest-report_mullvad_v2.pdf). Los investigadores de seguridad concluyeron:

> Cure53 y Assured AB están satisfechos con los resultados de la auditoría y el software deja una impresión general positiva. Con la dedicación a la seguridad del equipo interno de Mullvad VPN, los comprobadores no tienen dudas de que el proyecto va por buen camino desde el punto de vista de la seguridad.

In 2020 a second audit [was announced](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app) and the [final audit report](https://cure53.de/pentest-report_mullvad_2020_v2.pdf) was made available on Cure53's website:

> Los resultados del proyecto de mayo-junio de 2020 dirigido al complejo de Mullvad son bastante positivos. [...] El ecosistema general de aplicaciones utilizado por Mullvad deja una impresión sólida y estructurada. La estructura general de la aplicación facilita el despliegue de parches y correcciones de forma estructurada. Más que nada, los hallazgos detectados por Cure53 muestran la importancia de auditar y reevaluar constantemente los vectores de filtración actuales, para garantizar siempre la privacidad de los usuarios finales. Dicho esto, Mullvad hace un gran trabajo protegiendo al usuario final de las filtraciones comunes de Información personalmente identificable y de los riesgos relacionados con la privacidad.

In 2021 an infrastructure audit [was announced](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) and the [final audit report](https://cure53.de/pentest-report_mullvad_2021_v1.pdf) was made available on Cure53's website. Another report was commissioned [in June 2022](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data) and is available on [Assured's website](https://assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf).

#### :material-check:{ .pg-green } Clientes de Código Abierto

Mullvad proporciona el código fuente para sus clientes de escritorio y móviles en su [organización de GitHub](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Acepta Efectivo y Monero

Mullvad, además de aceptar tarjetas de crédito/débito y PayPal, acepta Bitcoin, Bitcoin Cash, **Monero** y **dinero en efectivo/moneda local** como formas de pago anónimas. \[WireGuard\](https://www.wireguard.com) es un protocolo más reciente que utiliza \[criptografía\](https://www.wireguard.com/protocol/) de última generación.

#### :material-check:{ .pg-green } Soporte de WireGuard

IVPN soporta el protocolo WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Además, WireGuard aspira ser más simple y veloz.

Mullvad [recommends](https://mullvad.net/en/help/why-wireguard) the use of WireGuard with their service. It is the default or only protocol on Mullvad's Android, iOS, macOS, and Linux apps, but on Windows you have to [manually enable](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-check:{ .pg-green } Soporte de IPv6

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support), as opposed to other providers which block IPv6 connections.

#### :material-alert-outline:{ .pg-orange } Reenvío Remoto de Puertos

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). La ausencia de esta característica podría afectar negativamente a ciertas aplicaciones, especialmente a las aplicaciones peer-to-peer como los clientes torrent.

#### :material-check:{ .pg-green } Evasión de la censura

Mullvad tiene un modo de ofuscación usando [Shadowsocks con v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) que puede ser útil en situaciones donde los protocolos VPN como OpenVPN o Wireguard están bloqueados.

#### :material-check:{ .pg-green } Clientes Móviles

Mullvad has published [App Store](https://apps.apple.com/app/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. El cliente de Android también está disponible en [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Funcionalidad Adicional

Mullvad is very transparent about which nodes they [own or rent](https://mullvad.net/en/servers). They use [ShadowSocks](https://shadowsocks.org) in their ShadowSocks + OpenVPN configuration, making them more resistant against firewalls with [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) trying to block VPNs. Supuestamente, [China tiene que utilizar un método diferente para bloquear los servidores de ShadowSocks](https://github.com/net4people/bbs/issues/22). El sitio web de Mullvad también es accesible a través de Tor en [o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion).

## Criterios

<div class="admonition danger" markdown>
<p class="admonition-title">Peligro</p>

Es importante tener en cuenta que el uso de un proveedor de VPN no le hará anónimo, pero le dará mayor privacidad en ciertas situaciones. Una VPN no es una herramienta para actividades ilegales. No confíes en una política de "sin registro".

</div>

**Por favor, tenga en cuenta que no estamos afiliados a ninguno de los proveedores que recomendamos. Esto nos permite ofrecer recomendaciones completamente objetivas.** Además de [nuestros cirterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos para cualquier proveedor de VPN que desee ser recomendado, incluyendo un cifrado fuerte, auditorías de seguridad independientes, tecnología moderna y más. Te sugerimos que te familiarices con esta lista antes de elegir un proveedor VPN, y lleves a cabo tu propia investigación para asegurar que el proveedor VPN que elijas sea lo más fiable posible.

### Tecnología

Requerimos que todos nuestros proveedores de VPN recomendados proporcionen archivos de configuración OpenVPN para ser usados en cualquier cliente. **Si** una VPN proporciona su propio cliente personalizado, requerimos un killswitch para bloquear las fugas de datos de la red cuando se desconecta.

**Mínimo para Calificar:**

- Soporte para protocolos fuertes como WireGuard & OpenVPN.
- Killswitch integrado en los clientes.
- Soporte de multisaltos. El multihopping es importante para mantener la privacidad de los datos en caso de que un solo nodo se vea comprometido.
- Si se proporcionan clientes VPN, deben ser de [código abierto](https://en.wikipedia.org/wiki/Open_source), como el software VPN que generalmente llevan incorporado. Creemos que la disponibilidad de [código fuente](https://en.wikipedia.org/wiki/Source_code) proporciona una mayor transparencia sobre lo que su dispositivo está haciendo realmente.

**Mejor Caso:**

- Soporte de WireGuard y OpenVPN.
- Killswitch con opciones altamente configurables (activar/desactivar en determinadas redes, en el arranque, etc.)
- Clientes VPN fáciles de usar
- Admite [IPv6](https://en.wikipedia.org/wiki/IPv6). Esperamos que los servidores permitan las conexiones entrantes a través de IPv6 y le permitan acceder a los servicios alojados en direcciones IPv6.
- La capacidad de [redirección de puertos](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) ayuda a crear conexiones cuando se utiliza software de intercambio de archivos P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)), Freenet, o se aloja un servidor (por ejemplo, Mumble).
- Tecnología de ofuscación que rellena los paquetes de datos con datos aleatorios para eludir la censura en Internet.

### Privacidad

Preferimos que nuestros proveedores recomendados recojan la menor cantidad de datos posible. Es necesario no recoger información personal en el momento de la inscripción y aceptar formas de pago anónimas.

**Mínimo para Calificar:**

- [Criptomoneda anónima](cryptocurrency.md) **o** opción de pago en efectivo.
- No se requiere información personal para registrarse: Sólo nombre de usuario, contraseña y correo electrónico como máximo.

**Mejor Caso:**

- Acepte múltiples [opciones de pago anónimo](advanced/payments.md).
- No se acepten datos personales (nombre de usuario autogenerado, no se requiere correo electrónico, etc.).

### Seguridad

Una VPN no tiene sentido si ni siquiera puede proporcionar una seguridad adecuada. Requerimos que todos nuestros proveedores recomendados que se atengan a las normas de seguridad vigentes para sus conexiones OpenVPN. Lo ideal sería que utilizaran por defecto esquemas de encriptación más resistentes al futuro. También requerimos que un tercero independiente audite la seguridad del proveedor, idealmente de una manera muy completa y sobre una base repetida (anual).

**Mínimo para Calificar:**

- Esquemas de cifrado fuertes: OpenVPN con autenticación SHA-256; RSA-2048 o mejor handshake; AES-256-CBC o cifrado de datos AES-256-GCM.
- Secreto Hacia Adelante.
- Auditorías de seguridad publicadas por una empresa externa de prestigio.

**Mejor Caso:**

- Cifrado más fuerte: RSA-4096.
- Secreto Hacia Adelante.
- Auditorías de seguridad exhaustivas publicadas por una empresa externa de prestigio.
- Programas de recompensa de errores y/o un proceso coordinado de divulgación de vulnerabilidades.

### Confianza

No confiarías tus finanzas a alguien con una identidad falsa, así que ¿por qué confiarle tus datos de Internet? Requerimos que nuestros proveedores recomendados sean públicos sobre su propiedad o liderazgo. También nos gustaría ver informes de transparencia frecuentes, especialmente en lo que se refiere a cómo se gestionan las solicitudes del gobierno.

**Mínimo para Calificar:**

- Liderazgo o titularidad de cara al público.

**Mejor Caso:**

- Liderazgo de cara al público.
- Informes de transparencia frecuentes.

### Marketing

Con los proveedores de VPN que recomendamos nos gusta ver un marketing responsable.

**Mínimo para Calificar:**

- Debe tener análisis propios (no Google Analytics, etc.). El sitio del proveedor también debe cumplir con [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) para las personas que quieran excluirse.

No debe tener ningún mercadeo que sea irresponsable:

- Haciendo garantías de proteger el anonimato al 100%. Cuando alguien afirma que algo es 100% significa que no hay certeza de fracaso. Sabemos que la gente puede desanonimizarse fácilmente de varias maneras, por ejemplo:
    - Reutilizando información personal (por ejemplo, cuentas de correo electrónico, seudónimos únicos, etc) a los que accedieron sin software de anonimato (Tor, VPN, etc.)
    - [Browser fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Afirmar que una VPN de un solo circuito es "más anónima" que Tor, el cual es un circuito de 3 o más saltos que cambia regularmente.
- Utilice un lenguaje responsable, por ejemplo, está bien decir que una VPN está "desconectada" o "no conectada", pero afirmar que alguien está "expuesto", "vulnerable" o "comprometido" es un uso innecesario de un lenguaje alarmante que puede ser incorrecto. Por ejemplo, esa persona podría simplemente estar en el servicio de otro proveedor de VPN o usar Tor.

**Mejor Caso:**

El marketing responsable que es a la vez educativo y útil para el consumidor podría incluir:

- Una comparación precisa para cuando [Tor](tor.md) se debe utilizar en su lugar.
- Disponibilidad del sitio web del proveedor de VPN a través de un .onion [Hidden Service](https://es.wikipedia.org/wiki/.onion)

### Funcionalidad Adicional

Aunque no son estrictamente requisitos, hay algunos factores en los que nos fijamos a la hora de determinar qué proveedores recomendar. Entre ellas se incluyen la funcionalidad de bloqueo de contenidos, los canarios de garantía, las conexiones multisalto, la excelente atención al cliente, el número de conexiones simultáneas permitidas, etc.
