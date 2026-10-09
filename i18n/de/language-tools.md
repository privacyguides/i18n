---
title: "Language Tools"
icon: material/alphabetical-variant
description: Diese Sprachtools senden deinen Eingabetext nicht an einen Server und können offline und selbst gehostet verwendet werden.
cover: language-tools.webp
---

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-server-network: Diensteanbieter](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: Überwachungskapitalismus](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

Texte, die in Grammatik-, Rechtschreib- und Stilprüfungsprogramme sowie in Übersetzungsdienste eingegeben werden, können vertrauliche Informationen enthalten, die auf deren Servern auf unbestimmte Zeit gespeichert und an Dritte verkauft werden können. The language tools listed on this page do not store your submitted text on a server and can be self-hosted and used offline for maximum control of your data.

## Translation Tools

### LibreTranslate

<div class="admonition recommendation" markdown>

![LibreTranslate logo](assets/img/language-tools/libretranslate.png){ align=right }

**LibreTranslate** is a free and open-source machine translation web interface and API server. It uses [Argos Translate](https://github.com/argosopentech/argos-translate) models on the backend for translations.

[:octicons-home-16: Homepage](https://libretranslate.com){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/LibreTranslate/LibreTranslate#mirrors){ .card-link title="Public Instances" }
[:octicons-code-16:](https://github.com/LibreTranslate/LibreTranslate){ .card-link title="Source Code" }

</div>

You can use LibreTranslate through a number of public instances, with some that offer a [Tor](tor.md) onion service or an [I2P](alternative-networks.md#i2p-the-invisible-internet-project) eepsite. You can also host the software yourself for maximum control over the text submitted for translation.

We use a self-hosted instance of LibreTranslate to automatically translate posts on our [forum](https://discuss.privacyguides.net) to multiple languages.

We use the VSCode extension in our GitHub repository configuration to find any grammar and spelling errors on our website and in our articles.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, in Verbindung stehen.** Zusätzlich zu [unseren Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen dir, dich mit der Liste vertraut zu machen, bevor du dich für ein Projekt entscheidest, und deine eigenen Recherchen anzustellen, um sicherzustellen, dass es die richtige Wahl für dich ist.

- Muss Open Source sein.
- Must run completely offline.
