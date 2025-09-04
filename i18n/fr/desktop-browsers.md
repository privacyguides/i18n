---
meta_title: "Navigateurs web respectueux de la vie privée pour PC et Mac - Privacy Guides"
title: Navigateurs de Bureau
icon: material/laptop
description: Ces navigateurs respectueux de la vie privée sont ceux que nous recommandons actuellement pour la navigation internet standard/non-anonyme sur les ordinateurs de bureau.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Recommandations de Navigateurs de Bureau Privés
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

Voici les **navigateurs internet** et configurations actuellement recommandés pour la navigation standard/non-anonyme. Nous recommandons le [Navigateur Mullvad](#mullvad-browser) si vous recherchez des protections solides de la vie privée et une protection contre la capture des empreintes numériques, [Firefox](#firefox) pour les internautes occasionnels qui recherchent une bonne alternative à Google Chrome, et [Brave](#brave) si vous avez besoin d'une compatibilité avec le navigateur Chromium.

Si vous avez besoin de naviguer anonymement sur Internet, vous devriez plutôt utiliser [Tor](tor.md). Nous faisons quelques recommandations de configuration sur cette page, mais tous les navigateurs autres que Tor Browser seront traçables par *quelqu'un* d'une manière ou d'une autre.

## Navigateur Mullvad

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

Le **navigateur Mullvad** est une version de [navigateur Tor](tor.md#tor-browser) avec les intégrations au réseau Tor supprimées. Il vise à fournir aux utilisateurs de VPN les technologies d'anti-capture d'empreintes numériques du Navigateur Tor, qui sont des protections clés contre la [:material-eye-outline: surveillance de masse](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. Il est développé par le projet Tor et distribué par [Mullvad](vpn.md#mullvad), et n'exige **pas** l'utilisation du VPN de Mullvad.

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title= "Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

A l'instar du [Navigateur Tor](tor.md), le Navigateur Mullvad est conçu pour empêcher la capture d'empreintes numériques (le "fingerprinting") en rendant l'empreinte numérique de votre navigateur identique à celle de tous les autres utilisateurs du Navigateur Mullvad, et il inclut des paramètres par défaut et des extensions qui sont automatiquement configurés par les niveaux de sécurité du navigateur : *Normal*, *Plus sûr* et *Le plus sûr*.

Il est donc impératif de ne pas modifier le navigateur mis à part l'ajustement des [niveaux de sécurité](https://tb-manual.torproject.org/security-settings) par défaut. Lorsque vous réglez le niveau de sécurité, vous **devez** toujours redémarrer le navigateur avant de continuer à l'utiliser. Dans le cas contraire, [les paramètres de sécurité peuvent ne pas être entièrement appliqués](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), ce qui vous expose à un risque plus élevé de captures d'empreinte et de vulnérabilités que vous ne l'auriez imaginé sur la base des paramètres choisis.

Toute modification autre que le réglage de ce paramètre rendrait votre empreinte digitale unique, ce qui irait à l'encontre de l'objectif poursuivi par l'utilisation de ce navigateur. Si vous souhaitez configurer votre navigateur de manière plus poussée et que la capture d'empreintes numériques ne vous préoccupe pas, nous vous recommandons plutôt [Firefox](#firefox).

### Système anti-capture d'empreintes numériques

**Sans** utiliser un [VPN](vpn.md), le Navigateur Mullvad offre les mêmes protections contre [les scripts de capture d'empreintes numériques naïfs](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) que d'autres navigateurs privés comme Firefox+[Arkenfox](#arkenfox-advanced) ou [Brave](#brave). Le Navigateur Mullvad fournit ces protections dès le départ, au détriment d'une certaine flexibilité et d'une commodité que d'autres navigateurs privés peuvent offrir.

==Pour une protection anti-capture d'empreintes numériques optimale, nous recommandons d'utiliser le Navigateur Mullvad en conjonction **avec** un VPN==, qu'il s'agisse de Mullvad ou d'un autre fournisseur de VPN recommandé. Lorsque vous utilisez un VPN avec le Navigateur Mullvad, vous partagez une empreinte numérique et un ensemble d'adresses IP avec de nombreux autres utilisateurs, ce qui vous permet de vous fondre dans la "foule". Cette stratégie est le seul moyen de contrecarrer les scripts de pistage avancés, et c'est la même technique anti-capture d'empreintes numériques utilisée par le Navigateur Tor.

Notez que si vous pouvez utiliser le Navigateur Mullvad avec n'importe quel fournisseur de VPN, d'autres personnes sur ce VPN doivent également utiliser le Navigateur Mullvad pour que cette "foule" existe, ce qui est plus probable sur le VPN Mullvad par rapport à d'autres fournisseurs, en particulier si peu de temps après le lancement du Navigateur Mullvad. Le Navigateur Mullvad ne dispose pas d'une connectivité VPN intégrée et ne vérifie pas non plus si vous utilisez un VPN avant de naviguer ; votre connexion VPN doit être configurée et gérée séparément.

Le Navigateur Mullvad est livré avec les extensions *uBlock Origin* et *NoScript* préinstallées. Bien que nous découragions généralement l'ajout d'[extensions de navigateur](browser-extensions.md), celles qui sont préinstallées avec le navigateur **ne** doivent **pas** être supprimées ou configurées en dehors de leurs valeurs par défaut, car cela rendrait votre empreinte numérique distincte de celle des autres utilisateurs du navigateur Mullvad. Il est également préinstallé avec l'extension de navigateur Mullvad, qui *peut* être supprimée en toute sécurité sans impact sur l'empreinte numérique de votre navigateur si vous le souhaitez, mais qui peut également être conservée en toute sécurité même si vous n'utilisez pas le VPN Mullvad.

### Mode de navigation privée

Le Navigateur Mullvad fonctionne en mode de navigation privée permanente, ce qui signifie que votre historique, vos cookies et autres données de site seront toujours effacés à chaque fois que le navigateur est fermé. Vos signets, vos paramètres de navigation et vos paramètres d'extension seront conservés.

Ceci est nécessaire pour empêcher les formes avancées de pistage, mais se fait au détriment de la commodité et de certaines fonctionnalités de Firefox, telles que les conteneurs multi-comptes. Rappelez-vous que vous pouvez toujours utiliser plusieurs navigateurs. Par exemple, vous pouvez envisager d'utiliser Firefox+Arkenfox pour quelques sites sur lesquels vous souhaitez rester connecté ou qui ne fonctionnent pas correctement dans le Navigateur Mullvad, et le Navigateur Mullvad pour la navigation générale.

### Mullvad Leta

Le navigateur Mullvad est livré avec [**Mullvad Leta**](search-engines.md#mullvad-leta) comme moteur de recherche par défaut, qui fonctionne comme un proxy vers les résultats de recherche de Google ou de Brave (configurable sur la page d'accueil de Mullvad Leta).

Si vous êtes un utilisateur de Mullvad VPN, il y a un certain risque à utiliser des services comme Mullvad Leta qui sont offerts par votre fournisseur VPN lui-même. Ceci est dû au fait que Mullvad a théoriquement accès à votre véritable adresse IP (via leur VPN) et à votre activité de recherche (via Leta), cette dernière étant une information qu'un VPN est généralement censé séparer. Même si Mullvad collecte très peu d'informations sur ses utilisateurs de son VPN ou ses utilisateurs de Leta, vous devriez envisager un autre moteur de recherche [](search-engines.md) si ce risque vous inquiète.

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
<summary>Téléchargements</summary>

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

Ces options sont disponibles sur :material-menu: → **Paramètres**.

#### Recherche

- [ ] Décochez **Afficher les suggestions de recherche**

Les fonctionnalités de suggestion de recherche peuvent ne pas être disponibles dans votre région.

Les suggestions de recherche envoient tout ce que vous tapez dans la barre d'adresse au moteur de recherche par défaut, que vous lanciez ou non une recherche. La désactivation des suggestions de recherche vous permet de contrôler plus précisément les données que vous envoyez à votre fournisseur de moteur de recherche.

##### Suggestions Firefox (États-Unis uniquement)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) est une fonction similaire aux suggestions de recherche qui n'est disponible qu'aux États-Unis. Nous recommandons de les désactiver pour la même raison que nous recommandons de désactiver les suggestions de recherche. Si vous ne voyez pas ces options dans l'en-tête de la **barre d'adresse**, c'est que vous n'avez pas la nouvelle expérience et que vous pouvez ignorer ces changements.

- [ ] Décochez **Suggestions de Firefox**
- [ ] Décochez **Suggestions des sponsors**

#### Confidentialité & sécurité

##### Protection renforcée contre le pistage

- [x] Sélectionnez **Stricte** Protection renforcée contre le pistage

Cela vous protège en bloquant les traceurs de réseaux sociaux, les scripts de capture d'empreinte (notez que cela ne vous protège pas de *toutes* les captures d'empreinte), les cryptomineurs, les cookies de suivi intersites et certains autres contenus de suivi. La PRP protège de nombreuses menaces courantes, mais ne bloque pas tous les moyens de suivi, car il est conçu pour avoir un impact minimal, voire nul, sur l'utilisation du site.

##### Supprimer à la fermeture

Si vous voulez rester connecté à des sites en particulier, vous pouvez autoriser des exceptions dans **Cookies et données de site** → **Gérer les exceptions....**

- [x] Cochez **Supprimer les cookies et les données du site lorsque Firefox est fermé**

Cela vous protège contre les cookies persistants, mais ne vous protège pas contre les cookies acquis au cours d'une même session de navigation. Lorsque cette option est activée, il devient possible de nettoyer facilement les cookies de votre navigateur en redémarrant simplement Firefox. Vous pouvez définir des exceptions par site, si vous souhaitez rester connecté à un site précis que vous visitez souvent.

##### Télémétrie

- [ ] Décochez **Autoriser Firefox à envoyer des données techniques et d'interaction à Mozilla**
- [ ] Décochez **Autoriser Firefox à installer et à exécuter des études**
- [ ] Décochez **Permettre à Firefox d'envoyer en votre nom les rapports de plantage**

Selon la politique de confidentialité de Mozilla pour Firefox,

> Firefox nous envoie des données sur la version et la langue de votre Firefox ; le système d'exploitation de l'appareil et la configuration matérielle ; la mémoire, les informations de base sur les plantages et les erreurs; les résultats de processus automatisés tels que les mises à jour, la navigation sécurisée et l'activation de notre système. Lorsque Firefox nous envoie des données, votre adresse IP est temporairement collectée dans les journaux de notre serveur.

De plus, le service Mozilla Accounts collecte [certaines données techniques](https://mozilla.org/privacy/mozilla-accounts). Si vous utilisez un compte Mozilla, vous pouvez le refuser :

1. Ouvrez les [paramètres de votre profil sur accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Décochez **Collecte et utilisation de données** > **Aidez à améliorer les comptes Firefox**

##### Préférences publicitaires des sites web

- [ ] Décocher **Autoriser les sites web à effectuer des mesures publicitaires en respectant la vie privée**

Avec la sortie de Firefox 128, un nouveau paramètre pour l'[attribution respectueuse de la vie privée](https://support.mozilla.org/kb/privacy-preserving-attribution) (privacy-preserving attribution, PPA) a été ajouté et est [activé par défaut](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). La PPA permet aux annonceurs d'utiliser votre navigateur web pour mesurer l'efficacité des campagnes web, au lieu d'utiliser un suivi traditionnel basé sur JavaScript. Nous considérons que ce comportement n'entre pas dans le cadre des responsabilités d'un agent utilisateur, et le fait qu'il soit désactivé par défaut dans Arkenfox est un indicateur supplémentaire en faveur de la désactivation de cette fonctionnalité.

##### Mode HTTPS uniquement

- [x] Sélectionnez **Activer le mode HTTPS uniquement dans toutes les fenêtres**

Cela vous empêche de vous connecter involontairement à un site Web en "clair" HTTP. Les sites sans HTTPS sont rares de nos jours. Cela ne devrait donc avoir que peu ou pas d'impact sur votre navigation quotidienne.

##### DNS sur HTTPS

Si vous utilisez un [fournisseur de DNS via HTTPS](dns.md) :

- [x] Sélectionnez **Protection maximale** et choisissez un fournisseur approprié

Protection maximale impose l'utilisation de DNS via HTTPS, et un avertissement de sécurité s'affichera si Firefox ne peut pas se connecter à votre résolveur DNS sécurisé, ou si votre résolveur DNS sécurisé indique que les enregistrements pour le domaine auquel vous essayez d'accéder n'existent pas. Cela empêche le réseau auquel vous êtes connecté de dégrader secrètement votre sécurité DNS.

#### Synchronisation

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) permet à vos données de navigation (historique, signets, etc.) d'être accessibles sur tous vos appareils et les protège avec du chiffrement de bout en bout.

### Arkenfox (avancé)

<div class="admonition tip" markdown>
<p class="admonition-title">Utilisez le Navigateur Mullvad pour une protection avancée contre les empreintes numérique</p>

Le [Navigateur Mullvad](#mullvad-browser) offre les mêmes protections contre la prise d'empreintes numérique qu'Arkenfox, et ne nécessite pas l'utilisation du VPN de Mullvad pour bénéficier de ces protections. Couplé à un VPN, le Navigateur Mullvad peut déjouer des scripts de pistage plus avancés qu'Arkenfox ne peut le faire. Arkenfox présente toujours l'avantage d'être beaucoup plus flexible et de permettre des exceptions par site pour les sites web auxquels vous devez rester connecté.

</div>

Le [projet Arkenfox](https://github.com/arkenfox/user.js) propose un ensemble d'options soigneusement étudiées pour Firefox. Si vous [décidez](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) d'utiliser Arkenfox, quelques [options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) sont subjectivement strictes et/ou peuvent empêcher certains sites web de fonctionner correctement. Vous pouvez [facilement les modifier](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) pour les adapter à vos besoins. Nous vous **recommandons vivement** de lire l'intégralité de leur [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox permet également la prise en charge des [conteneurs](https://support.mozilla.org/kb/containers#w_for-advanced-users).

Arkenfox vise uniquement à contrecarrer les scripts de pistage basiques ou naïfs grâce aux paramètres de configuration de randomisation du canevas et de la résistance aux empreintes numérique intégrée à Firefox. Il ne vise pas à faire en sorte que votre navigateur se fonde dans une foule d'autres utilisateurs d'Arkenfox, comme le font le Navigateur Mullvad ou le Navigateur Tor, ce qui est le seul moyen de contrecarrer les scripts avancés de pistage des empreintes numérique. Pour rappel, vous pouvez toujours utiliser plusieurs navigateurs internet. Par exemple, vous pourriez utiliser Firefox+Arkenfox pour les sites sur lesquels vous voudriez rester connecté ou en lesquels vous avez confiance, et utiliser Mullvad Browser pour la navigation standard.

## Brave

<div class="admonition recommendation annotate" markdown>

![Logo Brave](assets/img/browsers/brave.svg){ align=right }

Le navigateur **Brave** comprend un bloqueur de contenu intégré et des [fonctions de confidentialité](https://brave.com/privacy-features/), dont la plupart sont activées par défaut.

Brave est basé sur le projet de navigateur Web Chromium. Il devrait donc vous être familier et présenter un minimum de problèmes de compatibilité avec les sites Web.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

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

Ces options sont disponibles sur :material-menu: → **Paramètres**.

#### Boucliers (Shields)

Brave inclut des mesures anti-empreintes digitales dans sa fonctionnalité [Boucliers (Shields)](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Nous vous conseillons de configurer ces options de [manière globale](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) sur toutes les pages que vous visitez.

Les options "Boucliers" peuvent être réduites par site selon les besoins, mais par défaut, nous recommandons de définir les paramètres suivants:

<div class="annotate" markdown>

- [x] Sélectionnez **Agressif** dans *Blocage des traceurs et des publicités*.

<details class="warning" markdown>
<summary>Utiliser les listes de filtres par défaut</summary>

Brave vous permet de sélectionner des filtres de contenu supplémentaires dans la page interne `brave://adblock`. Nous vous déconseillons d'utiliser cette fonctionnalité ; conservez plutôt les listes de filtres par défaut. L'utilisation de listes supplémentaires vous distinguera des autres utilisateurs de Brave et peut également augmenter la surface d'attaque s'il y a une faille dans Brave et qu'une règle malveillante est ajoutée à l'une des listes que vous utilisez.

</details>

- [x] Sélectionnez **Strict** sous *Mettre les connexions à HTTPS*
- [x] (Facultatif) Sélectionnez **Bloquer les scripts** (1)
- [x] Cochez **Bloquer les empreintes digitales**
- [x] Sélectionnez **Bloquer les cookies tiers**
- [x] Cochez **M'oublier quand je ferme ce site** (2)
- [ ] Décochez tous les composants de médias sociaux.

</div>

1. Cette option désactive JavaScript, ce qui rendra inutilisable beaucoup de sites. Pour y remédier, vous pouvez définir des exceptions par site en cliquant sur l'icône du bouclier dans la barre d'adresse et en décochant ce paramètre dans la section *Contrôles avancés.*
2. Si vous souhaitez rester connecté à un site particulier que vous visitez souvent, vous pouvez définir des exceptions pour chaque site en cliquant sur l'icône du bouclier dans la barre d'adresse et en décochant ce paramètre sous *Contrôles avancés*.

#### Vie privée et sécurité

<div class="annotate" markdown>



</div>

1. La désactivation de l'optimiseur V8 réduit votre surface d'attaque en désactivant [*certaines*](https://grapheneos.social/@GrapheneOS/112708049232710156) parties de la compilation Just-In-Time (JIT) de JavaScript.

##### Fenêtres Tor

[**Fenêtre privée avec Tor (Private Window with Tor)**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) vous permet d'acheminer votre trafic via le réseau Tor dans les fenêtres privées et d'accéder aux services .onion, ce qui peut s'avérer utile dans certains cas. Cependant, Brave **n'est pas** aussi résistant aux empreintes digitales que le navigateur Tor, et beaucoup moins de personnes utilisent Brave avec Tor. Si votre modèle de menace exige un fort anonymat, utilisez le [navigateur Tor.](tor.md#tor-browser)

##### Collecte de données

- [ ] Décochez **Autoriser l'analyse de produits respectueuse de la vie privée (P3A)**
- [ ] Décochez **Envoyer automatiquement un signal d'utilisation quotidienne à Brave**
- [Décocher l'**option Envoyer automatiquement les rapports de diagnostic**

#### Web3

Les fonctionnalités Web3 de Brave peuvent potentiellement ajouter à l'empreinte numérique de votre navigateur et à la surface d'attaque. À moins que vous n'utilisiez l'une de ces fonctions, elles devraient être désactivées.

- Sélectionnez **Extensions (no fallback)** sous *Portefeuille Ethereum par défaut*
- Sélectionnez **Extensions (no fallback)** sous *Default Solana wallet (portefeuille Solana par défaut)*

#### Extensions

- [ ] Décochez toutes les extensions intégrées que vous n'utilisez pas

#### Moteur de recherche

Nous recommandons de désactiver les suggestions de recherche dans Brave pour la même raison que nous recommandons de désactiver cette fonctionnalité dans [Firefox](#search).

- [ ] Décochez **Afficher les suggestions de recherche**

#### Système

<div class="annotate" markdown>

- Décocher **Continuer l'exécution des applications en arrière-plan lorsque Brave est fermé** pour désactiver les applications en arrière-plan (1)

</div>

1. Cette option n'est pas présente sur toutes les plateformes.

#### Synchronisation Brave (Brave Sync)

La [Synchronisation Brave](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) permet à vos données de navigation (historique, favoris, etc.) d'être accessibles sur tous vos appareils sans nécessiter de compte et les protège avec E2EE.

#### Récompenses (Brave Rewards) et portefeuille Brave (Wallet)

**Brave Rewards** vous permet de recevoir de la crypto-monnaie Basic Attention Token (BAT) en effectuant certaines actions au sein de Brave. Elles s'appuient sur un compte dépositaire et sur la KYC d'un certain nombre de fournisseurs. Nous ne recommandons pas le BAT en tant que [crypto-monnaie privée](cryptocurrency.md), ni l'utilisation d'un [portefeuille de garde](advanced/payments.md#wallet-custody), et nous décourageons donc l'utilisation de cette fonctionnalité.

Le **Portefeuille Brave** fonctionne localement sur votre ordinateur, mais ne prend pas en charge les crypto-monnaies privées, nous vous déconseillons donc d'utiliser cette fonctionnalité.

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Doit être un logiciel open source.
- Doit prendre en charge les mises à jour automatiques.
- Doit recevoir les mises à jour du moteur dans un délai de 0 à 1 jour à compter de la publication en amont.
- Doit être disponible sur Linux, macOS et Windows.
- Les modifications nécessaires pour rendre le navigateur plus respectueux de la vie privée ne devraient pas avoir d'impact négatif sur l'expérience des utilisateurs.
- Bloque les cookies tiers par défaut.
- Doit prendre en charge le [partitionnement des états](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) afin d'atténuer le suivi intersites.[^1]

### Dans le meilleur des cas

Nos critères de cas idéal représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de cette fonctionnalité, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Doit inclure une fonctionnalité intégrée de blocage du contenu.
- Supporte la compartimentation des cookies (à la [Account Containers](https://support.mozilla.org/kb/containers)).
- Doit prendre en charge les applications Web progressives (PWA). Les PWAs vous permettent d'installer certains sites web comme s'il s'agissait d'applications natives sur votre ordinateur. Cela peut présenter des avantages par rapport à l'installation d'applications basées sur Electron, car vous bénéficiez des mises à jour de sécurité régulières de votre navigateur.
- Ne comprend pas de fonctionnalités supplémentaires (bloatwares) qui n'ont pas d'incidence sur la vie privée des utilisateurs.
- Ne devrait pas collecter de télémétrie par défaut.
- Devrait fournir une implémentation de serveur de synchronisation open-source.
- Le moteur de recherche par défaut est un [moteur de recherche privé](search-engines.md).

[^1]: L'implémentation de Brave est détaillée sur le site [Brave Privacy Updates : Partitionnement de l'état du réseau pour la protection de la vie privée](https://brave.com/privacy-updates/14-partitioning-network-state).
