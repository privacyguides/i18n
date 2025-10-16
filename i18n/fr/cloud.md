---
meta_title: "Les meilleurs services de stockage cloud privés et sécurisés - Privacy Guides"
title: Stockage cloud
icon: material/file-cloud
description: De nombreux fournisseurs de stockage cloud nécessitent que vous leur fassiez confiance pour ne pas consulter vos fichiers. Voici des alternatives privées !
cover: cloud.webp
---

<small>Protège contre la/les menaces suivantes :</small>

- [:material-bug-outline: Attaques passives](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Fournisseurs de service](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

La plupart des **fournisseurs de stockage cloud** nécessitent que vous leur fassiez entièrement confiance pour qu'ils ne regardent pas vos fichiers. Les alternatives suivantes éliminent ce besoin de confiance en proposant un chiffrement de bout en bout.

Si ces alternatives ne répondent pas à vos besoins, nous vous suggérons d'utiliser un logiciel de chiffrement tel que [Cryptomator](encryption.md#cryptomator-cloud) avec un autre fournisseur de cloud. L'utilisation de Cryptomator en complément de **tout** fournisseur de cloud (y compris ceux-ci) peut être une bonne idée pour réduire le risque de failles de chiffrement dans les clients natifs d'un fournisseur.

<details class="admonition info" markdown>
<summary>Vous cherchez Nextcloud ?</summary>

Pour nos lecteurs les plus avancés, nous [recommandons toujours](self-hosting/file-management.md#nextcloud) Nextcloud en tant que gestionnaire de fichier autohébergé, mais nous ne recommandons pas les fournisseurs de stockage proposés par Nextcloud pour le moment, car nous ne [recommandons pas](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) la fonctionnalité de chiffrement de bout-en-bout de Nextcloud pour les utilisateurs moyens.

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

La version web de Proton Drive a été auditionnée par l'organisme indépendant Securitum en [2021](https://proton.me/community/open-source), mais les nouveaux clients mobiles n'ont pas encore été publiquement auditionnés par une organisation tiers.

## Tresorit

<div class="admonition recommendation" markdown>

![Logo Tresorit](assets/img/cloud/tresorit.svg){ align=right }

**Tresorit** est un fournisseur suisse-hongrois de stockage cloud chiffré fondé en 2011. Tresorit appartient à la Poste suisse, le service postal national de la Suisse.

[:octicons-home-16: Page d'Accueil](https://tresorit.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tresorit.com/legal/privacy-policy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://support.tresorit.com){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Téléchargement</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.tresorit.mobile)
- [:simple-appstore: App Store](https://apps.apple.com/app/id722163232)
- [:fontawesome-brands-windows: Windows](https://tresorit.com/download)
- [:simple-apple: macOS](https://tresorit.com/download)
- [:simple-linux: Linux](https://tresorit.com/download)

</details>

</div>

Tresorit a fait l'objet d'un certain nombre d'audits de sécurité indépendants :

- [2022](https://tresorit.com/blog/tresorit-receives-iso-27001-certification): ISO/IEC 27001:2013[^1] Certification [de Conformité](https://certipedia.com/quality_marks/9108644476) par TÜV Rheinland InterCert Kft
- [2021](https://tresorit.com/blog/fresh-penetration-testing-confirms-tresorit-security): Test d'intrusion par Computest
    - Cet examen a permis d'évaluer la sécurité du client web de Tresorit, de l'application Android, de l'application Windows et de l'infrastructure associée.
    - Computest a découvert deux vulnérabilités qui ont été résolues.
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): Test d'intrusion par Ernst & Young.
    - Cette étude a analysé le code source complet de Tresorit et validé que la mise en œuvre correspond aux concepts décrits dans le [livre blanc](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf) de Tresorit.
    - Ernst & Young a également testé les clients web, mobiles et de bureau. Ils concluent :

        > Les résultats des tests n'ont révélé aucun écart par rapport aux déclarations de confidentialité des données de Tresorit.

Tresorit est également certifié par le Digital Trust Label, délivrée par la [Swiss Digital Initiative](https://efd.admin.ch/en/swiss-digital-initiative-en), qui exigent de satisfaire [35 critères](https://swiss-digital-initiative.org/criteria) en lien avec la sécurité, la confidentialité, et la fiabilité.

## Peergos

<div class="admonition recommendation" markdown>

![Logo de Peergos](assets/img/cloud/peergos.svg){ align=right }

**Peergos** est un protocole décentralisé et une plateforme open-source pour le stockage, les réseaux sociaux et les applications. It provides a secure and private space where users can store, share, view, and edit their photos, videos, documents, etc.

Peergos secures your files with quantum-resistant E2EE and ensures all data about your files remains private. It is also [self-hostable](https://book.peergos.org/features/self).

[:octicons-home-16: Page d'Accueil](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://book.peergos.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Code Source" }
[:octicons-heart-16:](https://github.com/peergos/peergos#support){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=peergos.android)
- [:simple-github: GitHub](https://github.com/Peergos/web-ui/releases)
- [:fontawesome-brands-windows: Windows](https://peergos.org/download#windows)
- [:simple-apple: macOS](https://peergos.org/download#macos)
- [:simple-linux: Linux](https://peergos.org/download#linux)
- [:octicons-browser-16: Web](https://peergos.net)

</details>

</div>

Peergos fonctionne avec le [système de fichier interplanétaire (InterPlanetary File System ou IPFS)](https://ipfs.tech), un protocole pair à  pair qui permet de contourner la [:material-close-outline: Censure](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}.

The client, server, and command line interface for Peergos all run from the same binary. Additionally, Peergos includes a [sync engine](https://book.peergos.org/features/sync) (accessible via the native apps) for bi-directionally synchronizing a local folder with a Peergos folder, and a [webdav bridge](https://book.peergos.org/features/webdav) to allow other applications to access your Peergos storage. You can refer to Peergos's documentation for a full overview of their numerous features.

Peergos a été [auditionné](https://peergos.org/posts/security-audit-2024) en novembre 2024 par Radically Open Security et tous les problèmes ont été corrigés. Ils ont été précédemment [auditionnés](https://cure53.de/pentest-report_peergos.pdf) par Cure53 en juin 2019, à la suite de quoi tous les problèmes trouvés ont été résolus.

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Doit mettre en œuvre un chiffrement de bout en bout (E2EE).
- Doit avoir une offre gratuite ou une période d'essai pour les tests.
- Doit prendre en charge l'authentification multifactorielle TOTP ou FIDO2, ou les clés d'accès.
- Doit offrir une interface web prennant en charge les fonctionnalités de base de gestion des fichiers.
- Doit permettre d'exporter facilement tous les fichiers/documents.

### Critères optimaux

Nos critères optimaux représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de ces fonctionnalités, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Les clients devraient être open source.
- Les clients doivent être auditionnés dans leur intégralité par un organisme indépendant.
- Devrait offrir des clients natifs pour Linux, Android, Windows, macOS et iOS.
    - Ces clients devraient s'intégrer aux outils natifs du système d'exploitation pour les fournisseurs de stockage cloud, comme l'intégration de l'application Fichiers sur iOS, ou la fonctionnalité DocumentsProvider sur Android.
- Devrait permettre de partager facilement des fichiers avec d'autres utilisateurs.
- Devrait offrir au moins une fonctionnalité de base d'aperçu et d'édition de fichiers sur l'interface web.

[^1]: La conformité à la norme [ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001):2013 concerne le [système de gestion de la sécurité de l'information](https://en.wikipedia.org/wiki/Information_security_management) de l'entreprise et couvre la vente, le développement, la maintenance et le soutien de ses services cloud.
