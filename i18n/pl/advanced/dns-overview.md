---
title: "Przegląd DNS"
icon: material/dns
description: System nazw domen (Domain Name System) to „książka telefoniczna Internetu”, która pomaga przeglądarce znaleźć poszukiwaną stronę internetową.
---

[System nazw domen](https://pl.wikipedia.org/wiki/Domain_Name_System) (*Domain Name System*) to „książka telefoniczna Internetu”. DNS tłumaczy nazwy domen na adresy IP, dzięki czemu przeglądarki i inne usługi mogą ładować zasoby internetowe za pośrednictwem zdecentralizowanej sieci serwerów.

## Czym jest DNS?

Gdy odwiedzasz stronę internetową, zwracany jest adres numeryczny. Na przykład podczas wizyty `privacyguides.org` zwracany jest adres `192.98.54.105`.

DNS istnieje od [początków](https://en.wikipedia.org/wiki/Domain_Name_System#History) istnienia Internetu. Żądania DNS wysyłane do i z serwerów DNS zazwyczaj **nie są** szyfrowane. W warunkach domowych klient otrzymuje serwery od dostawcy usług internetowych za pośrednictwem protokułu [DHCP](https://pl.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol).

Niezaszyfrowane żądania DNS mogą być łatwo **monitorowane** i **modyfikowane** podczas transferu. W niektórych częściach świata dostawcy usług internetowych są zobowiązani do stosowania prymitywnego [filtrowania DNS](https://en.wikipedia.org/wiki/DNS_blocking). Gdy zażądasz adresu IP domeny objętej blokadą, serwer może nie odpowiadać lub zwrócić inny adres IP. Ponieważ protokół DNS nie jest szyfrowany, ISP (lub dowolny operator sieci) może użyć [DPI](https://en.wikipedia.org/wiki/Deep_packet_inspection) do monitorowania żądań. Dostawcy ISP mogą też blokować żądania na podstawie wspólnych cech, niezależnie od używanego serwera DNS.

Poniżej omówiono i przedstawiono samouczek, który pokazuje, co zewnętrzny obserwator może zobaczyć, korzystając ze zwykłego, nieszyfrowanego DNS oraz z [szyfrowanego DNS](#what-is-encrypted-dns).

### Nieszyfrowany DNS

1. Używając [`tshark`](https://wireshark.org/docs/man-pages/tshark.html) (część projektu [Wireshark](https://pl.wikipedia.org/wiki/Wireshark)) możemy monitorować i rejestrować przepływ pakietów sieciowych. To polecenie zapisuje pakiety spełniające określone reguły:

    ```bash
    tshark -w /tmp/dns.pcap udp port 53 and host 1.1.1.1 or host 8.8.8.8
    ```

2. Następnie możemy użyć polecenia [`dig`](https://en.wikipedia.org/wiki/Dig_(command)) (Linux, macOS itp.) lub [`nslookup`](https://en.wikipedia.org/wiki/Nslookup) (Windows), aby wysłać zapytanie DNS do obu serwerów. Oprogramowanie, takie jak przeglądarki, wykonuje te zapytania automatycznie, o ile nie są skonfigurowane do korzystania z szyfrowanego DNS.

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

3. Następnie chcemy [przeanalizować](https://wireshark.org/docs/wsug_html_chunked/ChapterIntroduction.html#ChIntroWhatIs) wyniki:

    === "Wireshark"

        ```
        wireshark -r /tmp/dns.pcap
        ```

    === "tshark"

        ```
        tshark -r /tmp/dns.pcap
        ```

Jeśli uruchomisz powyższe polecenie Wireshark, górny panel pokaże „[ramki](https://en.wikipedia.org/wiki/Ethernet_frame)” (ang. *frames*), a dolny panel wyświetli wszystkie dane dotyczące wybranej ramki. Rozwiązania do filtrowania i monitorowania na poziomie korporacyjnym (takie, które mogą być zakupione przez rządy) potrafią wykonywać ten proces automatycznie, bez interwencji człowieka, oraz agregować te ramki w celu wygenerowania danych statystycznych użytecznych dla obserwatora sieci.

| Nr | Czas     | Źródło    | Adres docelowy | Protokół     | Długość | Informacje                                                             |
| -- | -------- | --------- | -------------- | ------------ | ------- | ---------------------------------------------------------------------- |
| 1  | 0.000000 | 192.0.2.1 | 1.1.1.1        | Wyszukiwarki | 104     | Standard query 0x58ba A privacyguides.org OPT                          |
| 2  | 0.293395 | 1.1.1.1   | 192.0.2.1      | Wyszukiwarki | 108     | Standard query response 0x58ba A privacyguides.org A 198.98.54.105 OPT |
| 3  | 1.682109 | 192.0.2.1 | 8.8.8.8        | Wyszukiwarki | 104     | Standard query 0xf1a9 A privacyguides.org OPT                          |
| 4  | 2.154698 | 8.8.8.8   | 192.0.2.1      | Wyszukiwarki | 108     | Standard query response 0xf1a9 A privacyguides.org A 198.98.54.105 OPT |

Obserwator mógłby zmodyfikować dowolny z tych pakietów.

## Czym jest „szyfrowany DNS”?

Szyfrowany DNS może odnosić się do kilku protokołów — najczęściej do [DNSCrypt](#dnscrypt), [DNS poprzez TLS](#dns-over-tls-dot) oraz [DNS poprzez HTTPS](#dns-over-https-doh).

### DNSCrypt

[**DNSCrypt**](https://en.wikipedia.org/wiki/DNSCrypt) był jedną z pierwszych metod szyfrowania zapytań DNS. DNSCrypt działa na porcie 443 i współpracuje zarówno z protokołami transmisji TCP, jak i UDP. DNSCrypt nigdy nie został zgłoszony do [Internet Engineering Task Force (IETF)](https://en.wikipedia.org/wiki/Internet_Engineering_Task_Force) ani nie przeszedł procesu [Request for Comments (RFC)](https://en.wikipedia.org/wiki/Request_for_Comments), dlatego poza kilkoma [implementacjami](https://dnscrypt.info/implementations) nie był szeroko stosowany. W rezultacie został on w dużej mierze wyparty przez bardziej popularny [DNS poprzez HTTPS](#dns-over-https-doh).

### DNS poprzez TLS (DoT)

[**DNS poprzez TLS**](https://en.wikipedia.org/wiki/DNS_over_TLS) to kolejna metoda szyfrowania komunikacji DNS, zdefiniowana w dokumencie [RFC 7858](https://datatracker.ietf.org/doc/html/rfc7858). Obsługa tej metody została po raz pierwszy zaimplementowana w systemach Android 9, iOS 14 oraz w [systemd-resolved](https://freedesktop.org/software/systemd/man/resolved.conf.html#DNSOverTLS=) na Linuksie w wersji 237. W ostatnich latach preferencje w branży odchodzą od DoT na rzecz DoH — DoT jest [stosunkowo złożonym protokołem](https://dnscrypt.info/faq), a istniejące implementacje różnią się zgodnością z RFC. DoT korzysta też z dedykowanego portu 853, który może być łatwo blokowany przez restrykcyjne zapory sieciowe.

### DNS poprzez HTTPS (DoH)

[**DNS poprzez HTTPS**](https://en.wikipedia.org/wiki/DNS_over_HTTPS), zdefiniowany w dokumencie [RFC 8484](https://datatracker.ietf.org/doc/html/rfc8484), pakuje zapytania w protokole [HTTP/2](https://en.wikipedia.org/wiki/HTTP/2) i zapewnia bezpieczeństwo dzięki HTTPS. Obsługa tej funkcji została po raz pierwszy dodana w przeglądarkach internetowych, takich jak Firefox 60 i Chrome 83.

Natywna implementacja DoH trafiła do systemów iOS 14, macOS 11, Microsoft Windows oraz Android 13 (nie będzie jednak [domyślnie](https://android-review.googlesource.com/c/platform/packages/modules/DnsResolver/+/1833144) włączona). Ogólne wsparcie dla środowisk desktopowych Linuksa oczekuje na [implementację](https://github.com/systemd/systemd/issues/8639) w systemd, więc [nadal wymagana jest instalacja oprogramowania firm trzecich](../dns.md#encrypted-dns-proxies).

### Natywne wsparcie systemów operacyjnych

#### Android

Android 9 i nowsze obsługują DNS poprzez TLS. Ustawienia te można znaleźć w: **Ustawienia** &rarr; **Sieć i internet** &rarr; **Prywatny DNS**.

#### Urządzenia Apple

Najnowsze wersje systemów iOS, iPadOS, tvOS i macOS obsługują zarówno DoT, jak i DoH. Oba protokoły są obsługiwane natywnie za pośrednictwem [profili konfiguracji](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) lub [interfejsu API DNS Settings](https://developer.apple.com/documentation/networkextension/dns_settings).

Po zainstalowaniu profilu konfiguracji lub aplikacji korzystającej z interfejsu API DNS Settings można wybrać konfigurację DNS. Jeśli aktywne jest połączenie VPN, rozwiązywanie nazw w tunelu VPN będzie korzystać z ustawień DNS tej sieci VPN, a nie z ustawień systemowych.

Apple nie udostępnia natywnego interfejsu do tworzenia profili szyfrowanego DNS. [Secure DNS profile creator](https://dns.notjakob.com/tool.html) to nieoficjalne narzędzie do tworzenia własnych profili szyfrowanego DNS, jednak takie profile nie będą podpisane. Preferowane są profile podpisane; podpis potwierdza pochodzenie profilu i pomaga zapewnić jego integralność. Podpisane profile otrzymują zieloną etykietę „Zweryfikowany”. Więcej informacji na temat podpisywania kodu można znaleźć w sekcji [About Code Signing](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html).

#### Linux

`systemd-resolved`, którego używa wiele dystrybucji Linuksa do obsługi zapytań DNS, nie obsługuje jeszcze [DoH](https://github.com/systemd/systemd/issues/8639). Aby korzystać z DoH, należy zainstalować proxy, takie jak [dnscrypt-proxy](../dns.md#dnscrypt-proxy), i [skonfigurować je](https://wiki.archlinux.org/title/Dnscrypt-proxy) tak, aby przejmowało wszystkie zapytania DNS od systemowego resolvera i przekazywało je poprzez HTTPS.

## What can an outside party see?

In this example we will record what happens when we make a DoH request:

1. First, start `tshark`:

    ```bash
    tshark -w /tmp/dns_doh.pcap -f "tcp port https and host 1.1.1.1"
    ```

2. Second, make a request with `curl`:

    ```bash
    curl -vI --doh-url https://1.1.1.1/dns-query https://privacyguides.org
    ```

3. After making the request, we can stop the packet capture with <kbd>CTRL</kbd> + <kbd>C</kbd>.

4. Analyze the results in Wireshark:

    ```bash
    wireshark -r /tmp/dns_doh.pcap
    ```

We can see the [connection establishment](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#Connection_establishment) and [TLS handshake](https://cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake) that occurs with any encrypted connection. When looking at the "application data" packets that follow, none of them contain the domain we requested or the IP address returned.

## Why **shouldn't** I use encrypted DNS?

In locations where there is internet filtering (or censorship), visiting forbidden resources may have its own consequences which you should consider in your [threat model](threat-modeling.md). **Nie zalecamy** używania szyfrowanego DNS w tym celu. Use [Tor](../advanced/tor-overview.md) or a [VPN](../vpn.md) instead. Jeśli korzystasz z sieci VPN, należy użyć serwerów DNS jej dostawcy. When using a VPN, you are already trusting them with all your network activity.

When we do a DNS lookup, it's generally because we want to access a resource. Below, we will discuss some of the methods that may disclose your browsing activities even when using encrypted DNS:

### Adres IP

Najprostszym sposobem na określenie aktywności przeglądania może być sprawdzenie adresów IP, z którymi łączą się Twoje urządzenia. Na przykład, jeśli obserwator wie, że `privacyguides.org` znajduje się pod adresem `198.98.54.105`, a Twoje urządzenie pobiera dane z adresu `198.98.54.105`, istnieje duże prawdopodobieństwo, że odwiedzasz witrynę Privacy Guides.

Ta metoda jest użyteczna tylko wtedy, gdy adres IP należy do serwera, na którym znajduje się tylko kilka stron internetowych. It's also not very useful if the site is hosted on a shared platform (e.g. GitHub Pages, Cloudflare Pages, Netlify, WordPress, Blogger, etc.). It also isn't very useful if the server is hosted behind a [reverse proxy](https://en.wikipedia.org/wiki/Reverse_proxy), which is very common on the modern Internet.

### Server Name Indication (SNI)

Server Name Indication is typically used when an IP address hosts many websites. This could be a service like Cloudflare, or some other [Denial-of-service attack](https://en.wikipedia.org/wiki/Denial-of-service_attack) protection.

1. Start capturing again with `tshark`. We've added a filter with our IP address, so you don't capture many packets:

    ```bash
    tshark -w /tmp/pg.pcap port 443 and host 198.98.54.105
    ```

2. Then we visit [https://privacyguides.org](https://privacyguides.org).

3. After visiting the website, we want to stop the packet capture with <kbd>CTRL</kbd> + <kbd>C</kbd>.

4. Next we want to analyze the results:

    ```bash
    wireshark -r /tmp/pg.pcap
    ```

    We will see the connection establishment, followed by the TLS handshake for the Privacy Guides website. Around frame 5. Around frame 5. you'll see a "Client Hello".

5. Expand the triangle &#9656; next to each field:

    ```text
    ▸ Transport Layer Security
      ▸ TLSv1.3 Record Layer: Handshake Protocol: Client Hello
        ▸ Handshake Protocol: Client Hello
          ▸ Extension: server_name (len=22)
            ▸ Server Name Indication extension
    ```

6. We can see the SNI value which discloses the website we are visiting. The `tshark` command can give you the value directly for all packets containing a SNI value:

    ```bash
    tshark -r /tmp/pg.pcap -Tfields -Y tls.handshake.extensions_server_name -e tls.handshake.extensions_server_name
    ```

This means even if we are using "Encrypted DNS" servers, the domain will likely be disclosed through SNI. The [TLS v1.3](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_1.3) protocol brings with it [Encrypted Client Hello](https://blog.cloudflare.com/encrypted-client-hello), which prevents this kind of leak.

Governments, in particular [China](https://zdnet.com/article/china-is-now-blocking-all-encrypted-https-traffic-using-tls-1-3-and-esni) and [Russia](https://zdnet.com/article/russia-wants-to-ban-the-use-of-secure-protocols-such-as-tls-1-3-doh-dot-esni), have either already [started blocking](https://en.wikipedia.org/wiki/Server_Name_Indication#Encrypted_Client_Hello) it or expressed a desire to do so. Recently, Russia has [started blocking foreign websites](https://github.com/net4people/bbs/issues/108) that use the [HTTP/3](https://en.wikipedia.org/wiki/HTTP/3) standard. This is because the [QUIC](https://en.wikipedia.org/wiki/QUIC) protocol that is a part of HTTP/3 requires that `ClientHello` also be encrypted.

### Online Certificate Status Protocol (OCSP)

Another way your browser can disclose your browsing activities is with the [Online Certificate Status Protocol](https://en.wikipedia.org/wiki/Online_Certificate_Status_Protocol). When visiting an HTTPS website, the browser might check to see if the website's [certificate](https://en.wikipedia.org/wiki/Public_key_certificate) has been revoked. This is generally done through the HTTP protocol, meaning it is **not** encrypted.

The OCSP request contains the certificate "[serial number](https://en.wikipedia.org/wiki/Public_key_certificate#Common_fields)", which is unique. It is sent to the "OCSP responder" in order to check its status.

We can simulate what a browser would do using the [`openssl`](https://en.wikipedia.org/wiki/OpenSSL) command.

1. Get the server certificate and use [`sed`](https://en.wikipedia.org/wiki/Sed) to keep just the important part and write it out to a file:

    ```bash
    openssl s_client -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_server.cert
    ```

2. Get the intermediate certificate. [Certificate Authorities (CA)](https://en.wikipedia.org/wiki/Certificate_authority) normally don't sign a certificate directly; they use what is known as an "intermediate" certificate.

    ```bash
    openssl s_client -showcerts -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_and_intermediate.cert
    ```

3. The first certificate in `pg_and_intermediate.cert` is actually the server certificate from step 1. We can use `sed` again to delete until the first instance of END:

    ```bash
    sed -n '/^-*END CERTIFICATE-*$/!d;:a n;p;ba' \
        /tmp/pg_and_intermediate.cert > /tmp/intermediate_chain.cert
    ```

4. Get the OCSP responder for the server certificate:

    ```bash
    openssl x509 -noout -ocsp_uri -in /tmp/pg_server.cert
    ```

    Our certificate shows the Lets Encrypt certificate responder. If we want to see all the details of the certificate we can use:

    ```bash
    openssl x509 -text -noout -in /tmp/pg_server.cert
    ```

5. Start the packet capture:

    ```bash
    tshark -w /tmp/pg_ocsp.pcap -f "tcp port http"
    ```

6. Make the OCSP request:

    ```bash
    openssl ocsp -issuer /tmp/intermediate_chain.cert \
                 -cert /tmp/pg_server.cert \
                 -text \
                 -url http://r3.o.lencr.org
    ```

7. Open the capture:

    ```bash
    wireshark -r /tmp/pg_ocsp.pcap
    ```

    There will be two packets with the "OCSP" protocol: a "Request" and a "Response". For the "Request" we can see the "serial number" by expanding the triangle &#9656; next to each field:

    ```bash
    ▸ Online Certificate Status Protocol
      ▸ tbsRequest
        ▸ requestList: 1 item
          ▸ Request
            ▸ reqCert
              serialNumber
    ```

    For the "Response" we can also see the "serial number":

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

8. Or use `tshark` to filter the packets for the Serial Number:

    ```bash
    tshark -r /tmp/pg_ocsp.pcap -Tfields -Y ocsp.serialNumber -e ocsp.serialNumber
    ```

If the network observer has the public certificate, which is publicly available, they can match the serial number with that certificate and therefore determine the site you're visiting from that. The process can be automated and can associate IP addresses with serial numbers. It is also possible to check [Certificate Transparency](https://en.wikipedia.org/wiki/Certificate_Transparency) logs for the serial number.

## Should I use encrypted DNS?

We made this flow chart to describe when you *should* use encrypted DNS:

``` mermaid
graph TB
    Start[Start] --> anonymous{Trying to be<br> anonymous?}
    anonymous--> | Yes | tor(Use Tor)
    anonymous --> | No | censorship{Avoiding<br> censorship?}
    censorship --> | Yes | vpnOrTor(Use<br> VPN or Tor)
    censorship --> | No | privacy{Want privacy<br> from ISP?}
    privacy --> | Yes | vpnOrTor
    privacy --> | No | obnoxious{ISP makes<br> obnoxious<br> redirects?}
    obnoxious --> | Yes | encryptedDNS(Use<br> encrypted DNS<br> with 3rd party)
    obnoxious --> | No | ispDNS{Does ISP support<br> encrypted DNS?}
    ispDNS --> | Yes | useISP(Use<br> encrypted DNS<br> with ISP)
    ispDNS --> | No | nothing(Do nothing)
```

Encrypted DNS with a third party should only be used to get around redirects and basic [DNS blocking](https://en.wikipedia.org/wiki/DNS_blocking) when you can be sure there won't be any consequences, or you're interested in a provider that does some rudimentary filtering.

[Lista polecanych serwerów DNS](../dns.md ""){.md-button}

## Co to jest DNSSEC?

[Domain Name System Security Extensions](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) (DNSSEC) to funkcja DNS uwierzytelniająca odpowiedzi na zapytania o nazwę domen. Nie zapewnia ona ochrony prywatności tych zapytań, ale uniemożliwia atakującym manipulowanie lub zatruwanie odpowiedzi na zapytania DNS.

Innymi słowy, DNSSEC podpisuje cyfrowo dane, aby zapewnić ich spójność. W celu zapewnienia bezpiecznego wyszukiwania, podpisywanie odbywa się na każdym poziomie procesu zapytania DNS. Dzięki temu wszystkie odpowiedzi z DNS są zaufane.

Proces podpisywania DNSSEC jest podobny do podpisywania dokumentu prawnego długopisem; osoba składająca podpis używa niepowtarzalnego podpisu, a ekspert sądowy może spojrzeć na ten podpis i zweryfikować, czy dokument został podpisany przez tę osobę. Te podpisy cyfrowe są gwarancją, że dane nie zostały naruszone.

DNSSEC wprowadza hierarchiczną politykę podpisywania cyfrowego we wszystkich warstwach DNS. For example, in the case of a `privacyguides.org` lookup, a root DNS server would sign a key for the `.org` nameserver, and the `.org` nameserver would then sign a key for `privacyguides.org`’s authoritative nameserver.

<small>Adapted from [DNS Security Extensions (DNSSEC) overview](https://cloud.google.com/dns/docs/dnssec) by Google and [DNSSEC: An Introduction](https://blog.cloudflare.com/dnssec-an-introduction) by Cloudflare, both licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0).</small>

## What is QNAME minimization?

A QNAME is a "qualified name", for example `discuss.privacyguides.net`. In the past, when resolving a domain name your DNS resolver would ask every server in the chain to provide any information it has about your full query. In this example below, your request to find the IP address for `discuss.privacyguides.net` gets asked of every DNS server provider:

| Server                 | Question Asked                              | Response                                    |
| ---------------------- | ------------------------------------------- | ------------------------------------------- |
| Root server            | What's the IP of discuss.privacyguides.net? | I don't know, ask .net's server...          |
| .net's server          | What's the IP of discuss.privacyguides.net? | I don't know, ask Privacy Guides' server... |
| Privacy Guides' server | What's the IP of discuss.privacyguides.net? | 5.161.195.190!                              |

With "QNAME minimization," your DNS resolver now only asks for just enough information to find the next server in the chain. In this example, the root server is only asked for enough information to find the appropriate nameserver for the .net TLD, and so on, without ever knowing the full domain you're trying to visit:

| Server                 | Question Asked                                       | Response                          |
| ---------------------- | ---------------------------------------------------- | --------------------------------- |
| Root server            | What's the nameserver for .net?                      | *Provides .net's server*          |
| .net's server          | What's the nameserver for privacyguides.net?         | *Provides Privacy Guides' server* |
| Privacy Guides' server | What's the nameserver for discuss.privacyguides.net? | This server!                      |
| Privacy Guides' server | What's the IP of discuss.privacyguides.net?          | 5.161.195.190                     |

While this process can be slightly more inefficient, in this example neither the central root nameservers nor the TLD's nameservers ever receive information about your *full* query, thus reducing the amount of information being transmitted about your browsing habits. Further technical description is defined in [RFC 7816](https://datatracker.ietf.org/doc/html/rfc7816).

## What is EDNS Client Subnet (ECS)?

The [EDNS Client Subnet](https://en.wikipedia.org/wiki/EDNS_Client_Subnet) is a method for a recursive DNS resolver to specify a [subnetwork](https://en.wikipedia.org/wiki/Subnetwork) for the [host or client](https://en.wikipedia.org/wiki/Client_(computing)) which is making the DNS query.

It's intended to "speed up" delivery of data by giving the client an answer that belongs to a server that is close to them such as a [content delivery network](https://en.wikipedia.org/wiki/Content_delivery_network), which are often used in video streaming and serving JavaScript web apps.

This feature does come at a privacy cost, as it tells the DNS server some information about the client's location, generally your IP network. For example, if your IP address is `198.51.100.32` the DNS provider might share `198.51.100.0/24` with the authoritative server. Some DNS providers anonymize this data by providing another IP address which is approximately near your location.

If you have `dig` installed you can test whether your DNS provider gives EDNS information out to DNS nameservers with the following command:

```bash
dig +nocmd -t txt o-o.myaddr.l.google.com +nocomments +noall +answer +stats
```

Note that this command will contact Google for the test, and return your IP as well as EDNS client subnet information. If you want to test another DNS resolver you can specify their IP, to test `9.9.9.11` for example:

```bash
dig +nocmd @9.9.9.11 -t txt o-o.myaddr.l.google.com +nocomments +noall +answer +stats
```

If the results include a second edns0-client-subnet TXT record (like shown below), then your DNS server is passing along EDNS information. The IP or network shown after is the precise information which was shared with Google by your DNS provider.

```text
o-o.myaddr.l.google.com. 60 IN TXT "198.51.100.32"
o-o.myaddr.l.google.com. 60 IN TXT "edns0-client-subnet 198.51.100.0/24"
;; Query time: 64 msec
;; SERVER: 9.9.9.11#53(9.9.9.11)
;; WHEN: Wed Mar 13 10:23:08 CDT 2024
;; MSG SIZE  rcvd: 130
```
