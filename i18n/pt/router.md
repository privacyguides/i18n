---
title: "Firmware do router"
icon: material/router-wireless
description: Alternative operating systems for securing your router or Wi-Fi access point.
cover: router.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Capitalismo de vigilância](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-bug-outline: Ataques passivos](basics/common-threats.md#security-and-privacy ""){.pg-orange}

Below are a few alternative operating systems that can be used on routers, Wi-Fi access points, etc.

## OpenWrt

<div class="admonition recommendation" markdown>

![Logótipo OpenWrt](assets/img/router/openwrt.svg#only-light){ align=right }
![Logótipo OpenWrt](assets/img/router/openwrt-dark.svg#only-dark){ align=right }

O **OpenWrt** é um sistema operativo baseado em Linux; é utilizado principalmente em dispositivos incorporados para encaminhar o tráfego de rede. Inclui util-linux, uClibc e BusyBox. Todos os componentes foram otimizados para routers domésticos.

[:octicons-home-16: Homepage](https://openwrt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title=Documentação}
[:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="Código-fonte" }
[:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=Contribuir }

</details>

</div>

Pode consultar a [tabela de hardware](https://openwrt.org/toh/start) do OpenWrt para verificar se o seu dispositivo é suportado.

## OPNsense

<div class="admonition recommendation" markdown>

![OPNsense logo](assets/img/router/opnsense.svg){ align=right }

**OPNsense** is an open-source, FreeBSD-based firewall and routing platform which incorporates many advanced features such as traffic shaping, load balancing, and VPN capabilities, with many more features available in the form of plugins. O OPNsense é normalmente implementado como firewall de perímetro, router, ponto de acesso sem fio, servidor DHCP, servidor DNS e ponto terminal de VPN.

[:octicons-home-16: Homepage](https://opnsense.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/opnsense){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opnsense.org/donate){ .card-link title=Contribute }

</details>

</div>

O OPNsense foi originalmente desenvolvido como um fork de [pfSense](https://en.wikipedia.org/wiki/PfSense), e ambos os projetos são conhecidos por serem distribuições de firewall livres e fiáveis que oferecem funcionalidades muitas vezes apenas encontradas em firewalls comerciais caras. O OPNsense foi lançado em 2015 como fork do pfSense, pelo facto dos seus desenvolvedores terem [detetado](https://docs.opnsense.org/history/thefork.html) uma série de problemas de segurança e qualidade do código produto original, além das preocupações relacionadas com a aquisição maioritária do pfSense pela Netgate, que colocavam dúvidas quanto ao seu futuro.

## Critérios

**Note que não estamos associados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrão](about/criteria.md), temos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar por um projeto e que desenvolva a sua própria investigação para garantir que se trata da escolha certa para si.

- Deve ser de fonte aberta.
- Deve receber atualizações regulares.
- Deve suportar uma grande variedade de hardware.
