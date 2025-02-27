---
title: "Firmware para Roteadores"
icon: material/router-wireless
description: Alternative operating systems for securing your router or Wi-Fi access point.
cover: router.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Surveillance Capitalism](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-bug-outline: Ataques Passivos](basics/common-threats.md#security-and-privacy ""){.pg-orange}

Below are a few alternative operating systems that can be used on routers, Wi-Fi access points, etc.

## OpenWrt

<div class="admonition recommendation" markdown>

![OpenWrt logo](assets/img/router/openwrt.svg#only-light){ align=right }
![OpenWrt logo](assets/img/router/openwrt-dark. vg#only-dark){ align=right }

**OpenWrt** é um sistema operacional baseado em Linux; ele é usado principalmente em dispositivos incorporados (embedded) para rotear o tráfego de rede. Inclui util-linux, uClibc e BusyBox. All the components have been optimized for home routers.

[:octicons-home-16: Homepage](https://openwrt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title=Documentação}
[:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="Source Code" }
[:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=Contribuir }

</details>

</div>

Você pode consultar a tabela [de hardware](https://openwrt.org/toh/start) do OpenWrt para verificar se o seu dispositivo é compatível.

## OPNsense

<div class="admonition recommendation" markdown>

![OPNsense logo](assets/img/router/opnsense.svg){ align=right }

**OPNsense** is an open-source, FreeBSD-based firewall and routing platform which incorporates many advanced features such as traffic shaping, load balancing, and VPN capabilities, with many more features available in the form of plugins. O OPNsense é comumente implantado como um firewall de perímetro, roteador, ponto de acesso wireless, servidor DHCP, servidor DNS e endpoint de VPN.

[:octicons-home-16: Homepage](https://opnsense.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/opnsense){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opnsense.org/donate){ .card-link title=Contribute }

</details>

</div>

OPNsense foi originalmente desenvolvido como um fork do [pfSense](https://en.wikipedia.org/wiki/PfSense), e ambos os projetos são conhecidos por serem distribuições de firewall gratuitas e confiáveis que oferecem recursos frequentemente encontrados apenas em firewalls comerciais caros. Lançado em 2015, os desenvolvedores do OPNsense [citaram](https://docs.opnsense.org/history/thefork.html) uma série de problemas de segurança e qualidade de código com o pfSense. Assim, eles sentiram necessário criar um fork do projeto, além de terem preocupações sobre a aquisição majoritária do pfSense pela Netgate e a direção futura do projeto pfSense.

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

- Deve ser de código aberto.
- Deve receber atualizações regulares.
- Must support a wide variety of hardware.
