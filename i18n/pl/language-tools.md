---
title: "Narzędzia językowe"
icon: material/alphabetical-variant
description: Te narzędzia językowe nie wysyłają wprowadzanego tekstu na serwer i można z nich korzystać offline oraz hostować je samodzielnie.
cover: language-tools.webp
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-server-network: Dostawcy usług](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: Kapitalizm inwigilacji](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

Tekst wprowadzany do narzędzi sprawdzających gramatykę, ortografię i styl oraz do usług tłumaczeniowych może zawierać poufne informacje, które mogą być przechowywane na serwerach tych usług przez nieokreślony czas i sprzedawane stronom trzecim. Narzędzia językowe wymienione na tej stronie nie przechowują przesyłanych tekstów na serwer i można je hostować samodzielnie, aby mieć maksymalną kontrolę nad swoimi danymi.

## Gramatyka i ortografia

### LanguageTool

<div class="admonition recommendation" markdown>

![Logo LanguageTool](assets/img/language-tools/languagetool.svg#only-light){ align=right }
![Logo LanguageTool](assets/img/language-tools/languagetool-dark.svg#only-dark){ align=right }

**LanguageTool** to wielojęzyczne narzędzie do sprawdzania gramatyki, stylu i ortografii, obsługujące ponad 20 języków. Zgodnie z ich polityką prywatności nie przechowuje żadnych treści przesyłanych do ich usługi w celu sprawdzenia, jednak dla większej pewności oprogramowanie można [hostować samodzielnie](https://dev.languagetool.org/http-server).

[:octicons-home-16: Strona główna](https://languagetool.org/pl){ .md-button .md-button--primary }
[:octicons-eye-16:](https://languagetool.org/pl/legal/privacy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://languagetooler.freshdesk.com/en/support/solutions){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/languagetool-org){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1534275760)
- [:fontawesome-brands-windows: Windows](https://languagetool.org/pl/windows-desktop)
- [:simple-apple: macOS](https://languagetool.org/pl/mac-desktop)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/languagetool)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/oldceeleldhonbafppcapldpdifcinji)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/hfjadhjooeceemgojogkhlppanjkbobc)
- [:simple-safari: Safari](https://apps.apple.com/app/id1534275760)

</details>

</div>

LanguageTool oferuje integrację z różnymi [pakietami biurowymi](https://languagetool.org/pl/services#text_editors) i [klientami poczty e-mail](https://languagetool.org/pl/services#mail_clients).

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

## Kryteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

- Musi być open source.
- Must be possible to self-host.
