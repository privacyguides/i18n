---
title: Gestione delle foto
icon: material/image
description: Questi strumenti per la gestione delle foto tengono le tue foto personali al riparo dagli occhi indiscreti dei fornitori di servizi di archiviazione su cloud e di altre parti non autorizzate.
cover: photo-management.webp
---

<small>Protezione dalle seguenti minacce:</small>

- [:material-bug-outline: Attacchi Passivi](basics/common-threats.md#security-and-privacy){ .pg-orange }
- [:material-server-network: Fornitori di Servizi ](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

La maggior parte delle **soluzioni di gestione delle foto** come Google Foto, Flickr e Amazon Foto non proteggono l'accesso alle tue foto da parte degli stessi fornitori di archiviazione cloud. Queste opzioni mantengono le foto personali private, consentendo di condividerle solo con i familiari e le persone fidate.

## Ente Foto

<div class="admonition recommendation" markdown>

![Logo di Ente](assets/img/photo-management/ente.svg){ align=right }

**Ente Foto** è un servizio di backup delle foto crittografato end-to-end che supporta i backup automatici su iOS e Android. Il codice sorgente è completamente open source, sia lato client che lato server. È anche [self hostable](https://github.com/ente-io/ente/tree/main/server#self-hosting).

The free plan offers 10 GB of storage as long as you use the service at least once a year.

[:octicons-home-16: Homepage](https://ente.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://ente.io/faq){ .card-link title="Documentazione" }
[:octicons-code-16:](https://github.com/ente-io/ente){ .card-link title="Codice Sorgente" }

<details class="downloads" markdown><0>Scarica</0>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.photos)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1542026904)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=photos)
- [:simple-android: Android](https://ente.io/download)
- [:fontawesome-brands-windows: Windows](https://ente.io/download)
- [:simple-apple: macOS](https://ente.io/download)
- [:simple-linux: Linux](https://ente.io/download)
- [:octicons-browser-16: Web](https://web.ente.io)

</details>

</div>

Ente Photos underwent an audit by [Cure53](https://ente.io/blog/cryptography-audit) in March 2023 and by [Fallible](https://ente.io/reports/Fallible-Audit-Report-19-04-2023.pdf) in April 2023.

## PhotoPrism

<div class="admonition recommendation" markdown>

![Logo di PhotoPrism](assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** è una piattaforma self-hostable per la gestione delle foto. Supporta la sincronizzazione e la condivisione degli album e molte altre [funzioni](https://photoprism.app/features). Non include E2EE, quindi è preferibile che venga ospitato su un server di cui ti fidi e che è sotto il tuo controllo.

[:octicons-home-16: Homepage](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Codice Sorgente" }

<details class="downloads" markdown><0>Scarica</0>

- [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto che consigliamo.** Oltre ai nostri [criteri standard](about/criteria.md), abbiamo sviluppato un chiaro insieme di requisiti per consentirci di fornire dei consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

### Requisiti minimi

- I servizi ospitati sul cloud devono avere la crittografia end-to-end (E2EE)
- Deve offrire un piano gratuito o un periodo di prova per testarlo.
- Deve supportare TOTP o FIDO2 per l'autenticazione a fattori multipli, oppure il login con le passkey.
- Deve offrire un'interfaccia web che supporti le funzionalità di base per la gestione dei file.
- Deve consentire un'esportazione facile di tutti i file/documenti.
- Deve essere open source.

### Miglior Caso

- Dovrebbe avere una recensione (audit) pubblicata da una terza parte rispettabile e indipendente.
