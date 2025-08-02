---
meta_title: "Navigateurs Internet pour Android et iOS qui respectent votre vie privée - Privacy Guides"
title: Navigateurs mobiles
icon: material/cellphone-information
description: Ces navigateurs sont ceux que nous recommandons actuellement pour la navigation internet standard/non anonyme sur votre téléphone.
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Recommandations de navigateurs mobiles privés
    url: "./"
    relatedLink: "../desktop-browsers/"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    applicationCategory: Web Browser
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Cromite
    image: /assets/img/browsers/cromite.svg
    url: https://cromite.org
    applicationCategory: Web Browser
    operatingSystem:
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://apple.com/safari
    applicationCategory: Navigateur Internet
    operatingSystem:
      - iOS
    subjectOf:
      "@type": Page Web
      url: "./"
---

<small>Protège contre les menaces suivantes :</small>

- [:material-account-cash: Capitalisme de surveillance](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Voici nos recommandations actuelles concernant les **navigateurs internet mobiles** et paramètres pour la navigation internet standard et non-anonyme. Si vous avez besoin de naviguer anonymement sur Internet, vous devriez plutôt utiliser [Tor](tor.md).

## Brave

<div class="admonition recommendation" markdown>

![Logo Brave](assets/img/browsers/brave.svg){ align=right }

Le navigateur **Brave** comprend un bloqueur de contenu intégré et des [fonctions de confidentialité](https://brave.com/privacy-features/), dont la plupart sont activées par défaut.

Brave est basé sur le projet de navigateur Web Chromium. Il devrait donc vous être familier et présenter un minimum de problèmes de compatibilité avec les sites Web.

[:octicons-home-16: Page d'accueil](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Service Onion" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-fdroid: F-Droid](https://brave-browser-apk-release.s3.brave.com/fdroid/repo/index.html)

</details>

</div>

### Configuration recommandée pour Brave

Le navigateur Tor est le seul moyen de vraiment naviguer anonymement sur Internet. Lorsque vous utilisez Brave, nous vous recommandons de modifier les paramètres suivants afin de protéger votre vie privée de certains tiers, mais tous les navigateurs autres que le [Navigateur Tor](tor.md#tor-browser) seront traçables par *quelqu'un* d'une manière ou d'une autre.

=== "Android"

    Ces options se trouvent dans :material-menu: → **Paramètres** → **Boucliers Brave et confidentialité**.

=== "iOS"

    Ces paramètres se trouvent dans :fontawesome-solid-ellipsis: → **Paramètres** → **Boucliers & Confidentialité**.

#### Paramètres par défaut des boucliers Brave

Brave inclut des mesures anti-empreintes digitales dans sa fonctionnalité [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Nous vous conseillons de configurer ces options de [manière globale](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) sur toutes les pages que vous visitez.

Les options "Boucliers" peuvent être réduites par site selon les besoins, mais par défaut, nous recommandons de définir les paramètres suivants:

=== "Android"

    <div class="annotate" markdown>

    - [x] Cochez **Agressif** sous *Bloquer les traqueurs et la publicité*
    - [x] Cochez **Auto-redirection des pages AMP**
    - [x] Cochez **Auto-redirection des URLs de pistage**
    - [x] Cochez **Exiger que toutes les connexions utilisent HTTPS (strict)** sous *Mettre à niveau les connexions vers HTTPS*.
    - \[x\] (Facultatif) Cochez **Bloquer les scripts** (1)
    - [x] Cochez **Bloquer les cookies tiers** sous *Bloquer les cookies*
    - [x] Cochez **Bloquer la prise d'empreinte digitale**
    - [x] Sélectionnez **Empêcher la prise d'empreintes digitales via les paramètres de langue**

    <details class="warning" markdown>
    <summary>Utilisez les listes de filtrage par défaut</summary>

    Brave vous permet de sélectionner des filtres de contenus supplémentaires dans le menu **Filtrage de contenu** ou la page interne `brave://adblock`. Nous vous déconseillons d'utiliser cette fonctionnalité ; conservez plutôt les listes de filtres par défaut. L'utilisation de listes supplémentaires vous distinguera des autres utilisateurs de Brave et peut également augmenter la surface d'attaque s'il y a une faille dans Brave et qu'une règle malveillante est ajoutée à l'une des listes que vous utilisez.

    </details>

    - [x] Cochez **Oubliez moi lorsque je ferme ce site**

    </div>

    1. Cette option désactive JavaScript, ce qui rendra inutilisable beaucoup de sites. Pour les débloquer, vous pouvez définir des exceptions par site en appuyant sur l'icône Bouclier dans la barre d'adresse et en décochant ce paramètre sous *Contrôles Avancés*.

=== "iOS"

    <div class="annotate" markdown>

    - [x] Cochez **Agressif** sous *Traqueurs & Blocage des publicités*
    - [x] Cochez **Strict** sous *Mise à niveau des connexions vers HTTPS*
    - [x] Cochez **Auto-redirection des pages AMP**
    - [x] Cochez **Auto-redirection des URLs de pistage**
    - \[x\] (Facultatif) Cochez **Bloquer les scripts** (1)
    - [x] Cochez **Bloquer la prise d'empreinte digitale**
    - [x] Select **Site Tabs Closed** under *Auto Shred*

    <details class="warning" markdown>
    <summary>Utiliser les listes de filtres par défaut</summary>

    Brave vous permet de sélectionner des filtres de contenu supplémentaires dans le menu **Filtrage du contenu.**. Nous vous déconseillons d'utiliser cette fonctionnalité ; conservez plutôt les listes de filtres par défaut. L'utilisation de listes supplémentaires vous distinguera des autres utilisateurs de Brave et peut également augmenter la surface d'attaque s'il y a une faille dans Brave et qu'une règle malveillante est ajoutée à l'une des listes que vous utilisez.

    </details>

    </div>

    1. Cette option désactive JavaScript, ce qui rendra inutilisable beaucoup de sites. Pour les débloquer, vous pouvez définir des exceptions par site en appuyant sur l'icône Bouclier dans la barre d'adresse et en décochant ce paramètre sous *Contrôles Avancés*.

##### Effacer les données de navigation (Android uniquement)

- [x] Sélectionner **Effacer les données en quittant**

##### Blocage des médias sociaux (Android uniquement)

- [ ] Décochez toutes les fonctionnalités de médias sociaux

#### Autres paramètres de confidentialité

=== "Android"

    <div class="annotate" markdown>

    - [x] Select **Disable non-proxied UDP** under [*WebRTC IP handling policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
    - \[x\] (Facultatif) Cochez **Aucune protection** sous *Navigation sécurisée* (1)
    - [] Décochez **Autoriser les sites à vérifier si vous avez enregistré des méthodes de paiement**
    - [ ] Uncheck **Javascript optimization & security** under the setting with the same name
    - [x] Cochez **Fermer les onglets en quittant**
    - [ ] Décochez **Autoriser l'analyse de produits respectueuse de la vie privée (P3A)**
    - [Décocher l'**option Envoyer automatiquement les rapports de diagnostic**
    - [ ] Décochez **Envoyer automatiquement un signal d'utilisation quotidienne à Brave**

    </div>

    1. [L'implémentation de Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) sur Brave pour Android **n'effectue pas** de proxy des [requêtes réseau de Safe Browsing](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) comme son homologue pour ordinateur de bureau. Cela signifie que votre adresse IP peut être vue (et enregistrée) par Google. Notez que Safe Browsing n'est pas disponible pour les appareils Android sans les services Google Play.

=== "iOS"

    - [ ] Décochez **Autoriser l'analyse de produits respectueuse de la vie privée (P3A)**
    - [ ] Décochez **Envoyer automatiquement un signal d'utilisation quotidienne à Brave**

#### Leo

Ces options se trouvent dans :material-menu: → **Paramètres** → **Leo**.

<div class="annotate" markdown>

- Décocher **Affichez les suggestions d'autocomplétions dans la barre d'adresse** (1)

</div>

1. Cette option n'est pas disponible dans l'applications iOS de Brave.

#### Moteurs de recherche

Ces options se trouvent dans :material-menu:/:fontawesome-solid-ellipsis: → **Paramètres** → **Moteurs de recherches**.

- [ ] Décochez **Afficher les suggestions de recherche**

#### Brave Sync

La [Synchronisation Brave](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) permet à vos données de navigation (historique, favoris, etc.) d'être accessibles sur tous vos appareils sans nécessiter de compte et les protège avec E2EE.

## Cromite (Android)

<div class="admonition recommendation" markdown>

![logo de Cromite](assets/img/browsers/cromite.svg){ align=right }

**Cromite** est un navigateur basé sur Chromium qui intègre le blocage des publicités, des protections contre l'empreinte digitale, et d'autres [améliorations en matière de confidentialité et de sécurité](https://github.com/uazo/cromite/blob/master/docs/FEATURES.md). Il s'agit d'une version dérivée du navigateur populaire Bromite, aujourd'hui abandonné.

[:octicons-home-16: Page d'accueil](https://cromite.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uazo/cromite/blob/master/docs/PRIVACY_POLICY.md){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://github.com/uazo/cromite?tab=readme-ov-file#docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/uazo/cromite){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

 [:simple-android: F-Droid](https://cromite.org/fdroid/repo/?fingerprint=49F37E74DEE483DCA2B991334FB5A0200787430D0B5F9A783DD5F13695E9517B)
- [:simple-github: GitHub](https://github.com/uazo/cromite/releases/latest)

</details>

</div>

### Configuration recommandée

Ces options se trouvent dans :material-menu: -> :gear: **Paramètres** -> **Vie privée et sécurité**.

#### Données de navigation

- [x] Cochez **Fermer les onglets en quittant**

#### Mode navigation privée

- [x] Cochez **Ouvrir les liens externes en mode navigation privée**

#### Sécurité

- [x] Cochez **Toujours utiliser une connexion sécurisée**

Cela vous empêche de vous connecter involontairement à un site Web en "clair" HTTP. Les sites sans HTTPS sont rares de nos jours. Cela ne devrait donc avoir que peu ou pas d'impact sur votre navigation quotidienne.

#### Paramètres d'Adblock Plus

Ces options se trouvent dans :material-menu: → :gear:**Paramètres** → **Paramètres d'Adblock Plus**.

Cromite inclus une version personnalisée d'Adblock Plus avec EasyList activé par défaut, ainsi que des options pour sélectionner d'autres listes de filtres dans le menu **Listes de filtres**.

L'utilisation de listes supplémentaires vous distinguera des autres utilisateurs de Brave et peut également augmenter la surface d'attaque s'il y a une faille dans Brave et qu'une règle malveillante est ajoutée à l'une des listes que vous utilisez.

- \[x\] (Facultatif) Sélectionnez **Activer l'anti-contournement et les snippets**

Ce paramètre ajoute une liste Adblock Plus supplémentaire qui peut augmenter l'efficacité du blocage de contenu de Cromite. Les mises en garde concernant le fait de se démarquer et d'augmenter potentiellement la surface d'attaque s'appliquent.

#### Legacy Adblock settings

These options can be found in :material-menu: → :gear: **Settings** → **Legacy Adblock settings**.

- [ ] Décocher le paramètre de mise à jour automatique

This disables update checks for the unmaintained Bromite adblock filter.

## Safari (iOS)

On iOS, any app that can browse the web is [restricted](https://developer.apple.com/app-store/review/guidelines) to using an Apple-provided [WebKit framework](https://developer.apple.com/documentation/webkit), so a browser like [Brave](#brave) does not use the Blink engine (the core component of Chromium) like its counterparts on other operating systems.

<div class="admonition recommendation" markdown>

![Logo Safari](assets/img/browsers/safari.svg){ align=right }

**Safari** est le navigateur par défaut dans iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites, so more devices look identical), and fingerprint randomization, as well as Private Relay for those with a paid iCloud+ subscription.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title="Documentation" }

</details>

</div>

### Configuration recommandée pour Safari

We would suggest installing [AdGuard](browser-extensions.md#adguard) if you want a content blocker in Safari.

The following privacy/security-related options can be found in :gear: **Settings** → **Apps** → **Safari**.

#### Allow Safari to Access

Under **Siri**:

- [ ] Disable **Learn from this App**
- [ ] Disable **Show in App**
- [ ] Disable **Show on Home Screen**
- [ ] Disable **Suggest App**

This prevents Siri from using content from Safari for Siri suggestions.

#### Recherche

- [ ] Disable **Search Engine Suggestions**

Ce paramètre envoie tout ce que vous tapez dans la barre d'adresse au moteur de recherche défini dans Safari. La désactivation des suggestions de recherche vous permet de contrôler plus précisément les données que vous envoyez à votre fournisseur de moteur de recherche.

#### Profils

Safari vous permet de séparer votre navigation en différents profils. Tous vos cookies, votre historique et les données de votre site web sont séparés pour chaque profil. Vous devriez utiliser des profils différents pour des objectifs différents, par exemple pour les achats, le travail ou l'école.

#### Confidentialité & sécurité

- [x] Enable **Prevent Cross-Site Tracking**

This enables WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). The feature helps protect against unwanted tracking by using on-device machine learning to stop trackers. ITP protects against many common threats, but does not block all tracking avenues because it is designed to not interfere with website usability.

- [x] Enable **Require Face ID/Touch ID to Unlock Private Browsing**

This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

- [ ] Disable **Fraudulent Website Warning**

Ce paramètre utilise Google Safe Browsing (ou Tencent Safe Browsing pour les utilisateurs en Chine continentale ou à Hong Kong) pour vous protéger lorsque vous naviguez. Ainsi, votre adresse IP peut être enregistrée par votre fournisseur de services de navigation sécurisée. Si vous désactivez ce paramètre, la journalisation sera désactivée, mais vous risquez d'être plus vulnérable aux sites d'hameçonnage connus.

- [x] Enable **Not Secure Connection Warning**

Ce paramètre affiche un écran d'avertissement si votre connexion à un site web n'utilise pas HTTPS. Safari essaiera automatiquement de mettre à niveau le site vers HTTPS, de sorte que vous ne devriez voir ce message que lorsqu'il n'y a pas de connexion HTTPS disponible.

- [ ] Disable **Highlights**

Apple's privacy policy for Safari states:

> Lors de la visite d'une page web, Safari peut envoyer des informations calculées à partir de l'adresse de la page web à Apple via OHTTP afin de déterminer si des mises en évidence pertinentes sont disponibles.

#### Settings for Websites

Under **Camera**

- [x] Select **Ask**

Under **Microphone**

- [x] Select **Ask**

Under **Location**

- [x] Select **Ask**

These settings ensure that websites can only access your camera, microphone, or location after you explicitly grant them access.

#### Other Privacy Settings

These options can be found in :gear: **Settings** → **Apps** → **Safari** → **Advanced**.

##### Fingerprinting Mitigations

Le paramètre **Protection avancée contre le suivi et le vol des empreintes** randomise certaines valeurs afin qu'il soit plus difficile de prendre vos empreintes numérique :

- [x] Sélectionnez **Toutes les activités de navigation** ou **Navigation privée**

##### Mesure Publicitaire Préservant la vie privée

- [ ] Désactiver **Mesure Publicitaire Préservant la vie privée**

La mesure des clics publicitaires a traditionnellement utilisé une technologie de suivi qui porte atteinte à la vie privée des utilisateurs. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) est une fonctionnalité de WebKit et une proposition de norme web visant à permettre aux annonceurs de mesurer l'efficacité des campagnes web sans compromettre la confidentialité des utilisateurs.

Cette fonction ne pose que peu de problèmes de confidentialité en soi, et même si vous pouvez choisir de la laisser activée, nous considérons que le fait qu'elle soit automatiquement désactivée en Navigation Privée est un indicateur pour la désactiver.

#### Navigation Privée Permanente

Ouvrez Safari et appuyez sur le bouton Onglets, situé en bas à droite. Then, expand the :material-format-list-bulleted: Tab Groups list.

- [x] Sélectionner **Privé**

Le mode de Navigation Privée de Safari offre des protections supplémentaires en matière de confidentialité. La Navigation Privée utilise une nouvelle session [éphémère](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) pour chaque onglet, ce qui signifie que les onglets sont isolés les uns des autres. La navigation privée offre également d'autres avantages plus modestes en matière de protection de la vie privée, comme le fait de ne pas envoyer l'adresse d'une page web à Apple lors de l'utilisation de la fonction de traduction de Safari.

Notez que la navigation privée n'enregistre pas les cookies et les données des sites web, et qu'il ne sera donc pas possible de rester connecté aux sites. Cela peut être un inconvénient.

#### Synchronisation iCloud

La synchronisation de l'Historique de Safari, des Groupes d'Onglets, des Onglets iCloud et des mots de passe enregistrés est E2EE. Cependant, par défaut, les favoris ne le sont [pas](https://support.apple.com/HT202303). Apple peut les déchiffrer et y accéder conformément à sa [politique de confidentialité](https://apple.com/legal/privacy/en-ww).

Vous pouvez activer l'E2EE pour vos favoris et vos téléchargements Safari en activant la [Protection avancée des données](https://support.apple.com/HT212520). Go to :gear: **Settings** → **iCloud** → **Advanced Data Protection**.

- [x] Activez **Protection avancée des données**

Si vous utilisez iCloud avec la Protection Avancée des Données désactivée, nous vous recommandons également de vérifier que l'emplacement de téléchargement par défaut de Safari est défini sur localement sur votre appareil. This option can be found in :gear: **Settings** → **Apps** → **Safari** → **General** → **Downloads**.

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Doit prendre en charge les mises à jour automatiques.
- Doit recevoir rapidement les mises à jour du moteur web parent.
- Doit prendre en charge le blocage du contenu.
- Les modifications nécessaires pour rendre le navigateur plus respectueux de la vie privée ne devraient pas avoir d'impact négatif sur l'expérience des utilisateurs.
