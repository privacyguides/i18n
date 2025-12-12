---
title: "Pozyskiwanie aplikacji"
description: Poniższe zalecenia dotyczą sposobów pozyskiwania aplikacji na Androida bez korzystania z Usług Google Play.
---

Istnieje wiele sposobów na prywatne pozyskanie aplikacji na Androida — nawet ze Sklepu Play — bez kontaktu z Usługami Google Play. Poniższe zalecenia przedstawiają metody pozyskiwania aplikacji na Androida, uporządkowane według preferencji.

## Obtainium

<div class="admonition recommendation" markdown>

![Logo Obtainium](../assets/img/android/obtainium.svg){ align=right }

**Obtainium** to menedżer aplikacji, który pozwala instalować i aktualizować aplikacje bezpośrednio z oficjalnej strony wydań dewelopera (np. GitHub, GitLab, strona internetowa dewelopera itp.), zamiast ze scentralizowanego sklepu czy repozytorium. Obsługuje automatyczne aktualizacje w tle na Androidzie 12 i nowszych.

[:octicons-repo-16: Repozytorium](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ImranR98/Obtainium/wiki){ .card-link title=Dokumentacja}
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=Wesprzyj }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

Obtainium umożliwia pobieranie plików instalacyjnych APK z wielu źródeł, jednak musisz upewnić się, że te źródła i aplikacje są wiarygodne. Na przykład instalowanie komunikatora Signal z [oficjalnej strony Signal z plikiem APK](https://signal.org/android/apk) powinno być w porządku, natomiast instalowanie z repozytoriów stron trzecich, takich jak Aptoide czy APKPure, może wiązać się z dodatkowym ryzykiem. Ryzyko zainstalowania złośliwej _aktualizacji_ jest niższe, ponieważ sam Android przed instalacją weryfikuje, czy wszystkie aktualizacje aplikacji są podpisane przez tego samego dewelopera, co dotychczasowa wersja aplikacji na urządzeniu.

## GrapheneOS App Store

Sklep z aplikacjami GrapheneOS jest dostępny w serwisie [GitHub](https://github.com/GrapheneOS/Apps/releases). Obsługuje on Androida 12 i nowsze oraz może samodzielnie się aktualizować. W sklepie znajdują się samodzielne aplikacje stworzone przez projekt GrapheneOS, takie jak [Auditor](../device-integrity.md#auditor-android), [Camera](general-apps.md#secure-camera) i [PDF Viewer](general-apps.md#secure-pdf-viewer). Jeśli szukasz tych aplikacji, zalecamy pobranie ich ze sklepu z aplikacjami GrapheneOS zamiast ze sklepu Google Play, ponieważ aplikacje dostępne w sklepie GrapheneOS są podpisane ich własnym kluczem, do którego Google nie ma dostępu.

## Aurora Store

Sklep Google Play wymaga konta Google do zalogowania się, co nie sprzyja prywatności. Możesz to obejść, korzystając z alternatywnego klienta, takiego jak Aurora Store.

<div class="admonition recommendation" markdown>

![Logo Aurora Store](../assets/img/android/aurora-store.webp){ align=right }

**Aurora Store** to klient Sklepu Google Play, który nie wymaga konta Google, Usług Google Play ani microG do pobierania aplikacji.

[:octicons-home-16: Strona główna](https://auroraoss.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="Polityka prywatności" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

Aurora Store nie pozwala pobierać płatnych aplikacji przy użyciu funkcji anonimowego konta. Opcjonalnie można zalogować się w Aurora Store za pomocą swojego konta Google, aby pobrać zakupione wcześniej aplikacje — wtedy Google uzyska dostęp do listy zainstalowanych aplikacji. Nadal jednak zyskujesz na tym, że nie musisz instalować pełnego klienta Sklepu Google Play ani Usług Google Play czy microG na urządzeniu.

## Ręcznie za pomocą powiadomień RSS

Dla aplikacji wydawanych na platformach takich jak GitHub czy GitLab możesz dodać kanał RSS do swojego [agregatora wiadomości](../news-aggregators.md), co ułatwi śledzenie nowych wydań.

![Kanał RSS dla nowych wersji aplikacji w formacie APK](../assets/img/android/rss-apk-light.png#only-light) ![Kanał RSS dla nowych wersji aplikacji w formacie APK](../assets/img/android/rss-apk-dark.png#only-dark) ![Lista zmian w nowych wersjach aplikacji w formacie APK](../assets/img/android/rss-changes-light.png#only-light) ![Lista zmian w nowych wersjach aplikacji w formacie APK](../assets/img/android/rss-changes-dark.png#only-dark)

### GitHub

W serwisie GitHub — biorąc za przykład aplikację [Secure Camera](general-apps.md#secure-camera) — przejdź na [stronę z wydaniami](https://github.com/GrapheneOS/Camera/releases) i dopisz `.atom` do adresu URL:

`https://github.com/GrapheneOS/Camera/releases.atom`

### GitLab

W serwisie GitLab — biorąc za przykład aplikację [Aurora Store](#aurora-store) — przejdź do [repozytorium projektu](https://gitlab.com/AuroraOSS/AuroraStore) i dopisz `/-/tags?format=atom` do adresu URL:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

### Weryfikacja odcisków APK

Jeśli pobierasz pliki APK i instalujesz je ręcznie, warto zweryfikować ich podpis za pomocą narzędzia [`apksigner`](https://developer.android.com/studio/command-line/apksigner), które jest częścią pakietu Android [build-tools](https://developer.android.com/studio/releases/build-tools).

1. Zainstaluj [Java JDK](https://oracle.com/pl/java/technologies/downloads).

2. Pobierz [narzędzia wiersza poleceń Android Studio](https://developer.android.com/studio#command-tools).

3. Rozpakuj pobrane archiwum:

   ```bash
   unzip commandlinetools-*.zip
   cd cmdline-tools
   ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
   ```

4. Uruchom polecenie weryfikujące podpis:

   ```bash
   ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
   ```

5. Otrzymane skróty (hash) można porównać z innym źródłem. Niektórzy deweloperzy, np. Signal, [publikują odciski palców](https://signal.org/android/apk) na swojej stronie. Przykładowy wynik:

   ```bash
   Signer #1 certificate DN: CN=GrapheneOS
   Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
   Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
   Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
   ```

## F-Droid

![Logo F-Droid](../assets/img/android/f-droid.svg){ align=right width=120px }

\==Zalecamy korzystanie z F-Droid tylko jako sposób pozyskania aplikacji, których nie da się zdobyć za pomocą metod opisanych powyżej.== F-Droid bywa polecany jako alternatywa dla sklepu Google Play, zwłaszcza w środowisku dbającym o prywatność. Możliwość dodawania zewnętrznych repozytoriów i wyjścia poza zamknięty ekosystem Google przyczyniła się do jego popularności. F-Droid dodatkowo oferuje [powtarzalne kompilacje](https://f-droid.org/en/docs/Reproducible_Builds) (_reproducible builds_) dla niektórych aplikacji i jest nastawiony na wolne oprogramowanie typu open source. Jednak sposób, w jaki F-Droid buduje, podpisuje i dostarcza pakiety, ma też pewne wady związane z bezpieczeństwem:

Z powodu procesu kompilacji aplikacje z _oficjalnego_ repozytorium F-Droid często są opóźnione względem aktualizacji. Opiekunowie F-Droida ponadto ponownie wykorzystują identyfikatory pakietów, podpisując aplikacje własnymi kluczami, co nie jest idealnym rozwiązaniem, bo daje to zespołowi F-Droid absolutne zaufanie. Co więcej wymagania dotyczące aplikacji, które mają zostać uwzględnione w oficjalnym repozytorium F-Droid, są mniej rygorystyczne niż w innych sklepach z aplikacjami, np. w Google Play, przez co F-Droid ma tendencję do hostowania znacznie większej liczby aplikacji starszych, porzuconych lub takich, które nie spełniają już [nowoczesnych standardów bezpieczeństwa](https://developer.android.com/google/play/requirements/target-sdk).

Inne popularne zewnętrzne repozytoria F-Droid, takie jak [IzzyOnDroid](https://apt.izzysoft.de/fdroid), łagodzą część tych problemów. Repozytorium IzzyOnDroid pobiera kompilacje bezpośrednio ze źródeł (GitHub, GitLab itp.) i jest najbliższe korzystaniu z repozytoriów twórców. Oferuje też [powtarzalne kompilacje](https://android.izzysoft.de/articles/named/iod-rbs-mirrors-clients) dla setek aplikacji i ma osoby w zespole, które weryfikują powtarzalność plików APK podpisanych przez deweloperów. Ponadto zespół IzzyOnDroid przeprowadza [dodatkowe skany bezpieczeństwa](https://android.izzysoft.de/articles/named/iod-scan-apkchecks) aplikacji w repozytorium, co często prowadzi do [konsultacji](https://github.com/gouravkhunger/QuotesApp/issues/22) z deweloperami i poprawek zwiększających prywatność. Należy jednak pamiętać, że aplikacje mogą być usuwane z repozytorium IzzyOnDroid w [pewnych okolicznościach](https://gitlab.com/IzzyOnDroid/repo#are-apps-removed-from-the-repo--and-when-does-that-happen).

Repozytoria [F-Droid](https://f-droid.org/pl/packages) i [IzzyOnDroid](https://apt.izzysoft.de/fdroid) zawierają ogromną liczbę aplikacji, więc mogą być przydatne do wyszukiwania i odkrywania aplikacji typu open source, które następnie można pozyskać innymi sposobami, np. za pośrednictwem sklepu Google Play, Aurora Store lub bezpośrednio z repozytorium dewelopera. Należy zachować rozwagę przy wybieraniu nowych aplikacji i zwracać uwagę na częstotliwość ich aktualizacji. Przestarzałe aplikacje mogą polegać na nieobsługiwanych już bibliotekach i stwarzać ryzyko bezpieczeństwa.

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

W rzadkich przypadkach zdarza się, że twórca dystrybuuje aplikację wyłącznie za pośrednictwem F-Droid (przykładem jest aplikacja [Gadgetbridge](../health-and-wellness.md#gadgetbridge)). Jeśli naprawdę potrzebujesz takiej aplikacji, zalecamy skorzystanie z nowszego klienta [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) zamiast oryginalnej aplikacji F-Droid. F-Droid Basic obsługuje automatyczne aktualizacje w tle bez potrzeby rozszerzeń z uprawnieniami uprzywilejowanymi czy roota i ma ograniczony zestaw funkcji (co zmniejsza powierzchnię ataku).

</div>
