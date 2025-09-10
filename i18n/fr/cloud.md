---
meta_title: "Les meilleurs services de stockage cloud privés et sécurisés - Privacy Guides"
title: "Stockage cloud"
icon: material/file-cloud
description: De nombreux fournisseurs de stockage cloud nécessitent que vous leur fassiez confiance pour ne pas consulter vos fichiers. Voici des alternatives privées !
cover: cloud.webp
---

<small>Protège contre la/les menaces suivantes :</small>

- [:material-bug-outline: Attaques passives](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Fournisseurs de service](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

La plupart des **fournisseurs de stockage cloud** nécessitent que vous leur fassiez entièrement confiance pour qu'ils ne regardent pas vos fichiers. Les alternatives suivantes éliminent ce besoin de confiance en proposant un chiffrement de bout en bout.

Si ces alternatives ne répondent pas à vos besoins, nous vous suggérons d'utiliser un logiciel de chiffrement tel que [Cryptomator](encryption.md#cryptomator-cloud) avec un autre fournisseur de cloud. L'utilisation de Cryptomator en conjonction avec **tout** fournisseur de cloud (y compris ceux-ci) peut être une bonne idée pour réduire le risque de failles de chiffrement dans les clients natifs d'un fournisseur.

<details class="admonition info" markdown>
<summary>Vous cherchez Nextcloud ?</summary>

Nextcloud est [toujours un outil recommandé](document-collaboration.md#nextcloud) en tant que gestionnaire de fichiers en auto-hébergement, cependant nous ne recommandons pas les fournisseurs tiers de stockage Nextcloud pour le moment car nous ne [recommandons pas](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) la fonctionnalité chiffrement en de bout en bout porposé par Nextcloud pour les utilisateurs moyens.

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Logo de Proton Drive](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive** est un fournisseur de stockage cloud chiffré proposé par le fournisseur de service mail chiffré [Proton Mail](email.md#proton-mail).

Le stockage de base gratuit est limité à 2 GB, mais en remplissant ]certaines conditions](https://proton.me/support/more-free-storage-existing-users), cette limite peut être repoussée à 5 GB.

[:octicons-home-16: Page d'accueil](https://proton.me/drive){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/drive/privacy-policy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Téléchargement</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)
- [:fontawesome-brands-windows: Windows](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

The Proton Drive web application has been independently audited by Securitum in [2021](https://proton.me/community/open-source), but the brand new mobile clients have not yet been publicly audited by a third party.

## Tresorit

<div class="admonition recommendation" markdown>

![Logo Tresorit](assets/img/cloud/tresorit.svg){ align=right }

**Tresorit** est un fournisseur suisse-hongrois de stockage cloud chiffré fondé en 2011. Tresorit appartient à la Poste suisse, le service postal national de la Suisse.

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
    - Cet examen a permis d'évaluer la sécurité du client web de Tresorit, de l'application Android, de l'application Windows et de l'infrastructure associée.
    - Computest a découvert deux vulnérabilités qui ont été résolues.
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): Penetration Testing by Ernst & Young.
    - Cette étude a analysé le code source complet de Tresorit et validé que la mise en œuvre correspond aux concepts décrits dans le [livre blanc](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf) de Tresorit.
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

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Must enforce E2EE.
- Doit avoir une offre gratuite ou une période d'essai pour les tests.
- Must support TOTP or FIDO2 multifactor authentication, or passkey logins.
- Doit offrir une interface web prennant en charge les fonctionnalités de base de gestion des fichiers.
- Doit permettre d'exporter facilement tous les fichiers/documents.

### Dans le meilleur des cas

Nos critères de cas idéal représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de cette fonctionnalité, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Les clients devraient être open source.
- Clients should be audited in their entirety by an independent third party.
- Devrait offrir des clients natifs pour Linux, Android, Windows, macOS et iOS.
    - Ces clients devraient s'intégrer aux outils natifs du système d'exploitation pour les fournisseurs de stockage cloud, comme l'intégration de l'application Fichiers sur iOS, ou la fonctionnalité DocumentsProvider sur Android.
- Should support easy file sharing with other users.
- Devrait offrir au moins une fonctionnalité de base d'aperçu et d'édition de fichiers sur l'interface web.

[^1]: La conformité à la norme [ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001):2013 concerne le [système de gestion de la sécurité de l'information](https://en.wikipedia.org/wiki/Information_security_management) de l'entreprise et couvre la vente, le développement, la maintenance et le soutien de ses services cloud.
