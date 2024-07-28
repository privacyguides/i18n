---
meta_title: "Browser web che rispettano la privacy per PC e Mac - Privacy Guides"
title: "Browser desktop"
icon: material/laptop
description: These privacy-protecting browsers are what we currently recommend for standard/non-anonymous internet browsing on desktop systems.
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

These are our currently recommended **desktop web browsers** and configurations for standard/non-anonymous browsing. Consigliamo [Mullvad Browser](#mullvad-browser) se sei interessato a una forte protezione della privacy e all'anti-fingerprinting pronti all'uso, [Firefox](#firefox) per i navigatori occasionali di Internet alla ricerca di una buona alternativa a Google Chrome e [Brave](#brave), se necessiti della compatibilità del browser con Chromium.

Invece, se necessiti di navigare anonimamente su Internet, dovresti utilizzare [Tor](tor.md). In questa pagina forniamo alcune raccomandazioni sulla configurazione, ma tutti i browser diversi da Tor Browser saranno rintracciabili da *qualcuno* in un modo o nell'altro.

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** è una versione di [Tor Browser](tor.md#tor-browser) con le integrazioni della rete Tor rimosse, con l'obiettivo di fornire le tecnologie anti-fingerprinting di Tor Browser agli utenti che usano una VPN. Sviluppato dal Tor Project e distribuito da [Mullvad](vpn.md#mullvad), **non** richiede l'utilizzo della VPN di Mullvad.

[:octicons-home-16: Pagina Iniziale](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Politica sulla privacy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title=Documentazione}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Come [Tor Browser](tor.md), Mullvad Browser è progettato per impedire il fingerprinting, rendendo l'impronta digitale del tuo browser identica a quella di tutti gli altri suoi utenti, e include impostazioni ed estensioni predefinite, configurate automaticamente dai livelli di sicurezza predefiniti: *Standard*, *Safer* e *Safest*. Dunque, è fondamentale che tu non modifichi affatto il browser, se non per regolare i [livelli di sicurezza](https://tb-manual.torproject.org/security-settings) predefiniti. Altre modifiche renderebbero la tua impronta digitale univoca, vanificando lo scopo di utilizzare tale browser. Se desideri configurare il tuo browser in modo più completo e il fingerprinting non ti preoccupa, consigliamo invece [Firefox](#firefox).

### Anti-Fingerprinting

**Senza** utilizzare una [VPN](vpn.md), Mullvad Browser fornisce le stesse protezioni dai [semplici script di fingerprinting](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) di altri browser privati, come Firefox+[Arkenfox](#arkenfox-advanced) o [Brave](#brave). Mullvad Browser fornisce tali protezioni "pronte all'uso", a scapito di una certa flessibilità e comodità che altri browser privati possono fornire.

==Per la massima protezione anti-fingerprinting, consigliamo di utilizzare Mullvad Browser **con** una VPN==, che sia di Mullvad o di un altro fornitore di VPN consigliato. Utilizzando una VPN con Mullvad Browser, condividi un'impronta digitale e un gruppo di indirizzi IP con molti altri utenti, offrendoti una "folla" con cui confonderti. Questa strategia è l'unico modo per contrastare gli script di tracciamento avanzati ed è la stessa tecnica anti-fingerprinting utilizzata da Tor Browser.

Nota che, sebbene tu possa utilizzare Mullvad Browser con qualsiasi fornitore VPN, altre persone su tale VPN devono anch'esse utilizzare Mullvad Browser affinché tale "folla" esista, il che è molto più probabile su Mullvad VPN, rispetto ad altri fornitori, in particolare così a breve distanza dal lancio di Mullvad Browser. Mullvad Browser non dispone di connettività VPN integrata, né verifica che tu stia utilizzando una VPN prima di navigare; la tua connessione VPN dev'essere configurata e gestita separatamente.

Mullvad Browser contiene le estensioni pre-installate di *uBlock Origin* e *NoScript*. Anche se in genere sconsigliamo di aggiungere *ulteriori* [estensioni del browser](browser-extensions.md), quelle preinstallate **non** devono essere rimosse o configurate al di fuori dei valori predefiniti, perché in questo modo l'impronta digitale del browser si distinguerebbe notevolmente da quella degli altri utenti di Mullvad Browser. Inoltre, presenta l'Estensione Mullvad Browser pre-installata, che *può* essere rimossa in sicurezza, senza influenzare l'impronta digitale del tuo browser, se lo desideri, ma è anche sicura da mantenere se non utilizzi la VPN di Mullvad.

### Modalità di Navigazione Privata

Mullvad Browser opera in modalità di navigazione privata permanente, ciò significa che la tua cronologia, cookie e altri dati dei siti saranno eliminati a ogni chiusura del browser. I tuoi segnalibri, le impostazioni del browser e dell'estensione saranno comunque conservati.

Ciò è necessario per impedire forme avanzate di tracciamento, a costo della comodità e di alcune funzionalità di Firefox, come i Contenitori Multi Profilo. Ricordati che puoi sempre utilizzare più browser, ad esempio, potresti considerare di utilizzare Firefox+Arkenfox per alcuni siti cui desideri rimanere connesso o, altrimenti, che non operano adeguatamente su Mullvad Browser, e Mullvad Browser per la navigazione generale.

### Mullvad Leta

Mullvad Browser integra DuckDuckGo come [motore di ricerca](search-engines.md) predefinito, ma include anche **Mullvad Leta**, un motore di ricerca che richiede un abbonamento attivo alla VPN di Mullvad, per potervi accedere. Mullvad Leta interroga direttamente l'API di ricerca a pagamento di Google, motivo per cui è limitata agli abbonati paganti. Tuttavia, è possibile per Mullvad correlare le query di ricerca e gli account VPN Mullvad a causa di questa limitazione. Per questo motivo sconsigliamo l'uso di Mullvad Leta, anche se Mullvad raccoglie pochissime informazioni sui propri abbonati alla VPN.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox logo](assets/img/browsers/firefox.svg){ align=right }

**Firefox** offre robuste impostazioni di privacy, come la [protezione antitracciamento avanzata](https://support.mozilla.org/it/kb/protezione-antitracciamento-avanzata-firefox-desktop), che aiuta a bloccare varie [tipologie di tracciamento](https://support.mozilla.org/it/kb/protezione-antitracciamento-avanzata-firefox-desktop#w_che-cosa-viene-bloccato-con-la-protezione-antitracciamento-avanzata).

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title=Documentazione}
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Codice sorgente" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Downloads</summary>

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

Queste opzioni si possono trovare in :material-menu: → **Impostazioni**.

#### Ricerca

- [ ] Disabilita **Visualizza suggerimenti di ricerca**

Le funzionalità di suggerimento di ricerca potrebbero non essere disponibili nella tua regione.

I suggerimenti di ricerca inviano qualsiasi cosa tu digiti nella barra degli indirizzi al motore di ricerca predefinito, indipendentemente dal fatto che tu invii una ricerca effettiva. Disabilitare i suggerimenti di ricerca ti consente di controllare più precisamente quali dati invii al fornitore del tuo motore di ricerca.

##### Firefox Suggest (solo USA)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) è una funzionalità simile ai suggerimenti di riceerca, disponibile esclusivamente negli Stati Uniti. Consigliamo di disabilitarla per le stesse motivazioni per cui consigliamo di disabilitare i suggerimenti di ricerca. Se non vedi queste opzioni sotto l'intestazione della **Barra degli Indirizzi**, non disponi della nuova esperienza e puoi ignorare tali modifiche.

- [ ] Deselezionare i **suggerimenti da Firefox**
- [ ] Rimuovi la spunta da **Suggestions from sponsors**

#### Privacy e sicurezza

##### Protezione antitracciamento avanzata

- [x] Seleziona Protezione antitracciamento avanzata **Restrittiva**

Questo ti protegge bloccando i tracciatori dei social, gli script di fingerprinting (nota che non ti protegge da *tutto* il fingerprinting), cryptominer, cookie di tracciamento dei tra siti e alcuni altri contenuti di tracciamento. La Protezione antitracciamento avanzata protegge da molte minacce comuni, ma non blocca tutte le vie di tracciamento, poiché è progettata per avere un impatto minimo o zero sull'utilizzabilità del sito.

##### Eliminazione alla Chiusura

Se vuoi mantenere l'accesso per alcuni siti in particolare, puoi consentire le eccezioni in **Cookie e dati dei siti web** → **Gestisci eccezioni...**

- [x] Spunta **Elimina cookie e dati dei siti web alla chiusura di Firefox**

Ciò ti protegge dai cookie persistenti, ma non da quelli acquisiti durante ogni sessione di navigazione. Con questa opzione attiva, è possibile eliminare facilmente i cookie del browser riavviando Firefox. Puoi impostare delle eccezioni a seconda del sito, se desideri rimanere connesso a un sito in particolare, che visiti spesso.

##### Telemetria

- [ ] Rimuovi la spunta da **Consenti a Firefox di inviare a Mozilla dati tecnici e relativi all’interazione con il browser**
- [ ] Rimuovi la spunta da **Consenti a Firefox di installare e condurre studi**
- [ ] Rimuovi la spunta da **Consenti a Firefox di inviare segnalazioni di arresto anomalo in sospeso**

> Firefox ci invia i dati sulla tua versione e lingua di Firefox; sistema operativo del dispositivo e configurazione hardware; memoria, informazioni essenziali su arresti anomali ed errori; risultati di processi automatizzati quali aggiornamenti, navigazione sicura e attivazione. Quando Firefox ci invia i dati, il tuo indirizzo IP è raccolto temporaneamente come parte dei registri del nostro server.

Inoltre, il servizio Mozilla Accounts raccoglie [alcuni dati tecnici](https://mozilla.org/privacy/mozilla-accounts). Se utilizzi un account Mozilla puoi disattivare questa funzione:

1. Apri le [impostazioni del tuo profilo su accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Deseleziona ** Raccolta e utilizzo dati ** > **Aiutaci a migliorare gli ⁨account Firefox⁩**

##### Website Advertising Preferences

- [ ] Uncheck **Allow websites to perform privacy-preserving ad measurement**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.

##### HTTPS-Only Mode

- [x] Seleziona **Attiva in tutte le finestre**

Ciò previene che ti connetta involontariamente a un sito web in HTTP semplice. I siti senza HTTPS sono poco comuni oggigiorno, quindi, ciò dovrebbe avere un impatto minimo o zero sulla tua navigazione quotidiana.

##### DNS over HTTPS

Se utilizzi un [fornitore di DNS su HTTPS](dns.md):

- [x] Seleziona **Protezione massima** e scegli un fornitore adatto

La Protezione Massima impone l'utilizzo di DNS su HTTPS; un avviso di sicurezza apparirà se Firefox non riesce a connettersi al tuo risolutore DNS sicuro, o se il tuo risolutore DNS sicuro dice che i registri per il dominio cui stai provando ad accedere, non esistono. Ciò impedisce alla rete cui sei connesso, di ridurre segretamente la sicurezza del tuo DNS.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) consente ai tuoi dati di navigazione (cronologia, segnalibri, etc.) di essere accessibili su tutti i tuoi dispositivi e li protegge con E2EE.

### Arkenfox (avanzato)

<div class="admonition tip" markdown>
<p class="admonition-title">Usa Mullvad Browser per l'anti-fingerprinting avanzato</p>

[Mullvad Browser](#mullvad-browser) fornisce le stesse protezioni anti-fingerprinting di Arkenfox pronte all'uso e non richiede l'utilizzo della VPN di Mullvad per beneficiarne. Insieme a una VPN, Mullvad Browser può contrastare gli script di tracciamento più avanzati, a differenza di Arkenfox. Tuttavia, Arkenfox presenta il vantaggio di essere molto più flessibile e di consentire eccezioni specifiche per i siti web a cui necessiti di rimanere connesso.

</div>

Il [progetto Arkenfox](https://github.com/arkenfox/user.js) fornisce una serie di opzioni attentamente selezionate per Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly—which you can [easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. **Consigliamo vivamente** di leggere la loro [wiki](https://github.com/arkenfox/user.js/wiki) completa. Arkenfox, inoltre, consente il supporto dei [contenitori](https://support.mozilla.org/kb/containers#w_for-advanced-users).

Arkenfox mira soltanto a contrastare gli script di tracciamento di base o semplici, tramite la casualizzazione dei canva e le impostazioni di configurazione della resistenza al fingerprint integrata di Firefox. Non mira a confondere il tuo browser con una grande folla di altri utenti di Arkenfox come Mullvad Browser o Tor Browser, che è il solo modo per contrastare gli script di tracciamento di fingerprint avanzati. Ricordati che puoi sempre utilizzare più browser, ad esempio, potresti considerare di utilizzare Firefox+Arkenfox per alcuni siti cui desideri rimanere connesso o, altrimenti fidarti, e Mullvad Browser per la navigazione generale.

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
<summary>Downloads</summary>

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

Queste opzioni si possono trovare in :material-menu: → **Impostazioni**.

#### Shields

Brave include delle misure anti-impronta digitale nella sua funzionalità, [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Suggeriamo di configurare queste opzioni [globalmente](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) tra tutte le pagine che visiti.

Le opzioni di Protezioni sono regolabili per ogni sito ma consigliamo di impostarle di default come segue:

<div class="annotate" markdown>

- [x] Select **Aggressive** under *Trackers & ads blocking*

<details class="warning" markdown>
<summary>Utilizza gli elenchi di filtri predefiniti</summary>

Brave consente di selezionare filtri aggiuntivi per i contenuti nella pagina interna `brave://adblock`. Sconsigliamo questa funzionalità; piuttosto, mantieni gli elenchi di filtri predefiniti. Utilzzare ulteriori elenchi ti distinguerà dagli altri utenti di Brave e potrebbe inoltre incrementare la superficie di attacco, se è presente un exploit su Brave e una regola dannosa viene aggiunta a uno degli elenchi che utilizzi.

</details>

- [x] Select **Strict** under *Upgrade connections to HTTPS*
- [x] (Optional) Select **Block Scripts** (1)
- [x] Check **Block fingerprinting**
- [x] Select **Block third-party cookies**
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. Questa opzione offre una funzionalità simile alle [modalità di blocco](https://github.com/gorhill/uBlock/wiki/Blocking-mode) avanzate di uBlock Origin.
2. Se desideri mantenere l'accesso in un particolare sito che visiti spesso, puoi selezionare le eccezioni per ogni sito cliccando sull'icona dello scudo sulla barra degli indirizzi.

#### Privacy and security

<div class="annotate" markdown>

- [x] Select **Don't allow sites to use the V8 optimizer** under *Security* → *Manage V8 security* (1)
- [x] Select **Automatically remove permissions from unused sites** under *Sites and Shields Settings*
- [x] Select **Disable non-proxied UDP** under [WebRTC IP Handling Policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **Prevent sites from fingerprinting me based on my language preferences**

</div>

1. Disabling the V8 optimizer reduces your attack surface by disabling [*some*](https://grapheneos.social/@GrapheneOS/112708049232710156) parts of JavaScript Just-In-Time (JIT) compilation.

<div class="admonition tip" markdown>
<p class="admonition-title">Sanitizzazione alla chiusura</p>

- [x] Select **Delete data sites have saved to your device when you close all windows** under *Sites and Shields Settings* → *Content* → *Additional content settings* → *On-device site data*.

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

##### Tor windows

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) allows you to route your traffic through the Tor network in Private Windows and access .onion services, which may be useful in some cases. However, Brave is **not** as resistant to fingerprinting as the Tor Browser and far fewer people use Brave with Tor, so you will stand out. If your threat model requires strong anonymity, use the [Tor Browser](tor.md#tor-browser).

##### Data Collection

- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**

#### Web3

Le funzionalità Web3 di Brave possono potenzialmente aumentare il fingerprint del browser e la superficie di attacco. Unless you use any of these features, they should be disabled.

- Select **Extensions (no fallback)** under *Default Ethereum wallet*
- Select **Extensions (no fallback)** under *Default Solana wallet*
- Set *Method to resolve IPFS resources* to **Disabled**

#### Extensions

- [ ] Uncheck all built-in extensions you don't use

#### System

<div class="annotate" markdown>

- [ ] Disabilita **Continua a eseguire applicazioni in background dopo la chiusura di Brave** per disabilitare le applicazioni in background (1)

</div>

1. Questa opzione non è presente su tutte le piattaforme.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) consente ai tuoi dati di navigazione (cronologia, segnalibri, ecc.) di essere accessibili su tutti i dispositivi, senza richiedere un profilo e li protegge con l'E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. Si affida a un conto custodiale e KYC da un dato numero di fornitori. Non raccomandiamo BAT come [criptovaluta privata](cryptocurrency.md), né raccomandiamo l'uso di un [wallet custodial](advanced/payments.md#wallet-custody), pertanto sconsigliamo di utilizzare questa funzione.

**Brave Wallet** opera localmente sul tuo computer, ma non supporta alcuna criptovaluta privata, quindi, scoraggiamo l'utilizzo di questa funzione.

## Risorse Aggiuntive

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcuno dei progetti consigliati.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questi elenchi, prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta migliore per te.

### Requisiti minimi

- Deve essere un software open source.
- Deve supportare gli aggiornamenti automatici.
- Must receive engine updates in 0-1 days from upstream release.
- Must be available on Linux, macOS, and Windows.
- Any changes required to make the browser more privacy-respecting must not negatively impact user experience.
- Must block third-party cookies by default.
- Must support [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### Miglior Caso

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere alcuna o tutte queste funzionalità, ma quelli che le presentano, potrebbero essere meglio classificati di altri su questa pagina.

- Should include built-in content blocking functionality.
- Should support cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Should support Progressive Web Apps. Le PWA consentono di installare determinati siti web come se fossero applicazioni native sul computer. This can have advantages over installing Electron-based apps, because PWAs benefit from your browser's regular security updates.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Should not collect telemetry by default.
- Should provide an open-source sync server implementation.
- Should default to a [private search engine](search-engines.md).

[^1]: L'implementazione di Brave è descritta in dettaglio in [Brave Privacy Updates: Partizionamento dello stato della rete per la privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
