---
meta_title: "Privacy Respecting Web Browsers for Android and iOS - Privacy Guides"
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
      - iOS
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

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Capitalismo di sorveglianza](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our currently recommended **mobile web browsers** and configurations for standard/non-anonymous internet browsing. Se hai bisogno di navigare in Internet in modo anonimo, dovresti invece usare [Tor](tor.md).

## Brave

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
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

### Configurazione consigliata di Brave

Il Tor Browser è l'unico che veramente permette di navigare Internet anonimamente. Quando utilizzi Brave, consigliamo di modificare le seguenti informazioni per proteggere la tua privacy da certe parti, ma tutti i browser tranne [Tor Browser](tor.md#tor-browser) saranno tracciabili da *qualcuno*, in un modo o nell'altro.

=== "Android"

    These options can be found in :material-menu: → **Settings** → **Brave Shields & privacy**.

=== "iOS"

    These options can be found in :fontawesome-solid-ellipsis: → **Settings** → **Shields & Privacy**.

#### Brave shields global defaults

Brave include delle misure anti-impronta digitale nella sua funzionalità, [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Suggeriamo di configurare queste opzioni [globalmente](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) tra tutte le pagine che visiti.

Le funzionalità di Shields possono essere ridotte per ogni sito se necessario; ciò nonostante, raccomandiamo le seguenti impostazioni:

=== "Android"

    <div class="annotate" markdown>

    - [x] Select **Aggressive** under *Block trackers & ads*
    - [x] Select **Auto-redirect AMP pages**
    - [x] Select **Auto-redirect tracking URLs**
    - [x] Select **Require all connections to use HTTPS (strict)** under *Upgrade connections to HTTPS*
    - \[x\] (Optional) Select **Block Scripts** (1)
    - [x] Select **Block third-party cookies** under *Block Cookies*
    - [x] Select **Block Fingerprinting**
    - [x] Select **Prevent fingerprinting via language settings**

    <details class="warning" markdown>
    <summary>Use default filter lists</summary>

    Brave allows you to select additional content filters within the **Content Filtering** menu or the internal `brave://adblock` page. Sconsigliamo di utilizzare questa funzionalità; piuttosto, mantieni gli elenchi di filtri predefiniti. Utilizzare ulteriori elenchi ti distinguerà dagli altri utenti di Brave e potrebbe inoltre incrementare la superficie di attacco, se è presente un exploit su Brave e una regola dannosa viene aggiunta a uno degli elenchi che utilizzi.

    </details>

    - [x] Select **Forget me when I close this site**

    </div>

    1. This option disables JavaScript, which will break a lot of sites. To unbreak them, you can set exceptions on a per-site basis by tapping on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

=== "iOS"

    <div class="annotate" markdown>

    - [x] Select **Aggressive** under *Trackers & Ads Blocking*
    - [x] Select **Strict** under *Upgrade Connections to HTTPS*
    - [x] Select **Auto-Redirect AMP pages**
    - [x] Select **Auto-Redirect Tracking URLs**
    - \[x\] (Optional) Select **Block Scripts** (1)
    - [x] Select **Block Fingerprinting**

    <details class="warning" markdown>
    <summary>Use default filter lists</summary>

    Brave allows you to select additional content filters within the **Content Filtering** menu. Sconsigliamo di utilizzare questa funzionalità; piuttosto, mantieni gli elenchi di filtri predefiniti. Utilizzare ulteriori elenchi ti distinguerà dagli altri utenti di Brave e potrebbe inoltre incrementare la superficie di attacco, se è presente un exploit su Brave e una regola dannosa viene aggiunta a uno degli elenchi che utilizzi.

    </details>

    </div>

    1. This option disables JavaScript, which will break a lot of sites. To unbreak them, you can set exceptions on a per-site basis by tapping on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

##### Clear browsing data (Android only)

- [x] Seleziona **Cancella dati all'uscita**

##### Social Media Blocking (Android only)

- [ ] Rimuovi la spunta da tutti i componenti social

#### Other privacy settings

=== "Android"

    <div class="annotate" markdown>

    - [x] Select **Disable non-proxied UDP** under [*WebRTC IP handling policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
    - \[x\] (Optional) Select **No protection** under *Safe Browsing* (1)
    - [ ] Uncheck **Allow sites to check if you have payment methods saved**
    - [x] Select **Close tabs on exit**
    - [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
    - [ ] Uncheck **Automatically send diagnostic reports**
    - [ ] Uncheck **Automatically send daily usage ping to Brave**

    </div>

    1. Brave's [implementation of Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) on Android **does not** proxy [Safe Browsing network requests](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) like its desktop counterpart. This means that your IP address may be seen (and logged) by Google. Note that Safe Browsing is not available for Android devices without Google Play Services.

=== "iOS"

    - [ ] Uncheck **Allow Privacy-Preserving Product Analytics (P3A)**
    - [ ] Uncheck **Automatically send daily usage ping to Brave**

### Leo

These options can be found in :material-menu: → **Settings** → **Leo**.

<div class="annotate" markdown>

- [ ] Uncheck **Show autocomplete suggestions in address bar** (1)

</div>

1. This option is not present in Brave's iOS app.

### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) consente ai tuoi dati di navigazione (cronologia, segnalibri, ecc.) di essere accessibili su tutti i dispositivi, senza richiedere un profilo e li protegge con l'E2EE.

## Mull (Android)

<div class="admonition recommendation" markdown>

![Logo Mull](assets/img/browsers/mull.svg){ align=right }

**Mull** è un browser Android orientato alla privacy e deblobbed, basato su Firefox. Rispetto a Firefox, offre una maggiore protezione dalle impronte digitali e disabilita la compilazione di JavaScript Just-in-Time (JIT) per una maggiore sicurezza. Inoltre, rimuove tutti gli elementi proprietari da Firefox, come la sostituzione dei riferimenti a Google Play Services.

[:octicons-home-16: Pagina Principale](https://divestos.org/pages/our_apps#mull){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://divestos.org/pages/browsers#tuningFenix){ .card-link title=Documentazione }
[:octicons-code-16:](https://codeberg.org/divested-mobile/mull-fenix){ .card-link title="Codice Sorgente" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-fdroid: F-Droid](https://f-droid.org/it/packages/us.spotco.fennec_dos/)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Attenzione</p>

I browser basati su Firefox (Gecko) su Android [non dispongono](https://bugzilla.mozilla.org/show_bug.cgi?id=1610822) dell' [isolamento dei siti](https://wiki.mozilla.org/Project_Fission),[^1] una potente funzione di sicurezza che protegge da un sito dannoso che esegue un attacco simile a [Spectre](https://it.wikipedia.org/wiki/Spectre_(vulnerabilità_di_sicurezza))per accedere alla memoria di un altro sito web che hai aperto.[^2] I browser basati su Chromium come [Brave](#brave) forniscono una protezione più solida contro i siti web dannosi.

</div>

Enable DivestOS's [F-Droid repository](https://divestos.org/fdroid/official) to receive updates directly from the developer. Scaricando Mull dal repository predefinito di F-Droid, i tuoi aggiornamenti potrebbero ritardare di qualche giorno o più.

Mull abilita molte delle funzionalità sviluppate dal [progetto Tor uplift](https://wiki.mozilla.org/Security/Tor_Uplift) utilizzando le preferenze di [Arkenfox](desktop-browsers.md#arkenfox-advanced). I blob proprietari vengono rimossi dal codice di Mozilla utilizzando gli script sviluppati per Fennec F-Droid.

### Recommended Mull Configuration

Suggeriamo di installare [uBlock Origin](browser-extensions.md#ublock-origin) come blocco dei contenuti se si desidera bloccare i tracker all'interno di Mull.

Mull è dotato di impostazioni di protezione della privacy configurate di default. Si può prendere in considerazione la possibilità di configurare l'opzione **Elimina dati di navigazione all'uscita ** nelle impostazioni di Mull, se si desidera chiudere automaticamente tutte le schede aperte all'uscita dell'applicazione, oppure cancellare automaticamente altri dati come la cronologia di navigazione e i cookie.

Poiché Mull ha attivato come impostazione predefinita protezioni della privacy più avanzate e rigorose rispetto alla maggior parte dei browser, alcuni siti web potrebbero non essere caricati o funzionare correttamente se non si regolano le impostazioni. È possibile consultare questo [elenco di problemi e soluzioni note](https://divestos.org/pages/broken#mull) per ottenere consigli su una possibile soluzione se incontri un sito non funzionante. La regolazione di un'impostazione per correggere un sito web potrebbe avere un impatto sulla tua privacy/sicurezza, quindi assicurati di aver compreso appieno le istruzioni che segui.

## Safari (iOS)

Su iOS, qualsiasi app che possa navigare sul web è [limitata](https://developer.apple.com/app-store/review/guidelines) all'utilizzo di un [quadro WebKit](https://developer.apple.com/documentation/webkit) fornito da Apple, quindi, non ci sono molti motivi per utilizzare un browser web di terze parti.

<div class="admonition recommendation" markdown>

![Logo di Safari](assets/img/browsers/safari.svg){ align=right }

**Safari** è il browser predefinito di iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Privacy Report, isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites so more devices look identical) as well as fingerprint randomization, and Private Relay for those with a paid iCloud+ subscription. It also allows you to separate your browsing with different profiles and lock private tabs with your biometrics/PIN.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title=Documentation}

</details>

</div>

### Configurazione consigliata di Safari

We would suggest installing [AdGuard](browser-extensions.md#adguard) if you want a content blocker in Safari.

Le seguenti opzioni, relative alla privacy/sicurezza, sono disponibili nell'app :gear: **Impostazioni** → **Safari**

#### Profili

Tutti i cookie, la cronologia e i dati del sito web saranno separati per ogni profilo. È consigliabile utilizzare profili diversi per scopi diversi, ad esempio per lo shopping, il lavoro o la scuola.

#### Privacy e sicurezza

- [x] Abilita **Impedisci Tracciamento Tra Siti**

    Ciò abilita la [Protezione Intelligente dal Tracciamento](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp) di WebKit. La funzionalità aiuta a proteggere dal tracciamento indesiderato utilizzando l'apprendimento automatico su dispositivo per bloccare i tracciatori. ITP protegge da molte minacce comuni, ma non blocca tutte le vie di tracciamento, poiché è progettata per non interferire con l'utilizzabilità del sito web.

- [x] Abilita **Richiedi il Face ID per sbloccare la navigazione privata**

    Questa impostazione consente di bloccare le schede private dietro la biometria/PIN quando non vengono utilizzate.

#### Avanzate → Privacy

L'impostazione **Protezione avanzata da tracciamento e fingerprinting** randomizza alcuni valori in modo che sia più difficile ottenere la tua fingerprint:

- [x] Seleziona **Tutto il browsing** o **Browsing Privato**

#### Rapporto sulla Privacy

Il Rapporto sulla Privacy fornisce un'istantanea dei tracciatori tra siti cui è al momento impedito profilarti, sul sito web che stai visitando. Inoltre, può mostrare un rapporto settimanale, per mostrare quali tracciatori sono stati bloccati nel tempo.

Il Rapporto sulla Privacy è accessibile tramite il menu Impostazioni della Pagina.

#### Misurazione degli Annunci a Tutela della Privacy

- [ ] Disabilita la **Misurazione della pubblicità che tutela la privacy**

Tradizionalmente, la misurazione dei click sugli annunci ha utilizzato la tecnologia di tracciamento, che viola la privacy degli utenti. La [misurazione privata dei clic](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) è una funzione di WebKit e uno standard web proposto per consentire agli inserzionisti di misurare l'efficacia delle campagne web senza compromettere la privacy degli utenti.

Questa, presenta poche preoccupazioni sulla privacy, quindi, sebbene tu possa scegliere di lasciarla attiva, consideriamo il fatto che sia automaticamente disabilitata per la Navigazione Privata, come un segnale per disabilitarla.

#### Navigazione privata sempre attiva

Apri Safari e tocca sul pulsante Schede, nell'angolo inferiore destro. Quindi, espandi l'elenco dei Gruppi di Schede.

- [x] Seleziona **Privata**

La modalità di Navigazione Privata di Safari offre ulteriori protezioni della privacy. La Navigazione Privata utilizza una nuova sessione [effimera](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) per ogni scheda, a significare che le schede sono isolate l'una dall'altra. Inoltre, la Navigazione Privata, presenta altri piccoli benefici per la privacy, come il mancato invio dell'indirizzo di una pagina web ad Apple, utilizzando la funzionalità di traduzione di Safari.

Nota che la Navigazione Privata non salva i cookie e dati dei siti web, quindi, non sarà possibile rimanere connesso ai siti. Ciò può essere sconveniente.

#### Sincronizzazione iCloud

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
