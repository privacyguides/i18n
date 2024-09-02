---
title: General Apps
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: General Android Apps
    url: ./
  - "@context": http://schema.org
    "@type": MobileApplication
    name: Shelter
    applicationCategory: Utilities
    operatingSystem: Android
  - "@context": http://schema.org
    "@type": MobileApplication
    name: Secure Camera
    applicationCategory: Utilities
    operatingSystem: Android
  - "@context": http://schema.org
    "@type": MobileApplication
    name: Secure PDF Viewer
    applicationCategory: Utilities
    operatingSystem: Android
robots: nofollow, max-snippet:-1, max-image-preview:large
---

We recommend a wide variety of Android apps throughout this site. The apps listed here are Android-exclusive and specifically enhance or replace key system functionality.

### Shelter

<div class="admonition recommendation" markdown>

![Shelter logo](../assets/img/android/shelter.svg){ align=right }

**Shelter** is an app that helps you leverage Android's Work Profile functionality to isolate or duplicate apps on your device.

Shelter supports blocking contact search cross profiles and sharing files across profiles via the default file manager ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).

[:octicons-repo-16: Repository](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Source Code" }
[:octicons-heart-16:](https://patreon.com/PeterCxy){ .card-link title=Contribute }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warnung</p>

Shelter is recommended over [Insular](https://secure-system.gitlab.io/Insular) and [Island](https://github.com/oasisfeng/island) as it supports [contact search blocking](https://secure-system.gitlab.io/Insular/faq.html).

When using Shelter, you are placing complete trust in its developer, as Shelter acts as a [Device Admin](https://developer.android.com/guide/topics/admin/device-admin) to create the Work Profile, and it has extensive access to the data stored within the Work Profile.

</div>

### Secure Camera

<div class="admonition recommendation" markdown>

![Secure camera Logo](../assets/img/android/secure_camera.svg#only-light){ align=right }
![Secure camera Logo](../assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

**Secure Camera** ist eine Kamera-App, die sich auf Datenschutz und Sicherheit konzentriert und Bilder, Videos und QR-Codes aufnehmen kann. CameraX vendor extensions (Portrait, HDR, Night Sight, Face Retouch, and Auto) are also supported on available devices.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

Main privacy features include:

- Auto removal of [Exif](https://en.wikipedia.org/wiki/Exif) metadata (enabled by default)
- Use of the new [Media](https://developer.android.com/training/data-storage/shared/media) API, therefore [storage permissions](https://developer.android.com/training/data-storage) are not required
- Microphone permission not required unless you want to record sound

<div class="admonition note" markdown>
<p class="admonition-title">Anmerkung</p>

Metadaten werden derzeit nicht aus Videodateien gelöscht, dies ist jedoch geplant.

Die Metadaten zur Bildausrichtung werden nicht gelöscht. Wenn du den Standort (in Secure Camera) aktivierst, wird dieser auch **nicht** gelöscht. Wenn du dies später löschen möchtest, musst du eine externe App wie [ExifEraser](../data-redaction.md#exiferaser-android) verwenden.

</div>

### Secure PDF Viewer

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-target-account: Targeted Attacks](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Passive Attacks](../basics/common-threats.md#security-and-privacy){ .pg-orange }

<div class="admonition recommendation" markdown>

![Secure PDF Viewer Logo](../assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Secure PDF Viewer Logo](../assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

**Secure PDF Viewer** ist ein PDF-Viewer, der auf [pdf.js](https://de.wikipedia.org/wiki/PDF.js) basiert und keine Berechtigungen benötigt. Das PDF wird in eine [sandboxed](https://en.wikipedia.org/wiki/Sandbox_\(software_development\)) [WebView](https://developer.android.com/guide/webapps/webview) eingespeist. Das bedeutet, dass es keine Berechtigung zum direkten Zugriff auf Inhalte oder Dateien benötigt.

[Content-Security-Policy](https://de.wikipedia.org/wiki/Content_Security_Policy) wird verwendet, um zu erzwingen, dass die JavaScript- und Styling-Eigenschaften innerhalb der WebView ausschließlich statische Inhalte sind.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, in Verbindung stehen.** Zusätzlich zu [unseren Standardkriterien](../about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen dir, dich mit der Liste vertraut zu machen, bevor du dich für ein Projekt entscheidest, und deine eigenen Recherchen anzustellen, um sicherzustellen, dass es die richtige Wahl für dich ist.

- Die Anwendungen auf dieser Seite dürfen nicht für eine andere Softwarekategorie auf der Website gelten.
- Allgemeine Anwendungen sollten die Kernfunktionen des Systems erweitern oder ersetzen.
- Die Anwendungen sollten regelmäßig aktualisiert und gewartet werden.
