---
title: Filtrado de DNS
meta_title: "Soluciones de Autoalojamiento de DNS - Privacy Guides"
icon: material/dns
description: Para nuestros lectores más técnicos, el autoalojamiento de una solución de DNS puede proporcionar filtrado para dispositivos no cubiertos por las soluciones de DNS basadas en la nube.
cover: dns.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-server-network: Proveedores de Servicios](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: Capitalismo de Vigilancia](../basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

El **autoalojamiento de DNS** es útil para proporcionar [filtrado de DNS](https://cloudflare.com/learning/access-management/what-is-dns-filtering) en plataformas controladas, como televisores inteligentes y otros dispositivos IoT, ya que no se necesita ningún software del lado del cliente. Ten en cuenta que las soluciones de DNS que se indican a continuación suelen estar restringidas a tu red doméstica o local, a menos que establezcas una configuración más avanzada.

## Sumideros de DNS

Los [**sumideros de DNS**](https://en.wikipedia.org/wiki/DNS_sinkhole) utilizan el filtrado de DNS para bloquear contenidos web no deseados, como la publicidad.

### Pi-Hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](../assets/img/self-hosting/pi-hole.svg){ align=right }

**Pi-hole** es un sumidero de DNS de código abierto que cuenta con una interfaz web intuitiva para ver información detallada y gestionar el contenido bloqueado. Pi-hole está diseñado para alojarse en una Raspberry Pi, pero no se limita a dicho hardware.

[:octicons-home-16: Página Principal](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title="Contribuir " }

</div>

### AdGuard Home

<div class="admonition recommendation" markdown>

![AdGuard Home logo](../assets/img/self-hosting/adguard-home.svg){ align=right }

**AdGuard Home** es un sumidero de DNS de código abierto que cuenta con una interfaz web pulida para ver información detallada y gestionar el contenido bloqueado.

[:octicons-home-16: Página Principal](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Código Fuente" }

</div>
