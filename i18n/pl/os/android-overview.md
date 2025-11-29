---
title: Przegląd systemu Android
icon: simple/android
description: Android to system operacyjny typu open-source z silnymi zabezpieczeniami, dlatego jest naszym pierwszym wyborem na telefony.
robots: nofollow, max-snippet:-1, max-image-preview:large
---

![Logo systemu Android](../assets/img/android/android.svg){ align=right }

**Projekt Android Open Source** to bezpieczny system operacyjny dla urządzeń mobilnych, oferujący zaawansowaną [izolację aplikacji](https://source.android.com/security/app-sandbox) (tzw. piaskownicę aplikacji), [Verified Boot](https://source.android.com/security/verifiedboot) (AVB) oraz rozbudowany [system uprawnień](https://developer.android.com/guide/topics/permissions/overview).

[:octicons-home-16:](https://source.android.com){ .card-link title=Strona główna }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Dokumentacja}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/main){ .card-link title="Kod źródłowy" }

[Nasze zalecenia dotyczące Androida :material-arrow-right-drop-circle:](../android/index.md ""){.md-button.md-button--primary}

## Mechanizmy zabezpieczeń

Kluczowe elementy modelu bezpieczeństwa Androida obejmują proces [Verified Boot](#verified-boot), [aktualizacje oprogramowania układowego](#firmware-updates) oraz rozbudowany [system uprawnień](#android-permissions). Te istotne funkcje bezpieczeństwa stanowią podstawę minimalnych kryteriów dla naszych zaleceń dotyczących [telefonów komórkowych](../mobile-phones.md) i [niestandardowych dystrybucji Androida](../android/distributions.md).

### Verified Boot

[**Verified Boot**](https://source.android.com/security/verifiedboot) jest ważnym elementem modelu bezpieczeństwa Androida. Zapewnia ochronę przed atakami typu [evil maid](https://en.wikipedia.org/wiki/Evil_maid_attack), przed trwałym utrzymaniem złośliwego oprogramowania oraz gwarantuje, że aktualizacje zabezpieczeń nie mogą zostać cofnięte dzięki [ochronie przed cofnięciem (rollback protection)](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection).

Android 10 i nowsze przeszły od szyfrowania całego dysku do bardziej elastycznego [szyfrowania opartego na plikach](https://source.android.com/security/encryption/file-based). Twoje dane są szyfrowane za pomocą unikatowych kluczy, natomiast pliki systemu operacyjnego pozostają nieszyfrowane.

Verified Boot zapewnia integralność plików systemu operacyjnego, uniemożliwiając osobie z fizycznym dostępem do urządzenia modyfikowanie lub instalowanie złośliwego oprogramowania. W mało prawdopodobnym przypadku, gdy złośliwe oprogramowanie wykorzysta inne części systemu i uzyska wyższe uprawnienia, Verified Boot powstrzyma i cofnie zmiany w partycji systemowej po ponownym uruchomieniu urządzenia.

Niestety producenci OEM są zobowiązani do obsługi Verified Boot tylko w swojej standardowej dystrybucji Androida. Tylko kilku producentów, takich jak Google, obsługuje rejestrację niestandardowych kluczy AVB na swoich urządzeniach. Ponadto niektóre pochodne AOSP, takie jak LineageOS czy /e/OS, nie obsługują Verified Boot nawet na sprzęcie, który technicznie wspiera Verified Boot dla systemów firm trzecich. Zalecamy sprawdzenie wsparcia **przed** zakupem nowego urządzenia. Pochodne AOSP, które nie obsługują Verified Boot, **nie są** zalecane.

Wielu producentów ma też wadliwą implementację Verified Boot, o czym warto wiedzieć poza ich materiałami marketingowymi. Na przykład Fairphone 3 i 4 nie są domyślnie bezpieczne, ponieważ [standardowy bootloader ufa publicznemu kluczowi podpisu AVB](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). Powoduje to przerwanie Verified Boot na oryginalnym urządzeniu Fairphone, ponieważ system uruchomi alternatywne systemy Android (takie jak /e/) [bez żadnego ostrzeżenia](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) o użyciu niestandardowego systemu operacyjnego.

### Aktualizacje oprogramowania układowego

**Aktualizacje oprogramowania układowego** są kluczowe dla utrzymania bezpieczeństwa — bez nich urządzenie nie może być bezpieczne. Producenci OEM zawierają umowy z partnerami na dostarczanie zamkniętych komponentów przez ograniczony okres wsparcia. [Qualcomm](https://www.qualcomm.com/news/releases/2020/12/16/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) oraz [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox/) oferując wsparcie dla swoich urządzeń przez 4 lata, podczas gdy tańsze produkty często mają krótszy okres wsparcia.

Ponieważ elementy telefonu, takie jak procesor i technologie radiowe, opierają się na zamkniętym oprogramowaniu, aktualizacje muszą być dostarczane przez odpowiednich producentów podzespołów. Dlatego ważne jest, żeby kupić urządzenie objęte aktywnym cyklem wsparcia. [Qualcomm](https://qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) i [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox) zapewniają wsparcie dla swoich urządzeń przez 4 lata, podczas gdy tańsze produkty często mają krótsze cykle wsparcia. Wraz z wprowadzeniem serii [Pixel 6](https://support.google.com/pixelphone/answer/4457705) Google produkuje teraz własne układy i oferuje co najmniej 5 lat wsparcia. Wraz z wprowadzeniem serii Pixel 8 Google wydłużyło ten okres wsparcia do 7 lat.

Urządzenia oznaczone jako EOL, które nie są już wspierane przez producenta SoC, nie mogą otrzymywać aktualizacji oprogramowania układowego od producentów OEM ani od zewnętrznych dystrybutorów systemu Android. Oznacza to, że luki bezpieczeństwa w takich urządzeniach pozostaną niezałatane.

Fairphone na przykład reklamuje model Fairphone 4 jako objęty 6-letnim wsparciem. Jednak SoC (Qualcomm Snapdragon 750G w Fairphone 4) ma znacznie krótszą datę zakończenia wsparcia. Oznacza to, że aktualizacje zabezpieczeń oprogramowania układowego od Qualcomm dla Fairphone 4 zakończyły się we wrześniu 2023 r., niezależnie od tego, czy Fairphone będzie nadal wydawać aktualizacje zabezpieczeń oprogramowania.

### Uprawnienia Androida

[**Uprawnienia w Androidzie**](https://developer.android.com/guide/topics/permissions/overview) dają Ci kontrolę nad tym, do czego aplikacje mają dostęp. Google regularnie wprowadza [ulepszenia](https://developer.android.com/about/versions/11/privacy/permissions) systemu uprawnień w każdej kolejnej wersji. Wszystkie instalowane przez Ciebie aplikacje są ściśle [izolowane](https://source.android.com/security/app-sandbox) (w piaskownicy), więc nie ma potrzeby instalowania żadnych aplikacji antywirusowych.

Smartfon z najnowszą wersją Androida będzie zawsze bezpieczniejszy niż stary smartfon z zakupionym antywirusem. Lepiej nie płacić za oprogramowanie antywirusowe i odłożyć pieniądze na zakup nowego smartfona, takiego jak [Google Pixel](../mobile-phones.md#google-pixel).

Android 10:

- [Scoped Storage](https://developer.android.com/about/versions/10/privacy/changes#scoped-storage) zapewnia większą kontrolę nad plikami i może ograniczać to, co może [uzyskać dostęp do pamięci zewnętrznej](https://developer.android.com/training/data-storage#permissions). Aplikacje mogą mieć określony katalog w pamięci zewnętrznej oraz możliwość zapisywania tam określonych typów multimediów.
- Zaostrzone uprawnienia do [lokalizacji urządzenia](https://developer.android.com/about/versions/10/privacy/changes#app-access-device-location) poprzez wprowadzenie uprawnienia `ACCESS_BACKGROUND_LOCATION`. Zapobiega to dostępowi aplikacji do lokalizacji podczas działania w tle bez wyraźnej zgody użytkownika.

Android 11:

- [Uprawnienia jednorazowe](https://developer.android.com/about/versions/11/privacy/permissions#one-time), które pozwalają przyznać aplikacji dostęp tylko na jedną sesję.
- [Automatyczne resetowanie uprawnień](https://developer.android.com/about/versions/11/privacy/permissions#auto-reset), które cofa [uprawnienia uruchomieniowe](https://developer.android.com/guide/topics/permissions/overview#runtime) przyznane podczas otwierania aplikacji.
- Drobniejsze uprawnienia dotyczące funkcji związanych z [numerami telefonów](https://developer.android.com/about/versions/11/privacy/permissions#phone-numbers).

Android 12:

- Uprawnienie umożliwiające przyznanie jedynie [przybliżonej lokalizacji](https://developer.android.com/about/versions/12/behavior-changes-12#approximate-location).
- Automatyczne resetowanie uprawnień dla [uśpionych aplikacji](https://developer.android.com/about/versions/12/behavior-changes-12#app-hibernation).
- Interfejs [Data Access Auditing](https://developer.android.com/about/versions/12/behavior-changes-12#data-access-auditing), który ułatwia ustalenie, która część aplikacji wykonuje określony rodzaj dostępu do danych.

Android 13:

- Uprawnienie do [dostępu do pobliskich urządzeń Wi-Fi](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). Adresy MAC pobliskich punktów dostępowych Wi-Fi były popularnym sposobem śledzenia lokalizacji użytkownika przez aplikacje.
- Bardziej [szczegółowe uprawnienia do multimediów](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions), co pozwala przyznać dostęp tylko do obrazów, tylko do obrazów, filmów lub plików audio.
- Użycie czujników w tle wymaga teraz uprawnienia [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission).

Aplikacja może poprosić o uprawnienia dla konkretnej funkcji, którą oferuje. Na przykład każda aplikacja skanująca kody QR będzie wymagać uprawnienia do kamery. Niektóre aplikacje mogą żądać więcej uprawnień, niż faktycznie potrzebują.

[Exodus](https://exodus-privacy.eu.org) może być pomocny przy porównywaniu aplikacji o podobnym przeznaczeniu. Jeśli dana aplikacja wymaga wielu uprawnień i zawiera dużo reklam oraz bibliotek analitycznych, jest to prawdopodobnie zły znak. Zalecamy przyjrzeć się poszczególnym trackerom i przeczytać ich opisy, zamiast po prostu **zliczać ich sumę** i zakładać, że wszystkie pozycje mają równą wagę.

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

Jeżeli aplikacja jest w dużej mierze usługą internetową, śledzenie może odbywać się po stronie serwera. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest) pokazuje „brak trackerów”, ale z pewnością śledzi zainteresowania i zachowanie użytkowników w obrębie serwisu. Aplikacje mogą unikać wykrycia, nie korzystając ze standardowych bibliotek reklamowych, choć jest to mało prawdopodobne.

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Uwaga</p>

Aplikacje przyjazne prywatności, takie jak [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest), mogą pokazać niektóre trackery, np. [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49). Biblioteka ta obejmuje [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging), które umożliwia dostarczać [powiadomienia push](https://en.wikipedia.org/wiki/Push_technology) w aplikacjach. To właśnie ma miejsce [w przypadku Bitwardena](https://fosstodon.org/@bitwarden/109636825700482007). Nie oznacza to jednak, że Bitwarden wykorzystuje wszystkie funkcje analityczne oferowane przez Google Firebase Analytics.

</div>

## Funkcje prywatności

### Profile użytkowników

Wiele **profilów użytkowników** znajduje się w :gear: **Ustawienia** → **System** → **Użytkownicy** i stanowią najprostszy sposób izolowania na Androidzie.

Dzięki profilom użytkowników możesz nałożyć ograniczenia na konkretny profil, np. dotyczące wykonywania połączeń, używania SMS-ów czy instalowania aplikacji. Każdy profil jest szyfrowany przy użyciu własnego klucza szyfrowania i nie może uzyskać dostępu do danych innych profili. Nawet właściciel urządzenia nie może przeglądać danych innych profili bez znajomości ich hasła. Wiele profili użytkowników to bezpieczniejsza metoda izolacji.

### Profil służbowy

[**Profile służbowe**](https://support.google.com/work/android/answer/6191949) to inny sposób izolowania poszczególnych aplikacji i może być wygodniejszy niż oddzielne profile użytkowników.

Do utworzenia profilu służbowego bez rozwiązania MDM w przedsiębiorstwie wymagane jest zainstalowanie aplikacji **kontrolera urządzenia**, takiej jak [Shelter](../android/general-apps.md#shelter), chyba że używany jest niestandardowy system Android, który taką funkcję zawiera.

Profil służbowy działa przy wsparciu kontrolera urządzenia. Funkcje takie jak *File Shuttle* oraz *blokowanie wyszukiwania kontaktów* lub dowolne funkcje izolacji muszą być zaimplementowane przez kontroler. Należy w pełni ufać aplikacji kontrolera urządzenia, ponieważ ma ona pełny dostęp do danych znajdujących się w profilu służbowym.

Ta metoda jest zazwyczaj mniej bezpieczna niż dodatkowy profil użytkownika; pozwala jednak na wygodę uruchamiania aplikacji jednocześnie w profilu właściciela i profilu służbowym.

### Przestrzeń prywatna

**Przestrzeń prywatna** to funkcja wprowadzona w Androidzie 15, dodająca kolejny sposób izolowania poszczególnych aplikacji. Przestrzeń prywatną można skonfigurować w profilu właściciela, przechodząc do :gear: **Ustawienia** → **Bezpieczeństwo i prywatność** → **Przestrzeń prywatna**. Po skonfigurowaniu Twoja przestrzeń prywatna znajduje się u dołu szuflady aplikacji.

Podobnie jak profile użytkowników, przestrzeń prywatna jest szyfrowana przy użyciu własnego klucza szyfrowania i daje możliwość ustawienia innej metody odblokowywania. Podobnie jak profile służbowe, można korzystać z aplikacji jednocześnie w profilu właściciela i przestrzeni prywatnej. Aplikacje uruchomione w przestrzeni prywatnej wyróżnia się ikoną przedstawiającą klucz w tarczy.

W odróżnieniu od profili służbowych, przestrzeń prywatna jest natywną funkcją Androida i nie wymaga aplikacji firm trzecich do zarządzania nią. Z tego powodu zazwyczaj zalecamy korzystanie z przestrzeni prywatnej zamiast profilu służbowego, choć można używać profilu służbowego równolegle z przestrzenią prywatną.

### Funkcja VPN kill switch

Android 7 i nowszy obsługuje kill switch VPN, dostępny bez konieczności instalowania aplikacji firm trzecich. Funkcja ta może zapobiegać wyciekom danych, gdy VPN zostanie rozłączony. Można ją znaleźć w :gear: **Ustawienia** → **Sieć i internet** → **VPN** → :gear: → **Blokuj połączenia bez VPN**.

### Globalne przełączniki

Nowoczesne urządzenia z Androidem mają globalne przełączniki do wyłączania Bluetooth i usług lokalizacyjnych. Android 12 wprowadził przełączniki dla aparatu i mikrofonu. Zalecamy wyłączać te funkcje, gdy nie są używane. Aplikacje nie mogą korzystać z wyłączonych funkcji (nawet jeśli mają przyznane indywidualne uprawnienia) do czasu ich ponownego włączenia.

## Usługi Google

Jeśli używasz urządzenia z usługami Google — czy to na standardowej dystrybucji systemu, czy na systemie, który bezpiecznie izoluje Usługi Google Play, takim jak GrapheneOS — możesz wprowadzić dodatkowe zmiany poprawiające Twoją prywatność. Nadal zalecamy całkowite unikanie usług Google albo ograniczenie Usług Google Play do konkretnego profilu użytkownika/profilu służbowego, łącząc aplikację kontrolera urządzenia, taką jak *Shelter*, z izolowaną aplikacją Google Play w GrapheneOS.

### Program ochrony zaawansowanej

Jeśli masz konto Google, zalecamy zapisanie się do [Programu ochrony zaawansowanej](https://landing.google.com/advancedprotection). Program jest dostępny bezpłatnie dla osób posiadających dwa lub więcej fizycznych kluczy bezpieczeństwa z obsługą [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online). Alternatywnie można użyć [kluczy dostępu](https://fidoalliance.org/passkeys).

Program ochrony zaawansowanej zapewnia wzmocnione monitorowanie zagrożeń i umożliwia:

- Zaostrzone uwierzytelnianie dwuskładnikowe; np. obowiązek stosowania [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) oraz wyłączenie użycia [SMS OTP](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) i [OAuth](../basics/account-creation.md#sign-in-with-oauth).
- Dostęp do danych konta mają tylko Google i zweryfikowane aplikacje firm trzecich.
- Skanowanie przychodzących wiadomości e-mail na kontach Gmail w poszukiwaniu prób [phishingu](https://en.wikipedia.org/wiki/Phishing#Email_phishing).
- Surowsze [skanowanie bezpieczeństwa przeglądarki](https://google.com/chrome/privacy/whitepaper.html#malware) w Google Chrome.
- Zaostrzony proces odzyskiwania konta w przypadku utraty danych uwierzytelniających.

 Jeśli korzystasz z nieizolowanych Usług Google Play (co jest powszechne w standardowych systemach Android), Program ochrony zaawansowanej oferuje [dodatkowe korzyści](https://support.google.com/accounts/answer/9764949), takie jak:

- Brak możliwości instalowania aplikacji spoza Sklepu Google Play, sklepu dostawcy systemu lub przez [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge).
- Wymuszone automatyczne skanowanie urządzenia za pomocą [Play Protect](https://support.google.com/googleplay/answer/2812853?#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work).
- Ostrzeganie o niezweryfikowanych aplikacjach.
- Włączenie opartej na sprzęcie funkcji ARM — [Memory Tagging Extension (MTE)](https://developer.arm.com/documentation/108035/0100/Introduction-to-the-Memory-Tagging-Extension) — dla obsługiwanych aplikacji, co zmniejsza prawdopodobieństwo wykorzystania błędów związanych z uszkodzeniem pamięci.

### Aktualizacje systemowe Google Play

W przeszłości aktualizacje bezpieczeństwa Androida musiały być dostarczane przez dostawcę systemu operacyjnego. Od Androida 10 system stał się bardziej modułowy i Google może przekazywać aktualizacje bezpieczeństwa dla **niektórych** komponentów systemowych za pośrednictwem uprzywilejowanych Usług Google Play.

Jeżeli posiadasz urządzenie EOL dostarczone z Androidem 10 lub nowszym i nie możesz uruchomić żadnego z naszych zalecanych systemów operacyjnych na swoim urządzeniu, prawdopodobnie korzystniej będzie pozostać przy standardowej instalacji OEM Androida (zamiast używania nieujętego tutaj systemu, takiego jak LineageOS czy /e/OS). Pozwoli to otrzymywać **pewne** poprawki bezpieczeństwa od Google, jednocześnie nie naruszając modelu bezpieczeństwa Androida przez użycie niebezpiecznej pochodnej i nie zwiększając powierzchni ataku. Mimo wszystko nadal zalecamy jak najszybszą wymianę na urządzenie objęte wsparciem.

### Identyfikator reklamowy

Wszystkie urządzenia z zainstalowanymi Usługami Google Play automatycznie generują [identyfikator reklamowy](https://support.google.com/googleplay/android-developer/answer/6048248) wykorzystywany do reklam spersonalizowanych. Wyłącz tę funkcję, aby ograniczyć zbierane o Tobie dane.

W dystrybucjach Androida z [izolowaną aplikacją Google Play](https://grapheneos.org/usage#sandboxed-google-play) przejdź do :gear: **Ustawienia** → **Aplikacje** → **Sandboxed Google Play** → **Ustawienia Google** → **Wszystkie usługi** → **Reklamy**.

- [x] Zaznacz **Delete advertising ID** (Usuń identyfikator reklamowy)

W dystrybucjach Androida z uprzywilejowanymi Usługami Google Play (co obejmuje standardową instalację na większości urządzeń) ustawienie to może znajdować się w innym miejscu. Sprawdź tu:

- :gear: **Ustawienia** → **Google** → **Reklamy**
- :gear: **Ustawienia** → **Prywatność** → **Reklamy**

Zostanie Ci przedstawiona opcja usunięcia identyfikatora reklamowego lub *rezygnacji z reklam opartych na zainteresowaniach* (zależy to od dystrybucji OEM Androida). Jeśli dostępna jest opcja usunięcia identyfikatora reklamowego — jest to preferowane rozwiązanie. Jeśli nie, upewnij się, że dokonasz rezygnacji i zresetowania swojego identyfikatora reklamowego.

### SafetyNet i Play Integrity API

Interfejsy [SafetyNet](https://developer.android.com/training/safetynet/attestation) i [Play Integrity API](https://developer.android.com/google/play/integrity) są zazwyczaj używane przez [aplikacje bankowe](https://grapheneos.org/usage#banking-apps). Wiele aplikacji bankowych działa poprawnie w systemie GrapheneOS z izolowanymi usługami Google Play, jednak niektóre aplikacje niebankowe stosują własne, prymitywne mechanizmy antymanipulacyjne, które mogą zawodzić. GrapheneOS passes the `basicIntegrity` check, but not the certification check `ctsProfileMatch`. Devices with Android 8 or later have hardware attestation support which cannot be bypassed without leaked keys or serious vulnerabilities.

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt out if you don't want your credit rating and personal information shared with affiliate marketing services.
