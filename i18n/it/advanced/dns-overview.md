---
title: "Panoramica DNS"
icon: material/dns
description: Il Sistema dei Nomi di Dominio è la "rubrica dell'Internet", aiutando il tuo browser a trovare il sito web che sta cercando.
---

The [Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System) is the 'phone book of the Internet'. Il DNS traduce i nomi di dominio in indirizzi IP, così che i browser e altri servizi possano caricare le risorse di Internet, tramite una rete decentralizzata di server.

## Cos'è il DNS?

Quando visiti un sito web, è restituito un indirizzo numerico. Ad esempio, quando visiti `privacyguides.org`, viene restituito l'indirizzo `192.98.54.105`.

Il DNS esiste dagli [albori](https://en.wikipedia.org/wiki/Domain_Name_System#History) di Internet. Le richieste DNS da e verso i server DNS **non** sono generalmente crittografate. In un ambiente residenziale, un cliente riceve dei server dall'ISP tramite [DHCP](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol).

Le richieste DNS non crittografate sono facilmente **sorvegliabili** e **modificabili** durante il transito. In alcune parti del mondo, gli ISP devono eseguire un primitivo [filtraggio DNS](https://en.wikipedia.org/wiki/DNS_blocking). Quando richiedi il blocco dell'indirizzo IP di un dominio, il server potrebbe non rispondere o fornire un indirizzo IP differente. Poiché il protocollo DNS non è crittografato, l'ISP (o qualsiasi operatore della rete), può utilizzare la [DPI](https://en.wikipedia.org/wiki/Deep_packet_inspection) per monitorare le richieste. Gli ISP possono inoltre bloccare le richieste secondo caratteristiche comuni, indipendentemente da quale server DNS è utilizzato.

Di seguito, discutiamo e forniamo un tutorial per provare ciò che un osservatore esterno possa vedere, utilizzando il DNS non crittografato e il [DNS crittografato](#what-is-encrypted-dns).

### DNS non crittografato

1. Utilizzando [`tshark`](https://wireshark.org/docs/man-pages/tshark.html) (parte del progetto [Wireshark](https://en.wikipedia.org/wiki/Wireshark)) possiamo monitorare e registrare il flusso di pacchetti Internet. Il comando registra i pacchetti che soddisfano le regole specificate:

    ```bash
    tshark -w /tmp/dns.pcap udp port 53 and host 1.1.1.1 or host 8.8.8.8
    ```

2. We can then use [`dig`](https://en.wikipedia.org/wiki/Dig_(command)) (Linux, macOS, etc.) or [`nslookup`](https://en.wikipedia.org/wiki/Nslookup) (Windows) to send the DNS lookup to both servers. I software come i browser web, svolgono automaticamente tali ricerche, a meno che non siano configurati per utilizzare il DNS crittografato.

    === "Linux, macOS"

        ```
        dig +noall +answer privacyguides.org @1.1.1.1
        dig +noall +answer privacyguides.org @8.8.8.8
        ```
    === "Windows"

        ```
        nslookup privacyguides.org 1.1.1.1
        nslookup privacyguides.org 8.8.8.8
        ```

3. Next, we want to [analyze](https://wireshark.org/docs/wsug_html_chunked/ChapterIntroduction.html#ChIntroWhatIs) the results:

    === "Wireshark"

        ```
        wireshark -r /tmp/dns.pcap
        ```

    === "tshark"

        ```
        tshark -r /tmp/dns.pcap
        ```

Se esegui il comando di Wireshark precedente, il pannello superiore mostra i "[quadri](https://en.wikipedia.org/wiki/Ethernet_frame)", mentre quello inferiore mostra tutti i dati sul quadro selezionato. Le soluzioni di filtraggio e monitoraggio aziendali (come quelle acquistate dai governi), possono svolgere il processo automaticamente, senza l'interazione umana, e possono aggregare tali quadri per produrre dati statistici, utili all'osservatore della rete.

| N. | Tempo    | Sorgente  | Destinazione | Protocollo | Lunghezza | Info                                                                   |
| -- | -------- | --------- | ------------ | ---------- | --------- | ---------------------------------------------------------------------- |
| 1  | 0.000000 | 192.0.2.1 | 1.1.1.1      | DNS        | 104       | Standard query 0x58ba A privacyguides.org OPT                          |
| 2  | 0.293395 | 1.1.1.1   | 192.0.2.1    | DNS        | 108       | Standard query response 0x58ba A privacyguides.org A 198.98.54.105 OPT |
| 3  | 1.682109 | 192.0.2.1 | 8.8.8.8      | DNS        | 104       | Standard query 0xf1a9 A privacyguides.org OPT                          |
| 4  | 2.154698 | 8.8.8.8   | 192.0.2.1    | DNS        | 108       | Standard query response 0xf1a9 A privacyguides.org A 198.98.54.105 OPT |

Un osservatore potrebbe modificare uno qualsiasi di questi pacchetti.

## Cos'è il "DNS crittografato"?

Il DNS cifrato può fare riferimento a uno dei diversi protocolli, i più comuni dei quali sono [DNSCrypt](#dnscrypt), [DNS over TLS](#dns-over-tls-dot) e [DNS over HTTPS](#dns-over-https-doh).

### DNSCrypt

[**DNSCrypt**](https://en.wikipedia.org/wiki/DNSCrypt) fu uno dei primi metodi per la crittografia delle richieste DNS. DNSCrypt opera sulla porta 443 e funziona con entrambi i protocolli di trasporto TCP e UDP. DNSCrypt has never been submitted to the [Internet Engineering Task Force (IETF)](https://en.wikipedia.org/wiki/Internet_Engineering_Task_Force) nor has it gone through the [Request for Comments (RFC)](https://en.wikipedia.org/wiki/Request_for_Comments) process, so it has not been used widely outside a few [implementations](https://dnscrypt.info/implementations). Di conseguenza, è stato ampiamente sostituito dal più popolare [DNS-over-HTTPS](#dns-over-https-doh).

### DNS-over-TLS (DoT)

[**DNS-over-TLS**](https://en.wikipedia.org/wiki/DNS_over_TLS) è un altro metodo per crittografare le comunicazioni DNS, definito in [RFC 7858](https://datatracker.ietf.org/doc/html/rfc7858). Il supporto è stato implementato per la prima volta in Android 9, iOS 14 e su Linux nella versione 237 di [systemd-resolved](https://freedesktop.org/software/systemd/man/resolved.conf.html#DNSOverTLS=). La preferenza nel settore è stata allontanarsi dal DoT al DoH negli ultimi anni, poiché DoT è un [protocollo complesso](https://dnscrypt.info/faq), avente una conformità variabile al RFC tra le implementazioni che esistono. Inoltre, DoT opera su una porta 853 dedicata, facilmente bloccabile dai firewall restrittivi.

### DNS-over-HTTPS (DoH)

[**DNS over HTTPS**](https://en.wikipedia.org/wiki/DNS_over_HTTPS), come definito nell'[RFC 8484](https://datatracker.ietf.org/doc/html/rfc8484), impacchetta le query nel protocollo [HTTP/2](https://en.wikipedia.org/wiki/HTTP/2) e garantisce la sicurezza con HTTPS. Il supporto è stato aggiunto per la prima volta nei browser web come Firefox 60 e Chrome 83.

L'implementazione nativa di DoH è arrivata su iOS 14, macOS 11, Microsoft Windows e Android 13 (tuttavia, non sarà abilitata [di default](https://android-review.googlesource.com/c/platform/packages/modules/DnsResolver/+/1833144)). Il supporto generale per i desktop Linux è in attesa dell'[implementazione](https://github.com/systemd/systemd/issues/8639) di systemd, quindi [è necessario installare un software di terze parti](../dns.md#encrypted-dns-proxies).

### Supporto Nativo del Sistema Operativo

#### Android

Android 9 e successive supportano il 'DNS over TLS'. Le impostazioni si possono trovare in: **Impostazioni** &rarr; **Rete e Internet** &rarr; **DNS Privato**.

#### Dispositivi Apple

Le versioni più recenti di iOS, iPadOS, tvOS e macOS, supportano sia DoT che DoH. Entrambi i protocolli sono supportati nativamente tramite i [profili di configurazione](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) o tramite l'[API delle Impostazioni DNS](https://developer.apple.com/documentation/networkextension/dns_settings).

Dopo l'installazione di un profilo di configurazione o di un'app che utilizza l'API delle Impostazioni DNS, è possibile selezionare la configurazione DNS. Se una VPN è attiva, la risoluzione nel tunnel VPN utilizzerà le impostazioni DNS della VPN e non le impostazioni di sistema.

Apple non fornisce un'interfaccia nativa per la creazione di profili DNS crittografati. [Secure DNS profile creator](https://dns.notjakob.com/tool.html) è uno strumento non ufficiale per creare i propri profili DNS crittografati, tuttavia, non saranno firmati. I profili firmati sono da preferire; la firma convalida l'origine di un profilo e contribuisce a garantire l'integrità. Un'etichetta verde "Verificato" è data ai profili di configurazione firmati. Per ulteriori informazioni sulla firma del codice, consulta [Informazioni sulla firma del codice](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html).

#### Linux

`systemd-resolved`, che molte distribuzioni Linux usano per eseguire le ricerche DNS, non supporta ancora [DoH](https://github.com/systemd/systemd/issues/8639). Se vuoi utilizzare DoH, è necessario installare un proxy come [dnscrypt-proxy](../dns.md#dnscrypt-proxy) e [configurarlo](https://wiki.archlinux.org/title/Dnscrypt-proxy) per intercettare tutte le query DNS dal tuo resolver di sistema e inoltrarle su HTTPS.

## Cosa può vedere una parte esterna?

In questo esempio registreremo cosa si verifica quando effettuiamo una richiesta DoH:

1. Prima di tutto, avvia `tshark`:

    ```bash
    tshark -w /tmp/dns_doh.pcap -f "tcp port https and host 1.1.1.1"
    ```

2. Poii, effettua una richiesta con `curl`:

    ```bash
    curl -vI --doh-url https://1.1.1.1/dns-query https://privacyguides.org
    ```

3. Dopo aver effettuato la richiesta, possiamo interrompere la cattura del pacchetto con <kbd>CTRL</kbd> + <kbd>C</kbd>.

4. Analyze the results in Wireshark:

    ```bash
    wireshark -r /tmp/dns_doh.pcap
    ```

Possiamo vedere la [creazione della connessione](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#Connection_establishment) e l'[handshake TLS](https://cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake) che si verifica con qualsiasi connessione crittografata. Osservando i successivi pacchetti di "dati dell'applicazione", nessuno di essi contiene il dominio richiesto o l'indirizzo IP restituito.

## Perché **non dovrei** utilizzare il DNS crittografato?

Nei luoghi in cui esiste il filtraggio (o censura) di Internet, visitare le risorse proibite potrebbe avere delle conseguenze, che dovresti considerare nel tuo [modello di minaccia](../basics/threat-modeling.md). Noi **non** suggeriamo di utilizzare il DNS crittografato per tale scopo. Utilizza invece [Tor](../advanced/tor-overview.md) o una [VPN](../vpn.md). Se stai utilizzando una VPN, dovresti utilizzare i server DNS della tua VPN. Utilizzando una VPN, stai già affidando loro tutta la tua attività di rete.

Quando effettuiamo una ricerca DNS, generalmente è perché desideriamo accedere a una risorsa. Di seguito, discuteremo di alcuni dei metodi che potrebbero divulgare le tue attività di navigazione, anche utilizzando il DNS crittografato:

### Indirizzo IP

Il metodo più semplice per determinare l'attività di navigazione, potrebbe essere quello di esaminare gli indirizzi IP accessibili ai tuoi dispositivi. Ad esempio, se l'osservatore sa che `privacyguides.org` si trova a `198.98.54.105` e il tuo dispositivo sta richiedendo dei dati da `198.98.54.105`, è molto probabile che tu stia visitando Privacy Guides.

Questo metodo è utile soltanto quando l'indirizzo IP appartiene a un server che ospita soltanto alcuni siti web. It's also not very useful if the site is hosted on a shared platform (e.g. GitHub Pages, Cloudflare Pages, Netlify, WordPress, Blogger, etc.). Inoltre, non è molto utile se il server è ospitato dietro un [proxy inverso](https://en.wikipedia.org/wiki/Reverse_proxy), molto comune sull'Internet moderno.

### Indicazione del Nome del Server (SNI)

Server Name Indication is typically used when an IP address hosts many websites. Potrebbe trattarsi di un servizio come Cloudflare, o di qualche altra protezione dagli [attacchi di Denial-of-service](https://en.wikipedia.org/wiki/Denial-of-service_attack).

1. Riavvia la cattura con `tshark`. We've added a filter with our IP address, so you don't capture many packets:

    ```bash
    tshark -w /tmp/pg.pcap port 443 and host 198.98.54.105
    ```

2. Quindi, visitiamo [https://privacyguides.org](https://privacyguides.org).

3. Dopo aver visitato il sito web, vogliamo interrompere la cattura dei pacchetti con <kbd>CTRL</kbd> + <kbd>C</kbd>.

4. Poi, vogliamo analizzare i risultati:

    ```bash
    wireshark -r /tmp/pg.pcap
    ```

    Vedremo l'instaurazione della connessione, seguita dall'handshake TLS per il sito web di Privacy Guides. Intorno al quadro 5, visualizzerai un "Saluto del Client".

5. Espandi il triangolo &#9656; affianco a ogni campo:

    ```text
    ▸ Transport Layer Security
      ▸ TLSv1.3 Record Layer: Handshake Protocol: Client Hello
        ▸ Handshake Protocol: Client Hello
          ▸ Extension: server_name (len=22)
            ▸ Server Name Indication extension
    ```

6. Possiamo vedere il valore SNI che rivela il sito web che stiamo visitando. Il comando `tshark` può darti direttamente il valore per tutti i pacchetti contenenti un valore SNI:

    ```bash
    tshark -r /tmp/pg.pcap -Tfields -Y tls.handshake.extensions_server_name -e tls.handshake.extensions_server_name
    ```

Ciò significa che, anche se stiamo utilizzando dei server "DNS Crittografati", il dominio sarà probabilmente divulgato tramite SNI. Il protocollo [TLS v1.3](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_1.3) prevede l'[Encrypted Client Hello](https://blog.cloudflare.com/encrypted-client-hello), che impedisce questo tipo di perdita.

I governi, in particolare [Cina](https://zdnet.com/article/china-is-now-blocking-all-encrypted-https-traffic-using-tls-1-3-and-esni) e [Russia](https://zdnet.com/article/russia-wants-to-ban-the-use-of-secure-protocols-such-as-tls-1-3-doh-dot-esni), hanno già [iniziato a bloccarlo](https://en.wikipedia.org/wiki/Server_Name_Indication#Encrypted_Client_Hello) o hanno espresso il desiderio di farlo. Di recente, la Russia ha [iniziato a bloccare i siti web stranieri](https://github.com/net4people/bbs/issues/108), che utilizzano lo standard [HTTP/3](https://en.wikipedia.org/wiki/HTTP/3). Questo perché il protocollo [QUIC](https://en.wikipedia.org/wiki/QUIC), parte di HTTP/3, richiede che anche `ClientHello` sia crittografato.

### Protocollo di Stato del Certificato Online (OCSP)

Un altro modo in cui il tuo browser può divulgare le tue attività di navigazione è con il [Protocollo di Stato del Certificato Online](https://en.wikipedia.org/wiki/Online_Certificate_Status_Protocol). Visitando un sito web HTTPS, il browser potrebbe verificare se il [certificato](https://en.wikipedia.org/wiki/Public_key_certificate) del sito web è stato revocato. Ciò avviene generalmente tramite il protocollo HTTP, a significare che **non** è crittografato.

La richiesta OCSP contiene il "[numero di serie](https://en.wikipedia.org/wiki/Public_key_certificate#Common_fields)" del certificato, che è univoco. Viene inviato al "risponditore OCSP", per poterne verificare lo stato.

Possiamo simulare ciò che un browser farebbe, utilizzando il comando [`openssl`](https://en.wikipedia.org/wiki/OpenSSL).

1. Ottieni il certificato del server e utilizza [`sed`](https://en.wikipedia.org/wiki/Sed) per mantenere soltanto la parte importante e scriverla in un file:

    ```bash
    openssl s_client -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_server.cert
    ```

2. Ottieni il certificato intermedio. Normalmente, le [Autorità di Certificazione (CA)](https://en.wikipedia.org/wiki/Certificate_authority) non firmano direttamente un certificato; utilizzano ciò che è noto come certificato "intermedio".

    ```bash
    openssl s_client -showcerts -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_and_intermediate.cert
    ```

3. Il primo certificato in `pg_and_intermediate-.cert` è in realtà il certificato del server dal passaggio 1. Possiamo riutilizzare `sed` per eliminare fino alla prima istanza di END:

    ```bash
    sed -n '/^-*END CERTIFICATE-*$/!d;:a n;p;ba' \
        /tmp/pg_and_intermediate.cert > /tmp/intermediate_chain.cert
    ```

4. Ottieni il risponditore OCSP per il certificato del server:

    ```bash
    openssl x509 -noout -ocsp_uri -in /tmp/pg_server.cert
    ```

    Il nostro certificato mostra il risponditore del certificato Lets Encrypt. Se desideri visualizzare tutti i dettagli del certificato, puoi utilizzare:

    ```bash
    openssl x509 -text -noout -in /tmp/pg_server.cert
    ```

5. Avvia la cattura dei pacchetti:

    ```bash
    tshark -w /tmp/pg_ocsp.pcap -f "tcp port http"
    ```

6. Effettua la richiesta OCSP:

    ```bash
    openssl ocsp -issuer /tmp/intermediate_chain.cert \
                 -cert /tmp/pg_server.cert \
                 -text \
                 -url http://r3.o.lencr.org
    ```

7. Apri la cattura:

    ```bash
    wireshark -r /tmp/pg_ocsp.pcap
    ```

    Ci saranno due pacchetti con il protocollo "OCSP": una "Richiesta" e una "Risposta". Per la "Richiesta", possiamo visualizzare il "numero di serie" espandendo il triangolo &#9656; affianco a ogni campo:

    ```bash
    ▸ Online Certificate Status Protocol
      ▸ tbsRequest
        ▸ requestList: 1 item
          ▸ Request
            ▸ reqCert
              serialNumber
    ```

    Anche per la "Risposta" possiamo visualizzare il "numero di serie":

    ```bash
    ▸ Online Certificate Status Protocol
      ▸ responseBytes
        ▸ BasicOCSPResponse
          ▸ tbsResponseData
            ▸ responses: 1 item
              ▸ SingleResponse
                ▸ certID
                  serialNumber
    ```

8. Altrimenti, utilizza `tshark` per filtrare i pacchetti per il Numero di Serie:

    ```bash
    tshark -r /tmp/pg_ocsp.pcap -Tfields -Y ocsp.serialNumber -e ocsp.serialNumber
    ```

Se l'osservatore della rete ha il certificato pubblico, disponibile pubblicamente, può abbinare il numero di serie a tale certificato e, dunque, determinare da ciò il sito che stai visitando. Il processo è automatizzabile e può associare gli indirizzi IP ai numeri di serie. Inoltre, puoi verificare i registri di [Trasparenza del Certificato](https://en.wikipedia.org/wiki/Certificate_Transparency) per il numero di serie.

## Dovrei utilizzare il DNS crittografato?

Abbiamo creato questo diagramma di flusso per descrivere quando *dovresti* utilizzare il DNS crittografato:

``` mermaid
graph TB
    Inizio[Inizio] --> anonymous{"Cerchi di<br> essere anonimo?"}
    anonymous --> | Sì | tor(Usa Tor)
    anonymous --> | No | censura{"Vuoi evitare<br> la censura?"}
    censura--> | Sì | vpnOrTor(Usa<br> VPN o Tor)
    censura --> | No | privacy{"Vuoi privacy<br> dall'ISP?"}
    privacy --> | Sì | vpnOrTor
    privacy --> | No | obnoxious{"L'ISP fa<br> reindirizzamenti<br> odiosi?"}
    obnoxious --> | Sì | encryptedDNS(Usa<br> DNS criptato<br> di terze parti)
    obnoxious --> | No | ispDNS{"L'ISP supporta<br> DNS criptato?"}
    ispDNS --> | Sì | useISP(Usa<br> DNS criptato<br> con l'ISP)
    ispDNS --> | No | nothing(Non fare nulla)
```

Encrypted DNS with a third party should only be used to get around redirects and basic [DNS blocking](https://en.wikipedia.org/wiki/DNS_blocking) when you can be sure there won't be any consequences, or you're interested in a provider that does some rudimentary filtering.

[Elenco dei server DNS consigliati](../dns.md ""){.md-button}

## Cosa sono le DNSSEC?

Le [Estensioni di Sicurezza del Sistema di Nome del Dominio](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) (DNSSEC), sono una funzionalità del DNS che autentica le risposte per le ricerche del nome di dominio. Non forniscono protezione della privacy per tali ricerche, ma impediscono ai malintenzionati di manipolare o avvelenare le risposte alle richieste DNS.

In altre parole, le DNSSEC firmano digitalmente i dati, per aiutare ad assicurarne la validità. Per poter garantire una ricerca sicura, la firma si verifica a ogni livello nel processo di ricerca del DNS. Di conseguenza, tutte le risposte dal DNS sono affidabili.

Il processo di firma delle DNSSEC è simile a quello di firma di un documento legale, con una penna; il firmatario utilizza una firma univoca, che nessun altro può creare e un esperto del tribunale può osservare tale firma e verificare che il documento sia stato firmato da una data persona. Queste firme digitali garantiscono che i dati non siano stati manomessi.

Le DNSSEC implementano una politica di firma digitale gerarchica, tra tutti i livelli del DNS. Ad esempio, nel caso di una ricerca di `privacyguides.org`, un server DNS di radice firmerebbe una chiave per il nome del server `.org`, e il nome del server `.org`, dunque, firmerebbe un chiave per quello autoritativo di `privacyguides.org`.

<small>Adattato da [DNS Security Extensions (DNSSEC) overview](https://cloud.google.com/dns/docs/dnssec) di Google e [DNSSEC: An Introduction](https://blog.cloudflare.com/dnssec-an-introduction) di Cloudflare, entrambi con licenza [CC BY 4.0](https://creativecommons.org/licenses/by/4.0).</small>

## Cos'è la minimizzazione dei QNAME?

Un QNAME è un "nome qualificato", ad esempio `discuss.privacyguides.net`. In passato, quando si risolveva un nome di dominio, il resolver DNS chiedeva a ogni server della catena di fornire tutte le informazioni di cui disponeva sulla query completa. Nell'esempio seguente, la richiesta di trovare l'indirizzo IP di `discuss.privacyguides.net` viene richiesta a ogni provider di server DNS:

| Server                   | Domanda fatta                             | Risposta                                         |
| ------------------------ | ----------------------------------------- | ------------------------------------------------ |
| Server root              | Qual è l'IP di discuss.privacyguides.net? | Non lo so, chiedi al server .net...              |
| Il server .net           | Qual è l'IP di discuss.privacyguides.net? | Non lo so, chiedi al server di Privacy Guides... |
| Server di Privacy Guides | Qual è l'IP di discuss.privacyguides.net? | 5.161.195.190!                                   |

Con la "minimizzazione del QNAME", il resolver DNS chiede solo le informazioni necessarie per trovare il server successivo nella catena. In questo esempio, al server root vengono chieste solo le informazioni sufficienti per trovare il nameserver appropriato per il TLD .net e così via, senza conoscere il dominio completo che si sta cercando di visitare:

| Server                   | Domanda fatta                                      | Risposta                               |
| ------------------------ | -------------------------------------------------- | -------------------------------------- |
| Server root              | Qual è il nameserver per .net?                     | *Fornisce il server di .net*           |
| Il server .net           | Qual è il nameserver di privacyguides.net?         | *Fornisce il server di Privacy Guides* |
| Server di Privacy Guides | Qual è il nameserver di discuss.privacyguides.net? | Questo server!                         |
| Server di Privacy Guides | Qual è l'IP di discuss.privacyguides.net?          | 5.161.195.190                          |

Sebbene questo processo possa essere leggermente più inefficiente, in questo esempio né il nameserver root centrale né i nameserver del TLD ricevono mai informazioni sulla query *completa*, riducendo così la quantità di informazioni trasmesse sulle abitudini di navigazione dell'utente. Un'ulteriore descrizione tecnica è definita nel [RFC 7816](https://datatracker.ietf.org/doc/html/rfc7816).

## Cos'è la Sottorete del Client EDNS (ECS)?

La [Sottorete del Client EDNS](https://en.wikipedia.org/wiki/EDNS_Client_Subnet) è un metodo per un risolutore DNS ricorsivo, per specificare una [sotto-rete](https://en.wikipedia.org/wiki/Subnetwork) per l'[host o il client](https://en.wikipedia.org/wiki/Client_(computing)) che sta effettuando la richiesta DNS.

Esiste per "velocizzare" la consegna dei dati, dando al client una risposta appartenente a un server nei suoi pressi, come una [rete di consegna dei contenuti](https://en.wikipedia.org/wiki/Content_delivery_network), spesso utilizzate nello streaming di video e per servire app web in JavaScript.

Questa funzionalità ha un costo in termini di privacy, in quanto comunica al server DNS alcune informazioni sulla posizione del client, in genere la tua rete IP. Ad esempio, se il tuo indirizzo IP è `198.51.100.32`, il provider DNS potrebbe condividere `198.51.100.0/24` con il server autoritativo. Alcuni provider DNS anonimizzano questi dati fornendo un altro indirizzo IP approssimativamente vicino alla tua posizione.

Se hai installato `dig`, puoi verificare se il tuo provider DNS fornisce informazioni EDNS ai server dei nomi DNS con il seguente comando:

```bash
dig +nocmd -t txt o-o.myaddr.l.google.com +nocomments +noall +answer +stats
```

Si noti che questo comando contatterà Google per il test e restituirà il tuo IP e le informazioni sulla subnet del client EDNS. Se desideri testare un altro resolver DNS, è possibile specificare il suo IP, per testare ad esempio `9.9.9.11`:

```bash
dig +nocmd @9.9.9.11 -t txt o-o.myaddr.l.google.com +nocomments +noall +answer +stats
```

Se i risultati includono un secondo record TXT edns0-client-subnet (come mostrato di seguito), il server DNS sta trasmettendo informazioni EDNS. L'IP o la rete mostrata dopo è l'informazione precisa che è stata condivisa con Google dal tuo provider DNS.

```text
o-o.myaddr.l.google.com. 60 IN TXT "198.51.100.32"
o-o.myaddr.l.google.com. 60 IN TXT "edns0-client-subnet 198.51.100.0/24"
;; Query time: 64 msec
;; SERVER: 9.9.9.11#53(9.9.9.11)
;; WHEN: Wed Mar 13 10:23:08 CDT 2024
;; MSG SIZE  rcvd: 130
```
