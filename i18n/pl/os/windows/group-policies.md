---
title: Ustawienia zasad grupy
description: Krótki przewodnik po konfigurowaniu zasad grupy, aby Windows nieco bardziej szanował Twoją prywatność.
---

Poza modyfikowaniem samego rejestru **Edytor lokalnych zasad grupy** to najsilniejsze narzędzie do zmiany wielu aspektów systemu bez instalowania programów firm trzecich. Zmiana tych ustawień wymaga [wersji Pro](index.md#windows-editions) lub lepszej.

Ustawienia te powinny być zastosowane na świeżej instalacji systemu Windows. Zastosowanie ich na już istniejącej instalacji powinno zadziałać, ale może wprowadzić nieprzewidywalne zachowanie — robisz to na własne ryzyko.

Wszystkie te ustawienia mają dołączone objaśnienia w edytorze zasad grupy, które wyjaśniają dokładnie, co robią, zwykle bardzo szczegółowo. Zwróć uwagę na te opisy podczas wprowadzania zmian, aby wiedzieć dokładnie, co tutaj zalecamy. Wyjaśniliśmy też niektóre z naszych wyborów tam, gdzie opis dołączony do systemu Windows był niewystarczający.

## Szablony administracyjne

Ustawienia te znajdziesz, otwierając `gpedit.msc` i przechodząc w lewym pasku bocznym do: **Zasady Komputer lokalny** > **Konfiguracja komputera** > **Szablony administracyjne**. Nagłówki na tej stronie odpowiadają folderom/podfolderom w Szablonach administracyjnych, a wypunktowania odpowiadają poszczególnym zasadom.

Aby zmienić dowolną zasadę grupy, kliknij ją dwukrotnie i wybierz w górnej cześci okna, które się pojawi — Włączone lub Wyłączone — w zależności od zalecanych ustawień poniżej. Niektóre zasady grupy mają dodatkowe opcje konfiguracyjne; jeśli tak jest, odpowiednie ustawienia są również zaznaczone poniżej.

### System

#### Device Guard

- Włącz zabezpieczenia oparte na wirtualizacji: **Włączone**
  - Wybierz poziom zabezpieczeń platformy: **Bezpieczny rozruch i ochrona DMA**
  - Konfiguracja funkcji Bezpieczne uruchomienie: **Włączone**

#### Zarządzanie komunikacją internetową

- Wyłącz Program poprawy jakości obsługi klienta systemu Windows: **Włączone**
- Wyłącz funkcję Raportowanie błędów systemu Windows: **Włączone**
- Wyłącz Program poprawy jakości obsługi klienta w programie Windows Messenger: **Włączone**

Zauważ, że wyłączenie Programu poprawy jakości obsługi klienta systemu Windows powoduje też wyłączenie niektórych innych funkcji śledzących, którymi można zarządzać osobno za pomocą zasad grupy. Nie wymieniamy ich wszystkich tutaj ani nie wyłączamy ich oddzielnie, ponieważ to ustawienie obejmuje te przypadki.

#### Zasady systemu operacyjnego

- Zezwalaj na historię schowka: **Wyłączone**
- Zezwalaj na synchronizację schowka między urządzeniami: **Wyłączone**
- Włącza kanał aktywności: **Wyłączone**
- Zezwalaj na publikowanie aktywności użytkownika: **Wyłączone**
- Zezwalaj na przekazywanie działań użytkownika: **Wyłączone**

#### Profile użytkowników

- Wyłącz identyfikator treści reklamowych: **Włączone**

### Składniki systemu Windows

#### Zasady funkcji Autoodtwarzanie

Autouruchamianie i Autoodtwarzanie to funkcje pozwalające systemowi Windows uruchamiać skrypt lub wykonywać inne zadanie po podłączeniu urządzenia, czasem omijając mechanizmy bezpieczeństwa wymagające zgody użytkownika. Może to pozwolić niezaufanym urządzeniom na uruchomienie złośliwego kodu bez Twojej wiedzy. Z punktu widzenia bezpieczeństwa najlepszą praktyką jest wyłączenie tych funkcji i ręczne otwieranie plików na dyskach zewnętrznych.

- Wyłącz funkcję Autoodtwarzanie: **Włączone**
- Wyłącz funkcję Autoodtwarzanie dla urządzeń niezawierających woluminów: **Włączone**
- Ustaw domyślne zachowanie autouruchamiania: **Włączone**
  - Domyślne zachowanie autouruchamiania: **Nie wykonuj żadnych poleceń autouruchamiania**

#### Szyfrowanie dysków funkcją BitLocker

Po zmianie tych ustawień może być konieczne ponowne zaszyfrowanie dysku systemowego.

- Wybierz metodę szyfrowania dysku i siłę szyfrowania (Windows Vista, Windows Server 2008, Windows 7, Windows Server 2008 R2): **Włączone**
  - Wybierz metodę szyfrowania: **AES 256 bitów**

Ustawienie siły szyfrowania w zasadzie dla systemu Windows 7 nadal wymusza tę siłę w nowszych wersjach systemu Windows.

##### Dyski z systemem operacyjnym

- Wymagaj dodatkowego uwierzytelniania przy uruchamianiu: **Włączone**
- Zezwalaj na używanie rozszerzonych numerów PIN przy uruchamianiu: **Włączone**

Mimo nazw tych zasad domyślnie niczego nie _wymagają_, ale odblokowują _możliwość_ skonfigurowania bardziej złożonego mechanizmu (np. wymaganie PIN-u przy uruchamianiu obok TPM) w kreatorze konfiguracji BitLockera.

#### Zawartość chmury

- Wyłączenie zawartości zoptymalizowanej pod kątem chmury: **Włączone**
- Wyłączenie zawartości stanu konta klienta w chmurze: **Włączone**
- Nie pokazuj porad dotyczących systemu Windows: **Włączone**
- Wyłącz funkcje użytkownika firmy Microsoft: **Włączone**

#### Interfejs użytkownika do obsługi poświadczeń

- Wymagaj ścieżki zaufanej do wprowadzania poświadczeń: **Włączone**
- Wyłącz możliwość używania pytań zabezpieczeń dla kont lokalnych: **Włączone**

#### Zbieranie danych i kompilacje w wersji Preview

- Zezwalaj na dane diagnostyczne: **Włączone**
  - Opcje: **Wysyłaj wymagane dane diagnostyczne** (w wersji Pro); lub
  - Options: **Diagnostic data off** (Enterprise or Education Edition)
- Ogranicz zbieranie dzienników diagnostycznych: **Włączone**
- Ogranicz zbieranie zrzutów: **Włączone**
- Ogranicz opcjonalne dane diagnostyczne dla usługi Desktop Analytics: **Włączone**
  - Opcje: **Wyłącz kolekcję usługi Desktop Analytics**
- Nie pokazuj powiadomień o opiniach: **Włączone**

#### Eksplorator plików

- Pokaż pliki na podstawie Twojego konta i aktywności dostawcy w chmurze: **Włączone**

#### MDM

- Wyłącz rejestrację w usłudze MDM: **Włączone**

#### OneDrive

- Domyślnie zapisuj dokumenty w usłudze OneDrive: **Wyłączone**
- Uniemożliwiaj aplikacji OneDrive generowanie ruchu sieciowego, dopóki użytkownik nie zaloguje się do usługi OneDrive: **Włączone**
- Nie zezwalaj na używanie usługi OneDrive na potrzeby przechowywania plików: **Włączone**

To ostatnie ustawienie wyłącza usługę OneDrive w systemie; jeśli korzystasz z tej usługi, ustaw je na **Wyłączone**.

#### Push To Install

- Wyłącz usługę Push To Install: **Włączone**

#### Wyszukaj

- Zezwalaj na Cortanę: **Wyłączone**
- Nie wyszukuj w sieci Web ani nie wyświetlaj wyników z sieci Web w funkcji wyszukiwania: **Włączone**
- Określ, jakie informacje mają być udostępniane w funkcji wyszukiwania: **Włączone**
  - Typ informacji: **Informacje anonimowe**

#### Synchronizuj ustawienia

- Nie synchronizuj: **Włączone**

#### Wprowadzanie tekstu

- Ulepsz rozpoznawanie pisma odręcznego i wpisywania: **Wyłączone**

#### Raportowanie błędów systemu Windows

- Nie wysyłaj dodatkowych danych: **Włączone**
- Zgoda > Konfiguruj domyślne ustawienia zgody: **Włączone**
  - Poziom zgody: **Zawsze pytaj przed wysłaniem danych**
