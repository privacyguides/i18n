---
title: Przegląd systemu Android
icon: simple/android
description: Android to system operacyjny typu open-source z silnymi zabezpieczeniami, dlatego jest naszym pierwszym wyborem na telefony.
robots: nofollow, max-snippet:-1, max-image-preview:large
---

![Android logo](../assets/img/android/android.svg){ align=right }

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

## Privacy Features

### User Profiles

Multiple **user profiles** can be found in :gear: **Settings** → **System** → **Users** and are the simplest way to isolate in Android.

With user profiles, you can impose restrictions on a specific profile, such as: making calls, using SMS, or installing apps. Each profile is encrypted using its own encryption key and cannot access the data of any other profiles. Even the device owner cannot view the data of other profiles without knowing their password. Multiple user profiles are a more secure method of isolation.

### Work Profile

[**Work Profiles**](https://support.google.com/work/android/answer/6191949) are another way to isolate individual apps and may be more convenient than separate user profiles.

A **device controller** app such as [Shelter](../android/general-apps.md#shelter) is required to create a Work Profile without an enterprise MDM, unless you're using a custom Android OS which includes one.

The work profile is dependent on a device controller to function. Features such as *File Shuttle* and *contact search blocking* or any kind of isolation features must be implemented by the controller. You must also fully trust the device controller app, as it has full access to your data inside the work profile.

This method is generally less secure than a secondary user profile; however, it does allow you the convenience of running apps in both the owner profile and work profile simultaneously.

### Private Space

**Private Space** is a feature introduced in Android 15 that adds another way of isolating individual apps. You can set up a private space in the owner profile by navigating to :gear: **Settings** → **Security & privacy** → **Private space**. Once set up, your private space resides at the bottom of the app drawer.

Like user profiles, a private space is encrypted using its own encryption key, and you have the option to set up a different unlock method. Like work profiles, you can use apps from both the owner profile and private space simultaneously. Apps launched from a private space are distinguished by an icon depicting a key within a shield.

Unlike work profiles, Private Space is a feature native to Android that does not require a third-party app to manage it. For this reason, we generally recommend using a private space over a work profile, though you can use a work profile alongside a private space.

### VPN kill switch

Android 7 and above supports a VPN kill switch, and it is available without the need to install third-party apps. This feature can prevent leaks if the VPN is disconnected. It can be found in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

### Global Toggles

Modern Android devices have global toggles for disabling Bluetooth and location services. Android 12 introduced toggles for the camera and microphone. When not in use, we recommend disabling these features. Apps cannot use disabled features (even if granted individual permissions) until re-enabled.

## Google Services

If you are using a device with Google services—whether with the stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS—there are a number of additional changes you can make to improve your privacy. We still recommend avoiding Google services entirely, or limiting Google Play Services to a specific user/work profile by combining a device controller like *Shelter* with GrapheneOS's Sandboxed Google Play.

### Advanced Protection Program

If you have a Google account we suggest enrolling in the [Advanced Protection Program](https://landing.google.com/advancedprotection). To umożliwi Ci otrzymywanie **niektórych** poprawek bezpieczeństwa od Google bez naruszania modelu zabezpieczeń Androida poprzez używanie systemu pochodnego od Androida i zwiększanie ryzyka na atak. Alternatively, you can use [passkeys](https://fidoalliance.org/passkeys).

The Advanced Protection Program provides enhanced threat monitoring and enables:

- Stricter two-factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](../basics/account-creation.md#sign-in-with-oauth)
- Only Google and verified third-party apps can access account data
- Scanning of incoming emails on Gmail accounts for [phishing](https://en.wikipedia.org/wiki/Phishing#Email_phishing) attempts
- Stricter [safe browser scanning](https://google.com/chrome/privacy/whitepaper.html#malware) with Google Chrome
- Stricter recovery process for accounts with lost credentials

 If you use non-sandboxed Google Play Services (common on stock operating systems), the Advanced Protection Program also comes with [additional benefits](https://support.google.com/accounts/answer/9764949) such as:

- Not allowing app installation outside the Google Play Store, the OS vendor's app store, or via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Mandatory automatic device scanning with [Play Protect](https://support.google.com/googleplay/answer/2812853?#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- Warning you about unverified applications
- Enabling ARM's hardware-based [Memory Tagging Extension (MTE)](https://developer.arm.com/documentation/108035/0100/Introduction-to-the-Memory-Tagging-Extension) for supported apps, which lowers the likelihood of device exploits happening through memory corruption bugs

### Aktualizacje systemowe Google Play

In the past, Android security updates had to be shipped by the operating system vendor. Android has become more modular beginning with Android 10, and Google can push security updates for **some** system components via the privileged Play Services.

If you have an EOL device shipped with Android 10 or above and are unable to run any of our recommended operating systems on your device, you are likely going to be better off sticking with your OEM Android installation (as opposed to an operating system not listed here such as LineageOS or /e/ OS). This will allow you to receive **some** security fixes from Google, while not violating the Android security model by using an insecure Android derivative and increasing your attack surface. We would still recommend upgrading to a supported device as soon as possible.

### Advertising ID

All devices with Google Play Services installed automatically generate an [advertising ID](https://support.google.com/googleplay/android-developer/answer/6048248) used for targeted advertising. Disable this feature to limit the data collected about you.

On Android distributions with [sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), go to :gear: **Settings** → **Apps** → **Sandboxed Google Play** → **Google Settings** → **All services** → **Ads**.

- [x] Select **Delete advertising ID**

On Android distributions with privileged Google Play Services (which includes the stock installation on most devices), the setting may be in one of several locations. Check

- :gear: **Settings** → **Google** → **Ads**
- :gear: **Settings** → **Privacy** → **Ads**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads* (this varies between OEM distributions of Android). If presented with the option to delete the advertising ID, that is preferred. If not, then make sure to opt out and reset your advertising ID.

### SafetyNet and Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) and the [Play Integrity APIs](https://developer.android.com/google/play/integrity) are generally used for [banking apps](https://grapheneos.org/usage#banking-apps). Many banking apps will work fine in GrapheneOS with sandboxed Play services, however some non-financial apps have their own crude anti-tampering mechanisms which might fail. GrapheneOS passes the `basicIntegrity` check, but not the certification check `ctsProfileMatch`. Devices with Android 8 or later have hardware attestation support which cannot be bypassed without leaked keys or serious vulnerabilities.

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt out if you don't want your credit rating and personal information shared with affiliate marketing services.
