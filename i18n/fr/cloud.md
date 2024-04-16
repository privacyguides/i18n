---
meta_title: "Les meilleurs services de stockage cloud privés et sécurisés - Privacy Guides"
title: "Stockage cloud"
icon: material/file-cloud
description: De nombreux fournisseurs de stockage cloud nécessitent que vous leur fassiez confiance pour ne pas consulter vos fichiers. Voici des alternatives privées !
cover: cloud.webp
---

De nombreux fournisseurs de stockage cloud nécessitent que vous leur fassiez entièrement confiance pour ne pas consulter vos fichiers. Les alternatives énumérées ci-dessous éliminent le besoin de confiance en mettant en œuvre un E2EE sécurisé.

Si ces alternatives ne répondent pas à vos besoins, nous vous suggérons d'utiliser un logiciel de chiffrement tel que [Cryptomator](encryption.md#cryptomator-cloud) avec un autre fournisseur de cloud. L'utilisation de Cryptomator en conjonction avec **tout** fournisseur de cloud (y compris ceux-ci) peut être une bonne idée pour réduire le risque de failles de chiffrement dans les clients natifs d'un fournisseur.

<details class="TYPE" markdown>
<summary>Vous cherchez Nextcloud ?</summary>

Nextcloud est [toujours un outil recommandé](productivity.md) pour l'auto-hébergement d'une suite de gestion de fichiers, mais nous ne recommandons pas de fournisseurs de stockage Nextcloud tiers pour le moment, car nous [ne recommandons pas](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) la fonctionnalité E2EE intégrée de Nextcloud pour les utilisateurs moyens.

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Logo Proton Drive](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive** est un fournisseur suisse de stockage cloud chiffré issu du populaire fournisseur d'email chiffré [Proton Mail](email.md#proton-mail). The initial free storage is limited to 2GB, but with completion of certain steps, additional storage can be obtained up to 5GB.

[:octicons-home-16: Page d'accueil](https://proton.me/drive){ class="md-button md-button--primary" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)
- [:simple-windows11: Windows](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

L'application web Proton Drive a fait l'objet d'un audit indépendant par Securitum en [2021](https://proton.me/blog/security-audit-all-proton-apps), tous les détails n'ont pas été communiqués, mais la lettre d'attestation de Securitum indique ce qui suit :

> Les auditeurs ont relevé deux faiblesses de faible gravité. En outre, cinq recommandations générales ont été formulées. En même temps, nous confirmons qu'aucun problème de sécurité important n'a été identifié pendant le test d'intrusion.

Proton Drive's brand new mobile clients have not yet been publicly audited by a third party.

## Tresorit

<div class="admonition recommendation" markdown>

![Logo Tresorit](assets/img/cloud/tresorit.svg){ align=right }

**Tresorit** est un fournisseur suisse-hongrois de stockage cloud chiffré fondé en 2011. Tresorit appartient à la Poste suisse, le service postal national de la Suisse.

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

Tresorit a fait l'objet d'un certain nombre d'audits de sécurité indépendants :

- [2022](https://tresorit.com/blog/tresorit-receives-iso-27001-certification): ISO/IEC 27001:2013[^1] Compliance [Certification](https://certipedia.com/quality_marks/9108644476) by TÜV Rheinland InterCert Kft
- [2021](https://tresorit.com/blog/fresh-penetration-testing-confirms-tresorit-security): Penetration Testing by Computest
    - Cet examen a permis d'évaluer la sécurité du client web de Tresorit, de l'application Android, de l'application Windows et de l'infrastructure associée.
    - Computest a découvert deux vulnérabilités qui ont été résolues.
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): Penetration Testing by Ernst & Young.
    - Cette étude a analysé le code source complet de Tresorit et validé que la mise en œuvre correspond aux concepts décrits dans le [livre blanc](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf) de Tresorit.
    - Ernst & Young a également testé les clients web, mobiles et de bureau : "Les résultats des tests n'ont révélé aucun écart par rapport aux affirmations de Tresorit en matière de confidentialité des données".

They have also received the Digital Trust Label, a certification from the [Swiss Digital Initiative](https://www.efd.admin.ch/efd/en/home/digitalisierung/swiss-digital-initiative.html) which requires passing [35 criteria](https://digitaltrust-label.swiss/criteria) related to security, privacy, and reliability.

## Peergos

<div class="admonition recommendation" markdown>

![Peergos logo](assets/img/cloud/peergos.svg){ align=right }

**Peergos** is a decentralized protocol and open-source platform for storage, social media, and applications. It provides a secure and private space where users can store, share, and view their photos, videos, documents, etc. Peergos secures your files with quantum-resistant end-to-end encryption and ensures all data about your files remains private. It is built on top of [IPFS (InterPlanetary File System)](https://ipfs.tech).

[:octicons-home-16: Homepage](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://book.peergos.org){ .card-link title="Documentation" }
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

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Doit imposer le chiffrement de bout en bout.
- Doit avoir une offre gratuite ou une période d'essai pour les tests.
- Doit prendre en charge l'authentification multifactorielle TOTP ou FIDO2, ou les connexions Passkey.
- Doit offrir une interface web prennant en charge les fonctionnalités de base de gestion des fichiers.
- Doit permettre d'exporter facilement tous les fichiers/documents.
- Doit utiliser un chiffrement standard et audité.

### Dans le meilleur des cas

Nos critères de cas idéal représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de cette fonctionnalité, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Les clients devraient être open source.
- Les clients devraient être audités dans leur intégralité par un tiers indépendant.
- Devrait offrir des clients natifs pour Linux, Android, Windows, macOS et iOS.
    - Ces clients devraient s'intégrer aux outils natifs du système d'exploitation pour les fournisseurs de stockage cloud, comme l'intégration de l'application Fichiers sur iOS, ou la fonctionnalité DocumentsProvider sur Android.
- Devrait permettre de partager facilement des fichiers avec d'autres utilisateurs.
- Devrait offrir au moins une fonctionnalité de base d'aperçu et d'édition de fichiers sur l'interface web.

[^1]: La conformité à la norme [ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001):2013 concerne le [système de gestion de la sécurité de l'information](https://en.wikipedia.org/wiki/Information_security_management) de l'entreprise et couvre la vente, le développement, la maintenance et le soutien de ses services cloud.
