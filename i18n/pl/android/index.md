---
title: "Android"
description: Nasze zalecenia dotyczące zastąpienia domyślnych, naruszających prywatność funkcji Androida prywatnymi i bezpiecznymi alternatywami.
icon: 'simple/android'
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Zalecenia dotyczące Androida
    url: "./"
  - "@context": http://schema.org
    "@type": CreativeWork
    name: Android
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://pl.wikipedia.org/wiki/Android_(system_operacyjny)
---

![Logo systemu Android](../assets/img/android/android.svg){ align=right }

**Projekt Android Open Source** (AOSP) to system operacyjny typu open source dla urządzeń mobilnych rozwijany przez Google, który napędza większość urządzeń mobilnych na świecie. Większość telefonów sprzedawanych z Androidem jest zmodyfikowana tak, by zawierała inwazyjne integracje i aplikacje, takie jak Usługi Google Play, dlatego możesz znacząco poprawić prywatność na swoim urządzeniu mobilnym, zastępując domyślną instalację telefonu wersją Androida pozbawioną tych inwazyjnych funkcji.

[Ogólny przegląd systemu Android] :material-arrow-right-drop-circle:](../os/android-overview.md){ .md-button .md-button--primary }

## Nasze zalecenia

### Zastąp usługi Google

Istnieje wiele sposobów na pozyskiwanie aplikacji na Androida bez korzystania z Google Play. Zawsze, gdy to możliwe, spróbuj skorzystać z jednego z tych sposobów, zanim pobierzesz aplikacje z nieprywatnych źródeł:

[Sposoby pozyskiwania aplikacji :material-arrow-right-drop-circle:](obtaining-apps.md){ .md-button }

Dostępnych jest także wiele prywatnych alternatyw dla aplikacji, które są domyślnie zainstalowane na Twoim telefonie, na przykład aplikacji aparatu. Oprócz aplikacji na Androida, które ogólnie zalecamy na całej stronie, przygotowaliśmy listę narzędzi systemowych specyficznych dla Androida, które mogą okazać się przydatne.

[Ogólne zalecenia dotyczące aplikacji :material-arrow-right-drop-circle:](general-apps.md){ .md-button }

### Zainstaluj niestandardową dystrybucję

Gdy kupujesz telefon z Androidem, domyślny system operacyjny jest dostarczany z aplikacjami i funkcjami, które nie są częścią Projektu Android Open Source. Wiele z tych aplikacji — nawet takich, które zapewniają podstawową funkcjonalność systemu, jak aplikacja do obsługi połączeń telefonicznych — wymaga inwazyjnych integracji z Usługami Google Play, które z kolei żądają uprawnień dostępu do plików, kontaktów, rejestru połączeń, wiadomości SMS, lokalizacji, aparatu, mikrofonu i wielu innych zasobów na urządzeniu, aby te podstawowe aplikacje systemowe i inne mogły w ogóle działać. Frameworki takie jak Usługi Google Play zwiększają powierzchnię ataku urządzenia i są źródłem różnych problemów prywatności związanych z Androidem.

Problem ten można rozwiązać, używając alternatywnej dystrybucji Androida, zwanej też jako _custom ROM_, która nie zawiera takich inwazyjnych integracji. Niestety wiele niestandardowych dystrybucji Androida często narusza model bezpieczeństwa Androida, nie obsługując krytycznych funkcji bezpieczeństwa, takich jak AVB, ochrona przed przywróceniem starszej wersji systemu (rollback protection), aktualizacje oprogramowania układowego i innych. Niektóre dystrybucje dostarczają też kompilacje [`userdebug`](https://source.android.com/setup/build/building#choose-a-target), które ujawniają uprawnienia root poprzez [ADB](https://developer.android.com/studio/command-line/adb) i wymagają [mniej restrykcyjnych] polityk SELinux, aby obsłużyć funkcje debugowania, co skutkuje dalszym zwiększeniem powierzchni ataku i osłabieniem modelu bezpieczeństwa.

Wybierając niestandardową dystrybucję Androida, warto upewnić się, że przestrzega ona modelu bezpieczeństwa Androida. Dystrybucja powinna oferować co najmniej kompilacje produkcyjne, obsługę AVB, ochronę przed przywróceniem starszej wersji systemu, terminowe aktualizacje oprogramowania układowego i systemu operacyjnego oraz SELinux w [trybie wymuszania](https://source.android.com/security/selinux/concepts#enforcement_levels). Wszystkie zalecane przez nas dystrybucje Androida spełniają te kryteria:

[Zalecane dystrybucje :material-arrow-right-drop-circle:](distributions.md){ .md-button }

### Unikaj roota

[Rootowanie](https://en.wikipedia.org/wiki/Rooting_\(Android\)) telefonu z Androidem może znacząco obniżyć bezpieczeństwo, osłabiając cały [model bezpieczeństwa Androida](https://en.wikipedia.org/wiki/Android_\(operating_system\)#Security_and_privacy). To z kolei może pogorszyć prywatność, jeśli pojawi się exploit wykorzystujący to osłabienie. Typowe metody rootowania polegają na bezpośredniej manipulacji partycją rozruchową, co uniemożliwia poprawne działanie Verified Boot. Aplikacje wymagające roota modyfikują też partycję systemową, więc Verified Boot musiałby pozostać wyłączony. Udostępnienie roota w interfejsie użytkownika zwiększa powierzchnię ataku urządzenia i może sprzyjać podatnościom umożliwiającym [eskalację uprawnień](https://en.wikipedia.org/wiki/Privilege_escalation) oraz obejścia polityk SELinux.

Blokery treści, które modyfikują [plik hosts](https://pl.wikipedia.org/wiki/Hosts) (np. AdAway) oraz zapory sieciowe wymagające stałego dostępu do roota (np. AFWall+) są niebezpieczne i nie powinny być używane. Nie są też właściwym sposobem rozwiązania problemów, do których są przeznaczone. W przypadku blokowania treści sugerujemy zaszyfrowany [DNS](../dns.md) lub funkcję blokowania treści oferowaną przez VPN. TrackerControl i AdAway w trybie bez roota zajmują gniazdo VPN (poprzez lokalną pętlę zwrotną VPN), uniemożliwiając korzystanie z usług zwiększających prywatność, takich jak [Orbot](../alternative-networks.md#orbot) czy [prawdziwa sieć VPN](../vpn.md).

AFWall+ działa w oparciu o podejście [filtrowania pakietów](https://en.wikipedia.org/wiki/Firewall_\(computing\)#Packet_filter) i może być w niektórych sytuacjach obejściem.

Uważamy, że poświęcenie bezpieczeństwa wynikające z rootowania telefonu nie jest warte wątpliwych korzyści w zakresie prywatności, które te aplikacje mogą oferować.

### Regularnie instaluj aktualizacje

It's important to not use an [end-of-life](https://endoflife.date/android) version of Android. Newer versions of Android receive not only security updates for the operating system but also important privacy enhancing updates too.

For example, [prior to Android 10](https://developer.android.com/about/versions/10/privacy/changes) any apps with the [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) permission could access sensitive and unique serial numbers of your phone such as [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), or your SIM card's [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity); whereas now they must be system apps to do so. System apps are only provided by the OEM or Android distribution.

### Use Built-in Sharing Features

You can avoid giving many apps permission to access your media with Android's built-in sharing features. Many applications allow you to "share" a file with them for media upload.

For example, if you want to post a picture to Discord you can open your file manager or gallery and share that picture with the Discord app, instead of granting Discord full access to your media and photos.
