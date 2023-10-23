---
meta_title: "I migliori gestori di password per proteggere la tua privacy e sicurezza - Privacy Guides"
title: "Gestori di password"
icon: material/form-textbox-password
description: I gestori di password ti consentono di memorizzare e gestire in sicurezza le password e altre credenziali.
cover: passwords.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Gestori di password consigliati
    url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Bitwarden
    image: /assets/img/password-management/bitwarden.svg
    url: https://bitwarden.com
    sameAs: https://it.wikipedia.org/wiki/Bitwarden
    applicationCategory: Gestore di password
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: 1Password
    image: /assets/img/password-management/1password.svg
    url: https://1password.com
    sameAs: https://en.wikipedia.org/wiki/1Password
    applicationCategory: Gestore di password
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Psono
    image: /assets/img/password-management/psono.svg
    url: https://psono.com
    applicationCategory: Gestore di password
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: KeePassXC
    image: /assets/img/password-management/keepassxc.svg
    url: https://keepassxc.org/
    sameAs: https://it.wikipedia.org/wiki/KeePassXC
    applicationCategory: Gestore di password
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: KeePassDX
    image: /assets/img/password-management/keepassdx.svg
    url: https://www.keepassdx.com/
    applicationCategory: Gestore di password
    operatingSystem: Android
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Strongbox
    image: /assets/img/password-management/strongbox.svg
    url: https://strongboxsafe.com/
    applicationCategory: Gestore di password
    operatingSystem: iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: gopass
    image: /assets/img/password-management/gopass.svg
    url: https://www.gopass.pw/
    applicationCategory: Gestore di password
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - FreeBSD
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
---

I gestori di password ti consentono di memorizzare e gestire in sicurezza le password e altre credenziali, utilizzando una password principale.

[Introduzione alle password :material-arrow-right-drop-circle:](./basics/passwords-overview.md)

