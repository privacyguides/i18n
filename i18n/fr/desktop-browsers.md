---
meta_title: "Navigateurs web respectueux de la vie privée pour PC et Mac - Privacy Guides"
title: "Navigateurs de bureau"
icon: material/laptop
description: Ces navigateurs web offrent des protections de la vie privée plus solides que Google Chrome.
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

Ce sont les navigateurs web de bureau et les configurations que nous recommandons actuellement pour une navigation classique/non anonyme. Nous recommandons [Mullvad Browser](#mullvad-browser) si vous recherchez des protections solides de la vie privée et une protection contre les empreintes numériques, [Firefox](#firefox) pour les internautes occasionnels qui recherchent une bonne alternative à Google Chrome, et [Brave](#brave) si vous avez besoin d'une compatibilité avec le navigateur Chromium.

Si vous avez besoin de naviguer anonymement sur Internet, vous devriez plutôt utiliser [Tor](tor.md). Nous faisons quelques recommandations de configuration sur cette page, mais tous les navigateurs autres que Tor Browser seront traçables par *quelqu'un* d'une manière ou d'une autre.

## Navigateur Mullvad

!!! recommendation

    ![Logo du navigateur Mullvad](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    Le **Navigateur Mullvad** est une version du [Navigateur Tor](tor.md#tor-browser) dont l'intégration au réseau Tor a été supprimée, visant à fournir les technologies de protection contre les empreintes numériques du Navigateur Tor aux utilisateurs de VPN. Il est développé par le projet Tor et distribué par [Mullvad](vpn.md#mullvad), et n'exige **pas** l'utilisation du VPN de Mullvad.
    
    [:octicons-home-16: Page d'accueil](https://mullvad.net/en/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Politique de confidentialité" }
    [:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Code source" }
    
    ??? downloads "Téléchargements"
    
        - [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

Comme le [Navigateur Tor](tor.md), le Navigateur Mullvad est conçu pour empêcher la prise d'empreintes numériques en rendant l'empreinte numérique de votre navigateur identique à celle de tous les autres utilisateurs du Navigateur Mullvad, et il inclut des paramètres par défaut et des extensions qui sont automatiquement configurés par les niveaux de sécurité par défaut : *Standard*, *Safer* et *Safest*. Il est donc impératif de ne pas modifier le navigateur mis à part l'ajustement des [niveaux de sécurité](https://tb-manual.torproject.org/security-settings/) par défaut. D'autres modifications rendraient votre empreinte numérique unique, ce qui irait à l'encontre de l'objectif poursuivi par l'utilisation de ce navigateur. Si vous souhaitez configurer votre navigateur de manière plus poussée et que la prise d'empreintes numériques ne vous préoccupe pas, nous vous recommandons plutôt [Firefox](#firefox).

### Système anti-empreintes numériques

**Sans** utiliser un [VPN](vpn.md), le Navigateur Mullvad offre les mêmes protections contre [les scripts d'empreintes numériques naïfs](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) que d'autres navigateurs privés comme Firefox+[Arkenfox](#arkenfox-advanced) ou [Brave](#brave). Le Navigateur Mullvad fournit ces protections dès le départ, au détriment d'une certaine flexibilité et d'une commodité que d'autres navigateurs privés peuvent offrir.

==Pour une protection anti-empreintes numériques optimale, nous recommandons d'utiliser le Navigateur Mullvad en conjonction **avec** un VPN==, qu'il s'agisse de Mullvad ou d'un autre fournisseur de VPN recommandé. Lorsque vous utilisez un VPN avec le Navigateur Mullvad, vous partagez une empreinte numérique et un ensemble d'adresses IP avec de nombreux autres utilisateurs, ce qui vous permet de vous fondre dans la "foule". Cette stratégie est le seul moyen de contrecarrer les scripts de pistage avancés, et c'est la même technique anti-empreintes numériques utilisée par le Navigateur Tor.

Notez que si vous pouvez utiliser le Navigateur Mullvad avec n'importe quel fournisseur de VPN, d'autres personnes sur ce VPN doivent également utiliser le Navigateur Mullvad pour que cette "foule" existe, ce qui est plus probable sur le VPN Mullvad par rapport à d'autres fournisseurs, en particulier si peu de temps après le lancement du Navigateur Mullvad. Le Navigateur Mullvad ne dispose pas d'une connectivité VPN intégrée et ne vérifie pas non plus si vous utilisez un VPN avant de naviguer ; votre connexion VPN doit être configurée et gérée séparément.

Le Navigateur Mullvad est livré avec les extensions *uBlock Origin* et *NoScript* préinstallées. Bien que nous ne [recommandions généralement pas](#extensions) d'ajouter des extensions de navigateur *supplémentaires*, ces extensions préinstallées avec le navigateur ne doivent **pas** être supprimées ou configurées en dehors de leurs valeurs par défaut, car cela rendrait l'empreinte numérique de votre navigateur sensiblement différente de celle des autres utilisateurs du Navigateur Mullvad. Il est également préinstallé avec l'extension de navigateur Mullvad, qui *peut* être supprimée en toute sécurité sans impact sur l'empreinte numérique de votre navigateur si vous le souhaitez, mais qui peut également être conservée en toute sécurité même si vous n'utilisez pas le VPN Mullvad.

### Mode de navigation privée

Le Navigateur Mullvad fonctionne en mode de navigation privée permanente, ce qui signifie que votre historique, vos cookies et autres données de site seront toujours effacés à chaque fois que le navigateur est fermé. Vos signets, vos paramètres de navigation et vos paramètres d'extension seront conservés.

Ceci est nécessaire pour empêcher les formes avancées de pistage, mais se fait au détriment de la commodité et de certaines fonctionnalités de Firefox, telles que les conteneurs multi-comptes. Rappelez-vous que vous pouvez toujours utiliser plusieurs navigateurs. Par exemple, vous pouvez envisager d'utiliser Firefox+Arkenfox pour quelques sites sur lesquels vous souhaitez rester connecté ou qui ne fonctionnent pas correctement dans le Navigateur Mullvad, et le Navigateur Mullvad pour la navigation générale.

### Mullvad Leta

Le navigateur Mullvad est livré avec DuckDuckGo comme [moteur de recherche](search-engines.md) par défaut, mais il est également préinstallé avec **Mullvad Leta**, un moteur de recherche qui nécessite un abonnement VPN Mullvad actif pour y accéder. Mullvad Leta interroge directement l'API de recherche payante de Google (c'est pourquoi il est limité aux abonnés payants). Cependant, en raison de cette limitation, il est possible pour Mullvad d'établir une corrélation entre les requêtes de recherche et les comptes VPN Mullvad. C'est pourquoi nous déconseillons l'utilisation de Mullvad Leta, même si Mullvad recueille très peu d'informations sur ses abonnés VPN.

## Firefox

!!! recommendation

    ![Logo Firefox](assets/img/browsers/firefox.svg){ align=right }
    
    **Firefox** offre de solides paramètres de confidentialité, tels que la [protection renforcée contre le suivi](https://support.mozilla.org/fr/kb/protection-renforcee-contre-pistage-firefox-ordinateur), qui peut contribuer à bloquer divers [types de suivi](https://support.mozilla.org/fr/kb/protection-renforcee-contre-pistage-firefox-ordinateur#w_what-enhanced-tracking-protection-blocks).
    
    [:octicons-home-16: Accueil](https://firefox.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mozilla.org/fr/privacy/firefox/){ .card-link title="Politique de confidentialité" }
    [:octicons-info-16:](https://firefox-source-docs.mozilla.org/){ .card-link title="Documentation"}
    [:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Code source"}
    [:octicons-heart-16:](https://donate.mozilla.org/fr/){ .card-link title=Contribuer}
    
    ??? downloads "Téléchargements"
    
        - [:simple-windows11: Windows](https://www.mozilla.org/firefox/windows)
        - [:simple-apple: macOS](https://www.mozilla.org/firefox/mac)
        - [:simple-linux: Linux](https://www.mozilla.org/firefox/linux)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

!!! warning "Avertissement"
    Firefox inclut un [jeton de téléchargement](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) unique dans les téléchargements effectués à partir du site Web de Mozilla et utilise la télémétrie dans Firefox pour envoyer le jeton. Le jeton **n'est pas** inclus dans les versions de [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

### Configuration recommandée

Ces options se trouvent dans :material-menu: → **Paramètres**

#### Recherche

- [ ] Décochez **Fournir des suggestions de recherche**

Les fonctionnalités de suggestion de recherche peuvent ne pas être disponibles dans votre région.

Les suggestions de recherche envoient tout ce que vous tapez dans la barre d'adresse au moteur de recherche par défaut, que vous lanciez ou non une recherche. La désactivation des suggestions de recherche vous permet de contrôler plus précisément les données que vous envoyez à votre fournisseur de moteur de recherche.

#### Confidentialité & sécurité

##### Protection renforcée contre le pistage

- [x] Sélectionnez **Stricte** Protection renforcée contre le pistage

Cela vous protège en bloquant les traceurs de réseaux sociaux, les scripts de prise d'empreinte (notez que cela ne vous protège pas de *toutes* les prises d'empreinte), les cryptomineurs, les cookies de suivi intersites et certains autres contenus de suivi. La PRT protège de nombreuses menaces courantes, mais ne bloque pas tous les moyens de suivi, car il est conçu pour avoir un impact minimal, voire nul, sur l'utilisation du site.

##### Suggestions Firefox (États-Unis uniquement)

Les [Suggestions Firefox](https://support.mozilla.org/en-US/kb/firefox-suggest) sont une fonctionnalité similaire aux suggestions de recherche qui ne sont disponible qu'aux États-Unis. Nous recommandons de les désactiver pour la même raison que nous recommandons de désactiver les suggestions de recherche. Si vous ne voyez pas ces options dans l'en-tête de la **barre d'adresse**, c'est que vous n'avez pas la nouvelle expérience et que vous pouvez ignorer ces changements.

- [ ] Décochez **Suggestions du web**
- [ ] Décochez **Suggestions des sponsors**

##### Supprimer à la fermeture

Si vous voulez rester connecté à des sites en particulier, vous pouvez autoriser des exceptions dans **Cookies et données de site** → **Gérer les exceptions....**

- [x] Cochez **Supprimer les cookies et les données du site lorsque Firefox est fermé**

Cela vous protège contre les cookies persistants, mais ne vous protège pas contre les cookies acquis au cours d'une même session de navigation. Lorsque cette option est activée, il devient possible de nettoyer facilement les cookies de votre navigateur en redémarrant simplement Firefox. Vous pouvez définir des exceptions par site, si vous souhaitez rester connecté à un site précis que vous visitez souvent.

##### Télémétrie

- [ ] Décochez **Autoriser Firefox à envoyer des données techniques et d'interaction à Mozilla**
- [ ] Décochez **Autoriser Firefox à installer et à exécuter des études**
- [ ] Décochez **Permettre à Firefox d'envoyer en votre nom les rapports de plantage**

> Firefox nous envoie des données sur la version et la langue de votre Firefox ; le système d'exploitation de l'appareil et la configuration matérielle ; la mémoire, les informations de base sur les plantages et les erreurs; les résultats de processus automatisés tels que les mises à jour, la navigation sécurisée et l'activation de notre système. Lorsque Firefox nous envoie des données, votre adresse IP est temporairement collectée dans les journaux de notre serveur.

En outre, le service Firefox Accounts collecte [certaines données techniques](https://www.mozilla.org/en-US/privacy/firefox/#firefox-accounts). Si vous utilisez un compte Firefox, vous pouvez la refuser :

1. Ouvrez les [paramètres de votre profil sur accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Décochez **Collecte et utilisation de données** > **Aidez à améliorer les comptes Firefox**

##### Mode HTTPS uniquement

- [x] Sélectionnez **Activer le mode HTTPS uniquement dans toutes les fenêtres**

Cela vous empêche de vous connecter involontairement à un site Web en "clair" HTTP. Les sites sans HTTPS sont rares de nos jours. Cela ne devrait donc avoir que peu ou pas d'impact sur votre navigation quotidienne.

##### DNS via HTTPS

Si vous utilisez un [fournisseur de DNS via HTTPS](dns.md) :

- [x] Sélectionnez **Protection maximale** et choisissez un fournisseur approprié

Protection maximale impose l'utilisation de DNS via HTTPS, et un avertissement de sécurité s'affichera si Firefox ne peut pas se connecter à votre résolveur DNS sécurisé, ou si votre résolveur DNS sécurisé indique que les enregistrements pour le domaine auquel vous essayez d'accéder n'existent pas. Cela empêche le réseau auquel vous êtes connecté de dégrader secrètement votre sécurité DNS.

#### Synchronisation

La [Synchronisation Firefox](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) permet à vos données de navigation (historique, favoris, etc.) d'être accessibles sur tous vos appareils et les protège avec le chiffrement de bout en bout (E2EE).

### Arkenfox (avancé)

!!! tip "Utilisez le Navigateur Mullvad pour une protection avancée contre les empreintes numérique"

    Le [Navigateur Mullvad](#mullvad-browser) offre les mêmes protections contre la prise d'empreintes numérique qu'Arkenfox, et ne nécessite pas l'utilisation du VPN de Mullvad pour bénéficier de ces protections. Couplé à un VPN, le Navigateur Mullvad peut déjouer des scripts de pistage plus avancés qu'Arkenfox ne peut le faire. Arkenfox présente toujours l'avantage d'être beaucoup plus flexible et de permettre des exceptions par site pour les sites web auxquels vous devez rester connecté.

Le projet [Arkenfox](https://github.com/arkenfox/user.js) fournit un ensemble d'options soigneusement étudiées pour Firefox. Si vous [décidez](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) d'utiliser Arkenfox, [quelques options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) sont subjectivement strictes et/ou peuvent empêcher certains sites web de fonctionner correctement. [Vous pouvez facilement modifier ces options](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) pour répondre à vos besoins. Nous **recommandons vivement** de lire l'intégralité de leur [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox permet également la prise en charge des [conteneurs](https://support.mozilla.org/fr/kb/conteneurs#w_for-advanced-users).

Arkenfox vise uniquement à contrecarrer les scripts de pistage basiques ou naïfs grâce aux paramètres de configuration de randomisation du canevas et de la résistance aux empreintes numérique intégrée à Firefox. Il ne vise pas à faire en sorte que votre navigateur se fonde dans une foule d'autres utilisateurs d'Arkenfox, comme le font le Navigateur Mullvad ou le Navigateur Tor, ce qui est le seul moyen de contrecarrer les scripts avancés de pistage des empreintes numérique. Rappelez-vous que vous pouvez toujours utiliser plusieurs navigateurs. Par exemple, vous pouvez envisager d'utiliser Firefox+Arkenfox pour quelques sites sur lesquels vous souhaitez rester connecté ou auxquels vous faites confiance, et le Navigateur Mullvad pour la navigation générale.

## Brave

!!! recommendation

    ![Logo Brave](assets/img/browsers/brave.svg){ align=right }
    
    **Le navigateur Brave** comprend un bloqueur de contenu intégré et des [fonctions de confidentialité](https://brave.com/privacy-features/), dont la plupart sont activées par défaut.
    
    Brave est basé sur le projet de navigateur Web Chromium. Il devrait donc vous être familier et présenter un minimum de problèmes de compatibilité avec les sites Web.
    
    [:octicons-home-16: Page d'accueil](https://brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Service onion" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Politique de confidentialité" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Code source" }
    
    ??? downloads annotate "Téléchargements"
    
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
        - [:simple-windows11: Windows](https://brave.com/download/)
        - [:simple-apple: macOS](https://brave.com/download/)
        - [:simple-linux: Linux](https://brave.com/linux/) (1)

    1. Nous vous déconseillons d'utiliser la version Flatpak de Brave, car elle remplace la sandbox de Chromium par celle de Flatpak, qui est moins efficace. De plus, le paquet n'est pas maintenu par Brave Software, Inc.

**Utilisateurs de macOS :** Le téléchargement du navigateur Brave depuis leur site officiel est un programme d'installation `.pkg` qui nécessite des privilèges d'administrateur pour être exécuté (et peut exécuter d'autres scripts inutiles sur votre machine). Vous pouvez également télécharger le dernier fichier `Brave-Browser-universal.dmg` à partir de la page [releases sur GitHub](https://github.com/brave/brave-browser/releases/latest), qui permet une installation traditionnelle par "glisser vers le dossier Applications".

!!! warning "Avertissement"

    Brave ajoute un "[code d'affiliation](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" au nom du fichier dans les téléchargements à partir du site Web de Brave, qui est utilisé pour suivre la source à partir de laquelle le navigateur a été téléchargé, par exemple `BRV002` dans un téléchargement nommé `Brave-Browser-BRV002.pkg`. Le programme d'installation enverra un ping au serveur de Brave avec le code d'affiliation à la fin du processus d'installation. Si cela vous inquiète, vous pouvez renommer le fichier d'installation avant de l'ouvrir.

### Configuration recommandée

Ces options se trouvent dans :material-menu: → **Paramètres**.

#### Paramètres

##### Shields

Brave inclut certaines mesures contre la prise d'empreinte numérique dans sa fonction [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-). Nous vous suggérons de configurer ces options [de manière globale](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) sur toutes les pages que vous visitez.

Les options Shields peuvent être réduites par site selon les besoins, mais par défaut, nous recommandons de définir les paramètres suivants:

<div class="annotate" markdown>

- [x] Sélectionnez **Empêchez les sites de prendre mon empreinte numérique en fonction de mes préférences linguistiques**
- [x] Sélectionnez **Agressif** dans la rubrique Blocage des pisteurs et annonces

    ??? warning "Utiliser les listes de filtres par défaut"
        Brave vous permet de sélectionner des filtres de contenu supplémentaires dans la page interne `brave://adblock`. Nous vous déconseillons d'utiliser cette fonctionnalité ; conservez plutôt les listes de filtres par défaut. L'utilisation de listes supplémentaires vous distinguera des autres utilisateurs de Brave et peut également augmenter la surface d'attaque s'il y a une faille dans Brave et qu'une règle malveillante est ajoutée à l'une des listes que vous utilisez.

- [x] Sélectionnez **Strict** sous **Mise à niveau des connexions vers HTTPS**
- [x] (Facultatif) Sélectionnez **Bloquer les scripts** (1)
- [x] Sélectionnez **Strict, peut endommager les sites** sous Bloquer les empreintes digitales

</div>

1. Cette option fournit une fonctionnalité similaire aux [modes de blocage](https://github.com/gorhill/uBlock/wiki/Blocking-mode) avancés de uBlock Origin ou l'extension [NoScript](https://noscript.net/).

##### Blocage des médias sociaux

- [ ] Décochez toutes les fonctionnalités de médias sociaux

##### Confidentialité et sécurité

<div class="annotate" markdown>

- [x] Sélectionnez **Désactiver les UDP sans proxy** sous [WebRTC IP Handling Policy](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Décochez **Utiliser les services Google pour la messagerie push**
- [ ] Décochez **Autoriser les analyses de produits préservant la vie privée (P3A)**
- [ ] Décochez **Envoyer automatiquement un ping quotidien d'utilisation à Brave**
- [ ] Décochez **Envoyer automatiquement des rapports de diagnostic**
- [ ] Décochez **Fenêtre privée avec Tor** (1)

    !!! tip "Nettoyer à la fermeture"

        - [x] Sélectionnez **Effacer les cookies et les données du site lorsque vous fermez toutes les fenêtres** dans le menu *Cookies et autres données du site*

        Si vous souhaitez rester connecté à un site particulier que vous visitez souvent, vous pouvez définir des exceptions par site dans la section *Comportements personnalisés*.

</div>

1. Brave **n'est pas** aussi résistant à la prise d'empreinte numérique que le navigateur Tor et beaucoup moins de personnes utilisent Brave avec Tor, vous sortirez donc du lot. Lorsqu'[un fort anonymat est nécessaire](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-) utilisez le [Navigateur Tor ](tor.md#tor-browser).

##### Extensions

Désactivez les extensions intégrées que vous n'utilisez pas dans **Extensions**

- [ ] Décochez **Hangouts**
- [ ] Décochez **WebTorrent**

##### Web3

Les fonctionnalités Web3 de Brave peuvent potentiellement ajouter à l'empreinte numérique de votre navigateur et à la surface d'attaque. À moins que vous n'utilisiez l'une ou l'autre de ces fonctions, elles devraient être désactivées.

- Sélectionnez **Extensions (pas de fallback)** sous Portefeuille Ethereum par défaut et Portefeuille Solana par défaut
- Définir **Méthode de résolution des ressources IPFS** à **Désactivé**

##### Système

<div class="annotate" markdown>

- [ ] Décochez **Continuer l'exécution des applications lorsque Brave est fermé** pour désactiver les applications en arrière-plan (1)

</div>

1. Cette option n'est pas présente sur toutes les plateformes.

#### Synchronisation

La [Synchronisation Brave](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) permet à vos données de navigation (historique, signets, etc.) d'être accessibles sur tous vos appareils sans nécessiter de compte et les protège avec E2EE.

#### Récompenses et portefeuille Brave

Les **Récompenses Brave** vous permettent de recevoir de la crypto-monnaie Basic Attention Token (BAT) en effectuant certaines actions dans Brave. Elles s'appuient sur un compte de garde et sur la connaissance du client (KYC) d'un certain nombre de fournisseurs. Nous ne recommandons pas le BAT en tant que [crypto-monnaie privée](cryptocurrency.md), ni l'utilisation d'un [portefeuille de garde](advanced/payments.md#other-coins-bitcoin-ethereum-etc), et nous décourageons donc l'utilisation de cette fonctionnalité.

Le **Portefeuille Brave** fonctionne localement sur votre ordinateur, mais ne prend pas en charge les crypto-monnaies privées, nous vous déconseillons donc d'utiliser cette fonctionnalité.

## Ressources supplémentaires

D'une manière générale, nous vous recommandons de limiter au maximum les extensions de votre navigateur afin de réduire votre surface d'attaque ; elles ont un accès privilégié dans votre navigateur, vous obligent à faire confiance au développeur, peuvent vous faire [sortir du lot](https://fr.wikipedia.org/wiki/Empreinte_digitale_d%27appareil), et [affaiblir](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) l'isolation des sites. Cependant, uBlock Origin peut s'avérer utile si vous appréciez la fonctionnalité de blocage de contenu.

### uBlock Origin

!!! recommendation

    ![Logo uBlock Origin](assets/img/browsers/ublock_origin.svg){ align=right }
    
    **uBlock Origin** est un bloqueur de contenu populaire qui peut vous aider à bloquer les publicités, les traqueurs et les scripts d'empreintes numériques.
    
    [:octicons-repo-16: Dépôt](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Politique de confidentialité" }
    [:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Code source" }
    
    ??? downloads "Téléchargements"
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

Nous vous suggérons de suivre la [documentation du développeur](https://github.com/gorhill/uBlock/wiki/Blocking-mode) et de choisir l'un des "modes". Des listes de filtres supplémentaires peuvent avoir un impact sur les performances et [peuvent augmenter la surface d'attaque](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

Voici d'autres [listes de filtres](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) que vous pourriez envisager d'ajouter :

- [x] Cochez **Confidentialité** > **AdGuard URL Tracking Protection**
- Ajoutez [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

### uBlock Origin Lite

uBlock Origin possède également une version "Lite" de leur extension, qui offre un ensemble de fonctionnalités très limité par rapport à l'extension originale. Cependant, elle a quelques avantages distincts par rapport à sa grande soeur, donc vous pouvez l'envisager si...

- ...vous ne voulez pas accorder les autorisations complètes de "lecture/modification des données de sites web" à une extension (même une de confiance comme uBlock Origin)
- ...vous voulez un bloqueur de contenu plus efficace en ressources (mémoire/CPU)[^1]
- ...votre navigateur ne prend en charge que les extensions Manifest V3

!!! recommendation

    ![logo uBlock Origin Lite](assets/img/browsers/ublock_origin_lite.svg){ align=right }
    
    **uBlock Origin Lite** est un bloqueur de contenu compatible Manifest V3. Comparée à l'original *uBlock Origin*, cette extension ne nécessite pas de larges autorisations "lecture/modification des données" pour fonctionner.
    
    [:octicons-repo-16: Dépôt](https://github.com/uBlockOrigin/uBOL-home#readme){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Politique de confidentialité" }
    [:octicons-info-16:](https://github.com/uBlockOrigin/uBOL-home/wiki){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/gorhill/uBlock/tree/master/platform/mv3){ .card-link title="Code source" }
    
    ??? downloads "Téléchargements"
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/addon/ublock-origin-lite/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin-lite/ddkjiahejlhfcafbddmgiahcphecmpfh)

Nous ne recommandons cette version d'uBlock Origin que si vous ne voulez jamais apporter de modifications à vos listes de filtres, parce qu'elle ne prend en charge que quelques listes présélectionnées et n'offre aucune option de personnalisation supplémentaire, y compris la possibilité de sélectionner des éléments à bloquer manuellement. Ces restrictions sont dues à des limitations dans la conception du manifeste V3.

Cette version offre trois niveaux de blocage : "Basique" fonctionne sans avoir besoin de privilèges spéciaux pour afficher et modifier le contenu du site, tandis que les niveaux "Optimal" et "Complet" requièrent cette large autorisation, mais offrent une meilleure expérience de filtrage avec des règles cosmétiques supplémentaires et des injections de scriptlet.

Si vous définissez le mode de filtrage par défaut à "Optimal" ou "Complet", l'extension demandera l'accès en lecture/modification à **tous** les sites Web que vous visitez. Cependant, vous avez également la possibilité de changer le réglage à "Optimal" ou "Complet" **par site** en ajustant le curseur dans le panneau pop-up de l'extension sur un site donné. Lorsque vous le faites, l'extension ne demandera qu'un accès en lecture/modification de ce site. Par conséquent, si vous voulez profiter de la configuration "sans autorisation" d'uBlock Origin Lite, vous devriez probablement laisser le paramètre par défaut sur "Basique" et ne l'augmenter que sur les sites où ce niveau n'est pas adéquat.

uBlock Origin Lite ne reçoit les mises à jour de la liste de blocage que lorsque l'extension est mise à jour depuis le marché des extensions de votre navigateur, et non pas sur demande. Cela signifie que vous risquez de manquer les nouvelles menaces bloquées pendant des semaines jusqu'à ce qu'une version complète de l'extension soit publiée.

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

!!! example "Cette section est récente"

    Nous travaillons à l'établissement de critères définis pour chaque section de notre site, et celles-ci peuvent être sujet à changement. Si vous avez des questions sur nos critères, veuillez [poser la question sur notre forum](https://discuss.privacyguides.net/latest) et ne supposez pas que nous n'avons pas pris en compte un élément dans nos recommandations s'il ne figure pas dans la liste. De nombreux facteurs sont pris en compte et discutés lorsque nous recommandons un projet, et la documentation de chacun d'entre eux est en cours.

### Exigences minimales

- Doit être un logiciel open source.
- Prend en charge les mises à jour automatiques.
- Reçoit les mises à jour du moteur dans un délai de 1 jour à partir de la publication en amont.
- Disponible sur Linux, macOS et Windows.
- Les modifications nécessaires pour rendre le navigateur plus respectueux de la vie privée ne devraient pas avoir d'impact négatif sur l'expérience des utilisateurs.
- Bloque les cookies tiers par défaut.
- Prend en charge le [cloisonnement des états](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) pour atténuer le suivi intersite.[^2]


### Dans le meilleur des cas

Nos critères de cas idéal représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de cette fonctionnalité, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Comprend une fonctionnalité intégrée de blocage du contenu.
- Supporte la compartimentation des cookies (à la [Multi-Account Containers](https://support.mozilla.org/en-US/kb/containers)).
- Prend en charge les Progressive Web Apps.  
  Les PWAs vous permettent d'installer certains sites web comme s'il s'agissait d'applications natives sur votre ordinateur. Cela peut présenter des avantages par rapport à l'installation d'applications basées sur Electron, car vous bénéficiez des mises à jour de sécurité régulières de votre navigateur.
- Ne comprend pas de fonctionnalités supplémentaires (bloatware) qui n'ont pas d'incidence sur la vie privée des utilisateurs.
- Ne collecte pas de télémétrie par défaut.
- Fournit une implémentation de serveur de synchronisation open-source.
- Le moteur de recherche par défaut est un [moteur de recherche privé](search-engines.md).

### Critères d'extension

- Ne doit pas dupliquer une fonctionnalité intégrée dans le navigateur ou dans le système d'exploitation.
- Doit avoir un impact direct sur la vie privée des utilisateurs, c'est-à-dire qu'il ne doit pas simplement fournir des informations.

[^1]: uBlock Origin Lite *lui-même* ne consommera aucune ressource, parce qu'il utilise des APIs plus récentes qui permettent au navigateur de traiter nativement les listes de filtres, au lieu d'exécuter du code JavaScript dans l'extension pour gérer le filtrage. Cependant, cet avantage de ressource est seulement [théorique](https://github.com/uBlockOrigin/uBOL-home/wiki/Frequently-asked-questions-(FAQ)#is-ubol-more-efficient-cpu--and-memory-wise-than-ubo), parce qu'il est possible que le code de filtrage standard d'uBlock Origin soit plus efficace que le code de filtrage natif de votre navigateur. Cela n'a pas encore été comparé.
[^2]: L'implémentation de Brave est détaillée dans [Mises à jour de la confidentialité de Brave : partitionnement de l'état du réseau pour la confidentialité](https://brave.com/privacy-updates/14-partitioning-network-state/).
