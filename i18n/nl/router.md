---
title: "Router Firmware"
icon: material/router-wireless
description: Alternative operating systems for securing your router or Wi-Fi access point.
cover: router.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Surveillance kapitalisme](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-bug-outline: Passieve aanvallen](basics/common-threats.md#security-and-privacy ""){.pg-orange}

Below are a few alternative operating systems that can be used on routers, Wi-Fi access points, etc.

## OpenWrt

<div class="admonition recommendation" markdown>

![OpenWrt logo](assets/img/router/openwrt.svg#only-light){ align=right }
![OpenWrt logo](assets/img/router/openwrt-dark.svg#only-dark){ align=right }

**OpenWrt** is een op Linux gebaseerd besturingssysteem; het wordt voornamelijk gebruikt op embedded apparaten om netwerkverkeer te routeren. De belangrijkste onderdelen zijn de Linux kernel, util-linux, uClibc, en BusyBox. All the components have been optimized for home routers.

[:octicons-home-16: Homepage](https://openwrt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title=Documentatie}
[:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="Broncode" }
[:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=Bijdragen}

</details>

</div>

Je kunt OpenWrt's [tabel van hardware](https://openwrt.org/toh/start) raadplegen om te controleren of jouw toestel ondersteund wordt.

## OPNsense

<div class="admonition recommendation" markdown>

![OPNsense logo](assets/img/router/opnsense.svg){ align=right }

**OPNsense** is an open-source, FreeBSD-based firewall and routing platform which incorporates many advanced features such as traffic shaping, load balancing, and VPN capabilities, with many more features available in the form of plugins. OPNsense wordt gewoonlijk ingezet als perimeter firewall, router, draadloos toegangspunt, DHCP server, DNS server en VPN eindpunt.

[:octicons-home-16: Homepage](https://opnsense.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/opnsense){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opnsense.org/donate){ .card-link title=Contribute }

</details>

</div>

OPNsense werd oorspronkelijk ontwikkeld als een fork van [pfSense](https://en.wikipedia.org/wiki/PfSense), en beide projecten staan bekend als vrije en betrouwbare firewall-distributies die mogelijkheden bieden die vaak alleen in dure commerciële firewalls te vinden zijn. De ontwikkelaars van OPNsense [, gelanceerd in 2015, noemden](https://docs.opnsense.org/history/thefork.html) een aantal beveiligings- en code-kwaliteitsproblemen met pfSense die volgens hen een fork van het project noodzakelijk maakten, evenals zorgen over de meerderheidsovername van pfSense door Netgate en de toekomstige richting van het pfSense-project.

## Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

- Moet open source zijn.
- Moet regelmatig updates ontvangen.
- Moet een grote verscheidenheid aan hardware ondersteunen.
