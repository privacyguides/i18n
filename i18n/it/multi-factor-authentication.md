---
title: "Autenticatori a più fattori"
icon: 'material/two-factor-authentication'
description: Questi strumenti ti assistano nella protezione dei tuoi profili Internet con l'Autenticazione a Più Fattori, senza inviare i tuoi codici segreti a terze parti.
cover: multi-factor-authentication.webp
---

## Chiavi di Sicurezza Hardware

### YubiKey

!!! recommendation

    ![YubiKeys](assets/img/multi-factor-authentication/yubikey.png)
    
    Le **YubiKey** sono tra le chiavi di sicurezza più popolari. Alcuni modelli di YubiKey dispongono di un'ampia gamma di funzionalità, quali, l'autenticazione a [Secondo Fattore Universale (U2F)](https://en.wikipedia.org/wiki/Universal_2nd_Factor), [FIDO2 e WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), [Yubico OTP](basics/multi-factor-authentication.md#yubico-otp), [Verifica dell'Identità Personale (PIV)](https://developers.yubico.com/PIV), [OpenPGP](https://developers.yubico.com/PGP/), [TOTP e HOTP](https://developers.yubico.com/OATH).
    
    Uno dei benefici della YubiKey è che una chiave (YubiKey 5) può fare quasi tutto ciò che ti potresti aspettare da una chiave di sicurezza hardware. Ti incoraggiamo a svolgere il [quiz](https://www.yubico.com/quiz/) prima dell'acquisto, per assicurarti di compiere la scelta giusta.
    
    [:octicons-home-16: Home](https://www.yubico.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://docs.yubico.com/){ .card-link title=Documentazione}

La [tabella di confronto](https://www.yubico.com/store/compare/) mostra le funzionalità e come si confrontano le YubiKeys. Ti consigliamo vivamente di selezionare le chiavi tra le YubiKey 5 Series.

Le YubiKey sono programmabili utilizzando [YubiKey Manager](https://www.yubico.com/support/download/yubikey-manager/) o [YubiKey Personalization Tools](https://www.yubico.com/support/download/yubikey-personalization-tools/). Per gestire i codici TOTP, puoi utilizzare [Yubico Authenticator](https://www.yubico.com/products/yubico-authenticator/). Tutti i client di Yubico sono open source.

Per i modelli che supportano HOTP e TOTP, esistono 2 slot nell'interfaccia OTP che potrebbero essere utilizzati per HOTP e 32 slot per memorizzare i codici segreti TOTP. Questi codici segreti sono memorizzati e crittografati sulla chiave e non sono mai esposti ai dispositivi cui questa è collegata. Una volta fornito un seed (codice segreto condiviso) a Yubico Authenticator, questo fornirà soltanto il codice a sei cifre, mai il seed. Questo modello di sicurezza aiuta a limitare ciò che un malintenzionato può fare, qualora dovesse compromettere uno dei dispositivi che operano Yubico Authenticator, rendendo la YubiKey resistente agli attacchi fisici.

!!! warning "attenzione"
    Il firmware di YubiKey non è open source e non è aggiornabile. Se desideri avere le funzionalità nelle versioni del firmware più recenti, o se è presente una vulnerabilità nella versione del firmware in uso, dovrai acquistare una nuova chiave.

### Nitrokey

!!! recommendation

    ![Nitrokey](assets/img/multi-factor-authentication/nitrokey.jpg){ align=right }
    
    **Nitrokey** dispone di una chiave di sicurezza che supporta [FIDO2 e WebAuthn] (basics/multi-factor-authentication.md#fido-fast-identity-online), detta **Nitrokey FIDO2**. Per il supporto PGP, devi acquistare un'altra delle loro chiavi, come la **Nitrokey Start**, la **Nitrokey Pro 2** o la **Nitrokey Storage 2**.
    
    [:octicons-home-16: Home](https://www.nitrokey.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.nitrokey.com/data-privacy-policy){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://docs.nitrokey.com/){ .card-link title=Documentazione}

La [tabella di confronto](https://www.nitrokey.com/#comparison) mostra le funzionalità e le differenze tra i modelli di Nitrokey. La **Nitrokey 3** elencata ha un insieme di funzionalità combinate.

I modelli di Nitrokey sono configurabili utilizzando l'[app di Nitrokey](https://www.nitrokey.com/download).

Per i modelli che supportano HOTP e TOTP, ci sono 3 slot per HOTP e 15 per TOTP. Alcune Nitrokey possono fungere da gestori di password. Possono memorizzare fino a 16 credenziali differenti e crittografarle utilizzando la stessa password dell'interfaccia OpenPGP.

!!! warning "Attenzione"

    Sebbene le Nitrokey non rilascino i codici segreti HOTP/TOTP al dispositivo a cui sono collegati, la memoria HOTP e TOTP *non* è crittografata ed è vulnerabile agli attacchi fisici. Se vorresti memorizzare i codici segreti HOTP e TOTP, consigliamo vivamente di utilizzare, piuttosto, una YubiKey.

!!! warning "Attenzione"

    Ripristinare l'interfaccia di OpenPGP su una Nitrokey, inoltre, renderà il database delle password [inaccessibile](https://docs.nitrokey.com/pro/factory-reset.html).

La Nitrokey Pro 2, Nitrokey Storage 2 e l'imminente Nitrokey 3 supportano la verifica dell'integrità del sistema per i portatili con il firmware [Coreboot](https://www.coreboot.org/) + [Heads](https://osresearch.net/).

Il firmware di Nitrokey è open source, a differenza di YubiKey. Il firmware dei modelli NitroKey moderni (tranne che per **NitroKey Pro 2**) è aggiornabile.

### Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

!!! example "Questa sezione è nuova"

    Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

#### Requisiti minimi

- Deve utilizzare moduli di sicurezza hardware di alta qualità e resistenti alla manomissione.
- Deve supportare le ultime specifiche di FIDO2.
- Non deve consentire l'estrazione della chiave privata.
- I dispositivi che costano più di $35 devono supportare la gestione di OpenPGP e S/MIME.

#### Miglior Caso

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- Dovrebbe essere disponibile in formato USB-C.
- Dovrebbe essere disponibile con NFC.
- Dovrebbe supportare l'archiviazione dei codici segreti TOTP.
- Dovrebbe supportare gli aggiornamenti del firmware sicuri.

## App di Autenticazione

Le App d'Autenticazione implementano uno standard di sicurezza aadottato dalla Task Force Ingegneristica di Internet (IETF), detto **Password Una Tantum basate sul Tempo** o **TOTP**. Tramite questo metodo i siti web condividono un codice segreto con te, utilizzato dalla tua app d'autenticazione per generare un codice (solitamente) a sei cifre, a seconda dell'ora corrente, che inserisci accedendo al sito web, per verificarti. Tipicamente, questi codici sono rigenerati ogni 30 secondi e, una volta generato un nuovo codice, quello precedente diventa inutile. Anche se un hacker ottiene il codice a sei cifre, non gli sarà possibile decrittografarlo per ottenere quello originale, o per altrimenti poter prevedere quali potrebbero essere i codici futuri.

Consigliamo vivamente l'utilizzo delle app TOTP mobili, invece delle alternative desktop, poiché Android e iOS forniscono una migliore sicurezza e isolamento delle app, rispetto a gran parte dei sistemi operativi per desktop.

### ente Auth

!!! recommendation

    ![Logo di ente Auth](assets/img/multi-factor-authentication/ente-auth.png){ align=right }
    
    **ente Auth** è un'app gratuita e open source che memorizza e genera token TOTP sul tuo dispositivo mobile. Può essere utilizzato con un account online per eseguire il backup e la sincronizzazione dei token tra i tuoi dispositivi (e per accedervi tramite un'interfaccia web) in modo sicuro, con crittografia end-to-end. Può essere utilizzato anche offline su un singolo dispositivo senza la necessità di un account.
    
    [:octicons-home-16: Home](https://ente.io/auth){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Politica sulla Privacy" }
    [:octicons-code-16:](https://github.com/ente-io/auth){ .card-link title="Codice Sorgente" }
    
    ??? downloads "Scarica"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
        - [:simple-appstore: App Store](https://apps.apple.com/it/app/ente-authenticator/id6444121398)
        - [:simple-github: GitHub](https://github.com/ente-io/auth/releases)
        - [:octicons-globe-16: Web](https://auth.ente.io)

### Aegis Authenticator (Android)

!!! recommendation "consiglio"

    ![Logo di Aegis](assets/img/multi-factor-authentication/aegis.png){ align=right }
    
    **Aegis Authenticator** è un'app gratuita, sicura e open source per gestire i token di verifica a due passaggi per i tuoi servizi online. Aegis Authenticator opera completamente offline/localmente, ma include l'opzione di esportare i token per il backup, a differenza di molte alternative.
    
    [:octicons-home-16: Home](https://getaegis.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://www.buymeacoffee.com/beemdevelopment){ .card-link title=Contribuisci }
    
    ??? downloads "Scarica"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
        - [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

### Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

!!! example "Questa sezione è nuova"

    Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

- Il codice sorgente dev'essere disponibile pubblicamente.
- Non deve richiedere la connessione a Internet.
- Non deve sincronizzarsi a un servizio su cloud di sincronizzazione/backup di terze parti.
    - **Facoltativo**: Il supporto alla sincronizzazione E2EE con strumenti nativi dell'OS è accettabile, es. sincronizzazione crittografata tramite iCloud.
