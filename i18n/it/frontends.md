---
title: "Frontend"
icon: material/flip-to-front
description: Questi frontend open source per vari servizi Internet ti consentono di accedere ai contenuti senza JavaScript o altri disturbi.
cover: frontends.webp
---

Talvolta, i servizi, proveranno a forzarti a iscriverti per un profilo, bloccando l'accesso ai contenuti con dei fastidiosi popup. Potrebbero anche corrompersi, se JavaScript è disabilitato. Questi frontend possono consentirti di aggirare queste restrizioni.

Se scegli di ospitare autonomamente tali frontend, è importante che tu disponga di altre persone che utilizzino la tua istanza, affinché tu possa confonderti. Dovresti stare attento a dove e come ospiti, poiché l'utilizzo di altre persone sarà collegato al tuo hosting.

Utilizzando un'istanza gestita da altri, assicurati di leggere la politica sulla privacy di quell'istanza nello specifico. Possono anche essere modificate dai proprietari e, dunque, potrebbero non riflettere la politica predefinita. Alcune istanze dispongono di indirizzi .onion di [Tor](tor.md), che potrebbero garantire della privacy, finché le tue richieste di ricerca non contengono PII.

## Reddit

### Redlib

<div class="admonition recommendation" markdown>

![Logo di Redlib](assets/img/frontends/redlib.svg){ align=right }

