---
meta_title: "Browser web che rispettano la privacy per PC e Mac - Privacy Guides"
title: "Browser desktop"
icon: material/laptop
description: Questi browser per la protezione della privacy sono quelli che attualmente consigliamo per la navigazione standard/non anonima su sistemi desktop.
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

<small>Protegge dalle seguenti minacce:</small>

- [:material-account-cash: Capitalismo di sorveglianza](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Questi sono i **browser desktop** e le configurazioni attualmente consigliati per la navigazione standard/non anonima. Consigliamo [Mullvad Browser](#mullvad-browser) se sei interessato a una forte protezione della privacy e all'anti-fingerprinting pronti all'uso, [Firefox](#firefox) per i navigatori occasionali di Internet alla ricerca di una buona alternativa a Google Chrome e [Brave](#brave), se necessiti della compatibilità del browser con Chromium.

Invece, se necessiti di navigare anonimamente su Internet, dovresti utilizzare [Tor](tor.md). In questa pagina forniamo alcune raccomandazioni sulla configurazione, ma tutti i browser diversi da Tor Browser saranno rintracciabili da *qualcuno* in un modo o nell'altro.

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Logo di Mullvad Browser](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** è una versione del [Tor Browser](tor.md#tor-browser) con le integrazioni della rete Tor rimosse. L'obiettivo è quello di fornire agli utenti di VPN le tecnologie anti-fingerprinting del Tor Browser, che sono protezioni fondamentali contro la [:material-eye-outline: Sorveglianza di Massa](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. Sviluppato dal Tor Project e distribuito da [Mullvad](vpn.md#mullvad), **non** richiede l'utilizzo della VPN di Mullvad.

[:octicons-home-16: Pagina Principale](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="Documentazione" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Codice Sorgente" }

<details class="downloads" markdown>
<summary>Download</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Come [Tor Browser](tor.md), Mullvad Browser è progettato per prevenire il fingerprinting rendendo l'impronta digitale del browser identica a quella di tutti gli altri utenti di Mullvad Browser e include impostazioni ed estensioni predefinite che vengono configurate automaticamente dai livelli di sicurezza predefiniti: *Standard*, *Sicuro* e *il più sicuro*.

Pertanto, è assolutamente necessario non modificare il browser al di fuori della regolazione dei [livelli di sicurezza](https://tb-manual.torproject.org/security-settings) predefiniti. Quando regoli il livello di sicurezza, è sempre **necessario** riavviare il browser prima di continuare a utilizzarlo. In caso contrario, [le impostazioni di sicurezza potrebbero non essere applicate completamente](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), esponendoti a un rischio di fingerprinting e di exploit più elevato di quello previsto in base all'impostazione da te scelta.

Modifiche diverse dalla regolazione di questa impostazione renderebbero la tua impronta digitale unica, vanificando lo scopo dell'utilizzo di questo browser. Se desideri configurare il tuo browser in modo più completo e il fingerprinting non ti preoccupa, consigliamo invece [Firefox](#firefox).

### Anti-Fingerprinting

**Senza** utilizzare una [VPN](vpn.md), Mullvad Browser fornisce le stesse protezioni dai [semplici script di fingerprinting](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) di altri browser privati, come Firefox+[Arkenfox](#arkenfox-advanced) o [Brave](#brave). Mullvad Browser fornisce tali protezioni "pronte all'uso", a scapito di una certa flessibilità e comodità che altri browser privati possono fornire.

==Per la massima protezione anti-fingerprinting, consigliamo di utilizzare Mullvad Browser **con** una VPN==, che sia di Mullvad o di un altro fornitore di VPN consigliato. Utilizzando una VPN con Mullvad Browser, condividi un'impronta digitale e un gruppo di indirizzi IP con molti altri utenti, offrendoti una "folla" con cui confonderti. Questa strategia è l'unico modo per contrastare gli script di tracciamento avanzati ed è la stessa tecnica anti-fingerprinting utilizzata da Tor Browser.

Nota che, sebbene tu possa utilizzare Mullvad Browser con qualsiasi fornitore VPN, altre persone su tale VPN devono anch'esse utilizzare Mullvad Browser affinché tale "folla" esista, il che è molto più probabile su Mullvad VPN, rispetto ad altri fornitori, in particolare così a breve distanza dal lancio di Mullvad Browser. Mullvad Browser non dispone di connettività VPN integrata, né verifica che tu stia utilizzando una VPN prima di navigare; la tua connessione VPN dev'essere configurata e gestita separatamente.

Mullvad Browser contiene le estensioni pre-installate di *uBlock Origin* e *NoScript*. Anche se in genere sconsigliamo di aggiungere *ulteriori* [estensioni del browser](browser-extensions.md), quelle preinstallate **non** devono essere rimosse o configurate al di fuori dei valori predefiniti, perché in questo modo l'impronta digitale del browser si distinguerebbe notevolmente da quella degli altri utenti di Mullvad Browser. Inoltre, presenta l'Estensione Mullvad Browser pre-installata, che *può* essere rimossa in sicurezza, senza influenzare l'impronta digitale del tuo browser, se lo desideri, ma è anche sicura da mantenere se non utilizzi la VPN di Mullvad.

### Modalità di Navigazione Privata

Mullvad Browser opera in modalità di navigazione privata permanente, ciò significa che la tua cronologia, cookie e altri dati dei siti saranno eliminati a ogni chiusura del browser. I tuoi segnalibri, le impostazioni del browser e dell'estensione saranno comunque conservati.

Ciò è necessario per impedire forme avanzate di tracciamento, a costo della comodità e di alcune funzionalità di Firefox, come i Contenitori Multi Profilo. Ricordati che puoi sempre utilizzare più browser, ad esempio, potresti considerare di utilizzare Firefox+Arkenfox per alcuni siti cui desideri rimanere connesso o, altrimenti, che non operano adeguatamente su Mullvad Browser, e Mullvad Browser per la navigazione generale.

### Mullvad Leta

Il Mullvad Browser viene fornito con [**Mullvad Leta**](https://leta.mullvad.net) come motore di ricerca predefinito, che funziona come proxy dei risultati di ricerca di Google o Brave (configurabile sulla pagina principale di Mullvad Leta).

Se sei un utente di Mullvad VPN, c'è qualche rischio nell'utilizzare servizi come Mullvad Leta, offerti dallo stesso fornitore VPN. Questo perché Mullvad ha teoricamente accesso al tuo vero indirizzo IP (tramite la loro VPN) e alla tua attività di ricerca (tramite Leta), informazioni che una VPN è in genere destinata a separare. Anche se Mullvad raccoglie pochissime informazioni sugli abbonati alla VPN o sugli utenti di Leta, dovresti considerare un altro [motore di ricerca](search-engines.md) se questo rischio ti preoccupa.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox logo](assets/img/browsers/firefox.svg){ align=right }

**Firefox** offre robuste impostazioni di privacy, come la [protezione antitracciamento avanzata](https://support.mozilla.org/it/kb/protezione-antitracciamento-avanzata-firefox-desktop), che aiuta a bloccare varie [tipologie di tracciamento](https://support.mozilla.org/it/kb/protezione-antitracciamento-avanzata-firefox-desktop#w_che-cosa-viene-bloccato-con-la-protezione-antitracciamento-avanzata).

[:octicons-home-16: Pagina Principale](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="Documentazione }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Contribuisci" }

<details class="downloads" markdown>
<summary>Download</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Firefox include un [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) unico nei download dal sito web di Mozilla e utilizza la telemetria di Firefox per inviare il token. Il token **non** è incluso nelle versioni di [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Configurazione consigliata di Firefox

Queste opzioni possono essere trovate in :material-menu: → **Impostazioni**.

#### Ricerca

- [ ] Disabilita **Visualizza suggerimenti di ricerca**

Le funzionalità di suggerimento di ricerca potrebbero non essere disponibili nella tua zona.

I suggerimenti di ricerca inviano tutto ciò che digiti nella barra degli indirizzi al motore di ricerca predefinito, anche se non effettui la ricerca. Disabilitare i suggerimenti di ricerca ti consente di controllare con maggiore precisione i dati inviati al fornitore del motore di ricerca.

##### Firefox Suggest (solo USA)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) è una funzionalità simile ai suggerimenti di ricerca, disponibile solo negli Stati Uniti. Consigliamo di disattivarla per lo stesso motivo per cui consigliamo di disattivare i suggerimenti di ricerca. Se non vedi queste opzioni sotto l'intestazione della **Barra degli indirizzi**, significa che non hai la nuova esperienza e puoi ignorare queste modifiche.

- [ ] Deselezionare i **suggerimenti da Firefox**
- [ ] Rimuovi la spunta da **Suggestions from sponsors**

#### Privacy e sicurezza

##### Protezione antitracciamento avanzata

- [x] Seleziona Protezione antitracciamento avanzata **Restrittiva**

Questo ti protegge bloccando i tracker dei social media, gli script di fingerprinting (nota che questo non ti protegge da *tutti* i fingerprinting), i cryptominer, i cookie intersito traccianti e altri contenuti di tracking. La Protezione antitracciamento avanzata protegge da molte minacce comuni, ma non blocca tutte le modalità di tracciamento perché è progettata per avere un impatto minimo o nullo sull'usabilità del sito.

##### Eliminazione alla Chiusura

Se desideri rimanere connesso a determinati siti, puoi consentire le eccezioni in **Cookie e dati dei siti web** → **Gestisci eccezioni...**

- [x] Spunta **Elimina cookie e dati dei siti web alla chiusura di Firefox**

Ciò ti protegge dai cookie persistenti, ma non da quelli acquisiti durante ogni sessione di navigazione. Quando e' abilitato,   puoi pulire facilmente i cookie del browser semplicemente riavviando Firefox. Puoi impostare eccezioni per ogni sito, se desideri rimanere connesso a un particolare sito che visiti spesso.

##### Telemetria

- [ ] Rimuovi la spunta da **Consenti a Firefox di inviare a Mozilla dati tecnici e relativi all’interazione con il browser**
- [ ] Rimuovi la spunta da **Consenti a Firefox di installare e condurre studi**
- [ ] Rimuovi la spunta da **Consenti a Firefox di inviare segnalazioni di arresto anomalo in sospeso**

Secondo la politica sulla privacy di Mozilla, Firefox:

> Firefox ci invia i dati sulla tua versione e lingua di Firefox; sistema operativo del dispositivo e configurazione hardware; memoria, informazioni essenziali su arresti anomali ed errori; risultati di processi automatizzati quali aggiornamenti, navigazione sicura e attivazione. Quando Firefox ci invia i dati, il tuo indirizzo IP è raccolto temporaneamente come parte dei registri del nostro server.

Inoltre, il servizio Mozilla Accounts raccoglie [alcuni dati tecnici](https://mozilla.org/privacy/mozilla-accounts). Se utilizzi un account Mozilla, puoi disattivare:

1. Apri le [impostazioni del tuo profilo su accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Deseleziona ** Raccolta e utilizzo dati ** > **Aiutaci a migliorare gli ⁨account Firefox⁩**

##### Impostazioni per le pubblicità nei siti web

- [ ] Rimuovi la spunta da **Permetti ai siti web di effettuare misurazioni pubblicitarie nel rispetto della privacy**

Con il rilascio di Firefox 128, è stata aggiunta una nuova impostazione per [l'attribuzione nel rispetto della privacy](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA), [attivata di default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). La PPA consente agli inserzionisti di utilizzare il tuo browser web per misurare l'efficacia delle campagne web, invece di utilizzare il tradizionale tracciamento basato su JavaScript. Riteniamo che questo comportamento non rientri nell'ambito delle responsabilità di un user agent e il fatto che sia disabilitato di default in Arkenfox è un ulteriore indicatore per disabilitare questa funzione.

##### Modalità solo HTTPS

- [x] Seleziona **Attiva in tutte le finestre**

Ciò previene che ti connetta involontariamente a un sito web in HTTP semplice. I siti privi di HTTPS sono ormai poco diffusi, quindi l'impatto sulla tua navigazione quotidiana dovrebbe essere minimo o nullo.

##### DNS su HTTPS

Se utilizzi un [fornitore DNS su HTTPS](dns.md):

- [x] Seleziona **Protezione massima** e scegli un fornitore adatto

La protezione massima impone l'uso del DNS su HTTPS e viene visualizzato un avviso di sicurezza se Firefox non riesce a connettersi al tuo risolutore DNS sicuro o se il tuo risolutore DNS sicuro dice che i record per il dominio a cui stai cercando di accedere non esistono. Questo impedisce alla rete a cui si è sei connesso di declassare segretamente la tua sicurezza DNS.

#### Sincronizzazione

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) permette ai dati di navigazione (cronologia, segnalibri, ecc.) di essere accessibili su tutti i tuoi dispositivi e li protegge con l'E2EE.

### Arkenfox (avanzato)

<div class="admonition tip" markdown>
<p class="admonition-title">Usa Mullvad Browser per l'anti-fingerprinting avanzato</p>

[Mullvad Browser](#mullvad-browser) fornisce le stesse protezioni anti-fingerprinting di Arkenfox pronte all'uso e non richiede l'utilizzo della VPN di Mullvad per beneficiarne. Insieme a una VPN, Mullvad Browser può contrastare gli script di tracciamento più avanzati, a differenza di Arkenfox. Tuttavia, Arkenfox presenta il vantaggio di essere molto più flessibile e di consentire eccezioni specifiche per i siti web a cui necessiti di rimanere connesso.

</div>

Il [progetto Arkenfox](https://github.com/arkenfox/user.js) offre una serie di opzioni attentamente valutate per Firefox. Se [decidi](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) di utilizzare Arkenfox, [alcune opzioni](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) sono soggettivamente rigide e/o potrebbero causare il malfunzionamento di alcuni siti web, ma puoi [facilmente modificarle](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) secondo le tue necessità. Ti **consigliamo vivamente** di leggere la loro [wiki](https://github.com/arkenfox/user.js/wiki) completa. Arkenfox consente anche il supporto [dei container](https://support.mozilla.org/kb/containers#w_for-advanced-users).

Arkenfox mira solo a contrastare gli script di tracciamento semplici attraverso la randomizzazione del canvas e le impostazioni di configurazione della resistenza al fingerprinting integrate in Firefox. Non mira a far sì che il tuo browser si confonda con una grande folla di altri utenti Arkenfox, come fanno Mullvad Browser o Tor Browser, che è l'unico modo per contrastare gli script avanzati di tracciamento fingerprinting avanzati. Ricordati che puoi sempre utilizzare più browser, ad esempio, potresti considerare di utilizzare Firefox+Arkenfox per alcuni siti cui desideri rimanere connesso o di cui ti fidi, e Mullvad Browser per la navigazione generale.

## Brave

<div class="admonition recommendation annotate" markdown>

![Logo di Brave](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** include un bloccatore dei contenuti integrato e [funzionalità per la privacy](https://brave.com/privacy-features), molte delle quali sono abilitate di default.

Brave è basato sul progetto del browser web di Chromium, quindi, dovrebbe risultare familiare e avere problemi minimi di compatibilità con i siti web.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Servizio Onion" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Download</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Brave aggiunge un "[codice di riferimento](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" al nome del file nei download dal sito web di Brave, che viene utilizzato per tracciare la fonte da cui è stato scaricato il browser, ad esempio `BRV002` in un download chiamato `Brave-Browser-BRV002.pkg`. Il programma d'installazione invierà un ping al server di Brave con il codice di riferimento al termine del processo d'installazione. Se sei preoccupato per questo motivo, puoi rinominare il file d'installazione prima di aprirlo.

</div>

### Configurazione consigliata di Brave

Queste opzioni possono essere trovate in :material-menu: → **Impostazioni**.

#### Shields

Brave include delle misure anti-fingerprinting nella sua funzione [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Suggeriamo di configurare queste opzioni [globalmente](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) in tutte le pagine che visiti.

Le funzionalità di Shields possono essere ridotte per ogni sito se necessario; ciò nonostante, raccomandiamo le seguenti impostazioni:

<div class="annotate" markdown>

- [x] Selezionare **Aggressivo** sotto *Blocco dei tracciatori e degli annunci*

<details class="warning" markdown>
<summary>Utilizza gli elenchi di filtri predefiniti</summary>

Brave consente di selezionare filtri aggiuntivi per i contenuti nella pagina interna `brave://adblock`. Sconsigliamo questa funzionalità; piuttosto, mantieni gli elenchi di filtri predefiniti. Utilzzare ulteriori elenchi ti distinguerà dagli altri utenti di Brave e potrebbe inoltre incrementare la superficie di attacco, se è presente un exploit su Brave e una regola dannosa viene aggiunta a uno degli elenchi che utilizzi.

</details>

- [x] Selezionare **Strict** sotto *Aggiornamento delle connessioni a HTTPS*
- [x] (Opzionale) Selezionare **Blocca Scripts** (1)
- [x] Spuntare **Blocca fingerprinting**
- [x] Selezionare **Blocca cookies di terze parti**
- [x] Spuntare **Dimenticami quando chiudo questo sito** (2)
- [ ] Deselezionare tutti i componenti dei social media

</div>

1. Questa opzione disabilita JavaScript, il che porterà al malfunzionamento di molti siti. Per risolvere il problema, è possibile impostare eccezioni per ogni sito facendo clic sull'icona dello scudo nella barra degli indirizzi e deselezionando questa impostazione in *Controlli avanzati*.
2. Se desideri mantenere l'accesso in un particolare sito che visiti spesso, puoi selezionare le eccezioni per ogni sito cliccando sull'icona dello scudo sulla barra degli indirizzi in *Controlli avanzati*.

#### Privacy e sicurezza

<div class="annotate" markdown>

- [x] Selezionare **Non consentire ai siti di utilizzare l'ottimizzatore V8** in *Sicurezza* → *Gestione della sicurezza V8* (1)
- [x] Selezionare **Rimuovi automaticamente le autorizzazioni dai siti non utilizzati** in *Impostazioni siti e schermature*
- [x] Selezionare **Disabilita UDP nonUDP non proxied** in [*Politiche di gestione IP WebRTC*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Deselezionare **Usa dei servizi Google per la messaggistica push**
- [x] Selezionare **Auto-redirect delle pagine AMP**
- [x] Selezionare **Auto-redirect degli URL di tracciamento**
- [x] Selezionare **Impedire ai siti di rilevare le mie impronte digitali in base alle mie preferenze linguistiche**

</div>

1. Disabilitando l'ottimizzatore V8 si ridurrà la superficie di attacco inibendo [*alcune*](https://grapheneos.social/@GrapheneOS/112708049232710156) parti della compilazione Just-In-Time (JIT) di JavaScript.

##### Finestre di TOR

[**Finestra privata con Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) consente di instradare il traffico attraverso la rete Tor in Finestre private e di accedere ai servizi .onion, il che può essere utile in alcuni casi. Brave **non è** resistente al fingerprinting come Tor Browser e molte meno persone utilizzano Brave con Tor, facendoti quindi riconoscere. Se il vostro modello di minaccia richiede un forte anonimato, utilizzate [Tor Browser](tor.md#tor-browser).

##### Raccolta dati

- [ ] Deseleziona **Acconsenti all'analisi dei prodotti di tutela della privacy (P3A)**
- [ ] Deseleziona **Invia automaticamente un ping di utilizzo giornaliero a Brave**
- [ ] Deseleziona **Inviare automaticamente i rapporti di diagnostica**

#### Web3

Le funzionalità Web3 di Brave possono potenzialmente aumentare il fingerprint del browser e la superficie di attacco. A meno che non si utilizzi una di queste funzioni, devono essere disattivate.

- Selezionare **Estensioni** sotto *Portafoglio Ethereum predefinito*
- Selezionare **Estensioni** sotto *Portafoglio Solana predefinito*

#### Estensioni

- [ ] Deselezionare tutte le estensioni integrate che non si utilizzano

#### Motore di ricerca

Si consiglia di disabilitare i suggerimenti di ricerca in Brave per lo stesso motivo per cui si consiglia di disabilitare questa funzione in [Firefox](#search).

- [ ] Disabilita **Visualizza suggerimenti di ricerca**

#### Sistema

<div class="annotate" markdown>

- [ ] Rimuovi la spunta da **Continua a eseguire applicazioni in background dopo la chiusura di Brave** per disabilitare le applicazioni in background (1)

</div>

1. Questa opzione non è presente su tutte le piattaforme.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) consente ai tuoi dati di navigazione (cronologia, segnalibri, ecc.) di essere accessibili su tutti i dispositivi, senza richiedere un profilo e li protegge con l'E2EE.

#### Brave Ricompense e Portafoglio di Brave

**Brave Ricompense** ti consente di ricevere la criptovaluta Basic Attention Token (BAT) per l'esecuzione di certe azioni su Brave. Si basa su un conto di deposito e sul KYC di un numero selezionato di fornitori. Sconsigliamo BAT come [criptovaluta privata](cryptocurrency.md), né consigliamo l'utilizzo di un [portafoglio di custodia](advanced/payments.md#wallet-custody).

**Portafoglio di Brave** opera localmente sul tuo computer, ma non supporta nessuna criptovaluta privata, quindi, sconsigliamo l'utilizzo di questa funzione.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

### Requisiti minimi

- Deve essere un software open source.
- Deve supportare gli aggiornamenti automatici.
- Deve ricevere gli aggiornamenti del motore di rendering in 0-1 giorni dal rilascio a monte.
- Deve essere disponibile su Linux, macOS e Windows.
- Qualsiasi modifica necessaria per rendere il browser più rispettoso della privacy non dovrebbe influenzare negativamente l'esperienza degli utenti.
- Deve bloccare i cookie di terze parti di default.
- Deve supportare il [partizionamento degli stati](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) per mitigare il tracciamento cross-site.[^1]

### Miglior Caso

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- Dovrebbe includere una funzionalità di blocco dei contenuti integrata.
- Dovrebbe supportare la compartimentazione dei cookie (come nei [Contenitori a Profilo Multiplo](https://support.mozilla.org/en-US/kb/containers)).
- Dovrebbe supportare le Applicazioni Web Progressive (PWA). Le PWA consentono di installare determinati siti web come se fossero applicazioni native sul computer. Ciò può comportare vantaggi rispetto all'installazione di app basate su Electron, poiché le PWA beneficiano degli aggiornamenti di sicurezza del tuo browser.
- Non dovrebbe includere funzionalità aggiuntive (bloatware) che non influiscono sulla privacy dell'utente.
- Non dovrebbe ricevere telemetria di default.
- Dovrebbe fornire una sincronizzazione con il server Open-Source.
- Dovrebbe essere predefinito un motore di ricerca privato [](search-engines.md).

[^1]: L'implementazione di Brave è descritta in dettaglio in [Brave Privacy Updates: Partizionamento dello stato della rete per la privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
