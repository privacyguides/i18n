---
title: "Frontend"
icon: material/flip-to-front
description: Questi frontend open source per vari servizi Internet ti consentono di accedere ai contenuti senza JavaScript o altri disturbi.
cover: frontends.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Capitalismo di sorveglianza](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Talvolta, i servizi, proveranno a forzarti a iscriverti per un profilo, bloccando l'accesso ai contenuti con dei fastidiosi popup. Potrebbero anche corrompersi, se JavaScript è disabilitato. These frontends can allow you to circumvent these restrictions.

Se scegli di ospitare autonomamente tali frontend, è importante che tu disponga di altre persone che utilizzino la tua istanza, affinché tu possa confonderti. Dovresti stare attento a dove e come ospiti, poiché l'utilizzo di altre persone sarà collegato al tuo hosting.

When you are using an instance run by someone else, make sure to read the privacy policy of that specific instance (if available). Possono anche essere modificate dai proprietari e, dunque, potrebbero non riflettere la politica predefinita. Some instances have [Tor](tor.md) .onion addresses, which may grant some privacy as long as your search queries don't contain personally identifiable information.

## Reddit

### Redlib

<div class="admonition recommendation" markdown>

![Logo di Redlib](assets/img/frontends/redlib.svg){ align=right }

**Redlib** è un frontend open source per il sito web [Reddit](https://reddit.com) che è anche auto-ospitabile. You can access Redlib through a number of public instances.

[:octicons-repo-16: Repository](https://github.com/redlib-org/redlib){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/redlib-org/redlib-instances/blob/main/instances.md){ .card-link title="Public Instances" }
[:octicons-info-16:](https://github.com/redlib-org/redlib?tab=readme-ov-file#table-of-contents){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/redlib-org/redlib){ .card-link title="Source Code" }

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Nota</p>

Il sito web [Old Reddit](https://old.reddit.com) non richiede tanto JavaScript quanto il nuovo sito web di Reddit, ma ha recentemente bloccato l'accesso agli indirizzi IP riservati alle VPN pubbliche. Puoi utilizzare Old Reddit insieme a [Tor](tor.md) Onion che è stato [lanciato nell'ottobre 2022](https://forum.torproject.org/t/reddit-onion-service-launch/5305) su [https://old.reddittorjg6rue252oqsxryoxengawnmo46qy4kyii5wtqnwfj4ooad.onion](https://old.reddittorjg6rue252oqsxryoxengawnmo46qy4kyii5wtqnwfj4ooad.onion).

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Suggerimento</p>

Redlib è utile se desideri disabilitare JavaScript nel tuo browser, come [Tor Browser](tor.md#tor-browser) al livello di sicurezza "Il più sicuro".

</div>

## TikTok

### ProxiTok

<div class="admonition recommendation" markdown>

![Logo di ProxiTok](assets/img/frontends/proxitok.svg){ align=right }

**ProxiTok** è un frontend open source per il sito web [TikTok](https://tiktok.com) che è anche auto-ospitabile.

There are a number of public instances, with some that offer a [Tor](tor.md) onion service or an [I2P](alternative-networks.md#i2p-the-invisible-internet-project) eepsite.

[:octicons-repo-16: Repository](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Public Instances" }
[:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Source Code" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Suggerimento</p>

ProxiTok è utile se desideri disabilitare JavaScript nel tuo browser, come [Tor Browser](tor.md#tor-browser) al livello di sicurezza Più Sicuro.

</div>

## YouTube

**Note:** YouTube has gradually rolled out changes to its video player and API that have thwarted some of the methods used by third-party frontends for extracting YouTube data. If you experience reliability issues with one YouTube frontend, consider trying out another that uses a different extraction method.

### Invidious

<div class="admonition recommendation" markdown>

![Logo di Invidious](assets/img/frontends/invidious.svg#only-light){ align=right }
![Logo di Invidious](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }

**Invidious** è un frontend gratuito e open source per [YouTube](https://youtube.com), che puoi anche ospitare autonomamente.

There are a number of public instances, with some that offer a [Tor](tor.md) onion service or an [I2P](alternative-networks.md#i2p-the-invisible-internet-project) eepsite.

[:octicons-home-16: Homepage](https://invidious.io){ .md-button .md-button--primary }
[:octicons-server-16:](https://docs.invidious.io/instances){ .card-link title="Public Instances" }
[:octicons-info-16:](https://docs.invidious.io){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Source Code" }
[:octicons-heart-16:](https://invidious.io/donate){ .card-link title="Contribute" }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Invidious non esegue il proxy dei flussi video, di default. I video guardati tramite Invidious continueranno a generare delle connessioni dirette ai server Google (es. `googlevideo.com`); tuttavia, alcune istanze supportano il proxy del video. Basta abilitare *Video proxy* nelle impostazioni delle istanze, o aggiungere `&local=true` all'URL.

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Suggerimento</p>

Invidious è utile se desideri disabilitare JavaScript nel tuo browser, come [Tor Browser](tor.md#tor-browser) al livello di sicurezza Più Sicuro. Non fornisce di per sé la privacy, e sconsigliamo di accedere a qualsiasi profilo.

</div>

### Piped

<div class="admonition recommendation" markdown>

![Logo di Piped](assets/img/frontends/piped.svg){ align=right }

**Piped** è un frontend gratuito e open source per [YouTube](https://youtube.com), che è anche ospitabile autonomamente.

Piped richiede JavaScript per funzionare e dispone di numerose istanze pubbliche.

[:octicons-repo-16: Repository](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/TeamPiped/documentation/blob/main/content/docs/public-instances/index.md){ .card-link title="Public Instances" }
[:octicons-info-16:](https://docs.piped.video/docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title="Contribute" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Suggerimento</p>

Piped is useful if you want to use [SponsorBlock](https://sponsor.ajay.app) without installing an extension. Non fornisce di per sé la privacy, e sconsigliamo di accedere a qualsiasi profilo.

</div>

### FreeTube

<div class="admonition recommendation" markdown>

![Logo di FreeTube](assets/img/frontends/freetube.svg){ align=right }

**FreeTube** è un'applicazione desktop gratuita e open source per [YouTube](https://youtube.com). FreeTube extracts data from YouTube using its built-in API based on [YouTube.js](https://github.com/LuanRT/YouTube.js) or the [Invidious](#invidious) API. You can configure either as the default, with the other serving as a fallback.

When using FreeTube, your subscription list, playlists, watch history and search history are saved locally on your device.

[:octicons-home-16: Homepage](https://freetubeapp.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.freetubeapp.io){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://freetubeapp.io/#download)
- [:simple-apple: macOS](https://freetubeapp.io/#download)
- [:simple-linux: Linux](https://freetubeapp.io/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

When using FreeTube, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io), or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Considera l'utilizzo di una [VPN](vpn.md) o di [Tor](tor.md) se il tuo [modello di minaccia](basics/threat-modeling.md) richiede di nascondere il tuo indirizzo IP.

</div>

Di default, FreeTube blocca tutte le inserzioni di YouTube. In addition, FreeTube optionally integrates with [SponsorBlock](https://sponsor.ajay.app) to help you skip sponsored video segments.

### Yattee

<div class="admonition recommendation" markdown>

![Yattee logo](assets/img/frontends/yattee.svg){ align=right }

**Yattee** is a free and open-source privacy oriented video player for iOS, tvOS, and macOS for [YouTube](https://youtube.com). Due to App Store restrictions, you will need to take a few [extra steps](https://web.archive.org/web/20230330122839/https://gonzoknows.com/posts/Yattee) before you can use Yattee to watch YouTube. Yattee allows you to connect to instances of [Invidious](#invidious) or [Piped](#piped).

When using Yattee, your subscription list is saved locally on your device.

[:octicons-home-16: Homepage](https://github.com/yattee/yattee){ .md-button .md-button--primary }
[:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-apple: App Store](https://apps.apple.com/it/app/yattee/id1595136629)
- [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

When using Yattee, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances), or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Considera l'utilizzo di una [VPN](vpn.md) o di [Tor](tor.md) se il tuo [modello di minaccia](basics/threat-modeling.md) richiede di nascondere il tuo indirizzo IP.

</div>

Di default, Yattee blocca tutte le inserzioni di YouTube. Inoltre, Yattee integra facoltativamente [SponsorBlock](https://sponsor.ajay.app) per aiutarti a saltare i segmenti sponsorizzati dei video.

### LibreTube (Android)

<div class="admonition recommendation" markdown>

![Logo di LibreTube](assets/img/frontends/libretube.svg#only-light){ align=right }
![Logo di LibreTube](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }

**LibreTube** è un'applicazione Android gratuita e open source per [YouTube](https://youtube.com) che utilizza l'API di [Piped](#piped).

Il tuo elenco delle iscrizioni e le playlist sono salvate localmente sul tuo dispositivo Android.

[:octicons-home-16: Homepage](https://libretube.dev){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/libre-tube/LibreTube/blob/master/PRIVACY_POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://libretube.dev/#faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/libre-tube/LibreTube#donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

When using LibreTube, your IP address will be visible to YouTube, [Piped](https://github.com/TeamPiped/Piped/wiki/Instances), or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Considera l'utilizzo di una [VPN](vpn.md) o di [Tor](tor.md) se il tuo [modello di minaccia](basics/threat-modeling.md) richiede di nascondere il tuo indirizzo IP.

</div>

Di default, LibreTube blocca tutte le inserzioni di YouTube. Inoltre, LibreTube utilizza [SponsorBlock](https://sponsor.ajay.app) per aiutarti a saltare i segmenti video sponsorizzati. Puoi configurare interamente i tipi di segmenti che SponsorBlock salterà, o disabilitarli interamente. È inoltre presente un pulsante, sul lettore dei video stesso, per disabilitarlo per un video specifico, se desiderato.

### NewPipe (Android)

<div class="admonition recommendation annotate" markdown>

![NewPipe logo](assets/img/frontends/newpipe.svg){ align=right }

**NewPipe** is a free and open-source Android application for [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com), and [PeerTube](https://joinpeertube.org) (1).

Il tuo elenco delle iscrizioni e le playlist sono salvate localmente sul tuo dispositivo Android.

[:octicons-home-16: Homepage](https://newpipe.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://newpipe.net/FAQ){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Source Code" }
[:octicons-heart-16:](https://newpipe.net/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

</details>

</div>

1. The default instance is [FramaTube](https://framatube.org), however more can be added via **Settings** → **Content** → **PeerTube instances**.

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Utilizzando NewPipe, il tuo indirizzo IP sarà visibile ai fornitori di video utilizzati. Considera l'utilizzo di una [VPN](vpn.md) o di [Tor](tor.md) se il tuo [modello di minaccia](basics/threat-modeling.md) richiede di nascondere il tuo indirizzo IP.

</div>

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

Consideriamo i frontend solo se una delle seguenti condizioni è vera per una piattaforma:

- Normalmente accessibile solo con JavaScript abilitato.
- Normalmente accessibile solo con un account.
- Blocca l'accesso dalle [VPN](vpn.md) commerciali.

Frontend consigliati...

- Deve essere un software open source.
- Deve essere ospitabile autonomamente.
- Deve fornire tutte le funzionalità di base del sito web a utenti anonimi.
