---
meta_title: "Privé VPN-Diensten Aanbevelingen en Vergelijkingen, Zonder Sponsors of Advertenties - Privacy Guides"
title: VPN-diensten
icon: material/vpn
description: De beste VPN-diensten om je privacy en veiligheid online te beschermen. Vind hier een provider die er niet op uit is om je te bespioneren.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Beschermt tegen de volgende bedreiging(en):</small>

- [:material-account-cash: Surveillance kapitalisme](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Als je op zoek bent naar extra *privacy* van je ISP, op een openbaar Wi-Fi-netwerk of tijdens het torrenten van bestanden, dan kan een **VPN** de oplossing voor jou zijn.

<div class="admonition danger" markdown>
<p class="admonition-title">VPN's bieden geen anonimiteit</p>

Het gebruik van een VPN houdt je surfgedrag **niet** anoniem en voegt geen extra beveiliging toe aan niet-beveiligd (HTTP) verkeer.

Als je op zoek bent naar **anonimiteit**, moet je de Tor Browser gebruiken. Als je op zoek bent naar extra **veiligheid**, moet je er altijd voor zorgen dat je verbinding maakt met websites via HTTPS. Een VPN is geen vervanging voor goede beveiligingspraktijken.

[Inleiding tot de Tor-browser](tor.md#tor-browser){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Gedetailleerd VPN-overzicht :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Aanbevolen Providers

De door ons aanbevolen providers gebruiken encryptie, ondersteunen WireGuard & OpenVPN en hebben een no logging policy. Lees onze [volledige lijst met criteria](#criteria) voor meer informatie.

| Provider              | Landen | WireGuard                     | Port forwarding                                                    | IPv6                                                              | Anonieme betalingen             |
| --------------------- | ------ | ----------------------------- | ------------------------------------------------------------------ | ----------------------------------------------------------------- | ------------------------------- |
| [Proton](#proton-vpn) | 127+   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Gedeeltelijke ondersteuning | :material-information-outline:{ .pg-blue } Beperkte ondersteuning | Contant Monero via derde partij |
| [IVPN](#ivpn)         | 41+    | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                             | :material-information-outline:{ .pg-blue } Alleen uitgaand        | Monero Cash                     |
| [Mullvad](#mullvad)   | 49+    | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                             | :material-check:{ .pg-green }                                     | Monero Cash                     |

### Proton VPN

<div class="admonition recommendation" markdown>

![Proton VPN logo](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** is een sterke speler in de VPN-ruimte en is in bedrijf sinds 2016. Proton AG is gevestigd in Zwitserland en biedt een beperkte gratis versie aan en ook een meer uitgebreide premium optie.

[:octicons-home-16: Homepage](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Privacybeleid" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title="Documentatie" }
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Broncode" }

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

#### :material-check:{ .pg-green } 127 Landen

Proton VPN heeft [servers in 127 landen](https://protonvpn.com/vpn-servers)(1) of [10](https://protonvpn.com/support/how-to-create-free-vpn-account) als je hun [gratis plan](https://protonvpn.com/blog/product-roadmap-winter-2025-2026) gebruikt.(2) Als je een VPN-provider kiest met een server het dichtst bij jou in de buurt, verminder je de vertraging van het netwerkverkeer dat je verstuurt. Dit komt door een kortere route (minder hops) naar de bestemming.
{ .annotate }

1. Of which at least 71 are virtual servers, meaning your IP will appear from the country but the server is in another. Nog eens 12 locaties hebben zowel hardware- als virtuele servers. [Bron](https://protonvpn.com/support/how-smart-routing-works)
2. Laatst gecontroleerd: 2025-10-28

Wij denken ook dat het beter is voor de veiligheid van de privésleutels van de VPN-provider als ze [dedicated servers](https://en.wikipedia.org/wiki/Dedicated_hosting_service) gebruiken, in plaats van goedkopere gedeelde servers (met andere klanten) zoals [virtual private servers](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Onafhankelijk geaudit

Independent security researcher Ruben Santamarta conducted audits for Proton VPN's [browser extensions](https://drive.proton.me/urls/RWDD2SHT98#v7ZrwNcafkG8) and [apps](https://drive.proton.me/urls/RVW8TXG484#uTXX5Fc9GADo) in September 2024 and January 2025, respectively. Proton VPN's infrastrcture has undergone [annual audits](https://protonvpn.com/blog/no-logs-audit) by Securitum since 2022.

Previously, Proton VPN underwent an independent audit by SEC Consult in January 2020. SEC Consult vond enkele kwetsbaarheden met een gemiddeld en laag risico in de Windows-, Android- en iOS-applicaties van Proton VPN, die allemaal door Proton VPN "naar behoren waren verholpen" voordat de rapporten werden gepubliceerd. Geen van de geconstateerde problemen zou een aanvaller op afstand toegang hebben verschaft tot jouw apparaat of verkeer. You can view individual reports for each platform in their dedicated [blog post](https://web.archive.org/web/20250307041036/https://protonvpn.com/blog/open-source) on the audit.

#### :material-check:{ .pg-green } Open-source clients

Proton VPN provides the source code for their desktop and mobile clients in their [GitHub organization](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Accepteert contant geld

Proton VPN, in addition to accepting credit/debit cards, PayPal, and [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), also accepts **cash/local currency** as an anonymous form of payment. You can also use [**Monero**](cryptocurrency.md#monero) to purchase vouchers for Proton VPN Plus and Proton Unlimited via their [official](https://discuss.privacyguides.net/t/add-monero-as-an-anonymous-payment-method-for-proton-services/31058/15) reseller [ProxyStore](https://dys2p.com/en/2025-09-09-proton.html).

#### :material-check:{ .pg-green } WireGuard ondersteuning

Proton VPN supports the WireGuard® protocol. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Bovendien streeft WireGuard ernaar om eenvoudiger en sneller te zijn.

Proton VPN [recommends](https://protonvpn.com/blog/wireguard) the use of WireGuard with their service. Proton VPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-alert-outline:{ .pg-orange } Limited IPv6 Support

Proton [now supports IPv6](https://protonvpn.com/support/prevent-ipv6-vpn-leaks) in their browser extension and Linux client, but only 80% of their servers are IPv6-compatible. On other platforms, the Proton VPN client will block all outgoing IPv6 traffic, so you don't have to worry about your IPv6 address being leaked, but you will not be able to connect to any IPv6-only sites, nor will you be able to connect to Proton VPN from an IPv6-only network.

#### :material-information-outline:{ .pg-info } Remote Port Forwarding

Proton VPN currently only supports ephemeral remote [port forwarding](https://protonvpn.com/support/port-forwarding) via NAT-PMP, with 60 second lease times. The official Windows and Linux apps provide an easy-to-access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup). Torrent toepassingen ondersteunen vaak de NAT-PMP volledig.

#### :material-information-outline:{ .pg-blue } Anti-Censorship

Proton VPN has their [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) protocol which *may* help in situations where VPN protocols like OpenVPN or WireGuard are blocked with various rudimentary techniques. Stealth encapsulates the VPN tunnel in TLS session in order to look like more generic internet traffic.

Unfortunately, it does not work very well in countries where sophisticated filters that analyze all outgoing traffic in an attempt to discover encrypted tunnels are deployed. Stealth is available on Android, iOS, Windows, and macOS, but it's not yet available on Linux.

#### :material-check:{ .pg-green } Mobiele Clients

Proton VPN has published [App Store](https://apps.apple.com/app/id1437005085) and [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/ProtonVPN/android-app/releases).

<div class="admonition warning" markdown>
<p class="admonition-title">How to opt out of sharing telemetry</p>

On Android, Proton hides telemetry settings under the misleadingly labeled "**Help us fight censorship**" menu in the settings panel. On other platforms these settings can be found under the "**Usage statistics**" menu.

We are noting this because while we don't necessarily recommend against sharing anonymous usage statistics with developers, it is important that these settings are easily found and clearly labeled.

</div>

#### :material-information-outline:{ .pg-blue } Aanvullende opmerkingen

Proton VPN clients support two-factor authentication on all platforms. Ze bieden adblocking en het blokkeren van bekende malware domeinen met hun DNS service. They offer content blocking and known-malware blocking with their DNS service. Additionally, Proton VPN also offers "Tor" servers allowing you to easily connect to onion sites, but we still strongly recommend using [the official Tor Browser](tor.md#tor-browser) for this purpose.

##### :material-alert-outline:{ .pg-orange } Kill switch feature is broken on Intel-based Macs

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch) on Intel-based Macs when using the VPN kill switch. Als je deze functie nodig hebt, en je gebruikt een Mac met Intel-chipset, moet je overwegen een andere VPN-dienst te gebruiken.

### IVPN

<div class="admonition recommendation" markdown>

![IVPN logo](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** is een premium VPN-provider en zijn actief sinds 2009. IVPN is gevestigd in Gibraltar en biedt geen gratis proefversie.

[:octicons-home-16: Homepage](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Privacybeleid" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title="Documentatie" }
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Broncode" }

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

#### :material-check:{ .pg-green } 41 Landen

IVPN has [servers in 41 countries](https://ivpn.net/status).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Dit komt door een kortere route (minder hops) naar de bestemming.
{ .annotate }

1. Laatst gecontroleerd: 2025-10-28

Wij denken ook dat het beter is voor de veiligheid van de privésleutels van de VPN-provider als ze [dedicated servers](https://en.wikipedia.org/wiki/Dedicated_hosting_service) gebruiken, in plaats van goedkopere gedeelde servers (met andere klanten) zoals [virtual private servers](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Onafhankelijk geaudit

IVPN has had multiple [independent audits](https://ivpn.net/en/blog/tags/audit) since 2019 and has publicly announced their commitment to [annual security audits](https://ivpn.net/blog/ivpn-apps-security-audit-concluded).

#### :material-check:{ .pg-green } Open-source clients

As of February 2020 [IVPN applications are now open source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). Broncode kan worden verkregen van hun [GitHub organisatie](https://github.com/ivpn).

#### :material-check:{ .pg-green } Accepteert contant geld en Monero

In addition to accepting credit/debit cards and PayPal, IVPN accepts Bitcoin, **Monero** and **cash/local currency** (on annual plans) as anonymous forms of payment. You can also purchase [prepaid cards](https://ivpn.net/knowledgebase/billing/voucher-cards-faq) with redeem codes.

#### :material-check:{ .pg-green } WireGuard ondersteuning

IVPN ondersteunt het WireGuard® protocol. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Bovendien streeft WireGuard ernaar om eenvoudiger en sneller te zijn.

IVPN [recommends](https://ivpn.net/wireguard) the use of WireGuard with their service and, as such, the protocol is the default on all of IVPN's apps. IVPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-information-outline:{ .pg-blue } IPv6-ondersteuning

IVPN allows you to [connect to services using IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6) but doesn't allow you to connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } Remote Port Forwarding

IVPN previously supported port forwarding, but removed the option in [June 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). Het ontbreken van deze functie kan bepaalde toepassingen negatief beïnvloeden, met name peer-to-peer applicaties zoals torrent clients.

#### :material-check:{ .pg-green } Anti-Censorship

IVPN has obfuscation modes using [V2Ray](https://v2ray.com/en/index) which helps in situations where VPN protocols like OpenVPN or WireGuard are blocked. It has two modes where it can use [VMess](https://guide.v2fly.org/en_US/basics/vmess) over QUIC or TCP connections. QUIC is a modern protocol with better congestion control and therefore may be faster with reduced latency. The TCP mode makes your data appear as regular HTTP traffic.

#### :material-check:{ .pg-green } Mobiele Clients

IVPN has published [App Store](https://apps.apple.com/app/id1193122683) and [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/ivpn/android-app/releases).

#### :material-information-outline:{ .pg-blue } Aanvullende opmerkingen

IVPN-clients ondersteunen tweestapsverificatie. IVPN also provides "[AntiTracker](https://ivpn.net/antitracker)" functionality, which blocks advertising networks and trackers from the network level.

### Mullvad

<div class="admonition recommendation" markdown>

![Mullvad logo](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** is een snelle en goedkope VPN met een serieuze focus op transparantie en veiligheid. Ze zijn actief sinds 2009. Mullvad is based in Sweden and offers a 14-day money-back guarantee for [payment methods](https://mullvad.net/en/help/refunds) that allow it.

[:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacybeleid" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title="Documentatie" }
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Broncode" }

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

#### :material-check:{ .pg-green } 49 Landen

Mullvad has [servers in 49 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Dit komt door een kortere route (minder hops) naar de bestemming.
{ .annotate }

1. Laatst gecontroleerd: 2025-10-28

Wij denken ook dat het beter is voor de veiligheid van de privésleutels van de VPN-provider als ze [dedicated servers](https://en.wikipedia.org/wiki/Dedicated_hosting_service) gebruiken, in plaats van goedkopere gedeelde servers (met andere klanten) zoals [virtual private servers](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Onafhankelijk geaudit

Mullvad has had multiple [independent audits](https://mullvad.net/en/blog/tag/audits) and has publicly announced their endeavors to conduct [annual audits](https://mullvad.net/en/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) of their apps and infrastructure.

#### :material-check:{ .pg-green } Open-source clients

Mullvad levert de broncode voor hun desktop en mobiele clients in hun [GitHub organisatie](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Accepteert contant geld en Monero

Mullvad, in addition to accepting credit/debit cards and PayPal, accepts Bitcoin, Bitcoin Cash, **Monero** and **cash/local currency** as anonymous forms of payment. You can also purchase [prepaid cards](https://mullvad.net/en/help/partnerships-and-resellers) with redeem codes. Mullvad also accepts Swish and bank wire transfers, as well as a few European payment systems.

#### :material-check:{ .pg-green } WireGuard ondersteuning

Mullvad ondersteunt het WireGuard® protocol. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Bovendien streeft WireGuard ernaar om eenvoudiger en sneller te zijn.

Mullvad [recommends](https://mullvad.net/en/help/why-wireguard) the use of WireGuard with their service. It is the only protocol supported on their mobile apps, and their desktop apps will [lose OpenVPN support](https://mullvad.net/en/blog/reminder-that-openvpn-is-being-removed) in 2025. Additionally, their servers will stop accepting OpenVPN connections by January 15, 2026. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-check:{ .pg-green } IPv6-ondersteuning

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) and connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } Remote Port Forwarding

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). Het ontbreken van deze functie kan bepaalde toepassingen negatief beïnvloeden, met name peer-to-peer applicaties zoals torrent clients.

#### :material-check:{ .pg-green } Anti-Censorship

Mullvad offers several features to help bypass censorship and access the internet freely:

- **Obfuscation modes**: Mullvad has two built-in obfuscation modes: "UDP-over-TCP" and ["WireGuard over Shadowsocks"](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard). These modes disguise your VPN traffic as regular web traffic, making it harder for censors to detect and block. Supposedly, China has to use a [new method to disrupt Shadowsocks-routed traffic](https://gfw.report/publications/usenixsecurity23/en).
- **Advanced obfuscation with Shadowsocks and v2ray**: For more advanced users, Mullvad provides a guide on how to use the [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) plugin with Mullvad clients. This setup provides an additional layer of obfuscation and encryption.
- **Custom server IPs**: To counter IP-blocking, you can request custom server IPs from Mullvad's support team. Once you receive the custom IPs, you can input the text file in the "Server IP override" settings, which will override the chosen server IP addresses with ones that aren't known to the censor.
- **Bridges and proxies**: Mullvad also allows you to use bridges or proxies to reach their API (needed for authentication), which can help bypass censorship attempts that block access to the API itself.

#### :material-check:{ .pg-green } Mobiele Clients

Mullvad has published [App Store](https://apps.apple.com/app/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. De Android client is ook beschikbaar op [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Aanvullende opmerkingen

Mullvad is very transparent about which nodes they [own or rent](https://mullvad.net/en/servers). They also provide the option to enable Defense Against AI-guided Traffic Analysis ([DAITA](https://mullvad.net/en/blog/daita-defense-against-ai-guided-traffic-analysis)) in their apps. DAITA protects against the threat of advanced traffic analysis which can be used to connect patterns in VPN traffic with specific websites.

## Criteria

<div class="admonition danger" markdown>
<p class="admonition-title">Let op</p>

Het is belangrijk op te merken dat het gebruik van een VPN-provider je niet anoniem maakt, maar het geeft je wel een betere privacy in bepaalde situaties. Een VPN is geen instrument voor illegale activiteiten. Vertrouw niet op een "no log" beleid.

</div>

**Wij zijn niet verbonden aan de providers die wij aanbevelen. Hierdoor kunnen wij volledig objectieve aanbevelingen doen.** Naast [onze standaardcriteria](about/criteria.md), hebben we een duidelijke reeks vereisten ontwikkeld voor elke VPN-provider die aanbevolen wil worden, waaronder sterke encryptie, onafhankelijke beveiligingsaudits, moderne technologie en meer. Wij raden je aan deze lijst goed door te nemen voordat je een VPN-provider kiest, en jouw eigen onderzoek te doen om er zeker van te zijn dat de VPN-provider die je kiest zo betrouwbaar mogelijk is.

### Technologie

We require all our recommended VPN providers to provide standard configuration files which can be used in a generic, open-source client. **If** a VPN provides their own custom client, we require a kill switch to block network data leaks when disconnected.

**Minimum om in aanmerking te komen:**

- Support for strong protocols such as WireGuard.
- Kill switch built in to clients.
- Multi-hop support. Multi-hopping is important to keep data private in case of a single node compromise.
- If VPN clients are provided, they should be [open source](https://en.wikipedia.org/wiki/Open_source), like the VPN software they generally have built into them. We believe that [source code](https://en.wikipedia.org/wiki/Source_code) availability provides greater transparency about what the program is actually doing.
- Censorship resistance features designed to bypass firewalls without DPI.

**Beste geval:**

- Kill switch with highly configurable options (enable/disable on certain networks, on boot, etc.)
- Gemakkelijk te gebruiken VPN-clients
- [IPv6](https://en.wikipedia.org/wiki/IPv6) support. We verwachten dat servers inkomende verbindingen via IPv6 zullen toestaan en je toegang zullen geven tot services die gehost worden op IPv6-adressen.
- De mogelijkheid van [remote port forwarding](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) helpt bij het maken van verbindingen bij het gebruik van P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) file sharing software, Freenet, of het hosten van een server (bv. Mumble).
- Obfuscation technology which camouflages the true nature of internet traffic, designed to circumvent advanced internet censorship methods like DPI.

### Privacy

Wij geven er de voorkeur aan dat de door ons aanbevolen aanbieders zo weinig mogelijk gegevens verzamelen. Er worden geen persoonlijke gegevens verzameld bij de registratie en er worden anonieme betalingsvormen aanvaard.

**Minimum om in aanmerking te komen:**

- [Anonieme cryptocurrency](cryptocurrency.md) **of** cash betalingsoptie.
- Geen persoonlijke informatie nodig om te registreren: Hooguit gebruikersnaam, wachtwoord en e-mail.

**Beste geval:**

- Accepteert meerdere [anonieme betalingsopties](advanced/payments.md).
- Er wordt geen persoonlijke informatie geaccepteerd (automatisch gegenereerde gebruikersnaam, geen e-mailadres vereist, enz.)

### Veiligheid

Een VPN is zinloos als het niet eens voldoende beveiliging kan bieden. We require all our recommended providers to abide by current security standards. Idealiter zouden zij standaard meer toekomstbestendige encryptiesystemen gebruiken. Wij eisen ook dat een onafhankelijke derde partij de beveiliging van de aanbieder controleert, idealiter op zeer uitgebreide wijze en herhaaldelijk (jaarlijks).

**Minimum om in aanmerking te komen:**

- Sterke coderingsschema's: OpenVPN met SHA-256 authenticatie; RSA-2048 of betere handshake; AES-256-GCM of AES-256-CBC data-encryptie.
- Forward Secrecy.
- Gepubliceerde veiligheidscontroles van een gerenommeerde derde partij.
- VPN servers that use full-disk encryption or are RAM-only.

**Beste geval:**

- Sterkste encryptie: RSA-4096.
- Optional quantum-resistant encryption.
- Uitgebreide gepubliceerde veiligheidscontroles door een gerenommeerde derde partij.
- Programma's voor bug-bounty's en/of een gecoördineerd proces voor de openbaarmaking van kwetsbaarheden.
- RAM-only VPN-servers.

### Vertrouwen

Je zou jouw financiën niet toevertrouwen aan iemand met een valse identiteit, dus waarom zou je hen jouw internetgegevens toevertrouwen? Wij eisen van onze aanbevolen aanbieders dat zij hun eigendom of leiderschap openbaar maken. Wij zouden ook graag zien dat regelmatig verslag wordt uitgebracht over de transparantie, met name wat betreft de wijze waarop verzoeken van de overheid worden behandeld.

**Minimum om in aanmerking te komen:**

- Publiekelijk leiderschap of eigendom.
- Company based in a jurisdiction where it cannot be forced to do secret logging.

**Beste geval:**

- Publieksgericht leiderschap.
- Frequente transparantieverslagen.

### Marketing

Bij de VPN providers die wij aanbevelen zien wij graag verantwoorde marketing.

**Minimum om in aanmerking te komen:**

- Must self-host analytics (i.e., no Google Analytics).

Mag geen marketing hebben die onverantwoord is:

- Garanties van 100% bescherming van de anonimiteit. Wanneer iemand beweert dat iets 100% is, betekent dit dat er geen zekerheid is voor mislukking. We weten dat mensen zichzelf vrij gemakkelijk kunnen deanonimiseren op een aantal manieren, bv.:
    - Hergebruik van persoonlijke informatie (bv. e-mailaccounts, unieke pseudoniemen, enz.) waartoe zij toegang hadden zonder anonimiteitssoftware (Tor, VPN, enz.)
    - [Browser vingerafdrukken](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Beweren dat een VPN met één circuit "anoniemer" is dan Tor, dat een circuit van drie of meer hops is dat regelmatig verandert.
- Gebruik verantwoordelijk taalgebruik: d.w.z. het is oké om te zeggen dat een VPN "losgekoppeld" of "niet aangesloten" is, maar beweren dat iemand "blootgesteld", "kwetsbaar" of "gecompromitteerd" is, is nodeloos gebruik van alarmerende taal die onjuist kan zijn. Die persoon kan bijvoorbeeld gewoon gebruik maken van de service van een andere VPN-provider of Tor gebruiken.

**Beste geval:**

Verantwoorde marketing die zowel educatief als nuttig is voor de consument zou kunnen bestaan uit:

- Een nauwkeurige vergelijking met wanneer Tor of andere [op zichzelf staande netwerken](tor.md) moeten worden gebruikt.
- Beschikbaarheid van de website van de VPN-provider via een [.onion-service](https://en.wikipedia.org/wiki/.onion)

### Extra functionaliteit

Hoewel het geen strikte vereisten zijn, zijn er enkele factoren die wij in aanmerking hebben genomen bij het bepalen van de aanbieders die wij aanbevelen. These include content blocking functionality, warrant canaries, excellent customer support, the number of allowed simultaneous connections, etc.
