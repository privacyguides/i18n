---
title: "Arten von Kommunikationsnetzen"
icon: 'material/transit-connection-variant'
description: Eine Übersicht über mehrere Netzwerkarchitekturen, die häufig von Instant-Messaging-Anwendungen verwendet werden.
---

Es gibt mehrere Netzwerkarchitekturen, die häufig verwendet werden, um Nachrichten zwischen Menschen zu übertragen. Diese Netzwerke können unterschiedliche Datenschutzgarantien bieten, weshalb es sich lohnt, bei der Entscheidung, welche App du verwenden möchtest, ihr [Bedrohungsmodell](../basics/threat-modeling.md) zu berücksichtigen.

[Empfohlene Instant Messenger](../real-time-communication.md ""){.md-button}

## Zentralisierte Netzwerke

![Diagramm eines zentralisierten Netzwerks](../assets/img/layout/network-centralized.svg){ align=left }

Zentralisierte Messenger sind solche, bei denen sich alle Teilnehmer auf demselben Server oder einem Netzwerk von Servern befinden, die von derselben Organisation kontrolliert werden.

Bei einigen selbst gehosteten Messengern kannst du deine eigenen Server einrichten. Self-Hosting kann zusätzliche Datenschutzgarantien bieten, z. B. keine Nutzungsprotokolle oder begrenzten Zugriff auf Metadaten (Daten darüber, wer mit wem spricht). Selbst gehostete, zentralisierte Messenger sind isoliert und jeder muss sich auf demselben Server befinden, um zu kommunizieren.

**Vorteile:**

- Neue Funktionen und Änderungen können schneller implementiert werden.
- Einfacher Einstieg und leichtere Kontaktaufnahme.
- Die meisten ausgereiften und stabilen Funktionen von Ökosystemen, da sie in einer zentralisierten Software leichter zu programmieren sind.
- Probleme mit dem Datenschutz können verringert werden, wenn du einem Server vertraust, den du selbst hostest.

**Nachteile:**

