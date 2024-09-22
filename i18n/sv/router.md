---
title: "Router Firmware"
icon: material/router-wireless
description: Alternative operating systems for securing your router or Wi-Fi access point.
cover: router.webp
---

Nedan följer några alternativa operativsystem som kan användas på routrar, Wi-Fi-accesspunkter osv.

## OpenWrt

<div class="admonition recommendation" markdown>

![OpenWrt-logotyp](assets/img/router/openwrt.svg#only-light){ align=right }
![OpenWrt logo](assets/img/router/openwrt-dark.svg#only-dark){ align=right }

**OpenWrt** är ett Linuxbaserat operativsystem som främst används på inbyggda enheter för att dirigera nätverkstrafik. Den innehåller util-linux, uClibc och BusyBox. Alla komponenter har optimerats för hem routrar.

[:octicons-home-16: Homepage](https://openwrt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="Source Code" }
[:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=Contribute }

</details>

</div>

Du kan se OpenWrts [tabell över maskinvara](https://openwrt.org/toh/start) för att kontrollera om din enhet stöds.

## OPNsense

<div class="admonition recommendation" markdown>

![OPNsense logo](assets/img/router/opnsense.svg){ align=right }

**OPNsense** is an open-source, FreeBSD-based firewall and routing platform which incorporates many advanced features such as traffic shaping, load balancing, and VPN capabilities, with many more features available in the form of plugins. OPNsense används vanligen som brandvägg, router, trådlös åtkomstpunkt, DHCP-server, DNS-server och VPN-slutpunkt.

[:octicons-home-16: Homepage](https://opnsense.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/opnsense){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opnsense.org/donate){ .card-link title=Contribute }

</details>

</div>

OPNsense utvecklades ursprungligen som en gaffel av [pfSense](https://en.wikipedia.org/wiki/PfSense), och båda projekten är kända för att vara fria och pålitliga brandväggsdistributioner som erbjuder funktioner som ofta endast finns i dyra kommersiella brandväggar. Utvecklarna av OPNsense [, som lanserades 2015, citerade](https://docs.opnsense.org/history/thefork.html) ett antal säkerhets- och kodkvalitetsproblem med pfSense som de ansåg nödvändiggjorde en delning av projektet, samt oro över Netgates majoritetsförvärv av pfSense och pfSense-projektets framtida inriktning.

## Kriterier

**Observera att vi inte är knutna till något av de projekt som vi rekommenderar.** Förutom [våra standardkriterier](about/criteria.md)har vi utvecklat en tydlig uppsättning krav som gör det möjligt för oss att ge objektiva rekommendationer. Vi föreslår att du bekantar dig med den här listan innan du väljer att använda ett projekt, och att du gör din egen forskning för att se till att det är rätt val för dig.

- Måste vara öppen källkod.
- Måste få regelbundna uppdateringar.
- Must support a wide variety of hardware.
