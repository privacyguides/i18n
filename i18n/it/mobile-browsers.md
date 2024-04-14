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
    name: Consigli sui browser privati per mobile
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
    url: https://www.apple.com/it/safari/
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

Questi sono i browser e le configurazioni che attualmente consigliamo per la navigazione standard/non anonima. Se hai bisogno di navigare in Internet in modo anonimo, dovresti invece usare [Tor](tor.md). In generale, consigliamo di mantenere al minimo il numero delle estensioni; hanno accesso privilegiato al tuo browser, ti richiedono di fidarti degli sviluppatori, possono [distinguerti](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint) e [indebolire](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) l'isolamento del sito.

## Android

### Brave

<div class="admonition recommendation" markdown>

![Logo di Brave](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** include un bloccatore dei contenuti integrato e [funzionalità per la privacy](https://brave.com/privacy-features), molte delle quali sono abilitate di default.

Brave si basa sul progetto del browser web di Chromium, quindi, dovrebbe sembrare familire e avere problemi di compatibilità minimali con i siti web.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Servizio Onion" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

#### Configurazione consigliata di Brave

Il Tor Browser è l'unico che veramente permette di navigare Internet anonimamente. Quando utilizzi Brave, consigliamo di modificare le seguenti informazioni per proteggere la tua privacy da certe parti, ma tutti i browser tranne [Tor Browser](tor.md#tor-browser) saranno tracciabili da *qualcuno*, in un modo o nell'altro.

Queste opzioni si possono trovare in :material-menu: → **Impostazioni** → **Protezioni Brave e privacy**

##### Shields

Brave include delle misure anti-impronta digitale nella sua funzionalità, [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Suggeriamo di configurare queste opzioni [globalmente](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) tra tutte le pagine che visiti.

##### Valori predefiniti globali di Brave Shields

Le funzionalità di Shields possono essere ridotte per ogni sito se necessario; ciò nonostante, raccomandiamo le seguenti impostazioni:

<div class="annotate" markdown>

- [x] Seleziona **Aggressivo** sotto **Blocca tracker e annunci**

<details class="warning" markdown>
<summary>Utilizza gli elenchi di filtri predefiniti</summary>

Brave consente di selezionare filtri aggiuntivi per i contenuti nella pagina interna `brave://adblock`. Sconsigliamo di utilizzare questa funzionalità; piuttosto, mantieni gli elenchi di filtri predefiniti. Utilizzare ulteriori elenchi ti distinguerà dagli altri utenti di Brave e potrebbe inoltre incrementare la superficie di attacco, se è presente un exploit su Brave e una regola dannosa viene aggiunta a uno degli elenchi che utilizzi.

</details>

- [x] Seleziona **Aggiorna le connessioni a HTTPS**
- [x] Seleziona **Utilizza sempre connessioni sicure**
- [x] (Facoltativo) Seleziona **Blocca gli Script** (1)
- [x] Seleziona **rigido, potrebbe non far funzionare alcuni siti** in **Blocca le impronte digitali**

</div>

1. Questa opzione fornisce una funzionalità simile alle [modalità di blocco](https://github.com/gorhill/uBlock/wiki/Blocking-mode) avanzate di uBlock Origin o all'estensione [NoScript](https://noscript.net).

##### Cancella dati di navigazione

- [x] Seleziona **Cancella dati all'uscita**

##### Blocco dei social media

- [ ] Rimuovi la spunta da tutti i componenti social

##### Altre impostazioni sulla privacy

<div class="annotate" markdown>

- [x] Seleziona **Disabilita l'UDP senza proxy** in [Gestione politica IP WebRTC](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Deseleziona **Consenti ai siti di controllare se hai metodi di pagamento salvati**
- [ ] Deseleziona **Gateway IPFS** (1)
- [x] Seleziona **Chiudi le schede quando esci**
- [ ] Deseleziona **Acconsenti all'analisi dei prodotto di tutela della privacy (P3A)**
- [ ] Deseleziona **Invia automaticamente i rapporti di diagnostica**
- [ ] Deseleziona **Invia automaticamente un ping di utilizzo giornaliero a Brave**

</div>

1. L'InterPlanetary File System (IPFS) è una rete peer-to-peer e decentralizzata, utilizzata per archiviare e condividere dati in un filesystem distribuito. A meno che tu non utilizzi questa funziona, disabilitala.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) consente ai tuoi dati di navigazione (cronologia, segnalibri, ecc.) di essere accessibili su tutti i dispositivi, senza richiedere un profilo e li protegge con l'E2EE.

### Mull

<div class="admonition danger" markdown>
<p class="admonition-title">Attenzione</p>

I browser basati su Firefox (Gecko) su Android [mancano l'isolamento dei processi per sito](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196), una potente funzione di sicurezza che offre una protezione aggiuntiva contro un sito web dannoso che sfrutta una vulnerabilità di sicurezza. La mancanza di questa funzione probabilmente non rappresenterà un problema per i browser web a basso rischio che mantengono il proprio browser aggiornato, ma coloro che visitano siti ad alto rischio o che sono a rischio di attacchi mirati/0-day dovrebbero prendere in considerazione un browser basato su Chromium come [Brave](#brave).

</div>

<div class="admonition recommendation" markdown>

![Logo Mull](assets/img/browsers/mull.svg){ align=right }

**Mull** è un browser Android orientato alla privacy e deblobbed, basato su Firefox. Rispetto a Firefox, offre una maggiore protezione dalle impronte digitali e disabilita la compilazione di JavaScript Just-in-Time (JIT) per una maggiore sicurezza. Inoltre, rimuove tutti gli elementi proprietari da Firefox, come la sostituzione dei riferimenti a Google Play Services.

[:octicons-home-16: Homepage](https://divestos.org/pages/our_apps#mull){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy){ .card-link title="Informatica sulla privacy" }
[:octicons-info-16:](https://divestos.org/pages/browsers#tuningFenix){ .card-link title=Documentazione }
[:octicons-code-16:](https://codeberg.org/divested-mobile/mull-fenix){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-fdroid: F-Droid](https://f-droid.org/it/packages/us.spotco.fennec_dos/)

</details>

</div>

Attiva [F-Droid Repo](https://divestos.org/fdroid/official) di DivestOS per ricevere gli aggiornamenti direttamente dallo sviluppatore. Scaricando Mull dalla repo predefinita di F-Droid, gli aggiornamenti potrebbero ritardare di qualche giorno o più.

Mull abilita molte delle funzionalità sviluppate dal [progetto Tor uplift](https://wiki.mozilla.org/Security/Tor_Uplift) utilizzando le preferenze di [Arkenfox](desktop-browsers.md#arkenfox-advanced). I blob proprietari vengono rimossi dal codice di Mozilla utilizzando gli script sviluppati per Fennec F-Droid.

#### Configurazione consigliata di Mull

Suggeriamo di installare [uBlock Origin](browser-extensions.md#ublock-origin) come blocco dei contenuti se si desidera bloccare i tracker all'interno di Mull.

Mull è dotato di impostazioni di protezione della privacy configurate di default. Si può prendere in considerazione la possibilità di configurare l'opzione **Elimina dati di navigazione all'uscita ** nelle impostazioni di Mull, se si desidera chiudere automaticamente tutte le schede aperte all'uscita dell'applicazione, oppure cancellare automaticamente altri dati come la cronologia di navigazione e i cookie.

## iOS

Su iOS, qualsiasi app che possa navigare sul web è [limitata](https://developer.apple.com/app-store/review/guidelines) all'utilizzo di un [quadro WebKit](https://developer.apple.com/documentation/webkit) fornito da Apple, quindi, non ci sono molti motivi per utilizzare un browser web di terze parti.

### Safari

<div class="admonition recommendation" markdown>

![Logo di Safari](assets/img/browsers/safari.svg){ align=right }

**Safari** è il browser predefinito di iOS. Include [funzioni per la privacy](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0) come [Prevenzione Intelligente del Tracciamento](https://webkit.org/blog/7675/intelligent-tracking-prevention), Report sulla Privacy, schede di navigazione privata isolate ed effimere, Relay privato iCloud, protezione delle impronte digitali attraverso la randomizzazione e la presentazione di una versione semplificata della configurazione del sistema ai siti web, in modo che più dispositivi appaiano identici, e la possibilità di bloccare le schede private con i propri dati biometrici/PIN. Consente inoltre di separare la navigazione con profili diversi.

[:octicons-home-16: Homepage](https://apple.com/it/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.apple.com/legal/privacy/data/it/safari/){ .card-link title="Informativa sulla privacy" }
[:octicons-info-16:](https://support.apple.com/it-it/guide/safari/welcome/mac){ .card-link title=Documentazione}

</details>

</div>

#### Configurazione consigliata di Safari

Suggeriamo di installare [AdGuard](browser-extensions.md#adguard) come blocco dei contenuti se si desidera bloccare i tracker in Safari.

Le seguenti opzioni, relative alla privacy/sicurezza, sono disponibili nell'app :gear: **Impostazioni** → **Safari**

##### Profili

Tutti i cookie, la cronologia e i dati del sito web saranno separati per ogni profilo. È consigliabile utilizzare profili diversi per scopi diversi, ad esempio per lo shopping, il lavoro o la scuola.

##### Privacy e sicurezza

- [x] Abilita **Impedisci Tracciamento Tra Siti**

    Ciò abilita la [Protezione Intelligente dal Tracciamento](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp) di WebKit. La funzionalità iuta a proteggere dal tracciamento indesiderato utilizzando l'apprendimento automatico su dispositivo per bloccare i tracciatori. ITP protegge da molte minacce comuni, ma non blocca tutte le vie di tracciamento, poiché è progettata per non interferire con l'utilizzabilità del sito web.

- [x] Abilita **Richiedi il Face ID per sbloccare la navigazione privata**

    Questa impostazione consente di bloccare le schede private dietro la biometria/PIN quando non vengono utilizzate.

##### Avanzate → Privacy

L'impostazione **Protezione avanzata da tracciamento e fingerprinting** randomizza alcuni valori in modo che sia più difficile ottenere la tua fingerprint:

- [x] Seleziona **Tutto il browsing** o **Browsing Privato**

##### Rapporto sulla Privacy

Il Rapporto sulla Privacy fornisce un'istantanea dei tracciatori tra siti cui è al momento impedito profilarti, sul sito web che stai visitando. Inoltre, può mostrare un rapporto settimanale, per mostrare quali tracciatori sono stati bloccati nel tempo.

Il Rapporto sulla Privacy è accessibile tramite il menu Impostazioni della Pagina.

##### Misurazione degli Annunci a Tutela della Privacy

- [ ] Disabilita la **Misurazione della pubblicità che tutela la privacy**

Tradizionalmente, la misurazione dei click sugli annunci ha utilizzato la tecnologia di tracciamento, che viola la privacy degli utenti. La [misurazione privata dei clic](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) è una funzione di WebKit e uno standard web proposto per consentire agli inserzionisti di misurare l'efficacia delle campagne web senza compromettere la privacy degli utenti.

Questa, presenta poche preoccupazioni sulla privacy, quindi, sebbene tu possa scegliere di lasciarla attiva, consideriamo il fatto che sia automaticamente disabilitata per la Navigazione Privata, come un segnale per disabilitarla.

##### Navigazione privata sempre attiva

Apri Safari e tocca sul pulsante Schede, nell'angolo inferiore destro. Quindi, espandi l'elenco dei Gruppi di Schede.

- [x] Seleziona **Privata**

La modalità di Navigazione Privata di Safari offre ulteriori protezioni della privacy. La Navigazione Privata utilizza una nuova sessione [effimera](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) per ogni scheda, a significare che le schede sono isolate l'una dall'altra. Inoltre, la Navigazione Privata, presenta altri piccoli benefici per la privacy, come il mancato invio dell'indirizzo di una pagina web ad Apple, utilizzando la funzionalità di traduzione di Safari.

Nota che la Navigazione Privata non salva i cookie e dati dei siti web, quindi, non sarà possibile rimanere connesso ai siti. Ciò può essere sconveniente.

##### Sincronizzazione iCloud

La sincronizzazione della Cronologia di Safari, dei Gruppi di Schede, delle Schede di iCloud e delle password salvate, avviene E2EE. Tuttavia, per impostazione predefinita, i segnalibri [non lo sono](https://support.apple.com/HT202303). Apple può decifrarli e accedervi in base alla propria [informativa sulla privacy](https://apple.com/legal/privacy/en-ww).

È possibile attivare E2EE per i segnalibri e i download di Safari attivando la [Protezione Avanzata dei Dati](https://support.apple.com/HT212520). Vai al tuo **nome ID Apple → iCloud → Protezione Avanzata dei Dati**.

- [x] Attiva la **Protezione Avanzata dei Dati**

Se utilizzi iCloud con la Protezione Avanzata dei Dati disabilitata, consigliamo inoltre di verificare e assicurarsi che la posizione di download predefinita di Safari, sia impostata localmente sul tuo dispositivo. Questa opzione si trova in :gear: **Impostazioni** → **Safari** → **Generale** → **Download**.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcuno dei progetti consigliati.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questi elenchi, prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta migliore per te.

### Requisiti minimi

- Deve supportare gli aggiornamenti automatici.
- Deve ricevere rapidamente gli aggiornamenti dalle release upstream.
- Deve supportare il blocco dei contenuti.
- Qualsiasi modifica necessaria per rendere il browser più rispettoso della privacy non dovrebbe avere un impatto negativo sull'esperienza dell'utente.
