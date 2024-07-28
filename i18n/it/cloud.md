---
meta_title: "I migliori fornitori di archiviazione su cloud privati e sicuri - Privacy Guides"
title: "Archiviazione su Cloud"
icon: material/file-cloud
description: Molti fornitori di spazio d'archiviazione su cloud richiedono ti richiedono di affidarti al fatto che non guarderanno i tuoi file. Queste sono alternative private!
cover: cloud.webp
---

Many **cloud storage providers** require your full trust that they will not look at your files. Le alternative elencate di seguito eliminano la necessità di fiducia implementando l'E2EE.

Se queste alternative non soddisfano le tue esigenze, ti suggeriamo di utilizzare un software di crittografia come [Cryptomator](encryption.md#cryptomator-cloud), con un altro fornitore su cloud. L'utilizzo di Cryptomator insieme a **qualsiasi** fornitore su cloud (compresi questi), può essere una buona idea per ridurre il rischio di vulnerabilità di crittografia nei client nativi di un fornitore.

<details class="admonition info" markdown>
<summary>Stai cercando Nextcloud?</summary>

Nextcloud is [still a recommended tool](document-collaboration.md#nextcloud) for self-hosting a file management suite, however we do not recommend third-party Nextcloud storage providers at the moment, because we do [not recommend](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) Nextcloud's built-in E2EE functionality for home users.

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Proton Drive logo](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive** is an encrypted cloud storage provider from the popular encrypted email provider [Proton Mail](email.md#proton-mail). The initial free storage is limited to 2GB, but with completion of certain steps, additional storage can be obtained up to 5GB.

[:octicons-home-16: Homepage](https://proton.me/drive){ class="md-button md-button--primary" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)
- [:fontawesome-brands-windows: Windows](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

The Proton Drive web application has been independently audited by Securitum in [2021](https://proton.me/community/open-source).

I nuovi clienti mobile di Proton Drive non sono ancora stati controllati pubblicamente da una terza parte.

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
- [:fontawesome-brands-windows: Windows](https://tresorit.com/download)
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

They have also received the Digital Trust Label, a certification from the [Swiss Digital Initiative](https://efd.admin.ch/en/swiss-digital-initiative-en) which requires passing [35 criteria](https://swiss-digital-initiative.org/criteria) related to security, privacy, and reliability.

## Peergos

<div class="admonition recommendation" markdown>

![Peergos logo](assets/img/cloud/peergos.svg){ align=right }

**Peergos** is a decentralized protocol and open-source platform for storage, social media, and applications. It provides a secure and private space where users can store, share, and view their photos, videos, documents, etc. Peergos secures your files with quantum-resistant end-to-end encryption and ensures all data about your files remains private. It is built on top of [IPFS (InterPlanetary File System)](https://ipfs.tech).

[:octicons-home-16: Homepage](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://book.peergos.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-globe-16: Web](https://peergos.net)
- [:fontawesome-brands-windows: Windows](https://github.com/Peergos/web-ui/releases)
- [:simple-apple: macOS](https://github.com/Peergos/web-ui/releases)
- [:simple-linux: Linux](https://github.com/Peergos/web-ui/releases)

</details>

</div>

Peergos is primarily a web app, but you can self-host the server either as a local cache for your remote Peergos account, or as a standalone storage server negating the need to register for a remote account and subscription. Il server di Peergos è un file `.jar`, ciò significa che Java 17+ Runtime Environment[(scarica OpenJDK](https://azul.com/downloads)) deve essere installato sul tuo computer per farlo funzionare.

Running a local version of Peergos alongside a registered account on their paid, hosted service allows you to access your Peergos storage without any reliance on DNS or TLS certificate authorities, and keep a copy of your data backed up to their cloud. The user experience should be the same whether you run their desktop server or just use their hosted web interface.

Peergos was [audited](https://cure53.de/pentest-report_peergos.pdf) by Cure53 in September 2019, and all found issues were subsequently fixed.

Also, the Android app is not available but it is [in the works](https://discuss.privacyguides.net/t/peergos-private-storage-sharing-social-media-and-application-platform/11825/25). The current workaround is to use the mobile [PWA](https://peergos.net) instead.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

### Requisiti minimi

- Deve imporre la crittografia end-to-end.
- Deve offrire un piano gratuito o un periodo di prova per testarlo.
- Must support TOTP or FIDO2 multi-factor authentication, or passkey logins.
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
