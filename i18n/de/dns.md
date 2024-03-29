---
title: "DNS-Resolver"
icon: material/dns
description: Dies sind einige verschlüsselte DNS-Provider, zu denen wir den Wechsel empfehlen, um die Standardkonfiguration Ihres ISP (Internetanbieters) zu ersetzen.
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

Encrypted DNS with third-party servers should only be used to get around basic [DNS blocking](https://en.wikipedia.org/wiki/DNS_blocking) when you can be sure there won't be any consequences. Verschlüsseltes DNS hilft dir nicht dabei, deine Browsing-Aktivitäten zu verbergen.

[Learn more about DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## Empfohlene DNS-Anbieter

| DNS-Anbieter                                                               | Datenschutzerklärung                                                                                 | Protokolle                                                                   | Protokollierung | ECS      | Filter                                                                                                                                                |
| -------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | --------------- | -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**AdGuard**](https://adguard.com/en/adguard-dns/overview.html)            | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                               | Cleartext <br> DoH/3 <br> DoT <br> DoQ <br> DNSCrypt | Some[^1]        | Yes      | Based on personal configuration. Die verwendete Filterliste findest du hier. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) | Klartext <br> DoH/3 <br> DoT                                     | Some[^2]        | Nein     | Based on personal configuration.                                                                                                                      |
| [**Control D**](https://controld.com/free-dns)                             | [:octicons-link-external-24:](https://controld.com/privacy)                                          | Klartext <br> DoH/3 <br> DoT <br> DoQ                      | Optional[^3]    | Nein     | Based on personal configuration.                                                                                                                      |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy)                    | DoH <br> DoT                                                           | Nein[^4]        | Nein     | Based on personal configuration. Die verwendete Filterliste findest du hier. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    |
| [**NextDNS**](https://nextdns.io)                                          | [:octicons-link-external-24:](https://nextdns.io/privacy)                                            | Klartext <br> DoH/3 <br> DoT <br> DoQ                      | Optional[^5]    | Optional | Based on personal configuration.                                                                                                                      |
| [**Quad9**](https://quad9.net)                                             | [:octicons-link-external-24:](https://quad9.net/privacy/policy)                                      | Klartext <br> DoH <br> DoT <br> DNSCrypt                   | Some[^6]        | Optional | Based on personal configuration, Malware blocking by default.                                                                                         |

### Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, verbunden sind.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen, sich mit dieser Liste vertraut zu machen, bevor sich für ein Projekt entschieden wird und eigenen Nachforschungen anzustellen, um sicherzustellen, dass es die richtige Wahl ist.

<div class="admonition example" markdown>
<p class="admonition-title">Dieser Abschnitt ist neu</p>

Wir arbeiten daran, definierte Kriterien für jeden Bereich unserer Website festzulegen, daher kann dies sich noch ändern. Bei Fragen zu unseren Kriterien, können diese [in unserem Forum] (https://discuss.privacyguides.net/latest) gestellt werden. Und gehen Sie nicht davon aus, dass wir etwas bei unseren Empfehlungen nicht berücksichtigt haben, wenn es hier nicht aufgeführt ist. Es gibt viele Faktoren, die berücksichtigt und besprochen werden, wenn wir ein Projekt empfehlen, und die Dokumentation jedes einzelnen Faktors ist ein laufender Prozess.

</div>

- Muss [DNSSEC](advanced/dns-overview.md#what-is-dnssec) unterstützen.
- [QNAME Minimierung](advanced/dns-overview.md#what-is-qname-minimization).
- Erlaubt es [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) zu deaktivieren.
- Bevorzugt [anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) Unterstützung oder Geo-Steering-Unterstützung.

## Native Betriebssystemunterstützung

### Android

Android 9 und höher unterstützen DNS über TLS. Die Einstellungen sind zu finden unter: **Einstellungen** &rarr; **Netzwerk & Internet** &rarr; **Privates DNS**.

### Apple-Geräte

Die neuesten Versionen von iOS, iPadOS, tvOS und macOS unterstützen sowohl DoT als auch DoH. Beide Protokolle werden nativ über [Konfigurationsprofile](https://support.apple.com/de-de/guide/security/secf6fb9f053/web) oder über die [DNS Settings API](https://developer.apple.com/documentation/networkextension/dns_settings)unterstützt.

Nach der Installation eines Konfigurationsprofils oder einer Anwendung, die die DNS-Einstellungs-API verwendet, kann die DNS-Konfiguration ausgewählt werden. Wenn ein VPN aktiv ist, verwendet die DNS Auflösung innerhalb des VPN-Tunnels die DNS-Einstellungen des VPN und nicht deine systemweiten Einstellungen.

#### Signierte Profile

Apple bietet keine native Schnittstelle zur Erstellung von Profilen mit verschlüsseltem DNS. [Secure DNS profile creator](https://dns.notjakob.com/tool.html) ist ein inoffizielles Tool zur Erstellung eigener Profile mit verschlüsseltem DNS, diese sind jedoch nicht signiert. Signierte Profile sind zu bevorzugen; das Signieren bestätigt die Herkunft eines Profils und trägt dazu bei, die Integrität der Profile zu gewährleisten. Signierte Konfigurationsprofile erhalten ein grünes "Verifiziert"-Label. For more information on code signing, see [About Code Signing](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html). **Signed profiles** are offered by [AdGuard](https://adguard.com/en/blog/encrypted-dns-ios-14.html), [NextDNS](https://apple.nextdns.io), and [Quad9](https://quad9.net/news/blog/ios-mobile-provisioning-profiles).

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

`systemd-resolved`, das viele Linux-Distributionen für ihre DNS Abfragen verwenden, unterstützt noch nicht [DoH](https://github.com/systemd/systemd/issues/8639). Wenn trotzdem DoH verwendent werden soll, muss ein Proxy wie [dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy) installiert und [konfiguriert](https://wiki.archlinux.org/title/Dnscrypt-proxy) werden, um alle DNS-Anfragen vom System-Resolver entgegenzunehmen und sie über HTTPS weiterzuleiten.

</div>

## Verschlüsselte DNS-Proxies

Verschlüsselte DNS-Proxy-Software stellt einen lokalen Proxy für den [unverschlüsselten DNS-](advanced/dns-overview.md#unencrypted-dns) Resolver zur Verfügung. Normalerweise wird es auf Plattformen verwendet, die [verschlüsseltes DNS](advanced/dns-overview.md#what-is-encrypted-dns) nicht unterstützen.

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ align=right }
![RethinkDNS logo](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** ist ein Open-Source Android-Client, der [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), [DNS-over-TLS](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) und DNS-Proxy unterstützt, DNS-Antworten zwischenspeichert, DNS-Anfragen lokal protokolliert und auch als Firewall verwendet werden kann.

[:octicons-home-16: Homepage](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

### dnscrypt-proxy

<div class="admonition recommendation" markdown>

![dnscrypt-proxy logo](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**dnscrypt-proxy** is a DNS proxy with support for [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), and [Anonymized DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

<div class="admonition warning" markdown>
<p class="admonition-title">The anonymized DNS feature does <a href="advanced/dns-overview.md#why-shouldnt-i0-use-encrypted-dns"><strong>not</strong></a> anonymize other network traffic.</p>
</div>

[:octicons-repo-16: Repository](https://github.com/DNSCrypt/dnscrypt-proxy){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

## Selbstgehostete Lösungen

Eine selbst gehostete DNS-Lösung ist nützlich für die Filterung auf kontrollierten Plattformen wie Smart-TVs und anderen IoT-Geräten, da keine clientseitige Software erforderlich ist.

### AdGuard Home

<div class="admonition recommendation" markdown>

![AdGuard Home logo](assets/img/dns/adguard-home.svg){ align=right }

**AdGuard Home** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

AdGuard Home bietet eine ausgefeilte Weboberfläche, über die Einblicke erhalten und blockierte Inhalte verwalten werden können.

[:octicons-home-16: Homepage](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Source Code" }

</details>

</div>

### Pi-hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](assets/img/dns/pi-hole.svg){ align=right }

**Pi-hole** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

Pi-hole ist für den Betrieb auf einem Raspberry Pi konzipiert, ist aber nicht auf diese Hardware beschränkt. The software features a friendly web interface to view insights and manage blocked content.

[:octicons-home-16: Homepage](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Source Code" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title=Contribute }

</details>

</div>

[^1]: AdGuard stores aggregated performance metrics of their DNS servers, namely the number of complete requests to a particular server, the number of blocked requests, and the speed of processing requests. They also keep and store the database of domains requested in within last 24 hours. "We need this information to identify and block new trackers and threats." "We also log how many times this or that tracker has been blocked. We need this information to remove outdated rules from our filters." [https://adguard.com/en/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: Cloudflare collects and stores only the limited DNS query data that is sent to the 1.1.1.1 resolver. The 1.1.1.1 resolver service does not log personal data, and the bulk of the limited non-personally identifiable query data is stored only for 25 hours. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: Control D only logs for Premium resolvers with custom DNS profiles. Free resolvers do not log data. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: Mullvad's DNS service is available to both subscribers and non-subscribers of Mullvad VPN. Their privacy policy explicitly claims they do not log DNS requests in any way. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^5]: When used with an account, NextDNS will enable insights and logging features by default (as some features require it). You can choose retention time and log storage location for any logs you choose to keep, or disable logs altogether. If used without an account, no data is logged. [https://nextdns.io/privacy](https://nextdns.io/privacy)
[^6]: Quad9 collects some data for the purposes of threat monitoring and response. That data may then be remixed and shared, such as for the purpose of security research. Quad9 does not collect or record IP addresses or other data they deem personally identifiable. [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
