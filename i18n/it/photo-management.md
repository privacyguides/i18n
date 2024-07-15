---
title: Gestione delle foto
icon: material/image
description: Strumenti di gestione delle foto per tenere le foto personali al sicuro da occhi indiscreti dei provider di cloud storage e da altri accessi non autorizzati.
cover: photo-management.webp
---

La maggior parte delle soluzioni di gestione delle foto cloud, come Google Photos, Flickr e Amazon Photos, non proteggono le foto dall'accesso da parte dei fornitori di spazio di archiviazione in cloud. Queste opzioni mantengono le foto personali private, consentendo di condividerle solo con i familiari e le persone fidate.

## Ente Photos

<div class="admonition recommendation" markdown>

![Logo di Ente](assets/img/photo-management/ente.svg#only-light){ align=right }
![Logo di Ente](assets/img/photo-management/ente-dark.svg#only-dark){ align=right }

**Ente Photos** è un servizio di backup delle foto crittografato end-to-end che supporta i backup automatici su iOS e Android. Il loro codice è completamente open source, sia dal lato del client che del server. È [ospitabile autonomamente](https://github.com/ente-io/ente/tree/main/server#self-hosting). It underwent an [audit by Cure53](https://ente.io/blog/cryptography-audit) in March 2023 and by [Fallible](https://ente.io/reports/Fallible-Audit-Report-19-04-2023.pdf) in April 2023. La prova gratuita offre 5GB di spazio di archiviazione per un anno.

[:octicons-home-16: Homepage](https://ente.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ente.io/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ente-io/ente){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.photos)
- [:simple-android: Android](https://ente.io/download)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1542026904)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=photos)
- [:fontawesome-brands-windows: Windows](https://ente.io/download)
- [:simple-apple: macOS](https://ente.io/download)
- [:simple-linux: Linux](https://ente.io/download)
- [:octicons-globe-16: Web](https://web.ente.io)

</details>

</div>

## Stingle

<div class="admonition recommendation" markdown>

![Logo Stingle](assets/img/photo-management/stingle.png#only-light){ align=right }
![Logo Stingle](assets/img/photo-management/stingle-dark.png#only-dark){ align=right }

**Stingle** è un'applicazione per gallerie e fotocamere con funzionalità integrate di backup e sincronizzazione crittografata end-to-end per foto e video. Lo storage parte da 1 GB per gli account gratuiti sul loro cloud, oppure puoi ospitare il tuo server API Stingle per una totale indipendenza.

[:octicons-home-16: Homepage](https://stingle.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://stingle.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://stingle.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/stingle){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.stingle.photos)
- [:simple-android: Android](https://f-droid.org/en/packages/org.stingle.photos)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1582535448)
- [:simple-github: GitHub](https://github.com/stingle/stingle-photos-android/releases)

</details>

</div>

## PhotoPrism

<div class="admonition recommendation" markdown>

![Logo PhotoPrism](assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** è una piattaforma self-hostable per la gestione delle foto. It supports album syncing and sharing as well as a variety of other [features](https://photoprism.app/features). Non include E2EE, quindi è meglio che sia ospitato su un server di fiducia e che sia sotto il tuo controllo.

[:octicons-home-16: Homepage](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

### Requisiti minimi

- I provider ospitati in cloud devono applicare la crittografia end-to-end.
- Deve offrire un piano gratuito o un periodo di prova per testarlo.
- Must support TOTP or FIDO2 multi-factor authentication, or passkey logins.
- Deve offrire un'interfaccia web che supporti le funzionalità di base per la gestione dei file.
- Deve consentire un'esportazione facile di tutti i file/documenti.
- Deve utilizzare una crittografia standard e controllata.
- Deve essere open source.

### Miglior Caso

- Dovrebbe disporre di un controllo pubblicato da una terza parte affidabile e indipendente.
