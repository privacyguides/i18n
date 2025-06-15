---
meta_title: "Przeglądarki internetowe na PC i Mac respektujące prywatność - Privacy Guides"
title: "Przeglądarki desktopowe"
icon: material/laptop
description: Te przeglądarki chroniące prywatność są obecnie zalecane do standardowego / nieanonimowego przeglądania Internetu na komputerach stacjonarnych.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Rekomendacje przeglądarek desktopowych
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/pl/download/browser
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

<small>Chroni przed następującym zagrożeniem(ami):</small>

- [:material-account-cash: Kapitalizm inwigilacji](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

To są obecnie zalecane przez nas **przeglądarki internetowe** i konfiguracje dla przeglądania standardowego/nieanonimowego. Polecamy [Mullvad Browser](#mullvad-browser), jeśli koncentrujesz się na silnej ochronie prywatności i ochronie przed odciskami palców bez konieczności konfiguracji, [Firefox](#firefox) dla standardowego przeglądania internetu służąca jako dobra alternatywa dla Google Chrome, oraz [Brave](#brave), jeśli potrzebujesz kompatybilności z przeglądarkami opartymi na silniku Chromium.

Jeśli chcesz przeglądać Internet anonimowo, powinieneś użyć sieci [Tor](tor.md). Na tej stronie przedstawiamy pewne zalecenia dotyczące konfiguracji, ale wszystkie przeglądarki inne niż Tor Browser będą w taki czy inny sposób możliwe do zidentyfikowania przez *innych*.

## Przeglądarka Mullvad

<div class="admonition recommendation" markdown>

![Logo przeglądarki Mullvad](assets/img/browsers/mullvad_browser.svg){ align=right }

**Przeglądarka Mullvad** to wersja [przeglądarki Tor](tor.md#tor-browser) z usuniętymi integracjami sieci Tor. Jej celem jest zapewnienie użytkownikom VPN technologii ograniczających pobieranie odcisku przeglądarki (tzw. fingerprinting), które stanowią kluczową ochronę przed [:material-eye-outline: masową inwigilacją](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. Jest rozwijany przez Tor Project i dystrybuowany przez [Mullvad](vpn.md#mullvad) i **nie** wymaga korzystania z sieci VPN od Mullvad.

[:octicons-home-16: Strona główna](https://mullvad.net/pl/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/pl/help/privacy-policy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://mullvad.net/pl/help/tag/mullvad-browser){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pliki do pobrania</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/pl/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/pl/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/pl/download/browser/linux)

</details>

</div>

Podobnie jak [Tor Browser](tor.md), przeglądarka Mullvad została zaprojektowana tak, aby zapobiegać pobieraniu odcisku przeglądarki, czyniąc odcisk identycznym z innymi użytkownikami przeglądarki Mullvad. Zawiera on domyślne ustawienia i rozszerzenia, które są automatycznie konfigurowane według domyślnych poziomów bezpieczeństwa: *Standardowy*, *Bezpieczniejszy* i *Najbezpieczniejszy*.

Dlatego niezwykle ważne jest, aby nie wprowadzać żadnych zmian w przeglądarce poza dostosowaniem domyślnych [poziomów bezpieczeństwa](https://tb-manual.torproject.org/security-settings). Przy zmianie poziomu bezpieczeństwa **musisz** zawsze ponownie uruchomić przeglądarkę, zanim zaczniesz z niej dalej korzystać. W przeciwnym razie [ustawienia bezpieczeństwa mogą nie zostać w pełni zastosowane](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), co narazi Cię na większe ryzyko pobierania odcisków przeglądarki i ataków, niż wynikałoby to z wybranego poziomu bezpieczeństwa.

Wprowadzanie jakichkolwiek innych zmian poza dostosowaniem tego ustawienia sprawi, że odcisk przeglądarki stanie się unikalny, co uczyniłoby bezcelowym prawidłowe i bezpiecznie korzystanie z tej przeglądarki. Jeśli chcesz bardziej skonfigurować swoją przeglądarkę, a fingerprinting nie jest dla Ciebie problemem, zalecamy zamiast tego przeglądarki [Firefox](#firefox).

### Ochrona przed fingerprintingiem

**Bez** korzystania z [VPN](vpn.md), przeglądarka Mullvad zapewnia taką samą ochronę przed [naiwnymi skryptami fingerprintingu](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) jak inne prywatne przeglądarki, takie jak Firefox+[Arkenfox](#arkenfox-advanced) lub [Brave](#brave). Przeglądarka Mullvad zapewnia te zabezpieczenia od razu po instalacji, kosztem pewnej elastyczności i wygody, które mogą zapewnić inne prywatne przeglądarki.

== Aby uzyskać najsilniejszą ochronę przed odciskami palców, zalecamy korzystanie z Mullvad Browser w połączeniu **z** VPN==, niezależnie od tego, czy jest to Mullvad, czy inny zalecany dostawca VPN. Korzystając z VPN i Mullvad Browser, będziesz współdzielić odcisk palca i pulę adresów IP z wieloma innymi użytkownikami, dając ci "tłum", w który możesz się wtopić. Ta strategia jest jedynym sposobem na udaremnienie zaawansowanych skryptów śledzących i jest to ta sama technika anty-fingerprint, którą stosuje przeglądarka Tor.

Należy pamiętać, że chociaż można korzystać z Mullvad Browser z dowolnym dostawcą VPN, inne osoby w tej sieci VPN muszą również korzystać z Mullvad Browser, aby ten "tłum" mógł istnieć, co jest bardziej prawdopodobne w przypadku Mullvad VPN w porównaniu z innymi dostawcami, szczególnie tak blisko uruchomienia Mullvad Browser. Mullvad Browser nie ma wbudowanej łączności VPN, ani nie sprawdza, czy korzystasz z VPN przed przeglądaniem; połączenie VPN musi być skonfigurowane i zarządzane osobno.

Przeglądarka Mullvad Browser jest dostarczana z preinstalowanymi rozszerzeniami przeglądarki *uBlock Origin* i *NoScript*. Chociaż zazwyczaj odradzamy dodawanie *dodatkowych* [rozszerzeń przeglądarki](browser-extensions.md), te rozszerzenia, które są preinstalowane z przeglądarką, **nie** powinny być usuwane ani konfigurowane poza ich domyślnymi wartościami, ponieważ spowodowałoby to zauważalne odróżnienie odcisku palca przeglądarki od innych użytkowników Mullvad Browser. Przeglądarka jest również dostarczana z preinstalowanym rozszerzeniem przeglądarki Mullvad, które *można* bezpiecznie usunąć bez wpływu na odcisk palca przeglądarki, ale można je również bezpiecznie pozostawić, nawet jeśli nie korzystasz z Mullvad VPN.

### Tryb prywatny przeglądarki

Mullvad Browser działa w stałym trybie przeglądania prywatnego, co oznacza, że historia, pliki cookie i inne dane witryn będą zawsze czyszczone po każdym zamknięciu przeglądarki. Zakładki, ustawienia przeglądarki i ustawienia rozszerzeń zostaną zachowane.

Jest to wymagane, aby zapobiec zaawansowanym formom śledzenia, ale odbywa się kosztem wygody i niektórych funkcji Firefox'a, takich jak kontenery z wieloma kontami. Pamiętaj, że zawsze możesz korzystać z wielu przeglądarek, na przykład możesz rozważyć użycie Firefox + Arkenfox dla kilku witryn, na których chcesz pozostać zalogowany lub które nie działają poprawnie w Mullvad Browser, oraz Mullvad Browser do ogólnego przeglądania.

### Mullvad Leta

Przeglądarka Mullvad domyślnie korzysta z [**Mullvad Leta**](https://leta.mullvad.net) jako wyszukiwarki, która działa jako proxy do wyników wyszukiwania Google lub Brave (do wyboru na stronie głównej Mullvad Leta).

Jeśli jesteś użytkownikiem Mullvad VPN, korzystanie z usług takich jak Mullvad Leta, oferowanych bezpośrednio przez samego dostawcę VPN, wiąże się z pewnym ryzykiem. Dzieje się tak, ponieważ Mullvad teoretycznie ma dostęp zarówno do prawdziwego adresu IP (poprzez VPN), jak i do aktywności wyszukiwania (poprzez Leta) - czyli do informacji, które VPN z założenia powinien od siebie oddzielać. Nawet jeśli Mullvad gromadzi bardzo mało informacji o swoich użytkownikach VPN czy Leta, powinieneś rozważyć użycie innej [wyszukiwarki](search-engines.md), jeśli to ryzyko budzi Twój niepokój.

## Firefox

<div class="admonition recommendation" markdown>

![Logo Firefox](assets/img/browsers/firefox.svg){ align=right }

**Firefox** zapewnia silne ustawienia prywatności, takie jak [wzmocniona ochrona przed śledzeniem](https://support.mozilla.org/pl/kb/wzmocniona-ochrona-przed-sledzeniem-firefox-desktop), które mogą pomóc zablokować różne [rodzaje śledzenia](https://support.mozilla.org/pl/kb/wzmocniona-ochrona-przed-sledzeniem-firefox-desktop#w_co-blokuje-wzmocniona-ochrona-przed-sledzeniem).

[:octicons-home-16: Strona główna](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Przyczyń się" }

<details class="downloads" markdown>
<summary>Pliki do pobrania</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

Firefox zawiera unikalny [token pobierania](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) w pobieraniach ze strony Mozilli i używa telemetrii w Firefox, aby wysłać token. Token **nie jest** zawarty w wydaniach z [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Zalecana konfiguracja przeglądarki Firefox

Te opcje znajdziesz w :material-menu: → **Ustawienia**.

#### Wyszukiwarka

- [ ] Odznacz **Podpowiedzi wyszukiwania**

Funkcje podpowiedzi wyszukiwania mogą nie być dostępne w Twoim regionie.

Podpowiedzi wyszukiwania przesyłają wszystko, co wpisujesz w pasku adresu, do domyślnej wyszukiwarki, niezależnie od tego, czy faktycznie zatwierdzisz wyszukiwanie. Wyłączenie podpowiedzi wyszukiwania pozwala bardziej precyzyjnie kontrolować dane wysyłane do dostawcy wyszukiwarki.

##### Firefox Suggest (tylko USA)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) to funkcja podobna do podpowiedzi wyszukiwania, która jest dostępna tylko w Stanach Zjednoczonych. Zalecamy wyłączenie tej funkcji z tego samego powodu, dla którego rekomendujemy wyłączenie podpowiedzi wyszukiwania. Jeśli nie widzisz tych opcji pod **paskiem adresu strony**, nie masz tej funkcjonalności i możesz zignorować te zmiany.

- [ ] Odznacz **Sugestie z Firefox**
- [ ] Odznacz **Sugestie od sponsorów**

#### Prywatność i bezpieczeństwo

##### Udoskonalona ochrona przed śledzeniem

- [x] Wybierz **Ścisła** ochrona przed śledzeniem

Chroni to użytkownika poprzez blokowanie modułów śledzących w mediach społecznościowych, skryptów służących do identyfikacji przeglądarki (należy pamiętać, że nie chroni to przed *wszystkimi* odciskami palców), koparek kryptowalut, ciasteczek śledzących różne witryny i niektórych innych treści śledzących. Ochrona przed śledzeniem chroni przed wieloma powszechnymi zagrożeniami, jednak nie blokuje wszystkich metod śledzenia, ponieważ została zaprojektowana tak, by mieć minimalny lub zerowy wpływ na użyteczność stron.

##### Wyczyść po zamknięciu

Jeśli chcesz pozostać zalogowany na wybranych stronach, możesz zezwolić na wyjątki w **Pliki cookie i dane witryn** → **Zarządzaj wyjątkami...**

- [x] Zaznacz **Usuń pliki cookie i dane witryn po zamknięciu przeglądarki Firefox**

Chroni to użytkownika przed trwałymi ciasteczkami, ale nie chroni przed ciasteczkami pozyskanymi podczas jednej sesji przeglądania. Po włączeniu tej opcji możliwe jest łatwe wyczyszczenie ciasteczek przeglądarki poprzez ponowne uruchomienie Firefoksa. Możesz ustawiać wyjątki dla poszczególnych stron, jeśli chcesz pozostać zalogowany na konkretnej stronie, którą często odwiedzasz.

##### Telemetria

- [ ] Odznacz **Wysyłanie danych technicznych i o interakcjach do Mozilli**
- [ ] Odznacz **Instalowanie i przeprowadzanie badań**
- [ ] Odznacz **Automatyczne wysyłanie zgłoszeń awarii**

Zgodnie z polityką prywatności Firefoksa opracowaną przez Mozillę,

> Firefox wysyła o nas dane o wersji i języku Firefoksa, systemie operacyjnym urządzeniach i konfiguracji sprzętowej, pamięci, podstawowe informacje o awariach i błędach oraz wynikach zautomatyzowanych procesów, takich jak aktualizacje, bezpieczne przeglądanie i aktywacja. Gdy przeglądarka Firefox wysyła nasze dane, adres IP użytkownika jest tymczasowo gromadzony w dziennikach serwera.

Ponadto usługa Mozilla Accounts gromadzi [pewne dane techniczne](https://mozilla.org/privacy/mozilla-accounts). Jeśli korzystasz z konta Firefox, możesz z tego zrezygnować:

1. Otwórz ustawienia profilu [na accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Odznacz **Gromadzenie i wykorzystywanie danych** > **Pomóż ulepszyć konta Firefox**

##### Preferencje dotyczące reklam na witrynach

- [ ] Odznacz **Zezwalanie witrynom na przeprowadzanie pomiarów reklam przy zachowaniu prywatności**

Wraz z wydaniem Firefoksa 128 dodano nowe ustawienie dotyczące [atrybucji z zachowaniem prywatności](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA), które jest [włączone domyślnie](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA pozwala reklamodawcom mierzyć skuteczność kampanii internetowych za pomocą danej przeglądarki, zamiast wykorzystywać do tego tradycyjne śledzenie oparte na JavaScript. Uważamy, że takie działanie wykracza poza zakres obowiązków przeglądarki, a fakt, że funkcja ta jest domyślnie wyłączona w Arkenfox, jest dodatkowym argumentem za jej wyłączeniem.

##### Tryb używania wyłącznie protokołu HTTPS

- [x] Zaznacz **Włącz we wszystkich oknach**

To zapobiega nieumyślnemu połączeniu się ze stroną przez niezabezpieczony protokół HTTP. Obecnie strony bez HTTPS są rzadkością, więc ta opcja nie powinna mieć żadnego wpływu na codzienne przeglądanie internetu.

##### DNS poprzez HTTPS

Jeśli korzystasz z [dostawcy DNS poprzez HTTPS](dns.md):

- [x] Wybierz opcję **Maksymalna ochrona** i wybierz odpowiedniego dostawcę

Maksymalna ochrona wymusza korzystanie z DNS poprzez HTTPS, a jeśli Firefox nie może połączyć się z bezpiecznym resolverem DNS lub jeśli ten poinformuje, że nie istnieją rekordy dla domeny, do której próbujesz uzyskać dostęp, pojawi się ostrzeżenie o bezpieczeństwie. To uniemożliwia sieci, z którą jesteś połączony, potajemne obniżenie poziomu bezpieczeństwa DNS.

#### Synchronizacja

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) umożliwia dostęp do danych przeglądania (historii, zakładek itd.) na wszystkich urządzeniach i chroni je za pomocą E2EE.

### Arkenfox (zaawansowany)

<div class="admonition tip" markdown>
<p class="admonition-title">Korzystaj z przeglądarki Mullvad do zaawansowanej ochrony przed odciskami palców</p>

[Przeglądarka Mullvad](#mullvad-browser) oferuje takie same zabezpieczenia przed identyfikacją przeglądarki jak Arkenfox już po instalacji i nie wymaga korzystania z VPN Mullvad, aby z nich korzystać. W połączeniu z VPN, przeglądarka Mullvad może zablokować bardziej zaawansowane skrypty śledzące, z którymi Arkenfox sobie nie poradzi. Arkenfox ma jednak tę przewagę, że jest znacznie bardziej elastyczny i pozwala na dodawanie wyjątków dla stron, na których chcesz pozostać zalogowany.

</div>

[Projekt Arkenfox](https://github.com/arkenfox/user.js) dostarcza zestaw starannie przemyślanych opcji dla Firefoksa. Jeśli [zdecydujesz się](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) korzystać z Arkenfox, [niektóre ustawienia](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) są subiektywnie restrykcyjne i/lub mogą powodować, że niektóre strony nie będą działać poprawnie — możesz je [łatwo zmienić](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) według własnych potrzeb. **Zdecydowanie zalecamy** przeczytanie całej ich [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox włącza także obsługę [kontenerów](https://support.mozilla.org/kb/containers#w_for-advanced-users).

Arkenfox ma na celu jedynie blokowanie podstawowych lub prostych skryptów śledzących, korzystając z losowego generowania zawartości elementów graficznych (tzw. canvas) oraz wbudowanych ustawień Firefoksa ograniczających możliwość identyfikacji przeglądarki użytkownika. Nie ma jednak na celu upodobnienia przeglądarki do dużej grupy innych użytkowników Arkenfox, tak jak robi to przeglądarka Mullvad czy przeglądarka Tor — a to jedyny sposób na zablokowanie zaawansowanych technik śledzenia odciskiem przeglądarki. Pamiętaj, że zawsze możesz korzystać z kilku przeglądarek. Na przykład, możesz używać Firefoksa z Arkenfox do tych kilku stron, na których musisz być zalogowany lub którym ufasz, a do ogólnego przeglądania internetu — przeglądarki Mullvad.

## Brave

<div class="admonition recommendation annotate" markdown>

![Logo Brave](assets/img/browsers/brave.svg){ align=right }

**Przeglądarka Brave** zawiera wbudowany bloker treści oraz [funkcje prywatności](https://brave.com/privacy-features), z których wiele jest domyślnie włączonych.

Brave jest oparty na projekcie przeglądarki Chromium, więc powinien wyglądać znajomo i nie sprawiać problemów z kompatybilnością na większości stron internetowych.

[:octicons-home-16: Strona główna](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Usługa Onion" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pliki do pobrania</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

Brave dodaje "[kod polecenia](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" do nazwy pliku podczas pobierania z oficjalnej strony Brave. Kod ten służy do śledzenia, z jakiego źródła przeglądarka została pobrana, na przykład `BRV002` w pliku o nazwie `Brave-Browser-BRV002.pkg`. Instalator po zakończeniu procesu instalacji wysyła kod polecenia na serwer Brave. Jeśli Cię to niepokoi, możesz przed uruchomieniem zmienić nazwę pliku instalacyjnego.

</div>

### Zalecana konfiguracja przeglądarki Brave

Te opcje znajdziesz w :material-menu: → **Ustawienia**.

#### Tarcze

Brave posiada pewne zabezpieczenia przed identyfikacją przeglądarki w ramach funkcji [Tarcze](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Zalecamy skonfigurowanie tych opcji [globalnie](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) – dla wszystkich odwiedzanych stron.

Ustawienia tarczy można w razie potrzeby obniżać dla wybranych stron, ale domyślnie zalecamy następujące ustawienia:

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

1. Ta opcja wyłącza JavaScript, co sprawi, że wiele stron przestanie działać poprawnie. Aby przywrócić ich działanie, możesz dodać wyjątki dla konkretnych stron, klikając ikonę tarczy w pasku adresu i odznaczając tę opcję w sekcji *Zaawansowane sterowanie*.
2. Jeśli chcesz pozostać zalogowany na wybranej stronie, którą odwiedzasz często, również możesz dodać wyjątek w ten sam sposób — klikając ikonę tarczy i odznaczając ustawienie w sekcji *Zaawansowane sterowanie*.

#### Prywatność i bezpieczeństwo

<div class="annotate" markdown>

* [x] Wybierz **Nie zezwalaj witrynom na korzystanie z optymalizatora V8** w sekcji *Bezpieczeństwo* → *Zarządzaj zabezpieczeniami V8* (1)
* [x] Wybierz **Automatycznie usuwaj uprawnienia nieużywanych witryn** w *Ustawienia stron i tarcz*
* [x] Wybierz **Wyłącz UDP bez proxy** w [*Zasady obsługi IP WebRTC IP*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
* [ ] Odznacz **Użyj usług Google do wiadomości typu push**
* [x] Wybierz **Automatyczne przekierowywanie stron AMP**
* [x] Wybierz **Automatycznie przekierowuj śledzące adresy URL**
* [x] Wybierz **Zablokuj zdejmowanie odcisków palców na podstawie moich preferencji językowych**

</div>

1. Wyłączenie optymalizatora V8 zmniejsza powierzchnię ataku, wyłączając [*niektóre*](https://grapheneos.social/@GrapheneOS/112708049232710156) elementy kompilacji JavaScript Just-In-Time (JIT).

##### Okna w Tor

[**Prywatne okno z Torem**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) umożliwia kierowanie ruchu przez sieć Tor w oknach prywatnych oraz dostęp do usług .onion, co w niektórych przypadkach może być przydatne. Jednak Brave **nie** zapewnia takiej ochrony przed identyfikacją przeglądarki jak Tor, a znacznie mniej osób korzysta z Brave w trybie Tor — przez co łatwiej się wyróżnisz. Jeśli Twój model zagrożeń wymaga silnej anonimowości, używaj [przeglądarki Tor](tor.md#tor-browser).

##### Gromadzenie danych

- [ ] Odznacz **Zezwól na zastosowanie analizy produktów z zachowaniem prywatności (P3A)**
- [ ] Odznacz **Automatycznie wysyłaj pingi dziennego użycia do Brave**
- [ ] Odznacz **Automatycznie wysyłaj raporty diagnostyczne**

#### Sieć Web3

Funkcje Web3 w Brave mogą potencjalnie zwiększać unikalność Twojej przeglądarki oraz powierzchnię ataku. Jeśli nie korzystasz z żadnej z tych funkcji, powinieneś je wyłączyć.

- Wybierz **Rozszerzenia (bez kopii zapasowej)** w sekcji *Domyślny portfel Ethereum*
- Wybierz **Rozszerzenia (bez kopii zapasowej)** w sekcji *Domyślny portfel Solana*

#### Rozszerzenia

- [ ] Odznacz wszystkie wbudowane rozszerzenia, z których nie korzystasz

#### Wyszukiwarka

Zalecamy wyłączenie podpowiedzi wyszukiwania w Brave z tego samego powodu, dla którego zalecamy wyłączenie tej funkcji w [Firefoksie](#search).

- [ ] Odznacz **Podpowiedzi wyszukiwania**

#### System

<div class="annotate" markdown>

- [ ] Odznacz **Kontynuuj działanie aplikacji w tle po zamknięciu Brave**, aby wyłączyć aplikacje działające w tle (1)

</div>

1. Ta opcja nie jest dostępna na wszystkich platformach.

#### Synchronizacja

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) umożliwia dostęp do danych przeglądania (historii, zakładek itd.) na wszystkich urządzeniach bez potrzeby zakładania konta i chroni je za pomocą E2EE.

#### Nagrody i Portfel Brave

**Nagrody Brave** pozwalają otrzymywać kryptowalutę Basic Attention Token (BAT) za wykonywanie określonych działań w przeglądarce Brave. Wymaga założenia konta powierniczego oraz weryfikacji tożsamości (KYC) u wybranych dostawców usług. Nie polecamy BAT jako [prywatnej kryptowaluty](cryptocurrency.md) ani korzystania z [portfela powierniczego](advanced/payments.md#wallet-custody), odradzamy używanie tej funkcji.

**Portfel Brave** działa lokalnie na Twoim komputerze, ale nie obsługuje żadnych prywatnych kryptowalut, dlatego również odradzamy korzystanie z tej funkcji.

## Kryteria

**Zwróć uwagę, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](about/criteria.md) opracowaliśmy również jasny zestaw wymagań, który pozwala nam przedstawiać obiektywne rekomendacje. Zalecamy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, by upewnić się, że jest to odpowiedni wybór dla Ciebie.

### Wymagania minimalne

- Musi być otwartym oprogramowaniem.
- Musi obsługiwać automatyczne aktualizacje.
- Musi otrzymywać aktualizacje silnika w ciągu 0-1 dnia od oficjalnego wydania.
- Musi być dostępne na Linuksa, macOS i Windows.
- Wszelkie zmiany mające na celu zwiększenie prywatności nie mogą negatywnie wpływać na doświadczenie użytkownika.
- Musi domyślnie blokować ciasteczka stron trzecich.
- Musi obsługiwać [partycjonowanie stanu](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning), aby ograniczać śledzenie między stronami.[^1]

### Najlepszy scenariusz

Nasze kryteria najlepszego scenariusza określają, czego oczekiwalibyśmy od idealnego projektu w tej kategorii. Nie wszystkie nasze rekomendacje muszą spełniać wszystkie te wymagania, jednak te, które je spełniają, mogą być oceniane wyżej od pozostałych na tej stronie.

- Powinien mieć wbudowaną funkcję blokowania treści.
- Powinien obsługiwać izolację ciasteczek (na wzór [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Powinien obsługiwać progresywne aplikacje internetowe (PWA). PWA umożliwiają instalowanie wybranych stron internetowych tak, jakby były natywnymi aplikacjami na komputerze. To rozwiązanie ma przewagę nad instalowaniem aplikacji opartych na Electronie, ponieważ PWA korzystają z regularnych aktualizacji bezpieczeństwa przeglądarki.
- Nie powinien zawierać dodatkowych funkcji (bloatware), które nie wpływają na prywatność użytkownika.
- Nie powinien domyślnie zbierać danych telemetrycznych.
- Powinien udostępniać otwartoźródłową implementację serwera synchronizacji.
- Domyślnie powinien korzystać z [prywatnej wyszukiwarki](search-engines.md).

[^1]: Implementacja Brave została opisana szczegółowo w [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
