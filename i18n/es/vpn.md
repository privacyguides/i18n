---
meta_title: "Recomendaciones y Comparación de Servicios VPN Privados, Sin Patrocinadores Ni Anuncios - Privacy Guides"
title: Servicios de VPN
icon: material/vpn
description: Los mejores servicios VPN para proteger tu privacidad y seguridad en Internet. Encuentra aquí un proveedor que no te espíe.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Si buscas *privacidad* adicional frente a tu ISP, en una red Wi-Fi pública o mientras haces torrenting de archivos, una **VPN** puede ser la solución para ti.

<div class="admonition danger" markdown>
<p class="admonition-title">Las VPN no proporcionan anonimato</p>

Usar una VPN **no** mantendrá tus hábitos de navegación anónimos, ni proporcionará seguridad adicional al tráfico poco seguro (HTTP).

Si buscas **anonimato**, deberías usar el Navegador Tor. Si buscas **seguridad** adicional, siempre debes asegurarte de que te conectas a sitios web usando HTTPS. Una VPN no sustituye las buenas prácticas de seguridad.

[Introduction to the Tor Browser](tor.md#tor-browser){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Resumen detallado de VPN :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Proveedores Recomendados

Nuestros proveedores recomendados usan cifrado, soportan Wireguard & OpenVPN, además de que tienen una política de cero registros. Lee nuestra \[lista completa de criterios\](#criterios) para más información.

| Proveedor             | Países | WireGuard                     | Redireccionamiento de puertos                          | IPv6                                                             | Pagos anónimos               |
| --------------------- | ------ | ----------------------------- | ------------------------------------------------------ | ---------------------------------------------------------------- | ---------------------------- |
| [Proton](#proton-vpn) | 127+   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Soporte Parcial | :material-information-outline:{ .pg-blue } Soporte Limitado      | Cash  Monero via third party |
| [IVPN](#ivpn)         | 41+    | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                 | :material-information-outline:{ .pg-blue } Sólo tráfico saliente | Monero  Cash                 |
| [Mullvad](#mullvad)   | 49+    | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                 | :material-check:{ .pg-green }                                    | Monero  Cash                 |

### Proton VPN

<div class="admonition recommendation" markdown>

![Logo de Proton VPN](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** es un fuerte contendiente en el espacio VPN, y han estado en funcionamiento desde 2016. Proton AG tiene su sede en Suiza y ofrece un nivel gratuito limitado, así como una opción premium con más funciones.

[:octicons-home-16: Homepage](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://protonvpn.com/download-windows)
- [:simple-apple: macOS](https://protonvpn.com/download-macos)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 127 Countries

Proton VPN has [servers in 127 countries](https://protonvpn.com/vpn-servers)(1) or [10](https://protonvpn.com/support/how-to-create-free-vpn-account) if you use their [free plan](https://protonvpn.com/blog/product-roadmap-winter-2025-2026).(2) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Esto se debe a que es una ruta más corta (menos saltos) hasta el destino.
{ .annotate }

1. Of which at least 71 are virtual servers, meaning your IP will appear from the country but the server is in another. 12 more locations have both hardware and virtual servers. [Source](https://protonvpn.com/support/how-smart-routing-works)
2. Last checked: 2025-10-28

También pensamos que es mejor para la seguridad de las claves privadas del proveedor de VPN si utilizan [servidores dedicados](https://en.wikipedia.org/wiki/Dedicated_hosting_service), en lugar de soluciones compartidas más baratas (con otros clientes) como los [[servidores privados virtuales](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Auditado independientemente

Independent security researcher Ruben Santamarta conducted audits for Proton VPN's [browser extensions](https://drive.proton.me/urls/RWDD2SHT98#v7ZrwNcafkG8) and [apps](https://drive.proton.me/urls/RVW8TXG484#uTXX5Fc9GADo) in September 2024 and January 2025, respectively. Proton VPN's infrastrcture has undergone [annual audits](https://protonvpn.com/blog/no-logs-audit) by Securitum since 2022.

Previously, Proton VPN underwent an independent audit by SEC Consult in January 2020. Los investigadores de seguridad concluyeron:

&gt; Cure53 y Assured AB están satisfechos con los resultados de la auditoría y el software deja una impresión positiva en general. Con la dedicación a la seguridad del equipo interno de Mullvad VPN, los testers no tienen dudas de que el proyecto va por buen camino desde el punto de vista de la seguridad. You can view individual reports for each platform in their dedicated [blog post](https://web.archive.org/web/20250307041036/https://protonvpn.com/blog/open-source) on the audit.

#### :material-check:{ .pg-green } Clientes de código abierto

Proton VPN provides the source code for their desktop and mobile clients in their [GitHub organization](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Acepta efectivo

Proton VPN, in addition to accepting credit/debit cards, PayPal, and [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), also accepts **cash/local currency** as an anonymous form of payment. You can also use [**Monero**](cryptocurrency.md#monero) to purchase vouchers for Proton VPN Plus and Proton Unlimited via their [official](https://discuss.privacyguides.net/t/add-monero-as-an-anonymous-payment-method-for-proton-services/31058/15) reseller [ProxyStore](https://dys2p.com/en/2025-09-09-proton.html).

#### :material-check:{ .pg-green } Soporte de WireGuard

Proton VPN soporta el protocolo WireGuard®. [WireGuard](https://wireguard.com) es un protocolo más reciente que utiliza [criptografía](https://wireguard.com/protocol) de última generación. Además, WireGuard aspira ser más simple y veloz.

Proton VPN [recomienda](https://protonvpn.com/blog/wireguard) el uso de WireGuard con su servicio. Proton VPN también ofrece un generador de configuración de WireGuard para su uso con las [aplicaciones](https://wireguard.com/install) oficiales de WireGuard.

#### :material-alert-outline:{ .pg-orange } Soporte IPv6 Limitado

Proton [ya admite IPv6](https://protonvpn.com/support/prevent-ipv6-vpn-leaks) en su extensión de navegador y en su cliente Linux, pero solo el 80% de sus servidores son compatibles con IPv6. En otras plataformas, el cliente Proton VPN bloqueará todo el tráfico IPv6 saliente, por lo que no tendrá que preocuparse de que se filtre su dirección IPv6, pero no podrá conectarse a ningún sitio solo IPv6, ni podrá conectarse a Proton VPN desde una red solo IPv6.

#### :material-information-outline:{ .pg-info } Reenvío remoto de puertos

Actualmente, Proton VPN solo admite el [ reenvío del puerto](https://protonvpn.com/support/port-forwarding) remoto y efímero a través de NAT-PMP, con tiempos de arrendamiento de 60 segundos. Las aplicaciones oficiales para Windows y Linux ofrecen una opción de fácil acceso, mientras que en otros sistemas operativos tendrás que ejecutar tu propio [cliente NAT-PMP](https://protonvpn.com/support/port-forwarding-manual-setup). Las aplicaciones de torrents suelen soportar NAT-PMP de forma nativa.

#### :material-information-outline:{ .pg-blue } Anti censura

Proton VPN tiene su protocolo [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) que *puede* ayudar en situaciones donde los protocolos VPN como OpenVPN o WireGuard están bloqueados con varias técnicas rudimentarias. Stealth encapsula el túnel VPN en una sesión TLS para que parezca tráfico de Internet más genérico.

Desafortunadamente, no funciona muy bien en países donde se despliegan sofisticados filtros que analizan todo el tráfico saliente en un intento de descubrir túneles cifrados. Stealth está disponible en Android, iOS, Windows y macOS, pero aún no en Linux.

#### :material-check:{ .pg-green } Clientes Móviles

Proton VPN ha publicado clientes en [App Store](https://apps.apple.com/app/id1437005085) y [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android), ambos con una interfaz fácil de usar que no requiere que configures manualmente tu conexión WireGuard. El cliente para Android también está disponible en [GitHub](https://github.com/ProtonVPN/android-app/releases).

<div class="admonition warning" markdown>
<p class="admonition-title">Cómo optar por no compartir telemetría</p>

En Android, Proton oculta los ajustes de telemetría bajo el engañosamente etiquetado menú "**Ayúdanos a luchar contra la censura**" del panel de ajustes. En otras plataformas, estos ajustes se encuentran en el menú "**Estadísticas de uso**".

Hacemos notar esto porque, aunque no recomendamos necesariamente que no se compartan estadísticas de uso anónimas con los desarrolladores, es importante que estos ajustes sean fáciles de encontrar y estén claramente etiquetados.

</div>

#### :material-information-outline:{ .pg-blue } Notas adicionales

Los clientes de Proton VPN soportan autenticación de doble factor en todas las plataformas. El cliente móvil en Android también está disponible en \[F-Droid\](https://f-droid.org/packages/net.mullvad.mullvadvpn), lo que garantiza que se compila con \[builds reproducibles\](https://www.f-droid.org/en/2019/05/05/trust-privacy-and-free-software.html). Ofrecen bloqueo de contenidos y bloqueo de malware conocido con su servicio DNS. Además, Proton VPN también ofrece servidores de "Tor" que te permiten conectarte con facilidad a los sitios onion, pero recomendamos encarecidamente usar [el navegador oficial de Tor](tor.md#tor-browser) para este propósito.

##### :material-alert-outline:{ .pg-orange } La función Kill Switch no funciona en los Macs basados en Intel

Los fallos del sistema [pueden ocurrir](https://protonvpn.com/support/macos-t2-chip-kill-switch) en Macs basados en Intel cuando se utiliza el kill switch del VPN. Utilizan \[ShadowSocks\](https://shadowsocks.org/en/index.html) en su configuración de ShadowSocks + OpenVPN, lo que les hace más resistentes contra los cortafuegos con \[Inspección profunda de paquete\](https://es.wikipedia.org/wiki/Deep_Packet_Inspection) que intentan bloquear las VPN.

### IVPN

<div class="admonition recommendation" markdown>

![IVPN logo](assets/img/vpn/protonvpn.svg){ align=right }

**IVPN** es un fuerte contendiente en el espacio de las VPNs, y ha estado en funcionamiento desde 2009. IVPN tiene su sede en Gibraltar y no ofrece una prueba gratuita.

[:octicons-home-16: Homepage](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-github: GitHub](https://github.com/ivpn/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 41 Countries

IVPN has [servers in 41 countries](https://ivpn.net/status).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Esto se debe a que es una ruta más corta (menos saltos) hasta el destino.
{ .annotate }

1. Last checked: 2025-10-28

También pensamos que es mejor para la seguridad de las claves privadas del proveedor de VPN si utilizan [servidores dedicados](https://en.wikipedia.org/wiki/Dedicated_hosting_service), en lugar de soluciones compartidas más baratas (con otros clientes) como los [[servidores privados virtuales](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Auditado independientemente

IVPN ha tenido múltiples [auditorías independientes](https://ivpn.net/en/blog/tags/audit) desde 2019 y ha anunciado públicamente su compromiso con [auditorías de seguridad anuales](https://ivpn.net/blog/ivpn-apps-security-audit-concluded).

#### :material-check:{ .pg-green } Clientes de Código Abierto

Desde febrero de 2020, [las aplicaciones IVPN son de código abierto](https://ivpn.net/blog/ivpn-applications-are-now-open-source). El código fuente puede ser obtenido en su [organización GitHub](https://github.com/ivpn).

#### :material-check:{ .pg-green } Acepta Efectivo y Monero

Además de tarjetas de crédito/débido y PayPal, IVPN acepta Bitcoin, **Monero** y **efectivo/moneda local** (en los planes anuales) como métodos anónimos de pago. You can also purchase [prepaid cards](https://ivpn.net/knowledgebase/billing/voucher-cards-faq) with redeem codes.

#### :material-check:{ .pg-green } Soporte de WireGuard

IVPN soporta el protocolo WireGuard®. [WireGuard](https://wireguard.com) es un protocolo más reciente que utiliza [criptografía](https://wireguard.com/protocol) de última generación. Además, WireGuard aspira ser más simple y veloz.

IVPN [recomienda](https://ivpn.net/wireguard) el uso de WireGuard con su servicio y, como tal, el protocolo es el predeterminado en todas las aplicaciones de IVPN. IVPN también ofrece un generador de configuración de WireGuard para utilizarlo con las [aplicaciones](https://wireguard.com/install) WireGuard oficiales.

#### :material-information-outline:{ .pg-blue } Soporte de IPv6

IVPN te permite [conectarte a servicios usando IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6) pero no te permite conectarte desde un dispositivo usando una dirección IPv6.

#### :material-alert-outline:{ .pg-orange } Reenvío Remoto de Puertos

Anteriormente, IVPN admitía el reenvío de puertos, pero eliminó la opción en [junio de 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). La ausencia de esta característica podría afectar negativamente a ciertas aplicaciones, especialmente a las aplicaciones peer-to-peer como los clientes torrent.

#### :material-check:{ .pg-green } Anti censura

IVPN tiene modos de ofuscación usando [V2Ray](https://v2ray.com/en/index.html) lo cual ayuda en situaciones donde los protocolos VPN como OpenVPN o Wireguard están bloqueados. Actualmente, esta característica solo está disponible en la versión para escritorio e [iOS](https://ivpn.net/knowledgebase/ios/v2ray). Este cuenta con dos modos donde puede usar [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) sobre QUIC o conexiones TCP. QUIC es un moderno protocolo con mejor control de la congestión y puede ser más rápido con menor latencia. El modo TCP ayuda para que tus datos aparezcan como tráfico HTTP regular.

#### :material-check:{ .pg-green } Clientes Móviles

IVPN ha publicado clientes [en App Store](https://apps.apple.com/app/id1193122683) y [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), ambos con una interfaz fácil de usar en lugar de requerir que configures manualmente tu conexión WireGuard. El cliente para Android también está disponible en [GitHub](https://github.com/ivpn/android-app/releases).

#### :material-information-outline:{ .pg-blue } Notas adicionales

Los clientes de IVPN soportan la autenticación de doble factor. IVPN también ofrece la función "[AntiTracker](https://ivpn.net/antitracker)", que bloquea las redes publicitarias y los rastreadores a nivel de red.

### Mullvad

<div class="admonition recommendation" markdown>

![Logo de Mullvad](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** es una VPN rápida y económica que se centra en la transparencia y la seguridad. Ha estado en operación desde 2009. Mullvad tiene su sede en Suecia y ofrece una garantía de devolución del dinero de 14 días para los [métodos de pago](https://mullvad.net/en/help/refunds) que lo permitan.

[:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 49 Países

Mullvad tiene [servidores en 49 países](https://mullvad.net/servers).(1) Elegir un proveedor de VPN con el servidor más cercano a ti reducirá la latencia del tráfico de red que envías. Esto se debe a que es una ruta más corta (menos saltos) hasta el destino.
{ .annotate }

1. Last checked: 2025-10-28

También pensamos que es mejor para la seguridad de las claves privadas del proveedor de VPN si utilizan [servidores dedicados](https://en.wikipedia.org/wiki/Dedicated_hosting_service), en lugar de soluciones compartidas más baratas (con otros clientes) como los [[servidores privados virtuales](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Auditado Independientemente

Mullvad se ha sometido a múltiples [auditorías independientes](https://mullvad.net/en/blog/tag/audits) y ha anunciado públicamente sus esfuerzos por realizar [auditorías anuales](https://mullvad.net/en/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) de sus aplicaciones e infraestructura.

#### :material-check:{ .pg-green } Clientes de Código Abierto

Mullvad proporciona el código fuente para sus clientes de escritorio y móviles en su [organización de GitHub](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Acepta Efectivo y Monero

Mullvad, además de tarjetas de crédito/débito y PayPal, también acepta Bitcoin, Bitcoin Cash, **Monero** y **efectivo/moneda local** como métodos anónimos de pago. You can also purchase [prepaid cards](https://mullvad.net/en/help/partnerships-and-resellers) with redeem codes. Mullvad también acepta Swish y transferencias bancarias, así como algunos sistemas de pago europeos.

#### :material-check:{ .pg-green } Soporte de WireGuard

IVPN soporta el protocolo WireGuard®. [WireGuard](https://wireguard.com) es un protocolo más reciente que utiliza [criptografía](https://wireguard.com/protocol) de última generación. Además, WireGuard aspira ser más simple y veloz.

Mullvad [recomienda a](https://mullvad.net/en/help/why-wireguard) el uso de WireGuard con su servicio. It is the only protocol supported on their mobile apps, and their desktop apps will [lose OpenVPN support](https://mullvad.net/en/blog/reminder-that-openvpn-is-being-removed) in 2025. Additionally, their servers will stop accepting OpenVPN connections by January 15, 2026. Mullvad también ofrece un generador de configuraciones WireGuard para su uso con las [aplicaciones](https://wireguard.com/install) oficiales de WireGuard.

#### :material-check:{ .pg-green } Soporte de IPv6

Mullvad te permite [acceder a servicios almacenados en IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) y conectarte desde un dispositivo usando una dirección IPv6.

#### :material-alert-outline:{ .pg-orange } Reenvío Remoto de Puertos

Anteriormente, Mullvad admitía el reenvío de puertos, pero eliminó esta opción en [mayo de 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). La ausencia de esta característica podría afectar negativamente a ciertas aplicaciones, especialmente a las aplicaciones peer-to-peer como los clientes torrent.

#### :material-check:{ .pg-green } Anti censura

Mullvad ofrece varias funciones para ayudar a eludir la censura y acceder libremente a Internet:

- **Modos de ofuscación**: Mullvad tiene dos modos de ofuscación incorporados: "UDP sobre TCP" y ["WireGuard sobre Shadowsocks"](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard). Estos modos disfrazan su tráfico VPN como tráfico web normal, lo que dificulta su detección y bloqueo por parte de los censores. Supuestamente, China tiene que utilizar un [nuevo método para interrumpir el tráfico enrutado por Shadowsocks](https://gfw.report/publications/usenixsecurity23/en).
- **Ofuscación avanzada con Shadowsocks y v2ray**: Para usuarios más avanzados, Mullvad proporciona una guía sobre cómo utilizar el plugin [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) con clientes Mullvad. Esta configuración proporciona una capa adicional de ofuscación y cifrado.
- **IPs de servidor personalizadas**: Para contrarrestar el bloqueo de IPs, puedes solicitar IPs de servidor personalizadas al equipo de soporte de Mullvad. Una vez que recibas las IPs personalizadas, puedes introducir el archivo de texto en la configuración de "Anulación de IPs del servidor", que anulará las direcciones IPs del servidor elegidas con otras que el censor no conozca.
- **Puentes y proxies**: Mullvad también permite utilizar puentes o proxies para llegar a su API (necesario para la autenticación), lo que puede ayudar a eludir los intentos de censura que bloquean el acceso a la propia API.

#### :material-check:{ .pg-green } Clientes Móviles

Mullvad ha publicado clientes para [App Store](https://apps.apple.com/app/id1488466513) y [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn), ambos con una interfaz fácil de usar en lugar de requerir que configures manualmente tu conexión WireGuard. El cliente de Android también está disponible en [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Notas adicionales

Mullvad es muy transparente sobre los nodos que [posee o alquila](https://mullvad.net/en/servers). También ofrecen la opción de activar la DefensaContra el Análisis de Tráfico Guiado por Inteligencia Artificial[(DAITA](https://mullvad.net/en/blog/daita-defense-against-ai-guided-traffic-analysis)) en sus aplicaciones. DAITA protege contra la amenaza del análisis avanzado de tráfico, que puede utilizarse para relacionar patrones en el tráfico VPN con sitios web específicos.

## Criterios

<div class="admonition danger" markdown>
<p class="admonition-title">Peligro</p>

Es importante tener en cuenta que el uso de un proveedor de VPN no le hará anónimo, pero le dará mayor privacidad en ciertas situaciones. Una VPN no es una herramienta para actividades ilegales. No confíes en una política de "sin registro".

</div>

**Por favor, tenga en cuenta que no estamos afiliados a ninguno de los proveedores que recomendamos. Esto nos permite ofrecer recomendaciones completamente objetivas.** Además de [nuestros cirterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos para cualquier proveedor de VPN que desee ser recomendado, incluyendo un cifrado fuerte, auditorías de seguridad independientes, tecnología moderna y más. Te sugerimos que te familiarices con esta lista antes de elegir un proveedor VPN, y lleves a cabo tu propia investigación para asegurar que el proveedor VPN que elijas sea lo más fiable posible.

### Tecnología

Exigimos que todos nuestros proveedores de VPN recomendados proporcionen archivos de configuración estándar que puedan utilizarse en un cliente genérico de código abierto. **Si** una VPN proporciona su propio cliente personalizado, requerimos un kill switch para bloquear las filtraciones de datos de red cuando se desconecte.

**Mínimo para Calificar:**

- Compatibilidad con protocolos robustos como WireGuard.
- Kill switch integrado en los clientes.
- Soporte de multisalto. Los saltos múltiples son importantes para mantener la privacidad de los datos en caso de que un solo nodo se vea comprometido.
- Si se proporcionan clientes VPN, deben ser de [código abierto](https://en.wikipedia.org/wiki/Open_source), como el software VPN que generalmente llevan incorporado. Creemos que la disponibilidad del [código fuente](https://en.wikipedia.org/wiki/Source_code) proporciona una mayor transparencia sobre lo que hace realmente el programa.
- Funciones de resistencia a la censura diseñadas para eludir cortafuegos sin DPI.

**Mejor Caso:**

- Kill switch con opciones altamente configurables (activar/desactivar en determinadas redes, en el arranque, etc.)
- Clientes VPN fáciles de usar
- Soporte de [IPv6](https://en.wikipedia.org/wiki/IPv6). Esperamos que los servidores permitan las conexiones entrantes a través de IPv6 y le permitan acceder a los servicios alojados en direcciones IPv6.
- La capacidad de [redirección de puertos](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) ayuda a crear conexiones cuando se utiliza software de intercambio de archivos P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)), Freenet, o se aloja un servidor (por ejemplo, Mumble).
- Tecnología de ofuscación que camufla la verdadera naturaleza del tráfico de Internet, diseñada para eludir métodos avanzados de censura de Internet como el DPI.

### Privacidad

Preferimos que nuestros proveedores recomendados recojan la menor cantidad de datos posible. Es necesario no recoger información personal en el momento de la inscripción y aceptar formas de pago anónimas.

**Mínimo para Calificar:**

- [Criptomoneda anónima](cryptocurrency.md) **o** opción de pago en efectivo.
- No se requiere información personal para registrarse: Sólo nombre de usuario, contraseña y correo electrónico como máximo.

**Mejor Caso:**

- Acepta múltiples [opciones de pago anónimo](advanced/payments.md).
- No se aceptan datos personales (nombre de usuario generado automáticamente, no se requiere correo electrónico, etc.).

### Seguridad

Una VPN no tiene sentido si ni siquiera puede proporcionar una seguridad adecuada. Exigimos que todos nuestros proveedores recomendados cumplan los estándares de seguridad actuales. Lo ideal sería que utilizaran por defecto esquemas de encriptación más resistentes al futuro. También requerimos que un tercero independiente audite la seguridad del proveedor, idealmente de una manera muy completa y sobre una base repetida (anual).

**Mínimo para Calificar:**

- Esquemas de cifrado fuertes: OpenVPN con autenticación SHA-256; RSA-2048 o mejor handshake; AES-256-CBC o cifrado de datos AES-256-GCM.
- Secreto Hacia Adelante.
- Auditorías de seguridad publicadas por una empresa externa de prestigio.
- Servidores VPN que utilizan encriptación de disco completo o son solo RAM.

**Mejor Caso:**

- Cifrado más fuerte: RSA-4096.
- Cifrado opcional de resistencia cuántica.
- Auditorías de seguridad exhaustivas publicadas por una empresa externa de prestigio.
- Programas de recompensa de errores y/o un proceso coordinado de divulgación de vulnerabilidades.
- Servidores VPN solo RAM.

### Confianza

No confiarías tus finanzas a alguien con una identidad falsa, así que ¿por qué confiarle tus datos de Internet? Requerimos que nuestros proveedores recomendados sean públicos sobre su propiedad o liderazgo. También nos gustaría ver informes de transparencia frecuentes, especialmente en lo que se refiere a cómo se gestionan las solicitudes del gobierno.

**Mínimo para Calificar:**

- Liderazgo o titularidad de cara al público.
- Empresa con sede en una jurisdicción donde no se la puede obligar a realizar registros secretos.

**Mejor Caso:**

- Liderazgo de cara al público.
- Informes de transparencia frecuentes.

### Marketing

Con los proveedores de VPN que recomendamos nos gusta ver un marketing responsable.

**Mínimo para Calificar:**

- Debe tener análisis propios (es decir, sin Google Analytics).

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

Aunque no son estrictamente requisitos, hay algunos factores en los que nos fijamos a la hora de determinar qué proveedores recomendar. Entre ellas, la funcionalidad de bloqueo de contenidos, los canarios de garantía, la excelente atención al cliente, el número de conexiones simultáneas permitidas, etc.
