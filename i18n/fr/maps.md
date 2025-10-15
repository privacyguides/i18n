---
meta_title: "Nos recommandations de cartes et d'applications de navigation - Privacy Guides"
title: Cartes et Navigation
icon: material/map
description: Des cartes et des applications de navigation respectueuses de la vie privée qui n'utilisent pas vos données de recherche et de localisation pour établir un profil publicitaire.
cover: maps.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-account-cash: Capitalisme de Surveillance](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

Utilisez **une carte et une application** de navigation respectueuses de la vie privée qui n'utilisent pas vos données de recherche et de localisation pour établir un profil publicitaire. A la place de Google Maps, Apple Maps ou Waze, nous vous recommandons ces alternatives respectueuses de la vie privée.

Les recommandations formulées ici ne recueillent pas d'informations d'identification personnelle (IPI), conformément à la politique de confidentialité de chaque application. Il n'y a cependant **aucune garantie** que ces politiques de confidentialité soient réellement respectées.

## Organic Maps

<div class="admonition recommendation" markdown>

![Logo de Organic Maps](assets/img/maps/organic-maps.svg){ align=right }

**Organic Maps** is an open-source, community-developed map display and satnav-style navigation app for walkers, drivers, and cyclists. The app offers worldwide, offline maps based on OpenStreetMap data, and navigation with privacy — no location tracking, no data collection, and no ads. The app can be used completely offline.

Features include cycling routes, hiking trails and walking paths, turn-by-turn navigation with voice guidance, and public transport route planning (only available in supported regions and cities).

[:octicons-home-16: Homepage](https://organicmaps.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://organicmaps.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://github.com/organicmaps/organicmaps){ .card-link title="Source Code" }

<details class="downloads" markdown><summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.organicmaps)
- [:simple-appstore: App Store](https://apps.apple.com/app/organic-maps/id1567437057)
- [:simple-github: GitHub](https://github.com/organicmaps/organicmaps/releases)
- [:simple-linux: Linux](https://flathub.org/apps/app.organicmaps.desktop)

</details>

</div>

Please note that Organic Maps is a simple, basic app that lacks certain features many users might expect, such as satellite images, street view images, and real-time traffic information.

## OsmAnd

<div class="admonition recommendation" markdown>

![OsmAnd logo](assets/img/maps/osmand.svg){ align=right }

**OsmAnd** est une application de cartographie et de navigation hors ligne basée sur OpenStreetMap qui offre une navigation immersive pour la marche, le vélo, la conduite, ainsi que les transports publics. You can find a detailed overview of OsmAnd's supported [features](https://wiki.openstreetmap.org/wiki/OsmAnd#Features) on the OpenStreet Map Wiki.

[:octicons-home-16: Homepage](https://osmand.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://osmand.net/docs/legal/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://osmand.net/docs/intro){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/osmandapp){ .card-link title="Source Code" }

<details class="downloads" markdown><summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.osmand)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/id934850257)
- [:simple-android: Android](https://osmand.net/docs/versions/free-versions)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Identifiant unique de l'utilisateur</p>

OsmAnd génère un [identifiant unique de l'utilisateur (UUID)](https://osmand.net/docs/legal/terms-of-use/#6-unique-user-indentifier) pour chaque  application installée qui tourne tous les trois mois et qui est utilisé pour les rapports internes et les statistiques. L'UUID est également envoyé aux serveurs d'OsmAnd lors du téléchargement des cartes. Sur Android, un paramètre permet de contrôler si l'UUID est envoyé avec chaque demande de téléchargement. Depuis l'écran d'accueil, allez sur :material-menu: → :gear: **Réglages** → :gear: **Réglages OsmAnd** → :material-web: **Identifiants**.

- [ ] Décochez **Envoyer l'identifiant unique de l'utilisateur (UUID)**

Ce paramètre n'est pas disponible sur l'application iOS.

</div>

L'application comprend également un paramètre permettant de partager des données anonymes sur les cartes téléchargées et les fonctions utilisées. Ce paramètre est désactivé par défaut sur Android, mais activé par défaut sur iOS. Pour la désactiver dans l'application iOS, touchez le site :material-menu: sur l'écran d'accueil pour accéder au menu **Réglages** de :gear: . Sélectionnez cette option, puis :gear: **OsmAnd settings**.

- [ ] Décochez **Envoyer des données anonymes**

OsmAnd allows you to overlay or underlay external map data, such as satellite images from Microsoft or [traffic data](https://themm.net/public/osmand_traffic) from Google, although the latter is ignored by the automatic route planning. OsmAnd also has an optional integration of street view images provided by [Mapillary](https://mapillary.com).

## Critères

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Must not collect PII per their privacy policy.
- Must not require users to create an account with them.
- Must not require users to share location data. If the user opts in to sharing their location, this data must be anonymized.
- Must retain core functionality when offline and allow users to download maps for offline use.

### Dans le meilleur des cas

Nos critères de cas idéal représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de cette fonctionnalité, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Apps should be open source.
- Should have route planning for public transport.
- Should have real-time traffic information for route planning.
- Should support advanced features such as detailed shop/point of interest (POI) information and reviews, topographic maps, and satellite and street view images.
