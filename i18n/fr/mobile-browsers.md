---
meta_title: "Privacy Respecting Web Browsers for Android and iOS - Privacy Guides"
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
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Capitalisme de surveillance](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our currently recommended **mobile web browsers** and configurations for standard/non-anonymous internet browsing. Si vous avez besoin de naviguer anonymement sur Internet, vous devriez plutôt utiliser [Tor](tor.md).

## Brave

<div class="admonition recommendation" markdown>

![Logo Brave](assets/img/browsers/brave.svg){ align=right }

Le navigateur **Brave** comprend un bloqueur de contenu intégré et des [fonctions de confidentialité](https://brave.com/privacy-features/), dont la plupart sont activées par défaut.

Brave est basé sur le projet de navigateur Web Chromium. Il devrait donc vous être familier et présenter un minimum de problèmes de compatibilité avec les sites Web.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

### Configuration recommandée pour Brave

Le navigateur Tor est le seul moyen de vraiment naviguer anonymement sur Internet. Lorsque vous utilisez Brave, nous vous recommandons de modifier les paramètres suivants afin de protéger votre vie privée de certains tiers, mais tous les navigateurs autres que le [Navigateur Tor](tor.md#tor-browser) seront traçables par *quelqu'un* d'une manière ou d'une autre.

=== "Android"

    These options can be found in :material-menu: → **Settings** → **Brave Shields & privacy**.

=== "iOS"

    These options can be found in :fontawesome-solid-ellipsis: → **Settings** → **Shields & Privacy**.

#### Brave shields global defaults

Brave inclut des mesures anti-empreintes digitales dans sa fonction [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Nous vous conseillons de configurer ces options de [manière globale](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) sur toutes les pages que vous visitez.

Les options "Boucliers" peuvent être réduites par site selon les besoins, mais par défaut, nous recommandons de définir les paramètres suivants:

=== "Android"

    <div class="annotate" markdown>

    - [x] Select **Aggressive** under *Block trackers & ads*
    - [x] Select **Auto-redirect AMP pages**
    - [x] Select **Auto-redirect tracking URLs**
    - [x] Select **Require all connections to use HTTPS (strict)** under *Upgrade connections to HTTPS*
    - \[x\] (Optional) Select **Block Scripts** (1)
    - [x] Select **Block third-party cookies** under *Block Cookies*
    - [x] Select **Block Fingerprinting**
    - [x] Select **Prevent fingerprinting via language settings**

    <details class="warning" markdown>
    <summary>Use default filter lists</summary>

    Brave allows you to select additional content filters within the **Content Filtering** menu or the internal `brave://adblock` page. Nous vous déconseillons d'utiliser cette fonctionnalité ; conservez plutôt les listes de filtres par défaut. L'utilisation de listes supplémentaires vous distinguera des autres utilisateurs de Brave et peut également augmenter la surface d'attaque s'il y a une faille dans Brave et qu'une règle malveillante est ajoutée à l'une des listes que vous utilisez.

    </details>

    - [x] Select **Forget me when I close this site**

    </div>

    1. This option disables JavaScript, which will break a lot of sites. To unbreak them, you can set exceptions on a per-site basis by tapping on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

=== "iOS"

    <div class="annotate" markdown>

    - [x] Select **Aggressive** under *Trackers & Ads Blocking*
    - [x] Select **Strict** under *Upgrade Connections to HTTPS*
    - [x] Select **Auto-Redirect AMP pages**
    - [x] Select **Auto-Redirect Tracking URLs**
    - \[x\] (Optional) Select **Block Scripts** (1)
    - [x] Select **Block Fingerprinting**

    <details class="warning" markdown>
    <summary>Use default filter lists</summary>

    Brave allows you to select additional content filters within the **Content Filtering** menu. Nous vous déconseillons d'utiliser cette fonctionnalité ; conservez plutôt les listes de filtres par défaut. L'utilisation de listes supplémentaires vous distinguera des autres utilisateurs de Brave et peut également augmenter la surface d'attaque s'il y a une faille dans Brave et qu'une règle malveillante est ajoutée à l'une des listes que vous utilisez.

    </details>

    </div>

    1. This option disables JavaScript, which will break a lot of sites. To unbreak them, you can set exceptions on a per-site basis by tapping on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

##### Clear browsing data (Android only)

- [x] Sélectionner **Effacer les données en quittant**

##### Social Media Blocking (Android only)

- [ ] Décochez toutes les fonctionnalités de médias sociaux

#### Other privacy settings

=== "Android"

    <div class="annotate" markdown>

    - [x] Select **Disable non-proxied UDP** under [*WebRTC IP handling policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
    - \[x\] (Optional) Select **No protection** under *Safe Browsing* (1)
    - [ ] Uncheck **Allow sites to check if you have payment methods saved**
    - [x] Select **Close tabs on exit**
    - [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
    - [ ] Uncheck **Automatically send diagnostic reports**
    - [ ] Uncheck **Automatically send daily usage ping to Brave**

    </div>

    1. Brave's [implementation of Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) on Android **does not** proxy [Safe Browsing network requests](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) like its desktop counterpart. This means that your IP address may be seen (and logged) by Google. Note that Safe Browsing is not available for Android devices without Google Play Services.

=== "iOS"

    - [ ] Uncheck **Allow Privacy-Preserving Product Analytics (P3A)**
    - [ ] Uncheck **Automatically send daily usage ping to Brave**

#### Leo

These options can be found in :material-menu: → **Settings** → **Leo**.

<div class="annotate" markdown>

- [ ] Uncheck **Show autocomplete suggestions in address bar** (1)

</div>

1. This option is not present in Brave's iOS app.

#### Search engines

These options can be found in :material-menu:/:fontawesome-solid-ellipsis: → **Settings** → **Search engines**.

- [ ] Décochez **Afficher les suggestions de recherche**

#### Brave Sync

La [Synchronisation Brave](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) permet à vos données de navigation (historique, favoris, etc.) d'être accessibles sur tous vos appareils sans nécessiter de compte et les protège avec E2EE.

## Cromite (Android)

<div class="admonition recommendation" markdown>

![Cromite logo](assets/img/browsers/cromite.svg){ align=right }

**Cromite** is a Chromium-based browser with built-in ad blocking, fingerprinting protections, and other [privacy and security enhancements](https://github.com/uazo/cromite/blob/master/docs/FEATURES.md). It is a fork of the discontinued **Bromite** browser.

[:octicons-home-16: Homepage](https://www.cromite.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uazo/cromite/blob/master/docs/PRIVACY_POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/uazo/cromite?tab=readme-ov-file#docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/uazo/cromite){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: F-Droid](https://www.cromite.org/fdroid/repo/?fingerprint=49F37E74DEE483DCA2B991334FB5A0200787430D0B5F9A783DD5F13695E9517B)
- [:simple-github: GitHub](https://github.com/uazo/cromite/releases/latest)

</details>

</div>

### Configuration recommandée

These options can be found in :material-menu: → :gear: **Settings** → **Privacy and security**.

#### Browsing data

- [x] Select **Close all open tabs on exit**

#### Incognito mode

- [x] Select **Open external links in incognito**

#### Sécurité

- [x] Select **Always use secure connections**

Cela vous empêche de vous connecter involontairement à un site Web en "clair" HTTP. HTTP is extremely uncommon nowadays, so this should have little to no impact on your day-to-day browsing.

#### Adblock Plus settings

These options can be found in :material-menu: → :gear: **Settings** → **Adblock Plus settings**.

Cromite contains a customized version of Adblock Plus with EasyList enabled by default, as well as options to select more filter lists within the **FIlter lists** menu.

Using extra lists will make you stand out from other Cromite users and may also increase attack surface if a malicious rule is added to one of the lists you use.

- \[x\] (Optional) Select **Enable anti-circumvention and snippets**

This setting adds an additional Adblock Plus list that may increase the effectiveness of Cromite's content blocking. The warnings about standing out and potentially increasing attack surface apply.

#### Legacy Adblock settings

These options can be found in :material-menu: → :gear: **Settings** → **Legacy Adblock settings**.

- [ ] Uncheck the autoupdate setting

This disables update checks for the unmaintained Bromite adblock filter.

## Mull (Android)

<div class="admonition recommendation" markdown>

![Logo Mull](assets/img/browsers/mull.svg){ align=right }

**Mull** est un navigateur Android basé sur Firefox, orienté vers la protection de la vie privée et déblobé. Par rapport à Firefox, il offre d'emblée une bien meilleure protection contre la capture d'empreintes numérique et désactive la compilation JavaScript Just-in-Time (JIT) pour une sécurité accrue. Il supprime également tous les éléments propriétaires de Firefox, comme le remplacement des références à Google Play Services.

[:octicons-home-16: Homepage](https://divestos.org/pages/our_apps#mull){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://divestos.org/pages/browsers#tuningFenix){ .card-link title="Documentation" }
[:octicons-code-16:](https://codeberg.org/divested-mobile/mull-fenix){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-fdroid: F-Droid](https://f-droid.org/en/packages/us.spotco.fennec_dos)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Les navigateurs basés sur Firefox (Gecko) sur Android [n'ont pas](https://bugzilla.mozilla.org/show_bug.cgi?id=1610822) [d'isolation de site](https://wiki.mozilla.org/Project_Fission),[^1] une fonction de sécurité puissante qui protège contre un site malveillant effectuant une attaque de type [Spectre](https://fr.wikipedia.org/wiki/Spectre_(vuln%C3%A9rabilit%C3%A9)) pour accéder à la mémoire d'un autre site web que vous avez ouvert.[^2] Les navigateurs basés sur Chromium comme [Brave](#brave) fourniront une protection plus robuste contre les sites web malveillants.

</div>

Enable DivestOS's [F-Droid repository](https://divestos.org/fdroid/official) to receive updates directly from the developer. En téléchargeant Mull à partir du dépôt par défaut de F-Droid, vos mises à jour pourraient être retardées de quelques jours ou plus.

Mull active de nombreuses fonctionnalités récupérées du [projet Tor uplift](https://wiki.mozilla.org/Security/Tor_Uplift) en utilisant les préférences d'[Arkenfox](desktop-browsers.md#arkenfox-advanced). Les blobs propriétaires sont supprimés du code de Mozilla à l'aide des scripts développés pour Fennec F-Droid.

### Recommended Mull Configuration

Nous vous conseillons d'installer [uBlock Origin](browser-extensions.md#ublock-origin) comme bloqueur de contenu si vous souhaitez bloquer les traqueurs dans Mull.

Mull est livré avec des paramètres de protection de la vie privée configurés par défaut. Vous pouvez envisager de configurer les options **Supprimer les données de navigation lorsque l'on quitte l'application** dans les paramètres de Mull si vous souhaitez fermer automatiquement tous vos onglets ouverts lorsque vous quittez l'application, ou effacer automatiquement d'autres données telles que l'historique de navigation et les cookies.

Les protections de la vie privée activées par défaut sur Mull étant plus avancées et plus strictes que celles de la plupart des navigateurs, il est possible que certains sites web ne se chargent pas ou ne fonctionnent pas correctement si vous n'ajustez pas ces paramètres. Vous pouvez consulter cette [liste de problèmes connus et de solutions de contournement](https://divestos.org/pages/broken#mull) pour obtenir des conseils sur une solution potentielle si vous rencontrez un site défectueux. Le fait d'ajuster un paramètre afin de corriger un site web peut avoir un impact sur votre vie privée/sécurité, assurez-vous donc de bien comprendre toutes les instructions que vous suivez.

## Safari (iOS)

On iOS, any app that can browse the web is [restricted](https://developer.apple.com/app-store/review/guidelines) to using an Apple-provided [WebKit framework](https://developer.apple.com/documentation/webkit), so a browser like [Brave](#brave) does not use the Chromium engine like its counterparts on other operating systems.

<div class="admonition recommendation" markdown>

![Logo Safari](assets/img/browsers/safari.svg){ align=right }

**Safari** est le navigateur par défaut dans iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites so more devices look identical), and fingerprint randomization, as well as Private Relay for those with a paid iCloud+ subscription.

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

This setting sends whatever you type in the address bar to the search engine set in Safari. La désactivation des suggestions de recherche vous permet de contrôler plus précisément les données que vous envoyez à votre fournisseur de moteur de recherche.

#### Profils

Safari allows you to separate your browsing with different profiles. All of your cookies, history, and website data are separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

#### Confidentialité & sécurité

- [x] Enable **Prevent Cross-Site Tracking**

This enables WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). The feature helps protect against unwanted tracking by using on-device machine learning to stop trackers. ITP protects against many common threats, but does not block all tracking avenues because it is designed to not interfere with website usability.

- [x] Enable **Require Face ID/Touch ID to Unlock Private Browsing**

This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

- [ ] Disable **Fraudulent Website Warning**

This setting uses Google Safe Browsing (or Tencent Safe Browsing for users in mainland China or Hong Kong) to protect you while you browse. As such, your IP address may be logged by your Safe Browsing provider. Disabling this setting will disable this logging, but you might be more vulnerable to known phishing sites.

- [ ] Disable **Highlights**

Apple's privacy policy for Safari states:

> When visiting a webpage, Safari may send information calculated from the webpage address to Apple over OHTTP to determine if relevant highlights are available.

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

Le mode de Navigation Privée de Safari offre des protections supplémentaires en matière de confidentialité. La Navigation Privée utilise une nouvelle session [éphémère](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) pour chaque onglet, ce qui signifie que les onglets sont isolés les uns des autres. La Navigation Privée présente également d'autres avantages mineurs en matière de protection de la vie privée, comme le fait de ne pas envoyer l'adresse d'une page web à Apple lors de l'utilisation de la fonction de traduction de Safari.

Do note that Private Browsing does not save cookies and website data, so it won't be possible to remain signed in to sites. Cela peut être un inconvénient.

#### Synchronisation iCloud

La synchronisation de l'Historique de Safari, des Groupes d'Onglets, des Onglets iCloud et des mots de passe enregistrés est E2EE. Cependant, par défaut, les favoris ne le sont [pas](https://support.apple.com/HT202303). Apple peut les déchiffrer et y accéder conformément à sa [politique de confidentialité](https://apple.com/legal/privacy/en-ww).

Vous pouvez activer l'E2EE pour vos favoris et vos téléchargements Safari en activant la [Protection avancée des données](https://support.apple.com/HT212520). Go to :gear: **Settings** → **iCloud** → **Advanced Data Protection**.

- [x] Turn on **Advanced Data Protection**

If you use iCloud with Advanced Data Protection disabled, we also recommend setting Safari's default download location to a local folder on your device. This option can be found in :gear: **Settings** → **Apps** → **Safari** → **General** → **Downloads**.

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Doit prendre en charge les mises à jour automatiques.
- Doit recevoir rapidement les mises à jour du moteur web parent.
- Doit prendre en charge le blocage du contenu.
- Les modifications nécessaires pour rendre le navigateur plus respectueux de la vie privée ne devraient pas avoir d'impact négatif sur l'expérience des utilisateurs.
