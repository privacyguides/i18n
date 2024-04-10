---
meta_title: "Navigateurs web respectueux de la vie privée pour Android et iOS - Privacy Guides"
title: "Navigateurs mobiles"
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
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://apple.com/safari
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

Il s'agit des navigateurs web mobiles et des configurations que nous recommandons actuellement. Si vous avez besoin de naviguer anonymement sur Internet, vous devriez plutôt utiliser [Tor](tor.md). D'une manière générale, nous vous recommandons de limiter au maximum les extensions ; elles ont un accès privilégié dans votre navigateur, vous obligent à faire confiance au développeur, peuvent vous faire sortir du lot [](https://fr.wikipedia.org/wiki/Empreinte_digitale_d%27appareil), et [affaiblissent l'isolation du site](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) .

## Android

### Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave est basé sur le projet de navigateur Web Chromium. Il devrait donc vous être familier et présenter un minimum de problèmes de compatibilité avec les sites Web.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

#### Recommended Brave Configuration

Le navigateur Tor est le seul moyen de vraiment naviguer anonymement sur Internet. Lorsque vous utilisez Brave, nous vous recommandons de modifier les paramètres suivants afin de protéger votre vie privée de certains tiers, mais tous les navigateurs autres que le [Navigateur Tor](tor.md#tor-browser) seront traçables par *quelqu'un* d'une manière ou d'une autre.

Ces options se trouvent dans :material-menu: → **Paramètres** → **Brave Shields & confidentialité**

##### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

##### Les valeurs par défaut de Brave Shields

Les options "Boucliers" peuvent être réduites par site selon les besoins, mais par défaut, nous recommandons de définir les paramètres suivants:

<div class="annotate" markdown>

- [x] Sélectionnez **Agressif** dans **Bloquer les traqueurs et les publicités**

<details class="warning" markdown>
<summary>Utiliser les listes de filtres par défaut</summary>

Brave vous permet de sélectionner des filtres de contenu supplémentaires dans la page interne `brave://adblock`. Nous vous déconseillons d'utiliser cette fonctionnalité ; conservez plutôt les listes de filtres par défaut. L'utilisation de listes supplémentaires vous distinguera des autres utilisateurs de Brave et peut également augmenter la surface d'attaque s'il y a une faille dans Brave et qu'une règle malveillante est ajoutée à l'une des listes que vous utilisez.

</details>

- [x] Sélectionnez **Mettre à niveau les connexions vers HTTPS**
- [x] Sélectionnez **Toujours utiliser des connexions sécurisées**
- [x] (Facultatif) Sélectionnez **Bloquer les scripts** (1)
- [x] Sélectionnez **Strict, peut casser les sites** sous **Bloquer les empreintes numériques**

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net) extension.

##### Effacer les données de navigation

- [x] Sélectionner **Effacer les données en quittant**

##### Blocage des Réseaux Sociaux

- [ ] Décochez toutes les fonctionnalités de médias sociaux

##### Autres paramètres de confidentialité

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP handling policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Allow sites to check if you have payment methods saved**
- [ ] Uncheck **IPFS Gateway** (1)
- [x] Select **Close tabs on exit**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Automatically send daily usage ping to Brave**

</div>

1. InterPlanetary File System (IPFS) est un réseau décentralisé, de pair à pair, permettant de stocker et de partager des données dans un système de fichiers distribué. À moins que vous n'utilisiez cette fonctionnalité, désactivez-la.

#### Synchronisation Brave

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

### Mull

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Firefox (Gecko)-based browsers on Android [lack per-site process isolation](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196), a powerful security feature that offers additional protection against a malicious website exploiting a security vulnerability. Missing this feature likely won't pose an issue for low-risk web browsers who keep their browser up-to-date, but those visiting higher-risk sites or at risk of targeted/0-day attacks should strongly consider a Chromium-based browser like [Brave](#brave) instead.

</div>

<div class="admonition recommendation" markdown>

![Mull logo](assets/img/browsers/mull.svg){ align=right }

**Mull** is a privacy oriented and deblobbed Android browser based on Firefox. Compared to Firefox, it offers much greater fingerprinting protection out of the box, and disables JavaScript Just-in-Time (JIT) compilation for enhanced security. It also removes all proprietary elements from Firefox, such as replacing Google Play Services references.

[:octicons-home-16: Homepage](https://divestos.org/pages/our_apps#mull){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://divestos.org/pages/browsers#tuningFenix){ .card-link title=Documentation }
[:octicons-code-16:](https://codeberg.org/divested-mobile/mull-fenix){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-fdroid: F-Droid](https://f-droid.org/en/packages/us.spotco.fennec_dos/)

</details>

</div>

Enable DivestOS's [F-Droid Repo](https://divestos.org/fdroid/official/) to receive updates directly from the developer. Downloading Mull from the default F-Droid repo will mean your updates could be delayed by a few days or longer.

Mull enables many features upstreamed by the [Tor uplift project](https://wiki.mozilla.org/Security/Tor_Uplift) using preferences from [Arkenfox](desktop-browsers.md#arkenfox-advanced). Proprietary blobs are removed from Mozilla's code using the scripts developed for Fennec F-Droid.

#### Recommended Mull Configuration

We would suggest installing [uBlock Origin](browser-extensions.md#ublock-origin) as a content blocker if you want to block trackers within Mull.

Mull comes with privacy protecting settings configured by default. You might consider configuring the **Delete browsing data on quit** options in Mull's settings if you want to close all your open tabs when quitting the app automatically, or clear other data such as browsing history and cookies automatically.

## iOS

Sur iOS, toute application capable de naviguer sur le web est [](https://developer.apple.com/app-store/review/guidelines) limitée à l'utilisation du cadre WebKit [fourni par Apple](https://developer.apple.com/documentation/webkit), de sorte qu'il y a peu de raisons d'utiliser un navigateur web tiers.

### Safari

<div class="admonition recommendation" markdown>

![Logo Safari](assets/img/browsers/safari.svg){ align=right }

**Safari** est le navigateur par défaut dans iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Privacy Report, isolated and ephemeral Private Browsing tabs, iCloud Private Relay, fingerprinting protection by randomizing and presenting a simplified version of the system configuration to websites so more devices look identical, and the ability to lock private tabs with your biometrics/PIN. Il vous permet également de séparer votre navigation selon différents profils.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentation}

</details>

</div>

#### Recommended Safari Configuration

We would suggest installing [AdGuard](browser-extensions.md#adguard) as a content blocker if you want to block trackers within Safari.

The following privacy/security-related options can be found in the :gear: **Settings** app → **Safari**

##### Profils

Tous vos cookies, votre historique et les données des sites web seront séparés pour chaque profil. Vous devriez utiliser des profils différents pour des objectifs différents, par exemple pour les achats, le travail ou l'école.

##### Confidentialité & sécurité

- [x] Activer **Empêcher le Pistage Intersite**

    Cela active la [Protection Intelligente contre le Pistage](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp) de WebKit. Cette fonction permet de se protéger contre les pistages non désirés en utilisant un apprentissage machine sur l'appareil pour arrêter les traqueurs. ITP protège contre de nombreuses menaces courantes, mais il ne bloque pas toutes les voies de pistage, car il est conçu pour ne pas interférer avec la convivialité des sites Web.

- [x] Activer **Exiger Face ID pour déverrouiller la navigation privée**

    Ce paramètre vous permet de verrouiller vos onglets privés derrière des données biométriques/PIN lorsque vous ne les utilisez pas.

##### Avancé → Confidentialité

Le paramètre **Protection avancée contre le suivi et le vol des empreintes** randomise certaines valeurs afin qu'il soit plus difficile de prendre vos empreintes numérique :

- [x] Sélectionnez **Toutes les activités de navigation** ou **Navigation privée**

##### Rapport de Confidentialité

Le Rapport de Confidentialité donne un aperçu des traqueurs intersites qui sont actuellement bloqués sur le site Web que vous visitez et ne peuvent pas vous profiler. Il peut également afficher un rapport hebdomadaire pour montrer quels traqueurs ont été bloqués au fil du temps.

Le Rapport de Confidentialité est accessible via le menu Paramètres de Page.

##### Mesure Publicitaire Préservant la vie privée

- [ ] Désactiver **Mesure Publicitaire Préservant la vie privée**

La mesure des clics publicitaires a traditionnellement utilisé une technologie de suivi qui porte atteinte à la vie privée des utilisateurs. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

Cette fonction ne pose que peu de problèmes de confidentialité en soi, et même si vous pouvez choisir de la laisser activée, nous considérons que le fait qu'elle soit automatiquement désactivée en Navigation Privée est un indicateur pour la désactiver.

##### Navigation Privée Permanente

Ouvrez Safari et appuyez sur le bouton Onglets, situé en bas à droite. Ensuite, développez la liste des Groupes d'Onglets.

- [x] Sélectionner **Privé**

Le mode de Navigation Privée de Safari offre des protections supplémentaires en matière de confidentialité. La Navigation Privée utilise une nouvelle session [éphémère](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) pour chaque onglet, ce qui signifie que les onglets sont isolés les uns des autres. La Navigation Privée présente également d'autres avantages mineurs en matière de protection de la vie privée, comme le fait de ne pas envoyer l'adresse d'une page web à Apple lors de l'utilisation de la fonction de traduction de Safari.

Notez que la Navigation Privée n'enregistre pas les cookies et les données des sites web. Il ne sera donc pas possible de rester connecté aux sites. Cela peut être un inconvénient.

##### Synchronisation iCloud

La synchronisation de l'Historique de Safari, des Groupes d'Onglets, des Onglets iCloud et des mots de passe enregistrés est E2EE. However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://apple.com/legal/privacy/en-ww).

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/HT212520). Accédez à votre **nom d'identifiant Apple → iCloud → Protection Avancée des Données**.

- [x] Activez **Protection Avancée des Données**

Si vous utilisez iCloud avec la Protection Avancée des Données désactivée, nous vous recommandons également de vérifier que l'emplacement de téléchargement par défaut de Safari est défini sur localement sur votre appareil. Cette option se trouve dans :gear: **Paramètres** → **Safari** → **Général** → **Téléchargements**.

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Doit prendre en charge les mises à jour automatiques.
- Must receive engine updates from upstream releases quickly.
- Must support content blocking.
- Les modifications nécessaires pour rendre le navigateur plus respectueux de la vie privée ne devraient pas avoir d'impact négatif sur l'expérience des utilisateurs.
