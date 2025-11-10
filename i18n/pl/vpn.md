---
meta_title: "Zalecenia i porównanie prywatnych usług VPN, bez sponsorów i reklam – Privacy Guides"
title: Usługi VPN
icon: material/vpn
description: Najlepsze usługi VPN chroniące Twoją prywatność i bezpieczeństwo w sieci. Znajdź dostawcę, który nie śledzi tego, co robisz.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-account-cash: Kapitalizm inwigilacji](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Jeżeli chcesz zwiększyć swoją *prywatność* wobec dostawcy Internetu, podczas korzystania z publicznej sieci Wi-Fi lub przy pobieraniu plików z torrentów, **VPN** może być rozwiązaniem dla Ciebie.

<div class="admonition danger" markdown>
<p class="admonition-title">VPN nie zapewnia anonimowości</p>

Korzystanie z VPN **nie** uczyni Twojej aktywności w sieci anonimową ani nie zwiększy bezpieczeństwa niezabezpieczonego ruchu (HTTP).

Jeśli zależy Ci na **anonimowości**, skorzystaj z przeglądarki Tor Browser. Jeśli zależy Ci na dodatkowym **bezpieczeństwie**, zawsze upewnij się, że łączysz się z witrynami za pomocą HTTPS. VPN nie zastępuje dobrych praktyk w zakresie bezpieczeństwa.

[Wprowadzenie do Tor Browser](tor.md#tor-browser){ .md-button .md-button--primary } [Mity dot. sieci Tor i FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Szczegółowy przegląd VPN :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Zalecani dostawcy

Zalecani przez nas dostawcy stosują szyfrowanie, obsługują WireGuard i OpenVPN oraz mają politykę braku logów. Szczegóły znajdziesz w naszej [pełnej liście kryteriów](#criteria).

| Dostawca              | Kraje | WireGuard                     | Przekierowanie portów                                     | IPv6                                                            | Płatności anonimowe          |
| --------------------- | ----- | ----------------------------- | --------------------------------------------------------- | --------------------------------------------------------------- | ---------------------------- |
| [Proton](#proton-vpn) | 127+  | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Częściowe wsparcie | :material-information-outline:{ .pg-blue } Ograniczone wsparcie | Cash  Monero via third party |
| [IVPN](#ivpn)         | 41+   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                    | :material-information-outline:{ .pg-blue } Tylko wychodzące     | Monero  Cash                 |
| [Mullvad](#mullvad)   | 49+   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                    | :material-check:{ .pg-green }                                   | Monero  Cash                 |

### Proton VPN

<div class="admonition recommendation" markdown>

![Logo Proton VPN](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** to mocny gracz na rynku VPN, działający od 2016 roku. Firma Proton AG ma siedzibę w Szwajcarii i oferuje zarówno ograniczoną darmową wersję, jak i pełniejszą wersję premium.

[:octicons-home-16: Strona główna](https://protonvpn.com/pl){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/pl/privacy-policy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://protonvpn.com/support/pl){ .card-link title="Dokumentacja" }
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

#### :material-check:{ .pg-green } 127 krajów

Proton VPN posiada [serwery w 127 krajach](https://protonvpn.com/pl/vpn-servers)(1) lub [10](https://protonvpn.com/support/pl/how-to-create-free-vpn-account), jeśli korzystasz z [darmowego planu](https://protonvpn.com/blog/pl/product-roadmap-winter-2025-2026).(2) Wybór dostawcy VPN z serwerem znajdującym się najbliżej Ciebie zmniejsza opóźnienia przesyłanych danych, ponieważ trasa do celu jest krótsza (mniej „przeskoków”).
{ .annotate }

1. Co najmniej 71 z nich to serwery wirtualne, co oznacza, że Twój adres IP będzie wskazywał dany kraj, ale serwer znajduje się tak naprawdę w innym. Dodatkowo 12 lokalizacji oferuje zarówno serwery fizyczne, jak i wirtualne. [Źródło](https://protonvpn.com/support/pl/how-smart-routing-works)
2. Stan na dzień: 28.10.2025

Uważamy też, że dla bezpieczeństwa kluczy prywatnych dostawcy VPN lepiej jest stosować [serwery dedykowane](https://en.wikipedia.org/wiki/Dedicated_hosting_service), zamiast tańszych rozwiązań współdzielonych z innymi klientami, takich jak [wirtualne serwery prywatne (VPS)](https://pl.wikipedia.org/wiki/Virtual_private_serverr).

#### :material-check:{ .pg-green } Niezależnie audytowany

Independent security researcher Ruben Santamarta conducted audits for Proton VPN's [browser extensions](https://drive.proton.me/urls/RWDD2SHT98#v7ZrwNcafkG8) and [apps](https://drive.proton.me/urls/RVW8TXG484#uTXX5Fc9GADo) in September 2024 and January 2025, respectively. Proton VPN's infrastrcture has undergone [annual audits](https://protonvpn.com/blog/no-logs-audit) by Securitum since 2022.

Previously, Proton VPN underwent an independent audit by SEC Consult in January 2020. Audyt wykazał kilka luk o średnim i niskim ryzyku w aplikacjach Proton VPN dla systemów Windows, Android i iOS, które zostały „należycie naprawione” przez Proton VPN przed publikacją raportów. Żaden ze znalezionych problemów nie mógł umożliwić atakującemu zdalnego dostępu do Twojego urządzenia ani ruchu sieciowego. Poszczególne raporty dla każdej platformy można znaleźć w ich dedykowanym [wpisie na blogu](https://web.archive.org/web/20250307041036/https://protonvpn.com/blog/open-source) na ten audytu.

#### :material-check:{ .pg-green } Oprogramowanie typu open source

Proton VPN udostępnia kod źródłowy swoich aplikacji desktopowych i mobilnych w serwisie [GitHub](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Akceptuje płatności gotówką

Proton VPN, oprócz kart kredytowych i debetowych, PayPala i [Bitcoina](advanced/payments.md#other-coins-bitcoin-ethereum-etc), akceptuje również **gotówkę/lokalną walutę** jako anonimową formę płatności. You can also use [**Monero**](cryptocurrency.md#monero) to purchase vouchers for Proton VPN Plus and Proton Unlimited via their [official](https://discuss.privacyguides.net/t/add-monero-as-an-anonymous-payment-method-for-proton-services/31058/15) reseller [ProxyStore](https://dys2p.com/en/2025-09-09-proton.html).

#### :material-check:{ .pg-green } Obsługa WireGuard

Proton VPN obsługuje protokół WireGuard®. [WireGuard](https://wireguard.com) to nowszy protokół wykorzystujący nowoczesną [kryptografię](https://wireguard.com/protocol). Ponadto WireGuard został zaprojektowany tak, aby był prostszy i bardziej wydajny.

Proton VPN [zaleca](https://protonvpn.com/blog/wireguard) korzystanie z WireGuard w swojej usłudze. Proton VPN oferuje również generator konfiguracji WireGuard do użycia z oficjalnymi [aplikacjami WireGuard](https://wireguard.com/install).

#### :material-alert-outline:{ .pg-orange } Ograniczona obsługa IPv6

Proton [obsługuje teraz IPv6](https://protonvpn.com/support/pl/prevent-ipv6-vpn-leaks) w rozszerzeniu do przeglądarki i aplikacji na Linuksa, ale tylko 80% ich serwerów jest kompatybilnych z IPv6. Na innych platformach klient Proton VPN blokuje cały wychodzący ruch IPv6, dzięki czemu nie musisz obawiać się wycieku swojego adresu IPv6, ale nie będziesz mógł łączyć się z witrynami działającymi wyłącznie w IPv6 ani korzystać z Proton VPN w sieci obsługującej tylko IPv6.

#### :material-information-outline:{ .pg-info } Zdalne przekierowanie portów

Proton VPN obecnie obsługuje jedynie efemeryczne zdalne [przekierowanie portów](https://protonvpn.com/support/pl/port-forwarding) poprzez NAT-PMP, z 60-sekundowym czasem dzierżawy. Oficjalne aplikacje dla systemów Windows i Linux oferują łatwo dostępne opcje konfiguracji, natomiast na innych systemach operacyjnych konieczne jest uruchomienie własnego [klienta NAT-PMP](https://protonvpn.com/support/pl/port-forwarding-manual-setup). Aplikacje do torrentów często obsługują NAT-PMP natywnie.

#### :material-information-outline:{ .pg-blue } Ochrona przed cenzurą

Proton VPN oferuje protokół [Stealth](https://protonvpn.com/blog/pl/stealth-vpn-protocol), który *może* pomóc w sytuacjach, gdy protokoły VPN, takie jak OpenVPN czy WireGuard, są blokowane przez różne proste metody. Stealth hermetyzuje tunel VPN w sesji TLS, aby wyglądał jak zwykły ruch internetowy.

Niestety, nie sprawdza się dobrze w krajach, które stosują zaawansowane filtry analizujące cały wychodzący ruch w celu wykrycia tuneli szyfrowanych. Stealth jest dostępny na systemach Android, iOS, Windows i macOS, ale nie jest jeszcze dostępny na Linuksa.

#### :material-check:{ .pg-green } Aplikacje mobilne

Proton VPN udostępnia aplikacje w [App Store](https://apps.apple.com/app/id1437005085) i [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android), oferujące łatwy w obsłudze interfejs, bez konieczności ręcznej konfiguracji połączenia WireGuard. Aplikacja na Androida dostępna jest również na [GitHubie](https://github.com/ProtonVPN/android-app/releases).

<div class="admonition warning" markdown>
<p class="admonition-title">Jak zrezygnować z udostępniania telemetrii</p>

Na Androidzie ustawienia telemetrii ukryte są w menu myląco nazwanym „**Pomóż nam w walce z cenzurą**” w panelu ustawień. Na innych platformach ustawienia te znajdują się w menu „**Statystyki użytkowania**”.

Warto o tym wspomnieć, ponieważ choć niekoniecznie odradzamy dzielenie się anonimowymi statystykami z deweloperami, ważne jest, aby te ustawienia były łatwo dostępne i jasno opisane.

</div>

#### :material-information-outline:{ .pg-blue } Dodatkowe uwagi

Aplikacje Proton VPN obsługują uwierzytelnianie dwuskładnikowe na wszystkich platformach. Proton VPN posiada własne serwery i centra danych w Szwajcarii, Islandii i Szwecji. Usługa oferuje blokowanie treści oraz znanego złośliwego oprogramowania poprzez serwery DNS. Dodatkowo Proton VPN udostępnia serwery „Tor”, umożliwiające łatwe łączenie się z witrynami .onion, choć wciąż zdecydowanie zalecamy korzystanie z [oficjalnej przeglądarki Tor Browser](tor.md#tor-browser) w tym celu.

##### :material-alert-outline:{ .pg-orange } Funkcja Kill Switch nie działa poprawnie na komputerach Mac z procesorami Intel

Na komputerach Mac z procesorami Intel użycie funkcji Kill Kwitch VPN [może prowadzić do awarii systemu](https://protonvpn.com/support/pl/macos-t2-chip-kill-switch). Jeśli potrzebujesz tej funkcji i korzystasz z Maca z chipsetem Intel, warto rozważyć użycie innej usługi VPN.

### IVPN

<div class="admonition recommendation" markdown>

![Logo IVPN](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** to kolejny dostawca usługi VPN klasy premium, działający od 2009 roku. Siedziba firmy znajduje się na Gibraltarze, a usługa nie oferuje bezpłatnego okresu próbnego.

[:octicons-home-16: Strona główna](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title="Dokumentacja" }
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

#### :material-check:{ .pg-green } 41 krajów

IVPN posiada [serwery w 41 krajach](https://ivpn.net/status).(1) Wybór dostawcy VPN z serwerem znajdującym się najbliżej Ciebie zmniejsza opóźnienia przesyłanych danych, ponieważ trasa do celu jest krótsza (mniej „przeskoków”).
{ .annotate }

1. Stan na dzień: 28.10.2025

Uważamy też, że dla bezpieczeństwa kluczy prywatnych dostawcy VPN lepiej jest stosować [serwery dedykowane](https://en.wikipedia.org/wiki/Dedicated_hosting_service), zamiast tańszych rozwiązań współdzielonych z innymi klientami, takich jak [wirtualne serwery prywatne (VPS)](https://pl.wikipedia.org/wiki/Virtual_private_serverr).

#### :material-check:{ .pg-green } Niezależnie audytowany

IVPN od 2019 roku przeszedł kilka [niezależnych audytów](https://ivpn.net/en/blog/tags/audit) i publicznie zadeklarował zobowiązanie do [corocznych audytów bezpieczeństwa](https://ivpn.net/blog/ivpn-apps-security-audit-concluded).

#### :material-check:{ .pg-green } Oprogramowanie typu open source

Od lutego 2020 roku [aplikacje IVPN są dostępne jako open source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). Kod źródłowy można znaleźć na ich profilu na [GitHubie](https://github.com/ivpn).

#### :material-check:{ .pg-green } Akceptuje płatności gotówką i Monero

Oprócz płatności kartą kredytową/debetową i PayPalem IVPN przyjmuje również płatności w Bitcoinach, **Monero** oraz **gotówce/walucie lokalnej** (w przypadku planów rocznych) jako anonimowe formy płatności. Można również użyć [kart przedpłaconych](https://ivpn.net/knowledgebase/billing/voucher-cards-faq) z kodami.

#### :material-check:{ .pg-green } Obsługa WireGuard

IVPN obsługuje protokół WireGuard®. [WireGuard](https://wireguard.com) to nowszy protokół wykorzystujący nowoczesną [kryptografię](https://wireguard.com/protocol). Ponadto WireGuard został zaprojektowany tak, aby był prostszy i bardziej wydajny.

IVPN [zaleca](https://ivpn.net/wireguard) korzystanie z WireGuard w swojej usłudze, dlatego jest to domyślny protokół we wszystkich aplikacjach IVPN. IVPN oferuje również generator konfiguracji WireGuard do użycia z oficjalnymi [aplikacjami WireGuard](https://wireguard.com/install).

#### :material-information-outline:{ .pg-blue } Obsługa IPv6

IVPN umożliwia [łączenie się z usługami za pomocą IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6), ale nie pozwala na ustanowienie połączenia z urządzenia korzystającego z adresu IPv6.

#### :material-alert-outline:{ .pg-orange } Zdalne przekierowanie portów

IVPN wcześniej oferował funkcję przekierowywania portów, jednak została ona usunięta w [czerwcu 2023 roku](https://ivpn.net/blog/gradual-removal-of-port-forwarding). Brak tej funkcji może negatywnie wpływać na działanie niektórych aplikacji, szczególnie tych opartych na komunikacji peer-to-peer, takich jak klienty torrentów.

#### :material-check:{ .pg-green } Ochrona przed cenzurą

IVPN oferuje tryby zaciemniania ruchu z wykorzystaniem [V2Ray](https://v2ray.com/en/index.html), co jest przydatne w sytuacjach, gdy protokoły VPN, takie jak OpenVPN czy WireGuard, są blokowane. Obecnie ta funkcja dostępna jest tylko na komputerach stacjonarnych i urządzeniach z systemem [iOS](https://ivpn.net/knowledgebase/ios/v2ray). Dostępne są dwa tryby działania: z użyciem [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) przez połączenia QUIC lub TCP. QUIC to nowoczesny protokół z lepszą kontrolą przeciążenia, co może przekładać się na wyższą prędkość i mniejsze opóźnienia. Tryb TCP sprawia, że Twój ruch sieciowy wygląda jak zwykły ruch HTTP.

#### :material-check:{ .pg-green } Aplikacje mobilne

IVPN udostępnia aplikacje w [App Store](https://apps.apple.com/app/id1193122683) oraz [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), obie z prostym w obsłudze interfejsem, który eliminuje konieczność ręcznej konfiguracji połączenia WireGuard. Aplikacja na Androida dostępna jest również na [GitHubie](https://github.com/ivpn/android-app/releases).

#### :material-information-outline:{ .pg-blue } Dodatkowe uwagi

Aplikacje IVPN obsługują uwierzytelnianie dwuskładnikowe. IVPN oferuje także funkcję „[AntiTracker](https://ivpn.net/antitracker)”, która blokuje sieci reklamowe i trackery już na poziomie sieciowym.

### Mullvad

<div class="admonition recommendation" markdown>

![Logo Mullvad](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** to szybka i niedroga usługa VPN, która kładzie duży nacisk na przejrzystość i bezpieczeństwo. Działa od 2009 roku. Siedziba firmy znajduje się w Szwecji, a użytkownicy mogą skorzystać z 14-dniowej gwarancji zwrotu pieniędzy dla [metod płatności](https://mullvad.net/pl/help/refunds), które na to pozwalają.

[:octicons-home-16: Strona główna](https://mullvad.net/pl){ .md-button .md-button--primary }
[:simple-torbrowser:]
(http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Usługa onion" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:fontawesome-brands-windows: Windows](https://mullvad.net/pl/download/windows)
- [:simple-apple: macOS](https://mullvad.net/pl/download/macos)
- [:simple-linux: Linux](https://mullvad.net/pl/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 49 krajów

Mullvad posiada [serwery w 49 krajach](https://mullvad.net/servers).(1) Wybór dostawcy VPN z serwerem znajdującym się najbliżej Ciebie zmniejsza opóźnienia przesyłanych danych, ponieważ trasa do celu jest krótsza (mniej „przeskoków”).
{ .annotate }

1. Stan na dzień: 28.10.2025

Uważamy też, że dla bezpieczeństwa kluczy prywatnych dostawcy VPN lepiej jest stosować [serwery dedykowane](https://en.wikipedia.org/wiki/Dedicated_hosting_service), zamiast tańszych rozwiązań współdzielonych z innymi klientami, takich jak [wirtualne serwery prywatne (VPS)](https://pl.wikipedia.org/wiki/Virtual_private_serverr).

#### :material-check:{ .pg-green } Niezależnie audytowany

Mullvad przeszedł liczne [niezależne audyty](https://mullvad.net/pl/blog/tag/audits) i publicznie zadeklarował zamiar przeprowadzania [corocznych audytów](https://mullvad.net/pl/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) swoich aplikacji i infrastruktury.

#### :material-check:{ .pg-green } Oprogramowanie typu open source

Mullvad udostępnia kod źródłowy swoich aplikacji desktopowych i mobilnych w serwisie [GitHub](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Akceptuje płatności gotówką i Monero

Oprócz płatności kartą kredytową/debetową i PayPalem, Mullvad przyjmuje również płatności Bitcoin, Bitcoin Cash, **Monero** oraz **gotówką/walutą lokalną** jako anonimowe formy płatności. Można również użyć [kart przedpłaconych](https://mullvad.net/en/help/partnerships-and-resellers) z kodami. Mullvad akceptuje ponadto płatności za pośrednictwem Swish, przelewów bankowych oraz kilku europejskich systemów płatności w tym Przelewy24.

#### :material-check:{ .pg-green } Obsługa WireGuard

Mullvad obsługuje protokół WireGuard®. [WireGuard](https://wireguard.com) to nowszy protokół wykorzystujący nowoczesną [kryptografię](https://wireguard.com/protocol). Ponadto WireGuard został zaprojektowany tak, aby był prostszy i bardziej wydajny.

Mullvad [zaleca](https://mullvad.net/pl/help/why-wireguard) korzystanie z WireGuard w swojej usłudze. Jest to jedyny obsługiwany protokół przez ich aplikacje mobilne, a w wersjach desktopowych wsparcie dla OpenVPN zostanie [zakończone](https://mullvad.net/pl/blog/reminder-that-openvpn-is-being-removed) w 2025 roku. Serwery Mullvad przestaną akceptować połączenia OpenVPN najpóźniej 15 stycznia 2026 roku. Mullvad oferuje również generator konfiguracji WireGuard do użycia z oficjalnymi [aplikacjami WireGuard](https://wireguard.com/install).

#### :material-check:{ .pg-green } Obsługa IPv6

Mullvad umożliwia [korzystanie z usług działających w sieci IPv6](https://mullvad.net/pl/blog/2014/9/15/ipv6-support) oraz łączenie się z niej bezpośrednio z urządzeń obsługujących adresy IPv6.

#### :material-alert-outline:{ .pg-orange } Zdalne przekierowanie portów

Mullvad wcześniej oferował funkcję przekierowywania portów, jednak została ona usunięta w [maju 2023 roku](https://mullvad.net/pl/blog/2023/5/29/removing-the-support-for-forwarded-ports). Brak tej funkcji może negatywnie wpływać na działanie niektórych aplikacji, szczególnie tych opartych na komunikacji peer-to-peer, takich jak klienty torrentów.

#### :material-check:{ .pg-green } Ochrona przed cenzurą

Mullvad oferuje szereg funkcji pomagających omijać cenzurę i swobodnie uzyskiwać dostęp do Internetu:

- **Tryby zaciemniania ruchu**: Mullvad udostępnia dwa wbudowane tryby zaciemniania — „UDP-over-TCP” oraz [„WireGuard over Shadowsocks”](https://mullvad.net/pl/blog/introducing-shadowsocks-obfuscation-for-wireguard). Tryby te maskują ruch VPN, sprawiając, że wygląda on jak zwykły ruch WWW, co utrudnia jego wykrycie i zablokowanie przez cenzurę. Według niektórych informacji Chiny muszą stosować [nowe metody zakłócania ruchu przez Shadowsocks](https://gfw.report/publications/usenixsecurity23/en).
- **Zaawansowane zaciemnianie z użyciem Shadowsocks i v2ray**: Dla bardziej zaawansowanych użytkowników Mullvad przygotował przewodnik, jak korzystać z wtyczki [Shadowsocks z v2ray](https://mullvad.net/pl/help/shadowsocks-with-v2ray) w połączeniu z klientem Mullvad. Takie rozwiązanie zapewnia dodatkową warstwę zaciemniania i szyfrowania.
- **Niestandardowe adresy IP serwerów**: Aby obejść blokowanie adresów IP, użytkownicy mogą poprosić zespół pomocy technicznej Mullvad o przydzielenie niestandardowych adresów IP. Po otrzymaniu niestandardowych adresów IP możesz wprowadzić plik tekstowy w ustawieniach w sekcji „Server IP override” (Zastępowanie adresu IP serwera), co spowoduje nadpisanie wybranych adresów IP serwerów adresami nieznanymi cenzurze.
- **Mostki i serwery proxy**: Mullvad umożliwia również korzystanie z mostków lub serwerów proxy do uzyskania dostępu do swojego interfejsu API (wymaganego do uwierzytelnienia), co pomaga w obejściu prób cenzury blokujących połączenia z API.

#### :material-check:{ .pg-green } Aplikacje mobilne

Mullvad udostępnia aplikacje w [App Store](https://apps.apple.com/app/id1488466513) oraz [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn), obie z prostym w obsłudze interfejsem, który eliminuje konieczność ręcznej konfiguracji połączenia WireGuard. Aplikacja na Androida dostępna jest również na [GitHubie](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Dodatkowe uwagi

Mullvad zachowuje pełną przejrzystość w kwestii tego, które węzły [posiada, a które wynajmuje](https://mullvad.net/pl/servers). Dodatkowo w aplikacjach dostępna jest opcja włączenia funkcji Defense Against AI-guided Traffic Analysis ([DAITA](https://mullvad.net/pl/blog/daita-defense-against-ai-guided-traffic-analysis)). DAITA chroni przed zaawansowaną analizą ruchu sieciowego, która może być wykorzystywana do powiązania wzorców ruchu VPN z konkretnymi odwiedzanymi stronami internetowymi.

## Kryteria

<div class="admonition danger" markdown>
<p class="admonition-title">Zagrożenie</p>

Ważne jest, aby pamiętać, że korzystanie z dostawcy usługi VPN nie czyni Cię anonimowym, choć w pewnych sytuacjach zwiększy Twoją prywatność. VPN nie jest narzędziem do działań niezgodnych z prawem. Nie polegaj na polityce „braku logów”.

</div>

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas dostawców. Pozwala nam to formułować całkowicie obiektywne zalecenia.** Oprócz [naszych standardowych kryteriów](about/criteria.md), opracowaliśmy jasny zestaw wymagań, które musi spełniać dostawca usługi VPN, aby mógł być przez nas polecany — obejmują one wdrożenie silnego szyfrowania, niezależnych audytów bezpieczeństwa, nowoczesnych technologii i nie tylko. Sugerujemy zapoznanie się z tą listą przed wyborem dostawcy usługi VPN i przeprowadzenie własnych badań, aby upewnić się, że wybrany dostawca jest jak najbardziej godny zaufania.

### Technologia

Wymagamy, aby wszyscy zalecani przez nas dostawcy VPN udostępniali standardowe pliki konfiguracyjne, które można wykorzystać w uniwersalnym kliencie VPN typu open-source. **Jeśli** dostawca udostępnia własną aplikację, musi ona mieć wbudowany tzw. „kill switch”, który blokuje przesyłanie danych po utracie połączenia z VPN, zapobiegając wyciekom ruchu sieciowego.

**Minimalne wymagania:**

- Obsługa silnych protokołów, takich jak WireGuard.
- Wbudowany kill switch w swoich aplikacjach.
- Obsługa multi-hop (łączenie przez wiele serwerów), co zwiększa prywatność w razie kompromitacji jednego z węzłów.
- Jeśli dostawca oferuje własne aplikacje, powinny być one [open source](https://en.wikipedia.org/wiki/Open_source), podobnie jak oprogramowanie VPN, na którym zazwyczaj są oparte. Wierzymy, że dostępność [kodu źródłowego](https://en.wikipedia.org/wiki/Source_code) zapewnia większą przejrzystość i możliwość weryfikacji działania programu.
- Funkcje odporne na cenzurę, zaprojektowane tak, aby omijać zapory sieciowe bez konieczności analizy głębokiej zawartości pakietów (DPI).

**Najlepszy scenariusz:**

- Kill switch z rozbudowanymi opcjami konfiguracji (np. włączenie/wyłączenie w określonych sieciach, uruchamianie przy starcie systemu itp.).
- Łatwe w obsłudze aplikacje VPN.
- Obsługa protokołu [IPv6](https://en.wikipedia.org/wiki/IPv6). Oczekujemy, że serwery umożliwiają zarówno połączenia przychodzące przez IPv6, jak i dostęp do usług działających w tej sieci.
- Możliwość [zdalnego przekierowywania portów](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding), co ułatwia tworzenie połączeń w aplikacjach typu P2P ([peer-to-peer](https://en.wikipedia.org/wiki/Peer-to-peer)) lub przy hostowaniu własnych usług (np. serwera Mumble).
- Technologia zaciemniania ruchu, która maskuje rzeczywisty charakter przesyłanych danych i pozwala obejść zaawansowane formy cenzury internetowej, takie jak DPI.

### Prywatność

Preferujemy, aby zalecani przez nas dostawcy gromadzili możliwie najmniej danych. Niezbieranie danych osobowych przy rejestracji oraz akceptowanie anonimowych form płatności są wymagane.

**Minimalne wymagania:**

- [Anonimowa kryptowaluta](cryptocurrency.md) **lub** opcja płatności gotówką.
- Brak konieczności podawania danych osobowych przy rejestracji: co najwyżej nazwa użytkownika, hasło i adres e-mail.

**Najlepszy scenariusz:**

- Akceptuje wiele [anonimowych opcji płatności](advanced/payments.md).
- Brak akceptowanych danych osobowych (nazwa użytkownika generowana automatycznie, brak wymogu podania adresu e-mail itp.).

### Bezpieczeństwo

VPN nie ma sensu, jeśli nie zapewnia odpowiedniego poziomu bezpieczeństwa. Wymagamy, aby wszyscy zalecani przez nas dostawcy przestrzegali aktualnych standardów bezpieczeństwa. Najlepiej, aby domyślnie stosowali bardziej przyszłościowe schematy szyfrowania. Wymagamy także niezależnego audytu bezpieczeństwa przeprowadzanego przez stronę trzecią — najlepiej kompleksowo i cyklicznie (co roku).

**Minimalne wymagania:**

- Silne schematy szyfrowania: OpenVPN z uwierzytelnianiem SHA-256; wymiana kluczy RSA-2048 lub lepsza; szyfrowanie danych AES-256-GCM lub AES-256-CBC.
- Utajnianie z wyprzedzeniem.
- Opublikowane audyty bezpieczeństwa przeprowadzone przez renomowaną firmę zewnętrzną.
- Serwery VPN korzystające z pełnego szyfrowania dysku lub działające wyłącznie w pamięci RAM.

**Najlepszy scenariusz:**

- Najsilniejsze szyfrowanie: RSA-4096.
- Opcjonalne szyfrowanie odporne na ataki kwantowe.
- Kompleksowe audyty bezpieczeństwa publikowane przez renomowaną firmę zewnętrzną.
- Programy bug-bounty i/lub skoordynowany proces ujawniania podatności.
- Serwery VPN działające wyłącznie w pamięci RAM.

### Zaufanie

Nie powierzył(a)byś swoich finansów komuś o fałszywej tożsamości, więc po co powierzać mu swoje dane internetowe? Wymagamy, aby zalecani przez nas dostawcy ujawniali informacje o właścicielach lub kadrze zarządzającej. Doceniamy również regularne raporty przejrzystości, szczególnie w zakresie tego, jak obsługiwane są żądania organów państwowych.

**Minimalne wymagania:**

- Publicznie dostępne informacje o właścicielu lub kadrze kierowniczej.
- Siedziba w jurysdykcji, w której firma nie może zostać prawnie zmuszona do prowadzenia tajnego rejestrowania aktywności użytkowników.

**Najlepszy scenariusz:**

- Publicznie dostępne informacje o właścicielu lub kadrze kierowniczej.
- Regularnie publikowane raporty przejrzystości.

### Marketing

W przypadku polecanych przez nas dostawców usługi VPN zwracamy uwagę na odpowiedzialne praktyki marketingowe.

**Minimalne wymagania:**

- Musi samodzielnie hostować analitykę (tj. bez korzystania z Google Analytics).

Brak nieodpowiedzialnych praktyk marketingowych, takich jak:

- Gwarancji pełnej anonimowości w 100%. Kiedy ktoś zapewnia o 100% skuteczności czegoś, oznacza to, że nie ma żadnej pewności co do niepowodzenia. Zdajemy sobie sprawę, że ludzie mogą dość łatwo ujawnić swoją tożsamość na wiele sposobów, np.:
    - używając tych samych danych osobowych lub pseudonimów bez korzystania z narzędzi zapewniających anonimowość (Tor, VPN itp.),
    - [przez unikalny odcisk przeglądarki (browser fingerprinting).](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Twierdzenie, że pojedynczy obwód VPN zapewnia „większą anonimowość” niż Tor, który opiera się na trzech lub więcej węzłach i regularnie zmienia trasę połączenia.
- Używanie alarmistycznego języka. Można napisać, że użytkownik jest „rozłączony” lub „niepołączony”, ale określenia typu „narażony”, „zagrożony” czy „podatny na ataki” są niepotrzebnie dramatyczne i często błędne. Przykładowo, dana osoba może po prostu korzystać z innego VPN-a lub z sieci Tor.

**Najlepszy scenariusz:**

Odpowiedzialny marketing, który jest zarówno edukacyjny, jak i przydatny dla użytkownika, może obejmować:

- rzetelne porównanie sytuacji, w których lepiej użyć sieci [Tor](tor.md) zamiast VPN,
- dostępność strony internetowej dostawcy VPN również za pośrednictwem [usługi onion](https://en.wikipedia.org/wiki/.onion).

### Dodatkowe funkcje

Nie są to ścisłe wymagania, lecz istnieją pewne czynniki, które są brane pod uwagę przy ocenie dostawców usługi VPN. Obejmują one funkcje blokowania treści, warrant canaries (publiczne oświadczenia o braku nakazów ujawnienia danych), wysoka jakość obsługi klienta, liczba dozwolonych jednoczesnych połączeń itp.
