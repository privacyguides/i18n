---
meta_title: "Browser web che rispettano la privacy per Android e iOS - Privacy Guides"
title: "Browser mobile"
icon: material/cellphone-information
description: Questi sono i browser consigliati al momento per la navigazione standard/non anonima sul tuo telefono.
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Consigli sui browser privati per cellulare
    url: "./"
    relatedLink: "../desktop-browsers/"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    applicationCategory: Web Browser
    operatingSystem:
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://www.apple.com/safari/
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

Questi sono i web browser consigliati al momento e le configurazioni per la navigazione standard/non anonima su Interrnet. Se hai bisogno di navigare in Internet in modo anonimo, dovresti invece usare [Tor](tor.md). In generale, consigliamo di mantenere al minimo il numero delle estensioni; hanno accesso privilegiato al tuo browser, ti richiedono di fidarti degli sviluppatori, possono [distinguerti](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint) e [indebolire](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) l'isolamento del sito.

## Android

Per Android, Firefox è meno sicuro delle alternative basate su Chromium: il motore di Mozilla, [GeckoView](https://mozilla.github.io/geckoview/), non supporta ancora [l'isolamento dei siti](https://hacks.mozilla.org/2021/05/introducing-firefox-new-site-isolation-security-architecture) e non ha abilitato [l'isolatedProcess](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196).

### Brave

!!! recommendation

    ![Logo di Brave](assets/img/browsers/brave.svg){ align=right }
    
    **Brave Browser** include un blocco di contenuti e [funzionalità per la privacy](https://brave.com/privacy-fetures/), molte delle quali abilitate di default.
    
    Brave si basa sul progetto del browser web di Chromium, quindi, dovrebbe sembrare familire e avere problemi di compatibilità minimali con i siti web.
    
    [:octicons-home-16: Homepage](https://brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }
    
    ??? downloads annotate "Scarica"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

#### Configurazione consigliata

Il Tor Browser è l'unico che veramente permette di navigare Internet anonimamente. Qundo utilizzi Brave, consigliamo di modificare le seguenti informazioni per proteggere la tua privacy da certe parti, m tutti i browser tranne [Tor Browser](tor.md#tor-browser) saranno tracciabili da *qualcuno*, in un modo o nell'altro.

Queste opzioni si possono trovare in :material-menu: → **Impostazioni** → **Protezioni Brave e privacy**

##### Shields

Brave include alcune misure contro il fingerprinting nella sua funzionalità [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-). Suggeriamo di configurarle [globalmente](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) tra tutte le pagine che visiti.

##### Valori predefiniti globali di Brave Shields

Le opzioni di Shields sono riducibili a seconda del sito come necessrio ma, di default, consigliamo impostarle come segue:

<div class="annotate" markdown>

- [x] Seleziona **Aggressivo** sotto **Blocca tracker e annunci**

??? warning "Usa gli elenchi di filtri predefiniti"
        Brave ti consente di selezionare ulteriori filtri di contenuti mediante la pagina interna `brave://adblock`. Si consiglia di non utilizzare questa funzione e di mantenere gli elenchi di filtri predefiniti. Utilzzare ulteriori elenchi ti distinguerà dagli altri utenti di Brave e potrebbe inoltre incrementare la superficie di attacco, se è presente un exploit su Brave e una regola dannosa viene aggiunta a uno degli elenchi che utilizzi.

- [x] Seleziona **Aggiorna le connessioni a HTTPS**
- [x] Seleziona **Utilizza sempre connessioni sicure**
- [x] (Facoltativo) Seleziona **Blocca gli Script** (1)
- [x] Seleziona **Rigido, potrebbe corrompere alcuni siti** in **Blocca il fingerprinting**

</div>

1. Quest'opzione fornisce una funzionalità simile alle [modalità di blocco](https://github.com/gorhill/uBlock/wiki/Blocking-mode) avanzata di uBlock Origin o all'estensione [NoScript](https://noscript.net/).

##### Cancella dati di navigazione

- [x] Seleziona **Cancella dati all'uscita**

##### Blocco dei social media

- [ ] Rimuovi la spunta da tutti i componenti social

##### Altre impostazioni sulla privacy

<div class="annotate" markdown>

- [x] Seleziona **Disabilita UDP senza proxy** nella [Gestione Politca IP WebRTC](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-chaange-my-Privacy-Settings-#webrtc)
- [ ] Rimuovi la spunta da "Consenti ai siti di controllare se hai metodi di pagamento salvati**
- [ ] Rimuovi la spunta da **Gateway IPFS** (1)
- [x] Seleziona **Chiudi le schede quando esci**
- [ ] Rimuovi la spunta da **Acconsenti all'analisi dei prodotti di tutela della privacy (P3A)**
- [ ] Rimuovi la spunta da **Invia automaticamente i rapporti di diagnostica**
- [ ] Rimuovi la spunta da **Invia automaticamente un ping di utilizzo giornaliero a Brave**

</div>

1. L'InterPlanetary File System (IPFS) è una rete peer-to-peer e decentralizzata, utilizzata per archiviare e condividere dati in un filesystem distribuito. A meno che tu non utilizzi questa funziona, disabilitala.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) consente ai tuoi dati di navigazione (cronologia, segnalibri, ecc.) di essere accessibili su tutti i dispositivi, senza richiedere un profilo e li protegge con l'E2EE.

## iOS

Su iOS, qualsiasi app che possa navigare sul web è [limitata](https://developer.apple.com/app-store/review/guidelines) all'utilizzo di un [quadro WebKit](https://developer.apple.com/documentation/webkit) fornito da Apple, quindi, non ci sono molti motivi per utilizzare un browser web di terze parti.

### Safari

!!! recommendation

    ![Logo di Safari](assets/img/browsers/safari.svg){ align=right }
    
    **Safari** è il browser web predefinito di iOS. Include [funzionalità per la privacy](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0) come la [Prevenzione Intelligente del Tracciamento](https://webkit.org/blog/7675/intelligent-tracking-prevention/), Rapporti sulla Privacy, schede di Navigazione Privaata isolate ed effimere, Trasmissione Privata su iCloud e riduzione del fingerprinting, presentando una versione semplice della configurzione di sistema ai siti web, così che più dispositivi appaiano identici.
    
    [:octicons-home-16: Homepage](https://www.apple.com/safari/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.apple.com/legal/privacy/data/en/safari/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentation}

#### Configurazione consigliata

Queste opzioni si possono trovare in :gear: **Impostazioni** → **Safari** → **Privacy e Sicurezza**.

##### Prevenzione del Tracciamento Tra Siti

- [x] Abilita **Impedisci Tracciamento Tra Siti**

Ciò abilita la [Protezione Intelligente dal Tracciamento](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp) di WebKit. La funzionalità iuta a proteggere dal tracciamento indesiderato utilizzndo l'apprendimento automatico su dispositivo per bloccare i tracciatori. ITP protegge da molte minacce comuni, ma non blocca tutte le vie di tracciamento, poiché è progettta per non interferire con l'utilizzabilità del sito web.

##### Rapporto sulla Privacy

Il Rapporto sulla Privacy fornisce un'istantanea dei tracciatori tra siti cui è al momento impedito profilarti, sul sito web che stai visitando. Inoltre, può mostrare un rapporto settimanale, per mostrare quali tracciatori sono stati bloccati nel tempo.

Il Rapporto sulla Privacy è accessibile tramite il menu Impostazioni della Pagina.

##### Misurazione degli Annunci a Tutela della Privacy

- [ ] Disabilita la **Misurazione della pubblicità che tutela la privacy**

Tradizionalmente, la misurazione dei click sugli annunci ha utilizzato la tecnologia di tracciamento, che viola la privacy degli utenti. La [Misurazione Privata dei Click](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm/) è una funzionalità di WebKit, nonché uno standrd web proposto, incentrato al consentire agli inserzionisti di misurare l'efficacia delle campagne web senza compromettere la privacy dell'utente.

Questa, presenta poche preoccupazioni sulla privacy, quindi, sebbene tu possa scegliere di lasciarla attiva, consideriamo il fatto che sia automaticamente disabilitata per la Navigazione Privata, come un segnale per disabilitarla.

##### Navigazione privata sempre attiva

Apri Safari e tocca sul pulsante Schede, nell'angolo inferiore destro. Quindi, espandi l'elenco dei Gruppi di Schede.

- [x] Seleziona **Privata**

La modalità di Navigazione Privata di Safri offre ulteriori protezioni della privacy. La Navigazione Privata utilizza una nuova sessione [effimera](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) per ogni scheda, a significare che le schede sono isolate l'una dall'altra. Inoltre, la Navigazione Privata, presenta altri piccoli benefici per la privacy, come il mancato invio dell'indirizzo di una pagina web ad Apple, utilizzando la funzionalità di traduzione di Safari.

Nota che la Navigazione Privata non salva i cookie e dati dei siti web, quindi, non sarà possibile rimanere connesso ai siti. Ciò potrebbe creare disturbo.

##### Sincronizzazione iCloud

La sincronizzazione della Cronologia di Safari, dei Gruppi di Schede, delle Schede di iCloud e delle password salvate, avviene in E2EE. Tuttavia, di default, i segnalibri [non](https://support.apple.com/en-us/HT202303) la prevedono. Apple può decrittografarli e accedervi, in conformità con la sua [politica sulla privacy](https://www.apple.com/legal/privacy/en-ww/).

Puoi abilitare la E2EE per i tuoi segnalibri e i download di Safari attivando la [Protezione avanzata dei dati](https://support.apple.com/it-it/HT212520). Vai al tuo **nome ID Apple → iCloud → Protezione Avanzata dei Dati**.

- [x] Attiva la **Protezione Avanzata dei Dati**

Se utilizzi iCloud con la Protezione Avanzata dei Dati disabilitata, consigliamo inoltre di verificare e assicurarsi che la posizione di download predefinita di Safari, sia impostata localmente sul tuo dispositivo. Questa opzione si trova in :gear: **Impostazioni** → **Safari** → **Generale** → **Download**.

### AdGuard

!!! recommendation

    ![Logo di AdGuard](assets/img/browsers/adguard.svg){ align=right }
    
    **AdGuard per iOS** è un'estensione per il blocco dei contenuti gratuita e open source per Safari che utilizza l'[API di Blocco dei Contenuti](https://developer.apple.com/documentation/safariservices/creating_a_content_blocker) integrata.
    
    AdGuard per iOS presenta delle funzionalità premium; tuttavia, il blocco di contenuti standard di Safari è gratuito.
    
    [:octicons-home-16: Homepage](https://adguard.com/en/adguard-ios/overview.html){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://adguard.com/privacy/ios.html){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="Source Code" }
    
    ??? downloads "Scarica"
    
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id1047223162)

Ulteriori elenchi di filtri potrebbero rallentare le prestazioni e incrementare la tua superficie d'attacco, quindi, applica soltanto quelli necessari.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcuno dei progetti consigliati.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questi elenchi, prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta migliore per te.

!!! esempio "Questa sezione è nuova"

    Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

### Requisiti minimi

- Deve supportare gli aggiornamenti automatici.
- Deve ricevere gli aggiornamenti del motore in 0-1 giorni dalla pubblicazione a monte.
- Qualsiasi modifica necessaria per rendere il browser più rispettoso della privacy non dovrebbe avere un impatto negativo sull'esperienza dell'utente.
- I browser Android devono utilizzare il motore Chromium.
    - Purtroppo, Mozilla GeckoView per ora è meno sicuro di Chromium su Android.
    - I browser iOS sono limitati a WebKit.

### Criteri delle estensioni

- Non deve replicare funzionalità integrate del browser o del sistema operativo.
- Deve influenzare direttamente la privacy dell'utente, cioè non deve semplicemente fornire informazioni.