**Redlib** è un frontend open source per il sito web [Reddit](https://reddit.com) che è anche auto-ospitabile.

Esistono numerose istanze pubbliche, alcune dotate del supporto ai servizi onion di [Tor](tor.md).

[:octicons-repo-16: Repository](https://github.com/redlib-org/redlib){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/redlib-org/redlib-instances/blob/main/instances.md){ .card-link title="Istanze Pubbliche"}
[:octicons-info-16:](https://github.com/redlib-org/redlib?tab=readme-ov-file#table-of-contents){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/redlib-org/redlib){ .card-link title="Codice Sorgente" }

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

[:octicons-home-16: Pagina Principale](https://freetubeapp.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://docs.freetubeapp.io){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-windows11: Windows](https://freetubeapp.io/#download)
- [:simple-apple: macOS](https://freetubeapp.io/#download)
- [:simple-linux: Linux](https://freetubeapp.io/#download)
- [:simple-flathub: Flathub](https://flathub.org/it/apps/io.freetubeapp.FreeTube)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Quando utilizzi FreeTube, il tuo indirizzo IP potrebbe essere ancora noto a YouTube, [Invidious](https://instances.invidious.io) o [SponsorBlock](https://sponsor.ajay.app) a seconda della tua configurazione. Considera l'utilizzo di una [VPN](vpn.md) o di [Tor](tor.md) se il tuo [modello di minaccia](basics/threat-modeling.md) richiede di nascondere il tuo indirizzo IP.

</div>

### Yattee

<div class="admonition recommendation" markdown>

![Logo di Yattee](assets/img/frontends/yattee.svg){ align=right }

**Yattee** è un lettore video gratuito e open source orientato alla privacy per iOS, tvOS e macOS per [YouTube](https://youtube.com). Utilizzando Yattee, il tuo elenco di iscrizioni è salvato localmente sul tuo dispositivo.

Dovrai effettuare alcuni [passaggi aggiuntivi](https://gonzoknows.com/posts/Yattee) prima di poter utilizzare Yattee per guardare YouTube, per via delle restrizioni dell'App Store.

[:octicons-home-16: Pagina Principale](https://github.com/yattee/yattee){ .md-button .md-button--primary }
[:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Codiice Sorgente" }
[:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-apple: App Store](https://apps.apple.com/it/app/yattee/id1595136629)
- [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Quando utilizzi Yattee, il tuo indirizzo IP potrebbe essere ancora noto a YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) o [SponsorBlock](https://sponsor.ajay.app) a seconda della tua configurazione. Considera l'utilizzo di una [VPN](vpn.md) o di [Tor](tor.md) se il tuo [modello di minaccia](basics/threat-modeling.md) richiede di nascondere il tuo indirizzo IP.

</div>

Di default, Yattee blocca tutte le inserzioni di YouTube. Inoltre, Yattee integra facoltativamente [SponsorBlock](https://sponsor.ajay.app) per aiutarti a saltare i segmenti sponsorizzati dei video.

### LibreTube (Android)

<div class="admonition recommendation" markdown>

![Logo di LibreTube](assets/img/frontends/libretube.svg#only-light){ align=right }
![Logo di LibreTube](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }

**LibreTube** è un'applicazione Android gratuita e open source per [YouTube](https://youtube.com) che utilizza l'API di [Piped](#piped).

LibreTube ti consente di memorizzare il tuo elenco di iscrizioni e playlist localmente sul tuo dispositivo Android, o su un profilo sulla tua istanza di Piped di scelta, che ti consente di accedervi senza problemi, anche su altri dispositivi.

[:octicons-home-16: Pagina Principale](https://libretube.dev){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/libre-tube/LibreTube/blob/master/PRIVACY_POLICY.md){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://libretube.dev/#faq){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://github.com/libre-tube/LibreTube#donate){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Quando utilizzi LibreTube, il tuo indirizzo IP sarà visibile all'istanza [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) da te scelta e/o [SponsorBlock](https://sponsor.ajay.app) a seconda della tua configurazione. Considera l'utilizzo di una [VPN](vpn.md) o di [Tor](tor.md) se il tuo [modello di minaccia](basics/threat-modeling.md) richiede di nascondere il tuo indirizzo IP.

</div>

Di default, LibreTube blocca tutte le inserzioni di YouTube. Inoltre, LibreTube utilizza [SponsorBlock](https://sponsor.ajay.app) per aiutarti a saltare i segmenti video sponsorizzati. Puoi configurare interamente i tipi di segmenti che SponsorBlock salterà, o disabilitarli interamente. È inoltre presente un pulsante, sul lettore dei video stesso, per disabilitarlo per un video specifico, se desiderato.

### NewPipe (Android)

<div class="admonition recommendation annotate" markdown>

![Logo di Newpipe](assets/img/frontends/newpipe.svg){ align=right }

**NewPipe** è un'applicazione Android gratuita e open source per [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com) e [PeerTube](https://joinpeertube.org/it) (1).

Il tuo elenco delle iscrizioni e le playlist sono salvate localmente sul tuo dispositivo Android.

[:octicons-home-16: Pagina Principale](https://newpipe.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://newpipe.net/FAQ){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://newpipe.net/donate){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

</details>

</div>

1. L'istanza predefinita è [FramaTube](https://framatube.org), ma se ne possono aggiungere altre tramite **Impostazioni** → **Contenuto** → **Istanze PeerTube**

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Utilizzando NewPipe, il tuo indirizzo IP sarà visibile ai fornitori di video utilizzati. Considera l'utilizzo di una [VPN](vpn.md) o di [Tor](tor.md) se il tuo [modello di minaccia](basics/threat-modeling.md) richiede di nascondere il tuo indirizzo IP.

</div>

### Invidious

<div class="admonition recommendation" markdown>

![Logo di Invidious](assets/img/frontends/invidious.svg#only-light){ align=right }
![Logo di Invidious](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }

**Invidious** è un frontend gratuito e open source per [YouTube](https://youtube.com), che puoi anche ospitare autonomamente.

Esistono numerose istanze pubbliche, alcune dotate del supporto ai servizi onion di [Tor](tor.md).

[:octicons-home-16: Pagina Principale](https://invidious.io){ .md-button .md-button--primary }
[:octicons-server-16:](https://instances.invidious.io){ .card-link title="Istanze Pubbliche"}
[:octicons-info-16:](https://docs.invidious.io){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://invidious.io/donate){ .card-link title=Contribuisci }

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
[:octicons-server-16:](https://github.com/TeamPiped/Piped/wiki/Instances){ .card-link title="Istanze Pubbliche"}
[:octicons-info-16:](https://docs.piped.video/docs){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title=Contribuisci }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Suggerimento</p>

Piped è utile se desideri utilizzare [SponsorBlock](https://sponsor.ajay.app) senza installare un'estensione o per accedere a contenuti con limiti d'età senza un profilo. Non fornisce di per sé la privacy, e sconsigliamo di accedere a qualsiasi profilo.

</div>

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

Frontend consigliati...

- Deve essere un software open source.
- Deve essere ospitabile autonomamente.
- Deve fornire tutte le funzionalità di base del sito web a utenti anonimi.

Consideriamo i frontend solo se una delle seguenti condizioni è vera per una piattaforma:

- Normalmente accessibile solo con JavaScript abilitato.
- Normalmente accessibile solo con un account.
- Blocca l'accesso dalle [VPN](vpn.md) commerciali.
