---
meta_title: "Przeglądarki internetowe szanujące prywatność dla PC i Mac – Privacy Guides"
title: Przeglądarki na komputery stacjonarne
icon: material/laptop
description: Te przeglądarki chroniące prywatność to obecnie nasze zalecenia do standardowego/nieanonimowego korzystania z Internetu na komputerach stacjonarnych.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Zalecane prywatne przeglądarki desktopowe
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/pl/browser
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Firefox
    image: /assets/img/browsers/firefox.svg
    url: https://firefox.com
    sameAs: https://pl.wikipedia.org/wiki/Firefox
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    sameAs: https://pl.wikipedia.org/wiki/Brave_(przegl%C4%85darka)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-account-cash: Kapitalizm inwigilacji](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Oto nasze aktualne zalecenia dotyczące **przeglądarek internetowych na komputery stacjonarne** oraz ich konfiguracji do standardowego/nieanonimowego przeglądania. Zalecamy przeglądarkę [Mullvad](#mullvad-browser), jeśli zależy Ci na silnej ochronie prywatności i wbudowanych zabezpieczeniach przed tzw. „odciskami palców” bez konieczności konfiguracji; [Firefox](#firefox) dla osób szukających dobrej alternatywy dla Google Chrome do codziennego przeglądania, oraz [Brave](#brave), jeśli potrzebujesz zgodności z przeglądarkami opartymi na silniku Chromium.

Jeśli chcesz przeglądać Internet anonimowo, skorzystaj z sieci [Tor](tor.md). Na tej stronie przedstawiamy pewne zalecenia dotyczące konfiguracji, jednak każda przeglądarka inna niż Tor Browser będzie możliwa do zidentyfikowania przez *kogoś* w taki czy inny sposób.

## Przeglądarka Mullvad

<div class="admonition recommendation" markdown>

![Logo przeglądarki Mullvad](assets/img/browsers/mullvad_browser.svg){ align=right }

