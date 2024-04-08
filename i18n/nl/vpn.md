---
meta_title: "Privé VPN Service Aanbevelingen en Vergelijkingen, Geen Sponsors of Advertenties - Privacy Guides"
title: "VPN-diensten"
icon: material/vpn
description: Dit zijn de beste VPN-diensten om jouw privacy en veiligheid online te beschermen. Vind hier een provider die er niet op uit is om je te bespioneren.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<!-- markdownlint-disable MD024 -->

If you're looking for additional **privacy** from your ISP, on a public Wi-Fi network, or while torrenting files, a VPN may be the solution for you.

<div class="admonition danger" markdown>
<p class="admonition-title">VPNs do not provide anonymity</p>

Using a VPN will **not** keep your browsing habits anonymous, nor will it add additional security to non-secure (HTTP) traffic.

If you are looking for **anonymity**, you should use the Tor Browser. If you're looking for added **security**, you should always ensure you're connecting to websites using HTTPS. Een VPN is geen vervanging voor goede beveiligingspraktijken.

[Download Tor](https://torproject.org){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Gedetailleerd VPN-overzicht :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Aanbevolen Providers

Our recommended providers use encryption, support WireGuard & OpenVPN, and have a no logging policy. Lees onze [volledige lijst met criteria](#criteria) voor meer informatie.

| Provider              | Countries | WireGuard                     | Port Forwarding                                            | IPv6                                                     | Anonymous Payments |
| --------------------- | --------- | ----------------------------- | ---------------------------------------------------------- | -------------------------------------------------------- | ------------------ |
| [Proton](#proton-vpn) | 91+       | :material-check:{ .pg-green } | :material-information-outline:{ .pg-blue } Partial Support | :material-alert-outline:{ .pg-orange }                   | Contant            |
| [IVPN](#ivpn)         | 37+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                     | :material-information-outline:{ .pg-blue } Outgoing Only | Monero, Cash       |
| [Mullvad](#mullvad)   | 41+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                            | Monero, Cash       |

### Proton VPN

<div class="admonition recommendation" markdown>

![Proton VPN logo](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** is een sterke speler in de VPN-ruimte en is in bedrijf sinds 2016. Proton AG is gevestigd in Zwitserland en biedt een beperkte gratis versie aan en ook een meer uitgebreide premium optie.

[:octicons-home-16: Homepage](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:simple-windows11: Windows](https://protonvpn.com/download-windows)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 91 Countries

Proton VPN has [servers in 91 countries](https://protonvpn.com/vpn-servers) or [5](https://protonvpn.com/support/how-to-create-free-vpn-account) if you use their [free plan](https://protonvpn.com/free-vpn/server).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Dit komt door een kortere route (minder hops) naar de bestemming.
{ .annotate }

1. Last checked: 2024-04-02

Wij denken ook dat het beter is voor de veiligheid van de privésleutels van de VPN-provider als ze [dedicated servers](https://en.wikipedia.org/wiki/Dedicated_hosting_service) gebruiken, in plaats van goedkopere gedeelde servers (met andere klanten) zoals [virtual private servers](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Onafhankelijk geaudit

Vanaf januari 2020, heeft Proton VPN een onafhankelijke audit door SEC Consult ondergaan. SEC Consult vond enkele kwetsbaarheden met een gemiddeld en laag risico in de Windows-, Android- en iOS-applicaties van Proton VPN, die allemaal door Proton VPN "naar behoren waren verholpen" voordat de rapporten werden gepubliceerd. Geen van de geconstateerde problemen zou een aanvaller op afstand toegang hebben verschaft tot jouw apparaat of verkeer. You can view individual reports for each platform at [protonvpn.com](https://protonvpn.com/blog/open-source). In April 2022 Proton VPN underwent [another audit](https://protonvpn.com/blog/no-logs-audit) and the report was [produced by Securitum](https://protonvpn.com/blog/wp-content/uploads/2022/04/securitum-protonvpn-nologs-20220330.pdf). Een [attestatiebrief](https://proton.me/blog/security-audit-all-proton-apps) werd op 9 november 2021 voor de apps van Proton VPN verstrekt door [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } Open-source clients

Proton VPN levert de broncode voor hun desktop en mobiele clients in hun [GitHub organisatie](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Accepteert contant geld

Proton VPN accepteert, naast credit/debit cards, PayPal en [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), ook **contant geld** als anonieme vorm van betaling.

#### :material-check:{ .pg-green } WireGuard ondersteuning

Proton VPN ondersteunt hoofdzakelijk het WireGuard® protocol. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Bovendien streeft WireGuard ernaar om eenvoudiger en sneller te zijn.

Proton VPN [recommends](https://protonvpn.com/blog/wireguard) the use of WireGuard with their service. On Proton VPN's Windows, macOS, iOS, Android, ChromeOS, and Android TV apps, WireGuard is the default protocol; however, [support](https://protonvpn.com/support/how-to-change-vpn-protocols) for the protocol is not present in their Linux app.

#### :material-alert-outline:{ .pg-orange } No IPv6 Support

Proton VPN's servers are only compatible with IPv4. The Proton VPN applications will block all outgoing IPv6 traffic, so you don't have to worry about your IPv6 address being leaked, but you will not be able to connect to any IPv6-only sites, and you will not be able to connect to Proton VPN from an IPv6-only network.

#### :material-information-outline:{ .pg-info } Remote Port Forwarding

Proton VPN currently only supports ephemeral remote [port forwarding](https://protonvpn.com/support/port-forwarding) via NAT-PMP, with 60 second lease times. The Windows app provides an easy to access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup). Torrent toepassingen ondersteunen vaak de NAT-PMP volledig.

#### :material-information-outline:{ .pg-blue } Anti-Censorship

Proton VPN has their [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) protocol which *may* help in situations where VPN protocols like OpenVPN or Wireguard are blocked with various rudimentary techniques. Stealth encapsulates the VPN tunnel in TLS session in order to look like more generic internet traffic.

Unfortunately it does not work very well in countries where sophisticated filters are deployed that analyze all outgoing traffic in an attempt to discover encrypted tunnels. Stealth is also not yet available on [Windows](https://github.com/ProtonVPN/win-app/issues/64) or Linux.

#### :material-check:{ .pg-green } Mobiele Clients

In addition to providing standard OpenVPN configuration files, Proton VPN has mobile clients for [App Store](https://apps.apple.com/app/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android), and [GitHub](https://github.com/ProtonVPN/android-app/releases) allowing for easy connections to their servers.

#### :material-alert-outline:{ .pg-orange } Additional Notes

Proton VPN heeft eigen servers en datacenters in Zwitserland, IJsland en Zweden. Ze bieden adblocking en het blokkeren van bekende malware domeinen met hun DNS service. They offer content blocking and known-malware blocking with their DNS service. Additionally, Proton VPN also offers "Tor" servers allowing you to easily connect to onion sites, but we still strongly recommend using [the official Tor Browser](https://torproject.org) for this purpose.

##### :material-alert-outline:{ .pg-orange } Killswitch-functie is kapot op Intel-gebaseerde Macs

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch) on Intel-based Macs when using the VPN killswitch. Als je deze functie nodig hebt, en je gebruikt een Mac met Intel-chipset, moet je overwegen een andere VPN-dienst te gebruiken.

### IVPN

<div class="admonition recommendation" markdown>

![IVPN logo](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** is een premium VPN-provider en zijn actief sinds 2009. IVPN is gevestigd in Gibraltar.

[:octicons-home-16: Homepage](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:simple-windows11: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 37 Countries

IVPN has [servers in 37 countries](https://ivpn.net/status).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Dit komt door een kortere route (minder hops) naar de bestemming.
{ .annotate }

1. Last checked: 2024-04-02

Wij denken ook dat het beter is voor de veiligheid van de privésleutels van de VPN-provider als ze [dedicated servers](https://en.wikipedia.org/wiki/Dedicated_hosting_service) gebruiken, in plaats van goedkopere gedeelde servers (met andere klanten) zoals [virtual private servers](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Onafhankelijk geaudit

IVPN heeft een [no-logging audit ondergaan van Cure53](https://cure53.de/audit-report_ivpn.pdf) die concludeerde in overeenstemming met de no-logging claim van IVPN. IVPN heeft ook een [uitgebreid pentest rapport afgerond Cure53](https://cure53.de/summary-report_ivpn_2019.pdf) in januari 2020. IVPN has also said they plan to have [annual reports](https://ivpn.net/blog/independent-security-audit-concluded) in the future. A further review was conducted [in April 2022](https://ivpn.net/blog/ivpn-apps-security-audit-2022-concluded) and was produced by Cure53 [on their website](https://cure53.de/pentest-report_IVPN_2022.pdf).

#### :material-check:{ .pg-green } Open-source clients

As of February 2020 [IVPN applications are now open source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). Broncode kan worden verkregen van hun [GitHub organisatie](https://github.com/ivpn).

#### :material-check:{ .pg-green } Accepteert contant geld en Monero

Mullvad accepteert naast creditcards en PayPal ook Bitcoin, Bitcoin Cash, **Monero** en **contant geld/lokale valuta** als anonieme vormen van betaling.

#### :material-check:{ .pg-green } WireGuard ondersteuning

IVPN ondersteunt het WireGuard® protocol. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Bovendien streeft WireGuard ernaar om eenvoudiger en sneller te zijn.

IVPN [recommends](https://ivpn.net/wireguard) the use of WireGuard with their service and, as such, the protocol is the default on all of IVPN's apps. IVPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-information-outline:{ .pg-blue } IPv6 Support

IVPN allows you to [connect to services using IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6) but doesn't allow you to connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } Remote Port Forwarding

IVPN previously supported port forwarding, but removed the option in [June 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). Het ontbreken van deze functie kan bepaalde toepassingen negatief beïnvloeden, met name peer-to-peer applicaties zoals torrent clients.

#### :material-check:{ .pg-green } Anti-Censorship

IVPN has obfuscation modes using the [v2ray](https://v2ray.com/en/index.html) project which helps in situations where VPN protocols like OpenVPN or Wireguard are blocked. Currently this feature is only available on Desktop and [iOS](https://ivpn.net/knowledgebase/ios/v2ray). It has two modes where it can use [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) over QUIC or TCP connections. QUIC is a modern protocol with better congestion control and therefore may be faster with reduced latency. The TCP mode makes your data appear as regular HTTP traffic.

#### :material-check:{ .pg-green } Mobiele Clients

In addition to providing standard OpenVPN configuration files, IVPN has mobile clients for [App Store](https://apps.apple.com/app/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), and [GitHub](https://github.com/ivpn/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } Additional Notes

IVPN-clients ondersteunen tweefactorauthenticatie (de clients van Mullvad niet). IVPN also provides "[AntiTracker](https://ivpn.net/antitracker)" functionality, which blocks advertising networks and trackers from the network level.

### Mullvad

<div class="admonition recommendation" markdown>

![Mullvad logo](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** is een snelle en goedkope VPN met een serieuze focus op transparantie en veiligheid. Zij zijn in bedrijf sinds **2009**. Mullvad is gevestigd in Zweden en heeft geen gratis proefversie.

[:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:simple-windows11: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 41 Countries

Mullvad has [servers in 41 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Dit komt door een kortere route (minder hops) naar de bestemming.
{ .annotate }

1. Last checked: 2024-04-02

Wij denken ook dat het beter is voor de veiligheid van de privésleutels van de VPN-provider als ze [dedicated servers](https://en.wikipedia.org/wiki/Dedicated_hosting_service) gebruiken, in plaats van goedkopere gedeelde servers (met andere klanten) zoals [virtual private servers](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Onafhankelijk geaudit

De VPN-clients van Mullvad zijn geaudit door Cure53 en Assured AB in een pentest-rapport [gepubliceerd op cure53.de](https://cure53.de/pentest-report_mullvad_v2.pdf). De beveiligingsonderzoekers concludeerden:

> Cure53 en Assured AB zijn blij met de resultaten van de audit en de software laat over het algemeen een positieve indruk achter. Dankzij de inzet van het interne team van Mullvad VPN, twijfelen de testers er niet aan dat het project vanuit een beveiligingsoogpunt op het juiste spoor zit.

In 2020 a second audit [was announced](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app) and the [final audit report](https://cure53.de/pentest-report_mullvad_2020_v2.pdf) was made available on Cure53's website:

> De resultaten van dit mei-juni 2020-project gericht op het Mullvad-complex zijn vrij positief. [...] Het totale applicatie-ecosysteem dat door Mullvad wordt gebruikt, laat een goede en gestructureerde indruk achter. De algemene structuur van de applicatie maakt het gemakkelijk om patches en fixes op een gestructureerde manier uit te rollen. De bevindingen van Cure53 laten vooral zien hoe belangrijk het is om de huidige lekken voortdurend te controleren en opnieuw te beoordelen, om de privacy van de eindgebruikers altijd te waarborgen. Dat gezegd hebbende, Mullvad beschermt de eindgebruiker uitstekend tegen veelvoorkomende lekken van PII en privacygerelateerde risico's.

In 2021 an infrastructure audit [was announced](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) and the [final audit report](https://cure53.de/pentest-report_mullvad_2021_v1.pdf) was made available on Cure53's website. Another report was commissioned [in June 2022](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data) and is available on [Assured's website](https://assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf).

#### :material-check:{ .pg-green } Open-source clients

Mullvad levert de broncode voor hun desktop en mobiele clients in hun [GitHub organisatie](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Accepteert contant geld en Monero

Mullvad accepteert naast creditcards en PayPal ook Bitcoin, Bitcoin Cash, **Monero** en **contant geld/lokale valuta** als anonieme vormen van betaling. Ze aanvaarden ook Swish en bankoverschrijvingen.

#### :material-check:{ .pg-green } WireGuard ondersteuning

Mullvad ondersteunt het WireGuard® protocol. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Bovendien streeft WireGuard ernaar om eenvoudiger en sneller te zijn.

Mullvad [recommends](https://mullvad.net/en/help/why-wireguard) the use of WireGuard with their service. It is the default or only protocol on Mullvad's Android, iOS, macOS, and Linux apps, but on Windows you have to [manually enable](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-check:{ .pg-green } IPv6-ondersteuning

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) and connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } Remote Port Forwarding

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). Het ontbreken van deze functie kan bepaalde toepassingen negatief beïnvloeden, met name peer-to-peer applicaties zoals torrent clients.

#### :material-check:{ .pg-green } Anti-Censorship

Mullvad has obfuscation an mode using [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) which may be useful in situations where VPN protocols like OpenVPN or Wireguard are blocked.

#### :material-check:{ .pg-green } Mobiele Clients

Mullvad has published [App Store](https://apps.apple.com/app/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. De Android client is ook beschikbaar op [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Additional Notes

Mullvad is very transparent about which nodes they [own or rent](https://mullvad.net/en/servers). They use [ShadowSocks](https://shadowsocks.org) in their ShadowSocks + OpenVPN configuration, making them more resistant against firewalls with [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) trying to block VPNs. Vermoedelijk moet [China een andere methode gebruiken om ShadowSocks servers te blokkeren](https://github.com/net4people/bbs/issues/22). Mullvad's website is ook toegankelijk via Tor via [o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion).

## Criteria

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Het is belangrijk op te merken dat het gebruik van een VPN provider je niet anoniem maakt, maar het geeft je wel een betere privacy in bepaalde situaties. Een VPN is geen instrument voor illegale activiteiten. Vertrouw niet op een "no log" beleid.

</div>

**Wij zijn niet verbonden aan de providers die wij aanbevelen. Hierdoor kunnen wij volledig objectieve aanbevelingen doen.** Naast [onze standaardcriteria](about/criteria.md), hebben we een duidelijke reeks vereisten ontwikkeld voor elke VPN-provider die aanbevolen wil worden, waaronder sterke encryptie, onafhankelijke beveiligingsaudits, moderne technologie en meer. Wij raden je aan deze lijst goed door te nemen voordat je een VPN-provider kiest, en jouw eigen onderzoek te doen om er zeker van te zijn dat de VPN-provider die je kiest zo betrouwbaar mogelijk is.

### Technologie

Wij eisen dat al onze aanbevolen VPN-providers OpenVPN-configuratiebestanden leveren die in elke client kunnen worden gebruikt. **Als** een VPN met een eigen aangepaste client aanbiedt, is een killswitch vereist om het lekken van netwerkgegevens te blokkeren wanneer de verbinding wordt verbroken.

**Minimum om in aanmerking te komen:**

- Ondersteuning voor sterke protocollen zoals WireGuard & OpenVPN.
- Killswitch ingebouwd in clients.
- Multihop ondersteuning. Multihopping is belangrijk om gegevens privé te houden in het geval van een compromittering door één knooppunt.
- If VPN clients are provided, they should be [open source](https://en.wikipedia.org/wiki/Open_source), like the VPN software they generally have built into them. Wij zijn van mening dat de beschikbaarheid van [broncode](https://en.wikipedia.org/wiki/Source_code) meer transparantie biedt over wat uw apparaat feitelijk doet.

**Beste geval:**

- Ondersteuning voor WireGuard en OpenVPN.
- Killswitch met in hoge mate configureerbare opties (inschakelen/uitschakelen op bepaalde netwerken, bij opstarten, enz.)
- Gemakkelijk te gebruiken VPN-clients
- Ondersteunt [IPv6](https://en.wikipedia.org/wiki/IPv6). Wij verwachten dat servers inkomende verbindingen via IPv6 zullen toestaan en u toegang zullen verschaffen tot diensten die op IPv6-adressen worden gehost.
- De mogelijkheid van [remote port forwarding](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) helpt bij het maken van verbindingen bij het gebruik van P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) file sharing software, Freenet, of het hosten van een server (bv. Mumble).
- Obfuscation technology which pads data packets with random data to circumvent internet censorship.

### Privacy

Wij geven er de voorkeur aan dat de door ons aanbevolen aanbieders zo weinig mogelijk gegevens verzamelen. Er worden geen persoonlijke gegevens verzameld bij de registratie en er worden anonieme betalingsvormen aanvaard.

**Minimum om in aanmerking te komen:**

- [Anonieme cryptocurrency](cryptocurrency.md) **of** cash betalingsoptie.
- Geen persoonlijke informatie nodig om te registreren: Hooguit gebruikersnaam, wachtwoord en e-mail.

**Beste geval:**

- Accepteert meerdere [anonieme betalingsopties](advanced/payments.md).
- Er wordt geen persoonlijke informatie geaccepteerd (automatisch gegenereerde gebruikersnaam, geen e-mail vereist, enz.).

### Veiligheid

Een VPN is zinloos als het niet eens voldoende beveiliging kan bieden. Wij eisen van al onze aanbevolen providers dat zij zich houden aan de huidige beveiligingsstandaarden voor hun OpenVPN-verbindingen. Idealiter zouden zij standaard meer toekomstbestendige encryptiesystemen gebruiken. Wij eisen ook dat een onafhankelijke derde partij de beveiliging van de aanbieder controleert, idealiter op zeer uitgebreide wijze en herhaaldelijk (jaarlijks).

**Minimum om in aanmerking te komen:**

- Sterke coderingsschema's: OpenVPN met SHA-256 authenticatie; RSA-2048 of betere handshake; AES-256-GCM of AES-256-CBC data-encryptie.
- Forward Secrecy.
- Gepubliceerde veiligheidscontroles van een gerenommeerde derde partij.

**Beste geval:**

- Sterkste encryptie: RSA-4096.
- Forward Secrecy.
- Uitgebreide gepubliceerde veiligheidscontroles door een gerenommeerde derde partij.
- Programma's voor bug-bounty's en/of een gecoördineerd proces voor de openbaarmaking van kwetsbaarheden.

### Vertrouwen

Je zou jouw financiën niet toevertrouwen aan iemand met een valse identiteit, dus waarom zou je hen jouw internetgegevens toevertrouwen? Wij eisen van onze aanbevolen aanbieders dat zij hun eigendom of leiderschap openbaar maken. Wij zouden ook graag zien dat regelmatig verslag wordt uitgebracht over de transparantie, met name wat betreft de wijze waarop verzoeken van de overheid worden behandeld.

**Minimum om in aanmerking te komen:**

- Publiekelijk leiderschap of eigendom.

**Beste geval:**

- Publieksgericht leiderschap.
- Frequente transparantieverslagen.

### Marketing

Bij de VPN providers die wij aanbevelen zien wij graag verantwoorde marketing.

**Minimum om in aanmerking te komen:**

- Moet zelf analytics hosten (d.w.z., geen Google Analytics). De site van de aanbieder moet ook voldoen aan [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) voor mensen die zich willen afmelden.

Mag geen marketing hebben die onverantwoord is:

- Garanties van 100% bescherming van de anonimiteit. Wanneer iemand beweert dat iets 100% is, betekent dit dat er geen zekerheid is voor mislukking. We weten dat mensen zichzelf vrij gemakkelijk kunnen deanonimiseren op een aantal manieren, bv.:
    - Hergebruik van persoonlijke informatie (bv. e-mailaccounts, unieke pseudoniemen, enz.) waartoe zij toegang hadden zonder anonimiteitssoftware (Tor, VPN, enz.)
    - [Browser vingerafdrukken](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Beweren dat een VPN met één circuit "anoniemer" is dan Tor, dat een circuit van drie of meer hops is dat regelmatig verandert.
- Gebruik verantwoordelijk taalgebruik: d.w.z. het is oké om te zeggen dat een VPN "losgekoppeld" of "niet aangesloten" is, maar beweren dat iemand "blootgesteld", "kwetsbaar" of "gecompromitteerd" is, is nodeloos gebruik van alarmerende taal die onjuist kan zijn. Die persoon kan bijvoorbeeld gewoon gebruik maken van de service van een andere VPN-provider of Tor gebruiken.

**Beste geval:**

Verantwoorde marketing die zowel educatief als nuttig is voor de consument zou kunnen bestaan uit:

- Een nauwkeurige vergelijking met wanneer Tor of andere [op zichzelf staande netwerken](tor.md) moeten worden gebruikt.
- Beschikbaarheid van de website van de VPN-provider via een .onion [Verborgen service](https://en.wikipedia.org/wiki/.onion)

### Extra functionaliteit

Hoewel het geen strikte vereisten zijn, zijn er enkele factoren die wij in aanmerking hebben genomen bij het bepalen van de aanbieders die wij aanbevelen. These include content blocking functionality, warrant canaries, multihop connections, excellent customer support, the number of allowed simultaneous connections, etc.
