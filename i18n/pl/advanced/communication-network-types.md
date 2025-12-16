---
title: "Rodzaje sieci komunikacyjnych"
icon: 'material/transit-connection-variant'
description: Przegląd kilku architektur sieciowych powszechnie używanych przez komunikatory internetowe.
---

Istnieje kilka architektur sieciowych powszechnie wykorzystywanych do przekazywania wiadomości między ludźmi. Sieci te mogą oferować różne gwarancje prywatności, dlatego warto wziąć pod uwagę swój [model zagrożeń](../basics/threat-modeling.md) przy wyborze aplikacji.

[Zalecane komunikatory](../real-time-communication.md ""){.md-button} [:material-movie-open-play-outline: Wideo: Czas przestać korzystać z SMS-ów](https://www.privacyguides.org/videos/2025/01/24/its-time-to-stop-using-sms-heres-why ""){.md-button}

## Sieci scentralizowane

![Schemat sieci scentralizowanych](../assets/img/layout/network-centralized.svg){ align=left }

Scentralizowane komunikatory to takie, w których wszyscy uczestnicy znajdują się na tym samym serwerze lub w sieci serwerów kontrolowanej przez jedną tę samą organizację.

Niektóre samodzielnie hostowane komunikatory umożliwiają skonfigurowanie własnego serwera. Samodzielne hostowanie może zapewnić dodatkowe gwarancje prywatności, takie jak brak dzienników użytkowania lub ograniczony dostęp do metadanych (danych o tym, kto z kim rozmawia). Scentralizowane komunikatory hostowane samodzielnie są odizolowane i wszyscy muszą być na tym samym serwerze, aby móc się komunikować.

**Zalety:**

- Nowe funkcje i zmiany mogą być wdrażane szybciej.
- Łatwiej jest rozpocząć korzystanie z nich i znaleźć kontakty.
- Bardziej dojrzały i stabilny ekosystem funkcji, ponieważ łatwiej je zaimplementować w oprogramowaniu scentralizowanym.
- Problemy z prywatnością mogą być mniejsze, jeśli ufa się serwerowi, który jest hostowany samodzielnie.

**Wady:**

- Mogą występować [ograniczenia kontroli lub dostępu](https://drewdevault.com/2018/08/08/Signal.html). Należą do nich na przykład:
- [Zabronienie podłączania klientów firm trzecich](https://github.com/LibreSignal/LibreSignal/issues/37#issuecomment-217211165) do sieci scentralizowanej, co mogłoby umożliwić większą personalizację lub lepsze wrażenia. Często określane w Warunkach korzystania z usługi.
- Słaba dokumentacja lub jej brak dla zewnętrznych deweloperów.
- [Własność](https://web.archive.org/web/20210729191953/https://blog.privacytools.io/delisting-wire), polityka prywatności i sposób działania usługi mogą łatwo ulec zmianie, gdy usługą zarządza jeden podmiot, co może później podważyć bezpieczeństwo usługi.
- Samodzielne hostowanie wymaga wysiłku i wiedzy na temat konfiguracji usługi.

## Sieci federacyjne

![Schemat sieci federacyjnych](../assets/img/layout/network-decentralized.svg){ align=left }

Komunikatory federacyjne korzystają z wielu niezależnych, zdecentralizowanych serwerów, które potrafią się ze sobą komunikować (przykładem usługi federacyjnej jest poczta e-mail). Federacja pozwala administratorom systemów kontrolować własny serwer, a jednocześnie nadal być częścią większej sieci komunikacyjnej.

Przy samodzielnym hostowaniu członkowie serwera federacyjnego mogą odnajdywać i komunikować się z członkami innych serwerów, choć niektóre serwery mogą pozostać prywatne i nieprzystępujące do federacji (np. serwer zespołu służbowego).

**Zalety:**

- Pozwala na większą kontrolę nad własnymi danymi przy korzystaniu z własnego serwera.
- Umożliwia wybór, komu powierzyć swoje dane, poprzez wybór spośród kilku „publicznych” serwerów.
- Często umożliwia korzystanie z klientów zewnętrznych, które mogą zapewnić bardziej natywne, spersonalizowane lub dostępne wrażenia.
- Oprogramowanie serwera można zweryfikować pod kątem zgodności z publicznym kodem źródłowym, o ile ma się dostęp do serwera lub ufa się osobie, która go posiada (np. członkowi rodziny).

**Wady:**

- Wprowadzanie nowych funkcji jest bardziej skomplikowane, ponieważ muszą być one ustandaryzowane i przetestowane, aby działały na wszystkich serwerach w sieci.
- Z powodu powyższego funkcje mogą być ograniczone, niekompletne lub działać w nieoczekiwany sposób w porównaniu z platformami scentralizowanymi, np. w zakresie przekazywania wiadomości, gdy odbiorca jest offline, czy usuwania wiadomości.
- Część metadanych może być dostępna (np. informacje o tym, „kto z kim rozmawia”), choć treść wiadomości pozostaje zaszyfrowana, jeżeli stosowane jest E2EE.
- Serwery federacyjne zazwyczaj wymagają zaufania do administratora serwera. Może to być hobbysta lub ktoś, kto nie jest „specjalistą ds. bezpieczeństwa”, i nie zawsze udostępnia standardowe dokumenty, takie jak polityka prywatności czy warunki korzystania z usługi opisujące sposób wykorzystania danych.
- Administratorzy serwerów czasem blokują inne serwery, które są źródłem niemoderowanych nadużyć lub łamią ogólnie przyjęte zasady. Utrudnia to komunikację z członkami tych serwerów.

## Sieci peer-to-peer (P2P)

![Schemat P2P](../assets/img/layout/network-distributed.svg){ align=left }

Komunikatory P2P łączą się z [rozproszoną siecią](https://en.wikipedia.org/wiki/Distributed_networking) węzłów, aby przekazać wiadomość do odbiorcy bez udziału serwera strony trzeciej.

Klienci (peery) zwykle odnajdują się nazwajem za pomocą [rozproszonych sieci komputerowej](https://en.wikipedia.org/wiki/Distributed_computing). Przykładem takiej sieci są [rozproszone tablice mieszające](https://pl.wikipedia.org/wiki/Rozproszona_tablica_mieszająca) (DHT), wykorzystywane na przykład przez [torrenty](https://pl.wikipedia.org/wiki/BitTorrent) czy [IPFS](https://en.wikipedia.org/wiki/InterPlanetary_File_System). Innym podejściem są sieci oparte na bliskości, gdzie połączenie nawiązywane jest przez Wi-Fi lub Bluetooth (np. Briar lub protokół społecznościowy [Scuttlebutt](https://scuttlebutt.nz)).

Gdy peer znajdzie trasę do kontaktu jedną z tych metod, nawiązuje się bezpośrednie połączenie między nimi. Choć wiadomości są zwykle szyfrowane, obserwator może nadal wywnioskować lokalizację i tożsamość nadawcy oraz odbiorcy.

Sieci P2P nie korzystają z serwerów — peery komunikują się między sobą bezpośrednio i dlatego nie da się ich typowo hostować samodzielnie. Jednak niektóre dodatkowe usługi, takie jak odnajdywanie użytkowników czy pośredniczenie w dostarczaniu wiadomości wysłanych, gdy odbiorca był offline, mogą polegać na serwerach scentralizowanych i wtedy skorzystać na samodzielnym hostowaniu.

**Zalety:**

- Minimalna ilość informacji jest ujawniana podmiotom trzecim.
- Nowoczesne platformy P2P domyślnie stosują E2EE. Brak serwerów, które mogłyby potencjalnie przechwycić i odszyfrować transmisje, w przeciwieństwie do modeli scentralizowanych i federacyjnych.

**Wady:**

- Ograniczony zestaw funkcji:
- Wiadomości można wysyłać tylko wtedy, gdy obie strony są online; klient może jednak przechowywać wiadomości lokalnie, czekając na powrót kontaktu do trybu online.
- Zazwyczaj większe zużycie baterii na urządzeniach mobilnych, ponieważ klient musi pozostać połączony z siecią rozproszoną, aby śledzić dostępność użytkowników.
- Niektóre powszechne funkcje komunikatorów mogą nie być zaimplementowane lub działać niekompletnie, np. usuwanie wiadomości.
- Twój adres IP oraz adresy kontaktów, z którymi się komunikujesz, mogą być ujawnione, jeśli nie używasz oprogramowania w połączeniu z siecią [VPN](../vpn.md) lub [Tor](../tor.md). W wielu krajach stosuje się pewną formę masowej inwigilacji i/lub przechowywania metadanych.

## Anonimowe trasowanie

![Schemat anonimowego trasowania](../assets/img/layout/network-anonymous-routing.svg){ align=left }

Komunikator wykorzystujący [anonimowe trasowanie](https://doi.org/10.1007/978-1-4419-5906-5_628) ukrywa tożsamość nadawcy, odbiorcy lub dowody na to, że się komunikacji. W idealnym przypadku komunikator powinien ukrywać wszystkie trzy elementy.

Istnieje [wiele](https://doi.org/10.1145/3182658) metod implementacji anonimowego trasowania. Jedną z najbardziej znanych jest [trasowanie cebulowe](https://pl.wikipedia.org/wiki/Trasowanie_cebulowe) (np. [Tor](tor-overview.md)), który przesyła zaszyfrowane wiadomości za pośrednictwem wirtualnej [sieci nakładkowej](https://en.wikipedia.org/wiki/Overlay_network), ukrywając lokalizację każdego węzła oraz nadawcę i odbiorcę wiadomości. Nadawca i odbiorca nigdy nie komunikują się bezpośrednio — spotykają się jedynie za pośrednictwem tajnego węzła spotkania, dzięki czemu nie następuje wyciek adresów IP ani lokalizacji fizycznej. Węzły nie mogą odszyfrować treści wiadomości ani poznać miejsca docelowego; tylko odbiorca ma możliwość pełnego odszyfrowania. Każdy węzeł pośredniczący odszyfrowuje jedynie fragment wskazujący, dokąd przesłać nadal zaszyfrowaną wiadomość, aż dotrze ona do odbiorcy, który odszyfrowuje całość — stąd nazwa „warstwy cebulowe”.

Samodzielne hostowanie węzła w sieci anonimowego trasowania nie zapewnia hostowi dodatkowych korzyści w zakresie prywatności, ale przyczynia się natomiast do odporności całej sieci na ataki identyfikacyjne z korzyścią dla wszystkich użytkowników.

**Zalety:**

- Minimalna lub żadna ilość informacji nie jest ujawniana innym podmiotom.
- Wiadomości mogą być przekazywane w sposób zdecentralizowany nawet wtedy, gdy jedna ze stron jest offline.

**Wady:**

- Powolne rozprzestrzenianie się wiadomości.
- Często ograniczone do mniejszej liczby typów multimediów, głównie tekstu, z uwagi na wolniejsze działanie sieci.
- Mniej niezawodne, jeśli węzły są wybierane losowo; niektóre węzły mogą być bardzo odległe względem nadawcy i odbiorcy, co zwiększa opóźnienia lub powoduje nawet niepowodzenie transmisji, gdy któryś z węzłów zniknie z sieci.
- Trudniejsze rozpoczęcie użytkowania, ponieważ wymagane jest utworzenie i bezpieczne wykonanie kopii zapasowej kryptograficznego klucza prywatnego.
- Podobnie jak w przypadku innych zdecentralizowanych platform, dodawanie funkcji jest trudniejsze dla deweloperów niż na platformie scentralizowanej. W rezultacie niektóre funkcje mogą być niedostępne lub niekompletnie zaimplementowane, np. przekazywanie wiadomości offline czy usuwanie wiadomości.
