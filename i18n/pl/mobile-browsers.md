---
meta_title: "Przeglądarki internetowe szanujące prywatność dla Androida i iOS – Privacy Guides"
title: Przeglądarki mobilne
icon: octicons/device-mobile-16
description: Te przeglądarki to obecnie nasze zalecenia do standardowego/nieanonimowego korzystania z Internetu na telefonie.
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Zalecane prywatne przeglądarki mobilne
    url: "./"
    relatedLink: "../desktop-browsers/"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    applicationCategory: Web Browser
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Cromite
    image: /assets/img/browsers/cromite.svg
    url: https://cromite.org
    applicationCategory: Web Browser
    operatingSystem:
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://apple.com/safari
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-account-cash: Kapitalizm inwigilacji](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Oto nasze aktualne zalecenia dotyczące **mobilnych przeglądarek internetowych** oraz ich konfiguracji do standardowego/nieanonimowego przeglądania. Jeśli chcesz przeglądać Internet anonimowo, skorzystaj z sieci [Tor](tor.md).

## Brave

<div class="admonition recommendation" markdown>

![Logo Brave](assets/img/browsers/brave.svg){ align=right }

**Przeglądarka Brave** zawiera wbudowany mechanizm blokowania treści oraz liczne [funkcje prywatności](https://brave.com/privacy-features), z których wiele jest domyślnie włączonych.

Oparta jest na projekcie przeglądarki Chromium, dzięki czemu jej interfejs i działanie powinny być dobrze znane większości osób, a problemy ze zgodnością stron internetowych być minimalne.

[:octicons-home-16: Strona główna](https://brave.com/pl){ .md-button .md-button--primary }
[:simple-torbrowser:]
(https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Usługa onion" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-fdroid: F-Droid](https://brave-browser-apk-release.s3.brave.com/fdroid/repo/index.html)

</details>

</div>

### Zalecana konfiguracja przeglądarki Brave

Tor Browser to jedyny sposób na prawdziwie anonimowe przeglądanie Internetu. Korzystając z Brave, zalecamy zmianę poniższych ustawień, aby lepiej chronić swoją prywatność przed niektórymi podmiotami, jednak każda przeglądarka inna niż [Tor Browser](tor.md#tor-browser) będzie możliwa do śledzenia przez *kogoś* w taki czy inny sposób.

=== "Android"

    Te opcje znajdziesz w :material-menu: → **Ustawienia** → **Tarcze Brave i prywatność**.

=== "iOS"

    Te opcje znajdziesz w :fontawesome-solid-ellipsis: → **Ustawienia** → **Tarcze i prywatność**.

#### Domyślne ustawienia Tarcz Brave

Brave posiada pewne zabezpieczenia przed identyfikacją przeglądarki w ramach funkcji [Tarcze](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Zalecamy skonfigurowanie tych ustawień [globalnie](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) – czyli dla wszystkich odwiedzanych stron.

W razie potrzeby można je obniżyć dla poszczególnych witryn, jednak domyślnie zalecamy następującą konfigurację:

=== "Android"

    <div class="annotate" markdown>

    - [x] Wybierz **agresywnie** w sekcji *Zablokuj skrypty śledzące i reklamy*
    - [x] Zaznacz **Automatyczne przekierowywanie stron AMP**
    - [x] Zaznacz **Automatycznie przekierowuj śledzące adresy URL**
    - [x] Wybierz **Wymagaj, aby wszystkie połączenia używały HTTPS (ścisłe)** w sekcji *Aktualizacje HTTPS*
    - \[x\] (Opcjonalnie) Zaznacz **Zablokuj skrypty** (1)
    - [x] Wybierz **Blokuj pliki cookie innych firm** w sekcji *Zablokuj pliki cookies*
    - [x] Zaznacz **Zablokuj rozpoznawanie urządzenia**
    - [x] Zaznacz **Zapobiegaj pobieraniu odcisków palców za pomocą ustawień językowych**

    <details class="warning" markdown>
    <summary>Używaj domyślnych list filtrów</summary>

    Brave umożliwia wybór dodatkowych filtrów treści w menu **Filtrowanie treści** lub na stronie wewnętrznej `brave://adblock`. Odradzamy korzystanie z tej funkcji; zamiast tego pozostaw domyślne listy filtrów. Korzystanie z dodatkowych list może sprawić, że będziesz się wyróżniać na tle innych użytkowników Brave, a także zwiększyć ryzyko ataku, jeśli w Brave pojawi się luka, a do którejś z list zostanie dodana złośliwa reguła.

    </details>

    - [x] Zaznacz **Zapomnij po zamknięciu tej strony**

    </div>

    1. Ta opcja wyłącza JavaScript, co sprawi, że wiele stron przestanie działać prawidłowo. Aby przywrócić ich działanie, możesz dodać wyjątki dla konkretnych stron, stukając ikonę tarczy w pasku adresu i odznaczając tę opcję w sekcji *Zaawansowane sterowanie*.

=== "iOS"

    <div class="annotate" markdown>

    - [x] Wybierz **agresywnie** w sekcji *Blokowanie skryptów śledzących i reklam*
    - [x] Wybierz **ścisłe** w sekcji *Aktualizacje HTTPS*
    - [x] Zaznacz **Automatyczne przekierowywanie stron AMP**
    - [x] Zaznacz **Automatycznie przekierowuj śledzące adresy URL**
    - \[x\] (Opcjonalnie) Zaznacz **Zablokuj skrypty** (1)
    - [x] Zaznacz **Zablokuj rozpoznawanie urządzenia**
    - [x] Select **Site Tabs Closed** under *Auto Shred*

    <details class="warning" markdown>
    <summary>Używaj domyślnych list filtrów</summary>

    Brave umożliwia wybór dodatkowych filtrów treści w menu **Filtrowanie treści**. Odradzamy korzystanie z tej funkcji; zamiast tego pozostaw domyślne listy filtrów. Korzystanie z dodatkowych list może sprawić, że będziesz się wyróżniać na tle innych użytkowników Brave, a także zwiększyć ryzyko ataku, jeśli w Brave pojawi się luka, a do którejś z list zostanie dodana złośliwa reguła.

    </details>

    </div>

    1. Ta opcja wyłącza JavaScript, co sprawi, że wiele stron przestanie działać prawidłowo. Aby przywrócić ich działanie, możesz dodać wyjątki dla konkretnych stron, stukając ikonę tarczy w pasku adresu i odznaczając tę opcję w sekcji *Zaawansowane sterowanie*.

##### Wyczyść dane przeglądania (tylko Android)

- [x] Zaznacz **Wyczyść dane przy wyjściu**

##### Zablokuj sieci społecznościowe (tylko Android)

- [ ] Odznacz wszystkie komponenty mediów społecznościowych

#### Inne ustawienia prywatności

=== "Android"

    <div class="annotate" markdown>

    - [x] Wybierz **Wyłącz UDP bez proxy** w sekcji [*Zasady obsługi IP WebRTC IP*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
    - \[x\] (Opcjonalnie) Wybierz **Brak ochrony** w sekcji *Bezpieczne przeglądanie* (1)
    - [ ] Odznacz **Zezwalaj stronom internetowym na sprawdzanie, czy masz zapisane formy płatności**
    - [ ] Odznacz **Optymalizacja i zabezpieczenia JavaScriptu** w sekcji o tej samej nazwie
    - [x] Zaznacz **Zamknij karty przy wyjściu**
    - [ ] Odznacz **Zezwól na zastosowanie analizy produktów z zachowaniem prywatności (P3A)**
    - [ ] Odznacz **Automatycznie wysyłaj raporty diagnostyczne**
    - [ ] Odznacz **Automatycznie wysyłaj pingi dziennego użycia do Brave**

    </div>

    1. Implementacja funkcji [Bezpiecznego przeglądania](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) w przeglądarce Brave na Androidzie **nie** przesyła [żądań sieciowych Bezpiecznego przeglądania](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) przez serwer pośredniczący, w przeciwieństwie do wersji na komputery stacjonarne. Oznacza to, że Twój adres IP może być widoczny (i rejestrowany) przez Google. Należy również pamiętać, że funkcja Bezpiecznego przeglądania nie jest dostępna na urządzeniach z Androidem bez Usług Google Play.

=== "iOS"

    - [ ] Odznacz **Zezwól na zastosowanie analizy produktów z zachowaniem prywatności (P3A)**
    - [ ] Odznacz **Automatycznie wysyłaj pingi dziennego użycia do Brave**

#### Leo

Te opcje znajdziesz w :material-menu: → **Ustawienia** → **Sztuczna inteligencja Leo**.

<div class="annotate" markdown>

- [ ] Odznacz **Pokaż sugestie automatycznego uzupełniania na pasku adresu** (1)

</div>

1. Ta opcja nie występuje w aplikacji Brave na iOS.

#### Wyszukiwarki

Te opcje znajdziesz w :material-menu:/:fontawesome-solid-ellipsis: → **Ustawienia** → **Wyszukiwarki**.

- [ ] Odznacz **Pokaż sugestie wyszukiwania**

#### Synchronizacja

[Brave Sync](https://support.brave.app/hc/pl/articles/360059793111-Zrozumienie-Brave-Sync) pozwala na dostęp do danych przeglądania (historii, zakładek itp.) na wszystkich Twoich urządzeniach bez potrzeby zakładania konta i chroni je za pomocą szyfrowania typu E2EE (end-to-end encryption).

## Cromite (Android)

<div class="admonition recommendation" markdown>

![Logo Cromite](assets/img/browsers/cromite.svg){ align=right }

**Cromite** to przeglądarka oparta na Chromium, oferująca wbudowane blokowanie reklam, ochronę przed odciskami palców oraz inne [ulepszenia w zakresie prywatności i bezpieczeństwa](https://github.com/uazo/cromite/blob/master/docs/FEATURES.md). Jest to fork porzuconej już przeglądarki **Bromite**.

[:octicons-home-16: Strona główna](https://cromite.org){ .md-button .md-button--primary }
[:octicons-eye-16:]
(https://github.com/uazo/cromite/blob/master/docs/PRIVACY_POLICY.md){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://github.com/uazo/cromite?tab=readme-ov-file#docs){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/uazo/cromite){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-android: F-Droid](https://cromite.org/fdroid/repo/?fingerprint=49F37E74DEE483DCA2B991334FB5A0200787430D0B5F9A783DD5F13695E9517B)
- [:simple-github: GitHub](https://github.com/uazo/cromite/releases/latest)

</details>

</div>

### Zalecana konfiguracja

Te opcje znajdziesz w :material-menu: → :gear: **Ustawienia** → **Prywatność i bezpieczeństwo**.

#### Browsing data (Dane przeglądania)

- [x] Zaznacz **Close all open tabs on exit**

#### Tryb incognito

- [x] Zaznacz **Open external links in incognito** (Otwieranie linków zewnętrznych w trybie incognito)

#### Bezpieczeństwo

- [x] Zaznacz **Zawsze używaj bezpiecznych połączeń** w sekcji o tej samej nazwie

Zapobiega to przypadkowemu łączeniu się ze stronami używającymi nieszyfrowanego protokołu HTTP. HTTP jest obecnie bardzo rzadko używany, więc ta opcja nie powinna mieć zauważalnego wpływu na codzienne przeglądanie Internetu.

#### Adblock Plus settings (Opcje Adblock Plus)

Te opcje znajdziesz w :material-menu: → :gear: **Ustawienia** → **Adblock Plus settings**.

Cromite zawiera zmodyfikowaną wersję Adblock Plus z domyślnie włączoną listą EasyList oraz możliwością wyboru dodatkowych list filtrów w menu **Filter lists** (Listy filtrów).

Korzystanie z dodatkowych list może sprawić, że będziesz się wyróżniać na tle innych użytkowników Cromite, a także zwiększyć ryzyko ataku, jeśli do którejś z list zostanie dodana złośliwa reguła.

- \[x\] (Opcjonalnie) Zaznacz **Enable anti-circumvention and snippets** (Włączenie ochrony przed obchodzeniem blokad i snippetów)

Ta opcja dodaje dodatkową listę Adblock Plus, która może zwiększyć skuteczność blokowania treści w Cromite. Nadal jednak obowiązują ostrzeżenia dotyczące wyróżniania się i potencjalnego zwiększenia powierzchni ataku.

#### Legacy Adblock settings (Starsze opcje Adblock)

Te opcje znajdziesz w :material-menu: → :gear: **Ustawienia** → **Legacy Adblock settings**.

- [ ] Odznacz opcję automatycznych aktualizacji

Wyłącza to sprawdzanie aktualizacji dla nieutrzymywanej już listy filtrów reklam z przeglądarki Bromite.

## Safari (iOS)

W systemie iOS każda aplikacja umożliwiająca przeglądanie Internetu jest [ograniczona](https://developer.apple.com/app-store/review/guidelines) do korzystania z udostępnionego przez Apple [frameworka WebKit](https://developer.apple.com/documentation/webkit). Oznacza to, że przeglądarka taka jak [Brave](#brave) nie korzysta z silnika Blink (rdzenia Chromium), jak jej odpowiedniki na innych systemach operacyjnych.

<div class="admonition recommendation" markdown>

![Logo Safari](assets/img/browsers/safari.svg){ align=right }

**Safari** jest domyślną przeglądarką w systemie iOS. Zawiera [funkcje prywatności](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios), takie jak [inteligentne zapobieganie śledzeniu](https://webkit.org/blog/7675/intelligent-tracking-prevention), izolowane i efemeryczne karty w trybie przeglądania prywatnego, ochrona przed odciskami palców (poprzez prezentowanie uproszczonej wersji konfiguracji systemu, co sprawia, że więcej urządzeń wygląda identycznie), losowa zmienność odcisków palców, a także usługę Przekazywanie prywatne dostępną dla subskrybentów iCloud+.

[:octicons-home-16: Strona główna](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/pl/safari){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title="Dokumentacja" }

</details>

</div>

### Zalecana konfiguracja przeglądarki Safari

Następujące opcje dotyczące prywatności i bezpieczeństwa znajdziesz w :gear: **Ustawienia** → **Aplikacje** → **Safari**.

#### Zezwalaj Safari na dostęp

W sekcji **Siri**:

- [ ] Disable **Learn from this App**
- [ ] Wyłącz **W aplikacji**
- [ ] Wyłącz **Na ekranie głównym**
- [ ] Wyłącz **Sugeruj aplikację**

To uniemożliwia Siri wykorzystywanie zawartości z Safari do generowania sugestii.

#### Wyszukiwarka

- [ ] Wyłącz **Sugestie wyszukiwarki**

Ta opcja powoduje, że wszystko, co wpisujesz w pasku adresu, jest wysyłane do wyszukiwarki ustawionej w Safari. Wyłączenie sugestii wyszukiwarki pozwala dokładniej kontrolować, jakie dane przekazujesz dostawcy wyszukiwarki.

#### Profile

Safari umożliwia oddzielenie przeglądania przy użyciu różnych profili. Wszystkie pliki cookie, historia oraz dane witryn są przechowywane osobno dla każdego profilu. Warto używać różnych profili do różnych celów, np. Osobisty, Praca czy Szkoła.

#### Prywatność i bezpieczeństwo

- [x] Włącz **Blokuj śledzenie poza witryną**

Ta opcja aktywuje [inteligentne zapobieganie śledzeniu (ITP)](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp) w silniku WebKit. Funkcja ta chroni przed niechcianym śledzeniem, wykorzystując lokalne uczenie maszynowe do blokowania trackerów. ITP zapewnia ochronę przed wieloma powszechnymi zagrożeniami, jednak nie eliminuje wszystkich metod śledzenia, ponieważ została zaprojektowana tak, by nie zakłócać działania stron internetowych.

- [x] Włącz **Wymagaj Face ID/Touch ID do odblokowywania przeglądania prywatnego**

Ta opcja pozwala zabezpieczyć karty w trybie przeglądania prywatnego za pomocą biometrii lub kodu PIN, gdy nie są używane.

- [ ] Wyłącz **Alerty o fałszywych witrynach**

Ta funkcja korzysta z usługi Bezpieczne przeglądanie Google (lub usługi Tencent Safe Browsing dla użytkowników z Chin kontynentalnych lub Hongkongu), aby chronić Cię podczas przeglądania. W efekcie Twój adres IP może być rejestrowany przez dostawcę usługi Bezpieczne przeglądanie. Wyłączenie tej funkcji uniemożliwi takie logowanie, ale jednocześnie zwiększy ryzyko wejścia na znane strony phishingowe.

- [x] Włącz **Ostrzeżenie o niezabezpieczonym połączeniu**

Ta opcja wyświetla ostrzeżenie, jeśli połączenie ze stroną nie jest szyfrowane przy użyciu protokołu HTTPS. Safari automatycznie spróbuje połączyć się z wersją HTTPS witryny, więc ostrzeżenie pojawi się tylko wtedy, gdy taka wersja nie jest dostępna.

- [ ] Wyłącz **Najważniejsze**

Zgodnie z polityką prywatności Apple dla Safari:

> Podczas odwiedzin w witrynie Safari może wysłać informacje uzyskane na podstawie jej adresu do Apple za pośrednictwem OHTTP w celu ustalenia, czy witryna zawiera istotne informacje do zaprezentowania.

#### Ustawienia dla witryn

W sekcji **Aparat**

- [x] Wybierz **Pytaj**

W sekcji **Mikrofon**

- [x] Wybierz **Pytaj**

W sekcji **Położenie**

- [x] Wybierz **Pytaj**

Te ustawienia sprawiają, że strony internetowe mogą uzyskać dostęp do aparatu, mikrofonu lub położenia (lokalizacji) dopiero po uzyskaniu Twojej wyraźnej zgody.

#### Inne ustawienia prywatności

Te opcje znajdziesz w :gear: **Ustawienia** → **Aplikacje** → **Safari** → **Zaawansowane**.

##### Fingerprinting Mitigations

The **Advanced Tracking and Fingerprinting Protection** setting will randomize certain values so that it's more difficult to fingerprint you:

- [x] Select **All Browsing** or **Private Browsing**

##### Miary dot. reklam zachowujące prywatność

- [ ] Wyłącz **Miary dot. reklam zachowujące prywatność**

Tradycyjne pomiary kliknięć reklamowych zwykle wykorzystują technologie śledzące, które naruszają prywatność użytkownika. [Miary dot. stuknięć zachowujące prywatność](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) (Private Click Measurement) to funkcja WebKit oraz proponowany standard sieciowy, mający umożliwić reklamodawcom pomiar skuteczności kampanii bez naruszania prywatności użytkowników.

Sama funkcja nie stanowi istotnego zagrożenia dla prywatności, jednak fakt, że jest automatycznie wyłączona w trybie prywatnego przeglądania, wskazuje, że warto ją wyłączyć również globalnie.

#### Zawsze włączony tryb przeglądania prywatnego

Otwórz Safari i stuknij przycisk Karty w prawym dolnym rogu. Następnie rozwiń listę grup kart :material-format-list-bulleted:.

- [x] Wybierz **Prywatne**

Tryb przeglądania prywatnego w przeglądarce Safari oferuje dodatkowe mechanizmy ochrony prywatności. Tryb ten korzysta z nowej sesji [efemerycznej](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) dla każdej karty, co oznacza, że karty są od siebie odizolowane. Istnieją też inne, drobniejsze korzyści w zakresie prywatności — np. w trybie przeglądania prywatnego Safari nie wysyła adresów stron do Apple przy korzystaniu z funkcji tłumaczenia.

Należy jednak pamiętać, że w trybie przeglądania prywatnego nie są zapisywane pliki cookie ani dane witryn, więc nie będzie możliwe pozostawanie zalogowanym na stronach — może to być pewną niedogodnością.

#### Synchronizacja iCloud

Synchronizacja historii Safari, grup kart, kart iCloud oraz zapisanych haseł jest chroniona szyfrowaniem E2EE. Jednak domyślnie zakładki [nie są](https://support.apple.com/HT202303) objęte tym zabezpieczeniem — Apple może je odszyfrować i uzyskać do nich dostęp zgodnie ze swoimi [Zasadami ochrony prywatności](https://apple.com/pl/legal/privacy/pl).

Możesz włączyć szyfrowanie E2EE dla zakładek i pobranych plików w Safari, aktywując funkcję [Zaawansowana ochrona danych](https://support.apple.com/HT212520). Przejdź do :gear: **Ustawienia** → **iCloud** → **Zaawansowana ochrona danych**.

- [x] Włącz **Zaawansowana ochrona danych**

Jeśli korzystasz z iCloud bez włączonej zaawansowanej ochrony danych, zaleca się ustawienie domyślnej lokalizacji pobierania w Safari na folder lokalny na Twoim urządzeniu. Opcję tę znajdziesz w :gear: **Ustawienia** → **Aplikacje** → **Safari** → **Ogólne** → **Pobrane**.

## Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

### Minimalne wymagania

- Musi obsługiwać automatyczne aktualizacje.
- Musi szybko otrzymywać aktualizacje silnika z wersji nadrzędnych (upstream).
- Musi obsługiwać blokowanie treści.
- Wszelkie zmiany mające na celu zwiększenie prywatności nie mogą pogarszać komfortu użytkowania.
