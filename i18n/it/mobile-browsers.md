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
    url: https://apple.com/safari
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

Questi sono i browser e le configurazioni che attualmente consigliamo per la navigazione standard/non anonima. Se hai bisogno di navigare in Internet in modo anonimo, dovresti invece usare [Tor](tor.md). In generale, consigliamo di mantenere al minimo il numero delle estensioni; hanno accesso privilegiato al tuo browser, ti richiedono di fidarti degli sviluppatori, possono [distinguerti](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint) e [indebolire](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) l'isolamento del sito.

## Android

On Android, Firefox is still less secure than Chromium-based alternatives: Mozilla's engine, [GeckoView](https://mozilla.github.io/geckoview), has yet to support [site isolation](https://hacks.mozilla.org/2021/05/introducing-firefox-new-site-isolation-security-architecture) or enable [isolatedProcess](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196).

### Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave si basa sul progetto del browser web di Chromium, quindi, dovrebbe sembrare familire e avere problemi di compatibilità minimali con i siti web.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

#### Configurazione consigliata

Il Tor Browser è l'unico che veramente permette di navigare Internet anonimamente. Quando utilizzi Brave, consigliamo di modificare le seguenti informazioni per proteggere la tua privacy da certe parti, ma tutti i browser tranne [Tor Browser](tor.md#tor-browser) saranno tracciabili da *qualcuno*, in un modo o nell'altro.

Queste opzioni si possono trovare in :material-menu: → **Impostazioni** → **Protezioni Brave e privacy**

##### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

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

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net) extension.

##### Cancella dati di navigazione

- [x] Seleziona **Cancella dati all'uscita**

##### Blocco dei social media

- [ ] Rimuovi la spunta da tutti i componenti social

##### Altre impostazioni sulla privacy

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP handling policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Allow sites to check if you have payment methods saved**
- [ ] Uncheck **IPFS Gateway** (1)
- [x] Select **Close tabs on exit**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Automatically send daily usage ping to Brave**

</div>

1. L'InterPlanetary File System (IPFS) è una rete peer-to-peer e decentralizzata, utilizzata per archiviare e condividere dati in un filesystem distribuito. A meno che tu non utilizzi questa funziona, disabilitala.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

## iOS

Su iOS, qualsiasi app che possa navigare sul web è [limitata](https://developer.apple.com/app-store/review/guidelines) all'utilizzo di un [quadro WebKit](https://developer.apple.com/documentation/webkit) fornito da Apple, quindi, non ci sono molti motivi per utilizzare un browser web di terze parti.

### Safari

<div class="admonition recommendation" markdown>

![Logo di Safari](assets/img/browsers/safari.svg){ align=right }

**Safari** è il browser predefinito di iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Privacy Report, isolated and ephemeral Private Browsing tabs, iCloud Private Relay, fingerprinting protection by randomizing and presenting a simplified version of the system configuration to websites so more devices look identical, and the ability to lock private tabs with your biometrics/PIN. Consente inoltre di separare la navigazione con profili diversi.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentation}

</details>

</div>

#### Configurazione consigliata

Queste opzioni si trovano in :gear: **Impostazioni** → **Safari**

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

Tradizionalmente, la misurazione dei click sugli annunci ha utilizzato la tecnologia di tracciamento, che viola la privacy degli utenti. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

Questa, presenta poche preoccupazioni sulla privacy, quindi, sebbene tu possa scegliere di lasciarla attiva, consideriamo il fatto che sia automaticamente disabilitata per la Navigazione Privata, come un segnale per disabilitarla.

##### Navigazione privata sempre attiva

Apri Safari e tocca sul pulsante Schede, nell'angolo inferiore destro. Quindi, espandi l'elenco dei Gruppi di Schede.

- [x] Seleziona **Privata**

La modalità di Navigazione Privata di Safari offre ulteriori protezioni della privacy. La Navigazione Privata utilizza una nuova sessione [effimera](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) per ogni scheda, a significare che le schede sono isolate l'una dall'altra. Inoltre, la Navigazione Privata, presenta altri piccoli benefici per la privacy, come il mancato invio dell'indirizzo di una pagina web ad Apple, utilizzando la funzionalità di traduzione di Safari.

Nota che la Navigazione Privata non salva i cookie e dati dei siti web, quindi, non sarà possibile rimanere connesso ai siti. Ciò può essere sconveniente.

##### Sincronizzazione iCloud

La sincronizzazione della Cronologia di Safari, dei Gruppi di Schede, delle Schede di iCloud e delle password salvate, avviene E2EE. However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://apple.com/legal/privacy/en-ww).

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/HT212520). Vai al tuo **nome ID Apple → iCloud → Protezione Avanzata dei Dati**.

- [x] Attiva la **Protezione Avanzata dei Dati**

Se utilizzi iCloud con la Protezione Avanzata dei Dati disabilitata, consigliamo inoltre di verificare e assicurarsi che la posizione di download predefinita di Safari, sia impostata localmente sul tuo dispositivo. Questa opzione si trova in :gear: **Impostazioni** → **Safari** → **Generale** → **Download**.

### AdGuard

<div class="admonition recommendation" markdown>

![Logo di AdGuard](assets/img/browsers/adguard.svg){ align=right }

**AdGuard per iOS** è un'estensione per il blocco dei contenuti gratuita e open source per Safari che utilizza l'[API di Blocco dei Contenuti](https://developer.apple.com/documentation/safariservices/creating_a_content_blocker) integrata.

AdGuard per iOS presenta delle funzionalità premium; tuttavia, il blocco di contenuti standard di Safari è gratuito.

[:octicons-home-16: Homepage](https://adguard.com/en/adguard-ios/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/ios.html){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1047223162)

</details>

</div>

Ulteriori elenchi di filtri potrebbero rallentare le prestazioni e incrementare la tua superficie d'attacco, quindi, applica soltanto quelli necessari.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcuno dei progetti consigliati.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questi elenchi, prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta migliore per te.

<div class="admonition example" markdown>
<p class="admonition-title">Questa sezione è nuova</p>

Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

</div>

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
