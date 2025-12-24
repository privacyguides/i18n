---
title: "Przegląd sieci Tor"
icon: 'simple/torproject'
description: Tor to bezpłatna, zdecentralizowana sieć zaprojektowana z myślą o możliwie największej prywatności podczas korzystania z Internetu.
---

![Logo Tor](../assets/img/self-contained-networks/tor.svg){ align=right }

[**Tor**](../alternative-networks.md#tor) to bezpłatna, zdecentralizowana sieć zaprojektowana tak, by umożliwiać korzystanie z Internetu z jak największym zachowaniem prywatności. Jeśli jest używana prawidłowo, sieć umożliwia prywatne i anonimowe przeglądanie oraz komunikację. Dzięki temu, że ruch w sieci Tor jest trudny do zablokowania i namierzenia, Tor stanowi skuteczne narzędzie do omijania cenzury.

[:material-movie-open-play-outline: Wideo: Dlaczego potrzebujesz Tora](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

Tor działa, kierując ruch internetowy przez serwery obsługiwane przez wolontariuszy, zamiast nawiązywać bezpośrednie połączenie ze stroną, którą próbuje się odwiedzić. Zaciera to informację, skąd pochodzi ruch — żaden serwer na trasie połączenia nie widzi pełnej ścieżki, skąd ruch pochodzi i dokąd zmierza, więc nawet serwery używane do połączenia nie są w stanie złamać Twojej anonimowości.

[:octicons-home-16:](https://torproject.org/pl){ .card-link title="Strona główna"}
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Usługa .onion" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Dokumentacja}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title="Wspomóż projekt" }

## Bezpieczne łączenie się z siecią Tor

Przed połączeniem się z siecią Tor należy dokładnie rozważyć, co chce się osiągnąć za jej pomocą, i przed kim próbuje się ukryć swoją aktywność w sieci.

Jeśli mieszkasz w wolnym kraju, korzystasz z Tora do przeglądania zwykłych treści, nie obawiasz się, że Twój dostawca usług internetowych (ISP) lub administratorzy lokalnej sieci dowiedzą się, że korzystasz z Tora i chcesz pomóc w [zniesieniu piętna](https://2019.www.torproject.org/about/torusers.html.en) związanego z korzystaniem z Tora, prawdopodobnie możesz bez obaw połączyć się z siecią Tor bezpośrednio za pomocą standardowych metod, np. przez przeglądarkę [Tor Browser](../tor.md).

Jeśli masz możliwość skorzystania z zaufanego dostawcy VPN i **którekolwiek** z poniższych stwierdzeń jest prawdziwe, prawie na pewno należy łączyć się z siecią Tor za pośrednictwem VPN:

- Już korzystasz z [zaufanego dostawcy VPN](../vpn.md)
- Twój model zagrożeń obejmuje przeciwnika, który jest w stanie wydobyć informacje od Twojego ISP
- Twój model zagrożeń obejmuje samego dostawcę usług internetowych jako przeciwnika
- Twój model zagrożeń obejmuje administratorów lokalnej sieci działających przed Twoim ISP jako przeciwników

Ponieważ już z różnych powodów [ogólnie zalecamy](../basics/vpn-overview.md), by zdecydowana większość osób korzystała z zaufanego dostawcy VPN, następujące zalecenie dotyczące łączenia się z siecią Tor za pośrednictwem VPN prawdopodobnie dotyczy także Ciebie. <mark>Nie ma potrzeby wyłączać VPN-a przed połączeniem się z siecią Tor</mark>, jak sugerują to niektóre źródła internetowe.

Łączenie się bezpośrednio z siecią Tor sprawi, że Twoje połączenie będzie się wyróżniać dla administratorów lokalnej sieci lub ISP. W przeszłości administratorzy sieci potrafili [wykryć i skorelować](https://edition.cnn.com/2013/12/17/justice/massachusetts-harvard-hoax) taki ruch, by zidentyfikować i zdeanonimizować konkretne osoby korzystające z Tora. Z drugiej jednak strony połączenie przez VPN zwykle wzbudza mniejsze podejrzenia, ponieważ komercyjne usługi VPN są wykorzystywane przez zwykłych konsumentów do różnych codziennych zadań, np. omijania ograniczeń geograficznych, nawet w krajach o silnych ograniczeniach Internetu.

Dlatego warto zadbać o ukrycie swojego adresu IP **przed** połączeniem z siecią Tor. Można to zrobić, łącząc się najpierw z VPN (poprzez klienta zainstalowanego na komputerze), a następnie uzyskując dostęp do sieci [Tor](../tor.md) normalnie (np. przez przeglądarkę Tor Browser). Powstaje wtedy następujący łańcuch połączeń:

- [x] Ty → VPN → Tor → Internet

Z perspektywy ISP wygląda to tak, jak zwykłe korzystanie z VPN (co daje pewną zasłonę). Z perspektywy dostawcy VPN widać połączenie z siecią Tor, ale nic o odwiedzanych przez Ciebie stronach. Z perspektywy Tora połączenie wygląda normalnie, a w mało prawdopodobnym przypadku kompromitacji sieci Tor ujawniony zostałby jedynie Twój adres IP VPN-a — konieczne byłoby *dodatkowe* naruszenie samej sieci VPN, by Cię zdeanonimizować.

**Nie** jest to zalecenie dotyczące obchodzenia cenzury, ponieważ jeśli ISP całkowicie blokuje Tor, prawdopodobnie zablokuje też VPN. Celem tego zalecenia jest raczej lepsze wtopienie się Twojego ruchu w zwykły ruch użytkowników VPN oraz zapewnienie pewnego poziomu możliwej do wyparcia wiarygodności, ukrywając fakt łączenia się z Tor przed dostawcą usług internetowych.

---

**Zdecydowanie odradzamy** łączenie Tora z VPN w jakikolwiek inny sposób. Nie konfiguruj połączenia w sposób przypominający którekolwiek z poniższych:

- Ty → Tor → VPN → Internet
- Ty → VPN → Tor → VPN → Internet
- Jakakolwiek inna konfiguracja

Niektórzy dostawcy VPN i inne publikacje okazjonalnie zalecają takie **złe** konfiguracje, by obejść blokady Tor (np. gdy w niektórych miejscach węzły wyjściowe są blokowane przez strony). [Zazwyczaj](https://support.torproject.org/#about_change-paths) Tor często zmienia ścieżkę obwodu w sieci. Gdy wybierze się stałe *miejsce docelowe* VPN (czyli łączenie z serwerem VPN *po* Tor), traci się tę przewagę i znacznie szkodzi się swojej anonimowości.

Ustawienie takich złych konfiguracji rzadko zdarza się przypadkowo, bo zwykle wymaga skonfigurowania niestandardowych ustawień proxy w przeglądarce Tor Browser lub niestandardowych ustawień w kliencie VPN, które kierują ruch VPN poprzez przeglądarkę Tor Browser. Unikając tych niestandardowych konfiguracji, najprawdopodobniej wszystko będzie w porządku.

---

<div class="admonition info" markdown>
<p class="admonition-title">Identyfikacja wzorców ruchu VPN/SSH</p>

Tor Project [zauważa](https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN#vpnssh-fingerprinting), że *teoretycznie* użycie VPN do ukrycia aktywności Tor przed dostawcą usług internetowych może nie być niezawodne. Wykryto przypadki, gdzie VPN-y były podatne na identyfikację wzorców ruchu na stronach internetowych — przeciwnik mógł odgadnąć, jaka strona jest odwiedzana, ponieważ poszczególne witryny mają charakterystyczne wzorce ruchu.

Dlatego nie jest nierozsądne przypuszczać, że zaszyfrowany ruch Tor ukryty przez VPN mógłby być wykryty podobnymi metodami. Nie ma na ten temat badań naukowych, ale wciąż uważamy, że korzyści płynące z korzystania z VPN znacznie przewyższają te ryzyka, ale jest to coś, co warto mieć na uwadze.

Jeżeli mimo uważasz, że transporty wtykowe (mostki) zapewniają dodatkową ochronę przed identyfikacją wzorców ruchu, której VPN nie zapewnia, zawsze masz możliwość korzystania z mostku *oraz* VPN jednocześnie.

</div>

Decyzja, czy najpierw użyć VPN przed połączeniem się z siecią Tor, wymaga zdrowego rozsądku i znajomości polityk własnego rządu oraz dostawcy usług internetowych dotyczących tego, z czym się łączysz. Powtórzmy: w większości przypadków lepiej będzie sprawiać wrażenie osoby łączącej się z komercyjną siecią VPN niż bezpośrednio z siecią Tor. Jeśli dostawcy VPN są cenzurowani w Twojej okolicy, możesz rozważyć użycie transportów wtykowych (np. mostków Snowflake lub meek) jako alternatywy, choć korzystanie z takich mostków może wzbudzać więcej podejrzeń niż standardowe tunele WireGuard/OpenVPN.

## Czym Tor nie jest

Sieć Tor nie jest doskonałym narzędziem do ochrony prywatności we wszystkich sytuacjach i ma szereg wad, które warto dokładnie rozważyć. Nie powinno to jednak zniechęcać cię do korzystania z Tora, jeśli jest on odpowiedni dla Twoich potrzeb — są to po prostu kwestie, które należy brać pod uwagę przy wyborze najbardziej dopasowanego rozwiązania dla Ciebie.

### Tor nie jest darmową siecią VPN

Pojawienie się aplikacji mobilnej *Orbot* spowodowało, że wiele osób zaczęło określać Tor mianem „darmowego VPN-a” dla całego ruchu urządzenia. Jednak traktowanie Tora w ten sposób niesie ze sobą pewne niebezpieczeństwa w porównaniu do typowej sieci VPN.

W przeciwieństwie do węzłów wyjściowych Tora, dostawcy VPN zwykle nie są *aktywnie* [złośliwi](#caveats). Ponieważ węzły wyjściowe Tora może uruchomić praktycznie każdy, stanowią one miejsca, gdzie często prowadzona jest rejestracja i modyfikacja ruchu. W 2020 roku udokumentowano wiele węzłów wyjściowych, które obniżały jakość ruchu HTTPS do HTTP, aby [przejmować transakcje kryptowalutowe](https://therecord.media/thousands-of-tor-exit-nodes-attacked-cryptocurrency-users-over-the-past-year). Zaobserwowano także inne ataki ze strony węzłów wyjściowych, np. zastępowanie pobieranych przez niezaszyfrowane kanały plików złośliwym oprogramowaniem. HTTPS w pewnym stopniu łagodzi te zagrożenia.

Jak już wspomnieliśmy, Tor jest również łatwy do zidentyfikowania w sieci. W przeciwieństwie do komercyjnego dostawcy VPN, korzystanie z Tora może wyróżniać Cię jako osobę prawdopodobnie próbującą unikać nadzoru władz. W idealnym świecie administratorzy sieci i organy władzy traktowaliby Tor jako narzędzie o wielu zastosowaniach (podobnie jak VPN), ale w praktyce postrzeganie Tora jest wciąż znacznie mniej wiarygodne niż postrzeganie komercyjnych sieci VPN. Dlatego korzystanie z prawdziwej sieci VPN daje większą możliwość wiarygodnego zaprzeczenia, np. „Używałem VPN-a tylko do oglądania Netflixa” itp.

### Korzystanie z sieci Tor nie jest niewykrywalne

**Nawet jeśli korzystasz z mostków i transportów wtykowych,** Tor Project nie udostępnia narzędzi, które ukrywałyby przed Twoim ISP fakt używania Tora. Nawet stosowanie zaciemnionych „transportów wtykowych” lub niepublicznych mostków nie ukrywa, że korzysta się z prywatnego kanału komunikacji. Najpopularniejsze transporty wtykowe, takie jak obfs4 (który zaciemnia ruch, by „nie przypominał niczego”) oraz meek (który wykorzystuje maskowanie domeny do maskowania ruchu), mogą być [wykrywane](https://hackerfactor.com/blog/index.php?/archives/889-Tor-0day-Burning-Bridges.html) przy użyciu dość standardowych technik analizy ruchu. Snowflake ma podobne problemy i może być [łatwo wykryty](https://hackerfactor.com/blog/index.php?/archives/944-Tor-0day-Snowflake.html) jeszcze *przed* nawiązaniem połączenia z siecią Tor.

Istnieją również inne niż te trzy transporty wtykowe, ale zazwyczaj opierają się one na zasadzie bezpieczeństwa przez zaciemnienie (*security through obscurity*). Nie są one niemożliwe do wykrycia — po prostu korzysta z nich tak niewiele osób, że nie opłaca się budować dla nich detektorów. Nie powinno się na nich polegać, jeśli konkretnie jesteś osobą monitorowaną.

Ważne jest rozróżnienie między omijaniem cenzury a unikaniem wykrycia. To pierwsze jest zwykle łatwiejsze ze względu na rzeczywiste ograniczenia, jakie mają cenzorzy sieci przy masowym działaniu, ale te techniki nie ukrywają faktu, że to *konkretnie* Ty używasz Tora przed zainteresowaną stroną monitorującą Twoją sieć.

### Tor Browser nie jest naj*bezpieczniejszą* przeglądarką

Anonimowość często stoi w sprzeczności z bezpieczeństwem: anonimowość sieci Tor wymaga, by wszyscy użytkownicy byli identyczni, co tworzy monokulturę (np. te same błędy występują u wszystkich użytkowników przeglądarki Tor Browser). Z punktu widzenia cyberbezpieczeństwa monokultury zwykle uznawane są za złe: bezpieczeństwo przez różnorodność (którego Tor nie zapewnia) naturalnie dzieli środowisko i ogranicza zasięg podatności, co z reguły jest pożądane, choć mniej korzystne dla anonimowości.

Ponadto przeglądarka Tor Browser bazuje na wydaniach Firefoksa o wydłużonym wsparciu (Extended Support Release – ESR), które otrzymują poprawki tylko dla podatności sklasyfikowanych jako *krytyczne* i *wysokie* (nie dla *średnich* i *niskich*). Oznacza to, że atakujący mogą (na przykład):

1. Szukać nowych podatności o statusie krytycznym lub wysokim w wersjach nightly lub beta Firefoksa, a następnie sprawdzać, czy można je wykorzystać w przeglądarce Tor Browser (okres, w którym luka pozostaje niezałatana, może trwać tygodniami).
2. Łączyć ze sobą *wiele* podatności o poziomie średnim/niskim, aż uzyskają pożądany poziom dostępu (okres ten może trwać miesiące lub dłużej).

Osoby narażone na ryzyko wynikające z luk przeglądarki powinny rozważyć dodatkowe środki ochronne przeciwko exploitom przeglądarki Tor Browser, na przykład korzystanie z Whonix w [Qubes](../os/qubes-overview.md) w celu odizolowania sesji przeglądania przez Tor w bezpiecznej maszynie wirtualnej i ochrony przed wyciekami.

## Budowanie ścieżki do usług w clearnecie

„Usługi w clearnecie” to strony internetowe, do których można uzyskać dostęp za pomocą dowolnej przeglądarki, np. [privacyguides.org](https://www.privacyguides.org). Tor umożliwia anonimowe łączenie się z takimi stronami, kierując ruch przez sieć składającą się z tysięcy serwerów prowadzonych przez wolontariuszy, zwanych węzłami (lub przekaźnikami).

Za każdym razem, gdy [łączysz się z siecią Tor](../tor.md), wybierze ona trzy węzły, aby zbudować ścieżkę do Internetu — ścieżka ta nazywana jest „obwodem”.

<figure markdown>
  ![Ścieżka Tora pokazująca, jak urządzenie łączy się z węzłem wejściowym, węzłem środkowym i węzłem wyjściowym przed dotarciem do strony docelowej](../assets/img/how-tor-works/tor-path.svg#only-light)
  ![Ścieżka Tora pokazująca, jak urządzenie łączy się z węzłem wejściowym, węzłem środkowym i węzłem wyjściowym przed dotarciem do strony docelowej](../assets/img/how-tor-works/tor-path-dark.svg#only-dark)
  <figcaption>Ścieżka obwodu Tor</figcaption>
</figure>

Każdy z tych węzłów pełni inną funkcję:

### Węzeł wejściowy

Węzeł wejściowy, często nazywany strażnikiem, to pierwszy węzeł, z którym łączy się klient Tor. Węzeł wejściowy jest w stanie zobaczyć Twój adres IP, jednak nie widzi, z jaką stroną się łączysz.

W przeciwieństwie do pozostałych węzłów, klient Tor losowo wybiera węzeł wejściowy i utrzymuje go przez okres dwóch–trzech miesięcy, aby chronić Cię przed pewnymi atakami[^1].

### Węzeł środkowy

Węzeł środkowy to drugi węzeł w obwodzie. Widzi, z którego węzła przyszedł ruch — czyli węzła wejściowego — i do którego węzła kieruje go dalej. Węzeł środkowy nie widzi Twojego adresu IP ani domeny, z którą się łączysz.

Dla każdego nowego obwodu węzeł środkowy jest wybierany losowo spośród wszystkich dostępnych węzłów Tor.

### Węzeł wyjściowy

Węzeł wyjściowy to punkt, w którym ruch opuszcza sieć Tor i jest przekazywany do żądanego miejsca docelowego. Węzeł wyjściowy nie widzi Twojego adresu IP, ale wie, z jaką stroną się łączysz.

Węzeł wyjściowy jest wybierany losowo spośród wszystkich dostępnych węzłów Tor uruchomionych z flagą przekaźnika wyjściowego[^2].

## Budowanie ścieżki do usług .onion

„Usługi .onion” (nazywane również jako „ukryte usługi”) to strony dostępne wyłącznie z poziomu przeglądarki Tor Browser. Strony te mają długą, losowo wygenerowaną nazwę domeny kończącą się na `.onion`.

Łączenie się z usługą .onion w sieci Tor działa bardzo podobnie jak łączenie z usługą w clearnecie, ale ruch kierowany jest przez łącznie **sześć** węzłów, zanim dotrze do serwera docelowego. Podobnie jak wcześniej, tylko trzy z tych węzłów odpowiadają za *Twoją* anonimowość, a pozostałe trzy chronią anonimowość *usługi .onion*, ukrywając prawdziwy adres IP i lokalizację strony internetowej w ten sam sposób, w jaki przeglądarka Tor Browser ukrywa Twój adres i lokalizację.

<figure style="width:100%" markdown>
  ![Ścieżka Tora pokazująca, jak ruch jest kierowany przez trzy węzły po Twojej stronie oraz trzy dodatkowe węzły ukrywające tożsamość strony internetowej](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![Ścieżka Tora pokazująca, jak ruch jest kierowany przez trzy węzły po Twojej stronie oraz trzy dodatkowe węzły ukrywające tożsamość strony internetowej](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Ścieżka obwodu Tor z usługami .onion. Węzły po stronie <span class="pg-blue">niebieskiej</span> należą do Twojej przeglądarki, natomiast węzły po stronie <span class="pg-red">czerwonej</span> należą do serwera, więc ich tożsamość jest przed Tobą ukryta.</figcaption>
</figure>

## Szyfrowanie

Tor szyfruje każdy pakiet (blok przesyłanych danych) trzykrotnie za pomocą kluczy węzła wyjściowego, środkowego i wejściowego, w tej właśnie kolejności.

Gdy Tor zbuduje obwód, transmisja danych odbywa się w następujący sposób:

1. Po pierwsze: gdy pakiet dociera do węzła wejściowego, usuwana jest pierwsza warstwa szyfrowania. W odszyfrowanym w ten sposób pakiecie znajduje się kolejny zaszyfrowany pakiet z adresem węzła środkowego. Węzeł wejściowy przekazuje potem pakiet do węzła środkowego.

2. Po drugie: gdy węzeł środkowy otrzyma pakiet od węzła wejściowego, także usuwa jedną warstwę szyfrowania za pomocą swojego klucza i znajduje zaszyfrowany pakiet z adresem węzła wyjściowego. Węzeł środkowy przekazuje następnie pakiet do węzła wyjściowego.

3. Na koniec: gdy węzeł wyjściowy otrzyma swój pakiet, usuwa ostatnią warstwę szyfrowania za pomocą swojego klucza. Węzeł wyjściowy widzi adres docelowy i przesyła pakiet dalej do tego adresu.

Poniżej znajduje się alternatywny diagram przedstawiający ten proces. Każdy węzeł usuwa swoją warstwę szyfrowania, a kiedy serwer docelowy zwraca dane, ten sam proces zachodzi w odwrotnym porządku. Na przykład węzeł wyjściowy nie zna Twojej tożsamości, ale wie, z którego węzła pochodzi pakiet — dodaje więc własną warstwę szyfrowania i odsyła dane z powrotem.

<figure markdown>
  ![Szyfrowanie w Torze](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![Szyfrowanie w Torze](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>Wysyłanie i odbieranie danych przez sieć Tor</figcaption>
</figure>

Tor umożliwia połączenie się z serwerem bez tego, by którakolwiek pojedyncza strona znała całą ścieżkę. Węzeł wejściowy zna Twój adres IP, ale nie wie, dokąd zmierzasz; węzeł środkowy nie zna ani Twojego adresu IP, ani docelowej domeny; węzeł wyjściowy wie, dokąd kierowany jest ruch, lecz nie wie, kim jesteś. Ponieważ to węzeł wyjściowy nawiązuje ostateczne połączenie z serwerem, serwer docelowy nigdy nie pozna Twojego adresu IP.

## Zastrzeżenia

Mimo że Tor zapewnia silne gwarancje prywatności, należy pamiętać, że nie jest ona narzędziem doskonałym:

- Tor nigdy nie ochroni przed ujawnieniem się na skutek błędu użytkownika, np. gdy udostępnione zostanie zbyt wiele informacji na temat prawdziwej tożsamości.
- Węzły wyjściowe Tor mogą **modyfikować** niezaszyfrowany ruch przechodzący przez nie. Oznacza to, że ruch niezabezpieczony, np. zwykły HTTP, może zostać zmieniony przez złośliwy węzeł wyjściowy. **Nigdy** nie pobieraj plików z niezabezpieczonego adresu `http://` przez Tor i upewnij się, że przeglądarka jest ustawiona tak, by zawsze podwyższać połączenia HTTP do HTTPS.
- Węzły wyjściowe mogą również monitorować ruch przechodzący przez nie. Niezaszyfrowany ruch zawierający dane umożliwiające identyfikację osoby może zdeanonimizować użytkownika względem tego węzła wyjściowego. Raz jeszcze — zalecamy korzystanie wyłącznie z HTTPS podczas korzystania z sieci Tor.
- Potężni przeciwnicy zdolni do pasywnego monitorowania *całego* ruchu sieciowego na świecie (tzw. *Global Passive Adversaries*) **nie** są tym, przed czym Tor chroni (i użycie Tora [w połączeniu z VPN](#safely-connecting-to-tor) tego nie zmienia).
- Dobrze finansowani przeciwnicy, którzy potrafią pasywnie obserwować *większość* światowego ruchu sieciowego, wciąż mają *szansę* na zdeanonimizowanie użytkowników Tora przy użyciu zaawansowanej analizy ruchu.

Jeżeli zamierzasz używać sieci Tor do przeglądania sieci, zalecamy wyłącznie **oficjalną** przeglądarkę Tor Browser — została zaprojektowana tak, by utrudniać identyfikację przez unikalny odcisk przeglądarki (*fingerprinting*).

- [Tor Browser :material-arrow-right-drop-circle:](../tor.md#tor-browser)

### Ochrona zapewniana przez mostki

Mostki Tor są często promowane jako alternatywa do ukrywania korzystania z Tora przed ISP zamiast sieci VPN (co sugerujemy, o ile to możliwe). Warto jednak pamiętać, że choć mostki mogą być skuteczne przy obchodzeniu cenzury, korzyść ta jest często *przejściowa*. Nie chronią one wystarczająco przed tym, że ISP może wykryć, że w *przeszłości* połączono się z siecią Tor, analizując historyczne dzienniki ruchu.

Aby to zilustrować, rozważmy następujący przykład: łączysz się z siecią Tor przez mostek, a twój ISP tego nie wykrywa, bo nie prowadzi zaawansowanej analizy ruchu, więc wszystko działa zgodnie z zamierzeniami. Po czterech miesiącach adres IP Twojego mostka zostaje ujawniony. Jest to bardzo częsta sytuacja — mostki są odkrywane i blokowane stosunkowo często, ale nie od razu.

Jeśli ISP chce zidentyfikować użytkowników Tora sprzed czterech miesięcy, ich ograniczone dzienniki metadanych mogą pokazać, że jesteś osobą, która łączyła się z adresem IP, który później okazał się mostkiem Tor. Praktycznie nie ma żadnego innego wytłumaczenia takiego połączenia, więc ISP może z wysokim prawdopodobieństwem stwierdzić, że w tamtym czasie korzystano z sieci Tor.

Dla kontrastu, spójrz na zalecany przez nas scenariusz, gdzie łączysz się z Torem za pośrednictwem VPN. Załóżmy, że po czterech miesiącach ISP ponownie chce zidentyfikować wszystkich, którzy korzystali z sieci Tor cztery miesiące temu. Analizując swoje dzienniki, ISP prawdopodobnie zobaczy jedynie połączenie z adresem IP dostawcy VPN. Wynika to z faktu, że większość dostawców usług internetowych przechowuje jedynie metadane, a nie pełną zawartość żądanego ruchu. Przechowywanie całości danych o ruchu wymagałoby ogromnej ilości pamięci masowej, której prawie żaden przeciwnik nie posiada.

Ponieważ ISP niemal na pewno nie śledzi wszystkich danych na poziomie pakietów i nie przechowuje ich w nieskończoność, to *po czasie* rzadko może on ustalić, dokąd dokładnie prowadziło połączenie „po” VPN, używając zaawansowanych technik, jak głęboka inspekcja pakietów, co daje pewien stopień możliwej do podważenia wiarygodności.

Z tego względu mostki sprawdzają się najlepiej jako *doraźny sposób* na obejście cenzury, ale nie zastępują one **wszystkich** zalet wynikających z użycia VPN razem z Torem. Raz jeszcze — nie chodzi tu o *odradzanie* użycia mostków Tor — warto jedynie być świadomym ich ograniczeń. W niektórych sytuacjach mostki mogą być *jedyną* opcją (np. gdy wszyscy dostawcy VPN są zablokowani), więc można nadal ich używać, mając na uwadze wymienione wcześniej ograniczenia.

Jeśli uważasz, że mostek może lepiej chronić przed identyfikacją lub inną zaawansowaną analizą ruchu niż sam szyfrowany tunel VPN, zawsze możesz użyć mostka w połączeniu z VPN. W ten sposób nadal korzystasz z technik zaciemniania transportu wtykowego, nawet jeśli przeciwnik uzyska pewien wgląd w tunel VPN. Jeżeli zdecydujesz się pójść tą drogą, zalecamy łączenie się z mostem obfs4 za pośrednictwem VPN dla optymalnej ochrony przed identyfikacją, zamiast używania meek lub Snowflake.

[Możliwym](https://discuss.privacyguides.net/t/clarify-tors-weaknesses-with-respect-to-observability/3676/16) rozwiązaniem, które może złagodzić część tych obaw, jest transport wtykowy [WebTunnel](https://forum.torproject.org/t/tor-relays-announcement-webtunnel-a-new-pluggable-transport-for-bridges-now-available-for-deployment/8180) będący obecnie w fazie testów. Będziemy śledzić rozwój tej technologii w miarę jej dojrzewania.

## Dodatkowe zasoby

- [Podręcznik użytkownika przeglądarki Tor Browser](https://tb-manual.torproject.org)
- [How Tor Works - Computerphile](https://youtube.com/watch?v=QRYzre4bf7I) [Jak działa Tor] <small>(YouTube, ang.)</small>
- [Tor Onion Services - Computerphile](https://youtube.com/watch?v=lVcbq_a5N9I) [Usługi .onion sieci Tor] <small>(YouTube, ang.)</small>

[^1]: Pierwszy przekaźnik w obwodzie nazywany jest „strażnikiem”. To szybki i stabilny przekaźnik, który pozostaje pierwszym elementem obwodu przez 2–3 miesiące, by chronić przed znanym atakiem łamiącym anonimowość. Reszta obwodu zmienia się przy każdej nowo odwiedzanej stronie, a wszystkie te przekaźniki razem zapewniają pełną ochronę prywatności Tora. Więcej informacji o działaniu przekaźników wejściowych można znaleźć w tym [wpisie na blogu](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) oraz w tym [artykule](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf). ([https://support.torproject.org/tbb/tbb-2](https://support.torproject.org/tbb/tbb-2))

[^2]: Flaga przekaźnika: specjalne przypisanie (lub odrzucenie przypisania) przekaźników do pozycji w obwodzie (np. „Guard”, „Exit”, „BadExit”), właściwości obwodu (np. „Fast”, „Stable”) lub ról (np. „Authority”, „HSDir”), nadawane przez władze katalogowe i określone w specyfikacji protokołu katalogu. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html#relay-flag))
