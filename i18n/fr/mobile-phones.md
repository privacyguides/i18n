---
title: Smartphones
icon: material/cellphone-check
description: Les smartphones suivants possèdent la meilleure sécurité matérielle (hardware) pour les systèmes d'exploitation Android alternatifs (ou custom ROMs).
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Recommandations de smartphones
    url: "./"
  - "@context": http://schema.org
    "@type": Article
    name: Pixel
    brand:
      "@type": Marque
      name: Google
    image: /assets/img/android/google-pixel.png
    sameAs: https://en.wikipedia.org/wiki/Google_Pixel
    review:
      "@type": Avis
      author:
        "@type": Organisation
        name: Privacy Guides
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Protège contre les menaces suivantes :</small>

- [:material-target-account: Attaque ciblée](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Attaque passive](basics/common-threats.md#security-and-privacy){ .pg-orange }

La plupart des fabricants d'équipement d'origine (OEM) fournissent des mises à jour de sécurité pour leurs **smartphones** seulement sur une courte période ; une fois que ces appareils atteignent la fin de leur période de support logiciel, ils ne **peuvent plus** être considérés comme sécurisés, car ils ne reçoivent plus de mise à jour de sécurité pour leur micrologiciel ou leurs drivers (pilotes).

Les smartphones présentés ici reçoivent des mises à jour de sécurité pendant plus longtemps et vous permettent d'installer un système d'exploitation alternatif sans contrevenir au modèle de sécurité Android.

[Recommandations de systèmes d'exploitation Android :material-arrow-right-drop-circle:](android/distributions.md){ .md-button .md-button--primary } [Détails sur la sécurité d'Android :material-arrow-right-drop-circle:](os/android-overview.md#security-protections){ .md-button }

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Les appareils en fin de vie (comme les appareils à "support prolongé" de GrapheneOS) ne reçoivent pas de mise à jour complète de leur micrologiciel en raison de l'abandon de ces mises à jour par les OEM. Ces appareils ne peuvent pas être considérés comme totalement sécurisés, quel que soit le logiciel installé.

</div>

## General Purchasing Advice

Lorsque vous achetez un appareil, nous vous recommandons d'en acheter un le plus neuf possible. Puisque le logiciel et le micrologiciel d'un appareil ne sont mis à jour que pendant une courte période, acheter un appareil neuf permet de profiter de celle-ci le plus longtemps possible.

Évitez d'acheter des téléphones auprès des opérateurs de réseaux mobiles. Ces appareils ont souvent un **bootloader vérouillé** et ne permettent pas le [déverouillage OEM](https://source.android.com/devices/bootloader/locking_unlocking). Cette fonctionnalité vous empêchera totalement d'installer des versions alternatives d'Android.

Soyez particulièrement **vigilant** lorsque vous acheter un smartphone d'occasion en ligne. Vérifiez toujours la réputation du vendeur. Si l'appareil est volé, il est peut-être inscrit sur la [base de donnée IMEI](https://gsma.com/get-involved/working-groups/terminal-steering-group/imei-database). Dans certains cas, vous pouvez également vous retrouver associé aux agissements du précédent propriétaire.

Quelques conseils supplémentaires en termes de sécurité sur Android et de compatibilité des systèmes d'exploitation :

- N'achetez pas des appareils en fin de vie ; l'appareil doit pouvoir bénéficier des mises à jour du fabricant.
- N'achetez pas de smartphone préinstallé avec  LineageOS ou /e/OS ou tout autre smartphone Android qui ne propose pas le [démarrage validé (ou verified boot)](https://source.android.com/security/verifiedboot)et les mises à jour micrologiciel. Ces appareils ne vous permettent pas de vous assurer de leur fiabilité.
- En bref, si un appareil n'apparait pas sur cette liste, c'est probablement pour une bonne raison. Consultez notre [forum](https://discuss.privacyguides.net) pour plus de détails !

## Google Pixel

Les téléphones Google Pixel sont les **seuls** smartphones que nous vous recommandons d'acheter. Les smartphones Pixel possèdent la meilleure sécurité hardware de tous les téléphones Android actuellement sur le marché, en raison de la compatibilité de leur AVB (Android Verified Boot) avec les systèmes d'exploitation alternatifs et de leur puce de sécurité [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) personnalisée par Google qui sert de Composant Sécurisé (Secure Element).

<div class="admonition recommendation" markdown>

![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }

Les appareils **Google Pixel** sont connus pour avoir une bonne sécurité et pour leur meilleure compatibilité avec le [Démarrage Vérifié](https://source.android.com/security/verifiedboot), même en y installant un système d'exploitation alternatif.

À partir des **Pixel 8** et **8 Pro**, les Pixels donne la garantie de recevoir des mises à jour de sécurité pendant 7 ans, leur offrant donc une meilleure durée de vie en comparaison avec les OEM concurrents dont le support logiciel est généralement compris entre 2 et 5 ans.

[:material-shopping: Google Store](https://store.google.com/category/phones){ .md-button .md-button--primary }

</div>

### Sécurité matérielle

Secure Elements like the Titan M2 are more limited than the processor's Trusted Execution Environment (TEE) used by most other phones as they are only used for secrets storage, hardware attestation, and rate limiting, not for running "trusted" programs. Les smartphones qui ne possèdent pas de Composant Sécurisé doivent utiliser le TEE pour _toutes_ ces fonctions, laissant ainsi une surface d'attaque plus importante.

Les Pixels utilisent un système d'exploitation particulier pour le TEE appelé Trusty qui, contrairement à beaucoup d'autres téléphones, est [open source](https://source.android.com/security/trusty#whyTrusty).

The Pixel 8 series and later supports ARM's Memory Tagging Extension ([MTE](https://developer.arm.com/documentation/108035/0100/Introduction-to-the-Memory-Tagging-Extension)), a hardware security enhancement that drastically lowers the probability of exploits occurring through memory corruption bugs. The stock Pixel OS allows you to enable MTE for supported apps through Google's Advanced Protection Program or via a developer option, but its usability is quite limited. [GrapheneOS](android/distributions.md#grapheneos), un système Android alternatif que nous recommandons, améliore considérablement l’ergonomie et la couverture de MTE dans sa mise en œuvre de cette fonctionnalité.

### Buying a Google Pixel

Quelques conseils supplémentaires :

- Pour profiter d'une bonne affaire, vous pouvez essayer d'acheter un modèle "**a**" juste après la sortie d'un nouveau modèle. Google propose souvent des réductions afin de vider leurs stocks.
- Cherchez les meilleures offres ou les réductions spéciales proposées dans les magasins physiques.
- Consultez régulièrement les sites communautaires de bonnes affaires de votre région. Ils peuvent vous informer en cas de réductions intéressantes.
- Google fourni une liste complète du [cycle de support](https://support.google.com/nexus/answer/4457705) pour chacun de leurs modèles. Le coût journalier d'un appareil peut être calculé comme suit : <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline" class="tml-display" style="display:inline math;"> <mfrac> <mtext>Coût</mtext> <mrow> <mtext>Date de fin de vie</mtext> <mo>−</mo> <mtext>Date du jour</mtext> </mrow> </mfrac> </math>
  , ce qui signifie que plus vous utilisez votre appareil longtemps, moins le coût journalier sera élevé.
- Si les Pixels ne sont pas disponibles à la vente dans votre pays, les [NitroPhones](https://shop.nitrokey.com/shop) peuvent être livrés dans le monde entier.

L'installation de GrapheneOS sur un Pixel est très simple grâce à leur [web installer](https://grapheneos.org/install/web)(en anglais uniquement, mais des tutoriels en français sont facilement trouvables). Si vous n'êtes pas à l'aise à l'idée de le faire vous-même et si cela entre dans votre budget, vous pouvez investir dans un [NitroPhone](https://shop.nitrokey.com/shop) préinstallé avec GrapheneOS, vendu par l'entreprise réputée [Nitrokey](https://nitrokey.com/about).

## Critères

**Nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de nos [critères de base](about/criteria.md), nous avons élaboré un ensemble d'exigences clair nous permettant de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de faire votre choix, et de mener vos propres recherches pour vous assurer que c'est ce choix vous correspond.

- Compatible avec au moins un des systèmes d'exploitation alternatifs que nous recommandons.
- Actuellement disponible neuf à la vente dans les magasins.
- Garantit minimum 5 ans de mises à jour de sécurité.
- Le hardware contient des composants sécurisés.
