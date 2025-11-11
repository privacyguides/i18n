---
meta_title: "Przeglądarka Tor Browser i sieć Tor: anonimowe przeglądanie Internetu – Privacy Guides"
title: "Tor Browser"
icon: simple/torbrowser
description: Chroń swoje przeglądanie Internetu przed ciekawskimi oczami, korzystając z sieci Tor — bezpiecznej sieci omijającej cenzurę.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org/pl
    sameAs: https://pl.wikipedia.org/wiki/Tor_(sieć_anonimowa)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-account-cash: Kapitalizm inwigilacji](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: Masowa inwigilacja](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Cenzura](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

**Tor** to sieć serwerów prowadzonych przez wolontariuszy, która pozwala na bezpłatne połączenie i zwiększenie prywatności oraz bezpieczeństwa w Internecie. Osoby fizyczne i organizacje mogą również wymieniać się informacjami w sieci Tor za pomocą „ukrytych usług .onion”, nie narażając swojej prywatności. Dzięki temu, że ruch w sieci Tor jest trudny do zablokowania i namierzenia, Tor stanowi skuteczne narzędzie do omijania cenzury.

[Szczegółowy przegląd sieci Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: Film: Dlaczego warto korzystać z sieci Tor?](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Porada</p>

Przed połączeniem się z siecią Tor zapoznaj się z naszym [przeglądem](advanced/tor-overview.md), wyjaśniającym czym jest Tor i jak bezpiecznie z niego korzystać. Często zalecamy łączenie się z Tor za pośrednictwem zaufanego [dostawcy VPN](vpn.md), ale należy zrobić to **prawidłowo**, aby nie obniżyć poziomu swojej anonimowości.

</div>

Istnieje kilka sposobów połączenia się z siecią Tor z urządzenia, z których najczęściej używaną jest przeglądarka **Tor Browser** — fork Firefoksa stworzony z myślą o [:material-incognito: anonimowym](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} przeglądaniu Internetu na komputerach stacjonarnych i Androidzie.

Niektóre aplikacje sprawdzają się lepiej niż inne; wybór zależy od Twojego modelu zagrożeń. Jeśli jesteś okazjonalnym użytkownikiem sieci Tor i nie obawiasz się, że Twój dostawca Internetu będzie gromadził dowody przeciwko Tobie, korzystanie z przeglądarek mobilnych, takich jak [Onion Browser](#onion-browser-ios), aby połączyć się z siecią Tor, jest w porządku. Zwiększenie liczby osób korzystających z sieci Tor na co dzień pomaga zmniejszyć negatywny stereotyp tej sieci i obniża wartość „list użytkowników Tor”, które mogą tworzyć ISP lub rządy.

Jeżeli w Twojej sytuacji pełna anonimowość jest kluczowa, zalecamy **wyłącznie** korzystanie z klienta desktopowego Tor Browser, najlepiej w konfiguracji [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os). Przeglądarki mobilne są mniej popularne w sieci Tor (i w rezultacie łatwiejsze do zidentyfikowania), a inne konfiguracje nie są tak gruntownie testowane pod kątem deanonimizacji.

## Tor Browser

<div class="admonition recommendation" markdown>

![Logo Tor Browser](assets/img/browsers/tor.svg){ align=right }

**Tor Browser** to najlepszy wybór, jeśli potrzebujesz anonimowości — zapewnia dostęp do sieci Tor i mostków, a także zawiera domyślne ustawienia i rozszerzenia automatycznie skonfigurowane w zależności od poziomu bezpieczeństwa: *standardowy*, *bezpieczniejszy* i *najbezpieczniejszy*.

[:octicons-home-16: Strona główna](https://torproject.org/pl){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Usługa onion" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title="Wspomóż projekt" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/pl/download/#android)
- [:fontawesome-brands-windows: Windows](https://torproject.org/pl/download)
- [:simple-apple: macOS](https://torproject.org/pl/download)
- [:simple-linux: Linux](https://torproject.org/pl/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Zagrożenie</p>

**Nigdy** nie instaluj żadnych dodatkowych rozszerzeń w przeglądarce Tor Browser ani nie modyfikuj ustawień w `about:config`, nawet tych, które zalecamy w przypadku Firefoksa. Dodatkowe rozszerzenia i niestandardowe ustawienia sprawiają, że wyróżniasz się spośród innych użytkowników sieci Tor, co ułatwia [identyfikację](https://support.torproject.org/glossary/browser-fingerprinting) Twojej przeglądarki.

</div>

Przeglądarka Tor Browser została zaprojektowana tak, by zapobiegać fingerprintingowi, czyli identyfikacji użytkownika na podstawie konfiguracji jego przeglądarki. Z tego powodu **nie należy** wprowadzać żadnych zmian w przeglądarce poza wybraniem domyślnych [poziomów bezpieczeństwa](https://tb-manual.torproject.org/security-settings). Po każdej zmianie poziomu bezpieczeństwa **koniecznie** należy ponownie uruchomić przeglądarkę przed dalszym korzystaniem. W przeciwnym razie [ustawienia bezpieczeństwa mogą nie zostać w pełni zastosowane](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), co zwiększa ryzyko identyfikacji lub wykorzystania luk, mimo że wybrany poziom ochrony może sugerować coś innego.

Oprócz instalacji przeglądarki Tor Browser bezpośrednio na komputerze, istnieją również systemy operacyjne zaprojektowane specjalnie do korzystania z sieci Tor, takie jak [Whonix](desktop.md#whonix) działający w środowisku [Qubes OS](desktop.md#qubes-os). Oferują one jeszcze wyższy poziom bezpieczeństwa i ochrony niż sam Tor Browser.

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Logo Onion Browser](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** to przeglądarka typu open source umożliwiająca anonimowe przeglądanie Internetu poprzez sieć Tor na urządzeniach z systemem iOS. Projekt jest oficjalnie wspierany przez [Tor Project](https://support.torproject.org/glossary/onion-browser).

[:material-star-box: Przeczytaj naszą ostatnią recenzję przeglądarki Onion Browser.](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review)

[:octicons-home-16: Strona główna](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title="Wspomóż projekt" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser nie zapewnia takiego samego poziomu ochrony prywatności jak Tor Browser na komputerach stacjonarnych. Do codziennego, zwykłego użytku jest w pełni wystarczająca do uzyskania dostępu do usług onion, jednak jeśli obawiasz się śledzenia lub monitorowania ze strony zaawansowanych przeciwników, nie powinieneś polegać na niej jako na narzędziu anonimowości.

[Warto zauważyć](https://github.com/privacyguides/privacyguides.org/issues/2929), że Onion Browser nie *gwarantuje*, iż cały ruch przechodzi przez sieć Tor. Korzystając z wbudowanej wersji Tora, [Twój prawdziwy adres IP **może** zostać ujawniony przez WebRTC oraz strumienie audio/wideo](https://onionbrowser.com/faqs) z powodu ograniczeń silnika WebKit. *Bezpieczniej* jest używać Onion Browser razem z aplikacją [Orbot](alternative-networks.md#orbot), choć nawet wtedy istnieją pewne ograniczenia wynikające z samego systemu iOS.
