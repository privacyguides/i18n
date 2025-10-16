---
meta_title: "I migliori fornitori di archiviazione su cloud privati e sicuri - Privacy Guides"
title: Archiviazione su Cloud
icon: material/file-cloud
description: Molti fornitori di spazio d'archiviazione su cloud richiedono ti richiedono di affidarti al fatto che non guarderanno i tuoi file. Queste sono alternative private!
cover: cloud.webp
---

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: Attacchi Passivi](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Fornitori di Servizi](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Many **cloud storage providers** require your full trust that they will not look at your files. The alternatives listed below eliminate the need for trust by implementing secure end-to-end encryption.

Se queste alternative non soddisfano le tue esigenze, ti suggeriamo di utilizzare un software di crittografia come [Cryptomator](encryption.md#cryptomator-cloud), con un altro fornitore su cloud. L'utilizzo di Cryptomator insieme a **qualsiasi** fornitore su cloud (compresi questi), può essere una buona idea per ridurre il rischio di vulnerabilità di crittografia nei client nativi di un fornitore.

<details class="admonition info" markdown>
<summary>Stai cercando Nextcloud?</summary>

For more technical readers, Nextcloud is [still a recommended tool](self-hosting/file-management.md#nextcloud) for self-hosting a file management suite, however we do not recommend third-party Nextcloud storage providers at the moment, because we do [not recommend](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) Nextcloud's built-in E2EE functionality for home users.

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Proton Drive logo](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive** is an encrypted cloud storage provider from the popular encrypted email provider [Proton Mail](email.md#proton-mail).

The initial free storage is limited to 2 GB, but with the completion of [certain steps](https://proton.me/support/more-free-storage-existing-users), additional storage can be obtained up to 5 GB.

[:octicons-home-16: Homepage](https://proton.me/drive){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/drive/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)
- [:fontawesome-brands-windows: Windows](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

The Proton Drive web application has been independently audited by Securitum in [2021](https://proton.me/community/open-source), but the brand new mobile clients have not yet been publicly audited by a third party.

## Tresorit

<div class="admonition recommendation" markdown>

![Logo di Tresorit](assets/img/cloud/tresorit.svg){ align=right }

**Tresorit** è un fornitore svizzero-ungherese di archiviazione crittografata su cloud, fondato nel 2011. Tresorit è di proprietà di Swiss Post, il servizio postale nazionale della Svizzera.

[:octicons-home-16: Homepage](https://tresorit.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tresorit.com/legal/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.tresorit.com){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.tresorit.mobile)
- [:simple-appstore: App Store](https://apps.apple.com/app/id722163232)
- [:fontawesome-brands-windows: Windows](https://tresorit.com/download)
- [:simple-apple: macOS](https://tresorit.com/download)
- [:simple-linux: Linux](https://tresorit.com/download)

</details>

</div>

Tresorit has received a number of independent security audits:

- [2022](https://tresorit.com/blog/tresorit-receives-iso-27001-certification): ISO/IEC 27001:2013[^1] Compliance [Certification](https://certipedia.com/quality_marks/9108644476) by TÜV Rheinland InterCert Kft
- [2021](https://tresorit.com/blog/fresh-penetration-testing-confirms-tresorit-security): Penetration Testing by Computest
    - Questa revisione ha valutato la sicurezza del client web di Tresorit, dell'app Android, dell'applicazione di Windows e della relativa infrastruttura.
    - Computest ha scoperto due vulnerabilità, successivamente risolte.
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): Penetration Testing by Ernst & Young.
    - Questa revisione ha analizzato il codice sorgente completo di Tresorit e ha convalidato che l'implementazione corrisponde ai concetti descritti [nel white paper](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf) di Tresorit.
    - Ernst & Young additionally tested the web, mobile, and desktop clients. They concluded:

        > Test results found no deviation from Tresorit’s data confidentiality claims.

They have also received the Digital Trust Label, a certification from the [Swiss Digital Initiative](https://efd.admin.ch/en/swiss-digital-initiative-en) which requires passing [35 criteria](https://swiss-digital-initiative.org/criteria) related to security, privacy, and reliability.

## Peergos

<div class="admonition recommendation" markdown>

![Peergos logo](assets/img/cloud/peergos.svg){ align=right }

**Peergos** is a decentralized protocol and open-source platform for storage, social media, and applications. It provides a secure and private space where users can store, share, view, and edit their photos, videos, documents, etc.

Peergos secures your files with quantum-resistant E2EE and ensures all data about your files remains private. It is also [self-hostable](https://book.peergos.org/features/self).

[:octicons-home-16: Homepage](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://book.peergos.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/peergos/peergos#support){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=peergos.android)
- [:simple-github: GitHub](https://github.com/Peergos/web-ui/releases)
- [:fontawesome-brands-windows: Windows](https://peergos.org/download#windows)
- [:simple-apple: macOS](https://peergos.org/download#macos)
- [:simple-linux: Linux](https://peergos.org/download#linux)
- [:octicons-browser-16: Web](https://peergos.net)

</details>

</div>

Peergos is built on top of the [InterPlanetary File System (IPFS)](https://ipfs.tech), a peer-to-peer architecture that protects against [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}.

The client, server, and command line interface for Peergos all run from the same binary. Additionally, Peergos includes a [sync engine](https://book.peergos.org/features/sync) (accessible via the native apps) for bi-directionally synchronizing a local folder with a Peergos folder, and a [webdav bridge](https://book.peergos.org/features/webdav) to allow other applications to access your Peergos storage. You can refer to Peergos's documentation for a full overview of their numerous features.

Peergos was [audited](https://peergos.org/posts/security-audit-2024) in November 2024 by Radically Open Security and all issues were fixed. They were previously [audited](https://cure53.de/pentest-report_peergos.pdf) by Cure53 in June 2019, and all found issues were subsequently fixed.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

### Requisiti minimi

- Must enforce E2EE.
- Deve offrire un piano gratuito o un periodo di prova per testarlo.
- Deve supportare TOTP o FIDO2 per l'autenticazione a fattori multipli, oppure il login con le passkey.
- Deve offrire un'interfaccia web che supporti le funzionalità di base per la gestione dei file.
- Deve consentire un'esportazione facile di tutti i file/documenti.

### Miglior Caso

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- I client dovrebbero essere open source.
- Clients should be audited in their entirety by an independent third party.
- Dovrebbero offrire client nativi per Linux, Android, Windows, macOS e iOS.
    - Questi client dovrebbero integrarsi con gli strumenti nativi del sistema operativo per i fornitori dell'archiviazione su cloud, come l'integrazione dell'app Files su iOS o la funzionalità di DocumentsProvider su Android.
- Should support easy file sharing with other users.
- Dovrebbero offrire almeno un'anteprima di base dei file e una funzionalità di modifica sull'interfaccia web.

[^1]: [ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001): La conformità 2013 riguarda la [Gestione della sicurezza informatica](https://en.wikipedia.org/wiki/Information_security_management) dell'azienda e copre la vendita, lo sviluppo, la manutenzione e il supporto dei servizi su cloud.
