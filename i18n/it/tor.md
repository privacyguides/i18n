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

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Capitalismo di sorveglianza](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: Sorveglianza di massa](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Censura](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

**Tor** è un gruppo di server gestiti da volontari che consente di connettersi gratuitamente e di migliorare la propria privacy e sicurezza su Internet. Individui e organizzazioni possono inoltre condividere le informazioni tramite la rete Tor con i "servizi nascosti .onion", senza comprometterne la privacy. Poiché il traffico di Tor è difficile da bloccare e tracciare, è un efficace strumento di elusione della censura.

[Detailed Tor Overview :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: Video: Why You Need Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor/ ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Suggerimento</p>

Prima di connetterti a Tor, ti preghiamo di assicurarti di aver letto la nostra [panoramica](advanced/tor-overview.md), su cos'è Tor e come connettersi a esso in modo sicuro. Spesso, consigliamo di connettersi a Tor tramite un [fornitore VPN](vpn.md) affidabile, ma devi farlo **adeguatamente** per evitare la riduzione del proprio anonimato.

</div>

There are a variety of ways to connect to the Tor network from your device, the most commonly used being the **Tor Browser**, a fork of Firefox designed for [:material-incognito: anonymous](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} browsing for desktop computers and Android.

Alcune di queste app sono migliori di altre e, anche in questo caso, la scelta dipende dal proprio modello di minaccia. Se sei un utente casuale di Tor e non sei preoccupato dal fatto che il tuo ISP raccolga prove contro di te, utilizzare app come [Orbot](#orbot) o le app browser per mobile per accedere alla rete di Tor va probabilmente bene. Incrementare il numero di persone che utilizzano Tor su una base giornaliera, aiuta a ridurre il cattivo stigma nei confronti di Tor, e riduce la qualità degli "elenchi di utenti di Tor", che gli ISP e i governi potrebbero compilare.

Se l'anonimato più completo è fondamentale per la tua situazione, dovresti utilizzare **soltanto** il client del Browser Tor per desktop, idealmente in una configurazione [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os). Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

## Tor Browser

<div class="admonition recommendation" markdown>

![Logo di Tor Browser](assets/img/browsers/tor.svg){ align=right }

Il **Tor Browser** è la scelta ideale per l'anonimato, fornendoti accesso alla rete e ai ponti di Tor e include impostazioni ed estensioni predefinite, configurate automaticamente dai livelli di sicurezza predefiniti: *Standard*, *Safer* e *Safest*.

[:octicons-home-16: Homepage](https://torproject.org/it){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentazione }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Codice sorgente" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Downloads</summary>

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

Tor Browser è progettato per impedire il fingerprinting, o la tua identificazione secondo la configurazione del tuo browser. Pertanto, è imperativo **non** modificare il browser oltre i livelli di [sicurezza](https://tb-manual.torproject.org/security-settings) predefiniti.

Oltre a installare Tor Browser direttamente sul tuo computer, esistono inoltre dei sistemi operativi specificamente progettati per connettersi alla rete di Tor, come [Whonix](desktop.md#whonix) su [Qubes OS](desktop.md#qubes-os), che forniscono sicurezza e protezioni persino maggiori, rispetto al solo Tor Browser standard.

## Orbot

<div class="admonition recommendation" markdown>

![Logo di Orbot](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** è una VPN di Tor gratuita per smartphone, che instrada il traffico da qualsiasi app sul tuo dispositivo, tramite la rete di Tor.

[:octicons-home-16: Homepage](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Informativa sulla privacy" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentazione}
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Codice sorgente" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

</details>

</div>

Abbiamo precedentemente consiglito di abilitare la preferenza *Isola Indirizzo di Destinazione* nelle impostazioni di Orbot. Sebbene quest'impostazione possa teoricamente migliorare la privacy, imponendo l'utilizzo di un circuito differente per ogni indirizzo IP cui ti connetti, non fornisce un vantaggio pratico per gran parte delle applicazioni (specialmente per la navigazione web), può comportare una significativa riduzione delle prestazioni e incrementa il carico sulla rete di Tor. Non consigliamo più la regolazione di quest'impostazione dal suo valore predefinito, a meno che tu sappia che è necessario.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Suggerimenti per Android</p>

Orbot può delegare le singole app, se supportano il proxy SOCKS o HTTP. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN kill switch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

Orbot è spesso obsoleto sul [repository di F-Droid](https://guardianproject.info/fdroid) di Guardian Project e su [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android), quindi, piuttosto, cerca di scaricarlo direttamente dal [repository di GitHub](https://github.com/guardianproject/orbot/releases).

All versions are signed using the same signature, so they should be compatible with each other.

</div>

On iOS, Orbot has some limitations that could potentially cause crashes or leaks: iOS does not have an effective OS-level feature to block connections without a VPN like Android does, and iOS has an artificial memory limit for network extensions that makes it challenging to run Tor in Orbot without crashes. Currently, it is always safer to use Tor on a desktop computer compared to a mobile device.

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Logo di Onion Browser](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** è un browser open-source che consente di navigare sul web in modo anonimo attraverso la rete Tor su dispositivi iOS ed è approvato dal [Tor Project](https://support.torproject.org/glossary/onion-browser). [:material-star-box: Read our latest Onion Browser review.](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review/)

[:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser does not provide the same levels of privacy protections as Tor Browser does on desktop platforms. For casual use it is a perfectly fine way to access hidden services, but if you're concerned about being traced or monitored by advanced adversaries you should not rely on this as an anonymity tool.

[Notably](https://github.com/privacyguides/privacyguides.org/issues/2929), Onion Browser does not *guarantee* all requests go through Tor. When using the built-in version of Tor, [your real IP **will** be leaked via WebRTC and audio/video streams](https://onionbrowser.com/faqs) due to limitations of WebKit. It is *safer* to use Onion Browser alongside Orbot, but this still comes with some limitations on iOS (noted in the Orbot section above).

[^1]: L'impostazione `IsolateDestAddr` è discussa nella [mailing list Tor](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) e nella [documentazione Stream Isolation di Whonix](https://whonix.org/wiki/Stream_Isolation), dove entrambi i progetti suggeriscono che di solito non è un buon approccio per la maggior parte delle persone.
