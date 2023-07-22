---
title: "Frontend"
icon: material/flip-to-front
description: Questi frontend open-source per vari servizi Internet consentono di accedere ai vari contenuti senza utilizzare JavaScript o altri fastidi.
cover: frontends.png
---

A volte i servizi tentano di costringerti ad iscriverti ad un account bloccando l'accesso ai contenuti con fastidiosi popup. Potrebbero anche cessare di funzionare correttamente senza l'abilitazione di JavaScript. Questi frontend possono consentire di aggirare queste restrizioni.

Se scegli di fare self-hosting di questi frontend, è importante che anche altre persone utilizzino la vostra istanza per poterti integrare facilmente. Devi stare attento a dove e a come effettui l'hosting, poiché l'utilizzo da parte di altre persone sarà direttamente collegato al tuo hosting.

Quando utilizzi un'istanza gestita da altri, assicurati di leggere la politica sulla privacy di quella specifica istanza. Possono essere modificate dai loro proprietari e quindi potrebbero non rispecchiare la politica di default. Alcune istanze hanno indirizzi Tor .onion che possono garantire una certa privacy, a patto che le stringhe di ricerca non contengano PII (Personally Identifiable Information, Informazioni di Identificazione Personale).

## Twitter

### Nitter

!!! recommendation

    ![Nitter logo](assets/img/frontends/nitter.svg){ align=right }
    
    **Nitter** è un frontend gratuito e open-source per [Twitter](https://twitter.com) che permette anche il self-hosting.
    
    Esistono diverse istanze pubbliche, alcune delle quali supportano i servizi onion di [Tor](https://www.torproject.org).
    
    [:octicons-repo-16: Repository](https://github.com/zedeus/nitter){ .md-button .md-button--primary }
    [:octicons-server-16:](https://github.com/zedeus/nitter/wiki/Instances){ .card-link title="istanze pubbliche"}
    [:octicons-info-16:](https://github.com/zedeus/nitter/wiki){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/zedeus/nitter){ .card-link title="Codice sorgente" }
    [:octicons-heart-16:](https://github.com/zedeus/nitter#nitter){ .card-link title=Contribuisci}

!!! tip

    Nitter è utile se si desidera navigare tra i contenuti di Twitter senza dover effettuare il login e se si desidera disabilitare JavaScript nel browser, come nel caso di [Tor Browser](https://www.torproject.org/) al livello di sicurezza Molto Sicuro. Permette anche di [creare feed RSS per Twitter] (news-aggregators.md#twitter).

## TikTok

### ProxiTok

!!! recommendation

    ![Logo ProxiTok](assets/img/frontends/proxitok.svg){ align=right }
    
    **ProxiTok** è un frontend open source per il sito web [TikTok](https://www.tiktok.com) che permette il self-hosting.
    
    Esistono diverse istanze pubbliche, alcune delle quali supportano i servizi onion di [Tor](https://www.torproject.org).
    
    [:octicons-repo-16: Repository](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
    [:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Istanze pubbliche"}
    [:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Codice sorgente" }

!!! tip

    ProxiTok è utile se desideri disabilitare JavaScript nel browser, come ad esempio con [Tor Browser](https://www.torproject.org/) sul livello di sicurezza Molto Sicuro.

## YouTube

### FreeTube

!!! recommendation

    ![FreeTube logo](assets/img/frontends/freetube.svg){ align=right }
    
    **FreeTube** è un'applicazione desktop gratuita e open-source per [YouTube](https://youtube.com). Quando si utilizza FreeTube, l'elenco delle iscrizioni e le playlist vengono salvate localmente sul dispositivo.
    
    Per impostazione predefinita, FreeTube blocca tutti gli annunci pubblicitari di YouTube. Inoltre, è possibile integrare [SponsorBlock](https://sponsor.ajay.app) per saltare i segmenti sponsorizzati dei video.
    
    [:octicons-home-16: Pagina principale](https://freetubeapp.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Politica sulla privacy" }
    [:octicons-info-16:](https://docs.freetubeapp.io/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Codice sorgente" }
    [:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title=Contribuisci }
    
    ??? downloads "Scarica"
    
        - [:simple-windows11: Windows](https://freetubeapp.io/#download)
        - [:simple-apple: macOS](https://freetubeapp.io/#download)
        - [:simple-linux: Linux](https://freetubeapp.io/#download)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

!!! warning

    Quando utilizzi FreeTube, l'indirizzo IP potrebbe essere ancora noto a YouTube, [Invidious](https://instances.invidious.io) o [SponsorBlock](https://sponsor.ajay.app/) a seconda della configurazione. Considera l'uso di [VPN](vpn.md) o [Tor](https://www.torproject.org) se il [modello di minaccia](basics/threat-modeling.md) richiede di nascondere l'indirizzo IP.

### Yattee

!!! recommendation

    ![Logo Yattee](assets/img/frontends/yattee.svg){ align=right }
    
    **Yattee** è un lettore video gratuito e open-source orientato alla privacy per iOS, tvOS e macOS per [YouTube](https://youtube.com). Quando utilizzi Yattee, l'elenco delle iscrizioni viene salvato localmente sul tuo dispositivo.
    
    Prima di poter utilizzare Yattee per guardare YouTube, è necessario effettuare alcuni [passaggi extra](https://gonzoknows.com/posts/Yattee/), a causa delle restrizioni dell'App Store.
    
    [:octicons-home-16: Pagina Principale](https://github.com/yattee/yattee){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title=Contribuisci }
    
    ??? downloads "Scarica"
    
        - [:simple-apple: App Store](https://apps.apple.com/it/app/yattee/id1595136629)
        - [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

!!! warning

    Quando usi Yattee, l'indirizzo IP potrebbe essere ancora visibile a YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) o [SponsorBlock](https://sponsor.ajay.app/) a seconda della tua configurazione. Considera l'uso di [VPN](vpn.md) o [Tor](https://www.torproject.org) se il [modello di minaccia](basics/threat-modeling.md) richiede di nascondere l'indirizzo IP.

Per impostazione predefinita, Yattee blocca tutti gli annunci pubblicitari di YouTube. Inoltre, Yattee si integra opzionalmente con [SponsorBlock](https://sponsor.ajay.app) per aiutarvi a saltare i segmenti video sponsorizzati.

### LibreTube (Android)

!!! recommendation

    ![Logo LibreTube](assets/img/frontends/libretube.svg#only-light){ align=right }
    ![Logo LibreTube](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }
    
    **LibreTube** è un'applicazione Android gratuita e open source per [YouTube](https://youtube.com) che utilizza l'API [Piped](#piped).
    
    LibreTube consente di memorizzare la lista delle iscrizioni e le playlist in locale sul dispositivo Android o su un account dell'istanza Piped scelta, in modo da potervi accedere senza problemi anche su altri dispositivi.
    
    [:octicons-home-16: Pagina Principale](https://libre-tube.github.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/libre-tube/LibreTube#privacy-policy-and-disclaimer){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://github.com/libre-tube/LibreTube#readme){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Codice Sorgente" }
    
    ??? downloads "Scarica"
    
        - [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

!!! warning

    Quando usi LibreTube, il tuo indirizzo IP sarà visibile all'istanza [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) scelta e/o [SponsorBlock](https://sponsor.ajay.app/) a seconda della configurazione. Considera l'uso di [VPN](vpn.md) o [Tor](https://www.torproject.org) se il [modello di minaccia](basics/threat-modeling.md) richiede di nascondere l'indirizzo IP.

Per impostazione predefinita, LibreTube blocca tutti gli annunci pubblicitari di YouTube. Inoltre, Libretube utilizza [SponsorBlock](https://sponsor.ajay.app) per aiutarvi a saltare i segmenti video sponsorizzati. Sei libero di configurare i tipi di segmenti che SponsorBlock salterà, oppure puoi disabilitarlo completamente. È presente anche un pulsante sul lettore video per disabilitarlo per un video specifico, se vuoi.

### NewPipe (Android)

!!! recommendation annotate

    ![Newpipe logo](assets/img/frontends/newpipe.svg){ align=right }
    
    **NewPipe** è un'applicazione Android gratuita e open-source per [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com) e [PeerTube](https://joinpeertube.org/) (1).
    
    L'elenco delle iscrizioni e delle playlist viene salvato localmente sul dispositivo Android.
    
    [:octicons-home-16: Pagina principale](https://newpipe.net){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Politica sulla privacy" }
    [:octicons-info-16:](https://teamnewpipe.github.io/documentation/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Codice sorgente" }
    [:octicons-heart-16:](https://newpipe.net/donate/){ .card-link title=Contribuisci }
    
    ??? downloads "Scarica"
    
        - [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

1. L'istanza predefinita è [FramaTube](https://framatube.org/), ma se ne possono aggiungere altre tramite **Impostazioni** → **Contenuti** → **Istanze di PeerTube**

!!! warning

    Quando utilizzi NewPipe, il tuo indirizzo IP sarà visibile ai fornitori di video utilizzati. Considera l'uso di [VPN](vpn.md) o [Tor](https://www.torproject.org) se il [modello di minaccia](basics/threat-modeling.md) richiede di nascondere l'indirizzo IP.

### Invidious

!!! recommendation

    ![Invidious logo](assets/img/frontends/invidious.svg#only-light){ align=right }
    ![Invidious logo](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }
    
    **Invidious** è un frontend gratuito e open-source per [YouTube](https://youtube.com) che permette anche il self-hosting.
    
    Esistono diverse istanze pubbliche, alcune delle quali supportano i servizi onion di [Tor](https://www.torproject.org).
    
    [:octicons-home-16: Pagina Principale](https://invidious.io){ .md-button .md-button--primary }
    [:octicons-server-16:](https://instances.invidious.io){ .card-link title="Istanze pubbliche"}
    [:octicons-info-16:](https://docs.invidious.io/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Codice sorgente" }
    [:octicons-heart-16:](https://invidious.io/donate/){ .card-link title=Contribuisci }

!!! warning

    Invidious non esegue il proxy dei video in modo predefinito. I video guardati attraverso Invidious continueranno a collegarsi direttamente ai server di Google (ad esempio, `googlevideo.com`); tuttavia, alcune istanze supportano il proxy video: è sufficiente attivare *Proxy video* nelle impostazioni dell'istanza o aggiungere `&local=true` all'URL.

!!! tip

    Invidious è utile se si desidera disabilitare JavaScript nel browser, ad esempio [Tor Browser](https://www.torproject.org/) al livello di sicurezza Molto Sicuro. Non garantisce di per sé la privacy e non consigliamo di accedere ad alcun account.

### Piped

!!! recommendation

    ![Piped logo](assets/img/frontends/piped.svg){ align=right }
    
    **Piped** è un frontend gratuito e open-source per [YouTube](https://youtube.com) che permette anche il self-hosting.
    
    Piped richiede JavaScript per funzionare e ci sono diverse istanze pubbliche.
    
    [:octicons-repo-16: Repository](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
    [:octicons-server-16:](https://piped.kavin.rocks/preferences#ddlInstanceSelection){ .card-link title="Istanze pubbliche"}
    [:octicons-info-16:](https://piped-docs.kavin.rocks/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Codice sorgente" }
    [:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title=Contribuisci }

!!! tip

    Piped è utile se si vuole utilizzare [SponsorBlock](https://sponsor.ajay.app) senza installare un'estensione o se si vuole accedere a contenuti con limiti d'età senza un account. Non garantisce di per sé la privacy e non consigliamo di accedere ad alcun account.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

!!! esempio "Questa sezione è nuova"

    Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

Frontend consigliati...

- Deve essere un software open-source.
- Deve essere auto-ostabile.
- Deve fornire tutte le funzionalità di base del sito web disponibili per gli utenti anonimi.

Prendiamo in considerazione solo frontend per siti web che sono...

- Non accessibili normalmente senza JavaScript.
