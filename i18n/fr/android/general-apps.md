---
title: "Applications générales"
description: Les applications répertoriées ici sont exclusives à Android et améliorent ou remplacent les principales fonctionnalités du système.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Applications Android génériques
    url: "./"
  - "@context": http://schema.org
    "@type": ApplicationMobile
    name: Shelter
    applicationCategory: Utilitaire
    operatingSystem: Android
  - "@context": http://schema.org
    "@type": ApplicationMobile
    name: Secure Camera
    applicationCategory: Utilitaire
    operatingSystem: Android
  - "@context": http://schema.org
    "@type": ApplicationMobile
    name: Secure PDF Viewer
    applicationCategory: Utilitaire
    operatingSystem: Android
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Protège contre les menaces suivantes :</small>

- [:material-bug-outline: Attaques passives](../basics/common-threats.md#security-and-privacy){ .pg-orange }

Nous recommandons une grande variété d'applications Android sur ce site. Les applications répertoriées ici sont exclusives à Android et améliorent ou remplacent les principales fonctionnalités du système.

### Shelter

Si votre appareil fonctionne sous Android 15 ou supérieur, nous vous recommandons d'utiliser la fonction native [Espace privé] (../os/android-overview.md#private-space), qui offre pratiquement la même fonctionnalité sans avoir à faire confiance à une application tierce et à lui accorder de puissantes autorisations.

<div class="admonition recommendation" markdown>

![Shelter logo](../assets/img/android/shelter.svg){ align=right }

**Shelter** est une application qui vous aide à tirer parti des fonctionnalités du profil professionnel d'Android pour isoler ou dupliquer des applications sur votre appareil.

Shelter prend en charge le blocage de la recherche de contacts entre profils et le partage de fichiers entre profils via le gestionnaire de fichiers par défaut ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).

[:octicons-repo-16: Répertoire](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Code Source" }
[:octicons-heart-16:](https://patreon.com/PeterCxy){ .card-link title=Contribuer }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

En utilisant Shelter, vous accordez une confiance totale à son développeur, car Shelter agit en tant qu'[administrateur de l'appareil](https://developer.android.com/guide/topics/admin/device-admin) pour créer le Profil professionnel, et il a un accès étendu aux données stockées dans ce dernier.

</div>

Shelter est recommandé par rapport à [Insular](https://secure-system.gitlab.io/Insular) et [Island](https://github.com/oasisfeng/island) car il permet le [blocage de la recherche de contact](https://secure-system.gitlab.io/Insular/faq.html).

### Secure Camera

<small>Protège contre la(les) menace(s) suivante(s)</small>

- [:material-account-search: Exposition Publique](../basics/common-threats.md#limiting-public-information){ .pg-green }

<div class="admonition recommendation" markdown>

![logo de Secure camera](../assets/img/android/secure_camera.svg#only-light){ align=right }
![logo de Secure camera](../assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

**Secure Camera** est une application de caméra axée sur la confidentialité et la sécurité qui permet de capturer des images, des vidéos et des codes QR. Les extensions du vendeur CameraX (Portrait, HDR, Night Sight, Face Retouch et Auto) sont également prises en charge sur les appareils disponibles.

[:octicons-repo-16: Répertoire](https://github.com/GrapheneOS/Camera#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Code Source" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contrribuer }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: Magasin d'applications de GrapheneOS](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

Les principales fonctionnalités de confidentialité incluent :

- Suppression automatique des métadonnées [Exif](https://en.wikipedia.org/wiki/Exif) (activée par défaut)
- Utilisation de la nouvelle API [Media](https://developer.android.com/training/data-storage/shared/media), par conséquent les [autorisations de stockage](https://developer.android.com/training/data-storage) ne sont pas nécessaires
- L'autorisation d'utiliser un microphone n'est pas nécessaire, sauf si vous souhaitez enregistrer du son

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Les métadonnées ne sont pour le moment pas supprimées des fichiers vidéo, mais cela est prévu.

Les métadonnées d'orientation de l'image ne sont pas supprimées. Si vous activez la fonction de localisation (dans Secure Camera), elle ne **sera pas** non plus supprimée. Si vous voulez la supprimer ultérieurement, vous devrez utiliser une application externe telle que [ExifEraser](../data-redaction.md#exiferaser-android).

</div>

### Secure PDF Viewer

<small>Protège contre la(les) menace(s) suivante(s) :</small>

- [:material-target-account: Attaques ciblées](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }

<div class="admonition recommendation" markdown>

![logo de Secure PDF Viewer](../assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![logo de Secure PDF Viewer](../assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

**Secure PDF Viewer** est une visionneuse de PDF basée sur [pdf.js](https://en.wikipedia.org/wiki/PDF.js) qui ne nécessite aucune permission. Le PDF est introduit dans une [webview](https://developer.android.com/guide/webapps/webview) [sandboxée](https://en.wikipedia.org/wiki/Sandbox_\(software_development\)). Cela signifie qu'il n'a pas besoin d'autorisation directe pour accéder au contenu ou aux fichiers.

[Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) est utilisé pour s'assurer que les propriétés JavaScript et de style à l'intérieur de la WebView sont entièrement statiques.

[:octicons-repo-16: Répertoire](https://github.com/GrapheneOS/PdfViewer#readme){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Code Source" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: Magasin d'applications de GrapheneOS](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](../about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

- Les applications de cette page ne doivent pas être applicables à une autre catégorie de logiciels sur le site.
- Les applications générales doivent étendre ou remplacer les fonctionnalités de base du système.
- Les applications doivent être régulièrement mises à jour et maintenues.
