---
meta_title: "Les meilleurs systèmes d'exploitation Android - Privacy Guides"
title: Distributions alternatives
description: Vous pouvez remplacer le système d'exploitation de votre téléphone Android par ces alternatives sécurisées et respectueuses de la vie privée.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Systèmes d'exploitation Android privés
    url: "./"
  - "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Protège contre la/les menaces suivantes :</small>

- [:material-target-account: Attaques ciblées](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Attaques passives](../basics/common-threats.md#security-and-privacy){ .pg-orange }

Un **système d'exploitation personnalisé basé sur Android** (parfois appelé un **ROM personnalisé**) peut être une façon d'atteindre un niveau plus élevé de confidentialité et de sécurité sur votre appareil. Cela contraste avec la version "stock" d'Android, qui est installé sur votre appareil par défaut lors de la fabrication. Cette version est souvent profondément intégrée aux services Google Play ainsi qu'à d'autres logiciels fournisseurs.

Nous recommandons d'installer GrapheneOS si vous avez un Google Pixel, puisqu'il procure des renforcements au niveau de sécurité et des fonctionnalités de confidentialité additionnelles. Les raisons pourquoi nous ne mentionnons pas d'autres systèmes d'opérations ou d'appareils sont les suivantes :

- Ils ont souvent une sécurité [plus faible](index.md#install-a-custom-distribution).
- Le support est fréquemment abandonné lorsque les mainteneurs perdent intérêt ou mettent à niveau leurs appareils, ce qui contraste avec les [cycles prédictibles de mises à jour](https://grapheneos.org/faq#device-lifetime) que GrapheneOS suit.
- Ils ont généralement peu ou pas d'améliorations notables en matière de confidentialité ou de sécurité qui justifie leur installation.

## GrapheneOS

<div class="admonition recommendation" markdown>

![GrapheneOS logo](../assets/img/android/grapheneos.svg#only-light){ align=right }
![GrapheneOS logo](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** est le meilleur choix en matière de confidentialité et de sécurité.

GrapheneOS fournit des [renforcements de sécurité](https://en.wikipedia.org/wiki/Hardening_\(computing\)) et de confidentialité supplémentaire. Il dispose d'un [allocateur de mémoire renforcé](https://github.com/GrapheneOS/hardened_malloc), de permissions de réseau et de capteurs, et de diverses autres [fonctions de sécurité](https://grapheneos.org/features). GrapheneOS est également livré avec des mises à jour complètes du micrologiciel et des versions signées, de sorte que le démarrage sécurisé est entièrement pris en charge.

[:octicons-home-16: Homepage](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title="Contribute" }

</div>

GrapheneOS prend en charge [l'isolation Google Play] (https://grapheneos.org/usage#sandboxed-google-play), qui exécute les services Google Play de façon isolée, comme n'importe quelle autre application. Cela signifie que vous pouvez profiter de la plupart des avantages des services Google Play, comme les notifications, tout en vous donnant le contrôle total à leurs permissions et leurs accès, en plus de les limiter à un [profil professionnel](../os/android-overview.md#work-profile) ou à un [profil personnel](../os/android-overview.md#user-profiles) de votre choix.

[Google Pixel phones](../mobile-phones.md#google-pixel) are the only devices that currently meet GrapheneOS's [hardware security requirements](https://grapheneos.org/faq#future-devices). The Pixel 8 and later support ARM's Memory Tagging Extension (MTE), a hardware security enhancement that drastically lowers the probability of exploits occurring through memory corruption bugs. GrapheneOS greatly expands the coverage of MTE on supported devices. Whereas the stock OS only allows you to opt in to a limited implementation of MTE via a developer option or Google's Advanced Protection Program, GrapheneOS features a more robust implementation of MTE by default in the system kernel, default system components, and their Vanadium web browser and its WebView.

GrapheneOS also provides a global toggle for enabling MTE on all user-installed apps at :gear: **Settings** → **Security & privacy** → **Exploit protection** → **Memory tagging** → **Enable by default**. The OS also features per-app toggles to opt out of MTE for apps which may crash due to compatibility issues.

### Vérifications de connectivité

Par défaut, Android effectue de nombreuses connexions réseau avec Google pour effectuer des vérifications de connectivité DNS, pour se synchroniser avec l'heure actuelle du réseau, pour vérifier votre connectivité réseau et pour de nombreuses autres tâches d'arrière-plan. GrapheneOS vient remplacer celles-ci par des connexions à des serveurs opérés par GrapheneOS qui sont soumis à leur propre politique de confidentialité. Cela cache votre information comme votre adresse IP [de Google](../basics/common-threats.md#privacy-from-service-providers), mais fais en sorte qu'il est trivial pour un administrateur de votre réseau ou pour votre fournisseur d'accès internet que vous faites des connexions à `grapheneos.network`, `grapheneos.org`, etc. et de déuire quel système d'exploitation vous utilisez.

Si vous voulez cacher ce type d'information à une personne en particulier sur votre réseau ou à votre FAI, vous **devez** utiliser un [VPN de confiance](../vpn.md) en plus de changer le paramètre de vérification de connectivité à **Standard (Google)**. Celui-ci se trouve dans :gear: **Paramètres** → **Réseau et internet** → **Vérification de la connectivité internet**. Cette option vous permet de vous connecter aux serveurs de Google pour vérifier la connectivité, ce qui, avec l'utilisation d'un VPN, vous aide à vous fondre dans un plus grand nombre d'appareils Android.

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](../about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

- Dois être un logiciel open source.
- Doit prendre en charge le verrouillage du chargeur d'amorçage avec prise en charge d'une clé AVB personnalisée.
- Doit recevoir les mises à jour majeures d'Android dans le mois suivant leur sortie.
- Doit recevoir les mises à jour des fonctionnalités d'Android (version mineure) dans les deux semaines après leur sortie.
- Doit recevoir les correctifs de sécurités réguliers dans les 5 jours suivants leur sortie.
- Ne doit **pas** être « rooté » dès sa sortie d’usine.
- **Ne** dois **pas** activer les services Google Play par défaut.
- **Ne** dois **pas** nécessiter une modification du système pour prendre en charge les services Google Play.
