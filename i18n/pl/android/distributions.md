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

GrapheneOS obsługuje [izolowaną aplikację Google Play](https://grapheneos.org/usage#sandboxed-google-play), które uruchamia Usługi Google Play w pełni w piaskownicy, jak każdą inną zwykłą aplikację. This means you can take advantage of most Google Play Services, such as push notifications, while giving you full control over their permissions and access, and while containing them to a specific [work profile](../os/android-overview.md#work-profile) or [user profile](../os/android-overview.md#user-profiles) of your choice.

[Google Pixel phones](../mobile-phones.md#google-pixel) are the only devices that currently meet GrapheneOS's [hardware security requirements](https://grapheneos.org/faq#future-devices). The Pixel 8 and later support ARM's Memory Tagging Extension (MTE), a hardware security enhancement that drastically lowers the probability of exploits occurring through memory corruption bugs. GrapheneOS greatly expands the coverage of MTE on supported devices. Whereas the stock OS only allows you to opt in to a limited implementation of MTE via a developer option or Google's Advanced Protection Program, GrapheneOS features a more robust implementation of MTE by default in the system kernel, default system components, and their Vanadium web browser and its WebView.

GrapheneOS also provides a global toggle for enabling MTE on all user-installed apps at :gear: **Settings** → **Security & privacy** → **Exploit protection** → **Memory tagging** → **Enable by default**. The OS also features per-app toggles to opt out of MTE for apps which may crash due to compatibility issues.

### Connectivity Checks

By default, Android makes many network connections to Google to perform DNS connectivity checks, to sync with current network time, to check your network connectivity, and for many other background tasks. GrapheneOS replaces these with connections to servers operated by GrapheneOS and subject to their privacy policy. This hides information like your IP address [from Google](../basics/common-threats.md#privacy-from-service-providers), but means it is trivial for an admin on your network or ISP to see you are making connections to `grapheneos.network`, `grapheneos.org`, etc. and deduce what operating system you are using.

If you want to hide information like this from an adversary on your network or ISP, you **must** use a [trusted VPN](../vpn.md) in addition to changing the connectivity check setting to **Standard (Google)**. It can be found in :gear: **Settings** → **Network & internet** → **Internet connectivity checks**. This option allows you to connect to Google's servers for connectivity checks, which, alongside the usage of a VPN, helps you blend in with a larger pool of Android devices.

## Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](../about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

- Must be open-source software.
- Must support bootloader locking with custom AVB key support.
- Must receive major Android updates within 0-1 months of release.
- Must receive Android feature updates (minor version) within 0-14 days of release.
- Must receive regular security patches within 0-5 days of release.
- Must **not** be "rooted" out of the box.
- Must **not** enable Google Play Services by default.
- Must **not** require system modification to support Google Play Services.
