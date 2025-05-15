---
meta_title: "De beste aanbieders van privé- en veilige cloud-opslag - Privacy Guides"
title: "Cloud opslag"
icon: material/file-cloud
description: Veel aanbieders van cloud-opslag eisen jouw volledige vertrouwen dat zij niet in jouw bestanden zullen kijken. Dit zijn de privé alternatieven!
cover: cloud.webp
---

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: Passieve aanvallen](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Dienstverleners](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Many **cloud storage providers** require your full trust that they will not look at your files. The alternatives listed below eliminate the need for trust by implementing secure end-to-end encryption.

Als deze alternatieven niet aan jouw behoeften voldoen, raden wij je aan te kijken naar het gebruik van encryptiesoftware zoals [Cryptomator](encryption.md#cryptomator-cloud) met een andere cloud provider. Het gebruik van Cryptomator in combinatie met **elke** cloud provider (inclusief deze) kan een goed idee zijn om het risico van versleutelingsfouten in de native clients van een provider te verminderen.

<details class="admonition info" markdown>
<summary>Looking for Nextcloud?</summary>

Nextcloud is [still a recommended tool](document-collaboration.md#nextcloud) for self-hosting a file management suite, however we do not recommend third-party Nextcloud storage providers at the moment, because we do [not recommend](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) Nextcloud's built-in E2EE functionality for home users.

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Proton Drive logo](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive** is an encrypted cloud storage provider from the popular encrypted email provider [Proton Mail](email.md#proton-mail).

The initial free storage is limited to 2 GB, but with the completion of [certain steps](https://proton.me/support/more-free-storage-existing-users), additional storage can be obtained up to 5 GB.

[:octicons-home-16: Homepage](https://proton.me/drive){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/drive/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)
- [:fontawesome-brands-windows: Windows](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

The Proton Drive web application has been independently audited by Securitum in [2021](https://proton.me/community/open-source), but the brand new mobile clients have not yet been publicly audited by a third party.

## Tresorit

<div class="admonition recommendation" markdown>

Tresorit logo](assets/img/cloud/tresorit.svg){ align=right }

**Tresorit** is een Zwitsers-Hongaarse aanbieder van versleutelde cloud-opslag, opgericht in 2011. Tresorit is eigendom van de Zwitserse Post, de nationale postdienst van Zwitserland.

[:octicons-home-16: Homepage](https://tresorit.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tresorit.com/legal/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.tresorit.com){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.tresorit.mobile)
- [:simple-appstore: App Store](https://apps.apple.com/app/id722163232)
- [:fontawesome-brands-windows: Windows](https://tresorit.com/download)
- [:simple-apple: macOS](https://tresorit.com/download)
- [:simple-linux: Linux](https://tresorit.com/download)

</details>

</div>

Tresorit has received a number of independent security audits:

- [2022](https://tresorit.com/blog/tresorit-receives-iso-27001-certification): ISO/IEC 27001:2013[^1] Compliance [Certification](https://certipedia.com/quality_marks/9108644476) by TÜV Rheinland InterCert Kft
- [2021](https://tresorit.com/blog/fresh-penetration-testing-confirms-tresorit-security): Penetration Testing by Computest
    - Bij deze evaluatie is de beveiliging van de Tresorit webclient, Android app, Windows app en bijbehorende infrastructuur beoordeeld.
    - Computest ontdekte twee kwetsbaarheden die zijn opgelost.
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): Penetration Testing by Ernst & Young.
    - Deze evaluatie analyseerde de volledige broncode van Tresorit en bevestigde dat de implementatie overeenkomt met de concepten die zijn beschreven in Tresorit's [white paper](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf).
    - Ernst & Young additionally tested the web, mobile, and desktop clients. They concluded:

        > Test results found no deviation from Tresorit’s data confidentiality claims.

They have also received the Digital Trust Label, a certification from the [Swiss Digital Initiative](https://efd.admin.ch/en/swiss-digital-initiative-en) which requires passing [35 criteria](https://swiss-digital-initiative.org/criteria) related to security, privacy, and reliability.

## Peergos

<div class="admonition recommendation" markdown>

![Peergos logo](assets/img/cloud/peergos.svg){ align=right }

**Peergos** is a decentralized protocol and open-source platform for storage, social media, and applications. It provides a secure and private space where users can store, share, and view their photos, videos, documents, etc. Peergos secures your files with quantum-resistant end-to-end encryption and ensures all data about your files remains private.

[:octicons-home-16: Homepage](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://book.peergos.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/peergos/peergos#support){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=peergos.android)
- [:simple-github: GitHub](https://github.com/Peergos/web-ui/releases)
- [:fontawesome-brands-windows: Windows](https://github.com/Peergos/web-ui/releases)
- [:simple-apple: macOS](https://github.com/Peergos/web-ui/releases)
- [:simple-linux: Linux](https://github.com/Peergos/web-ui/releases)
- [:octicons-browser-16: Web](https://peergos.net)

</details>

</div>

Peergos is built on top of the [InterPlanetary File System (IPFS)](https://ipfs.tech), a peer-to-peer architecture that protects against [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}.

Peergos is primarily a web app, but you can self-host the server either as a local cache for your remote Peergos account, or as a standalone storage server which negates the need to register for a remote account and subscription. The Peergos server is a `.jar` file, which means the Java 17+ Runtime Environment ([OpenJDK download](https://azul.com/downloads)) should be installed on your machine to get it working.

Running a local version of Peergos alongside a registered account on their paid, hosted service allows you to access your Peergos storage without any reliance on DNS or TLS certificate authorities, and keep a copy of your data backed up to their cloud. The user experience should be the same whether you run their desktop server or just use their hosted web interface.

Peergos was [audited](https://peergos.org/posts/security-audit-2024) in November 2024 by Radically Open Security and all issues were fixed. They were previously [audited](https://cure53.de/pentest-report_peergos.pdf) by Cure53 in June 2019, and all found issues were subsequently fixed.

## Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

### Minimale vereisten

- Must enforce E2EE.
- Moet een gratis plan of proefperiode aanbieden om te testen.
- Must support TOTP or FIDO2 multifactor authentication, or passkey logins.
- Moet een webinterface bieden die basisfuncties voor bestandsbeheer ondersteunt.
- Moet gemakkelijke export van alle bestanden/documenten mogelijk maken.

### Beste geval

Onze best-case criteria geven aan wat wij zouden willen zien van het perfecte project in deze categorie. Het is mogelijk dat onze aanbevelingen geen of niet alle functies bevatten, maar degene die dat wel doen kunnen hoger gerangschikt worden dan andere op deze pagina.

- Clients should be open source.
- Clients should be audited in their entirety by an independent third party.
- Moet native clients aanbieden voor Linux, Android, Windows, macOS en iOS.
    - Deze clients moeten integreren met native OS tools voor cloud storage providers, zoals Files app integratie op iOS, of DocumentsProvider functionaliteit op Android.
- Should support easy file sharing with other users.
- Moet ten minste een basisfunctionaliteit voor het bekijken en bewerken van bestanden op de webinterface bieden.

[^1]: [De naleving van ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001):2013 heeft betrekking op het beheersysteem voor informatiebeveiliging van het bedrijf [](https://en.wikipedia.org/wiki/Information_security_management) en heeft betrekking op de verkoop, de ontwikkeling, het onderhoud en de ondersteuning van hun clouddiensten.
