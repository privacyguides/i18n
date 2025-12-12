---
title: "Ogólne aplikacje"
description: Aplikacje wymienione poniżej są dostępne wyłącznie na Androida i stanowią rozszerzenie lub zamiennik kluczowych funkcji systemowych.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Ogólne aplikacje na Androida
    url: "./"
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

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-bug-outline: Ataki pasywne](../basics/common-threats.md#security-and-privacy){ .pg-orange }

Zamieszczamy tu szerokie zalecenia dotyczące aplikacji na Androida. Aplikacje wymienione poniżej są dostępne wyłącznie na Androida i stanowią rozszerzenie lub zamiennik kluczowych funkcji systemowych.

### Shelter

Jeśli Twoje urządzenie działa na Androidzie 15 lub nowszym, zalecamy zamiast tego skorzystanie z natywnej funkcji [Przestrzeni prywatnej](../os/android-overview.md#private-space), która oferuje niemal te same możliwości, bez potrzeby obdarzania zaufaniem aplikacji firm trzecich i przyznawania im rozległych uprawnień.

<div class="admonition recommendation" markdown>

![Logo Shelter](../assets/img/android/shelter.svg){ align=right }

**Shelte**r to aplikacja, która pomaga wykorzystać funkcję profilu służbowego w Androidzie do izolowania lub duplikowania aplikacji na urządzeniu.

Shelter umożliwia blokowanie wyszukiwania kontaktów między profilami oraz udostępnianie plików między profilami za pośrednictwem domyślnego menedżera plików ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).

[:octicons-repo-16: Repozytorium](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://patreon.com/PeterCxy){ .card-link title=Wesprzyj }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

Korzystając z aplikacji Shelter, należy całkowicie zaufać jego twórcy, ponieważ Shelter działa jako [administrator urządzenia](https://developer.android.com/guide/topics/admin/device-admin) w celu utworzenia profilu służbowego i ma szeroki dostęp do danych przechowywanych w tym profilu.

</div>

Shelter jest zalecany zamiast aplikacji [Insular](https://secure-system.gitlab.io/Insular) i [Island](https://github.com/oasisfeng/island), ponieważ obsługuje [blokowanie wyszukiwania kontaktów](https://secure-system.gitlab.io/Insular/faq.html).

### Secure Camera

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-account-search: Ekspozycja publiczna](../basics/common-threats.md#limiting-public-information){ .pg-green }

<div class="admonition recommendation" markdown>

![Logo Secure Camera](../assets/img/android/secure_camera.svg#only-light){ align=right }
![Logo Secure Camera](../assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

**Secure Camera** is a camera app focused on privacy and security which can capture images, videos, and QR codes. CameraX vendor extensions (Portrait, HDR, Night Sight, Face Retouch, and Auto) are also supported on available devices.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/Camera#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Pobierz</summary>

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
<p class="admonition-title">Uwaga</p>

Metadata is not currently deleted from video files, but that is planned.

The image orientation metadata is not deleted. If you enable location (in Secure Camera) that **won't** be deleted either. If you want to delete that later you will need to use an external app such as [ExifEraser](../data-redaction.md#exiferaser-android).

</div>

### Secure PDF Viewer

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-target-account: Ataki ukierunkowane](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }

<div class="admonition recommendation" markdown>

![Logo Secure PDF Viewer](../assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Logo Secure PDF Viewer](../assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

**Secure PDF Viewer** is a PDF viewer based on [pdf.js](https://en.wikipedia.org/wiki/PDF.js) that doesn't require any permissions. The PDF is fed into a [sandboxed](https://en.wikipedia.org/wiki/Sandbox_\(software_development\)) [WebView](https://developer.android.com/guide/webapps/webview). This means that it doesn't require permission directly to access content or files.

[Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) is used to enforce that the JavaScript and styling properties within the WebView are entirely static content.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer#readme){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](../about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

- Applications on this page must not be applicable to any other software category on the site.
- General applications should extend or replace core system functionality.
- Applications should receive regular updates and maintenance.
