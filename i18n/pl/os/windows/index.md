---
title: Przegląd systemu Windows
icon: material/microsoft-windows
description: Microsoft Windows to popularny system operacyjny, który w ustawieniach fabrycznych cechuje się bardzo niską prywatnością. Nasz przewodnik opisuje sposoby poprawy prywatności komputera bez konieczności zmiany systemu operacyjnego.
---

**Microsoft Windows** to popularny system operacyjny instalowany domyślnie na wielu komputerach. Poniższe zalecenia mają na celu przedstawić sposoby zwiększenia prywatności i ograniczenia domyślnej telemetrii oraz przechowywanych danych przez wyłączenie niektórych niepotrzebnych funkcji. Z biegiem czasu Microsoft dodaje do systemu funkcje, które często opierają się na usługach chmurowych. Funkcje te zwykle wymagają przesyłania pewnych [opcjonalnych danych](https://privacy.microsoft.com/data-collection-windows) do zdalnych serwerów w celu przetworzenia.

Jednym z najnowszych przykładów była funkcja **Recall**, będąca częścią zestawu funkcji Copilot AI. Recall okresowo wykonuje zrzuty ekranu wszystkiego, co pojawiło się na komputerze, aby móc to później wyświetlić. Takie „pomocne” funkcje generują znaczne ilości metadanych, które można poddać analizie kryminalistycznej. W większości przypadków wystarcza historia przeglądania, więc funkcję można bezpiecznie wyłączyć. Głównym problemem związanym z Recall było to, że dane są przechowywane w lokalnej bazie danych, która jest odszyfrowywana po włączeniu urządzenia — co czyni ją łatwym celem dla hakerów, jeśli urządzenie zostanie zainfekowane złośliwym oprogramowaniem. Recall nie zaciera ani nie usuwa wrażliwych informacji, takich jak skopiowane hasła czy dane finansowe, z bazy danych, ale chroni przed tworzeniem zrzutów ekranu treści objętych prawami autorskimi chronionymi systemami zarządzania prawami cyfrowymi (DRM).

Niestety funkcja ta została dodana bez większego namysłu nad konsekwencjami prywatności wynikającymi z jej domyślnego włączenia (choć obecnie już [nie jest domyślnie włączona](https://wired.com/story/microsoft-recall-off-default-security-concerns)). Nie jest to jednak odosobniony przykład. Innym było automatyczne [włączanie tworzenia kopii zapasowych folderów do OneDrive](https://neowin.net/news/windows-11-is-now-automatically-enabling-onedrive-folder-backup-without-asking-permission) na nowych instalacjach Windows 11, bez pytania o zgodę.

Możesz zwiększyć prywatność i bezpieczeństwo w systemie Windows bez instalowania narzędzi firm trzecich, korzystając z poniższych przewodników:

- Instalacja początkowa (wkrótce)
- [Ustawienia zasad grupy](group-policies.md)
- Ustawienia prywatności (wkrótce)
- Izolacja aplikacji (wkrótce)
- Wzmocnienie zabezpieczeń (wkrótce)

<div class="admonition example" markdown>
<p class="admonition-title">Ta sekcja jest nowa</p>

Sekcja ta jest w trakcie opracowywania, ponieważ przygotowanie instalacji Windows bardziej przyjaznej dla prywatności wymaga znacznie więcej czasu i pracy niż w przypadku innych systemów operacyjnych.

</div>

## Uwagi dotyczące prywatności

Microsoft Windows, zwłaszcza wersje skierowane do konsumentów, takie jak **Home**, często nie priorytetyzują rozwiązań przyjaznych prywatności [domyślnie](https://theguardian.com/technology/2015/jul/31/windows-10-microsoft-faces-criticism-over-privacy-default-settings). W efekcie częściej obserwuje się nadmierne [gromadzenie danych](https://en.wikipedia.org/wiki/Criticism_of_Microsoft#Telemetry_and_data_collection), bez jasnych ostrzeżeń, że takie zachowanie jest ustawieniem domyślnym. W ramach rywalizacji z Google na rynku reklamowym, [Cortana](https://pl.wikipedia.org/wiki/Cortana) wykorzystywałą unikalne identyfikatory, takie jak „identyfikator treści reklamowych”, aby korelować sposób korzystania z systemu i wspierać cele reklamodawców.  W momencie premiery telemetrii nie dało się wyłączyć w wersjach systemu Windows 10 niebędących wersjami korporacyjnymi. Nadal nie można jej całkowicie wyłączyć, ale Microsoft dodał możliwość [ograniczenia](https://extremetech.com/computing/243079-upcoming-windows-update-reduces-spying-microsoft-still-mum-data-collects) przesyłanych danych.

W systemie Windows 11 istnieje szereg ograniczeń lub ustawień domyślnych, takich jak:

- Wymaganie korzystania z konta Microsoft zamiast konta lokalnego.
- Utrudnienie znalezienia opcji kont lokalnych w wersjach Windows **Pro** i **Enterprise**.
- Domyślne włączanie wszystkich opcji gromadzenia danych, co wymaga od użytkownika „rezygnacji” z nich.
- Silna integracja usług Microsoftu, takich jak Bing, OneDrive i Teams, w sposób trudny do usunięcia i przedstawiany jako jedyna opcja.
- Ustawienie domyślnej przeglądarki na Edge lub przywracanie jej, jeśli zostanie zmieniona.
- Dodanie opartych na chmurze funkcji sztucznej inteligencji w wielu obszarach systemu Windows i różnych aplikacjach Microsoftu.
- Niepotrzebne przechowywanie wrażliwych danych. Nawet dane przechowywane lokalnie i niewysyłane do Microsoftu pozostają celem dla hakerów lub złośliwego oprogramowania na urządzeniu.

Microsoft często wykorzystuje mechanizm automatycznych aktualizacji do dodawania nowych funkcji i wprowadzania zmian, które gromadzą dane użytkownika i są domyślnie włączone. Niektóre [funkcje prywatności](https://blogs.windows.com/windows-insider/2023/11/16/previewing-changes-in-windows-to-comply-with-the-digital-markets-act-in-the-european-economic-area), na przykład opcja rezygnacji z synchronizacji konta Microsoft z systemem Windows, wymagają podczas instalacji wybrania kraju w EOG. Po zainstalowaniu systemu można to zmienić na rzeczywisty kraj.

## Wersje systemu Windows

Niestety wiele kluczowych funkcji prywatności i bezpieczeństwa jest zablokowanych za droższymi wersjami systemu Windows, zamiast być dostępnych w wersji Windows **Home**. Do funkcji brakujących w wersji **Home** należą m.in. szyfrowanie dysków funkcją BitLocker, Hyper-V i Windows Sandbox. W naszych przewodnikach dotyczących systemu Windows omówimy, jak prawidłowo korzystać z tych funkcji, więc posiadanie wersji premium systemu będzie konieczne.

Windows **Enterprise** zapewnia największą elastyczność przy konfigurowaniu wbudowanych ustawień prywatności i bezpieczeństwa. Na przykład tylko ta wersja pozwala włączyć najwyższy poziom ograniczeń dotyczących danych wysyłanych do Microsoftu za pomocą narzędzi telemetrycznych. Niestety Enterprise nie jest dostępna w sprzedaży detalicznej, więc może nie być dostępna dla Ciebie.

Najlepsza wersja dostępna w sprzedaży _detalicznej_ to Windows **Pro** — posiada niemal wszystkie funkcje potrzebne do zabezpieczenia urządzenia, w tym BitLocker, Hyper-V itd. Jedyną brakującą rzeczą są niektóre najsurowsze ograniczenia dotyczące telemetrii Microsoftu.

Studenci i nauczyciele mogą otrzymać licencję Windows **Education** (odpowiednik Enterprise) lub **Pro Education** (odpowiednik Pro) bezpłatnie, także na urządzeniach osobistych, od swojej instytucji edukacyjnej. Wiele szkół współpracuje z Microsoft za pośrednictwem OnTheHub lub Microsoft Azure for Education — warto sprawdzić te serwisy lub stronę korzyści swojej uczelni/szkoły, by dowiedzieć się, czy przysługuje Ci dostęp. Możliwość uzyskania takich licencji zależy wyłącznie od Twojej instytucji. Dla wielu osób może to być najprostszy sposób na uzyskanie wersji systemu Windows na poziomie Enterprise do użytku osobistego. Korzystanie z licencji Education nie wiąże się z żadnymi dodatkowymi ryzykami prywatności ani bezpieczeństwa w porównaniu z wersjami detalicznymi.

Nie zaleca się używania zmodyfikowanych wersji systemu Windows, takich jak Windows AME. Zmodyfikowane wydania nie otrzymują aktualizacji, co powoduje, że funkcje bezpieczeństwa i definicje antywirusowe w usłudze Windows Defender pozostają w tyle za aktualnym krajobrazem zagrożeń — naraża to system na ataki i czyni go mniej bezpiecznym.

## Uzyskanie systemu Windows

Currently, only Windows 11 license keys are available for purchase, but these keys will work on Windows 10 as well, so you can still purchase a Windows 11 Pro key to activate a Windows 10 install.

The official [Media Creation Tool](https://microsoft.com/software-download/windows11) is the best way to put a Windows installer on a USB flash drive. Third-party tools like Rufus or Etcher may unexpectedly modify the files, which could lead to boot issues or other troubles when installing.

This tool only lets you install a **Home** or **Pro** installation, as there are no publicly available downloads for Windows **Enterprise** edition. If you have an **Enterprise** license key, you can easily upgrade a **Pro** installation. To do this, install Windows **Pro** without entering a license key during setup, then enter your **Enterprise** key in the Settings app after completing the installation. Your **Pro** install will be upgraded to **Enterprise** automatically after entering a valid license key.

If you are installing an **Education** license then you will typically have a private download link that will be provided alongside your license key when you obtain it from your institution's benefits portal.
