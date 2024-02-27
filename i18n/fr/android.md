---
meta_title: "Recommandations Android : GrapheneOS et DivestOS - Privacy Guides"
title: "Android"
icon: 'simple/android'
description: Vous pouvez remplacer le système d'exploitation de votre téléphone Android par ces alternatives sécurisées et respectueuses de la vie privée.
cover: android.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Systèmes d'exploitation Android privés
    url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: Android
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://en.wikipedia.org/wiki/Android_(operating_system)
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: Divest
    image: /assets/img/android/divestos.svg
    url: https://divestos.org/
    sameAs: https://en.wikipedia.org/wiki/DivestOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": Product
    name: Pixel
    brand:
      "@type": Brand
      name: Google
    image: /assets/img/android/google-pixel.png
    sameAs: https://en.wikipedia.org/wiki/Google_Pixel
    review:
      "@type": Review
      author:
        "@type": Organization
        name: Privacy Guides
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Shelter
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Auditor
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Secure Camera
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Secure PDF Viewer
    applicationCategory: Utilities
    operatingSystem: Android
---

![Logo d'Android](assets/img/android/android.svg){ align=right }

**Android Open Source Project** est un système d'exploitation mobile open source dirigé par Google qui équipe la majorité des appareils mobiles dans le monde. La plupart des téléphones vendus avec Android sont modifiés pour inclure des intégrations et des applications invasives telles que Google Play Services. Vous pouvez donc améliorer considérablement votre vie privée sur votre appareil mobile en remplaçant l'installation par défaut de votre téléphone par une version d'Android dépourvue de ces fonctionnalités invasives.

[:octicons-home-16:](https://source.android.com/){ .card-link title=Page d'accueil }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/){ .card-link title="Code source" }

Voici les systèmes d'exploitation, les appareils et les applications Android que nous recommandons pour optimiser la sécurité et la confidentialité de votre appareil mobile. Pour en savoir plus sur Android :

[Présentation générale d'Android :material-arrow-right-drop-circle:](os/android-overview.md ""){.md-button}

## Dérivés de AOSP

Nous vous recommandons d'installer l'un de ces systèmes d'exploitation Android personnalisés sur votre appareil, classés par ordre de préférence, en fonction de la compatibilité de votre appareil avec ces systèmes d'exploitation.

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Les appareils en fin de vie (tels que les appareils à "support étendu" de GrapheneOS ou de CalyxOS) ne disposent pas de correctifs de sécurité complets (mises à jour de micrologiciel) en raison de l'arrêt du support par le constructeur. Ces appareils ne peuvent pas être considérés comme totalement sûrs, quel que soit le logiciel installé.

</div>

### GrapheneOS

<div class="admonition recommendation" markdown>

![Logo GrapheneOS](assets/img/android/grapheneos.svg#only-light){ align=right }
![Logo GrapheneOS](assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** est le meilleur choix en matière de confidentialité et de sécurité.

GrapheneOS apporte des améliorations supplémentaires en matière de [renforcement de la sécurité](https://fr.wikipedia.org/wiki/Durcissement_%28informatique%29) et de confidentialité. Il dispose d'un [allocateur de mémoire renforcé](https://github.com/GrapheneOS/hardened_malloc), d'autorisations pour le réseau et les capteurs, et de diverses autres [fonctions de sécurité](https://grapheneos.org/features). GrapheneOS est également livré avec des mises à jour complètes du micrologiciel et des versions signées, de sorte que le démarrage vérifié est entièrement pris en charge.

[:octicons-home-16: Page d'accueil ](https://grapheneos.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Code source" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuer }

</div>

GrapheneOS prend en charge [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), qui exécute les [Services Google Play](https://fr.wikipedia.org/wiki/Services_Google_Play) entièrement sandboxed comme toute autre application normale. Cela signifie que vous pouvez profiter de la plupart des services Google Play, tels que [les notifications push](https://firebase.google.com/docs/cloud-messaging/), tout en vous donnant un contrôle total sur leurs autorisations et leur accès, et tout en les contenant à un [profil de travail](os/android-overview.md#work-profile) ou un [profil d'utilisateur](os/android-overview.md#user-profiles) spécifique de votre choix.

Les téléphones Google Pixel sont les seuls appareils qui répondent actuellement aux [exigences de sécurité matérielle](https://grapheneos.org/faq#device-support) de GrapheneOS.

[Pourquoi nous recommandons GrapheneOS plutôt que CalyxOS :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/ ""){.md-button}

### DivestOS

<div class="admonition recommendation" markdown>

![Logo DivestOS](assets/img/android/divestos.svg){ align=right }

**DivestOS** est un léger dérivé de [LineageOS](https://lineageos.org/).
DivestOS hérite de nombreux [appareils pris en charge](https://divestos.org/index.php?page=devices&base=LineageOS) de LineageOS. Il a des versions signées, ce qui permet d'avoir un [démarrage vérifié](https://source.android.com/security/verifiedboot) sur certains appareils autres que des Pixel.

[:octicons-home-16: Page d'accueil](https://divestos.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Service onion" }
[:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="Code source" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Contribuer }

</div>

DivestOS a une [correction](https://gitlab.com/divested-mobile/cve_checker) automatique des vulnérabilités de noyau ([CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)), moins de blobs propriétaires, et un fichier [hosts](https://divested.dev/index.php?page=dnsbl) personnalisé. Sa WebView renforcée, [Mulch](https://gitlab.com/divested-mobile/mulch), permet [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) pour toutes les architectures et [un partitionnement de l'état du réseau](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning), et reçoit des mises à jour hors bande. DivestOS inclut également les correctifs de noyau de GrapheneOS et active toutes les fonctions de sécurité de noyau disponibles via le [renforcement defconfig](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). Tous les noyaux plus récents que la version 3.4 incluent une [désinfection](https://lwn.net/Articles/334747/) complète de la page et tous les ~22 noyaux compilés par Clang ont [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) activé.

DivestOS met en œuvre certains correctifs de renforcement du système développés à l'origine pour GrapheneOS. DivestOS 16.0 et plus implémente les autorisations [`INTERNET`](https://developer.android.com/training/basics/network-ops/connecting) et SENSORS de GrapheneOS, l'[allocateur de mémoire renforcé](https://github.com/GrapheneOS/hardened_malloc), l'[exec-spawning](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/#additional-hardening), la [constification](https://en.wikipedia.org/wiki/Java_Native_Interface) [JNI](https://en.wikipedia.org/wiki/Const_(computer_programming)), et des patchs de renforcement [bioniques](https://en.wikipedia.org/wiki/Bionic_(software)) partiels. Les versions 17.1 et supérieures offrent l'option de GrapheneOS pour [randomiser les adresses MAC](https://en.wikipedia.org/wiki/MAC_address#Randomization) entre réseaux, le contrôle [`ptrace_scope`](https://www.kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) et les options de redémarrage/coupure Wi-Fi/coupure Bluetooth automatique [sur délai](https://grapheneos.org/features).

DivestOS utilise F-Droid comme magasin d'applications par défaut. Nous [recommandons normalement d'éviter F-Droid](#f-droid), mais ce n'est pas possible sur DivestOS ; les développeurs mettent à jour leurs applications via leurs propres dépôts F-Droid ([DivestOS Official](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) et [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2)). Nous recommandons de désactiver l'application officielle F-Droid et d'utiliser [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic/) **avec les dépôts DivestOS activés** pour maintenir ces composants à jour. Pour les autres applications, nos méthodes recommandées pour les obtenir restent applicables.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

L'[état](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) des mises à jour du micrologiciel DivestOS et le contrôle de la qualité varient selon les appareils qu'il prend en charge. Nous recommandons toujours GrapheneOS en fonction de la compatibilité de votre appareil. Pour les autres appareils, DivestOS est une bonne alternative.

Tous les appareils pris en charge ne disposent pas d'un démarrage vérifié, et certains le font mieux que d'autres.

</div>

## Appareils Android

Lorsque vous achetez un appareil, nous vous recommandons d'en prendre un aussi neuf que possible. Les logiciels et les micrologiciels des appareils mobiles ne sont pris en charge que pour une durée limitée. L'achat de nouveaux appareils permet donc de prolonger cette durée de vie autant que possible.

Évitez d'acheter des téléphones auprès des opérateurs de réseaux mobiles. Ces derniers ont souvent un **chargeur d'amorçage verrouillé** et ne supportent pas le [déverrouillage constructeur](https://source.android.com/devices/bootloader/locking_unlocking). Ces variantes de téléphone vous empêcheront d'installer tout type de distribution Android alternative.

Soyez très **prudent** lorsque vous achetez des téléphones d'occasion sur des marchés en ligne. Vérifiez toujours la réputation du vendeur. Si l'appareil est volé, il est possible qu'il soit enregistré dans la [base de données IMEI](https://www.gsma.com/get-involved/working-groups/terminal-steering-group/imei-database). Il y a également un risque d'être associé à l'activité de l'ancien propriétaire.

Quelques conseils supplémentaires concernant les appareils Android et la compatibilité des systèmes d'exploitation :

- N'achetez pas d'appareils qui ont atteint ou sont sur le point d'atteindre leur fin de vie, des mises à jour supplémentaires du micrologiciel doivent être fournies par le fabricant.
- N'achetez pas de téléphones LineageOS ou /e/ OS préchargés ou tout autre téléphone Android sans prise en charge adéquate du [Démarrage Vérifié](https://source.android.com/security/verifiedboot) et sans mises à jour du micrologiciel. En outre, ces appareils ne vous permettent pas de vérifier s'ils ont été manipulés.
- En bref, si un appareil ou une distribution Android ne figure pas dans cette liste, il y a probablement une bonne raison. Consultez notre [forum](https://discuss.privacyguides.net/) pour en savoir plus !

### Google Pixel

Les téléphones Google Pixel sont les **seuls** appareils dont nous recommandons l'achat. Les téléphones Pixel ont une sécurité matérielle plus forte que tous les autres appareils Android actuellement sur le marché, grâce à une prise en charge AVB adéquate pour les systèmes d'exploitation tiers et aux puces de sécurité personnalisées [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) de Google faisant office d'Elément Sécurisé.

<div class="admonition recommendation" markdown>

![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }

Les appareils **Google Pixel** sont connus pour avoir une bonne sécurité et prendre correctement en charge le [Démarrage Vérifié](https://source.android.com/security/verifiedboot), même lors de l'installation de systèmes d'exploitation personnalisés.

À partir des **Pixel 8** et **8 Pro**, les appareils Pixel bénéficient d'un minimum de 7 ans de mises à jour de sécurité garanties, ce qui leur assure une durée de vie bien plus longue que les 2 à 5 ans généralement proposés par les constructeurs concurrents.

[:material-shopping: Boutique](https://store.google.com/category/phones){ .md-button .md-button--primary }

</div>

Les Eléments Sécurisés comme le Titan M2 sont plus limités que le Trusted Execution Environment du processeur utilisé par la plupart des autres téléphones, car ils ne sont utilisés que pour le stockage des secrets, l'attestation matérielle et la limitation du débit, et non pour exécuter des programmes "de confiance". Les téléphones dépourvus d'un Elément Sécurisé doivent utiliser le TEE pour *toutes* ces fonctions, ce qui élargit la surface d'attaque.

Les téléphones Google Pixel utilisent un OS TEE appelé Trusty qui est [open source](https://source.android.com/security/trusty#whyTrusty), contrairement à de nombreux autres téléphones.

L'installation de GrapheneOS sur un téléphone Pixel est facile avec leur [installateur web](https://grapheneos.org/install/web). Si vous ne vous sentez pas à l'aise pour le faire vous-même et que vous êtes prêt à dépenser un peu plus d'argent, consultez le site [NitroPhone](https://shop.nitrokey.com/shop) car ils sont préchargés avec GrapheneOS et viennent de la société réputée [Nitrokey](https://www.nitrokey.com/about).

Quelques conseils supplémentaires pour l'achat d'un Google Pixel :

- Si vous cherchez une bonne affaire pour un appareil Pixel, nous vous suggérons d'acheter un modèle "**a**", juste après la sortie du prochain produit phare de la marque. Des remises sont généralement disponibles parce que Google essaie d'écouler son stock.
- Tenez compte des offres spéciales et réductions proposées par les magasins en dur.
- Consultez les sites communautaires de bonnes affaires en ligne dans votre pays. Ils peuvent vous alerter lors de bonnes ventes.
- Google fournit une liste indiquant le [cycle de support](https://support.google.com/nexus/answer/4457705) pour chacun de ses appareils. Le prix par jour d'un appareil peut être calculé comme suit : $\text{Coût} \over \text {Date fin de vie}-\text{Date du jour}$, ce qui signifie que plus l'utilisation de l'appareil est longue, plus le coût par jour est faible.
- Si le pixel n'est pas disponible dans votre région, le [NitroPhone](https://shop.nitrokey.com/shop) peut être expédié dans le monde entier.

## Applications générales

Nous recommandons une grande variété d'applications Android sur ce site. Les applications répertoriées ici sont exclusives à Android et améliorent ou remplacent les principales fonctionnalités du système.

### Shelter

<div class="admonition recommendation" markdown>

![Logo Shelter](assets/img/android/shelter.svg){ align=right }

**Shelter** est une application qui vous aide à tirer parti de la fonctionnalité Profil professionnel d'Android pour isoler ou dupliquer des applications sur votre appareil.

Shelter prend en charge le blocage de la recherche de contacts entre profils et le partage de fichiers entre profils via le gestionnaire de fichiers par défaut ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).

[:octicons-repo-16: Dépôt](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Code source" }
[:octicons-heart-16:](https://www.patreon.com/PeterCxy){ .card-link title=Contribuer }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Shelter est recommandé par rapport à [Insular](https://secure-system.gitlab.io/Insular/) et [Island](https://github.com/oasisfeng/island) car il prend en charge le [blocage de la recherche de contact](https://secure-system.gitlab.io/Insular/faq.html).

En utilisant Shelter, vous accordez une confiance totale à son développeur, car Shelter agit en tant qu'[administrateur de l'appareil](https://developer.android.com/guide/topics/admin/device-admin) pour créer le Profil professionnel, et il a un accès étendu aux données stockées dans ce dernier.

</div>

### Secure Camera

<div class="admonition recommendation" markdown>

![Logo de Secure Camera](assets/img/android/secure_camera.svg#only-light){ align=right }
![Logo de Secure Camera](assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

**Secure Camera** est une application de caméra axée sur la confidentialité et la sécurité qui peut capturer des images, des vidéos et des QR codes. Les extensions du vendeur CameraX (Portrait, HDR, Night Sight, Face Retouch et Auto) sont également prises en charge sur les appareils disponibles.

[:octicons-repo-16: Dépôt](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Code source" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: Magasin d'applications de GrapheneOS](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

Les principales caractéristiques de confidentialité comprennent :

- Suppression automatique des métadonnées [Exif](https://en.wikipedia.org/wiki/Exif) (activée par défaut)
- Utilisation de la nouvelle API [Media](https://developer.android.com/training/data-storage/shared/media), donc les [autorisations de stockage](https://developer.android.com/training/data-storage) ne sont pas nécessaires
- L'autorisation microphone n'est pas nécessaire, sauf si vous souhaitez enregistrer des sons

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Les métadonnées ne sont pour le moment pas supprimées des fichiers vidéo, mais cela est prévu.

Les métadonnées d'orientation de l'image ne sont pas supprimées. Si vous activez la fonction de localisation (dans Secure Camera), elle ne **sera pas** non plus supprimée. Si vous voulez la supprimer ultérieurement, vous devrez utiliser une application externe telle que [ExifEraser](data-redaction.md#exiferaser).

</div>

### Secure PDF Viewer

<div class="admonition recommendation" markdown>

![Logo de Secure PDF Viewer](assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Logo de Secure PDF Viewer](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

**Secure PDF Viewer** est un visualiseur de PDF basé sur [pdf.js](https://en.wikipedia.org/wiki/PDF.js) qui ne nécessite aucune autorisation. Le PDF est introduit dans une [webview](https://developer.android.com/guide/webapps/webview) [sandboxed](https://en.wikipedia.org/wiki/Sandbox_(software_development)). Cela signifie qu'il n'a pas besoin d'autorisation directe pour accéder au contenu ou aux fichiers.

[Content-Security-Policy](https://fr.wikipedia.org/wiki/Content_Security_Policy) est utilisé pour faire en sorte que les propriétés JavaScript et de style dans la WebView soient entièrement statiques.

[:octicons-repo-16: Dépôt](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Code source" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## Obtenir des applications

### Obtainium

<div class="admonition recommendation" markdown>

![logo Obtainium](assets/img/android/obtainium.svg){ align=right }

**Obtainium** est un gestionnaire d'applications qui vous permet d'installer et de mettre à jour des applications directement à partir de la page de publication du développeur (i.e. GitHub, GitLab, le site web du développeur, etc.), plutôt qu'un magasin d'applications/dépôt centralisé. Il prend en charge les mises à jour automatiques en arrière-plan sur Android 12 et les versions ultérieures.

[:octicons-repo-16: Dépôt](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="Code source" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

Obtainium vous permet de télécharger des fichiers d'installation APK à partir d'une grande variété de sources, et c'est à vous de vous assurer que ces sources et ces applications sont légitimes. Par exemple, l'utilisation d'Obtainium pour installer Signal à partir de [la page de téléchargement APK de Signal](https://signal.org/android/apk/) devrait être correcte, mais l'installation à partir de dépôts APK tiers comme Aptoide ou APKPure peut présenter des risques supplémentaires. Le risque d'installer une *mise à jour* malveillante est plus faible, car Android vérifie lui-même que toutes les mises à jour d'applications sont signées par le même développeur que l'application existante sur votre téléphone avant de les installer.

### Magasin d'applications de GrapheneOS

Le magasin d'applications de GrapheneOS est disponible sur [GitHub](https://github.com/GrapheneOS/Apps/releases). Il prend en charge Android 12 et plus et est capable de se mettre à jour. Le magasin d'applications contient des applications indépendantes construites par le projet GrapheneOS, telles que [Auditor](https://attestation.app/), [Camera](https://github.com/GrapheneOS/Camera), et [PDF Viewer](https://github.com/GrapheneOS/PdfViewer). Si vous recherchez ces applications, nous vous recommandons vivement de les obtenir à partir du magasin d'applications de GrapheneOS plutôt que du Play Store, car les applications de leur magasin sont signées par la signature du projet GrapheneOS à laquelle Google n'a pas accès.

### Aurora Store

Le Google Play Store nécessite un compte Google pour se connecter, ce qui n'est pas idéal pour la confidentialité. Vous pouvez contourner ce problème en utilisant un client alternatif, tel que Aurora Store.

<div class="admonition recommendation" markdown>

![Logo Aurora Store](assets/img/android/aurora-store.webp){ align=right }

**Aurora Store** est un client Google Play Store qui ne nécessite pas de compte Google, de services Google Play ou microG pour télécharger des applications.

[:octicons-home-16: Page d'accueil](https://auroraoss.com/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="Politique de confidentialité" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

Aurora Store ne vous permet pas de télécharger des applications payantes grâce à sa fonction de compte anonyme. Vous pouvez éventuellement vous connecter avec votre compte Google sur Aurora Store pour télécharger les applications que vous avez achetées, ce qui donne accès à la liste des applications que vous avez installées à Google, mais vous bénéficiez toujours de l'avantage de ne pas avoir besoin du client Google Play complet et des services Google Play ou microG sur votre appareil.

### Manuellement avec les notifications RSS

Pour les applications publiées sur des plateformes telles que GitHub et GitLab, vous pouvez ajouter un flux RSS à votre [agrégateur d'actualités](news-aggregators.md) qui vous aidera à suivre les nouvelles versions.

![APK RSS](./assets/img/android/rss-apk-light.png#only-light) ![APK RSS](./assets/img/android/rss-apk-dark.png#only-dark) ![Notes de version APK](./assets/img/android/rss-changes-light.png#only-light) ![Notes de version APK](./assets/img/android/rss-changes-dark.png#only-dark)

#### GitHub

Sur GitHub, en prenant l'exemple de [Secure Camera](#secure-camera), vous naviguez vers sa [page de publications](https://github.com/GrapheneOS/Camera/releases) et ajoutez `.atom` à l'URL :

`https://github.com/GrapheneOS/Camera/releases.atom`

#### GitLab

Sur GitLab, en prenant l'exemple de [Aurora Store](#aurora-store), vous naviguez vers son [dépôt de projet](https://gitlab.com/AuroraOSS/AuroraStore) et ajoutez `/-/tags?format=atom` à l'URL :

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

#### Vérifier les empreintes numériques des APK

Si vous téléchargez des fichiers APK à installer manuellement, vous pouvez vérifier leur signature à l'aide de l'outil [`apksigner`](https://developer.android.com/studio/command-line/apksigner), qui fait partie des [build-tools](https://developer.android.com/studio/releases/build-tools) d'Android.

1. Installez [Java JDK](https://www.oracle.com/java/technologies/downloads/).

2. Téléchargez les [outils de ligne de commande d'Android Studio](https://developer.android.com/studio#command-tools).

3. Extrayez l'archive téléchargée :

    ```bash
    unzip commandlinetools-*.zip
    cd cmdline-tools
    ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
    ```

4. Exécutez la commande de vérification de la signature :

    ```bash
    ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
    ```

5. Les hachés obtenus peuvent ensuite être comparés avec une autre source. Certains développeurs, comme Signal, [fournissent les empreintes numériques](https://signal.org/android/apk/) sur leur site web.

    ```bash
    Signer #1 certificate DN: CN=GrapheneOS
    Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
    Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
    Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
    ```

### F-Droid

![Logo F-Droid](assets/img/android/f-droid.svg){ align=right width=120px }

==Nous recommandons F-Droid uniquement comme moyen d'obtenir des applications qui ne peuvent pas être obtenues par les moyens ci-dessus.== F-Droid est souvent recommandé comme alternative à Google Play, en particulier dans la communauté de la vie privée. La possibilité d'ajouter des dépôts tiers et de ne pas être confiné au jardin clos de Google a conduit à sa popularité. F-Droid dispose en outre de [versions reproductibles](https://f-droid.org/en/docs/Reproducible_Builds/) pour certaines applications et est dédié aux logiciels libres et open source. Cependant, la façon dont F-Droid construit, signe et livre les paquets présente quelques inconvénients liés à la sécurité :

En raison de leur processus de construction d'applications, les applications du dépôt officiel de F-Droid sont souvent en retard sur les mises à jour. Les mainteneurs de F-Droid réutilisent également les identifiants des paquets tout en signant les applications avec leurs propres clés, ce qui n'est pas idéal car cela donne à l'équipe F-Droid une confiance ultime. En outre, les conditions requises pour qu'une application soit incluse dans le répertoire officiel de F-Droid sont moins strictes que dans d'autres magasins d'applications comme Google Play, ce qui signifie que F-Droid a tendance à héberger beaucoup plus d'applications qui sont plus anciennes, non mises à jour, ou qui ne répondent plus aux [normes de sécurité modernes](https://developer.android.com/google/play/requirements/target-sdk).

D'autres dépôts tiers populaires pour F-Droid, tels que [IzzyOnDroid](https://apt.izzysoft.de/fdroid/) atténuent certains de ces problèmes. Le dépôt IzzyOnDroid récupère les versions directement depuis GitHub et constitue la meilleure alternative aux dépôts des développeurs. Cependant, ce n'est pas quelque chose que nous pouvons entièrement recommander, car les applications sont généralement [retirées](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446) de ce dépôt si elles sont ajoutées plus tard au dépôt principal de F-Droid. Bien que cela soit logique (puisque le but de ce dépôt particulier est d'héberger des applications avant qu'elles ne soient acceptées dans le dépôt principal de F-Droid), cela peut vous laisser avec des applications installées qui ne reçoivent plus de mises à jour.

Cela dit, les dépôts [F-Droid](https://f-droid.org/en/packages/) et [IzzyOnDroid](https://apt.izzysoft.de/fdroid/) abritent d'innombrables applications. Ils peuvent donc être un outil utile pour rechercher et découvrir des applications open-source que vous pouvez ensuite télécharger par d'autres moyens tels que le Play Store, Aurora Store ou en obtenant l'APK directement auprès du développeur. Vous devez faire preuve de discernement lorsque vous recherchez de nouvelles applications par cette méthode, et surveiller la fréquence des mises à jour de l'application. Des applications obsolètes peuvent s'appuyer sur des bibliothèques non maintenues, entre autres, ce qui constitue un risque potentiel pour la sécurité.

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

Dans certains cas rares, le développeur d'une application ne la distribue que par le biais de F-Droid ([Gadgetbridge](https://gadgetbridge.org/) en est un exemple). Si vous avez vraiment besoin d'une telle application, nous vous recommandons d'utiliser le nouveau client [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic/) au lieu de l'application F-Droid originale pour l'obtenir. F-Droid Basic peut effectuer des mises à jour en arrière-plan, sans extension privilégiée ou root, et possède un ensemble de fonctionnalités réduit (limitant la surface d'attaque).

</div>

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

<div class="admonition example" markdown>
<p class="admonition-title">Cette section est nouvelle</p>

Nous travaillons à l'établissement de critères définis pour chaque section de notre site, et celles-ci peuvent être sujet à changement. Si vous avez des questions sur nos critères, veuillez [poser la question sur notre forum](https://discuss.privacyguides.net/latest) et ne supposez pas que nous n'avons pas pris en compte un élément dans nos recommandations s'il ne figure pas dans la liste. De nombreux facteurs sont pris en compte et discutés lorsque nous recommandons un projet, et la documentation de chacun d'entre eux est en cours.

</div>

### Systèmes d'exploitation

- Doit être un logiciel open source.
- Doit prendre en charge le verrouillage du chargeur d'amorçage avec prise en charge d'une clé AVB personnalisée.
- Doit recevoir les mises à jour majeures d'Android dans le mois suivant leur publication.
- Doit recevoir les mises à jour des fonctionnalités d'Android (version mineure) dans les 14 jours suivant leur publication.
- Doit recevoir les correctifs de sécurité réguliers dans les 5 jours suivant leur publication.
- Ne doit **pas** être fourni "rooté".
- Ne doit **pas** activer les services Google Play par défaut.
- Ne doit **pas** nécessiter une modification du système pour prendre en charge les services Google Play.

### Appareils

- Doit prendre en charge au moins l'un des systèmes d'exploitation personnalisés que nous recommandons.
- Doit être actuellement vendu neuf en magasin.
- Doit recevoir un minimum de 5 ans de mises à jour de sécurité.
- Doit disposer d'un matériel dédié aux éléments sécurisés.

### Applications

- Les applications de cette page ne doivent pas être applicables à une autre catégorie de logiciels sur le site.
- Les applications générales doivent étendre ou remplacer les fonctionnalités de base du système.
- Les applications doivent être régulièrement mises à jour et maintenues.
