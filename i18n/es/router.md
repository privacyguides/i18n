---
title: "Firmware del Router"
icon: material/router-wireless
description: Sistemas operativos alternativos para proteger tu router o punto de acceso Wi-Fi.
cover: router.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-bug-outline: Ataques pasivos](basics/common-threats.md#security-and-privacy ""){.pg-orange}

A continuación se indican algunos sistemas operativos alternativos que pueden utilizarse en routers, puntos de acceso Wi-Fi, etc.

## OpenWrt

<div class="admonition recommendation" markdown>

![OpenWrt logo](assets/img/router/openwrt.svg#only-light){ align=right }
![OpenWrt logo](assets/img/router/openwrt-dark.svg#only-dark){ align=right }

**OpenWrt** es un sistema operativo basado en Linux; se utiliza principalmente en dispositivos integrados para enrutar el tráfico de red. Incluye util-linux, uClibc, y BusyBox. All the components have been optimized for home routers.

[:octicons-home-16: Página Principal](https://openwrt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="Código Fuente }
[:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=Contribuir }

</details>

</div>

Puedes consultar [ la tabla de hardware](https://openwrt.org/toh/start) de OpenWrt para comprobar si tu dispositivo es compatible.

## OPNsense

<div class="admonition recommendation" markdown>

![OPNsense logo](assets/img/router/opnsense.svg){ align=right }

**OPNsense** es una plataforma de enrutamiento y cortafuegos de código abierto basada en FreeBSD que incorpora muchas características avanzadas, como la conformación del tráfico, el equilibrio de carga y las capacidades de VPN, con muchas más características disponibles en forma de plugins. OPNsense se implementa habitualmente como cortafuegos perimetral, router, punto de acceso inalámbrico, servidor DHCP, servidor DNS y punto final VPN.

[:octicons-home-16: Página Principal](https://opnsense.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/opnsense){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://opnsense.org/donate){ .card-link title=Contribuir }

</details>

</div>

OPNsense se desarrolló originalmente como una bifurcación de [pfSense](https://en.wikipedia.org/wiki/PfSense), y ambos proyectos destacan por ser distribuciones de cortafuegos libres y fiables que ofrecen características que a menudo sólo se encuentran en los costosos cortafuegos comerciales. Lanzado en 2015, los desarrolladores de OPNsense [citaron a](https://docs.opnsense.org/history/thefork.html) una serie de problemas de seguridad y de calidad del código de pfSense que consideraban que necesitaba una bifurcación del proyecto, así como preocupaciones por la adquisición mayoritaria de pfSense por parte de Netgate y la futura dirección del proyecto pfSense.

## Criterios

**Por favor, ten en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten proporcionar recomendaciones objetivas. Te sugerimos que te familiarices con esta lista antes de elegir usar un proyecto, y que lleves a cabo tu propia investigación para asegurarte de que es la elección correcta para ti.

- Debe ser de código abierto.
- Debe recibir actualizaciones de manera periódica.
- Debe ser compatible con una amplia variedad de hardware.
