---
title: "DNS Resolverek"
icon: material/dns
description: Ezekre a titkosított DNS-szolgáltatókra való átállást javasoljuk, hogy lecseréld az internetszolgáltatód alapértelmezett konfigurációját.
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

Titkosított DNS-t harmadik féltől származó szerverekkel csak alapvető [DNS-blokkolás](https://en.wikipedia.org/wiki/DNS_blocking) megkerülésére kellene használni, ha biztos vagy benne, hogy annak nem lesz semmilyen következménye. A titkosított DNS nem fog segíteni elrejteni a böngészési tevékenységedet.

[További Információk a DNS-ről :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## Ajánlott Szolgáltatók

These are our favorite public DNS resolvers based on their privacy and security characteristics, and their worldwide performance. Some of these services offer basic DNS-level blocking of malware or trackers depending on the server you choose, but if you want to be able to see and customize what is blocked you should use a dedicated DNS filtering product instead.

| DNS Szolgáltatók                                                           | Adatvédelmi Tájékoztató                                                                              | Protokollok                              | Naplózás        | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | Szűrés                                                                                                                                | Signed Apple Profile                                                                                                     |
| -------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------- | --------------- | -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| [**AdGuard Public DNS**](https://adguard-dns.io/en/public-dns.html)        | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                               | Cleartext   DoH/3   DoT   DoQ   DNSCrypt | Némi[^1]        | Anonymized                                                     | Based on server choice. A használt szűrőlista itt található. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) | Yes [:octicons-link-external-24:](https://adguard.com/en/blog/encrypted-dns-ios-14.html)                                 |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) | Cleartext   DoH/3   DoT                  | Némi[^2]        | Nem                                                            | Based on server choice.                                                                                                               | No [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846) |
| [**Control D Free DNS**](https://controld.com/free-dns)                    | [:octicons-link-external-24:](https://controld.com/privacy)                                          | Cleartext   DoH/3   DoT   DoQ            | Választható[^3] | Nem                                                            | Based on server choice.                                                                                                               | Yes [:octicons-link-external-24:](https://docs.controld.com/docs/macos-platform)                                         |
| [**dns0.eu**](https://dns0.eu)                                             | [:octicons-link-external-24:](https://dns0.eu/privacy)                                               | Cleartext   DoH/3   DoH   DoT   DoQ      | Nem             | Anonymized                                                     | Based on server choice.                                                                                                               | Yes [:octicons-link-external-24:](https://dns0.eu/zero.dns0.eu.mobileconfig)                                             |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy)                    | DoH   DoT                                | Nem[^4]         | Nem                                                            | Based on server choice. A használt szűrőlista itt található. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    | Yes [:octicons-link-external-24:](https://mullvad.net/en/blog/profiles-to-configure-our-encrypted-dns-on-apple-devices)  |
| [**Quad9**](https://quad9.net)                                             | [:octicons-link-external-24:](https://quad9.net/privacy/policy)                                      | Cleartext   DoH   DoT   DNSCrypt         | Some[^5]        | Választható                                                    | Based on server choice, malware blocking by default.                                                                                  | Yes [:octicons-link-external-24:](https://quad9.net/news/blog/ios-mobile-provisioning-profiles)                          |

## Self-Hosted DNS Filtering

Egy saját üzemeltetésű DNS-megoldás hasznos ellenőrzött platformokon, például Smart TV-ken és más IoT-eszközökön történő szűrés biztosításához, mivel nincs szükség kliensoldali szoftverre.

### Pi-hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](assets/img/dns/pi-hole.svg){ align=right }

**Pi-hole** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

A Pi-hole-t úgy tervezték, hogy egy Raspberry Pi-n lehessen üzemeltetni, de az nem korlátozott erre a hardverre. Az szoftver egy kifinomult webes felületet kínál az betekintések megtekintéséhez és blokkolt tartalmak kezeléséhez.

[:octicons-home-16: Homepage](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Source Code" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title=Contribute }

</details>

</div>

### AdGuard Home

<div class="admonition recommendation" markdown>

![AdGuard Home logo](assets/img/dns/adguard-home.svg){ align=right }

**AdGuard Home** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

Az AdGuard Home egy kifinomult webes felületet kínál az betekintések megtekintéséhez és blokkolt tartalmak kezeléséhez.

[:octicons-home-16: Honlap](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Adatvédelmi Tájékoztató" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=Dokumentáció}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Forráskód" }

</details>

</div>

## Cloud-Based DNS Filtering

These DNS filtering solutions offer a web dashboard where you can customize the blocklists to your exact needs, similarly to a Pi-hole. These services are usually easier to set up and configure than self-hosted services like the ones above, and can be used more easily across multiple networks (self-hosted solutions are typically restricted to your home/local network unless you set up a more advanced configuration).

### Control D

<div class="admonition recommendation" markdown>

![Control D logo](assets/img/dns/control-d.svg){ align=right }

**Control D** is a customizable DNS service which lets you block security threats, unwanted content, and advertisements on a DNS level. In addition to their paid plans, they offer a number of preconfigured DNS resolvers you can use for free.

[:octicons-home-16: Homepage](https://controld.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://controld.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.controld.com/docs/getting-started){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/Control-D-Inc/ctrld){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-apple: macOS](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-linux: Linux](https://docs.controld.com/docs/ctrld)
- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.controld.setuputility)
- [:simple-appstore: App Store](https://apps.apple.com/app/1518799460)
- [:simple-github: GitHub](https://github.com/Control-D-Inc/ctrld/releases/tag/v1.3.5)

</details>

</div>

### NextDNS

<div class="admonition recommendation" markdown>

![NextDNS logo](assets/img/dns/nextdns.svg){ align=right }

**NextDNS** is a customizable DNS service which lets you block security threats, unwanted content, and advertisements on a DNS level. They offer a fully functional free plan for limited use.

[:octicons-home-16: Homepage](https://nextdns.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextdns.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.nextdns.io){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/nextdns/nextdns){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://github.com/nextdns/nextdns/wiki/Windows)
- [:simple-apple: macOS](https://apps.apple.com/us/app/nextdns/id1464122853)
- [:simple-linux: Linux](https://github.com/nextdns/nextdns/wiki)
- [:simple-appstore: App Store](https://apps.apple.com/app/nextdns/id1463342498)
- [:simple-github: GitHub](https://github.com/nextdns/nextdns/releases)

</details>

</div>

When used with an account, NextDNS will enable insights and logging features by default (as some features require it). You can choose retention time and log storage location for any logs you choose to keep, or disable logs altogether.

NextDNS's free plan is fully functional, but should not be relied upon for security or other critical filtering applications, because after 300,000 DNS queries in a month all filtering, logging, and other account-based functionality is disabled. It can still be used as a regular DNS provider after that point, so your devices will continue to function and make secure queries via DNS-over-HTTPS, just without your filter lists.

NextDNS also offers public DNS-over-HTTPS service at `https://dns.nextdns.io` and DNS-over-TLS/QUIC at `dns.nextdns.io`, which are available by default in Firefox and Chromium, and subject to their default no-logging [privacy policy](https://nextdns.io/privacy).

## Titkosított DNS proxyk

Egy titkosított DNS proxy szoftver helyi proxy-t biztosít a [titkosítatlan DNS](advanced/dns-overview.md#unencrypted-dns) resolver számára, amelyhez majd továbbít. Typically, it is used on platforms that don't natively support [encrypted DNS](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ align=right }
![RethinkDNS logo](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

A **RethinkDNS** egy nyílt forráskódú Android kliens, amely támogatja a [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), [DNS-over-TLS](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) és DNS Proxy funkciókat, valamint a DNS-válaszok gyorsítótárazását, a DNS-lekérdezések helyi naplózását, de használható tűzfalként is.

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

<div class="admonition warning" markdown>
<p class="admonition-title">Figyelmeztetés</p>

The anonymized DNS feature does [not](advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns) anonymize other network traffic.

</div>

## Követelmények

**Tartsd figyelemben, hogy nem állunk kapcsolatban az általunk ajánlott projektek egyikével sem.** Az [alap kritériumaink mellett](about/criteria.md), egyértelmű követelményrendszert dolgoztunk ki, hogy objektív ajánlásokat tudjunk tenni. Javasoljuk, hogy ismerkedj meg ezzel a listával, mielőtt kiválasztanál egy projektet, és végezz saját kutatásokat, hogy megbizonyosodj arról, hogy ez a megfelelő választás számodra.

### Alap elvárások

- [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- [QNAME Minimalizáció](advanced/dns-overview.md#what-is-qname-minimization).
- Anonymize [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) or disable it by default.
- Előnyben részesíti az [anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods), vagy a geo-steering támogatását.

[^1]: Az AdGuard tárolja a DNS szervereik összesített teljesítményméréseit, nevezetesen az adott szerverhez érkező teljes kérések számát, a blokkolt kérések számát és a kérések feldolgozásának sebességét. Az elmúlt 24 órában igényelt domainek adatbázisát is eltárolják. "We need this information to identify and block new trackers and threats." "We also log how many times this or that tracker has been blocked. We need this information to remove outdated rules from our filters." [https://adguard.com/hu/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: A Cloudflare csak azokat a korlátozott DNS-lekérdezési adatokat gyűjti és tárolja ami az 1.1.1.1 resolverhez érkezik. Az 1.1.1.1 resolver szolgáltatás nem naplóz személyes adatokat, és a korlátozott, személyazonosításra nem alkalmas lekérdezési adatok nagy részét csak 25 órán keresztül tárolja. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: A Control D csak az egyedi DNS-profilokkal rendelkező Premium resolverek esetében naplóz. Az ingyenes resolverek nem naplóznak adatokat. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: A Mullvad DNS szolgáltatása a Mullvad VPN előfizetői és nem előfizetői számára egyaránt elérhető. Az adatvédelmi irányelvük kifejezetten azt állítja, hogy semmilyen módon nem naplóznak DNS-kéréseket. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^5]: A Quad9 bizonyos adatokat a fenyegetések megfigyelése és elhárítása céljából gyűjt. Ezek az adatok ezután összekeverhetők és megoszthatók, például biztonsági kutatások céljából. A Quad9 nem gyűjt vagy rögzít IP-címeket vagy más, személyazonosításra alkalmasnak ítélt adatokat. [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
