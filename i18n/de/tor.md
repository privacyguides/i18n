---
meta_title: "Tor Browser und Netzwerk: Anonymes Surfen im Internet - Privacy Guides"
title: "Tor Browser"
icon: simple/torbrowser
description: Schütze dein Surfen im Internet vor neugierigen Blicken, indem du das Tor-Netzwerk nutzt, ein sicheres Netzwerk, das die Zensur umgeht.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
    sameAs: https://de.wikipedia.org/wiki/Tor_(Netzwerk)
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

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-account-cash: Überwachungskapitalismus](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: Massenüberwachung](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Zensur](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

Das **Tor** Netzwerk besteht aus von Freiwilligen betriebenen Servern, die es kostenlos ermöglichen, die eigene Privatsphäre und Sicherheit im Internet zu verbessern. Einzelpersonen und Organisationen können auch Informationen über das Tor-Netzwerk mit ".onion versteckten Diensten" austauschen, ohne ihre Privatsphäre zu gefährden. Da der Tor-Verkehr schwer zu blockieren und zurückzuverfolgen ist, ist Tor ein effektives Werkzeug zur Zensur Umgehung.

[Detaillierte Tor-Übersicht :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: Video: Why You Need Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor/ ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Tipp</p>

Bevor du dich mit Tor verbindest, stelle bitte sicher, dass du unsere in unserer [Übersicht](advanced/tor-overview.md) darüber gelesen hast, was Tor ist und wie man sich sicher mit Tor verbindet. Wir empfehlen oft, sich über einen vertrauenswürdigen [VPN-Anbieter](vpn.md) mit Tor zu verbinden, aber du musst das **sorgfältig** machen, um deine Anonymität nicht zu beeinträchtigen.

</div>

Es gibt eine Vielzahl von Möglichkeiten, sich von deinem Gerät aus mit dem Tor-Netzwerk zu verbinden. Die am häufigsten genutzte ist der **Tor Browser**, ein Fork (Abwandlung) von Firefox, der für [:material-incognito: anonymes](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} Surfen für Desktop-Computer und für Android entwickelt wurde.

Einige dieser Anwendungen sind besser als andere, und auch hier hängt die Entscheidung von deinem Bedrohungsmodell ab. Wenn du ein gelegentlicher Tor-Benutzer bist, der sich keine Sorgen darüber macht, dass dein Internetanbieter Beweise gegen dich sammelt, ist es wahrscheinlich in Ordnung, Anwendungen wie [Orbot](#orbot) oder mobile Browseranwendungen zu benutzen, um auf das Tor-Netzwerk zuzugreifen. Wenn mehr Menschen regelmäßig Tor nutzen, hilft das, das schlechte Stigma von Tor zu verringern und senkt zudem die Qualität der "Listen von Tor-Nutzern", die ISPs und Regierungen erstellen können.

Wenn du Wert auf vollständige Anonymität legst, solltest du **ausschließlich** den Tor-Browser-Client verwenden, idealerweise in einer Kombination aus [Whonix](desktop.md#whonix) und [Qubes](desktop.md#qubes-os). Mobile Browser sind bei Tor weniger verbreitet (und daher anfälliger für Fingerprinting). Außerdem sind diese Konfigurationen nicht so rigoros gegen Deanonymisierung getestet.

## Tor Browser

<div class="admonition recommendation" markdown>

![Tor-Browser-Logo](assets/img/browsers/tor.svg){ align=right }

**Tor Browser** ist die richtige Wahl, wenn du Anonymität brauchst, denn er bietet dir Zugang zum Tor-Netzwerk und zu den Brücken. Er enthält Standardeinstellungen und Erweiterungen, die automatisch durch die Standard-Sicherheitsstufen konfiguriert werden: *Standard*, *Sicherer* und *Am Sichersten*.

[:octicons-home-16: Homepage](https://www.torproject.org/de/){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org/de/){ .card-link title=Benutzerhandbuch}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Quelltext" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Unterstützen}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:fontawesome-brands-windows: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Achtung</p>

Du solltest **niemals** zusätzliche Erweiterungen für den Tor-Browser installieren oder die "about:config"-Einstellungen bearbeiten, auch nicht die, die wir für Firefox vorschlagen. Browsererweiterungen und nicht standardisierte Einstellungen heben dich von anderen im Tor-Netzwerk ab und machen deinen Browser einfacher zu [fingerprinten](https://support.torproject.org/glossary/browser-fingerprinting).

</div>

Der Tor-Browser wurde entwickelt, um Fingerprinting zu verhindern, oder um dich anhand deiner Browserkonfiguration zu identifizieren. Daher ist es absolut notwendig, dass du den Browser in **keiner Weise**veränderst, abgesehen von der Anpassung der [Standard-Sicherheitsstufen](https://tb-manual.torproject.org/security-settings).

Zusätzlich zur Installation des Tor-Browsers auf deinem Computer, gibt es auch Betriebssysteme, die speziell für die Verbindung mit dem Tor-Netzwerk entwickelt wurden, wie [Whonix](desktop.md#whonix) oder [Qubes OS](desktop.md#qubes-os), die noch mehr Sicherheit und Schutz bieten als alleine der Standard-Tor-Browser.

## Orbot

<div class="admonition recommendation" markdown>

![Orbot-Logo](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** ist ein kostenloser Tor-VPN für Smartphones, das den Datenverkehr von jeder App auf deinem Gerät durch das Tor-Netzwerk leitet.

[:octicons-home-16: Homepage](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Dokumentation}
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Quelltext" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Mitwirken}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

</details>

</div>

Wir haben bereits empfohlen, die Einstellung *Isolate Destination Address* in den Orbot-Einstellungen zu aktivieren. Während diese Einstellung theoretisch die Privatsphäre verbessern kann, indem sie für jede IP-Adresse, mit der du dich verbindest, eine andere Schaltung erzwingt, bietet sie für die meisten Anwendungen (vor allem für das Surfen im Internet) keinen praktischen Vorteil, kann mit einem erheblichen Leistungsverlust einhergehen und erhöht die Belastung des Tor-Netzwerks. Wir empfehlen nicht länger, diese Einstellung von ihrem Standardwert anzupassen, es sei denn, du weißt dass du das brauchst.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Tipps für Android</p>

Orbot kann einzelne Anwendungen proxyen, wenn diese SOCKS oder HTTP-Proxys unterstützen. Es kann auch alle deine Netzwerkverbindungen mit [VpnService](https://developer.android.com/reference/android/net/VpnService) proxyisieren und kann mit dem VPN-Kill-Switch in :gear: **Einstellungen** → **Netzwerk & Internet** → **VPN** → :gear: → **Verbindungen ohne VPN** blockieren.

Orbot ist auf dem [F-Droid Repository](https://guardianproject.info/fdroid) des Guardian Projects und [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android) oft veraltet, daher solltest du den Download direkt vom [GitHub Repository](https://github.com/guardianproject/orbot/releases) in Betracht ziehen.

Alle Versionen sind mit der gleichen Signatur versehen, sodass sie miteinander kompatibel sein sollten.

</div>

Unter iOS hat Orbot einige Einschränkungen, die zu Abstürzen oder Lecks führen können: iOS hat keine effektive Funktion auf Betriebssystemebene, um Verbindungen ohne VPN zu blockieren, wie es bei Android der Fall ist. iOS hat auch eine künstliche Speicherbegrenzung für Netzwerkerweiterungen, die es schwierig macht, Tor in Orbot ohne Abstürze zu betreiben. Derzeit ist es immer sicherer, Tor auf einem Desktop-Computer zu benutzen als auf einem mobilen Gerät.

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Onion Browser Logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

Der **Onion Browser** ist ein Open-Source-Browser, mit dem du auf iOS-Geräten anonym über das Tor-Netzwerk im Internet surfen kannst. Er wird vom [Tor-Projekt](https://support.torproject.org/glossary/onion-browser) unterstützt. [:material-star-box: Lies unsere neuste Onion Browser Review.](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review/)

[:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Spenden }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser bietet nicht das gleiche Maß an Datenschutz wie Tor Browser auf Desktop-Plattformen. Für den gelegentlichen Gebrauch ist es eine gute Möglichkeit, auf Hidden-Services zuzugreifen, aber wenn du dir Sorgen machst, von fortgeschrittenen Gegnern verfolgt oder überwacht zu werden, solltest du dich nicht auf dieses Anonymitätstool verlassen.

[Wichtig:](https://github.com/privacyguides/privacyguides.org/issues/2929) der Onion Browser *garantiert nicht*, dass alle Anfragen durch Tor gehen. Bei der Verwendung der integrierte Tor Version, [**wird** deine echte IP via WebRTC und Audio/Video-Streams geleakt werden](https://onionbrowser.com/faqs), aufgrund von Einschränkungen durch WebKit. Es ist *sicherer* den Onion Browser zusammen mit Orbot zu verwenden, aber auch das ist unter iOS mit einigen Einschränkungen verbunden (siehe den Orbot Abschnitt)

[^1]: Die `IsolateDestAddr`-Einstellung wird auf der [Tor Mailingliste](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) und [Whonix's Stream Isolation Dokumentation](https://whonix.org/wiki/Stream_Isolation)diskutiert, wo beide Projekte darauf hinweisen, dass es für die meisten Leute kein guter Ansatz ist.
