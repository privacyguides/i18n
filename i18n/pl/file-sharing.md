---
title: Udostępnianie i synchronizacja plików
icon: material/share-variant
description: Dowiedz się, jak prywatnie udostępniać pliki między urządzeniami, znajomymi i rodziną albo anonimowo w sieci.
cover: file-sharing.webp
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-server-network: Dostawcy usług](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Dowiedz się, jak prywatnie udostępniać pliki między urządzeniami, znajomymi i rodziną albo anonimowo w sieci.

## Udostępnianie plików

Jeśli już korzystasz z [Proton Drive](cloud.md#proton-drive)[^1] lub posiadasz subskrypcję [Bitwarden](passwords.md#bitwarden) Premium[^2], rozważ skorzystanie z oferowanych przez nie funkcji udostępniania plików — obie wykorzystują szyfrowanie end-to-end. W przeciwnym razie samodzielne rozwiązania wymienione poniżej zapewniają, że udostępniane pliki nie są odczytywane przez zdalny serwer.

### Send

<div class="admonition recommendation" markdown>

![Logo Send](assets/img/file-sharing-sync/send.svg){ align=right }

**Send** to fork wycofanej usługi Firefox Send od Mozilli, który pozwala wysyłać pliki innym za pomocą linku. Pliki są szyfrowane na urządzeniu, więc serwer nie ma do nich dostępu, a dodatkowo można je opcjonalnie chronić hasłem. Opiekun projektu Send udostępnia [instancję publiczną](https://send.vis.ee). Można też korzystać z innych publicznych instancji albo hostować Send samodzielnie.

[:octicons-home-16: Strona główna](https://send.vis.ee){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="Instancje publiczne"}
[:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title="Wesprzyj" }

</details>

</div>

Z Send można korzystać poprzez interfejs internetowy lub narzędzie [ffsend](https://github.com/timvisee/ffsend) w wierszu poleceń. Jeśli praca w wierszu poleceń nie jest Ci obca i często wysyłasz pliki, zalecamy korzystanie z klienta CLI, aby uniknąć szyfrowania opartego na JavaScript. Można wskazać konkretny serwer, używając flagi `--host`:

```bash
ffsend upload --host https://send.vis.ee/ FILE
```

### OnionShare

<div class="admonition recommendation" markdown>

![Logo OnionShare](assets/img/file-sharing-sync/onionshare.svg){ align=right }

**OnionShare** to narzędzie typu open source, które umożliwia bezpieczne i [:material-incognito: anonimowe](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } udostępnianie plików o dowolnym rozmiarze. Działa poprzez uruchomienie serwera WWW dostępnego jako usługa .onion w sieci Tor, z trudnym do odgadnięcia adresem URL, którym można podzielić się z odbiorcami, aby pobrali lub przesłali pliki.

[:octicons-home-16: Strona główna](https://onionshare.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="Usługa .onion" }
[:octicons-info-16:](https://docs.onionshare.org){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:fontawesome-brands-windows: Windows](https://onionshare.org/#download)
- [:simple-apple: macOS](https://onionshare.org/#download)
- [:simple-linux: Linux](https://onionshare.org/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/org.onionshare.OnionShare)

</details>

</div>

OnionShare oferuje również możliwość połączenia się za pośrednictwem [mostków Tor](https://docs.onionshare.org/2.6.2/pl/tor.html#automatic-censorship-circumvention), co pozwala obejść [:material-close-outline: cenzurę](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}.

### Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

- Nie może przechowywać odszyfrowanych danych na zdalnym serwerze.
- Musi być oprogramowaniem typu open source.
- Musi mieć klienty dla systemów Linux, macOS i Windows albo oferować interfejs internetowy.

## Synchronizacja plików

### Syncthing (P2P)

<div class="admonition recommendation" markdown>

![Logo Syncthing](assets/img/file-sharing-sync/syncthing.svg){ align=right }

**Syncthing** to narzędzie peer-to-peer typu open source do ciągłej synchronizacji plików. Służy do synchronizacji plików między dwoma lub więcej urządzeniami w sieci lokalnej lub przez Internet. Syncthing nie korzysta z serwera scentralizowanego; do transferu danych między urządzeniami używa protokołu [Block Exchange Protocol](https://docs.syncthing.net/specs/bep-v1.html#bep-v1). Wszystkie dane są szyfrowane przy użyciu protokołu TLS.

[:octicons-home-16: Strona główna](https://syncthing.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.syncthing.net){ .card-link title=Dokumentacja}
[:octicons-code-16:](https://github.com/syncthing){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://syncthing.net/donations){ .card-link title=Wesprzyj }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:fontawesome-brands-windows: Windows](https://syncthing.net/downloads)
- [:simple-apple: macOS](https://syncthing.net/downloads)
- [:simple-linux: Linux](https://syncthing.net/downloads)
- [:simple-freebsd: FreeBSD](https://syncthing.net/downloads)

</details>

</div>

### Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

#### Minimalne wymagania

- Nie może wymagać zewnętrznego serwera zdalnego ani usług chmurowych.
- Musi być oprogramowaniem typu open source.
- Musi mieć klienty dla systemów Linux, macOS i Windows albo oferować interfejs internetowy.

#### Najlepszy scenariusz

Nasze kryteria „najlepszego scenariusza” określają, jak powinien wyglądać idealny projekt w tej kategorii. Nasze zalecenia nie muszą spełniać wszystkich tych warunków, jednak projekty, które spełniają więcej z nich, mogą być oceniane wyżej od pozostałych na stronie.

- Powinien mieć aplikacje mobilne dla systemów iOS i Android, które przynajmniej obsługują podgląd dokumentów.
- Powinien obsługiwać tworzenie kopii zapasowych zdjęć z systemu iOS i Android, a opcjonalnie synchronizację plików i folderów na Androidzie.

[^1]: Proton Drive pozwala [udostępniać pliki lub foldery](https://proton.me/support/drive-shareable-link) poprzez wygenerowanie publicznego linku do udostępnienia albo przesłanie unikatowego linku na wskazany adres e-mail. Linki publiczne można zabezpieczyć hasłem, ustawić dla nich datę wygaśnięcia oraz całkowicie cofnąć dostęp; linki wysyłane za pośrednictwem wiadomości e-mail mogą mieć przypisane niestandardowe uprawnienia i również podlegać cofnięciu. Zgodnie z [polityką prywatności](https://proton.me/pl/drive/privacy-policy) Proton Drive, zawartość plików, nazwy plików i folderów oraz podglądy miniatur są szyfrowane end-to-end.
[^2]: Dzięki subskrypcji [Premium](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans), [Bitwarden Send](https://bitwarden.com/products/send) umożliwia bezpieczne udostępnianie plików i tekstu z użyciem [szyfrowania end-to-end](https://bitwarden.com/help/send-encryption). Można wymagać [hasła](https://bitwarden.com/help/send-privacy/#send-passwords) wraz z linkiem Send. Bitwarden Send oferuje też funkcję [automatycznego usuwania](https://bitwarden.com/help/send-lifespan).
