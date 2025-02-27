---
title: Allgemeine Apps
description: Die hier aufgeführten Apps sind Android-exklusiv und verbessern oder ersetzen wichtige Systemfunktionen.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Allgemeine Android-Apps
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

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-bug-outline: Passive Angriffe](../basics/common-threats.md#security-and-privacy){ .pg-orange }

Wir empfehlen auf dieser Website eine Vielzahl von Android-Apps. Die hier aufgeführten Apps sind Android-exklusiv und verbessern oder ersetzen wichtige Systemfunktionen.

### Shelter

If your device is on Android 15 or greater, we recommend using the native [Private Space](../os/android-overview.md#private-space) feature instead, which provides nearly the same functionality without needing to place trust in and grant powerful permissions to a third-party app.

<div class="admonition recommendation" markdown>

![Shelter Logo](../assets/img/android/shelter.svg){ align=right }

**Shelter** ist eine App, die dir hilft, die Arbeitsprofilfunktion von Android ausnutzen, um Anwendungen auf deinem Gerät zu isolieren oder zu duplizieren.

Shelter unterstützt die profilübergreifende Kontaktsuche und Freigabe von Dateien über den Standard-Dateimanager ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).

[:octicons-repo-16: Repository](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://patreon.com/PeterCxy){ .card-link title=Mitwirken }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warnung</p>

Bei der Verwendung von Shelter vertraust du vollständig dem Entwickler, da Shelter als [Geräteadministrator](https://developer.android.com/guide/topics/admin/device-admin) fungiert, um das Arbeitsprofil zu erstellen, und es hat umfassenden Zugriff auf die Daten, die im Arbeitsprofil gespeichert sind.

</div>

Shelter wird gegenüber [Insular](https://secure-system.gitlab.io/Insular) und [Island](https://github.com/oasisfeng/island) empfohlen, da es das [Blockieren der Kontaktsuche](https://secure-system.gitlab.io/Insular/faq.html) unterstützt.

### Secure Camera

<small>Protects against the following threat(s):</small>

- [:material-account-search: Public Exposure](../basics/common-threats.md#limiting-public-information){ .pg-green }

<div class="admonition recommendation" markdown>

![Secure camera Logo](../assets/img/android/secure_camera.svg#only-light){ align=right }
![Secure camera Logo](../assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

**Secure Camera** ist eine Kamera-App, die sich auf Datenschutz und Sicherheit konzentriert und Bilder, Videos und QR-Codes aufnehmen kann. CameraX Herstellererweiterungen (Porträt, HDR, Nachtsicht, Gesichtsretusche und Auto) sind auf unterstützten Geräten ebenfalls verfügbar.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Dokumentation}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Spenden }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

Zu den wichtigsten Privatsphäre-Funktionen gehören:

- Automatisches Entfernen von [Exif](https://de.wikipedia.org/wiki/Exchangeable_Image_File_Format) Metadaten (standardmäßig aktiviert)
- Verwendung der neuen [Medien](https://developer.android.com/training/data-storage/shared/media) API, daher sind [Speicherberechtigungen](https://developer.android.com/training/data-storage) nicht erforderlich
- Mikrofonberechtigung nicht erforderlich, es sei denn, du möchtest Ton aufnehmen

<div class="admonition note" markdown>
<p class="admonition-title">Anmerkung</p>

Metadata is not currently deleted from video files, but that is planned.

Die Metadaten zur Bildausrichtung werden nicht gelöscht. Wenn du den Standort (in Secure Camera) aktivierst, wird dieser auch **nicht** gelöscht. Wenn du dies später löschen möchtest, musst du eine externe App wie [ExifEraser](../data-redaction.md#exiferaser-android) verwenden.

</div>

### Secure PDF Viewer

<small>Protects against the following threat(s):</small>

- [:material-target-account: Targeted Attacks](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }

<div class="admonition recommendation" markdown>

![Secure PDF Viewer Logo](../assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Secure PDF Viewer Logo](../assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

**Secure PDF Viewer** ist ein PDF-Viewer, der auf [pdf.js](https://de.wikipedia.org/wiki/PDF.js) basiert und keine Berechtigungen benötigt. Das PDF wird in eine [sandboxed](https://en.wikipedia.org/wiki/Sandbox_\(software_development\)) [WebView](https://developer.android.com/guide/webapps/webview) eingespeist. Das bedeutet, dass es keine Berechtigung zum direkten Zugriff auf Inhalte oder Dateien benötigt.

[Content-Security-Policy](https://de.wikipedia.org/wiki/Content_Security_Policy) wird verwendet, um zu erzwingen, dass die JavaScript- und Styling-Eigenschaften innerhalb der WebView ausschließlich statische Inhalte sind.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Spenden }

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
