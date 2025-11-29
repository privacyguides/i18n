---
title: "語言工具"
icon: material/alphabetical-variant
description: 這些語言工具不會將您輸入的文字傳送至伺服器，可以離線或自行架設伺服器來使用。
cover: language-tools.webp
---

<small>防護下列威脅：</small>

- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

輸入到文法、拼寫和樣式檢查器以及翻譯服務的文字可能包含敏感資訊，這些資訊可能無限期地儲存在伺服器上，並被出售給第三方。 本頁面列出的語言工具不會將您遞交的文字除存在伺服器上，且能自行架設並離線使用，以最大程度控制您的資料。

## 文法與拼字

### LanguageTool

<div class="admonition recommendation" markdown>

![LanguageTool logo](assets/img/language-tools/languagetool.svg#only-light){ align=right }
![LanguageTool logo](assets/img/language-tools/languagetool-dark.svg#only-dark){ align=right }

**LanguageTool** 是多語言文法、風格與拼字檢查程式，支援超過 20 種語言。 根據其隱私權政策，該服務不會儲存任何提交審閱的內容，但為提供更高保障，此軟體具備[自行架設功能](https://dev.languagetool.org/http-server)。

[:octicons-home-16: 首頁](https://languagetool.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://languagetool.org/legal/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://languagetooler.freshdesk.com/en/support/solutions){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/languagetool-org){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1534275760)
- [:fontawesome-brands-windows: Windows](https://languagetool.org/windows-desktop)
- [:simple-apple: macOS](https://languagetool.org/mac-desktop)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/languagetool)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/oldceeleldhonbafppcapldpdifcinji)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/hfjadhjooeceemgojogkhlppanjkbobc)
- [:simple-safari: Safari](https://apps.apple.com/app/id1534275760)

</details>

</div>

LanguageTool 提供與多種 [辦公室套件](https://languagetool.org/services#text_editors) 及 [電子郵件客戶端](https://languagetool.org/services#mail_clients) 的整合。

## 翻譯工具

### LibreTranslate

<div class="admonition recommendation" markdown>

![LibreTranslate 標誌](assets/img/language-tools/libretranslate.png){ align=right }

**LibreTranslate** 是自由且開放原始碼的機器翻譯網頁介面與 API 伺服器。 其在後端使用 [Argos Translate](https://github.com/argosopentech/argos-translate) 模型進行翻譯。

[:octicons-home-16: 首頁](https://libretranslate.com){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/LibreTranslate/LibreTranslate#mirrors){ .card-link title="公開站台" }
[:octicons-code-16:](https://github.com/LibreTranslate/LibreTranslate){ .card-link title="原始碼" }

</div>

您可以透過許多公開站台使用 LibreTranslate，有些提供 [Tor](tor.md) 洋蔥服務或 pI2P](alternative-networks.md#i2p-the-invisible-internet-project) 匿名站點。 您亦可自行架設軟體，以獲得對遞交翻譯之文字的最大控制權。

我們使用 LibreTranslate 的自行架設站台，將我們[論壇](https://discuss.privacyguides.net)上的貼文自動翻譯成多國語言。

## 標準

\*\*請注意，我們與推薦的任何項目均無關。\*\*除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- 它必須是開源的。
- 必須可以自行託管。
