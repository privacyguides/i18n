---
meta_title: "Przeglądarki internetowe na Android/IOS szanujące prywatność - Privacy Guides"
title: Przeglądarki mobilne
icon: octicons/device-mobile-16
description: Obecnie zalecamy te przeglądarki do standardowego/nie anonimowego przeglądania internetu na swoim smartfonie.
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Rekomendowane Prywatne Przeglądarki Mobilne
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

- [:material-account-cash: Kapitalizm Nadzoru](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

To są obecnie zalecane przez nas **przeglądarki internetowe** oraz konfiguracje dla standardowego/nie anonimowego przeglądania internetu. Jeśli chcesz przeglądać Internet anonimowo, skorzystaj z sieci [Tor](tor.md).

## Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** zawiera wbudowany bloker treści i [funkcje prywatności](https://brave.com/privacy-features), z których większość jest włączona domyślnie.

Brave jest zbudowany na projekcie przeglądarki internetowej Chromium, 

[:octicons-home-16: Strona główna](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:]
(https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-fdroid: F-Droid](https://brave-browser-apk-release.s3.brave.com/fdroid/repo/index.html)

</details>

</div>

### Rekomendowana Konfiguracja Brave

Przeglądarka Tor to jedyny sposób aby na prawdę przeglądać internet anonimowo. Kiedy używasz Braver zalecamy zmianę następujących ustawień aby chronić twoją prywatność przed niektórymi stronami, ale wszystkie przeglądarki inne niż [Przeglądarka Tor](tor.md#tor-browser) będą możliwe do śledzenia przez *kogoś* w takim czy innym zakresie.

=== "Android"

    .

=== "iOS"

    Te opcje można znaleźć w :material-menu: → **Ustawienia** → **Tarcze & prywatność**.

####

Brave zawiera funkcje zapobiegające rozpoznawaniu urządzenia w sekcji [Tarcze](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Zalecamy skonfigurowanie tych ustawień [globalnie](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) pomiędzy wszystkimi stronami, które odwiedzasz.

Opcje Tarczy mogą być obniżane w zależności od potrzeb, ale domyślnie zalecamy ustawienie następujących opcji:

=== "Android"

    <div class="annotate" markdown>

    -
    - [x] Zaznacz **Automatyczne przekierowywanie stron AMP**
    - [x] Zaznacz **Automatycznie przekierowuj śledzące adresy URL**
    - [x] Zaznacz **Wymagaj, aby wszystkie połączenia używały HTTPS (ścisłe)** w *Aktualizacje HTTPS*
    - \[x\] (Opcjonalne) Zaznacz **Zablokuj skrypty**
    - [x] Zaznacz **Blokuj pliki cookie innych firm** w *Zablokuj pliki cookies</li>
    - [x] Zaznacz **Zablokuj rozpoznawanie urządzenia**
    - [x] Zaznacz **Zapobiegaj pobieraniu odcisków palców za pomocą ustawień językowych**

    <details class="warning" markdown>
    <summary>Używaj domyślnych list filtrów</summary>

    Brave pozwala wybrać dodatkowe filtry treści w menu **Filtrowanie Treści** lub bezpośrednio przez stronę `brave://adblock`. Nie zalecamy używania tej funkcji, zachowaj domyślne ustawienia list filtrów. Używanie dodatkowych list sprawi, że będziesz się wyróżniał na tle innych użytkowników i może zwiększyć ryzyko ataku powierzchniowego jeśli w Brave znajduje się exploit i złośliwa reguła zostanie dodana do jednej z list, których używasz.

    </details>

    - [x] Zaznacz **Zapomnij po zamknięciu strony**

    </div></ul>

    1. Ta opcja wyłącza JavaScript, co może wywołać nie poprawne działanie niektórych witryn. Aby je naprawić, możesz ustawić wyjątki dla poszczególnych witryn klikając na ikonę Tarczy na pasku adresu i odznaczając tą opcję w *Zaawansowane sterowanie*.

=== "iOS"

    <div class="annotate" markdown>

    - [x] Zaznacz **agresywnie** w *Zablokuj skrypty śledzące i reklamy*
    - [x] Zaznacz **ścisłe** w *Aktualizacje HTTPS*
    - [x] Zaznacz **Automatyczne przekierowywanie stron AMP**
    - [x] Zaznacz **Automatycznie przekierowuj śledzące adresy URL**
    - \[x\] (Opcjonalne) Zaznacz **Zablokuj skrypty**
    - [x] Zaznacz **Zablokuj rozpoznawanie urządzenia**
    - [x] Select **Site Tabs Closed** under *Auto Shred*

    <details class="warning" markdown>
    <summary>Używaj domyślnych list filtrów</summary>

    Brave pozwala na wybranie dodatkowych filtrów treści w menu **Filtrowanie Treści**. Odradzamy korzystanie z tej funkcji, zamiast tego zachowaj domyślne ustawienia listy filtrów. Korzystanie z dodatkowych list sprawi, że będziesz wyróżniać się na tle innych użytkowników Brave i również może zwiększyć powierzchnię ataku jeśli w Brave istnieje exploit i złośliwa reguła zostanie dodana do jednej z list, której używasz.

    </details>

    </div>

    1. Ta opcja wyłącza JavaScript,  Aby je naprawić, możesz ustawić wyjątki dla poszczególnych witryn klikając na ikonę Tarczy na pasku adresu i odznaczając tą opcję w *Zaawansowane sterowanie*.

##### Clear browsing data (Android only)

- [x] Select **Clear data on exit**

##### Social Media Blocking (Android only)

- [ ] Uncheck all social media components

#### Inne ustawienia prywatności

=== "Android"

    <div class="annotate" markdown>

    - [x] Zaznacz **Wyłącz UDP bez proxy** w [Zasady obsługi IP WebRTC IP</em>](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
    - \[x\] (Opcjonalne) Zaznacz **Brak ochrony** w *Bezpieczne przeglądanie*
    - [] Odznacz **Zezwalaj stronom internetowym na sprawdzanie, czy masz zapisane formy płatności**
    - [ ] Uncheck **Javascript optimization & security** under the setting with the same name
    - [x] Zaznacz **Zamknij karty przy wyjściu**
    - [] Odznacz **Zezwól na zastosowanie analizy produktów z zachowaniem prywatności (P3A)**
    - [] Odznacz **Automatycznie wysyłaj raporty diagnostyczne**
    - [] Odznacz **Automatycznie wysyłaj pingi dziennego użycia do Brave**

    </div>

    1. Brave's [implementation of Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) on Android **does not** proxy [Safe Browsing network requests](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) like its desktop counterpart. To oznacza, że twój adres IP może być widoczny (i rejestrowany) przez Google. Należy pamiętać, że Bezpieczne Przeglądanie nie jest dostępne na urządzeniach z Androidem bez Usług Google Play.

=== "iOS"

    - [] Odznacz **Zezwól na zastosowanie analizy produktów z zachowaniem prywatności (P3A)**
    - [] Odznacz **Automatycznie wysyłaj pingi dziennego użycia do Brave**

#### Leo

Te opcje można znaleźć w :material-menu: → **Ustawienia** → **Leo**

<div class="annotate" markdown>

- [] Odznacz **Pokaż sugestie automatycznego uzupełniania na pasku adresu**

</div>

1. Ta opcja jest nie dostępna w aplikacji Brave na IOS.

#### Wyszukiwarki

Te opcje można znaleźć w :material-menu:/:fontawesome-solid-ellipsis: → **Ustawienia** → **Wyszukiwarki**.

- [ ] Odznacz **Podpowiedzi wyszukiwania**

#### Synchronizacja

[Synchronizacja](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) umożliwia na dostęp do danych przeglądania (historia, zakładki, itd.) na wszystkich urządzeniach wymaganego konta i chroni je za pomocą E2EE.

## Cromite (Android)

<div class="admonition recommendation" markdown>

![Cromite logo](assets/img/browsers/cromite.svg){ align=right }

**Cromite** to przeglądarka oparta na Chromium z 
 wbudowanym blokowaniem reklam, ochroną przed rozpoznaniem urządzenia, i innymi [ulepszeniami prywatności i bezpieczeństwa]
(https://github.com/uazo/cromite/blob/master/docs/FEATURES.md).  To fork wycofanej przeglądarki **Bromite**.

[:octicons-home-16: Strona główna](https://cromite.org){ .md-button .md-button--primary }
[:octicons-eye-16:]
(https://github.com/uazo/cromite/blob/master/docs/PRIVACY_POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/uazo/cromite?tab=readme-ov-file#docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/uazo/cromite){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Pobieranie</summary>

- [:simple-android: F-Droid](https://cromite.org/fdroid/repo/?fingerprint=49F37E74DEE483DCA2B991334FB5A0200787430D0B5F9A783DD5F13695E9517B)
- [:simple-github: GitHub](https://github.com/uazo/cromite/releases/latest)

</details>

</div>

### Zalecana konfiguracja

Te opcje można znaleźć w  → :gear: **Ustawienia** → **Prywatność i bezpieczeństwo**.

#### Dane przeglądania

- [x] Zaznacz **Close all open tabs on exit**

#### Tryb Incognito

- [x] Zaznacz **Open external links in incognito**

#### Bezpieczeństwo

- [x] Zaznacz **Zawsze używaj bezpiecznych połączeń**

HTTP is extremely uncommon nowadays, so this should have little to no impact on your day-to-day browsing.

#### Adblock Plus settings

These options can be found in :material-menu: → :gear: **Settings** → **Adblock Plus settings**.

Cromite contains a customized version of Adblock Plus with EasyList enabled by default, as well as options to select more filter lists within the **Filter lists** menu.

Using extra lists will make you stand out from other Cromite users and may also increase attack surface if a malicious rule is added to one of the lists you use.

- \[x\] (Optional) Select **Enable anti-circumvention and snippets**

This setting adds an additional Adblock Plus list that may increase the effectiveness of Cromite's content blocking. The warnings about standing out and potentially increasing attack surface apply.

#### Legacy Adblock settings

These options can be found in :material-menu: → :gear: **Settings** → **Legacy Adblock settings**.

- [ ] Uncheck the autoupdate setting

This disables update checks for the unmaintained Bromite adblock filter.

## Safari (iOS)

On iOS, any app that can browse the web is [restricted](https://developer.apple.com/app-store/review/guidelines) to using an Apple-provided [WebKit framework](https://developer.apple.com/documentation/webkit), so a browser like [Brave](#brave) does not use the Blink engine (the core component of Chromium) like its counterparts on other operating systems.

<div class="admonition recommendation" markdown>

![Safari logo](assets/img/browsers/safari.svg){ align=right }

**Safari** is the default browser in iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites, so more devices look identical), and fingerprint randomization, as well as Private Relay for those with a paid iCloud+ subscription.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title="Documentation" }

</details>

</div>

### Recommended Safari Configuration

The following privacy/security-related options can be found in :gear: **Settings** → **Apps** → **Safari**.

#### Allow Safari to Access

Under **Siri**:

- [ ] Disable **Learn from this App**
- [ ] Disable **Show in App**
- [ ] Disable **Show on Home Screen**
- [ ] Disable **Suggest App**

This prevents Siri from using content from Safari for Siri suggestions.

#### Wyszukiwanie

- [ ] Disable **Search Engine Suggestions**

This setting sends whatever you type in the address bar to the search engine set in Safari. Wyłączenie podpowiedzi pozwala dokładniej kontrolować, jakie dane przekazujesz dostawcy wyszukiwarki.

#### Profiles

Safari allows you to separate your browsing with different profiles. All of your cookies, history, and website data are separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

#### Prywatność i bezpieczeństwo

- [x] Enable **Prevent Cross-Site Tracking**

This enables WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). The feature helps protect against unwanted tracking by using on-device machine learning to stop trackers. ITP protects against many common threats, but does not block all tracking avenues because it is designed to not interfere with website usability.

- [x] Enable **Require Face ID/Touch ID to Unlock Private Browsing**

This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

- [ ] Disable **Fraudulent Website Warning**

This setting uses Google Safe Browsing (or Tencent Safe Browsing for users in mainland China or Hong Kong) to protect you while you browse. As such, your IP address may be logged by your Safe Browsing provider. Disabling this setting will disable this logging, but you might be more vulnerable to known phishing sites.

- [x] Enable **Not Secure Connection Warning**

This setting shows a warning screen if your connection to a website isn't using HTTPS. Safari will automatically try to upgrade the site to HTTPS, so you should only see this when there is no HTTPS connection available.

- [ ] Disable **Highlights**

Apple's privacy policy for Safari states:

> When visiting a webpage, Safari may send information calculated from the webpage address to Apple over OHTTP to determine if relevant highlights are available.

#### Settings for Websites

Under **Camera**

- [x] Select **Ask**

Under **Microphone**

- [x] Select **Ask**

Under **Location**

- [x] Select **Ask**

These settings ensure that websites can only access your camera, microphone, or location after you explicitly grant them access.

#### Other Privacy Settings

These options can be found in :gear: **Settings** → **Apps** → **Safari** → **Advanced**.

##### Fingerprinting Mitigations

The **Advanced Tracking and Fingerprinting Protection** setting will randomize certain values so that it's more difficult to fingerprint you:

- [x] Select **All Browsing** or **Private Browsing**

##### Privacy Preserving Ad Measurement

- [ ] Disable **Privacy Preserving Ad Measurement**

Ad click measurement has traditionally used tracking technology that infringes on user privacy. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

The feature has little privacy concerns on its own, so while you can choose to leave it on, we consider the fact that it's automatically disabled in Private Browsing to be an indicator for disabling the feature.

#### Always-on Private Browsing

Open Safari and tap the Tabs button, located in the bottom right. Then, expand the :material-format-list-bulleted: Tab Groups list.

- [x] Select **Private**

Safari's Private Browsing mode offers additional privacy protections. Private Browsing uses a new [ephemeral](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) session for each tab, meaning tabs are isolated from one another. There are other smaller privacy benefits with Private Browsing too, such as not sending a webpage’s address to Apple when using Safari's translation feature.

Do note that Private Browsing does not save cookies and website data, so it won't be possible to remain signed in to sites. This may be an inconvenience.

#### iCloud Sync

Synchronization of Safari History, Tab Groups, iCloud Tabs and saved passwords are E2EE. However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://apple.com/legal/privacy/en-ww).

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/HT212520). Go to :gear: **Settings** → **iCloud** → **Advanced Data Protection**.

- [x] Turn on **Advanced Data Protection**

If you use iCloud with Advanced Data Protection disabled, we also recommend setting Safari's default download location to a local folder on your device. This option can be found in :gear: **Settings** → **Apps** → **Safari** → **General** → **Downloads**.

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

### Minimum Requirements

- Must support automatic updates.
- Must receive engine updates from upstream releases quickly.
- Must support content blocking.
- Any changes required to make the browser more privacy-respecting should not negatively impact user experience.
