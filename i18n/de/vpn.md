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

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support/), as opposed to other providers which block IPv6 connections.

#### :material-alert-outline:{ .pg-orange } Remote Portweiterleitung

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports/). Das Fehlen dieser Funktion könnte sich negativ auf bestimmte Anwendungen auswirken, insbesondere auf Peer-to-Peer-Anwendungen wie Torrent-Clients.

#### :material-check:{ .pg-green } Mobile Anwendungen

Mullvad has published [App Store](https://apps.apple.com/app/mullvad-vpn/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Zusätzliche Funktionalität

Mullvad is very transparent about which nodes they [own or rent](https://mullvad.net/en/servers/). They use [ShadowSocks](https://shadowsocks.org/) in their ShadowSocks + OpenVPN configuration, making them more resistant against firewalls with [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) trying to block VPNs. Supposedly, [China has to use a different method to block ShadowSocks servers](https://github.com/net4people/bbs/issues/22). Mullvad's website is also accessible via Tor at [o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion).

## Kriterien

!!! danger

    It is important to note that using a VPN provider will not make you anonymous, but it will give you better privacy in certain situations. Ein VPN ist kein Werkzeug für illegale Aktivitäten. Verlasse dich nicht auf "no Log" Richtlienen.

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, verbunden sind. Dies ermöglicht es uns, völlig objektive Empfehlungen zu geben.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen für alle VPN-Anbieter*innen entwickelt, die empfohlen werden wollen, darunter starke Verschlüsselung, unabhängige Sicherheitsprüfungen, moderne Technologie und mehr. We suggest you familiarize yourself with this list before choosing a VPN provider, and conduct your own research to ensure the VPN provider you choose is as trustworthy as possible.

### Technologie

We require all our recommended VPN providers to provide OpenVPN configuration files to be used in any client. **If** a VPN provides their own custom client, we require a killswitch to block network data leaks when disconnected.

**Mindestvoraussetzung um zu qualifizieren:**

- Unterstützung von starken Protokollen wie WireGuard & OpenVPN.
- Notaus ist in den Clients integriert.
- Multihop-Unterstützung. Multihopping ist wichtig, um Daten im Falle einer Kompromittierung eines einzelnen Knotens geheim zu halten.
- Wenn VPN-Clients zur Verfügung gestellt werden, sollten sie [Open Source](https://de.wikipedia.org/wiki/Open_Source)sein, wie die VPN-Software, die in der Regel in sie integriert ist. Wir sind der Meinung, dass [Quellcode](https://de.wikipedia.org/wiki/Quelltext) mehr Transparenz darüber bietet, was dein Gerät tatsächlich tut.

**Best Case:**

- Unterstützung von WireGuard und OpenVPN.
- Notaus mit hochgradig konfigurierbaren Optionen (Aktivierung/Deaktivierung in bestimmten Netzen, beim Booten usw.)
- Einfach zu bedienende VPN-Clients
- Unterstützt [IPv6](https://de.wikipedia.org/wiki/IPv6). Wir erwarten, dass die Server eingehende Verbindungen über IPv6 zulassen und dir den Zugang zu Diensten ermöglichen, die auf IPv6-Adressen gehostet werden.
- Capability of [remote port forwarding](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) assists in creating connections when using P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) file sharing software or hosting a server (e.g., Mumble).

### Datenschutz

Wir ziehen es vor, dass die von uns empfohlenen Anbieter*innen so wenig Daten wie möglich sammeln. Der Verzicht auf die Erhebung personenbezogener Daten bei der Anmeldung und die Annahme anonymer Zahlungsformen sind erforderlich.

**Mindestvoraussetzung um zu qualifizieren:**

- [Anonymous cryptocurrency](cryptocurrency.md) **or** cash payment option.
- Für die Registrierung sind keine persönlichen Daten erforderlich: Höchstens Benutzername, Passwort und E-Mail.

**Best Case:**

- Accepts multiple [anonymous payment options](advanced/payments.md).
- No personal information accepted (autogenerated username, no email required, etc.).

### Sicherheit

A VPN is pointless if it can't even provide adequate security. We require all our recommended providers to abide by current security standards for their OpenVPN connections. Ideally, they would use more future-proof encryption schemes by default. We also require an independent third-party to audit the provider's security, ideally in a very comprehensive manner and on a repeated (yearly) basis.

**Mindestvoraussetzung um zu qualifizieren:**

- Strong Encryption Schemes: OpenVPN with SHA-256 authentication; RSA-2048 or better handshake; AES-256-GCM or AES-256-CBC data encryption.
- Forward Secrecy.
- Published security audits from a reputable third-party firm.

**Best Case:**

- Strongest Encryption: RSA-4096.
- Forward Secrecy.
- Comprehensive published security audits from a reputable third-party firm.
- Bug-bounty programs and/or a coordinated vulnerability-disclosure process.

### Vertrauen

You wouldn't trust your finances to someone with a fake identity, so why trust them with your internet data? We require our recommended providers to be public about their ownership or leadership. We also would like to see frequent transparency reports, especially in regard to how government requests are handled.

**Mindestvoraussetzung um zu qualifizieren:**

- Public-facing leadership or ownership.

**Best Case:**

- Public-facing leadership.
- Frequent transparency reports.

### Marketing

With the VPN providers we recommend we like to see responsible marketing.

**Mindestvoraussetzung um zu qualifizieren:**

- Must self-host analytics (i.e., no Google Analytics). The provider's site must also comply with [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) for people who want to opt-out.

Must not have any marketing which is irresponsible:

- Making guarantees of protecting anonymity 100%. When someone makes a claim that something is 100% it means there is no certainty for failure. We know people can quite easily deanonymize themselves in a number of ways, e.g.:
    - Reusing personal information (e.g., email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
    - [Browser fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Claim that a single circuit VPN is "more anonymous" than Tor, which is a circuit of three or more hops that regularly changes.
- Use responsible language: i.e., it is okay to say that a VPN is "disconnected" or "not connected", however claiming that someone is "exposed", "vulnerable" or "compromised" is needless use of alarming language that may be incorrect. For example, that person might simply be on another VPN provider's service or using Tor.

**Best Case:**

Responsible marketing that is both educational and useful to the consumer could include:

- An accurate comparison to when [Tor](tor.md) should be used instead.
- Availability of the VPN provider's website over a [.onion service](https://en.wikipedia.org/wiki/.onion)

### Zusätzliche Funktionalitäten

While not strictly requirements, there are some factors we looked into when determining which providers to recommend. These include adblocking/tracker-blocking functionality, warrant canaries, multihop connections, excellent customer support, the number of allowed simultaneous connections, etc.
