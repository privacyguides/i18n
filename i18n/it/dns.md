---
title: "Risolutori DNS"
icon: material/dns
description: Questi sono alcuni dei fornitori DNS crittografati cui consigliamo di passare, per sostituire la configurazione predefinita del tuo ISP.
cover: dns.webp
---

I DNS crittografati con server di terze parti dovrebbero essere utilizzati soltanto per aggirare il [blocco DNS](https://en.wikipedia.org/wiki/DNS_blocking) di base, quando si può esser certi che non vi sarà alcuna conseguenza. Il DNS crittografato non ti aiuterà a nascondere alcuna tua attività di navigazione.

[Scopri di più sul DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## Fornitori consigliati

| Fornitore DNS                                                                   | Politica sulla Privacy                                                                                | Protocolli                                                    | Registrazione   | ECS         | Filtraggio                                                                                                                                                      |
| ------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------- | --------------- | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**AdGuard**](https://adguard.com/en/adguard-dns/overview.html)                 | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                                | Cleartext <br> DoH/3 <br> DoT <br> DNSCrypt | Parziale[^1]    | No          | Secondo la configurazione personale. L'elenco dei filtri utilizzati è disponibile qui. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setting-up-1.1.1.1/) | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/) | Cleartext <br> DoH/3 <br> DoT                     | Parziale[^2]    | No          | Secondo la configurazione personale.                                                                                                                            |
| [**Control D**](https://controld.com/free-dns)                                  | [:octicons-link-external-24:](https://controld.com/privacy)                                           | Cleartext <br> DoH/3 <br> DoT <br> DoQ      | Facoltativa[^3] | No          | Secondo la configurazione personale.                                                                                                                            |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls)      | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy/)                    | DoH <br> DoT                                            | No[^4]          | No          | Secondo la configurazione personale. L'elenco dei filtri utilizzati è disponibile qui. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    |
| [**NextDNS**](https://www.nextdns.io)                                           | [:octicons-link-external-24:](https://www.nextdns.io/privacy)                                         | Cleartext <br> DoH/3 <br> DoT <br> DoQ      | Facoltativa[^5] | Facoltativa | Secondo la configurazione personale.                                                                                                                            |
| [**Quad9**](https://quad9.net)                                                  | [:octicons-link-external-24:](https://quad9.net/privacy/policy/)                                      | Cleartext <br> DoH <br> DoT <br> DNSCrypt   | Parziale[^6]    | Facoltativa | Secondo la configurazione personale, blocco dei malware predefinito.                                                                                            |

### Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

!!! esempio "Questa sezione è nuova"

    Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Sono molti i fattori presi in considerazione e discussi quando raccomandiamo un progetto e documentare ogni singolo fattore è un lavoro in corso.

- Deve supportare le [DNSSEC](advanced/dns-overview.md#what-is-dnssec)
- [Minimizzazione QNAME](advanced/dns-overview.md#what-is-qname-minimization).
- Consente di disabilitare la [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs)
- Preferire il supporto di [anycast](https://it.wikipedia.org/wiki/Anycast) o il supporto di geo-steering

## Supporto Nativo del Sistema Operativo

### Android

Android 9 e successive supportano il 'DNS over TLS'. Le impostazioni si possono trovare in: **Impostazioni** &rarr; **Rete e Internet** &rarr; **DNS Privato**.

### Dispositivi Apple

Le versioni più recenti di iOS, iPadOS, tvOS e macOS, supportano sia DoT che DoH. Entrambi i protocolli sono supportati nativamente tramite i [profili di configurazione](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) o tramite l'[API delle Impostazioni DNS](https://developer.apple.com/documentation/networkextension/dns_settings).

Dopo l'installazione di un profilo di configurazione o di un'app che utilizza l'API delle Impostazioni DNS, è possibile selezionare la configurazione DNS. Se una VPN è attiva, la risoluzione nel tunnel VPN utilizzerà le impostazioni DNS della VPN e non le impostazioni di sistema.

#### Profili firmati

Apple non fornisce un'interfaccia nativa per la creazione di profili DNS crittografati. [Secure DNS profile creator](https://dns.notjakob.com/tool.html) è uno strumento non ufficiale per creare i propri profili DNS crittografati, tuttavia, non saranno firmati. I profili firmati sono da preferire; la firma convalida l'origine di un profilo e contribuisce a garantire l'integrità. Un'etichetta verde "Verificato" è data ai profili di configurazione firmati. Per ulteriori informazioni sulla firma del codice, consulta [Informazioni sulla firma del codice](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html). **I profili firmati** sono offerti da [AdGuard](https://adguard.com/en/blog/encrypted-dns-ios-14.html), [NextDNS](https://apple.nextdns.io) e [Quad9](https://www.quad9.net/news/blog/ios-mobile-provisioning-profiles/).

!!! info

    `systemd-resolved`, utilizzato da molte distribuzioni Linux per effettuare le ricerche DNS, non supporta ancora [DoH](https://github.com/systemd/systemd/issues/8639). Se vuoi usare DoH, è necessario installare un proxy come [dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy) e [configurarlo] (https://wiki.archlinux.org/title/Dnscrypt-proxy) per prendere tutte le query DNS dal resolver di sistema e inoltrarle tramite HTTPS.

## Proxy DNS Crittografati

I software proxy per il DNS crittografato forniscono un proxy locale a cui inoltrare le richieste [DNS non crittografate](advanced/dns-overview.md#unencrypted-dns). Tipicamente, è utilizzato sulle piattaforme che non supportano nativamente il [DNS crittografato](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

!!! recommendation

    ![Logo di RethinkDNS](assets/img/android/rethinkdns.svg#only-light){ align=right }
    ![Logo di RethinkDNS](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }
    
    **RethinkDNS** è un client Android open-source che supporta [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), [DNS-over-TLS](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) e DNS Proxy, oltre a memorizzare nella cache le risposte DNS, registrare localmente le richieste DNS, nonché utilizzabile come firewall.
    
    [:octicons-home-16: Home](https://rethinkdns.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://docs.rethinkdns.com/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Codice Sorgente" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
        - [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

### dnscrypt-proxy

!!! recommendation

    ![Logo di dnscrypt-proxy](assets/img/dns/dnscrypt-proxy.svg){ align=right }
    
    **dnscrypt-proxy** è un proxy DNS con supporto a [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh) e [DNS Anonimizzato](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).
    
    !!! warning "La funzione DNS anonimizzato [**non**](advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns) rende anonimo il resto del traffico di rete."
    
    [:octicons-repo-16: Repository](https://github.com/DNSCrypt/dnscrypt-proxy){ .md-button .md-button--primary }
    [:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title=Contribuisci }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
        - [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
        - [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

## Soluzioni ospitate autonomamente

Una soluzione DNS self-hosted è utile per fornire il filtraggio su piattaforme controllate, come Smart TV e altri dispositivi IoT, poiché non è necessario alcun software lato client.

### AdGuard Home

!!! recommendation

    ![Logo di AdGuard Home](assets/img/dns/adguard-home.svg){ align=right }
    
    **AdGuard Home** è un [DNS-sinkhole](https://wikipedia.org/wiki/DNS_sinkhole) open source che utilizza il [filtraggio DNS](https://www.cloudflare.com/learning/access-management/what-is-dns-filtering/) per bloccare i contenuti web indesiderati, come le inserzioni.
    
    AdGuard Home dispone di un'interfaccia web raffinata per visualizzare i dettagli e gestire i contenuti bloccati.
    
    [:octicons-home-16: Home](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Codice Sorgente" }

### Pi-hole

!!! recommendation

    ![Logo di Pi-hole](assets/img/dns/pi-hole.svg){ align=right }
    
    **Pi-hole** è un [DNS-sinkhole](https://wikipedia.org/wiki/DNS_sinkhole) open source che utilizza il [filtraggio DNS](https://www.cloudflare.com/learning/access-management/what-is-dns-filtering/) per bloccare i contenuti web indesiderati, come le inserzioni.
    
    Pi-hole è stato progettato per essere ospitato su un Raspberry Pi, ma non si limita a tale hardware. Il software dispone di un'interfaccia web intuitiva per visualizzare i dettagli e gestire i contenuti bloccati.
    
    [:octicons-home-16: Home](https://pi-hole.net/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://pi-hole.net/privacy/){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://docs.pi-hole.net/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title=Contribuisci }

[^1]: AdGuard memorizza le statistiche aggregate sulle prestazioni dei propri server DNS, ossia il numero di richieste complete a un server in particolare, il numero di richieste bloccate e la velocità d'elaborazione delle richieste. Inoltre, conserva e memorizza il database dei domini richiesti nelle ultime 24 ore. "Necessitiamo di queste informazioni per identificare e bloccare i nuovi tracciatori e minacce". "Inoltre, registriamo quante volte un tracciatore è stato bloccato. Necessitiamo di queste informazioni per rimuovere le regole obsolete dai nostri filtri." [https://adguard.com/it/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: Cloudflare raccoglie e memorizza soltanto i dati limitati delle richieste DNS inviate al risolutore 1.1.1.1. Il servizio del risolutore 1.1.1.1 non registra i dati personali e, gran parte dei dati delle richieste limitate e non personalmente identificabili, sono memorizzati soltanto per 25 ore. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/)
[^3]: Control D registra soltanto i risolutori Premium con profili DNS personalizzati. I risolutori gratuiti non registrano dati. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: Il servizio DNS di Mullvad è disponibile per tutti, abbonati a Mullvad VPN e non. La loro politica sulla privacy dichiara esplicitamente che non registrano in alcun modo le richieste DNS. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy/)
[^5]: NextDNS può fornire dettagli e funzionalità di registrazione su richiesta dell'utente. Puoi decidere il tempo di conservazione e la posizione dell'archivio per tutti i dati che decidi di registrare. A meno che non sia richiesto specificamente, nessun dato viene registrato. [https://nextdns.io/privacy](https://nextdns.io/privacy)
[^6]: Quad9 raccoglie alcuni dati per monitorare e rispondere a eventuali minacce. Tali dati potrebbero essere poi rimescolati e condivisi, ad esempio ai fini della ricerca sulla sicurezza. Quad9 non raccoglie o registra gli indirizzi IP o qualsiasi altro dato ritenuto personalmente identificabile. [https://www.quad9.net/privacy/policy/](https://www.quad9.net/privacy/policy/)
