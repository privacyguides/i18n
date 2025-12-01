---
title: Przegląd systemu iOS
icon: simple/apple
description: iOS to system operacyjny na urządzenia mobilne opracowany przez Apple dla iPhone’a.
---

**iOS** i **iPadOS** są zamkniętymi systemami operacyjnymi na urządzenia mobilne opracowanymi przez Apple odpowiednio dla produktów iPhone i iPad. Jeśli posiadasz urządzenie mobilne Apple, możesz zwiększyć swoją prywatność, wyłączając niektóre wbudowane funkcje telemetrii oraz wzmacniając ustawienia prywatności i zabezpieczeń dostępne w systemie.

## Uwagi dotyczące prywatności

Urządzenia z systemem iOS są często chwalone przez ekspertów ds. bezpieczeństwa za solidną ochronę danych i przestrzeganie nowoczesnych najlepszych praktyk. Jednak restrykcyjność ekosystemu Apple — zwłaszcza w przypadku urządzeń mobilnych — wciąż ogranicza prywatność na kilka sposobów.

Ogólnie rzecz biorąc, uważamy, że iOS zapewnia lepsze niż przeciętne poziomy ochrony prywatności i bezpieczeństwa dla większości osób w porównaniu ze standardowymi urządzeniami z Androidem od dowolnego producenta. Jeżeli jednak chcesz lub potrzebujesz całkowitej niezależności od usług chmurowych Apple i Google, jeszcze wyższy poziom prywatności można osiągnąć przy użyciu [niestandardowego systemu Android](../android/distributions.md), takiego jak GrapheneOS.

### Blokada aktywacji

Wszystkie urządzenia z systemem iOS sprawdzane są na serwerach blokady aktywacji Apple podczas pierwszej konfiguracji lub resetu, co oznacza, że połączenie z Internetem jest **wymagane**, by korzystać z urządzenia z systemem iOS.

### Obowiązkowa aplikacja App Store

The only source for apps on iOS is Apple's App Store, which requires an Apple Account to access. This means that Apple has a record of every app you install on your device, and can likely tie that information to your actual identity if you provide the App Store with a payment method.

### Inwazyjna telemetria

