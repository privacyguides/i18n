---
meta_title: "Private VPN Service Recommendations and Comparison, No Sponsors or Ads - Privacy Guides"
title: "VPN Szolgáltatások"
icon: material/vpn
description: Ezek a legjobb VPN-szolgáltatások az online magánéleted és biztonságod megvédéséhez. Find a provider here that isn’t out to spy on you.
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

If you are looking for **anonymity**, you should use the Tor Browser. If you're looking for added **security**, you should always ensure you're connecting to websites using HTTPS. Egy VPN nem helyettesít helyes biztonsági gyakorlatokat.

[Download Tor](https://torproject.org){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Detailed VPN Overview :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Ajánlott Szolgáltatók

Our recommended providers use encryption, support WireGuard & OpenVPN, and have a no logging policy. Read our [full list of criteria](#criteria) for more information.

| Provider              | Countries | WireGuard                     | Port Forwarding                                            | IPv6                                                     | Anonymous Payments |
| --------------------- | --------- | ----------------------------- | ---------------------------------------------------------- | -------------------------------------------------------- | ------------------ |
| [Proton](#proton-vpn) | 91+       | :material-check:{ .pg-green } | :material-information-outline:{ .pg-blue } Partial Support | :material-alert-outline:{ .pg-orange }                   | Cash               |
| [IVPN](#ivpn)         | 37+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                     | :material-information-outline:{ .pg-blue } Outgoing Only | Monero, Cash       |
| [Mullvad](#mullvad)   | 41+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                            | Monero, Cash       |

### Proton VPN

<div class="admonition recommendation" markdown>

![Proton VPN logo](assets/img/vpn/protonvpn.svg){ align=right }

A **Proton VPN** egy erős pályázó a VPN-térben, és 2016 óta vannak működésben. A svájci székhelyű Proton AG egy korlátozott ingyenes előfizetést, valamint egy jobban felszerelt prémium opciót is kínál.

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

Proton VPN has [servers in 91 countries](https://protonvpn.com/vpn-servers) or [5](https://protonvpn.com/support/how-to-create-free-vpn-account) if you use their [free plan](https://protonvpn.com/free-vpn/server).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Ennek oka a célállomáshoz vezető rövidebb útvonal (kevesebb ugrás).
{ .annotate }

1. Last checked: 2024-04-02

We also think it's better for the security of the VPN provider's private keys if they use [dedicated servers](https://en.wikipedia.org/wiki/Dedicated_hosting_service), instead of cheaper shared solutions (with other customers) such as [virtual private servers](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Independently Audited

A Proton VPN átesett a SEC Consult független felülvizsálatán 2020 januárjában. A SEC Consult közepes és alacsony kockázatú sebezhetőségeket talált a Proton VPN Windows, Android és iOS alkalmazásaiban, amelyeket a Proton VPN a jelentések közzététele előtt "megfelelően kijavított". Az azonosított problémák egyike sem biztosított volna egy támadó számára távoli hozzáférést az eszközödhöz vagy forgalmadhoz. You can view individual reports for each platform at [protonvpn.com](https://protonvpn.com/blog/open-source). In April 2022 Proton VPN underwent [another audit](https://protonvpn.com/blog/no-logs-audit) and the report was [produced by Securitum](https://protonvpn.com/blog/wp-content/uploads/2022/04/securitum-protonvpn-nologs-20220330.pdf). A [letter of attestation](https://proton.me/blog/security-audit-all-proton-apps) was provided for Proton VPN's apps on 9th November 2021 by [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } Open-Source Clients

Proton VPN provides the source code for their desktop and mobile clients in their [GitHub organization](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Elfogad Készpénzt

Proton VPN, in addition to accepting credit/debit cards, PayPal, and [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), also accepts **cash/local currency** as an anonymous form of payment.

#### :material-check:{ .pg-green } WireGuard Support

A Proton VPN többnyire támogatja a WireGuard® protokollt. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Emellett a WireGuard célja, hogy egyszerűbb és hatékonyabb legyen.

Proton VPN [recommends](https://protonvpn.com/blog/wireguard) the use of WireGuard with their service. On Proton VPN's Windows, macOS, iOS, Android, ChromeOS, and Android TV apps, WireGuard is the default protocol; however, [support](https://protonvpn.com/support/how-to-change-vpn-protocols) for the protocol is not present in their Linux app.

#### :material-alert-outline:{ .pg-orange } No IPv6 Support

Proton VPN's servers are only compatible with IPv4. The Proton VPN applications will block all outgoing IPv6 traffic, so you don't have to worry about your IPv6 address being leaked, but you will not be able to connect to any IPv6-only sites, and you will not be able to connect to Proton VPN from an IPv6-only network.

#### :material-information-outline:{ .pg-info } Remote Port Forwarding

Proton VPN currently only supports ephemeral remote [port forwarding](https://protonvpn.com/support/port-forwarding) via NAT-PMP, with 60 second lease times. The Windows app provides an easy to access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup). Torrent applications often support NAT-PMP natively.

#### :material-information-outline:{ .pg-blue } Anti-Censorship

Proton VPN has their [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) protocol which *may* help in situations where VPN protocols like OpenVPN or Wireguard are blocked with various rudimentary techniques. Stealth encapsulates the VPN tunnel in TLS session in order to look like more generic internet traffic.

Unfortunately it does not work very well in countries where sophisticated filters are deployed that analyze all outgoing traffic in an attempt to discover encrypted tunnels. Stealth is also not yet available on [Windows](https://github.com/ProtonVPN/win-app/issues/64) or Linux.

#### :material-check:{ .pg-green } Mobile Clients

In addition to providing standard OpenVPN configuration files, Proton VPN has mobile clients for [App Store](https://apps.apple.com/app/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android), and [GitHub](https://github.com/ProtonVPN/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } Additional Notes

Proton VPN clients support two factor authentication on all platforms. A Proton VPN saját szerverekkel és adatközpontokkal rendelkezik Svájcban, Izlandon és Svédországban. They offer content blocking and known-malware blocking with their DNS service. Additionally, Proton VPN also offers "Tor" servers allowing you to easily connect to onion sites, but we still strongly recommend using [the official Tor Browser](tor.md#tor-browser) for this purpose.

##### :material-alert-outline:{ .pg-orange } Killswitch feature is broken on Intel-based Macs

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch) on Intel-based Macs when using the VPN killswitch. Ha szükséged van erre a funkcióra, és Intel chipsettel rendelkező Mac-et használsz, akkor fontold meg egy másik VPN szolgáltatás használatát.

### IVPN

<div class="admonition recommendation" markdown>

![IVPN logo](assets/img/vpn/ivpn.svg){ align=right }

Az **IVPN** egy másik prémium VPN szolgáltató, és 2009 óta vannak működésben. IVPN is based in Gibraltar and does not offer a free trial.

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

IVPN has [servers in 37 countries](https://ivpn.net/status).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Ennek oka a célállomáshoz vezető rövidebb útvonal (kevesebb ugrás).
{ .annotate }

1. Last checked: 2024-04-02

We also think it's better for the security of the VPN provider's private keys if they use [dedicated servers](https://en.wikipedia.org/wiki/Dedicated_hosting_service), instead of cheaper shared solutions (with other customers) such as [virtual private servers](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Independently Audited

IVPN has undergone a [no-logging audit from Cure53](https://cure53.de/audit-report_ivpn.pdf) which concluded in agreement with IVPN's no-logging claim. IVPN has also completed a [comprehensive pentest report Cure53](https://cure53.de/summary-report_ivpn_2019.pdf) in January 2020. IVPN has also said they plan to have [annual reports](https://ivpn.net/blog/independent-security-audit-concluded) in the future. A further review was conducted [in April 2022](https://ivpn.net/blog/ivpn-apps-security-audit-2022-concluded) and was produced by Cure53 [on their website](https://cure53.de/pentest-report_IVPN_2022.pdf).

#### :material-check:{ .pg-green } Open-Source Clients

As of February 2020 [IVPN applications are now open source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). Source code can be obtained from their [GitHub organization](https://github.com/ivpn).

#### :material-check:{ .pg-green } Accepts Cash and Monero

In addition to accepting credit/debit cards and PayPal, IVPN accepts Bitcoin, **Monero** and **cash/local currency** (on annual plans) as anonymous forms of payment. Prepaid cards with redeem codes are [also available](https://ivpn.net/knowledgebase/billing/voucher-cards-faq).

#### :material-check:{ .pg-green } WireGuard Support

Az IVPN támogatja a WireGuard® protokollt. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Emellett a WireGuard célja, hogy egyszerűbb és hatékonyabb legyen.

IVPN [recommends](https://ivpn.net/wireguard) the use of WireGuard with their service and, as such, the protocol is the default on all of IVPN's apps. IVPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-information-outline:{ .pg-blue } IPv6 Support

IVPN allows you to [connect to services using IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6) but doesn't allow you to connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } Remote Port Forwarding

IVPN previously supported port forwarding, but removed the option in [June 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). Missing this feature could negatively impact certain applications, especially peer-to-peer applications like torrent clients.

#### :material-check:{ .pg-green } Anti-Censorship

IVPN has obfuscation modes using the [v2ray](https://v2ray.com/en/index.html) project which helps in situations where VPN protocols like OpenVPN or Wireguard are blocked. Currently this feature is only available on Desktop and [iOS](https://ivpn.net/knowledgebase/ios/v2ray). It has two modes where it can use [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) over QUIC or TCP connections. QUIC is a modern protocol with better congestion control and therefore may be faster with reduced latency. The TCP mode makes your data appear as regular HTTP traffic.

#### :material-check:{ .pg-green } Mobile Clients

In addition to providing standard OpenVPN configuration files, IVPN has mobile clients for [App Store](https://apps.apple.com/app/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), and [GitHub](https://github.com/ivpn/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } Additional Notes

IVPN clients support two factor authentication. IVPN also provides "[AntiTracker](https://ivpn.net/antitracker)" functionality, which blocks advertising networks and trackers from the network level.

### Mullvad

<div class="admonition recommendation" markdown>

![Mullvad logo](assets/img/vpn/mullvad.svg){ align=right }

A **Mullvad** egy gyors és olcsó VPN, amely komoly hangsúlyt fektet az átláthatóságra és a biztonságra. **2009** óta vannak működésben. Mullvad is based in Sweden and does not offer a free trial.

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

Mullvad has [servers in 41 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Ennek oka a célállomáshoz vezető rövidebb útvonal (kevesebb ugrás).
{ .annotate }

1. Last checked: 2024-04-02

We also think it's better for the security of the VPN provider's private keys if they use [dedicated servers](https://en.wikipedia.org/wiki/Dedicated_hosting_service), instead of cheaper shared solutions (with other customers) such as [virtual private servers](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Independently Audited

Mullvad's VPN clients have been audited by Cure53 and Assured AB in a pentest report [published at cure53.de](https://cure53.de/pentest-report_mullvad_v2.pdf). The security researchers concluded:

> Cure53 and Assured AB are happy with the results of the audit and the software leaves an overall positive impression. With security dedication of the in-house team at the Mullvad VPN compound, the testers have no doubts about the project being on the right track from a security standpoint.

In 2020 a second audit [was announced](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app) and the [final audit report](https://cure53.de/pentest-report_mullvad_2020_v2.pdf) was made available on Cure53's website:

> The results of this May-June 2020 project targeting the Mullvad complex are quite positive. [...] The overall application ecosystem used by Mullvad leaves a sound and structured impression. The overall structure of the application makes it easy to roll out patches and fixes in a structured manner. More than anything, the findings spotted by Cure53 showcase the importance of constantly auditing and re-assessing the current leak vectors, in order to always ensure privacy of the end-users. With that being said, Mullvad does a great job protecting the end-user from common PII leaks and privacy related risks.

In 2021 an infrastructure audit [was announced](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) and the [final audit report](https://cure53.de/pentest-report_mullvad_2021_v1.pdf) was made available on Cure53's website. Another report was commissioned [in June 2022](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data) and is available on [Assured's website](https://assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf).

#### :material-check:{ .pg-green } Open-Source Clients

Mullvad provides the source code for their desktop and mobile clients in their [GitHub organization](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Accepts Cash and Monero

Mullvad, in addition to accepting credit/debit cards and PayPal, accepts Bitcoin, Bitcoin Cash, **Monero** and **cash/local currency** as anonymous forms of payment. Prepaid cards with redeem codes are also available. Mullvad also accepts Swish and bank wire transfers.

#### :material-check:{ .pg-green } WireGuard Support

Mullvad supports the WireGuard® protocol. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Emellett a WireGuard célja, hogy egyszerűbb és hatékonyabb legyen.

Mullvad [recommends](https://mullvad.net/en/help/why-wireguard) the use of WireGuard with their service. It is the default or only protocol on Mullvad's Android, iOS, macOS, and Linux apps, but on Windows you have to [manually enable](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-check:{ .pg-green } IPv6 Support

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) and connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } Remote Port Forwarding

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). Missing this feature could negatively impact certain applications, especially peer-to-peer applications like torrent clients.

#### :material-check:{ .pg-green } Anti-Censorship

Mullvad has obfuscation an mode using [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) which may be useful in situations where VPN protocols like OpenVPN or Wireguard are blocked.

#### :material-check:{ .pg-green } Mobile Clients

Mullvad has published [App Store](https://apps.apple.com/app/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Additional Notes

Mullvad is very transparent about which nodes they [own or rent](https://mullvad.net/en/servers). They use [ShadowSocks](https://shadowsocks.org) in their ShadowSocks + OpenVPN configuration, making them more resistant against firewalls with [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) trying to block VPNs. Supposedly, [China has to use a different method to block ShadowSocks servers](https://github.com/net4people/bbs/issues/22).

## Követelmények

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Fontos megjegyezni, hogy egy VPN szolgáltató használata nem teszi téged anonimmá, de bizonyos helyzetekben jobb magánéletet biztosít. Egy VPN nem illegális tevékenységek eszköze. Ne hagyatkozz "no log" irányelvekre.

</div>

**Tartsd figyelemben, hogy nem állunk kapcsolatban az általunk ajánlott projektek egyikével sem. Ez lehetővé teszi számunkra, hogy teljesen objektív ajánlásokat tegyünk.** Az [alap kritériumaink mellett](about/criteria.md), egyértelmű követelményrendszert dolgoztunk ki minden olyan VPN-szolgáltató számára, amelyet ajánlani kívánunk, beleértve az erős titkosítást, független biztonsági felülvizsgálatokat, modern technológiát és még sok mást. Javasoljuk, hogy ismerkedj meg ezzel a listával, mielőtt kiválasztanál egy VPN-szolgáltatót, és végezz saját kutatásokat, hogy megbizonyosodj arról, hogy az általad választott VPN-szolgáltató a lehető legmegbízhatóbb.

### Technológia

Minden általunk ajánlott VPN-szolgáltatótól elvárjuk, hogy biztosítson OpenVPN konfigurációs fájlokat, amelyeket bármilyen kliensben használni lehet. **Ha** egy VPN saját egyedi klienst biztosít, akkor hálózati kapcsolat megszakadásakor az adatszivárgások megakadályozása miatt egy killswitch beépítését várjuk el.

**Alap elvárások minősítéshez:**

- Olyan erős protokollok támogatása, mint a WireGuard és az OpenVPN.
- Kliensekbe beépített killswitch.
- Multihop támogatás. Multihopping is important to keep data private in case of a single node compromise.
- If VPN clients are provided, they should be [open source](https://en.wikipedia.org/wiki/Open_source), like the VPN software they generally have built into them. Úgy véljük, hogy a [forráskód](https://en.wikipedia.org/wiki/Source_code) elérhetősége nagyobb átláthatóságot biztosít arról, hogy az eszközöd valójában mit csinál.

**Legjobb Esetben:**

- Killswitch jól konfigurálható beállításokkal (engedélyezés/tiltás bizonyos hálózatokon, indításkor, stb.)
- Könnyen használható VPN kliensek
- [IPv6](https://en.wikipedia.org/wiki/IPv6) támogatása. Elvárjuk, hogy szerverek engedélyezzék az IPv6-on keresztül érkező kapcsolatokat, és lehetővé tegyék IPv6-címeken üzemeltetett szolgáltatások elérését.
- A [távoli port forwardolás](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) képessége segíti a P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) fájlmegosztó szoftverek használatát vagy egy szerver (pl. Mumble) üzemeltetése esetén a kapcsolatok létrehozását.
- Obfuscation technology which pads data packets with random data to circumvent internet censorship.

### Adatvédelem

Jobban szeretjük, ha az általunk ajánlott szolgáltatók a lehető legkevesebb adatot gyűjtik. Személyes adatok nem gyűjtése a regisztráció során, és anonim fizetési formák elfogadása elvárás.

**Alap elvárások minősítéshez:**

- [Anoním kriptovaluta](cryptocurrency.md) **, vagy** készpénzes fizetési lehetőség.
- A regisztrációhoz nincs szükség személyes adatokra: Csak felhasználónév, jelszó és legfeljebb email cím.

**Legjobb Esetben:**

- Elfogad több [anonim fizetési lehetőséget](advanced/payments.md).
- Nem fogad el személyes adatokat (automatikusan generált felhasználónév, nincs szükség email címre, stb.).

### Adatbiztonság

Egy VPN értelmetlen, ha még megfelelő biztonságot sem tud nyújtani. Minden általunk ajánlott szolgáltatótól elvárjuk, hogy betartsa az OpenVPN kapcsolataikra vonatkozó jelenlegi biztonsági szabványokat. Ideális esetben alapértelmezés szerint jövőbelátóbb titkosítási sémákat használnának. Azt is elvárjuk, hogy egy független harmadik fél vizsgálja felül a szolgáltató biztonságát, ideális esetben nagyon átfogó módon és ismételten (évente).

**Alap elvárások minősítéshez:**

- Erős Titkosítási Rendszerek: OpenVPN SHA-256 hitelesítssel; RSA-2048 vagy jobb handshake; AES-256-GCM vagy AES-256-CBC adattitkosítás.
- Forward Secrecy.
- Közzétett biztonsági felülvizsgálatok egy megbízható harmadik feles cégtől.

**Legjobb Esetben:**

- Legerősebb Titkosítás: RSA-4096.
- Forward Secrecy.
- Széleskürű és közzétett biztonsági felülvizsgálatok egy megbízható harmadik feles cégtől.
- Bug-bounty programok és/vagy összehangolt sebezhetőség-közzétételi folyamat.

### Bizalom

A pénzügyeidet sem bíznád egy hamis személyazonosságú valakire, miért bíznád rá az internetes adataidat? Az általunk ajánlott szolgáltatóktól elvárjuk, hogy nyilvánosak legyenek a tulajdonlásukról vagy vezetésükről. Szeretnénk továbbá gyakori átláthatósági jelentéseket látni, különösen a kormányzati kérelmek kezelésének módját illetően.

**Alap elvárások minősítéshez:**

- Nyilvános vezetés vagy tulajdonlás.

**Legjobb esetben:**

- Nyilvános vezetés.
- Gyakori átláthatósági jelentések.

### Marketing

Az általunk ajánlott VPN-szolgáltatóknál felelős marketinget szeretünk látni.

**Alap elvárások minősítéshez:**

- Saját üzemeltetésű analitikai rendszerrel kell rendelkeznie (azaz nem Google Analytics). A szolgáltató webhelyének szintén be kell tartania a [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) kéréseket is, a követést elutasítani kívánó személyek számára.

Nem használhat felelőtlen marketinget:

- Az anonimitás 100%-os védelmének garantálása. Ha valaki azt állítja, hogy valami 100%-os, az azt jelenti, hogy nincs bizonyosság meghibásodásra. Tudjuk, hogy személyek elég könnyen és számos módon deanonimizálni tudják magukat, pl.:
    - Reusing personal information (e.g., email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
    - [Böngésző fingerprintelés](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Azt állítja, hogy egy egyáramkörös VPN "anonimabb", mint a Tor, amely egy három vagy több ugrásból álló, rendszeresen változó áramkör.
- Használjon felelősségteljes nyelvezetet: pl. nyugodtan mondhatja, hogy egy VPN "lecsatlakozott" vagy "nincs csatlakoztatva", azonban azt állítani, hogy valaki "védtelen", "sebezhető" vagy "veszélyeztetett", az riasztó nyelvezet felesleges használata, ami lehet, hogy helytelen is. Lehet, hogy az illető egyszerűen csak egy másik VPN-szolgáltató szolgáltatását, vagy a Tor-t használja.

**Legjobb Esetben:**

A felelős marketing, amely egyszerre oktató és hasznos a fogyasztó számára, a következőket foglalhatja magában:

- Pontos összehasonlítás, hogy mikor használandó a [Tor](tor.md) egy VPN helyett.
- A VPN szolgáltató weboldalának elérhetősége egy [.onion szolgáltatáson](https://en.wikipedia.org/wiki/.onion) keresztül

### További Funkciók

Bár nem szigorúan követelmények, van néhány tényező, amelyet figyelembe vettünk, amikor eldöntöttük, hogy mely szolgáltatókat ajánljuk. These include content blocking functionality, warrant canaries, multihop connections, excellent customer support, the number of allowed simultaneous connections, etc.
