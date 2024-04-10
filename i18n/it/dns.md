---
title: "Risolutori DNS"
icon: material/dns
description: Questi sono alcuni dei fornitori DNS crittografati a cui consigliamo di passare, per sostituire la configurazione predefinita del tuo ISP.
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

I DNS crittografati con server di terze parti dovrebbero essere utilizzati soltanto per aggirare il [blocco DNS](https://en.wikipedia.org/wiki/DNS_blocking) di base, quando si può esser certi che non vi sarà alcuna conseguenza. Il DNS crittografato non ti aiuterà a nascondere alcuna tua attività di navigazione.

[Scopri di più sul DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## Fornitori consigliati

These are our favorite public DNS resolvers based on their privacy and security characteristics, and their worldwide performance. Some of these services offer basic DNS-level blocking of malware or trackers depending on the server you choose, but if you want to be able to see and customize what is blocked you should use a dedicated DNS filtering product instead.

| Fornitore DNS                                                              | Politica sulla Privacy                                                                               | Protocolli                               | Registrazione   | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | Filtraggio                                                                                                                                         | Signed Apple Profile                                                                                                     |
| -------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------- | --------------- | -------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| [**AdGuard Public DNS**](https://adguard-dns.io/en/public-dns.html)        | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                               | Cleartext   DoH/3   DoT   DoQ   DNSCrypt | Parziale[^1]    | Anonymized                                                     | Based on server choice. L'elenco dei filtri utilizzati è disponibile qui. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) | Yes [:octicons-link-external-24:](https://adguard.com/en/blog/encrypted-dns-ios-14.html)                                 |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) | Cleartext   DoH/3   DoT                  | Parziale[^2]    | No                                                             | Based on server choice.                                                                                                                            | No [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846) |
| [**Control D Free DNS**](https://controld.com/free-dns)                    | [:octicons-link-external-24:](https://controld.com/privacy)                                          | Cleartext   DoH/3   DoT   DoQ            | Facoltativa[^3] | No                                                             | Based on server choice.                                                                                                                            | Yes [:octicons-link-external-24:](https://docs.controld.com/docs/macos-platform)                                         |
| [**dns0.eu**](https://dns0.eu)                                             | [:octicons-link-external-24:](https://dns0.eu/privacy)                                               | Cleartext   DoH/3   DoH   DoT   DoQ      | No              | Anonymized                                                     | Based on server choice.                                                                                                                            | Yes [:octicons-link-external-24:](https://dns0.eu/zero.dns0.eu.mobileconfig)                                             |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy)                    | DoH   DoT                                | No[^4]          | No                                                             | Based on server choice. L'elenco dei filtri utilizzati è disponibile qui. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    | Yes [:octicons-link-external-24:](https://mullvad.net/en/blog/profiles-to-configure-our-encrypted-dns-on-apple-devices)  |
| [**Quad9**](https://quad9.net)                                             | [:octicons-link-external-24:](https://quad9.net/privacy/policy)                                      | Cleartext   DoH   DoT   DNSCrypt         | Some[^5]        | Facoltativa                                                    | Based on server choice, malware blocking by default.                                                                                               | Yes [:octicons-link-external-24:](https://quad9.net/news/blog/ios-mobile-provisioning-profiles)                          |

## Self-Hosted DNS Filtering

Una soluzione DNS self-hosted è utile per fornire il filtraggio su piattaforme controllate, come Smart TV e altri dispositivi IoT, poiché non è necessario alcun software lato client.

### Pi-hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](assets/img/dns/pi-hole.svg){ align=right }

**Pi-hole** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

Pi-hole è stato progettato per essere ospitato su un Raspberry Pi, ma non si limita a tale hardware. Il software dispone di un'interfaccia web intuitiva per visualizzare i dettagli e gestire i contenuti bloccati.

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

AdGuard Home dispone di un'interfaccia web raffinata per visualizzare i dettagli e gestire i contenuti bloccati.

[:octicons-home-16: Home](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Codice Sorgente" }

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

## Proxy DNS Crittografati

I software proxy per il DNS crittografato forniscono un proxy locale a cui inoltrare le richieste [DNS non crittografate](advanced/dns-overview.md#unencrypted-dns). Typically, it is used on platforms that don't natively support [encrypted DNS](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

<div class="admonition recommendation" markdown>

![Logo di RethinkDNS](assets/img/android/rethinkdns.svg#only-light){ align=right }
![Logo di RethinkDNS](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** è un client Android open-source che supporta [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), [DNS-over-TLS](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) e DNS Proxy, oltre a memorizzare nella cache le risposte DNS, registrare localmente le richieste DNS, nonché utilizzabile come firewall.

[:octicons-home-16: Homepage](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

### dnscrypt-proxy

<div class="admonition recommendation" markdown>

![dnscrypt-proxy logo](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**dnscrypt-proxy** is a DNS proxy with support for [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), and [Anonymized DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

[:octicons-repo-16: Repository](https://github.com/DNSCrypt/dnscrypt-proxy){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Codice sorgente" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-windows11: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

The anonymized DNS feature does [not](advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns) anonymize other network traffic.

</div>

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

### Requisiti minimi

- [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- [Minimizzazione QNAME](advanced/dns-overview.md#what-is-qname-minimization).
- Anonymize [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) or disable it by default.
- Preferire il supporto di [anycast](https://it.wikipedia.org/wiki/Anycast) o il supporto di geo-steering

[^1]: AdGuard memorizza le statistiche aggregate sulle prestazioni dei propri server DNS, ossia il numero di richieste complete a un server in particolare, il numero di richieste bloccate e la velocità d'elaborazione delle richieste. Inoltre, conserva e memorizza il database dei domini richiesti nelle ultime 24 ore. "Necessitiamo di queste informazioni per identificare e bloccare i nuovi tracciatori e minacce." "Inoltre, registriamo quante volte un tracciatore è stato bloccato. Necessitiamo di queste informazioni per rimuovere le regole obsolete dai nostri filtri." [https://adguard.com/it/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: Cloudflare raccoglie e memorizza soltanto i dati limitati delle richieste DNS inviate al risolutore 1.1.1.1. Il servizio del risolutore 1.1.1.1 non registra i dati personali e, gran parte dei dati delle richieste limitate e non personalmente identificabili, sono memorizzati soltanto per 25 ore. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: Control D registra soltanto i risolutori Premium con profili DNS personalizzati. I risolutori gratuiti non registrano dati. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: Il servizio DNS di Mullvad è disponibile per tutti, abbonati a Mullvad VPN e non. La loro politica sulla privacy dichiara esplicitamente che non registrano in alcun modo le richieste DNS. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^5]: Quad9 raccoglie alcuni dati per monitorare e rispondere a eventuali minacce. Tali dati potrebbero essere poi rimescolati e condivisi, ad esempio ai fini della ricerca sulla sicurezza. Quad9 non raccoglie o registra gli indirizzi IP o qualsiasi altro dato ritenuto personalmente identificabile. [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
