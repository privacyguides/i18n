---
meta_title: "Tor Browser und Netzwerk: Anonymes Surfen im Internet - Privacy Guides"
title: "Tor-Netzwerk"
icon: simple/torproject
description: Schütze dein Surfen im Internet vor neugierigen Blicken, indem du das Tor-Netzwerk nutzt, ein sicheres Netzwerk, das die Zensur umgeht.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
    image: /assets/img/browsers/tor.svg
    url: https://www.torproject.org
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

![Tor logo](assets/img/self-contained-networks/tor.svg){ align=right }

Das **Tor** Netzwerk besteht aus von freiwillig betriebenen Servern, die es ermöglichen, kostenlos die eigene Privatsphäre und Sicherheit im Internet zu verbessern. Einzelpersonen und Organisationen können auch Informationen über das Tor-Netzwerk mit ".onion versteckten Diensten" austauschen, ohne ihre Privatsphäre zu gefährden. Da der Tor-Verkehr schwer zu blockieren und zurückzuverfolgen ist, ist Tor ein effektives Werkzeug zur Zensur Umgehung.

[:octicons-home-16:](https://www.torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }

Tor funktioniert, indem es deinen Internetverkehr über diese von Freiwilligen betriebenen Server leitet, anstatt eine direkte Verbindung zu der Website herzustellen, die du besuchen willst. Dadurch wird verschleiert, woher der Datenverkehr kommt, und kein Server im Verbindungspfad ist in der Lage, den vollständigen Pfad zu sehen, woher der Datenverkehr kommt und wohin er geht, was bedeutet, dass selbst die Server, die du für die Verbindung verwendest, deiner Anonymität nichts anhaben können.

[Detaillierte Tor-Übersicht :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Verbinden mit Tor

!!! tip

    Before connecting to Tor, please ensure you've read our [overview](advanced/tor-overview.md) on what Tor is and how to connect to it safely. We often recommend connecting to Tor through a trusted [VPN provider](vpn.md), but you have to do so **properly** to avoid decreasing your anonymity.

Es gibt eine Vielzahl von Möglichkeiten, sich von deinem Gerät aus mit dem Tor-Netzwerk zu verbinden. Die am häufigsten genutzte ist der **Tor Browser**, ein Fork (Abwandlung) von Firefox, der für anonymes Surfen für Desktop-Computer und Android entwickelt wurde.

Some of these apps are better than others, and again making a determination comes down to your threat model. If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using apps like [Orbot](#orbot) or mobile browser apps to access the Tor network is probably fine. Increasing the number of people who use Tor on an everyday basis helps reduce the bad stigma of Tor, and lowers the quality of "lists of Tor users" that ISPs and governments may compile.

If more complete anonymity is paramount to your situation, you should **only** be using the desktop Tor Browser client, ideally in a [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os) configuration. Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

### Tor Browser

!!! recommendation

    ![Tor-Browser-Logo](assets/img/browsers/tor.svg){ align=right }
    
    **Tor Browser** ist die richtige Wahl, wenn du Anonymität brauchst, denn er bietet dir Zugang zum Tor-Netzwerk und zu den Brücken. Er enthält Standardeinstellungen und Erweiterungen, die automatisch durch die Standard-Sicherheitsstufen konfiguriert werden: *Standard*, *Sicherer* und *Am Sichersten*.
    
    [:octicons-home-16: Homepage](https://www.torproject.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
    [:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Documentation }
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
        - [:simple-android: Android](https://www.torproject.org/download/#android)
        - [:simple-windows11: Windows](https://www.torproject.org/download/)
        - [:simple-apple: macOS](https://www.torproject.org/download/)
        - [:simple-linux: Linux](https://www.torproject.org/download/)

!!! !!! danger "Achtung"

    Du solltest **niemals** zusätzliche Erweiterungen für den Tor-Browser installieren oder die "about:config"-Einstellungen bearbeiten, auch nicht die, die wir für Firefox vorschlagen. Browsererweiterungen und nicht standardisierte Einstellungen heben dich von anderen im Tor-Netzwerk ab und machen deinen Browser einfacher zu [fingerprinten](https://support.torproject.org/glossary/browser-fingerprinting).

Der Tor-Browser wurde entwickelt, um Fingerprinting zu verhindern, oder um dich anhand deiner Browserkonfiguration zu identifizieren. Daher ist es zwingend erforderlich, dass du den Browser in **keiner Weise**veränderst, abgesehen von der Anpassung der [Standard-Sicherheitsstufen](https://tb-manual.torproject.org/security-settings/).

In addition to installing Tor Browser on your computer directly, there are also operating systems designed specifically to connect to the Tor network such as [Whonix](desktop.md#whonix) on [Qubes OS](desktop.md#qubes-os), which provide even greater security and protections than the standard Tor Browser alone.

### Orbot

!!! recommendation

    ![Orbot-Logo](assets/img/self-contained-networks/orbot.svg){ align=right }
    
    **Orbot** ist ein kostenloser Tor-VPN für Smartphones, das den Datenverkehr von jeder App auf deinem Gerät durch das Tor-Netzwerk leitet.
    
    [:octicons-home-16: Homepage](https://orbot.app/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title=Datenschutzrichtlinie }
    [:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Dokumentation}
    [:octicons-code-16:](https://orbot.app/code){ .card-link title=Quelltext}
    [:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Mitwirken }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/orbot/id1609461599)
        - [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

Wir haben bereits empfohlen, die Einstellung *Isolate Destination Address* in den Orbot-Einstellungen zu aktivieren. Während diese Einstellung theoretisch die Privatsphäre verbessern kann, indem sie für jede IP-Adresse, mit der du dich verbindest, eine andere Schaltung erzwingt, bietet sie für die meisten Anwendungen (vor allem für das Surfen im Internet) keinen praktischen Vorteil, kann mit einem erheblichen Leistungsverlust einhergehen und erhöht die Belastung des Tor-Netzwerks. Es wird nicht mehr empfohlen, diese Einstellung vom Standardwert abzuweichen, es sei denn, du weißt, dass dass du das tun musst.[^1]

!!! tip "Tipps für Android"

    Orbot kann einzelne Anwendungen proxyen, wenn diese SOCKS oder HTTP-Proxys unterstützen. Es kann auch alle Ihre Netzwerkverbindungen mit [VpnService](https://developer.android.com/reference/android/net/VpnService) proxyen und kann mit dem VPN-Killswitch in :gear: **Einstellungen** → **Netzwerk & internet** → **VPN** → :gear: → **Verbindungen ohne VPN** blockieren.
    
    Orbot ist auf dem [F-Droid Repository](https://guardianproject.info/fdroid) des Guardian Projects und [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android) oft veraltet, daher solltest du den Download direkt vom [GitHub Repository](https://github.com/guardianproject/orbot/releases) in Betracht ziehen.
    
    Alle Versionen sind mit der gleichen Signatur versehen, sodass sie miteinander kompatibel sein sollten.

### Onion Browser

!!! recommendation

    ![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }
    
    **Onion Browser** is an open-source browser that lets you browse the web anonymously over the Tor network on iOS devices and is endorsed by the [Tor Project](https://support.torproject.org/glossary/onion-browser/).
    
    [:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

## Relays und Bridges

### Snowflake

!!! recommendation

    ![Snowflake-Logo](assets/img/browsers/snowflake.svg#only-light){ align=right }
    ![Snowflake-Logo](assets/img/browsers/schneeflocken-dunkel.svg#nur-dunkel){ align=right }
    
    **Snowflake** ermöglicht es dir, Bandbreite an das Tor-Projekt zu spenden, indem du einen "Snowflake-Proxy" in deinem Browser betreibst.
    
    Menschen, die zensiert werden, können Snowflake-Proxys benutzen, um sich mit dem Tor-Netzwerk zu verbinden. Snowflake ist eine großartige Möglichkeit, zum Netzwerk beizutragen, auch wenn du nicht das technische Know-how hast, um einen Tor-Relay oder eine Bridge zu betreiben.
    
    [:octicons-home-16: Homepage](https://snowflake.torproject.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }

Du kannst Snowflake in deinem Browser aktivieren, indem du es in einem anderen Tab öffnest und den Schalter aktivierst. Du kannst es es im Hintergrund laufen lassen, während du surfst, um Ihre Verbindung zu spenden. Wir raten davon ab, Snowflake als Browser-Erweiterung zu installieren; das Hinzufügen von Erweiterungen von Drittanbietern kann deine Angriffsfläche vergrößern.

[Führe Snowflake in deinem Browser aus :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html ""){.md-button}

Snowflake erhöht in keiner Weise deine Privatsphäre und wird auch nicht für die Verbindung mit dem Tor-Netzwerk in deinem persönlichen Browser verwendet. Wenn deine Internetverbindung jedoch unzensiert ist, solltest du in Erwägung ziehen, es zu betreiben, um Menschen in zensierten Netzen zu helfen, ihre Privatsphäre besser zu schützen. Du brauchst dir keine Sorgen darüber zu machen, auf welche Webseiten die Leute über deinen Proxy zugreifen - deine sichtbare IP-Adresse wird mit der ihres Tor-Exit-Knotens übereinstimmen, nicht mit deiner.

Der Betrieb eines Snowflake-Proxys ist risikoarm, sogar risikoärmer als der Betrieb eines Tor-Relays oder einer Tor-Bridge, die ohnehin keine besonders riskanten Unternehmungen sind. Dennoch wird der Datenverkehr durch dein Netzwerk geleitet, was gewisse Auswirkungen haben kann, insbesondere wenn dein Netzwerk eine begrenzte Bandbreite hat. Vergewissere dich, dass du verstehst, [wie Snowflake funktioniert](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home), bevor du dich für die Verwendung eines Proxys entscheidest.

[^1]: Die `IsolateDestAddr` Einstellung wird auf der [Tor Mailingliste](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) und [Whonix's Stream Isolation Dokumentation](https://www.whonix.org/wiki/Stream_Isolation)diskutiert, wo beide Projekte darauf hinweisen, dass es für die meisten Leute kein guter Ansatz ist.
