---
meta_title: "Rekomendacje i porównanie prywatnych usług VPN, bez sponsorów i reklam - Privacy Guides"
title: "Usługi VPN"
icon: material/vpn
description: Najlepsze usługi VPN do ochrony prywatności i bezpieczeństwa w Internecie. Znajdź tutaj dostawcę, który nie jest po to, żeby Cię szpiegować.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-account-cash: Kapitalizm inwigilacji](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Jeśli szukasz dodatkowej *prywatności* od swojego dostawcy usług internetowych, w publicznej sieci Wi-Fi lub podczas torrentowania plików, **VPN** może być rozwiązaniem dla Ciebie.

<div class="admonition danger" markdown>
<p class="admonition-title">VPN nie zapewnia anonimowości</p>

Korzystanie z VPN **nie** zachowuje anonimowość Twoich nawyków przeglądania, ani nie zwiększy bezpieczeństwa niezabezpieczonego ruchu (HTTP).

Jeśli szukasz **anonimowości**, powinieneś korzystać z przeglądarki Tor. Jeśli szukasz dodatkowego **bezpieczeństwa**, powinieneś zawsze upewnić się, że łączysz się ze stronami internetowymi za pomocą HTTPS. VPN nie zastępuje dobrych praktyk w zakresie bezpieczeństwa.

[Pobierz Tor](https://torproject.org){ .md-button .md-button--primary } [Mity Tor & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Szczegółowy przegląd VPN :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Rekomendowani dostawcy

Polecani przez nas dostawcy stosują szyfrowanie, obsługują WireGuard & OpenVPN i stosują politykę braku logów. Przeczytaj naszą [pełną listę kryteriów](#criteria), aby uzyskać więcej informacji.

| Dostawca              | Kraje | WireGuard                     | Przekazywanie portów                                      | IPv6                                                            | Anonimowe płatności |
| --------------------- | ----- | ----------------------------- | --------------------------------------------------------- | --------------------------------------------------------------- | ------------------- |
| [Proton](#proton-vpn) | 112+  | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Częściowe wsparcie | :material-information-outline:{ .pg-blue } Ograniczone wsparcie | Gotówka             |
| [IVPN](#ivpn)         | 37+   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                    | :material-information-outline:{ .pg-blue } Tylko wychodzące     | Monero, Gotówka     |
| [Mullvad](#mullvad)   | 49+   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                    | :material-check:{ .pg-green }                                   | Monero, Gotówka     |

### Proton VPN

<div class="admonition recommendation" markdown>

![Logo Proton VPN](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** jest silnym konkurentem w przestrzeni VPN i działa od 2016 roku. Proton AG ma siedzibę w Szwajcarii i oferuje ograniczony bezpłatny plan, a także bardziej funkcjonalną opcję premium.

[:octicons-home-16: Strona główna](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title="Dokumentacja"}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>
- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://protonvpn.com/download-windows)
- [:simple-apple: macOS](https://protonvpn.com/download-macos)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 112 Krajów

Proton VPN ma [serwery w 112 krajach](https://protonvpn.com/vpn-servers) lub [5](https://protonvpn.com/support/how-to-create-free-vpn-account), jeśli korzystasz z ich [bezpłatnego planu](https://protonvpn.com/free-vpn/server).(1) Wybór dostawcy VPN z serwerem znajdującym się najbliżej Ciebie zmniejszy opóźnienia w wysyłanym ruchu sieciowym. Wynika to z krótszej trasy (mniej przeskoków) do miejsca docelowego.
{ .annotate }

1. Ostatnio sprawdzone: 2024-08-06

Uważamy również, że lepiej jest dla bezpieczeństwa kluczy prywatnych dostawcy VPN, jeśli korzysta on z [dedykowanych serwerów](https://en.wikipedia.org/wiki/Dedicated_hosting_service), zamiast tańszych rozwiązań współdzielonych (z innymi klientami), takich jak [wirtualne serwery prywatne](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Niezależny Audyt

W styczniu 2020 r. Proton VPN przeszedł niezależny audyt przeprowadzony przez SEC Consult. SEC Consult znalazł kilka luk średniego i niskiego ryzyka w aplikacjach Proton VPN dla systemów Windows, Android i iOS, z których wszystkie zostały "odpowiednio naprawione" przez Proton VPN przed opublikowaniem raportów. Żaden ze zidentyfikowanych błędów nie zapewniłby atakującemu zdalnego dostępu do urządzenia lub ruchu. Poszczególne raporty dla każdej platformy można wyświetlić na stronie [protonvpn.com.](https://protonvpn.com/blog/open-source) W kwietniu 2022 roku Proton VPN przeszedł [kolejny audyt](https://protonvpn.com/blog/no-logs-audit). [List atestacyjny](https://proton.me/blog/security-audit-all-proton-apps) został dostarczony dla aplikacji Proton VPN 9 listopada 2021 r. przez [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } Klienci Open-Source

Proton VPN udostępnia kod źródłowy ich aplikacji mobilnych i desktopowych na ich  [stronie GitHub](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Przyjmuje Gotówkę

Proton VPN, oprócz akceptowania kart kredytowych/debetowych, PayPal i [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), akceptuje również **gotówkę/walutę lokalną** jako anonimową formę płatności.

#### :material-check:{ .pg-green } Wsparcie WireGuard

Proton VPN obsługuje protokół WireGuard®. [WireGuard](https://wireguard.com) to nowszy protokół, który wykorzystuje najnowocześniejszą [kryptografię](https://wireguard.com/protocol). Ponadto WireGuard ma być prostszy i bardziej wydajny.

Proton VPN [zaleca](https://protonvpn.com/blog/wireguard) korzystanie z WireGuard w ramach swojej usługi. Proton VPN oferuje również generator konfiguracji WireGuard do użytku z oficjalnymi aplikacjami WireGuard [](https://wireguard.com/install).

#### :material-alert-outline:{ .pg-orange } Ograniczone Wsparcie IPv6

Proton [obsługuje teraz IPv6](https://protonvpn.com/support/prevent-ipv6-vpn-leaks) w swojej wtyczce przeglądarkowej i aplikacji Linux, ale tylko 80% ich serwerów jest kompatybilnych z IPv6. Na innych platformach klient Proton VPN zablokuje cały wychodzący ruch IPv6, więc nie musisz się martwić, że Twój adres IPv6 wycieknie, ale nie będziesz mógł połączyć się z żadnymi witrynami obsługującymi tylko IPv6, ani nie będziesz mógł połączyć się z Proton VPN z sieci obsługującej tylko IPv6.

#### :material-information-outline:{ .pg-info } Zdalne Przekierowanie Portów

Proton VPN obsługuje obecnie tylko efemeryczne zdalne [przekierowanie portów](https://protonvpn.com/support/port-forwarding) za pośrednictwem NAT-PMP,  z 60-sekundowym czasem dzierżawy. Oficjalne aplikacje dla systemów Windows i Linux zapewniają łatwy dostęp do tej opcji, podczas gdy w innych systemach operacyjnych konieczne będzie uruchomienie własnego [klienta NAT-PMP](https://protonvpn.com/support/port-forwarding-manual-setup). Aplikacje torrentowe często natywnie obsługują NAT-PMP.

#### :material-information-outline:{ .pg-blue } Anty-Cenzura

Proton VPN ma swój protokół [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol), który *może* pomóc w sytuacjach, w których protokoły VPN, takie jak OpenVPN lub WireGuard, są blokowane za pomocą różnych podstawowych technik. Stealth enkapsuluje tunel VPN w sesji TLS, aby wyglądał jak bardziej zwyczajny ruch internetowy.

Niestety, nie działa to zbyt dobrze w krajach, w których wdrożone są zaawansowane filtry analizujące cały ruch wychodzący w celu wykrycia zaszyfrowanych tuneli. Stealth jest dostępny na Androida, iOS, Windows i macOS, ale nie jest jeszcze dostępny na Linuksa.

#### :material-check:{ .pg-green } Aplikacje mobilne

Proton VPN opublikował klientów [App Store](https://apps.apple.com/app/id1437005085) i [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android), z których oba obsługują łatwy w użyciu interfejs, nie wymagający ręcznej konfiguracji połączenia WireGuard. Aplikacja na Androida jest również dostępna na [GitHub](https://github.com/ProtonVPN/android-app/releases).

<div class="admonition warning" markdown>
<p class="admonition-title">Jak zrezygnować z udostępniania danych telemetrycznych</p>

Na Androidzie Proton ukrywa ustawienia telemetrii pod myląco nazwanym menu "**Pomóż nam walczyć z cenzurą**" w panelu ustawień. Na innych platformach ustawienia te można znaleźć w menu "**Statystyki użytkowania**".

Zwracamy na to uwagę, ponieważ nie zalecamy udostępnianie anonimowych statystyk użytkowania deweloperom. Ważne jest, aby te ustawienia były łatwe do znalezienia i wyraźnie oznaczone.

</div>

#### :material-information-outline:{ .pg-blue } Dodatkowe Uwagi

Proton VPN obsługuje uwierzytelnianie dwuskładnikowe na wszystkich platformach. Proton VPN posiada własne serwery i centra danych w Szwajcarii, Islandii i Szwecji. Oferują blokowanie treści i blokowanie znanego złośliwego oprogramowania za pomocą swojej usługi DNS. Dodatkowo, Proton VPN oferuje również serwery "Tor" umożliwiające łatwe łączenie się z witrynami cebulowymi, ale nadal zdecydowanie zalecamy korzystanie z [oficjalnej przeglądarki Tor Browser](tor.md#tor-browser) do tego celu.

##### :material-alert-outline:{ .pg-orange } Funkcja Kill Switch nie działa na komputerach Mac z procesorami Intel

Podczas korzystania z funkcji Kill Switch VPN na komputerach Mac z procesorami Intel [mogą wystąpić](https://protonvpn.com/support/macos-t2-chip-kill-switch) awarie systemu. Jeśli wymagasz tej funkcji i korzystasz z komputera Mac z chipsetem Intel, powinieneś rozważyć skorzystanie z innej usługi VPN.

### IVPN

<div class="admonition recommendation" markdown>

![Logo IVPN](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** to kolejny dostawca VPN klasy premium, który działa od 2009 roku. IVPN ma siedzibę na Gibraltarze i nie oferuje bezpłatnego okresu próbnego.

[:octicons-home-16: Strona główna](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Polityka Prywatności" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title="Dokumentacja"}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-github: GitHub](https://github.com/ivpn/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 37 Krajów

IVPN posiada [serwery w 37 krajach](https://ivpn.net/status).(1) Wybór dostawcy VPN z serwerem znajdującym się najbliżej użytkownika zmniejszy opóźnienia w przesyłanym ruchu sieciowym. Wynika to z krótszej trasy (mniej przeskoków) do miejsca docelowego.
{ .annotate }

1. Ostatnio sprawdzone: 2024-08-06

Uważamy również, że lepiej jest dla bezpieczeństwa kluczy prywatnych dostawcy VPN, jeśli korzysta on z [dedykowanych serwerów](https://en.wikipedia.org/wiki/Dedicated_hosting_service), zamiast tańszych rozwiązań współdzielonych (z innymi klientami), takich jak [wirtualne serwery prywatne](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Niezależny Audyt

IVPN przeszła wiele [niezależnych audytów](https://ivpn.net/en/blog/tags/audit) od 2019 roku i publicznie ogłosiła swoje zobowiązanie do [corocznych audytów bezpieczeństwa.](https://ivpn.net/blog/ivpn-apps-security-audit-concluded)

#### :material-check:{ .pg-green } Klienci Open-Source

Od lutego 2020 r. [aplikacje IVPN są teraz Open-Source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). Kod źródłowy można uzyskać z ich [organizacji GitHub](https://github.com/ivpn).

#### :material-check:{ .pg-green } Akceptuje Gotówkę i Monero

Oprócz akceptowania kart kredytowych/debetowych i PayPal, IVPN akceptuje Bitcoin, **Monero** i **gotówkę/walutę lokalną** (w planach rocznych) jako anonimowe metody płatności. [Dostępne](https://ivpn.net/knowledgebase/billing/voucher-cards-faq) są również karty przedpłacone z kodami do realizacji.

#### :material-check:{ .pg-green } Wsparcie WireGuard

IVPN obsługuje protokół WireGuard®. [WireGuard](https://wireguard.com) to nowszy protokół, który wykorzystuje najnowocześniejszą [kryptografię](https://wireguard.com/protocol). Ponadto WireGuard ma być prostszy i bardziej wydajny.

IVPN [zaleca](https://ivpn.net/wireguard) korzystanie z WireGuard w swojej usłudze i jest domyślny we wszystkich aplikacjach IVPN. IVPN oferuje również generator konfiguracji WireGuard do użytku z oficjalnymi [aplikacjami](https://wireguard.com/install) WireGuard.

#### :material-information-outline:{ .pg-blue } Wsparcie IPv6

IVPN umożliwia [łączenie się z usługami przy użyciu protokołu IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6), ale nie pozwala na łączenie się z urządzenia przy użyciu adresu IPv6.

#### :material-alert-outline:{ .pg-orange } Zdalne Przekierowanie Portów

IVPN wcześniej obsługiwał przekierowanie portów, ale usunął tę opcję w [czerwcu 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding) roku. Brak tej funkcji może negatywnie wpłynąć na niektóre aplikacje, zwłaszcza aplikacje peer-to-peer, takie jak klienty torrent.

#### Anty-Cenzura

IVPN ma tryby zaciemniania przy użyciu [V2Ray](https://v2ray.com/en/index.html), które pomagają w sytuacjach, w których protokoły VPN, takie jak OpenVPN lub WireGuard, są blokowane. Obecnie funkcja ta jest dostępna tylko na komputerach stacjonarnych i [iOS](https://ivpn.net/knowledgebase/ios/v2ray). Ma dwa tryby, w których może używać [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) przez połączenia QUIC lub TCP. QUIC jest nowoczesnym protokołem z lepszą kontrolą przeciążenia, a zatem może być szybszy i mieć mniejsze opóźnienia. Tryb TCP sprawia, że dane wyglądają jak zwykły ruch HTTP.

#### :material-check:{ .pg-green } Klienci Mobilni

IVPN opublikował klientów [App Store](https://apps.apple.com/app/id1193122683) i [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), z których oba obsługują łatwy w użyciu interfejs, nie wymagający ręcznej konfiguracji połączenia WireGuard. Klient Android jest również dostępny na [GitHub](https://github.com/ivpn/android-app/releases).

#### :material-information-outline:{ .pg-blue } Dodatkowe Uwagi

Klienci IVPN obsługują uwierzytelnianie dwuskładnikowe. IVPN zapewnia również funkcję["AntiTracker](https://ivpn.net/antitracker)", która blokuje sieci reklamowe i trackery z poziomu sieci.

### Mullvad

<div class="admonition recommendation" markdown>

![Logo Mullvad](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** to szybka i niedroga sieć VPN, która kładzie duży nacisk na przejrzystość i bezpieczeństwo. Działają od 2009 roku. Mullvad ma siedzibę w Szwecji i oferuje 14-dniową gwarancję zwrotu pieniędzy dla [metod płatności](https://mullvad.net/en/help/refunds), które na to pozwalają.

[:octicons-home-16: Strona główna](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title="Dokumentacja"}
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pliki do pobrania</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 49 Krajów

Mullvad posiada [serwery w 49 krajach](https://mullvad.net/servers).(1) Wybór dostawcy VPN z serwerem znajdującym się najbliżej użytkownika zmniejszy opóźnienia w przesyłanym ruchu sieciowym. Wynika to z krótszej trasy (mniej przeskoków) do miejsca docelowego.
{ .annotate }

1. Ostatnio sprawdzone: 2025-03-10

Uważamy również, że lepiej jest dla bezpieczeństwa kluczy prywatnych dostawcy VPN, jeśli korzysta on z [dedykowanych serwerów](https://en.wikipedia.org/wiki/Dedicated_hosting_service), zamiast tańszych rozwiązań współdzielonych (z innymi klientami), takich jak [wirtualne serwery prywatne](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Niezależny audyt

Mullvad przeszedł wiele [niezależnych audytów](https://mullvad.net/en/blog/tag/audits) i publicznie ogłosił, że stara się przeprowadzać [coroczne audyty](https://mullvad.net/en/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) swoich aplikacji i infrastruktury.

#### :material-check:{ .pg-green } Klienci Open-Source

Mullvad udostępnia kod źródłowy swoich klientów stacjonarnych i mobilnych na ich [GitHubie.](https://github.com/mullvad/mullvadvpn-app)

#### :material-check:{ .pg-green } Akceptuje Gotówkę i Monero

Mullvad, oprócz akceptowania kart kredytowych/debetowych i PayPal, akceptuje Bitcoin, Bitcoin Cash, **Monero** i **gotówkę/walutę lokalną** jako anonimowe formy płatności. Dostępne są również karty przedpłacone z kodami do realizacji. Mullvad akceptuje również przelewy Swish i bankowe, a także kilka europejskich systemów płatności.

#### :material-check:{ .pg-green } Wsparcie WireGuard

Mullvad obsługuje protokół WireGuard®. [WireGuard](https://wireguard.com) to nowszy protokół, który wykorzystuje najnowocześniejszą [kryptografię](https://wireguard.com/protocol). Ponadto WireGuard ma być prostszy i bardziej wydajny.

Mullvad [zaleca](https://mullvad.net/en/help/why-wireguard) używanie WireGuard z ich usługą. Jest to domyślny lub jedyny protokół w aplikacjach Mullvad, iOS, macOS i Linux, ale w systemie Windows musisz [ręcznie włączyć](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Mullvad oferuje również generator konfiguracji WireGuard do użytku z oficjalnymi [aplikacjami](https://wireguard.com/install) WireGuard.

#### :material-check:{ .pg-green } Wsparcie IPv6

Mullvad umożliwia [dostęp do usług hostowanych na IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) i łączenie się z urządzenia korzystającego z adresu IPv6.

#### :material-alert-outline:{ .pg-orange } Zdalne przekierowanie portów

Mullvad wcześniej obsługiwał przekierowanie portów, ale usunął tę opcję w [maju 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports) roku. Brak tej funkcji może negatywnie wpłynąć na niektóre aplikacje, zwłaszcza aplikacje peer-to-peer, takie jak klienty torrent.

#### :material-check:{ .pg-green } Anty-Cenzura

Mullvad oferuje kilka funkcji, które pomagają ominąć cenzurę i uzyskać swobodny dostęp do Internetu:

- **Tryby zaciemniania**: Mullvad posiada dwa wbudowane tryby obfuskacji: ["](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard)UDP-over-TCP" i ["WireGuard over Shadowsocks"](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard). Tryby te ukrywają ruch VPN jako zwykły ruch internetowy, utrudniając cenzorom wykrywanie i blokowanie. Podobno Chiny muszą użyć [nowej metody, aby zakłócić ruch kierowany przez Shadowsocks](https://gfw.report/publications/usenixsecurity23/en).
- **Zaawansowane zaciemnianie za pomocą Shadowsocks i v2ray**: Dla bardziej zaawansowanych użytkowników Mullvad zapewnia przewodnik na temat korzystania z wtyczki [Shadowsocks z v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) z klientami Mullvad. Ta konfiguracja zapewnia dodatkową warstwę zaciemniania i szyfrowania.
- **Niestandardowe adresy IP serwerów**: Aby przeciwdziałać blokowaniu adresów IP, możesz poprosić zespół pomocy technicznej Mullvad o niestandardowe adresy IP serwerów. Po otrzymaniu niestandardowych adresów IP można wprowadzić plik tekstowy w ustawieniach "Zastępowanie adresów IP serwera", co spowoduje zastąpienie wybranych adresów IP serwera adresami, które nie są znane cenzorowi.
- **Mosty i serwery proxy**: Mullvad umożliwia również korzystanie z mostów lub serwerów proxy w celu uzyskania dostępu do interfejsu API (potrzebnego do uwierzytelniania), co może pomóc w ominięciu prób cenzury, które blokują dostęp do samego interfejsu API.

#### :material-check:{ .pg-green } Klienci Mobilni

Mullvad opublikował klientów [App Store](https://apps.apple.com/app/id1488466513) i [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn), z których oba obsługują łatwy w użyciu interfejs, nie wymagający ręcznej konfiguracji połączenia WireGuard. Klient Android jest również dostępny na [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Dodatkowe Uwagi

Mullvad jest bardzo przejrzysty, jeśli chodzi o węzły, które [posiada lub wynajmuje](https://mullvad.net/en/servers). Zapewniają one również opcję włączenia w swoich aplikacjach funkcji Defense Against AI-guided Traffic Analysis[(DAITA](https://mullvad.net/en/blog/daita-defense-against-ai-guided-traffic-analysis)). DAITA chroni przed zagrożeniami związanymi z zaawansowaną analizą ruchu, która może być wykorzystywana do łączenia wzorców w ruchu VPN z określonymi stronami internetowymi.

## Kryteria

<div class="admonition danger" markdown>
<p class="admonition-title">Zagrożenie</p>

Ważne jest, aby pamiętać, że korzystanie z usług dostawcy VPN nie zapewni anonimowości, ale zapewni lepszą prywatność w niektórych sytuacjach. VPN nie jest narzędziem do nielegalnych działań. Nie polegaj na polityce "no log".

</div>

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas dostawców. Pozwala nam to zapewnić całkowicie obiektywne rekomendacje.** Oprócz [naszych standardowych kryteriów](about/criteria.md), opracowaliśmy jasny zestaw wymagań dla każdego dostawcy VPN, który chce być rekomendowany, w tym silne szyfrowanie, niezależne audyty bezpieczeństwa, nowoczesną technologię i wiele innych. Zalecamy zapoznanie się z tą listą przed wyborem dostawcy VPN i przeprowadzenie własnych badań, aby upewnić się, że wybrany dostawca VPN jest tak godny zaufania, jak to tylko możliwe.

### Technologia

Wymagamy, aby wszyscy nasi rekomendowani dostawcy VPN dostarczali standardowe pliki konfiguracyjne, które mogą być używane w ogólnym kliencie open-source. **Jeśli** VPN udostępnia własnego klienta, wymagamy kill switch, aby zablokować wycieki danych sieciowych po rozłączeniu.

**Minimum do zakwalifikowania się:**

- Obsługa silnych protokołów, takich jak WireGuard.
- Kill Switch wbudowany w klientów.
- Wsparcie Wielokrotnego Przeskoku. Wielokrotny Przeskok jest ważny, aby zachować prywatność danych w przypadku naruszenia bezpieczeństwa pojedynczego węzła.
- Jeśli klienci VPN są dostarczani, powinni być [open source](https://en.wikipedia.org/wiki/Open_source), podobnie jak oprogramowanie VPN, które zazwyczaj jest w nich wbudowane. Uważamy, że dostępność [kodu źródłowego](https://en.wikipedia.org/wiki/Source_code) zapewnia większą przejrzystość tego, co program faktycznie robi.
- Funkcje odporności na cenzurę zaprojektowane do omijania zapór sieciowych bez DPI.

**Najlepszy scenariusz:**

- Kill Switch z wysoce konfigurowalnymi opcjami (włączanie/wyłączanie w określonych sieciach, podczas uruchamiania itp.)
- Łatwe w użyciu klienty VPN
- Obsługa protokołu [IPv6](https://en.wikipedia.org/wiki/IPv6). Oczekujemy, że serwery będą zezwalać na połączenia przychodzące przez IPv6 i umożliwiać dostęp do usług hostowanych na adresach IPv6.
- Możliwość [zdalnego przekierowania portów](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) pomaga w tworzeniu połączeń podczas korzystania z oprogramowania do udostępniania plików P2P[(Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) lub hostowania serwera (np. Mumble).
- Technologia zaciemniania, która kamufluje prawdziwą naturę ruchu internetowego, zaprojektowana w celu obejścia zaawansowanych metod cenzury internetowej, takich jak DPI.

### Prywatność

Preferujemy, aby nasi rekomendowani dostawcy gromadzili jak najmniej danych. Wymagane jest nie gromadzenie danych osobowych podczas rejestracji i akceptowanie anonimowych form płatności.

**Minimum do zakwalifikowania się:**

- [Anonimowa kryptowaluta](cryptocurrency.md) **lub** opcja płatności gotówką.
- Do rejestracji nie są wymagane żadne dane osobowe: Co najwyżej nazwa użytkownika, hasło i adres e-mail.

**Najlepszy scenariusz:**

- Akceptuje wiele [anonimowych opcji płatności](advanced/payments.md).
- Brak akceptacji danych osobowych (automatycznie generowana nazwa użytkownika, brak wymogu podania adresu e-mail itp.)

### Bezpieczeństwo

VPN nie ma sensu, jeśli nie może nawet zapewnić odpowiedniego bezpieczeństwa. Od wszystkich rekomendowanych przez nas dostawców wymagamy przestrzegania aktualnych standardów bezpieczeństwa. Idealnie byłoby, gdyby domyślnie używały bardziej przyszłościowych schematów szyfrowania. Wymagamy również, aby niezależna strona trzecia przeprowadziła audyt bezpieczeństwa dostawcy, najlepiej w bardzo kompleksowy sposób i w sposób powtarzalny (corocznie).

**Minimum do zakwalifikowania się:**

- Silne schematy szyfrowania: OpenVPN z uwierzytelnianiem SHA-256; RSA-2048 lub lepszy handshake; szyfrowanie danych AES-256-GCM lub AES-256-CBC.
- Utajnianie z wyprzedzeniem.
- Opublikowane audyty bezpieczeństwa przeprowadzone przez renomowaną firmę zewnętrzną.
- Serwery VPN wykorzystujące szyfrowanie pełnodyskowe lub tylko pamięć RAM.

**Najlepszy scenariusz:**

- Najsilniejsze szyfrowanie: RSA-4096.
- Opcjonalne szyfrowanie odporne na kwanty.
- Kompleksowe audyty bezpieczeństwa publikowane przez renomowaną firmę zewnętrzną.
- Programy Bug-Bounty i/lub skoordynowany proces ujawniania luk w zabezpieczeniach.
- Serwery VPN działające tylko w RAM.

### Zaufanie

Nie powierzyłbyś swoich finansów komuś z fałszywą tożsamością, więc po co powierzać mu swoje dane internetowe? Wymagamy, aby rekomendowani przez nas dostawcy publicznie informowali o swojej własności lub przywództwie. Chcielibyśmy również widzieć częste raporty przejrzystości, zwłaszcza w odniesieniu do sposobu obsługi wniosków rządowych.

**Minimum do zakwalifikowania się:**

- Publiczne przywództwo lub własność.
- Firma z siedzibą w jurysdykcji, w której nie można jej zmusić do prowadzenia tajnych rejestrów.

**Najlepszy scenariusz:**

- Publiczne przywództwo.
- Częste raporty przejrzystości.

### Marketing

W przypadku polecanych przez nas dostawców VPN lubimy widzieć odpowiedzialny marketing.

**Minimum do zakwalifikowania się:**

- Musi samodzielnie hostować analitykę (tj. bez Google Analytics).

Nie może mieć żadnego marketingu, który jest nie odpowiedzialny.

- Gwarantując ochronę anonimowości w 100%. Kiedy ktoś twierdzi, że coś jest w 100%, oznacza to, że nie ma pewności co do niepowodzenia. Wiemy, że ludzie mogą dość łatwo pozbawić się anonimowości na wiele sposobów, np:
    - Ponowne wykorzystanie danych osobowych (np. kont e-mail, unikalnych pseudonimów itp.), do których uzyskali dostęp bez oprogramowania zapewniającego anonimowość (Tor, VPN itp.).
    - [Browser Fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Twierdzenie, że pojedynczy obwód VPN jest "bardziej anonimowy" niż Tor, który jest obwodem składającym się z trzech lub więcej węzłów, które regularnie się zmieniają.
- Używaj odpowiedzialnego języka: tzn. w porządku jest powiedzieć, że VPN jest "odłączony" lub "niepodłączony", jednak twierdzenie, że ktoś jest "narażony", "podatny na ataki" lub "zagrożony" jest niepotrzebnym użyciem alarmującego języka, który może być niepoprawny. Na przykład, osoba ta może po prostu korzystać z usługi innego dostawcy VPN lub używać sieci Tor.

**Najlepszy scenariusz:**

Odpowiedzialny marketing, który jest zarówno edukacyjny, jak i użyteczny dla konsumenta, może obejmować:

- Dokładne porównanie, kiedy zamiast tego powinien być używany [Tor](tor.md).
- Dostępność strony internetowej dostawcy VPN za pośrednictwem [ usługi .onion](https://en.wikipedia.org/wiki/.onion)

### Dodatkowa funkcjonalność

Chociaż nie są to ścisłe wymagania, istnieją pewne czynniki, które wzięliśmy pod uwagę przy określaniu, których dostawców polecić. Obejmują one funkcje blokowania treści, kanały ostrzegawcze, doskonałą obsługę klienta, liczbę dozwolonych jednoczesnych połączeń itp.
