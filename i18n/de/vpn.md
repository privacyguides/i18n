---
meta_title: "Private VPN-Anbieter Empfehlungen und Vergleiche, kein Sponsoring und keine Werbung - Privacy Guides"
title: "VPN Anbieter"
icon: material/vpn
description: Dies sind die besten VPN-Anbieter zum Schutz deiner Privatsphäre und Sicherheit im Internet. Hier findest du einen Anbieter, der nicht darauf aus ist, dich auszuspionieren.
cover: vpn.png
---

Wenn du auf der Suche nach zusätzlicher **Privatsphäre** vor deinem ISP, in einem öffentlichen Wi-Fi-Netzwerk oder beim Torrenting von Dateien bist, kann ein VPN die Lösung für dich sein, solange du die damit verbundenen Risiken verstehst. Wir sind der Meinung, dass diese Anbieter über den Rest hinausragen:

<div class="grid cards" markdown>

- ![Proton VPN logo](assets/img/vpn/protonvpn.svg){ .twemoji } [Proton VPN](#proton-vpn)
- ![IVPN logo](assets/img/vpn/mini/ivpn.svg){ .twemoji } [IVPN](#ivpn)
- ![Mullvad logo](assets/img/vpn/mullvad.svg){ .twemoji } [Mullvad](#mullvad)

</div>

!!! danger "VPNs bieten keine Anonymität"

    Mit einem VPN bleiben deine Surfgewohnheiten **nicht** anonym, und es bietet auch keine zusätzliche Sicherheit für unsicheren (HTTP) Verkehr.
    
    Wenn du auf der Suche nach **Anonymität** bist, solltest du den Tor-Browser **anstelle** eines VPNs verwenden.
    
    Wenn du auf der Suche nach zusätzlicher **Sicherheit** bist, solltest du immer sicherstellen, dass du eine Verbindung zu Websites über HTTPS herstellst. Ein VPN ist kein Ersatz für gute Sicherheitspraktiken.
    
    [Tor herunterladen](https://www.torproject.org/){ .md-button .md-button--primary } [Tor-Mythen & FAQ](advanced/tor-overview.md){ .md-button }

[Detaillierte VPN-Übersicht :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Empfohlene Anbieter

Die von uns empfohlenen Anbieter verwenden Verschlüsselung, akzeptieren Monero, unterstützen WireGuard & OpenVPN, und haben eine No-Logging-Richtlinie. Weitere Informationen findest du in unserem [vollständigen Kriterienkatalog](#criteria).

### Proton VPN

!!! recommendation annotate

    ![Proton VPN logo](assets/img/vpn/protonvpn.svg){ align=right }
    
    **Proton VPN** ist ein starker Anwärter im VPN-Bereich und ist seit 2016 in Betrieb. Die Proton AG hat ihren Sitz in der Schweiz und bietet sowohl eine begrenzte kostenlose als auch eine umfangreichere Premium-Option an.
    
    [:octicons-home-16: Homepage](https://protonvpn.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Datenschutzrichtlinie" }
    [:octicons-info-16:](https://protonvpn.com/support/){ .card-link title=Dokumentation}
    [:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Quellcode" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id1437005085)
        - [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
        - [:simple-windows11: Windows](https://protonvpn.com/download-windows)
        - [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup/)

#### :material-check:{ .pg-green } 67 Länder

Proton VPN hat [Server in 67 Ländern](https://protonvpn.com/vpn-servers).(1) Die Auswahl eines VPN-Anbieters mit einem Server in deiner Nähe verringert die Latenz des von dir gesendeten Netzwerkverkehrs. Der Grund dafür ist eine kürzere Route (weniger Sprünge) zum Ziel.
{ .annotate }

1. Stand: 2022-09-16

Wir sind außerdem der Meinung, dass es für die Sicherheit der privaten Schlüssel des VPN-Anbieters besser ist, wenn er [dedizierte Server](https://en.wikipedia.org/wiki/Dedicated_hosting_service) verwendet, anstatt billigere gemeinsame Lösungen (mit anderen Kunden) wie [virtuelle private Server](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Unabhängig geprüft

Im Januar 2020 hat sich Proton VPN einem unabhängigen Audit durch SEC Consult unterzogen. SEC Consult fand einige Sicherheitslücken mit mittlerem und niedrigem Risiko in den Windows-, Android- und iOS-Anwendungen von Proton VPN, die alle von Proton VPN vor der Veröffentlichung der Berichte "ordnungsgemäß behoben" wurden. Keines der festgestellten Probleme hätte angreifenden Fernzugriff auf dein Gerät oder deinen Datenverkehr ermöglicht. Du kannst individuelle Berichte für jede Plattform unter [protonvpn.com](https://protonvpn.com/blog/open-source/) einsehen. Im April 2022 unterzog sich Proton VPN [einem weiteren Audit](https://protonvpn.com/blog/no-logs-audit/) und der Bericht [ wurde von Securitum](https://protonvpn.com/blog/wp-content/uploads/2022/04/securitum-protonvpn-nologs-20220330.pdf)erstellt. Eine [Bescheinigung](https://proton.me/blog/security-audit-all-proton-apps) wurde am 9. November 2021 von [Securitum](https://research.securitum.com)für die Apps von Proton VPN ausgestellt.

#### :material-check:{ .pg-green } Open-Source Anwendungen

Proton VPN stellt den Quellcode für seine Desktop- und mobilen Clients in seiner [GitHub Organisation](https://github.com/ProtonVPN)zur Verfügung.

#### :material-check:{ .pg-green } Akzeptiert Bargeld

Proton VPN akzeptiert nicht nur Kredit-/Debitkarten, PayPal und [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), sondern auch **Bargeld/lokale Währung** als anonyme Zahlungsform.

#### :material-check:{ .pg-green } WireGuard-Unterstützung

Proton VPN unterstützt hauptsächlich das WireGuard®-Protokoll. [WireGuard](https://www.wireguard.com) ist ein neueres Protokoll, das modernste [Kryptographie](https://www.wireguard.com/protocol/) verwendet. Darüber hinaus zielt WireGuard darauf ab, einfacher und leistungsfähiger zu sein.

Proton VPN [empfiehlt](https://protonvpn.com/blog/wireguard/) die Verwendung von WireGuard mit ihrem Dienst. In den Windows-, macOS-, iOS-, Android-, ChromeOS- und Android TV-Apps von Proton VPN ist WireGuard das Standardprotokoll; die Linux-App von Proton VPN [unterstützt](https://protonvpn.com/support/how-to-change-vpn-protocols/) das Protokoll jedoch nicht.

#### :material-alert-outline:{ .pg-orange } Remote Portweiterleitung

Proton VPN unterstützt derzeit nur vorrübergehende [Remote-Port-Weiterleitung](https://protonvpn.com/support/port-forwarding/) über NAT-PMP, mit 60 Sekunden Bestandszeit. Die Windows-App bietet eine leicht zugängliche Option dafür, während Sie auf anderen Betriebssystemen Ihren eigenen [NAT-PMP-Klient](https://protonvpn.com/support/port-forwarding-manual-setup/)ausführen müssen. Torrent-Anwendungen unterstützen oft NAT-PMP von Haus aus.

#### :material-check:{ .pg-green } Mobile Anwendungen

Zusätzlich zu den Standard-OpenVPN-Konfigurationsdateien bietet Proton VPN mobile Apps für [App Store](https://apps.apple.com/us/app/protonvpn-fast-secure-vpn/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android&hl=en_US)und [GitHub](https://github.com/ProtonVPN/android-app/releases) an, die eine einfache Verbindung zu ihren Servern ermöglichen.

#### :material-information-outline:{ .pg-blue } Zusätzliche Funktionalität

Proton VPN Clients unterstützen Zwei-Faktor-Authentifizierung auf allen Plattformen außer Linux. Proton VPN hat eigene Server und Rechenzentren in der Schweiz, Island und Schweden. Sie bieten mit ihrem DNS-Dienst die Möglichkeit, Werbung und Schadware zu blockieren. Darüber hinaus bietet Proton VPN auch "Tor"-Server an, die es dir ermöglichen, sich problemlos mit Onion-Seiten zu verbinden. Wir empfehlen jedoch dringend, zu diesem Zweck [den offiziellen Tor-Browser](https://www.torproject.org/) zu verwenden.

#### :material-alert-outline:{ .pg-orange } Killswitch-Funktion ist auf Intel-basierten Macs defekt

Systemabstürze [können](https://protonvpn.com/support/macos-t2-chip-kill-switch/) auf Intel-basierten Macs auftreten, wenn der VPN-Killswitch verwendet wird. Wenn du diese Funktion benötigst und einen Mac mit Intel-Chipsatz verwendest, solltest du einen anderen VPN-Dienst nutzen.

### IVPN

!!! recommendation

    ![IVPN logo](assets/img/vpn/ivpn.svg){ align=right }
    
    **IVPN** ist ein weiterer Premium-VPN-Anbieter und ist seit 2009 aktiv. IVPN hat den Sitz in Gibraltar.
    
    [:octicons-home-16: Homepage](https://www.ivpn.net/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.ivpn.net/privacy/){ .card-link title="Datenschutzrichtlinie" }
    [:octicons-info-16:](https://www.ivpn.net/knowledgebase/general/){ .card-link title=Dokumentation}
    [:octicons-code-16:](https://github.com/ivpn){ .card-link title="Quellcode" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
        - [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
        - [:simple-appstore: App Store](https://apps.apple.com/app/ivpn-serious-privacy-protection/id1193122683)
        - [:simple-windows11: Windows](https://www.ivpn.net/apps-windows/)
        - [:simple-apple: macOS](https://www.ivpn.net/apps-macos/)
        - [:simple-linux: Linux](https://www.ivpn.net/apps-linux/)

#### :material-check:{ .pg-green } 35 Länder

IVPN hat [Server in 35 Ländern](https://www.ivpn.net/server-locations).(1) Die Wahl eines VPN-Anbieters mit einem Server in deiner Nähe verringert die Latenz des von dir gesendeten Netzwerkverkehrs. Der Grund dafür ist eine kürzere Route (weniger Sprünge) zum Ziel.
{ .annotate }

1. Stand: 2022-09-16

Wir sind außerdem der Meinung, dass es für die Sicherheit der privaten Schlüssel des VPN-Anbieters besser ist, wenn er [dedizierte Server](https://en.wikipedia.org/wiki/Dedicated_hosting_service) verwendet, anstatt billigere gemeinsame Lösungen (mit anderen Kunden) wie [virtuelle private Server](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Unabhängig geprüft

IVPN hat sich einem [No-Logging-Audit von Cure53](https://cure53.de/audit-report_ivpn.pdf) unterzogen, das die Behauptung von IVPN, dass kein Logging stattfindet, bestätigte. IVPN hat auch einen [umfassenden Pentestbericht von Cure53](https://cure53.de/summary-report_ivpn_2019.pdf) vom Januar 2020. IVPN hat außerdem angekündigt, dass es in Zukunft [Jahresberichte](https://www.ivpn.net/blog/independent-security-audit-concluded) geben wird. Eine weitere Überprüfung wurde [im April 2022](https://www.ivpn.net/blog/ivpn-apps-security-audit-2022-concluded/) durchgeführt und von Cure53 [auf deren Website](https://cure53.de/pentest-report_IVPN_2022.pdf) veröffentlicht.

#### :material-check:{ .pg-green } Open-Source Anwendungen

Ab Februar 2020 sind [IVPN-Anwendungen quelloffen](https://www.ivpn.net/blog/ivpn-applications-are-now-open-source). Der Quellcode kann von ihrer [GitHub Organisation](https://github.com/ivpn) bezogen werden.

#### :material-check:{ .pg-green } Akzeptiert Bargeld und Monero

Neben Kredit-/Debitkarten und PayPal akzeptiert IVPN auch Bitcoin, **Monero** und **Bargeld** (bei Jahresplänen) als anonyme Zahlungsmittel.

#### :material-check:{ .pg-green } WireGuard-Unterstützung

IVPN unterstützt das WireGuard®-Protokoll. [WireGuard](https://www.wireguard.com) ist ein neueres Protokoll, das modernste [Kryptographie](https://www.wireguard.com/protocol/) verwendet. Darüber hinaus zielt WireGuard darauf ab, einfacher und leistungsfähiger zu sein.

IVPN [empfiehlt](https://www.ivpn.net/wireguard/) die Verwendung von WireGuard mit seinem Service, daher ist das Protokoll die Standardeinstellung für alle IVPN-Apps. IVPN bietet auch einen WireGuard-Konfigurationsgenerator zur Verwendung mit den [offiziellen WireGuard-Apps](https://www.wireguard.com/install/) an.

#### :material-alert-outline:{ .pg-orange } Remote Portweiterleitung

IVPN unterstützte früher die Portweiterleitung, entfernte diese Option aber im [Juni 2023](https://www.ivpn.net/blog/gradual-removal-of-port-forwarding). Das Fehlen dieser Funktion könnte sich negativ auf bestimmte Anwendungen auswirken, insbesondere auf Peer-to-Peer-Anwendungen wie Torrent-Clients.

#### :material-check:{ .pg-green } Mobile Anwendungen

Zusätzlich zu den Standard-OpenVPN-Konfigurationsdateien bietet IVPN mobile Clients für [App Store](https://apps.apple.com/us/app/ivpn-serious-privacy-protection/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)und [GitHub](https://github.com/ivpn/android-app/releases) an, die eine einfache Verbindung zu ihren Servern ermöglichen.

#### :material-information-outline:{ .pg-blue } Zusätzliche Funktionalität

IVPN-Clients unterstützen Zwei-Faktor-Authentifizierung (die Clients von Mullvad nicht). IVPN bietet auch die Funktion "[AntiTracker](https://www.ivpn.net/antitracker)", die Werbenetzwerke und Tracker auf der Netzwerkebene blockiert.

### Mullvad

!!! recommendation

    ![Mullvad logo](assets/img/vpn/mullvad.svg){ align=right }
    
    **Mullvad** ist ein schnelles und preiswertes VPN mit einem ernsthaften Fokus auf Transparenz und Sicherheit. Mullvad ist seit **2009** in Betrieb. Mullvad ist in Schweden ansässig und bietet keine kostenlose Testversion an.
    
    [:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Dienst" }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Datenschutzrichtlinie" }
    [:octicons-info-16:](https://mullvad.net/en/help/){ .card-link title=Dokumentation}
    [:octicons-code-16:](https://github.com/mullvad){ .card-link title="Quellcode" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
        - [:simple-appstore: App Store](https://apps.apple.com/app/mullvad-vpn/id1488466513)
        - [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
        - [:simple-windows11: Windows](https://mullvad.net/en/download/windows/)
        - [:simple-apple: macOS](https://mullvad.net/en/download/macos/)
        - [:simple-linux: Linux](https://mullvad.net/en/download/linux/)

#### :material-check:{ .pg-green } 41 Länder

Mullvad hat [Server in 41 Ländern](https://mullvad.net/servers/).(1) Die Wahl eines VPN-Anbieters mit einem Server in deiner Nähe verringert die Latenz des von dir gesendeten Netzwerkverkehrs. Der Grund dafür ist eine kürzere Route (weniger Sprünge) zum Ziel.
{ .annotate }

1. Stand: 2023-01-19

Wir sind außerdem der Meinung, dass es für die Sicherheit der privaten Schlüssel des VPN-Anbieters besser ist, wenn er [dedizierte Server](https://en.wikipedia.org/wiki/Dedicated_hosting_service) verwendet, anstatt billigere gemeinsame Lösungen (mit anderen Kunden) wie [virtuelle private Server](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Unabhängig geprüft

Die VPN-Clients von Mullvad wurden von Cure53 und Assured AB in einem Pentestbericht [geprüft, der auf cure53.de](https://cure53.de/pentest-report_mullvad_v2.pdf) auditiert. Die Sicherheitsforscher kamen zu dem Schluss:

> Cure53 und Assured AB sind mit den Ergebnissen des Audits zufrieden und die Software hinterlässt einen insgesamt positiven Eindruck. Dank des Engagements des internen Teams von Mullvad VPN haben die Tester keine Zweifel daran, dass das Projekt in puncto Sicherheit auf dem richtigen Weg ist.

Im Jahr 2020 wurde ein zweites Audit [angekündigt](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app/) und der [Abschlussbericht](https://cure53.de/pentest-report_mullvad_2020_v2.pdf) wurde auf der Webseite von Cure53 veröffentlicht:

> Die Ergebnisse dieses Mai-Juni 2020-Projekts, das auf den Mullvad-Komplex abzielt, sind recht positiv. [...] Das Gesamte von Mullvad verwendete Anwendungsökosystem hinterlässt einen soliden und strukturierten Eindruck. Die Gesamtstruktur der Anwendung macht es einfach, Patches und Korrekturen auf strukturierte Weise auszuführen. Die von Cure53 festgestellten Ergebnisse zeigen vor allem, wie wichtig es ist, die aktuellen Leckvektoren ständig zu überprüfen und neu zu bewerten, um die Privatsphäre der Endnutzer stets zu gewährleisten. In diesem Sinne leistet Mullvad gute Arbeit beim Schutz des Endbenutzers vor allgemeinen PII-Lecks und datenschutzbezogenen Risiken.

Im Jahr 2021 wurde ein Infrastruktur-Audit [angekündigt](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit/) und der [Abschlussbericht](https://cure53.de/pentest-report_mullvad_2021_v1.pdf) wurde auf der Webseite von Cure53 veröffentlicht. Ein weiterer Bericht wurde [im Juni 2022](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data/) in Auftrag gegeben und ist auf der [Webseite von Assured](https://www.assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf)verfügbar.

#### :material-check:{ .pg-green } Open-Source Anwendungen

Mullvad stellt den Quellcode für seine Desktop- und mobilen Clients in seiner [GitHub-Organisation](https://github.com/mullvad/mullvadvpn-app)zur Verfügung.

#### :material-check:{ .pg-green } Akzeptiert Bargeld und Monero

Mullvad akzeptiert nicht nur Kredit-/Debitkarten und PayPal, sondern auch Bitcoin, Bitcoin Cash, **Monero** und **Bargeld/lokale Währung** als anonyme Zahlungsmittel. Sie akzeptieren auch Swish- und Banküberweisungen.

#### :material-check:{ .pg-green } WireGuard-Unterstützung

Mullvad unterstützt das WireGuard®-Protokoll. [WireGuard](https://www.wireguard.com) ist ein neueres Protokoll, das modernste [Kryptographie](https://www.wireguard.com/protocol/) verwendet. Darüber hinaus zielt WireGuard darauf ab, einfacher und leistungsfähiger zu sein.

Mullvad [empfiehlt](https://mullvad.net/en/help/why-wireguard/) die Verwendung von WireGuard mit ihrem Dienst. Es ist das Standardprotokoll oder das einzige Protokoll in den Android-, iOS-, macOS- und Linux-Apps von Mullvad, aber unter Windows musst du WireGuard [manuell aktivieren](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app/). Mullvad bietet auch einen WireGuard-Konfigurationsgenerator zur Verwendung mit den offiziellen [WireGuard-Apps](https://www.wireguard.com/install/).

#### :material-check:{ .pg-green } IPv6-Unterstützung

Mit Mullvad kannst du [auf Dienste zugreifen, die mit IPv6 gehostet werden](https://mullvad.net/en/blog/2014/9/15/ipv6-support/), im Gegensatz zu anderen Anbietern, die IPv6-Verbindungen blockieren.

#### :material-alert-outline:{ .pg-orange } Remote Portweiterleitung

Mullvad unterstützte früher Portweiterleitung, entfernte diese Möglichkeit aber in [Mai 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports/). Das Fehlen dieser Funktion könnte sich negativ auf bestimmte Anwendungen auswirken, insbesondere auf Peer-to-Peer-Anwendungen wie Torrent-Clients.

#### :material-check:{ .pg-green } Mobile Anwendungen

Mullvad hat [App Store](https://apps.apple.com/app/mullvad-vpn/id1488466513) und [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) Clients veröffentlicht, die beide eine einfach zu bedienende Benutzeroberfläche haben, anstatt dass du deine WireGuard-Verbindung manuell konfigurieren musst. Der Android-Client ist auch auf [GitHub](https://github.com/mullvad/mullvadvpn-app/releases) verfügbar.

#### :material-information-outline:{ .pg-blue } Zusätzliche Funktionalität

Mullvad ist sehr transparent darüber, welche Netzwerk-Knotenpunkte sie [besitzen oder mieten](https://mullvad.net/en/servers/). Sie verwenden [ShadowSocks](https://shadowsocks.org/) in ihrer ShadowSocks + OpenVPN-Konfiguration, was sie resistenter gegen Firewalls mit [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) macht, die versuchen, VPNs zu blockieren. Angeblich muss [China eine andere Methode verwenden, um ShadowSocks-Server zu blockieren](https://github.com/net4people/bbs/issues/22). Die Website von Mullvad ist auch über Tor zugänglich: [o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion).

## Kriterien

!!! !!! danger "Achtung"

    Es ist wichtig zu wissen, dass die Nutzung eines VPN-Anbieters dich nicht anonym macht, aber in bestimmten Situationen einen besseren Datenschutz bietet. Ein VPN ist kein Werkzeug für illegale Aktivitäten. Verlasse dich nicht auf "no Log" Richtlienen.

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, verbunden sind. Dies ermöglicht es uns, völlig objektive Empfehlungen zu geben.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen für alle VPN-Anbieter*innen entwickelt, die empfohlen werden wollen, darunter starke Verschlüsselung, unabhängige Sicherheitsprüfungen, moderne Technologie und mehr. Wir empfehlen dir, dich mit dieser Liste vertraut zu machen, bevor du dich für einen VPN-Anbieter entscheidest, und deine eigenen Nachforschungen anstellst, um sicherzustellen, dass der von dir gewählte VPN-Anbieter so vertrauenswürdig wie möglich ist.

### Technologie

Wir setzen von allen von uns empfohlenen VPN-Anbietern voraus, dass sie OpenVPN-Konfigurationsdateien zur Verfügung stellen, die in jedem Client verwendet werden können. **Wenn** ein eigener VPN-Client bereitstellt wird, benötigt er einen Killswitch, um Datenlecks im Netzwerk zu blockieren, wenn die Verbindung getrennt wird.

**Mindestvoraussetzung um zu qualifizieren:**

- Unterstützung von starken Protokollen wie WireGuard & OpenVPN.
- Notaus ist in den Clients integriert.
- Multihop-Unterstützung. Multihopping ist wichtig, um Daten im Falle einer Kompromittierung eines einzelnen Knotens geheim zu halten.
- Wenn VPN-Clients zur Verfügung gestellt werden, sollten sie [Open Source](https://de.wikipedia.org/wiki/Open_Source)sein, wie die VPN-Software, die in der Regel in sie integriert ist. Wir sind der Meinung, dass [Quellcode](https://de.wikipedia.org/wiki/Quelltext) mehr Transparenz darüber bietet, was dein Gerät tatsächlich tut.

**Im besten Fall:**

- Unterstützung von WireGuard und OpenVPN.
- Notaus mit hochgradig konfigurierbaren Optionen (Aktivierung/Deaktivierung in bestimmten Netzen, beim Booten usw.)
- Einfach zu bedienende VPN-Clients
- Unterstützt [IPv6](https://de.wikipedia.org/wiki/IPv6). Wir erwarten, dass die Server eingehende Verbindungen über IPv6 zulassen und dir den Zugang zu Diensten ermöglichen, die auf IPv6-Adressen gehostet werden.
- Die Möglichkeit der [Remote-Port-Weiterleitung](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) hilft bei der Herstellung von Verbindungen bei der Verwendung von P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) Dateitauschbörsen-Software zum Austausch von Dateien oder zum Hosten eines Servers (z. B. Mumble).

### Datenschutz

Wir ziehen es vor, dass die von uns empfohlenen Anbieter*innen so wenig Daten wie möglich sammeln. Der Verzicht auf die Erhebung personenbezogener Daten bei der Anmeldung und die Annahme anonymer Zahlungsformen sind erforderlich.

**Mindestvoraussetzung um zu qualifizieren:**

- [Anonyme Kryptowährung](cryptocurrency.md) **oder** Barzahlung möglich.
- Für die Registrierung sind keine persönlichen Daten erforderlich: Höchstens Benutzername, Passwort und E-Mail.

**Im besten Fall:**

- Akzeptiert mehrere [anonyme Zahlungsmöglichkeiten](advanced/payments.md).
- Es werden keine persönlichen Informationen akzeptiert (automatisch generierter Benutzername, keine E-Mail erforderlich, usw.).

### Sicherheit

Ein VPN ist sinnlos, wenn es nicht einmal angemessene Sicherheit bieten kann. Wir setzen für all von uns empfohlenen Anbietern voraus, dass sie die aktuellen Sicherheitsstandards für ihre OpenVPN-Verbindungen einhalten. Idealerweise würden sie standardmäßig zukunftssichere Verschlüsselungsverfahren verwenden. Wir setzen auch voraus, dass ein unabhängiger Dritter die Sicherheit des Anbieters überprüft, idealerweise sehr umfassend und wiederholt (jährlich).

**Mindestvoraussetzung um zu qualifizieren:**

- Starke Verschlüsselungsschemata: OpenVPN mit SHA-256-Authentifizierung; RSA-2048 oder besserer Handshake; AES-256-GCM oder AES-256-CBC Datenverschlüsselung.
- Forward Secrecy (vorwärts gerichtete Geheimhaltung).
- Veröffentlichte Sicherheitsaudits durch ein angesehenes Drittunternehmen.

**Im besten Fall:**

- Stärkste Verschlüsselung: RSA-4096.
- Forward Secrecy (vorwärts gerichtete Geheimhaltung).
- Umfassende veröffentlichte Sicherheitsaudits durch ein angesehenes Drittunternehmen.
- Bug-Bounty-Programme und/oder ein koordiniertes Verfahren zur Offenlegung von Sicherheitslücken.

### Vertrauen

Du würdest nicht jemandem mit einer gefälschten Identität deine Finanzen anvertrauen, warum solltest du ihm also deine Internetdaten anvertrauen? Wir setzen für die von uns empfohlenen Anbietern voraus, dass sie ihre Eigentumsverhältnisse oder ihre Führungsrolle öffentlich gemacht haben. Außerdem wünschen wir uns häufige Transparenzberichte, insbesondere über die Bearbeitung von Regierungsanfragen.

**Mindestvoraussetzung um zu qualifizieren:**

- Öffentliche Führungs- oder Eigentumsverhältnisse.

**Im besten Fall:**

- Öffentliche Führung.
- Häufige Transparenzberichte.

### Marketing

Bei den von uns empfohlenen VPN-Anbietern legen wir Wert auf ein verantwortungsvolles Marketing.

**Mindestvoraussetzung um zu qualifizieren:**

- Sie müssen die Analysen selbst hosten (d. h. kein Google Analytics). Die Website des Anbieters muss auch die Anforderungen von [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) für Personen erfüllen, die das möchten.

Es darf kein Marketing geben, das unverantwortlich ist:

- Versprechung eines 100%-igen Schutzes der Anonymität. Wenn jemand behauptet, etwas sei zu 100% sicher, bedeutet das, dass es keine Möglichkeit für ein Scheitern gibt. Wir wissen, dass Menschen sich auf verschiedene Weise recht einfach deanonymisieren können, z. B.:
    - Wiederverwendung persönlicher Informationen (z. B. E-Mail-Konten, eindeutige Pseudonyme usw.), auf die sie ohne Anonymisierungssoftware (Tor, VPN usw.) zugegriffen haben
    - [Browser-Fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Behauptung, dass ein VPN mit einer einzigen Verbindung "anonymer" ist als Tor, das eine Verbindung mit drei oder mehr Sprüngen ist, die sich regelmäßig ändert.
- Verwendet eine verantwortungsbewusste Sprache: Es ist in Ordnung zu sagen, dass ein VPN "getrennt" oder "nicht verbunden" ist, aber zu behaupten, dass jemand "gefährdet", "angreifbar" oder "kompromittiert" ist, ist ein unnötiger Gebrauch von alarmierenden Worten, die möglicherweise nicht korrekt sind. Diese Person könnte zum Beispiel einfach den Dienst eines anderen VPN-Anbieters nutzen oder Tor verwenden.

**Im besten Fall:**

Verantwortungsbewusstes Marketing, das sowohl lehrreich als auch nützlich für den Verbraucher ist, könnte Folgendes beinhalten:

- Ein genauer Vergleich zu [Tor](tor.md) sollte stattdessen verwendet werden.
- Verfügbarkeit der Website des VPN-Anbieters über einen [.onion-Dienst](https://en.wikipedia.org/wiki/.onion)

### Zusätzliche Funktionalitäten

Obwohl es dafür keine strikten Anforderungen gibt, gibt es einige Faktoren, die wir geprüft haben, um zu ermitteln, welche Anbieter zu empfehlen sind. Dazu gehören Ad-/Tracker-Blocking-Funktionen, Warrant Canaries, Multihop-Verbindungen, ein ausgezeichneter Kundendienst, die Anzahl der zulässigen gleichzeitigen Verbindungen usw.
