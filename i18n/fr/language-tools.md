---
title: "Outils linguistiques"
icon: material/alphabetical-variant
description: Ces outils linguistiques n'envoient pas le texte saisi à un serveur, ils peuvent être utilisés hors ligne et être auto-hébergés.
cover: language-tools.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-server-network: Fournisseurs de Services](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: Capitalisme de Surveillance](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

Les textes passant par des correcteurs de grammaire, de style et d'orthographe, ou par des services de traduction, contiennent parfois des informations sensibles qui peuvent être stockées sur leurs serveurs indéfiniment ou être vendues à des tiers. Les outils linguistiques présentés ici ne stockent pas les textes analysés sur un serveur et peuvent être auto-hébergés et/ou utilisé hors-ligne pour vous donner un maximum de contrôle sur vos données.

## Grammaire et orthographe

### LanguageTool

<div class="admonition recommendation" markdown>

![Logo de LanguageTool](assets/img/language-tools/languagetool.svg#only-light){ align=right }
![Logo de LanguageTool](assets/img/language-tools/languagetool-dark.svg#only-dark){ align=right }

**LanguageTool** est un correcteur de grammaire, d'orthographe et de style disponible dans plus de 20 langues différentes. D'après leur politique de confidentialité, ils ne stockent aucune donnée envoyée à leurs services, mais pour une confidentialité plus élevée, le service peut être [auto-hébergé](https://dev.languagetool.org/http-server).

[:octicons-home-16: Page d'Accueil](https://languagetool.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://languagetool.org/legal/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://languagetooler.freshdesk.com/en/support/solutions){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/languagetool-org){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1534275760)
- [:fontawesome-brands-windows: Windows](https://languagetool.org/windows-desktop)
- [:simple-apple: macOS](https://languagetool.org/mac-desktop)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/languagetool)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/oldceeleldhonbafppcapldpdifcinji)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/hfjadhjooeceemgojogkhlppanjkbobc)
- [:simple-safari: Safari](https://apps.apple.com/app/id1534275760)

</details>

</div>

LanguageTool est compatible avec plusieurs [suites de bureautique](https://languagetool.org/services#text_editors) et [client mail](https://languagetool.org/services#mail_clients).

## Outils de traduction

### LibreTranslate

<div class="admonition recommendation" markdown>

![Logo de LibreTranslate](assets/img/language-tools/libretranslate.png){ align=right }

**LibreTranslate** est un outil de traduction automatique libre et open-source sous forme d'interface web et d'un serveur API. Il utilise les modèles de [Argos Translate](https://github.com/argosopentech/argos-translate) en arrière-plan pour les traductions.

[:octicons-home-16: Page d'Accueil](https://libretranslate.com){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/LibreTranslate/LibreTranslate#mirrors){ .card-link title="Instances Publiques" }
[:octicons-code-16:](https://github.com/LibreTranslate/LibreTranslate){ .card-link title="Code Source" }

</div>

Vous pouvez utiliser LibreTranslate via différentes instances publiques, dont certaines disposent d'un service onion [Tor](tor.md) ou d'un eepsite [I2P](alternative-networks.md#i2p-the-invisible-internet-project). Pour un maximum de contrôle, vous pouvez également auto-héberger le service.

Nous utilisons une instance auto-hébergée de LibreTranslate pour traduire automatiquement les posts sur notre [forum](https://discuss.privacyguides.net) en plusieurs langues.

## Critères

**Nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de nos [critères de base](about/criteria.md), nous avons élaboré une liste d'exigences claire qui nous permet de proposer des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

- Dois être open-source.
- Dois pouvoir être auto-hébergé.
