---
title: File Management
meta_title: "Self-Hosting File Management Tools - Privacy Guides"
icon: material/file-multiple-outline
description: For our more technical readers, self-hosting file management tools can provide additional privacy assurances by having maximum control over your data.
cover: cloud.webp
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-server-network: Usługodawcy](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

Self-hosting your own **file management** tools may be a good idea to reduce the risk of encryption flaws in a cloud provider's native clients.

## Zarządzanie zdjęciami

### PhotoPrism

<div class="admonition recommendation" markdown>

![Logo PhotoPrism](../assets/img/self-hosting/photoprism.svg){ align=right }

**PhotoPrism** to platforma do zarządzania zdjęciami. Obsługuje synchronizację i udostępnianie albumów oraz szereg innych [funkcji](https://photoprism.app/features). Nie oferuje jednak szyfrowania typu end-to-end, dlatego najlepiej hostować ją na zaufanym serwerze, nad którym masz pełną kontrolę.

[:octicons-home-16: Strona główna](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Kod źródłowy" }

</div>

## Udostępnianie i synchronizacja plików

### FreedomBox

<div class="admonition recommendation" markdown>

![Logo FreedomBox](../assets/img/self-hosting/freedombox.svg){ align=right }

**FreedomBox** is an operating system designed to be run on a [single-board computer (SBC)](https://en.wikipedia.org/wiki/Single-board_computer). The purpose is to make it easy to set up server applications for use cases like sharing files.

[:octicons-home-16: Strona główna](https://freedombox.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://freedomboxfoundation.org/donate){ .card-link title="Wesprzyj" }

</div>

### Nextcloud

<div class="admonition recommendation" markdown>

![Logo Nextcloud](../assets/img/self-hosting/nextcloud.svg){ align=right }

**Nextcloud** is a suite of free and open-source client-server software for creating your own file hosting services on a private server you control.

[:octicons-home-16: Strona główna](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title="Wesprzyj" }

<details class="downloads" markdown><0>Pobierz</0>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
- [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
- [:fontawesome-brands-windows: Windows](https://nextcloud.com/install/#install-clients)
- [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
- [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Zagrożenie</p>

We don't recommend using the [E2EE App](https://apps.nextcloud.com/apps/end_to_end_encryption) for Nextcloud as it may lead to data loss; it is highly experimental and not production quality. For this reason, we don't recommend third-party Nextcloud providers.

</div>
