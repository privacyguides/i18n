---
meta_title: "I migliori fornitori di archiviazione su cloud privati e sicuri - Privacy Guides"
title: "Archiviazione su Cloud"
icon: material/file-cloud
description: Molti fornitori di spazio d'archiviazione su cloud richiedono ti richiedono di affidarti al fatto che non guarderanno i tuoi file. Queste sono alternative private!
cover: cloud.webp
---

Molti fornitori di spazio di archiviazione su cloud richiedono la tua totale fiducia sul fatto che non guarderanno i tuoi file. Le alternative elencate di seguito eliminano la necessità di fiducia implementando l'E2EE.

Se queste alternative non soddisfano le tue esigenze, ti suggeriamo di utilizzare un software di crittografia come [Cryptomator](encryption.md#cryptomator-cloud), con un altro fornitore su cloud. L'utilizzo di Cryptomator insieme a **qualsiasi** fornitore su cloud (compresi questi), può essere una buona idea per ridurre il rischio di vulnerabilità di crittografia nei client nativi di un fornitore.

<details class="TYPE" markdown>
<summary>Stai cercando Nextcloud?</summary>

Nextcloud è [ancora uno strumento consigliato](productivity.md) per il self-hosting di una suite di gestione dei file, tuttavia al momento non raccomandiamo fornitori di storage Nextcloud di terze parti, perché [non raccomandiamo](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) la funzionalità E2EE integrata di Nextcloud per gli utenti privati.

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Logo di Proton Drive](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive** è un fornitore svizzero di spazio d'archiviazione crittografato su cloud, del popolare fornitore di email crittografate, [Proton Mail](email.md#proton-mail).

[:octicons-home-16: Homepage](https://proton.me/drive){ class="md-button md-button--primary" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)
- [:simple-windows11: Windows](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

L'applicazione web di Proton Drive è stata controllata indipendentemente da Securitum nel [2021](https://proton.me/blog/security-audit-all-proton-apps); i dettagli completi non sono stati resi disponibili, ma la lettera di attestazione di Securitum afferma che:

> I revisori hanno identificato due vulnerabilità di bassa gravità. Inoltre, sono stati segnalati cinque suggerimenti generali. Al contempo, confermiamo che non è stato identificato alcun problema di sicurezza importante, durante il pentest.

I nuovi client mobile di Proton Drive non sono ancora stati controllati pubblicamente da una terza parte.

## Tresorit

<div class="admonition recommendation" markdown>

![Logo di Tresorit](assets/img/cloud/tresorit.svg){ align=right }

**Tresorit** è un fornitore svizzero-ungherese di archiviazione crittografata su cloud, fondato nel 2011. Tresorit è di proprietà di Swiss Post, il servizio postale nazionale della Svizzera.

[:octicons-home-16: Homepage](https://tresorit.com){ class="md-button md-button--primary" }
[:octicons-eye-16:](https://tresorit.com/legal/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.tresorit.com){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.tresorit.mobile)
- [:simple-appstore: App Store](https://apps.apple.com/app/id722163232)
- [:simple-windows11: Windows](https://tresorit.com/download)
- [:simple-apple: macOS](https://tresorit.com/download)
- [:simple-linux: Linux](https://tresorit.com/download)

</details>

</div>

Tresorit ha ricevuto una serie di controlli di sicurezza indipendenti:

- [2022](https://tresorit.com/blog/tresorit-receives-iso-27001-certification): ISO/IEC 27001:2013[^1] Compliance [Certification](https://certipedia.com/quality_marks/9108644476) by TÜV Rheinland InterCert Kft
- [2021](https://tresorit.com/blog/fresh-penetration-testing-confirms-tresorit-security): Penetration Testing by Computest
    - Questa revisione ha valutato la sicurezza del client web di Tresorit, dell'app Android, dell'applicazione di Windows e della relativa infrastruttura.
    - Computest ha scoperto due vulnerabilità, successivamente risolte.
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): Penetration Testing by Ernst & Young.
    - Questa revisione ha analizzato il codice sorgente completo di Tresorit e ha convalidato che l'implementazione corrisponde ai concetti descritti [nel white paper](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf) di Tresorit.
    - Ernst & Young ha inoltre testato i client web, mobile e desktop: "I risultati dei test non hanno rilevato alcuna deviazione dalle dichiarazioni di Tresorit sulla confidenzialità dei dati."

They have also received the Digital Trust Label, a certification from the [Swiss Digital Initiative](https://www.efd.admin.ch/efd/en/home/digitalisierung/swiss-digital-initiative.html) which requires passing [35 criteria](https://digitaltrust-label.swiss/criteria) related to security, privacy, and reliability.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

<div class="admonition example" markdown>
<p class="admonition-title">Questa sezione è nuova</p>

Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

</div>

### Requisiti minimi

- Deve imporre la crittografia end-to-end.
- Deve offrire un piano gratuito o un periodo di prova per testarlo.
- Deve supportare l'autenticazione a più fattori TOTP o FIDO2, o gli accessi tramite Passkey.
- Deve offrire un'interfaccia web che supporti le funzionalità di base per la gestione dei file.
- Deve consentire un'esportazione facile di tutti i file/documenti.
- Deve utilizzare una crittografia standard e controllata.

### Miglior Caso

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- I client dovrebbero essere open source.
- I client dovrebbero essere interamente controllati da una terza parte indipendente.
- Dovrebbero offrire client nativi per Linux, Android, Windows, macOS e iOS.
    - Questi client dovrebbero integrarsi con gli strumenti nativi del sistema operativo per i fornitori dell'archiviazione su cloud, come l'integrazione dell'app Files su iOS o la funzionalità di DocumentsProvider su Android.
- Dovrebbero supportare una facile condivisione dei file con altri utenti.
- Dovrebbero offrire almeno un'anteprima di base dei file e una funzionalità di modifica sull'interfaccia web.

[^1]: [ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001): La conformità 2013 riguarda la [Gestione della sicurezza informatica](https://en.wikipedia.org/wiki/Information_security_management) dell'azienda e copre la vendita, lo sviluppo, la manutenzione e il supporto dei servizi su cloud.
