---
meta_title: "App raccomandate di mappe e navigazione - Privacy Guides"
title: Mappe e Navigazione
icon: material/map
description: Applicazioni di mappe e navigazione che rispettano la tua privacy e non costruiscono un profilo pubblicitario basato sulle tue ricerche e posizioni.
cover: maps.webp
---

<small>Protezione dalle seguenti minacce:</small>

- [:material-account-cash: Capitalismo della sorveglianza](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

Usa un'**app di mappe e navigazione** che non costruisce un profilo pubblicitario basato sulla cronologia delle tue ricerche e posizioni. Invece di utilizzare Google Maps, Apple Maps o Waze noi consigliamo queste alternative rispettose della privacy.

The recommendations here do not collect personally identifying information (PII) based on each application's privacy policy. **Non c'è garanzia** che queste informative sulla privacy siano rispettate.

## Organic Maps

<div class="admonition recommendation" markdown>

![Logo di Organic Maps](assets/img/maps/organic-maps.svg){ align=right }

**Organic Maps** è un'applicazione open-source, sviluppata dalla comunità per mappe e navigazione, per escursionisti, automobilisti e ciclisti. L'app offre mappe offline di tutto il mondo basate su dati di OpenStreetMap e navigazione privata — nessun tracciamento della posizione, nessuna raccolta di dati e nessun annuncio. L'app può essere utilizzata completamente offline.

Le funzioni includono percorsi ciclistici, sentieri escursionistici e pedonali, navigazione passo-passo con indicazioni vocali e pianificazione del percorso con i trasporti pubblici (disponibile solamente in regioni e città supportate).

[:octicons-home-16: Homepage](https://organicmaps.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://organicmaps.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://github.com/organicmaps/organicmaps){ .card-link title="Source Code" }

<details class="downloads" markdown><0>Scarica</0>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.organicmaps)
- [:simple-appstore: App Store](https://apps.apple.com/app/organic-maps/id1567437057)
- [:simple-github: GitHub](https://github.com/organicmaps/organicmaps/releases)
- [:simple-linux: Linux](https://flathub.org/apps/app.organicmaps.desktop)

</details>

</div>

Tieni presente che Organic Maps è un'app semplice e di base che non include alcune funzioni che molti utenti si aspettano, come immagini satellitari, vista stradale e informazioni sul traffico in tempo reale.

## OsmAnd

<div class="admonition recommendation" markdown>

![Logo di OsmAnd](assets/img/maps/osmand.svg){ align=right }

**OsmAnd** is an open-source, offline map and navigation application based on OpenStreetMap that offers turn-by-turn navigation for walking, cycling, driving, as well as public transport. Puoi trovare un elenco dettagliato delle [funzioni](https://wiki.openstreetmap.org/wiki/OsmAnd#Features) supportate da OsmAnd sulla Wiki di OpenStreetMap.

[:octicons-home-16: Homepage](https://osmand.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://osmand.net/docs/legal/privacy-policy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://osmand.net/docs/intro){ .card-link title="Documentazione" }
[:octicons-code-16:](https://github.com/osmandapp){ .card-link title="Codice Sorgente" }

<details class="downloads" markdown><summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.osmand)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/id934850257)
- [:simple-android: Android](https://osmand.net/docs/versions/free-versions)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Unique User Identifier</p>

OsmAnd generates a [unique user identifier (UUID)](https://osmand.net/docs/legal/terms-of-use/#6-unique-user-indentifier) for each app install that rotates every three months and is used for internal reports and statistics. The UUID is also sent to OsmAnd's servers when downloading maps. On Android, there is a setting that controls whether the UUID is sent with each download request. From the home screen, go to :material-menu: → :gear: **Settings** → :gear: **OsmAnd settings** → :material-web: **Identifiers**.

- [ ] Uncheck **Send Unique User Identifier (UUID)**

This setting is not available on the iOS app.

</div>

The app also includes a setting for sharing anonymous data about your downloaded maps and the features you use. This setting is disabled by default on Android, but enabled by default on iOS. To disable it in the iOS app, tap the :material-menu: on the home screen to find the :gear: **Settings** menu. Select that, then select :gear: **OsmAnd settings**.

- [ ] Uncheck **Send anonymous data**

OsmAnd consente di sovrapporre dati cartografici esterni, come le immagini satellitari di Microsoft o [dati sul traffico](https://themm.net/public/osmand_traffic) di Google, anche  se questi ultimi vengono ignorati dalla pianificazione automatica del percorso. OsmAnd dispone anche di un'integrazione opzionale per vedere immagini di vista stradale fornite [Mapillary](https://mapillary.com).

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto che consigliamo.** Oltre ai nostri [criteri standard](about/criteria.md), abbiamo sviluppato un chiaro insieme di requisiti per consentirci di fornire dei consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

### Requisiti minimi

- Non deve raccogliere informazioni d'identificazione personale secondo l'informativa sulla privacy.
- Non deve richiedere la creazione di un account da parte degli utenti.
- Non deve richiedere agli utenti di condividere i dati sulla posizione. Se l'utente acconsente a condividere la propria posizione questi dati devono essere anonimizzati.
- Deve mantenere le funzionalità di base anche offline e consente agli utenti di scaricare le mappe per utilizzarle offline.

### Caso migliore

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- L'app dovrebbe essere open source.
- Dovrebbe supportare di pianificare il percorso con i trasporti pubblici.
- Dovrebbe avere informazioni sul traffico in tempo reale per pianificare il percorso.
- Dovrebbe supportare funzioni avanzate come informazioni dettagliate su negozi e punti d'interesse (POI), recensioni, mappe topografiche e immagini satellitari e di vista stradale.
