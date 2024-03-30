---
title: "Router Firmware"
icon: material/router-wireless
description: These alternative operating systems can be used to secure your router or Wi-Fi access point.
cover: router.webp
---

Lejjebb bemutatunk néhány alternatív operációs rendszert, amelyek használhatók routereken, Wi-Fi hozzáférési pontokon, stb.

## OpenWrt

<div class="admonition recommendation" markdown>

![OpenWrt logo](assets/img/router/openwrt.svg#only-light){ align=right }
![OpenWrt logo](assets/img/router/openwrt-dark.svg#only-dark){ align=right }

Az **OpenWrt** egy Linux alapú operációs rendszer; elsősorban beágyazott eszközökön használatos, hálózati forgalom irányítására. Tartalmazza az util-linux, uClibc és BusyBox programokat. Az összes komponens otthoni routerekhez lett optimalizálva.

[:octicons-home-16: Honlap](https://openwrt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title=Dokumentáció}
[:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="Forráskód" }
[:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=Közreműködés }

</details>

</div>

Az OpenWrt [hardvertáblázatában](https://openwrt.org/toh/start) ellenőrizheted, hogy az eszközöd támogatott-e.

## OPNsense

<div class="admonition recommendation" markdown>

![OPNsense logo](assets/img/router/opnsense.svg){ align=right }

**OPNsense** is an open-source, FreeBSD-based firewall and routing platform which incorporates many advanced features such as traffic shaping, load balancing, and VPN capabilities, with many more features available in the form of plugins. Az OPNsense-t általában peremtűzfalként, routerként, vezeték nélküli hozzáférési pontként, DHCP-szerverként, DNS-szerverként és VPN végpontként vetik be.

[:octicons-home-16: Homepage](https://opnsense.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/opnsense){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opnsense.org/donate){ .card-link title=Contribute }

</details>

</div>

Az OPNsense eredetileg a [pfSense](https://en.wikipedia.org/wiki/PfSense) forkjaként lett kifejlesztve, és mindkét projekt arról ismert, hogy ingyenes és megbízható tűzfal disztribúciók, amelyek gyakran csak drága kereskedelmi tűzfalakban található funkciókat kínálnak. A 2015-ben indított OPNsense fejlesztői számos biztonsági és kódminőségi problémára, a Netgate általi többségi pfSense felvásárlásra, valamint a pfSense projekt jövőbeli irányára [hivatkozva](https://docs.opnsense.org/history/thefork.html) a pfSense-el kapcsolatban úgy érezték, hogy ezek miatt az aggályok miatt szükségessé vált egy projekt fork létrehozása.

## Követelmények

**Tartsd figyelemben, hogy nem állunk kapcsolatban az általunk ajánlott projektek egyikével sem.** Az [alap kritériumaink mellett](about/criteria.md), egyértelmű követelményrendszert dolgoztunk ki, hogy objektív ajánlásokat tudjunk tenni. Javasoljuk, hogy ismerkedj meg ezzel a listával, mielőtt kiválasztanál egy projektet, és végezz saját kutatásokat, hogy megbizonyosodj arról, hogy ez a megfelelő választás számodra.

- Nyílt forráskódúnak kell lennie.
- Rendszeres frissítéseket kell kapnia.
- Sokféle hardvert kell támogatnia.
