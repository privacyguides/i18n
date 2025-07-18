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

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Capitalismo di sorveglianza](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our currently recommended **desktop web browsers** and configurations for standard/non-anonymous browsing. Consigliamo [Mullvad Browser](#mullvad-browser) se sei interessato a una forte protezione della privacy e all'anti-fingerprinting pronti all'uso, [Firefox](#firefox) per i navigatori occasionali di Internet alla ricerca di una buona alternativa a Google Chrome e [Brave](#brave), se necessiti della compatibilità del browser con Chromium.

Invece, se necessiti di navigare anonimamente su Internet, dovresti utilizzare [Tor](tor.md). In questa pagina forniamo alcune raccomandazioni sulla configurazione, ma tutti i browser diversi da Tor Browser saranno rintracciabili da *qualcuno* in un modo o nell'altro.

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** is a version of [Tor Browser](tor.md#tor-browser) with Tor network integrations removed. It aims to provide to VPN users Tor Browser's anti-fingerprinting browser technologies, which are key protections against [:material-eye-outline: Mass Surveillance](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. Sviluppato dal Tor Project e distribuito da [Mullvad](vpn.md#mullvad), **non** richiede l'utilizzo della VPN di Mullvad.

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Like [Tor Browser](tor.md), Mullvad Browser is designed to prevent fingerprinting by making your browser fingerprint identical to all other Mullvad Browser users, and it includes default settings and extensions that are automatically configured by the default security levels: *Standard*, *Safer* and *Safest*.

Therefore, it is imperative that you do not modify the browser at all outside adjusting the default [security levels](https://tb-manual.torproject.org/security-settings). When adjusting the security level, you **must** always restart the browser before continuing to use it. Otherwise, [the security settings may not be fully applied](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), putting you at a higher risk of fingerprinting and exploits than you may expect based on the setting chosen.

Modifications other than adjusting this setting would make your fingerprint unique, defeating the purpose of using this browser. Se desideri configurare il tuo browser in modo più completo e il fingerprinting non ti preoccupa, consigliamo invece [Firefox](#firefox).

### Anti-Fingerprinting

**Senza** utilizzare una [VPN](vpn.md), Mullvad Browser fornisce le stesse protezioni dai [semplici script di fingerprinting](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) di altri browser privati, come Firefox+[Arkenfox](#arkenfox-advanced) o [Brave](#brave). Mullvad Browser fornisce tali protezioni "pronte all'uso", a scapito di una certa flessibilità e comodità che altri browser privati possono fornire.

==Per la massima protezione anti-fingerprinting, consigliamo di utilizzare Mullvad Browser **con** una VPN==, che sia di Mullvad o di un altro fornitore di VPN consigliato. Utilizzando una VPN con Mullvad Browser, condividi un'impronta digitale e un gruppo di indirizzi IP con molti altri utenti, offrendoti una "folla" con cui confonderti. Questa strategia è l'unico modo per contrastare gli script di tracciamento avanzati ed è la stessa tecnica anti-fingerprinting utilizzata da Tor Browser.

Nota che, sebbene tu possa utilizzare Mullvad Browser con qualsiasi fornitore VPN, altre persone su tale VPN devono anch'esse utilizzare Mullvad Browser affinché tale "folla" esista, il che è molto più probabile su Mullvad VPN, rispetto ad altri fornitori, in particolare così a breve distanza dal lancio di Mullvad Browser. Mullvad Browser non dispone di connettività VPN integrata, né verifica che tu stia utilizzando una VPN prima di navigare; la tua connessione VPN dev'essere configurata e gestita separatamente.

Mullvad Browser contiene le estensioni pre-installate di *uBlock Origin* e *NoScript*. Anche se in genere sconsigliamo di aggiungere *ulteriori* [estensioni del browser](browser-extensions.md), quelle preinstallate **non** devono essere rimosse o configurate al di fuori dei valori predefiniti, perché in questo modo l'impronta digitale del browser si distinguerebbe notevolmente da quella degli altri utenti di Mullvad Browser. Inoltre, presenta l'Estensione Mullvad Browser pre-installata, che *può* essere rimossa in sicurezza, senza influenzare l'impronta digitale del tuo browser, se lo desideri, ma è anche sicura da mantenere se non utilizzi la VPN di Mullvad.

### Modalità di Navigazione Privata

Mullvad Browser opera in modalità di navigazione privata permanente, ciò significa che la tua cronologia, cookie e altri dati dei siti saranno eliminati a ogni chiusura del browser. I tuoi segnalibri, le impostazioni del browser e dell'estensione saranno comunque conservati.

Ciò è necessario per impedire forme avanzate di tracciamento, a costo della comodità e di alcune funzionalità di Firefox, come i Contenitori Multi Profilo. Ricordati che puoi sempre utilizzare più browser, ad esempio, potresti considerare di utilizzare Firefox+Arkenfox per alcuni siti cui desideri rimanere connesso o, altrimenti, che non operano adeguatamente su Mullvad Browser, e Mullvad Browser per la navigazione generale.

### Mullvad Leta

Mullvad Browser comes with [**Mullvad Leta**](https://leta.mullvad.net) as the default search engine, which functions as a proxy to either Google or Brave search results (configurable on the Mullvad Leta homepage).

If you are a Mullvad VPN user, there is some risk in using services like Mullvad Leta which are offered by your VPN provider themselves. This is because Mullvad theoretically has access to your true IP address (via their VPN) and your search activity (via Leta), which is information a VPN is typically intended to separate. Even though Mullvad collects very little information about their VPN subscribers or Leta users, you should consider a different [search engine](search-engines.md) if this risk concerns you.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox logo](assets/img/browsers/firefox.svg){ align=right }

**Firefox** offre robuste impostazioni di privacy, come la [protezione antitracciamento avanzata](https://support.mozilla.org/it/kb/protezione-antitracciamento-avanzata-firefox-desktop), che aiuta a bloccare varie [tipologie di tracciamento](https://support.mozilla.org/it/kb/protezione-antitracciamento-avanzata-firefox-desktop#w_che-cosa-viene-bloccato-con-la-protezione-antitracciamento-avanzata).

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="Documentation" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Contribute" }

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

These options can be found in :material-menu: → **Settings**.

#### Ricerca

- [ ] Disabilita **Visualizza suggerimenti di ricerca**

Search suggestion features may not be available in your region.

Search suggestions send everything you type in the address bar to the default search engine, regardless of whether you submit an actual search. Disabling search suggestions allows you to more precisely control what data you send to your search engine provider.

##### Firefox Suggest (solo USA)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. We recommend disabling it for the same reason we recommend disabling search suggestions. If you don't see these options under the **Address Bar** header, you do not have the new experience and can ignore these changes.

- [ ] Deselezionare i **suggerimenti da Firefox**
- [ ] Rimuovi la spunta da **Suggestions from sponsors**

#### Privacy e sicurezza

##### Protezione antitracciamento avanzata

- [x] Seleziona Protezione antitracciamento avanzata **Restrittiva**

This protects you by blocking social media trackers, fingerprinting scripts (note that this does not protect you from *all* fingerprinting), cryptominers, cross-site tracking cookies, and some other tracking content. ETP protects against many common threats, but it does not block all tracking avenues because it is designed to have minimal to no impact on site usability.

##### Eliminazione alla Chiusura

If you want to stay logged in to particular sites, you can allow exceptions in **Cookies and Site Data** → **Manage Exceptions...**

- [x] Spunta **Elimina cookie e dati dei siti web alla chiusura di Firefox**

This protects you from persistent cookies, but does not protect you against cookies acquired during any one browsing session. Quando e' abilitato,   puoi pulire facilmente i cookie del browser semplicemente riavviando Firefox. You can set exceptions on a per-site basis, if you wish to stay logged in to a particular site you visit often.

##### Telemetry

- [ ] Rimuovi la spunta da **Consenti a Firefox di inviare a Mozilla dati tecnici e relativi all’interazione con il browser**
- [ ] Rimuovi la spunta da **Consenti a Firefox di installare e condurre studi**
- [ ] Rimuovi la spunta da **Consenti a Firefox di inviare segnalazioni di arresto anomalo in sospeso**

According to Mozilla's privacy policy for Firefox,

> Firefox ci invia i dati sulla tua versione e lingua di Firefox; sistema operativo del dispositivo e configurazione hardware; memoria, informazioni essenziali su arresti anomali ed errori; risultati di processi automatizzati quali aggiornamenti, navigazione sicura e attivazione. Quando Firefox ci invia i dati, il tuo indirizzo IP è raccolto temporaneamente come parte dei registri del nostro server.

Additionally, the Mozilla Accounts service collects [some technical data](https://mozilla.org/privacy/mozilla-accounts). If you use a Mozilla Account you can opt out:

1. Apri le [impostazioni del tuo profilo su accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Deseleziona ** Raccolta e utilizzo dati ** > **Aiutaci a migliorare gli ⁨account Firefox⁩**

##### Website Advertising Preferences

- [ ] Uncheck **Allow websites to perform privacy-preserving ad measurement**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.

##### HTTPS-Only Mode

- [x] Seleziona **Attiva in tutte le finestre**

This prevents you from unintentionally connecting to a website in plain-text HTTP. Sites without HTTPS are uncommon nowadays, so this should have little to no impact on your day-to-day browsing.

##### DNS over HTTPS

If you use a [DNS over HTTPS provider](dns.md):

- [x] Seleziona **Protezione massima** e scegli un fornitore adatto

Max Protection enforces the use of DNS over HTTPS, and a security warning will show if Firefox can’t connect to your secure DNS resolver, or if your secure DNS resolver says that records for the domain you are trying to access do not exist. This stops the network you're connected to from secretly downgrading your DNS security.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (avanzato)

<div class="admonition tip" markdown>
<p class="admonition-title">Usa Mullvad Browser per l'anti-fingerprinting avanzato</p>

[Mullvad Browser](#mullvad-browser) fornisce le stesse protezioni anti-fingerprinting di Arkenfox pronte all'uso e non richiede l'utilizzo della VPN di Mullvad per beneficiarne. Insieme a una VPN, Mullvad Browser può contrastare gli script di tracciamento più avanzati, a differenza di Arkenfox. Tuttavia, Arkenfox presenta il vantaggio di essere molto più flessibile e di consentire eccezioni specifiche per i siti web a cui necessiti di rimanere connesso.

</div>

The [Arkenfox project](https://github.com/arkenfox/user.js) provides a set of carefully considered options for Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly—which you can [easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. We **strongly recommend** reading through their full [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Ricordati che puoi sempre utilizzare più browser, ad esempio, potresti considerare di utilizzare Firefox+Arkenfox per alcuni siti cui desideri rimanere connesso o di cui ti fidi, e Mullvad Browser per la navigazione generale.

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

These options can be found in :material-menu: → **Settings**.

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

- [ ] Uncheck **Continue running background apps when Brave is closed** to disable background apps (1)

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
- Must receive engine updates in 0-1 days from upstream release.
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
