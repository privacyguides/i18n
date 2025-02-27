---
title: "Firmware per Router"
icon: material/router-wireless
description: Alternative operating systems for securing your router or Wi-Fi access point.
cover: router.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Capitalismo di sorveglianza](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-bug-outline: Attacchi Passivi](basics/common-threats.md#security-and-privacy ""){.pg-orange}

Below are a few alternative operating systems that can be used on routers, Wi-Fi access points, etc.

## OpenWrt

<div class="admonition recommendation" markdown>

![Logo di OpenWrt](assets/img/router/openwrt.svg#only-light){ align=right }
![Logo di OpenWrt](assets/img/router/openwrt-dark.svg#only-dark){ align=right }

**OpenWrt** è un sistema operativo basato su Linux, utilizzato principalmente su dispositivi incorporati per instradare il traffico di rete. Include util-linux, uClibc e BusyBox. All the components have been optimized for home routers.

[:octicons-home-16: Home](https://openwrt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=Contribuisci }

</details>

</div>

È possibile consultare la [tabella hardware](https://openwrt.org/toh/start) di OpenWrt per verificare se il tuo dispositivo è supportato.

## OPNsense

<div class="admonition recommendation" markdown>

![Logo di OPNsense](assets/img/router/opnsense.svg){ align=right }

**OPNsense** è una piattaforma open source di firewall e routing basata su FreeBSD che incorpora molte funzionalità avanzate come il traffic shaping, il bilanciamento del carico e le funzionalità VPN, con molte altre funzionalità disponibili sotto forma di plugin. OPNsense è comunemente distribuito come firewall perimetrale, router, punto d'accesso wireless, server DHCP, server DNS ed endpoint VPN.

[:octicons-home-16: Pagina Principale](https://opnsense.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/opnsense){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://opnsense.org/donate){ .card-link title=Contribuisci }

</details>

</div>

OPNsense è stato originariamente sviluppato come una biforcazione di [pfSense](https://en.wikipedia.org/wiki/PfSense), ed entrambi i progetti sono noti per essere distribuzioni di firewall gratuite e affidabili, che offrono funzionalità spesso trovate soltanto in costosi firewall commerciali. Lanciato nel 2015, gli sviluppatori di OPNsense hanno [citato](https://docs.opnsense.org/history/thefork.html) numerosi problemi di sicurezza e qualità del codice di pfSense che, a loro avviso, rendevano necessaria una biforcazione del progetto, nonché le numerose preoccupazioni sull'acquisizione di maggioranza di pfSense da parte di Netgate, e della futura direzione del progetto di pfSense.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

- Deve essere open source.
- Deve ricevere aggiornamenti regolari.
- Deve supportare un'ampia varietà di hardware.
