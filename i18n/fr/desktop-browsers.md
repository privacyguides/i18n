---
meta_title: "Navigateurs web respectueux de la vie privée pour PC et Mac - Privacy Guides"
title: "Navigateurs de bureau"
icon: material/laptop
description: Ces navigateurs respectueux de la vie privée sont ceux que nous recommandons actuellement pour la navigation internet standard/non-anonyme sur les ordinateurs de bureau.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Recommandations de navigateurs de bureau privés
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/fr/browser
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Firefox
    image: /assets/img/browsers/firefox.svg
    url: https://firefox.com
    sameAs: https://fr.wikipedia.org/wiki/Mozilla_Firefox
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    sameAs: https://fr.wikipedia.org/wiki/Brave_(navigateur_web)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Protège contre la (les) menace(s) suivante(s) :</small>

- [:material-account-cash: Capitalisme de surveillance](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Voici les **navigateurs internet** et configurations actuellement recommandés pour la navigation standard/non-anonyme. Nous recommandons [Mullvad Browser](#mullvad-browser) si vous recherchez des protections solides de la vie privée et une protection contre la capture des empreintes numériques, [Firefox](#firefox) pour les internautes occasionnels qui recherchent une bonne alternative à Google Chrome, et [Brave](#brave) si vous avez besoin d'une compatibilité avec le navigateur Chromium.

Si vous avez besoin de naviguer anonymement sur Internet, vous devriez plutôt utiliser [Tor](tor.md). Nous faisons quelques recommandations de configuration sur cette page, mais tous les navigateurs autres que Tor Browser seront traçables par *quelqu'un* d'une manière ou d'une autre.

## Navigateur Mullvad

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

Le **navigateur Mullvad** est une version du [navigateur Tor](tor.md#tor-browser) avec les intégrations au réseau Tor supprimées. Il vise à fournir aux utilisateurs de VPN les technologies d'anti-capture d'empreintes numériques du Navigateur Tor, qui sont des protections clés contre la [:material-eye-outline: surveillance de masse](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. Il est développé par le projet Tor et distribué par [Mullvad](vpn.md#mullvad), et n'exige **pas** l'utilisation du VPN de Mullvad.

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Comme le [Navigateur Tor](tor.md), le Navigateur Mullvad est conçu pour empêcher la capture d'empreintes numériques en rendant l'empreinte numérique de votre navigateur identique à celle de tous les autres utilisateurs du Navigateur Mullvad, et il inclut des paramètres par défaut et des extensions qui sont automatiquement configurés par les niveaux de sécurité par défaut : *Standard*, *Safer* et *Safest*. Il est donc impératif de ne pas modifier le navigateur mis à part l'ajustement des [niveaux de sécurité](https://tb-manual.torproject.org/security-settings) par défaut. D'autres modifications rendraient votre empreinte numérique unique, ce qui irait à l'encontre de l'objectif poursuivi par l'utilisation de ce navigateur. Si vous souhaitez configurer votre navigateur de manière plus poussée et que la capture d'empreintes numériques ne vous préoccupe pas, nous vous recommandons plutôt [Firefox](#firefox).

### Système anti-capture d'empreintes numériques

**Sans** utiliser un [VPN](vpn.md), le Navigateur Mullvad offre les mêmes protections contre [les scripts de capture d'empreintes numériques naïfs](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) que d'autres navigateurs privés comme Firefox+[Arkenfox](#arkenfox-advanced) ou [Brave](#brave). Le Navigateur Mullvad fournit ces protections dès le départ, au détriment d'une certaine flexibilité et d'une commodité que d'autres navigateurs privés peuvent offrir.

==Pour une protection anti-capture d'empreintes numériques optimale, nous recommandons d'utiliser le Navigateur Mullvad en conjonction **avec** un VPN==, qu'il s'agisse de Mullvad ou d'un autre fournisseur de VPN recommandé. Lorsque vous utilisez un VPN avec le Navigateur Mullvad, vous partagez une empreinte numérique et un ensemble d'adresses IP avec de nombreux autres utilisateurs, ce qui vous permet de vous fondre dans la "foule". Cette stratégie est le seul moyen de contrecarrer les scripts de pistage avancés, et c'est la même technique anti-capture d'empreintes numériques utilisée par le Navigateur Tor.

Notez que si vous pouvez utiliser le Navigateur Mullvad avec n'importe quel fournisseur de VPN, d'autres personnes sur ce VPN doivent également utiliser le Navigateur Mullvad pour que cette "foule" existe, ce qui est plus probable sur le VPN Mullvad par rapport à d'autres fournisseurs, en particulier si peu de temps après le lancement du Navigateur Mullvad. Le Navigateur Mullvad ne dispose pas d'une connectivité VPN intégrée et ne vérifie pas non plus si vous utilisez un VPN avant de naviguer ; votre connexion VPN doit être configurée et gérée séparément.

Le Navigateur Mullvad est livré avec les extensions *uBlock Origin* et *NoScript* préinstallées. Bien que nous découragions généralement l'ajout d'[extensions de navigateur](browser-extensions.md), celles qui sont préinstallées avec le navigateur **ne** doivent **pas** être supprimées ou configurées en dehors de leurs valeurs par défaut, car cela rendrait votre empreinte numérique distincte de celle des autres utilisateurs du navigateur Mullvad. Il est également préinstallé avec l'extension de navigateur Mullvad, qui *peut* être supprimée en toute sécurité sans impact sur l'empreinte numérique de votre navigateur si vous le souhaitez, mais qui peut également être conservée en toute sécurité même si vous n'utilisez pas le VPN Mullvad.

### Mode de navigation privée

Le Navigateur Mullvad fonctionne en mode de navigation privée permanente, ce qui signifie que votre historique, vos cookies et autres données de site seront toujours effacés à chaque fois que le navigateur est fermé. Vos signets, vos paramètres de navigation et vos paramètres d'extension seront conservés.

Ceci est nécessaire pour empêcher les formes avancées de pistage, mais se fait au détriment de la commodité et de certaines fonctionnalités de Firefox, telles que les conteneurs multi-comptes. Rappelez-vous que vous pouvez toujours utiliser plusieurs navigateurs. Par exemple, vous pouvez envisager d'utiliser Firefox+Arkenfox pour quelques sites sur lesquels vous souhaitez rester connecté ou qui ne fonctionnent pas correctement dans le Navigateur Mullvad, et le Navigateur Mullvad pour la navigation générale.

### Mullvad Leta

Mullvad Browser comes with [**Mullvad Leta**](https://leta.mullvad.net) as the default search engine, which functions as a proxy to either Google or Brave search results (configurable on the Mullvad Leta homepage).

Si vous êtes un utilisateur de Mullvad VPN, il y a un certain risque à utiliser des services comme Mullvad Leta qui sont offerts par votre fournisseur VPN lui-même. Ceci est dû au fait que Mullvad a théoriquement accès à votre véritable adresse IP (via leur VPN) et à votre activité de recherche (via Leta), alors qu'un VPN est généralement censé séparer l'IP de votre activité de recherche. Même si Mullvad collecte très peu d'informations sur ses utilisateurs de son VPN ou ses utilisateurs de Leta, vous devriez envisager un autre moteur de recherche [](search-engines.md) si ce risque vous inquiète.

## Firefox

<div class="admonition recommendation" markdown>

![Logo Firefox](assets/img/browsers/firefox.svg){ align=right }

**Firefox** offre de solides paramètres de confidentialité, tels que la [protection renforcée contre le suivi](https://support.mozilla.org/fr/kb/protection-renforcee-contre-pistage-firefox-ordinateur), qui peut contribuer à bloquer divers [types de suivi](https://support.mozilla.org/fr/kb/protection-renforcee-contre-pistage-firefox-ordinateur#w_what-enhanced-tracking-protection-blocks).

[:octicons-home-16: Accueil](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.mozilla.org/fr/privacy/firefox/){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://support.mozilla.org/fr/products/firefox){ .card-link title="Documentation" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Code Source" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Firefox inclut un [jeton de téléchargement](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) unique dans les téléchargements fais à partir du site web de Mozilla et utilise la télémétrie dans Firefox pour envoyer le jeton. Ce jeton n'est **pas** inclus dans les versions du [serveur FTP de Mozilla](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Configuration recommandée pour Firefox

These options can be found in :material-menu: → **Settings**.

#### Recherche

- [ ] Décochez **Afficher les suggestions de recherche**

Search suggestion features may not be available in your region.

Search suggestions send everything you type in the address bar to the default search engine, regardless of whether you submit an actual search. Disabling search suggestions allows you to more precisely control what data you send to your search engine provider.

##### Suggestions Firefox (États-Unis uniquement)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. We recommend disabling it for the same reason we recommend disabling search suggestions. If you don't see these options under the **Address Bar** header, you do not have the new experience and can ignore these changes.

- [ ] Décochez **Suggestions de Firefox**
- [ ] Décochez **Suggestions des sponsors**

#### Confidentialité & sécurité

##### Protection renforcée contre le pistage

- [x] Sélectionnez **Stricte** Protection renforcée contre le pistage

This protects you by blocking social media trackers, fingerprinting scripts (note that this does not protect you from *all* fingerprinting), cryptominers, cross-site tracking cookies, and some other tracking content. ETP protects against many common threats, but it does not block all tracking avenues because it is designed to have minimal to no impact on site usability.

##### Supprimer à la fermeture

If you want to stay logged in to particular sites, you can allow exceptions in **Cookies and Site Data** → **Manage Exceptions...**

- [x] Cochez **Supprimer les cookies et les données du site lorsque Firefox est fermé**

This protects you from persistent cookies, but does not protect you against cookies acquired during any one browsing session. When this is enabled, it becomes possible to easily cleanse your browser cookies by simply restarting Firefox. You can set exceptions on a per-site basis, if you wish to stay logged in to a particular site you visit often.

##### Telemetry

- [ ] Décochez **Autoriser Firefox à envoyer des données techniques et d'interaction à Mozilla**
- [ ] Décochez **Autoriser Firefox à installer et à exécuter des études**
- [ ] Décochez **Permettre à Firefox d'envoyer en votre nom les rapports de plantage**

According to Mozilla's privacy policy for Firefox,

> Firefox nous envoie des données sur la version et la langue de votre Firefox ; le système d'exploitation de l'appareil et la configuration matérielle ; la mémoire, les informations de base sur les plantages et les erreurs; les résultats de processus automatisés tels que les mises à jour, la navigation sécurisée et l'activation de notre système. Lorsque Firefox nous envoie des données, votre adresse IP est temporairement collectée dans les journaux de notre serveur.

Additionally, the Mozilla Accounts service collects [some technical data](https://mozilla.org/privacy/mozilla-accounts). If you use a Mozilla Account you can opt out:

1. Ouvrez les [paramètres de votre profil sur accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Décochez **Collecte et utilisation de données** > **Aidez à améliorer les comptes Firefox**

##### Préférences publicitaires des sites web

- [ ] Décocher **Autoriser les sites web à effectuer des mesures publicitaires en respectant la vie privée**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.

##### Mode HTTPS uniquement

- [x] Sélectionnez **Activer le mode HTTPS uniquement dans toutes les fenêtres**

This prevents you from unintentionally connecting to a website in plain-text HTTP. Sites without HTTPS are uncommon nowadays, so this should have little to no impact on your day-to-day browsing.

##### DNS sur HTTPS

If you use a [DNS over HTTPS provider](dns.md):

- [x] Sélectionnez **Protection maximale** et choisissez un fournisseur approprié

Max Protection enforces the use of DNS over HTTPS, and a security warning will show if Firefox can’t connect to your secure DNS resolver, or if your secure DNS resolver says that records for the domain you are trying to access do not exist. This stops the network you're connected to from secretly downgrading your DNS security.

#### Synchronisation

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (avancé)

<div class="admonition tip" markdown>
<p class="admonition-title">Utilisez le Navigateur Mullvad pour une protection avancée contre les empreintes numérique</p>

Le [Navigateur Mullvad](#mullvad-browser) offre les mêmes protections contre la prise d'empreintes numérique qu'Arkenfox, et ne nécessite pas l'utilisation du VPN de Mullvad pour bénéficier de ces protections. Couplé à un VPN, le Navigateur Mullvad peut déjouer des scripts de pistage plus avancés qu'Arkenfox ne peut le faire. Arkenfox présente toujours l'avantage d'être beaucoup plus flexible et de permettre des exceptions par site pour les sites web auxquels vous devez rester connecté.

</div>

The [Arkenfox project](https://github.com/arkenfox/user.js) provides a set of carefully considered options for Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly—which you can [easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. We **strongly recommend** reading through their full [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember that you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

## Brave

<div class="admonition recommendation annotate" markdown>

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

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Brave ajoute un "[code d'affiliation](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" au nom du fichier dans les téléchargements à partir du site Web de Brave, qui est utilisé pour suivre la source à partir de laquelle le navigateur a été téléchargé, par exemple `BRV002` dans un téléchargement nommé `Brave-Browser-BRV002.pkg`. Le programme d'installation enverra un ping au serveur de Brave avec le code d'affiliation à la fin du processus d'installation. Si cela vous inquiète, vous pouvez renommer le fichier d'installation avant de l'ouvrir.

</div>

### Configuration recommandée pour Brave

These options can be found in :material-menu: → **Settings**.

#### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

Les options "Boucliers" peuvent être réduites par site selon les besoins, mais par défaut, nous recommandons de définir les paramètres suivants:

<div class="annotate" markdown>

- [x] Select **Aggressive** under *Trackers & ads blocking*

<details class="warning" markdown>
<summary>Utiliser les listes de filtres par défaut</summary>

Brave vous permet de sélectionner des filtres de contenu supplémentaires dans la page interne `brave://adblock`. Nous vous déconseillons d'utiliser cette fonctionnalité ; conservez plutôt les listes de filtres par défaut. L'utilisation de listes supplémentaires vous distinguera des autres utilisateurs de Brave et peut également augmenter la surface d'attaque s'il y a une faille dans Brave et qu'une règle malveillante est ajoutée à l'une des listes que vous utilisez.

</details>

- [x] Select **Strict** under *Upgrade connections to HTTPS*
- [x] (Optional) Select **Block Scripts** (1)
- [x] Check **Block fingerprinting**
- [x] Select **Block third-party cookies**
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option disables JavaScript, which will break a lot of sites. To fix them, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

#### Privacy and security

<div class="annotate" markdown>



</div>

1. Disabling the V8 optimizer reduces your attack surface by disabling [*some*](https://grapheneos.social/@GrapheneOS/112708049232710156) parts of JavaScript Just-In-Time (JIT) compilation.

##### Tor windows

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) allows you to route your traffic through the Tor network in Private Windows and access .onion services, which may be useful in some cases. However, Brave is **not** as resistant to fingerprinting as the Tor Browser is, and far fewer people use Brave with Tor, so you will stand out. If your threat model requires strong anonymity, use the [Tor Browser](tor.md#tor-browser).

##### Data Collection

- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**

#### Web3

Brave's Web3 features can potentially add to your browser fingerprint and attack surface. Unless you use any of these features, they should be disabled.

- Select **Extensions (no fallback)** under *Default Ethereum wallet*
- Select **Extensions (no fallback)** under *Default Solana wallet*

#### Extensions

- [ ] Uncheck all built-in extensions you don't use

#### Search engine

We recommend disabling search suggestions in Brave for the same reason we recommend disabling this feature in [Firefox](#search).

- [ ] Décochez **Afficher les suggestions de recherche**

#### Système

<div class="annotate" markdown>

- [ ] Décochez **Continuer l'exécution des applications lorsque Brave est fermé** pour désactiver les applications en arrière-plan (1)

</div>

1. Cette option n'est pas présente sur toutes les plateformes.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Doit être un logiciel open source.
- Doit prendre en charge les mises à jour automatiques.
- Doit recevoir les mises à jour du moteur dans un délai de 0 à 1 jour à compter de la publication en amont.
- Doit être disponible sur Linux, macOS et Windows.
- Les modifications nécessaires pour rendre le navigateur plus respectueux de la vie privée ne devraient pas avoir d'impact négatif sur l'expérience des utilisateurs.
- Bloque les cookies tiers par défaut.
- Must support [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### Dans le meilleur des cas

Nos critères de cas idéal représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de cette fonctionnalité, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Doit inclure une fonctionnalité intégrée de blocage du contenu.
- Supporte la compartimentation des cookies (à la [Account Containers](https://support.mozilla.org/kb/containers)).
- Should support Progressive Web Apps (PWAs). Les PWAs vous permettent d'installer certains sites web comme s'il s'agissait d'applications natives sur votre ordinateur. This can have advantages over installing Electron-based apps because PWAs benefit from your browser's regular security updates.
- Ne comprend pas de fonctionnalités supplémentaires (bloatwares) qui n'ont pas d'incidence sur la vie privée des utilisateurs.
- Ne devrait pas collecter de télémétrie par défaut.
- Devrait fournir une implémentation de serveur de synchronisation open-source.
- Le moteur de recherche par défaut est un [moteur de recherche privé](search-engines.md).

[^1]: L'implémentation de Brave est détaillée sur le site [Brave Privacy Updates : Partitionnement de l'état du réseau pour la protection de la vie privée](https://brave.com/privacy-updates/14-partitioning-network-state).
