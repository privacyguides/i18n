---
title: "Browser desktop"
icon: material/laptop
description: These web browsers provide stronger privacy protections than Google Chrome.
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
    sameAs: https://en.wikipedia.org/wiki/Firefox
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
    sameAs: https://en.wikipedia.org/wiki/Brave_(web_browser)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

Questi sono i browser e le configurazioni per desktop attualmente consigliati per la navigazione standard/non anonima. We recommend [Mullvad Browser](#mullvad-browser) if you are focused on strong privacy protections and anti-fingerprinting out of the box, [Firefox](#firefox) for casual internet browsers looking for a good alternative to Google Chrome, and [Brave](#brave) if you need Chromium browser compatibility.

Se hai bisogno di navigare in Internet in modo anonimo, dovresti invece usare [Tor](tor.md). We make some configuration recommendations on this page, but all browsers other than Tor Browser will be traceable by *somebody* in some manner or another.

## Mullvad Browser

!!! recommendation

    ![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    **Mullvad Browser** is a version of [Tor Browser](tor.md#tor-browser) with Tor network integrations removed, aimed at providing Tor Browser's anti-fingerprinting browser technologies to VPN users. It is developed by the Tor Project and distributed by [Mullvad](vpn.md#mullvad), and does **not** require the use of Mullvad's VPN.
    
    [:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

Like [Tor Browser](tor.md), Mullvad Browser is designed to prevent fingerprinting by making your browser fingerprint identical to all other Mullvad Browser users, and it includes default settings and extensions that are automatically configured by the default security levels: *Standard*, *Safer* and *Safest*. Therefore, it is imperative that you do not modify the browser at all outside adjusting the default [security levels](https://tb-manual.torproject.org/security-settings/). Other modifications would make your fingerprint unique, defeating the purpose of using this browser. If you want to configure your browser more heavily and fingerprinting is not a concern for you, we recommend [Firefox](#firefox) instead.

### Anti-Fingerprinting

**Without** using a [VPN](vpn.md), Mullvad Browser provides the same protections against [naive fingerprinting scripts](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) as other private browsers like Firefox+[Arkenfox](#arkenfox-advanced) or [Brave](#brave). Mullvad Browser provides these protections out of the box, at the expense of some flexibility and convenience that other private browsers can provide.

==For the strongest anti-fingerprinting protection, we recommend using Mullvad Browser in conjunction **with** a VPN==, whether that is Mullvad or another recommended VPN provider. When using a VPN with Mullvad Browser, you will share a fingerprint and a pool of IP addresses with many other users, giving you a "crowd" to blend in with. This strategy is the only way to thwart advanced tracking scripts, and is the same anti-fingerprinting technique used by Tor Browser.

Note that while you can use Mullvad Browser with any VPN provider, other people on that VPN must also be using Mullvad Browser for this "crowd" to exist, something which is more likely on Mullvad VPN compared to other providers, particularly this close to the launch of Mullvad Browser. Mullvad Browser does not have built-in VPN connectivity, nor does it check whether you are using a VPN before browsing; your VPN connection has to be configured and managed separately.

Mullvad Browser comes with the *uBlock Origin* and *NoScript* browser extensions pre-installed. While we typically [don't recommend](#extensions) adding *additional* browser extensions, these extensions that come pre-installed with the browser should **not** be removed or configured outside their default values, because doing so would noticeably make your browser fingerprint distinct from other Mullvad Browser users. It also comes pre-installed with the Mullvad Browser Extension, which *can* be safely removed without impacting your browser fingerprint if you would like, but is also safe to keep even if you don't use Mullvad VPN.

### Private Browsing Mode

Mullvad Browser operates in permanent private browsing mode, meaning your history, cookies, and other site data will always be cleared every time the browser is closed. Your bookmarks, browser settings, and extension settings will still be preserved.

This is required to prevent advanced forms of tracking, but does come at the cost of convenience and some Firefox features, such as Multi-Account Containers. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise don't work properly in Mullvad Browser, and Mullvad Browser for general browsing.

### Mullvad Leta

Mullvad Browser comes with DuckDuckGo set as the default [search engine](search-engines.md), but it also comes preinstalled with **Mullvad Leta**, a search engine which requires an active Mullvad VPN subscription to access. Mullvad Leta queries Google's paid search API directly (which is why it is limited to paying subscribers), however because of this limitation it is possible for Mullvad to correlate search queries and Mullvad VPN accounts. For this reason we discourage the use of Mullvad Leta, even though Mullvad collects very little information about their VPN subscribers.

## Firefox

!!! recommendation

    ![Firefox logo](assets/img/browsers/firefox.svg){ align=right }
    
    **Firefox** offre robuste impostazioni di privacy, come la [protezione antitracciamento avanzata](https://support.mozilla.org/it/kb/protezione-antitracciamento-avanzata-firefox-desktop), che aiuta a bloccare varie [tipologie di tracciamento](https://support.mozilla.org/it/kb/protezione-antitracciamento-avanzata-firefox-desktop#w_che-cosa-viene-bloccato-con-la-protezione-antitracciamento-avanzata).
    
    [:octicons-home-16: Pagina principale](https://firefox.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mozilla.org/privacy/firefox/){ .card-link title="Informativa sulla privacy" }
    [:octicons-info-16:](https://firefox-source-docs.mozilla.org/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Codice sorgente" }
    [:octicons-heart-16:](https://donate.mozilla.org/){ .card-link title=Contribuisci }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://www.mozilla.org/firefox/windows)
        - [:simple-apple: macOS](https://www.mozilla.org/firefox/mac)
        - [:simple-linux: Linux](https://www.mozilla.org/firefox/linux)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

!!! warning
    Firefox include un [token di download](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) univoco nella sezione dei download del sito di Mozilla e utilizza la telemetria in Firefox per inviarlo. Il token **non** è incluso nelle versioni rilasciate dall'[FTP di Mozilla](https://ftp.mozilla.org/pub/firefox/releases/).

### Configurazione consigliata

Queste opzioni si trovano in :material-menu: → **Impostazioni** → **Privacy e sicurezza**.

##### Protezione antitracciamento avanzata

- [x] Seleziona Protezione antitracciamento avanzata **Restrittiva**

Essa ti protegge bloccando i tracker dei social, script di fingerprinting (nota che questo non ti protegge da *tutte* le forme di fingerprinting), minatori di criptovalute, cookie di tracciamento cross-site e altri contenuti di tracciamento. La Protezione antitracciamento avanzata protegge da molte minacce comuni, ma non blocca tutte le vie di tracciamente, perché progettata per avere minimo o nessun impatto sull'usabilità dei siti.

##### Sanitizzazione alla chiusura

Se vuoi mantenere l'accesso per alcuni siti in particolare, puoi consentire le eccezioni in **Cookie e dati dei siti web** → **Gestisci eccezioni...**

- [x] Seleziona **Elimina cookie e dati dei siti web alla chiusura di Firefox**

Ciò ti protegge dai cookie persistenti, ma non da quelli acquisiti durante ogni sessione di navigazione. Con questa opzione attiva, è possibile eliminare facilmente i cookie del browser riavviando Firefox. È possibile impostare le eccezioni per ogni sito, ad esempio se desideri mantenere l'accesso ad un sito particolare che frequenti spesso.

##### Suggerimenti di ricerca

- [ ] Disabilita **Visualizza suggerimenti di ricerca**

I suggerimenti di ricerca potrebbero non essere disponibili nella tua zona.

I suggerimento di ricerca inviano tutto quello che viene scritto nella barra di ricerca al motore di ricerca predefinito, indipendentemente se le stringe vengono inviate o meno. Disabilitare i suggerimenti di ricerca ti permette di controllare più precisamente quali dati invii al motore di ricerca che utilizzi.

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

### Firefox Sync

La [sincronizzazione via Firefox](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) permette ai tuoi dati di navigazione (cronologia, segnalibri, etc.) di essere accessibili su tutti i tuoi dispositivi; i dati vengono protetti mediante E2EE.

### Arkenfox (avanzato)

!!! tip "Use Mullvad Browser for advanced anti-fingerprinting"

    [Mullvad Browser](#mullvad-browser) provides the same anti-fingerprinting protections as Arkenfox out of the box, and does not require the use of Mullvad's VPN to benefit from these protections. Coupled with a VPN, Mullvad Browser can thwart more advanced tracking scripts which Arkenfox cannot. Arkenfox still has the advantage of being much more flexible, and allowing per-site exceptions for websites which you need to stay logged in to.

Il progetto [Arkenfox](https://github.com/arkenfox/user.js) fornisce un insieme di opzioni attentamente selezionate per Firefox. Se [decidi](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) di utilizzare Arkenfox, [alcune opzioni](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) sono più stringenti di altri e/o potrebbero causare il malfunzionamento di alcuni siti web - [opzioni che possono essere cambiate facilmente](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) per aderire alle tue necessità. **Consigliamo caldamente** di leggere tutto il loro [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox inoltre abilita il supporto per le [schede contenitore](https://support.mozilla.org/it/kb/containers-schede-contenitore-firefox#per-utenti-avanzati).

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

## Brave

!!! recommendation

    ![Brave logo](assets/img/browsers/brave.svg){ align=right }
    
    **Brave Browser** include un content blocker integrato e [funzionalità di privacy](https://brave.com/privacy-features/), molte delle quali attive in modo predefinito.
    
    Brave è sviluppato a partire dal progetto del browser web Chromium, quindi dovrebbe risultare familiare e avere problemi minimi di compatibilità con i siti web.
    
    [:octicons-home-16: Pagina principale](https://brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Servizio Onion" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Informativa sulla privacy" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Codice sorgente" }
    
    ??? downloads annotate
    
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
        - [:simple-windows11: Windows](https://brave.com/download/)
        - [:simple-apple: macOS](https://brave.com/download/)
        - [:simple-linux: Linux](https://brave.com/linux/) (1)

    1. Sconsigliamo l'utilizzo della versione Flatpack di Brave, in quanto rimpiazza il sandbox di Chromium con quello di Flatpak, il quale è meno efficace. Inoltre, il pacchetto non è gestito da Brave Software, Inc.

### Configurazione consigliata

Queste opzioni possono essere trovare in :material-menu: → **Impostazioni**.

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

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net/) extension.

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

    !!! important "Sanitizzazione alla chiusura"
        - [x] Seleziona **Cancella cookie e dati dei siti alla chiusura di tutte le finestre** nel menu *Cookie e altri dati dei siti*

        Se desideri rimanere connesso a un particolare sito che si visita spesso, è possibile impostare eccezioni su base individuale nella sezione *Comportamenti personalizzati*.

</div>

1. Brave **non è** resistente al fingerprinting come il Tor Browser e molte meno persone utilizzano Brave con Tor, facendoti quindi distinguere. Quando [è necessario un forte anonimato](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-) utilizzare il [Tor Browser](tor.md#tor-browser).

##### Estensioni

Disabilita le estensioni integrate che non utilizzi in **Estensioni**

- [ ] Disabilita **Hangouts**
- [ ] Disabilita **WebTorrent**

##### Web3

<div class="annotate" markdown>

- [x] Select **Disabled** on Method to resolve IPFS resources (1)

</div>

1. InterPlanetary File System (IPFS) is a decentralized, peer-to-peer network for storing and sharing data in a distributed filesystem. Unless you use the feature, disable it.

##### Impostazioni aggiuntive

Under the *System* menu

<div class="annotate" markdown>

- [ ] Uncheck **Continue running apps when Brave is closed** to disable background apps (1)

</div>

1. This option is not present on all platforms.

### Brave Sync

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) permette ai dati di navigazione (cronologia, segnalibri, ecc.) di essere accessibili su tutti i dispositivi senza richiedere un account e li protegge con E2EE.

## Risorse aggiuntive

In general, we recommend keeping your browser extensions to a minimum to decrease your attack surface; they have privileged access within your browser, require you to trust the developer, can make you [stand out](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), and [weaken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) site isolation. However, uBlock Origin may prove useful if you value content blocking functionality.

### uBlock Origin

!!! recommendation

    ![uBlock Origin logo](assets/img/browsers/ublock_origin.svg){ align=right }
    
    **uBlock Origin** è un popolare blocker di contenuti che aiuta a bloccare pubblicità, tracker e script di fingerprinting.
    
    [:octicons-repo-16: Repository](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Informativa sulla privacy" }
    [:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Codice sorgente" }
    
    ??? downloads
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

We suggest following the [developer's documentation](https://github.com/gorhill/uBlock/wiki/Blocking-mode) and picking one of the "modes". Additional filter lists can impact performance and [may increase attack surface](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

##### Altre liste

These are some other [filter lists](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) that you may want to consider adding:

- [x] Check **Privacy** > **AdGuard URL Tracking Protection**
- Add [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

## Criteri

**Si noti che non siamo affiliati a nessuno dei progetti che raccomandiamo.** Oltre ai [ nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie di requisiti chiari che ci consentono di fornire raccomandazioni obiettive. Ti consigliamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le vostre ricerche per assicurarvi che sia la scelta giusta per voi.

!!! esempio "Questa sezione è nuova"

    Stiamo lavorando per stabilire criteri ben definiti per ogni sezione del nostro sito, e questo potrebbe essere soggetto a modifiche. Se avete domande sui nostri criteri, vi preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e non date per scontato che non abbiamo preso in considerazione qualcosa nel formulare le nostre raccomandazioni se non è elencato qui. Sono molti i fattori presi in considerazione e discussi quando consigliamo un progetto, e stiamo lavorando per documentare ogni singolo fattore.

### Requisiti minimi

- Deve essere un software open-source.
- Supports automatic updates.
- Receives engine updates in 0-1 days from upstream release.
- Available on Linux, macOS, and Windows.
- Qualsiasi modifica necessaria per rendere il browser più rispettoso della privacy non dovrebbe avere un impatto negativo sull'esperienza dell'utente.
- Blocks third-party cookies by default.
- Supports [state partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### Caso migliore

KeePassXC memorizza i suoi dati di esportazione come file [CSV](https://en.wikipedia.org/wiki/Comma-separated_values). Ciò può comportare la perdita di dati se si importa questo file in un altro gestore di password.

- Includes built-in content blocking functionality.
- Supports cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/en-US/kb/containers)).
- Supports Progressive Web Apps.  
  PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps, because you benefit from your browser's regular security updates.
- Does not include add-on functionality (bloatware) that does not impact user privacy.
- Does not collect telemetry by default.
- Provides open-source sync server implementation.
- Defaults to a [private search engine](search-engines.md).

### Criteri delle estensioni

- Non deve replicare funzionalità integrate nel browser o del sistema operativo.
- Deve avere un impatto diretto sulla privacy dell'utente, cioè non deve limitarsi a fornire informazioni.

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state/).
