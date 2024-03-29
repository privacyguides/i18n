---
title: "Frontend"
icon: material/flip-to-front
description: Questi frontend open source per vari servizi Internet ti consentono di accedere ai contenuti senza JavaScript o altri disturbi.
cover: frontends.webp
---

Talvolta, i servizi, proveranno a forzarti a iscriverti per un profilo, bloccando l'accesso ai contenuti con dei fastidiosi popup. Potrebbero anche corrompersi, se JavaScript è disabilitato. Questi frontend possono consentirti di aggirare queste restrizioni.

Se scegli di ospitare autonomamente tali frontend, è importante che tu disponga di altre persone che utilizzino la tua istanza, affinché tu possa confonderti. Dovresti stare attento a dove e come ospiti, poiché l'utilizzo di altre persone sarà collegato al tuo hosting.

Utilizzando un'istanza gestita da altri, assicurati di leggere la politica sulla privacy di quell'istanza nello specifico. Possono anche essere modificate dai proprietari e, dunque, potrebbero non riflettere la politica predefinita. Alcune istanze dispongono di indirizzi .onion di [Tor](tor.md), che potrebbero garantire della privacy, finché le tue richieste di ricerca non contengono PII.

## TikTok

### ProxiTok

<div class="admonition recommendation" markdown>

![ProxiTok logo](assets/img/frontends/proxitok.svg){ align=right }

