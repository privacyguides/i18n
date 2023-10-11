---
title: "Firmware per router"
icon: material/router-wireless
description: Questi sistemi operativi alternativi sono utilizzabili per proteggere il tuo router o il punto d'accesso del Wi-Fi.
cover: router.webp
---

Di seguito sono elencati alcuni sistemi operativi alternativi, utilizzabili sui router, punti d'accesso della Wi-Fi, etc.

## OpenWrt

!!! recommendation

    ![Logo di OpenWrt](assets/img/router/openwrt.svg#only-light){ align=right }
    ![Logo di OpenWrt](assets/img/router/openwrt-dark.svg#only-dark){ align=right }
    
    **OpenWrt** è un sistema operativo basato su Linux, utilizzato principalmente su dispositivi incorporati per instradare il traffico di rete. Include util-linux, uClibc e BusyBox. Tutti i componenti sono stati ottimizzati per i router domestici.
    
    [:octicons-home-16: Home](https://openwrt.org){ .md-button .md-button--primary }
    [:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=Contribuisci }

È possibile consultare la [tabella hardware](https://openwrt.org/toh/start) di OpenWrt per verificare se il tuo dispositivo è supportato.

## OPNsense

!!! recommendation

    ![Logo di OPNSense](assets/img/router/opnsense.svg){ align=right }
    
    **OPNsense** è una piattaforma open source di firewall e instradamento basata su FreeBSD, che incorpora molte funzionalità avanzate come il modellamento del traffico, il bilanciamento del carico e le funzionalità VPN, con molte altre funzionalità disponibili sotto forma di plugin. OPNsense è comunemente distribuito come firewall perimetrale, router, punto d'accesso wireless, server DHCP, server DNS ed endpoint VPN.
    
    [:octicons-home-16: Home](https://opnsense.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/opnsense){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://opnsense.org/donate/){ .card-link title=Contribuisci}

OPNsense è stato originariamente sviluppato come una biforcazione di [pfSense](https://en.wikipedia.org/wiki/PfSense), ed entrambi i progetti sono noti per essere distribuzioni di firewall gratuite e affidabili, che offrono funzionalità spesso trovate soltanto in costosi firewall commerciali. Lanciato nel 2015, gli sviluppatori di OPNsense hanno [citato](https://docs.opnsense.org/history/thefork.html) numerosi problemi di sicurezza e qualità del codice di pfSense che, a loro avviso, rendevano necessaria una biforcazione del progetto, nonché le numerose preoccupazioni sull'acquisizione di maggioranza di pfSense da parte di Netgate, e della futura direzione del progetto di pfSense.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

!!! esempio "Questa sezione è nuova"

    Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

- Deve essere open source.
- Deve ricevere aggiornamenti regolari.
- Deve supportare un'ampia varietà di hardware.
