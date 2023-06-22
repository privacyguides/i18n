---
meta_title: "I migliori fornitori di archiviazione cloud privati e sicuri - Guide alla privacy"
title: "Archiviazione in cloud"
icon: material/file-cloud
description: Molti fornitori di spazio d'archiviazione in cloud richiedono la tua fiducia sul fatto che non guarderanno i tuoi file. Queste sono alternative private!
cover: cloud.png
---

Molti fornitori di spazio di archiviazione cloud richiedono la tua totale fiducia sul fatto che non guarderanno nei tuoi file. Le alternative elencate di seguito eliminano la necessità di fiducia implementando l'E2EE.

Se queste alternative non soddisfano le vostre esigenze, vi suggeriamo di utilizzare un software di crittografia come [Cryptomator](encryption.md#cryptomator-cloud) con un altro cloud provider. L'uso di Cryptomator insieme a **qualsiasi ** provider cloud (compresi questi) può essere una buona idea per ridurre il rischio di falle di crittografia nei client nativi di un provider.

??? question "Stai cercando Nextcloud?"

    Nextcloud è [ancora uno strumento consigliato](productivity.md) per il self-hosting di una suite di gestione dei file, tuttavia al momento non raccomandiamo fornitori di storage Nextcloud di terze parti, perché [non consigliamo](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) la funzionalità E2EE integrata di Nextcloud per gli utenti normali.

## Proton Drive

!!! recommendation

    ![Logo Proton Drive](assets/img/cloud/protondrive.svg){ align=right }
    
    **Proton Drive** è un provider svizzero di spazio d'archiviazione in cloud criptato del popolare provider di email criptate [Proton Mail](email.md#proton-mail).
    
    [:octicons-home-16: Pagina principale](https://proton.me/drive){ class="md-button md-button--primary" }
    [:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Politica sulla privacy" }
    [:octicons-info-16:](https://proton.me/support/drive){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Codice sorgente" }
    
    ??? downloads "Scarica"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)

L'applicazione web di Proton Drive è stata sottoposta ad un audit indipendente da parte di Securitum nel [2021](https://proton.me/blog/security-audit-all-proton-apps). Non sono stati resi noti i dettagli completi, ma la lettera di attestazione di Securitum afferma che:

> Gli auditor hanno identificato due vulnerabilità di bassa gravità. Inoltre, sono state riportate cinque raccomandazioni generali. Allo stesso tempo, confermiamo che durante il pentest non sono stati identificati problemi di sicurezza importanti.

I nuovi client mobile di Proton Drive non sono ancora stati sottoposti ad audit pubblici da terze parti.

## Tresorit

!!! recommendation

    ![Logo Tresorit](assets/img/cloud/tresorit.svg){ align=right }
    
    **Tresorit** è un provider di cloud storage criptato svizzero-ungherese fondato nel 2011. Tresorit è di proprietà di Swiss Post, il servizio postale nazionale della Svizzera.
    
    [:octicons-home-16: Pagina Principale](https://tresorit.com/){ class="md-button md-button--primary" }
    [:octicons-eye-16:](https://tresorit.com/legal/privacy-policy){ .card-link title="Politica sulla privacy" }
    [:octicons-info-16:](https://support.tresorit.com/hc/en-us){ .card-link title=Documentazione}
    
    ??? downloads "Scarica"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.tresorit.mobile)
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id722163232)
        - [:simple-windows11: Windows](https://tresorit.com/download)
        - [:simple-apple: macOS](https://tresorit.com/download)
        - [:simple-linux: Linux](https://tresorit.com/download)

Tresorit ha ricevuto una serie di audit di sicurezza indipendenti:

- [2022](https://tresorit.com/blog/tresorit-receives-iso-27001-certification/): ISO/IEC 27001:2013[^1] [Certificato](https://www.certipedia.com/quality_marks/9108644476) di Conformità da TÜV Rheinland InterCert Kft
- [2021](https://tresorit.com/blog/fresh-penetration-testing-confirms-tresorit-security/): test di penetrazione da Computest
    - Questo test ha valutato la sicurezza del client Web di Tresorit, dell'applicazione Android, dell'applicazione Windows e della relativa infrastruttura.
    - Computest ha scoperto due vulnerabilità che sono state successivamente risolte.
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture/): test di penetrazione da Ernst & Young.
    - Questo test ha analizzato il codice sorgente completo di Tresorit e ha convalidato che l'implementazione corrisponde ai concetti descritti [nel white paper di Tresorit](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf).
    - Ernst & Young ha inoltre testato i client web, mobile e desktop: "I risultati dei test non hanno rilevato alcuna deviazione dalle dichiarazioni di Tresorit sulla riservatezza dei dati"

Hanno anche ricevuto il Digital Trust Label, una certificazione della [Swiss Digital Initiative](https://www.swiss-digital-initiative.org/digital-trust-label/) che richiede il superamento di [35 criteri](https://digitaltrust-label.swiss/criteria/) relativi a sicurezza, privacy e affidabilità.

## Criteri

**Si noti che non siamo affiliati a nessuno dei progetti che raccomandiamo.** Oltre ai [ nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie di requisiti chiari che ci consentono di fornire raccomandazioni obiettive. Ti consigliamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le vostre ricerche per assicurarvi che sia la scelta giusta per voi.

!!! example "Questa sezione è nuova"

    Stiamo lavorando per stabilire criteri ben definiti per ogni sezione del nostro sito, e questo potrebbe essere soggetto a modifiche. Se avete domande sui nostri criteri, vi preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e non date per scontato che non abbiamo preso in considerazione qualcosa nel formulare le nostre raccomandazioni se non è elencato qui. Sono molti i fattori presi in considerazione e discussi quando consigliamo un progetto, e stiamo lavorando per documentare ogni singolo fattore.

### Requisiti minimi

- Deve forzare la crittografia end-to-end.
- Deve offrire un piano gratuito o un periodo di prova per testarlo.
- Deve supportare l'autenticazione a più fattori TOTP o FIDO2, o i login tramite Passkey.
- Deve offrire un'interfaccia web che supporti le funzionalità di base per la gestione dei file.
- Deve consentire una esportazione facile di tutti i file/documenti.
- Deve utilizzare una crittografia standard e verificata.

### Caso migliore

KeePassXC memorizza i suoi dati di esportazione come file [CSV](https://en.wikipedia.org/wiki/Comma-separated_values). Ciò può comportare la perdita di dati se si importa questo file in un altro gestore di password.

- I client dovrebbero essere open-source.
- I client dovrebbero essere completamente testati da una terza parte indipendente.
- Dovrebbero offrire client nativi per Linux, Android, Windows, macOS e iOS.
    - Questi client dovrebbero integrarsi con gli strumenti nativi del sistema operativo per i provider di spazio d'archiviazione cloud, come l'integrazione dell'app Files su iOS o la funzionalità di DocumentsProvider su Android.
- Dovrebbero supportare una facile condivisione dei file con altri utenti.
- Dovrebbero offrire almeno un'anteprima di base dei file e una funzionalità di modifica sull'interfaccia web.

[^1]: [ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001):La conformità 2013 riguarda la [Gestione della sicurezza informatica](https://it.wikipedia.org/wiki/Gestione_della_sicurezza_informatica) e copre la vendita, lo sviluppo, la manutenzione e il supporto dei servizi cloud.
