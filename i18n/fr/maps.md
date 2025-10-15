---
meta_title: "Nos recommandations de cartes et d'applications de navigation - Privacy Guides"
title: Cartes et Navigation
icon: material/map
description: Des cartes et des applications de navigation respectueuses de la vie privée qui n'utilisent pas vos données de recherche et de localisation pour établir un profil publicitaire.
cover: maps.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-account-cash: Capitalisme de Surveillance](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

Utilisez **une application de carte et de navigation** respectueuse de la vie privée qui n'utilise pas vos données de recherche et de localisation pour établir un profil publicitaire. A la place de Google Maps, Apple Maps ou Waze, nous vous recommandons ces alternatives respectueuses de la vie privée.

Les recommandations formulées ici ne recueillent pas d'Informations Personnellement Identifiables (IPI), conformément à la politique de confidentialité de chaque application. Il n'y a cependant **aucune garantie** que ces politiques de confidentialité soient réellement respectées.

## Organic Maps

<div class="admonition recommendation" markdown>

![Logo de Organic Maps](assets/img/maps/organic-maps.svg){ align=right }

**Organic Maps** est une application open-source de navigation type GPS et de carte pour les marcheurs, cyclistes et conducteurs. L'application permet d'accéder à des cartes du monde entier basées sur les données OpenStreetMap, elle dispose également d'une fonctionnalité de navigation respectueuse de la vie privée (pas de traçage de la localisation, pas de collecte de donnée, et pas de publicités). Cette application peut être utilisée hors-ligne.

Parmi les fonctionnalités de l'application on retrouve les itinéraires cyclables, les chemins de randonnée et de promenade, la navigation tour par tour avec guidage vocal et la planification d'itinéraire en transport en communs (uniquement disponible pour certaines régions ou villes).

[:octicons-home-16: Page d'Accueil](https://organicmaps.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://organicmaps.app/privacy){ .card-link title="Politique de confidentialité" }
[:octicons-code-16:](https://github.com/organicmaps/organicmaps){ .card-link title="Code Source" }

<details class="downloads" markdown><summary>Télécharger</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.organicmaps)
- [:simple-appstore: App Store](https://apps.apple.com/app/organic-maps/id1567437057)
- [:simple-github: GitHub](https://github.com/organicmaps/organicmaps/releases)
- [:simple-linux: Linux](https://flathub.org/apps/app.organicmaps.desktop)

</details>

</div>

Organic Maps reste une application assez basique, et ne propose pas certaines fonctionnalités avancées comme les images satellites, le street view ou les informations de trafic en temps réel.

## OsmAnd

<div class="admonition recommendation" markdown>

![Logo de OsmAnd](assets/img/maps/osmand.svg){ align=right }

**OsmAnd** est une application de carte et de navigation hors ligne basée sur OpenStreetMap qui offre une navigation tour par tour pour la marche, le vélo, la conduite, ainsi que les transports publics. Vous pouvez trouver la liste détaillée des [fonctionnalités](https://wiki.openstreetmap.org/wiki/OsmAnd#Features) d'OsmAnd sur le wiki OpenStreetMap.

[:octicons-home-16: Page d'Accueil](https://osmand.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://osmand.net/docs/legal/privacy-policy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://osmand.net/docs/intro){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/osmandapp){ .card-link title="Code Source" }

<details class="downloads" markdown><summary>Télécharger</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.osmand)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/id934850257)
- [:simple-android: Android](https://osmand.net/docs/versions/free-versions)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Identifiant unique de l'utilisateur</p>

OsmAnd génère un [identifiant unique de l'utilisateur (UUID)](https://osmand.net/docs/legal/terms-of-use/#6-unique-user-indentifier) pour chaque application installée qui tourne tous les trois mois et qui est utilisé pour les rapports internes et les statistiques. L'UUID est également envoyé aux serveurs d'OsmAnd lors du téléchargement des cartes. Sur Android, un paramètre permet de contrôler si l'UUID est envoyé avec chaque demande de téléchargement. Depuis l'écran d'accueil, allez dans :material-menu: → :gear: **Réglages** → :gear: **Réglages OsmAnd** → :material-web: **Identifiants**.

- [ ] Décochez **Envoyer l'identifiant unique de l'utilisateur (UUID)**

Ce paramètre n'est pas disponible sur l'application iOS.

</div>

L'application comprend également un paramètre permettant de partager des données anonymes sur les cartes téléchargées et les fonctions utilisées. Ce paramètre est désactivé par défaut sur Android, mais activé par défaut sur iOS. Pour la désactiver dans l'application iOS, touchez :material-menu: sur l'écran d'accueil pour accéder au menu :gear: des **Réglages** . Sélectionnez cette option, puis :gear: **OsmAnd settings**.

- [ ] Décochez **Envoyer des données anonymes**

OsmAnd vous permet de superposer des données cartographiques, par exemple des images satellite de Microsoft ou des [données sur le trafic](https://themm.net/public/osmand_traffic) de Google, bien que ces dernières ne soient pas prises en compte par le calcul d'itinéraires. Vous pouvez également intégrer les images street view de [Mapillary](https://mapillary.com) si vous le souhaitez.

## Critères

**Nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de nos [critères de base](about/criteria.md), nous avons mis en place un ensemble d'exigences clair qui nous permet d'établir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de faire votre choix, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Ne dois pas collecter d'IPI (Informations Personnellement Identifiables), conformément à leur politique de confidentialité.
- Les utilisateurs ne doivent pas être obligés de créer un compte pour utiliser le service.
- Les utilisateurs ne doivent pas obligés de partager leurs données de localisation. Si l'utilisateur choisit de partager sa localisation, celle-ci doit être anonymisée.
- Dois permettre d'utiliser un maximum de fonctionnalités hors-ligne et permettre aux utilisateurs de télécharger les cartes pour une utilisation hors-ligne.

### Fonctionnalités idéales

Nos critères optimaux représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de ces fonctionnalités, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Etre open-source.
- Possibilité de planifier des itinéraires en transport en commun.
- Informations sur le trafic en temps réel pour la planification d'itinéraires.
- Fonctionnalités avancées comme des cartes topographiques, des images satellites et street view ou encore des informations détaillées et des avis sur les commerces ou les points d'intérêt.