!!! info

    I gestori di password integrati nei software, come i browser e i sistemi operativi, a volte non sono all'altezza di un software di gestione delle password dedicato. Il vantaggio di un gestore di password integrato è la buona integrazione con il software, ma spesso può essere molto semplice e privo di funzionalità per la privacy e la sicurezza rispetto alle alternative indipendenti.
    
    Ad esempio, il gestore di password di Microsoft Edge non offre affatto E2EE. Il gestore di password Google dispone di E2EE [facoltativa](https://support.google.com/accounts/answer/11350823), e quello [di Apple](https://support.apple.com/en-us/HT202303) la offre di default.

## Basati su Cloud

Questi gestori di password, le sincronizzano su un server su cloud per una facile accessibilità da tutti i tuoi dispositivi e per la sicurezza contro la perdita del dispositivo.

### Bitwarden

!!! recommendation

    ![Logo di Bitwarden](assets/img/password-management/bitwarden.svg){ align=right }
    
    **Bitwarden** è un gestore di password gratuito e open-source. L'obiettivo è quello di risolvere i problemi di gestione delle password per individui, team e organizzazioni aziendali. Bitwarden è una delle soluzioni migliori e più sicure per memorizzare tutti i vostri login e password, mantenendoli comodamente sincronizzati tra tutti i vostri dispositivi.
    
    [:octicons-home-16: Home](https://bitwarden.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://bitwarden.com/privacy){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://bitwarden.com/help/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/bitwarden){ .card-link title="Codice Sorgente" }
    
    ??? downloads "Scarica"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.x8bit.bitwarden)
        - [:simple-appstore: App Store](https://apps.apple.com/app/bitwarden-password-manager/id1137397744)
        - [:simple-github: GitHub](https://github.com/bitwarden/mobile/releases)
        - [:simple-windows11: Windows](https://bitwarden.com/download)
        - [:simple-linux: Linux](https://bitwarden.com/download)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/com.bitwarden.desktop)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/bitwarden-password-manager)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/bitwarden-free-password-m/nngceckbapebfimnlniiiahkandclblb)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/jbkfoedolllekgbhcbcoahefnbanhhlh)

Inoltre, Bitwarden dispone di [Bitwarden Send](https://bitwarden.com/products/send/), che ti consente di condividere testi e file in sicurezza, con la [crittografia end-to-end](https://bitwarden.com/help/send-encryption). Una [password](https://bitwarden.com/help/send-privacy/#send-passwords) può essere richiesta insieme al link di invio. Bitwarden Send dispone inoltre di funzionalità di [cancellazione automatica](https://bitwarden.com/help/send-lifespan).

Per poter condividere i file è necessario il [piano Premium](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans). Il piano gratuito consente esclusivamente la condivisione di testo.

Il codice dal lato del server di Bitwarden è [open source](https://github.com/bitwarden/server), quindi, se non desideri utilizzare il cloud di Bitwarden, puoi facilmente ospitare il tuo server di sincronizzazione di Bitwarden.

**Vaultwarden** è un'implementazione alternativa del server di sincronizzazione di Bitwarden scritta in Rust e compatibile con i client ufficiali di Bitwarden, perfetta per la distribuzione ospitabile autonomamente, quando l'esecuzione del servizio ufficiale e ricco di risorse, potrebbe non essere ideale. Se desideri ospitare autonomamente il tuo server di Bitwarden, desidererai quasi sicuramente utilizzare Vaultwarden, rispetto al codice del server ufficiale di Bitwarden.

[:octicons-repo-16: Repository di Vaultwarden](https://github.com/dani-garcia/vaultwarden ""){.md-button} [:octicons-info-16:](https://github.com/dani-garcia/vaultwarden/wiki){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/dani-garcia/vaultwarden){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://github.com/sponsors/dani-garcia){ .card-link title=Contribuisci }

### 1Password

!!! recommendation

    ![Logo di 1Password](assets/img/password-management/1password.svg){ align=right }
    
    **1Password** è un gestore di password con una forte attenzione alla sicurezza e la facilità d'uso, che consente di archiviare password, carte di credito, licenze software e qualsiasi altra informazione sensibile in una cassaforte digitale sicura. La cassaforte personale è ospitata sui server di 1Password per una [tariffa mensile](https://1password.com/sign-up/). 1Password è [controllato](https://support.1password.com/security-assessments/) regolarmente e fornisce un'assistenza clienti eccezionale. 1Password è closed source; tuttavia, la sicurezza del prodotto è documentata in modo esauriente nel suo [white paper sulla sicurezza](https://1passwordstatic.com/files/security/1password-white-paper.pdf).
    
    [:octicons-home-16: Home](https://1password.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://1password.com/legal/privacy/){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://support.1password.com/){ .card-link title=Documentazione}
    
    ??? downloads "Scarica"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onepassword.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1511601750?mt=8)
        - [:simple-windows11: Windows](https://1password.com/downloads/windows/)
        - [:simple-apple: macOS](https://1password.com/downloads/mac/)
        - [:simple-linux: Linux](https://1password.com/downloads/linux/)

Tradizionalmente, **1Password** ha offerto la migliore esperienza d'uso del gestore di password per chi utilizza macOS e iOS; tuttavia, ora ha raggiunto la parità di funzionalità su tutte le piattaforme. Vanta molte caratteristiche orientate alle famiglie e alle persone meno tecniche, oltre a funzionalità avanzate.

La tua cassaforte di 1Password è protetta sia dalla password principale che da una chiave di sicurezza randomizzata di 34 caratteri per crittografare i tuoi dati sui loro server. Tale chiave di sicurezza aggiunge un livello di protezione ai tuoi dati, poiché, essi, sono protetti da un'entropia elevata, indipendentemente dalla tua password principale. Molti altri gestori delle password si affidano interamente alla forza della tua password principale per proteggere i tuoi dati.

Un vantaggio di 1Password rispetto a Bitwarden è il supporto di prima classe per i client nativi. Mentre Bitwarden relega molti doveri, specialmente le funzionalità di gestione dei profili, all'interfaccia della propria cassaforte web, 1Password rende disponibile quasi ogni funzionalità, nei propri client mobile o desktop nativi. Inoltre, i client di 1Password, dispongono di un'interfaccia utente più intuitiva, che ne semplifica l'utilizzo e la navigazione.

### Psono

!!! recommendation

    ![Logo Psono](assets/img/password-management/psono.svg){ align=right }
    
    **Psono** è un gestore di password gratuito e open-source sviluppato in Germania, con particolare attenzione alla gestione delle password per i team. Psono supporta la condivisione sicura di password, file, segnalibri ed email. Tutti i codici segreti sono protetti da una password principale.
    
    [:octicons-home-16: Home](https://psono.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://psono.com/privacy-policy){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://doc.psono.com){ .card-link title=Documentazione}
    [:octicons-code-16:](https://gitlab.com/psono){ .card-link title="Codice Sorgente" }
    
    ??? downloads "Scarica"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.psono.psono)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/psono-password-manager/id1545581224)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/psono-pw-password-manager)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/psonopw-password-manager/eljmjmgjkbmpmfljlmklcfineebidmlo)
        - [:simple-docker: Docker Hub](https://hub.docker.com/r/psono/psono-client)

Psono fornisce un'ampia documentazione sul proprio prodotto. Il client web per Psono è ospitabile autonomamente; altrimenti, puoi scegliere la Community Edition completa o l'Enterprise Edition con funzionalità aggiuntive.

### Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

!!! example "Questa sezione è nuova"

    Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

#### Requisiti minimi

- Deve utilizzare un'E2EE forte, basata sugli standard e moderna.
- Deve disporre di pratiche crittografiche e di sicurezza documentate approfonditamente.
- Deve disporre di un controllo pubblicato da una terza parte affidabile e indipendente.
- Tutta la telemetria non essenziale dev'essere facoltativa.
- Non deve raccogliere più PII di quanto necessario, per scopi di fatturazione.

#### Caso migliore

I nostri criteri del caso migliore rappresentano cosa vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- La telemetria dovrebbe essere su richiesta (disabilitata di default) o non raccolta affatto.
- Dovrebbe essere open source e ragionevolmente ospitabile autonomamente.

## Archiviazione locale

Queste opzioni ti consentono di gestire localmente un database di password crittografate.

### KeePassXC

!!! recommendation

    ![Logo di KeePassXC](assets/img/password-management/keepassxc.svg){ align=right }
    
    **KeePassXC** è una biforcazione di KeePassX, una conversione nativa e multipiattaforma di KeePass Password Safe, mirata a estenderla e migliorarla con nuove funzionalità e correzioni di bug, per fornire un gestore di password open source, ricco di funzionalità, multipiattaforma e moderno.
    
    [:octicons-home-16: Home](https://keepassxc.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://keepassxc.org/privacy){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://keepassxc.org/docs/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/keepassxreboot/keepassxc){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://keepassxc.org/donate/){ .card-link title=Contribuisci }
    
    ??? downloads "Scarica"
    
        - [:simple-windows11: Windows](https://keepassxc.org/download/#windows)
        - [:simple-apple: macOS](https://keepassxc.org/download/#mac)
        - [:simple-linux: Linux](https://keepassxc.org/download/#linux)
        - [:simple-flathub: Flatpak](https://flathub.org/apps/details/org.keepassxc.KeePassXC)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/keepassxc-browser)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/keepassxc-browser/oboonakemofpalcgghocfoadofidjkkk)

KeePassXC memorizza i suoi dati di esportazione come file [CSV](https://en.wikipedia.org/wiki/Comma-separated_values). Ciò potrebbe comportare la perdita di dati, se importi questo file in un altro gestore di password. Consigliamo di controllare manualmente ogni record.

### KeePassDX (Android)

!!! recommendation

    ![Logo di KeePassDX](assets/img/password-management/keepassdx.svg){ align=right }
    
    **KeePassDX** è un gestore di password leggero per Android, che consente la modifica dei dati crittografati in un singolo file nel formato KeePass, e può compilare i moduli in un modo sicuro. [Contributor Pro](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.pro) consente lo sblocco dei contenuti cosmetici e dispone di funzionalità non standard del protocollo ma, soprattutto, aiuta e incoraggia lo sviluppo.
    
    [:octicons-home-16: Home](https://www.keepassdx.com){ .md-button .md-button--primary }
    [:octicons-info-16:](https://github.com/Kunzisoft/KeePassDX/wiki){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/Kunzisoft/KeePassDX){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://www.keepassdx.com/#donation){ .card-link title=Contribuisci }
    
    ??? downloads "Scarica"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.free)
        - [:simple-github: GitHub](https://github.com/Kunzisoft/KeePassDX/releases)

### Strongbox (iOS e macOS)

!!! recommendation

    ![Logo di Strongbox](assets/img/password-management/strongbox.svg){ align=right }
    
    **Strongbox** è un gestore di password nativo e open source per iOS e macOS. Supportando sia i formati di KeePass che di Password Safe, è utilizzabile insieme ad altri gestori di password, come KeePassXC, sulle piattaforme non Apple. Impiegando un [modello freemium](https://strongboxsafe.com/pricing), Strongbox offre gran parte delle funzionalità sotto il proprio rango gratuito con [funzionalità](https://strongboxsafe.com/comparison/) più orientate alla comodità, come l'autenticazione biometrica, bloccate dietro un abbonamento o una licenza perpetua.
    
    [:octicons-home-16: Home](https://strongboxsafe.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://strongboxsafe.com/privacy/){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://strongboxsafe.com/getting-started/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/strongbox-password-safe/Strongbox){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://github.com/strongbox-password-safe/Strongbox#supporting-development){ .card-link title=Contribuisci }
    
    ??? downloads "Scarica"
    
        - [:simple-appstore: App Store](https://apps.apple.com/app/strongbox-keepass-pwsafe/id897283731)

Inoltre, è offerta una versione esclusivamente offline: [Strongbox Zero](https://apps.apple.com/app/strongbox-keepass-pwsafe/id1581589638). Questa versione è stata ridotta nel tentativo di ridurre la superficie di attacco.

### Riga di comando

Questi prodotti sono gestori di password minimali, utilizzabili nelle applicazioni di scripting.

#### gopass

!!! recommendation

    ![Logo di gopass](assets/img/password-management/gopass.svg){ align=right }
    
    **gopass** è un gestore di password a riga di comando scritto in Go. Funziona su tutti i sistemi operativi desktop e server principali (Linux, macOS, BSD, Windows).
    
    [:octicons-home-16: Home](https://www.gopass.pw){ .md-button .md-button--primary }
    [:octicons-info-16:](https://github.com/gopasspw/gopass/tree/master/docs){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/gopasspw/gopass){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://github.com/sponsors/dominikschulz){ .card-link title=Contribuisci }
    
    ??? downloads "Scarica"
    
        - [:simple-windows11: Windows](https://www.gopass.pw/#install-windows)
        - [:simple-apple: macOS](https://www.gopass.pw/#install-macos)
        - [:simple-linux: Linux](https://www.gopass.pw/#install-linux)
        - [:simple-freebsd: FreeBSD](https://www.gopass.pw/#install-bsd)

### Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

!!! example "Questa sezione è nuova"

    Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

- Deve essere multipiattaforma.
