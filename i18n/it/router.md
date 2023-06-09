---
title: "Firmware per router"
icon: material/router-wireless
description: Questi sistemi operativi alternativi possono essere utilizzati per proteggere il router o l'access point del Wi-Fi.
cover: router.png
---

Di seguito sono elencati alcuni sistemi operativi alternativi che possono essere usati su router, access point Wi-Fi, ecc.

## OpenWrt

!!! recommendation

    ![OpenWrt logo](assets/img/router/openwrt.svg#only-light){ align=right }
    ![OpenWrt logo](assets/img/router/openwrt-dark.svg#only-dark){ align=right }
    
    **OpenWrt** è un sistema operativo basato su Linux, usato principalmente su dispositivi embedded per instradare il traffico di rete. Include util-linux, uClibc e BusyBox. Tutti i componenti sono stati ottimizzati per i router domestici.
    
    [:octicons-home-16: Pagina Principale](https://openwrt.org){ .md-button .md-button--primary }
    [:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=Contribuisci }

È possibile consultare la [tabella degli hardware](https://openwrt.org/toh/start) di OpenWrt per verificare se il tuo dispositivo è supportato.

## OPNsense

!!! recommendation

    ![pfSense logo](assets/img/router/opnsense.svg){ align=right }
    
    **OPNsense** è una piattaforma open source di firewall e routing basata su FreeBSD che incorpora molte funzionalità avanzate come il traffic shaping, il bilanciamento del carico e le funzionalità VPN, con molte altre funzionalità disponibili sotto forma di plugin. OPNsense viene comunemente utilizzato come firewall perimetrale, router, access point wireless, server DHCP, server DNS ed endpoint VPN.
    
    [:octicons-home-16: Pagina Principale](https://opnsense.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/opnsense){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://opnsense.org/donate/){ .card-link title=Contribuisci}

OPNsense è stato originariamente sviluppato come fork di [pfSense](https://en.wikipedia.org/wiki/PfSense), ed entrambi i progetti sono noti per essere distribuzioni di firewall gratuite e affidabili che offrono funzionalità spesso presenti solo in costosi firewall commerciali. Lanciato nel 2015, gli sviluppatori di OPNsense [hanno citato](https://docs.opnsense.org/history/thefork.html) una serie di problemi di sicurezza e di qualità del codice di pfSense che, a loro avviso, rendevano necessario un fork del progetto, oltre a preoccupazioni sull'acquisizione della maggioranza di pfSense da parte di Netgate e sulla futura direzione del progetto pfSense.

## Criteri

**Si noti che non siamo affiliati a nessuno dei progetti che raccomandiamo.** Oltre ai [ nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie di requisiti chiari che ci consentono di fornire raccomandazioni obiettive. Ti consigliamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le vostre ricerche per assicurarvi che sia la scelta giusta per voi.

!!! example "Questa sezione è nuova"

    Stiamo lavorando per stabilire criteri ben definiti per ogni sezione del nostro sito, e questo potrebbe essere soggetto a modifiche. Se avete domande sui nostri criteri, vi preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e non date per scontato che non abbiamo preso in considerazione qualcosa nel formulare le nostre raccomandazioni se non è elencato qui. Sono molti i fattori presi in considerazione e discussi quando consigliamo un progetto, e stiamo lavorando per documentare ogni singolo fattore.

- Deve essere open source.
- Deve ricevere aggiornamenti regolari.
- Deve supportare un'ampia varietà di hardware.
