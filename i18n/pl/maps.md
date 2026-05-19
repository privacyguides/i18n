---
meta_title: "Zalecane mapy i aplikacje nawigacyjne - Privacy Guides"
title: Mapy i Nawigacja
icon: material/map
description: Szanujący prywatność dostawcy map i aplikacje nawigacyjne, które nie tworzą profilu reklamowego na podstawie wyszukiwań i lokalizacji użytkownika.
cover: maps.webp
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-account-cash: Kapitalizm inwigilacji](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

Korzystaj z **aplikacji do map i nawigacji**, która nie tworzy profilu reklamowego na podstawie twoich wyszukiwań i historii lokalizacji. Zamiast korzystać z Google Maps, Apple Maps lub Waze, zalecamy te alternatywne rozwiązania, które szanują prywatność.

Niniejsze zalecenia nie gromadzą informacji umożliwiających identyfikację użytkownika (PII) na podstawie politykę prywatności każdej z aplikacji. Nie ma **żadnej gwarancji**, że te polityki prywatności są przestrzegane.

## Organic Maps

<div class="admonition recommendation" markdown>

![Logo Organic Maps](assets/img/maps/organic-maps.svg){ align=right }

**Organic Maps** to rozwijana przez społeczność aplikacja open source do wyświetlania map i nawigacji satelitarnej dla pieszych, kierowców i rowerzystów. Aplikacja oferuje mapy całego świata, offline oparte na danych OpenStreetMap i nawigację z prywatnością — bez śledzenia lokalizacji, bez gromadzenia danych i bez reklam. Aplikacja może być używana całkowicie offline.

Funkcje obejmują trasy rowerowe, szlaki turystyczne i ścieżki spacerowe, nawigację zakręt po zakręcie ze wskazówkami głosowymi oraz planowanie tras transportu publicznego (dostępne tylko w obsługiwanych regionach i miastach).

[:octicons-home-16: Strona główna](https://organicmaps.app){ .md-button .md-button--primary }[:octicons-eye-16:](https://organicmaps.app/privacy){ .card-link title="Polityka prywatności" }
[:octicons-code-16:](https://github.com/organicmaps/organicmaps){ .card-link title="Dokumentacja"}
{ .card-link title="Kod źródłowy" }

<details class="downloads" markdown><0>Pobierz</0>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.organicmaps)
- [:simple-appstore: App Store](https://apps.apple.com/app/organic-maps/id1567437057)
- [:simple-github: GitHub](https://github.com/organicmaps/organicmaps/releases)
- [:simple-linux: Linux](https://flathub.org/apps/app.organicmaps.desktop)

</details>

</div>

Należy pamiętać, że Organic Maps to prosta, podstawowa aplikacja, w której brakuje niektórych funkcji, których wielu użytkowników może oczekiwać, takich jak zdjęcia satelitarne, zdjęcia z widokiem ulicy i informacje o ruchu drogowym w czasie rzeczywistym.

## OsmAnd

<div class="admonition recommendation" markdown>

![Logo OsmAnd](assets/img/maps/osmand.svg){ align=right }

**OsmAnd** jest mapa i aplikacja nawigacyjna offline i open source opartą na OpenStreetMap, która oferuje nawigację zakręt po zakręcie dla pieszych, rowerzystów, kierowców, a także transportu publicznego. Szczegółowy przegląd obsługiwanych przez OsmAnd [funkcji](https://wiki.openstreetmap.org/wiki/OsmAnd#Features) można znaleźć na OpenStreet Map Wiki.

[:octicons-home-16: Strona główna](https://osmand.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://osmand.net/docs/legal/privacy-policy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://osmand.net/docs/intro){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/osmandapp){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown><summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.osmand)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/id934850257)
- [:simple-android: Android](https://osmand.net/docs/versions/free-versions)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Unikalny identyfikator użytkownika</p>

OsmAnd generuje [unikalny identyfikator użytkownika (UUID)](https://osmand.net/docs/legal/terms-of-use/#6-unique-user-indentifier) dla każdej instalacji aplikacji, który zmienia się co trzy miesiące i jest używany do wewnętrznych raportów i statystyk. UUID jest również wysyłany do serwerów OsmAnd podczas pobierania map. W systemie Android istnieje ustawienie, które kontroluje, czy identyfikator UUID jest wysyłany z każdym żądaniem pobrania. Na ekranie głównym przejdź do :material-menu: → :gear: **Ustawienia** → :gear: **Ustawienia OsmAnd** → :material-web: **Identyfikatory**.

- [ ] Odznacz **Wyślij unikalny identyfikator użytkownika (UUID)**

To ustawienie nie jest dostępne w aplikacji na telefonach z iOS.

</div>

Aplikacja posiada również ustawienie udostępniania anonimowych danych o pobranych przez Ciebie mapach i używanych przez Ciebie funkcjach. To ustawienie jest domyślnie wyłączone w wersji na systemy Android, ale domyślnie włączone w wersji systemy iOS. Aby wyłączyć je w aplikacji iOS, dotknij :material-menu: na ekranie głównym, aby znaleźć menu :gear: **Ustawienia**. Wybierz tę opcję, a następnie wybierz :gear: **Ustawienia OsmAnd**.

- [ ] Odznacz **Wyślij anonimowe dane**

OsmAnd umożliwia nakładanie lub podkładanie zewnętrznych danych map, takich jak zdjęcia satelitarne od Microsoft lub [dane o ruchu drogowym](https://themm.net/public/osmand_traffic) od Google, chociaż te drugie są ignorowane przez automatyczne planowanie trasy. OsmAnd posiada również opcjonalną integrację obrazów widoku ulicy dostarczanych przez [Mapillary](https://mapillary.com).

## Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

### Minimalne wymagania

- Nie może gromadzić danych osobowych zgodnie z polityką prywatności.
- Nie może wymagać od użytkowników utworzenia konta.
- Nie może wymagać od użytkowników udostępniania danych o lokalizacji. Jeśli użytkownik wyrazi zgodę na udostępnianie swojej lokalizacji, dane te muszą zostać zanonimizowane.
- Musi zachowywać podstawowe funkcje w trybie offline i umożliwiać użytkownikom pobieranie map do użytku offline.

### Najlepszy scenariusz

Nasze kryteria „najlepszego scenariusza” określają, jak powinien wyglądać idealny projekt w tej kategorii. Nasze zalecenia nie muszą spełniać wszystkich tych warunków, jednak projekty, które spełniają więcej z nich, mogą być oceniane wyżej od pozostałych na stronie.

- Aplikacje powinny być open source.
- Powinny mieć możliwość planowania tras dla transportu publicznego.
- Powinny mieć informacje o ruchu drogowym w czasie rzeczywistym do planowania trasy.
- Powinny obsługiwać zaawansowane funkcje, takie jak szczegółowe informacje i recenzje sklepów/punktów zainteresowania (POI), mapy topograficzne oraz zdjęcia satelitarne i widoki ulic.