**ProxiTok** is an open-source frontend to the [TikTok](https://tiktok.com) website that is also self-hostable.

Esistono numerose istanze pubbliche, alcune dotate del supporto ai servizi onion di [Tor](tor.md).

[:octicons-repo-16: Repository](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Istanze Pubbliche"}
[:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Codice Sorgente" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Suggerimento</p>

ProxiTok è utile se desideri disabilitare JavaScript nel tuo browser, come [Tor Browser](tor.md#tor-browser) al livello di sicurezza Più Sicuro.

</div>

## YouTube

### FreeTube

<div class="admonition recommendation" markdown>

![Logo di FreeTube](assets/img/frontends/freetube.svg){ align=right }

**FreeTube** è un'applicazione desktop gratuita e open source per [YouTube](https://youtube.com). Utilizzando FreeTube, il tuo elenco di iscrizioni e playlist è salvato localmente sul tuo dispositivo.

Di default, FreeTube blocca tutte le inserzioni di YouTube. Inoltre, FreeTube integra facoltativamente [SponsorBlock](https://sponsor.ajay.app), per aiutarti a saltare i segmenti sponsorizzati dei video.

[:octicons-home-16: Homepage](https://freetubeapp.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.freetubeapp.io){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Download</summary>

- [:simple-windows11: Windows](https://freetubeapp.io/#download)
- [:simple-apple: macOS](https://freetubeapp.io/#download)
- [:simple-linux: Linux](https://freetubeapp.io/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

When using FreeTube, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io) or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Considera di utilizzare una [VPN](vpn.md) o [Tor](tor.md), se il tuo [modello di minaccia](basics/threat-modeling.md) ti richiede di mascherare l'indirizzo IP.

</div>

### Yattee

<div class="admonition recommendation" markdown>

![Logo di Yattee](assets/img/frontends/yattee.svg){ align=right }

**Yattee** è un lettore video gratuito e open source orientato alla privacy per iOS, tvOS e macOS per [YouTube](https://youtube.com). Utilizzando Yattee, il tuo elenco di iscrizioni è salvato localmente sul tuo dispositivo.

You will need to take a few [extra steps](https://gonzoknows.com/posts/Yattee) before you can use Yattee to watch YouTube, due to App Store restrictions.

[:octicons-home-16: Pagina Home](https://github.com/yattee/yattee){ .md-button .md-button--primary }
[:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Politica sulla privacy" }
[:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Codiice sorgente" }
[:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-apple: App Store](https://apps.apple.com/app/id1595136629)
- [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

When using Yattee, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Considera di utilizzare una [VPN](vpn.md) o [Tor](tor.md), se il tuo [modello di minaccia](basics/threat-modeling.md) ti richiede di mascherare l'indirizzo IP.

</div>

Di default, Yattee blocca tutte le inserzioni di YouTube. Inoltre, Yattee integra facoltativamente [SponsorBlock](https://sponsor.ajay.app) per aiutarti a saltare i segmenti sponsorizzati dei video.

### LibreTube (Android)

<div class="admonition recommendation" markdown>

![Logo di LibreTube](assets/img/frontends/libretube.svg#only-light){ align=right }
![Logo di LibreTube](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }

**LibreTube** è un'applicazione Android gratuita e open source per [YouTube](https://youtube.com) che utilizza l'API di [Piped](#piped).

LibreTube ti consente di memorizzare il tuo elenco di iscrizioni e playlist localmente sul tuo dispositivo Android, o su un profilo sulla tua istanza di Piped di scelta, che ti consente di accedervi senza problemi, anche su altri dispositivi.

[:octicons-home-16: Pagina Home](https://libre-tube.github.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/libre-tube/LibreTube#privacy-policy-and-disclaimer){ .card-link title="Politica sulla privacy" }
[:octicons-info-16:](https://github.com/libre-tube/LibreTube#readme){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Download</summary>

- [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

When using LibreTube, your IP address will be visible to the [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) instance you choose and/or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Considera di utilizzare una [VPN](vpn.md) o [Tor](tor.md), se il tuo [modello di minaccia](basics/threat-modeling.md) ti richiede di mascherare l'indirizzo IP.

</div>

Di default, LibreTube blocca tutte le inserzioni di YouTube. Inoltre, Libretube utilizza [SponsorBlock](https://sponsor.ajay.app) per aiutarti a saltare i segmenti sponsorizzati dei video. Puoi configurare interamente i tipi di segmenti che SponsorBlock salterà, o disabilitarli interamente. È inoltre presente un pulsante, sul lettore dei video stesso, per disabilitarlo per un video specifico, se desiderato.

### NewPipe (Android)

<div class="admonition recommendation annotate" markdown>

![Newpipe logo](assets/img/frontends/newpipe.svg){ align=right }

**NewPipe** is a free and open-source Android application for [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com), and [PeerTube](https://joinpeertube.org) (1).

Il tuo elenco delle iscrizioni e le playlist sono salvate localmente sul tuo dispositivo Android.

[:octicons-home-16: Homepage](https://newpipe.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://teamnewpipe.github.io/documentation){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Source Code" }
[:octicons-heart-16:](https://newpipe.net/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Download</summary>

- [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

</details>

</div>

1. The default instance is [FramaTube](https://framatube.org), however more can be added via **Settings** → **Content** → **PeerTube instances**

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Utilizzando NewPipe, il tuo indirizzo IP sarà visibile ai fornitori di video utilizzati. Considera di utilizzare una [VPN](vpn.md) o [Tor](tor.md), se il tuo [modello di minaccia](basics/threat-modeling.md) ti richiede di mascherare l'indirizzo IP.

</div>

### Invidious

<div class="admonition recommendation" markdown>

![Logo di Invidious](assets/img/frontends/invidious.svg#only-light){ align=right }
![Logo di Invidious](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }

**Invidious** è un frontend gratuito e open source per [YouTube](https://youtube.com), che puoi anche ospitare autonomamente.

Esistono numerose istanze pubbliche, alcune dotate del supporto ai servizi onion di [Tor](tor.md).

[:octicons-home-16: Homepage](https://invidious.io){ .md-button .md-button--primary }
[:octicons-server-16:](https://instances.invidious.io){ .card-link title="Public Instances"}
[:octicons-info-16:](https://docs.invidious.io){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Source Code" }
[:octicons-heart-16:](https://invidious.io/donate){ .card-link title=Contribute }

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
[:octicons-server-16:](https://piped.kavin.rocks/preferences#ddlInstanceSelection){ .card-link title="Public Instances"}
[:octicons-info-16:](https://piped-docs.kavin.rocks){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title=Contribute }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Suggerimento</p>

Piped è utile se desideri utilizzare [SponsorBlock](https://sponsor.ajay.app) senza installare un'estensione o per accedere a contenuti con limiti d'età senza un profilo. Non fornisce di per sé la privacy, e sconsigliamo di accedere a qualsiasi profilo.

</div>

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

<div class="admonition example" markdown>
<p class="admonition-title">Questa sezione è nuova</p>

Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

</div>

Frontend consigliati...

- Deve essere un software open source.
- Deve essere ospitabile autonomamente.
- Deve fornire tutte le funzionalità di base del sito web a utenti anonimi.

Consideriamo soltanto i frontend per i siti web che...

- Normalmente è accessibile solo con JavaScript abilitato.
