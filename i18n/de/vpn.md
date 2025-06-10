---
meta_title: "Private VPN-Anbieter Empfehlungen und Vergleiche, kein Sponsoring und keine Werbung - Privacy Guides"
title: "VPN Anbieter"
icon: material/vpn
description: Die besten VPN-Anbieter zum Schutz deiner Privatsphäre und Sicherheit im Internet. Hier findest du einen Anbieter, der nicht darauf aus ist, dich auszuspionieren.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-account-cash: Überwachungskapitalismus](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Wenn du zusätzliche *Privatsphäre* vor deinem ISP, in einem öffentlichen Wi-Fi-Netzwerk oder beim Herunterladen von Dateien über Torrents benötigst, könnte ein **VPN** die Lösung für dich sein.

<div class="admonition danger" markdown>
<p class="admonition-title">VPNs bieten keine Anonymität</p>

Mit einem VPN bleiben deine Surfgewohnheiten **nicht** anonym, und es bietet auch keine zusätzliche Sicherheit für unsicheren (HTTP) Verkehr.

Wenn du auf der Suche nach **Anonymität** bist, solltest du den Tor-Browser verwenden. Wenn du auf der Suche nach zusätzlicher **Sicherheit** bist, solltest du immer sicherstellen, dass du eine Verbindung zu Websites über HTTPS herstellst. Ein VPN ist kein Ersatz für gute Sicherheitspraktiken.

[Tor herunterladen](https://torproject.org){ .md-button .md-button--primary } [Tor Mythen & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Detaillierte VPN-Übersicht :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Empfohlene Anbieter

Die von uns empfohlenen Anbieter verwenden Verschlüsselung, unterstützen WireGuard & OpenVPN und haben eine No-Logging-Politik. Weitere Informationen findest du in unserem [vollständigen Kriterienkatalog](#criteria).

| Anbieter              | Länder | WireGuard                     | Port-Weiterleitung                                           | IPv6                                                                    | Anonyme Zahlungen |
| --------------------- | ------ | ----------------------------- | ------------------------------------------------------------ | ----------------------------------------------------------------------- | ----------------- |
| [Proton](#proton-vpn) | 112+   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Teilweise unterstützt | :material-information-outline:{ .pg-blue } Eingeschränkte Unterstützung | Bargeld           |
| [IVPN](#ivpn)         | 37+    | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                       | :material-information-outline:{ .pg-blue } Nur ausgehend                | Monero, Bargeld   |
| [Mullvad](#mullvad)   | 49+    | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                       | :material-check:{ .pg-green }                                           | Monero, Bargeld   |

### Proton VPN

<div class="admonition recommendation" markdown>

![Proton VPN logo](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** ist ein starker Anwärter im VPN-Bereich und ist seit 2016 in Betrieb. Die Proton AG hat ihren Sitz in der Schweiz und bietet sowohl eine begrenzte kostenlose als auch eine umfangreichere Premium-Option an.

[:octicons-home-16: Homepage](https://protonvpn.com/de){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/de/privacy-policy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://protonvpn.com/support/de){ .card-link title=Dokumentation}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Quellcode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://protonvpn.com/download-windows)
- [:simple-apple: macOS](https://protonvpn.com/download-macos)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 112 Länder

Proton VPN hat [Server in 112 Ländern](https://protonvpn.com/vpn-servers) bzw. [5](https://protonvpn.com/support/how-to-create-free-vpn-account) Server, wenn du die [kostenlose Version nutzt](https://protonvpn.com/free-vpn/server).(1) Die Auswahl eines VPN-Anbieters mit einem Server in deiner Nähe verringert die Latenz des von dir gesendeten Netzwerkverkehrs. Der Grund dafür ist eine kürzere Route (weniger Sprünge) zum Ziel.
{ .annotate }

1. Stand: 2024-08-06

Wir sind außerdem der Meinung, dass es für die Sicherheit der privaten Schlüssel des VPN-Anbieters besser ist, wenn er [dedizierte Server](https://en.wikipedia.org/wiki/Dedicated_hosting_service) verwendet, anstatt billigere gemeinsame Lösungen (mit anderen Kunden) wie [virtuelle private Server](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Unabhängig geprüft

Im Januar 2020 hat sich Proton VPN einem unabhängigen Audit durch SEC Consult unterzogen. SEC Consult fand einige Sicherheitslücken mit mittlerem und niedrigem Risiko in den Windows-, Android- und iOS-Anwendungen von Proton VPN, die alle von Proton VPN vor der Veröffentlichung der Berichte "ordnungsgemäß behoben" wurden. Keines der festgestellten Probleme hätte angreifenden Fernzugriff auf dein Gerät oder deinen Datenverkehr ermöglicht. Du kannst individuelle Berichte für jede Plattform unter [protonvpn.com](https://protonvpn.com/blog/open-source) einsehen. Im April 2022 wurde Proton VPN einem [weiteren Audit](https://protonvpn.com/blog/no-logs-audit) unterzogen. Eine [Bescheinigung](https://proton.me/blog/security-audit-all-proton-apps) wurde am 9. November 2021 von [Securitum](https://research.securitum.com) für die Apps von Proton VPN ausgestellt.

#### :material-check:{ .pg-green } Open-Source Anwendungen

Proton VPN stellt den Quellcode für seine Desktop- und mobilen Clients in seiner [GitHub Organisation](https://github.com/ProtonVPN)zur Verfügung.

#### :material-check:{ .pg-green } Akzeptiert Bargeld

Proton VPN akzeptiert nicht nur Kredit-/Debitkarten, PayPal und [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), sondern auch **Bargeld/lokale Währung** als anonyme Zahlungsform.

#### :material-check:{ .pg-green } WireGuard-Unterstützung

Proton VPN unterstützt das WireGuard®-Protokoll. [WireGuard](https://wireguard.com) ist ein neueres Protokoll, das modernste [Kryptographie](https://wireguard.com/protocol) verwendet. Darüber hinaus zielt WireGuard darauf ab, einfacher und leistungsfähiger zu sein.

Proton VPN [empfiehlt](https://protonvpn.com/blog/wireguard) die Verwendung von WireGuard mit ihrem Dienst. Proton VPN bietet auch einen WireGuard-Konfigurationsgenerator zur Verwendung mit den offiziellen WireGuard-[Apps](https://wireguard.com/install) an.

#### :material-alert-outline:{ .pg-orange } Eingeschränkte IPv6 Unterstützung

Proton [now supports IPv6](https://protonvpn.com/support/prevent-ipv6-vpn-leaks) in their browser extension and Linux client, but only 80% of their servers are IPv6-compatible. Auf anderen Plattformen blockiert der Proton VPN-Client den gesamten ausgehenden IPv6-Verkehr, so dass du dir keine Sorgen machen musst, dass deine IPv6-Adresse ausspioniert wird, aber du kannt dich weder mit reinen IPv6-Websites verbinden, noch dich von einem reinen IPv6-Netzwerk aus mit Proton VPN verbinden.

#### :material-information-outline:{ .pg-info } Remote Portweiterleitung

Proton VPN unterstützt derzeit nur vorrübergehende [Remote-Port-Weiterleitung](https://protonvpn.com/support/port-forwarding) über NAT-PMP, mit 60 Sekunden Bestandszeit. The official Windows and Linux apps provide an easy-to-access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup). Torrent-Anwendungen unterstützen oft NAT-PMP von Haus aus.

#### :material-information-outline:{ .pg-blue } Anti-Zensur

Proton VPN hat sein [Stealth-Protokoll](https://protonvpn.com/blog/stealth-vpn-protocol), das in Situationen helfen *kann*, in denen VPN-Protokolle wie OpenVPN oder WireGuard mit verschiedenen, rudimentären Techniken blockiert werden. Stealth kapselt den VPN-Tunnel in eine TLS-Sitzung ein, damit er mehr wie normaler Internetverkehr aussieht.

Leider funktioniert das nicht sehr gut in Ländern, in denen ausgeklügelte Filter eingesetzt werden, die den gesamten ausgehenden Datenverkehr analysieren und versuchen, verschlüsselte Tunnel zu entdecken. Stealth ist für Android, iOS, Windows und macOS verfügbar, aber noch nicht für Linux.

#### :material-check:{ .pg-green } Mobile Anwendungen

Proton VPN has published [App Store](https://apps.apple.com/app/id1437005085) and [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/ProtonVPN/android-app/releases).

<div class="admonition warning" markdown>
<p class="admonition-title">How to opt out of sharing telemetry</p>

On Android, Proton hides telemetry settings under the misleadingly labeled "**Help us fight censorship**" menu in the settings panel. On other platforms these settings can be found under the "**Usage statistics**" menu.

We are noting this because while we don't necessarily recommend against sharing anonymous usage statistics with developers, it is important that these settings are easily found and clearly labeled.

</div>

#### :material-information-outline:{ .pg-blue } Zusätzliche Hinweise

Proton VPN Clients unterstützen Zwei-Faktor-Authentisierung auf allen Plattformen. Proton VPN hat eigene Server und Rechenzentren in der Schweiz, Island und Schweden. Sie bieten mit ihrem DNS-Dienst die Blockierung von Inhalten und bekannter Malware an. Darüber hinaus bietet Proton VPN auch "Tor"-Server an, die es dir ermöglichen, sich problemlos mit Onion-Seiten zu verbinden. Wir empfehlen jedoch dringend, zu diesem Zweck [den offiziellen Tor-Browser](tor.md#tor-browser) zu verwenden.

##### :material-alert-outline:{ .pg-orange } Die Kill-Switch-Funktion ist auf Intel-basierten Macs defekt

Systemabstürze [können](https://protonvpn.com/support/macos-t2-chip-kill-switch) auf Intel-basierten Macs auftreten, wenn der VPN-Kill-Switch verwendet wird. Wenn du diese Funktion benötigst und einen Mac mit Intel-Chipsatz verwendest, solltest du einen anderen VPN-Dienst nutzen.

### IVPN

<div class="admonition recommendation" markdown>

![IVPN logo](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** ist ein weiterer Premium-VPN-Anbieter und ist seit 2009 aktiv. IVPN hat seinen Sitz in Gibraltar und bietet keine kostenlose Testversion an.

[:octicons-home-16: Homepage](https://www.ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.ivpn.net/privacy){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://www.ivpn.net/knowledgebase/general){ .card-link title=Dokumentation}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Quellcode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-github: GitHub](https://github.com/ivpn/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 37 Länder

IVPN hat [Server in 37 Ländern](https://ivpn.net/status).(1) Die Wahl eines VPN-Anbieters mit einem Server in deiner Nähe verringert die Latenz des von dir gesendeten Netzwerkverkehrs. Der Grund dafür ist eine kürzere Route (weniger Sprünge) zum Ziel.
{ .annotate }

1. Stand: 2024-08-06

Wir sind außerdem der Meinung, dass es für die Sicherheit der privaten Schlüssel des VPN-Anbieters besser ist, wenn er [dedizierte Server](https://en.wikipedia.org/wiki/Dedicated_hosting_service) verwendet, anstatt billigere gemeinsame Lösungen (mit anderen Kunden) wie [virtuelle private Server](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Unabhängig geprüft

IVPN hat sich seit 2019 mehreren [unabhängigen Audits](https://ivpn.net/en/blog/tags/audit) unterzogen und hat öffentlich angekündigt, dass es sich zu [jährlichen Sicherheitsaudits](https://ivpn.net/blog/ivpn-apps-security-audit-concluded) verpflichtet.

#### :material-check:{ .pg-green } Open-Source-Clients

Seit Februar 2020 [sind die IVPN-Anwendungen nun quelloffen](https://ivpn.net/blog/ivpn-applications-are-now-open-source). Der Quellcode kann von ihrer [GitHub Organisation](https://github.com/ivpn) bezogen werden.

#### :material-check:{ .pg-green } Akzeptiert Bargeld und Monero

Neben Kredit-/Debitkarten und PayPal akzeptiert IVPN auch Bitcoin, **Monero** und **Bargeld/lokale Währungen** (bei Jahresplänen) als anonyme Zahlungsmittel. Prepaid-Karten mit einlösbaren Codes sind [auch verfügbar](https://ivpn.net/knowledgebase/billing/voucher-cards-faq).

#### :material-check:{ .pg-green } WireGuard-Unterstützung

IVPN unterstützt das WireGuard®-Protokoll. [WireGuard](https://wireguard.com) ist ein neueres Protokoll, das modernste [Kryptographie](https://wireguard.com/protocol) verwendet. Darüber hinaus zielt WireGuard darauf ab, einfacher und leistungsfähiger zu sein.

IVPN [empfiehlt die](https://ivpn.net/wireguard) Verwendung von WireGuard mit seinem Service und daher ist das Protokoll die Standardeinstellung für alle IVPN-Apps. IVPN bietet auch einen WireGuard-Konfigurationsgenerator zur Verwendung mit den [offiziellen WireGuard-Apps](https://wireguard.com/install) an.

#### :material-information-outline:{ .pg-blue } IPv6-Unterstützung

IVPN ermöglicht dir die [Verbindung zu Diensten, die IPv6 verwenden](https://ivpn.net/knowledgebase/general/do-you-support-ipv6), aber nicht die Verbindung von einem Gerät mit einer IPv6-Adresse.

#### :material-alert-outline:{ .pg-orange } Remote Portweiterleitung

IVPN unterstützte früher die Portweiterleitung, entfernte diese Option aber im [Juni 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). Das Fehlen dieser Funktion könnte sich negativ auf bestimmte Anwendungen auswirken, insbesondere auf Peer-to-Peer-Anwendungen wie Torrent-Clients.

#### :material-check:{ .pg-green } Anti-Zensur

IVPN has obfuscation modes using [V2Ray](https://v2ray.com/en/index.html) which helps in situations where VPN protocols like OpenVPN or WireGuard are blocked. Derzeit ist diese Funktion nur auf Desktop und [iOS](https://ivpn.net/knowledgebase/ios/v2ray) verfügbar. Sie verfügt über zwei Modi, in denen man [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) über QUIC- oder TCP-Verbindungen nutzen kann. QUIC ist ein modernes Protokoll mit besserer Staukontrolle und kann daher schneller sein und geringere Latenzzeiten aufweisen. Der TCP-Modus lässt deine Daten als normalen HTTP-Verkehr erscheinen.

#### :material-check:{ .pg-green } Mobile Anwendungen

IVPN has published [App Store](https://apps.apple.com/app/id1193122683) and [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/ivpn/android-app/releases).

#### :material-information-outline:{ .pg-blue } Zusätzliche Hinweise

IVPN-Clients unterstützen die Zwei-Faktor-Authentisierung. IVPN bietet auch die Funktion "[AntiTracker](https://ivpn.net/antitracker)", die Werbenetzwerke und Tracker auf der Netzwerkebene blockiert.

### Mullvad

<div class="admonition recommendation" markdown>

![Mullvad logo](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** ist ein schnelles und preiswertes VPN mit einem ernsthaften Fokus auf Transparenz und Sicherheit. Sie sind seit 2009 in Betrieb. Mullvad hat seinen Sitz in Schweden und bietet eine 14-tägige Geld-zurück-Garantie für [Zahlungsarten](https://mullvad.net/en/help/refunds), die dies zulassen.

[:octicons-home-16: Homepage](https://mullvad.net/de){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Dienst" }
[:octicons-eye-16:](https://mullvad.net/de/help/privacy-policy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://mullvad.net/de/help){ .card-link title=Dokumentation}
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Quellcode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 49 Countries

Mullvad has [servers in 49 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Der Grund dafür ist eine kürzere Route (weniger Sprünge) zum Ziel.
{ .annotate }

1. Last checked: 2025-03-10

Wir sind außerdem der Meinung, dass es für die Sicherheit der privaten Schlüssel des VPN-Anbieters besser ist, wenn er [dedizierte Server](https://en.wikipedia.org/wiki/Dedicated_hosting_service) verwendet, anstatt billigere gemeinsame Lösungen (mit anderen Kunden) wie [virtuelle private Server](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Unabhängig geprüft

Mullvad wurde mehrfach [von unabhängiger Seite geprüft](https://mullvad.net/en/blog/tag/audits) und hat öffentlich angekündigt, seine Anwendungen und seine Infrastruktur [jährlich auditieren](https://mullvad.net/en/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) zu wollen.

#### :material-check:{ .pg-green } Open-Source Anwendungen

Mullvad stellt den Quellcode für seine Desktop- und mobilen Clients in seiner [GitHub-Organisation](https://github.com/mullvad/mullvadvpn-app)zur Verfügung.

#### :material-check:{ .pg-green } Akzeptiert Bargeld und Monero

Mullvad akzeptiert nicht nur Kredit-/Debitkarten und PayPal, sondern auch Bitcoin, Bitcoin Cash, **Monero** und **Bargeld/lokale Währungen** als anonyme Zahlungsmittel. Prepaid-Karten mit einlösbaren Codes sind auch verfügbar. Mullvad akzeptiert auch Swish und Banküberweisungen, sowie einige europäische Zahlungssysteme.

#### :material-check:{ .pg-green } WireGuard-Unterstützung

Mullvad unterstützt das WireGuard®-Protokoll. [WireGuard](https://wireguard.com) ist ein neueres Protokoll, das modernste [Kryptographie](https://wireguard.com/protocol) verwendet. Darüber hinaus zielt WireGuard darauf ab, einfacher und leistungsfähiger zu sein.

Mullvad [empfiehlt](https://mullvad.net/en/help/why-wireguard) die Verwendung von WireGuard mit ihrem Dienst. Es ist das Standardprotokoll bzw. das einzige Protokoll in den Android-, iOS-, macOS- und Linux-Apps von Mullvad; unter Windows musst du WireGuard [manuell aktivieren](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app). Mullvad bietet auch einen WireGuard-Konfigurationsgenerator zur Verwendung mit den offiziellen [WireGuard-Apps](https://wireguard.com/install).

#### :material-check:{ .pg-green } IPv6-Unterstützung

Mit Mullvad kannst du [auf Dienste zugreifen, die auf IPv6 gehostet werden](https://mullvad.net/en/blog/2014/9/15/ipv6-support), und eine Verbindung von einem Gerät mit einer IPv6-Adresse herstellen.

#### :material-alert-outline:{ .pg-orange } Remote Portweiterleitung

Mullvad unterstützte früher die Portweiterleitung, entfernte diese Option jedoch im [Mai 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). Das Fehlen dieser Funktion könnte sich negativ auf bestimmte Anwendungen auswirken, insbesondere auf Peer-to-Peer-Anwendungen wie Torrent-Clients.

#### :material-check:{ .pg-green } Anti-Zensur

Mullvad bietet mehrere Funktionen, die dabei helfen, Zensur zu umgehen und frei auf das Internet zuzugreifen:

- **Obfuscation modes**: Mullvad has two built-in obfuscation modes: "UDP-over-TCP" and ["WireGuard over Shadowsocks"](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard). These modes disguise your VPN traffic as regular web traffic, making it harder for censors to detect and block. Supposedly, China has to use a [new method to disrupt Shadowsocks-routed traffic](https://gfw.report/publications/usenixsecurity23/en).
- **Advanced obfuscation with Shadowsocks and v2ray**: For more advanced users, Mullvad provides a guide on how to use the [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) plugin with Mullvad clients. This setup provides an additional layer of obfuscation and encryption.
- **Custom server IPs**: To counter IP-blocking, you can request custom server IPs from Mullvad's support team. Once you receive the custom IPs, you can input the text file in the "Server IP override" settings, which will override the chosen server IP addresses with ones that aren't known to the censor.
- **Bridges and proxies**: Mullvad also allows you to use bridges or proxies to reach their API (needed for authentication), which can help bypass censorship attempts that block access to the API itself.

#### :material-check:{ .pg-green } Mobile Anwendungen

Mullvad hat [App Store-](https://apps.apple.com/app/id1488466513) und [Google Play-Clients](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) veröffentlicht, die beide eine einfach zu bedienende Benutzeroberfläche besitzen, so dass du deine WireGuard-Verbindung nicht manuell konfigurieren musst. Der Android-Client ist auch auf [GitHub](https://github.com/mullvad/mullvadvpn-app/releases) verfügbar.

#### :material-information-outline:{ .pg-blue } Zusätzliche Hinweise

Mullvad ist sehr transparent, welche Netzwerk-Knotenpunkte sie [besitzen oder mieten](https://mullvad.net/en/servers). They also provide the option to enable Defense Against AI-guided Traffic Analysis ([DAITA](https://mullvad.net/en/blog/daita-defense-against-ai-guided-traffic-analysis)) in their apps. DAITA protects against the threat of advanced traffic analysis which can be used to connect patterns in VPN traffic with specific websites.

## Kriterien

<div class="admonition danger" markdown>
<p class="admonition-title">Achtung</p>

Es ist wichtig zu wissen, dass die Nutzung eines VPN-Anbieters dich nicht anonym macht, aber in bestimmten Situationen einen besseren Datenschutz bietet. Ein VPN ist kein Werkzeug für illegale Aktivitäten. Verlasse dich nicht auf "no Log" Richtlienen.

</div>

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, verbunden sind. Dies ermöglicht es uns, völlig objektive Empfehlungen zu geben.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen für alle VPN-Anbieter*innen entwickelt, die empfohlen werden wollen, darunter starke Verschlüsselung, unabhängige Sicherheitsprüfungen, moderne Technologie und mehr. Wir empfehlen dir, dich mit dieser Liste vertraut zu machen, bevor du dich für einen VPN-Anbieter entscheidest, und deine eigenen Nachforschungen anstellst, um sicherzustellen, dass der von dir gewählte VPN-Anbieter so vertrauenswürdig wie möglich ist.

### Technologie

Wir verlangen von allen von uns empfohlenen VPN-Anbietern, dass sie Standard-Konfigurationsdateien bereitstellen, die in einem generischen Open-Source-Client verwendet werden können. **Wenn** ein eigener VPN-Client bereitstellt wird, benötigt er einen Kill-Switch, um Datenlecks im Netzwerk zu blockieren, wenn die Verbindung getrennt wird.

**Mindestvoraussetzung um zu qualifizieren:**

- Unterstützung von starken Protokollen wie WireGuard.
- In die Clients integrierter Kill-Switch.
- Multi-Hop-Unterstützung. Multi-Hopping ist wichtig, um Daten im Falle einer Kompromittierung eines einzelnen Knotens geheim zu halten.
- Wenn VPN-Clients zur Verfügung gestellt werden, sollten sie [Open Source](https://de.wikipedia.org/wiki/Open_Source)sein, wie die VPN-Software, die in der Regel in sie integriert ist. Wir sind der Meinung, dass die Verfügbarkeit des [Quellcodes](https://en.wikipedia.org/wiki/Source_code) mehr Transparenz darüber schafft, was das Programm tatsächlich tut.
- Zensurresistente Funktionen zur Umgehung von Firewalls ohne DPI.

**Im besten Fall:**

- Kill-Switch mit hochgradig konfigurierbaren Optionen (Aktivierung/Deaktivierung in bestimmten Netzen, beim Booten usw.)
- Einfach zu bedienende VPN-Clients
- [IPv6](https://en.wikipedia.org/wiki/IPv6) Unterstützung. Wir erwarten, dass die Server eingehende Verbindungen über IPv6 zulassen und dir den Zugang zu Diensten ermöglichen, die auf IPv6-Adressen gehostet werden.
- Die Möglichkeit der [Remote-Port-Weiterleitung](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) hilft bei der Herstellung von Verbindungen bei der Verwendung von P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) Dateitauschbörsen-Software zum Austausch von Dateien oder zum Hosten eines Servers (z. B. Mumble).
- Verschleierungstechnologie, die die wahre Natur des Internetverkehrs tarnt und dazu dient, fortschrittliche Internet-Zensurmethoden wie DPI zu umgehen.

### Datenschutz

Wir ziehen es vor, dass die von uns empfohlenen Anbieter*innen so wenig Daten wie möglich sammeln. Der Verzicht auf die Erhebung personenbezogener Daten bei der Anmeldung und die Annahme anonymer Zahlungsformen sind erforderlich.

**Mindestvoraussetzung um zu qualifizieren:**

- [Anonyme Kryptowährung](cryptocurrency.md) **oder** Barzahlung möglich.
- Für die Registrierung sind keine persönlichen Daten erforderlich: Höchstens Benutzername, Passwort und E-Mail.

**Im besten Fall:**

- Akzeptiert mehrere [anonyme Zahlungsmöglichkeiten](advanced/payments.md).
- Es werden keine persönlichen Informationen akzeptiert (automatisch generierter Benutzername, keine E-Mail erforderlich, usw.).

### Sicherheit

Ein VPN ist sinnlos, wenn es nicht einmal angemessene Sicherheit bieten kann. Wir setzen für all von uns empfohlenen Anbietern voraus, dass sie die aktuellen Sicherheitsstandards einhalten. Idealerweise würden sie standardmäßig zukunftssichere Verschlüsselungsverfahren verwenden. Wir setzen auch voraus, dass ein unabhängiger Dritter die Sicherheit des Anbieters überprüft, idealerweise sehr umfassend und wiederholt (jährlich).

**Mindestvoraussetzung um zu qualifizieren:**

- Starke Verschlüsselungsschemata: OpenVPN mit SHA-256-Authentifizierung; RSA-2048 oder besserer Handshake; AES-256-GCM oder AES-256-CBC Datenverschlüsselung.
- Forward Secrecy (vorwärts gerichtete Geheimhaltung).
- Veröffentlichte Sicherheitsaudits durch ein angesehenes Drittunternehmen.
- VPN-Server, die eine vollständige Festplattenverschlüsselung verwenden oder nur über RAM laufen.

**Im besten Fall:**

- Stärkste Verschlüsselung: RSA-4096.
- Optionale quantenresistente Verschlüsselung.
- Forward Secrecy (vorwärts gerichtete Geheimhaltung).
- Umfassende veröffentlichte Sicherheitsaudits durch ein angesehenes Drittunternehmen.
- Bug-Bounty-Programme und/oder ein koordiniertes Verfahren zur Offenlegung von Sicherheitslücken.
- VPN-Server die nur über RAM laufen.

### Vertrauen

Du würdest nicht jemandem mit einer gefälschten Identität deine Finanzen anvertrauen, warum solltest du ihm also deine Internetdaten anvertrauen? Wir setzen für die von uns empfohlenen Anbietern voraus, dass sie ihre Eigentumsverhältnisse oder ihre Führungsrolle öffentlich gemacht haben. Außerdem wünschen wir uns häufige Transparenzberichte, insbesondere über die Bearbeitung von Regierungsanfragen.

**Mindestvoraussetzung um zu qualifizieren:**

- Öffentliche Führungs- oder Eigentumsverhältnisse.
- Unternehmen mit Sitz in einer Rechtsordnung, in der es nicht gezwungen werden kann, heimlich zu protokollieren.

**Im besten Fall:**

- Öffentliche Führung.
- Häufige Transparenzberichte.

### Marketing

Bei den von uns empfohlenen VPN-Anbietern legen wir Wert auf ein verantwortungsvolles Marketing.

**Mindestvoraussetzung um zu qualifizieren:**

- Sie müssen Analyse-Tools selbst hosten (d. h. kein Google Analytics).

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

Obwohl es dafür keine strikten Anforderungen gibt, gibt es einige Faktoren, die wir geprüft haben, um zu ermitteln, welche Anbieter zu empfehlen sind. Dazu gehören Funktionen zum Sperren von Inhalten, Warrant Canaries, ein hervorragender Kundendienst, die Anzahl der zulässigen gleichzeitigen Verbindungen usw.
