---
meta_title: "Browser e Rete Tor: Navigazione Web Anonima - Privacy Guides"
title: "Rete Tor"
icon: simple/torproject
description: Proteggi la tua navigazione su Internet da occhi indiscreti, utilizzando la rete Tor, una rete sicura che elude la censura.
cover: tor.png
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
    image: /assets/img/browsers/tor.svg
    url: https://www.torproject.org/it/
    sameAs: https://it.wikipedia.org/wiki/Tor_(software)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
---

![Logo di Tor](assets/img/self-contained-networks/tor.svg){ align=right }

La rete di **Tor** è un gruppo di server gestiti da volontari che ti consente di connettert gratuitamente e migliora la tua privacy e sicurezza su Internet. Individui e organizzazioni possono inoltre condividere le informazioni tramite la rete Tor con i "servizi nascosti .onion", senza comprometterne la privacy. Poiché il traffico di Tor è difficile da bloccare e tracciare, è un efficace strumento di elusione della censura.

[:octicons-home-16:](https://www.torproject.org){ .card-link title="Pagina principale" }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Servizio Onion" }
[:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Documentazione}
[:octicons-code-16:](https://gitweb.torproject.org/tor.git){ .card-link title="Codice sorgente" }
[:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribuisci }

Tor funziona instradando il traffico tramite questi server gestiti da volontari, invece di effettuare una connessione diretta al sito che stai provando a visitare. Ciò offusca la provenienza del traffico e nessun server nel percorso di connesione riesce a visualizzare il percorso completo della provenienza e destinazione del traffico, a significare che nemmeno i server utilizzati per connettersi, possono violarne l'anonimato.

[Panoramica dettagliata di Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Connessione a Tor

Esistono svariati modi per connettersi alla rete di Tor dal tuo dispositivo, il più comunemente utilizzato dei quali è **Tor Browser**, una biforcazione di Firefox progettata per la navigazione anonima per i computer desktop e per Android. Oltre alle seguenti app, esistono inoltre dei sistemi operativi progettati specificamente per connettersi alla rete di Tor, come [Whonix](desktop.md#whonix) su [Qubes OS](desktop.md#qubes-os), che forniscono sicurezza e protezioni persino maggiori del Tor Browser standard.

### Tor Browser

!!! recommendation

    ![Logo di Tor Browser](assets/img/browsers/tor.svg){ align=right }
    
    Il **Tor Browser** è la scelta ideale per l'anonimato, fornendoti accesso alla rete e ai ponti di Tor e include impostazioni ed estensioni predefinite, configurate automaticamente dai livelli di sicurezza predefiniti: *Standard*, *Safer* e *Safest*.
    
    [:octicons-home-16: Homepage](https://www.torproject.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
    [:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Documentation }
    [:octicons-code-16:](https://gitweb.torproject.org/tor-browser.git/){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }
    
    ??? download
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
        - [:simple-android: Android](https://www.torproject.org/download/#android)
        - [:simple-windows11: Windows](https://www.torproject.org/download/)
        - [:simple-apple: macOS](https://www.torproject.org/download/)
        - [:simple-linux: Linux](https://www.torproject.org/download/)

!!! danger

    Non dovresti **mai** installare alcun'estensione aggiuntiva su Tor Browser o modificare le impostazioni di 'about:config', incluse quelle suggerite per Firefox. Le estensioni e impostazioni non standard del browser, ti distinguono dagli altri sulla rete di Tor, rendendo il tuo browser più esposto al [fingerprinting](https://support.torproject.org/glossary/browser-fingerprinting).

Tor Browser è progettato per impedire il fingerprinting, o la tua identificazione secondo la configurazione del tuo browser. Dunque, è indispensabile che tu **non** modifichi il browser oltre ai [livelli di sicurezza](https://tb-manual.torproject.org/security-settings/) predefiniti.

### Orbot

!!! recommendation

    ![Logo di Orbot](assets/img/self-contained-networks/orbot.svg){ align=right }
    
    **Orbot** è una VPN di Tor gratuita per smartphone, che instrada il traffico da qualsiasi app sul tuo dispositivo, tramite la rete di Tor.
    
    [:octicons-home-16: Homepage](https://orbot.app/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
    [:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribute }
    
    ??? download
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/orbot/id1609461599)
        - [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

Abbiamo precedentemente consiglito di abilitare la preferenza *Isola Indirizzo di Destinazione* nelle impostazioni di Orbot. Sebbene quest'impostazione possa teoricamente migliorare la privacy, imponendo l'utilizzo di un circuito differente per ogni indirizzo IP cui ti connetti, non fornisce un vantaggio pratico per gran parte delle applicazioni (specialmente per la navigazione web), può comportare una significativa riduzione delle prestazioni e incrementa il carico sulla rete di Tor. Non consigliamo più la regolazione di quest'impostazione dal suo valore predefinito, a meno che non sia necessario.[^1]

!!! tip "Consigli per Android"

    Orbot può delegare le singole app, se supportano il proxy SOCKS o HTTP. Inoltre, può delegare tutte le tue connessioni di rete utilizzando [VpnService](https://developer.android.com/reference/android/net/VpnService) ed è utilizzabile con l'interruttore di emergenza della VPN in :gear: **Impostazioni** → **Rete e Internet** → **VPN** → :gear: → **Blocca connessioni senza VPN**.
    
    Orbot è spesso obsoleto sulla [repository di F-Droid](https://guardianproject.info/fdroid) di Guardian Project e su [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android), quindi, piuttosto, considera di scaricarlo direttamente dalla [repository di GitHub](https://github.com/guardianproject/orbot/releases).
    
    Tutte le versioni sono firmate utilizzando la medesima firma, quindi, dovrebbero essere compatibili tra loro.

## Relay e Bridge

### Snowflake

!!! recommendation

    ![Logo di Snowflake](assets/img/browsers/snowflake.svg#only-light){ align=right }
    ![Logo di Snowflake](assets/img/browsers/snowflake-dark.svg#only-dark){ align=right }
    
    **Snowflake** ti consente di donare larghezza di banda a Tor Project, operando un "proxy di Snowflake" nel tuo browser.
    
    Gli individui sottoposti a censura possono utilizzare i proxy di Snowflake per connettersi alla rete di Tor. Snowflake è un ottimo modo per contribuire alla rete, anche senza le conoscenze tecniche per eseguire un relé o ponte di Tor.
    
    [:octicons-home-16: Homepage](https://snowflake.torproject.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitweb.torproject.org/pluggable-transports/snowflake.git/){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }

Puoi abilitare Snowflake nel tuo browser aprendolo in un'altra scheda e attivando l'interruttore. Puoi lasciarlo in esecuzione in background mentre navighi per contribuire alla tua connessione. Sconsigliamo di installare Snowflake come un'estensione del browser; aggiungere estensioni di terze parti può incrementare la superficie di attacco.

[Esegui Snowflake nel tuo browser :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html ""){.md-button}

Snowflake non incrementa la tua privacy in alcun modo, né è utilizzato per connettersi alla rete di Tor sul tuo browser personale. Tuttavia, se la tua connessione a Internet non è censurata, dovresti considerarne l'esecuzione per aiutare le persone su reti sottoposte a censura ad ottenere un migliore privacy. Non è necessario preoccuparsi di quali siti web siano acceduti dalle persone tramite il tuo proxy: il loro indirizzo IP di navigazione visibile corrisponderà al loro nodo d'uscita di Tor, non al tuo.

L'esecuzione di un proxy di Snowflake è a basso rischio, persino di più della gestione di un relé o ponte di Tor, che già non sono attività particolarmente rischiose. Tuttavia, comunque, delega il traffico attraverso la tua rete, il che può avere un certo impatto, specialmente se la rete ha una larghezza di banda limitata. Assicurati di comprendere [il funzionamento di Snowflake](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) prima di decidere se gestire un proxy.

[^1]: L'impostazione `IsolateDestAddr` è discussa nella [mailing list di Tor](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) e nella [documentazione sull'Isolamento del Flusso di Whonix](https://www.whonix.org/wiki/Stream_Isolation), dove entrambi i progetti suggeriscono che, di solito, non è un buon approccio per la maggior parte delle persone.
