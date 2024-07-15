---
meta_title: "Przeglądarki internetowe na PC i Mac respektujące prywatność - Privacy Guides"
title: "Przeglądarki desktopowe"
icon: material/laptop
description: Te przeglądarki zapewniają lepszą ochronę prywatności niż Google Chrome.
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

Są to obecnie zalecane przez nas przeglądarki internetowe na komputery stacjonarne i konfiguracje do standardowego / nieanonimowego przeglądania. Polecamy [Mullvad Browser](#mullvad-browser), jeśli koncentrujesz się na silnej ochronie prywatności i ochronie przed odciskami palców po instalacji, [Firefox](#firefox) dla standardowego przeglądania internetu jako dobra alternatywa dla Google Chrome, oraz [Brave](#brave), jeśli potrzebujesz kompatybilności z przeglądarką Chromium.

Jeśli chcesz przeglądać Internet anonimowo, powinieneś użyć [Tor](tor.md). Na tej stronie przedstawiamy pewne zalecenia dotyczące konfiguracji, ale wszystkie przeglądarki inne niż Tor Browser będą w taki czy inny sposób śledzone przez *kogoś*.

## Przeglądarka Mullvad

<div class="admonition recommendation" markdown>

![Logo Mullvad Browser](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** to wersja [przeglądarki Tor](tor.md#tor-browser) z usuniętymi integracjami sieci Tor, mająca na celu dostarczenie technologii przeglądarki Tor Browser zapobiegającej odciskom palców użytkownikom VPN. Jest on rozwijany przez Tor Project i dystrybuowany przez [Mullvad](vpn.md#mullvad) i **nie** wymaga korzystania z VPN Mullvad.

[:octicons-home-16: Strona główna](https://mullvad.net/pl/download/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/pl/help/privacy-policy/){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://mullvad.net/pl/help/tag/mullvad-browser/){ .card-link title="Dokumentacja"}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Podobnie jak [Tor Browser](tor.md), przeglądarka Mullvad Browser została zaprojektowana w celu zapobiegania pozostawiania odcisku palcac w sieci poprzez uczynienie odcisku palca przeglądarki identycznym ze wszystkimi innymi użytkownikami Mullvad Browser i zawiera domyślne ustawienia i rozszerzenia, które są automatycznie konfigurowane przez domyślne poziomy bezpieczeństwa: *Standardowy*, *Bezpieczniejszy* i *Najbezpieczniejszy*. Dlatego konieczne jest, aby w ogóle nie modyfikować przeglądarki poza dostosowaniem domyślnych [poziomów bezpieczeństwa](https://tb-manual.torproject.org/security-settings). Inne modyfikacje sprawiłyby, że odcisk palca byłby unikalny, co uniemożliwiłoby prawidłowe i bezpiecznie korzystanie z tej przeglądarki. Jeśli chcesz bardziej skonfigurować swoją przeglądarkę, a fingerprinting nie jest dla Ciebie problemem, zalecamy zamiast tego [Firefox](#firefox).

### Ochrona przed fingerprintingiem

**Bez** korzystania z [VPN](vpn.md), przeglądarka Mullvad zapewnia taką samą ochronę przed [naiwnymi skryptami fingerprintingu](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) jak inne prywatne przeglądarki, takie jak Firefox+[Arkenfox](#arkenfox-advanced) lub [Brave](#brave). Przeglądarka Mullvad zapewnia te zabezpieczenia po instalacji, kosztem pewnej elastyczności i wygody, które mogą zapewnić inne prywatne przeglądarki.

== Aby uzyskać najsilniejszą ochronę przed odciskami palców, zalecamy korzystanie z Mullvad Browser w połączeniu **z** VPN==, niezależnie od tego, czy jest to Mullvad, czy inny zalecany dostawca VPN. Korzystając z VPN z Mullvad Browser, będziesz współdzielić odcisk palca i pulę adresów IP z wieloma innymi użytkownikami, dając ci "tłum", w który możesz się wtopić. Ta strategia jest jedynym sposobem na udaremnienie zaawansowanych skryptów śledzących i jest to ta sama technika anty-fingerprint, którą stosuje przeglądarka Tor.

Należy pamiętać, że chociaż można korzystać z Mullvad Browser z dowolnym dostawcą VPN, inne osoby w tej sieci VPN muszą również korzystać z Mullvad Browser, aby ten "tłum" mógł istnieć, co jest bardziej prawdopodobne w przypadku Mullvad VPN w porównaniu z innymi dostawcami, szczególnie tak blisko uruchomienia Mullvad Browser. Mullvad Browser nie ma wbudowanej łączności VPN, ani nie sprawdza, czy korzystasz z VPN przed przeglądaniem; połączenie VPN musi być skonfigurowane i zarządzane osobno.

Przeglądarka Mullvad Browser jest dostarczana z preinstalowanymi rozszerzeniami przeglądarki *uBlock Origin* i *NoScript*. Chociaż zazwyczaj odradzamy dodawanie *dodatkowych* [rozszerzeń przeglądarki](browser-extensions.md), te rozszerzenia, które są fabrycznie zainstalowane z przeglądarką, **nie** powinny być usuwane ani konfigurowane poza ich domyślnymi wartościami, ponieważ spowodowałoby to zauważalne odróżnienie odcisku palca przeglądarki od innych użytkowników Mullvad Browser. </em> Przeglądarka jest również dostarczana z preinstalowanym rozszerzeniem przeglądarki Mullvad, które *można bezpiecznie usunąć bez wpływu na odcisk palca przeglądarki, ale można je również bezpiecznie pozostawić, nawet jeśli nie korzystasz z Mullvad VPN.</p>

### Tryb prywatny przeglądarki

Mullvad Browser działa w stałym trybie przeglądania prywatnego, co oznacza, że historia, pliki cookie i inne dane witryn będą zawsze czyszczone po każdym zamknięciu przeglądarki. Zakładki, ustawienia przeglądarki i ustawienia rozszerzeń zostaną zachowane.

Jest to wymagane, aby zapobiec zaawansowanym formom śledzenia, ale odbywa się kosztem wygody i niektórych funkcji Firefox'a, takich jak kontenery z wieloma kontami. Pamiętaj, że zawsze możesz korzystać z wielu przeglądarek, na przykład możesz rozważyć użycie Firefox + Arkenfox dla kilku witryn, na których chcesz pozostać zalogowany lub które nie działają poprawnie w Mullvad Browser, oraz Mullvad Browser do ogólnego przeglądania.

### Mullvad Leta

Mullvad Browser jest dostarczany z DuckDuckGo ustawionym jako domyślna wyszukiwarka [](search-engines.md), ale jest również preinstalowany z wyszukiwarką **Mullvad Leta**, która wymaga aktywnej subskrypcji Mullvad VPN, aby uzyskać do niej dostęp. Mullvad Leta odpytuje bezpośrednio API płatnego wyszukiwania Google, dlatego jest ograniczona do płatnych subskrybentów. Jednak z powodu tego ograniczenia Mullvad może skorelować zapytania wyszukiwania i konta Mullvad VPN. Z tego powodu odradzamy korzystanie z Mullvad Leta, mimo że Mullvad zbiera bardzo mało informacji o swoich subskrybentach VPN.

## Firefox

<div class="admonition recommendation" markdown>

![Logo Firefox](assets/img/browsers/firefox.svg){ align=right }

**Firefox** zapewnia silne ustawienia prywatności, takie jak [wzmocniona ochrona przed śledzeniem](https://support.mozilla.org/pl/kb/wzmocniona-ochrona-przed-sledzeniem-firefox-desktop), które mogą pomóc zablokować różne [rodzaje śledzenia](https://support.mozilla.org/pl/kb/wzmocniona-ochrona-przed-sledzeniem-firefox-desktop#w_co-blokuje-wzmocniona-ochrona-przed-sledzeniem).

[:octicons-home-16: Strona główna](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/pl/privacy/firefox){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="Dokumentacja"}
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Przyczyń się" }

<details class="downloads" markdown>
<summary>Downloads</summary>

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

These options can be found in :material-menu: → **Settings**.

#### Website Advertising Preferences

- [ ] Uncheck **Allow websites to perform privacy-preserving ad measurement**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2/). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.

#### Wyszukiwarka

- [ ] Odznacz **Pokaż sugestie wyszukiwania**

Funkcje sugestii wyszukiwania mogą być niedostępne w danym regionie.

Sugestie wyszukiwania wysyłają wszystko, co wpisujesz w pasku adresu, do domyślnej wyszukiwarki, niezależnie od tego, czy wysyłasz rzeczywiste wyszukiwanie. Wyłączenie sugestii wyszukiwania pozwala bardziej precyzyjnie kontrolować dane wysyłane do dostawcy wyszukiwarki.

##### Firefox Suggest (tylko USA)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) to funkcja podobna do sugestii wyszukiwania, która jest dostępna tylko w Stanach Zjednoczonych. Zalecamy jej wyłączenie z tego samego powodu, dla którego zalecamy wyłączenie sugestii wyszukiwania. Jeśli nie widzisz tych opcji pod **paskiem adresu strony** , nie masz tej funkcjonalności i możesz zignorować te zmiany.

- [ ] Odznacz **Sugestie z Firefox**
- [ ] Usuń zaznaczenie **Sugestie od sponsorów**

#### Prywatność i bezpieczeństwo

##### Udoskonalona ochrona przed śledzeniem

- [x] Wybierz **Ścisła** ochrona przed śledzeniem

Chroni to użytkownika poprzez blokowanie modułów śledzących w mediach społecznościowych, skryptów fingerprinting (należy pamiętać, że nie chroni to przed *wszystkimi* odciskami palców), koparek kryptowalut, plików cookie śledzących różne witryny i niektórych innych treści śledzących. Ochrona przed śledzeniem chroni przed wieloma typowymi zagrożeniami, ale nie blokuje wszystkich ścieżek śledzenia, ponieważ została zaprojektowana tak, aby mieć minimalny lub zerowy wpływ na użyteczność witryny.

##### Wyczyść po zamknięciu

Jeśli chcesz pozostać zalogowany w określonych witrynach, możesz zezwolić na wyjątki w **Pliki cookie i dane witryn** → **Zarządzaj wyjątkami....**

- [x] Zaznacz **Usuń pliki cookie i dane witryn po zamknięciu przeglądarki Firefox**

Chroni to użytkownika przed trwałymi plikami cookie, ale nie chroni przed plikami cookie pozyskanymi podczas jednej sesji przeglądania. Po włączeniu tej opcji możliwe jest łatwe wyczyszczenie plików cookie przeglądarki poprzez ponowne uruchomienie Firefoksa. Możesz ustawić wyjątki dla poszczególnych witryn, jeśli chcesz pozostać zalogowany w określonej witrynie, którą często odwiedzasz.

##### Telemetria

- [ ] Usuń zaznaczenie **Zezwalaj przeglądarce Firefox na wysyłanie danych technicznych i dotyczących interakcji do Mozilla**
- [ ] Usuń zaznaczenie **Zezwalaj przeglądarce Firefox na instalowanie i uruchamianie badań**
- [ ] Usuń zaznaczenie **Zezwalaj przeglądarce Firefox na wysyłanie raportów o awariach w Twoim imieniu**

> Firefox wysyła o nas dane o wersji i języku Firefoksa, systemie operacyjnym urządzeniach i konfiguracji sprzętowej, pamięci, podstawowe informacje o awariach i błędach oraz wynikach zautomatyzowanych procesów, takich jak aktualizacje, bezpieczne przeglądanie i aktywacja. Gdy przeglądarka Firefox wysyła nasze dane, adres IP użytkownika jest tymczasowo gromadzony w dziennikach serwera.

Ponadto usługa Mozilla Accounts gromadzi [pewne dane techniczne](https://mozilla.org/privacy/mozilla-accounts). Jeśli korzystasz z konta Firefox, możesz z tego zrezygnować:

1. Otwórz ustawienia profilu [na accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Usuń zaznaczenie **Gromadzenie i wykorzystywanie danych** > **Pomóż ulepszyć konta Firefox**

##### Tryb tylko HTTPS

- [x] Select **Enable HTTPS-Only Mode in all windows**

Zapobiega to niezamierzonemu łączeniu się z witryną internetową w postaci zwykłego tekstu HTTP. Witryny bez HTTPS są obecnie rzadkością, więc nie powinno to mieć żadnego wpływu na codzienne przeglądanie.

##### DNS przez HTTPS

Jeśli korzystasz z [dostawcy DNS over HTTPS](dns.md):

- [x] Wybierz opcję **Maksymalna ochrona** i wybierz odpowiedniego dostawcę

Maksymalna ochrona wymusza użycie DNS przez HTTPS, a ostrzeżenie o bezpieczeństwie pokaże się, jeśli Firefox nie może połączyć się z bezpiecznym resolwerem DNS, lub jeśli Twój bezpieczny resolwer DNS mówi, że rekordy domeny, do której próbujesz uzyskać dostęp, nie istnieją. Dzięki temu sieć, z którą jesteś połączony, nie będzie mogła potajemnie obniżyć Twoich zabezpieczeń DNS.

#### Synchronizacja

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (zaawansowany)

<div class="admonition tip" markdown>
<p class="admonition-title">Korzystaj z przeglądarki Mullvad Browser do zaawansowanej ochrony przed odciskami palców</p>

[Mullvad Browser](#mullvad-browser) provides the same anti-fingerprinting protections as Arkenfox out of the box, and does not require the use of Mullvad's VPN to benefit from these protections. Coupled with a VPN, Mullvad Browser can thwart more advanced tracking scripts which Arkenfox cannot. Arkenfox still has the advantage of being much more flexible, and allowing per-site exceptions for websites which you need to stay logged in to.

</div>

The [Arkenfox project](https://github.com/arkenfox/user.js) provides a set of carefully considered options for Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly - [which you can easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. We **strongly recommend** reading through their full [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave is built upon the Chromium web browser project, so it should feel familiar and have minimal website compatibility issues.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

**macOS users:** The download for Brave Browser from their official website is a `.pkg` installer which requires admin privileges to run (and may run other unnecessary scripts on your machine). As an alternative, you can download the latest `Brave-Browser-universal.dmg` file from their [GitHub releases](https://github.com/brave/brave-browser/releases/latest) page, which provides a traditional "drag to Applications folder" install.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Brave adds a "[referral code](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" to the file name in downloads from the Brave website, which is used to track which source the browser was downloaded from, for example `BRV002` in a download named `Brave-Browser-BRV002.pkg`. The installer will then ping Brave's server with the referral code at the end of the installation process. If you're concerned about this, you can rename the installer file before opening it.

</div>

### Recommended Brave Configuration

These options can be found in :material-menu: → **Settings**.

#### Settings

##### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

Shields' options can be downgraded on a per-site basis as needed, but by default we recommend setting the following:

<div class="annotate" markdown>

- [x] Select **Prevent sites from fingerprinting me based on my language preferences**
- [x] Select **Aggressive** under *Trackers & ads blocking*

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. We advise against using this feature; instead, keep the default filter lists. Using extra lists will make you stand out from other Brave users and may also increase attack surface if there is an exploit in Brave and a malicious rule is added to one of the lists you use.

</details>

- [x] Select **Strict** under *Upgrade connections to HTTPS*
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Strict, may break sites** under *Block fingerprinting*
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode).
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar.

##### Privacy and security

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP Handling Policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Private window with Tor** (1)

</div>

1. Brave is **not** as resistant to fingerprinting as the Tor Browser and far fewer people use Brave with Tor, so you will stand out. Where [strong anonymity is required](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) use the [Tor Browser](tor.md#tor-browser).

<div class="admonition tip" markdown>
<p class="admonition-title">Sanitizing on close</p>

- [x] In the *Sites and Shields Settings* menu, under Content, after clicking on the *On-device site data* menu, select **Delete data sites have saved to your device when you close all windows**.

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

##### Extensions

- [ ] Uncheck all built-in extensions you do not use

##### Web3

Brave's Web3 features can potentially add to your browser fingerprint and attack surface. Unless you use any of features, they should be disabled.

- Select **Extensions (no fallback)** under *Default Ethereum wallet* and *Default Solana wallet*
- Set *Method to resolve IPFS resources* to **Disabled**

##### System

<div class="annotate" markdown>

- [ ] Uncheck **Continue running apps when Brave is closed** to disable background apps (1)

</div>

1. This option is not present on all platforms.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

## Dodatkowe zasoby

## Kryteria

**Pamiętaj, że nie jesteśmy związani z żadnym z zalecanych projektów.** W dodatku do [naszych standardowych kryteriów](about/criteria.md), opracowaliśmy zestaw wymagań, które umożliwiają nam podejmowanie obiektywnych decyzji. Zalecamy zapoznanie się z tą listą przed zdecydowaniem o wyborze projektu oraz przeprowadzenie własnego rozeznania, aby upewnić się, że będzie dobrym wyborem dla Ciebie.

### Wymagania minimalne

- Must be open-source software.
- Must support automatic updates.
- Must receive engine updates in 0-1 days from upstream release.
- Must be available on Linux, macOS, and Windows.
- Any changes required to make the browser more privacy-respecting must not negatively impact user experience.
- Must block third-party cookies by default.
- Must support [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### Best-Case

Our best-case criteria represents what we would like to see from the perfect project in this category. Our recommendations may not include any or all of this functionality, but those which do may rank higher than others on this page.

- Should include built-in content blocking functionality.
- Should support cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Should support Progressive Web Apps. PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps, because PWAs benefit from your browser's regular security updates.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Should not collect telemetry by default.
- Should provide an open-source sync server implementation.
- Should default to a [private search engine](search-engines.md).

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
