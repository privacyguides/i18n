---
title: "語言工具"
icon: material/alphabetical-variant
description: 這些語言工具不會將您輸入的文字傳送至伺服器，可以離線或自行架設伺服器來使用。
cover: language-tools.webp
---

<small>防護下列威脅：</small>

- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

輸入到文法、拼寫和樣式檢查器以及翻譯服務的文字可能包含敏感資訊，這些資訊可能無限期地儲存在伺服器上，並被出售給第三方。 The language tools listed on this page do not store your submitted text on a server and can be self-hosted and used offline for maximum control of your data.

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

## 標準

\*\*請注意，我們與推薦的任何項目均無關。\*\*除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- 它必須是開源的。
- Must run completely offline.
