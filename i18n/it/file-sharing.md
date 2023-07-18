---
title: "Condivisione e sincronizzazione dei file"
icon: material/share-variant
description: Scopri come condividere privatamente i tuoi file tra i tuoi dispositivi, con i tuoi amici e familiari, o in modo anonimo online.
cover: file-sharing.png
---

Scopri come condividere privatamente i tuoi file tra i tuoi dispositivi, con i tuoi amici e familiari, o in modo anonimo online.

## Condivisione di file

### Send

!!! recommendation

    ![Logo Send](assets/img/file-sharing-sync/send.svg){ align=right }
    
    **Send** è un fork del servizio Firefox Send di Mozilla, ormai dismesso, che consente di inviare file ad altri con un link. I file vengono crittografati sul dispositivo in modo da non poter essere letti dal server e possono essere protetti da password. Il manutentore di Send ospita una [istanza pubblica](https://send.vis.ee/). È possibile utilizzare altre istanze pubbliche o ospitare Send autonomamente.
    
    [:octicons-home-16: Pagina principale](https://send.vis.ee){ .md-button .md-button--primary }
    [:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="Istanze pubbliche"}
    [:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="Codice sorgente" }
    [:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title=Contribuisci }

Send può essere utilizzato tramite la sua interfaccia web o tramite la CLI [ffsend](https://github.com/timvisee/ffsend). Se hai familiarità con la riga di comando e invii spesso file, consigliamo di utilizzare il client CLI per evitare la crittografia basata su JavaScript. È possibile specificare il flag `--host` per utilizzare un server specifico:

```bash
ffsend upload --host https://send.vis.ee/ FILE
```

### OnionShare

!!! recommendation

    ![Logo di OnionShare](assets/img/file-sharing-sync/onionshare.svg){ align=right }
    
    **OnionShare** è uno strumento open-source che consente di condividere in modo sicuro e anonimo file di qualsiasi dimensione. Funziona avviando un server web accessibile come servizio Tor onion, con un URL inesplicabile che si può condividere con i destinatari per scaricare o inviare file.
    
    [:octicons-home-16: Pagina principale](https://onionshare.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="Servizio Onion" }
    [:octicons-info-16:](https://docs.onionshare.org){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="Codice sorgente" }
    
    ??? downloads "Scarica"
    
        - [:simple-windows11: Windows](https://onionshare.org/#download)
        - [:simple-apple: macOS](https://onionshare.org/#download)
        - [:simple-linux: Linux](https://onionshare.org/#download)

### Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

!!! esempio "Questa sezione è nuova"

    Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

- Non deve memorizzare i dati decriptati su un server remoto.
- Deve essere un software open-source.
- Deve avere client per Linux, macOS, e Windows; o avere un'interfaccia web.

## FreedomBox

!!! recommendation

    ![FreedomBox logo](assets/img/file-sharing-sync/freedombox.svg){ align=right }
    
    **FreedomBox** è un sistema operativo progettato per essere eseguito su un [single-board computer (SBC)](https://it.wikipedia.org/wiki/Single-board_computer). Lo scopo è quello di semplificare la configurazione delle applicazioni server per le quali si desidera il self-hosting.
    
    [:octicons-home-16: Pagina Principale](https://freedombox.org){ .md-button .md-button--primary }
    [:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title=Documentazione}
    [:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://freedomboxfoundation.org/donate/){ .card-link title=Contribuisci }

## Sincronizzazione dei file

### Nextcloud (Client-Server)

!!! recommendation

    ![Logo Nextcloud](assets/img/productivity/nextcloud.svg){ align=right }
    
    **Nextcloud** è una suite di software gratuiti e open-source client-server per la creazione di servizi di file hosting su un server privato controllato dall'utente.
    
    [:octicons-home-16: Pagina Principale](https://nextcloud.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://nextcloud.com/support/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://nextcloud.com/contribute/){ .card-link title=Contribuisci }
    
    ??? downloads "Scarica"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
        - [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
        - [:simple-windows11: Windows](https://nextcloud.com/install/#install-clients)
        - [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
        - [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

!!! danger "Attenzione"

    Sconsigliamo di utilizzare l'[App E2EE](https://apps.nextcloud.com/apps/end_to_end_encryption) per Nextcloud, in quanto potrebbe causare la perdita di dati; è altamente sperimentale e non soddisfa i criteri di qualità.

### Syncthing (P2P)

!!! recommendation

    ![Logo Syncthing](assets/img/file-sharing-sync/syncthing.svg){ align=right }
    
    **Syncthing** è un'utility open-source di sincronizzazione continua dei file peer-to-peer. Viene utilizzata per sincronizzare i file tra due o più dispositivi sulla rete locale o su Internet. Syncthing non utilizza alcun server centralizzato, ma il [Block Exchange Protocol](https://docs.syncthing.net/specs/bep-v1.html#bep-v1) per trasferire i dati tra i vari dispositivi. Tutti i dati sono criptati usando TLS.
    
    [:octicons-home-16: Pagina Principale](https://syncthing.net){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.syncthing.net){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/syncthing){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://syncthing.net/donations/){ .card-link title=Contribuisci }
    
    ??? downloads "Scarica"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nutomic.syncthingandroid)
        - [:simple-windows11: Windows](https://syncthing.net/downloads/)
        - [:simple-apple: macOS](https://syncthing.net/downloads/)
        - [:simple-linux: Linux](https://syncthing.net/downloads/)
        - [:simple-freebsd: FreeBSD](https://syncthing.net/downloads/)

### Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

!!! esempio "Questa sezione è nuova"

    Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

#### Requisiti minimi

- Non deve richiedere un server remoto/cloud di terze parti.
- Deve essere un software open-source.
- Deve avere client per Linux, macOS, e Windows; o avere un'interfaccia web.

#### Caso migliore

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. Le nostre raccomandazioni potrebbero non includere tutte o alcune di queste funzionalità, ma quelle che le includono potrebbero avere una posizione più alta rispetto ad altre in questa pagina.

- Dispone di client mobile per iOS e Android, che supportano almeno le anteprime dei documenti.
- Supporta il backup delle foto da iOS e Android e, opzionalmente, la sincronizzazione di file e cartelle su Android.
