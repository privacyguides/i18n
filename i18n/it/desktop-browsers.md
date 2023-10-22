---
meta_title: "Browser web che rispettano la privacy per PC e Mac - Privacy Guides"
title: "Browser desktop"
icon: material/laptop
description: Questi browser web offrono una maggiore protezione della privacy rispetto a Google Chrome.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Browser desktop privati consigliati
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/it/browser
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Firefox
    image: /assets/img/browsers/firefox.svg
    url: https://firefox.com
    sameAs: https://it.wikipedia.org/wiki/Mozilla_Firefox
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    sameAs: https://it.wikipedia.org/wiki/Brave_(browser)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

Questi sono al momento i browser web consigliati per desktop e configurazioni per la navigazione standard e non anonima. Consigliamo [Mullvad Browser](#mullvad-browser) se sei interessato a una forte protezione della privacy e all'anti-fingerprinting pronti all'uso, [Firefox](#firefox) per i navigatori occasionali di Internet alla ricerca di una buona alternativa a Google Chrome e [Brave](#brave), se necessiti della compatibilità del browser con Chromium.

Invece, se necessiti di navigare anonimamente su Internet, dovresti utilizzare [Tor](tor.md). In questa pagina forniamo alcune raccomandazioni sulla configurazione, ma tutti i browser diversi da Tor Browser saranno rintracciabili da *qualcuno* in un modo o nell'altro.

## Mullvad Browser

!!! recommendation

    ![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    **Mullvad Browser** è una versione di [Tor Browser](tor.md#tor-browser) con le integrazioni della rete Tor rimosse, con l'obiettivo di fornire le tecnologie anti-fingerprinting di Tor Browser agli utenti che usano una VPN. Sviluppato dal Tor Project e distribuito da [Mullvad](vpn.md#mullvad), **non** richiede l'utilizzo della VPN di Mullvad.
    
    [:octicons-home-16: Home Page](https://mullvad.net/it/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/it/help/privacy-policy/){ .card-link title="Informativa sulla privacy" }
    [:octicons-info-16:](https://mullvad.net/it/help/tag/mullvad-browser/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Codice sorgente" }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://mullvad.net/it/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/it/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/it/download/browser/linux)

Come [Tor Browser](tor.md), Mullvad Browser è progettato per impedire il fingerprinting, rendendo l'impronta digitale del tuo browser identica a quella di tutti gli altri suoi utenti, e include impostazioni ed estensioni predefinite, configurate automaticamente dai livelli di sicurezza predefiniti: *Standard*, *Safer* e *Safest*. Dunque, è essenziale che tu non modifichi affatto il browser, tranne che per regolare i [livelli di sicurezza](https://tb-manual.torproject.org/security-settings/) predefiniti. Altre modifiche renderebbero la tua impronta digitale univoca, vanificando lo scopo di utilizzare tale browser. Se desideri configurare il tuo browser in modo più completo e il fingerprinting non ti preoccupa, consigliamo invece [Firefox](#firefox).

### Anti-Fingerprinting

**Senza** utilizzare una [VPN](vpn.md), Mullvad Browser fornisce le stesse protezioni dai [semplici script di fingerprinting](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) di altri browser privati, come Firefox+[Arkenfox](#arkenfox-advanced) o [Brave](#brave). Mullvad Browser fornisce tali protezioni "pronte all'uso", a scapito di una certa flessibilità e comodità che altri browser privati possono fornire.

==Per la massima protezione anti-fingerprinting, consigliamo di utilizzare Mullvad Browser **con** una VPN==, che sia di Mullvad o di un altro fornitore di VPN consigliato. Utilizzando una VPN con Mullvad Browser, condividi un'impronta digitale e un gruppo di indirizzi IP con molti altri utenti, offrendoti una "folla" con cui confonderti. Questa strategia è l'unico modo per contrastare gli script di tracciamento avanzati ed è la stessa tecnica anti-fingerprinting utilizzata da Tor Browser.

Nota che, sebbene tu possa utilizzare Mullvad Browser con qualsiasi fornitore VPN, altre persone su tale VPN devono anch'esse utilizzare Mullvad Browser affinché tale "folla" esista, il che è molto più probabile su Mullvad VPN, rispetto ad altri fornitori, in particolare così a breve distanza dal lancio di Mullvad Browser. Mullvad Browser non dispone di connettività VPN integrata, né verifica che tu stia utilizzando una VPN prima di navigare; la tua connessione VPN dev'essere configurata e gestita separatamente.

Mullvad Browser contiene le estensioni pre-installate di *uBlock Origin* e *NoScript*. Sebbene, di norma, [sconsigliamo](#extensions) l'aggiunta di *ulteriori* estensioni del browser, queste estensioni pre-installate **non** dovrebbero essere rimosse o configurate al di fuori dei valori predefiniti, poiché ciò renderebbe l'impronta digitale del tuo browser sensibilmente distinta da quella di altri utenti di Mullvad Browser. Inoltre, presenta l'Estensione Mullvad Browser pre-installata, che *può* essere rimossa in sicurezza, senza influenzare l'impronta digitale del tuo browser, se lo desideri, ma è anche sicura da mantenere se non utilizzi la VPN di Mullvad.

### Modalità di Navigazione Privata

Mullvad Browser opera in modalità di navigazione privata permanente, ciò significa che la tua cronologia, cookie e altri dati dei siti saranno eliminati a ogni chiusura del browser. I tuoi segnalibri, le impostazioni del browser e dell'estensione saranno comunque conservati.

Ciò è necessario per impedire forme avanzate di tracciamento, a costo della comodità e di alcune funzionalità di Firefox, come i Contenitori Multi Profilo. Ricordati che puoi sempre utilizzare più browser, ad esempio, potresti considerare di utilizzare Firefox+Arkenfox per alcuni siti cui desideri rimanere connesso o, altrimenti, che non operano adeguatamente su Mullvad Browser, e Mullvad Browser per la navigazione generale.

### Mullvad Leta

Mullvad Browser integra DuckDuckGo come [motore di ricerca](search-engines.md) predefinito, ma include anche **Mullvad Leta**, un motore di ricerca che richiede un abbonamento attivo alla VPN di Mullvad, per potervi accedere. Mullvad Leta utilizza direttamente l'API di ricerca a pagamento di Google (motivo per cui è limitato agli abbonati), tuttavia, a causa di tale limitazione, è possibile per Mullvad correlare le ricerche e i profili VPN di Mullvad. Per questo motivo sconsigliamo l'uso di Mullvad Leta, anche se Mullvad raccoglie pochissime informazioni sui propri abbonati alla VPN.

## Firefox

!!! recommendation

    ![Firefox logo](assets/img/browsers/firefox.svg){ align=right }
    
    **Firefox** offre robuste impostazioni di privacy, come la [protezione antitracciamento avanzata](https://support.mozilla.org/it/kb/protezione-antitracciamento-avanzata-firefox-desktop), che aiuta a bloccare varie [tipologie di tracciamento](https://support.mozilla.org/it/kb/protezione-antitracciamento-avanzata-firefox-desktop#w_che-cosa-viene-bloccato-con-la-protezione-antitracciamento-avanzata).
    
    [:octicons-home-16: Home page](https://www.mozilla.org/it/firefox/new){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mozilla.org/it/privacy/firefox/){ .card-link title="Informativa sulla Privacy" }
    [:octicons-info-16:](https://firefox-source-docs.mozilla.org/){ .card-link title=Documentatione}
    [:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://donate.mozilla.org/it/){ .card-link title=Contribuisci }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://www.mozilla.org/firefox/windows)
        - [:simple-apple: macOS](https://www.mozilla.org/firefox/mac)
        - [:simple-linux: Linux](https://www.mozilla.org/firefox/linux)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

!!! attenzione
    Firefox include un [token di download](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) univoco nei scaricati dal sito web di Mozilla e utilizza la telemetria su Firefox per inviarlo. Il token **non** è incluso nelle release da [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

### Configurazione Consigliata

Queste opzioni si possono trovare in :material-menu: → **Impostazioni**

#### Ricerca

- [ ] Disabilita **Visualizza suggerimenti di ricerca**

Le funzionalità di suggerimento di ricerca potrebbero non essere disponibili nella tua regione.

I suggerimenti di ricerca inviano qualsiasi cosa tu digiti nella barra degli indirizzi al motore di ricerca predefinito, indipendentemente dal fatto che tu invii una ricerca effettiva. Disabilitare i suggerimenti di ricerca ti consente di controllare più precisamente quali dati invii al fornitore del tuo motore di ricerca.

#### Privacy e sicurezza

##### Protezione antitracciamento avanzata

- [x] Seleziona Protezione antitracciamento avanzata **Restrittiva**

Questo ti protegge bloccando i tracciatori dei social, gli script di fingerprinting (nota che non ti protegge da *tutto* il fingerprinting), cryptominer, cookie di tracciamento dei tra siti e alcuni altri contenuti di tracciamento. La Protezione antitracciamento avanzata protegge da molte minacce comuni, ma non blocca tutte le vie di tracciamento, poiché è progettata per avere un impatto minimo o zero sull'utilizzabilità del sito.

##### Firefox Suggest (solo USA)

[Firefox Suggest](https://support.mozilla.org/en-US/kb/firefox-suggest) è una funzionalità simile ai suggerimenti di ricerca, disponibile soltanto negli USA. Consigliamo di disabilitarla per le stesse motivazioni per cui consigliamo di disabilitare i suggerimenti di ricerca. Se non vedi queste opzioni sotto l'intestazione della **Barra degli Indirizzi**, non disponi della nuova esperienza e puoi ignorare tali modifiche.

- [ ] Rimuovi la spunta **Suggestions from the web**
- [ ] Rimuovi la spunta da **Suggestions from sponsors**

##### Eliminazione alla Chiusura

Se desideri mantenere la connessione a siti in particolare, puoi consentire le eccezioni in **Cookie e Dati dei Siti** → **Gestisci Eccezioni...**

- [x] Spunta **Elimina cookie e dati dei siti web alla chiusura di Firefox**

Ciò ti protegge dai cookie persistenti, ma non dai cookie acquisiti durante qualsiasi singola sessione di navigazione. Quando tale opzione è abilitata, diventa possibile pulire facilmente i cookie del tuo browser, semplicemente riavviando Firefox. Puoi impostare delle eccezioni a seconda del sito, se desideri rimanere connesso a un sito in particolare, che visiti spesso.

##### Telemetria

- [ ] Rimuovi la spunta da **Consenti a Firefox di inviare a Mozilla dati tecnici e relativi all’interazione con il browser**
- [ ] Rimuovi la spunta da **Consenti a Firefox di installare e condurre studi**
- [ ] Rimuovi la spunta da **Consenti a Firefox di inviare segnalazioni di arresto anomalo in sospeso**

> Firefox ci invia i dati sulla tua versione e lingua di Firefox; sistema operativo del dispositivo e configurazione hardware; memoria, informazioni essenziali su arresti anomali ed errori; risultati di processi automatizzati quali aggiornamenti, navigazione sicura e attivazione. Quando Firefox ci invia i dati, il tuo indirizzo IP è raccolto temporaneamente come parte dei registri del nostro server.

Inoltre, il servizio Firefox Accounts raccoglie [alcuni dati tecnici](https://www.mozilla.org/en-US/privacy/firefox/#firefox-accounts). Se utilizzi un Profilo di Firefox, puoi disattivarlo:

1. Apri le [impostazioni del tuo profilo su accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Deseleziona ** Raccolta e utilizzo dati ** > **Aiutaci a migliorare gli ⁨account Firefox⁩**

##### Modalità solo HTTPS

- [x] Seleziona **Attiva in tutte le finestre**

Ciò previene che ti connetta involontariamente a un sito web in HTTP semplice. I siti senza HTTPS sono poco comuni oggigiorno, quindi, ciò dovrebbe avere un impatto minimo o zero sulla tua navigazione quotidiana.

##### DNS su HTTPS

Se utilizzi un [fornitore di DNS su HTTPS](dns.md):

- [x] Seleziona **Protezione massima** e scegli un fornitore adatto

La Protezione Massima impone l'utilizzo di DNS su HTTPS; un avviso di sicurezza apparirà se Firefox non riesce a connettersi al tuo risolutore DNS sicuro, o se il tuo risolutore DNS sicuro dice che i registri per il dominio cui stai provando ad acceedere, non esistono. Ciò impedisce alla rete cui sei connesso, di ridurre segretameente la sicurezza del tuo DNS.

#### Sincronizzazione

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) consente ai tuoi dati di navigazione (cronologia, segnalibri, etc.) di essere accessibili su tutti i tuoi dispositivi e di proteggerli con E2EE.

### Arkenfox (avanzato)

!!! consiglio "Utilizza Mullvad Browser per l'anti-fingerprinting avanzato"

    [Mullvad Browser](#mullvad-browser) fornisce le stesse protezioni anti-fingerprinting di Arkenfox pronte all'uso e non richiede l'utilizzo della VPN di Mullvad per beneficiarne. Insieme a una VPN, Mullvad Browser può contrastare gli script di tracciamento più avanzati, a differenza di Arkenfox. Tuttavia, Arkenfox presenta il vantaggio di essere molto più flessibile e di consentire eccezioni specifiche per i siti web a cui necessiti di rimanere connesso.

Il [progetto Arkenfox](https://github.com/arkenfox/user.js) fornisce una serie di opzioni attentamente selezionate per Firefox. Se [decidi](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) di utilizzarlo, [alcune opzioni](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) sono soggettivamente più stringenti di altre e/o potrrebbero causare il malfunzionamento di alcuni siti web, [che puoi modificare facilmente](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) affinché si adeguino alle tue esigenze. **Consigliamo vivamente** di leggere la loro [wiki](https://github.com/arkenfox/user.js/wiki) completa. Inoltre, Arkenfox consente il supporto ai [contenitori](https://support.mozilla.org/en-US/kb/containers#w_for-advanced-users).

Arkenfox mira soltanto a contrastare gli script di tracciamento di base o semplici, tramite la casualizzazione dei canva e le impostazioni di configurazione della resistenza al fingerprint integrata di Firefox. Non mira a confondere il tuo browser con una grande folla di altri utenti di Arkenfox come Mullvad Browser o Tor Browser, che è il solo modo per contrastare gli script di tracciamento di fingerprint avanzati. Ricordati che puoi sempre utilizzare più browser, ad esempio, potresti considerare di utilizzare Firefox+Arkenfox per alcuni siti cui desideri rimanere connesso o, altrimenti fidarti, e Mullvad Browser per la navigazione generale.

## Brave

!!! recommendation

    ![Brave logo](assets/img/browsers/brave.svg){ align=right }
    
    **Brave Browser** include un blocco di contenuti integrato e delle [funzionalità per la privacy](https://brave.com/privacy-features/), molte delle quali sono abilitate di default.
    
    Brave è basato sul progetto del browser web di Chromium, quindi, dovrebbe risultare familiare e avere problemi minimi di compatibilità con i siti web.
    
    [:octicons-home-16: Home page](https://brave.com/it/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Servizio Onion" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Informativa sulla Privacy" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Codice Sorgente" }
    
    ??? downloads annotate
    
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
        - [:simple-windows11: Windows](https://brave.com/it/download/)
        - [:simple-apple: macOS](https://brave.com/it/download/)
        - [:simple-linux: Linux](https://brave.com/linux/) (1)

    1. Sconsigliamo di utilizzare la versione Flatpak di Brave, poiché sostituisce il sandbox di Chromium con Flatpak, che è meno efficace. Inoltre, il pacchetto non è mantenuto da Brave Software, Inc.

### Configurazione Consigliata

Queste opzioni si possono trovare in :material-menu: → **Impostazioni**.

#### Impostazioni

##### Shields

Brave include alcune misure contro il fingerprinting nella sua funzionalità [Protezioni](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-). Consigliamo di configurarle [globalmente](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) tra tutte le pagine che visiti.

Le opzioni di Protezioni sono regolabili per ogni sito ma consigliamo di impostarle di default come segue:

<div class="annotate" markdown>

- [x] Seleziona **Impedisci ai siti di tracciarmi in base alle mie preferenze linguistiche**
- [x] Seleziona **Aggressivo** in Blocco di tracker e annunci

    ??? attenzione "Utilizza elenchi di filtraggio predefiniti"
        Brave ti consente di selezionare ulteriori filtri dei contenuti sulla pagina interna `brave://adblock`. Sconsigliamo questa funzionalità; piuttosto, mantieni gli elenchi di filtri predefiniti. Utilzzare ulteriori elenchi ti distinguerà dagli altri utenti di Brave e potrebbe inoltre incrementare la superficie di attacco, se è presente un exploit su Brave e una regola dannosa viene aggiunta a uno degli elenchi che utilizzi.

- [x] Seleziona **Restrittivo** in **Aggiorna le connessioni a HTTPS**
- [x] (Opzionale) Seleziona **Blocco degli script** (1)
- [x] Seleziona **Rigido, potrebbe non far funzionare alcuni siti** in Blocca il fingerprinting

</div>

1. Quest'opzione fornisce una funzionalità simile alle [modalità di blocco](https://github.com/gorhill/uBlock/wiki/Blocking-mode) avanzate di uBlock Origin o all'estensione [NoScript](https://noscript.net/).

##### Blocco social

- [ ] Rimuovi la spunta da tutti i componenti social

##### Privacy e sicurezza

<div class="annotate" markdown>

- [x] Seleziona **Disabilita UDP senza proxy** in [Gestione politica IP WebRTC](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Rimuovi la spunta da **Utilizza i servizi Google per la messaggistica push**
- [ ] Rimuovi la spunta da **Acconsenti all'analisi dei prodotti di tutela della privacy (P3A).**
- [ ] Rimuovi la spunta da **Invia automaticamente un ping di utilizzo giornaliero a Brave**
- [ ] Rimuovi la spunta da **Invia automaticamente i rapporti di diagnostica**
- [ ] Rimuovi la spunta da **Finestra in Incognito con Tor** (1)

    !!! tip "Pulizia alla chiusura"

        - [x] Selezionare **Cancella i cookie e i dati del sito alla chiusura di tutte le finestre** nel menu *Cookies e altri dati del sito*

        Se si desidera rimanere connessi a un particolare sito che si visita spesso, è possibile impostare eccezioni su base individuale nella sezione *Comportamenti personalizzati*.

</div>

1. Brave **non è** resistente al fingerprinting come il Tor Browser e molte meno persone utilizzano Brave con Tor, facendoti quindi distinguere. Quando [è necessario un forte anonimato](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-) utilizza [Tor Browser](tor.md#tor-browser).

##### Estensioni

Disabilita le estensioni integrate che non utilizzi in **Estensioni**

- [ ] Rimuovi la spunta da **Hangouts**
- [ ] Rimuovi la spunta da **WebTorrent**

##### Web3

Le funzionalità Web3 di Brave possono potenzialmente aumentare il fingerprint del browser e la superficie di attacco. Disattiva le funzioni, a meno che tu non le utilizzi.

- Seleziona **Estensioni (nessun backup)** sotto Wallet Ethereum predefinito e Wallet Solana predefinito
- Imposta **Metodo per risolvere le risorse IPFS ** su **Disabilitato**

##### Sistema

<div class="annotate" markdown>

- [ ] Disabilita **Continua a eseguire applicazioni in background dopo la chiusura di Brave** per disabilitare le applicazioni in background (1)

</div>

1. Questa opzione non è presente su tutte le piattaforme.

#### Sincronizzazione

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) consente ai tuoi dati di navigazione (cronologia, segnalibri, etc.) di essere accessibili su tutti i tuoi dispositivi, senza richiedere un profilo e li protegge con E2EE.

#### Ricompense e Portafoglio di Brave

**Brave Rewards** ti consente di ricevere la criptovaluta Basic Attention Token (BAT) per l'esecuzione di certe azioni su Brave. Si affida a un conto custodiale e KYC da un dato numero di fornitori. Sconsigliamo BAT come [criptovaluta privata](cryptocurrency.md), né consigliamo l'utilizzo di un [portafoglio di custodia](advanced/payments.md#other-coins-bitcoin-ethereum-etc), qundi ne scoraggeremo l'utiliizzo.

**Brave Wallet** opera localmente sul tuo computer, ma non supporta alcuna criptovaluta privata, quindi, scoraggiamo l'utilizzo di questa funzione.

## Risorse Aggiuntive

In generale, consigliamo di mantenere al minimo le estensioni del tuo browser per ridurre la tua superficie di attacco; hanno un accesso privilegiato sul tuo browser, ti richiedono di fidarti dello svilupptore, possono [distinguerti](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint) e [indebolire](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) l'isolamento del sito. Tuttavia, uBlock Origin potrebbe rivelarsi utile se apprezzi la funzionalità di blocco dei contenuti.

### uBlock Origin

!!! recommendation

    ![Logo di uBlock Origin](assets/img/browsers/ublock_origin.svg){ align=right }
    
    **uBlock Origin** è un popolare blocco di contenuti che potrebbe aiutarti a bloccare annunci, tracciatori e script di fingerprinting.
    
    [:octicons-repo-16: Repository](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Politica sulla privacy" }
    [:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Codice sorgente" }
    
    ??? downloads
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

Suggeriamo di seguire la [documentazione per sviluppatori](https://github.com/gorhill/uBlock/wiki/Blocking-mode) e di selezionare una delle "modalità". Ulteriori elenchi di filtri possono influenzare le prestazioni e [potrebbero incrementare la superficie di attacco](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

##### Altri elenchi

Ecco alcuni altri [elenchi di filtri](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) che potresti voler considerare di aggiungere:

- [x] Spunta **Privacy** > **AdGuard URL Tracking Protection**
- Aggiungi [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcuno dei progetti consigliati.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questi elenchi, prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta migliore per te.

!!! esempio "Questa sezione è nuova"

    Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

### Requisiti minimi

- Dev'essere un software open source.
- Supporta gli aggiornamenti automatici.
- Riceve gli aggiornamenti del motore in 0-1 giorni dal rilascio a monte.
- È disponibile su Linux, macOS e Windows.
- Qualsiasi modifica necessaria per rendere il browser più rispettoso della privacy non dovrebbe influenzare negativamente l'esperienza degli utenti.
- Blocca i cookie di terze parti di default.
- Supporta la [partizione dello stato](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) per mitigare il tracciamento tra siti.[^1]

### Miglior Caso

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere alcuna o tutte queste funzionalità, ma quelli che le presentano, potrebbero essere meglio classificati di altri su questa pagina.

- Include una funzionalità di blocco dei contenuti integrati.
- Supporta la compartimentazione dei cookie (come nei [Contenitori a Profilo Multiplo](https://support.mozilla.org/en-US/kb/containers)).
- Supporta le App Web Progressiive.  
  PWA ti consente di installare certi siti web come fossero app native sul tuo computer. Ciò può comportare vantaggi rispetto all'installazione di app basate su Electron, poiché benefici degli aggiornamenti di sicurezza regolari del tuo browser.
- Non include funzionalità aggiuntive (bloatware) che non influiscono sulla privacy dell'utente.
- Non raccoglie la telemetria di default.
- Fornisce un'implementazione open source del server di sincronizzazione.
- Presenta un [motore di ricerca privato](search-engines.md) di default.

### Criteri delle Estensioni

- Non deve replicare funzionalità integrate nel browser o del sistema operativo.
- Deve influenzare direttamente la privacy dell'utente, cioè non deve semplicemente fornire informazioni.

[^1]: L'implementazione di Brave è descritta nei dettagli su [Aggiornamenti sulla Privacy di Brave: Partizione dello stato della rete per la privacy](https://brave.com/privacy-updates/14-partitioning-network-state/).
