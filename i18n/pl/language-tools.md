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

We use the VSCode extension in our GitHub repository configuration to find any grammar and spelling errors on our website and in our articles.

## Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

- Musi być open source.
- Must run completely offline.