Apple miało w przeszłości problemy z odpowiednim odłączaniem telemetrii od kont Apple w systemie iOS. [W 2019 roku](https://theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings) wykazano, że nagrania z Siri — niektóre zawierające wysoce poufne informacje — były przesyłane na serwery Apple do ręcznej weryfikacji przez zewnętrznych wykonawców. Choć Apple tymczasowo wstrzymało ten program po [nagłośnieniu sprawy](https://theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana), w kolejnej aktualizacji wprowadzono możliwość [**rezygnacji** z przesyłania rozmów z Siri](https://theguardian.com/technology/2019/oct/30/apple-lets-users-opt-out-of-having-siri-conversations-recorded). Ponadto w 2021 roku [Apple przeprojektowało Siri](https://theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance) tak, aby nagrania głosowe były przetwarzane lokalnie zamiast wysyłania ich na swoje serwery.

Nowsze ustalenia wskazują, że Apple przesyła dane analityczne [nawet wtedy, gdy udostępnianie analiz jest wyłączone](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) na urządzeniu, i [wygląda na to](https://twitter.com/mysk_co/status/1594515229915979776), że te dane można stosunkowo łatwo powiązać z unikatowymi identyfikatorami kont iCloud, mimo iż miały być od nich oddzielone.

### Ruch poza aktywnymi połączeniami VPN

[Polityka prywatności Apple dotycząca sieci VPN](https://apple.com/legal/privacy/data/en/vpns) stwierdza:

> Nawet gdy sieć VPN jest aktywna, część ruchu niezbędna dla kluczowych usług systemowych musi odbywać się poza nią, aby urządzenie mogło prawidłowo działać.

## Zalecana konfiguracja

**Uwaga:** ten przewodnik zakłada, że korzystasz z najnowszej wersji systemu iOS.

### iCloud

Większość obaw związanych z prywatnością i bezpieczeństwem w produktach Apple wiąże się z usługami chmurowymi, a nie z samym sprzętem czy oprogramowaniem. Gdy korzystasz z usług Apple, takich jak iCloud, większość Twoich informacji przechowywana jest na ich serwerach i zabezpieczona kluczami, do których Apple ma domyślnie dostęp. Możesz sprawdzić [dokumentację Apple](https://support.apple.com/HT202303), aby dowiedzieć się, które usługi są szyfrowane end-to-end. Wszystko oznaczone jako „podczas transferu” lub „na serwerze” oznacza, że Apple może uzyskać dostęp do tych danych bez Twojej zgody. Taki poziom dostępu był czasami wykorzystywany przez organy ścigania, by obejść fakt, że dane są w inny sposób bezpiecznie zaszyfrowane na urządzeniu, a Apple, jak każda inna firma, jest także podatne na wycieki danych.

Dlatego, jeśli korzystasz z iCloud, zaleca się [włączenie **zaawansowanej ochrony danych**](https://support.apple.com/HT212520). Szyfruje to niemal wszystkie dane iCloud za pomocą kluczy przechowywanych na Twoich urządzeniach (szyfrowanie typu end-to-end), zamiast na serwerach Apple, dzięki czemu dane iCloud są zabezpieczone na wypadek wycieku i w normalnych warunkach ukryte przed Apple.

Szyfrowanie stosowane w zaawansowanej ochronie danych, choć silne, [nie jest *tak* odporne](https://discuss.privacyguides.net/t/apple-advances-user-security-with-powerful-new-data-protections/10778/4) jak szyfrowanie oferowane przez niektóre inne [usługi chmurowe](../cloud.md), zwłaszcza w przypadku iCloud Drive. Choć zdecydowanie zachęcamy do włączenia zaawansownej ochrony danych, jeśli korzystasz z iCloud, warto też rozważyć alternatywę dla iCloud u [dostawcy bardziej nastawionego na prywatność](../tools.md) — choć dla większości osób wspomniane niuanse szyfrowania prawdopodobnie nie będą miały większego znaczenia.

Możesz też chronić swoje dane, ograniczając to, co synchronizujesz z iCloud. Na górze aplikacji **Ustawienia** zobaczysz swoje imię i nazwisko oraz zdjęcie profilowe, jeśli zalogowano się do usługi iCloud. Wybierz je, następnie **iCloud**, i wyłącz wszystko przy usługach, których nie chcesz synchronizować z iCloud. Pod opcją **Pokaż wszystkie** mogą pojawić się aplikacje firm trzecich synchronizujące się z usługą iCloud — można je tutaj wyłączyć.

#### iCloud+

Płatna subskrypcja **iCloud+** (dowolny pakiet dyskowy w usłudze iCloud) zawiera funkcje chroniące prywatność. Choć dla obecnych klientów iCloud mogą one być wystarczające, nie zalecamy kupowania planu iCloud+ wyłącznie dla tych funkcji zamiast korzystania z [VPN-a](../vpn.md) i [samodzielnej usługi aliasingu e-mail](../email-aliasing.md).

[**Przekazywanie prywatne**](https://apple.com/legal/privacy/data/en/icloud-relay) to usługa proxy, która przekierowuje ruch z Safari, zapytania DNS oraz niezaszyfrowany ruch urządzenia przez dwa serwery: jeden należący do Apple i drugi do zewnętrznego dostawcy (m.in. Akamai, Cloudflare i Fastly). W teorii uniemożliwia to któremukolwiek z pojedynczych dostawców w łańcuchu — w tym Apple — uzyskanie pełnego wglądu w odwiedzane przez Ciebie strony. W przeciwieństwie do VPN, Przekazywanie prywatne nie chroni ruchu, który jest już zaszyfrowany.

**Ukryj mój adres email** to usługa aliasingu adresów e-mail oferowana przez Apple. Można tworzyć aliasy e-mail za darmo, korzystając z funkcji *Zaloguj się, używając konta Apple* na stronie lub w aplikacji, albo generować nieograniczoną liczbę aliasów na żądanie mając płatny pakiet iCloud+. Usługa Ukryj mój adres email ma tę przewagę, że używa domeny `@icloud.com` dla aliasów, co może zmniejszać ryzyko zablokowania w porównaniu z innymi usługami aliasingu, ale nie oferuje funkcji dostępnych w samodzielnych usługach, takich jak automatyczne szyfrowanie PGP czy obsługa wielu skrzynek pocztowych.

#### Multimedia i zakupy

Na górze aplikacji **Ustawienia** zobaczysz swoje imię i nazwisko oraz zdjęcie profilowe, jeśli zalogowano się na konto Apple. Wybierz je, następnie **Multimedia i zakupy** → **Wyświetl konto**.

- [ ] Wyłącz **Spersonalizowane rekomendacje**

#### Usługa Znajdź

**Znajdź** to usługa pozwalająca śledzić urządzenia Apple i udostępniać ich lokalizację znajomym i rodzinie. Umożliwia też zdalne wymazanie urządzenia w razie kradzieży, co zapobiega dostępowi niepożądanych osób do danych. Twoje dane lokalizacji w ramach usługi Znajdź [są szyfrowane end-to-end](https://apple.com/legal/privacy/data/en/find-my), gdy:

- lokalizacja jest udostępniana członkowi rodziny lub znajomemu i obie strony używają systemu iOS 17 lub nowszego,
- urządzenie jest offline i zlokalizowane przez sieć usługi Znajdź.

Dane lokalizacji nie są szyfrowane end-to-end, gdy urządzenie jest online i korzystasz z funkcji Znajdź mój iPhone do zdalnego zlokalizowania urządzenia. Trzeba więc rozważyć, czy te kompromisy są warte korzyści antykradzieżowych związanych z blokadą aktywacji.

Na górze aplikacji **Ustawienia** zobaczysz swoje imię i nazwisko oraz zdjęcie profilowe, jeśli zalogowano się na konto Apple. Wybierz je, a następnie opcję **Znajdź**. Tutaj możesz zdecydować, czy chcesz włączyć, czy wyłączyć funkcje lokalizacji usługi Znajdź.

### Ustawienia

Wiele innych ustawień związanych z prywatnością znajdziesz w aplikacji **Ustawienia**.

#### Tryb Samolot

Włączenie **trybu Samolot** (szerzej znanego jako **tryb samolotowy**) zatrzymuje łączenie telefonu z wieżami komórkowymi. Nadal możesz łączyć się z Wi-Fi i Bluetooth, więc zawsze, gdy masz połączenie z Wi-Fi, możesz włączyć tę opcję.

#### Wi-Fi

Możesz włączyć [losowanie adresu sprzętowego](https://support.apple.com/pl-pl/102509#triswitch), aby chronić się przed śledzeniem w różnych sieciach Wi-Fi oraz w tej samej sieci w czasie. W aktualnie używanej sieci naciśnij przycisk :material-information::

- [x] Ustaw **Prywatny adres Wi‑Fi** na **Stały** lub **Obrotowy**

Dostępna jest również opcja **Ograniczaj śledzenie adresu IP**. Działa to podobnie do funkcji Prywatne przekazywanie iCloud, ale dotyczy tylko połączeń ze „znanymi trackerami”. Ponieważ wpływa wyłącznie na połączenia z potencjalnie złośliwymi serwerami, ustawienie to można pozostawić włączone, ale jeśli nie chcesz, żeby *jakikolwiek* ruch przechodził przez serwery Apple, wyłącz je.

#### Bluetooth

**Bluetooth** powinien być wyłączony, gdy go nie używasz, ponieważ zwiększa on powierzchnię ataku. Wyłączenie Bluetooth (lub Wi-Fi) z Centrum sterowania jest tymczasowe: aby było skuteczne na stałe, trzeba wyłączyć je w Ustawieniach.

- [ ] Wyłącz **Bluetooth**

Należy pamiętać, że Bluetooth jest automatycznie włączany po każdej aktualizacji systemu.

#### Ogólne

Domyślna nazwa urządzenia Twojego iPhone'a zawiera Twoje imię i będzie widoczna dla każdego w sieciach, do których się łączysz. Zmień ją na coś bardziej ogólnego, jak „iPhone”. Wybierz **To urządzenie** → **Nazwa** i wpisz preferowaną nazwę urządzenia.

Ważne jest częste instalowanie aktualizacji oprogramowania, żeby otrzymywać najnowsze poprawki zabezpieczeń. Możesz włączyć automatyczne aktualizacje, żeby telefon był na bieżąco bez konieczności ręcznego sprawdzania dostępności aktualizacji. Wybierz **Uaktualnienia** → **Uaktualnienia automatyczne**:

- [x] Włącz **Instaluj automatycznie**

**AirDrop** jest często używany do łatwego udostępniania plików, ale stanowi istotne ryzyko prywatności. Protokół AirDrop stale rozgłasza informacje o użytkowniku w otoczeniu i ma [bardzo słabe](https://usenix.org/system/files/sec21-heinrich.pdf) zabezpieczenia. Twoją tożsamość można stosunkowo łatwo odkryć nawet przy ograniczonych zasobach, a chińskie władze [otwarcie przyznały się](https://arstechnica.com/security/2024/01/hackers-can-id-unique-apple-airdrop-users-chinese-authorities-claim-to-do-just-that) do wykorzystywania takich technik do identyfikacji użytkowników AirDrop w miejscach publicznych od 2022 r.

- [x] Wybierz **AirDrop** → **Odbieranie wyłączone**

**AirPlay** pozwala płynnie przesyłać treści z iPhone’a na telewizor; nie zawsze jednak chcesz robić to automatycznie. Wybierz **AirPlay i Continuity** → **AirPlay automatycznie**:

- [x] Wybierz **Nigdy** lub **Zapytaj**

Funkcja **Odświeżanie w tle** pozwala aplikacjom odświeżać zawartość, gdy z nich nie korzystasz. Może to powodować nawiązywanie niechcianych połączeń. Wyłączenie tej opcji może także oszczędzić czas pracy baterii, ale może wpłynąć na zdolność aplikacji do otrzymywania aktualizacji, w szczególności aplikacji pogodowych i komunikatorów.

Wybierz **Odświeżanie w tle** i wyłącz wszystkie aplikacje, które nie powinny odświeżać się w tle. Jeśli nie chcesz, aby jakiekolwiek aplikacje odświeżały się w tle, wybierz **Odświeżanie w tle** i ustaw **Wyłączone**.

#### Apple Intelligence i Siri

Funkcja ta jest dostępna, jeśli urządzenie obsługuje **[Apple Intelligence](https://support.apple.com/guide/iphone/apple-intelligence-and-privacy-iphe3f499e0e/ios)**. Apple Intelligence używa kombinacji przetwarzania na urządzeniu oraz ich **[prywatnej chmury obliczeniowej](https://security.apple.com/blog/private-cloud-compute)** do zadań wymagających większej mocy obliczeniowej niż ta dostępna lokalnie.

Aby zobaczyć raport wszystkich żądań wysłanych do serwerów Apple, przejdź do **Prywatność i bezpieczeństwo** → **Raport Apple Intelligence** i naciśnij **Eksportuj aktywność**, aby zobaczyć dane z ostatnich 15 minut lub 7 dni, w zależności od wybranej przez Ciebie opcji. Podobnie jak **Raport prywatności aplikacji**, który pokazuje ostatnie uprawnienia, do których uzyskały dostęp aplikacje w telefonie, Raport Apple Intelligence pokazuje, co jest wysyłane do serwerów Apple podczas korzystania z Apple Intelligence.

Apple Intelligence może integrować się z [ChatGPT](https://support.apple.com/guide/iphone/use-chatgpt-with-apple-intelligence-iph00fd3c8c2/ios). Aby dodać integrację z ChatGPT, przejdź do **ChatGPT** i naciśnij **Skonfiguruj**. Aby ją wyłączyć, przejdź w to samo miejsce:

- [ ] Wyłącz **Używaj ChatGPT**

Możesz też ustawić, żeby prośby były potwierdzane za każdym razem, jeśli integracja z ChatGPT jest włączona:

- [x] Włącz **Potwierdzaj polecenia ChatGPT**

Jeśli nie chcesz, aby ktoś mógł sterować Twoim telefonem za pomocą Siri, gdy jest on zablokowany, możesz to tutaj wyłączyć.

- [ ] Wyłącz **Dostęp do Siri przy blokadzie**

#### Face ID/Touch ID oraz kod

Ustawienie silnego hasła na telefonie to najważniejszy krok, jaki możesz podjąć w celu fizycznego zabezpieczenia urządzenia. Trzeba tu pogodzić wygodę z bezpieczeństwem: dłuższe hasło będzie irytujące przy każdorazowym wpisywaniu, natomiast krótsze hasło lub kod PIN będą łatwiejsze do odgadnięcia. Połączenie Face ID lub Touch ID z silnym hasłem to często dobry kompromis między użytecznością a bezpieczeństwem.

Wybierz **Włącz kod** lub **Zmień kod** → **Opcje kodu** → **Własny kod alfanumeryczny**. Upewnij się, że utworzysz [bezpieczne hasło](../basics/passwords-overview.md).

Jeżeli chcesz korzystać z Face ID lub Touch ID, możesz je skonfigurować teraz. Telefon będzie używać ustawionego wcześniej hasła jako zapasowej metody uwierzytelniania na wypadek niepowodzenia weryfikacji biometrycznej. Metody biometryczne służą głównie wygodzie, choć zapobiegają obserwowaniu wpisywanego kodu przez kamery monitoringu czy osoby stojące za Twoimi plecami.

Jeżeli używasz biometrii, warto wiedzieć, jak szybko ją wyłączyć w sytuacji awaryjnej. Przytrzymanie [przycisku bocznego](https://support.apple.com/pl-pl/105103) oraz *dowolnego* przycisku głośności, aż pojawi się suwak Wyłącz, spowoduje wyłączenie biometrii, wymagając podania kodu do odblokowania. Kod będzie wymagany po ponownym uruchomieniu urządzenia.

Podobnie można wyłączyć biometrię, naciskając pięć razy przycisk boczny, a w urządzeniach z Touch ID — przytrzymując jedynie przycisk boczny. Wypróbuj to wcześniej, aby wiedzieć, która metoda działa na Twoim urządzeniu.

**Ochrona skradzionego urządzenia** zapewnia dodatkowe zabezpieczenia mające chronić Twoje dane osobowe, jeśli urządzenie zostanie skradzione, gdy jest ono odblokowane. Jeśli włączysz zarówno uwierzytelnianie biometryczne, jak i funkcję [Znajdź](#find-my) mój iPhone, zalecamy włączenie tej ochrony:

- [x] Włącz **Ochrona skradzionego urządzenia**

Po włączeniu funkcji Ochrona skradzionego urządzenia [niektóre działania](https://support.apple.com/HT212510) będą wymagać uwierzytelnienia biometrycznego bez możliwości użycia hasła jako zapasowej metody (na wypadek, gdyby ktoś podglądający Twoje urządzenie uzyskał dostęp do Twojego kodu PIN), np. korzystanie z funkcji automatycznego wypełniania haseł, dostęp do informacji płatniczych czy wyłączenie trybu Utracony. Dodatkowo wprowadza opóźnienia bezpieczeństwa dla niektórych działań wykonywanych poza domem lub „znaną lokalizacją”, np. wymaga godziny na zresetowanie hasła do konta Apple lub wylogowania się z konta Apple. Opóźnienie to ma dać czas na włączenie trybu Utracony i zabezpieczenie konta, zanim złodziej będzie mógł zresetować urządzenie.

Opcja **Pozwalaj na dostęp z ekranu blokady** udostępnia opcje dotyczące tego, na co można zezwolić, gdy telefon jest zablokowany. Wybierz funkcje, które chcesz wyłączyć, aby zapobiec nieautoryzowanemu dostępowi, jeśli Twój telefon trafi w niepowołane ręce. Im więcej opcji wyłączysz, tym mniejszy zakres działań będzie dostępny bez podania hasła, ale jednocześnie zmniejszy się wygoda użytkowania dla Ciebie.

iPhone’y są odporne na ataki typu brute-force, wymuszając długie przerwy po wielu nieudanych próbach; jednak historycznie pojawiały się exploity omijające te zabezpieczenia. Dla dodatkowego bezpieczeństwa możesz ustawić automatyczne wymazanie urządzenia po 10 nieudanych próbach wpisania kodu.

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

Po włączeniu tego ustawienia ktoś mógłby celowo wymazać Twój telefon, wielokrotnie wpisując nieprawidłowe hasło. Upewnij się, że masz odpowiednie kopie zapasowe i włącz tę opcję tylko wtedy, jeśli czujesz się z nią komfortowo.

</div>

- [x] Włącz **Wymaż dane**

#### Prywatność i bezpieczeństwo

**Usługi lokalizacji** pozwalają na korzystanie z funkcji takich jak Mapy czy Znajdź. Jeśli nie potrzebujesz tych funkcji, możesz wyłączyć usługi lokalizacji. Alternatywnie możesz przejrzeć listę aplikacji i wybrać te, które mogą korzystać z Twojej lokalizacji. Wybierz **Usługi lokalizacji**:

- [ ] Wyłącz **Usługi lokalizacji**

Fioletowa strzałka przy aplikacji w tych ustawieniach oznacza, że aplikacja niedawno korzystała z lokalizacji; szara strzałka oznacza dostęp w ciągu ostatnich 24 godzin. Jeśli postanowisz pozostawić włączone usługi lokalizacyjne, Apple domyślnie użyje ich do usług systemowych. Możesz przeglądać i wyłączyć wybrane usługi systemowe. Jeżeli nie chcesz przesyłać danych analitycznych dotyczących lokalizacji do Apple, które są używane m.in. do poprawy map Apple Maps, możesz to tutaj wyłączyć. Wybierz **Usługi systemowe**:

- [ ] Wyłącz **Dane analizy iPhone’a**
- [ ] Wyłącz **Nawigacja i ruch**
- [ ] Wyłącz **Ulepszanie Map**

Możesz zdecydować, czy aplikacjom wolno prosić o możliwość **śledzenia** Cię. Wyłączenie tej opcji uniemożliwia wszystkim aplikacjom śledzenie za pomocą identyfikatora reklamowego telefonu. Wybierz **Śledzenie**:

- [ ] Wyłącz **Pozwalaj aplikacjom prosić o śledzenie**

Opcja ta jest domyślnie wyłączona i nie można jej zmienić dla użytkowników poniżej 18 roku życia.

Jeżeli nie chcesz brać udziału w badaniach, wyłącz opcję **Dane z czujników badawczych i dane użycia**. Wybierz **Dane z czujników badawczych i dane użycia**:

- [ ] Wyłącz **Dane z czujników badawczych i dane użycia**

**[Kontrola bezpieczeństwa](https://support.apple.com/guide/personal-safety/safety-check-iphone-ios-16-ips2aad835e1/1.0/web/1.0)** pozwala szybko przeglądać i cofać uprawnienia nadane osobom i aplikacjom, które mogą mieć dostęp do Twoich danych. Można tu wykonać **Zerowanie awaryjne**, natychmiast resetując uprawnienia dla wszystkich osób i aplikacji mających dostęp do zasobów urządzenia. Można też skorzystać z funkcji **Zarządzaj udostępnianiem i dostępem**, aby przeglądać i dostosowywać, kto i co ma dostęp do zasobów urządzenia i konta. Jeżeli znajdujesz się w sytuacji nadużyć, przeczytaj [Podręcznik bezpieczeństwa osobistego Apple](https://support.apple.com/guide/personal-safety/welcome/web), aby uzyskać wskazówki, co należy zrobić.

Jeżeli nie chcesz wysyłać danych o użytkowaniu do Apple, wyłącz dane analityczne. Wybierz **Analizy i udoskonalenia** i odznacz typ(y) danych analitycznych, których nie chcesz wysyłać do Apple.

Wyłącz **Reklamy spersonalizowane**, jeśli nie chcesz otrzymywać reklam dopasowanych do Twoich zainteresowań. Wybierz **Reklamy Apple**:

- [ ] Wyłącz **Reklamy spersonalizowane**

**Raport prywatności aplikacji** to wbudowane narzędzie pokazujące, których uprawnień używają aplikacje. Wybierz **Raport prywatności aplikacji**:

- [x] Wybierz **Włącz Raport prywatności aplikacji**

Ustaw akcesoria przewodowe tak, by prosiły o pozwolenie przy ich podłączaniu. Wybierz **Akcesoria przewodowe**:

- [x] Wybierz **Zawsze pytaj** lub **Pytaj w przypadku nowych akcesoriów**

**[Tryb blokady](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode)** to ustawienie bezpieczeństwa, które możesz włączyć, by zwiększyć odporność telefonu na ataki. Pamiętaj, że niektóre aplikacje i funkcje mogą wtedy [nie działać](https://support.apple.com/HT212650) tak, jak zwykle.

- [x] Wybierz **Włącz tryb blokady**

## Dodatkowe zalecenia

### Połączenia E2EE

Normalne połączenia telefoniczne wykonywane przez aplikację Telefon za pośrednictwem operatora nie są połączeniami E2EE. Zarówno połączenia FaceTime wideo, jak i FaceTime audio są połączeniami E2EE. Alternatywnie można użyć [innej aplikacji](../real-time-communication.md), np. Signal, do połączeń E2EE.

### Szyfrowane wiadomości iMessage

[Kolor dymku wiadomości](https://support.apple.com/en-us/104972) w aplikacji Wiadomości wskazuje, czy wiadomości są E2EE, czy nie. Niebieski dymek oznacza, że używasz iMessage z E2EE, natomiast zielony — że druga strona używa przestarzałych protokołów SMS/MMS lub RCS. RCS w systemie iOS **nie jest** E2EE. Obecnie jedynym sposobem na E2EE w aplikacji Wiadomości jest używanie iMessage przez obie strony na urządzeniach Apple.

Jeżeli Ty lub Twój rozmówca macie włączoną funkcję Backup w iCloud bez zaawansowanej ochrony danych, klucz szyfrowania będzie przechowywany na serwerach Apple, co oznacza, że Apple może mieć dostęp do Twoich wiadomości.

Domyślnie ufasz serwerom tożsamości Apple, że wysyłasz wiadomość do właściwej osoby. Aby chronić się przed potencjalnie złośliwym serwerem, można włączyć funkcję**[Weryfikacji kluczy kontaktów](https://support.apple.com/pl-pl/118246)**. W aplikacji **Ustawienia** w górnej części aplikacji, gdzie widnieje Twoje imię, wybierz je, a następnie **Weryfikacja kluczy kontaktów**.

- [x] Włącz **Weryfikacja kluczy kontaktów**

Zarówno Ty, jak i Twoje kontakty musicie włączyć weryfikację kluczy kontaktów i postępować zgodnie z [instrukcjami](https://support.apple.com/pl-pl/118246#verify) Apple, aby wymienione tam zabezpieczenia zaczęły działać.

### Uprawnienia do zdjęć

Gdy aplikacja poprosi o dostęp do biblioteki zdjęć, iOS daje opcje ograniczenia, które zdjęcia aplikacja może zobaczyć.

Zamiast zezwalać na dostęp do wszystkich zdjęć, możesz pozwolić jedynie na wybrane zdjęcia, wybierając w oknie uprawnień opcję „Wybierz zdjęcia...”. Dostęp do zdjęć można zmieniać w dowolnym momencie, przechodząc do: **Ustawienia** → **Prywatność i bezpieczeństwo** → **Zdjęcia**.

![Uprawnienia do zdjęć](../assets/img/ios/photo-permissions-light.png#only-light) ![Uprawnienia do zdjęć](../assets/img/ios/photo-permissions-dark.png#only-dark)

**Dodaj tylko zdjęcia** to uprawnienie, które pozwala aplikacji tylko zapisywać zdjęcia do biblioteki. Nie wszystkie aplikacje proszące o dostęp do biblioteki oferują tę opcję.

![Private Access](../assets/img/ios/private-access-light.png#only-light) ![Private Access](../assets/img/ios/private-access-dark.png#only-dark)

Some apps also support **Private Access**, which functions similarly to the **Limited Access** permission. However, photos shared to apps using Private Access include their location by default. Zalecamy wyłączenie tej opcji, jeśli wcześniej [nie usuniesz metadanych zdjęć](../data-redaction.md).

### Uprawnienia do kontaktów

Podobnie jak ze zdjęciami, zamiast pozwalać aplikacji na dostęp do wszystkich kontaktów, można zezwolić jej tylko na wybrane kontakty. Uprawnienia do kontaktów można zmieniać w dowolnym momencie, przechodząc do: **Ustawienia** → **Prywatność i bezpieczeństwo** → **Kontakty**.

![Uprawnienia do kontaktów](../assets/img/ios/contact-permissions-light.png#only-light) ![Uprawnienia do kontaktów](../assets/img/ios/contact-permissions-dark.png#only-dark)

### Wymagaj biometrii i ukrywaj aplikacje

iOS pozwala zablokować większość aplikacji przy użyciu Face ID/Touch ID lub kodu, co jest przydatne do ochrony wrażliwych treści w aplikacjach, które same takiej funkcji nie oferują. Aplikację można zablokować, przytrzymując jej ikonę i wybierając **Wymagaj Face ID/Touch ID**. Tak zabezpieczone aplikacje wymagają uwierzytelnienia przy każdym otwarciu lub przy próbie dostępu do ich zawartości z innych aplikacji; podglądy powiadomień dla zablokowanych aplikacji nie będą również wyświetlane.

Oprócz blokowania można ukryć aplikacje, aby nie pojawiały się na ekranie głównym, w bibliotece aplikacji, na liście w aplikacji **Ustawienia** itp. Ukrywanie bywa przydatne, gdy trzeba komuś podać odblokowany telefon, ale nie daje absolutnej ochrony — ukryta aplikacja nadal bywa widoczna w niektórych miejscach, np. w statystykach zużycia baterii. Przy ukrywaniu aplikacji tracisz też powiadomienia z niej.

Aplikację można ukryć, przytrzymując jej ikonę i wybierając **Wymagaj Face ID/Touch ID** → **Ukryj i wymagaj Face ID/Touch ID**. Należy pamiętać, że preinstalowane aplikacje Apple oraz domyślna przeglądarka internetowa i aplikacja poczty e-mail nie mogą zostać ukryte. Ukryte aplikacje znajdują się w folderze **Ukryte** na dole biblioteki aplikacji, który można odblokować biometrią. Folder ten pojawia się w bibliotece aplikacji niezależnie od tego, czy cokolwiek ukryto, co daje pewien margines zaprzeczalności.

### Dostęp nadzorowany

Czasami możesz chcieć podać telefon komuś, by wykonał połączenie lub wykonał konkretną czynność, nie dając mu jednocześnie pełnego dostępu do Twojego urządzenia. W takich sytuacjach możesz szybko włączyć funkcję **[Dostęp nadzorowany](https://support.apple.com/guide/iphone/lock-iphone-to-one-app-iph7fad0d10/ios)**, aby zablokować telefon w jednej konkretnej aplikacji do czasu uwierzytelnienia.

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

Dostęp nadzorowany nie jest niezawodny — istnieje ryzyko niezamierzonego wycieku danych albo obejścia funkcji. Używaj go tylko do sytuacji, gdy jedynie okazjonalnie podajesz komuś telefon do użycia. Nie stosuj go jako środka ochrony przed zaawansowanymi przeciwnikami.

</div>

### Redagowanie elementów na zdjęciach

Jeśli chcesz ukryć informacje na zdjęciu, możesz skorzystać z wbudowanych narzędzi do edycji Apple.

Na obsługiwanych urządzeniach dostępna jest funkcja [Oczyść](https://support.apple.com/en-us/121429), która pozwala zamazać twarze lub usunąć obiekty ze zdjęć.

- Otwórz aplikację **Zdjęcia** i wybierz zdjęcie przeznaczone do redakcji.
- Naciśnij :material-tune:.
- Naciśnij przycisk **Oczyść**.
- Narysuj kółko wokół tego, co chcesz zredagować. Twarze zostaną rozpikselowane, a system spróbuje usunąć inne elementy.

Nasze ostrzeżenie [przed rozmyciem tekstu](../data-redaction.md) ma tu również zastosowanie — zalecamy zamiast tego dodać czarny kształt ze 100% kryciem. Oprócz przeredagowania tekstu możesz też całkowicie zamalować twarz lub obiekt za pomocą aplikacji **Zdjęcia**:

<div class="annotate" markdown>

- Wybierz zdjęcie do redakcji.
- Naciśnij :material-tune: → :material-dots-horizontal: (1) → Oznaczenia → :material-plus:
- Wybierz **Dodaj kształt** i wybierz kwadrat lub okrąg.
- Na pasku narzędzi naciśnij okrąg i ustaw kolor wypełnienia na czarny. Możesz także przesunąć kształt i powiększyć go według potrzeby.

</div>

1. Opcja ta może nie pojawić się na niektórych modelach iPhone’a.

**Nie** używaj zakreślacza do ukrywania informacji — jego krycie nie wynosi 100%.

### Unikaj jailbreaku

Jailbreaking iPhone’a podważa jego bezpieczeństwo i naraża urządzenie na ataki. Uruchamianie niezaufanego oprogramowania firm trzecich może spowodować zainfekowanie urządzenia złośliwym oprogramowaniem.

### Wersje beta iOS

Apple udostępnia wersje beta systemu iOS osobom chętnym do znajdowania i zgłaszania błędów. Nie zalecamy instalowania oprogramowania w wersji beta na telefonie. Wersje beta mogą być niestabilne i zawierać nieodkryte luki bezpieczeństwa.

## Najważniejsze zagadnienia dotyczące bezpieczeństwa

### Przed pierwszym odblokowaniem

Jeśli w Twój model zagrożeń obejmuje [:material-target-account: Ataki ukierunkowane](../basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} wykorzystujące narzędzia kryminalistyczne, i chcesz zminimalizować ryzyko wykorzystania exploitów w celu dostępu do Twojego telefonu, warto często restartować urządzenie. Stan *po* ponownym uruchomieniu, ale *przed* pierwszym odblokowaniem urządzenia określany jest jako „Before First Unlock” (BFU, dosł. *przed pierwszym odblokowaniem*) — w tym stanie korzystanie z narzędzi sądowo-śledczych jest [znacząco utrudnione](https://belkasoft.com/checkm8_glossary). Stan BFU pozwala odbierać powiadomienia o połączeniach, SMS-ach i alarmach, podczas gdy większość danych na urządzeniu pozostaje zaszyfrowana i niedostępna. Może to być niepraktyczne, więc oceń, czy te kompromisy mają sens w Twojej sytuacji.

iPhone’y [automatycznie uruchamiają się ponownie](https://support.apple.com/guide/security/protecting-user-data-in-the-face-of-attack-secf5549a4f5/1/web/1#:~:text=On%20an%20iPhone%20or%20iPad%20with%20iOS%2018%20and%20iPadOS%2018%20or%20later%2C%20a%20new%20security%20protection%20will%20restart%20devices%20if%20they%20remain%20locked%20for%20a%20prolonged%20period%20of%20time.), jeśli nie są odblokowane przez pewien czas.

### MTE

Linia iPhone 17 i nowsze oferują rozszerzenie zabezpieczeń zwane [Memory Tagging Extension](https://developer.arm.com/documentation/108035/0100/Introduction-to-the-Memory-Tagging-Extension) (MTE), które znacznie utrudnia atakującemu wykorzystanie błędów korupcji pamięci. To stale aktywne zabezpieczenie zależy od wsparcia sprzętowego, więc nie jest dostępne na starszych urządzeniach.

Szczegóły implementacji MTE przez Apple można znaleźć we [wpisie na blogu](https://security.apple.com/blog/memory-integrity-enforcement) Apple Security Research. Opisujemy też implementację MTE przez Apple i porównujemy ją z implementacją Androida w seriach Google Pixel 8 i nowszych w [naszym artykule](https://www.privacyguides.org/posts/2025/09/20/memory-integrity-enforcement-changes-the-game-on-ios).
