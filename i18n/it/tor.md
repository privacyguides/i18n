---
meta_title: "Browser e Rete Tor: Navigazione Web Anonima - Privacy Guides"
title: "Tor Browser"
icon: simple/torbrowser
description: Proteggi la tua navigazione su Internet da occhi indiscreti, utilizzando la rete Tor, una rete sicura che elude la censura.
cover: tor.webp
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

<small>Protegge dalle seguenti minacce:</small>

- [:material-account-cash: Capitalismo di sorveglianza](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: Sorveglianza di massa](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Censura](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

**Tor** è un gruppo di server gestiti da volontari che consente di connettersi gratuitamente e di migliorare la propria privacy e sicurezza su Internet. Individui e organizzazioni possono inoltre condividere le informazioni tramite la rete Tor con i "servizi nascosti .onion", senza comprometterne la privacy. Poiché il traffico di Tor è difficile da bloccare e tracciare, è un efficace strumento di elusione della censura.

[Panoramica dettagliata di Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: Video: Perché hai bisogno di Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Suggerimento</p>

Prima di connetterti a Tor, ti preghiamo di assicurarti di aver letto la nostra [panoramica](advanced/tor-overview.md), su cos'è Tor e come connettersi a esso in modo sicuro. Spesso, consigliamo di connettersi a Tor tramite un [fornitore VPN](vpn.md) affidabile, ma devi farlo **adeguatamente** per evitare la riduzione del proprio anonimato.

</div>

Esistono diversi modi per connettersi alla rete Tor dal proprio dispositivo, il più utilizzato è il **Tor Browser**, un fork di Firefox progettato per la navigazione [:material-incognito: anonima ](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} per computer desktop e Android.

Alcune di queste app sono migliori di altre; la scelta dipende dal tuo modello di minaccia. Se sei un utente occasionale di Tor e non ti preoccupi che il tuo provider Internet raccolga prove contro di te, probabilmente va bene utilizzare un browser per dispositivi mobili come [Onion Browser](#onion-browser-ios) per accedere alla rete Tor. Incrementare il numero di persone che utilizzano Tor su una base giornaliera, aiuta a ridurre il cattivo stigma nei confronti di Tor, e riduce la qualità degli "elenchi di utenti di Tor", che gli ISP e i governi potrebbero compilare.

Se l'anonimato più completo è fondamentale per la tua situazione, dovresti utilizzare **soltanto** il client del Browser Tor per desktop, idealmente in una configurazione [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os). I browser mobile sono meno diffusi su Tor (di conseguenza, sono più facilmente rilevabili). Inoltre, altre configurazioni non sono testate in modo così rigoroso contro la de-anonimizzazione.

## Tor Browser

<div class="admonition recommendation" markdown>

![Logo di Tor Browser]assets/img/browsers/tor.svg{ align=right }

**Tor Browser** è la scelta migliore se hai bisogno di anonimato, poiché ti consente di accedere alla rete Tor e ai bridge, e include impostazioni e estensioni predefinite configurate automaticamente dai livelli di sicurezza predefiniti: *Standard*, *Sicuro* e *Il più sicuro*.

[:octicons-home-16: Pagina Principale](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Servizio Onion" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title="Documentazione" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title="Contribuisci" }

<details class="downloads" markdown>
<strong x-id="1">Scarica</strong>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:fontawesome-brands-windows: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Attenzione</p>

Non dovresti **mai** installare alcun'estensione aggiuntiva su Tor Browser o modificare le impostazioni di 'about:config', incluse quelle suggerite per Firefox. Le estensioni e le impostazioni non standard del browser, ti distinguono dagli altri sulla rete di Tor, rendendo il tuo browser più esposto al [fingerprint](https://support.torproject.org/it/glossary/browser-fingerprinting/).

</div>

Tor Browser è progettato per impedire il fingerprinting, o la tua identificazione secondo la configurazione del tuo browser. Pertanto, è imperativo **non** modificare il browser oltre i livelli di [sicurezza](https://tb-manual.torproject.org/security-settings) predefiniti. Quando modifichi il livello di sicurezza, **devi** sempre riavviare il browser prima di continuare a usarlo. In caso contrario, [le impostazioni di sicurezza potrebbero non essere applicate completamente](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), esponendoti a un rischio di fingerprinting e di exploit più elevato di quello previsto in base all'impostazione da te scelta.

Oltre a installare Tor Browser direttamente sul tuo computer, esistono inoltre dei sistemi operativi specificamente progettati per connettersi alla rete di Tor, come [Whonix](desktop.md#whonix) su [Qubes OS](desktop.md#qubes-os), che forniscono sicurezza e protezioni persino maggiori, rispetto al solo Tor Browser standard.

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Logo di Onion Browser](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** è un browser open-source che consente di navigare sul web in modo anonimo attraverso la rete Tor su dispositivi iOS ed è approvato dal [Tor Project](https://support.torproject.org/glossary/onion-browser).

[:material-star-box: Leggi la nostra ultima recensione su Onion Browser.](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review)

[:octicons-home-16: Pagina Principale](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Informativa Sulla Privacy" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title="Documentazione" }
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title="Contribuisci" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser non offre lo stesso livello di protezione della privacy rispetto a Tor Browser sulle piattaforme desktop. Per un uso occasionale è un modo perfettamente valido per accedere ai servizi nascosti, ma se sei preoccupato di essere tracciato o monitorato da avversari avanzati, non dovresti fare affidamento su di esso come strumento di anonimato.

È importante [notare](https://onionbrowser.com/faqs) che Onion Browser non **garantisce** che tutte le richieste passino attraverso Tor. Quando si utilizza la versione integrata di Tor, il tuo *vero indirizzo IP[trapelerà](alternative-networks.md#orbot) tramite WebRTC e flussi audio/video a causa delle limitazioni di WebKit. È *più sicuro* usare Onion Browser insieme a [Orbot](alternative-networks.md#orbot), ma ci sono comunque alcune limitazioni su iOS.</p>