- Kann [eingeschränkte Kontrolle oder Zugang](https://drewdevault.com/2018/08/08/Signal.html) beinhalten. Dazu können Dinge gehören wie:
- [Das Verbot, Drittanbieter-Clients](https://github.com/LibreSignal/LibreSignal/issues/37#issuecomment-217211165) an das zentrale Netzwerk anzuschließen, die eine bessere Anpassung oder ein besseres Erlebnis ermöglichen könnten. Häufig in den Nutzungsbedingungen definiert.
- Schlechte oder fehlende Dokumentation für Drittentwickler.
- Die [Eigentumsverhältnisse](https://web.archive.org/web/20210729191953/https://blog.privacytools.io/delisting-wire), die Datenschutzrichtlinien und der Betrieb des Dienstes können sich leicht ändern, wenn er von einer einzigen Stelle kontrolliert wird, was den Dienst zu einem späteren Zeitpunkt gefährden kann.
- Selbst-Hosting erfordert Anstrengungen und Kenntnisse darüber, wie man einen Service aufbauen kann.

## Föderierte Netzwerke

![Diagramm eines föderalen Netzwerks](../assets/img/layout/network-decentralized.svg){ align=left }

Föderierte Messenger verwenden mehrere unabhängige, dezentralisierte Server, die miteinander kommunizieren können (E-Mail ist ein Beispiel für einen föderierten Dienst). Durch die Föderation können Systemadministratoren ihren eigenen Server kontrollieren und dennoch Teil eines größeren Kommunikationsnetzes sein.

Wenn sie selbst gehostet werden, können die Mitglieder eines Verbund-Servers die Mitglieder anderer Server entdecken und mit ihnen kommunizieren, obwohl einige Server sich dafür entscheiden können, privat zu bleiben, indem sie nicht föderiert sind (z. B. ein Arbeitsteam-Server).

**Vorteile:**

- Ermöglicht eine bessere Kontrolle über deine eigenen Daten, wenn du deinen eigenen Server betreibst.
- Erlaubt dir auszuwählen, wem du deine Daten anvertraust, indem du zwischen mehreren "öffentlichen" Servern entscheiden kannst.
- Ermöglicht oft den Einsatz von Drittanbieter-Clients, die eine nativere, individuellere oder zugänglichere Erfahrung bieten können.
- Server software can be verified that it matches public source code, assuming you have access to the server, or you trust the person who does (e.g., a family member).

**Nachteile:**

- Das Hinzufügen neuer Funktionen ist komplexer, da diese Funktionen standardisiert und getestet werden müssen, um sicherzustellen, dass sie mit allen Servern im Netzwerk funktionieren.
- Aufgrund des vorhergehenden Punktes können Funktionen fehlen, unvollständig sein oder auf unerwartete Weise im Vergleich zu zentralisierten Plattformen funktionieren, wie z. B. die Weiterleitung von Nachrichten, wenn sie offline sind oder das Löschen von Nachrichten.
- Einige Metadaten können verfügbar sein (z. B. Informationen wie "wer spricht mit wem", aber nicht der eigentliche Nachrichteninhalt, wenn E2EE verwendet wird).
- Bei föderierten Servern ist es meist erforderlich, dem Administrator deines Servers zu vertrauen. Sie sind vielleicht Hobbyisten oder keine "Sicherheitsprofis" und stellen möglicherweise keine Standarddokumente wie Datenschutzrichtlinien oder Nutzungsbedingungen zur Verfügung, in denen die Verwendung deiner Daten genau beschrieben ist.
- Serveradministratoren entscheiden sich manchmal dafür, andere Server zu sperren, die eine Quelle von unmoderiertem Missbrauch sind oder gegen allgemeine Regeln des akzeptierten Verhaltens verstoßen. Dadurch wird die Kommunikation mit den Mitgliedern dieser Server behindert.

## Peer-to-Peer-Netzwerke

![P2P-Diagramm](../assets/img/layout/network-distributed.svg){ align=left }

P2P-Messenger stellen eine Verbindung zu einem [verteilten Netzwerk](https://en.wikipedia.org/wiki/Distributed_networking) von Knoten her, um eine Nachricht ohne einen Server von Dritten an die Zielperson weiterzuleiten.

Die Clients (Peers) finden einander in der Regel über ein [verteiltes Computernetz](https://en.wikipedia.org/wiki/Distributed_computing). Beispiele hierfür sind [verteilte Hashtabellen (DHT)](https://de.wikipedia.org/wiki/Verteilte_Hashtabelle), die z. B. von [Torrents](https://de.wikipedia.org/wiki/BitTorrent) und [IPFS](https://de.wikipedia.org/wiki/InterPlanetary_File_System) verwendet werden. Another approach is proximity based networks, where a connection is established over Wi-Fi or Bluetooth (for example, Briar or the [Scuttlebutt](https://scuttlebutt.nz) social network protocol).

Sobald ein Peer über eine dieser Methoden einen Weg zu dem Kontakt gefunden hat, wird eine direkte Verbindung zwischen beiden hergestellt. Obwohl die Nachrichten in der Regel verschlüsselt sind, kann ein Beobachter dennoch den Standort und die Identität von Absender und Empfänger feststellen.

P2P-Netze verwenden keine Server, da die Peers direkt miteinander kommunizieren und daher nicht selbst gehostet werden können. Einige zusätzliche Dienste können jedoch von zentralen Servern abhängen, wie z. B. die Benutzer-Entdeckung oder die Weiterleitung von Offline-Nachrichten, die von einem Selbst-Hosting profitieren können.

**Vorteile:**

- Es werden nur wenige Informationen an Dritte weitergegeben.
- Moderne P2P-Plattformen implementieren standardmäßig E2EE. Im Gegensatz zu zentralisierten und föderierten Modellen gibt es keine Server, die Ihre Übertragungen möglicherweise abfangen und entschlüsseln könnten.

**Nachteile:**

- Reduzierter Funktionsumfang:
- Nachrichten können nur gesendet werden, wenn beide Peers online sind. Dein Client kann jedoch Nachrichten lokal speichern, um zu warten, bis der Kontakt wieder online ist.
- Normalerweise erhöht sich der Akkuverbrauch auf mobilen Geräten, da der Client mit dem verteilten Netzwerk verbunden bleiben muss, um zu erfahren, wer online ist.
- Einige gängige Messenger-Funktionen sind möglicherweise nicht oder nur unvollständig implementiert, z. B. das Löschen von Nachrichten.
- Deine IP-Adresse und die der Kontakte, mit denen du kommunizierst, können aufgedeckt werden, wenn du die Software nicht in Verbindung mit einem [VPN](../vpn.md) oder [Tor](../tor.md) benutzt. In vielen Ländern gibt es eine Art von Massenüberwachung und/oder Metadatenspeicherung.

## Anonymes Routing

![Diagram von Anonymes Routing](../assets/img/layout/network-anonymous-routing.svg){ align=left }

Ein Messenger, der [anonymes Routing](https://doi.org/10.1007/978-1-4419-5906-5_628) verwendet, verbirgt entweder die Identität des Absenders, des Empfängers oder den Nachweis, dass sie miteinander kommuniziert haben. Im Idealfall sollte ein Messenger alle drei verstecken.

There are [many](https://doi.org/10.1145/3182658) ways to implement anonymous routing. Eines der bekanntesten ist das [Onion-Routing](https://de.wikipedia.org/wiki/Onion-Routing) (d. h. [Tor](tor-overview.md)), bei dem verschlüsselte Nachrichten über ein virtuelles [Overlay-Netzwerk](https://en.wikipedia.org/wiki/Overlay_network) übertragen werden, das den Standort jedes Knotens sowie den Empfänger und Absender jeder Nachricht verbirgt. Absender und Empfänger interagieren nie direkt, sondern treffen sich nur über einen geheimen Rendezvous-Knoten, so dass weder IP-Adressen noch physische Standorte bekannt werden. Die Knoten können die Nachrichten nicht entschlüsseln, ebenso wenig wie das endgültige Ziel, nur der Empfänger kann es. Jeder Zwischenknoten kann nur einen Teil entschlüsseln, der angibt, wohin die noch verschlüsselte Nachricht als Nächstes zu senden ist, bis sie beim Empfänger ankommt, der sie vollständig entschlüsseln kann, daher die "Onion Layer" (zu Deutsch: Zwiebelschichten).

Self-hosting a node in an anonymous routing network does not provide the host with additional privacy benefits, but rather contributes to the whole network's resilience against identification attacks for everyone's benefit.

**Vorteile:**

- Es werden nur wenige bis gar keine Informationen an andere Parteien weitergegeben.
- Nachrichten können dezentral weitergegeben werden, auch wenn eine der Parteien offline ist.

**Nachteile:**

- Langsame Nachrichtenausbreitung.
- Oft auf wenige Medientypen beschränkt, meist Text, da das Netzwerk langsam ist.
- Weniger zuverlässig, wenn die Knoten nach dem Zufallsprinzip ausgewählt werden. Einige Knoten können sehr weit von Sender und Empfänger entfernt sein, wodurch sich die Latenzzeit erhöht oder sogar Nachrichten nicht übertragen werden können, wenn einer der Knoten offline geht.
- Der Einstieg ist komplizierter, da die Erstellung und sichere Verwahrung eines kryptografischen privaten Schlüssels erforderlich ist.
- Genau wie bei anderen dezentralen Plattformen ist das Hinzufügen von Funktionen komplexer als bei einer zentralen Plattform. Daher kann es sein, dass Funktionen fehlen oder unvollständig implementiert sind, wie z. B. die Offline-Weiterleitung von Nachrichten oder das Löschen von Nachrichten.
