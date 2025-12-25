---
title: Rozszerzenia przeglądarki
icon: material/puzzle-outline
description: Te rozszerzenia przeglądarki mogą poprawić komfort przeglądania i chronić Twoją prywatność.
cover: browser-extensions.webp
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-account-cash: Kapitalizm inwigilacji](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

Zasadniczo zalecamy ograniczyć liczbę rozszerzeń przeglądarki do minimum, by zmniejszyć powierzchnię ataku. Mają one uprzywilejowany dostęp w przeglądarce, wymagają zaufania do twórcy, mogą sprawić, że się [wyróżnisz](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint) oraz mogą [osłabiać](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) izolację stron.

Niektóre jednak oferują funkcje, które w pewnych sytuacjach mogą przeważyć nad tymi wadami, szczególnie w kwestii [blokowania treści](basics/common-threats.md#mass-surveillance-programs).

Nie instaluj rozszerzeń, których od razu nie potrzebujesz, ani takich, które dublują funkcje przeglądarki. Dla przykładu użytkownicy przeglądarki [Brave](desktop-browsers.md#brave) nie muszą instalować rozszerzenia uBlock Origin, ponieważ Brave Shields już zapewnia tę samą funkcjonalność.

## Blokery treści

### uBlock Origin

<div class="admonition recommendation" markdown>

![Logo uBlock Origin](assets/img/browsers/ublock_origin.svg){ align=right }

**uBlock Origin** to popularny bloker treści, który może pomóc w blokowaniu reklam, trackerów i skryptów służących do identyfikacji użytkowników.

[:octicons-repo-16: Repozytorium](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Dokumentacja}
[:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

</details>

</div>

Zalecamy zapoznanie się z [dokumentacją twórcy](https://github.com/gorhill/uBlock/wiki/Blocking-mode) i wybranie jednego z „trybów”. Dodatkowe listy filtrów mogą obniżyć wydajność i [zwiększyć powierzchnię ataku](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

Oto kilka przykładowych [list filtrów](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists), których dodanie warto rozważyć:

- [x] Sprawdź **Prywatność** > **AdGuard URL Tracking Protection**
- Dodaj [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

### uBlock Origin Lite

uBlock Origin ma też wersję „Lite”, która oferuje bardzo ograniczony zestaw funkcji w porównaniu z oryginałem. Ma jednak kilka istotnych zalet względem swojej pełnoprawnej wersji, więc warto ją rozważyć, jeśli:

- nie chcesz przyznawać żadnym rozszerzeniom pełnych uprawnień „odczytu i modyfikacji danych witryn” (nawet zaufanemu jak uBlock Origin),
- zależy Ci na bardziej oszczędnym pod względem zasobów (pamięci/procesora) blokerze treści[^1],
- Twoja przeglądarka obsługuje jedynie rozszerzenia zgodne z Manifest V3.

<div class="admonition recommendation" markdown>

![Logo uBlock Origin Lite](assets/img/browsers/ublock_origin_lite.svg){ align=right }

**uBlock Origin Lite** to bloker treści zgodny z Manifest V3. W porównaniu z oryginalnym _uBlock Origin_ rozszerzenie to nie wymaga szerokich uprawnień „odczytu i modyfikacji danych witryn”, by działać, co zmniejsza ryzyko [:material-bug-outline: Ataków pasywnych](basics/common-threats.md#security-and-privacy){ .pg-orange } na przeglądarkę, jeśli do listy filtrów zostanie dodana złośliwa reguła.

[:octicons-repo-16: Repozytorium](https://github.com/uBlockOrigin/uBOL-home#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uBlockOrigin/uBOL-home/wiki/Privacy-policy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://github.com/uBlockOrigin/uBOL-home/wiki){ .card-link title=Dokumentacja}
[:octicons-code-16:](https://github.com/gorhill/uBlock/tree/master/platform/mv3){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin-lite/ddkjiahejlhfcafbddmgiahcphecmpfh)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/cimighlppcgcoapaliogpjjdehbnofhn)
- [:simple-safari: Safari](https://apps.apple.com/app/id6745342698)

</details>

</div>

Zalecamy korzystanie z tej wersji uBlock Origin tylko wtedy, gdy nie planuje się wprowadzać żadnych zmian w listach filtrów, ponieważ obsługuje ona wyłącznie kilka wcześniej wybranych list i nie oferuje dodatkowych opcji personalizacji, w tym możliwości ręcznego wybierania elementów do zablokowania. Ograniczenia te wynikają z ograniczeń projektowych Manifest V3.

Wersja ta oferuje trzy poziomy blokowania: „podstawowy” działa bez konieczności przyznawania specjalnych uprawnień do przeglądania i modyfikacji zawartości stron, natomiast poziomy „optymalny” i „kompletny” wymagają takich szerokich uprawnień, lecz zapewniają lepsze filtrowanie dzięki dodatkowym regułom kosmetycznym i wstrzykiwaniu skryptów.

Jeśli ustawisz domyślny tryb filtrowania na „optymalny” lub „kompletny”, rozszerzenie poprosi o dostęp do odczytu i modyfikacji **wszystkich** odwiedzanych witryn. Masz jednak opcję zmiany ustawienia na „optymalny” lub „kompletny” dla **pojedynczych witryn**, przesuwając suwak w wyskakującym panelu rozszerzenia na danej stronie. W takim przypadku rozszerzenie poprosi o uprawnienia odczytu i modyfikacji tylko do tej witryny. Jeśli chcesz korzystać z „konfiguracji bez uprawnień”, zostaw domyślny tryb „podstawowy” i podnoś go jedynie na stronach, gdzie jest to konieczne.

uBlock Origin Lite aktualizuje listy blokowania tylko przy aktualizacji rozszerzenia w sklepie z rozszerzeniami przeglądarki, a nie na żądanie. Google ma [przyspieszony proces przeglądu](https://developer.chrome.com/docs/webstore/skip-review) dla aktualizacji filtrów, co zwykle oznacza, że otrzymujesz aktualizacje list tak często, jak twórcy publikują wydania (historycznie co 2–7 dni). Jednak aktualizowane mogą być wyłącznie tzw. [bezpieczne reguły](https://developer.chrome.com/docs/extensions/reference/api/declarativeNetRequest#safe_rules), co może ograniczać częstotliwość aktualizacji list wykorzystujących zaawansowane techniki.

### AdGuard

Zalecamy przeglądarkę [Safari](mobile-browsers.md#safari-ios) dla użytkowników iOS, która niestety nie obsługuje uBlock Origin. Na szczęście AdGuard stanowi odpowiednią alternatywę:

<div class="admonition recommendation" markdown>

![Logo AdGuard](assets/img/browsers/adguard.svg){ align=right }

**AdGuard na iOS** to bezpłatne rozszerzenie typu open source do blokowania treści w przeglądarce Safari, korzystające z natywnego [Content Blocker API](https://developer.apple.com/documentation/safariservices/creating_a_content_blocker).

[:octicons-home-16: Strona główna](https://adguard.com/pl/adguard-ios/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/ios.html){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title=Dokumentacja}
[:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1047223162)

</details>

</div>

Dodatkowe listy filtrów mogą spowalniać działanie i zwiększać powierzchnię ataku, dlatego stosuj tylko to, czego potrzebujesz. AdGuard na iOS oferuje funkcje premium; podstawowe blokowanie treści w Safari jest jednak bezpłatne.

## Kryteria

- Nie może dublować wbudowanej funkcjonalności przeglądarki ani systemu operacyjnego.
- Musi bezpośrednio wpływać na prywatność użytkownika — innymi słowy, nie może jedynie dostarczać informacji.

[^1]: uBlock Origin Lite _sam w sobie_ nie zużywa zasobów bezpośrednio, ponieważ wykorzystuje nowsze interfejsy API, które sprawiają, że to przeglądarka natywnie przetwarza listy filtrów, zamiast uruchamiać kod JavaScript w rozszerzeniu do obsługi filtrowania. Ta przewaga zasobowa jest jednak jedynie [teoretyczna](https://github.com/uBlockOrigin/uBOL-home/wiki/Frequently-asked-questions-\(FAQ\)#is-ubol-more-efficient-cpu--and-memory-wise-than-ubo), ponieważ możliwe, że kod filtrowania standardowego uBlock Origin jest bardziej wydajny niż natywne filtrowanie przeglądarki. Nie zostało to jak dotąd zbadane.
