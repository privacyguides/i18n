---
meta_title: "Najlepsze systemy operacyjne Android – Privacy Guides"
title: Alternatywne dystrybucje
description: Możesz zastąpić system operacyjny w swoim telefonie z Androidem jednymi z tych bezpiecznych i dbających o prywatność alternatyw.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Prywatne systemy operacyjne Android
    url: "./"
  - "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://pl.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-target-account: Ataki ukierunkowane](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Ataki pasywne](../basics/common-threats.md#security-and-privacy){ .pg-orange }

**Niestandardowy system operacyjny oparty na Androidzie** (czasami określany jako **custom ROM**) może być sposobem na osiągnięcie wyższego poziomu prywatności i bezpieczeństwa na Twoim urządzeniu. Jest to przeciwieństwo „standardowej” wersji Androida, która jest fabrycznie zainstalowana w telefonie i często jest głęboko zintegrowana z Usługami Google Play oraz innym oprogramowaniem producenta.

Zalecamy zainstalowanie systemu GrapheneOS, jeśli masz Google Pixel, ponieważ zapewnia on wzmocnione zabezpieczenia i dodatkowe funkcje prywatności. Powody, dla których nie wymieniamy innych systemów operacyjnych ani urządzeń, są następujące:

- Często mają one [słabsze zabezpieczenia](index.md#install-a-custom-distribution).
- Wsparcie jest często porzucane, gdy opiekun projektu traci zainteresowanie lub zmienia urządzenie, co kontrastuje z przewidywalnym [cyklem wsparcia](https://grapheneos.org/faq#device-lifetime) stosowanym przez GrapheneOS.
- Zazwyczaj nie wnoszą znaczących ulepszeń prywatności ani bezpieczeństwa, które uzasadniałyby ich instalację.

## GrapheneOS

<div class="admonition recommendation" markdown>

![Logo GrapheneOS](../assets/img/android/grapheneos.svg#only-light){ align=right }
![Logo GrapheneOS](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** to najlepszy wybór pod względem prywatności i bezpieczeństwa.

GrapheneOS zapewnia dodatkowe [wzmocnienia zabezpieczeń](https://en.wikipedia.org/wiki/Hardening_\(computing\)) i usprawnienia prywatności. Posiada [wzmocniony alokator pamięci](https://github.com/GrapheneOS/hardened_malloc), uprawnienia do sieci i czujników oraz różne inne [funkcje bezpieczeństwa](https://grapheneos.org/features). GrapheneOS oferuje również pełne aktualizacje oprogramowania układowego i podpisane kompilacje, dzięki czemu funkcja zweryfikowanego rozruchu (_verified boot_) jest w pełni obsługiwana.

[:octicons-home-16: Strona główna](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title="Wesprzyj" }

</div>

GrapheneOS obsługuje [izolowaną aplikację Google Play](https://grapheneos.org/usage#sandboxed-google-play), które uruchamia Usługi Google Play w pełni w piaskownicy, jak każdą inną zwykłą aplikację. Oznacza to, że można korzystać z większości Usług Google Play, takich jak powiadomienia push, mając jednocześnie pełną kontrolę nad ich uprawnieniami i dostępem oraz ograniczając je do wybranego [profilu słuzbowego](../os/android-overview.md#work-profile) lub [profilu użytkownika](../os/android-overview.md#user-profiles).

[Telefony Google Pixel](../mobile-phones.md#google-pixel) to jedyne urządzenia, które obecnie spełniają [wymagania sprzętowe dotyczące bezpieczeństwa](https://grapheneos.org/faq#future-devices) GrapheneOS. Pixel 8 i nowsze wspierają Memory Tagging Extension (MTE) firmy ARM — sprzętowe usprawnienie bezpieczeństwa, które znacznie zmniejsza prawdopodobieństwo wystąpienia exploitów wynikających z błędów naruszenia pamięci. GrapheneOS znacząco rozszerza wykorzystanie MTE na obsługiwanych urządzeniach. Podczas gdy standardowy system operacyjny pozwala jedynie na ograniczone włączenie MTE za pośrednictwem opcji deweloperskiej lub Programu ochrony zaawansowanej Google, GrapheneOS stosuje bardziej solidną implementację MTE domyślnie w jądrze systemu, domyślnych komponentach systemowych oraz w przeglądarce internetowej Vanadium i jej WebView.

GrapheneOS udostępnia też globalny przełącznik włączający MTE dla wszystkich aplikacji instalowanych przez użytkownika w :gear: **Ustawienia** → **Bezpieczeństwo i prywatność** → **Exploit protection** → **Memory tagging** → **Włącz domyślnie**. System oferuje także przełączniki dla poszczególnych aplikacji, pozwalające wyłączyć MTE dla aplikacji, które mogą ulec awarii z powodu problemów ze zgodnością.

### Sprawdzanie łączności

Domyślnie Android nawiązuje wiele połączeń sieciowych z Google w celu sprawdzenia łączności DNS, synchronizacji z bieżącym czasem sieciowym, sprawdzania łączności sieciowej i realizowania innych zadań w tle. GrapheneOS zastępuje je połączeniami z serwerami obsługiwanymi przez GrapheneOS i objętymi ich polityką prywatności. Ukrywa to informacje takie jak adres IP [przed Google](../basics/common-threats.md#privacy-from-service-providers), ale oznacza, że administrator sieci lub dostawca usług internetowych może łatwo zauważyć połączenia do `grapheneos.network`, `grapheneos.org` itp. i wywnioskować, jakiego systemu operacyjnego używasz.

Jeśli celem jest ukrycie takich informacji przed przeciwnikiem obecnym w Twojej sieci lub dostawcą usług internetowych, **musisz** użyć [zaufanej sieci VPN](../vpn.md) oprócz zmiany ustawienia sprawdzania łączności na **Standard (Google)**. Opcja ta znajduje się w :gear: **Ustawienia** → **Sieć i internet** → **Internet connectivity checks**. Pozwala to na łączenie się z serwerami Google w celu sprawdzania łączności, co w połączeniu z użyciem sieci VPN pomaga wtopić się w szerszą pulę urządzeń z Androidem.

## Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](../about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

- Musi być oprogramowaniem typu open source.
- Musi obsługiwać blokadę bootloadera z obsługą niestandardowych kluczy AVB.
- Musi otrzymywać główne aktualizacje Androida w ciągu 0–1 miesiąca od wydania.
- Musi otrzymywać aktualizacje funkcji Androida (wersje poboczne) w ciągu 0–14 dni od wydania.
- Musi otrzymywać regularne poprawki bezpieczeństwa w ciągu 0–5 dni od wydania.
- **Nie** może być domyślnie „zrootowany”.
- **Nie** może domyślnie włączać Usług Google Play.
- **Nie** może wymagać modyfikacji systemu, aby obsługiwać Usługi Google Play.
