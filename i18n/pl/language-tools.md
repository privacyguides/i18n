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

## Narzędzia do tłumaczenia

### LibreTranslate

<div class="admonition recommendation" markdown>

![Logo LibreTranslate](assets/img/language-tools/libretranslate.png){ align=right }

\*_LibreTranslate_ to darmowy interfejs internetowy i serwer API do tłumaczenia maszynowego typu open source. Do tłumaczeń wykorzystuje on modele [Argos Translate](https://github.com/argosopentech/argos-translate).

[:octicons-home-16: Strona główna](https://libretranslate.com){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/LibreTranslate/LibreTranslate#mirrors){ .card-link title="Instancje publiczne" }
[:octicons-code-16:](https://github.com/LibreTranslate/LibreTranslate){ .card-link title="Kod źródłowy" }

</div>

Dostępne są publiczne instancje LibreTranslate, w tym niektóre oferujące usługę .onion przez [sieć Tor](tor.md) lub eepsite w [I2P](alternative-networks.md#i2p-the-invisible-internet-project). Można też uruchomić oprogramowanie samodzielnie, by mieć pełną kontrolę nad przesyłanymi tekstami.

Używamy hostowanej lokalnie instancji LibreTranslate do automatycznego tłumaczenia wpisów na naszym [forum](https://discuss.privacyguides.net) na wiele języków.

## Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

- Musi być open source.
- Musi być możliwy do samodzielnego hostowania.
