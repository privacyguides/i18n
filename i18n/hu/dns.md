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

| DNS Szolgáltatók                                                           | Adatvédelmi Tájékoztató                                                                              | Protokollok                                                                  | Naplózás        | ECS         | Szűrés                                                                                                                                         |
| -------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | --------------- | ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| [**AdGuard**](https://adguard.com/en/adguard-dns/overview.html)            | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                               | Cleartext <br> DoH/3 <br> DoT <br> DoQ <br> DNSCrypt | Némi[^1]        | Yes         | Based on personal configuration. A használt szűrőlista itt található. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) | Nyílt szöveg <br> DoH/3 <br> DoT                                 | Némi[^2]        | Nem         | Based on personal configuration.                                                                                                               |
| [**Control D**](https://controld.com/free-dns)                             | [:octicons-link-external-24:](https://controld.com/privacy)                                          | Nyílt szöveg <br> DoH/3 <br> DoT <br> DoQ                  | Választható[^3] | Nem         | Based on personal configuration.                                                                                                               |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy)                    | DoH <br> DoT                                                           | Nem[^4]         | Nem         | Based on personal configuration. A használt szűrőlista itt található. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    |
| [**NextDNS**](https://nextdns.io)                                          | [:octicons-link-external-24:](https://nextdns.io/privacy)                                            | Nyílt szöveg <br> DoH/3 <br> DoT <br> DoQ                  | Választható[^5] | Választható | Based on personal configuration.                                                                                                               |
| [**Quad9**](https://quad9.net)                                             | [:octicons-link-external-24:](https://quad9.net/privacy/policy)                                      | Nyílt szöveg <br> DoH <br> DoT <br> DNSCrypt               | Némi[^6]        | Választható | Based on personal configuration, Malware blocking by default.                                                                                  |

### Követelmények

**Tartsd figyelemben, hogy nem állunk kapcsolatban az általunk ajánlott projektek egyikével sem.** Az [alap kritériumaink mellett](about/criteria.md), egyértelmű követelményrendszert dolgoztunk ki, hogy objektív ajánlásokat tudjunk tenni. Javasoljuk, hogy ismerkedj meg ezzel a listával, mielőtt kiválasztanál egy projektet, és végezz saját kutatásokat, hogy megbizonyosodj arról, hogy ez a megfelelő választás számodra.

- Támogatnia kell a [DNSSEC](advanced/dns-overview.md#what-is-dnssec)-et.
- [QNAME Minimalizáció](advanced/dns-overview.md#what-is-qname-minimization).
- Lehetővé teszi az [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) letiltását.
- Előnyben részesíti az [anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods), vagy a geo-steering támogatását.

## Native Operating System Support

### Android

Az Android 9 és újabb verziói támogatják a DNS-t TLS-en keresztül. A beállítások megtalálhatók itt: **Beállítások** &rarr; **Hálózat és Internet** &rarr; **Privát DNS**.

### Apple Devices

Az iOS, iPadOS, tvOS és macOS legújabb verziói támogatják a DoT és a DoH funkciót is. Mindkét protokoll alapból támogatva van a [konfigurációs profilok](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) vagy a [DNS-beállítás API](https://developer.apple.com/documentation/networkextension/dns_settings)-n keresztül.

Egy konfigurációs profilt vagy egy DNS-beállítások API-t használó alkalmazás telepítése után kiválasztható a DNS-konfiguráció. Ha egy VPN aktív, a VPN-alagúton belüli elosztás a VPN DNS-beállításait fogja használni, nem pedig a rendszerbeállításokat.

#### Aláírt Profilok

Az Apple nem biztosít natív felületet titkosított DNS-profilok létrehozásához. A [Secure DNS profile creator](https://dns.notjakob.com/tool.html) egy nem hivatalos eszköz saját titkosított DNS-profilok létrehozására, azonban ezek a profilok nem lesznek aláírva. Az aláírt profilok előnyben részesítendők; az aláírás igazolja a profil eredetét, és segít biztosítani a profilok integritását. Az aláírt konfigurációs profilok zöld "Ellenőrzött" címkét kapnak. A kódaláírással kapcsolatos további információkért lásd: [About Code Signing](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html). **Signed profiles** are offered by [AdGuard](https://adguard.com/en/blog/encrypted-dns-ios-14.html), [NextDNS](https://apple.nextdns.io), and [Quad9](https://quad9.net/news/blog/ios-mobile-provisioning-profiles).

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

A `systemd-resolved`, amelyet sok Linux disztribúció használ a DNS-lekérdezéseikhez, még nem [támogatja a DoH-t](https://github.com/systemd/systemd/issues/8639). Ha a DoH-t szeretnéd használni, telepítened kell egy proxyt, mint például a [dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy) és [konfigurálnod kell azt](https://wiki.archlinux.org/title/Dnscrypt-proxy), hogy az átvegye az összes DNS-lekérdezést a rendszer resolverjétől, és azokat HTTPS-en keresztül továbbítsa.

</div>

## Titkosított DNS proxyk

Egy titkosított DNS proxy szoftver helyi proxy-t biztosít a [titkosítatlan DNS](advanced/dns-overview.md#unencrypted-dns) resolver számára, amelyhez majd továbbít. Általában olyan platformokon használatos, amelyek nem támogatják natívan a [titkosított DNS-t](advanced/dns-overview.md#what-is-encrypted-dns).

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

![dnscrypt-proxy logo](assets/img/dns/dns/dnscrypt-proxy.svg){ align=right }

A **dnscrypt-proxy** egy DNS-proxy, amely támogatja a [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh) és [Anonymizált DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS) funkciókat.

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

## Saját Üzemeltetésű Megoldások

Egy saját üzemeltetésű DNS-megoldás hasznos ellenőrzött platformokon, például Smart TV-ken és más IoT-eszközökön történő szűrés biztosításához, mivel nincs szükség kliensoldali szoftverre.

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

[^1]: Az AdGuard tárolja a DNS szervereik összesített teljesítményméréseit, nevezetesen az adott szerverhez érkező teljes kérések számát, a blokkolt kérések számát és a kérések feldolgozásának sebességét. Az elmúlt 24 órában igényelt domainek adatbázisát is eltárolják. "We need this information to identify and block new trackers and threats." "We also log how many times this or that tracker has been blocked. We need this information to remove outdated rules from our filters." [https://adguard.com/hu/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: A Cloudflare csak azokat a korlátozott DNS-lekérdezési adatokat gyűjti és tárolja ami az 1.1.1.1 resolverhez érkezik. Az 1.1.1.1 resolver szolgáltatás nem naplóz személyes adatokat, és a korlátozott, személyazonosításra nem alkalmas lekérdezési adatok nagy részét csak 25 órán keresztül tárolja. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: A Control D csak az egyedi DNS-profilokkal rendelkező Premium resolverek esetében naplóz. Az ingyenes resolverek nem naplóznak adatokat. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: A Mullvad DNS szolgáltatása a Mullvad VPN előfizetői és nem előfizetői számára egyaránt elérhető. Az adatvédelmi irányelvük kifejezetten azt állítja, hogy semmilyen módon nem naplóznak DNS-kéréseket. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^5]: When used with an account, NextDNS will enable insights and logging features by default (as some features require it). You can choose retention time and log storage location for any logs you choose to keep, or disable logs altogether. If used without an account, no data is logged. [https://nextdns.io/privacy](https://nextdns.io/privacy)
[^6]: A Quad9 bizonyos adatokat a fenyegetések megfigyelése és elhárítása céljából gyűjt. Ezek az adatok ezután összekeverhetők és megoszthatók, például biztonsági kutatások céljából. A Quad9 nem gyűjt vagy rögzít IP-címeket vagy más, személyazonosításra alkalmasnak ítélt adatokat. [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
