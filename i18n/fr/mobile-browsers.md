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

![Logo Brave](assets/img/browsers/brave.svg){ align=right }

Le navigateur **Brave** comprend un bloqueur de contenu intégré et des [fonctions de confidentialité](https://brave.com/privacy-features/), dont la plupart sont activées par défaut.

Brave est basé sur le projet de navigateur Web Chromium. Il devrait donc vous être familier et présenter un minimum de problèmes de compatibilité avec les sites Web.

[:octicons-home-16: Page d'accueil](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Service onion" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

#### Configuration recommandée pour Brave

Le navigateur Tor est le seul moyen de vraiment naviguer anonymement sur Internet. Lorsque vous utilisez Brave, nous vous recommandons de modifier les paramètres suivants afin de protéger votre vie privée de certains tiers, mais tous les navigateurs autres que le [Navigateur Tor](tor.md#tor-browser) seront traçables par *quelqu'un* d'une manière ou d'une autre.

Ces options se trouvent dans :material-menu: → **Paramètres** → **Brave Shields & confidentialité**

##### Shields

Brave inclut des mesures anti-empreintes digitales dans sa fonction [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Nous vous conseillons de configurer ces options de [manière globale](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) sur toutes les pages que vous visitez.

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

1. Cette option fournit une fonctionnalité similaire aux [modes de blocage](https://github.com/gorhill/uBlock/wiki/Blocking-mode) avancés de uBlock Origin ou l'extension [NoScript](https://noscript.net).

##### Effacer les données de navigation

- [x] Sélectionner **Effacer les données en quittant**

##### Blocage des Réseaux Sociaux

- [ ] Décochez toutes les fonctionnalités de médias sociaux

##### Autres paramètres de confidentialité

<div class="annotate" markdown>

- [x] Sélectionnez **Désactiver l'UDP pas en proxy** sous [Politique de gestion des adresses IP WebRTC](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Décochez **Autorisez les sites à vérifier si vous avez enregistré des méthodes de paiement**
- [ ] Décochez **Passerelle IPFS** (1)
- [x] Sélectionnez **Fermer les onglets lorsque vous quittez**
- [ ] Décochez **Autoriser l'analyse de produits respectueuse de la vie privée (P3A)**
- [ ] Décochez **Envoyer automatiquement les rapports de diagnostic**
- [ ] Décochez **Envoyer automatiquement un signal d'utilisation quotidienne à Brave**

</div>

1. InterPlanetary File System (IPFS) est un réseau décentralisé, de pair à pair, permettant de stocker et de partager des données dans un système de fichiers distribué. À moins que vous n'utilisiez cette fonctionnalité, désactivez-la.

#### Synchronisation Brave

La [Synchronisation Brave](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) permet à vos données de navigation (historique, favoris, etc.) d'être accessibles sur tous vos appareils sans nécessiter de compte et les protège avec E2EE.

### Mull

<div class="admonition recommendation" markdown>

![Logo Mull](assets/img/browsers/mull.svg){ align=right }

**Mull** est un navigateur Android basé sur Firefox, orienté vers la protection de la vie privée et déblobé. Par rapport à Firefox, il offre d'emblée une bien meilleure protection contre la capture d'empreintes numérique et désactive la compilation JavaScript Just-in-Time (JIT) pour une sécurité accrue. Il supprime également tous les éléments propriétaires de Firefox, comme le remplacement des références à Google Play Services.

[:octicons-home-16: Page d'accueil](https://divestos.org/pages/our_apps#mull){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://divestos.org/pages/browsers#tuningFenix){ .card-link title=Documentation }
[:octicons-code-16:](https://codeberg.org/divested-mobile/mull-fenix){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-fdroid: F-Droid](https://f-droid.org/en/packages/us.spotco.fennec_dos)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Les navigateurs basés sur Firefox (Gecko) sur Android [n'ont pas](https://bugzilla.mozilla.org/show_bug.cgi?id=1610822) [d'isolation de site](https://wiki.mozilla.org/Project_Fission),[^1] une fonction de sécurité puissante qui protège contre un site malveillant effectuant une attaque de type [Spectre](https://fr.wikipedia.org/wiki/Spectre_(vuln%C3%A9rabilit%C3%A9)) pour accéder à la mémoire d'un autre site web que vous avez ouvert.[^2] Les navigateurs basés sur Chromium comme [Brave](#brave) fourniront une protection plus robuste contre les sites web malveillants.

</div>

Activez le [dépôt F-Droid](https://divestos.org/fdroid/official) de DivestOS pour recevoir les mises à jour directement du développeur. En téléchargeant Mull à partir du dépôt par défaut de F-Droid, vos mises à jour pourraient être retardées de quelques jours ou plus.

Mull active de nombreuses fonctionnalités récupérées du [projet Tor uplift](https://wiki.mozilla.org/Security/Tor_Uplift) en utilisant les préférences d'[Arkenfox](desktop-browsers.md#arkenfox-advanced). Les blobs propriétaires sont supprimés du code de Mozilla à l'aide des scripts développés pour Fennec F-Droid.

#### Configuration Mull recommandée

Nous vous conseillons d'installer [uBlock Origin](browser-extensions.md#ublock-origin) comme bloqueur de contenu si vous souhaitez bloquer les traqueurs dans Mull.

Mull est livré avec des paramètres de protection de la vie privée configurés par défaut. Vous pouvez envisager de configurer les options **Supprimer les données de navigation lorsque l'on quitte l'application** dans les paramètres de Mull si vous souhaitez fermer automatiquement tous vos onglets ouverts lorsque vous quittez l'application, ou effacer automatiquement d'autres données telles que l'historique de navigation et les cookies.

Les protections de la vie privée activées par défaut sur Mull étant plus avancées et plus strictes que celles de la plupart des navigateurs, il est possible que certains sites web ne se chargent pas ou ne fonctionnent pas correctement si vous n'ajustez pas ces paramètres. Vous pouvez consulter cette [liste de problèmes connus et de solutions de contournement](https://divestos.org/pages/broken#mull) pour obtenir des conseils sur une solution potentielle si vous rencontrez un site défectueux. Le fait d'ajuster un paramètre afin de corriger un site web peut avoir un impact sur votre vie privée/sécurité, assurez-vous donc de bien comprendre toutes les instructions que vous suivez.

## iOS

Sur iOS, toute application capable de naviguer sur le web est [](https://developer.apple.com/app-store/review/guidelines) limitée à l'utilisation du cadre WebKit [fourni par Apple](https://developer.apple.com/documentation/webkit), de sorte qu'il y a peu de raisons d'utiliser un navigateur web tiers.

### Safari

<div class="admonition recommendation" markdown>

![Logo Safari](assets/img/browsers/safari.svg){ align=right }

**Safari** est le navigateur par défaut dans iOS. Il inclut des [fonctions de confidentialité](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0) telles que [la protection intelligente contre le pistage](https://webkit.org/blog/7675/intelligent-tracking-prevention/), le rapport de confidentialité, des onglets de navigation privée isolés et éphémères, le relais privé iCloud, la protection contre la capture d'empreintes numériques en randomisant et présentant une version simplifiée de la configuration du système aux sites web afin que d'avantage d'appareils soient identiques, et la possibilité de verrouiller les onglets privés à l'aide de vos données biométriques ou de votre code PIN. Il vous permet également de séparer votre navigation selon différents profils.

[:octicons-home-16: Page d'accueil](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentation}

</details>

</div>

#### Configuration recommandée pour Safari

Nous vous conseillons d'installer [AdGuard](browser-extensions.md#adguard) en tant que bloqueur de contenu si vous souhaitez bloquer les traqueurs dans Safari.

Les options suivantes relatives à la vie privée et à la sécurité se trouvent dans l'application :gear: **Réglages** → **Safari**

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

La mesure des clics publicitaires a traditionnellement utilisé une technologie de suivi qui porte atteinte à la vie privée des utilisateurs. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) est une fonctionnalité de WebKit et une proposition de norme web visant à permettre aux annonceurs de mesurer l'efficacité des campagnes web sans compromettre la confidentialité des utilisateurs.

Cette fonction ne pose que peu de problèmes de confidentialité en soi, et même si vous pouvez choisir de la laisser activée, nous considérons que le fait qu'elle soit automatiquement désactivée en Navigation Privée est un indicateur pour la désactiver.

##### Navigation Privée Permanente

Ouvrez Safari et appuyez sur le bouton Onglets, situé en bas à droite. Ensuite, développez la liste des Groupes d'Onglets.

- [x] Sélectionner **Privé**

Le mode de Navigation Privée de Safari offre des protections supplémentaires en matière de confidentialité. La Navigation Privée utilise une nouvelle session [éphémère](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) pour chaque onglet, ce qui signifie que les onglets sont isolés les uns des autres. La Navigation Privée présente également d'autres avantages mineurs en matière de protection de la vie privée, comme le fait de ne pas envoyer l'adresse d'une page web à Apple lors de l'utilisation de la fonction de traduction de Safari.

Notez que la Navigation Privée n'enregistre pas les cookies et les données des sites web. Il ne sera donc pas possible de rester connecté aux sites. Cela peut être un inconvénient.

##### Synchronisation iCloud

La synchronisation de l'Historique de Safari, des Groupes d'Onglets, des Onglets iCloud et des mots de passe enregistrés est E2EE. Cependant, par défaut, les favoris ne le sont [pas](https://support.apple.com/HT202303). Apple peut les déchiffrer et y accéder conformément à sa [politique de confidentialité](https://apple.com/legal/privacy/en-ww).

Vous pouvez activer l'E2EE pour vos favoris et vos téléchargements Safari en activant la [Protection avancée des données](https://support.apple.com/HT212520). Accédez à votre **nom d'identifiant Apple → iCloud → Protection avancée des données**.

- [x] Activez **Protection avancée des données**

Si vous utilisez iCloud avec la Protection avancée des données désactivée, nous vous recommandons également de vérifier que l'emplacement de téléchargement par défaut de Safari est défini sur localement sur votre appareil. Cette option se trouve dans :gear: **Paramètres** → **Safari** → **Général** → **Téléchargements**.

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Doit prendre en charge les mises à jour automatiques.
- Doit recevoir rapidement les mises à jour du moteur web parent.
- Doit prendre en charge le blocage du contenu.
- Les modifications nécessaires pour rendre le navigateur plus respectueux de la vie privée ne devraient pas avoir d'impact négatif sur l'expérience des utilisateurs.
