---
meta_title: "Browser web che rispettano la privacy per Android e iOS- Privacy Guides"
title: Browser mobile
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
    name: Cromite
    image: /assets/img/browsers/cromite.svg
    url: https://cromite.org
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
    applicationCategory: Browser Web
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Protegge dalle seguenti minacce:</small>

- [:material-account-cash: Capitalismo di sorveglianza](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Questi sono al momento i **browser mobile** e le configurazioni da noi consigliati per la navigazione standard/non anonima in rete. Se hai bisogno di navigare in Internet in modo anonimo, dovresti invece usare [Tor](tor.md).

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
<summary>Download</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-fdroid: F-Droid](https://brave-browser-apk-release.s3.brave.com/fdroid/repo/index.html)

</details>

</div>

### Configurazione consigliata di Brave

Il Tor Browser è l'unico che veramente permette di navigare Internet anonimamente. Quando utilizzi Brave, consigliamo di modificare le seguenti informazioni per proteggere la tua privacy da certe parti, ma tutti i browser tranne [Tor Browser](tor.md#tor-browser) saranno tracciabili da *qualcuno*, in un modo o nell'altro.

=== "Android"

    Queste opzioni si trovano in :material-menu: → **Impostazioni** → **Protezioni Brave e privacy**.

=== "iOS"

    These options can be found in :fontawesome-solid-ellipsis: → **Settings** → **Shields & Privacy**.

#### Brave shields global defaults

Brave include delle misure anti-fingerprinting nella sua funzione [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Suggeriamo di configurare queste opzioni [globalmente](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) in tutte le pagine che visiti.

Le funzionalità di Shields possono essere ridotte per ogni sito se necessario; ciò nonostante, raccomandiamo le seguenti impostazioni:

=== "Android"

    <div class="annotate" markdown>

    - [x] Seleziona **aggressivo** in *Blocca tracker e annunci*
    - [x] Seleziona **Reindirizzamento automatico pagine AMP**
    - [x] Seleziona **URL di tracciamento di reindirizzamento automatico**
    - [x] Seleziona **Richiedi a tutte le connessioni di utilizzare HTTPS (rigido)** in *Aggiorna le connessioni a HTTPS*
    - \[x\] (Opzionale) Seleziona **Blocca gli Script** (1)
    - [x] Seleziona **Blocca cookie di terze parti** in *Blocca i cookie*
    - [x] Seleziona **Blocca le impronte digitali**
    - [x] Seleziona **Impedisci il fingerprinting tramite le impostazioni della lingua**

    <details class="warning" markdown>
    <summary>Usa gli elenchi di filtri predefiniti</summary>

    Brave ti consente di selezionare ulteriori filtri per i contenuti all'interno del menu **Applicazione di filtri ai contenuti** o della pagina `brave://adblock`. Sconsigliamo di utilizzare questa funzionalità; piuttosto, mantieni gli elenchi di filtri predefiniti. Utilizzare ulteriori elenchi ti distinguerà dagli altri utenti di Brave e potrebbe inoltre incrementare la superficie di attacco, se è presente un exploit su Brave e una regola dannosa viene aggiunta a uno degli elenchi che utilizzi.

    </details>

    - [x] Seleziona **Dimenticami quando chiudo questo sito**

    </div>

    1. Questa opzione disabilita JavaScript, il che porterà al malfunzionamento di molti siti. Per far funzionare normalmente un sito, puoi impostare le eccezioni per ogni sito toccando l'icona dello scudo nella barra degli indirizzi e deselezionando l'impostazione in *Controlli avanzati*.

=== "iOS"

    <div class="annotate" markdown>

    - [x] Select **Aggressive** under *Trackers & Ads Blocking*
    - [x] Select **Strict** under *Upgrade Connections to HTTPS*
    - [x] Select **Auto-Redirect AMP pages**
    - [x] Select **Auto-Redirect Tracking URLs**
    - \[x\] (Opzionale) Seleziona **Blocca gli Script** (1)
    - [x] Seleziona **Blocca le impronte digitali**
    - [x] Select **Site Tabs Closed** under *Auto Shred*

    <details class="warning" markdown>
    <summary>Usa gli elenchi di filtri predefiniti</summary>

    Brave allows you to select additional content filters within the **Content Filtering** menu. Sconsigliamo di utilizzare questa funzionalità; piuttosto, mantieni gli elenchi di filtri predefiniti. Utilizzare ulteriori elenchi ti distinguerà dagli altri utenti di Brave e potrebbe inoltre incrementare la superficie di attacco, se è presente un exploit su Brave e una regola dannosa viene aggiunta a uno degli elenchi che utilizzi.

    </details>

    </div>

    1. Questa opzione disabilita JavaScript, il che porterà al malfunzionamento di molti siti. Per far funzionare normalmente un sito, puoi impostare le eccezioni per ogni sito toccando l'icona dello scudo nella barra degli indirizzi e deselezionando l'impostazione in *Controlli avanzati*.

##### Clear browsing data (Android only)

- [x] Seleziona **Cancella dati all'uscita**

##### Social Media Blocking (Android only)

- [ ] Rimuovi la spunta da tutti i componenti social

#### Altre impostazioni sulla privacy

=== "Android"

    <div class="annotate" markdown>

    - [x] Seleziona **Disabilita UDP senza proxy** in [*Gestione politica IP WebRTC*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
    - \[x\] (Opzionale) Seleziona **Nessuna protezione** in *Navigazione sicura* (1)
    - [ ] Rimuovi la spunta da **Consenti ai siti di controllare se hai metodi di pagamento salvati**
    - [ ] Uncheck **Javascript optimization & security** under the setting with the same name
    - [x] Seleziona **Chiudi le schede quando esci**
    - [ ] Deseleziona **Acconsenti all'analisi dei prodotti di tutela della privacy (P3A)**
    - [ ] Deseleziona **Inviare automaticamente i rapporti di diagnostica**
    - [ ] Deseleziona **Invia automaticamente un ping di utilizzo giornaliero a Brave**

    </div>

    1. Brave's [implementation of Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) on Android **does not** proxy [Safe Browsing network requests](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) like its desktop counterpart. This means that your IP address may be seen (and logged) by Google. Note that Safe Browsing is not available for Android devices without Google Play Services.

=== "iOS"

    - [ ] Uncheck **Allow Privacy-Preserving Product Analytics (P3A)**
    - [ ] Deseleziona **Invia automaticamente un ping di utilizzo giornaliero a Brave**

#### Leo

These options can be found in :material-menu: → **Settings** → **Leo**.

<div class="annotate" markdown>

- [ ] Uncheck **Show autocomplete suggestions in address bar** (1)

</div>

1. This option is not present in Brave's iOS app.

#### Motori di ricerca

Queste opzioni si trovano in :material-menu:/:fontawesome-solid-ellipsis: → **Impostazioni** → **Motori di ricerca**.

- [ ] Disabilita **Visualizza suggerimenti di ricerca**

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) consente ai tuoi dati di navigazione (cronologia, segnalibri, ecc.) di essere accessibili su tutti i dispositivi, senza richiedere un profilo e li protegge con l'E2EE.

## Cromite (Android)

<div class="admonition recommendation" markdown>

![Logo di Cromite](assets/img/browsers/cromite.svg){ align=right }

**Cromite** è un browser basato su Chromium con blocco degli annunci pubblicitari integrato, protezione delle impronte digitali e altri [miglioramenti della privacy e della sicurezza](https://github.com/uazo/cromite/blob/master/docs/FEATURES.md). It is a fork of the discontinued **Bromite** browser.

[:octicons-home-16: Homepage](https://cromite.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uazo/cromite/blob/master/docs/PRIVACY_POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/uazo/cromite?tab=readme-ov-file#docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/uazo/cromite){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Download</summary>

- [:simple-android: F-Droid](https://cromite.org/fdroid/repo/?fingerprint=49F37E74DEE483DCA2B991334FB5A0200787430D0B5F9A783DD5F13695E9517B)
- [:simple-github: GitHub](https://github.com/uazo/cromite/releases/latest)

</details>

</div>

### Configurazione consigliata

These options can be found in :material-menu: → :gear: **Settings** → **Privacy and security**.

#### Browsing data

- [x] Select **Close all open tabs on exit**

#### Incognito mode

- [x] Select **Open external links in incognito**

#### Sicurezza

- [x] Select **Always use secure connections**

Ciò previene che ti connetta involontariamente a un sito web in HTTP semplice. HTTP is extremely uncommon nowadays, so this should have little to no impact on your day-to-day browsing.

#### Adblock Plus settings

These options can be found in :material-menu: → :gear: **Settings** → **Adblock Plus settings**.

Cromite contains a customized version of Adblock Plus with EasyList enabled by default, as well as options to select more filter lists within the **Filter lists** menu.

Using extra lists will make you stand out from other Cromite users and may also increase attack surface if a malicious rule is added to one of the lists you use.

- \[x\] (Optional) Select **Enable anti-circumvention and snippets**

This setting adds an additional Adblock Plus list that may increase the effectiveness of Cromite's content blocking. The warnings about standing out and potentially increasing attack surface apply.

#### Legacy Adblock settings

These options can be found in :material-menu: → :gear: **Settings** → **Legacy Adblock settings**.

- [ ] Uncheck the autoupdate setting

This disables update checks for the unmaintained Bromite adblock filter.

## Safari (iOS)

On iOS, any app that can browse the web is [restricted](https://developer.apple.com/app-store/review/guidelines) to using an Apple-provided [WebKit framework](https://developer.apple.com/documentation/webkit), so a browser like [Brave](#brave) does not use the Blink engine (the core component of Chromium) like its counterparts on other operating systems.

<div class="admonition recommendation" markdown>

![Logo di Safari](assets/img/browsers/safari.svg){ align=right }

**Safari** è il browser predefinito di iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites, so more devices look identical), and fingerprint randomization, as well as Private Relay for those with a paid iCloud+ subscription.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title="Documentation" }

</details>

</div>

### Configurazione consigliata di Safari

We would suggest installing [AdGuard](browser-extensions.md#adguard) if you want a content blocker in Safari.

The following privacy/security-related options can be found in :gear: **Settings** → **Apps** → **Safari**.

#### Allow Safari to Access

Under **Siri**:

- [ ] Disable **Learn from this App**
- [ ] Disable **Show in App**
- [ ] Disable **Show on Home Screen**
- [ ] Disable **Suggest App**

This prevents Siri from using content from Safari for Siri suggestions.

#### Ricerca

- [ ] Disable **Search Engine Suggestions**

This setting sends whatever you type in the address bar to the search engine set in Safari. Disabilitare i suggerimenti di ricerca ti consente di controllare con maggiore precisione i dati inviati al fornitore del motore di ricerca.

#### Profili

Safari allows you to separate your browsing with different profiles. All of your cookies, history, and website data are separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

#### Privacy e sicurezza

- [x] Enable **Prevent Cross-Site Tracking**

This enables WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). The feature helps protect against unwanted tracking by using on-device machine learning to stop trackers. ITP protects against many common threats, but does not block all tracking avenues because it is designed to not interfere with website usability.

- [x] Enable **Require Face ID/Touch ID to Unlock Private Browsing**

This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

- [ ] Disable **Fraudulent Website Warning**

This setting uses Google Safe Browsing (or Tencent Safe Browsing for users in mainland China or Hong Kong) to protect you while you browse. As such, your IP address may be logged by your Safe Browsing provider. Disabling this setting will disable this logging, but you might be more vulnerable to known phishing sites.

- [x] Enable **Not Secure Connection Warning**

This setting shows a warning screen if your connection to a website isn't using HTTPS. Safari will automatically try to upgrade the site to HTTPS, so you should only see this when there is no HTTPS connection available.

- [ ] Disable **Highlights**

Apple's privacy policy for Safari states:

> When visiting a webpage, Safari may send information calculated from the webpage address to Apple over OHTTP to determine if relevant highlights are available.

#### Settings for Websites

Under **Camera**

- [x] Select **Ask**

Under **Microphone**

- [x] Select **Ask**

Under **Location**

- [x] Select **Ask**

These settings ensure that websites can only access your camera, microphone, or location after you explicitly grant them access.

#### Other Privacy Settings

These options can be found in :gear: **Settings** → **Apps** → **Safari** → **Advanced**.

##### Fingerprinting Mitigations

L'impostazione **Protezione avanzata da tracciamento e fingerprinting** randomizza alcuni valori in modo che sia più difficile ottenere la tua fingerprint:

- [x] Seleziona **Tutto il browsing** o **Browsing Privato**

##### Misurazione degli Annunci a Tutela della Privacy

- [ ] Disabilita la **Misurazione della pubblicità che tutela la privacy**

Tradizionalmente, la misurazione dei click sugli annunci ha utilizzato la tecnologia di tracciamento, che viola la privacy degli utenti. La [misurazione privata dei clic](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) è una funzione di WebKit e uno standard web proposto per consentire agli inserzionisti di misurare l'efficacia delle campagne web senza compromettere la privacy degli utenti.

Questa, presenta poche preoccupazioni sulla privacy, quindi, sebbene tu possa scegliere di lasciarla attiva, consideriamo il fatto che sia automaticamente disabilitata per la Navigazione Privata, come un segnale per disabilitarla.

#### Navigazione privata sempre attiva

Apri Safari e tocca sul pulsante Schede, nell'angolo inferiore destro. Then, expand the :material-format-list-bulleted: Tab Groups list.

- [x] Seleziona **Privata**

La modalità di Navigazione Privata di Safari offre ulteriori protezioni della privacy. La Navigazione Privata utilizza una nuova sessione [effimera](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) per ogni scheda, a significare che le schede sono isolate l'una dall'altra. There are other smaller privacy benefits with Private Browsing too, such as not sending a webpage’s address to Apple when using Safari's translation feature.

Do note that Private Browsing does not save cookies and website data, so it won't be possible to remain signed in to sites. Ciò può essere sconveniente.

#### Sincronizzazione iCloud

La sincronizzazione della Cronologia di Safari, dei Gruppi di Schede, delle Schede di iCloud e delle password salvate, avviene E2EE. Tuttavia, per impostazione predefinita, i segnalibri [non lo sono](https://support.apple.com/HT202303). Apple può decifrarli e accedervi in base alla propria [informativa sulla privacy](https://apple.com/legal/privacy/en-ww).

È possibile attivare E2EE per i segnalibri e i download di Safari attivando la [Protezione Avanzata dei Dati](https://support.apple.com/HT212520). Go to :gear: **Settings** → **iCloud** → **Advanced Data Protection**.

- [x] Turn on **Advanced Data Protection**

If you use iCloud with Advanced Data Protection disabled, we also recommend setting Safari's default download location to a local folder on your device. This option can be found in :gear: **Settings** → **Apps** → **Safari** → **General** → **Downloads**.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcuno dei progetti consigliati.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questi elenchi, prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta migliore per te.

### Requisiti minimi

- Deve supportare gli aggiornamenti automatici.
- Deve ricevere rapidamente gli aggiornamenti dalle release upstream.
- Deve supportare il blocco dei contenuti.
- Qualsiasi modifica necessaria per rendere il browser più rispettoso della privacy non dovrebbe avere un impatto negativo sull'esperienza dell'utente.
