---
meta_title: "Browser e Rete Tor: Navigazione Web Anonima - Privacy Guides"
title: "Rete Tor"
icon: simple/torproject
description: Proteggi la tua navigazione su Internet da occhi indiscreti, utilizzando la rete Tor, una rete sicura che elude la censura.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
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

La rete di **Tor** è un gruppo di server gestiti da volontari che ti consente di connetterti gratuitamente e migliora la tua privacy e sicurezza su Internet. Individui e organizzazioni possono inoltre condividere le informazioni tramite la rete Tor con i "servizi nascosti .onion", senza comprometterne la privacy. Poiché il traffico di Tor è difficile da bloccare e tracciare, è un efficace strumento di elusione della censura.

[:octicons-home-16:](https://torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

Tor funziona instradando il traffico tramite questi server gestiti da volontari, invece di effettuare una connessione diretta al sito che stai provando a visitare. In questo modo si offusca la provenienza del traffico e nessun server nel percorso di connessione è in grado di vedere il percorso completo del traffico proveniente e diretto, il che significa che nemmeno i server utilizzati per connettersi possono violare l'anonimato.

[Panoramica dettagliata di Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Connessione a Tor

<div class="admonition tip" markdown>
<p class="admonition-title">Suggerimento</p>

Prima di connetterti a Tor, ti preghiamo di assicurarti di aver letto la nostra [panoramica](advanced/tor-overview.md), su cos'è Tor e come connettersi a esso in modo sicuro. Spesso, consigliamo di connettersi a Tor tramite un [fornitore VPN](vpn.md) affidabile, ma devi farlo **adeguatamente** per evitare la riduzione del proprio anonimato.

</div>

Esistono svariati modi per connettersi alla rete di Tor dal tuo dispositivo, il più comunemente utilizzato dei quali è **Tor Browser**, una biforcazione di Firefox progettata per la navigazione anonima per i computer desktop e per Android.

Alcune di queste app sono migliori di altre e, anche in questo caso, la scelta dipende dal proprio modello di minaccia. Se sei un utente casuale di Tor e non sei preoccupato dal fatto che il tuo ISP raccolga prove contro di te, utilizzare app come [Orbot](#orbot) o le app browser per mobile per accedere alla rete di Tor va probabilmente bene. Incrementare il numero di persone che utilizzano Tor su una base giornaliera, aiuta a ridurre il cattivo stigma nei confronti di Tor, e riduce la qualità degli "elenchi di utenti di Tor", che gli ISP e i governi potrebbero compilare.

Se l'anonimato più completo è fondamentale per la tua situazione, dovresti utilizzare **soltanto** il client del Browser Tor per desktop, idealmente in una configurazione [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os). I browser per mobile sono meno comuni su Tor (e, di conseguenza, più rilevabili), e altre configurazioni non sono altrrettanto testate contro la deanonimizzazione.

### Tor Browser

<div class="admonition recommendation" markdown>

![Logo di Tor Browser](assets/img/browsers/tor.svg){ align=right }

Il **Tor Browser** è la scelta ideale per l'anonimato, fornendoti accesso alla rete e ai ponti di Tor e include impostazioni ed estensioni predefinite, configurate automaticamente dai livelli di sicurezza predefiniti: *Standard*, *Safer* e *Safest*.

[:octicons-home-16: Homepage](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:simple-windows11: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Attenzione</p>

Non dovresti **mai** installare alcun'estensione aggiuntiva su Tor Browser o modificare le impostazioni di 'about:config', incluse quelle suggerite per Firefox. Le estensioni e le impostazioni non standard del browser, ti distinguono dagli altri sulla rete di Tor, rendendo il tuo browser più esposto al [fingerprint](https://support.torproject.org/it/glossary/browser-fingerprinting/).

</div>

Tor Browser è progettato per impedire il fingerprinting, o la tua identificazione secondo la configurazione del tuo browser. Therefore, it is imperative that you do **not** modify the browser beyond the default [security levels](https://tb-manual.torproject.org/security-settings).

Oltre a installare Tor Browser direttamente sul tuo computer, esistono inoltre dei sistemi operativi specificamente progettati per connettersi alla rete di Tor, come [Whonix](desktop.md#whonix) su [Qubes OS](desktop.md#qubes-os), che forniscono sicurezza e protezioni persino maggiori, rispetto al solo Tor Browser standard.

### Orbot

<div class="admonition recommendation" markdown>

![Logo di Orbot](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** è una VPN di Tor gratuita per smartphone, che instrada il traffico da qualsiasi app sul tuo dispositivo, tramite la rete di Tor.

[:octicons-home-16: Homepage](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

</details>

</div>

Abbiamo precedentemente consiglito di abilitare la preferenza *Isola Indirizzo di Destinazione* nelle impostazioni di Orbot. Sebbene quest'impostazione possa teoricamente migliorare la privacy, imponendo l'utilizzo di un circuito differente per ogni indirizzo IP cui ti connetti, non fornisce un vantaggio pratico per gran parte delle applicazioni (specialmente per la navigazione web), può comportare una significativa riduzione delle prestazioni e incrementa il carico sulla rete di Tor. Non consigliamo più la regolazione di quest'impostazione dal suo valore predefinito, a meno che non sia necessario.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Suggerimenti per Android</p>

Orbot può delegare le singole app, se supportano il proxy SOCKS o HTTP. Può anche effettuare il proxy di tutte le connessioni di rete utilizzando [VpnService](https://developer.android.com/reference/android/net/VpnService) e può essere utilizzato con il killswitch VPN in :gear: **Impostazioni** → **Rete & Internet** → **VPN** → :gear: → **Blocca connessioni senza VPN**.

Orbot è spesso obsoleto sul [repository di F-Droid](https://guardianproject.info/fdroid) di Guardian Project e su [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android), quindi, piuttosto, cerca di scaricarlo direttamente dal [repository di GitHub](https://github.com/guardianproject/orbot/releases).

Tutte le versioni sono firmate utilizzando la medesima firma, quindi, dovrebbero essere compatibili tra loro.

</div>

### Onion Browser

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** is an open-source browser that lets you browse the web anonymously over the Tor network on iOS devices and is endorsed by the [Tor Project](https://support.torproject.org/glossary/onion-browser).

[:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Codice sorgente" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

## Relay e Bridge

### Snowflake

<div class="admonition recommendation" markdown>

![Logo di Snowflake](assets/img/browsers/snowflake.svg#only-light){ align=right }
![Logo di Snowflake](assets/img/browsers/snowflake-dark.svg#only-dark){ align=right }

**Snowflake** ti consente di donare larghezza di banda a Tor Project, operando un "proxy di Snowflake" nel tuo browser.

Gli individui sottoposti a censura possono utilizzare i proxy di Snowflake per connettersi alla rete di Tor. Snowflake è un ottimo modo per contribuire alla rete, anche senza le conoscenze tecniche per eseguire un relé o ponte di Tor.

[:octicons-home-16: Homepage](https://snowflake.torproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

</details>

</div>

Puoi abilitare Snowflake nel tuo browser aprendolo in un'altra scheda e attivando l'interruttore. Puoi lasciarlo in esecuzione in background mentre navighi per contribuire alla tua connessione. Sconsigliamo di installare Snowflake come un'estensione del browser; aggiungere estensioni di terze parti può incrementare la superficie di attacco.

[Esegui Snowflake nel tuo browser :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html ""){.md-button}

Snowflake non incrementa la tua privacy in alcun modo, né è utilizzato per connettersi alla rete di Tor sul tuo browser personale. Tuttavia, se la tua connessione a Internet non è censurata, dovresti considerarne l'esecuzione per aiutare le persone su reti sottoposte a censura ad ottenere un migliore privacy. Non è necessario preoccuparsi di quali siti web siano acceduti dalle persone tramite il tuo proxy: il loro indirizzo IP di navigazione visibile corrisponderà al loro nodo d'uscita di Tor, non al tuo.

L'esecuzione di un proxy di Snowflake è a basso rischio, persino di più della gestione di un relé o ponte di Tor, che già non sono attività particolarmente rischiose. Tuttavia, comunque, delega il traffico attraverso la tua rete, il che può avere un certo impatto, specialmente se la rete ha una larghezza di banda limitata. Assicurati di comprendere [il funzionamento di Snowflake](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) prima di decidere se gestire un proxy.

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) and [Whonix's Stream Isolation documentation](https://whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
