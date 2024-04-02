---
meta_title: "De beste aanbieders van privé- en veilige cloud-opslag - Privacy Guides"
title: "Cloud opslag"
icon: material/file-cloud
description: Veel aanbieders van cloud-opslag eisen jouw volledige vertrouwen dat zij niet in jouw bestanden zullen kijken. Dit zijn de privé alternatieven!
cover: cloud.webp
---

Veel aanbieders van cloud-opslag eisen jouw volledige vertrouwen dat zij niet in jouw bestanden zullen kijken. De onderstaande alternatieven elimineren de noodzaak van vertrouwen door veilige E2EE te implementeren.

Als deze alternatieven niet aan jouw behoeften voldoen, raden wij je aan te kijken naar het gebruik van encryptiesoftware zoals [Cryptomator](encryption.md#cryptomator-cloud) met een andere cloud provider. Het gebruik van Cryptomator in combinatie met **elke** cloud provider (inclusief deze) kan een goed idee zijn om het risico van versleutelingsfouten in de native clients van een provider te verminderen.

<details class="TYPE" markdown>
<summary>Looking for Nextcloud?</summary>

Nextcloud is [still a recommended tool](productivity.md) for self-hosting a file management suite, however we do not recommend third-party Nextcloud storage providers at the moment, because we do [not recommend](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) Nextcloud's built-in E2EE functionality for home users.

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Proton Drive logo](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive** is een E2EE algemene bestandsopslagdienst van de populaire versleutelde e-mailprovider [Proton Mail](email.md#proton-mail).

[:octicons-home-16: Homepage](https://proton.me/drive){ class="md-button md-button--primary" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)
- [:simple-windows11: Windows](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

De Proton Drive webapplicatie is onafhankelijk gecontroleerd door Securitum in [2021](https://proton.me/blog/security-audit-all-proton-apps), volledige details werden niet beschikbaar gesteld, maar in de verklaring van Securitum staat:

> De controleurs ontdekten twee zwakke plekken met een lage ernstgraad. Daarnaast werden vijf algemene aanbevelingen gedaan. Tegelijkertijd bevestigen wij dat tijdens de pentest geen belangrijke beveiligingsproblemen zijn vastgesteld.

Proton Drive's brand new mobile clients have not yet been publicly audited by a third party.

## Tresorit

<div class="admonition recommendation" markdown>

Tresorit logo](assets/img/cloud/tresorit.svg){ align=right }

**Tresorit** is een Zwitsers-Hongaarse aanbieder van versleutelde cloud-opslag, opgericht in 2011. Tresorit is eigendom van de Zwitserse Post, de nationale postdienst van Zwitserland.

[:octicons-home-16: Homepage](https://tresorit.com){ class="md-button md-button--primary" }
[:octicons-eye-16:](https://tresorit.com/legal/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.tresorit.com){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.tresorit.mobile)
- [:simple-appstore: App Store](https://apps.apple.com/app/id722163232)
- [:simple-windows11: Windows](https://tresorit.com/download)
- [:simple-apple: macOS](https://tresorit.com/download)
- [:simple-linux: Linux](https://tresorit.com/download)

</details>

</div>

Tresorit heeft een aantal onafhankelijke beveiligingsaudits ontvangen:

- [2022](https://tresorit.com/blog/tresorit-receives-iso-27001-certification): ISO/IEC 27001:2013[^1] Compliance [Certification](https://certipedia.com/quality_marks/9108644476) by TÜV Rheinland InterCert Kft
- [2021](https://tresorit.com/blog/fresh-penetration-testing-confirms-tresorit-security): Penetration Testing by Computest
    - Bij deze evaluatie is de beveiliging van de Tresorit webclient, Android app, Windows app en bijbehorende infrastructuur beoordeeld.
    - Computest ontdekte twee kwetsbaarheden die zijn opgelost.
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): Penetration Testing by Ernst & Young.
    - Deze evaluatie analyseerde de volledige broncode van Tresorit en bevestigde dat de implementatie overeenkomt met de concepten die zijn beschreven in Tresorit's [white paper](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf).
    - Ernst & Young testte bovendien de web-, mobiele en desktopclients: "Testresultaten vonden geen afwijking van Tresorit's claims over de vertrouwelijkheid van gegevens."

They have also received the Digital Trust Label, a certification from the [Swiss Digital Initiative](https://www.efd.admin.ch/efd/en/home/digitalisierung/swiss-digital-initiative.html) which requires passing [35 criteria](https://digitaltrust-label.swiss/criteria) related to security, privacy, and reliability.

## Peergos

<div class="admonition recommendation" markdown>

![Peergos logo](assets/img/cloud/peergos.svg){ align=right }

**Peergos** is a decentralized protocol and open-source platform for storage, social media, and applications. It provides a secure and private space where users can store, share, and view their photos, videos, documents, etc. Peergos secures your files with quantum-resistant end-to-end encryption and ensures all data about your files remains private. It is built on top of [IPFS (InterPlanetary File System)](https://ipfs.tech).

[:octicons-home-16: Homepage](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://book.peergos.net){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-globe-16: Web](https://peergos.net)
- [:simple-windows11: Windows](https://github.com/Peergos/web-ui/releases)
- [:simple-apple: macOS](https://github.com/Peergos/web-ui/releases)
- [:simple-linux: Linux](https://github.com/Peergos/web-ui/releases)

</details>

</div>

Peergos is primarily a web app, but you can self-host the server either as a local cache for your remote Peergos account, or as a standalone storage server negating the need to register for a remote account and subscription. The Peergos server is a `.jar` file, which means the Java 17+ Runtime Environment ([OpenJDK download](https://azul.com/downloads)) should be installed on your machine to get it working.

Running a local version of Peergos alongside a registered account on their paid, hosted service allows you to access your Peergos storage without any reliance on DNS or TLS certificate authorities, and keep a copy of your data backed up to their cloud. The user experience should be the same whether you run their desktop server or just use their hosted web interface.

Peergos was [audited](https://cure53.de/pentest-report_peergos.pdf) by Cure53 in September 2019, and all found issues were subsequently fixed.

Also, the Android app is not available but it is [in the works](https://discuss.privacyguides.net/t/peergos-private-storage-sharing-social-media-and-application-platform/11825/25). The current workaround is to use the mobile [PWA](https://peergos.net) instead.

## Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

### Minimale vereisten

- Moet end-to-end encryptie afdwingen.
- Moet een gratis plan of proefperiode aanbieden om te testen.
- Moet TOTP of FIDO2 multi-factor authenticatie ondersteunen, of Passkey-logins.
- Moet een webinterface bieden die basisfuncties voor bestandsbeheer ondersteunt.
- Moet gemakkelijke export van alle bestanden/documenten mogelijk maken.
- Gebruik standaard gecontroleerde versleuteling.

### Beste geval

Onze best-case criteria geven aan wat wij zouden willen zien van het perfecte project in deze categorie. Het is mogelijk dat onze aanbevelingen geen of niet alle functies bevatten, maar degene die dat wel doen kunnen hoger gerangschikt worden dan andere op deze pagina.

- Clients should be open source.
- Clients moeten in hun geheel door een onafhankelijke derde partij worden gecontroleerd.
- Moet native clients aanbieden voor Linux, Android, Windows, macOS en iOS.
    - Deze clients moeten integreren met native OS tools voor cloud storage providers, zoals Files app integratie op iOS, of DocumentsProvider functionaliteit op Android.
- Moet het gemakkelijk delen van bestanden met andere gebruikers ondersteunen.
- Moet ten minste een basisfunctionaliteit voor het bekijken en bewerken van bestanden op de webinterface bieden.

[^1]: [De naleving van ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001):2013 heeft betrekking op het beheersysteem voor informatiebeveiliging van het bedrijf [](https://en.wikipedia.org/wiki/Information_security_management) en heeft betrekking op de verkoop, de ontwikkeling, het onderhoud en de ondersteuning van hun clouddiensten.
