---
title: Extensions de navigateur
icon: material/puzzle-outline
description: Ces extensions de navigateur peuvent améliorer votre expérience de navigation et protéger votre vie privée.
cover: browser-extensions.webp
---

<small>Protège contre la(les) menace(s) suivante(s)</small>

- [:material-account-cash: Capitalisme de surveillance](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

En général, nous recommandons votre nombre d'extensions de navigateur à un minimum afin de réduire votre surface d'attaque. Ils ont un accès privilégié à votre navigateur, vous obligent à faire confiance au développeur, peuvent vous faire [resortir](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint) et [affaiblir](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) l'isolation du site.

Cependant, certaines offrent des fonctionnalités qui peuvent compenser ces inconvénients dans certaines situations, en particulier lorsqu'il s'agit de [blocage de contenu] (basics/common-threats.md#mass-surveillance-programs).

N'installez pas d'extensions dont vous n'avez pas immédiatement besoin ou qui dupliquent des fonctionnalités de votre navigateur. Par exemple, les utilisateurs de [Brave](desktop-browsers.md#brave) n'ont pas besoin d'installer uBlock Origin, car Brave Shields offre déjà la même fonction.

## Bloqueurs de contenu

### uBlock Origin

<div class="admonition recommendation" markdown>

![uBlock Origin logo](assets/img/browsers/ublock_origin.svg){ align=right }

**uBlock Origin** est un bloqueur de contenu populaire qui peut vous aider à bloquer les publicités, les traqueurs et les scripts d'empreintes numériques.

[:octicons-repo-16: Dépôt](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Politique de confidentialié" }
[:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

</details>

</div>

Nous recommandons de suivre la [documentation développeur] (https://github.com/gorhill/uBlock/wiki/Blocking-mode) et de choisir l'un des "modes". Les listes de filtres supplémentaires peuvent avoir un impact sur les performances et [peuvent augmenter la surface d'attaque] (https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

Voici d'autres [listes de filtres] (https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) que vous pourriez envisager d'ajouter :

- [x] Vérifier **Privacy** > **AdGuard URL Tracking Protection** (protection contre le traçage des URL)
- Ajoutez [Outil de raccourcissement d'URL légitime](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

### uBlock Origin Lite

uBlock Origin possède également une version "Lite" de leur extension, qui offre un ensemble de fonctionnalités très limité par rapport à l'extension originale. Cependant, elle a quelques avantages distincts par rapport à sa grande soeur, donc vous pouvez l'envisager si...

- ...vous ne voulez pas accorder les autorisations complètes de "lecture/modification des données de sites web" à une extension (même une de confiance comme uBlock Origin)
- ...vous voulez un bloqueur de contenu plus efficace en termes de ressources (mémoire/CPU)[^1]
- ...votre navigateur ne prend en charge que les extensions Manifest V3

<div class="admonition recommendation" markdown>

![uBlock Origin Lite logo](assets/img/browsers/ublock_origin_lite.svg){ align=right }

**uBlock Origin Lite** est un bloqueur de contenu compatible avec Manifest V3. Par rapport au _uBlock Origin_ de base, cette extension ne nécessite pas d'autorisations générales de "lecture/modification des données" pour fonctionner, ce qui réduit le risque d' [:material-bug-outline: Attaque Passive](basics/common-threats.md#security-and-privacy){ .pg-orange } sur votre navigateur si une règle malveillante est ajoutée à une liste de filtrage.

[:octicons-repo-16: Dépôt](https://github.com/uBlockOrigin/uBOL-home#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uBlockOrigin/uBOL-home/wiki/Privacy-policy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://github.com/uBlockOrigin/uBOL-home/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/gorhill/uBlock/tree/master/platform/mv3){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin-lite/ddkjiahejlhfcafbddmgiahcphecmpfh)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/cimighlppcgcoapaliogpjjdehbnofhn)
- [:simple-safari: Safari](https://apps.apple.com/app/id6745342698)

</details>

</div>

Nous ne recommandons cette version d'uBlock Origin que si vous ne voulez jamais apporter de modifications à vos listes de filtres, parce qu'elle ne prend en charge que quelques listes présélectionnées et n'offre aucune option de personnalisation supplémentaire, y compris la possibilité de sélectionner des éléments à bloquer manuellement. Ces restrictions sont dues à des limitations dans la conception du manifeste V3.

Cette version offre trois niveaux de blocage : "Basique" fonctionne sans avoir besoin de privilèges spéciaux pour afficher et modifier le contenu du site, tandis que les niveaux "Optimal" et "Complet" requièrent cette large autorisation, mais offrent une meilleure expérience de filtrage avec des règles cosmétiques supplémentaires et des injections de scriptlet.

Si vous définissez le mode de filtrage par défaut à "Optimal" ou "Complet", l'extension demandera l'accès en lecture/modification à **tous** les sites Web que vous visitez. Cependant, vous avez également la possibilité de changer le réglage à "Optimal" ou "Complet" **par site** en ajustant le curseur dans le panneau pop-up de l'extension sur un site donné. Lorsque vous le faites, l'extension ne demandera qu'un accès en lecture/modification de ce site. Par conséquent, si vous voulez profiter de la configuration "sans autorisation" d'uBlock Origin Lite, vous devriez probablement laisser le paramètre par défaut sur "Basique" et ne l'augmenter que sur les sites où ce niveau n'est pas adéquat.

uBlock Origin Lite ne reçoit les mises à jour de la liste de blocage que lorsque l'extension est mise à jour depuis le marché des extensions de votre navigateur, et non pas sur demande. Google a mis en place une [procédure de révision accélérée] (https://developer.chrome.com/docs/webstore/skip-review) pour les mises à jour de filtres, ce qui signifie que vous recevez toujours des mises à jour de la liste de filtres aussi souvent que uBlock Origin Lite choisit de publier une version (historiquement tous les 2 à 7 jours). Toutefois, seules les prétendues "[règles sûres](https://developer.chrome.com/docs/extensions/reference/api/declarativeNetRequest#safe_rules)" peuvent être mises à jour, ce qui peut limiter la fréquence de mise à jour des listes utilisant des techniques avancées.

### AdGuard

Nous recommandons [Safari](mobile-browsers.md#safari-ios) pour les utilisateurs d'iOS, qui n'est malheureusement pas pris supporté par uBlock Origin. Heureusement, AdGuard offre une alternative adéquate :

<div class="admonition recommendation" markdown>

![AdGuard logo](assets/img/browsers/adguard.svg){ align=right }

**AdGuard pour iOS** est une extension gratuite et open-source de blocage de contenu pour Safari qui utilise l'API native [Content Blocker API] (https://developer.apple.com/documentation/safariservices/creating_a_content_blocker).

[:octicons-home-16: Page d'accueil](https://adguard.com/en/adguard-ios/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/ios.html){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1047223162)

</details>

</div>

Les listes de filtres supplémentaires ralentissent la navigation et peuvent augmenter votre surface d'attaque. N'appliquez donc que ce dont vous avez besoin. AdGuard pour iOS dispose de quelques fonctions payantes, mais le blocage standard du contenu de Safari est gratuit.

## Critères

- Ne doit pas dupliquer une fonctionnalité intégrée dans le navigateur ou dans le système d'exploitation.
- Doit avoir un impact direct sur la vie privée des utilisateurs, c'est-à-dire qu'il ne doit pas simplement fournir des informations.

[^1]: uBlock Origin Lite _lui-même_ ne consommera aucune ressource, parce qu'il utilise des APIs plus récentes qui permettent au navigateur de traiter nativement les listes de filtres, au lieu d'exécuter du code JavaScript dans l'extension pour gérer le filtrage. Cependant, cet avantage en termes de ressources n'est que [théorique](https://github.com/uBlockOrigin/uBOL-home/wiki/Frequently-asked-questions-\(FAQ\)#is-ubol-more-efficient-cpu--and-memory-wise-than-ubo), car il est possible que le code de filtrage standard de uBlock Origin soit plus efficace que le code de filtrage natif de votre navigateur. Cela n'a pas encore été évalué.