**Przeglądarka Mullvad** to wersja [Tor Browser](tor.md#tor-browser) z usuniętą integracją z siecią Tor. Jej celem jest zapewnienie użytkownikom VPN technologii ochrony przed identyfikacją przeglądarki (tzw. fingerprinting), które stanowią kluczową barierę przeciwko [:material-eye-outline: masowej inwigilacji](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. Rozwijana jest przez Tor Project i dystrybuowana przez [Mullvad](vpn.md#mullvad); **nie** wymaga jednak korzystania z VPN od Mullvad.

[:octicons-home-16: Strona główna](https://mullvad.net/pl/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/pl/help/privacy-policy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://mullvad.net/pl/help/tag/mullvad-browser){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/pl/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/pl/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/pl/download/browser/linux)

</details>

</div>

Podobnie jak [Tor Browser](tor.md), przeglądarka Mullvad została zaprojektowana tak, aby zapobiegać identyfikacji przez „odcisk palca” przeglądarki, sprawiając, że Twój profil przeglądarki jest identyczny ze wszystkimi innymi użytkownikami przeglądarki Mullvad. Zawiera ona domyślne ustawienia i rozszerzenia automatycznie konfigurowane w zależności od wybranego poziomu zabezpieczeń: *Standardowy*, *Bezpieczniejszy* i *Najbezpieczniejszy*.

Z tego powodu nie należy wprowadzać żadnych zmian w przeglądarce poza dostosowaniem domyślnych [poziomów zabezpieczeń](https://tb-manual.torproject.org/security-settings). Po zmianie poziomu zabezpieczeń **koniecznie** należy ponownie uruchomić przeglądarkę przed dalszym korzystaniem. W przeciwnym razie [ustawienia bezpieczeństwa mogą nie zostać w pełni zastosowane](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), co zwiększa ryzyko identyfikacji lub wykorzystania luk, mimo że wybrany poziom ochrony może sugerować coś innego.

Jakiekolwiek inne modyfikacje sprawią, że Twój odcisk przeglądarki stanie się unikalny, co niweczy sens korzystania z tej przeglądarki. Jeśli chcesz bardziej dostosować przeglądarkę i nie obawiasz się śledzenia przez odcisk przeglądarki, zalecamy zamiast tego użycie przeglądarki [Firefox](#firefox).

### Ochrona przed identyfikacją (Anti-Fingerprinting)

**Bez** korzystania z [VPN-a](vpn.md), przeglądarka Mullvad zapewnia taki sam poziom ochrony przed [prostymi skryptami identyfikującymi](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) jak inne przeglądarki ukierunkowane na prywatność, takie jak Firefox+[Arkenfox](#arkenfox-advanced) czy [Brave](#brave). Przeglądarka Mullvad zapewnia te zabezpieczenia od razu po instalacji, kosztem pewnej elastyczności i wygody, które mogą zapewnić inne prywatne przeglądarki.

== Dla najskuteczniejszej ochrony przed identyfikacją zalecamy korzystanie z przeglądarki Mullvad w połączeniu z VPN-em ==, niezależnie od tego, czy będzie to Mullvad, czy inny zalecany dostawca VPN. Korzystając z przeglądarki Mullvad wraz z VPN, współdzielisz odcisk przeglądarki i pulę adresów IP z wieloma innymi użytkownikami, co pozwala Ci „zniknąć w tłumie”. To jedyna skuteczna metoda ochrony przed zaawansowanymi technikami śledzenia i jest to dokładnie taka technika, która stosuje Tor Browser.

Warto zauważyć, że choć przeglądarkę Mullvad można używać z dowolnym dostawcą VPN, efekt „tłumu” pojawi się tylko wtedy, gdy inni użytkownicy tego samego VPN również korzystają z przeglądarki Mullvad. Jest to obecnie bardziej prawdopodobne w przypadku Mullvad VPN niż innych usług, szczególnie że przeglądarka ta została wydana niedawno. Przeglądarka Mullvad nie ma wbudowanej obsługi VPN ani nie sprawdza, czy korzystasz z VPN przed rozpoczęciem przeglądania; połączenie VPN należy skonfigurować i utrzymywać samodzielnie.

Przeglądarka Mullvad dostarczana jest z wbudowanymi rozszerzeniami *uBlock Origin* i *NoScript*. Choć zazwyczaj odradzamy instalowanie *dodatkowych* [rozszerzeń przeglądarki](browser-extensions.md), te, które są preinstalowane, nie powinny być usuwane ani modyfikowane względem ustawień domyślnych, ponieważ mogłoby to wyraźnie odróżnić Twój odcisk przeglądarki od innych użytkowników przeglądarki Mullvad. Przeglądarka zawiera także rozszerzenie Mullvad Browser Extension, które *można* bezpiecznie usunąć bez wpływu na odcisk palca przeglądarki, ale jego pozostawienie również nie stanowi problemu, nawet jeśli nie korzystasz z Mullvad VPN.

### Przeglądanie w trybie prywatnym

Mullvad Browser działa w stałym trybie prywatnego przeglądania, co oznacza, że historia, pliki cookie i inne dane witryn są automatycznie usuwane po każdym zamknięciu przeglądarki. Zakładki, ustawienia przeglądarki oraz konfiguracje rozszerzeń są jednak zachowywane.

To rozwiązanie jest niezbędne, by zapobiec zaawansowanym formom śledzenia, lecz odbywa się kosztem wygody oraz pewnych funkcji Firefoksa, takich jak Multi-Account Containers. Warto pamiętać, że zawsze można używać kilku przeglądarek, na przykład Firefox z Arkenfoxem do kilku witryn, na których chcesz pozostać zalogowany lub które nie działają poprawnie w przeglądarce Mullvad, oraz przeglądarkę Mullvad do ogólnego przeglądania Internetu.

## Firefox

<div class="admonition recommendation" markdown>

![Logo Firefoksa](assets/img/browsers/firefox.svg){ align=right }

**Firefox** zapewnia zaawansowane ustawienia prywatności, takie jak [wzmocniona ochrona przed śledzeniem](https://support.mozilla.org/pl/kb/wzmocniona-ochrona-przed-sledzeniem-firefox-desktop), które mogą pomóc zablokować różne [rodzaje śledzenia](https://support.mozilla.org/pl/kb/wzmocniona-ochrona-przed-sledzeniem-firefox-desktop#w_co-blokuje-wzmocniona-ochrona-przed-sledzeniem).

[:octicons-home-16: Strona główna](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Wspomóż projekt" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/pl/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/pl/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/pl/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/pl/apps/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

Firefox zawiera unikalny [token pobierania](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) w instalatorach pobranych ze strony Mozilli i wykorzystuje telemetrię w Firefoksie do przesyłania tego tokena. Token **nie jest** zawarty w wydaniach dostępnych w [repozytorium FTP Mozilli](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Zalecana konfiguracja Firefoksa

Poniższe opcje można znaleźć w :material-menu: → **Ustawienia**.

#### Wyszukiwanie

- [ ] Odznacz **Podpowiedzi wyszukiwania**

Funkcje podpowiedzi wyszukiwania mogą nie być dostępne w Twoim regionie.

Podpowiedzi wyszukiwania powodują, że wszystko, co wpisujesz w pasku adresu, jest wysyłane do domyślnej wyszukiwarki – niezależnie od tego, czy faktycznie wysyłasz zapytanie. Wyłączenie podpowiedzi pozwala dokładniej kontrolować, jakie dane przekazujesz dostawcy wyszukiwarki.

##### Firefox Suggest (tylko w USA)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) to funkcja podobna do podpowiedzi wyszukiwania, dostępna wyłącznie w Stanach Zjednoczonych. Zalecamy jej wyłączenie z tego samego powodu, dla którego zalecamy wyłączenie podpowiedzi wyszukiwania. Jeśli nie widzisz tych opcji w sekcji **Pasek adresu**, oznacza to, że nie masz tej funkcji i możesz zignorować te zmiany.

- [ ] Odznacz **Sugestie od Firefoksa**
- [ ] Odznacz **Sugestie od sponsorów**

#### Prywatność i bezpieczeństwo

##### Wzmocniona ochrona przed śledzeniem

- [x] Wybierz **Ścisłą** ochronę przed śledzeniem

Chroni Cię ona poprzez blokowanie elementów śledzących z mediów społecznościowych, skryptów identyfikujących przeglądarkę (choć nie chroni przed *wszystkimi* metodami identyfikacji), koparek kryptowalut, ciasteczek śledzących między witrynami oraz innych form śledzenia. Wzmocniona ochrona przed śledzeniem chroni przed wieloma powszechnymi zagrożeniami, jednak nie eliminuje wszystkich metod śledzenia, ponieważ została zaprojektowana tak, by miała minimalny lub zerowy wpływ na działanie stron internetowych.

##### Czyszczenie danych podczas zamykania przeglądarki

Jeśli chcesz pozostać zalogowany na wybranych stronach, możesz dodać wyjątki w sekcji **Ciasteczka i dane witryn** → **Wyjątki...**

- [x] Zaznacz **Usuwanie ciasteczek i danych witryn podczas zamykania przeglądarki Firefox**

Chroni to przed trwałymi ciasteczkami, choć nie zabezpiecza przed tymi, które zostały zapisane w trakcie bieżącej sesji. Po włączeniu tej opcji możesz łatwo wyczyścić dane przeglądarki, po prostu ponownie uruchamiając Firefoksa. Możesz również ustawić wyjątki dla konkretnych stron, na których chcesz pozostać zalogowany.

##### Telemetria

- [ ] Odznacz **Wysyłanie danych technicznych i o interakcjach do Mozilli**
- [ ] Odznacz **Instalowanie i przeprowadzanie badań**
- [ ] Odznacz **Automatyczne wysyłanie zgłoszeń awarii**

Zgodnie z polityką prywatności Mozilli dla Firefoksa:

> Firefox przesyła dane dotyczące wersji i języka Firefoksa, systemu operacyjnego urządzenia i konfiguracji sprzętowej, pamięci, podstawowe informacje o awariach i błędach oraz wyniki zautomatyzowanych procesów, takich jak aktualizacje, bezpieczne przeglądanie i aktywacja. Podczas przesyłania danych do Mozilli Twój adres IP jest tymczasowo zapisywany w dziennikach serwera.

Ponadto usługa kont Mozilla Accounts gromadzi [pewne dane techniczne](https://www.mozilla.org/pl/privacy/mozilla-accounts). Jeśli korzystasz z konta Mozilli, możesz zrezygnować z udostępniania tych informacji:

1. Otwórz [ustawienia profilu na accounts.firefox.com](https://accounts.firefox.com/pl/settings#data-collection)
2. Odznacz **Gromadzenie i wykorzystywanie danych** > **Pomóż ulepszyć konta Firefox**

##### Preferencje dotyczące reklam na witrynach

- [ ] Odznacz **Zezwalanie witrynom na przeprowadzanie pomiarów reklam przy zachowaniu prywatności**

Wraz z wydaniem Firefoksa 128 dodano nowe ustawienie dotyczące [atrybucji z zachowaniem prywatności](https://support.mozilla.org/pl/kb/privacy-preserving-attribution) (PPA), które zostało [domyślnie włączone](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA pozwala reklamodawcom wykorzystywać Twoją przeglądarkę do mierzenia skuteczności kampanii internetowych zamiast tradycyjnych metod śledzenia opartych na JavaScripcie. Uważamy, że takie działanie wykracza poza zakres obowiązków przeglądarki, a fakt, że funkcja ta jest domyślnie wyłączona w Arkenfoxie, stanowi dodatkowy argument za jej wyłączeniem.

##### Tryb używania wyłącznie protokołu HTTPS

- [x] Zaznacz **Włącz we wszystkich oknach**

Zapobiega to przypadkowemu łączeniu się ze stronami używającymi nieszyfrowanego protokołu HTTP. Strony bez obsługi HTTPS są obecnie rzadkością, więc ta opcja nie powinna mieć zauważalnego wpływu na codzienne przeglądanie Internetu.

##### DNS poprzez HTTPS

Jeśli korzystasz z [dostawcy DNS poprzez HTTPS](dns.md):

- [x] Wybierz opcję **Maksymalna ochrona** i ustaw odpowiedniego dostawcę

Tryb Maksymalnej ochrony wymusza korzystanie z DNS poprzez HTTPS. W przypadku, gdy Firefox nie będzie mógł połączyć się z bezpiecznym resolverem DNS lub jeśli ten zgłosi, że rekordy dla danej domeny nie istnieją, przeglądarka wyświetli ostrzeżenie o bezpieczeństwie. Chroni to przed sytuacją, w której sieć, z której korzystasz, potajemnie obniża poziom zabezpieczeń DNS.

#### Synchronizacja

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) umożliwia dostęp do danych przeglądania (historii, zakładek itp.) na wszystkich Twoich urządzeniach i chroni je za pomocą szyfrowania typu E2EE (end-to-end encryption).

### Arkenfox (dla zaawansowanych)

<div class="admonition tip" markdown>
<p class="admonition-title">Korzystaj z przeglądarki Mullvad dla zaawansowanej ochrony przed identyfikacją</p>

[Przeglądarka Mullvad](#mullvad-browser) zapewnia taki sam poziom ochrony przed identyfikacją przeglądarki jak Arkenfox, i to od razu po instalacji — bez konieczności używania Mullvad VPN, aby z nich korzystać. W połączeniu z VPN przeglądarka Mullvad potrafi zablokować bardziej zaawansowane techniki śledzenia, z którymi Arkenfox sobie nie radzi. Arkenfox ma jednak tę przewagę, że jest znacznie bardziej elastyczna i pozwala na tworzenie wyjątków dla konkretnych witryn, na których chcesz pozostać zalogowany(-a).

</div>

[Projekt Arkenfox](https://github.com/arkenfox/user.js) dostarcza zestaw starannie dobranych ustawień dla Firefoksa. Jeśli [zdecydujesz się](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) korzystać z Arkenfox, [niektóre opcje](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) mogą być subiektywnie zbyt restrykcyjne lub powodować problemy z działaniem niektórych stron — co możesz [łatwo dostosować](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) według własnych potrzeb. **Zdecydowanie zalecamy** zapoznanie się z ich pełnym [wiki](https://github.com/arkenfox/user.js/wiki) projektu. Arkenfox włącza także obsługę [kontenerów](https://support.mozilla.org/pl/kb/containers#w_for-advanced-users).

Arkenfox ma na celu jedynie utrudnienie działania podstawowych lub prostych skryptów śledzących poprzez losową zmianę zawartości elementów graficznych (tzw. canvas) i użycie wbudowanych ustawień Firefoksa związanych z odpornością na identyfikację. Nie ma on jednak na celu ujednolicenia odcisku przeglądarki z dużą grupą innych użytkowników Arkenfoxa — tak jak robi to przeglądarka Mullvad czy Tor Browser — co jest jedyną skuteczną metodą ochrony przed zaawansowanym śledzeniem odcisku przeglądarki. Warto pamiętać, że zawsze można używać kilku przeglądarek, na przykład Firefox z Arkenfoxem do kilku witryn, na których chcesz pozostać zalogowany lub którym ufasz, a przeglądarkę Mullvad do ogólnego przeglądania internetu.

## Brave

<div class="admonition recommendation annotate" markdown>

![Logo Brave](assets/img/browsers/brave.svg){ align=right }

**Przeglądarka Brave** zawiera wbudowany mechanizm blokowania treści oraz liczne [funkcje prywatności](https://brave.com/privacy-features), z których wiele jest domyślnie włączonych.

Oparta jest na projekcie przeglądarki Chromium, dzięki czemu jej interfejs i działanie powinny być dobrze znane większości osób, a problemy ze zgodnością stron internetowych są minimalne.

[:octicons-home-16: Strona główna](https://brave.com/pl){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Usługa onion" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://support.brave.com/hc/pl){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/pl/download)
- [:simple-apple: macOS](https://brave.com/pl/download)
- [:simple-linux: Linux](https://brave.com/pl/linux)
- [:simple-flathub: Flathub](https://flathub.org/pl/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

Brave dodaje tzw. „[kod polecenia](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)” do nazwy pliku instalacyjnego pobieranego z oficjalnej strony Brave. Kod ten służy do śledzenia źródła, z którego przeglądarka została pobrana, na przykład `BRV002` w pliku o nazwie `Brave-Browser-BRV002.pkg`. Po zakończeniu instalacji instalator wysyła ten kod do serwera Brave. Jeśli Cię to niepokoi, możesz po prostu zmienić nazwę pliku instalacyjnego przed jego uruchomieniem.

</div>

### Zalecana konfiguracja przeglądarki Brave

Poniższe opcje można znaleźć w :material-menu: → **Ustawienia**.

#### Tarcze

Brave posiada pewne zabezpieczenia przed identyfikacją przeglądarki w ramach funkcji [Tarcze](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Zalecamy skonfigurowanie tych ustawień [globalnie](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) – czyli dla wszystkich odwiedzanych stron.

W razie potrzeby można je obniżyć dla poszczególnych witryn, jednak domyślnie zalecamy następującą konfigurację:

<div class="annotate" markdown>

- [x] Wybierz **Agresywnie** w sekcji *Zablokuj skrypty śledzące i reklamy*

<details class="warning" markdown>
<summary>Używaj domyślnych list filtrów</summary>

Brave pozwala wybrać dodatkowe filtry treści na wewnętrznej stronie `brave://adblock`. Odradzamy korzystanie z tej funkcji; zamiast tego pozostaw domyślne listy filtrów. Używanie dodatkowych list sprawi, że będziesz się wyróżniał na tle innych użytkowników i może zwiększyć ryzyko ataku powierzchniowego, jeśli w Brave znajduje się luka i złośliwa reguła zostanie dodana do jednej z list, których używasz.

</details>

- [x] Wybierz **Ścisłe** w sekcji *Aktualizacje HTTPS*
- [x] (Opcjonalnie) Zaznacz **Zablokuj skrypty** (1)
- [x] Zaznacz **Zablokuj zdejmowanie odcisków palca**
- [x] Wybierz **Blokuj pliki cookie innych firm**
- [x] Zaznacz **Zapomnij po zamknięciu tej strony** (2)
- [ ] Odznacz wszystkie komponenty mediów społecznościowych

</div>

1. Ta opcja wyłącza JavaScript, co sprawi, że wiele stron przestanie działać prawidłowo. Aby przywrócić ich działanie, możesz dodać wyjątki dla konkretnych stron, klikając ikonę tarczy w pasku adresu i odznaczając tę opcję w sekcji *Zaawansowane sterowanie*.
2. Jeśli chcesz pozostać zalogowany na wybranej stronie, którą odwiedzasz często, również możesz dodać wyjątek w ten sam sposób — klikając ikonę tarczy i odznaczając ustawienie w sekcji *Zaawansowane sterowanie*.

#### Prywatność i bezpieczeństwo

<div class="annotate" markdown>

- [x] Wybierz **Nie zezwalaj witrynom na korzystanie z optymalizacji JavaScriptu** w sekcji *Bezpieczeństwo* → *Zarządzanie optymalizacją i zabezpieczeniami JavaScriptu* (1)
- [x] Zaznacz **Automatycznie usuwaj uprawnienia nieużywanych witryn** w sekcji *Ustawienia stron i tarcz*
- [x] Wybierz **Wyłącz UDP bez proxy** w sekcji [*Zasady obsługi IP WebRTC IP*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Odznacz **Użyj usług Google do wiadomości typu push**
- [x] Zaznacz **Automatyczne przekierowywanie stron AMP**
- [x] Zaznacz **Automatycznie przekierowuj śledzące adresy URL**
- [x] Zaznacz **Zablokuj zdejmowanie odcisków palców na podstawie moich preferencji językowych**

</div>

1. Wyłączenie optymalizatora V8 zmniejsza powierzchnię ataku, wyłączając [*niektóre*](https://grapheneos.social/@GrapheneOS/112708049232710156) elementy kompilacji JavaScript Just-In-Time (JIT).

##### Okna w Tor

[**Prywatne okno z Torem**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) pozwala kierować ruch przez sieć Tor w oknach prywatnych oraz uzyskiwać dostęp do usług .onion, co może być przydatne w niektórych przypadkach. Jednak Brave **nie** zapewnia takiej ochrony przed identyfikacją przeglądarki jak Tor, a znacznie mniej osób korzysta z Brave w trybie Tor — przez co łatwiej się wyróżnisz. Jeśli Twój model zagrożeń wymaga silnej anonimowości, używaj [Tor Browser](tor.md#tor-browser).

##### Gromadzenie danych

- [ ] Odznacz **Zezwól na zastosowanie analizy produktów z zachowaniem prywatności (P3A)**
- [ ] Odznacz **Automatycznie wysyłaj pingi dziennego użycia do Brave**
- [ ] Odznacz **Automatycznie wysyłaj raporty diagnostyczne**

#### Sieć Web3

Funkcje Web3 w przeglądarce Brave mogą potencjalnie zwiększyć unikalność Twojego odcisku przeglądarki oraz powierzchnię ataku. Jeśli nie korzystasz z żadnej z tych funkcji, należy je wyłączyć.

- Wybierz **Rozszerzenia (bez kopii zapasowej)** w sekcji *Domyślny portfel Ethereum*
- Wybierz **Rozszerzenia (bez kopii zapasowej)** w sekcji *Domyślny portfel Solana*

#### Rozszerzenia

- [ ] Odznacz wszystkie wbudowane rozszerzenia, z których nie korzystasz

#### Wyszukiwarka

Zalecamy wyłączenie podpowiedzi wyszukiwania w Brave, zwanych tam sugestiami wyszukiwania, z tych samych powodów, dla których zalecamy to w [Firefoksie](#search).

- [ ] Odznacz **Sugestie wyszukiwania**

#### System

<div class="annotate" markdown>

- [ ] Odznacz **Kontynuuj działanie aplikacji w tle po zamknięciu Brave**, aby wyłączyć aplikacje działające w tle (1)

</div>

1. Ta opcja nie jest dostępna na wszystkich platformach.

#### Synchronizacja (Brave Sync)

[Brave Sync](https://support.brave.app/hc/pl/articles/360059793111-Zrozumienie-Brave-Sync) pozwala na dostęp do danych przeglądania (historii, zakładek itp.) na wszystkich Twoich urządzeniach bez potrzeby zakładania konta i chroni je za pomocą szyfrowania typu E2EE (end-to-end encryption).

#### Nagrody i portfel Brave

**Nagrody Brave** pozwalają na zdobywanie kryptowaluty Basic Attention Token (BAT) za wykonywanie określonych czynności w przeglądarce Brave. System ten wymaga konta powierniczego oraz weryfikacji na bazie procedury KYC u wybranych dostawców usług. Nie zalecamy BAT jako [prywatnej kryptowaluty](cryptocurrency.md) ani korzystania z [portfela powierniczego](advanced/payments.md#wallet-custody), dlatego odradzamy używanie tej funkcji.

**Portfel Brave** działa lokalnie na Twoim komputerze, ale nie obsługuje żadnych prywatnych kryptowalut, dlatego również odradzamy korzystanie z tej funkcji.

## Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

### Minimalne wymagania

- Musi być oprogramowaniem typu open source.
- Musi obsługiwać automatyczne aktualizacje.
- Musi otrzymywać aktualizacje silnika w ciągu 0–1 dnia od oficjalnego wydania.
- Musi być dostępne na systemach Linux, macOS i Windows.
- Wszelkie zmiany mające na celu zwiększenie prywatności nie mogą pogarszać komfortu użytkowania.
- Musi domyślnie blokować ciasteczka stron trzecich.
- Musi obsługiwać [partycjonowanie stanu](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) w celu ograniczenia śledzenia między witrynami.[^1]

### Najlepszy scenariusz

Nasze kryteria „najlepszego scenariusza” określają, jak powinien wyglądać idealny projekt w tej kategorii. Nasze zalecenia nie muszą spełniać wszystkich tych warunków, jednak projekty, które spełniają więcej z nich, mogą być oceniane wyżej od pozostałych na stronie.

- Powinien zawierać wbudowaną funkcję blokowania treści.
- Powinien obsługiwać izolację ciasteczek (na wzór [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Powinien obsługiwać progresywne aplikacje internetowe (PWA). PWA umożliwiają instalowanie wybranych stron internetowych tak, jakby były natywnymi aplikacjami na komputerze. To rozwiązanie ma przewagę nad aplikacjami opartymi na Electronie, ponieważ PWA korzystają z regularnych aktualizacji zabezpieczeń przeglądarki.
- Nie powinien zawierać dodatkowych funkcji (bloatware), które nie wpływają na prywatność użytkownika.
- Nie powinien domyślnie gromadzić danych telemetrycznych.
- Powinien udostępniać implementację serwera synchronizacji typu open source.
- Powinien domyślnie korzystać z [prywatnej wyszukiwarki](search-engines.md).

[^1]: Implementacja Brave’a została opisana szczegółowo tutaj: [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state)(ang.).
