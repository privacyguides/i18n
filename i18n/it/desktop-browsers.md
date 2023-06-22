---
meta_title: "Browser web che rispettano la privacy per PC e Mac - Privacy Guides"
title: "Browser desktop"
icon: material/laptop
description: Questi browser web offrono una maggiore protezione della privacy rispetto a Google Chrome.
cover: desktop-browsers.png
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Browser privati per desktop consigliati
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/en/browser
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

Questi sono i browser e le configurazioni per desktop attualmente consigliati per la navigazione quotidiana e non anonima. Raccomandiamo [Mullvad Browser](#mullvad-browser) se sei interessato a una forte protezione della privacy e all'anti-fingerprinting senza dover configuare le impostazioni del browser, [Firefox](#firefox) per i navigatori occasionali che cercano una buona alternativa a Google Chrome e [Brave](#brave) se hai bisogno della compatibilità con il browser Chromium.

Se hai bisogno di navigare in Internet in modo anonimo, dovresti invece usare [Tor](tor.md). In questa pagina forniamo alcune raccomandazioni sulla configurazione, ma tutti i browser diversi da Tor Browser saranno rintracciabili da *qualcuno* in un modo o nell'altro.

## Mullvad Browser

!!! recommendation

    ![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    **Mullvad Browser** è una versione di [Tor Browser](tor.md#tor-browser) con le integrazioni della rete Tor rimosse, con l'obiettivo di fornire le tecnologie anti-fingerprinting di Tor Browser agli utenti che usano una VPN. È sviluppato dal Progetto Tor e distribuito da [Mullvad](vpn.md#mullvad) e **non** richiede l'uso della VPN di Mullvad.
    
    [:octicons-home-16: Pagina Principale](https://mullvad.net/en/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Politica sulla privacy" }
    [:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Codice sorgente" }
    
    ??? downloads "Scarica"
    
        - [:simple-windows11: Windows](https://mullvad.net/it/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/it/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/it/download/browser/linux)

Come [Tor Browser](tor.md), Mullvad Browser è progettato per prevenire il fingerprinting rendendo l'impronta digitale del browser identica a quella di tutti gli altri utenti di Mullvad Browser e include impostazioni ed estensioni predefinite che vengono configurate automaticamente dai livelli di sicurezza predefiniti: *Standard*, *Safer* e *Safest*. Pertanto, è indispensabile **non** modificare il browser oltre i livelli di sicurezza [predefiniti](https://tb-manual.torproject.org/security-settings/). Altre modifiche renderebbero l'impronta digitale unica, vanificando lo scopo dell'utilizzo di questo browser. Se desideri configurare il tuo browser in modo più completo e il fingerprinting non vi preoccupa, vi consigliamo di utilizzare [Firefox](#firefox).

### Anti-Fingerprinting

**Senza** utilizzare una [VPN](vpn.md), Mullvad Browser fornisce le stesse protezioni contro [gli script di fingerprinting "naive"](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) di altri browser privati come Firefox+[Arkenfox](#arkenfox-advanced) o [Brave](#brave). Mullvad Browser fornisce queste protezioni "out of the box", a scapito di una certa flessibilità e comodità che altri browser privati possono offrire.

==Per ottenere la massima protezione anti-fingerprinting, si consiglia di utilizzare Mullvad Browser insieme a **** una VPN==, sia essa Mullvad o un altro provider VPN consigliato. Quando si utilizza una VPN con Mullvad Browser, si condivide un'impronta digitale e un pool di indirizzi IP con molti altri utenti, offrendo una "folla" con cui confondersi. Questa strategia è l'unico modo per contrastare gli script di tracciamento avanzati ed è la stessa tecnica anti-fingerprinting utilizzata da Tor Browser.

Si noti che, sebbene sia possibile utilizzare Mullvad Browser con qualsiasi provider VPN, affinché esista questa "folla" è necessario che anche altre persone su quella VPN utilizzino Mullvad Browser, cosa che è più probabile su Mullvad VPN rispetto ad altri provider, soprattutto a così breve distanza dal lancio di Mullvad Browser. Mullvad Browser non dispone di connettività VPN integrata, né controlla se si sta utilizzando una VPN prima di navigare; la connessione VPN deve essere configurata e gestita separatamente.

Mullvad Browser viene fornito con le estensioni del browser *uBlock Origin* e *NoScript* preinstallate. Anche se di solito [non consigliamo di](#extensions) aggiungere *estensioni aggiuntive* del browser, queste estensioni preinstallate con il browser non **dovrebbero essere rimosse o** configurate al di fuori dei valori predefiniti, perché in questo modo l'impronta digitale del browser si distinguerebbe notevolmente da quella degli altri utenti di Mullvad Browser. Viene inoltre preinstallata l'estensione per il browser Mullvad-Browser-Extension, che *può* essere rimossa in modo sicuro senza impattare sull'impronta digitale del browser, se lo si desidera, ma può essere mantenuta anche se non si utilizza Mullvad VPN.

### Modalità Navigazione privata

Mullvad Browser opera in modalità di navigazione privata permanente, il che significa che la cronologia, i cookie e altri dati del sito verranno sempre cancellati ogni volta che il browser viene chiuso. I segnalibri, le impostazioni del browser e le impostazioni delle estensioni saranno comunque conservate.

Ciò è necessario per impedire forme avanzate di tracciamento, ma comporta il costo della comodità e di alcune funzioni di Firefox, come i contenitori multi account. Ricordati che puoi sempre utilizzare più browser, ad esempio potresti considerare di utilizzare Firefox+Arkenfox per alcuni siti a cui vuoi rimanere loggato o che non funziona correttamente con Mullvad Browser, e Mullvad Browser per la navigazione generale.

### Mullvad Leta

Mullvad Browser utilizza DuckDuckGo come [motore di ricerca](search-engines.md) predefinito, ma include anche **Mullvad Leta**, un motore di ricerca che richiede un abbonamento attivo a Mullvad VPN per poterlo utilizzare. Mullvad Leta interroga direttamente l'API di ricerca a pagamento di Google (motivo per cui è limitata agli abbonati), tuttavia a causa di questa limitazione è possibile per Mullvad correlare le query di ricerca e gli account VPN Mullvad. Per questo motivo sconsigliamo l'uso di Mullvad Leta, anche se Mullvad raccoglie pochissime informazioni sui propri abbonati alla VPN.

## Firefox

!!! recommendation

    ![Firefox logo](assets/img/browsers/firefox.svg){ align=right }
    
    **Firefox** offre robuste impostazioni di privacy, come la [protezione antitracciamento avanzata](https://support.mozilla.org/it/kb/protezione-antitracciamento-avanzata-firefox-desktop), che aiuta a bloccare varie [tipologie di tracciamento](https://support.mozilla.org/it/kb/protezione-antitracciamento-avanzata-firefox-desktop#w_che-cosa-viene-bloccato-con-la-protezione-antitracciamento-avanzata).
    
    [:octicons-home-16: Pagina Principale](https://firefox.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mozilla.org/privacy/firefox/){ .card-link title="Politica sulla privacy" }
    [:octicons-info-16:](https://firefox-source-docs.mozilla.org/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Codice sorgente" }
    [:octicons-heart-16:](https://donate.mozilla.org/){ .card-link title=Contribuisci }
    
    ??? downloads "Scarica"
    
        - [:simple-windows11: Windows](https://www.mozilla.org/firefox/windows)
        - [:simple-apple: macOS](https://www.mozilla.org/firefox/mac)
        - [:simple-linux: Linux](https://www.mozilla.org/firefox/linux)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

!!! warning
    Firefox include un [token di download](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) univoco nella sezione dei download del sito di Mozilla e utilizza la telemetria in Firefox per inviarlo. Il token **non** è incluso nelle versioni rilasciate dall'[FTP di Mozilla](https://ftp.mozilla.org/pub/firefox/releases/).

### Configurazione consigliata

Queste opzioni possono essere trovare in :material-menu: → **Impostazioni**

#### Ricerca

- [ ] Disabilita **Visualizza suggerimenti di ricerca**

I suggerimenti di ricerca potrebbero non essere disponibili nella tua zona.

I suggerimento di ricerca inviano tutto quello che viene scritto nella barra di ricerca al motore di ricerca predefinito, indipendentemente se le stringe vengono inviate o meno. Disabilitare i suggerimenti di ricerca ti permette di controllare più precisamente quali dati invii al motore di ricerca che utilizzi.

#### Privacy & Sicurezza

##### Protezione antitracciamento avanzata

- [x] Seleziona Protezione antitracciamento avanzata **Restrittiva**

Essa ti protegge bloccando i tracker dei social, script di fingerprinting (nota che questo non ti protegge da *tutte* le forme di fingerprinting), minatori di criptovalute, cookie di tracciamento cross-site e altri contenuti di tracciamento. La Protezione antitracciamento avanzata protegge da molte minacce comuni, ma non blocca tutte le vie di tracciamente, perché progettata per avere minimo o nessun impatto sull'usabilità dei siti.

##### Firefox Suggest (esclusivo USA)

[Firefox Suggest](https://support.mozilla.org/it/kb/personalizzare-impostazioni-firefox-suggest) è una funzione simile ai suggerimenti di ricerca, disponibile solo negli Stati Uniti. Si consiglia di disattivarla per lo stesso motivo per cui si consiglia di disattivare i suggerimenti di ricerca. Se non vedi queste opzioni sotto l'intestazione della **barra degli indirizzi**, la nuova esperienza non è disponibile per te e puoi ignorare queste modifiche.

- [ ] Disabilita **Suggestions from the web**
- [ ] Disabilita **Suggestions from sponsors**

##### Sanitizzazione alla chiusura

Se vuoi mantenere l'accesso per alcuni siti in particolare, puoi consentire le eccezioni in **Cookie e dati dei siti web** → **Gestisci eccezioni...**

- [x] Seleziona **Elimina cookie e dati dei siti web alla chiusura di Firefox**

Ciò ti protegge dai cookie persistenti, ma non da quelli acquisiti durante ogni sessione di navigazione. Con questa opzione attiva, è possibile eliminare facilmente i cookie del browser riavviando Firefox. È possibile impostare le eccezioni per ogni sito, ad esempio se desideri mantenere l'accesso ad un sito particolare che frequenti spesso.

##### Telemetria

- [ ] Disabilita **Consenti a Firefox di inviare a Mozilla dati tecnici e relativi all’interazione con il browser**
- [ ] Disabilita **Consenti a Firefox di installare e condurre studi**
- [ ] Disabilita **Consenti a Firefox di inviare segnalazioni di arresto anomalo in sospeso**

> Firefox invia dati relativi alla versione e alla lingua di Firefox, al sistema operativo del dispositivo, alla configurazione hardware, memoria, informazioni basiche sugli arresti anomali ed errori, ai risultati dei processi automatici come gli aggiornamenti, Safebrowsing e l'attivazione a noi. Quando Firefox ci invia dati, il tuo indirizzo IP viene temporaneamente raccolto da parte dei nostri server.

Inoltre, il servizio Firefox Accounts raccoglie [alcuni dati tecnici](https://www.mozilla.org/en-US/privacy/firefox/#firefox-accounts). Se usi un Account Firefox, puoi disattivare questa funzione:

1. Apri le [ impostazioni del tuo profilo su accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Deseleziona ** Raccolta e utilizzo dati ** > **Aiutaci a migliorare gli ⁨account Firefox⁩**

##### Modalità solo HTTPS

- [x] Seleziona **Attiva in tutte le finestre**

Questo ti aiuta a prevenire il collegamento non intenzionale ad un sito web in HTTP. Siti web senza l'HTTPS sono piuttosto rari il giorno d'oggi, quindi questa opzione non dovrebbe avere un grosso impatto sulla tua navigazione quotidiana.

#### Sincronizzazione

La [sincronizzazione via Firefox](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) permette ai tuoi dati di navigazione (cronologia, segnalibri, etc.) di essere accessibili su tutti i tuoi dispositivi; i dati vengono protetti mediante E2EE.

### Arkenfox (avanzato)

!!! tip "Utilizza Mullvad Browser per una protezione avanzata contro il fingerprinting"

    [Mullvad Browser](#mullvad-browser) fornisce le stesse protezioni contro il fingerprinting di Arkenfox e non richiede l'uso della VPN di Mullvad per beneficiare di tali protezioni. Abbinato a una VPN, Mullvad Browser è in grado di contrastare gli script di tracciamento più avanzati, cosa che Arkenfox non può fare. Arkenfox ha comunque il vantaggio di essere molto più flessibile e di consentire eccezioni specifiche per i siti web ai quali è necessario rimanere connessi.

Il progetto [Arkenfox](https://github.com/arkenfox/user.js) fornisce un insieme di opzioni attentamente selezionate per Firefox. Se [decidi](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) di utilizzare Arkenfox, [alcune opzioni](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) sono più stringenti di altre e/o potrebbero causare il malfunzionamento di alcuni siti web - [opzioni che possono essere cambiate facilmente](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) per soddisfare le tue esigenze. Vi **consigliamo vivamente** di leggere tutta la loro [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox inoltre abilita il supporto per le [schede contenitore](https://support.mozilla.org/it/kb/containers-schede-contenitore-firefox#per-utenti-avanzati).

Arkenfox mira solo a contrastare gli script di tracciamento di base o ingenui attraverso la randomizzazione dei canvas e le impostazioni di configurazione della resistenza contro il fingerprint integrate in Firefox. Non mira a far sì che il browser si confonda con una grande folla di altri utenti di Arkenfox, come fanno Mullvad Browser o Tor Browser, che è l'unico modo per contrastare gli script avanzati di tracciamento. Ricordati che puoi sempre utilizzare più browser, ad esempio potresti considerare di utilizzare Firefox+Arkenfox per alcuni siti a cui non vuoi rimuovere l'accesso o di cui ti fidi, e Mullvad Browser per la navigazione generale.

## Brave

!!! recommendation

    ![Brave logo](assets/img/browsers/brave.svg){ align=right }
    
    **Brave Browser** include un content blocker integrato e [funzionalità di privacy](https://brave.com/privacy-features/), molte delle quali attive in modo predefinito.
    
    Brave è stato sviluppato utilizzando il progetto del browser Chromium, quindi dovrebbe risultarti familiare e avrai pochi problemi di compatibilità con i vari siti web.
    
    [:octicons-home-16: Pagina principale](https://brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Servizio Onion" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Politica sulla privacy" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Codice sorgente" }
    
    ??? downloads annotate "Scarica"
    
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
        - [:simple-windows11: Windows](https://brave.com/download/)
        - [:simple-apple: macOS](https://brave.com/download/)
        - [:simple-linux: Linux](https://brave.com/linux/) (1)

    1. Sconsigliamo l'utilizzo della versione Flatpack di Brave, in quanto rimpiazza il sandbox di Chromium con quello di Flatpak, il quale è meno efficace. Inoltre, il pacchetto non è gestito da Brave Software, Inc.

### Configurazione consigliata

Queste opzioni possono essere trovare in :material-menu: → **Impostazioni**.

#### Impostazioni

##### Shields

Brave include alcune misure contro il fingerprinting nella sua funzionalità [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-). Consigliamo di configurare queste opzioni [globalmente](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) applicate a tutti i siti che visiti.

Le funzionalità di Shields possono essere ridotte per ogni sito se necessario; ciò nonostante, raccomandiamo le seguenti impostazioni:

<div class="annotate" markdown>

- [x] Seleziona **Impedisci il fingerprinting tramite le impostazioni della lingua**
- [x] Seleziona il Blocco di tracker e annunci come **Aggressivo**

    ??? warning "Usa gli elenchi di filtri predefiniti"
        Brave ti consente di selezionare ulteriori filtri di contenuti mediante la pagina interna `brave://adblock`. Si consiglia di non utilizzare questa funzione e di mantenere gli elenchi di filtri predefiniti. il loro utilizzo ti distingue dagli altri utenti Brave, e potrebbe inoltre aumentare la superficie di attacco se esiste un exploit nel browser sfruttabile da codice malizioso presente nelle liste stesse.

- [x] (Opzionale) Seleziona **Blocco degli script** (1)
- [x] Sleziona Blocca il fingerprinting come **Rigido, potrebbe non far funzionare alcuni siti**

</div>

1. Questa opzione fornisce una funzionalità simile alla [modalità avanzata di blocco](https://github.com/gorhill/uBlock/wiki/Blocking-mode)dell'estensione uBlock Origin o [NoScript](https://noscript.net/).

##### Blocco dei social

- [ ] Deseleziona tutte le opzioni legate ai social

##### Privacy e sicurezza

<div class="annotate" markdown>

- [x] Seleziona **Disabilita UDP senza proxy** in [Gestione politica IP WebRTC IP](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Disabilita **Utilizza i servizzi Google per  la messaggistica push**
- [ ] Disabilita **Acconsenti all'analisi dei prodotti di tutel della privacy (P3A)**
- [ ] Disabilita **Invia automaticamente un ping di utilizzo giornaliero a Brave**
- [ ] Disabilita **Invia automaticamente i rapporti di diagnostica**
- [x] Seleziona **Utilizza sempre connessioni sicure** nel menu **Sicurezza** 
- [ ] Disabilita **Finestra in Incognito con Tor** (1)

    !!! tip "Pulizia alla chiusura"

        - [x] Selezionare **Cancella i cookie e i dati del sito alla chiusura di tutte le finestre** nel menu *Cookies e altri dati del sito*

        Se si desidera rimanere connessi a un particolare sito che si visita spesso, è possibile impostare eccezioni su base individuale nella sezione *Comportamenti personalizzati*.

</div>

1. Brave **non è** resistente al fingerprinting come il Tor Browser e molte meno persone utilizzano Brave con Tor, facendoti quindi distinguere. Quando [è necessario un forte anonimato](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-) utilizzare il [Tor Browser](tor.md#tor-browser).

##### Estensioni

Disabilita le estensioni integrate che non utilizzi in **Estensioni**

- [ ] Disabilita **Hangouts**
- [ ] Disabilita **WebTorrent**

##### Web3

Le funzionalità Web3 di Brave possono potenzialmente aumentare il fingerprint del browser e la superficie di attacco. Disattiva le funzioni, a meno che tu non le utilizzi.

Imposta **Wallet Ethereum predefinito** su **Estensioni (nessun backup)** Imposta **Wallet Solana predefinito** su **Estensioni (nessun backup)** Imposta **Metodo per risolvere le risorse IPFS** su **Disabilitato**

##### Sistema

<div class="annotate" markdown>

- [ ] Disabilita **Continua a eseguire applicazioni in background dopo la chiusura di Brave** per disabilitare le applicazioni in background (1)

</div>

1. Questa opzione non è presente su tutte le piattaforme.

#### Sincronizzazione

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) permette ai dati di navigazione (cronologia, segnalibri, ecc.) di essere accessibili su tutti i dispositivi senza richiedere un account e li protegge con E2EE.

#### Brave Rewards e Wallet

**Brave Rewards** consente di ricevere la criptovaluta Basic Attention Token (BAT) per aver compiuto determinate azioni all'interno di Brave. Si basa su un conto di deposito e sul KYC di un numero selezionato di fornitori. Non raccomandiamo il BAT come [criptovaluta privata](cryptocurrency.md), né raccomandiamo l'uso di un [portafoglio di deposito](advanced/payments.md#other-coins-bitcoin-ethereum-etc), pertanto sconsigliamo di utilizzare questa funzione.

**Brave Wallet** opera localmente sul vostro computer, ma non supporta alcuna criptovaluta privata, per cui vi sconsigliamo di utilizzare anche questa funzione.

## Risorse aggiuntive

In generale, si consiglia di ridurre al minimo le estensioni del browser; hanno un accesso privilegiato all'interno del browser, richiedono fiducia nello sviluppatore, possono farti [risaltare](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)e [indebolire](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) l'isolamento del sito. Tuttavia, uBlock Origin può rivelarsi utile se si apprezza la funzionalità di blocco dei contenuti.

### uBlock Origin

!!! recommendation

    ![uBlock Origin logo](assets/img/browsers/ublock_origin.svg){ align=right }
    
    **uBlock Origin** è un popolare blocker di contenuti che aiuta a bloccare pubblicità, tracker e script di fingerprinting.
    
    [:octicons-repo-16: Repository](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Informativa sulla privacy" }
    [:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Codice sorgente" }
    
    ??? downloads "Scarica"
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

Consigliamo di seguire la [documentazione dello sviluppatore](https://github.com/gorhill/uBlock/wiki/Blocking-mode) e di scegliere una delle "modalità". Ulteriori filtri potrebbero influire sulla performance e [ possono aumentare la superficie di attacco](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

##### Altre liste

Queste sono altre [liste di filtri](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) che potresti considerare di aggiungere:

- [x] Spunta **Privacy** > **AdGuard URL Tracking Protection**
- Aggiungi [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

## Criteri

**Si noti che non siamo affiliati a nessuno dei progetti che raccomandiamo.** Oltre ai [ nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie di requisiti chiari che ci consentono di fornire raccomandazioni obiettive. Ti consigliamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le vostre ricerche per assicurarvi che sia la scelta giusta per voi.

!!! example "Questa sezione è nuova"

    Stiamo lavorando per stabilire criteri ben definiti per ogni sezione del nostro sito, e questo potrebbe essere soggetto a modifiche. Se avete domande sui nostri criteri, vi preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e non date per scontato che non abbiamo preso in considerazione qualcosa nel formulare le nostre raccomandazioni se non è elencato qui. Sono molti i fattori presi in considerazione e discussi quando consigliamo un progetto, e stiamo lavorando per documentare ogni singolo fattore.

### Requisiti minimi

- Deve essere un software open-source.
- Supporta gli aggiornamenti automatici.
- Deve ricevere "engine updates" in 0-1 giorni dalla pubblicazione upstream.
- Disponibile su Linux, macOS, e Windows.
- Qualsiasi modifica necessaria per rendere il browser più rispettoso della privacy non dovrebbe avere un impatto negativo sull'esperienza dell'utente.
- Blocca i cookie di terze parti con le impostazioni predefinite.
- Supporta il [partizionamento degli stati](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) per mitigare il tracciamento cross-site.[^1]

### Criteri Ottimali

KeePassXC memorizza i suoi dati di esportazione come file [CSV](https://en.wikipedia.org/wiki/Comma-separated_values). Ciò può comportare la perdita di dati se si importa questo file in un altro gestore di password.

- Include una funzionalità di blocco dei contenuti integrata.
- Supporta la compartimentazione dei cookie (alla maniera di [Multi-Account Containers](https://support.mozilla.org/en-US/kb/containers)).
- Supporta le Progressive Web Apps.  
  Le PWA consentono di installare determinati siti web come se fossero applicazioni native sul computer. Questo può avere dei vantaggi rispetto all'installazione di applicazioni basate su Electron, perché si beneficia degli aggiornamenti di sicurezza regolari del browser.
- Non include funzionalità aggiuntive (bloatware) che non influiscono sulla privacy dell'utente.
- Non raccoglie la telemetria per impostazione predefinita.
- Fornisce un'implementazione open-source del server di sincronizzazione.
- [ Il motore di ricerca privato ](search-engines.md) è predefinito.

### Criteri delle estensioni

- Non deve replicare funzionalità integrate nel browser o del sistema operativo.
- Deve avere un impatto diretto sulla privacy dell'utente, cioè non deve limitarsi a fornire informazioni.

[^1]: L'implementazione di Brave è descritta in dettaglio su [Brave Privacy Updates: Partizione dello stato della rete per la privacy](https://brave.com/privacy-updates/14-partitioning-network-state/).
