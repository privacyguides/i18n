---
title: "Alternative Netzwerke"
icon: material/vector-polygon
description: These Werkzeuge erlauben dir Zugriff zu Netzwerke außerhalb des World Wide Webs.
cover: alternative-networks.webp
---

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-server-network: Dienstanbieter](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-eye-outline: Massenüberwachung](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }
- [:material-account-cash: Überwachungskapitalismus](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

## Anonymisierungsnetzwerke

Wenn es zu Anonymisierungsnetzwerke kommt, wollen wir notieren das [Tor](advanced/tor-overview.md) unsere erste Wahl ist. Es ist bei weitem das meist verwendete, robust untersuchte und aktiv entwickelte anonyme Netzwerk. Das Nutzen von anderen Netzwerken bringt größere Gefahr zu deiner [:material-incognito: Anonymität](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }, außer wenn du weißt was du machst.

### Tor

<div class="admonition recommendation" markdown>

![Tor logo](assets/img/self-contained-networks/tor.svg){ align=right }

Das **Tor** Netzwerk ist eine Gruppe von Freiwilligen betriebenen Servern die dir erlauben, sich kostenlos zu verbinden und deine Privatsphäre und Sicherheit im Internet zu verbessern. Einzelpersonen und Organisationen können auch Informationen über das Tor-Netzwerk mit ".onion versteckten Diensten" austauschen, ohne ihre Privatsphäre zu gefährden. Da Tor Verkehr schwer zu blockieren und zu verfolgen ist, ist Tor ein effektives Werkzeug gegen [:material-close-outline: Zensur](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }.

[:octicons-home-16:](https://torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Dokumentation }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=beitragen }

</div>

Der empfohlene Weg um das Tor Netzwerk zuzugreifen ist über den offiziellen Tor Browser, die folgende Seite beinhaltet mehr Informationen über den Browser:

[Tor Browser Information :material-arrow-right-drop-circle:](tor.md){ .md-button .md-button--primary } [detaillierte Tor Übersicht :material-arrow-right-drop-circle:](advanced/tor-overview.md){ .md-button }

Du kannst das Tor Netzwerk mit anderen Werkzeugen zugreifen, dies ist abhängig von deinem Bedrohungsmodell. Wenn du ein normaler Tor Nutzer bist, der keine Sorgen hat, dass dein Internetanbieter Beweise über dich sammelt, dann sind Apps wie [Orbot](#orbot) oder Mobile Browser Apps zum Zugriff vom Tor Netzwerk unproblematisch. Wenn mehr Menschen regelmäßig Tor nutzen, hilft das, das schlechte Stigma von Tor zu verringern und senkt zudem die Qualität der "Listen von Tor-Nutzern", die ISPs und Regierungen erstellen können.

<div class="admonition example" markdown>
<p class="admonition-title">Versuche es!</p>

Du kannst versuchen, über Tor bei [xoe4vn5uwdztif6goazfbmogh6wh5jc4up35bqdflu6bkdc5cas5vjqd.onion](http://www.xoe4vn5uwdztif6goazfbmogh6wh5jc4up35bqdflu6bkdc5cas5vjqd.onion) _Privacy Guides_ zu öffnen.

</div>

#### Orbot

<div class="admonition recommendation" markdown>

![Orbot logo](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** ist eine Handy-App, die Verkehr von jeder App auf deinem Handy über das Tor Netzwerk sendet.

[:octicons-home-16: Homepage](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Datenschutzbestimmungen" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title="beitragen" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)
- [:simple-fdroid: F-Droid](https://guardianproject.info/fdroid)

</details>

</div>

Wir haben vorher die Option _Zieladressen isolieren_ Einstellung innerhalb Orbot empfohlen. Obwohl diese Einstellung theoretisch deine Privatsphäre verbessern könnte, indem es für jede IP-Adresse zu der man sich verbindet einen eigenen Circuit benutzt, gibt es keinen praktischen Nutzen für die meisten Applikationen (insbesondere Web browsen). Ebenfalls kommt es mit einem Leistungsnachteil und erhöht Verkehr im Tor Netwerk. Wir empfehlen es nicht mehr diese Option zu ändern, außer wenn du es brauchst.[^1]

\=== "Android"

```
Orbot kann zu individuellen Apps weiterleiten, wenn sie SOCKS oder HTTP Proxying unterstützen. Es können ebenfalls alle deine Netzwerkverbindung mit [VpnService](https://developer.android.com/reference/android/net/VpnService) weitergeleitet werden und kann mit der VPN-Kill-Switch in :gear: **Einstellungen** → **Netzwerk & Internet** → **VPN** → :gear: → **Blockiere Verbindungen ohne VPN** benutzt werden.

Orbot ist oft auf Google Play und im Guardian Projects F-Droid Repository veraltet, also beachte dass du stattdessen Orbot von der Github Repository herunterladest. Alle Versionen werden mit der gleichen Signatur signiert, also sollten alle kompatible miteinander sein.
```

\=== "iOS"

```
Auf iOS hat Orbot beschränkungen die zu Abstürze oder zu leaks führen können: iOS hat kein effektives OS-Level Feature um Verbindungen ohne VPN zu blockieren, und iOS hat auch ein künstliches Speicherlimit für Netzwerkerweiterungen, dies macht es schwer, Tor über Orbot ohne Probleme zu benutzen. Derzeit ist es immer sicherer Tor auf einem Computer anstatt auf einem Handy zu benutzen.
```

#### Snowflake

<div class="admonition recommendation" markdown>

![Snowflake logo](assets/img/self-contained-networks/snowflake.svg#only-light){ align=right }
![Snowflake logo](assets/img/self-contained-networks/snowflake-dark.svg#only-dark){ align=right }

**Snowflake** erlaubt dir Bandbreite zum Tor Projekt zu spenden, indem man innerhalb seines Browsers eine "Snowflake Proxy" betreibt.

Leute die zensiert werden, können Snowflake-Proxies benutzen, um sich zum Tor Netzwerk zu verbinden. Snowflake ist ein guter Weg zum Netzwerk beizutragen, auch wenn man nicht das technische Know-How hat, um ein Tor Relay oder Bridge zu betreiben.

[:octicons-home-16: Homepage](https://snowflake.torproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Dokumentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="QuellCode" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=beitragen }

</details>

</div>

Du kannst Snowflake in deinem Browser aktivieren, indem man es in einem neuen Tab öffnet und den Schalter aktiviert. Du kannst es in Hintergrund laufen lassen während du browst, um deine Verbindung beizutragen. Wir empfehlen nicht Snowflake als Browsererweiterung, weil Erweiterungen von Dritten deine Angriffsoberfläche vergrößert.

[Führe Snowflake in deinem Browser aus :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html){ .md-button }

Snowflake erhöht nicht deine Privatsphäre. Ebenfalls kann es auch nicht benutzt werden, um innerhalb deines persönlichen Browsers Zugriff auf das Tor Netzwerk zu bekommen. Allerdings solltest du es Berücksichtigen, wenn deine Internetverbindung unzensiert ist, da es Leuten mit zensierter Verbinden mit deren Privatsphären helfen kann. Es gibt keinen Grund sich Sorgen zu machen, welche Webseiten Leute durch deiner Proxy besuchen, da ihre sichtbare IP-Adresse der ihrer Tor-Exit-Node entspricht, nicht deiner.

Das Betreiben einer Snowflake Proxy ist risikoarm, da das Betreiben eines Tor-Relays oder Bridge auch nicht sehr Risikoreich ist. Da aber Verkehr durch dein Netzwerk läuft, kann es wirkungsvoll auf deiner Verbindung sein, am meisten, wenn dein Netzwerk eine Bandbreitenlimitierung hat. Stelle sicher, dass du verstehst [wie Snowflake funktioniert](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) bevor du eine Proxy betreibst.

### I2P (The Invisible Internet Project)

<div class="admonition recommendation" markdown>

![I2P logo](assets/img/self-contained-networks/i2p.svg#only-light){ align=right }
![I2P logo](assets/img/self-contained-networks/i2p-dark.svg#only-dark){ align=right }

**I2P** ist eine Netzwerkschicht, die deine Verbindung verschlüsselt, und sie über ein Netzwerk von Computern auf der ganzen Welt leitet. Es ist hauptsächlich fokussiert ein alternatives, Privatsphäre-schützendes Netzwerk zu erstellen, statt normales Internetverkehr zu anonymisieren.

[:octicons-home-16: Homepage](https://geti2p.net/en){ .md-button .md-button--primary }
[:octicons-info-16:](https://geti2p.net/en/about/software){ .card-link title=Dokumentation }
[:octicons-code-16:](https://github.com/i2p/i2p.i2p){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://geti2p.net/en/get-involved){ .card-link title=beitragen }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.i2p.android)
- [:simple-android: Android](https://geti2p.net/en/download#android)
- [:fontawesome-brands-windows: Windows](https://geti2p.net/en/download#windows)
- [:simple-apple: macOS](https://geti2p.net/en/download#mac)
- [:simple-linux: Linux](https://geti2p.net/en/download#unix)

</details>

</div>

Im Gegensatz zu Tor ist jeder I2P Verkehr nur innerhalb des I2P Netzwerkes, dies heißt, dass normale Internetseiten **nicht** direkt über I2P verfügbar sind. Stattdessen kannst du dich zu Webseiten verbinden die anonym gehostet werden und direkt am I2P Netzwerk sind, sie heißen "eepsites" und haben Domains die mit `.i2p` enden.

<div class="admonition example" markdown>
<p class="admonition-title">Versuche es!</p>

Du kannst versuchen, dich bei _Privacy Guides_ über I2P zu verbinden: [privacyguides.i2p](http://privacyguides.i2p/?i2paddresshelper=fvbkmooriuqgssrjvbxu7nrwms5zyhf34r3uuppoakwwsm7ysv6q.b32.i2p).

</div>

Ebenfalls wird standardmäßig jeder I2P Knoten Verkehr für andere Nutzer weitergeleitet, statt eigene Relays von Freiwilligen zu benutzen. Es gibt ungefähr [10.000](https://metrics.torproject.org/networksize.html) Relays und Bridges im Tor Netzwerk, verglichen mit ~50.000 auf I2P, gibt es mehr Wege für deinen Verkehr weitergeleitet zu werden, um deine Anonymität zu maximieren. I2P ist öfter auch mehr leistungsfähiger als Tor, dies ist wahrscheinlich eine Nebenwirkung da Tor mehr auf normalen "Clearnet" Internetverkehr fokussiert ist, und dadurch mehr engpässige Exitknoten verwendet. Versteckte Service Leistung ist allgemein besser auf I2P verglichen mit Tor. Während P2P Applikationen wie BitTorrent schwer auf Tor zum Laufen sind (da es massive Wirkung auf die Netzwerkleistung von Tor hat), ist es relativ leicht und leistungsstark auf I2P.

Allerdings gibt es aber Nachteile bei I2P. Da Tor mehr auf das Weiterleiten auf gewidmeten Exitknoten vertraut, können es mehr Leute innerhalb weniger sicheren Umgebungen nutzen, und die Relay die auf Tor existieren sind wahrscheinlich mehr leistungsstärker und stabiler, weil es typischerweise nicht auf Hausanschlüsse laufen. Tor ist ebenfalls mit dem [Tor Browser](tor.md) auch mehr auf Browser-Privatsphäre fokussiert (das heißt Anti-Fingerprinting), damit deine Browsing-Aktivität so anonym wie möglich sein kann. I2P wird mit deinem [normalen Internetbrowser](desktop-browsers.md) verwendet, obwohl du deine Browsereinstellungen so ändern kannst, sodass sie mehr Privatsphäre-schützend sind, wirst du wahrscheinlich nicht den gleichen Browser-Fingerprint wie andere I2P-Nutzer haben (Dadurch gibt es keine "Menge" in der man sich vermischen kann).

Tor ist auch wahrscheinlich mehr resistenter gegen Zensur aufgrund ihres robusten Netzwerkes von Bridges und unterschiedlichen [einsteckbaren Transporten](https://tb-manual.torproject.org/circumvention). Andererseits benutzt I2P Verzeichnisserver für initiale Verbindungen, die unvertraulich sind und von Freiwilligen betrieben sind, verglichen mit den vertrauten/hardkodierten die Tor benutzt, die wahrscheinlich leichter zu blockieren sind.

[^1]: Die `IsolateDestAddr` Einstellung wurde auf der [Tor Mailingliste](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403) und der [Whonix Stream Isolation Dokumentation](https://whonix.org/wiki/Stream_Isolation) besprochen, wo beide Projekte vorschlagen, dass es nicht für die meisten geeignet ist.
